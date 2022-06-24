---
title: Öznitelikler ve öznitelik gruplarını yönetme
description: Bu makale, bir ürünü veya özelliklerini kullanıcı tanımlı alanlar aracılığıyla açıklamak için özniteliklerin nasıl kullanılacağını açıklar.
author: ashishmsft
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryAttribute, EcoResProductEntityAttributeTableFieldAssociation, EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResAttributeType, EcoResAttributeValue, EcoResCategoryAttributeGroup, EcoResCategoryFriendlyName
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: cd74cb7795366bdca80e47d79a9591af69a16daf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876676"
---
# <a name="manage-attributes-and-attribute-groups"></a>Öznitelikler ve öznitelik gruplarını yönetme

[!include [banner](includes/banner.md)]

*Öznitelikler* kullanıcı tanımlı alanlar aracılığıyla bir ürünü ve özelliklerini daha fazla açıklamak için bir yol sağlar (**Bellek boyutu**, **Sabit disk kapasitesi**, **Energy star uyumluluğu**, vb.). Öznitelikler ürün kategorileri ve kanalları gibi çeşitli Commerce varlıkları ile ilişkili olabilir ve bunlar için varsayılan değerler ayarlanabilir. Ürün kategorileri veya kanalları ile ilişkili olduğunda ürünler özniteliklerini ve varsayılan değerleri devralır. Varsayılan değerler tek tek ürün düzeyinde, kanal düzeyinde veya katalog düzeyinde geçersiz kılınabilir.


Örneğin, tipik bir televizyon ürünü aşağıdaki özniteliklere sahip olabilir.

| Kategori   | Öznitelik                | İzin verilen değerler          | Varsayılan değer |
|------------|--------------------------|-----------------------------|---------------|
| TV ve Video | Marka                    | Herhangi bir geçerli marka değeri       | Hiçbiri          |
| TV         | Ekran Boyutu              | 20–80 inç                | Hiçbiri          |
|            | Dikey Çözünürlük      | 480i, 720p, 1080i veya 1080p | 1080p         |
|            | Ekran yenileme hızı      | 60hz, 120hz veya 240hz       | 60hz          |
|            | HDMI Girdileri              | 0–10                        | 3             |
|            | DVI Girdileri               | 0–10                        | 1             |
|            | Bileşik Girdiler         | 0–10                        | 2             |
|            | Bileşen Girdileri         | 0–10                        | 1             |
| LCD        | 3D Hazır                 | Evet veya Hayır                   | Evet           |
|            | 3D etkin               | Evet veya Hayır                   | Hayır            |
| Plazma     | Çalıştırma Sıcaklığı Başlangıç      | 32–110 derece              | 32            |
|            | Çalıştırma Sıcaklığı Son        | 32–110 derece              | 100           |
| Projeksiyon | Projeksiyon tüp garanti | 6, 12 veya 18 ay         | 12            |
|            | \# Projeksiyon Tüplerinin sayısı   | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Öznitelikler ve öznitelik türleri

Öznitelikler *öznitelik türlerini* temel alır. Öznitelik türü, belirli bir öznitelik için girilebilen veri türünü tanımlar. Aşağıdaki öznitelik türleri desteklenir:

- **Para birimi** – Bu tür bir para birimi değerini destekler. Bağlı olabilir (diğer bir deyişle, bir değer aralığı destekleyebilir) veya açık bırakılabilir.
- **DateTime** – Bu tür, tarih ve saat değerini destekler. Bağlı veya açık bırakılmış olabilir.
- **Ondalık** – Bu tür, ondalık basamak içeren sayısal değeri destekler. Ayrıca, ölçü birimini de destekler. Bağlı veya açık bırakılmış olabilir.
- **Tamsayı** – Bu tür sayısal bir değeri destekler. Ayrıca, ölçü birimini de destekler. Bağlı veya açık bırakılmış olabilir.
- **Metin** – Bu tür metin değerini destekler. Ayrıca önceden tanımlanmış bir dizi olası değerleri de (*numaralandırma*) destekler.
- **Boole** – Bu tür ikili değeri destekler (**doğru** veya **yanlış**).
- **Referans** – Bu tür diğer özniteliklere referansta bulunur.

