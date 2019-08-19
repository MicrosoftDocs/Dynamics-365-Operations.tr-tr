---
title: CFO çalışma alanına mali boyutlar ekleme
description: Bu konu, genel muhasebe ve bütçe raporları için kullanılabilmeleri amacıyla CFO çalışma alanına mali boyutların nasıl ekleneceğini açıklar.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 508b491218ee0a09794371aeccd2d190735b3ab9
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839701"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a><span data-ttu-id="511f7-103">CFO çalışma alanına mali boyutlar ekleme</span><span class="sxs-lookup"><span data-stu-id="511f7-103">Add financial dimensions to the CFO workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="511f7-104">Bu konu, genel muhasebe ve bütçe raporları için kullanılabilmeleri amacıyla Mali İşler Müdürü (CFO) çalışma alanına mali boyutların nasıl ekleneceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="511f7-104">This topic explains how to add financial dimensions to the Chief Financial Officer (CFO) workspace, so that they can be used for the ledger and budget reports.</span></span> <span data-ttu-id="511f7-105">CFO çalışma alanı bir **Genel bakış** sekmesine ve bir **Mali** sekmesine sahiptir. Bu iki sekmedeki raporlar iki ölçüt tarafından desteklenir: LedgerActivityMeasure ve BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="511f7-105">The CFO workspace has an **Overview** tab and a **Financial** tab. The reports on these two tabs are backed by two measures: LedgerActivityMeasure and BudgetActivityMeasure.</span></span> <span data-ttu-id="511f7-106">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Temmuz 2017) içinde, bu iki ölçü ve DimensionCombinationEntity varlığı arasında ilişki vardır.</span><span class="sxs-lookup"><span data-stu-id="511f7-106">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), there is a relation between those two measures and the DimensionCombinationEntity entity.</span></span> <span data-ttu-id="511f7-107">Bu nedenle, boyutları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="511f7-107">Therefore, you can select dimensions.</span></span>

1. <span data-ttu-id="511f7-108">Finance and Operations'ta, **Varlık Deposu** sayfasında, **LedgerActivityMeasure** ve **BudgetActivityMeasure** ölçülerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="511f7-108">In Finance and Operations, on the **Entity Store** page, update the **LedgerActivityMeasure** and the **BudgetActivityMeasure** measures.</span></span>
2. <span data-ttu-id="511f7-109">Microsoft Visual Studio'da, Uygulama Gezgini'ni açın ve **LedgerCFO** aratın.</span><span class="sxs-lookup"><span data-stu-id="511f7-109">In Microsoft Visual Studio, open Application Explorer, and search for **LedgerCFO**.</span></span>
3. <span data-ttu-id="511f7-110">**Kaynaklar** altında, **LedgerCFOWorkspacePBIX** açın.</span><span class="sxs-lookup"><span data-stu-id="511f7-110">Under **Resources**, open **LedgerCFOWorkspacePBIX**.</span></span>
4. <span data-ttu-id="511f7-111">Kaynak Microsoft Power BI masaüstünde açıldığında **Veri Al**'ı seçin, **SQL Server veritabanı**'nı seçin ve daha sonra **Bağlan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-111">When the resource opens in Microsoft Power BI desktop, select **Get Data**, select **SQL Server database**, and then select **Connect**.</span></span>
5. <span data-ttu-id="511f7-112">Sunucu adını girin ve veritabanı olarak **AxDW** girin.</span><span class="sxs-lookup"><span data-stu-id="511f7-112">Enter the server name, and enter **AxDW** as the database.</span></span> <span data-ttu-id="511f7-113">**DirectQuery** seçin ve daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-113">Select **DirectQuery**, and then select **OK**.</span></span>
6. <span data-ttu-id="511f7-114">**LedgerActivityMeasure\_DimensionCombination** arayın ve seçin, daha sonra **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-114">Search for and select **LedgerActivityMeasure\_DimensionCombination**, and then select **Load**.</span></span>

    > [!TIP]
    > <span data-ttu-id="511f7-115">**Alanlar** listesinde kolayca ayırt edebilmek için **Mali boyutlar** tablosunun adını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="511f7-115">In the **Fields** list, rename the table **Financial dimensions**, so that it's easy to identify.</span></span>

7. <span data-ttu-id="511f7-116">**İlişkileri Yönet**'i seçin ve daha sonra **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-116">Select **Manage Relationships**, and then select **New**.</span></span>
8. <span data-ttu-id="511f7-117">İlk alanda **Genel Muhasebe Faaliyetleri**'ni seçin ve **LedgerDimension**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-117">In the first field, select **General Ledger Activities**, and then select **LedgerDimension**.</span></span>
9. <span data-ttu-id="511f7-118">İkinci alanda **LedgerActivityMeasure\_DimensionCombination** (veya tablonu adını değiştirdiyseniz **Mali boyutlar**) seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-118">In the second field, select **LedgerActivityMeasure\_DimensionCombination** (or **Financial dimensions** if you renamed the table).</span></span> <span data-ttu-id="511f7-119">**DimensionCombinationRECID** başlığını seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-119">Select the  **DimensionCombinationRECID** header.</span></span>
10. <span data-ttu-id="511f7-120">**Asallık** alanında **Birçoktan Bire**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-120">In the **Cardinality** field, select **Many to One**.</span></span>
11. <span data-ttu-id="511f7-121">**Çapraz filtre yönü** değerini **Tek** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="511f7-121">Change the **Cross filter direction** value to **Single**.</span></span>
12. <span data-ttu-id="511f7-122">**Bu ilişkiyi etkin yap** ve **Referans tutarlığını kabul et**'i seçin, **Tamam**'ı seçin ve daha sonra **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-122">Select both **Make this relationship active** and **Assume referential integrity**, select **OK**, and then select **Close**.</span></span>

    <span data-ttu-id="511f7-123">[![Bir ilişki oluştur](./media/Create-relationship.png)](./media/Create-relationship.png)</span><span class="sxs-lookup"><span data-stu-id="511f7-123">[![Create a relationship](./media/Create-relationship.png)](./media/Create-relationship.png)</span></span>

13. <span data-ttu-id="511f7-124">**Alanlar** listesinde, tabloyu veya kullanılabilir mali boyutları görebilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="511f7-124">In the **Fields** list, you should see the table and the available financial dimensions.</span></span> <span data-ttu-id="511f7-125">İstediğiniz mali boyutları raporlama düzeyi filtrelerine sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="511f7-125">Drag the financial dimensions that you want to the report-level filters.</span></span>
14. <span data-ttu-id="511f7-126">Değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="511f7-126">Save your changes.</span></span>
15. <span data-ttu-id="511f7-127">Uygulama Nesne Ağacı (AOT) içerisinde projeni sağ tıklayın ve sonra **Eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="511f7-127">In the Application Object Tree (AOT), right-click your project, and then select **Synchronize**.</span></span>
16. <span data-ttu-id="511f7-128">Projenizi oluşturun ve sonra sonuçları görmek için uygulamayı açın.</span><span class="sxs-lookup"><span data-stu-id="511f7-128">Build your project, and then open the application to view the results.</span></span>

    <span data-ttu-id="511f7-129">[![Tamamlanan çalışma alanı](./media/workspace.png)](./media/workspace.png)</span><span class="sxs-lookup"><span data-stu-id="511f7-129">[![Completed workspace](./media/workspace.png)](./media/workspace.png)</span></span>
