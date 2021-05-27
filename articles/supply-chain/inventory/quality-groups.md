---
title: Madde kalite grupları
description: Bu konu, otomatik oluşturma ve kalite emirleri oluşturmak üzere kalite ilişkilerine atanabilmeleri için ürünleri mantıksal olarak gruplamak üzere madde kalite gruplarının nasıl kullanılacağını açıklar.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022264"
---
# <a name="item-quality-groups"></a><span data-ttu-id="654d2-103">Madde kalite grupları</span><span class="sxs-lookup"><span data-stu-id="654d2-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="654d2-104">Kalite grubu, maddeler için ortak test gereksinimlerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="654d2-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="654d2-105">Bu konu, otomatik oluşturma ve kalite emirleri oluşturmak üzere kalite ilişkilerine atanabilmeleri için ürünleri mantıksal olarak gruplamak üzere madde kalite gruplarının nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="654d2-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="654d2-106">Bir kalite grubuna atanmış maddeleri veya bir maddeye atanmış kalite gruplarını ayarlamak, düzenlemek ve görüntülemek için **Stok yönetimi \> Kurulum \> Kalite grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="654d2-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="654d2-107">**Test grupları** sayfasındaki test gereksinimlerini tanımladıktan sonra, kalite emirlerini otomatik olarak oluşturmak için kurallar tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="654d2-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="654d2-108">İşlemi basitleştirmek için, kuralları her bir öğe için tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="654d2-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="654d2-109">Bunun yerine, **Kalite ilişkileri** sayfasında bir kalite grubu için kuralları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="654d2-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="654d2-110">Bir madde kalite grubu örneği</span><span class="sxs-lookup"><span data-stu-id="654d2-110">Example of an item quality group</span></span>

<span data-ttu-id="654d2-111">Üretim şirketi, gelen denetim için aynı test gereksinimlerine sahip çeşitli hammaddeler satın alıyor.</span><span class="sxs-lookup"><span data-stu-id="654d2-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="654d2-112">Bu nedenle, şirket bir kalite grubu tanımlar ve artından hammaddeler ile ilişkilendirilmiş olan madde numaralarını bu gruba atar.</span><span class="sxs-lookup"><span data-stu-id="654d2-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="654d2-113">Daha sonra aynı sınama gereksinimleri olan yeni bir hammadde türü şirket tarafından satın alınır.</span><span class="sxs-lookup"><span data-stu-id="654d2-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="654d2-114">Yeni malzeme için yeni test gereksinimleri ayarlamak yerine, şirket yeni malzeme için madde numarasını mevcut kalite grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="654d2-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="654d2-115">Aynı şirket, aynı üretim testi gereksinimlerine sahip maddeler de üretiyor ve ön sevkiyat testleri için aynı gereksinimlere sahip maddeleri sevk ediyor.</span><span class="sxs-lookup"><span data-stu-id="654d2-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="654d2-116">Bu nedenle, şirket iki ek kalite grubu tanımlıyor ve sonra her gruba ilgili madde numaralarını atıyor.</span><span class="sxs-lookup"><span data-stu-id="654d2-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="654d2-117">Kalite grubu oluşturun</span><span class="sxs-lookup"><span data-stu-id="654d2-117">Create a quality group</span></span>

<span data-ttu-id="654d2-118">Kalite grubu oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="654d2-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="654d2-119">**Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite grupları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="654d2-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="654d2-120">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="654d2-121">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="654d2-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="654d2-122">**Kalite grubu** – kalite grubu için benzersiz bir kod ya da ad girin.</span><span class="sxs-lookup"><span data-stu-id="654d2-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="654d2-123">**Açıklama** – Kalite grubunun detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="654d2-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="654d2-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="654d2-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="654d2-125">Kalite grubuna manuel olarak madde ekleme</span><span class="sxs-lookup"><span data-stu-id="654d2-125">Manually add items to a quality group</span></span>

