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
ms.openlocfilehash: 86f475cc0b78c620309301516b6c3b525b640637
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791569"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="04b62-103">Web etkinliği olay toplamasını iptal etme</span><span class="sxs-lookup"><span data-stu-id="04b62-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="04b62-104">Bu konu, müşterilerin Microsoft Dynamics 365 Commerce'te web etkinliği olay toplamasını nasıl iptal edebileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="04b62-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="04b62-105">Dynamics 365 Commerce, site yöneticilerinin, e-ticaret sitelerindeki kullanıcıların web etkinliğini analiz edebilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="04b62-105">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="04b62-106">Bu şekilde, sitelerinin nasıl kullanıldığını daha iyi anlayabilir ve daha iyi bir kullanıcı deneyimi sağlamak ve kurumsal hedeflerine ulaşmak amacıyla siteleri en iyi duruma getirebilirler.</span><span class="sxs-lookup"><span data-stu-id="04b62-106">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="04b62-107">Yöneticilerin iptal etme deneyimi sunma yolları</span><span class="sxs-lookup"><span data-stu-id="04b62-107">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="04b62-108">Yöneticiler, bir iptal etme deneyimini üç şekilde uygulayabilir.</span><span class="sxs-lookup"><span data-stu-id="04b62-108">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="04b62-109">Kullanıcılar adına iptal etme</span><span class="sxs-lookup"><span data-stu-id="04b62-109">Opt out on behalf of users</span></span>

<span data-ttu-id="04b62-110">Commerce Headquarters'daki (HQ) Hesap yönetiminde, yöneticiler kullanıcıların adına iptal edebilir.</span><span class="sxs-lookup"><span data-stu-id="04b62-110">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="04b62-111">HQ istemcisindeki **Tüm müşteriler** sayfasında, bir müşteriyi arayıp seçin.</span><span class="sxs-lookup"><span data-stu-id="04b62-111">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="04b62-112">Müşteri ayrıntıları sayfasındaki **Perakende** hızlı sekmesinin **Gizlilik** bölümünde **Web etkinliğini izleme** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="04b62-112">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Gizlilik ayarları](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="04b62-114">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="04b62-114">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="04b62-115">Modül tabanlı geri çevirme deneyimi</span><span class="sxs-lookup"><span data-stu-id="04b62-115">Module-based opt-out experience</span></span>

<span data-ttu-id="04b62-116">Yöneticiler, kimlik doğrulaması yapılmış kullanıcıların web etkinliği olay toplamasını kendilerinin iptal etmesine izin verebilir.</span><span class="sxs-lookup"><span data-stu-id="04b62-116">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="04b62-117">Bu çıkış deneyimini sağlamak için, müşteri hesap profili sayfalarına Kullanıcı geri çevirme modülünü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="04b62-117">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="04b62-118">Özel uzatmalar</span><span class="sxs-lookup"><span data-stu-id="04b62-118">Custom extensions</span></span>

<span data-ttu-id="04b62-119">Yöneticiler, kullanıcılar için iptal etme deneyimini yönetmek amacıyla kendi uzantılarını oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="04b62-119">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="04b62-120">Daha fazla bilgi için, bkz. [Perakende Sunucu API'lerini çağır](e-commerce-extensibility/call-retail-server-apis.md) ve [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="04b62-120">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
