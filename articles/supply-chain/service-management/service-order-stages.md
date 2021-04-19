---
title: Servis siparişi aşamaları
description: Servis siparişi aşamalarını tanımlayarak ve bunları çalışanlara atayarak, servis kuruluşundaki çeşitli kişilerin gerçekleştirdiği görevler üzerinden servis siparişi akışını kontrol edersiniz.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d4bb43c8f59a0ef55963ac9b453491a6112b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817521"
---
# <a name="service-order-stages"></a><span data-ttu-id="6b719-103">Servis siparişi aşamaları</span><span class="sxs-lookup"><span data-stu-id="6b719-103">Service order stages</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="6b719-104">Tamamlanması gereken görevleri, hangi sırayla tamamlanacaklarını ve bunları tamamlamakla sorumlu çalışanları tanımlamak servis siparişi aşamaları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b719-104">You can set up stages for a service order to define the tasks that must be completed, the order in which they are completed, and the workers who are responsible for completing them.</span></span> <span data-ttu-id="6b719-105">Servis siparişi aşamalarını tanımlayarak ve bunları çalışanlara atayarak, servis kuruluşundaki çeşitli kişilerin gerçekleştirdiği görevler üzerinden servis siparişi akışını kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b719-105">By defining the stages for a service order and assigning them to workers, you can control the flow of a service order through the tasks that various people perform in the service organization.</span></span> <span data-ttu-id="6b719-106">Aşamaların sırası bir başlangıç aşaması içermelidir.</span><span class="sxs-lookup"><span data-stu-id="6b719-106">The sequence of stages must include an initial stage.</span></span>

<span data-ttu-id="6b719-107">Ayrıca her aşama için izin verilen eylemleri tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b719-107">You can also define the actions that are permitted at each stage.</span></span> <span data-ttu-id="6b719-108">Örneğin, son aşama haricindeki tüm aşamalar için **Deftere naklet** onay kutusu seçimini kaldırırsanız, servis siparişlerinin servis siparişleri tüm aşamalarla işlenmeden önce deftere nakledilmesini önlemiş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="6b719-108">For example, if you clear the **Post** check box for all stages except the final stage, you prevent any service orders from being posted before the service orders are processed through the complete sequence of stages.</span></span>

## <a name="branching-in-service-order-stages"></a><span data-ttu-id="6b719-109">Servis siparişi aşamaları içinde dallara ayırma</span><span class="sxs-lookup"><span data-stu-id="6b719-109">Branching in service order stages</span></span>

<span data-ttu-id="6b719-110">Bir servis aşaması ayarladığınızda, daha sonraki servis aşaması için seçebileceğiniz birden çok seçenek ya da dal ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b719-110">When you set up a service stage, you can create multiple options, or branches, to select from for the next service stage.</span></span> <span data-ttu-id="6b719-111">Oluşturduğunuz tüm dallar ilk aşama tamamlandıktan sonra seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="6b719-111">All the branches that you create are available to select from when the initial stage is completed.</span></span> <span data-ttu-id="6b719-112">Örneğin, başlangıç aşaması olarak **Planlama**'yı ayarladınız.</span><span class="sxs-lookup"><span data-stu-id="6b719-112">For example, you set up **Planning** as an initial stage.</span></span> <span data-ttu-id="6b719-113">**İşlemde** ve **İptal** adında iki aşama oluşturdunuz ve **Planlama**'yı bunların üst öğesi olacak şekilde seçtiniz.</span><span class="sxs-lookup"><span data-stu-id="6b719-113">You create two stages named **In process** and **Cancel**, and then select **Planning** as the parent for them.</span></span> <span data-ttu-id="6b719-114">**Planlama** aşamasını satış siparişine atadınız.</span><span class="sxs-lookup"><span data-stu-id="6b719-114">You assign the **Planning** stage to sales order.</span></span> <span data-ttu-id="6b719-115">Satış siparişi için planlama aşaması tamamlandığında, satış siparişi üzerinde çalışmak için hazırsa **İşlemde** aşamasını ya da satış siparişi iptal edildiyse **İptal** aşamasını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6b719-115">When the planning stage for the sales order is completed, you can select the **In process** stage if the sales order is ready to work on, or you can select the **Cancel** stage if the sales order is canceled.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b719-116">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="6b719-116">See also</span></span>

[<span data-ttu-id="6b719-117">Servis siparişi aşamalarını ayarla</span><span class="sxs-lookup"><span data-stu-id="6b719-117">Set up service order stages</span></span>](set-up-service-order-stages.md)

[<span data-ttu-id="6b719-118">Servis siparişi aşamasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="6b719-118">Change the service order stage</span></span>](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]