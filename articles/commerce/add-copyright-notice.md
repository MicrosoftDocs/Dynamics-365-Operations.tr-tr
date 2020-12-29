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
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 838047cac694c65047332e146a7c43ee2ae0f401
ms.sourcegitcommit: 1a12b42cc17f004a981c716aed3da6cf538475a5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4416553"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="94fb7-103">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="94fb7-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94fb7-104">Bu konuda, e-ticaret Web sitenize telif hakkı bildirimi ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="94fb7-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="94fb7-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="94fb7-105">Prerequisites</span></span>

<span data-ttu-id="94fb7-106">Sitenize telif hakkı bildirimi ekleyebilmeniz için, aşağıdaki öğelere sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="94fb7-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="94fb7-107">Paylaşılan altbilgi parçası içeren bir şablon.</span><span class="sxs-lookup"><span data-stu-id="94fb7-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="94fb7-108">Bu şablonu kullanan sayfa.</span><span class="sxs-lookup"><span data-stu-id="94fb7-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="94fb7-109">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="94fb7-109">Add a copyright notice</span></span>

<span data-ttu-id="94fb7-110">Belirli bir şablonu kullanan her sayfanın altına telif hakkı bildirimi eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="94fb7-111">**Parçalar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-111">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="94fb7-112">**Yeni parça** iletişim kutusunda, **Alt bilgi** modülünü seçin ve parçayı adlandırın.</span><span class="sxs-lookup"><span data-stu-id="94fb7-112">In the **New fragment** dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="94fb7-113">Örneğin, **alt bilgi telif hakkı** girin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="94fb7-114">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-114">Select **OK**.</span></span>
1. <span data-ttu-id="94fb7-115">Gezinti bölmesinde, **Altbilgi** yanındaki üç nokta düğmesini (**...**) ve sonra da **Modül ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="94fb7-116">İletişim kutusunda **altbilgi kategorisi**'ni seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="94fb7-117">Gezinti bölmesinde, **Altbilgi kategorisi** yanındaki üç nokta düğmesini ve sonra da **Modül ekle** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="94fb7-118">İletişim kutusunda **Metin bloku**'nu seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="94fb7-119">Gezinti bölmesinde **Metin bloku** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="94fb7-120">Sağdaki Özellikler bölmesinde, **paragraf** alanına, telif hakkı iletinizi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="94fb7-121">Örneğin **(C) Fabrikam 2019** girin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="94fb7-122">**Kaydet**'i seçin, **Düzenlemeyi bitir**'i seçin ve sonra **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="94fb7-123">**Şablonlar**'a gidin, şablonu seçin ve sonra **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="94fb7-124">**Sayfa anahattı** altında, **gövde**'yi ve sonra **varsayılan sayfa**'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="94fb7-125">**Altbilgi yuvası**'nın yanındaki üç nokta düğmesini seçin ve **parçaEkle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="94fb7-126">Daha önce oluşturduğunuz parçayı seçin ve sonra **Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="94fb7-127">Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="94fb7-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="94fb7-128">Telif hakkı bildirimini içeren altbilgi, seçili şablonu kullanan tüm sayfaların altında otomatik olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="94fb7-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94fb7-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="94fb7-129">Additional resources</span></span>

[<span data-ttu-id="94fb7-130">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="94fb7-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="94fb7-131">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="94fb7-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="94fb7-132">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="94fb7-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="94fb7-133">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="94fb7-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="94fb7-134">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="94fb7-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="94fb7-135">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="94fb7-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="94fb7-136">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="94fb7-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

