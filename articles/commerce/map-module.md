---
title: Harita modülü
description: Bu konu harita modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: d2cbc67a186a76647a4f7ddc7942b15d3e469ece
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817218"
---
# <a name="map-module"></a><span data-ttu-id="f909d-103">Harita modülü</span><span class="sxs-lookup"><span data-stu-id="f909d-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="f909d-104">Bu konu harita modüllerini ve bunların Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f909d-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f909d-105">Özet</span><span class="sxs-lookup"><span data-stu-id="f909d-105">Overview</span></span>

<span data-ttu-id="f909d-106">Harita modülü, [Bing Haritalar V8 Web Denetimi](https://docs.microsoft.com/bingmaps/v8-web-control/) kullanılarak işlenen etkileşimli bir harita üzerindeki mağazaların konumlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f909d-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="f909d-107">Bir Bing Haritalar API anahtarı gereklidir ve Commerce Headquarters'daki paylaşılan parametreler sayfasına eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="f909d-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="f909d-108">Harita modülleri, kullanıcıların harita konumlarını görüntülemek için seçim yapabilen Yol, Uydu ve Streetside görünümü gibi farklı görünümler sağlar.</span><span class="sxs-lookup"><span data-stu-id="f909d-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="f909d-109">Ayrıca, yakınlaştırma ve kullanıcının konumunu kullanma gibi etkileşimlere de izin verir.</span><span class="sxs-lookup"><span data-stu-id="f909d-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="f909d-110">Bir harita modülü, bir haritada işlenmesi gereken mağazaların coğrafi konumlarını belirlemek için mağaza seçici modülüyle birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="f909d-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="f909d-111">Bir kullanıcı site sayfasında bu modüllerden birinde bir mağaza seçtiğinde mağaza seçici ve harita modülleri etkileşime girer.</span><span class="sxs-lookup"><span data-stu-id="f909d-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="f909d-112">Harita modülleri, mağaza seçici modülleriyle etkileşimi dışında diğer senaryolar için genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="f909d-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="f909d-113">Ancak, modül özelleştirmesi gereklidir.</span><span class="sxs-lookup"><span data-stu-id="f909d-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="f909d-114">Harita modülü Dynamics 365 Commerce 10.0.13 sürümünde bulunur.</span><span class="sxs-lookup"><span data-stu-id="f909d-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="f909d-115">Aşağıdaki resimde mağaza konumları sayfasında kullanılan bir harita modülü örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f909d-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Mağaza seçici modülü örneği](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="f909d-117">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="f909d-117">Module properties</span></span>

| <span data-ttu-id="f909d-118">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="f909d-118">Property name</span></span>             | <span data-ttu-id="f909d-119">Değer</span><span class="sxs-lookup"><span data-stu-id="f909d-119">Value</span></span>                 | <span data-ttu-id="f909d-120">Tanım</span><span class="sxs-lookup"><span data-stu-id="f909d-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f909d-121">Başlık</span><span class="sxs-lookup"><span data-stu-id="f909d-121">Heading</span></span> | <span data-ttu-id="f909d-122">Metin</span><span class="sxs-lookup"><span data-stu-id="f909d-122">Text</span></span> | <span data-ttu-id="f909d-123">Modülün başlığı.</span><span class="sxs-lookup"><span data-stu-id="f909d-123">The heading for the module.</span></span> |
| <span data-ttu-id="f909d-124">Raptiye seçenekleri: Varsayılan simge</span><span class="sxs-lookup"><span data-stu-id="f909d-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="f909d-125">Görüntü</span><span class="sxs-lookup"><span data-stu-id="f909d-125">Image</span></span> | <span data-ttu-id="f909d-126">Haritada gösterilen mağazalar için kullanılacak raptiye sembolü resmi.</span><span class="sxs-lookup"><span data-stu-id="f909d-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="f909d-127">Raptiye seçenekleri: Etkin simge</span><span class="sxs-lookup"><span data-stu-id="f909d-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="f909d-128">Görüntü</span><span class="sxs-lookup"><span data-stu-id="f909d-128">Image</span></span> | <span data-ttu-id="f909d-129">Haritada seçilen bir mağaza için kullanılacak raptiye sembolü resmi.</span><span class="sxs-lookup"><span data-stu-id="f909d-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="f909d-130">Raptiye seçenekleri: Varsayılan simge rengi</span><span class="sxs-lookup"><span data-stu-id="f909d-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="f909d-131">Karakter dizesi</span><span class="sxs-lookup"><span data-stu-id="f909d-131">Character string</span></span> | <span data-ttu-id="f909d-132">Haritadaki raptiye sembollerinin rengi için metin veya onaltılı değer.</span><span class="sxs-lookup"><span data-stu-id="f909d-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="f909d-133">Raptiye seçenekleri: Etkin simge rengi</span><span class="sxs-lookup"><span data-stu-id="f909d-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="f909d-134">Karakter dizesi</span><span class="sxs-lookup"><span data-stu-id="f909d-134">Character string</span></span> | <span data-ttu-id="f909d-135">Haritadaki seçili raptiye simgelerinin rengi için metin veya onaltılı değer.</span><span class="sxs-lookup"><span data-stu-id="f909d-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="f909d-136">Dizini göster</span><span class="sxs-lookup"><span data-stu-id="f909d-136">Show index</span></span> | <span data-ttu-id="f909d-137">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="f909d-137">**True** or **False**</span></span> | <span data-ttu-id="f909d-138">Bu özellik **Doğru** olarak ayarlanırsa bir mağazayı gösteren her raptiye sembolü, bir dizin gösterir.</span><span class="sxs-lookup"><span data-stu-id="f909d-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="f909d-139">Bu dizin, mağaza seçici modülünün gösterdiği liste görünümündeki dizinle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="f909d-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="f909d-140">İzin verilen eşleme URL'lerini sitenin içerik güvenlik ilkesi yönergelerinden ekleme</span><span class="sxs-lookup"><span data-stu-id="f909d-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="f909d-141">Haritalar modülünün Bing Haritalar ile etkileşime girmesini istiyorsanız, sitenizin içerik güvenlik ilkesi (CSP) uyarınca aşağıdaki eşleme URL'lerine izin verildiğinden ("izin verilenler" olarak da bilinir) emin olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f909d-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="f909d-142">Bu kurulum, çeşitli site CSP yönergelerine (örneğin, **img-src**) izin verilen URL'leri ekleyerek Commerce site oluşturucuda gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f909d-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="f909d-143">Daha fazla bilgi için bkz. [İçerik güvenlik ilkesi](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="f909d-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="f909d-144">**connect-src** yönergesine **&#42;.bing.com** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f909d-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="f909d-145">**img-src** yönergesine **&#42;.virtualearth.net** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f909d-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="f909d-146">**Script-src** yönergesine **&#42;.bing.com, &#42;.virtualearth.net** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f909d-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="f909d-147">**script style-src** yönergesine **&#42;.bing.com** ekleyin.</span><span class="sxs-lookup"><span data-stu-id="f909d-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="f909d-148">Sayfaya harita modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="f909d-148">Add a map module to a page</span></span>

<span data-ttu-id="f909d-149">Bir sayfada harita modülünü yapılandırma hakkında ayrıntılı bilgi için bkz. [Mağaza seçici modülü](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="f909d-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="f909d-150">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f909d-150">Additional resources</span></span>

[<span data-ttu-id="f909d-151">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="f909d-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f909d-152">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="f909d-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f909d-153">Alışveriş sepeti modülü</span><span class="sxs-lookup"><span data-stu-id="f909d-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f909d-154">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="f909d-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="f909d-155">Kuruluşunuz için Bing Haritalar'ı yönetme</span><span class="sxs-lookup"><span data-stu-id="f909d-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="f909d-156">Bing Haritalar V8 Web Denetimi</span><span class="sxs-lookup"><span data-stu-id="f909d-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
