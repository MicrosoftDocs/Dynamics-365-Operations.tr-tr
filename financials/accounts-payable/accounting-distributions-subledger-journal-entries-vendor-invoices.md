---
title: "Satıcı faturaları için hesap dağıtımları ve muavin defteri günlük girdileri"
description: "Muhasebe dağılımları, bir tutarın, örneğin giderin, verginin veya masrafların, bir satıcı faturasında nasıl hesaba katılacağını tanımlamak için kullanılır. Satıcı faturası günlüğe kaydedildiğinde hesaba katılması gereken tüm tutarlar, bir veya daha fazla muhasebe dağıtımına sahip olacaktır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8169c32dc47c1635f6d3d00852d14d677678868
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="12993-104">Satıcı faturaları için hesap dağıtımları ve muavin defteri günlük girdileri</span><span class="sxs-lookup"><span data-stu-id="12993-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="12993-105">Muhasebe dağılımları, bir tutarın, örneğin giderin, verginin veya masrafların, bir satıcı faturasında nasıl hesaba katılacağını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12993-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="12993-106">Satıcı faturası günlüğe kaydedildiğinde hesaba katılması gereken tüm tutarlar, bir veya daha fazla muhasebe dağıtımına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="12993-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="12993-107">Muhasebe dağılımları</span><span class="sxs-lookup"><span data-stu-id="12993-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="12993-108">Satıcı faturası sayfasında aşağıdaki düğmeleri kullanarak satıcı faturası üzerindeki her bir satır için muhasebe dağılımlarını görüntüleyebilir ve değiştirebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="12993-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="12993-109">**Tutarları dağıtmak** – Vergiler ve masraflar gibi tek bir satır ve tüm alt satırların muhasebe dağılımlarını görüntüleyip değiştirin.</span><span class="sxs-lookup"><span data-stu-id="12993-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="12993-110">Alt satır için muhasebe dağılımlarını da doğrudan satış vergisi hareketleri sayfasından veya Gider hareketlerini görüntüleyebilir ve değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12993-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="12993-111">Satıcı faturası başlığındaki gider veya para birimi yuvarlama gibi tutarları değiştirin.</span><span class="sxs-lookup"><span data-stu-id="12993-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="12993-112">Satıcı faturası satırı tutarlarını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="12993-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="12993-113">**Dağılımları görüntülemek** – Belge üzerindeki tüm satırların muhasebe dağılımlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="12993-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="12993-114">Muhasebe dağılımlarını bu görünümden değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="12993-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="12993-115">Başlığı ve satır tutarlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="12993-115">View header and line amounts.</span></span>

