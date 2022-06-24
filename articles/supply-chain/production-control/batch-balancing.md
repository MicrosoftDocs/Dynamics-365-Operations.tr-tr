---
title: Toplu iş dengelemesi
description: Bu makale toplu iş dengeleme işlemini açıklar.
author: johanhoffmann
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 50392e8aa0deb568a57e1df59ced70625a4f8a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856062"
---
# <a name="batch-balancing"></a>Toplu iş dengelemesi

[!include [banner](../includes/banner.md)]

Bu makale toplu iş dengeleme işleminin nasıl desteklendiğini açıklar.

Daha fazla bilgi için, [ toplu iş dengelemesine yönelik bir video](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be) izleyin.

Toplu iş dengeleme işleminde, bir ürün toplu işinde kullanılacak bileşenlerin miktarı seçilen ürün toplu işlerindeki etkin bileşenlerin yoğunluğundan hesaplanır.

## <a name="products-that-have-an-active-ingredient"></a>Etkin bileşeni olan ürünler

Bir ürün, etkin bir bileşenin yoğunluğuna göre tanımlanabilir. Bir ürünün etkin bileşeni bir minimum değeri, bir maksimum değeri ve bir hedef düzeyi bulunan ürüne özel toplu iş özniteliği kullanılarak modellenir.

Bir toplu iş özniteliğinin hedef düzeyi, bir üründeki etkin bileşenin tahmini yüzdesini temsil eder. Minimum ve maksimum değerler, hedef düzeyden kabul edilen sapmayı gösterir. Bunlar, örneğin, ürün girişinde toplu işler için kabul edilen tolerans olarak kullanılabilir.

Bir ürünün tek bir etkin bileşeni olabilir. Bir ürünün etkin bileşenini belirtmek için bir ürüne özel toplu iş özniteliği tanımlamalısınız. Daha sonra özniteliği ürünün temel özniteliği olarak ilişkilendirin.

Ürün düzeyinde, ürünün bir toplu işi için etkin bileşen düzeyinin nasıl kaydedileceğini belirtmeniz de gerekir: satınalma girişi işleminin bir parçası olarak veya bir kalite emri işleminin bir parçası olarak.

Bir temel özniteliği ürünle ilişkilendirmek için aşağıdaki kurulumun yapılması gerekir:

- Ürünün toplu iş denetimli olması gerekir. Ürünün toplu işlem denetimli olmasını sağlamak için etkin Toplu iş boyutu olan ürüne bir izleme boyutu grubu atamanız gerekir.

- Bileşen düzeylerini belirten özniteliğin ürün için ürüne özel toplu iş özniteliği olarak tanımlanması gerekir.

Bir toplu iş için etkin bileşenin asıl değerini arama ve düzenleme:
1. **Stok yönetimi \> Sorgular ve raporlar \> İzleme boyutları \> Toplu işler**'e gidin.
1. Izgaradan bir toplu iş numarası seçin.
1. Eylem Bölmesinde, **Görünüm** sekmesini açın ve ardından **Stok toplu iş öznitelikleri**'ni seçin.

## <a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a>Toplu iş dengeleme işleminde bileşen türleri ve etkileşimleri

Oluşturulan bir formül satırı bu bileşen türlerinden birini içerebilir:

- Hiçbiri
- Etkin
- Telafi
- Dolgu

Bu bölümün geri kalanında, her bileşen türünün çalışma şeklini gösteren örnekler verilmektedir. Örnekler toplam toplu iş boyutu 100 litre olan aşağıdaki formüle dayanır.

| Bileşen türü | Madde kodu | Formül satırı miktarı | Birim |
|---|---|---|---|
| Hiçbiri | A | 20 | Litre |
| Active | B: | 30 | Litre |
| Telafi | A | 10 | Litre |
| Dolgu | B | 40 | Litre |

Aşağıdaki tabloda, her bir örneğin sonuçlarına dair genel bir bakış sunulmaktadır.

| Madde kodu | Bileşen türü | Tahmini miktar | Denk miktar | Etkin miktar | Birim | Taban değer |
|---|---|---|---|---|---|---|
| A | Hiçbiri | 20 | 20 | | Litre | |
| M | Etkin | 30 | 25,71 | 9,00 | Litre | 30.00 |
| A | Telafi | 10 | 14.72 | | Litre | |
| B | Dolgu | 40 | 39.57 | | Litre | |

### <a name="active-ingredients"></a>Etkin bileşenler

Temel bir özniteliği olan bir ürün bir formül satırı eklendiğinde, buna formülün *etkin bileşeni* olarak başvurulur. Etkin bileşenleri içeren formüllere sahip toplu iş emirleri toplu iş dengeleme işlemi için kullanılabilir. Formüldeki her bileşen için, toplu iş dengeleme işlemi ürünün üretilmesi için gereken tutarı tahmin eder. Tahmin tutarları seçilen toplu işlerdeki etkin bileşenlerin yoğunluğunu temel alır.

#### <a name="active-ingredient-example"></a>Etkin bileşen örneği

