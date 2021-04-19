---
title: Çevrimiçi satışlar ve ödemeler deftere naklediliyor
description: Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.
author: psimolin
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2e482b0fb5f2cf67e687c2b278bc5b54ad09839
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802683"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="8d312-103">Çevrimiçi satışlar ve ödemeler deftere naklediliyor</span><span class="sxs-lookup"><span data-stu-id="8d312-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d312-104">Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="8d312-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="8d312-105">Çevrimiçi satış ve Ödemelerin deftere nakledilmesi iki aşamalı bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="8d312-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="8d312-106">HQ içindeki çevrimiçi ticaret hareket verileri çekiliyor.</span><span class="sxs-lookup"><span data-stu-id="8d312-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="8d312-107">HQ'da satış siparişleri oluşturmak için Siparişler eşitleniyor.</span><span class="sxs-lookup"><span data-stu-id="8d312-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="8d312-108">Çevrimiçi hareket verilerini çekme işlemi, P-iş ya el ile çalıştırarak ya da tekrarlayan bir toplu iş oluşturarak yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="8d312-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="8d312-109">P işi el ile çalıştırılıyor</span><span class="sxs-lookup"><span data-stu-id="8d312-109">Manually running the P-job</span></span>

1. <span data-ttu-id="8d312-110">Tüm iş yerleri > Perakende ve Ticaret BT'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="8d312-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="8d312-111">Dağıtım planı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="8d312-112">P-0001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8d312-112">Select P-0001.</span></span>
4. <span data-ttu-id="8d312-113">Gerekiyorsa kanal veritabanı gruplarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="8d312-114">Şimdi çalıştır üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-114">Click Run now.</span></span>
6. <span data-ttu-id="8d312-115">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8d312-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="8d312-116">Tekrarlayan bir P-iş planlama çizelgeleme</span><span class="sxs-lookup"><span data-stu-id="8d312-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="8d312-117">Tüm iş yerleri > Perakende ve Ticaret BT'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="8d312-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="8d312-118">Dağıtım planı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="8d312-119">P-0001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8d312-119">Select P-0001.</span></span>
4. <span data-ttu-id="8d312-120">Toplu iş oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-120">Click Create batch job.</span></span>
5. <span data-ttu-id="8d312-121">Arka planda çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-121">Click Run in the background.</span></span>
5. <span data-ttu-id="8d312-122">Toplu işlemi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="8d312-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="8d312-123">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-123">Click Recurrence..</span></span>
7. <span data-ttu-id="8d312-124">Bitiş tarihi yok seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="8d312-124">Select the No end date option.</span></span>
8. <span data-ttu-id="8d312-125">Sayım alanına, dakika cinsinden çalışma arasındaki aralığı girin.</span><span class="sxs-lookup"><span data-stu-id="8d312-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="8d312-126">Bu genellikle 5-10 olabilir.</span><span class="sxs-lookup"><span data-stu-id="8d312-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="8d312-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-127">Click OK.</span></span>
10. <span data-ttu-id="8d312-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-128">Click OK.</span></span>

<span data-ttu-id="8d312-129">Siparişler, "Siparişleri eşitle" işini manuel olarak çalıştırarak veya yinelenen bir toplu iş oluşturarak eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="8d312-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="8d312-130">El ile çalıştırılan siparişi eşitleme</span><span class="sxs-lookup"><span data-stu-id="8d312-130">Manually running order synchronization</span></span> 

<span data-ttu-id="8d312-131">"Siparişleri Eşitle" işini bir kez el ile çalıştırmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8d312-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="8d312-132">Tüm çalışma alanları > Mağaza mali öğeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8d312-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="8d312-133">Siparişleri eşitle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="8d312-134">Kuruluş hiyerarşisi alanında 'Bölgeye göre Mağazalar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8d312-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="8d312-135">Belirli bir çevrimiçi mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="8d312-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="8d312-136">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="8d312-137">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="8d312-138">Toplu işlemini devre dışı bırakın</span><span class="sxs-lookup"><span data-stu-id="8d312-138">Disable Batch processing</span></span>
6. <span data-ttu-id="8d312-139">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-139">Click Recurrence.</span></span>
7. <span data-ttu-id="8d312-140">Bu tarihten sonra biter seçeneğini belirleyin</span><span class="sxs-lookup"><span data-stu-id="8d312-140">Select End After option</span></span>
8. <span data-ttu-id="8d312-141">Bu tarihten sonra biter alanına 1 girin.</span><span class="sxs-lookup"><span data-stu-id="8d312-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="8d312-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-142">Click OK.</span></span>
10. <span data-ttu-id="8d312-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="8d312-144">Tekrarlanan sipariş eşitlemesini planlama</span><span class="sxs-lookup"><span data-stu-id="8d312-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="8d312-145">Bu yordam, çevrimiçi mağaza hareketleri için satış siparişleri ve ödemeler oluşturmak üzere yinelenen bir toplu işi yapılandırma ve çalıştırmayla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="8d312-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="8d312-146">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8d312-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="8d312-147">Tüm çalışma alanları > Mağaza mali öğeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8d312-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="8d312-148">Siparişleri eşitle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="8d312-149">Kuruluş hiyerarşisi alanında 'Bölgeye göre Mağazalar'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8d312-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="8d312-150">Belirli bir çevrimiçi mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="8d312-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="8d312-151">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="8d312-152">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="8d312-153">Toplu işlemi etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="8d312-153">Enable Batch processing</span></span>
6. <span data-ttu-id="8d312-154">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-154">Click Recurrence.</span></span>
7. <span data-ttu-id="8d312-155">Bitiş tarihi yok seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="8d312-155">Select the No end date option.</span></span>
8. <span data-ttu-id="8d312-156">Sayım alanına, dakika cinsinden çalışma arasındaki aralığı girin.</span><span class="sxs-lookup"><span data-stu-id="8d312-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="8d312-157">Bu genellikle 2-20 olabilir</span><span class="sxs-lookup"><span data-stu-id="8d312-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="8d312-158">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-158">Click OK.</span></span>
10. <span data-ttu-id="8d312-159">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8d312-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="8d312-160">İşlemde yer alan veri varlıkları</span><span class="sxs-lookup"><span data-stu-id="8d312-160">Data entities involved in the process</span></span>

- <span data-ttu-id="8d312-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="8d312-161">RetailTransactionTable</span></span>
- <span data-ttu-id="8d312-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="8d312-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="8d312-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="8d312-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="8d312-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="8d312-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="8d312-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="8d312-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="8d312-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="8d312-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="8d312-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="8d312-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="8d312-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="8d312-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="8d312-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="8d312-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="8d312-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="8d312-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="8d312-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="8d312-171">RetailTransactionAttributeTrans</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]