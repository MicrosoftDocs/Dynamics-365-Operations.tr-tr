---
title: Öznitelikler ve öznitelik gruplarını yönetme
description: Bu makalede, Microsoft Dynamics 365 Commerce'de ürünleri ve özelliklerini açıklamak amacıyla özniteliklerin ve öznitelik gruplarının nasıl yönetildiği açıklanır.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386985"
---
# <a name="manage-attributes-and-attribute-groups"></a>Öznitelikler ve öznitelik gruplarını yönetme

[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'de ürünleri ve özelliklerini açıklamak amacıyla özniteliklerin ve öznitelik gruplarının nasıl yönetildiği açıklanır.

*Öznitelikler* kullanıcı tanımlı alanlar aracılığıyla ürünleri ve özelliklerini açıklamanızı sağlar. Örnekler arasında bellek boyutu, sabit disk kapasitesi ve Energy Star uyumluluğu bulunur.

Öznitelikler ürün kategorileri ve kanalları gibi çeşitli Commerce varlıkları ile ilişkili olabilir ve bunlar için varsayılan değerler ayarlanabilir. Öznitelikler, ürün kategorileri veya kanallar ile ilişkilendirildiğinde ürünler bu öznitelikleri ve varsayılan değerlerini devralır. Varsayılan öznitelik değerleri tek tek ürün düzeyinde, kanal düzeyinde veya katalog düzeyinde geçersiz kılınabilir.

Örneğin, tipik bir televizyon ürünü aşağıdaki özniteliklere sahip olabilir.

| Kategori   | Öznitelik           | İzin verilen değerler                        | Varsayılan değer |
|------------|---------------------|-------------------------------------------|---------------|
| TV ve Video | Marka               | Herhangi bir geçerli marka değeri                     | Yok          |
| TV         | Ekran Boyutu         | 20–85 inç                              | 55 inç     |
|            | Dikey Çözünürlük | 4K (2160p), Full HD (1080p) veya HD (720p) | 4K (2160p)    |
|            | Ekran yenileme hızı | 60hz, 120hz veya 240hz                     | 60hz          |
|            | HDMI Girdileri         | 0–10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Öznitelikler ve öznitelik türleri

Öznitelikler *öznitelik türlerini* temel alır. Öznitelik türü, belirli bir öznitelik için girilebilen veri türünü tanımlar. Commerce'de aşağıdaki öznitelik türleri desteklenir:

- **Para birimi** – Bu tür bir para birimi değerini destekler. Bağlı olabilir (diğer bir deyişle, bir değer aralığı destekleyebilir) veya açık bırakılabilir.
- **DateTime** – Bu tür, tarih ve saat değerini destekler. Bağlı veya açık bırakılmış olabilir.
- **Ondalık** – Bu tür, ondalık basamak içeren sayısal değeri destekler. Ayrıca, ölçü birimini de destekler. Bağlı veya açık bırakılmış olabilir.
- **Tamsayı** – Bu tür sayısal bir değeri destekler. Ayrıca, ölçü birimini de destekler. Bağlı veya açık bırakılmış olabilir.
- **Metin** – Bu tür metin değerini destekler. **Sabit liste** ayarı etkinleştirildiğinde, olası önceden tanımlanmış değerler kümesini de destekler.
- **Boole** – Bu tür ikili değeri destekler (**doğru** veya **yanlış**).
- **Referans** – Bu tür diğer özniteliklere referansta bulunur.

> [!NOTE]
> [Azure arama dizini sınırlamaları](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search) nedeniyle **Ondalık** öznitelik türü, bulut destekli arama deneyimleri için desteklenmez. Azure Bilişsel Arama, **Ondalık** öznitelik türlerini **Edm.Double** hedef dizin alanı türlerine dönüştürmeyi desteklemez çünkü bu dönüşüm duyarlığı düşürebilir.

### <a name="set-up-attribute-types"></a>Öznitelik türlerini ayarla

Öznitelik türleri ayarlamak için bu örnek yordamdaki adımları izleyin.

1. Commerce headquarters'ta alım satım yöneticisi olarak oturum açın.
1. **Ürün bilgi yönetimi \> Kurulum \> Kategoriler ve öznitelikler \> Öznitelik türleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Öznitelik türü adı** alanına **Çanta türü** girin.
1. **Tür** alanında, **Metin**'i seçin.
1. **Sabit liste** seçeneğini **Evet** olarak ayarlayın.
1. **Değerler** hızlı sekmesinde **Ekle**'yi seçin.
1. Yeni satırda, **Değer** alanına **Omuz çantası** girin.
1. Beş satır daha ekleyin. Her biri için **Değer** alanına farklı bir değer girin: **El çantası**, **Askılı çanta**, **Sırt çantası**, **Postacı çantası** veya **Cüzdan**.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Öznitelik türü adı** alanına **Güneş gözlüğü markası** girin.
1. **Tür** alanında, **Metin**'i seçin.
1. **Sabit liste** seçeneğini **Evet** olarak ayarlayın.
1. **Değerler** hızlı sekmesinde **Ekle**'yi seçin.
1. Yeni satırda, **Değer** alanına **Ray ban** girin.
1. İki satır daha ekleyin. Her birine ait **Değer** alanına farklı bir değer girin: **Aviator** veya **Oakley**.
1. Eylem bölmesinde, **Kaydet**'i seçin.

![Öznitelik türleri sayfası.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Öznitelik ayarlama

Öznitelik ayarlamak için bu örnek yordamdaki adımları izleyin.

1. Commerce headquarters'ta alım satım yöneticisi olarak oturum açın.
1. **Ürün bilgi yönetimi \> Kurulum \> Kategoriler ve öznitelikler \> Öznitelikler**'e gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Ad** alanına, **Çanta türü** girin.
1. **Öznitelik türü adı** alanında **Çanta türü**'nü seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

![Öznitelikler sayfası.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Öznitelik meta verileri

*Öznitelik meta verisi* her ürün için özniteliklerin nasıl davranacağını belirtebileceğiniz seçenekler belirlemenize olanak tanır. Örneğin, özniteliklerin gerekli olup olmadığını, aramalar için kullanılıp kullanılamayacağını ve filtre olarak kullanılıp kullanılamayacağını belirtebilirsiniz.

Ürünler için, öznitelik meta verileri kanal düzeyinde geçersiz kılınabilir.

Bir özniteliğin **Öznitelikler** sayfası öznitelik meta verileriyle ilgili çeşitli seçenekler içerir. Örneğin, **Commerce kanalları için öznitelik metaverileri** altında **İyileştirilebilir** seçeneğini **Evet** olarak ayarlarsanız ürünlerin arama sonuçlarında ve kategori tarama sayfalarında iyileştirilmesi veya filtrelenmesi için öznitelik gösterilir. Özniteliği iyileştirilebilir olarak yapılandırmak için öncelikle Eylem Bölmesinde **Filtre ayarları**'nı seçmeniz ve öznitelik için filtre ayarlarını onaylamanız gerekir.

## <a name="filter-settings-for-attributes"></a>Öznitelik filtre ayarları

Özniteliklerin filtre ayarları, öznitelik filtrelerinin satış noktasında (POS) nasıl görüneceğini tanımlamanıza olanak tanır. Bir özniteliğe ilişkin filtre ayarlarına erişmek **Öznitelikler** sayfasında özniteliği seçin ve Eylem Bölmesine **Filtre ayarları**'nı seçin.

**Filtre ayarları** sayfası, aşağıdaki alanları içerir:

- **Ad** – Varsayılan olarak, bu alanın öznitelik adına ayarlanır. Ancak, değerde değişiklik yapabilirsiniz.
- **Görüntüleme seçeneği** – Aşağıdaki seçenekler mevcuttur:

    - **Tek bir değer** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Boole**, **Para birimi**, **Ondalık**, **Tamsayı** ve **Metin**. Kategori tarama ve ürün araması sonuç sayfaları gibi ürün listesi sayfasındaki iyileştiriciler için tek bir değer seçilmesine izin verir.
    - **Birden fazla değer** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Boole**, **Ondalık**, **Tamsayı** ve **Metin**. İstemcide iyileştirme için özniteliğe yönelik birden fazla değer seçilmesini sağlar.

- **Görüntüleme denetimi** – Aşağıdaki seçenekler mevcuttur:

    - **Liste** – Bu seçenek tüm öznitelik türleri için kullanılabilir.
    - **Aralık** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Para birimi**, **Ondalık** ve **Tamsayı**.
    - **Kaydırıcı** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Para birimi**, **Ondalık** ve **Tamsayı**.
    - **Çubuklarla birlikte kaydırıcı** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Para birimi**, **Ondalık** ve **Tamsayı**.

- **Eşik değeri** – Bu ayar görüntüleme denetim türü olarak **Aralık** seçmeniz durumunda gereklidir. Sınırlayıcı olarak noktalı virgül (;) kullanarak değerleri tanımlayabilirsiniz.

    Örneğin, **Tamsayı** öznitelik türüne sahip **Çanta Hacmi** özniteliği için eşik değeri **10; 20; 50; 100; 200; 500; 1000; 5000** olabilir. Bu durumda, POS şu aralıkları gösterir. Sonuç kümesinde ürün bulunmayan aralıklar karartılmış olarak görünür.

    - 10'den daha az
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 veya üzeri

Özniteliklerin filtre ayarları yalnızca ürün özniteliklerine uygulanabilir ve ürün arama ve kategori tarama sonuçlarını iyileştirmek için kullanılabilir. Müşteri veya sipariş bilgilerini zenginleştirmek için aynı öznitelikler kullanılabilmesine karşın müşteri arama veya sipariş arama için geçerli değildir.

Varsayılan Commerce modüllerinde, **Aralık**, **Kaydırıcı** ve **Çubuklarla kaydırıcı** gibi **Görüntüleme denetimi** filtre ayarları için kullanıma hazır destek yoktur. **Aralık** ve **Kaydırıcı** ayarları POS çözümleri için desteklenmeye devam eder ancak **Çubuklarla kaydırıcı** ayarı eski SharePoint çevrimiçi mağazaları için geçerlidir ve üçüncü taraf tümleştirme ve özel senaryolar için kullanılabilir.

Daraltılabilir özniteliklerin **Sabit liste** seçeneği etkinleştirilmiş **Metin** türünde bir özniteliği olmasını ve listeyi yönetilebilir durumda (100-200 benzersiz değere kadar) tutmanızı öneririz. İyileştirici 1.000 veya daha fazla benzersiz değer içerirse **Sabit liste** seçeneğinin devre dışı bırakıldığı **Metin** türünde bir öznitelik kullanmak daha uygun olur.

Çeviriler, öznitelik adları ve değerleri için önemlidir. **Sabit liste** seçeneğinin etkinleştirildiği **Metin** türündeki öznitelikler için **Öznitelik türü** altındaki öznitelik değerleri için çeviriler tanımlayabilirsiniz. Diğer tüm öznitelik türleri için, öznitelik değerlerini tanımladığınız sayfada çeviriler tanımlayabilirsiniz. Örneğin, **Metin** türünde bir öznitelik için özniteliğin **Öznitelikler** sayfasında varsayılan değer için çeviriler tanımlayabilirsiniz. Ancak, varsayılan değeri ürün düzeyinde geçersiz kılarsınız, ürünün **Ürün öznitelikleri** sayfasında öznitelik için çeviriler tanımlayabilirsiniz.

Bir öznitelik bir kanal için iyileştirilebilir olarak işaretlendikten sonra öznitelik türünü güncelleştirmemeniz gerekir. Aksi durumda, ürün verilerinin arama dizinine yayımlanmasını etkilersiniz. Bunun yerine, yeni bir iyileştirici türü için yeni bir öznitelik oluşturmanızı ve diğer öznitelik gruplarından kaldırarak önceki özniteliği devre dışı bırakmanızı öneririz.

Özniteliklere göre arama desteklenir ancak yalnızca arama sözcüklerinin tam eşleşmeleri için sonuçları getirir. Örneğin, **Kumaş** özniteliğini **Kaşmir pamuk** değerine sahip olsun. Müşteri "Kaş" için arama yaptığında kumaş olarak **Kaşmir pamuk** değerine sahip olan ürünler getirilmez. Ancak, Müşteri "Kaşmir", "Pamuk" veya "Kaşmir Pamuk" için arama yaptığında kumaş olarak **Kaşmir pamuk** değerine sahip olan ürünler getirilir.

### <a name="additional-attribute-metadata-options"></a>Ek öznitelik meta veri seçenekleri

> [!NOTE]
> Bu öznitelik meta veri seçenekleri yalnızca eski SharePoint çevrimiçi mağaza ve harici tümleştirmeler için geçerlidir. Bu öznitelik meta veri seçenekleri hakkında daha fazla bilgi için bkz. [SharePoint Server 2013'te arama şemasına genel bakış](/SharePoint/search/search-schema-overview).

Aşağıdaki ek öznitelik meta veri seçenekleri **Öznitelikler** sayfasında da bulunur:

- Aranabilir
- Alınabilir
- Sorgulanabilir
- Sıralanabilir
- Büyük-küçük harfi ve biçimi yok say
- Tam eşleşme

Bu seçeneklerin temel amacı çevrimiçi eski SharePoint tabanlı çevrimiçi mağazalar için arama işlevini geliştirmektir. Commerce e-ticaret web sitelerinde veya POS terminallerinde uygulanmaları gerekmez. Gözetimsiz tümleştirme desteklenmeye devam ettiğinden, bu seçenekler Commerce yazılım geliştirme seti (SDK) kullanılarak öznitelik meta verilerini dışa aktarmak için kullanılabilir. Ürünleri özel, iyileştirilmiş bir harici arama dizinine yerleştirmek için Commerce SDK'yı kullanabilirsiniz. Bu şekilde, yalnızca dizine eklenmesi gereken özniteliklerin dizine eklendiğinden emin olabilirsiniz.

## <a name="attribute-groups"></a>Öznitelik grupları

Bir *öznitelik grubu* bir ürün yapılandırma modelindeki bir bileşen veya alt bileşen için ayrı öznitelikleri gruplandırmak için kullanılır. Bir öznitelik birden fazla öznitelik grubuna dahil edilebilir. Çeşitli seçenekler belirli bir bağlam içinde düzenlenmiş olduğundan öznitelik grupları kullanıcıların ürünleri yapılandırmasına yardımcı olur. Öznitelik grupları kategorilere veya kanallara atanabilir. Bir öznitelik grubundaki öznitelikler için de varsayılan değerler ayarlayabilirsiniz.

![Öznitelik grupları sayfası.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Öznitelik grubu oluşturma

Öznitelik grubu oluşturmak için bu örnek yordamdaki adımları izleyin.

1. Commerce headquarters'ta alım satım yöneticisi olarak oturum açın.
1. **Ürün bilgi yönetimi \> Kurulum \> Kategoriler ve öznitelikler \> Öznitelik grupları**'na gidin.
1. **Frak Gömlekleri** adında bir öznitelik grubu oluşturun.
1. Aşağıdaki öznitelikleri ekleyin: **TemizlemeYöntemi**, **YakaTipi**, **Koleksiyon** ve **Tasarım**.

> [!NOTE]
> Öznitelik grubundaki özniteliklerin görüntüleme sırası değerleri, arama ve kategori tarama sonuçlarındaki iyileştiricilerin sırasını etkilemez veya bu sıraya uygulanmaz. Bunlar yalnızca "sipariş öznitelikleri" senaryosu için geçerlidir.

### <a name="assign-attribute-groups-to-categories"></a>Öznitelik gruplarını kategorilere atama

Aşağıdaki kategori hiyerarşileri türlerinde, bir veya daha fazla öznitelik grubu kategori düğümleriyle ilişkilendirilebilir:

- Ticaret ürün hiyerarşisi
- Kanal gezintisi kategori hiyerarşisi
- Tamamlayıcı ürün kategori hiyerarşisi

Ürünler öznitelik gruplarıyla ilişkili kategorilerde kategorilere ayrıldıklarında, bu öznitelik gruplarının içerdiği öznitelikleri devralırlar.

![Commerce ürün hiyerarşisi sayfasındaki ürün öznitelik grupları hızlı sekmesi.](media/AGRetailProdHierarchy_2022Series.png)

Commerce ürün hiyerarşisinde kategorilere öznitelik grupları atamak için bu örnek yordamdaki adımları izleyin.

1. Commerce headquarters'ta alım satım yöneticisi olarak oturum açın.
1. **Retail ve Commerce \> Ürünler ve kategoriler \> Commerce ürün hiyerarşisi**'ne gidin.
1. **Moda** gezinti hiyerarşisini seçin.
1. **Erkek giyim** altından **Pantolonlar** kategorisini seçin ve daha sonra **Ürün öznitelik grupları** hızlı sekmesinde **Erkek kemeri** adında bir öznitelik grubu ekleyin.
1. **Moda güneş gözlükleri** kategorisini seçin ve **Öznitelikleri görüntüle**'yi seçerek **Moda Güneş Gözlükleri** öznitelik grubundaki yeni öznitelikleri doğrulayın. Yeni öznitelik grubu yeni **Mercek şekli** ve **Güneş gözlüğü markası** özniteliklerini göstermelidir.
1. **Pantolonlar** kategorisini seçin ve **Öznitelikleri görüntüle**'yi seçerek **Erkek kemeri** öznitelik grubu için öznitelikleri doğrulayın. Öznitelik grubu **Erkek kemer markası**, **Kemer kumaşı** ve **Kemer boyu** özniteliklerini içermelidir.

Aynı temel yordam Kanal gezinti kategori hiyerarşisi ve tamamlayıcı ürün kategori hiyerarşisinde kategorilere öznitelik grupları atamak için de kullanılabilir. Ancak, adım 2'de, öznitelik grupları atamak istediğiniz hiyerarşiye bağlı olarak aşağıdaki yollardan birini kullanın:

- **Kanal gezinti kategori hiyerarşisi:** **Retail ve Commerce \> Kategori ve ürün yönetimi \> Kanal gezinti kategorileri**'ne gidin.
- **Tamamlayıcı ürün kategori hiyerarşisi:** **Retail ve Commerce \> Kategori ve ürün yönetimi \> Tamamlayıcı ürün kategorileri**'ne gidin.

> [!NOTE]
> Öznitelikk gruplarını **Kategori öznitelik değerleri** hızlı sekmesinde değil yalnızca **Ürün öznitelik grupları** hızlı sekmesinde öznitelik gruplarıyla ilişkilendirdiğinizden emin olun. **Kategori öznitelik değerleri** hızlı semesinde öznitelikler görüntülenirse Eylem Bölmesinde **Kategori hiyerarşisini düzenle**'yi seçin. Ardından **Kategori öznitelik grupları** hızlı sekmesinde kategori düğümlerini ve **Kaldır**'ı seçin. Commerce Scale Unit aracılığıyla öznitelikleri kategoriye göre getirme desteği yoktur.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Varsayılan ürün koleksiyonuna yönelik Commerce kanalları için görüntülenebilir ve iyileştirilebilir özniteliklerini tanımlayın

Çeşitli öznitelik gruplarını çeşitli hiyerarşilerde (Commerce ürün hiyerarşisi veya kanal gezinti kategorileri) kategoriler ile ilişkilendirdikten ve her bir ürün için öznitelik değerlerini tanımladıktan sonra kategori ilişkilendirmesine göre, bu özniteliklerin belirli bir kanalda görünebilmesini sağlamak için **Özniteliği Kanalda göster** bayrağını etkinleştirmeniz gerekir.

1. **Retail and Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.
1. **Öznitelik meta verilerini ayarla**'yı seçin ve ardından sol gezinti bölmesinden bir öznitelik seçin.
1. **Kanalın ürün öznitelikleri** hızlı sekmesinde (**Kategori öznitelikleri** hızlı sekmesinde değil), özniteliğin görüntülenebilir olması için **Özniteliği kanalda göster** seçeneğini **Evet** olarak ayarlayın.
1. Özniteliğin de iyileştirilebilir olmasını istiyorsanız **İyileştirilebilir** seçeneğini **Evet** olarak ayarlayın.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Boyut, stil ve renk gibi boyuta dayalı iyileştiricilerin denetim görünürlüğü

Boyut, stil ve renk gibi ürün boyutları en sık kullanılan iyileştiricilerdir. Bu ürün boyutlarının iyileştiriciler olarak kullanılabilmesini sağlamak için ürün boyut değerlerinden değerleri otomatik olarak devralan bir öznitelik türüne başvuru içeren bir bir öznitelik grubunu kanal düzeyinde ilişkilendirmeniz gerekir.

**Kanal kategorileri ve ürün öznitelikleri** sayfasındaki bayrakları güncelleştirerek ürün boyutlarının görüntülenebilir ve iyileştirilebilir olduğunu belirtebilirsiniz. Gezinti bölmesinde kök düğümü seçin ve sonra **Kanal ürün öznitelikleri** hızlı sekmesinde **Boyut**, **Stil** ve **Renk** öznitelikleri için **Kanlada özniteliği göster** seçeneğini **Evet** olarak ayarlayın. Bu özniteliklerin de de iyileştirilebilir olmasını istiyorsanız her biri için **İyileştirilebilir** seçeneğini **Evet** olarak ayarlayın.

![Boyut iyileştiriciler için öznitelik meta verilerini ayarlama.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Öznitelikleri, demo-veri tabanlı Houston kanalında kullanılabilir olacak şekilde etkinleştirmek için bu örnek yordamdaki adımları izleyin.

1. **Retail and Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.
1. **Houston** kanalını seçin.
1. Eylem Bölmesinde **Öznitelik meta verisi ayarla**'yı seçin.
1. **Moda** kategori düğümünü ve ardından **Kanal ürün öznitelikleri** hızlı sekmesinde her öznitelik için **Özniteliği ekle**'yi seçin.
1. **Moda Aksesuarlar** kategori düğümünü, **Moda Güneş Gözlükleri** kategorisini ve ardından **Kanal ürün öznitelikleri** hızlı sekmesinde her öznitelik için **Özniteliği ekle**'yi seçin.
1. **Erkek giyim** kategori düğümünü, **Pantolonlar** kategorisini ve ardından **Kanal ürün öznitelikleri** hızlı sekmesinde her öznitelik için **Özniteliği ekle**'yi seçin.
1. Hedeflenen öznitelikler ve iyileştiricileriniz için öznitelik meta verilerini güncelleştirdikten sonra değişikliklerinizi kaydedip **Kanal güncelleştirmelerini yayımla** işini çalıştırdığınızdan emin olun. Ardından, güncelleştirmeler yayımlandıktan sonra şu işleri çalıştırmanız gerekir: **1070** (**Kanal yapılandırması**), **1040** (**Ürünler**) ve **1150** (**Katalog**).

> [!NOTE]
> - İşletmeniz, gezinti hiyerarşisine sık olarak ürün eklemenizi veya kaldırmanızı gerektiriyorsa veya görüntüleme sırası değerlerini güncelleştirme, yeni kategori ekleme ve kategorilere yeni öznitelik grupları ekleme gibi değişiklikler yaparsanız **Kanal güncelleştirmelerini yayımla** işini sık kullanılan bir toplu iş olarak yapılandırmanızı öneririz. Alternatif olarak, **Kanal güncelleştirmelerini yayımla** işini ve şu Commerce Data Exchange (CDX) işlerini el ile tetikleyebilirsiniz: **1070** (**Kanal yapılandırması**), **1040** (**Ürünler**) ve **1150** (**Katalog**).
> - Bir **Devral** seçeneği bu kanalın öznitelik gruplarını hiyerarşideki üst kanalından alması gerektiğini belirtmenize olanak tanır. **Devral** seçeneğini **Evet** olarak ayarlarsanız, alt kanal düğümü tüm öznitelik gruplarını ve bu öznitelik gruplarındaki tüm öznitelikleri devralır.
> - Eylem bölmesindeki **Öznitelik meta verilerini ayarla** düğmesi kullanılamıyorsa **Gezinti hiyerarşisinin** **Genel** hızlı sekmesindeki kanalla ilişkilendirilmiş olduğundan emin olun.
> - Boyut tabanlı öznitelik grupları dışındaki herhangi bir öznitelik grubunu kanal düzeyinde ilişkilendirmemeniz gerekir (örneğin, **Kanal kategorileri ve ürün öznitelikleri** sayfasındaki **Öznitelik grupları**).
> - Commerce 10.0.27 sürümünde müşteriye özel işletmeler arası (B2B) kataloglarının desteklenmeye başlaması sonrasında, her B2B kataloğu için iyileştirici ve öznitelik ayarlarını bu makalede açıklananla aynı şekilde tanımlamanız beklenmektedir.

## <a name="override-attribute-values"></a>Öznitelik değerlerini geçersiz kılma

Özniteliklerinin varsayılan değerleri ayrı ürünler için ürün düzeyinde geçersiz kılınabilir. Varsayılan değerler belirli kanallarda hedeflenen belirli kataloglardaki ayrı ürünler için de geçersiz kılınabilir.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Tek bir ürününü öznitelik değerlerini geçersiz kılma

Tek bir ürünün öznitelik değerlerini geçersiz kılmak için bu örnek yordamdaki adımları izleyin.

1. Commerce headquarters'ta alım satım yöneticisi olarak oturum açın.
1. **Retail ve Commerce \> Kategori ve ürün yönetimi \> Kategoriye göre serbest bırakılan ürünler**'e gidin.
1. **Moda \> Moda Aksesuarlar \> Moda Güneş Gözlükleri**'ni seçin.
1. Izgaradan gerekli ürünü seçin. Ardından Eylem Bölmesinde, **Ürün** sekmesindeki **Ayar** gurubunda **Ürün öznitelikleri**'ni seçin.
1. Sol bölmeden bir öznitelik seçin ve ardından sağ bölmede değerini güncelleştirin.

![Ürün öznitelik değerleri sayfası.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Katalogdaki tüm ürünlerin öznitelik değerlerini geçersiz kılma

Katalogdaki tüm ürünlerin öznitelik değerlerini geçersiz kılmak için bu örnek yordamdaki adımları izleyin.

1. Commerce headquarters'ta alım satım yöneticisi olarak oturum açın.
1. **Retail ve Commerce \> Katalog yönetimi \> Tüm kataloglar**'a gidin.
1. **Fabrikam Temel Kataloğu** kataloğunu seçin.
1. **Moda \> Moda Aksesuarlar \> Moda Güneş Gözlükleri**'ni seçin.
1. **Ürünler** hızlı sekmesinde gerekli ürünü seçin ve ardından ızgaranın üstünden **Öznitelikler**'i seçin.
1. Aşağıdaki hızlı sekmelerde gereken özniteliklerin değerlerini güncelleştirin:

    - Paylaşılan ürün ortamı
    - Paylaşılan ürün öznitelikleri
    - Kanal ortamı
    - Kanal ürünü öznitelikleri

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Kanaldaki tüm ürünlerin öznitelik değerlerini geçersiz kılma

Kanaldaki tüm ürünlerin öznitelik değerlerini geçersiz kılmak için bu örnek yordamdaki adımları izleyin.

1. Commerce headquarters'ta alım satım yöneticisi olarak oturum açın.
1. **Retail and Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.
1. **Houston** kanalını seçin.
1. **Ürünler** hızlı sekmesinde gerekli ürünü seçin ve ardından ızgaranın üstünden **Öznitelikler**'i seçin.
1. Kullanılabilir ürün yoksa **Ürünler** hızlı sekmesinde **Ekle**'yi ve daha sonra **Ürün ekle** iletişim kutusunda gerekli ürünleri seçin.
1. Aşağıdaki hızlı sekmelerde gereken özniteliklerin değerlerini güncelleştirin:

    - Paylaşılan ürün ortamı
    - Paylaşılan ürün öznitelikleri
    - Kanal ortamı
    - Kanal ürünü öznitelikleri

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Varyanta özel öznitelik değerleri tanımlama ve ürün öznitelikleri için birden çok değer tanımlama

Varyanta özgü öznitelik değerleri tanımlamak ve ürün öznitelikleri için birden çok değer tanımlamak üzere bu örnek yordamdaki adımları izleyin.

1. Commerce headquarters'ta alım satım yöneticisi olarak oturum açın.
1. **Retail and Commerce \> Kanal Kurulumu \> Kanal kategorileri ve ürün öznitelikleri**'ne gidin.
1. **Houston** kanalını seçin.
1. **Ürünler** hızlı sekmesinde gerekli ürün varyantını seçin ve ardından ızgaranın üstünden **Öznitelikler**'i seçin.
1. Kullanılabilir ürün yoksa **Ürünler** hızlı sekmesinde **Ekle**'yi ve daha sonra **Ürün ekle** iletişim kutusunda gerekli ürün varyantlarını seçin.
1. Aşağıdaki hızlı sekmelerde gereken özniteliklerin değerlerini güncelleştirin:

    - Paylaşılan ürün ortamı
    - Paylaşılan ürün öznitelikleri
    - Kanal ortamı
    - Kanal ürünü öznitelikleri

#### <a name="example-of-variant-specific-attribute-configuration"></a>Varyanta özgü öznitelik yapılandırması örneği
        
Bu örnekte **P001-Master** ürünü üç varyantı bulunan bir çoklu etkinlik ayakkabısıdır: **Koşu**, **Yürüşüş** ve **Doğa yürüyüşü**. Her varyant için **Etkinlik** özniteliğinin değerini benzersiz olarak tanımlamak istiyorsunuz. Kanalınızın **Kanal kategorileri ve ürün özellikleri sayfasının** **Ürünler** hızlı sekmesinde aşağıdaki tabloda gösterildiği şekilde varyantlar için **Etkinlik** öznitelik değerini tanımlarsınız.

| Varyant     | Etkinlik öznitelik değeri |
|-------------|--------------------------|
| P001-Master | Spor                   |
| P001-1      | Koşu                  |
| P001-2      | Yürüyüş                  |
| P001-3      | Doğa yürüyüşü                 |

Bir kullanıcı "ayakkabı" araması yaparsa **P001-Master** ürünü arama sonuçlarında görünür. **Etkinlik** özniteliğini iyileştirilebilir olarak yapılandırdıysanız **Etkinlik** iyileştiricisi **Spor**'u iyileştirilebilir bir değer olarak listeler çünkü bu değer **P001-Master** ürün düzeyinde **Etkinlik** özniteiği için tanımlanmıştır.

Varsayılan olarak, varyant düzeyindeki özniteliklerin yalnızca ürün ayrıntıları sayfalarında (PDP'ler) kullanılması amaçlanmıştır. PDP'de belirli bir ürün çeşidi seçtiğinizde, PDP'deki ürün özellikleri bu özel varyant için güncelleştirilir.

İyileştiricilerin, ürün varyantı düzeyinde tanımlanan öznitelik değerlerini alması için ürün ana düzeyinde bir öznitelik tanımlamanız, **Çoklu değerlere izin ver** onay kutusunu seçmeniz ve öznitelik türünü **Metin** olarak ayarlamanız gerekir.

Daha sonra, ürün varyantlarınız için olası tüm değerleri belirlemeniz gerekir. Bu örnekte kullanılan **Etkinlik** özniteliği için olası değerler arasında şunlar bulunabilir: **Koşu**, **Yürüyüş**, **Hiking**, **Doğa yürüyüşü**, **Kampçılık**, **Su sporları** ve **Kar sporları**.

Varyant öznitelik değerlerinin ne olacağını belirledikten sonra bunları dikey çizgi ile ayrılmış değerler kullanarak ürün ana düzeyinde tanımlayabilirsiniz. **Etkinlik** özniteliği için ana üründe öznitelik değerini **Koşu|Yürüyüş|Hiking|Doğa yürüyüşü|Kampçılık|Su sporları|Kar sporları** olarak tanımlayabilirsiniz.

Daha sonra, her varyant için, dik çizgiyle ayrılmış değerler veya tek değerler girerek öznitelik değerleri tanımlayabilirsiniz. **Etkinlik** özniteliği için **Koşu|Yürüyüş|Hiking**, **Koşu**, **Koşu|Hiking|Su sporları** ve benzeri şekilde bireysel bir ürün varyantı yapılandırabilirsiniz.

Varyant öznitelik değerlerini tanımladıktan sonra **Kanal kategorileri ve ürün öznitelikleri** sayfasında, Eylem Bölmesinde **Kanal güncelleştirmelerini yayımla**'yı seçin ve **1150**, **1040**, ve **1070** işlerini çalıştırın.

İşler tamamlandıktan ve arama dizini güncelleştirildikten sonra, beklenen tüm değerlerin arama sonuçlarında ve kategori tarama sonuçlarında görünmesi gerekir.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
