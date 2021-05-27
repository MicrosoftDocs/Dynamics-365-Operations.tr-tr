---
title: Stok Görünürlüğü Eklentisi
description: Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisinin nasıl yüklendiğini ve yapılandırıldığını açıklar.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 84f5e949f0c81f840c8a9086d05bbcfc576e42aa
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017018"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="52784-103">Stok Görünürlüğü Eklentisi</span><span class="sxs-lookup"><span data-stu-id="52784-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="52784-104">Stok Görünürlüğü Eklentisi, gerçek zamanlı olarak elden stok takibi sağlayan ve böylece stok görünürlüğünün genel görünümünü sunan bağımsız ve yüksek ölçeklenebilir bir mikro hizmettir.</span><span class="sxs-lookup"><span data-stu-id="52784-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="52784-105">Eldeki stokla ilgili tüm bilgiler, düşük düzeyli SQL tümleştirmesi aracılığıyla neredeyse gerçek zamanlı olarak hizmete dışarı aktarılır.</span><span class="sxs-lookup"><span data-stu-id="52784-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="52784-106">Harici sistemler, verilen boyut kümeleri üzerindeki bilgileri sorgulamak için restful API'lar aracılığıyla hizmete erişir ve böylece eldeki mevcut pozisyonların bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="52784-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="52784-107">Stok Görünürlüğü, Microsoft Dataverse üzerine kurulmuş bir mikro hizmettir; diğer bir ifadeyle, iş gereksinimlerinizi karşılamak için özelleştirilmiş işlevsellik sağlamak için Power Apps oluşturup Power BI uygulayarak genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="52784-108">Envanter sorguları yapmak için dizini yükseltmeniz de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="52784-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="52784-109">Stok Görünürlüğü, birden çok üçüncü taraf sistemle tümleştirmeye olanak tanıyan yapılandırma seçenekleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="52784-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="52784-110">Standartlaştırılmış stok boyutunu, özelleştirilmiş genişletilebilirliği ve standartlaştırılmış, yapılandırılabilir hesaplanmış miktarları destekler.</span><span class="sxs-lookup"><span data-stu-id="52784-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="52784-111">Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi'nin nasıl yüklenilip yapılandırılacağını ve uygulama programlama arabiriminin (API) nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="52784-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="52784-112">Stok Görünürlüğü Eklentisini Yükleme</span><span class="sxs-lookup"><span data-stu-id="52784-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="52784-113">Stok Görünürlüğü Eklentisi'ni, Microsoft Dynamics Lifecycle Services'ı (LCS) kullanarak yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="52784-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="52784-114">LCS, Dynamics 365 Finance and Operations uygulamalarınızın uygulama yaşam döngüsünü yönetmenize yardımcı olan bir ortam ve düzenli olarak güncelleştirilen bir dizi hizmet sağlayan bir işbirliği portalıdır.</span><span class="sxs-lookup"><span data-stu-id="52784-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="52784-115">Daha fazla bilgi için bkz. [Lifecycle Services kaynakları](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span><span class="sxs-lookup"><span data-stu-id="52784-115">For more information, see [Lifecycle Services resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).</span></span>

### <a name="inventory-visibility-add-in-prerequisites"></a><span data-ttu-id="52784-116">Stok Görünürlüğü Eklentisi ön koşulları</span><span class="sxs-lookup"><span data-stu-id="52784-116">Inventory Visibility Add-in prerequisites</span></span>

<span data-ttu-id="52784-117">Stok Görünürlüğü Eklentisi'ni yüklemeden önce aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="52784-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="52784-118">En az bir ortam dağıtılan bir LCS uygulama projesi edinin.</span><span class="sxs-lookup"><span data-stu-id="52784-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="52784-119">[Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)'ta sağlanan eklentileri ayarlama ön koşullarının tamamlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="52784-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="52784-120">Stok Görünürlüğü, çift yazma bağlantısı gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="52784-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="52784-121">Aşağıdaki üç gerekli dosyayı almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü Ekibi'ne başvurun:</span><span class="sxs-lookup"><span data-stu-id="52784-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - <span data-ttu-id="52784-122">`Inventory Visibility Integration.zip` (Supply Chain Management'ın çalıştırdığınız bu sürümü 10.0.18 sürümünden daha eskiyse)</span><span class="sxs-lookup"><span data-stu-id="52784-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>
- <span data-ttu-id="52784-123">Buna ek olarak, aşağıdaki Package Deployer paketlerini almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü Ekibi'ne başvurun:</span><span class="sxs-lookup"><span data-stu-id="52784-123">Alternatively, contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package deployer packages.</span></span> <span data-ttu-id="52784-124">Bu paketler, resmi bir Package Deployer aracı tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="52784-124">These packages can be used by an official package deployer tool.</span></span>
  - `InventoryServiceBase.PackageDeployer.zip`
  - <span data-ttu-id="52784-125">`InventoryServiceApplication.PackageDeployer.zip`(Bu paket, `InventoryServiceBase` paketindeki tüm değişiklikleri ve ek kullanıcı arabirimi uygulama bileşenlerini içerir)</span><span class="sxs-lookup"><span data-stu-id="52784-125">`InventoryServiceApplication.PackageDeployer.zip` (this package contains all of the changes in the `InventoryServiceBase` package, plus additional UI application components)</span></span>
