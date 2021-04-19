---
title: CSS geçersiz kılma dosyalarıyla çalışma
description: Bu konu, Microsoft Dynamics 365 Commerce'te geçişli stil sayfalarının (CSS) nasıl geçersiz kılındığını, ne zaman ve nasıl kullanılacağını açıklamaktadır.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ef96070fe77b46622667301c7c7c402909ee7dfc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799505"
---
# <a name="work-with-css-override-files"></a><span data-ttu-id="f3820-103">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="f3820-103">Work with CSS override files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f3820-104">Bu konu, Microsoft Dynamics 365 Commerce'te geçişli stil sayfalarının (CSS) nasıl geçersiz kılındığını, ne zaman ve nasıl kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f3820-104">This topic describes why, when, and how to use Cascading Style Sheets (CSS) override files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f3820-105">Kalıcı site stilleri genellikle sitenin teması üzerinden işlenmelidir.</span><span class="sxs-lookup"><span data-stu-id="f3820-105">Permanent site styles should usually be handled through a site's theme.</span></span> <span data-ttu-id="f3820-106">Temalar, sitenizin herhangi bir sayfasında modüller için temel CSS ve stil ayarlarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="f3820-106">Themes provide the foundational CSS and style settings for the modules on any page of your site.</span></span> <span data-ttu-id="f3820-107">Temalar, Dynamics 365 Commerce çevrimiçi yazılım geliştirme SETI (SDK) kullanılarak oluşturulur ve bunlar Web siteleriniz ile Microsoft Dynamics Lifecycle Services (LCS) aracılığıyla dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="f3820-107">Themes are created by using the Dynamics 365 Commerce online software development kit (SDK), and they are deployed to your websites through Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="f3820-108">SDK yardımda Tema hata ayıklama özellikleri ve modül arabirim yapılandırmaları özelleştirilebilir ve ortaklaşa bulunmayan site tasarım paketleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3820-108">Theme debugging capabilities and module interface configurations in the SDK help site developers create customizable and cohesive site design packages.</span></span> <span data-ttu-id="f3820-109">Bu tasarım paketleri bir siteye dağıtıldığında, Site yazarları, site geliştirme yerine içerik oluşturma, düzenleme ve yayımlama işlemlerinde yoğunlaşabilir.</span><span class="sxs-lookup"><span data-stu-id="f3820-109">When these design packages are deployed to a site, site authors can focus on creating, editing, and publishing content instead of site development.</span></span>

<span data-ttu-id="f3820-110">Bir temanın normal ömrü verildiğinde, SDK ve LCS dağıtım ardışık düzeninde stil değişiklikleri yapmak amacıyla geliştiricilerin bağımlılığı bazı senaryolarda potansiyel olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="f3820-110">Given the usual lifecycle of a theme, the dependency on developers to make style changes through the SDK and LCS deployment pipeline can be prohibitive in some scenarios.</span></span> <span data-ttu-id="f3820-111">SDK yapılandırılmamışsa veya LCS dağıtımını beklemek için bir zaman kalmazsa, site prototipleri veya düzeltmeleri bir miktar görünebilir.</span><span class="sxs-lookup"><span data-stu-id="f3820-111">Site prototypes or hotfixes can seem cumbersome if the SDK isn't configured, or if you don't have time to wait for an LCS deployment.</span></span>

<span data-ttu-id="f3820-112">Bu senaryolarda, CSS dosyaları geçersiz kılma yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f3820-112">In these scenarios, CSS override files can help.</span></span> <span data-ttu-id="f3820-113">Commerce geliştirme araçlarında, kimliği doğrulanmış kullanıcılar bir CSS dosyayı karşıya yükleyebilir, önizleyebilir ve böylece sitenin temasını geçersiz kılmak için etkinleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="f3820-113">In the Commerce authoring tools, authenticated users can upload a CSS file, preview it, and then activate it to override a site's theme.</span></span> <span data-ttu-id="f3820-114">SDK veya LCS dağıtımının ek yükü gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="f3820-114">The overhead of SDK or LCS deployment isn't required.</span></span> <span data-ttu-id="f3820-115">CSS geçersiz kılma dosyasında belirtilen geçersiz kılmalar tek bir metin stilinde yapılan bir değişikliğe veya eksiksiz bir marka yelpazesinin geniş kapsamlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f3820-115">The overrides that are specified in a CSS override file can be as small as a change to a single text style or as wide-ranging as a complete brand overhaul.</span></span>

