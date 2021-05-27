---
title: Talep tahmini kayıtlarını içe aktardığınızda, tahmin edilen birim maliyeti güncelleştiremezsiniz
description: Talep tahmin kayıtlarını içe aktarmak için veri varlıklarını kullandığınızda, mevcut kayıtların maliyet fiyatı, içe aktarılan verilerle eşleşmesi için güncelleştirilmez.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026987"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="c11cd-103">Talep tahmini kayıtlarını içe aktardığınızda, tahmin edilen birim maliyeti güncelleştiremezsiniz</span><span class="sxs-lookup"><span data-stu-id="c11cd-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="c11cd-104">KB numarası: 4614109</span><span class="sxs-lookup"><span data-stu-id="c11cd-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="c11cd-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="c11cd-105">Symptoms</span></span>

<span data-ttu-id="c11cd-106">Talep tahmin kayıtlarını içe aktarmak için veri varlıklarını kullandığınızda, mevcut kayıtların **Tahmin edilen birim maliyeti** değeri, içe aktarılan verilerle eşleşmesi için güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="c11cd-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="c11cd-107">Nedeni</span><span class="sxs-lookup"><span data-stu-id="c11cd-107">Cause</span></span>

<span data-ttu-id="c11cd-108">**Tahmin edilen birim maliyet** salt okunur bir alandır.</span><span class="sxs-lookup"><span data-stu-id="c11cd-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="c11cd-109">Değer, ürün birim maliyetine dayanır ve içe aktarma yoluyla doğrudan ayarlanamaz.</span><span class="sxs-lookup"><span data-stu-id="c11cd-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="c11cd-110">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="c11cd-110">Resolution</span></span>

<span data-ttu-id="c11cd-111">Alan salt okunur olduğundan, buraya değerleri aktaramazsınız.</span><span class="sxs-lookup"><span data-stu-id="c11cd-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="c11cd-112">Değer, mevcut iş mantığına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="c11cd-112">The value will be calculated according to the existing business logic.</span></span>
