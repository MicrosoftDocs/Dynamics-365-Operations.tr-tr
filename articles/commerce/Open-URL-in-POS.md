---
title: POS'ta URL Aç
description: Bu konuda Dynamics 365 Commerce'da ürün ve müşteri arama özelliğinde yapılmış olan iyileştirmelere genel bakış sunulmaktadır.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 43f28d9b7acb05a83544b04f6786dfe91f2d9f18
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193215"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="0f31c-103">URL'yi POS'ta açma</span><span class="sxs-lookup"><span data-stu-id="0f31c-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0f31c-104">Bu konu, Dynamics 365 Commerce satış noktası (POS) içerisinde bir URL açmak için bir düğme yapılandırmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="0f31c-104">This topic describes how you can configure a button in Dynamics 365 Commerce point of sale (POS) to open a URL.</span></span> <span data-ttu-id="0f31c-105">Bu özellik bir kod özelleştirme gerektirmez ve geliştirici rolünde olmayan bir kişi tarafından yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="0f31c-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="0f31c-106">Bu özellik, POS'ta bir düğmenin bir URL açmak için düğme kılavuzu tasarımcısı kullanılarak yapılandırılmasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="0f31c-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="0f31c-107">Şu anda, bu aşağıdaki yapılandırmalarda desteklenmektedir:</span><span class="sxs-lookup"><span data-stu-id="0f31c-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="0f31c-108">Yeni pencerede aç.</span><span class="sxs-lookup"><span data-stu-id="0f31c-108">Open in new window.</span></span>
- <span data-ttu-id="0f31c-109">POS içinde açın.</span><span class="sxs-lookup"><span data-stu-id="0f31c-109">Open within POS.</span></span>
- <span data-ttu-id="0f31c-110">Yerel bir uygulama açın.</span><span class="sxs-lookup"><span data-stu-id="0f31c-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="0f31c-111">Yeni pencerede aç</span><span class="sxs-lookup"><span data-stu-id="0f31c-111">Open in new window</span></span>

<span data-ttu-id="0f31c-112">Bu yapılandırma, bir URL'nin yeni bir pencerede mi yoksa uygulama içinde mi açılacağını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="0f31c-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="0f31c-113">Bir web URL'sini uygulama içinde açmak üzere yapılandırıldığında, POS'un yan gezinti paneli ve üst çubuğu, kullanıcı etkileşimine görünür ve kullanılabilir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="0f31c-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="0f31c-114">Yeni bir pencerede açılmak üzere yapılandırıldığında, URL Modern POS for Windows içerisinde yeni bir uygulama penceresinde veya tüm diğer POS istemcilerinde yeni bir tarayıcı sekmesinde açılır.</span><span class="sxs-lookup"><span data-stu-id="0f31c-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="0f31c-115">Bunu etkinleştirmek için **Yeni pencerede aç** seçeneği seçiliyken URL'yi yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="0f31c-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="0f31c-116">POS içinde açın</span><span class="sxs-lookup"><span data-stu-id="0f31c-116">Open within POS</span></span>

<span data-ttu-id="0f31c-117">POS içerisinde bir web URL'sini açmak şu anda yalnızca Modern POS on Windows'ta desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="0f31c-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="0f31c-118">Diğer istemciler üzerinde, bu yeterlilik geliştirme altındadır ve gelecek güncelleştirmeler için planlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0f31c-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="0f31c-119">Bunu etkinleştirmek için **Yeni pencerede aç** seçeneği seçili değilken URL'yi yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="0f31c-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="0f31c-120">Yerel bir uygulama açın</span><span class="sxs-lookup"><span data-stu-id="0f31c-120">Open a native app</span></span>

