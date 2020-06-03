---
title: RCS'de ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme
description: Bu konuda, Microsoft Regulatory Configuration Services (RCS) içinde Elektronik raporlama (ER) yapılandırmasının nasıl oluşturulacağı ve Genel depoya nasıl yükleneceği açıklanmaktadır.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
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
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371273"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="65a6c-103">Regulatory Configuration Services (RCS) içinde ER yapılandırmaları oluşturma ve bunları Genel depoya yükleme</span><span class="sxs-lookup"><span data-stu-id="65a6c-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65a6c-104">Elektronik raporlama (ER) yapılandırmalarını tasarlamak ve kuruluşunuzda kullanılabilmeleri için yayımlamak üzere Microsoft Regulatory Configuration Services'ı (RCS) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65a6c-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="65a6c-105">Aşağıdaki yordamlarda, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının bir RCS örneğinde yapılandırılmış ER yapılandırmasının türetilmiş bir sürümünü nasıl oluşturabileceği ve sonra türetilmiş yapılandırmayı Genel depoya nasıl yükleyebileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="65a6c-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="65a6c-106">Bu yordamları tamamlamadan önce aşağıdaki önkoşulları tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="65a6c-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="65a6c-107">RCS örneğine erişin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-107">Access an RCS instance.</span></span>
- <span data-ttu-id="65a6c-108">Etkin bir yapılandırma sağlayıcısı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="65a6c-108">Create an active configuration provider.</span></span> <span data-ttu-id="65a6c-109">Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="65a6c-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="65a6c-110">Ayrıca, şirketiniz için bir RCS ortamının sağlandığından da emin olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="65a6c-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="65a6c-111">Finance and Operations uygulamasında, **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="65a6c-112">Şirketiniz için hiçbir RCS ortamı sağlanmamışsa **Regulatory services - Harici yapılandırma**'yı seçin ve ardından bir ortam sağlamak için yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="65a6c-113">Şirketiniz için zaten bir RCS ortamı sağlanmışsa oturum açma seçeneğini belirleyerek bu URL'ye erişmek için sayfa URL'sini kullanın.</span><span class="sxs-lookup"><span data-stu-id="65a6c-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="65a6c-114">RCS'de yapılandırmanın türetilmiş bir sürümünü oluşturma</span><span class="sxs-lookup"><span data-stu-id="65a6c-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="65a6c-115">**Elektronik raporlama** çalışma alanında, kuruluşunuz için etkin bir yapılandırma sağlayıcınız olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="65a6c-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="65a6c-116">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="65a6c-117">Yeni bir sürüm türetmek istediğiniz yapılandırmayı seçin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="65a6c-118">Aramanızı daraltmak için ağacın üzerindeki filtre alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65a6c-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="65a6c-119">**Yapılandırma oluştur** \> **İsimden Türet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="65a6c-120">Ad ve açıklama girin ve ardından yeni bir türetilmiş sürüm oluşturmak için **Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="65a6c-121">Yeni türetilen yapılandırmayı seçin, sürümün bir tanımını ekleyin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="65a6c-122">Yapılacak yapılandırmanın durumu **Tamamlandı** olarak değişir.</span><span class="sxs-lookup"><span data-stu-id="65a6c-122">The status of the configuration to is changed to **Completed**.</span></span>

![RCS'de yeni yapılandırma sürümü](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="65a6c-124">Yapılandırma durumu değiştirildiğinde bağlı uygulamalarla ilgili bir doğrulama hata mesajı alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65a6c-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="65a6c-125">Doğrulamayı kapatmak için **Yapılandırmalar** sekmesindeki Eylem Bölmesi'nde, **Kullanıcı parametreleri**'ni seçin ve ardından **Yapılandırmanın durum değişikliği ve yeniden temellendirmede doğrulamayı atla** seçeneğini **Evet** olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="65a6c-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="65a6c-126">Genel depoya bir yapılandırma yükleme</span><span class="sxs-lookup"><span data-stu-id="65a6c-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="65a6c-127">Kuruluşunuzla, yeni veya türetilmiş bir yapılandırmayı paylaşmak için yapılandırmayı Genel depoya yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65a6c-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="65a6c-128">Yapılandırmanın tamamlanmış sürümünü ve ardından **Depoya yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="65a6c-129">**Genel (Microsoft)** seçeneğini ve ardından **Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![Depo seçeneklerine yükleme](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="65a6c-131">Onay iletisi kutusunda **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="65a6c-132">Sürümün açıklamasını gerektiği gibi güncelleştirin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="65a6c-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="65a6c-133">Yapılandırmanın durumu **Paylaş** olarak güncelleştirilir ve yapılandırma Genel depoya yüklenir.</span><span class="sxs-lookup"><span data-stu-id="65a6c-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="65a6c-134">Oradan, aşağıdaki yollarla çalışabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="65a6c-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="65a6c-135">Dynamics 365 örneğinize aktarın.</span><span class="sxs-lookup"><span data-stu-id="65a6c-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="65a6c-136">Daha fazla bilgi için bkz. [(ER) Yapılandırmaları RCS'den içe aktarma](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="65a6c-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="65a6c-137">Üçüncü tarafla veya harici bir kuruluşla paylaşmak için bkz. [RCS, Elektronik raporlama (ER) yapılandırmalarını harici kuruluşlarla paylaşma](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="65a6c-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)</span></span>

![Genel depodaki Türetilmiş Intrastat Contoso yapılandırma sürümü](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
