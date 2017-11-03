--- 
title: "Siparişleri doğrudan teslim olarak sevk etme"
description: "Bu yordam, satış siparişi için bir doğrudan teslimat oluşturmayı göstermektedir."
author: omulvad
manager: AnnBe
ms.date: 02/12/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f674de4877dd2d6e6f1ff02f16a68cb4805d9864
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="ship-orders-as-direct-deliveries"></a><span data-ttu-id="8e15c-103">Siparişleri doğrudan teslim olarak sevk etme</span><span class="sxs-lookup"><span data-stu-id="8e15c-103">Ship orders as direct deliveries</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e15c-104">Bu yordam, satış siparişi için bir doğrudan teslimat oluşturmayı göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-104">This procedure demonstrates how to create a direct delivery for a sales order.</span></span> <span data-ttu-id="8e15c-105">Malları ilk önce ambarınız yerine doğrudan satıcınızdan müşteriye sevk etmek istediğinizde doğrudan teslimat seçeneğini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="8e15c-105">You use direct delivery when you want to ship goods to the customer directly from your vendor, instead of shipping them to your own warehouse first.</span></span> <span data-ttu-id="8e15c-106">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e15c-106">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="8e15c-107">"Doğrudan teslimatları çalışma alanından oluştur" ikincil alt görevini başarıyla tamamlamak için, satış siparişinde seçtiğiniz ürün için Serbest bırakılan ana ürünlerin Satınalma FastTab'inde belirtilmiş varsayılan bir Satıcı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="8e15c-107">To successfully complete the second sub-task "Create direct deliveries from the workbench", make sure that the item that you choose on the sales order has a default Vendor specified on the Purchase FastTab of the Released product master.</span></span>


## <a name="set-an-individual-order-for-direct-delivery"></a><span data-ttu-id="8e15c-108">Doğrudan teslimat için tek bir sipariş ayarlama</span><span class="sxs-lookup"><span data-stu-id="8e15c-108">Set an individual order for direct delivery</span></span>
1. <span data-ttu-id="8e15c-109">Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-109">Go to All sales orders.</span></span>
2. <span data-ttu-id="8e15c-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-110">Click New.</span></span>
3. <span data-ttu-id="8e15c-111">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-111">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="8e15c-112">USMF kullanıyorsanız, hesap US-001'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e15c-112">If you’re using USMF, you can select account US-001.</span></span>  
4. <span data-ttu-id="8e15c-113">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-113">Click OK.</span></span>
5. <span data-ttu-id="8e15c-114">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="8e15c-115">USMF kullanıyorsanız, T0020 öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e15c-115">If you’re using USMF, you can select item T0020.</span></span>  
6. <span data-ttu-id="8e15c-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-116">Click Save.</span></span>
7. <span data-ttu-id="8e15c-117">Eylem Bölmesinde, Satış siparişi öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-117">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="8e15c-118">Doğrudan teslimat öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-118">Click Direct delivery.</span></span>
    * <span data-ttu-id="8e15c-119">Teslimat oluştur sayfası, tüm açık satış siparişi satırlarını satış siparişinden kopyalayarak listeler.</span><span class="sxs-lookup"><span data-stu-id="8e15c-119">The Create delivery page lists all the open sales order lines as copied from the sales order.</span></span> <span data-ttu-id="8e15c-120">Sipariş ayrıntılarını gözden geçirebilir ve gerekiyorsa doğrudan teslimat oluşturmadan önce satınalma miktarı ve fiyatlandırma koşulları gibi ayrıntıları değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e15c-120">You can review the order details, and if required, you can modify details such purchase quantity and pricing terms before you create the direct delivery.</span></span>  
