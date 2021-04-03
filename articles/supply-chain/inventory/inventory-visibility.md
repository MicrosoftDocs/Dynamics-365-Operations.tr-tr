---
title: Stok Görünürlüğü Eklentisi
description: Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisinin nasıl yüklendiğini ve yapılandırıldığını açıklar.
author: sherry-zheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 4e588be2ac5aae395ca66e3c9a743a67d71db7c0
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574234"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="dab7e-103">Stok Görünürlüğü Eklentisi</span><span class="sxs-lookup"><span data-stu-id="dab7e-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="dab7e-104">Stok Görünürlüğü Eklentisi, gerçek zamanlı olarak elden stok takibi sağlayan ve böylece stok görünürlüğünün genel görünümünü sunan bağımsız ve yüksek ölçeklenebilir bir mikro hizmettir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="dab7e-105">Eldeki stokla ilgili tüm bilgiler, düşük düzeyli SQL tümleştirmesi aracılığıyla neredeyse gerçek zamanlı olarak hizmete dışarı aktarılır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="dab7e-106">Harici sistemler, verilen boyut kümeleri üzerindeki bilgileri sorgulamak için restful API'lar aracılığıyla hizmete erişir ve böylece eldeki mevcut pozisyonların bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="dab7e-107">Stok Görünürlüğü, Microsoft Dataverse üzerine kurulmuş bir mikro hizmettir; diğer bir ifadeyle, iş gereksinimlerinizi karşılamak için özelleştirilmiş işlevsellik sağlamak için Power Apps oluşturup Power BI uygulayarak genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="dab7e-108">Envanter sorguları yapmak için dizini yükseltmeniz de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="dab7e-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="dab7e-109">Stok Görünürlüğü, birden çok üçüncü taraf sistemle tümleştirmeye olanak tanıyan yapılandırma seçenekleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="dab7e-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="dab7e-110">Standartlaştırılmış stok boyutunu, özelleştirilmiş genişletilebilirliği ve standartlaştırılmış, yapılandırılabilir hesaplanmış miktarları destekler.</span><span class="sxs-lookup"><span data-stu-id="dab7e-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="dab7e-111">Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi'nin nasıl yüklenilip yapılandırılacağını ve uygulama programlama arabiriminin (API) nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="dab7e-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="dab7e-112">Stok Görünürlüğü Eklentisini Yükleme</span><span class="sxs-lookup"><span data-stu-id="dab7e-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="dab7e-113">Stok Görünürlüğü Eklentisi'ni, Microsoft Dynamics Lifecycle Services'ı (LCS) kullanarak yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="dab7e-114">LCS, Dynamics 365 Finance and Operations uygulamalarınızın uygulama yaşam döngüsünü yönetmenize yardımcı olan bir ortam ve düzenli olarak güncelleştirilen bir dizi hizmet sağlayan bir işbirliği portalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="dab7e-115">Daha fazla bilgi için bkz. [Lifecycle Services kaynakları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="dab7e-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="dab7e-116">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="dab7e-116">Prerequisites</span></span>

<span data-ttu-id="dab7e-117">Stok Görünürlüğü Eklentisi'ni yüklemeden önce aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="dab7e-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="dab7e-118">En az bir ortam dağıtılan bir LCS uygulama projesi edinin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="dab7e-119">[Eklentilere genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)'ta sağlanan eklentileri ayarlama ön koşullarının tamamlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="dab7e-119">Make sure that the prerequisites for setting up add-ins provided in the [Add-ins overview](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) have been completed.</span></span> <span data-ttu-id="dab7e-120">Stok Görünürlüğü, çift yazma bağlantısı gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="dab7e-120">Inventory Visibility doesn't require dual-write linking.</span></span>
- <span data-ttu-id="dab7e-121">Aşağıdaki üç gerekli dosyayı almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü Ekibi'ne başvurun:</span><span class="sxs-lookup"><span data-stu-id="dab7e-121">Contact the Inventory Visibility Team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the following three required files:</span></span>

    - `Inventory Visibility Dataverse Solution.zip`
    - `Inventory Visibility Configuration Trigger.zip`
    - <span data-ttu-id="dab7e-122">`Inventory Visibility Integration.zip` (Supply Chain Management'ın çalıştırdığınız bu sürümü 10.0.18 sürümünden daha eskiyse)</span><span class="sxs-lookup"><span data-stu-id="dab7e-122">`Inventory Visibility Integration.zip` (if the version of Supply Chain Management that you're running is earlier than version 10.0.18)</span></span>

> [!NOTE]
> <span data-ttu-id="dab7e-123">Şu anda desteklenen ülkeler/bölgeler arasında Kanada, ABD ve Avrupa Birliği (AB) bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-123">The currently supported countries and regions include Canada, the United States, and the European Union (EU).</span></span>

<span data-ttu-id="dab7e-124">Bu ön koşullarla ilgili herhangi bir sorunuz varsa lütfen Stok Görünürlüğü ürün takımıyla iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-124">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a><span data-ttu-id="dab7e-125">Ayarlama Dataverse</span><span class="sxs-lookup"><span data-stu-id="dab7e-125">Set up Dataverse</span></span>

<span data-ttu-id="dab7e-126">Dataverse'ü ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-126">Follow these steps to set up Dataverse.</span></span>

1. <span data-ttu-id="dab7e-127">Kiracınıza bir hizmet ilkesi ekleyin:</span><span class="sxs-lookup"><span data-stu-id="dab7e-127">Add a service principle to your tenant:</span></span>

    1. <span data-ttu-id="dab7e-128">Azure AD PowerShell Modülü v2'yi [ Graph için Azure Active Directory PowerShell'i Yüklema](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2) bölümünde açıklandığı gibi yükleyin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-128">Install Azure AD PowerShell Module v2 as described in [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
    1. <span data-ttu-id="dab7e-129">Aşağıdaki PowerShell komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-129">Run the following PowerShell command.</span></span>

        ```powershell
        Connect-AzureAD # (open a sign in window and sign in as a tenant user)

        New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
        ```

