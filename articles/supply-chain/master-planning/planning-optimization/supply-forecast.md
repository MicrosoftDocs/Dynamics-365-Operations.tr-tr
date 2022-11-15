---
title: Tedarik tahminleri ile master planlama
description: Bu makalede, tedarik tahminlerinin master planlama sırasında değerlendirileceği açıklanmaktadır.
author: t-benebo
ms.date: 09/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-21
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2bac9355bb1ac00f697ec459f494a64553e0eacc
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740154"
---
# <a name="master-planning-with-supply-forecasts"></a>Tedarik tahminleri ile master planlama

[!include [banner](../../includes/banner.md)]

Tedarik tahminleri, gelecekteki bir dönemde ihtiyaç duyacağınız tedariki belirlemenize olanak tanır. Genellik, bu tahminde geçmiş yılların satış bilgilerini temel alıp bütçeleme için tahmini kullanırsınız. Master planlarınızı planlama aşamasında tahminleri dikkate alacak şekilde de ayarlayabilirsiniz.

## <a name="set-up-a-master-plan-to-consider-supply-forecasts"></a>Master planı tedarik tahminlerini dikkate alacak şekilde ayarlama

Çalıştırıldığında tahminlerin dikkate alınıp alınmayacağını her master plan için ayrı ayrı belirleyebilirsiniz. Her plan için tahmin seçeneklerini aşağıdaki yordamı kullanarak ayarlayabilirsiniz.

1. **Master planlama \> Kurulum \> Planlar \> Master planlar** bölümüne gidin.
1. Liste bölmesinden mevcut bir master plan seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir plan oluşturun.
1. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Tahmin modeli** – Master planda dikkate alınmasını istediğiniz tedarik ve/veya talep tahminlerini içeren modeli seçin.
    - **Tedarik tahminini dahil et** – Master planın tedarik tahminlerini dikkate alması için bu seçeneği *Evet* olarak ayarlayın.
    - **Talep tahminini dahil et** – Master planın talep tahminlerini dikkate alması için bu seçeneği *Evet* olarak ayarlayın. Bu ayar **Tedarik tahminini dahil et** seçiminden bağımsız olsa da sayfadaki diğer ayarlardan bazıları hem tedarik hem talep tahminlerine uygulanır. Talep tahminlerini dikkate alan planlama hakkında daha fazla bilgi için [Talep tahminleri ile master planlama](demand-forecast.md) bölümüne bakın.
    - **Tahmin gereksinimlerini azaltmak için kullanılan yöntem** – Master planlama sırasında tahmin gereksinimlerini azaltmak için kullanılacak yöntemi seçin.

        - *Hiçbiri* – Master planlama sırasında tahmin gereksinimleri azaltılmaz.
        - *Yüzde - azaltma anahtarı* – Tahmin gereksinimleri azaltma anahtarında tanımlanan yüzdelere ve dönemlere göre azaltılır.
        - *Hareketler – azaltma anahtarı* – Tahmin gereksinimleri azaltma anahtarında tanımlanan dönemler içinde gerçekleşen hareketlere göre azaltılır.
        - *Hareketler – dinamik dönem* – Tahmin gereksinimleri, dinamik dönem içinde gerçekleşen sipariş hareketlerine göre azaltılır. Dinamik dönem, geçerli tahmin tarihlerini kapsar ve bir sonraki tahmin başladığında sona erer. *Hareketler – dinamik dönem* yönteminde bir azaltma anahtarı kullanılmaz veya gerekmez. Bu yöntemi kullandığınızda aşağıdaki koşullar geçerlidir:

            - Tahmin tümüyle azaltıldıysa, geçerli tahminin tahmin gereksinimleri 0 (sıfır) olur.
            - Gelecekte başka bir tahmin yoksa, girilen son tahmindeki tahmin gereksinimleri azaltılır.
            - Zaman dilimleri, tahmin azaltma hesaplamasına eklenir.
            - Artı günler, tahmin azaltma hesaplamasına eklenir.
            - Fiili sipariş hareketlerinin tahmin gereksinimlerini aşması durumunda, kalan hareketler sonraki tahmin dönemine iletilmez.

        > [!NOTE]
        > Master planlama için talep tahminlerini de etkinleştirdiyseniz **Tahmin gereksinimlerini azaltmak için kullanılan yöntem** ayarı talep tahminleri için de geçerlidir ve bu tahminleri de benzer şekilde etkiler. Daha fazla bilgi için [Talep tahminleri ile master planlama](demand-forecast.md) bölümüne bakın.

## <a name="set-reduction-options-for-coverage-groups"></a>Kapsam grupları için azaltma seçeneklerini ayarlama

