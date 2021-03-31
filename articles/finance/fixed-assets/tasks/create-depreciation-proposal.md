---
title: Amortisman önerisi oluşturma
description: Bu konu, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e4852b25ef628cdef6f75f6edf550c539e344a4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227076"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="81f64-103">Amortisman önerisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="81f64-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81f64-104">Bu konu, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="81f64-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="81f64-105">Bu görevde USMF demo şirketi ve muhasebeci rolü kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="81f64-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="81f64-106">Amortisman önerisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="81f64-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="81f64-107">Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Amortisman önerisi oluştur**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="81f64-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="81f64-108">**Günlüğün adı** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="81f64-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="81f64-109">**Bitiş tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="81f64-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="81f64-110">**Aylık amortismanlar**'ı bir günlük satırında özetlemek için Amortismanı özetle'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="81f64-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="81f64-111">Örneğin, Bitiş tarihi değeri 31 Mart 2015 ise, aşağıdaki açıklama oluşturulur: "31 Ocak 2015'ten itibaren amortisman".</span><span class="sxs-lookup"><span data-stu-id="81f64-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="81f64-112">Önerilen günlük satırları üzerindeki **Tarih** alanı 31 Mart 2015'tir.</span><span class="sxs-lookup"><span data-stu-id="81f64-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="81f64-113">Amortisman teklifine, kıymet, kıymet grubu veya diğer ölçütlere göre **Filtre** seçeneği kullanılarak filtre uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="81f64-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="81f64-114">**Sabit kıymetler için alım veya amortisman teklifleri oluşturun** formunu kullanırken amortismanı toplu işler halinde teklif edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81f64-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="81f64-115">Bu, daha fazla sistem kaynağı kullanan büyük teklifler için önerilir.</span><span class="sxs-lookup"><span data-stu-id="81f64-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="81f64-116">Toplu iş seçeneğini belirtirseniz, bu süre içinde diğer görevleri tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="81f64-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="81f64-117">Amortismanı bu yolla teklif ettiğiniz zaman, sabit kıymetlerle ilgili değer modelleri için amortisman hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="81f64-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="81f64-118">**Günlük oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="81f64-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="81f64-119">Amortisman girişlerini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="81f64-119">Review depreciation entries</span></span>
1. <span data-ttu-id="81f64-120">Gezinti bölmesinde **Modüller > Sabit kıymetler > Günlük girişleri> Sabit kıymetler günlüğü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="81f64-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="81f64-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="81f64-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="81f64-122">**Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="81f64-122">Select **Lines**.</span></span>
4. <span data-ttu-id="81f64-123">**Naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="81f64-123">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]