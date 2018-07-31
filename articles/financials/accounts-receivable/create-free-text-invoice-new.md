--- 
title: "Serbest metin faturası oluşturma"
description: "Bu makalede, serbest metin faturasının nasıl oluşturulduğu gösterilmektedir."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
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
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: tr-tr
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="b5716-103">Serbest metin faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5716-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5716-104">Bu makalede, serbest metin faturasının nasıl oluşturulduğu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b5716-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="b5716-105">Bu prosedür için USMF demo şirketini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b5716-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="b5716-106">Serbest metin faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5716-106">Create a free text invoice</span></span>

1. <span data-ttu-id="b5716-107">Alacak hesapları > Faturalar > Tüm serbest metin faturaları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b5716-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="b5716-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-108">Click New.</span></span>
3. <span data-ttu-id="b5716-109">Müşteri hesabı alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b5716-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="b5716-110">Fatura hesabı, varsayılan olarak müşteri hesabı için kullanılan hesap olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b5716-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="b5716-111">Fatura deftere nakledilmediyse, muhasebe durumunun başlangıç değeri İşlemde olur.</span><span class="sxs-lookup"><span data-stu-id="b5716-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="b5716-112">Fatura numarası fatura deftere nakledildiğinde atanır.</span><span class="sxs-lookup"><span data-stu-id="b5716-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="b5716-113">SEPA yönergelerini kullanıyorsanız, otomatik ödeme yönergesi müşteri hesabını seçtiğinizde otomatik olarak bir yönergeyle doldurulur.</span><span class="sxs-lookup"><span data-stu-id="b5716-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="b5716-114">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b5716-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b5716-115">Ana hesap alanında, boyutları olmayan bir hesap numarası belirtin.</span><span class="sxs-lookup"><span data-stu-id="b5716-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="b5716-116">Ayrıca ana hesap için bir veya daha fazla karakter girebilir ve hesabınızı bulmak için arama özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="b5716-117">Bu kılavuzda boyutları daha sonra gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="b5716-118">Ana hesabınıza boyutlar eklemek için Satır ayrıntıları hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="b5716-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="b5716-119">Mali boyutlar satırı sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="b5716-120">Boyutlar yalnızca seçilen satır için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5716-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="b5716-121">Satış vergisi grubu müşteriden doldurulur.</span><span class="sxs-lookup"><span data-stu-id="b5716-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="b5716-122">Müşterinin satış vergisi grubu yoksa, ana hesaptan alınan satış vergisi grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5716-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="b5716-123">Madde satış vergisi grubu ana hesaptan doldurulur.</span><span class="sxs-lookup"><span data-stu-id="b5716-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="b5716-124">Ana hesapta madde satış vergisi grubu yoksa, Genel muhasebe satış vergisi parametrelerindeki madde satış vergisi grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5716-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="b5716-125">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b5716-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b5716-126">Miktar isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b5716-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="b5716-127">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b5716-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="b5716-128">Birim fiyatı isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b5716-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="b5716-129">Tutar, miktarla birim fiyatı çarpılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="b5716-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="b5716-130">Ancak, hesabı geçersiz kılıp kendiniz bir tutar girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="b5716-131">Faturanız için hesaplanan satış vergisini görüntülemek için Satış vergisi öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="b5716-132">Bu sayfada satış vergisi tutarlarını görüntüleyebilir veya Ayarlama sekmesinde tutarları geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="b5716-133">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-133">Click OK.</span></span>
12. <span data-ttu-id="b5716-134">Faturanıza masraf eklemek için Masraflar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="b5716-135">Masraf kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b5716-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="b5716-136">Masraf değeri alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="b5716-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="b5716-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b5716-137">Close the page.</span></span>
16. <span data-ttu-id="b5716-138">Özet fatura ayrıntılarını ve toplamları görüntülemek için Toplamlar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="b5716-139">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-139">Click Close.</span></span>
18. <span data-ttu-id="b5716-140">Faturayı deftere nakletmek için Deftere naklet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-140">Click Post to post the invoice.</span></span> <span data-ttu-id="b5716-141">Deftere nakletmeden önce iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="b5716-142">Faturanızı yazdırma zamanını değiştirmek için:  Her faturayı güncelleştirilir güncelleştirilmez   yazdırmak için Geçerli'yi, tüm faturalar güncelleştirildikten sonra yazdırmak için  Sonra'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="b5716-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="b5716-143">Nakledilmeden önce müşteri kredi limitini kontrol etme yolunu değiştirmek isterseniz Kredi limiti türü'nü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b5716-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="b5716-144">Faturayı yazdırmak isterseniz Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b5716-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="b5716-145">Faturayı nakletmek isterseniz Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b5716-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="b5716-146">Faturayı nakletmeden yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="b5716-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="b5716-148">Satırları kopyala</span><span class="sxs-lookup"><span data-stu-id="b5716-148">Copy lines</span></span>
<span data-ttu-id="b5716-149">Serbest metin faturasında satırları kopyalamak için bir veya birden fazla satırı seçin ve Seçili satırları kopyala'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b5716-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="b5716-150">Almak istediğiniz kopya sayısını belirtebilir, notları ve ekleri de kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="b5716-151">Dağıtımları da kopyalayabilir ve deftere naklederken yeniden oluşturulmalarına da izin verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="b5716-152">Satırları kopyaladıktan sonra bilgilerde gerekli düzenlemeleri yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="b5716-153">Şablondan serbest metin faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5716-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="b5716-154">Şablondan serbest metin faturası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="b5716-155">Fatura sekmesinden "Şablondan yeni"yi seçtiğiniz zaman yeni serbest metin faturası için bir şablon adı ve müşterinin hesabını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="b5716-156">Ayrıca müşterinin ödeme yöntemi ve ödeme koşulları gibi varsayılan değerler belirlemeyi tercih edebilir veya şablonla kaydedilmiş değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="b5716-157">Yeni bir serbest metin faturası oluşturulur ve bu faturadaki değerleri düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5716-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


