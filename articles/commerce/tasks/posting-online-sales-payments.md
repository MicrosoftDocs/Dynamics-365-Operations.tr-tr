---
title: Çevrimiçi satışlar ve ödemeler deftere naklediliyor
description: Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140796"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="f820c-103">Çevrimiçi satışlar ve ödemeler deftere naklediliyor</span><span class="sxs-lookup"><span data-stu-id="f820c-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f820c-104">Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="f820c-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="f820c-105">Çevrimiçi satış ve Ödemelerin deftere nakledilmesi iki aşamalı bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="f820c-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="f820c-106">HQ içindeki çevrimiçi ticaret hareket verileri çekiliyor.</span><span class="sxs-lookup"><span data-stu-id="f820c-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="f820c-107">HQ'da satış siparişleri oluşturmak için Siparişler eşitleniyor.</span><span class="sxs-lookup"><span data-stu-id="f820c-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="f820c-108">Çevrimiçi hareket verilerini çekme işlemi, P-iş ya el ile çalıştırarak ya da tekrarlayan bir toplu iş oluşturarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="f820c-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="f820c-109">P işi el ile çalıştırılıyor</span><span class="sxs-lookup"><span data-stu-id="f820c-109">Manually running the P-job</span></span>

1. <span data-ttu-id="f820c-110">Tüm iş yerleri > Perakende ve Ticaret BT'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="f820c-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="f820c-111">Dağıtım planı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="f820c-112">P-0001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f820c-112">Select P-0001.</span></span>
4. <span data-ttu-id="f820c-113">Gerekiyorsa kanal veritabanı gruplarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="f820c-114">Şimdi çalıştır üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-114">Click Run now.</span></span>
6. <span data-ttu-id="f820c-115">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f820c-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="f820c-116">Tekrarlayan bir P-iş planlama çizelgeleme</span><span class="sxs-lookup"><span data-stu-id="f820c-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="f820c-117">Tüm iş yerleri > Perakende ve Ticaret BT'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="f820c-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="f820c-118">Dağıtım planı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="f820c-119">P-0001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f820c-119">Select P-0001.</span></span>
4. <span data-ttu-id="f820c-120">Toplu iş oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-120">Click Create batch job.</span></span>
5. <span data-ttu-id="f820c-121">Arka planda çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-121">Click Run in the background.</span></span>
5. <span data-ttu-id="f820c-122">Toplu işlemi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f820c-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="f820c-123">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-123">Click Recurrence..</span></span>
7. <span data-ttu-id="f820c-124">Bitiş tarihi yok seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="f820c-124">Select the No end date option.</span></span>
8. <span data-ttu-id="f820c-125">Sayım alanına, dakika cinsinden çalışma arasındaki aralığı girin.</span><span class="sxs-lookup"><span data-stu-id="f820c-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="f820c-126">Bu genellikle 5-10 olabilir.</span><span class="sxs-lookup"><span data-stu-id="f820c-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="f820c-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-127">Click OK.</span></span>
10. <span data-ttu-id="f820c-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-128">Click OK.</span></span>

<span data-ttu-id="f820c-129">Siparişler, "Siparişleri eşitle" işini manuel olarak çalıştırarak veya yinelenen bir toplu iş oluşturarak eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="f820c-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="f820c-130">El ile çalıştırılan siparişi eşitleme</span><span class="sxs-lookup"><span data-stu-id="f820c-130">Manually running order synchronization</span></span> 

<span data-ttu-id="f820c-131">"Siparişleri Eşitle" işini bir kez el ile çalıştırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f820c-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="f820c-132">Tüm çalışma alanları > Mağaza mali öğeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f820c-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="f820c-133">Siparişleri eşitle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="f820c-134">Kuruluş hiyerarşisi alanında 'Bölgeye göre Mağazalar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f820c-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="f820c-135">Belirli bir çevrimiçi mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="f820c-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="f820c-136">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="f820c-137">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="f820c-138">Toplu işlemini devre dışı bırakın</span><span class="sxs-lookup"><span data-stu-id="f820c-138">Disable Batch processing</span></span>
6. <span data-ttu-id="f820c-139">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-139">Click Recurrence.</span></span>
7. <span data-ttu-id="f820c-140">Bu tarihten sonra biter seçeneğini belirleyin</span><span class="sxs-lookup"><span data-stu-id="f820c-140">Select End After option</span></span>
8. <span data-ttu-id="f820c-141">Bu tarihten sonra biter alanına 1 girin.</span><span class="sxs-lookup"><span data-stu-id="f820c-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="f820c-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-142">Click OK.</span></span>
10. <span data-ttu-id="f820c-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="f820c-144">Tekrarlanan sipariş eşitlemesini planlama</span><span class="sxs-lookup"><span data-stu-id="f820c-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="f820c-145">Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="f820c-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="f820c-146">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f820c-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="f820c-147">Tüm çalışma alanları > Mağaza mali öğeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f820c-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="f820c-148">Siparişleri eşitle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="f820c-149">Kuruluş hiyerarşisi alanında 'Bölgeye göre Mağazalar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f820c-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="f820c-150">Belirli bir çevrimiçi mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="f820c-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="f820c-151">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="f820c-152">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="f820c-153">Toplu işlemi etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="f820c-153">Enable Batch processing</span></span>
6. <span data-ttu-id="f820c-154">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-154">Click Recurrence.</span></span>
7. <span data-ttu-id="f820c-155">Bitiş tarihi yok seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="f820c-155">Select the No end date option.</span></span>
8. <span data-ttu-id="f820c-156">Sayım alanına, dakika cinsinden çalışma arasındaki aralığı girin.</span><span class="sxs-lookup"><span data-stu-id="f820c-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="f820c-157">Bu genellikle 2-20 olabilir</span><span class="sxs-lookup"><span data-stu-id="f820c-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="f820c-158">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-158">Click OK.</span></span>
10. <span data-ttu-id="f820c-159">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f820c-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="f820c-160">İşlemde yer alan veri varlıkları</span><span class="sxs-lookup"><span data-stu-id="f820c-160">Data entities involved in the process</span></span>

- <span data-ttu-id="f820c-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="f820c-161">RetailTransactionTable</span></span>
- <span data-ttu-id="f820c-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="f820c-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="f820c-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="f820c-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="f820c-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="f820c-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="f820c-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="f820c-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="f820c-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="f820c-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="f820c-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="f820c-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="f820c-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="f820c-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="f820c-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="f820c-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="f820c-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="f820c-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="f820c-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="f820c-171">RetailTransactionAttributeTrans</span></span>
