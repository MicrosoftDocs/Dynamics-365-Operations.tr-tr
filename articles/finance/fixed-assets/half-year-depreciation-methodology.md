---
title: Yarı yıl amortisman yöntemi
description: Bu konu, sabit kıymetlerin, bir kıymetin ilk ve son yılı sırasında altı aylık amortismanı hesaplayan yarı yıl kuralını kullanarak amortismanı hesaplamak için kullandığı yöntemi açıklamaktadır.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 55fb03cf08d8ec042aa8fb37fd1fb858d98279b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448675"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="c0e92-103">Yarı yıl amortisman yöntemi</span><span class="sxs-lookup"><span data-stu-id="c0e92-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c0e92-104">Bu konu, yarı yıl kuralını kullanarak amortismanı hesaplamak üzere sabit kıymetlerde kullanılan yöntemi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c0e92-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="c0e92-105">Yarım yıl kuralı, bir kıymetin ilk ve son yılındaki hizmeti için altı aylık amortismanı hesaplar.</span><span class="sxs-lookup"><span data-stu-id="c0e92-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="c0e92-106">Amortisman kuralları hakkında daha fazla bilgi için bkz. [Amortisman yöntemleri ve kuralları](Fixed-asset-depreciation-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="c0e92-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="c0e92-107">Altı aylık amortisman kuralını kullandığınızda, sistem kıymetin satın alındığı yılı veya servise verildiği yılı kullanır, sonra bu yıldan beş yıllık amortismanı hesaplar ve sonra altı ay ekler.</span><span class="sxs-lookup"><span data-stu-id="c0e92-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="c0e92-108">Bu süreci görmek için, 50.000'lik bir fiyata alınmış ve 2020 Nisan ayında servise sokulmuş bir varlık düşünün.</span><span class="sxs-lookup"><span data-stu-id="c0e92-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="c0e92-109">Ayrıca, kıymetin beş yıllık servis ömrüne sahip olduğunu varsayın.</span><span class="sxs-lookup"><span data-stu-id="c0e92-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="c0e92-110">İlk servis yılı Aralık 2020'de sona erer ve bu da kıymetin beş yıllık servis ömrünün bitişinin Aralık 2024 olacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="c0e92-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="c0e92-111">Yarım yıl amortisman kuralı, kıymetin ömrüne altı ay ekler, yani servis ömrü 2025 Haziran 'da sona erer.</span><span class="sxs-lookup"><span data-stu-id="c0e92-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="c0e92-112">Yıllık amortisman 50.000/5 = 10.000 ve aylık amortisman 10000/12 = 833,33</span><span class="sxs-lookup"><span data-stu-id="c0e92-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="c0e92-113">İlk yıl yıpranma 10.000/2 = 5.000 ve sonraki aylık amortisman 5.000/9 = 555,56</span><span class="sxs-lookup"><span data-stu-id="c0e92-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="c0e92-114">[![Yarım yıl amortisman kuralı için amortisman planı](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="c0e92-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="c0e92-115">Yarım yıl kuralı ile eklenen uzatılmış amortisman dönemleri, amortismanın daha doğru tahsisatını sağlar.</span><span class="sxs-lookup"><span data-stu-id="c0e92-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="c0e92-116">Altı aylık kural, amortisman giderlerini daha eşit şekilde temsil eder ve kar ve zarar raporunun bildirilmesinde yararlı olur.</span><span class="sxs-lookup"><span data-stu-id="c0e92-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>
