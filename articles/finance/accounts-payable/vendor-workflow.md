---
title: Satıcı iş akışı
description: Satıcı bilgilerini değiştirin ve onaylamak için iş akışını kullanın.
author: mikefalkner
manager: annbe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Vendor
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: fb89b54b2f9377c216c447590a9434e3ff2d9bac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248147"
---
# <a name="vendor-workflow"></a><span data-ttu-id="e0db3-103">Satıcı iş akışı</span><span class="sxs-lookup"><span data-stu-id="e0db3-103">Vendor workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0db3-104">Satıcı iş akışı kullanıldığında belirli alanlarda yapılan değişiklikler, satıcıya eklenmeden önce onaylanmak üzere iş akışına gönderilir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-104">When the vendor workflow is used, changes that are made to specific fields are sent to the workflow for approval before they are added to the vendor.</span></span>

## <a name="set-up-the-vendor-workflow"></a><span data-ttu-id="e0db3-105">Satıcı iş akışının kurulumu</span><span class="sxs-lookup"><span data-stu-id="e0db3-105">Set up the vendor workflow</span></span>

<span data-ttu-id="e0db3-106">İş akışı özelliğini kullanmak için önce etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-106">Before you can use the workflow feature, you must enable it.</span></span>

1. <span data-ttu-id="e0db3-107">**Borç hesapları \> Kurulum \> Borç hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e0db3-107">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="e0db3-108">**Genel** sekmesinde **Satıcı onayı** hızlı sekmesinde, **Satıcı onaylarını etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e0db3-108">On the **General** tab, on the **Vendor approval** FastTab, set the **Enable vendor approvals** option to **Yes**.</span></span>
3. <span data-ttu-id="e0db3-109">**Veri varlığı davranışı** alanında, veriler içe aktarıldığında kullanılması gereken davranışı seçin:</span><span class="sxs-lookup"><span data-stu-id="e0db3-109">In the **Data entity behavior** field, select the behavior that should be used when data is imported:</span></span>

    - <span data-ttu-id="e0db3-110">**Onay olmadan değişikliklere izin ver**: Veri varlığı, satıcı kaydını iş akışında işlemeden güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-110">**Allow changes without approval** – The data entity can update the vendor record without processing it through the workflow.</span></span>
    - <span data-ttu-id="e0db3-111">**Değişiklikleri reddet**: Satıcı kaydında değişiklik yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="e0db3-111">**Reject changes** – Changes can't be made to the vendor record.</span></span> <span data-ttu-id="e0db3-112">İş akışı için etkinleştirilen alanlarda içe aktarma başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="e0db3-112">The import will fail for the fields that are enabled for the workflow.</span></span>
    - <span data-ttu-id="e0db3-113">**Değişiklik teklifleri oluştur**: İş akışı için etkinleştirilen alanlar dışında tüm alanlar değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-113">**Create change proposals** – All fields will be changed except the fields that are enabled for the workflow.</span></span> <span data-ttu-id="e0db3-114">Bu alanlar için yeni değerler önerilen değişiklikler olarak satıcıya eklenir ve iş akışı otomatik olarak başlatılır.</span><span class="sxs-lookup"><span data-stu-id="e0db3-114">The new values for those fields will be added to the vendor as proposed changes, and the workflow will be started automatically.</span></span>

4. <span data-ttu-id="e0db3-115">Satıcı alanı listesinde, değişiklik yapılmadan önce onaylanması gereken her alan için onay kutusunu **Etkinleştir** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e0db3-115">In the list of vendor fields, select the **Enable** check box for every field that must be approved before the changes can be made.</span></span>
5. <span data-ttu-id="e0db3-116">**Borç hesapları \> Kurulum \> Borç hesapları iş akışları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e0db3-116">Go to **Accounts payable \> Setup \> Accounts payable workflows**.</span></span>
6. <span data-ttu-id="e0db3-117">**Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e0db3-117">Select **New**.</span></span>
7. <span data-ttu-id="e0db3-118">**Önerilen satıcı değişiklikleri iş akışı** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e0db3-118">Select **Proposed vendor changes workflow**.</span></span> 
8. <span data-ttu-id="e0db3-119">İş akışını onay işleminizle eşleşecek şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e0db3-119">Set up the workflow so that it matches your approval process.</span></span> <span data-ttu-id="e0db3-120">**Önerilen satıcı değişikliği için iş akışı onayı** iş akışı onayı öğesi, satıcıda yapılan değişiklikleri uygular.</span><span class="sxs-lookup"><span data-stu-id="e0db3-120">The **Workflow approval for proposed vendor change** workflow approval element will apply the changes to the vendor.</span></span>

