---
title: 4xx/5xx durum kodu hataları için özel yanıt sayfaları oluşturma
description: Bu konu, Microsoft Dynamics 365 Commerce'un yazma araçlarını kullanarak 4xx ve 5xx durum kodu hataları için özel yanıt sayfaları oluşturma yöntemini açıklamaktadır .
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 4477a0a43971b5322c6acd6971cba2e79e2dc8c6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001165"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="b1744-103">4xx/5xx durum kodu hataları için özel yanıt sayfaları oluşturma</span><span class="sxs-lookup"><span data-stu-id="b1744-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b1744-104">Bu konu, Microsoft Dynamics 365 Commerce'un yazma araçlarını kullanarak 4xx ve 5xx durum kodu hataları için özel yanıt sayfaları oluşturma yöntemini açıklamaktadır .</span><span class="sxs-lookup"><span data-stu-id="b1744-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b1744-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="b1744-105">Overview</span></span>

<span data-ttu-id="b1744-106">Bir istek başarılı olmazsa, sunucu HTTP durum kodu hata yanıtları verir.</span><span class="sxs-lookup"><span data-stu-id="b1744-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="b1744-107">404 durum kodu yakalanarak sayfa bulunamazsa döndürülür ve sunucu hatası oluşursa 500 durum kodu yakalanır ve döndürülür.</span><span class="sxs-lookup"><span data-stu-id="b1744-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="b1744-108">Dynamics 365 Commerce'te uygulama kullanıcıları bu durum kodu hata yanıtları için kullanıcılara gösterilen özel durum kodu hata yanıtı sayfaları oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="b1744-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="b1744-109">Durum kodu oluştur hata yanıt sayfası</span><span class="sxs-lookup"><span data-stu-id="b1744-109">Build a status code error response page</span></span>

<span data-ttu-id="b1744-110">Durum kodu hata yanıtı sayfası oluşturmaya başlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b1744-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="b1744-111">Tercih ettiğiniz Web tarayıcınızda Dynamics 365 Commerce oturumu açın.</span><span class="sxs-lookup"><span data-stu-id="b1744-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="b1744-112">4xx/5xx durum kodu hata yanıtı sayfası oluşturmak istediğiniz siteyi seçin.</span><span class="sxs-lookup"><span data-stu-id="b1744-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="b1744-113">Şablonu oluştur</span><span class="sxs-lookup"><span data-stu-id="b1744-113">Build the template</span></span>

<span data-ttu-id="b1744-114">Durum kodu hata yanıtı sayfası oluşturmaya başlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b1744-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="b1744-115">**Şablonlar \> Yeni şablon**a gidin.</span><span class="sxs-lookup"><span data-stu-id="b1744-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="b1744-116">Yeni şablon adı verin.</span><span class="sxs-lookup"><span data-stu-id="b1744-116">Name the new template.</span></span>
1. <span data-ttu-id="b1744-117">Durum kodu hata yanıtı sayfasında olmasını istediğiniz yapıyı temel alarak şablonu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b1744-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="b1744-118">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="b1744-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="b1744-119">Durum kodu oluştur hata yanıt sayfası</span><span class="sxs-lookup"><span data-stu-id="b1744-119">Build the status code error response page</span></span>

<span data-ttu-id="b1744-120">Durum kodu hata yanıtı sayfası oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b1744-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="b1744-121">**Sayfalar \> Yeni Sayfa**ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b1744-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="b1744-122">Durum kodu hata yanıtı sayfasını adlandırın, ancak **URL** alanını **ayarlamayın**.</span><span class="sxs-lookup"><span data-stu-id="b1744-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="b1744-123">Sayfayı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b1744-123">Build the page.</span></span>
1. <span data-ttu-id="b1744-124">Sayfayı giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="b1744-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="b1744-125">4xx ve 5xx durum kodu hataları için ayrı durum kodu hatası yanıtı sayfaları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1744-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="b1744-126">Alternatif olarak, her iki hata kategorisi için de aynı genel durum kodu hata yanıtı sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1744-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="b1744-127">Durum kodu hatası için yeniden yönlendirme ayarlayın hata yanıtı sayfası</span><span class="sxs-lookup"><span data-stu-id="b1744-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="b1744-128">Durum kodu hata yanıtı sayfasına yeniden yönlendirme ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b1744-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="b1744-129">**URL'ler \> Yeni \> Yeni Diğer Ad**a gidin ve daha önce oluşturduğunuz durum kodu hata yanıtı sayfasını seçin.</span><span class="sxs-lookup"><span data-stu-id="b1744-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="b1744-130">**Diğer ad** alanına, yeniden yönlendirme ayarlamakta olduğunuz durum kodu hata yanıtı sayfasına bağlı olarak **varsayılan-4xx** veya **varsayılan-5xx** değerini girin.</span><span class="sxs-lookup"><span data-stu-id="b1744-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="b1744-131">Bu diğer adlar yayımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b1744-131">These aliases must be published.</span></span> <span data-ttu-id="b1744-132">Aksi durumda yeniden yönlendirme çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1744-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="b1744-133">Bağlantıyı onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="b1744-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="b1744-134">Her iki hata kategorisi için de tek bir durum kodu hata yanıtı sayfası kullanıyorsanız, diğer hata kategorisine ait diğer adı aynı sayfaya bağlamak için bu yordamı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="b1744-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1744-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b1744-135">Additional resources</span></span>

[<span data-ttu-id="b1744-136">Şablonlarla çalışma</span><span class="sxs-lookup"><span data-stu-id="b1744-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="b1744-137">Yeni site sayfası ekleme</span><span class="sxs-lookup"><span data-stu-id="b1744-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b1744-138">URL sayfası oluşturma</span><span class="sxs-lookup"><span data-stu-id="b1744-138">Create a page URL</span></span>](create-page-url.md)
