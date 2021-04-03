---
title: Üretim katı yürütme arabirimini tasarlama
description: Bu konuda her yapılandırma için kullanıcı arabirimi içeriğinin nasıl tasarlanacağı açıklanmaktadır.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration, JmgProductionFloorExecutionConfigurationTab
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 282785799b6d61a00a356fcc2ae86ff0e3b7b39f
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501042"
---
# <a name="design-the-production-floor-execution-interface"></a><span data-ttu-id="bec95-103">Üretim katı yürütme arabirimini tasarlama</span><span class="sxs-lookup"><span data-stu-id="bec95-103">Design the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="bec95-104">Üretim katı yürütme arabirimi tarafından kullanılan her yapılandırma için kullanıcı arabirimi içeriği tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bec95-104">You can design the content of the user interface for each configuration used by the production floor execution interface.</span></span> <span data-ttu-id="bec95-105">Örneğin, bir çalışma hücresindeki çalışanların üretim katındaki iş talimatlarını başka bir çalışma hücresinde açabilmesi gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="bec95-105">For example, workers in one work cell might need to be able to open job instructions on the production floor, while in another work cell, instructions are not needed.</span></span> <span data-ttu-id="bec95-106">Bu durumda, biri belge eklerini açmak için kullanılan bir düğmeye ve diğeri bu düğmeye sahip olmayan iki yapılandırma oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bec95-106">In that case, two configurations should be created, one with a button for opening document attachments and one without this button.</span></span>

## <a name="design-a-tab"></a><span data-ttu-id="bec95-107">Sekme tasarlama</span><span class="sxs-lookup"><span data-stu-id="bec95-107">Design a tab</span></span>

<span data-ttu-id="bec95-108">**Üretim katı yürütmesini yapılandırma** sayfasında, Eylem bölmesinde **Sekme tasarla**'yı seçerek sekme oluşturabilir ve yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bec95-108">On the **Configure production floor execution** page, you can create and configure tabs by selecting **Design tabs** on the Action Pane.</span></span>

<span data-ttu-id="bec95-109">Aşağıdaki çizimde gösterildiği gibi her sekme dört bölüme ayrılmıştır.</span><span class="sxs-lookup"><span data-stu-id="bec95-109">Each tab is divided into four sections, as shown in the following illustration.</span></span>

<span data-ttu-id="bec95-110">![Sekme düzeni](media/pfe-tab-layout.png "Sekme düzeni")</span><span class="sxs-lookup"><span data-stu-id="bec95-110">![Tab layout](media/pfe-tab-layout.png "Tab layout")</span></span>

<span data-ttu-id="bec95-111">Çizimde aşağıdaki öğeler gösterilir:</span><span class="sxs-lookup"><span data-stu-id="bec95-111">The following elements are shown in the illustration:</span></span>

1. <span data-ttu-id="bec95-112">Birincil araç çubuğu</span><span class="sxs-lookup"><span data-stu-id="bec95-112">Primary toolbar</span></span>
1. <span data-ttu-id="bec95-113">İkincil araç çubuğu</span><span class="sxs-lookup"><span data-stu-id="bec95-113">Secondary toolbar</span></span>
1. <span data-ttu-id="bec95-114">Ana görünüm</span><span class="sxs-lookup"><span data-stu-id="bec95-114">Main view</span></span>
1. <span data-ttu-id="bec95-115">Ayrıntılı görünüm</span><span class="sxs-lookup"><span data-stu-id="bec95-115">Detailed view</span></span>

<span data-ttu-id="bec95-116">Yeni bir sekme oluşturmak ve yapılandırmak için bu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="bec95-116">To create and configure a new tab, follow these steps:</span></span>

1. <span data-ttu-id="bec95-117">**Üretim denetimi \> Ayarlar \> Üretim yürütme \> Üretim katı yürütmesini konfigüre et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="bec95-117">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

1. <span data-ttu-id="bec95-118">**Sekme tasarla** sayfasını açmak için, eylem bölmesinde **Sekme tasarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bec95-118">Select **Design tabs** on the Action Pane to open the **Design tabs** page.</span></span>

    <span data-ttu-id="bec95-119">![Sekme tasarla sayfası](media/pfe-design-tabs.png "Sekme tasarla sayfası")</span><span class="sxs-lookup"><span data-stu-id="bec95-119">![The Design tabs page](media/pfe-design-tabs.png "The Design tabs page")</span></span>

1. <span data-ttu-id="bec95-120">Eylem Bölmesi'nde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bec95-120">Select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="bec95-121">Sayfanın üst bilgisinde aşağıdaki ayarları yapın:</span><span class="sxs-lookup"><span data-stu-id="bec95-121">Make the following settings in the header of the page:</span></span>

    - <span data-ttu-id="bec95-122">**Sekme adı**: Sekme için bir ad belirtin.</span><span class="sxs-lookup"><span data-stu-id="bec95-122">**Tab name** - Specify a name for the tab.</span></span>
    - <span data-ttu-id="bec95-123">**Ana görünüm**: Önceden tanımlanmış iş listeleri (*Etkin işler*, *Tüm işler* veya *Makinem*) arasında seçim yapın.</span><span class="sxs-lookup"><span data-stu-id="bec95-123">**Main view** - Select between the two pre-defined job lists (*Active jobs*, *All jobs*, or *My machine*).</span></span>
    - <span data-ttu-id="bec95-124">**Ayrıntılar görünümü**: Boş bir değer veya **İş ayrıntıları** arasında seçim yapın.</span><span class="sxs-lookup"><span data-stu-id="bec95-124">**Details view** - Select between a blank value or **Job details**.</span></span> <span data-ttu-id="bec95-125">Boş değeri seçerseniz, sekmede ayrıntılı görünüm olmaz. **İş detayları**'nı seçerseniz, ayrıntılı görünümde ana görünümdeki iş listesinde seçilen işin ayrıntılı açıklaması yer alır.</span><span class="sxs-lookup"><span data-stu-id="bec95-125">If you select the blank value, there will be no detailed view in the tab. If you select **Job details**, the detailed view will contain a detailed description of the job selected in the job list in the main view.</span></span>

