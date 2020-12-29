---
title: Servis siparişi aşamaları
description: Servis siparişi aşamalarını tanımlayarak ve bunları çalışanlara atayarak, servis kuruluşundaki çeşitli kişilerin gerçekleştirdiği görevler üzerinden servis siparişi akışını kontrol edersiniz.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bcb72e8222b378198fcd044428fa1a4a0e8944
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438982"
---
# <a name="service-order-stages"></a><span data-ttu-id="e2f82-103">Servis siparişi aşamaları</span><span class="sxs-lookup"><span data-stu-id="e2f82-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="e2f82-104">Tamamlanması gereken görevleri, hangi sırayla tamamlanacaklarını ve bunları tamamlamakla sorumlu çalışanları tanımlamak servis siparişi aşamaları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2f82-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="e2f82-105">Servis siparişi aşamalarını tanımlayarak ve bunları çalışanlara atayarak, servis kuruluşundaki çeşitli kişilerin gerçekleştirdiği görevler üzerinden servis siparişi akışını kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2f82-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="e2f82-106">Aşamaların sırası bir başlangıç aşaması içermelidir.</span><span class="sxs-lookup"><span data-stu-id="e2f82-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="e2f82-107">Ayrıca her aşama için izin verilen eylemleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2f82-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="e2f82-108">Örneğin, son aşama haricindeki tüm aşamalar için **Deftere naklet** onay kutusu seçimini kaldırırsanız, servis siparişlerinin servis siparişleri tüm aşamalarla işlenmeden önce deftere nakledilmesini önlemiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="e2f82-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="e2f82-109">Servis siparişi aşamaları içinde dallara ayırma</span><span class="sxs-lookup"><span data-stu-id="e2f82-109">Branching in service order stages</span></span>

<span data-ttu-id="e2f82-110">Bir servis aşaması ayarladığınızda, daha sonraki servis aşaması için seçebileceğiniz birden çok seçenek ya da dal ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2f82-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="e2f82-111">Oluşturduğunuz tüm dallar ilk aşama tamamlandıktan sonra seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="e2f82-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="e2f82-112">Örneğin, başlangıç aşaması olarak **Planlama**'yı ayarladınız.</span><span class="sxs-lookup"><span data-stu-id="e2f82-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="e2f82-113">**İşlemde** ve **İptal** adında iki aşama oluşturdunuz ve **Planlama**'yı bunların üst öğesi olacak şekilde seçtiniz.</span><span class="sxs-lookup"><span data-stu-id="e2f82-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="e2f82-114">**Planlama** aşamasını satış siparişine atadınız.</span><span class="sxs-lookup"><span data-stu-id="e2f82-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="e2f82-115">Satış siparişi için planlama aşaması tamamlandığında, satış siparişi üzerinde çalışmak için hazırsa **İşlemde** aşamasını ya da satış siparişi iptal edildiyse **İptal** aşamasını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e2f82-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2f82-116">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="e2f82-116">See also</span></span>

[<span data-ttu-id="e2f82-117">Servis siparişi aşamalarını ayarla</span><span class="sxs-lookup"><span data-stu-id="e2f82-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="e2f82-118">Servis siparişi aşamasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="e2f82-118">Change the service order stage</span></span>](change-service-order-stage.md)

  


