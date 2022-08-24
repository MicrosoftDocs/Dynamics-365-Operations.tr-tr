---
title: POS'ta stok arama işlemi
description: Bu makale, mağazalar ve ambarlar genelinde ürünlerin eldeki stok kullanılabilirliğini görüntülemek için stok arama işleminin Dynamics 365 Commerce satış noktasında (POS) nasıl kullanılacağını açıklar.
author: boycezhu
ms.date: 08/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: fc8c7dad0a7cb66ba7d6c6f527be84cfe74dee52
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288338"
---
# <a name="inventory-lookup-operation-in-pos"></a>POS'ta stok arama işlemi

[!include [banner](includes/banner.md)]

Bu makale, mağazalar ve ambarlar genelinde ürünlerin eldeki stok kullanılabilirliğini görüntülemek için stok arama işleminin Dynamics 365 Commerce satış noktasında (POS) nasıl kullanılacağını açıklar.

Bir kuruluştaki stoğun doğru görünümü mağaza görevlilerinin zamanında, etkili müşteri hizmeti sunmasını sağlar. En önemli olan zaman, müşterilerin satın alma kararını vermeye hazır olduğu andır. Perakende mağazasındaki kasiyerlerin gerçek zamanlı veya neredeyse gerçek zamanlı bilgileri parmaklarının ucunda bulması çok önemlidir; böylece ürün teslimatı ve alınması için doğru şekilde taahhütte bulunabilirler.

Commerce POS'taki stok arama işlemi, perakendecilere mağazalarını Commerce genel merkeze bağlayarak operasyonel mükemmeliyet kazanmalarına ve bilgiler edinmelerine olanak tanır. Bu işlev, mağazalar ve ambarlar genelinde ürünlerin stok kullanılabilirliği görünümünü sağlar. Ayrıca, stok planlamasını gerçek zamanlı geliştirerek perakendecilerin ek verimlilik ve maliyet tasarrufu sağlamasına yardımcı olur.

Stok arama işlemi POS uygulamasından başlatıldığında, POS kasiyeri stok bilgilerini sorgulamak üzere bir ürün numarası girmek için sayısal klavyeyi kullanır. Girilen ürünün çeşitleri varsa, kasiyer isteğe bağlı olarak belirli bir ürün çeşidinin stok bilgilerini denetlemek için boyutları veya diğer değerleri seçebilir.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Bağımsız ürünler için stok arama listesi görünümü

Tek bir ürün için stok arama işlemi, bir yerleşim listesi ile ilgili olarak aşağıdaki ürün bilgilerini gösteren bir stok arama listesi görünümü sağlar:

- **Stok**: Bir ürünün "kullanılabilir fiziksel" miktarını ifade eder.
- **Ayrılmış**: Genel merkezden alınan "fiziksel olarak rezerve edilmiş" miktarı ifade eder.
- **Sipariş edilen**: Genel merkezden alınan "toplam sipariş edilen" miktarı ifade eder.
- **Birim**: Genel merkezde yapılandırılan stok ölçü birimini ifade eder.

Yerleşimlerin liste görünümü, aşağıdaki örnek görüntüde gösterildiği gibi, geçerli mağazanın bağlantılı olduğu karşılama gruplarında yapılandırılan tüm mağaza ve ambarları içerir.

![Stok arama işlemi liste görünümü.](media/inventory-lookup-list-view.png)

> [!NOTE]
> Geçerli mağazanızın ilişkili karşılama gruplarına dahil edildiğinden emin olun.

Aşağıdaki eylemler, POS uygulama çubuğundan kullanılabilir:

- **Sırala**: Bu eylem, POS kullanıcısının, liste görünümündeki verileri çeşitli ölçütlere göre sıralamasına izin verir. Yerleşim temelli sıralama, varsayılan sıralama seçeneğidir.

    - **Coğrafi konum** (geçerli mağazaya olan mesafeye göre en yakın yerleşimden en uzak yerleşime)
    - **Ad** (artan veya azalan sırada)
    - **Mağaza numarası** (artan veya azalan sırada)
    - **Stok** (azalan sırada)
    - **Ayrılmış** (azalan sırada)
    - **Sipariş edilmiş** (azalan sırada)