B bileşeninin temel özniteliği X ve hedef düzeyi 30'dur ve her 100 litre ürün 30 litre B bileşeni gerektiren bir formüle dahil edilir. 100 litre bir toplu iş boyutu olan bir toplu iş emri oluşturulur. Toplu iş emri başlatılır ve toplu iş dengeleme işlemi sırasında, kullanıcı 35 kuvvet düzeyine sahip olan bir B bileşeni toplu işi seçer. 35 kuvvet düzeyi hedef düzey olan 30'dan daha büyük olduğu için, B bileşeninin dengelenen miktarı, tahmin edilen miktarla çarpılan kuvvet düzeyinin hedef düzeye oranı kullanarak azaltılır. Dengelenen miktar hesaplaması aşağıdaki gibidir:

(30 ÷ 35) × 30 litre = 25,71 litre

### <a name="none-ingredients"></a>Hiçbir bileşen

**Bileşen türü** *Hiçbiri* olduğunda toplu iş dengelemesi uygularsanız, tahmin edilen miktar ve toplu iş emrinin formül satırındaki dengelenen miktar aynı olur.

#### <a name="none-ingredient-example"></a>Hiçbir bileşen örneği

A bileşeni *Hiçbiri* türünde bir bileşene atanır ve bitmiş ürünü için bir formüle eklenir. Formül her 100 litre bitmiş ürün için 10 litre A bileşeni gerektirir. Bir toplu iş emri 200 litre gerektiğinde, A bileşeni için hem tahmin edilen miktar hem de dengelenen miktar 20 litre olarak hesaplanır.

### <a name="compensating-ingredients"></a>Telafi bileşenleri

Bir telafi bileşeni, üründeki etkin bileşenin etkisini dengeleyebilir veya tamamlayabilir. Bu nedenle, tüketilen telafi bileşeninin miktarı ürünün kuvvetine bağlıdır:

- **Karşıt etkisi** – Etkin bileşen miktarı tahmin edilenden fazlaysa, daha az telafi bileşeni eklemeniz gerekir.

- **Tamamlama etkisi** – Etkin bileşen miktarı tahmin edilenden azsa, daha fazla telafi bileşeni eklemeniz gerekir.

Etkin bileşen ve tamamlayıcı bileşen arasındaki ilişki **Telafi ilkesi** sayfasından ayarlanır.

Bileşenler arasındaki ilişkileri ayarlamak için aşağıdaki adımları izleyin:

1. **Ürün bilgileri yönetimi \> Reçeteler ve malzemeler ve formüller \> Formüller**'i seçin.
1. Formül satırını açın ve ardından **Telafi ilkesi** sayfasını açmak için **Bileşenler**'i seçin.
1. Bir telafi ilkesini temsil eden satırı seçin ve ardından telafi edilecek etkin bileşeni seçin.

Telafi ilkesinde, telafi edilecek miktarı belirtmek ve ilkenin karşıt mı yoksa tamamlayıcı mı olması gerektiğini belirlemek için pozitif veya negatif bir telafi faktörü seçin. Pozitif faktör tamamlayıcı bir etki ve negatif bir faktör karşıt etkiyi belirtir.

#### <a name="compensating-ingredient-example"></a>Telafi bileşeni örneği

B bileşeni temel özniteliği X ve hedef düzeyi 30 olan bir etkin bileşendir. Her 100 litre ürün 30 litre B bileşeni gerektiren formüle eklenir. C bileşeni bir telafi bileşenidir ve aynı formüle 10 miktarında eklenir. Telafi faktörü 1,10 telafi ilkesi için ayarlanır. Bu nedenle, telafi bileşeninin dengelenen miktarı etkin bileşenin dengelenen miktarı ile 1,10'la çarpılan tahmini gerekli miktar arasındaki farka göre azaltılır.

Örnekte, *Etkin* bileşeni türü için, gerekli etkin bileşenin dengelenen miktarı 25,71 olarak ve tahmini gerekli miktar 30 olarak hesaplanmıştır. Bu durumda, telafi bileşeninin dengelenmiş miktarı aşağıdaki gibi hesaplanacaktır:

1. Tahmini ve dengelenmiş miktar arasındaki fark belirlenir:  
    25,71 – 30 = -4,29

1. Sonuç telafi faktörüyle çarpılır:  
    4,29 × 1,10 = –4,72

1. Tahmini telafi miktarı -4,72 azaltılarak dengelenmiş telafi miktarı belirlenir:  
    10 – (–4,72) = 14,72

1,10 pozitif bir telafi faktörü olduğundan, bu telafi ilkesi tamamlayıcı bir etkiye sahiptir. Bu durumda, etkin bileşen beklenenden daha kuvvetlidir. Bu nedenle, daha fazla telafi bileşeni gerekir.

### <a name="filler-ingredients"></a>Dolgu bileşenleri

*Dolgu bileşeni*, bitmiş ürünün istenen çıktı miktarına erişmek için kullanılan nötr bir bileşendir. Dolgu miktarlarındaki ayarlamalar, standart miktara kıyasla etkin bileşendeki ve telafi bileşenindeki değişiklikler temel alınarak hesaplanır.

