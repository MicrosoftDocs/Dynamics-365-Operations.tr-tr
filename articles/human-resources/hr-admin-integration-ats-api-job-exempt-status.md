---
title: İş muafiyet durumu
description: Bu konu, Dynamics 365 Human Resources için İş Muafiyeti durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798309"
---
# <a name="job-exempt-status"></a><span data-ttu-id="107a8-103">İş muafiyet durumu</span><span class="sxs-lookup"><span data-stu-id="107a8-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="107a8-104">Bu konu, Dynamics 365 Human Resources için İş Muafiyeti durumu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="107a8-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="107a8-105">Fiziksel ad: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="107a8-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="107a8-106">Bu sabit listesi FLSA iş muafiyeti durum değerleri için seçenek kümesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="107a8-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="107a8-107">Bu, varolan cdm_jobexemptstatus seçenek kümesinde verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="107a8-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="107a8-108">Değer</span><span class="sxs-lookup"><span data-stu-id="107a8-108">Value</span></span> | <span data-ttu-id="107a8-109">Etiket</span><span class="sxs-lookup"><span data-stu-id="107a8-109">Label</span></span> | <span data-ttu-id="107a8-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="107a8-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="107a8-111">200000000</span><span class="sxs-lookup"><span data-stu-id="107a8-111">200000000</span></span> | <span data-ttu-id="107a8-112">Muafiyet</span><span class="sxs-lookup"><span data-stu-id="107a8-112">Exempt</span></span> | <span data-ttu-id="107a8-113">Bu işin, FLSA yönergelerine dayalı olarak muafiyet durumu vardır.</span><span class="sxs-lookup"><span data-stu-id="107a8-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="107a8-114">200000001</span><span class="sxs-lookup"><span data-stu-id="107a8-114">200000001</span></span> | <span data-ttu-id="107a8-115">Muaf Değil</span><span class="sxs-lookup"><span data-stu-id="107a8-115">NonExempt</span></span> | <span data-ttu-id="107a8-116">Bu işin, FLSA yönergelerine dayalı olarak muafiyet değil durumu vardır.</span><span class="sxs-lookup"><span data-stu-id="107a8-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="107a8-117">200000002</span><span class="sxs-lookup"><span data-stu-id="107a8-117">200000002</span></span> | <span data-ttu-id="107a8-118">Uygulanmaz</span><span class="sxs-lookup"><span data-stu-id="107a8-118">Does Not Apply</span></span> | <span data-ttu-id="107a8-119">FLSA durum yönergeleri iş için geçerli değil.</span><span class="sxs-lookup"><span data-stu-id="107a8-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="107a8-120">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="107a8-120">See also</span></span>

[<span data-ttu-id="107a8-121">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="107a8-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="107a8-122">Işe alma isteği için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="107a8-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]