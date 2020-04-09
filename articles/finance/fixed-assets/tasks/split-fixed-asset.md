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
ms.openlocfilehash: 85ccf187e77faf338ac29452d823c3652b806a21
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138127"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="a4296-103">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="a4296-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4296-104">Bu konu bir kıymet defteri yüzdesini yeni bir kıymet defterine bölmeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="a4296-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="a4296-105">Kılavuzda Muhasebeci rolü ve USMF demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a4296-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="a4296-106">Yeni bir sabit kıymet oluştur</span><span class="sxs-lookup"><span data-stu-id="a4296-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="a4296-107">Gezinti bölmesinde **Modüller > Sabit kıymetler > Sabit kıymetler > Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a4296-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="a4296-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-108">Select **New**.</span></span>
3. <span data-ttu-id="a4296-109">**Sabit kıymet grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="a4296-110">Sabit kıymet numarasını, bölme işleminde daha sonra kullanmak üzere not alın.</span><span class="sxs-lookup"><span data-stu-id="a4296-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="a4296-111">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a4296-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="a4296-112">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4296-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="a4296-113">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="a4296-113">Split a fixed asset</span></span>
1. <span data-ttu-id="a4296-114">Listede, bölünecek sabit kıymetin bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="a4296-115">**Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-115">Select **Books**.</span></span> <span data-ttu-id="a4296-116">Yeni kıymete bölünecek defteri seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="a4296-117">**İşlevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-117">Select **Functions**.</span></span>
4. <span data-ttu-id="a4296-118">**Sabit kıymet böl**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="a4296-119">**Sabit kıymet** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="a4296-120">**Deftere** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a4296-121">**Hareket tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a4296-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="a4296-122">**Yüzde** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a4296-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="a4296-123">**Günlük adı** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="a4296-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="a4296-125">Günlük hareketini deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="a4296-125">Post the journal transaction</span></span>
1. <span data-ttu-id="a4296-126">Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a4296-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="a4296-127">Listede, bölme işlemiyle oluşturulan günlüğü seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="a4296-128">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-128">Select **Lines**.</span></span>

    - <span data-ttu-id="a4296-129">Oluşturulan günlük satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a4296-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="a4296-130">Değeri, bölünme işlemi sırasında belirtilen yüzde oranında azaltmak üzere, orijinal kıymet için bir Alım düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a4296-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="a4296-131">Yeni kıymet için aynı tutarda bir düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a4296-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="a4296-132">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4296-132">Select **Post**.</span></span>

