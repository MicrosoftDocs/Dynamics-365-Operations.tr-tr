---
title: Satış komisyonlarını kaydetme
description: Bu konu, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini açıklar.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c6dbccc3e2c33c8dfec2373bd21c7bd217a889b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203254"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="d0fe6-103">Satış komisyonlarını kaydetme</span><span class="sxs-lookup"><span data-stu-id="d0fe6-103">Register sales commissions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0fe6-104">Bu konu, satış komisyonlarının nasıl hesaplanacağını ve kaydedileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-104">This topic explains how sales commissions are calculated and registered.</span></span> <span data-ttu-id="d0fe6-105">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d0fe6-106">Bu kılavuzu başlatmadan önce, gerekli tüm komisyon hesaplama ayarlarını yaptığınızdan emin olmak için "Satış komisyonu kuralları ayarlama" adlı kılavuzu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="d0fe6-107">Komisyon işlemi için seçtiğiniz müşteri ve ürün numaralarını not edin ve sorulduğunda bu kılavuzda bir satış siparişi oluşturmak için bunları kullanın.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="d0fe6-108">Bir satış elemanının bir komisyon için uygun olduğunu gösteren satış siparişini faturalama</span><span class="sxs-lookup"><span data-stu-id="d0fe6-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="d0fe6-109">Gezinti bölmesinde **Modüller > Satış ve pazarlama > Satış siperişler > Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-109">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="d0fe6-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-110">Select **New**.</span></span>
3. <span data-ttu-id="d0fe6-111">**Müşteri numarası** alanında, açılır menüden istediğiniz kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-111">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="d0fe6-112">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-112">Select **OK**.</span></span>
5. <span data-ttu-id="d0fe6-113">Eylem Bölmesinde, **Seçenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-113">On the Action Pane, select **Options**.</span></span>
6. <span data-ttu-id="d0fe6-114">**Görünümü değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-114">Select **Change view**.</span></span>
7. <span data-ttu-id="d0fe6-115">**Başlık görünümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-115">Select **Header view**.</span></span>
8. <span data-ttu-id="d0fe6-116">**Kurulum** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-116">Expand the **Setup** section.</span></span>

    - <span data-ttu-id="d0fe6-117">**Satış grubu** alanındaki değer, bir veya daha fazla satış temsilcisinin atandığı bir grubu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-117">The value in the **Sales group** field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="d0fe6-118">Sipariş faturalandırıldığında, gruptaki kişiler önceden tanımlanmış oranlara ve dağıtıma göre komisyonlarını alır.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-118">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   
    - <span data-ttu-id="d0fe6-119">Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-119">The value is copied from the Customer card, but you can change it if you wish.</span></span>  
    - <span data-ttu-id="d0fe6-120">Satış grubu, satış siparişi satırına da kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-120">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="d0fe6-121">Bir üstbilgiden ve/veya satırlar arası bilgiden farklı olabilmesi için bunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-121">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    - <span data-ttu-id="d0fe6-122">**Komisyon grubu** alanındaki değer, bir veya daha fazla müşteri için komisyonları izleme amacıyla oluşturduğunuz bir grubu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-122">The value in the **Commission group** field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   
    - <span data-ttu-id="d0fe6-123">Değer, Müşteri kartından kopyalanır ancak isterseniz değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-123">The value is copied from the Customer card, but you can change it if you wish.</span></span>   

9. <span data-ttu-id="d0fe6-124">Eylem Bölmesinde, **Seçenekler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-124">On the Action Pane, select **Options**.</span></span>
10. <span data-ttu-id="d0fe6-125">**Görünümü değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-125">Select **Change view**.</span></span>
11. <span data-ttu-id="d0fe6-126">**Satır görünümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-126">Select **Line view**.</span></span>
12. <span data-ttu-id="d0fe6-127">**Madde numarası** alanının açılır menüsünde, komisyonlar için ayarladığınız maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-127">In the drop down menu of the **Item number** field, select the item you have set up for commissions.</span></span> 
13. <span data-ttu-id="d0fe6-128">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-128">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="d0fe6-129">Satırın Net tutarını not edin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-129">Take note of the line's Net amount.</span></span> <span data-ttu-id="d0fe6-130">Bu, bu örnekte komisyon hesaplamasının temeli olan satış geliri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-130">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
14. <span data-ttu-id="d0fe6-131">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-131">Select **Save**.</span></span>
15. <span data-ttu-id="d0fe6-132">Eylem Bölmesinde, **Fatura**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-132">On the Action Pane, select **Invoice**.</span></span>
16. <span data-ttu-id="d0fe6-133">**Fatura**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-133">Select **Invoice**.</span></span>
17. <span data-ttu-id="d0fe6-134">**Parametreler** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-134">Expand the **Parameters** section.</span></span>
18. <span data-ttu-id="d0fe6-135">**Miktar** alanında **Tümü** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-135">In the **Quantity** field, select **All**.</span></span>
19. <span data-ttu-id="d0fe6-136">**Deftere nakil** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-136">Select **Yes** in the **Posting** field.</span></span>
20. <span data-ttu-id="d0fe6-137">**Tamam**'ı seçin ve sonraki bölmede **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-137">Select **OK**, then select **OK** in the next pane.</span></span> <span data-ttu-id="d0fe6-138">Bir hareketin deftere nakledilmesi bir dakika kadar sürebilir.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-138">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="d0fe6-139">İşleme koyulmasını ve tamamlanmasını bekleyin ve sayfayı kapatmayın.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-139">Allow the processing to complete and don't close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="d0fe6-140">Kayıtlı satış komisyonlarını gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="d0fe6-140">Review the registered sales commissions</span></span>
1. <span data-ttu-id="d0fe6-141">Eylem Panosunda, **Fatura**'yı ve sonra tekrar **Fatura**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-141">On the Action Pane, select **Invoice**, then select **Invoice** again.</span></span>
2. <span data-ttu-id="d0fe6-142">Eylem Panosunda, **Fatura**'yı ve sonra **Komisyon hareketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-142">On the Action Pane, select **Invoice**, then select **Commission transactions**.</span></span>

    - <span data-ttu-id="d0fe6-143">**Genel bakış** öğesi, faturalanan satış siparişiyle ilişkili satış temsilcilerine ödenecek komisyon tutarlarını temsil eden satırları gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-143">The **Overview** tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="d0fe6-144">Ayrıntıları gözden geçirelim.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-144">Let's review the details.</span></span>  
    - <span data-ttu-id="d0fe6-145">**Komisyon satışı** grubu ayarlamak için "Satış komisyonu kuralları ayarlama" kılavuzunu kullandıysanız, bir satış komisyonunu alacak iki satış elemanı olur ve komisyon ikisi arasında eşit olarak bölünür.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-145">If you used the "Set up sales commission rules" guide to set up the **Commission sales** group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    - <span data-ttu-id="d0fe6-146">Bu örnekte, komisyonun tutarı satış gelirinin (sipariş satırının net tutarı) bir yüzdesi olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-146">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>  
3. <span data-ttu-id="d0fe6-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-147">Close the page.</span></span>
4. <span data-ttu-id="d0fe6-148">**Fiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-148">Select **Voucher**.</span></span> <span data-ttu-id="d0fe6-149">Önceden tanımlanmış komisyon giderlerine ve komisyon borç hesaplarına nakledilen komisyon tutarlarının fiş hareketlerini gözden geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0fe6-149">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

