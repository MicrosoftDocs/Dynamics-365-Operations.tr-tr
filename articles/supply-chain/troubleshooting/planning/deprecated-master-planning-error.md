---
title: Yerleşik master planlama altyapısını çalıştırırken bir hata alıyorsunuz
description: Kullanım dışı bırakılan yerleşik master planlama altyapısını çalıştırdığınızda bir hata iletisi alıyorsunuz.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: Dialog_ReqCalcScheduleItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c950292a4f43319d21a7deafdfb341b7bef15d8
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294201"
---
# <a name="you-receive-an-error-when-running-the-built-in-master-planning-engine"></a><span data-ttu-id="3b377-103">Yerleşik master planlama altyapısını çalıştırırken bir hata alıyorsunuz</span><span class="sxs-lookup"><span data-stu-id="3b377-103">You receive an error when running the built-in master planning engine</span></span>

<span data-ttu-id="3b377-104">Hata kodu: ReqCalcScheduleItemTablePlanningOptimizationFitError</span><span class="sxs-lookup"><span data-stu-id="3b377-104">Error code: ReqCalcScheduleItemTablePlanningOptimizationFitError</span></span>

## <a name="symptoms"></a><span data-ttu-id="3b377-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="3b377-105">Symptoms</span></span>

<span data-ttu-id="3b377-106">Master planlamayı kullanım dışı bırakılan yerleşik master planlama altyapısını kullanarak çalıştırdığınızda aşağıdaki hata iletisini alırsınız:</span><span class="sxs-lookup"><span data-stu-id="3b377-106">When you run master planning by using the deprecated built-in master planning engine, you receive the following error message:</span></span>

> <span data-ttu-id="3b377-107">Bu hata iletisini, yerleşik master planlama altyapısı Planlama İyileştirmesi tarafından desteklenen senaryolar için kullanıldığı için alırsınız.</span><span class="sxs-lookup"><span data-stu-id="3b377-107">You receive this error message because the built-in master planning engine was used for scenarios supported by Planning Optimization.</span></span> <span data-ttu-id="3b377-108">Geçerli yerleşik master planlama kullanım dışı bırakılacağından şimdi Planlama İyileştirmesi'ne geçiş yapmalısınız.</span><span class="sxs-lookup"><span data-stu-id="3b377-108">You should migrate to Planning Optimization now, as the current built-in master planning will be deprecated.</span></span> <span data-ttu-id="3b377-109">Bu master planlama çalıştırmasının başarıyla tamamladığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3b377-109">Note that this master planning run did complete successfully.</span></span> <span data-ttu-id="3b377-110">Geçişinizin beklemedeki özelliklere güçlü bağımlılıkları olması durumunda, yerleşik master planlama altyapısının sürekli kullanımı için bir özel durum isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3b377-110">In case your migration has strong dependencies on pending features, an exception to continued usage of the built-in master planning engine can be requested.</span></span> <span data-ttu-id="3b377-111">Başlamak için lütfen aşağıdaki anketi doldurun ve ilgili istek durumunda Planlamayı En İyi Duruma Getirme'ye geçişle ilgili özel bir durum isteyin.</span><span class="sxs-lookup"><span data-stu-id="3b377-111">Please complete the following questionnaire to get started and, if relevant, request an exception from migration to Planning Optimization.</span></span> [<span data-ttu-id="3b377-112">Planlamayı En İyi Duruma Getirme geçişi ve özel durum anketi</span><span class="sxs-lookup"><span data-stu-id="3b377-112">Planning Optimization migration and exception questionnaire</span></span>](https://go.microsoft.com/fwlink/?linkid=2144962)

## <a name="cause"></a><span data-ttu-id="3b377-113">Nedeni</span><span class="sxs-lookup"><span data-stu-id="3b377-113">Cause</span></span>

<span data-ttu-id="3b377-114">Planlamayı çalıştırırsanız ve üretim denetimi özelliklerini kullanmıyorsanız, Planlamayı En İyi Duruma Getirme'ye geçiş yapmayı düşünmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="3b377-114">If you run planning and don't use production control features, you should consider migrating to Planning Optimization.</span></span> <span data-ttu-id="3b377-115">Yerleşik master planlama altyapısı kullanımdan kaldırılıyor.</span><span class="sxs-lookup"><span data-stu-id="3b377-115">The built-in master planning engine is being deprecated.</span></span> <span data-ttu-id="3b377-116">Bu nedenle, hata iletisi almadan kullanmaya devam etmek istiyorsanız, Microsoft'a bir özel durum başvurusunda bulunmalısınız.</span><span class="sxs-lookup"><span data-stu-id="3b377-116">Therefore, if you want to continue to use it without receiving the error message, you must apply for an exception from Microsoft.</span></span>

## <a name="resolution"></a><span data-ttu-id="3b377-117">Çözüm</span><span class="sxs-lookup"><span data-stu-id="3b377-117">Resolution</span></span>

<span data-ttu-id="3b377-118">Planlamayı En İyi Duruma Getirme'ye geçiş yapma veya bunun yerine kullanımdan kaldırılan yerleşik planlama altyapısını kullanmaya devam edebilmeniz için özel durum başvurusu yapma hakkında daha fazla bilgi için bkz. [Master planlama için Planlamayı En İyi Duruma Getirmeye Geçiş](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span><span class="sxs-lookup"><span data-stu-id="3b377-118">For more information about how to migrate to Planning Optimization, or how to apply for an exception so that you can continue to use the deprecated built-in planning engine instead, see [Migration to Planning Optimization for master planning](/dynamics365/supply-chain/master-planning/new-master-planning-engine).</span></span>
