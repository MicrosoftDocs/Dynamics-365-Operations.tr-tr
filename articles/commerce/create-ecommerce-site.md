---
title: E-ticaret sitesi oluşturma
description: Bu konu, Dynamics 365 Commerce site oluşturucusunda yeni bir e-ticaret sitesi oluşturmak için gereken adımları ve bilgileri açıklamaktadır.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7d552f29fd8f52b512a7c21b36b0a814cac50646
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517196"
---
# <a name="create-an-e-commerce-site"></a>E-ticaret sitesi oluşturma

[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Commerce site oluşturucusunda yeni bir e-ticaret sitesi oluşturmak için gereken adımları ve bilgileri açıklamaktadır.

Dynamics 365 Commerce yeteneklerine lisans verirken, site oluşturucu, kendi siteniz için temel olarak kullanabileceğiniz bir başlatıcı siteyle hazırlanacak. Ancak, baştan başlatmak veya ikinci bir site oluşturmak istiyorsanız, site geliştirme ortamında yeni bir site oluşturmanız gerekir. 

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
