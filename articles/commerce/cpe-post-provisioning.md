---
title: Dynamics 365 Commerce önizleme ortamını yapılandırma
description: Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d72caee25c03e8167b94dd387c7861f98bd0f4cb
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057729"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a>Dynamics 365 Commerce önizleme ortamını yapılandırma


[!include [banner](includes/banner.md)]

Bu konu, hazırlandıktan sonra Microsoft Dynamics 365 Commerce önizleme ortamının nasıl yapılandırılacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Bu konudaki yordamları yalnızca Commerce Preview ortamınızı sağlandıktan sonra tamamlayın. Commerce önizleme ortamını sağlamak hakkında bilgi için bkz. [Commerce önizleme ortamı sağlama](provisioning-guide.md).

Commerce Preview ortamınız sona kadar sağlanmış olduktan sonra, ortamı değerlendirmeye başlamadan önce ek sağlama sonrası konfigürasyon adımlarının tamamlanması gerekir. Bu adımları tamamlamak için, Microsoft Dynamics Lifecycle Services'i (LCS) ve Dynamics 365 Commerce öğesini kullanmalısınız.

## <a name="before-you-start"></a>Başlamadan önce

1. [LCS portalda](https://lcs.dynamics.com) oturum açın.
1. Projenize gidin.
1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Listeden ortamınızı seçin.
1. Sağdaki ortam bilgilerinde **tam ayrıntılar** 'ı tıklatın.
1. **Oturum aç**'ı tıklatın bir menü açmak için **ortamda oturum aç**'ı seçin.
1. Sağ üst köşede **USRT** hukuk varlığının seçildiğinden emin olun.

## <a name="configure-the-point-of-sale-in-lcs"></a>LCS'de satış noktasını konfigüre et

### <a name="associate-a-worker-with-your-identity"></a>Çalışanı kimlikle ilişkilendir

Bir çalışanı LCS ile sizin kimlik ile ilişkilendirmek için, aşağıdaki adımları izleyin.

1. Soldaki menüyü kullanarak, **Modüller \> perakende ve ticaret \> çalışanlar \> İşçiler**'e gidin.
1. Listede, **000713 - Andrew Collette** kaydı bulun ve seçin.
1. Eylem Bölmesinde, **Perakende**'yi seçin.
1. **Var olan kimliği ilişkilendir**'i seçin.
1. **E-posta** alanında (**E-posta kullanarak arama**'nın sağındaki) e-posta adresinizi yazın.
1. **Ara**'yı seçin.
1. Adınızı taşıyan kaydı seçin.
1. **Tamam**'ı seçin.
1. **Kaydet**'i seçin.

### <a name="activate-cloud-pos"></a>Bulut POS'u etkinleştirme

LCS içindeki POS'u etkinleştirmek için aşağıdaki adımları izleyin.

1. Üst menüden **bulut ile barındırılan ortamları** seçin.
1. Listeden ortamınızı seçin.
1. Sağdaki ortam bilgilerinde **tam ayrıntılar** 'ı tıklatın.
1. Bir menüyü açmak için **oturum aç**'ı seçin ve sonra satış noktasını açmak için **bulut satış noktasında oturum aç**'ı seçin.
1. **Sonraki**'yi seçin.
1. Microsoft Azure Active Directory (Azure AD) hesabınızı kullanarak oturum açın.
1. **Mağaza adı** altında, **San Francisco**'yu seçin.
1. **Sonraki**'yi seçin.
1. **Kayıt ve aygıt** altında, **SANFRAN-1** seçin.
1. **Etkinleştir**'i seçin. Oturumunuz kapalı ve POS oturum açma sayfasına götürülüyorsunuz.
1. Şimdi operatör Kodu **000713** ve parola **123** kullanarak Cloud POS deneyimlerinde oturum açabilirsiniz.

## <a name="set-up-your-site-in-commerce"></a>Commerce'te sitenizi ayarlama

Commerce'te önizleme sitenizi ayarlamaya başlamak için aşağıdaki adımları izleyin.

1. Sağlama sırasında e-ticareti başlattığınızda oluşan bir not oluşturduğunuz URL'yi kullanarak Commerce site yönetimi aracında oturum açın (bkz. [e-Ticareti başlat](provisioning-guide.md#initialize-e-commerce)).
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
1. İşin durumu **stopaj** ise, aşağıdaki adımları gerçekleştirin:

    1. Etkin kaydı seçin.
    1. Eylem Bölmesi'nde **Toplu iş**'te **Durumu değiştir**'i tıklayın.
    1. **Bekliyor**'u seçin ve sonra **Tamam**'i seçin.

### <a name="run-full-data-synchronization"></a>Tam veri eşitlemeyi çalıştır

Tam veri eşitlemesini Commerce'de çalıştırmak için aşağıdaki adımları izleyin.

1. Soldaki menüyü kullanarak, **Modüller \> Perakende ve ticaret \> Genel merkez ayarı \> Perakende planlayıcısı \> Kanal veritabanı** gidin.
1. **Varsayılan** kanal, soldaki listeden seçilir. Diğer kullanılabilir kanalı seçin. Bu kanala, **scXXXXXXXXX** adı verilmiştir.
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

Sağlama ve yapılandırma adımları tamamlandıktan sonra, önizleme ortamınızı değerlendirmeye hazırsınız demektir. Geliştirme deneyimine gitmek için Commerce site Management aracının URL 'sini kullanın. Perakende müşteri sitesi deneyimine gitmek için Commerce sitesi URL'sini kullanın.

Commerce Preview ortamınızla ilgili isteğe bağlı özellikleri konfigüre etmek için, bkz. [Commerce önizleme ortamınız için isteğe bağlı özellikler yapılandırın](cpe-optional-features.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce önizleme ortamına genel bakış](cpe-overview.md)

[Dynamics 365 Commerce önizleme ortamını hazırlama](provisioning-guide.md)

[Dynamics 365 Commerce önizleme ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)

[Dynamics 365 Commerce önizleme ortamıyla ilgili SSS](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portalı](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)
