---
title: Videoları karşıya yükleme
description: Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda videoları karşıya yükleme yöntemi açıklanmaktadır.
author: psimolin
ms.date: 03/03/2020
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
ms.openlocfilehash: 5ec20f8caee2f5a62230be05923dfd52600c1e35
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799217"
---
# <a name="upload-videos"></a><span data-ttu-id="720b8-103">Videoları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="720b8-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="720b8-104">Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda videoları karşıya yükleme yöntemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="720b8-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="720b8-105">Commerce site oluşturucu Ortam Kitaplığı videoları karşıya yüklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="720b8-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="720b8-106">Video farklı görünüm pencereleri ve kesme noktaları için otomatik olarak uygun duruma dönüştürüleceğinden her zaman en yüksek bit hızına ve çözünürlüğe sahip video sürümünü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="720b8-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="720b8-107">Karşıya yükleme sırasında belirtilen video bilgileri</span><span class="sxs-lookup"><span data-stu-id="720b8-107">Video information specified during upload</span></span>

<span data-ttu-id="720b8-108">Video karşıya yüklenirken, aşağıdaki bilgiler belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="720b8-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="720b8-109">**Başlık, Açıklama, Anahtar Sözcükler**: Videonun meta verileri.</span><span class="sxs-lookup"><span data-stu-id="720b8-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="720b8-110">**Açıklamalı alt yazıları otomatik oluştur**: Video için açıklamalı alt yazıların otomatik olarak oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b8-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="720b8-111">**Açıklamalı Altyazı**: Kullanılacak açıklamalı alt yazıları belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b8-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="720b8-112">**Normal Ses**: Kullanılacak normal ses parçasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b8-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="720b8-113">**Küçük resim**: Videonun küçük resmini belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b8-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="720b8-114">Belirtilmezse, otomatik olarak oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="720b8-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="720b8-115">**Açıklayıcı Ses**: Kullanılacak açıklayıcı ses parçasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="720b8-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="720b8-116">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="720b8-116">Upload a video</span></span>

<span data-ttu-id="720b8-117">Site oluşturucuda bir videoyu karşıya yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="720b8-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="720b8-118">Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="720b8-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="720b8-119">Komut çubuğunda, **Karşıya yükle \> Medya Öğelerini Karşıya Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="720b8-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="720b8-120">Dosya Gezgini penceresinde, karşıya yüklenecek bir veya daha fazla video dosyasını bulun ve seçin ve ardından **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="720b8-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="720b8-121">**Medya Öğesini Karşıya Yükle** iletişim kutusunda gerekli başlığı ve alt metni girin.</span><span class="sxs-lookup"><span data-stu-id="720b8-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="720b8-122">İsteğe bağlı açıklama ve anahtar sözcükleri girin ve isterseniz kategoriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="720b8-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="720b8-123">Görüntüleri karşıya yükledikten hemen sonra yayımlamak isterseniz, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin</span><span class="sxs-lookup"><span data-stu-id="720b8-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="720b8-124">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="720b8-124">Select **OK**.</span></span>

<span data-ttu-id="720b8-125">Birden çok varlık türünü aynı anda (örneğin, görüntüler ve videolar) karşıya yüklüyorsanız, **Ortam Öğesini Karşıya Yükle** iletişim kutusunda yalnızca anahtar sözcükler, dosyaların karşıya yüklendikten hemen sonra yayımlanıp yayımlanmayacağı ve video dosyaları için açıklamalı alt yazıların otomatik olarak oluşturulup oluşturulmayacağı belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="720b8-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="720b8-126">Tüm varlıklar aynı anahtar sözcükleri paylaşacaktır.</span><span class="sxs-lookup"><span data-stu-id="720b8-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="720b8-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="720b8-127">Additional resources</span></span>

[<span data-ttu-id="720b8-128">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="720b8-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="720b8-129">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="720b8-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="720b8-130">Dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="720b8-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="720b8-131">Resimleri kırpma</span><span class="sxs-lookup"><span data-stu-id="720b8-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="720b8-132">Görüntü odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="720b8-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="720b8-133">Statik dosyaları karşıya yükleme ve sunma</span><span class="sxs-lookup"><span data-stu-id="720b8-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
