---
title: Deyimleri hesaplamak için işi yapılandır ve çalıştır
description: Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri oluşturmak ve hesaplamak için yinelenen toplu işleri çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 973236acca0cb8c0d57171e4bb9d4daaa7faaf38
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416459"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="87507-103">Deyimleri hesaplamak için işi yapılandır ve çalıştır</span><span class="sxs-lookup"><span data-stu-id="87507-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87507-104">Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri oluşturmak ve hesaplamak için yinelenen toplu işleri çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar.</span><span class="sxs-lookup"><span data-stu-id="87507-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="87507-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="87507-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="87507-106">Tüm çalışma alanları > Mağaza mali öğeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="87507-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="87507-107">Ekstreleri hesapla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="87507-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="87507-108">Belirli bir mağaza seçin veya mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="87507-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="87507-109">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="87507-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="87507-110">Arka planda çalıştır sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="87507-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="87507-111">Toplu işlem altında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="87507-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="87507-112">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="87507-112">Click Recurrence.</span></span>
6. <span data-ttu-id="87507-113">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="87507-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="87507-114">Başlangıç saati alanına saati girin.</span><span class="sxs-lookup"><span data-stu-id="87507-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="87507-115">Bitiş tarihi yok seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="87507-115">Select the No end date option.</span></span>
9. <span data-ttu-id="87507-116">PatternUnit alanına 'Gün' girin.</span><span class="sxs-lookup"><span data-stu-id="87507-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="87507-117">Dönem alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="87507-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="87507-118">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="87507-118">Click OK.</span></span>
12. <span data-ttu-id="87507-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="87507-119">Click OK.</span></span>

