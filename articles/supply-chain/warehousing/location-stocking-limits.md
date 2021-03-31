---
title: Konum stoklama sınırları
description: Bu konu, konum stoklama limitlerinin işlevini açıklamaktadır.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e336b54b894669f8a49091473314e1d7d2639e5f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216993"
---
# <a name="location-stocking-limits"></a><span data-ttu-id="775c5-103">Konum stoklama sınırları</span><span class="sxs-lookup"><span data-stu-id="775c5-103">Location stocking limits</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="775c5-104">Fiziksel ürünlerin volümetrik hesaplamaları için daha gelişmiş işlemleri kullanmak sorunda kalmadan ambar konumlarındaki yük kapasitesini denetlemek amacıyla **Konum stoklama limitleri** sayfasını (**Ambar yönetimi \> Kurulum \> Ambar \> Konum stoklama limitleri**) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="775c5-104">You can use the **Location stocking limits** page (**Warehouse management \> Setup \> Warehouse \> Location stocking limits**) to control the load capacity at warehouse locations without having to use the more advanced processes for volumetric calculations of physical products.</span></span>

<span data-ttu-id="775c5-105">Konum stoklama limitlerinin amacı, bir konumun içerebileceği maksimum miktarı değerlendirmektir.</span><span class="sxs-lookup"><span data-stu-id="775c5-105">The purpose of location stocking limits is to evaluate the maximum quantity that a location can contain.</span></span> <span data-ttu-id="775c5-106">Özelliği, her biri **Konum stoklama limitleri** sayfasında kendi sekmesi bulunan üç düzeyden herhangi birine ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="775c5-106">You can set up the feature on any of three levels, each of which has its own tab on the **Location stocking limits** page:</span></span>

- <span data-ttu-id="775c5-107">Ürünler</span><span class="sxs-lookup"><span data-stu-id="775c5-107">Products</span></span>
- <span data-ttu-id="775c5-108">Ürün çeşitleri</span><span class="sxs-lookup"><span data-stu-id="775c5-108">Product variants</span></span>
- <span data-ttu-id="775c5-109">Konteyner türleri</span><span class="sxs-lookup"><span data-stu-id="775c5-109">Container types</span></span>

<span data-ttu-id="775c5-110">Her düzey için farklı alan değerleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="775c5-110">For each level, you can define different field values.</span></span> <span data-ttu-id="775c5-111">Sistem her satırın **Miktar** ve **birim** değerlerini esas alarak belirli bir konumun kapasitesini değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="775c5-111">The system will then evaluate the capacity of a specific location, based on the **Quantity** and **Unit** values for each row.</span></span> <span data-ttu-id="775c5-112">İlk olarak en ayrıntılı eşleşen kaydı seçer.</span><span class="sxs-lookup"><span data-stu-id="775c5-112">It will select the most detailed matching record first.</span></span> <span data-ttu-id="775c5-113">Örneğin, **Konum profil kodu** alanında değeri olan bir satır, yalnızca **Ambar** alanında değeri olan bir satırdan önce değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="775c5-113">For example, a row that has a value in the **Location profile ID** field will be evaluated before a row that has a value only in the **Warehouse** field.</span></span> <span data-ttu-id="775c5-114">Kullanılan konum stoklama limiti kaydı için **Miktar** değeri temel alınarak, kalan kapasite de değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="775c5-114">The remaining capacity will also be evaluated, based on the **Quantity** value for the location stocking limit record that is used.</span></span>

<span data-ttu-id="775c5-115">Bu sayfanın **Ürünler** bölümünde, konum stoklama limitleri araması için aşağıdaki alan değerlerini tanımlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="775c5-115">In the **Products** section of the page, you can define the following field values for the search for location stocking limits:</span></span>

- <span data-ttu-id="775c5-116">Ambar</span><span class="sxs-lookup"><span data-stu-id="775c5-116">Warehouse</span></span>
- <span data-ttu-id="775c5-117">Yerleşim profili kodu</span><span class="sxs-lookup"><span data-stu-id="775c5-117">Location profile ID</span></span>
- <span data-ttu-id="775c5-118">Yer</span><span class="sxs-lookup"><span data-stu-id="775c5-118">Location</span></span>
- <span data-ttu-id="775c5-119">Paket boyutu kategorisi kodu</span><span class="sxs-lookup"><span data-stu-id="775c5-119">Pack size category ID</span></span>
- <span data-ttu-id="775c5-120">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="775c5-120">Item number</span></span>
- <span data-ttu-id="775c5-121">Birim</span><span class="sxs-lookup"><span data-stu-id="775c5-121">Unit</span></span>

