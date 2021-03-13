---
title: MyLeaveRequests genel bakış
description: Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115548"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="b232c-103">MyLeaveRequests genel bakış</span><span class="sxs-lookup"><span data-stu-id="b232c-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="b232c-104">Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="b232c-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="b232c-105">Anahtar</span><span class="sxs-lookup"><span data-stu-id="b232c-105">Key</span></span>

  | <span data-ttu-id="b232c-106">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="b232c-106">Property Name</span></span> | <span data-ttu-id="b232c-107">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="b232c-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="b232c-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="b232c-108">dataAreaId</span></span>    | <span data-ttu-id="b232c-109">Dize</span><span class="sxs-lookup"><span data-stu-id="b232c-109">String</span></span>    |
  | <span data-ttu-id="b232c-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="b232c-110">RequestId</span></span>     | <span data-ttu-id="b232c-111">Dize</span><span class="sxs-lookup"><span data-stu-id="b232c-111">String</span></span>    |
  | <span data-ttu-id="b232c-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="b232c-112">LeaveType</span></span>     | <span data-ttu-id="b232c-113">Dize</span><span class="sxs-lookup"><span data-stu-id="b232c-113">String</span></span>    |
  | <span data-ttu-id="b232c-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="b232c-114">LeaveDate</span></span>     | <span data-ttu-id="b232c-115">Tarih</span><span class="sxs-lookup"><span data-stu-id="b232c-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="b232c-116">Özellikler</span><span class="sxs-lookup"><span data-stu-id="b232c-116">Properties</span></span>

  | <span data-ttu-id="b232c-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="b232c-117">Property Name</span></span>     | <span data-ttu-id="b232c-118">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="b232c-118">Data Type</span></span> | <span data-ttu-id="b232c-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="b232c-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="b232c-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="b232c-120">dataAreaId</span></span>        | <span data-ttu-id="b232c-121">Dize</span><span class="sxs-lookup"><span data-stu-id="b232c-121">String</span></span>    | <span data-ttu-id="b232c-122">X</span><span class="sxs-lookup"><span data-stu-id="b232c-122">X</span></span>        |
  | <span data-ttu-id="b232c-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="b232c-123">RequestId</span></span>         | <span data-ttu-id="b232c-124">Dize</span><span class="sxs-lookup"><span data-stu-id="b232c-124">String</span></span>    | <span data-ttu-id="b232c-125">X</span><span class="sxs-lookup"><span data-stu-id="b232c-125">X</span></span>        |
  | <span data-ttu-id="b232c-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="b232c-126">LeaveType</span></span>         | <span data-ttu-id="b232c-127">Dize</span><span class="sxs-lookup"><span data-stu-id="b232c-127">String</span></span>    | <span data-ttu-id="b232c-128">X</span><span class="sxs-lookup"><span data-stu-id="b232c-128">X</span></span>        |
  | <span data-ttu-id="b232c-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="b232c-129">LeaveDate</span></span>         | <span data-ttu-id="b232c-130">Tarih</span><span class="sxs-lookup"><span data-stu-id="b232c-130">Date</span></span>      | <span data-ttu-id="b232c-131">X</span><span class="sxs-lookup"><span data-stu-id="b232c-131">X</span></span>        |
  | <span data-ttu-id="b232c-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="b232c-132">ReasonCodeId</span></span>      | <span data-ttu-id="b232c-133">Dize</span><span class="sxs-lookup"><span data-stu-id="b232c-133">String</span></span>    |          |
  | <span data-ttu-id="b232c-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="b232c-134">PersonnelNumber</span></span>   | <span data-ttu-id="b232c-135">Dize</span><span class="sxs-lookup"><span data-stu-id="b232c-135">String</span></span>    | <span data-ttu-id="b232c-136">X</span><span class="sxs-lookup"><span data-stu-id="b232c-136">X</span></span>        |
  | <span data-ttu-id="b232c-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="b232c-137">RequestDate</span></span>       | <span data-ttu-id="b232c-138">Tarih</span><span class="sxs-lookup"><span data-stu-id="b232c-138">Date</span></span>      | <span data-ttu-id="b232c-139">X</span><span class="sxs-lookup"><span data-stu-id="b232c-139">X</span></span>        |
  | <span data-ttu-id="b232c-140">Açıklama</span><span class="sxs-lookup"><span data-stu-id="b232c-140">Comment</span></span>           | <span data-ttu-id="b232c-141">Dize</span><span class="sxs-lookup"><span data-stu-id="b232c-141">String</span></span>    |          |
  | <span data-ttu-id="b232c-142">Durum</span><span class="sxs-lookup"><span data-stu-id="b232c-142">Status</span></span>            | <span data-ttu-id="b232c-143">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="b232c-143">Enum</span></span>      | <span data-ttu-id="b232c-144">X</span><span class="sxs-lookup"><span data-stu-id="b232c-144">X</span></span>        |
  | <span data-ttu-id="b232c-145">Tutar</span><span class="sxs-lookup"><span data-stu-id="b232c-145">Amount</span></span>            | <span data-ttu-id="b232c-146">Gerçek</span><span class="sxs-lookup"><span data-stu-id="b232c-146">Real</span></span>      |          |
  | <span data-ttu-id="b232c-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="b232c-147">HalfDayDefinition</span></span> | <span data-ttu-id="b232c-148">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="b232c-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="b232c-149">Eylemler</span><span class="sxs-lookup"><span data-stu-id="b232c-149">Actions</span></span>

 | <span data-ttu-id="b232c-150">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="b232c-150">Action Name</span></span>                               | <span data-ttu-id="b232c-151">Tanım</span><span class="sxs-lookup"><span data-stu-id="b232c-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="b232c-152">gönder</span><span class="sxs-lookup"><span data-stu-id="b232c-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="b232c-153">İsteği iş akışı tarafından işlenecek şekilde gönder.</span><span class="sxs-lookup"><span data-stu-id="b232c-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b232c-154">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b232c-154">See also</span></span>

- [<span data-ttu-id="b232c-155">Bir izin isteğini iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="b232c-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="b232c-156">Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="b232c-156">Authentication</span></span>](hr-developer-api-authentication.md)