---
title: Görüntünün odak noktalarını özelleştirme
description: Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucuda görüntü odak noktalarının nasıl özelleştirileceği açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.openlocfilehash: 2c9bbd51f1fe9a19198a455eedd3ba744d54a165
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097095"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="8134f-103">Görüntünün odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="8134f-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8134f-104">Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucuda görüntü odak noktalarının nasıl özelleştirileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8134f-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="8134f-105">Özet</span><span class="sxs-lookup"><span data-stu-id="8134f-105">Overview</span></span>

<span data-ttu-id="8134f-106">Commerce site oluşturucu Ortam Kitaplığına bir görüntü yüklendiğinde, sistem görüntünün odak noktasını belirlemeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="8134f-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="8134f-107">Örneğin, görüntüde bir kişi varsa, sistem varsayılan olarak odak noktasını kişinin en yüzüne ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8134f-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="8134f-108">Çoğu durumda, odak noktasını otomatik olarak ayarlama tüm görünüm pencereleri için iyi çalışır, ancak bazen görüntünün belirli bir parçasının her zaman görünür olmasını sağlamak için odak noktasını ayarlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8134f-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="8134f-109">Görüntü için özel bir odak noktası tanımlama</span><span class="sxs-lookup"><span data-stu-id="8134f-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="8134f-110">Bir görüntü için özel bir odak noktası tanımlamak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8134f-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="8134f-111">Commerce site oluşturucunun sol gezinti bölmesinde, **Ortam Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8134f-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="8134f-112">Ana pencerede, değiştirmek istediğiniz görüntüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="8134f-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="8134f-113">Komut çubuğunda, dosyayı kullanıma almak için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8134f-113">On the command bar, select **Edit** to check out the file.</span></span>
1. <span data-ttu-id="8134f-114">**Düzenleme Modu**'na girmek için görüntüyü seçin.</span><span class="sxs-lookup"><span data-stu-id="8134f-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="8134f-115">**Düzenleme Modu** altında **Odak Noktasını Değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8134f-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="8134f-116">Görüntünün üzerinde döngüsel bir odak noktası denetimi görünür.</span><span class="sxs-lookup"><span data-stu-id="8134f-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="8134f-117">İstediğiniz odak noktasının üzerine taşımak için odak noktası denetimini seçin.</span><span class="sxs-lookup"><span data-stu-id="8134f-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="8134f-118">Bitirdiğinizde, komut çubuğunda, **Kaydet**'i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8134f-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8134f-119">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8134f-119">Additional resources</span></span>

[<span data-ttu-id="8134f-120">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="8134f-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="8134f-121">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="8134f-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="8134f-122">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="8134f-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="8134f-123">Dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="8134f-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="8134f-124">Görüntüleri kırpma</span><span class="sxs-lookup"><span data-stu-id="8134f-124">Crop images</span></span>](dam-crop-images.md)
