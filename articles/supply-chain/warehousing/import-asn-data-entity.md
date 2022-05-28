---
title: Gelen ÖSB'leri V3 veri varlığı üzerinden içe aktarma
description: Bu konu, gelen önceden sevkiyat bildirimlerinin (ÖSB'ler) Gelen ÖSB veri varlığı aracılığıyla içe aktarma işleminin nasıl yönetildiğini açıklar.
author: GalynaFedorova
ms.date: 05/11/2022
ms.topic: article
ms.search.form: WHSInboundASNV3Entity, WHSInboundASNEntity, DMFEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 44ec0230236451a413d483b3e9f3ddc58b49a0b0
ms.sourcegitcommit: 90ffd763d18f97654b9dbc9e3f71c998e6094c6b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740147"
---
# <a name="import-inbound-asns-through-the-v3-data-entity"></a>Gelen ÖSB'leri V3 veri varlığı üzerinden içe aktarma

[!include [banner](../../includes/banner.md)]

Önceden sevkiyat bildirimleri (ÖSB'ler), sizi satıcı teslimatları hakkında bilgilendirir. Gönderenin, bir sevkiyat içeriğini ve madde ve paketleme gibi ek bilgileri açıklamasına yardımcı olur.

ÖSB'ler ambar çalışanlarının nelerin ne zaman geldiğini öğrenmesine yardımcı olabilir. Bu şekilde hazırlık yapabilirler. Ayrıca, ambar çalışanları önceden oluşturulmuş ilgili satınalma siparişiyle bir sevkiyatın ayrıntılarını eşleştirmek için ÖSB'leri kullanabilirler.

Bu konu, örnekler aracılığıyla, ÖSB dosyalarının nasıl kullanılacağını gösteren bir dizi senaryoyu göstermektedir.

> [!IMPORTANT]
> *Gelen ÖSB*'yi içe aktarma, yalnızca Gelişmiş ambar yönetimi (WMS) için etkinleştirilen maddelere uygulanır. Bir ÖSB almadan önce, bir satınalma siparişinin söz konusu ÖSB'yi gönderen satıcıya karşı sisteme kaydedilmiş olması gerekir.

## <a name="inbound-asn-v3-entity"></a>Gelen ÖSB V3 varlığı

Gelen ÖSB'leri *Gelen ÖSB V3* birleşik veri varlığını kullanarak içe aktarırsınız. *Gelen ÖSB V3* aşağıdaki varlıklardan yararlanır:

- Gelen yük başlığı
- Gelen sevkiyat başlığı
- Gelen yük ambalaj yapıları
- Gelen yük ambalaj yapısı olayları
- Gelen yük ambalaj yapısı olay satırları
- Gelen yük ambalaj yapısı satırları

*Gelen ÖSB V3* birleşik veri varlığı, XML dosyası tabanlı içe aktarmaların kullanıldığı zaman uyumsuz tümleştirme senaryolarına yöneliktir.

## <a name="xml-format-for-importing-asns"></a>ÖSB'leri içeri aktarma için XML biçimi

Microsoft Dynamics 365 Supply Chain Management, ÖSBleri içe aktarmak için aşağıdaki XML biçimini destekler. XML dosyasındaki her düğüm, bağımsız bir varlıktan bir özniteliği temsil eder.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV3Entity>
                    </WHSInboundPackingStructureCaseLineV3Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV3Entity>
                </WHSInboundLoadPackingStructureLineV3Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a>Örnekler

Aşağıdaki alt bölümler satıcı sevkiyatları için ASN XML içe aktarma dosyası örnekleri sunar.

### <a name="example-1"></a>Örnek 1

Aşağıdaki örnek, hiçbir durum ayrıntısı dahil edilmediğinde bir satınalma siparişine ait satıcı sevk irsaliyelerini içe aktarmak için kullanılan bir XML dosyasını gösterir.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a>Örnek 2

Aşağıdaki örnek, durum ayrıntıları dahil edildiğinde bir satınalma siparişine ait satıcı sevk irsaliyelerini içe aktarmak için kullanılan bir XML dosyasını gösterir.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLine3Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a>Örnek 3

Aşağıdaki örnek, durum ayrıntıları dahil edildiğinde birden çok satınalma siparişine ait satıcı sevk irsaliyelerini içe aktarmak için kullanılan bir XML dosyasını gösterir.

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV3Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a>ÖSB dosyası içe aktarma sonuçlarını inceleme

ÖSB dosyası içe aktarma sonuçlarını incelemek için bu adımları izleyin.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. ÖSB içe aktarma işleminin parçası olarak oluşturulmuş bir yüklemeyi bulun ve açın.
1. **Yük** hızlı sekmesinde XML dosyasını temel alan değerleri görmeniz gerekir.
1. **Yük satırları** hızlı sekmesinde, XML dosyasını temel alan satın alma sipariş numaralarını ve madde ayrıntılarını görmeniz gerekir.
1. Eylem Bölmesinde, **Sevk ve teslim alma** sekmesinde, **Teslim alma** grubunda, yükün paket yapısını gözden geçirmek için **Paketleme yapısı**'nı seçin.
1. **Paletler** hızlı sekmesinde XML dosyasını temel alan plakaları görmeniz gerekir.
1. **Koliler** hızlı sekmesinde XML dosyasını temel alan kolileri görmeniz gerekir.
1. **Maddeler** hızlı sekmesinde XML dosyasını temel alan maddaleri ve miktarları görmeniz gerekir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
