---
title: Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlama
description: Bu konu, elektronik faturalama eklentisini kullanmaya nasıl başlayacağınızı açıklar.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592538"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="15fbe-103">Elektronik faturalama eklentisi hizmet yönetimini kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="15fbe-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="15fbe-104">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="15fbe-104">Prerequisites</span></span>

<span data-ttu-id="15fbe-105">Bu konudaki prosedürleri tamamlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:</span><span class="sxs-lookup"><span data-stu-id="15fbe-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="15fbe-106">Microsoft Dynamics Lifecycle Services (LCS) hesabınıza erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="15fbe-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="15fbe-107">Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'ın 10.0.17 veya sonraki sürümünü içeren bir LCS projeniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="15fbe-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="15fbe-108">Ayrıca, bu uygulamaların aşağıdaki Azure coğrafyalarından birinde dağıtılması gerekir:</span><span class="sxs-lookup"><span data-stu-id="15fbe-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="15fbe-109">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="15fbe-109">East US</span></span>
    - <span data-ttu-id="15fbe-110">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="15fbe-110">West US</span></span>
    - <span data-ttu-id="15fbe-111">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="15fbe-111">North EU</span></span>
    - <span data-ttu-id="15fbe-112">Batı AB</span><span class="sxs-lookup"><span data-stu-id="15fbe-112">West EU</span></span>

- <span data-ttu-id="15fbe-113">Dynamics 365 Regulatory Configuration Services (RCS) hesabınıza erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="15fbe-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="15fbe-114">Özellik yönetiminde RCS hesabınız için Globalleştirme özelliğini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="15fbe-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="15fbe-115">Daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="15fbe-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="15fbe-116">Azure'da bir anahtar kasası ve depolama hesabı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="15fbe-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="15fbe-117">Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="15fbe-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="15fbe-118">Lifecycle Services'de mikro hizmetler için eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="15fbe-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="15fbe-119">LCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="15fbe-120">**Önizleme özelliği yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="15fbe-121">**Genel Önizleme Özellikleri** bölümünde, **e-Faturalama hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="15fbe-122">**Önizleme özelliği etkin** seçeneğinin **Evet** olarak ayarlanmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="15fbe-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="15fbe-123">LCS panonuzda, LCS dağıtım projenizi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="15fbe-124">LCS projesi çalışıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="15fbe-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="15fbe-125">**Ortam eklentileri** sekmesinde, **Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="15fbe-126">**E-faturalama hizmetlerini** seçin ve **AAD uygulama kodu** alanına **091c98b0-a1c9-4b02-b62c-7753395ccabe** girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="15fbe-127">Bu sabit bir değerdir.</span><span class="sxs-lookup"><span data-stu-id="15fbe-127">This is a fixed value.</span></span>
10. <span data-ttu-id="15fbe-128">**AAD kiracı kimliği** alanında, Azure abonelik hesabınızın kiracı kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="15fbe-129">Hüküm ve koşulları inceleyin ve ardından onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="15fbe-130">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="15fbe-131">Elektronik faturalama eklentisiyle RCS entegrasyonu için parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="15fbe-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="15fbe-132">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="15fbe-133">**İlgili bağlantılar** içinde, **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="15fbe-134">**e-Faturalama hizmeti** sekmesinde, **Hizmet uç noktası URI**'si alanına, aşağıdaki tabloda gösterildiği gibi Azure coğrafyanız için uygun hizmet uç noktasını girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="15fbe-135">Veri merkezi Azure coğrafyası</span><span class="sxs-lookup"><span data-stu-id="15fbe-135">Datacenter Azure geography</span></span> | <span data-ttu-id="15fbe-136">Hizmet uç noktası URI'si</span><span class="sxs-lookup"><span data-stu-id="15fbe-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="15fbe-137">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="15fbe-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="15fbe-138">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="15fbe-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="15fbe-139">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="15fbe-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="15fbe-140">Batı AB</span><span class="sxs-lookup"><span data-stu-id="15fbe-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="15fbe-141">**Uygulama Kimliği** alanının **0cdb527f-a8d1-4bf8-9436-b352c68682b2** olarak ayarlı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="15fbe-142">Bu değer sabit bir değerdir.</span><span class="sxs-lookup"><span data-stu-id="15fbe-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="15fbe-143">**LCS Ortam Kimliği** alanına LCS abonelik hesabınızın kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="15fbe-144">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="15fbe-145">Key Vault gizli dizisini oluşturma</span><span class="sxs-lookup"><span data-stu-id="15fbe-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="15fbe-146">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="15fbe-147">**Genelleştirme özelliği** çalışma alanında, **Ortam** bölümünde, **Elektronik faturalama eklentisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="15fbe-148">**Ortam kurulumları** sayfasında, Eylem Bölmesi'nde **Hizmet ortamı**'nı ve ardından **Anahtar kasası parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="15fbe-149">Yeni bir anahtar kasası gizli dizisi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="15fbe-150">**Ad** alanına anahtar kasası gizli dizisi adını girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="15fbe-151">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="15fbe-152">**Anahtar Kasası URI**'si alanına, gizli dizi Azure Key Vault'tan yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="15fbe-153">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="15fbe-154">Depolama hesabı gizli dizisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="15fbe-154">Create Storage account secret</span></span>

