---
title: Regression Suite Automation Tool eğitimi kullanma
description: Bu konu, Regression Suite Automation Tool'un (RSAT) nasıl kullanılacağını gösterir. Çeşitli özellikleri tanımlar ve gelişmiş komut dosyası kullanan örnekler sağlar.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: cf3ca501efb4e540994b01e651eee5b8aab4ddbc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191098"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="9310d-104">Regression Suite Automation Tool eğitimi kullanma</span><span class="sxs-lookup"><span data-stu-id="9310d-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9310d-105">Bu sayfayı pdf formatında karşıdan yükleyip kaydetmek için internet tarayıcısı araçlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="9310d-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="9310d-106">Bu öğretici, Regression Suite Automation Tool (RSAT) gelişmiş özelliklerinden bazılarının arasında, bir demo ataması içerir ve strateji ve önemli öğrenme noktalarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="9310d-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="9310d-107">RSAT/Görev kaydedici özellikleri</span><span class="sxs-lookup"><span data-stu-id="9310d-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="9310d-108">Bir alan değeri doğrula</span><span class="sxs-lookup"><span data-stu-id="9310d-108">Validate a field value</span></span>

<span data-ttu-id="9310d-109">Bu özellik hakkında daha fazla bilgi için, bkz [Doğrulama işlevi olan yeni bir görev kaydı oluşturma](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="9310d-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="9310d-110">Kaydedilen değişken</span><span class="sxs-lookup"><span data-stu-id="9310d-110">Saved variable</span></span>

<span data-ttu-id="9310d-111">Bu özellik hakkında daha fazla bilgi için, bkz [Kaydedilmiş bir değişken oluşturmak için varolan görev kaydını değiştirme](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="9310d-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="9310d-112">Türetilmiş test olayı</span><span class="sxs-lookup"><span data-stu-id="9310d-112">Derived test case</span></span>

1. <span data-ttu-id="9310d-113">Regression Suite Automation Tool'u (RSAT) açın ve [Regression Suite Automation Tool eğitimi ayarlama ve yükleme](./hol-set-up-regression-suite-automation-tool.md)'da oluşturduğunuz test olaylarını seçin.</span><span class="sxs-lookup"><span data-stu-id="9310d-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="9310d-114">**Yeni \> Türetilmiş test olayı oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="9310d-114">Select **New \> Create derived test case**.</span></span>

    ![Yeni menüsünde türetilmiş test olayı komutu oluşturma](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="9310d-116">Geçerli test paketindeki her seçili test olayı için bir türetilmiş test olayının oluşturulduğunu ve her türetilmiş test olayının kendi Excel parametre dosyası kopyasına sahip olduğunu bildiren bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="9310d-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="9310d-117">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9310d-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9310d-118">Türetilmiş bir test olayı çalıştırdığınızda, üst test olayının görev kaydını ve kendi Excel parametre dosyası kopyasını kullanır.</span><span class="sxs-lookup"><span data-stu-id="9310d-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="9310d-119">Bu şekilde, birden fazla görev kaydını korumak zorunda kalmadan, aynı testi farklı parametrelerle çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="9310d-120">Türetilmiş test olayının master test olayı ile aynı test paketinin parçası olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="9310d-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![İleti kutusu](./media/use_rsa_tool_02.png)

    <span data-ttu-id="9310d-122">İki ek türev test çalışması oluşturulur ve **Türetilmiş mi?** onay kutusu seçili değildir.</span><span class="sxs-lookup"><span data-stu-id="9310d-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Türetilmiş test olayları oluşturuldu](./media/use_rsa_tool_03.png)

    <span data-ttu-id="9310d-124">Azure DevOps'ta otomatik olarak bir türetilmiş test olayı oluşturulur</span><span class="sxs-lookup"><span data-stu-id="9310d-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="9310d-125">Bu, **Yeni bir ürün oluştur** test olayının alt öğesidir ve özel bir anahtar sözcükle etiketlenir: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="9310d-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="9310d-126">Bu test olayları Azure DevOps'ta otomatik olarak test planına eklenir.</span><span class="sxs-lookup"><span data-stu-id="9310d-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![RSAT: DerivedTestSteps anahtar sözcüğü](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="9310d-128">Herhangi bir nedenle, oluşturulan türetilmiş test çalışmaları doğru sırada değilse test paketindeki test olaylarını doğru sırayla çalıştırabilmek için Azure DevOps'a gidin ve test olaylarını yeniden sıralayın, böylece RSAT onları doğru sırada çalıştırabilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="9310d-129">Yalnızca türetilmiş test olaylarını seçin ve sonra karşılık gelen Excel parametre dosyasını açmak için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9310d-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="9310d-130">Bu Excel parametre dosyalarını, ana dosyaları düzenlediğiniz şekilde düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="9310d-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="9310d-131">Başka bir deyişle, ürün kimliğinin otomatik olarak üretilmesine olanak verecek şekilde ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="9310d-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="9310d-132">Ayrıca, kaydedilen değişkenin ilgili alanlara kopyalanmış olduğundan da emin olun.</span><span class="sxs-lookup"><span data-stu-id="9310d-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="9310d-133">Hem Excel parametre dosyalarının **Genel** sekmesinde, hem de **Şirket** alanının değerini **USSI**olarak güncelleyin, böylece türetilmiş test olayları ana test olaylarından farklı bir tüzel kişiliğe karşı çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="9310d-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="9310d-134">Belirli bir kullanıcıya (veya belirli bir kullanıcıyla ilişkilendirilmiş role) göre test olaylarını çalıştırmak için, **Test Kullanıcısı** alanının değerini güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="9310d-135">**Çalıştır**'ı seçin ve ürünün hem USMF tüzel kişiliği hem de USSI tüzel kişiliği içinde oluşturulduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9310d-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="9310d-136">Bildirim doğrulama</span><span class="sxs-lookup"><span data-stu-id="9310d-136">Validate notifications</span></span>

<span data-ttu-id="9310d-137">Bu özellik, bir eylemin meydana geldiğini doğrulamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="9310d-138">Örneğin, bir üretim emri oluşturulduğunda, tahmin edildiğinde ve ardından başlatıldığında, uygulama üretim emrinin başlatıldığını size bildiren bir "Üretim-Başlangıcı" iletisi gösterir.</span><span class="sxs-lookup"><span data-stu-id="9310d-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Üretim – Başlangıç bildirimi](./media/use_rsa_tool_05.png)

<span data-ttu-id="9310d-140">Uygun kayıt için Excel parametre dosyasının **MessageValidation** sekmesine ileti metnini girerek bu iletiyi RSAT ile doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Mesaj doğrulama sekmesi](./media/use_rsa_tool_06.png)

<span data-ttu-id="9310d-142">Test olayı çalıştırıldıktan sonra Excel parametre dosyasındaki ileti gösterilen iletiyle karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="9310d-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="9310d-143">İletiler eşleşmezse test olayı başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="9310d-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="9310d-144">Excel parametre dosyasındaki **MessageValidation** sekmesine birden çok ileti girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="9310d-145">İletiler, bilgi iletileri yerine hata veya uyarı iletileri de olabilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="9310d-146">Değerleri işleçleri kullanarak doğrulama</span><span class="sxs-lookup"><span data-stu-id="9310d-146">Validate values by using operators</span></span>

<span data-ttu-id="9310d-147">RSAT'ın önceki sürümlerinde, değerleri yalnızca beklenen değerle eşitlenmiş bir denetim değeri olarak doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="9310d-148">Yeni özellik, bir değişkenin eşit olmadığını, daha küçük olduğunu veya belirtilen bir değerden fazla olduğunu doğrulamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9310d-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="9310d-149">Bu özelliği kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini  **yanlış**'tan **doğru**'ya çevirin.</span><span class="sxs-lookup"><span data-stu-id="9310d-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="9310d-150">Excel parametre dosyasında yeni bir **Operatör** alanı görünür.</span><span class="sxs-lookup"><span data-stu-id="9310d-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9310d-151">RSAT'ın daha eski bir sürümünü kullanıyorsanız yeni Excel parametre dosyaları oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="9310d-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Operatör alanı](./media/use_rsa_tool_07.png)

<span data-ttu-id="9310d-153">Aşağıdaki örnek, Eldeki stoğun 0'dan (sıfır) fazla olup olmadığı doğrulamak için bu özelliği nasıl kullanabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="9310d-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="9310d-154">**USMF** şirketinde demo verilerinde, aşağıdaki adımları içeren bir görev kaydı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="9310d-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="9310d-155">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="9310d-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="9310d-156">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="9310d-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9310d-157">Örneğin, **Ürün numarası** alanını **1000** değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="9310d-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="9310d-158">**Eldeki stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="9310d-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="9310d-159">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="9310d-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9310d-160">Örneğin,  **Site** alanını **1** değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="9310d-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="9310d-161">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="9310d-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="9310d-162">**Toplam kullanılabilir** alanının değerinin **411.0000000000000000** olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9310d-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="9310d-163">Görev kaydını LCS'deki BPM kitaplığına kaydedin ve Azure DevOps ile eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="9310d-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="9310d-164">Test durumunu test planına ekleyin ve test çalışmasını RSAT'a yükleyin.</span><span class="sxs-lookup"><span data-stu-id="9310d-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="9310d-165">Excel parametre dosyasını açın.</span><span class="sxs-lookup"><span data-stu-id="9310d-165">Open the Excel parameter file.</span></span> <span data-ttu-id="9310d-166">**InventOnhandItem** sekmesinde, **Operatör** alanı içeren bir **InventOnhandItem doğrula** bölümü göreceksiniz .</span><span class="sxs-lookup"><span data-stu-id="9310d-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Operatör alanı](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="9310d-168">Eldeki stok miktarının her zaman 0'dan büyük olacağını doğrulamak için **Değer** alanını **411**'den **0**'a ve **Operatör** alanının değerini eşittir işaretini (**=**) büyüktür işareti (**\>**) olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9310d-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Değer ve Operatör alanlarının değerleri değişti](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="9310d-170">Kaydedin ve Excel parametresi dosyasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="9310d-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="9310d-171">Excel parametre dosyasında yaptığınız değişiklikleri Azure DevOps'a kaydetmek için **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9310d-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="9310d-172">Şimdi, stokta belirtilen maddenin **Toplam Kullanılabilir** alanının değeri 0 (sıfır)'dan büyükse eldeki gerçek stok değerine bakılmaksızın testler geçer.</span><span class="sxs-lookup"><span data-stu-id="9310d-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="9310d-173">Oluşturucu günlükleri</span><span class="sxs-lookup"><span data-stu-id="9310d-173">Generator logs</span></span>

<span data-ttu-id="9310d-174">Bu özellik, çalıştırılan test olaylarının günlüklerini içeren bir klasör oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9310d-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="9310d-175">Bu özelliği kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini  **yanlış**'tan **doğru**'ya çevirin.</span><span class="sxs-lookup"><span data-stu-id="9310d-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="9310d-176">Test olaylarını çalıştırıldıktan sonra, günlük dosyalarını **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs** altında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![GeneratorLogs klasörü](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="9310d-178">.config dosyasındaki değeri değiştirmeden önce varolan test olayları varsa, yeni test çalışmaları dosyaları üretene kadar bu test olayları için günlükler oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="9310d-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Yeni menüde yalnızca Metin Yürütmesi ve Parametre Dosyaları oluştur komutu](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="9310d-180">Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="9310d-180">Snapshot</span></span>

<span data-ttu-id="9310d-181">Bu özellik, görev kaydı sırasında gerçekleştirilen adımların ekran görüntülerini alır.</span><span class="sxs-lookup"><span data-stu-id="9310d-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="9310d-182">Bu özelliği kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini  **yanlış**'tan **doğru**'ya çevirin.</span><span class="sxs-lookup"><span data-stu-id="9310d-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="9310d-183">**C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, altında çalışan her test olayı için ayrı bir klasör oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9310d-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Test olayı için anlık görüntü klasörü](./media/use_rsa_tool_12.png)

<span data-ttu-id="9310d-185">Bu klasörlerin her biri için, test olayları çalıştırılırken gerçekleştirilen adımların anlık görüntülerini bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Anlık görüntü dosyaları](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="9310d-187">Atama</span><span class="sxs-lookup"><span data-stu-id="9310d-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="9310d-188">Senaryo</span><span class="sxs-lookup"><span data-stu-id="9310d-188">Scenario</span></span>

1. <span data-ttu-id="9310d-189">Ürün tasarımcısı, yeni bir serbest bırakılan ürün oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9310d-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="9310d-190">Üretim yöneticisi, stok düzeyini iki parçaya getirmek için bir üretim emri başlatır.</span><span class="sxs-lookup"><span data-stu-id="9310d-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="9310d-191">Üretim, üretim emrini başlatır ve sonlandırır ve eldeki miktarın iki parçadan oluştuğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="9310d-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="9310d-192">Satış ekibi, yeni ürünün dört parçadan oluşan siparişini alır.</span><span class="sxs-lookup"><span data-stu-id="9310d-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="9310d-193">Bu nedenle, satış ekibi net gereksinimleri dinamik plan aracılığıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9310d-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="9310d-194">Kullanılabilir ek kapasite bulunmadığından, varsayılan sipariş ilkesi "yapmak yerine satın al" olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="9310d-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="9310d-195">Bu nedenle, planlı bir satınalma siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9310d-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="9310d-196">Alıcı bir satıcı ekler, planlı satınalma siparişi sağlar ve sonra satınalma siparişini onaylar.</span><span class="sxs-lookup"><span data-stu-id="9310d-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="9310d-197">Satın alınan mallar mağazaya ulaştığında, mağaza operatörü ilgili satınalma siparişini arar ve malları alır.</span><span class="sxs-lookup"><span data-stu-id="9310d-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="9310d-198">Sipariş şimdi tamamlanmış olduğundan, mallar çekilebilir ve satış siparişine göre paketlenebilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="9310d-199">Vade farkı, satınalma faturası ve satış faturasını deftere nakleder.</span><span class="sxs-lookup"><span data-stu-id="9310d-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="9310d-200">Aşağıdaki resim bu senaryo için akış işlemini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9310d-200">The following illustration shows the flow for this scenario.</span></span>

![Gösteri senaryosu için akış](./media/use_rsa_tool_14.png)

<span data-ttu-id="9310d-202">Aşağıdaki şekil, RSAT'da bu senaryoya yönelik iş süreçlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9310d-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Demo senaryosu için iş süreçleri](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="9310d-204">Strateji – Önemli öğrenme</span><span class="sxs-lookup"><span data-stu-id="9310d-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="9310d-205">Veriler</span><span class="sxs-lookup"><span data-stu-id="9310d-205">Data</span></span>

- <span data-ttu-id="9310d-206">Temsili veri birimlerinizin (ürün/altın yapılandırma verilerinin bir kopyası ve geçirilen veriler) olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9310d-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="9310d-207">Görev kaydediciyle yeni veri oluşturduğunuzda, varolan adlarla çakışmayacak test adları oluşturun (örneğin, **RSATxxx**gibi bir önek kullanın).</span><span class="sxs-lookup"><span data-stu-id="9310d-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="9310d-208">Katman olmayan 1 ortamlarda testleri yeniden çalıştırmak için Azure Point geri yüklemeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="9310d-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="9310d-209">Benzersiz bir birleşim oluşturmak için yalnızca **RASGELE** ve **ŞiMDi** Excel işlevlerini kullanabilseniz de çalışma oldukça yüksektir.</span><span class="sxs-lookup"><span data-stu-id="9310d-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="9310d-210">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="9310d-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="9310d-211">Görev kaydedici</span><span class="sxs-lookup"><span data-stu-id="9310d-211">Task recorder</span></span>

- <span data-ttu-id="9310d-212">Kayıt başlamadan önce senaryoları tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="9310d-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="9310d-213">İyi yönetilen bir projede önceden tanımlanmış test senaryoları vardır.</span><span class="sxs-lookup"><span data-stu-id="9310d-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="9310d-214">Bir test olayı oluşturmak için, test senaryolarının sonucunun ne kadar tahmin edilebilir olduğunu düşünün.</span><span class="sxs-lookup"><span data-stu-id="9310d-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="9310d-215">Kayıtları, farklı roller tarafından gerçekleştirildikleri takdirde veya bir sonraki adımdan önce bekleme süresi veya dış olay varsa bölün.</span><span class="sxs-lookup"><span data-stu-id="9310d-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="9310d-216">Listelerdeki değerleri seçmeyi önleyin.</span><span class="sxs-lookup"><span data-stu-id="9310d-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="9310d-217">Bunun yerine **FIFO**, **AudioRM**, ve **SiteWH** gibi değerleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="9310d-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="9310d-218">Bir listeyi seçtiğinizde, listedeki değerin konumu değil, değeri kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="9310d-219">Bu listeye öğe eklenirse değerin konumu değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="9310d-220">Bu nedenle, kaydınız farklı bir parametre kullanacak ve bu durumda senaryonun geri kalanı etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="9310d-221">Çok kullanıcılı davranış hakkında düşünün.</span><span class="sxs-lookup"><span data-stu-id="9310d-221">Think about multi-user behavior.</span></span> <span data-ttu-id="9310d-222">Örneğin, yeni oluşturulan satış siparişiniz her zaman otomatik olarak seçilebilir olarak kabul edilmez.</span><span class="sxs-lookup"><span data-stu-id="9310d-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="9310d-223">Bunun yerine, doğru sıralamayı bulmak için her zaman filtreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="9310d-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="9310d-224">Zincirleme test durumlarında kullanılabilmesi için yeni oluşturulan ürünün adını kaydetmek üzere Görev kaydedicisindeki Kopyala işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9310d-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="9310d-225">Adımların doğru çalışmasını doğrulayan denetim noktalarını ayarlamak için Görev kaydedicisinin içindeki Doğrulama işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9310d-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="9310d-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="9310d-226">RSAT</span></span>

- <span data-ttu-id="9310d-227">Testi başka bir şirkette çalıştırmak için, şirketi Excel parametre dosyasının **Genel** sekmesinde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="9310d-228">Ayarların ve verilerin yeni seçilen şirkette kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9310d-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="9310d-229">Test kullanıcısını Excel parametre dosyasının **Genel** sekmesinden değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="9310d-230">Test çalışmasını çalışacak kullanıcının e-posta kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="9310d-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="9310d-231">Bu şekilde, test olayı, belirtilen kullanıcının güvenlik izinleri kullanılarak çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="9310d-232">Test başlatılmadan önce beklemek için Excel parametre dosyasının **Genel** sekmesine bir duraklama tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="9310d-233">Bu duraklatma, bir toplu işlemde kullanılabilir (örneğin, bir sonraki adımın gerçekleştirilebilmesi için bir iş akışının çalıştırılması gerektiğinde).</span><span class="sxs-lookup"><span data-stu-id="9310d-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="9310d-234">Gelişmiş kodlama</span><span class="sxs-lookup"><span data-stu-id="9310d-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="9310d-235">Komut satırı</span><span class="sxs-lookup"><span data-stu-id="9310d-235">Command line</span></span>

<span data-ttu-id="9310d-236">RSAT, bir **Komut İstemi** penceresinden çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="9310d-237">**TestRoot** ortam değişkeninin RSAT yükleme yolu olarak ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9310d-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="9310d-238">(Microsoft Windows'ta **Kontrol Paneli**'ni açın, **Sistem ve Güvenlik \> Sistem \> Gelişmiş sistem ayarları**'nı seçin ve sonra **Çevre Değişkenleri**'ni seçin.)</span><span class="sxs-lookup"><span data-stu-id="9310d-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="9310d-239">Bir **Komut İstemi** penceresini yönetici olarak açın.</span><span class="sxs-lookup"><span data-stu-id="9310d-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="9310d-240">Aracı yükleme dizininden çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="9310d-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="9310d-241">Tüm komutları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="9310d-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="9310d-242">Windows PowerShell örnekleri</span><span class="sxs-lookup"><span data-stu-id="9310d-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="9310d-243">Bir döngüde test olayı çalıştırma</span><span class="sxs-lookup"><span data-stu-id="9310d-243">Run a test case in a loop</span></span>

<span data-ttu-id="9310d-244">Yeni bir müşteri oluşturan bir test koduna sahipsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="9310d-245">Kodlama yoluyla, bu test olayı, her yineleme çalıştırılmadan önce aşağıdaki verileri rasgele bir döngüde çalışabilir:</span><span class="sxs-lookup"><span data-stu-id="9310d-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="9310d-246">Müşteri kodu</span><span class="sxs-lookup"><span data-stu-id="9310d-246">Customer ID</span></span>
- <span data-ttu-id="9310d-247">Müşteri adı</span><span class="sxs-lookup"><span data-stu-id="9310d-247">Customer name</span></span>
- <span data-ttu-id="9310d-248">Müşteri adresi</span><span class="sxs-lookup"><span data-stu-id="9310d-248">Customer address</span></span>

<span data-ttu-id="9310d-249">Müşteri kimliği *ATCUS\<number\>*, biçiminde  \<number\> **000000001** ve **999999999** değerleri arasında olacaktır.</span><span class="sxs-lookup"><span data-stu-id="9310d-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="9310d-250">Aşağıdaki örnek, kullanılan ilk sayıyı tanımlamak için **başlangıç** parametresi olan bir parametreyi kullanır.</span><span class="sxs-lookup"><span data-stu-id="9310d-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="9310d-251">Oluşturulması gereken müşteri sayısını tanımlamak için ikinci parametre olan **NR**öğesini kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9310d-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="9310d-252">Her yinelemede, Excel parametre dosyasındaki parametreler bir UpdateCustomer işlevi kullanılarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="9310d-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="9310d-253">Sonra, RSAT komut satırı bir RunTestCase işlevinde çağrılır.</span><span class="sxs-lookup"><span data-stu-id="9310d-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="9310d-254">Yönetici modunda Microsoft Windows PowerShell Integrated Scripting Environment (ISE) açın ve aşağıdaki kodu **Untitled1.ps1** adlı pencereye yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="9310d-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="9310d-255">Microsoft Dynamics 365'teki verilere bağlı olan bir komut dosyası çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9310d-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="9310d-256">Aşağıdaki örnek bir satınalma siparişinin sipariş durumunu bulmak için bir Open Data Protocol (OData) çağrısı kullanır.</span><span class="sxs-lookup"><span data-stu-id="9310d-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="9310d-257">Durum **faturalanmamışsa**, örneğin, faturayı deftere nakleden bir RSAT test olayı çağrısı yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9310d-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
