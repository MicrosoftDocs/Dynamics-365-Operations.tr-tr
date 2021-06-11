---
title: Lifecycle Services'dan çift yazma kurulumu
description: Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103581"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="52ef2-103">Lifecycle Services'dan çift yazma kurulumu</span><span class="sxs-lookup"><span data-stu-id="52ef2-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="52ef2-104">Bu konuda, Microsoft Dynamics Lifecycle Services (LCS) portalından nasıl çift yazma bağlantısı ayarlayacağınız açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="52ef2-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="52ef2-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="52ef2-105">Prerequisites</span></span>

<span data-ttu-id="52ef2-106">Power Platform tümleştirmeyi aşağıdaki konularda açıklandığı gibi tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="52ef2-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="52ef2-107">Power Platform Tümleştirme - Ortam dağıtımı sırasında etkinleştir</span><span class="sxs-lookup"><span data-stu-id="52ef2-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="52ef2-108">Power Platform Tümleştirme - Ortam dağıtımı sonrasında ayarlama</span><span class="sxs-lookup"><span data-stu-id="52ef2-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="52ef2-109">Yeni Dataverse ortamları için çift yazmayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="52ef2-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="52ef2-110">LCS **Ortam Ayrıntıları** sayfasından çift yazma ayarlamak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="52ef2-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="52ef2-111">**Ortam Ayrıntıları** sayfasında **Power Platform Tümleştirme** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="52ef2-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="52ef2-112">**Çift yazma uygulaması** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="52ef2-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform Tümleştirmesi](media/powerplat_integration_step2.png)

3. <span data-ttu-id="52ef2-114">Hüküm ve koşulları inceleyin ve ardından **Yapılandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52ef2-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="52ef2-115">Devam etmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52ef2-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="52ef2-116">Ortam ayrıntıları sayfasını düzenli aralıklarla yenileyerek ilerleme durumunu izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52ef2-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="52ef2-117">Kurulum genellikle 30 dakika veya daha az sürer.</span><span class="sxs-lookup"><span data-stu-id="52ef2-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="52ef2-118">Kurulum tamamlandığında, işlemin başarılı olup olmadığını veya bir hata olup olmadığını bildiren bir ileti bildirir.</span><span class="sxs-lookup"><span data-stu-id="52ef2-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="52ef2-119">Kurulum başarısız olursa, ilgili bir hata iletisi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="52ef2-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="52ef2-120">Sonraki adıma geçmeden önce hataları düzeltmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="52ef2-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="52ef2-121">Geçerli ortamın veritabanları ile Dataverse arasında bağlantı oluşturmak için **Power Platform Ortama bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="52ef2-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="52ef2-122">Bu genellikle 5 dakikadan daha az sürer.</span><span class="sxs-lookup"><span data-stu-id="52ef2-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Power Platform ortamı bağlantısı":::

8. <span data-ttu-id="52ef2-124">Bağlama tamamlandığında, bir köprü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="52ef2-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="52ef2-125">Finance and Operations ortamdaki çift yazma yönetim alanına giriş yapmak için bağlantıyı kullanın.</span><span class="sxs-lookup"><span data-stu-id="52ef2-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="52ef2-126">Buradan varlık eşlemeleri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="52ef2-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="52ef2-127">Mevcut Dataverse ortamı için çift yazmayı ayarlama</span><span class="sxs-lookup"><span data-stu-id="52ef2-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="52ef2-128">Varolan bir Dataverse ortam için çift yazma ayarlamak için bir Microsoft [destek bileti](../../lifecycle-services/lcs-support.md) oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="52ef2-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="52ef2-129">Bilet şunları içermelidir:</span><span class="sxs-lookup"><span data-stu-id="52ef2-129">The ticket must include:</span></span>

+ <span data-ttu-id="52ef2-130">Finance and Operations ortam kimliğiniz.</span><span class="sxs-lookup"><span data-stu-id="52ef2-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="52ef2-131">Lifecycle Services'den ortam adınız.</span><span class="sxs-lookup"><span data-stu-id="52ef2-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="52ef2-132">Power Platform Yönetim Merkezi'ndeki Dataverse kuruluş kimliği veya Power Platform Ortam Kimliği.</span><span class="sxs-lookup"><span data-stu-id="52ef2-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="52ef2-133">Biletinizde, kimliğin Power Platform tümleştirme için kullanılan örnek olmasını isteyin.</span><span class="sxs-lookup"><span data-stu-id="52ef2-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="52ef2-134">Ortamların bağlantısını LCS kullanarak kaldıramazsınız.</span><span class="sxs-lookup"><span data-stu-id="52ef2-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="52ef2-135">Bir ortamın bağlantısını kaldırmak için Finance and Operations ortamdaki **Veri tümleştirme** çalışma alanını açın ve sonra **Bağlantıyı kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="52ef2-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
