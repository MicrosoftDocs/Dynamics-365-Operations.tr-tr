---
title: Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlama
description: Bu konu, elektronik faturalama eklentisini kullanmaya nasıl başlayacağınızı açıklar.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104448"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="35a7e-103">Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="35a7e-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="35a7e-104">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="35a7e-104">Prerequisites</span></span>

<span data-ttu-id="35a7e-105">Bu konudaki prosedürleri tamamlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:</span><span class="sxs-lookup"><span data-stu-id="35a7e-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="35a7e-106">Microsoft Dynamics Lifecycle Services (LCS) hesabınıza erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35a7e-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="35a7e-107">Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'ın 10.0.13 veya sonraki sürümünü içeren bir LCS projeniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35a7e-107">You must have an LCS project that includes version 10.0.13 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="35a7e-108">Ayrıca, bu uygulamaların aşağıdaki Azure coğrafyalarından birinde dağıtılması gerekir:</span><span class="sxs-lookup"><span data-stu-id="35a7e-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="35a7e-109">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="35a7e-109">East US</span></span>
    - <span data-ttu-id="35a7e-110">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="35a7e-110">West US</span></span>
    - <span data-ttu-id="35a7e-111">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="35a7e-111">North EU</span></span>
    - <span data-ttu-id="35a7e-112">Batı AB</span><span class="sxs-lookup"><span data-stu-id="35a7e-112">West EU</span></span>

- <span data-ttu-id="35a7e-113">Dynamics 365 Regulatory Configuration Services (RCS) hesabınıza erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="35a7e-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="35a7e-114">Özellik yönetiminde RCS hesabınız için Globalleştirme özelliğini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="35a7e-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="35a7e-115">Daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="35a7e-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="35a7e-116">Azure'da bir anahtar kasası ve depolama hesabı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="35a7e-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="35a7e-117">Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="35a7e-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="35a7e-118">Lifecycle Services'de mikro hizmetler için eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="35a7e-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="35a7e-119">LCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="35a7e-120">**Önizleme özelliği yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="35a7e-121">**Genel Önizleme Özellikleri** bölümünde, **e-Faturalama hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="35a7e-122">**Önizleme özelliği etkin** seçeneğinin **Evet** olarak ayarlanmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="35a7e-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="35a7e-123">Elektronik faturalama eklentisiyle RCS entegrasyonu için parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="35a7e-123">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="35a7e-124">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-124">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="35a7e-125">**İlgili bağlantılar** içinde, **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-125">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="35a7e-126">**e-Faturalama hizmeti** sekmesinde, **Hizmet uç noktası URI**'si alanına, aşağıdaki tabloda gösterildiği gibi Azure coğrafyanız için uygun hizmet uç noktasını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-126">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="35a7e-127">Veri merkezi Azure coğrafyası</span><span class="sxs-lookup"><span data-stu-id="35a7e-127">Datacenter Azure geography</span></span> | <span data-ttu-id="35a7e-128">Hizmet uç noktası URI'si</span><span class="sxs-lookup"><span data-stu-id="35a7e-128">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="35a7e-129">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="35a7e-129">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="35a7e-130">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="35a7e-130">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="35a7e-131">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="35a7e-131">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="35a7e-132">Batı AB</span><span class="sxs-lookup"><span data-stu-id="35a7e-132">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="35a7e-133">**Uygulama Kimliği** alanının **0cdb527f-a8d1-4bf8-9436-b352c68682b2** olarak ayarlı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-133">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="35a7e-134">Bu değer sabit bir değerdir.</span><span class="sxs-lookup"><span data-stu-id="35a7e-134">This value is a fixed value.</span></span>
5. <span data-ttu-id="35a7e-135">**LCS Ortam Kimliği** alanına LCS abonelik hesabınızın kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-135">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="35a7e-136">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-136">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="35a7e-137">Key Vault gizli dizisini oluşturma</span><span class="sxs-lookup"><span data-stu-id="35a7e-137">Create Key Vault secret</span></span>

