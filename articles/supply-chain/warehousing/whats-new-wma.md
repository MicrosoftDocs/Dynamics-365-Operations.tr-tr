---
title: Warehouse Management mobil uygulamasındaki yenilikler veya değiştirmeler
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management için Warehouse Management mobil uygulamasının yayımlanan her sürümü için yeni ve değiştirilmiş özellikleri listeler.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261804"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="f8ec1-103">Warehouse Management mobil uygulamasındaki yenilikler veya değiştirmeler</span><span class="sxs-lookup"><span data-stu-id="f8ec1-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8ec1-104">Bu konu, Microsoft Dynamics 365 Supply Chain Management için Warehouse Management mobil uygulamasının yayımlanan her sürümü için yeni özellikleri, iyileştirmeleri ve bilinen sorunları listeler.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="f8ec1-105">Sürüm 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="f8ec1-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="f8ec1-106">Sürüm 2.0.6.0'daki yeni özellikler, düzeltmeler ve iyileştirmeler</span><span class="sxs-lookup"><span data-stu-id="f8ec1-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="f8ec1-107">Bu sürüm aşağıdaki yeni özellikleri, düzeltmeleri ve iyileştirmeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="f8ec1-108">Demo modu artık tüm etiketleri cihaz dilinde göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="f8ec1-109">Aşağıdaki hata iletisini alma olasılığınız daha düşüktür: "Belirtilen boyut için uygun bir görünüm bulunamıyor."</span><span class="sxs-lookup"><span data-stu-id="f8ec1-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="f8ec1-110">İş kartları için en düşük yükseklik artırıldı (iş listesinde üç veya daha az alan görünecek şekilde yapılandırılan durumlar için).</span><span class="sxs-lookup"><span data-stu-id="f8ec1-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="f8ec1-111">Ayrıntılar kartlarının altındaki kenar boşlukları (soluk) geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="f8ec1-112">Sunucuyla değiştirilen XML dosyalarındaki geçersiz simgeler artık düzgün bir şekilde işleniyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="f8ec1-113">(Örneğin, yazdırılmayan karakterler artık düzgün şekilde işleniyor ve artık uygulamanın yanıt vermemesine neden olmuyor.)</span><span class="sxs-lookup"><span data-stu-id="f8ec1-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="f8ec1-114">Sunucu isteği gönderildiğinde HTTP hataları ("hata 503" gibi) artık düzgün bir şekilde işleniyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="f8ec1-115">Bir hata gösterilirken, birleşik giriş kutusu denetimleri için seçenekler listesi artık otomatik olarak gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="f8ec1-116">Kullanıcı ayarlarında seçilen görüntü yönü nedeniyle uygulama artık yanıt vermeyi durdurmuyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="f8ec1-117">Ürün görselleri artık self servis ortamlarında gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="f8ec1-118">(Bu değişiklik yalnızca düşük çözünürlüklü sürümler için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="f8ec1-119">Dosya yönetimi hizmeti self servis ortamlarda tam boyutlu görüntüleri desteklemez.)</span><span class="sxs-lookup"><span data-stu-id="f8ec1-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="f8ec1-120">Sıfır miktarlı kısa çekmelere neden olan bir sorun giderildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="f8ec1-121">Uygulama artık ayrıntılar kartı birden çok özdeş alan gösterdiğinde yanıt vermeyi durdurmuyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="f8ec1-122">Sürüm 2.0.6.0'daki bilinen sorunlar</span><span class="sxs-lookup"><span data-stu-id="f8ec1-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="f8ec1-123">Bu sürümde aşağıdaki bilinen sorunlar bulunmaktadır:</span><span class="sxs-lookup"><span data-stu-id="f8ec1-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="f8ec1-124">Uygulama (özellikle iş listesi) zamanla yavaşlıyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="f8ec1-125">**Windows sürümü:** Windows'ta tarama için bir USB tabanca kullanıldığında, tutarsız sonuçlar taranan sembollerin karıştırılmalarına neden oluyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="f8ec1-126">Sürüm 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="f8ec1-126">Version 2.0.5.0</span></span>

