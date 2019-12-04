---
title: Açılım için izlemeyi kullanma
description: Bu makalede, bir siparişi açılımının sonucu arkasındaki nedenleri keşfetmek için izlemeyi nasıl kullanabileceğiniz açıklanmaktadır.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f2821eb6a17d2caaacf399f8d519e4caf3ecd04
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813673"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="f7fbb-103">Açılım için izlemeyi kullanma</span><span class="sxs-lookup"><span data-stu-id="f7fbb-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7fbb-104">Bu makalede, bir siparişi açılımının sonucu arkasındaki nedenleri keşfetmek için izlemeyi nasıl kullanabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="f7fbb-105">İzlemeyi etkinleştirerek, belirli bir siparişin açılım sonucuna katkıda bulunan faktörler hakkında bilgiyi görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="f7fbb-106">Aşağıdaki örnekler, izleme bilgisini nasıl kullanabileceğinizi gösterir:</span><span class="sxs-lookup"><span data-stu-id="f7fbb-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="f7fbb-107">Tedarik zinciri ve stok rezervasyonlarını optimize etmek için planlı siparişler üzerindeki eylemler arasındaki ilişkileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="f7fbb-108">Önceden onaylanmış siparişlere olan ilişkileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="f7fbb-109">Türetilmiş gereksinimleri otomatik kesinleştirmeye odaklanabilirsiniz ve sonra siparişlere daha doğru bir şekilde öncelik verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="f7fbb-110">Planlama parametrelerinin uygun olup olmadığını belirlemek için planlama sonuçları simüle edin.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="f7fbb-111">Üretim tarihleri, miktarları ve sipariş öncelikleri gibi bilgilerin nasıl belirlendiğini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="f7fbb-112">Seçili sipariş hakkındaki vadeli işlem ve eylem ayrıntılarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="f7fbb-113">**Açılım** sayfası üzerinde bilgi izleme, **Açıklama** sekmesinin üst bölmesinden edinilebilir.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="f7fbb-114">Bir siparişi açtığınızda izleme oluşur.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="f7fbb-115">Sipariş için izlemeyi başlatmak için **Güncelleştirme**'ye tıklayın ve sonra **İzlemeyi etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="f7fbb-116">**Metin bul** alanını kullanarak günlükteki belirli bilgileri arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="f7fbb-117">Arama sonuçları ağaçta vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="f7fbb-117">Search results are highlighted in the tree.</span></span>

<a name="additional-resources"></a><span data-ttu-id="f7fbb-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f7fbb-118">Additional resources</span></span>
--------

[<span data-ttu-id="f7fbb-119">Master planlara genel bakış</span><span class="sxs-lookup"><span data-stu-id="f7fbb-119">Master plans overview</span></span>](master-plans.md)



