---
title: Bakım planlarını zamanla
description: Bu konuda Varlık Yönetimi'nde bakım planlarını zamanlama işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: df5bcd57c611ed5f77a417a28f28fca84057d734
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206001"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="86201-103">Bakım planlarını zamanla</span><span class="sxs-lookup"><span data-stu-id="86201-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="86201-104">Önleyici bakım zamanlaması, varlıklarda ayarlanan bakım planlarını temel alarak varlıklar üzerinde takvim girişleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86201-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="86201-105">Takvim girişlerini seçilen bakım planlarını, varlık türlerini ve varlıkları temel alarak zamanlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86201-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="86201-106">**Varlık yönetimi** > **Dönemsel** > **Önleyici bakım** > **Bakım planlarını zamanla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86201-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="86201-107">**Dönem** ve **Dönem sıklığı** alanlarında bir zaman aralığı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86201-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="86201-108">**Dönem** ve **Dönem sıklığı** alanları, oluşturduğunuz bakım planlarını temel alarak (zaman temelli veya sayaç temelli) bakım zamanlaması satırlarını ne kadar ileri bir zamanda oluşturmak istediğinizi belirtir.</span><span class="sxs-lookup"><span data-stu-id="86201-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="86201-109">Aşağıdaki şekilde, bakım zamanlaması satırları (= iş emri teklifleri) güncel tarihten itibaren ve üç ay sonrası için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="86201-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="86201-110">Bakım planı satırına göre iş emirlerinin otomatik olarak oluşturulması gerekiyorsa **Satırda belirtildiyse otomatik oluştur** geçiş düğmesinde "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="86201-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="86201-111">Bu geçiş düğmesi "Evet" olarak ayarlanırsa *ve* **Bakım planları**'ndaki bakım planı satırlarında **Otomatik oluştur** onay kutusu da seçilirse iş emirleri, bakım planı satırları temel alınarak oluşturulur ve "Oluşturulan iş emri" durumuna sahip bakım zamanlaması satırları da oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="86201-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="86201-112">Yalnızca bir seçenek belirlenirse (Bu iletişim kutusunda **Satırda belirtildiyse otomatik oluştur** geçiş düğmesi veya **Bakım planları** formundaki **Otomatik oluştur** onay kutusu) yalnızca "Oluşturuldu" durumuna sahip bakım zamanlaması satırları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="86201-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="86201-113">Bu durumda, iş emri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="86201-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="86201-114">Bakım planlarını (zaman veya sayaç), varlıkları, varlık türlerini, işlem yapılacak yerleşimleri ve işlem yapılacak yerleşim türlerini temel alan takvim girişleri oluşturmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="86201-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="86201-115">**Filtre** düğmesine tıklayın ve gerekirse seçimlerinizi yapın.</span><span class="sxs-lookup"><span data-stu-id="86201-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="86201-116">İşlem yapılacak yerleşimlerde bakım planlarının zamanlanmasıyla ilgili olarak: Bakım planlarını zamanladıktan sonra **Tüm işlem yapılacak yerleşimler** > **Bakım planları** hızlı sekmesindeki bakım planlarında varlık türleri, üreticiler ve modellerin ayarını güncelleştirirseniz, bu işlem yapılacak yerleşimle ilgili mevcut bakım zamanlaması girişleri otomatik olarak silinir.</span><span class="sxs-lookup"><span data-stu-id="86201-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="86201-117">İşlem yapılacak yerleşimdeki güncelleştirilmiş bakım planı ayarına karşılık gelen yeni takvim girişleri oluşturmak için, bu işlem yapılacak yerleşim için yeni bir bakım planı zamanlaması çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="86201-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="86201-118">[İşlem yapılacak yerleşimler oluşturma](../functional-locations/create-functional-locations.md) bölümünde işlem yapılacak yerleşimlerde varlık türleri, üreticiler ve modelleri ayarlama hakkında daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="86201-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="86201-119">*Örnek:* Belirli bir işlem yapılacak yerleşim için bir bakım planı oluşturmak isterseniz bu, bakım planını zamanladığınızda belirli bir sürede bu işlem yapılacak yerleşimdeki tüm varlık ayarlarının dahil edileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="86201-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="86201-120">Bu durumda, bir bakım planı oluşturabilir ve belirli bir işlem yapılacak yerleşimi seçebilirsiniz ancak bakım planına herhangi bir varlık EKLEYEMEZSİNİZ.</span><span class="sxs-lookup"><span data-stu-id="86201-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any assets in the maintenance plan.</span></span> <span data-ttu-id="86201-121">Bunun sonucunda, bu bakım planını zamanladığınızda bu süre içinde işlem yapılacak yerleşimle ilgili tüm varlıklar için bakım zamanlaması satırları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="86201-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="86201-122">**Varlık Türleri**'ndeki varlık türlerini, üreticileri ve modelleri değiştirirseniz bu değişiklikler yalnızca güncelleştirilmiş varlık türünü kullanan yeni varlıkları etkiler.</span><span class="sxs-lookup"><span data-stu-id="86201-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="86201-123">[Varlık türleri](../setup-for-objects/object-types.md) bölümünde varlık türü ayarlama hakkında daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="86201-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="86201-124">Varlıklarda bakım zamanlaması girişlerinin oluşturulmasını başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86201-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="86201-125">Oluşturulan girişler **Tüm bakım zamanlaması** liste sayfasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="86201-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span> <span data-ttu-id="86201-126">Aşağıdaki şekilde bir **Bakım planlarını zamanla** iletişim kutusu örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="86201-126">The following illustration shows an example of the **Schedule maintenance plans** dialog.</span></span>

