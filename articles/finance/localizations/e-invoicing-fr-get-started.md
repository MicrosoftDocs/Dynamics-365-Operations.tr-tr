---
title: Fransa için Elektronik faturalama eklentisini kullanmaya başlama
description: Bu makale, Fransa için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 3ac4af8c131e35d9a499d0d558c7cce1d4872b37
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573291"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Fransa için Elektronik faturalama eklentisini kullanmaya başlama

[!include [banner](../includes/banner.md)]

Bu makalede, Fransa için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler yer almaktadır. Regulatory Configuration Service (RCS) için ülkeye bağlı olan yapılandırma adımlarında size kılavuzluk eder. Bu adımlar, [Elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md) konusunda açıklanan adımları tamamlar.

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Fransa Chorus Pro gönderimi (FR) Elektronik faturalama özelliği için ülkeye özel yapılandırma

**Fransa Chorus Pro gönderim (FR)** Elektronik faturalama özelliğini yapılandırmak için bazı adımlar gereklidir. Yapılandırmadaki bazı parametreler varsayılan değerlerle yayınlanır. Bu değerlerin iş operasyonlarınızı daha iyi yansıtması için gözden geçirilmesi ve güncellenmesi gerekir.

### <a name="prerequisites"></a>Ön Koşullar

Bu makaledeki prosedürlere başlamadan önce, aşağıdaki ön koşulları tamamlayın:

- Elektronik faturalamaya aşina olun. Daha fazla bilgi için bkz. [Elektronik faturalamaya genel bakış](e-invoicing-service-overview.md).
- RCS için kaydolun ve Elektronik faturalamayı kurun. Daha fazla bilgi edinmek için aşağıdaki makalelere bakın:

    - [Elektronik Faturalama hizmetine kaydolup yükleyin](e-invoicing-sign-up-install.md)
    - [Elektronik faturalama için Azure kaynaklarını ayarlama](e-invoicing-set-up-azure-resources.md)
    - [Lifecycle Services'de mikro hizmetler için eklentiyi yükleme](e-invoicing-install-add-in-microservices-lcs.md)
    - [Elektronik faturalama ile tümleştirmeyi etkinleştirme ve kurma](e-invoicing-activate-setup-integration.md) – Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management uygulaması ile Elektronik Faturalama hizmetiniz arasında tümleştirmeyi etkinleştirmek için bu makaledeki bilgileri kullanın.
    - [NAF kodları ve siret numaraları](emea-fra-naf-codes-siret-numbers.md) ve [NAF kodları ve Siret numaralarını ayarlama](tasks/fr-00003-naf-codes-siret-numbers.md) – Tüzel kişiliklerinizde NAF kodları ve Siret numaraları ayarlamak için bu makalelerde bulunan bilgileri kullanın. 

- Chorus Pro ile çalışmak için kuruluşunuz kaydedilmelidir. Microsoft, bir uygulama programlama arabirimi (API) aracılığıyla OAuth2 modunda Chorus Pro ile tümleştirme sağlar. Chorus Pro kaydı ve uygulama etkinleştirme hakkında ayrıntılı bilgi için [resmi belgelere](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/) bakın.

    Chorus Pro'ya kaydolmak için şu adımları izleyin.

    1. Kaydınızı başlatmak için [PISTE portalına](https://piste.gouv.fr/en/component/apiportal/registration) gidin. 
    2. Bir uygulamayı kaydedin ve Open Authorization (OAuth) kimlik bilgilerini etkinleştirin.
    3. OAuth kimlik bilgilerinin istemci kimliğini ve gizli anahtarı kopyalayın ve kaydedin. Bu bilgileri sonraki adımlarda kullanacaksınız.
    4. Kayıt yaptırmak için [Chorus Pro portalına](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) gidin. 
    5. API erişimi için teknik bir hesap oluşturun. Daha fazla bilgi için bkz. [Üretimde API erişimi için teknik hesap oluşturma](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Teknik hesabın kullanıcı kimliğini ve parolayı kopyalayın. Bu bilgileri sonraki adımlarda kullanacaksınız.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Fransa Chorus Pro gönderimi (FR) Elektronik faturalama özelliği için uygulama kurulumunun ülkeye özel yapılandırması

**Fransa Chorus Pro gönderimi (FR) Elektronik faturalama** özelliğindeki parametrelerden bazıları, varsayılan değerlerle yayımlanır. Elektronik faturalama özelliğini hizmet ortamına dağıtmadan önce varsayılan değerleri inceleyin ve bunların işletme faaliyetlerinizi daha iyi yansıtması için gerektiği şekilde güncelleştirin.

1. Azure Key Vault'ta gizli diziler ve bunlara karşılık gelen referansları oluşturun. Daha fazla bilgi için [Müşteri sertifikaları ve gizli dizileri](e-invoicing-customer-certificates-secrets.md) konusuna bakın.
2. **Fransa Chorus Pro gönderimi (FR)** küreselleştirme özelliğinin en güncel sürümünü, [Global depodan özellikleri içe aktarma](e-invoicing-import-feature-global-repository.md) bölümünde açıklandığı şekilde içe aktarın.
3. İçe aktarılan genelleştirme özelliğinin bir kopyasını oluşturun ve yapılandırma sağlayıcınızı seçin. Daha fazla bilgi için [Genelleştirme özelliği oluşturma](e-invoicing-create-new-globalization-feature.md) konusuna bakın.
4. **Sürümler** sekmesinde **Taslak** sürümünün seçili olduğunu doğrulayın.
5. **Ayarlar** sekmesinde, kılavuzda, **Türetilen UBL Satış faturası** özellik ayarını seçin.
6. **Düzenle**'yi seçin ve sonra **İşleme ardışık düzeni** sekmesindeki **İşleme ardışık düzeni** bölümünde **(Önizleme) Fransa Chorus Pro ile tümleştir** seçeneğini **Fransa Chorus Pro gönderim** eylem adıyla seçin.
7. **Parametreler** bölümünde, **İstemci kimliği gizli anahtar adı** alanında, Key Vault'taki istemci kimliği için oluşturduğunuz gizli anahtar adını seçin.
8. **İstemci Gizli Anahtar adı** alanında, Key Vault'taki istemci gizli anahtarı için oluşturduğunuz gizli anahtar adını seçin.
9. **Teknik oturum açma gizli anahtarı adı** alanında, Key Vault'taki teknik hesap oturum açma bilgileri için oluşturduğunuz gizli anahtar adını seçin.
10. **Teknik parola gizli anahtarı adı** alanında, Key Vault'taki teknik hesap parolası için oluşturduğunuz gizli anahtar adını seçin.
11. **İşleme ardışık düzeni** sekmesindeki **İşleme ardışık düzeni** bölümünde **Fransa Chorus Pro ile tümleştir** seçeneğini **Fransa Chorus Pro istek durumu** eylem adıyla seçin.
12. **Parametreler** bölümünde, **İstemci kimliği gizli anahtar adı** alanında, Key Vault'taki istemci kimliği için oluşturduğunuz gizli anahtar adını seçin.
13. **İstemci Gizli Anahtar adı** alanında, Key Vault'taki istemci gizli anahtarı için oluşturduğunuz gizli anahtar adını seçin.
14. **Teknik oturum açma gizli anahtarı adı** alanında, Key Vault'taki teknik hesap oturum açma bilgileri için oluşturduğunuz gizli anahtar adını seçin.
15. **Teknik parola gizli anahtarı adı** alanında, Key Vault'taki teknik hesap parolası için oluşturduğunuz gizli anahtar adını seçin.
16. **Kaydet**'i seçip sayfayı kapatın.
17. 6-16 arasındaki adımları, **Türetilen UBL Proje faturası** özellik kurulumu, **UBL Satış Alacak Dekontu türetilmiş** özellik kurulumu ve **Türetilen UBL Proje Alacak Dekontu** özellik kurulumu için yineleyin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik faturalama eklentisine genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlama](e-invoicing-get-started-service-administration.md)
- [Elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md)
