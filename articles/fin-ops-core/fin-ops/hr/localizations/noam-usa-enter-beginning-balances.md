---
title: Bordro başlangıç bakiyelerini girin
description: Bu konu kazanç kodları, kesintiler, kazançlar ve vergiler girmek için gerekli adımları anlatır. Bu bilgiler, İş ortaklarının veriyi bir sistemden yeni bir Bordro uygulama sistemine taşıması veya aktarması için kullanışlıdır.
author: kherr75
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cab844e190140d2c3b605c9a1490d33a6f383ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180457"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="cb33d-104">Bordro başlangıç bakiyelerini girin</span><span class="sxs-lookup"><span data-stu-id="cb33d-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cb33d-105">Bu konu kazanç kodları, kesintiler, kazançlar ve vergiler girmek için gerekli adımları anlatır.</span><span class="sxs-lookup"><span data-stu-id="cb33d-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="cb33d-106">Bu bilgiler, veriyi bir sistemden yeni bir Bordro uygulama sistemine taşıması veya aktaran ortaklar için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="cb33d-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="cb33d-107">Bordro bakiyelerini girmeye hazırlanmak için aşağıdaki bilgileri doğrularız:</span><span class="sxs-lookup"><span data-stu-id="cb33d-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="cb33d-108">Personel kayıtlarının sisteme girilmiş ve kullanılabilir olması</span><span class="sxs-lookup"><span data-stu-id="cb33d-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="cb33d-109">Aşağıdaki verinin personele ayarlanmış ve atanmış olması:</span><span class="sxs-lookup"><span data-stu-id="cb33d-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="cb33d-110">Ödeme döngüleri ve ödeme dönemleri</span><span class="sxs-lookup"><span data-stu-id="cb33d-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="cb33d-111">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="cb33d-111">Earning codes</span></span>
    - <span data-ttu-id="cb33d-112">Vergiler</span><span class="sxs-lookup"><span data-stu-id="cb33d-112">Taxes</span></span>
    - <span data-ttu-id="cb33d-113">Kazançlar ve kesintiler</span><span class="sxs-lookup"><span data-stu-id="cb33d-113">Benefits and deductions</span></span>

