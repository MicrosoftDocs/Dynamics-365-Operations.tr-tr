---
title: "Stok miktarlarını rezerve etme"
description: "Bu konu stok rezervasyonunda kullanılabilen farklı seçenekleri açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 7361b2e04376284238c8c9b1f91d03d18b121d24
ms.lasthandoff: 03/31/2017


---

# <a name="reserve-inventory-quantities"></a>Stok miktarlarını rezerve etme

[!include[banner](../includes/banner.md)]


Bu konu stok rezervasyonunda kullanılabilen farklı seçenekleri açıklar.

Belirli bir satış siparişi için otomatik olarak stok miktarları rezerve edebilirsiniz. Böylece, stok rezervasyonu veya stok rezervasyonunun bir kısmı iptal edilmedikçe, rezerve edilen stok diğer siparişler için ambardan çekilemez.

Stok rezerve etmenin birkaç nedeni vardır:
-   İlk sipariş edilen ilk önce teslim edilir; böylece, müşteriler kullanılabilir maddeleri siparişi verme sıralarına göre alabilir.
-   Satıcının uzun süreli veya bilinmeyen bir teslimat zamanı nedeniyle maddede eksilme. Belirli müşteri veya siparişlere kullanılabilir ilk maddelere ait teslimat sağlamanız gerekebilir.
-   Belirli müşteri ve belirli sipariş tipleri teslimatta öncelik sahibidir.
-   Seri veya toplu iş numarası olan maddeler. Belirli siparişlere teslim edilmiş veya edilecek belirli maddelere işaret koyabilirsiniz.
-   Belirli siparişler için rezerve edilmiş özel olarak sipariş edilen maddeler.
-   Üretim siparişleri. Örneğin, belirli siparişleri için üretilen veya bunlara göre ayarlanan maddeleri işaretleyebilirsiniz.

Yeni sipariş satırı oluşturulduğunda stok otomatik olarak, stok da her sipariş için tek tek el ile rezerve edilebilir. toğu üretim sürecinin farklı aşamalarında rezerve etmek de mümkündür. Yalnızca stoğu tutulan ürünler rezerve edilebilir. Eldeki stok olmadığından hizmetler rezerve edilemez. Hem fiziksel olarak eldeki stok hem de sipariş verilmiş, ancak alınmamış stok rezerve edilebilir. Eldeki stokta bulunandan daha fazla miktar rezerve edilirse bu kadar büyük bir miktarı rezerve edemeyeceğinizi belirten bir ileti görüntülenir. Bu durumda miktarı yine de rezerve etmeyi seçebilir veya sipariş verilen miktarı değiştirebilirsiniz. Miktar ya rezerve edilir ya da değiştirilir. Kullanılabilen miktardan daha fazla madde rezerve edilirse, maddelerin bir sonraki teslimata hazır oluşunda bu eksiklik kapatılır.

## <a name="inventory-reservation-policies"></a>Stok rezervasyonu ilkeleri
Stok rezervasyonu ilkeleri **Madde model grupları **sayfasında, **Stok ve ambar yönetim parametreleri** sayfasında ve **Üretim parametreleri** sayfasında ayarlanır.
### <a name="policies-on-the-item-model-groups-page"></a>Madde model grupları sayfasındaki ilkeler