1. <span data-ttu-id="15fbe-155">**Sistem Yönetimi** > **kurulum** > **Key Vault parametreleri**'ne gidin ve bir anahtar kasası gizli dizisi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="15fbe-156">**Sertifikalar** bölümünde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="15fbe-157">**Ad** alanına, depolama hesabı gizli dizisinin adını girin ve **Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="15fbe-158">**Tür** alanında **Sertifika**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="15fbe-159">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="15fbe-160">Dijital sertifika gizli dizisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="15fbe-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="15fbe-161">**Sistem Yönetimi** > **kurulum** > **Key Vault parametreleri**'ne gidin ve bir anahtar kasası gizli dizisi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="15fbe-162">**Sertifikalar** bölümünde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="15fbe-163">**Ad** alanına, dijital sertifika gizli dizisinin adını girin ve **Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="15fbe-164">**Tür** alanında **Sertifika**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="15fbe-165">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="15fbe-166">Elektronik faturalama eklentisi ortamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="15fbe-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="15fbe-167">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="15fbe-168">**Genelleştirme özelliği** çalışma alanında, **Ortam** bölümünde, **Elektronik faturalama eklentisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="15fbe-169">Hizmet ortamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="15fbe-169">Create a service environment</span></span>

1. <span data-ttu-id="15fbe-170">**Ortam kurulumları** sayfasındaki Eylem bölmesinde **Hizmet ortamı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="15fbe-171">Yeni hizmet ortamı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="15fbe-172">**Ad** alanına E-faturalama ortamının adını girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="15fbe-173">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="15fbe-174">**Depolama SAS belirteci gizli dizisi** alanında, depolama hesabına erişimin kimliğini doğrulamak için kullanılması gereken depolama hesabı gizli dizisinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="15fbe-175">**Kullanıcılar** bölümünde, ortam üzerinden elektronik fatura göndermesine ve ayrıca depolama hesabına bağlanmasına izin verilen bir kullanıcı eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="15fbe-176">**Kullanıcı Kimliği** alanına,kullanıcının diğer adını girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="15fbe-177">**E-posta** alanına kullanıcının e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="15fbe-178">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-178">Select **Save**.</span></span>
8. <span data-ttu-id="15fbe-179">Ülke/bölgenize özgü faturalarınız dijital imzaları uygulamak için bir sertifika zinciri gerektiriyorsa, Eylem bölmesinde **Anahtar kasası parametreleri**'ni seçin, ardından **Sertifikalar zinciri**'ni seçin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="15fbe-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="15fbe-180">Bir sertifika zinciri oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="15fbe-181">**Ad** alanına sertifika zinciri adını girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="15fbe-182">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="15fbe-183">**Sertifikalar** bölümünde, zincire sertifika eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="15fbe-184">Sertifikanın zincirdeki konumunu değiştirmek için **Yukarı** veya **Aşağı** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="15fbe-185">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="15fbe-186">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-186">Close the page.</span></span>
9. <span data-ttu-id="15fbe-187">**Hizmet ortamı** sayfasında, Eylem Bölmesi'nde, ortamı bulutta yayınlamak için **Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="15fbe-188">**Durum** alanının değeri **Yayınlandı** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="15fbe-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="15fbe-189">Bağlı bir uygulama oluşturma</span><span class="sxs-lookup"><span data-stu-id="15fbe-189">Create a connected application</span></span>