## <a name="change-vendor-information-and-submit-the-changes-to-the-workflow"></a><span data-ttu-id="e0db3-121">Satıcı bilgilerini değiştirme ve değişiklikleri iş akışına gönderme</span><span class="sxs-lookup"><span data-stu-id="e0db3-121">Change vendor information and submit the changes to the workflow</span></span>

<span data-ttu-id="e0db3-122">İş akışı için etkinleştirilen bir alanı değiştirdiğinizde **Önerilen değişiklikler** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-122">When you change a field that is enabled for the workflow, the **Proposed changes** page appears.</span></span> <span data-ttu-id="e0db3-123">Bu sayfa alanın orijinal değerini ve girdiğiniz yeni değeri gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-123">This page shows the original value of the field and the new value that you entered.</span></span> <span data-ttu-id="e0db3-124">Değiştirdiğiniz alan orijinal değerine geri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="e0db3-124">The field that you changed is reverted to its original value.</span></span> <span data-ttu-id="e0db3-125">Ayrıca bir durum iletisi ile değişikliklerinizin gönderilmediği bilgisi verilir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-125">A status message also informs you that your changes haven't been submitted.</span></span> 

<span data-ttu-id="e0db3-126">İş akışı için etkinleştirilen bir alanı her değiştirdiğinizde bu alan, **Önerilen değişiklikler** sayfasındaki listeye eklenir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-126">Every time that you change a field that is enabled for the workflow, that field is added to the list on the **Proposed changes** page.</span></span> <span data-ttu-id="e0db3-127">Bir alan için önerilen değeri atmak isterseniz listedeki alanın yanında bulunan **At** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e0db3-127">To discard the proposed value for a field, use the **Discard** button next to the field in the list.</span></span> <span data-ttu-id="e0db3-128">Tüm değişiklikleri atmak için sayfanın alt kısmındaki **Tüm değişiklikleri at** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e0db3-128">To discard all changes, use the **Discard all changes** button at the bottom of the page.</span></span> <span data-ttu-id="e0db3-129">Sayfayı kapatmak için **Tamam** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e0db3-129">Select **OK** to close the page.</span></span>

<span data-ttu-id="e0db3-130">En az bir önerilen değişiklik yaptıktan sonra eylem bölmesinde iki ek sekme görüntülenir: **Önerilen değişiklikler** ve **İş akışı**.</span><span class="sxs-lookup"><span data-stu-id="e0db3-130">After you have at least one proposed change, two additional tabs appear on the action pane: **Proposed changes** and **Workflow**.</span></span>

1. <span data-ttu-id="e0db3-131">**Önerilen değişiklikler** sayfasını seçmek için **Önerilen değişiklikler** öğesini seçin ve değişikliklerinizi gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="e0db3-131">Select **Proposed changes** to open the **Proposed changes** page and review your changes.</span></span>
2. <span data-ttu-id="e0db3-132">Değişiklikleri iş akışına göndermek için **İş akışı \> Gönder** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e0db3-132">Select **Workflow \> Submit to submit the changes to workflow**.</span></span>

    <span data-ttu-id="e0db3-133">Sayfadaki durum **Değişiklikler onay bekliyor** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-133">The status on the page is changed to **Changes pending approval**.</span></span>

<span data-ttu-id="e0db3-134">İş akışı, standart iş akışı sürecini takip eder.</span><span class="sxs-lookup"><span data-stu-id="e0db3-134">The workflow follows the standard workflow process.</span></span> <span data-ttu-id="e0db3-135">Onaylayan, **Önerilen değişiklikler** sayfasındaki değişiklikleri inceleyebileceği ve **İş akışı \> Onayla**'yı seçerek iş akışını onaylayabileceği **Satıcı** sayfasına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-135">The approver is directed to the **Vendor** page where the changes can be reviewed on the **Proposed changes** page and then select **Workflow \> Approve** to approve the workflow.</span></span> <span data-ttu-id="e0db3-136">Tüm onaylar tamamlandığında, alanlar önerdiğiniz değerlerle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e0db3-136">After all approvals are completed, the fields are updated with the values that you proposed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]