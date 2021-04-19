---
title: Etki alanı adınızı yapılandırma
description: Bu konu, Microsoft Dynamics 365 e-ticaret sitesi için etki alanı adının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796063"
---
# <a name="configure-your-domain-name"></a>Etki alanı adınızı yapılandırma


[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 e-ticaret sitesi için etki alanı adının nasıl yapılandırılacağını açıklamaktadır. 

## <a name="add-domains-during-e-commerce-initialization"></a>E-ticaret başlatma sırasında etki alanları ekleme

Etki alanlarını Dynamics 365 Commerce e-ticaret ortamınızla ilişkilendirmek için, [yeni e-ticaret kiracısı dağıtma](deploy-ecommerce-site.md) konusunda açıklandığı gibi e-ticaret başlatın. Başlatma sırasında, e-ticaret ortamınızı sağlamak için kullanılacak bilgileri vermeniz istenir. **Desteklenen ana bilgisayar adları** alanında, bu ortamda kullanmayı planladığınız tüm etki alanlarını ekleyin. Birden çok etki alanı noktalı virgül ile ayrılmalıdır. Bu şekilde, etki alanları gerekli tüm e-ticaret bileşenlerinde yapılandırılır ve içerik teslim ağından (CDN) veya Web sunucusundan gelen trafiği değiştirdiğinizde ve bunu e-ticaret ön uçlarına işaret ettiğinizde kullanılmaya hazır hale gelir.

## <a name="add-domains-after-e-commerce-initialization"></a>E-ticaret başlatmadan sonra etki alanları ekleme

E-ticaret başlatmasının ardından yeni etki alanlarını e-ticaret ortamınızla ilişkilendirmek için, bir servis isteği göndermeniz gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Yeni bir e-ticaret kiracısını dağıtma](deploy-ecommerce-site.md)

[E-ticaret sitesi oluşturma](create-ecommerce-site.md)

[Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme](associate-site-online-store.md)

[robots.txt dosyalarını yönetme](manage-robots-txt-files.md)

[URL yeniden yönlendirmelerini toplu olarak yükleme](upload-bulk-redirects.md)

[Commerce'ta B2C kiracısı ayarlama](set-up-B2C-tenant.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)

[Commerce ortamında birden fazla B2C kiracısı yapılandırma](configure-multi-B2C-tenants.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]