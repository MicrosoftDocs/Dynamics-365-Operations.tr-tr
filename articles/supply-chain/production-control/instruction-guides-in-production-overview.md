---
title: Üretimdeki çalışanlar için karma gerçeklik Kılavuzları sağlama
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'taki üretim yönetimi modülünün Dynamics 365 Guides ile nasıl tümleştirileceğini açıklamaktadır.
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 14645f592275d07a6b633146bb6da35b89c1bf77
ms.sourcegitcommit: 6d2fc497c8a7f49c48e7662995e27b5f8cc10296
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000990"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="3b374-103">Üretimdeki çalışanlar için karma gerçeklik Kılavuzları sağlama</span><span class="sxs-lookup"><span data-stu-id="3b374-103">Provide mixed-reality Guides for workers in production</span></span>

<span data-ttu-id="3b374-104">Üretim süreçlerinde çalışan çalışanlar, çalışmaları bağlamında doğru zamanda sağlanan ilgili yönergelerden faydalanır.</span><span class="sxs-lookup"><span data-stu-id="3b374-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="3b374-105">*Yönergeler* aşağıdakiler dahil olmak üzere birçok iş alanında uygulanır: derleme servis, operasyonlar, sertifika ve güvenlik.</span><span class="sxs-lookup"><span data-stu-id="3b374-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="3b374-106">Devam eden eğitim yönergeleri bu temel iş işlevlerinin tümünde, çalışanların daha fazlasını elde etmesine ve daha iyi çalışmasına yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="3b374-107">Giriş</span><span class="sxs-lookup"><span data-stu-id="3b374-107">Introduction</span></span>

