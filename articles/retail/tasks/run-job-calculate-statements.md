--- 
title: "Deyimleri hesaplamak için işi yapılandır ve çalıştır"
description: "Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri oluşturmak ve hesaplamak için yinelenen toplu işleri çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar."
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
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="c7bdf-103">Deyimleri hesaplamak için işi yapılandır ve çalıştır</span><span class="sxs-lookup"><span data-stu-id="c7bdf-103">Configure and run job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c7bdf-104">Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri oluşturmak ve hesaplamak için yinelenen toplu işleri çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="c7bdf-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c7bdf-106">All workspaces > Retail store financials (Tüm çalışma alanları > Perakende mağaza finansmanları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="c7bdf-107">Ekstreleri hesapla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="c7bdf-108">Belirli bir mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="c7bdf-109">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="c7bdf-110">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="c7bdf-111">Toplu işlem altında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="c7bdf-112">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-112">Click Recurrence.</span></span>
6. <span data-ttu-id="c7bdf-113">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="c7bdf-114">Başlangıç saati alanına saati girin.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="c7bdf-115">Bitiş tarihi yok seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-115">Select the No end date option.</span></span>
9. <span data-ttu-id="c7bdf-116">PatternUnit alanına 'Gün' girin.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="c7bdf-117">Dönem alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="c7bdf-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-118">Click OK.</span></span>
12. <span data-ttu-id="c7bdf-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c7bdf-119">Click OK.</span></span>


