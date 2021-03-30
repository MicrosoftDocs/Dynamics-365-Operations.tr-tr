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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 57c8876f1faf08ce965ccd796551996a8651e2eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213950"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="13ba7-103">Tanımlama bilgisi izin modülü</span><span class="sxs-lookup"><span data-stu-id="13ba7-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="13ba7-104">Bu konu tanımlama bilgisi izin modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="13ba7-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="13ba7-105">Tanımlama bilgisi izin modülü, site kullanıcılarının, tarayıcı tanımlama bilgilerini izleyen herhangi bir özellik veya modülle ilgili tanımlama bilgilerine izin vermek için açıkça onay sağlamasını ister.</span><span class="sxs-lookup"><span data-stu-id="13ba7-105">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="13ba7-106">Bir site kullanıcısı yeni bir tarayıcı oturumunda siteye ilk kez göz attığında izin gereklidir.</span><span class="sxs-lookup"><span data-stu-id="13ba7-106">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="13ba7-107">İzin alındığında, izlenir ve site kullanıcısına yeniden izin sorulmaz.</span><span class="sxs-lookup"><span data-stu-id="13ba7-107">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="13ba7-108">Daha fazla bilgi için bkz. [Tanımlama bilgisi uyumluluğu](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="13ba7-108">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="13ba7-109">Site kullanıcısından tanımlama bilgisi izni alınmazsa, tanımlama bilgisi izni gerektiren tüm özellikler veya modüller sayfada işlenmez.</span><span class="sxs-lookup"><span data-stu-id="13ba7-109">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="13ba7-110">Örneğin, ödeme modülü, sosyal içerik paylaşım modülü ve tercih edilen mağaza özelliklerinin hepsi tanımlama bilgisi izni gerektirir ve site kullanıcısının izni alınmazsa işlenmez.</span><span class="sxs-lookup"><span data-stu-id="13ba7-110">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="13ba7-111">Bir tanımlama bilgisi izin modülü, sayfa yüklenirken uygulanabilmesi için bir sayfanın başlık bölümünden yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="13ba7-111">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="13ba7-112">Tanımlama bilgisi izin modülü, site kullanıcısına sitedeki tanımlama bilgisi kullanımına ilişkin bilgi veren açık bir iletiye sahip olmalıdır ve sitenin gizlilik sayfasına bir bağlantı sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="13ba7-112">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="13ba7-113">Aşağıdaki resimde, site sayfası üstbilgisinde görüntülenen sitenin gizlilik ilkesi sayfasına verilen bir bağlantı bulunan tanımlama bilgisi izin iletisi örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="13ba7-113">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="13ba7-114">![Tanımlama bilgisi izin modülü örneği](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="13ba7-114">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="13ba7-115">Tanımlama bilgisi izin modülünün özellikleri</span><span class="sxs-lookup"><span data-stu-id="13ba7-115">Cookie consent module properties</span></span>

| <span data-ttu-id="13ba7-116">Özellik adı</span><span class="sxs-lookup"><span data-stu-id="13ba7-116">Property name</span></span>             | <span data-ttu-id="13ba7-117">Değer</span><span class="sxs-lookup"><span data-stu-id="13ba7-117">Value</span></span>                 | <span data-ttu-id="13ba7-118">Tanım</span><span class="sxs-lookup"><span data-stu-id="13ba7-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="13ba7-119">Zengin Metin</span><span class="sxs-lookup"><span data-stu-id="13ba7-119">Rich Text</span></span>                  | <span data-ttu-id="13ba7-120">Zengin Metin</span><span class="sxs-lookup"><span data-stu-id="13ba7-120">Rich Text</span></span> | <span data-ttu-id="13ba7-121">Site kullanıcılarına sitenin tarayıcı tanımlama bilgileri kullandığı ve kullanıcıların tüm işlevlere erişmesi için tanımlama bilgisi kullanımını kabul etmelerini gerektiren zengin metin bildirimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="13ba7-121">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="13ba7-122">Bağlantılar</span><span class="sxs-lookup"><span data-stu-id="13ba7-122">Links</span></span> | <span data-ttu-id="13ba7-123">URL</span><span class="sxs-lookup"><span data-stu-id="13ba7-123">URL</span></span> | <span data-ttu-id="13ba7-124">Sitenin gizlilik sayfasına, sitede izlenen tanımlama bilgilerinin türlerini açıklayan bir veya daha fazla bağlantı eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="13ba7-124">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="13ba7-125">Site sayfalarına tanımlama bilgisi izin modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="13ba7-125">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="13ba7-126">Birden çok site sayfasına bir tanımlama bilgisi izin modülünü etkili şekilde eklemek için, paylaşılan sayfa üstbilgi parçasına eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="13ba7-126">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="13ba7-127">Üstbilgi parçası tüm site sayfalarına eklendikten sonra, bir site kullanıcısı herhangi bir site sayfasına ilk kez gittiğinde otomatik olarak bir tanımlama bilgisi izin bildirimi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="13ba7-127">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="13ba7-128">Üstbilgi parçaları ve modüller hakkında daha fazla bilgi için bkz. [Üstbilgi modülleri](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="13ba7-128">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13ba7-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="13ba7-129">Additional resources</span></span>

[<span data-ttu-id="13ba7-130">Modül kitaplığına genel bakış</span><span class="sxs-lookup"><span data-stu-id="13ba7-130">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="13ba7-131">Üst bilgi modülü</span><span class="sxs-lookup"><span data-stu-id="13ba7-131">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="13ba7-132">Tanımlama bilgisi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="13ba7-132">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]