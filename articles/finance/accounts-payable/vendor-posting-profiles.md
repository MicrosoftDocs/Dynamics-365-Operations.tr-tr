---
title: Satıcı deftere nakil profilleri
description: Satıcı deftere nakil profilleri, satıcı hareketlerinin genel muhasebeye naklini kontrol eder.
author: abruer
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4b38fd137e6479493da79d4b62d0111b502a632
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189505"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="057b9-103">Satıcı deftere nakil profilleri</span><span class="sxs-lookup"><span data-stu-id="057b9-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="057b9-104">Satıcı deftere nakil profilleri, satıcı hareketlerinin genel muhasebeye naklini kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="057b9-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

## <a name="vendor-posting-profiles"></a><span data-ttu-id="057b9-105">Satıcı deftere nakil profilleri</span><span class="sxs-lookup"><span data-stu-id="057b9-105">Vendor posting profiles</span></span>

<span data-ttu-id="057b9-106">Satıcı deftere nakil profilleri tüm satıcılara, bir satıcı grubuna veya tek bir satıcıya genel muhasebe hesapları ve belge ayarları atamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="057b9-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="057b9-107">Bu ayarlar satınalma siparişleri, satıcı faturaları ve nakit ödemeler oluşturduğunuzda kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="057b9-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="057b9-108">Bazı hareketler için, bu sayfadaki hareket için ayarlanan nakil profillerinden farklılık gösteren ve bunların yerini alan bir nakil profili seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="057b9-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="057b9-109">Varsayılan deftere nakletme profili, **Borç Hesapları parametreleri** sayfasındaki **Genel Muhasebe ve Satış Vergisi** hızlı sekmesinde tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="057b9-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="057b9-110">Varsayılan nakil profili, onu farklı nakil profiline gerekiyorsa değiştirebileceğiniz, yeni belge başlığındaki otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="057b9-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="057b9-111">Ayrıca, nakil tanımlarını hareket nakil türleriyle, **Hareket nakil tanımları** sayfasında ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="057b9-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="057b9-112">Nakil tanımları satıcı hareketlerinin, nakil profilleri yerine genel muhasebe defterine nakledilmesini denetler.</span><span class="sxs-lookup"><span data-stu-id="057b9-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="057b9-113">Bir nakil profili oluşturmak</span><span class="sxs-lookup"><span data-stu-id="057b9-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="057b9-114">**Kurulum**</span><span class="sxs-lookup"><span data-stu-id="057b9-114">**Setup**</span></span>

<span data-ttu-id="057b9-115">Seçili nakil profilini kullanan hareketlerin nakledilmesinde kullanılan genel muhasebe hesaplarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="057b9-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="057b9-116">Bir hesap kodu ve mümkün olduğu durumlarda seçili nakil profili için bir hesap veya grup numarası seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="057b9-117">Deftere nakil işleminde, en uygun hesap kodu, hesap numarası veya grup veya numara birleşimini aşağıdaki öncelik sırasına göre aranarak her hareket için en uygun nakil profili bulunur:</span><span class="sxs-lookup"><span data-stu-id="057b9-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="057b9-118">**Hesap kodu** alan değeri</span><span class="sxs-lookup"><span data-stu-id="057b9-118">**Account code** field value</span></span> | <span data-ttu-id="057b9-119">**Hesap/Grup numarası** alan değeri</span><span class="sxs-lookup"><span data-stu-id="057b9-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="057b9-120">Arama önceliği</span><span class="sxs-lookup"><span data-stu-id="057b9-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="057b9-121">**Tablo**</span><span class="sxs-lookup"><span data-stu-id="057b9-121">**Table**</span></span>                    | <span data-ttu-id="057b9-122">Belirtilmiş satıcı hesabı.</span><span class="sxs-lookup"><span data-stu-id="057b9-122">Specific vendor account</span></span>                     | <span data-ttu-id="057b9-123">1</span><span class="sxs-lookup"><span data-stu-id="057b9-123">1</span></span>               |
| <span data-ttu-id="057b9-124">**Grup**</span><span class="sxs-lookup"><span data-stu-id="057b9-124">**Group**</span></span>                    | <span data-ttu-id="057b9-125">Satıcıya atanmış satıcı grubu.</span><span class="sxs-lookup"><span data-stu-id="057b9-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="057b9-126">2</span><span class="sxs-lookup"><span data-stu-id="057b9-126">2</span></span>               |
| <span data-ttu-id="057b9-127">**Tümü**</span><span class="sxs-lookup"><span data-stu-id="057b9-127">**All**</span></span>                      | <span data-ttu-id="057b9-128">Boş</span><span class="sxs-lookup"><span data-stu-id="057b9-128">Blank</span></span>                                       | <span data-ttu-id="057b9-129">3</span><span class="sxs-lookup"><span data-stu-id="057b9-129">3</span></span>               |

