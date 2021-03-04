---
title: Müşteri iş akışı
description: Bu konu müşteri iş akışıyla ilgili bilgiler sağlar. Bir müşteri için belirli alanları değiştirebilir ve müşteri için eklenmeden önce iş akışı kullanarak değişiklikleri onaylanmak üzere gönderebilirsiniz.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a74b8ed226c4e13c8684fe86d4dca7236a84040e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012200"
---
# <a name="customer-workflow"></a><span data-ttu-id="1df85-104">Müşteri iş akışı</span><span class="sxs-lookup"><span data-stu-id="1df85-104">Customer workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1df85-105">Müşteri iş akışı, sürüm 8.0.4'e eklendi.</span><span class="sxs-lookup"><span data-stu-id="1df85-105">The customer workflow has been added to version 8.0.4.</span></span> <span data-ttu-id="1df85-106">Bir müşteri için belirli alanları değiştirebilir ve müşteri için eklenmeden önce iş akışı kullanarak değişiklikleri onaylanmak üzere gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1df85-106">You can change specific fields for a customer and then send those changes for approval by using the workflow before they are added to the customer.</span></span>

## <a name="set-up-the-customer-workflow"></a><span data-ttu-id="1df85-107">Müşteri iş akışı ayarlama</span><span class="sxs-lookup"><span data-stu-id="1df85-107">Set up the customer workflow</span></span>

<span data-ttu-id="1df85-108">Müşteri iş akışı özelliğini kullanabilmek için etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1df85-108">Before you can use the customer workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="1df85-109">**Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="1df85-109">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="1df85-110">Özelliği etkinleştirmek için **Genel** sekmesinde, **Müşteri onayı** hızlı sekmesinde **Müşteri onaylarını etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1df85-110">On the **General** tab, on the **Customer approval** FastTab, set the **Enable customer approvals** option to **Yes** to enable the feature.</span></span>
3. <span data-ttu-id="1df85-111">**Veri varlığı davranışı** alanında, veriler içe aktarıldığında veri varlıklarının kullanması gereken davranışı seçin:</span><span class="sxs-lookup"><span data-stu-id="1df85-111">In the **Data entity behavior** field, select the behavior that the data entities should use when data is imported:</span></span>

    - <span data-ttu-id="1df85-112">**Değişikliklere onay olmadan izin ver**: Varlık müşteri kaydını iş akışıyla işlemeden güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1df85-112">**Allow changes without approval** – An entity can update the customer record without processing it through the workflow.</span></span>
    - <span data-ttu-id="1df85-113">**Değişiklikleri reddet**: Müşteri kaydında değişiklik yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="1df85-113">**Reject changes** – Changes can't be made to the customer record.</span></span> <span data-ttu-id="1df85-114">İş akışı için etkinleştirilen alanlar içe aktarılamaz.</span><span class="sxs-lookup"><span data-stu-id="1df85-114">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="1df85-115">**Değişiklik önerileri oluştur**: İş akışı için etkinleştirilenler dışındaki tüm alanlar değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="1df85-115">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="1df85-116">Bu alanlara ilişkin yeni değerler müşteri kaydına önerilen değişiklikler olarak eklenir ve iş akışı otomatik olarak başlatılır.</span><span class="sxs-lookup"><span data-stu-id="1df85-116">The new values for those fields will be added to the customer as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="1df85-117">Müşteri alanları listesinde, değişiklik yapılmadan önce onaylanması gereken her alan için **Etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1df85-117">In the list of customer fields, select then **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="1df85-118">**Alacak hesapları \> Kurulum \> Alacak hesapları iş akışları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1df85-118">Go to **Accounts receivable \> Setup \> Accounts receivable workflows**.</span></span>
6. <span data-ttu-id="1df85-119">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1df85-119">Select **New**.</span></span>
7. <span data-ttu-id="1df85-120">**Önerilen müşteri değişikliği iş akışı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1df85-120">Select **Proposed customer change workflow**.</span></span> 
8. <span data-ttu-id="1df85-121">İş akışını onay sürecinizle eşleşecek şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1df85-121">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="1df85-122">**Önerilen müşteri değişikliği için iş akışı onayı** iş akışı onayı öğesi müşteri için değişiklikleri uygular.</span><span class="sxs-lookup"><span data-stu-id="1df85-122">The **Workflow approval for proposed customer change** workflow approval element will apply the changes to the customer.</span></span>

## <a name="change-customer-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="1df85-123">Müşteri bilgilerini değiştirme ve değişiklikleri iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="1df85-123">Change customer information and submit the changes to the workflow</span></span>

<span data-ttu-id="1df85-124">İş akışı için etkinleştirilen bir alanı değiştirdiğinizde **Önerilen değişiklikler** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1df85-124">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="1df85-125">Bu sayfa alanın orijinal değerini ve girdiğiniz yeni değeri gösterir.</span><span class="sxs-lookup"><span data-stu-id="1df85-125">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="1df85-126">Değiştirdiğiniz alan orijinal değerine geri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="1df85-126">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="1df85-127">Sayfadaki durum iletisi değişikliklerinizin gönderilmediği konusunda sizi bilgilendirir.</span><span class="sxs-lookup"><span data-stu-id="1df85-127">A status message on the page informs you that your changes haven't been submitted.</span></span>

<span data-ttu-id="1df85-128">İş akışı için etkinleştirilen bir alanı her değiştirdiğinizde, bu alan önerilen değişiklikler sayfasına eklenir.</span><span class="sxs-lookup"><span data-stu-id="1df85-128">Every time that you change a field that is enabled for the workflow, that field is added to the list of proposed changes.</span></span> <span data-ttu-id="1df85-129">Bir alan için önerilen değişikliği atmak üzere listede alanın yanındaki **At** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1df85-129">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="1df85-130">Tüm değişiklikleri atmak için sayfanın alt kısmındaki **Tüm değişiklikleri at** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1df85-130">To discard all changes, use the **Discard all change** button at the bottom of the page.</span></span> <span data-ttu-id="1df85-131">Sayfayı kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1df85-131">Select **OK** to close the page.</span></span>

<span data-ttu-id="1df85-132">En az bir önerilen değişikliğiniz olduğunda, Eylem Bölmesinde iki ek menü görüntülenir: **Önerilen değişiklikler** ve **İş akışı**.</span><span class="sxs-lookup"><span data-stu-id="1df85-132">After you have at least one proposed change, two additional menus appear on the Action Pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="1df85-133">**Önerilen değişiklikler** sayfasını açmak için **Önerilen değişiklikler**'i seçin ve değişikliklerinizi gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="1df85-133">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="1df85-134">Değişiklikleri iş akışına göndermek için **İş akışı \> Gönder**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1df85-134">Select **Workflow \> Submit** to submit the changes to the workflow.</span></span>

    <span data-ttu-id="1df85-135">Sayfadaki durum **Değişiklikler onay bekliyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="1df85-135">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="1df85-136">İş akışı, uygulamadaki standart iş akışı sürecini izler.</span><span class="sxs-lookup"><span data-stu-id="1df85-136">The workflow follows the standard workflow process in the application.</span></span> <span data-ttu-id="1df85-137">Onaylayan, **Önerilen değişiklikler** sayfasındaki değişiklikleri inceleyebileceği ve **İş akışı \> Onayla**'yı seçerek iş akışını onaylayabileceği **Müşteri** sayfasına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="1df85-137">The approver is directed to the **Customer** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="1df85-138">Tüm onaylar tamamlandığında, alanlar önerdiğiniz değerlerle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1df85-138">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>
