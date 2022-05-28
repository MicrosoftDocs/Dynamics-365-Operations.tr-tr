---
title: Gider hesabına naklet muhasebe ilkesi
description: Bu konu, gider hesabına naklet muhasebe ilkesine genel bakış sağlar.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 45dc1775c0db83faa89a7a1fa799bdd070d1b09a
ms.sourcegitcommit: 283e237d7bd2a76dd3a8ff64685b0a5f146edd25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721407"
---
# <a name="post-to-charge-account-accounting-principle"></a>Gider hesabına naklet muhasebe ilkesi

*Gider hesabına naklet* muhasebe ilkesi, fiziksel deftere nakil ve mali deftere nakil arasındaki birim fiyatta, satın alınan maddelerdeki dolaylı maliyetlerde veya satın alma siparişindeki giderler arasında meydana gelen farkları hesaba katmanıza ve bunlar için daha kolay mutabakat sağlamanıza olanak sağlar. 

Borç hesapları gider kodları için **Masraf kodu** sayfasındaki (**Borç hesapları \> Masraf kurulumu \> Masraf kodu**) iki yapılandırma, bir satın alma siparişinin stok varlıklarının değerlemesini etkilemesine neden olabilir:

- **Borç türü** alanının *Madde* olarak ayarlandığı ve **Alacak türü** alanının *Genel muhasebe hesabı* olarak ayarlandığı masraf kodları için, dolaylı içe alma hesabı olarak seçilen genel muhasebe hesabı bir stok değişim hesabı olarak davranır.
- **Borç türü** alanının *Madde* olarak ayarlandığı ve **Alacak türü** alanının *Müşteri/Satıcı* olarak ayarlandığı masraf kodları için gider, malzeme maliyeti olarak hesaba katılır ve maddenin stok değişim hesabı kullanılır.

## <a name="european-special-accounting-rule"></a>Avrupa özel muhasebe kuralı

Avrupa'da, *gider hesabına naklet* muhasebe ilkesi genellikle özel bir muhasebe kuralı eklemek için kullanılır. Örneğin, aşağıdaki yöntemlerden biri genellikle stok değişikliklerini dikkate almak için kullanılır:

- **Satış maliyeti yöntemi** – Standart stok deftere nakil profili yapılandırması bu yöntemi destekler. *Gider hesabına naklet* muhasebe ilkesi gerekli değildir.
- **Gider türü yöntemi** – Daha küçük kuruluşlar genellikle bu yöntemi kullanır. Tipik olarak aşağıdaki adımları içerir:

    1. Mal veya hizmetler giriş sırasında tamamen gider olarak işlenir.
    2. Dönemin sonunda döngü sayımı gerçekleştirilir.
    3. Miktar ve değer için el ile düzeltme, stoğa nakledilir. (Mahsup hesap, 1. adımda deftere nakledilen gideri mahsup eden bir stok değişim hesabıdır. Bu nedenle, stok değerindeki değişikliği yalnızca bu hesap üzerinde görürsünüz.)

*Gider hesabına naklet* ilkesi, iki deftere nakil işlemini tamamen otomatikleştirmenizi sağlar. Bu şekilde, dönem sonu kapatma düzeltmesinin deftere naklini ortadan kaldırabilirsiniz.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Gider hesabına naklet muhasebe ilkesini etkinleştirme

*Gider hesabına naklet* muhasebe ilkesini etkinleştirmek için, aşağıdaki adımları izleyin.

1. **Borç hesapları \> Kurulum \> Borç hesapları parametreleri**'ne gidin.
2. **Fatura** sekmesinde, **Fatura** hızlı sekmesinde, **Genel muhasebedeki gider hesabına naklet** seçeneğini *Evet* olarak ayarlayın.
3. Sayfayı kapatın.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Gider hesabına naklet muhasebe ilkesine ilişkin önkoşullar ve önerilen parametreler

Satın alma masrafları ve stok varyasyonlarını hesaba katmayı planlıyorsanız aşağıdaki önkoşulların sağlanması gerekir:

- **Borç hesapları parametreleri** sayfasındaki (**Borç hesapları \> Kurulum \> Borç hesapları parametreleri**) **Fatura** sekmesinde **Genel muhasebedeki gider hesabına naklet** seçeneği *Evet* olarak ayarlanmalıdır.
- **Madde modeli grupları** sayfasında (**Maliyet yönetimi \> Stok muhasebe ilkeleri kurulumu \> Madde model grupları**), bir satın alma siparişine dahil edilen maddeleri içeren her ilgili model grubu için aşağıdaki tüm seçeneklerin *Evet* olarak ayarlanması gerekir:

    - Fiziksel stoğu deftere naklet
    - Mali stoğun deftere nakli
    - Ürün girişindeki tahakkuk borcu

