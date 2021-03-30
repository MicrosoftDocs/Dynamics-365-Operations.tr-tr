---
title: Gizlilik ilkesi sayfası ekle
description: Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize gizlilik ilkesi sayfası ekleme yöntemi açıklanmıştır.
author: v-chgri
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 07a806ac040df9dee284e2466629221fbc3403a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209287"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="c020e-103">Gizlilik ilkesi sayfası ekle</span><span class="sxs-lookup"><span data-stu-id="c020e-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c020e-104">Bu konuda, Microsoft Dynamics 365 Commerce'te sitenize gizlilik ilkesi sayfası ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c020e-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c020e-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="c020e-105">Overview</span></span>

<span data-ttu-id="c020e-106">Gizlilik uyumluluğu, site kullanıcılarını verilerinin nasıl toplanacağı ve işlendiği hakkında bilgi veren kuruluş önlemleri içerir.</span><span class="sxs-lookup"><span data-stu-id="c020e-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="c020e-107">Böylece kullanıcılar, kişisel verilerinin nasıl işleneceğini istediklerini ve gerekli eylemleri nasıl ele alabilirler.</span><span class="sxs-lookup"><span data-stu-id="c020e-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="c020e-108">Dynamics 365 Commerce'te Microsoft Gizlilik Bildirimini inceleyin</span><span class="sxs-lookup"><span data-stu-id="c020e-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="c020e-109">Dynamics 365 Commerce yazma araçlarına oturum açarken Microsoft gizlilik bildirimi'ni gözden geçirmek için, sağ üst köşedeki **Yardım** düğmesini (**?**) seçin ve sonra **Gizlilik ve tanımlama bilgileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="c020e-110">[Microsoft gizlilik bildirimi](https://privacy.microsoft.com/privacystatement)'ne bağlantı içeren yeni bir sekme açılır.</span><span class="sxs-lookup"><span data-stu-id="c020e-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="c020e-111">Siteniz için bir gizlilik ilkesi sayfası oluşturun</span><span class="sxs-lookup"><span data-stu-id="c020e-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="c020e-112">Dynamics 365 Commerce'te, sitenizi kullanıcılarına Gizlilik ilkenizin erişim izni vermenin birkaç yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="c020e-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="c020e-113">Bu bölümde Gizlilik ilkesi sayfasının nasıl oluşturulacağı ve altbilgi parçası kullanılarak sayfaya nasıl referans bulunduğu gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c020e-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="c020e-114">Aşağıdaki kılavuz, bir ticaret sitesi için genel gizlilik ilkesi sayfasının nasıl oluşturulacağını gösteren bir örnektir.</span><span class="sxs-lookup"><span data-stu-id="c020e-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="c020e-115">Şirketinizin yasal gereksinimlerini en iyi karşılayan Gizlilik ilkesi sayfası çözümü tasarlanırken ve uygulamadığınızdan sorumlusunuz.</span><span class="sxs-lookup"><span data-stu-id="c020e-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="c020e-116">Başlatmak için, yazma araçlarında, bir gizlilik ilkesi sayfası oluşturmak istediğiniz siteye gidin.</span><span class="sxs-lookup"><span data-stu-id="c020e-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="c020e-117">Şablon oluştur</span><span class="sxs-lookup"><span data-stu-id="c020e-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="c020e-118">Gizlilik ilkesi sayfası için kullanılabilecek bir şablon zaten oluşturulmuşsa, bir [gizlilik ilkesi sayfası oluştur](#build-a-privacy-policy-page) bölümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="c020e-119">Bir şablon oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="c020e-120">Bir sayfa şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-120">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="c020e-121">**Yeni Şablon** iletişim kutusunda **Şablon adı** altında, **Promosyon başlığı şablonu**'nu girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-121">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c020e-122">Şablonda, gerekli tüm sayfa yuvalarına gerekli modülleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="c020e-123">Kılavuz için kırmızı Ünlem işaretlerinin üzerine gelin.</span><span class="sxs-lookup"><span data-stu-id="c020e-123">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="c020e-124">(Örneğin, **HTML Başı** yuvası bir **Varsayılan Harici Komut Dosyası** modülü gerektirebilir.)</span><span class="sxs-lookup"><span data-stu-id="c020e-124">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="c020e-125">**Gövde** yuvasında bir **varsayılan sayfa** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="c020e-126">**Varsayılan sayfa** modülünde, **Ana** yuvasına bir **içerik zengin blok** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="c020e-127">**İçerik zengin blok** modülünde, bir **içerik zengin blok öğe** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="c020e-128">**Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-128">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="c020e-129">Gizlilik ilkesi sayfası oluştur</span><span class="sxs-lookup"><span data-stu-id="c020e-129">Build a privacy policy page</span></span>

<span data-ttu-id="c020e-130">Gizlilik ilkesi sayfası oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="c020e-131">**Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-131">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="c020e-132">**Şablon seç** iletişim kutusunda gizlilik ilkesi sayfası şablonunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-132">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="c020e-133">Bir sayfa adı ve sayfa URL'si girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-133">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="c020e-134">Yeni sayfanın **ana** yuvasına bir **içerik zengin blok** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="c020e-135">**İçerik zengin blok** modülünde, bir **içerik zengin blok öğe** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="c020e-136">**İçerik zengin blok** modülü Özellikler bölmesinde **Veri Kaynağı Ekle**'yi ve sonra da **Zengin Metin İçeriği**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="c020e-137">Zengin metin düzenleyicisinde, Gizlilik ilkesi sayfası için içerik girin.</span><span class="sxs-lookup"><span data-stu-id="c020e-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="c020e-138">Zengin metin Düzenleyicisini gerektiğinde tam ekran moduna genişletin.</span><span class="sxs-lookup"><span data-stu-id="c020e-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="c020e-139">İçeriği girmeyi bitirdiğinizde, Web tarayıcısında sayfayı önizlemek için **Önizleme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="c020e-140">Sayfa ve modül özelliklerine kalan tüm eklemeleri tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="c020e-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="c020e-141">**Kaydet**'i seçin, sayfayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="c020e-142">Gizlilik ve ilke sayfası için URL yayınlamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="c020e-143">**URL**'lere gidin ve Gizlilik ilkesi sayfasının URL'sini seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="c020e-144">Seçili URL'yi yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-144">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="c020e-145">Altbilgide Gizlilik ilkesi sayfasına bağlantı oluştur</span><span class="sxs-lookup"><span data-stu-id="c020e-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="c020e-146">Bir parçaya Gizlilik ilkesi sayfası için bağlantı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c020e-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="c020e-147">Bu şekilde, bir bağlantıyı paylaşabilir ve parçaya başvurarak birden fazla site sayfası arasında güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c020e-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="c020e-148">Bu örnek, bir altbilgi parçasına gizlilik ilkesi sayfası bağlantısının nasıl ekleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c020e-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="c020e-149">Alt bilgi parçasına bğalantı eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="c020e-150">**Parçalar**'a gidin ve yeni sayfa parçası oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-150">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="c020e-151">**Yeni parça** iletişim kutusunda, **Alt bilgi** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-151">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="c020e-152">**Parça adı** altında, parça için bir ad girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-152">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c020e-153">**Altbilgi kategorisi** yuvasında bir **alt bilgi öğesi** modülü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="c020e-153">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="c020e-154">Sağdaki özellikler bölmesinde, **Bağlantı metni**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-154">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="c020e-155">**Bağlantı metni** iletişim kutusunda, Gizlilik ilkesi sayfasının bağlantı metnini ve bağlantı hedefini girin ve **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c020e-155">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="c020e-156">Gizlilik ilkesi sayfasının URL'sini almak için, **sayfalar**'a gidin, Gizlilik ilkesi sayfasına gidin ve Özellikler bölmesinden URL'yi kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="c020e-156">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="c020e-157">**Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c020e-157">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="c020e-158">Parçanın önizlemesine bakın ve Gizlilik ilkesi sayfası bağlantısını sınayın.</span><span class="sxs-lookup"><span data-stu-id="c020e-158">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="c020e-159">Parça artık diğer site sayfaları için şablonda başvurulabilir.</span><span class="sxs-lookup"><span data-stu-id="c020e-159">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="c020e-160">Bu parçaya bir şablonun **altbilgi** modülünde referans olduğu zaman, bağlantı başvurusu bu şablon kullanılarak oluşturulan tüm sayfalarda görünür.</span><span class="sxs-lookup"><span data-stu-id="c020e-160">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c020e-161">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="c020e-161">Additional resources</span></span>

[<span data-ttu-id="c020e-162">Uyumluluğa genel bakış</span><span class="sxs-lookup"><span data-stu-id="c020e-162">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="c020e-163">Erişilebilirlik özellikleri ve yetenekleri</span><span class="sxs-lookup"><span data-stu-id="c020e-163">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="c020e-164">Tanımlama bilgisi uyumluluğu</span><span class="sxs-lookup"><span data-stu-id="c020e-164">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="c020e-165">İzlenen içerik değişiklikleriyle ilişkili kullanıcı kimliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="c020e-165">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]