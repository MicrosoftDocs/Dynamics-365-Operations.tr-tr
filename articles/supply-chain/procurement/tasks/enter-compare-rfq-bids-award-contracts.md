---
title: RFQ tekliflerini girme ve karşılaştırma ve işi verme
description: Bu prosedürde bir teklif talebine (RFQ) yanıtların nasıl girileceği, tekliflerin nasıl puanlandırılacağı ve karşılaştırılacağı ve ardından sözleşme için satıcılardan birinin nasıl seçileceği gösterilmiştir.
author: mkirknel
manager: AnnBe
ms.date: 02/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45ddab03810b331bcd8965f6a2ba699ffb138910
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1533364"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="baea2-103">RFQ tekliflerini girme ve karşılaştırma ve işi verme</span><span class="sxs-lookup"><span data-stu-id="baea2-103">Enter and compare RFQ bids, and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="baea2-104">Bu prosedürde bir teklif talebine (RFQ) yanıtların nasıl girileceği, aldığınız tekliflerin nasıl puanlandırılacağı ve karşılaştırılacağı ve ardından sözleşme için teklif gönderen satıcılardan birinin nasıl seçileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="baea2-104">This procedure shows how to enter replies to a request for quotation (RFQ), score and compare bids that you receive, and then award the contract to one of the vendors who submitted bids.</span></span> <span data-ttu-id="baea2-105">Bu yordamı **USMF** demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-105">You can use this procedure in the **USMF** demo data company.</span></span>

<span data-ttu-id="baea2-106">Bu yordama başlamadan önce, en az iki satıcıya gönderilmiş ve iki satır içeren bir RFQ'ya sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="baea2-106">Before you start this procedure, you must have an RFQ that has two lines, and that has been sent to at least two vendors.</span></span> <span data-ttu-id="baea2-107">Bu RFQ'yu oluşturmak için [Teklif talebi oluşturma](create-request-quotation.md) yordamını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="baea2-107">To create this RFQ, complete the [Create a request for quotation](create-request-quotation.md) procedure.</span></span> <span data-ttu-id="baea2-108">Bu prosedürü tamamlamadan önce puanlama ölçütlerini belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="baea2-108">Scoring criteria must also be set up before you can complete this procedure.</span></span>

<span data-ttu-id="baea2-109">Teklifi satıcı veya tedarik uzmanı olarak girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-109">You can enter the bid as either a vendor or a procurement professional.</span></span> <span data-ttu-id="baea2-110">Daha fazla bilgi için bkz. [Satıcı işbirliğini ayarlama ve sürdürme](../set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="baea2-110">For more information, see [Set up and maintain vendor collaboration](../set-up-maintain-vendor-collaboration.md).</span></span>

## <a name="enter-a-reply-as-a-vendor"></a><span data-ttu-id="baea2-111">Bir satıcı olarak yanıt girme</span><span class="sxs-lookup"><span data-stu-id="baea2-111">Enter a reply as a vendor</span></span>