1. <span data-ttu-id="dab7e-130">Dataverse'te Stok Görünürlüğü için bir uygulama kullanıcısı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="dab7e-130">Create an application user for Inventory Visibility in Dataverse:</span></span>

    1. <span data-ttu-id="dab7e-131">Dataverse ortamınızın URL'sini açın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-131">Open the URL of your Dataverse environment.</span></span>
    1. <span data-ttu-id="dab7e-132">**Gelişmiş Ayar \> Sistem \> Güvenlik \> Kullanıcılar**'a gidin ve bir uygulama kullanıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dab7e-132">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="dab7e-133">Sayfa görünümünü **Uygulama Kullanıcıları** olarak değiştirmek için görünüm menüsünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-133">Use the view menu to change the page view to **Application Users**.</span></span>
    1. <span data-ttu-id="dab7e-134">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-134">Select **New**.</span></span> <span data-ttu-id="dab7e-135">Uygulama kimliğini *3022308a-b9bd-4a18-b8ac-2ddedb2075e1* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-135">Set the application ID to *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*.</span></span> <span data-ttu-id="dab7e-136">(Değişikliklerinizi kaydettiğinizde nesne kimliği otomatik olarak yüklenir.) Adı özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-136">(The object ID will automatically be loaded when you save your changes.) You can customize the name.</span></span> <span data-ttu-id="dab7e-137">Örneğin *Stok Görünürlüğü* olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-137">For example, you can change it to *Inventory Visibility*.</span></span> <span data-ttu-id="dab7e-138">Tamamladıktan sonra **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-138">When you've finished, select **Save**.</span></span>
    1. <span data-ttu-id="dab7e-139">**Rol Ata**'yı ve sonra **Sistem Yöneticisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-139">Select **Assign Role**, and then select **System Administrator**.</span></span> <span data-ttu-id="dab7e-140">**Common Data Service Kullanıcısı** adlı bir rol varsa onu da seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-140">If there is a role that is named **Common Data Service User**, select it too.</span></span>

    <span data-ttu-id="dab7e-141">Daha fazla bilgi için bkz. [Uygulama kullanıcısı oluşturma](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="dab7e-141">For more information, see [Create an application user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

1. <span data-ttu-id="dab7e-142">Dataverse yapılandırmasıyla ilgili varlıkları ve Power Apps'i içeren `Inventory Visibility Dataverse Solution.zip` dosyasını içeri aktarın:</span><span class="sxs-lookup"><span data-stu-id="dab7e-142">Import the `Inventory Visibility Dataverse Solution.zip` file, which includes Dataverse configuration related entities and Power Apps:</span></span>

    1. <span data-ttu-id="dab7e-143">**Çözümler** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-143">Go to the **Solutions** page.</span></span>
    1. <span data-ttu-id="dab7e-144">**İçe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-144">Select **Import**.</span></span>

1. <span data-ttu-id="dab7e-145">Yapılandırma yükseltme tetikleyici akışını içeri aktarın:</span><span class="sxs-lookup"><span data-stu-id="dab7e-145">Import the configuration upgrade trigger flow:</span></span>

    1. <span data-ttu-id="dab7e-146">Microsoft Flow sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-146">Go to the Microsoft Flow page.</span></span>
    1. <span data-ttu-id="dab7e-147">*Dataverse (eski)* olarak adlandırılan bağlantının mevcut olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="dab7e-147">Make sure that the connection that is named *Dataverse (legacy)* exists.</span></span> <span data-ttu-id="dab7e-148">(Yoksa oluşturun.)</span><span class="sxs-lookup"><span data-stu-id="dab7e-148">(If it doesn't exist, create it.)</span></span>
    1. <span data-ttu-id="dab7e-149">`Inventory Visibility Configuration Trigger.zip` dosyasını içeri aktarın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-149">Import the `Inventory Visibility Configuration Trigger.zip` file.</span></span> <span data-ttu-id="dab7e-150">İçeri aktarıldıktan sonra tetikleyici **Akışlarım** altında görünecektir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-150">After it's imported, the trigger will appear under **My flows**.</span></span>
    1. <span data-ttu-id="dab7e-151">Ortam bilgilerine bağlı olarak aşağıdaki dört değişkeni başlatın:</span><span class="sxs-lookup"><span data-stu-id="dab7e-151">Initialize the following four variables, based on the environment information:</span></span>

        - <span data-ttu-id="dab7e-152">Azure Kiracısı Kimliği</span><span class="sxs-lookup"><span data-stu-id="dab7e-152">Azure Tenant ID</span></span>
        - <span data-ttu-id="dab7e-153">Azure Uygulaması İstemci Kimliği</span><span class="sxs-lookup"><span data-stu-id="dab7e-153">Azure Application Client ID</span></span>
        - <span data-ttu-id="dab7e-154">Azure Uygulaması Gizli Anahtarı</span><span class="sxs-lookup"><span data-stu-id="dab7e-154">Azure Application Client Secret</span></span>
        - <span data-ttu-id="dab7e-155">Stok Görünürlüğü Uç Noktası</span><span class="sxs-lookup"><span data-stu-id="dab7e-155">Inventory Visibility Endpoint</span></span>

            <span data-ttu-id="dab7e-156">Bu değişken hakkında daha fazla bilgi için bu konuda ele alınacak olan [Stok Görünürlüğü tümleştirmesini ayarlama](#setup-inventory-visibility-integration) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-156">For more information about this variable, see the [Set up Inventory Visibility integration](#setup-inventory-visibility-integration) section later in this topic.</span></span>

        <span data-ttu-id="dab7e-157">![Yapılandırma tetikleyicisi](media/configuration-trigger.png "Yapılandırma tetikleyicisi")</span><span class="sxs-lookup"><span data-stu-id="dab7e-157">![Configuration trigger](media/configuration-trigger.png "Configuration trigger")</span></span>

    1. <span data-ttu-id="dab7e-158">**Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-158">Select **Turn on**.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="dab7e-159">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="dab7e-159">Install the add-in</span></span>

<span data-ttu-id="dab7e-160">Stok Görünürlüğü Eklentisi'ni yüklemek için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="dab7e-160">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="dab7e-161">[Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portalında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-161">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="dab7e-162">Ana sayfada, ortamınızın dağıtıldığı projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-162">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="dab7e-163">Proje sayfasında, eklentiyi yüklemek istediğiniz ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-163">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="dab7e-164">Ortam sayfasında, **Power Platform tümleştirmesi** bölümünde Dataverse ortamı adını bulabileceğiniz **Ortam eklentileri** bölümünü görene kadar aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-164">On the environment page, scroll down until you see the **Environment add-ins** section in the **Power Platform integration** section, where you can find the Dataverse environment name.</span></span>
1. <span data-ttu-id="dab7e-165">**Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-165">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>

    <span data-ttu-id="dab7e-166">![LCS'deki ortam sayfası](media/inventory-visibility-environment.png "LCS'deki ortam sayfası")</span><span class="sxs-lookup"><span data-stu-id="dab7e-166">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>

1. <span data-ttu-id="dab7e-167">**Yeni eklenti yükleyin** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-167">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="dab7e-168">Kullanılabilir eklentilerin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-168">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="dab7e-169">Listeden **Stok Görünürlüğü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-169">Select **Inventory Visibility** in the list.</span></span>
1. <span data-ttu-id="dab7e-170">Ortamınızın aşağıdaki alanlarının değerlerini girin:</span><span class="sxs-lookup"><span data-stu-id="dab7e-170">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="dab7e-171">**AAD uygulaması (istemci) kimliği**</span><span class="sxs-lookup"><span data-stu-id="dab7e-171">**AAD application (client) ID**</span></span>
    - <span data-ttu-id="dab7e-172">**AAD kiracı kimliği**</span><span class="sxs-lookup"><span data-stu-id="dab7e-172">**AAD tenant ID**</span></span>

    <span data-ttu-id="dab7e-173">![Eklenti kurulum sayfası](media/inventory-visibility-setup.png "Eklenti kurulum sayfası")</span><span class="sxs-lookup"><span data-stu-id="dab7e-173">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="dab7e-174">**Şartlar ve koşullar** onay kutusunu seçerek şartlar ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-174">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="dab7e-175">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-175">Select **Install**.</span></span> <span data-ttu-id="dab7e-176">Eklentinin durumu **Yükleniyor** olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="dab7e-176">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="dab7e-177">İşlem bittiğinde, durumun **Yüklendi** olarak değiştiğini görmek için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-177">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a><span data-ttu-id="dab7e-178">Eklentiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="dab7e-178">Uninstall the add-in</span></span>

<span data-ttu-id="dab7e-179">Eklentiyi kaldırmak için **Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-179">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="dab7e-180">LCS'yi yenilediğinizde Stok Görünürlüğü Eklentisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-180">When you refresh LCS, the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="dab7e-181">Kaldırma işlemi eklenti kaydını kaldırır ve hizmette depolanan tüm iş verilerini temizlemek için bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-181">The uninstall process removes the add-in registration and also starts a job to clean up all the business data that is stored in the service.</span></span>

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a><span data-ttu-id="dab7e-182">Supply Chain Management'tak eldeki stok verilerini kullanma</span><span class="sxs-lookup"><span data-stu-id="dab7e-182">Consume on-hand inventory data from Supply Chain Management</span></span>

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a><span data-ttu-id="dab7e-183">Stok Görünürlüğü tümleştirme paketini dağıtma</span><span class="sxs-lookup"><span data-stu-id="dab7e-183">Deploy the Inventory Visibility integration package</span></span>

<span data-ttu-id="dab7e-184">Supply Chain Management sürüm 10.0.17 veya önceki bir sürümünü çalıştırıyorsanız paket dosyasını almak için [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) adresinden Stok Görünürlüğü yerleşik destek ekibine başvurun.</span><span class="sxs-lookup"><span data-stu-id="dab7e-184">If you're running Supply Chain Management version 10.0.17 or earlier, contact the Inventory Visibility on-board support team at [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) to get the package file.</span></span> <span data-ttu-id="dab7e-185">Ardından LCS'de paketi dağıtın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-185">Then deploy the package in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="dab7e-186">Dağıtım sırasında bir sürüm uyuşmazlığı hatası oluşursa X++ projesini geliştirme ortamınıza el ile içeri aktarmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-186">If a version mismatch error occurs during deployment, you must manually import the X++ project into your development environment.</span></span> <span data-ttu-id="dab7e-187">Daha sonra, dağıtılabilir paketi geliştirme ortamınızda oluşturun ve üretim ortamınızda dağıtın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-187">Then create the deployable package in your development environment, and deploy it in your production environment.</span></span>
> 
> <span data-ttu-id="dab7e-188">Kod, Supply Chain Management sürüm 10.0.18'e dahildir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-188">The code is included with Supply Chain Management version 10.0.18.</span></span> <span data-ttu-id="dab7e-189">Bu sürümü veya sonraki bir sürümünü çalıştırıyorsanız dağıtım gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-189">If you're running that version or later, deployment isn't required.</span></span>

<span data-ttu-id="dab7e-190">Supply Chain Management ortamınızda aşağıdaki özelliklerin açık olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="dab7e-190">Make sure that the following features are turned on in your Supply Chain Management environment.</span></span> <span data-ttu-id="dab7e-191">(Varsayılan olarak bunlar açıktır.)</span><span class="sxs-lookup"><span data-stu-id="dab7e-191">(By default, they are turned on.)</span></span>

| <span data-ttu-id="dab7e-192">Özellik açıklaması</span><span class="sxs-lookup"><span data-stu-id="dab7e-192">Feature description</span></span> | <span data-ttu-id="dab7e-193">Kod sürümü</span><span class="sxs-lookup"><span data-stu-id="dab7e-193">Code version</span></span> | <span data-ttu-id="dab7e-194">Sınıfı değiştirme</span><span class="sxs-lookup"><span data-stu-id="dab7e-194">Toggle class</span></span> |
|---|---|---|
| <span data-ttu-id="dab7e-195">InventSum tablosunda stok boyutlarını kullanmayı etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="dab7e-195">Enable or disable using inventory dimensions on InventSum table</span></span> | <span data-ttu-id="dab7e-196">10.0.11</span><span class="sxs-lookup"><span data-stu-id="dab7e-196">10.0.11</span></span> | <span data-ttu-id="dab7e-197">InventUseDimOfInventSumToggle</span><span class="sxs-lookup"><span data-stu-id="dab7e-197">InventUseDimOfInventSumToggle</span></span> |
| <span data-ttu-id="dab7e-198">InventSumDelta tablosunda stok boyutlarını kullanmayı etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="dab7e-198">Enable or disable using inventory dimensions on InventSumDelta table</span></span> | <span data-ttu-id="dab7e-199">10.0.12</span><span class="sxs-lookup"><span data-stu-id="dab7e-199">10.0.12</span></span> | <span data-ttu-id="dab7e-200">InventUseDimOfInventSumDeltaToggle</span><span class="sxs-lookup"><span data-stu-id="dab7e-200">InventUseDimOfInventSumDeltaToggle</span></span> |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a><span data-ttu-id="dab7e-201">Stok Görünürlüğü tümleştirmesini kurma</span><span class="sxs-lookup"><span data-stu-id="dab7e-201">Set up Inventory Visibility integration</span></span>

1. <span data-ttu-id="dab7e-202">Supply Chain Management'ta **[Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** çalışma alanını açın ve **Stok Görünürlüğü Tümleştirmesi** özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-202">In Supply Chain Management, open the **[Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** workspace, and turn on the **Inventory Visibility Integration** feature.</span></span>
1. <span data-ttu-id="dab7e-203">**Stok Yönetimi \> Kurulum \> Stok Görünürlüğü Tümleştirme parametreleri**'ne gidin ve Stok Görünürlüğü'nü çalıştırdığınız ortamın URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-203">Go to **Inventory Management \> Set up \> Inventory Visibility Integration parameters**, and enter the URL of the environment where you're running Inventory Visibility.</span></span>

    <span data-ttu-id="dab7e-204">LCS ortamınızın Azure bölgesini bulun ve URL'yi girin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-204">Find your LCS environment's Azure region, and then enter the URL.</span></span> <span data-ttu-id="dab7e-205">URL aşağıdaki biçimde olur:</span><span class="sxs-lookup"><span data-stu-id="dab7e-205">The URL has the following form:</span></span>

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="dab7e-206">Örneğin, Avrupa'daysanız ortamınızda aşağıdaki URL'lerden biri bulunur:</span><span class="sxs-lookup"><span data-stu-id="dab7e-206">For example, if you're in Europe, your environment will have one of the following URLs:</span></span>

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com/`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com/`

    <span data-ttu-id="dab7e-207">Şu anda aşağıdaki bölgeler kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-207">The following regions are currently available.</span></span>

    | <span data-ttu-id="dab7e-208">Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="dab7e-208">Azure region</span></span> | <span data-ttu-id="dab7e-209">Bölge kısa adı</span><span class="sxs-lookup"><span data-stu-id="dab7e-209">Region short name</span></span> |
    |---|---|
    | <span data-ttu-id="dab7e-210">Doğu Avustralya</span><span class="sxs-lookup"><span data-stu-id="dab7e-210">Australia east</span></span> | <span data-ttu-id="dab7e-211">eau</span><span class="sxs-lookup"><span data-stu-id="dab7e-211">eau</span></span> |
    | <span data-ttu-id="dab7e-212">Güneydoğu Avustralya</span><span class="sxs-lookup"><span data-stu-id="dab7e-212">Australia southeast</span></span> | <span data-ttu-id="dab7e-213">seau</span><span class="sxs-lookup"><span data-stu-id="dab7e-213">seau</span></span> |
    | <span data-ttu-id="dab7e-214">Orta Kanada</span><span class="sxs-lookup"><span data-stu-id="dab7e-214">Canada central</span></span> | <span data-ttu-id="dab7e-215">cca</span><span class="sxs-lookup"><span data-stu-id="dab7e-215">cca</span></span> |
    | <span data-ttu-id="dab7e-216">Doğu Kanada</span><span class="sxs-lookup"><span data-stu-id="dab7e-216">Canada east</span></span> | <span data-ttu-id="dab7e-217">eca</span><span class="sxs-lookup"><span data-stu-id="dab7e-217">eca</span></span> |
    | <span data-ttu-id="dab7e-218">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="dab7e-218">North Europe</span></span> | <span data-ttu-id="dab7e-219">neu</span><span class="sxs-lookup"><span data-stu-id="dab7e-219">neu</span></span> |
    | <span data-ttu-id="dab7e-220">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="dab7e-220">West Europe</span></span> | <span data-ttu-id="dab7e-221">weu</span><span class="sxs-lookup"><span data-stu-id="dab7e-221">weu</span></span> |
    | <span data-ttu-id="dab7e-222">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="dab7e-222">East US</span></span> | <span data-ttu-id="dab7e-223">eus</span><span class="sxs-lookup"><span data-stu-id="dab7e-223">eus</span></span> |
    | <span data-ttu-id="dab7e-224">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="dab7e-224">West US</span></span> | <span data-ttu-id="dab7e-225">wus</span><span class="sxs-lookup"><span data-stu-id="dab7e-225">wus</span></span> |

1. <span data-ttu-id="dab7e-226">**Stok Yönetimi \> Periyodik \> Stok Görünürlüğü Tümleştirmesi**'ne gidin ve işi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-226">Go to **Inventory Management \> Periodic \> Inventory Visibility Integration**, and enable the job.</span></span> <span data-ttu-id="dab7e-227">Supply Chain Management'taki tüm stok değişikliği olayları artık Stok Görünürlüğü'ne nakledilecektir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-227">All inventory change events from Supply Chain Management will now be posted to Inventory Visibility.</span></span>

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a><span data-ttu-id="dab7e-228">Stok Görünürlüğü Eklentisi genel API'si</span><span class="sxs-lookup"><span data-stu-id="dab7e-228">The Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="dab7e-229">Stok Görünürlüğü Eklentisi'nin genel REST API'si, birkaç özel tümleştirme uç noktası sunar.</span><span class="sxs-lookup"><span data-stu-id="dab7e-229">The public REST API of the Inventory Visibility Add-in presents several specific endpoints for integration.</span></span> <span data-ttu-id="dab7e-230">Üç ana etkileşim türünü destekler:</span><span class="sxs-lookup"><span data-stu-id="dab7e-230">It supports three main interaction types:</span></span>

- <span data-ttu-id="dab7e-231">Harici bir sistemden eldeki stok değişiklikleri eklentiye deftere nakletmek</span><span class="sxs-lookup"><span data-stu-id="dab7e-231">Posting on-hand inventory changes to the add-in from an external system</span></span>
- <span data-ttu-id="dab7e-232">Harici bir sistemden eldeki geçerli miktarları sorgulamak</span><span class="sxs-lookup"><span data-stu-id="dab7e-232">Querying current on-hand quantities from an external system</span></span>
- <span data-ttu-id="dab7e-233">Supply Chain Management eldeki stoku ile otomatik eşitlemek</span><span class="sxs-lookup"><span data-stu-id="dab7e-233">Automatic synchronization with Supply Chain Management on-hand inventory</span></span>

<span data-ttu-id="dab7e-234">Otomatik eşitleme genel API kapsamında değildir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-234">Automatic synchronization isn't part of the public API.</span></span> <span data-ttu-id="dab7e-235">Bunun yerine, Stok Görünürlüğü Eklentisi'nin etkinleştirildiği ortamlar için arka planda işlenir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-235">Instead, it's handled in the background for environments where the Inventory Visibility Add-in is enabled.</span></span>

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a><span data-ttu-id="dab7e-236">Kimlik Doğrulama</span><span class="sxs-lookup"><span data-stu-id="dab7e-236">Authentication</span></span>

<span data-ttu-id="dab7e-237">Platform güvenlik belirteci, Stok Görünürlüğü Eklentisi'ni çağırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-237">The platform security token is used to call the Inventory Visibility Add-in.</span></span> <span data-ttu-id="dab7e-238">Bu nedenle, Azure AD uygulamanızı kullanarak bir *Azure Active Directory (Azure AD) belirteci* oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-238">Therefore, you must generate an *Azure Active Directory (Azure AD) token* by using your Azure AD application.</span></span> <span data-ttu-id="dab7e-239">Daha sonra güvenlik hizmetinden *erişim belirtecini* almak için Azure AD belirteci kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-239">You must then use the Azure AD token to get the *access token* from the security service.</span></span>

<span data-ttu-id="dab7e-240">Aşağıdakileri gerçekleştirerek güvenlik hizmeti belirteci alın:</span><span class="sxs-lookup"><span data-stu-id="dab7e-240">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="dab7e-241">Azure portalda oturum açın ve Supply Chain Management uygulamanız için `clientId` ve `clientSecret` bilgilerini bulmak için portalı kullanın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-241">Sign in to Azure portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="dab7e-242">Aşağıdaki özelliklere sahip bir HTTP isteği göndererek Azure Active Directory belirteci (`aadToken`) getirin:</span><span class="sxs-lookup"><span data-stu-id="dab7e-242">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="dab7e-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="dab7e-243">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="dab7e-244">**Yöntem** - `GET`</span><span class="sxs-lookup"><span data-stu-id="dab7e-244">**Method** - `GET`</span></span>
    - <span data-ttu-id="dab7e-245">**Gövde içeriği (form verileri)**:</span><span class="sxs-lookup"><span data-stu-id="dab7e-245">**Body content (form data)**:</span></span>

        | <span data-ttu-id="dab7e-246">key</span><span class="sxs-lookup"><span data-stu-id="dab7e-246">key</span></span> | <span data-ttu-id="dab7e-247">değer</span><span class="sxs-lookup"><span data-stu-id="dab7e-247">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="dab7e-248">client_id</span><span class="sxs-lookup"><span data-stu-id="dab7e-248">client_id</span></span> | <span data-ttu-id="dab7e-249">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="dab7e-249">${aadAppId}</span></span> |
        | <span data-ttu-id="dab7e-250">client_secret</span><span class="sxs-lookup"><span data-stu-id="dab7e-250">client_secret</span></span> | <span data-ttu-id="dab7e-251">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="dab7e-251">${aadAppSecret}</span></span> |
        | <span data-ttu-id="dab7e-252">grant_type</span><span class="sxs-lookup"><span data-stu-id="dab7e-252">grant_type</span></span> | <span data-ttu-id="dab7e-253">client_credentials</span><span class="sxs-lookup"><span data-stu-id="dab7e-253">client_credentials</span></span> |
        | <span data-ttu-id="dab7e-254">resource</span><span class="sxs-lookup"><span data-stu-id="dab7e-254">resource</span></span> | <span data-ttu-id="dab7e-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="dab7e-255">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="dab7e-256">Yanıt olarak aşağıdaki örneğe benzeyen bir `aadToken` almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-256">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="dab7e-257">Aşağıdakine benzer bir JSON isteğini formülleştirin:</span><span class="sxs-lookup"><span data-stu-id="dab7e-257">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="dab7e-258">Where:</span><span class="sxs-lookup"><span data-stu-id="dab7e-258">Where:</span></span>
    - <span data-ttu-id="dab7e-259">`client_assertion` değeri, önceki adımda aldığınız `aadToken` olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-259">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="dab7e-260">`context`değeri, eklentiyi dağıtmak istediğiniz ortam kimliği olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-260">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="dab7e-261">Diğer tüm değerleri örnekte gösterilen şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-261">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="dab7e-262">Aşağıdaki özelliklere sahip bir HTTP isteği gönderin:</span><span class="sxs-lookup"><span data-stu-id="dab7e-262">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="dab7e-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="dab7e-263">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="dab7e-264">**Yöntem** - `POST`</span><span class="sxs-lookup"><span data-stu-id="dab7e-264">**Method** - `POST`</span></span>
    - <span data-ttu-id="dab7e-265">**HTTP üst bilgisi**: API sürümünü ekleyin (anahtar: `Api-Version` ve değer: `1.0` olmalıdır)</span><span class="sxs-lookup"><span data-stu-id="dab7e-265">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="dab7e-266">**Gövde içeriği:** Önceki adımda oluşturduğunuz JSON isteğini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="dab7e-266">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="dab7e-267">Yanıt olarak bir `access_token` alırsınız.</span><span class="sxs-lookup"><span data-stu-id="dab7e-267">You will get an `access_token` in response.</span></span> <span data-ttu-id="dab7e-268">Stok Görünürlüğü API'sını çağırmak için taşıyıcı belirteç olarak ihtiyacınız olan budur.</span><span class="sxs-lookup"><span data-stu-id="dab7e-268">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="dab7e-269">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-269">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a><span data-ttu-id="dab7e-270">Stok Görünürlüğü API'sını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="dab7e-270">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="dab7e-271">Hizmeti kullanmadan önce, aşağıdaki alt bölümlerde açıklanan yapılandırmaları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-271">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="dab7e-272">Yapılandırma, ortamınızın ayrıntılarına bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-272">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="dab7e-273">Başlıca dört bölümden oluşur:</span><span class="sxs-lookup"><span data-stu-id="dab7e-273">It primarily includes four parts:</span></span>

- [<span data-ttu-id="dab7e-274">Bölümleme</span><span class="sxs-lookup"><span data-stu-id="dab7e-274">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="dab7e-275">Boyut yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="dab7e-275">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="dab7e-276">Dizin oluşturma</span><span class="sxs-lookup"><span data-stu-id="dab7e-276">Indexing</span></span>](#indexing)
- [<span data-ttu-id="dab7e-277">Özel ölçüm</span><span class="sxs-lookup"><span data-stu-id="dab7e-277">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="dab7e-278">Bölümleme</span><span class="sxs-lookup"><span data-stu-id="dab7e-278">Partitioning</span></span>

<span data-ttu-id="dab7e-279">Bölümleme, Stok Görünürlüğü API'sının performansını önemli ölçüde etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-279">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="dab7e-280">Anlamlı veri sorgularına izin verirken küçük veri gruplandırmalarına olanak tanıyan bir düzen tanımlamak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-280">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="dab7e-281">`organizationId` (Supply Chain Management'ta `dataAreaId`), her zaman bölümlemenin bir parçası olacaktır ve varsayılan olarak Stok Görünürlüğü, *Tesis + Konum* olarak boyutlara göre bölümlenecek şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-281">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="dab7e-282">Bu, hizmetin her zaman filtrelerde tanımlanan bu boyutlarla sorgulanması gerektiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-282">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="dab7e-283">*Tesis* ve *Konum*, Stok Görünürlüğü'nde iki genel varsayılan boyuttur.</span><span class="sxs-lookup"><span data-stu-id="dab7e-283">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="dab7e-284">Supply Chain Management'ta, bu boyutlara *Tesis* (`InventSiteId`) ve *Ambar* (`InventLocationId`) adı verilir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-284">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="dab7e-285">Boyut yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="dab7e-285">Dimension configurations</span></span>

<span data-ttu-id="dab7e-286">Stok Görünürlüğü, birden çok kaynağın sistem tümleştirmesini etkinleştirmek için genel varsayılan boyutların bir listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="dab7e-286">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="dab7e-287">Aşağıdaki tabloda, Stok Görünürlüğü'nde varsayılan boyut adları olacak stok boyutları listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-287">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="dab7e-288">Boyut türü</span><span class="sxs-lookup"><span data-stu-id="dab7e-288">Dimension type</span></span> | <span data-ttu-id="dab7e-289">Boyut adı</span><span class="sxs-lookup"><span data-stu-id="dab7e-289">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="dab7e-290">Ürün</span><span class="sxs-lookup"><span data-stu-id="dab7e-290">Product</span></span> | `ColorId` |
| <span data-ttu-id="dab7e-291">Ürün</span><span class="sxs-lookup"><span data-stu-id="dab7e-291">Product</span></span> | `SizeId` |
| <span data-ttu-id="dab7e-292">Ürün</span><span class="sxs-lookup"><span data-stu-id="dab7e-292">Product</span></span> | `StyleId` |
| <span data-ttu-id="dab7e-293">Ürün</span><span class="sxs-lookup"><span data-stu-id="dab7e-293">Product</span></span> | `ConfigId` |
| <span data-ttu-id="dab7e-294">İzleme</span><span class="sxs-lookup"><span data-stu-id="dab7e-294">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="dab7e-295">İzleme</span><span class="sxs-lookup"><span data-stu-id="dab7e-295">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="dab7e-296">Yer</span><span class="sxs-lookup"><span data-stu-id="dab7e-296">Location</span></span> | `LocationId` |
| <span data-ttu-id="dab7e-297">Yer</span><span class="sxs-lookup"><span data-stu-id="dab7e-297">Location</span></span> | `SiteId` |
| <span data-ttu-id="dab7e-298">Stok Durumu</span><span class="sxs-lookup"><span data-stu-id="dab7e-298">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="dab7e-299">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="dab7e-299">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="dab7e-300">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="dab7e-300">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="dab7e-301">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="dab7e-301">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="dab7e-302">Önceki tabloda listelenen boyut türü yalnızca referans içindir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-302">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="dab7e-303">Stok Görünürlüğü'nde boyut türünü tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="dab7e-303">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="dab7e-304">Özel bir boyut varsa ve Stok Görünürlüğü tarafından tüketildiğinde varsayılan değere ayarlanması gerekiyorsa Stok Görünürlüğü'nde **Özel boyut** adını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-304">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="dab7e-305">Harici sistemler, sorgulanacak belirli boyut kümeleri hakkında eldeki bilgilerin sorgulanmasını sağlayan RESTful API'lar aracılığıyla Stok Görünürlüğü'ne erişir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-305">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="dab7e-306">Tümleştirme için Stok Görünürlüğü, *dış kanal veri kaynağını* ve kaynak boyutunu Stok Görünürlüğü'ndeki *hedef boyutlara* yapılandırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="dab7e-306">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="dab7e-307">Hedef boyutlar aşağıdakilerden biri olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="dab7e-307">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="dab7e-308">Stok Görünürlüğü'ndeki varsayılan boyutlar</span><span class="sxs-lookup"><span data-stu-id="dab7e-308">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="dab7e-309">Özel boyutlar</span><span class="sxs-lookup"><span data-stu-id="dab7e-309">Custom dimensions</span></span>

<span data-ttu-id="dab7e-310">Boyut yapılandırmasının amacı, boyutlardaki sorgular ve boyutlarla deftere nakil olayı için çoklu sistem tümleştirmesini standartlaştırmaktır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-310">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="dab7e-311">Dizin oluşturma</span><span class="sxs-lookup"><span data-stu-id="dab7e-311">Indexing</span></span>

<span data-ttu-id="dab7e-312">Çoğu zaman, eldeki stok sorgusu yalnızca en yüksek "toplam" düzeyinde olmakla birlikte, sonuçları stok boyutlarına göre toplanmış olarak görmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-312">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="dab7e-313">Stok Görünürlüğü, boyuta veya boyutların karışımına göre dizinleri ayarlamanıza izin vererek esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="dab7e-313">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="dab7e-314">Şu anda, yalnızca en fazla beş adet dizin yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-314">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="dab7e-315">İş ihtiyaçlarınızı karşıladığından emin olmak için uygulamadan önce hangi boyutu veya boyut karışımını kullanacağınızı dikkatlice düşünmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-315">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="dab7e-316">Örneğin, ürünleri aşağıdaki gibi sorgulamak istiyorsanız:</span><span class="sxs-lookup"><span data-stu-id="dab7e-316">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="dab7e-317">Kümelenmiş ürün eldeki verilerini *Renk* ve *Boyut* boyutlarına göre sorgulayın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-317">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="dab7e-318">Bazı durumlarda, ürün üzerinde toplu olarak sorgu yapmak istersiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-318">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="dab7e-319">Aşağıdaki gibi tanımlanan iki dizininiz olur:</span><span class="sxs-lookup"><span data-stu-id="dab7e-319">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="dab7e-320">Boş köşeli ayraç, bölüm içindeki ürün kimliğine göre kümelenir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-320">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="dab7e-321">Dizin oluşturma, sonuçlarınızı `groupBy` sorgu ayarına göre nasıl gruplanabileceğinizi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="dab7e-321">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="dab7e-322">Bu durumda, herhangi bir `groupBy` değeri tanımlamazsanız, toplamları `productid` değerine göre alırsınız.</span><span class="sxs-lookup"><span data-stu-id="dab7e-322">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="dab7e-323">Aksi takdirde, `groupBy=ColorId&groupBy=SizeId` olarak `groupBy` tanımlarsanız sistemde farklı renk ve boyut kombinasyonlarına dayalı olarak döndürülen birden çok satır alırsınız.</span><span class="sxs-lookup"><span data-stu-id="dab7e-323">Otherwise, if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="dab7e-324">Sorgu ölçütlerinizi istek gövdesine koyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-324">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="dab7e-325">Renk ve boyut kombinasyonuna sahip ürün üzerinde gerçekleştirilen bir sorgu örneği.</span><span class="sxs-lookup"><span data-stu-id="dab7e-325">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="dab7e-326">Özel ölçüm</span><span class="sxs-lookup"><span data-stu-id="dab7e-326">Custom measurement</span></span>

<span data-ttu-id="dab7e-327">Varsayılan ölçüm miktarları Supply Chain Management'a bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-327">The default measurement quantities are linked to Supply Chain Management.</span></span> <span data-ttu-id="dab7e-328">Ancak varsayılan ölçümlerin birleşiminden oluşan bir miktara sahip olmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-328">However, you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="dab7e-329">Bunu yapmak için eldeki sorguların çıktısına eklenecek özel miktarlar yapılandırmanız olabilir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-329">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="dab7e-330">İşlev, özel ölçümü oluşturmak için eklenecek bir dizi ölçü ve/veya çıkarılacak bir dizi ölçü belirlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-330">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="dab7e-331">Örneğin, aşağıdaki sorgu koşulunda, `MyCustomAvailableforReservation` özel ölçüm miktarını tüketim sistemi tarafından tüketilecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-331">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="dab7e-332">Tüketim sistemi</span><span class="sxs-lookup"><span data-stu-id="dab7e-332">Consumption system</span></span> | <span data-ttu-id="dab7e-333">Hesaplanan ölçümler</span><span class="sxs-lookup"><span data-stu-id="dab7e-333">Calculated measurers</span></span> | <span data-ttu-id="dab7e-334">Veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="dab7e-334">Data source</span></span> | <span data-ttu-id="dab7e-335">Değiştirici</span><span class="sxs-lookup"><span data-stu-id="dab7e-335">Modifier</span></span> | <span data-ttu-id="dab7e-336">Değiştirici hesaplama türü</span><span class="sxs-lookup"><span data-stu-id="dab7e-336">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="dab7e-337">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="dab7e-337">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="dab7e-338">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="dab7e-338">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="dab7e-339">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="dab7e-339">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="dab7e-340">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="dab7e-340">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="dab7e-341">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="dab7e-341">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="dab7e-342">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="dab7e-342">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="dab7e-343">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="dab7e-343">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="dab7e-344">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="dab7e-344">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="dab7e-345">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="dab7e-345">Subtraction</span></span> |

<span data-ttu-id="dab7e-346">Bununla, özel ölçüm miktarı üzerindeki sorgu, aşağıdaki çıktıyı döndürecektir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-346">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="dab7e-347">`MyCustomAvailableforReservation` çıktısı, aşağıdaki gibi, özel ölçümlerdeki hesaplama ayarına dayanır:</span><span class="sxs-lookup"><span data-stu-id="dab7e-347">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="dab7e-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="dab7e-348">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="dab7e-349">Eldeki değişiklikleri deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="dab7e-349">Posting on-hand changes</span></span>

<span data-ttu-id="dab7e-350">Etkinliğin yayınlanacağı URL, coğrafi bölgenize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-350">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="dab7e-351">Şu şekilde olacaktır:</span><span class="sxs-lookup"><span data-stu-id="dab7e-351">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="dab7e-352">Kimlik doğrulaması yapıldığında, bu URL, hizmete eldeki değişiklik olaylarını göndermek için HTTP `POST` yöntemiyle birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-352">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="dab7e-353">Dynamics 365 hizmetleriyle HTTP istekleri üzerinden iletişim kurmak için özel bir üst bilgi kullanılır ve verilerin bağlı olduğu Supply Chain Management kurulumunun ortam kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-353">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="dab7e-354">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="dab7e-354">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="dab7e-355">Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 1</span><span class="sxs-lookup"><span data-stu-id="dab7e-355">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="dab7e-356">Bu örnekte Power Apps'te boyut yapılandırmasını ayarlayacağınız bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-356">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="dab7e-357">Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:</span><span class="sxs-lookup"><span data-stu-id="dab7e-357">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="dab7e-358">Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-358">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="dab7e-359">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="dab7e-359">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="dab7e-360">Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 2</span><span class="sxs-lookup"><span data-stu-id="dab7e-360">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="dab7e-361">Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-361">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="dab7e-362">`dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-362">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="dab7e-363">JSON belge alanı özellikleri</span><span class="sxs-lookup"><span data-stu-id="dab7e-363">JSON document field properties</span></span>

<span data-ttu-id="dab7e-364">Daha önce sağlanan JSON sorgu örneklerindeki alanlar aşağıdaki tabloda listelenen özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-364">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="dab7e-365">Alan kodu</span><span class="sxs-lookup"><span data-stu-id="dab7e-365">Field ID</span></span> | <span data-ttu-id="dab7e-366">Tanım</span><span class="sxs-lookup"><span data-stu-id="dab7e-366">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="dab7e-367">Belirli bir değişiklik olayı için benzersiz bir kimlik.</span><span class="sxs-lookup"><span data-stu-id="dab7e-367">A unique ID for the specific change event.</span></span> <span data-ttu-id="dab7e-368">Bu kimlik, deftere nakil sırasında hizmetle iletişim başarısız olursa olursa olayın yeniden gönderilmesinin aynı olayın sistemde iki kez sayılmasıyla sonuçlanmamasını sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-368">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="dab7e-369">Olayla bağlantılı kuruluşun tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="dab7e-369">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="dab7e-370">Bu, Supply Chain Management kuruluşları veya veri alanı kimlikleriyle eşlenir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-370">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="dab7e-371">Söz konusu ürünün tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="dab7e-371">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="dab7e-372">Eldeki miktarın değiştirilmesi gereken miktar.</span><span class="sxs-lookup"><span data-stu-id="dab7e-372">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="dab7e-373">Örneğin, bir rafa 10 yeni simit eklenseydi, bu değer 10 olur.</span><span class="sxs-lookup"><span data-stu-id="dab7e-373">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="dab7e-374">Raftan 3 simit çıkarılırsa veya satılırsa bu değer -3 olur.</span><span class="sxs-lookup"><span data-stu-id="dab7e-374">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="dab7e-375">Deftere nakil değişikliği olayı ve sorgusunda kullanılan boyutların veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="dab7e-375">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="dab7e-376">Veri kaynağını belirtirseniz belirtilen veri kaynağındaki özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-376">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="dab7e-377">Boyut yapılandırmasıyla, Stok Görünürlüğü özel boyutları genel varsayılan boyutlarla eşleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-377">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="dab7e-378">`dimensionDataSource` belirtilmemişse sorgularınızda yalnızca genel varsayılan boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-378">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="dab7e-379">Anahtar/değer çiftlerinden oluşan dinamik bir set.</span><span class="sxs-lookup"><span data-stu-id="dab7e-379">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="dab7e-380">Bunlar Supply Chain Management'taki bazı boyutlarla eşlenir ancak olay Supply Chain Management'tan veya harici bir sistemden geliyorsa gösterebilecek özel boyutlar *(Kaynak* gibi) da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-380">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="dab7e-381">Mevcut eldeki miktarı sorgulama</span><span class="sxs-lookup"><span data-stu-id="dab7e-381">Querying current on-hand</span></span>

<span data-ttu-id="dab7e-382">Mevcut eldeki miktarı sorgulamak için uç noktası, benzer bir URL'ye sahip olacaktır:</span><span class="sxs-lookup"><span data-stu-id="dab7e-382">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="dab7e-383">HTTP `POST` yöntemi ile sorgulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-383">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="dab7e-384">Geçerli eldeki miktar sorgusu örneği 1</span><span class="sxs-lookup"><span data-stu-id="dab7e-384">Current on-hand query example 1</span></span>

<span data-ttu-id="dab7e-385">Bu örnekte Power Apps'te boyut yapılandırmasını zaten tamamladığınız bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-385">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="dab7e-386">Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:</span><span class="sxs-lookup"><span data-stu-id="dab7e-386">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="dab7e-387">Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-387">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="dab7e-388">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="dab7e-388">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="dab7e-389">`DimensionDataSource` değerini `filters` içinde belirtebilir ve özel boyutları hem `filters` hem de `groupByValues` ile gelirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab7e-389">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="dab7e-390">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="dab7e-390">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="dab7e-391">Geçerli eldeki miktar sorgusu örneği 2</span><span class="sxs-lookup"><span data-stu-id="dab7e-391">Current on-hand query example 2</span></span>

<span data-ttu-id="dab7e-392">Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-392">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="dab7e-393">`filters` altındaki `dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dab7e-393">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="dab7e-394">Örnek döndürme sonucu</span><span class="sxs-lookup"><span data-stu-id="dab7e-394">Example return result</span></span>

<span data-ttu-id="dab7e-395">Önceki örneklerde gösterilen sorgular böyle bir sonuç döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="dab7e-395">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="dab7e-396">Miktar alanlarının ölçümler sözlüğü ve ilişkili değerleri şeklinde yapılandırıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="dab7e-396">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
