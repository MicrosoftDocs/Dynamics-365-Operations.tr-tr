---
title: Bir fiili ağırlık miktarı bölündüğünde, nominal miktar yerine minimum miktar kullanılıyor
description: Fiili ağırlık miktarı toplu işlemlere bölündüğünde, Malzeme çekme miktarı alanı, nominal miktarı değil madde için ayarlanan minimum miktarı kullanıyor.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026992"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="3ef53-103">Bir fiili ağırlık miktarı bölündüğünde, nominal miktar yerine minimum miktar kullanılıyor</span><span class="sxs-lookup"><span data-stu-id="3ef53-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="3ef53-104">KB numarası: 4612073</span><span class="sxs-lookup"><span data-stu-id="3ef53-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="3ef53-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="3ef53-105">Symptoms</span></span>

<span data-ttu-id="3ef53-106">Fiili ağırlık miktarı toplu işlemlere bölündüğünde, **Malzeme çekme miktarı** alanı, nominal miktarı değil madde için ayarlanan minimum miktarı kullanıyor.</span><span class="sxs-lookup"><span data-stu-id="3ef53-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="3ef53-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="3ef53-107">Resolution</span></span>

<span data-ttu-id="3ef53-108">Sistem, beklendiği şekilde davranıyordur.</span><span class="sxs-lookup"><span data-stu-id="3ef53-108">The system is behaving as designed.</span></span> <span data-ttu-id="3ef53-109">Sistem, her maddenin malzeme çekme için minimum miktar ayarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="3ef53-109">The system uses each item's minimum quantity setup for picking.</span></span>
