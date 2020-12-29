---
title: Çevrimiçi kanal raporları oluşturma
description: Bu konu, Microsoft Dynamics 365 Commerce uygulamasında çevrimiçi kanallarınız için nasıl rapor oluşturulacağını açıklamaktadır.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ae7b73c7a51ffa606876072d607fc219f5f6a2ba
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416451"
---
# <a name="generate-online-channel-reports"></a><span data-ttu-id="ac07a-103">Çevrimiçi kanal raporları oluşturma</span><span class="sxs-lookup"><span data-stu-id="ac07a-103">Generate online channel reports</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ac07a-104">Bu konu, Microsoft Dynamics 365 Commerce uygulamasında çevrimiçi kanallarınız için nasıl rapor oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="ac07a-104">This topic describes how to generate reports for your online channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ac07a-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="ac07a-105">Overview</span></span>

<span data-ttu-id="ac07a-106">Çevrimiçi kanalınızın nasıl çalıştığını görmek için Commerce'te birden fazla rapor oluşturabilir ve görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac07a-106">You can generate and view several reports in Commerce to see how your online channel is performing.</span></span>

## <a name="channel-summary-report"></a><span data-ttu-id="ac07a-107">Kanal özeti raporu</span><span class="sxs-lookup"><span data-stu-id="ac07a-107">Channel summary report</span></span>

<span data-ttu-id="ac07a-108">**Kanal özeti** raporu, seçili kanalın aşağıdaki hareketlerinin özetini gösterir:</span><span class="sxs-lookup"><span data-stu-id="ac07a-108">The **Channel summary** report shows a summary of the following transactions for the selected channel:</span></span>

- <span data-ttu-id="ac07a-109">Satış hareketleri</span><span class="sxs-lookup"><span data-stu-id="ac07a-109">Sales transactions</span></span>
- <span data-ttu-id="ac07a-110">Ödeme hareketleri</span><span class="sxs-lookup"><span data-stu-id="ac07a-110">Payment transactions</span></span>
- <span data-ttu-id="ac07a-111">Vergi hareketleri</span><span class="sxs-lookup"><span data-stu-id="ac07a-111">Tax transactions</span></span>
- <span data-ttu-id="ac07a-112">İskonto hareketleri</span><span class="sxs-lookup"><span data-stu-id="ac07a-112">Discounted transactions</span></span>

<span data-ttu-id="ac07a-113">Bir **kanal Özet** raporu oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-113">To generate a **Channel summary** report, follow these steps.</span></span>

1. <span data-ttu-id="ac07a-114">**Retail and Commerce \> Sorgular ve raporlar \> Satış raporları \> Kanalı Özet raporu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-114">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel summary report**.</span></span>
1. <span data-ttu-id="ac07a-115">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-115">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-116">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-116">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-117">**Kanal** alanında, çevrimiçi kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-117">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ac07a-118">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-118">Select **OK**.</span></span>
 
## <a name="channel-sales-by-year-report"></a><span data-ttu-id="ac07a-119">Yıla göre kanal satışları raporu</span><span class="sxs-lookup"><span data-stu-id="ac07a-119">Channel sales by year report</span></span> 

<span data-ttu-id="ac07a-120">**Yıla göre kanal satışları** raporu, belirli bir mağaza için yıllık satışların bir karşılaştırmasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac07a-120">The **Channel sales by year** report shows a comparison of year-over-year sales for a specific store.</span></span> <span data-ttu-id="ac07a-121">Satışların karşılaştırılacağı yılı seçersiniz ve rapor, seçilen yıla ait satışları önceki yıla ait satışlarla karşılaştırır.</span><span class="sxs-lookup"><span data-stu-id="ac07a-121">You select the year to compare the sales against, and the report compares sales for the selected year with sales for the previous year.</span></span>

<span data-ttu-id="ac07a-122">Bir **Yıla göre kanal satışları** raporu oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-122">To generate a **Channel sales by year** report, follow these steps.</span></span>

