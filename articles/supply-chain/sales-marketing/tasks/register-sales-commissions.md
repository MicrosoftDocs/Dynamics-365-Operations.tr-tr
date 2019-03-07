---
title: Satış komisyonlarını kaydetme
description: Bu yordam, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini göstermektedir.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "355162"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="4875b-103">Satış komisyonlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="4875b-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4875b-104">Bu yordam, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="4875b-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="4875b-105">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4875b-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4875b-106">Bu kılavuzu başlatmadan önce, gerekli tüm komisyon hesaplama ayarlarını yaptığınızdan emin olmak için "Satış komisyonu kuralları ayarlama" adlı kılavuzu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="4875b-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="4875b-107">Komisyon işlemi için seçtiğiniz müşteri ve ürün numaralarını not edin ve sorulduğunda bu kılavuzda bir satış siparişi oluşturmak için bunları kullanın.</span><span class="sxs-lookup"><span data-stu-id="4875b-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="4875b-108">Bir satış elemanının bir komisyon için uygun olduğunu gösteren satış siparişini faturalama</span><span class="sxs-lookup"><span data-stu-id="4875b-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="4875b-109">Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="4875b-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="4875b-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-110">Click New.</span></span>
3. <span data-ttu-id="4875b-111">Müşteri hesabı alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4875b-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4875b-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4875b-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4875b-114">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-114">Click OK.</span></span>
7. <span data-ttu-id="4875b-115">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="4875b-116">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-116">Click Change view.</span></span>
9. <span data-ttu-id="4875b-117">Başlık görünümü'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-117">Click Header view.</span></span>
10. <span data-ttu-id="4875b-118">Kurulum bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="4875b-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="4875b-119">Satış grubu alanındaki değer, bir veya daha fazla satış temsilcisinin atandığı bir grubu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="4875b-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="4875b-120">Sipariş faturalandırıldığında, gruptaki kişiler önceden tanımlanmış oranlara ve dağıtıma göre komisyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4875b-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="4875b-121">Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4875b-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="4875b-122">Satış grubu, satış siparişi satırına da kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="4875b-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="4875b-123">Bir üstbilgiden ve/veya satırlar arası bilgiden farklı olabilmesi için bunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4875b-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="4875b-124">Komisyon grubu alanındaki değer, bir veya daha fazla müşteri için komisyonları izleme amacıyla oluşturduğunuz bir grubu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="4875b-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="4875b-125">Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4875b-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="4875b-126">Eylem Bölmesinde, Seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="4875b-127">Görünümü değiştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-127">Click Change view.</span></span>
13. <span data-ttu-id="4875b-128">Satır görünümü'nü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4875b-128">Click Line view.</span></span>
14. <span data-ttu-id="4875b-129">Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="4875b-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="4875b-130">Listede, komisyonlar için ayarlamış olduğunuz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="4875b-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="4875b-131">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="4875b-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4875b-132">Satırın Net tutarını not edin.</span><span class="sxs-lookup"><span data-stu-id="4875b-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="4875b-133">Bu, bu örnekte komisyon hesaplamasının temeli olan satış geliri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="4875b-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="4875b-134">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-134">Click Save.</span></span>
18. <span data-ttu-id="4875b-135">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="4875b-136">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-136">Click Invoice.</span></span>
20. <span data-ttu-id="4875b-137">Parametreler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="4875b-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="4875b-138">Miktar alanında, 'Tümü' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4875b-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="4875b-139">Deftere nakil alanında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4875b-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="4875b-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-140">Click OK.</span></span>
24. <span data-ttu-id="4875b-141">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-141">Click OK.</span></span>
    * <span data-ttu-id="4875b-142">Bir hareketin deftere nakledilmesi bir dakika kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="4875b-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="4875b-143">İşleme koyulmasını ve tamamlanmasını bekleyin ve sayfayı kapatmayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="4875b-144">Kayıtlı satış komisyonlarını gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="4875b-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="4875b-145">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="4875b-146">Fatura'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-146">Click Invoice.</span></span>
3. <span data-ttu-id="4875b-147">Eylem Bölmesinde, Fatura öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="4875b-148">Komisyon hareketleri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4875b-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="4875b-149">Genel bakış sekmesi, faturalanan satış siparişiyle ilişkili satış temsilcilerine ödenecek komisyon tutarlarını temsil eden satırları gösterir.</span><span class="sxs-lookup"><span data-stu-id="4875b-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="4875b-150">Ayrıntıları gözden geçirelim.</span><span class="sxs-lookup"><span data-stu-id="4875b-150">Let's review the details.</span></span>     
    * <span data-ttu-id="4875b-151">Komisyon satışı grubu ayarlamak için "Satış komisyonu kuralları ayarlama" kılavuzunu kullandıysanız, bir satış komisyonunu alacak iki satış elemanı olur ve komisyon ikisi arasında eşit olarak bölünür.</span><span class="sxs-lookup"><span data-stu-id="4875b-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="4875b-152">Bu örnekte, komisyonun tutarı satış gelirinin (sipariş satırının net tutarı) bir yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="4875b-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="4875b-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4875b-153">Close the page.</span></span>
6. <span data-ttu-id="4875b-154">Fiş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4875b-154">Click Voucher.</span></span>
    * <span data-ttu-id="4875b-155">Önceden tanımlanmış komisyon giderlerine ve komisyon borç hesaplarına nakledilen komisyon tutarlarının fiş hareketlerini gözden geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4875b-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