1. <span data-ttu-id="35a7e-138">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-138">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="35a7e-139">**Globalleştirme özelliği** çalışma alanında **Ortam** bölmesinde **e-faturalama** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-139">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="35a7e-140">**Ortam kurulumları** sayfasında, Eylem Bölmesi'nde **Hizmet ortamı**'nı ve ardından **Anahtar kasası parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-140">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="35a7e-141">Yeni bir anahtar kasası gizli dizisi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-141">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="35a7e-142">**Ad** alanına anahtar kasası gizli dizisi adını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-142">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="35a7e-143">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-143">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="35a7e-144">**Anahtar Kasası URI**'si alanına, gizli dizi Azure Key Vault'tan yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-144">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="35a7e-145">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-145">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="35a7e-146">Depolama hesabı gizli dizisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="35a7e-146">Create Storage account secret</span></span>

1. <span data-ttu-id="35a7e-147">**Anahtar kasası parametreleri** sayfasında, **Sertifikalar** bölümünde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-147">On **Key vault parameters** page, in the **Certificates** section, select **Add**.</span></span>
2. <span data-ttu-id="35a7e-148">**Ad** alanına depolama hesabı gizli dizisinin adını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-148">In the **Name** field, enter the same of the storage account secret.</span></span> <span data-ttu-id="35a7e-149">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-149">In the **Description** field, enter a description.</span></span>
3. <span data-ttu-id="35a7e-150">**Tür** alanında **Sertifika**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-150">In the **Type** field, select **Certificate**.</span></span>
4. <span data-ttu-id="35a7e-151">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-151">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="35a7e-152">Elektronik faturalama eklentisi ortamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="35a7e-152">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="35a7e-153">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-153">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="35a7e-154">**Globalleştirme özelliği** çalışma alanında **Ortam** bölmesinde **e-faturalama** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-154">In the **Globalization feature** workspace, in the **Environment** section, select the **e-Invoicing** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="35a7e-155">Hizmet ortamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="35a7e-155">Create a service environment</span></span>

1. <span data-ttu-id="35a7e-156">**Ortam kurulumları** sayfasındaki Eylem bölmesinde **Hizmet ortamı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-156">On the **Environment setups** page, on the action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="35a7e-157">Yeni hizmet ortamı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-157">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="35a7e-158">**Ad** alanına E-faturalama ortamının adını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-158">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="35a7e-159">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-159">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="35a7e-160">**Depolama SAS belirteci gizli dizisi** alanında, depolama hesabına erişimin kimliğini doğrulamak için kullanılması gereken sertifikanın adını seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-160">In the **Storage SAS token secret** field, select the name of the certificate that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="35a7e-161">**Kullanıcılar** bölümünde, ortam üzerinden elektronik fatura göndermesine ve ayrıca depolama hesabına bağlanmasına izin verilen bir kullanıcı eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-161">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="35a7e-162">**Kullanıcı Kimliği** alanına,kullanıcının diğer adını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-162">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="35a7e-163">**E-posta** alanına kullanıcının e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-163">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="35a7e-164">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-164">Select **Save**.</span></span>
8. <span data-ttu-id="35a7e-165">Ülke/bölgenize özgü faturalarınız dijital imzaları uygulamak için bir sertifika zinciri gerektiriyorsa, Eylem bölmesinde **Anahtar kasası parametreleri**'ni seçin, ardından **Sertifikalar zinciri**'ni seçin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="35a7e-165">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="35a7e-166">Bir sertifika zinciri oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-166">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="35a7e-167">**Ad** alanına sertifika zinciri adını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-167">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="35a7e-168">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-168">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="35a7e-169">**Sertifikalar** bölümünde, zincire sertifika eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-169">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="35a7e-170">Sertifikanın zincirdeki konumunu değiştirmek için **Yukarı** veya **Aşağı** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-170">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="35a7e-171">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-171">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="35a7e-172">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-172">Close the page.</span></span>
9. <span data-ttu-id="35a7e-173">**Hizmet ortamı** sayfasında, Eylem Bölmesi'nde, ortamı bulutta yayınlamak için **Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-173">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="35a7e-174">**Durum** alanının değeri **Yayınlandı** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="35a7e-174">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="35a7e-175">Bağlı bir uygulama oluşturma</span><span class="sxs-lookup"><span data-stu-id="35a7e-175">Create a connected application</span></span>

