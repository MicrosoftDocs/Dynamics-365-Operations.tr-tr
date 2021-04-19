---
title: Görüntünün odak noktalarını özelleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucuda görüntü odak noktalarının nasıl özelleştirileceği açıklanmaktadır.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 962caff0e8e41487231c6075fa7b2df2a59dca48
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799313"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="34df9-103">Görüntünün odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="34df9-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="34df9-104">Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucuda görüntü odak noktalarının nasıl özelleştirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="34df9-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="34df9-105">Commerce site oluşturucu Ortam Kitaplığına bir görüntü yüklendiğinde, sistem görüntünün odak noktasını belirlemeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="34df9-105">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="34df9-106">Örneğin, görüntüde bir kişi varsa, sistem varsayılan olarak odak noktasını kişinin en yüzüne ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34df9-106">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="34df9-107">Çoğu durumda, odak noktasını otomatik olarak ayarlama tüm görünüm pencereleri için iyi çalışır, ancak bazen görüntünün belirli bir parçasının her zaman görünür olmasını sağlamak için odak noktasını ayarlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34df9-107">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="34df9-108">Görüntü için özel bir odak noktası tanımlama</span><span class="sxs-lookup"><span data-stu-id="34df9-108">Define a custom focal point for an image</span></span>

<span data-ttu-id="34df9-109">Bir görüntü için özel bir odak noktası tanımlamak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="34df9-109">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="34df9-110">Commerce site oluşturucunun sol gezinti bölmesinde, **Ortam Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="34df9-110">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="34df9-111">Ana pencerede, değiştirmek istediğiniz görüntüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="34df9-111">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="34df9-112">Komut çubuğunda, **Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="34df9-112">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="34df9-113">**Düzenleme Modu**'na girmek için görüntüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="34df9-113">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="34df9-114">**Düzenleme Modu** altında **Odak Noktasını Değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="34df9-114">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="34df9-115">Görüntünün üzerinde döngüsel bir odak noktası denetimi görünür.</span><span class="sxs-lookup"><span data-stu-id="34df9-115">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="34df9-116">İstediğiniz odak noktasının üzerine taşımak için odak noktası denetimini seçin.</span><span class="sxs-lookup"><span data-stu-id="34df9-116">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="34df9-117">Bitirdiğinizde, komut çubuğunda, **Kaydet**'i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="34df9-117">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34df9-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="34df9-118">Additional resources</span></span>

[<span data-ttu-id="34df9-119">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="34df9-119">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="34df9-120">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="34df9-120">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="34df9-121">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="34df9-121">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="34df9-122">Dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="34df9-122">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="34df9-123">Resimleri kırpma</span><span class="sxs-lookup"><span data-stu-id="34df9-123">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="34df9-124">Statik dosyaları karşıya yükleme ve sunma</span><span class="sxs-lookup"><span data-stu-id="34df9-124">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
