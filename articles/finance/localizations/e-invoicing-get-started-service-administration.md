---
title: Elektronik faturalama hizmet yönetimini kullanmaya başlama
description: Bu konu, elektronik faturalamayı kullanmaya nasıl başlayacağınızı açıklar.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ec431cb4a3620459d905f64a80fd820a2113290f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840160"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="fdc92-103">Elektronik faturalama hizmet yönetimini kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="fdc92-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="fdc92-104">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="fdc92-104">Prerequisites</span></span>

<span data-ttu-id="fdc92-105">Bu konudaki prosedürleri tamamlamadan önce, aşağıdaki önkoşulların yerine getirilmesi gerekir:</span><span class="sxs-lookup"><span data-stu-id="fdc92-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="fdc92-106">Microsoft Dynamics Lifecycle Services (LCS) hesabınıza erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fdc92-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="fdc92-107">Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management'ın 10.0.17 veya sonraki sürümünü içeren bir LCS projeniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fdc92-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fdc92-108">Ayrıca, bu uygulamaların aşağıdaki Azure coğrafyalarından birinde dağıtılması gerekir:</span><span class="sxs-lookup"><span data-stu-id="fdc92-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="fdc92-109">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="fdc92-109">East US</span></span>
    - <span data-ttu-id="fdc92-110">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="fdc92-110">West US</span></span>
    - <span data-ttu-id="fdc92-111">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="fdc92-111">North EU</span></span>
    - <span data-ttu-id="fdc92-112">Batı AB</span><span class="sxs-lookup"><span data-stu-id="fdc92-112">West EU</span></span>

- <span data-ttu-id="fdc92-113">Dynamics 365 Regulatory Configuration Services (RCS) hesabınıza erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fdc92-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="fdc92-114">Özellik yönetiminde RCS hesabınız için Globalleştirme özelliğini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="fdc92-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="fdc92-115">Daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="fdc92-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="fdc92-116">Azure'da bir anahtar kasası ve depolama hesabı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="fdc92-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="fdc92-117">Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="fdc92-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="fdc92-118">Lifecycle Services'de mikro hizmetler için eklentiyi yükleme</span><span class="sxs-lookup"><span data-stu-id="fdc92-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="fdc92-119">LCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="fdc92-120">**Önizleme özelliği yönetimi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="fdc92-121">**Genel Önizleme Özellikleri** bölümünde, **e-Faturalama hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="fdc92-122">**Önizleme özelliği etkin** seçeneğinin **Evet** olarak ayarlanmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="fdc92-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="fdc92-123">LCS panonuzda, LCS dağıtım projenizi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="fdc92-124">LCS projesi çalışıyor olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fdc92-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="fdc92-125">**Ortam eklentileri** sekmesinde, **Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="fdc92-126">**E-faturalama hizmetlerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-126">Select **e-invoicing Services**.</span></span>
9. <span data-ttu-id="fdc92-127">**AAD uygulama kodu** alanına şunu girin: **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span><span class="sxs-lookup"><span data-stu-id="fdc92-127">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="fdc92-128">Bu sabit bir değerdir.</span><span class="sxs-lookup"><span data-stu-id="fdc92-128">This is a fixed value.</span></span>
10. <span data-ttu-id="fdc92-129">**AAD kiracı kimliği** alanında, Azure abonelik hesabınızın kiracı kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-129">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="fdc92-130">Hüküm ve koşulları inceleyin ve ardından onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-130">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="fdc92-131">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-131">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="fdc92-132">Elektronik faturalamayla RCS entegrasyonu için parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="fdc92-132">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="fdc92-133">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-133">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="fdc92-134">**İlgili bağlantılar** içinde, **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-134">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="fdc92-135">**e-Faturalama hizmeti** sekmesinde, **Hizmet uç noktası URI**'si alanına, aşağıdaki tabloda gösterildiği gibi Azure coğrafyanız için uygun hizmet uç noktasını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-135">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="fdc92-136">Veri merkezi Azure coğrafyası</span><span class="sxs-lookup"><span data-stu-id="fdc92-136">Datacenter Azure geography</span></span> | <span data-ttu-id="fdc92-137">Hizmet uç noktası URI'si</span><span class="sxs-lookup"><span data-stu-id="fdc92-137">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="fdc92-138">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="fdc92-138">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="fdc92-139">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="fdc92-139">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="fdc92-140">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="fdc92-140">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="fdc92-141">Batı AB</span><span class="sxs-lookup"><span data-stu-id="fdc92-141">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="fdc92-142">**Uygulama Kimliği** alanının **0cdb527f-a8d1-4bf8-9436-b352c68682b2** olarak ayarlı olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-142">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="fdc92-143">Bu değer sabit bir değerdir.</span><span class="sxs-lookup"><span data-stu-id="fdc92-143">This value is a fixed value.</span></span>
5. <span data-ttu-id="fdc92-144">**LCS Ortam Kimliği** alanına LCS ortamınızın kimliğini girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-144">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="fdc92-145">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-145">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="fdc92-146">Key Vault başvuruları oluşturma</span><span class="sxs-lookup"><span data-stu-id="fdc92-146">Create Key Vault references</span></span>

