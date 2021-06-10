---
title: Başvuran tümleştirmesi sonucu
description: Bu konu, Dynamics 365 Human Resources için Başvuran tümleştirme sonucu seçenek kümesini açıklar.
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
ms.openlocfilehash: 8bef974abff18d7c07ecd679b7e01b31ea1459c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053911"
---
# <a name="applicant-integration-result"></a><span data-ttu-id="aa83b-103">Başvuran tümleştirmesi sonucu</span><span class="sxs-lookup"><span data-stu-id="aa83b-103">Applicant integration result</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="aa83b-104">Bu konu, Dynamics 365 Human Resources için Başvuran tümleştirme sonucu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="aa83b-104">This topic describes the Applicant integration result option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="aa83b-105">Fiziksel ad: mshr_hcmapplicantintegrationresult</span><span class="sxs-lookup"><span data-stu-id="aa83b-105">Physical name: mshr_hcmapplicantintegrationresult</span></span>

<span data-ttu-id="aa83b-106">Bu numaralandırma aday kaydı durumunu sağlar.</span><span class="sxs-lookup"><span data-stu-id="aa83b-106">This enumeration provides status for a candidate record.</span></span>

| <span data-ttu-id="aa83b-107">Değer</span><span class="sxs-lookup"><span data-stu-id="aa83b-107">Value</span></span> | <span data-ttu-id="aa83b-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="aa83b-108">Label</span></span> | <span data-ttu-id="aa83b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa83b-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="aa83b-110">200000000</span><span class="sxs-lookup"><span data-stu-id="aa83b-110">200000000</span></span> | <span data-ttu-id="aa83b-111">İşlenmedi</span><span class="sxs-lookup"><span data-stu-id="aa83b-111">Not processed</span></span> | <span data-ttu-id="aa83b-112">Aday hala değerlendirilmektedir.</span><span class="sxs-lookup"><span data-stu-id="aa83b-112">Candidate is still under consideration.</span></span> |
| <span data-ttu-id="aa83b-113">200000001</span><span class="sxs-lookup"><span data-stu-id="aa83b-113">200000001</span></span> | <span data-ttu-id="aa83b-114">İşe alındı</span><span class="sxs-lookup"><span data-stu-id="aa83b-114">Hired</span></span> | <span data-ttu-id="aa83b-115">Aday işe alındı.</span><span class="sxs-lookup"><span data-stu-id="aa83b-115">The candidate has been hired.</span></span> |
| <span data-ttu-id="aa83b-116">200000002</span><span class="sxs-lookup"><span data-stu-id="aa83b-116">200000002</span></span> | <span data-ttu-id="aa83b-117">İşe alınmadı</span><span class="sxs-lookup"><span data-stu-id="aa83b-117">Not hired</span></span> | <span data-ttu-id="aa83b-118">Adayı işe almama kararı verildi.</span><span class="sxs-lookup"><span data-stu-id="aa83b-118">Decision was made to not hire the candidate.</span></span> |
| <span data-ttu-id="aa83b-119">200000003</span><span class="sxs-lookup"><span data-stu-id="aa83b-119">200000003</span></span> | <span data-ttu-id="aa83b-120">Bırakıldı</span><span class="sxs-lookup"><span data-stu-id="aa83b-120">Dismissed</span></span> | <span data-ttu-id="aa83b-121">Aday değerlendirmeden çıkarıldı.</span><span class="sxs-lookup"><span data-stu-id="aa83b-121">The candidate was dismissed from consideration.</span></span> |

## <a name="see-also"></a><span data-ttu-id="aa83b-122">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="aa83b-122">See also</span></span>

[<span data-ttu-id="aa83b-123">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="aa83b-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="aa83b-124">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="aa83b-124">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]