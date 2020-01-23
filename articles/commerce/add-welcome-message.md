---
title: Hoş geldiniz iletisi ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce web sitenize bir hoş geldin mesajının nasıl ekleneceği açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 12/12/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914528"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="193b8-103">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="193b8-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="193b8-104">Bu konuda, Microsoft Dynamics 365 Commerce web sitenize bir hoş geldin mesajının nasıl ekleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="193b8-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="193b8-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="193b8-105">Overview</span></span>

<span data-ttu-id="193b8-106">E-ticaret web sitenizdeki bir hoş geldiniz iletisi, ziyaretçileri sürekli satışlar, site güncelleştirmeleri veya mevsimlik koleksiyonların kullanılabilirliğiyle ilgili olarak bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="193b8-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="193b8-107">Hoş geldiniz iletisi uyarı modülü kullanılarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="193b8-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="193b8-108">Uyarı modülü, üstbilgi parçasının **hata/bilgi iletileri** yuvasına eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="193b8-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="193b8-109">Uyarı modülü, gösterilen metni, metin rengini ve hizalamayı belirtmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="193b8-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="193b8-110">Ayrıca, sitenin bu iletiyi kapatabileceği konusunda da belirtme olanağı tanır.</span><span class="sxs-lookup"><span data-stu-id="193b8-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="193b8-111">Paylaşılan başlık parçasına bir hoş geldiniz iletisi eklendiğinde, bu paylaşılan başlık parçasının kullanıldığı şablonu kullanan her sayfada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="193b8-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="193b8-112">Sitenize hoş geldin mesajı eklemek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="193b8-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="193b8-113">Dynamics 365 Commerce'te sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="193b8-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="193b8-114">**Parçalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="193b8-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="193b8-115">İletinin ekleneceği başlık parçasını seçin.</span><span class="sxs-lookup"><span data-stu-id="193b8-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="193b8-116">Anahat ağacında, **hata/bilgi iletilerini** genişletin.</span><span class="sxs-lookup"><span data-stu-id="193b8-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="193b8-117">Uyarı modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="193b8-117">Select the alert module.</span></span>

    <span data-ttu-id="193b8-118">Uyarı modülü henüz yoksa, üç nokta düğmesini (**...**) **hata/bilgi iletilerinin** yanında, **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="193b8-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="193b8-119">Uyarı modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="193b8-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="193b8-120">Sağdaki Özellik bölmesinde, **veri** sekmesinde, **veri kaynağı Ekle**'yi seçin ve sonra **içeriği** seçin.</span><span class="sxs-lookup"><span data-stu-id="193b8-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="193b8-121">**Giriş metni** alanına hoş geldiniz iletisinin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="193b8-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="193b8-122">Üstbilgi parçasını kaydedin, giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="193b8-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="193b8-123">Hoş geldiniz iletisi şimdi, seçili başlık parçasını kullanan her site sayfasının üst kısmında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="193b8-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="193b8-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="193b8-124">Additional resources</span></span>

[<span data-ttu-id="193b8-125">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="193b8-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="193b8-126">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="193b8-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="193b8-127">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="193b8-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="193b8-128">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="193b8-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="193b8-129">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="193b8-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="193b8-130">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="193b8-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="193b8-131">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="193b8-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

