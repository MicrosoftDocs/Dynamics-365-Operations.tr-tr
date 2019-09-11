---
title: İş emri havuzları
description: Bu konuda Varlık Yönetimi'nde iş emri havuzlarıyla çalışma açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875946"
---
# <a name="work-order-pools"></a><span data-ttu-id="69e98-103">İş emri havuzları</span><span class="sxs-lookup"><span data-stu-id="69e98-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="69e98-104">Ortak bir şeyler içeren iş emirlerini gruplamak için iş emri havuzlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="69e98-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="69e98-105">Örneğin, şunlar için bir iş emri havuzu oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="69e98-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="69e98-106">iş ekibi, örneğin Bakım Ekibi, A, Bakım Ekibi B</span><span class="sxs-lookup"><span data-stu-id="69e98-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="69e98-107">profesyonel yetenekler, örneğin elektrikçi veya tesisatçı</span><span class="sxs-lookup"><span data-stu-id="69e98-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="69e98-108">fiziksel yerleşimler</span><span class="sxs-lookup"><span data-stu-id="69e98-108">physical locations</span></span>  

- <span data-ttu-id="69e98-109">zaman planlamaları, örneğin hafta veya diğer dönemler</span><span class="sxs-lookup"><span data-stu-id="69e98-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="69e98-110">Gerekirse, bir iş emri birçok iş emri havuzuna yerleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="69e98-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="69e98-111">İş emri havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="69e98-111">Create work order pool</span></span>

<span data-ttu-id="69e98-112">**Tüm iş emri havuzlarında** veya **Etkin iş emri havuzlarında**, iş emri havuzlarınızın genel görünümünü alabilir ve yeni havuzlar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="69e98-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="69e98-113">**Varlık yönetimi** > **Genel** > **İş emri havuzları** > **Tüm iş emri havuzları** veya **Etkin iş emri havuzları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="69e98-114">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-114">Click **New**.</span></span>

3. <span data-ttu-id="69e98-115">**Havuz** alanına bir iş havuzu kodu ve **Ad** alanına bir ad ekleyin.</span><span class="sxs-lookup"><span data-stu-id="69e98-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="69e98-116">İş emri havuzunun etkin olduğunu belirtmek için **Etkin** düğmesinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="69e98-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="69e98-117">İş siparişlerinin otomatik olarak iş emri havuzundan kaldırılmasını istiyorsanız, **İş emri ilişkilerini sil** iki durumlu düğmesinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="69e98-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="69e98-118">**Yaşam döngüsü durumunu sil** alanında, iş emri yaşam döngüsü durumunu seçin.</span><span class="sxs-lookup"><span data-stu-id="69e98-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="69e98-119">Örneğin, bir iş emrini tamamlamaya yönelik iş emri yaşam döngüsü durumu, iş emri havuzlarının ilişkilerini otomatik olarak silecek şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="69e98-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="69e98-120">İş siparişi havuzunuza iş emirlerini hemen eklemeye başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="69e98-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="69e98-121">**İş emirleri** hızlı sekmesinde **Satır ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="69e98-122">**İş emri** alanında bir iş emri seçin.</span><span class="sxs-lookup"><span data-stu-id="69e98-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="69e98-123">İlgili alanlar otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="69e98-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="69e98-124">Daha fazla iş emri eklemek istiyorsanız, 7-8 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="69e98-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="69e98-125">**Sıralama düzeni** alanında, iş emirlerinin belirli bir sırada gerçekleştirilmesi gerekip gerekmediğini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="69e98-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="69e98-126">Seçili iş emirleri için belirli bir sıra belirtmek üzere 1, 2, 3 ve bu şekilde sayılar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="69e98-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="69e98-127">İş emri havuzuna dahil edilen tüm iş emirlerinin listesini görmek için **İş emirleri** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="69e98-128">Bakım zamanlaması, planlanmamış iş emirleri ve planlanan iş emirleri için kapasite yükünü hesaplamak ve görüntülemek üzere **Kapasite yükü**'nü açmak için **Kapasite yükü** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="69e98-129">Bakım zamanlaması, planlanmamış iş emirleri ve planlanan iş emirleriyle ilgili maddeler (yedek parçalar ve diğer gerekli maddeler) için tahminleri hesaplamak ve görüntülemek üzere **Madde tahmini**'ni açmak için **Madde tahmini** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="69e98-130">İş emri havuzundaki iş emirleriyle ilgili satın alma taleplerinin listesini görmek için **İş emri satınalma talebi** listesini açmak üzere **İş emri satın alma talebi** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="69e98-131">İş emri havuzundaki iş emirleriyle ilgili satın alma siparişlerinin listesini görmek için **İş emri satınalma** listesini açmak üzere **İş emri satınalma** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="69e98-132">Bir iş emri havuzu artık çalışma planınızla ilgili değilse, **İş emri havuzu** liste görünümünde bu havuz için **Etkin** onay kutusunu "Hayır" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="69e98-133">Örneğin,daha sonra diğer iş emirleri için kullanabileceğiniz boş bir havuz oluşturmak üzere tüm iş emri satırlarını silmek istiyorsanız **İş emri ilişkilerini sil** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="69e98-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="69e98-134">Daha sonra yeni iş emri ilişkileri oluşturmak için iş emri havuzunu kullanmak istiyorsanız **İş emri ilişkilerini sil** onay kutusunun işaretini kaldırmayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Şekil 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="69e98-136">İş emri havuzuna iş emri ekleme</span><span class="sxs-lookup"><span data-stu-id="69e98-136">Add work order to a work order pool</span></span>

<span data-ttu-id="69e98-137">Yukarıdaki bölümde açıklandığı gibi, havuzu oluştururken iş emri havuzuna iş emirleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="69e98-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="69e98-138">Ayrıca **Tüm iş emirleri** listelerinin birinden iş emri havuzuna iş emri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="69e98-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="69e98-139">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="69e98-140">Listeden iş emrini seçin ve **İş emri havuzu**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="69e98-141">**Ekle/kaldır** alanında "Ekle"yi seçin.</span><span class="sxs-lookup"><span data-stu-id="69e98-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="69e98-142">**Havuz** alanında iş emri havuzunu seçin.</span><span class="sxs-lookup"><span data-stu-id="69e98-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="69e98-143">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-143">Click **OK**.</span></span>

6. <span data-ttu-id="69e98-144">Bir iş emri havuzuna iş emri ekledikten sonra iş emrini havuzda belirli bir sıraya yerleştirmek isterseniz: İŞ emri havuzları liste sayfalarından birini açın, havuzu seçin ve **Düzenle**'ye tıklayın ve **İş emri havuzu** formu > **İş emirleri** hızlı sekmesi > **Sıralama düzeni** alanında havuza dahil edilen iş emirlerini sıralama düzenini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="69e98-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="69e98-145">Seçili iş emrini bir iş emri havuzundan kaldırmak isterseniz, Adım 3'te "Kaldır" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="69e98-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

