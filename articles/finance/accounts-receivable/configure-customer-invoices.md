---
title: Müşteri faturası oluşturma
description: '**Satış siparişi için müşteri faturası** kuruluşun bir müşteriye verdiği, satışla ilişkili bir faturadır.'
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f5b9866fc7afba205b84b372c6a204ec4c8f64d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448683"
---
# <a name="create-a-customer-invoice"></a><span data-ttu-id="bed9e-103">Müşteri faturası oluşturma</span><span class="sxs-lookup"><span data-stu-id="bed9e-103">Create a customer invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bed9e-104">**Satış siparişi için müşteri faturası** kuruluşun bir müşteriye verdiği, satışla ilişkili bir faturadır.</span><span class="sxs-lookup"><span data-stu-id="bed9e-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="bed9e-105">Bu türdeki bir satış faturası, satış satırları ve madde numaraları içeren bir satış siparişine dayanarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bed9e-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="bed9e-106">Madde numaraları genel muhasebede belirtilir ve deftere kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="bed9e-107">Muavin defteri günlük girişleri, bir satış siparişi için müşteri faturası için kullanılamaz</span><span class="sxs-lookup"><span data-stu-id="bed9e-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="bed9e-108">Daha fazla bilgi için bkz. [Satış siparişi faturaları oluşturun](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="bed9e-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="bed9e-109">Bir **serbest metin faturası** satış siparişiyle ilişkili değildir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="bed9e-110">Genel muhasebe hesaplarının, serbest metin açıklamalarının ve girdiğiniz satış tutarının bulunduğu sipariş satırlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="bed9e-111">Bu tür bir faturaya bir madde numarası giremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="bed9e-112">Uygun satış vergisi bilgilerini girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="bed9e-113">Satış için bir ana hesap her fatura satırında belirtilir ve **serbest metin faturası** sayfasındaki **Dağıtım tutarları** üzerine tıklatarak birden çok genel muhasebe hesaplarına dağıtabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="bed9e-114">Ayrıca, müşteri bakiyesi gelen serbest metin faturası için kullanılan deftere nakil profili özet hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="bed9e-115">Daha fazla bilgi için bkz.:</span><span class="sxs-lookup"><span data-stu-id="bed9e-115">For more information see:</span></span>

[<span data-ttu-id="bed9e-116">Serbest metin faturaları oluştur</span><span class="sxs-lookup"><span data-stu-id="bed9e-116">Create free text invoices</span></span>](../accounts-receivable/create-free-text-invoice-new.md)

[<span data-ttu-id="bed9e-117">Serbest metin faturası şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="bed9e-117">Create a free text invoice template</span></span>](../accounts-receivable/create-free-text-invoice-template-new.md)