> [!NOTE]
> <span data-ttu-id="775c5-122">Her konum stoklama limiti kaydı için bir **Birim** değeri tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="775c5-122">You don't have to define a **Unit** value for each location stocking limit record.</span></span> <span data-ttu-id="775c5-123">Konum kapasitesi hesaplamaları, stok birimi miktarlarını temel alacaktır.</span><span class="sxs-lookup"><span data-stu-id="775c5-123">The location capacity calculations will be based on the inventory unit quantities.</span></span> <span data-ttu-id="775c5-124">Kullanılan bir değer için birim dönüştürme tanımlanmamışsa, konum stoklama limiti kaydı, kendisi için başka bir **Madde numarası** değeri tanımlanmış gibi atlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="775c5-124">If no unit conversion is defined for a value that is used, the location stocking limit record will be skipped, as if another **Item number** value is defined for it.</span></span>

## <a name="example--purchase-order-receiving"></a><span data-ttu-id="775c5-125">Örnek: Satın alma siparişi teslim alma</span><span class="sxs-lookup"><span data-stu-id="775c5-125">Example – Purchase order receiving</span></span>

<span data-ttu-id="775c5-126">Bu örnek, aşağıdaki değerlerin **Konum stoklama limitleri** sayfasının **Ürün çeşitleri** sekmesinde ayarlandığı, temiz bir *USMF* demo veri kümesine dayanır.</span><span class="sxs-lookup"><span data-stu-id="775c5-126">This example is based on a clean *USMF* demo data set, where the following values are set on the **Product variants** tab of the **Location stocking limits** page.</span></span>

| <span data-ttu-id="775c5-127">Ambar</span><span class="sxs-lookup"><span data-stu-id="775c5-127">Warehouse</span></span> | <span data-ttu-id="775c5-128">Yerleşim profili kodu</span><span class="sxs-lookup"><span data-stu-id="775c5-128">Location profile ID</span></span> | <span data-ttu-id="775c5-129">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="775c5-129">Item number</span></span> | <span data-ttu-id="775c5-130">Boyut</span><span class="sxs-lookup"><span data-stu-id="775c5-130">Size</span></span> | <span data-ttu-id="775c5-131">Miktar</span><span class="sxs-lookup"><span data-stu-id="775c5-131">Quantity</span></span> | <span data-ttu-id="775c5-132">Birim</span><span class="sxs-lookup"><span data-stu-id="775c5-132">Unit</span></span> |
|-----------|---------------------|-------------|------|----------|------|
| <span data-ttu-id="775c5-133">24</span><span class="sxs-lookup"><span data-stu-id="775c5-133">24</span></span>        | <span data-ttu-id="775c5-134">KAT</span><span class="sxs-lookup"><span data-stu-id="775c5-134">FLOOR</span></span>               | <span data-ttu-id="775c5-135">D0013</span><span class="sxs-lookup"><span data-stu-id="775c5-135">D0013</span></span>       | <span data-ttu-id="775c5-136">P</span><span class="sxs-lookup"><span data-stu-id="775c5-136">M</span></span>    | <span data-ttu-id="775c5-137">300</span><span class="sxs-lookup"><span data-stu-id="775c5-137">300</span></span>      | <span data-ttu-id="775c5-138">Her</span><span class="sxs-lookup"><span data-stu-id="775c5-138">Ea</span></span>   |
| <span data-ttu-id="775c5-139">24</span><span class="sxs-lookup"><span data-stu-id="775c5-139">24</span></span>        | <span data-ttu-id="775c5-140">KAT</span><span class="sxs-lookup"><span data-stu-id="775c5-140">FLOOR</span></span>               | <span data-ttu-id="775c5-141">D0013</span><span class="sxs-lookup"><span data-stu-id="775c5-141">D0013</span></span>       | <span data-ttu-id="775c5-142">L</span><span class="sxs-lookup"><span data-stu-id="775c5-142">L</span></span>    | <span data-ttu-id="775c5-143">240</span><span class="sxs-lookup"><span data-stu-id="775c5-143">240</span></span>      | <span data-ttu-id="775c5-144">Her</span><span class="sxs-lookup"><span data-stu-id="775c5-144">Ea</span></span>   |
| <span data-ttu-id="775c5-145">24</span><span class="sxs-lookup"><span data-stu-id="775c5-145">24</span></span>        | <span data-ttu-id="775c5-146">KAT</span><span class="sxs-lookup"><span data-stu-id="775c5-146">FLOOR</span></span>               | <span data-ttu-id="775c5-147">D0013</span><span class="sxs-lookup"><span data-stu-id="775c5-147">D0013</span></span>       | <span data-ttu-id="775c5-148">C</span><span class="sxs-lookup"><span data-stu-id="775c5-148">S</span></span>    | <span data-ttu-id="775c5-149">360</span><span class="sxs-lookup"><span data-stu-id="775c5-149">360</span></span>      | <span data-ttu-id="775c5-150">Her</span><span class="sxs-lookup"><span data-stu-id="775c5-150">Ea</span></span>   |

