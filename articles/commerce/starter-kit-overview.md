---
title: Modül kitaplığına genel bakış
description: Bu konu Microsoft Dynamics 365 Commerce modül kitaplığı hakkında bilgi sağlar.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76fd75c2ed9a3ba4728129b77a43b50267be3bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795345"
---
# <a name="module-library-overview"></a><span data-ttu-id="65ff5-103">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="65ff5-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65ff5-104">Bu konu Microsoft Dynamics 365 Commerce modül kitaplığı hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="65ff5-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="65ff5-105">Dynamics 365 Commerce modül kitaplığı, bir e-ticaret Web sitesi oluşturmak için kullanılabilen modüller topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="65ff5-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="65ff5-106">Modüllerin hem Kullanıcı arabirimi (UI) yönleri, hem de işlevsel davranış yönleri vardır.</span><span class="sxs-lookup"><span data-stu-id="65ff5-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="65ff5-107">Görünüm ve deneyimi değiştirmek için, Temalar, modül kitaplığındaki modüllere uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="65ff5-108">Temalar geçişli stil sayfaları (CSS) kullanır.</span><span class="sxs-lookup"><span data-stu-id="65ff5-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="65ff5-109">"Fabrikam" adlı hayali bir e-ticaret sitesi için Tema, modül kitaplığının bir parçası olarak sağlanmıştır ve bir referans olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="65ff5-110">Modül kitaplığı modülleri</span><span class="sxs-lookup"><span data-stu-id="65ff5-110">Module library modules</span></span>

<span data-ttu-id="65ff5-111">Aşağıdaki modül türleri, modül kitaplığında sağlanmıştır:</span><span class="sxs-lookup"><span data-stu-id="65ff5-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="65ff5-112">**Konteyner modülü** – Bir konteyner modülü, diğer modüller için ana bilgisayar görevi gören basit bir modüldür.</span><span class="sxs-lookup"><span data-stu-id="65ff5-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="65ff5-113">İçinde olan modüllerin yerleşimini denetler.</span><span class="sxs-lookup"><span data-stu-id="65ff5-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="65ff5-114">**Pazarlama modülleri** – Pazarlama modüllerinde engel, metin engeli, video oynatıcı ve döngü modüller bulunur.</span><span class="sxs-lookup"><span data-stu-id="65ff5-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="65ff5-115">İçeriğin gösterimi için tüm bu modüller kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="65ff5-116">İçerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="65ff5-117">**Üstbilgi ve altbilgi modülleri** – Üstbilgi ve altbilgi modülleri, tüm site sayfalarının üstbilgi ve altbilgisinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="65ff5-118">Bu modüller, özellikler üzerinden gerektikçe yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="65ff5-119">**Arama modülleri** – Başlıktaki arama modülü kullanılarak ürünler keşfedilebilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="65ff5-120">Arama sonuçları arama sonuçları sayfasında görünür.</span><span class="sxs-lookup"><span data-stu-id="65ff5-120">Search results appear on the search results page.</span></span> <span data-ttu-id="65ff5-121">Ürünler, kanal gezinti hiyerarşisinde desteklenen her kategori için adanmış sayfalar olan Kategori sayfalarında da bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="65ff5-122">Ek olarak, iyileştirici modülleri arama sonuçları ve kategori sayfalarındaki sonuçlara ek filtre uygulamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="65ff5-123">**Ürün ayrıntıları sayfası modülleri** – Ürün ayrıntıları sayfaları ürün bilgilerini göstermek için birkaç modül kullanır.</span><span class="sxs-lookup"><span data-stu-id="65ff5-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="65ff5-124">Satın alma kutusu modülü müşterilerin ürünleri görüntülemesine ve bunları alışveriş sepetine eklemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="65ff5-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="65ff5-125">Teknik özellikler modülü gibi diğer modüller ürün ayrıntılarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="65ff5-126">Derecelendirmeler ve incelemeler modülü incelemeleri görüntülemek ve sağlamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="65ff5-127">**Mağaza modülünde çevrimiçi mağazadan satın alın** – depo modülünde çevrimiçi mağazadan satın alma , Bing Haritalar ile tümleşiktir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="65ff5-128">Satın aldıkları ürünlerin nereden çekilebileceği, yakındaki mağazaların bulunması için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="65ff5-129">**Satın alma modülleri** – Satın alma modülleri, alışveriş sepetine madde eklemek için kullanılabilen sepet modülünü içerir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="65ff5-130">Kullanıma alma modülü sevkiyat adresini, teslimat seçeneklerini ve hediye kartını, bağlılık programı ve kredi kartı bilgilerini yakalar ve böylece bir sipariş işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="65ff5-131">Bir sipariş yerleştirildikten sonra, onay ayrıntılarını göstermek için sipariş teyidi modülü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="65ff5-132">**Hesap yönetimi modülleri** – oturum açma modülü müşterilerinin varolan bir hesapla oturum açmasına izin verir ve kaydolma modülü de yeni bir hesap oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65ff5-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="65ff5-133">Bir hesap oluşturulduktan sonra, sipariş geçmişi modülü en son siparişleri görüntülemek için kullanılabilir ve sipariş ayrıntıları modülü sipariş ayrıntılarını görüntülemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="65ff5-134">**Öneriler modülü** – Öneriler, ürün yerleştirme modülü kullanılarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="65ff5-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="65ff5-135">Bu modül herhangi bir sayfada gezinebilecek algoritmik ve düzenleme listelerini destekler.</span><span class="sxs-lookup"><span data-stu-id="65ff5-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65ff5-136">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="65ff5-136">Additional resources</span></span>

[<span data-ttu-id="65ff5-137">Konteyner modülü</span><span class="sxs-lookup"><span data-stu-id="65ff5-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="65ff5-138">Satınalma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="65ff5-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="65ff5-139">Sepet modülü</span><span class="sxs-lookup"><span data-stu-id="65ff5-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="65ff5-140">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="65ff5-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="65ff5-141">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="65ff5-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="65ff5-142">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="65ff5-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="65ff5-143">Alt bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="65ff5-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]