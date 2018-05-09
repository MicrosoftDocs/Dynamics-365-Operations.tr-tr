--- 
title: "Serbest metin faturası oluşturma"
description: "Bu görev kılavuzu, serbest metin faturası oluşturmayı gösterir."
author: mikefalkner
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 16fd3c6459389d20c59047d37ec8ca40424c62d2
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="97b89-103">Serbest metin faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="97b89-103">Create a free text invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97b89-104">Bu görev kılavuzu, serbest metin faturası oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="97b89-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="97b89-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="97b89-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="97b89-106">Alacak hesapları > Faturalar > Tüm serbest metin faturaları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="97b89-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="97b89-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="97b89-107">Click New.</span></span>
3. <span data-ttu-id="97b89-108">Müşteri hesabı alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="97b89-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="97b89-109">Fatura hesabı, varsayılan olarak müşteri hesabı için kullanılan hesap olacaktır.</span><span class="sxs-lookup"><span data-stu-id="97b89-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="97b89-110">Fatura deftere nakledilmediyse, muhasebe durumunun başlangıç değeri İşlemde olur.</span><span class="sxs-lookup"><span data-stu-id="97b89-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="97b89-111">Fatura numarası fatura deftere nakledildiğinde atanır.</span><span class="sxs-lookup"><span data-stu-id="97b89-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="97b89-112">SEPA yönergelerini kullanıyorsanız, otomatik ödeme yönergesi müşteri hesabını seçtiğinizde otomatik olarak bir yönergeyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="97b89-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="97b89-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="97b89-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="97b89-114">Ana hesap alanında, boyutları olmayan bir hesap numarası belirtin.</span><span class="sxs-lookup"><span data-stu-id="97b89-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="97b89-115">Ayrıca ana hesap için bir veya daha fazla karakter girebilir ve hesabınızı bulmak için arama özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b89-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="97b89-116">Bu kılavuzda boyutları daha sonra gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="97b89-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="97b89-117">Ana hesabınıza boyutlar eklemek için Satır ayrıntıları hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="97b89-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="97b89-118">Mali boyutlar satırı sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="97b89-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="97b89-119">Boyutlar yalnızca seçilen satır için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="97b89-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="97b89-120">Satış vergisi grubu müşteriden doldurulur.</span><span class="sxs-lookup"><span data-stu-id="97b89-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="97b89-121">Müşterinin satış vergisi grubu yoksa, ana hesaptan alınan satış vergisi grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="97b89-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="97b89-122">Madde satış vergisi grubu ana hesaptan doldurulur.</span><span class="sxs-lookup"><span data-stu-id="97b89-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="97b89-123">Ana hesapta madde satış vergisi grubu yoksa, Genel muhasebe satış vergisi parametrelerindeki madde satış vergisi grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="97b89-123">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="97b89-124">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="97b89-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="97b89-125">Miktar isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97b89-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="97b89-126">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="97b89-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="97b89-127">Birim fiyatı isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="97b89-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="97b89-128">Tutar, miktarla birim fiyatı çarpılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="97b89-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="97b89-129">Ancak, hesabı geçersiz kılıp kendiniz bir tutar girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b89-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="97b89-130">Faturanız için hesaplanan satış vergisini görüntülemek için Satış vergisi öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="97b89-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="97b89-131">Bu sayfada satış vergisi tutarlarını görüntüleyebilir veya Ayarlama sekmesinde tutarları geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b89-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="97b89-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="97b89-132">Click OK.</span></span>
12. <span data-ttu-id="97b89-133">Faturanıza masraf eklemek için Masraflar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="97b89-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="97b89-134">Masraf kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="97b89-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="97b89-135">Masraf değeri alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="97b89-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="97b89-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="97b89-136">Close the page.</span></span>
16. <span data-ttu-id="97b89-137">Özet fatura ayrıntılarını ve toplamları görüntülemek için Toplamlar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="97b89-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="97b89-138">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="97b89-138">Click Close.</span></span>
18. <span data-ttu-id="97b89-139">Faturayı deftere nakletmek için Deftere naklet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="97b89-139">Click Post to post the invoice.</span></span> <span data-ttu-id="97b89-140">Deftere nakletmeden önce iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b89-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="97b89-141">Faturanızı yazdırma zamanını değiştirmek için:  Her faturayı güncelleştirilir güncelleştirilmez   yazdırmak için Geçerli'yi, tüm faturalar güncelleştirildikten sonra yazdırmak için  Sonra'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="97b89-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="97b89-142">Nakledilmeden önce müşteri kredi limitini kontrol etme yolunu değiştirmek isterseniz Kredi limiti türü'nü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="97b89-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="97b89-143">Faturayı yazdırmak isterseniz Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="97b89-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="97b89-144">Faturayı nakletmek isterseniz Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="97b89-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="97b89-145">Faturayı nakletmeden yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="97b89-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="97b89-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="97b89-146">Click OK.</span></span>


