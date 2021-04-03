---
title: Mısır için Elektronik faturalama eklentisini kullanmaya başlama
description: Bu konu, Finance ve Supply Chain Management'ta Mısır için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592610"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a>Mısır için Elektronik faturalama eklentisini kullanmaya başlama

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Bu konu, Mısır için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Bu konu Regulatory Configuration Services'da (RCS) ülkeye bağlı olan yapılandırma adımlarında size kılavuzluk eder ve [Elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md) konusunda açıklanan adımları tamamlar.

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Mısır elektronik fatura (EG) Elektronik faturalama özelliği için ülkeye özel yapılandırma

Mısır elektronik fatura (EG) elektronik faturalama özelliğini yapılandırmak için tamamlanması gereken bazı adımlar vardır. Yapılandırmalardaki bazı parametreler varsayılan değerlerle yayımlanır, bu nedenle iş operasyonlarınıza daha iyi uymaları için incelenmeli ve güncelleştirilmelidir.

### <a name="prerequisites"></a>Önkoşullar

Bu bölümdeki yordamı tamamlamadan önce şunları yapmanız gerekir:

- [Electronic faturalama eklentisi hizmeti yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md) konusundaki **dijital sertifika gizli anahtarı oluştur** bölümünde açıklandığı gibi dijital bir sertifika gizli anahtarı oluşturun. Test amacıyla, Mısır vergi dairesi yalnızca test ve çözüm doğrulama aşamaları sırasında kullanılması gereken belirli bir test dijital sertifikaları sağlar. Daha fazla bilgi için, [Mısır e-faturalama SDK'sında](https://sdk.sit.invoicing.eta.gov.eg/faq/) sağlanan bağlantıyı kullanarak Mısır vergi dairesi Web sitesine bakın.
- [Elektronik faturalama eklentisini kullanmaya başlayın](e-invoicing-get-started.md) konusunun **kuruluş sağlayıcı bölümünde elektronik faturalama oluştur** bölümünde açıklandığı gibi, kuruluşunuz için bir Mısır  elektronik fatura (EG) elektronik faturalama özelliği oluşturun.

1. RCS'de **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama eklentisi** kutucuğunu seçin.
2. **Elektronik faturalama eklentisi özellikleri** sayfasında, oluşturduğunuz **Mısır elektronik fatura (EG)** elektronik faturalama özelliğinin seçili olduğunu doğrulayın.
3. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
4. **Ayarlar** sekmesinde, kılavuzda, **Satış faturası** özellik ayarını seçin.
5. **Düzenle** öğesini seçin ve **Eylemler** sekmesinde, **Eylemler** alan grubunda, **Mısır Vergi Dairesi için json belgesi imzala** seçeneğini belirleyin.
6. **Parametreler** alan grubunda parametreyi, **sertifika adını** seçin ve elektronik faturalama özelliğiyle kullanılmak üzere oluşturulan dijital sertifikanın adını seçin.
7. **Eylemler** alan grubunda **Mısır ETA hizmeti ile tümleştir**'i seçin. Bu eylemin iki tekrarı için bu adımı yineleyin.
8. **Parametreler** alan grubunda, **Web hizmeti URL**'sini ve **oturum açma hizmeti URL**'sini seçin ve gerekirse URL parametrelerini gözden geçirin. [Mısır e-faturalama SDK'sında](https://sdk.sit.invoicing.eta.gov.eg/faq/) sağlanan bağlantıyı kullanarak Test ve Üretim URL'sini almak için Mısır vergi dairesi Web sitesine bakın.
9. **Kaydet**'i seçip sayfayı kapatın.
10. Uygulama kurulumunu yapılandırmak için, [elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md) konusuna bakın.

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Mısır elektronik fatura (EG) elektronik faturalama özelliği için uygulama kurulumunun ülkeye özel yapılandırması

**Mısır elektronik fatura (EG)** elektronik faturalama özelliği için uygulama kurulumunun yapılandırması, belirli adımların tamamlanmasını gerektirir. Elektronik faturalama özelliğini elektronik faturalama eklenti servisi ortamınıza dağıtmadan önce, bu adımları tamamlamanız gerekir.

### <a name="prerequisites"></a>Önkoşullar

Bu bölümdeki yordamı tamamlamadan önce, [Elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md) konusunun **Uygulama kurulumunu yapılandırma** bölümünde açıklandığı gibi, **Mısır elektronik fatura (EG)** elektronik faturalama özelliği için uygulama kurulumunu yapılandırmak için **Mısır elektronik fatura (EG)** elektronik faturalama özelliği oluşturun ve başlatın.

1. RCS'de **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama eklentisi** kutucuğunu seçin.
2. **Elektronik faturalama eklentisi özellikleri** sayfasında, **Mısır elektronik fatura (EG)** elektronik faturalama özelliğinin seçili olduğunu doğrulayın.
3. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
4. **Ayarlar** sekmesinde, **Uygulama kurulumu**'nu seçin ve **bağlı uygulama** alanında, dağıtma işlemini yapmak istediğiniz uygulamayı seçin.
5. **Tablo adı** alanında, müşteri faturası günlüğünün seçili olduğunu doğrulayın.
6. **Yanıt türlerini** seçin ve ardından **yeni**'yi seçin.
7. **Yanıt türü** alanında, "yanıt"ı girin ve **Açıklama** alanına "Açıklama" yazın.
8. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
9. **Model eşleme** alanında, **Yanıt iletisinden model eşlemesi** ile **(Önizleme) Yanıt iletisi içe aktarma biçimi**'ni seçin ve ardından **Kaydet**'i seçin.
10. **Yeni**'yi seçin ve **Yanıt türü** alanında, sabit değer olarak "ResponseData" öğesini girin. **Açıklama** alanına "Açıklama" yazın.
11. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
12. **Veri varlığı adı** alanında, **Satış faturası başlıkları v2**'yi seçin.
13. **Model eşleme** alanında, **Mısır yanıt verisi içe aktarma** ile **(Önizleme) Mısır yanıt verisi içe aktarma**'yı seçin ve ardından **Kaydet**'i seçin.
14. Elektronik faturalama özelliğini dağıtmak için, [Elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md) konusuna bakın.

## <a name="privacy-notice"></a>Gizlilik bildirimi

**Mısır elektronik fatura (EG)** özelliğinin etkinleştirilmesi kuruluş vergi kayıt kodunu içeren sınırlı verilerin gönderilmesini gerektirebilir. Bu veriler, devlete ait Web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir. Bir yönetici, **Kuruluş yönetimi** >  **Kurulum** > **Elektronik belge parametreleri** sayfasına giderek özelliği etkinleştirebilir ve devre dışı bırakabilir. **Özellikler** sekmesinde **Mısır elektronik fatura (EG)** özelliğini içeren satırı seçin ve sonra uygun seçimi yapın. Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir. Daha fazla bilgi için, lütfen ülkeye özel özellik belgelerindeki Gizlilik bildirimi bölümlerine bakın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik faturalama eklentisine genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md)
- [Elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md)
- [Mısır'da elektronik müşteri faturaları](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
