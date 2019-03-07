---
title: Teslimat zaman çizelgeleri
description: Teslimat zaman çizelgeleri tek bir satış siparişi, satış teklifi veya satın alma emri için birden fazla teslimat kullanılıyorken sipariş çizgisi miktarını izlemenize olanak tanır.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 068a881a7fa9b19198bd3ad22988465be49c1fa3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "325147"
---
# <a name="delivery-schedules"></a><span data-ttu-id="2ba4b-103">Teslimat zaman çizelgeleri</span><span class="sxs-lookup"><span data-stu-id="2ba4b-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ba4b-104">Teslimat zaman çizelgeleri tek bir satış siparişi, satış teklifi veya satın alma emri için birden fazla teslimat kullanılıyorken sipariş çizgisi miktarını izlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="2ba4b-105">Bir sipariş veya teklif satırındaki toplam miktarın çok sayıda sevkiyat ile teslim edilmesi gerekiyorsa, bir teslimat planı kullanın.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="2ba4b-106">Bireysel sevkiyatlar teslimat satırlarıyla gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="2ba4b-107">İki veya daha fazla teslimat satırı bir teslimat planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="2ba4b-108">Teslimat satırları farklı teslim tarihleri; miktarları; teslimat şekilleri; tesis ve ambar gibi depolama boyutları içerebilir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="2ba4b-109">**Bir teslimat zamanlaması örneği**</span><span class="sxs-lookup"><span data-stu-id="2ba4b-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="2ba4b-110">Toplam sipariş (orijinal sipariş satırı)</span><span class="sxs-lookup"><span data-stu-id="2ba4b-110">Total order (original order line)</span></span> | <span data-ttu-id="2ba4b-111">600 sandalye</span><span class="sxs-lookup"><span data-stu-id="2ba4b-111">600 chairs</span></span>                               |
| <span data-ttu-id="2ba4b-112">Talep edilen teslimat planı</span><span class="sxs-lookup"><span data-stu-id="2ba4b-112">Requested delivery schedule</span></span>       | <span data-ttu-id="2ba4b-113">Aylık 100 sandalye</span><span class="sxs-lookup"><span data-stu-id="2ba4b-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="2ba4b-114">Teslimat için talep edilen zaman aralığı</span><span class="sxs-lookup"><span data-stu-id="2ba4b-114">Requested time frame for delivery</span></span> | <span data-ttu-id="2ba4b-115">6 ay, her ayın ilk gününde</span><span class="sxs-lookup"><span data-stu-id="2ba4b-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="2ba4b-116">Bu senaryoda, müşteri altı aylık bir dönem için 100 sandalyelik kümeler halinde 600 sandalye teslimatı talep etmektedir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="2ba4b-117">Teslimat gereksinimlerini takip etmek için bir teslimat zamanlaması oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="2ba4b-118">Teslimat planı sayfasında, altı ayrı teslimat satırı oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="2ba4b-119">Her teslimat satırında 100 sandalye vardır ve bu 100 sandalyenin teslimat tarihini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="2ba4b-120">Bu durumda, her satır takip eden altı aylık dönemin ilk ayına mahsup eder.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="2ba4b-121">Bir teslimat planı oluşturduğunuzda, orijinal sipariş satırının türü otomatik olarak **Birden fazla teslimatlı sipariş satırları** seçeneğine değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="2ba4b-122">Bu türde bir satıra ticari bir satır olarak bakılır ve bir simgeyle işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="2ba4b-123">Teslimat satırı, farklı bir simgeyle işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="2ba4b-124">Bir teslimat satırlarında bir miktarı değiştirirseniz. ticari satırı güncelleştirilip, teslimat planı toplam miktarına çevrilir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="2ba4b-125">Ticaret anlaşması sipariş için bir toplam iskonto tanımladıysa, teslimat zamanlaması siparişinizin toplam sipariş iskontosuna uygun olduğundan emin olur, sipariş birden fazla teslimata ayrılmış olsa bile.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="2ba4b-126">Teslimat planı olan siparişler teslimat satırları göz önüne alınarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="2ba4b-127">İşlemlere sevk irsaliyelerinin deftere nakli, ürün girişleri ve faturalama dahildir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="2ba4b-128">Teslimat planı olan siparişlerin belge çıktıları ve teklifleri yalnızca teslimat satırlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="2ba4b-129">Orijinal satırları (ticari satırlar) göstermez.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="2ba4b-130">**Not:** Ek olarak aşağıdaki işlemleri gerçekleştirdiğinizde yalnızca teslimat satırları gösterilir:</span><span class="sxs-lookup"><span data-stu-id="2ba4b-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="2ba4b-131">Naklet</span><span class="sxs-lookup"><span data-stu-id="2ba4b-131">Post</span></span>
-   <span data-ttu-id="2ba4b-132">Sayfaları kopyala</span><span class="sxs-lookup"><span data-stu-id="2ba4b-132">Copy pages</span></span>
-   <span data-ttu-id="2ba4b-133">Liste sayfalarına ve raporlara gözat</span><span class="sxs-lookup"><span data-stu-id="2ba4b-133">Browse list pages and reports</span></span>

<span data-ttu-id="2ba4b-134">Satış tekliflerini onayladığınızda, elde edilen satış siparişleri sipariş satırlarında birden çok teslimat olsa bile tam teslimat planını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="2ba4b-135">Ayrıca, tüm teslimat planı satış siparişleri, satış teklifleri ve satınalma siparişleri gibi önemli sayfaların tümünde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2ba4b-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>



