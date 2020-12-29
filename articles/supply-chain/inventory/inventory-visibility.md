---
title: Stok Görünürlüğü Eklentisi
description: Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisinin nasıl yüklendiğini ve yapılandırıldığını açıklar.
author: chuzheng
manager: tfehr
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 2976153a6a7e4b4130e8f7673ed128945aeabf65
ms.sourcegitcommit: 03c2e1717b31e4c17ee7bb9004d2ba8cf379a036
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/24/2020
ms.locfileid: "4625077"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="501cc-103">Stok Görünürlüğü Eklentisi</span><span class="sxs-lookup"><span data-stu-id="501cc-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="501cc-104">Stok Görünürlüğü Eklentisi, gerçek zamanlı olarak elden stok takibi sağlayan ve böylece stok görünürlüğünün genel görünümünü sunan bağımsız ve yüksek ölçeklenebilir bir mikro hizmettir.</span><span class="sxs-lookup"><span data-stu-id="501cc-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="501cc-105">Eldeki stokla ilgili tüm bilgiler, düşük düzeyli SQL tümleştirmesi aracılığıyla neredeyse gerçek zamanlı olarak hizmete dışarı aktarılır.</span><span class="sxs-lookup"><span data-stu-id="501cc-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="501cc-106">Harici sistemler, verilen boyut kümeleri üzerindeki bilgileri sorgulamak için restful API'lar aracılığıyla hizmete erişir ve böylece eldeki mevcut pozisyonların bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="501cc-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="501cc-107">Stok Görünürlüğü, Common Data Service üzerine kurulmuş bir mikro hizmettir; yani, iş gereksinimlerinizi karşılamak için özelleştirilmiş işlevsellik sağlamak için Power Apps oluşturup Power BI uygulayarak genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-107">Inventory Visibility is a microservice built on the Common Data Service, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="501cc-108">Envanter sorguları yapmak için dizini yükseltmeniz de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="501cc-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="501cc-109">Stok Görünürlüğü, birden çok üçüncü taraf sistemle tümleştirmeye olanak tanıyan yapılandırma seçenekleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="501cc-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="501cc-110">Standartlaştırılmış stok boyutunu, özelleştirilmiş genişletilebilirliği ve standartlaştırılmış, yapılandırılabilir hesaplanmış miktarları destekler.</span><span class="sxs-lookup"><span data-stu-id="501cc-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="501cc-111">Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi'nin nasıl yüklenilip yapılandırılacağını ve uygulama programlama arabiriminin (API) nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="501cc-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="501cc-112">Stok Görünürlüğü Eklentisini Yükleme</span><span class="sxs-lookup"><span data-stu-id="501cc-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="501cc-113">Stok Görünürlüğü Eklentisi'ni, Microsoft Dynamics Lifecycle Services'ı (LCS) kullanarak yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="501cc-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="501cc-114">LCS, Dynamics 365 Finance and Operations uygulamalarınızın uygulama yaşam döngüsünü yönetmenize yardımcı olan bir ortam ve düzenli olarak güncelleştirilen bir dizi hizmet sağlayan bir işbirliği portalıdır.</span><span class="sxs-lookup"><span data-stu-id="501cc-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="501cc-115">Daha fazla bilgi için bkz. [Lifecycle Services kaynakları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="501cc-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="501cc-116">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="501cc-116">Prerequisites</span></span>

<span data-ttu-id="501cc-117">Stok Görünürlüğü Eklentisi'ni yüklemeden önce aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="501cc-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="501cc-118">En az bir ortam dağıtılan bir LCS uygulama projesi edinin.</span><span class="sxs-lookup"><span data-stu-id="501cc-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="501cc-119">LCS'de sunduklarınız için beta anahtarlarını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="501cc-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="501cc-120">LCS'de kullanıcınız için sunduğunuz beta anahtarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="501cc-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="501cc-121">Microsoft Stok Görünürlüğü ürün takımına başvurun ve Stok Görünürlüğü Eklentisi'ni dağıtmak istediğiniz ortamın kimliği sağlayın.</span><span class="sxs-lookup"><span data-stu-id="501cc-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="501cc-122">Bu ön koşullarla ilgili herhangi bir sorunuz varsa lütfen Stok Görünürlüğü ürün takımıyla iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="501cc-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="501cc-123">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="501cc-123">Install the add-in</span></span>

