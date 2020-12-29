---
title: Hesap ve boyut kombinasyonları (segmentlere ayrılmış giriş kontrolü) girme
description: Bu makalede, hesap ve boyut birleşimlerinin veya genel muhasebe hesaplarının nasıl girileceği açıklanmaktadır. Giriş deneyimine sıklıkla bölümlenmiş giriş denetimi denir.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 872ee7812d98e6102798c3a10773176541c02c90
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448702"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="dc3fe-104">Hesap ve boyut kombinasyonları (segmentlere ayrılmış giriş kontrolü) girme</span><span class="sxs-lookup"><span data-stu-id="dc3fe-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc3fe-105">Bu makalede, hesap ve boyut birleşimlerinin veya genel muhasebe hesaplarının nasıl girileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="dc3fe-106">Giriş deneyimine sıklıkla bölümlenmiş giriş denetimi denir.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="dc3fe-107">Kullanıcılar çeşitli sayfalarda, örneğin genel günlük, bütçeleme ve nakil tanımları sayfalarında hesap ve boyut kombinasyonları girebilirler.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="dc3fe-108">Geçerli hesap ve boyut kombinasyonları, deftere atanan hesap yapılarına ve hesap yapılarına atanan gelişmiş kurallara bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="dc3fe-109">Kullanıcılar bir kombinasyon girdiğinde değerleri el ile yazabilir veya zengin, arama deneyiminin avantajlarından yararlanabilirler.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="dc3fe-110">Alana girdiğinizde, yazmaya başlayabilirsiniz ve alan değeri ve açıklamayı arar.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="dc3fe-111">Örneğin, 180 yazarsanız, bu sayı bileşimi ile başlayan herhangi bir değeri arar.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="dc3fe-112">Veya nakit yazabilirsiniz ve nakit ile başlayan bir açıklamaya sahip olan herhangi bir değeri arar.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="dc3fe-113">Değer veya açıklamanın arama kriterini içerip içermediğini aramak için \*Nakit veya \*180 gibi bir joker de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="dc3fe-114">Aşağıdaki tabloda arama kapatıldığında kullanılabilecek klavye kısayolları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc3fe-115">Klavye kısayolu</span><span class="sxs-lookup"><span data-stu-id="dc3fe-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="dc3fe-116">Eylem</span><span class="sxs-lookup"><span data-stu-id="dc3fe-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc3fe-117">Alt+Aşağı Ok</span><span class="sxs-lookup"><span data-stu-id="dc3fe-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="dc3fe-118">Aramayı açar.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-118">Open the lookup.</span></span> <span data-ttu-id="dc3fe-119">Alt + Aşağı Ok tuşlarına ikinci defa basarsanız odak, çıkmadaki segmentlere taşınır.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="dc3fe-120">Enter ve Shift+Enter</span><span class="sxs-lookup"><span data-stu-id="dc3fe-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="dc3fe-121">Hesap planı ayırıcısı</span><span class="sxs-lookup"><span data-stu-id="dc3fe-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="dc3fe-122">Sağ Ok ve Sol Ok</span><span class="sxs-lookup"><span data-stu-id="dc3fe-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="dc3fe-123">Bir sonraki veya bir önceki segmente geçer.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc3fe-124">Sekme</span><span class="sxs-lookup"><span data-stu-id="dc3fe-124">Tab</span></span></td>
<td><span data-ttu-id="dc3fe-125">Izgaradaki bir sonraki alana geçer.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="dc3fe-126">Aşağıdaki tabloda arama açıkken kullanılabilecek klavye kısayolları açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc3fe-127">Klavye kısayolu</span><span class="sxs-lookup"><span data-stu-id="dc3fe-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="dc3fe-128">Eylem</span><span class="sxs-lookup"><span data-stu-id="dc3fe-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc3fe-129">Esc</span><span class="sxs-lookup"><span data-stu-id="dc3fe-129">Esc</span></span></td>
<td><span data-ttu-id="dc3fe-130">Aramayı kapatır.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="dc3fe-131">Yukarı Ok ve Aşağı Ok</span><span class="sxs-lookup"><span data-stu-id="dc3fe-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="dc3fe-132">Page Up ve Page Down</span><span class="sxs-lookup"><span data-stu-id="dc3fe-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="dc3fe-133">Home ve End</span><span class="sxs-lookup"><span data-stu-id="dc3fe-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="dc3fe-134">Listelerdeki bir önceki veya bir sonraki değere, bir önceki veya bir sonraki değer grubuna veya aramadaki ilk veya son öğeye geçer.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="dc3fe-135">Hesap planı ayırıcısı</span><span class="sxs-lookup"><span data-stu-id="dc3fe-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="dc3fe-136">Sağ Ok ve Sol Ok</span><span class="sxs-lookup"><span data-stu-id="dc3fe-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="dc3fe-137">Bir sonraki veya bir önceki segmente geçer.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc3fe-138">Sekme</span><span class="sxs-lookup"><span data-stu-id="dc3fe-138">Tab</span></span></td>
<td><span data-ttu-id="dc3fe-139">Izgaradaki bir sonraki alana geçer.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc3fe-140">Alt+W</span><span class="sxs-lookup"><span data-stu-id="dc3fe-140">Alt+W</span></span></td>
<td><span data-ttu-id="dc3fe-141"><strong>Tümünü göster</strong> ile <strong>Geçerli olanı göster</strong> arasında geçiş sağlar.</span><span class="sxs-lookup"><span data-stu-id="dc3fe-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>





