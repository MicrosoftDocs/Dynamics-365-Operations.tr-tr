---
title: RCS'deki/Genel depodaki ER yapılandırmalarını harici kuruluşlarla paylaşma
description: Bu konuda, Microsoft Regulatory Configuration Services (RCS)/Genel depodaki Elektronik raporlama (ER) yapılandırmalarının harici kuruluşlarla doğrudan nasıl paylaşılacağı açıklanmaktadır.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0973d36a8fddd16d02776ac6567d424ac6ebc3ae
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994326"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="d7f9b-103">Regulatory Configuration Services (RCS)/Genel depodaki Elektronik raporlama (ER) yapılandırmalarını harici kuruluşlarla paylaşma</span><span class="sxs-lookup"><span data-stu-id="d7f9b-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7f9b-104">Elektronik raporlama (ER) yapılandırmalarını paylaşmak ve harici kuruluşlara yayımlamak için Microsoft Regulatory Configuration Services'ı (RCS) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="d7f9b-105">Aşağıdaki yordamlarda, bir RCS kullanıcısının harici kuruluşla bir RCS örneğinde yapılandırılmış bir ER yapılandırmasının sürümünü nasıl paylaşabileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="d7f9b-106">Bu yordamları tamamlamadan önce aşağıdaki önkoşulları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="d7f9b-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="d7f9b-107">RCS örneğine erişin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-107">Access an RCS instance.</span></span>
- <span data-ttu-id="d7f9b-108">Etkin bir yapılandırma sağlayıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-108">Create an active configuration provider.</span></span> <span data-ttu-id="d7f9b-109">Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d7f9b-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="d7f9b-110">ER yapılandırmasının yeni bir sürümünü oluşturun ve yükleyin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="d7f9b-111">Daha fazla bilgi için bkz. [Elektronik raporlama (ER) yapılandırmasının yeni bir sürümünü oluşturma ve yükleme](rcs-global-repo-upload.md).</span><span class="sxs-lookup"><span data-stu-id="d7f9b-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="d7f9b-112">Ayrıca, şirketiniz için bir RCS ortamının sağlandığından da emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="d7f9b-113">Finance and Operations uygulamasında, **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="d7f9b-114">Şirketiniz için hiçbir RCS ortamı sağlanmamışsa **Regulatory services - Harici yapılandırma**'yı seçin ve ardından bir ortam sağlamak için yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="d7f9b-115">Şirketiniz için zaten bir RCS ortamı sağlanmışsa oturum açma seçeneğini belirleyerek bu URL'ye erişmek için sayfa URL'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="d7f9b-116">Paylaşmak istediğiniz yapılandırmayı doğrulama</span><span class="sxs-lookup"><span data-stu-id="d7f9b-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="d7f9b-117">Paylaşmak istediğiniz yapılandırmanın Genel depoya önceden yüklenmiş olduğundan emin olmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="d7f9b-118">**Elektronik raporlama** çalışma alanında, yapılandırma sağlayıcınız için **Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![Konfigürasyon sağlayıcıları](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="d7f9b-120">**Genel havuz** \> **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="d7f9b-121">Paylaşmak istediğiniz yapılandırmayı arayın.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="d7f9b-122">Aramanızı daraltmak için filtre alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="d7f9b-123">Yapılandırmayı Genel depoda bulamazsanız [Elektronik raporlama (ER) yapılandırmasının yeni bir sürümünü oluşturma ve yükleme](rcs-global-repo-upload.md) konusundaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="d7f9b-124">ER yapılandırmalarını harici kuruluşlarla paylaşma</span><span class="sxs-lookup"><span data-stu-id="d7f9b-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="d7f9b-125">Yapılandırma sağlayıcınız altında bir yapılandırma oluşturulduktan sonra, **Genel yapılandırma deposu** sayfasındaki **Paylaşıldı** hızlı sekmesini kullanarak harici kuruluşlarla bunu doğrudan paylaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="d7f9b-126">**Elektronik raporlama** çalışma alanında, yapılandırma sağlayıcınız için **Depolar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="d7f9b-127">**Genel havuz** \> **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="d7f9b-128">Paylaşmak istediğiniz yapılandırmayı seçin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="d7f9b-129">**Paylaşıldı** hızlı sekmesinde **Kuruluş**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![Paylaşıldı hızlı sekmesi](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="d7f9b-131">İletişim kutusunda, harici kuruluşun etki alanı adını girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![Yapılandırma sürümünü harici kuruluş ile paylaş iletişim kutusu](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="d7f9b-133">Yapılandırma, harici kuruluşla paylaşılır ve Genel depodaki bu kuruluş tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="d7f9b-134">Buradan, kuruluşun RCS örneğine veya Finance and Operations uygulama örneklerine içe aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="d7f9b-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="d7f9b-135">Daha önce harici bir kuruluşla paylaşılan bir yapılandırmanın paylaşımını kaldırmak için yapılandırmayı seçin ve **Paylaşımı kaldır**'ı, ardından **Tamam**'ı seçin</span><span class="sxs-lookup"><span data-stu-id="d7f9b-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>
