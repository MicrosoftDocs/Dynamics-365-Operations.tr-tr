---
title: Genel sorun giderme
description: Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında genel sorun giderme bilgileri sağlar.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 6356ec6850667f32f9e9e4133686c40f0b6d76d7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688271"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="41e25-103">Genel sorun giderme</span><span class="sxs-lookup"><span data-stu-id="41e25-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="41e25-104">Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında genel sorun giderme bilgileri sağlar.</span><span class="sxs-lookup"><span data-stu-id="41e25-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41e25-105">Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="41e25-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="41e25-106">Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="41e25-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="41e25-107">İkili yazma paketini paket dağıtıcı aracını kullanarak yüklemeye çalıştığınızda, kullanılabilir çözüm gösterilmemiştir</span><span class="sxs-lookup"><span data-stu-id="41e25-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="41e25-108">Paket Dağıtıcı aracının bazı sürümleri çift yazma çözüm paketiyle uyumsuz.</span><span class="sxs-lookup"><span data-stu-id="41e25-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="41e25-109">Paketi başarılı bir şekilde yüklemek için, paket dağıtıcı aracının [sürüm 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) veya üstünü kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="41e25-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="41e25-110">Package Deployer aracını yükledikten sonra, aşağıdaki adımları izleyerek çözüm paketini yükleyin.</span><span class="sxs-lookup"><span data-stu-id="41e25-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="41e25-111">Yammer.Com ' dan en son çözüm paketi dosyasını karşıdan yükle.</span><span class="sxs-lookup"><span data-stu-id="41e25-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="41e25-112">Paket ZIP dosyası karşıdan yüklendikten sonra sağ tıklatın ve **Özellikler** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="41e25-113">**Engeli kaldır** onay kutusunu seçin ve **Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="41e25-114">**Engellemeyi kaldır** onay kutusunu görmüyorsanız, zip dosyasının engeli zaten kaldırılır ve bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41e25-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Özellikler iletişim kutusu](media/unblock_option.png)

2. <span data-ttu-id="41e25-116">Paket ZIP dosyasını ayıklayın ve **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** klasöründeki tüm dosyaları kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="41e25-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438 klasörü içeirği](media/extract_package.png)

