--- 
title: "Deyimleri nakletmek için işi yapılandır ve çalıştır"
description: "Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri deftere nakletmek için yinelenen toplu işi çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar."
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="14ebd-103">Deyimleri nakletmek için işi yapılandır ve çalıştır</span><span class="sxs-lookup"><span data-stu-id="14ebd-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="14ebd-104">Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri deftere nakletmek için yinelenen toplu işi çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar.</span><span class="sxs-lookup"><span data-stu-id="14ebd-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="14ebd-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="14ebd-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="14ebd-106">Tüm çalışma alanları > ..</span><span class="sxs-lookup"><span data-stu-id="14ebd-106">Go to All workspaces > ..</span></span> <span data-ttu-id="14ebd-107">> Perakende mağazası mali öğeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="14ebd-107">> Retail store financials.</span></span>
2. <span data-ttu-id="14ebd-108">Ekstreleri deftere naklet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14ebd-108">Click Post statements.</span></span>
    * <span data-ttu-id="14ebd-109">Bir kuruluş hiyerarşisi seçin ve kuruluş düğümleri ağacından tek bir mağaza veya bir düğüm seçin.</span><span class="sxs-lookup"><span data-stu-id="14ebd-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="14ebd-110">Bir mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="14ebd-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="14ebd-111">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14ebd-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="14ebd-112">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14ebd-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="14ebd-113">Toplu işlem onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="14ebd-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="14ebd-114">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14ebd-114">Click Recurrence.</span></span>
6. <span data-ttu-id="14ebd-115">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="14ebd-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="14ebd-116">Başlangıç saati alanına saati girin.</span><span class="sxs-lookup"><span data-stu-id="14ebd-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="14ebd-117">Yinelemenin belirli bir çalıştırma sayısı sonunda mı, belirli bir tarihte mi sonlandırılacağını yoksa hiçbir zaman sonlandırılmayacağını mı belirtin.</span><span class="sxs-lookup"><span data-stu-id="14ebd-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="14ebd-118">Ardından işin ne sıklıkta çalıştırılacağını belirtmek için çeşitli seçenekleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="14ebd-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="14ebd-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14ebd-119">Click OK.</span></span>
9. <span data-ttu-id="14ebd-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14ebd-120">Click OK.</span></span>


