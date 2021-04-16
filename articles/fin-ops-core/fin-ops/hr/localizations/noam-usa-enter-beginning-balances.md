---
title: Bordro başlangıç bakiyelerini girin
description: Bu konu kazanç kodları, kesintiler, kazançlar ve vergiler girmek için gerekli adımları anlatır.
author: andreabichsel
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752162"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="5b117-103">Bordro başlangıç bakiyelerini girme</span><span class="sxs-lookup"><span data-stu-id="5b117-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b117-104">Bu konu kazanç kodları, kesintiler, kazançlar ve vergiler girmek için gerekli adımları anlatır.</span><span class="sxs-lookup"><span data-stu-id="5b117-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="5b117-105">Bu bilgiler, veriyi bir sistemden yeni bir Bordro uygulama sistemine taşıması veya aktaran ortaklar için kullanışlıdır.</span><span class="sxs-lookup"><span data-stu-id="5b117-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="5b117-106">Bordro bakiyelerini girmeye hazırlanmak için aşağıdaki bilgileri doğrularız:</span><span class="sxs-lookup"><span data-stu-id="5b117-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="5b117-107">Personel kayıtlarının sisteme girilmiş ve kullanılabilir olması</span><span class="sxs-lookup"><span data-stu-id="5b117-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="5b117-108">Aşağıdaki verinin personele ayarlanmış ve atanmış olması:</span><span class="sxs-lookup"><span data-stu-id="5b117-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="5b117-109">Ödeme döngüleri ve ödeme dönemleri</span><span class="sxs-lookup"><span data-stu-id="5b117-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="5b117-110">Kazanç kodları</span><span class="sxs-lookup"><span data-stu-id="5b117-110">Earning codes</span></span>
    - <span data-ttu-id="5b117-111">Vergiler</span><span class="sxs-lookup"><span data-stu-id="5b117-111">Taxes</span></span>
    - <span data-ttu-id="5b117-112">Kazançlar ve kesintiler</span><span class="sxs-lookup"><span data-stu-id="5b117-112">Benefits and deductions</span></span>

