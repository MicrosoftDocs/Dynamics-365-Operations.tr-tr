--- 
title: " Bağlılık ödül puanlarını tanımlama"
description: "Bu yordam bağlılık ödül puanlarının nasıl belirleneceğini gösterir."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 26b5615df427fb01cc4a1764507fbaa11bf0d7a0
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="9ae92-103"> Bağlılık ödül puanlarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="9ae92-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9ae92-104">Bu yordam bağlılık ödül puanlarının nasıl belirleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ae92-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="9ae92-105">Bir bağlılık programı ayarlamadan önce bağlılık ödül puanları ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9ae92-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="9ae92-106">Bu yordam, USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="9ae92-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="9ae92-107">Retail and commerce > Customers > Loyalty > Loyalty reward points (Perakende ve ticaret > Müşteriler > Bağlılık > Bağlılık programı ödül puanları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="9ae92-107">Go to Retail and commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="9ae92-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ae92-108">Click New.</span></span>
3. <span data-ttu-id="9ae92-109">Ödül puanı kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9ae92-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="9ae92-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9ae92-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9ae92-111">Ödül puanı türü alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9ae92-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="9ae92-112">Ödül puanlarının en yakın tam sayıya yuvarlanmasını istiyorsanız Miktar seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="9ae92-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="9ae92-113">Ödül puanlarının para birimi yuvarlama kurallarına göre yuvarlanmasını istiyorsanız Tutar seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="9ae92-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="9ae92-114">Miktar'ı seçerseniz, bu yordamın bir sonraki adımına atlayın...</span><span class="sxs-lookup"><span data-stu-id="9ae92-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="9ae92-115">Para birimi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9ae92-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="9ae92-116">Tutar türü ödül puanları için, verilen tüm puanlar seçili para birimine sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="9ae92-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="9ae92-117">Miktar türü ödül puanları için bu alan kullanılmaz; bu adımı atlayın.</span><span class="sxs-lookup"><span data-stu-id="9ae92-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="9ae92-118">Kullanılabilir onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="9ae92-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="9ae92-119">Derecelendirme kullanma alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9ae92-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="9ae92-120">Derecelendirme kullanma, ürün ödemeleri için iki veya daha fazla kullanılabilir ödül puanı olduğunda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9ae92-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="9ae92-121">İki ödül puanı aynı derecelendirme kullanma durumuna sahipse, daha düşük sayıda puana sahip olan kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9ae92-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="9ae92-122">Sonra erme süresi değer alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9ae92-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="9ae92-123">Ödül puanlarının süresi, puanlar verildikten sonra belirtilen sayıda gün, ay veya yıl geçtiğinde sonra erer.</span><span class="sxs-lookup"><span data-stu-id="9ae92-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="9ae92-124">'0' değeri bağlılık ödül puanının süresiz olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ae92-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="9ae92-125">Sona erme süresi birimi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="9ae92-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="9ae92-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9ae92-126">Click Save.</span></span>


