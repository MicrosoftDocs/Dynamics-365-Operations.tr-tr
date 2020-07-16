---
title: Konum tabanlı mağaza algılamayı etkinleştirme
description: Bu konuda, Dynamics 365 Commerce siteniz için yerleşim tabanlı depo algılamanın nasıl açılacağı açıklanmaktadır.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4d3a423bf64900e547a23f2e5eeb90aa679ec5d1
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533402"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="a7a57-103">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a7a57-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a7a57-104">Bu konuda, Dynamics 365 Commerce siteniz için yerleşim tabanlı depo algılamanın nasıl açılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a7a57-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="a7a57-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="a7a57-105">Overview</span></span>

<span data-ttu-id="a7a57-106">Ticaretin yerleşim tabanlı mağaza algılaması, müşterilere, konumlarına göre ilgili site içeriği sağlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="a7a57-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="a7a57-107">Konum tabanlı mağaza algılaması açık olduğunda, Ticaret sağlama servisi müşteriyi, kullanılabilen en iyi coğrafi site konfigürasyonuna yönlendirmek için müşterinin web tarayıcısının IP adresinden ülke/bölge bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a7a57-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="a7a57-108">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="a7a57-108">Privacy notice</span></span>

<span data-ttu-id="a7a57-109">Konum temelli depo algılama özelliğini etkinleştirirseniz, müşterinin tarayıcısından alınan bilgiler Microsoft konum hizmetine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="a7a57-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="a7a57-110">Bu bilgiler daha sonra, konumuyla ilgili müşteri içeriğini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7a57-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="a7a57-111">Müşteri tarayıcısından gönderilen bilgiler ile müşteriye iade edilen yerleşim tabanlı bilgiler Gizlilik ve tanımlama bilgisi uyumluluk ilkelerine tabidir.</span><span class="sxs-lookup"><span data-stu-id="a7a57-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="a7a57-112">Konum tabanlı mağaza algılamayı açma</span><span class="sxs-lookup"><span data-stu-id="a7a57-112">Turn on location-based store detection</span></span>

<span data-ttu-id="a7a57-113">Ticari olarak konum tabanlı mağaza algılamasını etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a7a57-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a7a57-114">Düzenleme aracında sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="a7a57-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="a7a57-115">Soldaki gezinti bölmesinde **Site Yönetimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="a7a57-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="a7a57-116">**Site ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7a57-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="a7a57-117">**Konum tabanlı mağaza algılamasını etkinleştir** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a7a57-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7a57-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a7a57-118">Additional resources</span></span>

[<span data-ttu-id="a7a57-119">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a7a57-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a7a57-120">Yeni e-Ticaret sitesini dağıtma</span><span class="sxs-lookup"><span data-stu-id="a7a57-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a7a57-121">e-Ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a7a57-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a7a57-122">Çevrimiçi siteyi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="a7a57-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a7a57-123">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="a7a57-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a7a57-124">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="a7a57-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a7a57-125">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="a7a57-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a7a57-126">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="a7a57-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a7a57-127">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a7a57-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a7a57-128">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="a7a57-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