<span data-ttu-id="f3820-116">Dosyaları CSS geçersiz kılma işleminden önce, aşağıdaki sınırlamaları göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="f3820-116">Before you use CSS override files, be aware of the following limitations:</span></span>

- <span data-ttu-id="f3820-117">Aynı anda CSS bir sitede yalnızca bir geçersiz kılma dosyası etkin olabilir.</span><span class="sxs-lookup"><span data-stu-id="f3820-117">Only one CSS override file can be active on a site at a time.</span></span> <span data-ttu-id="f3820-118">Bu nedenle, tüm etkin geçersiz kılmalar tek bir geçersiz kılma dosyasında bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f3820-118">Therefore, all active overrides must be present in a single override file.</span></span>
- <span data-ttu-id="f3820-119">Geçersiz kılmaları Commerce geliştirme araçlarında önizleme yapabilseniz de, geçersiz kılmaların tanıtan hataları tanımlamaya yardımcı olan adanmış hata ayıklama özellikleri bulunmamaktadır.</span><span class="sxs-lookup"><span data-stu-id="f3820-119">Although you can preview the overrides in the Commerce authoring tools, there are no dedicated debugging features to help identify any bugs that the overrides introduce.</span></span> <span data-ttu-id="f3820-120">Başka bir deyişle, dosyaları CSS geçersiz kılma işlemini kullandığınızda, modül ve yazma doğrulaması için SDK'nın sağladığı araç takımı ile aynı olmaz.</span><span class="sxs-lookup"><span data-stu-id="f3820-120">In other words, when you use CSS override files, you don't have the same toolset that the SDK provides for module and authoring validation.</span></span>

<span data-ttu-id="f3820-121">Bununla birlikte CSS, dosyaları geçersiz kıl, bir tasarımı prototip almanın veya tam tema güncelleştirmesi geliştirip dağıtılmadan önce bir düzeltme uygulamaya yönelik olarak hızlı bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="f3820-121">Nevertheless, CSS override files provide a quick way to prototype a design or implement a hotfix before a full theme update is developed and deployed.</span></span>

## <a name="create-a-css-override-file"></a><span data-ttu-id="f3820-122">Bir CSS geçersiz kılma dosyası oluştur</span><span class="sxs-lookup"><span data-stu-id="f3820-122">Create a CSS override file</span></span>

<span data-ttu-id="f3820-123">CSS geçersiz kılma dosyası oluşturmak için herhangi bir tümleşik geliştirme ortamı (IDE), metin düzenleyicisi veya kaynak kodu düzenleyicisi kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3820-123">To create a CSS override file, you can use any integrated development environment (IDE), text editor, or source code editor.</span></span> <span data-ttu-id="f3820-124">Normal bir yaklaşım, varolan sitenizdeki stil seçicileri, özellikleri ve değerleri tanımlamak için tarayıcınızda standart Web hata ayıklayıcıları kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="f3820-124">A typical approach is to use standard web debuggers in your browser to identify style selectors, properties, and values on your existing site.</span></span> <span data-ttu-id="f3820-125">Birçok tarayıcı değerleri değiştirmenize ve hata ayıklayıcıda önizlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="f3820-125">Most browsers let you change values and preview them in the debugger.</span></span> <span data-ttu-id="f3820-126">Yapmak istediğiniz değişiklikleri tanımladıktan sonra, onları kendi CSS dosyanıza kaydedebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3820-126">After you've identified the changes that you want to make, you can save them to your own CSS file.</span></span>

## <a name="upload-a-css-override-file"></a><span data-ttu-id="f3820-127">CSS geçersiz kılma dosyası yükle</span><span class="sxs-lookup"><span data-stu-id="f3820-127">Upload a CSS override file</span></span>

<span data-ttu-id="f3820-128">Bir CSS dosyasını Commerce'te sitenize yüklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f3820-128">To upload a CSS file to your site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="f3820-129">Düzenleme araçlarında sitenize gidin.</span><span class="sxs-lookup"><span data-stu-id="f3820-129">In the authoring tools, go to your site.</span></span>
1. <span data-ttu-id="f3820-130">Soldaki gezinti bölmesinde **Tasarımcı** seçin.</span><span class="sxs-lookup"><span data-stu-id="f3820-130">In the navigation pane on the left, select **Design**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f3820-131">Kullanmakta olduğunuz Commerce geliştirme araçlarının sürümüne bağlı olarak, **tasarımcı** seçmeden önce gezinti bölmesindeki **ayarları** genişletmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="f3820-131">Depending on the version of the Commerce authoring tools that you're using, you might have to expand **Settings** in the navigation pane before you can select **Design**.</span></span>

