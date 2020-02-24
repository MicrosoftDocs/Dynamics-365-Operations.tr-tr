---
title: Kazanç yönetimine genel bakış
description: Dynamics 365 Human Resources'Deki sosyal haklar yönetimi önizleme özelliğinin Özeti. Çalışanlarınızı kullanımı kolay bir çevrimiçi deneyim sayesinde çalışanlarınızın genişletilmiş sosyal haklar seçeneklerini sunun.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029475"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="6666b-104">Kazanç yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="6666b-104">Benefits management overview</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="6666b-105">Rekabet edebilir durumda kalmak için, en iyi çalışanlarınızı ele almak ve bunları korumak amacıyla zengin bir avantaj kümesi sunmalısınız.</span><span class="sxs-lookup"><span data-stu-id="6666b-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="6666b-106">Tıp ve diş kapsamı gibi standart avantajlara ek olarak, benimseme yardımı, dinlenme programları ve giyme gibi genişletilmiş hizmetler de sunmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6666b-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="6666b-107">Microsoft Dynamics 365 Human Resources'un sosyal haklar yönetimi önizleme özelliği, çok çeşitli avantaj seçeneklerini destekleyen esnek bir çözüm sağlar.</span><span class="sxs-lookup"><span data-stu-id="6666b-107">The Benefits management preview feature in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="6666b-108">İnsan Kaynakları ayrıca, tekliflerinizi gösteren kullanımı kolay bir çalışan deneyimi de içerir.</span><span class="sxs-lookup"><span data-stu-id="6666b-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="6666b-109">Geliştirilmiş kazançlar planları, benzersiz kazanç planları oluşturmanıza ve yönetmenize ve karmaşık kazanç oranı tabloları ve iç içe geçmiş katmanları desteklebilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="6666b-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="6666b-110">Daha kolay bir çalışan deneyimi için, kolayca kazanç programları, paketleri ve otomatik kayıt kuralları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6666b-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="6666b-111">Esnek kredi programları, emeklilik ve diğer ömür olaylarını desteklemeye yönelik bir program sağlar.</span><span class="sxs-lookup"><span data-stu-id="6666b-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="6666b-112">Kapsamlı uygunluk kuralları, doğru çalışanların hak kazanın uygun olmasını sağlamayacaklarından emin olmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="6666b-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="6666b-113">Çevrimiçi yararlar kaydı, çalışanlarınız için kolay bir deneyim sağlar.</span><span class="sxs-lookup"><span data-stu-id="6666b-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="6666b-114">Nitelikli ömür olayı işleme, çalışan self servis ile tümleşir ve gelecekteki ömür olaylarını destekler.</span><span class="sxs-lookup"><span data-stu-id="6666b-114">Qualified life event processing integrates with Employee self service, and also supports future life events.</span></span>

<span data-ttu-id="6666b-115">Demo verilerine erişmek istiyorsanız korumalı alan ortamınızı yeniden dağıtmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6666b-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

<span data-ttu-id="6666b-116">Doğrudan geri bildirim veya konu rapor verebilirsiniz: D365BenefitsPreview@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="6666b-116">You can provide direct feedback or report issues to:  D365BenefitsPreview@microsoft.com.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="6666b-117">Kazanç yönetimiyle ilgili bilinen sorunlar</span><span class="sxs-lookup"><span data-stu-id="6666b-117">Benefits management known issues</span></span>

### <a name="eligibility-processing"></a><span data-ttu-id="6666b-118">Uygunluk işleniyor</span><span class="sxs-lookup"><span data-stu-id="6666b-118">Eligibility processing</span></span>

