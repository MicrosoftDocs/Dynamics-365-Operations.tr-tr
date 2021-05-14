---
title: Uygunsuzluk oluşturma ve işleme
description: Bu konu, uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmeyi açıklar.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956218"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="bb9d9-103">Uygunsuzluk oluşturma ve işleme</span><span class="sxs-lookup"><span data-stu-id="bb9d9-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb9d9-104">Bu konu, uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="bb9d9-105">Genel olarak, uygunsuzluk yönetimi bir kalite görevlisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="bb9d9-106">Önkoşul olarak, kullanılabilir bir kalite emrinizin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="bb9d9-107">(Kalite emri oluşturma hakkında bilgi edinmek için bkz. [ Malların kalitesini denetleme](inspect-quality-goods.md) .)</span><span class="sxs-lookup"><span data-stu-id="bb9d9-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="bb9d9-108">Bir kullanıcı uygunsuzluk onayını işlemeden önce  **Kullanıcılar** sayfasındaki **Kişi** alanında bir çalışanın atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="bb9d9-109">Ek olarak, kullanıcının belge notlarını kullanabilmesi için önce **Belge işlemeyi etkinleştir** seçeneğinin kullanıcı seçeneklerinde *Evet* olarak ayarlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="bb9d9-110">Uygunsuzluk oluşturma</span><span class="sxs-lookup"><span data-stu-id="bb9d9-110">Create a nonconformance</span></span>

<span data-ttu-id="bb9d9-111">Uygunsuzluk oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-112">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-113">Eylem Bölmesi'nde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="bb9d9-114">**Uygunsuzluk oluştur** iletişim kutusunda, **Sorun türü** alanında, denetleme işlemi sırasında bulunan sorunun türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="bb9d9-115">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="bb9d9-116">Bir uygunsuzluğu onaylama veya reddetme</span><span class="sxs-lookup"><span data-stu-id="bb9d9-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="bb9d9-117">Bir uygunsuzluğu onaylamak veya reddetmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-118">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-119">Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb9d9-120">Yalnızca onaylanan uygunsuzluklara düzeltme ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="bb9d9-121">Eylem Bölmesi'nde, uygunsuzluğu onaylamak için **İşlevler \> Uygunsuzluğu onayla**'yı seçin ya da reddetmek için **İşlevler \> Uygunsuzluğu reddet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="bb9d9-122">Onaylanmış uygunsuzlukları [ilgili işlemlerle](../quality-operations.md) ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="bb9d9-123">Bu şekilde, uygunsuzluk işlemenin bir parçası olarak yapılan çalışmayı ve düzeltme işleme işlemini kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="bb9d9-124">Seçiminizi onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="bb9d9-125">Devam etmek için **Eve**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="bb9d9-126">Uygunsuzluklara işlemler ve diğer ayrıntılar ekleme</span><span class="sxs-lookup"><span data-stu-id="bb9d9-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="bb9d9-127">Uygunsuzluk oluşturduktan sonra, ilgili işlemler eklemeye başlayabilir ve bu işlemlerle ilgili ek bilgiler belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="bb9d9-128">Yalnızca onaylanan uygunsuzluklara ilgili işlemler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="bb9d9-129">Temel bilgilerin yanı sıra, bir işleme aşağıdaki detayları da ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="bb9d9-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="bb9d9-130">**Öğeler** - Düzeltmeyi gerçekleştirmek için tüketilen öğelerin listesini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="bb9d9-131">Örneğin, bu öğeler tamamlanmış bir ürünün yeniden çalıştırılması için gerekli olan ekipman veya malzemeleri onarmak için gerekli ürünler olabilir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="bb9d9-132">**Kalite giderleri** – Harici kaynaklar için tahakkuk edilen veya faturalanan giderlerin listesini oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="bb9d9-133">**Zaman çizelgesi** – Her çalışanın işlemde harcadığı zamanı içeren bir günlük oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="bb9d9-134">Kalan ayarlar isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-134">The remaining settings are optional.</span></span> <span data-ttu-id="bb9d9-135">Her öğe, kalite ücreti ve zaman çizelgesinin maliyeti toplanır ve işlemde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="bb9d9-136">İşlemde **Maliyet** alanını doğrudan düzenleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="bb9d9-137">Uygunsuzluk için işlem oluşturma</span><span class="sxs-lookup"><span data-stu-id="bb9d9-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="bb9d9-138">Uygunsuzluk için bir işlem oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-139">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-140">Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb9d9-141">Yalnızca onaylanan uygunsuzluklara işlemler ekleyebilir veya güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="bb9d9-142">Eylem Bölmesi'nde, **İlgili işlemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="bb9d9-143">**İlgili işlemler** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="bb9d9-144">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="bb9d9-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="bb9d9-145">**İşlem** – Uygunsuzlukta gerçekleştirilecek işlemin kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="bb9d9-146">**Neden** – İşlemin neden gerekli olduğunu anlatan ayrıntılı bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="bb9d9-147">**Satış siparişi** – Seçilen işlem kodu satış siparişi türüyle ilişkiliyse işlemi bağladığınız satış siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="bb9d9-148">**Satınalma siparişi** – Seçilen işlem kodu satınalma siparişi türüyle ilişkiliyse işlemi bağladığınız satınalma siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="bb9d9-149">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="bb9d9-150">İşleme öğe ekleme</span><span class="sxs-lookup"><span data-stu-id="bb9d9-150">Add items to an operation</span></span>