Kapsam grubunun hareket temelli azaltma kullanan master planlarda tahmin gereksinimlerini nasıl azaltacağını denetleyen seçenekleri ayarlamak için aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Planlar \> Kapsam grupları**'na gidin.
1. Liste bölmesinden mevcut bir kapsam grubunu seçin veya Eylem Bölmesinden **Yeni**'yi seçerek yeni bir grup oluşturun.
1. **Tahmin gereksinimlerini azaltmak için kullanılan yöntem** alanının *Hareketler - azaltma anahtarı* veya *Hareketler - dinamik dönem* olarak ayarlandığı master planlarda, **Diğer** hızlı sekmesinde, **Tahmin azaltma ölçütü** alanında, kapsam grubundaki maddeler için tedarik tahmini gereksinimlerinin nasıl azaltılacağını belirtin. Aşağıdaki değerlerden birini seçin:

    - *Tüm hareketler*: Tüm hareketler tahmini azaltır.
    - *Siparişler* – Yalnızca aynı türden siparişler tahmini azaltır.

    Örneğin, bir maddenin varsayılan sipariş ayarlarının bu maddenin üretilmesi gerektiğini gösterdiğini varsayalım. 50 adet için bir tedarik tahmini satırı ve 20 adetlik mevcut bir satınalma siparişi olsun. **Tahmin azaltma ölçütü** alanı *Siparişler* olarak ayarlanmışsa planlı üretim emri 50 adet için oluşturulur. Bu alan *Tüm hareketler* olarak ayarlanmışsa planlı üretim emri 30 adete düşürülür.

    Bu ayar, talep tahminini azaltmak için de kullanılır. Daha fazla bilgi için [Talep tahminleri ile master planlama](demand-forecast.md) bölümüne bakın.

## <a name="enter-a-supply-forecast-for-a-product"></a>Ürün için bir tedarik tahmini girme

Ürüne bir tedarik tahmini girmek için aşağıdaki adımları izleyin.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Tahmin girmek istediğiniz ürünü seçin.
1. Eylem Bölmesi'nin **Plan** sekmesinde **Tedarik tahmini**'ni seçin.
1. Eylem Bölmesi'nin **Tedarik tahmini** sayfasında, **Yeni**'yi seçerek yeni bir ızgara ekleyin.
1. Tahminini belirtmek için gereken bilgileri yeni bir satır olarak girin.

## <a name="plan-for-an-item-with-supply-forecast-lines"></a>Tedarik tahmini satırları olan maddeyi planlama

Tedarik tahmini bulunan bir master plan çalıştırdığınızda, sistem girilmiş tedarik satırları için bir satınalma siparişi oluşturur. Maddenin varsayılan sipariş ayarları dikkate alınır. Bu varsayılan sipariş ayarlarında *Satınalma siparişi* için **Varsayılan sipariş türü** tanımlanmışsa ve tedarik tahmini satırında herhangi bir satıcı hesabı belirtilmemişse, sistem öğenin varsayılan satıcısını kullanır.

## <a name="check-whether-a-planned-order-is-a-supply-forecast-order"></a>Planlı siparişin tedarik tahmini siparişi olup olmadığını denetleme

Planlı bir siparişin tedarik tahmini sonucu oluşturulup oluşturulmadığını öğrenmek için aşağıdaki yordamı kullanın.

1. **Master planlama \> Master planlama \> Planlı siparişler** öğesine gidin.
1. İncelemek istediğini planlı siparişi açın.
1. **Genel** hızlı sekmesinde, **Tedarik tahmini** alanının değerine bakın. Sipariş bir tedarik tahminini kapsayacak şekilde oluşturulmuşsa, bu alanda *Evet* seçeneği görüntülenir.

## <a name="examples-of-master-planning-with-supply-forecasts"></a>Tedarik tahminleri ile master planlama örnekleri

Bu bölümde, tedarik tahminlerinin master planlamayı nasıl etkilediğini gösteren bazı örnekler verilmektedir.

### <a name="example-1-supply-forecast-for-an-item"></a>Örnek 1: Bir madde için tedarik tahmini

Varsayılan sipariş türü *Satınalma siparişi* ve varsayılan satıcısı *US-002* olan bir maddeniz olduğunu varsayalım. Maddenin tedarik tahmini satırı aşağıdaki gibidir.

| Model    | Tarih     | Satıcı hesabı | Satıcı grubu | Miktar | Birim | Site | Ambar |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | her biri   | 1    | 11        |

Master planlamayı çalıştırdığınızda, planlı satınalma siparişi *US-002* satıcısından *35 ea* için oluşturulur.