1. <span data-ttu-id="fdc92-147">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-147">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="fdc92-148">**Genelleştirme özelliği** çalışma alanında, **Ortam** bölümünde, **Elektronik faturalama** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-148">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="fdc92-149">**Ortam kurulumları** sayfasında, Eylem Bölmesi'nde **Hizmet ortamı**'nı ve ardından **Anahtar kasası parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-149">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="fdc92-150">Key Vault başvurusu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-150">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="fdc92-151">**Ad** alanına Key Vault başvurusunun adını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-151">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="fdc92-152">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-152">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="fdc92-153">**Key Vault URI** alanına, key vault gizli dizisini Azure Key Vault'tan yapıştırın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-153">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="fdc92-154">Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="fdc92-154">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="fdc92-155">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-155">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="fdc92-156">Depolama hesabı gizli dizisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="fdc92-156">Create Storage account secret</span></span>

1. <span data-ttu-id="fdc92-157">**Ortam kurulumları** sayfasında, Eylem Bölmesi'nde **Hizmet ortamı** > **Key Vault parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-157">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="fdc92-158">Bir **Key Vault başvurusu** seçin ve **Sertifikalar** bölümünde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-158">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="fdc92-159">**Ad** alanına depolama hesabı gizli dizisinin adını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-159">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="fdc92-160">Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="fdc92-160">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="fdc92-161">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-161">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="fdc92-162">**Tür** alanında **Gizli Dizi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-162">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="fdc92-163">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-163">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="fdc92-164">Dijital sertifika gizli dizisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="fdc92-164">Create a digital certificate secret</span></span>

1. <span data-ttu-id="fdc92-165">**Ortam kurulumları** sayfasında, Eylem Bölmesi'nde **Hizmet ortamı**'nı ve ardından **Key Vault parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-165">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="fdc92-166">Bir **Key Vault başvurusu** seçin ve ardından **Sertifikalar** bölümünde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-166">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="fdc92-167">**Ad** alanına dijital sertifika gizli dizisinin adını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-167">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="fdc92-168">Daha fazla bilgi için bkz. [Azure depolama hesabı ve bir anahtar kasası oluşturma](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="fdc92-168">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="fdc92-169">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-169">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="fdc92-170">**Tür** alanında **Sertifika**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-170">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="fdc92-171">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-171">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="fdc92-172">Hizmet ortamı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fdc92-172">Create a service environment</span></span>

1. <span data-ttu-id="fdc92-173">RCS hesabınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-173">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="fdc92-174">**Genelleştirme özelliği** çalışma alanında, **Ortam** bölümünde, **Elektronik faturalama** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-174">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="fdc92-175">**Ortam kurulumları** sayfasındaki Eylem bölmesinde **Hizmet ortamı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-175">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="fdc92-176">Yeni hizmet ortamı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-176">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="fdc92-177">**Ad** alanına E-faturalama ortamının adını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-177">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="fdc92-178">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-178">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="fdc92-179">**Depolama SAS belirteci gizli dizisi** alanında, depolama hesabına erişimin kimliğini doğrulamak için kullanılması gereken depolama hesabı gizli dizisinin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-179">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="fdc92-180">**Kullanıcılar** bölümünde, ortam üzerinden elektronik fatura göndermesine ve ayrıca depolama hesabına bağlanmasına izin verilen bir kullanıcı eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-180">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="fdc92-181">**Kullanıcı Kimliği** alanına,kullanıcının diğer adını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-181">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="fdc92-182">**E-posta** alanına kullanıcının e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-182">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="fdc92-183">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-183">Select **Save**.</span></span>
10. <span data-ttu-id="fdc92-184">Ülke/bölgenize özgü faturalarınız dijital imzaları uygulamak için bir sertifika zinciri gerektiriyorsa, Eylem bölmesinde **Anahtar kasası parametreleri**'ni seçin, ardından **Sertifikalar zinciri**'ni seçin ve şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="fdc92-184">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="fdc92-185">Bir sertifika zinciri oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-185">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="fdc92-186">**Ad** alanına sertifika zinciri adını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-186">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="fdc92-187">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-187">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="fdc92-188">**Sertifikalar** bölümünde, zincire sertifika eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-188">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="fdc92-189">Sertifikanın zincirdeki konumunu değiştirmek için **Yukarı** veya **Aşağı** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-189">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="fdc92-190">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-190">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="fdc92-191">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-191">Close the page.</span></span>
11. <span data-ttu-id="fdc92-192">**Hizmet ortamı** sayfasında, Eylem Bölmesi'nde, ortamı bulutta yayınlamak için **Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-192">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="fdc92-193">**Durum** alanının değeri **Yayınlandı** olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="fdc92-193">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="fdc92-194">Bağlı bir uygulama oluşturma</span><span class="sxs-lookup"><span data-stu-id="fdc92-194">Create a connected application</span></span>