- <span data-ttu-id="52784-126">Bir uygulamayı kaydettirmek ve Azure aboneliğiniz altında AAD'ye istemci gizli anahtarı eklemek için [Hızlı Başlangıç: Bir uygulamayı Microsoft kimlik platformuna kaydetme](/azure/active-directory/develop/quickstart-register-app) bölümünde verilen yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="52784-126">Follow the instructions given in [Quickstart: Register an application with the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register an application and add a client secret to AAD under your azure subscription.</span></span>
  - [<span data-ttu-id="52784-127">Uygulama kaydetme</span><span class="sxs-lookup"><span data-stu-id="52784-127">Register an application</span></span>](/azure/active-directory/develop/quickstart-register-app)
  - [<span data-ttu-id="52784-128">İstemci gizli anahtarı</span><span class="sxs-lookup"><span data-stu-id="52784-128">Add a client secret</span></span>](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - <span data-ttu-id="52784-129">**Uygulama(İstemci) Kimliği**, **İstemci Gizli Anahtarı** ve **Kiracı Kimliği** aşağıdaki adımlarda kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="52784-129">The **Application(Client) Id**, **Client Secret**, and **Tenant ID** will be used in the following steps.</span></span>

> [!NOTE]
> <span data-ttu-id="52784-130">Şu anda desteklenen ülkeler/bölgeler arasında Kanada, ABD ve Avrupa Birliği (AB) bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="52784-130">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="52784-131">Bu ön koşullarla ilgili herhangi bir sorunuz varsa lütfen Stok Görünürlüğü ürün takımıyla iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="52784-131">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="52784-132">Ayarlama Dataverse</span><span class="sxs-lookup"><span data-stu-id="52784-132">Set up Dataverse</span></span>

<span data-ttu-id="52784-133">Dataverse'ü Stok Görünürlüğüyle kullanılacak şekilde ayarlamak için, önce önkoşulları hazırlamanız ve sonra Dataverse'ü Package Deployer aracını kullanarak mı yoksa çözümleri el ile içe aktararak mı ayarlayacağınıza karar vermeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="52784-133">To set up Dataverse for use with Inventory Visibility, you must first prepare the prerequisites and then decide whether to set up Dataverse using either the package deployer tool or by manually importing the solutions (you don't have to do both).</span></span> <span data-ttu-id="52784-134">Ardından Stok Görünürlüğü Eklentisini yükleyin.</span><span class="sxs-lookup"><span data-stu-id="52784-134">Then install the Inventory Visibility Add-in.</span></span> <span data-ttu-id="52784-135">Aşağıdaki alt kısımlar, bu görevlerin nasıl tamamlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="52784-135">The following subsections describe how to complete each of these tasks.</span></span>

#### <a name="prepare-dataverse-prerequisites"></a><span data-ttu-id="52784-136">Dataverse önkoşullarını hazırlama</span><span class="sxs-lookup"><span data-stu-id="52784-136">Prepare Dataverse prerequisites</span></span>

<span data-ttu-id="52784-137">Dataverse'ü kurmaya başlamadan önce, aşağıdakileri gerçekleştirerek kiracınıza bir hizmet ilkesi ekleyin:</span><span class="sxs-lookup"><span data-stu-id="52784-137">Before you start to set up Dataverse, add a service principle to your tenant by doing the following:</span></span>

1. <span data-ttu-id="52784-138">Azure AD PowerShell Modülü v2'yi [ Graph için Azure Active Directory PowerShell'i Yüklema](/powershell/azure/active-directory/install-adv2) bölümünde açıklandığı gibi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="52784-138">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>

1. <span data-ttu-id="52784-139">Aşağıdaki PowerShell komutunu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="52784-139">Run the following PowerShell command:</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a><span data-ttu-id="52784-140">Package Deployer aracını kullanarak Dataverse'ü kurma</span><span class="sxs-lookup"><span data-stu-id="52784-140">Set up Dataverse using the package deployer tool</span></span>

<span data-ttu-id="52784-141">Önkoşulları yerine getirdikten sonra, Dataverse'ü Package Deployer aracını kullanarak ayarlamayı tercih ediyorsanız aşağıdaki prosedürü kullanın.</span><span class="sxs-lookup"><span data-stu-id="52784-141">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse using the package deployer tool.</span></span> <span data-ttu-id="52784-142">Bunun yerine, çözümlerin el ile nasıl içe aktarılacağı hakkında ayrıntılı bilgi için sonraki bölüme bakın (iki yöntemi birden uygulamayın).</span><span class="sxs-lookup"><span data-stu-id="52784-142">See the next section for details about how to import the solutions manually instead (don't do both).</span></span>

1. <span data-ttu-id="52784-143">Geliştirici araçlarını, [NuGet'ten araçları indirme](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget) bölümünde açıklandığı şekilde yükleyin.</span><span class="sxs-lookup"><span data-stu-id="52784-143">Install developer tools as described in [Download tools from NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).</span></span>

1. <span data-ttu-id="52784-144">İş gereksinimlerinize göre, `InventoryServiceBase` veya `InventoryServiceApplication` paketini seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-144">Based on your business requirements, choose the `InventoryServiceBase` or `InventoryServiceApplication` package.</span></span>

1. <span data-ttu-id="52784-145">Çözümleri içe aktarın:</span><span class="sxs-lookup"><span data-stu-id="52784-145">Import the solutions:</span></span>
    1. <span data-ttu-id="52784-146">`InventoryServiceBase` paketi için:</span><span class="sxs-lookup"><span data-stu-id="52784-146">For the `InventoryServiceBase` package:</span></span>
        - <span data-ttu-id="52784-147">`InventoryServiceBase.PackageDeployer.zip` zip dosyasını açın</span><span class="sxs-lookup"><span data-stu-id="52784-147">Unzip `InventoryServiceBase.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="52784-148">`InventoryServiceBase` klasörünü, `[Content_Types].xml` dosyasını, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll` dosyasını, `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` dosyasını ve `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` dosyasını bulun.</span><span class="sxs-lookup"><span data-stu-id="52784-148">Find folder `InventoryServiceBase`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`.</span></span> 
        - <span data-ttu-id="52784-149">Bu klasör ve dosyaların her birini, geliştirici araçlarını yüklediğinizde oluşturulan `.\Tools\PackageDeployment` dizinine kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="52784-149">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="52784-150">`InventoryServiceApplication` paketi için:</span><span class="sxs-lookup"><span data-stu-id="52784-150">For the `InventoryServiceApplication` package:</span></span>
        - <span data-ttu-id="52784-151">`InventoryServiceApplication.PackageDeployer.zip` zip dosyasını açın</span><span class="sxs-lookup"><span data-stu-id="52784-151">Unzip `InventoryServiceApplication.PackageDeployer.zip`</span></span>
        - <span data-ttu-id="52784-152">`InventoryServiceApplication` klasörünü, `[Content_Types].xml` dosyasını, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` dosyasını, `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` dosyasını ve `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` dosyasını bulun.</span><span class="sxs-lookup"><span data-stu-id="52784-152">Find folder `InventoryServiceApplication`, file `[Content_Types].xml`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`, and file `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.</span></span>
        - <span data-ttu-id="52784-153">Bu klasör ve dosyaların her birini, geliştirici araçlarını yüklediğinizde oluşturulan `.\Tools\PackageDeployment` dizinine kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="52784-153">Copy each of these folders and files to the `.\Tools\PackageDeployment` directory, which was created when you installed the developer tools.</span></span>
    1. <span data-ttu-id="52784-154">`.\Tools\PackageDeployment\PackageDeployer.exe`'yi yürütün.</span><span class="sxs-lookup"><span data-stu-id="52784-154">Execute `.\Tools\PackageDeployment\PackageDeployer.exe`.</span></span> <span data-ttu-id="52784-155">Çözümleri içe aktarmak için ekranınızdaki talimatları izleyin.</span><span class="sxs-lookup"><span data-stu-id="52784-155">Follow the instructions on your screen to import the solutions.</span></span>

1. <span data-ttu-id="52784-156">Uygulama kullanıcısına güvenlik rolleri atayın.</span><span class="sxs-lookup"><span data-stu-id="52784-156">Assign security roles to the application user.</span></span>
    1. <span data-ttu-id="52784-157">Dataverse ortamınızın URL'sini açın.</span><span class="sxs-lookup"><span data-stu-id="52784-157">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="52784-158">**Gelişmiş Ayarlar \> Sistem \> Güvenlik \> Kullanıcılar**'a gidin ve **# InventoryVisibility** adlı kullanıcıyı bulun.</span><span class="sxs-lookup"><span data-stu-id="52784-158">Go to **Advanced Setting \> System \> Security \> Users**, and find user the named **# InventoryVisibility**.</span></span>
    1. <span data-ttu-id="52784-159">**Rol Ata**'yı ve sonra **Sistem Yöneticisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-159">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="52784-160">**Common Data Service Kullanıcısı** adlı bir rol varsa bunu da seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-160">If there is a role that is named **Common Data Service User**, select it as well.</span></span>

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a><span data-ttu-id="52784-161">Çözümleri içe aktararak Dataverse'ü elle kurma</span><span class="sxs-lookup"><span data-stu-id="52784-161">Set up Dataverse manually by importing solutions</span></span>

<span data-ttu-id="52784-162">Önkoşulları yerine getirdikten sonra, Dataverse'ü çözümleri elle içe aktararak ayarlamayı tercih ediyorsanız aşağıdaki prosedürü kullanın.</span><span class="sxs-lookup"><span data-stu-id="52784-162">After you have the prerequisites in place, use the following procedure if you prefer to set up Dataverse by manually importing solutions.</span></span> <span data-ttu-id="52784-163">Bunun yerine Package Deployer aracının kullanımıyla ilgili ayrıntılar için önceki bölüme bakın (iki yöntemi birden uygulamayın).</span><span class="sxs-lookup"><span data-stu-id="52784-163">See the previous section for details about how to use the package deployer tool instead (don't do both).</span></span>

