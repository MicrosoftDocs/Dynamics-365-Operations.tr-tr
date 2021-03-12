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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2cf8d43062ec527755fdf1a28f0ea3ceac1fbc15
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003840"
---
# <a name="crop-images"></a><span data-ttu-id="d135a-103">Görüntüleri kırpma</span><span class="sxs-lookup"><span data-stu-id="d135a-103">Crop images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d135a-104">Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda görüntüleri kırpma yöntemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d135a-104">This topic describes how to crop images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="d135a-105">Özet</span><span class="sxs-lookup"><span data-stu-id="d135a-105">Overview</span></span>

<span data-ttu-id="d135a-106">Commerce site oluşturucusu Ortam Kitaplığı, farklı modül türleri ve görünüm pencereleri için en iyi duruma getirmek amacıyla görüntüleri kırpmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d135a-106">The Commerce site builder Media Library allows you to crop images to optimize them for different module types and viewports.</span></span>

## <a name="crop-an-image"></a><span data-ttu-id="d135a-107">Görüntüyü kırpma</span><span class="sxs-lookup"><span data-stu-id="d135a-107">Crop an image</span></span>

<span data-ttu-id="d135a-108">Site oluşturucuda bir görüntüyü kırpmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d135a-108">To crop an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d135a-109">Commerce site oluşturucunun sol gezinti bölmesinde, **Ortam Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-109">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="d135a-110">Ana pencerede, değiştirmek istediğiniz görüntüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-110">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="d135a-111">Komut çubuğunda, **Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-111">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="d135a-112">**Düzenleme Modu**'na girmek için görüntüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-112">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="d135a-113">**Düzenleme Modu** altında **Görünümü Modüle göre Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-113">Under **Edit Mode**, select **Edit View by Module**.</span></span>
1. <span data-ttu-id="d135a-114">**Modül** açılan menüsünde modül türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-114">From the **Module** drop-down menu, select the module type.</span></span>
1. <span data-ttu-id="d135a-115">**Görünüm türü** açılan menüsünde görünüm türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-115">From the **View type** drop-down menu, select the view type.</span></span>
1. <span data-ttu-id="d135a-116">**Yerleşim** açılır menüsünden görüntü yerleşimini seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-116">From the **Placement** drop-down menu, select the image placement.</span></span>
1. <span data-ttu-id="d135a-117">**Görünüm penceresi** açılan menüsünde görünüm penceresi boyutunu seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-117">From the **Viewport** drop-down menu, select the viewport size.</span></span>
1. <span data-ttu-id="d135a-118">Görüntü, kırpma bölgesini temsil eden alanla kaplanır.</span><span class="sxs-lookup"><span data-stu-id="d135a-118">The image is overlaid with the area representing the crop region.</span></span> <span data-ttu-id="d135a-119">Kırpma bölgesini gerektiği gibi taşıyın ve yeniden boyutlandırın.</span><span class="sxs-lookup"><span data-stu-id="d135a-119">Move and resize the crop region as needed.</span></span> <span data-ttu-id="d135a-120">En boy oranı otomatik olarak korunur.</span><span class="sxs-lookup"><span data-stu-id="d135a-120">The aspect ratio will be maintained automatically.</span></span>
1. <span data-ttu-id="d135a-121">Bitirdiğinizde, komut çubuğunda, **Kaydet**'i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d135a-121">When you're done, on the command bar, select **Save**, and then select **Finish editing**.</span></span> 

<span data-ttu-id="d135a-122">Özel kırpma tamamlandıktan sonra, görüntü değişiklikleri neredeyse hemen gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="d135a-122">After custom cropping is completed, image modifications will take effect almost immediately.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d135a-123">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d135a-123">Additional resources</span></span>

[<span data-ttu-id="d135a-124">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="d135a-124">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="d135a-125">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="d135a-125">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="d135a-126">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="d135a-126">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="d135a-127">Dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="d135a-127">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="d135a-128">Görüntü odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="d135a-128">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="d135a-129">Statik dosyaları karşıya yükleme ve sunma</span><span class="sxs-lookup"><span data-stu-id="d135a-129">Upload and serve static files</span></span>](upload-serve-static-files.md)
