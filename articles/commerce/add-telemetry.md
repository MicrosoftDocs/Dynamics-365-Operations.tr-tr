---
title: Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme
description: Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761261"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="336e3-103">Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="336e3-104">Bu konuda, istemci tarafı telemetri topluluğunu desteklemek üzere site sayfalarınıza istemci tarafında komut dosyası kodu ekleme yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="336e3-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="336e3-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="336e3-105">Overview</span></span>

<span data-ttu-id="336e3-106">Müşterilerinizin sitem ile nasıl etkileştiğini anlamak ve maksimum dönüştürme deneyimini en iyi duruma getirmeye yardımcı olacak kararlar vermek istediğinizde, Web analizi önemli bir araçtır.</span><span class="sxs-lookup"><span data-stu-id="336e3-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="336e3-107">Birçok web analizi paketi, Google Analytics, Click, Moz Analytics ve KISSMetrics gibi bu hedeflere ulaşmanıza yardımcı olacak şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="336e3-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="336e3-108">Çoğu web analizi paketi, sitenizin tüm sayfaları için HTML'nin **\<head\>** öğesine istemci tarafı kodu eklemenizi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="336e3-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="336e3-109">Bu konudaki yönergeler, Microsoft Dynamics 365 Commerce'un doğal olarak sunmadığı diğer özel istemci tarafı işlevleri için de geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="336e3-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="336e3-110">Komut dosyası kodunuz için yeniden kullanılabilir bir parça oluşturun</span><span class="sxs-lookup"><span data-stu-id="336e3-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="336e3-111">Parça, kendi kullandıkları şablondan bağımsız olarak, sitenizdeki tüm sayfalar arasında satır içi veya harici kod kodunu yeniden kullanmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="336e3-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="336e3-112">Satır içi Komut dosyası kodunuz için yeniden kullanılabilir parça oluşturma</span><span class="sxs-lookup"><span data-stu-id="336e3-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="336e3-113">Site oluşturucuda satır içi betik kodunuz için yeniden kullanılabilir bir parça oluşturmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="336e3-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="336e3-114">**Parçalar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="336e3-115">**Yeni parça** iletişim kutusunda, **Satır içi betik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="336e3-116">**Parça adı** altında, parça için bir ad girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="336e3-117">Oluşturduğunuz parçanın altında, **varsayılan satır içi kod** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="336e3-118">Özellik bölmesinde, **satır içi komut dosyası** altında, istemci tarafı komut dosyanızı girin.</span><span class="sxs-lookup"><span data-stu-id="336e3-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="336e3-119">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="336e3-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="336e3-120">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="336e3-121">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="336e3-122">Harici Komut dosyası kodunuz için yeniden kullanılabilir parça oluşturma</span><span class="sxs-lookup"><span data-stu-id="336e3-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="336e3-123">Site oluşturucuda harici betik kodunuz için yeniden kullanılabilir bir parça oluşturmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="336e3-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="336e3-124">**Parçalar**'a gidin ve **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="336e3-125">**Yeni parça** iletişim kutusunda, **Harici betik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="336e3-126">**Parça adı** altında, parça için bir ad girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="336e3-127">Oluşturduğunuz parçanın altında, **Varsayılan harici kod** modülünü seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="336e3-128">Sağdaki Özellik bölmesinde, **komut dosyası kaynağı** altında, harici komut dosyası kaynağı için HARICI veya göreli bir URL ekleyin.</span><span class="sxs-lookup"><span data-stu-id="336e3-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="336e3-129">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="336e3-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="336e3-130">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="336e3-131">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-131">Select **Publish**.</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="336e3-132">Bir şablona komut kodu içeren bir parça ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-132">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="336e3-133">Site oluşturucuda şablona komut kodu dahil eden bir parça eklemek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="336e3-133">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="336e3-134">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="336e3-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="336e3-135">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="336e3-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="336e3-136">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Parçası ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="336e3-137">Kodunuz için oluşturduğunuz parçayı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="336e3-138">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="336e3-139">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="336e3-140">Bir şablona doğrudan harici bir komut dosyası veya satıriçi komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="336e3-141">Bir satır içi veya harici bir kodu, tek bir şablon tarafından denetlenen bir sayfa kümesine doğrudan eklemek istiyorsanız, önce parça oluşturmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="336e3-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="336e3-142">Bir şablona doğrudan satıriçi komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="336e3-143">Site oluşturucuda bir şablona doğrudan satır içi komut dosyası eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="336e3-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="336e3-144">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="336e3-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="336e3-145">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="336e3-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="336e3-146">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="336e3-147">**Modül ekle** iletişim kutusunda, **satır içi betik** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="336e3-148">Özellik bölmesinde, **satır içi komut dosyası** altında, istemci tarafı komut dosyanızı girin.</span><span class="sxs-lookup"><span data-stu-id="336e3-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="336e3-149">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="336e3-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="336e3-150">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="336e3-151">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="336e3-152">Bir şablona doğrudan harici komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-152">Add an external script directly to a template</span></span>

<span data-ttu-id="336e3-153">Site oluşturucuda bir şablona doğrudan harici komut dosyası eklemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="336e3-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="336e3-154">**Şablonlara** gidin ve kodunuzu eklemek istediğiniz sayfaların şablonunu açın.</span><span class="sxs-lookup"><span data-stu-id="336e3-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="336e3-155">Sol bölmede, **HTML Baş** yuvasını göstermek için şablon hiyerarşisini genişletin.</span><span class="sxs-lookup"><span data-stu-id="336e3-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="336e3-156">**HTML Baş** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="336e3-157">**Modül ekle** iletişim kutusunda, **Harici betik** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="336e3-158">Sağdaki Özellik bölmesinde, **komut dosyası kaynağı** altında, harici komut dosyası kaynağı için HARICI veya göreli bir URL ekleyin.</span><span class="sxs-lookup"><span data-stu-id="336e3-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="336e3-159">Daha sonra, istediğiniz şekilde diğer seçenekleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="336e3-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="336e3-160">**Kaydet**i seçin ve sonra **Düzenlemeyi bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="336e3-161">**Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="336e3-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="336e3-162">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="336e3-162">Additional resources</span></span>

[<span data-ttu-id="336e3-163">Logo ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="336e3-164">Site teması seçme</span><span class="sxs-lookup"><span data-stu-id="336e3-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="336e3-165">CSS geçersiz kılma dosyalarıyla çalışma</span><span class="sxs-lookup"><span data-stu-id="336e3-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="336e3-166">Favicon ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="336e3-167">Hoş geldiniz iletisi ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="336e3-168">Telif hakkı bildirimi ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="336e3-169">Sitenize dil ekleme</span><span class="sxs-lookup"><span data-stu-id="336e3-169">Add languages to your site</span></span>](add-languages-to-site.md)
