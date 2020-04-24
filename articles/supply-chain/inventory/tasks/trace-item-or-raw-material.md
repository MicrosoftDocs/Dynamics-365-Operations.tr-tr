---
title: Maddeyi veya hammaddeyi izleme
description: Bu yordam, ürünlerin veya hammaddelerin kullanılmış veya kullanılmakta olduğunu belirlemek amacıyla ürün izleme işlevinin nasıl kullanılacağını gösterir.
author: pjacobse
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c39d34773a2b36cbf9477e4bdda8e45491d9c03
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213918"
---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="00805-103">Maddeyi veya hammaddeyi izleme</span><span class="sxs-lookup"><span data-stu-id="00805-103">Trace an item or raw material</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00805-104">Bu yordam, ürünlerin veya hammaddelerin kullanılmış veya kullanılmakta olduğunu belirlemek amacıyla ürün izleme işlevinin nasıl kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00805-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="00805-105">Bu yordamı kullanarak, bir ürünü belirleyebilir, kaynağına kadar izleyebilir ve sonra ürünün üretiminden satışına kadar olan ileriye yönelik izleme işlemleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00805-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="00805-106">Bu işlem, ilişkili müşterileri, satış siparişlerini ve daha fazlasını araştırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="00805-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="00805-107">Bu yordam, USP2 demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="00805-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="00805-108">Bilinen bir toplu iş numarası kullanarak bir ürünü geriye doğru izleme</span><span class="sxs-lookup"><span data-stu-id="00805-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="00805-109">**Gezinti panosu**'nda, **Modüller > Stok yönetimi > Sorgular ve raporlar > İzleme boyutları > Madde izleme**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="00805-109">In the **Navigation pane**, go to **Modules > Inventory management > Inquiries and reports > Tracking dimensions > Item tracing**.</span></span>
2. <span data-ttu-id="00805-110">**Madde numarası** alanında 'P9100' seçin.</span><span class="sxs-lookup"><span data-stu-id="00805-110">In the **Item number** field, select 'P9100'.</span></span>
3. <span data-ttu-id="00805-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00805-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="00805-112">**İleriye doğru veya Geriye doğru** alanında 'Geriye doğru'yu seçin.</span><span class="sxs-lookup"><span data-stu-id="00805-112">In the **Forward or backward** field, select 'Backward'.</span></span>
5. <span data-ttu-id="00805-113">**Toplu iş numarası** alanında '12-344-01' olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="00805-113">In the **Batch number** field, select 'as-12-344-01'.</span></span>
6. <span data-ttu-id="00805-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00805-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="00805-115">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00805-115">Click **OK**.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="00805-116">Bir ürünü tanımlama, ileriye doğru izleme ve analizini yapma</span><span class="sxs-lookup"><span data-stu-id="00805-116">Identify an item, trace it forward, and make an analysis</span></span>

<span data-ttu-id="00805-117">Ağacının en üst düğümü seçilen ürün ve toplu işe yönelik eldeki ürün miktarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00805-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="00805-118">İleriye doğru iz üzerinde yürütülmesi gereken maddeyi bulmak için ağaç düğümlerini genişletmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="00805-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="00805-119">Ağaçta 'Aşağıda açıklanan düğümler ve son düğümü seç' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="00805-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    
    <span data-ttu-id="00805-120">Genişletin: ' P9100 / 1 / 10 / olarak-12-344-01 2 ● ● 7.00 gal  \P9100 Çekildi satış siparişi 000072 ● ● 22/12/2015 ● ●-1 keg ● ●-4.00 gal keg Site = 1, ambar = 10, toplu iş numarası olarak-12-344-01  \P9100 ● B-000050 ● üretim 12/9/2015● 7 keg ● ● 27.00 gal = Site = 1, ambar = 10, toplu iş numarası olarak-12-344-01 ● yan ürünler =: P9101' ve bu düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="00805-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="00805-121">Ağaçta 'Aşağıda açıklanan düğüm ve bu düğümü seç' seçeneğini genişletin.</span><span class="sxs-lookup"><span data-stu-id="00805-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    
    <span data-ttu-id="00805-122">Yalnızca seçtiğiniz düğümünden başlayan genişletin ' M9103 ● B-000050 ● 9/12/2015 ● üretim satırı-160.00 lb ● boyutu = 70, renk Tamam, Site = = 1, ambar = 10, toplu iş numarası App01 =' ve bu düğümü seçin.</span><span class="sxs-lookup"><span data-stu-id="00805-122">Starting from the node that you've just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="00805-123">**İzleme başlangıç düğümü**'nü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00805-123">Click **Trace from node**.</span></span>
4. <span data-ttu-id="00805-124">**İleri**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="00805-124">Click **Forward**.</span></span>
5. <span data-ttu-id="00805-125">**Eylem Bölmesi**'nde **İzleme** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00805-125">On the **Action Pane**, click **Tracing**.</span></span>
    
    <span data-ttu-id="00805-126">İzlemekte olduğunuz madde tarafından etkilenen müşteriler ve gönderilmiş ve gönderilmemiş bu maddeyle ilgili satış siparişleri hakkında bilgi veren birkaç izleme seçeneği vardır.</span><span class="sxs-lookup"><span data-stu-id="00805-126">There are several tracing options which provide information about the customers impacted by the item that you're tracing, and the sales orders related to the item which have and haven't been shipped.</span></span>   
6. <span data-ttu-id="00805-127">**Müşteriler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00805-127">Click **Customers**.</span></span>
7. <span data-ttu-id="00805-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="00805-128">Close the page.</span></span>
8. <span data-ttu-id="00805-129">**Eylem Bölmesi**'nde **İzleme** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00805-129">On the **Action Pane**, click **Tracing**.</span></span>
9. <span data-ttu-id="00805-130">**Sevk edilmiş satış siparişleri**'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="00805-130">Click **Shipped sales orders**.</span></span>
10. <span data-ttu-id="00805-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="00805-131">Close the page.</span></span>

