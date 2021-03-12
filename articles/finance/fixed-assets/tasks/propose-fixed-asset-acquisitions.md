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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9259c9bbf52c1c09a7092db6976fc3fabca6601
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990451"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="ddde9-103">Sabit kıymet alımları teklif etme</span><span class="sxs-lookup"><span data-stu-id="ddde9-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ddde9-104">Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="ddde9-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="ddde9-105">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ddde9-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="ddde9-106">Sabit kıymeti sabit kıymet teklif günlüğü aracılığıyla almak için önce sabit kıymet kaydını oluşturmanız ve sonra kıymet defterinde edinme fiyatını tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ddde9-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

1. <span data-ttu-id="ddde9-107">Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="ddde9-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-108">Select **New**.</span></span>
3. <span data-ttu-id="ddde9-109">**Ad** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="ddde9-110">Eylem bölmesinde, **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-110">In the action pane, select **Lines**.</span></span>
5. <span data-ttu-id="ddde9-111">**Teklifler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-111">Select **Proposals**.</span></span>
6. <span data-ttu-id="ddde9-112">**Alım teklifi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-112">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="ddde9-113">**Filtre**'yi seç.</span><span class="sxs-lookup"><span data-stu-id="ddde9-113">Select **Filter**.</span></span> <span data-ttu-id="ddde9-114">Önceki değerleri temizlemek için **Sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-114">Select **Reset** to clear out previous values.</span></span>
8. <span data-ttu-id="ddde9-115">**Sabit varlık numarası** satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-115">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="ddde9-116">**Ölçütler** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-116">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="ddde9-117">Bu teklifle almak istediğiniz sabit kıymetler için kalan ölçütleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ddde9-117">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="ddde9-118">Bölmeden çıkmak için, iki kere **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-118">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="ddde9-119">Oluşturulan hareket satırlarını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ddde9-119">Verify the transaction lines created.</span></span>  
- <span data-ttu-id="ddde9-120">Yalnızca, defterde alım tarihi ve alım fiyatı ayarlanmış olan sabit kıymetler alım teklifine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="ddde9-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="ddde9-121">Bu sayfada **Defterler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-121">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="ddde9-122">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ddde9-122">Select **Post**.</span></span>
