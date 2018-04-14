--- 
title: "Talep tahminini el ile değiştirme"
description: "Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir."
author: YuyuScheller
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6fd59d3f6c3a5926a2191a89dd682154714c9fa1
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="dc923-103">Talep tahminini el ile değiştirme</span><span class="sxs-lookup"><span data-stu-id="dc923-103">Modify a demand forecast manually</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc923-104">Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="dc923-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="dc923-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="dc923-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dc923-106">Bu kayıt için üretim planlayıcısı içindir.</span><span class="sxs-lookup"><span data-stu-id="dc923-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="dc923-107">Bir madde için tahmin değiştirme</span><span class="sxs-lookup"><span data-stu-id="dc923-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="dc923-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="dc923-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="dc923-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dc923-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dc923-110">Tahminini değiştirmek istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="dc923-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="dc923-111">Örneğin, madde D0001'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc923-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="dc923-112">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc923-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="dc923-113">Talep tahmini öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc923-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="dc923-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dc923-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dc923-115">Tahmin satırı yoksa, </span><span class="sxs-lookup"><span data-stu-id="dc923-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="dc923-116">uygulama çubuğunda Yeni üzerine tıklayarak yeni bir satır oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dc923-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="dc923-117">Satış miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dc923-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="dc923-118">Bu sayı, madde için tahmin edilmiş miktarı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="dc923-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="dc923-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc923-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="dc923-120">Tahmini Excel'de değiştirin</span><span class="sxs-lookup"><span data-stu-id="dc923-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="dc923-121">Microsoft Office'te aç seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc923-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="dc923-122">Tahmin talebini Excel'de düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dc923-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="dc923-123">Excel'de talep tahmin satırlarını ekleyebilir, silebilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc923-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="dc923-124">Excel'deki verileri göremiyorsanız, Microsoft Dynamics 365 for Finance and Operations'a "oturumu koru" seçeneği etkin olarak oturum açmanız ve veri bağlantısı uygulamasına güvenmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc923-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


