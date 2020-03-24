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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097096"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="f18b2-103">Görüntüler ve videolar dışındaki dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="f18b2-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f18b2-104">Bu konu, Microsoft Dynamics 365 Commerce site oluşturucusunda görüntüler ve videolar dışındaki dosyaların nasıl karşıya yükleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f18b2-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="f18b2-105">Özet</span><span class="sxs-lookup"><span data-stu-id="f18b2-105">Overview</span></span>

<span data-ttu-id="f18b2-106">Commerce site oluşturucusu Ortam Kitaplığı, görüntüler veya videolar dışındaki ikili varlıkların karşıya yüklenmesini destekler.</span><span class="sxs-lookup"><span data-stu-id="f18b2-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="f18b2-107">Örneğin Microsoft Excel, Microsoft Word, Microsoft PowerPoint veya PDF dosyaları yüklemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f18b2-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="f18b2-108">Aşağıdaki belge türleri desteklenir:</span><span class="sxs-lookup"><span data-stu-id="f18b2-108">The following document types are supported:</span></span>
- <span data-ttu-id="f18b2-109">7Z</span><span class="sxs-lookup"><span data-stu-id="f18b2-109">7Z</span></span>
- <span data-ttu-id="f18b2-110">AVI</span><span class="sxs-lookup"><span data-stu-id="f18b2-110">AVI</span></span>
- <span data-ttu-id="f18b2-111">CS</span><span class="sxs-lookup"><span data-stu-id="f18b2-111">CS</span></span>
- <span data-ttu-id="f18b2-112">CSS</span><span class="sxs-lookup"><span data-stu-id="f18b2-112">CSS</span></span>
- <span data-ttu-id="f18b2-113">DOC</span><span class="sxs-lookup"><span data-stu-id="f18b2-113">DOC</span></span>
- <span data-ttu-id="f18b2-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="f18b2-114">DOCX</span></span>
- <span data-ttu-id="f18b2-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="f18b2-115">EPUB</span></span>
- <span data-ttu-id="f18b2-116">GIF</span><span class="sxs-lookup"><span data-stu-id="f18b2-116">GIF</span></span>
- <span data-ttu-id="f18b2-117">INDD</span><span class="sxs-lookup"><span data-stu-id="f18b2-117">INDD</span></span>
- <span data-ttu-id="f18b2-118">JAR</span><span class="sxs-lookup"><span data-stu-id="f18b2-118">JAR</span></span>
- <span data-ttu-id="f18b2-119">JPG</span><span class="sxs-lookup"><span data-stu-id="f18b2-119">JPG</span></span>
- <span data-ttu-id="f18b2-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="f18b2-120">JPEG</span></span>
- <span data-ttu-id="f18b2-121">JS</span><span class="sxs-lookup"><span data-stu-id="f18b2-121">JS</span></span>
- <span data-ttu-id="f18b2-122">MP3</span><span class="sxs-lookup"><span data-stu-id="f18b2-122">MP3</span></span>
- <span data-ttu-id="f18b2-123">MP4</span><span class="sxs-lookup"><span data-stu-id="f18b2-123">MP4</span></span>
- <span data-ttu-id="f18b2-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="f18b2-124">MPEG</span></span>
- <span data-ttu-id="f18b2-125">MPG</span><span class="sxs-lookup"><span data-stu-id="f18b2-125">MPG</span></span>
- <span data-ttu-id="f18b2-126">ODP</span><span class="sxs-lookup"><span data-stu-id="f18b2-126">ODP</span></span>
- <span data-ttu-id="f18b2-127">ODS</span><span class="sxs-lookup"><span data-stu-id="f18b2-127">ODS</span></span>
- <span data-ttu-id="f18b2-128">ODT</span><span class="sxs-lookup"><span data-stu-id="f18b2-128">ODT</span></span>
- <span data-ttu-id="f18b2-129">PDF</span><span class="sxs-lookup"><span data-stu-id="f18b2-129">PDF</span></span>
- <span data-ttu-id="f18b2-130">PNG</span><span class="sxs-lookup"><span data-stu-id="f18b2-130">PNG</span></span>
- <span data-ttu-id="f18b2-131">PPT</span><span class="sxs-lookup"><span data-stu-id="f18b2-131">PPT</span></span>
- <span data-ttu-id="f18b2-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="f18b2-132">PPTX</span></span>
- <span data-ttu-id="f18b2-133">PS</span><span class="sxs-lookup"><span data-stu-id="f18b2-133">PS</span></span>
- <span data-ttu-id="f18b2-134">QXP</span><span class="sxs-lookup"><span data-stu-id="f18b2-134">QXP</span></span>
- <span data-ttu-id="f18b2-135">RAR</span><span class="sxs-lookup"><span data-stu-id="f18b2-135">RAR</span></span>
- <span data-ttu-id="f18b2-136">RTF</span><span class="sxs-lookup"><span data-stu-id="f18b2-136">RTF</span></span>
- <span data-ttu-id="f18b2-137">SVG</span><span class="sxs-lookup"><span data-stu-id="f18b2-137">SVG</span></span>
- <span data-ttu-id="f18b2-138">TAR</span><span class="sxs-lookup"><span data-stu-id="f18b2-138">TAR</span></span>
- <span data-ttu-id="f18b2-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="f18b2-139">TGZ</span></span>
- <span data-ttu-id="f18b2-140">TXT</span><span class="sxs-lookup"><span data-stu-id="f18b2-140">TXT</span></span>
- <span data-ttu-id="f18b2-141">WMV</span><span class="sxs-lookup"><span data-stu-id="f18b2-141">WMV</span></span>
- <span data-ttu-id="f18b2-142">XLS</span><span class="sxs-lookup"><span data-stu-id="f18b2-142">XLS</span></span>
- <span data-ttu-id="f18b2-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="f18b2-143">XLSX</span></span>
- <span data-ttu-id="f18b2-144">XML</span><span class="sxs-lookup"><span data-stu-id="f18b2-144">XML</span></span>
- <span data-ttu-id="f18b2-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="f18b2-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="f18b2-146">Dosya yükle</span><span class="sxs-lookup"><span data-stu-id="f18b2-146">Upload a file</span></span>

<span data-ttu-id="f18b2-147">Bir dosyayı Commerce site oluşturucusuna yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f18b2-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f18b2-148">Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f18b2-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="f18b2-149">Komut çubuğunda, **Karşıya yükle \> Medya Öğelerini Karşıya Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f18b2-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="f18b2-150">Dosya Gezgini'nde, bir veya daha fazla dosya seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f18b2-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="f18b2-151">**Medya Öğesini Karşıya Yükle** iletişim kutusunda, gerekirse başlık, açıklama ve anahtar sözcük meta verilerini girin.</span><span class="sxs-lookup"><span data-stu-id="f18b2-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="f18b2-152">Dosyaları karşıya yükledikten hemen sonra yayımlamak için, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f18b2-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="f18b2-153">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f18b2-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f18b2-154">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f18b2-154">Additional resources</span></span>

[<span data-ttu-id="f18b2-155">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="f18b2-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="f18b2-156">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="f18b2-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="f18b2-157">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="f18b2-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="f18b2-158">Görüntüleri kırpma</span><span class="sxs-lookup"><span data-stu-id="f18b2-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="f18b2-159">Görüntünün odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="f18b2-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
