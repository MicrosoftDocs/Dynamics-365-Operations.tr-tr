---
title: Mısır için Elektronik faturalamayı kullanmaya başlama
description: Bu konu, Finance ve Supply Chain Management'ta Mısır için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: abae35db7e37e65950c05c8e21b8e8555edbf3be
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920793"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a>Mısır için Elektronik faturalamayı kullanmaya başlama

[!include [banner](../includes/banner.md)]

Bu konu, Mısır için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Bu konu Regulatory Configuration Services'da (RCS) ülkeye bağlı olan yapılandırma adımlarında size kılavuzluk eder ve [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusunda açıklanan adımları tamamlar.

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Mısır elektronik fatura (EG) Elektronik faturalama özelliği için ülkeye özel yapılandırma

**Mısır elektronik fatura (EG) elektronik faturalama özelliğindeki** parametrelerden bazıları varsayılan değerlerle yayımlanır. Değerleri gözden geçirin ve gerekirse, elektronik faturalama özelliğini servis ortamına dağıtmadan önce iş operasyonlarınızı daha iyi yansıtması için değerleri güncelleştirin.

Bu bölüm, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusunun **Elektronik Faturalama özelliği için ülkeye özgü yapılandırma** bölümünü tamamlayıcı niteliktedir.

### <a name="prerequisites"></a>Önkoşullar

Bu bölümdeki yordamı tamamlamadan önce şunları yapmanız gerekir:

- [Electronic faturalama hizmeti yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md) konusundaki **dijital sertifika gizli anahtarı oluştur** bölümünde açıklandığı gibi dijital bir sertifika gizli anahtarı oluşturun. Test amacıyla, Mısır vergi dairesi yalnızca test ve çözüm doğrulama aşamaları sırasında kullanılması gereken belirli bir test dijital sertifikaları sağlar. Daha fazla bilgi için, [Mısır e-faturalama SDK'sında](https://sdk.sit.invoicing.eta.gov.eg/faq/) sağlanan bağlantıyı kullanarak Mısır vergi dairesi Web sitesine bakın.

1. RCS'te **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
2. **Elektronik faturalama özellikleri** sayfasında, oluşturduğunuz **Mısır elektronik fatura (EG)** elektronik faturalama özelliğinin seçili olduğunu doğrulayın.
3. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
4. **Ayarlar** sekmesinde, kılavuzda, **Satış faturası** özellik ayarını seçin.
5. **Düzenle** öğesini seçin ve **Eylemler** sekmesinde, **Eylemler** alan grubunda, **Mısır Vergi Dairesi için json belgesi imzala** seçeneğini belirleyin.
6. **Parametreler** alan grubunda parametreyi, **sertifika adını** seçin ve elektronik faturalama özelliğiyle kullanılmak üzere oluşturulan dijital sertifikanın adını seçin.
7. **Eylemler** alan grubunda **Mısır ETA hizmeti ile tümleştir**'i seçin. Bu eylemin iki tekrarı için bu adımı yineleyin.
8. **Parametreler** alan grubunda, **Web hizmeti URL**'sini ve **oturum açma hizmeti URL**'sini seçin ve gerekirse URL parametrelerini gözden geçirin. [Mısır e-faturalama SDK'sında](https://sdk.sit.invoicing.eta.gov.eg/faq/) sağlanan bağlantıyı kullanarak Test ve Üretim URL'sini almak için Mısır vergi dairesi Web sitesine bakın.
9. **Kaydet**'i seçip sayfayı kapatın.
10. Elektronik faturalama özelliğini Service ortamına dağıtmak için, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusuna bakın.

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Mısır elektronik fatura (EG) elektronik faturalama özelliği için uygulama kurulumunun ülkeye özel yapılandırması

Uygulama kurulumunu Finance veya Supply Chain Management bağlı uygulamanıza dağıtmadan önce bu adımları tamamlayın.

Bu bölüm, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusunun **Uygulama kurulumunu ülkeye özgü yapılandırma** bölümünü tamamlayıcı niteliktedir.

1. RCS'te **Genelleştirme özelliği** çalışma alanının **Özellikler** bölümünde, **Elektronik faturalama** kutucuğunu seçin.
2. **Elektronik faturalama özellikleri** sayfasında, **Mısır elektronik fatura (EG)** elektronik faturalama özelliğinin seçili olduğunu doğrulayın.
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
14. Uygulama kurulumunu Finance veya Supply Chain Management bağlı uygulamasına dağıtmak için, [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) konusuna bakın.

## <a name="privacy-notice"></a>Gizlilik bildirimi

**Mısır elektronik fatura (EG)** özelliğinin etkinleştirilmesi kuruluş vergi kayıt kodunu içeren sınırlı verilerin gönderilmesini gerektirebilir. Bu veriler, devlete ait Web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir. Bir yönetici, **Kuruluş yönetimi** >  **Kurulum** > **Elektronik belge parametreleri** sayfasına giderek özelliği etkinleştirebilir ve devre dışı bırakabilir. **Özellikler** sekmesinde **Mısır elektronik fatura (EG)** özelliğini içeren satırı seçin ve sonra uygun seçimi yapın. Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir. Daha fazla bilgi için, lütfen ülkeye özel özellik belgelerindeki Gizlilik bildirimi bölümlerine bakın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik faturalamaya genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama hizmet yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md)
- [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md)
- [Mısır'da elektronik müşteri faturaları](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
