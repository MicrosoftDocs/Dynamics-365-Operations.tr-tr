---
title: Birden fazla müşteri siparişi ve faturası arasında iade kalemleri
description: Bu konuda Microsoft Dynamics 365 for Retail'daki birden fazla müşteri siparişi ve faturası arasında iadeleri etkinleştirme işlevi açıklanmaktadır.
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
ms.openlocfilehash: c201311028b11121d626e93859a2b98497c047d1
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2019
ms.locfileid: "777238"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="0726c-103">Birden fazla müşteri siparişi ve faturası arasında iade kalemleri</span><span class="sxs-lookup"><span data-stu-id="0726c-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="0726c-104">Dynamics 365 for Finance and Operations sürüm 10.0'da birden fazla sipariş ve fatura arasında iade yapılabilir ancak 10.0'dan önceki sürümlerde iadeler, yalnızca tek seferde tek bir fatura ile işlenebilmektedir.</span><span class="sxs-lookup"><span data-stu-id="0726c-104">In Dynamics 365 for Finance and Operations version 10.0, returns can be made across multiple orders and invoices, whereas in releases prior to 10.0, returns could only be processed by a single invoice at a time.</span></span> 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a><span data-ttu-id="0726c-105">Birden fazla müşteri siparişi ve faturası arasındaki iadeleri desteklemek için Retail'ı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="0726c-105">Configure Retail to support returns across multiple customer order and invoices</span></span>

1. <span data-ttu-id="0726c-106">**Retail parametreleri \> Müşteri siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="0726c-106">Go to **Retail parameters \> Customer orders**.</span></span>
1. <span data-ttu-id="0726c-107">**Birden fazla sipariş için iadeleri etkinleştirme** parametresini açın.</span><span class="sxs-lookup"><span data-stu-id="0726c-107">Turn on the **Enable returns for multiple orders** parameter.</span></span> 

## <a name="process-returns"></a><span data-ttu-id="0726c-108">İadeleri işleme</span><span class="sxs-lookup"><span data-stu-id="0726c-108">Process returns</span></span>

<span data-ttu-id="0726c-109">Parametre açıldıktan ve değişiklikler mağazalar ile eşitlendikten sonra mağazadaki kasiyer, iadeye yönelik olarak bir müşteri için birden fazla satış siparişi seçebilir.</span><span class="sxs-lookup"><span data-stu-id="0726c-109">After the parameter is turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="0726c-110">Siparişler seçildiğinde siparişler için tüm faturalar arasında tüm iade edilebilir ürünlerin listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0726c-110">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="0726c-111">Daha sonra kasiyer, iade edilecek ürünleri seçebilir.</span><span class="sxs-lookup"><span data-stu-id="0726c-111">The cashier can then select the products to return.</span></span> <span data-ttu-id="0726c-112">Seçilen tüm ürünler için tek bir iade emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0726c-112">A single return order will be created for all the selected products.</span></span>