- <span data-ttu-id="cb33d-114">Şirket, bordro başlangıç bakiyelerinin ayarlanabileceği bir tarih seçmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cb33d-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="cb33d-115">Bilgi, tüm kazançlardan, kazanç/kesintilerden, kazanç katkılarından, personel vergilerinden ve işveren vergileriyle onların eski sistemden YTD tutarlarından toplanmıştır.</span><span class="sxs-lookup"><span data-stu-id="cb33d-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="cb33d-116">Başlangıç bakiyelerini girmeyi planladığınızda, verinin ne kadar ayrıntılı olması gerektiğini göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="cb33d-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="cb33d-117">Çoğu işletme tek bir birleştirilmiş yılbaşından bugüne tutarını girer</span><span class="sxs-lookup"><span data-stu-id="cb33d-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="cb33d-118">Ancak, daha ayrıntılı bilgi gerekiyorsa, bakiyeler üç aylık aralıklarla girilebilir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="cb33d-119">Gerekli olan ayrıntı seviyesine karar vermek, her bir çalışan için kaç adet el ile ödeme ekstresinin oluşturulması gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="cb33d-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="cb33d-120">Tek bir yılbaşından bugüne tutarı için her bir çalışana yalnızca bir el ile ekstre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="cb33d-121">Bunu yapmak için önceki sistemden son ödeme ekstresinin yılbaşından bugüne tutarını, yeni bordro sisteminde girilen tutar olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="cb33d-122">Aşağıdaki örnek kazanç kodları, kazançlar, kesintiler ve vergiler de dahil personel bordro başlangıç bakiyelerini nasıl girebileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="cb33d-123">Bir gerçek dünya örneğinde, her bir kazanç kodu, kazanç kesintisi, kazanç katkısı, personel vergisi ve işveren vergisi için yılbaşından bugüne tutarında girilen tutar satır öğesine sahip olacaksınız.</span><span class="sxs-lookup"><span data-stu-id="cb33d-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="cb33d-124">Kodların ve tutarların bu listesini kullanarak, başlangıç bakiyelerini bordo amacıyla getirmek için muhasebe devre dışıyken bir el ile ödeme ve maaş ekstresini oluşturmak için izleyin.</span><span class="sxs-lookup"><span data-stu-id="cb33d-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="cb33d-125">Başlangıç bakiyesi ödeme ekstresini genel muhasebe defterinize nakletmek istemediğiniz için muhasebeyi devre dışı bırakırsınız.</span><span class="sxs-lookup"><span data-stu-id="cb33d-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="cb33d-126">Bu eski sistemde yapılmıştır ve Genel muhasebede başlangıç bakiyelerini ayarladığınızda gelecektir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="cb33d-127">A.</span><span class="sxs-lookup"><span data-stu-id="cb33d-127">A.</span></span> <span data-ttu-id="cb33d-128">Bordro başlangıç bakiyelerinde kullanılacak kazanç kodlarının ayarlanması</span><span class="sxs-lookup"><span data-stu-id="cb33d-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="cb33d-129">Bordro başlangıç bakiyeleri girdiğinizde, kullanacağınız kazanç kodlarının "Kazanç ekstresi oranlarının düzenlenmesine izin ver" seçeneği etkin olarak yapılandırılmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="cb33d-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="cb33d-130">Bu, eski sistemden tutarı el ile girmenize izin verecektir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="cb33d-131">B.</span><span class="sxs-lookup"><span data-stu-id="cb33d-131">B.</span></span> <span data-ttu-id="cb33d-132">Bir personelin bir başlangıç bakiyesine sahip olması için kazanç ekstreleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="cb33d-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="cb33d-133">Bu adım, eski sistemin son gün dönemi için, her bir çalışana bir kazanç ekstresini el ile yaratır ve bu da yeni bordro sisteminde kazanç ekstresi satırlarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb33d-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="cb33d-134">Kazanç kodu başına bir satır ve YTD tutarını ve saatlerini girin.</span><span class="sxs-lookup"><span data-stu-id="cb33d-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="cb33d-135">Örnek adımlar aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="cb33d-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="cb33d-136">**Tüm kazançlar ekstreleri** sayfasını açın ve **Yeni** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="cb33d-137">Aşağıdakileri girin:</span><span class="sxs-lookup"><span data-stu-id="cb33d-137">Enter the following:</span></span> 

    | <span data-ttu-id="cb33d-138">Alan</span><span class="sxs-lookup"><span data-stu-id="cb33d-138">Field</span></span>      | <span data-ttu-id="cb33d-139">Değer</span><span class="sxs-lookup"><span data-stu-id="cb33d-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="cb33d-140">Çalışan</span><span class="sxs-lookup"><span data-stu-id="cb33d-140">Worker</span></span>     | <span data-ttu-id="cb33d-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="cb33d-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="cb33d-142">Ödeme döngüsü</span><span class="sxs-lookup"><span data-stu-id="cb33d-142">Pay cycle</span></span>  | <span data-ttu-id="cb33d-143">sm</span><span class="sxs-lookup"><span data-stu-id="cb33d-143">sm</span></span>                    |
    | <span data-ttu-id="cb33d-144">Ödeme dönemi</span><span class="sxs-lookup"><span data-stu-id="cb33d-144">Pay period</span></span> | <span data-ttu-id="cb33d-145">16/06/2017- 30/06/2017</span><span class="sxs-lookup"><span data-stu-id="cb33d-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="cb33d-146">**Kazanç ekstre satırı** sekmesinde aşağıdakini girin:</span><span class="sxs-lookup"><span data-stu-id="cb33d-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="cb33d-147">Satır 1: **Kazanç ekstre satırı** sekmesi</span><span class="sxs-lookup"><span data-stu-id="cb33d-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="cb33d-148">Alan</span><span class="sxs-lookup"><span data-stu-id="cb33d-148">Field</span></span>            | <span data-ttu-id="cb33d-149">Değer</span><span class="sxs-lookup"><span data-stu-id="cb33d-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="cb33d-150">Kazançlar kodu</span><span class="sxs-lookup"><span data-stu-id="cb33d-150">Earnings code</span></span>    | <span data-ttu-id="cb33d-151">Düzenli ödeme</span><span class="sxs-lookup"><span data-stu-id="cb33d-151">Regular pay</span></span> |
    | <span data-ttu-id="cb33d-152">Miktar</span><span class="sxs-lookup"><span data-stu-id="cb33d-152">Quantity</span></span>         | <span data-ttu-id="cb33d-153">1.00</span><span class="sxs-lookup"><span data-stu-id="cb33d-153">1.00</span></span>        |
    | <span data-ttu-id="cb33d-154">Ücret</span><span class="sxs-lookup"><span data-stu-id="cb33d-154">Rate</span></span>             | <span data-ttu-id="cb33d-155">30,000</span><span class="sxs-lookup"><span data-stu-id="cb33d-155">30,000</span></span>      |
    | <span data-ttu-id="cb33d-156">Satır ayrıntıları sekmesi</span><span class="sxs-lookup"><span data-stu-id="cb33d-156">Line details tab</span></span> |             |
    | <span data-ttu-id="cb33d-157">El ile</span><span class="sxs-lookup"><span data-stu-id="cb33d-157">Manual</span></span>           | <span data-ttu-id="cb33d-158">(işaretli)</span><span class="sxs-lookup"><span data-stu-id="cb33d-158">(marked)</span></span>    |

    <span data-ttu-id="cb33d-159">Satır 2: **Kazanç ekstre satırı** sekmesi</span><span class="sxs-lookup"><span data-stu-id="cb33d-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="cb33d-160">Alan</span><span class="sxs-lookup"><span data-stu-id="cb33d-160">Field</span></span>            | <span data-ttu-id="cb33d-161">Değer</span><span class="sxs-lookup"><span data-stu-id="cb33d-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="cb33d-162">Kazançlar kodu</span><span class="sxs-lookup"><span data-stu-id="cb33d-162">Earnings code</span></span>    | <span data-ttu-id="cb33d-163">Prim</span><span class="sxs-lookup"><span data-stu-id="cb33d-163">Bonus</span></span>    |
    | <span data-ttu-id="cb33d-164">Miktar</span><span class="sxs-lookup"><span data-stu-id="cb33d-164">Quantity</span></span>         | <span data-ttu-id="cb33d-165">1,0000</span><span class="sxs-lookup"><span data-stu-id="cb33d-165">1.0000</span></span>   |
    | <span data-ttu-id="cb33d-166">Ücret</span><span class="sxs-lookup"><span data-stu-id="cb33d-166">Rate</span></span>             | <span data-ttu-id="cb33d-167">4250,00</span><span class="sxs-lookup"><span data-stu-id="cb33d-167">4250.00</span></span>  |
    | <span data-ttu-id="cb33d-168">Satır ayrıntıları sekmesi</span><span class="sxs-lookup"><span data-stu-id="cb33d-168">Line details tab</span></span> |          |
    | <span data-ttu-id="cb33d-169">El ile</span><span class="sxs-lookup"><span data-stu-id="cb33d-169">Manual</span></span>           | <span data-ttu-id="cb33d-170">(işaretli)</span><span class="sxs-lookup"><span data-stu-id="cb33d-170">(marked)</span></span> |

    <span data-ttu-id="cb33d-171">Satır 3: **Kazanç ekstre satırı** sekmesi</span><span class="sxs-lookup"><span data-stu-id="cb33d-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="cb33d-172">Alan</span><span class="sxs-lookup"><span data-stu-id="cb33d-172">Field</span></span>           | <span data-ttu-id="cb33d-173">Değer</span><span class="sxs-lookup"><span data-stu-id="cb33d-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="cb33d-174">Kazançlar kodu</span><span class="sxs-lookup"><span data-stu-id="cb33d-174">Earnings code</span></span>   | <span data-ttu-id="cb33d-175">Komisyon</span><span class="sxs-lookup"><span data-stu-id="cb33d-175">Commission</span></span> |
    | <span data-ttu-id="cb33d-176">Miktar</span><span class="sxs-lookup"><span data-stu-id="cb33d-176">Quantity</span></span>        | <span data-ttu-id="cb33d-177">1,0000</span><span class="sxs-lookup"><span data-stu-id="cb33d-177">1.0000</span></span>     |
    | <span data-ttu-id="cb33d-178">Ücret</span><span class="sxs-lookup"><span data-stu-id="cb33d-178">Rate</span></span>            | <span data-ttu-id="cb33d-179">!.299,00</span><span class="sxs-lookup"><span data-stu-id="cb33d-179">!,299.00</span></span>   |
    | <span data-ttu-id="cb33d-180">Ücret</span><span class="sxs-lookup"><span data-stu-id="cb33d-180">Rate</span></span>            | <span data-ttu-id="cb33d-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="cb33d-181">1,299.00</span></span>   |
    | <span data-ttu-id="cb33d-182">Satır ayrıntı sekmesi</span><span class="sxs-lookup"><span data-stu-id="cb33d-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="cb33d-183">El ile</span><span class="sxs-lookup"><span data-stu-id="cb33d-183">Manual</span></span>          | <span data-ttu-id="cb33d-184">(İşaretli)</span><span class="sxs-lookup"><span data-stu-id="cb33d-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="cb33d-185">**Satır Ayrıntıları** sekmesinde **El ile** kaydırıcısının ayarını her bir kazanç ekstre satırını için **Evet** olarak işaretlemek, her bir çalışan için bordro başlangıç bakiyelerinin girilmesini sağlamak için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="cb33d-186">**Eylem** bölmesinde, **Kazanç ekstrelerini serbest bırak** USA-FED-ER-FICA üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="cb33d-187">**Eylem** bölmesinde, **Ödeme ekstresi** üzerine tıklayarak **Ödeme ekstreleri oluştur** sayfasını açın ve aşağıdakileri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="cb33d-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="cb33d-188">Alan</span><span class="sxs-lookup"><span data-stu-id="cb33d-188">Field</span></span>              | <span data-ttu-id="cb33d-189">Değer</span><span class="sxs-lookup"><span data-stu-id="cb33d-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="cb33d-190">Ödeme tarihi</span><span class="sxs-lookup"><span data-stu-id="cb33d-190">Payment date</span></span>       | <span data-ttu-id="cb33d-191">30/06/2017</span><span class="sxs-lookup"><span data-stu-id="cb33d-191">6/30/2017</span></span> |
    | <span data-ttu-id="cb33d-192">Ödeme işlemi türü</span><span class="sxs-lookup"><span data-stu-id="cb33d-192">Payment run type</span></span>   | <span data-ttu-id="cb33d-193">El ile</span><span class="sxs-lookup"><span data-stu-id="cb33d-193">Manual</span></span>    |
    | <span data-ttu-id="cb33d-194">Muhasebeyi devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="cb33d-194">Disable accounting</span></span> |   <span data-ttu-id="cb33d-195">Evet</span><span class="sxs-lookup"><span data-stu-id="cb33d-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="cb33d-196">Bu, yalnızca ödeme yürütme türü el ile olduğunda ve kullanıcının ödeme çalıştırmasında muhasebeyi devre dışı bırakmak istediğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="cb33d-197">**Tamam** üzerine tıklayın ve **Bilgi günlüğü**'nü kapatın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="cb33d-198">Ödeme ekstreleri oluştururken Muhasebeyi Devre Dışı Bırak kaydırıcısı neden Evet olmalıdır?</span><span class="sxs-lookup"><span data-stu-id="cb33d-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="cb33d-199">Kaydırıcıyı **Evet** olarak ayarlamak, ödeme ekstresindeki satırların Genel muhasebeye dağıtılmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="cb33d-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="cb33d-200">Genel muhasebe tutarları, eski sistemden hesap bakiyeleri girildiğinde güncelleştirilmekteydi.</span><span class="sxs-lookup"><span data-stu-id="cb33d-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="cb33d-201">Bordro için başlangıç bakiyeleri girmek, önceki yıllardan bilgi içeren raporlar oluşturmanıza ve kazanç ve vergi amaçlı sınırlamaları belirlemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="cb33d-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="cb33d-202">C.</span><span class="sxs-lookup"><span data-stu-id="cb33d-202">C.</span></span> <span data-ttu-id="cb33d-203">Personeller için ödeme ekstreleri oluştur</span><span class="sxs-lookup"><span data-stu-id="cb33d-203">Create pay statements for employees</span></span>

