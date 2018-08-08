--- 
title: "Teklif talebi oluşturma"
description: "Bu prosedür, bir satın alma teklifinin nasıl oluşturulacağını gösterir."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f9927e291916ed1d7f0b706e5920d73835dc2755
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="f9da9-103">Teklif talebi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f9da9-103">Create a request for quotation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9da9-104">Bu prosedür, bir satın alma teklifinin nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="f9da9-105">Bu işlem tipik olarak bir satın alma temsilcisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="f9da9-106">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9da9-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f9da9-107">Başlamadan önce talep türlerini ayarlamış olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="f9da9-108">Bu işlemi tamamladıktan ve bir RFQ oluşturduktan ve gönderdikten sonra her bir satıcı için yanıtlar girebilir, bunları karşılaştırabilir ve işi verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9da9-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="f9da9-109">Yeni bir RFQ hazırlama</span><span class="sxs-lookup"><span data-stu-id="f9da9-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="f9da9-110">Tedarik ve kaynak atama > Teklif talepleri > Tüm teklif talepleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="f9da9-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-111">Click New.</span></span>
    * <span data-ttu-id="f9da9-112">Şu satın alma türleri kullanılabilir: Satın alma emri (varsayılan): ürün satın alınması teklifini veya ödeme karşılığında ürünlerin satılması teklifinin kabul edildiğini onaylayan belgedir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="f9da9-113">Satın alma talebi: doğudan bir satın alma talebinden bir RFQ oluşturduğunuzda bu tür otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="f9da9-114">Bu seçeneği el ile seçerseniz bir hata alırsınız.</span><span class="sxs-lookup"><span data-stu-id="f9da9-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="f9da9-115">Satın alma sözleşmesi: bir üründen belirli bir zaman aralığında belirli bir miktarda veya değerde satın alınması için yapılan sözleşmedir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="f9da9-116">Bu seçeneği belirlerseniz, satın alma sözleşmesi için geçerli olacak tarih aralığını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="f9da9-117">Belge başlığı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="f9da9-118">Talep türü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="f9da9-119">Talep türüyle bir puanlama yöntemi ilişkilendirilmişse bu, oluşturmakta olduğunuz RFQ için varsayılan puanlama yöntemi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="f9da9-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="f9da9-120">Puanlama yönteminin daha sonra değiştirilmesi mümkündür.</span><span class="sxs-lookup"><span data-stu-id="f9da9-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="f9da9-121">Teslimat tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="f9da9-122">Maddeleri almak istediğiniz son tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="f9da9-123">Bitiş tarihi ve saati alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="f9da9-124">Satıcıların RFQ'ya yanıt vermesi gereken son tarihi ve saati belirtin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="f9da9-125">Ambar alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="f9da9-126">Teslimat adresi varsayılan olarak ambar adresidir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="f9da9-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="f9da9-128">Satır ekle</span><span class="sxs-lookup"><span data-stu-id="f9da9-128">Add lines</span></span>
    * <span data-ttu-id="f9da9-129">RFQ'nuz hakkında temel bilgileri belirledikten sonra satıcıların teklif vermelerini istediğiniz malları veya hizmetleri belirlersiniz.</span><span class="sxs-lookup"><span data-stu-id="f9da9-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="f9da9-130">Madde, varsayılan olarak satır tipindedir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="f9da9-131">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="f9da9-132">USMF kullanıyorsanız, T0020'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9da9-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="f9da9-133">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="f9da9-134">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-134">Click Add line.</span></span>
4. <span data-ttu-id="f9da9-135">Satır türü alanından 'Kategori' seçin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="f9da9-136">Stokta olmayan mallar veya hizmetlere yönelik RFQ'lar oluşturmak için Kategori satır türünü kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9da9-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="f9da9-137">Daha sonra, bir satın alma kategorileri hiyerarşisinden malların veya hizmetlerin türünü seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="f9da9-138">Satın alma kategorisi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="f9da9-139">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="f9da9-140">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="f9da9-141">Birim alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="f9da9-142">Satıcı ekle</span><span class="sxs-lookup"><span data-stu-id="f9da9-142">Add vendors</span></span>
1. <span data-ttu-id="f9da9-143">Satır görünümünü Başlık görünümü olarak değiştirmek için Başlığı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="f9da9-144">Satıcı bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="f9da9-145">Satıcıları otomatik olarak ekle düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="f9da9-146">Talep edilen maddelerin satın alma kategorisine bağlı olarak RFQ'ya satıcıları otomatik olarak ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9da9-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="f9da9-147">Satırlara dahil olan kategoriler için onaylanmış satıcılar bulunmuyorsa satıcıları el ile ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9da9-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="f9da9-148">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-148">Click Add.</span></span>
5. <span data-ttu-id="f9da9-149">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="f9da9-150">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-150">Click Add.</span></span>
7. <span data-ttu-id="f9da9-151">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="f9da9-152">Bir satıcıyı seçtiğinizde durumu Oluşturuldu olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="f9da9-153">Bu da satıcı bilgilerinin RFQ'ya kaydedildiği, ancak RFQ'nun satıcıya göndermediğiniz anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f9da9-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="f9da9-154">Satıcı durumundan bağımsız olarak bir satıcıyı bir RFQ'ya ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f9da9-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="f9da9-155">RFQ'yu satıcılara gönderme</span><span class="sxs-lookup"><span data-stu-id="f9da9-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="f9da9-156">Gönder'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-156">Click Send.</span></span>
    * <span data-ttu-id="f9da9-157">Teklif talebi gönderiliyor sayfasında, listedeki satıcıların RFQ almasını istediğiniz satıcılarla aynı olduğunu kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="f9da9-158">Yazdır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-158">Click Print.</span></span>
    * <span data-ttu-id="f9da9-159">Bu iletişim kutusu RFQ'yu yazdırmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="f9da9-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="f9da9-160">Bir yanıt sayfasını yazdırmayı seçerseniz, bu işlemin içeriği Satın Alma ve Kaynak Kullanımı parametreleri altında tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f9da9-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="f9da9-161">Yanıt sayfalarının nasıl yazdırılacağını seçmek için Yazdırma iletişim kutusunu açtıktan sonra Gelişmiş yazdırma seçeneklerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="f9da9-162">Oluşturuldu veya Gönderildiği durumuna sahip satırlar içeren her bir satıcı için bir RFQ yazdırılır.</span><span class="sxs-lookup"><span data-stu-id="f9da9-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="f9da9-163">İptal edilmiş satırlar ve kaydedilmiş yanıtların yer aldığı satırlar yazdırılmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="f9da9-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="f9da9-164">İptal'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-164">Click Cancel.</span></span>
4. <span data-ttu-id="f9da9-165">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-165">Click OK.</span></span>
5. <span data-ttu-id="f9da9-166">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-166">Close the page.</span></span>
6. <span data-ttu-id="f9da9-167">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="f9da9-168">RFQ günlüğünü görüntüleme</span><span class="sxs-lookup"><span data-stu-id="f9da9-168">View the RFQ journal</span></span>
1. <span data-ttu-id="f9da9-169">Tedarik ve kaynak atama > Teklif talepleri > Teklif talepleri takibi > Teklif talebi günlükleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f9da9-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="f9da9-170">Önizleme/Yazdır düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="f9da9-171">Orijinal önizlemeyi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-171">Click Original preview.</span></span>
4. <span data-ttu-id="f9da9-172">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-172">Close the page.</span></span>
5. <span data-ttu-id="f9da9-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f9da9-173">Close the page.</span></span>