<span data-ttu-id="6666b-119">1-5X maaş, yüzde maaş ve sabit tutar karşılama tutarı kullanan avantajlar için uygunluğu çalıştırırken , **kullanım ayrıntıları** tarihini **çalışma geçmişi** içindeki **çalışan başlangıç tarihine** ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="6666b-119">When running eligibility for benefits that use a 1-5X Salary, % of Salary, and Flat Amount coverage amount, you must set the **Benefit details** date to the **Employee start date** in **Employment history**.</span></span> <span data-ttu-id="6666b-120">**Çalışılan saatleri**, **ödeme sıklığını** ve **yıllık kazançlar maaş tutarını** da dahil etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="6666b-120">You must also include **Hours worked**, **Payment frequency**, and **Annual benefits salary amount**.</span></span> <span data-ttu-id="6666b-121">Çalışanın sabit dengelemesi varsa, **çalışılan saatleri** ve **ödeme sıklığını** girin.</span><span class="sxs-lookup"><span data-stu-id="6666b-121">If the worker has fixed compensation, enter **Hours worked** and **Payment frequency**.</span></span> <span data-ttu-id="6666b-122">Yıllık maaş tutarı hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="6666b-122">The annual salary amount will calculate.</span></span> <span data-ttu-id="6666b-123">Çalışan maaşlı ise, **çalışılan saatleri** girmeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="6666b-123">If the employee is salaried, you don't need to enter **Hours worked**.</span></span> <span data-ttu-id="6666b-124">Yeni çalışanlar oluştururken önce sabit ücret girilmesini öneririz.</span><span class="sxs-lookup"><span data-stu-id="6666b-124">We recommend that when creating new workers, enter fixed compensation first.</span></span> <span data-ttu-id="6666b-125">Avantaj ayrıntıları kaydını güncelleştirmek için, **çalışan > çalışan geçmişi > istihdam ayrıntılarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="6666b-125">To update the benefit details record, navigate to **Worker > Worker history > Employment details**.</span></span> <span data-ttu-id="6666b-126">Tarihi çalışanın başlangıç tarihine ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6666b-126">Adjust the date to the worker's start date.</span></span>

### <a name="employee-self-service"></a><span data-ttu-id="6666b-127">Personel self servisi</span><span class="sxs-lookup"><span data-stu-id="6666b-127">Employee self-service</span></span>

<span data-ttu-id="6666b-128">Ömür için karşılama tutarı güncelleştirilirken çalışan tutarı hesaplamaz.</span><span class="sxs-lookup"><span data-stu-id="6666b-128">Employee amount doesn't calculate when updating the coverage amount for life insurance.</span></span> <span data-ttu-id="6666b-129">Örneğin bir çalışana bir hayat sigortası planı sunulduğunda 1000 liralık karşılama tutarı başına 36 kuruşluk maliyetle 50.000 liraya kadar bir karşılama tutarı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="6666b-129">For example, when an employee is offered a life insurance plan, they can select up to $50,000 in coverage at a cost of $.36 per $1,000 of coverage.</span></span>  <span data-ttu-id="6666b-130">Çalışan karşılama tutarını güncelleştirdiğinde, çalışanın ilişkili maliyeti sıfır olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="6666b-130">When the employee updates the coverage amount, the employee’s associated cost remains at zero.</span></span>

<span data-ttu-id="6666b-131">Bu plan türünde yalnızca tek bir seçime izin veren bir kazanç planı için, bir plan seçtikten sonra bir planı feragat etmeye çalışırsa Kullanıcı bir hata alır.</span><span class="sxs-lookup"><span data-stu-id="6666b-131">For a benefit plan that only allows a single selection of that plan type, the user receives an error if they attempt to waive a plan after selecting a plan.</span></span> <span data-ttu-id="6666b-132">Örneğin kullanıcı bir tıbbi plan seçip alışveriş sepetine ekliyor.</span><span class="sxs-lookup"><span data-stu-id="6666b-132">For example, a user selects a medical plan and places it in their cart.</span></span> <span data-ttu-id="6666b-133">Bunun ardından, başka bir tıbbi plan için **Feragat**'i seçiyor.</span><span class="sxs-lookup"><span data-stu-id="6666b-133">The user then selects **Waive** for another medical plan.</span></span> <span data-ttu-id="6666b-134">Kullanıcı bir hata alacaktır.</span><span class="sxs-lookup"><span data-stu-id="6666b-134">The user will receive an error.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="6666b-135">Kazanç Yönetimni etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6666b-135">Enable Benefits management</span></span>

