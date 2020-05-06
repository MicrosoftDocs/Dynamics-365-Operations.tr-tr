---
title: Finance and Operations uygulamaları yükseltmeleriyle ilgili sorunları giderme
description: Bu konu, Finance and Operations uygulamalardaki yükseltmelerle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 53df00de82b101aa02160d865a9c3bbebcfcae15
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275476"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="7e8e0-103">Finance and Operations uygulamaları yükseltmeleriyle ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="7e8e0-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="7e8e0-104">Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="7e8e0-105">Bu konu, Finance and Operations uygulamalardaki yükseltmelerle ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e8e0-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="7e8e0-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="7e8e0-108">Veritabanı eşitleme hataları</span><span class="sxs-lookup"><span data-stu-id="7e8e0-108">Database synchronization errors</span></span>

<span data-ttu-id="7e8e0-109">**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="7e8e0-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="7e8e0-110">Platform Güncelleştirmesi 30'a bir Finance and Operations uygulamayı güncelleştirmek için **dualwriteprojectconfiguration** varlığını kullanmaya çalıştığınızda aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="7e8e0-111">Sorunu düzeltmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="7e8e0-112">Finance and Operations uygulamanın sanal makinesine (VM) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="7e8e0-113">Yönetici olarak Visual Studio açın ve uygulama nesne ağacı (AOT) açın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="7e8e0-114">**DualWriteProjectConfiguration** öğesini arayın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="7e8e0-115">AOT'de, **DualWriteProjectConfiguration** öğesini sağ tıklatın ve **yeni projeye Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="7e8e0-116">Varsayılan seçenekleri kullanan yeni projeyi oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="7e8e0-117">Çözüm Gezgininde **proje özelliklerini** farenin sağ düğmesiyle tıklayın ve yapılardaki **veritabanını senkronize eti** **doğru** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="7e8e0-118">Projeyi oluşturun ve yapının başarılı olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="7e8e0-119">**Dynamics 365** menüsünde **veritabanını eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="7e8e0-120">Tam veritabanı eşitlemesi yapmak için **Eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="7e8e0-121">Tam veritabanı eşitleme işlemi başarılı olduktan sonra, Microsoft Dynamics Lifecycle Services (LCS) içindeki veritabanı eşitleme adımını yeniden çalıştırın ve uygun şekilde yükseltme betiklerini el ile kullanın; böylece güncelleştirmeye devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="7e8e0-122">Haritalarda eksik varlık alanları çıkışı</span><span class="sxs-lookup"><span data-stu-id="7e8e0-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="7e8e0-123">**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="7e8e0-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="7e8e0-124">**Çift-yazılır** sayfada aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7e8e0-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="7e8e0-125">*Şemada eksik kaynak alanı \<alan adı\>.*</span><span class="sxs-lookup"><span data-stu-id="7e8e0-125">*Missing source field \<field name\> in the schema.*</span></span>

![Eksik kaynak alan hata iletisi örneği](media/error_missing_field.png)

<span data-ttu-id="7e8e0-127">Bu sorunu gidermek için, öncelikle bu alanların varlıkta olduğundan emin olmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="7e8e0-128">Finance and Operations uygulamanın VM 'sine oturum açın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="7e8e0-129">**Çalışma alanları \>veri yönetimi**'ne gidin, **çerçeve parametreleri** kutucuğunu seçin ve sonra **varlık ayarları** sekmesinde, varlıkları yenilemek için **varlık listesini yenile** seçin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="7e8e0-130">**Çalışma alanları \> Veri yönetimi**'ne gidin, **veri varlıkları** sekmesini seçin ve varlığın listelendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="7e8e0-131">Varlık listelenmiyorsa, Finance and Operations uygulama için VM 'de oturum açın ve varlığın kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="7e8e0-132">Finance and Operations uygulamadaki **ikili yazma** sayfasından **varlık eşleme** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="7e8e0-133">Varlık eşlemelerinde alanları otomatik olarak doldurmak için **Varlık listesini yenile** seçin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="7e8e0-134">Sorun yine de düzeltilmemişse, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e8e0-135">Bu adımlar, bir varlığı silme ve sonra yeniden ekleme sürecinde size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="7e8e0-136">Sorunlardan kaçınmak için, adımları tam olarak takip edin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="7e8e0-137">Finance and Operations uygulamada, **Çalışma alanları \> Veri yönetimi**'ne gidin ve **Veri varlıkları** döşemesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="7e8e0-138">Özniteliğin eksik olduğu varlığı bulun.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-138">Find the entity that is missing the attribute.</span></span> <span data-ttu-id="7e8e0-139">Araç çubuğunda **Hedef eşlemeyi değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="7e8e0-140">**Hazırlamayı hedefe eşle** bölmesinde, **Eşleme oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="7e8e0-141">Finance and Operations uygulamadaki **ikili yazma** sayfasından **varlık eşleme** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-141">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="7e8e0-142">Öznitelik eşlemede otomatik olarak doldurulmamışsa, **Öznitelik ekle** düğmesine ve sonra **Kaydet**'e tıklayarak el ile ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="7e8e0-143">Eşlemeyi seçin **Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7e8e0-143">Select the map and click **Run**.</span></span>
