---
title: e-Ticaret sitesi oluşturma
description: Bu konu, Dynamics 365 Commerce'de yeni bir e-ticaret sitesi oluşturmayla ilişkili görevleri açıklamaktadır.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697141"
---
# <a name="create-an-e-commerce-site"></a>e-Ticaret sitesi oluşturma

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Commerce'de yeni bir e-ticaret sitesi oluşturmayla ilişkili görevleri açıklamaktadır.

## <a name="overview"></a>Genel Bakış

E-ticaret sitenizi geliştirmeye başlamak için, önce site geliştirme ortamında yeni bir site oluşturmanız gerekir. Yeni bir site oluşturabilmeniz için, Dynamics 365 Retail'de en az bir çevrimiçi mağazanın oluşturulması gereklidir. 

## <a name="set-up-your-site"></a>Sitenizi ayarlama

Sitenizi kurmak için aşağıdakileri yapın.

1. Microsoft Lifecycle Services (LCS) içinde, site yazma ortamı bağlantısını seçin. 
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

[Çevrimiçi mağazaya genel bakış](online-store-overview.md)

[Yeni e-Ticaret sitesini dağıtma](deploy-ecommerce-site.md)

[Çevrimiçi siteyi bir kanalla ilişkilendirme](associate-site-online-store.md)

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[Yazma giriş sayfasına genel bakış](authoring-home-overview.md)

[Yeni site sayfası ekleme](add-new-page.md)
