---
title: Müşteri yaşlandırma raporu
description: Müşteri yaşlandırma raporu müşterilerin ödemesi gereken bakiyeleri, tarih aralığına veya yaşlandırma dönemine göre sıralanmış olarak görüntüler.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 062e8972c879d770cc4106c2811cd4c16fff0446
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974873"
---
# <a name="customer-aging-report"></a><span data-ttu-id="17b9b-103">Müşteri yaşlandırma raporu</span><span class="sxs-lookup"><span data-stu-id="17b9b-103">Customer aging report</span></span> 

<span data-ttu-id="17b9b-104">**Müşteri yaşlandırma** raporu müşterilerin ödemesi gereken bakiyeleri, tarih aralığına veya yaşlandırma dönemine göre sıralanmış olarak görüntüler.</span><span class="sxs-lookup"><span data-stu-id="17b9b-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="17b9b-105">Raporu oluşturduğunuz zaman aşağıdaki varsayılan parametreler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="17b9b-106">Bu parametreleri, raporda gösterilecek verileri filtrelemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17b9b-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="17b9b-107">Daha fazla bilgi için bkz. [Koleksiyonlar ayarlama](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="17b9b-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17b9b-108">Alan</span><span class="sxs-lookup"><span data-stu-id="17b9b-108">Field</span></span></p></th>
<th><p><span data-ttu-id="17b9b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="17b9b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-110"><strong>Faturalama sınıflandırması</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-111">Rapora dahil edilecek bir veya daha fazla faturalama sınıflandırması seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="17b9b-112">**Not:** Bu denetim yalnızca <STRONG>Kamu Sektörü</STRONG> yapılandırma anahtarı seçildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17b9b-113"><strong>Faturalama sınıflandırması olmayan hareketleri dahil et</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-114">Bu onay kutusu işaretlenirse, kendilerine atanmış bir faturalama sınıflandırması bulunmayan tüm hareketler raporda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="17b9b-115">**Not:** Bu denetim yalnızca <STRONG>Kamu sektörü</STRONG> yapılandırma anahtarı seçildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-116"><strong>Yaşlandırma başlangıcı</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-117">Geçerli yaşlandırma aralığı üzerinde kullanılan tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-118"><strong>Bakiye tarihi</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-119">Müşteri bakiyelerinin görüntüleneceği tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="17b9b-120">Bu, hareketler için kesme tarihi olarak da bilinir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17b9b-121"><strong>Başlangıç tarihi</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-122">Rapora dahil edilecek ilk dönem aralığı veya yaşlandırma döneminde bulunan bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-123"><strong>Ölçütler</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-124">Raporun temel alacağı tarih türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="17b9b-125"><strong>Hareket tarihi</strong> - Hareketlerin deftere nakil tarihi.</span><span class="sxs-lookup"><span data-stu-id="17b9b-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="17b9b-126">Örneğin bu, vade tarihinin hesaplanması için temel oluşturan bir fatura tarihi olabilir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="17b9b-127"><strong>Vade tarihi</strong> – Ödeme koşullarınız temel alınarak belirlenen ve hareketlere ait vade tarihi.</span><span class="sxs-lookup"><span data-stu-id="17b9b-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="17b9b-128"><strong>Belge tarihi</strong> – Vade tarihinin hesaplanması için temel olarak alınan ve kullanıcı tarafından tanımlanmış belge tarihi.</span><span class="sxs-lookup"><span data-stu-id="17b9b-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17b9b-129"><strong>Yaşlandırma dönemi tanımı</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-130">Bir yaşlandırma dönemi tanımı seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-130">Select an aging period definition.</span></span> <span data-ttu-id="17b9b-131">Yaşlandırma aralığı tanımı seçerseniz <strong>aralık</strong> alanı kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="17b9b-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="17b9b-132">Altı yaşlandırma döneminden daha fazla dönem içeren yaşlandırma dönemi tanımları yazdırılan raporda kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="17b9b-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="17b9b-133">**Not:** <STRONG>Yaşlandırma dönemi tanımları</STRONG> sayfasında yaşlandırma dönemleri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17b9b-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-134"><strong>Yaşlandırma dönemi açıklamasını yazdır</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-135">Yaşlandırma dönemi açıklamalarını rapordaki her yaşlandırma dönemi sütununun üst kısmına dahil etmek için <strong>Evet</strong> seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="17b9b-136">Raporu sütun başlıkları olmadan yazdırmak için <strong>Hayır</strong>'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17b9b-137"><strong>Aralık</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-138">Her dönemdeki gün veya ay sayısını girerek, kullanılacak dönemi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="17b9b-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="17b9b-139">Örneğin, yaşlandırma bilgilerini haftalık olarak görüntülemek için bu alana 7 girin ve <strong>Gün/Ay</strong> alanında <strong>Gün</strong> seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="17b9b-140">**Not:** Bu alana girdiğiniz bilgiler yalnızca bir yaşlandırma dönemi tanımı seçmemişseniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="17b9b-141">Aksi durumda, yazdırma yönü yaşlandırma dönemi tanımında tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="17b9b-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-142"><strong>Gün/Ay</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-143"><strong>Aralık</strong> alanında dönemi tanımlamak için kullanılan birimi (<strong>Gün</strong> veya <strong>Ay</strong>) olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17b9b-144"><strong>Yazdırma yönü</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-145">Bakiyelerin hesapnaıp hesaplamayacağını ve geçmiş veya gelecekteki dönemler için yaşlandırma raporunu yazdırmayı seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="17b9b-146">Tarihler, <strong>Bakiyesi açık</strong> alanında seçilen tarihe göre değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="17b9b-147">Geçmiş dönemlerin bilgilerini göstermek için <strong>Geriye dönük</strong> seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="17b9b-148">Gelecek dönemlerin bilgilerini göstermek için <strong>İleriye dönük</strong> seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>

<span data-ttu-id="17b9b-149">**Not:** Bu alana girdiğiniz bilgiler yalnızca bir yaşlandırma dönemi tanımı seçmemişseniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-149">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-150"><strong>Ayrıntılı</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-151">Raporda gösterilen bakiyelere dahil edilen hareketleri listelemek için seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17b9b-152"><strong>Tutarları hareket para birimi cinsinden ekle</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-153">Muhasebe para birimi cinsinden tutarlara ek olarak, tutarları hareket para birimine dahil etmek için seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="17b9b-154">Bu onay kutusu işaretli değilse, rapordaki tutarlar yalnızca muhasebe para biriminde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-155"><strong>Eksi bakiye</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-156">Negatif bakiyeleri olan müşteri hesaplarını dahil etmek için seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17b9b-157"><strong>Sıfır bakiye hesaplarını hariç tut</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-158">Sıfır bakiyesi olan müşteri hesaplarını dışarıda bırakmak için seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17b9b-159"><strong>Ödeme yerleştirme</strong></span><span class="sxs-lookup"><span data-stu-id="17b9b-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="17b9b-160">Henüz kapatılmamış ödemeleri görüntülemek için seçin.</span><span class="sxs-lookup"><span data-stu-id="17b9b-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="17b9b-161">Bunlar raporun ilk sütununda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="17b9b-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

