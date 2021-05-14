---
title: Kalite ve uygunsuzluk yönetimini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite ve uygunsuzluk yönetimi özelliklerini ayarlama ve yapılandırma işlemine genel bakış sağlar.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956266"
---
# <a name="enable-quality-and-nonconformance-management"></a><span data-ttu-id="6449e-103">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6449e-103">Enable quality and nonconformance management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6449e-104">Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta kalite ve uygunsuzluk yönetimi özelliklerini ayarlama ve yapılandırma işlemine genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="6449e-104">This topic provides an overview of the process for setting up and configuring quality and nonconformance management features in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a><span data-ttu-id="6449e-105">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6449e-105">Enable quality and nonconformance management</span></span>

<span data-ttu-id="6449e-106">Sisteminizde kalite yönetimini etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6449e-106">Follow these steps to enable quality management on your system.</span></span>

1. <span data-ttu-id="6449e-107">**Stok yönetimi \> Kurulum \> Stok ve ambar yönetim parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="6449e-107">Go to **Inventory management \> Setup \> Inventory and warehouse management parameters**.</span></span>
1. <span data-ttu-id="6449e-108">**Kalite yönetimi** sekmesinde, **Kalite yönetimi kullan** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6449e-108">On the **Quality management** tab, set the **Use quality management** option to *Yes*.</span></span>
1. <span data-ttu-id="6449e-109">**Saatlik ücret** alanına saatlik işçilik ücretini yerel para birimi cinsinden girin.</span><span class="sxs-lookup"><span data-stu-id="6449e-109">In the **Hourly rate** field, enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="6449e-110">Saatlik ücret, uygunsuzlukla ilgili operasyonlar için maliyetlerin hesaplanmasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6449e-110">The hourly rate is used to calculate costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="6449e-111">Saatlik ücret ve hesaplanan maliyetler bir uyumsuzluk için referans bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="6449e-111">The hourly rate and calculated costs provide reference information for a nonconformance.</span></span> <span data-ttu-id="6449e-112">Diğer işlevlerle bir etkileşimi yoktur.</span><span class="sxs-lookup"><span data-stu-id="6449e-112">They don't interact with other functionality.</span></span>
1. <span data-ttu-id="6449e-113">**Rapor kurulumu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="6449e-113">Select **Report setup**.</span></span>
1. <span data-ttu-id="6449e-114">Çeşitli rapor türleri için yeni satırlar ekleyin ve her raporda kullanılacak belge türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="6449e-114">Add new lines for the various report types, and select the type of document to use for each report.</span></span>
1. <span data-ttu-id="6449e-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6449e-115">Close the page.</span></span>
1. <span data-ttu-id="6449e-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="6449e-116">Close the page.</span></span>

## <a name="quality-management-configuration-process"></a><span data-ttu-id="6449e-117">Kalite yönetimini yapılandırma işlemi</span><span class="sxs-lookup"><span data-stu-id="6449e-117">Quality management configuration process</span></span>

<span data-ttu-id="6449e-118">Kalite yönetimi özelliklerini kullanmaya ve kalite emirleri oluşturmaya başlamadan önce, sistemi ve önkoşulları yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6449e-118">Before you can start to use the quality management features and generate quality orders, you must configure the system and prerequisites.</span></span> <span data-ttu-id="6449e-119">Kalite yönetimini yapılandırmak için gerekli adımların listesini aşağıda bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6449e-119">Here is a list of the steps that are required to configure quality management.</span></span>

