---
title: Oluşturulan belgeler için özel depolama konumu belirtin
description: Bu konu, Elektronik raporlama (ER) biçimlerinin oluşturduğu belgeler için depolama konumlarının listesini genişletmeyi açıklar.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 98c08ae2ab4c7cceadb6caaf98fa431e56be4b97
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042746"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Oluşturulan belgeler için özel depolama konumu belirtin

[!include[banner](../includes/banner.md)]

Elektronik raporlama (ER) çerçevesinin Uygulama programlama arabirimi (API), ER biçimlerinin oluşturduğu depolama konumlarını genişletmenize olanak sağlar. Bu konu, özel bir depolama konumu eklemek için tamamlamanız gereken ana görevlerin genel bakışını içerir.

## <a name="prerequisites"></a>Önkoşullar

Sürekli yapılandırma destekleyen bir topoloji dağıtmanız gerekir. (Daha fazla bilgi için bkz. [Sürekli yapılandırma ve test otomasyonu destekleyen topolojiler dağıtın](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Bu topolojiye aşağıdaki rollerden biriyle erişiminiz olması gerekir:

- Elektronik raporlama geliştirici
- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

Bu topoloji için geliştirme ortamına da erişiminiz olması gerekir.

## <a name="create-or-import-an-er-format-configuration"></a>Bir ER biçimi yapılandırması oluşturun veya içe aktarın

Geçerli topolojide [yeni bir ER biçimi oluşturun](tasks/er-format-configuration-2016-11.md) bu sayede bir özel depolama konumu ekleyebileceğiniz belgeler oluşturabilirsiniz. Alternatif olarak [bu topolojiye mevcut bir ER biçimi içe aktarın](general-electronic-reporting-manage-configuration-lifecycle.md).

![Biçim tasarımcısı sayfası](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Oluşturduğunuz veya içe aktardığınız ER biçimi, aşağıdaki biçim öğelerinden en az birini içermelidir:
>
> - Dosya
> - Klasör
> - Birleştirici
> - Ek

## <a name="create-a-new-document-type"></a>Yeni bir belge tipi oluşturma

Bir ER biçiminin oluşturduğu belgelerin nasıl yönlendirileceğini belirtmek için [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md) yapılandırmanız gerekir. Oluşturulan belgeleri dosyalar olarak depolamak için yapılandırılmış her ER hedefinde, Belge yönetimi çerçevesinin belge türünü belirtmeniz gerekir. Farklı belge türleri farklı ER biçimlerinin oluşturduğu belgeleri yönlendirmekte kullanılabilir.

1. Daha önceden oluşturduğunuz veya içe aktardığınız ER biçimi için yeni bir [belge türü](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management) ekleyin. Aşağıdaki örnekte, belge türü **FileX**'tir.
2. Bu belge türünü diğer belge türlerinden ayırt etmek için adında belirli bir anahtar kelime dahil edin. Örneğin, aşağıdaki görselde, adı **(LOCAL) folder**'dır.
3. **Sınıf** alanında, **Dosya ekle** belirtin.
4. **Grup** alanında, **Dosya** belirtin.

![Belge türleri sayfası](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Belge türleri şirkete özeldir. Yapılandırılan hedefle ER biçimini birden fazla şirkette kullanmak için her bir şirkette ayrı bir belge türü yapılandırmalısınız.

## <a name="review-source-code"></a>Kaynak kod gözden geçirme

**ERDocuManagement** sınıfının **insertFile()** yönteminin kodunu gözden geçirin. **AttachingFile()** olayının, oluşturulan dosya bir kayda eklendiğinde oluştuğunu unutmayın.


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

**AttachingFile()** olayı aşağıdaki ER hedefleri işlendiğinde gerçekleşir:

- **Arşiv** – Bu hedef kullanıldığında ERFormatMappingRunJobTable tablosunda oluşturulan ER biçimi için yeni bir kayıt çalıştırılır. Bu kayıttaki **Arşiv** alanı **Hatalı**'dır. ER biçimi başarıyla çalışırsa, oluşturulan belge bu kayda eklenir ve **AttachingFile()** olayı oluşturulur. Bu ER hedefinde seçilen belge türü, eklenen dosyanın depolama konumunu belirle (Microsoft Azure Depolama veya bir Microsoft SharePoint klasörü).
- **İş arşivi** – Bu hedef kullanıldığında ERFormatMappingRunJobTable tablosunda oluşturulan ER formunda için yeni bir kayıt çalıştırılır. Bu kayıttaki **Arşiv** alanı **Doğru**'dır. ER biçimi başarıyla çalışırsa, oluşturulan belge bu kayda eklenir ve **AttachingFile()** olayı oluşturulur. ER parametrelerinde yapılandırılan belge türü, iliştirilen dosya için depolama konumunu belirler (Azure Depolama veya bir SharePoint klasörü).

![Elektronik raporlama parametreleri sayfası](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Bir ER hedefini yapılandırma

1. Oluşturduğunuz veya içe aktardığınız ER biçiminin önceden belirtilen öğelerden biri için (dosya, klasörü, birleştirme veya ek) arşivlenen hedefleri yapılandırın. Yönergeler için bkz. [ER Yapılandır hedefler](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Yapılandırılan hedef için daha önce eklediğiniz belge türünü kullanın. (Bu konudaki örnek için, belge türü **FileX**'tir.)

![Hedef ayarları iletişim kutusu](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Kaynak kodu değiştir

1. Microsoft Visual Studio projenize yeni bir sınıf ekleyin ve daha önceden belirtilen **AttachingFile()** etkinliğine abone olmak için kodu yazın. (Kullanılan genişletilebilirlik modeli hakkında daha fazla bilgi için bkz. [EventHandlerResult kullanarak yanıtla](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Örneğin, yeni sınıfta, aşağıdaki eylemleri gerçekleştiren kodu yazın:

    1. Oluşturulan dosyaları, Application Object Server (AOS) servisini çalıştıran sunucunun yerel dosya sisteminin bir klasöründe depolayın.
    2. Bu oluşturulan dosyaları yalnızca yeni belge türü (örneğin, adında "(LOCAL)" anahtar kelimesini içeren **FileX** türü) kullanıldığında, bir dosya ER çalıştırma iş günlüğünün kaydına eklendiğinde.

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. Projenizi yeniden inşa edin.

## <a name="run-the-er-format-that-you-created-or-imported"></a>Oluşturduğunuz veya içe aktardığınız ER biçimini yürütün

1. Oluşturduğunuz veya içe aktardığınız ER biçimini çalıştırın.
2. **Organizasyon yönetimi \> Elektronik raporlama \> Elektronik raporlama işleri**'ne gidin. Bu yürütme işi için oluşturulan ve oluşturulan dosyanın eklenmiş olduğu kaydı bulun.
3. Oluşturulan aynı dosyayı bulmak için yerel **C:\\0** klasörünü gezin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)
- [Genişletilebilirlik giriş sayfası](../extensibility/extensibility-home-page.md)
