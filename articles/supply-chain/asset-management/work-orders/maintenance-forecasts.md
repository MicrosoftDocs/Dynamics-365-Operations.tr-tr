---
title: Bakım tahminleri
description: Bu konuda Varlık Yönetimi'nde bakım tahminleri açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6428981fcf560c541634d9466695be7bce4cb453
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888965"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="0ee8b-103">Bakım tahminleri</span><span class="sxs-lookup"><span data-stu-id="0ee8b-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0ee8b-104">Bir iş emri oluşturduğunuzda, ilgili varlıklar ve bakım işi türleri bulunan iş emri işleri oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="0ee8b-105">Bakım tahminlerini içeren bir bakım işi türü seçtiğinizde, tahminler otomatik olarak iş emrine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="0ee8b-106">Bir iş emrine tahmin satırları ekleyebilir veya bunları bir iş emrinden silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="0ee8b-107">Bir iş emri yaşam döngüsü durumu, ilgili proje türü ve proje türüyle ilgili aşama kuralları kurulumu, tahmin satırları ekleyip ekleyemeyeceğinizi veya düzenleyip düzenleyemeyeceğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="0ee8b-108">İş emri yaşam döngüsü durumları ve ilgili proje aşamaları hakkında daha fazla bilgi için bkz. [Tahminler, iş emirleri ve projeler](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="0ee8b-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="0ee8b-109">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0ee8b-110">Listede iş emrini seçin ve sonra Eylem bölmesinde > **İş emri** sekmesinde > **Proje** grubunda **Tahmin** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="0ee8b-111">**İş emri bakım tahmini** sayfasında, iş emri işinde seçilen bakım işi türünden gelen tahmin satırları görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="0ee8b-112">İş emrine saat tahmini ekleme</span><span class="sxs-lookup"><span data-stu-id="0ee8b-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="0ee8b-113">**İş emri bakım tahmini** sayfasında, tahmin eklenecek iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="0ee8b-114">**Saatler** hızlı sekmesinde yeni bir satır oluşturmak için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="0ee8b-115">**Kategori** alanında bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="0ee8b-116">**Saat** alanına tahmini saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="0ee8b-117">**Satır özelliği** alanında, satırda kullanılması gereken masraf türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="0ee8b-118">İş emrine madde tahmini ekleme</span><span class="sxs-lookup"><span data-stu-id="0ee8b-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="0ee8b-119">Bir iş emri bakım tahminine madde eklemenin üç yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="0ee8b-120">Yedek parça listesi veya varlık ürün reçetesine (BOM) dahil edilmeyen maddeler (yedek parçalar) için satırlar oluşturabilir, onaylanan yedek parçalar listesinden yedek parçalar seçebilir veya maddeleri Varlık ürün reçetesinden seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="0ee8b-121">**İş emri bakım tahmini** sayfasında, tahmin eklenecek iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-121">On the **Work order maintenance forecast** page, select the work order job to to add a forecast to.</span></span>

- <span data-ttu-id="0ee8b-122">**Maddeler** hızlı sekmesinde, uygun yöntemi kullanarak bakım tahminine maddeler ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="0ee8b-123">Yedek parçalar listesi veya varlık ürün reçetesinde bulunmayan bir yedek parça için yeni bir satır oluşturmak üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="0ee8b-124">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-124">Select **Add**.</span></span>
2. <span data-ttu-id="0ee8b-125">**Madde numarası** alanında maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="0ee8b-126">**Satış miktarı** alanına miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="0ee8b-127">**Birim** alanında, miktar için ölçü birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="0ee8b-128">**Maliyet fiyatı** ve **Para birimi** alanlarına ilgili değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="0ee8b-129">**Satır özelliği** alanında bir satır özelliği seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="0ee8b-130">Madde satırlarında görüntülenen boyutların listesini değiştirmek için **Stok** > **Boyutları görüntüle**'yi seçin, boyutları seçin ve ardından **Kurulumu kaydet** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="0ee8b-131">Onaylı bir yedek parça listesinden yedek parça eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="0ee8b-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="0ee8b-132">**Yedek parça ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="0ee8b-133">Yedek parçayı seçin ve gerek duyduğunuz gibi ilgili bilgileri düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="0ee8b-134">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-134">Select **OK**.</span></span>

<span data-ttu-id="0ee8b-135">Varlık ürün reçetesinden bir madde eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="0ee8b-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="0ee8b-136">**Ürün reçetesi maddeleri ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="0ee8b-137">Maddeyi seçin ve gerek duyduğunuz gibi ilgili bilgileri düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="0ee8b-138">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-138">Select **OK**.</span></span>

<span data-ttu-id="0ee8b-139">Seçilen satırdaki maddenin Varlık Yönetiminde varlıklar, bakım işi türü varsayılanları, yedek parçalar ve iş emirleriyle ilişkili olarak nerede kullanıldığıyla ilgili genel bir bakış edinmek için **Maddenin kullanıldığı yer**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="0ee8b-140">Bu genel bakış hakkında daha fazla bilgi için bkz. [Maddenin kullanıldığı yer](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="0ee8b-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="0ee8b-141">İş emrine gider tahmini ekleme</span><span class="sxs-lookup"><span data-stu-id="0ee8b-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="0ee8b-142">**İş emri bakım tahmini** sayfasında, tahmin eklenecek iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="0ee8b-143">**Gider** hızlı sekmesinde satır oluşturmak için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="0ee8b-144">**Kategori** alanında bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="0ee8b-145">**Miktar** alanına miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="0ee8b-146">**Maliyet fiyatı**, **Satış para birimi** ve **Satış fiyatı** alanlarına uygun değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="0ee8b-147">**Satır özelliği** alanında, satırda kullanılması gereken masraf türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="0ee8b-148">**Bakım tahmini toplamları** hızlı sekmesi, seçili iş emri işi ve iş emri için her hızlı sekmede oluşturulan satır sayısının genel görünümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="0ee8b-149">Ayrıca, iş emri işi ve iş emri için tahmin edilen çalışma saatlerinin toplamını da gösterir.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="0ee8b-150">Aşağıdaki şekilde **İş emri bakım bakım tahmini** sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Şekil 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="0ee8b-152">İş emri tahminlerini otomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="0ee8b-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="0ee8b-153">Microsoft Dynamics 365 for Finance and Operations'daki diğer modüllerde saat maliyetleri, madde maliyetleri ve giderler güncelleştirilirse Varlık Yönetimindeki iş emri tahminleri bu değişiklikleri yansıtacak şekilde otomatik olarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="0ee8b-154">Bu özellik, en son maliyet fiyatlarının iş emri tahminlerinde her zaman kullanılmasını sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="0ee8b-155">[Bakım işi türü tahminlerinde](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) de benzer güncelleştirmeler yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="0ee8b-156">**Varlık yönetimi** > **Periyodik** > **Tahmin** > **İş emri tahminini güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="0ee8b-157">**İş emri tahminini güncelleştir** iletişim kutusunda, **Dahil edilecek kayıtlar** hızlı sekmesinde gerekirse, belirli iş emirleri veya iş emri işleriyle ilgili seçimler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="0ee8b-158">İlgili seçimleri yapmak için **Filtre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="0ee8b-159">**Arka planda çalıştır** hızlı sekmesinde gerektiğinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="0ee8b-160">Tahmin güncelleştirmesini başlatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="0ee8b-161">Aşağıdaki şekilde **İş emri tahmini güncelleştir** iletişim kutusu örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0ee8b-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Şekil 2](media/07-work-orders.png)
