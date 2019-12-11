---
title: Uyarı modülü
description: Bu konu uyarı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785364"
---
# <a name="alert-module"></a><span data-ttu-id="d7e61-103">Uyarı modülü</span><span class="sxs-lookup"><span data-stu-id="d7e61-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d7e61-104">Bu konu uyarı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="d7e61-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d7e61-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="d7e61-105">Overview</span></span>

<span data-ttu-id="d7e61-106">Bir sayfada satır içi bilgilendirici iletiler göstermek için bir uyarı modülü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d7e61-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="d7e61-107">Uyarı modülleri bir metin iletisini ve bir bağlantıyı destekler.</span><span class="sxs-lookup"><span data-stu-id="d7e61-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="d7e61-108">Bir e-ticaret sitesinin tüm sayfalarında görünen site çapında yükseltmeleri göstermek için kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="d7e61-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="d7e61-109">Uyarı modülleri, içerik yönetimi sistemindeki (CMS) veriler tarafından yönlendiriliyor ve herhangi bir sayfaya konabilir.</span><span class="sxs-lookup"><span data-stu-id="d7e61-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="d7e61-110">E-ticarette uyarı modülleri örnekleri</span><span class="sxs-lookup"><span data-stu-id="d7e61-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="d7e61-111">Site üstbilgisinde site çapında yükseltmeler veya iletiler olduğu için uyarı modülleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d7e61-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="d7e61-112">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="d7e61-112">Here are some examples:</span></span>

<span data-ttu-id="d7e61-113">"Yıllık satış, 10 gün içinde biter"</span><span class="sxs-lookup"><span data-stu-id="d7e61-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="d7e61-114">"Okul satışı ile büyük bir tasarruf yapın.</span><span class="sxs-lookup"><span data-stu-id="d7e61-114">"Save big with back to school sale.</span></span> <span data-ttu-id="d7e61-115">Şimdi alışveriş yap."</span><span class="sxs-lookup"><span data-stu-id="d7e61-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="d7e61-116">Uyarı modülü özellikleri</span><span class="sxs-lookup"><span data-stu-id="d7e61-116">Alert module properties</span></span>

| <span data-ttu-id="d7e61-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="d7e61-117">Property name</span></span>  | <span data-ttu-id="d7e61-118">Değer</span><span class="sxs-lookup"><span data-stu-id="d7e61-118">Value</span></span>                              | <span data-ttu-id="d7e61-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7e61-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="d7e61-120">Metin</span><span class="sxs-lookup"><span data-stu-id="d7e61-120">Text</span></span>           | <span data-ttu-id="d7e61-121">Metin</span><span class="sxs-lookup"><span data-stu-id="d7e61-121">Text</span></span>                               | <span data-ttu-id="d7e61-122">Uyarı modülünde görünen metin iletisi.</span><span class="sxs-lookup"><span data-stu-id="d7e61-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="d7e61-123">Metin hizalama</span><span class="sxs-lookup"><span data-stu-id="d7e61-123">Text alignment</span></span> | <span data-ttu-id="d7e61-124">**Sağ**, **Sol** veya **Orta**</span><span class="sxs-lookup"><span data-stu-id="d7e61-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="d7e61-125">Metnin uyarı modülünde nasıl hizalandığını tanımlayan bir değer.</span><span class="sxs-lookup"><span data-stu-id="d7e61-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="d7e61-126">Uyarıyı kapat</span><span class="sxs-lookup"><span data-stu-id="d7e61-126">Dismiss alert</span></span>  | <span data-ttu-id="d7e61-127">**Doğru** veya **yanlış**</span><span class="sxs-lookup"><span data-stu-id="d7e61-127">**True** or **False**</span></span>              | <span data-ttu-id="d7e61-128">Değer **doğru** olarak ayarlanırsa, müşteri uyarıyı yok edebilir.</span><span class="sxs-lookup"><span data-stu-id="d7e61-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="d7e61-129">Bağla</span><span class="sxs-lookup"><span data-stu-id="d7e61-129">Link</span></span>           | <span data-ttu-id="d7e61-130">URL</span><span class="sxs-lookup"><span data-stu-id="d7e61-130">URL</span></span>                                | <span data-ttu-id="d7e61-131">İsteğe bağlı bağlantı için URL.</span><span class="sxs-lookup"><span data-stu-id="d7e61-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="d7e61-132">Sayfaya uyarı modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="d7e61-132">Add an alert module to a page</span></span> 

<span data-ttu-id="d7e61-133">Bir sayfaya uyarı modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d7e61-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="d7e61-134">**Uyarı şablonu** adlı bir sayfa şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d7e61-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="d7e61-135">Varsayılan sayfanın **ana** yuvasına bir uyarı modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d7e61-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="d7e61-136">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="d7e61-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="d7e61-137">**Uyarı sayfası** adlı bir sayfa oluşturmak için yeni oluşturduğunuz uyarı şablonunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="d7e61-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="d7e61-138">Yeni sayfanın **ana** yuvasına bir uyarı modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d7e61-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="d7e61-139">Uyarı modülünün ayarlarında uyarı metnini girin.</span><span class="sxs-lookup"><span data-stu-id="d7e61-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="d7e61-140">Uyarı modülünü daha fazla özelleştirmek istiyorsanız diğer özellikleri düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d7e61-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="d7e61-141">Sayfayı kaydet ve önizleyin.</span><span class="sxs-lookup"><span data-stu-id="d7e61-141">Save and preview the page.</span></span> <span data-ttu-id="d7e61-142">Sayfanın üst kısmında, eklediğiniz metni içeren bir uyarı görmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="d7e61-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="d7e61-143">Sayfayı giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="d7e61-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d7e61-144">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d7e61-144">Additional resources</span></span>

[<span data-ttu-id="d7e61-145">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="d7e61-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d7e61-146">Döngü modülü</span><span class="sxs-lookup"><span data-stu-id="d7e61-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="d7e61-147">İçerik zengin blok modülü</span><span class="sxs-lookup"><span data-stu-id="d7e61-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="d7e61-148">İçerik yerleştirme modülü</span><span class="sxs-lookup"><span data-stu-id="d7e61-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="d7e61-149">Özellik modülü</span><span class="sxs-lookup"><span data-stu-id="d7e61-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="d7e61-150">Hero modülü</span><span class="sxs-lookup"><span data-stu-id="d7e61-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="d7e61-151">Video oynatıcı modülü</span><span class="sxs-lookup"><span data-stu-id="d7e61-151">Video player module</span></span>](add-video-player.md)
