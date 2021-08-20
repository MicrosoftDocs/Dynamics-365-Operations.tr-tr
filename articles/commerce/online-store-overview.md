---
title: E-ticaret sitesine genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce ile e-ticaret siteleri desteğinin genel görünümünü sağlar .
author: bicyclingfool
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d8d1b563b08cce1d7b56c0ab5ebc06d1c900f281e1ceb961721978ba8718eba8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741124"
---
# <a name="e-commerce-site-overview"></a>E-ticaret sitesine genel bakış

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce ile e-ticaret siteleri desteğinin genel görünümünü sağlar . E-ticaret çevrimiçi mağazaların Dynamics 365 Commerce uygulamasında nasıl başlatıldığı ve yönetildiği hakkında bilgi içerir . Ayrıca, çevrimiçi mağazalar ve e-ticaret sitesinin nasıl ayarlanacağı ve yapılandırılacağı hakkında bilgi sağlayan bir bağlantı da sağlar. Bu konu, temel bilgilerin çoğunu kapsasa da, üretim e-ticaret sitesini ayarlamak için gereken her şeyi kapsamaz. Dynamics 365 Commerce Belgelerde daha gelişmiş konular bulunabilir .

## <a name="online-store-channel"></a>Çevrimiçi mağaza kanalı

Yeni bir site oluşturabilmeniz için Dynamics 365 Commerce'de en az bir çevrimiçi mağaza kanalının oluşturulması gereklidir. Daha fazla bilgi için, bkz. [Çevrimiçi kanal ayarlama](channel-setup-online.md). 

Dynamics 365 Commerce uygulamasında, ürünleri, fiyatları, dilleri, ödeme yöntemlerini, teslim modlarını, karşılama merkezlerini ve müşterileriniz için kullanılabilir olması gereken çevrimiçi deneyimlerin diğer özelliklerini oluşturmak için bir çevrimiçi mağaza kanalı kullanırsınız.

Dynamics 365 Commerce kullanmaya başlamadan önce yalnızca bir çevrimiçi mağaza kanalının kurulması yeterlidir. Ancak, tek e-ticaret sitesi birden çok çevrimiçi mağaza için çevrimiçi deneyim sağlayabilir. Örneğin, birden fazla çevrimiçi mağaza farklı coğrafi bölgeleri destekleyecek şekilde ayarlandıysa, her bir mağaza tarafından tanımlanan benzersiz deneyimleri sağlamak için tek bir e-ticaret sayfaları kümesi kullanılabilir. Birden çok çevrimiçi mağaza destekleyecek bir siteyi konfigüre etme hakkında daha fazla bilgi için, bkz. [Kanalla çevrimiçi site ilişkilendirme](associate-site-online-store.md).

Çevrimiçi bir mağaza kurduktan sonra, çevrimiçi storefront işlevi görecek Dynamics 365 Commerce siteyle ilişkilendirilebilir. Çevrimiçi mağazalar ve bunların nasıl ayarlanacağı hakkında daha fazla bilgi için [Çevrimiçi mağazaları ayarla](/dynamics365/unified-operations/retail/online-stores)'ya bakın.

## <a name="deploy-a-new-e-commerce-tenant"></a>Yeni bir e-ticaret kiracısını dağıtma