<span data-ttu-id="cb33d-204">Başlangıç bakiyelerine sahip ödeme ekstreleri oluşturduktan sonra, ödeme ekstrelerinin bordro verisini doğru şekilde yansıttığını doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="cb33d-205">Kazanç ve vergi bilgisini de önceki bordro sistemindeki verilerle eşleşecek şekilde el ile güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="cb33d-206">Önceki bordro sisteminden tutarları, geçerli ödeme ekstrelerindeki tutarlarla eşleştiğini doğruladıktan sonra, ödeme ekstrelerini sonlandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="cb33d-207">**Tüm ödeme ekstreleri** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="cb33d-208">Michael Redmond için son oluşturulan ödeme ekstresini vurgulayın</span><span class="sxs-lookup"><span data-stu-id="cb33d-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="cb33d-209">**Ödeme ekstresi** sayfasını açmak için **Düzenle** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="cb33d-210">**Kazanç kesintileri** sekmesini açın ve aşağıdakini girin:</span><span class="sxs-lookup"><span data-stu-id="cb33d-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="cb33d-211">Alan</span><span class="sxs-lookup"><span data-stu-id="cb33d-211">Field</span></span>             | <span data-ttu-id="cb33d-212">Değer</span><span class="sxs-lookup"><span data-stu-id="cb33d-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="cb33d-213">Kazanç</span><span class="sxs-lookup"><span data-stu-id="cb33d-213">Benefit</span></span>           | <span data-ttu-id="cb33d-214">Kesinti tutarı</span><span class="sxs-lookup"><span data-stu-id="cb33d-214">Deduction amount</span></span> |
    | <span data-ttu-id="cb33d-215">401K</span><span class="sxs-lookup"><span data-stu-id="cb33d-215">401K</span></span>              | <span data-ttu-id="cb33d-216">Katıl</span><span class="sxs-lookup"><span data-stu-id="cb33d-216">Participate</span></span>      |
    | <span data-ttu-id="cb33d-217">Diş</span><span class="sxs-lookup"><span data-stu-id="cb33d-217">Dental</span></span>            | <span data-ttu-id="cb33d-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="cb33d-218">SubSp</span></span>            |
    | <span data-ttu-id="cb33d-219">Dep bakım harcaması</span><span class="sxs-lookup"><span data-stu-id="cb33d-219">Dep care spending</span></span> | <span data-ttu-id="cb33d-220">Katıl</span><span class="sxs-lookup"><span data-stu-id="cb33d-220">Participate</span></span>      |
    | <span data-ttu-id="cb33d-221">Görme</span><span class="sxs-lookup"><span data-stu-id="cb33d-221">Vision</span></span>            | <span data-ttu-id="cb33d-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="cb33d-222">SupSp</span></span>            |

