---
title: İş muafiyet durumu
description: Bu konu, Dynamics 365 Human Resources için İş Muafiyeti durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053863"
---
# <a name="job-exempt-status"></a><span data-ttu-id="9fa75-103">İş muafiyet durumu</span><span class="sxs-lookup"><span data-stu-id="9fa75-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9fa75-104">Bu konu, Dynamics 365 Human Resources için İş Muafiyeti durumu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="9fa75-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9fa75-105">Fiziksel ad: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="9fa75-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="9fa75-106">Bu sabit listesi FLSA iş muafiyeti durum değerleri için seçenek kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fa75-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="9fa75-107">Bu, varolan cdm_jobexemptstatus seçenek kümesinde verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9fa75-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="9fa75-108">Değer</span><span class="sxs-lookup"><span data-stu-id="9fa75-108">Value</span></span> | <span data-ttu-id="9fa75-109">Etiket</span><span class="sxs-lookup"><span data-stu-id="9fa75-109">Label</span></span> | <span data-ttu-id="9fa75-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fa75-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9fa75-111">200000000</span><span class="sxs-lookup"><span data-stu-id="9fa75-111">200000000</span></span> | <span data-ttu-id="9fa75-112">Muafiyet</span><span class="sxs-lookup"><span data-stu-id="9fa75-112">Exempt</span></span> | <span data-ttu-id="9fa75-113">Bu işin, FLSA yönergelerine dayalı olarak muafiyet durumu vardır.</span><span class="sxs-lookup"><span data-stu-id="9fa75-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="9fa75-114">200000001</span><span class="sxs-lookup"><span data-stu-id="9fa75-114">200000001</span></span> | <span data-ttu-id="9fa75-115">Muaf Değil</span><span class="sxs-lookup"><span data-stu-id="9fa75-115">NonExempt</span></span> | <span data-ttu-id="9fa75-116">Bu işin, FLSA yönergelerine dayalı olarak muafiyet değil durumu vardır.</span><span class="sxs-lookup"><span data-stu-id="9fa75-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="9fa75-117">200000002</span><span class="sxs-lookup"><span data-stu-id="9fa75-117">200000002</span></span> | <span data-ttu-id="9fa75-118">Uygulanmaz</span><span class="sxs-lookup"><span data-stu-id="9fa75-118">Does Not Apply</span></span> | <span data-ttu-id="9fa75-119">FLSA durum yönergeleri iş için geçerli değil.</span><span class="sxs-lookup"><span data-stu-id="9fa75-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9fa75-120">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="9fa75-120">See also</span></span>

[<span data-ttu-id="9fa75-121">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="9fa75-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9fa75-122">Işe alma isteği için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="9fa75-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]