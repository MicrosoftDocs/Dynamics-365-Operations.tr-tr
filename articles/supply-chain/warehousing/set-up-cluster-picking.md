---
title: "Küme malzeme çekme ayarlama"
description: "Bu konu küme malzeme çekmenin nasıl ayarlanacağını ve küme malzeme çekmeyle madde onayının nasıl uygulanacağını açıklar."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2ec0890963b2b01407acac8003453faf370894b4
ms.openlocfilehash: 1c23421ddfda8c5f6fa27a31831a00ead6094db9
ms.contentlocale: tr-tr
ms.lasthandoff: 04/11/2018

---

[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="5f1f4-103">Küme malzeme çekme ayarlama</span><span class="sxs-lookup"><span data-stu-id="5f1f4-103">Set up cluster picking</span></span>

<span data-ttu-id="5f1f4-104">Bu konu çalışanlara aynı anda birden çok iş emri için tek bir yerleşimden maddeleri çekebilmeleri için mobil cihazlardan malzeme çekme işlerini kümeler halinde gruplandırma olanağı sağlamayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="5f1f4-105">Buna *küme malzeme çekme* denir.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="5f1f4-106">Küme malzeme çekme hakkında</span><span class="sxs-lookup"><span data-stu-id="5f1f4-106">About cluster picking</span></span>

<span data-ttu-id="5f1f4-107">İş emirleri ambara serbest bırakıldıktan sonra çalışan emirleri bir kümeye atamak için mobil cihaz kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="5f1f4-108">Küme çalışan için malzeme çekme işini düzenler.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="5f1f4-109">Bir iş emri bir kümeye atandığında, çalışanın iş emri için malzeme çekme işlemini gerçekleştirmek için küme malzeme çekme kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="5f1f4-110">Çalışan diğer malzeme çekme yöntemlerini kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="5f1f4-111">Bir iş emri bir kümeye yanlışlıkla atanırsa, çalışanın kümeyi bozması ve yeniden oluşturması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="5f1f4-112">Gerekirse, çalışan kümeyi başka bir çalışana geçirebilir.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="5f1f4-113">Bu, kümenin durumunu Geçirildi olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="5f1f4-114">Çalışan malzeme çekme ve koyma işinin tamamlandığını belirtmek için bir mobil cihaz kullandığında, sevkiyat veya yüklemenin Dynamics 365 for Finance and Operations istemcisinde onaylanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the Dynamics 365 for Finance and Operations client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="5f1f4-115">Küme malzeme çekme ayarlama</span><span class="sxs-lookup"><span data-stu-id="5f1f4-115">Set up cluster picking</span></span>

<span data-ttu-id="5f1f4-116">Küme malzeme çekmeyi etkinleştirmek için şunları ayarlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="5f1f4-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="5f1f4-117">**Küme profilleri** – Küme kodlarının otomatik oluşturulup oluşturulmayacağını, kullanılacak pozisyon sayısını, kümelerin ne zaman ayrılacağını ve malzeme çekme işinin nasıl sıralanıp doğrulanacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="5f1f4-118">**İş şablonları** – Küme malzeme çekme için malzeme çekme içinin nasıl oluşturulacağını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="5f1f4-119">**Yerleşim yönergeleri** – Maddelerin nereden çekileceğini ve nereye konulacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="5f1f4-120">**Mobil cihaz menü öğeleri** – Küme malzeme çekme tarafından yönlendirilen mevcut işi kullanmak için bir mobil cihaz menüsü yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="5f1f4-121">Mobil cihazlarda görünmesi için menüyü mobil cihaz menüsüne eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="5f1f4-122">**Ambar Yönetimi parametreleri** – Kümeler için tanımlayıcılar oluşturmak istiyorsanız, kullanılacak numara serisini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="5f1f4-123">Küme profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="5f1f4-123">Set up a cluster profile</span></span>

<span data-ttu-id="5f1f4-124">Küme profili ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="5f1f4-125">**Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Küme profilleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="5f1f4-126">Yeni bir profil oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="5f1f4-127">**Küme oluştur**'a tıklayın ve **Küme sıralama** altından **Yeni**'yi tıklayarak küme için sıralama ölçütü ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="5f1f4-128">Bu sıralama kriteri, çalışanın malzeme çekme işini hangi sırada yapacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="5f1f4-129">İhtiyaç duyduğunuz sayıda ölçüt ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="5f1f4-130">**Sıra numarası** alanında, sıralama ölçütü işlenme sırasını belirlemek için bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="5f1f4-131">**Alan adı** alanında, sıralamayı belirleyecek alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="5f1f4-132">Örneğin **WMSLocationId** alanını seçerseniz iş yerleşime göre sıralanır.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="5f1f4-133">**Sıralama** alanında aşağıdaki seçeneklerden birini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="5f1f4-134">**Seçenek**</span><span class="sxs-lookup"><span data-stu-id="5f1f4-134">**Option**</span></span>     | <span data-ttu-id="5f1f4-135">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="5f1f4-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1f4-136">**Artan**</span><span class="sxs-lookup"><span data-stu-id="5f1f4-136">**Ascending**</span></span>  | <span data-ttu-id="5f1f4-137">Malzeme çekme işi sıralama ölçütünü temel alarak artan düzende sıralanır.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="5f1f4-138">Örneğin sıralama ölçütü olarak **WMSLocationId** kullanırsanız ve yerleşim kodlarının 1, 2, 3 ve 4 ise önce yerleşim 4'ten malzeme çekersiniz.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="5f1f4-139">**Azalan**</span><span class="sxs-lookup"><span data-stu-id="5f1f4-139">**Descending**</span></span> | <span data-ttu-id="5f1f4-140">Malzeme çekme işi sıralama ölçütünü temel alarak azalan düzende sıralanır.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="5f1f4-141">Örneğin sıralama ölçütü olarak **WMSLocationId** kullanırsanız ve yerleşim kodlarının 1, 2, 3 ve 4 ise önce yerleşim 1'den malzeme çekersiniz.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="5f1f4-142">Madde onayı</span><span class="sxs-lookup"><span data-stu-id="5f1f4-142">Item confirmation</span></span>

<span data-ttu-id="5f1f4-143">Küme malzeme çekme uygulandığında, öğe yapılandırması maddelerin kümelere eklendiğinden emin olmak için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="5f1f4-144">Küme malzeme çekme işlemi sırasında küme malzeme çekme içerisindeki öğeleri doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="5f1f4-145">Kurulum ürün barkod kurulumuna dayanır.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="5f1f4-146">Küme malzeme çekme ile madde doğrulamayı ayarlamak</span><span class="sxs-lookup"><span data-stu-id="5f1f4-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="5f1f4-147">Mobil cihaz menü öğesinden iş onayı için kurulum formunu açın: **Ambar yönetimi** \> **Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menü öğeleri**.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="5f1f4-148">Mobil cihaz menü öğesinden **İş onayı ayarını** açın.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="5f1f4-149">**Ürün onayı** seçeneği tarandığında her stok parçasını mobil cihazınızdan doğrulamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="5f1f4-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