<span data-ttu-id="3b374-108">Yönergeleri farklı şekillerde sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="3b374-109">Kullanıma hazır olarak gelen etkili bir sistem [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) kullanır.</span><span class="sxs-lookup"><span data-stu-id="3b374-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="3b374-110">Dynamics 365 Guides uygulamalı eğitimle çalışanlarınızı desteklemenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="3b374-111">Çalışanlarınıza gereksinim duydukları araçlar ve parçalara yönelik kılavuzluk sağlayan adım adım yönergelerle standartlaştırılmış süreçler belirleyebilir ve bu araçların gerçek çalışma durumlarında nasıl kullanılacağını çalışanlarınıza gösterebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="3b374-112">Kılavuzları, üretim denetiminin aşağıdakiler dahil çeşitli aşamalarına iliştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="3b374-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="3b374-113">Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3b374-113">Resources</span></span>](#resources)
- [<span data-ttu-id="3b374-114">Kaynak grupları</span><span class="sxs-lookup"><span data-stu-id="3b374-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="3b374-115">Serbest bırakılan ürünler</span><span class="sxs-lookup"><span data-stu-id="3b374-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="3b374-116">Formüller</span><span class="sxs-lookup"><span data-stu-id="3b374-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="3b374-117">Formül sürümleri</span><span class="sxs-lookup"><span data-stu-id="3b374-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="3b374-118">Ürün reçeteleri (BOM'lar)</span><span class="sxs-lookup"><span data-stu-id="3b374-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="3b374-119">BOM süürmleri</span><span class="sxs-lookup"><span data-stu-id="3b374-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="3b374-120">Rotalar</span><span class="sxs-lookup"><span data-stu-id="3b374-120">Routes</span></span>](#routes)
- [<span data-ttu-id="3b374-121">Rota sürümleri</span><span class="sxs-lookup"><span data-stu-id="3b374-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="3b374-122">Rota operasyonu ilişkileri</span><span class="sxs-lookup"><span data-stu-id="3b374-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="3b374-123">Ayrıca, VArlık Yönetimi ile de Kılavuzlar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="3b374-124">Bu seçenek hakkında daha fazla bilgi için bkz. [Dynamics 365 Supply Chain Management'ı (Varlık Yönetimi) Dynamics 365 Guides ile tümleştirme](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="3b374-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="3b374-125">Bir saha çalışan Supply Chain Management üzerinden atölyede bir iş seçtiğinde, çalışan [ilgili kılavuzları](#logic) iş kartında görebilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="3b374-126">Çalışan belirli bir kılavuzu seçtiğinde, ekranda o kılavuz için bir QR kodu gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="3b374-127">Çalışan, QR kodunu taramak HoloLens'i kullanır ve bu, Guides'ı başlatarak gerekli yönergeleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="3b374-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="3b374-128">Aşağıdaki alt bölümlerde, farklı sektörlerdeki şirketlerin üretim yönergelerini sunmak için Guides kullanırken en büyük değeri elde ettiği birkaç seçili senaryo açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3b374-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="3b374-129">Montaj</span><span class="sxs-lookup"><span data-stu-id="3b374-129">Assembly</span></span>

<span data-ttu-id="3b374-130">![Derleme görevlerinde Guides kullanma](media/instruction-guides-hero-assembly.png "Servis görevlerinde Guides kullanma")</span><span class="sxs-lookup"><span data-stu-id="3b374-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="3b374-131">Derleme işlemlerinde yönergeler, çalışanlara gereksinim duydukları araç ve bölümleri ve gerçek çalışma durumlarında bunların nasıl kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b374-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="3b374-132">Üretim yöneticileri, örneğin [üretim rotaları](routes-operations.md), [operasyon ilişkileri](routes-operations.md#operation-relations) veya [ürün reçeteleri](bill-of-material-bom.md) için Kılavuzlar oluşturabilir ve atayabilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="3b374-133">Çalışanlar ilgili yönergeleri, atölyede ilgili operasyon deneyiminde bulabilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="3b374-134">Servis</span><span class="sxs-lookup"><span data-stu-id="3b374-134">Service</span></span>

<span data-ttu-id="3b374-135">![Servis görevlerinde Guides kullanma](media/instruction-guides-hero-service.png "Servis görevlerinde Guides kullanma")</span><span class="sxs-lookup"><span data-stu-id="3b374-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="3b374-136">Teknisyenleri iş sahasında kılavuzlu talimatlarla donatın ve ek ziyaretler planlama ihtiyacını ortadan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="3b374-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="3b374-137">Servis yöneticileri, örneğin kalite değerlendirmesi yordamlarına geçiş yapan belirli [ürünlere](../../commerce/product.md) Kılavuzlar atayabilirler.</span><span class="sxs-lookup"><span data-stu-id="3b374-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="3b374-138">Kalite</span><span class="sxs-lookup"><span data-stu-id="3b374-138">Quality</span></span>

<span data-ttu-id="3b374-139">![Kalite güvence görevlerinde Guides kullanma](media/instruction-guides-hero-quality.png "Kalite güvence görevlerinde Guides kullanma")</span><span class="sxs-lookup"><span data-stu-id="3b374-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="3b374-140">Yeni süreçler kullanıma sunun ve çalışanların bilgisini tekrarlanabilir bir araca çevirerek artan tutarlılık sağlayın.</span><span class="sxs-lookup"><span data-stu-id="3b374-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="3b374-141">Kalite güvencesi yöneticileri, örneğin kalite değerlendirmesi yordamlarına geçiş yapan belirli [ürünlere](../../commerce/product.md) kılavuzlar atayabilirler.</span><span class="sxs-lookup"><span data-stu-id="3b374-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="3b374-142">Sertifikalar</span><span class="sxs-lookup"><span data-stu-id="3b374-142">Certifications</span></span>

<span data-ttu-id="3b374-143">![Sertifika ile ilgili görevler için Guides kullanma](media/instruction-guides-hero-certification.png "Sertifika ile ilgili görevler için Guides kullanma")</span><span class="sxs-lookup"><span data-stu-id="3b374-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="3b374-144">Kimin ve nerede yardıma ihtiyacı olduğunu hızlı bir şekilde tanımlayarak, her çalışanın yüksek standartları karşıladığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="3b374-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="3b374-145">Güvenlik</span><span class="sxs-lookup"><span data-stu-id="3b374-145">Safety</span></span>

<span data-ttu-id="3b374-146">![İş güvenliği yönergelerinde Guides kullanma](media/instruction-guides-hero-safety.png "İş güvenliği yönergelerinde Guides kullanma")</span><span class="sxs-lookup"><span data-stu-id="3b374-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="3b374-147">Fiziksel ortamda çalışmadan önce tehlikeli yordamları sanal olarak uygulayan yönergeler sağlayın.</span><span class="sxs-lookup"><span data-stu-id="3b374-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="3b374-148">Karma gerçeklik yaklaşımıyla, çalışanlar tehlikeli yordamları sanal olarak deneyimleyebilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="3b374-149">Üretim yöneticileri [ürün öğelerine ](../../commerce/product.md), [rotalara](routes-operations.md) ve [operasyonlara](routes-operations.md#operation-relations) yönergeler atayarak, tehlikeli malzeme işleme veya hassas malzeme işleme yordamları için özel işleme yönergeleri sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="3b374-150">Yönergeler ve Guides ile başlayın</span><span class="sxs-lookup"><span data-stu-id="3b374-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="3b374-151">Üretim süreçlerinde yönergeleri etkinleştirmek için, Supply Chain Management, Dynamics 365 Guides ile kullanıma hazır tümleştirme sağlar.</span><span class="sxs-lookup"><span data-stu-id="3b374-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="3b374-152">Üretim varlıklarına ve işine karma gerçeklik yönergeleri oluşturmak, yönetmek ve atamak için Guides'ın lisanslı ve yüklenmiş uygulama örneği gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3b374-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3b374-153">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="3b374-153">Prerequisites</span></span>

<span data-ttu-id="3b374-154">Bu özelliği kullanmak için sisteminizde şunlar olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="3b374-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="3b374-155">Dynamics 365 Supply Chain Management sürüm 10.0.15 veya üstü</span><span class="sxs-lookup"><span data-stu-id="3b374-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="3b374-156">Supply Chain Management uygulamaları için [Çift yazma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write).</span><span class="sxs-lookup"><span data-stu-id="3b374-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="3b374-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) sürüm 400.0.1.48 veya üstü</span><span class="sxs-lookup"><span data-stu-id="3b374-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="3b374-158">Özelliği etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3b374-158">Turn on the feature</span></span>

<span data-ttu-id="3b374-159">Özelliği sisteminizde kullanılabilir hale getirmek için yapılandırma anahtarlarını etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b374-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="3b374-160">Bunu yalnızca bir kere yapmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b374-160">You only need to do this once.</span></span> <span data-ttu-id="3b374-161">Bunu yapmak için bir yöneticinin aşağıdakileri yapması gerekir:</span><span class="sxs-lookup"><span data-stu-id="3b374-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="3b374-162">Sisteminizi [Bakım modunda](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) anlatıldığı şekilde bakım moduna alın.</span><span class="sxs-lookup"><span data-stu-id="3b374-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="3b374-163">**Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="3b374-164">**Karma gerçeklik** bölümünü genişletin ve sonra **Karma gerçeklik kılavuzu** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="3b374-165">**Üretim yönetimi** bölümünü genişletin ve sonra **Üretim yönergeleri** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="3b374-166">[Bakım modunda](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) anlatıldığı şekilde bakım modunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="3b374-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="3b374-167">Guides'ın atölyede nasıl görüneceğini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3b374-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="3b374-168">Guides'ın atölyede nasıl görüneceğini konfigüre etmek için **Karma Gerçeklik \> Dynamics 365 Guides \> Guides tümleştirmesini yapılandır** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="3b374-169">![Üretim için Guides tümleştirmesini yapılandırma](media/instruction-guides-configure-integration.png "Üretim için Guides tümleştirmesini yapılandırma")</span><span class="sxs-lookup"><span data-stu-id="3b374-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="3b374-170">Aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="3b374-170">Set the following fields:</span></span>

- <span data-ttu-id="3b374-171">**Common Data Service alt etki alanı** - Bu alan zaten bir değer göstermelidir.</span><span class="sxs-lookup"><span data-stu-id="3b374-171">**Common Data Service subdomain** - This field should already show a value.</span></span> <span data-ttu-id="3b374-172">Bu alan, Kılavuzlarınızı oluşturduğunuz Common Data Service ortamının alt etki alanını içerir.</span><span class="sxs-lookup"><span data-stu-id="3b374-172">This field holds the subdomain for the Common Data Service environment where you create your Guides.</span></span> <span data-ttu-id="3b374-173">Alt etki alanı, URL'nin ilk bölümüdür ve genellikle kuruluşunuzun adıyla adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="3b374-173">The subdomain is the first part of the URL and is typically named after your organization.</span></span> <span data-ttu-id="3b374-174">Örneğin, Common Data Service URL'niz "contoso.crm4.dynamics.com" ise, buraya *contoso* girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b374-174">For example, if your Common Data Service URL is "contoso.crm4.dynamics.com", you should enter *contoso* here.</span></span> <span data-ttu-id="3b374-175">Bu değer kılavuzlarınız için adres oluşturmak amacıyla kullanılır ve QR kodlarına kodlanır.</span><span class="sxs-lookup"><span data-stu-id="3b374-175">This value is used to compose addresses for your guides and will be encoded into the QR codes.</span></span>
- <span data-ttu-id="3b374-176">**QR kodu boyutu** - İşlenen QR kodu boyutunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3b374-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="3b374-177">Ekranınızın büyük bir boyutunu dolduracak, ancak daha fazlasını doldurmayacak bir boyut seçmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="3b374-178">Genellikle, *15* iyi bir değerdir.</span><span class="sxs-lookup"><span data-stu-id="3b374-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="3b374-179">**QR kodu hata düzeltme düzeyi** - QR kodunun öğe boyutunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3b374-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="3b374-180">Yüksek öğe boyutu, kodun güvenilirliğini artırmaya yardımcı olabilir ancak **QR kodu boyutunuz** seçtiğiniz düzeltme düzeyinin gerektirdiği ayrıntı düzeyini destekleyecek büyüklükte olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3b374-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>


> [!TIP]
> - <span data-ttu-id="3b374-181">Ekranınız için çok büyük olan QR kodu boyutlarının işlenmesi biraz daha uzun sürer ve ekrana sığacak şekilde ölçeklenir.</span><span class="sxs-lookup"><span data-stu-id="3b374-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="3b374-182">Bunlar bir avantaj sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="3b374-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="3b374-183">Çok küçük olan QR kodu boyutları, HoloLens'in bazı ortamlarda kodu doğru okuma yeteneğini azaltabilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="3b374-184">QR kodları görüntüleyen her cihazın ayarlarını HoloLens kullanıcıları için test etmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="3b374-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="3b374-185">Atölye ortamınıza yeterli okunabilirlik sağlayan ayarları seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="3b374-186">Tüm Kılavuz atamalarının genel görünümünü alma</span><span class="sxs-lookup"><span data-stu-id="3b374-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="3b374-187">Kuruluşunuzdaki tüm kullanılabilir Kılavuzların listesini ve üretim süreçlerinize ve kaynaklarınıza yapılan tüm atamaları görmek için **Tüm Kılavuzlar** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b374-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="3b374-188">Açmak için, **Karma gerçeklik \> Kılavuzlar \> Tüm Kılavuzlar** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="3b374-189">Üstteki listede bulunan tüm Kılavuzlar gösterilir ve bu alanı, listeye filtre uygulamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="3b374-190">Alttaki listede tüm Kılavuz atamaları gösterilir ve bunları yönetmek için bir araç çubuğu sağlanır.</span><span class="sxs-lookup"><span data-stu-id="3b374-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="3b374-191">![Kılavuzları Yönetme](media/instruction-guides-allguides.png "Kılavuzları Yönetme")</span><span class="sxs-lookup"><span data-stu-id="3b374-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="3b374-192">Aşağıdaki bölümlerde, Kılavuzlar atayabildiğiniz nesne türleri açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3b374-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="3b374-193">Her atanan kılavuz, ilgili üretim işlerine otomatik olarak eklenen yönergeleri sağlar ve atölyede kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3b374-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="3b374-194">Kılavuzu kaynakla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="3b374-195">Kılavuzu ilgili üretim işleri bağlamında sunmak için bir [kaynağa](operations-resources.md) Kılavuz ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3b374-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="3b374-196">Kaynakları kullanan tipik senaryo</span><span class="sxs-lookup"><span data-stu-id="3b374-196">Typical scenario using resources</span></span>

<span data-ttu-id="3b374-197">Örneğin, genel makine güvenliğiyle veya makine türündeki bir kaynağa ilişkin yönergeleri ele alarak bir Kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="3b374-198">Daha sonra, bu Kılavuz makinede gerçekleştirilen her iş için kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3b374-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="3b374-199">Kaynağa Kılavuz ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-199">Add a Guide to a resource</span></span>

<span data-ttu-id="3b374-200">Kaynağa Kılavuz eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="3b374-201">**Üretim denetimi \> Kurulum \> Kaynaklar \> Kaynaklar** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="3b374-202">Liste bölmesinden Kılavuz atamak istediğiniz kaynağı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-203">**İlişkili Kılavuzlar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3b374-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="3b374-204">**İlişkili Kılavuzlar** araç çubuğundan **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="3b374-205">Kılavuza yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="3b374-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="3b374-206">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="3b374-207">Çok sayıda Kılavuzunuz varsa, aradığınız bir kılavuzu bulmak için listeye filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="3b374-208">![Kılavuzları Yönetme](media/instruction-guides-allguides.png "Kılavuzları Yönetme")</span><span class="sxs-lookup"><span data-stu-id="3b374-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="3b374-209">Kılavuzu kaynak grubuyla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="3b374-210">Makine gruplarını, üretim hatlarını veya çalışma hücrelerini yönetmek için kullanıyorsanız [kaynak gruplarına](tasks/define-discrete-manufacturing-resource-group.md) kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="3b374-211">Kaynak gruplarını kullanan tipik senaryolar</span><span class="sxs-lookup"><span data-stu-id="3b374-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="3b374-212">**Örnek 1:** Aynı model birkaç makine için bir kaynak grubu tanımladınız.</span><span class="sxs-lookup"><span data-stu-id="3b374-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="3b374-213">İlgili her kaynağa makine modeli için uygun işleme talimatı kılavuzu atamak yerine, Kılavuzu makine modelini yansıtan kaynak grubuna atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="3b374-214">**Örnek 2:** Farklı makineler içeren bir çalışma hücresi için bir kaynak grubu tanımladınız ve çalışma hücresinin nasıl yönetileceğine ilişkin genel yönergeler sağlayan bir Kılavuzunuz var.</span><span class="sxs-lookup"><span data-stu-id="3b374-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="3b374-215">Kılavuz bu iş hücresindeki tüm üretim faaliyetleri için geçerli olur.</span><span class="sxs-lookup"><span data-stu-id="3b374-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="3b374-216">Kaynak grubuna Kılavuz ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="3b374-217">Kaynak grubuna Kılavuz eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="3b374-218">**Üretim denetimi \> Kurulum \> Kaynaklar \> Kaynaklar grupları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="3b374-219">Liste bölmesinden Kılavuz atamak istediğiniz kaynak grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-220">**İlişkili Kılavuzlar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3b374-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="3b374-221">**İlişkili Kılavuzlar** araç çubuğundan **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="3b374-222">Kılavuza yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="3b374-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="3b374-223">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="3b374-224">Çok sayıda Kılavuzunuz varsa, aradığınız bir kılavuzu bulmak için listeye filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="3b374-225">![Kaynak grubuna Kılavuz ekleme](media/instruction-guides-resourcegroup.png "Kaynak grubuna Kılavuz ekleme")</span><span class="sxs-lookup"><span data-stu-id="3b374-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="3b374-226">Kılavuzu serbest bırakılan ürünle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="3b374-227">Herhangi bir [serbest bırakılan ürüne](../pim/tasks/create-released-product-single-company.md) kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="3b374-228">Serbest bırakılan ürünler kullanan tipik senaryo</span><span class="sxs-lookup"><span data-stu-id="3b374-228">Typical scenario using released products</span></span>

<span data-ttu-id="3b374-229">Ürün düzeyindeki Kılavuzlar, belirli bir serbest bırakılan ürün veya maddeyi çalıştırma veya işleme ile ilgili yönergelerle atölye çalışanlarına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3b374-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="3b374-230">Kılavuzu serbest bırakılan ürüne ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-230">Add a Guide to a released product</span></span>

<span data-ttu-id="3b374-231">Serbest bırakılan ürüne Kılavuz eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="3b374-232">**Üretim bilgi yönetimi \> Ürünler \> Serbest bırakılan ürünler** 'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="3b374-233">Kılavuz atamak istediğiniz ürünü açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-234">Eylem Bölmesinde, **Mühendis** sekmesini açın ve **Görünüm** grubundan **İlişkili Kılavuzlar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="3b374-235">Seçili ürününüz için **İlişkili Kılavuzlar** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="3b374-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="3b374-236">Eylem bölmesinde, kılavuza yeni satır eklemek için **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="3b374-237">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="3b374-238">![Serbest bırakılan ürüne Kılavuz ekleme](media/instruction-guides-ReleasedProduct-AddGuides.png "Serbest bırakılan ürüne Kılavuz ekleme")</span><span class="sxs-lookup"><span data-stu-id="3b374-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="3b374-239">Kılavuzu formülle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="3b374-240">Herhangi bir [formüle](bill-of-material-bom.md#formulas-co-products-and-by-products) kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="3b374-241">Formülleri kullanan tipik senaryo</span><span class="sxs-lookup"><span data-stu-id="3b374-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="3b374-242">Formül düzeyindeki Kılavuzlar, atölye çalışanlarına bir formül veya reçete bağlamında, kılavuzlu işleme talimatları sağlar.</span><span class="sxs-lookup"><span data-stu-id="3b374-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="3b374-243">Kılavuzlar, bir formülün sürümlerine de atanabilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="3b374-244">Bir rotaya, rota sürümüne veya rota operasyon ilişkilerine formüle dayalı olarak üretim süreçleriyle ilgili kılavuz atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="3b374-245">Kılavuzlar, şu anda bireysel formül satırlarına eklenemez.</span><span class="sxs-lookup"><span data-stu-id="3b374-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="3b374-246">Formüle Kılavuz ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-246">Add a Guide to a formula</span></span>

<span data-ttu-id="3b374-247">Formüle Kılavuz eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="3b374-248">**Üretim bilgi yönetimi \> Ürün reçeteleri ve formülleri \> Formüller** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="3b374-249">Kılavuz atamak istediğiniz formülü açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-250">Üst hızlı sekmenin yukarısındaki **Başlık** sekmesini açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="3b374-251">**İlişkili Kılavuzlar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3b374-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="3b374-252">**İlişkili Kılavuzlar** araç çubuğundan **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="3b374-253">Kılavuza yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="3b374-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="3b374-254">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="3b374-255">![Formüle Kılavuz ekleme](media/instruction-guides-Formula.png "Formüle Kılavuz ekleme")</span><span class="sxs-lookup"><span data-stu-id="3b374-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="3b374-256">Kılavuzu formül sürümüyle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="3b374-257">Herhangi bir [formül sürümüne](bill-of-material-bom.md#bom-and-formula-versions) kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="3b374-258">Formül sürümlerini kullanan tipik senaryo</span><span class="sxs-lookup"><span data-stu-id="3b374-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="3b374-259">Bir formülün bağımsız bir sürümüne eklenen kılavuzlar, atölye çalışanlarına formül reçetesinin söz konusu sürümünün üretiminde yol gösteren yönergeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="3b374-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="3b374-260">Bir rotaya, rota sürümüne veya rota operasyon ilişkilerine bu formül sürümüne dayalı olarak üretim süreçleriyle ilgili kılavuz atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="3b374-261">Kılavuzlar, şu anda bireysel formül satırlarına eklenemez.</span><span class="sxs-lookup"><span data-stu-id="3b374-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="3b374-262">Formül sürümüne Kılavuz ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="3b374-263">Formül sürümüne Kılavuz eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="3b374-264">**Üretim bilgi yönetimi \> Ürün reçeteleri ve formülleri \> Formüller** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="3b374-265">Kılavuza atamak istediğiniz sürümü içeren formülü açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-266">Üst hızlı sekmenin yukarısındaki **Başlık** sekmesini açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="3b374-267">**Formül sürümleri** hızlı sekmesinde, Kılavuz atamak istediğiniz sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-268">**Formül sürümleri** araç çubuğunda **İlişkili Kılavuzlar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="3b374-269">![Seçili formül sürümüyle ilişkilendirilen Kılavuzları açma](media/instruction-guides-FormulaVersion.png "Seçili formül sürümüyle ilişkilendirilen Kılavuzları açma")</span><span class="sxs-lookup"><span data-stu-id="3b374-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="3b374-270">Formül sürümünüz için **İlişkili Kılavuzlar** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="3b374-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="3b374-271">Eylem bölmesinde, kılavuza yeni satır eklemek için **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="3b374-272">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="3b374-273">![Formül sürümüne Kılavuz ekleme](media/instruction-guides-FormulaVersionAddGuide.png "Formül sürümüne Kılavuz ekleme")</span><span class="sxs-lookup"><span data-stu-id="3b374-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="3b374-274">Kılavuzu ürün reçeteleriyle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="3b374-275">Herhangi bir [ürün reçetesine](bill-of-material-bom.md) (BOM) bir kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="3b374-276">Ürün reçeteleri kullanan tipik senaryo</span><span class="sxs-lookup"><span data-stu-id="3b374-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="3b374-277">Ürün reçetesine iliştirilen kılavuzlar, atölye çalışanlarına bir ürün reçetesinin nasıl hazırlanacağını ve işleneceğini açıklayan yönergeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="3b374-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="3b374-278">Kılavuzlar, bir ürün reçetesinin sürümlerine de atanabilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="3b374-279">Kılavuzlar, şu anda bireysel BOM satırlarına eklenemez.</span><span class="sxs-lookup"><span data-stu-id="3b374-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="3b374-280">Ürün reçetelerine Kılavuz ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="3b374-281">Ürün reçeteine Kılavuz eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="3b374-282">**Ürün bilgi yönetimi \> Ürün reçeteleri ve formüller \> Ürün reçetesi** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="3b374-283">Kılavuz atamak istediğiniz ürün reçetesini açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-284">Üst hızlı sekmenin yukarısındaki **Başlık** sekmesini açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="3b374-285">**İlişkili Kılavuzlar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3b374-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="3b374-286">**İlişkili Kılavuzlar** araç çubuğundan **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="3b374-287">Kılavuza yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="3b374-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="3b374-288">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="3b374-289">![BOM'a Kılavuz ekleme](media/instruction-guides-BOM.png "BOM'a Kılavuz ekleme")</span><span class="sxs-lookup"><span data-stu-id="3b374-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="3b374-290">Kılavuzu ürün reçetesi sürümüyle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="3b374-291">Herhangi bir [ürün reçetesi sürümüne](bill-of-material-bom.md#bom-and-formula-versions) bir kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="3b374-292">Ürün reçetesi sürümleri kullanan tipik senaryo</span><span class="sxs-lookup"><span data-stu-id="3b374-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="3b374-293">Tek bir ürün reçetesi sürümüne iliştirilmiş kılavuzlar, atölye çalışanlarına genel ürün reçetesinden veya bunun diğer sürümlerinden farklı bir ürün reçetesi sürümü için malzemenin nasıl hazırlanacağını ve işleneceğini açıklayan yönergeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="3b374-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="3b374-294">Kılavuzlar, şu anda bireysel BOM satırlarına eklenemez.</span><span class="sxs-lookup"><span data-stu-id="3b374-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="3b374-295">Ürün reçetesi sürümüne Kılavuz ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="3b374-296">Ürün reçetesi sürümüne Kılavuz eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="3b374-297">**Ürün bilgi yönetimi \> Ürün reçeteleri ve formüller \> Ürün reçetesi** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="3b374-298">Kılavuza atamak istediğiniz sürümü içeren BOM'u açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-299">Üst hızlı sekmenin yukarısındaki **Başlık** sekmesini açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="3b374-300">**BOM sürümleri** hızlı sekmesinde, Kılavuz atamak istediğiniz sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-301">**BOM sürümleri** araç çubuğunda **İlişkili Kılavuzlar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="3b374-302">![Seçili BOM sürümüyle ilişkilendirilen Kılavuzları açma](media/instruction-guides-BOMVersion.png "Seçili BOM sürümüyle ilişkilendirilen Kılavuzları açma")</span><span class="sxs-lookup"><span data-stu-id="3b374-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="3b374-303">BOM sürümünüz için **İlişkili Kılavuzlar** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="3b374-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="3b374-304">Eylem bölmesinde, kılavuza yeni satır eklemek için **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="3b374-305">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="3b374-306">![BOM sürümüne Kılavuz ekleme](media/instruction-guides-BOMVersionAddGuide.png "BOM sürümüne Kılavuz ekleme")</span><span class="sxs-lookup"><span data-stu-id="3b374-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="3b374-307">Kılavuzu rotayla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-307">Associate a Guide to a route</span></span>

<span data-ttu-id="3b374-308">Herhangi bir [rotaya](routes-operations.md) kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="3b374-309">Rotaları kullanan tipik senaryo</span><span class="sxs-lookup"><span data-stu-id="3b374-309">Typical scenario using routes</span></span>

<span data-ttu-id="3b374-310">Rotalar genellikle, belirli bir serbest bırakılan ürünün bir ürün reçetesine veya ürün reçetesi sürümüne dayalı olup, bir dizi kaynak veya kaynak grubu ile ilgili olarak nasıl üretileceğini belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3b374-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="3b374-311">İlgili üretim işlemiyle ilgili adım adım yönergeler sağlamak için bir rotaya bir kılavuz atayın.</span><span class="sxs-lookup"><span data-stu-id="3b374-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="3b374-312">Rotaya Kılavuz ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-312">Add a Guide to a route</span></span>

<span data-ttu-id="3b374-313">Rotaya Kılavuz eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="3b374-314">**Üretim denetimi \> Tüm rotalar** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="3b374-315">Kılavuz atamak istediğiniz rotayı açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-316">**İlişkili Kılavuzlar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3b374-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="3b374-317">**İlişkili Kılavuzlar** araç çubuğundan **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="3b374-318">Kılavuza yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="3b374-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="3b374-319">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="3b374-320">![Rotaya Kılavuz ekleme](media/instruction-guides-Route.png "Rotaya Kılavuz ekleme")</span><span class="sxs-lookup"><span data-stu-id="3b374-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="3b374-321">Kılavuzu rota sürümüyle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="3b374-322">Herhangi bir [rota sürümüne](routes-operations.md#route-versions) kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="3b374-323">Rota sürümlerini kullanan tipik senaryo</span><span class="sxs-lookup"><span data-stu-id="3b374-323">Typical scenario using route versions</span></span>

<span data-ttu-id="3b374-324">Rota sürümleri genellikle, varolan bir rotaya dayalı olarak üretim süreçlerinin varyantlarını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3b374-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="3b374-325">Her rota sürümüne farklı Kılavuzlar atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="3b374-326">Rota sürümüne Kılavuz ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-326">Add a Guide to a route version</span></span>

<span data-ttu-id="3b374-327">Rota sürümüne Kılavuz eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="3b374-328">**Üretim denetimi \> Tüm rotalar** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="3b374-329">Kılavuz atamak istediğiniz rotayı açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-330">**Sürümler** hızlı sekmesinde, Kılavuz atamak istediğiniz sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-331">**Sürümler** araç çubuğunda **İlişkili Kılavuzlar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="3b374-332">![Seçili rota sürümüyle ilişkilendirilen Kılavuzları açma](media/instruction-guides-RouteVersion.png "Seçili rota sürümüyle ilişkilendirilen Kılavuzları açma")</span><span class="sxs-lookup"><span data-stu-id="3b374-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="3b374-333">BOM sürümünüz için **İlişkili Kılavuzlar** sayfası açılır.</span><span class="sxs-lookup"><span data-stu-id="3b374-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="3b374-334">Eylem bölmesinde, kılavuza yeni satır eklemek için **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="3b374-335">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="3b374-336">![Rota sürümüne Kılavuz ekleme](media/instruction-guides-RouteVersionAddGuide.png "Rota sürümüne Kılavuz ekleme")</span><span class="sxs-lookup"><span data-stu-id="3b374-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="3b374-337">Kılavuzu rota operasyonu ilişkisiyle ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="3b374-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="3b374-338">Herhangi bir [rota operasyonu ilişkisine](routes-operations.md#operation-relations) kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="3b374-339">Rota operasyonu ilişkilerini kullanan tipik senaryo</span><span class="sxs-lookup"><span data-stu-id="3b374-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="3b374-340">Operasyon ilişkileri, bir ürün işlemine ve ilgili operasyonlarına rehberlik eklemenin en belirgin yoludur.</span><span class="sxs-lookup"><span data-stu-id="3b374-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="3b374-341">Bir rotadaki her operasyon için rehberlik belirtebilir ve belirli maddeler, yapılandırmalar ve daha fazlası gibi bir rotaya ilişkin herhangi bir ilişki bağlamı türü için farklı bir kılavuz belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="3b374-342">Ayrıca, kılavuzun operasyonda uyguladığı aşamaları (kurulum, kuyruğa alma, işleme veya taşıma gibi) belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="3b374-343">Bir rotanın çeşitli operasyon ilişkileri için kılavuzlar belirtirseniz, bu kılavuzlar arasından yalnızca en belirli ilişkilerden gelen kılavuz oluşturulan iş için atölyede gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="3b374-344">Kılavuzu rota operasyonu ilişkisine ekleme</span><span class="sxs-lookup"><span data-stu-id="3b374-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="3b374-345">Kılavuzu rota operasyonu ilişkisine eklemek için:</span><span class="sxs-lookup"><span data-stu-id="3b374-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="3b374-346">**Üretim denetimi \> Tüm rotalar** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3b374-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="3b374-347">Kılavuz atamak istediğiniz rotayı açın.</span><span class="sxs-lookup"><span data-stu-id="3b374-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="3b374-348">Eylem Bölmesinde, **Rota** sekmesini açın ve **Yönet** grubundan **Rota ayrıntıları** 'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="3b374-349">**Rota ayrıntıları** sayfası, seçtiğiniz rota için açılır.</span><span class="sxs-lookup"><span data-stu-id="3b374-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="3b374-350">Üst kılavuzda, kılavuzluk sağlamak istediğiniz işlemi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="3b374-351">Alt kılavuzda, belirli bir ilişki (veya genel **Tümü** ilişkisini) seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="3b374-352">![Bir operasyon ve ardından bir ilişki seçin](media/instruction-guides-RouteOperationRelation.png "Bir operasyon ve ardından bir ilişki seçin")</span><span class="sxs-lookup"><span data-stu-id="3b374-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="3b374-353">Alt kılavuzun üzerinde, **İlişkili kılavuzlar** sekmesini açın. ![İlişkili Kılavuzlar sekmesi](media/instruction-guides-RouteOperationRelation-AddGuide.png "İlişkili Kılavuzlar sekmesi")</span><span class="sxs-lookup"><span data-stu-id="3b374-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="3b374-354">Kılavuza yeni bir satır eklemek için, alt kılavuzun üstündeki araç çubuğundan **Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="3b374-355">Yeni satır için, **Ad** sütunundaki açılan listeyi kullanarak atamak istediğiniz Kılavuzu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="3b374-356">Satırın geri kalanında, seçili Kılavuzun kullanılabilir olması gereken her bağlamın onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="3b374-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="3b374-357">Her bir operasyonun her aşaması için bir veya daha fazla kılavuz ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b374-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="3b374-358">Atölye yürütme arabiriminden kılavuz seçme</span><span class="sxs-lookup"><span data-stu-id="3b374-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="3b374-359">Bir çalışan atölye yürütme arabiriminde bir iş listesi açtığında, Supply Chain Management gösterilen işler için ilgili kılavuzları bulur.</span><span class="sxs-lookup"><span data-stu-id="3b374-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="3b374-360">İlgili kılavuzları görüntülemek için **Kılavuzlar** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b374-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="3b374-361">![Atölye yürütme arabirimindeki Kılavuzlar düğmesi](media/instruction-guides-Shopfloor1.png "Atölye yürütme arabirimindeki Kılavuzlar düğmesi")</span><span class="sxs-lookup"><span data-stu-id="3b374-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="3b374-362">Daha sonra HoloLens'e yerleştirin ve QR kodunu kullanarak ve ilgili Kılavuzu etkinleştirerek ilgili kılavuza erişin.</span><span class="sxs-lookup"><span data-stu-id="3b374-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="3b374-363">![HoloLens kullanarak kılavuzlara erişmek için QR kodu](media/instruction-guides-Shopfloor2.png "HoloLens kullanarak kılavuzlara erişmek için QR kodu")</span><span class="sxs-lookup"><span data-stu-id="3b374-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="3b374-364">Kılavuz seçme mantığını çözme</span><span class="sxs-lookup"><span data-stu-id="3b374-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="3b374-365">Aşağıdaki üretim verilerine Kılavuzlar ekleyebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="3b374-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="3b374-366">Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3b374-366">Resources</span></span>](#resources)
- [<span data-ttu-id="3b374-367">Kaynak grupları</span><span class="sxs-lookup"><span data-stu-id="3b374-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="3b374-368">Serbest bırakılan ürünler</span><span class="sxs-lookup"><span data-stu-id="3b374-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="3b374-369">Formüller</span><span class="sxs-lookup"><span data-stu-id="3b374-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="3b374-370">Formül sürümleri</span><span class="sxs-lookup"><span data-stu-id="3b374-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="3b374-371">Ürün reçeteleri (BOM'lar)</span><span class="sxs-lookup"><span data-stu-id="3b374-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="3b374-372">BOM sürümleri</span><span class="sxs-lookup"><span data-stu-id="3b374-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="3b374-373">Rotalar</span><span class="sxs-lookup"><span data-stu-id="3b374-373">Routes</span></span>](#routes)
- [<span data-ttu-id="3b374-374">Rota sürümleri</span><span class="sxs-lookup"><span data-stu-id="3b374-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="3b374-375">Rota operasyonu ilişkileri</span><span class="sxs-lookup"><span data-stu-id="3b374-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="3b374-376">Supply Chain Management üretim katı için işleri oluşturduğunda, ilgili Kılavuzları bu kaynaklardan alır.</span><span class="sxs-lookup"><span data-stu-id="3b374-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="3b374-377">Aşağıdaki önemli kurallara dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="3b374-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="3b374-378">Bir rotaya veya üretim emrine ürün reçetesi sürümü veya formül sürümü eklerseniz, bu sürüme iliştirilmiş tüm Kılavuzlar ve ayrıca o sürümün ana ürün reçetesine veya formülüne eklenen kılavuzlar işte gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="3b374-379">Bir üretim emrine rota sürümü eklerseniz, bu sürüme iliştirilmiş tüm Kılavuzlar ve ayrıca o sürümün ana reçetesine eklenen kılavuzlar işte gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="3b374-380">*Tümü* ilişkisi içeren birkaç rota operasyonu ilişkisi tanımlarsanız ve bunlara Kılavuzlar atarsanız, iş için yalnızca en belirgin ilişkideki Kılavuzlar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="3b374-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="3b374-381">![İlgili kılavuzları çözümlemeyle ilgili diyagram](media/instruction-guides-Resolve.png "İlgili kılavuzları çözümlemeyle ilgili diyagram")</span><span class="sxs-lookup"><span data-stu-id="3b374-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>
