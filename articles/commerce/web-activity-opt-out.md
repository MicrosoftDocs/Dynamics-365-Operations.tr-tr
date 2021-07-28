---
title: Web etkinliği olay toplamasını iptal etme
description: Bu konu, web sitenizin ziyaretçilerinin Microsoft Dynamics 365 Commerce'teki web etkinliği olay toplamasını nasıl iptal etmesine izin verebileceğinizi açıklamaktadır.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 25464c89352f44a77a96dee6ad2f633b7a55669e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350292"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Web etkinliği olay toplamasını iptal etme
[!include [banner](includes/banner.md)]

Bu konu, müşterilerin Microsoft Dynamics 365 Commerce'te web etkinliği olay toplamasını nasıl iptal edebileceğini açıklamaktadır.

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