[<span data-ttu-id="bed9e-118">Bir müşteriye serbest metin faturası şablonu atayın</span><span class="sxs-lookup"><span data-stu-id="bed9e-118">Assign free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="bed9e-119">Yinelenen serbest metin faturaları oluşturma ve deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="bed9e-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="bed9e-120">Bir **Proforma fatura** bir fatura deftere nakledilmeden önce gerçek fatura tutarlarının bir tahmini olarak hazırlanan faturadır.</span><span class="sxs-lookup"><span data-stu-id="bed9e-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="bed9e-121">Satış siparişi için müşteri faturası veya bir serbest metin faturası için bir proforma fatura yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="bed9e-122">Satış siparişine dayalı olan tekil müşteri faturalarını deftere nakledin veya yazdırın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="bed9e-123">Bir satış siparişini temel alan bir fatura oluşturmak için bu işlemi kullanın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="bed9e-124">Mal veya hizmeti teslim etmeden önce müşteriye fatura kesmek isterseniz bunu yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="bed9e-125">Bir faturayı deftere naklettiğinizde, her maddenin **Fatura kalan tutarı** miktarı, seçili satış siparişinden faturalanan miktarların toplamı ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="bed9e-126">Eğer tüm maddeler için **Fatura kalanı** miktarı ve **Teslimat bakiyesi** satış siparişindeki miktarı 0 (sıfır) olursa, satış siparişinin durumu **Faturalandı** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="bed9e-127">Eğer **Fatura kalanı** miktarı 0 (sıfır) değilse, satış siparişinin durumu değiştirilmez ve buna ek faturalar girilebilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="bed9e-128">Satış siparişlerinin durumunu **Tüm satış siparişleri** listesi sayfasından görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="bed9e-129">**Açık müşteri faturaları** liste sayfasını deftere nakledilen faturaları görüntülemek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="bed9e-130">Sevk irsaliyesine ve tarihe dayalı olan tekil müşteri faturalarını deftere nakledin veya yazdırın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="bed9e-131">Bu işlemi, satış siparişine bir veya daha fazla sevk irsaliyesinin deftere nakledildiğinde kullanın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="bed9e-132">Müşteri faturası bu sevk irsaliyelerine dayanır ve bunların miktarlarını yansıtır.</span><span class="sxs-lookup"><span data-stu-id="bed9e-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="bed9e-133">Faturanın mali bilgileri, faturayı naklettiğinizde girilen bilgilere dayanır.</span><span class="sxs-lookup"><span data-stu-id="bed9e-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="bed9e-134">Belirli bir satış siparişi için olan tüm maddeler henüz sevk edilmemiş olsa bile, o tarihe kadar sevk edilmiş sevk irsaliyesi satır maddelerine dayanan bir satış müşteri faturası oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="bed9e-135">Bunu, örneğin, tüzel kişiliğiniz müşteri başına, o ayda sevk ettiğiniz tüm teslimatları içeren bir fatura kesiyorsa yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="bed9e-136">Her sevk irsaliyesi, satış siparişindeki maddelerin kısmen veya tamamen sevk edildiğini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="bed9e-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="bed9e-137">Faturayı deftere naklettiğinizde, her madde için **Faturan kalan** miktarı, seçili sevk irsaliyelerinden sevk edilmiş miktarların toplamı ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="bed9e-138">Eğer tüm maddeler için **Fatura kalanı** miktarı ve **Teslimat bakiyesi** satış siparişindeki miktarı 0 (sıfır) olursa, satış siparişinin durumu **Faturalandı** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="bed9e-139">Eğer **Fatura kalanı** miktarı 0 (sıfır) değilse, satış siparişinin durumu değiştirilmez ve buna ek faturalar girilebilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="bed9e-140">Stok hareketleri fatura numarasıyla güncelleştirilir ve satış siparişindeki **Satır durumu** alanı **Faturalandı** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="bed9e-141">Satış siparişlerinin durumunu **Tüm satış siparişleri** listesi sayfasından görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="bed9e-142">Satış siparişlerini veya sevk irsaliyelerini deftere nakletmek için konsolide edin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="bed9e-143">Bu işlemi, bir veya daha fazla satış siparişi faturalanmaya hazır durumda olduğunda ve bunları tek bir faturada birleştirmek istediğinizde kullanın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="bed9e-144">**Satış siparişi** liste sayfasında birden fazla fatura seçebilirsiniz ve sonra **Faturalar oluştur**'u kullanarak bunları birleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="bed9e-145">**Sipariş özeti** ayarını, **Faturayı deftere nakletme** sayfasında siparişi numarasına göre özetlemek için (tek bir satış siparişi için birden çok sevk irsaliyesi olduğunda) veya fatura hesabına göre (tek bir fatura hesabı için birden fazla satış siparişi bulunduğunda) değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="bed9e-146">**Yerleştir** düğmesini kullanıp satış siparişlerini **Sipariş özeti** ayarlarına dayanarak tek bir faturada bir araya getirin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="bed9e-147">Deftere nakil davranışını değiştiren ek ayarlar</span><span class="sxs-lookup"><span data-stu-id="bed9e-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="bed9e-148">Aşağıdaki alanlar deftere nakil işleminin davranışını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bed9e-149">Alan</span><span class="sxs-lookup"><span data-stu-id="bed9e-149">Field</span></span></th>
<th><span data-ttu-id="bed9e-150">Açıklama</span><span class="sxs-lookup"><span data-stu-id="bed9e-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bed9e-151">Miktar</span><span class="sxs-lookup"><span data-stu-id="bed9e-151">Quantity</span></span></td>
<td><span data-ttu-id="bed9e-152">Belgenin deftere naklinde temel alınacak miktarları seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="bed9e-153">Kullanılabilecek seçenekler, hangi türde bir belgeyi naklettiğinize göre, örneğin sevk irsaliyesi veya fatura gibi, değişmektedir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="bed9e-154"><strong>Şimdi teslim et</strong>: <strong>Şimdi teslim et</strong> alanına girilen tüm miktarları seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="bed9e-155">Bu seçeneği kısmi bir siparişi onaylamak veya teslim etmek için kullanın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="bed9e-156"><strong>Çekilen</strong>: Çekilen tüm miktarları seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="bed9e-157"><strong>Tümü</strong> – Geçerli belge türü ile henüz güncelleştirilmeyen satış siparişlerindeki tüm miktarları seçmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bed9e-157"><strong>All</strong> – Select all quantities on the sales order that haven&#39;t yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="bed9e-158"><strong>Sevk irsaliyesi</strong>: Sevk irsaliyesiyle güncelleştirilen tüm miktarları seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="bed9e-159"><strong>Çekilen miktar ve stoklanmayan ürünler</strong> – Çekilen tüm miktarları ve stoklanmamış tüm ürün miktarlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren&#39;t stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed9e-160">Deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="bed9e-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="bed9e-161">Satış siparişini günlüğe girmek için bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="bed9e-162">Proforma satış siparişi yazdırmak için bu seçeneği kaldırın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="bed9e-163"><strong>Not:</strong> Ödeme planı için anlaşma yaptıysanız, ödeme planı proforma satış siparişinde gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="bed9e-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn&#39;t shown on the pro forma sales order.</span></span> <span data-ttu-id="bed9e-164">Ödeme planları yalnızca fiili satış emirlerinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed9e-165">Geç seçim</span><span class="sxs-lookup"><span data-stu-id="bed9e-165">Late selection</span></span></td>
<td><span data-ttu-id="bed9e-166">Seçili sorguyu daha sonra uygulamak için bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="bed9e-167">Bu seçenek, toplu işler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bed9e-167">This option is used for batch jobs.</span></span> <span data-ttu-id="bed9e-168">Toplu iş çalıştırıldığında, sorgu çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="bed9e-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed9e-169">Miktarı azalt</span><span class="sxs-lookup"><span data-stu-id="bed9e-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="bed9e-170">Belge deftere nakledildiğinde, teslim edilen miktarın kullanılabilir stoğa eşit olması için teslim edilen miktarı otomatik olarak azaltmak için bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed9e-171">Yazdır</span><span class="sxs-lookup"><span data-stu-id="bed9e-171">Print</span></span></td>
<td><span data-ttu-id="bed9e-172">Belgelerin ne zaman yazdırılacağını seçin:</span><span class="sxs-lookup"><span data-stu-id="bed9e-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="bed9e-173"><strong>Cari</strong> - Belgeleri her bir faturayı güncelleştirildikten sonra yazdırın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="bed9e-174"><strong>Sonra</strong>: Tüm faturalar güncelleştirildikten sonra belgeleri yazdırın.</span><span class="sxs-lookup"><span data-stu-id="bed9e-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="bed9e-175">
<strong>Not:</strong> <strong>Yazdır alanı</strong> yalnızca, <strong>Faturayı yazdır</strong>, <strong>Onayı yazdır</strong>, <strong>Malzeme çekme listesini yazdır</strong> veya <strong>Sevk irsaliyesi yazdır</strong> seçeneğini seçerseniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="bed9e-176">Örneğin, <strong>Form sıralaması</strong> sayfasında, sistemi bilgileri fatura hesabına göre sıralayacak şekilde ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="bed9e-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="bed9e-177">Fatura hesabı tarafından sıralanan toplu işteki belgeleri yazdırmak için <strong>Sonra</strong>'yı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="bed9e-178">Aksi halde, belgeler işleme tamamlanmadan önce yazdırılır ve belgeler <strong>Form sıralama</strong> sayfasında belirtilen sırada sıralanmaz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-178">Otherwise, the documents are printed before processing is completed, and the documents aren&#39;t sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed9e-179">Faturayı yazdır</span><span class="sxs-lookup"><span data-stu-id="bed9e-179">Print invoice</span></span></td>
<td><span data-ttu-id="bed9e-180">Faturayı yazdırmak için bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-180">Select this option to print the invoice.</span></span> <span data-ttu-id="bed9e-181">Bu seçenek devre dışı bırakılırsa, yazdırma olmadan bir faturayı deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bed9e-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed9e-182">E-posta gönder</span><span class="sxs-lookup"><span data-stu-id="bed9e-182">Send e-mail</span></span></td>
<td><span data-ttu-id="bed9e-183">Fatura deftere nakledildikten sonra satış siparişinin faturasını müşteriye e-posta eki göndermek için bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="bed9e-184">Ekler PDF ve XML dosyaları olarak gönderilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="bed9e-185">Bu seçenek yalnızca <strong>Elektronik fatura parametreleri </strong>sayfasındaki <strong>CFD etkinleştir (elektronik faturalar)</strong>'ı seçtiğinizde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="bed9e-186"><strong>Not:</strong> (MEX) Bu denetim yalnızca birincil adresi Meksika'daki tüzel kişilikler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed9e-187">Yazdırma yönetimi hedefini kullan</span><span class="sxs-lookup"><span data-stu-id="bed9e-187">Use print management destination</span></span></td>
<td><span data-ttu-id="bed9e-188">Bu seçeneği <strong>Yazdırma Yönetimi Kurulumu</strong> sayfasında hareket, belge veya modülü üzerinde belirtilen yazdırma ayarlarını kullanmak için seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed9e-189">Kredi limitini denetle</span><span class="sxs-lookup"><span data-stu-id="bed9e-189">Check credit limit</span></span></td>
<td><span data-ttu-id="bed9e-190">Kredi limiti denetimi gerçekleştirilirken analiz edilmesi gereken bilgileri seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="bed9e-191"><strong>Yok</strong>: Kredi limiti kontrolü için bir gereksinim mevcut değildir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="bed9e-192"><strong>Bakiye</strong> - Kredi limiti müşteri bakiyesine karşı denetlenir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="bed9e-193"><strong>Bakiye + sevk irsaliyesi veya ürün girişi</strong>: Kredi limiti müşteri bakiyesi ve teslimatlara göre denetlenir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="bed9e-194"><strong>Bakiye + Tümü</strong> - Kredi limiti müşteri bakiyesiyle, teslimatlarla ve açık siparişlerle karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="bed9e-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed9e-195">Alacak düzeltme</span><span class="sxs-lookup"><span data-stu-id="bed9e-195">Credit correction</span></span></td>
<td><span data-ttu-id="bed9e-196">Alacak dekontunu fiş hareketlerinde borç olarak görüntülemek için bu seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bed9e-197">Kalan alacak miktarı</span><span class="sxs-lookup"><span data-stu-id="bed9e-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="bed9e-198">Borç dekontunu deftere naklediyorsanız, kalan miktarı siparişte bırakmak için bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-198">If you&#39;re posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="bed9e-199">Bu seçenek işaretlenmezse kalan miktar 0 (sıfır) olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="bed9e-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed9e-200">Özet güncelleştirme kapsamı</span><span class="sxs-lookup"><span data-stu-id="bed9e-200">Summary update for</span></span></td>
<td><span data-ttu-id="bed9e-201">Birden fazla satış siparişinin nasıl özetlenmesi gerektiğini seçin:</span><span class="sxs-lookup"><span data-stu-id="bed9e-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="bed9e-202"><strong>Hiçbiri</strong> - Satış siparişlerini özetleme.</span><span class="sxs-lookup"><span data-stu-id="bed9e-202"><strong>None</strong> – Don&#39;t summarize sales orders.</span></span> <span data-ttu-id="bed9e-203">Örneğin, her satış siparişi için ayrı bir fatura oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bed9e-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="bed9e-204"><strong>Fatura hesabı</strong>: Seçilen tüm siparişleri <strong>Özet güncelleştirme parametreleri</strong> sayfasında ayarlanmış olan ölçüte göre özetleyin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="bed9e-205"><strong>Sipariş</strong>: Seçilen aralıktaki siparişlerin tek bir sipariş olarak özetler.</span><span class="sxs-lookup"><span data-stu-id="bed9e-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="bed9e-206">Siparişler, <strong>Özet güncelleştirme parametreleri</strong> sayfasında ayarlanan ölçütlere göre özetlenir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="bed9e-207">Bu seçenek işaretlerseniz, <strong>Satış siparişi</strong> alanında bir değer işaretlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="bed9e-208"><strong>Otomatik özet</strong>: Eğer özet güncelleştirmeleri <strong>Özet güncelleştirme</strong> sayfasında belirtildiyse, <strong>Özet güncelleştirme parametreleri</strong> sayfasında belirlenen kriterlere dayanarak tüm siparişleri özetleyin.</span><span class="sxs-lookup"><span data-stu-id="bed9e-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="bed9e-209">Eğer Özet güncelleştirmeleri belirlemezseniz, sipariş ayrı olarak deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-209">If summary updates haven&#39;t been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="bed9e-210"><strong>Sevk irsaliyesi</strong>: Seçilen aralıktaki siparişleri sevk irsaliyesi başına bir fatura şeklinde özetler.</span><span class="sxs-lookup"><span data-stu-id="bed9e-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="bed9e-211">Bu seçenek yalnızca, <strong>Miktar</strong> alanında <strong>Sevk irsaliyesi</strong> seçiliyse kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bed9e-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





