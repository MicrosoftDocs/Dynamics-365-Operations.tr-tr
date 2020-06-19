---
title: Kazanç yönetimi parametrelerini ayarlama
description: Microsoft Dynamics 365 Human Resources'Ta sosyal haklar yönetimiyle ilgili parametreleri yapılandırın.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430004"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="3ad1b-103">Kazanç yönetimi parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="3ad1b-103">Set Benefits management parameters</span></span>

<span data-ttu-id="3ad1b-104">Microsoft Dynamics 365 Human Resources'ta çıkış planları kurmadan önce, kazançlar yönetimi parametrelerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="3ad1b-105">Bu parametreler varsayılan değerleri, neden kodları ve diğer seçenekleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="3ad1b-106">Genel parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3ad1b-106">Configure general parameters</span></span>

1. <span data-ttu-id="3ad1b-107">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="3ad1b-108">**Genel** sekmesinde, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="3ad1b-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="3ad1b-109">Alan</span><span class="sxs-lookup"><span data-stu-id="3ad1b-109">Field</span></span> | <span data-ttu-id="3ad1b-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ad1b-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3ad1b-111">**Ülke/bölge**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-111">**Country/region**</span></span> | <span data-ttu-id="3ad1b-112">**Ülke/bölge** alanı, posta kodlarının/durumlarının görüntülenme düzenini belirler.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="3ad1b-113">Seçili ülke, aşağı açılan listede ilk olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="3ad1b-114">**Kayıt nedeni kodu**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-114">**Enrollment reason code**</span></span> | <span data-ttu-id="3ad1b-115">Açık kayıt işleme sırasında çalışan planları oluşturulduğunda kullanılacak varsayılan neden kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="3ad1b-116">**İptal nedeni kodu**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-116">**Cancellation reason code**</span></span> | <span data-ttu-id="3ad1b-117">Bir çalışan avantajı planı iptal edildiğinde kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="3ad1b-118">İptal işlemi sırasında bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="3ad1b-119">Gerekirse, kullanıcılar bunu **iptal nedeni kodu** ile değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="3ad1b-120">**Neden kodunu yeniden aç**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-120">**Reopen reason code**</span></span> | <span data-ttu-id="3ad1b-121">Bir çalışan avantajı planı yeniden açıldığında kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="3ad1b-122">İptal işlemi sırasında bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="3ad1b-123">Gerekirse, kullanıcılar bunu **Yeniden açma neden kodu** ile değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="3ad1b-124">**Yaşam olayı neden kodu**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-124">**Life event reason code**</span></span> | <span data-ttu-id="3ad1b-125">Ömür olayı oluştuğunda kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="3ad1b-126">**Oran değişikliği neden kodu**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-126">**Rate change reason code**</span></span> | <span data-ttu-id="3ad1b-127">Güncelleştirme oranı değişimi sürecinde bir çalışan avantajı planının iptal edilmesi ve yeniden açma işlemi sırasında kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="3ad1b-128">Güncelleştirme oranı değişimi işlemi oran ile hangi kayıtların değiştiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="3ad1b-129">**Yeni işe alınan kişi uygun**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-129">**New hire eligible**</span></span> | <span data-ttu-id="3ad1b-130">Yeni işe alımların uygun olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="3ad1b-131">**Yeni işe alma kaydı dönemi**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-131">**New hire enrollment period**</span></span> | <span data-ttu-id="3ad1b-132">Yeni işe alma kaydına izin verildiği zaman dilimi.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="3ad1b-133">**Not**: Bu ayar, plan uygunluğu kuralında ayarladığınız tüm yeni işe alma dönemini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="3ad1b-134">**Yaşam olayları etkin**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-134">**Life events enabled**</span></span> | <span data-ttu-id="3ad1b-135">Yaşam olaylarını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-135">Enables life events.</span></span> |
   | <span data-ttu-id="3ad1b-136">**Eski kazanç formlarını gizle**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="3ad1b-137">Eski kazanç formlarını gizlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="3ad1b-138">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="3ad1b-139">Personel self servisi parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3ad1b-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="3ad1b-140">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="3ad1b-141">**Personel self servisi** sekmesinde, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="3ad1b-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="3ad1b-142">Alan</span><span class="sxs-lookup"><span data-stu-id="3ad1b-142">Field</span></span> | <span data-ttu-id="3ad1b-143">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ad1b-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="3ad1b-144">**Kazanç doğrulaması**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-144">**Benefit verification**</span></span> | <span data-ttu-id="3ad1b-145">Kendi kendine faydaların kullanıma alma sırasında kullanılacak doğrulama metni.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="3ad1b-146">**Görevlileri otomatik olarak seç**</span><span class="sxs-lookup"><span data-stu-id="3ad1b-146">**Auto select designees**</span></span> | <span data-ttu-id="3ad1b-147">Plan seçeneklerine uygunluğuna göre otomatik olarak bağımlılar ve lehdarlar oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="3ad1b-148">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3ad1b-148">Select **Save**.</span></span>
