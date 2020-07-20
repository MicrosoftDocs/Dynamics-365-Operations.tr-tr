---
title: POS kullanıcı arabirimi görsel yapılandırmaları
description: Bu konu Dynamics 365 Commerce satış noktası (POS) deneyimleri için ekran düzenleri hakkında bilgi sağlar.
author: boycezhu
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: boycezhu
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a037c8514d7838b3a4797f21b3ef3f6d5736e840
ms.sourcegitcommit: f7294160d18f15cb762c24f2459b4f0887c37541
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/25/2020
ms.locfileid: "3505646"
---
# <a name="pos-user-interface-visual-configurations"></a>POS kullanıcı arabirimi görsel yapılandırmaları

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Microsoft Dynamics 365 Commerce satış noktası (POS) kullanıcı arabirimi, mağazalara, kasalara ve kullanıcılara atanan görsel profiller ve ekran düzenleri birleşimi kullanılarak yapılandırılabilir. Bu konu, bu yapılandırma seçenekleri hakkında bilgi sağlar.

Aşağıdaki çizimde, yapılandırılabilir POS kullanıcı arabirimi özelliklerini oluşturan çeşitli varlıklar arasındaki ilişkiler gösterilmektedir.

![POS ekran düzeni varlıkları](../commerce/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Görsel profil

Görsel profiller kasalara atanır ve kasaya özel ve kullanıcılar arasında paylaşılan görsel öğeleri belirtir. Kasada oturum açan her kullanıcı aynı temayı, düzeni, renkleri ve resimleri görür.

![POS hoş geldiniz ekranı - Açık tema](../commerce/media/POS-Welcome-Screen-with-Light-theme.png)

![POS Hareket ekranı - Koyu tema](../commerce/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profil numarası** – Profil numarası, görsel profilin benzersiz tanımlayıcısıdır.
- **Açıklama** – Durumunuz için doğru profili tanımlamaya yardımcı olacak anlamlı bir ad belirtebilirsiniz.
- **Tema** – **Açık** veya **Koyu** uygulama temaları arasından seçim yapabilirsiniz. Tema, uygulamanın tümünde yazı tipini ve arka plan renklerini etkiler.
- **Vurgu rengi** – Vurgu rengi tüm POS genelinde kutucuk, komut düğmesi ve köprü gibi belirli görsel öğeleri ayırt etmek veya vurgulamak için kullanılır. Bunlar genellikle işlem yapılabilecek öğelerdir.
- **Başlık rengi** – Sayfa başlığının rengini, perakendecinin marka gereksinimlerini karşılayacak şekilde yapılandırabilirsiniz.
- **Yazı tipi düzeni** – **Standart** ve **Büyük** yazı tipi düzenleri arasından seçim yapabilirsiniz. Yazı tipi düzeni tüm uygulama boyunca yazı tipi boyutunu etkiler. Varsayılan seçim **Standart**'tır.
- **Uygulama çubuğu etiketlerini her zaman göster** – Bu seçenek etkinken, etiket metni her zaman uygulama çubuğu düğmelerinin altında görünür.
- **Düzen** – **Ortalanmış** ve **Sağ** düzenleri arasında seçim yapabilirsiniz. Düzen, oturum açma ekranındaki oturum açma kutusunun hizalamasını etkiler. Varsayılan seçim **Ortalanmış**'tır.
- **Tarihi/saati göster** - Bu seçenek etkinleştirildiğinde, POS başlığında ve oturum açma ekranında geçerli tarih ve saat gösterilir.
- **Klavye** – Oturum açma ekranında giriş için kullanılan varsayılan klavyeyi belirtmek için **Varsayılan olarak işletim sistemi klavyesi** ve **Sayı takımını göster**'i seçebilirsiniz. Sayı takımı, özellikle dokunmatik tabanlı aygıtlarda kullanılan sanal bir klavyedir. Varsayılan seçim **Varsayılan olarak İşletim Sistemi klavyesi**'dir.
- **Logo resmi** – Oturum açma ekranında gösterilen bir logo resmi belirtebilirsiniz. Arka planı saydam olan bir görüntü kullanmanızı öneririz. Büyük dosyaların depolanması ve yüklenmesi, uygulama davranışını ve performansını olumsuz etkileyebileceği için, dosya boyutu olabildiğince küçük tutulmalıdır.
- **Oturum açma arka planı** – Oturum açma ekranı için bir arka plan resmi belirtebilirsiniz. Arka plan görüntülerinin dosya boyutu mümkün olduğunca küçük tutulmalıdır.
- **Arka plan** – Uygulama genelinde düz tema rengi yerine kullanılacak bir arka plan resmi belirtebilirsiniz. Oturum açma ekranına ait arka plan görüntülerinde olduğu gibi, dosya boyutu olabildiğince küçük tutulmalıdır.

> [!NOTE]
> **Sağ** düzeni ve tarih/saat görünümü, oturum açma ekranına sıkıştırılmış görünümde uygulanmaz.

## <a name="screen-layouts"></a>Ekran düzenleri

Ekran düzeni yapılandırmaları POS **Hoş geldiniz** ekranındaki ve **Hareket** ekranındaki eylemleri, içeriği ve kullanıcı arabirimi denetimlerinin yerleşimini belirler.

![POS Ekranı düzeninin görünümü](../commerce/media/POS-Screen-Layout-View.png)

- **Hoş Geldiniz ekranı** – Çoğu durumda, hoş geldiniz ekranı, kullanıcıların POS'ta ilk oturum açtıklarında gördüğü sayfadır. Hoş geldiniz ekranı bir marka görüntüsünden ve POS işlemlerine erişim sağlayan düğme gruplarından oluşabilir. Genellikle, geçerli harekete özgü olmayan işlemler bu ekrana yerleştirilir.

    ![POS hoş geldiniz ekranı](../commerce/media/POS-Welcome-Screen.png)

- **Hareket ekranı** – **Hareket** ekranı, POS'ta satış hareketlerinin ve siparişlerin işlendiği ana ekrandır. İçerik ve düzen, ekran düzeni tasarımcısıyla yapılandırılır.

    ![POS Hareket ekranı](../commerce/media/POS-Transaction-Screen.png)

- **Varsayılan başlangıç ekranı** – Bazı perakendeciler kasiyerlerin oturum açtıktan sonra doğrudan **Hareket** ekranına gitmesini tercih eder. **Varsayılan başlangıç ekranı** ayarı, oturum açıldıktan sonra, her ekran düzeni için varsayılan ekranı belirtmenize olanak sağlar.

### <a name="assignment"></a>Atama

Ekran düzenleri mağaza, kasa veya kullanıcı düzeyinde atanabilir. Kullanıcı ataması kasa ve mağaza atamalarını geçersiz kılar; kasa ataması ise mağaza atamasını geçersiz kılar. Tüm kullanıcıların, kasa veya rol ne olursa olsun, aynı düzeni kullandığı basit bir senaryoda ekran düzeni yalnızca mağaza düzeyinde ayarlanabilir. Belirli kasalar veya kullanıcılar için özelleştirilmiş düzenlerin gerektiği senaryolarda, bu düzenler atanabilir.

### <a name="layout-sizes"></a>Düzen boyutları

POS kullanıcı arabiriminin çoğu özelliği duyarlı olduğu için, düzen, ekran boyutuna ve yönüne göre otomatik olarak yeniden boyutlandırılır ve ayarlanır. Bununla birlikte, POS **Hareket** ekranı, beklenen her ekran çözünürlüğü için yapılandırılmalıdır.

POS uygulaması, başlangıçta, cihaz için yapılandırılmış en yakın düzen boyutunu otomatik olarak seçer. Bir ekran düzeni hem yatay hem de dikey modlara ve hem en büyük hem de küçük cihazlara yönelik yapılandırmalar da içerebilir. Bu sayede, kullanıcılar mağazada kullanılan farklı boyutlarda ve form faktörlerinde çalışan tek bir ekran düzenine atanabilir.

![POS düzen boyutları](../commerce/media/POS-Screen-Layout-Sizes.png)

- **Ad** – Ekran boyutunu bildiren bir ad girebilirsiniz.
- **Düzen türü** – POS uygulaması, belirli bir cihazda en iyi kullanıcı deneyimi sağlamak için, kendi kullanıcı arabirimini çeşitli modlarda gösterebilir.

    - **Modern POS - Tam** – Tam düzenler genellikle masaüstü monitör veya tablet gibi daha geniş ekranlar için en uygun düzendir. Dahil edilecek kullanıcı arabirimi öğelerini seçebilir, bu öğelerin boyutunu ve yerleşimini belirtebilir ve ayrıntılı özelliklerini yapılandırabilirsiniz. Tam düzenler hem dikey hem de yatay yapılandırmaları destekler.
    - **Modern POS – Kompakt** – Kompakt düzenler, genellikle telefonlar veya küçük tabletler için en uygun düzenlerdir. Küçük cihazlar için tasarım olanakları sınırlıdır. Giriş ve toplam panelleri için sütunları ve alanları yapılandırabilirsiniz.

- **Genişlik/Yükseklik** – Bu değerler, düzen için beklenen geçerli ekran boyutunu piksel cinsinden gösterir. Bazı işletim sistemlerinin yüksek çözünürlüklü ekranlar için ölçekleme kullandığını unutmayın.

> [!TIP]
> Uygulamada çözünürlüğü görüntüleyerek, POS ekranı için gereken düzen boyutunu öğrenebilirsiniz. POS'u başlatın ve **Ayarlar \> Oturum bilgileri**'ne gidin. POS, o anda yüklü olan ekran düzenini, düzen boyutunu ve uygulama penceresinin çözünürlüğünü gösterir.

![O anda yüklü olan ekran düzenini, düzen boyutunu ve uygulama penceresinin çözünürlüğünü gösteren POS oturum bilgileri sayfası.](../commerce/media/POS-Session-Information.png)

### <a name="button-grids"></a>Düğme grupları

Bir ekran düzenindeki her düzen boyutu için, POS hoş geldiniz ekranına ve **Hareket** ekranına ilişkin düğme grupları yapılandırıp atayabilirsiniz. Hoş geldiniz ekranının düğme grupları otomatik olarak soldan sağa ve en düşük numaradan (Hoş geldiniz ekranı 1) en yüksek numaraya doğru yerleştirilir.

Tam POS düzenlerinde düğme gruplarının yerleşimi, ekran düzeni tasarımcısında belirtilir.

Kompakt POS düzenlerinde düğme grupları otomatik olarak yukarıdan aşağıya ve en düşük numaradan (Hareket ekranı 1) en yüksek numaraya doğru yerleştirilir. Bunlara **Eylemler** menüsünden erişilebilir.

![Kompakt düzen düğme grupları](../commerce/media/Compact-View-Button-Grids.png)

### <a name="images"></a>Resimler

Bir ekran düzenindeki her bir düzen boyutu için, POS kullanıcı arabirimine eklenecek resimleri belirtebilirsiniz. Tam POS düzenlerinde, hoş geldiniz ekranı için tek bir resim belirtilebilir. Bu resim, soldaki ilk kullanıcı arabirimi öğesi olarak görünür. **Hareket** ekranında resimler sekme resmi veya logo olarak kullanılabilir. Kompakt POS düzenleri bu resimleri kullanmaz.

### <a name="screen-layout-designer"></a>Ekran düzeni tasarımcısı

Ekran düzeni tasarımcısıyla, POS **Hareket** ekranının çeşitli özelliklerini her düzen boyutu için hem dikey hem de yatay modlarda ve hem Tam hem de Kompakt düzenler için yapılandırabilirsiniz. Ekran düzeni tasarımcısı, kullanıcı tarafından her erişildiğinde, uygulamanın en son sürümünü indirmek, yüklemek ve başlatmak için ClickOnce dağıtım teknolojisini kullanır. ClickOnce için tarayıcı gereksinimlerini kontrol ettiğinizden emin olun. Google Chrome gibi bazı tarayıcılar için uzantılar gerekir.

> [!IMPORTANT]
> Tanımlanan ve POS tarafından kullanılan Her düzen boyutu için bir ekran düzeni yapılandırmanız gerekir.

### <a name="full-layout-designer"></a>Tam düzen tasarımcısı

Tam düzen tasarımcısı, POS **Hareket** ekranına kullanıcı arabirimi denetimlerini sürüklemenize ve bu denetimlerin ayarlarını yapılandırmanıza olanak sağlar.

![POS Tam düzen tasarımcısı (yatay mod)](../commerce/media/POS-Full-Layout-Designer-Landscape.png)

- **Düzeni içe aktar/Düzeni dışa aktar** – POS ekran düzeni tasarımlarını XML dosyaları halinde içe veya dışa aktarabilir ve bu sayede kolaylıkla yeniden kullanabilir ve ortamlar arasında paylaşabilirsiniz. Doğru düzen boyutları için düzen tasarımlarını içe aktarmanız önemlidir. Aksi takdirde, kullanıcı arabirimi öğeleri ekrana doğru bir şekilde sığmayabilir.
- **Yatay/Dikey** – POS cihazı, kullanıcıların yatay ve dikey modlar arasında geçiş yapmasına izin veriyorsa, her mod için bir ekran düzeni tanımlamanız gerekir. POS ekran yönünü otomatik olarak algılar ve doğru düzeni gösterir.
- **Düzen kılavuzu** – POS düzen tasarımcısı 4 piksellik kılavuz kullanır. Kullanıcı arabirimi denetimleri kılavuza "tutunarak," içeriği doğru hizalamanıza yardımcı olur.
- **Tasarımcı yakınlaştırma** – Tasarımcı görünümünü yakınlaştırıp uzaklaştırarak POS ekranında içeriği daha iyi görüntüleyebilirsiniz. POS'taki ekran çözünürlüğü, tasarımcıda kullanılan ekranın çözünürlüğünden çok farklıysa bu özellik yararlı olur.
- **Gezinme çubuğunu göster/gizle** – Tam POS düzenleri için, soldaki gezinme çubuğunun **Hareket** ekranında görünüp görünmeyeceğini seçebilirsiniz. Bu özellik, düşük çözünürlüklü ekranlar için yararlıdır. Görünürlüğü ayarlamak için, tasarımcıdaki gezinti çubuğuna sağ tıklayıp **Her zaman görünür** onay kutusunu işaretleyin veya kutudaki işareti kaldırın. Gezinti çubuğu gizliyse, POS kullanıcıları yine de sol üstteki menüden çubuğa erişebilir.

    ![Gezinti çubuğunu gösterme/gizleme](../commerce/media/Navigation-Bar.PNG)

- **POS denetimleri** – POS düzeni tasarımcısı aşağıdaki denetimleri destekler. Birçok denetimi, üstlerine sağ tıklayıp kısayol menüsünü kullanarak yapılandırabilirsiniz.

    ![POS kullanıcı arabirimi denetimleri](../commerce/media/POS-UI-Controls.png)

    - **Rakam takımı** - Rakam takımı, POS **Hareket** ekranında kullanıcı girişi için ana mekanizmadır. Denetimi yapılandırarak rakam takımının tamamen gösterilmesini sağlayabilirsiniz. Bu seçenek dokunmatik ekranlı cihazlar için idealdir. Alternatif olarak, bu denetimi yalnızca giriş alanı gösterilecek şekilde yapılandırabilirsiniz. Bu durumda, giriş için fiziksel bir klavye kullanılır. Rakam takımı ayarları yalnızca Tam düzenlerde kullanılabilir. Kompakt düzenler için, **Hareket** alanında tam rakam takımı her zaman tam olarak gösterilir.
    - **Toplamlar paneli** - Toplamlar panelini satır sayısı, indirim tutarı, giderler, alt toplam ve vergi gibi değerleri göstermek üzere bir veya iki sütun halinde yapılandırabilirsiniz. Kompakt düzenler yalnızca bir sütunu destekler.
    - **Giriş paneli** - Giriş paneli, POS'ta işlenen ürünler ve hizmetler için satış satırlarını, ödeme satırlarını ve teslimat bilgilerini içerir. Sütunları, genişlikleri ve yerleşimi belirtebilirsiniz. Kompakt düzenlerde ana satır altındaki satırda görünen ek bilgileri de yapılandırabilirsiniz.
    - **Müşteri kartı** – Müşteri kartı, mevcut hareketle ilişkili müşteri hakkındaki bilgileri gösterir. Müşteri kartını, ek bilgiler gösterecek veya gizleyecek şekilde yapılandırılabilirsiniz.
    - **Sekme denetimi** - Bir ekran düzenine sekme denetimi ekleyebilir ve ardından rakam takımı, müşteri kartı, düğme grupları gibi başka denetimleri içine yerleştirebilirsiniz. Sekme denetimi, ekrana daha fazla içerik sığdırmanıza yardımcı olan bir kapsayıcıdır. Sekme denetimi yalnızca Tam düzenler için kullanılabilir.
    - **Görüntü** - **Hareket** ekranında mağaza logosunu veya diğer marka görüntülerini göstermek için görüntü denetimini kullanabilirsiniz. Görüntü denetimi yalnızca Tam düzenler için kullanılabilir.
    - **Önerilen ürünler** - Ortam için yapılandırılması durumunda, önerilen ürünler denetimi makine öğrenimini temel alarak ürün önerileri gösterir.
    - **Özel denetim** – Özel denetim, ekran düzeni içinde bir yer tutucu gibi davranarak, özel içerik için yer ayırmanıza olanak sağlar. Özel denetim yalnızca Tam düzenler için kullanılabilir.

### <a name="compact-layout-designer"></a>Kompakt düzen tasarımcısı

Tam düzen tasarımcısı gibi, Kompakt düzen tasarımcısı da telefonlar ve küçük tabletler için POS ekran düzenini yapılandırmanıza olanak sağlar. Ancak bu durumda düzenin kendisi sabittir. Düzendeki denetimleri, üstlerine sağ tıklayıp kısayol menüsünü kullanarak yapılandırabilirsiniz. Bununla birlikte, ek içerik için sürükle-bırak işlemlerini kullanamazsınız.

![Kompakt düzen tasarımcısı](../commerce/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Düğme grubu tasarımcısı

Düğme grubu tasarımcısı, POS hoş geldiniz ekranında ve **Hareket** ekranında Tam ve Kompakt düzenler için kullanılabilecek düğme grupları yapılandırmanıza olanak sağlar. Aynı düğme grubu, farklı düzenlerde ve düzen türlerinde kullanılabilir. Ekran düzeni tasarımcısı gibi, düğme grubu tasarımcısı, kullanıcı tarafından her erişildiğinde, uygulamanın en son sürümünü indirmek, yüklemek ve başlatmak için ClickOnce dağıtım teknolojisini kullanır. ClickOnce için tarayıcı gereksinimlerini kontrol ettiğinizden emin olun. Google Chrome gibi bazı tarayıcılar için uzantılar gerekir.

![Düğme grubu tasarımcısı](../commerce/media/Button-Grid-Designer.png)

- **Yeni düğme** – Düğme grubuna yeni bir düğme eklemek için tıklayın. Varsayılan olarak, yeni düğmeler kılavuzun sol üst köşesinde görünür. Bununla birlikte, düğmeleri sürükleyerek düzende yerleştirebilirsiniz.

    > [!IMPORTANT]
    > Düğmeg grubunun içerikleri çakışabilir. Düğmelerin yerleşimini düzenlerken diğer düğmeleri örtmediklerinden emin olun.

- **Yeni tasarım** – Satır ve sütun başına düğme sayısını belirterek bir düğme grubu düzenini otomatik şekilde ayarlamak için tıklayın.
- **Düğme özellikleri** – Düğme özelliklerini, düğmeye sağ tıklayıp kısayol menüsünü kullanarak yapılandırabilirsiniz.

    > [!IMPORTANT]
    > Bazı düğme grubu ayarları Modern POS'ta veya Cloud POS'ta değil, yalnızca Enterprise POS'ta geçerlidir.

    ![Düğme grubu düğme özellikleri](../commerce/media/Button-grid-button-properties.png)

    - **Eylem** – İlgili POS işlemleri listesinde, POS'ta düğme tıklanınca çağrılacak işlemi seçin.

        Desteklenen POS işlemlerinin listesi için bkz. [Çevrimiçi ve çevrimdışı satış noktası (POS) işlemleri](pos-operations.md).

    - **Eylem parametreleri** – Bazı POS işlemleri, çağrıldıkları zaman ek parametreler kullanır. Örneğin, Ürün ekle işlemi için, kullanıcılar eklenecek ürünü belirtebilir.
    - **Düğme metni** – POS'taki düğmede görüntülenecek metni belirtin.
    - **Düğme metnini gizle** – Düğme metnini göstermek veya gizlemek için bu onay kutusunu kullanın. Yalnızca bir simge gösteren küçük düğmelerde düğme metni çoğu zaman gizlidir.
    - **Araç ipucu** – Kullanıcılar fareyi düğme üzerine getirdiği zaman görünecek ek Yardım metni belirtin.
    - **Sütun olarak boyut/Satır olarak boyut** – Düğmenin yüksekliğini ve genişliğini belirtebilirsiniz.

        ![Satır ve sütun olarak POS düğme boyutları](../commerce/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Özel yazı tipi** – **POS için özel yazı tipini etkinleştir** onay kutusunu işaretlediğiniz zaman, POS için varsayılan sistem yazı tipinden farklı bir yazı tipi belirtebilirsiniz.
    - **Özel tema** – Varsayılan olarak, POS düğmeleri görsel profilden alınan vurgu rengini kullanır. **Özel tema kullan** onay kutusunu işaretlediğiniz zaman, ek renkler belirtebilirsiniz.

        > [!NOTE]
        > Modern POS ve Cloud POS yalnızca **Arka plan rengi** ve **Yazı tipi rengi** değerlerini kullanır.

    - **Düğme görüntüsünü** – Düğmeler görüntü veya simgeler içerebilir. **Perakende ve Ticaret \> Kanal kurulumu \> POS kurulumu \> POS \> Resimler**'de belirtilen kullanılabilir görüntülerden seçim yapın.

![POS'ta düğme grubu örneği](../commerce/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Retail satış noktası (POS) düzeni tasarımcısını yükleme](install-pos-layout-designer.md)
