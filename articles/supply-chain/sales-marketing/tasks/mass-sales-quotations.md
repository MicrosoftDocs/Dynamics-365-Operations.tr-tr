--- 
title: "Satış tekliflerini toplu olarak oluştur"
description: "Bu yordam, birden fazla müşteriye gönderilecek ürünler ve hizmetler kümesi sunan tekliflerin nasıl etkin biçimde oluşturulacağını göstermektedir."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e3bc39912d19880258ff7dd56c74b77b52deda3a
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="a9c5d-103">Satış tekliflerini toplu olarak oluştur</span><span class="sxs-lookup"><span data-stu-id="a9c5d-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9c5d-104">Bu yordam, birden fazla müşteriye gönderilecek ürünler ve hizmetler kümesi sunan tekliflerin nasıl etkin biçimde oluşturulacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="a9c5d-105">Bu toplu teklif oluşturma işlemi teklif şablonlarını temel alır.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="a9c5d-106">Bu yordamı, kendi verilerinizle veya USMF demo verisi şirketin çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="a9c5d-107">Bir teklif şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9c5d-107">Create a quotation template</span></span>
1. <span data-ttu-id="a9c5d-108">Sales and marketing > Setup > Quotations > Template groups (Satış ve pazarlama > Ayarlama > Teklifler > Şablon grupları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="a9c5d-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-109">Click New.</span></span>
3. <span data-ttu-id="a9c5d-110">Grup Kodu alanında seçtiğiniz kod türünü girin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="a9c5d-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a9c5d-112">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-112">Click Save.</span></span>
6. <span data-ttu-id="a9c5d-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-113">Close the page.</span></span>
7. <span data-ttu-id="a9c5d-114">Sales and marketing > Sales quotations > All quotations (Satış ve pazarlama > Satış teklifleri > Tüm teklifler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="a9c5d-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-115">Click New.</span></span>
9. <span data-ttu-id="a9c5d-116">Hesap türü alanında 'Müşteri' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="a9c5d-117">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="a9c5d-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-118">Click OK.</span></span>
    * <span data-ttu-id="a9c5d-119">Bir teklifin şablona dönüşmesi için teklif başlığındaki kurulum adımlarını gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="a9c5d-120">Bunu teklife satır eklemeden önce yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="a9c5d-121">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="a9c5d-122">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-122">Click Change view.</span></span>
14. <span data-ttu-id="a9c5d-123">Başlık görünümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-123">Click Header view.</span></span>
15. <span data-ttu-id="a9c5d-124">Kurulum bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="a9c5d-125">Grup kodu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="a9c5d-126">Şablon adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="a9c5d-127">Etkin alanında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="a9c5d-128">Yeni bir satış teklifine bir şablon uyguladığınızda, yalnızca etkin şablonlar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="a9c5d-129">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="a9c5d-130">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-130">Click Change view.</span></span>
21. <span data-ttu-id="a9c5d-131">Satır görünümü'nü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-131">Click Line view.</span></span>
22. <span data-ttu-id="a9c5d-132">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="a9c5d-133">Ürün alanında bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="a9c5d-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-134">Close the page.</span></span>
25. <span data-ttu-id="a9c5d-135">İskonto yüzdesi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="a9c5d-136">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-136">Click Add line.</span></span>
27. <span data-ttu-id="a9c5d-137">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="a9c5d-138">Ürün alanında bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="a9c5d-139">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-139">Close the page.</span></span>
30. <span data-ttu-id="a9c5d-140">Birim fiyat alanında, yeni fiyat girin veya geçerli olanı değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="a9c5d-141">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-141">Click Add line.</span></span>
32. <span data-ttu-id="a9c5d-142">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="a9c5d-143">Ürün alanında bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="a9c5d-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-144">Close the page.</span></span>
35. <span data-ttu-id="a9c5d-145">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="a9c5d-146">İskonto alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="a9c5d-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="a9c5d-148">Tek bir teklif oluşturmak için şablon uygulama</span><span class="sxs-lookup"><span data-stu-id="a9c5d-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="a9c5d-149">Sales and marketing > Sales quotations > All quotations (Satış ve pazarlama > Satış teklifleri > Tüm teklifler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="a9c5d-150">Yeni oluşturduğunuz teklifin şablon olarak işaretlendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="a9c5d-151">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-151">Click New.</span></span>
3. <span data-ttu-id="a9c5d-152">Hesap türü alanında 'Müşteri' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="a9c5d-153">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="a9c5d-154">Şablon bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-154">Expand the Template section.</span></span>
6. <span data-ttu-id="a9c5d-155">Grup kodu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="a9c5d-156">Şablon adı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="a9c5d-157">Hesaplama yöntemi alanında 'Şablon değerlerine dayalı' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="a9c5d-158">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-158">Click OK.</span></span>
    * <span data-ttu-id="a9c5d-159">Yeni teklif şablonun verileri ve koşulları temel alınarak oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="a9c5d-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-160">Close the page.</span></span>
11. <span data-ttu-id="a9c5d-161">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="a9c5d-162">Teklifleri toplu şekilde oluşturmak için şablon uygulama</span><span class="sxs-lookup"><span data-stu-id="a9c5d-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="a9c5d-163">Sales and marketing > Sales quotations > Quotation update > Mass create quotations (Satış ve pazarlama > Satış teklifleri > Teklif güncelleştirmesi > Teklifleri toplu olarak oluştur) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="a9c5d-164">Hesap türü alanında 'Müşteri' seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="a9c5d-165">Grup kodu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="a9c5d-166">Şablon adı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="a9c5d-167">Hesaplama yöntemi alanında 'Şablon değerlerine dayalı' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="a9c5d-168">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="a9c5d-169">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-169">Click Filter.</span></span>
8. <span data-ttu-id="a9c5d-170">Ölçüt alanında, bu toplu teklif oluşturma işlemine dahil etmek istediğiniz müşterileri kapsamına alan bir filtre ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="a9c5d-171">Şu biçimi kullanın: "Customer1..CustomerN.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="a9c5d-172">Örneğin, filtreyi US-001..US-004 olarak ayarlayabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a9c5d-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="a9c5d-173">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-173">Click OK.</span></span>
10. <span data-ttu-id="a9c5d-174">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-174">Click OK.</span></span>
11. <span data-ttu-id="a9c5d-175">Sales and marketing > Sales quotations > All quotations (Satış ve pazarlama > Satış teklifleri > Tüm teklifler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="a9c5d-176">Tekliflerin seçili şablon temel alınarak toplu güncelleştirme rutininde belirtilen tüm müşteriler için oluşturulduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a9c5d-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  


