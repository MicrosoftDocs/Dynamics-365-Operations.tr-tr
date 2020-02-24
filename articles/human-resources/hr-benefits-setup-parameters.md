---
title: Kazanç yönetimi parametrelerini ayarlama
description: Microsoft Dynamics 365 Human Resources'Ta sosyal haklar yönetimiyle ilgili parametreleri yapılandırın.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010871"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="bf0e5-103">Kazanç yönetimi parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="bf0e5-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="bf0e5-104">Microsoft Dynamics 365 Human Resources'ta çıkış planları kurmadan önce, kazançlar yönetimi parametrelerini konfigüre etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="bf0e5-105">Bu parametreler varsayılan değerleri, neden kodları ve diğer seçenekleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="bf0e5-106">Genel parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bf0e5-106">Configure general parameters</span></span>

1. <span data-ttu-id="bf0e5-107">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="bf0e5-108">**Genel** sekmesinde, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="bf0e5-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="bf0e5-109">Alan</span><span class="sxs-lookup"><span data-stu-id="bf0e5-109">Field</span></span> | <span data-ttu-id="bf0e5-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf0e5-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bf0e5-111">**Ülke/bölge**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-111">**Country/region**</span></span> | <span data-ttu-id="bf0e5-112">**Ülke/bölge** alanı, posta kodlarının/durumlarının görüntülenme düzenini belirler.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="bf0e5-113">Seçili ülke, aşağı açılan listede ilk olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="bf0e5-114">**Kayıt nedeni kodu**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-114">**Enrollment reason code**</span></span> | <span data-ttu-id="bf0e5-115">Açık kayıt işleme sırasında çalışan planları oluşturulduğunda kullanılacak varsayılan neden kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="bf0e5-116">**İptal nedeni kodu**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-116">**Cancellation reason code**</span></span> | <span data-ttu-id="bf0e5-117">Bir çalışan avantajı planı iptal edildiğinde kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="bf0e5-118">İptal işlemi sırasında bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="bf0e5-119">Gerekirse, kullanıcılar bunu **iptal nedeni kodu** ile değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="bf0e5-120">**Neden kodunu yeniden aç**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-120">**Reopen reason code**</span></span> | <span data-ttu-id="bf0e5-121">Bir çalışan avantajı planı yeniden açıldığında kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="bf0e5-122">İptal işlemi sırasında bir iletişim kutusunda görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="bf0e5-123">Gerekirse, kullanıcılar bunu **Yeniden açma neden kodu** ile değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="bf0e5-124">**Yaşam olayı neden kodu**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-124">**Life event reason code**</span></span> | <span data-ttu-id="bf0e5-125">Ömür olayı oluştuğunda kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="bf0e5-126">**Oran değişikliği neden kodu**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-126">**Rate change reason code**</span></span> | <span data-ttu-id="bf0e5-127">Güncelleştirme oranı değişimi sürecinde bir çalışan avantajı planının iptal edilmesi ve yeniden açma işlemi sırasında kullanılacak neden kodu.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="bf0e5-128">Güncelleştirme oranı değişimi işlemi oran ile hangi kayıtların değiştiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="bf0e5-129">**Yeni işe alınan kişi uygun**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-129">**New hire eligible**</span></span> | <span data-ttu-id="bf0e5-130">Yeni işe alımların uygun olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="bf0e5-131">**Yeni işe alma kaydı dönemi**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-131">**New hire enrollment period**</span></span> | <span data-ttu-id="bf0e5-132">Yeni işe alma kaydına izin verildiği zaman dilimi.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="bf0e5-133">**Not**: Bu ayar, plan uygunluğu kuralında ayarladığınız tüm yeni işe alma dönemini geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="bf0e5-134">**Yıllık maaş iyileştirmesi**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="bf0e5-135">**İstihdam avantajı ayrıntılarında** **yıllık maaş tutarının** otomatik olarak hesaplayıp hesaplamayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="bf0e5-136">Çalışanın **sabit maaş ödeme oranını**, **ortalama saatleri** ve **ödeme sıklığını** temel alır.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="bf0e5-137">**Ortalama saatler** x **sabit ödeme oranı** x **ödeme sıklığı** (ödeme dönemlerinin sayısı) = **yıllık kazanç maaş**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="bf0e5-138">**Ortalama saatlerdeki** değerlerden herhangi biri, **sabit maaş ödeme oranı** veya **ödeme sıklığı** alanlarının değişmesi durumunda, sistem, çalışanın **yıllık kazanç** tutarını değiştirilen değerlere göre otomatik olarak yeniden hesaplar.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="bf0e5-139">Sistem, değişikliğin gerçekleştiği tarih ve saati tam olarak tanımlamak için **yürürlülük tarihi** kaydı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="bf0e5-140">Gerekirse, **yıllık kazancın maaş** tutarını el ile düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="bf0e5-141">**Yaşam olayları etkin**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-141">**Life events enabled**</span></span> | <span data-ttu-id="bf0e5-142">Yaşam olaylarını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-142">Enables life events.</span></span> |
   | <span data-ttu-id="bf0e5-143">**Eski kazanç formlarını gizle**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="bf0e5-144">Eski kazanç formlarını gizlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="bf0e5-145">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="bf0e5-146">Personel self servisi parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bf0e5-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="bf0e5-147">**Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="bf0e5-148">**Personel self servisi** sekmesinde, aşağıdaki alanların değerleri belirtin:</span><span class="sxs-lookup"><span data-stu-id="bf0e5-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="bf0e5-149">Alan</span><span class="sxs-lookup"><span data-stu-id="bf0e5-149">Field</span></span> | <span data-ttu-id="bf0e5-150">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf0e5-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bf0e5-151">**Kazanç doğrulaması**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-151">**Benefit verification**</span></span> | <span data-ttu-id="bf0e5-152">Kendi kendine faydaların kullanıma alma sırasında kullanılacak doğrulama metni.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="bf0e5-153">**Görevlileri otomatik olarak seç**</span><span class="sxs-lookup"><span data-stu-id="bf0e5-153">**Auto select designees**</span></span> | <span data-ttu-id="bf0e5-154">Plan seçeneklerine uygunluğuna göre otomatik olarak bağımlılar ve lehdarlar oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="bf0e5-155">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bf0e5-155">Select **Save**.</span></span>
