---
title: "Bir veritabanını geri yükledikten sonra mali raporlama veri reyonunu sıfırlama"
description: "Bu konu Microsoft Dynamics 365 for Finance and Operations veritabanını geri yüklendikten sonra mali raporlama veri reyonunun nasıl sıfırlanacağını açıklar."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: tr-tr
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="21454-103">Bir veritabanını geri yükledikten sonra mali raporlama veri reyonunu sıfırlama</span><span class="sxs-lookup"><span data-stu-id="21454-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="21454-104">Bu konu Microsoft Dynamics 365 for Finance and Operations veritabanını geri yüklendikten sonra mali raporlama veri reyonunun nasıl sıfırlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="21454-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="21454-105">Finance and Operations veritabanınızı bir yedekten kurtarırsanız veya veritabanını bir ortamdan diğerine kopyalarsanız, mali raporlama verisinin mart'ın Finance and Operations veritabanını doğru kullandığından emin olmak için bu konudaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="21454-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="21454-106">Bu işlemdeki adımların Dynamics 365 for Operation Mayıs 2016 sürümü (Uygulama yapısı 7.0.1265.23014 ve mali raporlama yapısı 7.0.10000.4) ve daha yeni sürümler için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="21454-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="21454-107">Finance and Operations'ın önceki bir sürümüne sahipseniz, yardım için Destek ekibimize başvurun.</span><span class="sxs-lookup"><span data-stu-id="21454-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="21454-108">Rapor tanımlarını dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="21454-108">Export report definitions</span></span>
<span data-ttu-id="21454-109">İlk olarak, Rapor Tasarımcısı'nda bulunan rapor tasarımlarını aşağıdaki adımları uygulayarak dışa aktarın:</span><span class="sxs-lookup"><span data-stu-id="21454-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="21454-110">Rapor Tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="21454-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="21454-111">Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21454-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="21454-112">Finance and Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.</span><span class="sxs-lookup"><span data-stu-id="21454-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="21454-113">Dışa aktarılacak rapor tanımlarını seçin:</span><span class="sxs-lookup"><span data-stu-id="21454-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="21454-114">Tüm rapor tanımlarını ve ilgili yapı taşlarını dışa aktarmak için **Tümünü Seç** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21454-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="21454-115">Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini dışa aktarmak için ilgili sekmeye tıklayın ve ardından dışa aktarılacak maddeleri seçin.</span><span class="sxs-lookup"><span data-stu-id="21454-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="21454-116">Bir sekmede birden fazla madde seçmek için CTRL tuşunu basılı tutun.</span><span class="sxs-lookup"><span data-stu-id="21454-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="21454-117">Dışa aktarılacak raporları seçtiğinizde ilişkili satırlar, sütunlar, ağaçlar ve boyut kümeleri seçilir.</span><span class="sxs-lookup"><span data-stu-id="21454-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="21454-118">**Dışa Aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21454-118">Click **Export**.</span></span>
5.  <span data-ttu-id="21454-119">Bir dosya adı girin ve dışarı aktarılan rapor tanımlarını kaydetmek için istediğiniz güvenli bir konumu seçin.</span><span class="sxs-lookup"><span data-stu-id="21454-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="21454-120">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21454-120">Click **Save**.</span></span>

