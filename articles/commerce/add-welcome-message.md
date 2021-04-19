---
title: Hoş geldiniz iletisi ekleme
description: Bu konuda, Microsoft Dynamics 365 Commerce web sitenize bir hoş geldin mesajının nasıl ekleneceği açıklanmaktadır.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797395"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="aeadb-103">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="aeadb-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aeadb-104">Bu konuda, Microsoft Dynamics 365 Commerce web sitenize bir hoş geldin mesajının nasıl ekleneceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="aeadb-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="aeadb-105">E-ticaret web sitenizdeki bir hoş geldiniz iletisi, ziyaretçileri sürekli satışlar, site güncelleştirmeleri veya mevsimlik koleksiyonların kullanılabilirliğiyle ilgili olarak bildirebilir.</span><span class="sxs-lookup"><span data-stu-id="aeadb-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="aeadb-106">Hoş geldiniz iletisi uyarı modülü kullanılarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="aeadb-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="aeadb-107">Uyarı modülü, üstbilgi parçasının **hata/bilgi iletileri** yuvasına eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="aeadb-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="aeadb-108">Uyarı modülü, gösterilen metni, metin rengini ve hizalamayı belirtmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="aeadb-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="aeadb-109">Ayrıca, sitenin bu iletiyi kapatabileceği konusunda da belirtme olanağı tanır.</span><span class="sxs-lookup"><span data-stu-id="aeadb-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="aeadb-110">Paylaşılan başlık parçasına bir hoş geldiniz iletisi eklendiğinde, bu paylaşılan başlık parçasının kullanıldığı şablonu kullanan her sayfada gösterilir.</span><span class="sxs-lookup"><span data-stu-id="aeadb-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="aeadb-111">Sitenize hoş geldin mesajı eklemek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="aeadb-112">Commerce site oluşturucuda sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="aeadb-113">**Parçalar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="aeadb-114">İletinin ekleneceği başlık parçasını seçin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="aeadb-115">Anahat ağacında, **hata/bilgi iletilerini** genişletin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="aeadb-116">Uyarı modülünü seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="aeadb-117">Uyarı modülü henüz yoksa, önce üç nokta düğmesini (**...**) **Hata/bilgi iletilerinin** yanında, **Modül ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="aeadb-118">Sağdaki Özellik bölmesinde, **veri** sekmesinde, **veri kaynağı Ekle**'yi seçin ve sonra **içeriği** seçin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="aeadb-119">**Giriş metni** alanına hoş geldiniz iletisinin metnini girin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="aeadb-120">**Kaydet**'i seçin, başlık parçasını iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="aeadb-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="aeadb-121">Hoş geldiniz iletisi şimdi, seçili başlık parçasını kullanan her site sayfasının üst kısmında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="aeadb-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aeadb-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="aeadb-122">Additional resources</span></span>

[<span data-ttu-id="aeadb-123">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="aeadb-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="aeadb-124">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="aeadb-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="aeadb-125">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="aeadb-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="aeadb-126">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="aeadb-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="aeadb-127">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="aeadb-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="aeadb-128">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="aeadb-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="aeadb-129">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="aeadb-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