1. <span data-ttu-id="ac07a-123">**Retail and Commerce \> Sorgular ve raporlar \> Satış raporları \> Yıla göre kanal satışları raporu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-123">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by year report**.</span></span>
1. <span data-ttu-id="ac07a-124">**Takvim yılından** alanına yıl girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-124">In the **From calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="ac07a-125">**Takvim yılına** alanına yıl girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-125">In the **To calendar year** field, enter a year.</span></span>
1. <span data-ttu-id="ac07a-126">**Kanal** alanında, çevrimiçi kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-126">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ac07a-127">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-127">Select **OK**.</span></span>

## <a name="channel-sales-by-hour-report"></a><span data-ttu-id="ac07a-128">Saate göre kanal satışları raporu</span><span class="sxs-lookup"><span data-stu-id="ac07a-128">Channel sales by hour report</span></span>

<span data-ttu-id="ac07a-129">**Saate göre kanal satışları** raporu, seçilen bir kanal veya çalışma birimi için saat başına satış ölçümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac07a-129">The **Channel sales by hour** report shows sales metrics per hour for a selected channel or operating unit.</span></span>

<span data-ttu-id="ac07a-130">Bir **Saate göre kanal satışları** raporu oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-130">To generate a **Channel sales by hour** report, follow these steps.</span></span>

1. <span data-ttu-id="ac07a-131">**Retail and Commerce \> Sorgular ve raporlar \> Satış raporları \> Saate göre kanal satışları raporu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-131">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Channel sales by hour report**.</span></span>
1. <span data-ttu-id="ac07a-132">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-132">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-133">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-133">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-134">**Kanal** alanında, çevrimiçi kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-134">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ac07a-135">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-135">Select **OK**.</span></span>

## <a name="top-customers-report"></a><span data-ttu-id="ac07a-136">En önemli müşteriler raporu</span><span class="sxs-lookup"><span data-stu-id="ac07a-136">Top customers report</span></span>

<span data-ttu-id="ac07a-137">**İlk müşteriler** raporu, seçili bir kanal veya çalışma birimi için en iyi *N* müşteri için satış ölçümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac07a-137">The **Top customers** report shows sales metrics for the top *N* customers for a selected channel or operating unit.</span></span> <span data-ttu-id="ac07a-138">*N* değeri , 10-100 arasında bir sayıdır ve Kullanıcı tarafından seçilen bir toplu ölçüyü temel alarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="ac07a-138">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="ac07a-139">Bir **En iyi müşteriler** raporu oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-139">To generate a **Top customers** report, follow these steps.</span></span>

1. <span data-ttu-id="ac07a-140">**Retail and Commerce \> Sorgular ve raporlar \> Satış raporları \> En önemli müşteriler raporu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-140">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top customers report**.</span></span>
1. <span data-ttu-id="ac07a-141">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-141">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-142">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-142">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-143">**Kanal** alanında, çevrimiçi kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-143">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ac07a-144">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-144">Select **OK**.</span></span>

## <a name="top-discounts-report"></a><span data-ttu-id="ac07a-145">En yüksek iskontolar raporu</span><span class="sxs-lookup"><span data-stu-id="ac07a-145">Top discounts report</span></span>

<span data-ttu-id="ac07a-146">**İlk indirimler** raporu, seçili bir kanal veya çalışma birimi için en iyi *N* indirimler için satış ölçümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac07a-146">The **Top discounts** report shows sales metrics for the top *N* discounts for a selected channel or operating unit.</span></span> <span data-ttu-id="ac07a-147">*N* değeri , 10-100 arasında bir sayıdır ve Kullanıcı tarafından seçilen bir toplu ölçüyü temel alarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="ac07a-147">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="ac07a-148">Bir **En iyi indirimler** raporu oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-148">To generate a **Top discounts** report, follow these steps.</span></span>

1. <span data-ttu-id="ac07a-149">**Retail and Commerce \> Sorgular ve raporlar \> Satış raporları \> En yüksek iskontolar raporu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-149">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top discounts report**.</span></span>
1. <span data-ttu-id="ac07a-150">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-150">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-151">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-151">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-152">**Kanal** alanında, çevrimiçi kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-152">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ac07a-153">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-153">Select **OK**.</span></span>

## <a name="top-products-report"></a><span data-ttu-id="ac07a-154">En çok satılan ürünler raporu</span><span class="sxs-lookup"><span data-stu-id="ac07a-154">Top products report</span></span>

