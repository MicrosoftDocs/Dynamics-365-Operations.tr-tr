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
ms.openlocfilehash: c2e994d11bbd45907a48c1f3955fa751a676a327
ms.sourcegitcommit: e69cfc74e9dbce64ae0e1ab7cd441e5ae6efd4c9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2020
ms.locfileid: "3353700"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="46636-103">Bir izin isteğini iş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="46636-103">Create a leave request workflow</span></span>

<span data-ttu-id="46636-104">Dynamics 365 Human Resources'ta izin isteklerini sürekli olarak yönetmek Için bir izin ve devamsızlık isteği iş akışı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="46636-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="46636-105">**İzin ve devamsızlık** iş akışı şunları yapmanızı sağlar:</span><span class="sxs-lookup"><span data-stu-id="46636-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="46636-106">Görevleri tanımla</span><span class="sxs-lookup"><span data-stu-id="46636-106">Define tasks</span></span>
- <span data-ttu-id="46636-107">Görevleri kimin tamamlayagerektiğini belirleyin</span><span class="sxs-lookup"><span data-stu-id="46636-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="46636-108">İstekleri kimlerin onaylayabilir veya reddedilebileceği belirtin</span><span class="sxs-lookup"><span data-stu-id="46636-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="46636-109">Bir izin ve devamsızlık isteğini iş akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="46636-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="46636-110">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="46636-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="46636-111">**Kurulum**'un altında, **İnsan kaynakları iş akışlarını** seçin.</span><span class="sxs-lookup"><span data-stu-id="46636-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="46636-112">**Yeni**'ı seçin ve sonra **İzin ve devamsızlık isteği**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="46636-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="46636-113">**Bu dosya açılsın mı?** ileti kutusu görüntülenirse, **aç**'ı seçin ve şirket kimlik bilgilerinizle oturum açın.</span><span class="sxs-lookup"><span data-stu-id="46636-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="46636-114">İzin talepleriniz için iş akışı oluşturmak üzere iş akışı düzenleyicisini kullanın.</span><span class="sxs-lookup"><span data-stu-id="46636-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="46636-115">İş akışlarıyla çalışma hakkında daha fazla bilgi için bkz. [İş akışları genel bakışı oluştur](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="46636-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="46636-116">Bir izin ve devamsızlık isteği iş akışı veri öğeleri</span><span class="sxs-lookup"><span data-stu-id="46636-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="46636-117">İzin ve devamsızlık istekleri iş akışlarında koşullu veya otomatik onaylar oluşturmak için aşağıdaki veri öğelerini kullanabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="46636-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="46636-118">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="46636-118">**Comment**</span></span>
- <span data-ttu-id="46636-119">**Şirket**</span><span class="sxs-lookup"><span data-stu-id="46636-119">**Company**</span></span>
- <span data-ttu-id="46636-120">**Oluşturan**</span><span class="sxs-lookup"><span data-stu-id="46636-120">**Created by**</span></span>
- <span data-ttu-id="46636-121">**Oluşturma tarihi ve saati**</span><span class="sxs-lookup"><span data-stu-id="46636-121">**Created date and time**</span></span>
- <span data-ttu-id="46636-122">**Bitiş tarihi**</span><span class="sxs-lookup"><span data-stu-id="46636-122">**End date**</span></span>
- <span data-ttu-id="46636-123">**İzin türü**</span><span class="sxs-lookup"><span data-stu-id="46636-123">**Leave type**</span></span>
- <span data-ttu-id="46636-124">**Değiştiren**</span><span class="sxs-lookup"><span data-stu-id="46636-124">**Modified by**</span></span>
- <span data-ttu-id="46636-125">**Değiştirilme tarihi ve saati**</span><span class="sxs-lookup"><span data-stu-id="46636-125">**Modified date and time**</span></span>
- <span data-ttu-id="46636-126">**Neden kodu**</span><span class="sxs-lookup"><span data-stu-id="46636-126">**Reason code**</span></span>
- <span data-ttu-id="46636-127">**İstek kodu**</span><span class="sxs-lookup"><span data-stu-id="46636-127">**Request ID**</span></span>
- <span data-ttu-id="46636-128">**Başlangıç tarihi**</span><span class="sxs-lookup"><span data-stu-id="46636-128">**Start date**</span></span>
- <span data-ttu-id="46636-129">**Durum**</span><span class="sxs-lookup"><span data-stu-id="46636-129">**Status**</span></span> 
- <span data-ttu-id="46636-130">**Gönderme tarihi**</span><span class="sxs-lookup"><span data-stu-id="46636-130">**Submission date**</span></span>
- <span data-ttu-id="46636-131">**Gönderen:**</span><span class="sxs-lookup"><span data-stu-id="46636-131">**Submitted by**</span></span>
- <span data-ttu-id="46636-132">**İnsan kaynakları tarafından gönderildi**</span><span class="sxs-lookup"><span data-stu-id="46636-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="46636-133">**Yönetici tarafından gönderildi**</span><span class="sxs-lookup"><span data-stu-id="46636-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="46636-134">**Adına gönderildi**</span><span class="sxs-lookup"><span data-stu-id="46636-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="46636-135">**Çalışan**</span><span class="sxs-lookup"><span data-stu-id="46636-135">**Worker**</span></span>
- <span data-ttu-id="46636-136">**Çalışan türü**</span><span class="sxs-lookup"><span data-stu-id="46636-136">**Worker type**</span></span>

<span data-ttu-id="46636-137">Bu örnekler, şu veri öğelerini kullanarak nasıl farklı iş akışı koşulları oluşturabileceğinizi göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="46636-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="46636-138">Hastalık izni isteklerini onay için İK'ya **Cerrahi** neden koduyla yönlendirmek için **Neden kodu**'nu koşullu ifadede kullanın ve diğer tüm neden kodlarını yöneticiye yönlendirin.</span><span class="sxs-lookup"><span data-stu-id="46636-138">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="46636-139">Koşullu ifadeler hakkında daha fazla bilgi için, bkz. [İş akışında koşullu kararları yapılandırma](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="46636-139">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="46636-140">Bu rollerin personel adına gönderdiği izin isteklerini otomatik olarak onaylamak için otomatik eylemdeki **İnsan kaynakları tarafından gönderildi** ve **Yönetici tarafından gönderildi** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="46636-140">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="46636-141">Otomatik eylemler hakkında daha fazla bilgi için bkz. [İş akışında onay süreçlerini yapılandırma](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="46636-141">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="46636-142">İş akışının belirli izin türlerine sahip istekleri nasıl yönlendireceğini kontrol etmek için koşullu deyimde veya otomatik eylemde **İzin türü** kullanın.</span><span class="sxs-lookup"><span data-stu-id="46636-142">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="46636-143">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="46636-143">See also</span></span>

- [<span data-ttu-id="46636-144">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="46636-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
