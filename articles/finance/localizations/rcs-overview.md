---
title: Regulatory Configuration Service
description: Bu konu, Regulatory Configuration Service (RCS) yeteneklerine genel bakış sağlar ve hizmete nasıl erişebileceğinizi açıklar.
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890812"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="11baf-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="11baf-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11baf-104">Regulatory Configuration Service (RCS), kodsuz/az kodlu genelleştirme işlevi için bağımsız bir tasarımcı ve yaşam döngüsü yönetim hizmetidir.</span><span class="sxs-lookup"><span data-stu-id="11baf-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="11baf-105">RCS, genelleştirme paydaşlarının geliştiricilere gereksinim duymadan vergi, e-faturalama, yasal raporlama, banka ve iş belgelerine ilişkin temel genelleştirme alanlarını genişletmesine ve özelleştirmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="11baf-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="11baf-106">Bu kodsuz/az kodlu genelleştirme yaklaşımı genelleştirmenin daha kolay, hızlı ve daha düşük maliyetli şekilde oluşturulmasını veya genişletilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="11baf-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="11baf-107">RCS aşağıdaki özellikleri sunar:</span><span class="sxs-lookup"><span data-stu-id="11baf-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="11baf-108">Elektronik raporlama (ER) tarafından sağlanan tüm işlevler için destek.</span><span class="sxs-lookup"><span data-stu-id="11baf-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="11baf-109">Yeni genelleştirme mikro hizmetlerini yapılandırmaya yönelik bir önkoşul.</span><span class="sxs-lookup"><span data-stu-id="11baf-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="11baf-110">Elektronik Faturalama desteği.</span><span class="sxs-lookup"><span data-stu-id="11baf-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="11baf-111">Daha fazla bilgi için bkz. [Elektronik Faturalama](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="11baf-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="11baf-112">Vergi Hesaplama destekleri.</span><span class="sxs-lookup"><span data-stu-id="11baf-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="11baf-113">Daha fazla bilgi için bkz. [Vergi hizmeti](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="11baf-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="11baf-114">Çok bileşenli özelliklerinin yaşam döngüsü yönetimini basitleştiren ve eylemleri yapılandırmak ve özellik parametrelerini ayarlamak için ek yetenek sağlayan yeni genelleştirme özelliği işlevselliği için destek.</span><span class="sxs-lookup"><span data-stu-id="11baf-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="11baf-115">Daha fazla bilgi için bkz. [Regulatory Configuration Service – genelleştirme hizmetleri için basitleştirilmiş genelleştirme özelliği yönetimi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="11baf-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="11baf-116">Microsoft Dynamics Lifecycle Services (LCS) kullanılmasına gerek kalmadan, yapılandırma yönetimini basitleştirmek için Genel depodaki özel yapılandırmaları merkezi olarak yayımlama, depolama ve paylaşma desteği.</span><span class="sxs-lookup"><span data-stu-id="11baf-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="11baf-117">RCS'ye erişim</span><span class="sxs-lookup"><span data-stu-id="11baf-117">Access RCS</span></span>

<span data-ttu-id="11baf-118">RCS'ye [Regulatory Configuration Service sayfasından](https://marketing.configure.global.dynamics.com/) kaydolabilir veya oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11baf-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS kaydolma/oturum açma](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="11baf-120">**Regulatory Configuration Service** sayfasında, hizmetin ek kullanım hüküm ve koşullarını inceleyin ve kabul edin ve ardından aşağıdaki düğmelerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="11baf-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="11baf-121">**Kaydol**: Hizmeti ilk kez kullanacaksanız ve kuruluşunuza servis ortamı sağlamak için iş e-posta adresi kullanıyorsanız</span><span class="sxs-lookup"><span data-stu-id="11baf-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="11baf-122">**Oturum aç**: Hizmete daha önce kaydolduysanız ve kuruluşunuzun ortamına erişmek istiyorsanız</span><span class="sxs-lookup"><span data-stu-id="11baf-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="11baf-123">Bölgesel kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="11baf-123">Regional availability</span></span>

<span data-ttu-id="11baf-124">RCS, aşağıdaki bölgelerde genel kullanıma sunulmuştur:</span><span class="sxs-lookup"><span data-stu-id="11baf-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="11baf-125">Amerika Birleşik Devletleri</span><span class="sxs-lookup"><span data-stu-id="11baf-125">United States</span></span>
- <span data-ttu-id="11baf-126">Hindistan</span><span class="sxs-lookup"><span data-stu-id="11baf-126">India</span></span>
- <span data-ttu-id="11baf-127">Fransa</span><span class="sxs-lookup"><span data-stu-id="11baf-127">France</span></span>
- <span data-ttu-id="11baf-128">Avrupa</span><span class="sxs-lookup"><span data-stu-id="11baf-128">Europe</span></span>

<span data-ttu-id="11baf-129">Bölgelerin tam listesi için bkz. [Dynamics 365 ve Power Platform: Kullanılabilirlik, veri konumu, dil ve yerelleştirme](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="11baf-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="11baf-130">İlgili RCS belgeleri</span><span class="sxs-lookup"><span data-stu-id="11baf-130">Related RCS documentation</span></span>

<span data-ttu-id="11baf-131">İlgili bileşenler hakkında daha fazla bilgi için aşağıdaki belgelere bakın:</span><span class="sxs-lookup"><span data-stu-id="11baf-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="11baf-132">**Genel depo:**</span><span class="sxs-lookup"><span data-stu-id="11baf-132">**Global repository:**</span></span>

    - [<span data-ttu-id="11baf-133">ER yapılandırması oluşturma ve Genel depoya yükleme</span><span class="sxs-lookup"><span data-stu-id="11baf-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="11baf-134">Genel depoda yapılandırma paylaşma</span><span class="sxs-lookup"><span data-stu-id="11baf-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="11baf-135">Genel depoda gelişmiş filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="11baf-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="11baf-136">Genel depodan ER yapılandırmalarını indirme</span><span class="sxs-lookup"><span data-stu-id="11baf-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="11baf-137">Genel depodaki yapılandırmaları durdurma</span><span class="sxs-lookup"><span data-stu-id="11baf-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="11baf-138">**Genelleştirme özelliği:**</span><span class="sxs-lookup"><span data-stu-id="11baf-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="11baf-139">Regulatory Configuration Service (RCS) - Genelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="11baf-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)