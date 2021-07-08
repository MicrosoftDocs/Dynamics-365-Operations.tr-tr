---
title: İptal edilen ürün girişleri hareket durumunu Kaydedildi olarak güncelleştirmez
description: Gelen yükteki ürün girişlerini iptal ettikten sonra, sistem stok hareket durumunu otomatik olarak Alındı yerine Sipariş Edildi olarak güncelleştirir.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294198"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="39309-103">İptal edilen ürün girişleri hareket durumunu Kaydedildi olarak güncelleştirmez</span><span class="sxs-lookup"><span data-stu-id="39309-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="39309-104">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="39309-104">Symptoms</span></span>

<span data-ttu-id="39309-105">Gelen yükteki **Ürün girişlerini iptal et** eylemini çalıştırdıktan sonra, sistem stok hareketlerinin durumunu otomatik olarak *Alındı* yerine *Sipariş Edildi* olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="39309-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="39309-106">Çözüm</span><span class="sxs-lookup"><span data-stu-id="39309-106">Resolution</span></span>

<span data-ttu-id="39309-107">Sevk irsaliyeleri giden yükler için iptal edildiğinde, stok hareketlerinin durumu *Çekildi* olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="39309-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="39309-108">Ancak, gelen yükten gelen ürün girişleri iptal edildiğinde, stok hareketlerinin durumu *Kayıtlı* durumuna geri döndürülmez.</span><span class="sxs-lookup"><span data-stu-id="39309-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="39309-109">Bu nedenle, gelen yükten gelen bir ürün girişi iptal edildikten sonra, ambar çalışanının madde miktarlarını yükler için yeniden kaydetmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="39309-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="39309-110">Daha fazla bilgi için bkz. [Bir gelen yükte gelen madde miktarlarını kaydetme](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="39309-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
