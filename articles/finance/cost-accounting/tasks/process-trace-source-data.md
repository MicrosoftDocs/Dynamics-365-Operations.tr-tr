---
title: Kaynak verilerini işleme ve izleme
description: Tüm veri işleme işler tarafından yürütülür.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a23443c985ac681c8c31956ae5ea3e513337577
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4448945"
---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="f5e1f-103">Kaynak verilerini işleme ve izleme</span><span class="sxs-lookup"><span data-stu-id="f5e1f-103">Process and trace source data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5e1f-104">Tüm veri işleme işler tarafından yürütülür.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-104">All data processing is run by jobs.</span></span> <span data-ttu-id="f5e1f-105">Her bir iş ve veri sağlayıcı için geçerli işin işlendiği girişler ve işlemin çalıştırıldığı belge için bir günlük oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="f5e1f-106">Bir veri kaynağı kurmak için bu yordamı kullanın ve belirli maliyet girişinin kaynağını izleyin.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="f5e1f-107">Bu kayıt USP2 demo veri şirketini USP2 kullanır.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="f5e1f-108">Bu görevi tamamlamadan önce, aşağıdaki görev kılavuzlarını yürüttüğünüzden emin olun: "Bir maliyet muhasebesi defteri oluştur", "Maliyet kontrol birimleri tanımla" ve "Maliyet muhasebesi defteri için veri kaynağını yönet".</span><span class="sxs-lookup"><span data-stu-id="f5e1f-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="f5e1f-109">Maliyet muhasebesi > Genel muhasebe kurulumu > Maliyet muhasebesi defterleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="f5e1f-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f5e1f-111">Daha önce oluşturduğunuz maliyet muhasebesi defterini seçin.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="f5e1f-112">Güncel sürümler üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-112">Click Actual versions.</span></span>
4. <span data-ttu-id="f5e1f-113">Eylem Bölmesinde, Veri kaynağı işleme'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="f5e1f-114">Genel muhasebe girişi transfer günlükleri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="f5e1f-115">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f5e1f-116">Günlük girişleri üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-116">Click Journal entries.</span></span>
8. <span data-ttu-id="f5e1f-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f5e1f-118">Maliyet girişleri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-118">Click Cost entries.</span></span>
10. <span data-ttu-id="f5e1f-119">Kaynak girişi üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-119">Click Source entry.</span></span>
11. <span data-ttu-id="f5e1f-120">Eylem Bölmesinde, Veri kaynağı işleme'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="f5e1f-121">Genel muhasebe üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-121">Click General ledger.</span></span>
13. <span data-ttu-id="f5e1f-122">Mali takvim dönemi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="f5e1f-123">Bu örnekte, Mali 2017 Dönem 9'u seçin.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="f5e1f-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f5e1f-124">Click OK.</span></span>