<span data-ttu-id="ac07a-155">**İlk ürünler** raporu, seçili bir kanal veya çalışma birimi için en iyi *N* ürünler için satış ölçümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac07a-155">The **Top products** report shows sales metrics for the top *N* products for a selected channel or operating unit.</span></span> <span data-ttu-id="ac07a-156">*N* değeri , 10-100 arasında bir sayıdır ve Kullanıcı tarafından seçilen bir toplu ölçüyü temel alarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="ac07a-156">The value *N* is a number from 10 to 100 and is based on a user-selected aggregate measure.</span></span>

<span data-ttu-id="ac07a-157">Bir **En iyi ürünler** raporu oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-157">To generate a **Top products** report, follow these steps.</span></span>

1. <span data-ttu-id="ac07a-158">**Retail and Commerce \> Sorgular ve raporlar \> Satış raporları \> En çok satılan ürünler raporu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-158">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Top products report**.</span></span>
1. <span data-ttu-id="ac07a-159">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-159">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-160">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-160">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-161">**Kanal** alanında, çevrimiçi kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-161">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ac07a-162">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-162">Select **OK**.</span></span>

## <a name="category-sales-report"></a><span data-ttu-id="ac07a-163">Kategori satışı raporu</span><span class="sxs-lookup"><span data-stu-id="ac07a-163">Category sales report</span></span>

<span data-ttu-id="ac07a-164">**Kategori satış** raporu, seçili bir kanal veya çalışma birimi için bir kategori hiyerarşisinin her bir düğümü için seçili bir dönemdeki satış ölçümlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac07a-164">The **Category sales** report shows sales metrics over a selected period for each node of a category hierarchy for a selected channel or operating unit.</span></span>

<span data-ttu-id="ac07a-165">Bir **Kategori satışları** raporu oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-165">To generate a **Category sales** report, follow these steps.</span></span>

1. <span data-ttu-id="ac07a-166">**Retail and Commerce \> Sorgular ve raporlar \> Satış raporları \> Kategori satış raporu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-166">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Category sales report**.</span></span>
1. <span data-ttu-id="ac07a-167">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-167">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-168">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-168">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-169">**Kanal** alanında, çevrimiçi kanalı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-169">In the **Channel** field, select the online channel.</span></span>
1. <span data-ttu-id="ac07a-170">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-170">Select **OK**.</span></span>

## <a name="organization-sales-report"></a><span data-ttu-id="ac07a-171">Kuruluş satış raporu</span><span class="sxs-lookup"><span data-stu-id="ac07a-171">Organization sales report</span></span>

<span data-ttu-id="ac07a-172">**Kuruluş satış raporu**, mağazalarınızın organizasyon birimine göre performansını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac07a-172">The **Organization sales** report shows the performance of your stores by organization unit.</span></span> <span data-ttu-id="ac07a-173">Bu rapor, her mağaza için satış miktarını ve mağaza tutarını ve kar marjını içerir.</span><span class="sxs-lookup"><span data-stu-id="ac07a-173">This report includes the sales quantity and amount by store, and the profit margin for each store.</span></span> <span data-ttu-id="ac07a-174">Organizasyon birimi, varsayılan raporlama hiyerarşisine dayanır.</span><span class="sxs-lookup"><span data-stu-id="ac07a-174">The organization unit is based on the default reporting hierarchy.</span></span>

<span data-ttu-id="ac07a-175">Bir **Organizasyon satışları** raporu oluşturmak için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-175">To generate an **Organization sales** report, follow these steps.</span></span>

1. <span data-ttu-id="ac07a-176">**Retail and Commerce \> Sorgular ve raporlar \> Satış raporları \> Kuruluş satış raporu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-176">Go to **Retail and Commerce \> Inquiries and reports \> Sales reports \> Organization sales report**.</span></span>
1. <span data-ttu-id="ac07a-177">**Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-177">In the **From date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-178">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-178">In the **To date** field, enter a date.</span></span>
1. <span data-ttu-id="ac07a-179">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac07a-179">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac07a-180">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ac07a-180">Additional resources</span></span>

- [<span data-ttu-id="ac07a-181">Commerce giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="ac07a-181">Commerce home page</span></span>](../retail/index.md)
