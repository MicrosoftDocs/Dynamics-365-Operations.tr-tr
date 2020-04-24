---
title: Regression Suite Automation Tool eğitimini kullanma
description: Bu konu, Regression Suite Automation Tool'un (RSAT) nasıl kullanılacağını gösterir. Çeşitli özellikleri tanımlar ve gelişmiş komut dosyası kullanan örnekler sağlar.
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 2d3dde69b102ce161e5c1f1dd393ffceca608bcb
ms.sourcegitcommit: 4fdee254649a751d46632fb4d0d48698e112fa72
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248748"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="11948-104">Regression Suite Automation Tool eğitimi kullanma</span><span class="sxs-lookup"><span data-stu-id="11948-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="11948-105">Bu sayfayı pdf formatında karşıdan yükleyip kaydetmek için internet tarayıcısı araçlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="11948-106">Bu öğretici, Regression Suite Automation Tool (RSAT) gelişmiş özelliklerinden bazılarının arasında, bir demo ataması içerir ve strateji ve önemli öğrenme noktalarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="11948-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span> 

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="11948-107">RSAT ve Görev kaydedicinin önemli özellikleri</span><span class="sxs-lookup"><span data-stu-id="11948-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="11948-108">Bir alan değeri doğrula</span><span class="sxs-lookup"><span data-stu-id="11948-108">Validate a field value</span></span>

<span data-ttu-id="11948-109">RSAT, beklenen değerleri doğrulamak için test olayınıza doğrulama adımları dahil etmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="11948-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="11948-110">Bu özellik hakkında bilgi için [Beklenen değerleri doğrulama](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="11948-110">For information about this feature, see the article [Validate expected values](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span></span>

