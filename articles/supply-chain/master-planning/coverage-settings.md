---
title: Kapsam ayarları
description: Bu konu, Master planlamanın madde gereksinimlerini hesaplamak için kullandığı kapsam ayarlarıyla ilgili bilgi sağlar.
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
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538906"
---
# <a name="coverage-settings"></a><span data-ttu-id="271ea-103">Kapsam ayarları</span><span class="sxs-lookup"><span data-stu-id="271ea-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="271ea-104">Master planlama, madde gereksinimlerini hesaplamak için karşılama ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="271ea-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="271ea-105">Karşılama ayarlarını birkaç şekilde belirtebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="271ea-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="271ea-106">Bir kapsam grubuna yönelik kapsam ayarlarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="271ea-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="271ea-107">Kapsam grubuyla bağlantılı tüm ürünlere yönelik ayarları içeren bir kapsam grubu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="271ea-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="271ea-108">Bir kapsam grubu oluşturmak için **Master planlama &gt; Kurulum &gt; Kapsam &gt; Kapsam grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="271ea-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="271ea-109">Ürüne bir kapsam grubu bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="271ea-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="271ea-110">Bağlantı belirli bir siteye, ambara veya ürün boyutuna ise, **Madde kapsamı** sayfasındaki **Kapsam grubu** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="271ea-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="271ea-111">Bağlantı genel ise, ürün boyutlarından bağımsız olarak **Ürün ayrıntıları** sayfasındaki **Plan** hızlı sekmesinde yer alan **Kapsam grubu** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="271ea-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="271ea-112">Varsayılan olarak, bir kapsam grubunu bir ürüne bağlamazsanız, master planlama **Master planlama parametreleri** sayfasında belirtilen genel kapsam grubunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="271ea-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="271ea-113">Bir ürün için kapsam ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="271ea-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="271ea-114">Özel bir ürün için kapsam ayarları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="271ea-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="271ea-115">**Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="271ea-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="271ea-116">Ürünü seçin ardından Eylem Bölmesi'nde, **Plan** sekmesinde, **Kapsam** grubunda **Madde kapsamı**'nı seçerek **Madde kapsamı** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="271ea-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="271ea-117">Ürün bir kapsam grubuna zaten bağlanmışsa, **Üstüne yazdır** alanını kullanarak kapsam grubu ayarlarının üstüne yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="271ea-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="271ea-118">**Madde kapsamı** sayfasındaki kapsam ayarları, **Kapsam grubu** sayfasındaki ayarlardan önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="271ea-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="271ea-119">Sihirbaz kullanarak bir ürüne yönelik kapsam ayarlarını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="271ea-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="271ea-120">Sihirbaz, birincil madde kapsamı parametrelerini ayarlama sürecinde size adım adım yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="271ea-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="271ea-121">**Madde kapsamı** sayfasında, Eylem Bölmesinde **Sihirbaz**'ı seçerek **Madde Kapsamı Sihirbazı**'nı açın.</span><span class="sxs-lookup"><span data-stu-id="271ea-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="271ea-122">Boyut grubu için kapsam ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="271ea-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="271ea-123">**Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="271ea-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="271ea-124">**Serbest bırakılan ürün ayrıntıları** sayfasında, **Genel** hızlı sekmesinde, **Yönetim** bölümünde, **Depolama boyut grubu** alanındaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="271ea-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="271ea-125">**Depolama boyut grupları** sayfasında **Boyuta göre kapsam planı** onay kutusunu seçerek depolama boyut grubundaki bir boyut için kapsam ayarları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="271ea-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="271ea-126">Yapılandırma, renk, boyut, stil gibi tüm ürün boyutları için **Boyuta göre kapsam planı** alanı seçilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="271ea-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="271ea-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="271ea-127">Additional resources</span></span>

[<span data-ttu-id="271ea-128">Master planlar</span><span class="sxs-lookup"><span data-stu-id="271ea-128">Master plans</span></span>](master-plans.md)