- <span data-ttu-id="5b117-113">Şirket, bordro başlangıç bakiyelerinin ayarlanabileceği bir tarih seçmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5b117-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="5b117-114">Tüm kazançlar, kazanç/kesintiler, kazanç katkıları, personel vergileri ve işveren vergileri ile onların eski sistemdeki YTD tutarları hakkında bilgi toplanmıştır.</span><span class="sxs-lookup"><span data-stu-id="5b117-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="5b117-115">Başlangıç bakiyelerini girmeyi planladığınızda, verinin ne kadar ayrıntılı olması gerektiğini göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="5b117-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="5b117-116">Çoğu işletme tek bir birleştirilmiş yılbaşından bugüne tutarını girer</span><span class="sxs-lookup"><span data-stu-id="5b117-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="5b117-117">Ancak, daha ayrıntılı bilgi gerekiyorsa, bakiyeler üç aylık aralıklarla girilebilir.</span><span class="sxs-lookup"><span data-stu-id="5b117-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="5b117-118">Gerekli olan ayrıntı seviyesine karar vermek, her bir çalışan için kaç adet el ile ödeme ekstresinin oluşturulması gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="5b117-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="5b117-119">Tek bir yılbaşından bugüne tutarı için her bir çalışana yalnızca bir el ile ekstre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5b117-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="5b117-120">Bunu yapmak için önceki sistemden son ödeme ekstresinin yılbaşından bugüne tutarını, yeni bordro sisteminde girilen tutar olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b117-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="5b117-121">Aşağıdaki örnek kazanç kodları, kazançlar, kesintiler ve vergiler de dahil personel bordro başlangıç bakiyelerini nasıl girebileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b117-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="5b117-122">Bir gerçek dünya örneğinde, her bir kazanç kodu, kazanç kesintisi, kazanç katkısı, personel vergisi ve işveren vergisi için yılbaşından bugüne tutarında girilen tutar satır öğesine sahip olacaksınız.</span><span class="sxs-lookup"><span data-stu-id="5b117-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="5b117-123">Kodların ve tutarların bu listesini kullanarak, başlangıç bakiyelerini bordo amacıyla getirmek için muhasebe devre dışıyken bir el ile ödeme ve maaş ekstresini oluşturmak için izleyin.</span><span class="sxs-lookup"><span data-stu-id="5b117-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="5b117-124">Başlangıç bakiyesi ödeme ekstresini genel muhasebe defterinize nakletmek istemediğiniz için muhasebeyi devre dışı bırakırsınız.</span><span class="sxs-lookup"><span data-stu-id="5b117-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="5b117-125">Bu eski sistemde yapılmıştır ve Genel muhasebede başlangıç bakiyelerini ayarladığınızda gelecektir.</span><span class="sxs-lookup"><span data-stu-id="5b117-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="5b117-126">A.</span><span class="sxs-lookup"><span data-stu-id="5b117-126">A.</span></span> <span data-ttu-id="5b117-127">Bordro başlangıç bakiyelerinde kullanılacak kazanç kodlarının ayarlanması</span><span class="sxs-lookup"><span data-stu-id="5b117-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="5b117-128">Bordro başlangıç bakiyeleri girdiğinizde, kullanacağınız kazanç kodlarının "Kazanç ekstresi oranlarının düzenlenmesine izin ver" seçeneği etkin olarak yapılandırılmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="5b117-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="5b117-129">Bu, eski sistemden tutarı el ile girmenize izin verecektir.</span><span class="sxs-lookup"><span data-stu-id="5b117-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="5b117-130">B.</span><span class="sxs-lookup"><span data-stu-id="5b117-130">B.</span></span> <span data-ttu-id="5b117-131">Bir personelin bir başlangıç bakiyesine sahip olması için kazanç ekstreleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="5b117-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="5b117-132">Bu adım, eski sistemin son gün dönemi için, her bir çalışana bir kazanç ekstresini el ile yaratır ve bu da yeni bordro sisteminde kazanç ekstresi satırlarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b117-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="5b117-133">Kazanç kodu başına bir satır ve YTD tutarını ve saatlerini girin.</span><span class="sxs-lookup"><span data-stu-id="5b117-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="5b117-134">Örnek adımlar aşağıdaki gibidir:</span><span class="sxs-lookup"><span data-stu-id="5b117-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="5b117-135">**Tüm kazançlar ekstreleri** sayfasını açın ve **Yeni** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b117-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="5b117-136">Aşağıdakileri girin:</span><span class="sxs-lookup"><span data-stu-id="5b117-136">Enter the following:</span></span> 

    | <span data-ttu-id="5b117-137">Alan</span><span class="sxs-lookup"><span data-stu-id="5b117-137">Field</span></span>      | <span data-ttu-id="5b117-138">Değer</span><span class="sxs-lookup"><span data-stu-id="5b117-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="5b117-139">Çalışan</span><span class="sxs-lookup"><span data-stu-id="5b117-139">Worker</span></span>     | <span data-ttu-id="5b117-140">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="5b117-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="5b117-141">Ödeme döngüsü</span><span class="sxs-lookup"><span data-stu-id="5b117-141">Pay cycle</span></span>  | <span data-ttu-id="5b117-142">sm</span><span class="sxs-lookup"><span data-stu-id="5b117-142">sm</span></span>                    |
    | <span data-ttu-id="5b117-143">Ödeme dönemi</span><span class="sxs-lookup"><span data-stu-id="5b117-143">Pay period</span></span> | <span data-ttu-id="5b117-144">16/06/2017- 30/06/2017</span><span class="sxs-lookup"><span data-stu-id="5b117-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="5b117-145">**Kazanç ekstre satırı** sekmesinde aşağıdakini girin:</span><span class="sxs-lookup"><span data-stu-id="5b117-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="5b117-146">Satır 1: **Kazanç ekstre satırı** sekmesi</span><span class="sxs-lookup"><span data-stu-id="5b117-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="5b117-147">Alan</span><span class="sxs-lookup"><span data-stu-id="5b117-147">Field</span></span>            | <span data-ttu-id="5b117-148">Değer</span><span class="sxs-lookup"><span data-stu-id="5b117-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="5b117-149">Kazançlar kodu</span><span class="sxs-lookup"><span data-stu-id="5b117-149">Earnings code</span></span>    | <span data-ttu-id="5b117-150">Düzenli ödeme</span><span class="sxs-lookup"><span data-stu-id="5b117-150">Regular pay</span></span> |
    | <span data-ttu-id="5b117-151">Miktar</span><span class="sxs-lookup"><span data-stu-id="5b117-151">Quantity</span></span>         | <span data-ttu-id="5b117-152">1.00</span><span class="sxs-lookup"><span data-stu-id="5b117-152">1.00</span></span>        |
    | <span data-ttu-id="5b117-153">Ücret</span><span class="sxs-lookup"><span data-stu-id="5b117-153">Rate</span></span>             | <span data-ttu-id="5b117-154">30,000</span><span class="sxs-lookup"><span data-stu-id="5b117-154">30,000</span></span>      |
    | <span data-ttu-id="5b117-155">Satır ayrıntıları sekmesi</span><span class="sxs-lookup"><span data-stu-id="5b117-155">Line details tab</span></span> |             |
    | <span data-ttu-id="5b117-156">El ile</span><span class="sxs-lookup"><span data-stu-id="5b117-156">Manual</span></span>           | <span data-ttu-id="5b117-157">(işaretli)</span><span class="sxs-lookup"><span data-stu-id="5b117-157">(marked)</span></span>    |

    <span data-ttu-id="5b117-158">Satır 2: **Kazanç ekstre satırı** sekmesi</span><span class="sxs-lookup"><span data-stu-id="5b117-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="5b117-159">Alan</span><span class="sxs-lookup"><span data-stu-id="5b117-159">Field</span></span>            | <span data-ttu-id="5b117-160">Değer</span><span class="sxs-lookup"><span data-stu-id="5b117-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="5b117-161">Kazançlar kodu</span><span class="sxs-lookup"><span data-stu-id="5b117-161">Earnings code</span></span>    | <span data-ttu-id="5b117-162">Prim</span><span class="sxs-lookup"><span data-stu-id="5b117-162">Bonus</span></span>    |
    | <span data-ttu-id="5b117-163">Miktar</span><span class="sxs-lookup"><span data-stu-id="5b117-163">Quantity</span></span>         | <span data-ttu-id="5b117-164">1,0000</span><span class="sxs-lookup"><span data-stu-id="5b117-164">1.0000</span></span>   |
    | <span data-ttu-id="5b117-165">Ücret</span><span class="sxs-lookup"><span data-stu-id="5b117-165">Rate</span></span>             | <span data-ttu-id="5b117-166">4250,00</span><span class="sxs-lookup"><span data-stu-id="5b117-166">4250.00</span></span>  |
    | <span data-ttu-id="5b117-167">Satır ayrıntıları sekmesi</span><span class="sxs-lookup"><span data-stu-id="5b117-167">Line details tab</span></span> |          |
    | <span data-ttu-id="5b117-168">El ile</span><span class="sxs-lookup"><span data-stu-id="5b117-168">Manual</span></span>           | <span data-ttu-id="5b117-169">(işaretli)</span><span class="sxs-lookup"><span data-stu-id="5b117-169">(marked)</span></span> |

    <span data-ttu-id="5b117-170">Satır 3: **Kazanç ekstre satırı** sekmesi</span><span class="sxs-lookup"><span data-stu-id="5b117-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="5b117-171">Alan</span><span class="sxs-lookup"><span data-stu-id="5b117-171">Field</span></span>           | <span data-ttu-id="5b117-172">Değer</span><span class="sxs-lookup"><span data-stu-id="5b117-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="5b117-173">Kazançlar kodu</span><span class="sxs-lookup"><span data-stu-id="5b117-173">Earnings code</span></span>   | <span data-ttu-id="5b117-174">Komisyon</span><span class="sxs-lookup"><span data-stu-id="5b117-174">Commission</span></span> |
    | <span data-ttu-id="5b117-175">Miktar</span><span class="sxs-lookup"><span data-stu-id="5b117-175">Quantity</span></span>        | <span data-ttu-id="5b117-176">1,0000</span><span class="sxs-lookup"><span data-stu-id="5b117-176">1.0000</span></span>     |
    | <span data-ttu-id="5b117-177">Ücret</span><span class="sxs-lookup"><span data-stu-id="5b117-177">Rate</span></span>            | <span data-ttu-id="5b117-178">!.299,00</span><span class="sxs-lookup"><span data-stu-id="5b117-178">!,299.00</span></span>   |
    | <span data-ttu-id="5b117-179">Ücret</span><span class="sxs-lookup"><span data-stu-id="5b117-179">Rate</span></span>            | <span data-ttu-id="5b117-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="5b117-180">1,299.00</span></span>   |
    | <span data-ttu-id="5b117-181">Satır ayrıntı sekmesi</span><span class="sxs-lookup"><span data-stu-id="5b117-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="5b117-182">El ile</span><span class="sxs-lookup"><span data-stu-id="5b117-182">Manual</span></span>          | <span data-ttu-id="5b117-183">(İşaretli)</span><span class="sxs-lookup"><span data-stu-id="5b117-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="5b117-184">**Satır Ayrıntıları** sekmesinde **El ile** kaydırıcısının ayarını her bir kazanç ekstre satırını için **Evet** olarak işaretlemek, her bir çalışan için bordro başlangıç bakiyelerinin girilmesini sağlamak için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="5b117-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="5b117-185">**Eylem** bölmesinde, **Kazanç ekstrelerini serbest bırak** USA-FED-ER-FICA üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b117-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="5b117-186">**Eylem** bölmesinde, **Ödeme ekstresi** üzerine tıklayarak **Ödeme ekstreleri oluştur** sayfasını açın ve aşağıdakileri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="5b117-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="5b117-187">Alan</span><span class="sxs-lookup"><span data-stu-id="5b117-187">Field</span></span>              | <span data-ttu-id="5b117-188">Değer</span><span class="sxs-lookup"><span data-stu-id="5b117-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="5b117-189">Ödeme tarihi</span><span class="sxs-lookup"><span data-stu-id="5b117-189">Payment date</span></span>       | <span data-ttu-id="5b117-190">30/06/2017</span><span class="sxs-lookup"><span data-stu-id="5b117-190">6/30/2017</span></span> |
    | <span data-ttu-id="5b117-191">Ödeme işlemi türü</span><span class="sxs-lookup"><span data-stu-id="5b117-191">Payment run type</span></span>   | <span data-ttu-id="5b117-192">El ile</span><span class="sxs-lookup"><span data-stu-id="5b117-192">Manual</span></span>    |
    | <span data-ttu-id="5b117-193">Muhasebeyi devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="5b117-193">Disable accounting</span></span> |   <span data-ttu-id="5b117-194">Evet</span><span class="sxs-lookup"><span data-stu-id="5b117-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="5b117-195">Bu, yalnızca ödeme yürütme türü el ile olduğunda ve kullanıcının ödeme çalıştırmasında muhasebeyi devre dışı bırakmak istediğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5b117-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="5b117-196">**Tamam** üzerine tıklayın ve **Bilgi günlüğü**'nü kapatın.</span><span class="sxs-lookup"><span data-stu-id="5b117-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="5b117-197">Ödeme ekstreleri oluştururken Muhasebeyi Devre Dışı Bırak kaydırıcısı neden Evet olmalıdır?</span><span class="sxs-lookup"><span data-stu-id="5b117-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="5b117-198">Kaydırıcıyı **Evet** olarak ayarlamak, ödeme ekstresindeki satırların Genel muhasebeye dağıtılmasını engeller.</span><span class="sxs-lookup"><span data-stu-id="5b117-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="5b117-199">Genel muhasebe tutarları, eski sistemden hesap bakiyeleri girildiğinde güncelleştirilmekteydi.</span><span class="sxs-lookup"><span data-stu-id="5b117-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="5b117-200">Bordro için başlangıç bakiyeleri girmek, önceki yıllardan bilgi içeren raporlar oluşturmanıza ve kazanç ve vergi amaçlı sınırlamaları belirlemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="5b117-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="5b117-201">C.</span><span class="sxs-lookup"><span data-stu-id="5b117-201">C.</span></span> <span data-ttu-id="5b117-202">Personeller için ödeme ekstreleri oluştur</span><span class="sxs-lookup"><span data-stu-id="5b117-202">Create pay statements for employees</span></span>