<span data-ttu-id="bb9d9-151">Bir işleme öğeler eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-152">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-153">Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb9d9-154">Yalnızca onaylanan uygunsuzluklara işlemler ekleyebilir veya güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="bb9d9-155">Eylem Bölmesi'nde, **İlgili işlemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="bb9d9-156">**İlgili işlemler** sayfasında, öğe eklemek istediğiniz işlemi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="bb9d9-157">Eylem Bölmesinde, **Maddeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="bb9d9-158">**İlgili işlemler** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="bb9d9-159">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="bb9d9-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="bb9d9-160">**Öğe numarası** – Seçilen işlemin parçası olarak tüketilecek ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="bb9d9-161">**Miktar** – Tüketilecek öğelerin sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb9d9-162">Öğenin maliyetini **Genel** sekmesindeki **Maliyet** alanında görüntüleyebilirsiniz . Gösterilen maliyet, **Serbest bırakılan ürün** sayfasında ayarlanan maliyetten alınır.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="bb9d9-163">Maliyet, **İlgili işlem öğesi** sayfasında doğrudan güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="bb9d9-164">**İlgili operasyon maddeleri** sayfasına eklenen tüm öğelerin maliyeti, **İlgili operasyonlar** sayfasındaki **Maliyet** alanına otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="bb9d9-165">Eklemeniz gereken her ek öğe için önceki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="bb9d9-166">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="bb9d9-167">Bir işleme kalite giderleri ekleme</span><span class="sxs-lookup"><span data-stu-id="bb9d9-167">Add quality charges to an operation</span></span>