<span data-ttu-id="501cc-124">Stok Görünürlüğü Eklentisi'ni yüklemek için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="501cc-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="501cc-125">[Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portalında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="501cc-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="501cc-126">Ana sayfada, ortamınızın dağıtıldığı projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="501cc-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="501cc-127">Proje sayfasında, eklentiyi yüklemek istediğiniz ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="501cc-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="501cc-128">Ortam sayfasında, **Ortam eklentileri** bölümünü görene kadar aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="501cc-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="501cc-129">Bölüm görünmüyorsa, ön koşuldaki beta anahtarlarının tam olarak işlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="501cc-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="501cc-130">**Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="501cc-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="501cc-131">![LCS'deki ortam sayfası](media/inventory-visibility-environment.png "LCS'deki ortam sayfası")</span><span class="sxs-lookup"><span data-stu-id="501cc-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="501cc-132">**Yeni eklenti yükleyin** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="501cc-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="501cc-133">Kullanılabilir eklentilerin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="501cc-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="501cc-134">Listeden **Stok hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="501cc-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="501cc-135">(Not: Bu çözüm artık **Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi** olarak listelenmiş olabilir.)</span><span class="sxs-lookup"><span data-stu-id="501cc-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="501cc-136">Ortamınızın aşağıdaki alanlarının değerlerini girin:</span><span class="sxs-lookup"><span data-stu-id="501cc-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="501cc-137">**AAD uygulama kodu**</span><span class="sxs-lookup"><span data-stu-id="501cc-137">**AAD application ID**</span></span>
    - <span data-ttu-id="501cc-138">**AAD kiracı kimliği**</span><span class="sxs-lookup"><span data-stu-id="501cc-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="501cc-139">![Eklenti kurulum sayfası](media/inventory-visibility-setup.png "Eklenti kurulum sayfası")</span><span class="sxs-lookup"><span data-stu-id="501cc-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="501cc-140">**Şartlar ve koşullar** onay kutusunu seçerek şartlar ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="501cc-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="501cc-141">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="501cc-141">Select **Install**.</span></span> <span data-ttu-id="501cc-142">Eklentinin durumu **Yükleniyor** olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="501cc-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="501cc-143">İşlem bittiğinde, durumun **Yüklendi** olarak değiştiğini görmek için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="501cc-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="501cc-144">Güvenlik hizmeti belirteci alma</span><span class="sxs-lookup"><span data-stu-id="501cc-144">Get a security service token</span></span>

<span data-ttu-id="501cc-145">Güvenlik hizmeti belirteci almak için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="501cc-145">To get a security service token, do the following:</span></span>