### <a name="example-2-several-supply-forecast-lines-with-and-without-a-vendor"></a>Örnek 2: Satıcısı olan ve olmayan birden fazla tedarik tahmini satırı

Varsayılan sipariş türü *Satınalma siparişi* ve varsayılan satıcısı *US-002* olan bir maddeniz olduğunu varsayalım. Maddenin tedarik tahmini satırları aşağıdaki gibidir.

| Model    | Tarih     | Satıcı hesabı | Satıcı grubu | Miktar | Birim | Site | Ambar |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                |              | 35       | her biri   | 1    | 11        |
| CurrentF | 10/10/22 | US-101         |              | 25       | her biri   | 1    | 11        |

Bu durumda, sistem satıcı belirtilmeyen satırı genel tahmin olarak kabul eder ve satıcı belirtilen satırın genel tahminden çıkarılması gerektiğini varsayar. Bu nedenle, master planlama bu madde için aşağıdaki planlı satınalma siparişlerini oluşturur:

- *US-101* satıcısından *25 ea* adetlik bir planlı satınalma siparişi (Tahmin satırında belirtilen satır ve miktar kullanılır.)
- *US-002* satıcısından *10 ea* adetlik bir planlı satınalma siparişi (Diğer tahmin satırında satıcı belirtilmediğinden varsayılan satıcı kullanılır. Bu tahmin satırının miktarı satıcı belirtilmiş olan tahmin satırındaki miktar düşülerek belirlenir.)

### <a name="example-3-plans-that-use-the-transactions---dynamic-period-reduction-method-in-a-single-forecast-period"></a>Örnek 3: Tek bir tahmin döneminde azaltma yöntemi olarak Hareketler - dinamik dönem kullanan planlar

Tahmin azaltma yöntemi olarak *Hareketler - dinamik dönem* kullanan master planlarda, tedarik özellikleriyle eşleşen mevcut hareketler varsa master planlamada tahmin miktarları azaltılır.

Örneğin, varsayılan sipariş türü *Satınalma siparişi* olan bir maddeniz olduğunu varsayalım. Maddenin tedarik tahmini satırı aşağıdaki gibidir.

| Model    | Tarih     | Satıcı hesabı | Satıcı grubu | Miktar | Birim | Site | Ambar |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | her biri   | 1    | 11        |

Tek bir tedarik tahmini satırı olduğundan yalnızca bir tahmin dönemi vardır.

Azaltma yöntemi olarak *Hareketler – dinamik dönem* kullanmaya ayarlanmış bir master planı çalıştırdığınızda aşağıdaki sonuçlardan biri meydana gelebilir:

- *US-101* satıcısı için *10 ea* adetlik bir satınalma siparişi varsa ve **Tedarik tahmini** alanı *Evet* olarak ayarlanmışsa, master planlama *10 ea* üzerinden kalan miktar için yeni bir planlı satınalma siparişi oluşturur. Satıcı mevcut satınalma siparişiyle eşleştiğinden, tahmin satırı azaltılır.
- *US-102* satıcısı, *1* tesisi, *11* ambarı için *10 ea* adetlik bir satınalma siparişi varsa ve **Tedarik tahmini** alanı *Evet* olarak ayarlanmışsa, master planlama toplam *25 ea* adetlik yeni bir planlı satınalma siparişi oluşturur. Mevcut satınalma siparişinden farklı bir satıcıya sahip olduğundan, tahmin satırı azaltılmaz.

> [!NOTE]
> Bir satıcı ilişkilendirilmiş planlı satınalma siparişlerinde bu durumla karşılaşabilirsiniz. Ancak transfer emirleri ve üretim emirlerinde, bu sipariş türlerinde satıcı belirtilmediğinden, tedarik tahmini miktarları her zaman mevcut sipariş kadar azaltılır.

### <a name="example-4-plans-that-use-the-transactions---dynamic-period-reduction-method-over-several-forecast-periods"></a>Örnek 4: Birden fazla tahmin döneminde azaltma yöntemi olarak Hareketler - dinamik dönem kullanan planlar

Örneğin, varsayılan sipariş türü *Satınalma siparişi* olan bir maddeniz olduğunu varsayalım. Maddenin tedarik tahmini satırları aşağıdaki gibidir.

| Model    | Tarih     | Satıcı hesabı | Satıcı grubu | Miktar | Birim | Site | Ambar |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | her biri   | 1    | 11        |
| CurrentF | 15/10/22 | US-101         |              | 25       | her biri   | 1    | 11        |

