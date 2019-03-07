---
title: Tüketim talebi oluşturma
description: Bu yordam, bir talep oluşturma işleminde size yol gösterir.
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "366570"
---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="09ee7-103">Tüketim talebi oluşturma</span><span class="sxs-lookup"><span data-stu-id="09ee7-103">Create a requisition for consumption</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09ee7-104">Bu yordam, bir talep oluşturma işleminde size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="09ee7-105">Ürün tedarik kataloğunuzda bulunan ürünleri arama ve kataloğunuzda bulunmayanları nasıl ekleyeceğiniz hakkında farklı yolları gösterir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="09ee7-106">Bu yordama başlamadan önce Tüketim'in varsayılan talep türü olarak ayarlanmış olduğu bir satın alma ilkeniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="09ee7-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="09ee7-107">Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09ee7-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="09ee7-108">Yordam, yalnızca çalışan olarak ayarlanmış bir kullanıcı profili tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="09ee7-109">Bu görev normalde bir personel tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="09ee7-110">Personel işe alma güvenlik rolü, görevleri gerçekleştirmenize izin verir veya USMF kullanıyorsanız, Sibel olarak oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09ee7-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="09ee7-111">Yeni bir talep oluştur</span><span class="sxs-lookup"><span data-stu-id="09ee7-111">Create a new requisition</span></span>
1. <span data-ttu-id="09ee7-112">Tedarik ve kaynak Hizmeti'nden > Satınalma talepleri > Satınalma talepleri benim tarafından hazırlandı'ya git.</span><span class="sxs-lookup"><span data-stu-id="09ee7-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="09ee7-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-113">Click New.</span></span>
3. <span data-ttu-id="09ee7-114">İsim alanında, talebe bir ad verin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="09ee7-115">Talep edilen tarih alanında, bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="09ee7-116">Varsayılan olarak, istenen tarih ve hesap oluşturma tarihi satınalma talebi satırlarına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="09ee7-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="09ee7-117">Satır düzeyinde değiştirilebilirler.</span><span class="sxs-lookup"><span data-stu-id="09ee7-117">They can be changed at the line level.</span></span> <span data-ttu-id="09ee7-118">Talep tarihi, talep edilen teslimat tarihidir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="09ee7-119">Muhasebe tarihi alanında bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="09ee7-120">Muhasebe tarihi, muhasebe girişini genel deftere kaydetmek için ve bütçe fonlarının mevcut olup olmadığını doğrulamak için kullanılan tarihtir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="09ee7-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-121">Click OK.</span></span>
7. <span data-ttu-id="09ee7-122">Sebep alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="09ee7-123">Varsayılan olarak, seçtiğiniz işletme gerekçesi sebebi, satınalma talebi satırında belirecektir fakat bunu satır seviyesinde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09ee7-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="09ee7-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="09ee7-125">Sebebi seçin</span><span class="sxs-lookup"><span data-stu-id="09ee7-125">Select the reason</span></span>
10. <span data-ttu-id="09ee7-126">Detaylar alanında talep için daha açıklayıcı bir gerekçe girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="09ee7-127">Talebe bir satır ekle</span><span class="sxs-lookup"><span data-stu-id="09ee7-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="09ee7-128">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-128">Click Add line.</span></span>
    * <span data-ttu-id="09ee7-129">Satınalma talebine satırlar eklemenin iki yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="09ee7-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="09ee7-130">Ürün numarasını zaten biliyorsanız ya da ürün kataloğunda olmayan bir ürün talep edeceğinizi zaten biliyorsanız, "Satır Ekle" ile doğrudan satırı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09ee7-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="09ee7-131">Diğer bir yol ürün kataloğunda maddeleri bulmak için arama ve filtreleme kullanabileceğiniz "Ürün Ekle" seçeneğini kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="09ee7-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="09ee7-132">Yeni oluşturduğunuz satıra tıklatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="09ee7-133">Talepte bulunan, talebi isteyen çalışandır.</span><span class="sxs-lookup"><span data-stu-id="09ee7-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="09ee7-134">Talebi hazırlayan kişi varsayılan olarak talep eden kişidir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="09ee7-135">Başka bir çalışan adına bir talep satırı hazırlamanız için izin verilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="09ee7-136">Bu tür izinleriniz varsa diğer çalışanlar bu aramada gösterilecektir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="09ee7-137">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="09ee7-138">Seçmeniz için kullanılabilir olan öğeler, kategori erişim ilkesi ve tüzel kişilik için satın alma tedarik katalog ile sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="09ee7-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="09ee7-139">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="09ee7-140">Talebe daha fazla ürün ekle</span><span class="sxs-lookup"><span data-stu-id="09ee7-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="09ee7-141">Ürünler ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-141">Click Add products.</span></span>
    * <span data-ttu-id="09ee7-142">Bu, ürün kataloğu içinde ürünler arayabileceğiniz bir seçenektir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="09ee7-143">Tedarik kataloğu düğümü bul alanında, aradığınız kategorinin adının ilk bölümünü yazın ve Enter tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="09ee7-144">Örneğin, comput yazın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-144">For example, type comput.</span></span>  
