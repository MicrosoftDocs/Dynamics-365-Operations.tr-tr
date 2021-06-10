---
title: İşe alma isteği durumu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059196"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="9445e-103">İşe alma isteği durumu</span><span class="sxs-lookup"><span data-stu-id="9445e-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9445e-104">Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="9445e-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9445e-105">Fiziksel ad: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="9445e-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="9445e-106">Bu sabit listesi, İşe alma İsteği durum değerleri için seçenek kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9445e-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="9445e-107">Değer</span><span class="sxs-lookup"><span data-stu-id="9445e-107">Value</span></span> | <span data-ttu-id="9445e-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="9445e-108">Label</span></span> | <span data-ttu-id="9445e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9445e-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9445e-110">200000000</span><span class="sxs-lookup"><span data-stu-id="9445e-110">200000000</span></span> | <span data-ttu-id="9445e-111">Taslak</span><span class="sxs-lookup"><span data-stu-id="9445e-111">Draft</span></span> | <span data-ttu-id="9445e-112">İstek taslak halindedir ve aktif işe alım için hazır değildir.</span><span class="sxs-lookup"><span data-stu-id="9445e-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="9445e-113">200000001</span><span class="sxs-lookup"><span data-stu-id="9445e-113">200000001</span></span> | <span data-ttu-id="9445e-114">İncelemede</span><span class="sxs-lookup"><span data-stu-id="9445e-114">In Review</span></span> | <span data-ttu-id="9445e-115">İstek gönderildi ve iş akışı tarafından onay için yönlendiriliyor.</span><span class="sxs-lookup"><span data-stu-id="9445e-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="9445e-116">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9445e-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="9445e-117">200000002</span><span class="sxs-lookup"><span data-stu-id="9445e-117">200000002</span></span> | <span data-ttu-id="9445e-118">Bekliyor</span><span class="sxs-lookup"><span data-stu-id="9445e-118">Pending</span></span> | <span data-ttu-id="9445e-119">İstek iş akışı eylemini bekliyor.</span><span class="sxs-lookup"><span data-stu-id="9445e-119">The request is pending workflow action.</span></span> <span data-ttu-id="9445e-120">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9445e-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="9445e-121">200000003</span><span class="sxs-lookup"><span data-stu-id="9445e-121">200000003</span></span> | <span data-ttu-id="9445e-122">İptal Edildi</span><span class="sxs-lookup"><span data-stu-id="9445e-122">Canceled</span></span> | <span data-ttu-id="9445e-123">İstek iptal edildi.</span><span class="sxs-lookup"><span data-stu-id="9445e-123">The request has been canceled.</span></span> <span data-ttu-id="9445e-124">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9445e-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="9445e-125">200000004</span><span class="sxs-lookup"><span data-stu-id="9445e-125">200000004</span></span> | <span data-ttu-id="9445e-126">Reddedildi</span><span class="sxs-lookup"><span data-stu-id="9445e-126">Denied</span></span> | <span data-ttu-id="9445e-127">İstek reddedildi.</span><span class="sxs-lookup"><span data-stu-id="9445e-127">The request has been denied.</span></span> <span data-ttu-id="9445e-128">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9445e-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="9445e-129">200000005</span><span class="sxs-lookup"><span data-stu-id="9445e-129">200000005</span></span> | <span data-ttu-id="9445e-130">Active</span><span class="sxs-lookup"><span data-stu-id="9445e-130">Active</span></span> | <span data-ttu-id="9445e-131">Herhangi bir iş akışı tamamlanıp onaylanır ve istek etkin işe alım için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="9445e-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="9445e-132">200000006</span><span class="sxs-lookup"><span data-stu-id="9445e-132">200000006</span></span> | <span data-ttu-id="9445e-133">Kapatıldı</span><span class="sxs-lookup"><span data-stu-id="9445e-133">Closed</span></span> | <span data-ttu-id="9445e-134">İşe alım isteği kapatıldı.</span><span class="sxs-lookup"><span data-stu-id="9445e-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9445e-135">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="9445e-135">See also</span></span>

[<span data-ttu-id="9445e-136">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="9445e-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9445e-137">Işe alma isteği için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="9445e-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]