1. <span data-ttu-id="15fbe-190">**Ortam kurulumları** sayfasındaki Eylem bölmesinde **Bağlı uygulamalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="15fbe-191">Yeni bir bağlı uygulama oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="15fbe-192">**Ad** alanına bağlanacak uygulamanın adını girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="15fbe-193">**Uygulama** alanına, bağlanılacak Finance ve Supply Chain Management ortamının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="15fbe-194">**Kiracı** alanına, Finance ve Supply Chain Management ortamının kiracısını girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="15fbe-195">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-195">Select **Save**.</span></span>
6. <span data-ttu-id="15fbe-196">Eylem bölmesinde, ortamla bağlantıyı test etmek için **Bağlantıyı denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="15fbe-197">Ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="15fbe-198">Bağlı uygulamaları ortamlara bağlama</span><span class="sxs-lookup"><span data-stu-id="15fbe-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="15fbe-199">**Ortam kurulumları** sayfasında, bir ortama bağlı bir uygulama atamak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="15fbe-200">**Bağlı uygulama** alanından, bağlı bir uygulama seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="15fbe-201">**Hizmet ortamı** alanında, bir hizmet ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="15fbe-202">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="15fbe-203">Finance ve Supply Chain Management'ta Elektronik faturalama eklentisi tümleştirmesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="15fbe-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="15fbe-204">Elektronik faturalama eklenti tümleştirme özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="15fbe-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="15fbe-205">Finance veya Supply Chain Management kurulumunuzda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="15fbe-206">**Özellik yönetimi** çalışma alanında, **Elektronik faturalama eklentisini tümleştirme** özelliğini arayın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="15fbe-207">Bu özellik sayfada görünmüyorsa **Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="15fbe-208">Özelliği seçin ve **Şimdi etkinleştir** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="15fbe-209">Servis uç noktası URL'sini ayarlama</span><span class="sxs-lookup"><span data-stu-id="15fbe-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="15fbe-210">**Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="15fbe-211">**Gönderim hizmeti** sekmesinde, **Hizmet uç noktası URL**'si alanına, aşağıdaki tabloda gösterildiği gibi Azure coğrafyanız için uygun hizmet uç noktasını girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="15fbe-212">Veri merkezi Azure coğrafyası</span><span class="sxs-lookup"><span data-stu-id="15fbe-212">Datacenter Azure geography</span></span> | <span data-ttu-id="15fbe-213">Hizmet uç noktası URL'si</span><span class="sxs-lookup"><span data-stu-id="15fbe-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="15fbe-214">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="15fbe-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="15fbe-215">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="15fbe-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="15fbe-216">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="15fbe-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="15fbe-217">Batı AB</span><span class="sxs-lookup"><span data-stu-id="15fbe-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="15fbe-218">**Ortam** alanına Elektronik faturalama eklentissi ortamının adını girin.</span><span class="sxs-lookup"><span data-stu-id="15fbe-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="15fbe-219">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="15fbe-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
