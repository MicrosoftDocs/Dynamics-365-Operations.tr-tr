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
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477720"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="f04ae-103">robots.txt dosyalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="f04ae-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f04ae-104">Bu konuda, Microsoft Dynamics 365 Commerce'te robots.txt dosyalarının nasıl yönetileceği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f04ae-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f04ae-105">Robotlar özel durum standardı veya robots.txt, Web sitelerinin ağ robotları ile iletişim kurmak için kullandığı standarttır.</span><span class="sxs-lookup"><span data-stu-id="f04ae-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="f04ae-106">Web robotları bir Web sitesinin herhangi bir alanını ziyaret etmemesini söyler.</span><span class="sxs-lookup"><span data-stu-id="f04ae-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="f04ae-107">Robotlar, Web sitelerinin dizinini oluşturmada genellikle arama motorları tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f04ae-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="f04ae-108">Robotları bir sunucudan dışlamak için, sunucuda bir dosya oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="f04ae-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="f04ae-109">Bu dosyada, robotlar ile ilgili bir erişim ilkesi belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f04ae-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="f04ae-110">Dosya, **/robots.txt** yerel URL'sinde http aracılığıyla erişilebilir olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f04ae-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="f04ae-111">Robots.txt dosyası, arama alt yapılarının sitenizdeki içeriği dizine almanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="f04ae-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="f04ae-112">Dynamics 365 Commerce etki alanınız için robots.txt dosyasını karşıya yüklemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f04ae-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="f04ae-113">Commerce ortamınızdaki her etki alanı için bir robots.txt dosyası karşıya yükleyebilir ve bu etki alanıyla ilişkilendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f04ae-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="f04ae-114">Robots.txt dosyası hakkında daha fazla bilgi için [Web robots sayfalarını](https://www.robotstxt.org/) ziyaret edin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="f04ae-115">Robots.txt dosyasını karşıya yükleme</span><span class="sxs-lookup"><span data-stu-id="f04ae-115">Upload a robots.txt file</span></span>

<span data-ttu-id="f04ae-116">Robots.txt dosyanızı [robots dışlama standardına](https://www.robotstxt.org/orig.html) göre oluşturup düzenledikten sonra, Commerce geliştirme araçlarını kullanacağınız bilgisayarda dosyaya erişilebildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="f04ae-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="f04ae-117">Dosya **robots.txt** olarak adlandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f04ae-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="f04ae-118">En iyi sonuçlar için, bu, standart olarak belirtilen biçimde olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f04ae-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="f04ae-119">Her bir Commerce müşterisi, robots.txt dosyasının içeriğini doğrulamadan ve korumadan sorumludur.</span><span class="sxs-lookup"><span data-stu-id="f04ae-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="f04ae-120">Robots.txt dosyasını karşıya yüklemek için, Commerce'te sistem yöneticisi olarak oturum açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f04ae-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="f04ae-121">Bir robots.txt dosyasını ticari olarak karşıya yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f04ae-122">Commerce'te sistem yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="f04ae-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="f04ae-123">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).</span><span class="sxs-lookup"><span data-stu-id="f04ae-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="f04ae-124">**Kiracı ayarları** altında **robots.txt** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="f04ae-125">Ortamınız ile ilişkilendirilmiş tüm etki alanlarının listesi pencerenin ana bölümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f04ae-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="f04ae-126">Ortamınızdaki bir etki alanı için robots.txt dosyası yüklemek için **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="f04ae-127">Sağdaki menüde, robots.txt dosyasıyla ilişkilendirilmiş etki alanının yanında bulunan **Yükle** düğmesini (yukarı yönlü ok) seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="f04ae-128">Bir dosya tarayıcısı iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f04ae-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="f04ae-129">İletişim kutusunda, ilişkili etki alanı için karşıya yüklemek istediğiniz robots.txt dosyasını bulup seçin ve sonra yüklemeyi tamamlamak için **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="f04ae-130">Karşıya yükleme sırasında, Commerce dosyanın bir metin dosyası olduğunu doğrular, ancak dosyanın içeriğini doğrulamaz.</span><span class="sxs-lookup"><span data-stu-id="f04ae-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="f04ae-131">Robots.txt dosyasını indirme</span><span class="sxs-lookup"><span data-stu-id="f04ae-131">Download a robots.txt file</span></span>

<span data-ttu-id="f04ae-132">Bir robots.txt dosyasını ticari olarak indirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f04ae-133">Commerce'te sistem yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="f04ae-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="f04ae-134">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).</span><span class="sxs-lookup"><span data-stu-id="f04ae-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="f04ae-135">**Kiracı ayarları** altında **robots.txt** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="f04ae-136">Ortamınız ile ilişkilendirilmiş tüm etki alanlarının listesi pencerenin ana bölümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f04ae-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="f04ae-137">Ortamınızdaki bir etki alanı için robots.txt dosyası indirmek için **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="f04ae-138">Sağdaki menüde, robots.txt dosyasıyla ilişkilendirilmiş etki alanının yanında bulunan **İndir** düğmesini (aşağı yönlü ok) seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="f04ae-139">Bir dosya tarayıcısı iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f04ae-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="f04ae-140">İletişim kutusunda, yerel sürücünüzde istediğiniz konuma gidin, bir dosya adı doğrulayın veya girin ve karşıdan yüklemeyi tamamlamak için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="f04ae-141">Bu yordam, daha önce Commerce geliştirme araçlarıyla karşıya yüklenen robots.txt dosyalarını karşıdan yüklemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f04ae-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="f04ae-142">Robots.txt dosyasını silme</span><span class="sxs-lookup"><span data-stu-id="f04ae-142">Delete a robots.txt file</span></span>

<span data-ttu-id="f04ae-143">Bir robots.txt dosyasını ticari olarak silmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f04ae-144">Commerce'te sistem yöneticisi olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="f04ae-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="f04ae-145">Sol gezinti bölmesinde, genişletmek için **Kiracı Ayarlarını** seçin (dişli simgesinin yanında).</span><span class="sxs-lookup"><span data-stu-id="f04ae-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="f04ae-146">**Kiracı ayarları** altında **robots.txt** dosyasını seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="f04ae-147">Ortamınız ile ilişkilendirilmiş tüm etki alanlarının listesi pencerenin ana bölümünde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f04ae-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="f04ae-148">Ortamınızdaki bir etki alanı için robots.txt dosyası silmek için **Yönet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="f04ae-149">Sağdaki menüde, robots.txt dosyasıyla ilişkilendirilmiş etki alanının yanında bulunan **Sil** düğmesini (çöp kutusu simgesi) seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="f04ae-150">Bir dosya tarayıcı penceresi görünür.</span><span class="sxs-lookup"><span data-stu-id="f04ae-150">A file browser window appears.</span></span>
6. <span data-ttu-id="f04ae-151">Dosya tarayıcı penceresinde, ilişkili etki alanı için silmek istediğiniz robots.txt dosyasını bulup seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="f04ae-152">Bir uyarı iletisi kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f04ae-152">A warning message box appears.</span></span>
7. <span data-ttu-id="f04ae-153">Robots.txt dosyasının silinmesini onaylamak için, ileti kutusunda, **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f04ae-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="f04ae-154">Bu yordam, daha önce Commerce geliştirme araçlarıyla karşıya yüklenen robots.txt dosyalarını silmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f04ae-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f04ae-155">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f04ae-155">Additional resources</span></span>

[<span data-ttu-id="f04ae-156">Etki alanı adınızı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f04ae-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="f04ae-157">Yeni bir e-ticaret kiracısını dağıtma</span><span class="sxs-lookup"><span data-stu-id="f04ae-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="f04ae-158">E-ticaret sitesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f04ae-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="f04ae-159">Dynamics 365 Commerce sitesini çevrimiçi bir kanalla ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="f04ae-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="f04ae-160">URL yeniden yönlendirmelerini toplu olarak yükleme</span><span class="sxs-lookup"><span data-stu-id="f04ae-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="f04ae-161">Commerce'ta B2C kiracısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="f04ae-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="f04ae-162">Kullanıcı oturum açma işlemleri için özel sayfalar ayarlama</span><span class="sxs-lookup"><span data-stu-id="f04ae-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="f04ae-163">Commerce ortamında birden fazla B2C kiracısı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f04ae-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="f04ae-164">İçerik teslim ağı (CDN) için destek ekleme</span><span class="sxs-lookup"><span data-stu-id="f04ae-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="f04ae-165">Konum tabanlı mağaza algılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f04ae-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
