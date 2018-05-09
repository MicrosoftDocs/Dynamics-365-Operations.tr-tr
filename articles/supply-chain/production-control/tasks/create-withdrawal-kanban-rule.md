--- 
title: "Çekme kanbanı kuralı oluşturma"
description: "Bu prosedürde, yalın bir ortamda malzeme aktarılması için bir çekme kanban kuralının oluşturulmasında gerekli kurulum açıklanmıştır."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b533d1b7b0c92fd6072500f2856036f0dffb7809
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="dc633-103">Çekme kanbanı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc633-103">Create a withdrawal kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc633-104">Bu prosedürde, yalın bir ortamda malzeme aktarılması için bir çekme kanban kuralının oluşturulmasında gerekli kurulum açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="dc633-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="dc633-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="dc633-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="dc633-106">Bu prosedür, yeni veya değiştirilmiş bir malzemenin stokta yenilenmesi için hazırlık yaparken İşlem Mühendisinin veya Değer Akışı Yöneticisinin yararlanması için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="dc633-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="dc633-107">Yeni kanban kuralı oluştur</span><span class="sxs-lookup"><span data-stu-id="dc633-107">Create new kanban rule</span></span>
1. <span data-ttu-id="dc633-108">Kanban kuralları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="dc633-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="dc633-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc633-109">Click New.</span></span>
3. <span data-ttu-id="dc633-110">Tür alanından 'Çek' seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="dc633-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="dc633-111">Çekme türü, malzemelerin veya malların transfer edilmesi için kanban kurallarına yönelik kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc633-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="dc633-112">İlk plan alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="dc633-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="dc633-113">ReplenishSpeakerComponents öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dc633-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="dc633-114">Bu etkinlik, bileşenleri ambar 11'den ve konum 11'den ambar 12'ye ve konum 12'ye taşıyacak şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dc633-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="dc633-115">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="dc633-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="dc633-116">M0007 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dc633-116">Select M0007.</span></span>  
6. <span data-ttu-id="dc633-117">Sağlama süresi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dc633-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="dc633-118">Örneğin, 60.</span><span class="sxs-lookup"><span data-stu-id="dc633-118">For example, 60.</span></span>  
7. <span data-ttu-id="dc633-119">Ölçü birimi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="dc633-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="dc633-120">Örneğin, Dakikalar.</span><span class="sxs-lookup"><span data-stu-id="dc633-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="dc633-121">Kanban için miktarları ayarlama</span><span class="sxs-lookup"><span data-stu-id="dc633-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="dc633-122">Varsayılan mktarı '5' olacak şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dc633-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="dc633-123">Bu, her kanban için transfer edilecek miktardır.</span><span class="sxs-lookup"><span data-stu-id="dc633-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="dc633-124">Sabit kanban miktarı alanına '2' girin.</span><span class="sxs-lookup"><span data-stu-id="dc633-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="dc633-125">Bu, kanbanların etkin olması gereken tutardır.</span><span class="sxs-lookup"><span data-stu-id="dc633-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="dc633-126">Bu durumda, her 5 tane için 2 kanban aktarılır.</span><span class="sxs-lookup"><span data-stu-id="dc633-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="dc633-127">Uyarı sınırı minimumı alanında '1' girin.</span><span class="sxs-lookup"><span data-stu-id="dc633-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="dc633-128">Hedefte olması gereken tam kanbanların minimum tutarını izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc633-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="dc633-129">Örneğin, bu kanban tutarının genel görünümüne ilişkin kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc633-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="dc633-130">Uyarı sınırı maksimumu alanında '2' girin.</span><span class="sxs-lookup"><span data-stu-id="dc633-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="dc633-131">Hedefte olması gereken tam kanbanların maksimum tutarını izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc633-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="dc633-132">Örneğin, bu kanban tutarının genel görünümüne ilişkin kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dc633-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="dc633-133">Kanban oluştur</span><span class="sxs-lookup"><span data-stu-id="dc633-133">Create kanbans</span></span>
1. <span data-ttu-id="dc633-134">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc633-134">Click Save.</span></span>
    * <span data-ttu-id="dc633-135">Kanbanlar oluşturulmadan önce kanban kuralının kaydedilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc633-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="dc633-136">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dc633-136">Click Add.</span></span>
    * <span data-ttu-id="dc633-137">Önerilen kanban 'Yeni kanban sayısı' 2 olduğundan hiçbir etkin kanban olmadığını unutmayın. Bu, 'Sabit kanban tutarı' ile eşittir.</span><span class="sxs-lookup"><span data-stu-id="dc633-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="dc633-138">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dc633-138">Click Create.</span></span>
    * <span data-ttu-id="dc633-139">Bu da iki kanban oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc633-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="dc633-140">Bu çekme kanbanı kuralı için her 5 başına 2 kanban oluşturulduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="dc633-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="dc633-141">Bu yordamın son aşamasıdır.</span><span class="sxs-lookup"><span data-stu-id="dc633-141">This is the last step in this procedure.</span></span>  


