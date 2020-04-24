---
title: Hediye kartı modülü
description: Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261595"
---
# <a name="gift-card-module"></a><span data-ttu-id="673f1-103">Hediye kartı modülü</span><span class="sxs-lookup"><span data-stu-id="673f1-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="673f1-104">Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="673f1-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="673f1-105">Özet</span><span class="sxs-lookup"><span data-stu-id="673f1-105">Overview</span></span>

<span data-ttu-id="673f1-106">Hediye kartları, genel bir ödeme biçimidir ve hediye kartı kabul etmek üzere ödeme modülünde bir hediye kartı modülü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="673f1-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="673f1-107">Hediye kartı modülü Dynamics 365, SVS ve Givex hediye kartlarını destekler.</span><span class="sxs-lookup"><span data-stu-id="673f1-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="673f1-108">SVS ve Givex hediye kartları, Adyen ödeme sağlayıcısı aracılığıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="673f1-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="673f1-109">SVS ve Givex gibi harici hediye kartları desteği hakkında daha fazla bilgi için bkz. [Harici hediye kartları için destek](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="673f1-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

## <a name="module-properties"></a><span data-ttu-id="673f1-110">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="673f1-110">Module properties</span></span>

- <span data-ttu-id="673f1-111">**Ek alanları göster** - Bu özellik, her zaman varsayılan olarak görüntülenen hediye kartı numarasına ek olarak, hediye kartları için hangi alanların görüntüleneceğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="673f1-111">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="673f1-112">Örneğin, bazı hediye kartları bir kişisel kimlik numarası (PIN) görüntülemeyi ve başka hediye kartları PIN ve son kullanma tarihini görüntülemeyi destekler.</span><span class="sxs-lookup"><span data-stu-id="673f1-112">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="673f1-113">Alternatif olarak, bu özellik yalnızca hediye kartı numarasını görüntüleyebilen ve ek alanlar içermeyen "Hiçbiri" seçeneğine ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="673f1-113">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="673f1-114">Desteklenen değerler:</span><span class="sxs-lookup"><span data-stu-id="673f1-114">Supported values:</span></span>
-   <span data-ttu-id="673f1-115">PIN</span><span class="sxs-lookup"><span data-stu-id="673f1-115">PIN</span></span>
-   <span data-ttu-id="673f1-116">Son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="673f1-116">Expiration date</span></span>
-   <span data-ttu-id="673f1-117">PIN ve son kullanma tarihi</span><span class="sxs-lookup"><span data-stu-id="673f1-117">PIN and expiration date</span></span> 
-   <span data-ttu-id="673f1-118">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="673f1-118">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="673f1-119">Hediye kartı modülleri için site ayarları</span><span class="sxs-lookup"><span data-stu-id="673f1-119">Site settings for gift card modules</span></span>

<span data-ttu-id="673f1-120">Commerce site oluşturucuda **Site Ayarları \> Uzantılar**altında, **Desteklenen hediye kartı türü** adında bir hediye kartı modülü ayarı vardır.</span><span class="sxs-lookup"><span data-stu-id="673f1-120">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="673f1-121">Bu ayar üç değeri destekler:</span><span class="sxs-lookup"><span data-stu-id="673f1-121">This setting supports three values:</span></span>
- <span data-ttu-id="673f1-122">**Dynamics 365 hediye kartı** - Bu ayar uygulandığında, hediye kartı modülü yalnızca Dynamics 365 hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="673f1-122">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="673f1-123">Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="673f1-123">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="673f1-124">**SVS ve Givex hediye kartları** - Bu ayar uygulandığında, hediye kartı modülü yalnızca Givex ve SVS hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="673f1-124">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="673f1-125">Bu ayar e-Ticaret sitesindeki oturum açmış ve anonim kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="673f1-125">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="673f1-126">**Dynamics 365, SVS ve Givex hediye kartları** - Bu ayar uygulandığında, hediye kartı modülü Dynamics 365, Givex ve SVS hediye kartlarının kullanılmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="673f1-126">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="673f1-127">Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="673f1-127">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="673f1-128">Sayfaya hediye kartı modülü ekleme</span><span class="sxs-lookup"><span data-stu-id="673f1-128">Add a gift card module to a page</span></span>

<span data-ttu-id="673f1-129">Bir ödeme sayfasına hediye kartı modülü ekleme ve gerekli özellikleri ayarlama yönergeleri için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="673f1-129">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="673f1-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="673f1-130">Additional resources</span></span>

[<span data-ttu-id="673f1-131">Başlangıç paketine genel bakış</span><span class="sxs-lookup"><span data-stu-id="673f1-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="673f1-132">Ödeme modülü</span><span class="sxs-lookup"><span data-stu-id="673f1-132">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="673f1-133">Harici hediye kartları için destek</span><span class="sxs-lookup"><span data-stu-id="673f1-133">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
