---
title: Web etkinliği olay toplamasını iptal etme
description: Bu konu, web sitenizin ziyaretçilerinin Microsoft Dynamics 365 Commerce'teki web etkinliği olay toplamasını nasıl iptal etmesine izin verebileceğinizi açıklamaktadır.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416445"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Web etkinliği olay toplamasını iptal etme
[!include [banner](includes/banner.md)]

Bu konu, müşterilerin Microsoft Dynamics 365 Commerce'te web etkinliği olay toplamasını nasıl iptal edebileceğini açıklamaktadır.

## <a name="overview"></a>Özet

Dynamics 365 Commerce, site yöneticilerinin, e-ticaret sitelerindeki kullanıcıların web etkinliğini analiz edebilmesini sağlar. Bu şekilde, sitelerinin nasıl kullanıldığını daha iyi anlayabilir ve daha iyi bir kullanıcı deneyimi sağlamak ve kurumsal hedeflerine ulaşmak amacıyla siteleri en iyi duruma getirebilirler.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Yöneticilerin iptal etme deneyimi sunma yolları

Yöneticiler, bir iptal etme deneyimini üç şekilde uygulayabilir.

### <a name="opt-out-on-behalf-of-users"></a>Kullanıcılar adına iptal etme

Commerce Headquarters'daki (HQ) Hesap yönetiminde, yöneticiler kullanıcıların adına iptal edebilir.

1. HQ istemcisindeki **Tüm müşteriler** sayfasında, bir müşteriyi arayıp seçin.
1. Müşteri ayrıntıları sayfasındaki **Perakende** hızlı sekmesinin **Gizlilik** bölümünde **Web etkinliğini izleme** seçeneğini **Evet** olarak ayarlayın.

    ![Gizlilik ayarları](media/Disablepersonalizationpart2.png)

1. **Kaydet**'i seçip sayfayı kapatın.

### <a name="module-based-opt-out-experience"></a>Modül tabanlı geri çevirme deneyimi

Yöneticiler, kimlik doğrulaması yapılmış kullanıcıların web etkinliği olay toplamasını kendilerinin iptal etmesine izin verebilir. Bu çıkış deneyimini sağlamak için, müşteri hesap profili sayfalarına Kullanıcı geri çevirme modülünü ekleyin.

### <a name="custom-extensions"></a>Özel uzatmalar

Yöneticiler, kullanıcılar için iptal etme deneyimini yönetmek amacıyla kendi uzantılarını oluşturabilir. Daha fazla bilgi için, bkz. [Perakende Sunucu API'lerini çağır](e-commerce-extensibility/call-retail-server-apis.md) ve [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).