<span data-ttu-id="12993-116">Satıcı faturası bir satınalma emrini referans alıyorsa, stoklanmamış bir madde içeren satırlar için muhasebe dağılımlarını bölüp değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12993-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="12993-117">Satıcı faturası satırı bir satınalma emri satırını referans almıyorsa, muhasebe dağılımını silmeniz de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="12993-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="12993-118">Masraflar, vergiler ve satır iskontoları için satırları bölemez veya silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="12993-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="12993-119">Genel muhasebe hesabını değiştirebilirsiniz, ancak tutarları veya yüzdeleri değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="12993-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="12993-120">Ana satırda stoklanmamış bir madde varsa ve muhasebe dağılımları bölünmüşse, alt satır ana satırın mali boyutları ile eşleşecek şekilde otomatik olarak bölünecektir.</span><span class="sxs-lookup"><span data-stu-id="12993-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="12993-121">Alt satır için muhasebe dağılımları ayrıca bölünemez veya silinemez ancak alt satırın kurulumuna bağlı olarak, alt satırın muhasebe dağılımlarına yönelik ana muhasebe hesabını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12993-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="12993-122">Dağılım tutarları</span><span class="sxs-lookup"><span data-stu-id="12993-122">Distributing amounts</span></span>
<span data-ttu-id="12993-123">Satıcı faturası girdiğinizde, her tutar aşağıdaki şekilde dağılır.</span><span class="sxs-lookup"><span data-stu-id="12993-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12993-124">Satıcı faturası satırının türü</span><span class="sxs-lookup"><span data-stu-id="12993-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="12993-125">Ana hesabın nereden görüntüleneceğini belirleyen öncelik sırası</span><span class="sxs-lookup"><span data-stu-id="12993-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="12993-126">Hangi varsayılan mali boyutun görüntüleneceğini belirleyen öncelik sırası</span><span class="sxs-lookup"><span data-stu-id="12993-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12993-127">Stoğu tutulan ürün</span><span class="sxs-lookup"><span data-stu-id="12993-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="12993-128">Satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-129">Deftere nakletme sayfasında Ürün için satınalma harcaması seçiliyken Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-130">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-131">Satıcı faturası üzerindeki varsayılan mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12993-132">Bir tedarik kategori veya ürün stoklanmamış</span><span class="sxs-lookup"><span data-stu-id="12993-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="12993-133">Satınalma emri satırı için muhasebe dağılımı, satıcı faturası satırı bir satınalma emri satırını referans alıyorsa.</span><span class="sxs-lookup"><span data-stu-id="12993-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="12993-134">Deftere nakletme sayfasında Harcama için satınalma harcaması seçiliyken Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-135">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-136">Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="12993-137">Satıcı faturası üzerindeki varsayılan mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="12993-138">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-139">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12993-140">Sabit kıymet</span><span class="sxs-lookup"><span data-stu-id="12993-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="12993-141">Satınalma emri satırı için muhasebe dağılımı, satıcı faturası satırı bir satınalma emri satırını referans alıyorsa.</span><span class="sxs-lookup"><span data-stu-id="12993-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="12993-142">Satıcı faturası formundaki Hareket türü alanında Alım seçili ise, Sabit kıymet nakil profilleri sayfasında Alım seçiliyken ise Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="12993-143">Satıcı faturası formundaki Hareket türü alanında Alım ayarlama seçili ise, Sabit kıymet nakil profilleri sayfasında Alım seçiliyken ise Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-144">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="12993-145">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-146">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12993-147">Satıcı faturası satırında tanımlı proje</span><span class="sxs-lookup"><span data-stu-id="12993-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="12993-148">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="12993-149">Proje grupları sayfasındaki Maliyetleri naklet - madde alanında Bakiye seçili ise, Genel muhasebe defterine nakil ayarı sayfasında Maliyet seçiliyken Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="12993-150">Proje grupları sayfasındaki Maliyetleri naklet - madde alanında Kar ve zarar seçili ise, Genel muhasebe defterine nakil ayarı sayfasında Maliyet - madde seçiliyken Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-151">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12993-152">Satır iskontosu</span><span class="sxs-lookup"><span data-stu-id="12993-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="12993-153">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="12993-154">Nakil sayfasında İskonto seçiliyken Ana hesap alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="12993-155">Bir iskonto için deftere nakil profilinde ana muhasebe tanımlı değilse, satınalma emri satırındaki genişletilmiş fiyatın muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-156">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-157">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-158">Satıcı faturası satırı için mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-159">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12993-160">Satınalma emri satırının Fiyat ve iskonto sekmesine girilen satınalma masrafı</span><span class="sxs-lookup"><span data-stu-id="12993-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="12993-161">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="12993-162">Satınalma emri satırındaki genişletilmiş fiyatın muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-163">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-164">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12993-165">Satır masrafı</span><span class="sxs-lookup"><span data-stu-id="12993-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="12993-166">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="12993-167">Masraflar kodu formundaki borç Türü alanında Genel muhasebe seçili ise, Masraflar kodu sayfasındaki borç Hesabı alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="12993-168">Masraflar kodu formundaki borç Türü alanında Madde seçiliyse, satınalma emri satırındaki genişletilmiş fiyat için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-169">Masraflar kodu formundaki borç Türü alanında Müşteri/Satıcı seçili ise, Masraflar kodu sayfasındaki kredi Hesabı alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-170">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-171">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-172">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-173">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12993-174">Aşağıdaki koşulla vergi:</span><span class="sxs-lookup"><span data-stu-id="12993-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="12993-175">Genel muhasebe parametreleri sayfasında ABD vergilendirme kurallarını uygula seçeneği seçili.</span><span class="sxs-lookup"><span data-stu-id="12993-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="12993-176">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="12993-177">Genişletilmiş fiyatın veya masrafın muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-178">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-179">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-180">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12993-181">Aşağıdaki koşullarla vergi:</span><span class="sxs-lookup"><span data-stu-id="12993-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="12993-182">Genel muhasebe parametreleri sayfasında ABD vergilendirme kurallarını uygula seçeneği seçili değil.</span><span class="sxs-lookup"><span data-stu-id="12993-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="12993-183">Satış vergi grupları sayfasında Satış vergi grubu için vergi alanını kullan seçili değil.</span><span class="sxs-lookup"><span data-stu-id="12993-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="12993-184">Vergi tutarı düşülebilir ise, Genel muhasebe deftere nakil grupları sayfasındaki Satış vergisi alacakları alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="12993-185">Vergi tutarı düşülebilir değilse, masraf için genişletilmiş fiyat veya muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="12993-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-186">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-187">Satıcı faturası satırındaki masraf için genişletilmiş fiyat veya muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-188">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-189">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12993-190">Aşağıdaki koşullarla vergi:</span><span class="sxs-lookup"><span data-stu-id="12993-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="12993-191">Genel muhasebe parametreleri sayfasında ABD vergilendirme kurallarını uygula seçeneği seçili değil.</span><span class="sxs-lookup"><span data-stu-id="12993-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="12993-192">Satış vergi grupları sayfasında Satış vergi grubu için vergi alanını kullan seçili.</span><span class="sxs-lookup"><span data-stu-id="12993-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="12993-193">Vergi tutarı düşülebilir ise, Genel muhasebe deftere nakil grupları sayfasındaki Satış vergisi alacakları alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="12993-194">Vergi tutarı düşülebilir değilse, Genel muhasebe deftere nakil grupları sayfasındaki Kullanım vergisi gideri alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-195">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-196">Satıcı faturası satırındaki masraf için genişletilmiş fiyat veya muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-197">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-198">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12993-199">Masraf başlığı</span><span class="sxs-lookup"><span data-stu-id="12993-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="12993-200">Masraflar kodu formundaki borç Türü alanında Genel muhasebe seçili ise, Masraflar kodu sayfasındaki borç Hesabı alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="12993-201">Masraflar kodu formundaki borç Türü alanında Müşteri/Satıcı seçili ise, Masraflar kodu sayfasındaki kredi Hesabı alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-202">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-203">Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="12993-204">Satıcı faturası başlığından gelen mali boyut varsayılan şablon değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="12993-205">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-206">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12993-207">Başlık iskontosu</span><span class="sxs-lookup"><span data-stu-id="12993-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="12993-208">Otomatik hareketler sayfasındaki Hesaplar içindeki Satıcı faturası iskontosu deftere nakil türü için Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="12993-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="12993-209">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="12993-210">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-211">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="12993-212">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12993-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

 
<a name="distributing-taxes"></a><span data-ttu-id="12993-213">Vergileri dağıtma</span><span class="sxs-lookup"><span data-stu-id="12993-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="12993-214">Vergiler için muhasebe dağılımları, vergiler hesaplanana dek oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="12993-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="12993-215">Satış vergilerini hesaplamak için Satıcı faturası sayfasında aşağıdaki görevleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="12993-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="12993-216">Fatura toplamını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="12993-216">View the invoice total.</span></span>
-   <span data-ttu-id="12993-217">Satış vergisini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="12993-217">View the sales tax.</span></span>
-   <span data-ttu-id="12993-218">Yardımcı defter günlüğünü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="12993-218">View the subledger journal.</span></span>
-   <span data-ttu-id="12993-219">Komple satıcı faturası için muhasebe dağılımlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="12993-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="12993-220">Satıcı faturasını beklemeye alın.</span><span class="sxs-lookup"><span data-stu-id="12993-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="12993-221">Satıcı faturasını deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="12993-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="12993-222">Satıcı faturaları için muavin defteri günlükleri</span><span class="sxs-lookup"><span data-stu-id="12993-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="12993-223">Bir satıcı faturasını deftere nakletmeden önce, faturanın doğru hesaplara nakledildiğini teyit etmek için, borçlar ve alacaklar dahil, faturanın tüm muhasebe girdisini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12993-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="12993-224">Bu tam görünümün muavin defteri günlük hesap girişi olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="12993-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="12993-225">Satıcı faturasını günlüğe geçirmeden önce önizlemesini görüntülediğinizde muavin defteri günlük girdisi yanlış ise, muavin defteri günlük girdisi değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="12993-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="12993-226">Bunun yerine, hesap dağılımlarını veya deftere nakil profilini değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="12993-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="12993-227">Hesap dağıtımları muhasebe girişi, Borç veya alacak bir tarafı tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="12993-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="12993-228">Mahsup eden muavin defteri günlüğü hesabı girişi, satıcı hesabından veya vergi gibi deftere nakil profilleri kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="12993-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>






