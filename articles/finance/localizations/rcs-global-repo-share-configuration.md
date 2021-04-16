---
title: RCS'deki/Genel depodaki ER yapılandırmalarını harici kuruluşlarla paylaşma
description: Bu konuda, Microsoft Regulatory Configuration Services (RCS)/Genel depodaki Elektronik raporlama (ER) yapılandırmalarının harici kuruluşlarla doğrudan nasıl paylaşılacağı açıklanmaktadır.
author: JaneA07
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ace62319bbfa38bcf4be7157882dd0c8989e25bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838757"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="401cb-103">Regulatory Configuration Services (RCS)/Genel depodaki Elektronik raporlama (ER) yapılandırmalarını harici kuruluşlarla paylaşma</span><span class="sxs-lookup"><span data-stu-id="401cb-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="401cb-104">Elektronik raporlama (ER) yapılandırmalarını paylaşmak ve harici kuruluşlara yayımlamak için Microsoft Regulatory Configuration Services'ı (RCS) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="401cb-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="401cb-105">Aşağıdaki yordamlarda, bir RCS kullanıcısının harici kuruluşla bir RCS örneğinde yapılandırılmış bir ER yapılandırmasının sürümünü nasıl paylaşabileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="401cb-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="401cb-106">Bu yordamları tamamlamadan önce aşağıdaki önkoşulları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="401cb-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="401cb-107">RCS örneğine erişin.</span><span class="sxs-lookup"><span data-stu-id="401cb-107">Access an RCS instance.</span></span>
- <span data-ttu-id="401cb-108">Etkin bir yapılandırma sağlayıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="401cb-108">Create an active configuration provider.</span></span> <span data-ttu-id="401cb-109">Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="401cb-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="401cb-110">ER yapılandırmasının yeni bir sürümünü oluşturun ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="401cb-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="401cb-111">Daha fazla bilgi için bkz. [Elektronik raporlama (ER) yapılandırmasının yeni bir sürümünü oluşturma ve yükleme](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="401cb-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="401cb-112">Ayrıca, şirketiniz için bir RCS ortamının sağlandığından da emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="401cb-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="401cb-113">Finance and Operations uygulamasında, **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="401cb-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="401cb-114">Şirketiniz için hiçbir RCS ortamı sağlanmamışsa **Regulatory services - Harici yapılandırma**'yı seçin ve ardından bir ortam sağlamak için yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="401cb-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="401cb-115">Şirketiniz için zaten bir RCS ortamı sağlanmışsa oturum açma seçeneğini belirleyerek bu URL'ye erişmek için sayfa URL'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="401cb-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="401cb-116">Paylaşmak istediğiniz yapılandırmayı doğrulama</span><span class="sxs-lookup"><span data-stu-id="401cb-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="401cb-117">Paylaşmak istediğiniz yapılandırmanın Genel depoya önceden yüklenmiş olduğundan emin olmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="401cb-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="401cb-118">**Elektronik raporlama** çalışma alanında, yapılandırma sağlayıcınız için **Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="401cb-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Konfigürasyon sağlayıcıları](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="401cb-120">**Genel havuz** \> **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="401cb-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="401cb-121">Paylaşmak istediğiniz yapılandırmayı arayın.</span><span class="sxs-lookup"><span data-stu-id="401cb-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="401cb-122">Aramanızı daraltmak için filtre alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="401cb-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="401cb-123">Yapılandırmayı Genel depoda bulamazsanız [Elektronik raporlama (ER) yapılandırmasının yeni bir sürümünü oluşturma ve yükleme](rcs-global-repo-upload.md) konusundaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="401cb-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="401cb-124">ER yapılandırmalarını harici kuruluşlarla paylaşma</span><span class="sxs-lookup"><span data-stu-id="401cb-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="401cb-125">Yapılandırma sağlayıcınız altında bir yapılandırma oluşturulduktan sonra, **Genel yapılandırma deposu** sayfasındaki **Paylaşıldı** hızlı sekmesini kullanarak harici kuruluşlarla bunu doğrudan paylaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="401cb-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="401cb-126">**Elektronik raporlama** çalışma alanında, yapılandırma sağlayıcınız için **Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="401cb-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="401cb-127">**Genel havuz** \> **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="401cb-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="401cb-128">Paylaşmak istediğiniz yapılandırmayı seçin.</span><span class="sxs-lookup"><span data-stu-id="401cb-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="401cb-129">**Paylaşıldı** hızlı sekmesinde **Kuruluş**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="401cb-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Paylaşıldı hızlı sekmesi](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="401cb-131">İletişim kutusunda, harici kuruluşun etki alanı adını girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="401cb-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Yapılandırma sürümünü harici kuruluş ile paylaş iletişim kutusu](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="401cb-133">Yapılandırma, harici kuruluşla paylaşılır ve Genel depodaki bu kuruluş tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="401cb-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="401cb-134">Buradan, kuruluşun RCS örneğine veya Finance and Operations uygulama örneklerine içe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="401cb-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="401cb-135">Daha önce harici bir kuruluşla paylaşılan bir yapılandırmanın paylaşımını kaldırmak için yapılandırmayı seçin ve **Paylaşımı kaldır**'ı, ardından **Tamam**'ı seçin</span><span class="sxs-lookup"><span data-stu-id="401cb-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]