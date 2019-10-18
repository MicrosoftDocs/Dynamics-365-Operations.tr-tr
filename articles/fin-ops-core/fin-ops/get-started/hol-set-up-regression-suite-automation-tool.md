---
title: Regression Suite Automation Tool eğitimi ayarlama ve yükleme
description: Bu konu,Regression Suite Automation Tool'un (RSAT). nasıl ayarlanacağını ve yükleneceğini gösteren bir eğitimdir.
author: kfend
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 50450669387f4e2c9e81975d5345c525c7929c47
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180657"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="2f776-103">Regression Suite Automation Tool eğitimi ayarlama ve yükleme</span><span class="sxs-lookup"><span data-stu-id="2f776-103">Set up and install Regression suite automation tool tutorial</span></span>
<span data-ttu-id="2f776-104">Bu konu, RSAT ve RSAT kullanmayla ilgili araçları almanıza ve bu kurulumu başlatmanıza yardımcı olan bir eğitimdir.</span><span class="sxs-lookup"><span data-stu-id="2f776-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span> 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="2f776-105">Bu sayfayı PDF formatında karşıdan yükleyip kaydetmek için internet tarayıcısı araçlarını kullanın.</span><span class="sxs-lookup"><span data-stu-id="2f776-105">Use your internet browser tools to download and save this page in PDF format.</span></span> 

## <a name="key-concepts"></a><span data-ttu-id="2f776-106">Kilit kavramlar</span><span class="sxs-lookup"><span data-stu-id="2f776-106">Key concepts</span></span>

- <span data-ttu-id="2f776-107">Regression Suite Automation Tool'u (RSAT) destekleyen çeşitli uygulamalar için gerekli olan yükleme ve önkoşul kurulumunu anlayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="2f776-108">Görev kaydedici özelliğinin Microsoft Dynamics Lifecycle Services (LCS) ve Microsoft Azure DevOps ile birlikte test çalıştırmalarını oluşturmanıza, yapılandırmanıza, çalıştırmanıza, araştırmanıza ve raporlamanıza nasıl olanak tanıdığını öğrenin.</span><span class="sxs-lookup"><span data-stu-id="2f776-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="2f776-109">Görev kaydediciyi kullanarak iş görevlerini kaydetmek ve sonra görev kayıtlarını kaynak kodu yazmak zorunda kalmadan otomatik bir test paketine dönüştürmek için işlevsel kullanıcıları güçlendirin.</span><span class="sxs-lookup"><span data-stu-id="2f776-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="2f776-110">Başlamadan önce</span><span class="sxs-lookup"><span data-stu-id="2f776-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="2f776-111">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="2f776-111">Prerequisites</span></span>

- <span data-ttu-id="2f776-112">Bu öğretici için Microsoft Dynamics 365 for Finance and Operations sürüm 10.0 (Nisan 2019) ya da sonraki bir sürümü çalıştıran bir ortam gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2f776-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="2f776-113">Microsoft Dynamics 365 for Finance and Operations Enterprise edition 7.3, Platform update 20 (PU20) ya da sonrasını kullanan müşteriler için desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="2f776-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="2f776-114">Kullanıcının ortamda yönetici hakları olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f776-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="2f776-115">Müşteri kiracı LCS'sine ve Azure DevOps'a (daha önce Microsoft Visual Studio Team Services \[VSTS\] olarak bilinen)sahip olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="2f776-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="2f776-116">Test paketleri oluşturan ve yöneten kullanıcının Azure DevOps Test Planları veya Test Yöneticisi lisansı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f776-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="2f776-117">Aşağıdaki lisanslar Test Planlarına erişmenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="2f776-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="2f776-118">Visual Studio Kuruluş lisansı</span><span class="sxs-lookup"><span data-stu-id="2f776-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="2f776-119">Visual Studio Test Uzmanı lisansı</span><span class="sxs-lookup"><span data-stu-id="2f776-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="2f776-120">MSDN Platformları abone lisansı</span><span class="sxs-lookup"><span data-stu-id="2f776-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="2f776-121">RSAT'ın bir web tarayıcısı aracılığıyla test ortamına erişimi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f776-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="2f776-122">Test parametreleri oluşturmak ve düzenlemek için Microsoft Excel yüklü olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f776-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="2f776-123">Azure DevOps'ı yapılandır</span><span class="sxs-lookup"><span data-stu-id="2f776-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="2f776-124">Kullanıcı uygunluğu</span><span class="sxs-lookup"><span data-stu-id="2f776-124">User eligibility</span></span>

<span data-ttu-id="2f776-125">Kullanıcının Azure DevOps'da oluşturulduğundan ve Azure Test Planlarına erişim sağlayan bir abonelik düzeyine sahip olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2f776-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="2f776-126">Azure DevOps Test planı lisansının yalnızca, kullanıcının test çalışmalarını oluşturması ve yönetmesi gerekir (tüm RSAT kullanıcıları bu lisansı gerektirmez).</span><span class="sxs-lookup"><span data-stu-id="2f776-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="2f776-127">Lisans gereksinimleri hakkında daha fazla bilgi için bkz.  [Lisans gereklilikleri](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="2f776-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="2f776-128">Yeni Azure DevOps projesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f776-128">Create a new Azure DevOps project</span></span>
<span data-ttu-id="2f776-129">RSAT test çalışması için Azure DevOps, test paketi yönetimi, raporlama ve test olayı sonuçlarını araştırmaya yönelik kullanır.</span><span class="sxs-lookup"><span data-stu-id="2f776-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span> 