<span data-ttu-id="775c5-151">Ürünler için farklı ölçü birimi ürün çeşitleri ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="775c5-151">Different unit of measure product variants are set up for the products.</span></span> <span data-ttu-id="775c5-152">Bu çeşitler üç palet (PL) için konum stoklama limitleriyle hizalanır:</span><span class="sxs-lookup"><span data-stu-id="775c5-152">These variants are aligned with the location stocking limits for three pallets (PL):</span></span>

- <span data-ttu-id="775c5-153">**M Boyutu:** 1 PL = her biri 100 (Ea)</span><span class="sxs-lookup"><span data-stu-id="775c5-153">**Size M:** 1 PL = 100 each (Ea)</span></span>
- <span data-ttu-id="775c5-154">**L Boyutu:** 1 PL = 80 Ea</span><span class="sxs-lookup"><span data-stu-id="775c5-154">**Size L:** 1 PL = 80 Ea</span></span>
- <span data-ttu-id="775c5-155">**S Boyutu:** 1 PL = 120 Ea</span><span class="sxs-lookup"><span data-stu-id="775c5-155">**Size S:** 1 PL = 120 Ea</span></span>

<span data-ttu-id="775c5-156">Bu nedenle, **Konum profili kodu** değerinin *KAT* olarak ayarlandığı her konum D *0013* madde numarasından *3* *PL* içerebilir.</span><span class="sxs-lookup"><span data-stu-id="775c5-156">Therefore, each location where the **Location profile ID** value is set to *FLOOR* can carry *3* *PL* of item number *D0013*.</span></span>

### <a name="prepare-for-the-example"></a><span data-ttu-id="775c5-157">Örneğe hazırlık</span><span class="sxs-lookup"><span data-stu-id="775c5-157">Prepare for the example</span></span>

<span data-ttu-id="775c5-158">Bu örnekte, iki satır için bir satın alma siparişi teslim alma akışı çalıştırırsınız.</span><span class="sxs-lookup"><span data-stu-id="775c5-158">In this example, you will run a purchase order receiving flow for two lines.</span></span> <span data-ttu-id="775c5-159">Ancak, konumların karışık maddelerin taşınmasına izin verdiğinden, yalnızca *FL-002* ile *FL-004* arasındaki boş konumların kullanıldığından ve açık bir gelen iş bulunmadığından emin olmak için öncelikle demo verilerini aşağıdaki şekilde güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="775c5-159">However, you must first update the demo data in the following way to ensure that the locations allow mixed items to be carried, only the empty locations *FL-002* through *FL-004* are used, and there is no open inbound work.</span></span>

