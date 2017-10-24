---
title: "Satıcı deftere nakil profilleri"
description: "Satıcı deftere nakil profilleri, satıcı hareketlerinin genel muhasebeye naklini kontrol eder."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 540ad7be384e34054454cdc34c4945ed505b7963
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-posting-profiles"></a><span data-ttu-id="29ade-103">Satıcı deftere nakil profilleri</span><span class="sxs-lookup"><span data-stu-id="29ade-103">Vendor posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="29ade-104">Satıcı deftere nakil profilleri, satıcı hareketlerinin genel muhasebeye naklini kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="29ade-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="29ade-105">Satıcı deftere nakil profilleri</span><span class="sxs-lookup"><span data-stu-id="29ade-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="29ade-106">Satıcı deftere nakil profilleri tüm satıcılara, bir satıcı grubuna veya tek bir satıcıya genel muhasebe hesapları ve belge ayarları atamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="29ade-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="29ade-107">Bu ayarlar satınalma siparişleri, satıcı faturaları ve nakit ödemeler oluşturduğunuzda kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="29ade-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="29ade-108">Bazı hareketler için, bu sayfadaki hareket için ayarlanan nakil profillerinden farklılık gösteren ve bunların yerini alan bir nakil profili seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29ade-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="29ade-109">Varsayılan deftere nakletme profili, Borç Hesapları parametreleri sayfasındaki Genel Muhasebe ve Satış Vergisi hızlı sekmesinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="29ade-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="29ade-110">Varsayılan nakil profili, onu farklı nakil profiline gerekiyorsa değiştirebileceğiniz, yeni belge başlığındaki otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="29ade-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="29ade-111">Ayrıca, nakil tanımlarını hareket nakil türleriyle, Hareket nakil tanımları sayfasında ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29ade-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="29ade-112">Nakil tanımları satıcı hareketlerinin, nakil profilleri yerine genel muhasebe defterine nakledilmesini denetler.</span><span class="sxs-lookup"><span data-stu-id="29ade-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="29ade-113">Bir nakil profili oluşturmak</span><span class="sxs-lookup"><span data-stu-id="29ade-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="29ade-114">**Kurulum**</span><span class="sxs-lookup"><span data-stu-id="29ade-114">**Setup**</span></span>

<span data-ttu-id="29ade-115">Seçili nakil profilini kullanan hareketlerin nakledilmesinde kullanılan genel muhasebe hesaplarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="29ade-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="29ade-116">Bir hesap kodu ve mümkün olduğu durumlarda seçili nakil profili için bir hesap veya grup numarası seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="29ade-117">Deftere nakil işleminde, en uygun hesap kodu, hesap numarası veya grup veya numara birleşimini aşağıdaki öncelik sırasına göre aranarak her hareket için en uygun nakil profili bulunur.</span><span class="sxs-lookup"><span data-stu-id="29ade-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="29ade-118">**Hesap kodu** alan değeri</span><span class="sxs-lookup"><span data-stu-id="29ade-118">**Account code** field value</span></span> | <span data-ttu-id="29ade-119">**Hesap/Grup numarası** alan değeri</span><span class="sxs-lookup"><span data-stu-id="29ade-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="29ade-120">Arama önceliği</span><span class="sxs-lookup"><span data-stu-id="29ade-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="29ade-121">**Tablo**</span><span class="sxs-lookup"><span data-stu-id="29ade-121">**Table**</span></span>                    | <span data-ttu-id="29ade-122">Belirtilmiş satıcı hesabı.</span><span class="sxs-lookup"><span data-stu-id="29ade-122">Specific vendor account</span></span>                     | <span data-ttu-id="29ade-123">1</span><span class="sxs-lookup"><span data-stu-id="29ade-123">1</span></span>               |
| <span data-ttu-id="29ade-124">**Grup**</span><span class="sxs-lookup"><span data-stu-id="29ade-124">**Group**</span></span>                    | <span data-ttu-id="29ade-125">satıcıya atanmış satıcı grubu.</span><span class="sxs-lookup"><span data-stu-id="29ade-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="29ade-126">2</span><span class="sxs-lookup"><span data-stu-id="29ade-126">2</span></span>               |
| <span data-ttu-id="29ade-127">**Tümü**</span><span class="sxs-lookup"><span data-stu-id="29ade-127">**All**</span></span>                      | <span data-ttu-id="29ade-128">Boşluk</span><span class="sxs-lookup"><span data-stu-id="29ade-128">Blank</span></span>                                       | <span data-ttu-id="29ade-129">3</span><span class="sxs-lookup"><span data-stu-id="29ade-129">3</span></span>               |

