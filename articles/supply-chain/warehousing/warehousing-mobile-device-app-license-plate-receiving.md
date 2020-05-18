---
title: Ambarlama uygulaması aracılığıyla plaka teslim alma
description: Bu konu, fiziksel stoğu almak için bir plaka teslim alma işlemi kullanmayı desteklemek üzere ambarlama uygulamasının nasıl ayarlanacağını açıklamaktadır.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346388"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a><span data-ttu-id="de43b-103">Ambarlama uygulaması aracılığıyla plaka teslim alma</span><span class="sxs-lookup"><span data-stu-id="de43b-103">License plate receiving via the warehousing app</span></span>

<span data-ttu-id="de43b-104">Bu konu, fiziksel stoğu almak için bir plaka teslim alma işlemi kullanmayı destekleyecek şekilde ambarlama uygulasımanın nasıl ayarlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="de43b-104">This topic explains how to set up the warehousing app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="de43b-105">Bu işlevi, bir ön sevkiyat bildirimi (ÖSB) ile ilgili gelen stoğun girişini hızlı bir şekilde kaydetmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de43b-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="de43b-106">Ambar yönetim işlemleri transfer emri sevk etmek için kullanıldığında, sistem otomatik olarak bir ÖSB oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de43b-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="de43b-107">Satınalma siparişi işlemi için, ÖSB el ile kaydedilebilir veya bir gelen ÖSB veri varlığı işlemi kullanılarak otomatik olarak içe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="de43b-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="de43b-108">ÖSB verileri, paletlerin (ana plakalar) kutular içerebildiği (iç içe geçmiş plakalar) *paketleme yapıları* aracılığıyla yüklere ve sevkiyatlara bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="de43b-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="de43b-109">İç içe geçmiş plakalara sahip paketleme yapıları kullanıldığında, stok hareketlerinin sayısını azaltmak için sistem ana plakadaki fiziksel eldeki stoku kaydeder.</span><span class="sxs-lookup"><span data-stu-id="de43b-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="de43b-110">Fiziksel eldeki stoğun hareketinin ana plakadan iç içe geçmiş plakalara taşınmasını tetiklemek için, paketleme yapısı verilerine göre, mobil cihazın *İçe içe geçmiş plakalara paketle* işi oluşturma işlemini temel alan bir menü öğesi sağlaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="de43b-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="de43b-111">Teslim alma özet sayfasını gösterme veya atlama</span><span class="sxs-lookup"><span data-stu-id="de43b-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="de43b-112">*Mobil cihazlarda teslim alma özet sayfası görüntülenip görüntülenmeyeceğni denetle* özelliğini, plaka teslim alma işleminin bir parçası olarak ek bir ayrıntılı ambarlama uygulaması akışından yararlanmak üzere kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de43b-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed warehousing app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="de43b-113">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="de43b-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="de43b-114">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="de43b-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="de43b-115">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="de43b-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="de43b-116">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="de43b-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="de43b-117">**Özellik adı:** *Mobil cihazlarda bir teslim alma özet sayfasının görüntülenip görüntülenmeyeceğini denetler*</span><span class="sxs-lookup"><span data-stu-id="de43b-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="de43b-118">Bu özellik etkinleştirildiğinde, plaka teslim alma veya plaka teslim alma ve yerine koyma için mobil cihaz menüsü öğeleri bir **Teslim alma özeti sayfası görüntüle** ayarı sağlar.</span><span class="sxs-lookup"><span data-stu-id="de43b-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="de43b-119">Bu ayar aşağıdaki seçeneklere sahiptir:</span><span class="sxs-lookup"><span data-stu-id="de43b-119">This setting has the following options:</span></span>

- <span data-ttu-id="de43b-120">**Ayrıntılı özet görüntüle** - Plaka teslim alma sırasında çalışanlar tam ÖSB bilgilerini gösteren ek bir sayfa görürler.</span><span class="sxs-lookup"><span data-stu-id="de43b-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="de43b-121">**Özeti atla** – Çalışanlar tüm ÖSB bilgilerini göremez.</span><span class="sxs-lookup"><span data-stu-id="de43b-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="de43b-122">Ambar çalışanları da bir değerlendirme kodu ayarlayamaz veya teslim alma işlemi sırasında özel durumlar ekleyemez.</span><span class="sxs-lookup"><span data-stu-id="de43b-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="de43b-123">Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelleme</span><span class="sxs-lookup"><span data-stu-id="de43b-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="de43b-124">Bir ÖSB zaten varolan plaka kimliği içeriyorsa ve plaka kaydının oluştuğu ambar yerleşimden başka bir ambar yerleşimindeki eldeki fiziksel stok verilerine sahipse, plaka teslim alma işlemi kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="de43b-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="de43b-125">Transit ambarının plakaları izlemediği (ve bu nedenle her plaka için fiziksel eldeki stoğu izlemediği) transfer emri senaryoları için, transitteki plakaların fiziksel eldeki stoklarının güncelleştirilmesini önlemek için *Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelle* özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de43b-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="de43b-126">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="de43b-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="de43b-127">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="de43b-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="de43b-128">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="de43b-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="de43b-129">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="de43b-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="de43b-130">**Özellik adı:** *Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelleme*</span><span class="sxs-lookup"><span data-stu-id="de43b-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="de43b-131">Bu özellik kullanılabilir olduğunda işlevselliği yönetmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="de43b-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="de43b-132">**Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="de43b-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="de43b-133">**Genel** sekmesinde **Plakalar** hızlı sekmesinde, **Transit ambarı plaka ilkesi** alanını aşağıdaki değerlerden birine ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="de43b-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="de43b-134">**İzlenemeyen plakanın yeniden kullanılmasına izin ver** – Sistem, *Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelleme* özelliğinin kullanılabilir olmadığı durumlardaki gibi çalışır.</span><span class="sxs-lookup"><span data-stu-id="de43b-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="de43b-135">Bu değer, özelliği ilk etkinleştirdiğinizde varsayılan ayardır.</span><span class="sxs-lookup"><span data-stu-id="de43b-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="de43b-136">**İzlenmeyen plakanın yeniden kullanılmasını engelle** – Transfer emri alınana kadar hedef ambarda, yalnızca sevk edilen plakayla ilgili olan eldeki stok güncelleştirmelerine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="de43b-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="de43b-137">Daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="de43b-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="de43b-138">Mobil cihaz menü öğeleri hakkında daha fazla bilgi için bkz. [Ambar işi için mobil cihazları ayarlama](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="de43b-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
