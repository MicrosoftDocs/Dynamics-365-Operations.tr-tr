---
title: Satıcı iş birliğini kullanarak konsinye stoğu izleme
description: Bu yordam müşteriye konsinye olarak bıraktığınız ürünün stok düzeyi hakkında bilgileri görmek için satıcı işbirliğini kullanmayı gösterir.
author: sherry-zheng
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e397c12b9f605d1c864ce053477090ed8c1700
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839283"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="e7b36-103">Satıcı iş birliğini kullanarak konsinye stoğu izleme</span><span class="sxs-lookup"><span data-stu-id="e7b36-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7b36-104">Bu yordam müşteriye konsinye olarak bıraktığınız ürünün stok düzeyi hakkında bilgileri görmek için satıcı işbirliğini kullanmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7b36-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="e7b36-105">Ayrıca müşteri stoğun sahipliğini üzerine aldığında stok tüketimini de izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b36-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="e7b36-106">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b36-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="e7b36-107">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="e7b36-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="e7b36-108">Tüketilen stoğu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="e7b36-108">View consumed inventory</span></span>
1. <span data-ttu-id="e7b36-109">Satıcı iş birliği > Konsinye stok > Konsinye stoktan alınan ürünler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="e7b36-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="e7b36-110">Liste, konsinye stoğun sahipliği satıcıdan müşteri olarak değiştirildiğinde oluşturulan ürün giriş satırlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7b36-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="e7b36-111">Miktarları ve diğer bilgileri görmek için ekranı sağa doğru kaydırmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e7b36-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="e7b36-112">Bu listedeki bilgileri müşteriniz için fatura oluşturmada kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b36-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="e7b36-113">Ayrıca verileri Microsoft Excel'e dışa aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b36-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="e7b36-114">Satınalma siparişini görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e7b36-114">Click View purchase order.</span></span>
3. <span data-ttu-id="e7b36-115">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e7b36-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="e7b36-116">Satır, Konsinye olarak işaretlenir ve başlık bölümü satınalma siparişinin Alındı durumuna sahip olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7b36-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="e7b36-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e7b36-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="e7b36-118">Eldeki stoğu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="e7b36-118">View on-hand inventory</span></span>
1. <span data-ttu-id="e7b36-119">Satıcı iş birliği > Konsinye stok > Eldeki konsinye stok'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e7b36-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="e7b36-120">Eldeki konsinye stok sayfası müşterinin ambarında sahip olduğunu stoğu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7b36-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="e7b36-121">Boyutları görüntüle sekmesine tıklayarak, tesis ve ambar gibi ek boyutları da görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e7b36-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]