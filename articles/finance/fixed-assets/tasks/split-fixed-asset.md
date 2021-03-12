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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75938e6fdf5fd8f10ac9719fc449a586c08d06b8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975953"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="3d5e3-103">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="3d5e3-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3d5e3-104">Bu konu bir kıymet defteri yüzdesini yeni bir kıymet defterine bölmeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="3d5e3-105">Kılavuzda Muhasebeci rolü ve USMF demo verileri kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="3d5e3-106">Yeni bir sabit kıymet oluştur</span><span class="sxs-lookup"><span data-stu-id="3d5e3-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="3d5e3-107">Gezinti bölmesinde **Modüller \> Sabit kıymetler \> Sabit kıymetler \> Sabit kıymetler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="3d5e3-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-108">Select **New**.</span></span>
3. <span data-ttu-id="3d5e3-109">**Sabit kıymet grubu** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="3d5e3-110">Sabit kıymet numarasını, bölme işleminde daha sonra kullanmak üzere not alın.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="3d5e3-111">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="3d5e3-112">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="3d5e3-113">Sabit kıymeti bölme</span><span class="sxs-lookup"><span data-stu-id="3d5e3-113">Split a fixed asset</span></span>

<span data-ttu-id="3d5e3-114">Tam amortismana tabi bir kıymet bölünmeden önce, kıymet defteri durumunun elle **Kapalı**'dan **Açık**'a değiştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="3d5e3-115">Bu adım gereklidir, çünkü kıymetle ilgili işlemleri deftere nakletmeniz gerekiyorsa (örneğin, elden çıkarma satışı için) Defter durumunun **Açık** olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="3d5e3-116">**Genel muhasebe parametreleri** sayfasının **Genel** sekmesinde **Tek bir fiş içinde birden fazla harekete izin ver** parametresini de açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="3d5e3-117">Varlık defter durumu değiştirildikten ve bir fiş içinde birden fazla harekete izin verildikten sonra varlığı bölmek için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="3d5e3-118">Listede, bölünecek sabit kıymetin bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="3d5e3-119">**Defterler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-119">Select **Books**.</span></span> <span data-ttu-id="3d5e3-120">Yeni kıymete bölünecek defteri seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="3d5e3-121">**İşlevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-121">Select **Functions**.</span></span>
4. <span data-ttu-id="3d5e3-122">**Sabit kıymet böl**'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="3d5e3-123">**Sabit kıymet** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="3d5e3-124">**Deftere** alanında, aramayı açmak için açılır menü düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3d5e3-125">**Hareket tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="3d5e3-126">**Yüzde** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="3d5e3-127">**Günlük adı** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="3d5e3-128">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="3d5e3-129">Günlük hareketini deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="3d5e3-129">Post the journal transaction</span></span>

1. <span data-ttu-id="3d5e3-130">Gezinti bölmesinde **Modüller \> Sabit kıymetler \> Günlük girişleri \> Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="3d5e3-131">Listede, bölme işlemiyle oluşturulan günlüğü seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="3d5e3-132">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-132">Select **Lines**.</span></span>

    - <span data-ttu-id="3d5e3-133">Oluşturulan günlük satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="3d5e3-134">Değeri, bölünme işlemi sırasında belirtilen yüzde oranında azaltmak üzere, orijinal kıymet için bir Alım düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="3d5e3-135">Yeni kıymet için aynı tutarda bir düzeltme hareketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="3d5e3-136">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3d5e3-136">Select **Post**.</span></span>
