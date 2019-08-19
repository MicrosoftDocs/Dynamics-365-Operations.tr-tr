---
title: Sabit kıymet alımları teklif etme
description: Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
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
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839917"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="53a97-103">Sabit kıymet alımları teklif etme</span><span class="sxs-lookup"><span data-stu-id="53a97-103">Propose fixed asset acquisitions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53a97-104">Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="53a97-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="53a97-105">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="53a97-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="53a97-106">Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="53a97-106">In the Navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="53a97-107">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-107">Select **New**.</span></span>
3. <span data-ttu-id="53a97-108">**Ad** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-108">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="53a97-109">Eylem bölmesinde, **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-109">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="53a97-110">**Teklifler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-110">Select **Proposals**.</span></span>
6. <span data-ttu-id="53a97-111">**Alım teklifi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-111">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="53a97-112">**Filtre**'yi seç.</span><span class="sxs-lookup"><span data-stu-id="53a97-112">Select **Filter**.</span></span> <span data-ttu-id="53a97-113">Önceki değerleri temizlemek için **Sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-113">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="53a97-114">**Sabit varlık numarası** satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-114">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="53a97-115">**Ölçütler** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="53a97-116">Bu teklifle almak istediğiniz sabit kıymetler için kalan ölçütleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="53a97-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="53a97-117">Bölmeden çıkmak için, iki kere **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-117">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="53a97-118">Oluşturulan hareket satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="53a97-118">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="53a97-119">Yalnızca, defterde alım tarihi ve alım fiyatı ayarlanmış olan sabit kıymetler alım teklifine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="53a97-119">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="53a97-120">Bu sayfada **Defterler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-120">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="53a97-121">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="53a97-121">Select **Post**.</span></span>