1. <span data-ttu-id="35a7e-176">**Ortam kurulumları** sayfasındaki Eylem bölmesinde **Bağlı uygulamalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-176">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="35a7e-177">Yeni bir bağlı uygulama oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-177">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="35a7e-178">**Ad** alanına bağlanacak uygulamanın adını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-178">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="35a7e-179">**Uygulama** alanına, bağlanılacak Finance ve Supply Chain Management ortamının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-179">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="35a7e-180">**Kiracı** alanına, Finance ve Supply Chain Management ortamının kiracısını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-180">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="35a7e-181">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-181">Select **Save**.</span></span>
6. <span data-ttu-id="35a7e-182">Eylem bölmesinde, ortamla bağlantıyı test etmek için **Bağlantıyı denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-182">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="35a7e-183">Ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-183">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="35a7e-184">Bağlı uygulamaları ortamlara bağlama</span><span class="sxs-lookup"><span data-stu-id="35a7e-184">Link connected applications to environments</span></span>

1. <span data-ttu-id="35a7e-185">**Ortam kurulumları** sayfasında, bir ortama bağlı bir uygulama atamak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-185">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="35a7e-186">**Bağlı uygulama** alanından, bağlı bir uygulama seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-186">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="35a7e-187">**Hizmet ortamı** alanında, bir hizmet ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-187">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="35a7e-188">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-188">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="35a7e-189">Finance ve Supply Chain Management'ta Elektronik faturalama eklentisi tümleştirmesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="35a7e-189">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="35a7e-190">Elektronik faturalama eklenti tümleştirme özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="35a7e-190">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="35a7e-191">Finance veya Supply Chain Management kurulumunuzda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-191">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="35a7e-192">**Özellik yönetimi** çalışma alanında, **Elektronik faturalama eklentisini tümleştirme** özelliğini arayın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-192">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="35a7e-193">Bu özellik sayfada görünmüyorsa **Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-193">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="35a7e-194">Özelliği seçin ve **Şimdi etkinleştir** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-194">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="35a7e-195">Servis uç noktası URL'sini ayarlama</span><span class="sxs-lookup"><span data-stu-id="35a7e-195">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="35a7e-196">**Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-196">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="35a7e-197">**Gönderim hizmeti** sekmesinde, **Hizmet uç noktası URL**'si alanına, aşağıdaki tabloda gösterildiği gibi Azure coğrafyanız için uygun hizmet uç noktasını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-197">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="35a7e-198">Veri merkezi Azure coğrafyası</span><span class="sxs-lookup"><span data-stu-id="35a7e-198">Datacenter Azure geography</span></span> | <span data-ttu-id="35a7e-199">Hizmet uç noktası URL'si</span><span class="sxs-lookup"><span data-stu-id="35a7e-199">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="35a7e-200">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="35a7e-200">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="35a7e-201">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="35a7e-201">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="35a7e-202">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="35a7e-202">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="35a7e-203">Batı AB</span><span class="sxs-lookup"><span data-stu-id="35a7e-203">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="35a7e-204">**Ortam** alanına Elektronik faturalama eklentissi ortamının adını girin.</span><span class="sxs-lookup"><span data-stu-id="35a7e-204">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="35a7e-205">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="35a7e-205">Select **Save**, and then close the page.</span></span>
