---
title: Gelen ÖSB'leri V2 veri varlığı üzerinden içe aktarma
description: Bu konu, gelen önceden sevkiyat bildirimlerinin (ÖSB'ler) Gelen ÖSB V2 veri varlığı aracılığıyla içe aktarma işleminin nasıl yönetildiğini açıklar.
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: WHSInboundASNV2Entity, WHSInboundASNEntity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-04
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 470cc0c39f211a5d0f106c4c6e193867388e2b53
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249183"
---
# <a name="import-inbound-asns-through-the-v2-data-entity"></a><span data-ttu-id="1561b-103">Gelen ÖSB'leri V2 veri varlığı üzerinden içe aktarma</span><span class="sxs-lookup"><span data-stu-id="1561b-103">Import inbound ASNs through the V2 data entity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1561b-104">Önceden sevkiyat bildirimleri (ÖSB'ler), sizi satıcı teslimatları hakkında bilgilendirir.</span><span class="sxs-lookup"><span data-stu-id="1561b-104">Advanced shipping notices (ASNs) notify you about vendor deliveries.</span></span> <span data-ttu-id="1561b-105">Gönderenin, bir sevkiyat içeriğini ve madde ve paketleme gibi ek bilgileri açıklamasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1561b-105">They help the sender describe the contents of a shipment and additional information about it, such as the items and packaging.</span></span>

<span data-ttu-id="1561b-106">ÖSB'ler ambar çalışanlarının nelerin ne zaman geldiğini öğrenmesine yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1561b-106">ASNs can help warehouse workers learn what is arriving when.</span></span> <span data-ttu-id="1561b-107">Bu şekilde hazırlık yapabilirler.</span><span class="sxs-lookup"><span data-stu-id="1561b-107">Therefore, they can prepare.</span></span> <span data-ttu-id="1561b-108">Ayrıca, ambar çalışanları önceden oluşturulmuş ilgili satınalma siparişiyle bir sevkiyatın ayrıntılarını eşleştirmek için ÖSB'leri kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="1561b-108">In addition, warehouse workers can use ASNs to match the details of a shipment to the related purchase order that was previously created.</span></span>

<span data-ttu-id="1561b-109">Bu konu, örnekler aracılığıyla, ÖSB dosyalarının nasıl kullanılacağını gösteren bir dizi senaryoyu göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="1561b-109">This topic presents a collection of scenarios that show, through examples, how to work with ASN files.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1561b-110">*Gelen ÖSB*'yi içe aktarma, yalnızca Gelişmiş ambar yönetimi (WMS) için etkinleştirilen maddelere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="1561b-110">*Inbound ASN* import applies only to items that are enabled for advanced warehouse management (WMS).</span></span> <span data-ttu-id="1561b-111">Bir ÖSB almadan önce, bir satınalma siparişinin söz konusu ÖSB'yi gönderen satıcıya karşı sisteme kaydedilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="1561b-111">Before you receive an ASN, a purchase order must be registered in the system against the vendor who is sending that ASN.</span></span>

## <a name="inbound-asn-v2-entity"></a><span data-ttu-id="1561b-112">Gelen ÖSB V2 varlığı</span><span class="sxs-lookup"><span data-stu-id="1561b-112">Inbound ASN V2 entity</span></span>

<span data-ttu-id="1561b-113">Gelen ÖSB'leri *Gelen ÖSB V2* birleşik veri varlığını kullanarak içe aktarırsınız.</span><span class="sxs-lookup"><span data-stu-id="1561b-113">You import inbound ASNs by using the *Inbound ASN V2* composite data entity.</span></span> <span data-ttu-id="1561b-114">*Gelen ÖSB V2* aşağıdaki varlıklardan yararlanır:</span><span class="sxs-lookup"><span data-stu-id="1561b-114">*Inbound ASN V2* takes advantage of the following entities:</span></span>

- <span data-ttu-id="1561b-115">Gelen yük başlığı</span><span class="sxs-lookup"><span data-stu-id="1561b-115">Inbound load header</span></span>
- <span data-ttu-id="1561b-116">Gelen sevkiyat başlığı</span><span class="sxs-lookup"><span data-stu-id="1561b-116">Inbound shipment header</span></span>
- <span data-ttu-id="1561b-117">Gelen yük ambalaj yapıları</span><span class="sxs-lookup"><span data-stu-id="1561b-117">Inbound load packing structures</span></span>
- <span data-ttu-id="1561b-118">Gelen yük ambalaj yapısı olayları</span><span class="sxs-lookup"><span data-stu-id="1561b-118">Inbound load packing structure cases</span></span>
- <span data-ttu-id="1561b-119">Gelen yük ambalaj yapısı olay satırları</span><span class="sxs-lookup"><span data-stu-id="1561b-119">Inbound load packing structure case lines</span></span>
- <span data-ttu-id="1561b-120">Gelen yük ambalaj yapısı satırları</span><span class="sxs-lookup"><span data-stu-id="1561b-120">Inbound load packing structure lines</span></span>

<span data-ttu-id="1561b-121">*Gelen ÖSB V2* birleşik veri varlığı, XML dosyası tabanlı içe aktarmaların kullanıldığı zaman uyumsuz tümleştirme senaryolarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="1561b-121">The *Inbound ASN V2* composite data entity is intended for asynchronous integration scenarios where XML file–based imports are used.</span></span>

## <a name="xml-format-for-importing-asns"></a><span data-ttu-id="1561b-122">ÖSB'leri içeri aktarma için XML biçimi</span><span class="sxs-lookup"><span data-stu-id="1561b-122">XML format for importing ASNs</span></span>

<span data-ttu-id="1561b-123">Microsoft Dynamics 365 Supply Chain Management, ÖSBleri içe aktarmak için aşağıdaki XML biçimini destekler.</span><span class="sxs-lookup"><span data-stu-id="1561b-123">Microsoft Dynamics 365 Supply Chain Management supports the following XML format for importing ASNs.</span></span> <span data-ttu-id="1561b-124">XML dosyasındaki her düğüm, bağımsız bir varlıktan bir özniteliği temsil eder.</span><span class="sxs-lookup"><span data-stu-id="1561b-124">Each node in the XML file represents an attribute from an individual entity.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity>
        <WHSInboundShipmentHeaderEntity>
            <WHSInboundLoadPackingStructureEntity>
                <WHSInboundLoadPackingStructureCaseEntity>
                    <WHSInboundPackingStructureCaseLineV2Entity>
                    </WHSInboundPackingStructureCaseLineV2Entity>
                </WHSInboundLoadPackingStructureCaseEntity>
                <WHSInboundLoadPackingStructureLineV2Entity>
                </WHSInboundLoadPackingStructureLineV2Entity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="examples"></a><span data-ttu-id="1561b-125">Örnekler</span><span class="sxs-lookup"><span data-stu-id="1561b-125">Examples</span></span>

<span data-ttu-id="1561b-126">Aşağıdaki alt bölümler satıcı sevkiyatları için ASN XML içe aktarma dosyası örnekleri sunar.</span><span class="sxs-lookup"><span data-stu-id="1561b-126">The following subsections provide examples of ASN XML import files for vendor shipments.</span></span>

### <a name="example-1"></a><span data-ttu-id="1561b-127">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1561b-127">Example 1</span></span>

<span data-ttu-id="1561b-128">Aşağıdaki örnek, hiçbir durum ayrıntısı dahil edilmediğinde bir satınalma siparişine ait satıcı sevk irsaliyelerini içe aktarmak için kullanılan bir XML dosyasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1561b-128">The following example shows an XML file for importing vendor shipments for one purchase order when no case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VENDORADDRESSSTREET = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="1" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-2"></a><span data-ttu-id="1561b-129">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1561b-129">Example 2</span></span>

<span data-ttu-id="1561b-130">Aşağıdaki örnek, durum ayrıntıları dahil edildiğinde bir satınalma siparişine ait satıcı sevk irsaliyelerini içe aktarmak için kullanılan bir XML dosyasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1561b-130">The following example shows an XML file for importing vendor shipments for one purchase order when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity ESTIMATEDARRIVALDATETIME="2021-04-25T11:00:00+00:00">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="MVR_SNN_0004">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="MVR_SNN_0004" PACKEDTOTALQUANTITY="2.00">
                <WHSInboundLoadPackingStructureCaseEntity PARENTPACKINGSTRUCTURELICENSEPLATENUMBER="MVR_SNN_0004" LICENSEPLATENUMBER="MVR_SNN_0004A" PACKEDTOTALQUANTITY="2.00" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000175" ITEMNUMBER="A0001" PURCHASEORDERLINENUMBER="1" QUANTITY="2.00" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

### <a name="example-3"></a><span data-ttu-id="1561b-131">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="1561b-131">Example 3</span></span>

<span data-ttu-id="1561b-132">Aşağıdaki örnek, durum ayrıntıları dahil edildiğinde birden çok satınalma siparişine ait satıcı sevk irsaliyelerini içe aktarmak için kullanılan bir XML dosyasını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1561b-132">The following example shows an XML file for importing vendor shipments for multiple purchase orders when case details are included.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document>
    <WHSInboundLoadHeaderEntity TRACTORNUMBER="0000101">
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_01" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000176" ITEMNUMBER="A0001" QUANTITY="100" UNITSYMBOL="ea" />
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
        <WHSInboundShipmentHeaderEntity VENDORSHIPMENTID="VendASN_02" VENDORADDRESSCOUNTRYREGIONID = "USA" VendorAddressStreet = "123 Coffee Street" VENDORADDRESSSTATEID = "WA" VENDORADDRESSCITY = "Redmond" VENDORADDRESSZIPCODE = "98052">
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_001">
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="200" UNITSYMBOL="ea" />
                <WHSInboundLoadPackingStructureLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="P0004" QUANTITY="300" UNITSYMBOL="ea" ITEMBATCHNUMBER="BN0001" />
            </WHSInboundLoadPackingStructureEntity>
            <WHSInboundLoadPackingStructureEntity LICENSEPLATENUMBER="LP_ASN_002">
                <WHSInboundLoadPackingStructureCaseEntity LICENSEPLATENUMBER="LP_ASN_002_C01">
                    <WHSInboundLoadPackingStructureCaseLineV2Entity PURCHASEORDERNUMBER="00000177" ITEMNUMBER="A0001" QUANTITY="400" UNITSYMBOL="ea" />
                </WHSInboundLoadPackingStructureCaseEntity>
            </WHSInboundLoadPackingStructureEntity>
        </WHSInboundShipmentHeaderEntity>
    </WHSInboundLoadHeaderEntity>
</Document>
```

## <a name="inspect-the-results-of-importing-an-asn-file"></a><span data-ttu-id="1561b-133">ÖSB dosyası içe aktarma sonuçlarını inceleme</span><span class="sxs-lookup"><span data-stu-id="1561b-133">Inspect the results of importing an ASN file</span></span>

<span data-ttu-id="1561b-134">ÖSB dosyası içe aktarma sonuçlarını incelemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1561b-134">Follow these steps to inspect the results of importing an ASN file.</span></span>

1. <span data-ttu-id="1561b-135">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1561b-135">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1561b-136">ÖSB içe aktarma işleminin parçası olarak oluşturulmuş bir yüklemeyi bulun ve açın.</span><span class="sxs-lookup"><span data-stu-id="1561b-136">Find and open a load that was created as part of an ASN import.</span></span>
1. <span data-ttu-id="1561b-137">**Yük** hızlı sekmesinde XML dosyasını temel alan değerleri görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1561b-137">On the **Load** FastTab, you should see values that are based on the XML file.</span></span>
1. <span data-ttu-id="1561b-138">**Yük satırları** hızlı sekmesinde, XML dosyasını temel alan satın alma sipariş numaralarını ve madde ayrıntılarını görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1561b-138">On the **Load lines** FastTab, you should see purchase order numbers and item details that are based on the XML file.</span></span>
1. <span data-ttu-id="1561b-139">Eylem Bölmesinde, **Sevk ve teslim alma** sekmesinde, **Teslim alma** grubunda, yükün paket yapısını gözden geçirmek için **Paketleme yapısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="1561b-139">On the Action Pane, on the **Ship and receive** tab, in the **Receive** group, select **Packing structure** to review the packing structure of the load.</span></span>
1. <span data-ttu-id="1561b-140">**Paletler** hızlı sekmesinde XML dosyasını temel alan plakaları görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1561b-140">On the **Pallets** FastTab, you should see license plates that are based on the XML file.</span></span>
1. <span data-ttu-id="1561b-141">**Koliler** hızlı sekmesinde XML dosyasını temel alan kolileri görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1561b-141">On the **Cases** FastTab, you should see cases that are based on the XML file.</span></span>
1. <span data-ttu-id="1561b-142">**Maddeler** hızlı sekmesinde XML dosyasını temel alan maddaleri ve miktarları görmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1561b-142">On the **Items** FastTab, you should see items and quantities that are based on the XML file.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
