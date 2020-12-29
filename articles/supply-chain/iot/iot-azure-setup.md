---
title: IoT Zekası için Azure kaynaklarını ayarlama
description: Bu konu, IoT Zekası için gerekli olan Microsoft Azure kaynaklarının nasıl oluşturulacağını ve yapılandırılacağını açıklamaktadır.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1277d2ab8bb1f2925874f7469250e164f6bde62d
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439612"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="86362-103">IoT Zekası için Azure kaynaklarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="86362-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86362-104">Bu konu, IoT Zekası için gerekli olan Microsoft Azure kaynaklarının nasıl oluşturulacağını ve yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="86362-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="86362-105">Azure kaynakları oluşturma</span><span class="sxs-lookup"><span data-stu-id="86362-105">Create Azure resources</span></span>

<span data-ttu-id="86362-106">Bir IoT hub'ı, Redis önbelleği ve Microsoft Dynamics 365 Supply Chain Management tarafından erişilebilen bir anahtar kasası oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="86362-107">Microsoft Dynamics ERP Mikro Hizmetleri birinci taraf uygulama kimliğinin kiracınızda olduğunu doğrulama</span><span class="sxs-lookup"><span data-stu-id="86362-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="86362-108">Microsoft Dynamics ERP Mikro Hizmetleri birinci taraf uygulama kimliğinin kiracınızda olduğunu doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="86362-109">Azure portalında <https://portal.azure.com> adresinden oturum açın.</span><span class="sxs-lookup"><span data-stu-id="86362-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="86362-110">**Azure Active Directory** gidin.</span><span class="sxs-lookup"><span data-stu-id="86362-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="86362-111">**Kurumsal uygulamalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="86362-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="86362-112">**Uygulama türü** alanında, **Microsoft uygulamaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="86362-113">Arama alanına, **Microsoft Dynamics ERP Mikro Hizmetleri**'ni girin.</span><span class="sxs-lookup"><span data-stu-id="86362-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="86362-114">**Microsoft Dynamics ERP Mikro Hizmetleri**'nin listede olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="86362-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="86362-115">Diğer uygulamaların benzer adları vardır.</span><span class="sxs-lookup"><span data-stu-id="86362-115">Other applications have similar names.</span></span> <span data-ttu-id="86362-116">Bu nedenle, doğru uygulamayı bulmaya özen gösterin.</span><span class="sxs-lookup"><span data-stu-id="86362-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="86362-117">Uygulama kimliği şudur: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="86362-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="86362-118">Uygulama listede değilse kiracınıza eklemeniz gerekir:</span><span class="sxs-lookup"><span data-stu-id="86362-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="86362-119">Azure portalının araç çubuğunda, Azure Cloud Shell'i açmak için düğmeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="86362-120">**Install-Module AzureAD** komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="86362-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="86362-121">Modülü yüklemek için **Y** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="86362-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="86362-122">Modülün yüklü olduğunu doğrulamak için **Get-InstalledModule -Name "AzureAD"** komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="86362-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="86362-123">Doğrulamayı çalıştırmak için **Connect-AzureAD -Confirm** komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="86362-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="86362-124">**New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2** komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="86362-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="86362-125">Uygulama kimliğinin kiracınızda olduğunu doğrulamak için şimdi 1'den 6'ya kadar olan adımları tekrarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86362-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="86362-126">Anahtar kasası kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="86362-126">Create a key vault resource</span></span>

<span data-ttu-id="86362-127">Anahtar kasası kaynağı oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="86362-128">Azure portalında, bir kaynak grubu oluşturun veya bir kaynak grubuna gidin.</span><span class="sxs-lookup"><span data-stu-id="86362-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="86362-129">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-129">Select **Add**.</span></span>
3. <span data-ttu-id="86362-130">**Yeni** sayfasındaki arama alanına **Anahtar kasası** yazın.</span><span class="sxs-lookup"><span data-stu-id="86362-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="86362-131">Ardından **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-131">Then select **Create**.</span></span>
4. <span data-ttu-id="86362-132">**Anahtar kasası oluştur** sayfasında, **Anahtar kasası adı** alanına bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="86362-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="86362-133">Varsayılan değerleri gözden geçirin ve sonra **Gözden geçir + oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="86362-134">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-134">Select **Create**.</span></span>

<span data-ttu-id="86362-135">Anahtar kasası arka planda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="86362-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="86362-136">IoT hub kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="86362-136">Create an IoT hub resource</span></span>

<span data-ttu-id="86362-137">Bir IoT hub kaynağı oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="86362-138">Kaynak grubu oluşturun veya bir kaynak grubuna gidin.</span><span class="sxs-lookup"><span data-stu-id="86362-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="86362-139">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-139">Select **Add**.</span></span>
3. <span data-ttu-id="86362-140">**Yeni** sayfasındaki arama alanına **IoT Hub** yazın.</span><span class="sxs-lookup"><span data-stu-id="86362-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="86362-141">Ardından **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-141">Then select **Create**.</span></span>
4. <span data-ttu-id="86362-142">**IoT hub adı** alanında, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="86362-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="86362-143">Varsayılan değerleri gözden geçirin ve sonra **Gözden geçir + oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="86362-144">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-144">Select **Create**.</span></span>

