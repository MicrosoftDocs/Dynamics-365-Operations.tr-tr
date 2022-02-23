---
title: Stil ön ayarlarıyla çalışma
description: Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucuda önceden belirlenmiş düzenlerle nasıl çalışılacağı açıklanmaktadır.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 250f2386cefee8bef45df66c4eef31b4e7fc2686
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416494"
---
# <a name="work-with-style-presets"></a>Stil ön ayarlarıyla çalışma

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce site oluşturucuda önceden belirlenmiş düzenlerle nasıl çalışılacağı açıklanmaktadır.

## <a name="overview"></a>Özet

Stil hazır ayarı, bir sitenin teması içinde bulunan tüm depolama uyumlu stil değerleri kümesidir. Site oluşturucudan sitenin görünümünü hemen değiştirmek için kullanılabilir. Stil hazır ayarları, Commerce Site Builder yazarlarının, basamaklı stil sayfaları (CSS) veya temaları kullanmak zorunda kalmadan bir dizi stil değerini kendi siteleri üzerinde hızla değiştirmesini, önizlemenizi ve etkinleştirmesini sağlar. Yazı tipi stilleri, düğme stilleri ve site renkleri, stil hazır ayarları aracılığıyla yönetilebilen stil değişkenlerinin tipik örnekleridir.

Bir sitede kullanılabilen stil değişkenleri kümesi, bir sitenin kiracısına dağıtılan Tema ve modül kitaplığı tarafından belirlenir. Dynamics 365 Commerce Çevrimiçi yazılım geliştirme seti (SDK), geliştiricilerin belirli bir temaya göre gerektirdikleri kadar çok sayıda (veya az) authorable stil değişkeni uygulayabilmelerini sağlar. Bir tema geliştiricisi, daha fazla stil değişkeni etkinleştirilerek site oluşturma yazarlarının yerine, site stilleri hakkında son seçimler yapabilir. Bu nedenle, uygulama geliştiricileri araç takımını kullanarak site stillerini güncelleştirebilir ve önizleyebilir. Bu özellik, aynı zamanda doğrudan temalarda değişiklik yapılan veya CSS gereksiz yüke neden olan tüm senaryolarda yararlıdır.

Yetkilendirilebilir tarzı değişkenlerinin etkin olduğu temalar varsayılan bir stil hazır ayarı gerektirir. Bunlar isteğe bağlı olarak dağıtılmış Tema paketinin bir parçası olarak ek hazır ayar seçenekleri içerebilir. Örneğin, tek bir varsayılan "Modern hafif" stil hazır ayarı bulunan bir tema dağıtılabilir. Alternatif olarak, varsayılan hazır ayarın yanı sıra "modern karanlık", "vintage açık" veya "vintage karanlık" gibi ek stil hazır ayar seçenekleri de bulunabilir. Bu yerleşik tema hazır ayarları geliştiriciler tarafından oluşturulur ve yeni site tasarımları için başlangıç noktaları olarak kullanılabilir.

Site oluşturucuda, yazarlar temanın yerleşik hazır ayarları arasından seçim yapabilir veya etkin stil değişkenlerini kullanarak kendi stil hazır ayarlarını ve özelleştirmelerini oluşturabilirler. Bir stil hazır ayarı, Site oluşturucuda, canlı sitede etkinleştirilmeden önce önizlenebilir. Yazarın stil değişiklikleri gözden geçirildikten sonra, stil hazır ayarı canlı site için "etkin" olarak ayarlanabilir.

## <a name="preview-a-style-preset"></a>Stil hazır ayarını Önizleme

Site oluşturucuda sitenizdeki bir stil hazır ayarını önizlemek için, aşağıdaki adımları izleyin.

