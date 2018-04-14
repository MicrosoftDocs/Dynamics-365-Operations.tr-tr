---
title: "POS için ekran düzenleri yapılandırma"
description: "Bu konu Microsoft Dynamics 365 for Retail satış noktası (POS) deneyimleri için ekran düzenleri hakkında bilgi sağlar."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad425ab0848ab04003b7378cb5c488650f01c441
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="configure-screen-layouts-for-pos"></a>POS için ekran düzenini yapılandırma

[!INCLUDE [banner](includes/banner.md)]

Bu konu Microsoft Dynamics 365 for Retail satış noktası (POS) deneyimleri için ekran düzenleri hakkında bilgi sağlar.

Microsoft Dynamics 365 for Retail satış noktası (POS) kullanıcı arabirimi, mağazalara, kasalara ve/veya kullanıcılara atanan görsel profiller ve ekran düzenleri birleşimi kullanılarak yapılandırılabilir.

## <a name="visual-profile"></a>Görsel profil
Görsel profiller kasalara atanır ve kasaya ve kullanıcılar arasında paylaşılan görsel öğeleri belirlemek için kullanılır. Kasada oturum açan herhangi bir kullanıcı, aynı tema, renkler ve resimlere sahip olacaktır. 

**Profil numarası** - Profil numarası Görsel profilin benzersiz tanımlayıcısıdır. 

**Açıklama** - Açıklama, durumunuz için doğru profili tanımlamaya yardımcı olacak anlamlı bir ad belirtmenizi sağlar.

**Tema** - Kullanıcılar Açık veya Koyu uygulama temaları arasından seçim yapabilir. Bu ayarlar, uygulamanın tamamındaki yazı tipi ve arka plan renklerini etkiler.

**Vurgu rengi** - Vurgu rengi POS boyunca kutular, komut düğmeleri veya köprüler gibi bazı görsel öğeleri farklılaştırmak veya vurgulamak için kullanılır. Bu genellikle işlem yapılabilecek öğelerdir.

**Başlık rengi** - Başlık rengi kullanıcıya perakendecinin markalama ihtiyaçlarını karşılamak üzere sayfa başlık rengini yapılandırma olanağı sağlar. Bu özellik yalnızca Dynamics 365 for Retail sürüm 1611'de bulunur.

**Oturum açma arkaplanları** - Kullanıcılar oturum açma ekranı için bir arka plan resmi belirleyebilir. Büyük dosyaları depolama ve yükleme uygulama davranışı ve performansı üzerinde etkili olabileceğinden arka plan resimlerinin dosya boyutu olabildiğince küçük tutulmalıdır.

**Uygulama arkaplanı** - POS uygulamada düz tema rengi yerine arkaplan olarak bir görüntü de kullanabilir. Oturum açma arka planlarında olduğu gibi, bu dosya boyutunun da mümkün olduğunca küçük olması önerilir.

## <a name="screen-layouts"></a>Ekran düzenleri
Ekran düzeni yapılandırması POS Hoş geldiniz ekranındaki ve Hareket ekranındaki eylemleri, içeriği ve UI denetimlerinin yerleşimini belirler. 

**Hoş Geldiniz ekranı**- Çoğu durumda, Hoş Geldiniz ekranı, kullanıcıların POS'ta ilk oturum açtıklarında göreceği sayfadır. Hoş Geldiniz ekranı bir marka görüntüsü ve POS işlemlerine erişim sağlayan düğme gruplarını kapsayabilir. Genellikle, geçerli harekete özgü olmayan işlemler buraya yerleştirilir. 

**Hareket ekranı** - Hareket ekranı, POS'ta satış hareketlerinin ve siparişlerin işlendiği ana ekrandır. Hareket ekranı, Ekran düzeni tasarımcısı kullanılarak yapılandırılabilir. 

**Varsayılan başlangıç ekranı** - Bazı perakendeciler kasiyerin oturum açtıktan sonra doğrudan Hareket ekranına gitmesini tercih eder. Varsayılan başlangıç ekran ayarı, kullanıcıların bunu her ekran düzeni için ayarlamasına olanak tanır.

### <a name="assignment"></a>Atama

Ekran düzenleri mağaza, kasa veya kullanıcı düzeyinde atanabilir. Kullanıcı ataması kasa ve mağaza atamasını geçersiz kılar ve kasa ataması mağaza atamasını geçersiz kılar. Tüm kullanıcıların kayıt veya rol ne olursa olsun aynı düzeni kullandığı basit bir senaryoda, ekran düzeni yalnızca mağazadan ayarlanabilir. Belirli kasaların veya kullanıcıların özelleştirilmiş düzenler gerektirdiği durumlarda, bunlar uygun şekilde atanabilirler.

### <a name="layout-sizes"></a>Düzen boyutları