<span data-ttu-id="057b9-130">Tüm satıcı hareketlerinin aynı deftere nakil profili içermesini istiyorsanız, **Hesap kodu** alanında **Tümü** değerini içeren yalnızca bir nakil profili ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="057b9-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="057b9-131">Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="057b9-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="057b9-132">Alan</span><span class="sxs-lookup"><span data-stu-id="057b9-132">Field</span></span></th>
<th><span data-ttu-id="057b9-133">Tanım</span><span class="sxs-lookup"><span data-stu-id="057b9-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="057b9-134"><strong>Deftere nakil profili</strong></span><span class="sxs-lookup"><span data-stu-id="057b9-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="057b9-135">Nakil profili için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="057b9-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="057b9-136">Örneğin ulusal para birimini içeren satıcı bakiyeleri için bir hesap elde etmek üzere iki nakil profili, yabancı bir para birimini içeren satıcı bakiyeleri için başka bir nakil profili oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="057b9-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="057b9-137">Birini Ulusal, diğerini Yabancı olarak adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="057b9-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="057b9-138"><strong>Açıklama</strong></span><span class="sxs-lookup"><span data-stu-id="057b9-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="057b9-139">Nakil profilinin açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="057b9-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="057b9-140"><strong>Hesap kodu</strong></span><span class="sxs-lookup"><span data-stu-id="057b9-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="057b9-141">Nakil profilinin belirli bir satıcı, bir satıcı grubu veya tüm satıcılar için mi geçerli olduğunu belirtin:</span><span class="sxs-lookup"><span data-stu-id="057b9-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="057b9-142"><strong>Tablo</strong> – Nakil profili bir satıcı için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="057b9-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="057b9-143"><strong>Hesap/Grup numarası</strong> alanında satıcı hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="057b9-144"><strong>Grup</strong> – Nakil profili bir satıcı grubu geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="057b9-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="057b9-145"><strong>Hesap/Grup numarası</strong> alanında satıcı grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="057b9-146"><strong>Tümü</strong> – Nakil profili tüm satıcılar için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="057b9-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="057b9-147"><strong>Hesap/Grup numarası</strong> alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="057b9-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="057b9-148"><strong>Hesap/Grup numarası</strong></span><span class="sxs-lookup"><span data-stu-id="057b9-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="057b9-149"><strong>Hesap kodu</strong> alanında <strong>Tablo</strong> seçiliyse, nakil profiliyle ilişkilendirilmiş satıcının hesap numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="057b9-150"><strong>Grup</strong> seçiliyse bir satıcı grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="057b9-151"><strong>Tümü</strong> seçiliyse bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="057b9-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="057b9-152"><strong>Özet hesap</strong></span><span class="sxs-lookup"><span data-stu-id="057b9-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="057b9-153">Nakil profilinin ilişkili olduğu satıcılar için özet hesabı olarak kullanılacak genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="057b9-154">Bu ana hesap için <strong> el ile girme</strong> giriş parametresine izin verme parametresi işaretlenecek.</span><span class="sxs-lookup"><span data-stu-id="057b9-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="057b9-155">Bu hesabı sonradan hedef deftere nakit profilinden kaldırırsanız <strong>Ana hesaplar</strong> sayfasında <strong>El ile giriş yapılmasına izin verme</strong> ayarını da doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="057b9-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="057b9-156"><strong>Not:</strong> Eğer <strong>Nakil tanımlarını kullan</strong> seçeneği <strong>Genel muhasebe parametreleri</strong> sayfasında seçiliyse özet hesabı yerine satıcı faturaları için hareket nakil tanımı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="057b9-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="057b9-157"><strong>Kapatma hesabı</strong></span><span class="sxs-lookup"><span data-stu-id="057b9-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="057b9-158">Nakit akışı tahminleri için kullanılacak likidite genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="057b9-159">Bu alan yalnızca nakit akışı tahmini etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="057b9-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="057b9-160"><strong>Satış vergisi ön ödemeleri</strong></span><span class="sxs-lookup"><span data-stu-id="057b9-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="057b9-161">Avans olarak alınmış ödemeler için satış vergisinin hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="057b9-162"><strong>Not:</strong> Bir ödeme, ön ödeme olarak işaretlendiğinde kullanılan <strong>Nakil</strong> profili, <strong>Borç hesapları parametreleri</strong>  sayfasının <strong>Genel muhasebe ve satış vergisi</strong>bölümündeki <strong>Ön ödeme günlüğü fişi</strong> alanında seçilir.</span><span class="sxs-lookup"><span data-stu-id="057b9-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="057b9-163"><strong>Varış</strong></span><span class="sxs-lookup"><span data-stu-id="057b9-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="057b9-164">Onaylanmayan satıcı faturaları hakkındaki bilgilerin nakledildiği genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="057b9-165">Bilgiler Fatura kayıt günlüğüne girilir.</span><span class="sxs-lookup"><span data-stu-id="057b9-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="057b9-166">Örneğin, bir kullanıcı, fatura kaydına girdiklerinde satıcı faturaları hakkındaki temel bilgileri girer.</span><span class="sxs-lookup"><span data-stu-id="057b9-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="057b9-167">Fatura kaydı nakledildiğinde, hareketler buraya ve <strong>Mahsup hesap</strong> alanına girilen hesaba nakledilir.</span><span class="sxs-lookup"><span data-stu-id="057b9-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="057b9-168">Faturalar onaylandığında, borç varış hesabından satıcı özet hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="057b9-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="057b9-169"><strong>Mahsup hesabı</strong></span><span class="sxs-lookup"><span data-stu-id="057b9-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="057b9-170">Fatura kaydını kullanarak güncelleştirilen onaylanmamış satıcı faturalarının mahsuben kullanılan genel muhasebe hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="057b9-171">Mahsup hesabı Varış hesaplarına nakledilen hareketler için mahsup hesabı olarak işlev görür.</span><span class="sxs-lookup"><span data-stu-id="057b9-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="057b9-172">Bu nedenle, hesap henüz onaylanmamış satıcı satınalma işlemleri içerir.</span><span class="sxs-lookup"><span data-stu-id="057b9-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="057b9-173">**Tablo kısıtlamaları**</span><span class="sxs-lookup"><span data-stu-id="057b9-173">**Table restrictions**</span></span>

