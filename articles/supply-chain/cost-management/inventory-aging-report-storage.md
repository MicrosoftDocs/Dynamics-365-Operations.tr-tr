---
title: Stok eskime raporu depolama
description: Bu konuda, bir Stok yaşlandırma raporu çalıştırmanıza ve çıktının form ve grafik olarak kullanılabilmesini sağlamanıza olanak tanıyan işlevler açıklanmaktadır.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9148a9032615222a1fdfe453488e716bacadbabc
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275591"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="1ecf7-103">Stok eskime raporu depolama</span><span class="sxs-lookup"><span data-stu-id="1ecf7-103">Inventory aging report storage</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="1ecf7-104">Microsoft Dynamics 365 Supply Chain Management'ta, bir **Stok yaşlandırma raporu depolama** raporu çalıştırabilir ve çıktının form ve grafik olarak kullanılabilmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="1ecf7-105">Formda, sütunlar ve toplam bakiyeler yapılandırılan düzene göre dinamik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="1ecf7-106">Grafik, filtrelemeyi destekleyen ve ayrıntılara inmenizi sağlayan görsel bir genel bakış sunar.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="1ecf7-107">Ek olarak, **Stok yaşlandırma raporu** olarak adlandırılan bir veri varlığı, **Stok yaşlandırma raporu depolama** raporunun sonuçlarını Microsoft Excel dosyası veya PDF dosyası gibi bir biçimde dışa aktarmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="1ecf7-108">Bu **Stok yaşlandırma raporu depolama** raporunu çalıştırma yöntemi, çıktının çok fazla satır içerdiği durumlarda yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="1ecf7-109">Örneğin, 50.000 madde ve ambar olarak oluşturulan 300 mağazanız varsa ve ürüne, tesise ve ambara göre stok yaşlandırma yapmak istiyorsanız çıktı çok fazla satır içerir.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="1ecf7-110">Stok değeri depolama raporu özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1ecf7-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="1ecf7-111">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="1ecf7-112">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="1ecf7-113">Burada, özellik şu şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="1ecf7-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="1ecf7-114">**Modül**: Maliyet yönetimi</span><span class="sxs-lookup"><span data-stu-id="1ecf7-114">**Module** - Cost management</span></span>
- <span data-ttu-id="1ecf7-115">**Özellik adı** - Stok yaşlandırma raporu depolama</span><span class="sxs-lookup"><span data-stu-id="1ecf7-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="1ecf7-116">Stok yaşlandırma raporu depolaması çalıştırma</span><span class="sxs-lookup"><span data-stu-id="1ecf7-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="1ecf7-117">**Maliyet yönetimi \> Sorgular ve raporlar \> Stok yaşlandırma raporu depolama alanı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="1ecf7-118">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-118">Select **New**.</span></span>
1. <span data-ttu-id="1ecf7-119">**İşlem Tanımlayıcısı – Ad** alanına rapor için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="1ecf7-120">**Kimlik – Kod** raporunu seçin ve gerektiği şekilde filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="1ecf7-121">Rapor yürütme her zaman toplu işte yapılır.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="1ecf7-122">Toplu iş tamamlandıktan sonra çıktı **Stok yaşlandırma raporu depolama alanı** sayfasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="1ecf7-123">Çıktıyı geleneksel ızgara düzenine sahip bir form olarak görüntülemek için **Ayrıntıları görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="1ecf7-124">Çıktıyı toplam grafiği olarak görüntülemek için **Grafiği görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ecf7-125">Form, rapor düzeninde tanımlanan alt toplamları içermez.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="1ecf7-126">**Stok yaşlandırma raporu** veri varlığı, **İşlem Tanımlayıcısı – Ad** alanı için bir filtre uygulayarak **Stok yaşlandırma raporu depolama** raporunun çıktısını Veri yönetiminin desteklediği herhangi bir biçimde dışa aktarmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1ecf7-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
