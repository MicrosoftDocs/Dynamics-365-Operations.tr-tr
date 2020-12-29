---
title: 4xx/5xx durum kodu hataları için özel yanıt sayfaları oluşturma
description: Bu konu, Microsoft Dynamics 365 Commerce'un yazma araçlarını kullanarak 4xx ve 5xx durum kodu hataları için özel yanıt sayfaları oluşturma yöntemini açıklamaktadır .
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416395"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="99e8e-103">4xx/5xx durum kodu hataları için özel yanıt sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="99e8e-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="99e8e-104">Bu konu, Microsoft Dynamics 365 Commerce'un yazma araçlarını kullanarak 4xx ve 5xx durum kodu hataları için özel yanıt sayfaları oluşturma yöntemini açıklamaktadır .</span><span class="sxs-lookup"><span data-stu-id="99e8e-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="99e8e-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="99e8e-105">Overview</span></span>

<span data-ttu-id="99e8e-106">Bir istek başarılı olmazsa, sunucu HTTP durum kodu hata yanıtları verir.</span><span class="sxs-lookup"><span data-stu-id="99e8e-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="99e8e-107">404 durum kodu yakalanarak sayfa bulunamazsa döndürülür ve sunucu hatası oluşursa 500 durum kodu yakalanır ve döndürülür.</span><span class="sxs-lookup"><span data-stu-id="99e8e-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="99e8e-108">Dynamics 365 Commerce'te uygulama kullanıcıları bu durum kodu hata yanıtları için kullanıcılara gösterilen özel durum kodu hata yanıtı sayfaları oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="99e8e-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="99e8e-109">Durum kodu oluştur hata yanıt sayfası</span><span class="sxs-lookup"><span data-stu-id="99e8e-109">Build a status code error response page</span></span>

<span data-ttu-id="99e8e-110">Durum kodu hata yanıtı sayfası oluşturmaya başlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="99e8e-111">Tercih ettiğiniz Web tarayıcınızda Dynamics 365 Commerce oturumu açın.</span><span class="sxs-lookup"><span data-stu-id="99e8e-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="99e8e-112">4xx/5xx durum kodu hata yanıtı sayfası oluşturmak istediğiniz siteyi seçin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="99e8e-113">Şablonu oluştur</span><span class="sxs-lookup"><span data-stu-id="99e8e-113">Build the template</span></span>

<span data-ttu-id="99e8e-114">Durum kodu hata yanıtı sayfası oluşturmaya başlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="99e8e-115">**Şablonlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="99e8e-116">Yeni sayfa şablonu oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="99e8e-117">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, yeni şablon için ad girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="99e8e-118">Durum kodu hata yanıtı sayfasında olmasını istediğiniz yapıyı temel alarak şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="99e8e-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="99e8e-119">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="99e8e-120">Durum kodu oluştur hata yanıt sayfası</span><span class="sxs-lookup"><span data-stu-id="99e8e-120">Build the status code error response page</span></span>

<span data-ttu-id="99e8e-121">Durum kodu hata yanıtı sayfası oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="99e8e-122">**Sayfalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="99e8e-123">Sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="99e8e-124">**Şablon seç** iletişim kutusunda bir şablon seçin ve sonra **Sayfa adı** altında, durum kodu hata yanıt sayfası için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="99e8e-125">**Sayfa URL**'si alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="99e8e-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="99e8e-126">Sayfayı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="99e8e-126">Build the page.</span></span>
1. <span data-ttu-id="99e8e-127">**Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="99e8e-128">4xx ve 5xx durum kodu hataları için ayrı durum kodu hatası yanıtı sayfaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99e8e-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="99e8e-129">Alternatif olarak, her iki hata kategorisi için de aynı genel durum kodu hata yanıtı sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99e8e-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="99e8e-130">Durum kodu hatası için yeniden yönlendirme ayarlayın hata yanıtı sayfası</span><span class="sxs-lookup"><span data-stu-id="99e8e-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="99e8e-131">Durum kodu hata yanıtı sayfasına yeniden yönlendirme ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="99e8e-132">**URL'ler \> Yeni \> Yeni Diğer Ad** a gidin ve daha önce oluşturduğunuz durum kodu hata yanıtı sayfasını seçin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="99e8e-133">**Diğer ad** alanına, yeniden yönlendirme ayarlamakta olduğunuz durum kodu hata yanıtı sayfasına bağlı olarak **varsayılan-4xx** veya **varsayılan-5xx** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="99e8e-134">Bu diğer adlar yayımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="99e8e-134">These aliases must be published.</span></span> <span data-ttu-id="99e8e-135">Aksi durumda yeniden yönlendirme çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99e8e-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="99e8e-136">Bağlantıyı onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="99e8e-137">Her iki hata kategorisi için de tek bir durum kodu hata yanıtı sayfası kullanıyorsanız, diğer hata kategorisine ait diğer adı aynı sayfaya bağlamak için bu yordamı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="99e8e-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99e8e-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="99e8e-138">Additional resources</span></span>

[<span data-ttu-id="99e8e-139">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="99e8e-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="99e8e-140">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="99e8e-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="99e8e-141">URL sayfası oluşturma</span><span class="sxs-lookup"><span data-stu-id="99e8e-141">Create a page URL</span></span>](create-page-url.md)
