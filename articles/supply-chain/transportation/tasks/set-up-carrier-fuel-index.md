---
title: Taşıyıcı yakıt dizinini ayarlama
description: Bu kılavuz yakıt dizin bölgesi, yakıt dizini ve taşıyıcı yakıt dizini oluşturmayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f72de7ad54a2b2dc1bf40fd8cb86d8b055e2d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552104"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="dc7d9-103">Taşıyıcı yakıt dizinini ayarlama</span><span class="sxs-lookup"><span data-stu-id="dc7d9-103">Set up a carrier fuel index</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc7d9-104">Bu kılavuz yakıt dizin bölgesi, yakıt dizini ve taşıyıcı yakıt dizini oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="dc7d9-105">Yakıt dizin bölgesi, yakıt dizininin hangi bölgeye uygulanacağını belirtmektedir ve yakıt dizini belirli bir süre için yakıt fiyatını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="dc7d9-106">Zaman içerisinde yakıt fiyatlarındaki değişimi yansıtmak için bir taşıyıcı ile birden fazla yakıt dizini ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="dc7d9-107">Bu görevler genellikle taşımacılık düzenleyicisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="dc7d9-108">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizi kullanarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="dc7d9-109">Bir yakıt dizini bölgesi oluştur</span><span class="sxs-lookup"><span data-stu-id="dc7d9-109">Create a fuel index region</span></span>
1. <span data-ttu-id="dc7d9-110">Taşıma yönetimi > Kurulum > Yakıt dizinleri > Yakıt dizini bölgeleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="dc7d9-111">Önce faaliyet gösterdiğiniz ve farklı yakıt ek giderleri hesapladığınız bölgeleri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="dc7d9-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-112">Click New.</span></span>
3. <span data-ttu-id="dc7d9-113">Bölge alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="dc7d9-114">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="dc7d9-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="dc7d9-116">Yakıt dizini oluştur</span><span class="sxs-lookup"><span data-stu-id="dc7d9-116">Create a fuel index</span></span>
1. <span data-ttu-id="dc7d9-117">Taşıma yönetimi > Kurulum > Yakıt dizinleri > Yakıt dizinleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="dc7d9-118">Ayarlamış olduğunuz bölgeler için geçerli yakıt fiyatını girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="dc7d9-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-119">Click New.</span></span>
3. <span data-ttu-id="dc7d9-120">Bölge alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dc7d9-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="dc7d9-122">Galon başına fiyat alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="dc7d9-123">Yürürlükteki başlangıç tarihi ve saati alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="dc7d9-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="dc7d9-125">Taşıyıcı yakıt dizini oluştur</span><span class="sxs-lookup"><span data-stu-id="dc7d9-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="dc7d9-126">Taşıma yönetimi > Kurulum > Yakıt dizinleri > Taşıyıcı yakıt dizinleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="dc7d9-127">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-127">Click New.</span></span>
3. <span data-ttu-id="dc7d9-128">Taşıyıcı yakıt dizini alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="dc7d9-129">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dc7d9-130">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-130">Click New.</span></span>
6. <span data-ttu-id="dc7d9-131">Yürürlükteki başlangıç tarihi ve saati alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="dc7d9-132">Gelen PPG alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="dc7d9-133">Bu örnekte, Gelen PPG alanını 1,95'e ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="dc7d9-134">Giden PPG alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="dc7d9-135">Bu örnekte, Giden PPG alanını 2'e ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="dc7d9-136">Yüzde alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="dc7d9-137">Bu örnekte, yüzdeyi 3'e ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="dc7d9-138">Para birimi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="dc7d9-139">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="dc7d9-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="dc7d9-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc7d9-141">Click Save.</span></span>

