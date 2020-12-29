---
title: Üretim emirlerini serbest bırakma
description: Serbest bırakılmış bir üretim emri, üretim için yetkilendirilmiş bir emirdir. Serbest bırakılmış terimi, üretim emri yaşam döngüsünde, üretim emrinin üretim atölye katında uygulamaya geçirilmeye ve ambar işlemlerine hazır olduğu bir durumu ifade eder.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc6d53fc87bac2e23c0d1e67954be02749042004
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439576"
---
# <a name="release-production-orders"></a><span data-ttu-id="6a5ea-104">Üretim emirlerini serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="6a5ea-104">Release production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a5ea-105">Serbest bırakılmış bir üretim emri, üretim için yetkilendirilmiş bir emirdir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-105">A released production order is an order that has been authorized for production.</span></span> <span data-ttu-id="6a5ea-106">Serbest bırakılmış terimi, üretim emri yaşam döngüsünde, üretim emrinin üretim atölye katında uygulamaya geçirilmeye ve ambar işlemlerine hazır olduğu bir durumu ifade eder.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-106">The term Released is used to describe a state in the production order life cycle, where the production order is available for execution on the production shop floor and for warehouse processes.</span></span> 

<a name="characteristics-of-the-released-state"></a><span data-ttu-id="6a5ea-107">Serbest durumu özellikleri</span><span class="sxs-lookup"><span data-stu-id="6a5ea-107">Characteristics of the Released state</span></span>
-------------------------------------

<span data-ttu-id="6a5ea-108">**Serbest** durumu, üretim emri yaşam döngüsündeki bir durumdur.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-108">The **Released** state is one state in the production order life cycle.</span></span> <span data-ttu-id="6a5ea-109">**Serbest** durumundaki üretim siparişleri, üretim atölyesinde işleme konma ve ambar işlemleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-109">Production orders that are in the **Released** state are available for execution on the production shop floor and for warehouse processes.</span></span> <span data-ttu-id="6a5ea-110">**Serbest** durumu aşağıdaki özelliklere sahiptir:</span><span class="sxs-lookup"><span data-stu-id="6a5ea-110">The **Released** state has the following characteristics:</span></span>

-   <span data-ttu-id="6a5ea-111">Bir üretim emrinin durumu üretim emrinden veya bir toplu iş işlemi kullanılarak **Serbest** olarak değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-111">A production order can be changed to the **Released** state either from the production order or by using a batch process.</span></span> <span data-ttu-id="6a5ea-112">Üretim emri, **Master plan** sayfasındaki **Kesinleştirme zaman dilimi** alanı kullanılarak kesinleştirilmiş planlı üretim emirlerinden otomatik olarak güncellenebilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-112">The production order can also be updated automatically from planned production orders that are firmed by using the **Firming time fence** field on the **Master plan** page.</span></span>
-   <span data-ttu-id="6a5ea-113">**Serbest** durumu, atölye operatörleri (operatörler) için üretim işlerinin atölyede işleme konması için bir sinyaldir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-113">The **Released** state is the signal for the shop floor operators (operators) to start executing the production jobs on the shop floor.</span></span>
-   <span data-ttu-id="6a5ea-114">Rota kartları, rota işleri ve iş kartları gibi üretim evrakı, üretim işleri hakkında bilgi sağlar ve yayınlanabilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-114">Production papers, such as route cards, route jobs, and jobs cards provide information about production jobs and can be issued.</span></span>
-   <span data-ttu-id="6a5ea-115">Fiziksel olarak rezerve edilmiş malzemelerde, üretim emri için malzeme çekmek üzere ambar çalışması üretilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-115">For materials that are physically reserved, warehouse work is generated to pick materials for the production order.</span></span>

## <a name="releasing-jobs-to-the-shop-floor"></a><span data-ttu-id="6a5ea-116">İşleri atölyeye serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="6a5ea-116">Releasing jobs to the shop floor</span></span>
<span data-ttu-id="6a5ea-117">Bir üretim emri serbest bırakıldıktan sonra, siparişle ilgili üretim işleri görünür ve kayda hazır durumdadır.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-117">After a production order is released, production jobs that are related to the order are visible and ready for registration.</span></span> <span data-ttu-id="6a5ea-118">İşleçler **İş kartı terminali** veya **İş kartı cihazı** sayfasında Başlatma, Durdurma ve Tamamlama gibi iş kayıtları yapabilirler.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-118">The operators can make job registrations, such as Start, Stop, and Completion, on either the **Job card terminal** page or the **Job card device** page.</span></span> <span data-ttu-id="6a5ea-119">Kaydedilen süre ve miktar, harcanan süre ve miktarın izlenmesi için otomatik olarak kayıt sayfalarından üretim günlüklerine transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-119">The registered time and quantity are automatically transferred from the registration pages to production journals to keep track of the consumed time and quantity.</span></span>

