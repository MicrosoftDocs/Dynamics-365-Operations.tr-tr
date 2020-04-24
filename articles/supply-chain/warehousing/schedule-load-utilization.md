---
title: Yük kullanımını zamanla
description: Bu konu bir ambar için yükün nasıl ayarlanacağını ve zamanlanacağını açıklar.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87455077c69834c9ace6409f4cc611ae6e14beb4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204643"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="b77ce-103">Yük kullanımını zamanla</span><span class="sxs-lookup"><span data-stu-id="b77ce-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b77ce-104">Seçilen yerleşim türleri için yük kullanımını zamanlayabilir ve geçerli ve gelecekteki yük kullanımını da planlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b77ce-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="b77ce-105">Bir veya daha fazla tesis, yük birimleri (bölge veya ambar) veya bir bölge ve ambar birleşimi için yükü planlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b77ce-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="b77ce-106">Bir ambar veya tesis için yükü zamanlama ve görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b77ce-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="b77ce-107">Tesisler, ambarlar veya bölgeler için yükü zamanlamak için bir alan kullanım kurulumu oluşturun ve bunu bir master plan ile ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="b77ce-108">Alan kullanımı kurulumunda, alan kullanımının nasıl planlanacağını belirtmek için **Toplu yerleşim** ve **Malzeme çekme yerleşimi** gibi yerleşim türleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="b77ce-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="b77ce-109">**Bölge** gibi bir depolama yük modu belirtin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="b77ce-110">Gelecekteki alan kullanımı planlaması ilişkilendirilen master planda hesaplanan bilgileri temel alır.</span><span class="sxs-lookup"><span data-stu-id="b77ce-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="b77ce-111">Master plan üretim ve işlemler için gelen ve giden siparişlere yönelik kaynak planlamasını tahmin eder.</span><span class="sxs-lookup"><span data-stu-id="b77ce-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="b77ce-112">Kullanılabilir alan planlaması seçili master plan ile alan kullanımı kurulumu arasındaki ilişkiyi temel alır.</span><span class="sxs-lookup"><span data-stu-id="b77ce-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="b77ce-113">Yer kullanımı kurulumunda seçtiğiniz depolama yükü modunu kullanarak yükün her ambar veya bölge için mi planlanacağını veya planlamaların ambarlar ve bölgeler hakkında daha fazla bilgi içermesi gerekip gerekmediğini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b77ce-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="b77ce-114">Ayrıca engellenen yerleşimlerin yük kullanımı hesaplaması dışında tutulup tutulmayacağını da belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b77ce-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="b77ce-115">Alan kullanımını **Ambar yük kullanımı** raporu oluşturarak planlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b77ce-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="b77ce-116">Bu raporu oluşturduğunuzda, yük kullanımının her tesis için mi, tesisler arasında mı yoksa bölge veya ambar gibi seçilen yük birimi için mi planlanması gerektiğini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b77ce-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="b77ce-117">Ambar için alan kullanım kurulumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="b77ce-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="b77ce-118">**Stok yönetimi** \> **Kurulum** \> **Ambar izleme** \> **Alan kullanımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="b77ce-119">Alan kullanımı kurulumu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="b77ce-120">Bir kurulum için bir kod veya bir ad belirtin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="b77ce-121">**Depolama yükü modu** alanında, alan kullanımına genel bakışın bilgileri ambara, bölgeye veya ambar ve bölgeye göre mi göstermesi gerektiğini seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="b77ce-122">Engellenen stok yerleşimlerini kullanılabilir alan hesaplaması dışında tutmak için **Engellenen yerleşimleri hariç tut** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b77ce-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="b77ce-123">**Stok yerleşimleri** sayfasındaki **Diğer** hızlı sekmesinde bulunan **Giriş engellendi** veya **Çıkış engellendi** alanında yerleşim için bir engelleme nedeni belirterek girdi ve çıktı için bir stok yerleşimini engelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b77ce-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="b77ce-124">**Yerleşim türü** hızlı sekmesinde alan kullanımı hesaplamalarına dahil edilecek yerleşim türlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="b77ce-125">Planlama için en az bir yerleşim türü seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="b77ce-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="b77ce-126">Bir alan kullanım kurulumunu bir master plan ile ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="b77ce-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="b77ce-127">**Stok Yönetimi** \> **Periyodik görevler** \> **Yük kullanımını zamanla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="b77ce-128">**Master plan** alanında bir master plan seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="b77ce-129">**Gün sayısı** alanında, geçerli ve gelecekteki iş yüklerinin planlanmasına dahil edilecek gün sayısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="b77ce-130">**Alan kullanımı** alanında, geçerli ve gelecekteki iş yüklerinin planlanması için kullanılacak alan kullanımı kurulumunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="b77ce-131">Yük kullanım planlamasını belirtme ve bilgileri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b77ce-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="b77ce-132">**Stok Yönetimi** \> **Sorgular ve raporlar** \> **Fiziksel stok raporları** \> **Ambar yük kullanımı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="b77ce-133">**Gösterme ölçütü** alanında, alan kullanımı planlaması düzeyini seçin:</span><span class="sxs-lookup"><span data-stu-id="b77ce-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="b77ce-134">**Tesis** – Her tesis için alan kullanımını yansıtır.</span><span class="sxs-lookup"><span data-stu-id="b77ce-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="b77ce-135">Bu yansıtma, örneğin, bir tesis için tüm ambarları görüntülemek istediğinizde yararlıdır; böylece, ambarlar arasında alan kullanımını dengeleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b77ce-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="b77ce-136">**Yük birimi** – Bölgeler veya alanlar için alan kullanımını yansıtır.</span><span class="sxs-lookup"><span data-stu-id="b77ce-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="b77ce-137">Kullanılabilir alan, alan kullanımı kurulumunu oluştururken **Alan kullanımı** sayfasındaki **Depolama yükü modu** alanında seçtiğiniz değere göre yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="b77ce-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="b77ce-138">Önceki adımda seçtiğiniz değere bağlı olarak, aşağıdaki adımlardan birini izleyin:</span><span class="sxs-lookup"><span data-stu-id="b77ce-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="b77ce-139">**Gösterme ölçütü** alanında **Tesis**'i seçtiyseniz **Tesis** alanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b77ce-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="b77ce-140">Yansıtmaya dahil edilecek bir veya daha fazla tesis seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="b77ce-141">**Gösterme ölçütü** alanında **Yük birimi**'ni seçtiyseniz **Yük birimi** alanı kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b77ce-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="b77ce-142">Yük birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-142">Select the load unit.</span></span>

4. <span data-ttu-id="b77ce-143">**Yükleme türü** alanında alanın planlanacağı ambar işletme birimini belirtmek **Hacim** veya **Ağırlık** seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="b77ce-144">**Alan kullanımı kurulumu** alanında, yansıtmanın temel alacağı alan kullanımı kurulumunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b77ce-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>
