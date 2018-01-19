---
title: "Katıştırılmış Power BI kullanarak çalışma alanlarına analiz ekleme"
description: "bu konu bir Power BI raporunu bir çalışma alanının Analizler sekmesine katıştırmayı gösterir."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 7a3ff5a00af72dd7810337d1390b39d4f849dada
ms.contentlocale: tr-tr
ms.lasthandoff: 01/19/2018

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="a3279-103">Katıştırılmış Power BI kullanarak çalışma alanlarına analiz ekleme</span><span class="sxs-lookup"><span data-stu-id="a3279-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a3279-104">Bu özellik Dynamics 365 for Finance and Operations (sürüm 7.2 ve sonrası) için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a3279-104">This feature is supported in Dynamics 365 for Finance and Operations (version 7.2 and later).</span></span>

# <a name="introduction"></a><span data-ttu-id="a3279-105">Giriş</span><span class="sxs-lookup"><span data-stu-id="a3279-105">Introduction</span></span>
<span data-ttu-id="a3279-106">bu konu bir Microsoft Power BI raporunu bir çalışma alanının **Analizler** sekmesine katıştırmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3279-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="a3279-107">Burada verilen örnek için Filo Yönetimi uygulamasındaki **Rezervasyon yönetimi** çalışma alanını, bir **Analizler** sekmesinde bir analitik çalışma alanı katıştırmak üzere genişleteceğiz.</span><span class="sxs-lookup"><span data-stu-id="a3279-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

# <a name="prerequisites"></a><span data-ttu-id="a3279-108">Ön koşullar</span><span class="sxs-lookup"><span data-stu-id="a3279-108">Prerequisites</span></span>
+ <span data-ttu-id="a3279-109">Platform güncelleştirmesi 8 veya sonraki bir sürümü çalıştıran bir geliştirici ortamına erişin.</span><span class="sxs-lookup"><span data-stu-id="a3279-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="a3279-110">Microsoft Power BI Masaüstü kullanarak oluşturulmuş ve kaynağı Varlık deposu veritabanı olan bir veri modeline sahip bir analitik rapor (.pbix dosyası).</span><span class="sxs-lookup"><span data-stu-id="a3279-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

