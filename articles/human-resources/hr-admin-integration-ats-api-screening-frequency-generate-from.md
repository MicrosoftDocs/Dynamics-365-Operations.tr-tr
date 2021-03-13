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
ms.openlocfilehash: f291e28584dadc465092d99a1354fda793ff7560
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126158"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="2090f-103">Filtreleme sıklığı oluşturma kaynağı</span><span class="sxs-lookup"><span data-stu-id="2090f-103">Screening frequency generate from</span></span>

<span data-ttu-id="2090f-104">Bu konu, Dynamics 365 Human Resources için Filtreleme sıklığı oluşturma kaynağı seçenek kümesini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2090f-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="2090f-105">Fiziksel ad: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="2090f-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="2090f-106">Bu numaralandırma, sonraki gereken filtreleme için hesaplamanın başlangıç tarihini belirlemek için seçenek kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="2090f-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="2090f-107">Değer</span><span class="sxs-lookup"><span data-stu-id="2090f-107">Value</span></span> | <span data-ttu-id="2090f-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="2090f-108">Label</span></span> | <span data-ttu-id="2090f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2090f-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="2090f-110">200000000 Seçilmedi</span><span class="sxs-lookup"><span data-stu-id="2090f-110">200000000 Not selected</span></span> | <span data-ttu-id="2090f-111">Hiçbir değer seçilmedi.</span><span class="sxs-lookup"><span data-stu-id="2090f-111">No value has been selected.</span></span> |
| <span data-ttu-id="2090f-112">200000001 Tamamlanma tarihi</span><span class="sxs-lookup"><span data-stu-id="2090f-112">200000001 Date completed</span></span> | <span data-ttu-id="2090f-113">Hesaplama, tamamlanan son filtreleme tarihinden itibaren gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2090f-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="2090f-114">200000002 İstendiği tarih</span><span class="sxs-lookup"><span data-stu-id="2090f-114">200000002 Date required</span></span> | <span data-ttu-id="2090f-115">Hesaplama, istenen son filtreleme tarihinden itibaren gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2090f-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="2090f-116">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="2090f-116">See also</span></span>

[<span data-ttu-id="2090f-117">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="2090f-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="2090f-118">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="2090f-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