<span data-ttu-id="5b117-203">Başlangıç bakiyelerine sahip ödeme ekstreleri oluşturduktan sonra, ödeme ekstrelerinin bordro verisini doğru şekilde yansıttığını doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5b117-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="5b117-204">Kazanç ve vergi bilgisini de önceki bordro sistemindeki verilerle eşleşecek şekilde el ile güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5b117-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="5b117-205">Önceki bordro sisteminden tutarları, geçerli ödeme ekstrelerindeki tutarlarla eşleştiğini doğruladıktan sonra, ödeme ekstrelerini sonlandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5b117-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="5b117-206">**Tüm ödeme ekstreleri** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="5b117-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="5b117-207">Michael Redmond için son oluşturulan ödeme ekstresini vurgulayın</span><span class="sxs-lookup"><span data-stu-id="5b117-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="5b117-208">**Ödeme ekstresi** sayfasını açmak için **Düzenle** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b117-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="5b117-209">**Kazanç kesintileri** sekmesini açın ve aşağıdakini girin:</span><span class="sxs-lookup"><span data-stu-id="5b117-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="5b117-210">Alan</span><span class="sxs-lookup"><span data-stu-id="5b117-210">Field</span></span>             | <span data-ttu-id="5b117-211">Değer</span><span class="sxs-lookup"><span data-stu-id="5b117-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="5b117-212">Kazanç</span><span class="sxs-lookup"><span data-stu-id="5b117-212">Benefit</span></span>           | <span data-ttu-id="5b117-213">Kesinti tutarı</span><span class="sxs-lookup"><span data-stu-id="5b117-213">Deduction amount</span></span> |
    | <span data-ttu-id="5b117-214">401K</span><span class="sxs-lookup"><span data-stu-id="5b117-214">401K</span></span>              | <span data-ttu-id="5b117-215">Katıl</span><span class="sxs-lookup"><span data-stu-id="5b117-215">Participate</span></span>      |
    | <span data-ttu-id="5b117-216">Diş</span><span class="sxs-lookup"><span data-stu-id="5b117-216">Dental</span></span>            | <span data-ttu-id="5b117-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="5b117-217">SubSp</span></span>            |
    | <span data-ttu-id="5b117-218">Dep bakım harcaması</span><span class="sxs-lookup"><span data-stu-id="5b117-218">Dep care spending</span></span> | <span data-ttu-id="5b117-219">Katıl</span><span class="sxs-lookup"><span data-stu-id="5b117-219">Participate</span></span>      |
    | <span data-ttu-id="5b117-220">Görme</span><span class="sxs-lookup"><span data-stu-id="5b117-220">Vision</span></span>            | <span data-ttu-id="5b117-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="5b117-221">SupSp</span></span>            |

