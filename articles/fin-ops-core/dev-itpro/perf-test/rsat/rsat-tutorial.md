---
title: Regression Suite Automation Tool eğitimi
description: Bu konu, Regression Suite Automation Tool'un (RSAT) nasıl kullanılacağını gösterir. Çeşitli özellikleri tanımlar ve gelişmiş komut dosyası kullanan örnekler sağlar.
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: a194e14c76827650e6752f331081ebe0c2130a13
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866168"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="ac33f-104">Regression Suite Automation Tool eğitimi</span><span class="sxs-lookup"><span data-stu-id="ac33f-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="ac33f-105">Bu sayfayı pdf formatında karşıdan yükleyip kaydetmek için internet tarayıcısı araçlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-105">Use your internet browser tools to download and save this page in pdf format.</span></span>

<span data-ttu-id="ac33f-106">Bu öğretici, Regression Suite Automation Tool (RSAT) gelişmiş özelliklerinden bazılarının arasında, bir demo ataması içerir ve strateji ve önemli öğrenme noktalarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="ac33f-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="ac33f-107">RSAT ve Görev kaydedicinin önemli özellikleri</span><span class="sxs-lookup"><span data-stu-id="ac33f-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="ac33f-108">Bir alan değeri doğrula</span><span class="sxs-lookup"><span data-stu-id="ac33f-108">Validate a field value</span></span>

