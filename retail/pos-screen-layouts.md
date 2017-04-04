---
title: "Ekran düzenleri POS için yapılandırma"
description: "Bu konu Microsoft Dynamics 365 işlemleri - perakende noktası (POS) satış deneyimleri için ekran düzenleri hakkında bilgi sağlar."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Ekran düzenleri POS için yapılandırma

Bu konu Microsoft Dynamics 365 işlemleri - perakende noktası (POS) satış deneyimleri için ekran düzenleri hakkında bilgi sağlar.

Görsel profilleri ve ekran düzenleri, mağazalar, kasalar ve/veya kullanıcılar atanmış bir birleşimini kullanarak Microsoft Dynamics 365 işlemleri - perakende satış (POS) kullanıcı arabirimi noktası için yapılandırılabilir.

## <a name="visual-profile"></a>Görsel profil
Görsel profilleri kasalar için atanır ve özel kasa ve paylaşılan kullanıcıları arasında görsel öğeleri belirtmek için kullanılır. Kasada açan herhangi bir kullanıcı, tema, renkler ve resimler olacaktır. **Profil sayısı** -Profil numarası Görsel profil benzersiz tanımlayıcısıdır. **Açıklama** -açıklama, durumunuz için doğru profili tanımlamak için yardımcı olacak anlamlı bir ad belirtmenizi sağlar. **Tema** -kullanıcılar arasında açık veya koyu uygulama temaları seçebilirsiniz. Bu ayarlar, uygulama boyunca yazı tipi ve arka plan renkleri etkiler. **Vurgu rengi** -Vurgu rengi POS ayırt etmek veya döşeme, komut düğmesi veya köprü gibi bazı görsel öğeleri vurgulamak için kullanılır. Bu öğeler genellikle kalırdı. **Üstbilgi renk** -başlık rengi satıcıya markalama ihtiyaçlarını karşılamak üzere sayfa üstbilgisi rengini yapılandırmak kullanıcı sağlar. Bu özellik yalnızca operasyonlar için sürüm 1611 Dynamics 365 içinde kullanılabilir. **Oturum açma arka** -kullanıcı oturum açma ekranı için bir arka plan resmi belirleyebilirsiniz. Depolama ve büyük dosyaları yükleme uygulama davranış ve performans üzerinde etkili olabilecek gibi arka plan resimleri dosya boyutunu olabildiğince küçük tutulmalıdır. **Uygulama arka plan** -POS de kullanabilirsiniz görüntünün arka plan düz Tema rengi yerine uygulama boyunca olarak. İle oturum açma arka planlar gibi bu dosya boyutunu mümkün olduğunca az tutmak için önerilir.

## <a name="screen-layouts"></a>Ekran düzenleri
Ekran düzeni yapılandırma eylemleri, içerik ve POS Hoş Geldiniz ekranı ve hareket ekran UI denetimleri yerleşimini belirler. ** Hoş Geldiniz ekranı **-çoğu durumda, Hoş Geldiniz ekranı, POS ilk oturum açtıklarında kullanıcıların göreceği sayfasıdır. Hoş Geldiniz ekranı bir marka görüntüsü ve POS işlemlerine erişim sağlayan düğme grupları kapsayabilir. Genellikle, geçerli hareket için belirli olmayan işlemler burada yerleştirilir. **Hareket ekran** -TRANSACTION ekran ana ekranında POS satış hareketlerinin ve siparişleri işlemek için olur. Hareket ekran ekran düzeni Tasarımcısı'nı kullanarak yapılandırılabilir. **Varsayılan başlangıç ekran** -bazı Perakendeciler kasiyer oturum sonra hareket ekrana doğrudan gitmek tercih. Varsayılan başlangıç ekran ayarı, kullanıcıların bu her ekran düzenini ayarlamak sağlar.

### <a name="assignment"></a>Atama

Ekran düzenleri mağaza, Kaydet veya kullanıcı düzeyinde atanabilir. Kullanıcı atama kayıt geçersiz kılar ve atama ve kayıt ataması geçersiz kılmaları mağaza atama saklayın. Burada tüm kullanıcıların kayıt veya rol ne olursa olsun aynı düzeni kullanmak basit bir senaryoda, ekran düzeni mağazada ayarlayabilirsiniz. Burada belirli kayıtları veya kullanıcılara özelleştirilmiş düzenleri gerektiren durumlarda uygun şekilde atanabilirler.

### <a name="layout-sizes"></a>Düzen boyutları