1. <span data-ttu-id="501cc-146">`aadToken` alın ve uç noktasına çağrı yapın: https://securityservice.operations365.dynamics.com/token.</span><span class="sxs-lookup"><span data-stu-id="501cc-146">Get your `aadToken` and call the endpoint: https://securityservice.operations365.dynamics.com/token.</span></span>
1. <span data-ttu-id="501cc-147">Gövdedeki `client_assertion` değerini `aadToken` ile değiştirin.</span><span class="sxs-lookup"><span data-stu-id="501cc-147">Replace the `client_assertion` in the body with your `aadToken`.</span></span>
1. <span data-ttu-id="501cc-148">Gövdedeki bağlamı eklentiyi dağıtmak istediğiniz ortamla değiştirin.</span><span class="sxs-lookup"><span data-stu-id="501cc-148">Replace the context in the body with the environment where you want to deploy the add-in.</span></span>
1. <span data-ttu-id="501cc-149">Gövdedeki kapsamı aşağıdakilerle değiştirin:</span><span class="sxs-lookup"><span data-stu-id="501cc-149">Replace the scope in the body with the following:</span></span>

    - <span data-ttu-id="501cc-150">MCK kapsamı - "https://inventoryservice.operations365.dynamics.cn/.default"</span><span class="sxs-lookup"><span data-stu-id="501cc-150">Scope for MCK - "https://inventoryservice.operations365.dynamics.cn/.default"</span></span>  
    <span data-ttu-id="501cc-151">(MCK için Azure Active Directory uygulama kimliği ve kiracı kimliğini `appsettings.mck.json` dosyasında bulabilirsiniz.)</span><span class="sxs-lookup"><span data-stu-id="501cc-151">(You can find the Azure Active Directory application ID and tenant ID for MCK in `appsettings.mck.json`.)</span></span>
    - <span data-ttu-id="501cc-152">PROD kapsamı - "https://inventoryservice.operations365.dynamics.com/.default"</span><span class="sxs-lookup"><span data-stu-id="501cc-152">Scope for PROD - "https://inventoryservice.operations365.dynamics.com/.default"</span></span>  
    <span data-ttu-id="501cc-153">(PROD için Azure Active Directory uygulama kimliği ve kiracı kimliğini `appsettings.prod.json` dosyasında bulabilirsiniz.)</span><span class="sxs-lookup"><span data-stu-id="501cc-153">(You can find the Azure Active Directory application ID and tenant ID for PROD in `appsettings.prod.json`.)</span></span>

    <span data-ttu-id="501cc-154">Sonuç, aşağıdaki örneğe benzeyecektir.</span><span class="sxs-lookup"><span data-stu-id="501cc-154">The result should resemble the following example.</span></span>

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{**Your_AADToken**}",
        "scope":"**https://inventoryservice.operations365.dynamics.com/.default**",
        "context": "**5dbf6cc8-255e-4de2-8a25-2101cd5649b4**",
        "context_type": "finops-env"
    }
    ```

1. <span data-ttu-id="501cc-155">Yanıt olarak bir `access_token` alırsınız.</span><span class="sxs-lookup"><span data-stu-id="501cc-155">You will get an `access_token` in response.</span></span> <span data-ttu-id="501cc-156">Stok Görünürlüğü API'sını çağırmak için taşıyıcı belirteç olarak ihtiyacınız olan budur.</span><span class="sxs-lookup"><span data-stu-id="501cc-156">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="501cc-157">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="501cc-157">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="501cc-158">Eklentiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="501cc-158">Uninstall the add-in</span></span>

<span data-ttu-id="501cc-159">Eklentiyi kaldırmak için **Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="501cc-159">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="501cc-160">LCS'yi yenilediğinizde Stok Görünürlüğü Eklentisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="501cc-160">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="501cc-161">Kaldırma işlemi eklenti kaydını kaldırır ve hizmette depolanan tüm iş verilerini temizlemek için bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="501cc-161">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="501cc-162">Stok Görünürlüğü Eklentisi genel API'sı</span><span class="sxs-lookup"><span data-stu-id="501cc-162">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="501cc-163">Stok Görünürlüğü Eklentisi'nin genel REST API'sı, birkaç özel tümleştirme uç noktası sunar.</span><span class="sxs-lookup"><span data-stu-id="501cc-163">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="501cc-164">Üç ana etkileşim türünü destekler:</span><span class="sxs-lookup"><span data-stu-id="501cc-164">It supports three main interaction types:</span></span>

- <span data-ttu-id="501cc-165">Harici bir sistemden eldeki değişiklikleri eklentiye deftere nakletmek.</span><span class="sxs-lookup"><span data-stu-id="501cc-165">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="501cc-166">Harici bir sistemden eldeki geçerli miktarları sorgulamak.</span><span class="sxs-lookup"><span data-stu-id="501cc-166">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="501cc-167">Eldeki Supply Chain Management ile otomatik eşitleme.</span><span class="sxs-lookup"><span data-stu-id="501cc-167">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="501cc-168">Otomatik eşitleme, genel API'nın bir parçası değildir ancak Stok Görünürlüğü Eklentisi'ni etkinleştiren ortamlar için arka planda işlenir.</span><span class="sxs-lookup"><span data-stu-id="501cc-168">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="501cc-169">Kimlik Doğrulama</span><span class="sxs-lookup"><span data-stu-id="501cc-169">Authentication</span></span>

<span data-ttu-id="501cc-170">Platform güvenlik belirteci, Stok Görünürlüğü Eklentisi'ni çağırmak için kullanılır, bu nedenle Azure Active Directory uygulamanızı kullanarak bir Azure Active Directory belirteci oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="501cc-170">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="501cc-171">Güvenlik belirtecini alma hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü Eklentisi'ni Yükleme](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="501cc-171">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="501cc-172">Stok Görünürlüğü API'sını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="501cc-172">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="501cc-173">Hizmeti kullanmadan önce, aşağıdaki alt bölümlerde açıklanan yapılandırmaları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="501cc-173">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="501cc-174">Yapılandırma, ortamınızın ayrıntılarına bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="501cc-174">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="501cc-175">Başlıca dört bölümden oluşur:</span><span class="sxs-lookup"><span data-stu-id="501cc-175">It primarily includes four parts:</span></span>

- [<span data-ttu-id="501cc-176">Bölümleme</span><span class="sxs-lookup"><span data-stu-id="501cc-176">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="501cc-177">Boyut yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="501cc-177">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="501cc-178">Dizin oluşturma</span><span class="sxs-lookup"><span data-stu-id="501cc-178">Indexing</span></span>](#indexing)
- [<span data-ttu-id="501cc-179">Özel ölçüm</span><span class="sxs-lookup"><span data-stu-id="501cc-179">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="501cc-180">Bölümleme</span><span class="sxs-lookup"><span data-stu-id="501cc-180">Partitioning</span></span>

<span data-ttu-id="501cc-181">Bölümleme, Stok Görünürlüğü API'sının performansını önemli ölçüde etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="501cc-181">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="501cc-182">Anlamlı veri sorgularına izin verirken küçük veri gruplandırmalarına olanak tanıyan bir düzen tanımlamak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="501cc-182">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="501cc-183">`organizationId` (Supply Chain Management'ta `dataAreaId`), her zaman bölümlemenin bir parçası olacaktır ve varsayılan olarak Stok Görünürlüğü, *Tesis + Konum* olarak boyutlara göre bölümlenecek şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="501cc-183">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="501cc-184">Bu, hizmetin her zaman filtrelerde tanımlanan bu boyutlarla sorgulanması gerektiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="501cc-184">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="501cc-185">*Tesis* ve *Konum*, Stok Görünürlüğü'nde iki genel varsayılan boyuttur.</span><span class="sxs-lookup"><span data-stu-id="501cc-185">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="501cc-186">Supply Chain Management'ta, bu boyutlara *Tesis* (`InventSiteId`) ve *Ambar* (`InventLocationId`) adı verilir.</span><span class="sxs-lookup"><span data-stu-id="501cc-186">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="501cc-187">Boyut yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="501cc-187">Dimension configurations</span></span>

<span data-ttu-id="501cc-188">Stok Görünürlüğü, birden çok kaynağın sistem tümleştirmesini etkinleştirmek için genel varsayılan boyutların bir listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="501cc-188">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="501cc-189">Aşağıdaki tabloda, Stok Görünürlüğü'nde varsayılan boyut adları olacak stok boyutları listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="501cc-189">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="501cc-190">Boyut türü</span><span class="sxs-lookup"><span data-stu-id="501cc-190">Dimension type</span></span> | <span data-ttu-id="501cc-191">Boyut adı</span><span class="sxs-lookup"><span data-stu-id="501cc-191">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="501cc-192">Ürün</span><span class="sxs-lookup"><span data-stu-id="501cc-192">Product</span></span> | `ColorId` |
| <span data-ttu-id="501cc-193">Ürün</span><span class="sxs-lookup"><span data-stu-id="501cc-193">Product</span></span> | `SizeId` |
| <span data-ttu-id="501cc-194">Ürün</span><span class="sxs-lookup"><span data-stu-id="501cc-194">Product</span></span> | `StyleId` |
| <span data-ttu-id="501cc-195">Ürün</span><span class="sxs-lookup"><span data-stu-id="501cc-195">Product</span></span> | `ConfigId` |
| <span data-ttu-id="501cc-196">İzleme</span><span class="sxs-lookup"><span data-stu-id="501cc-196">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="501cc-197">İzleme</span><span class="sxs-lookup"><span data-stu-id="501cc-197">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="501cc-198">Yer</span><span class="sxs-lookup"><span data-stu-id="501cc-198">Location</span></span> | `LocationId` |
| <span data-ttu-id="501cc-199">Yer</span><span class="sxs-lookup"><span data-stu-id="501cc-199">Location</span></span> | `SiteId` |
| <span data-ttu-id="501cc-200">Stok Durumu</span><span class="sxs-lookup"><span data-stu-id="501cc-200">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="501cc-201">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="501cc-201">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="501cc-202">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="501cc-202">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="501cc-203">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="501cc-203">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="501cc-204">Önceki tabloda listelenen boyut türü yalnızca referans içindir.</span><span class="sxs-lookup"><span data-stu-id="501cc-204">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="501cc-205">Stok Görünürlüğü'nde boyut türünü tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="501cc-205">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="501cc-206">Özel bir boyut varsa ve Stok Görünürlüğü tarafından tüketildiğinde varsayılan değere ayarlanması gerekiyorsa Stok Görünürlüğü'nde **Özel boyut** adını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-206">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="501cc-207">Harici sistemler, sorgulanacak belirli boyut kümeleri hakkında eldeki bilgilerin sorgulanmasını sağlayan RESTful API'lar aracılığıyla Stok Görünürlüğü'ne erişir.</span><span class="sxs-lookup"><span data-stu-id="501cc-207">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="501cc-208">Tümleştirme için Stok Görünürlüğü, *dış kanal veri kaynağını* ve kaynak boyutunu Stok Görünürlüğü'ndeki *hedef boyutlara* yapılandırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="501cc-208">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="501cc-209">Hedef boyutlar aşağıdakilerden biri olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="501cc-209">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="501cc-210">Stok Görünürlüğü'ndeki varsayılan boyutlar</span><span class="sxs-lookup"><span data-stu-id="501cc-210">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="501cc-211">Özel boyutlar</span><span class="sxs-lookup"><span data-stu-id="501cc-211">Custom dimensions</span></span>

<span data-ttu-id="501cc-212">Boyut yapılandırmasının amacı, boyutlardaki sorgular ve boyutlarla deftere nakil olayı için çoklu sistem tümleştirmesini standartlaştırmaktır.</span><span class="sxs-lookup"><span data-stu-id="501cc-212">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="501cc-213">Dizin oluşturma</span><span class="sxs-lookup"><span data-stu-id="501cc-213">Indexing</span></span>

<span data-ttu-id="501cc-214">Çoğu zaman, eldeki stok sorgusu yalnızca en yüksek "toplam" düzeyinde olmakla birlikte, sonuçları stok boyutlarına göre toplanmış olarak görmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-214">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="501cc-215">Stok Görünürlüğü, boyuta veya boyutların karışımına göre dizinleri ayarlamanıza izin vererek esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="501cc-215">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="501cc-216">Şu anda, yalnızca en fazla beş adet dizin yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-216">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="501cc-217">İş ihtiyaçlarınızı karşıladığından emin olmak için uygulamadan önce hangi boyutu veya boyut karışımını kullanacağınızı dikkatlice düşünmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="501cc-217">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="501cc-218">Örneğin, ürünleri aşağıdaki gibi sorgulamak istiyorsanız:</span><span class="sxs-lookup"><span data-stu-id="501cc-218">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="501cc-219">Kümelenmiş ürün eldeki verilerini *Renk* ve *Boyut* boyutlarına göre sorgulayın.</span><span class="sxs-lookup"><span data-stu-id="501cc-219">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="501cc-220">Bazı durumlarda, ürün üzerinde toplu olarak sorgu yapmak istersiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-220">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="501cc-221">Aşağıdaki gibi tanımlanan iki dizininiz olur:</span><span class="sxs-lookup"><span data-stu-id="501cc-221">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="501cc-222">Boş köşeli ayraç, bölüm içindeki ürün kimliğine göre kümelenir.</span><span class="sxs-lookup"><span data-stu-id="501cc-222">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="501cc-223">Dizin oluşturma, sonuçlarınızı `groupBy` sorgu ayarına göre nasıl gruplanabileceğinizi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="501cc-223">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="501cc-224">Bu durumda, herhangi bir `groupBy` değeri tanımlamazsanız, toplamları `productid` değerine göre alırsınız.</span><span class="sxs-lookup"><span data-stu-id="501cc-224">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="501cc-225">Aksi takdirde, `groupBy=ColorId&groupBy=SizeId` olarak `groupBy` tanımlarsanız sistemde farklı renk ve boyut kombinasyonlarına dayalı olarak döndürülen birden çok satır alırsınız.</span><span class="sxs-lookup"><span data-stu-id="501cc-225">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="501cc-226">Sorgu ölçütlerinizi istek gövdesine koyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-226">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="501cc-227">Renk ve boyut kombinasyonuna sahip ürün üzerinde gerçekleştirilen bir sorgu örneği.</span><span class="sxs-lookup"><span data-stu-id="501cc-227">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="501cc-228">Özel ölçüm</span><span class="sxs-lookup"><span data-stu-id="501cc-228">Custom measurement</span></span>

<span data-ttu-id="501cc-229">Varsayılan ölçüm miktarları Supply Chain Management'a bağlıdır, ancak varsayılan ölçümlerin bir karışımından oluşan bir miktara sahip olmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-229">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="501cc-230">Bunu yapmak için eldeki sorguların çıktısına eklenecek özel miktarlar yapılandırmanız olabilir.</span><span class="sxs-lookup"><span data-stu-id="501cc-230">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="501cc-231">İşlev, özel ölçümü oluşturmak için eklenecek bir dizi ölçü ve/veya çıkarılacak bir dizi ölçü belirlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="501cc-231">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="501cc-232">Örneğin, aşağıdaki sorgu koşulunda, `MyCustomAvailableforReservation` özel ölçüm miktarını tüketim sistemi tarafından tüketilecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-232">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="501cc-233">Tüketim sistemi</span><span class="sxs-lookup"><span data-stu-id="501cc-233">Consumption system</span></span> | <span data-ttu-id="501cc-234">Hesaplanan ölçümler</span><span class="sxs-lookup"><span data-stu-id="501cc-234">Calculated measurers</span></span> | <span data-ttu-id="501cc-235">Veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="501cc-235">Data source</span></span> | <span data-ttu-id="501cc-236">Değiştirici</span><span class="sxs-lookup"><span data-stu-id="501cc-236">Modifier</span></span> | <span data-ttu-id="501cc-237">Değiştirici hesaplama türü</span><span class="sxs-lookup"><span data-stu-id="501cc-237">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="501cc-238">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="501cc-238">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="501cc-239">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="501cc-239">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="501cc-240">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="501cc-240">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="501cc-241">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="501cc-241">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="501cc-242">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="501cc-242">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="501cc-243">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="501cc-243">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="501cc-244">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="501cc-244">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="501cc-245">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="501cc-245">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="501cc-246">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="501cc-246">Subtraction</span></span> |

<span data-ttu-id="501cc-247">Bununla, özel ölçüm miktarı üzerindeki sorgu, aşağıdaki çıktıyı döndürecektir.</span><span class="sxs-lookup"><span data-stu-id="501cc-247">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="501cc-248">`MyCustomAvailableforReservation` çıktısı, aşağıdaki gibi, özel ölçümlerdeki hesaplama ayarına dayanır:</span><span class="sxs-lookup"><span data-stu-id="501cc-248">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="501cc-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="501cc-249">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="501cc-250">Eldeki değişiklikleri deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="501cc-250">Posting on-hand changes</span></span>

<span data-ttu-id="501cc-251">Etkinliğin yayınlanacağı URL, coğrafi bölgenize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="501cc-251">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="501cc-252">Şu şekilde olacaktır:</span><span class="sxs-lookup"><span data-stu-id="501cc-252">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="501cc-253">Kimlik doğrulaması yapıldığında, bu URL, hizmete eldeki değişiklik olaylarını göndermek için HTTP `POST` yöntemiyle birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="501cc-253">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="501cc-254">Dynamics 365 hizmetleriyle HTTP istekleri üzerinden iletişim kurmak için özel bir üst bilgi kullanılır ve verilerin bağlı olduğu Supply Chain Management kurulumunun ortam kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="501cc-254">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="501cc-255">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="501cc-255">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="501cc-256">Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 1</span><span class="sxs-lookup"><span data-stu-id="501cc-256">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="501cc-257">Bu örnekte Power Apps'te boyut yapılandırmasını ayarlayacağınız bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="501cc-257">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="501cc-258">Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:</span><span class="sxs-lookup"><span data-stu-id="501cc-258">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="501cc-259">Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-259">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="501cc-260">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="501cc-260">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="501cc-261">Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 2</span><span class="sxs-lookup"><span data-stu-id="501cc-261">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="501cc-262">Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="501cc-262">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="501cc-263">`dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="501cc-263">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="501cc-264">JSON belge alanı özellikleri</span><span class="sxs-lookup"><span data-stu-id="501cc-264">JSON document field properties</span></span>

