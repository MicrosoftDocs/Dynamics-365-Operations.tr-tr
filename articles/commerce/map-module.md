---
title: Harita modülü
description: Bu konu harita modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/31/2020
ms.locfileid: "3647070"
---
# <a name="map-module"></a><span data-ttu-id="cf85a-103">Harita modülü</span><span class="sxs-lookup"><span data-stu-id="cf85a-103">Map module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="cf85a-104">Bu konu harita modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="cf85a-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cf85a-105">Özet</span><span class="sxs-lookup"><span data-stu-id="cf85a-105">Overview</span></span>

<span data-ttu-id="cf85a-106">Harita modülü, [Bing Haritalar V8 Web Denetimi](https://docs.microsoft.com/bingmaps/v8-web-control/) kullanılarak işlenen etkileşimli bir harita üzerindeki mağazaların konumlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="cf85a-107">Bir Bing Haritalar API anahtarı gereklidir ve Commerce Headquarters'daki paylaşılan parametreler sayfasına eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="cf85a-108">Harita modülleri, kullanıcıların harita konumlarını görüntülemek için seçim yapabilen Yol, Uydu ve Streetside görünümü gibi farklı görünümler sağlar.</span><span class="sxs-lookup"><span data-stu-id="cf85a-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="cf85a-109">Ayrıca, yakınlaştırma ve kullanıcının konumunu kullanma gibi etkileşimlere de izin verir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="cf85a-110">Bir harita modülü, bir haritada işlenmesi gereken mağazaların coğrafi konumlarını belirlemek için mağaza seçici modülüyle birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="cf85a-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="cf85a-111">Bir kullanıcı site sayfasında bu modüllerden birinde bir mağaza seçtiğinde mağaza seçici ve harita modülleri etkileşime girer.</span><span class="sxs-lookup"><span data-stu-id="cf85a-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="cf85a-112">Harita modülleri, mağaza seçici modülleriyle etkileşimi dışında diğer senaryolar için genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="cf85a-113">Ancak, modül özelleştirmesi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-113">However, module customization is required.</span></span>

<span data-ttu-id="cf85a-114">Harita modülü Commerce 10.0.13 sürümünde kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="cf85a-114">The map module was introduced in Commerce version 10.0.13.</span></span>

<span data-ttu-id="cf85a-115">Aşağıdaki resimde mağaza konumları sayfasında kullanılan bir harita modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Mağaza seçici modülü örneği](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="cf85a-117">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="cf85a-117">Module properties</span></span>

| <span data-ttu-id="cf85a-118">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="cf85a-118">Property name</span></span>             | <span data-ttu-id="cf85a-119">Değer</span><span class="sxs-lookup"><span data-stu-id="cf85a-119">Value</span></span>                 | <span data-ttu-id="cf85a-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf85a-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="cf85a-121">Başlık</span><span class="sxs-lookup"><span data-stu-id="cf85a-121">Heading</span></span> | <span data-ttu-id="cf85a-122">Metin</span><span class="sxs-lookup"><span data-stu-id="cf85a-122">Text</span></span> | <span data-ttu-id="cf85a-123">Modülün başlığı.</span><span class="sxs-lookup"><span data-stu-id="cf85a-123">The heading for the module.</span></span> |
| <span data-ttu-id="cf85a-124">Raptiye seçenekleri: Varsayılan simge</span><span class="sxs-lookup"><span data-stu-id="cf85a-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="cf85a-125">Görüntü</span><span class="sxs-lookup"><span data-stu-id="cf85a-125">Image</span></span> | <span data-ttu-id="cf85a-126">Haritada gösterilen mağazalar için kullanılacak raptiye sembolü resmi.</span><span class="sxs-lookup"><span data-stu-id="cf85a-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="cf85a-127">Raptiye seçenekleri: Etkin simge</span><span class="sxs-lookup"><span data-stu-id="cf85a-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="cf85a-128">Görüntü</span><span class="sxs-lookup"><span data-stu-id="cf85a-128">Image</span></span> | <span data-ttu-id="cf85a-129">Haritada seçilen bir mağaza için kullanılacak raptiye sembolü resmi.</span><span class="sxs-lookup"><span data-stu-id="cf85a-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="cf85a-130">Raptiye seçenekleri: Varsayılan simge rengi</span><span class="sxs-lookup"><span data-stu-id="cf85a-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="cf85a-131">Karakter dizesi</span><span class="sxs-lookup"><span data-stu-id="cf85a-131">Character string</span></span> | <span data-ttu-id="cf85a-132">Haritadaki raptiye sembollerinin rengi için metin veya onaltılı değer.</span><span class="sxs-lookup"><span data-stu-id="cf85a-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="cf85a-133">Raptiye seçenekleri: Etkin simge rengi</span><span class="sxs-lookup"><span data-stu-id="cf85a-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="cf85a-134">Karakter dizesi</span><span class="sxs-lookup"><span data-stu-id="cf85a-134">Character string</span></span> | <span data-ttu-id="cf85a-135">Haritadaki seçili raptiye simgelerinin rengi için metin veya onaltılı değer.</span><span class="sxs-lookup"><span data-stu-id="cf85a-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="cf85a-136">Dizini göster</span><span class="sxs-lookup"><span data-stu-id="cf85a-136">Show index</span></span> | <span data-ttu-id="cf85a-137">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="cf85a-137">**True** or **False**</span></span> | <span data-ttu-id="cf85a-138">Bu özellik **Doğru** olarak ayarlanırsa bir mağazayı gösteren her raptiye sembolü, bir dizin gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="cf85a-139">Bu dizin, mağaza seçici modülünün gösterdiği liste görünümündeki dizinle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="cf85a-140">İzin verilen eşleme URL'lerini sitenin içerik güvenlik ilkesi yönergelerinden ekleme</span><span class="sxs-lookup"><span data-stu-id="cf85a-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="cf85a-141">Haritalar modülünün Bing Haritalar ile etkileşime girmesini istiyorsanız, sitenizin içerik güvenlik ilkesi (CSP) uyarınca aşağıdaki eşleme URL'lerine izin verildiğinden ("izin verilenler" olarak da bilinir) emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="cf85a-142">Bu kurulum, çeşitli site CSP yönergelerine (örneğin, **img-src**) izin verilen URL'leri ekleyerek Commerce site oluşturucuda gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="cf85a-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="cf85a-143">Daha fazla bilgi için bkz. [İçerik güvenlik ilkesi](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="cf85a-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="cf85a-144">**connect-src** yönergesine **&#42;.bing.com** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cf85a-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="cf85a-145">**img-src** yönergesine **&#42;.virtualearth.net** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cf85a-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="cf85a-146">**Script-src** yönergesine **&#42;.bing.com, &#42;.virtualearth.net** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cf85a-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="cf85a-147">**script style-src** yönergesine **&#42;.bing.com** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cf85a-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="cf85a-148">Sayfaya harita modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="cf85a-148">Add a map module to a page</span></span>

<span data-ttu-id="cf85a-149">Bir sayfada harita modülünü yapılandırma hakkında ayrıntılı bilgi için bkz. [Mağaza seçici modülü](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="cf85a-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="cf85a-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cf85a-150">Additional resources</span></span>

[<span data-ttu-id="cf85a-151">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="cf85a-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cf85a-152">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="cf85a-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="cf85a-153">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="cf85a-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cf85a-154">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="cf85a-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="cf85a-155">Kuruluşunuz için Bing Haritalar'ı yönetme</span><span class="sxs-lookup"><span data-stu-id="cf85a-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="cf85a-156">Bing Haritalar V8 Web Denetimi</span><span class="sxs-lookup"><span data-stu-id="cf85a-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
