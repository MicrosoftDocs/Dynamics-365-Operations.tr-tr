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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7038269c66092367a0faf147766cb45eb5364e1b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3890141"
---
# <a name="maintenance-requests"></a><span data-ttu-id="387b1-103">Bakım talepleri</span><span class="sxs-lookup"><span data-stu-id="387b1-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="387b1-104">Bakım talepleri, bir varlığın bir bakım veya onarım işi gerektirebileceği ancak bir iş emri oluşturmadan yöneticiye veya planlayıcıya bildirmek için oluşturulan notlar veya beyanlardır.</span><span class="sxs-lookup"><span data-stu-id="387b1-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="387b1-105">Bakım talebinin içeriği geçerli kabul edilir, bir iş emri daha sonra bakım talebine göre oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="387b1-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="387b1-106">Bakım talepleri, Varlık yönetimi'ndeki herhangi bir varlık için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="387b1-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="387b1-107">Şirketinizin bakım taleplerini nasıl kullandığına bağlı olarak çeşitli bakım talepleri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="387b1-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="387b1-108">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="387b1-108">Here are some examples:</span></span>

- <span data-ttu-id="387b1-109">Bakım talepleri</span><span class="sxs-lookup"><span data-stu-id="387b1-109">Maintenance requests</span></span>
- <span data-ttu-id="387b1-110">Notlar</span><span class="sxs-lookup"><span data-stu-id="387b1-110">Notes</span></span>
- <span data-ttu-id="387b1-111">Düzeltmeler ya da yükseltmeler</span><span class="sxs-lookup"><span data-stu-id="387b1-111">Corrections or enhancements</span></span>
- <span data-ttu-id="387b1-112">Yatırımlar</span><span class="sxs-lookup"><span data-stu-id="387b1-112">Investments</span></span>
- <span data-ttu-id="387b1-113">Depo onarımı (Bu tür, bir bakım veya onarım işi yapmak ve iş tamamlandıktan sonra varlığı geri dönmek için başka bir konumdan varlıklar aldığınızda kullanılır.)</span><span class="sxs-lookup"><span data-stu-id="387b1-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="387b1-114">Bakım taleplerini görüntüle</span><span class="sxs-lookup"><span data-stu-id="387b1-114">View maintenance requests</span></span>

<span data-ttu-id="387b1-115">Bakım taleplerini görüntülemek için **Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Tüm bakım talepleri**, **Etkin bakım talepleri**, ya da **İşlem yapılacak yerleşim bakım talepleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="387b1-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="387b1-116">Her liste sayfası bir bakım talebi ile ilgili bazı bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="387b1-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Bakım taleplerini görüntüle](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="387b1-118">Çalışan olarak ilişkili olduğunuz işlem yapılacak yerleşimleri veya ilişkili olduğunuz işlem yapılacak yerleşimlere yüklü varlıkları içeren bakım taleplerinin listesini görüntülemek için **İşlem yapılacak yerleşim bakım talepleri** liste sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="387b1-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="387b1-119">(Bakım çalışanlarında işlem yapılacak yerleri ayarlama hakkında daha fazla bilgi için bkz: [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="387b1-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="387b1-120">Müşteri hesabı bilgileri Varlık hizmeti yönetimi'nde (dış bakım) kullanılabilir olsa da, Varlık yönetimi'nde (iç bakım) kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="387b1-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="387b1-121">Bir kaydın Ayrıntılar görünümünü açmak için, **Tüm bakım talepleri** listesi sayfasında, kılavuz görünümünde, **Bakım talebi** sütununda bir bağlantı seçin.</span><span class="sxs-lookup"><span data-stu-id="387b1-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Bakım talebi ayrıntılarını görüntüleme](media/02-manage-maintenance-requests.png)

<span data-ttu-id="387b1-123">Eylem Bölmesi'ndeki düğmeler sekmeler halinde düzenlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="387b1-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="387b1-124">Aşağıdaki tabloda Kıymet Yönetimi'yle ilgili düğmeler kısaca açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="387b1-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="387b1-125">Düğme adı</span><span class="sxs-lookup"><span data-stu-id="387b1-125">Button name</span></span>                      | <span data-ttu-id="387b1-126">Tanım</span><span class="sxs-lookup"><span data-stu-id="387b1-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="387b1-127">Düzenle</span><span class="sxs-lookup"><span data-stu-id="387b1-127">Edit</span></span>                             | <span data-ttu-id="387b1-128">Seçili bakım talebini düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="387b1-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="387b1-129">Yeni</span><span class="sxs-lookup"><span data-stu-id="387b1-129">New</span></span>                              | <span data-ttu-id="387b1-130">Yeni bakım talebi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="387b1-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="387b1-131">Sil</span><span class="sxs-lookup"><span data-stu-id="387b1-131">Delete</span></span>                           | <span data-ttu-id="387b1-132">Seçili bakım talebini silin.</span><span class="sxs-lookup"><span data-stu-id="387b1-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="387b1-133">İş emri havuzu</span><span class="sxs-lookup"><span data-stu-id="387b1-133">Work order pool</span></span>                  | <span data-ttu-id="387b1-134">Seçili bakım talebini bir iş emri havuzuna bağlayın.</span><span class="sxs-lookup"><span data-stu-id="387b1-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="387b1-135">İş emri</span><span class="sxs-lookup"><span data-stu-id="387b1-135">Work order</span></span>                       | <span data-ttu-id="387b1-136">Seçili bakım talebine bağlı olarak bir iş emri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="387b1-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="387b1-137">Varlık hatası</span><span class="sxs-lookup"><span data-stu-id="387b1-137">Asset fault</span></span>                      | <span data-ttu-id="387b1-138">Seçili bakım talebine hata kaydı oluşturabileceğiniz **varlık hataları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="387b1-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="387b1-139">İş emirleri</span><span class="sxs-lookup"><span data-stu-id="387b1-139">Work orders</span></span>                      | <span data-ttu-id="387b1-140">Seçili bakım talebine bağlı olan tüm iş siparişlerinin bir listesini göster.</span><span class="sxs-lookup"><span data-stu-id="387b1-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="387b1-141">Bakım talebi durumunu güncelleştir</span><span class="sxs-lookup"><span data-stu-id="387b1-141">Update maintenance request state</span></span> | <span data-ttu-id="387b1-142">Bakım talebi durumunu güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="387b1-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="387b1-143">Yaşam döngüsü durumu günlüğü</span><span class="sxs-lookup"><span data-stu-id="387b1-143">Lifecycle state log</span></span>              | <span data-ttu-id="387b1-144">Seçili bakım talebinin yaşam döngüsü durumlarını gösteren günlüğü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="387b1-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="387b1-145">Bakım talebi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="387b1-145">Maintenance request details</span></span>      | <span data-ttu-id="387b1-146">Seçili bakım talebinin ayrıntılarını gösteren bir rapor yazdırın.</span><span class="sxs-lookup"><span data-stu-id="387b1-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="387b1-147">Ödünç varlığı gönder</span><span class="sxs-lookup"><span data-stu-id="387b1-147">Send loan asset</span></span>                  | <span data-ttu-id="387b1-148">Seçili bakım talebinde seçilen varlığın geçici olarak değiştirilmesi gereken bir kredi varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="387b1-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="387b1-149">Kredi varlıklarını iade etme</span><span class="sxs-lookup"><span data-stu-id="387b1-149">Return loan asset</span></span>                | <span data-ttu-id="387b1-150">İade edilen ödünç varlığını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="387b1-150">Register the loan asset as returned.</span></span> |

