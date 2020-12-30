---
title: Bir izin isteğini iş akışı oluşturma
description: Dynamics 365 Human Resources'ta izin isteklerini sürekli olarak yönetmek Için bir izin ve devamsızlık isteği iş akışı oluşturun.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 209f0ec7236778cc0a828102e554b02206b45b73
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420876"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="6fd3d-103">Bir izin isteğini iş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6fd3d-103">Create a leave request workflow</span></span>

<span data-ttu-id="6fd3d-104">Dynamics 365 Human Resources'ta izin isteklerini sürekli olarak yönetmek Için bir izin ve devamsızlık isteği iş akışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="6fd3d-105">**İzin ve devamsızlık** iş akışı şunları yapmanızı sağlar:</span><span class="sxs-lookup"><span data-stu-id="6fd3d-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="6fd3d-106">Görevleri tanımla</span><span class="sxs-lookup"><span data-stu-id="6fd3d-106">Define tasks</span></span>
- <span data-ttu-id="6fd3d-107">Görevleri kimin tamamlayagerektiğini belirleyin</span><span class="sxs-lookup"><span data-stu-id="6fd3d-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="6fd3d-108">İstekleri kimlerin onaylayabilir veya reddedilebileceği belirtin</span><span class="sxs-lookup"><span data-stu-id="6fd3d-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="6fd3d-109">Bir izin ve devamsızlık isteğini iş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6fd3d-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="6fd3d-110">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6fd3d-111">**Kurulum**'un altında, **İnsan kaynakları iş akışlarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="6fd3d-112">**Yeni**'ı seçin ve sonra **İzin ve devamsızlık isteği**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="6fd3d-113">**Bu dosya açılsın mı?** ileti kutusu görüntülenirse, **aç**'ı seçin ve şirket kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="6fd3d-114">İzin talepleriniz için iş akışı oluşturmak üzere iş akışı düzenleyicisini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="6fd3d-115">İş akışlarıyla çalışma hakkında daha fazla bilgi için bkz. [İş akışları genel bakışı oluştur](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="6fd3d-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="6fd3d-116">Bir izin ve devamsızlık isteği iş akışı veri öğeleri</span><span class="sxs-lookup"><span data-stu-id="6fd3d-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="6fd3d-117">İzin ve devamsızlık istekleri iş akışlarında koşullu veya otomatik onaylar oluşturmak için aşağıdaki veri öğelerini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="6fd3d-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="6fd3d-118">**Tutar**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-118">**Amount**</span></span>
- <span data-ttu-id="6fd3d-119">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-119">**Comment**</span></span>
- <span data-ttu-id="6fd3d-120">**Şirket**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-120">**Company**</span></span>
- <span data-ttu-id="6fd3d-121">**Oluşturan**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-121">**Created by**</span></span>
- <span data-ttu-id="6fd3d-122">**Oluşturma tarihi ve saati**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-122">**Created date and time**</span></span>
- <span data-ttu-id="6fd3d-123">**Bitiş tarihi**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-123">**End date**</span></span>
- <span data-ttu-id="6fd3d-124">**İzin türü**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-124">**Leave type**</span></span>
- <span data-ttu-id="6fd3d-125">**Değiştiren**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-125">**Modified by**</span></span>
- <span data-ttu-id="6fd3d-126">**Değiştirilme tarihi ve saati**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-126">**Modified date and time**</span></span>
- <span data-ttu-id="6fd3d-127">**Neden kodu**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-127">**Reason code**</span></span>
- <span data-ttu-id="6fd3d-128">**İstek kodu**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-128">**Request ID**</span></span>
- <span data-ttu-id="6fd3d-129">**Başlangıç tarihi**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-129">**Start date**</span></span>
- <span data-ttu-id="6fd3d-130">**Durum**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-130">**Status**</span></span> 
- <span data-ttu-id="6fd3d-131">**Gönderme tarihi**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-131">**Submission date**</span></span>
- <span data-ttu-id="6fd3d-132">**Gönderen:**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-132">**Submitted by**</span></span>
- <span data-ttu-id="6fd3d-133">**İnsan kaynakları tarafından gönderildi**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="6fd3d-134">**Yönetici tarafından gönderildi**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="6fd3d-135">**Adına gönderildi**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="6fd3d-136">**Çalışan**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-136">**Worker**</span></span>
- <span data-ttu-id="6fd3d-137">**Çalışan türü**</span><span class="sxs-lookup"><span data-stu-id="6fd3d-137">**Worker type**</span></span>

<span data-ttu-id="6fd3d-138">Bu örnekler, şu veri öğelerini kullanarak nasıl farklı iş akışı koşulları oluşturabileceğinizi göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="6fd3d-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="6fd3d-139">Hastalık izni isteklerini onay için İK'ya **Cerrahi** neden koduyla yönlendirmek için **Neden kodu**'nu koşullu ifadede kullanın ve diğer tüm neden kodlarını yöneticiye yönlendirin.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="6fd3d-140">Koşullu ifadeler hakkında daha fazla bilgi için, bkz. [İş akışında koşullu kararları yapılandırma](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="6fd3d-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="6fd3d-141">Bu rollerin personel adına gönderdiği izin isteklerini otomatik olarak onaylamak için otomatik eylemdeki **İnsan kaynakları tarafından gönderildi** ve **Yönetici tarafından gönderildi** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="6fd3d-142">Otomatik eylemler hakkında daha fazla bilgi için bkz. [İş akışında onay süreçlerini yapılandırma](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="6fd3d-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="6fd3d-143">İş akışının belirli izin türlerine sahip istekleri nasıl yönlendireceğini kontrol etmek için koşullu deyimde veya otomatik eylemde **İzin türü** kullanın.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="6fd3d-144">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="6fd3d-144">See also</span></span>

- [<span data-ttu-id="6fd3d-145">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="6fd3d-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
