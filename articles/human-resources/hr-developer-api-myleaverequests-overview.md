---
title: MyLeaveRequests genel bakış
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010859"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="f85fd-102">MyLeaveRequests genel bakış</span><span class="sxs-lookup"><span data-stu-id="f85fd-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="f85fd-103">Microsoft Dynamics 365 Human Resources'un MyLeaveRequests varlığı, sistemdeki bırakma isteklerinin listesini, varlığı sorgulayan geçerli kullanıcının erişebileceği isteklere kapsam dışı (sınırlı) olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="f85fd-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="f85fd-104">Anahtar</span><span class="sxs-lookup"><span data-stu-id="f85fd-104">Key</span></span>

  | <span data-ttu-id="f85fd-105">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="f85fd-105">Property Name</span></span> | <span data-ttu-id="f85fd-106">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="f85fd-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="f85fd-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f85fd-107">dataAreaId</span></span>    | <span data-ttu-id="f85fd-108">Dize</span><span class="sxs-lookup"><span data-stu-id="f85fd-108">String</span></span>    |
  | <span data-ttu-id="f85fd-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="f85fd-109">RequestId</span></span>     | <span data-ttu-id="f85fd-110">Dize</span><span class="sxs-lookup"><span data-stu-id="f85fd-110">String</span></span>    |
  | <span data-ttu-id="f85fd-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f85fd-111">LeaveType</span></span>     | <span data-ttu-id="f85fd-112">Dize</span><span class="sxs-lookup"><span data-stu-id="f85fd-112">String</span></span>    |
  | <span data-ttu-id="f85fd-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f85fd-113">LeaveDate</span></span>     | <span data-ttu-id="f85fd-114">Tarih</span><span class="sxs-lookup"><span data-stu-id="f85fd-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="f85fd-115">Özellikler</span><span class="sxs-lookup"><span data-stu-id="f85fd-115">Properties</span></span>

  | <span data-ttu-id="f85fd-116">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="f85fd-116">Property Name</span></span>     | <span data-ttu-id="f85fd-117">Veri Türü</span><span class="sxs-lookup"><span data-stu-id="f85fd-117">Data Type</span></span> | <span data-ttu-id="f85fd-118">Gerekli</span><span class="sxs-lookup"><span data-stu-id="f85fd-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="f85fd-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="f85fd-119">dataAreaId</span></span>        | <span data-ttu-id="f85fd-120">Dize</span><span class="sxs-lookup"><span data-stu-id="f85fd-120">String</span></span>    | <span data-ttu-id="f85fd-121">X</span><span class="sxs-lookup"><span data-stu-id="f85fd-121">X</span></span>        |
  | <span data-ttu-id="f85fd-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="f85fd-122">RequestId</span></span>         | <span data-ttu-id="f85fd-123">Dize</span><span class="sxs-lookup"><span data-stu-id="f85fd-123">String</span></span>    | <span data-ttu-id="f85fd-124">X</span><span class="sxs-lookup"><span data-stu-id="f85fd-124">X</span></span>        |
  | <span data-ttu-id="f85fd-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="f85fd-125">LeaveType</span></span>         | <span data-ttu-id="f85fd-126">Dize</span><span class="sxs-lookup"><span data-stu-id="f85fd-126">String</span></span>    | <span data-ttu-id="f85fd-127">X</span><span class="sxs-lookup"><span data-stu-id="f85fd-127">X</span></span>        |
  | <span data-ttu-id="f85fd-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="f85fd-128">LeaveDate</span></span>         | <span data-ttu-id="f85fd-129">Tarih</span><span class="sxs-lookup"><span data-stu-id="f85fd-129">Date</span></span>      | <span data-ttu-id="f85fd-130">X</span><span class="sxs-lookup"><span data-stu-id="f85fd-130">X</span></span>        |
  | <span data-ttu-id="f85fd-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="f85fd-131">ReasonCodeId</span></span>      | <span data-ttu-id="f85fd-132">Dize</span><span class="sxs-lookup"><span data-stu-id="f85fd-132">String</span></span>    |          |
  | <span data-ttu-id="f85fd-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="f85fd-133">PersonnelNumber</span></span>   | <span data-ttu-id="f85fd-134">Dize</span><span class="sxs-lookup"><span data-stu-id="f85fd-134">String</span></span>    | <span data-ttu-id="f85fd-135">X</span><span class="sxs-lookup"><span data-stu-id="f85fd-135">X</span></span>        |
  | <span data-ttu-id="f85fd-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="f85fd-136">RequestDate</span></span>       | <span data-ttu-id="f85fd-137">Tarih</span><span class="sxs-lookup"><span data-stu-id="f85fd-137">Date</span></span>      | <span data-ttu-id="f85fd-138">X</span><span class="sxs-lookup"><span data-stu-id="f85fd-138">X</span></span>        |
  | <span data-ttu-id="f85fd-139">Açıklama</span><span class="sxs-lookup"><span data-stu-id="f85fd-139">Comment</span></span>           | <span data-ttu-id="f85fd-140">Dize</span><span class="sxs-lookup"><span data-stu-id="f85fd-140">String</span></span>    |          |
  | <span data-ttu-id="f85fd-141">Durum</span><span class="sxs-lookup"><span data-stu-id="f85fd-141">Status</span></span>            | <span data-ttu-id="f85fd-142">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="f85fd-142">Enum</span></span>      | <span data-ttu-id="f85fd-143">X</span><span class="sxs-lookup"><span data-stu-id="f85fd-143">X</span></span>        |
  | <span data-ttu-id="f85fd-144">Tutar</span><span class="sxs-lookup"><span data-stu-id="f85fd-144">Amount</span></span>            | <span data-ttu-id="f85fd-145">Gerçek</span><span class="sxs-lookup"><span data-stu-id="f85fd-145">Real</span></span>      |          |
  | <span data-ttu-id="f85fd-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="f85fd-146">HalfDayDefinition</span></span> | <span data-ttu-id="f85fd-147">Numaralandırma</span><span class="sxs-lookup"><span data-stu-id="f85fd-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="f85fd-148">Eylemler</span><span class="sxs-lookup"><span data-stu-id="f85fd-148">Actions</span></span>

 | <span data-ttu-id="f85fd-149">Eylem adı</span><span class="sxs-lookup"><span data-stu-id="f85fd-149">Action Name</span></span>                               | <span data-ttu-id="f85fd-150">Tanım</span><span class="sxs-lookup"><span data-stu-id="f85fd-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="f85fd-151">gönder</span><span class="sxs-lookup"><span data-stu-id="f85fd-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="f85fd-152">İsteği iş akışı tarafından işlenecek şekilde gönder.</span><span class="sxs-lookup"><span data-stu-id="f85fd-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="f85fd-153">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="f85fd-153">See also</span></span>

- [<span data-ttu-id="f85fd-154">Bir izin isteğini iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="f85fd-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="f85fd-155">Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="f85fd-155">Authentication</span></span>](hr-developer-api-authentication.md)