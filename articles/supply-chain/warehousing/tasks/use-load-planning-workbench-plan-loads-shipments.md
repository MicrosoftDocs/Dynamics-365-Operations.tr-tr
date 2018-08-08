--- 
title: "Yük planlama çalışma ekranını kullanarak yükleri ve sevkiyatları planlama"
description: "Bu yordam, yük planlama çalışma alanını, bir satış siparişi için bir yükleme oluşturmada nasıl kullanacağınızı gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="2f54b-103">Yük planlama çalışma ekranını kullanarak yükleri ve sevkiyatları planlama</span><span class="sxs-lookup"><span data-stu-id="2f54b-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f54b-104">Bu yordam, yük planlama çalışma alanını, bir satış siparişi için bir yükleme oluşturmada nasıl kullanacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f54b-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="2f54b-105">Bir önkoşul olarak satış siparişi ilk oluşturacağız.</span><span class="sxs-lookup"><span data-stu-id="2f54b-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="2f54b-106">Bu yordamı ulaşım koordinatörü için günlük çalışmanın bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="2f54b-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="2f54b-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="2f54b-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="2f54b-108">Satış siparişi oluştur</span><span class="sxs-lookup"><span data-stu-id="2f54b-108">Create a sales order</span></span>
1. <span data-ttu-id="2f54b-109">Alacak hesapları > Siparişler > Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2f54b-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="2f54b-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-110">Click New.</span></span>
3. <span data-ttu-id="2f54b-111">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2f54b-112">Hesap US-004'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="2f54b-112">Select account US-004.</span></span>
5. <span data-ttu-id="2f54b-113">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-113">Click OK.</span></span>
6. <span data-ttu-id="2f54b-114">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="2f54b-115">Madde A0001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f54b-115">Select item A0001.</span></span>
    * <span data-ttu-id="2f54b-116">A0001, taşıma yönetimi için etkindir.</span><span class="sxs-lookup"><span data-stu-id="2f54b-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="2f54b-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="2f54b-118">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="2f54b-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="2f54b-119">Ambar alanına '24' yazın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="2f54b-120">Bu örnekte ambar 24'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="2f54b-120">In this example select warehouse 24.</span></span> <span data-ttu-id="2f54b-121">Bu ambar taşımacılık ve gelişmiş ambar yönetimi için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2f54b-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="2f54b-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-122">Click Save.</span></span>
12. <span data-ttu-id="2f54b-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="2f54b-124">Yeni bir yük oluştur</span><span class="sxs-lookup"><span data-stu-id="2f54b-124">Create a new load</span></span>
1. <span data-ttu-id="2f54b-125">Taşıma yönetimi > Planlama > Yük planlama çalışma ekranına gidin.</span><span class="sxs-lookup"><span data-stu-id="2f54b-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="2f54b-126">Satış vergisi satırını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="2f54b-127">Şimdi oluşturduğunuz satış siparişi için yük oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="2f54b-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="2f54b-128">Yükler satınalma siparişlerinin, transfer emirleri ve satış siparişlerinin arz ve talebine göre oluşturulabilirler</span><span class="sxs-lookup"><span data-stu-id="2f54b-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="2f54b-129">Eylem Bölmesinde, Arz ve Talep'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="2f54b-130">Yeni yüke'ye tılayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-130">Click To new load.</span></span>
5. <span data-ttu-id="2f54b-131">Şablon kimliği yükle alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2f54b-132">Yük şablonu, ağırlık ve hacim için tüm yükte geçerli olacak maksimum ölçümleri belirler.</span><span class="sxs-lookup"><span data-stu-id="2f54b-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="2f54b-133">Yük şablonu örneğin bir konteyner veya kamyonun boyutunu temsil edebilir.</span><span class="sxs-lookup"><span data-stu-id="2f54b-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="2f54b-134">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2f54b-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="2f54b-136">Yük için orana ve rota</span><span class="sxs-lookup"><span data-stu-id="2f54b-136">Rate and route the load</span></span>
1. <span data-ttu-id="2f54b-137">Oran ve rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="2f54b-138">Rota çalışma ekranı oranı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="2f54b-139">Atölye oranı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-139">Click Rate shop.</span></span>
4. <span data-ttu-id="2f54b-140">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2f54b-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="2f54b-141">Atama'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-141">Click Assign.</span></span>
6. <span data-ttu-id="2f54b-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-142">Close the page.</span></span>
7. <span data-ttu-id="2f54b-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2f54b-143">Close the page.</span></span>