Bu özellik, yalnızca Dynamics 365 arası 1611 işlemleri sürümü için geçerlidir. Çoğu zaman ekran düzenleri birden çok ekran boyutlarına ve çözümleri kullanılabilir olduğundan, kullanıcılar kendi düzenini ve içeriğini her biri için yapılandırabilirsiniz. POS uygulaması, başlangıç tarihindeki en yakın yerleşim boyutu aygıtın otomatik olarak seçecektir. Ekran düzeni için tam ve kompakt aygıt yapılandırmaları da içerebilir. Bu yapılandırma, çeşitli boyutları ve mağaza içinde form faktörleri arasında çalışır bir tek ekran düzeni için atanmış bir kullanıcı sağlar. **Modern POS - tam** -tam düzenleri genellikle en iyi şekilde kullanılır PC monitör veya tabletler gibi daha büyük görüntü için. Kullanıcılar dahil, kendi boyutunu ve yerini belirlemek ve bunların ayrıntılı özelliklerini yapılandırmak için kullanıcı Arabirimi öğeleri seçebilirsiniz. Tam düzenleri hem dikey hem de yatay yapılandırmalarını destekler. **Modern POS - Compact** -sıkıştırma düzenleri genellikle en iyi şekilde kullanılır telefonları veya küçük tabletler için. Küçük aygıtlar için tasarım olanakları sınırlıdır. Kullanıcılar sütun ve alanları alındı ve toplamları bölmeleri için yapılandırabilirsiniz.

### <a name="screen-layout-designer"></a>Ekran düzeni tasarımcısı

Her yerleşim boyutu ekran düzeni içinde ekran düzeni Tasarımcısı'nı kullanarak yapılandırılmış olması gerekir. Tasarımcı belirtin ve hareket ekran UI öğeleri yapılandırmak kullanıcılar sağlar. Karşıdan yükleme, yükleme ve başlatma uygulaması kullanıcının eriştiği her zaman en son sürümünü ClickOnce ekran düzeni tasarımcısı kullanır. ClickOnce kullanarak tarayıcı gereksinimleri kontrol ettiğinizden emin olun — krom gibi bazı tarayıcılar uzantılarını isteyebilir. **Sayı panelini** -sayı takımını hareket POS ekranında ana kullanıcı girdileri gelir. Tüm ekran dokunmatik ekranlar için ideal olan pad veya fiziksel bir klavye ile kullanılabilmesi için yalnızca giriş alanı gösterecek şekilde yapılandırılabilir. Sayı paneli ayarları yalnızca tam görünümde kullanılabilir. İşlemleri sürüm 1611'de 365 Dynamics, kompakt düzenleri kullanılabilir hareket ekrandan tam sayı takımını her zaman vardır. **Toplamları panel** - toplamları Masası ikisinden biri içinde yapılandırılabilir veya alanları gibi göstermek için iki sütun satır sayısı, iskonto tutarı, giderler, alt toplam ve vergi. İşlemleri sürüm 1611'de 365 Dynamics, kompakt düzenleri yalnızca tek bir toplam sütunu destekler. **Giriş** -** ** giriş paneli satış satırlarını, ödeme satırlarının ve ürünler ve hizmetler POS işlenen için teslimat bilgilerini içerir. Kullanıcılar, sütun genişlikleri ve yerleşim belirtebilirsiniz. İşlemleri sürüm 1611 Dynamics 365 içinde kompakt düzenleri içinde ana boru hattı altındaki satırda görünecek ek bilgiler de yapılandırabilirsiniz. **Müşteri Kartı** - Geçerli hareketle ilişkili müşterinin ilgili müşteri kartı bilgi gösterir. Müşteri Kartı, ek bilgileri göstermek veya gizlemek için yapılandırılabilir. **Sekme denetimi** - sekme denetiminin ekran düzeni ve sayı takımını, müşteri kartı, gibi diğer denetimler üzerine yerleştirilebilir veya düğme grupları sekmesini yerleştirilebilir. Sekme denetiminin ekranda daha fazla içeriğe sığdırmak için kullanıcılara yardım eden bir kapsayıcıdır. Sekme denetimi yalnızca tam düzenleri için kullanılabilir. ** Görüntü **-resim denetimi deposu logo veya başka marka görüntü hareket ekranda göstermek için kullanılabilir. Resim denetimi, yalnızca tam düzenleri için kullanılabilir. **Önerilen ürünleri** - denetim makine öğrenmeyi temel ürün önerileri göster önerilen ürünleri ortamı için yapılandırılmış. Önerilen ürünleri denetim, yalnızca Dynamics 365 tam düzenleri 1611 işlemleri sürümü için kullanılabilir. ** Özel denetim **-özel denetim için ekran düzeni içinde yer tutucu özel içerik için yer ayırmak kullanıcılara gibi davranır. Özel denetim, yalnızca tam düzenleri için kullanılabilir.

<a name="see-also"></a>Ayrıca bkz.
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)


