---
title: RFQ kullanan bir talep oluşturma
description: Bu konu, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini açıklar.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6083afe0e2bfafd337d572863a198330e8cb6cc8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812146"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="a8d49-103">RFQ kullanan bir talep oluşturma</span><span class="sxs-lookup"><span data-stu-id="a8d49-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8d49-104">Bu konu, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="a8d49-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="a8d49-105">Bu kılavuzda gösterilen örnek USMF demo verileri şirketinde kullanılabilir ve tüm adımları tamamlamak için bir Yönetici olarak oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a8d49-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="a8d49-106">Bu kılavuzdaki görevler genellikle tedarik profesyonelleri tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="a8d49-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="a8d49-107">Talep oluşturun</span><span class="sxs-lookup"><span data-stu-id="a8d49-107">Create a requisition</span></span>
1. <span data-ttu-id="a8d49-108">Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Satınalma talepleri > Tarafımdan hazırlanan satınalma talepleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="a8d49-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-109">Select **New**.</span></span>
3. <span data-ttu-id="a8d49-110">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a8d49-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="a8d49-111">**Talep edilen tarih** alanına, bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="a8d49-112">**Muhasebe tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="a8d49-113">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-113">Select **OK**.</span></span>
7. <span data-ttu-id="a8d49-114">**Neden** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="a8d49-115">**Satır ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-115">Select **Add line**.</span></span>
9. <span data-ttu-id="a8d49-116">**Tedarik kategorisi** alanında ağaç içinde bir kategori seçin ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8d49-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="a8d49-117">**Ürün adı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a8d49-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="a8d49-118">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="a8d49-119">**Birim** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="a8d49-120">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-120">Select **Save**.</span></span>
14. <span data-ttu-id="a8d49-121">Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="a8d49-122">**Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-122">Select **Submit**.</span></span>
16. <span data-ttu-id="a8d49-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a8d49-123">Close the page.</span></span>
17. <span data-ttu-id="a8d49-124">**Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="a8d49-125">İş akışı görevini yeniden atayın</span><span class="sxs-lookup"><span data-stu-id="a8d49-125">Reassign a workflow task</span></span>
<span data-ttu-id="a8d49-126">Sonraki görev satıcılardan ürün için teklifleri almak için bir RFQ oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="a8d49-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="a8d49-127">USMF demo verilerinde talep iş akışı, bir satıcı seçilmediğinde veya bir satır için birim fiyat 0 olduğunda belirli bir çalışana bir RFQ oluşturması için bir görevin atandığı bir kural ile ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="a8d49-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="a8d49-128">Bu kılavuz ile devam etmek için bu görevi başka bir kullanıcıya (kendinize) yeniden atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a8d49-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="a8d49-129">Bunu yalnızca bir Yönetici olarak oturum açtıysanız yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d49-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="a8d49-130">Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="a8d49-131">**Geçmişi görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-131">Select **View history**.</span></span>
3. <span data-ttu-id="a8d49-132">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-132">Refresh the page.</span></span>
4. <span data-ttu-id="a8d49-133">**İzleme ayrıntıları**  bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="a8d49-134">Ağaçta, "Satır iş akışı etkinleştirildi" ile başlayan satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="a8d49-135">**İş akış ayrıntılarını görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="a8d49-136">**İş öğeleri**  bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="a8d49-137">**Yeniden ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="a8d49-138">**Kullanıcı** alanında **Yönetici**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="a8d49-139">**Yeniden ata**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="a8d49-140">İki sayfayı da kapatın.</span><span class="sxs-lookup"><span data-stu-id="a8d49-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="a8d49-141">RFQ oluşturun</span><span class="sxs-lookup"><span data-stu-id="a8d49-141">Create an RFQ</span></span>

1. <span data-ttu-id="a8d49-142">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-142">Refresh the page.</span></span>
2. <span data-ttu-id="a8d49-143">**Teklif talebi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="a8d49-144">**Satın alma tüzel kişiliği** alanında **USMF**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="a8d49-145">Talep satırında bulunan aynı yasal varlığı seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d49-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="a8d49-146">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-146">In the list, mark the selected row.</span></span> <span data-ttu-id="a8d49-147">Satınalma talebinde birden fazla satırınız varsa RFQ'ya eklemek istediğiniz tüm satırları seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="a8d49-148">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-148">Select **OK**.</span></span>
6. <span data-ttu-id="a8d49-149">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-149">Refresh the page.</span></span>
7. <span data-ttu-id="a8d49-150">Bilgi kutusunun açık olduğundan emin olun ve **İlgili belgeler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="a8d49-151">Yeni oluşturulan RFQ'yu açmak için **Teklif talebi** alanındaki bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="a8d49-152">**Başlık** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-152">Select **Header**.</span></span>
10. <span data-ttu-id="a8d49-153">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-153">Select **Add**.</span></span>
11. <span data-ttu-id="a8d49-154">**Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="a8d49-155">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-155">Select **Add**.</span></span>
13. <span data-ttu-id="a8d49-156">**Satıcı hesabı** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="a8d49-157">**Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-157">Select **Send**.</span></span>
15. <span data-ttu-id="a8d49-158">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-158">Select **OK**.</span></span>
16. <span data-ttu-id="a8d49-159">**Yanıt gir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="a8d49-160">Eylem Bölmesinde, **Yanıtla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="a8d49-161">**Verileri yanıta kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="a8d49-162">Bu, RFQ'dan yanıta miktar ve tarihler gibi verileri kopyalar.</span><span class="sxs-lookup"><span data-stu-id="a8d49-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="a8d49-163">**Birim fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="a8d49-164">Bu, satıcıdan aldığınız fiyattır.</span><span class="sxs-lookup"><span data-stu-id="a8d49-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="a8d49-165">Ayrıca satıcıdan ek bilgiler girmek de isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a8d49-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="a8d49-166">**Kabul et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-166">Select **Accept**.</span></span>
21. <span data-ttu-id="a8d49-167">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="a8d49-168">Satıcı ve fiyatın talebe aktarılmış olduğunu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="a8d49-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="a8d49-169">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a8d49-169">Close the page.</span></span>
2. <span data-ttu-id="a8d49-170">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-170">Select **Lines**.</span></span>
3. <span data-ttu-id="a8d49-171">**İlgili bilgiler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-171">Select **Related information**.</span></span>
4. <span data-ttu-id="a8d49-172">**Satınalma talebi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="a8d49-173">RFQ'ya transfer edilen satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="a8d49-174">Fiyatın ve satıcının talebe kopyalandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a8d49-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="a8d49-175">Açılır iletişim kutusunu açmak için **İş akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="a8d49-176">Tamamlandı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-176">Select Complete.</span></span>
8. <span data-ttu-id="a8d49-177">Sayfayı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-177">Select the page.</span></span>
9. <span data-ttu-id="a8d49-178">Tamamlandı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a8d49-178">Select Complete.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]