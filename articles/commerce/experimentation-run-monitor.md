---
title: Deneme çalıştırma ve izleme
description: Bu konuda, üçüncü taraf bir hizmette deneme çalıştırma ve izlemenin nasıl yapılacağı anlatılmaktadır. Ayrıca deneme başlatıldıktan sonra varyasyonlarda nasıl değişiklik yapılacağı da açıklanmaktadır.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4cb7d863d9d69612aa0c340099c1f7861c9d12ba
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930307"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="a5a57-104">Deneme çalıştırma ve izleme</span><span class="sxs-lookup"><span data-stu-id="a5a57-104">Run and monitor an experiment</span></span>

<span data-ttu-id="a5a57-105">Bu konu, üçüncü taraf bir uygulamada denemelerinizin nasıl çalıştırılacağını ve izleneceğini ve gerekirse varyasyonların nasıl değiştirileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="a5a57-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="a5a57-106">Bu konudaki adımları tamamlamadan önce denemenizi Commerce'ta [yayımlamanız](experimentation-preview-publish.md) gerekir.</span><span class="sxs-lookup"><span data-stu-id="a5a57-106">Before you complete the steps in this topic, you'll need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> <span data-ttu-id="a5a57-107">Aşağıdaki diyagramda, Dynamics 365 Commerce'taki bir e-Ticaret web sitesinde deneme ayarlama ve çalıştırmayla ilgili tüm adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a5a57-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a5a57-108">Ek adımlar ayrı konularda ele alınmıştır.</span><span class="sxs-lookup"><span data-stu-id="a5a57-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="a5a57-109">[ ![Deneme kullanıcı yolculuğu - Çalıştırma ve İzleme](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="a5a57-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="a5a57-110">Varyasyonlarınızı yayımladıktan sonra, Commerce'ta denemenizi çalıştırmak için yapmanız gereken tüm adımlar gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a5a57-110">After you publish your variations, all the steps you need to do in Commerce to run your experiment are done.</span></span> <span data-ttu-id="a5a57-111">Sonraki adım, bir sayfa istediklerinde her kullanıcıya hangi varyasyonun gösterileceğini belirlemektir.</span><span class="sxs-lookup"><span data-stu-id="a5a57-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="a5a57-112">Üçüncü taraf hizmeti bu belirlemeyi yapar ancak önce hizmet içinde denemeyi etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a5a57-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="a5a57-113">Deneme etkinleştirme adımları hizmetler arasında farklılık gösterdiğinden, hizmetiniz veya sağlayıcınızla birlikte gelen yönergeleri izlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a5a57-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="a5a57-114">Deneme etkinleştirilmemişse, kullanıcılar yalnızca sayfanın varsayılan sürümünü görürler - hiçbir varyasyon görüntülenmez.</span><span class="sxs-lookup"><span data-stu-id="a5a57-114">If the experiment is not activated, users will only see the default version of the page - no variations will be displayed.</span></span>

<span data-ttu-id="a5a57-115">İstatistiksel olarak geçerli sonuçlar için veri toplamak amacıyla denemeyi uzun süre çalışır durumda tutmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a5a57-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="a5a57-116">Deneme çalışırken, denemeyle ilgili verileri ve analizleri izlemek için üçüncü taraf hizmetini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a5a57-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="a5a57-117">Varyasyonlarınızı ayarlama</span><span class="sxs-lookup"><span data-stu-id="a5a57-117">Adjust your variations</span></span>
<span data-ttu-id="a5a57-118">Herhangi bir nedenle varyasyonlarınızı değiştirmeniz gerekirse, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="a5a57-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5a57-119">Commerce veya üçüncü taraf hizmetindeki canlı bir denemede değişiklik yaparsanız, sonuçlarınız önemli ölçüde etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="a5a57-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="a5a57-120">Denemenin çalışmaya devam etmesine izin verin ve sonra büyük değişiklikler için yeni bir deneme oluşturmayı deneyin.</span><span class="sxs-lookup"><span data-stu-id="a5a57-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="a5a57-121">Site oluşturucuda **Denemeler** sekmesine gidin ve denemeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a5a57-121">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
1. <span data-ttu-id="a5a57-122">Açılan menüden güncelleştirmek istediğiniz varyasyonu seçin.</span><span class="sxs-lookup"><span data-stu-id="a5a57-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="a5a57-123">Gerekli değişiklikleri yapın, sonra da varyasyonları önizleyin ve yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="a5a57-123">Make needed changes, then preview and publish the variations.</span></span> <span data-ttu-id="a5a57-124">Daha fazla bilgi için, bkz. [Denemeyi önizleme ve yayımlama](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="a5a57-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="a5a57-125">Bir denemenin kurulumuyla ilgili değişiklikler yapmak için üçüncü taraf hizmetine gidin.</span><span class="sxs-lookup"><span data-stu-id="a5a57-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="a5a57-126">Önceki adım</span><span class="sxs-lookup"><span data-stu-id="a5a57-126">Previous step</span></span>
[<span data-ttu-id="a5a57-127">Deneme önizleme ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="a5a57-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="a5a57-128">Sonraki adım</span><span class="sxs-lookup"><span data-stu-id="a5a57-128">Next step</span></span>
[<span data-ttu-id="a5a57-129">Varyasyon yükseltme ve denemeyi tamamlama</span><span class="sxs-lookup"><span data-stu-id="a5a57-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)