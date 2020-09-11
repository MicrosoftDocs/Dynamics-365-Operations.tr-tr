---
title: Bırakma ve devamsızlık parametrelerini konfigüre et
description: Dynamics 365 Human Resources'ta izin ve devamsızlık için insan kaynakları parametrelerini tanımlayın.
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712388"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="7f5fc-103">Bırakma ve devamsızlık parametrelerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="7f5fc-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="7f5fc-104">Dynamics 365 Human Resources'ta , izin ve devamsızlık planlarını ayarlamadan önce, aşağıdakiler dahil olmak üzere ilgili tüm insan kaynakları parametrelerinin ayarlarını doğrulamak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="7f5fc-105">İzin talepleri için numara serisi</span><span class="sxs-lookup"><span data-stu-id="7f5fc-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="7f5fc-106">Aile sağlık ve izin Yasası (FMLA) ayarları</span><span class="sxs-lookup"><span data-stu-id="7f5fc-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="7f5fc-107">İzin ve devamsızlık talepleri için çalışan self servis ayarları</span><span class="sxs-lookup"><span data-stu-id="7f5fc-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="7f5fc-108">İzin ve devamsızlık parametreleri</span><span class="sxs-lookup"><span data-stu-id="7f5fc-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="7f5fc-109">İnsan kaynakları parametrelerini görüntüle ve değiştir</span><span class="sxs-lookup"><span data-stu-id="7f5fc-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="7f5fc-110">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7f5fc-111">**Kurulum**'un altında, **İnsan kaynakları parametrelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="7f5fc-112">**Numara serileri** sekmesinde, **izin talebi kodunun** **numara serisi kodunu** doğrulayın ve gerekli değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="7f5fc-113">Bu ayar, isteklere izin vermek üzere otomatik olarak kimlik atamak için kullanılan sırayı belirler.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="7f5fc-114">**FMLA** sekmesinde, FMLA ayarlarını doğrulayın ve gerektiği şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="7f5fc-115">**Çalışan self servis** sekmesinde, yöneticilerin çalışanlar adına bırakma ve devamsızlık talepleri girip giremeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="7f5fc-116">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="7f5fc-117">İzin ve devamsızlık parametrelerini görüntüleme ve değiştirme</span><span class="sxs-lookup"><span data-stu-id="7f5fc-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="7f5fc-118">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7f5fc-119">**Kurulum** altında, **İzin ve devamsızlık parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="7f5fc-120">**Genel** sekmesinde, aşağıdaki parametreleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="7f5fc-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="7f5fc-121">**İzin ve devamsızlık birimini** saat veya gün olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="7f5fc-122">Gün olarak ayarlarsanız, çalışanların izin isteklerinde günün ilk veya ikinci yarısını seçmelerine izin vermek için **Yarım tüm tanımını etkinleştir**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="7f5fc-123">Tahakkuk oranlarının hizmet ayları kullanılarak izin planları için geçerli olacağı zamanı ayarlamak için **Hizmet ayları geçerlilik tarihi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="7f5fc-124">Bugün veya tahakkuk dönemi itibarıyla bakiyeyi görüntülemek için **Bakiye hesaplaması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="7f5fc-125">**Bugün itibarıyla bakiye**'yi seçerseniz, bakiye bugün itibarıyla tahakkukların, ayarlamaların ve isteklerin toplamını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="7f5fc-126">**Tahakkuk dönemi itibarıyla bakiye**'yi seçerseniz bakiye, izin planındaki sıklık tarafından tanımlanan tahakkuk dönemi itibarıyla tüm tahakkukların, ayarlamaların ve isteklerin toplamını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="7f5fc-127">Sona erme tarihini ilerletme toplu işi için başlangıç zamanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="7f5fc-128">**Personelin izin satın almasına izin ver** ve **Personelin izin satmasına izin ver** için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="7f5fc-129">Bu seçenekler için **Evet**'i seçerseniz izin satın alma ve satma ilkeleri oluşturabilir ve personelin izin satın alma ve satma istekleri göndermesine olanak tanıyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="7f5fc-130">Takvim parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7f5fc-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="7f5fc-131">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7f5fc-132">**Kurulum** altında, **İzin ve devamsızlık parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="7f5fc-133">**Takvim** sekmesinde, takvim ayarlarını gerektiği şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="7f5fc-134">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f5fc-135">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="7f5fc-135">See also</span></span>

- [<span data-ttu-id="7f5fc-136">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="7f5fc-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