1. <span data-ttu-id="f3820-132">Ana tasarım bölmesinin en üstünde, henüz seçilmemişse, **CSS geçersiz kıl** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f3820-132">At the top of the main design pane, select the **CSS override** tab, if it isn't already selected.</span></span>
1. <span data-ttu-id="f3820-133">**Kullanılabilir CSS geçersiz kılmalar** altında, **CSS dosyasını karşıya yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f3820-133">Under **Available CSS overrides**, select **Upload CSS file**.</span></span> <span data-ttu-id="f3820-134">Bir Dosya Gezgini penceresi görünür.</span><span class="sxs-lookup"><span data-stu-id="f3820-134">A File Explorer window appears.</span></span>
1. <span data-ttu-id="f3820-135">Dosya Gezgininde, CSS dosyaya gözatın ve dosyayı seçin ve sonra **Aç**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3820-135">In File Explorer, browse to and select a CSS file, and then select **Open**.</span></span> <span data-ttu-id="f3820-136">Karşıya yüklenen CSS dosya artık **mevcut CSS geçersiz kılmalar** altında görünür.</span><span class="sxs-lookup"><span data-stu-id="f3820-136">The uploaded CSS file now appears under **Available CSS overrides**.</span></span>

## <a name="preview-a-css-override-file"></a><span data-ttu-id="f3820-137">CSS geçersiz kılma dosyasını önizlemede görüntüleme</span><span class="sxs-lookup"><span data-stu-id="f3820-137">Preview a CSS override file</span></span>

<span data-ttu-id="f3820-138">CSS geçersiz kılma dosyasını, canlı sitenizde etkin hale getirmek üzere önizlemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f3820-138">To preview a CSS override file before you make it active on your live site, follow these steps.</span></span>

1. <span data-ttu-id="f3820-139">Sol taraftaki gezinme bölmesinde, **tasarım**'ı seçin ve sonra **CSS geçersiz kılma** sekmesinde, kullanılabilir **CSS geçersiz kılmalar** altında önizlemek istediğiniz CSS dosyayı bulun.</span><span class="sxs-lookup"><span data-stu-id="f3820-139">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to preview.</span></span>
1. <span data-ttu-id="f3820-140">CSS dosya adının yanında **önizleme sitesi** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f3820-140">Next to the CSS file name, select **Preview site**.</span></span>
1. <span data-ttu-id="f3820-141">**URL Seç** iletişim kutusunda, geçersiz kılmanın uygulanmasını görmek istediğiniz sitenin URL 'sini seçin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3820-141">In the **Select a URL** dialog box, select the URL of the site that you want to see the override applied to, and then select **OK**.</span></span>
1. <span data-ttu-id="f3820-142">Seçili URL'nin birden çok çeşidi varsa, görüntülenen **önizleme çeşitlemeleri** iletişim kutusunda istediğiniz değişkeni seçin.</span><span class="sxs-lookup"><span data-stu-id="f3820-142">If there are multiple variants for the selected URL, select the desired variant in the **Preview variations** dialog box that appears.</span></span>

<span data-ttu-id="f3820-143">Kendi stilinize karşı stilinizi doğrulayabileceğiniz yeni bir tarayıcı sekmesi veya penceresi açılır.</span><span class="sxs-lookup"><span data-stu-id="f3820-143">A new browser tab or window is opened, where you can validate your style overrides against your site.</span></span> <span data-ttu-id="f3820-144">Daha sonra, URL'yi gözden geçirip görüş bildirme amacıyla diğer kimliği doğrulanmış Commerce kullanıcılarıyla paylaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3820-144">You can then share the URL with other authenticated Commerce users for review and feedback.</span></span>

## <a name="activate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="f3820-145">Canlı sitenizdeki CSS bir geçersiz kılma dosyasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f3820-145">Activate a CSS override file on your live site</span></span>

<span data-ttu-id="f3820-146">CSS geçersiz kılma dosyasını önizledikten ve onayladıktan sonra, calı sitenizde etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3820-146">After you've previewed and approved the CSS override file, you can activate it on your live site.</span></span>