1. <span data-ttu-id="baea2-112">Panoda, **Satıcı teklifi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-112">On the dashboard, select **Vendor bidding**.</span></span>
2. <span data-ttu-id="baea2-113">**Yeni teklif davetleri** listesinde, henüz gönderilmiş bir RFQ bulun.</span><span class="sxs-lookup"><span data-stu-id="baea2-113">In the **New bid invitations** list, find an RFQ that was just sent.</span></span> <span data-ttu-id="baea2-114">Neyin istenmiş olduğunu incelemek için RFQ'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-114">Select the RFQ to review what was requested.</span></span>
3. <span data-ttu-id="baea2-115">Eklenmiş ekleri gözden geçirmek için **RFQ ekleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-115">Select **RFQ attachments** to review any attachments that have been added.</span></span>
4. <span data-ttu-id="baea2-116">Alanları düzenlenebilir yapmak için **Teklif**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-116">Select **Bid** to make the fields editable.</span></span> <span data-ttu-id="baea2-117">**Teklif ilerlemesi** alanının **Satıcı güncelleştiriliyor**olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="baea2-117">Notice that the **Bid progress** field is set to **Vendor is updating**.</span></span>
5. <span data-ttu-id="baea2-118">Başlık ve satırlara, teklif yanıtındaki değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="baea2-118">On the header and lines, enter the values from the bid reply.</span></span>
6. <span data-ttu-id="baea2-119">Teklife ek eklenmesi gerekiyorsa, **Teklif ekleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-119">If any attachments should be added to the bid, select **Bid attachments**.</span></span>
7. <span data-ttu-id="baea2-120">Herhangi bir belge gerekip gerekmediğini görmek için **Teklif kılavuzu maddeleri** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-120">Select the **Bidding guiding items** FastTab to view whether any documents are required.</span></span>
8. <span data-ttu-id="baea2-121">RFQ'nun değiştirilip değiştirilmediğini görmek için **Değişiklikler** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-121">Select the **Amendments** FastTab to view whether the RFQ has been amended.</span></span>
9. <span data-ttu-id="baea2-122">**Soru formu** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-122">Select the **Questionnaire** FastTab.</span></span> <span data-ttu-id="baea2-123">Burada görünen soru formlarının yanıtlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="baea2-123">Any questionnaires that appear here must be answered.</span></span>
10. <span data-ttu-id="baea2-124">Satırla ilgili genişletilmiş bilgileri görüntülemek için **Satır ayrıntıları** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-124">Select the **Line details** FastTab to view extended information about the line.</span></span>
11. <span data-ttu-id="baea2-125">Girilmiş değerleri orijinal RFQ değerlerine sıfırlamanız gerekiyorsa **RFQ'dan Sıfırla** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="baea2-125">Select **Reset from RFQ** only if you must reset the values that have been entered to the original RFQ values.</span></span>
12. <span data-ttu-id="baea2-126">Teklifi istediğiniz zaman kaydedebilir ve sona erme tarihi ve saatinin geçmemiş olması koşuluyla daha sonra ek işlem yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-126">You can save the bid at any time and do additional processing later, provided that the expiration date and time haven't passed.</span></span> <span data-ttu-id="baea2-127">Bu durumda, teklifi **Satıcı teklifi** çalışma alanındaki **Devam eden teklifler** listesinde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-127">In this case, you can find the bid in the **Bids in progress** list in the **Vendor bidding** workspace.</span></span>
13. <span data-ttu-id="baea2-128">Teklif gönderilmeye hazır olduğunda **Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-128">When the bid is ready to be sent, select **Submit**.</span></span> <span data-ttu-id="baea2-129">Teklif vermek istemiyorsanız **Reddet**'i seçin</span><span class="sxs-lookup"><span data-stu-id="baea2-129">If you don't want to bid, select **Decline**.</span></span>

    <span data-ttu-id="baea2-130">Gönderilen teklifler **Satıcı teklifi** çalışma alanındaki **Gönderilen teklifler** listesinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="baea2-130">Submitted bids are available in the **Submitted bids** list in the **Vendor bidding** workspace.</span></span>

14. <span data-ttu-id="baea2-131">Teklif gönderildikten sonra, zaman aşımı tarihi ve saatinden önce istediğiniz zaman geri çağırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-131">After the bid is submitted, you can recall it at any time before the expiration date and time.</span></span> <span data-ttu-id="baea2-132">Bir teklif geri çağrıldığında gönderilmiş olarak değerlendirilmez.</span><span class="sxs-lookup"><span data-stu-id="baea2-132">Note that when a bid is recalled, it isn't treated as submitted.</span></span>

    <span data-ttu-id="baea2-133">Teklif tedarik departmanı tarafından kabul edildiğinde veya reddedildiğinde **Satıcı teklifi** çalışma alanındaki **Kazanılan teklifler** veya **Kaybedilen teklifler** listesinde görünür.</span><span class="sxs-lookup"><span data-stu-id="baea2-133">When the bid is accepted or rejected by the procurement department, it appears in either the **Awarded bids** or **Lost bids** list in the **Vendor bidding** workspace.</span></span>

