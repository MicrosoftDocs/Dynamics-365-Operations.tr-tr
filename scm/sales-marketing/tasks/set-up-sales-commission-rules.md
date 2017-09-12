--- 
title: "Satış komisyonu kurallarını ayarlama"
description: "Bu yordam, satış komisyonu hesaplamanın ve izlemenin nasıl ayarlanacağını ve etkinleştirileceğini gösterir."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0ab5b3b5447e56eb8ed012a67454400cb2357af4
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="106d1-103">Satış komisyonu kurallarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="106d1-103">Set up sales commission rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="106d1-104">Bu yordam, satış komisyonu hesaplamanın ve izlemenin nasıl ayarlanacağını ve etkinleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="106d1-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="106d1-105">Bu yordam, hem müşteri hem de ürün komisyon gruplarının nasıl oluşturulacağını ve seçili bir müşterinin ve ürünün ilgili gruplara nasıl bağlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="106d1-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="106d1-106">Bu gruplar daha sonra bir müşteri, ürün ve satış temsilcisinin komisyona hak kazanabilmesi için satış siparişiyle eşleşmesi gereken bir satış temsilcisi kombinasyonu oluşturmak üzere komisyon hesaplaması ayarlarında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="106d1-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="106d1-107">Komisyonun hesaplanması tek bir müşteri ve/veya ürün için de yapılabileceğinden müşteri mi yoksa ürün komisyon grubu oluşturulacağı isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="106d1-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="106d1-108">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="106d1-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="106d1-109">Komisyon gruplarını ve komisyon oranlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="106d1-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="106d1-110">Satış ve pazarlama > Komisyonlar > Komisyon için müşteri grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="106d1-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="106d1-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-111">Click New.</span></span>
3. <span data-ttu-id="106d1-112">Grup alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="106d1-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="106d1-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="106d1-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="106d1-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-114">Click Save.</span></span>
6. <span data-ttu-id="106d1-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-115">Close the page.</span></span>
7. <span data-ttu-id="106d1-116">Satış ve pazarlama > Komisyonlar > Ürün grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="106d1-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="106d1-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-117">Click New.</span></span>
9. <span data-ttu-id="106d1-118">Grup alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="106d1-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="106d1-119">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="106d1-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="106d1-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-120">Close the page.</span></span>
12. <span data-ttu-id="106d1-121">Satış ve pazarlama > Komisyonlar > Satış grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="106d1-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="106d1-122">Komisyon satış grubu, ilgili satış grubuyla ilişkili bir müşteri belirli ürünler satın aldığında bir komisyon kazanmaya uygun olan satış temsilcisi rollerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="106d1-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="106d1-123">USMF demo verisi şirketinde, "Satış temsilcileri ABD." adında bir satış grubu vardır.</span><span class="sxs-lookup"><span data-stu-id="106d1-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="106d1-124">Eylem Bölmesinde, Genel öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="106d1-125">Satış temsilcisi'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-125">Click Sales rep..</span></span>
    * <span data-ttu-id="106d1-126">Satış temsilcisi</span><span class="sxs-lookup"><span data-stu-id="106d1-126">The Sales rep.</span></span> <span data-ttu-id="106d1-127">sayfası, şirketin bir özel komisyon grubu ile ilişkili olan satış personelinin bir listesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="106d1-127">page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="106d1-128">Aynı gruba birden fazla satış temsilcisi atayabilirsiniz ve bunların ilgili toplam komisyon ücreti payını bir yüzde değeri olarak tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="106d1-128">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="106d1-129">Tüm çalışanlar arasında toplam komisyon payı 100'ü geçemez.</span><span class="sxs-lookup"><span data-stu-id="106d1-129">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="106d1-130">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="106d1-130">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="106d1-131">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-131">Click Edit.</span></span>