#### <a name="filler-ingredient-example"></a>Dolgu bileşeni örneği

100 litre formül boyutu için A, B, C ve D bileşenlerini içeren bir ürün formüle ettiniz. Yalnızca tek bir satırda kullanılan *Dolgu* bileşeni türü hariç tüm etkin bileşen türlerinin dengelenmiş miktarını hesapladınız.
Dolgu bileşeninin dengelenmiş miktarı, 100 litrelik toplu iş boyutu ile A,B ve C bileşenlerinin toplamı arasındaki fark olarak hesaplanır.

100 – (20 + 25,71 + 14,72) = 39,57

## <a name="the-batch-balancing-process"></a>Toplu iş dengeleme işlemi

Toplu iş dengeleme işlemi **Toplu iş dengelemesi** sayfasından gerçekleştirilir.
**Maliyet yönetimi \> Toplu iş emirleri**'ni seçin ve ardından **İşlem** sekmesinde **Toplu iş dengelemesi**'ni seçin. Toplu iş dengelemesi **Başlatıldı** durumundaki toplu iş emirleri için kullanılabilir.

Genel olarak, formülde **Bileşen türü**'nün *Etkin* olduğu en az bir formül satırı varsa toplu iş dengelemesi toplu iş emirlerine uygulanabilir. (Bu kuralın özel durumu için, bu makalenin ilerleyen bölümlerindeki "Toplu iş dengelemesi kullanılmayan toplu iş emirleri" bölümüne bakın.)

Toplu iş dengeleme işlemi iki alt işleme bölünebilir:

1. Toplu iş bileşenlerini dengele
1. Formül onaylama ve serbest bırakma

### <a name="balance-batch-ingredients"></a>Toplu iş bileşenlerini dengele

Toplu iş bileşenlerini dengeleme alt işleminde, bir ürün toplu işinde kullanılacak bileşenlerin miktarı etkin bileşenleri bulunan seçili ürün toplu işi temel alınarak hesaplanır. Kural olarak, hesaplama yalnızca tüm bileşenler için tam karşılama olması durumunda tamamlanabilir. Üretim için ayarlanan toplu iş emrinde toplu işin yalnızca bir bölümünü dengeleyemezsiniz.

> [!NOTE]
> Bir hesaplamayı kaydedip toplu iş dengeleme işlemini daha sonra tamamlayamazsınız. **Toplu iş dengeleme** sayfasını kapatırsanız, işlemi tamamlamak için hesaplamayı tekrarlamanız gerekir.

### <a name="confirm-and-release-the-formula"></a>Formül onaylama ve serbest bırakma

Bileşen miktarları hesaplandıktan sonra, formülü onaylayıp serbest bırakabilirsiniz. Serbest bırakma işlemi, ürünlerin ambar yönetim işlemleri için etkin olup olmamasına bağlı olarak farklılık gösterir:

- Bir ürün ambar yönetimi işlemleri için etkinleştirilmişse, formül satırı ambar yönetim işlemleriyle ilgili ilkelere uygun olarak ambara serbest bırakılır. Formül satırı, dengelenen miktarlarla eşleşen miktarlarda serbest bırakılır ve etkin bileşenler için seçilen belirli toplu işler için serbest bırakılır.

    > [!NOTE]
    > Formül satırları yalnızca ambara toplu iş dengeleme işleminin bir bölümü olarak serbest bırakılır. Üretim için malzemeleri ambara serbest bırakmak için başka seçenekler bulunmasına karşın, bu seçenekler formül satırları için kullanılamaz.

- Bir ürün ambar yönetim işlemleri için etkinleştirilmemişse, ürün için formülü onaylayıp serbest bıraktığınızda bir üretim malzeme çekme listesi oluşturulur.

Tek bir formülde, ambar yönetimi işlemleri için etkin olan ürünler ile ambar yönetimi işlemleri için etkin olmayan ürünleri birleştirebilirsiniz. Bir formüle iki tür ürün dahil olduğunda, ambar yönetimi işlemleri için etkin olan ürünler ambara serbest bırakılır. Ambar yönetim işlemleri için etkinleştirilmemiş ürünler için, formülü onaylayıp serbest bıraktığınızda bir malzeme çekme listesi oluşturulur.

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a>Toplu iş dengelemesi kullanılmayan toplu iş emirleri

Formülde **Bileşen türü**'nün *Etkin* olduğu en az bir formül satırı bulunması durumunda toplu iş emirlerinin toplu iş dengelemesi için kullanılmasına yönelik kuralın iki istisnası bulunur.

1. Formül ambar yönetim işlemleri için etkinleştirilmiş bir ürün için etkin bileşen içeriyor ancak toplu iş numarası rezervasyon hiyerarşisinde yerleşimin altında yer alıyorsa, toplu iş dengelemesi toplu iş emri için kullanılamaz.
1. Formül ölçü birimi etkin bileşenin ölçü biriminden farklıysa toplu iş emri toplu iş dengelemesi için geçerli olmaz.

Toplu iş dengelemesi kullanılamayan bir toplu iş emri toplu iş emirlerine yönelik normal süreçten geçer.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]