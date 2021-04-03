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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b5cf1a634ef5ab60707cf471ef017ec167e3013f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263674"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="3bf90-103">Bakım tahminleri</span><span class="sxs-lookup"><span data-stu-id="3bf90-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3bf90-104">Bir iş emri oluşturduğunuzda, ilgili varlıklar ve bakım işi türleri bulunan iş emri işleri oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="3bf90-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="3bf90-105">Bakım tahminlerini içeren bir bakım işi türü seçtiğinizde, tahminler otomatik olarak iş emrine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="3bf90-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="3bf90-106">Bir iş emrine tahmin satırları ekleyebilir veya bunları bir iş emrinden silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3bf90-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="3bf90-107">Bir iş emri yaşam döngüsü durumu, ilgili proje türü ve proje türüyle ilgili aşama kuralları kurulumu, tahmin satırları ekleyip ekleyemeyeceğinizi veya düzenleyip düzenleyemeyeceğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="3bf90-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="3bf90-108">İş emri yaşam döngüsü durumları ve ilgili proje aşamaları hakkında daha fazla bilgi için bkz. [Tahminler, iş emirleri ve projeler](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="3bf90-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="3bf90-109">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3bf90-110">Listede iş emrini seçin ve sonra Eylem bölmesinde > **İş emri** sekmesinde > **Proje** grubunda **Tahmin** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="3bf90-111">**İş emri bakım tahmini** sayfasında, iş emri işinde seçilen bakım işi türünden gelen tahmin satırları görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3bf90-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="3bf90-112">İş emrine saat tahmini ekleme</span><span class="sxs-lookup"><span data-stu-id="3bf90-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="3bf90-113">**İş emri bakım tahmini** sayfasında, tahmin eklenecek iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="3bf90-114">**Saatler** hızlı sekmesinde yeni bir satır oluşturmak için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="3bf90-115">**Kategori** alanında bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="3bf90-116">**Saat** alanına tahmini saat sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="3bf90-117">**Satır özelliği** alanında, satırda kullanılması gereken masraf türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="3bf90-118">İş emrine madde tahmini ekleme</span><span class="sxs-lookup"><span data-stu-id="3bf90-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="3bf90-119">Bir iş emri bakım tahminine madde eklemenin üç yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="3bf90-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="3bf90-120">Yedek parça listesi veya varlık ürün reçetesine (BOM) dahil edilmeyen maddeler (yedek parçalar) için satırlar oluşturabilir, onaylanan yedek parçalar listesinden yedek parçalar seçebilir veya maddeleri Varlık ürün reçetesinden seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3bf90-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="3bf90-121">**İş emri bakım tahmini** sayfasında, tahmin eklenecek iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-121">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

- <span data-ttu-id="3bf90-122">**Maddeler** hızlı sekmesinde, uygun yöntemi kullanarak bakım tahminine maddeler ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="3bf90-123">Yedek parçalar listesi veya varlık ürün reçetesinde bulunmayan bir yedek parça için yeni bir satır oluşturmak üzere şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="3bf90-124">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-124">Select **Add**.</span></span>
2. <span data-ttu-id="3bf90-125">**Madde numarası** alanında maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="3bf90-126">**Satış miktarı** alanına miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="3bf90-127">**Birim** alanında, miktar için ölçü birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="3bf90-128">**Maliyet fiyatı** ve **Para birimi** alanlarına ilgili değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="3bf90-129">**Satır özelliği** alanında bir satır özelliği seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="3bf90-130">Madde satırlarında görüntülenen boyutların listesini değiştirmek için **Stok** > **Boyutları görüntüle**'yi seçin, boyutları seçin ve ardından **Kurulumu kaydet** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3bf90-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="3bf90-131">Onaylı bir yedek parça listesinden yedek parça eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="3bf90-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="3bf90-132">**Yedek parça ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="3bf90-133">Yedek parçayı seçin ve gerek duyduğunuz gibi ilgili bilgileri düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="3bf90-134">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-134">Select **OK**.</span></span>

<span data-ttu-id="3bf90-135">Varlık ürün reçetesinden bir madde eklemek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="3bf90-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="3bf90-136">**Ürün reçetesi maddeleri ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="3bf90-137">Maddeyi seçin ve gerek duyduğunuz gibi ilgili bilgileri düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="3bf90-138">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-138">Select **OK**.</span></span>

<span data-ttu-id="3bf90-139">Seçilen satırdaki maddenin Varlık Yönetiminde varlıklar, bakım işi türü varsayılanları, yedek parçalar ve iş emirleriyle ilişkili olarak nerede kullanıldığıyla ilgili genel bir bakış edinmek için **Maddenin kullanıldığı yer**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="3bf90-140">Bu genel bakış hakkında daha fazla bilgi için bkz. [Maddenin kullanıldığı yer](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="3bf90-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="3bf90-141">İş emrine gider tahmini ekleme</span><span class="sxs-lookup"><span data-stu-id="3bf90-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="3bf90-142">**İş emri bakım tahmini** sayfasında, tahmin eklenecek iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="3bf90-143">**Gider** hızlı sekmesinde satır oluşturmak için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="3bf90-144">**Kategori** alanında bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="3bf90-145">**Miktar** alanına miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="3bf90-146">**Maliyet fiyatı**, **Satış para birimi** ve **Satış fiyatı** alanlarına uygun değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="3bf90-147">**Satır özelliği** alanında, satırda kullanılması gereken masraf türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="3bf90-148">**Bakım tahmini toplamları** hızlı sekmesi, seçili iş emri işi ve iş emri için her hızlı sekmede oluşturulan satır sayısının genel görünümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="3bf90-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="3bf90-149">Ayrıca, iş emri işi ve iş emri için tahmin edilen çalışma saatlerinin toplamını da gösterir.</span><span class="sxs-lookup"><span data-stu-id="3bf90-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="3bf90-150">Aşağıdaki şekilde **İş emri bakım bakım tahmini** sayfası örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3bf90-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Şekil 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="3bf90-152">İş emri tahminlerini otomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3bf90-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="3bf90-153">Microsoft Dynamics 365 for Finance and Operations'daki diğer modüllerde saat maliyetleri, madde maliyetleri ve giderler güncelleştirilirse Varlık Yönetimindeki iş emri tahminleri bu değişiklikleri yansıtacak şekilde otomatik olarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3bf90-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="3bf90-154">Bu özellik, en son maliyet fiyatlarının iş emri tahminlerinde her zaman kullanılmasını sağlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3bf90-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="3bf90-155">[Bakım işi türü tahminlerinde](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) de benzer güncelleştirmeler yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3bf90-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="3bf90-156">**Varlık yönetimi** > **Periyodik** > **Tahmin** > **İş emri tahminini güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="3bf90-157">**İş emri tahminini güncelleştir** iletişim kutusunda, **Dahil edilecek kayıtlar** hızlı sekmesinde gerekirse, belirli iş emirleri veya iş emri işleriyle ilgili seçimler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3bf90-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="3bf90-158">İlgili seçimleri yapmak için **Filtre**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="3bf90-159">**Arka planda çalıştır** hızlı sekmesinde gerektiğinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3bf90-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="3bf90-160">Tahmin güncelleştirmesini başlatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3bf90-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="3bf90-161">Aşağıdaki şekilde **İş emri tahmini güncelleştir** iletişim kutusu örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3bf90-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Şekil 2](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]