<span data-ttu-id="86362-145">IoT hub arka planda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="86362-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="86362-146">Her ortam için yalnızca bir IoT hub kaynağı oluşturmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="86362-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="86362-147">Redis önbelleği kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="86362-147">Create a Redis cache resource</span></span>

<span data-ttu-id="86362-148">Bir Redis önbelleği kaynağı oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="86362-149">Kaynak grubu oluşturun veya bir kaynak grubuna gidin.</span><span class="sxs-lookup"><span data-stu-id="86362-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="86362-150">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-150">Select **Add**.</span></span>
3. <span data-ttu-id="86362-151">**Yeni** sayfasındaki arama alanına **Redis için Azure Önbelleği** yazın.</span><span class="sxs-lookup"><span data-stu-id="86362-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="86362-152">Ardından **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-152">Then select **Create**.</span></span>
4. <span data-ttu-id="86362-153">**DNS adı** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="86362-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="86362-154">Varsayılan değerleri gözden geçirin ve sonra **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="86362-155">Redis önbelleği arka planda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="86362-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="86362-156">Her ortam için yalnızca bir Redis önbelleği oluşturmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="86362-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="86362-157">Tüm kaynaklar artık oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="86362-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="86362-158">Azure kaynaklarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="86362-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="86362-159">IoT hub'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="86362-159">Configure the IoT hub</span></span>

<span data-ttu-id="86362-160">IoT hub'ı yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="86362-161">Kaynaklarınızda IoT hub kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="86362-162">Sol gezinti bölmesinde, **Yerleşik uç noktalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="86362-163">**Tüketici grupları** altında, aşağıdaki tüketici gruplarını yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="86362-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="86362-164">Bu tüketici grupları, hazır senaryolara karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="86362-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="86362-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="86362-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="86362-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="86362-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="86362-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="86362-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="86362-168">Anahtar kasasını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="86362-168">Configure the key vault</span></span>

<span data-ttu-id="86362-169">Anahtar kasasını yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="86362-170">Kaynaklarınızda anahtar kasası kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="86362-171">Sol gezinti bölmesinde **Erişim ilkeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="86362-172">**Erişim ilkesi ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="86362-173">**Erişim ilkesi ekle** sayfasındaki **Gizli izinler** alanında, **Alma** ve **Liste**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="86362-174">**Birincil olan seç**'i tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86362-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="86362-175">**Birincil** iletişim kutusunda, **Microsoft Dynamics ERP Mikro Hizmetleri**'ni arayın ve seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="86362-176">Sonra, **Seç** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-176">Then select **Select**.</span></span>
7. <span data-ttu-id="86362-177">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-177">Select **Add**.</span></span>
8. <span data-ttu-id="86362-178">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-178">Select **Save**.</span></span>

<span data-ttu-id="86362-179">Uygulama şimdi anahtar kasasındaki gizli dizilere erişebilir.</span><span class="sxs-lookup"><span data-stu-id="86362-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="86362-180">IoT hub bağlantı dizesi gizli dizisini kaydetme</span><span class="sxs-lookup"><span data-stu-id="86362-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="86362-181">IoT hub bağlantı dizesinin gizli dizisini kaydetmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="86362-182">Kaynaklarınızda IoT hub kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="86362-183">Sol gezinti bölmesinde, **Yerleşik uç noktalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="86362-184">**Olay Hub'ı ile uyumlu uç nokta** alanındaki değeri kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="86362-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="86362-185">Anahtar kasası kaynağına gidin.</span><span class="sxs-lookup"><span data-stu-id="86362-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="86362-186">Sol gezinti bölmesinde **Gizli diziler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="86362-187">**Oluştur/İçe aktar** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="86362-188">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="86362-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="86362-189">**Değer** alanında, önceden kopyaladığınız uç nokta değerini yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="86362-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="86362-190">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="86362-191">Redis önbelleği bağlantı dizesi gizli dizisini kaydetme</span><span class="sxs-lookup"><span data-stu-id="86362-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="86362-192">Redis önbelleği bağlantı dizesinin gizli dizisini kaydetmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="86362-193">Kaynaklarınızda Redis önbelleği kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="86362-194">**Erişim anahtarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="86362-195">**Birincil bağlantı dizesi** alanındaki değeri kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="86362-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="86362-196">Anahtar kasası kaynağına gidin.</span><span class="sxs-lookup"><span data-stu-id="86362-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="86362-197">Sol gezinti bölmesinde **Gizli diziler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="86362-198">**Oluştur/İçe aktar** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="86362-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="86362-199">**Ad** alanına, bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="86362-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="86362-200">**Değer** alanında, önceden kopyaladığınız bağlantı dizesini yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="86362-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="86362-201">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="86362-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="86362-202">Bağlantı dizelerinden birini her güncelleştirdiğinizde gizli dizi değerlerini de güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="86362-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="86362-203">Gerekli Azure kaynaklarını sağlamayı şimdi bitirdiniz.</span><span class="sxs-lookup"><span data-stu-id="86362-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="86362-204">Sonraki adım, [Microsoft Dynamics LifeCycle Services'daki (LCS) IoT Zekası eklentisinin yüklenmesi](iot-lcs-setup.md) ile ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="86362-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>
