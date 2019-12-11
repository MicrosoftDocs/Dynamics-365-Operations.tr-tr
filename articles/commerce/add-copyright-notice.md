---
title: Telif hakkı bildirimi ekleme
description: Bu konuda, e-ticaret Web sitenize telif hakkı bildirimi ekleme yöntemi açıklanmıştır.
author: psimolin
manager: AnnBe
ms.date: 10/31/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39135a2eca25336097ee9eddf06dc6709c102571
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696957"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="ea8a0-103">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="ea8a0-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ea8a0-104">Bu konuda, e-ticaret Web sitenize telif hakkı bildirimi ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ea8a0-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="ea8a0-105">Prerequisites</span></span>

<span data-ttu-id="ea8a0-106">Sitenize telif hakkı bildirimi ekleyebilmeniz için, aşağıdaki öğelere sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="ea8a0-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="ea8a0-107">Paylaşılan altbilgi parçası içeren bir şablon.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="ea8a0-108">Bu şablonu kullanan sayfa.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="ea8a0-109">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="ea8a0-109">Add a copyright notice</span></span>

<span data-ttu-id="ea8a0-110">Belirli bir şablonu kullanan her sayfanın altına telif hakkı bildirimi eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="ea8a0-111">**Parçalara** gidin ve **yeni sayfa parçası**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="ea8a0-112">İletişim kutusunda, **altbilgi** modülünü seçin ve parçayı adlandırın.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="ea8a0-113">Örneğin, **alt bilgi telif hakkı** girin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="ea8a0-114">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-114">Select **OK**.</span></span>
1. <span data-ttu-id="ea8a0-115">Gezinti bölmesinde, **Altbilgi** yanındaki üç nokta düğmesini (**...**) ve sonra da **Modül ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ea8a0-116">İletişim kutusunda **altbilgi kategorisi**'ni seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="ea8a0-117">Gezinti bölmesinde, **Altbilgi kategorisi** yanındaki üç nokta düğmesini ve sonra da **Modül ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ea8a0-118">İletişim kutusunda **İçerik zengin blok öğesi**'ni seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="ea8a0-119">Gezinti bölmesinde, **içerik zengin blok öğesini** seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="ea8a0-120">Sağdaki Özellikler bölmesinde, **paragraf** alanına, telif hakkı iletinizi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="ea8a0-121">Örneğin **(C) Fabrikam 2019** girin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="ea8a0-122">**Kaydet**'i seçin, **Giriş**'i seçin ve sonra **yayınla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="ea8a0-123">**Şablonlara** gidin, şablonu seçin ve sonra **Çıkış**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="ea8a0-124">**Sayfa anahattı** altında, **gövde**'yi ve sonra **varsayılan sayfa**'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="ea8a0-125">**Altbilgi yuvası**'nın yanındaki üç nokta düğmesini seçin ve **parçaEkle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="ea8a0-126">Daha önce oluşturduğunuz parçayı seçin ve sonra **Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="ea8a0-127">Şablonu giriş yapın ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="ea8a0-128">Telif hakkı bildirimini içeren altbilgi, seçili şablonu kullanan tüm sayfaların altında otomatik olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ea8a0-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea8a0-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ea8a0-129">Additional resources</span></span>

[<span data-ttu-id="ea8a0-130">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="ea8a0-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="ea8a0-131">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="ea8a0-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="ea8a0-132">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="ea8a0-132">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="ea8a0-133">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="ea8a0-133">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="ea8a0-134">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="ea8a0-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="ea8a0-135">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="ea8a0-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

