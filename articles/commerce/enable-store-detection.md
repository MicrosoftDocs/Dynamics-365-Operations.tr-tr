---
title: Konum tabanlı mağaza algılamayı etkinleştirme
description: Bu konuda, Dynamics 365 Commerce siteniz için yerleşim tabanlı depo algılamanın nasıl açılacağı açıklanmaktadır.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: c5fb59a9798e2cddfb75b71235ee7754e54b0e28
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945795"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="2605d-103">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2605d-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2605d-104">Bu konuda, Dynamics 365 Commerce siteniz için yerleşim tabanlı depo algılamanın nasıl açılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="2605d-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="2605d-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="2605d-105">Overview</span></span>

<span data-ttu-id="2605d-106">Ticaretin yerleşim tabanlı mağaza algılaması, müşterilere, konumlarına göre ilgili site içeriği sağlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="2605d-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="2605d-107">Konum tabanlı mağaza algılaması açık olduğunda, Ticaret sağlama servisi müşteriyi, kullanılabilen en iyi coğrafi site konfigürasyonuna yönlendirmek için müşterinin web tarayıcısının IP adresinden ülke/bölge bilgilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2605d-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="2605d-108">Gizlilik bildirimi</span><span class="sxs-lookup"><span data-stu-id="2605d-108">Privacy notice</span></span>

<span data-ttu-id="2605d-109">Konum temelli depo algılama özelliğini etkinleştirirseniz, müşterinin tarayıcısından alınan bilgiler Microsoft konum hizmetine gönderilir.</span><span class="sxs-lookup"><span data-stu-id="2605d-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="2605d-110">Bu bilgiler daha sonra, konumuyla ilgili müşteri içeriğini sağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2605d-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="2605d-111">Müşteri tarayıcısından gönderilen bilgiler ile müşteriye iade edilen yerleşim tabanlı bilgiler Gizlilik ve tanımlama bilgisi uyumluluk ilkelerine tabidir.</span><span class="sxs-lookup"><span data-stu-id="2605d-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="2605d-112">Konum tabanlı mağaza algılamayı açma</span><span class="sxs-lookup"><span data-stu-id="2605d-112">Turn on location-based store detection</span></span>

<span data-ttu-id="2605d-113">Ticari olarak konum tabanlı mağaza algılamasını etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2605d-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2605d-114">Düzenleme aracında sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="2605d-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="2605d-115">Soldaki gezinti bölmesinde **Site Yönetimi** seçin.</span><span class="sxs-lookup"><span data-stu-id="2605d-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="2605d-116">**Site ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="2605d-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="2605d-117">**Konum tabanlı mağaza algılamasını etkinleştir** seçeneğini **açık** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2605d-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2605d-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2605d-118">Additional resources</span></span>

[<span data-ttu-id="2605d-119">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2605d-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="2605d-120">Yeni e-Ticaret sitesini dağıtma</span><span class="sxs-lookup"><span data-stu-id="2605d-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="2605d-121">e-Ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2605d-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="2605d-122">Çevrimiçi siteyi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="2605d-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="2605d-123">Robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="2605d-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="2605d-124">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="2605d-124">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="2605d-125">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="2605d-125">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
