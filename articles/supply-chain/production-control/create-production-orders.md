---
title: "Üretim emirleri oluşturma"
description: "Üretim emri oluşturulunca, madde imalatını başlatmak için bir talepte bulunulur. Üretim emri neyin ne kadar üretileceği ve planlanan bitiş tarihi hakkındaki bilgileri içerir. Ayrıca, maddeyi üretmek için tüketilecek malzemeler ve izlenecek süreç hakkında bilgiler de içerir."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d962dbf5a5a4e3847252171d3631f78341640bc7
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="create-production-orders"></a><span data-ttu-id="16c8d-105">Üretim emirleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="16c8d-105">Create production orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="16c8d-106">Üretim emri oluşturulunca, madde imalatını başlatmak için bir talepte bulunulur.</span><span class="sxs-lookup"><span data-stu-id="16c8d-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="16c8d-107">Üretim emri neyin ne kadar üretileceği ve planlanan bitiş tarihi hakkındaki bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="16c8d-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="16c8d-108">Ayrıca, maddeyi üretmek için tüketilecek malzemeler ve izlenecek süreç hakkında bilgiler de içerir.</span><span class="sxs-lookup"><span data-stu-id="16c8d-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="16c8d-109">Bir üretim emri, üretim döngüsü aşamalarından geçer.</span><span class="sxs-lookup"><span data-stu-id="16c8d-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="16c8d-110">Bir emir oluşturulduğunda, durumu **Oluşturulmuş** olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="16c8d-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="16c8d-111">Bir emir tamamlandığında, durumu **Sonlandırılmış** olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="16c8d-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="16c8d-112">Her aşamada bulunan bir parametre ayarı, kullanıcının tüm adımları yapılandırmasına izin verir.</span><span class="sxs-lookup"><span data-stu-id="16c8d-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="16c8d-113">Bu ayar, tek bir kullanıcı veya tüm kullanıcılar için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="16c8d-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="16c8d-114">Üretim ürün reçetesi ve üretim rotası, üretim emrinin ana varlıklarıdır.</span><span class="sxs-lookup"><span data-stu-id="16c8d-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="16c8d-115">Bunlar, üretilmek için seçilen öğeye ve miktarına dayalı olarak üretim emrine kopyalanırlar.</span><span class="sxs-lookup"><span data-stu-id="16c8d-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="16c8d-116">Üretim emri başlamadan önce üretim ürün reçeteleri ve rotaları düzenlenebilir.</span><span class="sxs-lookup"><span data-stu-id="16c8d-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="16c8d-117">Üretim emri aşağıdaki senaryolarda oluşturulabilir:</span><span class="sxs-lookup"><span data-stu-id="16c8d-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="16c8d-118">Malzeme talebine göre ana planlama yürütme tarafından oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="16c8d-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="16c8d-119">Bir satış siparişi satırından ya da üst düzey bir üretim emri oluşturulduğunda ve (pegged tedarik) tahmini doğrudan oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="16c8d-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="16c8d-120">El ile oluşturulmuş.</span><span class="sxs-lookup"><span data-stu-id="16c8d-120">Created manually.</span></span>





