---
title: Faturalama planı özellikleri
description: Bu konuda, fiyatlandırma yöntemleri, artışlar ve iskontolar, uyumlu hale getirme tarihleri, eşit dağıtma, ters faturalama ve bölünmüş madde grupları gibi faturalama planı özellikleri açıklanmaktadır.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 0ce323565a94e8e70d90a65b7a3143e984a1c159
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8700733"
---
# <a name="billing-schedule-features"></a>Faturalama planı özellikleri

[!include [banner](../includes/banner.md)]

Bu konu, faturalama planlarının ve fatura planı satırlarının özelliklerini açıklar. Fiyatlandırma için kullanılan farklı yöntemleri, artış ve indirimlerin nasıl kullanılacağını ve faturalama döneminin nasıl tersine çevrileceğini açıklar. Eşit dağıtma hesaplamaları ve bölünmüş madde grupları ile ilgili örnekleri de içerir.

## <a name="pricing-methods"></a>Fiyatlandırma yöntemleri

Bir maddenin birim fiyatını hesaplamak için aşağıdaki fiyatlandırma yöntemlerinden birini kullanabilirsiniz:

* Düz
* Standart
* Katman
* Düz katman

### <a name="flat-pricing"></a>Düz fiyatlandırma

Düz fiyatlandırma yöntemi kullanıldığında, **Tüm faturalama planları** sayfasındaki bir faturalama planı satırı öğesinin birim fiyatı, istediğiniz herhangi bir değere göre düzenlenebilir. **Fiyat birimi** değeri her zaman **1**'dir. Bu nedenle, bir maddenin **Birim fiyat** ve **Net tutar** değerleri aynıdır.

### <a name="standard-pricing-without-a-trade-agreement"></a>Standart fiyatlandırma (ticari anlaşma olmadan)

Standart fiyatlandırma yöntemi bir ticari sözleşme olmadan kullanıldığında, **Serbest bırakılan ürün detayları** sayfasında **Ürün bilgileri yönetimi**'ni seçerek bir faturalama planı satır maddesi için birim fiyatı ayarlarsınız. Birim fiyat, **Temel satış fiyatı** bölümünde gösterilir. *Fiyat* &divide; *Fiyat miktarı* olarak hesaplanır.

### <a name="standard-pricing-with-a-trade-agreement"></a>Standart fiyatlandırma (ticari anlaşma ile)

Aşağıdaki örneklerde, bir ticari anlaşma mevcut olduğunda standart fiyatlandırma hesaplamaları gösterilmektedir. **Serbest bırakılan ürün detayları** sayfasından ticari sözleşmeler oluşturabilirsiniz.

Örneklerin her ikisi de aşağıdaki fiyat aralıklarına sahip bir öğeyi kullanır.

| En az miktar | En çok miktar | U/M | Fiyat | Fiyata esas miktar |
|---|---|---|---|---|
| 0 | 100 | Her biri | 1,50 | 1 |
| 100 | 200 | Her biri | 1.25 | 1 |
| 200 | 999999 | Her biri | 1,00 | 1 |

**Örnek 1**

Fatura miktarı 250'dir, standart fiyatlandırma yöntemi kullanılır. Miktar 200-999.999 fiyat miktarı aralığında olduğundan birim fiyat 1,00'dır. 

Net tutar aşağıdaki şekilde hesaplanır:

*Net tutar* = (*Miktar* &times; *Fiyat*) &divide; *Fiyat birimi* = (250 &times; 1,00) &divide; 1 = 250

**Örnek 2**

Fatura miktarı 100'dür, standart fiyatlandırma yöntemi kullanılır. Fatura miktarı 0-100 fiyat miktarı aralığında olduğundan birim fiyat 1,50'dir.

> [!NOTE]
> Fatura miktarı 100 – 200 aralığı yerine 0 – 100 aralığındadır çünkü standart miktar eşleme davranışında miktar, "en az" miktardan *daha büyük veya buna eşitse* ve "en çok" miktardan *daha azsa* eşleşir.

Net tutar aşağıdaki şekilde hesaplanır:

*Net tutar* = (100 &times; 1,50) &divide; 1 = 150

### <a name="tier-pricing"></a>Katmanlı fiyatlandırma

Aşağıdaki örnekte, şu fiyat aralıklarına sahip bir öğe kullanılır.