Bir e-ticaret sitesinin başlatılması sırasında, bir etki alanı adı istenir. Commerce etki alanları hakkında daha fazla bilgi için, bkz. [Etki alanı adınızı yapılandırın](configure-your-domain-name.md) ve [Dynamics 365 Commerce'teki etki alanları](domains-commerce.md). [Microsoft Dynamics Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) kullanarak yeni bir e-ticaret kiracısı dağıtmak için [Yeni bir e-ticaret kiracısı dağıtma adımlarını izleyin ](deploy-ecommerce-site.md). E-ticaret kiracınız LCS'de ayarlandığında, Commerce Site Builder'a bir bağlantı sağlanır. Daha sonra, e-ticaret sitelerinizi başlatmak ve yapılandırmak için Commerce Site Builder 'ı kullanabilirsiniz.

## <a name="initialize-your-e-commerce-site"></a>E-ticaret sitenizi başlatma

LCS 'den Commerce Site Builder 'ı başlattığınızda, **siteler** sayfası görüntülenir. Bu sayfa, aşağıdaki çizimdeki örnekte gösterildiği gibi, **varsayılan** ve **Fabrikam** olmak üzere önceden yapılandırılmış iki siteyi içerir.

![Commerce site oluşturucudaki siteler sayfası.](media/e-commerce-site-01.png)

Bu sitelerden birini seçtiğinizde, bir etki alanı adı, varsayılan bir çevrimiçi mağaza kanalı, seçili kanal için desteklenen bir dil ve bir yol seçmeniz istenir. Yalnızca bir kanal kullanılıyorsa yolu boş bırakabilirsiniz. Daha sonra Commerce Site Builder'da daha fazla çevrimiçi mağaza kanalı veya dili konfigüre edilebilir. Her ek kanal veya dil benzersiz bir yol gerektirir. Örneğin, tek bir siteyle ilişkilendirilmiş iki çevrimiçi kanallarınız vardır ve sitenin etki alanı adı: `www.fabrikam.com`. Bu durumda, bir kanalın yolu (`https://www.fabrikam.com`) içermeyen varsayılan değer olabilir ve ikinci kanal `https://www.fabrikam.com/site2` URL 'yi alacak olan **site2** gibi yeni bir yola ayarlanabilir. Aşağıdaki çizimde, Commerce Site Builder'da bir site başlatma iletişim kutusu örneği gösterilmektedir.

![Commerce site oluşturucusunda site başlatma iletişim kutusu.](media/e-commerce-site-02.png)

**Siteler** sayfası **Yeni bir site** düğmesi de içerir. Bu düğmeyi seçtiğinizde görüntülenen iletişim kutusu site başlatma iletişim kutusuna benzer, ancak yeni bir site oluşturmak için kullanılır. Yeni siteler boş. **Varsayılan** ve **Fabrikam** tesislerinde sağlanan varsayılan şablonlar, parçalar, sayfalar ve görüntüler de yer alır . Ancak, gereksinim duyduğunuz gibi, varsayılan içeriğin bir kopyasının yeni boş bir siteye eklenmesini istemek için bir destek bileti açabilirsiniz. Daha fazla bilgi için, bkz [e-ticaret sitesi oluşturma](create-ecommerce-site.md).

Yeni bir site başlatıldıktan sonra, Commerce Site Builder **giriş** sayfası görüntülenir. Bu sayfa, aşağıdaki çizimdeki örnekte gösterildiği gibi, sık kullanılan eylemlere ve kılavuz içeriğine bağlantılar içerir.

![Commerce site oluşturucudaki giriş sayfasındaki bağlantılar.](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Çevrimiçi mağaza kanallarını değiştirin veya bir e-ticaret sitesine çevrimiçi mağaza kanalları ekleyin

Bir e-ticaret sitesi oluşturulduktan sonra, [bir e-ticaret sitesini çevrimiçi kanalla ilişkilendirme](associate-site-online-store.md) adımlarını izleyerek ilişkili olduğu kanalı değiştirebilirsiniz. Aşağıdaki çizimde yer alan örnek, **Kanallar** sayfasında kanal işletim birimi numarası (OUN) nasıl değiştirilebileceği gösterilmiştir (**Site ayarlar \> Kanallar**). Değişiklik yapmayı bitirdikten sonra, **Kaydet ve Yayımla**'yı seçtiğinizden emin olun. Bu şekilde, değişikliğin yayımlanmasını güvence altına alırsınız.

![Commerce site oluşturucudaki kanallar sayfası.](media/e-commerce-site-04.png)

**Kanal ekle** 'yi seçerek yeni kanallar ekleyebilirsiniz . Bir kanala yeni diller eklemek için kanalı seçin ve sonra görüntülenen kanal iletişim kutusunda bir **yerel ayar Ekle**'yi seçin. Yerel ayarların iletişim kutusunda görünebilmesi için önce Commerce Headquarters 'daki çevrimiçi mağaza kanalı için önceden konfigüre edilmiş olmaları gerekir.

![Commerce site oluşturucuda kanal iletişim kutusu.](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Bir Azure B2C kiracısı ayarla

Dynamics 365 Commerce, kullanıcı kimlik bilgileri ve kimlik doğrulama akışlarını desteklemek için Azure Active Directory (Azure AD) iş-müşteri B2C kullanır. Azure B2C kiracınızı kurma hakkında bilgi için, bkz. [Commerce'te bir B2C kiracısı kurun](set-up-b2c-tenant.md), [Kullanıcı oturumu için özel sayfalar ayarlayın](custom-pages-user-logins.md) ve [Commerce ortamında birden fazla B2C kiracıları konfigüre edin](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Varsayılan site sayfalarına genel bakış

**Varsayılan** ve **fabrikam** siteleri, başlamanıza yardımcı olacak önceden yapılandırılmış şablonları, parçaları ve sayfaları içerir. Daha fazla bilgi edinmek için aşağıdaki konulara bakın:

- [Giriş sayfasına genel bakış](quick-tour-home-page.md)
- [Ürün ayrıntıları sayfalarına genel bakış](quick-tour-pdp.md)
- [Sepet ve ödeme sayfalarına genel bakış](quick-tour-cart-checkout.md)
- [Hesap yönetimi sayfalarına genel bakış](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Site ayarlarını yönetme

Site ayarlarınızı yönetme hakkında daha fazla bilgi için aşağıdaki konulara bakın:

- [e-Ticaret kullanıcıları ve rolleri yönetme](manage-ecommerce-users-roles.md)
- [Siteniz için arama alt yapısını en iyi duruma getirmeyle (SEO) ilgili konular](/search-engine-optimization-considerations.md)
- [İçerik Güvenliği İlkesini (CSP) yönetme](manage-csp.md)
- [Site teması seçme](select-site-theme.md)

## <a name="manage-site-content"></a>Site içeriğini yönetme

Site içeriğini yönetme hakkında daha fazla bilgi için aşağıdaki konulara bakın:

- [Sayfa modeli sözlüğü](page-elements-overview.md)
- [Belge durumları ve yaşam döngüsü](document-states-overview.md)
- [Şablonlar ve düzenler](templates-layouts-overview.md)
- [Parçalarla çalışma](work-with-fragments.md)
- [Modüllerle çalışma](work-with-modules.md)
- [Dijital varlık yönetimine genel bakış](dam-overview.md)
- [Modül kitaplığına genel bakış](starter-kit-overview.md)

## <a name="additional-resources"></a>Ek kaynaklar

[E-ticaret sitesi oluşturma](create-ecommerce-site.md)

[Yeni e-Ticaret sitesini dağıtma](deploy-ecommerce-site.md)

[Çevrimiçi siteyi bir kanalla ilişkilendirme](associate-site-online-store.md)

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]