---
title: Favicon ekleme
description: Bu konu, sitenize bir tercih simgesi ekleneceğini açıklamaktadır.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001560"
---
# <a name="add-a-favicon"></a><span data-ttu-id="77346-103">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="77346-103">Add a favicon</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="77346-104">Bu konu, sitenize bir tercih simgesi ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="77346-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="77346-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="77346-105">Overview</span></span>

<span data-ttu-id="77346-106">Bir tercih edilen simge, Web tarayıcısı sekmesinde, adres çubuğunda, gözatma geçmişinde ve diğer yerlerin yanı sıra yer imleri veya Sık Kullanılanlar'da gösterilen küçük bir grafik dosyasıdır.</span><span class="sxs-lookup"><span data-stu-id="77346-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="77346-107">Markanızı temsil ettiğinden ve yeniden zorlayan ve sitenizi müşterilerinizin ziyaret ettiği diğer sitelerden ayırt etmenize yardımcı olacağından sitenize bir tercih edilen bir simge eklemeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="77346-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="77346-108">Sitenize çeşitli boyutlarda ve dosya türlerindeki birçok tercih edilebilir simge ekleyebilmenize rağmen bu konu, tek bir tercih edilen simgenin nasıl ekleneceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="77346-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="77346-109">Ancak, aynı işlem ve yer, daha fazla tercih edilen simge eklemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="77346-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="77346-110">Sitenizin varlık koleksiyonuna bir tercih simgesi yükleyin</span><span class="sxs-lookup"><span data-stu-id="77346-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="77346-111">Sitenizin varlık koleksiyonuna bir tercih simgesi yüklemek için aşağıdakileri takip edin.</span><span class="sxs-lookup"><span data-stu-id="77346-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="77346-112">**Varlıklar \> Yükle \> Varlıkları yükle**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="77346-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="77346-113">Yerel dosya sisteminizdeki tercih simgesini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="77346-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="77346-114">Bir başlık girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="77346-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="77346-115">Sağdaki özellik bölmesinde, tercih edilen simgenin ortak URL'sini kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="77346-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="77346-116">**Yükledikten sonra varlıkları Yayınla** seçeneğini seçmezseniz, **varlıklar** sayfasına dönmeniz ve daha sonra yeniden öncelik simgesini el ile yayımlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="77346-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="77346-117">Tercih simgesi için HTML oluşturun</span><span class="sxs-lookup"><span data-stu-id="77346-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="77346-118">Tercih edilen simgenin HTML'i oluşturmak için aşağıdaki HTML kod parçacığını kullanın.</span><span class="sxs-lookup"><span data-stu-id="77346-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="77346-119">**Href** özniteliği için, **Tercih\_simgeniz\_için\_genel\_URL**'yi önceden kopyaladığınız ortak URL ile değiştirin.</span><span class="sxs-lookup"><span data-stu-id="77346-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="77346-120">Tercih simgesi için HTML'yi sayfalarınızın \<baş\> öğesine ekleyin</span><span class="sxs-lookup"><span data-stu-id="77346-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="77346-121">Sitenize bir tercih simgesi eklemek için, site sayfalarınızın **\<baş\>** öğesine herhangi bir türdeki HTML veya kod eklemek için kullanılan yordamın aynısını kullanın.</span><span class="sxs-lookup"><span data-stu-id="77346-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77346-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="77346-122">Additional resources</span></span>

[<span data-ttu-id="77346-123">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="77346-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="77346-124">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="77346-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="77346-125">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="77346-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="77346-126">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="77346-126">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="77346-127">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="77346-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="77346-128">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="77346-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="77346-129">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="77346-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

