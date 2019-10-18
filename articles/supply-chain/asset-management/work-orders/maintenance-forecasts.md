---
title: Bakım tahminleri
description: Bu konuda Varlık Yönetimi'nde bakım tahminleri açıklanmaktadır.
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
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024511"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="d88bc-103">Bakım tahminleri</span><span class="sxs-lookup"><span data-stu-id="d88bc-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="d88bc-104">Bir iş emri oluşturduğunuzda, ilgili varlıklar ve bakım işi türleriyle iş emri işleri oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="d88bc-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="d88bc-105">Bakım tahminlerini içeren bir bakım işi türü seçtiğinizde, tahminler otomatik olarak iş emrine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="d88bc-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="d88bc-106">Bir iş emrinde tahmin satırları ekleyebilir veya silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88bc-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="d88bc-107">Bir iş emri yaşam döngüsü durumu, ilgili proje türü ve proje tipiyle ilgili aşama kuralları kurulumu, tahmin satırları ekleyip ekleyemeyeceğinizi veya düzenleyip düzenleyemeyeceğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="d88bc-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="d88bc-108">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="d88bc-109">Listeden iş emrini seçin ve **Tahmin**'e tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="d88bc-110">**İş emri bakım tahmininde**, iş emri işinde seçilen bakım işi türünden gelen tahmin satırları görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d88bc-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="d88bc-111">İş emrine tahmin saatleri ekleme</span><span class="sxs-lookup"><span data-stu-id="d88bc-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="d88bc-112">Tahmin eklemek istediğiniz iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="d88bc-113">**Saatler** hızlı sekmesinde yeni bir satır oluşturmak için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="d88bc-114">**Kategori** alanında bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="d88bc-115">**Saat** alanına tahmini saat sayısı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="d88bc-116">**Satır özelliği** alanında, satırda kullanılacak masraf türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="d88bc-117">İş emrine madde tahminleri ekleme</span><span class="sxs-lookup"><span data-stu-id="d88bc-117">Add items forecast to a work order</span></span>

<span data-ttu-id="d88bc-118">Bir iş emri bakım tahminine madde eklemenin üç yolu vardır: Yedek parça listesi veya varlık ürün reçetesine dahil edilmeyen maddeler (yedek parçalar) için satırlar oluşturabilir, onaylanan yedek parçalar listesinden yedek parçalar seçebilir ve maddeleri Varlık ürün reçetesinden seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88bc-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="d88bc-119">Tahmin eklemek istediğiniz iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="d88bc-120">**Maddeler** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="d88bc-121">Yedek parçalar listesi veya varlık ürün reçetesi listesinde bulunmayan bir yedek parça için yeni bir satır oluşturmak üzere **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="d88bc-122">**Madde numarası** alanında bir maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="d88bc-123">**Satış miktarı** alanına miktar ekleyin ve **Birim** alanında bir miktar birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="d88bc-124">İlgili alanlara maliyet fiyatını ve para birimini ekleyin ve bir **Satır özelliği** seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="d88bc-125">Madde satırlarında görüntülenen boyutların listesini değiştirmek isterseniz **Stok** > **Boyutları görüntüle**'ye tıklayın, boyutları seçin ve **Kurulumu kaydet** düğmesinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="d88bc-126">Bakım tahminine onaylı bir yedek parça eklemek istiyorsanız, **Yedek parça ekle**'ye tıklayın, yedek parçayı seçin, gerekiyorsa ilgili bilgileri düzenleyin **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="d88bc-127">Tahmine varlık ürün reçetesi maddeleri eklemek istiyorsanız, **Ürün reçetesi maddeleri ekle**'ye tıklatın, maddeyi seçin, gerekiyorsa ilgili bilgileri düzenleyin ve **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="d88bc-128">Seçilen satırdaki maddenin Varlık Yönetiminde varlıklar, bakım iş türü varsayılanları, yedek parçalar ve iş emirleriyle ilişkili olarak nerede kullanıldığıyla ilgili genel bir bakış edinmek için **Maddenin kullanıldığı yer**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="d88bc-129">İş emrine gider tahminleri ekleme</span><span class="sxs-lookup"><span data-stu-id="d88bc-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="d88bc-130">Bu konu, bir iş emrine nasıl gider tahmini ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="d88bc-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="d88bc-131">Formun sol tarafında, tahmin eklemek istediğiniz iş emri işini seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="d88bc-132">**Gider** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="d88bc-133">Yeni bir satır oluşturmak için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="d88bc-134">**Kategori** alanında bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="d88bc-135">**Miktar** alanına miktarı girin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="d88bc-136">İlgili alanlara maliyet fiyatı, satış para birimi ve satış fiyatını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="d88bc-137">**Satır özelliği** alanında, satırda kullanılacak masraf türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="d88bc-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="d88bc-138">**Bakım tahmini toplamları** hızlı sekmesinde, seçili iş emri işi ve iş emri için her bir sekmede oluşturulan satır sayısının genel görünümünü görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88bc-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="d88bc-139">Ayrıca, iş emri işi ve iş emri için tahmin edilen çalışma saatlerinin toplamını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88bc-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Şekil 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="d88bc-141">İş emri tahminlerini otomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d88bc-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="d88bc-142">Varlık Yönetimi'nde, diğer modüllerde güncelleştirilen saat maliyetleri, madde maliyetleri ve giderler için iş emri tahminlerindeki değişiklikleri otomatik olarak güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88bc-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="d88bc-143">Bu işlem, en son maliyet fiyatlarının iş emri tahminlerinde her zaman kullanılmasını sağlamak için yapılır.</span><span class="sxs-lookup"><span data-stu-id="d88bc-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="d88bc-144">[Bakım işi türü tahminlerinde](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) de benzer güncelleştirmeler yapmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="d88bc-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="d88bc-145">**Varlık yönetimi** > **Periyodik** > **Tahmin** > **İş emri tahmini güncelleştir** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="d88bc-146">**İş emri tahminini güncelleştir** iletişim kutusunda gerekirse, belirli iş emirleri veya iş emri işleriyle ilgili seçimler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88bc-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="d88bc-147">Bu seçimleri yapmak için **Filtre**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="d88bc-148">Gerekirse, **Arka planda çalıştır** hızlı sekmesinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d88bc-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="d88bc-149">Tahmin güncelleştirmesini başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d88bc-149">Click **OK** to start the forecast update.</span></span>


![Şekil 2](media/07-work-orders.png)

