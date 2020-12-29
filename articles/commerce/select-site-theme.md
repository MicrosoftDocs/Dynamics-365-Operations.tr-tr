---
title: Site teması seçme
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta sitenizin temasını nasıl ayarlayabileceğiniz veya değiştirileceği açıklanmaktadır.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: c54a3e9471fdeb56f27fe7c567c7cd7f0b7fd218
ms.sourcegitcommit: 2ef23dcd4e42362186b9951e675010d97d55c6bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4556441"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="fe7b9-103">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="fe7b9-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe7b9-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta sitenizin temasını nasıl ayarlayabileceğiniz veya değiştirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fe7b9-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="fe7b9-105">Overview</span></span>

<span data-ttu-id="fe7b9-106">Sitenin yerleşimi ve stili (örneğin, yazı tipleri, boyutlar ve renkler) seçtiğiniz ve siteye uyguladığınız Tema tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="fe7b9-107">Bir tema, şirketinizdeki bir geliştirici tarafından oluşturulur ve dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="fe7b9-108">Temalara genel bakış için, bkz [Temalara genel bakış](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="fe7b9-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="fe7b9-109">Kural oluşturmayla ve temaları dağıtmayla ilgili daha fazla bilgi için bkz. [Yeni tema oluşturma](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="fe7b9-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="fe7b9-110">Varsayılan olarak, bir siteyi ilk oluşturduğunuzda **Fabrikam** adlı bir tema kullanılır.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="fe7b9-111">Bu varsayılan tema, Commerce modül kitaplığının bir parçası olarak sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="fe7b9-112">Siteniz için ek temalar dağıttıktan sonra, siteyi, bunun yerine bunlardan birini kullanacak şekilde konfigüre edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="fe7b9-113">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="fe7b9-113">Select the site theme</span></span>

<span data-ttu-id="fe7b9-114">Sitenize uygulanacak temayı seçmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="fe7b9-115">Site düzenleme ortamında sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="fe7b9-116">**Site yönetimi** \> **Genişletilebilirliği** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="fe7b9-117">**Tema** altında, açılan menüden bir tema seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="fe7b9-118">Seçili temayı sitenize uygulamak için **Kaydet ve Yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="fe7b9-119">Seçtiğiniz tema,**genişletilebilirlik** sayfasında **Kaydet ve Yayımla**'yı seçtiğiniz anda sitenize yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="fe7b9-120">Siz uygulamadan önce bir temayı sitenizde önizlemek için, geliştirme veya korumalı alan ortamınızı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe7b9-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe7b9-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fe7b9-121">Additional resources</span></span>

[<span data-ttu-id="fe7b9-122">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="fe7b9-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="fe7b9-123">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="fe7b9-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="fe7b9-124">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="fe7b9-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="fe7b9-125">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="fe7b9-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="fe7b9-126">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="fe7b9-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="fe7b9-127">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="fe7b9-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="fe7b9-128">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="fe7b9-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="fe7b9-129">Tema oluşturmaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="fe7b9-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="fe7b9-130">Yeni tema oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe7b9-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)

