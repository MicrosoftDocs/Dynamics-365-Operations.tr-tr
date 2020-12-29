---
title: Serbest metin faturası oluşturma
description: Bu konuda, serbest metin faturalarının nasıl oluşturulacağı açıklanmaktadır.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 1ac06e7d702ffe3a8cdb6bd2823f2ffdc055c722
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448681"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="c7939-103">Serbest metin faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="c7939-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7939-104">Bu konuda, serbest metin faturalarının nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c7939-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="c7939-105">Prosedür için **USMF** demo şirketini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c7939-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="c7939-106">Serbest metin faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="c7939-106">Create a free text invoice</span></span>

1. <span data-ttu-id="c7939-107">**Alacak hesapları \> Faturalar \> Tüm serbest metin faturaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="c7939-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="c7939-108">**Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-108">Select **New**.</span></span>
3. <span data-ttu-id="c7939-109">**Müşteri hesabı** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="c7939-110">Varsayılan olarak müşteri hesabı olarak seçilen hesap fatura hesabı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7939-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="c7939-111">Fatura deftere nakledilmediyse muhasebe durumunun başlangıç değeri **İşlemde** olur.</span><span class="sxs-lookup"><span data-stu-id="c7939-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="c7939-112">Fatura numarası fatura deftere nakledildiğinde atanır.</span><span class="sxs-lookup"><span data-stu-id="c7939-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="c7939-113">Tek Euro Ödemeleri Alanı (SEPA) yönergelerini kullanıyorsanız otomatik ödeme yönergesi müşteri hesabını seçtiğinizde otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="c7939-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="c7939-114">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c7939-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="c7939-115">**Ana hesap** alanında, boyutları olmayan bir hesap numarası belirtin.</span><span class="sxs-lookup"><span data-stu-id="c7939-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="c7939-116">Boyutları bu konunun ilerleyen bölümlerinde gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="c7939-117">Ayrıca ana hesap için bir veya daha fazla karakter girebilir ve hesabı bulmak için arama özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="c7939-118">Ana hesaba boyutlar eklemek için **Satır ayrıntıları** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="c7939-119">**Mali boyutlar satırı** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="c7939-120">Boyutlar yalnızca seçilen satır için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7939-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="c7939-121">Satış vergisi grubu, müşteriden doldurulur.</span><span class="sxs-lookup"><span data-stu-id="c7939-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="c7939-122">Müşterinin satış vergisi grubu yoksa ana hesaptan alınan satış vergisi grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7939-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="c7939-123">Madde satış vergisi grubu ana hesaptan doldurulur.</span><span class="sxs-lookup"><span data-stu-id="c7939-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="c7939-124">Ana hesapta madde satış vergisi grubu yoksa, Genel muhasebe satış vergisi parametrelerinde belirtilen madde satış vergisi grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c7939-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="c7939-125">İsteğe bağlı: **Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c7939-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="c7939-126">İsteğe bağlı: **Birim fiyatı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c7939-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="c7939-127">Tutar, miktarla birim fiyatı çarpılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="c7939-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="c7939-128">Ancak kendiniz bir tutar girerek hesabı geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="c7939-129">Fatura için hesaplanan satış vergisini görüntülemek için **Satış vergisi** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="c7939-130">Bu sayfada satış vergisi tutarlarını görüntüleyebilir veya **Ayarlama** sekmesinde tutarları geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="c7939-131">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-131">Select **OK**.</span></span>
12. <span data-ttu-id="c7939-132">Faturanıza masraf eklemek için **Masraflar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="c7939-133">**Masraf kodu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c7939-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="c7939-134">**Masraf değeri** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c7939-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="c7939-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c7939-135">Close the page.</span></span>
16. <span data-ttu-id="c7939-136">Fatura ayrıntılarının ve toplamların bir özetini görüntülemek için **Toplamlar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="c7939-137">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-137">Select **Close**.</span></span>
18. <span data-ttu-id="c7939-138">Faturayı deftere nakletmek için **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="c7939-139">Gerçekte deftere nakletmeden önce iptal etme olanağınız vardır.</span><span class="sxs-lookup"><span data-stu-id="c7939-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="c7939-140">Fatura yazdırmanın zamanlamasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="c7939-141">Her faturayı güncelleştirildiğinde yazdırmak için **Geçerli**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="c7939-142">Tüm faturalar güncelleştirildikten sonra yazdırmak için **Sonra**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="c7939-143">Fatura deftere nakledilmeden önce müşterinin kredi limitinin doğrulama yöntemini değiştirmek için **Kredi limiti türü** alanındaki değeri değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c7939-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="c7939-144">Faturayı yazdırmak için seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c7939-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="c7939-145">Faturayı deftere nakletmek için seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c7939-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="c7939-146">Faturayı nakletmeden yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="c7939-147">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c7939-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="c7939-148">Satırları kopyala</span><span class="sxs-lookup"><span data-stu-id="c7939-148">Copy lines</span></span>
<span data-ttu-id="c7939-149">Serbest metin faturasında satırları kopyalamak için bir veya birden fazla satırı seçin ve **Seçili satırları kopyala** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="c7939-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="c7939-150">Alınacak kopya sayısını belirtebilir, notları ve ekleri de kopyalayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="c7939-151">Dağıtımları kopyalayabilir veya deftere naklederken yeniden oluşturulmalarına izin verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="c7939-152">Satırları kopyaladıktan sonra bilgilerde ihtiyacınız olan düzenlemeleri yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="c7939-153">Şablondan serbest metin faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="c7939-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="c7939-154">Şablondan serbest metin faturası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="c7939-155">**Fatura** sekmesinde **Şablondan yeni** öğesini seçtiğinizde yeni serbest metin faturası için bir şablon adı ve müşterinin hesabını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="c7939-156">Müşterinin ödeme yöntemi ve ödeme koşulları gibi varsayılan değerler, müşteriden otomatik olarak doldurulabilir veya şablonda kaydedilmiş değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="c7939-157">Yeni bir serbest metin faturası oluşturulur ve ihtiyacınız olan değerleri düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7939-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