<span data-ttu-id="0f31c-121">Bu özellik, web URL'si olmayanları da yerel uygulamada açmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="0f31c-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="0f31c-122">Örneğin, MailTo, SIP, IM veya MSTEAMS gibi URL protokollerini belirtebilirsiniz, bu sayede bunlar ana cihazdaki bunlara karşılık gelen uygulamalar tarafından ele alınabilir.</span><span class="sxs-lookup"><span data-stu-id="0f31c-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="0f31c-123">Bunu etkinleştirmek için **Yeni pencerede aç** seçeneği seçiliyken URL'yi yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="0f31c-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="0f31c-124">Windows bilgisayarlarda Deployment Image Servicing and Management (DISM) kullanarak bilgisayarınızı ayarlıyorsanız, varsayılan protokol ilişkilendirmelerini ayarlamak için bkz [Varsayılan Uygulama İlişkilendirmelerini İçe veya Dışa Aktarma](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations)</span><span class="sxs-lookup"><span data-stu-id="0f31c-124">For Windows computers, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="0f31c-125">Windows bilgisayarlarınızı yönetmek için Intune gibi bir MDM kullanıyorsanız, bkz. [Policy CSP ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="0f31c-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="0f31c-126">Özel bir web sitesi kurmakta olan bir geliştiriciyseniz bkz [Bir URI için varsayılan uygulamayı çalıştırmak](/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="0f31c-126">If you are a developer building a custom website, see [Launch the default app for a URI](/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="0f31c-127">Yerel bir uygulamayı sorunsuzca açın</span><span class="sxs-lookup"><span data-stu-id="0f31c-127">Open a native app seamlessly</span></span>

<span data-ttu-id="0f31c-128">Windows, iOS ve Android, uygulama protokolü ilişkilendirmelerine dayanarak uygulamaların daha pürüzsüzce açılmasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="0f31c-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="0f31c-129">Uygulamanız bir web tarayıcısından açılmak için halihazırda yapılandırılmamışsa, bunun yapılandırılması için bir geliştiriciye ihtiyaç duyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f31c-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="0f31c-130">Windows için bkz. [Uygulama URI işleyicileri kullanarak web siteleri için uygulamaları etkinleştirmek](/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="0f31c-130">For Windows, see [Enable apps for websites using app URI handlers](/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="0f31c-131">iOS bkz. [Geliştiriciler için Evrensel Bağlantılar](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="0f31c-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="0f31c-132">Android için bkz. [Android Uygulama Bağlantılarını işlemek](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="0f31c-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="0f31c-133">İstemci</span><span class="sxs-lookup"><span data-stu-id="0f31c-133">Client</span></span>                | <span data-ttu-id="0f31c-134">Yeni pencerede aç</span><span class="sxs-lookup"><span data-stu-id="0f31c-134">Open in new window</span></span> | <span data-ttu-id="0f31c-135">Yerel uygulama açın</span><span class="sxs-lookup"><span data-stu-id="0f31c-135">Open native app</span></span> | <span data-ttu-id="0f31c-136">POS içinde açın</span><span class="sxs-lookup"><span data-stu-id="0f31c-136">Open within POS</span></span> | <span data-ttu-id="0f31c-137">Ayrıntılı</span><span class="sxs-lookup"><span data-stu-id="0f31c-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="0f31c-138">Modern POS on Windows</span><span class="sxs-lookup"><span data-stu-id="0f31c-138">Modern POS on Windows</span></span> | <span data-ttu-id="0f31c-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="0f31c-139">✓\*</span></span>                | <span data-ttu-id="0f31c-140">✓</span><span class="sxs-lookup"><span data-stu-id="0f31c-140">✓</span></span>               | <span data-ttu-id="0f31c-141">✓</span><span class="sxs-lookup"><span data-stu-id="0f31c-141">✓</span></span>              | <span data-ttu-id="0f31c-142">\* Yeni Modern POS penceresinde açar</span><span class="sxs-lookup"><span data-stu-id="0f31c-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="0f31c-143">Bulut POS</span><span class="sxs-lookup"><span data-stu-id="0f31c-143">Cloud POS</span></span>             | <span data-ttu-id="0f31c-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="0f31c-144">✓\*</span></span>                | <span data-ttu-id="0f31c-145">✓</span><span class="sxs-lookup"><span data-stu-id="0f31c-145">✓</span></span>               | <span data-ttu-id="0f31c-146">X</span><span class="sxs-lookup"><span data-stu-id="0f31c-146">X</span></span>              | <span data-ttu-id="0f31c-147">\* Yeni tarayıcı sekmesinde açar</span><span class="sxs-lookup"><span data-stu-id="0f31c-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="0f31c-148">Modern POS on iOS</span><span class="sxs-lookup"><span data-stu-id="0f31c-148">Modern POS on iOS</span></span>     | <span data-ttu-id="0f31c-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="0f31c-149">✓\*</span></span>                | <span data-ttu-id="0f31c-150">✓</span><span class="sxs-lookup"><span data-stu-id="0f31c-150">✓</span></span>               | <span data-ttu-id="0f31c-151">X</span><span class="sxs-lookup"><span data-stu-id="0f31c-151">X</span></span>              | <span data-ttu-id="0f31c-152">\* Yeni tarayıcı sekmesinde açar</span><span class="sxs-lookup"><span data-stu-id="0f31c-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="0f31c-153">Modern POS on Android</span><span class="sxs-lookup"><span data-stu-id="0f31c-153">Modern POS on Android</span></span> | <span data-ttu-id="0f31c-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="0f31c-154">✓\*</span></span>                | <span data-ttu-id="0f31c-155">✓</span><span class="sxs-lookup"><span data-stu-id="0f31c-155">✓</span></span>               | <span data-ttu-id="0f31c-156">X</span><span class="sxs-lookup"><span data-stu-id="0f31c-156">X</span></span>              | <span data-ttu-id="0f31c-157">\* Yeni tarayıcı sekmesinde açar</span><span class="sxs-lookup"><span data-stu-id="0f31c-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="0f31c-158">Başlamadan önce</span><span class="sxs-lookup"><span data-stu-id="0f31c-158">Before you begin</span></span>

<span data-ttu-id="0f31c-159">Başlamadan önce, nasıl yapılandırılacağını gözden geçirin [Satış noktası (POS) için ekran düzenleri](pos-screen-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="0f31c-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="0f31c-160">POS'ta URL Aç</span><span class="sxs-lookup"><span data-stu-id="0f31c-160">Open URL in POS</span></span>

<span data-ttu-id="0f31c-161">Bir URL'nin POS içinde açılmasını yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="0f31c-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="0f31c-162">Ana ofiste, **Perakende ve Ticaret \> Kanal Kurulumu \> POS Kurulumu \> POS \> Ekran Düzenleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="0f31c-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="0f31c-163">**Düğme Grupları \> Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0f31c-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="0f31c-164">Yeni bir düğme oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f31c-164">Create a new button.</span></span>
4. <span data-ttu-id="0f31c-165">**Düğme** nitelikleri seçin.</span><span class="sxs-lookup"><span data-stu-id="0f31c-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="0f31c-166">**URL Aç**'ı eylem olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="0f31c-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="0f31c-167">Kullanmak istediğiniz URL'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0f31c-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="0f31c-168">URL'nin yeni pencerede açılmasını isteyip istemediğinizi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="0f31c-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