<span data-ttu-id="f8ec1-127">Bu sürüm aşağıdaki yeni özellikleri, düzeltmeleri ve iyileştirmeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="f8ec1-128">İstemci gizli anahtarı artık bağlantı ayarları kurulumunda gizlenmiyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="f8ec1-129">Artık tam olarak görmek için herhangi bir metne uzun süre basabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="f8ec1-130">Depolama izinleri eksik olduğunda gösterilen hata iletisi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="f8ec1-131">Bazı akışlar için yeni denetim sıraları eklendi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="f8ec1-132">Pencere boyutu nedeniyle gönder düğmesi artık hatalı şekilde kullanılamaz duruma gelmiyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="f8ec1-133">Kaydırıcılar artık daha büyük düğme boyutları kullanıldığında daha küçük ekranlarda edebiliyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="f8ec1-134">Dört düğmeli katman artık kesilmiyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="f8ec1-135">Klavye artık sil düğmesini destekliyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="f8ec1-136">Klavyeye basıldığında oluşabilen bir parlaklık sorunu giderildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="f8ec1-137">Çeşitli demo veri sorunları giderildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="f8ec1-138">Ayrıntılar sayfasındaki sayısal alanları etkileyen bir sorun giderildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="f8ec1-139">Ekran klavyesi artık bazı cihazlarda zaman zaman kaybolmuyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="f8ec1-140">Arka plan rengini ve konumlandırmasını etkileyen hatalar gibi çeşitli kullanıcı arabirimi (UI) hataları düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="f8ec1-141">Rusça kullanıcı arabirimi geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="f8ec1-142">Sistemin yanıt vermeyi durdurmasına neden olan çeşitli sorunlar giderildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="f8ec1-143">Hesap makinesinin yeniden açılmasıyla ilgili bir sorun giderildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="f8ec1-144">**Android sürümü:** Android 4.4'ün başlangıçta yanıt vermeyi durdurmasına neden olan bir sorun giderildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="f8ec1-145">**Android sürümü:** Minimum ölçeklendirme yüzde 50'ye düşürüldü.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="f8ec1-146">Sürüm 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="f8ec1-146">Version 2.0.4.0</span></span>

<span data-ttu-id="f8ec1-147">Sürüm 2.0.4.0, Warehouse Management mobil uygulamasının genel kullanıma sunulan ilk sürümüydü.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="f8ec1-148">Sürüm 2.0.4.0'daki yeni özellikler, düzeltmeler ve iyileştirmeler</span><span class="sxs-lookup"><span data-stu-id="f8ec1-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="f8ec1-149">Bu sürüm, önizleme sürümünde bulunmayan aşağıdaki yeni özellikleri, düzeltmeleri ve iyileştirmeleri sunar:</span><span class="sxs-lookup"><span data-stu-id="f8ec1-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="f8ec1-150">Ayrıntılar kartı aynı verilere sahip iki etiket içeriyorsa, etiketlerden biri gizlenir.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="f8ec1-151">Özel karakterler artık varsayılan olarak gösteriliyor ve bunları gizleme seçeneği kullanıcı ayarlarından kaldırıldı.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="f8ec1-152">Devre dışı bırakılan gönderme düğmeleri artık kompakt kola takılan görünümde kullanılamıyor olarak gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="f8ec1-153">Denetimler için sıralama mantığında yapılan bir değişiklik, cihazlar arasında daha sorunsuz ölçeklendirme sağlıyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="f8ec1-154">Bu nedenle, yazı tiplerinin veya düğmelerin ölçeklendirmesini ayarlamaya daha az ihtiyaç vardır.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="f8ec1-155">Varsayılan renk teması *Koyu* olarak değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="f8ec1-156">Devre dışı bırakılmış gönder düğmesinin eksik simgesi şerit görünümüne eklendi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="f8ec1-157">Zaman aşımı özel durumları artık satır içi hata göstermek yerine sizi bağlantı sayfasına götürüyor.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="f8ec1-158">Kullanılabilir gönderme eylemi yoksa (**Tamam**, **Evet**, **Kabul**, **Bitti** veya **Tamamlandı** gibi), gönder düğmesi devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="f8ec1-159">Uygulama kararlılığı geliştirildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-159">App stability has been improved.</span></span>
- <span data-ttu-id="f8ec1-160">Güvenlik açığı için bir düzeltme hazırlandı: [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="f8ec1-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="f8ec1-161">**Windows sürümü:** Windows'ta pencere yeniden boyutlandırıldıktan sonra menülerin yanıt vermemesine neden olan bir sorun giderildi.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="f8ec1-162">Sürüm 2.0.4.0'daki bilinen sorun</span><span class="sxs-lookup"><span data-stu-id="f8ec1-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="f8ec1-163">Bu sürümde aşağıdaki bilinen sorun bulunmaktadır:</span><span class="sxs-lookup"><span data-stu-id="f8ec1-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="f8ec1-164">Bu sürümde Android 4.4 kullanan cihazlarla ilgili bir sorun vardır.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="f8ec1-165">Uygulamayı bu Android sürümünde kullandığınızda sorunlarla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f8ec1-165">You might experience issues when you use the app on this Android version.</span></span>
