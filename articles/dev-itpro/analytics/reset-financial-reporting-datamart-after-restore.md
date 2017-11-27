---
title: "Bir veritabanını geri yükledikten sonra mali raporlama veri reyonunu sıfırlama"
description: "Bu konu Microsoft Dynamics 365 for Finance and Operations veritabanını geri yüklendikten sonra mali raporlama veri reyonunun nasıl sıfırlanacağını açıklar."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e3f78fb2f6528449d2a411225cd0e14ca33443e
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="e5df4-103">Bir veritabanını geri yükledikten sonra mali raporlama veri reyonunu sıfırlama</span><span class="sxs-lookup"><span data-stu-id="e5df4-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e5df4-104">Bu konu Microsoft Dynamics 365 for Finance and Operations veritabanını geri yüklendikten sonra mali raporlama veri reyonunun nasıl sıfırlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="e5df4-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="e5df4-105">Finance and Operations veritabanınızı bir yedekten kurtarırsanız veya veritabanını bir ortamdan diğerine kopyalarsanız, mali raporlama verisinin mart'ın Finance and Operations veritabanını doğru kullandığından emin olmak için bu konudaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e5df4-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
> [!Note] 
> <span data-ttu-id="e5df4-106">Bu işlemdeki adımların Dynamics 365 for Operation Mayıs 2016 sürümü (Uygulama yapısı 7.0.1265.23014 ve mali raporlama yapısı 7.0.10000.4) ve daha yeni sürümler için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="e5df4-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="e5df4-107">Finance and Operations'ın önceki bir sürümüne sahipseniz, yardım için Destek ekibimize başvurun.</span><span class="sxs-lookup"><span data-stu-id="e5df4-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="e5df4-108">Rapor tanımlarını dışa aktarma</span><span class="sxs-lookup"><span data-stu-id="e5df4-108">Export report definitions</span></span>
<span data-ttu-id="e5df4-109">İlk olarak, Rapor Tasarımcısı'nda bulunan rapor tasarımlarını aşağıdaki adımları uygulayarak dışa aktarın:</span><span class="sxs-lookup"><span data-stu-id="e5df4-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="e5df4-110">Rapor Tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e5df4-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="e5df4-111">Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-111">Select the building block group to export, and click **Export**.</span></span> 

    > [!Note] 
    > <span data-ttu-id="e5df4-112">Finance and Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.</span><span class="sxs-lookup"><span data-stu-id="e5df4-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="e5df4-113">Dışa aktarılacak rapor tanımlarını seçin:</span><span class="sxs-lookup"><span data-stu-id="e5df4-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="e5df4-114">Tüm rapor tanımlarını ve ilgili yapı taşlarını dışa aktarmak için **Tümünü Seç** öğesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="e5df4-115">Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini dışa aktarmak için ilgili sekmeye tıklayın ve ardından dışa aktarılacak maddeleri seçin.</span><span class="sxs-lookup"><span data-stu-id="e5df4-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="e5df4-116">Bir sekme birden fazla öğeyi seçmek için Ctrl tuşunu basılı tutun. Dışa aktarılacak raporları seçtiğinizde ilişkili satırlar, sütunlar, ağaçlar ve boyut kümeleri seçilir.</span><span class="sxs-lookup"><span data-stu-id="e5df4-116">Press and hold the Ctrl key to select multiple items in a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="e5df4-117">**Dışa Aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-117">Click **Export**.</span></span>
5.  <span data-ttu-id="e5df4-118">Bir dosya adı girin ve dışarı aktarılan rapor tanımlarını kaydetmek için istediğiniz güvenli bir konumu seçin.</span><span class="sxs-lookup"><span data-stu-id="e5df4-118">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="e5df4-119">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-119">Click **Save**.</span></span>

