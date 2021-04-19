---
title: Navlun taşımacılık yönetiminde mutabakat sağlama
description: Bu konu altında navlun mutabakatı işlemi anlatılmaktadır.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d523af235d645bd282af07d6a1f617bca5fba2dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809098"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="95b03-103">Navlun taşımacılık yönetiminde mutabakat sağlama</span><span class="sxs-lookup"><span data-stu-id="95b03-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95b03-104">Bu konu altında navlun mutabakatı işlemi anlatılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="95b03-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="95b03-105">Navlun mutabakatı el ile yapılabilir veya otomatik olarak gerçekleşmek üzere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="95b03-106">Otomatik navlun mutabakatı kullanmak için, otomatik olarak eşleştirilecek navlun faturalarını belirleyen ölçütleri tanımlayabileceğiniz bir ana denetim ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="95b03-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="95b03-107">Navlun mutabakat işlemi</span><span class="sxs-lookup"><span data-stu-id="95b03-107">The freight reconciliation process</span></span>

<span data-ttu-id="95b03-108">Navlun oranları ilgili sevkiyat taşıyıcısı ile ilişkilendirilmiş değerlendirme altyapısı tarafından hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="95b03-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="95b03-109">Bir yük onaylandığında, navlun faturası oluşturulur ve navlun giderleri bu faturaya aktarılır.</span><span class="sxs-lookup"><span data-stu-id="95b03-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="95b03-110">Navlun giderleri normal faturalandırma sürecinde kullanılan kuruluma bağlı olarak, ilgili kaynak belgesine sair masraflar (satınalma siparişi, satış siparişi ve/veya transfer emri) olarak paylaştırılır.</span><span class="sxs-lookup"><span data-stu-id="95b03-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="95b03-111">Navlun mutabakatı süreci (eşleştirme süreci olarak da adlandırılır) navlun faturası sevkiyat taşıyıcısından ulaştığı anda başlayabilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="95b03-112">Fatura elektronik veya kağıt üzerinde alınabilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="95b03-113">Fatura kağıt üzerinde alınırsa navlun faturasını şablon olarak kullanarak elektronik bir fatura oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95b03-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="95b03-114">[![Navlun mutabakatı işlemi](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="95b03-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="95b03-115">El ile mutabakat</span><span class="sxs-lookup"><span data-stu-id="95b03-115">Manual reconciliation</span></span>

