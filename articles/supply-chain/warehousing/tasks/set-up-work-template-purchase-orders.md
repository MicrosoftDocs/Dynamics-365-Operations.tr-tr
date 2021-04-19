---
title: Satın alma siparişleri için iş şablonunu ayarlama
description: Bu konu, alınan ürünler yerine koyulurken kullanılacak basit bir iş şablonunun nasıl ayarlanacağını açıklar.
author: ShylaThompson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e79c4e1810cf095a342a370018190fd0d587c15
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817305"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="3e6a6-103">Satın alma siparişleri için iş şablonunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="3e6a6-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3e6a6-104">Bu konu, alınan ürünler yerine koyulurken kullanılacak basit bir iş şablonunun nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="3e6a6-105">İş şablonları, ürünler teslim alma alanından taşınırken bir mobil cihazda ambara yönelik yönergeler kümesini belirler.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="3e6a6-106">Bu yordamı, USMF demo verileri şirketinde söz edilen verilerle kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="3e6a6-107">Bu kılavuzu başlatmadan önce bir iş havuzu kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="3e6a6-108">Bu örnekte Gelen içinde bir iş havuzu kodu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="3e6a6-109">Bu yordam ambar yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="3e6a6-110">Gezinti bölmesinde **Modüller > Ambar yönetimi > Kurulum > İş > İş şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="3e6a6-111">**İş siparişi türü** alanında **Satınalma siparişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="3e6a6-112">İş şablonu başlığı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3e6a6-112">Create a work template header</span></span>
1. <span data-ttu-id="3e6a6-113">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-113">Select **New**.</span></span>
2. <span data-ttu-id="3e6a6-114">**Sıra numarası** alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="3e6a6-115">Bu, iş şablonlarının değerlendirileceği sıradır.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="3e6a6-116">Gerekirse sırada değişiklik yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="3e6a6-117">**İş şablonu** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="3e6a6-118">Bu, şablon için benzersiz tanımlayıcıdır.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="3e6a6-119">**İş şablonu açıklaması** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="3e6a6-120">**Geçerli** seçeneği, şablon için gereken tüm bilgiler tamamlanana ve sonra **Kaydet** seçilene kadar işaretlenmez.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="3e6a6-121">**Satınalma siparişi** türünün iş emri otomatik olarak işlenemez, bu nedenle **Otomatik olarak işleme koy** seçenek kümesini **Hayır** olarak bırakın.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="3e6a6-122">**İş havuzu kodu** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="3e6a6-123">İş havuzu kodları, işi gruplar halinde düzenlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="3e6a6-124">Burada belirlediğiniz değer, bu şablon kullanılarak oluşturulan herhangi bir iş için varsayılan değer olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="3e6a6-125">**İş önceliği** alanında `1` değerini girin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="3e6a6-126">Bu, işin önemini gösterir ve burada belirlediğiniz değer bu şablon kullanılarak oluşturulan herhangi bir iş için varsayılan değer olur.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="3e6a6-127">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-127">Select **Save**.</span></span> <span data-ttu-id="3e6a6-128">**Sorguyu Düzenle** düğmesi kullanılabilir olmadan önce iş şablonu başlığını kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="3e6a6-129">İş şablonu sorgusunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="3e6a6-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="3e6a6-130">**Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-130">Select **Edit query**.</span></span> <span data-ttu-id="3e6a6-131">Şablonun yalnızca belirli bir ambarın içinde kullanılabileceği şekilde bir sınırlama ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="3e6a6-132">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-132">Select **Add**.</span></span>
3. <span data-ttu-id="3e6a6-133">Yeni satırın **Alan** alanında, `warehouse` yazın.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="3e6a6-134">**Ölçütler** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="3e6a6-135">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-135">Select **OK**.</span></span>
6. <span data-ttu-id="3e6a6-136">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="3e6a6-137">İş şablonu ayrıntılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="3e6a6-137">Set work template details</span></span>
1. <span data-ttu-id="3e6a6-138">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-138">Select **New**.</span></span>
2. <span data-ttu-id="3e6a6-139">**İş türü** alanında **Malzeme çekme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="3e6a6-140">**İş sınıfı kodu** alanında `purchase` değerini girin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="3e6a6-141">Burada ayarladığınız çalışma sınıfı, bu şablon kullanılarak oluşturulan Malzeme çekme türündeki tüm iş satırlarında varsayılan olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="3e6a6-142">İş sınıfı, iş siparişi satırlarından değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="3e6a6-143">İş sınıfları, ambar çalışanı tarafından bir mobil cihazda işlenebilecek iş emri satırlarının türünü yönetmek ve/veya sınırlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="3e6a6-144">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-144">Select **New**.</span></span>
5. <span data-ttu-id="3e6a6-145">**İş türü** alanında, **Yerine koyma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="3e6a6-146">**İş sınıfı kodu** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="3e6a6-147">Malzeme çekme ve yerine koyma yönergeleri bir kümedir.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="3e6a6-148">Her bir malzeme çekme/yerine koyma çifti aynı iş sınıfında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="3e6a6-149">Malzeme çekme yönergesi için sağladığınız aynı iş sınıfını kullanın.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="3e6a6-150">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-150">Select **Save**.</span></span> <span data-ttu-id="3e6a6-151">**Geçerli** onay kutusunun işaretli olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="3e6a6-151">Note that the **Valid** checkbox is now checked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]