1. <span data-ttu-id="fdc92-195">**Ortam kurulumları** sayfasındaki Eylem bölmesinde **Bağlı uygulamalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-195">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="fdc92-196">Yeni bir bağlı uygulama oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-196">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="fdc92-197">**Ad** alanına bağlanacak uygulamanın adını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-197">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="fdc92-198">**Uygulama** alanına, bağlanılacak Finance ve Supply Chain Management ortamının URL'sini girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-198">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="fdc92-199">**Kiracı** alanına, Finance ve Supply Chain Management ortamının kiracısını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-199">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="fdc92-200">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-200">Select **Save**.</span></span>
6. <span data-ttu-id="fdc92-201">Eylem bölmesinde, ortamla bağlantıyı test etmek için **Bağlantıyı denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-201">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="fdc92-202">Ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-202">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="fdc92-203">Bağlı uygulamaları ortamlara bağlama</span><span class="sxs-lookup"><span data-stu-id="fdc92-203">Link connected applications to environments</span></span>

1. <span data-ttu-id="fdc92-204">**Ortam kurulumları** sayfasında, bir ortama bağlı bir uygulama atamak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-204">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="fdc92-205">**Bağlı uygulama** alanından, bağlı bir uygulama seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-205">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="fdc92-206">**Hizmet ortamı** alanında, bir hizmet ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-206">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="fdc92-207">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-207">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="fdc92-208">Finance ve Supply Chain Management uygulamalarında Elektronik faturalama kurulumu</span><span class="sxs-lookup"><span data-stu-id="fdc92-208">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="fdc92-209">Elektronik faturalama tümleştirme özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="fdc92-209">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="fdc92-210">Finance veya Supply Chain Management kurulumunuzda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-210">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="fdc92-211">**Özellik yönetimi** çalışma alanında, **Elektronik faturalamayı tümleştirme** özelliğini arayın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-211">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="fdc92-212">Bu özellik sayfada görünmüyorsa **Güncelleştirmeleri denetle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-212">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="fdc92-213">Özelliği seçin ve **Şimdi etkinleştir** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-213">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="fdc92-214">Servis uç noktası URL'sini ayarlama</span><span class="sxs-lookup"><span data-stu-id="fdc92-214">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="fdc92-215">**Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-215">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="fdc92-216">**Gönderim hizmeti** sekmesinde, **Hizmet uç noktası URL**'si alanına, aşağıdaki tabloda gösterildiği gibi Azure coğrafyanız için uygun hizmet uç noktasını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-216">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="fdc92-217">Veri merkezi Azure coğrafyası</span><span class="sxs-lookup"><span data-stu-id="fdc92-217">Datacenter Azure geography</span></span> | <span data-ttu-id="fdc92-218">Hizmet uç noktası URL'si</span><span class="sxs-lookup"><span data-stu-id="fdc92-218">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="fdc92-219">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="fdc92-219">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="fdc92-220">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="fdc92-220">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="fdc92-221">Kuzey AB</span><span class="sxs-lookup"><span data-stu-id="fdc92-221">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="fdc92-222">Batı AB</span><span class="sxs-lookup"><span data-stu-id="fdc92-222">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="fdc92-223">**Ortam** alanına Elektronik faturalamada yayınlanan hizmet ortamının adını girin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-223">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="fdc92-224">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fdc92-224">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="fdc92-225">Deneme anahtarlarını etkinleştir</span><span class="sxs-lookup"><span data-stu-id="fdc92-225">Enable Flighting keys</span></span>

<span data-ttu-id="fdc92-226">Microsoft Dynamics 365 Finance veya Microsoft Dynamics 365 Supply Chain Management sürümleri 10.0.17 veya öncesi için deneme anahtarlarını etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-226">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="fdc92-227">Aşağıdaki SQL komutunu çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="fdc92-227">Execute the following SQL command:</span></span>

    <span data-ttu-id="fdc92-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span><span class="sxs-lookup"><span data-stu-id="fdc92-228">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="fdc92-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span><span class="sxs-lookup"><span data-stu-id="fdc92-229">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="fdc92-230">Tüm AOS işlemleri için IISreset komutu gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="fdc92-230">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
