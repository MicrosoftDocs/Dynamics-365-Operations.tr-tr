--- 
title: "Tek bir şirket için serbest bırakılan ürün oluşturma"
description: "Bu yordam, tek bir yasal birim bağlamında yayımlanan tek bir ürün oluşturmayı adım adım anlatılmaktadır."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f23ddf59d986f16c350e9e978333cd7c9b47389a
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="d8f6e-103">Tek bir şirket için serbest bırakılan ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8f6e-103">Create a released product for a single company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8f6e-104">Bu yordam, tek bir yasal birim bağlamında yayımlanan tek bir ürün oluşturmayı adım adım anlatılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="d8f6e-105">Yayımlanan ürün oluşturulduktan sonra, yalnızca bu birimde hemen kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="d8f6e-106">Bu yordamı, USMF demo verisi şirketi aracılığıyla uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="d8f6e-107">Bu görev, genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="d8f6e-108">Serbest bırakılan ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8f6e-108">Create a released product</span></span>
1. <span data-ttu-id="d8f6e-109">Serbest bırakılan ürünler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-109">Go to Released products.</span></span>
2. <span data-ttu-id="d8f6e-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-110">Click New.</span></span>
3. <span data-ttu-id="d8f6e-111">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="d8f6e-112">Ürün numarası, ürün numarası alanına otomatik olarak girilmezse, benzersiz bir ürün numarasını yazın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="d8f6e-113">Bu adım yalnızca ürün numaraları için numara sırası ayarlanmadıysa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="d8f6e-114">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="d8f6e-115">Ürün adı, arama adına varsayılan olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="d8f6e-116">Gerekirse, arama adını değiştirmeyi tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="d8f6e-117">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-118">Bu madde modeli grupları, maddelerin madde girişlerinde ve çıkışlarında kontrol edilme ve işlenme biçimini belirleyen ayarları içerir.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="d8f6e-119">Bu ayarlar madde tüketiminin nasıl hesaplanacağını da belirler.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="d8f6e-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d8f6e-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d8f6e-122">Madde modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-123">Stok maddelerini madde özelliklerini temel alan gruplara ayırarak stoku yönetmek için madde grupları kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="d8f6e-124">Örneğin, bilgilerin ana hesaplara nasıl aktarıldığını yönetmek için bir dizi belirli ana hesap ile ilişkili farklı madde grupları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="d8f6e-125">Bu maddelerin stok değerini farklı aşamalarda izlemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="d8f6e-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="d8f6e-127">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="d8f6e-128">Depolama alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-129">Depolama stok boyutları maddelerin nasıl depolandığını ve stoktan alındığını kontrol etmenize yardım eder.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="d8f6e-130">Örneğin, bir depolama boyutu, tesis ve ambar olabilir.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="d8f6e-131">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="d8f6e-132">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d8f6e-133">İzleme boyutu grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-134">İzleme boyutu grubu hangi izleme boyutlarını bir ürüne atayabileceğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="d8f6e-135">Örneğin, toplu iş numarası ve seri numarası, stok maddelerini izlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="d8f6e-136">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="d8f6e-137">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="d8f6e-138">Stok birimi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-139">Stok tutma birimi, ürünün stokta depolandığında miktarının nasıl ölçüleceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="d8f6e-140">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="d8f6e-141">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="d8f6e-142">Satınalma birimi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-143">Satınalma birimi, ürünün bir satıcıdan satın alındığında miktar ölçümünün nasıl yapılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-143">The purchase unit determines how the product is quantified when it’s purchased from a vendor.</span></span>  
21. <span data-ttu-id="d8f6e-144">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="d8f6e-145">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="d8f6e-146">Satış birimi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-147">Satış birimi, ürünün müşteriye satıldığında miktar ölçümünün nasıl yapılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-147">The sales unit determines how the product is quantified when it’s sold to a customer.</span></span>  
24. <span data-ttu-id="d8f6e-148">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="d8f6e-149">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="d8f6e-150">Ürün reçetesi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-151">Ürün reçetesi birimi (BOM), ürün reçetesi de dahil olmak üzere, ürünün nasıl ölçüleceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="d8f6e-152">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="d8f6e-153">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="d8f6e-154">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-155">Satış vergi grubundaki madde satış vergisi grubu, satış vergisinin her bir madde için nasıl hesaplandığını belirler.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="d8f6e-156">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="d8f6e-157">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="d8f6e-158">Madde satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d8f6e-159">Satınalma vergilendirmesi grubundaki madde satış vergisi grubu, satınalma vergisinin her bir madde için nasıl hesaplandığını belirler.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="d8f6e-160">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="d8f6e-161">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="d8f6e-162">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="d8f6e-163">Ürün özellikleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-163">Add product characteristics</span></span>
1. <span data-ttu-id="d8f6e-164">Stok yönetimi bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="d8f6e-165">Net ağırlık alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="d8f6e-166">Dara alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="d8f6e-167">Brüt derinlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="d8f6e-168">Brüt genişlik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="d8f6e-169">Brüt yükselik alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="d8f6e-170">Hacim alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="d8f6e-171">Mali boyutlar ekleyin</span><span class="sxs-lookup"><span data-stu-id="d8f6e-171">Add financial dimensions</span></span>
1. <span data-ttu-id="d8f6e-172">Mali boyutlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="d8f6e-173">BusinessUnit alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d8f6e-174">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d8f6e-175">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d8f6e-176">CostCenter alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d8f6e-177">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d8f6e-178">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d8f6e-179">Departman alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d8f6e-180">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="d8f6e-181">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="d8f6e-182">ItemGroup modeli alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="d8f6e-183">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="d8f6e-184">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8f6e-184">In the list, click the link in the selected row.</span></span>


