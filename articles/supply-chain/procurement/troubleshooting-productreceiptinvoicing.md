---
title: Ürün girişleri ve faturalama ile ilgili sorunları giderme
description: Bu konu, ürün girişleri ve faturalama ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 3522a024261ff6dfffb53f2101139460be7669e4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832022"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="98747-103">Ürün girişleri ve faturalama ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="98747-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="98747-104">Bu konu, ürün girişleri ve faturalama ile ilgili çalışırken karşılaşabileceğiniz sorunların nasıl düzeltilebileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="98747-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="98747-105">Kategori tabanlı ögeler içeren bir satınalma siparişi satırı için birden fazla faturayı deftere nakledemiyorum.</span><span class="sxs-lookup"><span data-stu-id="98747-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="98747-106">Faturaları deftere nakletmek istiyorsanız miktar değeri zorunludur.</span><span class="sxs-lookup"><span data-stu-id="98747-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="98747-107">Bu nedenle, bir satırın tam miktarı yalnızca kısmi bir tutar için faturalanmışsa, kalan tutarı başka bir faturada faturalayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="98747-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="98747-108">Satınalma siparişi teyidi sırasında "Nesne başvurusu ayarlanmadı" hatasını alıyorum veya satıcı faturasının deftere nakli sırasında "Bir çağrı hedefi tarafından özel durum oluşturuldu" özel durumu oluştu.</span><span class="sxs-lookup"><span data-stu-id="98747-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="98747-109">Bu sorun, satınalma siparişi dağılımlarında tutarsızlık olması nedeniyle oluşabilir.</span><span class="sxs-lookup"><span data-stu-id="98747-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="98747-110">Bu sorunun engelini kaldırmak ve satınalma siparişini *Taslak* durumuna sıfırlamak için, **Satın alma ve kaynak hizmeti \> Dönemsel görevler \> Temizle \> Satınalma siparişi dağılımını sıfırlama** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="98747-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="98747-111">Daha fazla bilgi için aşağıdaki blog postasına bakın: [SAS dağıtım hatalarını Dynamics 365 Supply Chain Management'da çözümle](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="98747-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="98747-112">Çoklu ürün girişlerini tek bir satınalma siparişinde birleştiremiyorum.</span><span class="sxs-lookup"><span data-stu-id="98747-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="98747-113">Farklı ürün giriş satırları farklı muhasebe tarihlerine sahipse, çoklu ürün girişlerini tek bir satınalma siparişinde birleştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="98747-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="98747-114">Microsoft Dynamics 365 Supply Chain Management uygulamasının önceki sürümlerinde, bu durumda birleştirmeye izin veriliyordu.</span><span class="sxs-lookup"><span data-stu-id="98747-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="98747-115">Ancak, uygulama hataya açıktır.</span><span class="sxs-lookup"><span data-stu-id="98747-115">However, the practice is prone to error.</span></span> <span data-ttu-id="98747-116">Oluşturulan satınalma siparişi satırlarındaki hesap tarihi, bu satınalma siparişi satırlarının oluşturulduğu ürün giriş satırlarındaki hesap tarihinden farklı olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="98747-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="98747-117">(Satınalma siparişi satırlarındaki muhasebe tarihi, satınalma siparişi başlığındaki hesap tarihiyle eşleşir.) Bu nedenle, çoklu ürün girişinin tek bir satınalma siparişinde birleştirilmesine artık izin verilmez.</span><span class="sxs-lookup"><span data-stu-id="98747-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="98747-118">Muhasebe tarihi, örneğin bütçe rezervasyonları ve tutarlılık için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="98747-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="98747-119">Bu nedenle, ürün girişinden satınalma siparişine geçiş sırasında tutulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="98747-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="98747-120">Ürün girişleri iptal edildiğinde, hareketler askıya alınan genel muhasebe hesabına nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="98747-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="98747-121">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="98747-121">Issue description</span></span>

<span data-ttu-id="98747-122">Bir ürün girişi iptal edilirse, ana hesaplar askıya alınmış olsa bile, sistem hareketlerin askıya alınan genel muhasebe hesaplarına nakledilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="98747-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="98747-123">Sorunu yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="98747-123">Reproduce the issue</span></span>

<span data-ttu-id="98747-124">Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="98747-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="98747-125">**Borç hesapları parametreleri** sayfasındaki **Genel** sekmesinde, **Ürün girişini deftere naklet** seçeneğinin *Evet* olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="98747-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="98747-126">Satınalma siparişi oluşturun ve *bir ürün için 1.000'lik miktarı içeren bir sipariş satırı ekleyin*.</span><span class="sxs-lookup"><span data-stu-id="98747-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="98747-127">Satınalma siparişini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="98747-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="98747-128">Ürün girişini deftere nakledin ve fişleri denetleyin.</span><span class="sxs-lookup"><span data-stu-id="98747-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="98747-129">*200140* ve *140200* olan ilgili ana hesapları askıya alın.</span><span class="sxs-lookup"><span data-stu-id="98747-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="98747-130">Deftere nakledilen ürün girişini iptal edin.</span><span class="sxs-lookup"><span data-stu-id="98747-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="98747-131">Hareketlerin askıya alınan muhasebe hesaplara nakledilebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="98747-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98747-132">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="98747-132">Issue resolution</span></span>

