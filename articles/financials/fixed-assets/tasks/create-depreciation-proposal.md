---
title: "Amortisman önerisi oluştur"
description: "Bu prosedür, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---

# <a name="create-depreciation-proposal"></a><span data-ttu-id="7bfd7-103">Amortisman önerisi oluştur</span><span class="sxs-lookup"><span data-stu-id="7bfd7-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7bfd7-104">Bu prosedür, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="7bfd7-105">Bu görevde USMF demo şirketi ve muhasebeci rolü kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="7bfd7-106">Amortisman önerisi oluştur</span><span class="sxs-lookup"><span data-stu-id="7bfd7-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="7bfd7-107">Sabit kıymetler > Günlük girişleri > Amortisman tekifi oluştur'a gidin.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="7bfd7-108">Günlüğün adı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7bfd7-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7bfd7-110">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="7bfd7-111">Aylık amortismanları bir günlük satırında özetlemek için Amortismanı özetle'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="7bfd7-112">Örneğin, Bitiş tarihi değeri 31 Mart 2015 ise, aşağıdaki açıklama oluşturulur: "31 Ocak 2015'ten itibaren amortisman".</span><span class="sxs-lookup"><span data-stu-id="7bfd7-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="7bfd7-113">Önerilen günlük satırları üzerindeki Tarih alanı 31 Mart 2015'tir.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="7bfd7-114">Amortisman teklifine, kıymet, kıymet grubu veya diğer ölçütlere göre Filtre seçeneği kullanılarak filtre uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="7bfd7-115">Sabit kıymetler için alım veya amortisman teklifleri oluşturun formunu kullanırken amortismanı toplu işler halinde teklif edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="7bfd7-116">Bu, daha fazla sistem kaynağı kullanan büyük teklifler için önerilir.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="7bfd7-117">Toplu iş seçeneğini belirtirseniz, bu süre içinde diğer görevleri tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="7bfd7-118">Amortismanı bu yolla teklif ettiğiniz zaman, sabit kıymetlerle ilgili değer modelleri için amortisman hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="7bfd7-119">Günlük oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="7bfd7-120">Amortisman girişlerini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="7bfd7-120">Review depreciation entries</span></span>
1. <span data-ttu-id="7bfd7-121">Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="7bfd7-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7bfd7-123">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-123">Click Lines.</span></span>
4. <span data-ttu-id="7bfd7-124">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7bfd7-124">Click Post.</span></span>


