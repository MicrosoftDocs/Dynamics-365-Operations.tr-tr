---
title: Regulatory Configuration Service
description: Bu konu, Regulatory Configuration Service (RCS) yeteneklerine genel bakış sağlar ve hizmete nasıl erişebileceğinizi açıklar.
author: JaneA07
ms.date: 06/04/2021
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
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216574"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="9f3d7-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="9f3d7-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f3d7-104">Regulatory Configuration Service (RCS), kodsuz/az kodlu genelleştirme işlevi için bağımsız bir tasarımcı ve yaşam döngüsü yönetim hizmetidir.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="9f3d7-105">RCS, genelleştirme paydaşlarının geliştiricilere gereksinim duymadan vergi, e-faturalama, yasal raporlama, banka ve iş belgelerine ilişkin temel genelleştirme alanlarını genişletmesine ve özelleştirmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="9f3d7-106">Bu kodsuz/az kodlu genelleştirme yaklaşımı genelleştirmenin daha kolay, hızlı ve daha düşük maliyetli şekilde oluşturulmasını veya genişletilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="9f3d7-107">RCS aşağıdaki özellikleri sunar:</span><span class="sxs-lookup"><span data-stu-id="9f3d7-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="9f3d7-108">Elektronik raporlama (ER) tarafından sağlanan tüm işlevler için destek.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="9f3d7-109">Yeni genelleştirme mikro hizmetlerini yapılandırmaya yönelik bir önkoşul.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="9f3d7-110">Elektronik Faturalama desteği.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="9f3d7-111">Daha fazla bilgi için bkz. [Elektronik Faturalama](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="9f3d7-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="9f3d7-112">Vergi Hesaplama destekleri.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="9f3d7-113">Daha fazla bilgi için bkz. [Vergi hizmeti](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="9f3d7-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="9f3d7-114">Çok bileşenli özelliklerinin yaşam döngüsü yönetimini basitleştiren ve eylemleri yapılandırmak ve özellik parametrelerini ayarlamak için ek yetenek sağlayan yeni genelleştirme özelliği işlevselliği için destek.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="9f3d7-115">Daha fazla bilgi için bkz. [Regulatory Configuration Service – genelleştirme hizmetleri için basitleştirilmiş genelleştirme özelliği yönetimi](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="9f3d7-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="9f3d7-116">Microsoft Dynamics Lifecycle Services (LCS) kullanılmasına gerek kalmadan, yapılandırma yönetimini basitleştirmek için Genel depodaki özel yapılandırmaları merkezi olarak yayımlama, depolama ve paylaşma desteği.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="9f3d7-117">RCS'ye erişim</span><span class="sxs-lookup"><span data-stu-id="9f3d7-117">Access RCS</span></span>

<span data-ttu-id="9f3d7-118">RCS'ye [Regulatory Configuration Service sayfasından](https://marketing.configure.global.dynamics.com/) kaydolabilir veya oturum açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS kaydolma/oturum açma](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="9f3d7-120">**Regulatory Configuration Service** sayfasında, hizmetin ek kullanım hüküm ve koşullarını inceleyin ve kabul edin ve ardından aşağıdaki düğmelerden birini seçin:</span><span class="sxs-lookup"><span data-stu-id="9f3d7-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="9f3d7-121">**Kaydol**: Hizmeti ilk kez kullanacaksanız ve kuruluşunuza servis ortamı sağlamak için iş e-posta adresi kullanıyorsanız</span><span class="sxs-lookup"><span data-stu-id="9f3d7-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="9f3d7-122">**Oturum aç**: Hizmete daha önce kaydolduysanız ve kuruluşunuzun ortamına erişmek istiyorsanız</span><span class="sxs-lookup"><span data-stu-id="9f3d7-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="9f3d7-123">Bölgesel kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="9f3d7-123">Regional availability</span></span>

<span data-ttu-id="9f3d7-124">RCS, aşağıdaki bölgelerde genel kullanıma sunulmuştur:</span><span class="sxs-lookup"><span data-stu-id="9f3d7-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="9f3d7-125">Amerika Birleşik Devletleri</span><span class="sxs-lookup"><span data-stu-id="9f3d7-125">United States</span></span>
- <span data-ttu-id="9f3d7-126">Hindistan</span><span class="sxs-lookup"><span data-stu-id="9f3d7-126">India</span></span>
- <span data-ttu-id="9f3d7-127">Fransa</span><span class="sxs-lookup"><span data-stu-id="9f3d7-127">France</span></span>
- <span data-ttu-id="9f3d7-128">Avrupa</span><span class="sxs-lookup"><span data-stu-id="9f3d7-128">Europe</span></span>

<span data-ttu-id="9f3d7-129">Bölgelerin tam listesi için bkz. [Dynamics 365 ve Power Platform: Kullanılabilirlik, veri konumu, dil ve yerelleştirme](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="9f3d7-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="9f3d7-130">RCS varsayılan şirket</span><span class="sxs-lookup"><span data-stu-id="9f3d7-130">RCS default company</span></span>

<span data-ttu-id="9f3d7-131">RCS'de kullanılan tasarım zamanı işlevi tüm şirketler arasında paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="9f3d7-132">Şirkete özgü işlevler yoktur.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-132">There is no company-specific functionality.</span></span> <span data-ttu-id="9f3d7-133">Bu nedenle, RCS ortamınızla bir şirket, **DAT**, kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="9f3d7-134">Ancak bazı senaryolarda, ER biçimlerinin belirli bir tüzel kişilikle ilişkili parametreleri kullanmasını isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="9f3d7-135">Yalnızca bu senaryolarda, varsayılan şirket değiştiricisini kullanmalısınız.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="9f3d7-136">Örneğin, bkz. [ER biçimini her tüzel kişilik için belirtilen parametreleri kullanmak üzere yapılandırma](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md)</span><span class="sxs-lookup"><span data-stu-id="9f3d7-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="9f3d7-137">İlgili RCS belgeleri</span><span class="sxs-lookup"><span data-stu-id="9f3d7-137">Related RCS documentation</span></span>

<span data-ttu-id="9f3d7-138">İlgili bileşenler hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="9f3d7-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="9f3d7-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="9f3d7-139">**RCS:**</span></span>

    - [<span data-ttu-id="9f3d7-140">RCS'de ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme</span><span class="sxs-lookup"><span data-stu-id="9f3d7-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="9f3d7-141">**Genel depo:**</span><span class="sxs-lookup"><span data-stu-id="9f3d7-141">**Global repository:**</span></span>

    - [<span data-ttu-id="9f3d7-142">ER yapılandırması oluşturma ve Genel depoya yükleme</span><span class="sxs-lookup"><span data-stu-id="9f3d7-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="9f3d7-143">Genel depoda yapılandırma paylaşma</span><span class="sxs-lookup"><span data-stu-id="9f3d7-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="9f3d7-144">Genel depoda gelişmiş filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="9f3d7-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="9f3d7-145">Genel depodan ER yapılandırmalarını indirme</span><span class="sxs-lookup"><span data-stu-id="9f3d7-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="9f3d7-146">Genel depodaki yapılandırmaları durdurma</span><span class="sxs-lookup"><span data-stu-id="9f3d7-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="9f3d7-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) depolama kullanımdan kalkma</span><span class="sxs-lookup"><span data-stu-id="9f3d7-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="9f3d7-148">**Genelleştirme özelliği:**</span><span class="sxs-lookup"><span data-stu-id="9f3d7-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="9f3d7-149">Regulatory Configuration Service (RCS) - Genelleştirme özelliği</span><span class="sxs-lookup"><span data-stu-id="9f3d7-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="9f3d7-150">RCS'ye kaydolmayla ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="9f3d7-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="9f3d7-151">Hizmet sayfasından RCS'ye kayolduğunuzda Azure Active Directory (Azure AD) ile ilgili bir sorunla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="9f3d7-152">Aldığınız hata iletisi, RCS kaydolma işleminin şu an kapalı olduğunu ve kaydolma işlemini tamamlayabilmeniz için etkinleştirilmesi gerektiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![RCS kaydolma hata iletisi](media/01_RCSSignUpError.jpg)

<span data-ttu-id="9f3d7-154">Sorun, dinamik aboneliklere kaydolma izniniz olmadığını ve `AllowAdHocSubscriptions` özelliğinin kiracınızda etkin olması gerektiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="9f3d7-155">BT departmanınız, kuruluşunuzun Azure kiracılarını yönetiyorsa sorunu bildirmek için BT departmana başvurun.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="9f3d7-156">Azure kiralamalarınızı yönetmekten siz sorumluysanız, [Azure Active Directory için self servis kaydolma nedir](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings) bölümündeki adımları izleyerek bu sorunları çözebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f3d7-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
