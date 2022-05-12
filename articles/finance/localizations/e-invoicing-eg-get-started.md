---
title: Mısır için elektronik faturalandırma
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile Mısır için elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e21c4ce4d676c3194665672a078dc1e3d0492799
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661736"
---
# <a name="electronic-invoicing-for-egypt"></a>Mısır için elektronik faturalandırma

[!include [banner](../includes/banner.md)]

Bu konu, Mısır için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Regulatory Configuration Service (RCS) için ülkeye bağlı olan yapılandırma adımlarında size kılavuzluk eder. Bu adımlar, [Elektronik faturalamayı kurma](e-invoicing-set-up-overview.md) konusunda açıklanan adımları tamamlar.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki prosedürlere başlamadan önce, aşağıdaki önkoşulları tamamlayın:

- [Elektronik faturalamaya genel bakış](e-invoicing-service-overview.md) bölümünde açıklandığı şekilde Elektronik faturalama hakkında bilgi sahibi olun.
- RCS için kaydolun ve Elektronik faturalamayı kurun. Daha fazla bilgi edinmek için aşağıdaki konulara bakın:

    - [Elektronik Faturalama hizmetine kaydolup yükleyin](e-invoicing-sign-up-install.md)
    - [Elektronik faturalama için Azure kaynaklarını ayarlama](e-invoicing-set-up-azure-resources.md)
    - [Lifecycle Services'de mikro hizmetler için eklentiyi yükleme](e-invoicing-install-add-in-microservices-lcs.md)
    
- Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management uygulaması ile Elektronik Faturalama hizmeti arasında, [Elektronik faturalama ile tümleştirmeyi etkinleştirme ve kurma](e-invoicing-activate-setup-integration.md) bölümünde açıklandığı üzere tümleştirmeyi etkinleştirin.
- Azure Key Vault'ta bir dijital sertifika gizli dizisi oluşturun ve bunu, [Müşteri sertifkaları ve gizli dizileri](e-invoicing-customer-certificates-secrets.md) bölümünde açıklandığı şekilde kurun. Test amacıyla, Mısır vergi dairesi yalnızca test ve çözüm doğrulama aşamaları sırasında kullanılması gereken belirli bir test dijital sertifikaları sağlar. Daha fazla bilgi için, [Mısır e-faturalama SDK'sında](https://sdk.invoicing.eta.gov.eg/faq/) sağlanan bağlantıyı kullanarak Mısır vergi dairesi web sitesine gidin.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Mısır elektronik fatura (EG) özelliği için ülkeye özel yapılandırma

**Mısır elektronik fatura (EG) elektronik faturalama özelliğindeki** parametrelerden bazıları, varsayılan değerlerle yayımlanır. Elektronik faturalama özelliğini hizmet ortamına dağıtmadan önce varsayılan değerleri inceleyin ve bunların işletme faaliyetlerinizi daha iyi yansıtması için gerektiği şekilde güncelleştirin.

1. **Mısır elektronik fatura (EG)** Küreselleştirme özelliğinin en güncel sürümünü, [Global depodan özellikleri içe aktarma](e-invoicing-import-feature-global-repository.md) bölümünde açıklandığı şekilde içe aktarın.
2. İçe aktarılan Küreselleştirme özelliğinin bir kopyasını oluşturun ve bunun için yapılandırma sağlayıcınızı, [Küreselleştirme özelliği oluşturma](e-invoicing-create-new-globalization-feature.md) bölümünde açıklandığı şekilde seçin.
3. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
4. **Ayarlar** sekmesinde, kılavuzda, **Satış faturası türetilen** özellik ayarını seçin.
5. **Düzenle** öğesini seçin.
6. **İşleme ardışık düzeni** sekmesinde, **İşleme ardışık düzeni** bölümünde, **Mısır Vergi Dairesi için json belgesini imzala** seçeneğini belirleyin.
7. **Parametreler** bölümünde, **Sertifika adı**'nı seçin ve sonra da oluşturduğunuz dijital sertifikanın adını seçin.
8. **İşleme ardışık düzeni** bölümünde, **Mısır ETA hizmeti ile tümleştir**'i seçin. Bu eylemin iki tekrarı için bu adımı yineleyin.
9. **Parametreler** bölümünde, **Web hizmeti URL'si** ve **Oturum açma hizmeti URL'si** öğesini seçin. Ardından URL parametrelerini inceleyin. Test ve üretim URL'sini almak için, [Mısır e-faturalama SDK'sında](https://sdk.invoicing.eta.gov.eg/faq/) sağlanan bağlantıyı kullanarak Mısır vergi dairesi web sitesine gidin.
10. **Kaydet**'i seçip sayfayı kapatın.
11. **Proje faturası türetilmiş** özellik kurulumu için 4 ile 10 arasındaki adımları yineleyin.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Mısır elektronik fatura (EG) uygulama kurulumu için ülkeye özel yapılandırma

Finance veya Supply Chain Management ortamınızda ayarlanması gereken parametreler var. Bu kurulumu iki yerden tamamlayabilirsiniz:

- Doğrudan Finance veya Supply Chain Management ortamınızda. Daha fazla bilgi için bkz. [Elektronik faturalama parametrelerini kurma](e-invoicing-set-up-parameters.md).
- RCS'de. Elektronik faturalama özellik kurulumu kapsamında, tüm parametreleri tanımlayabilir ve elektronik faturalama özelliğini dağıtırken, bunları doğrudan Finance veya Supply Chain Management ortamınıza dağıtabilirsiniz.

Her iki seçenek için de parametreler aynıdır. Elektronik faturalama hizmetinde ilk özelliğini ayarlıyorsanız, parametreleri RCS olarak ayarlamak ve sonra bunları bağlantılı uygulamanıza dağıtmak için aşağıdaki adımları izlemeniz önerilir.

> [!NOTE]
> Bazı elektronik faturalama özellik sürümleri, Finance veya Supply Chain Management için önceden tanımlanmış bir uygulamaya özel parametre kümesi içerebilir. Bu durumda, verilerin doğru olduğunu doğrulamanız gerekir. Aksi durumda parametreleri el ile ayarlayın.

1. **Mısır elektronik fatura (EG)** Genelleştirme özelliğinin kopyasını bulun.
2. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
3. **Kurulumlar** sekmesinde **Uygulama Kurulumu**'nu seçin.
4. **Bağlı uygulamalar** alanında, parametreleri dağıtmak istediğiniz uygulamayı seçin.
5. **Elektronik belge türleri** sayfasında, kayıt oluşturmak için **Ekle**'yi seçin.
6. **Tablo adı** alanında, **CustInvoiceJour** ekleyin.
7. **Bağlam** alanında, **Müşteri faturası bağlam** eşleme adına bir referans ekleyin. Konfigürasyon, **Müşteri faturası bağlam modeli**'dir.
8. **Elektronik belge eşlemesi** alanında, **Müşteri faturası** eşleme adına bir referans ekleyin. Konfigürasyon, **Fatura model eşlemesi**'dir.
9. **Kaydet**'i seçin.
10. **Yanıt türleri** sayfasında **Ekle**'yi seçin.
11. **Yanıt türü** alanında, **Yanıt**'ı girin.
12. **Açıklama** alanına, **İşlem yanıtı** girin.
13. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
14. **Model eşleme** alanında, **Yanıt iletisi içe aktar**'ı seçin. Konfigürasyon, **Mısır yanıt iletisi içe aktarma (EG)**'dir.
15. **Kaydet**'i seçin.
16. **Ekle**'yi seçin.
17. **Yanıt türü** alanında, **ResponseData** girin.
18. **Açıklama** alanına, **İşlem yanıtı verileri** girin.
19. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
20. **Veri varlığı adı** alanında, **SalesInvoiceHeaderV2Entity**'yi seçin.
21. **Model eşleme** alanında, **Yanıt verileri içe aktar**'ı seçin. Konfigürasyon, **Mısır yanıt verileri içe aktarma biçimi (EG)**'dir.
22. **Kaydet**'i seçip sayfayı kapatın.
23. Sayfayı kapatın.

Bir özelliği hizmet ortamına ve bir uygulama kurulumunu Finance veya Supply Chain Management'a bağlı uygulamaya dağıtmak için bkz. [Genelleştirme özelliği tamamlama, yayımlama ve dağıtma](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Gizlilik bildirimi

**Mısır elektronik fatura (EG)** özelliğini etkinleştirmek, sınırlı verilerin gönderilmesini gerektirebilir. Bu verilere kuruluşun vergi kayıt kodu dahildir. Bu veriler, devlete ait web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir. Bir yönetici, **Kuruluş yönetimi** \> **Kurulum** \> **Elektronik belge parametreleri** sayfasına giderek özelliği etkinleştirebilir ve devre dışı bırakabilir. **Özellikler** sekmesinde **Mısır elektronik fatura (EG)** özelliğini içeren satırı seçin ve sonra uygun seçimi yapın. Harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir. Daha fazla bilgi için ülkeye özel özellik belgelerindeki "Gizlilik bildirimi" bölümüne bakın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik faturalamaya genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama hizmet yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md)
- [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md)
- [Mısır'da elektronik müşteri faturaları](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