1. <span data-ttu-id="52784-164">Dataverse'te Stok Görünürlüğü için bir uygulama kullanıcısı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="52784-164">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="52784-165">Dataverse ortamınızın URL'sini açın.</span><span class="sxs-lookup"><span data-stu-id="52784-165">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="52784-166">**Gelişmiş Ayar \> Sistem \> Güvenlik \> Kullanıcılar**'a gidin ve bir uygulama kullanıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="52784-166">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="52784-167">Sayfa görünümünü **Uygulama Kullanıcıları** olarak değiştirmek için görünüm menüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="52784-167">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="52784-168">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-168">Select **New**.</span></span> <span data-ttu-id="52784-169">Uygulama kimliğini *3022308a-b9bd-4a18-b8ac-2ddedb2075e1* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52784-169">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="52784-170">(Değişikliklerinizi kaydettiğinizde nesne kimliği otomatik olarak yüklenir.) Adı özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-170">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="52784-171">Örneğin *Stok Görünürlüğü* olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-171">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="52784-172">Tamamladıktan sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-172">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="52784-173">**Rol Ata**'yı ve sonra **Sistem Yöneticisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-173">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="52784-174">**Common Data Service Kullanıcısı** adlı bir rol varsa onu da seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-174">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="52784-175">Daha fazla bilgi için bkz. [Uygulama kullanıcısı oluşturma](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="52784-175">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="52784-176">Dataverse varsayılan diliniz **İngilizce** değilse:</span><span class="sxs-lookup"><span data-stu-id="52784-176">If the default language of your Dataverse is not **English**:</span></span>

    1. <span data-ttu-id="52784-177">**Gelişmiş Ayar \> Yönetim \>Diller**'e gidin,</span><span class="sxs-lookup"><span data-stu-id="52784-177">Go to **Advanced Setting \> Administration \> Languages**,</span></span>
    1. <span data-ttu-id="52784-178">**İngilizce (LanguageCode=1033)** dilini ve **Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-178">Select **English (LanguageCode=1033)** and select **Apply**.</span></span>

1. <span data-ttu-id="52784-179">Dataverse yapılandırmasıyla ilgili varlıkları ve Power Apps'i içeren `Inventory Visibility Dataverse Solution.zip` dosyasını içeri aktarın:</span><span class="sxs-lookup"><span data-stu-id="52784-179">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="52784-180">**Çözümler** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="52784-180">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="52784-181">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-181">Select **Import**.</span></span>

1. <span data-ttu-id="52784-182">Yapılandırma yükseltme tetikleyici akışını içeri aktarın:</span><span class="sxs-lookup"><span data-stu-id="52784-182">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="52784-183">Microsoft Flow sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="52784-183">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="52784-184">*Dataverse (eski)* olarak adlandırılan bağlantının mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="52784-184">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="52784-185">(Yoksa oluşturun.)</span><span class="sxs-lookup"><span data-stu-id="52784-185">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="52784-186">`Inventory Visibility Configuration Trigger.zip` dosyasını içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="52784-186">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="52784-187">İçeri aktarıldıktan sonra tetikleyici **Akışlarım** altında görünecektir.</span><span class="sxs-lookup"><span data-stu-id="52784-187">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="52784-188">Ortam bilgilerine bağlı olarak aşağıdaki dört değişkeni başlatın:</span><span class="sxs-lookup"><span data-stu-id="52784-188">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="52784-189">Azure Kiracısı Kimliği</span><span class="sxs-lookup"><span data-stu-id="52784-189">Azure Tenant ID</span></span>
        - <span data-ttu-id="52784-190">Azure Uygulaması İstemci Kimliği</span><span class="sxs-lookup"><span data-stu-id="52784-190">Azure Application Client ID</span></span>
        - <span data-ttu-id="52784-191">Azure Uygulaması Gizli Anahtarı</span><span class="sxs-lookup"><span data-stu-id="52784-191">Azure Application Client Secret</span></span>
        - <span data-ttu-id="52784-192">Stok Görünürlüğü Uç Noktası</span><span class="sxs-lookup"><span data-stu-id="52784-192">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="52784-193">Bu değişken hakkında daha fazla bilgi için bu konuda ele alınacak olan [Stok Görünürlüğü tümleştirmesini ayarlama](#setup-inventory-visibility-integration) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="52784-193">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="52784-194">![Yapılandırma tetikleyicisi](media/configuration-trigger.png "Yapılandırma tetikleyicisi")</span><span class="sxs-lookup"><span data-stu-id="52784-194">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="52784-195">**Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-195">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="52784-196">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="52784-196">Install the add-in</span></span>

<span data-ttu-id="52784-197">Stok Görünürlüğü Eklentisi'ni yüklemek için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="52784-197">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="52784-198">[Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portalında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="52784-198">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="52784-199">Ana sayfada, ortamınızın dağıtıldığı projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-199">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="52784-200">Proje sayfasında, eklentiyi yüklemek istediğiniz ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-200">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="52784-201">Ortam sayfasında, **Power Platform tümleştirmesi** bölümünde Dataverse ortamı adını bulabileceğiniz **Ortam eklentileri** bölümünü görene kadar aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="52784-201">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="52784-202">**Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-202">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="52784-203">![LCS'deki ortam sayfası](media/inventory-visibility-environment.png "LCS'deki ortam sayfası")</span><span class="sxs-lookup"><span data-stu-id="52784-203">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="52784-204">**Yeni eklenti yükleyin** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-204">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="52784-205">Kullanılabilir eklentilerin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="52784-205">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="52784-206">Listeden **Stok Görünürlüğü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-206">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="52784-207">Ortamınızın aşağıdaki alanlarının değerlerini girin:</span><span class="sxs-lookup"><span data-stu-id="52784-207">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="52784-208">**AAD uygulaması (istemci) kimliği**</span><span class="sxs-lookup"><span data-stu-id="52784-208">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="52784-209">**AAD kiracı kimliği**</span><span class="sxs-lookup"><span data-stu-id="52784-209">**AAD tenant ID**</span></span>

    <span data-ttu-id="52784-210">![Eklenti kurulum sayfası](media/inventory-visibility-setup.png "Eklenti kurulum sayfası")</span><span class="sxs-lookup"><span data-stu-id="52784-210">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="52784-211">**Şartlar ve koşullar** onay kutusunu seçerek şartlar ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="52784-211">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="52784-212">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-212">Select **Install**.</span></span> <span data-ttu-id="52784-213">Eklentinin durumu **Yükleniyor** olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="52784-213">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="52784-214">İşlem bittiğinde, durumun **Yüklendi** olarak değiştiğini görmek için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="52784-214">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="52784-215">Eklentiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="52784-215">Uninstall the add-in</span></span>

<span data-ttu-id="52784-216">Eklentiyi kaldırmak için **Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52784-216">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="52784-217">LCS'yi yenilediğinizde Stok Görünürlüğü Eklentisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="52784-217">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="52784-218">Kaldırma işlemi eklenti kaydını kaldırır ve hizmette depolanan tüm iş verilerini temizlemek için bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="52784-218">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="52784-219">Supply Chain Management'tak eldeki stok verilerini kullanma</span><span class="sxs-lookup"><span data-stu-id="52784-219">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="52784-220">Stok Görünürlüğü tümleştirme paketini dağıtma</span><span class="sxs-lookup"><span data-stu-id="52784-220">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="52784-221">Supply Chain Management sürüm 10.0.17 veya önceki bir sürümünü çalıştırıyorsanız paket dosyasını almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü yerleşik destek ekibine başvurun.</span><span class="sxs-lookup"><span data-stu-id="52784-221">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="52784-222">Ardından LCS'de paketi dağıtın.</span><span class="sxs-lookup"><span data-stu-id="52784-222">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="52784-223">Dağıtım sırasında bir sürüm uyuşmazlığı hatası oluşursa X++ projesini geliştirme ortamınıza el ile içeri aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52784-223">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="52784-224">Daha sonra, dağıtılabilir paketi geliştirme ortamınızda oluşturun ve üretim ortamınızda dağıtın.</span><span class="sxs-lookup"><span data-stu-id="52784-224">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="52784-225">Kod, Supply Chain Management sürüm 10.0.18'e dahildir.</span><span class="sxs-lookup"><span data-stu-id="52784-225">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="52784-226">Bu sürümü veya sonraki bir sürümünü çalıştırıyorsanız dağıtım gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="52784-226">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="52784-227">Supply Chain Management ortamınızda aşağıdaki özelliklerin açık olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="52784-227">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="52784-228">(Varsayılan olarak bunlar açıktır.)</span><span class="sxs-lookup"><span data-stu-id="52784-228">(By default, they are turned on.)</span></span>

| <span data-ttu-id="52784-229">Özellik açıklaması</span><span class="sxs-lookup"><span data-stu-id="52784-229">Feature description</span></span> | <span data-ttu-id="52784-230">Kod sürümü</span><span class="sxs-lookup"><span data-stu-id="52784-230">Code version</span></span> | <span data-ttu-id="52784-231">Sınıfı değiştirme</span><span class="sxs-lookup"><span data-stu-id="52784-231">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="52784-232">InventSum tablosunda stok boyutlarını kullanmayı etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="52784-232">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="52784-233">10.0.11</span><span class="sxs-lookup"><span data-stu-id="52784-233">10.0.11</span></span> | <span data-ttu-id="52784-234">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="52784-234">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="52784-235">InventSumDelta tablosunda stok boyutlarını kullanmayı etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="52784-235">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="52784-236">10.0.12</span><span class="sxs-lookup"><span data-stu-id="52784-236">10.0.12</span></span> | <span data-ttu-id="52784-237">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="52784-237">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="52784-238">Stok Görünürlüğü tümleştirmesini kurma</span><span class="sxs-lookup"><span data-stu-id="52784-238">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="52784-239">Supply Chain Management'ta **[Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** çalışma alanını açın ve **Stok Görünürlüğü Tümleştirmesi** özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="52784-239">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="52784-240">**Stok Yönetimi \> Kurulum \> Stok Görünürlüğü Tümleştirme parametreleri**'ne gidin ve Stok Görünürlüğü'nü çalıştırdığınız ortamın URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="52784-240">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="52784-241">LCS ortamınızın Azure bölgesini bulun ve URL'yi girin.</span><span class="sxs-lookup"><span data-stu-id="52784-241">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="52784-242">URL aşağıdaki biçimde olur:</span><span class="sxs-lookup"><span data-stu-id="52784-242">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="52784-243">Örneğin, Avrupa'daysanız ortamınızda aşağıdaki URL'lerden biri bulunur:</span><span class="sxs-lookup"><span data-stu-id="52784-243">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    <span data-ttu-id="52784-244">Şu anda aşağıdaki bölgeler kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="52784-244">The following regions are currently available.</span></span>

    | <span data-ttu-id="52784-245">Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="52784-245">Azure region</span></span> | <span data-ttu-id="52784-246">Bölge kısa adı</span><span class="sxs-lookup"><span data-stu-id="52784-246">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="52784-247">Doğu Avustralya</span><span class="sxs-lookup"><span data-stu-id="52784-247">Australia east</span></span> | <span data-ttu-id="52784-248">eau</span><span class="sxs-lookup"><span data-stu-id="52784-248">eau</span></span> |
    | <span data-ttu-id="52784-249">Güneydoğu Avustralya</span><span class="sxs-lookup"><span data-stu-id="52784-249">Australia southeast</span></span> | <span data-ttu-id="52784-250">seau</span><span class="sxs-lookup"><span data-stu-id="52784-250">seau</span></span> |
    | <span data-ttu-id="52784-251">Orta Kanada</span><span class="sxs-lookup"><span data-stu-id="52784-251">Canada central</span></span> | <span data-ttu-id="52784-252">cca</span><span class="sxs-lookup"><span data-stu-id="52784-252">cca</span></span> |
    | <span data-ttu-id="52784-253">Doğu Kanada</span><span class="sxs-lookup"><span data-stu-id="52784-253">Canada east</span></span> | <span data-ttu-id="52784-254">eca</span><span class="sxs-lookup"><span data-stu-id="52784-254">eca</span></span> |
    | <span data-ttu-id="52784-255">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="52784-255">North Europe</span></span> | <span data-ttu-id="52784-256">neu</span><span class="sxs-lookup"><span data-stu-id="52784-256">neu</span></span> |
    | <span data-ttu-id="52784-257">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="52784-257">West Europe</span></span> | <span data-ttu-id="52784-258">weu</span><span class="sxs-lookup"><span data-stu-id="52784-258">weu</span></span> |
    | <span data-ttu-id="52784-259">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="52784-259">East US</span></span> | <span data-ttu-id="52784-260">eus</span><span class="sxs-lookup"><span data-stu-id="52784-260">eus</span></span> |
    | <span data-ttu-id="52784-261">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="52784-261">West US</span></span> | <span data-ttu-id="52784-262">wus</span><span class="sxs-lookup"><span data-stu-id="52784-262">wus</span></span> |

1. <span data-ttu-id="52784-263">**Stok Yönetimi \> Periyodik \> Stok Görünürlüğü Tümleştirmesi**'ne gidin ve işi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="52784-263">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="52784-264">Supply Chain Management'taki tüm stok değişikliği olayları artık Stok Görünürlüğü'ne nakledilecektir.</span><span class="sxs-lookup"><span data-stu-id="52784-264">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="52784-265">Stok Görünürlüğü Eklentisi genel API'si</span><span class="sxs-lookup"><span data-stu-id="52784-265">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="52784-266">Stok Görünürlüğü Eklentisi'nin genel REST API'si, birkaç özel tümleştirme uç noktası sunar.</span><span class="sxs-lookup"><span data-stu-id="52784-266">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="52784-267">Üç ana etkileşim türünü destekler:</span><span class="sxs-lookup"><span data-stu-id="52784-267">It supports three main interaction types:</span></span>

- <span data-ttu-id="52784-268">Harici bir sistemden eldeki stok değişiklikleri eklentiye deftere nakletmek</span><span class="sxs-lookup"><span data-stu-id="52784-268">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="52784-269">Harici bir sistemden eldeki geçerli miktarları sorgulamak</span><span class="sxs-lookup"><span data-stu-id="52784-269">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="52784-270">Supply Chain Management eldeki stoku ile otomatik eşitlemek</span><span class="sxs-lookup"><span data-stu-id="52784-270">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="52784-271">Otomatik eşitleme genel API kapsamında değildir.</span><span class="sxs-lookup"><span data-stu-id="52784-271">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="52784-272">Bunun yerine, Stok Görünürlüğü Eklentisi'nin etkinleştirildiği ortamlar için arka planda işlenir.</span><span class="sxs-lookup"><span data-stu-id="52784-272">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="52784-273">Kimlik Doğrulama</span><span class="sxs-lookup"><span data-stu-id="52784-273">Authentication</span></span>

<span data-ttu-id="52784-274">Platform güvenlik belirteci, Stok Görünürlüğü Eklentisi'ni çağırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52784-274">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="52784-275">Bu nedenle, Azure AD uygulamanızı kullanarak bir *Azure Active Directory (Azure AD) belirteci* oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52784-275">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="52784-276">Daha sonra güvenlik hizmetinden *erişim belirtecini* almak için Azure AD belirteci kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52784-276">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="52784-277">Aşağıdakileri gerçekleştirerek güvenlik hizmeti belirteci alın:</span><span class="sxs-lookup"><span data-stu-id="52784-277">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="52784-278">Azure portalda oturum açın ve Supply Chain Management uygulamanız için `clientId` ve `clientSecret` bilgilerini bulmak için portalı kullanın.</span><span class="sxs-lookup"><span data-stu-id="52784-278">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="52784-279">Aşağıdaki özelliklere sahip bir HTTP isteği göndererek Azure Active Directory belirteci (`aadToken`) getirin:</span><span class="sxs-lookup"><span data-stu-id="52784-279">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="52784-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="52784-280">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="52784-281">**Yöntem** - `GET`</span><span class="sxs-lookup"><span data-stu-id="52784-281">**Method** - `GET`</span></span>
    - <span data-ttu-id="52784-282">**Gövde içeriği (form verileri)**:</span><span class="sxs-lookup"><span data-stu-id="52784-282">**Body content (form data)**:</span></span>

        | <span data-ttu-id="52784-283">key</span><span class="sxs-lookup"><span data-stu-id="52784-283">key</span></span> | <span data-ttu-id="52784-284">değer</span><span class="sxs-lookup"><span data-stu-id="52784-284">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="52784-285">client_id</span><span class="sxs-lookup"><span data-stu-id="52784-285">client_id</span></span> | <span data-ttu-id="52784-286">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="52784-286">${aadAppId}</span></span> |
        | <span data-ttu-id="52784-287">client_secret</span><span class="sxs-lookup"><span data-stu-id="52784-287">client_secret</span></span> | <span data-ttu-id="52784-288">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="52784-288">${aadAppSecret}</span></span> |
        | <span data-ttu-id="52784-289">grant_type</span><span class="sxs-lookup"><span data-stu-id="52784-289">grant_type</span></span> | <span data-ttu-id="52784-290">client_credentials</span><span class="sxs-lookup"><span data-stu-id="52784-290">client_credentials</span></span> |
        | <span data-ttu-id="52784-291">resource</span><span class="sxs-lookup"><span data-stu-id="52784-291">resource</span></span> | <span data-ttu-id="52784-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="52784-292">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="52784-293">Yanıt olarak aşağıdaki örneğe benzeyen bir `aadToken` almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52784-293">You should receive an `aadToken` in response, which resembles the following example.</span></span>

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. <span data-ttu-id="52784-294">Aşağıdakine benzer bir JSON isteğini formülleştirin:</span><span class="sxs-lookup"><span data-stu-id="52784-294">Formulate a JSON request that resembles the following:</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    <span data-ttu-id="52784-295">Where:</span><span class="sxs-lookup"><span data-stu-id="52784-295">Where:</span></span>
    - <span data-ttu-id="52784-296">`client_assertion` değeri, önceki adımda aldığınız `aadToken` olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="52784-296">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="52784-297">`context`değeri, eklentiyi dağıtmak istediğiniz ortam kimliği olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="52784-297">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="52784-298">Diğer tüm değerleri örnekte gösterilen şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52784-298">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="52784-299">Aşağıdaki özelliklere sahip bir HTTP isteği gönderin:</span><span class="sxs-lookup"><span data-stu-id="52784-299">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="52784-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="52784-300">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="52784-301">**Yöntem** - `POST`</span><span class="sxs-lookup"><span data-stu-id="52784-301">**Method** - `POST`</span></span>
    - <span data-ttu-id="52784-302">**HTTP üst bilgisi**: API sürümünü ekleyin (anahtar: `Api-Version` ve değer: `1.0` olmalıdır)</span><span class="sxs-lookup"><span data-stu-id="52784-302">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="52784-303">**Gövde içeriği:** Önceki adımda oluşturduğunuz JSON isteğini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="52784-303">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="52784-304">Yanıt olarak bir `access_token` alırsınız.</span><span class="sxs-lookup"><span data-stu-id="52784-304">You will get an `access_token` in response.</span></span> <span data-ttu-id="52784-305">Stok Görünürlüğü API'sını çağırmak için taşıyıcı belirteç olarak ihtiyacınız olan budur.</span><span class="sxs-lookup"><span data-stu-id="52784-305">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="52784-306">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="52784-306">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a><span data-ttu-id="52784-307">Örnek İstek</span><span class="sxs-lookup"><span data-stu-id="52784-307">Sample Request</span></span>

<span data-ttu-id="52784-308">İncelemeniz için örnek bir http isteği verilmiştir. Bu isteği göndermek için herhangi bir aracı veya kodlama dilini kullanabilirsiniz (örneğin ``Postman``).</span><span class="sxs-lookup"><span data-stu-id="52784-308">For your reference, here is a sample http request, you can use any tools or coding language to send this request, such as  ``Postman``.</span></span>

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="52784-309">Stok Görünürlüğü API'sını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="52784-309">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="52784-310">Hizmeti kullanmadan önce, aşağıdaki alt bölümlerde açıklanan yapılandırmaları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52784-310">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="52784-311">Yapılandırma, ortamınızın ayrıntılarına bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="52784-311">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="52784-312">Başlıca dört bölümden oluşur:</span><span class="sxs-lookup"><span data-stu-id="52784-312">It primarily includes four parts:</span></span>

- [<span data-ttu-id="52784-313">Bölümleme</span><span class="sxs-lookup"><span data-stu-id="52784-313">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="52784-314">Boyut yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="52784-314">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="52784-315">Dizin oluşturma</span><span class="sxs-lookup"><span data-stu-id="52784-315">Indexing</span></span>](#indexing)
- [<span data-ttu-id="52784-316">Özel ölçüm</span><span class="sxs-lookup"><span data-stu-id="52784-316">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="52784-317">Bölümleme</span><span class="sxs-lookup"><span data-stu-id="52784-317">Partitioning</span></span>

<span data-ttu-id="52784-318">Bölümleme, Stok Görünürlüğü API'sının performansını önemli ölçüde etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="52784-318">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="52784-319">Anlamlı veri sorgularına izin verirken küçük veri gruplandırmalarına olanak tanıyan bir düzen tanımlamak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="52784-319">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="52784-320">`organizationId` (Supply Chain Management'ta `dataAreaId`), her zaman bölümlemenin bir parçası olacaktır ve varsayılan olarak Stok Görünürlüğü, *Tesis + Konum* olarak boyutlara göre bölümlenecek şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="52784-320">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="52784-321">Bu, hizmetin her zaman filtrelerde tanımlanan bu boyutlarla sorgulanması gerektiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="52784-321">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="52784-322">*Tesis* ve *Konum*, Stok Görünürlüğü'nde iki genel varsayılan boyuttur.</span><span class="sxs-lookup"><span data-stu-id="52784-322">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="52784-323">Supply Chain Management'ta, bu boyutlara *Tesis* (`InventSiteId`) ve *Ambar* (`InventLocationId`) adı verilir.</span><span class="sxs-lookup"><span data-stu-id="52784-323">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="52784-324">Boyut yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="52784-324">Dimension configurations</span></span>

<span data-ttu-id="52784-325">Stok Görünürlüğü, birden çok kaynağın sistem tümleştirmesini etkinleştirmek için genel varsayılan boyutların bir listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="52784-325">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="52784-326">Aşağıdaki tabloda, Stok Görünürlüğü'nde varsayılan boyut adları olacak stok boyutları listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="52784-326">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="52784-327">Boyut türü</span><span class="sxs-lookup"><span data-stu-id="52784-327">Dimension type</span></span> | <span data-ttu-id="52784-328">Boyut adı</span><span class="sxs-lookup"><span data-stu-id="52784-328">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="52784-329">Ürün</span><span class="sxs-lookup"><span data-stu-id="52784-329">Product</span></span> | `ColorId` |
| <span data-ttu-id="52784-330">Ürün</span><span class="sxs-lookup"><span data-stu-id="52784-330">Product</span></span> | `SizeId` |
| <span data-ttu-id="52784-331">Ürün</span><span class="sxs-lookup"><span data-stu-id="52784-331">Product</span></span> | `StyleId` |
| <span data-ttu-id="52784-332">Ürün</span><span class="sxs-lookup"><span data-stu-id="52784-332">Product</span></span> | `ConfigId` |
| <span data-ttu-id="52784-333">İzleme</span><span class="sxs-lookup"><span data-stu-id="52784-333">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="52784-334">İzleme</span><span class="sxs-lookup"><span data-stu-id="52784-334">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="52784-335">Yer</span><span class="sxs-lookup"><span data-stu-id="52784-335">Location</span></span> | `LocationId` |
| <span data-ttu-id="52784-336">Yer</span><span class="sxs-lookup"><span data-stu-id="52784-336">Location</span></span> | `SiteId` |
| <span data-ttu-id="52784-337">Stok Durumu</span><span class="sxs-lookup"><span data-stu-id="52784-337">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="52784-338">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="52784-338">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="52784-339">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="52784-339">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="52784-340">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="52784-340">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="52784-341">Önceki tabloda listelenen boyut türü yalnızca referans içindir.</span><span class="sxs-lookup"><span data-stu-id="52784-341">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="52784-342">Stok Görünürlüğü'nde boyut türünü tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="52784-342">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="52784-343">Özel bir boyut varsa ve Stok Görünürlüğü tarafından tüketildiğinde varsayılan değere ayarlanması gerekiyorsa Stok Görünürlüğü'nde **Özel boyut** adını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-343">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="52784-344">Harici sistemler, sorgulanacak belirli boyut kümeleri hakkında eldeki bilgilerin sorgulanmasını sağlayan RESTful API'lar aracılığıyla Stok Görünürlüğü'ne erişir.</span><span class="sxs-lookup"><span data-stu-id="52784-344">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="52784-345">Tümleştirme için Stok Görünürlüğü, *dış kanal veri kaynağını* ve kaynak boyutunu Stok Görünürlüğü'ndeki *hedef boyutlara* yapılandırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="52784-345">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="52784-346">Hedef boyutlar aşağıdakilerden biri olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="52784-346">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="52784-347">Stok Görünürlüğü'ndeki varsayılan boyutlar</span><span class="sxs-lookup"><span data-stu-id="52784-347">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="52784-348">Özel boyutlar</span><span class="sxs-lookup"><span data-stu-id="52784-348">Custom dimensions</span></span>

<span data-ttu-id="52784-349">Boyut yapılandırmasının amacı, boyutlardaki sorgular ve boyutlarla deftere nakil olayı için çoklu sistem tümleştirmesini standartlaştırmaktır.</span><span class="sxs-lookup"><span data-stu-id="52784-349">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="52784-350">Dizin oluşturma</span><span class="sxs-lookup"><span data-stu-id="52784-350">Indexing</span></span>

<span data-ttu-id="52784-351">Çoğu zaman, eldeki stok sorgusu yalnızca en yüksek "toplam" düzeyinde olmakla birlikte, sonuçları stok boyutlarına göre toplanmış olarak görmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-351">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="52784-352">Stok Görünürlüğü, boyuta veya boyutların karışımına göre dizinleri ayarlamanıza izin vererek esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="52784-352">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="52784-353">Şu anda, yalnızca en fazla beş adet dizin yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-353">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="52784-354">İş ihtiyaçlarınızı karşıladığından emin olmak için uygulamadan önce hangi boyutu veya boyut karışımını kullanacağınızı dikkatlice düşünmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="52784-354">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="52784-355">Örneğin, ürünleri aşağıdaki gibi sorgulamak istiyorsanız:</span><span class="sxs-lookup"><span data-stu-id="52784-355">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="52784-356">Kümelenmiş ürün eldeki verilerini *Renk* ve *Boyut* boyutlarına göre sorgulayın.</span><span class="sxs-lookup"><span data-stu-id="52784-356">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="52784-357">Bazı durumlarda, ürün üzerinde toplu olarak sorgu yapmak istersiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-357">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="52784-358">Aşağıdaki gibi tanımlanan iki dizininiz olur:</span><span class="sxs-lookup"><span data-stu-id="52784-358">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="52784-359">Boş köşeli ayraç, bölüm içindeki ürün kimliğine göre kümelenir.</span><span class="sxs-lookup"><span data-stu-id="52784-359">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="52784-360">Dizin oluşturma, sonuçlarınızı `groupBy` sorgu ayarına göre nasıl gruplanabileceğinizi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="52784-360">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="52784-361">Bu durumda, herhangi bir `groupBy` değeri tanımlamazsanız, toplamları `productid` değerine göre alırsınız.</span><span class="sxs-lookup"><span data-stu-id="52784-361">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="52784-362">Aksi takdirde, `groupBy=ColorId&groupBy=SizeId` olarak `groupBy` tanımlarsanız sistemde farklı renk ve boyut kombinasyonlarına dayalı olarak döndürülen birden çok satır alırsınız.</span><span class="sxs-lookup"><span data-stu-id="52784-362">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="52784-363">Sorgu ölçütlerinizi istek gövdesine koyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-363">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="52784-364">Renk ve boyut kombinasyonuna sahip ürün üzerinde gerçekleştirilen bir sorgu örneği.</span><span class="sxs-lookup"><span data-stu-id="52784-364">Here is a sample query on the product with color and size combination.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

<span data-ttu-id="52784-365">`filters` alanı için şu anda yalnızca `ProductId` birden çok değeri desteklemektedir.</span><span class="sxs-lookup"><span data-stu-id="52784-365">For the `filters` field, currently only `ProductId` supports multiple values.</span></span> <span data-ttu-id="52784-366">`ProductId` boş bir diziyse, tüm ürünler sorgulanır.</span><span class="sxs-lookup"><span data-stu-id="52784-366">If the `ProductId` is an empty array, all products will be queried.</span></span>

#### <a name="custom-measurement"></a><span data-ttu-id="52784-367">Özel ölçüm</span><span class="sxs-lookup"><span data-stu-id="52784-367">Custom measurement</span></span>

<span data-ttu-id="52784-368">Varsayılan ölçüm miktarları Supply Chain Management'a bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="52784-368">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="52784-369">Ancak varsayılan ölçümlerin birleşiminden oluşan bir miktara sahip olmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-369">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="52784-370">Bunu yapmak için eldeki sorguların çıktısına eklenecek özel miktarlar yapılandırmanız olabilir.</span><span class="sxs-lookup"><span data-stu-id="52784-370">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="52784-371">İşlev, özel ölçümü oluşturmak için eklenecek bir dizi ölçü ve/veya çıkarılacak bir dizi ölçü belirlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="52784-371">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="52784-372">Örneğin, aşağıdaki sorgu koşulunda, `MyCustomAvailableforReservation` özel ölçüm miktarını tüketim sistemi tarafından tüketilecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-372">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| <span data-ttu-id="52784-373">Tüketim sistemi</span><span class="sxs-lookup"><span data-stu-id="52784-373">Consumption system</span></span> | <span data-ttu-id="52784-374">Hesaplanan ölçümler</span><span class="sxs-lookup"><span data-stu-id="52784-374">Calculated measurers</span></span> | <span data-ttu-id="52784-375">Veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="52784-375">Data source</span></span> | <span data-ttu-id="52784-376">Değiştirici</span><span class="sxs-lookup"><span data-stu-id="52784-376">Modifier</span></span> | <span data-ttu-id="52784-377">Değiştirici hesaplama türü</span><span class="sxs-lookup"><span data-stu-id="52784-377">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="52784-378">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="52784-378">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="52784-379">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="52784-379">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="52784-380">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="52784-380">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="52784-381">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="52784-381">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="52784-382">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="52784-382">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="52784-383">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="52784-383">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="52784-384">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="52784-384">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="52784-385">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="52784-385">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="52784-386">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="52784-386">Subtraction</span></span> |

<span data-ttu-id="52784-387">Bununla, özel ölçüm miktarı üzerindeki sorgu, aşağıdaki çıktıyı döndürecektir.</span><span class="sxs-lookup"><span data-stu-id="52784-387">With that, the query on the custom measurement quantity will return the following output.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="52784-388">`MyCustomAvailableforReservation` çıktısı, aşağıdaki gibi, özel ölçümlerdeki hesaplama ayarına dayanır:</span><span class="sxs-lookup"><span data-stu-id="52784-388">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="52784-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="52784-389">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="52784-390">Eldeki değişiklikleri deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="52784-390">Posting on-hand changes</span></span>

<span data-ttu-id="52784-391">Etkinliğin yayınlanacağı URL, coğrafi bölgenize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="52784-391">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="52784-392">Şu şekilde olacaktır:</span><span class="sxs-lookup"><span data-stu-id="52784-392">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="52784-393">Kimlik doğrulaması yapıldığında, bu URL, hizmete eldeki değişiklik olaylarını göndermek için HTTP `POST` yöntemiyle birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="52784-393">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="52784-394">Dynamics 365 hizmetleriyle HTTP istekleri üzerinden iletişim kurmak için özel bir üst bilgi kullanılır ve verilerin bağlı olduğu Supply Chain Management kurulumunun ortam kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52784-394">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="52784-395">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="52784-395">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="52784-396">Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 1</span><span class="sxs-lookup"><span data-stu-id="52784-396">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="52784-397">Bu örnekte Power Apps'te boyut yapılandırmasını ayarlayacağınız bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="52784-397">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="52784-398">Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:</span><span class="sxs-lookup"><span data-stu-id="52784-398">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="52784-399">Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-399">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="52784-400">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="52784-400">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="52784-401">Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 2</span><span class="sxs-lookup"><span data-stu-id="52784-401">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="52784-402">Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="52784-402">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="52784-403">`dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="52784-403">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a><span data-ttu-id="52784-404">JSON belge alanı özellikleri</span><span class="sxs-lookup"><span data-stu-id="52784-404">JSON document field properties</span></span>

<span data-ttu-id="52784-405">Daha önce sağlanan JSON sorgu örneklerindeki alanlar aşağıdaki tabloda listelenen özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="52784-405">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="52784-406">Alan kodu</span><span class="sxs-lookup"><span data-stu-id="52784-406">Field ID</span></span> | <span data-ttu-id="52784-407">Tanım</span><span class="sxs-lookup"><span data-stu-id="52784-407">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="52784-408">Belirli bir değişiklik olayı için benzersiz bir kimlik.</span><span class="sxs-lookup"><span data-stu-id="52784-408">A unique ID for the specific change event.</span></span> <span data-ttu-id="52784-409">Bu kimlik, deftere nakil sırasında hizmetle iletişim başarısız olursa olursa olayın yeniden gönderilmesinin aynı olayın sistemde iki kez sayılmasıyla sonuçlanmamasını sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52784-409">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="52784-410">Olayla bağlantılı kuruluşun tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="52784-410">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="52784-411">Bu, Supply Chain Management kuruluşları veya veri alanı kimlikleriyle eşlenir.</span><span class="sxs-lookup"><span data-stu-id="52784-411">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="52784-412">Söz konusu ürünün tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="52784-412">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="52784-413">Eldeki miktarın değiştirilmesi gereken miktar.</span><span class="sxs-lookup"><span data-stu-id="52784-413">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="52784-414">Örneğin, bir rafa 10 yeni simit eklenseydi, bu değer 10 olur.</span><span class="sxs-lookup"><span data-stu-id="52784-414">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="52784-415">Raftan 3 simit çıkarılırsa veya satılırsa bu değer -3 olur.</span><span class="sxs-lookup"><span data-stu-id="52784-415">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="52784-416">Deftere nakil değişikliği olayı ve sorgusunda kullanılan boyutların veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="52784-416">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="52784-417">Veri kaynağını belirtirseniz belirtilen veri kaynağındaki özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-417">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="52784-418">Boyut yapılandırmasıyla, Stok Görünürlüğü özel boyutları genel varsayılan boyutlarla eşleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="52784-418">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="52784-419">`dimensionDataSource` belirtilmemişse sorgularınızda yalnızca genel varsayılan boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-419">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="52784-420">Anahtar/değer çiftlerinden oluşan dinamik bir set.</span><span class="sxs-lookup"><span data-stu-id="52784-420">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="52784-421">Bunlar Supply Chain Management'taki bazı boyutlarla eşlenir ancak olay Supply Chain Management'tan veya harici bir sistemden geliyorsa gösterebilecek özel boyutlar *(Kaynak* gibi) da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-421">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="52784-422">Mevcut eldeki miktarı sorgulama</span><span class="sxs-lookup"><span data-stu-id="52784-422">Querying current on-hand</span></span>

<span data-ttu-id="52784-423">Mevcut eldeki miktarı sorgulamak için uç noktası, benzer bir URL'ye sahip olacaktır:</span><span class="sxs-lookup"><span data-stu-id="52784-423">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="52784-424">HTTP `POST` yöntemi ile sorgulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="52784-424">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="52784-425">Geçerli eldeki miktar sorgusu örneği 1</span><span class="sxs-lookup"><span data-stu-id="52784-425">Current on-hand query example 1</span></span>

<span data-ttu-id="52784-426">Bu örnekte Power Apps'te boyut yapılandırmasını zaten tamamladığınız bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="52784-426">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="52784-427">Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:</span><span class="sxs-lookup"><span data-stu-id="52784-427">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="52784-428">Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-428">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="52784-429">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="52784-429">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="52784-430">`DimensionDataSource` değerini `filters` içinde belirtebilir ve özel boyutları hem `filters` hem de `groupByValues` ile gelirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52784-430">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="52784-431">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="52784-431">The system will automatically convert custom dimensions to base dimensions.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="52784-432">Geçerli eldeki miktar sorgusu örneği 2</span><span class="sxs-lookup"><span data-stu-id="52784-432">Current on-hand query example 2</span></span>

<span data-ttu-id="52784-433">Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="52784-433">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="52784-434">`filters` altındaki `dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="52784-434">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a><span data-ttu-id="52784-435">Örnek döndürme sonucu</span><span class="sxs-lookup"><span data-stu-id="52784-435">Example return result</span></span>

<span data-ttu-id="52784-436">Önceki örneklerde gösterilen sorgular böyle bir sonuç döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="52784-436">The queries shown in the previous examples could return a result like this.</span></span>

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

<span data-ttu-id="52784-437">Miktar alanlarının ölçümler sözlüğü ve ilişkili değerleri şeklinde yapılandırıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="52784-437">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
