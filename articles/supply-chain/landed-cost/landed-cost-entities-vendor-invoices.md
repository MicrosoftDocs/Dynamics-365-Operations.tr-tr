---
title: Satıcı faturası varlıkları
description: Bu makale, dahili maliyetler veya harici olarak türetilmiş maliyetler için maliyet türü kodlarının yapılandırılmasına olanak tanıyan satıcı faturası varlıkları hakkında bilgi sağlar.
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
ms.openlocfilehash: 171b383e1549babd76fd18e4932436a66aa62cc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873941"
---
# <a name="vendor-invoice-entities"></a>Satıcı faturası varlıkları

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

**Son teslim alma maliyeti** modülü, maliyet türü kodlarının dahili maliyetler veya harici olarak türetilmiş maliyetler için yapılandırılmasını sağlar. Maliyet işletme açısından hariciyse hizmet sağlayıcısından bir fatura beklenir. Bu fatura, bir seyahat ile ilişkilendirilebilecek bir fatura günlüğü olarak işlenir ve faturanın değeri, bir veya daha fazla seyahat maliyeti arasında dağıtılabilir.

Satıcı faturası varlıkları, bir günlük satırı değerinin aynı maliyet türü koduna sahip olan bir veya daha fazla seyahat maliyeti arasında tahsis edilmesine olanak tanır.

Maliyet yalnızca fatura günlük üst bilgisi ve fatura günlüğü satırları varsa tahsis edilebilir.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Satıcı seyahat maliyeti tahsisatları (ITMLedgerJournalCostLinesVoyagesEntity)

Satıcı seyahat maliyeti tahsisatları veri varlığı, satıcı faturası satırının seyahat maliyeti alanına uygulanan bir veya daha fazla maliyet arasında tahsis edilmesini sağlar. Bu işlev, `ITMLedgerJournalCostLinesVoyagesEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Dağıtılan tutar | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | No. | No. |
| Maliyet hareketi satır numarası | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük satırı numarası | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük numarası | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Evet** | No. |
| Seyahat | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Evet** | No. |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Satıcı sevkiyat konteyneri maliyet tahsisatları (ITMLedgerJournalCostLinesContainersEntity)

Satıcı sevkiyat konteyneri maliyet tahsisatları veri varlığı, satıcı faturası satırının sevkiyat konteyneri maliyeti alanına uygulanan bir veya daha fazla maliyet arasında tahsis edilmesini sağlar. Bu işlev, `ITMLedgerJournalCostLinesContainersEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Dağıtılan tutar | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | No. | No. |
| Sevkiyat konteyneri | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Evet** | No. |
| Maliyet hareketi satır numarası | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük satırı numarası | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük numarası | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Evet** | No. |
| Seyahat | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Evet** | No. |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Satıcı folyo maliyeti tahsisatları (ITMLedgerJournalCostLinesFoliosEntity)

Satıcı folyo maliyeti tahsisatları veri varlığı, satıcı faturası satırının folyo maliyeti alanına uygulanan bir veya daha fazla maliyet arasında tahsis edilmesini sağlar. Bu işlev, `ITMLedgerJournalCostLinesFoliosEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Dağıtılan tutar | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | No. | No. |
| Maliyet hareketi satır numarası | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Evet** | No. |
| Folyo | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Evet** | No. |
| Günlük satırı numarası | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük numarası | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Evet** | No. |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Satıcı satınalma siparişi maliyeti tahsisatları (ITMLedgerJournalCostLinesPurchTableEntity)

Satıcı satınalma siparişi maliyet tahsisatları veri varlığı, satıcı faturası satırının satınalma siparişi maliyeti alanına uygulanan bir veya daha fazla maliyet arasında tahsis edilmesini sağlar. Bu işlev, `ITMLedgerJournalCostLinesPurchTableEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Dağıtılan tutar | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | No. | No. |
| Maliyet hareketi satır numarası | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük satırı numarası | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük numarası | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Evet** | No. |
| Satın alma siparişi | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Evet** | No. |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Satıcı madde maliyeti tahsisatları (ITMLedgerJournalCostLinesPurchLineEntity)

