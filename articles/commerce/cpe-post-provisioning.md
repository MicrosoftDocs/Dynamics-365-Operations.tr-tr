---
title: Dynamics 365 Commerce korumalı alan ortamı yapılandırma
description: Bu makale, sağlandıktan sonra Microsoft Dynamics 365 Commerce korumalı alan ortamının nasıl yapılandırılacağını açıklamaktadır.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ae6a8c63721ac32f525e1846a10c0b2caeb08f9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270385"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>Dynamics 365 Commerce korumalı alan ortamı yapılandırma

[!include [banner](includes/banner.md)]

Bu makale, sağlandıktan sonra Microsoft Dynamics 365 Commerce korumalı alan ortamının nasıl yapılandırılacağını açıklamaktadır.

Bu makaledeki yordamları yalnızca Commerce korumalı alan ortamınızı sağlandıktan sonra tamamlayın. Commerce korumalı alan ortamını sağlama hakkında bilgi için bkz. [Commerce korumalı alan ortamı sağlama](provisioning-guide.md).

Commerce korumalı alan ortamınız uçtan uca sağlandıktan sonra, ortamı kullanmaya başlayabilmeniz için sağlama sonrası yapılandırmaya ilişkin ek adımların tamamlanması gerekir. Bu adımları tamamlamak için, Microsoft Dynamics Lifecycle Services'i (LCS) ve Dynamics 365 Commerce öğesini kullanmalısınız.

## <a name="before-you-start"></a>Başlamadan önce

