---
title: "Açılım için izlemeyi kullanma"
description: "Bu makalede, bir siparişi açılımının sonucu arkasındaki nedenleri keşfetmek için izlemeyi nasıl kullanabileceğiniz açıklanmaktadır."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f3891688542ac6d4f9afce026808c65992a592d4
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="use-tracing-for-explosion"></a><span data-ttu-id="b3b7b-103">Açılım için izlemeyi kullanma</span><span class="sxs-lookup"><span data-stu-id="b3b7b-103">Use tracing for explosion</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b3b7b-104">Bu makalede, bir siparişi açılımının sonucu arkasındaki nedenleri keşfetmek için izlemeyi nasıl kullanabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="b3b7b-105">İzlemeyi etkinleştirerek, belirli bir siparişin açılım sonucuna katkıda bulunan faktörler hakkında bilgiyi görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="b3b7b-106">Aşağıdaki örnekler, izleme bilgisini nasıl kullanabileceğinizi gösterir:</span><span class="sxs-lookup"><span data-stu-id="b3b7b-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="b3b7b-107">Tedarik zinciri ve stok rezervasyonlarını optimize etmek için planlı siparişler üzerindeki eylemler arasındaki ilişkileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="b3b7b-108">Önceden onaylanmış siparişlere olan ilişkileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="b3b7b-109">Türetilmiş gereksinimleri otomatik kesinleştirmeye odaklanabilirsiniz ve sonra siparişlere daha doğru bir şekilde öncelik verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="b3b7b-110">Planlama parametrelerinin uygun olup olmadığını belirlemek için planlama sonuçları simüle edin.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="b3b7b-111">Üretim tarihleri, miktarları ve sipariş öncelikleri gibi bilgilerin nasıl belirlendiğini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="b3b7b-112">Seçili sipariş hakkındaki vadeli işlem ve eylem ayrıntılarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="b3b7b-113">**Açılım** sayfası üzerinde bilgi izleme, **Açıklama** sekmesinin üst bölmesinden edinilebilir.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="b3b7b-114">Bir siparişi açtığınızda izleme oluşur.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="b3b7b-115">Sipariş için izlemeyi başlatmak için **Güncelleştirme**'ye tıklayın ve sonra **İzlemeyi etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="b3b7b-116">**Metin bul** alanını kullanarak günlükteki belirli bilgileri arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="b3b7b-117">Arama sonuçları ağaçta vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-117">Search results are highlighted in the tree.</span></span>

<a name="see-also"></a><span data-ttu-id="b3b7b-118">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b3b7b-118">See also</span></span>
--------

[<span data-ttu-id="b3b7b-119">Master planlar</span><span class="sxs-lookup"><span data-stu-id="b3b7b-119">Master plans</span></span>](master-plans.md)