> [!NOTE]
> <span data-ttu-id="2f776-130">Varolan Azure DevOps projesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="2f776-131">Bununla birlikte, mevcut Azure DevOps projeniz özel bir şablona sahip olacak şekilde ayarlandıysa test olaylarını İş süreci modelleyiciden (BPM) Azure DevOps ile senkronize ettiğinizde "VSTS Senkronizasyon Hatası" hatası alırsınız (bkz. [BPM ile Azure DevOps eşitlemesini test etme](#test-the-synchronization-from-bpm-to-azure-devops) bölümü).</span><span class="sxs-lookup"><span data-stu-id="2f776-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="2f776-132">Aşağıdaki en iyi uygulamalar özel şablon için kullanılıyorsa test olaylarını Azure DevOps'a eşitleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="2f776-133">(Bu en iyi yöntemler hata iletisinde listelenmiştir.)</span><span class="sxs-lookup"><span data-stu-id="2f776-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="2f776-134">Herhangi bir iş öğesi türünü veya kullanıma hazır alanı silmeyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="2f776-135">İş öğesi türüne ilişkin herhangi bir durumu silmeyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="2f776-136">İş öğesi türüne herhangi bir gerekli alan eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-136">Do not add any required fields to a work item type.</span></span>

![En iyi yöntemler listesi ile ilgili hata iletisi](./media/setup_rsa_tool_02.png)

<span data-ttu-id="2f776-138">Aksi takdirde, bu öğreticide yeni bir Azure DevOps proje oluşturmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="2f776-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="2f776-139">Daha fazla bilgi için bkz. [Özel bir Azure DevOps (VSTS) işlem şablonu kullanarak BPM ile eşitleme sorunları](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="2f776-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="2f776-140">Azure DevOps URL'sini açma (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="2f776-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="2f776-141">Azure DevOps sayfasının sağ üst köşesinde **Proje oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Proje düğmesi oluşturma](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="2f776-143">Aşağıdaki alanları doldurun ve **Oluştur**'u seçin:</span><span class="sxs-lookup"><span data-stu-id="2f776-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="2f776-144">**Proje adı**</span><span class="sxs-lookup"><span data-stu-id="2f776-144">**Project name**</span></span>
    - <span data-ttu-id="2f776-145">**Sürüm kontrolü** –  **Team Foundation Sürüm Kontrolü**nü seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="2f776-146">**Git** varsayılan seçeneğinin desteklenmediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="2f776-147">**İş maddesi süreci**</span><span class="sxs-lookup"><span data-stu-id="2f776-147">**Work item process**</span></span>

    ![Yeni proje iletişim kutusu oluştur](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="2f776-149">Kişisel erişim belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f776-149">Create a personal access token</span></span>

<span data-ttu-id="2f776-150">Bu öğreticide, bir test durumu kitaplığı oluşturmak ve test olaylarınızı Azure DevOps ile eşitlemek için LCS İş Süreci Modelleyicisi'ni (BPM) kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="2f776-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="2f776-151">BPM ile Azure DevOps'u eşitlemek için kişisel erişim belirtecine ihtiyacınız olacak.</span><span class="sxs-lookup"><span data-stu-id="2f776-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="2f776-152">Azure DevOps projenize ait sayfanın sağ üst köşesinde bulunan profil simgesini seçin ve **Güvenlik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Güvenlik komutu](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="2f776-154">Sol bölmede, **Güvenlik** altında, **Kişisel erişim belirteçleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="2f776-155">Sonra **Yeni belirteç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-155">Then select **New Token**.</span></span>

    ![Kullanıcı ayarlarındaki kişisel erişim belirteçleri sekmesinde yeni belirteç düğmesi](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="2f776-157">Aşağıdaki alanları doldurun ve **Oluştur**'u seçin:</span><span class="sxs-lookup"><span data-stu-id="2f776-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="2f776-158">**Dosya Adı**</span><span class="sxs-lookup"><span data-stu-id="2f776-158">**Name**</span></span>
    - <span data-ttu-id="2f776-159">**Süre sonu (UTC)** – **Özel tanımlanmış** olarak seçeneği belirleyin ve sonra son kullanılabilir tarihi seçmek için tarih seçiciyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="2f776-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="2f776-160">**Kapsamlar** - **Tam erişim** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Yeni kişisel erişim belirteci iletişim kutusu oluşturma](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="2f776-162">Oluşturulan kişisel erişim belirtecini not edin.</span><span class="sxs-lookup"><span data-stu-id="2f776-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="2f776-163">RSAT yapılandırmasını kurduğunuzda daha sonra ihtiyacınız olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2f776-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Kişisel erişim belirteci](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="2f776-165">LCS projesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2f776-165">Configure the LCS project</span></span>

<span data-ttu-id="2f776-166">Ana test kitaplığınız için bir Lifecycle Services (LCS) projesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f776-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="2f776-167">İş Süreci Modelleyici (BPM) test durumlarınız için ana kitaplık olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2f776-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="2f776-168">BPM, test kitaplıklarını LCS projeleri üzerinden yönetmek ve dağıtmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2f776-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="2f776-169">Örneğin, bir Microsoft ortağı veya bağımsız yazılım satıcısı (ISV) oluşturma testi kitaplığı, test olayları BPM kitaplıkları biçiminde serbest bırakacaktır.</span><span class="sxs-lookup"><span data-stu-id="2f776-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="2f776-170">BPM'de, test olayları iş sürecine göre düzenlenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="2f776-171">BPM, test geçişinin yürütme sırasını veya sıklığını tanımlamaz.</span><span class="sxs-lookup"><span data-stu-id="2f776-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="2f776-172">Bu detaylar, bu konunun ilerisinde anlatıldığı gibi Azure DevOps'ta yönetilir.</span><span class="sxs-lookup"><span data-stu-id="2f776-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="2f776-173">LCS projeniz için varolan bir müşteri uygulamasını veya ortak projeyi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="2f776-174">LCS dil kodunu güncelleştir</span><span class="sxs-lookup"><span data-stu-id="2f776-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="2f776-175">İş süreçlerini doğru şekilde göstermek üzere Kullanıcı arabirimi (UI) için, LCS tercih edilen dili **İngilizce (Amerika Birleşik Devletleri)** olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f776-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="2f776-176">LCS uygulama projesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2f776-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="2f776-177">**Ayarlar** düğmesini (çark simgesi) sayfanın sağ üst köşesinde seçin ve sonra **Dil tercihleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Ayarlar menüsündeki komutlar](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="2f776-179">**Tercih edilen dil** alanında **İngilizce (Amerika Birleşik Devletleri)**'ni, seçin ve sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Kullanıcı ayarlarındaki dil tercihi sekmesi](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="2f776-181">LCS'yi Azure DevOps projesine bağlanacak şekilde yapılandırın</span><span class="sxs-lookup"><span data-stu-id="2f776-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="2f776-182">Daha önce yeni bir Azure DevOps projesi oluşturduysanız LCS projesini bu projeye bağlanacak şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="2f776-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="2f776-183">Bunun dışındaki durumlarda, LCS projeniz Azure DevOps projenize zaten bağlıysa sonraki bölüme devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="2f776-184">LCS uygulama projesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2f776-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="2f776-185">**Menü** düğmesini seçin ve sonra **Proje ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Proje sunucu komutu](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="2f776-187">Sol bölmede **Visual Studio Team Services**'i seçin ve sonra **Setup Visual Studio Team Services**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Proje ayarlarında Visual Studio Team Services sekmesi](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="2f776-189">**Azure DevOps sitesi URL'sinde** Azure DevOps sitesinin URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="2f776-190">**Kişisel erişim belirteci** alanında, daha önce oluşturulmuş olan kişisel erişim belirtecini girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-191">VSTS şimdi Azure DevOps olarak bilinmesine rağmen, LCS'yi Azure DevOps projenize bağlamak için eski URL'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="2f776-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="2f776-192">Örneğin bu örnekte kullanılan Azure DevOps URL'si: `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="2f776-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="2f776-193">Ancak, aşağıdaki çizimde şu şekilde girilmiştir: `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="2f776-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Kurulum adım 1 Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="2f776-195">**Devam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-195">Select **Continue**.</span></span>
6. <span data-ttu-id="2f776-196">**Visual Studio Team Services projesi** alanında LCS projesiyle ilişkilendirmek için seçilen sitedeki VSTS projesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="2f776-197">**Süreç şablonu** alanında **Çevik**'i varsayılan olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="2f776-198">Özel bir şablon için [Yeni bir Azure DevOps projesi oluşturma](#create-a-new-azure-devops-project) bölümündeki en iyi yöntem kılavuzunu gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="2f776-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="2f776-199">Sonra **Devam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-199">Then select **Continue**.</span></span>

    ![Kurulum adım 2 Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="2f776-201">Ayarlarınızı gözden geçirip **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-201">Review your settings, and then select **Save**.</span></span>

    ![Kurulum adım 3 Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="2f776-203">Adınıza **Yapılandırılmış** Azure DevOps sitesine erişmek ve VSTS ile birleşen özellikleri açmak için LCS'yi yetkilendirmek üzere Yetkilendir'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Yetkilendir düğmesi](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="2f776-205">"Visual Studio Team Services'a sizin adınıza bağlanması için LCS'yi yetkilendirmek üzere harici bir siteye yönlendirilmek üzeresiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="2f776-206">Devam edilsin mi?" sorusunu soracak bir mesaj kutusu görünür</span><span class="sxs-lookup"><span data-stu-id="2f776-206">Proceed?"</span></span> <span data-ttu-id="2f776-207">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-207">Select **Yes**.</span></span>

    ![İleti kutusu](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="2f776-209">**Kabul et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-209">Select **Accept**.</span></span>

    ![Erişim yetkilendiriliyor](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="2f776-211">Bir kullanıcı olarak yetkiniz varsa UI, LCS proje ayarları sayfasına dönmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Yetkilendiren kullanıcı](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="2f776-213">Yeni BPM kitaplığı oluştur</span><span class="sxs-lookup"><span data-stu-id="2f776-213">Create a new BPM library</span></span>

1. <span data-ttu-id="2f776-214">LCS uygulama projesine gidin.</span><span class="sxs-lookup"><span data-stu-id="2f776-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="2f776-215">**Menü** düğmesini seçin ve sonra **İş süreci modelleyici**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![İş süreci modelleyici komutu](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="2f776-217">**Yeni kitaplık**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-217">Select **New library**.</span></span>

    ![Yeni kitaplık oluştur düğmesi](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="2f776-219">**Kitaplık adı** alanına bir ad girin ve **oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="2f776-220">Bu öğretici için BPM kitaplığını **RSAT** olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="2f776-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Yeni kitaplık iletişim kutusu oluşturma](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="2f776-222">Yeni **RSAT** BPM kitaplığını açın.</span><span class="sxs-lookup"><span data-stu-id="2f776-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="2f776-223">**Örnek Çekirdek İş Süreci** sürecini seçin ve sağ taraftaki **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Düzenleme modu düğmesi](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="2f776-225">Hem **Ad** alanını hem de **Açıklama** alanını **Ürün oluştur** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2f776-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="2f776-226">Sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-226">Then select **Save**.</span></span>

    ![Ad ve Açıklama alanları](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="2f776-228">Ortam</span><span class="sxs-lookup"><span data-stu-id="2f776-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="2f776-229">Sürüm gereksinimi</span><span class="sxs-lookup"><span data-stu-id="2f776-229">Version requirement</span></span>

<span data-ttu-id="2f776-230">Sürüm 10'un çalıştığı test veya korumalı alan ortamı gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2f776-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="2f776-231">7.3, Platform update 20 (PU20) ya da sonrasını kullanan müşteriler için desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="2f776-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="2f776-232">RSAT'ın bir web tarayıcısı aracılığıyla test ortamına erişimi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f776-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="2f776-233">Kullanıcı ölçütü</span><span class="sxs-lookup"><span data-stu-id="2f776-233">User criteria</span></span>

<span data-ttu-id="2f776-234">Kullanıcının bu ortamda yönetici hakları olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f776-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="2f776-235">LCS ile bağlantı kurmak için yardım ayarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="2f776-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="2f776-236">Bu adım, LCS ile ilgili olarak görev kayıtlarının istemci aracılığıyla LCS içindeki uygun BPM kitaplığına kaydedilebileceği şekilde bağlanmak için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2f776-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="2f776-237">İstemciyi açın.</span><span class="sxs-lookup"><span data-stu-id="2f776-237">Open the client.</span></span>
2. <span data-ttu-id="2f776-238">**Sistem Yönetimi \> Kurulum \> Sistem parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2f776-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="2f776-239">**Yardım** sekmesinde **Lifecycle Services yardım yapılandırması** alanında ilgili LCS projesini (bu eğiticide**RSAT**) seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Yardım sekmesindeki Lifecycle Services Yardımı yapılandırma sekmesi](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="2f776-241">BPM kitaplıkları uygun LCS projesi altında doldurulur.</span><span class="sxs-lookup"><span data-stu-id="2f776-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="2f776-242">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-242">Select **Save**.</span></span>
5. <span data-ttu-id="2f776-243">Güncelleştirilmiş Yardım içeriğini görmek için tarayıcıyı yenilemeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="2f776-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Tarayıcıyı yenileme hakkında bildirim](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="2f776-245">Görev kayıtları</span><span class="sxs-lookup"><span data-stu-id="2f776-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="2f776-246">Tüm görev kayıtlarınızın ana panoda göründüğünden emin olun.</span><span class="sxs-lookup"><span data-stu-id="2f776-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="2f776-247">Tek kayıtların kısa kalmasını sağlayın ve satış siparişi oluşturma gibi bir iş görevine odaklanın.</span><span class="sxs-lookup"><span data-stu-id="2f776-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="2f776-248">Görev kaydı oluşturma ve bunu BPM kitaplığına kaydetme</span><span class="sxs-lookup"><span data-stu-id="2f776-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="2f776-249">Yeni BPM kitaplığında oluşturulan basit iş sürecine ekleyebileceğiniz ilgili bir görev kaydı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2f776-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="2f776-250">İstemciyi açın.</span><span class="sxs-lookup"><span data-stu-id="2f776-250">Open the client.</span></span>
2. <span data-ttu-id="2f776-251">Ana panoda **Ayarlar** düğmesini (çark simgesi) seçin ve sonra **Görev kaydedici**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Ayarlar menüsündeki komutlar](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="2f776-253">**Kayıt oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-253">Select **Create recording**.</span></span>

    ![Yeni kayıt oluşturma düğmesi](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="2f776-255">**Kayıt adı** ve **Kayıt açıklaması** alanlarını doldurun ve **Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Kayıt adı ve Kayıt açıklaması alanları](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="2f776-257">Ürün oluşturma adımlarını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2f776-257">Record the steps for creating a product.</span></span> <span data-ttu-id="2f776-258">Bitirdiğinizde kaydı durdurmak için **Durdur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Bir ürün oluşturma adımları](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="2f776-260">**Lifecycle Services'e kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-260">Select **Save to Lifecycle Services**.</span></span>

    ![Kaydetme seçenekleri](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="2f776-262">Kitaplık bilgileri LCS'den yüklenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-262">Library information is loaded from LCS.</span></span>

    ![İlerleme göstergesi](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="2f776-264">Görev kaydını ilişkilendirmek için BPM kitaplığını seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="2f776-265">Bu öğretici için, yukarıda oluşturulmuş **RSAT** BPM kitaplığını seçin ve altında **Ürün oluşturma** iş sürecini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="2f776-266">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-266">Then select **OK**.</span></span>

    ![Görev kaydını bir BPM kitaplığıyla ve bir iş süreciyle ilişkilendirme](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="2f776-268">Bir "Lifecycle Services'a başarıyla kaydedildi" iletisi görünür.</span><span class="sxs-lookup"><span data-stu-id="2f776-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![LCS'ye başarılı bir kayıt ile ilgili ileti](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="2f776-270">Görev kaydını yerel olarak kaydetmek ve daha sonra LCS yoluyla BPM ile yüklemek istiyorsanız şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="2f776-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="2f776-271">Kayıt tamamlandıktan sonra **Bu bilgisayara kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Kaydetme seçenekleri](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="2f776-273">Dosyayı yerel bilgisayarınıza kaydetmek için tarayıcının bildirim çubuğunda **Kaydet** veya **Farklı kaydet** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Bildirim çubuğu](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="2f776-275">**RSAT** BPM kitaplığına gidin ve görev kaydını kaydedeceğiniz iş sürecini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="2f776-276">**Genel** sekmesinde **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Yükle düğmesi](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="2f776-278">**Gözat**'ı seçin ve daha önce kaydettiğiniz .axtr dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="2f776-279">Sonra **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-279">Then select **Upload**.</span></span>

        ![Karşıya yüklenecek. axtr dosyasını seçme](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="2f776-281">BPM ile Azure DevOps eşitlemesini test etme</span><span class="sxs-lookup"><span data-stu-id="2f776-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="2f776-282">Bir görev kaydı iş sürecine iliştirildiğinde, (sırasıyla) LCS'deki VSTS eşitleme özelliğini kullanarak iş işleminin ve ilişkili görev kaydının özellik ve test olayı Azure DevOps olarak eşitlenebildiğini doğrulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f776-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="2f776-283">' Azure DevOps'ta oluşturulan ilgili iş öğesi türü, LCS projesini Azure DevOps'ta yapılandırdığınızda yeni [Yeni bir Azure DevOps projesi oluşturma](#create-a-new-azure-devops-project) bölümünde açıklandığı gibi seçtiğiniz işlem şablonuna bağlı olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="2f776-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="2f776-284">BPM kitaplığına gidin ve daha önce oluşturduğunuz **RSAT** kitaplığını açın.</span><span class="sxs-lookup"><span data-stu-id="2f776-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="2f776-285">Üç nokta düğmesini (**...**) ve **VSTS Eşitleme** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![Üç nokta menüsünde VSTS eşitleme komutu](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="2f776-287">VSTS eşitleme işlemi tamamlandıktan sonra sol tarafta**Gereksinimler** sekmesi görünür ve bu, ilgili Azure DevOps iş öğesini içerir.</span><span class="sxs-lookup"><span data-stu-id="2f776-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-288">Azure DevOps'ta oluşturulan iş öğesi başlığı ön eki olarak BPM kitaplığının adına sahip olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2f776-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Gereksinimler sekmesi](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="2f776-290">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-290">Refresh the page.</span></span>
4. <span data-ttu-id="2f776-291">Üç nokta düğmesini (**...**) Ek bir seçenek olan **Test olaylarını eşitle**'de göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="2f776-292">Bu seçeneği seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-292">Select this option.</span></span>

    ![Üç nokta menüsünde test olaylarını eşitle menüsü](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="2f776-294">**Test olaylarını eşitle** sayfayı yeniledikten sonra da açılmıyorsa BPM için ana sayfaya gidin ve tüm kitaplık için **Test olaylarını eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="2f776-295">Böylece, tüm kitaplık için eşitlemeyi etkili şekilde zorlarsınız.</span><span class="sxs-lookup"><span data-stu-id="2f776-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    > 
    > ![Tüm kitaplık için test olaylarını Eşitlemeyi seçme](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="2f776-297">Test olaylarını eşitlemeyi tamamlandıktan sonra **Gereksinimler** sekmesinde yeni bir test olayı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2f776-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Gereksinimler sekmesinde yeni test olayı](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="2f776-299">Azure DevOps projenize gidin ve  **Panolar \> Çalışma Maddeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Panolar altında Çalışma Maddeleri komutu](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="2f776-301">BPM eşitlemesi aracılığıyla oluşturduğunuz iş öğesinin ve test olayının varolduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![İş maddesi ve test olayı](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="2f776-303">RSAT'ı yükleme ve Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2f776-303">Install and Configure RSAT</span></span>

<span data-ttu-id="2f776-304">RSAT, Windows 10 çalıştıran ve ortama bir web tarayıcısı üzerinden bağlanabilen herhangi bir bilgisayara kurulabilir (Internet Explorer ya da Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="2f776-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="2f776-305">Aracın yeni bir sürümünü yüklemeden önce önceki sürümü kaldırmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="2f776-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="2f776-306">Kimlik doğrulama sertifikası yükleme</span><span class="sxs-lookup"><span data-stu-id="2f776-306">Install an authentication certificate</span></span>

<span data-ttu-id="2f776-307">Kimlik doğrulamayı etkinleştirmek için, RSAT'ın çalıştığı bilgisayara bir sertifika oluşturmanız ve yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f776-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="2f776-308">Yeni bir sertifika oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f776-308">Generate a certificate</span></span>

1. <span data-ttu-id="2f776-309">Sertifika dosyası oluşturmak için, bir Microsoft Windows PowerShell penceresini yönetici olarak açın ve aşağıdaki komutu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2f776-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="2f776-310">**Çalıştır** iletişim kutusuna **certlm.msc** girerek sertifika yöneticisini açın ve **Kişisel \> Sertifikalar**'ın altındaki **D365 Otomatik test sertifikası** sertifikasını onaylayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-311">Sertifikalar yerel bilgisayarda depolandığından **certmgr.msc** değil **certlm.msc** yazdığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2f776-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![D365 otomatik test sertifikası sertifikası](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="2f776-313">Sertifikada sağa tıklayın ve sonra **Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="2f776-314">**Güvenilen Kök Sertifika Yetkilileri \> Sertifikalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2f776-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Güvenilen Kök Sertifika Yetkilileri klasörü altındaki sertifikalar klasörü](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="2f776-316">**Eylem** menüsünde sertifikayı **Güvenilen Kök Sertifika Yetkilileri** konumuna yapıştırmak için **Yapıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Yapıştır komutu Eylem menüsü](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="2f776-318">Boşluk veya özel karakterler olmadan yüklü sertifikanın parmak izini almak için bir Windows PowerShell penceresini yönetici olarak açın ve aşağıdaki komutları çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2f776-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="2f776-319">Daha sonra Uygulama Nesne Sunucusu (AOS) için .wif dosyalarını güncelleştirdiğinizde ve RSAT yapılandırmasını kurduğunuzda bu dosyaya ihtiyacınız olacağından parmak izini kaydedin.</span><span class="sxs-lookup"><span data-stu-id="2f776-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="2f776-320">AOS bilgisayarını bağlantıya güvenecek şekilde yapılandırın</span><span class="sxs-lookup"><span data-stu-id="2f776-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="2f776-321">Ortam bir katman 2 + ortamıysa ortam için **Tüm** AOS bilgisayarları için wif.config dosyasında sertifika parmak izi güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2f776-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="2f776-322">AOS bilgisayarına bir Uzaktan Masaüstü Protokolü (RDP) bağlantısı kurun.</span><span class="sxs-lookup"><span data-stu-id="2f776-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="2f776-323">Oturum açma ayrıntıları LCS içindeki ortam ayrıntıları sayfasında bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="2f776-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="2f776-324">Microsoft Internet Information Services'i (IIS) açın ve site listesinde **AOSService**'i bulun.</span><span class="sxs-lookup"><span data-stu-id="2f776-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![Siteler listesinde AOSService](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="2f776-326">**\<Sürücü\>: \\AosService\\WebRoot** dosyasını açmak için **Keşfet**'e sağ tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="2f776-327">**wif.config** dosyasını bulun.</span><span class="sxs-lookup"><span data-stu-id="2f776-327">Find the **wif.config** file.</span></span>

    ![WebRoot klasöründe wif.config dosyası](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="2f776-329">Aşağıdaki örnekte gösterildiği gibi, **wif.config** dosyasını sertifikanız ve yetki adınız için yeni bir yetki girişi ekleyerek günceştirin.</span><span class="sxs-lookup"><span data-stu-id="2f776-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="2f776-330">Birden fazla kullanıcı aynı uygulamayı kullanıyorsa her kullanıcı ayrı parmak izleri oluşturmalı ve bu parmak izlerinin her biri **\<anahtarlar\>** bölümüne eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="2f776-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="2f776-331">Birden fazla AOS bilgisayarı varsa her ek bilgisayar için 3. ile 4. adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-332">Eski katman 2 ortamlarından farklı olarak yeni katman 2 ortamları iki AOS örneğiyle dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="2f776-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="2f776-333">Tüm AOS bilgisayarlarında **iisreset**'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2f776-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-334">Bir katman 1 bilgisayarında **iistreset**'i çalıştırmak için yönetici haklarına sahip değilseniz LCS içindeki ortam ayrıntıları sayfasında, Yönet > Yeniden başlat hizmetlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="2f776-335">Katman 2+ ortamı</span><span class="sxs-lookup"><span data-stu-id="2f776-335">Tier 2+ environment</span></span>

<span data-ttu-id="2f776-336">Katman 2 + (Standart kabul testi sanal alanı veya daha ileri) ortamı kullanılıyorsa RSAT'ın yüklendiği bilgisayarda aşağıdaki kayıt defteri ayarını doğrulayın veya ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="2f776-337">Bu adım, kimlik doğrulama veya RSAT bağlantı hatalarından kaçınmanıza yardımcı olacağından gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2f776-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="2f776-338">RSAT öğesini yükle</span><span class="sxs-lookup"><span data-stu-id="2f776-338">Install RSAT</span></span>

1. <span data-ttu-id="2f776-339"><https://www.microsoft.com/download/details.aspx?id=57357>'a gidin ve **İndir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="2f776-340">Tüm dosyaları seçin ve sonra **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-340">Select all the files, and then select **Next**.</span></span>

    ![Tüm dosyalar seçiliyor](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="2f776-342">Yükleyiciyi çalıştırmak için .msi paketine çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="2f776-343">Yükleme tamamlandığında **Son**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT Yükleyici dosyası](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="2f776-345">Selenium ve tarayıcı sürücülerini yükleme</span><span class="sxs-lookup"><span data-stu-id="2f776-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="2f776-346">RSAT'ın eski sürümlerinde, Selenium ve Tarayıcı sürücülerini yüklemeniz gerekiyordu.</span><span class="sxs-lookup"><span data-stu-id="2f776-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="2f776-347">Bu sürücüleri, otomatik olarak yüklendiğinden yüklemeniz artık gerekmez.</span><span class="sxs-lookup"><span data-stu-id="2f776-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="2f776-348">RSAT'ı ilk açışınızda, Selenium'u otomatik olarak karşıdan yükleyip kurmanız istenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="2f776-349">Daha fazla bilgi için [Configure RSAT](#configure-rsat) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="2f776-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="2f776-350">Bir test olayını çalıştırabilmeniz için, RSAT yapılandırmasında seçilen varsayılan tarayıcıya karşılık gelen tarayıcı sürücüsünü otomatik olarak karşıdan yükleyip kurmanız istenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="2f776-351">Daha fazla bilgi için [Test çalışmalarını yükleme ve çalıştırma](#load-and-run-test-cases) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="2f776-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="2f776-352">RSAT kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="2f776-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="2f776-353">Test planı ve test paketleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f776-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="2f776-354">Azure DevOps projesine gidin ve **Test Planları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Test planları komutu](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="2f776-356">**Yeni Test Planı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-356">Select **New Test Plan**.</span></span>

    ![Yeni Test Planı düğmesi](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="2f776-358">**Ad** alanını doldurun ve sonra **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="2f776-359">Bu öğretici için test planını **RSAT test planı** olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="2f776-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Yeni Test Planı iletişim kutusu](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="2f776-361">Artı işaretini (**+**) seçin ve sonra yeni test planı altında **Statik paket** oluşturmak için statik paketi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="2f776-362">Yeni test paketini **T01 – Stoka Aktar** olarak adlandırın.</span><span class="sxs-lookup"><span data-stu-id="2f776-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-363">Ayrıca, yeni test olaylarını BPM'den otomatik olarak RSAT test paketine çekilmesini istiyorsanız sorgu tabanlı bir paket oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Statik bir paket oluşturma](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="2f776-365">Test paketlerine test olayları iliştirme</span><span class="sxs-lookup"><span data-stu-id="2f776-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="2f776-366">Test paketine varolan test olaylarını eklemek için sağ taraftan **Varolanı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Varolan faaliyeti ekleme düğmesi](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="2f776-368">**Pakete test olaylarını ekle** sayfasında **Sorguyu çalıştır**'ı seçin, ve sonra test paketine eklenecek test olayını seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="2f776-369">Bu eğitici için, **Yeni bir ürün oluştur** test olayı seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="2f776-370">Sonra sayfanın sağ alt köşesindeki **Test olayları ekle**'yi seçin (Bu düğme aşağıdaki çizimde gösterilmez).</span><span class="sxs-lookup"><span data-stu-id="2f776-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Sorgu çalıştırma düğmesi](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="2f776-372">Test olayı **T01-Stoka Aktar** test paketine eklenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Test paketine eklenen test olayı](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="2f776-374">RSAT konfigüre et</span><span class="sxs-lookup"><span data-stu-id="2f776-374">Configure RSAT</span></span>

1. <span data-ttu-id="2f776-375">RSAT'ı açın.</span><span class="sxs-lookup"><span data-stu-id="2f776-375">Open RSAT.</span></span>

    ![RSAT simgesi](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="2f776-377">The Regression Suite Automation Tool'un Selenium gerektirdiğini, şimdi otomatik olarak karşıdan yükleyip kurmak isteyip istemediğinizi belirten bir uyarı iletisi mi alıyorsunuz?</span><span class="sxs-lookup"><span data-stu-id="2f776-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="2f776-378">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-378">Select **Yes**.</span></span>

    ![Uyarı iletisi](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="2f776-380">Sağ üst köşedeki **Ayarlar** düğmesini (çark sembolü) seçin ve sonra görünen iletişim kutusunda aşağıdaki alanları doldurun:</span><span class="sxs-lookup"><span data-stu-id="2f776-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="2f776-381">**Azure DevOps Url** – Azure DevOps projenizin `https://yourAzureDevOpsUrlHere.visualStudio.com` gibi URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="2f776-382">**Erişim Belirteci** – Aracın Azure DevOps'a bağlanmasını sağlayan erişim belirtecini girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="2f776-383">Bu öğreticide daha önce oluşturduğunuz kişisel erişim belirtecini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2f776-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="2f776-384">Daha fazla bilgi için bkz. [Kişisel erişim belirteçleriyle erişimi doğrulama](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="2f776-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="2f776-385">**Proje Adı** – Azure DevOps projenizin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="2f776-386">**Test planı** - Test olaylarınızı içeren Azure DevOps test planını seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="2f776-387">Daha fazla bilgi için bkz. [Test planları ve test paketleri oluşturma](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="2f776-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="2f776-388">Test planı seçtikten sonra Azure DevOps bağlantınızı test etmek için **test bağlantısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="2f776-389">**Ana bilgisayar adı** – Test ortamının ana bilgisayar adını **\<myaos\>.cloudax.dynamics.com** örneğindeki gibi girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="2f776-390">**https://** ya da **http://** öneki eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="2f776-391">**SOAP Ana bilgisayar Adı** – Test ortamının SOAP ana bilgisayar adını girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="2f776-392">Genellikle, SOAP ana bilgisayar adı ana bilgisayar adıyla aynıdır, ancak **soap** soneki vardır.</span><span class="sxs-lookup"><span data-stu-id="2f776-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="2f776-393">Örnek: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="2f776-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="2f776-394">**https://** ya da **http://** öneki eklemeyin.</span><span class="sxs-lookup"><span data-stu-id="2f776-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="2f776-395">Ana bilgisayar adını ve SOAP ana bilgisayar adını bulmak için, IIS Yöneticisini açın, **Siteler \> AOSService**'e sağ tıklayın **Bağlama düzenleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="2f776-396">**Ana bilgisayar adı** sütunundaki değerler, size ana bilgisayar adı ve SOAP ana bilgisayar adı verir (SOAP ana bilgisayar adı URL'de son ek **SOAP**'ye sahiptir).</span><span class="sxs-lookup"><span data-stu-id="2f776-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Ana makine adı sütununda ana bilgisayar adı ve SOAP ana bilgisayar adı](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="2f776-398">**Yönetici kullanıcı adı** – Test ortamında bir yönetici kullanıcısının e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="2f776-399">**Parmak izi** – Bu öğreticide daha önce anlatıldığı şekilde, kimlik doğrulama sertifikasının parmak izini girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="2f776-400">**Çalışma dizini** – Excel test veri dosyaları gibi test otomasyon dosyalarını depolamak için klasör konumunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="2f776-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="2f776-401">Örneğin, **C:\\Temp\\RegressionTool** girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="2f776-402">Klasörün adında boşluk varsa klasör bulunamadığı için yürütme işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="2f776-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="2f776-403">Bu sorun bilinen bir sorundur ve aracın en son sürümünde düzeltilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2f776-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="2f776-404">**Varsayılan tarayıcı** – ya **Internet Explorer** ya da **Google Chrome**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="2f776-405">Uygun tarayıcı sürücülerinin yüklenmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2f776-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="2f776-406">**Test çalıştırması zaman aşımı** – test çalıştırmaları için zaman aşımı süresini dakika cinsinden belirtin.</span><span class="sxs-lookup"><span data-stu-id="2f776-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="2f776-407">Zaman aşımı süresi geçtiğinde, tüm etkin pencereler kapatılır ve bekleyen test olayları başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="2f776-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="2f776-408">**Test eylemi zaman aşımı** – bu alan, Finance and Operations ortamı sunucu istekleri için zaman aşımı süresini dakika cinsinden denetler.</span><span class="sxs-lookup"><span data-stu-id="2f776-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="2f776-409">Genellikle varsayılan değer (2 dakika) yeterli olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2f776-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="2f776-410">Ancak, daha yavaş ortamlarda, zaman aşımları ile ilgili hatalar oluşursa bu değeri arttırmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="2f776-411">**Şirket adı** – Excel parametre dosyaları oluşturulurken varsayılan şirket olarak kullanılacak şirket adını girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="2f776-412">Şirketi daha sonra Excel parametre dosyasını düzenleyerek değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Ayarlar iletişim kutusu](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="2f776-414">Ayarlarınızı uygulamak ve kaydetmek için **Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="2f776-415">Geçerli ayarlarınızı bilgisayarınızdaki bir yapılandırma dosyasına kaydetmek için **Farklı kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="2f776-416">Geçerli ayarlarınızı bilgisayarınızdaki bir yapılandırma dosyasına geri yüklemek için **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="2f776-417">İletişim kutusunu kapatmak için **Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="2f776-418">Test çalışmalarını yükleme ve çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2f776-418">Load and run test cases</span></span>

1. <span data-ttu-id="2f776-419">Azure DevOps projesinden **RSAT Test Planı**'nı yüklemek için **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Yükle düğmesi](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="2f776-421">**Yeni bir ürün oluştur** test olayını test paketinden seçin ve sonra **Yeni \> Test Yürütmesi ve Parametresi dosyalarını oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Yeni menüde Test Yürütmesi ve Parametre Dosyaları oluştur komutu](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="2f776-423">Excel parametre dosyası, RSAT yapılandırmasında belirttiğiniz yerel klasörde oluşturulur. (örneğin **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="2f776-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Oluşturulan Excel parametre dosyası](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="2f776-425">Parametre dosyalarını kaydetmek istiyorsanız **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="2f776-426">Tüm seçili test olaylarının test otomasyon dosyaları, ileride kullanılmak üzere Azure DevOps'a yüklenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="2f776-427">(Bu dosyalar Excel test parametre dosyalarını içerir.)</span><span class="sxs-lookup"><span data-stu-id="2f776-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="2f776-428">Bu şekilde parametre dosyalarını (ve otomasyon dosyalarını) test olayından doğrudan Azure DevOps konumundan yüklemek için **Yükle**'yi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="2f776-429">Parametre dosyalarını yeniden oluşturmak zorunda değilsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="2f776-430">Değişiklikleri parametre dosyasında tutmak ve bunların üzerine yazılmasını istemiyorsanız bu yaklaşım daha sonra da önemli olacak.</span><span class="sxs-lookup"><span data-stu-id="2f776-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="2f776-431">Otomasyon dosyalarının ve Azure DevOps parametre dosyalarının kaydedildiğini doğrulamak için Azure DevOps projesine gidin,**Panolar \> İş Maddesi**'ni seçin ve **Yeni ürün oluştur** test olayını seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="2f776-432">**Ekler** sekmesinde dört dosya görmelisiniz:</span><span class="sxs-lookup"><span data-stu-id="2f776-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="2f776-433">**.cs** – C\# otomasyon dosyası</span><span class="sxs-lookup"><span data-stu-id="2f776-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="2f776-434">**. dll** – Derleme olarak derlenen otomasyon dosyası</span><span class="sxs-lookup"><span data-stu-id="2f776-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="2f776-435">**.xlsx** – Excel parametre dosyası</span><span class="sxs-lookup"><span data-stu-id="2f776-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="2f776-436">**.xml** – Kayıt dosyası</span><span class="sxs-lookup"><span data-stu-id="2f776-436">**.xml** – Recording file</span></span>

    ![Ekler sekmesindeki dosyalar](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="2f776-438">Çalıştırılacak test olayını seçin ve sonra **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-439">Test olaylarını çalıştırmadan önce tarayıcı olarak Internet Explorer kullanıyorsanız **Windows Görüntü Ayarları \> Ölçek ve Düzen**'in **%100** olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2f776-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="2f776-440">Bu ayarı bir sanal makinede (VM) değiştirmek istemezseniz VM'ye erişmeye çalıştığınız istemci (dizüstü bilgisayar) üzerinde bunu değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2f776-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="2f776-441">Böylece, çözünürlük ayarları VM görüntü ayarları tarafından devralınır.</span><span class="sxs-lookup"><span data-stu-id="2f776-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Masaüstü çözünürlüğü %100 olarak ayarlandı](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="2f776-443">Tarayıcı sürücüleri sistemde yüklü değilse "Bu işlem \<tarayıcı adı\> sürücüsü gerektirir.</span><span class="sxs-lookup"><span data-stu-id="2f776-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="2f776-444">Şimdi otomatik olarak karşıdan yükleyip kurmak istiyor musunuz?" uyarısı alacaksınız.</span><span class="sxs-lookup"><span data-stu-id="2f776-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="2f776-445">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-445">Select **Yes**.</span></span>

    ![Internet Explorer için uyarı iletisi](./media/setup_rsa_tool_69.png)

    ![Chrome için uyarı iletisi](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="2f776-448">Tarayıcı olarak Chrome kullanıyorsanız ve Chrome sürümü doğru olmadığı için oturumun oluşturulmadığını bildiren bir hata iletisi alıyorsanız en son Chrome sürücüsünü <http://chromedriver.chromium.org/downloads> **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Ortak\\Dış\\Selenium** dosyasına indirin.</span><span class="sxs-lookup"><span data-stu-id="2f776-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Chrome için hata uyarısı iletisi](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="2f776-450">Test olayı çalıştırılır ve **Sonuç** alanı güncellenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-450">The test case is run, and the **Result** field is updated.</span></span>

    ![İlerleme göstergesi](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="2f776-452">Bu öğreticiyi yazıldığı gibi izlediyseniz **Ürün oluşturmak için görev kaydı** ürün adını sabit kodlanmış değer olarak kaydetmediği için, yeni ürün test olayı oluşturma başarısız olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2f776-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="2f776-453">Aynı test olayını yeniden çalıştırırsanız ürün zaten varolduğu için bir hata iletisi almalısınız.</span><span class="sxs-lookup"><span data-stu-id="2f776-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Sonuç alanı Başarısız olarak ayarlandı](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="2f776-455">Test sonuçlarını görüntüleme</span><span class="sxs-lookup"><span data-stu-id="2f776-455">View the test results</span></span>

1. <span data-ttu-id="2f776-456">Başarısız test çalışmasına çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="2f776-457">Hata iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="2f776-457">You receive an error message.</span></span>

    ![Hata iletisi](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="2f776-459">Hata iletisinin tamamını görüntülemek için **Ayrıntıları** seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-459">Select **Details** to view the whole error message.</span></span>

    ![Tüm hata iletisi](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="2f776-461">Hata iletisinin ayrıntılı bir sürümünü Azure DevOps'ta görüntülemek için **Azure DevOps'da Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="2f776-462">Azure DevOps'ta, test olayının durumunu ve ayrıntılı hata iletisini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Azure DevOps'ta ayrıntılı hata iletisi](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="2f776-464">Azure DevOps test sonuçlarını doğrudan proje içinde görüntülemek için,**Test Planları \> Test Planları \> Çalıştır**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="2f776-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="2f776-465">Daha fazla ayrıntı görmek istediğiniz test olayına çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-465">Double-click the test run that you want to see more details for.</span></span>

    ![Azure DevOps'ta test çalışmalarının listesi](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="2f776-467">**Çalıştırma özeti** sekmesi test olayının başarısız olduğunu gösterir, ancak gerçek hata iletisini sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="2f776-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="2f776-468">Ayrıntılı hata iletisini görüntülemek için **Test sonuçları** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Çalıştırma özeti sekmesi](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="2f776-470">**Test sonuçları** sekmesi, sonuç ve hata iletisiyle birlikte test olayı bilgilerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2f776-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Test sonuçları sekmesi](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="2f776-472">Ayrıntılı hata iletisini görüntülemek için ilgili kayda çift tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Ayrıntılı hata iletisi](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="2f776-474">Tüm hata iletileri yerel olarak **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**'te de bulunur.</span><span class="sxs-lookup"><span data-stu-id="2f776-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="2f776-475">Test olayı sonuçlarını, **Dışa aktar**'ı seçerek test planı düzeyinden de dışa aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Test planını dışa aktarma](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="2f776-477">Excel parametre dosyasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="2f776-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="2f776-478">RSAT'ı açın.</span><span class="sxs-lookup"><span data-stu-id="2f776-478">Open RSAT.</span></span>
2. <span data-ttu-id="2f776-479">Test olayını seçin ve sonra Excel parametre dosyasını açmak için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="2f776-480">**EcoResProductCreate** tablosunda, **Ürün numarası** alanı değerinin sabit kodlanmış olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="2f776-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="2f776-481">Test olayını yeniden çalıştırmadan önce bu alanı yeni bir ürün numarasıyla güncelleştirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="2f776-482">Excel parametre dosyasını yeniden açmak ve her seferinde ürün numarasını el ile güncelleştirmek zorunda kalmadan her çalışma için benzersiz bir ürün numarası oluşturmak için aşağıdaki Excel formülünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="2f776-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="2f776-483">**Genel** sekmesine ek olarak the Excel parametre dosyası, test olayının ziyaretlerinin her form sayfası için bir veri sekmesi içerir.</span><span class="sxs-lookup"><span data-stu-id="2f776-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Ürün numarası dosyası](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="2f776-485">**Kaydet**'i seçip Excel .çalışma sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2f776-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="2f776-486">Excel parametre dosyasını Azure DevOps'a kaydetmek için **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![İleti yükleme başarılı](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="2f776-488">Test olaylarını belirli bir kullanıcı bağlamında çalıştırmak için, kullanıcının e-posta kodunu Excel parametre dosyasının **Genel** sekmesindeki **Test Kullanıcısı** alanına girin.</span><span class="sxs-lookup"><span data-stu-id="2f776-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="2f776-489">RSAT'ın en son sürümünde, Excel parametre dosyasındaki alanların düzeni güncelleştirildi, ancak kavram aynı kaldı.</span><span class="sxs-lookup"><span data-stu-id="2f776-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Test Kullanıcısı alanı](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="2f776-491">Sonuçları doğrulama</span><span class="sxs-lookup"><span data-stu-id="2f776-491">Validate the results</span></span>

- <span data-ttu-id="2f776-492">Test olayını yeniden çalıştırmak için **Çalıştır**'ı seçin ve test olayının geçtiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="2f776-493">Test sonuçlarını, [View the test results](#view-the-test-results)'ta tanımlandığı gibi görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Sonuç alanı Başarılı olarak ayarlandı](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="2f776-495">Test olaylarının zincirlenmesi</span><span class="sxs-lookup"><span data-stu-id="2f776-495">Chaining of test cases</span></span>

<span data-ttu-id="2f776-496">RSAT'ın en önemli özelliklerinden biri test olaylarının zincirlenmesidir (bir başka deyişle, bir testin diğer testlere geçiş yeteneği).</span><span class="sxs-lookup"><span data-stu-id="2f776-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="2f776-497">Test olayları, Azure DevOps test planındaki tanımlı sıralara göre çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="2f776-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="2f776-498">(Bu sıra test aracının kendisinde de güncelleştirilebilir.) Bu nedenle, değişkenleri bir test olayından diğerine geçirmek istiyorsanız testlerin doğru sırada olması çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="2f776-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="2f776-499">Bu bölümde, ilk test olayında bir kaydedilmiş değişken oluşturacak, ikinci bir test olayı yaratmayacak ve kaydedilmiş değişkeni ilk test olayından ikinci test olayına geçireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="2f776-500">Daha sonra test olaylarını RSAT'da zincirleme bir test olayı olarak çalıştırırsınız.</span><span class="sxs-lookup"><span data-stu-id="2f776-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="2f776-501">Kaydedilmiş bir değişken oluşturmak için varolan görev kaydını değiştirme</span><span class="sxs-lookup"><span data-stu-id="2f776-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="2f776-502">İstemciyi açın.</span><span class="sxs-lookup"><span data-stu-id="2f776-502">Open the client.</span></span>
2. <span data-ttu-id="2f776-503">**Ayarlar** düğmesini (çark simgesi) seçin ve sonra **Görev kaydedici**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="2f776-504">**Kaydı Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-504">Select **Edit Recording**.</span></span>

    ![Kaydı Düzenle düğmesi](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="2f776-506">**Lifecycle Services'tan Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-506">Select **Open from Lifecycle Services**.</span></span>

    ![Lifecycle Services'tan aç düğmesi](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="2f776-508">**Lifecycle Services kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Lifecycle Services kitaplığını seç düğmesi](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="2f776-510">BPM kitaplıkları LCS'den yüklenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-510">BPM libraries are loaded from LCS.</span></span>

    ![İlerleme göstergesi](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="2f776-512">BPM kitaplıkları LCS'den yüklendikten sonra **RSAT** BPM kitaplığını seçin ve görev kaydının ilişkilendirildiği **Yeni bir ürün oluştur** iş süreci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2f776-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="2f776-513">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-513">Then select **OK**.</span></span>

    ![BPM kitaplığı ve iş süreci seçme](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="2f776-515">Uygun görev kaydının adı **Kayıt adı** alanına girilir.</span><span class="sxs-lookup"><span data-stu-id="2f776-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="2f776-516">**Başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-516">Select **Start**.</span></span>

    ![Kayıt adı alanına görev kaydı için benzersiz bir ad girin.](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="2f776-518">**Ürün bilgileri yönetimi \> Ürünler**'e gidin ve **Ürün oluştur**'un kaydedildiği orijinal görev kaydetmede **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="2f776-519">**Adım ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-520">Yeni adım, bölmesinde seçtiğiniz adımdan **sonra** eklenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Adım ekle düğmesi](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="2f776-522">**Ürün numarası** alanına sağ tıklayın ve sonra **Görev kaydedici \> Kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Komutu kopyalama](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="2f776-524">Yeni adım bölmeye eklenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-524">A new step is added in the pane.</span></span> <span data-ttu-id="2f776-525">Daha sonra gereksinim duyacağınız **Ürün numarası** alanındaki değeri not edin.</span><span class="sxs-lookup"><span data-stu-id="2f776-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Yeni adım eklendi](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="2f776-527">**Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="2f776-528"> **Save to Lifecycle Services**'e kaydeti seçin ve yeni görev kaydını, özgün görev kaydının ilişkilendirildiği aynı BPM kitaplığıyla ve iş süreciyle ilişkilendirin.</span><span class="sxs-lookup"><span data-stu-id="2f776-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="2f776-529">Daha fazla bilgi için [Görev kaydı oluşturma ve bunu BPM kitaplığına kaydetme](#create-a-task-recording-and-save-it-to-the-bpm-library)bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="2f776-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="2f776-530">BPM kitaplığına gidin ve **Test olaylarını eşitle**'yi [BPM ile Azure DevOps eşitlemesini test etme](#test-the-synchronization-from-bpm-to-azure-devops) bölümünde açıklandığı gibi Azure DevOps'a iliştirin.</span><span class="sxs-lookup"><span data-stu-id="2f776-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="2f776-531">RSAT'ı açın ve test paketindeki tüm test olaylarını yeniden yüklemek için **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="2f776-532">Test olayını seçerek ve [Test olaylarını yükleme ve çalıştırma](#load-and-run-test-cases) bölümünde açıklandığı gibi **Yeni \> Test Yürütme ve Parametre dosyaları**'nı seçerek uygun test olayı için otomasyon ve parametre dosyalarını yeniden oluşturmalısınız.</span><span class="sxs-lookup"><span data-stu-id="2f776-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-533">Excel parametre dosyası açık bırakılırsa yeniden oluşturma işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="2f776-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="2f776-534">Bu nedenle, yeni Excel parametre dosyasını oluşturmadan önce test olayı için Excel parametre dosyasının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2f776-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="2f776-535">Yeni Excel parametre dosyasını açmak için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="2f776-536">Çevrimiçi 9 yeni bir **Kaydedilmiş değişken** girişi göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="2f776-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="2f776-537">Bu değişken **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, görev kaydının XML dosyasına kaydedilir ve sonraki testlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2f776-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Kaydedilen değişken girişi](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="2f776-539">Yeni bir test olayı oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f776-539">Create a new test case</span></span>

1. <span data-ttu-id="2f776-540">**RSAT** BPM kitaplığına gidin.</span><span class="sxs-lookup"><span data-stu-id="2f776-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="2f776-541">**Örnek Desteği İş Süreci** sürecini seçin ve sağ taraftaki **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="2f776-542">Hem **Ad** alanını hem de **Açıklama** alanını **Ürünü serbest bırak** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2f776-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="2f776-543">Sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-543">Then select **Save**.</span></span>

    ![Ad ve açıklama bir ürünü serbest bırakmak için değişti](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="2f776-545">Doğrulama işlevi olan yeni bir görev kaydı oluşturma</span><span class="sxs-lookup"><span data-stu-id="2f776-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="2f776-546">Daha önce USRT tüzel kişiliği tarafından oluşturulan ürünü serbest bırakmak için bir görev kaydı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2f776-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="2f776-547">Daha fazla bilgi için [Görev kaydı oluşturma ve bunu BPM kitaplığına kaydetme](#create-a-task-recording-and-save-it-to-the-bpm-library)bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="2f776-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2f776-548">Zincirleme test olayları için, *alan değerini el ile yazarak* gereksinim duyduğunuz kaydı bulmanız veya filtreleyerek her zaman önerilir.</span><span class="sxs-lookup"><span data-stu-id="2f776-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="2f776-549">Bu şekilde, söz konusu eylem, sonraki test olayında dikkate alınması gereken kaydı belirleyebilir.</span><span class="sxs-lookup"><span data-stu-id="2f776-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Doğrulama işlevi olan yeni bir görev kaydı](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="2f776-551">Yukarıdaki resimde gösterildiği gibi ürün Quick Filter'la bulunduktan sonra ancak **Ürünleri serbest bırak**'ı seçmeden önce, **Ürün numarası** alanının değerini doğrulamak için ürün kimliğinin daha önce oluşturulmuş ürün kimliği olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2f776-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="2f776-552">Değeri doğrulamak için **ürün numarası** alanına sağ tıklayın ve **Görev kaydedici \> Doğrula \> Geçerli Değer**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Geçerli kaydı doğrulama](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="2f776-554">Görev kaydetmeyi BPM'e kaydetme</span><span class="sxs-lookup"><span data-stu-id="2f776-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="2f776-555">Görev kaydı tamamlandıktan sonra **Lifecycle Services'e kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Kaydetme seçenekleri](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="2f776-557">Kitaplık bilgileri LCS'den yüklenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-557">Library information is loaded from LCS.</span></span>

    ![İlerleme göstergesi](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="2f776-559">Görev kaydını ilişkilendirmek için BPM kitaplığını seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="2f776-560">Bu öğretici için, yukarıda oluşturulmuş **RSAT** BPM kitaplığını seçin ve altında **Ürünü serbest bırakma** iş sürecini seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="2f776-561">Daha sonra **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="2f776-562">BPM'i Azure DevOps ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="2f776-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="2f776-563">BPM kitaplığına gidin ve **RSAT** kitaplığını açın.</span><span class="sxs-lookup"><span data-stu-id="2f776-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="2f776-564">**VSTS eşitleme**'yi seçin ve sonra **Test olaylarını eşitle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="2f776-565">Daha fazla bilgi için [BPM ile Azure DevOps eşitlemesini test etme](#test-the-synchronization-from-bpm-to-azure-devops) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="2f776-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="2f776-566">Eşitleme tamamlandıktan sonra yeni iş maddesi ve **Bir ürünü serbest bırakma**'ya karşılık gelen test olayı **Panolar \> İş Maddeleri**'ndeki .Azure DevOps'da görünür</span><span class="sxs-lookup"><span data-stu-id="2f776-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="2f776-567">Varolan test paketine yeni test çalışmasını ekleme</span><span class="sxs-lookup"><span data-stu-id="2f776-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="2f776-568">**Test planları \> Test planları**'na gidin ve **RSAT Test Planı** planını seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="2f776-569">**Varolanı ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="2f776-570">**Test olaylarını pakete ekle** sayfasında **Sorguyu çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="2f776-571">**Bir ürünü serbest bırakmak** için oluşturulan yeni test olayını seçin ve sonra sayfanın sağ alt köşesinde **Test olayları ekle**'yi seçin (Bu düğme aşağıdaki çizimde gösterilmez).</span><span class="sxs-lookup"><span data-stu-id="2f776-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Paket sayfasına test durumları ekleme](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="2f776-573">Test paketinin şimdi iki test olayı vardır.</span><span class="sxs-lookup"><span data-stu-id="2f776-573">The test suite now has two test cases.</span></span>

    ![Test paketinin şimdi iki test olayı var](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="2f776-575">RSAT'a test olaylarını yükleme</span><span class="sxs-lookup"><span data-stu-id="2f776-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="2f776-576">RSAT'ı açın ve **Yükle**yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="2f776-577">Test olayları yüklenir ve "Bu eylem Excel test veri dosyalarının üzerine yazacak, yerel değişikliklerin kaybolmasına neden olacak.</span><span class="sxs-lookup"><span data-stu-id="2f776-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="2f776-578">Devam etmek istiyor musunuz?" yazan bir uyarı alacaksınız</span><span class="sxs-lookup"><span data-stu-id="2f776-578">Do you want to proceed?"</span></span> <span data-ttu-id="2f776-579">Excel parametresi dosyalarını yerel sistemde güncelleştirmek ama Azure DevOps'a yüklenen Excel parametre dosyalarını güncelleştirmemek için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Uyarı iletisi](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="2f776-581">Her iki test olayı da, ilk test olayı için Excel parametre dosyası ile birlikte yüklenir.</span><span class="sxs-lookup"><span data-stu-id="2f776-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="2f776-582">Son çalıştırmada karşıya **Yükle**'yi seçtiğinizden, parametre dosyaları Azure DevOps'tan çekilir .</span><span class="sxs-lookup"><span data-stu-id="2f776-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Test senaryoları yüklendi](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="2f776-584">Yalnızca ikinci test olayını seçin ve sonra  **Yeni \> Test Yürütmesi ve Parametre Dosyaları oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="2f776-585">Excel parametre dosyasını düzenleme</span><span class="sxs-lookup"><span data-stu-id="2f776-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="2f776-586">Yalnızca ikinci test olayını seçin ve sonra karşılık gelen Excel parametre dosyasını açmak için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="2f776-587">Kaydedilmiş değişken **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**'yi ilk test olayından ürün numarasının kullanıldığı tüm alanlara kopyalayın ([Kaydedilmiş bir değişken oluşturmak için varolan görev kaydını değiştirme](#modify-an-existing-task-recording-to-create-a-saved-variable) bölümüne bakın).</span><span class="sxs-lookup"><span data-stu-id="2f776-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="2f776-588">Bu durumda, değişkeni **Ürün numarasına** ve **Ürün Numarasını Doğrula** alanlarını **EcoResProductListPage** sayfasına kopyalarsınız.</span><span class="sxs-lookup"><span data-stu-id="2f776-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Ürün numarası ve ürün numarası doğrulama alanları](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="2f776-590">Değişkenler, yalnızca aynı test olayı sırasında testler arasında geçirilebilir.</span><span class="sxs-lookup"><span data-stu-id="2f776-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="2f776-591">Değişkenlerin adlarının tam olarak eşleşmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f776-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="2f776-592">**Kaydet**'i seçip Excel .çalışma sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="2f776-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="2f776-593">Excel parametre dosyasında yaptığınız değişiklikleri kaydetmek için **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="2f776-594">Zincirleme test olaylarını çalıştırma</span><span class="sxs-lookup"><span data-stu-id="2f776-594">Run the chained test cases</span></span>

1. <span data-ttu-id="2f776-595">Çalıştırılacak iki test olayını da seçin ve sonra **Çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f776-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="2f776-596">Her iki test olayının da geçtiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="2f776-596">Verify that both test cases have passed.</span></span>

    ![Her iki test çalışması için de sonuç alanı geçildi](./media/setup_rsa_tool_105.png)
