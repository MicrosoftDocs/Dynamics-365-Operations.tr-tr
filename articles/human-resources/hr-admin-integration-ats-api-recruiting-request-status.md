---
title: İşe alma isteği durumu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464658"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="1f089-103">İşe alma isteği durumu</span><span class="sxs-lookup"><span data-stu-id="1f089-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1f089-104">Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="1f089-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="1f089-105">Fiziksel ad: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="1f089-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="1f089-106">Bu sabit listesi, İşe alma İsteği durum değerleri için seçenek kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1f089-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="1f089-107">Değer</span><span class="sxs-lookup"><span data-stu-id="1f089-107">Value</span></span> | <span data-ttu-id="1f089-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="1f089-108">Label</span></span> | <span data-ttu-id="1f089-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f089-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1f089-110">200000000</span><span class="sxs-lookup"><span data-stu-id="1f089-110">200000000</span></span> | <span data-ttu-id="1f089-111">Taslak</span><span class="sxs-lookup"><span data-stu-id="1f089-111">Draft</span></span> | <span data-ttu-id="1f089-112">İstek taslak halindedir ve aktif işe alım için hazır değildir.</span><span class="sxs-lookup"><span data-stu-id="1f089-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="1f089-113">200000001</span><span class="sxs-lookup"><span data-stu-id="1f089-113">200000001</span></span> | <span data-ttu-id="1f089-114">İncelemede</span><span class="sxs-lookup"><span data-stu-id="1f089-114">In Review</span></span> | <span data-ttu-id="1f089-115">İstek gönderildi ve iş akışı tarafından onay için yönlendiriliyor.</span><span class="sxs-lookup"><span data-stu-id="1f089-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="1f089-116">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1f089-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="1f089-117">200000002</span><span class="sxs-lookup"><span data-stu-id="1f089-117">200000002</span></span> | <span data-ttu-id="1f089-118">Bekliyor</span><span class="sxs-lookup"><span data-stu-id="1f089-118">Pending</span></span> | <span data-ttu-id="1f089-119">İstek iş akışı eylemini bekliyor.</span><span class="sxs-lookup"><span data-stu-id="1f089-119">The request is pending workflow action.</span></span> <span data-ttu-id="1f089-120">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1f089-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="1f089-121">200000003</span><span class="sxs-lookup"><span data-stu-id="1f089-121">200000003</span></span> | <span data-ttu-id="1f089-122">İptal Edildi</span><span class="sxs-lookup"><span data-stu-id="1f089-122">Canceled</span></span> | <span data-ttu-id="1f089-123">İstek iptal edildi.</span><span class="sxs-lookup"><span data-stu-id="1f089-123">The request has been canceled.</span></span> <span data-ttu-id="1f089-124">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1f089-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="1f089-125">200000004</span><span class="sxs-lookup"><span data-stu-id="1f089-125">200000004</span></span> | <span data-ttu-id="1f089-126">Reddedildi</span><span class="sxs-lookup"><span data-stu-id="1f089-126">Denied</span></span> | <span data-ttu-id="1f089-127">İstek reddedildi.</span><span class="sxs-lookup"><span data-stu-id="1f089-127">The request has been denied.</span></span> <span data-ttu-id="1f089-128">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1f089-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="1f089-129">200000005</span><span class="sxs-lookup"><span data-stu-id="1f089-129">200000005</span></span> | <span data-ttu-id="1f089-130">Active</span><span class="sxs-lookup"><span data-stu-id="1f089-130">Active</span></span> | <span data-ttu-id="1f089-131">Herhangi bir iş akışı tamamlanıp onaylanır ve istek etkin işe alım için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="1f089-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="1f089-132">200000006</span><span class="sxs-lookup"><span data-stu-id="1f089-132">200000006</span></span> | <span data-ttu-id="1f089-133">Kapatıldı</span><span class="sxs-lookup"><span data-stu-id="1f089-133">Closed</span></span> | <span data-ttu-id="1f089-134">İşe alım isteği kapatıldı.</span><span class="sxs-lookup"><span data-stu-id="1f089-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="1f089-135">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1f089-135">See also</span></span>

[<span data-ttu-id="1f089-136">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="1f089-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="1f089-137">Işe alma isteği için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="1f089-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]