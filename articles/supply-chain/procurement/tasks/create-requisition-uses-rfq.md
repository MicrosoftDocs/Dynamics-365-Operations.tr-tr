---
title: RFQ kullanan bir talep oluşturma
description: Bu kılavuz, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini gösterir.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547418"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="36b87-103">RFQ kullanan bir talep oluşturma</span><span class="sxs-lookup"><span data-stu-id="36b87-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36b87-104">Bu kılavuz, bir RFQ işleminden satınalma talebine fiyat ve satıcı bilgilerinin nasıl ekleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="36b87-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="36b87-105">Bu kılavuzda gösterilen örnek USMF demo verileri şirketinde kullanılabilir ve tüm adımları tamamlamak için bir Yönetici olarak oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="36b87-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="36b87-106">Bu kılavuzdaki görevler genellikle tedarik profesyonelleri tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="36b87-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="36b87-107">Talep oluşturun</span><span class="sxs-lookup"><span data-stu-id="36b87-107">Create a requisition</span></span>
1. <span data-ttu-id="36b87-108">Tedarik ve kaynak Hizmeti'nden > Satınalma talepleri > Satınalma talepleri benim tarafından hazırlandı'ya git.</span><span class="sxs-lookup"><span data-stu-id="36b87-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="36b87-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-109">Click New.</span></span>
3. <span data-ttu-id="36b87-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="36b87-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="36b87-111">Talep edilen tarih alanında, bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="36b87-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="36b87-112">Muhasebe tarihi alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="36b87-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="36b87-113">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-113">Click OK.</span></span>
7. <span data-ttu-id="36b87-114">Neden alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="36b87-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="36b87-115">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-115">Click Add line.</span></span>
9. <span data-ttu-id="36b87-116">Tedarik kategorisi alanında ağaç içinde bir kategori seçin ve Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="36b87-117">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="36b87-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="36b87-118">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="36b87-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="36b87-119">Birim alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="36b87-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="36b87-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-120">Click Save.</span></span>
14. <span data-ttu-id="36b87-121">İletişim kutusu formunu açmak için İş akışı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="36b87-122">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-122">Click Submit.</span></span>
16. <span data-ttu-id="36b87-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-123">Close the page.</span></span>
17. <span data-ttu-id="36b87-124">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="36b87-125">İş akışı görevini yeniden atayın</span><span class="sxs-lookup"><span data-stu-id="36b87-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="36b87-126">Sonraki görev satıcılardan ürün için teklifleri almak için bir RFQ oluşturmaktır.</span><span class="sxs-lookup"><span data-stu-id="36b87-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="36b87-127">USMF demo verilerinde talep iş akışı, bir satıcı seçilmediğinde veya bir satır için birim fiyat 0 olduğunda belirli bir çalışana bir RFQ oluşturması için bir görevin atandığı bir kural ile ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="36b87-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="36b87-128">Bu kılavuz ile devam etmek için bu görevi başka bir kullanıcıya (kendinize) yeniden atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="36b87-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="36b87-129">Bunu yalnızca bir Yönetici olarak oturum açtıysanız yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36b87-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="36b87-130">İletişim kutusu formunu açmak için İş akışı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="36b87-131">Geçmişi görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-131">Click View history.</span></span>
3. <span data-ttu-id="36b87-132">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="36b87-132">Refresh the page.</span></span>
4. <span data-ttu-id="36b87-133">İzleme ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="36b87-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="36b87-134">Ağaç içinde, "Satır maddesi iş akışı etkinleştirildi" ile başlayan satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="36b87-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="36b87-135">İş akış ayrıntılarını görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-135">Click View workflow details.</span></span>
7. <span data-ttu-id="36b87-136">İş öğeleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="36b87-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="36b87-137">Yeniden Ata'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-137">Click Reassign.</span></span>
9. <span data-ttu-id="36b87-138">Kullanıcı alanında Yönetici'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36b87-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="36b87-139">Yeniden Ata'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-139">Click Reassign.</span></span>
11. <span data-ttu-id="36b87-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-140">Close the page.</span></span>
12. <span data-ttu-id="36b87-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="36b87-142">RFQ oluşturun</span><span class="sxs-lookup"><span data-stu-id="36b87-142">Create an RFQ</span></span>
1. <span data-ttu-id="36b87-143">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="36b87-143">Refresh the page.</span></span>
2. <span data-ttu-id="36b87-144">Teklif talebi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="36b87-145">Satın alma tüzel kişiliği alanında USMF'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="36b87-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="36b87-146">Talep satırında bulunan aynı yasal varlığı seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="36b87-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="36b87-147">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="36b87-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="36b87-148">Satınalma talebinde birden fazla satırınız varsa RFQ'ya eklemek istediğiniz tüm satırları seçin.</span><span class="sxs-lookup"><span data-stu-id="36b87-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="36b87-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-149">Click OK.</span></span>
6. <span data-ttu-id="36b87-150">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="36b87-150">Refresh the page.</span></span>
7. <span data-ttu-id="36b87-151">Bilgi kutusunu açın ve ardından İlgili belgeler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="36b87-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="36b87-152">Bilgi kutusu zaten açık olabilir.</span><span class="sxs-lookup"><span data-stu-id="36b87-152">You may already have the FactBox open.</span></span> <span data-ttu-id="36b87-153">Satırlar/Başlık geçiş düğmelerinin sağında, üzerinde bir ok olan simgeyi arayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="36b87-154">Ok sağı gösteriyorsa bilgi kutusu zaten açıktır.</span><span class="sxs-lookup"><span data-stu-id="36b87-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="36b87-155">Ok solu gösteriyorsa bilgi kutusunu açmak için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="36b87-156">Yeni oluşturulan RFQ'yu açmak için Teklif talebi alanındaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="36b87-157">Başlık'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-157">Click Header.</span></span>
10. <span data-ttu-id="36b87-158">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-158">Click Add.</span></span>
11. <span data-ttu-id="36b87-159">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="36b87-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="36b87-160">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-160">Click Add.</span></span>
13. <span data-ttu-id="36b87-161">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="36b87-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="36b87-162">Gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-162">Click Send.</span></span>
15. <span data-ttu-id="36b87-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-163">Click OK.</span></span>
16. <span data-ttu-id="36b87-164">Yanıt gir düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-164">Click Enter reply.</span></span>
17. <span data-ttu-id="36b87-165">Eylem Bölmesinde, Yanıtla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="36b87-166">Verileri yanıta kopyala düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="36b87-167">Bu, RFQ'dan yanıta miktar ve tarihler gibi verileri kopyalar.</span><span class="sxs-lookup"><span data-stu-id="36b87-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="36b87-168">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="36b87-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="36b87-169">Bu, satıcıdan aldığınız fiyattır.</span><span class="sxs-lookup"><span data-stu-id="36b87-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="36b87-170">Ayrıca satıcıdan ek bilgiler girmek de isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36b87-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="36b87-171">Kabul et düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-171">Click Accept.</span></span>
21. <span data-ttu-id="36b87-172">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="36b87-173">Satıcı ve fiyatın talebe aktarılmış olduğunu doğrulayın</span><span class="sxs-lookup"><span data-stu-id="36b87-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="36b87-174">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-174">Close the page.</span></span>
2. <span data-ttu-id="36b87-175">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-175">Click Lines.</span></span>
3. <span data-ttu-id="36b87-176">İlgili bilgiler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-176">Click Related information.</span></span>
4. <span data-ttu-id="36b87-177">Satınalma talebi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="36b87-178">RFQ'ya transfer edilen satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="36b87-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="36b87-179">Fiyatın ve satıcının talebe kopyalandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="36b87-180">İletişim kutusu formunu açmak için İş akışı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="36b87-181">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-181">Click Complete.</span></span>
8. <span data-ttu-id="36b87-182">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36b87-182">Close the page.</span></span>
9. <span data-ttu-id="36b87-183">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36b87-183">Click Complete.</span></span>