5. <span data-ttu-id="5b117-222">**Kazanç katkıları** sekmesinde aşağıdakileri girin:</span><span class="sxs-lookup"><span data-stu-id="5b117-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="5b117-223">Alan</span><span class="sxs-lookup"><span data-stu-id="5b117-223">Field</span></span>   | <span data-ttu-id="5b117-224">Değer</span><span class="sxs-lookup"><span data-stu-id="5b117-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="5b117-225">Kazanç</span><span class="sxs-lookup"><span data-stu-id="5b117-225">Benefit</span></span> | <span data-ttu-id="5b117-226">Katkı tutarı</span><span class="sxs-lookup"><span data-stu-id="5b117-226">Contribution amount</span></span> |
    | <span data-ttu-id="5b117-227">401K</span><span class="sxs-lookup"><span data-stu-id="5b117-227">401K</span></span>    | <span data-ttu-id="5b117-228">Katıl</span><span class="sxs-lookup"><span data-stu-id="5b117-228">Participate</span></span>         |
    | <span data-ttu-id="5b117-229">Diş</span><span class="sxs-lookup"><span data-stu-id="5b117-229">Dental</span></span>  | <span data-ttu-id="5b117-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="5b117-230">SubSp</span></span>               |
    | <span data-ttu-id="5b117-231">Görme</span><span class="sxs-lookup"><span data-stu-id="5b117-231">Vision</span></span>  | <span data-ttu-id="5b117-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="5b117-232">SubSp</span></span>               |

