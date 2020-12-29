---
title: Üretim emrini bitirme
description: Bu yordam, bir üretim emrini nasıl sonlandırabileceğinizi gösterir.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fade659c320e0ea1059644324859c9a3cb273c96
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438997"
---
# <a name="end-a-production-order"></a><span data-ttu-id="e7ac6-103">Üretim emrini bitirme</span><span class="sxs-lookup"><span data-stu-id="e7ac6-103">End a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7ac6-104">Bu yordam, bir üretim emrini nasıl sonlandırabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="e7ac6-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e7ac6-106">Bu, üretim emri ömrünü açıklayan yedi yordamdan sonuncusudur.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="e7ac6-107">Üretim emrini bitirme</span><span class="sxs-lookup"><span data-stu-id="e7ac6-107">End a production order</span></span>
1. <span data-ttu-id="e7ac6-108">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="e7ac6-109">Durumu, bitirildi olarak raporlandı olan bir üretim emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="e7ac6-110">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="e7ac6-111">Sonlandır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-111">Click End.</span></span>
    * <span data-ttu-id="e7ac6-112">Bu sayfada, üretim emrini sonlandırmak istediğinizi onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="e7ac6-113">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-113">Click the General tab.</span></span>
5. <span data-ttu-id="e7ac6-114">Tarih alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="e7ac6-115">Hurda yordamı alanında 'Tahsisat' seçeneğini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="e7ac6-116">Tahsisat yöntemini seçtiğinizde, hurda malzeme maliyetleri mamullere eklenir.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="e7ac6-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="e7ac6-118">Hesaplama sonuçlarını doğrulayın</span><span class="sxs-lookup"><span data-stu-id="e7ac6-118">Validate calculation results</span></span>
1. <span data-ttu-id="e7ac6-119">Eylem Bölmesi'nde, Maliyetleri yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="e7ac6-120">Maliyet karşılaştırmasını görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="e7ac6-121">Üretim emrini sona erdirdikten sonra, üretim farklarının genel bir bakış elde etmek için, tahmini maliyet fiyatını, gerçekleşmiş maliyet fiyatı ile karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7ac6-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
