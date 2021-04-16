---
title: Sabit kıymet alımları teklif etme
description: Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817184"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="dac6a-103">Sabit kıymet alımları teklif etme</span><span class="sxs-lookup"><span data-stu-id="dac6a-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dac6a-104">Bu konu, Sabit kıymetler günlüğündeki alım teklifi kullanılarak bir sabit kıymetin nasıl alındığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="dac6a-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="dac6a-105">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="dac6a-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="dac6a-106">Sabit kıymeti sabit kıymet teklif günlüğü aracılığıyla almak için önce sabit kıymet kaydını oluşturmanız ve sonra kıymet defterinde edinme fiyatını tanımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dac6a-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="dac6a-107">Kıymet alım teklifi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dac6a-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="dac6a-108">Bir kıymet Alım teklifi oluşturmak için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="dac6a-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="dac6a-109">Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="dac6a-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-110">Select **New**.</span></span>
3. <span data-ttu-id="dac6a-111">**Ad** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="dac6a-112">Eylem Bölmesinde, **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="dac6a-113">**Teklifler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="dac6a-114">**Alım teklifi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="dac6a-115">**Filtre**'yi seç.</span><span class="sxs-lookup"><span data-stu-id="dac6a-115">Select **Filter**.</span></span> <span data-ttu-id="dac6a-116">Önceki değerleri temizlemek için **Sıfırla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="dac6a-117">**Sabit varlık numarası** satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="dac6a-118">**Ölçütler** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="dac6a-119">Bu teklifle almak istediğiniz sabit kıymetler için kalan ölçütleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dac6a-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="dac6a-120">Bölmeden çıkmak için, iki kere **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="dac6a-121">İşlem satırlarının oluşturulduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="dac6a-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="dac6a-122">Yalnızca, defterde alım tarihi ve alım fiyatı ayarlanmış olan sabit kıymetler alım teklifine dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="dac6a-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="dac6a-123">Bu sayfada **Defterler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="dac6a-124">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="dac6a-125">Alım teklifine varsayılan mali boyutları dahil et</span><span class="sxs-lookup"><span data-stu-id="dac6a-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="dac6a-126">Alım işlemi, **Sabit kıymetler > Günlük girişleri > Sabit kıymet günlüğü**'ne giderek Excel eklentileri kullanılarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="dac6a-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="dac6a-127">Yeni bir günlük oluşturun ve sayfadaki **satırlar** bölümüne gidin ve Excel simgesini seçin ve sonra bir sabit kıymet günlük satırı seçin.</span><span class="sxs-lookup"><span data-stu-id="dac6a-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="dac6a-128">Sistem, günlük satırlarını temsil eden bir Excel şablonu oluşturur ve açar.</span><span class="sxs-lookup"><span data-stu-id="dac6a-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="dac6a-129">Şablona eklemekte olduğunuz günlük satırları için veri ekleyebilir ve sonra bu bilgileri sisteme geri yayımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dac6a-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="dac6a-130">Seçili kıymet defteri ve Excel şablonunda girilen ilgili sabit kıymetler için varsayılan boyutlar ayarlanmışsa, günlük, Excel'den sisteme yayımlandığında varsayılan finansal boyutlar kıymet defteri ana verilerinden çağrılır.</span><span class="sxs-lookup"><span data-stu-id="dac6a-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="dac6a-131">Sabit kıymet günlüğünü Excel eklentisinden yayımlarken, bir kıymet defterine mali boyutları otomatik olarak eklemek için varsayılan boyutlar önceden ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dac6a-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
