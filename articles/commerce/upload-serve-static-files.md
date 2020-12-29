---
title: Statik dosyaları karşıya yükleme ve sunma
description: Bu konu, Microsoft Dynamics 365 Commerce site Builder'a statik bir dosya yükleme ve bu dosyayı istemek için kullanılabilecek özel bir URL ve dosya adı oluşturma konularını açıklamaktadır.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
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
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 981bbf03480abfd812b4020173b7acfdad0fef14
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595006"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="86825-103">Statik dosyaları karşıya yükleme ve sunma</span><span class="sxs-lookup"><span data-stu-id="86825-103">Upload and serve static files</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="86825-104">Bu konu, Microsoft Dynamics 365 Commerce site Builder'a statik bir dosya yükleme ve bu dosyayı istemek için kullanılabilecek özel bir URL ve dosya adı oluşturma konularını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="86825-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="86825-105">Bazı üçüncü taraf bağlayıcılar, bir dosyanın barındırılmasını ve e-ticaret sitesinden sunulmasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="86825-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="86825-106">Bu bağlayıcılar, dosyanın istekler tarafından belirli bir geri arama URL'sine yol ve dosya adıyla verilmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="86825-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="86825-107">Bu nedenle bu konu, bir Dynamics 365 Commerce e-ticaret sitesinde Kullanıcı tarafından tanımlanabilir bir URL ve dosya adı bulunan statik bir dosyanın nasıl karşıya yükleneceğini ve hizmet verileceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="86825-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="86825-108">Statik dosya döndüren bir site URL'si oluştur</span><span class="sxs-lookup"><span data-stu-id="86825-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="86825-109">Commerce Site Builder 'da statik dosya döndüren bir site URL'si oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86825-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="86825-110">Sitenizin ortam kitaplığına gidin ve tanımladığınız URL'ye istek tarafından sunulması gereken dosyayı karşıya yükleyin.</span><span class="sxs-lookup"><span data-stu-id="86825-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="86825-111">Dosyayı zaten karşıya yüklediyseniz, bu adımı atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86825-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="86825-112">Sitenizin **URL**'lerine gidin.</span><span class="sxs-lookup"><span data-stu-id="86825-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="86825-113">**Yeni \> Yeni URL**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="86825-114">**Yenı URL** iletişim kutusunda **ortam kitaplığı varlığı** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="86825-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="86825-115">**URL yolu** alanına URL yolunu girin.</span><span class="sxs-lookup"><span data-stu-id="86825-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="86825-116">Yola dosya adını dahil edin.</span><span class="sxs-lookup"><span data-stu-id="86825-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="86825-117">**Sonraki**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-117">Select **Next**.</span></span> <span data-ttu-id="86825-118">Ortam kitaplığı açılır ve **belge** türünün yüklenmiş olduğu tüm ortam varlıklarını gösterir .</span><span class="sxs-lookup"><span data-stu-id="86825-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="86825-119">Adım 5'te tanımladığınız URL'ye yönelik istekler için sunulması gereken dosyayı seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="86825-120">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-120">Select **Save**.</span></span>

<span data-ttu-id="86825-121">Bu noktada, oluşturduğunuz URL Taslak durumundadır.</span><span class="sxs-lookup"><span data-stu-id="86825-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="86825-122">URL'nin gösterdiği dosya, siz URL'yi yayınlana kadar döndürülmez.</span><span class="sxs-lookup"><span data-stu-id="86825-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="86825-123">URL'yi yayımlamadan önce, doğru verileri döndüren doğrulamasını doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86825-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="86825-124">URL doğrulayın ve yayınlayın</span><span class="sxs-lookup"><span data-stu-id="86825-124">Validate and publish a URL</span></span>

<span data-ttu-id="86825-125">Yayınlamadan önce URL'yi doğrulamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86825-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="86825-126">Sitenizin **URL** 'lerine gidin ve önizlenecek URL'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="86825-127">Sağdaki Özellikler bölmesinde, **Düzenle** düğmesinin altında, doğru URL bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="86825-128">Yeni bir tarayıcı penceresi açılır ve bir 404 hatası almalısınız.</span><span class="sxs-lookup"><span data-stu-id="86825-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="86825-129">**?preview=inprogress** sorgu dizesini URL 'ye ekleyin (örneğin `https://yoursite.com/callback.html?preview=inprogress`) ve sayfayı yeniden yükleyin.</span><span class="sxs-lookup"><span data-stu-id="86825-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="86825-130">Ortam kitaplığına yüklediğiniz dosya yanıt olarak döndürülmeli.</span><span class="sxs-lookup"><span data-stu-id="86825-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="86825-131">URL'yi doğruladıktan sonra yayımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86825-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="86825-132">Sitenizin **URL** 'lerine gidin ve URL'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="86825-133">Komut çubuğunda, **Yayınla** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="86825-134">URL'nin gösterdiği dosyayı Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="86825-134">Update the file that a URL points to</span></span>