1. Sitenizin sol gezinti bölmesinde, **site ayarları \>tasarıma** gidin.
1. Tasarım düzenleyicisinin üst kısmındaki **stil hazır ayarları** sekmesinde, **kullanılabilir hazır ayarlar** listesinde bir hazır ayar seçin ve sonra hazır ayar düzenleyicisine gitmek için **görüntüle**'yi seçin.

    **Mevcut hazır ayarlar** listesinde şu anda önayar yoksa özel stil hazır ayarı oluşturma hakkında bilgi için [özel stil hazır ayarı oluşturma](#create-a-custom-style-preset) konusuna bakın.

    > [!NOTE]
    > Temayla birlikte gelen hazır ayarlar, **yerleşik** bir rozet ile belirtilir. Bu yerleşik hazır ayarlar salt okunurdur. Yerleşik bir hazır ayarı yeni bir özelleştirilebilir hazır ayar olarak kopyalamak için, hazır ayar için üç nokta düğmesini (**...**) seçin ve **farklı kaydet**'i seçin.

1. Komut çubuğunda, **Önizleme** öğesini seçin.
1. Stil hazır ayarını önizlerken kullanmak üzere sitenizdeki bir URL'yi seçin ve **Tamam**'ı seçin.
1. Varyantın adını seçerek önizlemek üzere kanala özel ve yerel ayarlara özgü URL türevini seçin. Seçilen stil ön ayarı belirtilen sayfaya uygulandığı yeni bir önizleme tarayıcı penceresi açılır.

> [!NOTE]
> Önizleme URL'si kalıcıdır ve doğrulanır. Bu nedenle, canlı sitenizde "etkin" olarak ayarlamadan önce, bunu gözden geçirilmek üzere diğer kimlik doğrulama iş arkadaşlarına kopyalayabilir, yapıştırabilir ve gönderebilirsiniz. Önizleme URL'si farklı aygıtlardaki, farklı tarayıcılarda ve farklı ekranlarda stilleri denetlemek için de yararlıdır.

> [!TIP]
> Bir stil hazır ayarını düzenlerken, tarayıcı penceresini ayrı bir tarayıcı penceresinde açık bırakmayı yararlı olabilir; böylece değişikliklerinizi hızlı şekilde doğrulayabilirsiniz. Yaptığınız değişiklikleri hazır ayar olarak kaydettikten sonra, Kullanıcı deneyimini doğrulamak için açık tarayıcı penceresini yenileyin.

## <a name="create-a-custom-style-preset"></a>Özel bir stil hazır ayarı oluşturma

Site oluşturucuda özel bir stil hazır ayarını oluşturmak için, aşağıdaki adımları izleyin.

1. Sitenizin sol gezinti bölmesinde, **site ayarları \>tasarıma** gidin.
1. Tasarım düzenleyicisinin üst kısmındaki **stil hazır ayarları** sekmesinde, komut çubuğunda **Yeni hazır ayar** 'ı seçin.
1. Yeni önayar için bir ad ve açıklama girin ve **Kaydet**' seçin. Temanın varsayılan değerlerini başlangıç noktası olarak kullanan, yeni, özelleştirilebilir bir hazır ayar oluşturulur.

> [!NOTE]
> Ayrıca, o hazır ayar için üç nokta düğmesini (**...**) seçip **farklı kaydet**'i seçerek varolan herhangi bir hazır ayar için yeni bir özel stil hazır ayarı da oluşturabilirsiniz. Alternatif olarak, hazır ayar düzenleyicisindeki komut çubuğunda **farklı kaydet**'i seçin.

## <a name="modify-global-and-module-type-style-values"></a>Global ve modül türü stil değerlerini Değiştir

Temanın stil değişkenlerinin bazıları birden çok Modül türü arasında paylaşılıyor. Bu stil değişkenlerine *genel* stil değişkenleri denir. Birincil site renkleri, varsayılan yazı tipi stilleri ve düğme stilleri arasında örnek verilmiştir. Genel değişkenleri ayarlayarak, farklı birçok modül türünde görünümü değiştirebilirsiniz.

Bazı stil değerleri bir modül türü için benzersiz olabilir veya isteğe bağlı olarak varsayılan bir Global değeri geçersiz kılmak zorunda kalabilir. Bir sitenin teması Modül türü stil değişkenleri uygulamışsa, Site Builder yazarları modül türünün stilini global ayarlardan bağımsız olarak özelleştirebilir. Modül tipi değişkenleri bir temadaki Global stil değişkenlerini artırabilir ya da geçersiz kılabilir.

> [!NOTE]
> Bir sitedeki stil değerleri hiyerarşisi aşağıdaki şekilde davranır. Sağa doğru görünen stil değerleri bunların solundaki stil değerlerini geçersiz kılar.
>
> Tema varsayılan değerleri \< Global stil değerleri \< Modül türü stil değerler \< CSS geçersiz kılma

Site oluşturucuda bir stil hazır ayarının Global ya da modül türü değerlerini değiştirmek için aşağıdaki adımları izleyin.

1. Sitenizin sol gezinti bölmesinde, **site ayarları \>tasarıma** gidin.
1. Tasarım düzenleyicisinin üst kısmındaki **stil hazır ayarları** sekmesinde, hazır ayar düzenleyicisine gitmek için herhangi bir stil hazır ayarı **Görüntüle**'yi seçin.
1. Önceden belirlenmiş ayar için, **önizleme**'yi seçin ve sonra URL seçim adımlarını izleyerek bir tam tarayıcı pencere görünümü açın. Bu önizleme tarayıcı penceresini açık bırakın.
1. Hazır ayar düzenleyicide, sağ üst köşedeki **Düzenle** seçin.
1. Bazı genel stil değerlerini değiştirmek için, düzenleyicideki stil değişkeni kontrollerini kullanın.
1. Düzenleyicinin üst kısmında, **Genel** sekmesinin sağındaki **modüller** sekmesinde , stillendirilmiş olması gereken bir modül türü seçin.
1. Modül türünün bazı değerlerini değiştirmek için stil kontrollerini kullanın.
1. Değişikliklerinizin önizlemesine önizleme uygulamak için hazır olduğunuzda, komut çubuğunda **Kaydet**'i seçin.
1. Önizleme tarayıcı penceresine dönün ve yenileyin. Tam tarayıcı pencere önizleme, farklı görünümdeki, farklı tarayıcılarda ve farklı cihaz platformlarındaki stil değişikliklerini denetlemek için yararlıdır.
1. Tüm değişiklikler tamamlandığında ve doğrulandığında, düzenleyicinin sağ üst köşesindeki **son düzenlemeyi** seçin.

> [!NOTE]
> Sitenizde etkin durumda olan stil hazır ayarını düzenliyorsanız, düzenleyicide mavi bir **etkin** rozet görürsünüz. Bu rozet, hazır ayarın Şu anda Web sitenizde etkin olduğunu gösterir. Etkin hazır ayarı değiştirirseniz, Bu değişiklikleri canlı sitenize göndermek için **Yayınla**'yı seçin.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Yeni bir stil hazır ayarını canlı sitenizde etkin hale getirin

Sitenizde yeni etkin ayar olarak bir stil hazır ayarı ayarlamak için, aşağıdaki adımları izleyin.

- Şu konumlardan birinde **etkin yap düğmesini** seçin:

    - Stil hazır ayarı düzenleyicisindeki komut çubuğu
    - **Site ayarları \> tasarımdaki** **stil hazır ayarları** sekmesi üzerindeki ana görünümdeki kullanılabilir herhangi bir hazır ayar için üç nokta menüsü (**...**)

Hazır ayarın stil değerleri herkese açık Web sitenizde etkin hale getirilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Logo ekleme](add-logo.md)

[Site teması seçme](select-site-theme.md)

[CSS geçersiz kılma dosyalarıyla çalışma](css-override-files.md)

[Favicon ekleme](add-favicon.md)

[Hoş geldiniz iletisi ekleme](add-welcome-message.md)

[Telif hakkı bildirimi ekleme](add-copyright-notice.md)

[Sitenize dil ekleme](add-languages-to-site.md)

[Telemetriyi desteklemek için site sayfalarına komut dosyası kodu ekleme](add-telemetry.md)
