---
title: Temel tahmin oluşturma
description: Üretim planlayıcısı, zaman serisi tahmin modellerini kullanarak veya geçmiş talebi kopyalayarak bir taban tahmini oluşturabilir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d23e245ed1c084c26554ef3f859fdadaef9990d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553011"
---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="56d20-103">Temel tahmin oluşturma</span><span class="sxs-lookup"><span data-stu-id="56d20-103">Create a baseline forecast</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56d20-104">Üretim planlayıcısı, zaman serisi tahmin modellerini kullanarak veya geçmiş talebi kopyalayarak bir taban tahmini oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="56d20-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="56d20-105">Bu yordam, tüm ürünler için, bir madde tahsisatı anahtarı kullanarak bir temel tahmini oluşturup geçmiş talebi kopyalamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="56d20-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="56d20-106">Madde tahsisat anahtarı ayarlama</span><span class="sxs-lookup"><span data-stu-id="56d20-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="56d20-107">Master planlama > Kurulum > Şirketlerarası planlama grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="56d20-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="56d20-108">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="56d20-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="56d20-109">Örneğin, İsim alanı üzerinde '10' değerini girerek filtreleme yapın.</span><span class="sxs-lookup"><span data-stu-id="56d20-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="56d20-110">Talep tahmini tüzel kişilikler arasında çalışır.</span><span class="sxs-lookup"><span data-stu-id="56d20-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="56d20-111">Bu nedenle tahminler oluşturmak istediğiniz tüm şirketleri bir şirketlerarası planlama grubuna dahil etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="56d20-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="56d20-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="56d20-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="56d20-113">Madde tahsisat anahtarlarına tıkla.</span><span class="sxs-lookup"><span data-stu-id="56d20-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="56d20-114">Tahminleri oluşturmak istediğiniz tüm madde tahsisat anahtarlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="56d20-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="56d20-115">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="56d20-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="56d20-116">D_Aloc madde tahsisat anahtarını seçin.</span><span class="sxs-lookup"><span data-stu-id="56d20-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="56d20-117">> öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56d20-117">Click >.</span></span>
7. <span data-ttu-id="56d20-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="56d20-118">Close the page.</span></span>
8. <span data-ttu-id="56d20-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="56d20-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-paramters"></a><span data-ttu-id="56d20-120">Talep tahmini için parametreleri ayarlayın</span><span class="sxs-lookup"><span data-stu-id="56d20-120">Set up the demand forecasting paramters</span></span>
1. <span data-ttu-id="56d20-121">Master planlama > Kurulum > Talep tahmini > Talep tahmini parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="56d20-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="56d20-122">Tahmin algoritma parametreleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="56d20-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="56d20-123">Tahmin oluşturma strateji alanında 'Geçmiş talep üzerine kopyala' seçin.</span><span class="sxs-lookup"><span data-stu-id="56d20-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="56d20-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56d20-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="56d20-125">Temel tahmin oluşturma</span><span class="sxs-lookup"><span data-stu-id="56d20-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="56d20-126">Master planlama > Tahmin > Talep tahmini > İstatistik temel tahmini oluştur seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="56d20-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="56d20-127">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="56d20-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="56d20-128">1 Ocak 2015'den sonra satış emirleriniz varsa, bu tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="56d20-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="56d20-129">Bunu yapmazsanız, satış siparişlerinizin en erken tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="56d20-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="56d20-130">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="56d20-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="56d20-131">Satış emirlerinin son tarihini (örneğin '2015-03-31') girin.</span><span class="sxs-lookup"><span data-stu-id="56d20-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="56d20-132">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="56d20-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="56d20-133">'2015-04-01' girin.</span><span class="sxs-lookup"><span data-stu-id="56d20-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="56d20-134">Bu tarih bir sonraki tahmin kovasının başlangıç tarihi olarak otomatik hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="56d20-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="56d20-135">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="56d20-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="56d20-136">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56d20-136">Click Filter.</span></span>
7. <span data-ttu-id="56d20-137">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="56d20-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="56d20-138">Alan = Şirketlerarası planlama grubu olan satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="56d20-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="56d20-139">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="56d20-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="56d20-140">Şirketlerarası planlama grubu, örneğin, ilk görevinde kullandığınız, 10'u yazın.</span><span class="sxs-lookup"><span data-stu-id="56d20-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="56d20-141">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="56d20-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="56d20-142">Alan = Madde tahsisatı anahtarı olanı seçin.</span><span class="sxs-lookup"><span data-stu-id="56d20-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="56d20-143">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="56d20-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="56d20-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56d20-144">Click OK.</span></span>
12. <span data-ttu-id="56d20-145">Gelişmiş parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="56d20-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="56d20-146">Tahmin aralığı alanında, 'Ay' seçin.</span><span class="sxs-lookup"><span data-stu-id="56d20-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="56d20-147">Tahmin dönemi alanında, '3' girin.</span><span class="sxs-lookup"><span data-stu-id="56d20-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="56d20-148">Dondurulmuş zaman dilimi alanında '1' girin.</span><span class="sxs-lookup"><span data-stu-id="56d20-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="56d20-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56d20-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="56d20-150">Talep tahminini görselleştirin</span><span class="sxs-lookup"><span data-stu-id="56d20-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="56d20-151">Master planlama > Tahmin > Talep tahmini > Düzeltilmiş talep tahmini seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="56d20-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="56d20-152">Toplanmış görünüm tablosunda, sıra 1 sütun 2 konumundaki hücreyi seçin.</span><span class="sxs-lookup"><span data-stu-id="56d20-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="56d20-153">Bu tahmin oluşturduğunuz ikinci aydır.</span><span class="sxs-lookup"><span data-stu-id="56d20-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="56d20-154">QtyCell 'i 400'e ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="56d20-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="56d20-155">Hücrede, ilk olarak tahminde bulunduğunuzdan farklı bir sayı girin, örneğin 400.</span><span class="sxs-lookup"><span data-stu-id="56d20-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="56d20-156">Tahminde el ile bir düzeltme uyguladınız.</span><span class="sxs-lookup"><span data-stu-id="56d20-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="56d20-157">Sonraki adımdaki grafik göstergeye dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="56d20-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="56d20-158">Tahmin satırı ayrıntıları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56d20-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="56d20-159">Bu sayfada, doğruluk değerleri, geçmiş talep, ve tahminleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="56d20-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="56d20-160">Bu tahminde değişiklikler de yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="56d20-160">You can make changes to the forecast as well.</span></span>  

