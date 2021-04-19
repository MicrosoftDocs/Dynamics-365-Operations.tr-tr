---
title: Görüntüler ve videolar dışındaki dosyaları karşıya yükleme
description: Bu konu, Microsoft Dynamics 365 Commerce site oluşturucusunda görüntüler ve videolar dışındaki ikili dosyaların nasıl karşıya yükleneceğini açıklamaktadır.
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799265"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="156bb-103">Görüntüler ve videolar dışındaki dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="156bb-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="156bb-104">Bu konu, Microsoft Dynamics 365 Commerce site oluşturucusunda görüntüler ve videolar dışındaki dosyaların nasıl karşıya yükleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="156bb-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="156bb-105">Commerce site oluşturucusu Ortam Kitaplığı, görüntüler veya videolar dışındaki ikili varlıkların karşıya yüklenmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="156bb-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="156bb-106">Örneğin Microsoft Excel, Microsoft Word, Microsoft PowerPoint veya PDF dosyaları yüklemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="156bb-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="156bb-107">Aşağıdaki belge türleri desteklenir:</span><span class="sxs-lookup"><span data-stu-id="156bb-107">The following document types are supported:</span></span>
- <span data-ttu-id="156bb-108">7Z</span><span class="sxs-lookup"><span data-stu-id="156bb-108">7Z</span></span>
- <span data-ttu-id="156bb-109">AVI</span><span class="sxs-lookup"><span data-stu-id="156bb-109">AVI</span></span>
- <span data-ttu-id="156bb-110">CS</span><span class="sxs-lookup"><span data-stu-id="156bb-110">CS</span></span>
- <span data-ttu-id="156bb-111">CSS</span><span class="sxs-lookup"><span data-stu-id="156bb-111">CSS</span></span>
- <span data-ttu-id="156bb-112">DOC</span><span class="sxs-lookup"><span data-stu-id="156bb-112">DOC</span></span>
- <span data-ttu-id="156bb-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="156bb-113">DOCX</span></span>
- <span data-ttu-id="156bb-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="156bb-114">EPUB</span></span>
- <span data-ttu-id="156bb-115">GIF</span><span class="sxs-lookup"><span data-stu-id="156bb-115">GIF</span></span>
- <span data-ttu-id="156bb-116">INDD</span><span class="sxs-lookup"><span data-stu-id="156bb-116">INDD</span></span>
- <span data-ttu-id="156bb-117">JAR</span><span class="sxs-lookup"><span data-stu-id="156bb-117">JAR</span></span>
- <span data-ttu-id="156bb-118">JPG</span><span class="sxs-lookup"><span data-stu-id="156bb-118">JPG</span></span>
- <span data-ttu-id="156bb-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="156bb-119">JPEG</span></span>
- <span data-ttu-id="156bb-120">JS</span><span class="sxs-lookup"><span data-stu-id="156bb-120">JS</span></span>
- <span data-ttu-id="156bb-121">MP3</span><span class="sxs-lookup"><span data-stu-id="156bb-121">MP3</span></span>
- <span data-ttu-id="156bb-122">MP4</span><span class="sxs-lookup"><span data-stu-id="156bb-122">MP4</span></span>
- <span data-ttu-id="156bb-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="156bb-123">MPEG</span></span>
- <span data-ttu-id="156bb-124">MPG</span><span class="sxs-lookup"><span data-stu-id="156bb-124">MPG</span></span>
- <span data-ttu-id="156bb-125">ODP</span><span class="sxs-lookup"><span data-stu-id="156bb-125">ODP</span></span>
- <span data-ttu-id="156bb-126">ODS</span><span class="sxs-lookup"><span data-stu-id="156bb-126">ODS</span></span>
- <span data-ttu-id="156bb-127">ODT</span><span class="sxs-lookup"><span data-stu-id="156bb-127">ODT</span></span>
- <span data-ttu-id="156bb-128">PDF</span><span class="sxs-lookup"><span data-stu-id="156bb-128">PDF</span></span>
- <span data-ttu-id="156bb-129">PNG</span><span class="sxs-lookup"><span data-stu-id="156bb-129">PNG</span></span>
- <span data-ttu-id="156bb-130">PPT</span><span class="sxs-lookup"><span data-stu-id="156bb-130">PPT</span></span>
- <span data-ttu-id="156bb-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="156bb-131">PPTX</span></span>
- <span data-ttu-id="156bb-132">PS</span><span class="sxs-lookup"><span data-stu-id="156bb-132">PS</span></span>
- <span data-ttu-id="156bb-133">QXP</span><span class="sxs-lookup"><span data-stu-id="156bb-133">QXP</span></span>
- <span data-ttu-id="156bb-134">RAR</span><span class="sxs-lookup"><span data-stu-id="156bb-134">RAR</span></span>
- <span data-ttu-id="156bb-135">RTF</span><span class="sxs-lookup"><span data-stu-id="156bb-135">RTF</span></span>
- <span data-ttu-id="156bb-136">SVG</span><span class="sxs-lookup"><span data-stu-id="156bb-136">SVG</span></span>
- <span data-ttu-id="156bb-137">TAR</span><span class="sxs-lookup"><span data-stu-id="156bb-137">TAR</span></span>
- <span data-ttu-id="156bb-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="156bb-138">TGZ</span></span>
- <span data-ttu-id="156bb-139">TXT</span><span class="sxs-lookup"><span data-stu-id="156bb-139">TXT</span></span>
- <span data-ttu-id="156bb-140">WMV</span><span class="sxs-lookup"><span data-stu-id="156bb-140">WMV</span></span>
- <span data-ttu-id="156bb-141">XLS</span><span class="sxs-lookup"><span data-stu-id="156bb-141">XLS</span></span>
- <span data-ttu-id="156bb-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="156bb-142">XLSX</span></span>
- <span data-ttu-id="156bb-143">XML</span><span class="sxs-lookup"><span data-stu-id="156bb-143">XML</span></span>
- <span data-ttu-id="156bb-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="156bb-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="156bb-145">Dosya yükle</span><span class="sxs-lookup"><span data-stu-id="156bb-145">Upload a file</span></span>

<span data-ttu-id="156bb-146">Bir dosyayı Commerce site oluşturucusuna yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="156bb-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="156bb-147">Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="156bb-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="156bb-148">Komut çubuğunda, **Karşıya yükle \> Medya Öğelerini Karşıya Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="156bb-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="156bb-149">Dosya Gezgini'nde, bir veya daha fazla dosya seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="156bb-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="156bb-150">**Medya Öğesini Karşıya Yükle** iletişim kutusunda, gerekirse başlık, açıklama ve anahtar sözcük meta verilerini girin.</span><span class="sxs-lookup"><span data-stu-id="156bb-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="156bb-151">Dosyaları karşıya yükledikten hemen sonra yayımlamak için, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="156bb-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="156bb-152">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="156bb-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="156bb-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="156bb-153">Additional resources</span></span>

[<span data-ttu-id="156bb-154">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="156bb-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="156bb-155">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="156bb-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="156bb-156">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="156bb-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="156bb-157">Resimleri kırpma</span><span class="sxs-lookup"><span data-stu-id="156bb-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="156bb-158">Görüntü odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="156bb-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="156bb-159">Statik dosyaları karşıya yükleme ve sunma</span><span class="sxs-lookup"><span data-stu-id="156bb-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
