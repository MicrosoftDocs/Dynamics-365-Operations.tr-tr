---
title: Telif hakkı bildirimi ekleme
description: Bu konuda, e-ticaret Web sitenize telif hakkı bildirimi ekleme yöntemi açıklanmıştır.
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
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
ms.openlocfilehash: 2ea04854636fdd0c2b3223bb19d5f06a19836151
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206379"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="237ca-103">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="237ca-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="237ca-104">Bu konuda, e-ticaret Web sitenize telif hakkı bildirimi ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="237ca-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="237ca-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="237ca-105">Prerequisites</span></span>

<span data-ttu-id="237ca-106">Sitenize telif hakkı bildirimi ekleyebilmeniz için, aşağıdaki öğelere sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="237ca-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="237ca-107">Paylaşılan altbilgi parçası içeren bir şablon.</span><span class="sxs-lookup"><span data-stu-id="237ca-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="237ca-108">Bu şablonu kullanan sayfa.</span><span class="sxs-lookup"><span data-stu-id="237ca-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="237ca-109">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="237ca-109">Add a copyright notice</span></span>

<span data-ttu-id="237ca-110">Belirli bir şablonu kullanan her sayfanın altına telif hakkı bildirimi eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="237ca-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="237ca-111">**Parçalar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-111">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="237ca-112">**Yeni parça** iletişim kutusunda, **Alt bilgi** modülünü seçin ve parçayı adlandırın.</span><span class="sxs-lookup"><span data-stu-id="237ca-112">In the **New fragment** dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="237ca-113">Örneğin, **alt bilgi telif hakkı** girin.</span><span class="sxs-lookup"><span data-stu-id="237ca-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="237ca-114">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-114">Select **OK**.</span></span>
1. <span data-ttu-id="237ca-115">Gezinti bölmesinde, **Altbilgi** yanındaki üç nokta düğmesini (**...**) ve sonra da **Modül ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="237ca-116">İletişim kutusunda **altbilgi kategorisi**'ni seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="237ca-117">Gezinti bölmesinde, **Altbilgi kategorisi** yanındaki üç nokta düğmesini ve sonra da **Modül ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="237ca-118">İletişim kutusunda **Metin bloku**'nu seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="237ca-119">Gezinti bölmesinde **Metin bloku** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="237ca-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="237ca-120">Sağdaki Özellikler bölmesinde, **paragraf** alanına, telif hakkı iletinizi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="237ca-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="237ca-121">Örneğin **(C) Fabrikam 2019** girin.</span><span class="sxs-lookup"><span data-stu-id="237ca-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="237ca-122">**Kaydet**'i seçin, **Düzenlemeyi bitir**'i seçin ve sonra **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="237ca-123">**Şablonlar**'a gidin, şablonu seçin ve sonra **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="237ca-124">**Sayfa anahattı** altında, **gövde**'yi ve sonra **varsayılan sayfa**'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="237ca-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="237ca-125">**Altbilgi yuvası**'nın yanındaki üç nokta düğmesini seçin ve **parçaEkle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="237ca-126">Daha önce oluşturduğunuz parçayı seçin ve sonra **Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="237ca-127">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="237ca-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="237ca-128">Telif hakkı bildirimini içeren altbilgi, seçili şablonu kullanan tüm sayfaların altında otomatik olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="237ca-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="237ca-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="237ca-129">Additional resources</span></span>

[<span data-ttu-id="237ca-130">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="237ca-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="237ca-131">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="237ca-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="237ca-132">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="237ca-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="237ca-133">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="237ca-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="237ca-134">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="237ca-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="237ca-135">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="237ca-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="237ca-136">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="237ca-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]