![Şekil 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="86201-128">**Bakım planlarını zamanla** iletişim kutusunda düzenli aralıklarla otomatik olarak takvim girişleri oluşturmak için **Arka planda çalıştır** hızlı sekmesinde toplu işler ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86201-128">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="86201-129">Önleyici bakım zamanladığınızda sistem tarihi ve saatinden önceki beklenen başlangıç tarihi ve saatine sahip bakım zamanlaması satırları oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="86201-129">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="86201-130">Aşağıdaki şekilde zaman temelli bir bakım planı hesaplamasının grafik resmi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="86201-130">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![Şekil 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="86201-132">Sayaç temelli bakım planlarıyla ilgili olarak: Aşağıdaki şekillerde, iki farklı sayaç kaydı döngüsü gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="86201-132">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="86201-133">Bunlar, varlığın (araç) her ay yaklaşık 2.000 km çalışmasının beklendiği "V0001" varlığı için ayarlanan bir bakım planını temel alır.</span><span class="sxs-lookup"><span data-stu-id="86201-133">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="86201-134">İlk örnekte, beklenen 2.000 km'ye her ay ulaşılmaz.</span><span class="sxs-lookup"><span data-stu-id="86201-134">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="86201-135">Sayaç temelli bakım planına göre, eşik değer 2.000 km'dir. Bu, bir bakım planı zamanlaması çalıştırdığınızda 2.000 kilometre eşik değerine her ulaşıldığında bir bakım zamanlaması satırının oluşturulması gerektiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="86201-135">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="86201-136">Örnek 1'de, 4 kayıt satırı bulunur ancak 2.000 kilometre eşik değerine yalnızca bir kez ulaşılır.</span><span class="sxs-lookup"><span data-stu-id="86201-136">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="86201-137">Bu, örneğin 3 aylık bir dönem için bu varlığa yönelik bakım planlarını zamanlamayı çalıştırdığınızda yalnızca bir bakım zamanlaması satırı oluşturulacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="86201-137">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="86201-138">Sonraki şekilde, her ay 2.000 km veya daha fazla değer kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="86201-138">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="86201-139">Bu nedenle, bu varlığın bakım planlarını 3 aylık bir dönem için zamanlarsanız üç bakım satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="86201-139">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="86201-140">Burada açıklanan örnekler, bir varlıkta gerçekleştirilen tüm sayaç kayıtlarının, varlığın aşınma ve yıpranma eğilimini gösterdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="86201-140">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="86201-141">Bu eğilim, bakım planı zamanlaması sırasında hesaplamaya dayalı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="86201-141">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![Şekil 3](media/11-preventive-maintenance.png)

![Şekil 4](media/12-preventive-maintenance.png)

