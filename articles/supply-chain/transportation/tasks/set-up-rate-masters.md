---
title: Ana oranları ayarlama
description: Bu yordam, bir ana oran kurmayı göstermektedir.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77629cbaec4c4d4608b8941e55ab23a106d38727
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233619"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="9edcc-103">Ana oranları ayarlama</span><span class="sxs-lookup"><span data-stu-id="9edcc-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9edcc-104">Bu yordam, bir ana oran kurmayı göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="9edcc-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="9edcc-105">Genellikle Lojistik Yöneticisi, taşıyıcılar ile imzalanmış olan sözleşmelere bağlı olarak ana oranları ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9edcc-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="9edcc-106">Bu senaryoda bir hava taşıyıcısı için ana oran ayarlayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="9edcc-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="9edcc-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="9edcc-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="9edcc-108">Ana kırılımı ayarlama</span><span class="sxs-lookup"><span data-stu-id="9edcc-108">Set up break master</span></span>

1. <span data-ttu-id="9edcc-109">**Taşıma yönetimi > Kurulum > Derecelendirme > Ana kırılım** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="9edcc-110">Kesme kalıpları, fiyatlandırma yapısını ve onun kırılma noktalarını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9edcc-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="9edcc-111">Fiyatlandırma yapısı, fiziksel boyutlara dayanan katmanlı fiyatlandırmalar kullanır.</span><span class="sxs-lookup"><span data-stu-id="9edcc-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="9edcc-112">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-112">Select **New**.</span></span>
1. <span data-ttu-id="9edcc-113">**Ana kırılım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="9edcc-114">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="9edcc-115">**Veri türü** alanında bir veri türü seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="9edcc-116">**Karşılaştırma** alanına, istenen karşılaştırma türünü (işleçler kullanarak) girin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="9edcc-117">**Kırılım birimi** alanında, kırılım birimini girin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="9edcc-118">**Ayrıntılar** bölümünde, fiyatlandırma yapısı için gerektiği kadar kırılım oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9edcc-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="9edcc-119">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="9edcc-120">Ana oranı ayarlayın</span><span class="sxs-lookup"><span data-stu-id="9edcc-120">Set up rate master</span></span>

1. <span data-ttu-id="9edcc-121">**Taşıma yönetimi > Kurulum > Derecelendirme > Ana oran** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="9edcc-122">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-122">Select **New**.</span></span>
1. <span data-ttu-id="9edcc-123">**Ana oran** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="9edcc-124">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="9edcc-125">**Değerlendirme meta veri kimliği** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="9edcc-126">Bu oran asıl kullanarak taşıma yönetimi altyapısı tarafından beklenen meta verileri tanımlar gibi kuru master için gerekli veri derecelendirme meta veriler kimliği belirleyecektir.</span><span class="sxs-lookup"><span data-stu-id="9edcc-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="9edcc-127">Bu örnekte, P2P seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-127">For this example, select the P2P option.</span></span> <span data-ttu-id="9edcc-128">Bu, demo verilerinde zaten tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="9edcc-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="9edcc-129">Listeden, seçilen satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="9edcc-130">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="9edcc-131">Oran tabanını ayarla</span><span class="sxs-lookup"><span data-stu-id="9edcc-131">Set up rate base</span></span>

1. <span data-ttu-id="9edcc-132">**Oran tabanı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="9edcc-133">Taban oranı, taşıyıcının oranını belirler ve gümrük tarifesi yapısı oluşturmada, kesme kalıplarında belirtilen kesme noktalarındaki oranları yapılandırdığı için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9edcc-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="9edcc-134">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-134">Select **New**.</span></span>
3. <span data-ttu-id="9edcc-135">**Oran tabanı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="9edcc-136">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9edcc-137">**Ana kırılım** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9edcc-138">Kesme kalıpları, fiyatlandırma yapısını ve onun kırılma noktalarını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9edcc-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="9edcc-139">Fiyatlandırma yapısı, fiziksel boyutlara dayanan katmanlı fiyatlandırmalar kullanır.</span><span class="sxs-lookup"><span data-stu-id="9edcc-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="9edcc-140">Bu örnek için ağırlık değerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-140">For this example, use weight.</span></span> <span data-ttu-id="9edcc-141">Bu, demo verilerinde zaten tanımlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="9edcc-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="9edcc-142">Listeden, vurgulanan satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="9edcc-143">**Ayrıntılar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="9edcc-144">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-144">Select **New**.</span></span>
10. <span data-ttu-id="9edcc-145">**Teslimat Posta Kodu Kaynağı** alanına, "30301" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="9edcc-146">**Teslimat Posta Kodu Hedefi** alanına, "30318" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="9edcc-147">**Teslimat ülkesi bölgesi** alanına "ABD" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="9edcc-148">**<1,00 Lbs** alanına "100" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="9edcc-149">Yükün toplam ağırlığı 1 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="9edcc-150">**<5,00 Lbs** alanına "300" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="9edcc-151">Yükün toplam ağırlığı 5 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="9edcc-152">**<20,00 Lbs** alanına "500" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="9edcc-153">Yükün toplam ağırlığı 20 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="9edcc-154">**<100,00 Lbs** alanına "1000" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="9edcc-155">Yükün toplam ağırlığı 100 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="9edcc-156">**<1.000,00 Lbs** alanına "3000" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="9edcc-157">Yükün toplam ağırlığı 1000 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="9edcc-158">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-158">Select **Save**.</span></span>
19. <span data-ttu-id="9edcc-159">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="9edcc-160">Oran tabanı atama</span><span class="sxs-lookup"><span data-stu-id="9edcc-160">Assign rate base</span></span>

1. <span data-ttu-id="9edcc-161">**Oran tabanı atamaları** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="9edcc-162">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-162">Select **New**.</span></span>
    * <span data-ttu-id="9edcc-163">Her ana oran için birden fazla oran tabanı atamanız olabilir.</span><span class="sxs-lookup"><span data-stu-id="9edcc-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="9edcc-164">Bu hedeflere, hizmetlere veya farklı taba oranlarına bağlı olarak her taşıyıcı için birkaç farklı fiyat noktaları oluşturmaya olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="9edcc-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="9edcc-165">Bu yordamda sadece bir oranı tabanı ataması oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="9edcc-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="9edcc-166">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="9edcc-167">**Oran tabanı** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9edcc-168">Listeden, vurgulanan satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="9edcc-169">**Servis** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9edcc-170">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9edcc-171">Listeden, vurgulanan satırdaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="9edcc-172">**Çekme Posta Kodu** alanına "98052" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="9edcc-173">Bu oran tabanı atamasının hangi posta kodundan itibaren geçerli olacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="9edcc-174">**Çekme Ülke Bölgesi** alanında "ABD" yazın.</span><span class="sxs-lookup"><span data-stu-id="9edcc-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="9edcc-175">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9edcc-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]