# <a name="overview"></a><span data-ttu-id="a3279-111">Özet</span><span class="sxs-lookup"><span data-stu-id="a3279-111">Overview</span></span>
<span data-ttu-id="a3279-112">Mevcut bir uygulama çalışma alanını genişlettiğinizde veya kendinize ait yeni bir çalışma alanı kullandığınızda, iş verilerinize bilgilendirici ve etkileşimli görünümler sunan katıştırılmış analitik görünümler kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3279-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="a3279-113">Bir analitik çalışma alanı sekmesi eklemenin dört adımı vardır.</span><span class="sxs-lookup"><span data-stu-id="a3279-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="a3279-114">Dynamics 365 kaynağına bir .pbix dosyası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a3279-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="a3279-115">Bir analitik çalışma alanı sekmesi belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a3279-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="a3279-116">.pbix kaynağını çalışma alanı sekmesine gömün.</span><span class="sxs-lookup"><span data-stu-id="a3279-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="a3279-117">İsteğe bağlı: Görünümü özelleştirmek için uzantılar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a3279-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="a3279-118">Analitik raporlar oluşturmak hakkında daha fazla bilgi için bkz. [Power BI Masaüstü ile çalışmaya başlamak](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="a3279-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="a3279-119">Bu sayfa, ilgi çekici analitik raporlama çözümleri oluşturmanıza yardımcı olacak harika bir bilgi kaynağıdır.</span><span class="sxs-lookup"><span data-stu-id="a3279-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

# <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="a3279-120">Bir .pbix dosyasını bir kaynak olarak ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a3279-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="a3279-121">Başlamadan önce, çalışma alanına katıştıracağınız Power BI raporunu oluşturun veya alın.</span><span class="sxs-lookup"><span data-stu-id="a3279-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="a3279-122">Analitik raporlar oluşturmak hakkında daha fazla bilgi için bkz. [Power BI Masaüstü ile çalışmaya başlamak](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span><span class="sxs-lookup"><span data-stu-id="a3279-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span>
 
<span data-ttu-id="a3279-123">Bir .pbix doyasını bir Visual Studio yapıtı olarak eklemek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a3279-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="a3279-124">Uygun modelde yeni bir proje oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a3279-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="a3279-125">Çözüm Gezgini'nde projeye sağ tıklayın ve sonra **Ekle** > **Yeni Madde**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-125">In Solution Explorer, select the project, right-click, and then select **Add** > **New Item**.</span></span>
3. <span data-ttu-id="a3279-126">**Yeni Madde Ekle** iletişim kutusunda, **Operasyonlar Yapıları** altında **Kaynak** şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="a3279-127">X++ meta verisindeki raporu referans olarak kullanacak bir ad girin ve **Ekle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a3279-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![Yeni Madde Ekle iletişim kutusu](media/analytical-workspace-add.png)

5. <span data-ttu-id="a3279-129">Analitik raporun tanımını içeren .pbix dosyasını bulun ve **Aç**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a3279-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![Bir Kaynak dosya iletişim kutusu seçin](media/analytical-workspace-select-resource.png)
  
<span data-ttu-id="a3279-131">Şimdi .pbix dosyasını bir Dynamics 365 kaynağı olarak ekledikten sonra, raporları çalışma alanlarına katıştırabilir ve menü öğelerini kullanarak doğrudan bağlantılar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3279-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

# <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="a3279-132">Bir uygulama çalışma alanına bir sekme denetimi ekleyin</span><span class="sxs-lookup"><span data-stu-id="a3279-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="a3279-133">Bu örnekte Filo Yönetimi modelinde, **Analizler** sekmesini **FMClerkWorkspace** formuna ekleyerek **Rezervasyon yönetimi** çalışma alanını genişleteceğiz.</span><span class="sxs-lookup"><span data-stu-id="a3279-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>
 
<span data-ttu-id="a3279-134">Aşağıdaki görsel, **FMClerkWorkspace** formunun Microsoft Visual Studio tasarımcısında nasıl görüneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3279-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![Değişikliklerden önce FMClerkWorkspace formu](media/analytical-workspace-definition-before.png)

<span data-ttu-id="a3279-136">**Rezervasyon yönetimi** çalışma alanının form tanımını genişletmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a3279-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="a3279-137">Tasarım tanımını genişletmek için form tasarımcısını açın.</span><span class="sxs-lookup"><span data-stu-id="a3279-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="a3279-138">Tasarım tanımında, **Tasarım | Desen: Çalışma Alanı Operasyonel** olarak etiketlenmiş üst öğeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="a3279-139">Sağ tıklayın ve daha sonra **FormTabControl1** adında yeni bir denetim eklemek için **Yeni** > **Sekme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-139">Right-click, and then select **New** > **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="a3279-140">Form tasarımcısında **FormTabControl1**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="a3279-141">Sağ tıklayın ve daha sonra yeni bir sekme sayfası eklemek için **Yeni Sekme Sayfası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="a3279-142">Sekme sayfasının adını **Çalışma alanı** gibi anlamlı bir şeye değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a3279-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="a3279-143">Form tasarımcısında **FormTabControl1**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="a3279-144">Sağ tıklayın ve daha sonra **Yeni Sekme Sayfası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="a3279-145">Sekme sayfasının adını **Analizler** gibi anlamlı bir şeye değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a3279-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="a3279-146">Form tasarımcısında **Analizler (Sekme Sayfası)**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="a3279-147">**Başlık** özelliğin **Analizler** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a3279-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="a3279-148">Kontrole sağ tıklayın ve daha sonra yeni bir form grup denetimi eklemek için **Yeni** > **Grup**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-148">Right-click the control, and then select **New** > **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="a3279-149">Form grubunun adını **powerBIReportGroup** gibi anlamlı bir şeye değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a3279-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="a3279-150">Form tasarımcısında **PanoramaBody (Sekme)** seçin. ve denetimi **Çalışma alanı** sekmesine sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="a3279-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="a3279-151">Tasarım tanımında, **Tasarım | Desen: Çalışma Alanı Operasyonel** olarak etiketlenmiş üst öğeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="a3279-152">Sağ tıklayın ve daha sonra **Deseni sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="a3279-153">Yeniden sağ tıklayın ve **Desen ekle** > **Sekmeli Çalışma Alanı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a3279-153">Right-click again, and then select **Add pattern** > **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="a3279-154">Yaptığınız değişiklikleri doğrulamak için bir yapı gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="a3279-154">Perform a build to verify your changes.</span></span>
 
<span data-ttu-id="a3279-155">Aşağıdaki görsel, bu değişiklikler uygulandıktan sonra tasarımın nasıl görüneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3279-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![Değişikliklerden sonra FMClerkWorkspace](media/analytical-workspace-definition-after.png)

<span data-ttu-id="a3279-157">Çalışma alanı raporunu katıştırmak için kullanılacak form denetimlerini ekledikten sonra, düzeni bulunduracak üst denetimin boyutunu tanımlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="a3279-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="a3279-158">Varsayılan olarak hem **Filtrelre Bölmesi** sayfası hem de **Sekmeler** sayfası raporda görünür olur.</span><span class="sxs-lookup"><span data-stu-id="a3279-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="a3279-159">Bunula birlikte, bu denetimlerin görünürlüğünü raporun hedef tüketicisi için uygun şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3279-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>
 
> [!NOTE]
> <span data-ttu-id="a3279-160">Katıştırılmış çalışma alanları için tutarlılık amacıyla hem **Filtrelre Bölmesi** hem de **Sekme** sayfasını gizleyecek uzantılar kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="a3279-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>
 
<span data-ttu-id="a3279-161">Şimdi uygulama form tanımını genişletme görevini tamamladınız.</span><span class="sxs-lookup"><span data-stu-id="a3279-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="a3279-162">Uzantıların nasıl kullanılacağı ve özelleştirmelerin nasıl yapılacağına dair daha fazla bilgi için bkz.  [Özelleştirme: Katmanlama ve uzantılar](../extensibility/customization-overlayering-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a3279-162">For more information about how to use extensions to do customizations, see  [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="a3279-163">Bir görüntüleyici denetimi katıştırmak için X++ iş mantığı ekleyin</span><span class="sxs-lookup"><span data-stu-id="a3279-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="a3279-164">**Rezervasyon yönetimi** çalışma alanına katıştırılmış olan rapor görüntüleyici denetimini başlatan bir iş mantığı eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a3279-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="a3279-165">Tasarım tanımını genişletmek için **FMClerkWorkspace** form tasarımcısını açın.</span><span class="sxs-lookup"><span data-stu-id="a3279-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="a3279-166">Kod tanımının arkasındaki koda erişmek için F7'ye basın.</span><span class="sxs-lookup"><span data-stu-id="a3279-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="a3279-167">Aşağıdaki X++ kodunu ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a3279-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="a3279-168">Yaptığınız değişiklikleri doğrulamak için bir yapı gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="a3279-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="a3279-169">Katıştırılmış rapor görüntüleme denetimini başlatmak için iş mantığı ekleme görevini şimdi tamamladınız.</span><span class="sxs-lookup"><span data-stu-id="a3279-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="a3279-170">Aşağıdaki görsel, bu değişiklikler uygulandıktan sonra çalışma alanının nasıl görüneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a3279-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![Çalışma alanına katıştırılmış rapor](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="a3279-172">Sayfa başlığının altındaki çalışma alanı sekmelerini kullanarak mevcut operasyonel görünümlere erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3279-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

# <a name="reference"></a><span data-ttu-id="a3279-173">Referans</span><span class="sxs-lookup"><span data-stu-id="a3279-173">Reference</span></span>

## <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="a3279-174">PBIReportHelper.initializeReportControl yöntemi</span><span class="sxs-lookup"><span data-stu-id="a3279-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="a3279-175">Bu bölüm, bir Power BI raporunu (.pbix kaynağı) bir form grubu denetimine eklemek için kullanılan yardımcı sınıf hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="a3279-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

### <a name="syntax"></a><span data-ttu-id="a3279-176">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="a3279-176">Syntax</span></span>
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a><span data-ttu-id="a3279-177">Parametreler</span><span class="sxs-lookup"><span data-stu-id="a3279-177">Parameters</span></span>

| <span data-ttu-id="a3279-178">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="a3279-178">Name</span></span> | <span data-ttu-id="a3279-179">Açıklama</span><span class="sxs-lookup"><span data-stu-id="a3279-179">Description</span></span> |
|---|---|
| <span data-ttu-id="a3279-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="a3279-180">resourceName</span></span> | <span data-ttu-id="a3279-181">.pbix kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="a3279-181">The name of the .pbix resource.</span></span> |
| <span data-ttu-id="a3279-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="a3279-182">formGroupControl</span></span> | <span data-ttu-id="a3279-183">Power BI rapor denetiminin uygulanacağı form grup denetimi.</span><span class="sxs-lookup"><span data-stu-id="a3279-183">The form group control to apply the Power BI report control to.</span></span> |
| <span data-ttu-id="a3279-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="a3279-184">defaultPageName</span></span> | <span data-ttu-id="a3279-185">Varsayılan sayfa adı.</span><span class="sxs-lookup"><span data-stu-id="a3279-185">The default page name.</span></span> |
| <span data-ttu-id="a3279-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="a3279-186">showFilterPane</span></span> | <span data-ttu-id="a3279-187">Bir Boole değeri, filtre panosunun gösterilip (**doğru**) gösterilmeyeceğini (**yanlış**) belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3279-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="a3279-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="a3279-188">showNavPane</span></span> | <span data-ttu-id="a3279-189">Bir Boole değeri, gezinti panosunun gösterilip (**doğru**) gösterilmeyeceğini (**yanlış**) belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3279-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="a3279-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="a3279-190">defaultFilters</span></span> | <span data-ttu-id="a3279-191">Power BI raporu için varsayılan filtreler.</span><span class="sxs-lookup"><span data-stu-id="a3279-191">The default filters for the Power BI report.</span></span> |

