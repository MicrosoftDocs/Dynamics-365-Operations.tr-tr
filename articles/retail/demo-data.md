---
title: "MPOS/CPOS'taki tanıtım verileri ekranı düzenleri"
description: "Bu konu, Microsoft Dynamics 365 for Retail'deki satış noktası (POS) deneyimleriyle ilgili tanıtım verileri kümesiyle dahil edilen ekran düzenlerine ilişkin bilgiler sağlar."
author: zlinster
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: zlinster
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 563c89c75e2136294f8f841bec094c2aeb85d580
ms.openlocfilehash: b758b48230e8d9fabdccbe267a6ad6b9e74af0ff
ms.contentlocale: tr-tr
ms.lasthandoff: 10/17/2017

---

# <a name="demo-data-screen-layouts-in-mposcpos"></a>MPOS/CPOS'taki tanıtım verileri ekranı düzenleri

[!include[banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 for Retail'deki satış noktası (POS) deneyimleriyle ilgili tanıtım verileri kümesiyle dahil edilen ekran düzenlerine ilişkin bilgiler sağlar.

## <a name="overview"></a>Özet

Retail tanıtım verileriyle birlikte gelen örnek ekran düzenleri çeşitli perakende segmentleri, mağaza çalışanı rolleri ve cihazlar için optimize edilmiş içerikler sağlar. Mağaza çalışanları cihazlar ve çözümler arasında geçiş yaparken kapsamın sağlanmasına yardımcı olmak amacıyla tek bir düzen çeşitli düzen boyutları ve kombinasyonları içerebilir. Bu konu bu düzenler, sağladıkları işlemler ve sundukları genel deneyimler arasındaki farklılıkları açıklar.

![Cihazlar arası tanıtım verileri düzenleri](../retail/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Bir ekran düzeni kodunun anatomisi

Retail'de ekran düzenlerini bulmak için **Retail** > **Kanal kurulumu** > **POS kurulumu** > **POS** > **Ekran düzenleri**'ne gidin.

![Retail'deki ekran düzenleri sayfası](../retail/media/demo-screen-layouts-fig-2-1.png)

Ekran düzeni kodları en çok 10 karaktere sahip olabilir. Kod, üç bilgi parçasından oluşan bir dizedir. Bu siparişte:

1. Şirket
2. Düzen sürümü
3. Kişi

### <a name="company"></a>Şirket

| Mektup | Şirket         |
|--------|-----------------|
| A      | Adventure Works |
| F      | Fabrikam        |
| Ş      | Contoso         |

### <a name="layout-version"></a>Düzen sürümü

| Sürüm numarası | Tanım                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Çeşitli cihazlar ve en-boy oranları için birden fazla ekran boyutunu destekleyen temel sürüm |
| 3.1            | **Önerilen ürünler** paneli için ek destek sağlayan temel sürüm        |

### <a name="persona"></a>Kişi

| Kısaltma | Kişi       | İçindekiler |
|--------------|---------------|----------|
| CSH          | Kasiyer       | Kasiyer düzenleri müşteri siparişleri, iadeler, indirimler, geçersiz kılmalar ve hediye kartları gibi tüm hareketlerle ilgili işlemleri içerir. Bu düzenler ayrıca fiyat denetimleri, stok aramaları ve stok sayımları gibi stok yönetimiyle ilgili günlük görevleri de içerir. Başlangıç tutarları, beklemede olan vardiyalar ve saat gibi temel vardiya yönetimi de sağlanır. |
| MGR          | Mağaza Yöneticisi | Mağaza Yöneticisi düzenlerini Kasiyer düzenlerinde bulunan tüm hareketlerle ilgili işlemleri ve vergi geçersiz kılma işlemlerini içerir. Bu düzenler ayrıca fiyat denetimleri, stok aramaları ve stok sayımları gibi stok yönetimiyle ilgili günlük görevleri de içerir. Vardiyaları başlatma, beklemeye alma ve kapatma için vardiya yönetimi özelliği de sağlanır. Ayrıca, düzenler girişler, çıkarmalar, kasa sayımları ve kasaya ve bankaya para nakliyle ilgili çekmece işlemlerini içerir. Son olarak, bu düzenler performans raporlarına erişim içerir ve X ve Z raporlarının yazdırılabilmesini sağlar. |
| STK          | Stok Memuru   | Stok Memuru düzenleri stok yönetimi için optimize edilmiştir. Bunlar fiyat denetimleri, stok aramaları, malzeme çekme ve teslim alma, stok sayımları ve set ayrıştırmayla ilgili günlük görevlere erişim içerir. Bu düzenler saat ve askıya alınan vardiyalarla ilgili temel vardiya işlemlerini de sağlar. Bu düzenler temel olarak arka ofis görevleriyle ilgili olmakla birlikte, stok memurları da hareket ekranlarında kasiyerlerle aynı işlemlere sahiptir. |

### <a name="example-layout"></a>Örnek düzen

Burada Fabrikam şirketi, düzen sürümü 3 ve Mağaza Yöneticisi kişisi için bir ekran düzeni kodu örneği verilmektedir:

F3MGR

Aşağıdaki şekilde Fabrikam mağaza yöneticisinin Karşılama ekranının örneği gösterilmektedir.

![Fabrikam mağaza yöneticisi için Karşılama ekranı](../retail/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Düzen boyutları

### <a name="full-vs-compact-layouts"></a>Tam düzenler ile kompakt düzenler

Ekran düzeninde hem tam hem de kompakt cihazlar için yapılandırmalar bulunabilir. Bu nedenle, bir kullanıcı mağaza içindeki farklı boyutlar ve form faktörlerinde çalışacak tek bir ekran düzenine atanabilir.

- **Modern POS - Tam** - Tipik olarak, tam düzenler genellikle en iyi masaüstü bilgisayar ekranları veya tabletler gibi geniş ekranlarda kullanılır. Kullanıcılar düzenin içerdiği kullanıcı arabirimi öğelerini seçebilir, bu öğelerin yerleşimini ve boyutunu belirleyebilir ve ayrıntılı özelliklerini yapılandırabilir. Tam düzenler hem dikey hem de yatay yapılandırmaları destekler.
- **Modern POS - Kompakt** - Tipik olarak kompakt düzenler genellikle telefonlar veya küçük tabletler için uygundur. Küçük cihazlar için tasarım olanakları sınırlıdır. Kullanıcılar giriş bölmesi ve toplam bölmesi için sütunları ve alanları yapılandırabilir.

### <a name="screen-resolutions-that-are-provided"></a>Sağlanan ekran çözünürlükleri

Aşağıdaki tablo normal ekran çözünürlükleri için sağlanan düzen boyutlarını gösterir.

| Düzen türü | Çözünürlük | En boy oranı | Hedef ekran          |
|-------------|------------|--------------|-------------------------|
| Sıkıştır\*   | 480 × 853  | 16:9         | Telefonlar                  |
| Dolu        | 1024 × 768 | 4:3          | Tabletler                 |
| Dolu\*      | 1280 × 720 | 16:9         | Tabletler                 |
| Dolu        | 1366 × 768 | 16:9         | Tabletler, daha geniş ekran |
| Dolu        | 1440 × 960 | 3:2          | Tabletler, daha geniş ekran |

\* Bu ek düzenler yalnızca Adventure Works ve Fabrikam düzenlerinde kullanılabilir.


>[!TIP]
> POS, geçerli uygulama penceresinin ekran çözünürlüğü için kullanılabilir olan en yakın boyutu temel alarak düzen boyutlarını otomatik olarak seçer. Kullanılmakta olan ekran düzeni kodunu ve düzen çözünürlüğünü bulmak için, Retail Modern POS (MPOS) veya Retail Cloud POS (CPOS)'ta **Ayarlar** sayfasını açın ve **Oturum bilgileri** bölümüne bakın. Geçerli uygulamanızın veya tarayıcı pencerenizin gerçek çözünürlüğünü de görebilirsiniz. Bu bilgileri aldıktan sonra, düzen içeriğinin kaynağını Retail içinde **Kanal kurulumu** > **POS kurulumu** > **POS** > **Ekran düzenleri**'ne giderek bulabilirsiniz.


![Retail ve POS'taki ekran düzenleri ve düzen çözünürlükleri/boyutları](../retail/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Şirketler ve markalar

Her hayali şirket farklı bir perakende segmenti için hedeflenmiştir ve şirketin pazarına göre ayarlanmış ürün kataloglarına sahiptir. Her şirketin ürünlerine eşlik eden benzersiz görsel markası bulunur. Marka öğeleri vurgu rengini, açık veya koyu temayı ve gerçekçi deneyimler sağlayan fotoğrafları içerir.

### <a name="company-segment-and-visual-characteristics"></a>Şirket segmenti ve görsel özellikler

| Şirket         | Yer |  segmenti        | Vurgu | Tema |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Spor Eşyaları | Mavi   | Koyu  |
| Fabrikam        | Houston  | Moda        | Yeşil  | Açık |
| Contoso         | Boston   | Elektronik    | Kırmızı    | Koyu  |


>[!NOTE]
> Adventure Works ve Fabrikam iki lider markadır. Contoso kullanılabilir, ancak tüm düzenler sağlanmaz.


Aşağıdaki örneklerde üç hayali şirket için karşılama sayfası ve işlem sayfası örnekleri gösterilmektedir.

### <a name="adventure-works"></a>Adventure Works

![Adventure Works için tanıtım verileri karşılama sayfası](../retail/media/demo-screen-layouts-fig-4-1a.png)

![Adventure Works için tanıtım verileri hareket sayfası](../retail/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Fabrikam için tanıtım verileri karşılama sayfası](../retail/media/demo-screen-layouts-fig-4-2a.png)

![Fabrikam için tanıtım verileri hareket sayfası](../retail/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Contoso için tanıtım verileri düzenler](../retail/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Kullanıcı oturum açma matrisi

Kullanıcılara çeşitli ekran düzenleri sağlanmıştır. Aşağıdaki tabloyu kullanarak, herhangi bir ekrana erişmeniz mümkün olmalıdır. Uygun işleç kimliği kullanarak oturum açmanız yeterlidir.

| Şirket         | Ekran düzeni kodu | Kişi          | İşleç kodları           |
|-----------------|------------------|---------------   |------------------------|
| Adventure Works | A3MGR            | Mağaza Yöneticisi    | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Kasiyer          | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Stok Memuru      | 000155, 000181, 000152 |
| Fabrikam        | F3MGR            | Mağaza Yöneticisi    | 000160, 000168, 000163 |
| Fabrikam        | F3CSH            | Kasiyer          | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Stok Memuru      | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Mağaza Yöneticisi    | 000100, 000111         |
| Contoso         | C3CSH            | Kasiyer          | 000110, 000120         |
| Contoso         | Uygulanamaz   | Stok Memuru      | Uygulanamaz         |


>[!TIP]
> En iyi sonuçları elde etmek için, ilgili mağaza konumundaki karşılık gelen bir kaydı etkinleştirin ve şirketi oturum açarken kullanmayı planladığınız kişinin şirketine ayarlayın. Bu şekilde, görsel profilin ve marka resimlerinin deneyim süresince uyumlu olmasını sağlamaya yardımcı olursunuz. Örneğin, bir kasiyer için Fabrikam düzenini görmek istiyorsanız, Houston mağazasındaki bir kaydı etkinleştirmeniz gerekir.


<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail > Channel setup > POS setup > POS > Images**. -->

<!-- ![Images in Dynamics 365 for Retail](../retail/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../retail/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->