<span data-ttu-id="29ade-130">Tüm satıcı hareketlerinin aynı deftere nakil profili içermesini istiyorsanız, Hesap kodu alanında Tümü değerini içeren yalnızca bir nakil profili ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="29ade-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="29ade-131">Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="29ade-131">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="29ade-132">Alan</span><span class="sxs-lookup"><span data-stu-id="29ade-132">Field</span></span></th>
<th><span data-ttu-id="29ade-133">Açıklama</span><span class="sxs-lookup"><span data-stu-id="29ade-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29ade-134"><strong>Nakil profili</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="29ade-135">Nakil profili için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="29ade-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="29ade-136">Örneğin ulusal para birimini içeren satıcı bakiyeleri için bir hesap elde etmek üzere iki nakil profili, yabancı bir para birimini içeren satıcı bakiyeleri için başka bir nakil profili oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29ade-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="29ade-137">Birini Ulusal, diğerini Yabancı olarak adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29ade-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29ade-138"><strong>Açıklama</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="29ade-139">Nakil profilinin açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="29ade-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29ade-140"><strong>Hesap kodu</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="29ade-141">Nakil profilinin belirli bir satıcı, bir satıcı grubu veya tüm satıcılar için mi geçerli olduğunu belirtin:</span><span class="sxs-lookup"><span data-stu-id="29ade-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="29ade-142"><strong>Tablo</strong> – Nakil profili bir satıcı için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="29ade-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="29ade-143">Hesap/Grup numarası alanında satıcı hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="29ade-144"><strong>Grup</strong> – Nakil profili bir satıcı grubu geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="29ade-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="29ade-145">Hesap/Grup numarası alanında satıcı grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="29ade-146"><strong>Tümü</strong> – Nakil profili tüm satıcılar için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="29ade-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="29ade-147">Hesap/Grup numarası alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="29ade-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29ade-148"><strong>Hesap/Grup numarası</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="29ade-149">Hesap kodu alanında Tablo seçiliyse, nakil profiliyle ilişkilendirilmiş satıcının hesap numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="29ade-150">Eğer Grup seçiliyse, bir satıcı grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="29ade-151">Tümü seçiliyse, bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="29ade-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29ade-152"><strong>Özet hesap</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="29ade-153">Nakil profilinin ilişkili olduğu satıcılar için özet hesabı olarak kullanılacak genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="29ade-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Not:</span><span class="sxs-lookup"><span data-stu-id="29ade-154"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="29ade-155"><strong>Not</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29ade-156">Eğer Nakil tanımlarını kullan hızlı geçişi Genel muhasebe parametreleri sayfasında seçiliyse, özet hesabı yerine satıcı faturaları için hareket nakil tanımı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="29ade-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29ade-157"><strong>Kapatma hesabı</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="29ade-158">Nakit akışı tahminleri için kullanılacak likidite genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="29ade-159">Bu alan yalnızca nakit akışı tahmini etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="29ade-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29ade-160"><strong>Satış vergisi ön ödemeleri</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="29ade-161">Avans olarak alınmış ödemeler için satış vergisinin hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="29ade-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Not:</span><span class="sxs-lookup"><span data-stu-id="29ade-162"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="29ade-163"><strong>Not</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29ade-164">Bir ödeme, ön ödeme olarak işaretlendiğinde kullanılan nakil profili, Borç hesapları parametreleri sayfasının Genel muhasebe ve satış vergisi bölümündeki Ön ödeme günlüğü fiş alanında seçilir.</span><span class="sxs-lookup"><span data-stu-id="29ade-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29ade-165"><strong>Varış</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="29ade-166">Onaylanmayan satıcı faturaları hakkındaki bilgilerin nakledildiği genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="29ade-167">Bilgiler Fatura kayıt günlüğüne girilir.</span><span class="sxs-lookup"><span data-stu-id="29ade-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="29ade-168">Örneğin, bir kullanıcı, fatura kaydına girdiklerinde satıcı faturaları hakkındaki temel bilgileri girer.</span><span class="sxs-lookup"><span data-stu-id="29ade-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="29ade-169">Fatura kaydı nakledildiğinde, hareketler buraya ve Mahsup hesap alanına girilen hesaba nakledilir.</span><span class="sxs-lookup"><span data-stu-id="29ade-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="29ade-170">Faturalar onaylandığında, borç varış hesabından satıcı özet hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="29ade-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29ade-171"><strong>Mahsup hesap</strong></span><span class="sxs-lookup"><span data-stu-id="29ade-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="29ade-172">Fatura kaydını kullanarak güncelleştirilen onaylanmamış satıcı faturalarının mahsuben kullanılan genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="29ade-173">Mahsup hesabı Varış hesaplarına nakledilen hareketler için mahsup hesabı olarak işlev görür.</span><span class="sxs-lookup"><span data-stu-id="29ade-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="29ade-174">Bu nedenle, hesap henüz onaylanmamış satıcı satınalma işlemleri içerir.</span><span class="sxs-lookup"><span data-stu-id="29ade-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a><span data-ttu-id="29ade-175">**Tablo kısıtlamaları**</span><span class="sxs-lookup"><span data-stu-id="29ade-175">**Table restrictions**</span></span>

