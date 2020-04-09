---
title: Tüzel kişilikler arasında sabit kıymet amortismanı hesaplama
description: Sabit kıymet amortismanı tüzel kişilikler arasında tek bir adımda çalıştırılabilir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 074a1b80584050302920a95c20fb547523a4866c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142927"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="e458e-103">Tüzel kişilikler arasında sabit kıymet amortismanı hesaplama</span><span class="sxs-lookup"><span data-stu-id="e458e-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e458e-104">Sabit kıymet amortismanı tüzel kişilikler arasında tek bir adımda çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="e458e-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="e458e-105">Bu yordam, birden fazla tüzel kişilik için işlemi nasıl ayarlayacağınızı ve çalıştıracağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e458e-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="e458e-106">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e458e-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="e458e-107">Şirketler arası amortisman çalıştırma günlüklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="e458e-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="e458e-108">Sabit kıymetler > Kurulum > Sabit kıymet parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e458e-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="e458e-109">Sabit kıymet teklifleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e458e-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="e458e-110">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e458e-110">Click Add.</span></span>
4. <span data-ttu-id="e458e-111">Deftere nakil katmanı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e458e-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="e458e-112">Günlük adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e458e-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="e458e-113">Her tüzel kişilik için Sabit kıymet parametreleri sayfasında günlük kurulumunu yineleyin.</span><span class="sxs-lookup"><span data-stu-id="e458e-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="e458e-114">Amortisman çalıştırma</span><span class="sxs-lookup"><span data-stu-id="e458e-114">Depreciation run</span></span>
1. <span data-ttu-id="e458e-115">Sabit kıymetler > Günlük girişleri > Amortisman tekifi oluştur'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e458e-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="e458e-116">Deftere nakil katmanı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e458e-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="e458e-117">Günlük adı varsayılan olarak Sabit kıymet parametrelerinden alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="e458e-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="e458e-118">Burada geçerli tüzel kişilik için değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e458e-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="e458e-119">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="e458e-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="e458e-120">Amortisman çalıştırmaya dahil edilecek tüzel kişilikleri seçin.</span><span class="sxs-lookup"><span data-stu-id="e458e-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="e458e-121">Yalnızca Sabit kıymet parametreleri sayfasında Sabit kıymet teklifleri için ayarlanan günlükleri bulunan tüzel kişilikler listede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e458e-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="e458e-122">Günlükleri deftere naklet alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e458e-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="e458e-123">Filtreleme alanları, bu amortisman çalıştırma için seçilen tüzel kişiliklerle ilgili tüm sabit kıymetleri, grupları ve defterleri içerir.</span><span class="sxs-lookup"><span data-stu-id="e458e-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="e458e-124">Toplu işleme seçeneği varsayılan olarak etkindir.</span><span class="sxs-lookup"><span data-stu-id="e458e-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="e458e-125">Bu seçenek etkinleştirildiğinde, amortisman günlüğü oluşturma ve deftere nakletme arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="e458e-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="e458e-126">Günlük oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e458e-126">Click Create journal.</span></span>
6. <span data-ttu-id="e458e-127">Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e458e-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

