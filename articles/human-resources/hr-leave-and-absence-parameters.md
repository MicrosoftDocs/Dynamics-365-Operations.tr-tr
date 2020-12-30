---
title: Bırakma ve devamsızlık parametrelerini konfigüre et
description: Dynamics 365 Human Resources'ta izin ve devamsızlık için insan kaynakları parametrelerini tanımlayın.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
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
ms.openlocfilehash: e1b2de94f9d9ac1ada16b6ef0e7628edbc9d683f
ms.sourcegitcommit: ffb5998e611b83c2e4f98323f39e3e8f6419c652
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/02/2020
ms.locfileid: "4421027"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="b66f3-103">Bırakma ve devamsızlık parametrelerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="b66f3-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="b66f3-104">Dynamics 365 Human Resources'ta , izin ve devamsızlık planlarını ayarlamadan önce, aşağıdakiler dahil olmak üzere ilgili tüm insan kaynakları parametrelerinin ayarlarını doğrulamak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="b66f3-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="b66f3-105">İzin talepleri için numara serisi</span><span class="sxs-lookup"><span data-stu-id="b66f3-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="b66f3-106">Aile sağlık ve izin Yasası (FMLA) ayarları</span><span class="sxs-lookup"><span data-stu-id="b66f3-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="b66f3-107">İzin ve devamsızlık talepleri için çalışan self servis ayarları</span><span class="sxs-lookup"><span data-stu-id="b66f3-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="b66f3-108">İzin ve devamsızlık parametreleri</span><span class="sxs-lookup"><span data-stu-id="b66f3-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="b66f3-109">İnsan kaynakları parametrelerini görüntüle ve değiştir</span><span class="sxs-lookup"><span data-stu-id="b66f3-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="b66f3-110">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b66f3-111">**Kurulum**'un altında, **İnsan kaynakları parametrelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="b66f3-112">**Numara serileri** sekmesinde, **izin talebi kodunun** **numara serisi kodunu** doğrulayın ve gerekli değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="b66f3-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="b66f3-113">Bu ayar, isteklere izin vermek üzere otomatik olarak kimlik atamak için kullanılan sırayı belirler.</span><span class="sxs-lookup"><span data-stu-id="b66f3-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="b66f3-114">**FMLA** sekmesinde, FMLA ayarlarını doğrulayın ve gerektiği şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="b66f3-115">**Çalışan self servis** sekmesinde, yöneticilerin çalışanlar adına bırakma ve devamsızlık talepleri girip giremeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="b66f3-116">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="b66f3-117">Şirketler arasında ayrılma ve devamsızlıkların görüntülenmesi Şu anda önizleme modunda.</span><span class="sxs-lookup"><span data-stu-id="b66f3-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="b66f3-118">Bırak ve devamsızlık seçeneğini görüntülemek için bunu **korumalı alan** ortamınızda etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b66f3-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="b66f3-119">Önizleme özelliklerini etkinleştirme hakkında daha fazla bilgi edinmek için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="b66f3-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="b66f3-120">İnsan kaynakları paylaşılan parametrelerini görüntüle ve değiştir</span><span class="sxs-lookup"><span data-stu-id="b66f3-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="b66f3-121">**Personel yönetimi** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b66f3-122">**Kurulum**'un altında, **İnsan kaynakları paylaşılan parametrelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="b66f3-123">**Gelişmiş erişim** sekmesinde, Şirket genelinde görüntülenenler görünümüne izin vermek için **şirketler arası bırak görünümünü etkinleştir** için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="b66f3-124">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="b66f3-125">İzin ve devamsızlık parametrelerini görüntüleme ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="b66f3-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="b66f3-126">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b66f3-127">**Kurulum** altında, **İzin ve devamsızlık parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="b66f3-128">**Genel** sekmesinde, aşağıdaki parametreleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b66f3-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="b66f3-129">**İzin ve devamsızlık birimini** saat veya gün olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b66f3-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="b66f3-130">Gün olarak ayarlarsanız, çalışanların izin isteklerinde günün ilk veya ikinci yarısını seçmelerine izin vermek için **Yarım tüm tanımını etkinleştir**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b66f3-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="b66f3-131">Tahakkuk oranlarının hizmet ayları kullanılarak izin planları için geçerli olacağı zamanı ayarlamak için **Hizmet ayları geçerlilik tarihi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="b66f3-132">Bugün veya tahakkuk dönemi itibarıyla bakiyeyi görüntülemek için **Bakiye hesaplaması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="b66f3-133">**Bugün itibarıyla bakiye**'yi seçerseniz, bakiye bugün itibarıyla tahakkukların, ayarlamaların ve isteklerin toplamını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b66f3-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="b66f3-134">**Tahakkuk dönemi itibarıyla bakiye**'yi seçerseniz bakiye, izin planındaki sıklık tarafından tanımlanan tahakkuk dönemi itibarıyla tüm tahakkukların, ayarlamaların ve isteklerin toplamını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b66f3-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="b66f3-135">Sona erme tarihini ilerletme toplu işi için başlangıç zamanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="b66f3-136">**Personelin izin satın almasına izin ver** ve **Personelin izin satmasına izin ver** için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="b66f3-137">Bu seçenekler için **Evet**'i seçerseniz izin satın alma ve satma ilkeleri oluşturabilir ve personelin izin satın alma ve satma istekleri göndermesine olanak tanıyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b66f3-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="b66f3-138">Takvim parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b66f3-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="b66f3-139">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b66f3-140">**Kurulum** altında, **İzin ve devamsızlık parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="b66f3-141">**Takvim** sekmesinde, takvim ayarlarını gerektiği şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="b66f3-142">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b66f3-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b66f3-143">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b66f3-143">See also</span></span>

- [<span data-ttu-id="b66f3-144">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="b66f3-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
