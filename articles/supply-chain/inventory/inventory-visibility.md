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
ms.openlocfilehash: 4e6f7e0a3978bbf7e520f8cbcfd27c4cfe507777
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114682"
---
# <a name="inventory-visibility-add-in"></a><span data-ttu-id="8be0f-103">Stok Görünürlüğü Eklentisi</span><span class="sxs-lookup"><span data-stu-id="8be0f-103">Inventory Visibility Add-in</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

<span data-ttu-id="8be0f-104">Stok Görünürlüğü Eklentisi, gerçek zamanlı olarak elden stok takibi sağlayan ve böylece stok görünürlüğünün genel görünümünü sunan bağımsız ve yüksek ölçeklenebilir bir mikro hizmettir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-104">The Inventory Visibility Add-in is an independent and highly scalable microservice that enables real-time on-hand inventory tracking, thus providing a global view of inventory visibility.</span></span>

<span data-ttu-id="8be0f-105">Eldeki stokla ilgili tüm bilgiler, düşük düzeyli SQL tümleştirmesi aracılığıyla neredeyse gerçek zamanlı olarak hizmete dışarı aktarılır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-105">All information that relates to on-hand inventory is exported to the service in near real-time through low-level SQL integration.</span></span> <span data-ttu-id="8be0f-106">Harici sistemler, verilen boyut kümeleri üzerindeki bilgileri sorgulamak için restful API'lar aracılığıyla hizmete erişir ve böylece eldeki mevcut pozisyonların bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-106">External systems access the service through RESTful APIs to query on-hand information on given sets of dimensions, thus retrieving a list of available on-hand positions.</span></span>

<span data-ttu-id="8be0f-107">Stok Görünürlüğü, Microsoft Dataverse üzerine kurulmuş bir mikro hizmettir; diğer bir ifadeyle, iş gereksinimlerinizi karşılamak için özelleştirilmiş işlevsellik sağlamak için Power Apps oluşturup Power BI uygulayarak genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-107">Inventory Visibility is a microservice built on Microsoft Dataverse, which means you can extend it by building Power Apps and applying Power BI to provide customized functionality to meet your business requirements.</span></span> <span data-ttu-id="8be0f-108">Envanter sorguları yapmak için dizini yükseltmeniz de mümkündür.</span><span class="sxs-lookup"><span data-stu-id="8be0f-108">It is also possible to upgrade the index to do inventory queries.</span></span>

<span data-ttu-id="8be0f-109">Stok Görünürlüğü, birden çok üçüncü taraf sistemle tümleştirmeye olanak tanıyan yapılandırma seçenekleri sağlar.</span><span class="sxs-lookup"><span data-stu-id="8be0f-109">Inventory Visibility provides configuration options that let it integrate with multiple third-party systems.</span></span> <span data-ttu-id="8be0f-110">Standartlaştırılmış stok boyutunu, özelleştirilmiş genişletilebilirliği ve standartlaştırılmış, yapılandırılabilir hesaplanmış miktarları destekler.</span><span class="sxs-lookup"><span data-stu-id="8be0f-110">It supports the standardized inventory dimension, customized extensibility, and standardized, configurable calculated quantities.</span></span>

<span data-ttu-id="8be0f-111">Bu konu, Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi'nin nasıl yüklenilip yapılandırılacağını ve uygulama programlama arabiriminin (API) nasıl kullanılacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="8be0f-111">This topic describes how to install and configure the Inventory Visibility Add-in for Dynamics 365 Supply Chain Management, and how to use its application programming interface (API).</span></span>

## <a name="install-the-inventory-visibility-add-in"></a><span data-ttu-id="8be0f-112">Stok Görünürlüğü Eklentisini Yükleme</span><span class="sxs-lookup"><span data-stu-id="8be0f-112">Install the Inventory Visibility Add-in</span></span>

<span data-ttu-id="8be0f-113">Stok Görünürlüğü Eklentisi'ni, Microsoft Dynamics Lifecycle Services'ı (LCS) kullanarak yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-113">You need to install the Inventory Visibility Add-in using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8be0f-114">LCS, Dynamics 365 Finance and Operations uygulamalarınızın uygulama yaşam döngüsünü yönetmenize yardımcı olan bir ortam ve düzenli olarak güncelleştirilen bir dizi hizmet sağlayan bir işbirliği portalıdır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-114">LCS is a collaboration portal that provides an environment and a set of regularly updated services that help you manage the application lifecycle of your Dynamics 365 Finance and Operations apps.</span></span>