Satıcı madde maliyeti tahsisatları veri varlığı, satıcı faturası satırının madde maliyeti alanına uygulanan bir veya daha fazla maliyet arasında tahsis edilmesini sağlar. Madde maliyeti alanı, satınalma siparişi satırındaki maliyetleri kapsar. Bu işlev, `ITMLedgerJournalCostLinesPurchLineEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Dağıtılan tutar | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | No. | No. |
| Maliyet hareketi satır numarası | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük satırı numarası | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük numarası | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Evet** | No. |
| Satın alma siparişi | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Evet** | No. |
| Satınalma siparişi satır numarası | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Evet** | No. |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Satıcı transfer emri satırı maliyeti tahsisatları (ITMLedgerJournalCostLinesTransferLineEntity)

Satıcı transfer emri satırı maliyeti tahsisatları veri varlığı, satıcı faturası satırının transfer satırı maliyeti alanına uygulanan bir veya daha fazla maliyet arasında tahsis edilmesini sağlar. Bu işlev, `ITMLedgerJournalCostLinesTransferLineEntity` varlığı tarafından desteklenir. Aşağıdaki tabloda, bu varlığı oluşturan alanlar ve eşlemeler listelenmektedir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Dağıtılan tutar | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | No. | No. |
| Maliyet hareketi satır numarası | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük satırı numarası | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Evet** | No. |
| Günlük numarası | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Evet** | No. |
| Transfer emri | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Evet** | No. |
| Transfer emri satır numarası | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Evet** | No. |

### <a name="reference-table"></a>Referans tablosu

Seyahat maliyeti satırları, maliyet hareketi kaydıyla doğrudan ilişkilidir. Bu kayıt, **Referans tablosu kodu** değerini içeriyor. Bu değer her maliyet alanı için benzersizdir (seyahat, sevkiyat konteyneri, vb.). Veri varlıkları kullanılarak oluşturulan veriler için belirli tablo numaralarına başvurulduğunda, varlıklar **Referans tablosu kodu** değerlerine göre bölünür.

Referans tablosu (`RefTableId`) ve hareket türü (`TransType`) değerleri, Son teslim alma maliyeti satınalma satırı veya Son teslim alma maliyeti transfer satırı varlığı seçiminde örtüktür.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Satıcı faturası günlüğü satırları (VendorInvoiceJournalLineEntity)

Günlük satırı değeri, **Son teslim alma maliyeti** modülünde bir veya daha fazla maliyete tahsis edilmeden önce günlük satırı maliyet alanıyla ilişkilendirilmelidir. Bu işlevi desteklemek için **Son teslim alma maliyeti** modülü günlük satırları tablosuna bazı yeni alanlar ekler (`LedgerJournalTrans`).

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Satıcı faturası günlüğü satırı varlığına eklenen alanlar

Aşağıdaki tabloda, **Son teslim alma maliyeti** modülünün satıcı faturası günlüğü satırı varlığına (`VendorInvoiceJournalLineEntity`) eklediği alanlar listelenir. Bu alanlar, sistemin günlük satırları oluşturmasına ve bunlara göre maliyet tahsis etmesine olanak tanır.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Maliyet alanı | LedgerJournalTrans.ITMCostArea | Int | No. | No. |
| Maliyet türü kodu | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | No. | No. |

### <a name="mainoffset-account"></a>Ana/mahsup hesap

Son teslim alma maliyeti seyahatiyle ilişkili fatura günlüğü satırı için ana/mahsup hesap maliyet türü kodu tarafından belirlenir. Maliyet türü kodu fatura günlüğü satırına dahil edildiğinde, senaryoya göre kodun kliring hesabı olarak ana hesap veya mahsup hesap kullanılır:

- **Tek satırlı günlük**: Bir ana hesap (başka bir deyişle satıcı hesabı) tanımlanmışsa ve maliyet türü kodu sağlanmışsa, söz konusu maliyet türü kodu için kliring hesabı değeri mahsup hesaba girilir.
- **Çok satırlı günlük**: Bir ana hesap tanımlanmamış ancak maliyet türü kodu sağlanmışsa, söz konusu maliyet türü kodu için kliring hesabı değeri ana hesaba girilir. Satıcıyı alacaklandıran günlük satırı maliyet türü koduna başvurmaz.

## <a name="sequencing"></a>Sıralama

Günlük ve günlük satırları tabloları arasındaki bağımlılıklar nedeniyle, önce seyahat kaydı oluşturulmalıdır. Seyahat satırları yalnızca seyahat, sevkiyat konteyneri ve folyolar oluşturulduktan sonra oluşturulabilir.

Sistem, seyahat faturasını tahsis etmek için varlıkları aşağıdaki sıraya göre işlemelidir:

1. Fatura günlüğü üst bilgisi (`VendInvoiceJournalHeaderEntity`)
1. Fatura günlüğü satırı (`VendInvoiceJournalLineEntity`)
1. Son teslim alma maliyeti tahsisatları (`ITMLedgerJournalEntities`)
