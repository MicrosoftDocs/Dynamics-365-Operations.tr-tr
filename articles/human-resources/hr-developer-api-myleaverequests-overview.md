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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803645"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="8dc0e-103">MyLeaveRequests genel bakış</span><span class="sxs-lookup"><span data-stu-id="8dc0e-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8dc0e-104">Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="8dc0e-105">Anahtar</span><span class="sxs-lookup"><span data-stu-id="8dc0e-105">Key</span></span>

  | <span data-ttu-id="8dc0e-106">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="8dc0e-106">Property Name</span></span> | <span data-ttu-id="8dc0e-107">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="8dc0e-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="8dc0e-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8dc0e-108">dataAreaId</span></span>    | <span data-ttu-id="8dc0e-109">Dize</span><span class="sxs-lookup"><span data-stu-id="8dc0e-109">String</span></span>    |
  | <span data-ttu-id="8dc0e-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="8dc0e-110">RequestId</span></span>     | <span data-ttu-id="8dc0e-111">Dize</span><span class="sxs-lookup"><span data-stu-id="8dc0e-111">String</span></span>    |
  | <span data-ttu-id="8dc0e-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8dc0e-112">LeaveType</span></span>     | <span data-ttu-id="8dc0e-113">Dize</span><span class="sxs-lookup"><span data-stu-id="8dc0e-113">String</span></span>    |
  | <span data-ttu-id="8dc0e-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8dc0e-114">LeaveDate</span></span>     | <span data-ttu-id="8dc0e-115">Tarih</span><span class="sxs-lookup"><span data-stu-id="8dc0e-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="8dc0e-116">Özellikler</span><span class="sxs-lookup"><span data-stu-id="8dc0e-116">Properties</span></span>

  | <span data-ttu-id="8dc0e-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="8dc0e-117">Property Name</span></span>     | <span data-ttu-id="8dc0e-118">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="8dc0e-118">Data Type</span></span> | <span data-ttu-id="8dc0e-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="8dc0e-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="8dc0e-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8dc0e-120">dataAreaId</span></span>        | <span data-ttu-id="8dc0e-121">Dize</span><span class="sxs-lookup"><span data-stu-id="8dc0e-121">String</span></span>    | <span data-ttu-id="8dc0e-122">X</span><span class="sxs-lookup"><span data-stu-id="8dc0e-122">X</span></span>        |
  | <span data-ttu-id="8dc0e-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="8dc0e-123">RequestId</span></span>         | <span data-ttu-id="8dc0e-124">Dize</span><span class="sxs-lookup"><span data-stu-id="8dc0e-124">String</span></span>    | <span data-ttu-id="8dc0e-125">X</span><span class="sxs-lookup"><span data-stu-id="8dc0e-125">X</span></span>        |
  | <span data-ttu-id="8dc0e-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8dc0e-126">LeaveType</span></span>         | <span data-ttu-id="8dc0e-127">Dize</span><span class="sxs-lookup"><span data-stu-id="8dc0e-127">String</span></span>    | <span data-ttu-id="8dc0e-128">X</span><span class="sxs-lookup"><span data-stu-id="8dc0e-128">X</span></span>        |
  | <span data-ttu-id="8dc0e-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8dc0e-129">LeaveDate</span></span>         | <span data-ttu-id="8dc0e-130">Tarih</span><span class="sxs-lookup"><span data-stu-id="8dc0e-130">Date</span></span>      | <span data-ttu-id="8dc0e-131">X</span><span class="sxs-lookup"><span data-stu-id="8dc0e-131">X</span></span>        |
  | <span data-ttu-id="8dc0e-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="8dc0e-132">ReasonCodeId</span></span>      | <span data-ttu-id="8dc0e-133">Dize</span><span class="sxs-lookup"><span data-stu-id="8dc0e-133">String</span></span>    |          |
  | <span data-ttu-id="8dc0e-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="8dc0e-134">PersonnelNumber</span></span>   | <span data-ttu-id="8dc0e-135">Dize</span><span class="sxs-lookup"><span data-stu-id="8dc0e-135">String</span></span>    | <span data-ttu-id="8dc0e-136">X</span><span class="sxs-lookup"><span data-stu-id="8dc0e-136">X</span></span>        |
  | <span data-ttu-id="8dc0e-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="8dc0e-137">RequestDate</span></span>       | <span data-ttu-id="8dc0e-138">Tarih</span><span class="sxs-lookup"><span data-stu-id="8dc0e-138">Date</span></span>      | <span data-ttu-id="8dc0e-139">X</span><span class="sxs-lookup"><span data-stu-id="8dc0e-139">X</span></span>        |
  | <span data-ttu-id="8dc0e-140">Açıklama</span><span class="sxs-lookup"><span data-stu-id="8dc0e-140">Comment</span></span>           | <span data-ttu-id="8dc0e-141">Dize</span><span class="sxs-lookup"><span data-stu-id="8dc0e-141">String</span></span>    |          |
  | <span data-ttu-id="8dc0e-142">Durum</span><span class="sxs-lookup"><span data-stu-id="8dc0e-142">Status</span></span>            | <span data-ttu-id="8dc0e-143">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="8dc0e-143">Enum</span></span>      | <span data-ttu-id="8dc0e-144">X</span><span class="sxs-lookup"><span data-stu-id="8dc0e-144">X</span></span>        |
  | <span data-ttu-id="8dc0e-145">Tutar</span><span class="sxs-lookup"><span data-stu-id="8dc0e-145">Amount</span></span>            | <span data-ttu-id="8dc0e-146">Gerçek</span><span class="sxs-lookup"><span data-stu-id="8dc0e-146">Real</span></span>      |          |
  | <span data-ttu-id="8dc0e-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="8dc0e-147">HalfDayDefinition</span></span> | <span data-ttu-id="8dc0e-148">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="8dc0e-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="8dc0e-149">Eylemler</span><span class="sxs-lookup"><span data-stu-id="8dc0e-149">Actions</span></span>

 | <span data-ttu-id="8dc0e-150">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="8dc0e-150">Action Name</span></span>                               | <span data-ttu-id="8dc0e-151">Tanım</span><span class="sxs-lookup"><span data-stu-id="8dc0e-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="8dc0e-152">gönder</span><span class="sxs-lookup"><span data-stu-id="8dc0e-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="8dc0e-153">İsteği iş akışı tarafından işlenecek şekilde gönder.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8dc0e-154">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="8dc0e-154">See also</span></span>

- [<span data-ttu-id="8dc0e-155">Bir izin isteğini iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="8dc0e-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="8dc0e-156">Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="8dc0e-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]