---
title: "Satıcı faturası günlükleri ve fatura onay günlükleri için varsayılan mahsup hesaplar"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c2b62eafc71b5d1ad4eaaf252efd1dcbb97b86f3
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="5bd2d-102">Satıcı faturası günlükleri ve fatura onay günlükleri için varsayılan mahsup hesaplar</span><span class="sxs-lookup"><span data-stu-id="5bd2d-102">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="5bd2d-103">Varsayılan mahsup hesapları, aşağıdaki satıcı faturası günlük sayfalarında kullanılır:</span><span class="sxs-lookup"><span data-stu-id="5bd2d-103">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="5bd2d-104">Fatura günlüğü</span><span class="sxs-lookup"><span data-stu-id="5bd2d-104">Invoice journal</span></span>
-   <span data-ttu-id="5bd2d-105">Fatura onay günlüğü</span><span class="sxs-lookup"><span data-stu-id="5bd2d-105">Invoice approval journal</span></span>

<span data-ttu-id="5bd2d-106">Fatura günlükleri için varsayılan hesaplar atamanız gerekip gerekmediğine karar vermenize yardımcı olacak aşağıdaki tabloyu kullanın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-106">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5bd2d-107">Varsayılan hesapları buradan ayarla</span><span class="sxs-lookup"><span data-stu-id="5bd2d-107">Set up default accounts here</span></span></th>
<th><span data-ttu-id="5bd2d-108">Varsayılan hesaplar nerede sağlanıyor</span><span class="sxs-lookup"><span data-stu-id="5bd2d-108">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="5bd2d-109">Bu seçenek işlemi nasıl etkiler</span><span class="sxs-lookup"><span data-stu-id="5bd2d-109">How this option affects processing</span></span></th>
<th><span data-ttu-id="5bd2d-110">Ne zaman bu seçeneği kullanmalısınız</span><span class="sxs-lookup"><span data-stu-id="5bd2d-110">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5bd2d-111"><strong>Satıcı grubu</strong> – <strong>Varsayılan hesap ayarı</strong> sayfasında satıcı grupları için varsayılan mahsup hesapları ayarlayın. Bu sayfayı <strong>Satıcı grupları</strong> sayfasından açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-111"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="5bd2d-112">Satıcı hesabı</span><span class="sxs-lookup"><span data-stu-id="5bd2d-112">Vendor account</span></span></li>
<li><span data-ttu-id="5bd2d-113">Satıcı hesapları için varsayılan hesaplar belirtilmediyse, satıcı grubundaki satıcı hesapları için günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="5bd2d-113">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="5bd2d-114">Satıcı grupları için varsayılan mahsup hesaplar <strong>Varsayılan hesap ayarı</strong> sayfasındaki satıcılar için varsayılan mahsup hesapları olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-114">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="5bd2d-115">Bu sayfayı <strong>Tüm satıcılar</strong> liste sayfasından açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-115">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="5bd2d-116">Genellikle zaman içinde aynı satıcı gruplarından aynı türde maddeler için ödeme yapıyorsanız bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-116">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5bd2d-117"><strong>Satıcı hesabı</strong> – <strong>Varsayılan hesap ayarı</strong> sayfasındaki satıcı hesapları için varsayılan hesaplar ayarlayın. Bu sayfayı <strong>Satıcılar</strong> sayfasından açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-117"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="5bd2d-118">Satıcı hesabı için günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="5bd2d-118">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="5bd2d-119">Satıcı hesapları için varsayılan mahsup hesaplar, satıcı hesabına ilişkin günlük girişleri için varsayılan mahsup hesapları olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-119">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="5bd2d-120">Genellikle zaman içinde aynı satıcılara aynı türde maddeler için ödeme yapıyorsanız bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-120">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5bd2d-121"><strong>Günlük adları</strong> – <strong>Günlük adları</strong> sayfasında günlükler için varsayılan mahsup hesapları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-121"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="5bd2d-122"><strong>Sabit mahsup hesap</strong> seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-122">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="5bd2d-123">Günlük adlarının günlük türü <strong>Fatura kaydı</strong> veya <strong>Onay</strong> olduğunda, günlük adlarında varsayılan mahsup hesapları belirtemeyeceğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-123">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="5bd2d-124">Günlük adını kullanan günlük başlığı</span><span class="sxs-lookup"><span data-stu-id="5bd2d-124">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="5bd2d-125">Günlük adını kullanan günlüklerdeki günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="5bd2d-125">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="5bd2d-126"><strong>Günlük adları</strong> sayfasında <strong>Sabit mahsup hesap</strong> seçeneği seçilirse, günlük adı için mahsup hesap satıcı veya satıcı grubuna ilişkin varsayılan mahsup hesabı geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-126">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="5bd2d-127">Satıcı veya satıcının ait olduğu satıcı grubuna bakılmaksızın, belirli hesaplara borçlandırılan belirli maliyetler ve giderler için günlükleri ayarlarken bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-127">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5bd2d-128"><strong>Günlük adları</strong> – <strong>Günlük adları</strong> sayfasında günlükler için varsayılan mahsup hesapları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-128"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="5bd2d-129"><strong>Sabit mahsup hesap</strong> seçimini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-129">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="5bd2d-130">Günlük adlarının günlük türü <strong>Fatura kaydı</strong> veya <strong>Onay</strong> olduğunda, günlük adlarında varsayılan mahsup hesapları belirtemeyeceğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-130">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="5bd2d-131">Günlük başlığı</span><span class="sxs-lookup"><span data-stu-id="5bd2d-131">Journal header</span></span></li>
<li><span data-ttu-id="5bd2d-132">Günlük adını kullanan günlüklerdeki günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="5bd2d-132">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="5bd2d-133">Bu varsayılan girişler günlük başlığı sayfalarında kullanılır ve günlük başlığı sayfasındaki mahsup hesap, günlük fişi sayfalarında varsayılan giriş olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-133">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="5bd2d-134"><strong>Günlük adları </strong>sayfasındaki varsayılan hesaplar yalnızca satıcı hesabı için varsayılan hesaplar ayarlanmadığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-134">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="5bd2d-135">Bu seçeneği, varsayılan satıcı mahsup hesabı atanmadığında kullanılan varsayılan hesaplar ayarlamak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-135">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5bd2d-136"><strong>Günlük başlığı</strong> – Günlük fişi sayfalarındaki varsayılan giriş olarak bir günlük için varsayılan mahsup hesap ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-136"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="5bd2d-137">Günlük adlarının günlük türü <strong>Fatura kaydı</strong> veya <strong>Onay</strong> olduğunda, günlük başlığında varsayılan mahsup hesaplar belirtemeyeceğinizi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-137">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="5bd2d-138">Günlükteki günlük girişleri</span><span class="sxs-lookup"><span data-stu-id="5bd2d-138">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="5bd2d-139">Bir günlüğe ilişkin varsayılan mahsup hesabı, günlük fişi sayfalarında varsayılan giriş olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-139">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="5bd2d-140">Bir günlükteki girişlerin çoğu aynı mahsup hesabına sahip olduğunda veri girişini hızlandırmak için bu seçeneği kullanın.</span><span class="sxs-lookup"><span data-stu-id="5bd2d-140">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