- **Tedarik ve kaynak atama parametreleri** sayfasının **Teslim** sekmesinde (**Tedarik ve kaynak \> Kurulum \> Tedarik ve kaynak parametreleri**), **Ürün girişinde masraf oluştur** seçeneği *Evet* olarak ayarlanmalıdır.
- **Stok ve ambar yönetimi parametreleri** sayfasının (**Stok Yönetimi \> Kurulum \> Stok ve ambar yönetimi parametreleri**) **Stok muhasebesi** sekmesinde, **Sevk irsaliyesini genel muhasebeye naklet** seçeneğini *Evet* olarak ayarlamalısınız.
- Aşağıdaki deftere nakil tiplerinin her biri için, **Deftere nakil** sayfasının ( **Stok yönetimi \> Kurulum \> Deftere nakil \> Deftere nakil**) **Satın alma siparişi** sekmesinde, her ilgili maddeye uygulanan ana hesaplar belirtilmelidir:

    - Faturalanmamış satınalma harcaması
    - Ürün için satınalma harcaması
    - Stok değişimi

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Örnek senaryo 1: Birim maliyet fiyatındaki değişiklik

Bu örnek senaryo aşağıdaki önkoşullara sahiptir:

- İlk giren ilk çıkar (FIFO) maliyetlendirme modeli

Aşağıdaki prosedür, bir satın alma siparişinin birim maliyet fiyatını değiştirdiğinizde neler olacağını gösteren bir örnek sağlar.

1. Miktar olarak 1, birim fiyatı olarak 100,00 şeklinde bir satın alma siparişi oluşturun.
2. Satınalma siparişini doğrulayın.
3. Satın alma siparişi için ürün girişini deftere nakledin.
4. Ürün girişinde fişi doğrulayın. Aşağıdaki tabloda örnek bir fiş gösterilmektedir.

    | Deftere nakil türü | Ana hesap | Ana hesap adı | Hesap türü | Borç/Alacak? | Kliring hesabı | Fiziksel/Mali? | Tutar |
    |---|---|---|---|---|---|---|---|
    | Satın alma, stok değişimi | 600170 | Stok değişim malzemeleri | Gider | Kredi | No. | Fiziksel | -100,00 |
    | Stoğa giren satın alınmış malzemelerin maliyeti | 140100 | Malzeme Stoğu | Varlık | Borç | Evet | Fiziksel | 100.00 |
    | Faturalanmamış satınalma harcaması | 600180 | Malzeme Girişleri | Gider | Borç | Evet | Fiziksel | 100.00 |
    | Satınalma, tahakkuk | 200140 | Tahakkuk Eden Satın Almalar | Pasif | Kredi | Evet | Fiziksel | -100,00 |

5. Güncelleştirilmiş birim fiyatı 110,00 olan satın alma siparişinin faturasını deftere nakledin.
6. Faturadaki fişi doğrulayın. Aşağıdaki tabloda örnek bir fiş gösterilmektedir.

    | Deftere nakil türü | Ana hesap | Ana hesap adı | Hesap türü | Borç/Alacak? | Kliring hesabı | Fiziksel/Mali? | Tutar |
    |---|---|---|---|---|---|---|---|
    | Satın alma, stok değişimi | 600170 | Stok değişim malzemeleri | Gider | Kredi | No. | Mali | -10,00 |
    | Stoğa giren satın alınmış malzemelerin maliyeti | 140100 | Malzeme Stoğu | Varlık | Borç | Evet | Mali | -100,00 |
    | Faturalanmamış satınalma harcaması | 600180 | Malzeme Girişleri | Gider | Borç | Evet | Mali | -100,00 |
    | Satınalma, tahakkuk | 200140 | Tahakkuk Eden Satın Almalar | Pasif | Kredi | Evet | Mali | 100.00 |
    | Faturalanan satın alınmış malzemelerin maliyeti | 140100 | Malzeme Stoğu | Varlık | Borç | No. | Mali | 110.00 |
    | Ürün için satınalma harcaması | 600180 | Malzeme Girişi | Gider | Kredi | No. | Mali | 110.00 |
    | Satıcı bakiyesi | 211000 | Borç Hesapları Ticari | Pasif | Kredi | No. | Mali | -110,00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Örnek 2: Satın alma siparişindeki giderler ve dolaylı maliyetler