1. <span data-ttu-id="775c5-160">*FL-001* konumu için **Konum profili** alanının değerini *KAT* yerine *KAT-05* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="775c5-160">For location *FL-001*, change the value of the **Location profile** field from *FLOOR* to *FLOOR-05*.</span></span>
1. <span data-ttu-id="775c5-161">*KAT* konumu profili için **Karışık maddelere izin ver** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="775c5-161">For the *FLOOR* location profile, set the **Allow mixed items** option to *Yes*.</span></span>
1. <span data-ttu-id="775c5-162">Aşağıdaki iki satıra sahip satın alma siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="775c5-162">Create a purchase order that has the following two lines.</span></span>

    | <span data-ttu-id="775c5-163">Ambar</span><span class="sxs-lookup"><span data-stu-id="775c5-163">Warehouse</span></span> | <span data-ttu-id="775c5-164">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="775c5-164">Item number</span></span> | <span data-ttu-id="775c5-165">Boyut</span><span class="sxs-lookup"><span data-stu-id="775c5-165">Size</span></span> | <span data-ttu-id="775c5-166">Miktar</span><span class="sxs-lookup"><span data-stu-id="775c5-166">Quantity</span></span> | <span data-ttu-id="775c5-167">Birim</span><span class="sxs-lookup"><span data-stu-id="775c5-167">Unit</span></span> |
    |-----------|-------------|------|----------|------|
    | <span data-ttu-id="775c5-168">24</span><span class="sxs-lookup"><span data-stu-id="775c5-168">24</span></span>        | <span data-ttu-id="775c5-169">D0013</span><span class="sxs-lookup"><span data-stu-id="775c5-169">D0013</span></span>       | <span data-ttu-id="775c5-170">C</span><span class="sxs-lookup"><span data-stu-id="775c5-170">S</span></span>    | <span data-ttu-id="775c5-171">4</span><span class="sxs-lookup"><span data-stu-id="775c5-171">4</span></span>        | <span data-ttu-id="775c5-172">PL</span><span class="sxs-lookup"><span data-stu-id="775c5-172">PL</span></span>   |
    | <span data-ttu-id="775c5-173">24</span><span class="sxs-lookup"><span data-stu-id="775c5-173">24</span></span>        | <span data-ttu-id="775c5-174">D0013</span><span class="sxs-lookup"><span data-stu-id="775c5-174">D0013</span></span>       | <span data-ttu-id="775c5-175">L</span><span class="sxs-lookup"><span data-stu-id="775c5-175">L</span></span>    | <span data-ttu-id="775c5-176">4</span><span class="sxs-lookup"><span data-stu-id="775c5-176">4</span></span>        | <span data-ttu-id="775c5-177">PL</span><span class="sxs-lookup"><span data-stu-id="775c5-177">PL</span></span>   |

### <a name="process-the-example"></a><span data-ttu-id="775c5-178">Örneği işleme</span><span class="sxs-lookup"><span data-stu-id="775c5-178">Process the example</span></span>

<span data-ttu-id="775c5-179">Önce *S* boyutunda *4* birim *PL* miktarı alacak ve oluşturulan iş için yerine koyma satırı konumlarını gözden geçireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="775c5-179">You will first receive a quantity of *4* of unit *PL* in size *S*, and review the put line locations for the work that is created.</span></span> <span data-ttu-id="775c5-180">Daha sonra *L* boyutunda *4* birim *PL* miktarı alacak ve oluşturulan iş için yerine koyma satırı konumlarını gözden geçireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="775c5-180">You will then receive a quantity of *4* of unit *PL* in size *L*, and review the put line locations for the work that is created.</span></span>

1. <span data-ttu-id="775c5-181">Ambar uygulamasında, kullanıcı kimliği *24* ve parola olarak *1*'i kullanarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="775c5-181">In the warehouse app, sign in by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="775c5-182">**Gelen** \> **Satın Alma Teslim Alma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="775c5-182">Select **Inbound** \> **Purchase Receive**.</span></span>
1. <span data-ttu-id="775c5-183">Madde numarası *D0013*'ten *S* boyutunda *4* *PL* alır.</span><span class="sxs-lookup"><span data-stu-id="775c5-183">Receive *4* *PL* of item number *D0013* in size *S*.</span></span>
1. <span data-ttu-id="775c5-184">Oluşturulan yerine koyma işini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="775c5-184">Review the putaway work that was created.</span></span> <span data-ttu-id="775c5-185">Aşağıdaki sonucu görmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="775c5-185">You should see the following result:</span></span>

    - <span data-ttu-id="775c5-186">3 PL -\> FL-002</span><span class="sxs-lookup"><span data-stu-id="775c5-186">3 PL -\> FL-002</span></span>
    - <span data-ttu-id="775c5-187">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="775c5-187">1 PL -\> FL-003</span></span>

