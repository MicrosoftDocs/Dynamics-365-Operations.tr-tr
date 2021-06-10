---
title: MyLeaveRequests genel bakış
description: Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054968"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="bd4a2-103">MyLeaveRequests genel bakış</span><span class="sxs-lookup"><span data-stu-id="bd4a2-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bd4a2-104">Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="bd4a2-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="bd4a2-105">Anahtar</span><span class="sxs-lookup"><span data-stu-id="bd4a2-105">Key</span></span>

  | <span data-ttu-id="bd4a2-106">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="bd4a2-106">Property Name</span></span> | <span data-ttu-id="bd4a2-107">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="bd4a2-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="bd4a2-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="bd4a2-108">dataAreaId</span></span>    | <span data-ttu-id="bd4a2-109">Dize</span><span class="sxs-lookup"><span data-stu-id="bd4a2-109">String</span></span>    |
  | <span data-ttu-id="bd4a2-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="bd4a2-110">RequestId</span></span>     | <span data-ttu-id="bd4a2-111">Dize</span><span class="sxs-lookup"><span data-stu-id="bd4a2-111">String</span></span>    |
  | <span data-ttu-id="bd4a2-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="bd4a2-112">LeaveType</span></span>     | <span data-ttu-id="bd4a2-113">Dize</span><span class="sxs-lookup"><span data-stu-id="bd4a2-113">String</span></span>    |
  | <span data-ttu-id="bd4a2-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="bd4a2-114">LeaveDate</span></span>     | <span data-ttu-id="bd4a2-115">Tarih</span><span class="sxs-lookup"><span data-stu-id="bd4a2-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="bd4a2-116">Özellikler</span><span class="sxs-lookup"><span data-stu-id="bd4a2-116">Properties</span></span>

  | <span data-ttu-id="bd4a2-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="bd4a2-117">Property Name</span></span>     | <span data-ttu-id="bd4a2-118">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="bd4a2-118">Data Type</span></span> | <span data-ttu-id="bd4a2-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="bd4a2-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="bd4a2-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="bd4a2-120">dataAreaId</span></span>        | <span data-ttu-id="bd4a2-121">Dize</span><span class="sxs-lookup"><span data-stu-id="bd4a2-121">String</span></span>    | <span data-ttu-id="bd4a2-122">X</span><span class="sxs-lookup"><span data-stu-id="bd4a2-122">X</span></span>        |
  | <span data-ttu-id="bd4a2-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="bd4a2-123">RequestId</span></span>         | <span data-ttu-id="bd4a2-124">Dize</span><span class="sxs-lookup"><span data-stu-id="bd4a2-124">String</span></span>    | <span data-ttu-id="bd4a2-125">X</span><span class="sxs-lookup"><span data-stu-id="bd4a2-125">X</span></span>        |
  | <span data-ttu-id="bd4a2-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="bd4a2-126">LeaveType</span></span>         | <span data-ttu-id="bd4a2-127">Dize</span><span class="sxs-lookup"><span data-stu-id="bd4a2-127">String</span></span>    | <span data-ttu-id="bd4a2-128">X</span><span class="sxs-lookup"><span data-stu-id="bd4a2-128">X</span></span>        |
  | <span data-ttu-id="bd4a2-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="bd4a2-129">LeaveDate</span></span>         | <span data-ttu-id="bd4a2-130">Tarih</span><span class="sxs-lookup"><span data-stu-id="bd4a2-130">Date</span></span>      | <span data-ttu-id="bd4a2-131">X</span><span class="sxs-lookup"><span data-stu-id="bd4a2-131">X</span></span>        |
  | <span data-ttu-id="bd4a2-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="bd4a2-132">ReasonCodeId</span></span>      | <span data-ttu-id="bd4a2-133">Dize</span><span class="sxs-lookup"><span data-stu-id="bd4a2-133">String</span></span>    |          |
  | <span data-ttu-id="bd4a2-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="bd4a2-134">PersonnelNumber</span></span>   | <span data-ttu-id="bd4a2-135">Dize</span><span class="sxs-lookup"><span data-stu-id="bd4a2-135">String</span></span>    | <span data-ttu-id="bd4a2-136">X</span><span class="sxs-lookup"><span data-stu-id="bd4a2-136">X</span></span>        |
  | <span data-ttu-id="bd4a2-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="bd4a2-137">RequestDate</span></span>       | <span data-ttu-id="bd4a2-138">Tarih</span><span class="sxs-lookup"><span data-stu-id="bd4a2-138">Date</span></span>      | <span data-ttu-id="bd4a2-139">X</span><span class="sxs-lookup"><span data-stu-id="bd4a2-139">X</span></span>        |
  | <span data-ttu-id="bd4a2-140">Açıklama</span><span class="sxs-lookup"><span data-stu-id="bd4a2-140">Comment</span></span>           | <span data-ttu-id="bd4a2-141">Dize</span><span class="sxs-lookup"><span data-stu-id="bd4a2-141">String</span></span>    |          |
  | <span data-ttu-id="bd4a2-142">Durum</span><span class="sxs-lookup"><span data-stu-id="bd4a2-142">Status</span></span>            | <span data-ttu-id="bd4a2-143">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="bd4a2-143">Enum</span></span>      | <span data-ttu-id="bd4a2-144">X</span><span class="sxs-lookup"><span data-stu-id="bd4a2-144">X</span></span>        |
  | <span data-ttu-id="bd4a2-145">Tutar</span><span class="sxs-lookup"><span data-stu-id="bd4a2-145">Amount</span></span>            | <span data-ttu-id="bd4a2-146">Gerçek</span><span class="sxs-lookup"><span data-stu-id="bd4a2-146">Real</span></span>      |          |
  | <span data-ttu-id="bd4a2-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="bd4a2-147">HalfDayDefinition</span></span> | <span data-ttu-id="bd4a2-148">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="bd4a2-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="bd4a2-149">Eylemler</span><span class="sxs-lookup"><span data-stu-id="bd4a2-149">Actions</span></span>

 | <span data-ttu-id="bd4a2-150">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="bd4a2-150">Action Name</span></span>                               | <span data-ttu-id="bd4a2-151">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd4a2-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="bd4a2-152">gönder</span><span class="sxs-lookup"><span data-stu-id="bd4a2-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="bd4a2-153">İsteği iş akışı tarafından işlenecek şekilde gönder.</span><span class="sxs-lookup"><span data-stu-id="bd4a2-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="bd4a2-154">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="bd4a2-154">See also</span></span>

- [<span data-ttu-id="bd4a2-155">Bir izin isteğini iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="bd4a2-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="bd4a2-156">Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="bd4a2-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]