## <a name="route-cards"></a><span data-ttu-id="6a5ea-120">Rota kartları</span><span class="sxs-lookup"><span data-stu-id="6a5ea-120">Route cards</span></span>
<span data-ttu-id="6a5ea-121">Rota kartı, rota ve operasyon ayarları ve operasyon ve iş çizelgeleme yöntemlerinden gelen bilgiler için bir genel bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-121">A route card provides an overview of information that comes from route and operation setups, and from operation and job scheduling methods.</span></span>

## <a name="route-jobs"></a><span data-ttu-id="6a5ea-122">Rotadaki işler</span><span class="sxs-lookup"><span data-stu-id="6a5ea-122">Route jobs</span></span>
<span data-ttu-id="6a5ea-123">Bir rota işi, bir operasyonun her işini ayrıntılı olarak listeler ve kurulum, işlem, kuyruk ve taşıma sürelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-123">A route job lists each job of an operation in detail, and includes setup, process, queue, and transportation times.</span></span> <span data-ttu-id="6a5ea-124">Örneğin, boyama gibi bir operasyon kurulum, çalışma süresi (boyama işlemi için) ve kuyruk süresi (kurutma için) gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-124">For example, an operation such as painting might require individual jobs, such as setup time, run time for the painting process, and queue time for drying.</span></span>

## <a name="job-cards"></a><span data-ttu-id="6a5ea-125">İş kartları</span><span class="sxs-lookup"><span data-stu-id="6a5ea-125">Job cards</span></span>
<span data-ttu-id="6a5ea-126">Bir iş kartı, belirli bir operasyonun tek tek iş numaralarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-126">A job card lists the individual job numbers of a particular operation.</span></span> <span data-ttu-id="6a5ea-127">Her sayfada bir iş görünür.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-127">One job appears on each page.</span></span> <span data-ttu-id="6a5ea-128">Bir iş kartına dahil olan işler ve tahmini süreleri rotadan ve operasyon kurulum bilgilerinden gelir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-128">The jobs that are included on a job card, and their estimated times, come from the route and operation setup information.</span></span> <span data-ttu-id="6a5ea-129">Bir iş kartından, **Üretim günlüğü satırları**, **iş kartı** sayfasını açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-129">From a job card, you can open the **Production journal lines**, **job card** page.</span></span> <span data-ttu-id="6a5ea-130">Operasyon kaynaklarını çalıştıran kişiler üretim sürecinde geri bildirim sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-130">People who run operations resources can provide feedback about the production process.</span></span> <span data-ttu-id="6a5ea-131">Bunlar, tüketim istatistikleri ve hata miktarı gibi bilgileri girebileceğiniz alanlardır.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-131">There are fields where you can enter consumption statistics and information such as the error quantity.</span></span>

## <a name="warehouse-work-for-raw-material-picking"></a><span data-ttu-id="6a5ea-132">Hammadde çekmek için ambar çalışması</span><span class="sxs-lookup"><span data-stu-id="6a5ea-132">Warehouse work for raw material picking</span></span>
<span data-ttu-id="6a5ea-133">Hammadde çekme işi, serbest bırakma sırasında üretilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-133">Work for raw material picking is generated during release.</span></span> <span data-ttu-id="6a5ea-134">İş yalnızca sipariş serbest bırakılmadan önce üretim emri için fiziksel olarak rezerve edilmiş olan miktarda malzeme için üretilir.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-134">Work is generated only for the quantity of materials that was physically reserved for the production order before the order was released.</span></span> <span data-ttu-id="6a5ea-135">Aşağıdaki kurulum hammadde çekme için ambar oluşturma işi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="6a5ea-135">The following setup is required to generate warehouse work for raw material picking:</span></span>

-   <span data-ttu-id="6a5ea-136">Hammadde çekmeye yönelik ve malzemelerin çekileceği ambar konumunu belirleyen bir konum yönergesi</span><span class="sxs-lookup"><span data-stu-id="6a5ea-136">A location directive for raw materials picking that determines which warehouse location to pick the materials in</span></span>
-   <span data-ttu-id="6a5ea-137">Hammaddeler için, ambar çalışmasının yürütülmesine yönelik politikaların yapılandırıldığı bir dalga şablonu</span><span class="sxs-lookup"><span data-stu-id="6a5ea-137">A wave template for raw materials, where policies for the execution of warehouse work are configured</span></span>
-   <span data-ttu-id="6a5ea-138">Malzemelerin koyulacağı yeri belirleyen bir üretim girdisi konumu</span><span class="sxs-lookup"><span data-stu-id="6a5ea-138">A production input location that determines where materials are put</span></span>




