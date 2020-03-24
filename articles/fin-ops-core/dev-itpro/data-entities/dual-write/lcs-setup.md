---
title: Lifecycle Services'tan çift yazma kurulumu
description: Bu konu, yeni bir Finance and Operations ortamı ile yeni bir Common Data Service ortamı arasında Microsoft Dynamics Lifecycle Services'tan (LCS) nasıl çift yazma bağlantısı kurulabileceğini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 75765c0cc03c64030fac6bc656f57a143828b85b
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112536"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="6d14c-103">Lifecycle Services'tan çift yazma kurulumu</span><span class="sxs-lookup"><span data-stu-id="6d14c-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6d14c-104">Bu konu, yeni bir Finance and Operations ortamı ile yeni bir Common Data Service ortamı arasında Microsoft Dynamics Lifecycle Services'tan (LCS) nasıl çift yazma bağlantısı kurulabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="6d14c-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6d14c-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="6d14c-105">Prerequisites</span></span>

<span data-ttu-id="6d14c-106">Çift yazma bağlantısı kurmak için yönetici olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d14c-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="6d14c-107">Kiracıya erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6d14c-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="6d14c-108">Hem Finance and Operations ortamları hem de Common Data Service ortamlarında yönetici olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d14c-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="6d14c-109">Çift yazma bağlantısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="6d14c-109">Set up a dual-write connection</span></span>

<span data-ttu-id="6d14c-110">Çift yazma bağlantısı ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="6d14c-111">LCS'de projenize gidin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="6d14c-112">Yeni bir ortam dağıtmak için **Yapılandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="6d14c-113">Sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-113">Select the version.</span></span> 
4. <span data-ttu-id="6d14c-114">Topolojiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-114">Select the topology.</span></span> <span data-ttu-id="6d14c-115">Kullanılabilir yalnızca bir topoloji varsa, otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="6d14c-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="6d14c-116">**Dağıtım ayarları** sihirbazında ilk adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="6d14c-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="6d14c-117">**Common Data Service** sekmesinde, aşağıdaki adımlardan birini uygulayın:</span><span class="sxs-lookup"><span data-stu-id="6d14c-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="6d14c-118">Common Data Service ortamı kiracınız için zaten sağlanmışsa, onu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d14c-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="6d14c-119">**Common Data Service'ı yapılandır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6d14c-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="6d14c-120">**Kullanılabilir ortamlar** alanında, Finance and Operations verileriyle tümleştirilecek ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="6d14c-121">Liste, yönetici ayrıcalıklarına sahip olduğunuz tüm ortamları içerir.</span><span class="sxs-lookup"><span data-stu-id="6d14c-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="6d14c-122">Hüküm ve koşulları kabul etmiş olduğunuzu belirtmek için **Kabul et** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Common Data Service ortamı kiracınız için zaten sağlandığında Common Data Service sekmesi](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="6d14c-124">Kiracınızda Common Data Service ortamı yoksa, yeni bir ortam sağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="6d14c-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="6d14c-125">**Common Data Service'ı yapılandır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6d14c-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="6d14c-126">Common Data Service ortamı için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="6d14c-127">Ortamın dağıtılacağı bölgeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="6d14c-128">Ortam için varsayılan dili ve para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="6d14c-129">Dil ve para birimini daha sonra değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d14c-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="6d14c-130">Hüküm ve koşulları kabul etmiş olduğunuzu belirtmek için **Kabul et** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Kiracınızda Common Data Service ortamı olmadığında Common Data Service sekmesi](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="6d14c-132">**Dağıtım ayarları** sihirbazında kalan adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="6d14c-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="6d14c-133">Ortamın durumu **Dağıtıldı** olduktan sonra, ortam ayrıntıları sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="6d14c-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="6d14c-134">**Common Data Service ortam bilgileri** bölümü, Finance and Operations ortamı adını ve bağlanan Common Data Service ortamı adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d14c-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![Common Data Service ortam bilgileri bölümü](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="6d14c-136">Finance and Operations ortam yöneticisinin LCS'de oturum açması ve bağlantıyı tamamlamak için **Uygulamalar için CDS'ye Bağla**'yı seçmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d14c-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="6d14c-137">Ortam ayrıntıları sayfası yöneticinin ilgili kişi bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d14c-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="6d14c-138">Bağlantı tamamlandıktan sonra, durum **Ortam bağlantısı başarıyla tamamlandı** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6d14c-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="6d14c-139">Finance and Operations ortamındaki **Veri tümleştirme** çalışma alanını açmak ve kullanılabilir şablonları kontrol etmek için **Uygulamalar için CDS'ye Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Common Data Service ortam bilgileri bölümündeki Uygulamalar için CDS'ye Bağla düğmesi](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="6d14c-141">Ortamların bağlantısını LCS kullanarak kaldıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="6d14c-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="6d14c-142">Bir ortamın bağlantısını kaldırmak için Finance and Operations ortamdaki **Veri tümleştirme** çalışma alanını açın ve sonra **Bağlantıyı kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="6d14c-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
