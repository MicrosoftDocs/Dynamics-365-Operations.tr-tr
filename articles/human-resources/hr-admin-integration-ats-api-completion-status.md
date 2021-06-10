---
title: Tamamlanma durumu
description: Bu konu, Dynamics 365 Human Resources için Tamamlanma durumu seçenek kümesini açıklar.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 54ad5cc8f5f18d57b6713304cceb985acfdc93d1
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055376"
---
# <a name="completion-status"></a><span data-ttu-id="49de4-103">Tamamlanma durumu</span><span class="sxs-lookup"><span data-stu-id="49de4-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="49de4-104">Bu konu, Dynamics 365 Human Resources için Tamamlanma durumu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="49de4-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="49de4-105">Fiziksel ad: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="49de4-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="49de4-106">Bu numaralandırma, aday filtreleme için durum değerleri seçenek kümesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="49de4-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="49de4-107">Değer</span><span class="sxs-lookup"><span data-stu-id="49de4-107">Value</span></span> | <span data-ttu-id="49de4-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="49de4-108">Label</span></span> | <span data-ttu-id="49de4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="49de4-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="49de4-110">200000000</span><span class="sxs-lookup"><span data-stu-id="49de4-110">200000000</span></span> | <span data-ttu-id="49de4-111">Tamamlanmadı</span><span class="sxs-lookup"><span data-stu-id="49de4-111">Not Complete</span></span> | <span data-ttu-id="49de4-112">Aday henüz filtreleme işlemini tamamlamadı.</span><span class="sxs-lookup"><span data-stu-id="49de4-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="49de4-113">200000001</span><span class="sxs-lookup"><span data-stu-id="49de4-113">200000001</span></span> | <span data-ttu-id="49de4-114">Geçiş</span><span class="sxs-lookup"><span data-stu-id="49de4-114">Pass</span></span> | <span data-ttu-id="49de4-115">Aday filtreleme aşamasını geçti.</span><span class="sxs-lookup"><span data-stu-id="49de4-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="49de4-116">200000002</span><span class="sxs-lookup"><span data-stu-id="49de4-116">200000002</span></span> | <span data-ttu-id="49de4-117">Başarısız</span><span class="sxs-lookup"><span data-stu-id="49de4-117">Fail</span></span> | <span data-ttu-id="49de4-118">Aday filtreleme aşamasını geçemedi.</span><span class="sxs-lookup"><span data-stu-id="49de4-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="49de4-119">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="49de4-119">See also</span></span>

[<span data-ttu-id="49de4-120">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="49de4-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="49de4-121">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="49de4-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]