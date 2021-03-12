---
title: Görüntüler ve videolar dışındaki dosyaları karşıya yükleme
description: Bu konu, Microsoft Dynamics 365 Commerce site oluşturucusunda görüntüler ve videolar dışındaki ikili dosyaların nasıl karşıya yükleneceğini açıklamaktadır.
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
ms.openlocfilehash: 3392f5f36d04e8cb0a9d6e6b7db31ff62c987649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995782"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="8620c-103">Görüntüler ve videolar dışındaki dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="8620c-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8620c-104">Bu konu, Microsoft Dynamics 365 Commerce site oluşturucusunda görüntüler ve videolar dışındaki dosyaların nasıl karşıya yükleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="8620c-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="8620c-105">Özet</span><span class="sxs-lookup"><span data-stu-id="8620c-105">Overview</span></span>

<span data-ttu-id="8620c-106">Commerce site oluşturucusu Ortam Kitaplığı, görüntüler veya videolar dışındaki ikili varlıkların karşıya yüklenmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="8620c-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="8620c-107">Örneğin Microsoft Excel, Microsoft Word, Microsoft PowerPoint veya PDF dosyaları yüklemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8620c-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="8620c-108">Aşağıdaki belge türleri desteklenir:</span><span class="sxs-lookup"><span data-stu-id="8620c-108">The following document types are supported:</span></span>
- <span data-ttu-id="8620c-109">7Z</span><span class="sxs-lookup"><span data-stu-id="8620c-109">7Z</span></span>
- <span data-ttu-id="8620c-110">AVI</span><span class="sxs-lookup"><span data-stu-id="8620c-110">AVI</span></span>
- <span data-ttu-id="8620c-111">CS</span><span class="sxs-lookup"><span data-stu-id="8620c-111">CS</span></span>
- <span data-ttu-id="8620c-112">CSS</span><span class="sxs-lookup"><span data-stu-id="8620c-112">CSS</span></span>
- <span data-ttu-id="8620c-113">DOC</span><span class="sxs-lookup"><span data-stu-id="8620c-113">DOC</span></span>
- <span data-ttu-id="8620c-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="8620c-114">DOCX</span></span>
- <span data-ttu-id="8620c-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="8620c-115">EPUB</span></span>
- <span data-ttu-id="8620c-116">GIF</span><span class="sxs-lookup"><span data-stu-id="8620c-116">GIF</span></span>
- <span data-ttu-id="8620c-117">INDD</span><span class="sxs-lookup"><span data-stu-id="8620c-117">INDD</span></span>
- <span data-ttu-id="8620c-118">JAR</span><span class="sxs-lookup"><span data-stu-id="8620c-118">JAR</span></span>
- <span data-ttu-id="8620c-119">JPG</span><span class="sxs-lookup"><span data-stu-id="8620c-119">JPG</span></span>
- <span data-ttu-id="8620c-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="8620c-120">JPEG</span></span>
- <span data-ttu-id="8620c-121">JS</span><span class="sxs-lookup"><span data-stu-id="8620c-121">JS</span></span>
- <span data-ttu-id="8620c-122">MP3</span><span class="sxs-lookup"><span data-stu-id="8620c-122">MP3</span></span>
- <span data-ttu-id="8620c-123">MP4</span><span class="sxs-lookup"><span data-stu-id="8620c-123">MP4</span></span>
- <span data-ttu-id="8620c-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="8620c-124">MPEG</span></span>
- <span data-ttu-id="8620c-125">MPG</span><span class="sxs-lookup"><span data-stu-id="8620c-125">MPG</span></span>
- <span data-ttu-id="8620c-126">ODP</span><span class="sxs-lookup"><span data-stu-id="8620c-126">ODP</span></span>
- <span data-ttu-id="8620c-127">ODS</span><span class="sxs-lookup"><span data-stu-id="8620c-127">ODS</span></span>
- <span data-ttu-id="8620c-128">ODT</span><span class="sxs-lookup"><span data-stu-id="8620c-128">ODT</span></span>
- <span data-ttu-id="8620c-129">PDF</span><span class="sxs-lookup"><span data-stu-id="8620c-129">PDF</span></span>
- <span data-ttu-id="8620c-130">PNG</span><span class="sxs-lookup"><span data-stu-id="8620c-130">PNG</span></span>
- <span data-ttu-id="8620c-131">PPT</span><span class="sxs-lookup"><span data-stu-id="8620c-131">PPT</span></span>
- <span data-ttu-id="8620c-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="8620c-132">PPTX</span></span>
- <span data-ttu-id="8620c-133">PS</span><span class="sxs-lookup"><span data-stu-id="8620c-133">PS</span></span>
- <span data-ttu-id="8620c-134">QXP</span><span class="sxs-lookup"><span data-stu-id="8620c-134">QXP</span></span>
- <span data-ttu-id="8620c-135">RAR</span><span class="sxs-lookup"><span data-stu-id="8620c-135">RAR</span></span>
- <span data-ttu-id="8620c-136">RTF</span><span class="sxs-lookup"><span data-stu-id="8620c-136">RTF</span></span>
- <span data-ttu-id="8620c-137">SVG</span><span class="sxs-lookup"><span data-stu-id="8620c-137">SVG</span></span>
- <span data-ttu-id="8620c-138">TAR</span><span class="sxs-lookup"><span data-stu-id="8620c-138">TAR</span></span>
- <span data-ttu-id="8620c-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="8620c-139">TGZ</span></span>
- <span data-ttu-id="8620c-140">TXT</span><span class="sxs-lookup"><span data-stu-id="8620c-140">TXT</span></span>
- <span data-ttu-id="8620c-141">WMV</span><span class="sxs-lookup"><span data-stu-id="8620c-141">WMV</span></span>
- <span data-ttu-id="8620c-142">XLS</span><span class="sxs-lookup"><span data-stu-id="8620c-142">XLS</span></span>
- <span data-ttu-id="8620c-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="8620c-143">XLSX</span></span>
- <span data-ttu-id="8620c-144">XML</span><span class="sxs-lookup"><span data-stu-id="8620c-144">XML</span></span>
- <span data-ttu-id="8620c-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="8620c-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="8620c-146">Dosya yükle</span><span class="sxs-lookup"><span data-stu-id="8620c-146">Upload a file</span></span>

<span data-ttu-id="8620c-147">Bir dosyayı Commerce site oluşturucusuna yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8620c-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="8620c-148">Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8620c-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="8620c-149">Komut çubuğunda, **Karşıya yükle \> Medya Öğelerini Karşıya Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8620c-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="8620c-150">Dosya Gezgini'nde, bir veya daha fazla dosya seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8620c-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="8620c-151">**Medya Öğesini Karşıya Yükle** iletişim kutusunda, gerekirse başlık, açıklama ve anahtar sözcük meta verilerini girin.</span><span class="sxs-lookup"><span data-stu-id="8620c-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="8620c-152">Dosyaları karşıya yükledikten hemen sonra yayımlamak için, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="8620c-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="8620c-153">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8620c-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8620c-154">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8620c-154">Additional resources</span></span>

[<span data-ttu-id="8620c-155">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="8620c-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="8620c-156">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="8620c-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="8620c-157">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="8620c-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="8620c-158">Resimleri kırpma</span><span class="sxs-lookup"><span data-stu-id="8620c-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="8620c-159">Görüntü odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="8620c-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="8620c-160">Statik dosyaları karşıya yükleme ve sunma</span><span class="sxs-lookup"><span data-stu-id="8620c-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