| En az miktar | En çok miktar | U/M | Fiyat | Fiyata esas miktar |
|---|---|---|---|---|
| 0 | 100 | Her biri | 1,50 | 10 |
| 100 | 200 | Her biri | 1.25 | 10 |
| 200 | 999999 | Her biri | 1,00 | 10 |

Fatura miktarı 250 ise ve katmanlı fiyatlandırma yöntemi kullanılırsa, maddelerin fiyatları fiyatlandırma aralıkları temel alınarak aşağıdaki şekilde hesaplanır:

- **İlk 100 öğe:** 100 &times; 1,50 = 150,00
- **İkinci 100 öğe:** 100 &times; 1,25 = 125,00
- **Kalan öğeler:** 50 &times; 1,00 = 50,00

Net tutar aşağıdaki şekilde hesaplanır:

*Net tutar* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Net tutar hesaplandıktan sonra birim fiyat, net tutarın miktara bölünmesiyle hesaplanır:

*Birim fiyat* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Düz katmanlı fiyatlandırma

Aşağıdaki örnekte, şu fiyat aralıklarına sahip bir öğe kullanılır.

| En az miktar | En çok miktar | U/M | Düz katman tutarı | Fiyata esas miktar |
|---|---|---|---|---|
| 0 | 50 | Her biri | 100.00 | 50 |
| 50 | 200 | Her biri | 150.00 | 200 |

Aşağıdaki tabloda, satın alınan farklı miktarlar için faturalar ve birim fiyatlar gösterilmektedir. Önce net tutar, ardından da birim fiyat hesaplanır.

| Fatura | Satın alınan miktar | Birim fiyatı | Net tutar |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Artışlar ve iskontolar

*Artış*, faturanın henüz oluşturulmamış olduğu gelecekteki bir faturalama dönemi için fiyat artışıdır. *İskonto*, faturanın henüz oluşturulmamış olduğu gelecekteki bir faturalama dönemi için fiyat düşüşüdür.

Abonelik faturalamasında, artışlar ve iskontolar bir faturalama planına geriye dönük olarak uygulanamaz. Örneğin artışı, üç ay önceki bir faturalama planına uygulayamazsınız ve işleyemezsiniz. Diğer bir deyişle, üç ay önce oluşan bir fiyat artışı uygulayamazsınız.

Aşağıdaki konumlardan birinde, bir faturalama planı veya faturalama planı satırına artış veya iskonto uygulayabilirsiniz:

- **Tüm/Etkin faturalama planları** liste sayfası
- Belirli bir faturalama planı
- Belirli bir faturalama planı satırı

### <a name="apply-an-escalation-or-discount"></a>Artış veya iskonto uygulama

Bir faturalama planına artış veya iskonto uygulamak için, aşağıdaki adımları izleyin.

1. Bir faturalama planı veya bir faturalama planı satırı seçin.
2. **Artış ve iskonto** sekmesinde ya da faturalama planı satırında **Artış ve iskonto**'yu seçin.
3. Artış veya indirimi hesaplamak için bir tüketici fiyat endeksi kullanılıyorsa, **Tüketici fiyat endeksi hesaplaması** alanında bir değer seçin.
4. Bir artış veya indirim satırı eklemek için **Yeni**'yi seçin.
5. İskonto için, **İskonto** onay kutusunu seçin. Artış için, **İskonto** onay kutusunu işareti kaldırılmış durumda bırakın.
6. **Başlangıç tarihi** ve **Sıklık** alanlarını ayarlayın.
7. Faturalanmamış gelir özelliğini kullanan erteleme maddeleri için **Bitiş tarihi** alanını ayarlayın.
8. **Yüzde**, **Tutar** veya **Tüketici fiyat endeksi planı** alanını ayarlayın.
9. **Bitiş tarihi** alanını ayarlayın.
10. **Tamam**'ı seçin.
11. Gereksinim duyduğunuz her ek artış veya indirim satırı için 4 ile 10 arasındaki adımları yineleyin.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Faturalama planı satırları sayfasındaki alanlar

**Faturalama planı satırları** sayfası, aşağıdaki alanları içerir.

