---
title: Warehouse Management mobil uygulaması için adım simgeleri ve başlıklar atama
description: Bu konuda, Warehouse Management mobil uygulaması için yeni veya özelleştirilmiş görev akışları için adım simgelerinin ve başlıklarının nasıl atandığı açıklanmaktadır.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049376"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="a320b-103">Warehouse Management mobil uygulaması için adım simgeleri ve başlıklar atama</span><span class="sxs-lookup"><span data-stu-id="a320b-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a320b-104">Bu konuda, Warehouse Management mobil uygulaması için yeni veya özelleştirilmiş görev akışları için adım simgelerinin ve adım başlıklarının nasıl atandığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a320b-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="a320b-105">Aşağıdaki çizimlerde, adım simgelerinin ve başlıkların Warehouse Management mobil uygulamasında nasıl göründüğü gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a320b-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="a320b-106">![Warehouse Management mobil uygulamasında adım simgesi ve adım başlığı örneği](media/step-icon-example.png "Warehouse Management mobil uygulamasında adım simgesi ve adım başlığı örneği")</span><span class="sxs-lookup"><span data-stu-id="a320b-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="a320b-107">Sisteminizde bu özelliği etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a320b-107">Turn on this feature in your system</span></span>

<span data-ttu-id="a320b-108">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a320b-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a320b-109">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="a320b-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="a320b-110">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="a320b-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a320b-111">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="a320b-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a320b-112">**Özellik adı:** *Yeni ambar uygulaması için kullanıcı ayarları, simgeler ve adım başlıkları*</span><span class="sxs-lookup"><span data-stu-id="a320b-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="a320b-113">Standart adım kimlikleri, sınıflar ve simgeler</span><span class="sxs-lookup"><span data-stu-id="a320b-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="a320b-114">Görev akışındaki her adım bir adım kimliğiyle tanımlanır ve her adım kimliğinin karşılık gelen bir adım sınıfı vardır.</span><span class="sxs-lookup"><span data-stu-id="a320b-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="a320b-115">Adım simgesi ve başlığı her adım sınıfında belirtilir.</span><span class="sxs-lookup"><span data-stu-id="a320b-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="a320b-116">Adım kimlikleri ve adım sınıfları</span><span class="sxs-lookup"><span data-stu-id="a320b-116">Step IDs and step classes</span></span>

