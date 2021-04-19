---
title: B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama
description: Bu konu, işletmeler arası (B2B) e-ticaret siteleri için ürün miktarı sınırlarının nasıl ayarlanacağını açıklar.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e9f14bc9aa6586e87f3e8ccb82e63d0ec2e46534
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799793"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a><span data-ttu-id="c5909-103">B2B e-ticaret siteleri için ürün miktarı sınırlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="c5909-103">Set product quantity limits for B2B e-commerce sites</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5909-104">Bu konu, işletmeler arası (B2B) e-ticaret siteleri için ürün miktarı sınırlarının nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="c5909-104">This topic describes how to set product quantity limits for business-to-business (B2B) e-commerce sites.</span></span>

<span data-ttu-id="c5909-105">Çoğu ürünün, gruplandırmasını tanımlayan ölçü birimi vardır.</span><span class="sxs-lookup"><span data-stu-id="c5909-105">Most products have a unit of measure that defines their grouping.</span></span> <span data-ttu-id="c5909-106">Gruplandırma ürünlerin nasıl satılabilir olduğunu etkiler.</span><span class="sxs-lookup"><span data-stu-id="c5909-106">The grouping affects how the products can be sold.</span></span> <span data-ttu-id="c5909-107">Bazı ürünlerde miktar için ek bir gruplama olabilir.</span><span class="sxs-lookup"><span data-stu-id="c5909-107">Some products might have an additional grouping for quantities.</span></span> <span data-ttu-id="c5909-108">Bu gruplandırma, ürünlerin ayrı birimler veya katları olarak satılıp satılmayacağını ve izlenmesi gereken minimum veya maksimum sipariş miktarı sınırı olup olmadığını belirler.</span><span class="sxs-lookup"><span data-stu-id="c5909-108">This grouping determines whether the products can be sold as individual units or multiples, and whether there is a minimum or maximum order quantity limit that must be followed.</span></span>

<span data-ttu-id="c5909-109">Miktar sınırlaması özelliği, Microsoft Dynamics 365 Commerce'te (varsayılan sipariş ayarları veya Commerce site oluşturucu site ayarlarında) konfigüre edilen minimum, maksimum, çoklu ve standart miktarların bir e-ticaret sitesine yerleştirilen müşteri siparişleri için geçerli olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5909-109">The quantity limiting feature ensures that the minimum, maximum, multiple, and standard quantities that are configured in Microsoft Dynamics 365 Commerce (in the default order settings or the Commerce site builder site settings) are applied to customer orders that are placed on an e-commerce site.</span></span> <span data-ttu-id="c5909-110">Ürün miktarı sınırları şu anda satış noktası (POS) ve çağrı merkezleri için desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="c5909-110">Product quantity limits aren't currently supported for the point of sale (POS) and call centers.</span></span>

<span data-ttu-id="c5909-111">Pek çok perakendeci, çeşitli ürün ve yerine getirme gereksinimlerini karşılamak için müşteri siparişleri (özel siparişler olarak da adlandırılır) seçeneği veya özel siparişler sağlar.</span><span class="sxs-lookup"><span data-stu-id="c5909-111">Many retailers provide the option of customer orders (also known as special orders) to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="c5909-112">Burada bazı tipik senaryolar vardır:</span><span class="sxs-lookup"><span data-stu-id="c5909-112">Here are some typical scenarios:</span></span>

- <span data-ttu-id="c5909-113">Bir müşteri belirli çeşitlerin çarpımlarının katları olarak satılmasını istiyor.</span><span class="sxs-lookup"><span data-stu-id="c5909-113">A customer wants products of specific variants to be sold in multiples of a few.</span></span>
- <span data-ttu-id="c5909-114">Bir müşteri, ürünleri, müşterinin satın aldığı mağazadan başka bir konumda bulunan bir mağazadan teslim almak istiyor.</span><span class="sxs-lookup"><span data-stu-id="c5909-114">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span> <span data-ttu-id="c5909-115">Ancak, mağazaların ambalaj standartları çevrimiçi satış dağıtımı için ambalaj standartlarından farklıdır.</span><span class="sxs-lookup"><span data-stu-id="c5909-115">However, the packing standards for the stores differ from the packing standards for online sales distribution.</span></span>
- <span data-ttu-id="c5909-116">Müşteri, satın alınabilecek kalemler için maksimum miktar sınırı olan bir sınırlı sürümde ürün satın almak istiyor.</span><span class="sxs-lookup"><span data-stu-id="c5909-116">A customer wants to buy a limited-edition product that has a maximum quantity limit for items that can be purchased.</span></span>

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a><span data-ttu-id="c5909-117">Commerce Headquarters'da varsayılan sipariş ayarları özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="c5909-117">Turn on the default order settings feature in Commerce headquarters</span></span>

<span data-ttu-id="c5909-118">Ürün miktar sınırlarını ayarlamadan önce, Commerce Headquarters'da varsayılan sipariş ayarları özelliği açık olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c5909-118">Before you can set product quantity limits, the default order settings feature must be turned on in Commerce headquarters.</span></span>

<span data-ttu-id="c5909-119">Varsayılan sipariş ayarları özelliğini etkinleştirmek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c5909-119">To turn on the default order settings feature, follow these steps.</span></span>

