---
title: Amortisman önerisi oluştur
description: Bu prosedür, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "361303"
---
# <a name="create-depreciation-proposal"></a><span data-ttu-id="fda98-103">Amortisman önerisi oluştur</span><span class="sxs-lookup"><span data-stu-id="fda98-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fda98-104">Bu prosedür, toplu amortisman tekliflerinin nasıl işlediğini ve sabit kıymetler için amortisman teklifinin nasıl yapıldığını açıklar.</span><span class="sxs-lookup"><span data-stu-id="fda98-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="fda98-105">Bu görevde USMF demo şirketi ve muhasebeci rolü kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="fda98-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="fda98-106">Amortisman önerisi oluştur</span><span class="sxs-lookup"><span data-stu-id="fda98-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="fda98-107">Sabit kıymetler > Günlük girişleri > Amortisman tekifi oluştur'a gidin.</span><span class="sxs-lookup"><span data-stu-id="fda98-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="fda98-108">Günlüğün adı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="fda98-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="fda98-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda98-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="fda98-110">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="fda98-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="fda98-111">Aylık amortismanları bir günlük satırında özetlemek için Amortismanı özetle'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fda98-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="fda98-112">Örneğin, Bitiş tarihi değeri 31 Mart 2015 ise, aşağıdaki açıklama oluşturulur: "31 Ocak 2015'ten itibaren amortisman".</span><span class="sxs-lookup"><span data-stu-id="fda98-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="fda98-113">Önerilen günlük satırları üzerindeki Tarih alanı 31 Mart 2015'tir.</span><span class="sxs-lookup"><span data-stu-id="fda98-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="fda98-114">Amortisman teklifine, kıymet, kıymet grubu veya diğer ölçütlere göre Filtre seçeneği kullanılarak filtre uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="fda98-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="fda98-115">Sabit kıymetler için alım veya amortisman teklifleri oluşturun formunu kullanırken amortismanı toplu işler halinde teklif edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda98-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="fda98-116">Bu, daha fazla sistem kaynağı kullanan büyük teklifler için önerilir.</span><span class="sxs-lookup"><span data-stu-id="fda98-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="fda98-117">Toplu iş seçeneğini belirtirseniz, bu süre içinde diğer görevleri tamamlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fda98-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="fda98-118">Amortismanı bu yolla teklif ettiğiniz zaman, sabit kıymetlerle ilgili değer modelleri için amortisman hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="fda98-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="fda98-119">Günlük oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda98-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="fda98-120">Amortisman girişlerini gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="fda98-120">Review depreciation entries</span></span>
1. <span data-ttu-id="fda98-121">Sabit kıymetler > Günlük girişler > Sabit kıymetler günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="fda98-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="fda98-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="fda98-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fda98-123">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda98-123">Click Lines.</span></span>
4. <span data-ttu-id="fda98-124">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fda98-124">Click Post.</span></span>

