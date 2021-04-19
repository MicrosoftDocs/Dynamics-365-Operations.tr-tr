---
title: Deyimleri nakletmek için işi yapılandır ve çalıştır
description: Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri deftere nakletmek için yinelenen toplu işi çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar.
author: josaw1
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52baa707c36f3468263782dc8ec735e44af88e38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804245"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="22987-103">Deyimleri nakletmek için işi yapılandır ve çalıştır</span><span class="sxs-lookup"><span data-stu-id="22987-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22987-104">Bu yordam, seçili bir mağaza veya mağaza grubuna ilişkin ekstreleri deftere nakletmek için yinelenen toplu işi çalıştırma ve yapılandırmayla ilgili açıklamalar sağlar.</span><span class="sxs-lookup"><span data-stu-id="22987-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="22987-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="22987-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="22987-106">Tüm çalışma alanları > ..</span><span class="sxs-lookup"><span data-stu-id="22987-106">Go to All workspaces > ..</span></span> <span data-ttu-id="22987-107">> Mağaza mali öğeleri.</span><span class="sxs-lookup"><span data-stu-id="22987-107">> Store financials.</span></span>
2. <span data-ttu-id="22987-108">Ekstreleri toplu işle deftere naklet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="22987-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="22987-109">Bir kuruluş hiyerarşisi seçin ve kuruluş düğümleri ağacından tek bir mağaza veya bir düğüm seçin.</span><span class="sxs-lookup"><span data-stu-id="22987-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="22987-110">Bir mağaza grubu için toplu iş oluşturmak istiyorsanız bir düğüm belirtin.</span><span class="sxs-lookup"><span data-stu-id="22987-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="22987-111">Seçiminizi eklemek için oka tıklayın.</span><span class="sxs-lookup"><span data-stu-id="22987-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="22987-112">Arka plan sekmesinde Çalıştır'a tıklayın. ![Arka planda çalıştır](../dev-itpro/media/runbackground.png "Arka planda çalıştır")</span><span class="sxs-lookup"><span data-stu-id="22987-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="22987-113">Toplu işlem onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="22987-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="22987-114">![Toplu İşlem](../dev-itpro/media/batchprocessing.png "Toplu İşlem ve yineleme")</span><span class="sxs-lookup"><span data-stu-id="22987-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="22987-115">Yineleme'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="22987-115">Click Recurrence.</span></span>
6. <span data-ttu-id="22987-116">Başlangıç tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="22987-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="22987-117">Başlangıç saati alanına saati girin.</span><span class="sxs-lookup"><span data-stu-id="22987-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="22987-118">Yinelemenin belirli bir çalıştırma sayısı sonunda mı, belirli bir tarihte mi sonlandırılacağını yoksa hiçbir zaman sonlandırılmayacağını mı belirtin.</span><span class="sxs-lookup"><span data-stu-id="22987-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="22987-119">Ardından işin ne sıklıkta çalıştırılacağını belirtmek için çeşitli seçenekleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="22987-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="22987-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="22987-120">Click OK.</span></span>
9. <span data-ttu-id="22987-121">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="22987-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]