---
title: Dynamics 365 Commerce değerlendirme ortamı yapılandırma
description: Bu konu, sağlandıktan sonra Microsoft Dynamics 365 Commerce değerlendirme ortamının nasıl yapılandırılacağını açıklamaktadır.
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
ms.openlocfilehash: 10e80830a1cb0864c7eef19857b91e36ad27cdef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795871"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce değerlendirme ortamı yapılandırma

[!include [banner](includes/banner.md)]

Bu konu, sağlandıktan sonra Microsoft Dynamics 365 Commerce değerlendirme ortamının nasıl yapılandırılacağını açıklamaktadır.

Bu konudaki yordamları yalnızca Commerce değerlendirme ortamınızı sağlandıktan sonra tamamlayın. Commerce değerlendirme ortamını sağlamak hakkında bilgi için bkz. [Commerce değerlendirme ortamı sağlama](provisioning-guide.md).

Commerce değerlendirme ortamınız sona kadar sağlanmış olduktan sonra, ortamı değerlendirmeye başlamadan önce ek sağlama sonrası yapılandırma adımlarının tamamlanması gerekir. Bu adımları tamamlamak için, Microsoft Dynamics Lifecycle Services'i (LCS) ve Dynamics 365 Commerce öğesini kullanmalısınız.

## <a name="before-you-start"></a>Başlamadan önce

