--- 
title: "Ana oranları ayarlama"
description: "Bu yordam, bir ana oran kurmayı göstermektedir."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2e44c4b4d96d9e3d7048a42a147713b682533b4f
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-rate-masters"></a><span data-ttu-id="61525-103">Ana oranları ayarlama</span><span class="sxs-lookup"><span data-stu-id="61525-103">Set up rate masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="61525-104">Bu yordam, bir ana oran kurmayı göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="61525-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="61525-105">Genellikle Lojistik Yöneticisi, taşıyıcılar ile imzalanmış olan sözleşmelere bağlı olarak ana oranları ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61525-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="61525-106">Bu senaryoda bir hava taşıyıcısı için ana oran ayarlayacaksınız.</span><span class="sxs-lookup"><span data-stu-id="61525-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="61525-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="61525-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="61525-108">Ana oranı ayarlayın</span><span class="sxs-lookup"><span data-stu-id="61525-108">Set up rate master</span></span>
1. <span data-ttu-id="61525-109">Taşıma yönetimi > Kurulum > Derecelendirme > Ana oran öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="61525-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="61525-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-110">Click New.</span></span>
3. <span data-ttu-id="61525-111">Ana oran alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="61525-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="61525-113">Oran meta veri kimliği alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="61525-114">Bu oran asıl kullanarak TMS altyapısı tarafından beklenen meta verileri tanımlar gibi kuru master için gerekli veri derecelendirme meta veriler kimliği belirleyecektir.</span><span class="sxs-lookup"><span data-stu-id="61525-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="61525-115">Bu örnekte, P2P seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="61525-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="61525-116">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="61525-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="61525-118">Oran tabanını ayarla</span><span class="sxs-lookup"><span data-stu-id="61525-118">Set up rate base</span></span>
1. <span data-ttu-id="61525-119">Taban türü oranı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-119">Click Rate base.</span></span>
    * <span data-ttu-id="61525-120">Taban oranı, taşıyıcının oranını belirler ve gümrük tarifesi yapısı oluşturmada, kesme kalıplarında belirtilen kesme noktalarındaki oranları yapılandırdığı için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="61525-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="61525-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-121">Click New.</span></span>
3. <span data-ttu-id="61525-122">Taban türü oranı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="61525-123">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="61525-124">Ana mola alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="61525-125">Kesme kalıpları, fiyatlandırma yapısını ve onun kırılma noktalarını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="61525-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="61525-126">Fiyatlandırma yapısı, fiziksel boyutlara dayanan katmanlı fiyatlandırmalar kullanır.</span><span class="sxs-lookup"><span data-stu-id="61525-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="61525-127">Bu örnek için ağırlık kullanın.</span><span class="sxs-lookup"><span data-stu-id="61525-127">For this example, use weight</span></span>
7. <span data-ttu-id="61525-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="61525-129">Ayrıntılar bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="61525-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="61525-130">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="61525-130">Click New.</span></span>
10. <span data-ttu-id="61525-131">Teslim posta kodu kaynağı alanında, '30301' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="61525-132">Giden posta kodu bırakma alanında, '30318' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="61525-133">Teslimat ülkesi bölgesi alanına 'ABD' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="61525-134"><1,00 Lbs alanında '100' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="61525-135">Yükün toplam ağırlığı 1 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="61525-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="61525-136">< 5,00 Lbs alanında, '300' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="61525-137">Yükün toplam ağırlığı 5 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="61525-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="61525-138">< 20,00 Lbs alanında, '500' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="61525-139">Yükün toplam ağırlığı 20 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="61525-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="61525-140">< 100,00 Lbs alanında, '1000' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="61525-141">Yükün toplam ağırlığı 100 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="61525-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="61525-142">< 1.000,00 Lbs alanında, '3000' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="61525-143">Yükün toplam ağırlığı 1000 libreden az ise lbs başına ücret girin.</span><span class="sxs-lookup"><span data-stu-id="61525-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="61525-144">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-144">Click Save.</span></span>
19. <span data-ttu-id="61525-145">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="61525-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="61525-146">Oran tabanı atama</span><span class="sxs-lookup"><span data-stu-id="61525-146">Assign rate base</span></span>
1. <span data-ttu-id="61525-147">Taban oranı atamaları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="61525-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="61525-148">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-148">Click New.</span></span>
    * <span data-ttu-id="61525-149">Her ana oran için birden fazla oran tabanı atamanız olabilir.</span><span class="sxs-lookup"><span data-stu-id="61525-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="61525-150">Bu hedeflere, hizmetlere veya farklı taba oranlarına bağlı olarak her taşıyıcı için birkaç farklı fiyat noktaları oluşturmaya olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="61525-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="61525-151">Bu yordamda sadece bir oranı tabanı ataması oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="61525-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="61525-152">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="61525-153">Taban oranı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="61525-154">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="61525-155">Hizmet alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="61525-156">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="61525-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="61525-157">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="61525-158">Çekme posta kodu alanına '98052' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="61525-159">Bu oran tabanı atamasının hangi posta kodundan itibaren geçerli olacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="61525-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="61525-160">Çekme Ülke Bölge alanında 'USA' yazın.</span><span class="sxs-lookup"><span data-stu-id="61525-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="61525-161">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61525-161">Click Save.</span></span>


