--- 
title: " Ekstreleri hesaplamak için işi yapılandırma ve çalıştırma"
description: "Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri oluşturmak ve hesaplamak için yinelenen toplu işleri çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7bc936cdba771d322676565c2615ad75649cc50b
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="3e01f-103"> Ekstreleri hesaplamak için işi yapılandırma ve çalıştırma</span><span class="sxs-lookup"><span data-stu-id="3e01f-103">Configure and run a job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3e01f-104">Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri oluşturmak ve hesaplamak için yinelenen toplu işleri çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar.</span><span class="sxs-lookup"><span data-stu-id="3e01f-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="3e01f-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3e01f-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="3e01f-106">All workspaces > Retail store financials (Tüm çalışma alanları > Perakende mağaza finansmanları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="3e01f-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="3e01f-107">Ekstreleri hesapla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e01f-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="3e01f-108">Belirli bir mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="3e01f-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="3e01f-109">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e01f-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="3e01f-110">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e01f-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="3e01f-111">Toplu işlem altında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3e01f-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="3e01f-112">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e01f-112">Click Recurrence.</span></span>
6. <span data-ttu-id="3e01f-113">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="3e01f-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="3e01f-114">Başlangıç saati alanına saati girin.</span><span class="sxs-lookup"><span data-stu-id="3e01f-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="3e01f-115">Bitiş tarihi yok seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="3e01f-115">Select the No end date option.</span></span>
9. <span data-ttu-id="3e01f-116">PatternUnit alanına 'Gün' girin.</span><span class="sxs-lookup"><span data-stu-id="3e01f-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="3e01f-117">Dönem alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3e01f-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="3e01f-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e01f-118">Click OK.</span></span>
12. <span data-ttu-id="3e01f-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e01f-119">Click OK.</span></span>