> [!NOTE]
> <span data-ttu-id="f3820-147">Aynı anda sitede yalnızca bir CSS geçersiz kılma dosyası etkin olabilir.</span><span class="sxs-lookup"><span data-stu-id="f3820-147">Only one CSS override file can be active on your site at a time.</span></span> <span data-ttu-id="f3820-148">Yeni bir geçersiz kılma dosyasını etkinleştirirseniz, önceki geçersiz kılma dosyası devre dışı demektir.</span><span class="sxs-lookup"><span data-stu-id="f3820-148">If you activate a new override file, the previous override file is inactivated.</span></span> <span data-ttu-id="f3820-149">Bu nedenle, tek bir CSS geçersiz kılma dosyasında gerekli tüm geçersiz kılmaların bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="f3820-149">Therefore, make sure that all required overrides are present in a single CSS override file.</span></span>

<span data-ttu-id="f3820-150">CSS geçersiz kılma dosyasını etkinleştirmek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f3820-150">To activate a CSS override file, follow these steps.</span></span>

1. <span data-ttu-id="f3820-151">Sol taraftaki gezinme bölmesinde, **tasarım**'ı seçin ve sonra **CSS geçersiz kılma** sekmesinde, kullanılabilir **CSS geçersiz kılmalar** altında etkinleştirmek istediğiniz CSS dosyayı bulun.</span><span class="sxs-lookup"><span data-stu-id="f3820-151">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to activate.</span></span>
1. <span data-ttu-id="f3820-152">CSS dosya adı altında **Etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3820-152">Under the CSS file name, select **Activate**.</span></span> <span data-ttu-id="f3820-153">Geçersiz kılma dosyası, canlı sitenizde hemen etkin hale gelir.</span><span class="sxs-lookup"><span data-stu-id="f3820-153">The override file immediately becomes active on your live site.</span></span>

## <a name="deactivate-a-css-override-file-on-your-live-site"></a><span data-ttu-id="f3820-154">Canlı sitenizdeki CSS bir geçersiz kılma dosyasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="f3820-154">Deactivate a CSS override file on your live site</span></span>

<span data-ttu-id="f3820-155">Sitenizdeki bir CSS geçersiz kılma dosyasını devre dışı bırakmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f3820-155">To deactivate a CSS override file on your site, follow these steps.</span></span>

1. <span data-ttu-id="f3820-156">Sol taraftaki gezinme bölmesinde, **tasarım**'ı seçin ve sonra **CSS geçersiz kılma** sekmesinde, kullanılabilir **CSS geçersiz kılmalar** altında devre dışı bırakmak istediğiniz CSS dosyayı bulun.</span><span class="sxs-lookup"><span data-stu-id="f3820-156">In the navigation pane on the left, select **Design**, and then, on the **CSS override** tab, under **Available CSS overrides**, find the CSS file that you want to deactivate.</span></span>
1. <span data-ttu-id="f3820-157">CSS dosya adı altında **Devre dışı bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3820-157">Under the CSS file name, select **Deactivate**.</span></span> <span data-ttu-id="f3820-158">Geçersiz kılma dosyası, canlı sitenizde hemen devre dışı hale gelir.</span><span class="sxs-lookup"><span data-stu-id="f3820-158">The override file immediately becomes inactive on your live site.</span></span>

> [!TIP]
> <span data-ttu-id="f3820-159">CSS geçersiz kılma dosyalarına ek seçeneklere erişmek için üç nokta (**...**) CSS dosya adının yanında.</span><span class="sxs-lookup"><span data-stu-id="f3820-159">To access additional options for CSS override files, select the ellipsis (**...**) next to the CSS file name.</span></span> <span data-ttu-id="f3820-160">**Karşıdan yükleme**, **yenidenadlandırma** ve **değiştirme** seçenekleri, varolan bir CSS geçersiz kılma dosyasında hızlı değişiklikler yapmak için yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="f3820-160">The **Download**, **Rename**, and **Replace** options are useful for quick changes to an existing CSS override file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3820-161">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f3820-161">Additional resources</span></span>

[<span data-ttu-id="f3820-162">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="f3820-162">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f3820-163">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="f3820-163">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="f3820-164">Stil ön ayarlarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="f3820-164">Work with style presets</span></span>](style-presets.md)

[<span data-ttu-id="f3820-165">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="f3820-165">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f3820-166">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="f3820-166">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f3820-167">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="f3820-167">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f3820-168">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="f3820-168">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f3820-169">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="f3820-169">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
