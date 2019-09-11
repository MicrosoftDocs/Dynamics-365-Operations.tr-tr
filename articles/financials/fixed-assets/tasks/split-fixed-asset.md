---
title: Sabit kıymeti bölme
description: Bu konu bir kıymet defteri yüzdesini yeni bir kıymet defterine bölmeyi açıklar.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867595"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="c35d0-103">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="c35d0-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c35d0-104">Bu konu bir kıymet defteri yüzdesini yeni bir kıymet defterine bölmeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="c35d0-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="c35d0-105">Kılavuzda Muhasebeci rolü ve USMF demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c35d0-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="c35d0-106">Yeni bir sabit kıymet oluştur</span><span class="sxs-lookup"><span data-stu-id="c35d0-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="c35d0-107">Gezinti bölmesinde **Modüller > Sabit kıymetler > Sabit kıymetler > Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="c35d0-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-108">Select **New**.</span></span>
3. <span data-ttu-id="c35d0-109">**Sabit kıymet grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="c35d0-110">Sabit kıymet numarasını, bölme işleminde daha sonra kullanmak üzere not alın.</span><span class="sxs-lookup"><span data-stu-id="c35d0-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="c35d0-111">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c35d0-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c35d0-112">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="c35d0-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="c35d0-113">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="c35d0-113">Split a fixed asset</span></span>
1. <span data-ttu-id="c35d0-114">Listede, bölünecek sabit kıymetin bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="c35d0-115">**Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-115">Select **Books**.</span></span> <span data-ttu-id="c35d0-116">Yeni kıymete bölünecek defteri seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="c35d0-117">**İşlevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-117">Select **Functions**.</span></span>
4. <span data-ttu-id="c35d0-118">**Sabit kıymet böl**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="c35d0-119">**Sabit kıymet** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="c35d0-120">**Deftere** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c35d0-121">**Hareket tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="c35d0-122">**Yüzde** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="c35d0-123">**Günlük adı** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="c35d0-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="c35d0-125">Günlük hareketini deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="c35d0-125">Post the journal transaction</span></span>
1. <span data-ttu-id="c35d0-126">Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="c35d0-127">Listede, bölme işlemiyle oluşturulan günlüğü seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="c35d0-128">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-128">Select **Lines**.</span></span>

    - <span data-ttu-id="c35d0-129">Oluşturulan günlük satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="c35d0-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="c35d0-130">Değeri, bölünme işlemi sırasında belirtilen yüzde oranında azaltmak üzere, orijinal kıymet için bir Alım düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c35d0-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="c35d0-131">Yeni kıymet için aynı tutarda bir düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c35d0-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="c35d0-132">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c35d0-132">Select **Post**.</span></span>