| Alan | Açıklama |
|---|---|
| Madde numarası | Faturalama planı satırının madde numarası. Bu alan yalnızca, sayfa bir faturalama planı satır maddesinden açıldığında kullanılabilir. |
| Tüketici fiyat endeksi hesaplaması | <p>Tüketici fiyat endeksi artışını hesaplamak için kullanılan yöntemi seçin:</p><ul><li>**Önceki tüketici fiyat endeksi** – Artış hesaplaması için önceki tüketici fiyat endeksi değerini kullanın.</li><li>**Temel tüketici fiyat endeksi** – Artış hesaplaması için temel tüketici fiyat endeksi değerini kullanın.</li></ul> |
| **Satır** kılavuzu | |
| İskonto | <p>Tutarda yapılan değişikliğin bir artış veya indirim olup olmayacağını belirtmek için onay kutusunu ayarlayın:</p><ul><li>**Seçildi** - Değişiklik, faturalama planı veya faturalama planı satırına iskonto uygular.</li><li>**Temizlendi** - Değişiklik, bir faturalama planına veya faturalama satırına artış uygular.</li></ul><p>Bu onay kutusunun ayarı, faturalanmamış gelir özelliğini kullanan maddeler için değiştirilemez. Ek olarak, gelir bölmeyi kullanan maddelere iskonto uygulanamaz.</p> |
| Başlangıç tarihi | Artış veya iskontonun başlangıç tarihini seçin. |
| Sıklık | Artış veya indirimin sıklığını seçin: **Yok**, **Aylık**, **Üç aylık**, **Altı aylık** veya **Yıllık**. |
| Yüzde | Artış veya iskontonun yüzdesini belirtin. |
| Tutar | Artış veya iskontonun miktarını belirtin. |
| Tüketici fiyat endeksi planı | Hesaplamalar için kullanılan tüketici fiyat endeksi planını seçin. |
| Bitiş tarihi | <p>Artış veya iskontonun bitiş tarihini seçin.</p><p>**Not:** Bu alan, faturalanmamış gelir özelliğini kullanan maddeler için gereklidir.</p> |
| Erteleme planı numarası | <p>Erteleme planı numarası.</p><p>Bu alan yalnızca, sayfa bir faturalama planı satırından açıldığında kullanılabilir.</p> |
| Günlük toplu iş numarası | <p>Günlük toplu iş numarası.</p><p>Bu alan yalnızca, sayfa bir faturalama planı satırından açıldığında kullanılabilir.</p> |
| Toplam iskonto tutarı | <p>Kılavuzdaki tüm satırlar için iskonto tutarlarının toplamı.</p><p>Bu alan yalnızca, sayfa bir faturalama planı satırından açıldığında kullanılabilir.</p> |
| Geçerli kısa dönemli faturalanmamış gelir tutarı | <p>Geçerli kısa dönemli faturalanmamış gelir tutarı.</p><p>Bu tutar, **Yinelenen sözleşme faturalama parametreleri** sayfasında kısa vadeli erteleme yöntemi seçildiğinde ve satır maddesine yönelik hesaplar **Faturalanmamış gelir kurulumu** sayfasında ayarlandığında görüntülenir.</p> |
| Geçerli uzun dönemli faturalanmamış gelir tutarı | <p>Geçerli uzun dönemli faturalanmamış gelir tutarı.</p><p>Bu tutar, **Yinelenen sözleşme faturalama parametreleri** sayfasında kısa vadeli erteleme yöntemi seçildiğinde ve satır maddesine yönelik hesaplar **Faturalanmamış gelir kurulumu** sayfasında ayarlandığında görüntülenir.</p> |

## <a name="proration-examples"></a>Eşit dağıtma örnekleri

Eşit dağıtmayla ilgili hesaplamalar gün sayısını veya ay sayısını temel alabilir. Eşit dağıtma hesaplaması için kullanılan yöntem, **Yinelenen sözleşme faturalama parametreleri** sayfasında ayarlanır. Eşit dağıtma yöntemi, aşağıdaki durumlarda tutarların bir faturalama planı için nasıl hesaplandığını etkiler:

- İlk oluşturma
- Artış veya iskonto uygulaması
- Sonlandırma
- Beklemeye alma veya beklemeyi kaldırma
- Destek veya yenileme eklenmesi

Eşit dağıtma yöntemi aynı zamanda aylık yinelenen gelir (MRR) raporundaki hesaplamaları da etkiler.

### <a name="example-1"></a>Örnek 1

Bir faturalama planının yıllık tutarı 5.000 $'dır. Başlangıç tarihi 12 Ağustos 2019 ve bitiş tarihi 22 Aralık 2019'dur. Faturalama sıklığı yıllıktır. Günlük veya aylık hesaplama yönteminin kullanılmasına bağlı olarak, eşit dağıtılmış tutar aşağıdaki şekilde hesaplanır:

- **Günlük**

    - *Gün sayısı* = *Bitiş tarihi* – *Başlangıç tarihi* + 1 = 133 gün
    - *Yıl içindeki gün sayısı* = 11 Ağustos 2020 – 12 Ağustos 2019 + 1 = 366 gün
    - *Eşit dağıtılmış tutar* = 5.000 &times; (133 &divide; 366) = 1816,94

- **Monthly**

    - *Başlangıç ayı bölümü* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Aradaki aylar* = 3
    - *Bitiş ayı bölümü* = 22 &divide; 31
    - Eşit dağıtılmış tutar = 5.000 &divide; 12 &times; \[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>Örnek 2

Bir faturalama planının yıllık tutarı 12.000 $'dır. Başlangıç tarihi 1 Ağustos 2019 ve bitiş tarihi 31 Aralık 2019'dur. Faturalama sıklığı yıllıktır. Eşit olarak dağıtılmış tutar, hesaplama yöntemine bağlı olarak aşağıdaki şekillerde hesaplanır:

- **Günlük**

    - *Gün sayısı* = *Bitiş tarihi* – *Başlangıç tarihi* + 1 = 153 gün
    - *Yıl içindeki gün sayısı* = 31 Temmuz 2020 – 1 Ağustos 2019 + 1 = 366 gün
    - *Eşit dağıtılmış tutar* = 12.000 &times; (153 &divide; 366) = 5016,39

- **Aylık (Tam ay)**

    - *Ay sayısı* = 5
    - *Toplam ay sayısı* = 12
    - *Eşit dağıtılmış tutar* = (12.000 &times; 5) &divide; 12 = 5.000

## <a name="reversing-a-period-billing"></a>Dönem faturalamasını tersine alma

Bu örnekte, faturalama planında yalnızca bir satır vardır:

- Faturalama aylık olarak Ocak ayından Aralık ayına kadar 12 ay boyunca yapılır.
- Faturalar, Nisan ayı boyunca tüm dönemler için oluşturulmuştur.

Nisan ayı faturalama dönemi için faturayı tersine çevirmek istiyorsunuz.

Nisan ayı faturalama dönemi için henüz bir satış faturası oluşturulmadıysa, satış siparişini silebilirsiniz. Bu durumda, detay için **Faturalandı** durumu kaldırılır. Ancak faturalama dönemi için bir fatura oluşturulduğundan, detay için **Faturalandı** durumu temizlenemez. Bu nedenle, Nisan faturalamasını tersine çevirmek için, satır için bir mahsup alacak dekontu oluşturmanız gerekir.

1. **Tüm faturalama planları** sayfasında aynı madde için bir plan satırı oluşturun.
2. Maddenin **Miktar** değerini orijinal miktarın negatif değeri olarak değiştirin.
3. **Faturalama sıklığı** alanını **Tek seferlik** olarak ayarlayın.
4. Başlangıç ve bitiş tarihlerini, alacak dekontu oluşturmak istediğiniz faturalama ayrıntısı satırı tarihleriyle eşleşecek şekilde güncelleştirin. Bu örnekte, başlangıç tarihini 1 Nisan 2019 ve bitiş tarihini 30 Nisan 2019 olarak ayarlayın.
5. Değişikliklerinizi kaydedin.
6. **Fatura oluştur** sayfasını açın ve belirtilen dönem için alacak dekontuna sahip satış siparişini oluşturun.
7. İsteğe bağlı: Faturayı nakledin.

Faturalama planı için satırları gözden geçirdikten sonra, yeni satırın alacak dekontuna bir bağlantısı olduğunu fark edeceksiniz. Orijinal satır, orijinal Nisan faturasının bağlantısına sahip olmaya devam eder.

## <a name="split-item-group-examples"></a>Madde grubu örneklerini ayırma

Bu örnekte, aşağıdaki ayarlar belirlenir:

- **Yinelenen sözleşme faturalama parametreleri** sayfasında, **Madde grubuna göre ayır** seçilir ve **Benzersiz plan türü** alanı **Müşteri** olarak ayarlanır.
- Üç madde grubu oluşturuldu: **PREFIX**, **DATAHUB** ve **SPP**.
- Müşteri US-001, madde grubunun PREFIX veya DATAHUB olduğu birden çok faturalama planına sahiptir.
- Müşteri US-002, madde grubunun PREFIX veya SPP olduğu birden çok faturalama planına sahiptir.

| Fatura planı numarası | Müşteri | Madde grubu |
|---|---|---|
| SCH001 | US-001 | PREFIX |
| SCH002 | US-001 | DATAHUB |
| SCH003 | US-002 | PREFIX |
| SCH004 | US-002 | SPP |

Müşteri US-001, PREFIX madde grubuna ait bir yenileme maddesi satın alır. Bu hareket yeni bir satış siparişidir.

| Satış siparişi numarası | Müşteri | Ana madde | Yenileme maddesi | Yenileme maddesi grubu | Fatura planı numarası |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | PREFIX | SCH001 |

Satış siparişinin faturası deftere nakledildiğinde, yenileme maddesi müşterinin varolan faturalama planına (SCH001) eklenir. Bu faturalama planı PREFIX madde grubunu kullanır. Aynı madde grubuna ait tüm yenileme maddeleri aynı faturalama planına konur.

**Üst bilgi**
 
| Fatura planı numarası | Müşteri | Madde grubu |
|---|---|---| 
| SCH001 | US-001 | PREFIX |

**Satır**

| Fatura planı numarası | Müşteri | Madde grubu |
|---|---|---|
| SCH001 | US-001 | D0002 |

Müşteri US-001 şimdi SPP madde grubuna ait bir yenileme maddesi satın alır. Bu hareket yeni bir satış siparişidir.

| Satış siparişi numarası | Müşteri | Ana madde | Yenileme maddesi | Yenileme maddesi grubu | Fatura planı numarası |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP | |

Şu anda müşteri US-001, SPP madde grubunu kullanan bir faturalama planına sahip değil. Bu nedenle, yeni bir faturalama planı oluşturulur.

**Üst bilgi**

| Fatura planı numarası| Müşteri | Madde grubu |
|---|---|---|
| SCH005 | US-001 | SPP |

**Satır**

| Fatura planı numarası | Müşteri | Madde grubu |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Aynı son kullanıcı ve müşteri için çoklu faturalama planları

Bu örnekte, aşağıdaki ayarlar belirlenir:

- **Yinelenen sözleşme faturalama parametreleri** sayfasında, **Madde grubuna göre ayır** seçilir ve **Benzersiz plan türü** alanı **Son kullanıcı** olarak ayarlanır.
- **Son kullanıcılar** sayfasında, aşağıdaki müşteri ve son kullanıcı ilişkisi ayarlanmıştır.

    | Müşteri hesabı | Son kullanıcı hesabı |
    |---|---|
    | US-001 | US-221 |

Müşteri ve son kullanıcı kombinasyonu için birden çok faturalama planı oluşturulur. **Yinelenen sözleşme faturalama parametreleri** sayfasında **Madde grubuna göre ayır** seçili olduğundan, aynı müşteri ve son kullanıcı ilişkisi için birden fazla faturalama planı oluşturulabilir.

| Fatura planı numarası | Müşteri | Son kullanıcı hesabı | Madde grubu kodu |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

**Madde kurulumu** sayfasında, destek ve yenileme maddesi ilişkileri oluşturursunuz.

| Madde kodu | Madde ilişkisi | Destek maddesi | Yenileme maddesi | Yenileme maddesi grubu |
|---|---|---|---|---|
| Tablo | D001 | ITEM27 | D007 | IG1 |
| Tablo | D002 | ITEM28 | D005 | IG2 |
| Tablo | D003 | ITEM29 | D006 | IG3 |

Şimdi US-001 müşterisi için bir satış siparişi oluşturursunuz. Bu satış siparişi, **Madde kurulumu** sayfasında maddelere sahiptir. Satış siparişi oluşturduğunuzda, **Destek ve yenileme işlemi** sayfasını açın ve **Son kullanıcı hesabı** alanını ve yenileme öğesi için gerekli tüm diğer bilgileri ayarlayın.

Hareket için fatura oluşturulduğunda ve deftere nakledildiğinde, müşteri/son kullanıcı ve madde grubu kombinasyonu için farklı ödeme planları oluşturulur. Aynı satış siparişindeki birden fazla satır aynı faturalama planına atanabilir.

| Satış siparişi numarası | Müşteri | Son kullanıcı hesabı | Ana madde | Destek maddesi | Yenileme maddesi | Fatura planı numarası |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | ITEM27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | ITEM28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | ITEM29 | D006 | SCH005 |
