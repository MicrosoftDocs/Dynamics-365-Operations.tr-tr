---
title: Satınalma siparişleri için iş şablonunu ayarlama
description: Bu yordam, alınan ürünler yerine koyulurken kullanılacak basit bir iş şablonunun nasıl ayarlanacağına odaklanır.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d737f9dfd1888602266a87853e54407618ae2781
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558331"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="93c67-103">Satınalma siparişleri için iş şablonunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="93c67-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93c67-104">Bu yordam, alınan ürünler yerine koyulurken kullanılacak basit bir iş şablonunun nasıl ayarlanacağına odaklanır.</span><span class="sxs-lookup"><span data-stu-id="93c67-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="93c67-105">İş şablonları, ürünler teslim alma alanından taşınırken bir mobil cihazda ambara yönelik yönergeler kümesini belirler.</span><span class="sxs-lookup"><span data-stu-id="93c67-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="93c67-106">Bu yordamı, USMF demo verileri şirketinde söz edilen verilerle kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93c67-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="93c67-107">Bu kılavuzu başlatmadan önce bir iş havuzu kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="93c67-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="93c67-108">Bu örnekte Gelen içinde bir iş havuzu kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="93c67-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="93c67-109">Bu yordam ambar yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="93c67-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="93c67-110">Ambar yönetimi > Kurulum > İş > İş şablonları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="93c67-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="93c67-111">İş siparişi türü alanında "Satınalma siparişi"ni seçin.</span><span class="sxs-lookup"><span data-stu-id="93c67-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="93c67-112">İş şablonu başlığı oluşturma</span><span class="sxs-lookup"><span data-stu-id="93c67-112">Create a work template header</span></span>
1. <span data-ttu-id="93c67-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93c67-113">Click New.</span></span>
2. <span data-ttu-id="93c67-114">Sıra numarası alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="93c67-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="93c67-115">Bu, iş şablonlarının değerlendirileceği sıradır.</span><span class="sxs-lookup"><span data-stu-id="93c67-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="93c67-116">Gerekirse sırada değişiklik yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93c67-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="93c67-117">İş şablonu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="93c67-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="93c67-118">Bu, şablon için benzersiz tanımlayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="93c67-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="93c67-119">İş şablonu açıklaması alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="93c67-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="93c67-120">Geçerli seçeneği, şablon için gereken tüm bilgiler tamamlanana ve sonra Kaydet tıklatılana kadar işaretlenmez.</span><span class="sxs-lookup"><span data-stu-id="93c67-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="93c67-121">Satınalma siparişi türünün iş emri otomatik olarak işlenemez, bu nedenle Otomatik olarak işleme koy seçeneğini Hayır olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="93c67-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="93c67-122">İş havuzu kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="93c67-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="93c67-123">İş havuzu kodları, işi gruplar halinde düzenlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="93c67-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="93c67-124">Burada belirlediğiniz değer, bu şablon kullanılarak oluşturulan herhangi bir iş için varsayılan değer olacaktır.</span><span class="sxs-lookup"><span data-stu-id="93c67-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="93c67-125">İş önceliği alanında '1' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="93c67-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="93c67-126">Bu, işin önemini gösterir ve burada belirlediğiniz değer bu şablon kullanılarak oluşturulan herhangi bir iş için varsayılan değer olur.</span><span class="sxs-lookup"><span data-stu-id="93c67-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="93c67-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93c67-127">Click Save.</span></span>
    * <span data-ttu-id="93c67-128">Sorguyu Düzenle düğmesi kullanılabilir olmadan önce iş şablonu başlığını kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="93c67-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="93c67-129">İş şablonu sorgusunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="93c67-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="93c67-130">Sorguyu düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93c67-130">Click Edit query.</span></span>
    * <span data-ttu-id="93c67-131">Şablonun yalnızca belirli bir ambarın içinde kullanılabileceği şekilde bir sınırlama ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="93c67-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="93c67-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93c67-132">Click Add.</span></span>
3. <span data-ttu-id="93c67-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="93c67-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="93c67-134">Alan alanında 'ambar' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="93c67-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="93c67-135">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="93c67-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="93c67-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93c67-136">Click OK.</span></span>
7. <span data-ttu-id="93c67-137">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93c67-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="93c67-138">İş şablonu ayrıntılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="93c67-138">Set work template details</span></span>
1. <span data-ttu-id="93c67-139">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93c67-139">Click New.</span></span>
2. <span data-ttu-id="93c67-140">İş türü alanında 'Malzeme çekme öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="93c67-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="93c67-141">İş sınıfı kodu alanında 'satınalma' değerini girin.</span><span class="sxs-lookup"><span data-stu-id="93c67-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="93c67-142">Burada ayarladığınız çalışma sınıfı, bu şablon kullanılarak oluşturulan Malzeme çekme türündeki tüm iş satırlarında varsayılan olacaktır.</span><span class="sxs-lookup"><span data-stu-id="93c67-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="93c67-143">İş sınıfı, iş siparişi satırlarından değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="93c67-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="93c67-144">İş sınıfları, ambar çalışanı tarafından bir mobil cihazda işlenebilecek iş emri satırlarının türünü yönetmek ve/veya sınırlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="93c67-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="93c67-145">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93c67-145">Click New.</span></span>
5. <span data-ttu-id="93c67-146">İş türü alanında, 'Yerine koyma'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="93c67-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="93c67-147">İş sınıfı kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="93c67-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="93c67-148">Malzeme çekme ve yerine koyma yönergeleri bir kümedir.</span><span class="sxs-lookup"><span data-stu-id="93c67-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="93c67-149">Her bir malzeme çekme/yerine koyma çifti aynı iş sınıfında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="93c67-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="93c67-150">Malzeme çekme yönergesi için sağladığınız aynı iş sınıfını kullanın.</span><span class="sxs-lookup"><span data-stu-id="93c67-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="93c67-151">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93c67-151">Click Save.</span></span>
    * <span data-ttu-id="93c67-152">Geçerli onay kutusunun işaretli olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="93c67-152">Note that the Valid checkbox is now checked.</span></span>  

