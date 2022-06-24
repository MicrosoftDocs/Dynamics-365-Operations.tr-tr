---
title: Maliyet hareketi varlıkları
description: Bu makale, paylaştırma yönteminin seçilmesi aracılığıyla maliyet değerinin maliyet alanı içerikleri arasında bölünmesine olanak tanıyan maliyet hareketi varlıkları hakkında bilgi sağlar.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 3aabc1356eba27de797fa696dd928cb401d8501b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860826"
---
# <a name="cost-transaction-entities"></a>Maliyet hareketi varlıkları

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

## <a name="apportionment"></a>Paylaştırma

Son teslim alma maliyeti, paylaştırma yönteminin seçilmesi aracılığıyla maliyet değerinin maliyet alanı içerikleri (seyahat, sevkiyat konteyneri vb.) bölünmesine olanak tanır. Paylaştırma yöntemi, iş kurallarına dayalı otomatik maliyetlerin yapılandırmasının bir parçası olarak ayarlanmıştır. Seyahat satırı oluşturulurken maliyetin bir parçası olarak çekilir.

### <a name="configure-the-apportionment-mapping-for-use-with-data-entities"></a>Veri varlıklarıyla kullanmak üzere paylaştırma eşlemesini yapılandırma

Nakliye aracısı gibi harici bir kaynaktan maliyet oluşturulduğunda, söz konusu harici kaynak maliyet değerini paylaştırmak için tercih edilen yöntemi belirtemez. Paylaştırma eşlemesi, her maliyet türü kodu için varsayılan paylaştırma yöntemini tanımlar. Paylaştırma eşlemesi tablosuna Microsoft Dynamics 365 Supply Chain Management'taki **Paylaştırma eşlemesi** sayfasından ulaşılır (**Son Teslim Alma Maliyeti \> Maliyetlendirme kurulumu \> Paylaştırma eşlemesi**).

Bir eşleme birleşimi tanımlanmışsa ve maliyet hareketi varlığı kullanılarak maliyet türü koduyla eşleşen bir maliyet oluşturulmuşsa, varlığa sağlanan herhangi bir değer yerine eşlenen paylaştırma yöntemi kullanılır.

Eşleme tablosunda herhangi bir değer yoksa, ancak varlığa bir değer sağlanmışsa, sağlanan değer kullanılır.

Eşleme tablosunda veya varlığa gönderilen kayıtta herhangi bir değer yoksa, oluşturma işlemi başarısız olur.

### <a name="apportionment-mapping-itmapportionmentmapping"></a>Paylaştırma yöntemi (ITMApportionmentMapping)

Paylaştırma eşlemesi varlığı (`ITMApportionmentMapping`), paylaştırma eşlemesi ilişkileri oluşturur ve kullanıcıların kayıt oluşturmasına veya güncelleştirmesine olanak tanır.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Paylaştırma yöntemi | ITMApportionmentMapping.ApportionmentMethod | Int | No. | No. |
| Maliyet türü kodu | ITMApportionmentMapping.ShipCostTypeId | Nvarchar(20) | **Evet** | No. |

## <a name="voyage-costs-itmcosttransvoyageentity"></a>Seyahat maliyetleri (ITMCostTransVoyageEntity)

Seyahat maliyeti varlığı (`ITMCostTransVoyageEntity`), seyahat düzeyinde uygulanan seyahat maliyeti hareketleri oluşturur. İçeri aktarma işlemi sırasında sistem, maliyet değerinin seyahat içerikleri arasında nasıl paylaştırılacağını belirlemek için varlığa eklenen **Kategori** ve **Paylaştırma yöntemi** değerlerini kullanır.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Paylaştırma yöntemi | ITMCostTrans.ApportionmentMethod | Int | No. | No. |
| Maliyet değeri | ITMCostTrans.CostValue | Numeric(32, 6) | No. | No. |
| Para birimi | ITMCostTrans.CurrencyCode | Nvarchar(3) | No. | **Evet** |
| Satır numarası | ITMCostTrans.LineNum | Numeric(32, 16) | **Evet** | No. |
| Bağlı maliyet türü | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | No. | No. |
| Minimum maliyet | ITMCostTrans.MinCostAmount | Numeric(32, 6) | No. | No. |
| Kategori | ITMCostTrans.ShipCostCategory | Int | No. | No. |
| Maliyet türü kodu | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | No. | No. |
| Şirket | ITMCostTrans.ShipDataArea | Nvarchar(4) | No. | **Evet** |
| Seyahat | ITMCostTrans.TransRecId | Nvarchar(20) | **Evet** | No. |
| Madde satış vergisi grubu | ITMCostTrans.TaxItemGroup | Nvarchar(10) | No. | No. |

