--- 
title: "İlave atamaları ayarlama"
description: "Bu yordam, bir ilave atama kurmayı göstermektedir."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 31787aa180639b934b837b98dc170070d33fd56f
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="41dc0-103">İlave atamaları ayarlama</span><span class="sxs-lookup"><span data-stu-id="41dc0-103">Set up accessorial assignments</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41dc0-104">Bu yordam, bir ilave atama kurmayı göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="41dc0-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="41dc0-105">Bu genellikle taşımacılık düzenleyicisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="41dc0-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="41dc0-106">Bu kılavuzu kullanmadan önce "Hub ek giderleri ve ana ilaveleri ayarlama" kılavuzunu çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="41dc0-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="41dc0-107">İlave atamalar ayarlayın</span><span class="sxs-lookup"><span data-stu-id="41dc0-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="41dc0-108">Taşıma yönetimi > Kurulum > Derecelendirme > Ek atamalar öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="41dc0-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="41dc0-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41dc0-109">Click New.</span></span>
3. <span data-ttu-id="41dc0-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="41dc0-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="41dc0-111">Ayrıntılar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="41dc0-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="41dc0-112">Hub alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41dc0-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="41dc0-113">Listede, "Hub ek giderleri ve ana ilaveleri ayarlama" kılavuzunu çalıştırdığınızda oluşturduğunuz ana ilave Hub'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="41dc0-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="41dc0-114">Hub ilave kimliği alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41dc0-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="41dc0-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41dc0-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="41dc0-116">Ölçütler bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="41dc0-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="41dc0-117">Ölçüt bölümünde giderin uygulanacağı tam ölçütleri, burada sunulan farklı değerleri temel alarak, seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41dc0-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="41dc0-118">Her zaman uygula seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="41dc0-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="41dc0-119">İlave atama düzeyi alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="41dc0-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="41dc0-120">Hesaplama bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="41dc0-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="41dc0-121">İlave ücret türü alanında, 'Sabit'i seçin.</span><span class="sxs-lookup"><span data-stu-id="41dc0-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="41dc0-122">İlave ücret türü, gerçek ücretin nasıl hesaplanacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="41dc0-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="41dc0-123">Bu örnekte bu bir sabit ücrettir.</span><span class="sxs-lookup"><span data-stu-id="41dc0-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="41dc0-124">İlave ücret alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="41dc0-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="41dc0-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41dc0-125">Click Save.</span></span>


