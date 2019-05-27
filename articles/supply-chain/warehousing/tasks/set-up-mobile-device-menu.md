---
title: Satınalma siparişi iş türünü tamamlamak için bir mobil cihaz menü öğesi ayarlama
description: Bu yordam bir Mobil cihaz menü öğesinin nasıl kurulacağını gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFAutoConfirm, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 326a0039d2769ee5f459a87c302c93604d2379aa
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545891"
---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order"></a><span data-ttu-id="3449f-103">Satınalma siparişi iş türünü tamamlamak için bir mobil cihaz menü öğesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="3449f-103">Set up a mobile device menu item for completing work of type Purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3449f-104">Bu yordam bir Mobil cihaz menü öğesinin nasıl kurulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3449f-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="3449f-105">Bu örnekte, menü öğesi Satın alma siparişi türünde işi yapan için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3449f-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="3449f-106">Menü öğesiyle ilişkili iş sınıfı, hangi işin geçerli olduğunu belirler.</span><span class="sxs-lookup"><span data-stu-id="3449f-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="3449f-107">Bu kılavuzu USMF demo şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3449f-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="3449f-108">Bu yordam genel olarak bir depo yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="3449f-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="3449f-109">Mobil cihaz menü öğesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="3449f-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="3449f-110">Mobil cihaz menü öğelerine gidin.</span><span class="sxs-lookup"><span data-stu-id="3449f-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="3449f-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3449f-111">Click New.</span></span>
3. <span data-ttu-id="3449f-112">Menü öğesi adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3449f-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="3449f-113">Özgün bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3449f-113">Enter a unique value.</span></span> <span data-ttu-id="3449f-114">Örneğin, POMove yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3449f-114">For example, you could type POMove.</span></span> <span data-ttu-id="3449f-115">Değeri unutmayın, daha sonra ihtiyacınız olacak.</span><span class="sxs-lookup"><span data-stu-id="3449f-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="3449f-116">Başlık alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3449f-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="3449f-117">Bu, mobil cihazda görüntülenen başlıktır.</span><span class="sxs-lookup"><span data-stu-id="3449f-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="3449f-118">Örneğin, PO Move yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3449f-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="3449f-119">Mod alanında, 'İş' seçin.</span><span class="sxs-lookup"><span data-stu-id="3449f-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="3449f-120">Mevcut işi kullan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3449f-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="3449f-121">Bu mobil cihaz menü öğesi varolan işi gerçekleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3449f-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="3449f-122">Bu nedenle, bu değeri Evet olarak ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3449f-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="3449f-123">Stok durumunu görüntüle alanı eldeki stoğun stok durumunun mobil cihazda ambar çalışanına görüntülenip görüntülenmeyeceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="3449f-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="3449f-124">Yöneten alanında 'Sistem gruplandırma' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3449f-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="3449f-125">Yöneten alanında bir seçim yaptığınızda, bu sayfadaki Genel bölümünde ek alanlar belirir.</span><span class="sxs-lookup"><span data-stu-id="3449f-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="3449f-126">Beliren alanlar yaptığınız seçime bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3449f-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="3449f-127">Sistem gruplaması seçtiğinizde iki yeni alan eklenir.</span><span class="sxs-lookup"><span data-stu-id="3449f-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="3449f-128">Bunlar aşağıda açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3449f-128">These are explained below.</span></span>  
8. <span data-ttu-id="3449f-129">Sistem gruplama alanında 'WorkPoolId' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3449f-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="3449f-130">Ambar çalışanları bu menü öğesini açtıklarında bir İş havuzu kodunu taramaları istenir.</span><span class="sxs-lookup"><span data-stu-id="3449f-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="3449f-131">Bu İş havuzu koduna sahip tüm iş emirleri ve bu menü öğesine eklenen iş sınıflarından birinin bulunduğu açık iş emri satırları kullanıcıya gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3449f-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="3449f-132">Sistem gruplandırma etiketi alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3449f-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="3449f-133">Bu, mobil cihazda kullanıcıya görüntülenen metindir.</span><span class="sxs-lookup"><span data-stu-id="3449f-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="3449f-134">Örneğin, İş havuzu yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3449f-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="3449f-135">Yerine koyma sırasında plakayı geçersiz kıl için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3449f-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="3449f-136">Bu seçenek maddeler plaka denetimli bir yerleşime bırakıldığında ambar çalışanlarının hedef plakayı geçersiz kılmalarına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3449f-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="3449f-137">Grup yerine koyma alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3449f-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="3449f-138">İş emrindeki tüm Yerine koyma satırları aynı yerleşimi paylaşıyorsa kullanıcı tüm satırlar için birleştirilmiş tek bir Yerine koy yönergesi alır.</span><span class="sxs-lookup"><span data-stu-id="3449f-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="3449f-139">Denetim şablonu kodu: İş denetimi şablonu bir menü öğesinin iş sürecinin başka bir işlem gerçekleştirebilmek üzere kesilip kesilmeyeceğini belirtmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="3449f-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="3449f-140">Örneğin, bu menü öğesi gelen iş içinse, denetim şablonu çalışanın sıcaklığı denetlemesini gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="3449f-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="3449f-141">Sürecin kesintiye uğradığı nokta denetim şablonunda belirtilir ve örneğin, iş başladığında veya tamamlandığında veya durumu değiştiğinde.</span><span class="sxs-lookup"><span data-stu-id="3449f-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="3449f-142">İş sınıfları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3449f-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="3449f-143">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3449f-143">Click New.</span></span>
14. <span data-ttu-id="3449f-144">İş sınıfı kimliği alanında 'Satınalma' yazın.</span><span class="sxs-lookup"><span data-stu-id="3449f-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="3449f-145">İş havuzu menü öğesinin kullanılabileceği işi kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="3449f-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="3449f-146">Bu durumda, Satınalma iş sınıfı koduna sahip iş emri satırlarını açmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3449f-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="3449f-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3449f-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="3449f-148">İş onayı kurulumu</span><span class="sxs-lookup"><span data-stu-id="3449f-148">Set up work confirmation</span></span>
1. <span data-ttu-id="3449f-149">İş onayı kurulumu'nu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3449f-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="3449f-150">İş türü alanında 'Malzeme çekme öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3449f-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="3449f-151">Otomatik onayla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3449f-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="3449f-152">Çekme iş türüne sahip çalışma yönergesi otomatik olarak onaylanır.</span><span class="sxs-lookup"><span data-stu-id="3449f-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="3449f-153">Bu yönerge kullanıcıya sunulmaz.</span><span class="sxs-lookup"><span data-stu-id="3449f-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="3449f-154">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3449f-154">Click New.</span></span>
5. <span data-ttu-id="3449f-155">İş türü alanında, 'Yerine koyma'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3449f-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="3449f-156">Konum onayı onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3449f-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="3449f-157">Madde bırakıldığında ambar çalışanından yerleşim için bir onay taraması gerçekleştirmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="3449f-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="3449f-158">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3449f-158">Click Save.</span></span>
8. <span data-ttu-id="3449f-159">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3449f-159">Close the page.</span></span>
9. <span data-ttu-id="3449f-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3449f-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="3449f-161">Mobil cihaz menüsüne menü öğesi ekleme</span><span class="sxs-lookup"><span data-stu-id="3449f-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="3449f-162">Mobil cihaz menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="3449f-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="3449f-163">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3449f-163">Click Edit.</span></span>
3. <span data-ttu-id="3449f-164">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="3449f-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3449f-165">Örneğin, İsim alanı üzerinde 'gelen' değerini girerek filtreleme yapın.</span><span class="sxs-lookup"><span data-stu-id="3449f-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="3449f-166">Gelen menü öğeleri için kullandığınız menüyü bulmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="3449f-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="3449f-167">USMF'de bu Gelen olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="3449f-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="3449f-168">Ağaçta, 'bir değer' seçin.</span><span class="sxs-lookup"><span data-stu-id="3449f-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="3449f-169">Sağ tarafı gösteren oku tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3449f-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="3449f-170">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3449f-170">Click Save.</span></span>
7. <span data-ttu-id="3449f-171">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3449f-171">Close the page.</span></span>