**Stok ilkeleri** bölümü aşağıdaki rezervasyon ilkelerini içerir.
|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Rezervasyon ilkesi**  | **Açıklama**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| FIFO tarihi denetimli    | **FIFO tarihi denetimli** seçeneğini belirlerseniz stok rezervasyonu FIFO ilkesine göre bir sıralama tarihi ile denetlenir. İlk giren ilk çıkar (FIFO) ilkesine göre, toplu işler maddenin en erken giriş tarihine göre rezerve edilir.                                                                                                                                                                                                                                                                       |
| Sevk tarihinden geriye doğru | Bu seçenek yalnızca **FIFO tarihi denetimli** seçeneğini belirlediğinizde kullanılabilir. **Sevk tarihinden geriye doğru** seçeneğini belirlerseniz stok son giren ilk çıkar (LIFO) ilkesine göre, istenen sevk tarihinden geriye doğru rezerve edilir. Sevk tarihinden önce bir giriş yoksa bir FIFO rezervasyonu kullanılır.                                                                                                                                                                                                           |
| Madde satış rezervasyonu  | Madde rezervasyonunun el ile veya otomatik olduğunu belirler. Rezervasyon otomatikse stok, sipariş satırları oluşturulduğunda rezerve edilir. Rezervasyonları ürün reçeteleri için madde numarası düzeyinde (**Otomatik** seçeneği) veya bir ürün reçetesinin ayrı ayrı öğeleri için (**Açılım** seçeneği) yapmak mümkündür. **Madde satış rezervasyonu** için varsayılan değer **Alacak hesapları parametrelerinden** devralınabilir. Bu sayfada, değer **Genel** sekmesindeki **Varsayılan satış değerleri** **bölümünde**  ayarlanabilir. |
| Aynı toplu iş seçimi    | Aynı toplu iş rezervasyonu, tek bir stok toplu işine karşılık bir satış siparişi satırı için stok rezerve etmenizi sağlar. Bu seçeneği kullanmak isterseniz **Gereksinimi konsolide et** seçeneğini de **Evet** olarak ayarlamanız gerekir. İzleme boyutu grubu ve depolama boyutu grubu için gerekli olan ek ayarlar bulunmaktadır. Daha fazla bilgi için bkz. [Satış siparişi için aynı toplu işi rezerve etme](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Gereksinimi konsolide et | Bu seçenek **Aynı toplu iş seçimi** seçeneğine benzer ve satış siparişi satırları için rezerve edilen stoğu tek bir gereksinimde birleştirir.                                                                                                                                                                                                                                                                                                                                                                                      |
| FEFO tarih denetimli    | Bu seçenek, bitiş tarihi veya son kullanma tarihi yaklaşan toplu işleri rezerve etmenize olanak tanır. Ayrıca, **Bitiş tarihi** veya **Son kullanma tarihi** seçimi yapmak için **Çekme ölçütü** alanını da ayarlamanız gerekir.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>FIFO tarihi denetimli ve Sevk tarihinden geriye doğru örneği

Bu örnekte, madde numarası A için eldeki stok üç farklı toplu iş numarası için mevcuttur.
| Madde kodu | Parti numarası | Miktar | Tarih             |
|-------------|--------------|----------|------------------|
| A:           | 1000         | 5        | 2 Şubat 2016 |
| A:           | 1001         | 3        | 1 Ocak 2016  |
| A:           | 1002         | 7        | 3 Mart 2016    |

Otomatik olarak rezerve edilmesi gereken ve 4 Nisan 2016 tarihinde teslim edilen bir satış siparişi aşağıdaki toplu işi rezerve eder:
-   **FIFO tarihi denetimli** ve **Sevk tarihinden geriye doğru** onay kutularının işareti kaldırılırsa en küçük numaraya sahip toplu iş olduğu için 1000 toplu işi rezerve edilir.
-   **FIFO tarihi denetimli** onay kutusu seçilir ve **Sevk tarihinden geriye doğru** onay kutusunun işareti kaldırılırsa ilk giriş tarihine (FIFO) sahip olduğu için 1001 toplu işi rezerve edilir.
-   **FIFO tarihi denetimli** ve **Sevk tarihinden geriye doğru** onay kutuları işaretlenirse satış siparişi sevk tarihine en yakın toplu iş girişi olduğu için 1002 toplu işi rezerve edilir.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Stok ve ambar yönetimi parametresi sayfasındaki ilkeler

**Stok ve ambar yönetim parametreleri** sayfasındaki rezervasyonlarla ilgili iki seçenek bulunmaktadır:
-   **General** sekmesindeki **Sipariş edilen maddeleri rezerve et** seçeneği Alacak hesapları, Proje yönetimi ve muhasebe ile Üretim denetimi içindeki madde çıkışlarına karşı sipariş edilen madde girişlerini rezerve etmenize olanak tanır. Bu seçimi kaldırdığınızda yalnızca fiziksel olarak girişi yapılan maddeleri rezerve edebilirsiniz. Belirli bir madde negatif stoku kabul edecek şekilde ayarlandığında, bu alan ilgisizdir.
-   **Taşıma** sekmesindeki **Maddeleri otomatik olarak ayır** seçeneği, maddeler transfer emirleri için otomatik olarak rezerve edilmişse varsayılan ayarı belirler. Varsayılan ayar tek tek transfer emirlerinden geçersiz kılınabilir.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Üretim parametreleri sayfasındaki stok rezervasyonu ilkeleri

**Üretim parametreleri** sayfasında bulunan **Genel** sekmesindeki **Rezervasyon** alanının değeri üretim sürecinde stoğun rezerve edilmesi gereken varsayılan noktayı belirler. Örneğin, stok iş zamanlanırken veya iş başlatıldığında rezerve edilebilir.




