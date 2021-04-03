---
title: Tamamlanma durumu
description: Bu konu, Dynamics 365 Human Resources için Tamamlanma durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: d8ea90785f303301a21a4ac799578b08cabd0e3d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468215"
---
# <a name="completion-status"></a><span data-ttu-id="af90c-103">Tamamlanma durumu</span><span class="sxs-lookup"><span data-stu-id="af90c-103">Completion status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="af90c-104">Bu konu, Dynamics 365 Human Resources için Tamamlanma durumu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="af90c-104">This topic describes the Completion status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="af90c-105">Fiziksel ad: mshr_hcmcompletionstatus</span><span class="sxs-lookup"><span data-stu-id="af90c-105">Physical name: mshr_hcmcompletionstatus</span></span>

<span data-ttu-id="af90c-106">Bu numaralandırma, aday filtreleme için durum değerleri seçenek kümesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="af90c-106">This enumeration provides the option set of status values for candidate screenings.</span></span> 

| <span data-ttu-id="af90c-107">Değer</span><span class="sxs-lookup"><span data-stu-id="af90c-107">Value</span></span> | <span data-ttu-id="af90c-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="af90c-108">Label</span></span> | <span data-ttu-id="af90c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="af90c-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="af90c-110">200000000</span><span class="sxs-lookup"><span data-stu-id="af90c-110">200000000</span></span> | <span data-ttu-id="af90c-111">Tamamlanmadı</span><span class="sxs-lookup"><span data-stu-id="af90c-111">Not Complete</span></span> | <span data-ttu-id="af90c-112">Aday henüz filtreleme işlemini tamamlamadı.</span><span class="sxs-lookup"><span data-stu-id="af90c-112">The candidate has not yet completed the screening.</span></span> |
| <span data-ttu-id="af90c-113">200000001</span><span class="sxs-lookup"><span data-stu-id="af90c-113">200000001</span></span> | <span data-ttu-id="af90c-114">Geçiş</span><span class="sxs-lookup"><span data-stu-id="af90c-114">Pass</span></span> | <span data-ttu-id="af90c-115">Aday filtreleme aşamasını geçti.</span><span class="sxs-lookup"><span data-stu-id="af90c-115">The candidate has passed the screening.</span></span> |
| <span data-ttu-id="af90c-116">200000002</span><span class="sxs-lookup"><span data-stu-id="af90c-116">200000002</span></span> | <span data-ttu-id="af90c-117">Başarısız</span><span class="sxs-lookup"><span data-stu-id="af90c-117">Fail</span></span> | <span data-ttu-id="af90c-118">Aday filtreleme aşamasını geçemedi.</span><span class="sxs-lookup"><span data-stu-id="af90c-118">The candidate has failed the screening.</span></span> |

## <a name="see-also"></a><span data-ttu-id="af90c-119">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="af90c-119">See also</span></span>

[<span data-ttu-id="af90c-120">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="af90c-120">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="af90c-121">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="af90c-121">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]