<span data-ttu-id="86825-135">URL yayımlandıktan sonra, farklı bir dosyayı işaret eden şekilde güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86825-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="86825-136">Alternatif olarak, sonraki bölümde açıklandığı gibi, URL'yi farklı türden bir kaynağa işaret eden bir kaynak türü gösteren şekilde güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86825-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="86825-137">Örneğin, URL'yi dahili bir sayfaya veya yeniden yönlendirmeye işaret edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86825-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="86825-138">URL'nin gösterdiği dosyayı güncelleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86825-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="86825-139">Sitenizin **URL** 'lerine gidin ve güncellenecek URL'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="86825-140">Sağdaki özellikler bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="86825-141">**URL ataması altında**, **Adım 2** kutusunu seçin ve ortam kitaplığından yeni bir belge seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="86825-142">**Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="86825-143">URL'nin gösterdiği varlık türünü güncelleştir</span><span class="sxs-lookup"><span data-stu-id="86825-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="86825-144">Ayrıca bir URL'yi, dahili sayfa veya yeniden yönlendirme gibi farklı bir varlık türünü (kaynak) işaret eden şekilde güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86825-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="86825-145">URL'nin gösterdiği varlık türünü güncelleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86825-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="86825-146">Sitenizin **URL** 'lerine gidin ve güncellenecek URL'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="86825-147">Sağdaki özellikler bölmesinde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="86825-148">**URL ataması** altında , **1. adımda** farklı bir varlık türü seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="86825-149">**Adım 2** kutusunu seçin ve sonra yeni varlığı seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="86825-150">**Uygula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="86825-151">URL yolunu değiştir</span><span class="sxs-lookup"><span data-stu-id="86825-151">Change the URL path</span></span>

<span data-ttu-id="86825-152">URL oluşturulduktan sonra, yolu değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="86825-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="86825-153">Bir dosyaya veya başka bir kaynak türüne hizmet veren URL yolunu değiştirmeniz gerekiyorsa, yeni bir URL oluşturmanız, varolan dosya veya diğer kaynakla eşlemeniz ve sonra eski URL'yi yayımdan kaldırmanız ve silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="86825-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="86825-154">URL yolu değiştirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="86825-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="86825-155">Yeni bir URL oluşturmak ve varolan bir dosyaya veya başka bir kaynağa eşlemek için, [Bu konunun yukarısındaki statik dosya bölümü döndüren bir site URL 'si oluştur konusundaki yönergeleri izleyin ](#create-a-site-url-that-returns-a-static-file).</span><span class="sxs-lookup"><span data-stu-id="86825-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="86825-156">Yeni URL'yi seçin ve komut çubuğunda **yayınla** 'yı seçin .</span><span class="sxs-lookup"><span data-stu-id="86825-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="86825-157">Yeni URL yayımlandı.</span><span class="sxs-lookup"><span data-stu-id="86825-157">The new URL is published.</span></span>
1. <span data-ttu-id="86825-158">Eski URL'yi yayımdan kaldırmak için, onu seçin ve sonra komut çubuğunda **Yayımdan Kaldır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="86825-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="86825-159">İsterseniz eski URL'yi artık silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86825-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86825-160">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="86825-160">Additional resources</span></span>

[<span data-ttu-id="86825-161">Dijital varlık yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="86825-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="86825-162">Resimleri karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="86825-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="86825-163">Videoları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="86825-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="86825-164">Resimler ve videolar dışındaki dosyaları karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="86825-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="86825-165">Resimleri kırpma</span><span class="sxs-lookup"><span data-stu-id="86825-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="86825-166">Görüntü odak noktalarını özelleştirme</span><span class="sxs-lookup"><span data-stu-id="86825-166">Customize image focal points</span></span>](dam-custom-focal-point.md)
