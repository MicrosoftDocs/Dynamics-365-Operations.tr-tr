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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3f7e9a3acde508f405ce85f125db552c3ae3656b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000741"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="a129a-103">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a129a-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a129a-104">Bu konuda, Dynamics 365 Commerce siteniz için yerleşim tabanlı depo algılamanın nasıl açılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a129a-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="a129a-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="a129a-105">Overview</span></span>

<span data-ttu-id="a129a-106">Ticaretin yerleşim tabanlı mağaza algılaması, müşterilere, konumlarına göre ilgili site içeriği sağlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="a129a-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="a129a-107">Konum tabanlı mağaza algılaması açık olduğunda, Ticaret sağlama servisi müşteriyi, kullanılabilen en iyi coğrafi site konfigürasyonuna yönlendirmek için müşterinin web tarayıcısının IP adresinden ülke/bölge bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a129a-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="a129a-108">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="a129a-108">Privacy notice</span></span>

<span data-ttu-id="a129a-109">Konum temelli depo algılama özelliğini etkinleştirirseniz, müşterinin tarayıcısından alınan bilgiler Microsoft konum hizmetine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="a129a-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="a129a-110">Bu bilgiler daha sonra, konumuyla ilgili müşteri içeriğini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a129a-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="a129a-111">Müşteri tarayıcısından gönderilen bilgiler ile müşteriye iade edilen yerleşim tabanlı bilgiler Gizlilik ve tanımlama bilgisi uyumluluk ilkelerine tabidir.</span><span class="sxs-lookup"><span data-stu-id="a129a-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="a129a-112">Konum tabanlı mağaza algılamayı açma</span><span class="sxs-lookup"><span data-stu-id="a129a-112">Turn on location-based store detection</span></span>

<span data-ttu-id="a129a-113">Ticari olarak konum tabanlı mağaza algılamasını etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a129a-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a129a-114">Düzenleme aracında sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="a129a-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="a129a-115">Soldaki gezinti bölmesinde **Site Yönetimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="a129a-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="a129a-116">**Site ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a129a-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="a129a-117">**Konum tabanlı mağaza algılamasını etkinleştir** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a129a-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a129a-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a129a-118">Additional resources</span></span>

[<span data-ttu-id="a129a-119">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a129a-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a129a-120">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="a129a-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a129a-121">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a129a-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a129a-122">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="a129a-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a129a-123">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="a129a-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a129a-124">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="a129a-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a129a-125">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="a129a-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a129a-126">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="a129a-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a129a-127">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="a129a-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a129a-128">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="a129a-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
