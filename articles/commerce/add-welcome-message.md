---
title: Hoş geldiniz iletisi ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce web sitenize bir hoş geldin mesajının nasıl ekleneceği açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5910ab85b1b0b2df992a24ad3cf7a032e7b98ea9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980144"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="99563-103">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="99563-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="99563-104">Bu konuda, Microsoft Dynamics 365 Commerce web sitenize bir hoş geldin mesajının nasıl ekleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="99563-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="99563-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="99563-105">Overview</span></span>

<span data-ttu-id="99563-106">E-ticaret web sitenizdeki bir hoş geldiniz iletisi, ziyaretçileri sürekli satışlar, site güncelleştirmeleri veya mevsimlik koleksiyonların kullanılabilirliğiyle ilgili olarak bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="99563-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="99563-107">Hoş geldiniz iletisi uyarı modülü kullanılarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="99563-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="99563-108">Uyarı modülü, üstbilgi parçasının **hata/bilgi iletileri** yuvasına eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="99563-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="99563-109">Uyarı modülü, gösterilen metni, metin rengini ve hizalamayı belirtmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="99563-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="99563-110">Ayrıca, sitenin bu iletiyi kapatabileceği konusunda da belirtme olanağı tanır.</span><span class="sxs-lookup"><span data-stu-id="99563-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="99563-111">Paylaşılan başlık parçasına bir hoş geldiniz iletisi eklendiğinde, bu paylaşılan başlık parçasının kullanıldığı şablonu kullanan her sayfada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="99563-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="99563-112">Sitenize hoş geldin mesajı eklemek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="99563-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="99563-113">Commerce site oluşturucuda sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="99563-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="99563-114">**Parçalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="99563-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="99563-115">İletinin ekleneceği başlık parçasını seçin.</span><span class="sxs-lookup"><span data-stu-id="99563-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="99563-116">Anahat ağacında, **hata/bilgi iletilerini** genişletin.</span><span class="sxs-lookup"><span data-stu-id="99563-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="99563-117">Uyarı modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="99563-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="99563-118">Uyarı modülü henüz yoksa, önce üç nokta düğmesini (**...**) **Hata/bilgi iletilerinin** yanında, **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="99563-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="99563-119">Sağdaki Özellik bölmesinde, **veri** sekmesinde, **veri kaynağı Ekle**'yi seçin ve sonra **içeriği** seçin.</span><span class="sxs-lookup"><span data-stu-id="99563-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="99563-120">**Giriş metni** alanına hoş geldiniz iletisinin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="99563-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="99563-121">**Kaydet**'i seçin, başlık parçasını iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="99563-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="99563-122">Hoş geldiniz iletisi şimdi, seçili başlık parçasını kullanan her site sayfasının üst kısmında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="99563-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99563-123">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="99563-123">Additional resources</span></span>

[<span data-ttu-id="99563-124">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="99563-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="99563-125">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="99563-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="99563-126">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="99563-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="99563-127">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="99563-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="99563-128">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="99563-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="99563-129">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="99563-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="99563-130">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="99563-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