<span data-ttu-id="a320b-117">Aşağıdaki tabloda, şu anda kullanılabilen her adım kimliği listelenmiştir ve bu, karşılık gelen adım sınıfıdır.</span><span class="sxs-lookup"><span data-stu-id="a320b-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="a320b-118">Birincil giriş alanının denetim adı adım kimliği olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a320b-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="a320b-119">Bu adım kimliklerinin ve sınıflarının nasıl kullanıldığını gösteren bir örnek için, bu konunun sonraki bölümlerinde yer alan [Örnek: Özel akış bölümü için adım simgeleri ve başlıklar atama](#example) bölümünde `WHSMobileAppStepInfoBuilder.stepId()` yöntemin uygulanmasına bakın.</span><span class="sxs-lookup"><span data-stu-id="a320b-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="a320b-120">Adım kodu</span><span class="sxs-lookup"><span data-stu-id="a320b-120">Step ID</span></span> | <span data-ttu-id="a320b-121">Adım Sınıfı</span><span class="sxs-lookup"><span data-stu-id="a320b-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="a320b-122">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="a320b-122">BatchDisposition</span></span> | <span data-ttu-id="a320b-123">WHSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="a320b-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="a320b-124">Taşıyıcı</span><span class="sxs-lookup"><span data-stu-id="a320b-124">Carrier</span></span> | <span data-ttu-id="a320b-125">WHSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="a320b-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="a320b-126">CatchWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-126">CatchWeight</span></span> | <span data-ttu-id="a320b-127">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="a320b-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="a320b-129">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="a320b-130">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="a320b-130">CatchWeightTag</span></span> | <span data-ttu-id="a320b-131">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="a320b-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="a320b-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="a320b-133">WHSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="a320b-134">ChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="a320b-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="a320b-135">WHSMobileAppStepChangeWarehouseSuccess</span><span class="sxs-lookup"><span data-stu-id="a320b-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="a320b-136">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="a320b-136">CheckDigit</span></span> | <span data-ttu-id="a320b-137">WHSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="a320b-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="a320b-138">ClusterId</span><span class="sxs-lookup"><span data-stu-id="a320b-138">ClusterId</span></span> | <span data-ttu-id="a320b-139">WHSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="a320b-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="a320b-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="a320b-141">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="a320b-142">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="a320b-142">ClusterPosition</span></span> | <span data-ttu-id="a320b-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="a320b-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="a320b-144">ConfigId</span><span class="sxs-lookup"><span data-stu-id="a320b-144">ConfigId</span></span> | <span data-ttu-id="a320b-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="a320b-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="a320b-146">Onay</span><span class="sxs-lookup"><span data-stu-id="a320b-146">Confirmation</span></span> | <span data-ttu-id="a320b-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="a320b-148">ConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="a320b-149">WHSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="a320b-150">ConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="a320b-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="a320b-152">ConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="a320b-153">WHSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="a320b-154">ContainerType</span><span class="sxs-lookup"><span data-stu-id="a320b-154">ContainerType</span></span> | <span data-ttu-id="a320b-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="a320b-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="a320b-156">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="a320b-156">CountingReasonCode</span></span> | <span data-ttu-id="a320b-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="a320b-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="a320b-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="a320b-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="a320b-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="a320b-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="a320b-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="a320b-160">CycleCountQty1</span></span> | <span data-ttu-id="a320b-161">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="a320b-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="a320b-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="a320b-162">CycleCountQty2</span></span> | <span data-ttu-id="a320b-163">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="a320b-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="a320b-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="a320b-164">CycleCountQty3</span></span> | <span data-ttu-id="a320b-165">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="a320b-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="a320b-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="a320b-166">CycleCountQty4</span></span> | <span data-ttu-id="a320b-167">WHSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="a320b-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="a320b-168">Elden Çıkarma</span><span class="sxs-lookup"><span data-stu-id="a320b-168">Disposition</span></span> | <span data-ttu-id="a320b-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="a320b-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="a320b-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="a320b-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="a320b-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="a320b-172">DriverCheckInId</span></span> | <span data-ttu-id="a320b-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="a320b-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="a320b-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="a320b-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="a320b-176">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="a320b-176">DriverCheckOutId</span></span> | <span data-ttu-id="a320b-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="a320b-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="a320b-178">ExpDate</span><span class="sxs-lookup"><span data-stu-id="a320b-178">ExpDate</span></span> | <span data-ttu-id="a320b-179">WHSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="a320b-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="a320b-180">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="a320b-180">FromBatchDisposition</span></span> | <span data-ttu-id="a320b-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="a320b-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="a320b-182">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="a320b-182">FromInventoryStatus</span></span> | <span data-ttu-id="a320b-183">WHSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="a320b-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="a320b-184">FullQty</span><span class="sxs-lookup"><span data-stu-id="a320b-184">FullQty</span></span> | <span data-ttu-id="a320b-185">WHSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="a320b-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="a320b-186">InboundPut</span><span class="sxs-lookup"><span data-stu-id="a320b-186">InboundPut</span></span> | <span data-ttu-id="a320b-187">WHSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="a320b-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="a320b-188">InventBatchId</span><span class="sxs-lookup"><span data-stu-id="a320b-188">InventBatchId</span></span> | <span data-ttu-id="a320b-189">WHSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="a320b-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="a320b-190">InventColorId</span><span class="sxs-lookup"><span data-stu-id="a320b-190">InventColorId</span></span> | <span data-ttu-id="a320b-191">WHSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="a320b-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="a320b-192">InventLocation</span><span class="sxs-lookup"><span data-stu-id="a320b-192">InventLocation</span></span> | <span data-ttu-id="a320b-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="a320b-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="a320b-194">InventLocationId</span><span class="sxs-lookup"><span data-stu-id="a320b-194">InventLocationId</span></span> | <span data-ttu-id="a320b-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="a320b-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="a320b-196">InventSerialId</span><span class="sxs-lookup"><span data-stu-id="a320b-196">InventSerialId</span></span> | <span data-ttu-id="a320b-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="a320b-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="a320b-198">InventSizeId</span><span class="sxs-lookup"><span data-stu-id="a320b-198">InventSizeId</span></span> | <span data-ttu-id="a320b-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="a320b-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="a320b-200">InventStatusId</span><span class="sxs-lookup"><span data-stu-id="a320b-200">InventStatusId</span></span> | <span data-ttu-id="a320b-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="a320b-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="a320b-202">InventStyleId</span><span class="sxs-lookup"><span data-stu-id="a320b-202">InventStyleId</span></span> | <span data-ttu-id="a320b-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="a320b-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="a320b-204">InventVersionId</span><span class="sxs-lookup"><span data-stu-id="a320b-204">InventVersionId</span></span> | <span data-ttu-id="a320b-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="a320b-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="a320b-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="a320b-206">ItemId</span></span> | <span data-ttu-id="a320b-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="a320b-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="a320b-208">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="a320b-208">ITMContainerID</span></span> | <span data-ttu-id="a320b-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="a320b-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="a320b-210">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="a320b-210">ITMShipmentID</span></span> | <span data-ttu-id="a320b-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="a320b-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="a320b-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="a320b-212">KanbanCardId</span></span> | <span data-ttu-id="a320b-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="a320b-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="a320b-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="a320b-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="a320b-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="a320b-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="a320b-216">KanbanOrCardId</span><span class="sxs-lookup"><span data-stu-id="a320b-216">KanbanOrCardId</span></span> | <span data-ttu-id="a320b-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="a320b-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="a320b-218">LicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-218">LicensePlateId</span></span> | <span data-ttu-id="a320b-219">WHSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="a320b-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="a320b-220">LoadId</span><span class="sxs-lookup"><span data-stu-id="a320b-220">LoadId</span></span> | <span data-ttu-id="a320b-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="a320b-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="a320b-222">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="a320b-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="a320b-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="a320b-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="a320b-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="a320b-224">LocOrLP</span></span> | <span data-ttu-id="a320b-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="a320b-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="a320b-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="a320b-226">LocOrLP_From</span></span> | <span data-ttu-id="a320b-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="a320b-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="a320b-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="a320b-228">LocOrLP_To</span></span> | <span data-ttu-id="a320b-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="a320b-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="a320b-230">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="a320b-230">LocOrLPCheck</span></span> | <span data-ttu-id="a320b-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="a320b-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="a320b-232">LocVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-232">LocVerification</span></span> | <span data-ttu-id="a320b-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="a320b-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="a320b-234">LPAdjustIn</span></span> | <span data-ttu-id="a320b-235">WHSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="a320b-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="a320b-236">LPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="a320b-236">LPBreakChildLP</span></span> | <span data-ttu-id="a320b-237">WHSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="a320b-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="a320b-238">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="a320b-238">LPBreakParentLP</span></span> | <span data-ttu-id="a320b-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="a320b-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="a320b-240">LPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="a320b-240">LPBuildChildLP</span></span> | <span data-ttu-id="a320b-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="a320b-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="a320b-242">LPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="a320b-242">LPBuildParentLP</span></span> | <span data-ttu-id="a320b-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="a320b-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="a320b-244">LPVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-244">LPVerification</span></span> | <span data-ttu-id="a320b-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="a320b-246">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="a320b-246">MergeContainerId</span></span> | <span data-ttu-id="a320b-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="a320b-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="a320b-248">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="a320b-248">MixedLPLineNum</span></span> | <span data-ttu-id="a320b-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="a320b-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="a320b-250">MobileDeviceQueueMessageCollectionIdentifierId</span><span class="sxs-lookup"><span data-stu-id="a320b-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="a320b-251">WHSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="a320b-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="a320b-252">MovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="a320b-252">MovementConfirmCancel</span></span> | <span data-ttu-id="a320b-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="a320b-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="a320b-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-254">NewCaptureWeight</span></span> | <span data-ttu-id="a320b-255">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="a320b-256">NewQty</span><span class="sxs-lookup"><span data-stu-id="a320b-256">NewQty</span></span> | <span data-ttu-id="a320b-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="a320b-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="a320b-258">OutboundCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="a320b-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="a320b-259">WHSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="a320b-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="a320b-260">OutboundPut</span><span class="sxs-lookup"><span data-stu-id="a320b-260">OutboundPut</span></span> | <span data-ttu-id="a320b-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="a320b-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="a320b-262">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-262">OutboundWeight</span></span> | <span data-ttu-id="a320b-263">WHSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="a320b-264">OverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="a320b-264">OverridePutNewLocation</span></span> | <span data-ttu-id="a320b-265">WHSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="a320b-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="a320b-266">PieceByPieceConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="a320b-267">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="a320b-268">POLineNum</span><span class="sxs-lookup"><span data-stu-id="a320b-268">POLineNum</span></span> | <span data-ttu-id="a320b-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="a320b-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="a320b-270">Satın Alma Siparişi Numarası</span><span class="sxs-lookup"><span data-stu-id="a320b-270">PONum</span></span> | <span data-ttu-id="a320b-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="a320b-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="a320b-272">PositionFull</span><span class="sxs-lookup"><span data-stu-id="a320b-272">PositionFull</span></span> | <span data-ttu-id="a320b-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="a320b-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="a320b-274">PositionFullQty</span><span class="sxs-lookup"><span data-stu-id="a320b-274">PositionFullQty</span></span> | <span data-ttu-id="a320b-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="a320b-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="a320b-276">Kuvvet</span><span class="sxs-lookup"><span data-stu-id="a320b-276">Potency</span></span> | <span data-ttu-id="a320b-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="a320b-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="a320b-278">PrinterName</span><span class="sxs-lookup"><span data-stu-id="a320b-278">PrinterName</span></span> | <span data-ttu-id="a320b-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="a320b-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="a320b-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="a320b-280">ProdId</span></span> | <span data-ttu-id="a320b-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="a320b-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="a320b-282">ProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="a320b-283">WHSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="a320b-284">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-284">ProductConfirmation</span></span> | <span data-ttu-id="a320b-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="a320b-286">ProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="a320b-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="a320b-288">Yerine Koy</span><span class="sxs-lookup"><span data-stu-id="a320b-288">Put</span></span> | <span data-ttu-id="a320b-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="a320b-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="a320b-290">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="a320b-290">PutawayClusterId</span></span> | <span data-ttu-id="a320b-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="a320b-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="a320b-292">Miktar</span><span class="sxs-lookup"><span data-stu-id="a320b-292">Qty</span></span> | <span data-ttu-id="a320b-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="a320b-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="a320b-294">QtyAdjust</span><span class="sxs-lookup"><span data-stu-id="a320b-294">QtyAdjust</span></span> | <span data-ttu-id="a320b-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="a320b-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="a320b-296">QtyShort</span><span class="sxs-lookup"><span data-stu-id="a320b-296">QtyShort</span></span> | <span data-ttu-id="a320b-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="a320b-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="a320b-298">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="a320b-298">QtyToConsume</span></span> | <span data-ttu-id="a320b-299">WHSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="a320b-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="a320b-300">QtyToPick</span><span class="sxs-lookup"><span data-stu-id="a320b-300">QtyToPick</span></span> | <span data-ttu-id="a320b-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="a320b-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="a320b-302">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="a320b-302">QtyToPut</span></span> | <span data-ttu-id="a320b-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="a320b-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="a320b-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="a320b-304">QtyToScrap</span></span> | <span data-ttu-id="a320b-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="a320b-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="a320b-306">QtyVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-306">QtyVerification</span></span> | <span data-ttu-id="a320b-307">WHSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="a320b-308">QtyWithScanningLimit</span><span class="sxs-lookup"><span data-stu-id="a320b-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="a320b-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="a320b-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="a320b-310">ReasonString</span><span class="sxs-lookup"><span data-stu-id="a320b-310">ReasonString</span></span> | <span data-ttu-id="a320b-311">WHSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="a320b-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="a320b-312">RecvLocationId</span><span class="sxs-lookup"><span data-stu-id="a320b-312">RecvLocationId</span></span> | <span data-ttu-id="a320b-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="a320b-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="a320b-314">RemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="a320b-314">RemoveContainerId</span></span> | <span data-ttu-id="a320b-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="a320b-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="a320b-316">ReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="a320b-317">WHSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="a320b-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="a320b-318">RMANum</span></span> | <span data-ttu-id="a320b-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="a320b-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="a320b-320">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="a320b-320">ShortPickReason</span></span> | <span data-ttu-id="a320b-321">WHSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="a320b-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="a320b-322">SortConOrLP</span><span class="sxs-lookup"><span data-stu-id="a320b-322">SortConOrLP</span></span> | <span data-ttu-id="a320b-323">WHSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="a320b-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="a320b-324">SortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-324">SortLicensePlateId</span></span> | <span data-ttu-id="a320b-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="a320b-326">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="a320b-326">SortPositionId</span></span> | <span data-ttu-id="a320b-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="a320b-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="a320b-328">SortVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-328">SortVerification</span></span> | <span data-ttu-id="a320b-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="a320b-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="a320b-330">StartLocationId</span><span class="sxs-lookup"><span data-stu-id="a320b-330">StartLocationId</span></span> | <span data-ttu-id="a320b-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="a320b-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="a320b-332">StartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="a320b-333">WHSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="a320b-334">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-334">TargetLicensePlateId</span></span> | <span data-ttu-id="a320b-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="a320b-336">TOLineNum</span><span class="sxs-lookup"><span data-stu-id="a320b-336">TOLineNum</span></span> | <span data-ttu-id="a320b-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="a320b-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="a320b-338">ToLocation</span><span class="sxs-lookup"><span data-stu-id="a320b-338">ToLocation</span></span> | <span data-ttu-id="a320b-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="a320b-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="a320b-340">TONum</span><span class="sxs-lookup"><span data-stu-id="a320b-340">TONum</span></span> | <span data-ttu-id="a320b-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="a320b-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="a320b-342">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="a320b-342">ToWarehouse</span></span> | <span data-ttu-id="a320b-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="a320b-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="a320b-344">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="a320b-344">TransportLoadId</span></span> | <span data-ttu-id="a320b-345">WHSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="a320b-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="a320b-346">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="a320b-346">WaveLabelId</span></span> | <span data-ttu-id="a320b-347">WHSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="a320b-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="a320b-348">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="a320b-348">WaveLblQty</span></span> | <span data-ttu-id="a320b-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="a320b-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="a320b-350">Ağırlık</span><span class="sxs-lookup"><span data-stu-id="a320b-350">Weight</span></span> | <span data-ttu-id="a320b-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="a320b-352">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="a320b-352">WeightToConsume</span></span> | <span data-ttu-id="a320b-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="a320b-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="a320b-354">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="a320b-354">WHSAdjustmentType</span></span> | <span data-ttu-id="a320b-355">WHSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="a320b-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="a320b-356">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="a320b-356">WHSReceivingException</span></span> | <span data-ttu-id="a320b-357">WHSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="a320b-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="a320b-358">WHSWorkException</span><span class="sxs-lookup"><span data-stu-id="a320b-358">WHSWorkException</span></span> | <span data-ttu-id="a320b-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="a320b-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="a320b-360">WHSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="a320b-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="a320b-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="a320b-362">WMSLocationId</span></span> | <span data-ttu-id="a320b-363">WHSMobileAppStepLocation</span><span class="sxs-lookup"><span data-stu-id="a320b-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="a320b-364">WorkId</span><span class="sxs-lookup"><span data-stu-id="a320b-364">WorkId</span></span> | <span data-ttu-id="a320b-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="a320b-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="a320b-366">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="a320b-366">WorkIdToCancel</span></span> | <span data-ttu-id="a320b-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="a320b-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="a320b-368">WorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="a320b-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="a320b-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="a320b-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="a320b-370">WorkPoolId</span><span class="sxs-lookup"><span data-stu-id="a320b-370">WorkPoolId</span></span> | <span data-ttu-id="a320b-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="a320b-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="a320b-372">ZoneId</span><span class="sxs-lookup"><span data-stu-id="a320b-372">ZoneId</span></span> | <span data-ttu-id="a320b-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="a320b-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="a320b-374">Kullanılabilir adım simgeleri</span><span class="sxs-lookup"><span data-stu-id="a320b-374">Available step icons</span></span>

