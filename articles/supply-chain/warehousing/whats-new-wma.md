---
title: Warehouse Management mobil uygulamasındaki yenilikler veya değiştirmeler
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management için Warehouse Management mobil uygulamasının yayımlanan her sürümü için yeni ve değiştirilmiş özellikleri listeler.
author: ivanv-microsoft
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 43d1381e73d5659bfd6ae6c6d944b7e6918b681a4f89df7ad23abbed5b4a0d3c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720096"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Warehouse Management mobil uygulamasındaki yenilikler veya değiştirmeler

[!include [banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Supply Chain Management için Warehouse Management mobil uygulamasının yayımlanan her sürümü için yeni özellikleri, iyileştirmeleri ve bilinen sorunları listeler.

## <a name="2070"></a>2.0.7.0

### <a name="new-features-fixes-and-improvements-in-version-2070"></a>Sürüm 2.0.7.0'daki yeni özellikler, düzeltmeler ve iyileştirmeler

- Uygulamanın en son yayımlanan sürümünü denetleyen **Hakkında** sayfasına bir bölüm eklendi.
- Sayfalar arasında hızlı kaydırma ve çekme kolaylaştırıldı.
- İş listesindeki artan/azalan düğmesinin simgesi değiştirildi.
- Daha fazla bilgi sığdırmak için **Ayrıntılar** kartındaki kenar boşlukları azaltıldı.
- Uygulamanın zamanla yavaşlama sorununu azaltmak için çeşitli performans iyileştirmeleri uygulandı.
- Ekrana sığdırılandan daha fazla denetim varsa ve bu da sayfalamaya neden oluyorsa döndürücü denetimi artık sayfayla aynı şekilde kaymaz.
- Görev başlığını göstermek yerine son taranan değeri göstermeye öncelik verildi, bu nedenle bunların çakışması durumunda görev başlığı kesilir.
- Sistemin yanıt vermemesine neden olan çeşitli sorunlar giderildi.
- Çeşitli yerlerdeki metinler artık bazı dillerde kesilmiyor.
- Uygulama artık varsayılan olarak tam ekran modunda çalışıyor.
- Bazı cihazlarda ana sayfadaki taramaların zaman zaman yok sayılmasına neden olan bir sorun giderildi.

### <a name="known-issues-in-version-2070"></a>Sürüm 2.0.7.0'daki bilinen sorunlar

- Bazı cihazlarda, uygulamayı başlattığınızda veya bir göreve başladığınızda şu hata iletisini alırsınız: "Belirtilen boyut için uygun bir görünüm bulunamıyor." Bu hata iletisini herhangi bir cihazınızda görüyorsanız Warehouse Management mobil uygulamasını o cihazda 2.0.6.0 sürümüne düşürmeli ve uygulamanın bir sonraki sürümü yayımlanana kadar yükseltmeyi bekletmelisiniz.

## <a name="version-2060"></a>Sürüm 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Sürüm 2.0.6.0'daki yeni özellikler, düzeltmeler ve iyileştirmeler

Bu sürüm aşağıdaki yeni özellikleri, düzeltmeleri ve iyileştirmeleri içerir.

- Demo modu artık tüm etiketleri cihaz dilinde göstermektedir.
- Aşağıdaki hata iletisini alma olasılığınız daha düşüktür: "Belirtilen boyut için uygun bir görünüm bulunamıyor."
- İş kartları için en düşük yükseklik artırıldı (iş listesinde üç veya daha az alan görünecek şekilde yapılandırılan durumlar için).
- Ayrıntılar kartlarının altındaki kenar boşlukları (soluk) geliştirildi.
- Sunucuyla değiştirilen XML dosyalarındaki geçersiz simgeler artık düzgün bir şekilde işleniyor. (Örneğin, yazdırılmayan karakterler artık düzgün şekilde işleniyor ve artık uygulamanın yanıt vermemesine neden olmuyor.)
- Sunucu isteği gönderildiğinde HTTP hataları ("hata 503" gibi) artık düzgün bir şekilde işleniyor.
- Bir hata gösterilirken, birleşik giriş kutusu denetimleri için seçenekler listesi artık otomatik olarak gösterilmez.
- Kullanıcı ayarlarında seçilen görüntü yönü nedeniyle uygulama artık yanıt vermeyi durdurmuyor.
- Ürün görselleri artık self servis ortamlarında gösteriliyor. (Bu değişiklik yalnızca düşük çözünürlüklü sürümler için geçerlidir. Dosya yönetimi hizmeti self servis ortamlarda tam boyutlu görüntüleri desteklemez.)
- Sıfır miktarlı kısa çekmelere neden olan bir sorun giderildi.
- Uygulama artık ayrıntılar kartı birden çok özdeş alan gösterdiğinde yanıt vermeyi durdurmuyor.

### <a name="known-issues-in-version-2060"></a>Sürüm 2.0.6.0'daki bilinen sorunlar

Bu sürümde aşağıdaki bilinen sorunlar bulunmaktadır:

- Uygulama (özellikle iş listesi) zamanla yavaşlıyor.
- **Windows sürümü:** Windows'ta tarama için bir USB tabanca kullanıldığında, tutarsız sonuçlar taranan sembollerin karıştırılmalarına neden oluyor.

## <a name="version-2050"></a>Sürüm 2.0.5.0

Bu sürüm aşağıdaki yeni özellikleri, düzeltmeleri ve iyileştirmeleri içerir.

- İstemci gizli anahtarı artık bağlantı ayarları kurulumunda gizlenmiyor.
- Artık tam olarak görmek için herhangi bir metne uzun süre basabilirsiniz.
- Depolama izinleri eksik olduğunda gösterilen hata iletisi geliştirildi.
- Bazı akışlar için yeni denetim sıraları eklendi.
- Pencere boyutu nedeniyle gönder düğmesi artık hatalı şekilde kullanılamaz duruma gelmiyor.
- Kaydırıcılar artık daha büyük düğme boyutları kullanıldığında daha küçük ekranlarda edebiliyor.
- Dört düğmeli katman artık kesilmiyor.
- Klavye artık sil düğmesini destekliyor.
- Klavyeye basıldığında oluşabilen bir parlaklık sorunu giderildi.
- Çeşitli demo veri sorunları giderildi.
- Ayrıntılar sayfasındaki sayısal alanları etkileyen bir sorun giderildi.
- Ekran klavyesi artık bazı cihazlarda zaman zaman kaybolmuyor.
- Arka plan rengini ve konumlandırmasını etkileyen hatalar gibi çeşitli kullanıcı arabirimi (UI) hataları düzeltildi.
- Rusça kullanıcı arabirimi geliştirildi.
- Sistemin yanıt vermeyi durdurmasına neden olan çeşitli sorunlar giderildi.
- Hesap makinesinin yeniden açılmasıyla ilgili bir sorun giderildi.
- **Android sürümü:** Android 4.4'ün başlangıçta yanıt vermeyi durdurmasına neden olan bir sorun giderildi.
- **Android sürümü:** Minimum ölçeklendirme yüzde 50'ye düşürüldü.

## <a name="version-2040"></a>Sürüm 2.0.4.0

Sürüm 2.0.4.0, Warehouse Management mobil uygulamasının genel kullanıma sunulan ilk sürümüydü.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Sürüm 2.0.4.0'daki yeni özellikler, düzeltmeler ve iyileştirmeler

Bu sürüm, önizleme sürümünde bulunmayan aşağıdaki yeni özellikleri, düzeltmeleri ve iyileştirmeleri sunar:

- Ayrıntılar kartı aynı verilere sahip iki etiket içeriyorsa, etiketlerden biri gizlenir.
- Özel karakterler artık varsayılan olarak gösteriliyor ve bunları gizleme seçeneği kullanıcı ayarlarından kaldırıldı.
- Devre dışı bırakılan gönderme düğmeleri artık kompakt kola takılan görünümde kullanılamıyor olarak gösteriliyor.
- Denetimler için sıralama mantığında yapılan bir değişiklik, cihazlar arasında daha sorunsuz ölçeklendirme sağlıyor. Bu nedenle, yazı tiplerinin veya düğmelerin ölçeklendirmesini ayarlamaya daha az ihtiyaç vardır.
- Varsayılan renk teması *Koyu* olarak değiştirildi.
- Devre dışı bırakılmış gönder düğmesinin eksik simgesi şerit görünümüne eklendi.
- Zaman aşımı özel durumları artık satır içi hata göstermek yerine sizi bağlantı sayfasına götürüyor.
- Kullanılabilir gönderme eylemi yoksa (**Tamam**, **Evet**, **Kabul**, **Bitti** veya **Tamamlandı** gibi), gönder düğmesi devre dışı bırakılır.
- Uygulama kararlılığı geliştirildi.
- Güvenlik açığı için bir düzeltme hazırlandı: [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Windows sürümü:** Windows'ta pencere yeniden boyutlandırıldıktan sonra menülerin yanıt vermemesine neden olan bir sorun giderildi.

### <a name="known-issue-in-version-2040"></a>Sürüm 2.0.4.0'daki bilinen sorun

Bu sürümde aşağıdaki bilinen sorun bulunmaktadır:

- Bu sürümde Android 4.4 kullanan cihazlarla ilgili bir sorun vardır. Uygulamayı bu Android sürümünde kullandığınızda sorunlarla karşılaşabilirsiniz.
