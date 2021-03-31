---
title: İş emri havuzları
description: Bu konuda Varlık Yönetimi'nde iş emri havuzlarıyla çalışma açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6154282045d8ef6da00ecc70ff67f1f9fd3dc53b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223494"
---
# <a name="work-order-pools"></a><span data-ttu-id="ce1bd-103">İş emri havuzları</span><span class="sxs-lookup"><span data-stu-id="ce1bd-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="ce1bd-104">Ortak bir şeyler içeren iş emirlerini gruplamak için iş emri havuzlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="ce1bd-105">Aşağıda, iş emri havuzları oluşturabileceğiniz şeylerle ilgili bazı örnekler yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="ce1bd-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="ce1bd-106">İş ekipleri, örneğin Bakım Ekibi, A veya Bakım Ekibi B</span><span class="sxs-lookup"><span data-stu-id="ce1bd-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="ce1bd-107">Profesyonel yetenekler, örneğin elektrikçi veya tesisatçı</span><span class="sxs-lookup"><span data-stu-id="ce1bd-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="ce1bd-108">Fiziksel yerleşimler</span><span class="sxs-lookup"><span data-stu-id="ce1bd-108">Physical locations</span></span>  

- <span data-ttu-id="ce1bd-109">Zaman planlamaları, örneğin hafta veya diğer dönemler</span><span class="sxs-lookup"><span data-stu-id="ce1bd-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="ce1bd-110">Gerektiğinde, bir iş emrini birden fazla iş emri havuzuna koyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="ce1bd-111">İş emri havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ce1bd-111">Create a work order pool</span></span>

<span data-ttu-id="ce1bd-112">**Tüm iş emri havuzları** veya **Etkin iş emri havuzları** liste sayfasında, iş emri havuzlarınızın genel görünümünü alabilir ve yeni havuzlar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="ce1bd-113">**Varlık yönetimi** > **Genel** > **İş emri havuzları** > **Tüm iş emri havuzları** veya **Etkin iş emri havuzları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="ce1bd-114">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-114">Select **New**.</span></span>

3. <span data-ttu-id="ce1bd-115">**Havuz** alanına iş emri havuzu için bir kimlik girin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="ce1bd-116">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="ce1bd-117">İş emri havuzunun etkin olduğunu belirtmek için **Etkin** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="ce1bd-118">İş emirlerinin otomatik olarak iş emri havuzundan kaldırılması için **İş emri ilişkilerini sil** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="ce1bd-119">**Yaşam döngüsü durumunu sil** alanında, iş emri yaşam döngüsü durumunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="ce1bd-120">Örneğin, bir iş emrini tamamlamaya yönelik iş emri yaşam döngüsü durumu, iş emri havuzlarının ilişkilerini otomatik olarak silecek şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="ce1bd-121">İş siparişi havuzunuza iş emirlerini hemen eklemeye başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="ce1bd-122">**İş emirleri** hızlı sekmesinde **Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="ce1bd-123">**İş emri** alanında bir iş emri seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="ce1bd-124">İlgili alanlar otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="ce1bd-125">Daha fazla iş emri eklemek için 8 ile 9. adımlar arasındaki işlemleri tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="ce1bd-126">Eklediğiniz iş emirlerinin belirli bir sırada gerçekleştirilmesi gerekiyorsa, sıralamayı belirtmek için **Sıralama düzeni** alanına **1**, **2**, **3**, vb. sayılarını girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="ce1bd-127">İş emri havuzuna dahil edilen tüm iş emirlerinin listesini görmek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde bulunan **İlgili iş emri havuzunu görüntüle** grubunda **İş emirleri**'ni seçerek **Tüm iş emirleri** liste sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="ce1bd-128">Bakım zamanlaması, zamanlanmamış iş emirleri ve zamanlanmış iş emirleri için kapasite yükünü hesaplamak ve görüntülemek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde, **İlgili iş emri havuzunu görüntüle** grubunda **Kapasite yükünü** seçerek **Kapasite yükünü hesapla** iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="ce1bd-129">Bakım zamanlaması, zamanlanmamış iş emirleri ve zamanlanmış iş emirleriyle ilgili maddeler için (yedek parçalar ve diğer gerekli maddeler) tahminleri hesaplamak ve görüntülemek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde, **İlgili iş emri havuzunu görüntüle** grubunda **Madde tahminini** seçerek **Madde tahminini hesapla** iletişim kutusunu açın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="ce1bd-130">İş emri havuzundaki iş emirleriyle ilgili satınalma taleplerinin listesini görmek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde bulunan **Tedarik** grubunda **İş emri satınalma talebi**'ni seçerek **İş emri satınalma talebi** liste sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="ce1bd-131">İş emri havuzundaki iş emirleriyle ilgili satınalma siparişlerinin listesini görmek için, Eylem bölmesindeki **İş emri havuzu** sekmesinde bulunan **Tedarik** grubunda **İş emri satınalma işlemi**'ni seçerek **İş emri satınalma işlemi** liste sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="ce1bd-132">Bir iş emri havuzu artık iş planınızla ilgili değilse, **İş emri havuzu** sayfasındaki liste görünümünde havuz için **Etkin** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="ce1bd-133">Tüm iş emri satırlarını silmek için, **İş emri ilişkilerini sil** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="ce1bd-134">Bu seçenek, örneğin, daha sonra diğer iş emirleri için kullanabileceğiniz boş bir havuz oluşturmak istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="ce1bd-135">Daha sonra yeni iş emri ilişkileri oluşturmak için iş emri havuzunu kullanmaya hazır olduğunuzda **İş emri ilişkilerini sil** seçeneğini **Hayır** olarak ayarlamayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="ce1bd-136">Aşağıdaki şekilde **İş emri havuzu** liste sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Şekil 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="ce1bd-138">İş emri havuzuna iş emri ekleme</span><span class="sxs-lookup"><span data-stu-id="ce1bd-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="ce1bd-139">Önceki bölümde açıklandığı gibi, havuzu oluştururken iş emri havuzuna iş emirleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="ce1bd-140">Ayrıca, **Tüm iş emirleri** veya **Etkin iş emirleri** listesi sayfasındaki iş emri havuzuna da iş emirleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="ce1bd-141">İş emrini seçin ve sonra Eylem bölmesinde **İş emri** sekmesinde, **Koru** grubunda **İş emri havuzu** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="ce1bd-142">Listeden iş emrini seçin ve **İş emri havuzu**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="ce1bd-143">**İş emri havuzunu koru** iletişim kutusunda, **Ekle/Kaldır** alanında, **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="ce1bd-144">**Havuz** alanında iş emri havuzunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="ce1bd-145">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-145">Select **OK**.</span></span>

6. <span data-ttu-id="ce1bd-146">Belirli bir sırada eklediğiniz iş emrini iş emri havuzuna koymak için **Tüm işemri havuzları** veya **Etkin iş emri havuzları** liste sayfasında havuzu ve ardından **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="ce1bd-147">Ardından **İş emri havuzu** sayfasında **İş emirleri** hızlı sekmesinde, havuza dahil edilen iş emirlerinin sıralama düzenini ayarlamak için **Sıralama düzeni** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="ce1bd-148">Bir iş emrini iş emri havuzundan kaldırmak için bu adımları tekrarlayın ancak adım 3'te **Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ce1bd-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]