### <a name="set-up-attribute-types"></a>Öznitelik türlerini ayarla

1. Alım satım yöneticisi olarak arka ofis istemcisinde oturum açın.
2. **Ürün bilgi yönetimi** &gt; **Kurulum** &gt; **Kategoriler ve öznitelikler** &gt; **Öznitelik türleri**'ne gidin.
3. **Metin** türünde iki öznitelik türü oluşturun, **Sabit liste** seçeneğini **Evet** olarak ayarlayın ve sonra değerler listesi ekleyin:

    - Bir öznitelik türüne **Mercek şekli** adını verin ve şu değerleri ekleyin: **Oval**, **Kare** ve **Dikdörtgen**.
    - Diğer öznitelik türüne **Güneç gözlüğü markası** adını verin ve şu değerleri ekleyin: **Ray ban**, **Aviator** ve **Oakley**.

![Öznitelik türleri.](media/AttributeType.png)

### <a name="set-up-an-attribute"></a>Öznitelik ayarlama

1. Alım satım yöneticisi olarak arka ofis istemcisinde oturum açın.
2. **Ürün bilgi yönetimi** &gt; **Kurulum** &gt; **Kategoriler ve öznitelikler** &gt; **Öznitelikler**'e gidin.
3. **Mercek** adında bir öznitelik oluşturun.
4. **Öznitelik türü** alanını **Mercek şekli** olarak ayarlayın.

![Öznitelikler.](media/Attribute.png)

## <a name="attribute-metadata"></a>Öznitelik meta verileri

*Öznitelik meta verisi* her ürün için özniteliklerin nasıl davranacağını belirtebileceğiniz seçenekler belirlemenize olanak tanır. Örneğin, özniteliklerin gerekli olup olmadığını, aramalar için kullanılıp kullanılamayacağını ve filtre olarak kullanılıp kullanılamayacağını belirtebilirsiniz.

Ürünler için, öznitelik meta verileri kanal düzeyinde geçersiz kılınabilir. Bu özellik bu makalenin ilerleyen bölümlerinde açıklanmıştır.

Sizin de göreceğiniz gibi **Öznitelikler** sayfası öznitelik meta verileriyle ilgili seçenekler içerir. **POS için öznitelik değerleri** altında, **İyileştirilebilir** adına sahip bir seçenek satış noktasındaki (POS) öznitelik değerlerinin davranışını veya sistemin bu öznitelik değerlerini ele alma şeklini etkiler. Yalnızca, **İyileştirilebilir** seçeneğini **Evet** olarak ayarlayabileceğiniz öznitelikler POS'taki ürünleri iyileştirilmesi veya filtrelenmesi için gösterir.

**Öznitelikler** sayfasındaki diğer öznitelik meta veri seçenekleri şunlardır:

- Aranabilir
- Alınabilir
- Sorgulanabilir
- Sıralanabilir
- Birden fazla değere izin ver
- Büyük-küçük harfi ve biçimi yok say
- Tam eşleşme

Bu seçeneklerin temel amacı çevrimiçi mağaza için arama işlevini geliştirmektir. Kullanıma hazır olarak çevrimiçi mağaza içermese de e-Ticaret Yayımlama Yazılım Geliştirme Seti (SDK) içerir. Müşteriler bu SDK'yı kullanarak ürünleri istedikleri arama dizinine koyabilir. Ürün verileri içe aktarılsa da müşteriler aranabilir verileri, sorgulanabilecek verileri, vb. birbirinden ayırabilir. Bu şekilde, yalnızca *kendi görüşlerine göre* dizinlenmesi gereken öznitelikleri dizinlediklerinden emin olmak için optimum dizini oluşturabilir.

