---
title: POS'ta URL Aç
description: Bu konu Microsoft Dynamics 365 for Retail içinde ürün ve müşteri arama özelliğinde yapılmış olan iyileştirmeler hakkında genel bakış sağlar.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 729caf9fad9097a3ecbf7d546c8f8a96f67aec92
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845703"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="dada0-103">URL'yi POS'ta açma</span><span class="sxs-lookup"><span data-stu-id="dada0-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dada0-104">Bu konu, Retail point of sale (POS) içerisinde bir URL açmak için bir düğme yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="dada0-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="dada0-105">Bu özellik bir kod özelleştirme gerektirmez ve geliştirici rolünde olmayan bir kişi tarafından yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="dada0-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> <span data-ttu-id="dada0-106">Bu özellik, Dynamics 365 for Finance and Operations sürüm 8.1.3 sürümünün (yapı 8.1.227.10014) ve sonrasının parçası olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dada0-106">This feature is available as part of the Dynamics 365 for Finance and Operations version 8.1.3 release (build 8.1.227.10014) and later.</span></span> 

<span data-ttu-id="dada0-107">Bu özellik, POS'ta bir düğmenin bir URL açmak için düğme kılavuzu tasarımcısı kullanılarak yapılandırılmasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="dada0-107">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="dada0-108">Şu anda, bu aşağıdaki yapılandırmalarda desteklenmektedir:</span><span class="sxs-lookup"><span data-stu-id="dada0-108">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="dada0-109">Yeni pencerede aç.</span><span class="sxs-lookup"><span data-stu-id="dada0-109">Open in new window.</span></span>
- <span data-ttu-id="dada0-110">POS içinde açın.</span><span class="sxs-lookup"><span data-stu-id="dada0-110">Open within POS.</span></span>
- <span data-ttu-id="dada0-111">Yerel bir uygulama açın.</span><span class="sxs-lookup"><span data-stu-id="dada0-111">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="dada0-112">Yeni pencerede aç</span><span class="sxs-lookup"><span data-stu-id="dada0-112">Open in new window</span></span>

<span data-ttu-id="dada0-113">Bu yapılandırma, bir URL'nin yeni bir pencerede mi yoksa uygulama içinde mi açılacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="dada0-113">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="dada0-114">Bir web URL'sini uygulama içinde açmak üzere yapılandırıldığında, POS'un yan gezinti paneli ve üst çubuğu, kullanıcı etkileşimine görünür ve kullanılabilir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="dada0-114">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="dada0-115">Yeni bir pencerede açılmak üzere yapılandırıldığında, URL Modern POS for Windows içerisinde yeni bir uygulama penceresinde veya tüm diğer POS istemcilerinde yeni bir tarayıcı sekmesinde açılır.</span><span class="sxs-lookup"><span data-stu-id="dada0-115">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="dada0-116">Bunu etkinleştirmek için **Yeni pencerede aç** seçeneği seçiliyken URL'yi yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="dada0-116">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="dada0-117">POS içinde açın</span><span class="sxs-lookup"><span data-stu-id="dada0-117">Open within POS</span></span>

<span data-ttu-id="dada0-118">POS içerisinde bir web URL'sini açmak şu anda yalnızca Modern POS on Windows'ta desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="dada0-118">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="dada0-119">Diğer istemciler üzerinde, bu yeterlilik geliştirme altındadır ve gelecek güncelleştirmeler için planlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dada0-119">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="dada0-120">Bunu etkinleştirmek için **Yeni pencerede aç** seçeneği seçili değilken URL'yi yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="dada0-120">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="dada0-121">Yerel bir uygulama açın</span><span class="sxs-lookup"><span data-stu-id="dada0-121">Open a native app</span></span>