3. <span data-ttu-id="09ee7-145">InvokeDefaultButton kısayolunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="09ee7-146">Seçilen kategorideki ürünler listesine filtre uygulamak için Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="09ee7-147">Talebe eklemek istediğiniz ürün kartını seçin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="09ee7-148">Satırlara ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-148">Click Add to lines.</span></span>
7. <span data-ttu-id="09ee7-149">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="09ee7-150">Tedarik kataloğu düğümü bul alanında, aradığınız kategorinin adının ilk bölümünü yazın ve Enter tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="09ee7-151">Örneğin, yüksek (vurgulayıcılar) yazın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="09ee7-152">InvokeDefaultButton kısayolunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="09ee7-153">Tedarik Kataloğu'nda listelenmemiş bir ürün eklemek Listelenmemiş ürünü satırlara ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="09ee7-154">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="09ee7-155">Birim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="09ee7-156">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-156">Click OK.</span></span>
14. <span data-ttu-id="09ee7-157">Madde açıklaması alanına madde için bir açıklama yazın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="09ee7-158">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="09ee7-159">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="09ee7-160">(Seçtiğiniz satıcı hesabı alanına) belirli bir satıcı için fiyatı biliyorsanız, bu fiyatı girebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="09ee7-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="09ee7-161">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="09ee7-162">Bu alanda seçilebilecek satıcılar, satınalma ilkelerine ve satıcının geçerli tedarik kategorisinin durumuna bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="09ee7-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="09ee7-163">Burada bir satıcı seçmeye alternatif olarak, Satıcı Öner düğmesini tıklatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09ee7-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="09ee7-164">Listede kullanmak istediğiniz satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="09ee7-165">Harici madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="09ee7-166">Bu, satıcı tarafından bilinen bir ürün için referans numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="09ee7-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="09ee7-167">Örneğin, bu satıcının kendi kataloğundaki ürünün madde numarası olabilir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="09ee7-168">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="09ee7-169">Tutarları dağıt</span><span class="sxs-lookup"><span data-stu-id="09ee7-169">Distribute amounts</span></span>
1. <span data-ttu-id="09ee7-170">Finansal öğeler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-170">Click Financials.</span></span>
2. <span data-ttu-id="09ee7-171">Dağıtım tutarlarını'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="09ee7-172">Bu işlem ilk satır maliyetini 2 hesapları arasında dağıtmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="09ee7-173">Bu daha sonra, talep incelemede olduğunda da yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="09ee7-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="09ee7-174">Yeni bir dağıtım satırı oluşturmak için Böl'e tıklatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="09ee7-175">Genel muhasebe hesabı alanında maliyetin bir kısmını üstlenecek ilk maliyet merkezini seçin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="09ee7-176">Diğer dağıtım satırını seç.</span><span class="sxs-lookup"><span data-stu-id="09ee7-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="09ee7-177">Genel muhasebe hesabı alanında diğer maliyet merkezi belirtin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="09ee7-178">Eşit olarak dağıt'ı tıkaltın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="09ee7-179">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="09ee7-180">Satır ayrıntılarını görüntüle</span><span class="sxs-lookup"><span data-stu-id="09ee7-180">View line details</span></span>
1. <span data-ttu-id="09ee7-181">Satır ayrıntıları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="09ee7-182">Talebi gönder</span><span class="sxs-lookup"><span data-stu-id="09ee7-182">Submit the requisition</span></span>
1. <span data-ttu-id="09ee7-183">İletişim kutusu formunu açmak için İş akışı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="09ee7-184">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-184">Click Submit.</span></span>
3. <span data-ttu-id="09ee7-185">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-185">Close the page.</span></span>
4. <span data-ttu-id="09ee7-186">Yorum alanına, talebin onaylayıcısı için bir not yazın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="09ee7-187">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-187">Click Submit.</span></span>
6. <span data-ttu-id="09ee7-188">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="09ee7-188">Close the page.</span></span>
7. <span data-ttu-id="09ee7-189">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="09ee7-189">Refresh the page.</span></span>

