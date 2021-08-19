---
title: Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma
description: Bu konu, katıştırılmış resim ve şekillere sahip iş belgeleri oluşturmak için Elektronik raporlama aracını kullanmayı açıklamaktadır.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 550ecca31af48e624e292b342d909abd6eb3e87af122f736eb388524b42f1e05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730647"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) aracını, gerekli elektronik belgeleri oluşturmak için çalıştırabileceğiniz raporlar tasarlamak amacıyla kullanabilirsiniz. Bir raporun düzenini belirtmek için, Microsoft Excel veya Microsoft Word belgelerini kullanabilirsiniz. ER İşlemleri tasarımcısı, rapor için bir Excel veya Word belgesi eklemenize olanak tanır. Ekli şablondaki adlandırılmış öğeler, ER raporunun biçim öğeleriyle ilişkilendirilmiştir: Raporun biçim öğeleri veri kaynaklarına bağlıdır. Bu öğeler çalışma zamanında oluşturulan belgelere girilecek verileri belirtir.

Bu yeni işlev, Microsoft Office biçimlerdeki belgeleri oluşturmak için mevcut ER yeteneklerinin ötesine geçer. Daha fazla bilgi edinmek için aşağıdaki görev kılavuzlarını yürütün. Bu görev kılavuzlarını, 7.5.4.3 BT hizmeti/çözümü bileşenleri Al/Geliştir (10677) iş süreci altında bulabilirsiniz.

- ER OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama
- ER Microsoft WORD biçiminde raporlar oluşturmak için yapılandırma tasarlama

## <a name="embed-an-image-in-an-excel-document"></a>Excel belgesine resim katıştırma

### <a name="embed-an-image-in-an-excel-worksheet"></a>Excel çalışma sayfasına resim katıştırma

İlk olarak, Excel belgesinde resim için bir yer tutucu eklemeniz gerekir. Excel çalışma kitabı açın ve daha sonra ekleyebileceğiniz görüntü için yer tutucu olarak bir resim ekleyin. Daha sonra, tasarlamakta olduğunuz raporu dahil etmek üzere yeni bir ER biçimi yapılandırması eklemek için ER aracını kullanın. Excel çalışma kitabını raporun biçimi için şablon olarak ekleyin ve sonra çalışma kitabının içeriğini ER biçimine aktarın. Biçim tanımı otomatik olarak oluşturulur. Eklediğiniz resim yer tutucusu, ER biçimi tanımına bir **HÜCRE** öğesi olarak eklenecektir.

> [!NOTE]
> Biçim tanımını içe aktarmak yerine el ile belirtebilirsiniz. Değişikliklerinizi kaydettiğinizde, biçim doğrulanır.

