---
title: Birden fazla müşteri siparişi ve faturasındaki maddeleri iade etme
description: Bu konuda, Dynamics 365 Commerce'teki birden fazla müşteri siparişi ve faturası arasında iadeleri etkinleştirme işlevi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: ee4c863e617b9351e55e1fc652ea8905f17c8346
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976675"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a><span data-ttu-id="5d190-103">Birden fazla müşteri siparişi ve faturasındaki maddeleri iade etme</span><span class="sxs-lookup"><span data-stu-id="5d190-103">Return items across multiple customer orders and invoices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="5d190-104">Bu makalede, müşteri siparişi iadelerini birden fazla fatura üzerinden en iyi duruma getiren iki özellik açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5d190-104">This article describes two features that optimize customer order returns over multiple invoices.</span></span> 

## <a name="enable-refunds-over-multiple-captures"></a><span data-ttu-id="5d190-105">Birden fazla yakalama üzerinden geri ödemeleri etkinleştir</span><span class="sxs-lookup"><span data-stu-id="5d190-105">Enable refunds over multiple captures</span></span>

<span data-ttu-id="5d190-106">Bu özellik aynı müşteri siparişine karşı çoklu bağlantılı geri ödemeleri etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="5d190-106">This feature enables multiple linked refunds against the same customer order.</span></span> 

1. <span data-ttu-id="5d190-107">**Özellik yönetimi** çalışma alanına gidin ve **Çoklu yakalamalar üzerinde geri ödemeleri etkinleştir**'i arayın.</span><span class="sxs-lookup"><span data-stu-id="5d190-107">Go to the **Feature management** workspace and search for **Enable refunds over multiple captures**.</span></span>
2. <span data-ttu-id="5d190-108">**Çoklu siparişler üzerinde geri ödemeleri etkinleştir**'i seçin ve **Etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5d190-108">Select **Enable refunds over multiple orders** and then click **Enable**.</span></span> 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a><span data-ttu-id="5d190-109">Kısmi miktarlı iadeler için doğru vergi hesaplamasını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="5d190-109">Enable proper tax calculation for returns with partial quantity</span></span>

<span data-ttu-id="5d190-110">Bu özellik, bir sipariş birden çok fatura kullanılarak iade edildiğinde, vergilerin sonunda uygulanan vergi tutarına eşit olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="5d190-110">This feature ensures that when an order is returned using multiple invoices, the taxes will ultimately be equal to the tax amount originally charged.</span></span> 

1. <span data-ttu-id="5d190-111">**Özellik yönetimi** çalışma alanına gidin ve **Kısmi miktarlı iadeler için uygun vergi hesaplamasını etkinleştir**'i arayın.</span><span class="sxs-lookup"><span data-stu-id="5d190-111">Go to the **Feature management** workspace and search for **Enable proper tax calculation for returns with partial quantity**.</span></span>
2. <span data-ttu-id="5d190-112">**Kısmi miktarlı iadelerle ilgili doğru vergi hesaplamasını etkinleştir**'ı seçin ve ardından **Etkinleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5d190-112">Select **Enable proper tax calculation for returns with partial quantity** and then click **Enable**.</span></span> 


## <a name="process-returns"></a><span data-ttu-id="5d190-113">İadeleri işleme</span><span class="sxs-lookup"><span data-stu-id="5d190-113">Process returns</span></span>

<span data-ttu-id="5d190-114">Bu özellikler açıldıktan ve değişiklikler mağazalar ile eşitlendikten sonra mağazadaki kasiyer, iadeye yönelik olarak bir müşteri için birden fazla satış siparişi seçebilir.</span><span class="sxs-lookup"><span data-stu-id="5d190-114">After these features are turned on and the changes are synchronized to the stores, the cashier in the store can select multiple sales orders for a customer for their return.</span></span>

<span data-ttu-id="5d190-115">Siparişler seçildiğinde siparişler için tüm faturalar arasında tüm iade edilebilir ürünlerin listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5d190-115">When the orders are selected, a list of all the returnable products across all the invoices for the orders will display.</span></span> <span data-ttu-id="5d190-116">Daha sonra kasiyer, iade edilecek ürünleri seçebilir.</span><span class="sxs-lookup"><span data-stu-id="5d190-116">The cashier can then select the products to return.</span></span> <span data-ttu-id="5d190-117">Seçilen tüm ürünler için tek bir iade emri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5d190-117">A single return order will be created for all the selected products.</span></span>

<span data-ttu-id="5d190-118">Sipariş tam olarak iade edilirse müşteriye iade edilen vergilerin tutarı başlangıçta uygulanan vergi tutarına eşit olur.</span><span class="sxs-lookup"><span data-stu-id="5d190-118">If the order is fully returned, the amount of taxes returned to the customer will be equal to the amount of tax originally charged.</span></span>

