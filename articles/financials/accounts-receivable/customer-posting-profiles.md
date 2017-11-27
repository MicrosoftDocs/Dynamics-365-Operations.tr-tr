---
title: "Müşteri deftere nakil profilleri"
description: "Müşteri deftere nakil profilleri, müşteri hareketlerinin genel muhasebeye naklini kontrol eder."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ccd663a769aa98afb800f6fcd6217f39bb513597
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="customer-posting-profiles"></a><span data-ttu-id="7e008-103">Müşteri deftere nakil profilleri</span><span class="sxs-lookup"><span data-stu-id="7e008-103">Customer posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7e008-104">Müşteri deftere nakil profilleri, müşteri hareketlerinin genel muhasebeye naklini kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="7e008-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="7e008-105">Müşteri deftere nakil profilleri</span><span class="sxs-lookup"><span data-stu-id="7e008-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="7e008-106">Müşteri deftere nakil profilleri tüm müşterilere, bir müşteri grubuna veya tek bir müşteriye genel muhasebe hesapları ve belge ayarları atamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="7e008-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="7e008-107">Satış siparişleri, serbest metin faturaları, nakit ödemeler, tahsilat mektupları ve vade farkı dekontları işlemleri oluşturduğunuzda, bu ayarlar kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7e008-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="7e008-108">Bazı hareketler için, bu sayfadaki hareket için ayarlanan nakil profillerinden farklılık gösteren ve bunların yerini alan bir nakil profili seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e008-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="7e008-109">Varsayılan deftere nakletme profili, Alacak Hesapları sayfasındaki Genel Muhasebe ve Satış Vergisi hızlı sekmesinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="7e008-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="7e008-110">Varsayılan nakil profili, onu farklı nakil profiline gerekiyorsa değiştirebileceğiniz, yeni belge başlığındaki otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="7e008-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="7e008-111">Ayrıca, nakil tanımlarını hareket nakil türleriyle, Hareket nakil tanımları sayfasında ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e008-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="7e008-112">Nakil tanımları müşteri hareketlerinin, nakil profilleri yerine genel muhasebe defterine nakledilmesini denetler.</span><span class="sxs-lookup"><span data-stu-id="7e008-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="7e008-113">Bir nakil profili oluşturmak</span><span class="sxs-lookup"><span data-stu-id="7e008-113">Creating a posting profile</span></span>
<span data-ttu-id="7e008-114">Seçili nakil profilini kullanan hareketlerin nakledilmesinde kullanılan genel muhasebe hesaplarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="7e008-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="7e008-115">Bir hesap kodu ve mümkün olduğu durumlarda seçili nakil profili için bir hesap veya grup numarası seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="7e008-116">Deftere nakil işleminde, en uygun hesap kodu, hesap numarası veya grup veya numara birleşimini aşağıdaki öncelik sırasına göre aranarak her hareket için en uygun nakil profili bulunur.</span><span class="sxs-lookup"><span data-stu-id="7e008-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="7e008-117">**Hesap kodu** alan değeri</span><span class="sxs-lookup"><span data-stu-id="7e008-117">**Account code** field value</span></span> | <span data-ttu-id="7e008-118">**Hesap/Grup numarası** alan değeri</span><span class="sxs-lookup"><span data-stu-id="7e008-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="7e008-119">Arama önceliği</span><span class="sxs-lookup"><span data-stu-id="7e008-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="7e008-120">**Tablo**</span><span class="sxs-lookup"><span data-stu-id="7e008-120">**Table**</span></span>                    | <span data-ttu-id="7e008-121">Özel müşteri hesabı</span><span class="sxs-lookup"><span data-stu-id="7e008-121">Specific customer account</span></span>                       | <span data-ttu-id="7e008-122">1</span><span class="sxs-lookup"><span data-stu-id="7e008-122">1</span></span>               |
| <span data-ttu-id="7e008-123">**Grup**</span><span class="sxs-lookup"><span data-stu-id="7e008-123">**Group**</span></span>                    | <span data-ttu-id="7e008-124">Müşteriye atanmış olan müşteri grubu</span><span class="sxs-lookup"><span data-stu-id="7e008-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="7e008-125">2</span><span class="sxs-lookup"><span data-stu-id="7e008-125">2</span></span>               |
| <span data-ttu-id="7e008-126">**Tümü**</span><span class="sxs-lookup"><span data-stu-id="7e008-126">**All**</span></span>                      | <span data-ttu-id="7e008-127">Boşluk</span><span class="sxs-lookup"><span data-stu-id="7e008-127">Blank</span></span>                                           | <span data-ttu-id="7e008-128">3</span><span class="sxs-lookup"><span data-stu-id="7e008-128">3</span></span>               |