<span data-ttu-id="95b03-116">Navlun mutabakatını el ile gerçekleştiriyorsanız her fatura satırını faturalandırılan yüke ait navlun faturasındaki satır veya satırlarla eşleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="95b03-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="95b03-117">Bu eşleştirme işlemi **Navlun faturası ve fatura eşleştirme** sayfasından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="95b03-118">Fatura satırındaki tutar navlun faturası tutarıyla eşleşmiyorsa, aradaki fark için bir mutabakat nedeni seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="95b03-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="95b03-119">Mutabakatın birden fazla nedeni varsa eşleşmeyen tutarı bu nedenler arasında paylaştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95b03-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="95b03-120">Mutabakat nedeni farklı tutarların genel muhasebe defterine nasıl nakledileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="95b03-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="95b03-121">Tüm fatura tutarının mutabakatı açıklandığında, onay için gönderilir ve deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="95b03-122">Aşağıdaki resimde navlun faturası oluşturma ve navlun mutabakatı gerçekleştirme işlemleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="95b03-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="95b03-123">[![Navlun mutabakat görevleri](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="95b03-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="95b03-124">Otomatik mutabakat</span><span class="sxs-lookup"><span data-stu-id="95b03-124">Automatic reconciliation</span></span>

<span data-ttu-id="95b03-125">Otomatik mutabakat kullanmak için mutabakatın zaman çizelgesini, faturaları ve kullanılacak sevkiyat taşıyıcılarını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="95b03-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="95b03-126">Fatura satırları ile navlun faturalarını eşleştirme işlemi ana denetim kurulumuna ve navlun faturası türüne göre gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="95b03-127">Otomatik mutabakat çalıştırdıktan sonra sistemin eşleştiremediği tüm faturaları el ile incelemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="95b03-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="95b03-128">Bundan sonra tüm faturaları ödeme için nakledebilmeniz için bu faturaları el ile işlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="95b03-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="95b03-129">Otomatik veya el ile mutabakatı kullanarak navlun fişleriyle navlun faturalarını eşleştirme</span><span class="sxs-lookup"><span data-stu-id="95b03-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="95b03-130">*Eşleme*, her navlun faturasına karşılık gelen navlun fişlerini bulma işlemidir.</span><span class="sxs-lookup"><span data-stu-id="95b03-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="95b03-131">Bu işlem, fatura satırlarını birer birer (el ile eşleşme) ile veya tüm kullanılabilir faturaların aynı anda eşleştirilmesiyle (otomatik eşleştirme) yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="95b03-132">Otomatik eşleme</span><span class="sxs-lookup"><span data-stu-id="95b03-132">Auto matching</span></span>

<span data-ttu-id="95b03-133">Birden fazla navlun faturasını aynı navlun fişiyle eşleştirmek için otomatik eşleme işlemi aşağıdaki şekilde çalışır:</span><span class="sxs-lookup"><span data-stu-id="95b03-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="95b03-134">Eşlenmeyen tüm navlun faturaları, en başta en büyük tutar olacak şekilde tutara göre sıralanır.</span><span class="sxs-lookup"><span data-stu-id="95b03-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="95b03-135">Navlun fişinde pozitif tutar kalmayana kadar navlun faturaları birer birer eşleştirilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="95b03-136">Ana denetimin kurulumuna ve navlun faturalarının kalan tutarına bağlı olarak kalan tutar ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="95b03-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="95b03-137">El ile eşleştirme</span><span class="sxs-lookup"><span data-stu-id="95b03-137">Manual matching</span></span>

<span data-ttu-id="95b03-138">Pozitif tutarları olan tüm navlun fişleri, eşleme için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="95b03-139">Otomatik eşlemeye benzer şekilde kullanıcı, yalnızca negatif tutarı olan navlun faturalarını tamamen eşlenmeyen navlun fişleriyle eşleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="95b03-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="95b03-140">Örnek</span><span class="sxs-lookup"><span data-stu-id="95b03-140">Example</span></span>

<span data-ttu-id="95b03-141">1500 tutarında bir navlun faturanız (FB) olduğunu ve aşağıdaki ayarlarla her fatura için bir fatura satırı içeren navlun fişi için üç navlun faturası oluşturduğunuzu varsayın:</span><span class="sxs-lookup"><span data-stu-id="95b03-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="95b03-142">Orijinal navlun fişini (FB): Tutar 1500</span><span class="sxs-lookup"><span data-stu-id="95b03-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="95b03-143">Fatura 1 (Inv1): Tutar 1000</span><span class="sxs-lookup"><span data-stu-id="95b03-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="95b03-144">Fatura 2 (Inv2): Tutar 600</span><span class="sxs-lookup"><span data-stu-id="95b03-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="95b03-145">Fatura 3 (Inv3): Tutar -100</span><span class="sxs-lookup"><span data-stu-id="95b03-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="95b03-146">Otomatik eşleştirme sonucu</span><span class="sxs-lookup"><span data-stu-id="95b03-146">Automatic matching result</span></span>

<span data-ttu-id="95b03-147">Otomatik eşleme aşağıdaki sırada çalışır:</span><span class="sxs-lookup"><span data-stu-id="95b03-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="95b03-148">Tüm navlun faturalarını tutara göre azalan düzende sırala: Inv1-> Inv2-> Inv3.</span><span class="sxs-lookup"><span data-stu-id="95b03-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="95b03-149">Inv1 ile FB'yi eşleştirme.</span><span class="sxs-lookup"><span data-stu-id="95b03-149">Match Inv1 with FB.</span></span> <span data-ttu-id="95b03-150">Inv1, 1000 tutarını eşleştirdi ve FB'nin kalan tutarı 500 oldu. Böylece durum *Kısmen eşleştirildi* olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="95b03-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="95b03-151">Inv2 ile FB'yi eşleştirme.</span><span class="sxs-lookup"><span data-stu-id="95b03-151">Match Inv2 with FB.</span></span> <span data-ttu-id="95b03-152">Inv2, 500 tutarını eşleştirdi ve FB'nin kalan tutarı 0 oldu. Böylece durum *Tamamen eşleştirildi* olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="95b03-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="95b03-153">FB şu anda tümüyle eşleştirildiğinden Inv3 işlenmez.</span><span class="sxs-lookup"><span data-stu-id="95b03-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="95b03-154">El ile eşleme sonucu</span><span class="sxs-lookup"><span data-stu-id="95b03-154">Manual matching result</span></span>

<span data-ttu-id="95b03-155">El ile eşleştirme için, sonuçlar, aşağıdaki örnek durumlarda gösterildiği gibi, eşleştirme sırasına göre değişir.</span><span class="sxs-lookup"><span data-stu-id="95b03-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="95b03-156">El ile eşleme durumu 1</span><span class="sxs-lookup"><span data-stu-id="95b03-156">Manual matching case 1</span></span>

<span data-ttu-id="95b03-157">Bu örnek için el ile eşleştirme yapmanın bir yolu aşağıdakileri yapmaktır:</span><span class="sxs-lookup"><span data-stu-id="95b03-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="95b03-158">FB'yi Inv1 ile eşleştirme.</span><span class="sxs-lookup"><span data-stu-id="95b03-158">Match FB with Inv1.</span></span> <span data-ttu-id="95b03-159">FB'nin kalan tutarı 500'dür. Bu nedenle, durum *Kısmen eşleştirildi* olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="95b03-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="95b03-160">Inv2 ile FB'yi eşleştirme.</span><span class="sxs-lookup"><span data-stu-id="95b03-160">Match Inv2 with FB.</span></span> <span data-ttu-id="95b03-161">Inv2, 500 tutarını eşleştirdi ve FB'nin kalan tutarı 0 oldu. Böylece durum *Tamamen eşleştirildi* olarak ayarlandı.</span><span class="sxs-lookup"><span data-stu-id="95b03-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="95b03-162">Inv3 el ile eşleştirildiğinde, herhangi bir eşlenmeyen navlun fişi bulamazsınız.</span><span class="sxs-lookup"><span data-stu-id="95b03-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="95b03-163">Bu durum temelde, otomatik eşleme ile aynıdır</span><span class="sxs-lookup"><span data-stu-id="95b03-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="95b03-164">El ile eşleme durumu 2</span><span class="sxs-lookup"><span data-stu-id="95b03-164">Manual matching case 2</span></span>

<span data-ttu-id="95b03-165">Bu örnek için el ile eşleştirme yapmanın bir diğer yolu da aşağıdakileri yapmaktır:</span><span class="sxs-lookup"><span data-stu-id="95b03-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="95b03-166">FB'yi Inv3 ile eşleştirme.</span><span class="sxs-lookup"><span data-stu-id="95b03-166">Match Inv3 with FB.</span></span> <span data-ttu-id="95b03-167">Şimdi FB'nin kalan tutarı 1600'dür. Bu, 1500'ün üzerine eksi 100 çıkarmak anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="95b03-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="95b03-168">Hem FB hem de Inv3'ün eşleşen miktarı -100 olur.</span><span class="sxs-lookup"><span data-stu-id="95b03-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="95b03-169">Inv1 ve Inv 2'yi arka arkaya FB ile eşleştirme.</span><span class="sxs-lookup"><span data-stu-id="95b03-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="95b03-170">FB, tümüyle eşlenir.</span><span class="sxs-lookup"><span data-stu-id="95b03-170">FB is fully matched.</span></span>

<span data-ttu-id="95b03-171">Bu örnekte görüldüğü gibi, negatif tutarlarla sahip navlun faturalarını eşleme işlemi yalnızca el ile yapılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="95b03-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="95b03-172">Böylece, eşleşen sırayı denetleyebileceğinzi için navlun faturalarını her zaman tam olarak eşleştirilmeyen bir navlun fişiyle eşleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95b03-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]