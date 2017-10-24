--- 
title: "RFQ tekliflerini girip karşılaştırma ve işi verme"
description: "Bu prosedürde bir RFQ'ya yanıtların nasıl girileceği, tekliflerin nasıl puanlandırılacağı ve karşılaştırılacağı ve ardından teklif için satıcılardan birinin nasıl seçileceği gösterilmiştir."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="3d67b-103">RFQ tekliflerini girip karşılaştırma ve işi verme</span><span class="sxs-lookup"><span data-stu-id="3d67b-103">Enter and compare RFQ bids and award contracts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d67b-104">Bu prosedürde bir RFQ'ya yanıtların nasıl girileceği, tekliflerin nasıl puanlandırılacağı ve karşılaştırılacağı ve ardından teklif için satıcılardan birinin nasıl seçileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="3d67b-105">Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="3d67b-106">Başlamadan önce, en az iki satıcıya gönderilmiş iki satır içeren bir RFQ'ya sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="3d67b-107">Bunun oluşturulması için bir ön şart olarak "Teklif için bir talep oluştur" prosedürünü yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="3d67b-108">Bu prosedürü yürütmeden önce puanlama ölçütlerini belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="3d67b-109">Bir satıcı yanıtı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="3d67b-110">Tedarik ve kaynak atama > Teklif talepleri > Tüm teklif talepleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="3d67b-111">Gönderilmiş durumuna sahip bir RFQ seçin ve Teklif talebi olay numarası üzerindeki bağlantıyı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="3d67b-112">RFQ en az 2 satıcıya gönderilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3d67b-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="3d67b-113">Satıcıların listesine gitmek için Başlığı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="3d67b-114">RFQ için bir yanıt girmek istediğiniz satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="3d67b-115">Yanıt gir düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-115">Click Enter reply.</span></span>
6. <span data-ttu-id="3d67b-116">Eylem Bölmesinde, Yanıtla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="3d67b-117">Verileri yanıta kopyala düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="3d67b-118">Bu eylem seçili verileri, örneğin, RFQ olayındaki miktarları RFQ yanıtına kopyalar.</span><span class="sxs-lookup"><span data-stu-id="3d67b-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="3d67b-119">Alternatif olarak, bu eylemi atlayabilir ve yanıtı düzenlerken tüm yanıt alanlarını el ile doldurabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="3d67b-120">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-120">Click Edit.</span></span>
9. <span data-ttu-id="3d67b-121">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="3d67b-122">Başka bir teklif satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="3d67b-123">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="3d67b-124">Teklifi puanlama</span><span class="sxs-lookup"><span data-stu-id="3d67b-124">Score the bid</span></span>
1. <span data-ttu-id="3d67b-125">Teklif puanlamasına gitmek için Başlığı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="3d67b-126">Teklif puanlama bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="3d67b-127">Puan alanına, bir puanlama ölçütü için bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="3d67b-128">Fare imlecini bir puanlama ölçütünün üzerine getirdiğinizde, puanınızın bulunması gereken aralığı gösteren bir araç ipucu açılır.</span><span class="sxs-lookup"><span data-stu-id="3d67b-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="3d67b-129">Bu demoda tüm ölçütler için 1 ile 5 arasında bir sayı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="3d67b-130">Başka bir puanlama ölçütünü seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="3d67b-131">Puan alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="3d67b-132">Anketler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="3d67b-133">RFQ olayı, satıcılara gönderilen bir ankete sahipse, satıcıların yanıtlarını anket bölümüne girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="3d67b-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="3d67b-135">Başka bir satıcı için yanıt girme</span><span class="sxs-lookup"><span data-stu-id="3d67b-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="3d67b-136">Bir az önce yanıt girdiğiniz satıcıyı silerek ve ardından bir sonraki satıcı için satırı seçerek bir sonraki satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="3d67b-137">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3d67b-138">Yanıt gir düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-138">Click Enter reply.</span></span>
4. <span data-ttu-id="3d67b-139">Verileri yanıta kopyala düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="3d67b-140">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-140">Click Edit.</span></span>
6. <span data-ttu-id="3d67b-141">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="3d67b-142">Başka bir teklif satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="3d67b-143">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="3d67b-144">İkinci teklifi puanlama</span><span class="sxs-lookup"><span data-stu-id="3d67b-144">Score the second bid</span></span>
1. <span data-ttu-id="3d67b-145">Teklif puanlamasına gitmek için Başlığı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="3d67b-146">Puan alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="3d67b-147">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="3d67b-148">Puan alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="3d67b-149">Teklifleri karşılaştırma</span><span class="sxs-lookup"><span data-stu-id="3d67b-149">Compare the replies</span></span>
1. <span data-ttu-id="3d67b-150">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="3d67b-151">Yanıtları karşılaştır düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-151">Click Compare replies.</span></span>
3. <span data-ttu-id="3d67b-152">Sıralama alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="3d67b-153">Bu sayfada başlık ve satırlarıyla birlikte teklifler ve başlık seviyesinde toplam puan gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="3d67b-154">Satırları, karşılaştırabilir satırlar birbirinin yanına gelecek şekilde ızgarada sıralayarak karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="3d67b-155">Bu bilgiler ayrıca şunları içerir:   Miktar: Satıcı tarafından teklif edilen miktar.</span><span class="sxs-lookup"><span data-stu-id="3d67b-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="3d67b-156">Bu miktar, RFQ tarafından belirtilen miktara eşit olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="3d67b-157">Net miktar: Bir satıcı tarafından satırda belirtilen maddeler için iskontolar çıkarıldıktan sonra teklif edilen fiyattır.</span><span class="sxs-lookup"><span data-stu-id="3d67b-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="3d67b-158">Sapma: Teklif başlığında veya satırında belirtilen teslimat tarihinin RFQ başlığında veya RFQ satırında talep edilen teslimat tarihine göre, gün cinsinden sapma miktarı.</span><span class="sxs-lookup"><span data-stu-id="3d67b-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="3d67b-159">Her bir teklif için bira aralık girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="3d67b-160">Sıralamak istediğiniz diğer tekliflerin başlık satırlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="3d67b-161">Sıralama alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="3d67b-162">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="3d67b-163">Bir teklifi reddetme</span><span class="sxs-lookup"><span data-stu-id="3d67b-163">Reject a bid</span></span>
1. <span data-ttu-id="3d67b-164">Reddetmek istediğiniz teklifin başlık satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="3d67b-165">Aynı anda sadece bir teklifi veya bir teklif içindeki satırları kabul edebilir, reddedebilir veya iade edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="3d67b-166">İşaret onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="3d67b-167">Teklif başlığındaki seçim kutusunu İşaretle seçimini yaparsanız tüm satırlar işaretlenecektir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="3d67b-168">Ayrıca, reddetmek veya kabul etmek için bir teklif içindeki satırların bir alt kümesini de işaretlemeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="3d67b-169">Bir satıcının teklifinin bir RFQ'nun bazı satırları için kabul edilmesi ve ardından diğer RFQ satırlarının başka bir satıcıya verilmesi mümkündür, ancak aynı anda bir teklif olacak şekilde bunu 2 adımda gerçekleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="3d67b-170">Başka satırlar varsa, sadece orijinal teklif satırını veya başka bir satırı kabule edebilirsiniz, her ikisini aynı anda kabul edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="3d67b-171">Reddet düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-171">Click Reject.</span></span>
4. <span data-ttu-id="3d67b-172">İletişim kutusunu açmak için Parametreler'i tıklatın</span><span class="sxs-lookup"><span data-stu-id="3d67b-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="3d67b-173">Reddetme gerekçesi alanında, bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="3d67b-174">Reddetme nedeni cevaba kaydedilecektir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="3d67b-175">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-175">Click OK.</span></span>
7. <span data-ttu-id="3d67b-176">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-176">Click OK.</span></span>
8. <span data-ttu-id="3d67b-177">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-177">Close the page.</span></span>
9. <span data-ttu-id="3d67b-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-178">Close the page.</span></span>
10. <span data-ttu-id="3d67b-179">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="3d67b-180">Bir teklifi kabul etme</span><span class="sxs-lookup"><span data-stu-id="3d67b-180">Accept a bid</span></span>
1. <span data-ttu-id="3d67b-181">Kabul etmek istediğiniz teklifi seçin ve ardından Teklif talebi alanında bağlantıyı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="3d67b-182">Eylem Bölmesinde, Yanıtla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="3d67b-183">Kabul et düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-183">Click Accept.</span></span>
    * <span data-ttu-id="3d67b-184">Belirli satırları işaretler ve belirli satırları işaretlemezseniz, kabul eylemi sadece işaretlenmiş satırları içerecektir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="3d67b-185">Teklifteki tüm satırları kabul etmek isterseniz, satırları işaretlemenize gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="3d67b-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="3d67b-186">İletişim kutusunu açmak için Parametreler'i tıklatın</span><span class="sxs-lookup"><span data-stu-id="3d67b-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="3d67b-187">Bu da teklifin kabul edilmesi için bir gerekçe kaydetmenize olanak verir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="3d67b-188">Gerekçe, teklif üzerine kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="3d67b-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="3d67b-189">Kabul gerekçesi alanında, bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="3d67b-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="3d67b-190">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-190">Click OK.</span></span>
7. <span data-ttu-id="3d67b-191">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-191">Click OK.</span></span>
    * <span data-ttu-id="3d67b-192">Tamam düğmesini tıkladığınızda RFQ kabulüne dahil edilen satırlara dayalı olarak bir satın alma emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3d67b-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="3d67b-193">Henüz işlenmemiş (kabul edilmiş, reddedilmiş veya iade edilmiş) başka teklifler varsa sistem, kalan teklifleri reddetmeniz için bir mesaj görüntüler.</span><span class="sxs-lookup"><span data-stu-id="3d67b-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="3d67b-194">Oluşturulmuş bir satın alma emrini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="3d67b-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="3d67b-195">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="3d67b-196">Satın alma siparişini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-196">Click Purchase order.</span></span>
    * <span data-ttu-id="3d67b-197">Burada, teklifi kabul ettiğinizde oluşturulmuş olan satın alma emrini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d67b-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="3d67b-198">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-198">Close the page.</span></span>
4. <span data-ttu-id="3d67b-199">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-199">Close the page.</span></span>
5. <span data-ttu-id="3d67b-200">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-200">Close the page.</span></span>
6. <span data-ttu-id="3d67b-201">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d67b-201">Close the page.</span></span>


