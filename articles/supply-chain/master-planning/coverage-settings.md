---
title: Kapsam ayarları
description: Master planlama, madde gereksinimlerini hesaplamak için karşılama ayarlarını kullanır.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50f47394a4d4e95b4e158ea42a630d9e6e91f05b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "322571"
---
# <a name="coverage-settings"></a><span data-ttu-id="ab449-103">Kapsam ayarları</span><span class="sxs-lookup"><span data-stu-id="ab449-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab449-104">Master planlama, madde gereksinimlerini hesaplamak için karşılama ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="ab449-104">Master scheduling uses coverage settings to calculate item requirements.</span></span> 

<span data-ttu-id="ab449-105">Karşılama ayarlarını birkaç şekilde belirtebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ab449-105">You can specify coverage settings in several ways:</span></span>

-   <span data-ttu-id="ab449-106">Bir kapsam grubuna yönelik kapsam ayarlarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ab449-106">Specify coverage settings for a coverage group.</span></span> <span data-ttu-id="ab449-107">Kapsam grubuyla bağlantılı tüm ürünlere yönelik ayarları içeren bir kapsam grubu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab449-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="ab449-108">**Master planlama &gt; Kurulum &gt; Kapsam &gt; Kapsam grupları'na** tıklayarak karşılama grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ab449-108">Click **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups** to create a coverage group.</span></span> <span data-ttu-id="ab449-109">Ürüne bir kapsam grubu bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab449-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="ab449-110">Bağlantı belirli bir siteye, ambara veya ürün boyutuna ise, **Madde kapsamı** sayfasındaki **Kapsam grubu** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="ab449-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="ab449-111">Bağlantı genel ise, ürün boyutlarından bağımsız olarak **Ürün ayrıntıları** sayfasındaki **Plan** FastTab'inde yer alan **Kapsam grubu**'un kullanın.</span><span class="sxs-lookup"><span data-stu-id="ab449-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** on the **Plan** FastTab on the **Product details** page.</span></span> <span data-ttu-id="ab449-112">Bir kapsam grubunu bir ürüne bağlamazsanız, master planlama **Master planlama parametreleri** sayfasında varsayılan olarak belirtilen **Genel kapsam grubu**'nu kullanır.</span><span class="sxs-lookup"><span data-stu-id="ab449-112">If you do not link a coverage group to a product, master planning uses the **General coverage group** that is specified on the **Master planning parameters** page as the default.</span></span>

-   <span data-ttu-id="ab449-113">Bir ürün için kapsam ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="ab449-113">Specify coverage settings for a product.</span></span> <span data-ttu-id="ab449-114">Özel bir ürün için kapsam ayarları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab449-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="ab449-115">**Ürün bilgileri yönetimi &gt; Ürünler &gt; Serbest bırakılan ürünler** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab449-115">Click **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="ab449-116">Ürünü seçin, **Eylem Bölmesi**'nde, **Plan** sekmesinde, **Kapsam grubu**'nda **Madde kapsamı**'na tıklayarak **Madde kapsamı** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="ab449-116">Select the product, on the **Action Pane**, on the **Plan** tab, in the **Coverage group**, click **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="ab449-117">Ürün bir kapsam grubuna zaten bağlanmışsa, **Üstüne yazdır** alanını kullanarak kapsam grubu ayarlarının üstüne yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab449-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="ab449-118">**Madde kapsamı** sayfasındaki kapsam ayarları, **Kapsam grubu** sayfasındaki ayarlardan önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="ab449-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

<!-- -->

-   <span data-ttu-id="ab449-119">Sihirbaz kullanarak bir ürüne yönelik kapsam ayarlarını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="ab449-119">Specify coverage settings for a product by using a wizard.</span></span> <span data-ttu-id="ab449-120">Sihirbaz, birincil madde karşılama parametrelerini ayarlamaya yönelik bir adım adım kılavuzdur.</span><span class="sxs-lookup"><span data-stu-id="ab449-120">The wizard is a step-by-step guide to help you set up the primary item coverage parameters.</span></span> <span data-ttu-id="ab449-121">**Madde kapsamı** sayfasında **Sihirbaz**'a tıklayarak **Madde Kapsamı Sihirbazı**'nı açın.</span><span class="sxs-lookup"><span data-stu-id="ab449-121">On the **Item coverage** page, click **Wizard** to open the **Item Coverage Wizard**.</span></span>

<!-- -->

- <span data-ttu-id="ab449-122">Boyut grubu için kapsam ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="ab449-122">Specify coverage settings for a dimension group.</span></span> <span data-ttu-id="ab449-123">**Ürün bilgileri yönetimi &gt; Ortak &gt; Serbest bırakılan ürünler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab449-123">Click **Product information management &gt; Common &gt; Released products**.</span></span> <span data-ttu-id="ab449-124">**Serbest bırakılan ürün ayrıntısı** sayfasında, **Genel** sekmesinde, **Yönetim** grubunda, **Depolama boyut grubu** bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ab449-124">On the **Released product detail** page, on the **General** tab, in the **Administration** group, click the **Storage dimension group** link.</span></span> <span data-ttu-id="ab449-125">**Depolama boyut grubu** sayfasında **Boyuta göre kapsam planı** alanını seçerek depolama boyut grubundaki bir boyut için kapsam ayarları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab449-125">On the **Storage dimension group** page, select the **Coverage plan by dimension** field to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="ab449-126">Yapılandırma, renk, boyut, stil gibi tüm ürün boyutlarının **Boyuta göre kapsam planı** alanı seçilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ab449-126">All product dimensions, such as configuration, color, size, style, must have the **Coverage plan by dimension** field selected.</span></span>



<a name="additional-resources"></a><span data-ttu-id="ab449-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ab449-127">Additional resources</span></span>
--------

[<span data-ttu-id="ab449-128">Master planlar</span><span class="sxs-lookup"><span data-stu-id="ab449-128">Master plans</span></span>](master-plans.md)



