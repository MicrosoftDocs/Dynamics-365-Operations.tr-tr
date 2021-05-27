---
title: Yeni bir lot kodu seçildiğinde toplu iş numarası temizlenir
description: Bir malzeme çekme listesi günlük satırını incelediğiniz zaman, Lot Kodu alanında yeni bir değer seçerseniz Toplu iş numarası alanındaki değer temizlenir.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026968"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="72f36-103">Yeni bir lot kodu seçildiğinde toplu iş numarası temizlenir</span><span class="sxs-lookup"><span data-stu-id="72f36-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="72f36-104">KB numarası: 4613107</span><span class="sxs-lookup"><span data-stu-id="72f36-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="72f36-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="72f36-105">Symptoms</span></span>

<span data-ttu-id="72f36-106">Bir malzeme çekme listesi günlük satırını incelediğiniz zaman, **Lot Kodu** alanında yeni bir değer seçerseniz **Toplu iş numarası** alanındaki değer temizlenir.</span><span class="sxs-lookup"><span data-stu-id="72f36-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="72f36-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="72f36-107">Resolution</span></span>

<span data-ttu-id="72f36-108">Sistem, beklendiği şekilde davranıyordur.</span><span class="sxs-lookup"><span data-stu-id="72f36-108">The system is behaving as designed.</span></span> <span data-ttu-id="72f36-109">Lot kodunu değiştirirseniz, madde bağlamını değiştirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72f36-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="72f36-110">Bu nedenle, toplu iş numarası sıfırlanır.</span><span class="sxs-lookup"><span data-stu-id="72f36-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="72f36-111">Toplu iş numarasını bir lot koduyla ilişkilendirmek için, önce lot kodunu ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="72f36-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
