---
title: Tek bir girişte birden fazla çalışma başlığı için yalnızca bir etiket yazdırılıyor
description: Tek bir girişte birden fazla çalışma başlığı için yalnızca bir etiket yazdırılıyor.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026982"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="9cee3-103">Tek bir girişte birden fazla çalışma başlığı için yalnızca bir etiket yazdırılıyor</span><span class="sxs-lookup"><span data-stu-id="9cee3-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="9cee3-104">KB numarası: 4614667</span><span class="sxs-lookup"><span data-stu-id="9cee3-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="9cee3-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="9cee3-105">Symptoms</span></span>

<span data-ttu-id="9cee3-106">Tek bir ambar uygulaması alma olayının parçası olarak aynı hedef plaka için birden fazla iş üstbilgisi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cee3-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="9cee3-107">Ancak, ürün alındığında yalnızca bir plaka etiketi yazdırılır.</span><span class="sxs-lookup"><span data-stu-id="9cee3-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="9cee3-108">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="9cee3-108">Resolution</span></span>

<span data-ttu-id="9cee3-109">Sistem, beklendiği şekilde davranıyordur.</span><span class="sxs-lookup"><span data-stu-id="9cee3-109">The system is behaving as designed.</span></span>

<span data-ttu-id="9cee3-110">Geçerli tasarımda, varolan çalışma başlığı ve iş satırı birleşimlerinin sayısına bakmaksızın, her zaman tek bir plaka etiketi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="9cee3-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="9cee3-111">Oluşturulan etiket, yalnızca bir birleşimin bilgilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="9cee3-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="9cee3-112">Bu soruna geçici bir çözüm olarak, iş üstbilgi oluşturmanın her zaman tek bir hedef plakaya eşlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="9cee3-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>
