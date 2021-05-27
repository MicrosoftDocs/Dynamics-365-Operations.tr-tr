---
title: Madde fiyatı sayfasının Etkin fiyatlar sekmesinde Başlangıç tarihi değeri yok
description: Madde fiyatı sayfasının Etkin fiyatlar sekmesinde Başlangıç tarihi değeri yok.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026998"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="c6f99-103">Madde fiyatı sayfasının Etkin fiyatlar sekmesinde Başlangıç tarihi değeri yok</span><span class="sxs-lookup"><span data-stu-id="c6f99-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="c6f99-104">KB numarası: 4613548</span><span class="sxs-lookup"><span data-stu-id="c6f99-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="c6f99-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="c6f99-105">Symptoms</span></span>

<span data-ttu-id="c6f99-106">**Madde fiyatı** sayfasının **Etkin fiyatlar** sekmesinde **Başlangıç tarihi** değeri yok.</span><span class="sxs-lookup"><span data-stu-id="c6f99-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="c6f99-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="c6f99-107">Resolution</span></span>

<span data-ttu-id="c6f99-108">Bekleyen fiyata ayarlanan **Başlangıç tarihi** değeri (geçerlilik tarihi) etkin fiyata transfer edilmedi.</span><span class="sxs-lookup"><span data-stu-id="c6f99-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="c6f99-109">Bir madde maliyeti kaydı ilk olarak girildiğinde *Bekleyen* durumunda olur ve amaçlanan yürürlük tarihi vardır.</span><span class="sxs-lookup"><span data-stu-id="c6f99-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="c6f99-110">Madde maliyeti kaydını etkinleştirdiğinizde, durumu *Etkin* olarak güncellenir ve yürürlük tarihini etkinleştirme tarihine güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c6f99-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="c6f99-111">Bu nedenle, etkin fiyatın etkinleştirme tarihi her zaman etkinleştirmenin gerçek tarihidir.</span><span class="sxs-lookup"><span data-stu-id="c6f99-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="c6f99-112">Daha fazla bilgi için bkz. [Maliyetlendirme sürümlerine genel bakış](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="c6f99-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
