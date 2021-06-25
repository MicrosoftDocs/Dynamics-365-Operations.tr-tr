---
title: Açılım için izlemeyi kullanma
description: Bu makalede, bir siparişi açılımının sonucu arkasındaki nedenleri keşfetmek için izlemeyi nasıl kullanabileceğiniz açıklanmaktadır.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19231
ms.assetid: 9bc9bfbe-a7a9-437b-a947-826229b0585a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75d994db80071c4ef9e23caf24cb4cadbc1473ad
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189904"
---
# <a name="use-tracing-for-explosion"></a><span data-ttu-id="79ff4-103">Açılım için izlemeyi kullanma</span><span class="sxs-lookup"><span data-stu-id="79ff4-103">Use tracing for explosion</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79ff4-104">Bu makalede, bir siparişi açılımının sonucu arkasındaki nedenleri keşfetmek için izlemeyi nasıl kullanabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="79ff4-104">This article explains how you can use tracing to explore the causes behind the outcome of an order explosion.</span></span>

<span data-ttu-id="79ff4-105">İzlemeyi etkinleştirerek, belirli bir siparişin açılım sonucuna katkıda bulunan faktörler hakkında bilgiyi görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79ff4-105">By enabling tracing, you can view information about the factors that contributed to the outcome of the explosion of a particular order.</span></span> <span data-ttu-id="79ff4-106">Aşağıdaki örnekler, izleme bilgisini nasıl kullanabileceğinizi gösterir:</span><span class="sxs-lookup"><span data-stu-id="79ff4-106">The following examples show how you can use the tracing information:</span></span>

-   <span data-ttu-id="79ff4-107">Tedarik zinciri ve stok rezervasyonlarını optimize etmek için planlı siparişler üzerindeki eylemler arasındaki ilişkileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="79ff4-107">View relations between the actions on planned orders to optimize the supply chain and inventory reservations.</span></span>
-   <span data-ttu-id="79ff4-108">Önceden onaylanmış siparişlere olan ilişkileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="79ff4-108">View relations to orders that are already approved.</span></span> <span data-ttu-id="79ff4-109">Türetilmiş gereksinimleri otomatik kesinleştirmeye odaklanabilirsiniz ve sonra siparişlere daha doğru bir şekilde öncelik verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79ff4-109">You can focus on automatically firming derived requirements and then prioritize orders more accurately.</span></span>
-   <span data-ttu-id="79ff4-110">Planlama parametrelerinin uygun olup olmadığını belirlemek için planlama sonuçları simüle edin.</span><span class="sxs-lookup"><span data-stu-id="79ff4-110">Simulate planning results to determine whether the planning parameters are optimal.</span></span>
-   <span data-ttu-id="79ff4-111">Üretim tarihleri, miktarları ve sipariş öncelikleri gibi bilgilerin nasıl belirlendiğini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="79ff4-111">Identify how information such as production dates, quantities, and priorities for an order were determined.</span></span>

<span data-ttu-id="79ff4-112">Seçili sipariş hakkındaki vadeli işlem ve eylem ayrıntılarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79ff4-112">You can view details about futures and actions for a selected order.</span></span> <span data-ttu-id="79ff4-113">**Açılım** sayfası üzerinde bilgi izleme, **Açıklama** sekmesinin üst bölmesinden edinilebilir.</span><span class="sxs-lookup"><span data-stu-id="79ff4-113">On the **Explosion** page, tracing information is available on the **Explanation** tab in the upper pane.</span></span> <span data-ttu-id="79ff4-114">Bir siparişi açtığınızda izleme oluşur.</span><span class="sxs-lookup"><span data-stu-id="79ff4-114">Tracing occurs when you explode an order.</span></span> <span data-ttu-id="79ff4-115">Sipariş için izlemeyi başlatmak için **Güncelleştirme**'ye tıklayın ve sonra **İzlemeyi etkinleştir** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="79ff4-115">To start tracing for the order, click **Update**, and then select the **Enable trace** check box.</span></span> <span data-ttu-id="79ff4-116">**Metin bul** alanını kullanarak günlükteki belirli bilgileri arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79ff4-116">You can use the **Find text** field to search the log for specific information.</span></span> <span data-ttu-id="79ff4-117">Arama sonuçları ağaçta vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="79ff4-117">Search results are highlighted in the tree.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79ff4-118">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="79ff4-118">Additional resources</span></span>

[<span data-ttu-id="79ff4-119">Master planlara genel bakış</span><span class="sxs-lookup"><span data-stu-id="79ff4-119">Master plans overview</span></span>](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]