<span data-ttu-id="057b9-174">Seçili nakil profilini içeren hareketler için hareketlerin otomatik olarak kapatılması, faiz hesaplanması ve tahsilat mektuplarının verilip verilmeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="057b9-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="057b9-175">Ayrıca, seçili nakil profilini içeren hareketler kapatıldığında kullanılan hesabı seçin seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="057b9-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="057b9-176">Deftere nakil profilinizi ayarlamak için aşağıdaki değerleri belirtin</span><span class="sxs-lookup"><span data-stu-id="057b9-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="057b9-177">Alan</span><span class="sxs-lookup"><span data-stu-id="057b9-177">Field</span></span>          | <span data-ttu-id="057b9-178">Tanım</span><span class="sxs-lookup"><span data-stu-id="057b9-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="057b9-179">**Kapatma**</span><span class="sxs-lookup"><span data-stu-id="057b9-179">**Settlement**</span></span> | <span data-ttu-id="057b9-180">Bu nakil profilini içeren hareketlerin otomatik kapatılmasını etkinleştirmek için bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="057b9-181">Bu seçenek temizlenirse, hareketleri, **Açık hareketleri kapat** sayfasını kullanarak elden kapatmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="057b9-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="057b9-182">**İptal**</span><span class="sxs-lookup"><span data-stu-id="057b9-182">**Cancel**</span></span>     | <span data-ttu-id="057b9-183">Bu nakil profilini içeren hareketlerin iptal edilmesi seçeneğine sahip olmak istiyorsanız bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="057b9-184">**Kapat**</span><span class="sxs-lookup"><span data-stu-id="057b9-184">**Close**</span></span>      | <span data-ttu-id="057b9-185">Bu nakil profilini içeren hareketler kapatılırken değiştirmek istediğiniz nakil profilini seçin.</span><span class="sxs-lookup"><span data-stu-id="057b9-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="057b9-186">Bir hareket tamamen kapatıldığında kapanmış kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="057b9-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]