5. <span data-ttu-id="cb33d-223">**Kazanç katkıları** sekmesinde aşağıdakileri girin:</span><span class="sxs-lookup"><span data-stu-id="cb33d-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="cb33d-224">Alan</span><span class="sxs-lookup"><span data-stu-id="cb33d-224">Field</span></span>   | <span data-ttu-id="cb33d-225">Değer</span><span class="sxs-lookup"><span data-stu-id="cb33d-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="cb33d-226">Kazanç</span><span class="sxs-lookup"><span data-stu-id="cb33d-226">Benefit</span></span> | <span data-ttu-id="cb33d-227">Katkı tutarı</span><span class="sxs-lookup"><span data-stu-id="cb33d-227">Contribution amount</span></span> |
    | <span data-ttu-id="cb33d-228">401K</span><span class="sxs-lookup"><span data-stu-id="cb33d-228">401K</span></span>    | <span data-ttu-id="cb33d-229">Katıl</span><span class="sxs-lookup"><span data-stu-id="cb33d-229">Participate</span></span>         |
    | <span data-ttu-id="cb33d-230">Diş</span><span class="sxs-lookup"><span data-stu-id="cb33d-230">Dental</span></span>  | <span data-ttu-id="cb33d-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="cb33d-231">SubSp</span></span>               |
    | <span data-ttu-id="cb33d-232">Görme</span><span class="sxs-lookup"><span data-stu-id="cb33d-232">Vision</span></span>  | <span data-ttu-id="cb33d-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="cb33d-233">SubSp</span></span>               |