<span data-ttu-id="29ade-176">Seçili nakil profilini içeren hareketler için hareketlerin otomatik olarak kapatılması, faiz hesaplanması ve tahsilat mektuplarının verilip verilmeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="29ade-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="29ade-177">Ayrıca, seçili nakil profilini içeren hareketler kapatıldığında kullanılan hesabı seçin seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29ade-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="29ade-178">Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="29ade-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="29ade-179">Alan</span><span class="sxs-lookup"><span data-stu-id="29ade-179">Field</span></span>          | <span data-ttu-id="29ade-180">Açıklama</span><span class="sxs-lookup"><span data-stu-id="29ade-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29ade-181">**Kapatma**</span><span class="sxs-lookup"><span data-stu-id="29ade-181">**Settlement**</span></span> | <span data-ttu-id="29ade-182">Bu nakil profilini içeren hareketlerin otomatik kapatılmasını etkinleştirmek için bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="29ade-183">Bu seçenek temizlenirse, hareketleri, Açık hareketleri kapat sayfasını kullanarak elden kapatmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="29ade-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="29ade-184">**İptal**</span><span class="sxs-lookup"><span data-stu-id="29ade-184">**Cancel**</span></span>     | <span data-ttu-id="29ade-185">Bu nakil profilini içeren hareketlerin iptal edilmesi seçeneğine sahip olmak istiyorsanız bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="29ade-186">**Kapat**</span><span class="sxs-lookup"><span data-stu-id="29ade-186">**Close**</span></span>      | <span data-ttu-id="29ade-187">Bu nakil profilini içeren hareketler kapatılırken değiştirmek istediğiniz nakil profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="29ade-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="29ade-188">Bir hareket tamamen kapatıldığında kapanmış kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="29ade-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |






