--- 
title: "Serbest metin faturaları oluştur"
description: "Bu konuda, serbest metin faturalarının nasıl oluşturulacağı açıklanmaktadır."
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: f64292a1b3726ea9b43f959a44c4ed2a1f392484
ms.openlocfilehash: f6ee6fda0b52b8af7c253b7d22e470345a8a421f
ms.contentlocale: tr-tr
ms.lasthandoff: 09/05/2018

---

# <a name="create-free-text-invoices"></a><span data-ttu-id="a923a-103">Serbest metin faturaları oluştur</span><span class="sxs-lookup"><span data-stu-id="a923a-103">Create free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a923a-104">Bu konuda, serbest metin faturalarının nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a923a-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="a923a-105">Prosedür için **USMF** demo şirketini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a923a-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="a923a-106">Serbest metin faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="a923a-106">Create a free text invoice</span></span>

1. <span data-ttu-id="a923a-107">**Alacak hesapları \> Faturalar \> Tüm serbest metin faturaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a923a-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="a923a-108">**Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-108">Select **New**.</span></span>
3. <span data-ttu-id="a923a-109">**Müşteri hesabı** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="a923a-110">Varsayılan olarak müşteri hesabı olarak seçilen hesap fatura hesabı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a923a-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="a923a-111">Fatura deftere nakledilmediyse muhasebe durumunun başlangıç değeri **İşlemde** olur.</span><span class="sxs-lookup"><span data-stu-id="a923a-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="a923a-112">Fatura numarası fatura deftere nakledildiğinde atanır.</span><span class="sxs-lookup"><span data-stu-id="a923a-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="a923a-113">Tek Euro Ödemeleri Alanı (SEPA) yönergelerini kullanıyorsanız otomatik ödeme yönergesi müşteri hesabını seçtiğinizde otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="a923a-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="a923a-114">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a923a-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="a923a-115">**Ana hesap** alanında, boyutları olmayan bir hesap numarası belirtin.</span><span class="sxs-lookup"><span data-stu-id="a923a-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="a923a-116">Boyutları bu konunun ilerleyen bölümlerinde gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="a923a-117">Ayrıca ana hesap için bir veya daha fazla karakter girebilir ve hesabı bulmak için arama özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="a923a-118">Ana hesaba boyutlar eklemek için **Satır ayrıntıları** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="a923a-119">**Mali boyutlar satırı** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="a923a-120">Boyutlar yalnızca seçilen satır için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a923a-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="a923a-121">Satış vergisi grubu, müşteriden doldurulur.</span><span class="sxs-lookup"><span data-stu-id="a923a-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="a923a-122">Müşterinin satış vergisi grubu yoksa ana hesaptan alınan satış vergisi grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a923a-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="a923a-123">Madde satış vergisi grubu ana hesaptan doldurulur.</span><span class="sxs-lookup"><span data-stu-id="a923a-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="a923a-124">Ana hesapta madde satış vergisi grubu yoksa, Genel muhasebe satış vergisi parametrelerinde belirtilen madde satış vergisi grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a923a-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="a923a-125">İsteğe bağlı: **Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a923a-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="a923a-126">İsteğe bağlı: **Birim fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a923a-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="a923a-127">Tutar, miktarla birim fiyatı çarpılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a923a-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="a923a-128">Ancak kendiniz bir tutar girerek hesabı geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="a923a-129">Fatura için hesaplanan satış vergisini görüntülemek için **Satış vergisi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="a923a-130">Bu sayfada satış vergisi tutarlarını görüntüleyebilir veya **Ayarlama** sekmesinde tutarları geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="a923a-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-131">Select **OK**.</span></span>
12. <span data-ttu-id="a923a-132">Faturanıza masraf eklemek için **Masraflar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="a923a-133">**Masraf kodu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a923a-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="a923a-134">**Masraf değeri** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a923a-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="a923a-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a923a-135">Close the page.</span></span>
16. <span data-ttu-id="a923a-136">Fatura ayrıntılarının ve toplamların bir özetini görüntülemek için **Toplamlar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="a923a-137">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-137">Select **Close**.</span></span>
18. <span data-ttu-id="a923a-138">Faturayı deftere nakletmek için **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="a923a-139">Gerçekte deftere nakletmeden önce iptal etme olanağınız vardır.</span><span class="sxs-lookup"><span data-stu-id="a923a-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="a923a-140">Fatura yazdırmanın zamanlamasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="a923a-141">Her faturayı güncelleştirildiğinde yazdırmak için **Geçerli**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="a923a-142">Tüm faturalar güncelleştirildikten sonra yazdırmak için **Sonra**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="a923a-143">Fatura deftere nakledilmeden önce müşterinin kredi limitinin doğrulama yöntemini değiştirmek için **Kredi limiti türü** alanındaki değeri değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a923a-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="a923a-144">Faturayı yazdırmak için seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a923a-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="a923a-145">Faturayı deftere nakletmek için seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a923a-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="a923a-146">Faturayı nakletmeden yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="a923a-147">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a923a-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="a923a-148">Satırları kopyala</span><span class="sxs-lookup"><span data-stu-id="a923a-148">Copy lines</span></span>
<span data-ttu-id="a923a-149">Serbest metin faturasında satırları kopyalamak için bir veya birden fazla satırı seçin ve **Seçili satırları kopyala** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a923a-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="a923a-150">Alınacak kopya sayısını belirtebilir, notları ve ekleri de kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="a923a-151">Dağıtımları kopyalayabilir veya deftere naklederken yeniden oluşturulmalarına izin verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="a923a-152">Satırları kopyaladıktan sonra bilgilerde ihtiyacınız olan düzenlemeleri yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="a923a-153">Şablondan serbest metin faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="a923a-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="a923a-154">Şablondan serbest metin faturası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="a923a-155">**Fatura** sekmesinde **Şablondan yeni** öğesini seçtiğinizde yeni serbest metin faturası için bir şablon adı ve müşterinin hesabını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="a923a-156">Müşterinin ödeme yöntemi ve ödeme koşulları gibi varsayılan değerler, müşteriden otomatik olarak doldurulabilir veya şablonda kaydedilmiş değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="a923a-157">Yeni bir serbest metin faturası oluşturulur ve ihtiyacınız olan değerleri düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a923a-157">A new free text invoice is created, and you can edit the values as you require.</span></span>

