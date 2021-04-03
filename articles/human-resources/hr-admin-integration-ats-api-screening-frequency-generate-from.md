---
title: Filtreleme sıklığı oluşturma kaynağı
description: Bu konu, Dynamics 365 Human Resources için Filtreleme sıklığı oluşturma kaynağı seçenek kümesini açıklamaktadır.
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
ms.openlocfilehash: 238cd5da750d815c904090cc9002e3d1a5d2bcc7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464586"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="bc8fb-103">Filtreleme sıklığı oluşturma kaynağı</span><span class="sxs-lookup"><span data-stu-id="bc8fb-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bc8fb-104">Bu konu, Dynamics 365 Human Resources için Filtreleme sıklığı oluşturma kaynağı seçenek kümesini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="bc8fb-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="bc8fb-105">Fiziksel ad: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="bc8fb-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="bc8fb-106">Bu numaralandırma, sonraki gereken filtreleme için hesaplamanın başlangıç tarihini belirlemek için seçenek kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="bc8fb-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="bc8fb-107">Değer</span><span class="sxs-lookup"><span data-stu-id="bc8fb-107">Value</span></span> | <span data-ttu-id="bc8fb-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="bc8fb-108">Label</span></span> | <span data-ttu-id="bc8fb-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc8fb-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="bc8fb-110">200000000 Seçilmedi</span><span class="sxs-lookup"><span data-stu-id="bc8fb-110">200000000 Not selected</span></span> | <span data-ttu-id="bc8fb-111">Hiçbir değer seçilmedi.</span><span class="sxs-lookup"><span data-stu-id="bc8fb-111">No value has been selected.</span></span> |
| <span data-ttu-id="bc8fb-112">200000001 Tamamlanma tarihi</span><span class="sxs-lookup"><span data-stu-id="bc8fb-112">200000001 Date completed</span></span> | <span data-ttu-id="bc8fb-113">Hesaplama, tamamlanan son filtreleme tarihinden itibaren gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bc8fb-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="bc8fb-114">200000002 İstendiği tarih</span><span class="sxs-lookup"><span data-stu-id="bc8fb-114">200000002 Date required</span></span> | <span data-ttu-id="bc8fb-115">Hesaplama, istenen son filtreleme tarihinden itibaren gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="bc8fb-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="bc8fb-116">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="bc8fb-116">See also</span></span>

[<span data-ttu-id="bc8fb-117">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="bc8fb-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="bc8fb-118">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="bc8fb-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]