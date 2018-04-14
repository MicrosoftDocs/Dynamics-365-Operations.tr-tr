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
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 510e3ac8bbec891436eaf6849dfe00b68ba2eb40
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="ae92f-104">Satıcı faturaları için hesap dağıtımları ve muavin defteri günlük girdileri</span><span class="sxs-lookup"><span data-stu-id="ae92f-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ae92f-105">Muhasebe dağılımları, bir tutarın, örneğin giderin, verginin veya masrafların, bir satıcı faturasında nasıl hesaba katılacağını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ae92f-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="ae92f-106">Satıcı faturası günlüğe kaydedildiğinde hesaba katılması gereken tüm tutarlar, bir veya daha fazla muhasebe dağıtımına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ae92f-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="ae92f-107">Muhasebe dağılımları</span><span class="sxs-lookup"><span data-stu-id="ae92f-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="ae92f-108">Satıcı faturası sayfasında aşağıdaki düğmeleri kullanarak satıcı faturası üzerindeki her bir satır için muhasebe dağılımlarını görüntüleyebilir ve değiştirebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ae92f-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="ae92f-109">**Tutarları dağıtmak** – Vergiler ve masraflar gibi tek bir satır ve tüm alt satırların muhasebe dağılımlarını görüntüleyip değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="ae92f-110">Alt satır için muhasebe dağılımlarını da doğrudan satış vergisi hareketleri sayfasından veya Gider hareketlerini görüntüleyebilir ve değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae92f-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="ae92f-111">Satıcı faturası başlığındaki gider veya para birimi yuvarlama gibi tutarları değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="ae92f-112">Satıcı faturası satırı tutarlarını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="ae92f-113">**Dağılımları görüntülemek** – Belge üzerindeki tüm satırların muhasebe dağılımlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="ae92f-114">Muhasebe dağılımlarını bu görünümden değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae92f-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="ae92f-115">Başlığı ve satır tutarlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-115">View header and line amounts.</span></span>