6. <span data-ttu-id="5b117-233">**Vergi kesintileri** sekmesinde aşağıdakileri girin:</span><span class="sxs-lookup"><span data-stu-id="5b117-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="5b117-234">Alan</span><span class="sxs-lookup"><span data-stu-id="5b117-234">Field</span></span>           | <span data-ttu-id="5b117-235">Değer</span><span class="sxs-lookup"><span data-stu-id="5b117-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="5b117-236">Vergi kodu.</span><span class="sxs-lookup"><span data-stu-id="5b117-236">Tax code</span></span>        | <span data-ttu-id="5b117-237">Kesinti tutarı</span><span class="sxs-lookup"><span data-stu-id="5b117-237">Deduction amount</span></span> |
    | <span data-ttu-id="5b117-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="5b117-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="5b117-239">1600,00</span><span class="sxs-lookup"><span data-stu-id="5b117-239">1600.00</span></span>          |
    | <span data-ttu-id="5b117-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="5b117-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="5b117-241">825,75</span><span class="sxs-lookup"><span data-stu-id="5b117-241">825.75</span></span>           |

7. <span data-ttu-id="5b117-242">**Vergi katkıları** sekmesinde aşağıdakileri girin:</span><span class="sxs-lookup"><span data-stu-id="5b117-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="5b117-243">**Hesapla** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b117-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="5b117-244">Çalışan için ödeme ekstresi toplamlarının eski sistemin YTD'si ile eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="5b117-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="5b117-245">Tüm ödeme ekstrelerinin toplamında bazı genel doğrulamalar gerçekleştirmek için sonraki adımda sonlandırmayı bekletmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b117-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="5b117-246">Doğrulandıktan sonra, tüm ödeme ekstreleri arasında çalıştırın ve onları sonlandırın.</span><span class="sxs-lookup"><span data-stu-id="5b117-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="5b117-247">Aynı işlem gerek duyulursa, yıl içerisindeki tüm önceki çeyrekler için üç aylık aralıklarla yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="5b117-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="5b117-248">Bu yalnızca müşterinin eski sisteme geri gitmeden veriyi üç alık olarak görmesi gerekiyorsa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5b117-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="5b117-249">Bir Personel için Başlangıç Bakiyelerini girerken bir hata yaptıysanız</span><span class="sxs-lookup"><span data-stu-id="5b117-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="5b117-250">Hareketleri geri almak ve yeniden girmek mümkündür.</span><span class="sxs-lookup"><span data-stu-id="5b117-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="5b117-251">Hareketleri geri almak için tek yapmanız gereken **Tüm ödeme ekstreleri** sayfasında aşağıdaki adımları tamamlamaktır.</span><span class="sxs-lookup"><span data-stu-id="5b117-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="5b117-252">**Terse çevir** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b117-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="5b117-253">"Bu ödeme ekstresini geri çevirdiğinizde, bu ödeme ekstresini dengelemek için bir ters ödeme ekstresi oluşturulacaktır" iletisi üzerinde **Evet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5b117-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="5b117-254">Hiçbir ödeme ekstresi düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="5b117-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="5b117-255">Bu ödeme ekstresini ters çevirmek istiyor musunuz?"</span><span class="sxs-lookup"><span data-stu-id="5b117-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="5b117-256">görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5b117-256">displays.</span></span> 

<span data-ttu-id="5b117-257">Ödem ekstresini terse çevirdikten sonra, daha önce oluşturmuş olduğunuz kazanç ekstresinden çalışan için yeni bir ödeme ekstresi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5b117-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="5b117-258">Yeni ödeme ekstresini oluşturmadan önce kazanç ekstresindeki hatalı satırları düzelttiğinizden emin olun ve sonra doğru tutarlarla yeni ödemeleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5b117-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]