<span data-ttu-id="501cc-265">Daha önce sağlanan JSON sorgu örneklerindeki alanlar aşağıdaki tabloda listelenen özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="501cc-265">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="501cc-266">Alan kodu</span><span class="sxs-lookup"><span data-stu-id="501cc-266">Field ID</span></span> | <span data-ttu-id="501cc-267">Tanım</span><span class="sxs-lookup"><span data-stu-id="501cc-267">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="501cc-268">Belirli bir değişiklik olayı için benzersiz bir kimlik.</span><span class="sxs-lookup"><span data-stu-id="501cc-268">A unique ID for the specific change event.</span></span> <span data-ttu-id="501cc-269">Bu kimlik, deftere nakil sırasında hizmetle iletişim başarısız olursa olursa olayın yeniden gönderilmesinin aynı olayın sistemde iki kez sayılmasıyla sonuçlanmamasını sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="501cc-269">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="501cc-270">Olayla bağlantılı kuruluşun tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="501cc-270">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="501cc-271">Bu, Supply Chain Management kuruluşları veya veri alanı kimlikleriyle eşlenir.</span><span class="sxs-lookup"><span data-stu-id="501cc-271">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="501cc-272">Söz konusu ürünün tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="501cc-272">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="501cc-273">Eldeki miktarın değiştirilmesi gereken miktar.</span><span class="sxs-lookup"><span data-stu-id="501cc-273">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="501cc-274">Örneğin, bir rafa 10 yeni simit eklenseydi, bu değer 10 olur.</span><span class="sxs-lookup"><span data-stu-id="501cc-274">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="501cc-275">Raftan 3 simit çıkarılırsa veya satılırsa bu değer -3 olur.</span><span class="sxs-lookup"><span data-stu-id="501cc-275">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="501cc-276">Deftere nakil değişikliği olayı ve sorgusunda kullanılan boyutların veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="501cc-276">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="501cc-277">Veri kaynağını belirtirseniz belirtilen veri kaynağındaki özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-277">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="501cc-278">Boyut yapılandırmasıyla, Stok Görünürlüğü özel boyutları genel varsayılan boyutlarla eşleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="501cc-278">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="501cc-279">`dimensionDataSource` belirtilmemişse sorgularınızda yalnızca genel varsayılan boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-279">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="501cc-280">Anahtar/değer çiftlerinden oluşan dinamik bir set.</span><span class="sxs-lookup"><span data-stu-id="501cc-280">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="501cc-281">Bunlar Supply Chain Management'taki bazı boyutlarla eşlenir ancak olay Supply Chain Management'tan veya harici bir sistemden geliyorsa gösterebilecek özel boyutlar *(Kaynak* gibi) da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-281">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="501cc-282">Mevcut eldeki miktarı sorgulama</span><span class="sxs-lookup"><span data-stu-id="501cc-282">Querying current on-hand</span></span>