<span data-ttu-id="a320b-375">Sistem, özel adımlarınız için de kullanabileceğiniz standart adım simgeleri koleksiyonu içerir.</span><span class="sxs-lookup"><span data-stu-id="a320b-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="a320b-376">Şu anda özel adım simgelerini yükleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="a320b-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="a320b-377">Bu nedenle, her zaman standart adım simgelerinden birini seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="a320b-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="a320b-378">Aşağıdaki tabloda, şu anda kullanılabilen her standart adım simgesi ve adı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a320b-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Adım simgesi hakkında"><br><span data-ttu-id="a320b-380">Hakkında</span><span class="sxs-lookup"><span data-stu-id="a320b-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Plaka veya öğe adımı simgesi ekleme"><br><span data-ttu-id="a320b-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="a320b-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Toplu iş değerlendirme adım simgesi"><br><span data-ttu-id="a320b-384">BatchDisposition</span><span class="sxs-lookup"><span data-stu-id="a320b-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Operatör adımı simgesi"><br><span data-ttu-id="a320b-386">Taşıyıcı</span><span class="sxs-lookup"><span data-stu-id="a320b-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Fiili ağırlık etiketi adım simgesi"><br><span data-ttu-id="a320b-388">CatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="a320b-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Fiili ağırlık etiketi ağırlık adım simgesi"><br><span data-ttu-id="a320b-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Basamak adımını denetle simgesi"><br><span data-ttu-id="a320b-392">CheckDigit</span><span class="sxs-lookup"><span data-stu-id="a320b-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Kimlik giriş veya çıkış adım simgesi"><br><span data-ttu-id="a320b-394">CheckInOutId</span><span class="sxs-lookup"><span data-stu-id="a320b-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Alt lisans plakası adımı simgesi"><br><span data-ttu-id="a320b-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="a320b-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Küme Kimliği adım simgesi"><br><span data-ttu-id="a320b-398">ClusterId</span><span class="sxs-lookup"><span data-stu-id="a320b-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Küme pozisyonu adım simgesi"><br><span data-ttu-id="a320b-400">ClusterPosition</span><span class="sxs-lookup"><span data-stu-id="a320b-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Yapılandırma Kimliği adım simgesi"><br><span data-ttu-id="a320b-402">ConfigId</span><span class="sxs-lookup"><span data-stu-id="a320b-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Yapılandırılmış alan adımı simgesi"><br><span data-ttu-id="a320b-404">ConfiguredField</span><span class="sxs-lookup"><span data-stu-id="a320b-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con veya LP adım simgesi"><br><span data-ttu-id="a320b-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="a320b-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Plaka kimliği adımı simgesinden konsolide"><br><span data-ttu-id="a320b-408">ConsolidateFromLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="a320b-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Plaka kimliği adımı simgesine konsolide"><br><span data-ttu-id="a320b-410">ConsolidateToLicensePlateID</span><span class="sxs-lookup"><span data-stu-id="a320b-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Kapsayıcı türü adım simgesi"><br><span data-ttu-id="a320b-412">ContainerType</span><span class="sxs-lookup"><span data-stu-id="a320b-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Adım sayma simgesi"><br><span data-ttu-id="a320b-414">Sayım</span><span class="sxs-lookup"><span data-stu-id="a320b-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Neden kodu adımı simgesini sayma"><br><span data-ttu-id="a320b-416">CountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="a320b-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Menşe ülke kodu adımı simgesi"><br><span data-ttu-id="a320b-418">CountryOfOrigin</span><span class="sxs-lookup"><span data-stu-id="a320b-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Değerlendirme adım simgesi"><br><span data-ttu-id="a320b-420">Değerlendirme</span><span class="sxs-lookup"><span data-stu-id="a320b-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Bitti adımı simgesi"><br><span data-ttu-id="a320b-422">Bitti</span><span class="sxs-lookup"><span data-stu-id="a320b-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Sürücü iade onay adımı simgesi"><br><span data-ttu-id="a320b-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Kimlik adımı simgesinde sürücü denetimi"><br><span data-ttu-id="a320b-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="a320b-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Kimlik çıkış adımı simgesinde sürücü denetimi"><br><span data-ttu-id="a320b-428">DriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="a320b-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Son kullanma tarihi adımı simgesi"><br><span data-ttu-id="a320b-430">ExpDate</span><span class="sxs-lookup"><span data-stu-id="a320b-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Alan adımı simgesi"><br><span data-ttu-id="a320b-432">Alan</span><span class="sxs-lookup"><span data-stu-id="a320b-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Toplu iş değerlendirmeden adım simgesi"><br><span data-ttu-id="a320b-434">FromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="a320b-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Stok durumundan adımı simgesinden"><br><span data-ttu-id="a320b-436">FromInventoryStatus</span><span class="sxs-lookup"><span data-stu-id="a320b-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Kimlik özniteliği adım simgesi"><br><span data-ttu-id="a320b-438">IdAttribute</span><span class="sxs-lookup"><span data-stu-id="a320b-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Stok toplu iş kimliği adım simgesi"><br><span data-ttu-id="a320b-440">InventBatchID</span><span class="sxs-lookup"><span data-stu-id="a320b-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Stok renkli kimliği adım simgesi"><br><span data-ttu-id="a320b-442">InventColorID</span><span class="sxs-lookup"><span data-stu-id="a320b-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Stok konumu adım simgesi"><br><span data-ttu-id="a320b-444">InventLocation</span><span class="sxs-lookup"><span data-stu-id="a320b-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Stok seri kimliği adım simgesi"><br><span data-ttu-id="a320b-446">InventSerialID</span><span class="sxs-lookup"><span data-stu-id="a320b-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Stok boyut kimliği adım simgesi"><br><span data-ttu-id="a320b-448">InventSizeID</span><span class="sxs-lookup"><span data-stu-id="a320b-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Stok durumu kimliği adım simgesi"><br><span data-ttu-id="a320b-450">InventStatusID</span><span class="sxs-lookup"><span data-stu-id="a320b-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Stok stili kimliği adım simgesi"><br><span data-ttu-id="a320b-452">InventStyleID</span><span class="sxs-lookup"><span data-stu-id="a320b-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Stok sürümü kimliği adım simgesi"><br><span data-ttu-id="a320b-454">InventVersionID</span><span class="sxs-lookup"><span data-stu-id="a320b-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Madde Kimliği adım simgesi"><br><span data-ttu-id="a320b-456">ItemID</span><span class="sxs-lookup"><span data-stu-id="a320b-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM Kapsayıcı kimlik adım simgesi"><br><span data-ttu-id="a320b-458">ITMContainerID</span><span class="sxs-lookup"><span data-stu-id="a320b-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM sevkiyat kimliği adımı simgesi"><br><span data-ttu-id="a320b-460">ITMShipmentID</span><span class="sxs-lookup"><span data-stu-id="a320b-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban kart kimliği adım simgesi"><br><span data-ttu-id="a320b-462">KanbanCardID</span><span class="sxs-lookup"><span data-stu-id="a320b-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban veya kart kimliği adım simgesi"><br><span data-ttu-id="a320b-464">KanbanOrCardID</span><span class="sxs-lookup"><span data-stu-id="a320b-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Lisans plakası kimlik adım simgesi"><br><span data-ttu-id="a320b-466">LicensePlateID</span><span class="sxs-lookup"><span data-stu-id="a320b-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Yük Kimliği adım simgesi"><br><span data-ttu-id="a320b-468">LoadId</span><span class="sxs-lookup"><span data-stu-id="a320b-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Yerleşim plaka konum adım simgesi"><br><span data-ttu-id="a320b-470">LocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="a320b-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Konum veya lisans plakası adımı simgesi"><br><span data-ttu-id="a320b-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="a320b-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Konum veya lisans plakası denetim adımı simgesi"><br><span data-ttu-id="a320b-474">LocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="a320b-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Konum veya lisans plakasından adımı simgesi"><br><span data-ttu-id="a320b-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="a320b-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Konum veya lisans plakasına adımı simgesi"><br><span data-ttu-id="a320b-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="a320b-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Uzun işlem tamamlandı adım simgesi"><br><span data-ttu-id="a320b-480">LongProcessCompleted</span><span class="sxs-lookup"><span data-stu-id="a320b-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP kesme üst LP adım simgesi"><br><span data-ttu-id="a320b-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="a320b-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Birleştirme Kapsayıcı kimlik adım simgesi"><br><span data-ttu-id="a320b-484">MergeContainerId</span><span class="sxs-lookup"><span data-stu-id="a320b-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Karışık lisans plakası satır numarası adım simgesi"><br><span data-ttu-id="a320b-486">MixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="a320b-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Giden ağırlık adımı simgesi"><br><span data-ttu-id="a320b-488">OutboundWeight</span><span class="sxs-lookup"><span data-stu-id="a320b-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Sahip adımı simgesi"><br><span data-ttu-id="a320b-490">Sahip</span><span class="sxs-lookup"><span data-stu-id="a320b-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Üst lisans plakası adımı simgesi"><br><span data-ttu-id="a320b-492">ParentLP</span><span class="sxs-lookup"><span data-stu-id="a320b-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Lütfen onaylayın adım simgesi"><br><span data-ttu-id="a320b-494">PleaseConfirm</span><span class="sxs-lookup"><span data-stu-id="a320b-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Satın alma sipariş satır numarası adım simgesi"><br><span data-ttu-id="a320b-496">POLineNum</span><span class="sxs-lookup"><span data-stu-id="a320b-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Satın alma sipariş numarası adım simgesi"><br><span data-ttu-id="a320b-498">Satın Alma Siparişi Numarası</span><span class="sxs-lookup"><span data-stu-id="a320b-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Pozisyon tam adım simgesi"><br><span data-ttu-id="a320b-500">PositionFull</span><span class="sxs-lookup"><span data-stu-id="a320b-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Kuvvet adım simgesi"><br><span data-ttu-id="a320b-502">Kuvvet</span><span class="sxs-lookup"><span data-stu-id="a320b-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Yazıcı adı adım simgesi"><br><span data-ttu-id="a320b-504">PrinterName</span><span class="sxs-lookup"><span data-stu-id="a320b-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Ürün Kimliği adım simgesi"><br><span data-ttu-id="a320b-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="a320b-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Ürün onay adımı simgesi"><br><span data-ttu-id="a320b-508">ProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Yerine koy adım simgesi"><br><span data-ttu-id="a320b-510">Yerine Koy</span><span class="sxs-lookup"><span data-stu-id="a320b-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Yerine koyma küme Kimliği adım simgesi"><br><span data-ttu-id="a320b-512">PutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="a320b-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Miktar adımı simgesi"><br><span data-ttu-id="a320b-514">Miktar</span><span class="sxs-lookup"><span data-stu-id="a320b-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Miktar ayarlama adım simgesi"><br><span data-ttu-id="a320b-516">QtyAdjustIn</span><span class="sxs-lookup"><span data-stu-id="a320b-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Miktar kısa adımı simgesi"><br><span data-ttu-id="a320b-518">QtyShort</span><span class="sxs-lookup"><span data-stu-id="a320b-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Tüketilecek miktar adım simgesi"><br><span data-ttu-id="a320b-520">QtyToConsume</span><span class="sxs-lookup"><span data-stu-id="a320b-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Koyulacak miktar adım simgesi"><br><span data-ttu-id="a320b-522">QtyToPut</span><span class="sxs-lookup"><span data-stu-id="a320b-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Iskarta miktarı adım simgesi"><br><span data-ttu-id="a320b-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="a320b-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Miktar onay adımı simgesi"><br><span data-ttu-id="a320b-526">QuantityConfirmation</span><span class="sxs-lookup"><span data-stu-id="a320b-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Tamamlandı bildirimi bitiş işi adımı simgesi"><br><span data-ttu-id="a320b-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="a320b-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Konum kimliği adımı simgesini al"><br><span data-ttu-id="a320b-530">RecvLocationID</span><span class="sxs-lookup"><span data-stu-id="a320b-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Kaldırma Kapsayıcı kimlik adım simgesi"><br><span data-ttu-id="a320b-532">RemoveContainerID</span><span class="sxs-lookup"><span data-stu-id="a320b-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA numarası adımı simgesi"><br><span data-ttu-id="a320b-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="a320b-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Sipariş seç adımı simgesi"><br><span data-ttu-id="a320b-536">SelectOrder</span><span class="sxs-lookup"><span data-stu-id="a320b-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Kısa çekme nedeni adım simgesi"><br><span data-ttu-id="a320b-538">ShortPickReason</span><span class="sxs-lookup"><span data-stu-id="a320b-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Konum kimliğini sınıflandır adım simgesi"><br><span data-ttu-id="a320b-540">SortPositionId</span><span class="sxs-lookup"><span data-stu-id="a320b-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Hedef Lisans plakası kimlik adım simgesi"><br><span data-ttu-id="a320b-542">TargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Satır numarası adım simgesine"><br><span data-ttu-id="a320b-544">ToLineNum</span><span class="sxs-lookup"><span data-stu-id="a320b-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Konuma adım simgesi"><br><span data-ttu-id="a320b-546">ToLocation</span><span class="sxs-lookup"><span data-stu-id="a320b-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Numaraya adımı simgesi"><br><span data-ttu-id="a320b-548">ToNum</span><span class="sxs-lookup"><span data-stu-id="a320b-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Ambara adım simgesi"><br><span data-ttu-id="a320b-550">ToWarehouse</span><span class="sxs-lookup"><span data-stu-id="a320b-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Taşıma yükü Kimliği adım simgesi"><br><span data-ttu-id="a320b-552">TransportLoadId</span><span class="sxs-lookup"><span data-stu-id="a320b-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Satıcı toplu iş kimliği adım simgesi"><br><span data-ttu-id="a320b-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="a320b-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Dalga etiketi kimliği adım simgesi"><br><span data-ttu-id="a320b-556">WaveLabelId</span><span class="sxs-lookup"><span data-stu-id="a320b-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Dalga etiketi miktarı adım simgesi"><br><span data-ttu-id="a320b-558">WaveLblQty</span><span class="sxs-lookup"><span data-stu-id="a320b-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Ağırlık adımı simgesi"><br><span data-ttu-id="a320b-560">Ağırlık</span><span class="sxs-lookup"><span data-stu-id="a320b-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Tüketilecek ağırlık adım simgesi"><br><span data-ttu-id="a320b-562">WeightToConsume</span><span class="sxs-lookup"><span data-stu-id="a320b-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS ayar türü adım simgesi"><br><span data-ttu-id="a320b-564">WHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="a320b-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS özel durum alma adım simgesi"><br><span data-ttu-id="a320b-566">WHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="a320b-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS konum kimliği adım simgesi"><br><span data-ttu-id="a320b-568">WMSLocationID</span><span class="sxs-lookup"><span data-stu-id="a320b-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="İş Kimliği adım simgesi"><br><span data-ttu-id="a320b-570">WorkId</span><span class="sxs-lookup"><span data-stu-id="a320b-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="İptal edilecek iş kimliği Adım simgesi"><br><span data-ttu-id="a320b-572">WorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="a320b-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="İş Lisans plakası kimlik adım simgesi"><br><span data-ttu-id="a320b-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="a320b-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="İş Lisans plakası kimlik koyma kümesi adım simgesi"><br><span data-ttu-id="a320b-576">WorkLPIDPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="a320b-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="İş havuzu Kimliği adım simgesi"><br><span data-ttu-id="a320b-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="a320b-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Bölge Kimliği adım simgesi"><br><span data-ttu-id="a320b-580">ZoneID</span><span class="sxs-lookup"><span data-stu-id="a320b-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="a320b-581">Örnek: Özel akış bölümü için adım simgeleri ve başlıklar atama</span><span class="sxs-lookup"><span data-stu-id="a320b-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="a320b-582">Bu örnek, özel bir görev akışı için adım simgelerinin ve başlıklarının nasıl ayarlanıp ayarlananın açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a320b-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="a320b-583">Senaryo, aşağıdaki blog gönderisinde daha ayrıntılı olarak sunulan ve araştırılan özel bir görev akışı örneği üzerine kuruludur: [Depolama Mobil Uygulamasını Özelleştirme](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="a320b-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="a320b-584">Görev akışı aşağıdaki şekilde çalışır:</span><span class="sxs-lookup"><span data-stu-id="a320b-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="a320b-585">Uygulama, çalışandan bir kapsayıcı kimliği sağlamasını isteyen bir sayfa gösterir (örneğin, bir barkodu tarayarak).</span><span class="sxs-lookup"><span data-stu-id="a320b-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="a320b-586">Kapsayıcı kimliği geçerliyse, uygulama çalışandan ağırlığı isteyen yeni bir sayfa açar.</span><span class="sxs-lookup"><span data-stu-id="a320b-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="a320b-587">(Kapsayıcı kimliği geçerli değilse, çalışan ilk sayfaya döndürülür.)</span><span class="sxs-lookup"><span data-stu-id="a320b-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="a320b-588">Çalışan geçerli bir ağırlık girdiğinde, sistem ağırlığı depolar ve çalışanı ilk sayfaya döndürür.</span><span class="sxs-lookup"><span data-stu-id="a320b-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="a320b-589">Aşağıdaki şekilde bu görev akışı gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a320b-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="a320b-590">![Görev akışı diyagramı](media/step-icons-example-task-flow.png "Görev akışı diyagramı")</span><span class="sxs-lookup"><span data-stu-id="a320b-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="a320b-591">Kapsayıcı giriş sayfası için adım sınıfı oluşturma</span><span class="sxs-lookup"><span data-stu-id="a320b-591">Create a step class for the container input page</span></span>

<span data-ttu-id="a320b-592">Kapsayıcı giriş sayfası, çalışanın bir kapsayıcı kimliği taramasına veya girmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="a320b-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="a320b-593">![Kapsayıcı giriş sayfası](media/step-icons-example-container-input.png "Kapsayıcı giriş sayfası")</span><span class="sxs-lookup"><span data-stu-id="a320b-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="a320b-594">Kapsayıcı giriş sayfasında, giriş alanının denetim adı `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="a320b-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="a320b-595">Bu denetim adı [adım kimlikleri listesinde](#step-ids-classes) olmadığından, temel alan varolan bir adımı bulamazsınız.</span><span class="sxs-lookup"><span data-stu-id="a320b-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="a320b-596">Bu nedenle, adımı temsil eden bir adım sınıfı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a320b-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="a320b-597">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a320b-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="a320b-598">Adım simgesinin tanımlayıcısı `defaultStepIcon` sınıf üyesinde, adım başlığı ise `defaultStepTitle` sınıf üyesinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="a320b-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="a320b-599">Adım simgesi atamak için, bu konunun önceki bölümlerindeki [Kullanılabilir adım simgeleri](#step-icons) bölümünde listelenen simge kimliklerinden birine `defaultStepIcon` ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a320b-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="a320b-600">Ağırlık girişi için standart veya özel adım simgesi ve başlığı kullanma</span><span class="sxs-lookup"><span data-stu-id="a320b-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="a320b-601">Ağırlık giriş sayfası, çalışanın bir ağırlık girmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="a320b-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="a320b-602">![Ağırlık giriş sayfası](media/step-icons-example-weight-input.png "Ağırlık giriş sayfası")</span><span class="sxs-lookup"><span data-stu-id="a320b-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="a320b-603">Ağırlık giriş sayfasında, giriş alanının denetim adı `Weight`, bu da [adım kimlikleri listesindedir](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="a320b-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="a320b-604">Bu nedenle, `WHSMobileAppStepWeight` sınıfta tanımlanan adım simgesi ve başlığı sizin için kabul edilebilirse, bu adım için hiçbir şeyi değiştirmeniz gerekmemektedir.</span><span class="sxs-lookup"><span data-stu-id="a320b-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="a320b-605">Ancak, bu adım için farklı bir simge veya başlık kullanmayı tercih ederseniz, `stepId()` yöntemi veya `stepInfo()` yöntemi oluşturucu sınıfında geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a320b-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="a320b-606">Her görev akışının kendi adım bilgisi oluşturucusu vardır.</span><span class="sxs-lookup"><span data-stu-id="a320b-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="a320b-607">stepId() yöntemini geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="a320b-607">Override the stepId() method</span></span>

<span data-ttu-id="a320b-608">Aşağıdaki örnek, `stepId()` yöntemi geçersiz kılarak bir oluşturucu sınıfını değiştirmenin bir yolunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a320b-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="a320b-609">Daha sonra `NewWeight` adım için bir adım sınıfı oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="a320b-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="a320b-610">Kod, bu konuda daha önce gösterilen `ContainerId` örneğin koduna benzemelidir.</span><span class="sxs-lookup"><span data-stu-id="a320b-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="a320b-611">stepInfo() yöntemini geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="a320b-611">Override the stepInfo() method</span></span>

<span data-ttu-id="a320b-612">Aşağıdaki örnek, `stepInfo()` yöntemi geçersiz kılarak bir oluşturucu sınıfını değiştirmenin bir yolunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a320b-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="a320b-613">Daha sonra bir `WHSMobileAppStepInfo` nesnesi oluşturursunuz ve simgeyi ve/veya başlığı doğrudan ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="a320b-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a320b-614">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a320b-614">Additional resources</span></span>

- [<span data-ttu-id="a320b-615">Ambar Yönetimi mobil uygulamasını yükleme ve bağlama</span><span class="sxs-lookup"><span data-stu-id="a320b-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="a320b-616">Mobil cihaz kullanıcı ayarları</span><span class="sxs-lookup"><span data-stu-id="a320b-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
