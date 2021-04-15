---
title: Başvuran tümleştirmesi sonucu
description: Bu konu, Dynamics 365 Human Resources için Başvuran tümleştirme sonucu seçenek kümesini açıklar.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8e41fe485cc70a668d4610ce6eabba5cd16ac86
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795129"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="5a2ea-103">Başvuran tümleştirmesi sonucu</span><span class="sxs-lookup"><span data-stu-id="5a2ea-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="5a2ea-104">Bu konu, Dynamics 365 Human Resources için Başvuran tümleştirme sonucu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="5a2ea-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5a2ea-105">Fiziksel ad: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="5a2ea-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="5a2ea-106">Bu numaralandırma aday kaydı durumunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="5a2ea-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="5a2ea-107">Değer</span><span class="sxs-lookup"><span data-stu-id="5a2ea-107">Value</span></span> | <span data-ttu-id="5a2ea-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="5a2ea-108">Label</span></span> | <span data-ttu-id="5a2ea-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a2ea-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5a2ea-110">200000000</span><span class="sxs-lookup"><span data-stu-id="5a2ea-110">200000000</span></span> | <span data-ttu-id="5a2ea-111">İşlenmedi</span><span class="sxs-lookup"><span data-stu-id="5a2ea-111">Not processed</span></span> | <span data-ttu-id="5a2ea-112">Aday hala değerlendirilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5a2ea-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="5a2ea-113">200000001</span><span class="sxs-lookup"><span data-stu-id="5a2ea-113">200000001</span></span> | <span data-ttu-id="5a2ea-114">İşe alındı</span><span class="sxs-lookup"><span data-stu-id="5a2ea-114">Hired</span></span> | <span data-ttu-id="5a2ea-115">Aday işe alındı.</span><span class="sxs-lookup"><span data-stu-id="5a2ea-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="5a2ea-116">200000002</span><span class="sxs-lookup"><span data-stu-id="5a2ea-116">200000002</span></span> | <span data-ttu-id="5a2ea-117">İşe alınmadı</span><span class="sxs-lookup"><span data-stu-id="5a2ea-117">Not hired</span></span> | <span data-ttu-id="5a2ea-118">Adayı işe almama kararı verildi.</span><span class="sxs-lookup"><span data-stu-id="5a2ea-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="5a2ea-119">200000003</span><span class="sxs-lookup"><span data-stu-id="5a2ea-119">200000003</span></span> | <span data-ttu-id="5a2ea-120">Bırakıldı</span><span class="sxs-lookup"><span data-stu-id="5a2ea-120">Dismissed</span></span> | <span data-ttu-id="5a2ea-121">Aday değerlendirmeden çıkarıldı.</span><span class="sxs-lookup"><span data-stu-id="5a2ea-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5a2ea-122">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="5a2ea-122">See also</span></span>

[<span data-ttu-id="5a2ea-123">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="5a2ea-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="5a2ea-124">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="5a2ea-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]