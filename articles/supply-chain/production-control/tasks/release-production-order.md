---
title: Üretim emrini serbest bırakma
description: Bu prosedürde bir üretim emrinin nasıl verildiği gösterilmektedir.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 917fe1ef826c9b112be29ebce78ebd750652db64
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "345088"
---
# <a name="release-a-production-order"></a><span data-ttu-id="06209-103">Üretim emrini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="06209-103">Release a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06209-104">Bu prosedürde bir üretim emrinin nasıl verildiği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="06209-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="06209-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="06209-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="06209-106">Bu, üretim emri yaşam döngüsünü açıklayan yedi prosedürün dördüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="06209-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="06209-107">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="06209-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="06209-108">Kılavuzda, Planlandı durumundaki bir üretim emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="06209-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="06209-109">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06209-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="06209-110">Serbest bırak öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06209-110">Click Release.</span></span>
    * <span data-ttu-id="06209-111">Bu sayfada, seçilen üretim emirleri aralığının serbest bırakılmasını onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06209-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="06209-112">Siparişler eklemek istiyorsanız Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06209-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="06209-113">Serbest bırakma adımı, bire üretim siparişinin üretim atölyesine serbest bırakıldığını, böylece atölye operatörlerinin üretim işleri üzerindeki ilerlemeyi raporlayabileceklerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="06209-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="06209-114">İşleri işleme hakkında ilgili bilgiler içeren üretim kağıtları verilebilir.</span><span class="sxs-lookup"><span data-stu-id="06209-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="06209-115">Hammadde çekme için ambar işi, ambar işlemi için ayarlanan öğeler için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="06209-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="06209-116">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06209-116">Click the General tab.</span></span>
    * <span data-ttu-id="06209-117">Hangi üretim raporlarının yazdırılacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="06209-117">Select which production reports should be printed.</span></span> <span data-ttu-id="06209-118">İş kartı raporu, her bir iş için birer sayfa yazdırır ve proje düzeyinde planlanacak üretim emri gerektirir.</span><span class="sxs-lookup"><span data-stu-id="06209-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="06209-119">Rapor, planlanan başlangıç ve bitiş saati, üretilecek miktar ve işi yürütecek kaynaklar hakkında bilgiler içerir.</span><span class="sxs-lookup"><span data-stu-id="06209-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="06209-120">Rota işi raporu, aynı sayfadaki aynı bilgileri toplar, ancak her iş için bir sayfa yazdırmaz.</span><span class="sxs-lookup"><span data-stu-id="06209-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="06209-121">Rota kartı raporu yalnızca işlemleri gösterir; işleri göstermez.</span><span class="sxs-lookup"><span data-stu-id="06209-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="06209-122">Bu nedenle, bu rapor iş planlaması gerektirmez, ancak, üretim emirleri işlem düzeyinde planlandığı zaman kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="06209-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="06209-123">Rota kartını yazdır onay kutusuna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06209-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="06209-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06209-124">Click OK.</span></span>
7. <span data-ttu-id="06209-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="06209-125">Close the page.</span></span>