9. <span data-ttu-id="8e15c-121">Tümünü dahil et alanında Evet seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-121">Select Yes in the Include all field.</span></span>
    * <span data-ttu-id="8e15c-122">Satış siparişi satırlarının yalnızca bir alt kümesi için bir doğrudan teslimat oluşturmak istiyorsanız, bunları tek tek seçin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-122">If you want to generate a direct delivery for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="8e15c-123">Satıcı hesabı alanı bir satıcı numarası ile önceden doldurulmuş olabilir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-123">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="8e15c-124">Varsayılan satıcı ürün için (ilişkili ürün kapsamında) ayarlanmışsa, bu satıcı satıra kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="8e15c-124">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied to the line.</span></span> <span data-ttu-id="8e15c-125">Aksi takdirde, manüel olarak bir satıcı girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-125">Otherwise, you must enter a vendor manually.</span></span> <span data-ttu-id="8e15c-126">Bu örnekte, bir tanesi önceden doldurulmuş olsa bile, sonraki adımda yeni bir satıcı seçilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-126">In this example, we’ll select a new vendor in the next step, even if one is already populated.</span></span>   
10. <span data-ttu-id="8e15c-127">Satıcı hesabı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-127">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="8e15c-128">USMF kullanıyorsanız, hesap 1001'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e15c-128">If you’re using USMF, you can select account 1001.</span></span>  
11. <span data-ttu-id="8e15c-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-129">Click OK.</span></span>
    * <span data-ttu-id="8e15c-130">İleti, satınalma siparişinin oluşturulduğunu bildirir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-130">The message informs you that the purchase order has now been created.</span></span>   
12. <span data-ttu-id="8e15c-131">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-131">Expand the Line details section.</span></span>
13. <span data-ttu-id="8e15c-132">Teslimat sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-132">Click the Delivery tab.</span></span>
    * <span data-ttu-id="8e15c-133">Doğrudan teslimat alanı artık Evet olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8e15c-133">The Direct delivery field is now set to Yes.</span></span>  
    * <span data-ttu-id="8e15c-134">Doğrudan teslimat durumu oluşturulan Satınalma siparişini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-134">The Direct delivery status shows the Purchase order created.</span></span>   
14. <span data-ttu-id="8e15c-135">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-135">On the Action Pane, click General.</span></span>
15. <span data-ttu-id="8e15c-136">İlgili siparişleri tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-136">Click Related orders.</span></span>
16. <span data-ttu-id="8e15c-137">Satınalma siparişi alanındaki bağlantıyı izlemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-137">Click to follow the link in the Purchase order field.</span></span>
17. <span data-ttu-id="8e15c-138">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-138">Expand the Line details section.</span></span>
18. <span data-ttu-id="8e15c-139">Adres sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-139">Click the Address tab.</span></span>
    * <span data-ttu-id="8e15c-140">Bu satınalma siparişi satırındaki teslimat adresinin şirketinizin adresi değil müşterinin teslimat adresi olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-140">Note that the delivery address for this purchase order line is the customer's delivery address and not your company's address.</span></span>  
    * <span data-ttu-id="8e15c-141">Satınalma siparişi satırında ya da kaynak satış siparişi satırında teslimat adresini değiştirirseniz, ilgili sipariş satırı otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-141">If you change the delivery address on either the purchase order line or the originating sales order line, the address on the corresponding order line will be automatically updated.</span></span>  
19. <span data-ttu-id="8e15c-142">Teslimat sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-142">Click the Delivery tab.</span></span>
    * <span data-ttu-id="8e15c-143">Tıpkı satış siparişi satırı gibi ilgili satınalma siparişi satırı türü de Doğrudan teslimat olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8e15c-143">Like the sales order line, the associated purchase order line type is also set to Direct delivery.</span></span>  
    * <span data-ttu-id="8e15c-144">Satınalma siparişi satırının Teslimat tarihi ve Onaylı teslimat tarihi, sırasıyla satış siparişi satırındaki Talep edilen giriş tarihi ve Onaylı giriş tarihi şeklinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8e15c-144">The purchase order line's Delivery  date and the Confirmed delivery date are set to the Requested receipt date and Confirmed receipt date of the originating sales order line respectively.</span></span>   
    * <span data-ttu-id="8e15c-145">Satınalma satırında ya da satış satırında bu tarihlerin birini güncelleştirirseniz, ilgili siparişin tarihleri otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-145">If you update any of these dates on either the purchase line or the sales line, the dates on the corresponding order will be automatically updated.</span></span>     
    * <span data-ttu-id="8e15c-146">Malların doğrudan müşteriye teslimatı şeklinde ayarlanan satınalma siparişi özel bir ilişki üzerinden kaynak satış siparişine bağlanır.</span><span class="sxs-lookup"><span data-stu-id="8e15c-146">The purchase order that is set to deliver goods directly the customer is linked to the originating sales order by means of a special association.</span></span> <span data-ttu-id="8e15c-147">Bu ilişkilendirme, satış siparişinin sevk irsaliyesi güncelleştirmesinin kendiliğinden satış siparişinden yapılamayacağı ve satınalma siparişi kullanılarak yapılması gerektiği kuralını zorunlu kılar.</span><span class="sxs-lookup"><span data-stu-id="8e15c-147">This association imposes the rule that the packing slip update of the sales order can't be done from the sales order itself and must be done by using the purchase order.</span></span> <span data-ttu-id="8e15c-148">Ancak, müşteri faturalandırması satış siparişinden gerçekleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-148">However, customer invoicing must be carried out from the sales order.</span></span>  
