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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125966"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="c4be5-103">İşe alma isteği durumu</span><span class="sxs-lookup"><span data-stu-id="c4be5-103">Recruiting request status</span></span>

<span data-ttu-id="c4be5-104">Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="c4be5-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c4be5-105">Fiziksel ad: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="c4be5-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="c4be5-106">Bu sabit listesi, İşe alma İsteği durum değerleri için seçenek kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="c4be5-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="c4be5-107">Değer</span><span class="sxs-lookup"><span data-stu-id="c4be5-107">Value</span></span> | <span data-ttu-id="c4be5-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="c4be5-108">Label</span></span> | <span data-ttu-id="c4be5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4be5-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c4be5-110">200000000</span><span class="sxs-lookup"><span data-stu-id="c4be5-110">200000000</span></span> | <span data-ttu-id="c4be5-111">Taslak</span><span class="sxs-lookup"><span data-stu-id="c4be5-111">Draft</span></span> | <span data-ttu-id="c4be5-112">İstek taslak halindedir ve aktif işe alım için hazır değildir.</span><span class="sxs-lookup"><span data-stu-id="c4be5-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="c4be5-113">200000001</span><span class="sxs-lookup"><span data-stu-id="c4be5-113">200000001</span></span> | <span data-ttu-id="c4be5-114">İncelemede</span><span class="sxs-lookup"><span data-stu-id="c4be5-114">In Review</span></span> | <span data-ttu-id="c4be5-115">İstek gönderildi ve iş akışı tarafından onay için yönlendiriliyor.</span><span class="sxs-lookup"><span data-stu-id="c4be5-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="c4be5-116">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c4be5-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c4be5-117">200000002</span><span class="sxs-lookup"><span data-stu-id="c4be5-117">200000002</span></span> | <span data-ttu-id="c4be5-118">Bekliyor</span><span class="sxs-lookup"><span data-stu-id="c4be5-118">Pending</span></span> | <span data-ttu-id="c4be5-119">İstek iş akışı eylemini bekliyor.</span><span class="sxs-lookup"><span data-stu-id="c4be5-119">The request is pending workflow action.</span></span> <span data-ttu-id="c4be5-120">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c4be5-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c4be5-121">200000003</span><span class="sxs-lookup"><span data-stu-id="c4be5-121">200000003</span></span> | <span data-ttu-id="c4be5-122">İptal Edildi</span><span class="sxs-lookup"><span data-stu-id="c4be5-122">Canceled</span></span> | <span data-ttu-id="c4be5-123">İstek iptal edildi.</span><span class="sxs-lookup"><span data-stu-id="c4be5-123">The request has been canceled.</span></span> <span data-ttu-id="c4be5-124">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c4be5-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c4be5-125">200000004</span><span class="sxs-lookup"><span data-stu-id="c4be5-125">200000004</span></span> | <span data-ttu-id="c4be5-126">Reddedildi</span><span class="sxs-lookup"><span data-stu-id="c4be5-126">Denied</span></span> | <span data-ttu-id="c4be5-127">İstek reddedildi.</span><span class="sxs-lookup"><span data-stu-id="c4be5-127">The request has been denied.</span></span> <span data-ttu-id="c4be5-128">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c4be5-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="c4be5-129">200000005</span><span class="sxs-lookup"><span data-stu-id="c4be5-129">200000005</span></span> | <span data-ttu-id="c4be5-130">Active</span><span class="sxs-lookup"><span data-stu-id="c4be5-130">Active</span></span> | <span data-ttu-id="c4be5-131">Herhangi bir iş akışı tamamlanıp onaylanır ve istek etkin işe alım için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="c4be5-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="c4be5-132">200000006</span><span class="sxs-lookup"><span data-stu-id="c4be5-132">200000006</span></span> | <span data-ttu-id="c4be5-133">Kapatıldı</span><span class="sxs-lookup"><span data-stu-id="c4be5-133">Closed</span></span> | <span data-ttu-id="c4be5-134">İşe alım isteği kapatıldı.</span><span class="sxs-lookup"><span data-stu-id="c4be5-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c4be5-135">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="c4be5-135">See also</span></span>

[<span data-ttu-id="c4be5-136">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="c4be5-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="c4be5-137">Işe alma isteği için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="c4be5-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
