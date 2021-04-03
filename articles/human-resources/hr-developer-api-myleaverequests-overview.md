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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465522"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="4378d-103">MyLeaveRequests genel bakış</span><span class="sxs-lookup"><span data-stu-id="4378d-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4378d-104">Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="4378d-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="4378d-105">Anahtar</span><span class="sxs-lookup"><span data-stu-id="4378d-105">Key</span></span>

  | <span data-ttu-id="4378d-106">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="4378d-106">Property Name</span></span> | <span data-ttu-id="4378d-107">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="4378d-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="4378d-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="4378d-108">dataAreaId</span></span>    | <span data-ttu-id="4378d-109">Dize</span><span class="sxs-lookup"><span data-stu-id="4378d-109">String</span></span>    |
  | <span data-ttu-id="4378d-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="4378d-110">RequestId</span></span>     | <span data-ttu-id="4378d-111">Dize</span><span class="sxs-lookup"><span data-stu-id="4378d-111">String</span></span>    |
  | <span data-ttu-id="4378d-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="4378d-112">LeaveType</span></span>     | <span data-ttu-id="4378d-113">Dize</span><span class="sxs-lookup"><span data-stu-id="4378d-113">String</span></span>    |
  | <span data-ttu-id="4378d-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="4378d-114">LeaveDate</span></span>     | <span data-ttu-id="4378d-115">Tarih</span><span class="sxs-lookup"><span data-stu-id="4378d-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="4378d-116">Özellikler</span><span class="sxs-lookup"><span data-stu-id="4378d-116">Properties</span></span>

  | <span data-ttu-id="4378d-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="4378d-117">Property Name</span></span>     | <span data-ttu-id="4378d-118">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="4378d-118">Data Type</span></span> | <span data-ttu-id="4378d-119">Gerekli</span><span class="sxs-lookup"><span data-stu-id="4378d-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="4378d-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="4378d-120">dataAreaId</span></span>        | <span data-ttu-id="4378d-121">Dize</span><span class="sxs-lookup"><span data-stu-id="4378d-121">String</span></span>    | <span data-ttu-id="4378d-122">X</span><span class="sxs-lookup"><span data-stu-id="4378d-122">X</span></span>        |
  | <span data-ttu-id="4378d-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="4378d-123">RequestId</span></span>         | <span data-ttu-id="4378d-124">Dize</span><span class="sxs-lookup"><span data-stu-id="4378d-124">String</span></span>    | <span data-ttu-id="4378d-125">X</span><span class="sxs-lookup"><span data-stu-id="4378d-125">X</span></span>        |
  | <span data-ttu-id="4378d-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="4378d-126">LeaveType</span></span>         | <span data-ttu-id="4378d-127">Dize</span><span class="sxs-lookup"><span data-stu-id="4378d-127">String</span></span>    | <span data-ttu-id="4378d-128">X</span><span class="sxs-lookup"><span data-stu-id="4378d-128">X</span></span>        |
  | <span data-ttu-id="4378d-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="4378d-129">LeaveDate</span></span>         | <span data-ttu-id="4378d-130">Tarih</span><span class="sxs-lookup"><span data-stu-id="4378d-130">Date</span></span>      | <span data-ttu-id="4378d-131">X</span><span class="sxs-lookup"><span data-stu-id="4378d-131">X</span></span>        |
  | <span data-ttu-id="4378d-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="4378d-132">ReasonCodeId</span></span>      | <span data-ttu-id="4378d-133">Dize</span><span class="sxs-lookup"><span data-stu-id="4378d-133">String</span></span>    |          |
  | <span data-ttu-id="4378d-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="4378d-134">PersonnelNumber</span></span>   | <span data-ttu-id="4378d-135">Dize</span><span class="sxs-lookup"><span data-stu-id="4378d-135">String</span></span>    | <span data-ttu-id="4378d-136">X</span><span class="sxs-lookup"><span data-stu-id="4378d-136">X</span></span>        |
  | <span data-ttu-id="4378d-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="4378d-137">RequestDate</span></span>       | <span data-ttu-id="4378d-138">Tarih</span><span class="sxs-lookup"><span data-stu-id="4378d-138">Date</span></span>      | <span data-ttu-id="4378d-139">X</span><span class="sxs-lookup"><span data-stu-id="4378d-139">X</span></span>        |
  | <span data-ttu-id="4378d-140">Açıklama</span><span class="sxs-lookup"><span data-stu-id="4378d-140">Comment</span></span>           | <span data-ttu-id="4378d-141">Dize</span><span class="sxs-lookup"><span data-stu-id="4378d-141">String</span></span>    |          |
  | <span data-ttu-id="4378d-142">Durum</span><span class="sxs-lookup"><span data-stu-id="4378d-142">Status</span></span>            | <span data-ttu-id="4378d-143">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="4378d-143">Enum</span></span>      | <span data-ttu-id="4378d-144">X</span><span class="sxs-lookup"><span data-stu-id="4378d-144">X</span></span>        |
  | <span data-ttu-id="4378d-145">Tutar</span><span class="sxs-lookup"><span data-stu-id="4378d-145">Amount</span></span>            | <span data-ttu-id="4378d-146">Gerçek</span><span class="sxs-lookup"><span data-stu-id="4378d-146">Real</span></span>      |          |
  | <span data-ttu-id="4378d-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="4378d-147">HalfDayDefinition</span></span> | <span data-ttu-id="4378d-148">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="4378d-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="4378d-149">Eylemler</span><span class="sxs-lookup"><span data-stu-id="4378d-149">Actions</span></span>

 | <span data-ttu-id="4378d-150">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="4378d-150">Action Name</span></span>                               | <span data-ttu-id="4378d-151">Tanım</span><span class="sxs-lookup"><span data-stu-id="4378d-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="4378d-152">gönder</span><span class="sxs-lookup"><span data-stu-id="4378d-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="4378d-153">İsteği iş akışı tarafından işlenecek şekilde gönder.</span><span class="sxs-lookup"><span data-stu-id="4378d-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4378d-154">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="4378d-154">See also</span></span>

- [<span data-ttu-id="4378d-155">Bir izin isteğini iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="4378d-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="4378d-156">Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="4378d-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]