<span data-ttu-id="501cc-283">Mevcut eldeki miktarı sorgulamak için uç noktası, benzer bir URL'ye sahip olacaktır:</span><span class="sxs-lookup"><span data-stu-id="501cc-283">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="501cc-284">HTTP `POST` yöntemi ile sorgulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="501cc-284">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="501cc-285">Geçerli eldeki miktar sorgusu örneği 1</span><span class="sxs-lookup"><span data-stu-id="501cc-285">Current on-hand query example 1</span></span>

<span data-ttu-id="501cc-286">Bu örnekte Power Apps'te boyut yapılandırmasını zaten tamamladığınız bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="501cc-286">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="501cc-287">Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:</span><span class="sxs-lookup"><span data-stu-id="501cc-287">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="501cc-288">Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-288">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="501cc-289">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="501cc-289">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="501cc-290">`DimensionDataSource` değerini `filters` içinde belirtebilir ve özel boyutları hem `filters` hem de `groupByValues` ile gelirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="501cc-290">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="501cc-291">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="501cc-291">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="501cc-292">Geçerli eldeki miktar sorgusu örneği 2</span><span class="sxs-lookup"><span data-stu-id="501cc-292">Current on-hand query example 2</span></span>

<span data-ttu-id="501cc-293">Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="501cc-293">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="501cc-294">`filters` altındaki `dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="501cc-294">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="501cc-295">Örnek döndürme sonucu</span><span class="sxs-lookup"><span data-stu-id="501cc-295">Example return result</span></span>

<span data-ttu-id="501cc-296">Önceki örneklerde gösterilen sorgular böyle bir sonuç döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="501cc-296">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="501cc-297">Miktar alanlarının ölçümler sözlüğü ve ilişkili değerleri şeklinde yapılandırıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="501cc-297">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