## <a name="shipping-container-costs-itmcosttransshippingcontainerentity"></a>Sevkiyat konteyneri maliyetleri (ITMCostTransShippingContainerEntity)

Sevkiyat konteyneri maliyeti varlığı (`ITMCostTransShippingContainerEntity`), sevkiyat konteyneri düzeyinde uygulanan sevkiyat konteyneri maliyetleri oluşturur. İçeri aktarma işlemi sırasında sistem, maliyet değerinin sevkiyat konteyneri içerikleri arasında nasıl paylaştırılacağını belirlemek için varlığa eklenen **Kategori** ve **Paylaştırma yöntemi** değerlerini kullanır.

**Toplam**, **Durak** ve **Bağlı durak** alanları, **Maliyet alanı** değerinin *Sevkiyat konteyneri* olduğu kayıtlara özeldir. Bu nedenle, diğer maliyet alanlarının veri varlıklarında mevcut değildir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Topla | ITMCostTrans.AggregatedCost | Int | No. | No. |
| Paylaştırma yöntemi | ITMCostTrans.ApportionmentMethod | Int | No. | No. |
| Maliyet değeri | ITMCostTrans.CostValue | Numeric(32, 6) | No. | No. |
| Para birimi | ITMCostTrans.CurrencyCode | Nvarchar(3) | No. | **Evet** |
| Satır numarası | ITMCostTrans.LineNum | Numeric(32, 16) | **Evet** | No. |
| Bağlı maliyet türü | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | No. | No. |
| Bağlı durak | ITMCostTrans.LinkLegId | Nvarchar(20) | No. | No. |
| Minimum maliyet | ITMCostTrans.MinCostAmount | Numeric(32, 6) | No. | No. |
| Sevkiyat Konteyneri | ITMCostTrans.TransRecId | Nvarchar(20) | **Evet** | No. |
| Kategori | ITMCostTrans.ShipCostCategory | Int | No. | No. |
| Maliyet türü kodu | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | No. | No. |
| Şirket | ITMCostTrans.ShipDataArea | Nvarchar(4) | No. | **Evet** |
| Seyahat | ITMCostTrans.TransRecId | Nvarchar(20) | **Evet** | No. |
| Durak | ITMCostTrans.ShipLegId | Nvarchar(20) | No. | No. |
| Madde satış vergisi grubu | ITMCostTrans.TaxItemGroup | Nvarchar(10) | No. | No. |

## <a name="folio-costs-itmcosttransfolioentity"></a>Folyo maliyetleri (ITMCostTransFolioEntity)

Folyo maliyeti varlığı (`ITMCostTransFolioEntity`), folyo düzeyinde uygulanan maliyet hareketi kayıtları oluşturur. İçeri aktarma işlemi sırasında sistem, maliyet değerinin her bir folyo içeriği arasında nasıl paylaştırılacağını belirlemek için varlığa eklenen **Kategori** ve **Paylaştırma yöntemi** değerlerini kullanır.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Paylaştırma yöntemi | ITMCostTrans.ApportionmentMethod | Int | No. | No. |
| Maliyet değeri | ITMCostTrans.CostValue | Numeric(32, 6) | No. | No. |
| Para birimi | ITMCostTrans.CurrencyCode | Nvarchar(3) | No. | **Evet** |
| Satır numarası | ITMCostTrans.LineNum | Numeric(32, 16) | **Evet** | No. |
| Bağlı maliyet türü | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | No. | No. |
| Minimum maliyet | ITMCostTrans.MinCostAmount | Numeric(32, 6) | No. | No. |
| Kategori | ITMCostTrans.ShipCostCategory | Int | No. | No. |
| Maliyet türü kodu | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | No. | No. |
| Şirket | ITMCostTrans.ShipDataArea | Nvarchar(4) | No. | **Evet** |
| Folyo | ITMCostTrans.TransRecId | Nvarchar(20) | **Evet** | No. |
| Madde satış vergisi grubu | ITMCostTrans.TaxItemGroup | Nvarchar(10) | No. | No. |

