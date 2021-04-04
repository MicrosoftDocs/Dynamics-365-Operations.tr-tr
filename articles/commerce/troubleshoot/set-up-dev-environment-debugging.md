---
title: Katman 1 Retail Server sanal makinede hata ayıklama için e-ticaret geliştirme ortamı ayarlama
description: Bu konuda Katman 1 Retail Server sanal makinede (VM) hata ayıklama için e-ticaret geliştirme ortamının nasıl ayarlandığı açıklanmaktadır.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35380a559a4f1b22bdf04ff25cb2bbfc51aff45b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585564"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="f6456-103">Katman 1 Retail Server sanal makinede hata ayıklama için e-ticaret geliştirme ortamı ayarlama</span><span class="sxs-lookup"><span data-stu-id="f6456-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6456-104">Bu konuda Katman 1 Retail Server sanal makinede (VM) hata ayıklama için e-ticaret geliştirme ortamının nasıl ayarlandığı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f6456-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="f6456-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6456-105">Description</span></span>

<span data-ttu-id="f6456-106">Microsoft Dynamics 365 Commerce Katman 1 ortamları normal olarak Commerce Runtime (CRT) ve satış noktası (POS) uzantısı için dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="f6456-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="f6456-107">Bunlar bağımsız ortamlardır.</span><span class="sxs-lookup"><span data-stu-id="f6456-107">They are standalone environments.</span></span> <span data-ttu-id="f6456-108">Mimarinin hizmet olarak yazılım (SaaS) yapısı nedeniyle, bunlar e-ticaret bileşenleri içermez.</span><span class="sxs-lookup"><span data-stu-id="f6456-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="f6456-109">Bazı senaryolarda, bir katman 1 ortamındaki uzantılara yapılan çağrıları test etmek isteyebilirsiniz, böylece e-ticaret bileşenlerinden gelen uzantılar için hata ayıklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6456-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="f6456-110">Genel yönergeler için bkz. [Katman 1 Commerce geliştirme ortamında hata ayıklama](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="f6456-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="f6456-111">Bir katman 1 ortamına karşı hata ayıklarken, site şimdi farklı bir Retail Server aradığı için, çapraz sunucu çağrıları içerik güvenlik ilkesiyle ilişkili çeşitli hatalara neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="f6456-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="f6456-112">Aşağıdaki resimde, ürün ayrıntıları sayfasında bir varyant seçildiğinde oluşabilecek bir hata örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f6456-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Ürün Ayrıntıları sayfasında bir varyant seçildiğinde oluşan hata](media/unhandled-rejection-error.jpg)

<span data-ttu-id="f6456-114">Aşağıdaki çizimde, tarayıcının hata ayıklama araçlarında (F12 geliştirici araçları) benzer bir hatanın örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f6456-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="f6456-115">Hata iletisi, içerik güvenlik ilkesi yönergesinin ihlalinden bahseder.</span><span class="sxs-lookup"><span data-stu-id="f6456-115">The error message mentions violation of the content security policy directive.</span></span>

![Hata ayıklayıcı araçları hatası](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="f6456-117">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="f6456-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="f6456-118">Commerce site oluşturucuda sitenin içerik güvenliği ilkesini devre dışı bırakın</span><span class="sxs-lookup"><span data-stu-id="f6456-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="f6456-119">Üzerinde çalıştığınız siteyi seçin.</span><span class="sxs-lookup"><span data-stu-id="f6456-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="f6456-120">**Ayarlar**'ı ve daha sonra **Uzantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6456-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="f6456-121">**İçerik güvenlik ilkesi** sekmesinde **içerik güvenlik ilkesini devre dışı bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6456-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="f6456-122">**Kaydet ve yayınla** yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6456-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="f6456-123">İşletme-tüketici (B2C) oturumu açma, yerel bir geliştirme ortamında çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6456-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="f6456-124">Ancak, kullanıcı olarak oturum açmak gerektiğinde konuk olarak ödeme yapmayı kullanabilir veya sahte sayfa oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6456-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6456-125">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f6456-125">Additional resources</span></span>

[<span data-ttu-id="f6456-126">E-ticaret çevrimiçi genişletilebilirlik geliştirmesini kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="f6456-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="f6456-127">E-ticaret sitesinde içerik güvenlik ilkesini (CSP) Yönetme</span><span class="sxs-lookup"><span data-stu-id="f6456-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
