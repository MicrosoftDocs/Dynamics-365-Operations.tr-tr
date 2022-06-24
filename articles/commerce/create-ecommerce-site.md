---
title: E-ticaret sitesi oluşturma
description: Bu makale, Dynamics 365 Commerce site oluşturucusunda yeni bir e-ticaret sitesi oluşturmak için gereken adımları ve bilgileri açıklamaktadır.
author: bicyclingfool
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b4ac8d1b930c89bf330a2332c0b510dadb92e51f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855782"
---
# <a name="create-an-e-commerce-site"></a>E-ticaret sitesi oluşturma

[!include [banner](includes/banner.md)]

Bu makale, Dynamics 365 Commerce site oluşturucusunda yeni bir e-ticaret sitesi oluşturmak için gereken adımları ve bilgileri açıklamaktadır.

Dynamics 365 Commerce yeteneklerine lisans verirken, site oluşturucu, kendi siteniz için temel olarak kullanabileceğiniz bir başlatıcı siteyle hazırlanacak. Ancak, baştan başlatmak veya ikinci bir site oluşturmak istiyorsanız, site geliştirme ortamında yeni bir site oluşturmanız gerekir. 

## <a name="site-creation-prerequisites"></a>Site oluşturma ön koşulları

Bir site oluşturucu kullanıcısının, e-ticaret sistem yöneticileri için atanmış Azure AD güvenlik grubunda bulunan bir Microsoft Azure Active Directory (Azure AD) kullanıcı hesabına sahip olması gerekir. Daha fazla bilgi için bkz. [Yeni e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md).

> [!NOTE]
> Azure AD konuk kullanıcıların, Azure AD kiracınızda farklı erişim izinleri olabilir. Bir konuk kullanıcı, e-ticaret sistem yöneticilerine atanmış olan bir Azure AD güvenlik grubuna dahil olsa bile, Commerce'te bir e-ticaret sitesi oluşturmak için Azure AD **Harici kullanıcılar** izin ayarına sahip olması gerekebilir. 

Azure AD **Harici kullanıcı** ayarlarını yapmak için aşağıdaki adımları izleyin.

1. Azure portalında Azure AD kiracınıza gidin.
1. **Kullanıcı ayarları \> Harici kullanıcılar**'a gidin ve **Harici iş birliği ayarlarını yönet** bağlantısını seçin. Bu, konuk kullanıcı erişiminin, konuk davetiye ayarlarının ve birlikte çalışma kısıtlamalarının ayarlanabildiği **Harici işbirliği ayarları** sayfasını açar. 
1. Şirket güvenlik ilkelerine uygun olarak harici işbirliği ayarlarını yapın. 

## <a name="set-up-your-site"></a>Sitenizi ayarlama

Sitenizi kurmak için aşağıdakileri yapın.

1. Site oluşturucu ortamını açın. Microsoft Lifecycle Services'teki (LCS) site oluşturucuya bir bağlantıyı Commerce'in ortam özellikleri sayfasında bulabilirsiniz.
1. Site geliştirme ortamının giriş sayfasında **Yeni site**'yi seçin.
1. **Yeni site** iletişim kutusuna, aşağıdaki bilgileri girin.

| Alan                               | Tanım |
|-------------------------------------|-------------|
| Site adı                           | Site geliştirme ortamında siteniz için kullanılacak görünen adı girin. Bu ad yalnızca geliştirme ortamında görünür ve müşteriler tarafından gösterilmez. |
| Site yöneticisinin güvenlik grubu | Bu sitede site Yöneticisi rolüne sahip kullanıcıları yöneten Microsoft Azure Active Directory (Azure AD) güvenlik grubunu belirtin. |
| Varsayılan kanal (faaliyet birimi numarası) | Bu sitenin Web mağazası olarak hizmet verdiği çevrimiçi mağazayı seçin. E-ticaret sitenizin çoklu çevrimiçi mağazaları desteklemesini istiyorsanız, site yüklendikten sonra depoları **site ayarlarında** siteyle ilişkilendirmelisiniz. |
| Varsayılan dil                            | Bu çevrimiçi mağaza ve pazar için varsayılan dili belirtin. Çevrimiçi bir mağaza birden çok dili destekleyebilir. Bu çevrimiçi mağaza veya başka bir çevrimiçi mağaza için birden fazla dili desteklemek istiyorsanız, site yüklendikten sonra bu desteği **Site Ayarları**'nda yapılandırabilirsiniz.  |
| Etki Alanı                              | Bu çevrimiçi mağaza için etki alanı olarak hizmet verdiği etki alanı adını seçin. LCS'de herhangi bir etki alanı konfigüre etmediyseniz, bu alanı boş bırakabilirsiniz. Etki alanınız LCS'de yapılandırıldıktan sonra, **Site ayarlarındaki** çevrimiçi deponuza eklemeniz gerekir.  |
| Yol                              | Siteniz belirli bir etki alanı adı için birden fazla dili destekliyorsa, bu etki alanı ve dil birleşimi için benzersiz bir site URL 'SI oluşturmak üzere yol alanını kullanın. **Varsayılan dil** alanında belirttiğiniz dil bu etki alanı için desteklerinizin tek dili ise veya sitenizi ek dillere yerelleştirdikten sonra varsayılan dil olmaya devam edecek ise, bu alanı boş bırakmanız önerilir. |

Siteniz oluşturulduktan sonra, **ürünler** sekmesini seçerek çevrimiçi deponuzla ilişkili olduğunu doğrulayabilirsiniz. Çevrimiçi mağazaya tahsis edilen ürün sınıflamayı görmelisiniz. Kategoriye göre ilgili ürüne erişmek için sayfanın sol üst tarafındaki açılan menüyü da kullanabilirsiniz.

## <a name="rename-your-site"></a>Sitenizi yeniden adlandırma

Sitenizi site oluşturucuda yeniden adlandırmak için şu adımları izleyin.

1. Site listesi görünümünü açmak için sağ üst köşedeki **Site değiştirici**'yi seçin ve sonra **Siteleri yönet**'i seçin. 
1. Yeniden adlandırmak istediğiniz sitenin yanındaki onay kutusunu seçin ve sonra komut çubuğunda **Yeniden adlandır**'ı seçin.
1. **Yeni site adı** iletişim kutusunda yeni site adını girin ve **Tamam**'ı seçin. Site listesi, sitenin yeni adını gösterecek şekilde güncelleştirilecek.

## <a name="delete-a-site"></a>Site sil

Site oluşturucuda bir site silmek için aşağıdaki adımları izleyin.

1. Site listesi görünümünü açmak için sağ üst köşedeki **Site değiştirici**'yi seçin ve sonra **Siteleri yönet**'i seçin.
1. Silmek istediğiniz siteyi seçin ve sonra komut çubuğunda **Sil**'i seçin.
1. **Sil \<site name\>** iletişim kutusunda site adını girin ve **Sil**'i seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Yeni bir e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md)

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

[robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

[Commerce'ta B2C kiracısı ayarlama](set-up-B2C-tenant.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[Commerce ortamında birden fazla B2C kiracısı yapılandırma](configure-multi-B2C-tenants.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
