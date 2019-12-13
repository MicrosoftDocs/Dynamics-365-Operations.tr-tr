---
title: Etki alanı adınızı yapılandırma
description: Bu konu, Microsoft Dynamics 365 e-ticaret sitesi için etki alanı adının nasıl yapılandırılacağını açıklamaktadır.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770470"
---
# <a name="configure-your-domain-name"></a>Etki alanı adınızı yapılandırma

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 e-ticaret sitesi için etki alanı adının nasıl yapılandırılacağını açıklamaktadır. 

## <a name="add-domains-during-e-commerce-initialization"></a>E-ticaret başlatma sırasında etki alanları ekleme

Etki alanlarını e-ticaret ortamınızla ilişkilendirmek için, [yeni e-ticaret sitesini dağıtma](deploy-ecommerce-site.md) konusunda açıklandığı gibi e-ticaret başlatın. Başlatma sırasında, e-ticaret ortamınızı sağlamak için kullanılacak bilgileri vermeniz istenir. **Desteklenen ana bilgisayar adları** alanında, bu ortamda kullanmayı planladığınız tüm etki alanlarını ekleyin. Birden çok etki alanı noktalı virgül ile ayrılmalıdır. Bu şekilde, etki alanları gerekli tüm e-ticaret bileşenlerinde yapılandırılır ve içerik teslim ağından (CDN) veya Web sunucusundan gelen trafiği değiştirdiğinizde ve bunu e-ticaret ön uçlarına işaret ettiğinizde kullanılmaya hazır hale gelir.

## <a name="add-domains-after-e-commerce-initialization"></a>E-ticaret başlatmadan sonra etki alanları ekleme

E-ticaret başlatmasının ardından yeni etki alanlarını e-ticaret ortamınızla ilişkilendirmek için, bir servis isteği göndermeniz gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

[Çevrimiçi mağazaya genel bakış](online-store-overview.md)

[e-Ticaret sitesi oluşturma](create-ecommerce-site.md)

[Yeni e-Ticaret sitesini dağıtma](deploy-ecommerce-site.md)

[Çevrimiçi siteyi bir kanalla ilişkilendirme](associate-site-online-store.md)

[İçerik teslim ağı (CDN) için destek ekleme](add-cdn-support.md)

[Konum tabanlı mağaza algılamayı etkinleştirme](enable-store-detection.md)

[Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama](custom-pages-user-logins.md)
