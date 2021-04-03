---
title: Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme
description: Bu konu, Microsoft Dynamics 365 Finance çözümü için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b1b5ac8e256835332a4c53ed2872ee609253ad9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568737"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="55ec2-103">Elektronik raporlama (ER) yapılandırması yaşam döngüsünü yönetme</span><span class="sxs-lookup"><span data-stu-id="55ec2-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55ec2-104">Bu konu, Microsoft Dynamics 365 Finance çözümü için Elektronik raporlama (ER) yapılandırmalarının yaşam döngüsünün nasıl yönetileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="55ec2-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="55ec2-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="55ec2-105">Overview</span></span>

<span data-ttu-id="55ec2-106">Elektronik raporlama (ER), gerekli yasal ve ülkeye özel elektronik belgeleri destekleyen bir motorudur.</span><span class="sxs-lookup"><span data-stu-id="55ec2-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="55ec2-107">Genel olarak, ER tek bir elektronik belge için bir yeteneğin aşağıdaki görevleri gerçekleştirdiğini varsayar.</span><span class="sxs-lookup"><span data-stu-id="55ec2-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="55ec2-108">Daha fazla bilgi için bkz. [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="55ec2-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="55ec2-109">Elektronik belge için bir şablon tasarlayın:</span><span class="sxs-lookup"><span data-stu-id="55ec2-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="55ec2-110">Belgede sunulabilen gerekli veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="55ec2-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="55ec2-111">Temel veriler (veri tabloları, veri varlıkları, sınıflar vb. gibi ).</span><span class="sxs-lookup"><span data-stu-id="55ec2-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="55ec2-112">İşlem belirli özellikler (yürütme tarihi ve saati ve saat dilimi, vb. gibi).</span><span class="sxs-lookup"><span data-stu-id="55ec2-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="55ec2-113">Kullanıcı giriş parametreleri (çalışma zamanı sırasında son kullanıcı tarafından belirtilen).</span><span class="sxs-lookup"><span data-stu-id="55ec2-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="55ec2-114">Son belge biçimini belirtmek için gerekli belgele öğelerini ve topolojilerini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="55ec2-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="55ec2-115">Seçili veri kaynaklarından istenen veri akışını (veri kaynağı bağlantıları aracılığıyla belge biçimi bileşenlerine) tanımlanan belge öğelerine yapılandırın ve işlem denetim mantığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="55ec2-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="55ec2-116">Diğer örneklerde de kullanılabilecek bir şablonu kullanılır hale getirin:</span><span class="sxs-lookup"><span data-stu-id="55ec2-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="55ec2-117">Uygulamada oluşturulmuş bir belge şablonunu ER yapılandırmasına dönüştürün ve yapılandırmayı geçerli örnekten yerel olarak veya LCS içinde depolanabilen XML paketi halinde dışa aktarın.</span><span class="sxs-lookup"><span data-stu-id="55ec2-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="55ec2-118">ER yapılandırmasını uygulama belge şablonuna dönüştürün.</span><span class="sxs-lookup"><span data-stu-id="55ec2-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="55ec2-119">Yerel olarak ve LCS içinde depolanan bir XML paketini geçerli örneğe aktarın.</span><span class="sxs-lookup"><span data-stu-id="55ec2-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="55ec2-120">Bir elektronik belge şablonunu özelleştirin:</span><span class="sxs-lookup"><span data-stu-id="55ec2-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="55ec2-121">Bir LCS şablonunu ER yapılandırması olarak geçerli örneğe getirin.</span><span class="sxs-lookup"><span data-stu-id="55ec2-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="55ec2-122">Bir ER yapılandırmasının özel sürümünü tasarlayın ve taban sürüme bir referans verin.</span><span class="sxs-lookup"><span data-stu-id="55ec2-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="55ec2-123">Bir şablonu belirli bir iş süreciyle uygulama içinde kullanılabilir olacak şekilde tümleştirin:</span><span class="sxs-lookup"><span data-stu-id="55ec2-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="55ec2-124">Uygulamanın işlemle ilgili bir parametrede ilgili yapılandırmaya başvurarak bir ER yapılandırmasını kullanmaya başlayabileceği şekilde ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="55ec2-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="55ec2-125">(Örneğin, faturaları işlemek için elektronik ödeme ileti oluşturmak amacıyla belirli bir Borç hesapları ödeme yönteminde ER yapılandırmasına başvurun).</span><span class="sxs-lookup"><span data-stu-id="55ec2-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="55ec2-126">Belirli bir iş sürecinde şablon kullanın:</span><span class="sxs-lookup"><span data-stu-id="55ec2-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="55ec2-127">Belirli bir iş işleminde ER yapılandırmasını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="55ec2-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="55ec2-128">Örneğin, ER yapılandırmasına referans gösteren bir ödeme yöntemi seçildiğinde faturaları işlemek için bir ödeme yöntemi iletisi oluşturmak için.</span><span class="sxs-lookup"><span data-stu-id="55ec2-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="55ec2-129">Kavramlar</span><span class="sxs-lookup"><span data-stu-id="55ec2-129">Concepts</span></span>
<span data-ttu-id="55ec2-130">Aşağıdaki roller ve ilgili etkinlikler ER yapılandırma yaşam döngüsü ile ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="55ec2-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="55ec2-131">Rol</span><span class="sxs-lookup"><span data-stu-id="55ec2-131">Role</span></span>                                       | <span data-ttu-id="55ec2-132">Faaliyetler</span><span class="sxs-lookup"><span data-stu-id="55ec2-132">Activities</span></span>                                                      | <span data-ttu-id="55ec2-133">Açıklama</span><span class="sxs-lookup"><span data-stu-id="55ec2-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="55ec2-134">Elektronik raporlama işlev danışmanı</span><span class="sxs-lookup"><span data-stu-id="55ec2-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="55ec2-135">ER bileşenleri oluşturun ve yönetin (modeller ve biçimler).</span><span class="sxs-lookup"><span data-stu-id="55ec2-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="55ec2-136">ER etki alanına özgü veri modellerini tasarlayan, elektronik belgeler için gerekli şablonları tasarlayan ve bunları uygun şekilde bağlayan işadamı.</span><span class="sxs-lookup"><span data-stu-id="55ec2-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="55ec2-137">Elektronik raporlama geliştirici</span><span class="sxs-lookup"><span data-stu-id="55ec2-137">Electronic reporting developer</span></span>             | <span data-ttu-id="55ec2-138">Veri modeli eşlemeleri oluşturun ve yönetin.</span><span class="sxs-lookup"><span data-stu-id="55ec2-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="55ec2-139">Gerekli Finance veri kaynaklarını seçen ve bunları ER etki alanına özgü veri modellerine bağlayan uzman.</span><span class="sxs-lookup"><span data-stu-id="55ec2-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="55ec2-140">Muhasebe gözetmeni</span><span class="sxs-lookup"><span data-stu-id="55ec2-140">Accounting supervisor</span></span>                      | <span data-ttu-id="55ec2-141">ER yapılarına başvuran süreçle ilgili ayarları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="55ec2-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="55ec2-142">Örneğin, bir ER yapılandırmasının ayarlarının faturaların işlenmesi için elektronik ödeme iletisi oluşturmak amacıyla belirli bir Borç hesapları ödeme yönteminde kullanılmasına izin veren bir **Muhasebe gözetmeni** rolü.</span><span class="sxs-lookup"><span data-stu-id="55ec2-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="55ec2-143">Borç hesapları ödeme memuru</span><span class="sxs-lookup"><span data-stu-id="55ec2-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="55ec2-144">ER yapılarını belirli bir iş sürecinde kullanın.</span><span class="sxs-lookup"><span data-stu-id="55ec2-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="55ec2-145">Örneğin, belirli bir ödeme yöntemi için yapılandırılan ER biçimine göre faturaların işlenmesi için elektronik ödeme iletileri oluşturulmasına izin veren **Borç hesapları ödeme memuru** rolü.</span><span class="sxs-lookup"><span data-stu-id="55ec2-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="55ec2-146">ER yapılandırması geliştirme yaşam döngüsü</span><span class="sxs-lookup"><span data-stu-id="55ec2-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="55ec2-147">Aşağıdaki ER ile ilgili nedenlerden dolayı, ER yapılandırmalarını geliştirme ortamında ayrı Finance and Operations kurulumları olarak tasarlamanızı öneririz:</span><span class="sxs-lookup"><span data-stu-id="55ec2-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="55ec2-148">**Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar yapılandırmaları düzenleyebilir ve sınama amacıyla bunları çalıştırabilir.</span><span class="sxs-lookup"><span data-stu-id="55ec2-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="55ec2-149">Bu senaryo iş verilerine ve örneğin performansına zararı olabilecek sınıflar ve tabloların çağrı yöntemlerine neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="55ec2-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="55ec2-150">ER yapılandırmasının ER veri kaynağı olarak sınıflar ve tabloların çağrı yöntemleri giriş noktaları ve oturum açan şirket içeriği ile sınırlı değildir.</span><span class="sxs-lookup"><span data-stu-id="55ec2-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="55ec2-151">Bu nedenle, **Elektronik raporlama geliştirici** rolü veya **Elektronik raporlama işlev danışmanı** rolündeki kullanıcılar iş açısından hassas verilere erişebilir.</span><span class="sxs-lookup"><span data-stu-id="55ec2-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="55ec2-152">Geliştirme ortamı içinde tasarlanan ER yapılandırmaları, yapılandırma değerlendirmesi (uygun işlem tümleştirme, sonuçların doğruluğu ve performans) ve kalite güvencesi (role dayalı erişim hakları doğruluğu ve görev ayrımı gibi) için test ortamı'na yüklenebilir.</span><span class="sxs-lookup"><span data-stu-id="55ec2-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="55ec2-153">ER yapılandırması değişimi sağlayan özellikler bu amaçla kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="55ec2-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="55ec2-154">Son olarak, kanıtlanan ER yapılandırmaları hizmet aboneleri ile paylaşılmak için LCS'ye veya iç kullanım için üretim ortamına yüklenebilir, aşağıdaki resimlerde gösterildiği gibi.</span><span class="sxs-lookup"><span data-stu-id="55ec2-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![ER yapılandırma yaşam döngüsü](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="55ec2-156">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="55ec2-156">Additional resources</span></span>

[<span data-ttu-id="55ec2-157">Elektronik raporlamaya (ER) genel bakış</span><span class="sxs-lookup"><span data-stu-id="55ec2-157">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]