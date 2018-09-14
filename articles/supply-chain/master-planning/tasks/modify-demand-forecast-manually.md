--- 
title: "Talep tahminini el ile değiştirme"
description: "Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 063554c98b8a6261ebe69073f214a8e45850c623
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="a5104-103">Talep tahminini el ile değiştirme</span><span class="sxs-lookup"><span data-stu-id="a5104-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5104-104">Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a5104-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="a5104-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="a5104-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a5104-106">Bu kayıt için üretim planlayıcısı içindir.</span><span class="sxs-lookup"><span data-stu-id="a5104-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="a5104-107">Bir madde için tahmin değiştirme</span><span class="sxs-lookup"><span data-stu-id="a5104-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="a5104-108">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a5104-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="a5104-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a5104-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a5104-110">Tahminini değiştirmek istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a5104-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="a5104-111">Örneğin, madde D0001'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5104-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="a5104-112">Eylem Bölmesinde, Planla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5104-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="a5104-113">Talep tahmini öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5104-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="a5104-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a5104-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="a5104-115">Tahmin satırı yoksa, </span><span class="sxs-lookup"><span data-stu-id="a5104-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="a5104-116">uygulama çubuğunda Yeni üzerine tıklayarak yeni bir satır oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a5104-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="a5104-117">Satış miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a5104-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="a5104-118">Bu sayı, madde için tahmin edilmiş miktarı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="a5104-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="a5104-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5104-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="a5104-120">Tahmini Excel'de değiştirin</span><span class="sxs-lookup"><span data-stu-id="a5104-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="a5104-121">Microsoft Office'te aç seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a5104-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="a5104-122">Tahmin talebini Excel'de düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a5104-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="a5104-123">Excel'de talep tahmin satırlarını ekleyebilir, silebilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a5104-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="a5104-124">Excel'deki verileri göremiyorsanız, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a "oturumu koru" seçeneği etkin olarak oturum açmanız ve veri bağlantısı uygulamasına güvenmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a5104-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


