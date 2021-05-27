---
title: Konum tabanlı mağaza algılamayı etkinleştirme
description: Bu konuda, Dynamics 365 Commerce siteniz için yerleşim tabanlı depo algılamanın nasıl açılacağı açıklanmaktadır.
author: brianshook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e26c3130914ebef5a63b79c477d7d5846fd5b71
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027612"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="0c846-103">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0c846-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c846-104">Bu konuda, Dynamics 365 Commerce siteniz için yerleşim tabanlı depo algılamanın nasıl açılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0c846-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="0c846-105">Ticaretin yerleşim tabanlı mağaza algılaması, müşterilere, konumlarına göre ilgili site içeriği sağlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="0c846-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="0c846-106">Konum tabanlı mağaza algılaması açık olduğunda, Ticaret sağlama servisi müşteriyi, kullanılabilen en iyi coğrafi site konfigürasyonuna yönlendirmek için müşterinin web tarayıcısının IP adresinden ülke/bölge bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0c846-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="0c846-107">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="0c846-107">Privacy notice</span></span>

<span data-ttu-id="0c846-108">Konum temelli depo algılama özelliğini etkinleştirirseniz, müşterinin tarayıcısından alınan bilgiler Microsoft konum hizmetine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="0c846-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="0c846-109">Bu bilgiler daha sonra, müşterinin konumuyla ilgili müşteri içeriğini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0c846-109">This information is then used to provide the customer content that is relevant to the customer's location.</span></span> <span data-ttu-id="0c846-110">Müşteri tarayıcısından gönderilen bilgiler ile müşteriye iade edilen yerleşim tabanlı bilgiler Gizlilik ve tanımlama bilgisi uyumluluk ilkelerine tabidir.</span><span class="sxs-lookup"><span data-stu-id="0c846-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="0c846-111">Konum tabanlı mağaza algılamayı açma</span><span class="sxs-lookup"><span data-stu-id="0c846-111">Turn on location-based store detection</span></span>

<span data-ttu-id="0c846-112">Ticari olarak konum tabanlı mağaza algılamasını etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0c846-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0c846-113">Düzenleme aracında sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="0c846-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="0c846-114">Soldaki gezinti bölmesinde **Site Yönetimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="0c846-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="0c846-115">**Site ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0c846-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="0c846-116">**Konum tabanlı mağaza algılamasını etkinleştir** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0c846-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c846-117">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0c846-117">Additional resources</span></span>

[<span data-ttu-id="0c846-118">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0c846-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="0c846-119">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="0c846-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="0c846-120">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c846-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="0c846-121">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="0c846-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="0c846-122">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="0c846-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="0c846-123">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="0c846-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="0c846-124">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="0c846-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="0c846-125">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="0c846-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="0c846-126">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0c846-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="0c846-127">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="0c846-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
