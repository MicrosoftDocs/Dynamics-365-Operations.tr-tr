---
title: Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özelliklerin nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6bc968c2659380bb8c92292ee19e3a7ec8a20a2b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795919"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özelliklerin nasıl yapılandırılacağını açıklamaktadır.

## <a name="prerequisites"></a>Önkoşullar

İşlem e-posta özelliklerini değerlendirmek istiyorsanız, aşağıdaki önkoşulların karşılanması gerekir:

- Kullanılabilir bir e-posta sunucunuz var (Basit Posta Transfer Protokolü \[SMTP\] sunucusu); Bunlar, değerlendirme ortamını temin ettiğiniz Microsoft Azure aboneliğinden kullanılabilir.
- Sunucunun tam etki alanı adına (FQDN)/IP adresi, SMTP bağlantı noktası numaranız ve kullanılabilir kimlik doğrulama detayları vardır.

## <a name="configure-the-image-back-end"></a>Görüntüyü arka arkaya konfigüre etme

### <a name="find-your-media-base-url"></a>Medya taban URL'nizi bulun

> [!NOTE]
> Bu yordamı tamamlayabilmek için, [sitenizi Commerce'ta ayarlama](cpe-post-provisioning.md#set-up-your-site-in-commerce) adımlarını tamamlamanız gerekir.

1. Sağlama sırasında e-Ticareti başlattığınız zamanı not ettiğiniz URL'yi kullanarak Commerce site oluşturucu aracında oturum açın (bkz. [e-Ticareti başlatma](provisioning-guide.md#initialize-e-commerce)).
1. **Fabrikam** sitesini açın.
1. Soldaki menüden **Medya Kitaplığı**'nı seçin.
1. Herhangi bir tek resim varlığı seçin.
1. Sağdaki Özellik denetçisinde, **genel URL** özelliğini bulun. Değer bir URL. Aşağıda bir örnek verilmiştir:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. URL'deki son tanımlayıcıyı (önceki örnek URL'de **MA1nQC**) aşağıdaki dizeyle Değiştirin: **search?fileName=**. Örnek URL'nin bu değişiklik yapıldıktan sonra nasıl göründüğü aşağıda vardır:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Bu URL, ortam taban URL'sidir. Not alın.

### <a name="update-the-media-base-url"></a>Ortam temel URL'si güncelleştirin

1. Commerce Headquarters'da oturum açın.
1. Soldaki menüyü kullanarak, **Modüller \> Perakende ve ticaret \>> Kanal ayarı \> Kanal profilleri** gidin.
1. **Düzenle** öğesini seçin.
1. **Profil özelliklerinden**, **ortam sunucusu temel URL**'sinin özellik değerini daha önce oluşturduğunuz ortam taban URL'siyle değiştirin.
1. **scXXXXXXXXX** adlı kanalı seçin.
1. **Profil özellikleri** altında, **Ekle**'yi seçin.
1. Eklenen özellik için, özellik anahtarı olarak **ortam sunucusu temel URL**'yi seçin. Özellik değeri olarak, önceden oluşturduğunuz ortam taban URL'sini girin.
1. **Kaydet**'i seçin.

## <a name="configure-and-test-the-email-server"></a>E-posta sunucusunu yapılandırma ve test etme

> [!NOTE]
> Burada girdiğiniz SMTP sunucusu ya da e-posta hizmetinin, ortam için kullandığınız Azure aboneliği içinden erişilebilir olması gerekir.

1. Commerce Headquarters'da oturum açın.
1. Soldaki menüyü kullanarak, **Modüller \> Retail ve Commerce \> Headquarters kurulumu \> Parametreler \> E-posta parametreleri**'ne gidin.
1. **SMTP** ayarları sekmesinde, **giden posta sunucusu** alanına SMTP sunucunuzun veya e-posta hizmetinizin FQDN'sini veya IP adresini girin.
1. **SMTP port numarası** alanına port numarasını girin. (Güvenli Yuvalar katmanı \[SSL\]'yi kullanmıyorsanız, varsayılan bağlantı noktası numarası **25**'tir.)
1. Kimlik doğrulama gerekliyse, değerleri **Kullanıcı adı** ve **parola** alanlarına girin.
1. **Kaydet**'i seçin.
1. **Yenile**'yi seçin.
1. **Test e-postası** sekmesinde, **e-posta sağlayıcısı** alanından **SMTP**'yi seçin.
1. **Gönder** alanına, test e-adresinin teslim edilmesini istediğiniz e-posta adresini girin.
1. **Test e-postası gönder**'i seçin.

## <a name="configure-email-templates"></a>E-posta şablonlarını yapılandır

E-postalarını göndermek istediğiniz her işlemsel olay için e-posta şablonunun geçerli bir gönderen e-posta adresiyle güncelleştirilmesi gerekir.

