---
title: "İş yükü kapasitesini zamanlama"
description: "Bu konu bir ambardaki çalışanlar veya tüm ambar için iş yükü kapasitesini ayarlamayı ve zamanlamayı açıklar."
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69b9c5590e6f9311696bbbed2e63a6eeba2a90bf
ms.openlocfilehash: 1b93cfaf098b4cff3e72ee9bb599eadfdac2a9b9
ms.contentlocale: tr-tr
ms.lasthandoff: 05/03/2018

---

# <a name="schedule-workload-capacity"></a><span data-ttu-id="414b5-103">İş yükü kapasitesini zamanlama</span><span class="sxs-lookup"><span data-stu-id="414b5-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="414b5-104">Ambarlar için iş yükü kapasitesini zamanlayabilir ve ayrı ambarlardaki çalışanlar için mevcut ve gelecekteki iş yüklerini yansıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="414b5-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="414b5-105">Tüm ambar için iş yükünü veya gelen ve giden iş yükleri için iş yükünü ayrı olarak yansıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="414b5-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="414b5-106">Seçili ambarlar için proje iş yükü çıktısını yansıtmak için master planlama verileri bu ambarlar için kullanılabilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="414b5-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="414b5-107">Daha fazla bilgi için bkz. [Master planlar](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="414b5-107">For more information, see [Master plans](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="414b5-108">Bir ambar için iş yüklerini zamanlama ve görüntüleme</span><span class="sxs-lookup"><span data-stu-id="414b5-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="414b5-109">Bir ambar için iş yükü kapasitesini zamanlamak üzere bir veya daha fazla ambar için bir iş yükü kurulumu oluşturun ve ardından iş yükü kurulumu bir master plan ile ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="414b5-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="414b5-110">İş yükü kapasitesi kurulumunda, gelen ve giden hareketler için ağırlık veya hacim sınırları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="414b5-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="414b5-111">Her ambar için birden fazla kurulum oluşturabilir ve ardından kurulumu ayrı master planlarla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="414b5-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="414b5-112">Örneğin, işgücündeki dönemsel değişikliklere uyum sağlamak için bu yöntemi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="414b5-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="414b5-113">Bir ambar için çalışanlar hem gelen hem de giden iş yükü hareketleriyle çalışıyorsa, ambar kapasitesi kurulumunu iş yükü birleştirilmiş görünümde yansıtılacak şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="414b5-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="414b5-114">Ambarlar için iş yüklerini zamanlamak ve görüntülemek için aşağıdaki görevleri tamamlamalısınız:</span><span class="sxs-lookup"><span data-stu-id="414b5-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="414b5-115">Bir iş yükü kapasitesi kurulumu oluşturun ve bir veya daha fazla ambar için iş yükü kapasite sınırlarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="414b5-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="414b5-116">İş yükü tahminleri oluşturmak için kapasite iş yükü kurulumunu master plan ile ilişkilendirin ve bu tahminlerin ne kadar süreyle uygulanacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="414b5-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="414b5-117">Bir ambar için bir iş yükü kapasite kurulumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="414b5-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="414b5-118">**Stok yönetimi** \> **Kurulum** \> **Ambar izleme** \> **Kapasite iş yükü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="414b5-119">Eylem bölmesinde, iş yükü kapasite kurulumu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="414b5-120">**Ambarlar** hızlı sekmesinde **Yeni**'yi seçin ve bir ambarı iş yükü kapasite kurulumuyla ilişkilendirmek için satırdaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="414b5-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="414b5-121">**Kapasite iş yükü** raporunun gelen ve giden hareketler için toplam iş yükünü tek bir görünümde göstermesi gerekiyorsa **Birleştirilmiş gelen ve giden iş yükü** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="414b5-122">**Hareket türleri** hızlı sekmesinde iş yükü sınırlarının uygulanacağı gelen ve giden hareket türlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="414b5-123">Hem gelen iş yükü hem de giden iş yükü için en az bir hareket türü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="414b5-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="414b5-124">Hacim veya ağırlık için sınırları tanımlama</span><span class="sxs-lookup"><span data-stu-id="414b5-124">Define limits for volume or weight</span></span>

<span data-ttu-id="414b5-125">Ambar iş gücü için ilgili sınırlamaya bağlı olarak, hacim veya ağırlık sınırları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="414b5-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="414b5-126">Belirttiğiniz sınırlar **İş yükü kapasite** raporunda görebileceğiniz iş gücü kapasite yansıtmasına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="414b5-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="414b5-127">Maddeler için hacim ve ağırlıkla ilgili bilgileri yansıtmak için, tüm ürünler için bir stok maddesinin standart hacmi ve bir stok maddesinin ağırlığı belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="414b5-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="414b5-128">Gerekli alanlar aşağıdaki **Serbest bırakılan ürün ayrıntıları** sayfasının **Stok yönetimi** hızlı sekmesindeki alan gruplarında bulunur:</span><span class="sxs-lookup"><span data-stu-id="414b5-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="414b5-129">İşleme</span><span class="sxs-lookup"><span data-stu-id="414b5-129">Handling</span></span>
- <span data-ttu-id="414b5-130">Fiziksel boyutlar</span><span class="sxs-lookup"><span data-stu-id="414b5-130">Physical dimensions</span></span>
- <span data-ttu-id="414b5-131">Ağırlık ölçümleri</span><span class="sxs-lookup"><span data-stu-id="414b5-131">Weight measurements</span></span>

<span data-ttu-id="414b5-132">Bu bilgiler doğru bir şekilde belirtilmezse, **İŞ yükü kapasite** raporu oluşturduğunuzda bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="414b5-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="414b5-133">Rapordan, daha sonra gelecekteki iş yükünü yansıtmak için gereken eksik bilgileri tanımlamak üzere ayrıntıya girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="414b5-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="414b5-134">Bir iş yükü kapasite kurulumunu bir master plan ile ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="414b5-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="414b5-135">**Stok Yönetimi** \> **Periyodik** \> **İş yükünü zamanla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="414b5-136">**Master plan** alanında, iş yükü tahminleri için kullanılacak master planı seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="414b5-137">**Gün sayısı** alanında, iş yükü tahmininin kapsadığı gün sayısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="414b5-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="414b5-138">**iş yükü** alanında, master plan ile ilişkilendirilecek iş yükü kurulumu seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="414b5-139">İş yükü kapasitesini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="414b5-139">View workload capacity</span></span>

1. <span data-ttu-id="414b5-140">**Stok Yönetimi** \> **Sorgular ve raporlar** \> **Fiziksel stok raporları** \> **İş yükü kapasitesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="414b5-141">**Sütun sayısı** alanında, raporda gösterilecek sütun sayısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="414b5-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="414b5-142">**Sipariş türü** alanında raporda yansıtılacak siparişlerin türünü belirtmek için **Planlandı ve onaylandı**, **Planlandı** veya **Onaylandı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="414b5-143">**Yük türü** alanında, iş yükü kapasitesinin hacim veya ağırlık için mi yansıtılacağını belirtmek üzere bir yük türü seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="414b5-144">**İş yükü kapasitesi** alanında bir iş yükü kapasitesi kurulumu seçin.</span><span class="sxs-lookup"><span data-stu-id="414b5-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>