<span data-ttu-id="6666b-136">Kazançlar yönetimi bir önizleme özelliğidir ve yalnızca **korumalı alan** ortamlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6666b-136">Benefits management is a preview feature, and is only available in **Sandbox** environments.</span></span> <span data-ttu-id="6666b-137">Bu makalelerde İnsan Kaynakları Önizleme özelliklerinin nasıl açılacağı açıklanır.</span><span class="sxs-lookup"><span data-stu-id="6666b-137">These articles describe how to turn on preview features in Human Resources.</span></span> <span data-ttu-id="6666b-138">Bunlar ayrıca, sosyal haklar yönetimini etkinleştirdiğinizde İnsan Kaynakları olan, sosyal haklar yönetiminin hangi varolan özelliklerinin yerini aldığını veya devre dışı bırakıldığını da bildirir.</span><span class="sxs-lookup"><span data-stu-id="6666b-138">They also tell which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

- [<span data-ttu-id="6666b-139">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="6666b-139">Manage features</span></span>](hr-admin-manage-features.md)
- [<span data-ttu-id="6666b-140">Önizleme özelliği: Kazanç yönetimi</span><span class="sxs-lookup"><span data-stu-id="6666b-140">Preview feature: Benefits management</span></span>](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a><span data-ttu-id="6666b-141">Kazanç yönetimini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-141">Configure Benefits management</span></span>

<span data-ttu-id="6666b-142">Çalışanlarınız için kazanç planları oluşturabilmeniz için, planların seçeneklerini konfigüre etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6666b-142">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="6666b-143">Kazanç yönetimi parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="6666b-143">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="6666b-144">Uygunluk kurallarını ve seçeneklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-144">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="6666b-145">Kişisel iletişim uygunluk seçeneklerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-145">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="6666b-146">Kapsam seçeneklerini oluşturma</span><span class="sxs-lookup"><span data-stu-id="6666b-146">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="6666b-147">Ödeme sıklıklarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6666b-147">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="6666b-148">Yaşam olayı türlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-148">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="6666b-149">Plan türleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="6666b-149">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="6666b-150">Neden kodlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="6666b-150">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="6666b-151">Katman kodlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6666b-151">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="6666b-152">Oranları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-152">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="6666b-153">Kesintileri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-153">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="6666b-154">Bekleme günlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-154">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="6666b-155">Bekleme dönemlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-155">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="6666b-156">Yuvarlama kurallarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6666b-156">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="6666b-157">İstihdam kategorileri oluşturma</span><span class="sxs-lookup"><span data-stu-id="6666b-157">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="6666b-158">İstihdam türlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="6666b-158">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="6666b-159">Personel self servisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-159">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="6666b-160">Kazanç planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="6666b-160">Create benefit plans</span></span>

<span data-ttu-id="6666b-161">Bu makaleler, ambalajlarla esnek kredi programları dahil olmak üzere kazanç planlarının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6666b-161">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="6666b-162">Kazanç planlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6666b-162">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="6666b-163">Çalışan kazanç planları oluşturma</span><span class="sxs-lookup"><span data-stu-id="6666b-163">Create worker benefit plans</span></span>](hr-benefits-plans-worker.md)
- [<span data-ttu-id="6666b-164">Esnek kredi programları ayarlama</span><span class="sxs-lookup"><span data-stu-id="6666b-164">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)
- [<span data-ttu-id="6666b-165">Gelecekteki yaşam olaylarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6666b-165">Configure future life events</span></span>](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="6666b-166">Kazanç planlarını işleme</span><span class="sxs-lookup"><span data-stu-id="6666b-166">Process benefit plans</span></span>

<span data-ttu-id="6666b-167">Yaptığınız değişikliklerin bazılarını etkin hale getirmek için onları işlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6666b-167">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="6666b-168">Kayıt uygunluğunu işleme</span><span class="sxs-lookup"><span data-stu-id="6666b-168">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="6666b-169">Yaşam olaylarını işleme</span><span class="sxs-lookup"><span data-stu-id="6666b-169">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="6666b-170">Yaşam olayı değişikliklerini işleme</span><span class="sxs-lookup"><span data-stu-id="6666b-170">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="6666b-171">Yaşam olayı uygunluğunu işleme</span><span class="sxs-lookup"><span data-stu-id="6666b-171">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="6666b-172">Oran değişikliklerini işleme</span><span class="sxs-lookup"><span data-stu-id="6666b-172">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