- **Filtre**: Bu eylem, POS kullanıcısının belirli bir yerleşim için filtre uygulanmış verileri görüntülemesine olanak tanır.
- **Mağaza kullanılabilirliğini göster**: Bu eylem, POS kullanıcısının seçili mağazadaki bir ürünle ilgili olarak kullanılabilir taahhüt (KM) miktarlarını görüntülemesine olanak tanır.
- **Mağaza konumunu göster**: Bu eylem, seçili mağazaya ait harita görünümü, adres ve mağaza saatlerini göstermek için ayrı bir sayfa açar.
- **Mağazadan teslim al**: Bu eylem, seçilen mağazadan teslim alınacak ürün için bir müşteri siparişi oluşturur ve kullanıcıyı hareket ekranına yönlendirir.
- **Ürün sevk et**: Bu eylem, seçilen mağazadan sevk edilecek ürün için bir müşteri siparişi oluşturur ve kullanıcıyı hareket ekranına yönlendirir.
- **Tüm çeşitleri görüntüle**: Bu eylem, çeşitleri olan bir ürün için liste görünümünden ürünün tüm çeşitleriyle ilgili stok bilgilerini görüntüleyen bir matris görünümüne geçer.
- **Harekete ekle**: Bu eylem, ürünü alışveriş sepetine ekler ve kullanıcıyı hareket ekranına yönlendirir.

> [!NOTE]
> Commerce 10.0.17 sürümünde tanıtılan yerleşim temelli sıralama, geçerli mağazayı en üstte gösterir. Diğer yerleşimler için yerleşim ve geçerli mağaza arasındaki mesafe, Commerce genel merkezde tanımlanan koordinatlara göre (enlem ve boylam) belirlenir. Mağaza için, yerleşim bilgileri mağazayla ilişkilendirilmiş olan faaliyet biriminin birincil adresinde tanımlanmıştır. Mağaza olmayan ambar için, yerleşim bilgileri ambar adresinde tanımlanmıştır. 10.0.17'den önceki sürümlerde liste görünümü her zaman geçerli mağazayı en üstte gösterir ve diğer yerleşimleri alfabetik olarak sıralar.
>
> **Mağaza kullanılabilirliğini göster**, **Mağaza konumunu göster**, **Mağazada teslim al** ve **Ürünü sevk et** eylemleri, mağaza dışı yerleşimlerde kullanılamaz.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Çeşitler için stok arama matrisi görünümü

Çeşitleri bulunan bir ana ürün için stok arama işlemi, ana ürünün seçilen yerleşimdeki tüm çeşitlerini görüntülemek üzere stok kullanılabilirlik bilgilerini görüntüleyen bir boyut tabanlı matris görünümü de sağlar. Varsayılan olarak, matris görünümü geçerli mağazanın verilerini gösterir. Geçerli mağazanın bağlantılı olduğu karşılama gruplarında yapılandırılan diğer mağazalardaki stok bilgilerini aramak için uygulama çubuğundaki **Mağaza** eylemini kullanabilirsiniz.

Aşağıdaki örnek görüntü, POS'ta bulunan stok arama matrisi görünümünü gösterir.

![Stok arama işlemi matris görünümü.](media/inventory-lookup-matrix-view.png)

Matris görünümünde, her hücre tek bir çeşidi temsil eder ve sağ alt köşede bulunan eldeki stok (kullanılabilir fiziksel) ve sol üst köşedeki **ayrılmış** (fiziksel ayrılan) ve **sipariş edilmiş** (toplam sipariş edilen) değerleri de görüntülenir. Aşağıdaki tablo, çeşitli eldeki değerlerin anlamını açıklar.

| Eldeki değer                            | Tanım |
|------------------------------------------|-------------|
| 0 (sıfır)'dan büyük olan sayısal değer | Seçili yerleşime bir ürün çeşidi serbest bırakılmıştır ve hücrede ek eylemler gerçekleştirebilirsiniz. |
| **0** (sıfır)                             | Bir ürün çeşidi seçili yerleşime serbest bırakılır ancak madde seçili yerleşimde kullanılabilir değildir. Hücrede ek eylemler gerçekleştirebilirsiniz. |
| **yok** veya etkin olmayan bir hücre              | Seçili yerleşime bir ürün çeşidi serbest bırakılmamıştır ve hücrede ek eylemler gerçekleştiremezsiniz. |

