--- 
title: " Ekstreleri deftere nakletmek için işi yapılandırma ve çalıştırma"
description: "Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri deftere nakletmek için yinelenen toplu işi çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0e2dae54cc9ccfc0a85046c5478e539585c3744d
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="5511f-103"> Ekstreleri deftere nakletmek için işi yapılandırma ve çalıştırma</span><span class="sxs-lookup"><span data-stu-id="5511f-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5511f-104">Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri deftere nakletmek için yinelenen toplu işi çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar.</span><span class="sxs-lookup"><span data-stu-id="5511f-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="5511f-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5511f-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="5511f-106">Tüm çalışma alanları > ..</span><span class="sxs-lookup"><span data-stu-id="5511f-106">Go to All workspaces > ..</span></span> <span data-ttu-id="5511f-107">> Perakende mağazası mali öğeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="5511f-107">> Retail store financials.</span></span>
2. <span data-ttu-id="5511f-108">Ekstreleri deftere naklet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5511f-108">Click Post statements.</span></span>
    * <span data-ttu-id="5511f-109">Bir kuruluş hiyerarşisi seçin ve kuruluş düğümleri ağacından tek bir mağaza veya bir düğüm seçin.</span><span class="sxs-lookup"><span data-stu-id="5511f-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="5511f-110">Bir mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="5511f-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="5511f-111">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5511f-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="5511f-112">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5511f-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="5511f-113">Toplu işlem onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="5511f-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="5511f-114">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5511f-114">Click Recurrence.</span></span>
6. <span data-ttu-id="5511f-115">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="5511f-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="5511f-116">Başlangıç saati alanına saati girin.</span><span class="sxs-lookup"><span data-stu-id="5511f-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="5511f-117">Yinelemenin belirli bir çalıştırma sayısı sonunda mı, belirli bir tarihte mi sonlandırılacağını yoksa hiçbir zaman sonlandırılmayacağını mı belirtin.</span><span class="sxs-lookup"><span data-stu-id="5511f-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="5511f-118">Ardından işin ne sıklıkta çalıştırılacağını belirtmek için çeşitli seçenekleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="5511f-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="5511f-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5511f-119">Click OK.</span></span>
9. <span data-ttu-id="5511f-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5511f-120">Click OK.</span></span>