Sonra, ER biçiminin **HÜCRE** öğesini, çalışma zamanında resmin verilerini ikili biçimde sağlayan biçimin veri kaynağından alınan alana bağlayın. ER veri modeli biçimin veri kaynağı olarak kullanıldığında, alanın veri türü [Kapsayıcı](er-formula-supported-data-types-composite.md#container) olmalıdır. Şu anda, [Kapsayıcı](er-formula-supported-data-types-composite.md#container) veri türüne sahip bir ER veri modeli alanı görüntüleri ikili biçiminde döndüren çeşitli veri kaynağı türüne bağlı olabilir. Belge yönetimi çerçevesini kullanarak, veri tablosundaki bir alana ve veri tablosunun kaydına iliştirilmiş bir dosyaya erişebilirsiniz.

> [!IMPORTANT]
> - Excel şablonunu kullanarak oluşturduğunuz belgede resim yer tutucusunu doldurmak istiyorsanız, ER biçimi Excel şablonundaki adlandırılmış resim öğesine başvuran **HÜCRE** öğesini içermelidir. Aksi durumda, raporun çıktısında hiçbir resim yer tutucusu görünmez. **HÜCRE** öğesinin bağlaması çalışma zamanında veri döndürmezse, oluşturulan belge şablondaki görüntü yer tutucusunu gösterecektir. Oluşturduğunuz belgedeki bir görüntüyü gizlemek için bir **HÜCRE** öğesi tanımlayın ve **Etkinleştirme** ifadesinin **YANLIŞ** değeri döndürmesi gerektiğini belirtin.
> - Excel şablonunda, her öğe için benzersiz bir ad kullanın. Bu öğeler resimleri ve hücreleri içerir. Bir öğe adını çoğalttığınızda, oluşturulan raporun içeriği belirsiz ve kafa karıştırıcı olacaktır.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Excel çalışma sayfasının üst bilgisine ve alt bilgisine resim katıştırma

Raporun düzenini belirtmek için Excel çalışma kitabı belgesini şablon olarak kullanın. Çalışma kitabı, her biri bir üst bilgi ve alt bilgi içerecek şekilde tasarlanabilen birden çok çalışma sayfası içerebilir. Excel, her çalışma sayfasının üst bilgi ve alt bilgisinde en fazla üç görüntüyü destekler. Görüntüler sola, sağa veya ortaya hizalanabilir.

Finans sürüm 10.0.21'de, Excel şablonu bulunan bir ER çözümü tarafından oluşturulan üst bilgi ve alt bilgi resimlerini yönetebilirsiniz.

Oluşturulan bir belgenin üst bilgisinde veya alt bilgisinde varsayılan bir resmin görünmesini istiyorsanız, bir ER şablonunun çalışma sayfasının üst bilgisine veya alt bilgisine resim ekleyebilirsiniz. Bu görüntüye ER biçiminizde erişmek için, **Resim** bileşenini biçimin [Üst bilgi](er-fillable-excel.md#header-component) veya [Alt bilgi](er-fillable-excel.md#footer-component) bileşeninin altına eklemeniz gerekir. **Resim** bileşeninin hizalamasını uygun şekilde yapılandırın. 

Ayrıca, şablon varsayılan görüntü içermese bile çalışma zamanında oluşturulan bir belgenin üst bilgisine veya alt bilgisine resim yerleştirmek için **Resim** bileşenini de kullanabilirsiniz. Oluşturulan bir belgenin üst bilgisine veya alt bilgisine, yeni bir görüntü olarak veya varsayılan bir görüntünün yerine eklenecek ortam içeriğini belirtmek için, **Resim** bileşenini bir görüntüyü ikili biçimde temsil eden [Kapsayıcı](er-formula-supported-data-types-composite.md#container) türündeki bir veri kaynağına bağlamanız gerekir.

Her **Üst bilgi** veya **Alt bilgi** bileşeni desteklenen her hizalama için tek bir **resim** bileşeni içerebilir: **Sol**, **Orta** ve **Sağ**.

**Resim** bileşeninin özelliği **Yüksekliği ölçeklendir** özelliği bir görüntünün boyutunu kontrol etmek için yapılandırılmış bağlamayı kullanmanızı sağlar:

- Görüntünün başlangıç boyutunu korumak için **Orijinal**'i seçin.
- Görüntünün yüksekliğini, o görüntüyü tutan üst bilgi veya alt bilginin yüksekliğiyle orantılı olarak ölçeklemek için **Göreli**'yi seçin.

    - Bu durumda, görüntünün yüksekliği üst başlık veya alt bilginin yüzdesi olarak tanımlanmalıdır.
    - Ölçekleme değeri yüzde 100'ü aşarsa, görüntü ilgili çalışma sayfasının veri alanıyla çakışabilir.
    - Ölçekleme uygulandığında görüntünün yüksekliği değiştirilirse, görüntünün özgün en boy oranını korumak için Genişlik de değiştirilir.

- Görüntüyü tasarım zamanında sağlanan yükseklik ve genişlik değerlerine (piksel olarak) göre yeniden boyutlandırmak için, **Mutlak**'ı seçin.

    - Belirtilen yükseklik ana üst bilgi veya alt bilginin yüksekliğini aşıyorsa, görüntü ilgili çalışma sayfasının veri alanıyla çakışabilir.

Bu bileşeni kullanarak oluşturulan bir belgeye eklenen bir görüntünün görünürlüğünü denetlemek için **Resim** bileşeninin **Etkin** özelliğini de kullanabilirsiniz.

> [!NOTE]
> Düzenlenebilir ER biçimine bir **Resim** bileşeni eklemek için ER biçim tasarımcısını kullanmanız gerekir. İş belgesinin şablonunu düzenlemek için [İş belgeleri yönetimi](er-business-document-management.md) çalışma alanını kullandığınızda bileşeni ekleyemezsiniz.

Bu işlev hakkında daha fazla bilgi edinmek için, [Sayfa üst bilgilerinde veya alt bilgilerinde katıştırılmış görüntüler içeren Excel biçiminde bir rapor oluşturmak üzere bir ER biçimi tasarlama](er-embed-images-header-footer-excel-reports.md) adımlarını izleyin.

## <a name="embed-a-shape-in-an-excel-document"></a>Excel belgesine şekil katıştırma

İlk olarak, Excel belgesinde şekil için bir yer tutucu eklemeniz gerekir. Bir Excel çalışma kitabı açın ve **Şekil**, **Metin kutusu** veya **WordArt**'ı şeklin yer tutucusu olarak seçin. Daha sonra, tasarlamakta olduğunuz raporu dahil etmek üzere yeni bir ER biçimi yapılandırması eklemek için ER aracını kullanın. Excel çalışma kitabını raporun biçimi için şablon olarak ekleyin ve sonra çalışma kitabının içeriğini ER biçimine aktarın. Biçim tanımı otomatik olarak oluşturulur. Eklediğiniz şekil yer tutucusu, bu adlandırılmış Excel şekil öğesine başvuran bir **HÜCRE** öğesi olarak ER biçim tanımına eklenecektir.

> [!NOTE]
> Biçim tanımını içe aktarmak yerine el ile belirtebilirsiniz. Değişikliklerinizi kaydettiğinizde, biçim doğrulanır.

Sonra, ER biçiminin **HÜCRE** öğesini, çalışma zamanında veri sağlayan biçimin veri kaynağından alınan alana bağlayın. Bu veriler bir metin dizesine dönüştürülebilir. ER biçimindeki **HÜCRE** öğesi metni destekleyen Excel şablonundaki bir şekil öğesine başvurduğunda, çalışma zamanında bu bağlama aracılığıyla sağlanan metin oluşturulan belgede bir şekil içinde gösterilir.

> [!IMPORTANT]
> - Yeni bir belge oluşturmak için şekil yer tutucusunu içeren Excel şablonunu kullanmak istiyorsanız, ER biçimi Excel şekil öğesine başvuran bir **HÜCRE** öğesi içermelidir. Aksi durumda, raporun çıktısında hiçbir şekil yer tutucusu görünmez. Adlandırılmış Excel şekil öğesine başvuran bir **HÜCRE** öğesinin bağlaması çalışma zamanında hiçbir veri döndürmezse, oluşturulan belge Excel şablonundaki şekil yer tutucunun metnini gösterir. Oluşturduğunuz belgedeki bir şekli gizlemek için bir adlandırılan Excel şekil öğesine başvuran bir **HÜCRE** öğesi tanımlayın ve **Etkinleştirme** ifadesinin **YANLIŞ** değeri döndürmesi gerektiğini belirtin.
> - Excel şablonunda, her öğe için benzersiz bir ad kullanın. Bu öğeler şekilleri ve hücreleri içerir. Bir öğe adını çoğalttığınızda, oluşturulan raporun içeriği belirsiz ve kafa karıştırıcı olacaktır.

## <a name="embed-an-image-in-a-word-document"></a>Word belgesine resim katıştırma
> [!IMPORTANT]
> Katıştırılmış görüntüler içeren belgeler oluşturmak için Excel şablonu kullanan ER biçimini yeniden kullanabilirsiniz. ER biçiminde, Excel'deki adlandırılmış bir resim öğesine başvuran ve çalışma zamanında resim döndüren bir veri kaynağına bağlı olan **HÜCRE** öğesi için bir ad belirtildiğinden emin olun.

Önce, Word belgesinin düzenini yapılandırmalısınız. Katıştırılmış resim için yer tutucu oluşturmak üzere **Resim İçeriği** denetimini kullanın. Bu denetime erişmek için, ilk olarak **Geliştirici** sekmesini Word şeridinde görünür yapmalısınız.

Sonra, Excel şablonunu ER biçiminden silin ve Word şablon belgesini iliştirin. Şablon başvurusunu güncelleştirin ve yaptığınız değişiklikleri kaydedin. Geçerli ER biçiminin yapısı, Word şablonuna **Rapor** adında yeni bir özel XML bölümü olarak eklenir.

Sonra, geçerli ER biçimi için Word şablonunu yerel bilgisayarınıza kaydedin. Şablonu açın ve **XML Eşleme** bölmesini açın. **Rapor** adlı özel XML bölümünü bulun ve ardından ikili biçimde bir görüntü döndüren bir veri kaynağına bağlı olan ER raporu içindeki **HÜCRE** öğesine yönlendirin. Bu XML parçasının öğesini seçili **Resim İçeriği** denetimine eşleyin ve değişikliklerinizi kaydedin.

[![görüntüleri katıştırma.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Son olarak, Word şablonunu ER biçiminden silin ve eşlenen özel XML parçalarını içeren Word belgesini iliştirin. Şablona yapılan biçim başvurusunu güncelleştirin ve bu ER biçiminde yaptığınız değişiklikleri kaydedin.

## <a name="more-information"></a>Daha fazla bilgi
Bu özelliğin ayrıntıları hakkında bilgi sahibi olmak için, görev kılavuzları kümesini yürütün, **ER Katıştırılmış görüntüler içeren MS Office biçimlerinde raporlar yapma**. Bu görev kılavuzları, Excel ve Word belgelerinde ER Aracı kullanılarak oluşturulan ödeme çeklerine şirket logosu ve yetkili kişi imzasının görüntülerini nasıl katıştırabileceğinizi gösterir.

Aşağıdaki tabloda, **ER Katıştırılmış görüntüler içeren MS Office biçimlerinde raporlar yapma** görev kılavuzlarını tamamlamak için gereken dosyalar listelenmektedir. Dosyaları indirin ve yerel bilgisayarınıza kaydedin.

| Tanım                                          | Dosya adı                   |
|------------------------------------------------------|-----------------------------|
| ER data model configuration                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER format configuration                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Şirket logosu resmi                                   | [Şirket logosu.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| İmza resmi                                      | [İmza resmi.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternatif imza resmi                          | [İmza resmi 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Ödeme çeklerini yazdırmak için Microsoft Word şablonu  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Ödeme çeklerini yazdırmak için Microsoft Excel şablonu | [Cheque template.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

Aşağıdaki grafik Excel şablonundan oluşturulan bir ödeme çeki için test çıktısı örneği sağlar.

[![Ödeme çeki test çıktısı.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
