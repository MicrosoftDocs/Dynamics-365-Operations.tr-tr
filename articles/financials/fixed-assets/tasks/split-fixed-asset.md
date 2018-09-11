--- 
title: "Sabit kıymeti bölme"
description: "Bu görev kılavuzu bir kıymet defteri yüzdesini yeni bir kıymet defterine böler."
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 9126514d397250f52633554a1df2f66f4747d42a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="459e5-103">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="459e5-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="459e5-104">Bu görev kılavuzu bir kıymet defteri yüzdesini yeni bir kıymet defterine böler.</span><span class="sxs-lookup"><span data-stu-id="459e5-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="459e5-105">Kılavuzda Muhasebeci rolü ve USMF demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="459e5-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="459e5-106">Yeni bir sabit kıymet oluştur</span><span class="sxs-lookup"><span data-stu-id="459e5-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="459e5-107">Sabit kıymetler > Sabit kıymetler > Sabit kıymetler menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="459e5-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="459e5-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="459e5-108">Click New.</span></span>
3. <span data-ttu-id="459e5-109">Sabit kıymet grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="459e5-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="459e5-110">Sabit kıymet numarasını, bölme işleminde daha sonra kullanmak üzere not alın.</span><span class="sxs-lookup"><span data-stu-id="459e5-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="459e5-111">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="459e5-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="459e5-112">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="459e5-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="459e5-113">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="459e5-113">Split a fixed asset</span></span>
1. <span data-ttu-id="459e5-114">Listede, bölünecek sabit kıymeti seçin.</span><span class="sxs-lookup"><span data-stu-id="459e5-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="459e5-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="459e5-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="459e5-116">Defterler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="459e5-116">Click Books.</span></span>
    * <span data-ttu-id="459e5-117">Yeni kıymete bölünecek defteri seçin.</span><span class="sxs-lookup"><span data-stu-id="459e5-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="459e5-118">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="459e5-118">Click Functions.</span></span>
5. <span data-ttu-id="459e5-119">Sabit kıymet parçala'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="459e5-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="459e5-120">Sabit kıymet alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="459e5-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="459e5-121">Deftere alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="459e5-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="459e5-122">Hareket tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="459e5-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="459e5-123">Yüzde alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="459e5-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="459e5-124">Günlük adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="459e5-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="459e5-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="459e5-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="459e5-126">Günlük hareketini deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="459e5-126">Post the journal transaction</span></span>
1. <span data-ttu-id="459e5-127">Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="459e5-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="459e5-128">Listede, bölme işlemiyle oluşturulan günlüğü seçin.</span><span class="sxs-lookup"><span data-stu-id="459e5-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="459e5-129">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="459e5-129">Click Lines.</span></span>
    * <span data-ttu-id="459e5-130">Oluşturulan günlük satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="459e5-130">Verify the journal lines created.</span></span>  <span data-ttu-id="459e5-131">Değeri, bölünme işlemi sırasında belirtilen yüzde oranında azaltmak üzere, orijinal kıymet için bir Alım düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="459e5-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="459e5-132">Yeni kıymet için aynı tutarda bir düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="459e5-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="459e5-133">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="459e5-133">Click Post.</span></span>