<span data-ttu-id="ac33f-109">RSAT, beklenen değerleri doğrulamak için test olayınıza doğrulama adımları dahil etmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ac33f-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="ac33f-110">Bu özellik hakkında bilgi için [Beklenen değerleri doğrulama](rsat-validate-expected.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-110">For information about this feature, see the article [Validate expected values](rsat-validate-expected.md).</span></span>

<span data-ttu-id="ac33f-111">Aşağıdaki örnek, Eldeki stoğun 0'dan (sıfır) fazla olup olmadığı doğrulamak için bu özelliği nasıl kullanabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="ac33f-112">**USMF** şirketinde demo verilerinde, aşağıdaki adımları içeren bir görev kaydı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="ac33f-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="ac33f-113">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="ac33f-114">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ac33f-115">Örneğin, **Ürün numarası** alanını **1000** değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="ac33f-116">**Eldeki stok**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="ac33f-117">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ac33f-118">Örneğin,  **Site** alanını **1** değeriyle filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="ac33f-119">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="ac33f-120">**Toplam kullanılabilir** alanının değerinin **411.0000000000000000** olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="ac33f-121">Görev kaydını **geliştirici kaydı** olarak kaydedin ve Azure DevOps'ta test olayınıza ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-121">Save the task recording as a **developer recording** and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="ac33f-122">Test durumunu test planına ekleyin ve test çalışmasını RSAT'a yükleyin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="ac33f-123">Excel parametre dosyasını açın ve **TestCaseSteps** sekmesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-123">Open the Excel parameter file and go to the **TestCaseSteps** tab.</span></span>
5. <span data-ttu-id="ac33f-124">Eldeki stokun her zaman **0**'dan fazla olup olmayacağını doğrulamak için **Kullanılabilir Toplamı Doğrulama** adımına gidin ve değerini **411** yerine **0** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-124">To validate whether the inventory on-hand will always be more than **0**, go to the **Validate Total Available** step and change its value from **411** to **0**.</span></span> <span data-ttu-id="ac33f-125">**İşleç** alanının değerini, eşittir işareti (**=**) değerinden büyüktür işaretine (**\>**) değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-125">Change the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>
6. <span data-ttu-id="ac33f-126">Kaydedin ve Excel parametresi dosyasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-126">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="ac33f-127">Excel parametre dosyasında yaptığınız değişiklikleri Azure DevOps'a kaydetmek için **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-127">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="ac33f-128">Şimdi, stokta belirtilen maddenin **Toplam Kullanılabilir** alanının değeri 0 (sıfır)'dan büyükse eldeki gerçek stok değerine bakılmaksızın testler geçer.</span><span class="sxs-lookup"><span data-stu-id="ac33f-128">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="ac33f-129">Kaydedilen değişkenler ve test olayları zinciri</span><span class="sxs-lookup"><span data-stu-id="ac33f-129">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="ac33f-130">RSAT'ın en önemli özelliklerinden biri test olaylarının zincirlenmesidir. Bir başka deyişle, bir testin diğer testlere değişken geçirme yeteneğidir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-130">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="ac33f-131">Daha fazla bilgi için [Test olaylarını zincirlemek için değişkenleri kopyalama](rsat-chain-test-cases.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-131">For more information, see the article [Copy variables to chain test cases](rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="ac33f-132">Türetilmiş test olayı</span><span class="sxs-lookup"><span data-stu-id="ac33f-132">Derived test case</span></span>

<span data-ttu-id="ac33f-133">RSAT, bir görevin farklı veri yapılandırmalarıyla çalışacak şekilde etkinleştirerek, aynı görev kaydını birden fazla test olayı ile kullanmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ac33f-133">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="ac33f-134">Daha fazla bilgi için [Türetilmiş test olayları](rsat-derived-test-cases.md) makalesine bakın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-134">See the article [Derived test cases](rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="ac33f-135">Bildirimleri ve iletileri doğrulama</span><span class="sxs-lookup"><span data-stu-id="ac33f-135">Validate notifications and messages</span></span>

<span data-ttu-id="ac33f-136">Bu özellik, bir eylemin meydana geldiğini doğrulamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-136">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="ac33f-137">Örneğin, bir üretim emri oluşturulduğunda, tahmin edildiğinde ve ardından başlatıldığında, uygulama üretim emrinin başlatıldığını size bildiren bir "Üretim-Başlangıcı" iletisi gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-137">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Üretim – Başlangıç bildirimi](./media/use_rsa_tool_05.png)

<span data-ttu-id="ac33f-139">Uygun kayıt için Excel parametre dosyasının **MessageValidation** sekmesine ileti metnini girerek bu iletiyi RSAT ile doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-139">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Mesaj doğrulama sekmesi](./media/use_rsa_tool_06.png)

<span data-ttu-id="ac33f-141">Test olayı çalıştırıldıktan sonra Excel parametre dosyasındaki ileti gösterilen iletiyle karşılaştırılır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-141">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="ac33f-142">İletiler eşleşmezse test olayı başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="ac33f-142">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="ac33f-143">Excel parametre dosyasındaki **MessageValidation** sekmesine birden çok ileti girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-143">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="ac33f-144">İletiler, bilgi iletileri yerine hata veya uyarı iletileri de olabilir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-144">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="ac33f-145">Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="ac33f-145">Snapshot</span></span>

<span data-ttu-id="ac33f-146">Bu özellik, görev kaydı sırasında gerçekleştirilen adımların ekran görüntülerini alır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-146">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="ac33f-147">Denetleme veya hata ayıklama amacıyla yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-147">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="ac33f-148">Bu özelliği kullanmak için RSAT yükleme dosyasının altındaki (örneğin **C:\\Program Files (x86)\\Regression Suite Automation Tool**), **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** dosyasını açın ve aşağıdaki öğenin değerini  **yanlış**'tan **doğru**'ya çevirin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-148">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="ac33f-149">Test olayını çalıştırdığınızda RSAT, çalışma dizinindeki test olaylarının oynatma klasöründeki adımlarının anlık görüntülerini (görüntüler) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac33f-149">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="ac33f-150">RSAT'ın eski bir sürümünü kullanıyorsanız, görüntüler **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** konumuna kaydedilir, çalıştırılan her test olayı için ayrı bir klasör oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ac33f-150">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="ac33f-151">Assignment</span><span class="sxs-lookup"><span data-stu-id="ac33f-151">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="ac33f-152">Senaryo</span><span class="sxs-lookup"><span data-stu-id="ac33f-152">Scenario</span></span>

1. <span data-ttu-id="ac33f-153">Ürün tasarımcısı, yeni bir serbest bırakılan ürün oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac33f-153">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="ac33f-154">Üretim yöneticisi, stok düzeyini iki parçaya getirmek için bir üretim emri başlatır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-154">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="ac33f-155">Üretim, üretim emrini başlatır ve sonlandırır ve eldeki miktarın iki parçadan oluştuğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="ac33f-155">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="ac33f-156">Satış ekibi, yeni ürünün dört parçadan oluşan siparişini alır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-156">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="ac33f-157">Bu nedenle, satış ekibi net gereksinimleri dinamik plan aracılığıyla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-157">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="ac33f-158">Kullanılabilir ek kapasite bulunmadığından, varsayılan sipariş ilkesi "yapmak yerine satın al" olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-158">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="ac33f-159">Bu nedenle, planlı bir satınalma siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ac33f-159">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="ac33f-160">Alıcı bir satıcı ekler, planlı satınalma siparişi sağlar ve sonra satınalma siparişini onaylar.</span><span class="sxs-lookup"><span data-stu-id="ac33f-160">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="ac33f-161">Satın alınan mallar mağazaya ulaştığında, mağaza operatörü ilgili satınalma siparişini arar ve malları alır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-161">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="ac33f-162">Sipariş şimdi tamamlanmış olduğundan, mallar çekilebilir ve satış siparişine göre paketlenebilir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-162">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="ac33f-163">Vade farkı, satınalma faturası ve satış faturasını deftere nakleder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-163">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="ac33f-164">Aşağıdaki resim bu senaryo için akış işlemini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-164">The following illustration shows the flow for this scenario.</span></span>

![Gösteri senaryosu için akış](./media/use_rsa_tool_14.png)

<span data-ttu-id="ac33f-166">Aşağıdaki şekil, LCS İş Süreci Modelleyicisinde bu senaryoya ilişkin iş süreçleri hiyerarşisini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-166">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Demo senaryosu için iş süreçleri](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="ac33f-168">Strateji – Önemli öğrenme</span><span class="sxs-lookup"><span data-stu-id="ac33f-168">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="ac33f-169">Veriler</span><span class="sxs-lookup"><span data-stu-id="ac33f-169">Data</span></span>

- <span data-ttu-id="ac33f-170">Temsili veri birimlerinizin (ürün/altın yapılandırma verilerinin bir kopyası ve geçirilen veriler) olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ac33f-170">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="ac33f-171">Görev kaydediciyle yeni veri oluşturduğunuzda, var olan adlarla çakışmayacak test adları oluşturun (örneğin, **RSATxxx** gibi bir önek kullanın).</span><span class="sxs-lookup"><span data-stu-id="ac33f-171">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="ac33f-172">Katman olmayan 1 ortamlarda testleri yeniden çalıştırmak için Azure Point geri yüklemeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-172">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="ac33f-173">Benzersiz bir birleşim oluşturmak için yalnızca **RASGELE** ve **ŞiMDi** Excel işlevlerini kullanabilseniz de çalışma oldukça yüksektir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-173">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="ac33f-174">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-174">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="ac33f-175">Görev kaydedici</span><span class="sxs-lookup"><span data-stu-id="ac33f-175">Task recorder</span></span>

- <span data-ttu-id="ac33f-176">Kayıt başlamadan önce senaryoları tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-176">Define scenarios before you start recording.</span></span> <span data-ttu-id="ac33f-177">İyi yönetilen bir projede önceden tanımlanmış test senaryoları vardır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-177">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="ac33f-178">Bir test olayı oluşturmak için, test senaryolarının sonucunun ne kadar tahmin edilebilir olduğunu düşünün.</span><span class="sxs-lookup"><span data-stu-id="ac33f-178">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="ac33f-179">Kayıtları, farklı roller tarafından gerçekleştirildikleri takdirde veya bir sonraki adımdan önce bekleme süresi veya dış olay varsa bölün.</span><span class="sxs-lookup"><span data-stu-id="ac33f-179">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="ac33f-180">Listelerdeki değerleri seçmeyi önleyin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-180">Avoid selecting values in lists.</span></span> <span data-ttu-id="ac33f-181">Bunun yerine **FIFO**, **AudioRM**, ve **SiteWH** gibi değerleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-181">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="ac33f-182">Bir listeyi seçtiğinizde, listedeki değerin konumu değil, değeri kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-182">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="ac33f-183">Bu listeye öğe eklenirse değerin konumu değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-183">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="ac33f-184">Bu nedenle, kaydınız farklı bir parametre kullanacak ve bu durumda senaryonun geri kalanı etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-184">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="ac33f-185">Çok kullanıcılı davranış hakkında düşünün.</span><span class="sxs-lookup"><span data-stu-id="ac33f-185">Think about multi-user behavior.</span></span> <span data-ttu-id="ac33f-186">Örneğin, yeni oluşturulan satış siparişiniz her zaman otomatik olarak seçilebilir olarak kabul edilmez.</span><span class="sxs-lookup"><span data-stu-id="ac33f-186">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="ac33f-187">Bunun yerine, doğru sıralamayı bulmak için her zaman filtreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-187">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="ac33f-188">Zincirleme test durumlarında kullanılabilmesi için yeni oluşturulan ürünün adını kaydetmek üzere Görev kaydedicisindeki Kopyala işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-188">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="ac33f-189">Adımların doğru çalışmasını doğrulayan denetim noktalarını ayarlamak için Görev kaydedicisinin içindeki Doğrulama işlevini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-189">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="ac33f-190">RSAT</span><span class="sxs-lookup"><span data-stu-id="ac33f-190">RSAT</span></span>

- <span data-ttu-id="ac33f-191">Testi başka bir şirkette çalıştırmak için, şirketi Excel parametre dosyasının **Genel** sekmesinde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-191">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ac33f-192">Ayarların ve verilerin yeni seçilen şirkette kullanılabilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ac33f-192">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="ac33f-193">Test kullanıcısını Excel parametre dosyasının **Genel** sekmesinden değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-193">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ac33f-194">Test çalışmasını çalışacak kullanıcının e-posta kimliğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-194">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="ac33f-195">Bu şekilde, test olayı, belirtilen kullanıcının güvenlik izinleri kullanılarak çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-195">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="ac33f-196">Test başlatılmadan önce beklemek için Excel parametre dosyasının **Genel** sekmesine bir duraklama tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-196">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ac33f-197">Bu duraklatma, bir toplu işlemde kullanılabilir (örneğin, bir sonraki adımın gerçekleştirilebilmesi için bir iş akışının çalıştırılması gerektiğinde).</span><span class="sxs-lookup"><span data-stu-id="ac33f-197">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="ac33f-198">Gelişmiş kodlama</span><span class="sxs-lookup"><span data-stu-id="ac33f-198">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="ac33f-199">CLI</span><span class="sxs-lookup"><span data-stu-id="ac33f-199">CLI</span></span>

<span data-ttu-id="ac33f-200">RSAT, bir **Komut İstemi** ya da **PowerShell** penceresinden çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-200">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="ac33f-201">**TestRoot** ortam değişkeninin RSAT yükleme yolu olarak ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-201">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="ac33f-202">(Microsoft Windows'ta **Kontrol Paneli**'ni açın, **Sistem ve Güvenlik \> Sistem \> Gelişmiş sistem ayarları**'nı seçin ve sonra **Çevre Değişkenleri**'ni seçin.)</span><span class="sxs-lookup"><span data-stu-id="ac33f-202">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="ac33f-203">Bir **Komut İstemi** ya da **PowerShell** penceresini yönetici olarak açın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-203">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="ac33f-204">RSAT yükleme dizinine gidin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-204">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="ac33f-205">Tüm komutları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="ac33f-205">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="ac33f-206">?</span><span class="sxs-lookup"><span data-stu-id="ac33f-206">?</span></span>

<span data-ttu-id="ac33f-207">Kullanılabilen tüm komutlar ve parametreleriyle ilgili yardım gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-207">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a><span data-ttu-id="ac33f-208">?: İsteğe bağlı parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-208">?: Optional parameters</span></span>

<span data-ttu-id="ac33f-209">`command`: ``[command]`` öğesinin aşağıda belirtilen komutlardan biri olması durumu.</span><span class="sxs-lookup"><span data-stu-id="ac33f-209">`command`: Where ``[command]`` is one of the commands specified below.</span></span>

#### <a name="about"></a><span data-ttu-id="ac33f-210">hakkında</span><span class="sxs-lookup"><span data-stu-id="ac33f-210">about</span></span>

<span data-ttu-id="ac33f-211">Geçerli sürümü gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-211">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="ac33f-212">cls</span><span class="sxs-lookup"><span data-stu-id="ac33f-212">cls</span></span>

<span data-ttu-id="ac33f-213">Ekranı temizler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-213">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a><span data-ttu-id="ac33f-214">indir</span><span class="sxs-lookup"><span data-stu-id="ac33f-214">download</span></span>

<span data-ttu-id="ac33f-215">Belirtilen test çalışmasının eklerini çıkış dizinine yükler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-215">Downloads attachments for the specified test case to the output directory.</span></span>
<span data-ttu-id="ac33f-216">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-216">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ac33f-217">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-217">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a><span data-ttu-id="ac33f-218">download: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-218">download: required parameters</span></span>

+ <span data-ttu-id="ac33f-219">`test_case_id`: Test olayı kodunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-219">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="ac33f-220">`output_dir`: Çıktı dizinini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-220">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="ac33f-221">Dizin mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-221">The directory must exist.</span></span>

##### <a name="download-examples"></a><span data-ttu-id="ac33f-222">download: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-222">download: examples</span></span>

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a><span data-ttu-id="ac33f-223">düzenle</span><span class="sxs-lookup"><span data-stu-id="ac33f-223">edit</span></span>

<span data-ttu-id="ac33f-224">Excel programında parametreleri dosya açmanıza ve düzenlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-224">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a><span data-ttu-id="ac33f-225">edit: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-225">edit: required parameters</span></span>

+ <span data-ttu-id="ac33f-226">`excel_file`: Mevcut bir Excel dosyasının tam yolunu içermelidir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-226">`excel_file`: Must contain a full path to an existing Excel file.</span></span>

##### <a name="edit-examples"></a><span data-ttu-id="ac33f-227">edit: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-227">edit: examples</span></span>

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a><span data-ttu-id="ac33f-228">oluştur</span><span class="sxs-lookup"><span data-stu-id="ac33f-228">generate</span></span>

<span data-ttu-id="ac33f-229">Çıkış dizininde belirtilen test çalışması için test yürütmesi ve parametre dosyaları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac33f-229">Generates test execution and parameter files for the specified test case in the output directory.</span></span> <span data-ttu-id="ac33f-230">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-230">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ac33f-231">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-231">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a><span data-ttu-id="ac33f-232">generate: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-232">generate: required parameters</span></span>

+ <span data-ttu-id="ac33f-233">`test_case_id`: Test olayı kodunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-233">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="ac33f-234">`output_dir`: Çıktı dizinini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-234">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="ac33f-235">Dizin mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-235">The directory must exist.</span></span>

##### <a name="generate-examples"></a><span data-ttu-id="ac33f-236">generate: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-236">generate: examples</span></span>

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a><span data-ttu-id="ac33f-237">generatederived</span><span class="sxs-lookup"><span data-stu-id="ac33f-237">generatederived</span></span>

<span data-ttu-id="ac33f-238">Sağlanan test çalışmasının türevi olan yeni bir test durumu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac33f-238">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="ac33f-239">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-239">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ac33f-240">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-240">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a><span data-ttu-id="ac33f-241">generatederived: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-241">generatederived: required parameters</span></span>

+ <span data-ttu-id="ac33f-242">`parent_test_case_id`: Üst öğe test olayı kodunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-242">`parent_test_case_id`: Represents the parent test case ID.</span></span>
+ <span data-ttu-id="ac33f-243">`test_plan_id`: Test planı kodunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-243">`test_plan_id`: Represents the test plan ID.</span></span>
+ <span data-ttu-id="ac33f-244">`test_suite_id`: Test paketi kodunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-244">`test_suite_id`: Represents the test suite ID.</span></span>

##### <a name="generatederived-examples"></a><span data-ttu-id="ac33f-245">generatederived: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-245">generatederived: examples</span></span>

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a><span data-ttu-id="ac33f-246">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="ac33f-246">generatetestonly</span></span>

<span data-ttu-id="ac33f-247">Çıkış dizininde belirtilen test çalışması için yalnızca test yürütmesi dosyası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac33f-247">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="ac33f-248">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-248">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ac33f-249">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-249">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a><span data-ttu-id="ac33f-250">generatetestonly: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-250">generatetestonly: required parameters</span></span>

+ <span data-ttu-id="ac33f-251">`test_case_id`: Test olayı kodunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-251">`test_case_id`: Represents the test case ID.</span></span>
+ <span data-ttu-id="ac33f-252">`output_dir`: Çıktı dizinini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-252">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="ac33f-253">Dizin mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-253">The directory must exist.</span></span>

##### <a name="generatetestonly-examples"></a><span data-ttu-id="ac33f-254">generatetestonly: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-254">generatetestonly: examples</span></span>

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a><span data-ttu-id="ac33f-255">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="ac33f-255">generatetestsuite</span></span>

<span data-ttu-id="ac33f-256">Belirtilen paket için çıkış dizininde tüm test çalışmalarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ac33f-256">Generates all test cases for the specified suite in the output directory.</span></span> <span data-ttu-id="ac33f-257">Tüm kullanılabilir test süitlerini almak için ``listtestsuitenames`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-257">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="ac33f-258">Sütundaki **test_suite_name** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-258">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a><span data-ttu-id="ac33f-259">generatetestsuite: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-259">generatetestsuite: required parameters</span></span>

+ <span data-ttu-id="ac33f-260">`test_suite_name`: Test paketi adını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-260">`test_suite_name`: Represents the test suite name.</span></span>
+ <span data-ttu-id="ac33f-261">`output_dir`: Çıktı dizinini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ac33f-261">`output_dir`: Represents the output directory.</span></span> <span data-ttu-id="ac33f-262">Dizin mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-262">The directory must exist.</span></span>

##### <a name="generatetestsuite-examples"></a><span data-ttu-id="ac33f-263">generatetestsuite: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-263">generatetestsuite: examples</span></span>

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a><span data-ttu-id="ac33f-264">yardım</span><span class="sxs-lookup"><span data-stu-id="ac33f-264">help</span></span>

<span data-ttu-id="ac33f-265">Benzer mi [?](#section)</span><span class="sxs-lookup"><span data-stu-id="ac33f-265">Identical to the [?](#section)</span></span> <span data-ttu-id="ac33f-266">command.</span><span class="sxs-lookup"><span data-stu-id="ac33f-266">command.</span></span>

#### <a name="list"></a><span data-ttu-id="ac33f-267">liste</span><span class="sxs-lookup"><span data-stu-id="ac33f-267">list</span></span>

<span data-ttu-id="ac33f-268">Tüm kullanılabilir test çalışmalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-268">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a><span data-ttu-id="ac33f-269">listtestplans</span><span class="sxs-lookup"><span data-stu-id="ac33f-269">listtestplans</span></span>

<span data-ttu-id="ac33f-270">Tüm kullanılabilir test planlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-270">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a><span data-ttu-id="ac33f-271">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="ac33f-271">listtestsuite</span></span>

<span data-ttu-id="ac33f-272">Belirtilen test paketiyle ilgili test çalışmalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-272">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="ac33f-273">Tüm kullanılabilir test paketlerini almak için ``listtestsuitenames`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-273">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="ac33f-274">İlk sütundaki **suite_name** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-274">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a><span data-ttu-id="ac33f-275">listtestsuite: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-275">listtestsuite: required parameters</span></span>

+ <span data-ttu-id="ac33f-276">`suite_name`: İstenen paketin adı.</span><span class="sxs-lookup"><span data-stu-id="ac33f-276">`suite_name`: Name of the desired suite.</span></span>

##### <a name="listtestsuite-examples"></a><span data-ttu-id="ac33f-277">listtestsuite: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-277">listtestsuite: examples</span></span>

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a><span data-ttu-id="ac33f-278">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="ac33f-278">listtestsuitenames</span></span>

<span data-ttu-id="ac33f-279">Tüm kullanılabilir test paketlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-279">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a><span data-ttu-id="ac33f-280">yürütme</span><span class="sxs-lookup"><span data-stu-id="ac33f-280">playback</span></span>

<span data-ttu-id="ac33f-281">Excel dosyası kullanarak bir test durumunu yürütür.</span><span class="sxs-lookup"><span data-stu-id="ac33f-281">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a><span data-ttu-id="ac33f-282">playback: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-282">playback: required parameters</span></span>

+ <span data-ttu-id="ac33f-283">`excel_file`: Excel dosyasının tam yolu.</span><span class="sxs-lookup"><span data-stu-id="ac33f-283">`excel_file`: A full path to the Excel file.</span></span> <span data-ttu-id="ac33f-284">Dosya var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-284">File must exist.</span></span>

##### <a name="playback-examples"></a><span data-ttu-id="ac33f-285">playback: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-285">playback: examples</span></span>

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a><span data-ttu-id="ac33f-286">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="ac33f-286">playbackbyid</span></span>

<span data-ttu-id="ac33f-287">Aynı anda birden fazla test çalışmasını kayıttan yürütür.</span><span class="sxs-lookup"><span data-stu-id="ac33f-287">Plays back multiple test cases at once.</span></span> <span data-ttu-id="ac33f-288">Tüm kullanılabilir test çalışmalarını almak için ``list`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-288">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ac33f-289">İlk sütundaki **test_case_id** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-289">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a><span data-ttu-id="ac33f-290">playbackbyid: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-290">playbackbyid: required parameters</span></span>

+ <span data-ttu-id="ac33f-291">`test_case_id1`: Mevcut test olayının kodu.</span><span class="sxs-lookup"><span data-stu-id="ac33f-291">`test_case_id1`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="ac33f-292">`test_case_id2`: Mevcut test olayının kodu.</span><span class="sxs-lookup"><span data-stu-id="ac33f-292">`test_case_id2`: ID of exisiting test case.</span></span>
+ <span data-ttu-id="ac33f-293">`test_case_idN`: Mevcut test olayının kodu.</span><span class="sxs-lookup"><span data-stu-id="ac33f-293">`test_case_idN`: ID of exisiting test case.</span></span>

##### <a name="playbackbyid-examples"></a><span data-ttu-id="ac33f-294">playbackbyid: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-294">playbackbyid: examples</span></span>

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a><span data-ttu-id="ac33f-295">playbackmany</span><span class="sxs-lookup"><span data-stu-id="ac33f-295">playbackmany</span></span>

<span data-ttu-id="ac33f-296">Excel dosyalarını kullanarak birçok test çalışmasını aynı anda kayıttan çalar.</span><span class="sxs-lookup"><span data-stu-id="ac33f-296">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a><span data-ttu-id="ac33f-297">playbackmany: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-297">playbackmany: required parameters</span></span>

+ <span data-ttu-id="ac33f-298">`excel_file1`: Excel dosyasının tam yolu.</span><span class="sxs-lookup"><span data-stu-id="ac33f-298">`excel_file1`: Full path to the Excel file.</span></span> <span data-ttu-id="ac33f-299">Dosya var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-299">File must exist.</span></span>
+ <span data-ttu-id="ac33f-300">`excel_file2`: Excel dosyasının tam yolu.</span><span class="sxs-lookup"><span data-stu-id="ac33f-300">`excel_file2`: Full path to the Excel file.</span></span> <span data-ttu-id="ac33f-301">Dosya var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-301">File must exist.</span></span>
+ <span data-ttu-id="ac33f-302">`excel_fileN`: Excel dosyasının tam yolu.</span><span class="sxs-lookup"><span data-stu-id="ac33f-302">`excel_fileN`: Full path to the Excel file.</span></span> <span data-ttu-id="ac33f-303">Dosya var olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-303">File must exist.</span></span>

##### <a name="playbackmany-examples"></a><span data-ttu-id="ac33f-304">playbackmany: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-304">playbackmany: examples</span></span>

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a><span data-ttu-id="ac33f-305">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="ac33f-305">playbacksuite</span></span>

<span data-ttu-id="ac33f-306">Belirtilen test paketinden tüm test çalışmalarını kayıttan yürütür.</span><span class="sxs-lookup"><span data-stu-id="ac33f-306">Plays back all test cases from the specified test suite.</span></span>
<span data-ttu-id="ac33f-307">Tüm kullanılabilir test paketlerini almak için ``listtestsuitenames`` komutunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-307">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="ac33f-308">İlk sütundaki **suite_name** parametre olarak herhangi bir değeri kullanın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-308">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a><span data-ttu-id="ac33f-309">playbacksuite: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-309">playbacksuite: required parameters</span></span>

+ <span data-ttu-id="ac33f-310">`suite_name`: İstenen paketin adı.</span><span class="sxs-lookup"><span data-stu-id="ac33f-310">`suite_name`: Name of the desired suite.</span></span>

##### <a name="playbacksuite-examples"></a><span data-ttu-id="ac33f-311">playbacksuite: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-311">playbacksuite: examples</span></span>

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a><span data-ttu-id="ac33f-312">çıkış</span><span class="sxs-lookup"><span data-stu-id="ac33f-312">quit</span></span>

<span data-ttu-id="ac33f-313">Uygulamayı kapatır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-313">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a><span data-ttu-id="ac33f-314">yükle</span><span class="sxs-lookup"><span data-stu-id="ac33f-314">upload</span></span>

<span data-ttu-id="ac33f-315">Belirtilen test paketine veya test çalışmalarına ait olan tüm dosyaları karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-315">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a><span data-ttu-id="ac33f-316">upload: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-316">upload: required parameters</span></span>

+ <span data-ttu-id="ac33f-317">`suite_name`: Belirtilen test paketine ait olan tüm dosyaları karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-317">`suite_name`: All files belonging to the specified test suite will be uploaded.</span></span>
+ <span data-ttu-id="ac33f-318">`testcase_id`: Belirtilen test olaylarına ait olan tüm dosyaları karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-318">`testcase_id`: All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="upload-examples"></a><span data-ttu-id="ac33f-319">upload: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-319">upload: examples</span></span>

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a><span data-ttu-id="ac33f-320">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="ac33f-320">uploadrecording</span></span>

<span data-ttu-id="ac33f-321">Belirtilen test çalışmalarına ait olan yalnızca kayıt dosyasını karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-321">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a><span data-ttu-id="ac33f-322">uploadrecording: gerekli parametreler</span><span class="sxs-lookup"><span data-stu-id="ac33f-322">uploadrecording: required parameters</span></span>

+ <span data-ttu-id="ac33f-323">`testcase_id`: Belirtilen test olaylarına ait olan kayıt dosyasını karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="ac33f-323">`testcase_id`: Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="uploadrecording-examples"></a><span data-ttu-id="ac33f-324">uploadrecording: örnekler</span><span class="sxs-lookup"><span data-stu-id="ac33f-324">uploadrecording: examples</span></span>

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a><span data-ttu-id="ac33f-325">kullanım</span><span class="sxs-lookup"><span data-stu-id="ac33f-325">usage</span></span>

<span data-ttu-id="ac33f-326">Bu uygulamayı başlatmak için iki yol gösterir: bir tane varsayılan ayar dosyası kullanıldığında, diğeri ayar dosyası sağlar.</span><span class="sxs-lookup"><span data-stu-id="ac33f-326">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a><span data-ttu-id="ac33f-327">Windows PowerShell örnekleri</span><span class="sxs-lookup"><span data-stu-id="ac33f-327">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="ac33f-328">Bir döngüde test olayı çalıştırma</span><span class="sxs-lookup"><span data-stu-id="ac33f-328">Run a test case in a loop</span></span>

<span data-ttu-id="ac33f-329">Yeni bir müşteri oluşturan bir test koduna sahipsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-329">You have a test script that creates a new customer.</span></span> <span data-ttu-id="ac33f-330">Kodlama yoluyla, bu test olayı, her yineleme çalıştırılmadan önce aşağıdaki verileri rasgele bir döngüde çalışabilir:</span><span class="sxs-lookup"><span data-stu-id="ac33f-330">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="ac33f-331">Müşteri kodu</span><span class="sxs-lookup"><span data-stu-id="ac33f-331">Customer ID</span></span>
- <span data-ttu-id="ac33f-332">Müşteri adı</span><span class="sxs-lookup"><span data-stu-id="ac33f-332">Customer name</span></span>
- <span data-ttu-id="ac33f-333">Müşteri adresi</span><span class="sxs-lookup"><span data-stu-id="ac33f-333">Customer address</span></span>

<span data-ttu-id="ac33f-334">Müşteri kimliği *ATCUS\<number\>* biçiminde, \<number\> **000000001** ve **999999999** değerleri arasında olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-334">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="ac33f-335">Aşağıdaki örnek, kullanılan ilk sayıyı tanımlamak için **başlangıç** parametresi olan bir parametreyi kullanır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-335">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="ac33f-336">Oluşturulması gereken müşteri sayısını tanımlamak için ikinci parametre olan **NR** öğesini kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-336">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="ac33f-337">Her yinelemede, Excel parametre dosyasındaki parametreler bir UpdateCustomer işlevi kullanılarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac33f-337">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="ac33f-338">Sonra, RSAT komut satırı bir RunTestCase işlevinde çağrılır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-338">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="ac33f-339">Yönetici modunda Microsoft Windows PowerShell Integrated Scripting Environment (ISE) açın ve aşağıdaki kodu **Untitled1.ps1** adlı pencereye yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="ac33f-339">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="ac33f-340">Microsoft Dynamics 365'teki verilere bağlı olan bir komut dosyası çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ac33f-340">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="ac33f-341">Aşağıdaki örnek bir satınalma siparişinin sipariş durumunu bulmak için bir Open Data Protocol (OData) çağrısı kullanır.</span><span class="sxs-lookup"><span data-stu-id="ac33f-341">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="ac33f-342">Durum **faturalanmamışsa**, örneğin, faturayı deftere nakleden bir RSAT test olayı çağrısı yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac33f-342">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]