6. <span data-ttu-id="cb33d-234">**Vergi kesintileri** sekmesinde aşağıdakileri girin:</span><span class="sxs-lookup"><span data-stu-id="cb33d-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="cb33d-235">Alan</span><span class="sxs-lookup"><span data-stu-id="cb33d-235">Field</span></span>           | <span data-ttu-id="cb33d-236">Değer</span><span class="sxs-lookup"><span data-stu-id="cb33d-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="cb33d-237">Vergi kodu.</span><span class="sxs-lookup"><span data-stu-id="cb33d-237">Tax code</span></span>        | <span data-ttu-id="cb33d-238">Kesinti tutarı</span><span class="sxs-lookup"><span data-stu-id="cb33d-238">Deduction amount</span></span> |
    | <span data-ttu-id="cb33d-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="cb33d-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="cb33d-240">1600,00</span><span class="sxs-lookup"><span data-stu-id="cb33d-240">1600.00</span></span>          |
    | <span data-ttu-id="cb33d-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="cb33d-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="cb33d-242">825,75</span><span class="sxs-lookup"><span data-stu-id="cb33d-242">825.75</span></span>           |

7. <span data-ttu-id="cb33d-243">**Vergi katkıları** sekmesinde aşağıdakileri girin:</span><span class="sxs-lookup"><span data-stu-id="cb33d-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="cb33d-244">**Hesapla** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="cb33d-245">Çalışan için ödeme ekstresi toplamlarının eski sistemin YTD'si ile eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="cb33d-246">Tüm ödeme ekstrelerinin toplamında bazı genel doğrulamalar gerçekleştirmek için sonraki adımda sonlandırmayı bekletmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb33d-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="cb33d-247">Doğrulandıktan sonra, tüm ödeme ekstreleri arasında çalıştırın ve onları sonlandırın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="cb33d-248">Aynı işlem gerek duyulursa, yıl içerisindeki tüm önceki çeyrekler için üç aylık aralıklarla yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="cb33d-249">Bu yalnızca müşterinin eski sisteme geri gitmeden veriyi üç alık olarak görmesi gerekiyorsa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="cb33d-250">Bir Personel için Başlangıç Bakiyelerini girerken bir hata yaptıysanız</span><span class="sxs-lookup"><span data-stu-id="cb33d-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="cb33d-251">Hareketleri geri almak ve yeniden girmek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="cb33d-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="cb33d-252">Hareketleri geri almak için tek yapmanız gereken **Tüm ödeme ekstreleri** sayfasında aşağıdaki adımları tamamlamaktır.</span><span class="sxs-lookup"><span data-stu-id="cb33d-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="cb33d-253">**Terse çevir** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="cb33d-254">"Bu ödeme ekstresini geri çevirdiğinizde, bu ödeme ekstresini dengelemek için bir ters ödeme ekstresi oluşturulacaktır" iletisi üzerinde **Evet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb33d-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="cb33d-255">Hiçbir ödeme ekstresi düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="cb33d-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="cb33d-256">Bu ödeme ekstresini ters çevirmek istiyor musunuz?"</span><span class="sxs-lookup"><span data-stu-id="cb33d-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="cb33d-257">görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="cb33d-257">displays.</span></span> 

<span data-ttu-id="cb33d-258">Ödem ekstresini terse çevirdikten sonra, daha önce oluşturmuş olduğunuz kazanç ekstresinden çalışan için yeni bir ödeme ekstresi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb33d-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="cb33d-259">Yeni ödeme ekstresini oluşturmadan önce kazanç ekstresindeki hatalı satırları düzelttiğinizden emin olun ve sonra doğru tutarlarla yeni ödemeleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="cb33d-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 
