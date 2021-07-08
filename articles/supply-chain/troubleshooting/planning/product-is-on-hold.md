---
title: Ürün hareketler için beklemede
description: Planlama emirlerini kesinleştirdikten sonra, maddenin hareketler için beklemede olduğunu bildiren bir hata iletisi alırsınız.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301291"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="bea53-103">Ürün hareketler için beklemede</span><span class="sxs-lookup"><span data-stu-id="bea53-103">Product is on hold for transactions</span></span>

<span data-ttu-id="bea53-104">Hata kodu: SYS13295</span><span class="sxs-lookup"><span data-stu-id="bea53-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="bea53-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="bea53-105">Symptoms</span></span>

<span data-ttu-id="bea53-106">Planlı siparişleri kesinleştirdikten sonra aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="bea53-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="bea53-107">%1 maddesi %2 hareketleri için durdurulmuş durumda.</span><span class="sxs-lookup"><span data-stu-id="bea53-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="bea53-108">Nedeni</span><span class="sxs-lookup"><span data-stu-id="bea53-108">Cause</span></span>

<span data-ttu-id="bea53-109">Engellenmiş maddeleri açıklarken, sistem *engellendi*, *durduruldu* ve *beklemede* terimlerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="bea53-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="bea53-110">Bu hata, maddenin varsayılan sipariş ayarlarında **Durduruldu** olarak ayarlandığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="bea53-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="bea53-111">Bir madde engellenirse ve bunu bir satınalma siparişine veya satış siparişi satırına eklerseniz, uyarı iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="bea53-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="bea53-112">Bir madde engellendiğinde, satınalma siparişi veya satış siparişi satırıyla ilgili stok hareketleri, örneğin bir sevk irsaliyesini veya faturayı deftere naklederken, değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="bea53-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="bea53-113">Satın alınan bir maddeyi engelleyebilir ve aynı zamanda satabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea53-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="bea53-114">Bu durumda, **Durduruldu** onay kutusu bir satınalma siparişinde seçilir ancak madde stokta veya satış siparişinde engellenmez.</span><span class="sxs-lookup"><span data-stu-id="bea53-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="bea53-115">Aşağıda, bir madde numarasının satılmasını engellemeye neden olabilecek bazı koşullar yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="bea53-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="bea53-116">Madde hala geliştirilme veya üretim aşamasındadır.</span><span class="sxs-lookup"><span data-stu-id="bea53-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="bea53-117">Bu nedenle, satılmasını veya rezerve olmasını istemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea53-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="bea53-118">Birçok kusurlu madde aldınız ve maddenin satılabilmesi için hataların düzeltilmesi gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="bea53-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="bea53-119">Bu tür durumlarda, sorun çözülünceye kadar maddeyi bloke edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea53-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="bea53-120">Bir madde bloke edildiyse ve iade emri satırı oluşturduysanız bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="bea53-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="bea53-121">Bir madde dizisini veya lotunu bloke edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea53-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="bea53-122">Maddenin bazı bölümlerinin bloke edilmesi gerekiyorsa bunları stoku taşıyarak veya maddenin o döneme ait tüm stokunu engelleyerek yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea53-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="bea53-123">Çözüm</span><span class="sxs-lookup"><span data-stu-id="bea53-123">Resolution</span></span>

- <span data-ttu-id="bea53-124">Madde için **Varsayılan sipariş ayarları** sayfasını açın ve **Durduruldu** onay kutusunu temizleyin.</span><span class="sxs-lookup"><span data-stu-id="bea53-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