<span data-ttu-id="11948-111">Aşağıdaki örnek, Eldeki stoğun 0'dan (sıfır) fazla olup olmadığı doğrulamak için bu özelliği nasıl kullanabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="11948-112">**USMF** şirketinde demo verilerinde, aşağıdaki adımları içeren bir görev kaydı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="11948-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="11948-113">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="11948-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="11948-114">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="11948-115">Örneğin, **Ürün numarası** alanını **1000** değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="11948-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="11948-116">**Eldeki stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="11948-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="11948-117">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="11948-118">Örneğin,  **Site** alanını **1** değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="11948-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="11948-119">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="11948-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="11948-120">**Toplam kullanılabilir** alanının değerinin **411.0000000000000000** olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="11948-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="11948-121">Görev kaydını kaydedin ve Azure DevOps'da test olayınıza ekleyin.</span><span class="sxs-lookup"><span data-stu-id="11948-121">Save the task recording and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="11948-122">Test durumunu test planına ekleyin ve test çalışmasını RSAT'a yükleyin.</span><span class="sxs-lookup"><span data-stu-id="11948-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="11948-123">Excel parametre dosyasını açın.</span><span class="sxs-lookup"><span data-stu-id="11948-123">Open the Excel parameter file.</span></span> <span data-ttu-id="11948-124">**InventOnhandItem** sekmesinde, **Operatör** alanı içeren bir **InventOnhandItem doğrula** bölümü göreceksiniz .</span><span class="sxs-lookup"><span data-stu-id="11948-124">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Operatör alanı](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="11948-126">Eldeki stok miktarının her zaman 0'dan büyük olacağını doğrulamak için **Değer** alanını **411**'den **0**'a ve **Operatör** alanının değerini eşittir işaretini (**=**) büyüktür işareti (**\>**) olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="11948-126">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Değer ve Operatör alanlarının değerleri değişti](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="11948-128">Kaydedin ve Excel parametresi dosyasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="11948-128">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="11948-129">Excel parametre dosyasında yaptığınız değişiklikleri Azure DevOps'a kaydetmek için **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="11948-129">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="11948-130">Şimdi, stokta belirtilen maddenin **Toplam Kullanılabilir** alanının değeri 0 (sıfır)'dan büyükse eldeki gerçek stok değerine bakılmaksızın testler geçer.</span><span class="sxs-lookup"><span data-stu-id="11948-130">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="11948-131">Kaydedilen değişkenler ve test olayları zinciri</span><span class="sxs-lookup"><span data-stu-id="11948-131">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="11948-132">RSAT'ın en önemli özelliklerinden biri test olaylarının zincirlenmesidir. Bir başka deyişle, bir testin diğer testlere değişken geçirme yeteneğidir.</span><span class="sxs-lookup"><span data-stu-id="11948-132">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="11948-133">Daha fazla bilgi için [Test olaylarını zincirlemek için değişkenleri kopyalama](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="11948-133">For more information, see the article [Copy variables to chain test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="11948-134">Türetilmiş test olayı</span><span class="sxs-lookup"><span data-stu-id="11948-134">Derived test case</span></span>

<span data-ttu-id="11948-135">RSAT, bir görevin farklı veri yapılandırmalarıyla çalışacak şekilde etkinleştirerek, aynı görev kaydını birden fazla test olayı ile kullanmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="11948-135">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="11948-136">Daha fazla bilgi için [Türetilmiş test olayları](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="11948-136">See the article [Derived test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="11948-137">Bildirimleri ve iletileri doğrulama</span><span class="sxs-lookup"><span data-stu-id="11948-137">Validate notifications and messages</span></span>

<span data-ttu-id="11948-138">Bu özellik, bir eylemin meydana geldiğini doğrulamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="11948-138">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="11948-139">Örneğin, bir üretim emri oluşturulduğunda, tahmin edildiğinde ve ardından başlatıldığında, uygulama üretim emrinin başlatıldığını size bildiren bir "Üretim-Başlangıcı" iletisi gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-139">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Üretim – Başlangıç bildirimi](./media/use_rsa_tool_05.png)

<span data-ttu-id="11948-141">Uygun kayıt için Excel parametre dosyasının **MessageValidation** sekmesine ileti metnini girerek bu iletiyi RSAT ile doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-141">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Mesaj doğrulama sekmesi](./media/use_rsa_tool_06.png)

<span data-ttu-id="11948-143">Test olayı çalıştırıldıktan sonra Excel parametre dosyasındaki ileti gösterilen iletiyle karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="11948-143">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="11948-144">İletiler eşleşmezse test olayı başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="11948-144">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="11948-145">Excel parametre dosyasındaki **MessageValidation** sekmesine birden çok ileti girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-145">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="11948-146">İletiler, bilgi iletileri yerine hata veya uyarı iletileri de olabilir.</span><span class="sxs-lookup"><span data-stu-id="11948-146">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="11948-147">Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="11948-147">Snapshot</span></span>

<span data-ttu-id="11948-148">Bu özellik, görev kaydı sırasında gerçekleştirilen adımların ekran görüntülerini alır.</span><span class="sxs-lookup"><span data-stu-id="11948-148">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="11948-149">Denetleme veya hata ayıklama amacıyla yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="11948-149">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="11948-150">Bu özelliği kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini  **yanlış**'tan **doğru**'ya çevirin.</span><span class="sxs-lookup"><span data-stu-id="11948-150">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="11948-151">Test olayını çalıştırdığınızda RSAT, çalışma dizinindeki test olaylarının oynatma klasöründeki adımlarının anlık görüntülerini (görüntüler) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11948-151">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="11948-152">RSAT'ın eski bir sürümünü kullanıyorsanız, görüntüler **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** konumuna kaydedilir, çalıştırılan her test olayı için ayrı bir klasör oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="11948-152">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="11948-153">Assignment</span><span class="sxs-lookup"><span data-stu-id="11948-153">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="11948-154">Senaryo</span><span class="sxs-lookup"><span data-stu-id="11948-154">Scenario</span></span>

1. <span data-ttu-id="11948-155">Ürün tasarımcısı, yeni bir serbest bırakılan ürün oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11948-155">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="11948-156">Üretim yöneticisi, stok düzeyini iki parçaya getirmek için bir üretim emri başlatır.</span><span class="sxs-lookup"><span data-stu-id="11948-156">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="11948-157">Üretim, üretim emrini başlatır ve sonlandırır ve eldeki miktarın iki parçadan oluştuğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="11948-157">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="11948-158">Satış ekibi, yeni ürünün dört parçadan oluşan siparişini alır.</span><span class="sxs-lookup"><span data-stu-id="11948-158">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="11948-159">Bu nedenle, satış ekibi net gereksinimleri dinamik plan aracılığıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="11948-159">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="11948-160">Kullanılabilir ek kapasite bulunmadığından, varsayılan sipariş ilkesi "yapmak yerine satın al" olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="11948-160">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="11948-161">Bu nedenle, planlı bir satınalma siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="11948-161">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="11948-162">Alıcı bir satıcı ekler, planlı satınalma siparişi sağlar ve sonra satınalma siparişini onaylar.</span><span class="sxs-lookup"><span data-stu-id="11948-162">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="11948-163">Satın alınan mallar mağazaya ulaştığında, mağaza operatörü ilgili satınalma siparişini arar ve malları alır.</span><span class="sxs-lookup"><span data-stu-id="11948-163">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="11948-164">Sipariş şimdi tamamlanmış olduğundan, mallar çekilebilir ve satış siparişine göre paketlenebilir.</span><span class="sxs-lookup"><span data-stu-id="11948-164">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="11948-165">Vade farkı, satınalma faturası ve satış faturasını deftere nakleder.</span><span class="sxs-lookup"><span data-stu-id="11948-165">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="11948-166">Aşağıdaki resim bu senaryo için akış işlemini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-166">The following illustration shows the flow for this scenario.</span></span>

![Gösteri senaryosu için akış](./media/use_rsa_tool_14.png)

<span data-ttu-id="11948-168">Aşağıdaki şekil, LCS İş Süreci Modelleyicisinde bu senaryoya ilişkin iş süreçleri hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-168">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Demo senaryosu için iş süreçleri](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="11948-170">Strateji – Önemli öğrenme</span><span class="sxs-lookup"><span data-stu-id="11948-170">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="11948-171">Veriler</span><span class="sxs-lookup"><span data-stu-id="11948-171">Data</span></span>

- <span data-ttu-id="11948-172">Temsili veri birimlerinizin (ürün/altın yapılandırma verilerinin bir kopyası ve geçirilen veriler) olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="11948-172">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="11948-173">Görev kaydediciyle yeni veri oluşturduğunuzda, var olan adlarla çakışmayacak test adları oluşturun (örneğin, **RSATxxx**gibi bir önek kullanın).</span><span class="sxs-lookup"><span data-stu-id="11948-173">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="11948-174">Katman olmayan 1 ortamlarda testleri yeniden çalıştırmak için Azure Point geri yüklemeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-174">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="11948-175">Benzersiz bir birleşim oluşturmak için yalnızca **RASGELE** ve **ŞiMDi** Excel işlevlerini kullanabilseniz de çalışma oldukça yüksektir.</span><span class="sxs-lookup"><span data-stu-id="11948-175">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="11948-176">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="11948-176">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="11948-177">Görev kaydedici</span><span class="sxs-lookup"><span data-stu-id="11948-177">Task recorder</span></span>

- <span data-ttu-id="11948-178">Kayıt başlamadan önce senaryoları tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="11948-178">Define scenarios before you start recording.</span></span> <span data-ttu-id="11948-179">İyi yönetilen bir projede önceden tanımlanmış test senaryoları vardır.</span><span class="sxs-lookup"><span data-stu-id="11948-179">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="11948-180">Bir test olayı oluşturmak için, test senaryolarının sonucunun ne kadar tahmin edilebilir olduğunu düşünün.</span><span class="sxs-lookup"><span data-stu-id="11948-180">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="11948-181">Kayıtları, farklı roller tarafından gerçekleştirildikleri takdirde veya bir sonraki adımdan önce bekleme süresi veya dış olay varsa bölün.</span><span class="sxs-lookup"><span data-stu-id="11948-181">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="11948-182">Listelerdeki değerleri seçmeyi önleyin.</span><span class="sxs-lookup"><span data-stu-id="11948-182">Avoid selecting values in lists.</span></span> <span data-ttu-id="11948-183">Bunun yerine **FIFO**, **AudioRM**, ve **SiteWH** gibi değerleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-183">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="11948-184">Bir listeyi seçtiğinizde, listedeki değerin konumu değil, değeri kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="11948-184">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="11948-185">Bu listeye öğe eklenirse değerin konumu değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="11948-185">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="11948-186">Bu nedenle, kaydınız farklı bir parametre kullanacak ve bu durumda senaryonun geri kalanı etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="11948-186">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="11948-187">Çok kullanıcılı davranış hakkında düşünün.</span><span class="sxs-lookup"><span data-stu-id="11948-187">Think about multi-user behavior.</span></span> <span data-ttu-id="11948-188">Örneğin, yeni oluşturulan satış siparişiniz her zaman otomatik olarak seçilebilir olarak kabul edilmez.</span><span class="sxs-lookup"><span data-stu-id="11948-188">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="11948-189">Bunun yerine, doğru sıralamayı bulmak için her zaman filtreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-189">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="11948-190">Zincirleme test durumlarında kullanılabilmesi için yeni oluşturulan ürünün adını kaydetmek üzere Görev kaydedicisindeki Kopyala işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-190">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="11948-191">Adımların doğru çalışmasını doğrulayan denetim noktalarını ayarlamak için Görev kaydedicisinin içindeki Doğrulama işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-191">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="11948-192">RSAT</span><span class="sxs-lookup"><span data-stu-id="11948-192">RSAT</span></span>

- <span data-ttu-id="11948-193">Testi başka bir şirkette çalıştırmak için, şirketi Excel parametre dosyasının **Genel** sekmesinde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-193">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="11948-194">Ayarların ve verilerin yeni seçilen şirkette kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="11948-194">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="11948-195">Test kullanıcısını Excel parametre dosyasının **Genel** sekmesinden değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-195">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="11948-196">Test çalışmasını çalışacak kullanıcının e-posta kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="11948-196">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="11948-197">Bu şekilde, test olayı, belirtilen kullanıcının güvenlik izinleri kullanılarak çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="11948-197">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="11948-198">Test başlatılmadan önce beklemek için Excel parametre dosyasının **Genel** sekmesine bir duraklama tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-198">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="11948-199">Bu duraklatma, bir toplu işlemde kullanılabilir (örneğin, bir sonraki adımın gerçekleştirilebilmesi için bir iş akışının çalıştırılması gerektiğinde).</span><span class="sxs-lookup"><span data-stu-id="11948-199">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="11948-200">Gelişmiş kodlama</span><span class="sxs-lookup"><span data-stu-id="11948-200">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="11948-201">CLI</span><span class="sxs-lookup"><span data-stu-id="11948-201">CLI</span></span>

<span data-ttu-id="11948-202">RSAT, bir **Komut İstemi** ya da **PowerShell** penceresinden çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="11948-202">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="11948-203">**TestRoot** ortam değişkeninin RSAT yükleme yolu olarak ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="11948-203">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="11948-204">(Microsoft Windows'ta **Kontrol Paneli**'ni açın, **Sistem ve Güvenlik \> Sistem \> Gelişmiş sistem ayarları**'nı seçin ve sonra **Çevre Değişkenleri**'ni seçin.)</span><span class="sxs-lookup"><span data-stu-id="11948-204">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="11948-205">Bir **Komut İstemi** ya da **PowerShell** penceresini yönetici olarak açın.</span><span class="sxs-lookup"><span data-stu-id="11948-205">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="11948-206">RSAT yükleme dizinine gidin.</span><span class="sxs-lookup"><span data-stu-id="11948-206">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="11948-207">Tüm komutları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="11948-207">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="11948-208">?</span><span class="sxs-lookup"><span data-stu-id="11948-208">?</span></span> 
<span data-ttu-id="11948-209">Kullanılabilen tüm komutlar ve parametreleriyle ilgili yardım gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-209">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="11948-210">İsteğe bağlı parametreleri</span><span class="sxs-lookup"><span data-stu-id="11948-210">Optional parameters</span></span>

**``command``**


<span data-ttu-id="11948-211">``[command]`` aşağıda belirtilen komutlardan biridir.</span><span class="sxs-lookup"><span data-stu-id="11948-211">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="11948-212">hakkında</span><span class="sxs-lookup"><span data-stu-id="11948-212">about</span></span>
<span data-ttu-id="11948-213">Geçerli sürümü gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-213">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="11948-214">cls</span><span class="sxs-lookup"><span data-stu-id="11948-214">cls</span></span>
<span data-ttu-id="11948-215">Ekranı temizler.</span><span class="sxs-lookup"><span data-stu-id="11948-215">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="11948-216">indir</span><span class="sxs-lookup"><span data-stu-id="11948-216">download</span></span>
<span data-ttu-id="11948-217">Belirtilen test çalışmasının eklerini çıkış dizinine yükler.</span><span class="sxs-lookup"><span data-stu-id="11948-217">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="11948-218">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-218">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="11948-219">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-219">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-220">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-220">Required parameters</span></span>
<span data-ttu-id="11948-221">**``test_case_id``** test çalışması kimliğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-221">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="11948-222">**``output_dir``** çıktı dizinini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-222">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="11948-223">Dizin mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11948-223">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-224">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-224">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="11948-225">düzenle</span><span class="sxs-lookup"><span data-stu-id="11948-225">edit</span></span>
<span data-ttu-id="11948-226">Excel programında parametreleri dosya açmanıza ve düzenlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="11948-226">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-227">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-227">Required parameters</span></span>
<span data-ttu-id="11948-228">**``excel_file``** varolan bir Excel dosyasının tam yolunu içermelidir.</span><span class="sxs-lookup"><span data-stu-id="11948-228">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-229">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-229">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="11948-230">oluştur</span><span class="sxs-lookup"><span data-stu-id="11948-230">generate</span></span>
<span data-ttu-id="11948-231">Çıkış dizininde belirtilen test çalışması için test yürütmesi ve parametre dosyaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11948-231">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="11948-232">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-232">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="11948-233">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-233">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-234">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-234">Required parameters</span></span>
<span data-ttu-id="11948-235">**``test_case_id``** test çalışması kimliğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-235">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="11948-236">**``output_dir``** çıktı dizinini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-236">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="11948-237">Dizin mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11948-237">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-238">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-238">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="11948-239">generatederived</span><span class="sxs-lookup"><span data-stu-id="11948-239">generatederived</span></span>
<span data-ttu-id="11948-240">Sağlanan test çalışmasının türevi olan yeni bir test durumu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11948-240">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="11948-241">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-241">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="11948-242">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-242">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-243">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-243">Required parameters</span></span>
<span data-ttu-id="11948-244">**``parent_test_case_id``** üst öğe test çalışması kimliğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-244">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="11948-245">**``test_plan_id``** test planı kimliğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-245">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="11948-246">**``test_suite_id``** test süiti kimliğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-246">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-247">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-247">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="11948-248">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="11948-248">generatetestonly</span></span>
<span data-ttu-id="11948-249">Çıkış dizininde belirtilen test çalışması için yalnızca test yürütmesi dosyası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11948-249">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="11948-250">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-250">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="11948-251">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-251">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-252">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-252">Required parameters</span></span>
<span data-ttu-id="11948-253">**``test_case_id``** test çalışması kimliğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-253">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="11948-254">**``output_dir``** çıktı dizinini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-254">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="11948-255">Dizin mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11948-255">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-256">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-256">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="11948-257">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="11948-257">generatetestsuite</span></span>
<span data-ttu-id="11948-258">Belirtilen paket için çıkış dizininde tüm test çalışmalarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="11948-258">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="11948-259">Tüm kullanılabilir test süitlerini almak için ``listtestsuitenames`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-259">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="11948-260">Sütundaki **test_suite_name** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-260">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-261">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-261">Required parameters</span></span>
<span data-ttu-id="11948-262">**``test_suite_name``** test süiti adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-262">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="11948-263">**``output_dir``** çıktı dizinini gösterir.</span><span class="sxs-lookup"><span data-stu-id="11948-263">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="11948-264">Dizin mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11948-264">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-265">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-265">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="11948-266">yardım</span><span class="sxs-lookup"><span data-stu-id="11948-266">help</span></span>
<span data-ttu-id="11948-267">Benzer mi [?](#section)</span><span class="sxs-lookup"><span data-stu-id="11948-267">Identical to the [?](#section)</span></span> <span data-ttu-id="11948-268">komut</span><span class="sxs-lookup"><span data-stu-id="11948-268">command</span></span>


#### <a name="list"></a><span data-ttu-id="11948-269">liste</span><span class="sxs-lookup"><span data-stu-id="11948-269">list</span></span>
<span data-ttu-id="11948-270">Tüm kullanılabilir test çalışmalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="11948-270">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="11948-271">listtestplans</span><span class="sxs-lookup"><span data-stu-id="11948-271">listtestplans</span></span>
<span data-ttu-id="11948-272">Tüm kullanılabilir test planlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="11948-272">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="11948-273">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="11948-273">listtestsuite</span></span>
<span data-ttu-id="11948-274">Belirtilen test paketiyle ilgili test çalışmalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="11948-274">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="11948-275">Tüm kullanılabilir test paketlerini almak için ``listtestsuitenames`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-275">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="11948-276">İlk sütundaki **suite_name** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-276">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-277">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-277">Required parameters</span></span>
<span data-ttu-id="11948-278">**``suite_name``** istenen paketin adı.</span><span class="sxs-lookup"><span data-stu-id="11948-278">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-279">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-279">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="11948-280">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="11948-280">listtestsuitenames</span></span>
<span data-ttu-id="11948-281">Tüm kullanılabilir test paketlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="11948-281">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="11948-282">yürütme</span><span class="sxs-lookup"><span data-stu-id="11948-282">playback</span></span>
<span data-ttu-id="11948-283">Excel dosyası kullanarak bir test durumunu yürütür.</span><span class="sxs-lookup"><span data-stu-id="11948-283">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-284">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-284">Required parameters</span></span>
<span data-ttu-id="11948-285">**``excel_file``** Excel dosyasının tam yolu.</span><span class="sxs-lookup"><span data-stu-id="11948-285">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="11948-286">Dosya var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11948-286">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="11948-287">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-287">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="11948-288">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="11948-288">playbackbyid</span></span>
<span data-ttu-id="11948-289">Aynı anda birden fazla test çalışmasını kayıttan yürütür.</span><span class="sxs-lookup"><span data-stu-id="11948-289">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="11948-290">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-290">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="11948-291">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-291">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-292">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-292">Required parameters</span></span>
<span data-ttu-id="11948-293">**``test_case_id1``** Varolan test çalışmasının kodu.</span><span class="sxs-lookup"><span data-stu-id="11948-293">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="11948-294">**``test_case_id2``** Varolan test çalışmasının kodu.</span><span class="sxs-lookup"><span data-stu-id="11948-294">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="11948-295">**``test_case_idN``** Varolan test çalışmasının kodu.</span><span class="sxs-lookup"><span data-stu-id="11948-295">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="11948-296">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-296">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="11948-297">playbackmany</span><span class="sxs-lookup"><span data-stu-id="11948-297">playbackmany</span></span>
<span data-ttu-id="11948-298">Excel dosyalarını kullanarak birçok test çalışmasını aynı anda kayıttan çalar.</span><span class="sxs-lookup"><span data-stu-id="11948-298">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-299">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-299">Required parameters</span></span>
<span data-ttu-id="11948-300">**``excel_file1``** Excel dosyasının tam yolu.</span><span class="sxs-lookup"><span data-stu-id="11948-300">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="11948-301">Dosya var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11948-301">File must exist.</span></span>  
<span data-ttu-id="11948-302">**``excel_file2``** Excel dosyasının tam yolu.</span><span class="sxs-lookup"><span data-stu-id="11948-302">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="11948-303">Dosya var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11948-303">File must exist.</span></span>  
<span data-ttu-id="11948-304">**``excel_fileN``** Excel dosyasının tam yolu.</span><span class="sxs-lookup"><span data-stu-id="11948-304">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="11948-305">Dosya var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="11948-305">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="11948-306">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-306">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="11948-307">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="11948-307">playbacksuite</span></span>
<span data-ttu-id="11948-308">Belirtilen test paketinden tüm test çalışmalarını kayıttan yürütür.</span><span class="sxs-lookup"><span data-stu-id="11948-308">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="11948-309">Tüm kullanılabilir test paketlerini almak için ``listtestsuitenames`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="11948-310">İlk sütundaki **suite_name** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="11948-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-311">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-311">Required parameters</span></span>
<span data-ttu-id="11948-312">**``suite_name``** istenen paketin adı.</span><span class="sxs-lookup"><span data-stu-id="11948-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-313">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-313">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="11948-314">çıkış</span><span class="sxs-lookup"><span data-stu-id="11948-314">quit</span></span>
<span data-ttu-id="11948-315">Uygulamayı kapatır.</span><span class="sxs-lookup"><span data-stu-id="11948-315">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="11948-316">yükle</span><span class="sxs-lookup"><span data-stu-id="11948-316">upload</span></span>
<span data-ttu-id="11948-317">Belirtilen test paketine veya test çalışmalarına ait olan tüm dosyaları karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="11948-317">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="11948-318">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-318">Required parameters</span></span>
<span data-ttu-id="11948-319">**``suite_name``** Belirtilen test paketine ait olan tüm dosyaları karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="11948-319">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="11948-320">**``testcase_id``** Belirtilen test çalışmalarına ait olan tüm dosyaları karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="11948-320">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-321">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-321">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="11948-322">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="11948-322">uploadrecording</span></span>
<span data-ttu-id="11948-323">Belirtilen test çalışmalarına ait olan yalnızca kayıt dosyasını karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="11948-323">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="11948-324">Gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="11948-324">Required parameters</span></span>
<span data-ttu-id="11948-325">**``testcase_id``** Belirtilen test çalışmalarına ait olan kayıt dosyasını karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="11948-325">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="11948-326">Örnekler</span><span class="sxs-lookup"><span data-stu-id="11948-326">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="11948-327">kullanım</span><span class="sxs-lookup"><span data-stu-id="11948-327">usage</span></span>
<span data-ttu-id="11948-328">Bu uygulamayı başlatmak için iki yol gösterir: bir tane varsayılan ayar dosyası kullanıldığında, diğeri ayar dosyası sağlar.</span><span class="sxs-lookup"><span data-stu-id="11948-328">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="11948-329">Windows PowerShell örnekleri</span><span class="sxs-lookup"><span data-stu-id="11948-329">Windows PowerShell examples</span></span>

[!IMPORTANT] <span data-ttu-id="11948-330">Aşağıdaki örnek komut dosyaları, gösterim amacıyla OLDUĞU GİBİ sağlanmıştır ve Microsoft tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="11948-330">The example scripts below are provided AS IS for illustration purposes and are not supported by Microsoft.</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="11948-331">Bir döngüde test olayı çalıştırma</span><span class="sxs-lookup"><span data-stu-id="11948-331">Run a test case in a loop</span></span>

<span data-ttu-id="11948-332">Yeni bir müşteri oluşturan bir test koduna sahipsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-332">You have a test script that creates a new customer.</span></span> <span data-ttu-id="11948-333">Kodlama yoluyla, bu test olayı, her yineleme çalıştırılmadan önce aşağıdaki verileri rasgele bir döngüde çalışabilir:</span><span class="sxs-lookup"><span data-stu-id="11948-333">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="11948-334">Müşteri kodu</span><span class="sxs-lookup"><span data-stu-id="11948-334">Customer ID</span></span>
- <span data-ttu-id="11948-335">Müşteri adı</span><span class="sxs-lookup"><span data-stu-id="11948-335">Customer name</span></span>
- <span data-ttu-id="11948-336">Müşteri adresi</span><span class="sxs-lookup"><span data-stu-id="11948-336">Customer address</span></span>

<span data-ttu-id="11948-337">Müşteri kimliği *ATCUS\<number\>*, biçiminde  \<number\> **000000001** ve **999999999** değerleri arasında olacaktır.</span><span class="sxs-lookup"><span data-stu-id="11948-337">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="11948-338">Aşağıdaki örnek, kullanılan ilk sayıyı tanımlamak için **başlangıç** parametresi olan bir parametreyi kullanır.</span><span class="sxs-lookup"><span data-stu-id="11948-338">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="11948-339">Oluşturulması gereken müşteri sayısını tanımlamak için ikinci parametre olan **NR**öğesini kullanılır.</span><span class="sxs-lookup"><span data-stu-id="11948-339">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="11948-340">Her yinelemede, Excel parametre dosyasındaki parametreler bir UpdateCustomer işlevi kullanılarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="11948-340">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="11948-341">Sonra, RSAT komut satırı bir RunTestCase işlevinde çağrılır.</span><span class="sxs-lookup"><span data-stu-id="11948-341">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="11948-342">Yönetici modunda Microsoft Windows PowerShell Integrated Scripting Environment (ISE) açın ve aşağıdaki kodu **Untitled1.ps1** adlı pencereye yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="11948-342">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
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
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="11948-343">Microsoft Dynamics 365'teki verilere bağlı olan bir komut dosyası çalıştırın</span><span class="sxs-lookup"><span data-stu-id="11948-343">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="11948-344">Aşağıdaki örnek bir satınalma siparişinin sipariş durumunu bulmak için bir Open Data Protocol (OData) çağrısı kullanır.</span><span class="sxs-lookup"><span data-stu-id="11948-344">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="11948-345">Durum **faturalanmamışsa**, örneğin, faturayı deftere nakleden bir RSAT test olayı çağrısı yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11948-345">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
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
