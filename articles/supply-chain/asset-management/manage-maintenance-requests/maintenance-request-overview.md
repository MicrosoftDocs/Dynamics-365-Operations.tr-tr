---
title: Bakım talepleri
description: Bu konu, varlık yönetimi'nde bakım taleplerini yönetme hakkında genel bir bakış sağlar
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e0071ae745987a1217525b2841e3320933a9242
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019641"
---
# <a name="maintenance-requests"></a><span data-ttu-id="ae5f7-103">Bakım talepleri</span><span class="sxs-lookup"><span data-stu-id="ae5f7-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="ae5f7-104">Bakım talepleri, bir varlığın bir bakım veya onarım işi gerektirebileceği ancak bir iş emri oluşturmadan yöneticiye veya planlayıcıya bildirmek için oluşturulan notlar veya beyanlardır.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="ae5f7-105">Bakım talebinin içeriği geçerli kabul edilir, bir iş emri daha sonra bakım talebine göre oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="ae5f7-106">Bakım talepleri, Varlık yönetimi'ndeki herhangi bir varlık için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="ae5f7-107">Şirketinizin bakım taleplerini nasıl kullandığına bağlı olarak çeşitli bakım talepleri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="ae5f7-108">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="ae5f7-108">Here are some examples:</span></span>

- <span data-ttu-id="ae5f7-109">Bakım talepleri</span><span class="sxs-lookup"><span data-stu-id="ae5f7-109">Maintenance requests</span></span>
- <span data-ttu-id="ae5f7-110">Notlar</span><span class="sxs-lookup"><span data-stu-id="ae5f7-110">Notes</span></span>
- <span data-ttu-id="ae5f7-111">Düzeltmeler ya da yükseltmeler</span><span class="sxs-lookup"><span data-stu-id="ae5f7-111">Corrections or enhancements</span></span>
- <span data-ttu-id="ae5f7-112">Yatırımlar</span><span class="sxs-lookup"><span data-stu-id="ae5f7-112">Investments</span></span>
- <span data-ttu-id="ae5f7-113">Depo onarımı (Bu tür, bir bakım veya onarım işi yapmak ve iş tamamlandıktan sonra varlığı geri dönmek için başka bir konumdan varlıklar aldığınızda kullanılır.)</span><span class="sxs-lookup"><span data-stu-id="ae5f7-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="ae5f7-114">Bakım taleplerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="ae5f7-114">View maintenance requests</span></span>

<span data-ttu-id="ae5f7-115">Bakım taleplerini görüntülemek için **Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Tüm bakım talepleri**, **Etkin bakım talepleri**, ya da **İşlem yapılacak yerleşim bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="ae5f7-116">Her liste sayfası bir bakım talebi ile ilgili bazı bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Bakım taleplerini görüntüle](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="ae5f7-118">Çalışan olarak ilişkili olduğunuz işlem yapılacak yerleşimleri veya ilişkili olduğunuz işlem yapılacak yerleşimlere yüklü varlıkları içeren bakım taleplerinin listesini görüntülemek için **İşlem yapılacak yerleşim bakım talepleri** liste sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="ae5f7-119">(Bakım çalışanlarında işlem yapılacak yerleri ayarlama hakkında daha fazla bilgi için bkz: [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="ae5f7-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="ae5f7-120">Müşteri hesabı bilgileri Varlık hizmeti yönetimi'nde (dış bakım) kullanılabilir olsa da, Varlık yönetimi'nde (iç bakım) kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="ae5f7-121">Bir kaydın Ayrıntılar görünümünü açmak için, **Tüm bakım talepleri** listesi sayfasında, kılavuz görünümünde, **Bakım talebi** sütununda bir bağlantı seçin.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Bakım talebi ayrıntılarını görüntüleme](media/02-manage-maintenance-requests.png)

<span data-ttu-id="ae5f7-123">Eylem Bölmesi'ndeki düğmeler sekmeler halinde düzenlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="ae5f7-124">Aşağıdaki tabloda Kıymet Yönetimi'yle ilgili düğmeler kısaca açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="ae5f7-125">Düğme adı</span><span class="sxs-lookup"><span data-stu-id="ae5f7-125">Button name</span></span>                      | <span data-ttu-id="ae5f7-126">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae5f7-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="ae5f7-127">Düzenle</span><span class="sxs-lookup"><span data-stu-id="ae5f7-127">Edit</span></span>                             | <span data-ttu-id="ae5f7-128">Seçili bakım talebini düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="ae5f7-129">Yeni</span><span class="sxs-lookup"><span data-stu-id="ae5f7-129">New</span></span>                              | <span data-ttu-id="ae5f7-130">Yeni bakım talebi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="ae5f7-131">Sil</span><span class="sxs-lookup"><span data-stu-id="ae5f7-131">Delete</span></span>                           | <span data-ttu-id="ae5f7-132">Seçili bakım talebini silin.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="ae5f7-133">İş emri havuzu</span><span class="sxs-lookup"><span data-stu-id="ae5f7-133">Work order pool</span></span>                  | <span data-ttu-id="ae5f7-134">Seçili bakım talebini bir iş emri havuzuna bağlayın.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="ae5f7-135">İş emri</span><span class="sxs-lookup"><span data-stu-id="ae5f7-135">Work order</span></span>                       | <span data-ttu-id="ae5f7-136">Seçili bakım talebine bağlı olarak bir iş emri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="ae5f7-137">Varlık hatası</span><span class="sxs-lookup"><span data-stu-id="ae5f7-137">Asset fault</span></span>                      | <span data-ttu-id="ae5f7-138">Seçili bakım talebine hata kaydı oluşturabileceğiniz **varlık hataları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="ae5f7-139">İş emirleri</span><span class="sxs-lookup"><span data-stu-id="ae5f7-139">Work orders</span></span>                      | <span data-ttu-id="ae5f7-140">Seçili bakım talebine bağlı olan tüm iş siparişlerinin bir listesini göster.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="ae5f7-141">Bakım talebi durumunu güncelleştir</span><span class="sxs-lookup"><span data-stu-id="ae5f7-141">Update maintenance request state</span></span> | <span data-ttu-id="ae5f7-142">Bakım talebi durumunu güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="ae5f7-143">Yaşam döngüsü durumu günlüğü</span><span class="sxs-lookup"><span data-stu-id="ae5f7-143">Lifecycle state log</span></span>              | <span data-ttu-id="ae5f7-144">Seçili bakım talebinin yaşam döngüsü durumlarını gösteren günlüğü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="ae5f7-145">Bakım talebi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="ae5f7-145">Maintenance request details</span></span>      | <span data-ttu-id="ae5f7-146">Seçili bakım talebinin ayrıntılarını gösteren bir rapor yazdırın.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="ae5f7-147">Ödünç varlığı gönder</span><span class="sxs-lookup"><span data-stu-id="ae5f7-147">Send loan asset</span></span>                  | <span data-ttu-id="ae5f7-148">Seçili bakım talebinde seçilen varlığın geçici olarak değiştirilmesi gereken bir kredi varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="ae5f7-149">Kredi varlıklarını iade etme</span><span class="sxs-lookup"><span data-stu-id="ae5f7-149">Return loan asset</span></span>                | <span data-ttu-id="ae5f7-150">İade edilen ödünç varlığını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="ae5f7-150">Register the loan asset as returned.</span></span> |