Bu örnekte, her biri farklı tarihe sahip iki tahmin satırı vardır. Bu nedenle, tahmin dönemlerinin sınırlarını bu tarihler belirler. İlk dönem 10 Ekim - 14 Ekim 2022 (10/10/2022–14/10/2022) arasıdır. İkinci dönem de 15 Ekim 2022 (15/10/2022) ve sonrasıdır.

*US-101* satıcısı için *10 ea* adetlik, *12/10/2022* (12 Ekim 2022) tarihli mevcut bir satınalma siparişi vardır. Azaltma yöntemi olarak *Hareketler – dinamik dönem* kullanmaya ayarlanmış bir master planı çalıştırdığınızda aşağıdaki siparişler oluşturulur:

- *10/10/2022* tarihli *15 ea* adetlik bir planlı sipariş (Miktar aynı tahmin dönemine tarihlenmiş mevcut satınalma siparişi kadar azaltılır.)
- *15/10/2022* tarihli *25 ea* adetlik bir planlı sipariş (Miktar tahminin tam miktarı kadardır.)

### <a name="example-5-plans-that-use-no-reduction"></a>Örnek 5: Azaltma kullanmayan planlar

Tahmin azaltma yöntemi *Hiçbiri* olarak ayarlanmış bir plan çalıştırdığınızda, master planlama her zaman, tüm tedarik tahmini satırları için planlı tedarik oluşturur. Planlı tedarik onaylandıktan sonra bu miktarı gelecek planlı siparişlerden düşer. Ancak satınalma siparişleri tedarik tahmini satırlarını azaltmaz.

Örneğin, varsayılan sipariş türü *Satınalma siparişi* olan bir maddeniz olduğunu varsayalım. Maddenin tedarik tahmini satırı aşağıdaki gibidir.

| Model    | Tarih     | Satıcı hesabı | Satıcı grubu | Miktar | Birim | Site | Ambar |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 | US-101         |              | 25       | her biri   | 1    | 11        |

*US-101* satıcısı, *1* tesisi, *11* ambarı için *25 ea* adetlik, *10/10/22* tarihli mevcut bir satınalma siparişi vardır. 

Azaltma yöntemi olarak *Hiçbiri* kullanmaya ayarlanmış bir master plan çalıştırdığınızda *US-101* satıcısı, *1* tesisi, *11* ambarı için *25 ea* adetlik, *10/10/22* tarihli bir planlı satınalma siparişi oluşturur. Diğer bir deyişle, tahmin azaltma yöntemi *Hiçbiri* olduğundan mevcut satınalma siparişi azaltılmaz.

Son planlama çalıştırmasından sonra oluşturulan planlı satınalma siparişini bu aşamada düzenleyip miktarı *15 ea* olarak değiştirin. Ardından siparişi onaylayın. Master planı bir sonraki çalıştırmanızda, *US-101* satıcısı, *1* tesisi, *11* ambarı için *10 ea* adetlik, *10/10/22* tarihli bir planlı satınalma siparişi oluşturur. Bu kez, miktar, önceki planlama çalıştırmasından gelen onaylanmış mevcut siparişin miktarını yansıtacak şekilde azaltılır.

## <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Planlama Optimizasyonu ile kullanımdan kaldırılan master planlama altyapısı arasındaki farklar

Tedarik tahminleri, kullandığınız planlama altyapısına (Planlama Optimizasyonu veya kullanımdan kaldırılan master planlama altyapısı) bağlı olarak farklı şekillerde çalışır. Bu bölümde bu farklar açıklanmaktadır.

### <a name="vendor-groups"></a>Satıcı grupları

Bir tahmin satırı eklediğinizde, bir satıcı ve satıcı grubu belirtebilirsiniz. Kullanımdan kaldırılan master planlama altyapısında, oluşturulan planlı siparişler satıcı ve satıcı grubu değerlerinin birleşimine göre gruplanır. Planlama Optimizasyonu'nda, planlı siparişler satıcıya göre gruplanır.

Aşağıdaki tabloda bir madde için tedarik tahmini satırı örnekleri verilmiştir.

| Model    | Tarih     | Satıcı hesabı | Satıcı grubu | Miktar | Birim | Site | Ambar |
|----------|----------|----------------|--------------|----------|------|------|-----------|
| CurrentF | 10/10/22 |                | VendorGroupA | 5        | her biri   | 1    | 11        |
| CurrentF | 10/10/22 |                | VendorGroupA | 6        | her biri   | 1    | 11        |
| CurrentF | 10/10/22 |                |              | 7        | her biri   | 1    | 11        |

*VendorA* satıcısı *VendorGroupA* satıcı grubu için varsayılan satıcıdır. Ayrıca madde için de varsayılan satıcıdır.