Bu özellik yalnızca Dynamics 365 for Retail sürüm 1611 için geçerlidir. Çoğu zaman ekran düzenleri birden çok ekran boyutunda ve çözünürlüğünde kullanılabildiğinden, her kullanıcı kendi düzenini ve içeriğini yapılandırabilir. POS uygulaması, cihaz için başlangıç zamanındaki en yakın düzen boyutunu otomatik olarak seçecektir. Ekran düzeni hem tam hem de kompakt cihazlar için yapılandırmaları içerebilir. Bu yapılandırma, kullanıcının mağaza içindeki farklı boyutlar ve form faktörlerinde çalışacak tek bir ekran düzenine atanmasına olanak tanır. 

**Modern POS - Tam** - Tam düzenler genellikle en iyi PC ekranları veya tabletler gibi geniş ekranlarda kullanılır. Kullanıcılar eklenecek UI öğelerini seçebilir, kendi boyut ve yerleşimlerini belirleyebilir ve ayrıntılı özellikleri yapılandırabilirler. Tam düzenler hem dikey hem de yatay yapılandırmaları destekler. 

**Modern POS - Kompakt** - Kompakt düzenler genellikle telefonlar veya küçük tabletler için uygundur. Küçük cihazlar için tasarım olanakları sınırlıdır. Kullanıcılar giriş ve toplam bölmeleri için sütunları ve alanları yapılandırabilir.

### <a name="screen-layout-designer"></a>Ekran düzeni tasarımcısı

Bir ekran düzenindeki her yerleşim boyutu Ekran düzeni tasarımcısı kullanılarak yapılandırılmalıdır. Tasarımcı kullanıcılara Hareket ekranındaki UI öğelerini belirleme ve yapılandırma olanağı sağlar. Ekran düzeni tasarımcısı, kullanıcı her eriştiğinde uygulamanın en son sürümünü indirmek, yüklemek ve başlatmak için ClickOnce'ı kullanır. ClickOnce kullanmak için tarayıcı gereksinimlerini kontrol ettiğinizden emin olun — Chrome gibi bazı tarayıcılar uzantılar gerektirebilir. 

**Sayı takımı** - Sayı takımı POS Hareket ekranındaki ana kullanıcı girişidir. Dokunmatik ekranlar için ideal olan tam ekran dokunmatik sayı takımını göstermek veya fiziksel bir klavyeyle kullanılabilen yalnızca giriş alanını göstermek üzere yapılandırılabilir. Sayı paneli ayarları yalnızca tam düzen görünümde kullanılabilir. Dynamics 365 for Retail sürüm 1611'de, kompakt düzenler için daima Hareket ekranından tam sayı takımı kullanılabilir.

**Toplamlar panel** - Toplamlar paneli satır sayısı, indirim tutarı, giderler, alt toplam ve vergi gibi alanları göstermek üzere bir veya iki sütunda yapılandırılabilir. Dynamics 365 for Retail sürüm 1611'de, kompakt düzenleri yalnızca tek bir toplam sütununu destekler. 

**Giriş** - Giriş paneli satış satırlarını, ödeme satırlarını ve POS'ta işlenen ürünler ve hizmetler için teslimat bilgilerini içerir. Kullanıcılar sütunları, genişlikleri ve yerleşimi belirtebilir. Dynamics 365 for Retail sürüm 1611'de kompakt düzenlerde, ana satırın altındaki satırda görüntülenecek ek bilgileri de yapılandırabilirsiniz. 

**Müşteri kartı** - Müşteri kartı hareketle ilşkili olan müşteriyle ilgili bilgileri gösterir. Müşteri kartı, ek bilgileri göstermek veya gizlemek üzere yapılandırılabilir. 

**Sekme denetimi** - Sekme denetimi ekran düzenine ve sayı takımı, müşteri kartı veya sekme içine yerleştirilebilen düğme grubları gibi diğer denetimlere yerleştirilebilir. Sekme denetimi, kullanıcıların ekrana daha fazla içerik sığdırmasına yardımcı olan bir kapsayıcıdır. Sekme denetimi yalnızca tam düzenler için kullanılabilir. 

**Görüntü** - Görüntü denetimi mağaza logosunu veya diğer marka görüntülerini hareket ekranında göstermek için kullanılabilir. Görüntü denetimi yalnızca tam düzenler için kullanılabilir. 

**Önerilen ürünler** - Ortam için yapılandırılması durumunda önerilen ürünler denetimi makine öğrenimini temel alarak ürün önerileri gösterecektir. Önerilen ürünler denetimi, yalnızca Dynamics 365 for Retail sürüm 1611'de tam düzenler için kullanılabilir. ** Özel denetim **- Özel denetim, kullanıcılara özel içerik için yer sağlamak amacıyla ekran düzeni içindeki bir yer tutucu gibi davranır. Özel denetim yalnızca tam düzenler için kullanılabilir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Retail POS Düzen tasarımcısını yükleme](install-pos-layout-designer.md)




