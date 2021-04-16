---
title: İşe alma isteği durumu
description: Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.
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
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806054"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="9d15b-103">İşe alma isteği durumu</span><span class="sxs-lookup"><span data-stu-id="9d15b-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9d15b-104">Bu konu, Dynamics 365 Human Resources için İşe alma isteği durumu seçenek kümesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="9d15b-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9d15b-105">Fiziksel ad: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="9d15b-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="9d15b-106">Bu sabit listesi, İşe alma İsteği durum değerleri için seçenek kümesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9d15b-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="9d15b-107">Değer</span><span class="sxs-lookup"><span data-stu-id="9d15b-107">Value</span></span> | <span data-ttu-id="9d15b-108">Etiket</span><span class="sxs-lookup"><span data-stu-id="9d15b-108">Label</span></span> | <span data-ttu-id="9d15b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d15b-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9d15b-110">200000000</span><span class="sxs-lookup"><span data-stu-id="9d15b-110">200000000</span></span> | <span data-ttu-id="9d15b-111">Taslak</span><span class="sxs-lookup"><span data-stu-id="9d15b-111">Draft</span></span> | <span data-ttu-id="9d15b-112">İstek taslak halindedir ve aktif işe alım için hazır değildir.</span><span class="sxs-lookup"><span data-stu-id="9d15b-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="9d15b-113">200000001</span><span class="sxs-lookup"><span data-stu-id="9d15b-113">200000001</span></span> | <span data-ttu-id="9d15b-114">İncelemede</span><span class="sxs-lookup"><span data-stu-id="9d15b-114">In Review</span></span> | <span data-ttu-id="9d15b-115">İstek gönderildi ve iş akışı tarafından onay için yönlendiriliyor.</span><span class="sxs-lookup"><span data-stu-id="9d15b-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="9d15b-116">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9d15b-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="9d15b-117">200000002</span><span class="sxs-lookup"><span data-stu-id="9d15b-117">200000002</span></span> | <span data-ttu-id="9d15b-118">Bekliyor</span><span class="sxs-lookup"><span data-stu-id="9d15b-118">Pending</span></span> | <span data-ttu-id="9d15b-119">İstek iş akışı eylemini bekliyor.</span><span class="sxs-lookup"><span data-stu-id="9d15b-119">The request is pending workflow action.</span></span> <span data-ttu-id="9d15b-120">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9d15b-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="9d15b-121">200000003</span><span class="sxs-lookup"><span data-stu-id="9d15b-121">200000003</span></span> | <span data-ttu-id="9d15b-122">İptal Edildi</span><span class="sxs-lookup"><span data-stu-id="9d15b-122">Canceled</span></span> | <span data-ttu-id="9d15b-123">İstek iptal edildi.</span><span class="sxs-lookup"><span data-stu-id="9d15b-123">The request has been canceled.</span></span> <span data-ttu-id="9d15b-124">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9d15b-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="9d15b-125">200000004</span><span class="sxs-lookup"><span data-stu-id="9d15b-125">200000004</span></span> | <span data-ttu-id="9d15b-126">Reddedildi</span><span class="sxs-lookup"><span data-stu-id="9d15b-126">Denied</span></span> | <span data-ttu-id="9d15b-127">İstek reddedildi.</span><span class="sxs-lookup"><span data-stu-id="9d15b-127">The request has been denied.</span></span> <span data-ttu-id="9d15b-128">Yalnızca iş akışı etkinleştirildiğinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9d15b-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="9d15b-129">200000005</span><span class="sxs-lookup"><span data-stu-id="9d15b-129">200000005</span></span> | <span data-ttu-id="9d15b-130">Active</span><span class="sxs-lookup"><span data-stu-id="9d15b-130">Active</span></span> | <span data-ttu-id="9d15b-131">Herhangi bir iş akışı tamamlanıp onaylanır ve istek etkin işe alım için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="9d15b-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="9d15b-132">200000006</span><span class="sxs-lookup"><span data-stu-id="9d15b-132">200000006</span></span> | <span data-ttu-id="9d15b-133">Kapatıldı</span><span class="sxs-lookup"><span data-stu-id="9d15b-133">Closed</span></span> | <span data-ttu-id="9d15b-134">İşe alım isteği kapatıldı.</span><span class="sxs-lookup"><span data-stu-id="9d15b-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9d15b-135">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="9d15b-135">See also</span></span>

[<span data-ttu-id="9d15b-136">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="9d15b-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9d15b-137">Işe alma isteği için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="9d15b-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]