## <a name="purchase-order-costs-itmcosttranspurchaseentity"></a>Satınalma siparişi maliyetleri (ITMCostTransPurchaseEntity)

Satınalma siparişi maliyeti varlığı (`ITMCostTransPurchaseEntity`), satın almacı emri üst bilgisinde uygulanan maliyet hareketleri oluşturur. İçeri aktarma işlemi sırasında sistem, maliyet değerinin her bir folyo içeriği arasında nasıl paylaştırılacağını belirlemek için varlığa eklenen **Kategori** ve **Paylaştırma yöntemi** değerlerini kullanır.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Paylaştırma yöntemi | ITMCostTrans.ApportionmentMethod | Int | No. | No. |
| Maliyet değeri | ITMCostTrans.CostValue | Numeric(32, 6) | No. | No. |
| Para birimi | ITMCostTrans.CurrencyCode | Nvarchar(3) | No. | **Evet** |
| Satır numarası | ITMCostTrans.LineNum | Numeric(32, 16) | **Evet** | No. |
| Bağlı maliyet türü | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | No. | No. |
| Minimum maliyet | ITMCostTrans.MinCostAmount | Numeric(32, 6) | No. | No. |
| Satın alma siparişi | ITMCostTrans.TransRecId | Nvarchar(20) | **Evet** | No. |
| Kategori | ITMCostTrans.ShipCostCategory | Int | No. | No. |
| Maliyet türü kodu | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | No. | No. |
| Şirket | ITMCostTrans.ShipDataArea | Nvarchar(4) | No. | **Evet** |
| Madde satış vergisi grubu | ITMCostTrans.TaxItemGroup | Nvarchar(10) | No. | No. |

## <a name="item-costs-itmcosttransitementity"></a>Madde maliyetleri (ITMCostTransItemEntity)

Madde maliyeti varlığı (`ITMCostTransItemEntity`), madde düzeyinde uygulanan maliyet hareketlerini oluşturur. Bu varlık, satınalma siparişi satırlarındaki maddelere özgüdür. Maliyet değeri satıra tam olarak uygulanır.

**Düzeltme tutarı** ve **Değer düzeltme** alanları satır düzeyi maliyet alanlarına özgüdür. Bu nedenle, diğer maliyet alanlarının veri varlıklarında mevcut değildir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Ayarlama tutarı | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | No. | No. |
| Maliyet değeri | ITMCostTrans.CostValue | Numeric(32, 6) | No. | No. |
| Para birimi | ITMCostTrans.CurrencyCode | Nvarchar(3) | No. | **Evet** |
| Satır numarası | ITMCostTrans.LineNum | Numeric(32, 16) | **Evet** | No. |
| Bağlı maliyet türü | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | No. | No. |
| Minimum maliyet | ITMCostTrans.MinCostAmount | Numeric(32, 6) | No. | No. |
| Satın alma siparişi | ITMCostTrans.TransRecId | Nvarchar(20) | **Evet** | No. |
| Satınalma siparişi satır numarası | ITMCostTrans.TransRecId | Nvarchar(20) | **Evet** | No. |
| Kategori | ITMCostTrans.ShipCostCategory | Int | No. | No. |
| Maliyet türü kodu | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | No. | No. |
| Şirket | ITMCostTrans.ShipDataArea | Nvarchar(4) | No. | **Evet** |
| Madde satış vergisi grubu | ITMCostTrans.TaxItemGroup | Nvarchar(10) | No. | No. |
| Değer düzeltme | ITMCostTrans.ValueAdjustmentMethod | Int | No. | No. |

## <a name="transfer-line-costs-itmcosttranstransferlineentity"></a>Transfer satırı maliyetleri (ITMCostTransTransferLineEntity)

Transfer satırı maliyeti varlığı (`ITMCostTransTransferLineEntity`), transfer emri satır düzeyine uygulanan maliyet hareketleri oluşturur. Bu maliyetlerin değeri, transfer emri satırına tam olarak uygulanır.

