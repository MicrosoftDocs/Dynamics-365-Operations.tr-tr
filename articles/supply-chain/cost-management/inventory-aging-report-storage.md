---
title: Stok eskime raporu
description: Bu konuda, bir Stok yaşlandırma raporu çalıştırmanıza ve çıktının form ve grafik olarak kullanılabilmesini sağlamanıza olanak tanıyan işlevler açıklanmaktadır.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810263"
---
# <a name="inventory-aging-report"></a><span data-ttu-id="363be-103">Stok eskime raporu</span><span class="sxs-lookup"><span data-stu-id="363be-103">Inventory aging report</span></span>


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="363be-104">Microsoft Dynamics 365 Supply Chain Management'ta, bir **Stok yaşlandırma** raporu çalıştırabilir ve çıktının form ve grafik olarak kullanılabilmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="363be-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="363be-105">Formda, sütunlar ve toplam bakiyeler yapılandırılan düzene göre dinamik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="363be-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="363be-106">Grafik, filtrelemeyi destekleyen ve ayrıntılara inmenizi sağlayan görsel bir genel bakış sunar.</span><span class="sxs-lookup"><span data-stu-id="363be-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="363be-107">Ek olarak, **Stok yaşlandırma raporu** olarak adlandırılan bir veri varlığı, **Stok yaşlandırma** raporunun sonuçlarını Microsoft Excel dosyası veya PDF dosyası gibi bir biçimde dışa aktarmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="363be-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="363be-108">Bu **Stok yaşlandırma** raporunu çalıştırma yöntemi, çıktının çok fazla satır içerdiği durumlarda yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="363be-108">This method of running an **Inventory aging** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="363be-109">Örneğin, 50.000 madde ve ambar olarak oluşturulan 300 mağazanız varsa ve ürüne, tesise ve ambara göre stok yaşlandırma yapmak istiyorsanız çıktı çok fazla satır içerir.</span><span class="sxs-lookup"><span data-stu-id="363be-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="run-an-inventory-aging-report"></a><span data-ttu-id="363be-110">Stok yaşlandırma raporunu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="363be-110">Run an Inventory aging report</span></span>

1. <span data-ttu-id="363be-111">**Maliyet yönetimi \> Sorgular ve raporlar \> Stok yaşlandırma raporu depolama alanı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="363be-111">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="363be-112">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="363be-112">Select **New**.</span></span>
1. <span data-ttu-id="363be-113">**İşlem Tanımlayıcısı – Ad** alanına rapor için benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="363be-113">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="363be-114">**Kimlik – Kod** raporunu seçin ve gerektiği şekilde filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="363be-114">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="363be-115">Rapor yürütme her zaman toplu işte yapılır.</span><span class="sxs-lookup"><span data-stu-id="363be-115">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="363be-116">Toplu iş tamamlandıktan sonra çıktı **Stok yaşlandırma raporu depolama alanı** sayfasında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="363be-116">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="363be-117">Çıktıyı geleneksel ızgara düzenine sahip bir form olarak görüntülemek için **Ayrıntıları görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="363be-117">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="363be-118">Çıktıyı toplam grafiği olarak görüntülemek için **Grafiği görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="363be-118">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="363be-119">Form, rapor düzeninde tanımlanan alt toplamları içermez.</span><span class="sxs-lookup"><span data-stu-id="363be-119">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="363be-120">**Stok yaşlandırma raporu** veri varlığı, **İşlem Tanımlayıcısı – Ad** alanı için bir filtre uygulayarak **Stok yaşlandırma** raporunun çıktısını Veri yönetiminin desteklediği herhangi bir biçimde dışa aktarmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="363be-120">The **Inventory aging report** data entity lets you export the output of an **Inventory aging** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