Kullanımdan kaldırılan master planlama altyapısı aşağıdaki siparişleri oluşturur:

- *VendorA* satıcısı, *VendorGroupA* satıcı grubu için *11* adetlik bir planlı satınalma siparişi
- *VendorA* satıcısı için *7* adetlik bir planlı satınalma siparişi

Planlama Optimizasyonu yalnızca bir sipariş oluşturur:

- *VendorA* satıcısı, *VendorGroupA* satıcı grubu için *18* adetlik bir planlı satınalma siparişi

### <a name="reduction-of-general-forecasts-by-more-specific-forecasts"></a>Genel tahminleri daha belirgin tahminlere göre azaltma

Kullanımdan kaldırılan master planlama altyapısında, bazı tahminlerin satıcısı belirtilip bazılarının belirtilmediğinde sonuç öngörülemez.

Planlama Optimizasyonu'nda, genel tahminler her zaman daha belirgin tahminler kadar azaltılır. Aşağıda bir örnek verilmiştir.

Aşağıdaki tabloda bir madde için tedarik tahmini satırı örnekleri verilmiştir.

| Tarih       | Miktar | Satıcı   | Satıcı grubu  |
|------------|----------|----------|---------------|
| 02/11/2022 | 5.00     | Vendor-A | VendorGroup-A |
| 02/11/2022 | 6,00     | Vendor-A | VendorGroup-A |
| 02/11/2022 | 15.00    |          |               |

Genel tahmin (15,00 adet için) daha belirgin tahminler (5,00 + 6,00 = 11,00 adet) kadar azaltılır. Kalan miktar varsayılan satıcıya atanır. Aşağıdaki tabloda, planlı siparişler gösterilmektedir.

| Tarih       | Miktar | Satıcı   | Satıcı grubu  |
|------------|----------|----------|---------------|
| 02/11/2022 | 11.00    | Vendor-A | VendorGroup-A |
| 02/11/2022 | 4.00     | Vendor-A | VendorGroup-A |

### <a name="respect-for-default-order-settings-when-planned-orders-are-generated"></a>Planlı siparişler oluşturulurken varsayılan sipariş ayarlarına uyum

Her maddenin minimum satınalma siparişi miktarı gibi varsayılan sipariş ayarları olabilir. Kullanımdan kaldırılan master planlama altyapısı bu ayarları yoksayar ve tahminleri aynı miktara sahip planlı siparişlere çevirir. Planlama Optimizasyonu planlı siparişler tedarik tahminlerine göre oluşturulduğunda bu ayarları geçerli sayar. 

### <a name="aggregation-of-planned-orders-as-a-result-of-reduction-by-approved-orders"></a>Onaylanmış siparişlere göre yapılan azaltma sonucunda planlı siparişlerin toplamı

Kullanımdan kaldırılan master planlama altyapısı yalnızca bir siparişin mevcut tedarik tahminini azaltacağını varsayar. Bu nedenle, bir tedarik tahmini satırıyla eşleşen birden fazla sipariş olduğunda yalnızca ilk sipariş tahminden düşülür. Planlama Optimizasyonu'nda, tedarik tahminiyle eşleşen tüm siparişler tahminden düşülür.

### <a name="reduction-of-forecasts-by-matching-vendors-only"></a>Tahminleri yalnızca eşleşen satıcılara göre azaltma

Kullanımdan kaldırılan master planlama altyapısı bir tahmini mevcut serbest bırakılmış satınalma siparişlerine göre azaltırken, satınalma siparişindeki satıcının tahmindeki satıcıyla eşleşip eşlemediğini denetlemez. Planlama Optimizasyonu tahminleri yalnızca satıcı alanındaki değerleri eşleşen satınalma siparişlerine göre azaltır.

Transfer ve üretim emirlerinde, satıcı bilgisi bu sipariş türleriyle ilgili olmadığından satıcı alanı her zaman yoksayılır.

### <a name="reduction-of-forecasts-by-transfer-orders"></a>Tahminleri transfer emirlerine göre azaltma

Bir maddenin varsayılan sipariş türü *Transfer* olarak ayarlanmışsa, tahminler yalnızca mevcut planlı transfer emirlerine göre azaltılabilir. Ancak üretim emirleri ve satınalma siparişlerinde, yalnızca serbest bırakılan siparişler tedarik tahminini azaltır.

Kullanımdan kaldırılan master planlama altyapısı tüm transfer emri durumlarında miktarı azaltırken Planlama Optimizasyonu yalnızca *Serbest Bırakıldı* durumundaki transfer emirlerinin miktarını azaltır.