**Düzeltme tutarı** ve **Değer düzeltme** alanları satır düzeyi maliyet alanlarına özgüdür. Bu nedenle, diğer maliyet alanlarının veri varlıklarında mevcut değildir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Ayarlama tutarı | ITMCostTrans.AdjustmentAmount | Numeric(32, 6) | No. | No. |
| Maliyet değeri | ITMCostTrans.CostValue | Numeric(32, 6) | No. | No. |
| Para birimi | ITMCostTrans.CurrencyCode | Nvarchar(3) | No. | **Evet** |
| Satır numarası | ITMCostTrans.LineNum | Numeric(32, 16) | **Evet** | No. |
| Bağlı maliyet türü | ITMCostTrans.LinkCostTypeId | Nvarchar(20) | No. | No. |
| Minimum maliyet | ITMCostTrans.MinCostAmount | Numeric(32, 6) | No. | No. |
| Kategori | ITMCostTrans.ShipCostCategory | Int | No. | No. |
| Maliyet türü kodu | ITMCostTrans.ShipCostTypeId | Nvarchar(20) | No. | No. |
| Şirket | ITMCostTrans.ShipDataArea | Nvarchar(4) | No. | **Evet** |
| Transfer emri | ITMCostTrans.TransRecId | Nvarchar(20) | **Evet** | No. |
| Transfer emri satır numarası | ITMCostTrans.TransRecId | Nvarchar(20) | **Evet** | No. |
| Madde satış vergisi grubu | ITMCostTrans.TaxItemGroup | Nvarchar(10) | No. | No. |
| Değer düzeltme | ITMCostTrans.ValueAdjustmentMethod | Int | No. | No. |

### <a name="transaction-table"></a>Hareket tablosu

Maliyet hareketi kaydı, bir hareket tablosu numarasının (`TransTableId`) atanması yoluyla maliyet alanıyla ilişkilendirilir. Belirli tablo tanımlayıcısı numaraları gerektiğinde, varlıklar bu değerlere göre bölünür; böylece her maliyet alanı için bir varlık bulunur.

Hareket tablosu (`TransTableId`), maliyet hareketi varlığının seçiminde örtüktür.

### <a name="calculated-fields"></a>Hesaplanan alanlar

Bir maliyet hareketi varlığı kullanıldığında aşağıdaki alanlar, yalnızca seyahat kaydında belirli eylemler tamamlandığında ayarlandığı için ekleme veya güncelleştirme için kullanılamaz:

- **Tahmini maliyet**: Bu alan, seyahat için bir fatura deftere nakledildiğinde (satınalma siparişi) veya bir transfer alındığında ayarlanır.
- **Tahmini maliyet para birimi**: Bu alan, seyahat için bir fatura deftere nakledildiğinde (satınalma siparişi) veya bir transfer alındığında ayarlanır.
- **Fiili maliyet**: Bu alan, satıcı faturası deftere nakledildiğinde ayarlanır. Maliyetle ilişkilidir.

### <a name="find-auto-costs"></a>Otomatik maliyetleri bul

Her maliyet alanı (seyahat, sevkiyat konteyneri vb.) için kullanılabilen bir **Otomatik maliyetleri bul** düğmesi, yapılandırma tablolarındaki bilgiler kullanılarak söz konusu maliyet alanı için maliyet hareketlerinin güncelleştirilmesini sağlayan bir yöntem sunar. Maliyet alanının düğmesini seçtiğinizde sistem, söz konusu maliyet alanı için mevcut maliyetleri temizler ve otomatik maliyet kurulumu tablolarının geçerli yapılandırmasına göre yeni kayıtlar oluşturur.

Veri varlığı kullanılarak oluşturulan maliyet hareketi kayıtları içeri aktarılmış olarak işaretlenir. Bu kayıtlar, otomatik maliyet kurulumu tabloları kullanılarak yeniden oluşturulmadığından **Otomatik maliyetleri bul** seçeneğini belirlediğinizde silinmez. Ancak içeri aktarılmış olarak işaretlenen bir maliyet hareketi kaydı yine de silinebilir.

### <a name="linked-fields"></a>Bağlı alanlar

Her maliyet hareketi, aynı maliyet alanındaki başka bir kayıtla ilişkilendirilebilir. Bu ilişki, **Bağlı maliyet türü** alanı aracılığıyla kurulur. Maliyet değerinin başka bir maliyetin yüzdesi olarak hesaplanmasını sağlar.

**Bağlı maliyet türü** alanı, yalnızca başvurulan kayıt önce işlendiyse veya tabloda zaten varsa doğrulanabilir. Aynı şart, yalnızca sevkiyat konteyneri maliyeti alanındaki maliyetler için kullanılan **Bağlı durak** alanı için geçerlidir.
