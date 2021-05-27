---
title: Değişiklik talep ettikten sonra bir satınalma talebine satır ekleyemezsiniz
description: Sistem, değişiklik talep ettikten sonra bir satınalma talebine satır eklemenize izin vermez.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchReqTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: jeyao
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5dbb55a6a352a7acf16729c1cfe1afdac2e2eef8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026988"
---
# <a name="you-cant-add-a-line-to-a-purchase-requisition-after-you-request-a-change"></a><span data-ttu-id="dd920-103">Değişiklik talep ettikten sonra bir satınalma talebine satır ekleyemezsiniz</span><span class="sxs-lookup"><span data-stu-id="dd920-103">You can't add a line to a purchase requisition after you request a change</span></span>

<span data-ttu-id="dd920-104">KB numarası: 4611211</span><span class="sxs-lookup"><span data-stu-id="dd920-104">KB number: 4611211</span></span>

## <a name="symptoms"></a><span data-ttu-id="dd920-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="dd920-105">Symptoms</span></span>

<span data-ttu-id="dd920-106">Sistem, değişiklik talep ettikten sonra bir satınalma talebine satır eklemenize izin vermez.</span><span class="sxs-lookup"><span data-stu-id="dd920-106">The system doesn't allow you to add a line to a purchase requisition after you request a change.</span></span>

## <a name="resolution"></a><span data-ttu-id="dd920-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="dd920-107">Resolution</span></span>

<span data-ttu-id="dd920-108">İş akışını geri çağırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="dd920-108">You must recall the workflow.</span></span> <span data-ttu-id="dd920-109">Satınalma talebi *Taslak* durumunda olduktan sonra, düzenleme işlemine veya satır eklemeye devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd920-109">After the purchase requisition is in *Draft* status, you can continue to edit it or add a line to it.</span></span>
