---
title: RCS'de ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme
description: Bu konuda, Microsoft Regulatory Configuration Services (RCS) içinde Elektronik raporlama (ER) yapılandırmasının nasıl oluşturulacağı ve Genel depoya nasıl yükleneceği açıklanmaktadır.
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834245"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="f22f6-103">Regulatory Configuration Services (RCS) içinde ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme</span><span class="sxs-lookup"><span data-stu-id="f22f6-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f22f6-104">Elektronik raporlama (ER) yapılandırmalarını tasarlamak ve kuruluşunuzda kullanılabilmeleri için yayımlamak üzere Microsoft Regulatory Configuration Services'ı (RCS) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f22f6-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="f22f6-105">Aşağıdaki yordamlarda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının bir RCS örneğinde yapılandırılmış ER yapılandırmasının türetilmiş bir sürümünü nasıl oluşturabileceği ve sonra türetilmiş yapılandırmayı Genel depoya nasıl yükleyebileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f22f6-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="f22f6-106">Bu yordamları tamamlamadan önce aşağıdaki önkoşulları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="f22f6-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="f22f6-107">RCS örneğine erişin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-107">Access an RCS instance.</span></span>
- <span data-ttu-id="f22f6-108">Etkin bir yapılandırma sağlayıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f22f6-108">Create an active configuration provider.</span></span> <span data-ttu-id="f22f6-109">Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f22f6-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="f22f6-110">Ayrıca, şirketiniz için bir RCS ortamının sağlandığından da emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="f22f6-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="f22f6-111">Finance and Operations uygulamasında, **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f22f6-112">Şirketiniz için hiçbir RCS ortamı sağlanmamışsa **Regulatory services - Harici yapılandırma**'yı seçin ve ardından bir ortam sağlamak için yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="f22f6-113">Şirketiniz için zaten bir RCS ortamı sağlanmışsa oturum açma seçeneğini belirleyerek bu URL'ye erişmek için sayfa URL'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f22f6-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="f22f6-114">RCS'de yapılandırmanın türetilmiş bir sürümünü oluşturma</span><span class="sxs-lookup"><span data-stu-id="f22f6-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="f22f6-115">**Elektronik raporlama** çalışma alanında, kuruluşunuz için etkin bir yapılandırma sağlayıcınız olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="f22f6-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="f22f6-116">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="f22f6-117">Yeni bir sürüm türetmek istediğiniz yapılandırmayı seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="f22f6-118">Aramanızı daraltmak için ağacın üzerindeki filtre alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f22f6-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="f22f6-119">**Yapılandırma oluştur** \> **İsimden Türet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="f22f6-120">Ad ve açıklama girin ve ardından yeni bir türetilmiş sürüm oluşturmak için **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="f22f6-121">Yeni türetilen yapılandırmayı seçin, sürümün bir tanımını ekleyin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="f22f6-122">Yapılacak yapılandırmanın durumu **Tamamlandı** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="f22f6-122">The status of the configuration to is changed to **Completed**.</span></span>

![RCS'de yeni yapılandırma sürümü](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="f22f6-124">Yapılandırma durumu değiştirildiğinde bağlı uygulamalarla ilgili bir doğrulama hata mesajı alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f22f6-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="f22f6-125">Doğrulamayı kapatmak için **Yapılandırmalar** sekmesindeki Eylem Bölmesi'nde, **Kullanıcı parametreleri**'ni seçin ve ardından **Yapılandırmanın durum değişikliği ve yeniden temellendirmede doğrulamayı atla** seçeneğini **Evet** olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="f22f6-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="f22f6-126">Genel depoya bir yapılandırma yükleme</span><span class="sxs-lookup"><span data-stu-id="f22f6-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="f22f6-127">Kuruluşunuzla, yeni veya türetilmiş bir yapılandırmayı paylaşmak için yapılandırmayı Genel depoya yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f22f6-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="f22f6-128">Yapılandırmanın tamamlanmış sürümünü ve ardından **Depoya yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="f22f6-129">**Genel (Microsoft)** seçeneğini ve ardından **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Depo seçeneklerine yükleme](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="f22f6-131">Onay iletisi kutusunda **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="f22f6-132">Sürümün açıklamasını gerektiği gibi güncelleştirin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="f22f6-133">Yapılandırmanın durumu **Paylaş** olarak güncelleştirilir ve yapılandırma Genel depoya yüklenir.</span><span class="sxs-lookup"><span data-stu-id="f22f6-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="f22f6-134">Oradan, aşağıdaki yollarla çalışabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f22f6-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="f22f6-135">Dynamics 365 örneğinize aktarın.</span><span class="sxs-lookup"><span data-stu-id="f22f6-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="f22f6-136">Daha fazla bilgi için bkz. [(ER) Yapılandırmaları RCS'den içe aktarma](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="f22f6-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="f22f6-137">Üçüncü tarafla veya harici bir kuruluşla paylaşmak için bkz. [RCS, Elektronik raporlama (ER) yapılandırmalarını harici kuruluşlarla paylaşma](rcs-global-repo-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="f22f6-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![Genel depodaki Türetilmiş Intrastat Contoso yapılandırma sürümü](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="f22f6-139">Genel depodan bir yapılandırma silme</span><span class="sxs-lookup"><span data-stu-id="f22f6-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="f22f6-140">Kuruluşunuzun oluşturmuş olduğu bir yapılandırmayı silmek için aşağıdaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="f22f6-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="f22f6-141">**Elektronik raporlama** çalışma alanında, yapılandırma sağlayıcınızın **Etkin** olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="f22f6-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="f22f6-142">Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f22f6-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="f22f6-143">Etkin yapılandırma sağlayıcınızda, **Depo**'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="f22f6-144">Havuz türünü **Genel** olarak seçin ve **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="f22f6-145">**Filtre** hızlı sekmesinde, **Filtre** işlevini kullanarak silmek istediğiniz yapılandırmayı bulun.</span><span class="sxs-lookup"><span data-stu-id="f22f6-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="f22f6-146">**Sürüm** hızlı sekmesinde, silmek istediğiniz yapılandırmayla ilgili sürümü seçin ve **Sil**'i seçin:</span><span class="sxs-lookup"><span data-stu-id="f22f6-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![Genel depodan bir yapılandırma silme](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="f22f6-148">Onay iletisi kutusunda **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f22f6-148">In the confirmation message box, select **Yes**.</span></span>

    ![Yapılandırma sürümü onay iletisini silme](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="f22f6-150">Yapılandırma sürümü silindi ve onay iletisi gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="f22f6-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="f22f6-151">Yapılandırmalar yalnızca kendilerini oluşturan Yapılandırma sağlayıcısı tarafından silinebilir.</span><span class="sxs-lookup"><span data-stu-id="f22f6-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="f22f6-152">Yapılandırma başka bir kuruluşla paylaşılıyorsa, silmeden önce bu yapılandırmanın paylaşımdan kaldırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f22f6-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 
