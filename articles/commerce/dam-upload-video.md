---
title: Videoları karşıya yükleme
description: Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda videoları karşıya yükleme yöntemi açıklanmaktadır.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.openlocfilehash: a8cabcd3528308919697a9f2ecb2a81ad5acbe31
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000937"
---
# <a name="upload-videos"></a><span data-ttu-id="9bf07-103">Videoları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="9bf07-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9bf07-104">Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda videoları karşıya yükleme yöntemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9bf07-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="9bf07-105">Özet</span><span class="sxs-lookup"><span data-stu-id="9bf07-105">Overview</span></span>

<span data-ttu-id="9bf07-106">Commerce site oluşturucu Ortam Kitaplığı videoları karşıya yüklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9bf07-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="9bf07-107">Video farklı görünüm pencereleri ve kesme noktaları için otomatik olarak uygun duruma dönüştürüleceğinden her zaman en yüksek bit hızına ve çözünürlüğe sahip video sürümünü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9bf07-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="9bf07-108">Karşıya yükleme sırasında belirtilen video bilgileri</span><span class="sxs-lookup"><span data-stu-id="9bf07-108">Video information specified during upload</span></span>

<span data-ttu-id="9bf07-109">Video karşıya yüklenirken, aşağıdaki bilgiler belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="9bf07-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="9bf07-110">**Başlık, Açıklama, Anahtar Sözcükler**: Videonun meta verileri.</span><span class="sxs-lookup"><span data-stu-id="9bf07-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="9bf07-111">**Açıklamalı alt yazıları otomatik oluştur**: Video için açıklamalı alt yazıların otomatik olarak oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bf07-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="9bf07-112">**Açıklamalı Altyazı**: Kullanılacak açıklamalı alt yazıları belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bf07-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="9bf07-113">**Normal Ses**: Kullanılacak normal ses parçasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bf07-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="9bf07-114">**Küçük resim**: Videonun küçük resmini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bf07-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="9bf07-115">Belirtilmezse, otomatik olarak oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="9bf07-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="9bf07-116">**Açıklayıcı Ses**: Kullanılacak açıklayıcı ses parçasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9bf07-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="9bf07-117">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="9bf07-117">Upload a video</span></span>

<span data-ttu-id="9bf07-118">Site oluşturucuda bir videoyu karşıya yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9bf07-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="9bf07-119">Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="9bf07-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="9bf07-120">Komut çubuğunda, **Karşıya yükle \> Medya Öğelerini Karşıya Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9bf07-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="9bf07-121">Dosya Gezgini penceresinde, karşıya yüklenecek bir veya daha fazla video dosyasını bulun ve seçin ve ardından **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9bf07-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="9bf07-122">**Medya Öğesini Karşıya Yükle** iletişim kutusunda gerekli başlığı ve alt metni girin.</span><span class="sxs-lookup"><span data-stu-id="9bf07-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="9bf07-123">İsteğe bağlı açıklama ve anahtar sözcükleri girin ve isterseniz kategoriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="9bf07-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="9bf07-124">Görüntüleri karşıya yükledikten hemen sonra yayımlamak isterseniz, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin</span><span class="sxs-lookup"><span data-stu-id="9bf07-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="9bf07-125">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="9bf07-125">Select **OK**.</span></span>

<span data-ttu-id="9bf07-126">Birden çok varlık türünü aynı anda (örneğin, görüntüler ve videolar) karşıya yüklüyorsanız, **Ortam Öğesini Karşıya Yükle** iletişim kutusunda yalnızca anahtar sözcükler, dosyaların karşıya yüklendikten hemen sonra yayımlanıp yayımlanmayacağı ve video dosyaları için açıklamalı alt yazıların otomatik olarak oluşturulup oluşturulmayacağı belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="9bf07-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="9bf07-127">Tüm varlıklar aynı anahtar sözcükleri paylaşacaktır.</span><span class="sxs-lookup"><span data-stu-id="9bf07-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bf07-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9bf07-128">Additional resources</span></span>

[<span data-ttu-id="9bf07-129">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="9bf07-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="9bf07-130">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="9bf07-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="9bf07-131">Dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="9bf07-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="9bf07-132">Resimleri kırpma</span><span class="sxs-lookup"><span data-stu-id="9bf07-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="9bf07-133">Görüntü odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="9bf07-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="9bf07-134">Statik dosyaları karşıya yükleme ve sunma</span><span class="sxs-lookup"><span data-stu-id="9bf07-134">Upload and serve static files</span></span>](upload-serve-static-files.md)
