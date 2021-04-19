---
title: İş kimlikleri için birleşik numara serisi
description: Bu özellik, üretim denetimi, üretim yürütmesi, zaman ve katılımcı modülleri için iş kimlikleri oluşturan tek, Birleşik bir numara serisi sağlar.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824954"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="b336e-103">İş kimlikleri için birleşik numara serisi</span><span class="sxs-lookup"><span data-stu-id="b336e-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b336e-104">Bu özellik, üretim denetimi, üretim yürütmesi, zaman ve katılımcı modülleri için iş kimlikleri oluşturan tek, Birleşik bir numara serisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="b336e-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="b336e-105">Daha önce, bu modüllerin her biri için farklı bir numara serisi seçebiliyordunuz ve bu da sıraların iki ya da daha fazlası özdeş bir biçim kullandığında iş kimliklerinin çakışmasına neden olabiliyordu.</span><span class="sxs-lookup"><span data-stu-id="b336e-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="b336e-106">Bu tür bir çakışma veri bozulmasına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="b336e-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="b336e-107">Sisteminiz için bu özelliği etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b336e-107">Turn on this feature for your system</span></span>

<span data-ttu-id="b336e-108">Sisteminiz bu konuda açıklanan özelliği zaten içermiyorsa [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve *İş kimlikleri için birleşik numara serisi* özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="b336e-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="b336e-109">İş kimlikleri için birleşik numara serisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="b336e-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="b336e-110">Bu özellik etkinleştirildikten sonra, Üretim denetimi, üretim yürütmesi ve zaman ve katılımcı modülleri için parametreler sayfalarında bulunan varolan **iş tanımlayıcısı** numara serisi ayarları kullanım dışı bırakılır ve yeni bir **birleşik iş kodu** alanı eklenir.</span><span class="sxs-lookup"><span data-stu-id="b336e-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="b336e-111">**Birleşik iş kodu** değeri tüm modüllerin aynı numara serisine başvuruda bulunduğunu garanti ederek bu üç modül tarafından paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="b336e-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="b336e-112">Bu nedenle, iş kimlikleri tüm üç modülde benzersiz olacaktır ve bir çakışma hiçbir zaman gerçekleşmez.</span><span class="sxs-lookup"><span data-stu-id="b336e-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="b336e-113">İş kimlikleri için birleşik numara serisini ayarlamak için:</span><span class="sxs-lookup"><span data-stu-id="b336e-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="b336e-114">Bu özelliği önceki bölümde açıklandığı gibi açın.</span><span class="sxs-lookup"><span data-stu-id="b336e-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="b336e-115">Birleştirilmiş iş kimlikleriniz için kullanmak istediğiniz numara serisini tanımlayın veya yeni bir tane oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b336e-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="b336e-116">Daha fazla bilgi için bkz. [Numara serilerine genel bakış](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b336e-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="b336e-117">**Üretim Denetim parametreleri**, **Üretim yürütme parametreleri** veya **zaman ve katılımcı parametreleri** sayfasına gidin.</span><span class="sxs-lookup"><span data-stu-id="b336e-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="b336e-118">Hangisini seçtiğinizin bir önemi yoktur, çünkü bu ayarı bu sayfalardan herhangi birinde yaptığınızda, tüm diğer sayfalar otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b336e-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="b336e-119">Seçili parametreler sayfanızdaki **numara serileri** sekmesini açın.</span><span class="sxs-lookup"><span data-stu-id="b336e-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="b336e-120">Daha önce tanımladığınız **numara serisi kodunu** kılavuzun **Birleşik iş kimlikleri** satırına atayın.</span><span class="sxs-lookup"><span data-stu-id="b336e-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
