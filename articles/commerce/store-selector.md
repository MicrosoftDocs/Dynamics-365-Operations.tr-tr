---
title: Mağaza seçicisi modülü
description: Bu konu mağaza seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378220"
---
# <a name="store-selector-module"></a><span data-ttu-id="8ceb2-103">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="8ceb2-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8ceb2-104">Bu konu mağaza seçici modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8ceb2-105">Özet</span><span class="sxs-lookup"><span data-stu-id="8ceb2-105">Overview</span></span>

<span data-ttu-id="8ceb2-106">"Çevrimiçi satın al, mağazadan al" "(BOPIS) müşteri senaryosu için bir depolama Seçicisi modülü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="8ceb2-107">Bir ürünün malzeme çekme için uygun olduğu mağazaların listesini ve her mağazanın depolama saatlerini ve ürün envanterini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="8ceb2-108">Mağaza Seçicisi modülü, mağazaları bulmak için bir ürün bağlamı ve bir arama konumu gerektirir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="8ceb2-109">Arama konumu olmadığında, müşteri izin vermek koşuluyla müşterinin tarayıcı yerleşimi varsayılan olur.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="8ceb2-110">Modül, müşterinin yakındaki mağazaları bulmak için bir konum (posta kodu veya şehir ve il) girmesine olanak sağlayan bir giriş kutusu içerir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="8ceb2-111">Mağaza seçici modülü Bing Haritalar Coğrafi kodlama uygulama programlama arayüzü (API) ile tümleştirilmiştir ve bu sayede konumu bir enlem ve boylama dönüştürür.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="8ceb2-112">Bir Bing Haritalar API anahtarı gereklidir ve Dynamics 365 Commerce içinde Commerce paylaşılan parametreler sayfasına eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8ceb2-113">Ürün Ayrıntıları sayfasındaki (PDP) bir ürünün malzeme çekme için uygun olduğu mağazaları görüntülemek için, bir satın alma kutusu modülüne Mağaza Seçici modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="8ceb2-114">Bir sepet modülüne da eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-114">It can also be added to a cart module.</span></span> <span data-ttu-id="8ceb2-115">Bir sepet modülüne eklendiğinde, mağaza seçici modülü her bir sepet çizgisi öğesi için toplama seçeneklerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="8ceb2-116">Ek olarak, özel kodlamaya sahip bu modül Uzantılar ve özelleştirmeler aracılığıyla diğer sayfalara veya modüllere eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="8ceb2-117">BOPIS senaryosunun çalışması için, ürünlerin "müşteri malzeme çekme" teslim moduyla konfigüre edilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="8ceb2-118">Aksi durumda, modül ilgili sayfalarda gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="8ceb2-119">Teslimat modunun konfigüre edilmesine ilişkin ayrıntılar için bkz. [Teslimat modları ayarla](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="8ceb2-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="8ceb2-120">Aşağıdaki resimde, PDP üzerinde kullanılan bir Mağaza Seçicisi modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Mağaza seçici modülü örneği](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="8ceb2-122">e-Ticarette mağaza seçici modül kullanımı</span><span class="sxs-lookup"><span data-stu-id="8ceb2-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="8ceb2-123">Ürün Ayrıntıları sayfasındaki (PDP) bir ürünün malzeme çekme için uygun olduğu mağazaları görüntülemek için, bir satın alma kutusu modülüne Mağaza Seçici modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="8ceb2-124">Sepet sayfasındaki (PDP) bir ürünün malzeme çekme için uygun olduğu mağazaları görüntülemek için, bir satın alma kutusu modülüne Mağaza Seçici modülü eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="8ceb2-125">Mağaza seçicisi modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="8ceb2-125">Store selector module properties</span></span>

| <span data-ttu-id="8ceb2-126">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="8ceb2-126">Property name</span></span>             | <span data-ttu-id="8ceb2-127">Değer</span><span class="sxs-lookup"><span data-stu-id="8ceb2-127">Value</span></span>                 | <span data-ttu-id="8ceb2-128">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ceb2-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="8ceb2-129">Arama yarıçapı</span><span class="sxs-lookup"><span data-stu-id="8ceb2-129">Search radius</span></span> | <span data-ttu-id="8ceb2-130">Sayı</span><span class="sxs-lookup"><span data-stu-id="8ceb2-130">Number</span></span> | <span data-ttu-id="8ceb2-131">Mağazalar için, mil cinsinden, arama yarıçapını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="8ceb2-132">Herhangi bir değer belirtilmezse, varsayılan arama yarıçapı olan 50 mil değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="8ceb2-133">Hizmet Koşulları</span><span class="sxs-lookup"><span data-stu-id="8ceb2-133">Terms of Service</span></span> | <span data-ttu-id="8ceb2-134">URL</span><span class="sxs-lookup"><span data-stu-id="8ceb2-134">URL</span></span>    |  <span data-ttu-id="8ceb2-135">Bing Haritalar hizmeti için bir hizmet koşulları URL'si gereklidir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="8ceb2-136">Bir sayfaya mağaza seçici modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="8ceb2-136">Add a store selector module to a page</span></span>

<span data-ttu-id="8ceb2-137">Bir mağaza seçici modülü bir ürünün bağlamını gerektiriyor, bu nedenle yalnızca satın alma kutusu ve sepet modülleri içinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="8ceb2-138">Mağaza seçici modülleri bu modüllerin dışında çalışmıyor.</span><span class="sxs-lookup"><span data-stu-id="8ceb2-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="8ceb2-139">Satın alma kutusu modülüne bir mağaza Seçicisi modülü ekleme hakkında bilgi için bkz. [Satın alma kutusu modülü](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="8ceb2-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="8ceb2-140">Sepet kutusu modülüne bir mağaza Seçicisi modülü ekleme hakkında bilgi için bkz. [Sepet modülü](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="8ceb2-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ceb2-141">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8ceb2-141">Additional resources</span></span>

[<span data-ttu-id="8ceb2-142">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="8ceb2-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8ceb2-143">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="8ceb2-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8ceb2-144">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="8ceb2-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8ceb2-145">PDP'ye hızlı gezinti</span><span class="sxs-lookup"><span data-stu-id="8ceb2-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="8ceb2-146">Sepet ve ödemede hızlı tur</span><span class="sxs-lookup"><span data-stu-id="8ceb2-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="8ceb2-147">Teslimat şekillerini ayarla</span><span class="sxs-lookup"><span data-stu-id="8ceb2-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="8ceb2-148">Kuruluşunuz için Bing Haritalar'ı yönetme</span><span class="sxs-lookup"><span data-stu-id="8ceb2-148">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)
