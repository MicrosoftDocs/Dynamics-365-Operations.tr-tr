---
title: Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme
description: Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154098"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="85f1f-103">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="85f1f-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="85f1f-104">Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="85f1f-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="85f1f-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="85f1f-105">Overview</span></span>

<span data-ttu-id="85f1f-106">Müşterilerinizin sitem ile nasıl etkileştiğini anlamak ve maksimum dönüştürme deneyimini en iyi duruma getirmeye yardımcı olacak kararlar vermek istediğinizde, Web analizi önemli bir araçtır.</span><span class="sxs-lookup"><span data-stu-id="85f1f-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="85f1f-107">Birçok web analizi paketi, Google Analytics, Click, Moz Analytics ve KISSMetrics gibi bu hedeflere ulaşmanıza yardımcı olacak şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="85f1f-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="85f1f-108">Çoğu Web analizi paketi, sitenizin tüm sayfaları için HTML'nin **\<baş\>** öğesine istemci tarafı kodu eklemenizi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="85f1f-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="85f1f-109">Bu konudaki yönergeler, Microsoft Dynamics 365 Commerce'un doğal olarak sunmadığı diğer özel istemci tarafı işlevleri için de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="85f1f-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="85f1f-110">Komut dosyası kodunuz için yeniden kullanılabilir sayfa parça oluşturun</span><span class="sxs-lookup"><span data-stu-id="85f1f-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="85f1f-111">Sayfa parçası, kendi kullandıkları şablondan bağımsız olarak, sitenizdeki tüm sayfalar arasında satır içi veya harici kod kodunu yeniden kullanmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="85f1f-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="85f1f-112">Satır içi Komut dosyası kodunuz için yeniden kullanılabilir sayfa parça oluşturun</span><span class="sxs-lookup"><span data-stu-id="85f1f-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="85f1f-113">Site oluşturucuda satır içi betik kodunuz için yeniden kullanılabilir bir sayfa parçası oluşturmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85f1f-114">**Sayfa Parçalarına** gidin ve **yeni**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-114">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="85f1f-115">**Yeni sayfa parçası** iletişim kutusunda, **satır içi betik** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-115">In the **New Page Fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="85f1f-116">**Sayfa parçası adı** altında, parça için bir ad girin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-116">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="85f1f-117">Oluşturduğunuz sayfa parçasının altında, **varsayılan satır içi kod** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="85f1f-118">Özellik bölmesinde, **satır içi komut dosyası** altında, istemci tarafı komut dosyanızı girin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="85f1f-119">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="85f1f-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="85f1f-120">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85f1f-121">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="85f1f-122">Harici Komut dosyası kodunuz için yeniden kullanılabilir sayfa parça oluşturun</span><span class="sxs-lookup"><span data-stu-id="85f1f-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="85f1f-123">Site oluşturucuda sharici betik kodunuz için yeniden kullanılabilir bir sayfa parçası oluşturmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85f1f-124">**Sayfa Parçalarına** gidin ve **yeni**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-124">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="85f1f-125">**Yeni sayfa parçası** iletişim kutusunda, **Harici betik** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-125">In the **New Page Fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="85f1f-126">**Sayfa parçası adı** altında, parça için bir ad girin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-126">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="85f1f-127">Oluşturduğunuz sayfa parçasının altında, **varsayılan harici kod** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="85f1f-128">Sağdaki Özellik bölmesinde, **komut dosyası kaynağı** altında, harici komut dosyası kaynağı için HARICI veya göreli bir URL ekleyin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="85f1f-129">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="85f1f-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="85f1f-130">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85f1f-131">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="85f1f-132">Bir şablona kod kodu içeren bir sayfa parçası ekler</span><span class="sxs-lookup"><span data-stu-id="85f1f-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="85f1f-133">Site oluşturucuda şablona komut kodu dahil eden bir sayfa parçası eklemek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85f1f-134">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="85f1f-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="85f1f-135">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="85f1f-136">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Sayfa parçası Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="85f1f-137">Kodunuz için oluşturduğunuz parçayı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="85f1f-138">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85f1f-139">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="85f1f-140">Bir şablona doğrudan harici bir komut dosyası veya satıriçi komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="85f1f-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="85f1f-141">Bir satır içi veya harici bir kodu, tek bir şablon tarafından denetlenen bir sayfa kümesine doğrudan eklemek istiyorsanız, önce sayfa parçası oluşturmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="85f1f-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="85f1f-142">Bir şablona doğrudan satıriçi komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="85f1f-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="85f1f-143">Site oluşturucuda bir şablona doğrudan satır içi komut dosyası eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85f1f-144">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="85f1f-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="85f1f-145">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="85f1f-146">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="85f1f-147">**Modül ekle** iletişim kutusunda, **satır içi betik** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="85f1f-148">Özellik bölmesinde, **satır içi komut dosyası** altında, istemci tarafı komut dosyanızı girin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="85f1f-149">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="85f1f-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="85f1f-150">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85f1f-151">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="85f1f-152">Bir şablona doğrudan harici komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="85f1f-152">Add an external script directly to a template</span></span>

<span data-ttu-id="85f1f-153">Site oluşturucuda bir şablona doğrudan harici komut dosyası eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="85f1f-154">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="85f1f-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="85f1f-155">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="85f1f-156">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="85f1f-157">**Modül ekle** iletişim kutusunda, **Harici betik** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="85f1f-158">Sağdaki Özellik bölmesinde, **komut dosyası kaynağı** altında, harici komut dosyası kaynağı için HARICI veya göreli bir URL ekleyin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="85f1f-159">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="85f1f-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="85f1f-160">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="85f1f-161">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="85f1f-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85f1f-162">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="85f1f-162">Additional resources</span></span>

[<span data-ttu-id="85f1f-163">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="85f1f-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="85f1f-164">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="85f1f-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="85f1f-165">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="85f1f-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="85f1f-166">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="85f1f-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="85f1f-167">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="85f1f-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="85f1f-168">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="85f1f-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="85f1f-169">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="85f1f-169">Add languages to your site</span></span>](add-languages-to-site.md)