## <a name="enter-a-reply-from-a-vendor-as-a-procurement-professional"></a><span data-ttu-id="baea2-134">Tedarik uzmanı olarak bir satıcıdan gelen yanıtı girme</span><span class="sxs-lookup"><span data-stu-id="baea2-134">Enter a reply from a vendor as a procurement professional</span></span>

1. <span data-ttu-id="baea2-135">Satıcı tekliflerini düzenleme izninin ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="baea2-135">Make sure that the permission to edit vendor bids is set up.</span></span> <span data-ttu-id="baea2-136">**Tedarik ve kaynak atama \> Kurulum \> Tedarik ve kaynak atama parametrelerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="baea2-136">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span> <span data-ttu-id="baea2-137">**Teklif talebi** sekmesinde, **Satınalmacı satıcı teklifini düzenleyebilir** seçeneğini **Evet**olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="baea2-137">On the **Request for quotations** tab, set the **Purchaser can edit vendors bid** option to **Yes**.</span></span>
2. <span data-ttu-id="baea2-138">**Tedarik ve kaynak atama \> Teklif talepleri \> Tüm teklif talepleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="baea2-138">Go to **Procurement and sourcing \> Requests for quotations \> All requests for quotations**.</span></span>
3. <span data-ttu-id="baea2-139">**Gönderildi** durumuna sahip bir RFQ seçin ve **Teklif talebi olayı** alanındaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-139">Select an RFQ that has a status of **Sent**, and then select the link in the **Request for quotation case** field.</span></span>
4. <span data-ttu-id="baea2-140">**Yanıtları yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-140">Select **Manage replies**.</span></span> <span data-ttu-id="baea2-141">Beliren sayfa, teklife davet edilen her satıcı için bir RFQ gösterir.</span><span class="sxs-lookup"><span data-stu-id="baea2-141">The page that appears shows an RFQ for each vendor that was invited to bid.</span></span>
5. <span data-ttu-id="baea2-142">Yanıtmamış bir RFQ seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-142">Select an RFQ that hasn't been replied to.</span></span> <span data-ttu-id="baea2-143">( **Yanıt ilerlemesi** alanı **Başlatılmadı** olarak ayarlanmalıdır.)</span><span class="sxs-lookup"><span data-stu-id="baea2-143">(The **Reply progress** field should be set to **Not started**.)</span></span>
6. <span data-ttu-id="baea2-144">**Düzenle \> RFQ yanıtını düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-144">Select **Edit \> Edit RFQ reply**.</span></span>

    <span data-ttu-id="baea2-145">**RFQ yanıtı** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="baea2-145">The **RFQ reply** page appears.</span></span> <span data-ttu-id="baea2-146">Tedarik uzmanı olarak, şimdi satıcı adına yanıt girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-146">As a procurement professional, you can now enter the reply on behalf of the vendor.</span></span> <span data-ttu-id="baea2-147">**Teklif ilerlemesi** alanının **Satınalmacı güncelleştiriliyor** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="baea2-147">Notice that the **Bid progress** field is set to **Purchaser is updating**.</span></span>

7. <span data-ttu-id="baea2-148">Teklif verilerini girin.</span><span class="sxs-lookup"><span data-stu-id="baea2-148">Enter the bid data.</span></span> <span data-ttu-id="baea2-149">Tamamladıktan sonra **Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-149">When you've finished, select **Submit**.</span></span>

## <a name="score-the-bids"></a><span data-ttu-id="baea2-150">Teklifleri puanlama</span><span class="sxs-lookup"><span data-stu-id="baea2-150">Score the bids</span></span>