<span data-ttu-id="21454-121">Dosya güvenli bir konuma kopyalanabilir veya yüklenebilir; bu dosyanın daha sonra farklı bir ortama aktarılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="21454-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="21454-122">Microsoft Azure depolama hesabı kullanma hakkındaki bilgileri [>AzCopy Komut Satırı Yardımcı Programı ile veri transferi](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy) bölümünde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21454-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="21454-123">Microsoft, Finance and Operations sözleşmenizin bir parçası olarak bir depolama hesabı sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="21454-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="21454-124">Bir depolama hesabı satın almanız veya ayrı bir Azure aboneliğine ait bir depolama hesabını kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="21454-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="21454-125">Azure Sanal Makineler'de D sürücüsünün davranışını dikkate alın.</span><span class="sxs-lookup"><span data-stu-id="21454-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="21454-126">Dışa aktarılan yapı taşı gruplarınızı burada kalıcı olarak saklamayın.</span><span class="sxs-lookup"><span data-stu-id="21454-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="21454-127">Geçici sürücüler hakkında daha fazla bilgi için bkz. [Microsoft Azure Sanal Makinelerindeki geçici sürücüyü anlama](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="21454-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="21454-128">Hizmetleri durdurma</span><span class="sxs-lookup"><span data-stu-id="21454-128">Stop services</span></span>
<span data-ttu-id="21454-129">Ortamdaki tüm bilgisayarlara bağlanmak ve services.msc'yi kullanarak aşağıdaki Windows hizmetlerini durdurmak için Uzak Masaüstü'nü kullanın:</span><span class="sxs-lookup"><span data-stu-id="21454-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="21454-130">World wide web publishing service (tüm AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="21454-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="21454-131">Microsoft Dynamics 365 for Finance and Operations Toplu İŞ Yönetimi Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="21454-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="21454-132">Management Reporter 2012 İşlem Hizmeti (yalnızca BI bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="21454-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="21454-133">Bu hizmetlerin Finance and Operations veritabanına açık bağlantıları olacaktır.</span><span class="sxs-lookup"><span data-stu-id="21454-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="21454-134">Sıfırla</span><span class="sxs-lookup"><span data-stu-id="21454-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="21454-135">En güncel MinorVersionDataUpgrade.zip paketini bulun ve indirin.</span><span class="sxs-lookup"><span data-stu-id="21454-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="21454-136">[MinorVersionDataUpgrade.zip komut dosyasını indirme](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package) konusundaki yönergeleri kullanarak en son MinorVersionDataUpgrade.zip paketini bulun.</span><span class="sxs-lookup"><span data-stu-id="21454-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="21454-137">Yönergeler veri yükseltme paketinin doğru sürümünü nasıl bulacağınızı ve indireceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="21454-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="21454-138">MinorVersionDataUpgrade.zip paketini indirmek için bir güncelleştirme gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="21454-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="21454-139">"En son veri yükseltme dağıtılabilir paketini karşıdan yükleme" bölümündeki adımları MinorVersionDataUpgrade.zip paketinin bir kopyasını almak için makalesinde yapmadan diğer adımları tamamlamak yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="21454-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="21454-140">Finance and Operations veritabanı için komut dosyalarını çalıştırma</span><span class="sxs-lookup"><span data-stu-id="21454-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="21454-141">Aşağıdaki komut dosyalarını Finance and Operations veritabanı için çalıştırın (finansal raporlama veritabanı için değil).</span><span class="sxs-lookup"><span data-stu-id="21454-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="21454-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="21454-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="21454-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="21454-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="21454-144">Bu komut dosyaları kullanıcıların, rollerin ve değişiklik izleme ayarlarının doğru olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="21454-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="21454-145">Veritabanını sıfırlamak için PowerShell komutunu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="21454-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="21454-146">Finance and Operations ve mali raporlama tümleştirmesini sıfırlamak için doğrudan AOS bilgisayarındaki aşağıdaki komutu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="21454-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="21454-147">Windows PowerShell'i Yönetici olarak açın.</span><span class="sxs-lookup"><span data-stu-id="21454-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="21454-148">Execute: F:</span><span class="sxs-lookup"><span data-stu-id="21454-148">Execute: F:</span></span>
3.  <span data-ttu-id="21454-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="21454-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="21454-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="21454-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="21454-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span><span class="sxs-lookup"><span data-stu-id="21454-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="21454-152">Onaylamak için "Y" girmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="21454-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="21454-153">Parametre açıklaması:</span><span class="sxs-lookup"><span data-stu-id="21454-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="21454-154">Neden - için geçerli değerler şunlardır: SERVICING, BADDATA, OTHER</span><span class="sxs-lookup"><span data-stu-id="21454-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="21454-155">ReasonDetail parametresi serbest metindir.</span><span class="sxs-lookup"><span data-stu-id="21454-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="21454-156">Neden ve reasonDetail telemetri/ortam izlemede kaydedilecektir.</span><span class="sxs-lookup"><span data-stu-id="21454-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="21454-157">Hizmetleri başlatma</span><span class="sxs-lookup"><span data-stu-id="21454-157">Start services</span></span>
<span data-ttu-id="21454-158">Daha önce durdurduğunuz hizmetleri yeniden başlatmak için services.msc'yi kullanın:</span><span class="sxs-lookup"><span data-stu-id="21454-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="21454-159">World wide web publishing service (tüm AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="21454-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="21454-160">Microsoft Dynamics 365 for Finance and Operations Toplu İŞ Yönetimi Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="21454-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="21454-161">Management Reporter 2012 İşlem Hizmeti (yalnızca BI bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="21454-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="21454-162">Rapor tanımlarını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="21454-162">Import report definitions</span></span>
<span data-ttu-id="21454-163">Rapor Tasarımcısı'ndan rapor tanımlarınızı dışa aktarma sırasında oluşturulan dosyayı kullanarak içe aktarın:</span><span class="sxs-lookup"><span data-stu-id="21454-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="21454-164">Rapor Tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="21454-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="21454-165">Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21454-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="21454-166">Finance and Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.</span><span class="sxs-lookup"><span data-stu-id="21454-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="21454-167">**Varsayılan** yapı bloğunu seçin ve **İçe Aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21454-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="21454-168">Dışa aktarılan rapor tanımlarını içeren dosyayı seçin **Aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21454-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="21454-169">İçe Aktar iletişim kutusunda, içe aktarılacak rapor tanımlarını seçin:</span><span class="sxs-lookup"><span data-stu-id="21454-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="21454-170">Rapor tanımlarının ve destekleyici yapı taşlarının tümünü içe aktarmak için **Tümünü Seç** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21454-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="21454-171">Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini içe aktarmak için, içe aktarılacak raporları, satırları, sütunları, ağaçları veya boyut kümelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="21454-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="21454-172">**İçe aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="21454-172">Click **Import**.</span></span>