<span data-ttu-id="ae92f-116">Satıcı faturası bir satınalma emrini referans alıyorsa, stoklanmamış bir madde içeren satırlar için muhasebe dağılımlarını bölüp değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae92f-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="ae92f-117">Satıcı faturası satırı bir satınalma emri satırını referans almıyorsa, muhasebe dağılımını silmeniz de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="ae92f-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="ae92f-118">Masraflar, vergiler ve satır iskontoları için satırları bölemez veya silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae92f-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="ae92f-119">Genel muhasebe hesabını değiştirebilirsiniz, ancak tutarları veya yüzdeleri değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae92f-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="ae92f-120">Ana satırda stoklanmamış bir madde varsa ve muhasebe dağılımları bölünmüşse, alt satır ana satırın mali boyutları ile eşleşecek şekilde otomatik olarak bölünecektir.</span><span class="sxs-lookup"><span data-stu-id="ae92f-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="ae92f-121">Alt satır için muhasebe dağılımları ayrıca bölünemez veya silinemez ancak alt satırın kurulumuna bağlı olarak, alt satırın muhasebe dağılımlarına yönelik ana muhasebe hesabını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae92f-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="ae92f-122">Dağılım tutarları</span><span class="sxs-lookup"><span data-stu-id="ae92f-122">Distributing amounts</span></span>
<span data-ttu-id="ae92f-123">Satıcı faturası girdiğinizde, her tutar aşağıdaki şekilde dağılır.</span><span class="sxs-lookup"><span data-stu-id="ae92f-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae92f-124">Satıcı faturası satırının türü</span><span class="sxs-lookup"><span data-stu-id="ae92f-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="ae92f-125">Ana hesabın nereden görüntüleneceğini belirleyen öncelik sırası</span><span class="sxs-lookup"><span data-stu-id="ae92f-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="ae92f-126">Hangi varsayılan mali boyutun görüntüleneceğini belirleyen öncelik sırası</span><span class="sxs-lookup"><span data-stu-id="ae92f-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae92f-127">Stoğu tutulan ürün</span><span class="sxs-lookup"><span data-stu-id="ae92f-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="ae92f-128">Satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-129">Deftere nakletme sayfasında Ürün için satınalma harcaması seçiliyken Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-130">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-131">Satıcı faturası üzerindeki varsayılan mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae92f-132">Bir tedarik kategori veya ürün stoklanmamış</span><span class="sxs-lookup"><span data-stu-id="ae92f-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="ae92f-133">Satınalma emri satırı için muhasebe dağılımı, satıcı faturası satırı bir satınalma emri satırını referans alıyorsa.</span><span class="sxs-lookup"><span data-stu-id="ae92f-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-134">Deftere nakletme sayfasında Harcama için satınalma harcaması seçiliyken Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-135">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-136">Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="ae92f-137">Satıcı faturası üzerindeki varsayılan mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="ae92f-138">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-139">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae92f-140">Sabit kıymet</span><span class="sxs-lookup"><span data-stu-id="ae92f-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="ae92f-141">Satınalma emri satırı için muhasebe dağılımı, satıcı faturası satırı bir satınalma emri satırını referans alıyorsa.</span><span class="sxs-lookup"><span data-stu-id="ae92f-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-142">Satıcı faturası formundaki Hareket türü alanında Alım seçili ise, Sabit kıymet nakil profilleri sayfasında Alım seçiliyken ise Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="ae92f-143">Satıcı faturası formundaki Hareket türü alanında Alım ayarlama seçili ise, Sabit kıymet nakil profilleri sayfasında Alım seçiliyken ise Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-144">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-145">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-146">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae92f-147">Satıcı faturası satırında tanımlı proje</span><span class="sxs-lookup"><span data-stu-id="ae92f-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="ae92f-148">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-149">Proje grupları sayfasındaki Maliyetleri naklet - madde alanında Bakiye seçili ise, Genel muhasebe defterine nakil ayarı sayfasında Maliyet seçiliyken Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="ae92f-150">Proje grupları sayfasındaki Maliyetleri naklet - madde alanında Kar ve zarar seçili ise, Genel muhasebe defterine nakil ayarı sayfasında Maliyet - madde seçiliyken Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-151">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae92f-152">Satır iskontosu</span><span class="sxs-lookup"><span data-stu-id="ae92f-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="ae92f-153">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-154">Nakil sayfasında İskonto seçiliyken Ana hesap alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="ae92f-155">Bir iskonto için deftere nakil profilinde ana muhasebe tanımlı değilse, satınalma emri satırındaki genişletilmiş fiyatın muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-156">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-157">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-158">Satıcı faturası satırı için mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-159">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae92f-160">Satınalma emri satırının Fiyat ve iskonto sekmesine girilen satınalma masrafı</span><span class="sxs-lookup"><span data-stu-id="ae92f-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="ae92f-161">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-162">Satınalma emri satırındaki genişletilmiş fiyatın muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-163">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-164">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae92f-165">Satır masrafı</span><span class="sxs-lookup"><span data-stu-id="ae92f-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="ae92f-166">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-167">Masraflar kodu formundaki borç Türü alanında Genel muhasebe seçili ise, Masraflar kodu sayfasındaki borç Hesabı alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="ae92f-168">Masraflar kodu formundaki borç Türü alanında Madde seçiliyse, satınalma emri satırındaki genişletilmiş fiyat için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-169">Masraflar kodu formundaki borç Türü alanında Müşteri/Satıcı seçili ise, Masraflar kodu sayfasındaki kredi Hesabı alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-170">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-171">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-172">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-173">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae92f-174">Aşağıdaki koşulla vergi:</span><span class="sxs-lookup"><span data-stu-id="ae92f-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="ae92f-175">Genel muhasebe parametreleri sayfasında ABD vergilendirme kurallarını uygula seçeneği seçili.</span><span class="sxs-lookup"><span data-stu-id="ae92f-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="ae92f-176">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-177">Genişletilmiş fiyatın veya masrafın muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-178">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-179">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-180">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae92f-181">Aşağıdaki koşullarla vergi:</span><span class="sxs-lookup"><span data-stu-id="ae92f-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="ae92f-182">Genel muhasebe parametreleri sayfasında ABD vergilendirme kurallarını uygula seçeneği seçili değil.</span><span class="sxs-lookup"><span data-stu-id="ae92f-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="ae92f-183">Satış vergi grupları sayfasında Satış vergi grubu için vergi alanını kullan seçili değil.</span><span class="sxs-lookup"><span data-stu-id="ae92f-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="ae92f-184">Vergi tutarı düşülebilir ise, Genel muhasebe deftere nakil grupları sayfasındaki Satış vergisi alacakları alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="ae92f-185">Vergi tutarı düşülebilir değilse, masraf için genişletilmiş fiyat veya muhasebe dağılımı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-186">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-187">Satıcı faturası satırındaki masraf için genişletilmiş fiyat veya muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-188">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-189">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae92f-190">Aşağıdaki koşullarla vergi:</span><span class="sxs-lookup"><span data-stu-id="ae92f-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="ae92f-191">Genel muhasebe parametreleri sayfasında ABD vergilendirme kurallarını uygula seçeneği seçili değil.</span><span class="sxs-lookup"><span data-stu-id="ae92f-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="ae92f-192">Satış vergi grupları sayfasında Satış vergi grubu için vergi alanını kullan seçili.</span><span class="sxs-lookup"><span data-stu-id="ae92f-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="ae92f-193">Vergi tutarı düşülebilir ise, Genel muhasebe deftere nakil grupları sayfasındaki Satış vergisi alacakları alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="ae92f-194">Vergi tutarı düşülebilir değilse, Genel muhasebe deftere nakil grupları sayfasındaki Kullanım vergisi gideri alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-195">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-196">Satıcı faturası satırındaki masraf için genişletilmiş fiyat veya muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-197">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-198">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae92f-199">Masraf başlığı</span><span class="sxs-lookup"><span data-stu-id="ae92f-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="ae92f-200">Masraflar kodu formundaki borç Türü alanında Genel muhasebe seçili ise, Masraflar kodu sayfasındaki borç Hesabı alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="ae92f-201">Masraflar kodu formundaki borç Türü alanında Müşteri/Satıcı seçili ise, Masraflar kodu sayfasındaki kredi Hesabı alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-202">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-203">Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="ae92f-204">Satıcı faturası başlığından gelen mali boyut varsayılan şablon değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="ae92f-205">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-206">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae92f-207">Başlık iskontosu</span><span class="sxs-lookup"><span data-stu-id="ae92f-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="ae92f-208">Otomatik hareketler sayfasındaki Hesaplar içindeki Satıcı faturası iskontosu deftere nakil türü için Ana muhasebe alanı.</span><span class="sxs-lookup"><span data-stu-id="ae92f-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="ae92f-209">Fatura satırı bir satınalma emri satırını referans alıyorsa, satınalma emri satırı için muhasebe dağılımını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="ae92f-210">Satıcı fatura satırındaki genişletilmiş fiyat için muhasebe dağılımlarından gelen mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-211">Satıcı faturası satırından mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="ae92f-212">Hesap planları sayfasındaki ana muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="ae92f-213">Vergileri dağıtma</span><span class="sxs-lookup"><span data-stu-id="ae92f-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="ae92f-214">Vergiler için muhasebe dağılımları, vergiler hesaplanana dek oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="ae92f-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="ae92f-215">Satış vergilerini hesaplamak için Satıcı faturası sayfasında aşağıdaki görevleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="ae92f-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="ae92f-216">Fatura toplamını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-216">View the invoice total.</span></span>
-   <span data-ttu-id="ae92f-217">Satış vergisini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-217">View the sales tax.</span></span>
-   <span data-ttu-id="ae92f-218">Yardımcı defter günlüğünü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-218">View the subledger journal.</span></span>
-   <span data-ttu-id="ae92f-219">Komple satıcı faturası için muhasebe dağılımlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="ae92f-220">Satıcı faturasını beklemeye alın.</span><span class="sxs-lookup"><span data-stu-id="ae92f-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="ae92f-221">Satıcı faturasını deftere nakledin.</span><span class="sxs-lookup"><span data-stu-id="ae92f-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="ae92f-222">Satıcı faturaları için muavin defteri günlükleri</span><span class="sxs-lookup"><span data-stu-id="ae92f-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="ae92f-223">Bir satıcı faturasını deftere nakletmeden önce, faturanın doğru hesaplara nakledildiğini teyit etmek için, borçlar ve alacaklar dahil, faturanın tüm muhasebe girdisini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae92f-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="ae92f-224">Bu tam görünümün muavin defteri günlük hesap girişi olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="ae92f-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="ae92f-225">Satıcı faturasını günlüğe geçirmeden önce önizlemesini görüntülediğinizde muavin defteri günlük girdisi yanlış ise, muavin defteri günlük girdisi değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae92f-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="ae92f-226">Bunun yerine, hesap dağılımlarını veya deftere nakil profilini değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ae92f-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="ae92f-227">Hesap dağıtımları muhasebe girişi, Borç veya alacak bir tarafı tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ae92f-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="ae92f-228">Mahsup eden muavin defteri günlüğü hesabı girişi, satıcı hesabından veya vergi gibi deftere nakil profilleri kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ae92f-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>






