---
title: İzin satın alma ve satma isteği iş akışı oluşturma
description: Dynamics 365 Human Resources'ta izin satın alma ve satma isteklerini tutarlı bir şekilde yönetmek için izin satın alma ve satma isteği iş akışı oluşturun.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d490e0c36ea0e854c5d7afc5b3bf75f6b65e542c
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712634"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="5a43a-103">İzin satın alma ve satma isteği iş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a43a-103">Create a buy and sell leave request workflow</span></span>

<span data-ttu-id="5a43a-104">Dynamics 365 Human Resources'ta izin satın alma ve satma isteklerinizi tutarlı bir şekilde yönetmek için bir iş akışı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5a43a-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="5a43a-105">**İzin satın alma ve satma** iş akışı şunları yapmanızı sağlar:</span><span class="sxs-lookup"><span data-stu-id="5a43a-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="5a43a-106">Görevleri tanımla</span><span class="sxs-lookup"><span data-stu-id="5a43a-106">Define tasks</span></span>
- <span data-ttu-id="5a43a-107">Görevleri kimin tamamlayagerektiğini belirleyin</span><span class="sxs-lookup"><span data-stu-id="5a43a-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="5a43a-108">İstekleri kimlerin onaylayabilir veya reddedilebileceği belirtin</span><span class="sxs-lookup"><span data-stu-id="5a43a-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="5a43a-109">İzin satın alma ve satma isteği iş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a43a-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="5a43a-110">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5a43a-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="5a43a-111">**Kurulum**'un altında, **İnsan kaynakları iş akışlarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="5a43a-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="5a43a-112">**Yeni**'yi, ardından **İzin satın alma ve satma isteği**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="5a43a-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="5a43a-113">**Bu dosya açılsın mı?** ileti kutusu görüntülenirse, **aç**'ı seçin ve şirket kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="5a43a-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="5a43a-114">İzin talepleriniz için iş akışı oluşturmak üzere iş akışı düzenleyicisini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a43a-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="5a43a-115">İş akışlarıyla çalışma hakkında daha fazla bilgi için bkz. [İş akışları genel bakışı oluştur](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="5a43a-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="5a43a-116">Bir izin ve devamsızlık isteği iş akışı veri öğeleri</span><span class="sxs-lookup"><span data-stu-id="5a43a-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="5a43a-117">İzin satın alma ve satma istekleri iş akışlarında koşullu veya otomatik onaylar oluşturmak için aşağıdaki veri öğelerini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="5a43a-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="5a43a-118">**Tutar**</span><span class="sxs-lookup"><span data-stu-id="5a43a-118">**Amount**</span></span>
- <span data-ttu-id="5a43a-119">**İzin satın alma ve satma ilkesi**</span><span class="sxs-lookup"><span data-stu-id="5a43a-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="5a43a-120">**Şirket**</span><span class="sxs-lookup"><span data-stu-id="5a43a-120">**Company**</span></span>
- <span data-ttu-id="5a43a-121">**Oluşturan**</span><span class="sxs-lookup"><span data-stu-id="5a43a-121">**Created by**</span></span>
- <span data-ttu-id="5a43a-122">**Oluşturulma tarihi ve saati**</span><span class="sxs-lookup"><span data-stu-id="5a43a-122">**Created date and time**</span></span>
- <span data-ttu-id="5a43a-123">**Bitiş tarihi**</span><span class="sxs-lookup"><span data-stu-id="5a43a-123">**End date**</span></span>
- <span data-ttu-id="5a43a-124">**İzin türü**</span><span class="sxs-lookup"><span data-stu-id="5a43a-124">**Leave type**</span></span>
- <span data-ttu-id="5a43a-125">**Değiştiren**</span><span class="sxs-lookup"><span data-stu-id="5a43a-125">**Modified by**</span></span>
- <span data-ttu-id="5a43a-126">**Değiştirilme tarihi ve saati**</span><span class="sxs-lookup"><span data-stu-id="5a43a-126">**Modified date and time**</span></span>
- <span data-ttu-id="5a43a-127">**İstek kodu**</span><span class="sxs-lookup"><span data-stu-id="5a43a-127">**Request ID**</span></span>
- <span data-ttu-id="5a43a-128">**Başlangıç tarihi**</span><span class="sxs-lookup"><span data-stu-id="5a43a-128">**Start date**</span></span>
- <span data-ttu-id="5a43a-129">**Durum**</span><span class="sxs-lookup"><span data-stu-id="5a43a-129">**Status**</span></span> 
- <span data-ttu-id="5a43a-130">**Gönderme tarihi**</span><span class="sxs-lookup"><span data-stu-id="5a43a-130">**Submission date**</span></span>
- <span data-ttu-id="5a43a-131">**Gönderen:**</span><span class="sxs-lookup"><span data-stu-id="5a43a-131">**Submitted by**</span></span>
- <span data-ttu-id="5a43a-132">**İnsan kaynakları tarafından gönderildi**</span><span class="sxs-lookup"><span data-stu-id="5a43a-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="5a43a-133">**Yönetici tarafından gönderildi**</span><span class="sxs-lookup"><span data-stu-id="5a43a-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="5a43a-134">**Adına gönderildi**</span><span class="sxs-lookup"><span data-stu-id="5a43a-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="5a43a-135">**Çalışan**</span><span class="sxs-lookup"><span data-stu-id="5a43a-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="5a43a-136">İş akışı örnekleri</span><span class="sxs-lookup"><span data-stu-id="5a43a-136">Workflow examples</span></span>

<span data-ttu-id="5a43a-137">Bu örnekler, şu veri öğelerini kullanarak nasıl farklı iş akışı koşulları oluşturabileceğinizi göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="5a43a-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="5a43a-138">Bu rollerin personel adına gönderdiği izin satın alma ve satma isteklerini otomatik olarak onaylamak için otomatik eylemdeki **İnsan kaynakları tarafından gönderildi** ve **Yönetici tarafından gönderildi** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a43a-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="5a43a-139">Otomatik eylemler hakkında daha fazla bilgi için bkz. [İş akışında onay süreçlerini yapılandırma](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="5a43a-139">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="5a43a-140">İş akışının belirli izin türlerine sahip istekleri nasıl yönlendireceğini kontrol etmek için koşullu deyimde veya otomatik eylemde **İzin türü** kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a43a-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a43a-141">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="5a43a-141">See also</span></span>

[<span data-ttu-id="5a43a-142">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="5a43a-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="5a43a-143">İzin satın alma ve satma ilkelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="5a43a-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
