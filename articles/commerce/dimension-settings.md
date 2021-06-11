---
title: Ürün boyutları için görüntü ayarlarını uygulama
description: Bu konu, ürün boyutlarının görüntü ayarlarını kapsar ve Microsoft Dynamics 365 Commerce'de bunların nasıl uygulanacağını açıklar.
author: anupamar-ms
ms.date: 05/28/2021
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
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117251"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="8180c-103">Ürün boyutları için görüntü ayarlarını uygulama</span><span class="sxs-lookup"><span data-stu-id="8180c-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="8180c-104">Bu konu, ürün boyutlarının görüntü ayarlarını kapsar ve Microsoft Dynamics 365 Commerce'de bunların nasıl uygulanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="8180c-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8180c-105">Dynamics 365 Commerce, ürün çeşitlerini ayırt etmek için boyut, stil ve renk boyutlarını destekler.</span><span class="sxs-lookup"><span data-stu-id="8180c-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="8180c-106">Boyutlar genellikle boyutlar için "Küçük", "Orta" ve "Büyük" ve renkler için "Siyah" ve "Kahverengi" gibi metin değerleri olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8180c-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="8180c-107">Ancak, bir ürün birçok varyasyonu destekliyorsa her varyasyon için görüntüyü görüntülemek için birden fazla seçim gerektiğinden, ürün varyasyonlarına göz atmak zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="8180c-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="8180c-108">Ürün varyasyonlarına göz atmayı kolaylaştırmak için, Commerce'in 10.0.20 sürümü, boyutları renk örneği olarak göstermek için görüntüleri ve onaltılık (onaltılık) kodları kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="8180c-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="8180c-109">Commerce site oluşturucusunda, boyut ayarları **Site Ayarlar \> Uzantılar \> Boyut Ayarları** altında tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="8180c-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="8180c-110">Aşağıdaki resimde, site oluşturucudaki boyut ayarlarına bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8180c-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Commerce site oluşturucusunda site ayarları örneği](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="8180c-112">İki boyut ayarı kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="8180c-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="8180c-113">**Görüntü olarak görüntülenecek boyutlar** – Ürün ayrıntıları sayfaları (PDP'ler) ve arama sonuç listesi sayfaları gibi e-ticaret sitesi sayfalarında hangi boyutların renk örneği olarak görünmesi gerektiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8180c-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="8180c-114">Renk, boyut ve stil boyutlarının herhangi bir birleşimi renk örneği olarak gösterilebilir.</span><span class="sxs-lookup"><span data-stu-id="8180c-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="8180c-115">Renk örneği olarak görüntülenmek üzere bir boyut seçilirse, Commerce modülü işleme, altıgen kod renk örneğinin kullanılabilir bir yapılandırmasını arar.</span><span class="sxs-lookup"><span data-stu-id="8180c-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="8180c-116">Her iki kod yapılandırılmamışsa, sistem mantığı bir görüntü URL'si renk örneğinin yapılandırmalarını arar.</span><span class="sxs-lookup"><span data-stu-id="8180c-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="8180c-117">Ne bir altıgen kod ne de bir resim URL'si yapılandırılmamışsa, metin gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8180c-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="8180c-118">Aşağıdaki resimde, bir e-ticaret sitesindeki PDP'nin renk ve boyut örnekleri içerdiği bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8180c-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="8180c-119">Bu örnekte, renk boyutu için bir altıgen kod yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="8180c-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="8180c-120">Bu nedenle, renk örnekleri renk olarak gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8180c-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="8180c-121">Ancak, boyut boyutu için bir altıgen kod veya resim URL'si yapılandırılmaz.</span><span class="sxs-lookup"><span data-stu-id="8180c-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="8180c-122">Bu nedenle, metin gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8180c-122">Therefore, text is shown.</span></span>

    ![E-ticaret ürün ayrıntıları sayfasında renk örneği olarak gösterilen renk boyutu örneği](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="8180c-124">**Ürün kartında görüntülenecek boyutlar** – Listelerde ve liste sayfalarında gösterilen ürün kartlarında hangi boyutların görünleneceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8180c-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="8180c-125">Boyutun ürün kartında görünebilmesi için önce bu ayarın bu boyut için etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="8180c-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="8180c-126">**Görüntü olarak görüntülenecek Boyutlar** ayarı da etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="8180c-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="8180c-127">Ürün kartlarındaki renk örneği seçimi davranışı renk boyutu için en iyi duruma getirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8180c-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="8180c-128">Diğer boyutlar için renk örneği seçim davranışını özelleştirmek için bir görünüm uzantısı gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="8180c-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="8180c-129">Aşağıdaki resimde, bir e-ticaret sitesindeki liste sayfasının renk örnekleri içeren ürün kartları içerdiği bir örnek gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8180c-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![E-ticaret liste sayfasında renk örneği olarak gösterilen renk boyutu örneği](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="8180c-131">Ürün boyutlarını site sayfalarında renk örneği olarak gösterilecek şekilde yapılandırma hakkında bilgi için bkz. [Ürün boyutu değerlerini renk örneği olarak görünecek şekilde yapılandırma](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="8180c-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8180c-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8180c-132">Additional resources</span></span>

[<span data-ttu-id="8180c-133">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="8180c-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8180c-134">Arama sonuçları modülü</span><span class="sxs-lookup"><span data-stu-id="8180c-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="8180c-135">Satın alma kutusu modülü</span><span class="sxs-lookup"><span data-stu-id="8180c-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8180c-136">Ürün boyutu değerlerini renk örneği olarak görünecek şekilde yapılandırma</span><span class="sxs-lookup"><span data-stu-id="8180c-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
