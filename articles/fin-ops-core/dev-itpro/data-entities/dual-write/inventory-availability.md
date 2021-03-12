---
title: Çift yazılarda stok kullanılabilirliği
description: Bu konu, çift yazmada envanter kullanılabilirliğini kontrol etme hakkında bilgi sağlar.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839561"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="f625b-103">Çift yazılarda stok kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="f625b-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f625b-104">Stok kullanılabilirliğini kullanarak, bir ürünü Microsoft Dynamics 365 Sales'te model temelli uygulamalardaki **Teklifler**, **Siparişler** veya **Faturalar** sayfasına eklemeden önce Stoğunuzu kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f625b-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="f625b-105">Örneğin, stok denetimi ve karşılama tarihi belirleme [aday müşteriden nakde](dual-write-prospect-to-cash.md) işlemindeki anahtar görevdir.</span><span class="sxs-lookup"><span data-stu-id="f625b-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="f625b-106">Yeterli stoğa sahip değilseniz, tahmini stok alış girişlerine ve çıkışlarına göre bir teslimat tarihi tahmin edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f625b-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="f625b-107">Ayrıca, ATP miktarını önceden tanımlanmış zaman diliminden bulabileceğiniz, maddenin taahhüt edilebilir (ATP) bilgilerini de denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f625b-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="f625b-108">Eldeki stok</span><span class="sxs-lookup"><span data-stu-id="f625b-108">On-hand inventory</span></span>

<span data-ttu-id="f625b-109">Dynamics 365 Sales'te **Teklifler**, **Siparişler** ve **Fatura** sayfalarının başlığına yen bir **Eldeki stok** düğmesi eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="f625b-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="f625b-110">Bu düğmeyi seçtiğinizde, bir iletişim kutusu görüntülenir ve eldeki stoğu denetlemek istediğiniz şirketi ve ürünü burada belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f625b-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="f625b-111">Bu iletişim kutusu [Eldeki stok](../../../../supply-chain/inventory/tasks/check-availability-stock.md) ile aynı bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="f625b-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="f625b-112">İletişim kutusu Dynamics 365 Supply Chain Management'tan stok bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="f625b-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f625b-113">Bilgiler aşağıdaki miktarları içerir:</span><span class="sxs-lookup"><span data-stu-id="f625b-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="f625b-114">Eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="f625b-114">On-hand quantity</span></span>
- <span data-ttu-id="f625b-115">Tersine çevrilen eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="f625b-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="f625b-116">Kullanılabilir eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="f625b-116">Available on-hand quantity</span></span>
- <span data-ttu-id="f625b-117">Sipariş miktarı</span><span class="sxs-lookup"><span data-stu-id="f625b-117">Ordered quantity</span></span>
- <span data-ttu-id="f625b-118">Siparişteki miktar</span><span class="sxs-lookup"><span data-stu-id="f625b-118">On-order quantity</span></span>
- <span data-ttu-id="f625b-119">Ayrılan sipariş edilen miktar</span><span class="sxs-lookup"><span data-stu-id="f625b-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="f625b-120">Toplam kullanılabilir miktar</span><span class="sxs-lookup"><span data-stu-id="f625b-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="f625b-121">KM bilgileri</span><span class="sxs-lookup"><span data-stu-id="f625b-121">ATP information</span></span>

<span data-ttu-id="f625b-122">Sales'te **Teklifler**, **Siparişler** ve **Faturalar** sayfalarındaki satır öğelerine yeni bir **ATP Bilgileri** düğmesi eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="f625b-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="f625b-123">Bu düğmeyi seçtiğinizde, bir iletişim kutusu görüntülenir ve şirketi, stok tesisini, stok ambarını ve sipariş miktarını burada belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f625b-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="f625b-124">Bu iletişim kutusu, [Sipariş taahhüdü](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) bölümünde açıklananlarla aynı ayarlara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="f625b-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="f625b-125">İletişim kutusu, Supply Chain Management'taki ATP bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f625b-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="f625b-126">Bilgiler aşağıdaki miktarları içerir:</span><span class="sxs-lookup"><span data-stu-id="f625b-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="f625b-127">KM miktarı</span><span class="sxs-lookup"><span data-stu-id="f625b-127">ATP quantity</span></span>
- <span data-ttu-id="f625b-128">Giriş  miktarı</span><span class="sxs-lookup"><span data-stu-id="f625b-128">Receipt quantity</span></span>
- <span data-ttu-id="f625b-129">Çıkış miktarı</span><span class="sxs-lookup"><span data-stu-id="f625b-129">Issue quantity</span></span>
- <span data-ttu-id="f625b-130">Eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="f625b-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="f625b-131">Nasıl çalışır</span><span class="sxs-lookup"><span data-stu-id="f625b-131">How it works</span></span>

