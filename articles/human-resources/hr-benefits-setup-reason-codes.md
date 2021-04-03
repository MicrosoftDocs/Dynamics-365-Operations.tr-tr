---
title: Neden kodlarını ayarla
description: Dynamics 365 Human Resources bir çalışanın yararlarını nasıl değiştirdiğinizi açıklamak için neden kodları kullanır.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c799a81f38a5dbd5996afbda9529fa83d7fe5cf9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468407"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="eba0e-103">Neden kodlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="eba0e-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eba0e-104">Dynamics 365 Human Resources bir çalışanın yararlarını nasıl değiştirdiğinizi açıklamak için neden kodları kullanır.</span><span class="sxs-lookup"><span data-stu-id="eba0e-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="eba0e-105">Ocak 2021 itibarıyla, neden kodları **Yan hak yönetimi** çalışma alanı yerine **Personel yönetimi** çalışma alanına geçiriliyor.</span><span class="sxs-lookup"><span data-stu-id="eba0e-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="eba0e-106">Daha fazla bilgi için, bkz. [Neden kodlarını el ile Personel yönetimine geçirme](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="eba0e-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="eba0e-107">Neden kodları oluşturma</span><span class="sxs-lookup"><span data-stu-id="eba0e-107">Create reason codes</span></span>

1. <span data-ttu-id="eba0e-108">**Personel yönetimi** çalışma alanında (veya neden kodlarınız henüz geçirilmediyse **Yan hak yönetimi** çalışma alanı), **Bağlantılar**'ı ve ardından **Neden kodları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="eba0e-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="eba0e-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="eba0e-109">Select **New**.</span></span>

3. <span data-ttu-id="eba0e-110">Aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="eba0e-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="eba0e-111">Alan</span><span class="sxs-lookup"><span data-stu-id="eba0e-111">Field</span></span> | <span data-ttu-id="eba0e-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="eba0e-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="eba0e-113">**Neden kodu**</span><span class="sxs-lookup"><span data-stu-id="eba0e-113">**Reason code**</span></span> | <span data-ttu-id="eba0e-114">Bir çalışanın bir kazanç planı kaydını değiştiren nedenini tanımlamak için benzersiz ad.</span><span class="sxs-lookup"><span data-stu-id="eba0e-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="eba0e-115">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="eba0e-115">**Description**</span></span> | <span data-ttu-id="eba0e-116">Neden kodunun açıklaması.</span><span class="sxs-lookup"><span data-stu-id="eba0e-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="eba0e-117">**Uygulanabilir senaryolar** altında, **Yan hak yönetimi**'ni **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="eba0e-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="eba0e-118">(Neden kodlarınız henüz **Personel yönetimi** çalışma alanına geçirilmediyse geçerli değildir.)</span><span class="sxs-lookup"><span data-stu-id="eba0e-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="eba0e-119">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="eba0e-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="eba0e-120">Neden kodlarını Personel yönetimine el ile geçirme</span><span class="sxs-lookup"><span data-stu-id="eba0e-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="eba0e-121">Ocak 2021'de, neden kodları **Yan hak yönetimi** çalışma alanı yerine **Personel yönetimi** çalışma alanına geçiriliyor.</span><span class="sxs-lookup"><span data-stu-id="eba0e-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="eba0e-122">Çoğu neden kodu verileri ortamınıza otomatik olarak geçiş yapacaktır.</span><span class="sxs-lookup"><span data-stu-id="eba0e-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="eba0e-123">Bazı neden kod verileri geçirilemeyebilir.</span><span class="sxs-lookup"><span data-stu-id="eba0e-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="eba0e-124">Örneğin, neden kodları artık en fazla 15 karaktere sahiptir, bu nedenle 15 karakterden uzun herhangi bir neden kodu otomatik olarak geçirilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="eba0e-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="eba0e-125">**Yan hak yönetimi** çalışma alanının **Bağlantılar** sayfasında, geçişle ilgili ve herhangi bir neden kodunun geçirilmemesi hakkında sizi bilgilendiren bir başlık görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="eba0e-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="eba0e-126">Geçiş durumuyla ilgili ayrıntılar için **Neden kodları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="eba0e-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="eba0e-127">[![Neden kodları](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="eba0e-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="eba0e-128">Geçirilemeyen bir neden kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="eba0e-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="eba0e-129">[![Neden kodu geçiş durumu](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="eba0e-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="eba0e-130">**Neden kodunu taşı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="eba0e-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="eba0e-131">[![Neden kodunu taşı](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="eba0e-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="eba0e-132">**Yan hak neden kodu geçişi** bölmesinde, Personel yönetimi neden koduyla eşlemek için iki seçeneğiniz vardır:</span><span class="sxs-lookup"><span data-stu-id="eba0e-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="eba0e-133">Personel yönetiminde var olan bir neden kodunu kullanmak için **Var olan neden kodunu kullan** açılan menüsünün içinden birini seçin.</span><span class="sxs-lookup"><span data-stu-id="eba0e-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="eba0e-134">Personel yönetiminde var olan bir neden kodunu yalnızca başka bir Yan hak yönetimi neden kodu zaten geçiş yapmamışsa kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eba0e-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="eba0e-135">Personel yönetiminde yeni bir neden kodu oluşturmak için **Yeni neden kodu** bölümünde yeni bir neden kodu girin ve sonra **Yeni açıklama**'ya bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="eba0e-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="eba0e-136">[![Personel yönetimi neden koduyla eşleme](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="eba0e-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="eba0e-137">Neden kodları Personel yönetimine geçtikten sonra, bunları Yan hak yönetiminde kullanma seçeneği otomatik olarak **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="eba0e-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="eba0e-138">[![Yan hak yönetiminde neden kodunu kullanma](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="eba0e-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]