<span data-ttu-id="bb9d9-168">Bir işleme kalite giderleri eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-169">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-170">Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb9d9-171">Yalnızca onaylanan uygunsuzluklara işlemler ekleyebilir veya güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="bb9d9-172">Eylem Bölmesi'nde, **İlgili işlemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="bb9d9-173">**İlgili işlemler** sayfasında, kalite giderleri eklemek istediğiniz işlemi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="bb9d9-174">Eylem Bölmesi'nde, **Kalite giderleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="bb9d9-175">**İlgili işlem giderleri** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="bb9d9-176">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="bb9d9-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="bb9d9-177">**Gider kodu** – Eklemek istediğiniz kalite giderini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="bb9d9-178">**Açıklama**: Gider grubunun detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="bb9d9-179">**Gider değeri** – Gider tutarını girin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="bb9d9-180">Eklemeniz gereken her ek gider için önceki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="bb9d9-181">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="bb9d9-182">**Gider değeri** alanındaki tutar tüm kalite gideri için otomatik olarak toplanır ve **İlgili işlemler** sayfasındaki **Maliyet** alanındaki diğer tüm tutarlara eklenir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="bb9d9-183">Bir işlemde zaman çizelgesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bb9d9-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="bb9d9-184">Bir işleme zaman çizelgesi eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-185">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-186">Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb9d9-187">Yalnızca onaylanan uygunsuzluklara işlemler ekleyebilir veya güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="bb9d9-188">Eylem Bölmesi'nde, **İlgili işlemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="bb9d9-189">**İlgili işlemler** sayfasında, zaman çizelgesi eklemek istediğiniz işlemi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="bb9d9-190">Eylem Bölmesi'nde **Zaman çizelgesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="bb9d9-191">**İlgili işlem zaman çizelgeleri** sayfasında, Eylem Bölmesi'nde, kılavuza satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="bb9d9-192">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="bb9d9-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="bb9d9-193">**Tarih** – Çalışmanın yapıldığı tarihi belirtin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="bb9d9-194">Varsayılan olarak bu alan şu anki tarihe ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="bb9d9-195">**Çalışan** – Çalışmayı gerçekleştiren çalışanı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="bb9d9-196">Varsayılan olarak, bu alan geçerli kullanıcıya atanan çalışana ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="bb9d9-197">**İşlem saatleri** – Seçili işleme harcanan saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="bb9d9-198">**Faturalanan** – Ayrılan süre faturada bir müşteriye veya satıcıya faturalanmışsa bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb9d9-199">Maliyeti, **Genel** sekmesindeki **Maliyet** alanında görüntüleyebilirsiniz. Maliyet, **Stok yönetimi parametreleri** sayfasında tanımladığınız oran kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="bb9d9-200">Eklemeniz gereken her ek zaman çizelgesi satırı için önceki adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="bb9d9-201">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="bb9d9-202">**Gider** alanındaki tutar tüm zaman çizelgesi satırları için toplanır ve **İlgili işlemler** sayfasındaki **Maliyet** alanındaki diğer tüm tutarlara eklenir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="bb9d9-203">Bir uygunsuzluğa düzeltme ekleme</span><span class="sxs-lookup"><span data-stu-id="bb9d9-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="bb9d9-204">Bir uygunsuzluğa düzeltme eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-205">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-206">Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb9d9-207">Yalnızca onaylanan uygunsuzluklara düzeltme ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="bb9d9-208">Eylem Bölmesi'nde, **Düzeltmeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="bb9d9-209">Eylem Bölmesinde, **Düzeltmeler** sayfasında ızgaraya satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="bb9d9-210">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="bb9d9-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="bb9d9-211">**Tanılama** – Oluşturmakta olduğunuz düzeltme türünü belirten tanılama türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="bb9d9-212">**Çalışan** – Düzeltmeden sorumlu kişiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="bb9d9-213">**Düzeltme önceliği** – Düzeltmenin nasıl önceliklendirilmesi gerektiğini ( *Düşük*, *Normal* veya *Yüksek*) belirtmek için bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="bb9d9-214">**Talep edilen tarih** – Düzeltici eylemin talep edildiği tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="bb9d9-215">**Planlanan tarih** – Düzeltmenin tamamlanması beklenen tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="bb9d9-216">**Kısa vadeli çözüm** – Düzeltici eylem uygunsuzluğu yalnızca kısa bir süre için düzelttiyse bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="bb9d9-217">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="bb9d9-218">Düzeltmeyi tamamlandı olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="bb9d9-218">Mark a correction as completed</span></span>