1. <span data-ttu-id="775c5-188">Madde numarası *D0013*'ten *L* boyutunda *4* *PL* alır.</span><span class="sxs-lookup"><span data-stu-id="775c5-188">Receive *4* *PL* of item number *D0013* in size *L*.</span></span>
1. <span data-ttu-id="775c5-189">Oluşturulan yerine koyma işini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="775c5-189">Review the putaway work that was created.</span></span> <span data-ttu-id="775c5-190">Aşağıdaki sonucu görmeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="775c5-190">You should see the following result:</span></span>

    - <span data-ttu-id="775c5-191">1 PL -\> FL-003</span><span class="sxs-lookup"><span data-stu-id="775c5-191">1 PL -\> FL-003</span></span>
    - <span data-ttu-id="775c5-192">3 PL -\> FL-004</span><span class="sxs-lookup"><span data-stu-id="775c5-192">3 PL -\> FL-004</span></span>

<span data-ttu-id="775c5-193">Sonuçlara göre, sistemin doğru yerine koyma konumlarını tahsis edemediği sonucuna varabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="775c5-193">Based on the results, you might conclude that the system failed to allocate the correct putaway locations.</span></span> <span data-ttu-id="775c5-194">Değilse, sistem son adımda *FL-003* konumuna *L* boyutundan neden yalnızca *1* *PL* ekleyip *2* *PL* eklemedi?</span><span class="sxs-lookup"><span data-stu-id="775c5-194">Otherwise, why did the system add only *1* *PL* of size *L* to location *FL-003* in the last step, not *2* *PL*?</span></span> <span data-ttu-id="775c5-195">Yani, bu konuma yerine koyma için neden toplam *3* *PL* yok?</span><span class="sxs-lookup"><span data-stu-id="775c5-195">That is, why isn't there is a total of *3* *PL* for putaway to that location?</span></span>

<span data-ttu-id="775c5-196">Bu görünür hatayı açıklamak için konum stoklama limitlerinin seçim ölçütünü anlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="775c5-196">To explain this apparent failure, you must understand the selection criteria for the location stocking limits.</span></span> <span data-ttu-id="775c5-197">Sistem en ayrıntılı eşleşen kaydı seçer.</span><span class="sxs-lookup"><span data-stu-id="775c5-197">The system selects the most detailed matching record.</span></span> <span data-ttu-id="775c5-198">Bu örnekte, en ayrıntılı eşleme kaydı **Boyut** değerinin *L* olduğu, **Miktar** değerinin *240* olduğu ve **Birim** değerinin de *Ea* olduğu satırdır.</span><span class="sxs-lookup"><span data-stu-id="775c5-198">In this example, the most detailed matching record is the line where the **Size** value is *L*, the **Quantity** value is *240*, and the **Unit** value is *Ea*.</span></span> <span data-ttu-id="775c5-199">*S* boyutundan önceki *120* *Ea* miktarı girişten açık işiniz olduğu için kalan kapasite *240* – *120* = *120* *Ea* olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="775c5-199">Because you already have open work from the previous receipt of a quantity of *120* *Ea* of size *S*, the remaining capacity is calculated as *240* – *120* = *120* *Ea*.</span></span> <span data-ttu-id="775c5-200">Bu nedenle, kalan kapasite yalnızca *1* *PL* *80* *Ea* taşıyabilir</span><span class="sxs-lookup"><span data-stu-id="775c5-200">Therefore, the remaining capacity can carry only *1* *PL* of *80* *Ea*.</span></span>

> [!NOTE]
> <span data-ttu-id="775c5-201">Aynı konumda farklı miktarları olan maddelerin stok yenilemesini denetlemek için konum stoklama limitlerini kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="775c5-201">You can't use location stocking limits to control, for example, the replenishment of items that have different quantities in the same location.</span></span> <span data-ttu-id="775c5-202">Bu durumda, bir *stok yenileme şablonu* kullanın.</span><span class="sxs-lookup"><span data-stu-id="775c5-202">In this case, use a *replenishment template*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]