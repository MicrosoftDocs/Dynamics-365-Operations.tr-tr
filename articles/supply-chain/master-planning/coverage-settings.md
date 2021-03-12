---
title: Kapsam ayarları
description: Bu konu, Master planlamanın madde gereksinimlerini hesaplamak için kullandığı kapsam ayarlarıyla ilgili bilgi sağlar.
author: roxanadiaconu
manager: tfehr
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard, ReqItemTableSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0aaacf28701542d329afedd8206a12f7c11b7ac7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999993"
---
# <a name="coverage-settings"></a><span data-ttu-id="10026-103">Kapsam ayarları</span><span class="sxs-lookup"><span data-stu-id="10026-103">Coverage settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10026-104">Master planlama, madde gereksinimlerini hesaplamak için karşılama ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="10026-104">Master scheduling uses coverage settings to calculate item requirements.</span></span>

<span data-ttu-id="10026-105">Karşılama ayarlarını birkaç şekilde belirtebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="10026-105">You can specify coverage settings in several ways:</span></span>

- <span data-ttu-id="10026-106">Bir kapsam grubuna yönelik kapsam ayarlarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="10026-106">Specify coverage settings for a coverage group.</span></span>

    <span data-ttu-id="10026-107">Kapsam grubuyla bağlantılı tüm ürünlere yönelik ayarları içeren bir kapsam grubu oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10026-107">You can create a coverage group that contains settings for all products that are linked to the coverage group.</span></span> <span data-ttu-id="10026-108">Bir kapsam grubu oluşturmak için **Master planlama &gt; Kurulum &gt; Kapsam &gt; Kapsam grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="10026-108">To create a coverage group, go to **Master planning &gt; Setup &gt; Coverage &gt; Coverage groups**.</span></span> <span data-ttu-id="10026-109">Ürüne bir kapsam grubu bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10026-109">You can link a coverage group to a product.</span></span> <span data-ttu-id="10026-110">Bağlantı belirli bir siteye, ambara veya ürün boyutuna ise, **Madde kapsamı** sayfasındaki **Kapsam grubu** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="10026-110">If the link is specific to a site, warehouse, or product dimension, use the **Coverage group** field on the **Item coverage** page.</span></span> <span data-ttu-id="10026-111">Bağlantı genel ise, ürün boyutlarından bağımsız olarak **Ürün ayrıntıları** sayfasındaki **Plan** hızlı sekmesinde yer alan **Kapsam grubu** alanını kullanın.</span><span class="sxs-lookup"><span data-stu-id="10026-111">If the link is generic, regardless of the product dimensions, use the **Coverage group** field on the **Plan** FastTab of the **Product details** page.</span></span> <span data-ttu-id="10026-112">Varsayılan olarak, bir kapsam grubunu bir ürüne bağlamazsanız, master planlama **Master planlama parametreleri** sayfasında belirtilen genel kapsam grubunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="10026-112">By default, if you don't link a coverage group to a product, master planning uses the general coverage group that is specified on the **Master planning parameters** page.</span></span>

- <span data-ttu-id="10026-113">Bir ürün için kapsam ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="10026-113">Specify coverage settings for a product.</span></span>

    <span data-ttu-id="10026-114">Özel bir ürün için kapsam ayarları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10026-114">You can create coverage settings for a specific product.</span></span> <span data-ttu-id="10026-115">**Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="10026-115">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="10026-116">Ürünü seçin ardından Eylem Bölmesi'nde, **Plan** sekmesinde, **Kapsam** grubunda **Madde kapsamı**'nı seçerek **Madde kapsamı** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="10026-116">Select the product, and then, on the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage** to open the **Item coverage** page.</span></span> <span data-ttu-id="10026-117">Ürün bir kapsam grubuna zaten bağlanmışsa, **Üstüne yazdır** alanını kullanarak kapsam grubu ayarlarının üstüne yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10026-117">If the product is already linked to a coverage group, you can override the coverage group settings by using the **Override** field.</span></span> <span data-ttu-id="10026-118">**Madde kapsamı** sayfasındaki kapsam ayarları, **Kapsam grubu** sayfasındaki ayarlardan önceliklidir.</span><span class="sxs-lookup"><span data-stu-id="10026-118">The coverage settings on the **Item coverage** page take precedence over the settings on the **Coverage group** page.</span></span>

- <span data-ttu-id="10026-119">Sihirbaz kullanarak bir ürüne yönelik kapsam ayarlarını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="10026-119">Specify coverage settings for a product by using a wizard.</span></span>

    <span data-ttu-id="10026-120">Sihirbaz, birincil madde kapsamı parametrelerini ayarlama sürecinde size adım adım yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="10026-120">The wizard guides you step by step through the process of setting up the primary item coverage parameters.</span></span> <span data-ttu-id="10026-121">**Madde kapsamı** sayfasında, Eylem Bölmesinde **Sihirbaz**'ı seçerek **Madde Kapsamı Sihirbazı**'nı açın.</span><span class="sxs-lookup"><span data-stu-id="10026-121">On the **Item coverage** page, on the Action Pane, select **Wizard** to open the **Item Coverage Wizard**.</span></span>