Bu kalan seçeneklerin amacı hakkında bilgi için bkz. [SharePoint Server 2013'te arama şemasına genel bakış](/SharePoint/search/search-schema-overview).

## <a name="filter-settings-for-attributes"></a>Öznitelik filtre ayarları

Özniteliklerin filtre ayarları özniteliklerle ilgili filtrelerin POS'ta nasıl görüneceğini tanımlamanıza olanak tanır. Bir özniteliğe ilişkin filtre ayarlarına erişmek **Öznitelikler** sayfasında özniteliği seçin ve Eylem Bölmesine **Filtre ayarları**'nı seçin.

**Filtre görüntüleme tercihleri** sayfası, aşağıdaki alanları içerir:

- **Ad** – Varsayılan olarak, bu alanın öznitelik adına ayarlanır. Ancak, değerde değişiklik yapabilirsiniz.
- **Görüntüleme seçeneği** – Aşağıdaki seçenekler mevcuttur:

    - **Tek bir değer** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Boole**, **Para birimi**, **Ondalık**, **Tamsayı** ve **Metin**. Bu seçenek istemcide iyileştirme için bu özniteliklere yönelik tek bir değer seçimi sağlar.
    - **Birden fazla değer** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Boole**, **Ondalık**, **Tamsayı** ve **Metin**. Bu seçenek istemcide iyileştirme için bu özniteliğe yönelik tek birden fazla değer seçimi sağlar.

- **Görüntüleme denetimi** – Aşağıdaki seçenekler mevcuttur:

    - **Liste** – Bu seçenek tüm öznitelik türleri için kullanılabilir.
    - **Aralık** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Para birimi**, **Ondalık** ve **Tamsayı**.
    - **Kaydırıcı** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Para birimi**, **Ondalık** ve **Tamsayı**.
    - **Çubuklarla birlikte kaydırıcı** – Bu seçenek aşağıdaki öznitelik türleri için kullanılabilir: **Para birimi**, **Ondalık** ve **Tamsayı**.

- **Eşik değeri** – Bu ayar görüntüleme denetim türü olarak **Aralık** seçmeniz durumunda gereklidir. Sınırlayıcı olarak noktalı virgül (;) kullanarak değerleri tanımlayabilirsiniz.

    Örneğin, **Torba Hacmi** gibi bir filtre için eşik değeri **10; 20; 50; 100; 200; 500; 1000; 5000** olabilir. Bu durumda, POS şu aralıkları gösterir. Sonuç kümesinde ürün bulunmayan aralıklar karartılmış olarak görünür.

    - 10'den daha az
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 veya üzeri

![Öznitelik filtresi ayarları.](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Öznitelik grupları

Öznitelikler tanımladıktan sonra öznitelik gruplarına atanabilir. Bir *öznitelik grubu* bir ürün yapılandırma modelindeki bir bileşen veya alt bileşen için ayrı öznitelikleri gruplandırmak için kullanılır. Bir öznitelik birden fazla öznitelik grubuna dahil edilebilir. Çeşitli seçenekler belirli bir bağlam içinde düzenlenmiş olduğundan öznitelik grupları kullanıcıların ürünleri yapılandırmasına yardımcı olur. Öznitelik grupları kategorilere veya kanallara atanabilir.

Bir öznitelik grubuna dahil olan öznitelikler için de varsayılan değerler ayarlayabilirsiniz. Örneğin, bir öznitelik grubuna renk için öznitelik ekleyebilir ve varsayılan öznitelik değeri olarak **Mavi** seçebilirsiniz. Bu durumda, öznitelik grubu, özniteliklerinden biri olarak renk içeren bir ürüne eklendiğinde **Mavi** bu ürün için varsayılan renk olarak görünür.

![Öznitelik grupları.](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Öznitelik grubu oluşturma

1. Alım satım yöneticisi olarak arka ofis istemcisinde oturum açın.
2. **Ürün bilgi yönetimi** &gt; **Kurulum** &gt; **Kategoriler ve öznitelikler** &gt; **Öznitelik grupları**'na gidin.
3. **Moda Güneş Gözlükleri** adında bir öznitelik grubu oluşturun.
4. Şu öznitelikleri ekleyin: **Mercek şekli** ve **Güneş gözlüğü markası**.

### <a name="assign-attribute-groups-to-categories"></a>Öznitelik gruplarını kategorilere atama

Bir veya daha fazla öznitelik grubu, şu türdeki perakende kategorisi hiyerarşilerinde kategori düğümleri ile ilişkilendirilebilir: Commerce ürün hiyerarşisi, Kanal gezinti kategori hiyerarşisi ve Ek ürün kategori hiyerarşisi. Ürünler kategorize edildiğinde, öznitelik gruplarına dahil edilen öznitelikleri devralır.

![Ürün hiyerarşisi – Ürün öznitelik grupları.](media/AGRetailProdHierarchy.PNG)

Commerce ürün hiyerarşisinde kategorilere öznitelik grupları atamak için şu adımları izleyin.

1. Alım satım yöneticisi olarak arka ofis istemcisinde oturum açın.
2. **Retail ve Commerce** &gt; **Kategori ve ürün yönetimi** &gt; **Commerce ürün hiyerarşisi**'ne gidin.
3. **Moda gezinti hiyerarşi**'ni seçin.
4. **Erkek giyim** altından **Pantolonlar** kategorisini seçin ve daha sonra **Ürün öznitelik grupları** hızlı sekmesinde **Erkek kemeri** adında bir öznitelik grubu ekleyin.
5. **Moda güneş gözlükleri** kategorisini seçin ve **Öznitelikleri görüntüle**'yi seçerek **Moda Güneş Gözlükleri** öznitelik grubundaki yeni öznitelikleri doğrulayın.

    Yeni öznitelik grubu yeni **Mercek şekli** ve **Güneş gözlüğü markası** özniteliklerini göstermelidir.

6. **Erkek giyim** altından **Pantolonlar** kategorisini seçin ve **Öznitelikleri görüntüle**'yi seçerek **Erkek kemeri** öznitelik grubu için öznitelikleri doğrulayın.

    Öznitelik grubu **Erkek kemer markası**, **Kemer kumaşı** ve **Kemer boyu** özniteliklerini içermelidir.

> [!NOTE]
> Bu yordam Kanal gezinti kategori hiyerarşisi ve Ek ürün kategori hiyerarşisinde kategorilere öznitelik grupları atamak için de kullanılabilir. Adım 2'de, aşağıdaki gezinti yollarını kullanın:
>
> - Retail ve Commerce &gt; Kategori ve ürün yönetimi &gt; Kanal gezinti kategorileri
> - Retail ve Commerce &gt; Kategori ve ürün yönetimi &gt; Ek ürün kategorileri.

### <a name="assign-attribute-groups-to-stores"></a>Öznitelik gruplarını mağazalarına atama

Bir veya daha fazla öznitelik grubu mağaza hiyerarşisindeki bir veya daha fazla mağaza ile ilişkilendirilebilir. Daha sonra, ürünler belirli mağazalar için zenginleştirildiğinde, öznitelik gruplarına dahil edilen öznitelikleri devralır.

1. Alım satım yöneticisi olarak arka ofis istemcisinde oturum açın.
2. **Retail ve Commerce** &gt; **Kanal kurulumu** &gt; **Kanal kategorileri ve ürün öznitelikleri**.
3. Houston kanalına öznitelik grupları atayın:

    1. **Houston** kanalını seçin.
    2. **Öznitelik grubu** hızlı sekmesinde, **Ekle**'yi ve **Ad** alanında **SharePointProvisionedProductAttributeGroup** öğesini seçin.
    3. Yeniden **Ekle**'yi seçin ve **Ad** alanında **Erkek kemeri**'ni seçin.
    4. Yeniden **Ekle**'yi seçin ve **Ad** alanında **Moda Güneç Gözlükleri**'ni seçin.

        > [!NOTE]
        > Bir seçenek bu kanalın öznitelik gruplarını hiyerarşideki üst kanalından alması gerektiğini belirtmenize olanak tanır. **Devral** seçeneğini **Evet** olarak ayarlarsanız, alt kanal düğümü tüm öznitelik gruplarını ve bu öznitelik gruplarındaki tüm öznitelikleri devralır.

4. Houston kanalında kullanılabilir olması için öznitelikleri etkinleştirin:

    1. Eylem Bölmesinde **Öznitelik meta verisi ayarla**'yı seçin.
    2. **Moda** kategori düğümünü ve ardından **Kanal ürün öznitelikleri** hızlı sekmesinde her öznitelik için **Özniteliği ekle**'yi seçin.
    3. **Moda Aksesuarlar** kategori düğümünü, **Moda Güneş Gözlükleri** kategorisini ve ardından **Kanal ürün öznitelikleri** hızlı sekmesinde her öznitelik için **Özniteliği ekle**'yi seçin.
    4. **Erkek giyim** kategori düğümünü, **Pantolonlar** kategorisini ve ardından **Kanal ürün öznitelikleri** hızlı sekmesinde her öznitelik için **Özniteliği ekle**'yi seçin.

![Kanal kategorileri ve ürün öznitelikleri - Öznitelik grupları.](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Geçersiz kılınan öznitelik değerleri

Özniteliklerinin varsayılan değerleri ayrı ürünler için ürün düzeyinde geçersiz kılınabilir. Varsayılan değerler belirli kanallarda hedeflenen belirli kataloglardaki ayrı ürünler için de geçersiz kılınabilir.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Tek bir ürününü öznitelik değerlerini geçersiz kılma

1. Alım satım yöneticisi olarak arka ofis istemcisinde oturum açın.
2. **Retail ve Commerce** &gt; **Kategori ve ürün yönetimi** &gt; **Kategoriye göre serbest bırakılan ürünler**'e gidin.
3. **Moda** &gt; **Moda Aksesuarlar** &gt; **Moda Güneş Gözlükleri** kategori düğümünü seçin.
4. Izgaradan gerekli ürünü seçin. Ardından Eylem Bölmesinde, **Ürün** sekmesindeki **Ayar** gurubunda **Ürün öznitelikleri**'ni seçin.
5. Sol bölmeden bir öznitelik seçin ve ardından sağ bölmede değerini güncelleştirin.

![Ürün ayrıntıları sayfası – Ürün öznitelik grupları.](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Katalogdaki ürünlerin öznitelik değerlerini geçersiz kılma

1. Alım satım yöneticisi olarak arka ofis istemcisinde oturum açın.
2. **Retail ve Commerce** &gt; **Katalog yönetimi** &gt; **Tüm kataloglar**'a gidin.
3. **Fabrikam Temel Kataloğu** kataloğunu seçin.
4. **Moda** &gt; **Moda Aksesuarlar** &gt; **Moda Güneş Gözlükleri** kategori düğümünü seçin.
5. **Ürünler** hızlı sekmesinde gerekli ürünü seçin ve ardından ızgaranın üstünden **Öznitelikler**'i seçin.
6. Aşağıdaki hızlı sekmelerde gereken özniteliklerin değerlerini güncelleştirin:

    - Paylaşılan ürün ortamı
    - Paylaşılan ürün öznitelikleri
    - Kanal ortamı
    - Kanal ürünü öznitelikleri

    > [!NOTE]
    > Paylaşılan ürün ortamı ve paylaşılan ürün öznitelikleri oluşturulursa, tüm ürünlere uygulanır.

![Katalog ürünü öznitelik grupları.](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Kanaldaki ürünlerin öznitelik değerlerini geçersiz kılma

1. Alım satım yöneticisi olarak arka ofis istemcisinde oturum açın.
2. **Retail ve Commerce** &gt; **Kanal kurulumu** &gt; **Kanal kategorileri ve ürün öznitelikleri**.
3. **Houston** kanalını seçin.
4. **Ürünler** hızlı sekmesinde gerekli ürünü seçin ve ardından ızgaranın üstünden **Öznitelikler**'i seçin.

    > [!NOTE]
    > Kullanılabilir ürün yoksa **Ürünler** hızlı sekmesinde **Ekle**'yi ve daha sonra **Ürün ekle** iletişim kutusunda gerekli ürünleri seçerek ürün ekleyin.

5. Aşağıdaki hızlı sekmelerde gereken özniteliklerin değerlerini güncelleştirin:

    - Paylaşılan ürün ortamı
    - Paylaşılan ürün öznitelikleri
    - Kanal ortamı
    - Kanal ürünü öznitelikleri

    > [!NOTE]
    > Paylaşılan ürün ortamı ve paylaşılan ürün öznitelikleri oluşturulursa, tüm ürünlere uygulanır.


[!INCLUDE[footer-include](../includes/footer-banner.md)]