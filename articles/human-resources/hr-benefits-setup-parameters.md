---
title: Tüm şirketler için Kazanç yönetimi ve Personel self servisi parametrelerini ayarlama
description: Microsoft Dynamics 365 Human Resources'ta Kazanç yönetimi ve Personel self servisi için parametreleri yapılandırma.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 10f5310ba4feba4a196d02c406ff3217637e447e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791498"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="025c8-103">Tüm şirketler için Kazanç yönetimi ve Personel self servisi parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="025c8-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="025c8-104">Microsoft Dynamics 365 Human Resources'ta kazanç planları kurmadan önce, kazançlar yönetimi parametrelerini yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="025c8-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="025c8-105">Bu parametreler varsayılan değerleri, neden kodları ve diğer seçenekleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="025c8-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="025c8-106">Genel parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="025c8-106">Configure general parameters</span></span>

1. <span data-ttu-id="025c8-107">**Kazanç yönetimi** çalışma alanında, **Kurulum** altında **İnsan Kaynakları Paylaşılan Parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="025c8-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="025c8-108">**Kazanç yönetimi** sekmesinde, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="025c8-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="025c8-109">Alan</span><span class="sxs-lookup"><span data-stu-id="025c8-109">Field</span></span> | <span data-ttu-id="025c8-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="025c8-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="025c8-111">**Ülke/bölge**</span><span class="sxs-lookup"><span data-stu-id="025c8-111">**Country/region**</span></span> | <span data-ttu-id="025c8-112">**Ülke/bölge** alanı, posta kodlarının/durumlarının görüntülenme düzenini belirler.</span><span class="sxs-lookup"><span data-stu-id="025c8-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="025c8-113">Seçili ülke, aşağı açılan listede ilk olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="025c8-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="025c8-114">**Kayıt nedeni kodu**</span><span class="sxs-lookup"><span data-stu-id="025c8-114">**Enrollment reason code**</span></span> | <span data-ttu-id="025c8-115">Açık kayıt işleme sırasında çalışan planları oluşturulduğunda kullanılacak varsayılan neden kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="025c8-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="025c8-116">**İptal nedeni kodu**</span><span class="sxs-lookup"><span data-stu-id="025c8-116">**Cancellation reason code**</span></span> | <span data-ttu-id="025c8-117">Bir çalışan avantajı planı iptal edildiğinde kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="025c8-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="025c8-118">İptal işlemi sırasında bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="025c8-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="025c8-119">Gerekirse, kullanıcılar bunu **iptal nedeni kodu** ile değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="025c8-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="025c8-120">**Neden kodunu yeniden aç**</span><span class="sxs-lookup"><span data-stu-id="025c8-120">**Reopen reason code**</span></span> | <span data-ttu-id="025c8-121">Bir çalışan avantajı planı yeniden açıldığında kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="025c8-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="025c8-122">İptal işlemi sırasında bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="025c8-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="025c8-123">Gerekirse, kullanıcılar bunu **Yeniden açma neden kodu** ile değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="025c8-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="025c8-124">**Yaşam olayı neden kodu**</span><span class="sxs-lookup"><span data-stu-id="025c8-124">**Life event reason code**</span></span> | <span data-ttu-id="025c8-125">Ömür olayı oluştuğunda kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="025c8-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="025c8-126">**Oran değişikliği neden kodu**</span><span class="sxs-lookup"><span data-stu-id="025c8-126">**Rate change reason code**</span></span> | <span data-ttu-id="025c8-127">Güncelleştirme oranı değişimi sürecinde bir çalışan avantajı planının iptal edilmesi ve yeniden açma işlemi sırasında kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="025c8-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="025c8-128">Güncelleştirme oranı değişimi işlemi oran ile hangi kayıtların değiştiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="025c8-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="025c8-129">**Kazanç yıllık maaş**</span><span class="sxs-lookup"><span data-stu-id="025c8-129">**Benefits annual salary**</span></span> | <span data-ttu-id="025c8-130">Bir personel için **Kazanç yıllık maaş** tutarını ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="025c8-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="025c8-131">İnsan Kaynakları, karşılama tutarlarını belirlerken yıllık sabit ücret tutarı yerine **Kazançlar yıllık maaş** alanını kullanacaktır.</span><span class="sxs-lookup"><span data-stu-id="025c8-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="025c8-132">**Yeni işe alınan kişi uygun**</span><span class="sxs-lookup"><span data-stu-id="025c8-132">**New hire eligible**</span></span> | <span data-ttu-id="025c8-133">Yeni işe alımların uygun olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="025c8-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="025c8-134">**Yeni işe alma kaydı dönemi**</span><span class="sxs-lookup"><span data-stu-id="025c8-134">**New hire enrollment period**</span></span> | <span data-ttu-id="025c8-135">Yeni işe alma kaydına izin verildiği zaman dilimi.</span><span class="sxs-lookup"><span data-stu-id="025c8-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="025c8-136">**Not**: Bu ayar, plan uygunluğu kuralında ayarladığınız tüm yeni işe alma dönemini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="025c8-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="025c8-137">**Varsayılan ödeme sıklığı**</span><span class="sxs-lookup"><span data-stu-id="025c8-137">**Default pay frequency**</span></span> | <span data-ttu-id="025c8-138">Yeni çalışanlar eklendiğinde kullanılacak varsayılan ödeme sıklığı.</span><span class="sxs-lookup"><span data-stu-id="025c8-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="025c8-139">**Yaşam olayları etkin**</span><span class="sxs-lookup"><span data-stu-id="025c8-139">**Life events enabled**</span></span> | <span data-ttu-id="025c8-140">Yaşam olaylarını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="025c8-140">Enables life events.</span></span> |
   | <span data-ttu-id="025c8-141">**Eski kazanç formlarını gizle**</span><span class="sxs-lookup"><span data-stu-id="025c8-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="025c8-142">Eski kazanç formlarını gizlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="025c8-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="025c8-143">**Kazanç doğrulaması**</span><span class="sxs-lookup"><span data-stu-id="025c8-143">**Benefit verification**</span></span> | <span data-ttu-id="025c8-144">Kendi kendine faydaların kullanıma alma sırasında kullanılacak doğrulama metni.</span><span class="sxs-lookup"><span data-stu-id="025c8-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="025c8-145">**Görevlileri otomatik olarak seç**</span><span class="sxs-lookup"><span data-stu-id="025c8-145">**Auto select designees**</span></span> | <span data-ttu-id="025c8-146">Plan seçeneklerine uygunluğuna göre otomatik olarak bağımlılar ve lehdarlar oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="025c8-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="025c8-147">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="025c8-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="025c8-148">Personel self servisi parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="025c8-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="025c8-149">**Kazanç yönetimi** çalışma alanında, **Kurulum** altında **İnsan Kaynakları Parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="025c8-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="025c8-150">**Kazanç yönetimi** sekmesinde, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="025c8-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="025c8-151">Alan</span><span class="sxs-lookup"><span data-stu-id="025c8-151">Field</span></span> | <span data-ttu-id="025c8-152">Tanım</span><span class="sxs-lookup"><span data-stu-id="025c8-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="025c8-153">**Kazanç doğrulaması**</span><span class="sxs-lookup"><span data-stu-id="025c8-153">**Benefit verification**</span></span> | <span data-ttu-id="025c8-154">Kendi kendine faydaların kullanıma alma sırasında kullanılacak doğrulama metni.</span><span class="sxs-lookup"><span data-stu-id="025c8-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="025c8-155">**Görevlileri otomatik olarak seç**</span><span class="sxs-lookup"><span data-stu-id="025c8-155">**Auto select designees**</span></span> | <span data-ttu-id="025c8-156">Plan seçeneklerine uygunluğuna göre otomatik olarak bağımlılar ve lehdarlar oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="025c8-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="025c8-157">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="025c8-157">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]