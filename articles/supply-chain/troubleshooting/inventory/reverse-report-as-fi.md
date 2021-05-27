---
title: Tamamlandı bildiriminin tersine çevrilmesi, beklenmedik bir açık hareket oluşturuyor
description: Tamamlandı bildiriminin tersine çevrilmesi, tersine çevrilmiş miktarın tersine çevrilmiş hareketle aynı stok boyutlarına sahip olduğu bir açık hareket oluşturur.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026995"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="266a7-103">Tamamlandı bildiriminin tersine çevrilmesi, beklenmedik bir açık hareket oluşturuyor</span><span class="sxs-lookup"><span data-stu-id="266a7-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="266a7-104">KB numarası: 4612469</span><span class="sxs-lookup"><span data-stu-id="266a7-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="266a7-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="266a7-105">Symptoms</span></span>

<span data-ttu-id="266a7-106">Tamamlandı bildirimini tersine çevirirseniz, sistem, tersine çevrilmiş miktarın tersine çevrilmiş hareketle aynı stok boyutlarına sahip olduğu bir açık hareket oluşturur.</span><span class="sxs-lookup"><span data-stu-id="266a7-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="266a7-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="266a7-107">Resolution</span></span>

<span data-ttu-id="266a7-108">Tamamlandı bildirimi işlemini tersine çevirdiğinizde, stok boyutu üretim günlüğünden başlatılır.</span><span class="sxs-lookup"><span data-stu-id="266a7-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="266a7-109">Bu nedenle, toplu iş numarasını alır.</span><span class="sxs-lookup"><span data-stu-id="266a7-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="266a7-110">İşaretleme nedeniyle, satış siparişi hareketleri toplu iş numarasını devralır.</span><span class="sxs-lookup"><span data-stu-id="266a7-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="266a7-111">Tamamlandı bildirimi deftere nakledildiğinde boyut sıfırlanabilir.</span><span class="sxs-lookup"><span data-stu-id="266a7-111">The dimension can be reset when the reporting as finished is posted.</span></span>
