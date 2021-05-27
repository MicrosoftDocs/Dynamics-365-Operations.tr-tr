---
title: Birden fazla kalite emri oluşturulduğunda, Son test tarihi alanı güncelleştirilmiyor
description: Birden fazla kalite emri oluşturulduğunda, Son test tarihi alanı güncelleştirilmiyor.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026994"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a><span data-ttu-id="ad7dc-103">Birden fazla kalite emri oluşturulduğunda, Son test tarihi alanı güncelleştirilmiyor</span><span class="sxs-lookup"><span data-stu-id="ad7dc-103">The Last tested date field isn't updated when multiple quality orders are created</span></span>

<span data-ttu-id="ad7dc-104">KB numarası: 4612803</span><span class="sxs-lookup"><span data-stu-id="ad7dc-104">KB number: 4612803</span></span>

## <a name="symptoms"></a><span data-ttu-id="ad7dc-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="ad7dc-105">Symptoms</span></span>

<span data-ttu-id="ad7dc-106">Birden fazla kalite emri oluşturulduğunda, **Son test tarihi** alanı güncelleştirilmiyor.</span><span class="sxs-lookup"><span data-stu-id="ad7dc-106">The **Last tested date** field isn't updated when multiple quality orders are created.</span></span>

## <a name="resolution"></a><span data-ttu-id="ad7dc-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="ad7dc-107">Resolution</span></span>

<span data-ttu-id="ad7dc-108">Sistem, beklendiği şekilde davranıyordur.</span><span class="sxs-lookup"><span data-stu-id="ad7dc-108">The system is behaving as designed.</span></span> <span data-ttu-id="ad7dc-109">Son test tarihi, kalite emirleriyle ilgili değildir.</span><span class="sxs-lookup"><span data-stu-id="ad7dc-109">The last tested date isn't related to quality orders.</span></span> <span data-ttu-id="ad7dc-110">Tamamlanan malların ilk olarak satın alındığı veya üretildiği tarihi depolar.</span><span class="sxs-lookup"><span data-stu-id="ad7dc-110">It stores the date when the finished goods were first purchased or manufactured.</span></span> <span data-ttu-id="ad7dc-111">Bu tarih, önerilen raf ömrü tarihini hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ad7dc-111">This date is used to calculate the shelf life advice date.</span></span>