<span data-ttu-id="dada0-122">Bu özellik, web URL'si olmayanları da yerel uygulamada açmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="dada0-122">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="dada0-123">Örneğin, MailTo, SIP, IM veya MSTEAMS gibi URL protokollerini belirtebilirsiniz, bu sayede bunlar ana cihazdaki bunlara karşılık gelen uygulamalar tarafından ele alınabilir.</span><span class="sxs-lookup"><span data-stu-id="dada0-123">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="dada0-124">Bunu etkinleştirmek için **Yeni pencerede aç** seçeneği seçiliyken URL'yi yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="dada0-124">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="dada0-125">Windows bilgisayarlarda Deployment Image Servicing and Management (DISM) kullanarak bilgisayarınızı ayarlıyorsanız, varsayılan protokol ilişkilendirmelerini ayarlamak için bkz [Varsayılan Uygulama İlişkilendirmelerini İçe veya Dışa Aktarma](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)</span><span class="sxs-lookup"><span data-stu-id="dada0-125">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="dada0-126">Windows bilgisayarlarınızı yönetmek için Intune gibi bir MDM kullanıyorsanız, bkz. [Policy CSP ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="dada0-126">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="dada0-127">Özel bir web sitesi kurmakta olan bir geliştiriciyseniz bkz [Bir URI için varsayılan uygulamayı çalıştırmak](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="dada0-127">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="dada0-128">Yerel bir uygulamayı sorunsuzca açın</span><span class="sxs-lookup"><span data-stu-id="dada0-128">Open a native app seamlessly</span></span>

<span data-ttu-id="dada0-129">Windows, iOS ve Android, uygulama protokolü ilişkilendirmelerine dayanarak uygulamaların daha pürüzsüzce açılmasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="dada0-129">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="dada0-130">Uygulamanız bir web tarayıcısından açılmak için halihazırda yapılandırılmamışsa, bunun yapılandırılması için bir geliştiriciye ihtiyaç duyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dada0-130">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="dada0-131">Windows için bkz. [Uygulama URI işleyicileri kullanarak web siteleri için uygulamaları etkinleştirmek](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="dada0-131">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="dada0-132">iOS bkz. [Geliştiriciler için Evrensel Bağlantılar](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="dada0-132">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="dada0-133">Android için bkz. [Android Uygulama Bağlantılarını işlemek](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="dada0-133">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="dada0-134">İstemci</span><span class="sxs-lookup"><span data-stu-id="dada0-134">Client</span></span>                | <span data-ttu-id="dada0-135">Yeni pencerede aç</span><span class="sxs-lookup"><span data-stu-id="dada0-135">Open in new window</span></span> | <span data-ttu-id="dada0-136">Yerel uygulama açın</span><span class="sxs-lookup"><span data-stu-id="dada0-136">Open native app</span></span> | <span data-ttu-id="dada0-137">POS içinde açın</span><span class="sxs-lookup"><span data-stu-id="dada0-137">Open within POS</span></span> | <span data-ttu-id="dada0-138">Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="dada0-138">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="dada0-139">Modern POS on Windows</span><span class="sxs-lookup"><span data-stu-id="dada0-139">Modern POS on Windows</span></span> | <span data-ttu-id="dada0-140">✓\*</span><span class="sxs-lookup"><span data-stu-id="dada0-140">✓\*</span></span>                | <span data-ttu-id="dada0-141">✓</span><span class="sxs-lookup"><span data-stu-id="dada0-141">✓</span></span>               | <span data-ttu-id="dada0-142">✓</span><span class="sxs-lookup"><span data-stu-id="dada0-142">✓</span></span>              | <span data-ttu-id="dada0-143">\* Yeni Modern POS penceresinde açar</span><span class="sxs-lookup"><span data-stu-id="dada0-143">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="dada0-144">Bulut POS</span><span class="sxs-lookup"><span data-stu-id="dada0-144">Cloud POS</span></span>             | <span data-ttu-id="dada0-145">✓\*</span><span class="sxs-lookup"><span data-stu-id="dada0-145">✓\*</span></span>                | <span data-ttu-id="dada0-146">✓</span><span class="sxs-lookup"><span data-stu-id="dada0-146">✓</span></span>               | <span data-ttu-id="dada0-147">X</span><span class="sxs-lookup"><span data-stu-id="dada0-147">X</span></span>              | <span data-ttu-id="dada0-148">\* Yeni tarayıcı sekmesinde açar</span><span class="sxs-lookup"><span data-stu-id="dada0-148">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="dada0-149">Modern POS on iOS</span><span class="sxs-lookup"><span data-stu-id="dada0-149">Modern POS on iOS</span></span>     | <span data-ttu-id="dada0-150">✓\*</span><span class="sxs-lookup"><span data-stu-id="dada0-150">✓\*</span></span>                | <span data-ttu-id="dada0-151">✓</span><span class="sxs-lookup"><span data-stu-id="dada0-151">✓</span></span>               | <span data-ttu-id="dada0-152">X</span><span class="sxs-lookup"><span data-stu-id="dada0-152">X</span></span>              | <span data-ttu-id="dada0-153">\* Yeni tarayıcı sekmesinde açar</span><span class="sxs-lookup"><span data-stu-id="dada0-153">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="dada0-154">Modern POS on Android</span><span class="sxs-lookup"><span data-stu-id="dada0-154">Modern POS on Android</span></span> | <span data-ttu-id="dada0-155">✓\*</span><span class="sxs-lookup"><span data-stu-id="dada0-155">✓\*</span></span>                | <span data-ttu-id="dada0-156">✓</span><span class="sxs-lookup"><span data-stu-id="dada0-156">✓</span></span>               | <span data-ttu-id="dada0-157">X</span><span class="sxs-lookup"><span data-stu-id="dada0-157">X</span></span>              | <span data-ttu-id="dada0-158">\* Yeni tarayıcı sekmesinde açar</span><span class="sxs-lookup"><span data-stu-id="dada0-158">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="dada0-159">Başlamadan önce</span><span class="sxs-lookup"><span data-stu-id="dada0-159">Before you begin</span></span>

<span data-ttu-id="dada0-160">Başlamadan önce, nasıl yapılandırılacağını gözden geçirin [Satış noktası (POS) için ekran düzenleri](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="dada0-160">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="dada0-161">POS'ta URL Aç</span><span class="sxs-lookup"><span data-stu-id="dada0-161">Open URL in POS</span></span>

<span data-ttu-id="dada0-162">Bir URL'nin POS içinde açılmasını yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dada0-162">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="dada0-163">Ana ofiste, **Perakende \> Kanal Kurulumu \> POS Kurulumu \> POS \> Ekran Düzenleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="dada0-163">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="dada0-164">**Düğme Grupları \> Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="dada0-164">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="dada0-165">Yeni bir düğme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dada0-165">Create a new button.</span></span>
4. <span data-ttu-id="dada0-166">**Düğme** nitelikleri seçin.</span><span class="sxs-lookup"><span data-stu-id="dada0-166">Select **Button** properties.</span></span>
5. <span data-ttu-id="dada0-167">**URL Aç**'ı eylem olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="dada0-167">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="dada0-168">Kullanmak istediğiniz URL'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dada0-168">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="dada0-169">URL'nin yeni pencerede açılmasını isteyip istemediğinizi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="dada0-169">Configure whether to open the URL in a new window.</span></span>
