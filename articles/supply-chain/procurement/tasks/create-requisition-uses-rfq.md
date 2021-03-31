---
title: RFQ kullanan bir talep oluşturma
description: Bu konu, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini açıklar.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e67dafd02a3b2a38832d8a4f0e9809adffcbb80
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211850"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="57bf2-103">RFQ kullanan bir talep oluşturma</span><span class="sxs-lookup"><span data-stu-id="57bf2-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57bf2-104">Bu konu, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="57bf2-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="57bf2-105">Bu kılavuzda gösterilen örnek USMF demo verileri şirketinde kullanılabilir ve tüm adımları tamamlamak için bir Yönetici olarak oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="57bf2-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="57bf2-106">Bu kılavuzdaki görevler genellikle tedarik profesyonelleri tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="57bf2-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="57bf2-107">Talep oluşturun</span><span class="sxs-lookup"><span data-stu-id="57bf2-107">Create a requisition</span></span>
1. <span data-ttu-id="57bf2-108">Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Satınalma talepleri > Tarafımdan hazırlanan satınalma talepleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="57bf2-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-109">Select **New**.</span></span>
3. <span data-ttu-id="57bf2-110">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="57bf2-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="57bf2-111">**Talep edilen tarih** alanına, bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="57bf2-112">**Muhasebe tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="57bf2-113">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-113">Select **OK**.</span></span>
7. <span data-ttu-id="57bf2-114">**Neden** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="57bf2-115">**Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-115">Select **Add line**.</span></span>
9. <span data-ttu-id="57bf2-116">**Tedarik kategorisi** alanında ağaç içinde bir kategori seçin ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="57bf2-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="57bf2-117">**Ürün adı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="57bf2-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="57bf2-118">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="57bf2-119">**Birim** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="57bf2-120">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-120">Select **Save**.</span></span>
14. <span data-ttu-id="57bf2-121">Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="57bf2-122">**Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-122">Select **Submit**.</span></span>
16. <span data-ttu-id="57bf2-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="57bf2-123">Close the page.</span></span>
17. <span data-ttu-id="57bf2-124">**Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="57bf2-125">İş akışı görevini yeniden atayın</span><span class="sxs-lookup"><span data-stu-id="57bf2-125">Reassign a workflow task</span></span>
<span data-ttu-id="57bf2-126">Sonraki görev satıcılardan ürün için teklifleri almak için bir RFQ oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="57bf2-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="57bf2-127">USMF demo verilerinde talep iş akışı, bir satıcı seçilmediğinde veya bir satır için birim fiyat 0 olduğunda belirli bir çalışana bir RFQ oluşturması için bir görevin atandığı bir kural ile ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="57bf2-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="57bf2-128">Bu kılavuz ile devam etmek için bu görevi başka bir kullanıcıya (kendinize) yeniden atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="57bf2-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="57bf2-129">Bunu yalnızca bir Yönetici olarak oturum açtıysanız yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57bf2-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="57bf2-130">Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="57bf2-131">**Geçmişi görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-131">Select **View history**.</span></span>
3. <span data-ttu-id="57bf2-132">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-132">Refresh the page.</span></span>
4. <span data-ttu-id="57bf2-133">**İzleme ayrıntıları**  bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="57bf2-134">Ağaçta, "Satır iş akışı etkinleştirildi" ile başlayan satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="57bf2-135">**İş akış ayrıntılarını görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="57bf2-136">**İş öğeleri**  bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="57bf2-137">**Yeniden ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="57bf2-138">**Kullanıcı** alanında **Yönetici**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="57bf2-139">**Yeniden ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="57bf2-140">İki sayfayı da kapatın.</span><span class="sxs-lookup"><span data-stu-id="57bf2-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="57bf2-141">RFQ oluşturun</span><span class="sxs-lookup"><span data-stu-id="57bf2-141">Create an RFQ</span></span>

1. <span data-ttu-id="57bf2-142">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-142">Refresh the page.</span></span>
2. <span data-ttu-id="57bf2-143">**Teklif talebi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="57bf2-144">**Satın alma tüzel kişiliği** alanında **USMF**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="57bf2-145">Talep satırında bulunan aynı yasal varlığı seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="57bf2-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="57bf2-146">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-146">In the list, mark the selected row.</span></span> <span data-ttu-id="57bf2-147">Satınalma talebinde birden fazla satırınız varsa RFQ'ya eklemek istediğiniz tüm satırları seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="57bf2-148">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-148">Select **OK**.</span></span>
6. <span data-ttu-id="57bf2-149">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-149">Refresh the page.</span></span>
7. <span data-ttu-id="57bf2-150">Bilgi kutusunun açık olduğundan emin olun ve **İlgili belgeler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="57bf2-151">Yeni oluşturulan RFQ'yu açmak için **Teklif talebi** alanındaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="57bf2-152">**Başlık** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-152">Select **Header**.</span></span>
10. <span data-ttu-id="57bf2-153">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-153">Select **Add**.</span></span>
11. <span data-ttu-id="57bf2-154">**Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="57bf2-155">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-155">Select **Add**.</span></span>
13. <span data-ttu-id="57bf2-156">**Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="57bf2-157">**Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-157">Select **Send**.</span></span>
15. <span data-ttu-id="57bf2-158">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-158">Select **OK**.</span></span>
16. <span data-ttu-id="57bf2-159">**Yanıt gir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="57bf2-160">Eylem Bölmesinde, **Yanıtla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="57bf2-161">**Verileri yanıta kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="57bf2-162">Bu, RFQ'dan yanıta miktar ve tarihler gibi verileri kopyalar.</span><span class="sxs-lookup"><span data-stu-id="57bf2-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="57bf2-163">**Birim fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="57bf2-164">Bu, satıcıdan aldığınız fiyattır.</span><span class="sxs-lookup"><span data-stu-id="57bf2-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="57bf2-165">Ayrıca satıcıdan ek bilgiler girmek de isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57bf2-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="57bf2-166">**Kabul et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-166">Select **Accept**.</span></span>
21. <span data-ttu-id="57bf2-167">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="57bf2-168">Satıcı ve fiyatın talebe aktarılmış olduğunu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="57bf2-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="57bf2-169">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="57bf2-169">Close the page.</span></span>
2. <span data-ttu-id="57bf2-170">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-170">Select **Lines**.</span></span>
3. <span data-ttu-id="57bf2-171">**İlgili bilgiler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-171">Select **Related information**.</span></span>
4. <span data-ttu-id="57bf2-172">**Satınalma talebi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="57bf2-173">RFQ'ya transfer edilen satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="57bf2-174">Fiyatın ve satıcının talebe kopyalandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="57bf2-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="57bf2-175">Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="57bf2-176">Tamamlandı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-176">Select Complete.</span></span>
8. <span data-ttu-id="57bf2-177">Sayfayı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-177">Select the page.</span></span>
9. <span data-ttu-id="57bf2-178">Tamamlandı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57bf2-178">Select Complete.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]