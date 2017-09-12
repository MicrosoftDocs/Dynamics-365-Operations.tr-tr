--- 
title: "Satış teklifleri oluşturma ve düzenleme"
description: "Bu yordam, bir satış teklifinin nasıl oluşturulacağını ve güncelleştirileceğini göstermektedir."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f56b495131836689395a2124d5a834579e1646b7
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="b9fd4-103">Satış teklifleri oluşturma ve düzenleme</span><span class="sxs-lookup"><span data-stu-id="b9fd4-103">Create and edit sales quotations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9fd4-104">Bu yordam, bir satış teklifinin nasıl oluşturulacağını ve güncelleştirileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="b9fd4-105">Bu yordamı, kendi verilerinizle veya USMF demo verisi şirketin çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="b9fd4-106">Satış teklifi oluşturma</span><span class="sxs-lookup"><span data-stu-id="b9fd4-106">Create a sales quotation</span></span>
1. <span data-ttu-id="b9fd4-107">Sales and marketing > Sales quotations > All quotations (Satış ve pazarlama > Satış teklifleri > Tüm teklifler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="b9fd4-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-108">Click New.</span></span>
3. <span data-ttu-id="b9fd4-109">Hesap türü alanında Aday müşteri'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="b9fd4-110">Aday müşteri alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="b9fd4-111">Genel bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-111">Expand the General section.</span></span>
    * <span data-ttu-id="b9fd4-112">Satış ve Pazarlama alanında bir teklif oluşturmayı seçtiğinizden, tür otomatik olarak Satış teklifi olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="b9fd4-113">Bir projeye ilişkin teklif oluşturmak için Proje yönetimi ve muhasebe modülünden projeye erişmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="b9fd4-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-114">Click OK.</span></span>
    * <span data-ttu-id="b9fd4-115">Teklif satırlarındaki alanlar ve eylemler satış siparişi satırlarındakilere çok benzerdir.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="b9fd4-116">Satış siparişleri gibi teklifler de belirli bir ürün için oluşturulabilir. Ayrıca, ürün kodu bilinmiyorsa veya teklif oluşturma sırasında yoksa, teklifler bir satış kategorisi için de oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="b9fd4-117">Ürün alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="b9fd4-118">Ürün alanında bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="b9fd4-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-119">Close the page.</span></span>
10. <span data-ttu-id="b9fd4-120">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b9fd4-121">Satırda seçilen ürüne ilişkin geçerli ticari anlaşmalar varsa, uygun fiyat ve iskontolar teklif satırına otomatik olarak kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="b9fd4-122">Birim fiyat alanında bir değer bulunduğundan emin olun ve istiyorsanız iskonto değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="b9fd4-123">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-123">Click Save.</span></span>
12. <span data-ttu-id="b9fd4-124">Eylem Bölmesinde, Satış teklifi öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="b9fd4-125">Toplamlar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-125">Click Totals.</span></span>
14. <span data-ttu-id="b9fd4-126">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-126">Click OK.</span></span>
15. <span data-ttu-id="b9fd4-127">Satış teklifi satırına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="b9fd4-128">Fiyatlar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-128">Click Prices.</span></span>
    * <span data-ttu-id="b9fd4-129">Fiyat benzetimi çalıştır sayfasında istenen birim fiyatı, iskonto tutarı, iskonto yüzdesi, toplam tutarı, marjı veya katkı oranı temelinde teklifin beklenen gelirini ve kârlılığını ayarlayarak deneme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="b9fd4-130">Hedef rakamlar istediğiniz seviyeye geldiğinde öneriyi teklif satırına uygulayın, ardından fiyat ile ilgili alanları buna göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="b9fd4-131">İstediğiniz sayıda fiyat benzetimi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="b9fd4-132">Yeni'yi tıklattığınızda, geçerli teklif satırındaki fiyat koşulları sayfaya kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="b9fd4-133">Daha sonra fiyat ile ilgili herhangi bir alanda değerleri değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="b9fd4-134">Alanlardan birinde yapılan değişiklik tüm diğer alanlarda yeniden hesaplama yapılmasını tetikler.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="b9fd4-135">Sistemin satış marjının ve katkı oranının hesaplanabilmesi için ürünün birim maliyeti bilinmelidir.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="b9fd4-136">Orijinal fiyatların, önerilen fiyatların ve teklif toplamlarına etkisinin ayrıntılı bir görünümü için Benzetimli fiyatlar sekmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="b9fd4-137">Genel bir kural olarak, yeni bir tutar ayarlayan bir benzetim teklif satırına uygulandığında sistem yeniden hesaplama yapar ve Birim fiyat alanında yeni bir değer girer.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="b9fd4-138">Benzetim yeni bir marjı veya katkı oranını esas alıyorsa, yalnızca Net Tutar alanı güncelleştirilir ve Birim fiyat boş bırakılır.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="b9fd4-139">Her iki durumda da, benzetimden önce teklif satırında bulunan tüm iskontolar silinir.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="b9fd4-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-140">Close the page.</span></span>
18. <span data-ttu-id="b9fd4-141">Eylem Bölmesinde Teklif öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="b9fd4-142">Teklifi gönder öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-142">Click Send quotation.</span></span>
20. <span data-ttu-id="b9fd4-143">Teklifi yazdır alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="b9fd4-144">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-144">Click OK.</span></span>
    * <span data-ttu-id="b9fd4-145">Raporun oluşturulması bir dakika kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-145">The report may take a minute to generate.</span></span> <span data-ttu-id="b9fd4-146">Oluşturulana kadar sayfayı kapatmayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="b9fd4-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="b9fd4-148">Satış teklifini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b9fd4-148">Update a sales quotation</span></span>
1. <span data-ttu-id="b9fd4-149">Eylem Bölmesinde İzle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="b9fd4-150">Müşteriye dönüştür'ü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="b9fd4-151">Müşteri hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="b9fd4-152">Denetle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-152">Click Check.</span></span>
    * <span data-ttu-id="b9fd4-153">Yazdığınız hesap numarasının kullanılabileceğini belirten bir ileti gördüğünüzden emin olun.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="b9fd4-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-154">Click OK.</span></span>
    * <span data-ttu-id="b9fd4-155">Sistem, teklifteki aday müşteri için yeni bir müşteri hesabı oluşturmuştur.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="b9fd4-156">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-156">Close the page.</span></span>
7. <span data-ttu-id="b9fd4-157">Eylem Bölmesinde İzle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="b9fd4-158">Onayla seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-158">Click Confirm.</span></span>
9. <span data-ttu-id="b9fd4-159">Neden alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="b9fd4-160">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-160">Click OK.</span></span>
11. <span data-ttu-id="b9fd4-161">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="b9fd4-162">Satış siparişleri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-162">Click Sales orders.</span></span>
13. <span data-ttu-id="b9fd4-163">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b9fd4-163">Close the page.</span></span>


