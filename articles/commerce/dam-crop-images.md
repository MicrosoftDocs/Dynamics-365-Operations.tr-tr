---
title: Görüntüleri kırpma
description: Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda görüntüleri kırpma yöntemi açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9496a1f96e2d0e18eb477a9743927b2076c5548a
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269579"
---
# <a name="crop-images"></a><span data-ttu-id="d8382-103">Görüntüleri kırpma</span><span class="sxs-lookup"><span data-stu-id="d8382-103">Crop images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d8382-104">Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda görüntüleri kırpma yöntemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d8382-104">This topic describes how to crop images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="d8382-105">Özet</span><span class="sxs-lookup"><span data-stu-id="d8382-105">Overview</span></span>

<span data-ttu-id="d8382-106">Commerce site oluşturucusu Ortam Kitaplığı, farklı modül türleri ve görünüm pencereleri için en iyi duruma getirmek amacıyla görüntüleri kırpmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d8382-106">The Commerce site builder Media Library allows you to crop images to optimize them for different module types and viewports.</span></span>

## <a name="crop-an-image"></a><span data-ttu-id="d8382-107">Görüntüyü kırpma</span><span class="sxs-lookup"><span data-stu-id="d8382-107">Crop an image</span></span>

<span data-ttu-id="d8382-108">Site oluşturucuda bir görüntüyü kırpmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d8382-108">To crop an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d8382-109">Commerce site oluşturucunun sol gezinti bölmesinde, **Ortam Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-109">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="d8382-110">Ana pencerede, değiştirmek istediğiniz görüntüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-110">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="d8382-111">Komut çubuğunda, **Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-111">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="d8382-112">**Düzenleme Modu**'na girmek için görüntüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-112">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="d8382-113">**Düzenleme Modu** altında **Görünümü Modüle göre Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-113">Under **Edit Mode**, select **Edit View by Module**.</span></span>
1. <span data-ttu-id="d8382-114">**Modül** açılan menüsünde modül türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-114">From the **Module** drop-down menu, select the module type.</span></span>
1. <span data-ttu-id="d8382-115">**Görünüm türü** açılan menüsünde görünüm türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-115">From the **View type** drop-down menu, select the view type.</span></span>
1. <span data-ttu-id="d8382-116">**Yerleşim** açılır menüsünden görüntü yerleşimini seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-116">From the **Placement** drop-down menu, select the image placement.</span></span>
1. <span data-ttu-id="d8382-117">**Görünüm penceresi** açılan menüsünde görünüm penceresi boyutunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-117">From the **Viewport** drop-down menu, select the viewport size.</span></span>
1. <span data-ttu-id="d8382-118">Görüntü, kırpma bölgesini temsil eden alanla kaplanır.</span><span class="sxs-lookup"><span data-stu-id="d8382-118">The image is overlaid with the area representing the crop region.</span></span> <span data-ttu-id="d8382-119">Kırpma bölgesini gerektiği gibi taşıyın ve yeniden boyutlandırın.</span><span class="sxs-lookup"><span data-stu-id="d8382-119">Move and resize the crop region as needed.</span></span> <span data-ttu-id="d8382-120">En boy oranı otomatik olarak korunur.</span><span class="sxs-lookup"><span data-stu-id="d8382-120">The aspect ratio will be maintained automatically.</span></span>
1. <span data-ttu-id="d8382-121">Bitirdiğinizde, komut çubuğunda, **Kaydet**'i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d8382-121">When you're done, on the command bar, select **Save**, and then select **Finish editing**.</span></span> 

<span data-ttu-id="d8382-122">Özel kırpma tamamlandıktan sonra, görüntü değişiklikleri neredeyse hemen gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="d8382-122">After custom cropping is completed, image modifications will take effect almost immediately.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8382-123">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d8382-123">Additional resources</span></span>

[<span data-ttu-id="d8382-124">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="d8382-124">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="d8382-125">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="d8382-125">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="d8382-126">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="d8382-126">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="d8382-127">Dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="d8382-127">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="d8382-128">Görüntünün odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="d8382-128">Customize image focal points</span></span>](dam-custom-focal-point.md)