Bu örnek senaryo aşağıdaki önkoşullara sahiptir:

- FIFO maliyetlendirme modeli
- **Masraf kodu 1:** %10 ile maddeyi borçlandırır ve genel muhasebe hesabını alacaklandırır
- **Masraf kodu 2:** 10,00 ile orantılı olarak maddeyi borçlandırır ve müşteriyi/satıcıyı alacaklandırır
- **Dolaylı maliyet:** Satın alma fiyatına %2,00 eklenir

Aşağıdaki prosedür, bir satın alma siparişine giderleri ve dolaylı maliyetleri dahil ettiğinizde neler olacağını gösteren bir örnek sağlar.

1. Miktar olarak 1, birim fiyatı olarak 100,00 şeklinde bir satın alma siparişi oluşturun.
2. Maddeyi borçlandıran ve genel muhasebeyi alacaklandıran yüzde 10 için bir masraf kodu ekleyin.
3. Maddeyi borçlandıran ve müşteriyi/satıcıyı alacaklandıran 10,00 için bir masraf kodu ekleyin.
4. Masrafları satın alma siparişi satırlarına tahsis edin.
5. Satınalma siparişini doğrulayın.
6. Satın alma siparişi için ürün girişini deftere nakledin.
7. Ürün girişinde fişi doğrulayın. Aşağıdaki tabloda örnek bir fiş gösterilmektedir.

    | Deftere nakil türü | Ana hesap | Ana hesap adı | Hesap türü | Borç/Alacak? | Kliring hesabı | Fiziksel veya Mali | Tutar |
    |---|---|---|---|---|---|---|---|
    | Satın alma, stok değişimi | 600170 | Stok değişim malzemeleri | Gider | Kredi | No. | Fiziksel | -110,00 |
    | Mahsup edilen tahmini dolaylı maliyet | 600520 | Mahsup Edilen Dolaylı Maliyetler | Gider | Kredi | Evet | Fiziksel | -2,40 |
    | Satınalma navlunu | 600120 | Navlun/Nakliye Maliyetleri | Gider | Kredi | No. | Fiziksel | -10,00 |
    | Stoğa giren satın alınmış malzemelerin maliyeti | 140100 | Malzeme Stoğu | Varlık | Borç | Evet | Fiziksel | 122.40 |
    | Faturalanmamış satınalma harcaması | 600180 | Malzeme Girişleri | Gider | Borç | Evet | Fiziksel | 110.00 |
    | Satınalma, tahakkuk | 200140 | Tahakkuk Eden Satın Almalar | Pasif | Kredi | Evet | Fiziksel | -110,00 |

8. Satın alma siparişiyle ilgili faturayı deftere nakledin.
9. Faturadaki fişi doğrulayın. Aşağıdaki tabloda örnek bir fiş gösterilmektedir.

    | Deftere nakil türü | Ana hesap | Ana hesap adı | Hesap türü | Borç/Alacak? | Kliring hesabı | Fiziksel/Mali? | Tutar |
    |---|---|---|---|---|---|---|---|
    | Satın alma, stok değişimi | 600170 | Stok değişim malzemeleri | Gider | Kredi | No. | Mali | 0,00 |
    | Mahsup edilen tahmini dolaylı maliyet | 600520 | Mahsup Edilen Dolaylı Maliyetler | Gider | Borç | Evet | Mali | 2.40 |
    | Mahsup edilen dolaylı maliyet | 600520 | Mahsup Edilen Dolaylı Maliyetler | Gider | Borç | No. | Mali | -2,40 |
    | Stoğa giren satın alınmış malzemelerin maliyeti | 140100 | Malzeme Stoğu | Varlık | Kredi | Evet | Mali | -110,00 |
    | Faturalanmamış satınalma harcaması | 600180 | Malzeme Girişleri | Gider | Kredi | Evet | Mali | -110,00 |
    | Satınalma, tahakkuk | 200140 | Tahakkuk Eden Satın Almalar | Pasif | Borç | Evet | Mali | 110.00 |
    | Faturalanan satın alınmış malzemelerin maliyeti | 140100 | Malzeme Stoğu | Varlık | Borç | No. | Mali | 110.00 |
    | Ürün için satınalma harcaması | 600180 | Malzeme Girişi | Gider | Kredi | No. | Mali | 110.00 |
    | Satıcı bakiyesi | 211000 | Borç Hesapları Ticari | Pasif | Kredi | No. | Mali | -110,00 |
