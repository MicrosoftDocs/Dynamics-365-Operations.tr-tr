---
title: Konum tabanlı mağaza algılamayı etkinleştirme
description: Bu makalede, Dynamics 365 Commerce siteniz için yerleşim tabanlı depo algılamanın nasıl açılacağı açıklanmaktadır.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 38c93e30a606d818d909a4ec014009c18c25e8c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274353"
---
# <a name="enable-location-based-store-detection"></a>Konum tabanlı mağaza algılamayı etkinleştirme

[!include [banner](includes/banner.md)]

Bu makalede, Dynamics 365 Commerce siteniz için yerleşim tabanlı depo algılamanın nasıl açılacağı açıklanmaktadır.

Ticaretin yerleşim tabanlı mağaza algılaması, müşterilere, konumlarına göre ilgili site içeriği sağlamanıza olanak sağlar. Konum tabanlı mağaza algılaması açık olduğunda, Ticaret sağlama servisi müşteriyi, kullanılabilen en iyi coğrafi site konfigürasyonuna yönlendirmek için müşterinin web tarayıcısının IP adresinden ülke/bölge bilgilerini kullanır.

## <a name="privacy-notice"></a>Gizlilik bildirimi

Konum temelli depo algılama özelliğini etkinleştirirseniz, müşterinin tarayıcısından alınan bilgiler Microsoft konum hizmetine gönderilir. Bu bilgiler daha sonra, müşterinin konumuyla ilgili müşteri içeriğini sağlamak için kullanılır. Müşteri tarayıcısından gönderilen bilgiler ile müşteriye iade edilen yerleşim tabanlı bilgiler Gizlilik ve tanımlama bilgisi uyumluluk ilkelerine tabidir.

## <a name="turn-on-location-based-store-detection"></a>Konum tabanlı mağaza algılamayı açma

Ticari olarak konum tabanlı mağaza algılamasını etkinleştirmek için aşağıdaki adımları izleyin.

1. Düzenleme aracında sitenize gidin.
1. Soldaki gezinti bölmesinde **Site Yönetimi** seçin.
1. **Site ayarları**'nı seçin.
1. **Konum tabanlı mağaza algılamasını etkinleştir** seçeneğini **açık** olarak ayarlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Etki alanı adınızı yapılandırma](configure-your-domain-name.md)

[Yeni bir e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md)

[E-ticaret sitesi oluşturma](create-ecommerce-site.md)

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

[robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

[Commerce'ta B2C kiracısı ayarlama](set-up-B2C-tenant.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[Commerce ortamında birden fazla B2C kiracısı yapılandırma](configure-multi-B2C-tenants.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