20. <span data-ttu-id="8e15c-149">Eylem Bölmesinde, Satınalma öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-149">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="8e15c-150">Onay'a tıklayın</span><span class="sxs-lookup"><span data-stu-id="8e15c-150">Click Confirmation.</span></span>
22. <span data-ttu-id="8e15c-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-151">Click OK.</span></span>
23. <span data-ttu-id="8e15c-152">Eylem Bölmesinde, Al öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-152">On the Action Pane, click Receive.</span></span>
24. <span data-ttu-id="8e15c-153">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-153">Click Product receipt.</span></span>
25. <span data-ttu-id="8e15c-154">Ürün girişi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-154">In the Product receipt field, type a value.</span></span>
26. <span data-ttu-id="8e15c-155">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-155">Click OK.</span></span>
27. <span data-ttu-id="8e15c-156">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-156">On the Action Pane, click General.</span></span>
28. <span data-ttu-id="8e15c-157">İlgili siparişleri tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-157">Click Related orders.</span></span>
29. <span data-ttu-id="8e15c-158">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-158">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8e15c-159">Satınalma siparişi 'alındı' olarak güncelleştirildikten veya başka bir deyişle satıcı malları müşterinin adresine sevk ettikten sonra, kaynak satış siparişinin durumu otomatik olarak Teslim edildi olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-159">After the purchase order has been updated as received, or in other words, after the vendor has shipped the goods to your customer's address, the status of the originating sales order is automatically updated to Delivered.</span></span>  
    * <span data-ttu-id="8e15c-160">Satış siparişi artık faturalandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-160">The sales order can now be invoiced.</span></span>    
30. <span data-ttu-id="8e15c-161">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-161">Click OK.</span></span>
31. <span data-ttu-id="8e15c-162">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-162">Close the page.</span></span>
32. <span data-ttu-id="8e15c-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-163">Click OK.</span></span>

## <a name="create-direct-deliveries-from-the-workbench"></a><span data-ttu-id="8e15c-164">Çalışma alanından doğrudan teslimatlar oluşturma</span><span class="sxs-lookup"><span data-stu-id="8e15c-164">Create direct deliveries from the workbench</span></span>
1. <span data-ttu-id="8e15c-165">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-165">Close the page.</span></span>
2. <span data-ttu-id="8e15c-166">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-166">Close the page.</span></span>
3. <span data-ttu-id="8e15c-167">Tüm satış siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-167">Go to All sales orders.</span></span>
4. <span data-ttu-id="8e15c-168">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-168">Click New.</span></span>
5. <span data-ttu-id="8e15c-169">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-169">In the Customer account field, enter or select a value.</span></span>
6. <span data-ttu-id="8e15c-170">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-170">Click OK.</span></span>
7. <span data-ttu-id="8e15c-171">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-171">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="8e15c-172">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-172">Expand the Line details section.</span></span>
9. <span data-ttu-id="8e15c-173">Teslimat sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-173">Click the Delivery tab.</span></span>
    * <span data-ttu-id="8e15c-174">Önceki yordamda olduğu gibi bir doğrudan teslimatı satış siparişi işleminin parçası olarak oluşturmak yerine, bu görevi bir satınalma uzmanına bırakmayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e15c-174">Instead of creating a direct delivery as part of the sales order processing as in the previous procedure, you can choose to hand over this task to a purchasing professional.</span></span> <span data-ttu-id="8e15c-175">Satış siparişi satırını doğrudan teslimat işleme işlemine dahil etmek için doğrudan teslimatın satırını işaretlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-175">To include the sales order line in the direct delivery handling process, you must mark the line for direct delivery.</span></span>  
