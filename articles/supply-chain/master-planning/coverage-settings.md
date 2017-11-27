---
title: "Kapsam ayarları"
description: "Master planlama, madde gereksinimlerini hesaplamak için karşılama ayarlarını kullanır."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bd85f89917659ac9c94590bace765b2123d6e556
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="coverage-settings"></a><span data-ttu-id="58cb5-103">Kapsam ayarları</span><span class="sxs-lookup"><span data-stu-id="58cb5-103">Coverage settings</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="58cb5-104">Master planlama, madde gereksinimlerini hesaplamak için karşılama ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="58cb5-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="58cb5-105">Karşılama ayarlarını birkaç şekilde belirtebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="58cb5-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="58cb5-106">Bir kapsam grubuna yönelik kapsam ayarlarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="58cb5-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="58cb5-107">Kapsam grubuyla bağlantılı tüm ürünlere yönelik ayarları içeren bir kapsam grubu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58cb5-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="58cb5-108">**Master planlama &gt; Kurulum &gt; Kapsam &gt; Kapsam grupları'na** tıklayarak karşılama grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="58cb5-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="58cb5-109">Ürüne bir kapsam grubu bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58cb5-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="58cb5-110">Bağlantı belirli bir siteye, ambara veya ürün boyutuna ise, **Madde kapsamı** sayfasındaki **Kapsam grubu** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="58cb5-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="58cb5-111">Bağlantı genel ise, ürün boyutlarından bağımsız olarak **Ürün ayrıntıları** sayfasındaki **Plan** FastTab'inde yer alan **Kapsam grubu**'un kullanın.</span><span class="sxs-lookup"><span data-stu-id="58cb5-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="58cb5-112">Bir kapsam grubunu bir ürüne bağlamazsanız, master planlama **Master planlama parametreleri** sayfasında varsayılan olarak belirtilen **Genel kapsam grubu**'nu kullanır.</span><span class="sxs-lookup"><span data-stu-id="58cb5-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="58cb5-113">Bir ürün için kapsam ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="58cb5-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="58cb5-114">Özel bir ürün için kapsam ayarları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58cb5-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="58cb5-115">**Ürün bilgileri yönetimi &gt; Ürünler &gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58cb5-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="58cb5-116">Ürünü seçin, **Eylem Bölmesi**'nde, **Plan** sekmesinde, **Kapsam grubu**'nda **Madde kapsamı**'na tıklayarak **Madde kapsamı** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="58cb5-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="58cb5-117">Ürün bir kapsam grubuna zaten bağlanmışsa, **Üstüne yazdır** alanını kullanarak kapsam grubu ayarlarının üstüne yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58cb5-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="58cb5-118">**Madde kapsamı** sayfasındaki kapsam ayarları, **Kapsam grubu** sayfasındaki ayarlardan önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="58cb5-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="58cb5-119">Sihirbaz kullanarak bir ürüne yönelik kapsam ayarlarını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="58cb5-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="58cb5-120">Sihirbaz, birincil madde karşılama parametrelerini ayarlamaya yönelik bir adım adım kılavuzdur.</span><span class="sxs-lookup"><span data-stu-id="58cb5-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="58cb5-121">**Madde kapsamı** sayfasında **Sihirbaz**'a tıklayarak **Madde Kapsamı Sihirbazı**'nı açın.</span><span class="sxs-lookup"><span data-stu-id="58cb5-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

-   <span data-ttu-id="58cb5-122">Boyut grubu için kapsam ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="58cb5-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="58cb5-123">**Ürün bilgileri yönetimi &gt; Ortak &gt; Serbest bırakılan ürünler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58cb5-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="58cb5-124">**Serbest bırakılan ürün ayrıntısı **sayfasında, **Genel** sekmesinde, **Yönetim** grubunda, **Depolama boyut grubu** bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="58cb5-124">On the **Released product detail **page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="58cb5-125">**Depolama boyut grubu** sayfasında **Boyuta göre kapsam planı** alanını seçerek depolama boyut grubundaki bir boyut için kapsam ayarları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58cb5-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="58cb5-126">Yapılandırma, renk, boyut, stil gibi tüm ürün boyutlarının **Boyuta göre kapsam planı** alanı seçilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="58cb5-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="see-also"></a><span data-ttu-id="58cb5-127">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="58cb5-127">See also</span></span>
--------

[<span data-ttu-id="58cb5-128">Master planlar</span><span class="sxs-lookup"><span data-stu-id="58cb5-128">Master plans</span></span>](master-plans.md)




