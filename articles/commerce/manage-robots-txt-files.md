---
title: robots.txt dosyalarını yönetme
description: Bu konuda, Microsoft Dynamics 365 Commerce'te robots.txt dosyalarının nasıl yönetileceği açıklanmaktadır.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1f7a779d69bf49d3416de3e92d4414cfabf358eb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983635"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="0bef5-103">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="0bef5-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0bef5-104">Bu konuda, Microsoft Dynamics 365 Commerce'te robots.txt dosyalarının nasıl yönetileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0bef5-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0bef5-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="0bef5-105">Overview</span></span>

<span data-ttu-id="0bef5-106">Robotlar özel durum standardı veya robots.txt, Web sitelerinin ağ robotları ile iletişim kurmak için kullandığı standarttır.</span><span class="sxs-lookup"><span data-stu-id="0bef5-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="0bef5-107">Web robotları bir Web sitesinin herhangi bir alanını ziyaret etmemesini söyler.</span><span class="sxs-lookup"><span data-stu-id="0bef5-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="0bef5-108">Robotlar, Web sitelerinin dizinini oluşturmada genellikle arama motorları tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0bef5-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="0bef5-109">Robotları bir sunucudan dışlamak için, sunucuda bir dosya oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="0bef5-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="0bef5-110">Bu dosyada, robotlar ile ilgili bir erişim ilkesi belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0bef5-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="0bef5-111">Dosya, **/robots.txt** yerel URL'sinde http aracılığıyla erişilebilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0bef5-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="0bef5-112">Robots.txt dosyası, arama alt yapılarının sitenizdeki içeriği dizine almanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0bef5-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="0bef5-113">Dynamics 365 Commerce etki alanınız için robots.txt dosyasını karşıya yüklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="0bef5-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="0bef5-114">Commerce ortamınızdaki her etki alanı için bir robots.txt dosyası karşıya yükleyebilir ve bu etki alanıyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0bef5-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="0bef5-115">Robots.txt dosyası hakkında daha fazla bilgi için [Web robots sayfalarını](https://www.robotstxt.org/) ziyaret edin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="0bef5-116">Robots.txt dosyasını karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="0bef5-116">Upload a robots.txt file</span></span>

<span data-ttu-id="0bef5-117">Robots.txt dosyanızı [robots dışlama standardına](https://www.robotstxt.org/orig.html) göre oluşturup düzenledikten sonra, Commerce geliştirme araçlarını kullanacağınız bilgisayarda dosyaya erişilebildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="0bef5-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="0bef5-118">Dosya **robots.txt** olarak adlandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0bef5-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="0bef5-119">En iyi sonuçlar için, bu, standart olarak belirtilen biçimde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="0bef5-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="0bef5-120">Her bir Commerce müşterisi, robots.txt dosyasının içeriğini doğrulamadan ve korumadan sorumludur.</span><span class="sxs-lookup"><span data-stu-id="0bef5-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="0bef5-121">Robots.txt dosyasını karşıya yüklemek için, Commerce'te sistem yöneticisi olarak oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0bef5-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="0bef5-122">Bir robots.txt dosyasını ticari olarak karşıya yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0bef5-123">Commerce'te sistem yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="0bef5-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="0bef5-124">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).</span><span class="sxs-lookup"><span data-stu-id="0bef5-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="0bef5-125">**Kiracı ayarları** altında **robots.txt** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="0bef5-126">Ortamınız ile ilişkilendirilmiş tüm etki alanlarının listesi pencerenin ana bölümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0bef5-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="0bef5-127">Ortamınızdaki bir etki alanı için robots.txt dosyası yüklemek için **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="0bef5-128">Sağdaki menüde, robots.txt dosyasıyla ilişkilendirilmiş etki alanının yanında bulunan **Yükle** düğmesini (yukarı yönlü ok) seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="0bef5-129">Bir dosya tarayıcısı iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0bef5-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="0bef5-130">İletişim kutusunda, ilişkili etki alanı için karşıya yüklemek istediğiniz robots.txt dosyasını bulup seçin ve sonra yüklemeyi tamamlamak için **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="0bef5-131">Karşıya yükleme sırasında, Commerce dosyanın bir metin dosyası olduğunu doğrular, ancak dosyanın içeriğini doğrulamaz.</span><span class="sxs-lookup"><span data-stu-id="0bef5-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="0bef5-132">Robots.txt dosyasını indirme</span><span class="sxs-lookup"><span data-stu-id="0bef5-132">Download a robots.txt file</span></span>

<span data-ttu-id="0bef5-133">Bir robots.txt dosyasını ticari olarak indirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0bef5-134">Commerce'te sistem yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="0bef5-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="0bef5-135">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).</span><span class="sxs-lookup"><span data-stu-id="0bef5-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="0bef5-136">**Kiracı ayarları** altında **robots.txt** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="0bef5-137">Ortamınız ile ilişkilendirilmiş tüm etki alanlarının listesi pencerenin ana bölümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0bef5-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="0bef5-138">Ortamınızdaki bir etki alanı için robots.txt dosyası indirmek için **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="0bef5-139">Sağdaki menüde, robots.txt dosyasıyla ilişkilendirilmiş etki alanının yanında bulunan **İndir** düğmesini (aşağı yönlü ok) seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="0bef5-140">Bir dosya tarayıcısı iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0bef5-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="0bef5-141">İletişim kutusunda, yerel sürücünüzde istediğiniz konuma gidin, bir dosya adı doğrulayın veya girin ve karşıdan yüklemeyi tamamlamak için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="0bef5-142">Bu yordam, daha önce Commerce geliştirme araçlarıyla karşıya yüklenen robots.txt dosyalarını karşıdan yüklemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0bef5-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="0bef5-143">Robots.txt dosyasını silme</span><span class="sxs-lookup"><span data-stu-id="0bef5-143">Delete a robots.txt file</span></span>

<span data-ttu-id="0bef5-144">Bir robots.txt dosyasını ticari olarak silmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0bef5-145">Commerce'te sistem yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="0bef5-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="0bef5-146">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).</span><span class="sxs-lookup"><span data-stu-id="0bef5-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="0bef5-147">**Kiracı ayarları** altında **robots.txt** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="0bef5-148">Ortamınız ile ilişkilendirilmiş tüm etki alanlarının listesi pencerenin ana bölümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0bef5-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="0bef5-149">Ortamınızdaki bir etki alanı için robots.txt dosyası silmek için **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="0bef5-150">Sağdaki menüde, robots.txt dosyasıyla ilişkilendirilmiş etki alanının yanında bulunan **Sil** düğmesini (çöp kutusu simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="0bef5-151">Bir dosya tarayıcı penceresi görünür.</span><span class="sxs-lookup"><span data-stu-id="0bef5-151">A file browser window appears.</span></span>
6. <span data-ttu-id="0bef5-152">Dosya tarayıcı penceresinde, ilişkili etki alanı için silmek istediğiniz robots.txt dosyasını bulup seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="0bef5-153">Bir uyarı iletisi kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0bef5-153">A warning message box appears.</span></span>
7. <span data-ttu-id="0bef5-154">Robots.txt dosyasının silinmesini onaylamak için, ileti kutusunda, **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0bef5-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="0bef5-155">Bu yordam, daha önce Commerce geliştirme araçlarıyla karşıya yüklenen robots.txt dosyalarını silmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0bef5-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bef5-156">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0bef5-156">Additional resources</span></span>

[<span data-ttu-id="0bef5-157">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0bef5-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="0bef5-158">Yeni e-Ticaret sitesini dağıtma</span><span class="sxs-lookup"><span data-stu-id="0bef5-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="0bef5-159">e-Ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0bef5-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="0bef5-160">Çevrimiçi siteyi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="0bef5-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="0bef5-161">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="0bef5-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="0bef5-162">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="0bef5-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="0bef5-163">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="0bef5-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="0bef5-164">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0bef5-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="0bef5-165">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="0bef5-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="0bef5-166">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="0bef5-166">Enable location-based store detection</span></span>](enable-store-detection.md)
