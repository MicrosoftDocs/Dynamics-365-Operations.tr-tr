---
title: Finance and Operations uygulamaları yükseltmelerinden sorunları giderme
description: Bu konu, Finance and Operations uygulamalardaki yükseltmelerle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: ae54ffc9f7a97793dfaddc29f5aae66e5b06c931
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561214"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="0818e-103">Finance and Operations uygulamaları yükseltmelerinden sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="0818e-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0818e-104">Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="0818e-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="0818e-105">Bu konu, Finance and Operations uygulamalardaki yükseltmelerle ilgili sorunları çözmenize yardımcı olabilecek bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="0818e-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0818e-106">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="0818e-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0818e-107">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0818e-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="0818e-108">Veritabanı eşitleme hataları</span><span class="sxs-lookup"><span data-stu-id="0818e-108">Database synchronization errors</span></span>

<span data-ttu-id="0818e-109">**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="0818e-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="0818e-110">Bir Finance and Operations uygulamasını Platform güncelleştirmesi 30'a yükseltmek için **DualWriteProjectConfiguration** tablosunu kullanmaya çalışırken aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0818e-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="0818e-111">Sorunu düzeltmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0818e-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="0818e-112">Finance and Operations uygulamanın sanal makinesine (VM) oturum açın.</span><span class="sxs-lookup"><span data-stu-id="0818e-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="0818e-113">Yönetici olarak Visual Studio açın ve uygulama nesne ağacı (AOT) açın.</span><span class="sxs-lookup"><span data-stu-id="0818e-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="0818e-114">**DualWriteProjectConfiguration** öğesini arayın.</span><span class="sxs-lookup"><span data-stu-id="0818e-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="0818e-115">AOT'de, **DualWriteProjectConfiguration** öğesini sağ tıklatın ve **yeni projeye Ekle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0818e-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="0818e-116">Varsayılan seçenekleri kullanan yeni projeyi oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0818e-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="0818e-117">Çözüm Gezgininde **proje özelliklerini** farenin sağ düğmesiyle tıklayın ve yapılardaki **veritabanını senkronize eti** **doğru** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0818e-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="0818e-118">Projeyi oluşturun ve yapının başarılı olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="0818e-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="0818e-119">**Dynamics 365** menüsünde **veritabanını eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0818e-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="0818e-120">Tam veritabanı eşitlemesi yapmak için **Eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0818e-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="0818e-121">Tam veritabanı eşitleme işlemi başarılı olduktan sonra, Microsoft Dynamics Lifecycle Services (LCS) içindeki veritabanı eşitleme adımını yeniden çalıştırın ve uygun şekilde yükseltme betiklerini el ile kullanın; böylece güncelleştirmeye devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0818e-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="0818e-122">Eşlemelerde eksik tablo sütunları sorunu</span><span class="sxs-lookup"><span data-stu-id="0818e-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="0818e-123">**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="0818e-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="0818e-124">**Çift-yazılır** sayfada aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="0818e-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="0818e-125">*Şemada eksik kaynak alanı \<field name\>.*</span><span class="sxs-lookup"><span data-stu-id="0818e-125">*Missing source field \<field name\> in the schema.*</span></span>

![Eksik kaynak sütun hata iletisi örneği](media/error_missing_field.png)

<span data-ttu-id="0818e-127">Bu sorunu gidermek için, öncelikle bu sütunların tabloda olduğundan emin olmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0818e-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="0818e-128">Finance and Operations uygulamanın VM 'sine oturum açın.</span><span class="sxs-lookup"><span data-stu-id="0818e-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="0818e-129">**Çalışma alanları \> Veri yönetimi**'ne gidin, **Çerçeve parametreleri** kutucuğunu seçin ve sonra **Tablo ayarları** sekmesinde, tabloları yenilemek için **Tablo listesini yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0818e-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="0818e-130">**Çalışma alanları \> Veri yönetimi**'ne gidin, **Veri tabloları** sekmesini seçin ve tablonun listelendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="0818e-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="0818e-131">Tablo listede değilse Finance and Operations uygulaması için VM'de oturum açın ve tablonun kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="0818e-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="0818e-132">Finance and Operations uygulamasındaki **Çift yazma** sayfasından **Tablo eşleme** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="0818e-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="0818e-133">Tablo eşlemelerindeki sütunları otomatik olarak doldurmak için **Tablo listesini yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0818e-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="0818e-134">Sorun yine de düzeltilmemişse, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0818e-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0818e-135">Bu adımlar, bir tabloyu silme ve sonra yeniden ekleme sürecinde size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="0818e-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="0818e-136">Sorunlardan kaçınmak için, adımları tam olarak takip edin.</span><span class="sxs-lookup"><span data-stu-id="0818e-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="0818e-137">Finance and Operations uygulamasında, **Çalışma alanları \> Veri yönetimi**'ne gidin ve **Veri tabloları** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0818e-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="0818e-138">Özniteliğin eksik olduğu tabloyu bulun.</span><span class="sxs-lookup"><span data-stu-id="0818e-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="0818e-139">Araç çubuğunda **Hedef eşlemeyi değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0818e-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="0818e-140">**Hazırlamayı hedefe eşle** bölmesinde, **Eşleme oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0818e-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="0818e-141">Finance and Operations uygulamasındaki **Çift yazma** sayfasından **Tablo eşleme** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="0818e-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="0818e-142">Öznitelik eşlemede otomatik olarak doldurulmamışsa, **Öznitelik ekle** düğmesine ve sonra **Kaydet**'e tıklayarak el ile ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0818e-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="0818e-143">Eşlemeyi seçin **Çalıştır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0818e-143">Select the map and click **Run**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]