--- 
title: "Üretim emrini bitirme"
description: "Bu yordam, bir üretim emrini nasıl sonlandırabileceğinizi gösterir."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 75b91ea330258a5b57e9e58cb32539d57e458f28
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="end-a-production-order"></a><span data-ttu-id="8385f-103">Üretim emrini bitirme</span><span class="sxs-lookup"><span data-stu-id="8385f-103">End a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8385f-104">Bu yordam, bir üretim emrini nasıl sonlandırabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="8385f-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="8385f-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="8385f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8385f-106">Bu, üretim emri ömrünü açıklayan yedi yordamdan sonuncusudur.</span><span class="sxs-lookup"><span data-stu-id="8385f-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="8385f-107">Üretim emrini bitirme</span><span class="sxs-lookup"><span data-stu-id="8385f-107">End a production order</span></span>
1. <span data-ttu-id="8385f-108">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8385f-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="8385f-109">Durumu, bitirildi olarak raporlandı olan bir üretim emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="8385f-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="8385f-110">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8385f-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="8385f-111">Sonlandır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8385f-111">Click End.</span></span>
    * <span data-ttu-id="8385f-112">Bu sayfada, üretim emrini sonlandırmak istediğinizi onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8385f-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="8385f-113">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8385f-113">Click the General tab.</span></span>
5. <span data-ttu-id="8385f-114">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8385f-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="8385f-115">Hurda yordamı alanında 'Tahsisat' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8385f-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="8385f-116">Tahsisat yöntemini seçtiğinizde, hurda malzeme maliyetleri mamullere eklenir.</span><span class="sxs-lookup"><span data-stu-id="8385f-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="8385f-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8385f-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="8385f-118">Hesaplama sonuçlarını doğrulayın</span><span class="sxs-lookup"><span data-stu-id="8385f-118">Validate calculation results</span></span>
1. <span data-ttu-id="8385f-119">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8385f-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="8385f-120">Maliyet karşılaştırmasını görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8385f-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="8385f-121">Üretim emrini sona erdirdikten sonra, üretim farklarının genel bir bakış elde etmek için, tahmini maliyet fiyatını, gerçekleşmiş maliyet fiyatı ile karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8385f-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  


