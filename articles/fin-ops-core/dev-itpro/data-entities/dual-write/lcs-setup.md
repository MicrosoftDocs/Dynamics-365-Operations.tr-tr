---
title: Lifecycle Services'dan çift yazma kurulumu
description: Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: df67e498b963af3ded7464f46f37bb4b2ca7d852
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127605"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="ed028-103">Lifecycle Services'dan çift yazma kurulumu</span><span class="sxs-lookup"><span data-stu-id="ed028-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ed028-104">Bu konu, yeni bir Finance and Operations ortamı ile yeni bir Dataverse ortamı arasında Microsoft Dynamics Lifecycle Services'tan (LCS) nasıl çift yazma bağlantısı kurulabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ed028-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ed028-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="ed028-105">Prerequisites</span></span>

<span data-ttu-id="ed028-106">Çift yazma bağlantısı kurmak için yönetici olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ed028-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="ed028-107">Kiracıya erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ed028-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="ed028-108">Hem Finance and Operations ortamları hem de Dataverse ortamlarında yönetici olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ed028-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="ed028-109">Çift yazma bağlantısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="ed028-109">Set up a dual-write connection</span></span>

<span data-ttu-id="ed028-110">Çift yazma bağlantısı ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ed028-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="ed028-111">LCS'de projenize gidin.</span><span class="sxs-lookup"><span data-stu-id="ed028-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="ed028-112">Yeni bir ortam dağıtmak için **Yapılandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="ed028-113">Sürümü seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-113">Select the version.</span></span> 
4. <span data-ttu-id="ed028-114">Topolojiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-114">Select the topology.</span></span> <span data-ttu-id="ed028-115">Kullanılabilir yalnızca bir topoloji varsa, otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="ed028-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="ed028-116">**Dağıtım ayarları** sihirbazında ilk adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="ed028-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="ed028-117">**Dataverse** sekmesinde, aşağıdaki adımlardan birini uygulayın:</span><span class="sxs-lookup"><span data-stu-id="ed028-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="ed028-118">Dataverse ortamı kiracınız için zaten sağlanmışsa, onu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed028-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="ed028-119">**Dataverse'ı yapılandır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ed028-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="ed028-120">**Kullanılabilir ortamlar** sütununda, Finance and Operations verileriyle tümleştirilecek ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="ed028-121">Liste, yönetici ayrıcalıklarına sahip olduğunuz tüm ortamları içerir.</span><span class="sxs-lookup"><span data-stu-id="ed028-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="ed028-122">Hüküm ve koşulları kabul etmiş olduğunuzu belirtmek için **Kabul et** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse ortamı kiracınız için zaten sağlandığında Dataverse sekmesi](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="ed028-124">Kiracınızda Dataverse ortamı yoksa, yeni bir ortam sağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="ed028-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="ed028-125">**Dataverse'ı yapılandır** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ed028-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="ed028-126">Dataverse ortamı için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="ed028-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="ed028-127">Ortamın dağıtılacağı bölgeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="ed028-128">Ortam için varsayılan dili ve para birimini seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="ed028-129">Dil ve para birimini daha sonra değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed028-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="ed028-130">Hüküm ve koşulları kabul etmiş olduğunuzu belirtmek için **Kabul et** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Kiracınızda Dataverse ortamı olmadığında Dataverse sekmesi](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="ed028-132">**Dağıtım ayarları** sihirbazında kalan adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="ed028-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="ed028-133">Ortamın durumu **Dağıtıldı** olduktan sonra, ortam ayrıntıları sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="ed028-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="ed028-134">**Power Platform Tümleştirmesi** bölümü, Finance and Operations ortamı adını ve bağlanan Dataverse ortamı adını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed028-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Power Platform Tümleştirmesi bölümü](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="ed028-136">Finance and Operations ortam yöneticisinin LCS'de oturum açması ve bağlantıyı tamamlamak için **Uygulamalar için CDS'ye Bağla**'yı seçmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ed028-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="ed028-137">Ortam ayrıntıları sayfası yöneticinin ilgili kişi bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed028-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="ed028-138">Bağlantı tamamlandıktan sonra, durum **Ortam bağlantısı başarıyla tamamlandı** olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ed028-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="ed028-139">Finance and Operations ortamındaki **Veri tümleştirme** çalışma alanını açmak ve kullanılabilir şablonları kontrol etmek için **Uygulamalar için CDS'ye Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Power Platform Tümleştirmesi bölümündeki Uygulamalar için CDS'ye Bağla düğmesi](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="ed028-141">Ortamların bağlantısını LCS kullanarak kaldıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="ed028-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="ed028-142">Bir ortamın bağlantısını kaldırmak için Finance and Operations ortamdaki **Veri tümleştirme** çalışma alanını açın ve sonra **Bağlantıyı kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ed028-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

