---
title: Kıymet kiralama kuralları
description: Bu konuda kiralanan kıymetlere yönelik kurallar anlatılmıştır.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ea89d54f1ce3a1e971d41623bf44f909f7dfdf09
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131311"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="f424c-103">Kıymet kiralama kuralları</span><span class="sxs-lookup"><span data-stu-id="f424c-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f424c-104">Bu konuda kiralanan kıymetlere yönelik kurallar anlatılmıştır.</span><span class="sxs-lookup"><span data-stu-id="f424c-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="f424c-105">Kiralama sözleşmeleri, bir kiralama defterinin başlangıç tarihini belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f424c-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="f424c-106">Kiralama kuralı **Yok** olarak ayarlanırsa, başlangıç tarihi kiralamanın başlangıç tarihiyle (diğer bir deyişle, **Kiralama başlangıç tarihi** alanının değeri) aynıdır.</span><span class="sxs-lookup"><span data-stu-id="f424c-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="f424c-107">Kiralama sözleşmesi **Tam ay** olarak ayarlanırsa, başlangıç tarihi, kiralamanın başlangıç tarihinin bulunduğu ayın ilk günüdür.</span><span class="sxs-lookup"><span data-stu-id="f424c-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="f424c-108">Başlangıç tarihi, borç amortismanı ve kıymet amortisman çizelgeleri için dönemin başlangıç tarihini belirler.</span><span class="sxs-lookup"><span data-stu-id="f424c-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="f424c-109">Faiz giderleri ve amortisman giderleri, ilgili çizelgelerin dönem bitiş tarihinde deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="f424c-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="f424c-110">İlk denklik ve ayarlama günlüğü girişi, başlangıç tarihinde deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="f424c-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="f424c-111">Kiralama kuralları özelliği, Özellik Yönetimi aracılığıyla açılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f424c-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="f424c-112">**Özellik yönetimi** çalışma alanında, **Varlık kiralama için kiralama kuralı** özelliği olarak adlandırılan özelliği bulup seçin ve **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f424c-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="f424c-113">Kiralama kuralları, kiralama varlığı defterinin kurulumuna atanır.</span><span class="sxs-lookup"><span data-stu-id="f424c-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="f424c-114">Kiralama sözleşmesini görüntülemek veya atamak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f424c-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="f424c-115">**Varlık kiralama \> Kurulum \> Kiralama defterleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f424c-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="f424c-116">**Kiralama kuraı** alanında, aşağıdaki değerlerden birini seçin.</span><span class="sxs-lookup"><span data-stu-id="f424c-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="f424c-117">Kiralama kuralı</span><span class="sxs-lookup"><span data-stu-id="f424c-117">Leasing convention</span></span> | <span data-ttu-id="f424c-118">Tanım</span><span class="sxs-lookup"><span data-stu-id="f424c-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="f424c-119">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="f424c-119">None</span></span>               | <span data-ttu-id="f424c-120">Borç amortismanı ve varlık amortisman çizelgeleri kiralamanın başlangıç tarihinde başlar çünkü başlangıç tarihi kiralamanın başlangıç tarihine eşittir.</span><span class="sxs-lookup"><span data-stu-id="f424c-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="f424c-121">Bitiş tarihi bir ay sonrasıdır.</span><span class="sxs-lookup"><span data-stu-id="f424c-121">The end date is one month later.</span></span> <span data-ttu-id="f424c-122">Bu kiralama kuralı, faizin her ayın son günü deftere nakledileceğini garanti etmez.</span><span class="sxs-lookup"><span data-stu-id="f424c-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="f424c-123">Tam ay</span><span class="sxs-lookup"><span data-stu-id="f424c-123">Full month</span></span>         | <span data-ttu-id="f424c-124">Ay içinde herhangi bir zamanda gerçekleşen bir başlangıç tarihi olan kiralamalar için, borç amortismanı ve varlık amortismanı çizelgeleri o ayın ilk gününde gider tahakkuk etmeye başlar.</span><span class="sxs-lookup"><span data-stu-id="f424c-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="f424c-125">Bu kiralama kuralı, faizin tüm ay boyunca her ayın son gününde tahakkuk ettirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="f424c-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="f424c-126">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f424c-126">Select **Save**.</span></span>

<span data-ttu-id="f424c-127">Bir kiralama oluşturulduğunda, her defterin başlangıç tarihi, kiralama için girilen başlangıç tarihine ve defter için belirtilen kiralama kuralına göre otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="f424c-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>
