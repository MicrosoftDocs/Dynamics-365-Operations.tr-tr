---
title: Tahsilat mektuplarını işleme örneği
description: Bu konu, Tahsilat mektuplarının oluşturulması, yazdırılması ve deftere nakledilmesi sürecini gösteren bir örnek sunar.
author: JodiChristiansen
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 1b80532463d86dd59b867fca2ee24675396ce717
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826359"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="9db7a-103">Tahsilat mektuplarını işleme örneği</span><span class="sxs-lookup"><span data-stu-id="9db7a-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9db7a-104">Bu konu, Tahsilat mektuplarının oluşturulması, yazdırılması ve deftere nakledilmesi sürecini gösteren bir örnek sunar.</span><span class="sxs-lookup"><span data-stu-id="9db7a-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="9db7a-105">Bu örnek, alacak ve tahsilatlardaki **tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneğini temel alır.</span><span class="sxs-lookup"><span data-stu-id="9db7a-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="9db7a-106">USMF demo şirketinde bulunan verileri ve yeni bir müşteri olan US-045'i kullanır.</span><span class="sxs-lookup"><span data-stu-id="9db7a-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="9db7a-107">Başlamak için **Alacak hesapları \> müşteriler \> tüm müşteriler**'e gidin, **Yeni**'yi seçin ve sonra müşteri US-045'i oluşturmak için gerekli bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="9db7a-108">Bitirdiğinizde aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="9db7a-109">**Alacak ve tahsilatlar \> tahsilat mektubu \> Tahsilat mektubu sırasına ayarla**'ya gidin  ve tahsilat mektubu sırasını, müşteri deftere nakil profiline atanan aşağıdaki tabloda gösterildiği şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9db7a-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="9db7a-110">Tahsilat mektubu kodu</span><span class="sxs-lookup"><span data-stu-id="9db7a-110">Collection   letter code</span></span>      |     <span data-ttu-id="9db7a-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="9db7a-111">Description</span></span>                           |     <span data-ttu-id="9db7a-112">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="9db7a-112">Currency</span></span>      |     <span data-ttu-id="9db7a-113">Ana hesap</span><span class="sxs-lookup"><span data-stu-id="9db7a-113">Main   account</span></span>        |     <span data-ttu-id="9db7a-114">Para birimi cinsinden ücret</span><span class="sxs-lookup"><span data-stu-id="9db7a-114">Fee   in currency</span></span>     |     <span data-ttu-id="9db7a-115">En az</span><span class="sxs-lookup"><span data-stu-id="9db7a-115">Minimum   over</span></span>        |     <span data-ttu-id="9db7a-116">Bloklanan gün sayısı</span><span class="sxs-lookup"><span data-stu-id="9db7a-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="9db7a-117">Tahsilat mektubu 1</span><span class="sxs-lookup"><span data-stu-id="9db7a-117">Collection   letter 1</span></span>         |     <span data-ttu-id="9db7a-118">Ücretli ikinci bildirim</span><span class="sxs-lookup"><span data-stu-id="9db7a-118">Second   notification with fee</span></span>        |     <span data-ttu-id="9db7a-119">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="9db7a-119">USD</span></span>           |                           |     <span data-ttu-id="9db7a-120">0,00</span><span class="sxs-lookup"><span data-stu-id="9db7a-120">0.00</span></span>                  |     <span data-ttu-id="9db7a-121">0,00</span><span class="sxs-lookup"><span data-stu-id="9db7a-121">0.00</span></span>                  |     <span data-ttu-id="9db7a-122">2</span><span class="sxs-lookup"><span data-stu-id="9db7a-122">2</span></span>                 |
|     <span data-ttu-id="9db7a-123">Tahsilat mektubu 2</span><span class="sxs-lookup"><span data-stu-id="9db7a-123">Collection   letter 2</span></span>         |     <span data-ttu-id="9db7a-124">Ücretli ikinci bildirim</span><span class="sxs-lookup"><span data-stu-id="9db7a-124">Second   notification with fee</span></span>        |     <span data-ttu-id="9db7a-125">USC</span><span class="sxs-lookup"><span data-stu-id="9db7a-125">USC</span></span>           |     <span data-ttu-id="9db7a-126">403150</span><span class="sxs-lookup"><span data-stu-id="9db7a-126">403150</span></span>                |     <span data-ttu-id="9db7a-127">20.00</span><span class="sxs-lookup"><span data-stu-id="9db7a-127">20.00</span></span>                 |     <span data-ttu-id="9db7a-128">10,00</span><span class="sxs-lookup"><span data-stu-id="9db7a-128">10.00</span></span>                 |     <span data-ttu-id="9db7a-129">3</span><span class="sxs-lookup"><span data-stu-id="9db7a-129">3</span></span>                 |
|     <span data-ttu-id="9db7a-130">Tahsilat</span><span class="sxs-lookup"><span data-stu-id="9db7a-130">Collection</span></span>                    |     <span data-ttu-id="9db7a-131">Ücretli son bildirim</span><span class="sxs-lookup"><span data-stu-id="9db7a-131">Final   notification with fee</span></span>         |     <span data-ttu-id="9db7a-132">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="9db7a-132">USD</span></span>           |     <span data-ttu-id="9db7a-133">403150</span><span class="sxs-lookup"><span data-stu-id="9db7a-133">403150</span></span>                |     <span data-ttu-id="9db7a-134">50.00</span><span class="sxs-lookup"><span data-stu-id="9db7a-134">50.00</span></span>                 |     <span data-ttu-id="9db7a-135">100.00</span><span class="sxs-lookup"><span data-stu-id="9db7a-135">100.00</span></span>                |     <span data-ttu-id="9db7a-136">15</span><span class="sxs-lookup"><span data-stu-id="9db7a-136">15</span></span>                |