- <span data-ttu-id="10026-122">Boyut grubu için kapsam ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="10026-122">Specify coverage settings for a dimension group.</span></span>

    <span data-ttu-id="10026-123">**Ürün bilgi yönetimi &gt; Ürünler &gt; Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="10026-123">Go to **Product information management &gt; Products &gt; Released products**.</span></span> <span data-ttu-id="10026-124">**Serbest bırakılan ürün ayrıntıları** sayfasında, **Genel** hızlı sekmesinde, **Yönetim** bölümünde, **Depolama boyut grubu** alanındaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="10026-124">On the **Released product details** page, on the **General** FastTab, in the **Administration** section, select the link in the **Storage dimension group** field.</span></span> <span data-ttu-id="10026-125">**Depolama boyut grupları** sayfasında **Boyuta göre kapsam planı** onay kutusunu seçerek depolama boyut grubundaki bir boyut için kapsam ayarları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="10026-125">On the **Storage dimension groups** page, select the **Coverage plan by dimension** check box to create the coverage settings for a dimension in the storage dimension group.</span></span> <span data-ttu-id="10026-126">Yapılandırma, renk, boyut, stil gibi tüm ürün boyutları için **Boyuta göre kapsam planı** alanı seçilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="10026-126">The **Coverage plan by dimension** field must be selected for all product dimensions, such as configuration, color, size, and style.</span></span>


## <a name="coverage-codes"></a><span data-ttu-id="10026-127">Karşılama kodları</span><span class="sxs-lookup"><span data-stu-id="10026-127">Coverage codes</span></span>

<span data-ttu-id="10026-128">Master planlama farklı stok yenileme yöntemleri kullanacak şekilde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="10026-128">Master planning can be configured to use different replenishment methods.</span></span> <span data-ttu-id="10026-129">Stok yenileme yöntemleri veya lot boyutlandırma yöntemleri, sistem tarafından satın alınan veya üretilen maddelerin toplu iş boyutunu belirlemek için kullanılan tekniklerdir.</span><span class="sxs-lookup"><span data-stu-id="10026-129">The replenishment methods or lot-sizing methods are the techniques used by the system to determine the batch size for purchased or produced items.</span></span> 

<span data-ttu-id="10026-130">Her stok yenileme yöntemine aşağıdaki karşılama kodlarından biri atanır:</span><span class="sxs-lookup"><span data-stu-id="10026-130">Each replenishment method is assigned one of the following coverage codes:</span></span>

- <span data-ttu-id="10026-131">**El ile** : Sistemin madde için satın alınan, transfer veya üretim emirlerini önermediği lot boyutlandırma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="10026-131">**Manual** - The lot-sizing method where the system does not suggest purchased, transfer, or production orders for the item.</span></span> <span data-ttu-id="10026-132">Maddenin planlayıcısı, maddenin stok yenileme işlemi için gerekli siparişlerin oluşturulmasından sorumlu olacaktır.</span><span class="sxs-lookup"><span data-stu-id="10026-132">The planner for the item will be in charge of creating the required orders for the replenishment of the item.</span></span>
- <span data-ttu-id="10026-133">**Gereksinim başına**: Sistemin madde için her gereksinim başına bir planlı satınalma, transfer veya üretim emri oluşturduğu lot boyutlandırma yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="10026-133">**Per requirement** - The lot-sizing method in which the system creates a planned purchase, transfer, or production order per requirement for the item.</span></span> <span data-ttu-id="10026-134">Bu genellikle, aralıklı talep bulunan pahalı maddeler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="10026-134">This is generally used for expensive items with intermittent demand.</span></span>  
- <span data-ttu-id="10026-135">**Dönem başına**: Madde için bir döneme ait tüm talepleri tek bir siparişte olacak şekilde birleştiren lot boyutlandırma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="10026-135">**Per period** - The lot-sizing method that combines all the demand for a period into one order for the item.</span></span> <span data-ttu-id="10026-136">Sipariş dönemin ilk günü için planlanacaktır ve miktarı ayarlanan dönem içindeki net gereksinimleri karşılayacaktır.</span><span class="sxs-lookup"><span data-stu-id="10026-136">The order will be planned for the first day of the period and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="10026-137">Dönem, maddeye yapılan ilk taleple başlar ve tanımlanan süreyi olduğu gibi kapsar.</span><span class="sxs-lookup"><span data-stu-id="10026-137">The period starts with the first demand of the item and covers the defined length in time.</span></span> <span data-ttu-id="10026-138">Sonraki dönem, maddenin sonraki gereksinimleri itibarıyla başlar.</span><span class="sxs-lookup"><span data-stu-id="10026-138">The next period will start with the next requirements of the item.</span></span>
- <span data-ttu-id="10026-139">**Minimum/Maksimum**: Tahmini eldeki değeri bir eşiğin altında olduğunda, belirli bir düzeye kadar stok stok yenilemesini içeren lot boyutlandırma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="10026-139">**Min/Max** - The lot-sizing method that contains the replenishment of inventory up to a certain level when the predicted on-hand is below a threshold.</span></span> <span data-ttu-id="10026-140">Stok yenileme miktarı maksimum düzey ve eldeki tahmini düzey arasındaki fark olur.</span><span class="sxs-lookup"><span data-stu-id="10026-140">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="10026-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="10026-141">Additional resources</span></span>

[<span data-ttu-id="10026-142">Master planlara genel bakış</span><span class="sxs-lookup"><span data-stu-id="10026-142">Master plans overview</span></span>](master-plans.md)
