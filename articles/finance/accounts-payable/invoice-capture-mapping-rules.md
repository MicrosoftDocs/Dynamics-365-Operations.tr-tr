---
title: Invoice Capture çözümü eşleme kuralları
description: Bu makalede, Invoice Capture çözümünde eşleme kurallarını ayarlama hakkında bilgi verilmektedir.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691249"
---
# <a name="invoice-capture-solution-mapping-rules"></a>Invoice Capture çözümü eşleme kuralları

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Eşleme kuralları temel ana verileri Microsoft Dynamics 365 Finance veya kurumsal kaynak planlama (ERP) sisteminden getirir. Eşleme kuralları ayarlandıktan sonra, Finance'te satıcı faturası oluşturmak için gereken bilgiler türetilir. Eşleme kuralları kullanılırken, Borç hesapları memuru eksik alanlardaki değerleri el ile doldurmak yerine durumu denetler.

Dört tür eşleme kuralı vardır:

- Tüzel kişilik
- Satıcı hesabı
- Öğe
- Gider türü

## <a name="manage-mapping-rules-by-using-the-app"></a>Eşleme kurallarını uygulamayı kullanarak yönetme

Eşleme kurallarını uygulamayı kullanarak yönetmek için **Kurulum**'u seçin. **Eşleme kuralı kurulumu** sekmesinde dört seçenek sunulur:

- Tüzel kişilik 
- Satıcı hesabı 
- Madde eşlemesi 
- Gider türü

Örneğin, **Tüzel kişilik eşleme kuralları** seçeneğini belirlediniz. Tüzel kişilik kodu şirket adı, adresi ve vergi sicil numarası kullanılarak tanımlanır. **LE-USPM** adlı bir kural için, şirket adı "Contoso Robotics USA" metnini içeriyorsa, tüzel kişilik kodu **USPM** olur.

Sayfada tüm etkin eşleme kuralları gösterilir. Etkin olmayan eşleme kurallarını görüntülemek için **Etkin eşleme tüzel kişilik kuralları**'nı, ardından **Etkin olmayan eşleme tüzel kişilik kuralları**'nı seçin.

Eşleme kuralları için aşağıdaki eylemler kullanılabilir.

### <a name="create-a-mapping-rule"></a>Eşleme kuralı oluşturma

Eşleme kuralı oluşturmak için kullanabileceğiniz iki yöntem vardır:

- Yeni bir eşleme kuralı oluşturmak için **Yeni**'yi seçin. Ardından eşleme kuralının bilgilerini girin. **Kural Adı** değeri her eşleme kuralı türü için benzersiz olmalıdır.
- Varolan bir eşleme kuralını seçerseniz, **Kopyala** düğmesi etkin hale gelir. Bu düğmeyi seçip açılan iletişim kutusundan **Tamam** seçeneğini belirleyin. Seçili kural çoğaltılarak bir eşleme kuralı oluşturulur.

### <a name="edit-a-mapping-rule"></a>Eşleme kuralını düzenleme

Eşleme kuralını düzenlemek için bir alan seçip alanın değerini değiştirin.

### <a name="activatedeactivate-mapping-rules"></a>Eşleme kurallarını etkinleştirme/devre dışı bırakma

Bir veya daha fazla eşleme kuralını devre dışı bırakmak için **Etkin eşleme kuralları** sayfasından bu kuralları işaretleyip **Devre dışı bırak**'ı seçin. Kurallar **Etkin eşleme kuralları** sayfasından **Etkin olmayan eşleme kuralları** sayfasına taşınır.

Aynı şekilde, eşleme kuralını etkinleştirmek için de **Etkin olmayan eşleme kuralları** sayfasından bu kuralları işaretleyip **Etkinleştir**'i seçin.

### <a name="remove-mapping-rules"></a>Eşleme kurallarını kaldırma

Eşleme kurallarını kaldırmak için kuralları işaretleyip **Sil**'i seçin.

### <a name="check-for-conflicts"></a>Çakışmaları denetleme

İki eşleme kuralı aynı **Tüzel Kişilik** ve **Satıcı Hesabı** değerlerine sahip olup **Madde Adı** değerleri farklıysa bir çakışma algılanır ve eşleme kuralı oluşturulmaz veya güncelleştirilmez.

## <a name="importexport-mapping-rules-from-excel"></a>Eşleme kurallarını Excel'den içeri aktarma/Excel'e dışarı aktarma

Kuralları toplu olarak yönetmek için bir Excel eklentisi kullanılabilir. Aşağıdaki seçenekler bulunur:

- Bir Excel şablonu indirin.
- Excel'e dışarı aktarın.
- Excel'den içeri aktarın.

### <a name="download-an-excel-template"></a>Excel şablonu indirme

Bir Excel şablonu indirmek için **Şablon indir**'i seçin. Ardından şablona eklenecek alanları seçin.

### <a name="export-to-excel"></a>Excel'e dışarı aktarma

İki yolla dışarı aktarabilirsiniz:

- **Excel Online'da Aç** seçeneğiyle dosyayı Excel'de açabilirsiniz. Daha sonra dosyayı çevrimiçi olarak düzenleyebilirsiniz. Tamamladıktan sonra **Kaydet**'i seçin. Yaptığınız tüm değişiklikler **Eşleme kuralı** sayfasına kaydedilir.
- Eşleme kurallarını içeren bir Excel dosyası indirmek için **Çalışma sayfası indir**'i seçin. Daha sonra dosyayı düzenleyebilirsiniz. Düzenleme işlemi tamamlandığında **Excel'den içeri aktar** seçeneğini kullanarak güncelleştirilmiş çalışma sayfasını karşıya yükleyebilirsiniz.

### <a name="import-from-excel"></a>Excel'den içeri aktarma

1. Bir XLSX dosyasından verileri içeri aktarmak için **Excel'den içeri aktar**'ı seçin. Ayrıca virgülle ayrılmış değerler (CSV) veya XML dosyalarından da verileri içeri aktarabilirsiniz. İçeri aktarmadan önce, yinelenen öğelere izin verilip verilmeyeceğine karar vermeniz gerekir.
2. Öznitelik eşlemesini gözden geçirmek ve doğru olup olmadığını belirlemek için **Eşlemeyi Gözden Geçir**'i seçin. Eşleme ilişkisini değiştirebilirsiniz.
3. İşiniz bittiğinde, içeri aktarma işlemini başlatmak için **İçeri Aktarmayı Tamamla**'yı seçin.
4. **İşlemi İzle** seçeneğinden içeri aktarma işleminin ilerleme durumunu takip edebilirsiniz.

    İçeri aktarma durumu sırasıyla **Bitir**, **Ayrıştırılıyor**, **Dönüştürülüyor** ve son olarak da **Tamamlandı** olarak güncelleştirilir.

İçeri aktarma işlemi tamamlandığında başarılı işlemler, kısmen başarısız olan işlemler, hatalar ve toplam işlenen verilere ilişkin istatistikler gösterilir.
