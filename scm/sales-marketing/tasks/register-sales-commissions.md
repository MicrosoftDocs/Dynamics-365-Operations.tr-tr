--- 
title: "Satış komisyonlarını kaydetme"
description: "Bu yordam, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini göstermektedir."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f195f9e466eab3cf87afea2b5d430d0ea25c5a83
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="register-sales-commissions"></a><span data-ttu-id="49e49-103">Satış komisyonlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="49e49-103">Register sales commissions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49e49-104">Bu yordam, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="49e49-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="49e49-105">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49e49-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="49e49-106">Bu kılavuzu başlatmadan önce, gerekli tüm komisyon hesaplama ayarlarını yaptığınızdan emin olmak için "Satış komisyonu kuralları ayarlama" adlı kılavuzu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="49e49-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="49e49-107">Komisyon işlemi için seçtiğiniz müşteri ve ürün numaralarını not edin ve sorulduğunda bu kılavuzda bir satış siparişi oluşturmak için bunları kullanın.</span><span class="sxs-lookup"><span data-stu-id="49e49-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="49e49-108">Bir satış elemanının bir komisyon için uygun olduğunu gösteren satış siparişini faturalama</span><span class="sxs-lookup"><span data-stu-id="49e49-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="49e49-109">Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="49e49-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="49e49-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-110">Click New.</span></span>
3. <span data-ttu-id="49e49-111">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="49e49-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="49e49-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="49e49-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="49e49-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-114">Click OK.</span></span>
7. <span data-ttu-id="49e49-115">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="49e49-116">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-116">Click Change view.</span></span>
9. <span data-ttu-id="49e49-117">Başlık görünümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-117">Click Header view.</span></span>
10. <span data-ttu-id="49e49-118">Kurulum bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="49e49-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="49e49-119">Satış grubu alanındaki değer, bir veya daha fazla satış temsilcisinin atandığı bir grubu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="49e49-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="49e49-120">Sipariş faturalandırıldığında, gruptaki kişiler önceden tanımlanmış oranlara ve dağıtıma göre komisyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="49e49-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="49e49-121">Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49e49-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="49e49-122">Satış grubu, satış siparişi satırına da kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="49e49-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="49e49-123">Bir üstbilgiden ve/veya satırlar arası bilgiden farklı olabilmesi için bunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49e49-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="49e49-124">Komisyon grubu alanındaki değer, bir veya daha fazla müşteri için komisyonları izleme amacıyla oluşturduğunuz bir grubu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="49e49-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="49e49-125">Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49e49-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="49e49-126">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="49e49-127">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-127">Click Change view.</span></span>
13. <span data-ttu-id="49e49-128">Satır görünümü'nü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49e49-128">Click Line view.</span></span>
14. <span data-ttu-id="49e49-129">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="49e49-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="49e49-130">Listede, komisyonlar için ayarlamış olduğunuz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="49e49-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="49e49-131">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="49e49-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="49e49-132">Satırın Net tutarını not edin.</span><span class="sxs-lookup"><span data-stu-id="49e49-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="49e49-133">Bu, bu örnekte komisyon hesaplamasının temeli olan satış geliri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="49e49-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="49e49-134">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-134">Click Save.</span></span>
18. <span data-ttu-id="49e49-135">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="49e49-136">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-136">Click Invoice.</span></span>
20. <span data-ttu-id="49e49-137">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="49e49-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="49e49-138">Miktar alanında, 'Tümü' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="49e49-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="49e49-139">Deftere nakil alanında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="49e49-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="49e49-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-140">Click OK.</span></span>
24. <span data-ttu-id="49e49-141">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-141">Click OK.</span></span>
    * <span data-ttu-id="49e49-142">Bir hareketin deftere nakledilmesi bir dakika kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="49e49-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="49e49-143">İşleme koyulmasını ve tamamlanmasını bekleyin ve sayfayı kapatmayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="49e49-144">Kayıtlı satış komisyonlarını gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="49e49-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="49e49-145">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="49e49-146">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-146">Click Invoice.</span></span>
3. <span data-ttu-id="49e49-147">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="49e49-148">Komisyon hareketleri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="49e49-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="49e49-149">Genel bakış sekmesi, faturalanan satış siparişiyle ilişkili satış temsilcilerine ödenecek komisyon tutarlarını temsil eden satırları gösterir.</span><span class="sxs-lookup"><span data-stu-id="49e49-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="49e49-150">Ayrıntıları gözden geçirelim.</span><span class="sxs-lookup"><span data-stu-id="49e49-150">Let's review the details.</span></span>     
    * <span data-ttu-id="49e49-151">Komisyon satışı grubu ayarlamak için "Satış komisyonu kuralları ayarlama" kılavuzunu kullandıysanız, bir satış komisyonunu alacak iki satış elemanı olur ve komisyon ikisi arasında eşit olarak bölünür.</span><span class="sxs-lookup"><span data-stu-id="49e49-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="49e49-152">Bu örnekte, komisyonun tutarı satış gelirinin (sipariş satırının net tutarı) bir yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="49e49-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="49e49-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="49e49-153">Close the page.</span></span>
6. <span data-ttu-id="49e49-154">Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="49e49-154">Click Voucher.</span></span>
    * <span data-ttu-id="49e49-155">Önceden tanımlanmış komisyon giderlerine ve komisyon borç hesaplarına nakledilen komisyon tutarlarının fiş hareketlerini gözden geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="49e49-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


