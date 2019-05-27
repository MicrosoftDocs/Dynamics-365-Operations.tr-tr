---
title: Taşıma yükü kısmi sevkiyatı
description: Bu konu yükü nasıl kısmen sevk edebileceğinizi ve yük için kapasite planlamasını nasıl erteleyebileceğinizi açıklar.
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c172f1b66e56f60e89f56ea98910f8d0e4f3e36
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545279"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="57847-103">Taşıma yükü kısmi sevkiyatı</span><span class="sxs-lookup"><span data-stu-id="57847-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="57847-104">Yüklerin kısmi sevkiyatını ayarlayarak bir yüke tüm satış satırları eklenene kadar kapasitenin belirlenemediği yükleri işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57847-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="57847-105">İşlem kesin palet sayısı bilindiğinde sonlandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="57847-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="57847-106">Bu nedenle, bir taşıma fiziksel olarak hazırlanmış stoktan yüklendiği zamana kadar hangi paletlerin hangi taşımaya atanacağına karar vermeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="57847-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="57847-107">Bu özellik, malzeme çekme veya yükleme işi oluşturulmadan önce hangi paletlerin hangi taşımaya atanacağını belirlemenizi gerektiren daha katı yapı bir yapının oluşturduğu zorlamaya bir alternatif sunar.</span><span class="sxs-lookup"><span data-stu-id="57847-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="57847-108">Bunun yerine, kullanıcılar kısmı bir sevkiyat onayı için tek tek yükleri yapılandırabilir.</span><span class="sxs-lookup"><span data-stu-id="57847-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="57847-109">Bu yükler için taşıma yüklemesi işlemleri daha sonra gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="57847-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="57847-110">Bu nedenle, taşıma planlama departmanı yükleri tek tek taşıyıcıların kapasitesini dikkate almak zorunda kalmadan planlayabilir.</span><span class="sxs-lookup"><span data-stu-id="57847-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="57847-111">Yükleme zamanında, çalışanlar paletin yüklenebileceği yeni bir taşıma yükü tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="57847-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="57847-112">Alternatif olarak, varolan bir taşıma yükü tanımlayabilirler.</span><span class="sxs-lookup"><span data-stu-id="57847-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="57847-113">Bu veriler bir mobil cihazla kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="57847-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="57847-114">Bu nedenle, birden fazla ambar çalışanı yanı kamyona aynı yüklerden veya farklı yüklerden stok yükleyebilir.</span><span class="sxs-lookup"><span data-stu-id="57847-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="57847-115">Yükler daha sonra tamamen veya kısmen sevk edilebilir.</span><span class="sxs-lookup"><span data-stu-id="57847-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="57847-116">Stoğu bir yükten belirli bir taşıma yüküne yüklemek ve yükü kısmen sevk etmek için işin iş şablonunda yükleme sınıfı kullanılarak oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="57847-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="57847-117">**Malzeme çekme** türündeki normal malzeme çekme işi kamyon gibi bir taşıma yüküne yüklenemez.</span><span class="sxs-lookup"><span data-stu-id="57847-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="57847-118">Kısmi sevkiyat için taşıma yüklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="57847-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="57847-119">Yüklerin kısmı sevkiyatının kurulumu aşağıdaki iki yordamdan oluşur.</span><span class="sxs-lookup"><span data-stu-id="57847-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="57847-120">Yükleme stratejisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="57847-120">Set the loading strategy</span></span>

<span data-ttu-id="57847-121">Yükleme stratejisini ayarlayarak kısmi yüklemeyi etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="57847-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="57847-122">Bir yük oluşturduktan sonra yükleme stratejisini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57847-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="57847-123">**Ambar yönetimi** \> **Yükler** \> **Tüm yükler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57847-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="57847-124">Bir yük seçin, sonra **Başlık** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="57847-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="57847-125">**Yükleme stratejisi** alanında **Kısmi yük sevkiyatına izin verildi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="57847-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="57847-126">Taşıma yüklerinin yüklenmesi için bir menü öğesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="57847-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="57847-127">Yüklenecek taşıma yüklerini etkinleştiren yeni bir menü öğesi oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="57847-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="57847-128">Bir taşıma yükü iş satırlarını bir yükten veya birden fazla yükten gruplandırmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="57847-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="57847-129">Taşıma yüküne eklenen her şey bir mobil tarayıcı kullanılarak sevk edilebilir.</span><span class="sxs-lookup"><span data-stu-id="57847-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="57847-130">**Ambar yönetimi** \> **Kurulum** \> **Mobil cihaz** \> **Mobil cihaz menüsü öğeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="57847-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="57847-131">**Yeni**'yi seçin ve sonra **Mod** alanında, **İş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57847-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="57847-132">**Mevcut işi kullan** seçeneğinde **Evet**'i işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="57847-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="57847-133">**Genel** sekmesinde, **Yöneten** alanında **Taşıma yüklemesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="57847-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="57847-134">Bir mobil tarayıcıdan sevkiyat onayını etkinleştirmek için **İzin verilen sevk onay türü** alanında **Taşıma yükü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="57847-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="57847-135">Bir taşıma yükünün sevkiyatını istemciden onaylama</span><span class="sxs-lookup"><span data-stu-id="57847-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="57847-136">Bu ayar sevk edilecek bir tam yük veya kısmen yüklenmiş yük içeren bir taşıma yükünü onaylamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="57847-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="57847-137">**Ambar yönetimi** \> **Yükler** \> **Taşıma yükleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="57847-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="57847-138">Eylem Bölmesinde **Sevk ve teslim alma** sekmesindeki **Onayla** grubunda **Taşıma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57847-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>
