---
title: "Satıcı faturası günlükleri ve fatura onay günlükleri için varsayılan mahsup hesaplar"
description: "Bu konu, fatura günlükleri için varsayılan hesaplar atamanız gerekip gerekmediğine karar vermenize yardımcı olur."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f876e5dfdab67dd98b2449993c3ba2baacde1587
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="cb8f4-103">Satıcı faturası günlükleri ve fatura onay günlükleri için varsayılan mahsup hesaplar</span><span class="sxs-lookup"><span data-stu-id="cb8f4-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb8f4-104">Varsayılan mahsup hesapları, aşağıdaki satıcı faturası günlük sayfalarında kullanılır:</span><span class="sxs-lookup"><span data-stu-id="cb8f4-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="cb8f4-105">Fatura günlüğü</span><span class="sxs-lookup"><span data-stu-id="cb8f4-105">Invoice journal</span></span>
-   <span data-ttu-id="cb8f4-106">Fatura onay günlüğü</span><span class="sxs-lookup"><span data-stu-id="cb8f4-106">Invoice approval journal</span></span>

<span data-ttu-id="cb8f4-107">Fatura günlükleri için varsayılan hesaplar atamanız gerekip gerekmediğine karar vermenize yardımcı olacak aşağıdaki tabloyu kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb8f4-108">Varsayılan hesapları buradan ayarla</span><span class="sxs-lookup"><span data-stu-id="cb8f4-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="cb8f4-109">Varsayılan hesaplar nerede sağlanıyor</span><span class="sxs-lookup"><span data-stu-id="cb8f4-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="cb8f4-110">Bu seçenek işlemi nasıl etkiler</span><span class="sxs-lookup"><span data-stu-id="cb8f4-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="cb8f4-111">Ne zaman bu seçeneği kullanmalısınız</span><span class="sxs-lookup"><span data-stu-id="cb8f4-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb8f4-112"><strong>Satıcı grubu</strong> – <strong>Varsayılan hesap ayarı</strong> sayfasında satıcı grupları için varsayılan mahsup hesapları ayarlayın. Bu sayfayı <strong>Satıcı grupları</strong> sayfasından açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="cb8f4-113">Satıcı hesabı</span><span class="sxs-lookup"><span data-stu-id="cb8f4-113">Vendor account</span></span></li>
<li><span data-ttu-id="cb8f4-114">Satıcı hesapları için varsayılan hesaplar belirtilmediyse, satıcı grubundaki satıcı hesapları için günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="cb8f4-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="cb8f4-115">Satıcı grupları için varsayılan mahsup hesaplar <strong>Varsayılan hesap ayarı</strong> sayfasındaki satıcılar için varsayılan mahsup hesapları olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="cb8f4-116">Bu sayfayı <strong>Tüm satıcılar</strong> liste sayfasından açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="cb8f4-117">Genellikle zaman içinde aynı satıcı gruplarından aynı türde maddeler için ödeme yapıyorsanız bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb8f4-118"><strong>Satıcı hesabı</strong> – <strong>Varsayılan hesap ayarı</strong> sayfasındaki satıcı hesapları için varsayılan hesaplar ayarlayın. Bu sayfayı <strong>Satıcılar</strong> sayfasından açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="cb8f4-119">Satıcı hesabı için günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="cb8f4-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="cb8f4-120">Satıcı hesapları için varsayılan mahsup hesaplar, satıcı hesabına ilişkin günlük girişleri için varsayılan mahsup hesapları olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="cb8f4-121">Genellikle zaman içinde aynı satıcılara aynı türde maddeler için ödeme yapıyorsanız bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb8f4-122"><strong>Günlük adları</strong> – <strong>Günlük adları</strong> sayfasında günlükler için varsayılan mahsup hesapları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="cb8f4-123"><strong>Sabit mahsup hesap</strong> seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="cb8f4-124">Günlük adlarının günlük türü <strong>Fatura kaydı</strong> veya <strong>Onay</strong> olduğunda, günlük adlarında varsayılan mahsup hesapları belirtemeyeceğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="cb8f4-125">Günlük adını kullanan günlük başlığı</span><span class="sxs-lookup"><span data-stu-id="cb8f4-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="cb8f4-126">Günlük adını kullanan günlüklerdeki günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="cb8f4-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="cb8f4-127"><strong>Günlük adları</strong> sayfasında <strong>Sabit mahsup hesap</strong> seçeneği seçilirse, günlük adı için mahsup hesap satıcı veya satıcı grubuna ilişkin varsayılan mahsup hesabı geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="cb8f4-128">Satıcı veya satıcının ait olduğu satıcı grubuna bakılmaksızın, belirli hesaplara borçlandırılan belirli maliyetler ve giderler için günlükleri ayarlarken bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb8f4-129"><strong>Günlük adları</strong> – <strong>Günlük adları</strong> sayfasında günlükler için varsayılan mahsup hesapları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="cb8f4-130"><strong>Sabit mahsup hesap</strong> seçimini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="cb8f4-131">Günlük adlarının günlük türü <strong>Fatura kaydı</strong> veya <strong>Onay</strong> olduğunda, günlük adlarında varsayılan mahsup hesapları belirtemeyeceğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="cb8f4-132">Günlük başlığı</span><span class="sxs-lookup"><span data-stu-id="cb8f4-132">Journal header</span></span></li>
<li><span data-ttu-id="cb8f4-133">Günlük adını kullanan günlüklerdeki günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="cb8f4-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="cb8f4-134">Bu varsayılan girişler günlük başlığı sayfalarında kullanılır ve günlük başlığı sayfasındaki mahsup hesap, günlük fişi sayfalarında varsayılan giriş olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="cb8f4-135"><strong>Günlük adları </strong>sayfasındaki varsayılan hesaplar yalnızca satıcı hesabı için varsayılan hesaplar ayarlanmadığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="cb8f4-136">Bu seçeneği, varsayılan satıcı mahsup hesabı atanmadığında kullanılan varsayılan hesaplar ayarlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb8f4-137"><strong>Günlük başlığı</strong> – Günlük fişi sayfalarındaki varsayılan giriş olarak bir günlük için varsayılan mahsup hesap ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="cb8f4-138">Günlük adlarının günlük türü <strong>Fatura kaydı</strong> veya <strong>Onay</strong> olduğunda, günlük başlığında varsayılan mahsup hesaplar belirtemeyeceğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="cb8f4-139">Günlükteki günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="cb8f4-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="cb8f4-140">Bir günlüğe ilişkin varsayılan mahsup hesabı, günlük fişi sayfalarında varsayılan giriş olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="cb8f4-141">Bir günlükteki girişlerin çoğu aynı mahsup hesabına sahip olduğunda veri girişini hızlandırmak için bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb8f4-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