10. <span data-ttu-id="8e15c-176">Doğrudan teslimat alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-176">Select Yes in the Direct delivery field.</span></span>
    *   <span data-ttu-id="8e15c-177">Ürün zaten varsayılan olarak doğrudan teslimat için ayarlanmışsa, alan sipariş satırı girişinde otomatik olarak Evet olarak ayarlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="8e15c-177">If the item has already been set up for direct delivery by default, the field will automatically be set to Yes at the order line entry.</span></span> <span data-ttu-id="8e15c-178">Doğrudan teslimat seçeneğini Evet olarak ayarlayarak ve varsayılan bir Doğrudan teslimat ambarı seçerek Serbest bırakılan ana üründe doğrudan teslimat için bir ürün ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e15c-178">You can set up an item for direct delivery on the Released product's master by setting the Direct delivery option to Yes and selecting a default Direct delivery warehouse.</span></span>  
    * <span data-ttu-id="8e15c-179">Satınalma siparişi henüz oluşturulmadığından, Doğrudan teslimat durumu Doğrudan teslim edilecek şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8e15c-179">Because the purchase order has not yet been created, the Direct delivery status is set to To be direct delivered.</span></span>   
11. <span data-ttu-id="8e15c-180">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-180">Close the page.</span></span>
12. <span data-ttu-id="8e15c-181">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-181">Close the page.</span></span>
13. <span data-ttu-id="8e15c-182">Doğrudan teslimat'a gidin.</span><span class="sxs-lookup"><span data-stu-id="8e15c-182">Go to Direct delivery.</span></span>
    * <span data-ttu-id="8e15c-183">Doğrudan teslimat sayfası, satınalma aracısına doğrudan teslim edilecek tüm satış siparişi satırlarına yönelik genel bakış sağlayan bir çalışma ekranı olarak iş görür ve bunlara ilgili satınalma siparişlerini oluşturulma imkanı sağlar.</span><span class="sxs-lookup"><span data-stu-id="8e15c-183">The Direct delivery page acts as a workbench that provides the purchasing agent with an overview of all the sales order lines that are to be direct delivered and it allows them to create the respective purchase orders.</span></span> <span data-ttu-id="8e15c-184">Ayrıca, bunlar Onay ve Teslimat sekmelerinde açık doğrudan teslimat siparişlerini ve doğrulanan siparişleri görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="8e15c-184">In addition, they can view the open direct delivery orders and the confirmed orders on the Confirmation and Delivery tabs.</span></span>   
14. <span data-ttu-id="8e15c-185">Doğrudan teslimat oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-185">Click Create direct delivery.</span></span>
15. <span data-ttu-id="8e15c-186">Onay sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8e15c-186">Click the Confirmation tab.</span></span>
    * <span data-ttu-id="8e15c-187">Bir doğrudan teslimat siparişi oluşturduktan sonra, bu otomatik olarak Onay sekmesine gönderilir. Doğrudan bu sayfadan siparişi onaylamayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8e15c-187">After you have created a direct delivery order, it automatically moved to the Confirmation tab. You can choose to confirm the order directly from this page.</span></span> <span data-ttu-id="8e15c-188">Satınalma onaylandığında, girişini kaydettirdiğiniz Teslimat sekmesine otomatik olarak taşınır.</span><span class="sxs-lookup"><span data-stu-id="8e15c-188">When the purchase is confirmed, it will automatically move to the Delivery tab, from which you can registered its receipt.</span></span>  