1. <span data-ttu-id="bec95-126">**Birincil araç çubuğu** bölümünde, birincil araç çubuğunda hangi düğmelerin kullanılabilir olmasını istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="bec95-126">In the **Primary toolbar** section, choose which buttons should be available in the primary toolbar.</span></span> <span data-ttu-id="bec95-127">**Kullanılabilir eylemler** sütunu, eklenebilecek tüm düğmelerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bec95-127">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="bec95-128">**Seçilen eylemler** sütunları, geçerli yapılandırmaya dahil edilen tüm düğmelerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bec95-128">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="bec95-129">Sütunlar arasında seçili öğeleri gerektiği gibi taşımak için sütunlar arasındaki düğmeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="bec95-129">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="bec95-130">Düğmelerin kullanıcı arabiriminde sunulduğu sırayı denetlemek için **Seçili eylemler** sütununun yanındaki yukarı ve aşağı düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bec95-130">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

1. <span data-ttu-id="bec95-131">**İkincil** **araç çubuğu** bölümünde, ikincil araç çubuğunda hangi düğmelerin kullanılabilir olmasını istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="bec95-131">In the **Secondary** **toolbar** section, choose which buttons should be available in the secondary toolbar.</span></span> <span data-ttu-id="bec95-132">**Kullanılabilir eylemler** sütunu, eklenebilecek tüm düğmelerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bec95-132">The **Available actions** column shows a list of all the buttons that can be added.</span></span> <span data-ttu-id="bec95-133">**Seçilen eylemler** sütunları, geçerli yapılandırmaya dahil edilen tüm düğmelerin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bec95-133">The **Selected actions** columns shows a list of all the buttons that are included in the current configuration.</span></span> <span data-ttu-id="bec95-134">Sütunlar arasında seçili öğeleri gerektiği gibi taşımak için sütunlar arasındaki düğmeleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="bec95-134">Use the buttons between the columns to move selected items between the columns as needed.</span></span> <span data-ttu-id="bec95-135">Düğmelerin kullanıcı arabiriminde sunulduğu sırayı denetlemek için **Seçili eylemler** sütununun yanındaki yukarı ve aşağı düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bec95-135">Use the up and down buttons next to the **Selected actions** column to control the order in which the buttons are presented in the user interface.</span></span>

## <a name="associate-a-tab-with-a-configuration"></a><span data-ttu-id="bec95-136">Sekmeyi yapılandırma ile ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="bec95-136">Associate a tab with a configuration</span></span>

<span data-ttu-id="bec95-137">Gereksinim duyduğunuz tüm sekmeleri tasarladıktan sonra, bunları bir yapılandırma ile ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bec95-137">After you designed all the tabs you need, you can associate them with a configuration.</span></span>

1. <span data-ttu-id="bec95-138">**Üretim denetimi \> Ayarlar \> Üretim yürütme \> Üretim katı yürütmesini konfigüre et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="bec95-138">Go to **Production control \> Setup \> Manufacturing execution \> Configure production floor execution**.</span></span>

    <span data-ttu-id="bec95-139">![Üretim katı yürütmeyi yapılandır](media/pfe-config-prod-floor-execution.png "Üretim katı yürütmeyi yapılandır")</span><span class="sxs-lookup"><span data-stu-id="bec95-139">![Configure production floor execution](media/pfe-config-prod-floor-execution.png "Configure production floor execution")</span></span>

1. <span data-ttu-id="bec95-140">**Sekme seçimi** hızlı sekmesinde **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bec95-140">On the **Tab selection** FastTab, select **Add**.</span></span>

1. <span data-ttu-id="bec95-141">Kılavuza yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="bec95-141">A new row is added to the grid.</span></span> <span data-ttu-id="bec95-142">Bu yeni satır için yapılandırmaya eklemek istediğiniz sekmenin adını seçin.</span><span class="sxs-lookup"><span data-stu-id="bec95-142">For this new row, select the name of a tab that you want to add to the configuration.</span></span>

1. <span data-ttu-id="bec95-143">Gerektikçe ek sekmeler eklemeye devam edin.</span><span class="sxs-lookup"><span data-stu-id="bec95-143">Continue to add additional tabs as needed.</span></span>

1. <span data-ttu-id="bec95-144">Sekmeleri gerektiği gibi düzenlemek için araç çubuğundaki **Yukarı taşı** ve **Aşağı taşı** düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bec95-144">Use the **Move up** and **Move down** buttons on the toolbar to arrange the tabs as needed.</span></span> <span data-ttu-id="bec95-145">Sekmeler, yukarıdaki ekran görüntüsünde gösterilen sırada soldan sağa doğru görüntülenecektir (üstteki sekme solda gösterilir).</span><span class="sxs-lookup"><span data-stu-id="bec95-145">The tabs will be displayed from left to right in the order shown in the above screenshot (the tab at the top is shown on the left).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]