1. [LCS portalda](https://lcs.dynamics.com) oturum açın.
1. Projenize gidin.
1. Listeden ortamınızı seçin.
1. Sağdaki ortam bilgilerinde **Ortamda oturum aç**'a tıklayın. Commerce Headquarters'a gönderilirsiniz.
1. Sağ üst köşede **USRT** hukuk varlığının seçildiğinden emin olun. Bu tüzel kişilik, demo verilerinde önceden yapılandırılmıştır.
1. **Commerce parametreleri \> Yapılandırma parametreleri** bölümüne gidin ve **ProductSearch.UseAzureSearch** için **doğru** olarak ayarlanmış bir giriş olduğundan emin olun. Bu girdi eksikse, ekleyin ve değerini **true** olarak ayarlayın.
1. **Retail ve Commerce \> Headquarters kurulumu \> Commerce planlayıcısı \> Commerce planlayıcısını başlat**'a gidin. **Commerce planlayıcısını başlat** açılır menüsünde, **Var olan yapılandırmayı sil** seçeneğini **Evet** olarak ayarlayın ve **Tamam**'ı seçin.
1. Mağazanın ve e-ticaret kanallarının düzgün çalışması için, bunların Commerce Scale Unit'e eklenmesi gerekir. **Retail ve Commerce \> Headquarters kurulumu \> Commerce planlayıcısı \> Kanal veritabanı**'na gidin ve ardından sol panelde Commerce Scale Unit'i seçin. **Perakende kanalı** hızlı sekmesinde, **AW çevrimiçi mağaza**, **AW Business çevrimiçi mağaza** ve **Fabrikam genişletilmiş çevrimiçi mağaza** kanalları arasından kullanmayı planladığınız e-ticaret kanallarını ekleyin. İsteğe bağlı olarak, satış noktasını (POS) kullanacaksanız perakende mağazaları da ekleyebilirsiniz (örneğin, **Seattle**, **San Francisco** ve/veya **San Jose**).
1. Tüm değişikliklerin kanal veritabanıyla eşitlendiğinden emin olmak için, Commerce Scale Unit için **Kanal Veritabanı \> Tam veri eşitlemesi**'ni seçin.

Commerce Headquarters'daki sağlama sonrası etkinlikler sırasında, **USRT** yasal varlığının her zaman seçili olduğundan emin olun.

## <a name="configure-the-point-of-sale"></a>Satış noktası yapılandırma

### <a name="associate-a-worker-with-your-identity"></a>Çalışanı kimlikle ilişkilendir

Bir çalışanı kimliğinizle ilişkilendirmek için, Commerce Headquarters'daki adımları izleyin.

1. Soldaki menüyü kullanarak, **Modüller \> perakende ve ticaret \> çalışanlar \> İşçiler**'e gidin.
1. Listede, **000713 - Andrew Collette** kaydı bulun ve seçin. Bu örnek kullanıcı, sonraki bölümde kullanılacak olan San Francisco mağazasıyla ilişkilidir.
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

## <a name="set-up-your-e-commerce-sites"></a>E-ticaret sitelerinizi ayarlama

Kullanılabilir üç e-ticaret demo sitesi vardır: Fabrikam, Adventure Works ve Adventure Works Business. Her demo sitesini yapılandırmak için aşağıdaki adımları izleyin.

1. Sağlama sırasında e-Ticareti başlattığınız zaman not ettiğiniz URL'yi kullanarak site oluşturucu aracında oturum açın (bkz. [e-Ticareti başlatma](provisioning-guide.md#initialize-e-commerce)).
1. Site kurulumu iletişim kutusunu açmak için siteyi (**Fabrikam**, **Adventure Works** veya **Adventure Works Business**) seçin.
1. Commerce'ü başlatırken girdiğiniz etki alanını seçin.
1. Headquarters'da, varsayılan kanala karşılık gelen önceden yapılandırılmış çevrimiçi mağaza kanalını (**Fabrikam genişletilmiş çevrimiçi mağaza**, **AW çevrimiçi mağaza** veya **AW Business çevrimiçi mağaza**) seçin.
1. Varsayılan dil için **tr-tr** seçeneğini belirleyin.
1. Yol alanlarını yapılandırın. Bu, tek bir site için boş bırakılabilir, ancak birden çok site için aynı etki alanı adı kullanılıyorsa yapılandırılmalıdır. Örneğin, etki alanı adı `https://www.constoso.com` ise, Fabrikam için boş bir yol (`https://contoso.com`) kullanabilir ve sonra Adventure Works için "aw" (`https://contoso.com/aw`) ve Adventure Works iş sitesi için "awbusiness"ı (`https://contoso.com/awbusiness`) kullanabilirsiniz.
1. **Tamam**'ı seçin. Sitedeki Sayfalar listesi görüntülenir.
1. İsteğe bağlı olarak, diğer demo sitelerini gerektiği gibi yapılandırmak için 2-7 arasındaki adımları yineleyin.

## <a name="enable-jobs"></a>İşleri etkinleştir

Commerce'de işleri etkinleştirmek için şu adımları izleyin:

1. Headquarters ortamında oturum açın.
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

1. İşin durumu **Durduruldu** ise aşağıdaki adımları gerçekleştirin:

    1. Etkin kaydı seçin.
    1. Eylem Bölmesi'nde **Toplu iş**'te **Durumu değiştir**'i tıklayın.
    1. **Bekliyor**'u seçin ve sonra **Tamam**'i seçin.

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
- **Son kullanma tarihi:** 10/30
- **Kart doğrulama değeri (CVV) kod:** 737

> [!IMPORTANT]
> Herhangi bir koşulda test sitesinde gerçek kredi kartı bilgilerini kullanmaya çalışmayın!

## <a name="next-steps"></a>Sonraki adımlar

Sağlama ve yapılandırma adımları tamamlandıktan sonra, korumalı alan ortamınızı kullanmaya başlayabilirsiniz. Yazma deneyimine gitmek için Commerce site oluşturucu URL'sini kullanın. Perakende müşteri site deneyimine gitmek için Commerce sitesi URL'sini kullanın.

Commerce korumalı alan ortamınızla ilgili isteğe bağlı özellikleri yapılandırmak için bkz. [Commerce korumalı alan ortamınız için isteğe bağlı özellikler yapılandırın](cpe-optional-features.md).

E-ticaret kullanıcılarının e-ticaret sitesinde oturum açmasını sağlamak için, Azure Active Directory işletmeden tüketiciye (B2C) aracılığıyla site kimlik doğrulamasını etkinleştirmek üzere ek yapılandırma gereklidir. Talimatlar için bkz. [Commerce'te B2C kiracısı ayarlama](set-up-b2c-tenant.md).

## <a name="troubleshooting"></a>Sorun Giderme

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Site yapılandırılırken site oluşturucu kanal listesi boş

Site oluşturucu herhangi bir çevrimiçi mağaza kanalı göstermezse, yukarıdaki [Başlamadan önce](#before-you-start) bölümünde açıklandığı gibi Headquarters'da kanalların Commerce Scale Unit'e eklendiğinden emin olun. Ayrıca, **Varolan yapılandırmayı sil** değeri **Evet** olarak ayarlanmış şekilde **Commerce planlayıcısını başlat**'ı çalıştırın.  Bu adımlar tamamlandıktan sonra, **Kanal veritabanı** sayfasında (**Retail ve Commerce \> Headquarters kurulumu \> Commerce planlayıcısı \> Kanal veritabanı**), Commerce Scale Unit'te **9999** işini çalıştırın.

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Renk örnekleri kategori sayfasında işlenmiyor, ancak ürün ayrıntıları sayfasında (PDP) işleniyor

Renk ve boyut renk örneklerinin daraltılabilir olarak ayarlandığından emin olmak için bu adımları izleyin.

1. Headquarters'da **Retail ve Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.
1. Sol bölmede, çevrimiçi mağaza kanalını seçin ve sonra **Öznitelik meta verilerini ayarla**'yı seçin.
1. **Özniteliği kanalda göster** seçeneğini **Evet** olarak ayarlayın, **İyileştirilebilir** seçeneğini **Evet** olarak ayarlayın ve sonra **Kaydet**'i seçin. 
1. Çevrimiçi mağaza kanalı sayfasına dönün ve sonra **Kanal güncelleştirmelerini yayınla**'yı seçin.
1. **Retail ve Commerce \> Headquarters kurulumu \> Commerce planlayıcısı \> Kanal veritabanı**'na gidin ve Commerce Scale Unit'te **9999** işini çalıştırın.

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>AdventureWorks iş sitesi için işletme özellikleri açık görünmüyor

Headquarters'da, çevrimiçi mağaza kanalının, **Müşteri türü** olarak **B2B** ayarlanmış şekilde yapılandırıldığından emin olun. **Müşteri türü** **B2C** olarak ayarlanmışsa, varolan kanal düzenlenemediği için yeni bir kanal oluşturulmalıdır. 

Commerce 10.0.26 ve önceki sürümlerde gönderilen demo verileri, **AW Business çevrimiçi mağaza** kanalının yanlış yapılandırılmasıyla ilgili bir hataya sahipti. Geçici çözüm, **B2B** olarak ayarlanması gereken **Müşteri türü** dışında aynı ayar ve yapılandırmalarla yeni bir kanal oluşturmaktır.

## <a name="additional-resources"></a>Ek kaynaklar

[Dynamics 365 Commerce korumalı alan ortamını hazırlama](provisioning-guide.md)

[Dynamics 365 Commerce korumalı alan ortamı için isteğe bağlı özellikleri yapılandırma](cpe-optional-features.md)

[Dynamics 365 Commerce korumalı alan ortamında BOPIS'i yapılandırma](cpe-bopis.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portalı](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce web sitesi](https://aka.ms/Dynamics365CommerceWebsite)

[Commerce'te B2C kiracısı ayarlama](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
