---
title: MyLeaveRequests genel bakış
description: Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420869"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="faf52-103">MyLeaveRequests genel bakış</span><span class="sxs-lookup"><span data-stu-id="faf52-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="faf52-104">Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="faf52-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="faf52-105">Anahtar</span><span class="sxs-lookup"><span data-stu-id="faf52-105">Key</span></span>

  | <span data-ttu-id="faf52-106">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="faf52-106">Property Name</span></span> | <span data-ttu-id="faf52-107">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="faf52-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="faf52-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="faf52-108">dataAreaId</span></span>    | <span data-ttu-id="faf52-109">Dize</span><span class="sxs-lookup"><span data-stu-id="faf52-109">String</span></span>    |
  | <span data-ttu-id="faf52-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="faf52-110">RequestId</span></span>     | <span data-ttu-id="faf52-111">Dize</span><span class="sxs-lookup"><span data-stu-id="faf52-111">String</span></span>    |
  | <span data-ttu-id="faf52-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="faf52-112">LeaveType</span></span>     | <span data-ttu-id="faf52-113">Dize</span><span class="sxs-lookup"><span data-stu-id="faf52-113">String</span></span>    |
  | <span data-ttu-id="faf52-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="faf52-114">LeaveDate</span></span>     | <span data-ttu-id="faf52-115">Tarih</span><span class="sxs-lookup"><span data-stu-id="faf52-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="faf52-116">Özellikler</span><span class="sxs-lookup"><span data-stu-id="faf52-116">Properties</span></span>

  | <span data-ttu-id="faf52-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="faf52-117">Property Name</span></span>     | <span data-ttu-id="faf52-118">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="faf52-118">Data Type</span></span> | <span data-ttu-id="faf52-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="faf52-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="faf52-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="faf52-120">dataAreaId</span></span>        | <span data-ttu-id="faf52-121">Dize</span><span class="sxs-lookup"><span data-stu-id="faf52-121">String</span></span>    | <span data-ttu-id="faf52-122">X</span><span class="sxs-lookup"><span data-stu-id="faf52-122">X</span></span>        |
  | <span data-ttu-id="faf52-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="faf52-123">RequestId</span></span>         | <span data-ttu-id="faf52-124">Dize</span><span class="sxs-lookup"><span data-stu-id="faf52-124">String</span></span>    | <span data-ttu-id="faf52-125">X</span><span class="sxs-lookup"><span data-stu-id="faf52-125">X</span></span>        |
  | <span data-ttu-id="faf52-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="faf52-126">LeaveType</span></span>         | <span data-ttu-id="faf52-127">Dize</span><span class="sxs-lookup"><span data-stu-id="faf52-127">String</span></span>    | <span data-ttu-id="faf52-128">X</span><span class="sxs-lookup"><span data-stu-id="faf52-128">X</span></span>        |
  | <span data-ttu-id="faf52-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="faf52-129">LeaveDate</span></span>         | <span data-ttu-id="faf52-130">Tarih</span><span class="sxs-lookup"><span data-stu-id="faf52-130">Date</span></span>      | <span data-ttu-id="faf52-131">X</span><span class="sxs-lookup"><span data-stu-id="faf52-131">X</span></span>        |
  | <span data-ttu-id="faf52-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="faf52-132">ReasonCodeId</span></span>      | <span data-ttu-id="faf52-133">Dize</span><span class="sxs-lookup"><span data-stu-id="faf52-133">String</span></span>    |          |
  | <span data-ttu-id="faf52-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="faf52-134">PersonnelNumber</span></span>   | <span data-ttu-id="faf52-135">Dize</span><span class="sxs-lookup"><span data-stu-id="faf52-135">String</span></span>    | <span data-ttu-id="faf52-136">X</span><span class="sxs-lookup"><span data-stu-id="faf52-136">X</span></span>        |
  | <span data-ttu-id="faf52-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="faf52-137">RequestDate</span></span>       | <span data-ttu-id="faf52-138">Tarih</span><span class="sxs-lookup"><span data-stu-id="faf52-138">Date</span></span>      | <span data-ttu-id="faf52-139">X</span><span class="sxs-lookup"><span data-stu-id="faf52-139">X</span></span>        |
  | <span data-ttu-id="faf52-140">Açıklama</span><span class="sxs-lookup"><span data-stu-id="faf52-140">Comment</span></span>           | <span data-ttu-id="faf52-141">Dize</span><span class="sxs-lookup"><span data-stu-id="faf52-141">String</span></span>    |          |
  | <span data-ttu-id="faf52-142">Durum</span><span class="sxs-lookup"><span data-stu-id="faf52-142">Status</span></span>            | <span data-ttu-id="faf52-143">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="faf52-143">Enum</span></span>      | <span data-ttu-id="faf52-144">X</span><span class="sxs-lookup"><span data-stu-id="faf52-144">X</span></span>        |
  | <span data-ttu-id="faf52-145">Tutar</span><span class="sxs-lookup"><span data-stu-id="faf52-145">Amount</span></span>            | <span data-ttu-id="faf52-146">Gerçek</span><span class="sxs-lookup"><span data-stu-id="faf52-146">Real</span></span>      |          |
  | <span data-ttu-id="faf52-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="faf52-147">HalfDayDefinition</span></span> | <span data-ttu-id="faf52-148">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="faf52-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="faf52-149">Eylemler</span><span class="sxs-lookup"><span data-stu-id="faf52-149">Actions</span></span>

 | <span data-ttu-id="faf52-150">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="faf52-150">Action Name</span></span>                               | <span data-ttu-id="faf52-151">Tanım</span><span class="sxs-lookup"><span data-stu-id="faf52-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="faf52-152">gönder</span><span class="sxs-lookup"><span data-stu-id="faf52-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="faf52-153">İsteği iş akışı tarafından işlenecek şekilde gönder.</span><span class="sxs-lookup"><span data-stu-id="faf52-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="faf52-154">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="faf52-154">See also</span></span>

- [<span data-ttu-id="faf52-155">Bir izin isteğini iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="faf52-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="faf52-156">Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="faf52-156">Authentication</span></span>](hr-developer-api-authentication.md)