1. <span data-ttu-id="6449e-120">[Kalite ve uygunsuzluk yönetimini etkinleştirme](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="6449e-120">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="6449e-121">İsteğe bağlı: [Test araçlarını yapılandırma](quality-test-instruments.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-121">Optional: [Configure test instruments](quality-test-instruments.md).</span></span>
1. <span data-ttu-id="6449e-122">[Testleri yapılandırma](quality-tests.md)</span><span class="sxs-lookup"><span data-stu-id="6449e-122">[Configure tests](quality-tests.md).</span></span>
1. <span data-ttu-id="6449e-123">[Test değişkenlerini ve sonuçları yapılandırma](quality-test-variables.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-123">[Configure test variables and outcomes](quality-test-variables.md).</span></span>
1. <span data-ttu-id="6449e-124">[Test gruplarını yapılandırma](quality-test-groups.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-124">[Configure test groups](quality-test-groups.md).</span></span>
1. <span data-ttu-id="6449e-125">İsteğe bağlı: [Kalite gruplarını yapılandırma ve ürünlerle ilişkilendirme](quality-groups.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-125">Optional: [Configure quality groups, and link to products](quality-groups.md).</span></span>
1. <span data-ttu-id="6449e-126">İsteğe bağlı: [Kalite ilişkilendirmelerini yapılandırma](quality-associations.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-126">Optional: [Configure quality associations](quality-associations.md).</span></span>

<span data-ttu-id="6449e-127">Yapılandırma tamamlandıktan sonra, kalite emirleri oluşturmaya ve işlemeye başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6449e-127">After the configuration is completed, you can start to create and process quality orders.</span></span> <span data-ttu-id="6449e-128">Kalite emirleriyle çalışma hakkında daha fazla bilgi için bkz. [Kalite emirleri](quality-orders.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-128">For more information about how to create and work with quality orders, see [Quality orders](quality-orders.md).</span></span>

## <a name="nonconformance-management-configuration-process"></a><span data-ttu-id="6449e-129">Uygunsuzluk yönetimini yapılandırma işlemi</span><span class="sxs-lookup"><span data-stu-id="6449e-129">Nonconformance management configuration process</span></span>

<span data-ttu-id="6449e-130">Uygunsuzluk yönetimi özelliklerini kullanmaya ve uygunsuzluklar oluşturmaya başlamadan önce, sistemi ve önkoşulları yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6449e-130">Before you can start to use the nonconformance management features and generate nonconformances, you must configure the system and prerequisites.</span></span> <span data-ttu-id="6449e-131">Uygunsuzluk yönetimini yapılandırmak için gerekli adımların listesini aşağıda bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6449e-131">Here is a list of the steps that are required to configure nonconformance management.</span></span>

1. <span data-ttu-id="6449e-132">[Kalite ve uygunsuzluk yönetimini etkinleştirme](#enable-qm).</span><span class="sxs-lookup"><span data-stu-id="6449e-132">[Enable quality and nonconformance management](#enable-qm).</span></span>
1. <span data-ttu-id="6449e-133">[Uygunsuzlukları onaylamaktan sorumlu çalışanları yapılandırma](quality-responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-133">[Configure workers who are responsible for approving nonconformances](quality-responsible-workers.md).</span></span>
1. <span data-ttu-id="6449e-134">[Sorunlu türlerini yapılandırma](quality-problem-types.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-134">[Configure problem types](quality-problem-types.md).</span></span>
1. <span data-ttu-id="6449e-135">[Karantina bölgelerini yapılandırma](quality-quarantine-zones.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-135">[Configure quarantine zones](quality-quarantine-zones.md).</span></span>
1. <span data-ttu-id="6449e-136">[Tanılama türlerini yapılandırma](quality-diagnostic-types.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-136">[Configure diagnostic types](quality-diagnostic-types.md).</span></span>
1. <span data-ttu-id="6449e-137">[İşlemleri yapılandırma](quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-137">[Configure operations](quality-operations.md).</span></span>
1. <span data-ttu-id="6449e-138">İsteğe bağlı: [Kalite giderlerini yapılandırma](quality-charges.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-138">Optional: [Configure quality charges](quality-charges.md).</span></span>

<span data-ttu-id="6449e-139">Yapılandırma tamamlandıktan sonra, uygunsuzluklar oluşturmaya ve işlemeye başlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6449e-139">After the configuration is completed, you can start to create and process nonconformances.</span></span> <span data-ttu-id="6449e-140">Uygunsuzluk oluşturma ve bunlarla çalışma hakkında daha fazla bilgi için bkz. [Uygunsuzluklar oluşturma ve işleme](tasks/create-process-non-conformance.md).</span><span class="sxs-lookup"><span data-stu-id="6449e-140">For more information about how to create and work with nonconformances, see [Create and process nonconformances](tasks/create-process-non-conformance.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6449e-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6449e-141">Additional resources</span></span>

- [<span data-ttu-id="6449e-142">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="6449e-142">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="6449e-143">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6449e-143">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="6449e-144">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="6449e-144">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
