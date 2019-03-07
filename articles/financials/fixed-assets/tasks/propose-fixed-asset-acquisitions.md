---
title: Sabit kıymet alımları teklif etme
description: Bu yordam, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını gösterir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1891206bb266b126eccfa789b8c8062c9bfa688b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "350654"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="68dc9-103">Sabit kıymet alımları teklif etme</span><span class="sxs-lookup"><span data-stu-id="68dc9-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="68dc9-104">Bu yordam, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68dc9-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="68dc9-105">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="68dc9-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="68dc9-106">Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="68dc9-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="68dc9-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-107">Click New.</span></span>
3. <span data-ttu-id="68dc9-108">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="68dc9-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="68dc9-109">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-109">Click Lines.</span></span>
5. <span data-ttu-id="68dc9-110">Teklifler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-110">Click Proposals.</span></span>
6. <span data-ttu-id="68dc9-111">Alım teklifi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="68dc9-112">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-112">Click Filter.</span></span>
8. <span data-ttu-id="68dc9-113">Önceki değerleri temizlemek için sıfırla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="68dc9-114">Sabit kıymet numarası satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="68dc9-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="68dc9-115">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="68dc9-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="68dc9-116">Bu teklifle almak istediğiniz sabit kıymetler için kalan ölçütleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="68dc9-117">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-117">Click OK.</span></span>
12. <span data-ttu-id="68dc9-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-118">Click OK.</span></span>
    * <span data-ttu-id="68dc9-119">Oluşturulan hareket satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="68dc9-120">Yalnızca, defterde alım tarihi ve alım fiyatı ayarlanmış olan sabit kıymetler alım teklifine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="68dc9-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="68dc9-121">Defterler sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-121">Click the Books tab.</span></span>
14. <span data-ttu-id="68dc9-122">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="68dc9-122">Click Post.</span></span>

