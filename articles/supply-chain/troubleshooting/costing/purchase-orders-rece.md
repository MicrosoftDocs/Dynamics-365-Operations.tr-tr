---
title: Fiziksel olarak alınan satınalma siparişleri stok kapatma raporunda görünmüyor
description: Fiziksel olarak alınan satınalma siparişleri, stok kapatma raporu olan Açık miktarları denetle seçeneğinde görünmüyor.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026983"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="1e6e9-103">Fiziksel olarak alınan satınalma siparişleri stok kapatma raporunda görünmüyor</span><span class="sxs-lookup"><span data-stu-id="1e6e9-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="1e6e9-104">KB numarası: 4612595</span><span class="sxs-lookup"><span data-stu-id="1e6e9-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="1e6e9-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="1e6e9-105">Symptoms</span></span>

<span data-ttu-id="1e6e9-106">Fiziksel olarak alınan satınalma siparişleri, stok kapatma raporu olan **Açık miktarları denetle** seçeneğinde görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="1e6e9-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="1e6e9-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="1e6e9-107">Resolution</span></span>

<span data-ttu-id="1e6e9-108">**Açık miktarları denetle** raporu, seçilen kapanış tarihi itibariyle, mali olarak güncelleştirilmiş stok girişlerinde kapatılamayan çıkış hareketlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e6e9-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="1e6e9-109">Fiziksel girişleri rapora dahil etmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1e6e9-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="1e6e9-110">Bu durumda, kapatılamayan çıkış hareketlerini kapsayabiliyorlarsa fiziksel girişler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1e6e9-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="1e6e9-111">Daha fazla bilgi için bkz. [Stok kapatma işlemini çalıştırmaya hazırlanma](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="1e6e9-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