17. <span data-ttu-id="106d1-132">Komisyon payını '50' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-132">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="106d1-133">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-133">Click New.</span></span>
19. <span data-ttu-id="106d1-134">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="106d1-134">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="106d1-135">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="106d1-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="106d1-136">Örneğin, Ad alanını 'Sema Yıldırım' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="106d1-136">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="106d1-137">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-137">Click Select.</span></span>
22. <span data-ttu-id="106d1-138">Komisyon payını '50' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-138">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="106d1-139">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-139">Click Save.</span></span>
24. <span data-ttu-id="106d1-140">Satış ve pazarlama > Komisyonlar > Komisyon hesaplama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="106d1-140">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="106d1-141">Komisyon hesaplama sayfasında, müşteri ve ürüne ilişkin önceden ayarlanmış bir kombinasyon içerdiğinde satış hareketi için çalışanın alacağı komisyon oranını tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="106d1-141">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="106d1-142">Komisyon oranı ayarının bir parçası olarak, komisyon hesaplama temelini ve iskonto içerip içermeyeceğini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="106d1-142">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="106d1-143">Komisyon oranı etkin olduğunda bir geçerlilik dönemi de girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="106d1-143">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="106d1-144">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-144">Click New.</span></span>
26. <span data-ttu-id="106d1-145">Madde kodu alanında, "Grup"u seçin.</span><span class="sxs-lookup"><span data-stu-id="106d1-145">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="106d1-146">Madde ilişkisi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-146">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="106d1-147">Listede, daha önce oluşturduğunuz grubu bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="106d1-147">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="106d1-148">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-148">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="106d1-149">Müşteri kodu alanında 'Grup' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="106d1-149">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="106d1-150">Müşteri ilişkisi alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-150">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="106d1-151">Listede, daha önce ayarladığınız grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="106d1-151">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="106d1-152">Satış temsilcisi</span><span class="sxs-lookup"><span data-stu-id="106d1-152">In the Sales rep.</span></span> <span data-ttu-id="106d1-153">ilişki alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-153">relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="106d1-154">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="106d1-154">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="106d1-155">"Satır iskontosundan önce" seçeneğini tutun.</span><span class="sxs-lookup"><span data-stu-id="106d1-155">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="106d1-156">Komisyon değeri hesaplaması için temel olarak "Gelir" seçeneği tutun.</span><span class="sxs-lookup"><span data-stu-id="106d1-156">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="106d1-157">Komisyon yüzdesi alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="106d1-157">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="106d1-158">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-158">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="106d1-159">Komisyon nakil ayarları</span><span class="sxs-lookup"><span data-stu-id="106d1-159">Setting up commission posting</span></span>
1. <span data-ttu-id="106d1-160">Satış ve pazarlama > Komisyonlar > Komisyon nakil'e gidin.</span><span class="sxs-lookup"><span data-stu-id="106d1-160">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="106d1-161">Komisyon ücretleri çalışanlara ödeneceğinden Genel muhasebe'de mali nakli uygun hesaplara doğru şekilde yapılacak biçimde ayarlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="106d1-161">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="106d1-162">Bu komisyon nakil sayfasında yapılır.</span><span class="sxs-lookup"><span data-stu-id="106d1-162">This is done in the Commission posting page.</span></span> <span data-ttu-id="106d1-163">Geçerli şirket için kullanılabilir ayarı gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="106d1-163">Review the setup that is available for the current company.</span></span> <span data-ttu-id="106d1-164">Genellikle, komisyon tutarları özel bir gider hesabına nakledilir ve özel bir alacaklı hesabına mahsup edilir.</span><span class="sxs-lookup"><span data-stu-id="106d1-164">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="106d1-165">Komisyon nakil kuralları ayarlanmamışsa, sistem komisyona uygun olan satış siparişini faturalama işlemini tamamlayamaz.</span><span class="sxs-lookup"><span data-stu-id="106d1-165">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="106d1-166">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-166">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="106d1-167">Bir müşteri ve bir ürün için bir komisyon grubu atama</span><span class="sxs-lookup"><span data-stu-id="106d1-167">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="106d1-168">Satış ve pazarlama > Komisyonlar > Tüm müşteriler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="106d1-168">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="106d1-169">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="106d1-169">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="106d1-170">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-170">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="106d1-171">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-171">Click Edit.</span></span>
5. <span data-ttu-id="106d1-172">Satış siparişi varsayılanları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="106d1-172">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="106d1-173">Komisyon grubu alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-173">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="106d1-174">Listede, daha önce oluşturduğunuz grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="106d1-174">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="106d1-175">Satış grubu alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-175">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="106d1-176">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="106d1-176">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="106d1-177">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-177">Click Save.</span></span>
11. <span data-ttu-id="106d1-178">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="106d1-178">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="106d1-179">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="106d1-179">Use the Quick Filter to find records.</span></span> <span data-ttu-id="106d1-180">Örneğin, Ürün numarası alanını 'T0020' değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="106d1-180">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="106d1-181">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="106d1-181">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="106d1-182">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-182">Click Edit.</span></span>
15. <span data-ttu-id="106d1-183">Satış bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="106d1-183">Expand the Sell section.</span></span>
16. <span data-ttu-id="106d1-184">Komisyon grubu alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="106d1-184">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="106d1-185">Listede, daha önce oluşturduğunuz komisyon grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="106d1-185">In the list, select the commission group that you created earlier.</span></span>