<span data-ttu-id="e5df4-120">Dosya güvenli bir konuma kopyalanabilir veya yüklenebilir; bu dosyanın daha sonra farklı bir ortama aktarılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e5df4-120">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="e5df4-121">Microsoft Azure depolama hesabı kullanma hakkındaki bilgileri [>AzCopy Komut Satırı Yardımcı Programı ile veri transferi](/azure/storage/storage-use-azcopy) bölümünde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5df4-121">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="e5df4-122">Microsoft, Finance and Operations sözleşmenizin bir parçası olarak bir depolama hesabı sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="e5df4-122">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="e5df4-123">Bir depolama hesabı satın almanız veya ayrı bir Azure aboneliğine ait bir depolama hesabını kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5df4-123">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="e5df4-124">Azure Sanal Makineler'de D sürücüsünün davranışını dikkate alın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-124">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="e5df4-125">Dışa aktarılan yapı taşı gruplarınızı burada kalıcı olarak saklamayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-125">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="e5df4-126">Geçici sürücüler hakkında daha fazla bilgi için bkz. [Microsoft Azure Sanal Makinelerindeki geçici sürücüyü anlama](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="e5df4-126">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="e5df4-127">Hizmetleri durdurma</span><span class="sxs-lookup"><span data-stu-id="e5df4-127">Stop services</span></span>
<span data-ttu-id="e5df4-128">Ortamdaki tüm bilgisayarlara bağlanmak ve services.msc'yi kullanarak aşağıdaki Windows hizmetlerini durdurmak için Uzak Masaüstü'nü kullanın:</span><span class="sxs-lookup"><span data-stu-id="e5df4-128">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="e5df4-129">World wide web publishing service (tüm AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="e5df4-129">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="e5df4-130">Microsoft Dynamics 365 for Finance and Operations Toplu İŞ Yönetimi Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="e5df4-130">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="e5df4-131">Management Reporter 2012 İşlem Hizmeti (yalnızca BI bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="e5df4-131">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="e5df4-132">Bu hizmetlerin Finance and Operations veritabanına açık bağlantıları olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e5df4-132">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="e5df4-133">Sıfırla</span><span class="sxs-lookup"><span data-stu-id="e5df4-133">Reset</span></span>
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="e5df4-134">En güncel MinorVersionDataUpgrade.zip paketini bulun ve indirin.</span><span class="sxs-lookup"><span data-stu-id="e5df4-134">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="e5df4-135">[MinorVersionDataUpgrade.zip komut dosyasını indirme](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages) konusundaki yönergeleri kullanarak en son MinorVersionDataUpgrade.zip paketini bulun.</span><span class="sxs-lookup"><span data-stu-id="e5df4-135">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="e5df4-136">Yönergeler veri yükseltme paketinin doğru sürümünü nasıl bulacağınızı ve indireceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="e5df4-136">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="e5df4-137">MinorVersionDataUpgrade.zip paketini indirmek için bir güncelleştirme gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="e5df4-137">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="e5df4-138">"En son veri yükseltme dağıtılabilir paketini karşıdan yükleme" bölümündeki adımları MinorVersionDataUpgrade.zip paketinin bir kopyasını almak için makalesinde yapmadan diğer adımları tamamlamak yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="e5df4-138">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="e5df4-139">Finance and Operations veritabanı için komut dosyalarını çalıştırma</span><span class="sxs-lookup"><span data-stu-id="e5df4-139">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="e5df4-140">Aşağıdaki komut dosyalarını Finance and Operations veritabanı için çalıştırın (finansal raporlama veritabanı için değil).</span><span class="sxs-lookup"><span data-stu-id="e5df4-140">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="e5df4-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="e5df4-141">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="e5df4-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="e5df4-142">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="e5df4-143">Bu komut dosyaları kullanıcıların, rollerin ve değişiklik izleme ayarlarının doğru olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="e5df4-143">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="e5df4-144">Veritabanını sıfırlamak için PowerShell komutunu çalıştırma</span><span class="sxs-lookup"><span data-stu-id="e5df4-144">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="e5df4-145">Finance and Operations ve mali raporlama tümleştirmesini sıfırlamak için doğrudan AOS bilgisayarındaki aşağıdaki komutları PowerShell içerisinde bir Yönetici olarak çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="e5df4-145">On the AOS computer, execute the following commands in PowerShell as an Administrator to reset the integration between Finance and Operations and financial reporting:</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> <span data-ttu-id="e5df4-146">Komutları çalıştırdıktan sonra, onaylamak için "Y" girmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="e5df4-146">After executing the commands, you will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="e5df4-147">Parametre açıklaması:</span><span class="sxs-lookup"><span data-stu-id="e5df4-147">Explanation of parameters:</span></span>

-   <span data-ttu-id="e5df4-148">Neden - için geçerli değerler şunlardır: SERVICING, BADDATA, OTHER</span><span class="sxs-lookup"><span data-stu-id="e5df4-148">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="e5df4-149">ReasonDetail parametresi serbest metindir.</span><span class="sxs-lookup"><span data-stu-id="e5df4-149">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="e5df4-150">Neden ve reasonDetail telemetri/ortam izlemede kaydedilecektir.</span><span class="sxs-lookup"><span data-stu-id="e5df4-150">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="e5df4-151">Hizmetleri başlatma</span><span class="sxs-lookup"><span data-stu-id="e5df4-151">Start services</span></span>
<span data-ttu-id="e5df4-152">Daha önce durdurduğunuz hizmetleri yeniden başlatmak için services.msc'yi kullanın:</span><span class="sxs-lookup"><span data-stu-id="e5df4-152">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="e5df4-153">World wide web publishing service (tüm AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="e5df4-153">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="e5df4-154">Microsoft Dynamics 365 for Finance and Operations Toplu İŞ Yönetimi Hizmeti (yalnızca özel olmayan AOS bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="e5df4-154">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="e5df4-155">Management Reporter 2012 İşlem Hizmeti (yalnızca BI bilgisayarlarda)</span><span class="sxs-lookup"><span data-stu-id="e5df4-155">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="e5df4-156">Rapor tanımlarını içe aktarma</span><span class="sxs-lookup"><span data-stu-id="e5df4-156">Import report definitions</span></span>
<span data-ttu-id="e5df4-157">Rapor Tasarımcısı'ndan rapor tanımlarınızı dışa aktarma sırasında oluşturulan dosyayı kullanarak içe aktarın:</span><span class="sxs-lookup"><span data-stu-id="e5df4-157">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="e5df4-158">Rapor Tasarımcısında, **Şirket** &gt; **Yapı Taşı Grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e5df4-158">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="e5df4-159">Dışa aktarılacak yapı taşı grubunu seçin ve **Dışa Aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-159">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="e5df4-160">Finance and Operations için yalnızca bir yapı taşı grubu desteklenir, **Varsayılan**.</span><span class="sxs-lookup"><span data-stu-id="e5df4-160">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="e5df4-161">**Varsayılan** yapı bloğunu seçin ve **İçe Aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-161">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="e5df4-162">Dışa aktarılan rapor tanımlarını içeren dosyayı seçin **Aç**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-162">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="e5df4-163">İçe Aktar iletişim kutusunda, içe aktarılacak rapor tanımlarını seçin:</span><span class="sxs-lookup"><span data-stu-id="e5df4-163">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="e5df4-164">Tüm rapor tanımlarını ve destekleyici yapı taşlarını içe aktarmak için **Tümünü Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-164">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="e5df4-165">Belirli raporları, satırları, sütunları, ağaçları veya boyut kümelerini içe aktarmak için, içe aktarılacak raporları, satırları, sütunları, ağaçları veya boyut kümelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="e5df4-165">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="e5df4-166">**İçe aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5df4-166">Click **Import**.</span></span>