1. <span data-ttu-id="baea2-151">**Tüm teklif talepleri** sayfasında, yanıtlarını puanlamak istediğiniz RFQ olayını seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-151">On the **All requests for quotations** page, select the RFQ case that you want to score replies for.</span></span>
2. <span data-ttu-id="baea2-152">**Yanıtları yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-152">Select **Manage replies**.</span></span>
3. <span data-ttu-id="baea2-153">Puanlanacak yanıtı seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-153">Select the reply to score.</span></span>
4. <span data-ttu-id="baea2-154">Teklif için puanı görüntüleyebilmek üzere **Başlık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-154">Select **Header** so that you can view the scoring for the bid.</span></span>
5. <span data-ttu-id="baea2-155">**Teklif puanı** hızlı sekmesinde **Puan** alanına, bir puanlama ölçütü için bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="baea2-155">On the **Bid scoring** FastTab, enter a number in the **Score** field for one of the scoring criteria.</span></span>

    <span data-ttu-id="baea2-156">Fare imlecini bir puanlama ölçütünün üzerine getirdiğinizde, puanınızın yer alması gereken aralığı gösteren bir araç ipucu açılır.</span><span class="sxs-lookup"><span data-stu-id="baea2-156">If you hover over a scoring criterion, a tooltip shows the range that the score must be within.</span></span> <span data-ttu-id="baea2-157">Bu demoda tüm puanlama ölçütleri için 1 ile 5 arasında bir sayı girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-157">In this demo, you can enter a number between 1 and 5 for any of the scoring criteria.</span></span>

6. <span data-ttu-id="baea2-158">Başka bir puan ölçütü için 5. adımı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="baea2-158">Repeat step 5 for another scoring criterion.</span></span>
7. <span data-ttu-id="baea2-159">RFQ olayı, satıcılara gönderilen bir soru formuna sahipse, satıcıların yanıtlarını **Soru formları** hızlı sekmesinden girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-159">If the RFQ case has a questionnaire that was sent to the vendors, you can enter the vendor responses on the **Questionnaires** FastTab.</span></span>
8. <span data-ttu-id="baea2-160">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="baea2-160">Close the page.</span></span>
9. <span data-ttu-id="baea2-161">Tüm diğer teklifler için 1 ile 8 arasındaki adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="baea2-161">Repeat steps 1 through 8 for all the other bids.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="baea2-162">Teklifleri karşılaştırma</span><span class="sxs-lookup"><span data-stu-id="baea2-162">Compare the replies</span></span>

1. <span data-ttu-id="baea2-163">Eylem Bölmesi'ndeki **Genel** sekmesinde, **Yanıtları karşılaştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-163">On the Action Pane, on the **General** tab, select **Compare replies**.</span></span>
2. <span data-ttu-id="baea2-164">**Sıralama** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="baea2-164">In the **Rank** field, enter a number.</span></span>

    <span data-ttu-id="baea2-165">Bu sayfada başlık ve satır bilgileriyle birlikte teklifler ve başlık seviyesinde toplam puan gösterilir.</span><span class="sxs-lookup"><span data-stu-id="baea2-165">This page shows the bids, together with the header and line information, and also the total score at the header level.</span></span> <span data-ttu-id="baea2-166">Satırları, karşılaştırabilir satırlar birbirinin yanına gelecek şekilde ızgarada sıralayarak karşılaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-166">You can compare the lines by sorting the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="baea2-167">Aşağıdaki bilgiler de eklenir:</span><span class="sxs-lookup"><span data-stu-id="baea2-167">The following information is also included:</span></span>

    - <span data-ttu-id="baea2-168">**Miktar**: Satıcı tarafından teklif edilen miktar.</span><span class="sxs-lookup"><span data-stu-id="baea2-168">**Quantity** – The quantity that the vendor quoted.</span></span> <span data-ttu-id="baea2-169">Bu miktar, RFQ'da belirtilen miktara eşit olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="baea2-169">This quantity might not equal the quantity that is specified in the RFQ.</span></span>
    - <span data-ttu-id="baea2-170">**Net tutar**: Satıcı tarafından satırda belirtilen maddeler için iskontolar çıkarıldıktan sonra teklif edilen fiyat.</span><span class="sxs-lookup"><span data-stu-id="baea2-170">**Net amount** – The price that the vendor quoted for the items on the line, minus any discounts.</span></span>
    - <span data-ttu-id="baea2-171">**Sapma**: Teklif başlığında veya satırında belirtilen teslimat tarihinin RFQ başlığında veya satırında talep edilen teslimat tarihine göre, gün cinsinden sapma miktarı.</span><span class="sxs-lookup"><span data-stu-id="baea2-171">**Deviation** – The number of days by which the delivery date on the bid header or line differs from the requested delivery date on the RFQ header or line.</span></span> <span data-ttu-id="baea2-172">Her bir teklif için bira aralık girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-172">You can enter a rank for each bid.</span></span>