<span data-ttu-id="f625b-132">**Teklifler**, **Siparişler** veya **Faturalar** sayfasında **Eldeki Stok** düğmesini seçtiğinizde, **Eldeki Stok API**'sine canlı bir çift yazma çağrısı yapılır.</span><span class="sxs-lookup"><span data-stu-id="f625b-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="f625b-133">API, belirli ürün için eldeki stoku hesaplar.</span><span class="sxs-lookup"><span data-stu-id="f625b-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="f625b-134">Sonuç, **InventCDSInventoryOnHandRequestEntity** ve **InventCDSInventoryOnHandEntryEntity** tablolarında saklanır ve daha sonra çift yazma tarafından Dataverse'e yazılır.</span><span class="sxs-lookup"><span data-stu-id="f625b-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="f625b-135">Bu işlevi kullanmak için, aşağıdaki çift yazma eşlemelerini çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="f625b-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="f625b-136">Eşlemeleri çalıştırdığınızda ilk eşitlemeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="f625b-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="f625b-137">CDS eldeki stok girişleri (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="f625b-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="f625b-138">CDS eldeki stok istekleri (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="f625b-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="f625b-139">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="f625b-139">Templates</span></span>
<span data-ttu-id="f625b-140">Eldeki stok verilerini göstermek için aşağıdaki şablonlar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f625b-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="f625b-141">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="f625b-141">Finance and Operations apps</span></span> | <span data-ttu-id="f625b-142">Müşteri etkileşimi uygulaması</span><span class="sxs-lookup"><span data-stu-id="f625b-142">Customer engagement app</span></span> | <span data-ttu-id="f625b-143">Tanım</span><span class="sxs-lookup"><span data-stu-id="f625b-143">Description</span></span> 
---|---|---
[<span data-ttu-id="f625b-144">CDS eldeki stok girişleri</span><span class="sxs-lookup"><span data-stu-id="f625b-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="f625b-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="f625b-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="f625b-146">CDS eldeki stok istekleri</span><span class="sxs-lookup"><span data-stu-id="f625b-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="f625b-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="f625b-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="f625b-148">CDS eldeki stok girişleri (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="f625b-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="f625b-149">Bu şablon, Finance and Operations uygulamaları ve Dataverse arasında verileri eşitler.</span><span class="sxs-lookup"><span data-stu-id="f625b-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="f625b-150">Finance and Operations alanı</span><span class="sxs-lookup"><span data-stu-id="f625b-150">Finance and Operations field</span></span> | <span data-ttu-id="f625b-151">Eşleme türü</span><span class="sxs-lookup"><span data-stu-id="f625b-151">Map type</span></span> | <span data-ttu-id="f625b-152">Müşteri etkileşimi alanı</span><span class="sxs-lookup"><span data-stu-id="f625b-152">Customer engagement field</span></span> | <span data-ttu-id="f625b-153">Varsayılan değer</span><span class="sxs-lookup"><span data-stu-id="f625b-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="f625b-154">CDS eldeki stok istekleri (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="f625b-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="f625b-155">Bu şablon, Finance and Operations uygulamaları ve Dataverse arasında verileri eşitler.</span><span class="sxs-lookup"><span data-stu-id="f625b-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="f625b-156">Finance and Operations alanı</span><span class="sxs-lookup"><span data-stu-id="f625b-156">Finance and Operations field</span></span> | <span data-ttu-id="f625b-157">Eşleme türü</span><span class="sxs-lookup"><span data-stu-id="f625b-157">Map type</span></span> | <span data-ttu-id="f625b-158">Müşteri etkileşimi alanı</span><span class="sxs-lookup"><span data-stu-id="f625b-158">Customer engagement field</span></span> | <span data-ttu-id="f625b-159">Varsayılan değer</span><span class="sxs-lookup"><span data-stu-id="f625b-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |




