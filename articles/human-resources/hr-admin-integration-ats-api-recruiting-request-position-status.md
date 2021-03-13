---
title: İşe alma isteği pozisyon durumu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği pozisyon durumu seçenek kümesini açıklar.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126062"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="22262-103">İşe alma isteği pozisyon durumu</span><span class="sxs-lookup"><span data-stu-id="22262-103">Recruiting request position status</span></span>

<span data-ttu-id="22262-104">Bu konu, Dynamics 365 Human Resources için İşe alma isteği pozisyon durumu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="22262-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="22262-105">Fiziksel ad: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="22262-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="22262-106">Bu numaralandırma, RecruitingRequestPosition varlığındaki her bir işe alma isteği için durum değerlerine yönelik seçenek kümesini sunar.</span><span class="sxs-lookup"><span data-stu-id="22262-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="22262-107">Değer</span><span class="sxs-lookup"><span data-stu-id="22262-107">Value</span></span> | <span data-ttu-id="22262-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="22262-108">Label</span></span> | <span data-ttu-id="22262-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="22262-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="22262-110">200000000</span><span class="sxs-lookup"><span data-stu-id="22262-110">200000000</span></span> | <span data-ttu-id="22262-111">Açık</span><span class="sxs-lookup"><span data-stu-id="22262-111">Open</span></span> | <span data-ttu-id="22262-112">İşe alma isteğindeki konum işe alma için açıktır.</span><span class="sxs-lookup"><span data-stu-id="22262-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="22262-113">Bu, pozisyon için geçerli olarak etkin pozisyon ataması bulunmadığını göstermez.</span><span class="sxs-lookup"><span data-stu-id="22262-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="22262-114">İşe alma sırasında pozisyonda çalışan olabilir.</span><span class="sxs-lookup"><span data-stu-id="22262-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="22262-115">Yalnızca işe alma isteği bağlamında, pozisyonun işe alma için kullanılabilir olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="22262-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="22262-116">200000001</span><span class="sxs-lookup"><span data-stu-id="22262-116">200000001</span></span> | <span data-ttu-id="22262-117">Dolu</span><span class="sxs-lookup"><span data-stu-id="22262-117">Filled</span></span> | <span data-ttu-id="22262-118">Pozisyonun atanması için bir çalışan seçildi.</span><span class="sxs-lookup"><span data-stu-id="22262-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="22262-119">200000002</span><span class="sxs-lookup"><span data-stu-id="22262-119">200000002</span></span> | <span data-ttu-id="22262-120">İptal Edildi</span><span class="sxs-lookup"><span data-stu-id="22262-120">Canceled</span></span> | <span data-ttu-id="22262-121">Bu pozisyon için işe alınmış istek iptal edildi.</span><span class="sxs-lookup"><span data-stu-id="22262-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="22262-122">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="22262-122">See also</span></span>

[<span data-ttu-id="22262-123">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="22262-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="22262-124">Işe alma isteği için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="22262-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
