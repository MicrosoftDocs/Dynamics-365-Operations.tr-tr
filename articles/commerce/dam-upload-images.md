---
title: Resimleri karşıya yükleme
description: Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda görüntüleri karşıya yükleme yöntemi açıklanmaktadır.
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
ms.openlocfilehash: 69b812c58739357dfdb3f9e65e34e5d54d890284
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963022"
---
# <a name="upload-images"></a><span data-ttu-id="0d280-103">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="0d280-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d280-104">Bu konuda, Microsoft Dynamics 365 Commerce' site oluşturucuda görüntüleri karşıya yükleme yöntemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0d280-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="0d280-105">Özet</span><span class="sxs-lookup"><span data-stu-id="0d280-105">Overview</span></span>

<span data-ttu-id="0d280-106">Commerce site oluşturucusu Ortam Kitaplığı, görüntüleri tek tek veya klasörler kullanarak toplu şekilde karşıya yüklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0d280-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="0d280-107">Görüntü yeniden boyutlandırıcı bileşeni, görüntüyü farklı görünüm pencereleri ve kesme noktalarıyla en iyi duruma otomatik olarak getireceğinden her zaman en yüksek çözünürlük ve kaliteye sahip görüntü sürümünü yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0d280-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="0d280-108">Karşıya yükleme sırasında belirtilen görüntü bilgileri</span><span class="sxs-lookup"><span data-stu-id="0d280-108">Image information specified during upload</span></span>

<span data-ttu-id="0d280-109">Görüntü karşıya yüklenirken, aşağıdaki bilgiler belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="0d280-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="0d280-110">**Başlık, Alt Metin, Açıklama, Anahtar Sözcükler**: Görüntü veya görüntülerin meta verileri.</span><span class="sxs-lookup"><span data-stu-id="0d280-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="0d280-111">Başlık ve alt metin gerekli değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="0d280-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="0d280-112">**Kategori seç**:</span><span class="sxs-lookup"><span data-stu-id="0d280-112">**Select category**:</span></span>
    - <span data-ttu-id="0d280-113">**Hiçbiri**: e-Ticaret öykülerinin görüntüsü veya görüntüleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0d280-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="0d280-114">**Ürün, Kategori, Müşteri, Personel, Katalog**: Dynamics 365 Commerce  çok yönlü kanal görüntüsü veya görüntüleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0d280-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="0d280-115">**Karşıya yükleme sonrasında varlıkları yayımla**: Bu onay kutusu seçildiğinde, görüntü veya görüntüler karşıya yüklemeden hemen sonra yayımlanır.</span><span class="sxs-lookup"><span data-stu-id="0d280-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="0d280-116">Kategori atanan görüntü varlıkları da belirli bir kategorinin varlıklarını aramaya yardımcı olacak şekilde kategori ile otomatik olarak etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="0d280-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="0d280-117">Çok yönlü kanal görüntüleri için adlandırma kuralları</span><span class="sxs-lookup"><span data-stu-id="0d280-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="0d280-118">Ortam Kitaplığını çok yönlü kanal görüntüsü arka ucu olarak yapılandırdıysanız, karşıya yüklenen görüntünün hangi kategoriye ait olduğunu göstermek için görüntü kategorilerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d280-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="0d280-119">Ayrıca, görüntülerin satış noktası (POS) gibi diğer kanallar tarafından doğru şekilde alınmasını sağlamak için izlenmesi gereken bir adlandırma kuralı da vardır.</span><span class="sxs-lookup"><span data-stu-id="0d280-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="0d280-120">Varsayılan adlandırma kuralı kategoriye göre değişir:</span><span class="sxs-lookup"><span data-stu-id="0d280-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="0d280-121">Katalog görüntülerinin şu şekilde adlandırılması gerekir: "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="0d280-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="0d280-122">Kategori görüntülerinin şu şekilde adlandırılması gerekir: "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="0d280-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="0d280-123">Müşteri görüntülerinin şu şekilde adlandırılması gerekir: "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="0d280-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="0d280-124">Personel görüntülerinin şu şekilde adlandırılması gerekir: "**/Workers/\{WorkerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="0d280-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="0d280-125">Ürün görüntülerinin şu şekilde adlandırılması gerekir: "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="0d280-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="0d280-126">001 görüntünün sırasıdır ve 001, 002, 003, 004 veya 005 olabilir</span><span class="sxs-lookup"><span data-stu-id="0d280-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="0d280-127">Ürün çeşidi görüntülerinin şu şekilde adlandırılması gerekir: "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="0d280-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="0d280-128">Görüntüyü karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="0d280-128">Upload an image</span></span>

<span data-ttu-id="0d280-129">Site oluşturucuda bir görüntüyü karşıya yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0d280-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0d280-130">Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="0d280-131">Komut çubuğunda, **Karşıya yükle \> Medya Öğelerini Karşıya Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="0d280-132">Dosya Gezgini penceresinde, karşıya yüklenecek bir veya daha fazla resim dosyasını bulun ve seçin ve ardından **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="0d280-133">**Medya Öğesini Karşıya Yükle** iletişim kutusunda gerekli başlığı ve alt metni girin.</span><span class="sxs-lookup"><span data-stu-id="0d280-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="0d280-134">İsteğe bağlı açıklama ve anahtar sözcükleri girin ve isterseniz kategoriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="0d280-135">Görüntüleri karşıya yükledikten hemen sonra yayımlamak isterseniz, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="0d280-136">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="0d280-137">Görüntü klasörünü karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="0d280-137">Upload a folder of images</span></span>

<span data-ttu-id="0d280-138">Site oluşturucuda bir görüntü klasörünü toplu olarak karşıya yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0d280-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="0d280-139">Soldaki gezinti bölmesinde **Medya Kitaplığı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="0d280-140">Komut çubuğunda, **Karşıya yükle \> Klasörü Karşıya Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="0d280-141">Dosya Gezgini penceresinde, karşıya yüklenecek klasörü bulun ve seçin ve ardından **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="0d280-142">**Medya Öğelerini Karşıya Yükle** iletişim kutusunda isteğe bağlı anahtar sözcükleri girin ve isterseniz bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="0d280-143">Klasördeki görüntüleri karşıya yükledikten hemen sonra yayımlamak isterseniz, **Karşıya yükleme sonrasında medyayı yayımla** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="0d280-144">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0d280-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d280-145">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0d280-145">Additional resources</span></span>

[<span data-ttu-id="0d280-146">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="0d280-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="0d280-147">Videoyu karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="0d280-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="0d280-148">Dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="0d280-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="0d280-149">Resimleri kırpma</span><span class="sxs-lookup"><span data-stu-id="0d280-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="0d280-150">Görüntü odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="0d280-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="0d280-151">Statik dosyaları karşıya yükleme ve sunma</span><span class="sxs-lookup"><span data-stu-id="0d280-151">Upload and serve static files</span></span>](upload-serve-static-files.md)