3. <span data-ttu-id="41e25-118">Kopyalanan tüm dosyaları, Paket Dağıtıcı aracı'nın **Araçlar** klasörüne yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="41e25-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="41e25-119">Dataverse Ortamı seçmek ve çözümleri yüklemek için **PackageDeployer. exe** dosyasını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="41e25-119">Run **PackageDeployer.exe** to select the Dataverse environment and install the solutions.</span></span>

    ![Araçlar klasörünün içeriği](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a><span data-ttu-id="41e25-121">Hata ayrıntılarını görmek için Dataverse'te eklenti izleme günlüğünü etkinleştirme ve görüntüleme</span><span class="sxs-lookup"><span data-stu-id="41e25-121">Enable and view the plug-in trace log in Dataverse to view error details</span></span>

<span data-ttu-id="41e25-122">**İzleme günlüğünü açmak ve hataları görüntülemek için gerekli rol:** Sistem Yöneticisi</span><span class="sxs-lookup"><span data-stu-id="41e25-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="41e25-123">İz günlüğünü açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="41e25-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="41e25-124">Dynamics 365'teki model yönetimli uygulamada oturum açın, **Ayarlar** sayfasını açın ve sonra **Sistem** altında **Yönetim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-124">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="41e25-125">**Yönetim** sayfasında **Sistem Ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="41e25-126">**Özelleştirme** sekmesinde, eklenti ve **özel iş akışı faaliyet izleme** alanında, eklenti izleme günlüğünü etkinleştirmek için **tümü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="41e25-127">Yalnızca özel durumlar gerçekleştiğinde izleme günlüklerini günlüğe kaydetmek istiyorsanız, bunun yerine **özel durum** seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41e25-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="41e25-128">İz günlüğünü açmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="41e25-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="41e25-129">Dynamics 365'teki model yönetimli uygulamada oturum açın, **Ayarlar** sayfasını açın ve sonra **Özelleştirme** altında **Eklenti İzleme Günlüğü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-129">Sign in to the model-driven app in Dynamics 365, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="41e25-130">**Tür Adı** alanının **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin** olarak ayarlandığı izleme günlüklerini bulun.</span><span class="sxs-lookup"><span data-stu-id="41e25-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.</span></span>
3. <span data-ttu-id="41e25-131">Tam günlüğü görüntülemek için bir öğeyi çift tıklatın ve sonra **yürütme** hızlı sekmesinde **ileti öbeği** metnini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="41e25-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="41e25-132">Finance and Operations Uygulamalardaki canlı eşitleme sorunlarını gidermek için hata ayıklama modunu etkinleştir</span><span class="sxs-lookup"><span data-stu-id="41e25-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="41e25-133">**Hataları görüntülemek için gerekli olan rol:** Dataverse uygulamasında yer alan sistem yöneticisi Çift yazma hataları Finance and Operations uygulamasında görünebilir.</span><span class="sxs-lookup"><span data-stu-id="41e25-133">**Required role to view the errors:** System admin Dual-write errors that originate in Dataverse can appear in the Finance and Operations app.</span></span> <span data-ttu-id="41e25-134">Bazı durumlarda, ileti çok uzun veya kişisel tanımlayıcı bilgiler (PII) içerdiğinden hata iletisinin tam metni kullanılamıyor.</span><span class="sxs-lookup"><span data-stu-id="41e25-134">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="41e25-135">Hata için ayrıntılı günlüğü, aşağıdaki adımları izleyerek açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41e25-135">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="41e25-136">Finance and Operations Uygulamalardaki tüm proje yapılandırmalarında **dualwriteprojectconfiguration** varlığında bir **ısdebugmode** özelliği vardır.</span><span class="sxs-lookup"><span data-stu-id="41e25-136">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="41e25-137">**DualWriteProjectConfiguration** varlığını Excel eklentisini kullanarak açın.</span><span class="sxs-lookup"><span data-stu-id="41e25-137">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="41e25-138">Varlığı açmanın kolay bir yolu, Excel eklentilerinde **tasarım** modunu etkinleştirmek ve sonra da çalışma sayfasına **dualwriteprojectconfigurationentity** öğesini eklemektir.</span><span class="sxs-lookup"><span data-stu-id="41e25-138">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="41e25-139">Daha fazla bilgi için bkz. [Varlık verilerini Excel'de açma ve Excel eklentisini kullanarak güncelleştirme](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="41e25-139">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="41e25-140">**Isdebugmode** özelliğini proje için **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="41e25-140">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="41e25-141">Hata oluşturan senaryoyu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="41e25-141">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="41e25-142">Ayrıntılı Günlükler DualWriteErrorLog tablosunda bulunur.</span><span class="sxs-lookup"><span data-stu-id="41e25-142">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="41e25-143">Verileri tablo tarayıcısında aramak için aşağıdaki URL 'yi kullanın (**xxx**'yi uygun şekilde değiştirin):</span><span class="sxs-lookup"><span data-stu-id="41e25-143">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="41e25-144">Finance and Operations Uygulamaya ilişkin sanal makinedeki eşitleme hatalarını denetle</span><span class="sxs-lookup"><span data-stu-id="41e25-144">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="41e25-145">**Hataları görüntülemek için gerekli rol:** Sistem yöneticisi</span><span class="sxs-lookup"><span data-stu-id="41e25-145">**Required role to view the errors:** System administrator</span></span>

1. <span data-ttu-id="41e25-146">Microsoft Dynamics Lifecycle Services (LCS)'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="41e25-146">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="41e25-147">Çift yazma sınaması gerçekleştirmek için seçtiğiniz LCS projesini açın.</span><span class="sxs-lookup"><span data-stu-id="41e25-147">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="41e25-148">**Bulutta barındırılan ortamlar** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-148">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="41e25-149">Finance and Operations Uygulamanın sanal makinesine (VM) oturum açmak Için uzak masaüstü 'nü kullanın.</span><span class="sxs-lookup"><span data-stu-id="41e25-149">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="41e25-150">LCS içinde gösterilen yerel hesabı kullanın.</span><span class="sxs-lookup"><span data-stu-id="41e25-150">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="41e25-151">Olay Görüntüleyiciyi açın.</span><span class="sxs-lookup"><span data-stu-id="41e25-151">Open Event viewer.</span></span>
6. <span data-ttu-id="41e25-152">**Uygulamalar ve Hizmetler günlükleri \> Microsoft \> Dynamics \> AX-DualWriteSync \> İşletim**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="41e25-152">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="41e25-153">En son hataların listesini gözden geçirin.</span><span class="sxs-lookup"><span data-stu-id="41e25-153">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="41e25-154">Bir Finance and Operations uygulamadan başka bir Dataverse ortam bağlantısını kaldır ve bağlantıyı kes</span><span class="sxs-lookup"><span data-stu-id="41e25-154">Unlink and link another Dataverse environment from a Finance and Operations app</span></span>

<span data-ttu-id="41e25-155">**Ortamın bağlantısını kaldırmak için gerekli rol:** Finance and Operations veya Dataverse uygulaması için sistem yöneticisi.</span><span class="sxs-lookup"><span data-stu-id="41e25-155">**Required role to unlink the environment:** System administrator for either Finance and Operations app or Dataverse.</span></span>

1. <span data-ttu-id="41e25-156">Finance and Operations Uygulamaya oturum açın.</span><span class="sxs-lookup"><span data-stu-id="41e25-156">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="41e25-157">**Çalışma alanları \> veri yönetimi**'ne gidin ve **ikili yazma** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-157">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="41e25-158">Çalışan tüm eşlemeleri seçin ve **Durdur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="41e25-158">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="41e25-159">**Ortam bağlantısını kaldırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-159">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="41e25-160">Operasyonu onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="41e25-160">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="41e25-161">Şimdi yeni bir ortam bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="41e25-161">You can now link a new environment.</span></span>

## <a name="unable-to-view-the-sales-order-line-information-form"></a><span data-ttu-id="41e25-162">Satış siparişi satırı Bilgi formu görüntülenemiyor</span><span class="sxs-lookup"><span data-stu-id="41e25-162">Unable to view the sales order line Information form</span></span> 

<span data-ttu-id="41e25-163">Dynamics 365 Sales içinde bir satış siparişi oluşturduğunuzda, **+ Ürün ekle**'ye tıklamak, sizi Dynamics 365 Project Operations sipariş satırı formuna yönlendirebilir.</span><span class="sxs-lookup"><span data-stu-id="41e25-163">When you create a sales order in Dynamics 365 Sales, clicking on **+ Add products** might redirect you to the Dynamics 365 Project Operations order line form.</span></span> <span data-ttu-id="41e25-164">Satış siparişi satırı **Bilgi** formunu görüntülemek için bu formdan bir yol yoktur.</span><span class="sxs-lookup"><span data-stu-id="41e25-164">There is no way from that form to view the sales order line **Information** form.</span></span> <span data-ttu-id="41e25-165">**Bilgi** seçeneği, **Yeni Sipariş Satırı** altındaki açılan listede görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="41e25-165">The option for **Information** does not appear in the dropdown below **New Order Line**.</span></span> <span data-ttu-id="41e25-166">Bunun nedeni, Project Operations'ın ortamınıza yüklenmiş olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="41e25-166">This happens because Project Operations has been installed in your environment.</span></span>

<span data-ttu-id="41e25-167">**Bilgi** formu seçeneğini yeniden etkinleştirmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="41e25-167">To re-enable the **Information** form option, follow these steps:</span></span>
1. <span data-ttu-id="41e25-168">**Sipariş satırı** varlığına gidin.</span><span class="sxs-lookup"><span data-stu-id="41e25-168">Navigate to the **Order Line** entity.</span></span>
2. <span data-ttu-id="41e25-169">Formlar düğümünün altından **Bilgi** formunu bulun.</span><span class="sxs-lookup"><span data-stu-id="41e25-169">Find the **Information** form under the forms node.</span></span> 
3. <span data-ttu-id="41e25-170">**Bilgi** formunu seçin ve **Güvenlik rollerini etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="41e25-170">Select the **Information** form and click **Enable security roles**.</span></span> 
4. <span data-ttu-id="41e25-171">Güvenlik ayarını **Herkese göster** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="41e25-171">Change the security setting to **Display to everyone**.</span></span>