<span data-ttu-id="654d2-126">Kalite grubuna manuel olarak madde eklemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="654d2-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="654d2-127">**Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite grupları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="654d2-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="654d2-128">Madde eklemek istediğiniz kalite grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="654d2-129">Eylem Bölmesinde, **Maddeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="654d2-130">**Kalite grubundaki maddeler** sayfasında, Eylem Bölmesi'nde, ızgaraya satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="654d2-131">Yeni satır için **Madde numarası** alanını eklemek istediğiniz madde numarasına ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="654d2-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="654d2-132">Eklenmesi gereken her ek öğe için önceki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="654d2-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="654d2-133">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="654d2-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="654d2-134">Kalite grubuna birden fazla madde ekleme</span><span class="sxs-lookup"><span data-stu-id="654d2-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="654d2-135">Kalite grubuna birden fazla madde eklemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="654d2-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="654d2-136">**Stok yönetimi \> Kurulum \> Kalite kontrol \> Kalite grupları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="654d2-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="654d2-137">Madde eklemek istediğiniz kalite grubunu oluşturun ya da seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="654d2-138">Eylem Bölmesinde, **Madde ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="654d2-139">**Sorgulama** iletişim kutusunda, eklemek istediğiniz maddeler için filtre ölçütlerini girin.</span><span class="sxs-lookup"><span data-stu-id="654d2-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="654d2-140">Örneğin, belirli bir madde grubundaki tüm maddeleri filtreleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="654d2-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="654d2-141">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-141">Select **OK**.</span></span>
1. <span data-ttu-id="654d2-142">**Madde ekle** iletişim kutusunda, bir ızgara sorgunuzla eşleşen tüm öğeleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="654d2-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="654d2-143">Sonuçları inceleyin.</span><span class="sxs-lookup"><span data-stu-id="654d2-143">Review the results.</span></span>

    <span data-ttu-id="654d2-144">Herhangi bir değişiklik yapılması gerekiyorsa, **Sorgulama** iletişim kutusuna dönmek ve sorgunuzu ayarlamak için **Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="654d2-145">Sonuçlar, eklemek istediğiniz tüm maddeleri kapsadığında, **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="654d2-146">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="654d2-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="654d2-147">Bir maddeyi bir kalite grubuyla manuel olarak ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="654d2-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="654d2-148">Bir maddeyi bir kalite grubuyla ilişkilendirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="654d2-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="654d2-149">**Stok yönetimi \> Kurulum \> Kalite kontrol \> Madde kalite grupları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="654d2-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="654d2-150">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="654d2-151">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="654d2-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="654d2-152">**Madde numarası** – Eklenecek madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="654d2-153">**Kalite grubu** – Maddeye atanacak kalite grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="654d2-154">Bir maddenin ve eklenmesi gereken kalite grubunun her ek birleşimi için önceki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="654d2-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="654d2-155">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="654d2-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="654d2-156">Serbest bırakılan ürünler sayfasından bir kalite grubunu el ile ekleme</span><span class="sxs-lookup"><span data-stu-id="654d2-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="654d2-157">**Serbest bırakılan ürünler** sayfasından bir kalite grubunu el ile eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="654d2-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="654d2-158">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="654d2-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="654d2-159">Kalite grubu atamak istediğiniz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="654d2-160">Eylem Bölmesinde, **Stok yönetimi** sekmesindeki **Kalite** grubunda **Madde kalite grupları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="654d2-161">**Kalite grubundaki maddeler** sayfasında, Eylem Bölmesi'nde, ızgaraya satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="654d2-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="654d2-162">Yeni satır için, **Kalite grubu** alanını ürüne atamak istediğiniz kalite grubuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="654d2-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="654d2-163">Ürüne atamak istediğiniz her ek kalite grubu için önceki adımı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="654d2-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="654d2-164">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="654d2-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="654d2-165">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="654d2-165">Additional resources</span></span>

- [<span data-ttu-id="654d2-166">Kalite yönetimi test gereçleri</span><span class="sxs-lookup"><span data-stu-id="654d2-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="654d2-167">Kalite yönetimi testleri</span><span class="sxs-lookup"><span data-stu-id="654d2-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="654d2-168">Kalite yönetimi test grupları</span><span class="sxs-lookup"><span data-stu-id="654d2-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="654d2-169">Kalite yönetimi test değişkenleri</span><span class="sxs-lookup"><span data-stu-id="654d2-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="654d2-170">Kalite ilişkileri</span><span class="sxs-lookup"><span data-stu-id="654d2-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
