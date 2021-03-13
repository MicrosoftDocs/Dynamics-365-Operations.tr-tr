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
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2c396060017db6d7ce830b350f242d3097876e50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012325"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="fb2aa-103">Web etkinliği olay toplamasını iptal etme</span><span class="sxs-lookup"><span data-stu-id="fb2aa-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="fb2aa-104">Bu konu, müşterilerin Microsoft Dynamics 365 Commerce'te web etkinliği olay toplamasını nasıl iptal edebileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fb2aa-105">Özet</span><span class="sxs-lookup"><span data-stu-id="fb2aa-105">Overview</span></span>

<span data-ttu-id="fb2aa-106">Dynamics 365 Commerce, site yöneticilerinin, e-ticaret sitelerindeki kullanıcıların web etkinliğini analiz edebilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="fb2aa-107">Bu şekilde, sitelerinin nasıl kullanıldığını daha iyi anlayabilir ve daha iyi bir kullanıcı deneyimi sağlamak ve kurumsal hedeflerine ulaşmak amacıyla siteleri en iyi duruma getirebilirler.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="fb2aa-108">Yöneticilerin iptal etme deneyimi sunma yolları</span><span class="sxs-lookup"><span data-stu-id="fb2aa-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="fb2aa-109">Yöneticiler, bir iptal etme deneyimini üç şekilde uygulayabilir.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="fb2aa-110">Kullanıcılar adına iptal etme</span><span class="sxs-lookup"><span data-stu-id="fb2aa-110">Opt out on behalf of users</span></span>

<span data-ttu-id="fb2aa-111">Commerce Headquarters'daki (HQ) Hesap yönetiminde, yöneticiler kullanıcıların adına iptal edebilir.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="fb2aa-112">HQ istemcisindeki **Tüm müşteriler** sayfasında, bir müşteriyi arayıp seçin.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="fb2aa-113">Müşteri ayrıntıları sayfasındaki **Perakende** hızlı sekmesinin **Gizlilik** bölümünde **Web etkinliğini izleme** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Gizlilik ayarları](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="fb2aa-115">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="fb2aa-116">Modül tabanlı geri çevirme deneyimi</span><span class="sxs-lookup"><span data-stu-id="fb2aa-116">Module-based opt-out experience</span></span>

<span data-ttu-id="fb2aa-117">Yöneticiler, kimlik doğrulaması yapılmış kullanıcıların web etkinliği olay toplamasını kendilerinin iptal etmesine izin verebilir.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="fb2aa-118">Bu çıkış deneyimini sağlamak için, müşteri hesap profili sayfalarına Kullanıcı geri çevirme modülünü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="fb2aa-119">Özel uzatmalar</span><span class="sxs-lookup"><span data-stu-id="fb2aa-119">Custom extensions</span></span>

<span data-ttu-id="fb2aa-120">Yöneticiler, kullanıcılar için iptal etme deneyimini yönetmek amacıyla kendi uzantılarını oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="fb2aa-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="fb2aa-121">Daha fazla bilgi için, bkz. [Perakende Sunucu API'lerini çağır](e-commerce-extensibility/call-retail-server-apis.md) ve [Çevrimiçi kanal genişletilebilirliği](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="fb2aa-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
