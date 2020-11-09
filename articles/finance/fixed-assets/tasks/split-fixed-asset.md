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
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000305"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="c8a9a-103">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="c8a9a-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8a9a-104">Bu konu bir kıymet defteri yüzdesini yeni bir kıymet defterine bölmeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="c8a9a-105">Kılavuzda Muhasebeci rolü ve USMF demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="c8a9a-106">Yeni bir sabit kıymet oluştur</span><span class="sxs-lookup"><span data-stu-id="c8a9a-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="c8a9a-107">Gezinti bölmesinde **Modüller \> Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler** 'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="c8a9a-108">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-108">Select **New**.</span></span>
3. <span data-ttu-id="c8a9a-109">**Sabit kıymet grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="c8a9a-110">Sabit kıymet numarasını, bölme işleminde daha sonra kullanmak üzere not alın.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="c8a9a-111">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="c8a9a-112">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="c8a9a-113">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="c8a9a-113">Split a fixed asset</span></span>

<span data-ttu-id="c8a9a-114">Tam amortismana tabi bir kıymet bölünmeden önce, kıymet defteri durumunun elle **Kapalı** 'dan **Açık** 'a değiştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="c8a9a-115">Bu adım gereklidir, çünkü kıymetle ilgili işlemleri deftere nakletmeniz gerekiyorsa (örneğin, elden çıkarma satışı için) Defter durumunun **Açık** olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="c8a9a-116">Kıymet defteri durumu değiştirildikten sonra, kıymeti bölmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-116">After the asset book status is changed, follow these steps to split the asset.</span></span>

1. <span data-ttu-id="c8a9a-117">Listede, bölünecek sabit kıymetin bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-117">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="c8a9a-118">**Defterler** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-118">Select **Books**.</span></span> <span data-ttu-id="c8a9a-119">Yeni kıymete bölünecek defteri seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-119">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="c8a9a-120">**İşlevler** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-120">Select **Functions**.</span></span>
4. <span data-ttu-id="c8a9a-121">**Sabit kıymet böl** 'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-121">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="c8a9a-122">**Sabit kıymet** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-122">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="c8a9a-123">**Deftere** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-123">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c8a9a-124">**Hareket tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-124">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="c8a9a-125">**Yüzde** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-125">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="c8a9a-126">**Günlük adı** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-126">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="c8a9a-127">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-127">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="c8a9a-128">Günlük hareketini deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="c8a9a-128">Post the journal transaction</span></span>

1. <span data-ttu-id="c8a9a-129">Gezinti bölmesinde **Modüller \> Sabit kıymetler \> Günlük girişleri \> Sabit kıymetler günlüğü** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-129">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="c8a9a-130">Listede, bölme işlemiyle oluşturulan günlüğü seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-130">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="c8a9a-131">**Satırlar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-131">Select **Lines**.</span></span>

    - <span data-ttu-id="c8a9a-132">Oluşturulan günlük satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-132">Verify the journal lines created.</span></span>
    - <span data-ttu-id="c8a9a-133">Değeri, bölünme işlemi sırasında belirtilen yüzde oranında azaltmak üzere, orijinal kıymet için bir Alım düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-133">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="c8a9a-134">Yeni kıymet için aynı tutarda bir düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-134">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="c8a9a-135">**Naklet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c8a9a-135">Select **Post**.</span></span>
