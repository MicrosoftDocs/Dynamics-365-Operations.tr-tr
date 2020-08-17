---
title: Sabit kıymet alımları teklif etme
description: Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar.
author: saraschi2
manager: AnnBe
ms.date: 07/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0997af638c141661afb677e2407a90a883168aed
ms.sourcegitcommit: a8201e0b9033c2afc2b1702b0337facaf7ad4b92
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/28/2020
ms.locfileid: "3628897"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="21d19-103">Sabit kıymet alımları teklif etme</span><span class="sxs-lookup"><span data-stu-id="21d19-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21d19-104">Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="21d19-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="21d19-105">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="21d19-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="21d19-106">Sabit kıymeti sabit kıymet teklif günlüğü aracılığıyla almak için önce sabit kıymet kaydını oluşturmanız ve sonra kıymet defterinde edinme fiyatını tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="21d19-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="21d19-107">Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="21d19-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="21d19-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-108">Select **New**.</span></span>
3. <span data-ttu-id="21d19-109">**Ad** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="21d19-110">Eylem bölmesinde, **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="21d19-111">**Teklifler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="21d19-112">**Alım teklifi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="21d19-113">**Filtre**'yi seç.</span><span class="sxs-lookup"><span data-stu-id="21d19-113">Select **Filter**.</span></span> <span data-ttu-id="21d19-114">Önceki değerleri temizlemek için **Sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="21d19-115">**Sabit varlık numarası** satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="21d19-116">**Ölçütler** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="21d19-117">Bu teklifle almak istediğiniz sabit kıymetler için kalan ölçütleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="21d19-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="21d19-118">Bölmeden çıkmak için, iki kere **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="21d19-119">Oluşturulan hareket satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="21d19-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="21d19-120">Yalnızca, defterde alım tarihi ve alım fiyatı ayarlanmış olan sabit kıymetler alım teklifine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="21d19-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="21d19-121">Bu sayfada **Defterler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="21d19-122">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="21d19-122">Select **Post**.</span></span>
