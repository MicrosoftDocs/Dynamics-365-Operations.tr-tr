---
title: Tanımlama bilgisi izin modülü
description: Bu konu tanımlama bilgisi izin modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817294"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="528d9-103">Tanımlama bilgisi izin modülü</span><span class="sxs-lookup"><span data-stu-id="528d9-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="528d9-104">Bu konu tanımlama bilgisi izin modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="528d9-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="528d9-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="528d9-105">Overview</span></span>

<span data-ttu-id="528d9-106">Tanımlama bilgisi izin modülü, site kullanıcılarının, tarayıcı tanımlama bilgilerini izleyen herhangi bir özellik veya modülle ilgili tanımlama bilgilerine izin vermek için açıkça onay sağlamasını ister.</span><span class="sxs-lookup"><span data-stu-id="528d9-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="528d9-107">Bir site kullanıcısı yeni bir tarayıcı oturumunda siteye ilk kez göz attığında izin gereklidir.</span><span class="sxs-lookup"><span data-stu-id="528d9-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="528d9-108">İzin alındığında, izlenir ve site kullanıcısına yeniden izin sorulmaz.</span><span class="sxs-lookup"><span data-stu-id="528d9-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="528d9-109">Daha fazla bilgi için bkz. [Tanımlama bilgisi uyumluluğu](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="528d9-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="528d9-110">Site kullanıcısından tanımlama bilgisi izni alınmazsa, tanımlama bilgisi izni gerektiren tüm özellikler veya modüller sayfada işlenmez.</span><span class="sxs-lookup"><span data-stu-id="528d9-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="528d9-111">Örneğin, ödeme modülü, sosyal içerik paylaşım modülü ve tercih edilen mağaza özelliklerinin hepsi tanımlama bilgisi izni gerektirir ve site kullanıcısının izni alınmazsa işlenmez.</span><span class="sxs-lookup"><span data-stu-id="528d9-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="528d9-112">Bir tanımlama bilgisi izin modülü, sayfa yüklenirken uygulanabilmesi için bir sayfanın başlık bölümünden yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="528d9-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="528d9-113">Tanımlama bilgisi izin modülü, site kullanıcısına sitedeki tanımlama bilgisi kullanımına ilişkin bilgi veren açık bir iletiye sahip olmalıdır ve sitenin gizlilik sayfasına bir bağlantı sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="528d9-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="528d9-114">Aşağıdaki resimde, site sayfası üstbilgisinde görüntülenen sitenin gizlilik ilkesi sayfasına verilen bir bağlantı bulunan tanımlama bilgisi izin iletisi örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="528d9-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="528d9-115">![Tanımlama bilgisi izin modülü örneği](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="528d9-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="528d9-116">Tanımlama bilgisi izin modülünün özellikleri</span><span class="sxs-lookup"><span data-stu-id="528d9-116">Cookie consent module properties</span></span>

| <span data-ttu-id="528d9-117">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="528d9-117">Property name</span></span>             | <span data-ttu-id="528d9-118">Değer</span><span class="sxs-lookup"><span data-stu-id="528d9-118">Value</span></span>                 | <span data-ttu-id="528d9-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="528d9-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="528d9-120">Zengin Metin</span><span class="sxs-lookup"><span data-stu-id="528d9-120">Rich Text</span></span>                  | <span data-ttu-id="528d9-121">Zengin Metin</span><span class="sxs-lookup"><span data-stu-id="528d9-121">Rich Text</span></span> | <span data-ttu-id="528d9-122">Site kullanıcılarına sitenin tarayıcı tanımlama bilgileri kullandığı ve kullanıcıların tüm işlevlere erişmesi için tanımlama bilgisi kullanımını kabul etmelerini gerektiren zengin metin bildirimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="528d9-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="528d9-123">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="528d9-123">Links</span></span> | <span data-ttu-id="528d9-124">URL</span><span class="sxs-lookup"><span data-stu-id="528d9-124">URL</span></span> | <span data-ttu-id="528d9-125">Sitenin gizlilik sayfasına, sitede izlenen tanımlama bilgilerinin türlerini açıklayan bir veya daha fazla bağlantı eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="528d9-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="528d9-126">Site sayfalarına tanımlama bilgisi izin modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="528d9-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="528d9-127">Birden çok site sayfasına bir tanımlama bilgisi izin modülünü etkili şekilde eklemek için, paylaşılan sayfa üstbilgi parçasına eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="528d9-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="528d9-128">Üstbilgi parçası tüm site sayfalarına eklendikten sonra, bir site kullanıcısı herhangi bir site sayfasına ilk kez gittiğinde otomatik olarak bir tanımlama bilgisi izin bildirimi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="528d9-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="528d9-129">Üstbilgi parçaları ve modüller hakkında daha fazla bilgi için bkz. [Üstbilgi modülleri](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="528d9-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="528d9-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="528d9-130">Additional resources</span></span>

[<span data-ttu-id="528d9-131">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="528d9-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="528d9-132">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="528d9-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="528d9-133">Tanımlama bilgisi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="528d9-133">Cookie compliance</span></span>](cookie-compliance.md)