<span data-ttu-id="8be0f-115">Daha fazla bilgi için bkz. [Lifecycle Services kaynakları](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span><span class="sxs-lookup"><span data-stu-id="8be0f-115">For more information, see [Lifecycle Services resources](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="8be0f-116">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="8be0f-116">Prerequisites</span></span>

<span data-ttu-id="8be0f-117">Stok Görünürlüğü Eklentisi'ni yüklemeden önce aşağıdakileri yapmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="8be0f-117">Before you install the Inventory Visibility Add-in, you must do the following:</span></span>

- <span data-ttu-id="8be0f-118">En az bir ortam dağıtılan bir LCS uygulama projesi edinin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-118">Obtain an LCS implementation project with at least one environment deployed.</span></span>
- <span data-ttu-id="8be0f-119">LCS'de sunduklarınız için beta anahtarlarını oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8be0f-119">Generate the beta keys for your offering in LCS.</span></span>
- <span data-ttu-id="8be0f-120">LCS'de kullanıcınız için sunduğunuz beta anahtarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-120">Enable the beta keys for your offering for your user in LCS.</span></span>
- <span data-ttu-id="8be0f-121">Microsoft Stok Görünürlüğü ürün takımına başvurun ve Stok Görünürlüğü Eklentisi'ni dağıtmak istediğiniz ortamın kimliği sağlayın.</span><span class="sxs-lookup"><span data-stu-id="8be0f-121">Contact the Microsoft Inventory Visibility product team and provide an environment ID where you want to deploy the Inventory Visibility Add-in.</span></span>

<span data-ttu-id="8be0f-122">Bu ön koşullarla ilgili herhangi bir sorunuz varsa lütfen Stok Görünürlüğü ürün takımıyla iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-122">If you have any questions about these prerequisites, please contact the Inventory Visibility product team.</span></span>

### <a name="install-the-add-in"></a><a name="install-add-in"></a><span data-ttu-id="8be0f-123">Eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="8be0f-123">Install the add-in</span></span>

<span data-ttu-id="8be0f-124">Stok Görünürlüğü Eklentisi'ni yüklemek için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="8be0f-124">To install the Inventory Visibility Add-in, do the following:</span></span>

1. <span data-ttu-id="8be0f-125">[Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portalında oturum açın.</span><span class="sxs-lookup"><span data-stu-id="8be0f-125">Sign in to the [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) portal.</span></span>
1. <span data-ttu-id="8be0f-126">Ana sayfada, ortamınızın dağıtıldığı projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-126">On the home page, select the project where your environment is deployed.</span></span>
1. <span data-ttu-id="8be0f-127">Proje sayfasında, eklentiyi yüklemek istediğiniz ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-127">On the project page, select the environment where you want to install the add-in.</span></span>
1. <span data-ttu-id="8be0f-128">Ortam sayfasında, **Ortam eklentileri** bölümünü görene kadar aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="8be0f-128">On the environment page, scroll down until you see the **Environment add-ins** section.</span></span> <span data-ttu-id="8be0f-129">Bölüm görünmüyorsa, ön koşuldaki beta anahtarlarının tam olarak işlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="8be0f-129">If the section isn't visible, make sure the prerequisite beta keys have been fully processed.</span></span>
1. <span data-ttu-id="8be0f-130">**Ortam eklentileri** bölümünde, **Yeni bir eklenti yükleyin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-130">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
    <span data-ttu-id="8be0f-131">![LCS'deki ortam sayfası](media/inventory-visibility-environment.png "LCS'deki ortam sayfası")</span><span class="sxs-lookup"><span data-stu-id="8be0f-131">![The environment page in LCS](media/inventory-visibility-environment.png "The environment page in LCS")</span></span>
1. <span data-ttu-id="8be0f-132">**Yeni eklenti yükleyin** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-132">Select the **Install a new add-in** link.</span></span> <span data-ttu-id="8be0f-133">Kullanılabilir eklentilerin bir listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-133">A list of available add-ins opens.</span></span>
1. <span data-ttu-id="8be0f-134">Listeden **Stok hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-134">Select **Inventory service** from the list.</span></span> <span data-ttu-id="8be0f-135">(Not: Bu çözüm artık **Dynamics 365 Supply Chain Management için Stok Görünürlüğü Eklentisi** olarak listelenmiş olabilir.)</span><span class="sxs-lookup"><span data-stu-id="8be0f-135">(Note, this may now be listed as **Inventory Visibility Add-in for Dynamics 365 Supply Chain Management**.)</span></span>
1. <span data-ttu-id="8be0f-136">Ortamınızın aşağıdaki alanlarının değerlerini girin:</span><span class="sxs-lookup"><span data-stu-id="8be0f-136">Enter values for the following fields for your environment:</span></span>

    - <span data-ttu-id="8be0f-137">**AAD uygulama kodu**</span><span class="sxs-lookup"><span data-stu-id="8be0f-137">**AAD application ID**</span></span>
    - <span data-ttu-id="8be0f-138">**AAD kiracı kimliği**</span><span class="sxs-lookup"><span data-stu-id="8be0f-138">**AAD tenant ID**</span></span>

    <span data-ttu-id="8be0f-139">![Eklenti kurulum sayfası](media/inventory-visibility-setup.png "Eklenti kurulum sayfası")</span><span class="sxs-lookup"><span data-stu-id="8be0f-139">![Add in setup page](media/inventory-visibility-setup.png "Add-in setup page")</span></span>

1. <span data-ttu-id="8be0f-140">**Şartlar ve koşullar** onay kutusunu seçerek şartlar ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-140">Agree to the terms and condition by selecting the **Terms and conditions** check box.</span></span>
1. <span data-ttu-id="8be0f-141">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-141">Select **Install**.</span></span> <span data-ttu-id="8be0f-142">Eklentinin durumu **Yükleniyor** olarak görünür.</span><span class="sxs-lookup"><span data-stu-id="8be0f-142">The status of the add-in will show as **Installing**.</span></span> <span data-ttu-id="8be0f-143">İşlem bittiğinde, durumun **Yüklendi** olarak değiştiğini görmek için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-143">When it's done, refresh the page to see the status change to **Installed**.</span></span>

### <a name="get-a-security-service-token"></a><span data-ttu-id="8be0f-144">Güvenlik hizmeti belirteci alma</span><span class="sxs-lookup"><span data-stu-id="8be0f-144">Get a security service token</span></span>

<span data-ttu-id="8be0f-145">Aşağıdakileri gerçekleştirerek güvenlik hizmeti belirteci alın:</span><span class="sxs-lookup"><span data-stu-id="8be0f-145">Get a security service token by doing the following:</span></span>

1. <span data-ttu-id="8be0f-146">Azure portalında oturum açın ve Supply Chain Management uygulamanız için `clientId` ve `clientSecret` öğelerini bulurken bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="8be0f-146">Sign in to Azure Portal and use it to find the `clientId` and `clientSecret` for your Supply Chain Management application.</span></span>
1. <span data-ttu-id="8be0f-147">Aşağıdaki özelliklere sahip bir HTTP isteği göndererek Azure Active Directory belirteci (`aadToken`) getirin:</span><span class="sxs-lookup"><span data-stu-id="8be0f-147">Fetch an Azure Active Directory token (`aadToken`) by submitting an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="8be0f-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span><span class="sxs-lookup"><span data-stu-id="8be0f-148">**URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`</span></span>
    - <span data-ttu-id="8be0f-149">**Yöntem** - `GET`</span><span class="sxs-lookup"><span data-stu-id="8be0f-149">**Method** - `GET`</span></span>
    - <span data-ttu-id="8be0f-150">**Gövde içeriği (form verileri)**:</span><span class="sxs-lookup"><span data-stu-id="8be0f-150">**Body content (form data)**:</span></span>

        | <span data-ttu-id="8be0f-151">key</span><span class="sxs-lookup"><span data-stu-id="8be0f-151">key</span></span> | <span data-ttu-id="8be0f-152">değer</span><span class="sxs-lookup"><span data-stu-id="8be0f-152">value</span></span> |
        | --- | --- |
        | <span data-ttu-id="8be0f-153">client_id</span><span class="sxs-lookup"><span data-stu-id="8be0f-153">client_id</span></span> | <span data-ttu-id="8be0f-154">${aadAppId}</span><span class="sxs-lookup"><span data-stu-id="8be0f-154">${aadAppId}</span></span> |
        | <span data-ttu-id="8be0f-155">client_secret</span><span class="sxs-lookup"><span data-stu-id="8be0f-155">client_secret</span></span> | <span data-ttu-id="8be0f-156">${aadAppSecret}</span><span class="sxs-lookup"><span data-stu-id="8be0f-156">${aadAppSecret}</span></span> |
        | <span data-ttu-id="8be0f-157">grant_type</span><span class="sxs-lookup"><span data-stu-id="8be0f-157">grant_type</span></span> | <span data-ttu-id="8be0f-158">client_credentials</span><span class="sxs-lookup"><span data-stu-id="8be0f-158">client_credentials</span></span> |
        | <span data-ttu-id="8be0f-159">resource</span><span class="sxs-lookup"><span data-stu-id="8be0f-159">resource</span></span> | <span data-ttu-id="8be0f-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="8be0f-160">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
1. <span data-ttu-id="8be0f-161">Yanıt olarak aşağıdaki örneğe benzeyen bir `aadToken` almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-161">You should receive an `aadToken` in response, which resembles the following example.</span></span>

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

1. <span data-ttu-id="8be0f-162">Aşağıdakine benzer bir JSON isteğini formülleştirin:</span><span class="sxs-lookup"><span data-stu-id="8be0f-162">Formulate a JSON request that resembles the following:</span></span>

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

    <span data-ttu-id="8be0f-163">Where:</span><span class="sxs-lookup"><span data-stu-id="8be0f-163">Where:</span></span>
    - <span data-ttu-id="8be0f-164">`client_assertion` değeri, önceki adımda aldığınız `aadToken` olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-164">The `client_assertion` value must be the `aadToken` you received in the previous step.</span></span>
    - <span data-ttu-id="8be0f-165">`context`değeri, eklentiyi dağıtmak istediğiniz ortam kimliği olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-165">The `context` value must be the environment ID where you want to deploy the add-in.</span></span>
    - <span data-ttu-id="8be0f-166">Diğer tüm değerleri örnekte gösterilen şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8be0f-166">Set all of other values as shown in the example.</span></span>

1. <span data-ttu-id="8be0f-167">Aşağıdaki özelliklere sahip bir HTTP isteği gönderin:</span><span class="sxs-lookup"><span data-stu-id="8be0f-167">Submit an HTTP request with the following properties:</span></span>
    - <span data-ttu-id="8be0f-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span><span class="sxs-lookup"><span data-stu-id="8be0f-168">**URL** - `https://securityservice.operations365.dynamics.com/token`</span></span>
    - <span data-ttu-id="8be0f-169">**Yöntem** - `POST`</span><span class="sxs-lookup"><span data-stu-id="8be0f-169">**Method** - `POST`</span></span>
    - <span data-ttu-id="8be0f-170">**HTTP üst bilgisi**: API sürümünü ekleyin (anahtar: `Api-Version` ve değer: `1.0` olmalıdır)</span><span class="sxs-lookup"><span data-stu-id="8be0f-170">**HTTP header** - Include the API version (key is `Api-Version` and value is `1.0`)</span></span>
    - <span data-ttu-id="8be0f-171">**Gövde içeriği:** Önceki adımda oluşturduğunuz JSON isteğini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-171">**Body content** - Include the JSON request that you created in the previous step.</span></span>

1. <span data-ttu-id="8be0f-172">Yanıt olarak bir `access_token` alırsınız.</span><span class="sxs-lookup"><span data-stu-id="8be0f-172">You will get an `access_token` in response.</span></span> <span data-ttu-id="8be0f-173">Stok Görünürlüğü API'sını çağırmak için taşıyıcı belirteç olarak ihtiyacınız olan budur.</span><span class="sxs-lookup"><span data-stu-id="8be0f-173">This is what you need as a bearer token to call the Inventory Visibility API.</span></span> <span data-ttu-id="8be0f-174">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-174">Here is an example.</span></span>

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="uninstall-the-add-in"></a><span data-ttu-id="8be0f-175">Eklentiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="8be0f-175">Uninstall the add-in</span></span>

<span data-ttu-id="8be0f-176">Eklentiyi kaldırmak için **Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8be0f-176">To uninstall the add-in, select **Uninstall**.</span></span> <span data-ttu-id="8be0f-177">LCS'yi yenilediğinizde Stok Görünürlüğü Eklentisi kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-177">Refresh LCS and the Inventory Visibility Add-in will be removed.</span></span> <span data-ttu-id="8be0f-178">Kaldırma işlemi eklenti kaydını kaldırır ve hizmette depolanan tüm iş verilerini temizlemek için bir iş başlatır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-178">The uninstall process will remove the add-in registration and also start a job to clean up all of the business data stored in the service.</span></span>

## <a name="inventory-visibility-add-in-public-api"></a><span data-ttu-id="8be0f-179">Stok Görünürlüğü Eklentisi genel API'sı</span><span class="sxs-lookup"><span data-stu-id="8be0f-179">Inventory Visibility Add-in public API</span></span>

<span data-ttu-id="8be0f-180">Stok Görünürlüğü Eklentisi'nin genel REST API'sı, birkaç özel tümleştirme uç noktası sunar.</span><span class="sxs-lookup"><span data-stu-id="8be0f-180">The public REST API of the of the Inventory Visibility Add-in presents several specific endpoints of integration.</span></span> <span data-ttu-id="8be0f-181">Üç ana etkileşim türünü destekler:</span><span class="sxs-lookup"><span data-stu-id="8be0f-181">It supports three main interaction types:</span></span>

- <span data-ttu-id="8be0f-182">Harici bir sistemden eldeki değişiklikleri eklentiye deftere nakletmek.</span><span class="sxs-lookup"><span data-stu-id="8be0f-182">Posting on-hand changes to the add-in from an external system.</span></span>
- <span data-ttu-id="8be0f-183">Harici bir sistemden eldeki geçerli miktarları sorgulamak.</span><span class="sxs-lookup"><span data-stu-id="8be0f-183">Querying current on-hand quantities from an external system.</span></span>
- <span data-ttu-id="8be0f-184">Eldeki Supply Chain Management ile otomatik eşitleme.</span><span class="sxs-lookup"><span data-stu-id="8be0f-184">Automatic synchronization with Supply Chain Management on-hand.</span></span>

<span data-ttu-id="8be0f-185">Otomatik eşitleme, genel API'nın bir parçası değildir ancak Stok Görünürlüğü Eklentisi'ni etkinleştiren ortamlar için arka planda işlenir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-185">The automatic synchronization isn't part of the public API but is instead handled in the background for environments that have enabled the Inventory Visibility Add-in.</span></span>

### <a name="authentication"></a><span data-ttu-id="8be0f-186">Kimlik Doğrulama</span><span class="sxs-lookup"><span data-stu-id="8be0f-186">Authentication</span></span>

<span data-ttu-id="8be0f-187">Platform güvenlik belirteci, Stok Görünürlüğü Eklentisi'ni çağırmak için kullanılır, bu nedenle Azure Active Directory uygulamanızı kullanarak bir Azure Active Directory belirteci oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-187">The platform security token is used to call the Inventory Visibility Add-in, so you must generate an Azure Active Directory token using your Azure Active Directory application.</span></span>

<span data-ttu-id="8be0f-188">Güvenlik belirtecini alma hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü Eklentisi'ni Yükleme](#install-add-in).</span><span class="sxs-lookup"><span data-stu-id="8be0f-188">For more information about how to get the security token, see [Install the Inventory Visibility Add-in](#install-add-in).</span></span>

### <a name="configure-the-inventory-visibility-api"></a><span data-ttu-id="8be0f-189">Stok Görünürlüğü API'sını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8be0f-189">Configure the Inventory Visibility API</span></span>

<span data-ttu-id="8be0f-190">Hizmeti kullanmadan önce, aşağıdaki alt bölümlerde açıklanan yapılandırmaları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-190">Before using the service, you must complete the configurations described in the following subsections.</span></span> <span data-ttu-id="8be0f-191">Yapılandırma, ortamınızın ayrıntılarına bağlı olarak değişebilir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-191">The configuration may vary based on the details of your environment.</span></span> <span data-ttu-id="8be0f-192">Başlıca dört bölümden oluşur:</span><span class="sxs-lookup"><span data-stu-id="8be0f-192">It primarily includes four parts:</span></span>

- [<span data-ttu-id="8be0f-193">Bölümleme</span><span class="sxs-lookup"><span data-stu-id="8be0f-193">Partitioning</span></span>](#partitioning)
- [<span data-ttu-id="8be0f-194">Boyut yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="8be0f-194">Dimension configurations</span></span>](#dimension-configurations)
- [<span data-ttu-id="8be0f-195">Dizin oluşturma</span><span class="sxs-lookup"><span data-stu-id="8be0f-195">Indexing</span></span>](#indexing)
- [<span data-ttu-id="8be0f-196">Özel ölçüm</span><span class="sxs-lookup"><span data-stu-id="8be0f-196">Custom measurement</span></span>](#custom-measurement)

#### <a name="partitioning"></a><span data-ttu-id="8be0f-197">Bölümleme</span><span class="sxs-lookup"><span data-stu-id="8be0f-197">Partitioning</span></span>

<span data-ttu-id="8be0f-198">Bölümleme, Stok Görünürlüğü API'sının performansını önemli ölçüde etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-198">Partitioning can significantly influence the performance of the Inventory Visibility API.</span></span> <span data-ttu-id="8be0f-199">Anlamlı veri sorgularına izin verirken küçük veri gruplandırmalarına olanak tanıyan bir düzen tanımlamak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-199">It's a good idea to define a scheme that allows for small groupings of data while still allowing for meaningful data queries.</span></span>

<span data-ttu-id="8be0f-200">`organizationId` (Supply Chain Management'ta `dataAreaId`), her zaman bölümlemenin bir parçası olacaktır ve varsayılan olarak Stok Görünürlüğü, *Tesis + Konum* olarak boyutlara göre bölümlenecek şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-200">The `organizationId` (`dataAreaId` in Supply Chain Management) will always be part of the partitioning, and by default Inventory Visibility is set to partition by dimensions as *Site + Location*.</span></span> <span data-ttu-id="8be0f-201">Bu, hizmetin her zaman filtrelerde tanımlanan bu boyutlarla sorgulanması gerektiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-201">This means that the service must always be queried with these dimensions defined on the filters.</span></span>

> [!NOTE]
> <span data-ttu-id="8be0f-202">*Tesis* ve *Konum*, Stok Görünürlüğü'nde iki genel varsayılan boyuttur.</span><span class="sxs-lookup"><span data-stu-id="8be0f-202">*Site* and *Location* are two general default dimensions in Inventory Visibility.</span></span> <span data-ttu-id="8be0f-203">Supply Chain Management'ta, bu boyutlara *Tesis* (`InventSiteId`) ve *Ambar* (`InventLocationId`) adı verilir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-203">In Supply Chain Management, those dimensions are called *Site* (`InventSiteId`) and *Warehouse* (`InventLocationId`)</span></span>

### <a name="dimension-configurations"></a><span data-ttu-id="8be0f-204">Boyut yapılandırmaları</span><span class="sxs-lookup"><span data-stu-id="8be0f-204">Dimension configurations</span></span>

<span data-ttu-id="8be0f-205">Stok Görünürlüğü, birden çok kaynağın sistem tümleştirmesini etkinleştirmek için genel varsayılan boyutların bir listesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="8be0f-205">Inventory Visibility will provide a list of general default dimensions to enable the multiple source system integration.</span></span>

<span data-ttu-id="8be0f-206">Aşağıdaki tabloda, Stok Görünürlüğü'nde varsayılan boyut adları olacak stok boyutları listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-206">The following table lists the inventory dimensions that will be the default dimension names in Inventory Visibility.</span></span>

| <span data-ttu-id="8be0f-207">Boyut türü</span><span class="sxs-lookup"><span data-stu-id="8be0f-207">Dimension type</span></span> | <span data-ttu-id="8be0f-208">Boyut adı</span><span class="sxs-lookup"><span data-stu-id="8be0f-208">Dimension name</span></span> |
|---|---|
| <span data-ttu-id="8be0f-209">Ürün</span><span class="sxs-lookup"><span data-stu-id="8be0f-209">Product</span></span> | `ColorId` |
| <span data-ttu-id="8be0f-210">Ürün</span><span class="sxs-lookup"><span data-stu-id="8be0f-210">Product</span></span> | `SizeId` |
| <span data-ttu-id="8be0f-211">Ürün</span><span class="sxs-lookup"><span data-stu-id="8be0f-211">Product</span></span> | `StyleId` |
| <span data-ttu-id="8be0f-212">Ürün</span><span class="sxs-lookup"><span data-stu-id="8be0f-212">Product</span></span> | `ConfigId` |
| <span data-ttu-id="8be0f-213">İzleme</span><span class="sxs-lookup"><span data-stu-id="8be0f-213">Tracking</span></span> | `BatchId` |
| <span data-ttu-id="8be0f-214">İzleme</span><span class="sxs-lookup"><span data-stu-id="8be0f-214">Tracking</span></span> | `SerialId` |
| <span data-ttu-id="8be0f-215">Yer</span><span class="sxs-lookup"><span data-stu-id="8be0f-215">Location</span></span> | `LocationId` |
| <span data-ttu-id="8be0f-216">Yer</span><span class="sxs-lookup"><span data-stu-id="8be0f-216">Location</span></span> | `SiteId` |
| <span data-ttu-id="8be0f-217">Stok Durumu</span><span class="sxs-lookup"><span data-stu-id="8be0f-217">Inventory Status</span></span> | `StatusId` |
| <span data-ttu-id="8be0f-218">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="8be0f-218">Warehouse Specific</span></span> | `WMSLocationId` |
| <span data-ttu-id="8be0f-219">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="8be0f-219">Warehouse Specific</span></span> | `WMSPalletId` |
| <span data-ttu-id="8be0f-220">Ambara Özel</span><span class="sxs-lookup"><span data-stu-id="8be0f-220">Warehouse Specific</span></span> | `LicensePlateId` |

> [!NOTE]
> <span data-ttu-id="8be0f-221">Önceki tabloda listelenen boyut türü yalnızca referans içindir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-221">The dimension type listed in the previous table is for reference only.</span></span> <span data-ttu-id="8be0f-222">Stok Görünürlüğü'nde boyut türünü tanımlamanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="8be0f-222">You don't need to define the dimension type in Inventory Visibility.</span></span>

<span data-ttu-id="8be0f-223">Özel bir boyut varsa ve Stok Görünürlüğü tarafından tüketildiğinde varsayılan değere ayarlanması gerekiyorsa Stok Görünürlüğü'nde **Özel boyut** adını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-223">If a custom dimension exists and needs to flow to a default value when consumed by Inventory Visibility, you can configure the **Custom dimension** name in Inventory Visibility.</span></span>

<span data-ttu-id="8be0f-224">Harici sistemler, sorgulanacak belirli boyut kümeleri hakkında eldeki bilgilerin sorgulanmasını sağlayan RESTful API'lar aracılığıyla Stok Görünürlüğü'ne erişir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-224">External systems access Inventory Visibility through RESTful APIs that enable on-hand information on given sets of dimensions to be queried.</span></span> <span data-ttu-id="8be0f-225">Tümleştirme için Stok Görünürlüğü, *dış kanal veri kaynağını* ve kaynak boyutunu Stok Görünürlüğü'ndeki *hedef boyutlara* yapılandırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="8be0f-225">For the integration, Inventory Visibility enables you to configure the *external channel data source* and the source dimension to the *target dimensions* in Inventory Visibility.</span></span>

<span data-ttu-id="8be0f-226">Hedef boyutlar aşağıdakilerden biri olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="8be0f-226">The target dimensions should be one of the following:</span></span>

- <span data-ttu-id="8be0f-227">Stok Görünürlüğü'ndeki varsayılan boyutlar</span><span class="sxs-lookup"><span data-stu-id="8be0f-227">Default dimensions in Inventory Visibility</span></span>
- <span data-ttu-id="8be0f-228">Özel boyutlar</span><span class="sxs-lookup"><span data-stu-id="8be0f-228">Custom dimensions</span></span>

<span data-ttu-id="8be0f-229">Boyut yapılandırmasının amacı, boyutlardaki sorgular ve boyutlarla deftere nakil olayı için çoklu sistem tümleştirmesini standartlaştırmaktır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-229">The purpose of dimension configuration is to standardize the multi-system integration for the query on dimensions and the posting event with dimensions.</span></span>

#### <a name="indexing"></a><span data-ttu-id="8be0f-230">Dizin oluşturma</span><span class="sxs-lookup"><span data-stu-id="8be0f-230">Indexing</span></span>

<span data-ttu-id="8be0f-231">Çoğu zaman, eldeki stok sorgusu yalnızca en yüksek "toplam" düzeyinde olmakla birlikte, sonuçları stok boyutlarına göre toplanmış olarak görmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-231">Most of the time, the inventory on-hand query will not only be on the highest "total" level, but you may want to see results aggregated based on the inventory dimensions.</span></span>

<span data-ttu-id="8be0f-232">Stok Görünürlüğü, boyuta veya boyutların karışımına göre dizinleri ayarlamanıza izin vererek esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="8be0f-232">Inventory Visibility provides flexibility by allowing you to set up the indexes, which are based on the dimension or the combination of the dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="8be0f-233">Şu anda, yalnızca en fazla beş adet dizin yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-233">Currently, you can only configure indexes to a maximum of five.</span></span> <span data-ttu-id="8be0f-234">İş ihtiyaçlarınızı karşıladığından emin olmak için uygulamadan önce hangi boyutu veya boyut karışımını kullanacağınızı dikkatlice düşünmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-234">You need to carefully consider which dimension or dimension combination you will use before the implementation to ensure that it will meet your business needs.</span></span> <span data-ttu-id="8be0f-235">Örneğin, ürünleri aşağıdaki gibi sorgulamak istiyorsanız:</span><span class="sxs-lookup"><span data-stu-id="8be0f-235">For example, if you want to query products as follows:</span></span>

- <span data-ttu-id="8be0f-236">Kümelenmiş ürün eldeki verilerini *Renk* ve *Boyut* boyutlarına göre sorgulayın.</span><span class="sxs-lookup"><span data-stu-id="8be0f-236">Query the aggregated product on-hand by the *Color* and *Size* dimensions.</span></span>
- <span data-ttu-id="8be0f-237">Bazı durumlarda, ürün üzerinde toplu olarak sorgu yapmak istersiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-237">In some cases, you just want to query on the product in total.</span></span>

<span data-ttu-id="8be0f-238">Aşağıdaki gibi tanımlanan iki dizininiz olur:</span><span class="sxs-lookup"><span data-stu-id="8be0f-238">You would have two indexes defined as the following:</span></span>

- `["ColorId", "SizeId"]`
- `[]`

<span data-ttu-id="8be0f-239">Boş köşeli ayraç, bölüm içindeki ürün kimliğine göre kümelenir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-239">The empty bracket will aggregate based on the product ID within the partition.</span></span>

<span data-ttu-id="8be0f-240">Dizin oluşturma, sonuçlarınızı `groupBy` sorgu ayarına göre nasıl gruplanabileceğinizi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8be0f-240">The indexing defines how you can group your results based on the `groupBy` query setting.</span></span> <span data-ttu-id="8be0f-241">Bu durumda, herhangi bir `groupBy` değeri tanımlamazsanız, toplamları `productid` değerine göre alırsınız.</span><span class="sxs-lookup"><span data-stu-id="8be0f-241">In this case if you don't define any `groupBy` values, you'll get totals by `productid`.</span></span> <span data-ttu-id="8be0f-242">Aksi takdirde, `groupBy=ColorId&groupBy=SizeId` olarak `groupBy` tanımlarsanız sistemde farklı renk ve boyut kombinasyonlarına dayalı olarak döndürülen birden çok satır alırsınız.</span><span class="sxs-lookup"><span data-stu-id="8be0f-242">Otherwise if you define `groupBy` as `groupBy=ColorId&groupBy=SizeId`, you'll get multiple lines returned, based on the different color and size combinations in the system.</span></span>

<span data-ttu-id="8be0f-243">Sorgu ölçütlerinizi istek gövdesine koyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-243">You can put your query criteria in the request body.</span></span>

<span data-ttu-id="8be0f-244">Renk ve boyut kombinasyonuna sahip ürün üzerinde gerçekleştirilen bir sorgu örneği.</span><span class="sxs-lookup"><span data-stu-id="8be0f-244">Here is a sample query on the product with color and size combination.</span></span>

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

#### <a name="custom-measurement"></a><span data-ttu-id="8be0f-245">Özel ölçüm</span><span class="sxs-lookup"><span data-stu-id="8be0f-245">Custom measurement</span></span>

<span data-ttu-id="8be0f-246">Varsayılan ölçüm miktarları Supply Chain Management'a bağlıdır, ancak varsayılan ölçümlerin bir karışımından oluşan bir miktara sahip olmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-246">The default measurement quantities are linked to Supply Chain Management, however you may want to have a quantity that is made up of a combination of the default measurements.</span></span> <span data-ttu-id="8be0f-247">Bunu yapmak için eldeki sorguların çıktısına eklenecek özel miktarlar yapılandırmanız olabilir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-247">To do this, you can have a configuration of custom quantities, which will be added to the output of the on-hand queries.</span></span>

<span data-ttu-id="8be0f-248">İşlev, özel ölçümü oluşturmak için eklenecek bir dizi ölçü ve/veya çıkarılacak bir dizi ölçü belirlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-248">The functionality simply allows you to define a set of measures that will be added, and/or a set of measures that will be subtracted, in order to form the custom measurement.</span></span>

<span data-ttu-id="8be0f-249">Örneğin, aşağıdaki sorgu koşulunda, `MyCustomAvailableforReservation` özel ölçüm miktarını tüketim sistemi tarafından tüketilecek şekilde yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-249">For example, with the following query condition, you will configure the custom measurement quantity as `MyCustomAvailableforReservation` to be consumed by the consumption system.</span></span>

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



| <span data-ttu-id="8be0f-250">Tüketim sistemi</span><span class="sxs-lookup"><span data-stu-id="8be0f-250">Consumption system</span></span> | <span data-ttu-id="8be0f-251">Hesaplanan ölçümler</span><span class="sxs-lookup"><span data-stu-id="8be0f-251">Calculated measurers</span></span> | <span data-ttu-id="8be0f-252">Veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="8be0f-252">Data source</span></span> | <span data-ttu-id="8be0f-253">Değiştirici</span><span class="sxs-lookup"><span data-stu-id="8be0f-253">Modifier</span></span> | <span data-ttu-id="8be0f-254">Değiştirici hesaplama türü</span><span class="sxs-lookup"><span data-stu-id="8be0f-254">Modifier calculation type</span></span> |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | <span data-ttu-id="8be0f-255">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="8be0f-255">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | <span data-ttu-id="8be0f-256">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="8be0f-256">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | <span data-ttu-id="8be0f-257">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="8be0f-257">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | <span data-ttu-id="8be0f-258">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="8be0f-258">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | <span data-ttu-id="8be0f-259">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="8be0f-259">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | <span data-ttu-id="8be0f-260">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="8be0f-260">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | <span data-ttu-id="8be0f-261">Fark hesap eki</span><span class="sxs-lookup"><span data-stu-id="8be0f-261">Addition</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | <span data-ttu-id="8be0f-262">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="8be0f-262">Subtraction</span></span> |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | <span data-ttu-id="8be0f-263">Çıkarma</span><span class="sxs-lookup"><span data-stu-id="8be0f-263">Subtraction</span></span> |

<span data-ttu-id="8be0f-264">Bununla, özel ölçüm miktarı üzerindeki sorgu, aşağıdaki çıktıyı döndürecektir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-264">With that, the query on the custom measurement quantity will return the following output.</span></span>

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

<span data-ttu-id="8be0f-265">`MyCustomAvailableforReservation` çıktısı, aşağıdaki gibi, özel ölçümlerdeki hesaplama ayarına dayanır:</span><span class="sxs-lookup"><span data-stu-id="8be0f-265">The `MyCustomAvailableforReservation` output is based on the calculation setting in the custom measurements as:</span></span>  
 <span data-ttu-id="8be0f-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span><span class="sxs-lookup"><span data-stu-id="8be0f-266">*100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*</span></span>

### <a name="posting-on-hand-changes"></a><span data-ttu-id="8be0f-267">Eldeki değişiklikleri deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="8be0f-267">Posting on-hand changes</span></span>

<span data-ttu-id="8be0f-268">Etkinliğin yayınlanacağı URL, coğrafi bölgenize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-268">The exact URL that the event will be posted to will depend on your geographical region.</span></span> <span data-ttu-id="8be0f-269">Şu şekilde olacaktır:</span><span class="sxs-lookup"><span data-stu-id="8be0f-269">It will take the form:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand`

<span data-ttu-id="8be0f-270">Kimlik doğrulaması yapıldığında, bu URL, hizmete eldeki değişiklik olaylarını göndermek için HTTP `POST` yöntemiyle birlikte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-270">When authenticated, this URL can be used along with the HTTP `POST` method to send on-hand change events to the service.</span></span>

<span data-ttu-id="8be0f-271">Dynamics 365 hizmetleriyle HTTP istekleri üzerinden iletişim kurmak için özel bir üst bilgi kullanılır ve verilerin bağlı olduğu Supply Chain Management kurulumunun ortam kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-271">A special header is used for communicating with Dynamics 365 services through HTTP requests, denoting the environment ID of the Supply Chain Management instance the data is linked to.</span></span> <span data-ttu-id="8be0f-272">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="8be0f-272">For example:</span></span>

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a><span data-ttu-id="8be0f-273">Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 1</span><span class="sxs-lookup"><span data-stu-id="8be0f-273">Posting on-hand changes query example 1</span></span>

<span data-ttu-id="8be0f-274">Bu örnekte Power Apps'te boyut yapılandırmasını ayarlayacağınız bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-274">This example shows a scenario where you will set up the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="8be0f-275">Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:</span><span class="sxs-lookup"><span data-stu-id="8be0f-275">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="8be0f-276">Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-276">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="8be0f-277">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="8be0f-277">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="posting-on-hand-changes-query-example-2"></a><span data-ttu-id="8be0f-278">Eldeki değişikliklerle ilgili sorguyu deftere nakletme örneği 2</span><span class="sxs-lookup"><span data-stu-id="8be0f-278">Posting on-hand changes query example 2</span></span>

<span data-ttu-id="8be0f-279">Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-279">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="8be0f-280">`dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-280">All dimensions must be base dimensions when the `dimensionDataSource` field is null, empty, or whitespace.</span></span>

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

#### <a name="json-document-field-properties"></a><span data-ttu-id="8be0f-281">JSON belge alanı özellikleri</span><span class="sxs-lookup"><span data-stu-id="8be0f-281">JSON document field properties</span></span>

<span data-ttu-id="8be0f-282">Daha önce sağlanan JSON sorgu örneklerindeki alanlar aşağıdaki tabloda listelenen özelliklere sahiptir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-282">The fields from the JSON query examples provided previously have the properties listed in the following table.</span></span>

| <span data-ttu-id="8be0f-283">Alan kodu</span><span class="sxs-lookup"><span data-stu-id="8be0f-283">Field ID</span></span> | <span data-ttu-id="8be0f-284">Tanım</span><span class="sxs-lookup"><span data-stu-id="8be0f-284">Description</span></span> |
|---|---|
| `id` | <span data-ttu-id="8be0f-285">Belirli bir değişiklik olayı için benzersiz bir kimlik.</span><span class="sxs-lookup"><span data-stu-id="8be0f-285">A unique ID for the specific change event.</span></span> <span data-ttu-id="8be0f-286">Bu kimlik, deftere nakil sırasında hizmetle iletişim başarısız olursa olursa olayın yeniden gönderilmesinin aynı olayın sistemde iki kez sayılmasıyla sonuçlanmamasını sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-286">This ID is used to ensure that if communication with the service fails during posting, resubmitting the event would not result in the same event being counted twice in the system.</span></span> |
| `organizationId` | <span data-ttu-id="8be0f-287">Olayla bağlantılı kuruluşun tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="8be0f-287">The identifier of the organization linked to the event.</span></span> <span data-ttu-id="8be0f-288">Bu, Supply Chain Management kuruluşları veya veri alanı kimlikleriyle eşlenir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-288">This maps to Supply Chain Management organizations or data area IDs.</span></span> |
| `productId` | <span data-ttu-id="8be0f-289">Söz konusu ürünün tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="8be0f-289">The identifier of the product in question.</span></span> |
| `quantity` | <span data-ttu-id="8be0f-290">Eldeki miktarın değiştirilmesi gereken miktar.</span><span class="sxs-lookup"><span data-stu-id="8be0f-290">The quantity by which the on-hand needs to be changed.</span></span> <span data-ttu-id="8be0f-291">Örneğin, bir rafa 10 yeni simit eklenseydi, bu değer 10 olur.</span><span class="sxs-lookup"><span data-stu-id="8be0f-291">If, for instance, 10 new bagels were added to a shelf, this value would be 10.</span></span> <span data-ttu-id="8be0f-292">Raftan 3 simit çıkarılırsa veya satılırsa bu değer -3 olur.</span><span class="sxs-lookup"><span data-stu-id="8be0f-292">If 3 bagels were then removed from the shelf or sold, this value would be -3.</span></span> |
| `dimensionDataSource` | <span data-ttu-id="8be0f-293">Deftere nakil değişikliği olayı ve sorgusunda kullanılan boyutların veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="8be0f-293">The data source of the dimensions used in the posting change event and query.</span></span> <span data-ttu-id="8be0f-294">Veri kaynağını belirtirseniz belirtilen veri kaynağındaki özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-294">If you specify the data source, you can use the custom dimensions from the specified data source.</span></span> <span data-ttu-id="8be0f-295">Boyut yapılandırmasıyla, Stok Görünürlüğü özel boyutları genel varsayılan boyutlarla eşleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-295">With the dimension configuration, Inventory Visibility can map the custom dimensions to the general default dimensions.</span></span> <span data-ttu-id="8be0f-296">`dimensionDataSource` belirtilmemişse sorgularınızda yalnızca genel varsayılan boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-296">If the `dimensionDataSource` is not specified, you can only use the general default dimensions in your queries.</span></span>   |
| `dimensions` | <span data-ttu-id="8be0f-297">Anahtar/değer çiftlerinden oluşan dinamik bir set.</span><span class="sxs-lookup"><span data-stu-id="8be0f-297">A dynamic bag of key/value pairs.</span></span> <span data-ttu-id="8be0f-298">Bunlar Supply Chain Management'taki bazı boyutlarla eşlenir ancak olay Supply Chain Management'tan veya harici bir sistemden geliyorsa gösterebilecek özel boyutlar *(Kaynak* gibi) da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-298">These will map to some of the dimensions in Supply Chain Management, but you could also add custom dimensions (like *Source*) that may denote if the event was coming from Supply Chain Management or an external system.</span></span> |

### <a name="querying-current-on-hand"></a><span data-ttu-id="8be0f-299">Mevcut eldeki miktarı sorgulama</span><span class="sxs-lookup"><span data-stu-id="8be0f-299">Querying current on-hand</span></span>

<span data-ttu-id="8be0f-300">Mevcut eldeki miktarı sorgulamak için uç noktası, benzer bir URL'ye sahip olacaktır:</span><span class="sxs-lookup"><span data-stu-id="8be0f-300">The endpoint for querying the current on-hand will have a similar URL:</span></span>

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

<span data-ttu-id="8be0f-301">HTTP `POST` yöntemi ile sorgulanacaktır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-301">It will be queried with the HTTP `POST` method.</span></span>

#### <a name="current-on-hand-query-example-1"></a><span data-ttu-id="8be0f-302">Geçerli eldeki miktar sorgusu örneği 1</span><span class="sxs-lookup"><span data-stu-id="8be0f-302">Current on-hand query example 1</span></span>

<span data-ttu-id="8be0f-303">Bu örnekte Power Apps'te boyut yapılandırmasını zaten tamamladığınız bir senaryo gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-303">This example shows a scenario where you have already completed the dimension configuration in Power Apps.</span></span>

<span data-ttu-id="8be0f-304">Power Apps'te boyut eşlemesini yapılandırmak için aşağıdaki sorguyu kullanın:</span><span class="sxs-lookup"><span data-stu-id="8be0f-304">Use the following query to configure the dimension mapping in Power Apps:</span></span>

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

<span data-ttu-id="8be0f-305">Artık sorgularınızda `dimensionDataSource` belirtebilir ve özel boyutları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-305">Now you can specify the `dimensionDataSource` and use custom dimensions in your queries.</span></span> <span data-ttu-id="8be0f-306">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="8be0f-306">The system will automatically convert custom dimensions to base dimensions.</span></span> <span data-ttu-id="8be0f-307">`DimensionDataSource` değerini `filters` içinde belirtebilir ve özel boyutları hem `filters` hem de `groupByValues` ile gelirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be0f-307">You can specify the `DimensionDataSource` in `filters` and specify custom dimensions in both `filters` and `groupByValues`.</span></span> <span data-ttu-id="8be0f-308">Sistem, özel boyutları otomatik olarak temel boyutlara dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="8be0f-308">The system will automatically convert custom dimensions to base dimensions.</span></span>

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

#### <a name="current-on-hand-query-example-2"></a><span data-ttu-id="8be0f-309">Geçerli eldeki miktar sorgusu örneği 2</span><span class="sxs-lookup"><span data-stu-id="8be0f-309">Current on-hand query example 2</span></span>

<span data-ttu-id="8be0f-310">Bu örnekte, Power Apps'te boyut yapılandırması için eşlemelerin ayarlandığı bir senaryo gösterilmektedir, bu nedenle deftere nakil de temel boyutları kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-310">This example shows a scenario where no mappings are set up for the dimension configuration in Power Apps, so the posting should also use the base dimensions.</span></span> <span data-ttu-id="8be0f-311">`filters` altındaki `dimensionDataSource` alanı null, boş veya boşluk olduğunda tüm boyutlar temel boyutlar olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8be0f-311">All dimensions must be base dimensions when the `dimensionDataSource` field, under `filters` is null, empty, or whitespace.</span></span>

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

#### <a name="example-return-result"></a><span data-ttu-id="8be0f-312">Örnek döndürme sonucu</span><span class="sxs-lookup"><span data-stu-id="8be0f-312">Example return result</span></span>

<span data-ttu-id="8be0f-313">Önceki örneklerde gösterilen sorgular böyle bir sonuç döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="8be0f-313">The queries shown in the previous examples could return a result like this.</span></span>

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

<span data-ttu-id="8be0f-314">Miktar alanlarının ölçümler sözlüğü ve ilişkili değerleri şeklinde yapılandırıldığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8be0f-314">Note that the quantities fields are structured as a dictionary of measures and their associated values.</span></span>
