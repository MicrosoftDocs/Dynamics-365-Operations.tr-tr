---
title: "Eleme kuralları"
description: "Bu konuda, eleme kuralları ve elemeler hakkında raporlama için çeşitli seçenekler ile ilgili bilgiler verilmektedir."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0809ee798dc00ad3d252d5e8704259ea5cbe4956
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="elimination-rules"></a><span data-ttu-id="1ba76-103">Eleme kuralları</span><span class="sxs-lookup"><span data-stu-id="1ba76-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ba76-104">Bu konuda, eleme kuralları ve elemeler hakkında raporlama için çeşitli seçenekler ile ilgili bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="1ba76-105">Bir ana tüzel kişilik bir veya daha fazla tüzel kişilikle iş yapıyor ve konsolide finansal raporlama kullanıyorsa eleme hareketleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="1ba76-106">Konsolide mali tablolar yalnızca konsolide kuruluş ve bu kuruluşların dışındaki diğer varlıklar arasındaki hareketleri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="1ba76-107">Bu nedenle, aynı kuruluşun parçası olan tüzel kişilikler arasındaki hareketler genel muhasebeden kaldırılarak veya elenerek mali raporlarda görünmemesi sağlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ba76-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="1ba76-108">Elemeler hakkında rapor hazırlamanın birden çok yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="1ba76-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="1ba76-109">Konsolidasyon veya eleme şirketinde bir eleme kuralı oluşturabilir veya işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="1ba76-110">Elemeler hesaplarını ve boyutlarını belirli satır veya sütunda göstermek için mali raporlama kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="1ba76-111">Elemeleri izlemek üzere el ile hareket girişlerini nakletmek için ayrı bir tüzel kişilik kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="1ba76-112">Bu konuda, konsolidasyon veya eleme şirketinde işlenen eleme kurallarına odaklanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1ba76-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="1ba76-113">Elemeler için hedef tüzel kişilik olarak belirtilen bir tüzel kişilikte eleme hareketleri oluşturmak için eleme kuralları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="1ba76-114">Bu hedef tüzel kişilik, eleme tüzel kişiliği olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="1ba76-115">Eleme günlükleri konsolidasyon işlemi sırasında veya bir eleme günlüğü teklifi kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="1ba76-116">Eliminasyon günlükleri ayarlamadan önce aşağıdaki terimler hakkında bilginiz olmalı:</span><span class="sxs-lookup"><span data-stu-id="1ba76-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="1ba76-117">**Kaynak tüzel kişilik** – Elenmekte olan tutarların nakledildiği tüzel kişilik.</span><span class="sxs-lookup"><span data-stu-id="1ba76-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="1ba76-118">**Hedef tüzel kişilik** – Eleme kurallarının çıkarıldığı tüzel kişilik.</span><span class="sxs-lookup"><span data-stu-id="1ba76-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="1ba76-119">**Eleme tüzel kişiliği** – Elemeler içi hedef tüzel kişilik olarak belirtilen tüzel kişilik.</span><span class="sxs-lookup"><span data-stu-id="1ba76-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="1ba76-120">**Konsolide edilen tüzel kişilik** – Bir tüzel kişilikler grubu için oluşturulan mali sonuçların raporunu hazırlamak için oluşturulmuş bir tüzel kişilik.</span><span class="sxs-lookup"><span data-stu-id="1ba76-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="1ba76-121">Tüzel kişiliklerden gelen mali veriler bu tüzel kişilikte konsolide edilir ve birleştirilmiş veriler kullanılarak bir mali rapor oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1ba76-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="1ba76-122">Aşağıdaki tabloda, elenmesi gerekebilecek hareket türleri gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ba76-123">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="1ba76-123">Transaction type</span></span></th>
<th><span data-ttu-id="1ba76-124">Örnek</span><span class="sxs-lookup"><span data-stu-id="1ba76-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ba76-125">Satış siparişi girişi ve faturalandırma (merkezi işlem)</span><span class="sxs-lookup"><span data-stu-id="1ba76-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="1ba76-126">Bir müşteriye kuruluşunuzdaki başka bir tüzel kişilik adına bir ürün satıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba76-127">Satış siparişi girişi (şirketlerarası/şirketiçi) ve faturalandırma</span><span class="sxs-lookup"><span data-stu-id="1ba76-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="1ba76-128">Kuruluşunuzdaki tüzel kişilikler arasında ürünler satıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba76-129">Satın alma siparişleri (merkezi işlem)</span><span class="sxs-lookup"><span data-stu-id="1ba76-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="1ba76-130">Bir satıcıdan kuruluşunuzdaki başka bir tüzel kişilik adına stok, malzemeler, hizmetler, sabit kıymetler ve başka ürünler alıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba76-131">Stok yönetimi (şirketlerarası/şirketiçi)</span><span class="sxs-lookup"><span data-stu-id="1ba76-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="1ba76-132">Bir tüzel kişiliğin stoğunu, kuruluşunuzdaki başka bir tüzel kişiliğin sabit kıymetlerine aktarıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="1ba76-133">Bir tüzel kişiliğin stoğunu, kuruluşunuzdaki başka bir tüzel kişiliğin stoğuna aktarıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba76-134">Transit stok izleme</span><span class="sxs-lookup"><span data-stu-id="1ba76-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="1ba76-135">Aynı tüzel kişilikte farklı coğrafi tesislerdeki ambarlar arasında madde aktarıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba76-136">Borç hesapları merkezi fatura işleme</span><span class="sxs-lookup"><span data-stu-id="1ba76-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="1ba76-137">Kuruluşunuzdaki başka bir tüzel kişilik adına fatura kaydediyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba76-138">Borç hesapları merkezi ödeme işleme</span><span class="sxs-lookup"><span data-stu-id="1ba76-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="1ba76-139">Kuruluşunuzdaki başka bir tüzel kişilik adına fatura ödüyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba76-140">Nakit yönetimi ve hazine (merkezi işlem)</span><span class="sxs-lookup"><span data-stu-id="1ba76-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="1ba76-141">Vergi ödemelerini, vergi iadelerini, faiz giderlerini, ödünç verilenleri, avansları, temettü ödemelerini, önceden ödenmiş hak bedellerini veya komisyonları işliyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="1ba76-142">Kuruluşunuzdaki başka bir tüzel kişilik adına gider ödüyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="1ba76-143">Fatura, hedef tüzel kişiliğin defterlerine girilir ve tüzel kişilikler arasında çapraz kapatma yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="1ba76-144">Örneğin, bir tüzel kişilik başka bir tüzel kişilikteki bir çalışanın gider raporunu öder.</span><span class="sxs-lookup"><span data-stu-id="1ba76-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="1ba76-145">Bu durumda, çalışanın gider raporunda başka bir tüzel kişilikle ilgili giderler olur.</span><span class="sxs-lookup"><span data-stu-id="1ba76-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="1ba76-146">Nakdi kuruluşunuzdaki bir tüzel kişilikten bir diğerine aktarırsınız.</span><span class="sxs-lookup"><span data-stu-id="1ba76-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba76-147">Alacak hesapları (merkezi işlem)</span><span class="sxs-lookup"><span data-stu-id="1ba76-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="1ba76-148">Başka bir tüzel kişiliğin müşteri faturası için nakit alırsınız ve çeki o tüzel kişiliğin banka hesabına havale edersiniz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba76-149">Bordro (merkezi işlem, şirketlerarası/şirketiçi)</span><span class="sxs-lookup"><span data-stu-id="1ba76-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="1ba76-150">Başka bir tüzel kişiliğin bordrosunu ödüyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="1ba76-151">Örneğin, bir tüzel kişilik kendi çalışanları için olan kendi bordrosunu ödüyor, ancak bir çalışanın bu bordro işlemi sırasında başka bir tüzel kişilik için yaptığı işi geri masraflandırıyor.</span><span class="sxs-lookup"><span data-stu-id="1ba76-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="1ba76-152">Veya bir çalışan A tüzel kişiliği için yarı zamanlı ve B tüzel kişiliği için yarı zamanlı çalışmıştır ve kazançlar tüm ödemelere yayılmıştır.</span><span class="sxs-lookup"><span data-stu-id="1ba76-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="1ba76-153">Bu gibi durumlarda çalışana ödeme, her iki tüzel kişilikten yapılan ödemeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="1ba76-154">Yalnızca maaşlar nakledilmez, maaşlar için vergiler, kazançlar, kesintiler ve tahakkuklar da nakledilir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="1ba76-155">Bir departman veya bölümden bir diğerine işgücü aktarıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ba76-156">Sabit kıymetler (şirketlerarası/şirketiçi)</span><span class="sxs-lookup"><span data-stu-id="1ba76-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="1ba76-157">Bir tüzel kişiliğin sabit kıymetlerine veya stoğuna sabit kıymetler aktarıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ba76-158">Tahsisatlar (şirketlerarası/şirketiçi)</span><span class="sxs-lookup"><span data-stu-id="1ba76-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="1ba76-159">Şirket tahsisatlarını işliyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-159">You process corporate allocations.</span></span> <span data-ttu-id="1ba76-160">Tahsisatlar, kaynak modülden bağımsız olarak tahsis edilmiş herhangi bir hesaba yönelik faaliyetlerdir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="1ba76-161">Örnek</span><span class="sxs-lookup"><span data-stu-id="1ba76-161">Example</span></span>
<span data-ttu-id="1ba76-162">Tüzel kişiliğiniz (A tüzel kişiliği) kuruluşunuzdaki başka bir tüzel kişiliğe (B tüzel kişiliği) bir şeyler satıyor. Aşağıdaki örnekte, iki tüzel kişilik arasında gerçekleşen hareketlerin nasıl elenmesi gerekebileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="1ba76-163">A tüzel kişiliği, 10,00 lira maliyetli bir malı B tüzel kişiliğine 10,00 liraya satıyor.</span><span class="sxs-lookup"><span data-stu-id="1ba76-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="1ba76-164">A tüzel kişiliği 10,00 lira maliyetli bir malı B tüzel kişiliğine 10,00 lira artı 2,00 lira fiili sevkiyat maliyetiyle satıyor.</span><span class="sxs-lookup"><span data-stu-id="1ba76-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="1ba76-165">A tüzel kişiliği, 10,00 lira maliyetli bir malı B tüzel kişiliğine 15,00 liraya satıyor ve satıştan bir marj elde ediyor.</span><span class="sxs-lookup"><span data-stu-id="1ba76-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="1ba76-166">A tüzel kişiliği, 10,00 lira maliyetli bir malı B tüzel kişiliğine 15,00 liraya satıyor ve satıştan marjın yarısını elde ediyor.</span><span class="sxs-lookup"><span data-stu-id="1ba76-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="1ba76-167">B tüzel kişiliği, satıştan elde edilen marjın diğer yarısını alıyor.</span><span class="sxs-lookup"><span data-stu-id="1ba76-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="1ba76-168">Böylece, gelir bölünüyor.</span><span class="sxs-lookup"><span data-stu-id="1ba76-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="1ba76-169">Bölünmüş gelir, dışarıdan bir kuruluştan değil de kuruluştaki başka bir tüzel kişilikten siparişe bir teşvik oluşturuyor.</span><span class="sxs-lookup"><span data-stu-id="1ba76-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="1ba76-170">Tüm bu hareketler, borç ve alacak hesaplarına nakledilen şirketlerarası hareketleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ba76-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="1ba76-171">Ayrıca bu hareketler, şirketlerarası satış ve satılan malların maliyeti eşit olmadığı zaman artırma ve azaltma tutarlarını da içerebilir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="1ba76-172">Eliminasyon kurallarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="1ba76-172">Set up elimination rules</span></span>
<span data-ttu-id="1ba76-173">Microsoft Dynamics 365 for Finance and Operations içinde eleme kuralları ayarlanırken eleme amaçlı ayrı bir mali boyut oluşturmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="1ba76-174">Müşterilerin çoğu buna Ticaret Ortağı veya benzer bir ad verirler.</span><span class="sxs-lookup"><span data-stu-id="1ba76-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="1ba76-175">Bir mali boyut kullanmamaya karar verirseniz, yalnızca şirketlerarası harektelere özel bir ana hesaba sahip olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="1ba76-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="1ba76-176">Elemeler için kurulum, Konsolidasyonlar modülünün kurulum alanında bulunur.</span><span class="sxs-lookup"><span data-stu-id="1ba76-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="1ba76-177">Bir kural için bir açıklama girdikten sonra, eleme günlüğünün nakledeceği şirketi seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="1ba76-178">Bu, Tüzel varlık kurulumunda **Mali eleme sürecini kullan**'ın seçilmiş olduğu bir şirket olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1ba76-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="1ba76-179">Gerekirse, eleme kuralının ne zaman geçerli olacağını ve ne süresinin ne zaman dolacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="1ba76-180">Eleme öneri işleminde kullanılabilir olmasını istiyorsanız **Etkin**'i **Evet** olarak ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="1ba76-181">Bir tür **Eleme**'ye sahip bir günlük adı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ba76-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="1ba76-182">Temelleri tanımladıktan sonra, **Satırlar** üzerine tıklatarak gerçek işleme kurallarını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="1ba76-183">Elemeler için iki seçenek mevcuttur; net değişim tutarını eleme veya sabit bir tutar tanımlama.</span><span class="sxs-lookup"><span data-stu-id="1ba76-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="1ba76-184">Kaynak hesabınızı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ba76-184">Select your source account.</span></span> <span data-ttu-id="1ba76-185">Joker karakter olarak bir yıldız (\*) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="1ba76-186">Örneğin, 1\* tahsisat için veri kaynağı olarak 1 ile başlayan tüm hesapları seçer.</span><span class="sxs-lookup"><span data-stu-id="1ba76-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="1ba76-187">Kaynak hesaplarınızı seçtikten sonra **Hesap belirtimi**, hedef şirketinden kullanılan hesabı belirler.</span><span class="sxs-lookup"><span data-stu-id="1ba76-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="1ba76-188">**Kaynak** hesabında tanımlanan aynı ana hesabı kullanmak istiyorsanız **Kaynak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ba76-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="1ba76-189">**Kullanıcı tanımlı**'yı seçerseniz, bir hedef hesabı belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="1ba76-190">Boyut belirtimi de aynı şekilde davranır.</span><span class="sxs-lookup"><span data-stu-id="1ba76-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="1ba76-191">**Kaynak**'ı seçerseniz, hedef şirkette de kaynak şirkette kullandığı aynı boyutları kullanır.</span><span class="sxs-lookup"><span data-stu-id="1ba76-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="1ba76-192">**Kullanıcı tanımlı**'yı seçerseniz, hedef şirketteki boyutları **Hedef boyutları** menü öğesini seçerek belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="1ba76-193">Kaynak boyutları ve eleme için kaynakta kullanılacak finansal boyutları ve değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="1ba76-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="1ba76-194">Eliminasyon hareketlerini işleme koy</span><span class="sxs-lookup"><span data-stu-id="1ba76-194">Process elimination transactions</span></span>
<span data-ttu-id="1ba76-195">Eleme hareketlerini işlemenin iki yolu vardır; birleştirme işlemi sırasında veya bir eleme günlüğü oluşturarak ve eleme teklif işlemini yürüterek.</span><span class="sxs-lookup"><span data-stu-id="1ba76-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="1ba76-196">Bu bölüm, günlüğü oluşturmaya ve eleme işlemini çalıştırmaya odaklanır.</span><span class="sxs-lookup"><span data-stu-id="1ba76-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="1ba76-197">Bir eleme şirketi olarak tanımlanan bir şirkette, Birleştirme modülü içerisinde **Eleme günlüğü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="1ba76-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="1ba76-198">Günlük adını seçtikten sonra, **Satırlar**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1ba76-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="1ba76-199">**Teklifler** menüsünü seçtikten sonra **Eleme teklifi**'ni seçerek teklifi çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="1ba76-200">Birleştirilmiş verinin kaynağı olan şirketi seçin ve sonra işlemek istediğiniz kuralı seçin.</span><span class="sxs-lookup"><span data-stu-id="1ba76-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="1ba76-201">Eleme tutarlarını aramaya başlamak için bir başlangıç tarihi ve eleme tutarları bitişi için bir bitiş tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="1ba76-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="1ba76-202">**GL deftere nakil tarihi** alanı, günlüğü genel muhasebe defterine nakletmek için kullanılan tarihtir.</span><span class="sxs-lookup"><span data-stu-id="1ba76-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="1ba76-203">**Tamam**'ı tıklattıktan sonra, tutarları görebilir ve günlüğü deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ba76-203">After you click **OK**, you can review the amounts and post the journal.</span></span>




