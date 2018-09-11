--- 
title: "Sabit kıymet alımları teklif etme"
description: "Bu yordam, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını gösterir."
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 34638f9dc88eb3850f659e4b9741d02418213112
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="b2d50-103">Sabit kıymet alımları teklif etme</span><span class="sxs-lookup"><span data-stu-id="b2d50-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2d50-104">Bu yordam, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2d50-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="b2d50-105">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b2d50-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="b2d50-106">Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b2d50-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="b2d50-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-107">Click New.</span></span>
3. <span data-ttu-id="b2d50-108">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b2d50-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="b2d50-109">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-109">Click Lines.</span></span>
5. <span data-ttu-id="b2d50-110">Teklifler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-110">Click Proposals.</span></span>
6. <span data-ttu-id="b2d50-111">Alım teklifi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="b2d50-112">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-112">Click Filter.</span></span>
8. <span data-ttu-id="b2d50-113">Önceki değerleri temizlemek için sıfırla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="b2d50-114">Sabit kıymet numarası satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="b2d50-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="b2d50-115">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="b2d50-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="b2d50-116">Bu teklifle almak istediğiniz sabit kıymetler için kalan ölçütleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="b2d50-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-117">Click OK.</span></span>
12. <span data-ttu-id="b2d50-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-118">Click OK.</span></span>
    * <span data-ttu-id="b2d50-119">Oluşturulan hareket satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="b2d50-120">Yalnızca, defterde alım tarihi ve alım fiyatı ayarlanmış olan sabit kıymetler alım teklifine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="b2d50-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="b2d50-121">Defterler sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-121">Click the Books tab.</span></span>
14. <span data-ttu-id="b2d50-122">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b2d50-122">Click Post.</span></span>