<span data-ttu-id="98747-133">Ürün girişleri iptal edildiğinde, hareketler, bu yaklaşım deftere doğru nakledilmeye olanak sağladığında, bekleyen genel muhasebe defterine nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="98747-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="98747-134">Ürün girişi sırasında hiçbir mali fiş oluşturulmasa da, bir ürün girişi fiş numarası kullanılır.</span><span class="sxs-lookup"><span data-stu-id="98747-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="98747-135">Malzeme modeli grubu için **Ürün girişindeki tahakkuk borcu** seçeneği *Hayır* olarak ayarlanmışsa, genel muhasebeye nakil yapılmaz.</span><span class="sxs-lookup"><span data-stu-id="98747-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="98747-136">Ancak, bir alt genel muhasebede muhasebe amacıyla fiziksel bir olay kaydedilir ve bu olay bir fiş numarası gerektirir.</span><span class="sxs-lookup"><span data-stu-id="98747-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="98747-137">Bu fiş numarası stok hareketlerinde referans alınan fiş numarasıdır.</span><span class="sxs-lookup"><span data-stu-id="98747-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="98747-138">Aşağıdaki Web günlüğünde açıklandığı gibi, **Ürün girişindeki tahakkuk borcu** seçeneğini *Evet* olarak ayarlamanız önerilir: [Ürün makbuzu oluşturulurken sair giderleri deftere nakletme](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="98747-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="98747-139">Genel muhasebedeki gider hesabına naklet ayarı açık değil.</span><span class="sxs-lookup"><span data-stu-id="98747-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="98747-140">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="98747-140">Issue description</span></span>

<span data-ttu-id="98747-141">Bu sorun bir satınalma siparişi faturalandığında, **Borç hesapları parametreleri** sayfasındaki **Fatura** sekmesinde **Genel muhasebedeki gider hesabına naklet** seçeneği *Evet* olarak ayarlandığında oluşur.</span><span class="sxs-lookup"><span data-stu-id="98747-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="98747-142">Sorunu yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="98747-142">Reproduce the issue</span></span>

<span data-ttu-id="98747-143">Aşağıdaki yordamda, bu sorunu yeniden oluşturmanın bir yolu gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="98747-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="98747-144">**Borç hesapları \> Kurulum \> Borç hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="98747-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="98747-145">**Fatura** sekmesinde, **Genel muhasebedeki gider hesabına naklet** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="98747-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="98747-146">**Stok Yönetimi \> Kurulum \> Deftere nakil \> Deftere nakil** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="98747-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="98747-147">**Satınalma siparişi** sekmesinde, ürünle ilgili satın alma harcamaları içindeki tüm satırları sildiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="98747-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="98747-148">**Borç hesapları \> Satın alma siparişleri \> Tüm satınalma siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="98747-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="98747-149">Bir satınalma siparişi oluşturmak.</span><span class="sxs-lookup"><span data-stu-id="98747-149">Create a purchase order.</span></span> <span data-ttu-id="98747-150">**Satıcı hesabı** alanında, *1001 Acme Office Supplies* ögesini seçin.</span><span class="sxs-lookup"><span data-stu-id="98747-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="98747-151">Aşağıdaki ayarlara sahip satınalma siparişi satırı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="98747-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="98747-152">**Malzeme numarası:** *D0011 lazer projektör*</span><span class="sxs-lookup"><span data-stu-id="98747-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="98747-153">**Tesis:** *1*</span><span class="sxs-lookup"><span data-stu-id="98747-153">**Site:** *1*</span></span>
    - <span data-ttu-id="98747-154">**Ambar:** *11*</span><span class="sxs-lookup"><span data-stu-id="98747-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="98747-155">**Miktar:** *4*</span><span class="sxs-lookup"><span data-stu-id="98747-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="98747-156">Eylem Bölmesi'nde, **Satın al** sekmesindeki **Eylem** grubunda **Onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="98747-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="98747-157">Eylem Bölmesi'nde, **Teslim al** sekmesindeki **Oluştur** grubunda **Ürün girişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="98747-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="98747-158">**Ürün girişi naklediliyor** iletişim kutusunda, **Ürün girişi** alanında rastgele bir numara girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="98747-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="98747-159">Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="98747-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="98747-160">**Numara** alanına, fatura numarası olarak rasgele bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="98747-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="98747-161">Eşleştirme durumunu güncelleştirin ve deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="98747-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="98747-162">Bir satınalma siparişinden fatura oluştururken şimdi aşağıdaki hatayı alacağınızı unutmayın: "Ürün için satınalma harcamaları hareket türü için hesap numarası yok."</span><span class="sxs-lookup"><span data-stu-id="98747-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="98747-163">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="98747-163">Issue resolution</span></span>

<span data-ttu-id="98747-164">Bu, fatura ve fatura gruplarının parametre ayarlarına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="98747-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="98747-165">Daha fazla bilgi için, aşağıdaki Web günlüğü postasına bakın: [Satınalma ücreti ve stok farkı için hesap](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="98747-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]