<span data-ttu-id="bb9d9-219">Bir uygunsuzluk düzeltmesini tamamlandı olarak işaretlemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-220">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-221">Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bb9d9-222">Yalnızca onaylanan uygunsuzluklara düzeltme ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="bb9d9-223">Eylem Bölmesi'nde, **Düzeltmeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="bb9d9-224">**Düzeltmeler** sayfasında, ızgarada, tamamlandı olarak işaretlemek istediğiniz düzeltmeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="bb9d9-225">Eylem Bölmesinde, **Tamamlandı olarak işaretle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="bb9d9-226">Seçiminizi onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="bb9d9-227">Devam etmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-227">Select **OK** to continue.</span></span> <span data-ttu-id="bb9d9-228">**Tamamlanma tarihi ve saati** alanı, geçerli tarih ve saate ayarlanır ve **Tamamlandı** onay kutusu işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="bb9d9-229">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="bb9d9-230">Tamamlanmış bir düzeltmeyi yeniden açma</span><span class="sxs-lookup"><span data-stu-id="bb9d9-230">Reopen a completed correction</span></span>

<span data-ttu-id="bb9d9-231">Tamamlanan bir düzeltmeyi yeniden açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-232">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Uygunsuzluklar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-233">Listede, güncelleştirmek istediğiniz uygunsuzluğu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="bb9d9-234">Eylem Bölmesi'nde, **Düzeltmeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="bb9d9-235">**Düzeltmeler** sayfasında, ızgarada, yeniden açmak istediğiniz düzeltmeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="bb9d9-236">Eylem Bölmesi'nde, **Yeniden aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="bb9d9-237">Seçiminizi onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="bb9d9-238">Devam etmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-238">Select **OK** to continue.</span></span> <span data-ttu-id="bb9d9-239">Değer, **Tamamlanma tarihi ve saati** alanından silinir ve **Tamamlandı** onay kutusu temizlenir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="bb9d9-240">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-240">Close the page.</span></span>

<span data-ttu-id="bb9d9-241">Artık düzeltmeye ek düzenlemeler veya güncelleştirmeler yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="bb9d9-242">İşinizi bitirdiğinizde düzeltmeyi yeniden tamamlandı olarak işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="bb9d9-243">Bir uygunsuzluğu kapat</span><span class="sxs-lookup"><span data-stu-id="bb9d9-243">Close a nonconformance</span></span>

<span data-ttu-id="bb9d9-244">Uygunsuzluğu kapatmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="bb9d9-245">**Stok yönetimi \> Periyodik görevler \> Kalite yönetimi \> Kalite emirleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="bb9d9-246">Izgarada bir kalite emri seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="bb9d9-247">Eylem Bölmesi'nde, **Sorgular \> Uygunsuzluklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="bb9d9-248">**Uygunsuzluklar** sayfasında, ızgaradaki hedef uygunsuzluğu seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="bb9d9-249">Eylem Bölmesi'nde, **İşlevler \> Uygunsuzluğu kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="bb9d9-250">Seçiminizi onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="bb9d9-251">Devam etmek için **Eve**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="bb9d9-252">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="bb9d9-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb9d9-253">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bb9d9-253">Additional resources</span></span>

- [<span data-ttu-id="bb9d9-254">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="bb9d9-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="bb9d9-255">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="bb9d9-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="bb9d9-256">Uygunsuzlukları onaylamaktan sorumlu çalışanlar</span><span class="sxs-lookup"><span data-stu-id="bb9d9-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="bb9d9-257">Uygunsuzluklar için karantina bölgeleri</span><span class="sxs-lookup"><span data-stu-id="bb9d9-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="bb9d9-258">Uygunsuzluklar için tanılama türleri</span><span class="sxs-lookup"><span data-stu-id="bb9d9-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="bb9d9-259">Uygunsuzluklar için kalite masrafları</span><span class="sxs-lookup"><span data-stu-id="bb9d9-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="bb9d9-260">Uygunsuzluklar için işlemler</span><span class="sxs-lookup"><span data-stu-id="bb9d9-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="bb9d9-261">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="bb9d9-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
