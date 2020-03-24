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
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092049"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="5cc16-103">MyLeaveRequests genel bakış</span><span class="sxs-lookup"><span data-stu-id="5cc16-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="5cc16-104">Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="5cc16-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="5cc16-105">Anahtar</span><span class="sxs-lookup"><span data-stu-id="5cc16-105">Key</span></span>

  | <span data-ttu-id="5cc16-106">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="5cc16-106">Property Name</span></span> | <span data-ttu-id="5cc16-107">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="5cc16-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="5cc16-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="5cc16-108">dataAreaId</span></span>    | <span data-ttu-id="5cc16-109">Dize</span><span class="sxs-lookup"><span data-stu-id="5cc16-109">String</span></span>    |
  | <span data-ttu-id="5cc16-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="5cc16-110">RequestId</span></span>     | <span data-ttu-id="5cc16-111">Dize</span><span class="sxs-lookup"><span data-stu-id="5cc16-111">String</span></span>    |
  | <span data-ttu-id="5cc16-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="5cc16-112">LeaveType</span></span>     | <span data-ttu-id="5cc16-113">Dize</span><span class="sxs-lookup"><span data-stu-id="5cc16-113">String</span></span>    |
  | <span data-ttu-id="5cc16-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="5cc16-114">LeaveDate</span></span>     | <span data-ttu-id="5cc16-115">Tarih</span><span class="sxs-lookup"><span data-stu-id="5cc16-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="5cc16-116">Özellikler</span><span class="sxs-lookup"><span data-stu-id="5cc16-116">Properties</span></span>

  | <span data-ttu-id="5cc16-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="5cc16-117">Property Name</span></span>     | <span data-ttu-id="5cc16-118">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="5cc16-118">Data Type</span></span> | <span data-ttu-id="5cc16-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="5cc16-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="5cc16-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="5cc16-120">dataAreaId</span></span>        | <span data-ttu-id="5cc16-121">Dize</span><span class="sxs-lookup"><span data-stu-id="5cc16-121">String</span></span>    | <span data-ttu-id="5cc16-122">X</span><span class="sxs-lookup"><span data-stu-id="5cc16-122">X</span></span>        |
  | <span data-ttu-id="5cc16-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="5cc16-123">RequestId</span></span>         | <span data-ttu-id="5cc16-124">Dize</span><span class="sxs-lookup"><span data-stu-id="5cc16-124">String</span></span>    | <span data-ttu-id="5cc16-125">X</span><span class="sxs-lookup"><span data-stu-id="5cc16-125">X</span></span>        |
  | <span data-ttu-id="5cc16-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="5cc16-126">LeaveType</span></span>         | <span data-ttu-id="5cc16-127">Dize</span><span class="sxs-lookup"><span data-stu-id="5cc16-127">String</span></span>    | <span data-ttu-id="5cc16-128">X</span><span class="sxs-lookup"><span data-stu-id="5cc16-128">X</span></span>        |
  | <span data-ttu-id="5cc16-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="5cc16-129">LeaveDate</span></span>         | <span data-ttu-id="5cc16-130">Tarih</span><span class="sxs-lookup"><span data-stu-id="5cc16-130">Date</span></span>      | <span data-ttu-id="5cc16-131">X</span><span class="sxs-lookup"><span data-stu-id="5cc16-131">X</span></span>        |
  | <span data-ttu-id="5cc16-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="5cc16-132">ReasonCodeId</span></span>      | <span data-ttu-id="5cc16-133">Dize</span><span class="sxs-lookup"><span data-stu-id="5cc16-133">String</span></span>    |          |
  | <span data-ttu-id="5cc16-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="5cc16-134">PersonnelNumber</span></span>   | <span data-ttu-id="5cc16-135">Dize</span><span class="sxs-lookup"><span data-stu-id="5cc16-135">String</span></span>    | <span data-ttu-id="5cc16-136">X</span><span class="sxs-lookup"><span data-stu-id="5cc16-136">X</span></span>        |
  | <span data-ttu-id="5cc16-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="5cc16-137">RequestDate</span></span>       | <span data-ttu-id="5cc16-138">Tarih</span><span class="sxs-lookup"><span data-stu-id="5cc16-138">Date</span></span>      | <span data-ttu-id="5cc16-139">X</span><span class="sxs-lookup"><span data-stu-id="5cc16-139">X</span></span>        |
  | <span data-ttu-id="5cc16-140">Açıklama</span><span class="sxs-lookup"><span data-stu-id="5cc16-140">Comment</span></span>           | <span data-ttu-id="5cc16-141">Dize</span><span class="sxs-lookup"><span data-stu-id="5cc16-141">String</span></span>    |          |
  | <span data-ttu-id="5cc16-142">Durum</span><span class="sxs-lookup"><span data-stu-id="5cc16-142">Status</span></span>            | <span data-ttu-id="5cc16-143">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="5cc16-143">Enum</span></span>      | <span data-ttu-id="5cc16-144">X</span><span class="sxs-lookup"><span data-stu-id="5cc16-144">X</span></span>        |
  | <span data-ttu-id="5cc16-145">Tutar</span><span class="sxs-lookup"><span data-stu-id="5cc16-145">Amount</span></span>            | <span data-ttu-id="5cc16-146">Gerçek</span><span class="sxs-lookup"><span data-stu-id="5cc16-146">Real</span></span>      |          |
  | <span data-ttu-id="5cc16-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="5cc16-147">HalfDayDefinition</span></span> | <span data-ttu-id="5cc16-148">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="5cc16-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="5cc16-149">Eylemler</span><span class="sxs-lookup"><span data-stu-id="5cc16-149">Actions</span></span>

 | <span data-ttu-id="5cc16-150">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="5cc16-150">Action Name</span></span>                               | <span data-ttu-id="5cc16-151">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cc16-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="5cc16-152">gönder</span><span class="sxs-lookup"><span data-stu-id="5cc16-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="5cc16-153">İsteği iş akışı tarafından işlenecek şekilde gönder.</span><span class="sxs-lookup"><span data-stu-id="5cc16-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5cc16-154">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="5cc16-154">See also</span></span>

- [<span data-ttu-id="5cc16-155">Bir izin isteğini iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="5cc16-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="5cc16-156">Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="5cc16-156">Authentication</span></span>](hr-developer-api-authentication.md)