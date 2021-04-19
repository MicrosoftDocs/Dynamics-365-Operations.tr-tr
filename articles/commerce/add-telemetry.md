---
title: Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme
description: Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797443"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="3315d-103">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3315d-104">Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3315d-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="3315d-105">Müşterilerinizin sitem ile nasıl etkileştiğini anlamak ve maksimum dönüştürme deneyimini en iyi duruma getirmeye yardımcı olacak kararlar vermek istediğinizde, Web analizi önemli bir araçtır.</span><span class="sxs-lookup"><span data-stu-id="3315d-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="3315d-106">Birçok web analizi paketi, Google Analytics, Click, Moz Analytics ve KISSMetrics gibi bu hedeflere ulaşmanıza yardımcı olacak şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3315d-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="3315d-107">Çoğu web analizi paketi, sitenizin tüm sayfaları için HTML'nin **\<head\>** öğesine istemci tarafı kodu eklemenizi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="3315d-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="3315d-108">Bu konudaki yönergeler, Microsoft Dynamics 365 Commerce'un doğal olarak sunmadığı diğer özel istemci tarafı işlevleri için de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="3315d-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="3315d-109">Komut dosyası kodunuz için yeniden kullanılabilir bir parça oluşturun</span><span class="sxs-lookup"><span data-stu-id="3315d-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="3315d-110">Parça, kendi kullandıkları şablondan bağımsız olarak, sitenizdeki tüm sayfalar arasında satır içi veya harici kod kodunu yeniden kullanmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="3315d-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="3315d-111">Satır içi Komut dosyası kodunuz için yeniden kullanılabilir parça oluşturma</span><span class="sxs-lookup"><span data-stu-id="3315d-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="3315d-112">Site oluşturucuda satır içi betik kodunuz için yeniden kullanılabilir bir parça oluşturmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3315d-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3315d-113">**Parçalar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="3315d-114">**Yeni parça** iletişim kutusunda, **Satır içi betik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="3315d-115">**Parça adı** altında, parça için bir ad girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="3315d-116">Oluşturduğunuz parçanın altında, **varsayılan satır içi kod** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="3315d-117">Özellik bölmesinde, **satır içi komut dosyası** altında, istemci tarafı komut dosyanızı girin.</span><span class="sxs-lookup"><span data-stu-id="3315d-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="3315d-118">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="3315d-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="3315d-119">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="3315d-120">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="3315d-121">Harici Komut dosyası kodunuz için yeniden kullanılabilir parça oluşturma</span><span class="sxs-lookup"><span data-stu-id="3315d-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="3315d-122">Site oluşturucuda harici betik kodunuz için yeniden kullanılabilir bir parça oluşturmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3315d-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3315d-123">**Parçalar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="3315d-124">**Yeni parça** iletişim kutusunda, **Harici betik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="3315d-125">**Parça adı** altında, parça için bir ad girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="3315d-126">Oluşturduğunuz parçanın altında, **Varsayılan harici kod** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="3315d-127">Sağdaki Özellik bölmesinde, **komut dosyası kaynağı** altında, harici komut dosyası kaynağı için HARICI veya göreli bir URL ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3315d-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="3315d-128">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="3315d-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="3315d-129">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="3315d-130">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="3315d-131">Siteniz için içerik güvenliği ilkesi (CSP) etkinse, tüm harici URL'lerin Commerce site oluşturucudaki **script-src** CSP yönergesine eklendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="3315d-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="3315d-132">Daha fazla bilgi için bkz. [İçerik Güvenlik İlkesini (CSP) yönetme](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="3315d-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="3315d-133">Bir şablona komut kodu içeren bir parça ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="3315d-134">Site oluşturucuda şablona komut kodu dahil eden bir parça eklemek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3315d-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3315d-135">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="3315d-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="3315d-136">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3315d-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="3315d-137">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Parçası ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="3315d-138">Kodunuz için oluşturduğunuz parçayı seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="3315d-139">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="3315d-140">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="3315d-141">Bir şablona doğrudan harici bir komut dosyası veya satıriçi komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="3315d-142">Bir satır içi veya harici bir kodu, tek bir şablon tarafından denetlenen bir sayfa kümesine doğrudan eklemek istiyorsanız, önce parça oluşturmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="3315d-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="3315d-143">Bir şablona doğrudan satıriçi komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="3315d-144">Site oluşturucuda bir şablona doğrudan satır içi komut dosyası eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3315d-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3315d-145">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="3315d-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="3315d-146">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3315d-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="3315d-147">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3315d-148">**Modül ekle** iletişim kutusunda, **satır içi betik** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="3315d-149">Özellik bölmesinde, **satır içi komut dosyası** altında, istemci tarafı komut dosyanızı girin.</span><span class="sxs-lookup"><span data-stu-id="3315d-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="3315d-150">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="3315d-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="3315d-151">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="3315d-152">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="3315d-153">Bir şablona doğrudan harici komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-153">Add an external script directly to a template</span></span>

<span data-ttu-id="3315d-154">Site oluşturucuda bir şablona doğrudan harici komut dosyası eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="3315d-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3315d-155">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="3315d-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="3315d-156">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3315d-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="3315d-157">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3315d-158">**Modül ekle** iletişim kutusunda, **Harici betik** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="3315d-159">Sağdaki Özellik bölmesinde, **komut dosyası kaynağı** altında, harici komut dosyası kaynağı için HARICI veya göreli bir URL ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3315d-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="3315d-160">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="3315d-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="3315d-161">**Kaydet** i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="3315d-162">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3315d-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3315d-163">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3315d-163">Additional resources</span></span>

[<span data-ttu-id="3315d-164">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3315d-165">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="3315d-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3315d-166">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="3315d-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="3315d-167">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="3315d-168">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="3315d-169">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="3315d-170">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="3315d-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