<span data-ttu-id="9db7a-137">Aşağıdaki resimde tabloda gösterilen bilgiler, **tahsilat mektupları** sayfasında görüneceği şekilde gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9db7a-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="9db7a-138">[![Tahsilat mektubu sırası ayarlama](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="9db7a-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="9db7a-139">Şimdi bu örnek için gereken iki parametreyi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9db7a-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="9db7a-140">**Alacak ve tahsilatlar \> Kurulum \> Alacak hesabı parametreleri**'ne gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9db7a-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="9db7a-141">**Tahsilatlar** sekmesinde **tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9db7a-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="9db7a-142">**Her seferinde tahsilat mektubu oluştur** alanının **Müşteri** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="9db7a-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="9db7a-143">[![Alacak Tahsilatları için alacak hesapları parametreleri ayarlama](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="9db7a-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="9db7a-144">**Alacak hesapları \> faturalar \> Tüm serbest metin faturaları** kısmına gidin, **Yeni**'yi seçin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9db7a-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="9db7a-145">**Müşteri hesabı** alanında **US-045**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="9db7a-146">**Fatura tarihi** alanına **1/15/2021** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="9db7a-147">**Son tarih** alanına **1/16/2021** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="9db7a-148">**Fatura satırları** hızlı sekmesinde, **ana hesap** alanına **401100** girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="9db7a-149">**Birim fiyatı** alanına **500.00** yazın.</span><span class="sxs-lookup"><span data-stu-id="9db7a-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="9db7a-150">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-150">Select **Post**.</span></span>

    <span data-ttu-id="9db7a-151">Şimdi müşteri için iki alacak dekontu girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9db7a-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="9db7a-152">**Yeni**'yi seçin ve ardından aşağıdaki adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9db7a-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="9db7a-153">**Müşteri hesabı** alanında **US-045**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="9db7a-154">**Fatura tarihi** alanına **1/15/2021** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="9db7a-155">**Son tarih** alanına **1/16/2021** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="9db7a-156">**Fatura satırları** hızlı sekmesinde, **ana hesap** alanına **401100** girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="9db7a-157">**Birim fiyatı** alanına **-100,00** yazın.</span><span class="sxs-lookup"><span data-stu-id="9db7a-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="9db7a-158">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-158">Select **Post**.</span></span>

5. <span data-ttu-id="9db7a-159">4. adımı yineleyin, ancak **birim fiyat** alanına **-200,00** girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="9db7a-160">**Alacak hesapları \>müşteriler \> tüm müşteriler**'e gidin ve müşteri **US-045**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="9db7a-161">Sonra, eylem bölmesinde, daha önce deftere naklettiğiniz müşteri işlemlerini gözden geçirmek üzere **İşlemler \> İşlemler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="9db7a-162">[![Deftere nakledilen müşteri işlemlerini gözden geçirme](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="9db7a-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="9db7a-163">Şimdi müşteri US-045 için tahsilat mektupları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9db7a-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="9db7a-164">**Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını oluştur**'a gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9db7a-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="9db7a-165">**Fatura** ve **alacak dekontu** seçeneklerini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9db7a-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="9db7a-166">Varsayılan olarak, **tahsilat mektubu** alanı **müşteri başına tahsilat** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9db7a-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="9db7a-167">**Tahsilat mektubu tarihi** alanına **1/19/2021** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="9db7a-168">**Dahil edilecek kayıtlar** hızlı sekmesinde, **filtre**'yi seçin ve **müşteri hesabı** alanına, müşteri **US-045**'i ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="9db7a-169">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-169">Select **OK**.</span></span>
    5. <span data-ttu-id="9db7a-170">Tahsilat mektupları oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="9db7a-171">**Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını incele ve işle**'ye gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9db7a-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="9db7a-172">Bu tahsilat mektubu dizideki ilk tahsilat mektubu olduğundan, hem başlık, hem işlem satırlarında tahsilat mektubu kodunun **tahsilat mektubu 1** olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="9db7a-173">(İşlem satırlarını görüntülemek için, **İşlemler** Hızlı sekmesini seçmeniz gerekebilir.)</span><span class="sxs-lookup"><span data-stu-id="9db7a-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="9db7a-174">[![Başlıkta ve satırlarda aynı tahsilat mektubu kodunun göründüğünü doğrulama](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="9db7a-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="9db7a-175">Eylem Bölmesinde **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="9db7a-176">**Deftere nakletme tarihi** alanına **1/19/2021** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="9db7a-177">Şimdi müşteri US-045 için tahsilat mektuplarını tekrar oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9db7a-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="9db7a-178">**Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını oluştur**'a gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9db7a-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="9db7a-179">**Fatura** ve **alacak dekontu** seçeneklerini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9db7a-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="9db7a-180">Varsayılan olarak, **tahsilat mektubu** alanı **müşteri başına tahsilat** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9db7a-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="9db7a-181">**Tahsilat mektubu tarihi** alanına **1/23/2021** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="9db7a-182">**Dahil edilecek kayıtlar** hızlı sekmesinde, **filtre**'yi seçin ve **müşteri hesabı** alanına, müşteri **US-045**'i ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="9db7a-183">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-183">Select **OK**.</span></span>
    5. <span data-ttu-id="9db7a-184">Tahsilat mektupları oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="9db7a-185">**Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını incele ve işle**'ye gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9db7a-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="9db7a-186">Başlıktaki tahsilat mektubu kodunun **tahsilat mektubu 1** olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="9db7a-187">Ancak, işlem satırlarındaki kod **Tahsilat mektubu 2**'dir.</span><span class="sxs-lookup"><span data-stu-id="9db7a-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="9db7a-188">[![Başlıkta ve satırlarda farklı tahsilat mektubu kodlarının göründüğünü doğrular](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="9db7a-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="9db7a-189">**Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneği **Evet** olarak ayarlandığı için kodlar farklıdır.</span><span class="sxs-lookup"><span data-stu-id="9db7a-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="9db7a-190">Bu Tahsilat mektubunu deftere nakletmeyin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="9db7a-191">**Alacak ve tahsilatlar \> Kurulum \> Alacak hesapları parametrelerine** gidin ve ardından **Tahsilatlar** sekmesinde, **tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9db7a-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="9db7a-192">[![Tahsilat mektubu kodunu hesaplarken için ödemeleri ve alacak notlarını yoksayma seçeneğini Hayır olarak ayarlama](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="9db7a-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="9db7a-193">Şimdi müşteri US-045 için tahsilat mektuplarını tekrar oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9db7a-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="9db7a-194">**Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını oluştur**'a gidin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="9db7a-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="9db7a-195">**Fatura** ve **alacak dekontu** seçeneklerini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9db7a-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="9db7a-196">Varsayılan olarak, **tahsilat mektubu** alanı **müşteri başına tahsilat** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9db7a-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="9db7a-197">**Tahsilat mektubu tarihi** alanına **1/23/2021** tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="9db7a-198">**Dahil edilecek kayıtlar** hızlı sekmesinde, **filtre**'yi seçin ve **müşteri hesabı** alanına, müşteri **US-045**'i ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="9db7a-199">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-199">Select **OK**.</span></span>
    5. <span data-ttu-id="9db7a-200">Tahsilat mektupları oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="9db7a-201">**Alacak ve tahsilatlar \> Tahsilat mektubu \> Tahsilat mektuplarını gözden geçir ve izle** bölümüne gidin ve hem başlık, hem işlem satırlarında tahsilat mektubu kodunun **tahsilat mektubu 2** olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="9db7a-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="9db7a-202">[![Başlıkta ve satırlarda aynı tahsilat mektubu kodunun olduğunu tekrar gösterme](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="9db7a-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="9db7a-203">**Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** seçeneği şimdi **Hayır** olarak ayarlandığı için her iki yerde de aynı kod görünür.</span><span class="sxs-lookup"><span data-stu-id="9db7a-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