Matris görünümündeki boyut değerlerinin görüntülenme düzeni, Commerce genel merkezdeki boyut görüntüleme sırası yapılandırmasını temel alır. Kullanılacak yeni bir boyut seçerek boyut görüntüleme sırası yapılandırmasını değiştirebilirsiniz. 

Aşağıdaki eylemler, matris görünümü hücresinde kullanılabilir:

- **Şimdi sat**: Bu eylem, seçili ürün çeşidini alışveriş sepetine ekler ve kullanıcıyı hareket ekranına yönlendirir.
- **Mağazadan teslim al**: Bu eylem, seçilen mağazadan teslim alınacak ürün çeşidi için bir müşteri siparişi oluşturur ve kullanıcıyı hareket ekranına yönlendirir.
- **Ürün sevk et**: Bu eylem, seçilen mağazadan sevk edilecek ürün çeşidi için bir müşteri siparişi oluşturur ve kullanıcıyı hareket ekranına yönlendirir.
- **Kullanılabilirlik**: Bu eylem kullanıcıyı seçili mağazada seçili ürün çeşidi için KM miktarlarını gösteren ayrı bir sayfaya götürür.
- **Tüm yerleşimleri göster**: Bu eylem, seçilen ürün çeşidinin stok bilgilerini gösteren standart stok kullanılabilirliği listesi görünümüne geçer.
- **Ürün ayrıntılarını görüntüle**: Bu eylem, kullanıcıyı seçili ürün çeşidinin ürün ayrıntıları sayfasına (PDP) yönlendirir.

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>POS'taki diğer sayfalardan stok aramasına erişim

POS kullanıcıları, stok arama işlemine POS'taki diğer sayfalardan da erişebilir.

Aşağıdaki örnek görüntü, POS'taki bir PDP'de stok arama sonuçlarını gösterir.

![Ürün ayrıntıları sayfasından stok arama.](media/inventory-lookup-from-product-details-page.png)

Bir ana ürünün PDP'si üzerinde, geçerli mağazanın bir ürünün tüm çeşitlerine ait stok kullanılabilirlik bilgilerini görüntüleyen stok arama matrisi görünümünü başlatmak için uygulama çubuğundaki **Tüm çeşitleri görüntüle** eylemini kullanabilirsiniz. Tek bir ürün için, PDP geçerli mağazada o ürünün eldeki stok (kullanılabilir fiziksel) değerini görüntüler. Ek olarak, diğer mağazalar veya ambarlarda bir ürünün stok kullanılabilirliğini denetlemek üzere stok arama işlemini başlatmak için **Diğer mağazaların stokları** bağlantısını da seçebilirsiniz.

> [!NOTE]
> PDP'de **Tüm ürün çeşitlerini görüntüle** eylemi, yalnızca ürün çeşitleri bulunan ana ürünler için kullanılabilir. Belirli ürünler veya setler için kullanılamaz.

Stok arama işlemini, POS hareket ekranındaki düğme kılavuzunda bir bağlantı olarak görüntülenecek şekilde yapılandırabilirsiniz. Yapılandırmadan sonra, kullanıcı bir sepet satırı seçip daha sonra **Stok arama** düğmesini seçtiğinde, seçili ürün için stok arama listesi görünümü görüntülenir. POS ekranı düzen tasarımcısı aracını kullanarak düğme ızgaralarını yapılandırma hakkında daha fazla bilgi için bkz. [POS kullanıcı arabirimi görsel yapılandırmaları](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Kanal tarafı hesaplama ile stok araması

Commerce 10.0.9 ve önceki sürümlerde, stok arama işlemindeki **kullanılabilir fiziksel** değeri, gerçek zamanlı servis çağrısı aracılığıyla Commerce genel merkezden alınır. Commerce 10.0.10 ve sonraki sürümlerde, henüz genel merkezle eşitlenmemiş hareket verileri hesaba katarak eldeki stoğun daha güvenilir ve daha doğru tahminini sağlayabilen kullanılabilir fiziksel değeri belirlemek için, POS stok arama işlemini Commerce sunucusunda kanal taraflı hesaplamayı kullanacak şekilde yapılandırabilirsiniz. Kanal taraflı stok hesaplaması ve genel merkezde ilgili POS yapılandırmaları hakkında daha fazla bilgi için bkz. [Perakende kanalları için stok kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Ek kaynaklar

[POS kullanıcı arabirimi görsel yapılandırmaları](pos-screen-layouts.md)

[Perakende kanalları için stok kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
