---
title: Birden fazla müşteri siparişi ve faturası arasında iade kalemleri
description: Bu konuda, Dynamics 365 Retail'daki birden fazla müşteri siparişi ve faturası arasında iadeleri etkinleştirme işlevi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018001"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="717c6-103">Birden fazla müşteri siparişi ve faturası arasında iade kalemleri</span><span class="sxs-lookup"><span data-stu-id="717c6-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="717c6-104">İadeler, birden fazla sipariş ve fatura arasında yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="717c6-104">Returns can be made across multiple orders and invoices.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="717c6-105">Birden fazla müşteri siparişi ve faturası arasındaki iadeleri desteklemek için Retail'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="717c6-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="717c6-106">**Perakende parametreleri \> Müşteri siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="717c6-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="717c6-107">**Birden fazla sipariş için iadeleri etkinleştirme** parametresini açın.</span><span class="sxs-lookup"><span data-stu-id="717c6-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="717c6-108">İadeleri işleme</span><span class="sxs-lookup"><span data-stu-id="717c6-108">Process returns</span></span>

<span data-ttu-id="717c6-109">Parametre açıldıktan ve değişiklikler mağazalar ile eşitlendikten sonra mağazadaki kasiyer, iadeye yönelik olarak bir müşteri için birden fazla satış siparişi seçebilir.</span><span class="sxs-lookup"><span data-stu-id="717c6-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="717c6-110">Siparişler seçildiğinde siparişler için tüm faturalar arasında tüm iade edilebilir ürünlerin listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="717c6-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="717c6-111">Daha sonra kasiyer, iade edilecek ürünleri seçebilir.</span><span class="sxs-lookup"><span data-stu-id="717c6-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="717c6-112">Seçilen tüm ürünler için tek bir iade emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="717c6-112">A single return order will be created for all the selected products.</span></span>
