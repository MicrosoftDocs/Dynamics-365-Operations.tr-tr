---
title: "Serbest metin faturaları için hesap dağıtımları ve muavin defteri günlük girdileri"
description: "Muhasebe dağılımları, bir tutarın, örneğin gelirin, verginin veya masrafların bir serbest metin faturasında nasıl hesaba katılacağını tanımlamak için kullanılır. Serbest metin faturası günlüğe kaydedildiğinde hesaba katılması gereken tüm tutarlar, bir veya daha fazla muhasebe dağıtımına sahip olacaktır."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e413a5aaba59215790ed5c5460e8c95c47f18973
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="4f676-104">Serbest metin faturaları için hesap dağıtımları ve muavin defteri günlük girdileri</span><span class="sxs-lookup"><span data-stu-id="4f676-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f676-105">Muhasebe dağılımları, bir tutarın, örneğin gelirin, verginin veya masrafların bir serbest metin faturasında nasıl hesaba katılacağını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4f676-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="4f676-106">Serbest metin faturası günlüğe kaydedildiğinde hesaba katılması gereken tüm tutarlar, bir veya daha fazla muhasebe dağıtımına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4f676-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="4f676-107">Muhasebe dağılımları</span><span class="sxs-lookup"><span data-stu-id="4f676-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="4f676-108">Serbest metin faturası sayfasında aşağıdaki düğmeleri kullanarak serbest metin faturası üzerindeki her bir satır için muhasebe dağılımlarını görüntüleyebilir ve değiştirebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4f676-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="4f676-109">**Tutarları dağıtmak**—Vergiler ve masraflar gibi tek bir satır ve tüm alt satırların muhasebe dağılımlarını görüntüleyip, değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4f676-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="4f676-110">Alt satır için muhasebe dağılımlarını da doğrudan satış vergisi hareketleri sayfasından veya Gider hareketlerini görüntüleyebilir ve değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f676-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="4f676-111">Serbest metin faturası başlığındaki tutarlar, örneğin gider veya para birimi yuvarlama tutarlarını, değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4f676-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="4f676-112">Serbest metin faturası satır tutarlarını değiştirme</span><span class="sxs-lookup"><span data-stu-id="4f676-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="4f676-113">**Dağılımları görüntülemek**— Belge üzerindeki tüm satırların muhasebe dağılımlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4f676-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="4f676-114">Muhasebe dağılımlarını bu görünümden değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f676-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="4f676-115">Başlığı ve satır tutarlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4f676-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="4f676-116">Dağılım tutarları</span><span class="sxs-lookup"><span data-stu-id="4f676-116">Distributing amounts</span></span>
<span data-ttu-id="4f676-117">Serbest metin faturası girdiğinizde, her tutar aşağıdaki şekilde dağılır.</span><span class="sxs-lookup"><span data-stu-id="4f676-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f676-118">Parasal tutarın türü</span><span class="sxs-lookup"><span data-stu-id="4f676-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="4f676-119">Ana hesabın nereden görüntüleneceği</span><span class="sxs-lookup"><span data-stu-id="4f676-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="4f676-120">Hangi varsayılan mali boyutun görüntüleneceğini belirleyen öncelik sırası</span><span class="sxs-lookup"><span data-stu-id="4f676-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4f676-121">Serbest metin faturası satırı</span><span class="sxs-lookup"><span data-stu-id="4f676-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="4f676-122">Serbest metin fatura satırındaki genel muhasebe hesabı.</span><span class="sxs-lookup"><span data-stu-id="4f676-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="4f676-123">Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="4f676-124">Ana hesap tahsisat hesabı değilse, serbest metin faturası satırındaki mali boyut varsayılan şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4f676-125">Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4f676-126">Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f676-127">Sabit kıymet numarası ve değer modeli birleşimi için serbest metinli fatura satırı</span><span class="sxs-lookup"><span data-stu-id="4f676-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4f676-128"><strong>Not </strong></span><span class="sxs-lookup"><span data-stu-id="4f676-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4f676-129">Serbest metin faturası satırındaki ana hesap, sabit kıymet elden hesabı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4f676-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="4f676-130">Serbest metin fatura satırındaki genel muhasebe hesabı.</span><span class="sxs-lookup"><span data-stu-id="4f676-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="4f676-131">Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4f676-132">Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f676-133">Serbest metinli fatura iskonto tutarı</span><span class="sxs-lookup"><span data-stu-id="4f676-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="4f676-134">Ana hesap müşteri nakit iskontolarının sayfa alanında iskontoları.</span><span class="sxs-lookup"><span data-stu-id="4f676-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="4f676-135">Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="4f676-136">Ana hesap tahsisat hesabı değilse, serbest metin faturası satırındaki mali boyut varsayılan şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4f676-137">Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4f676-138">Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4f676-139">Serbest metin faturası satış vergisi tutarı</span><span class="sxs-lookup"><span data-stu-id="4f676-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="4f676-140">Genel muhasebe deftere nakil grupları sayfasındaki satış vergisi borcu alanı.</span><span class="sxs-lookup"><span data-stu-id="4f676-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="4f676-141">Serbest metin faturası satır tutarında veya satır tutarı dağıtım giderinde tanımlanan mali boyutları kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="4f676-142">Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4f676-143">Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4f676-144">Serbest metin faturası masraf satır tutarı</span><span class="sxs-lookup"><span data-stu-id="4f676-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="4f676-145">Masraflar kodu sayfasındaki alacak hesabı alanı.</span><span class="sxs-lookup"><span data-stu-id="4f676-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="4f676-146">Ana hesap bir tahsisat hesabıysa, tahsisat hesap tanımından varsayılan değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="4f676-147">Ana hesap tahsisat hesabı değilse, serbest metin faturası satırındaki mali boyut varsayılan şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4f676-148">Serbest metin faturası satırındaki varsayılan mali boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="4f676-149">Hesap planı sayfasındaki genel muhasebe hesabının varsayılan finansal boyut değerlerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f676-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="4f676-150">Vergileri dağıtma</span><span class="sxs-lookup"><span data-stu-id="4f676-150">Distributing taxes</span></span>
<span data-ttu-id="4f676-151">Vergiler için muhasebe dağılımları, vergiler hesaplanana dek oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="4f676-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="4f676-152">Satış vergilerini hesaplamak için serbest metin faturası formunda aşağıdaki görevleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="4f676-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="4f676-153">Satış vergisini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4f676-153">View the sales tax.</span></span>
-   <span data-ttu-id="4f676-154">Fatura toplamını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4f676-154">View the invoice total.</span></span>
-   <span data-ttu-id="4f676-155">Nakit akışı tahminini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4f676-155">View the cash flow.</span></span>
-   <span data-ttu-id="4f676-156">Serbest metin faturasının tamamının içindeki muhasebe dağılımlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4f676-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="4f676-157">Yardımcı defter günlüğünü görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4f676-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="4f676-158"> Serbest metin faturaları için muavin defter günlükleri</span><span class="sxs-lookup"><span data-stu-id="4f676-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="4f676-159">Tam bir serbest metin faturasını deftere nakletmeden önce, faturanın doğru hesaplara nakledildiğini teyit etmek için, borçlar ve alacaklar dahil, faturanun tüm muhasebe girdisini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f676-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="4f676-160">Bu tam görünümün muavin defteri günlük hesap girişi olarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="4f676-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="4f676-161">Serbest metin faturasını günlüğe geçirmeden önce önizlemesini görüntülediğinizde muavin defteri günlük girdisi yanlış ise, muavin defteri günlük girdisi değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f676-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="4f676-162">Bunun yerine, hesap dağıtımları veya deftere nakil profili değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4f676-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="4f676-163">Hesap dağıtımları muhasebe girişi, Borç veya alacak bir tarafı tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4f676-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="4f676-164">Muavin defteri günlük mahsuplaştırma hesabı girişi deftere nakil profilleri gibi müşteri hesabı ya da vergi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4f676-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>