1. [LCS portalda](https://lcs.dynamics.com) oturum açın.
1. Projenize gidin.
1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Listeden ortamınızı seçin.
1. Sağdaki ortam bilgilerinde **Ortamda oturum aç**'a tıklayın. Commerce Headquarters'a gönderilirsiniz.
1. Sağ üst köşede **USRT** hukuk varlığının seçildiğinden emin olun.

Commerce Headquarters'daki sağlama sonrası etkinlikler sırasında, **USRT** yasal varlığının her zaman seçili olduğundan emin olun.

## <a name="configure-the-point-of-sale"></a>Satış noktası yapılandırma

### <a name="associate-a-worker-with-your-identity"></a>Çalışanı kimlikle ilişkilendir

Bir çalışanı kimliğinizle ilişkilendirmek için, Commerce Headquarters'daki adımları izleyin.

1. Soldaki menüyü kullanarak, **Modüller \> perakende ve ticaret \> çalışanlar \> İşçiler**'e gidin.
1. Listede, **000713 - Andrew Collette** kaydı bulun ve seçin.
1. Eylem Bölmesinde **Commerce** öğesini seçin.
1. **Var olan kimliği ilişkilendir**'i seçin.
1. **E-posta** alanında (**E-posta kullanarak arama**'nın sağındaki) e-posta adresinizi yazın.
1. **Ara**'yı seçin.
1. Adınızı taşıyan kaydı seçin.
1. **Tamam**'ı seçin.
1. **Kaydet**'i seçin.

### <a name="activate-cloud-pos"></a>Bulut POS'u etkinleştirme

Bulut POS'u etkinleştirmek için LCS'deki şu adımları izleyin.

1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Listeden ortamınızı seçin.
1. Sağdaki ortam bilgilerinde **Bulut Satış Noktasında oturum aç**'ı seçin.
1. **Başlamadan önce** iletişim kutusunu açmak için **İleri**'yi seçin.
1. **Sunucu URL'si** alanını olduğu gibi bırakın. **Sonraki**'yi seçin.
1. Microsoft Azure Active Directory (Azure AD) hesabınızı kullanarak oturum açın.
1. **Mağaza adı** altında, **San Francisco**'yu ve ardından **İleri**'yi seçin.
1. **Kayıt ve aygıt** altında, **SANFRAN-1** seçin.
1. **Etkinleştir**'i seçin. Oturumunuz kapalı ve POS oturum açma sayfasına götürülüyorsunuz.
1. Şimdi operatör Kodu **000713** ve parola **123** kullanarak Cloud POS deneyimlerinde oturum açabilirsiniz.

## <a name="set-up-your-site-in-commerce"></a>Commerce'te sitenizi ayarlama

Commerce'te değerlendirme sitenizi ayarlamaya başlamak için aşağıdaki adımları izleyin.

1. Sağlama sırasında e-Ticareti başlattığınız zaman not ettiğiniz URL'yi kullanarak site oluşturucu aracında oturum açın (bkz. [e-Ticareti başlatma](provisioning-guide.md#initialize-e-commerce)).
1. Site kurulum iletişim kutusunu açmak için **Fabrikam** sitesine tıklayın.
1. E-ticaret'i başlattığınızda girdiğiniz etki alanını seçin.
1. Varsayılan kanal için **Fabrikam genişletilmiş çevrimiçi mağaza**'yı seçin. (**Genişletilmiş** çevrimiçi mağazayı seçtiğinizden emin olun)
1. Varsayılan dil için **tr-tr** seçeneğini belirleyin.
1. **Yol** alanının değerini olduğu gibi bırakın.
1. **Tamam**'ı seçin. Sitedeki Sayfalar listesi görüntülenir.

## <a name="enable-jobs"></a>İşleri etkinleştir

Commerce'de işleri etkinleştirmek için şu adımları izleyin:

1. Ortama oturum açın (HQ).
1. Soldaki menüyü kullanarak **perakende ve ticaret \> Sorgulamalar ve raporlar \> toplu işler**'e gidin.

    Bu yordamın geri kalan adımlarının aşağıdaki işlerin her biri için tamamlanması gerekir:

    * Perakende siparişi e-posta bildirimini işle
    * Ürün bulunabilirliği
    * P-0001
    * Sipariş işlerini eşitle

1. Yukarıdaki adı kullanarak işi aramak için hızlı filtre'yi kullanın.
1. İşin durumu **Yürütülüyor** ise, aşağıdaki adımları izleyin:

    1. Etkin kaydı seçin.
    1. Eylem Bölmesi'nde **Toplu iş**'te **Durumu değiştir**'i tıklayın.
    1. **İptal ediliyor**'u ve ardından **Tamam**'ı seçin.

İsteğe bağlı olarak, yineleme aralığını aşağıdaki işler için bir (1) dakikaya ayarlayabilirsiniz:

* Perakende siparişi e-posta bildirimini işleme işi
* P-0001 iş
* Sipariş işlerini eşitle

### <a name="run-full-data-synchronization"></a>Tam veri eşitlemeyi çalıştır

Commerce'de tam veri eşitlemesini çalıştırmak için Commerce Headquarters'da aşağıdaki adımları izleyin.

1. Soldaki menüyü kullanarak, **Modüller \> Perakende ve ticaret \> Genel merkez ayarı \> Ticaret planlayıcısı \> Kanal veritabanı** gidin.
1. **scXXXXXXXXX** adlı kanalı seçin.
1. Eylem bölmesinde **tam veri eşitleme**'yi tıklatın.
1. Dağıtım planı olarak **9999**'ı seçin.
1. **Tamam**'ı seçin.
1. **Tamam**'ı seçin.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Test satın almaları gerçekleştirmek için kredi kartı bilgilerini sına

Sitede test hareketleri gerçekleştirmek için, aşağıdaki test kredi kartı bilgilerini kullanabilirsiniz:

- **Kart numarası:** 4111-1111-1111-1111
- **Son kullanma tarihi:** 10/20
- **Kart doğrulama değeri (CVV) kod:** 737

> [!IMPORTANT]
> Herhangi bir koşulda test sitesinde gerçek kredi kartı bilgilerini kullanmaya çalışmayın!

## <a name="next-steps"></a>Sonraki adımlar

Sağlama ve yapılandırma adımları tamamlandıktan sonra, değerlendirme ortamınızı kullanmaya başlayabilirsiniz. Yazma deneyimine gitmek için Commerce site oluşturucu URL'sini kullanın. Perakende müşteri site deneyimine gitmek için Commerce sitesi URL'sini kullanın.

Commerce değerlendirme ortamınızla ilgili isteğe bağlı özellikleri yapılandırmak için bkz. [Commerce değerlendirme ortamınız için isteğe bağlı özellikler yapılandırma](cpe-optional-features.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce değerlendirme ortamına genel bakış](cpe-overview.md)

[Dynamics 365 Commerce değerlendirme ortamı sağlama](provisioning-guide.md)

[Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)

[Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma](cpe-bopis.md)

[Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portalı](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
