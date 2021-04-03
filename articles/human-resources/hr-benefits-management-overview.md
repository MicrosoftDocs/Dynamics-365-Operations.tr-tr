---
title: Kazanç yönetimine genel bakış
description: Dynamics 365 Human Resources'taki Kazanç yönetimi özelliğine genel bakış. Çalışanlarınızı kullanımı kolay bir çevrimiçi deneyim sayesinde çalışanlarınızın genişletilmiş sosyal haklar seçeneklerini sunun.
author: andreabichsel
manager: tfehr
ms.date: 09/17/2020
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
ms.openlocfilehash: ba6623102431eb45bf5d0c96b6583615663d1081
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464338"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="9b0a2-104">Kazanç yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="9b0a2-104">Benefits management overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9b0a2-105">Rekabet edebilir durumda kalmak için, en iyi çalışanlarınızı ele almak ve bunları korumak amacıyla zengin bir avantaj kümesi sunmalısınız.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="9b0a2-106">Tıp ve diş kapsamı gibi standart avantajlara ek olarak, benimseme yardımı, dinlenme programları ve giyme gibi genişletilmiş hizmetler de sunmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="9b0a2-107">Microsoft Dynamics 365 Human Resources'taki Kazanç yönetimi, çok çeşitli kazanç seçeneklerini destekleyen esnek bir çözüm sağlar.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="9b0a2-108">İnsan Kaynakları ayrıca, tekliflerinizi gösteren kullanımı kolay bir çalışan deneyimi de içerir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="9b0a2-109">Geliştirilmiş kazançlar planları, benzersiz kazanç planları oluşturmanıza ve yönetmenize ve karmaşık kazanç oranı tabloları ve iç içe geçmiş katmanları desteklebilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="9b0a2-110">Daha kolay bir çalışan deneyimi için, kolayca kazanç programları, paketleri ve otomatik kayıt kuralları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="9b0a2-111">Esnek kredi programları, emeklilik ve diğer ömür olaylarını desteklemeye yönelik bir program sağlar.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="9b0a2-112">Kapsamlı uygunluk kuralları, doğru çalışanların hak kazanın uygun olmasını sağlamayacaklarından emin olmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="9b0a2-113">Çevrimiçi yararlar kaydı, çalışanlarınız için kolay bir deneyim sağlar.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="9b0a2-114">Uygun yaşam olayı işleme işlemi gelecekteki yaşam olaylarını destekler.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="9b0a2-115">Demo verilerine erişmek istiyorsanız korumalı alan ortamınızı yeniden dağıtmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="9b0a2-116">Kazanç Yönetimni etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9b0a2-116">Enable Benefits management</span></span>

<span data-ttu-id="9b0a2-117">Bu konuda Human Resources'taki özelliklerin nasıl etkinleştirileceği açıklanır.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="9b0a2-118">Ayrıca, Kazanç yönetimini etkinleştirdiğinizde, Kazanç yönetiminin Human Resources'taki hangi mevcut özelliklerin yerini aldığını veya devre dışı bırakıldığını da bildirir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b0a2-119">**Üretim** ortamında Kazanç yönetimini etkinleştirdikten sonra devre dışı bırakamazsınız.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="9b0a2-120">**Üretim** ortamında etkinleştirmeden önce Kazanç yönetimini **Korumalı alan** ortamında etkinleştirmenizi ve test etmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="9b0a2-121">Eski Kazanç işlevi ile ek kurulum gerektiren yeni Kazanç yönetimi işlevi arasında önemli farklar vardır ve üretim ortamına alınmadan önce test edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="9b0a2-122">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="9b0a2-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="9b0a2-123">Personel bilgilerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-123">Configure employee information</span></span>

<span data-ttu-id="9b0a2-124">Çalışanları kazançalara kaydedebilmek için gerekli bilgileri sağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="9b0a2-125">Bir çalışanı başlama tarihinde bir **Sabit ücret planına** kaydetmeniz ve **Çalışan** formundaki **İstihdam ayrıntıları** bölümünde bir **Kazanç ödeme sıklığı** seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="9b0a2-126">Komisyonlar gibi ek ücret alan personeliniz varsa, çalışan kaydından bir **Kazançlar yıllık maaş** tutarı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="9b0a2-127">İnsan Kaynakları, karşılama tutarlarını belirlerken yıllık sabit ücret tutarı yerine **Kazançlar yıllık maaş** alanını kullanacaktır.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="9b0a2-128">**Kazançlar yıllık maaş** personel işe başlama tarihi veya kazanç dönemi başlangıcı (hangisi sonraysa) itibarıyla geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="9b0a2-129">Bir personel için hem sabit ücret hem de kazançlar yıllık maaş tutarı kaydedilirse, karşılama tutarlarını belirlemede kazançlar yıllık maaş kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="9b0a2-130">Cinsiyet veya yaşa dayalı oranlar kullanan bir kazanç planı oluşturduğunuzda, bir çalışanın kazanç maliyetini hesaplamak için doğum tarihi ve cinsiyet girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="9b0a2-131">Kazanç yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-131">Configure Benefits management</span></span>

<span data-ttu-id="9b0a2-132">Çalışanlarınız için kazanç planları oluşturabilmeniz için, planların seçeneklerini konfigüre etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="9b0a2-133">Kazanç yönetimi parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="9b0a2-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="9b0a2-134">Uygunluk kurallarını ve seçeneklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="9b0a2-135">Kişisel iletişim uygunluk seçeneklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="9b0a2-136">Kapsam seçeneklerini oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="9b0a2-137">Ödeme sıklıklarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="9b0a2-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="9b0a2-138">Yaşam olayı türlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="9b0a2-139">Plan türleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="9b0a2-140">Neden kodlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="9b0a2-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="9b0a2-141">Katman kodlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="9b0a2-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="9b0a2-142">Oranları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="9b0a2-143">Kesintileri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="9b0a2-144">Bekleme günlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="9b0a2-145">Bekleme dönemlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="9b0a2-146">Yuvarlama kurallarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="9b0a2-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="9b0a2-147">İstihdam kategorileri oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="9b0a2-148">İstihdam türlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="9b0a2-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="9b0a2-149">Personel self servisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="9b0a2-150">Kazanç planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b0a2-150">Create benefit plans</span></span>

<span data-ttu-id="9b0a2-151">Bu makaleler, ambalajlarla esnek kredi programları dahil olmak üzere kazanç planlarının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="9b0a2-152">Kazanç planlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="9b0a2-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="9b0a2-153">Esnek kredi programları ayarlama</span><span class="sxs-lookup"><span data-stu-id="9b0a2-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="9b0a2-154">Kazanç planlarını işleme</span><span class="sxs-lookup"><span data-stu-id="9b0a2-154">Process benefit plans</span></span>

<span data-ttu-id="9b0a2-155">Yaptığınız değişikliklerin bazılarını etkin hale getirmek için onları işlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9b0a2-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="9b0a2-156">Kayıt uygunluğunu işleme</span><span class="sxs-lookup"><span data-stu-id="9b0a2-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="9b0a2-157">Yaşam olaylarını işleme</span><span class="sxs-lookup"><span data-stu-id="9b0a2-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="9b0a2-158">Yaşam olayı değişikliklerini işleme</span><span class="sxs-lookup"><span data-stu-id="9b0a2-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="9b0a2-159">Yaşam olayı uygunluğunu işleme</span><span class="sxs-lookup"><span data-stu-id="9b0a2-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="9b0a2-160">Oran değişikliklerini işleme</span><span class="sxs-lookup"><span data-stu-id="9b0a2-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]