<span data-ttu-id="7e008-129">Tüm müşteri hareketlerinin aynı deftere nakil profili içermesini istiyorsanız, Hesap kodu alanında Tümü değerini içeren yalnızca bir nakil profili ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e008-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="7e008-130">Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="7e008-130">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e008-131">Alan</span><span class="sxs-lookup"><span data-stu-id="7e008-131">Field</span></span></th>
<th><span data-ttu-id="7e008-132">Açıklama</span><span class="sxs-lookup"><span data-stu-id="7e008-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e008-133"><strong>Nakil profili</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="7e008-134">Nakil profili için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="7e008-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="7e008-135">Örneğin ulusal para birimini içeren müşteri bakiyeleri için bir hesap elde etmek üzere iki nakil profili, yabancı para birimini içeren müşteri bakiyeleri için başka bir nakil profili oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e008-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="7e008-136">Birini Ulusal, diğerini Yabancı olarak adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e008-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e008-137"><strong>Açıklama</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="7e008-138">Nakil profilinin açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="7e008-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="7e008-139">Bu yalnızca bu sayfada görüntülediğinizde, deftere nakil profilini daha iyi tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7e008-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e008-140"><strong>Hesap kodu</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="7e008-141">Nakil profilinin tek bir müşteri, bir müşteri grubu veya tüm müşteriler için mi geçerli olduğunu belirtin:</span><span class="sxs-lookup"><span data-stu-id="7e008-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="7e008-142"><strong>Tablo</strong> – Nakil profili bir müşteri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="7e008-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="7e008-143">Hesap/Grup numarası alanında müşteri hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="7e008-144"><strong>Grup</strong> – Nakil profili bir müşteri grubu geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="7e008-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="7e008-145">Hesap/Grup numarası alanında müşteri grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="7e008-146"><strong>Tümü</strong> – Nakil profili tüm müşteriler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="7e008-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="7e008-147">Hesap/Grup numarası alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="7e008-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e008-148"><strong>Hesap/Grup numarası</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="7e008-149">Hesap kodu alanında Tablo seçiliyse, nakil profiliyle ilişkilendirilmiş müşterinin hesap numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="7e008-150">Eğer Grup seçiliyse, müşteri grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="7e008-151">Tümü seçiliyse, bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="7e008-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e008-152"><strong>Özet hesap</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="7e008-153">Nakil profiliyle ilişkilendirilmiş müşteriler için müşteri özet hesabı olarak kullanılacak genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e008-154"><strong>Kapatma hesabı</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="7e008-155">Nakit akışı tahminleri için kullanılacak likidite genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="7e008-156">Bu alan yalnızca nakit akışı tahminleri etkinleştirilmişse görünür.</span><span class="sxs-lookup"><span data-stu-id="7e008-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e008-157"><strong>Satış vergisi ön ödemeleri</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="7e008-158">Avans olarak alınmış ödemeler için satış vergisinin hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7e008-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Not:</span><span class="sxs-lookup"><span data-stu-id="7e008-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="7e008-160"><strong>Not</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e008-161">Bir ödeme bir ön ödeme olarak işaretlendiğinde kullanılacak nakil profilini belirtmek için Alacak hesapları parametreleri sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="7e008-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e008-162"><strong>İskonto hesabı borçları</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="7e008-163">İskonto borçları genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e008-164"><strong>Tahsilat mektubu sırası</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="7e008-165">Tahsilat mektubu sırasının, nakil profilinin atandığı müşteriler için kullanılacak tanımlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e008-166"><strong>Vade farkı kodu</strong></span><span class="sxs-lookup"><span data-stu-id="7e008-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="7e008-167">Nakil profilinin atandığı müşteriler için faizin hesaplanmasında kullanılacak faiz kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="7e008-168">**Tablo kısıtlamaları**</span><span class="sxs-lookup"><span data-stu-id="7e008-168">**Table restrictions**</span></span>

<span data-ttu-id="7e008-169">Seçili nakil profilini içeren hareketler için hareketlerin otomatik olarak kapatılması, faiz hesaplanması ve tahsilat mektuplarının verilip verilmeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7e008-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="7e008-170">Ayrıca, seçili nakil profilini içeren hareketler kapatıldığında kullanılan hesabı seçin seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e008-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="7e008-171">Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="7e008-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="7e008-172">Alan</span><span class="sxs-lookup"><span data-stu-id="7e008-172">Field</span></span>                 | <span data-ttu-id="7e008-173">Açıklama</span><span class="sxs-lookup"><span data-stu-id="7e008-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e008-174">**Kapatma**</span><span class="sxs-lookup"><span data-stu-id="7e008-174">**Settlement**</span></span>        | <span data-ttu-id="7e008-175">Bu nakil profilini içeren hareketlerin otomatik kapatılmasını etkinleştirmek için bu geçiş tuşunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="7e008-176">Bu geçiş tuşu temizlenirse, hareketleri, Açık hareketleri kapat sayfasını ya da Müşteri ödemelerini girme sayfasını kullanarak elden kapatmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7e008-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="7e008-177">**İlgi alanı**</span><span class="sxs-lookup"><span data-stu-id="7e008-177">**Interest**</span></span>          | <span data-ttu-id="7e008-178">Bu profili kullanan müşteri hesapları için bekleyen bakiyelerdeki vade farkı hesaplanacaksa bu geçiş tuşunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="7e008-179">Bu geçiş tuşu temizlenirse, bu müşteriler için vade farkı hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="7e008-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="7e008-180">**Tahsilat mektubu**</span><span class="sxs-lookup"><span data-stu-id="7e008-180">**Collection letter**</span></span> | <span data-ttu-id="7e008-181">Bu profili kullanan müşteri hesapları için tahsilat mektupları oluşturulacaksa, bu geçiş tuşunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="7e008-182">Bu geçiş tuşu temizlenirse, bu müşteriler için tahsilat mektupları oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="7e008-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="7e008-183">**Kapat**</span><span class="sxs-lookup"><span data-stu-id="7e008-183">**Close**</span></span>             | <span data-ttu-id="7e008-184">Bu nakil profilini içeren hareketler kapatılırken değiştirmek istediğiniz nakil profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="7e008-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="7e008-185">Bir hareket tamamen kapatıldığında kapanmış kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="7e008-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="7e008-186">Daha fazla bilgi için bkz. [Müşteri ödeme genel bakışı](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7e008-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>