1. Commerce Headquarters'da oturum açın.
1. Soldaki menüyü kullanarak, **Modüller \> Retail ve Commerce \> Headquarters kurulumu \> Parametreler \> Kuruluş e-posta şablonları**'na gidin.
1. **Listeyi göster**'i seçin.
1. Listedeki her şablon için şu adımları izleyin:

    1. **Gönderen e-postası** alanına Gönderen e-posta adresini girin.
    1. İsteğe bağlı: **gönderen adı** alanına gönderen adı olarak kullanılacak adı girin.

1. **Kaydet**'i seçin.

## <a name="customize-email-templates"></a>E-posta şablonlarını özelleştirme

E-posta şablonlarını farklı görüntüler kullanacak şekilde özelleştirmek isteyebilirsiniz. Veya şablonların bağlantılarını, değerlendirme ortamınıza gitmeleri için güncelleştirmek isteyebilirsiniz. Bu prosedür, varsayılan şablonların nasıl karşıdan yükleneceğini açıklar, bunları özelleştirin ve sistemdeki şablonları güncelleştirir.

1. Tarayıcı kullanarak, [Microsoft Dynamics 365 Commerce Değerlendirme varsayılan e-posta şablonları zip dosyasını](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) indirin. Bu dosya aşağıdaki HTML belgelerini içerir:

    - Sipariş onayı şablonu
    - Hediye kartı şablonu
    - Yeni sipariş şablonu
    - Paket sipariş şablonu
    - Sipariş şablonu al

1. Metin veya HTML Düzenleyicisi kullanarak şablonları özelleştirin. [Desteklenen belirteçler](#supported-tokens-in-the-email-template) listesine bu konunun ilerisinde bakın.
1. Commerce'de oturum açın.
1. Soldaki menüyü kullanarak, **Modüller \> Kuruluş yönetimi \> Kurulum \>> Kuruluş e-posta şablonları** gidin.
1. Tüm şablonları görmek için soldaki listeyi genişletin.
1. Özelleştirmek istediğiniz her şablon için şu adımları izleyin:

    1. Listeden şablonunu seçin.
    1. **E -posta iletisi içeriği** altında, listeden uygun dil sürümünü seçin. (Varsayılan dil değeri **tr-tr**'dir.)
    1. **E-posta iletisi içeriği** altında **Düzenle**'yi seçin. **E-posta şablonu karşıya yükle** bölmesi görünür.
    1. **Gözat**'ı seçin ve özelleştirilmiş içeriğe sahip olan HTML dosyasını bulun.
    1. **Yükle**'yi seçin. Şablonunuz sisteme yüklenir ve bir önizleme gösterilir.
    1. **Tamam**'ı seçin.
    1. İsteğe bağlı: Şablonun **konu** özelliğini özelleştirin.
    1. **Kaydet**'i seçin.

### <a name="supported-tokens-in-the-email-template"></a>E-posta şablonunda desteklenen belirteçler

E-posta oluşturulduğunda, bu belirteçler, müşteriye uygulanan gerçek değerlerle e-posta işleme zamanında değiştirilecek.

#### <a name="sales-order"></a>Satış siparişi

Aşağıdaki belirteçler genel satış siparişi için geçerlidir.

| Belirtecin adı | Belirteç |
|-------------------|-------|
| Sipariş numarası      | %salesid% |
| Müşteri adı   | %customername% |
| Teslimat adresi  | %deliveryaddress% |
| Fatura adresi   | %customeraddress% |
| Sipariş tarihi        | %shipdate% |
| Teslimat şekli     | %modeofdelivery% |
| İskonto          | %discount% |
| Satış vergisi         | %tax% |
| Sipariş toplamı       | %total% |

#### <a name="sales-line"></a>Satış satırı

Aşağıdaki belirteçler siparişteki her ürün için değerlerle değiştirilir.

> [!NOTE]
> **Ürün listesi - Başlangıç** belirtecini her ürün için tekrarlanan HTML bloğunun başına yerleştirin ve bloğun sonuna **ürün listesi - uç** belirtecini koyun.

| Belirtecin adı      | Belirteç |
|------------------------|-------|
| Ürün listesi - başlangıç   | \<!--%tablebegin.salesline% --\> |
| Ürün listesi - bitiş     | \<!--%tableend.salesline%--\> |
| Ürün adı           | %lineproductname% |
| Tanım            | %lineproductdescription% |
| Miktar               | %linequantity% |
| Satır birim fiyatı        | %lineprice% (doğrula) |
| satır maddesi toplamı        | %linenetamount% |
| satır iskontosu          | %linediscount% |
| Sevk tarihi              | %lineshipdate% |
| Tedarik yöntemi     | %linedeliverymode% |
| teslimat adresi       | %linedeliveryaddress% |
| Satırın satış birimi | %lineunit% |

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce değerlendirme ortamına genel bakış](cpe-overview.md)

[Dynamics 365 Commerce değerlendirme ortamı sağlama](provisioning-guide.md)

[Dynamics 365 Commerce değerlendirme ortamı yapılandırma](cpe-post-provisioning.md)

[Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma](cpe-bopis.md)

[Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portalı](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]