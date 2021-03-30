---
title: Veri tümleştirici projesi oluşturma (önizleme)
description: Bu konuda, veri tümleştirici projesinin nasıl oluşturulacağı açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 050c4f0fe1aea07c3866e2e9d7a6db6c758205ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208521"
---
# <a name="create-a-data-integrator-project-preview"></a><span data-ttu-id="bcc9f-103">Veri tümleştirici projesi oluşturma (önizleme)</span><span class="sxs-lookup"><span data-stu-id="bcc9f-103">Create a data integrator project (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="bcc9f-104">Bu konuda, veri tümleştirici projesinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-104">This topic explains how to create a data integrator project.</span></span>

1. <span data-ttu-id="bcc9f-105">Microsoft Dynamics 365 Finance'te oturum açın.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-105">Sign in to Microsoft Dynamics 365 Finance.</span></span>
2. <span data-ttu-id="bcc9f-106">**Çalışma alanları \> Veri yönetimi** bölümüne gidin ve **Veri varlıkları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-106">Go to **Workspaces \> Data management**, and select **Data entities**.</span></span> <span data-ttu-id="bcc9f-107">Bir sonraki adıma geçmeden önce tüm veri varlıkları yenilenene kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-107">Wait until all the data entities have been refreshed before you move on to the next step.</span></span>
3. <span data-ttu-id="bcc9f-108">[Power Apps portalını](https://make.powerapps.com/) açıp şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="bcc9f-108">Open the [Power Apps portal](https://make.powerapps.com/), and follow these steps:</span></span>

    1. <span data-ttu-id="bcc9f-109">Uygun ortamı seçin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-109">Select the appropriate environment.</span></span>
    2. <span data-ttu-id="bcc9f-110">Sol gezinti bölmesinde **Veri \> Bağlantılar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-110">In the left navigation pane, select **Data \> Connections**.</span></span>
    3. <span data-ttu-id="bcc9f-111">Aşağıdaki öğelerin uygun kurulumlarına bağlanın:</span><span class="sxs-lookup"><span data-stu-id="bcc9f-111">Connect to appropriate instances of the following items:</span></span>

        - <span data-ttu-id="bcc9f-112">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bcc9f-112">Dynamics 365</span></span>
        - <span data-ttu-id="bcc9f-113">Fin & Ops için Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bcc9f-113">Dynamics 365 for Fin & Ops</span></span>

4. <span data-ttu-id="bcc9f-114">[Power Apps ortamlarını](https://admin.powerapps.com/environments) açıp şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="bcc9f-114">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>

    1. <span data-ttu-id="bcc9f-115">**Veri tümleştiricisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-115">Select **Data Integrator**.</span></span>
    2. <span data-ttu-id="bcc9f-116">**Bağlantı kümeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-116">Select **Connection sets**.</span></span>
    3. <span data-ttu-id="bcc9f-117">**Yeni bağlantı kümesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-117">Select **New connection set**.</span></span>
    4. <span data-ttu-id="bcc9f-118">Bağlantı için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-118">Enter a name for the connection.</span></span>
    5. <span data-ttu-id="bcc9f-119">Aşağıdaki öğeler için uygun bağlantıları seçin:</span><span class="sxs-lookup"><span data-stu-id="bcc9f-119">Select the appropriate connections for the following items:</span></span>

        - <span data-ttu-id="bcc9f-120">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bcc9f-120">Dynamics 365</span></span>
        - <span data-ttu-id="bcc9f-121">Fin & Ops için Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="bcc9f-121">Dynamics 365 for Fin & Ops</span></span>

    6. <span data-ttu-id="bcc9f-122">Uygun kuruluş eşlemesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-122">Select the appropriate organization mapping.</span></span>
    7. <span data-ttu-id="bcc9f-123">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-123">Select **Create**.</span></span>

5. <span data-ttu-id="bcc9f-124">[Power Apps ortamlarını](https://admin.powerapps.com/environments) açıp şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="bcc9f-124">Open the [Power Apps environments](https://admin.powerapps.com/environments), and follow these steps:</span></span>  

    1. <span data-ttu-id="bcc9f-125">Yeni oluşturduğunuz bağlantı kümesini kullanarak aşağıdaki şablonlar için veri tümleştirme projeleri oluşturun:</span><span class="sxs-lookup"><span data-stu-id="bcc9f-125">Create data integration projects for the following templates by using the connection set that you just created:</span></span>

        - <span data-ttu-id="bcc9f-126">Müşteri ödeme içgörüleri sonuçları (CDS-Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="bcc9f-126">Customer payment insights results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="bcc9f-127">Nakit akışı zaman serisi sonuçları (CDS-Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="bcc9f-127">Cash flow time series results (CDS to Fin and Ops)</span></span>
        - <span data-ttu-id="bcc9f-128">Bütçe zaman serisi sonuçları (CDS-Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="bcc9f-128">Budget time series results (CDS to Fin and Ops)</span></span>

    2. <span data-ttu-id="bcc9f-129">Her proje için uygun zamanlamayı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-129">Set the appropriate scheduling for each project.</span></span>

> [!NOTE]
> <span data-ttu-id="bcc9f-130">CDS'te gerekli varlıkları göremiyorsanız **Alacak ve tahsilatlar > Kurulum > Mali İçgörüler > Mali içgörü parametreleri** bölümüne gidin, Müşteri ödeme tahminleri özelliğini etkinleştirin ve **Tahmin modeli oluştur** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-130">If you do not see the required entities in CDS, please go to **Credit and collections > Setup > Finance Insights > Finance insights parameters**, enable Customer payment predictions feature and click on **Create prediction model** button.</span></span> <span data-ttu-id="bcc9f-131">Yapay zeka modelinin dağıtımı tamamlandığında (başarılı veya başarısız), tümleştirmeyi oluşturmak için gerekli CDS varlıkları CDS'ye dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-131">When the deployment of AI model is completed (successful or failed), the CDS entities needed to create integration will be deployed in CDS.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="bcc9f-132">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="bcc9f-132">Privacy notice</span></span>

<span data-ttu-id="bcc9f-133">Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="bcc9f-133">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]