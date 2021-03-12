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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b09bbe4d0143aa521ca0a4cf67e86b7165b0f4f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968966"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="a8cfc-103">Tüzel kişilikler arasında sabit kıymet amortismanı hesaplama</span><span class="sxs-lookup"><span data-stu-id="a8cfc-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8cfc-104">Sabit kıymet amortismanı tüzel kişilikler arasında tek bir adımda çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="a8cfc-105">Bu yordam, birden fazla tüzel kişilik için işlemi nasıl ayarlayacağınızı ve çalıştıracağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="a8cfc-106">Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="a8cfc-107">Şirketler arası amortisman çalıştırma günlüklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="a8cfc-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="a8cfc-108">Sabit kıymetler > Kurulum > Sabit kıymet parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="a8cfc-109">Sabit kıymet teklifleri bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="a8cfc-110">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-110">Click Add.</span></span>
4. <span data-ttu-id="a8cfc-111">Deftere nakil katmanı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="a8cfc-112">Günlük adı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="a8cfc-113">Her tüzel kişilik için Sabit kıymet parametreleri sayfasında günlük kurulumunu yineleyin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="a8cfc-114">Amortisman çalıştırma</span><span class="sxs-lookup"><span data-stu-id="a8cfc-114">Depreciation run</span></span>
1. <span data-ttu-id="a8cfc-115">Sabit kıymetler > Günlük girişleri > Amortisman tekifi oluştur'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="a8cfc-116">Deftere nakil katmanı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="a8cfc-117">Günlük adı varsayılan olarak Sabit kıymet parametrelerinden alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="a8cfc-118">Burada geçerli tüzel kişilik için değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="a8cfc-119">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="a8cfc-120">Amortisman çalıştırmaya dahil edilecek tüzel kişilikleri seçin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="a8cfc-121">Yalnızca Sabit kıymet parametreleri sayfasında Sabit kıymet teklifleri için ayarlanan günlükleri bulunan tüzel kişilikler listede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="a8cfc-122">Günlükleri deftere naklet alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="a8cfc-123">Filtreleme alanları, bu amortisman çalıştırma için seçilen tüzel kişiliklerle ilgili tüm sabit kıymetleri, grupları ve defterleri içerir.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="a8cfc-124">Toplu işleme seçeneği varsayılan olarak etkindir.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="a8cfc-125">Bu seçenek etkinleştirildiğinde, amortisman günlüğü oluşturma ve deftere nakletme arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="a8cfc-126">Günlük oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-126">Click Create journal.</span></span>
6. <span data-ttu-id="a8cfc-127">Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a8cfc-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