1. <span data-ttu-id="c5909-120">**Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c5909-120">Go to **System administration \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="c5909-121">**Müşteri siparişinde Site ve Varsayılan sipariş ayarlarını destekle** özelliğini bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="c5909-121">Find and select the **Support the Site and Default order settings in the customer order** feature.</span></span>
1. <span data-ttu-id="c5909-122">Sağ bölmenin alt kısmında **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c5909-122">At the bottom of the right pane, select **Enable now**.</span></span> 

## <a name="define-quantity-settings"></a><span data-ttu-id="c5909-123">Miktar ayarlarını tanımlama</span><span class="sxs-lookup"><span data-stu-id="c5909-123">Define quantity settings</span></span> 

<span data-ttu-id="c5909-124">Miktar ayarlarını **Varsayılan sipariş ayarları** sayfasında tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c5909-124">You can define the quantity settings on the **Default order settings** page.</span></span>

<span data-ttu-id="c5909-125">Miktar ayarlarını tanımlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c5909-125">To define the quantity settings, follow these steps.</span></span> 

1. <span data-ttu-id="c5909-126">Ürün **Perakende ve Ticaret \> Ürünler ve kategoriler \> Kategoriye göre serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c5909-126">Go to Product **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="c5909-127">Sevk edilen ürünleri seçin.</span><span class="sxs-lookup"><span data-stu-id="c5909-127">Select a released product.</span></span>
1. <span data-ttu-id="c5909-128">Eylem Bölmesinde **Stoğu yönet** sekmesinde, **Sipariş ayarları** grubunda, **Varsayılan sipariş ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c5909-128">On the Action Pane, on the **Manage inventory** tab, in the **Order settings** group, select **Default order settings**.</span></span> 
1. <span data-ttu-id="c5909-129">**Varsayılan sipariş ayarları** sayfasında, **Satış siparişi** hızlı sekmesinde, **Satış miktarı** bölümünde ürün satış miktarlarını ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="c5909-129">On the **Default order settings** page, on the **Sales order** FastTab, in the **Sales quantity** section, set the product sales quantities:</span></span>

    - <span data-ttu-id="c5909-130">**Çoklu** – Ürünün katları olarak satın alınabileceği miktar.</span><span class="sxs-lookup"><span data-stu-id="c5909-130">**Multiple** – The quantity that the product can be bought in multiples of.</span></span>
    - <span data-ttu-id="c5909-131">**Minimum Sipariş Miktarı** - Satın alınması gereken minimum ürün sayısı.</span><span class="sxs-lookup"><span data-stu-id="c5909-131">**Minimum Order Quantity** – The minimum number of products that must be purchased.</span></span>
    - <span data-ttu-id="c5909-132">**Maksimum Sipariş Miktarı** - Satın alınabilecek maksimum ürün sayısı.</span><span class="sxs-lookup"><span data-stu-id="c5909-132">**Maximum Order Quantity** – The maximum number of products that can be purchased.</span></span>
    - <span data-ttu-id="c5909-133">**Standart Sipariş Miktarı** – Ürün seçildiğinde otomatik olarak girilen varsayılan miktar.</span><span class="sxs-lookup"><span data-stu-id="c5909-133">**Standard Order Quantity** – The default quantity that is automatically entered when the product is selected.</span></span>

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a><span data-ttu-id="c5909-134">Commerce site oluşturucuda B2B sipariş miktarı sınırları özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="c5909-134">Turn on the B2B order quantity limits feature in Commerce site builder</span></span>

<span data-ttu-id="c5909-135">Commerce site oluşturucuda B2B sipariş miktarı sınırları özelliğini açmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c5909-135">To turn on the B2B order quantity limits feature in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c5909-136">**Site ayarları \> Uzantılar**'a gidin</span><span class="sxs-lookup"><span data-stu-id="c5909-136">Go to **Site settings \> Extensions**</span></span>
1. <span data-ttu-id="c5909-137">**Sipariş Miktarı Sınırlarını Etkinleştir** altında, açılır menüden **B2B müşterileri için etkin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c5909-137">Under **Enable Order Quantity Limits**, select **Enabled for B2B customers** in the drop-down menu.</span></span> 

> [!NOTE] 
> <span data-ttu-id="c5909-138">Güncelleştirilen site oluşturucu ayarları yalnızca app.settings.json dosyası güncelleştirildikten sonra etkinleşir.</span><span class="sxs-lookup"><span data-stu-id="c5909-138">Updated site builder settings take effect only after the app.settings.json file has been updated.</span></span> <span data-ttu-id="c5909-139">Daha fazla bilgi için bkz. [SDK ve Modül kitaplığı güncelleştirmeleri](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="c5909-139">For more information, see [SDK and Module library updates](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5909-140">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c5909-140">Additional resources</span></span>

[<span data-ttu-id="c5909-141">B2B e-ticaret sitesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="c5909-141">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="c5909-142">B2B kuruluşlar için kuruluş modelleme hiyerarşileri oluşturma</span><span class="sxs-lookup"><span data-stu-id="c5909-142">Create org modeling hierarchies for B2B organizations</span></span>](org-model.md)

[<span data-ttu-id="c5909-143">B2B e-ticaret sitelerindeki iş ortağı kullanıcılarını yönetme</span><span class="sxs-lookup"><span data-stu-id="c5909-143">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="c5909-144">B2B e-ticaret siteleri için müşteri hesabı ödeme yöntemini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c5909-144">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]