3. <span data-ttu-id="baea2-173">Sıralamak istediğiniz diğer tekliflerin başlık satırlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-173">Select the header line for the other bid that you want to rank.</span></span>
4. <span data-ttu-id="baea2-174">**Sıralama** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="baea2-174">In the **Rank** field, enter a number.</span></span>
5. <span data-ttu-id="baea2-175">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-175">Select **Save**.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="baea2-176">Bir teklifi reddetme</span><span class="sxs-lookup"><span data-stu-id="baea2-176">Reject a bid</span></span>

1. <span data-ttu-id="baea2-177">Reddetmek istediğiniz teklifin başlık satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-177">Select the header line for the bid that you want to reject.</span></span>

    <span data-ttu-id="baea2-178">Aynı anda sadece bir teklifi veya bir teklifteki satırları kabul edebilir, reddedebilir veya iade edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-178">You can accept, reject, or return only one bid or the lines on only one bid at a time.</span></span>

2. <span data-ttu-id="baea2-179">**İşaretle** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-179">Select the **Mark** check box.</span></span>

    <span data-ttu-id="baea2-180">Teklif başlığındaki **İşaretle** onay kutusunu seçerseniz tüm satırlar işaretlenecektir.</span><span class="sxs-lookup"><span data-stu-id="baea2-180">If you select the **Mark** check box on the header of the bid, all the lines are also marked.</span></span> <span data-ttu-id="baea2-181">Teklifteki bazı satırları reddetmek veya kabul etmek için, yalnızca bu satırları işaretleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-181">To reject or accept only some of the lines on the bid, you can mark just those lines.</span></span> <span data-ttu-id="baea2-182">Ek olarak, bir RFQ'daki bazı satırlar için bir satıcının teklifini kabul edebilir ve diğer RFQ satırlarını farklı bir satıcıya verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-182">Additionally, you can accept one vendor's bid for some lines of an RFQ and then award other RFQ lines to a different vendor.</span></span> <span data-ttu-id="baea2-183">Ancak, bir seferde tek bir teklif yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="baea2-183">However, you must do one bid at a time.</span></span>

    <span data-ttu-id="baea2-184">Başka satırlar varsa, orijinal teklif satırını veya başka bir satırı kabule edebilirsiniz, her ikisini aynı anda kabul edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-184">If alternate lines are present, you can accept either the original bid line or its alternate, but not both.</span></span>

3. <span data-ttu-id="baea2-185">**Reddet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-185">Select **Reject**.</span></span>
4. <span data-ttu-id="baea2-186">**Parametreleri**seçin ve ardından **Reddetme nedeni** alanında, teklifi reddetme nedeninizi girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-186">Select **Parameters**, and then, in the **Reason reject** field, enter or select your reason for rejecting the bid.</span></span>

    <span data-ttu-id="baea2-187">Neden yanıtta saklanır.</span><span class="sxs-lookup"><span data-stu-id="baea2-187">The reason is stored in the reply.</span></span>

