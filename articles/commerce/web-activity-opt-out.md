---
title: Web etkinliği olay toplamasını iptal etme
description: Bu makale, web sitenizin ziyaretçilerinin Microsoft Dynamics 365 Commerce'teki web etkinliği olay toplamasını nasıl iptal etmesine izin verebileceğinizi açıklamaktadır.
author: bebeale
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 81343f5033366484140f73fcc313ecd9f35e7d47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286738"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Web etkinliği olay toplamasını iptal etme
[!include [banner](includes/banner.md)]

Bu makale, müşterilerin Microsoft Dynamics 365 Commerce'te web etkinliği olay toplamasını nasıl iptal edebileceğini açıklamaktadır.

Dynamics 365 Commerce, site yöneticilerinin, e-ticaret sitelerindeki kullanıcıların web etkinliğini analiz edebilmesini sağlar. Bu şekilde, sitelerinin nasıl kullanıldığını daha iyi anlayabilir ve daha iyi bir kullanıcı deneyimi sağlamak ve kurumsal hedeflerine ulaşmak amacıyla siteleri en iyi duruma getirebilirler.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Yöneticilerin iptal etme deneyimi sunma yolları

Yöneticiler, bir iptal etme deneyimini üç şekilde uygulayabilir.

### <a name="opt-out-on-behalf-of-users"></a>Kullanıcılar adına iptal etme

Commerce Headquarters'daki (HQ) Hesap yönetiminde, yöneticiler kullanıcıların adına iptal edebilir.

1. HQ istemcisindeki **Tüm müşteriler** sayfasında, bir müşteriyi arayıp seçin.
1. Müşteri ayrıntıları sayfasındaki **Perakende** hızlı sekmesinin **Gizlilik** bölümünde **Web etkinliğini izleme** seçeneğini **Evet** olarak ayarlayın.

    ![Gizlilik ayarları.](media/Disablepersonalizationpart2.png)

1. **Kaydet**'i seçip sayfayı kapatın.

### <a name="module-based-opt-out-experience"></a>Modül tabanlı geri çevirme deneyimi

Yöneticiler, kimlik doğrulaması yapılmış kullanıcıların web etkinliği olay toplamasını kendilerinin iptal etmesine izin verebilir. Bu çıkış deneyimini sağlamak için, müşteri hesap profili sayfalarına Kullanıcı geri çevirme modülünü ekleyin.

### <a name="custom-extensions"></a>Özel uzatmalar

Yöneticiler, kullanıcılar için iptal etme deneyimini yönetmek amacıyla kendi uzantılarını oluşturabilir. Daha fazla bilgi için, bkz. [Perakende Sunucu API'lerini çağır](e-commerce-extensibility/call-retail-server-apis.md) ve [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
