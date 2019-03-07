---
title: Hub konsolidasyonu kullanarak yükleri planlama
description: Bu makalede aynı müşteriye farklı ambarlardan ürün teslim ederken veya ürünler farklı satıcılardan aynı ambara teslim edilirken sevkiyatları bir hub'da konsolide etme özelliği açıklanmaktadır.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6743338819da3821cde18ec34a9c79290036ca23
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "339959"
---
# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="b5b7b-103">Hub konsolidasyonu kullanarak yükleri planlama</span><span class="sxs-lookup"><span data-stu-id="b5b7b-103">Plan loads using hub consolidation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5b7b-104">Bu makalede aynı müşteriye farklı ambarlardan ürün teslim ederken veya ürünler farklı satıcılardan aynı ambara teslim edilirken sevkiyatları bir hub'da konsolide etme özelliği açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="b5b7b-105">Aynı müşteriye farklı ambarlardan ürün teslim ederken veya ürünler farklı satıcılardan aynı ambara teslim edilirken sevkiyatları bir hub'da konsolide etmek yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="b5b7b-106">Yük oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5b7b-106">Building loads</span></span>
<span data-ttu-id="b5b7b-107">Hub konsolidasyonu özelliğini kullanabilmek için **Taşıma yönetimi parametreleri** sayfasında **Transit planlamada** seçeneğini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="b5b7b-108">Ayrıca konsolidasyonun gerçekleşeceği hub'ları da oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="b5b7b-109">Aşağıdaki diyagramda bir hub konsolidasyonu örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="b5b7b-110">Bu örnekte, farklı ambarlardan alınan satış siparişleri aynı müşteriye gönderilecek.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="b5b7b-111">Temel yükler satış siparişlerine göre her zamanki yöntemle, **Yük planlama çalışma ekranı** sayfasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="b5b7b-112">İki yükü müşteriye teslim edilmeden önce bir hub'da konsolide etmek için, **Yük planlama çalışma ekranı** sayfasında, **Taşıma** alanında **Hub konsolidasyonu** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="b5b7b-113">Her yük için doğru hub'ı seçtiğinizde, yüklerin "bırakma" hedefi olarak bu hub görünür.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="b5b7b-114">Ayrıca **Yük planlama çalışma ekranı** sayfasındaki **Arz ve Talep** bölümünde iki "taşıma talebi satırı" bulunur.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="b5b7b-115">Bundan sonra bu iki satırı yeni bir yüke ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="b5b7b-116">Bu yeni yük iki satış siparişi satırını da içerir ve "alma" adresi olarak hub "bırakma" hedefi olarak da müşteri A görünür.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="b5b7b-117">Üç yük bundan sonra derecelendirilmeye ve diğer yükler gibi rotalarının belirlenmesine hazırdır.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="b5b7b-118">Her yük için sistemin önerdiği sevkiyat taşıyıcısını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="b5b7b-119">[![Hub konsolidasyonu](./media/hubconsol.jpg)](./media/hubconsol.jpg) Aynı yöntemi birden çok transfer emrine ait yükleri konsolide etmek için de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="b5b7b-120">Bu örnekte, önceki diyagramdaki müşteri A ambardır.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="b5b7b-121">Alternatif olarak yüklerin farklı satıcılardan aynı ambara teslim edildiği, birden fazla satınalma emrine ilişkin yükleri de konsolide edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="b5b7b-122">Birden fazla konsolidasyon hub'ı oluşturabilir ve farklı ambarlardan gelen daha fazla yük için birden fazla hub'ı konsolide edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="b5b7b-123">Temel yüklerinizi oluşturup hub konsolidasyon seçeneğini kullandıktan sonra, konsolide edilmiş taşıma istekleri satırını kullanarak yeni yükler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="b5b7b-124">Bundan sonra yüklerinizi derecelendirebilir ve rotalarını belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b5b7b-124">You then rate and route your loads.</span></span>