5. <span data-ttu-id="baea2-188">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-188">Select **OK**.</span></span>
6. <span data-ttu-id="baea2-189">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-189">Select **OK**.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="baea2-190">Bir teklifi kabul etme</span><span class="sxs-lookup"><span data-stu-id="baea2-190">Accept a bid</span></span>

1. <span data-ttu-id="baea2-191">Kabul etmek istediğiniz teklifi seçin ve ardından **Teklif talebi** alanındaki bağlantıyı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="baea2-191">Select the bid to accept, and then select the link in the **Request for quotation** field.</span></span>

    <span data-ttu-id="baea2-192">**Teklif talebi yanıtlarını karşılaştır** sayfasında iseniz, vurgulanmış teklif sistemin Kabul etme eylemi sırasında göz önünde bulundurduğu tekliftir.</span><span class="sxs-lookup"><span data-stu-id="baea2-192">If you're on the **Compare request for quotation replies** page, the highlighted bid that has focus is the bid that the system will consider during the Accept action.</span></span> <span data-ttu-id="baea2-193">Bir seferde yalnızca bir teklifin satırlarını kabul edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-193">You can accept lines from only one bid at a time.</span></span>

2. <span data-ttu-id="baea2-194">Eylem Bölmesinde, **Yanıtla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-194">On the Action Pane, select **Reply**.</span></span>
3. <span data-ttu-id="baea2-195">**Kabul et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-195">Select **Accept**.</span></span>

    <span data-ttu-id="baea2-196">Yalnızca belirli satırları işaretlediyseniz, Kabul et eylemi yalnızca bu satırları dahil eder.</span><span class="sxs-lookup"><span data-stu-id="baea2-196">If you marked only specific lines, the Accept action will include only those lines.</span></span> <span data-ttu-id="baea2-197">Teklifteki tüm satırları kabul etmek isterseniz, satırları işaretlemenize gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="baea2-197">If you want to accept all the lines on the bid, you don't have to mark the lines.</span></span>

4. <span data-ttu-id="baea2-198">**Parametreler**'i seçin ve ardından **Kabul etme nedeni** alanında, teklifi kabul etme nedeninizi girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-198">Select **Parameters**, and then, in the **Reason accept** field, enter or select your reason for accepting the bid.</span></span>

    <span data-ttu-id="baea2-199">Neden teklifte saklanır.</span><span class="sxs-lookup"><span data-stu-id="baea2-199">The reason is stored in the bid.</span></span>

5. <span data-ttu-id="baea2-200">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-200">Select **OK**.</span></span>
6. <span data-ttu-id="baea2-201">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-201">Select **OK**.</span></span>

    <span data-ttu-id="baea2-202">**Tamam**'ı seçtiğinizde RFQ kabulüne dahil edilen satırlara dayalı olarak bir satın alma emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="baea2-202">When you select **OK**, a purchase order is generated based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="baea2-203">Henüz işlenmemiş (kabul edilmiş, reddedilmiş veya iade edilmiş) başka teklifler varsa sistem bunları reddetmeniz için bir mesaj görüntüler.</span><span class="sxs-lookup"><span data-stu-id="baea2-203">If there are other bids that haven't been processed (accepted, rejected, or returned), the system prompts you to reject them.</span></span>

## <a name="view-the-purchase-order-that-is-generated"></a><span data-ttu-id="baea2-204">Oluşturulmuş bir satın alma emrini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="baea2-204">View the purchase order that is generated</span></span>

- <span data-ttu-id="baea2-205">Eylem Bölmesi'ndeki **Genel** sekmesinde, **Satınalma emri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="baea2-205">On the Action Pane, on the **General** tab, select **Purchase order**.</span></span>

    <span data-ttu-id="baea2-206">Görüntülenen sayfada teklifi kabul ettiğinizde oluşturulmuş olan satın alma emrini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="baea2-206">The page that appears shows the purchase order that was generated when you accepted the bid.</span></span>
