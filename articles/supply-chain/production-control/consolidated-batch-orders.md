---
title: "Konsolide toplu iş emirleri"
description: "Bu makale konsolide edilen toplu siparişler kavramını açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3ca9c920ea333bd21defebc29b40243d3a618a3d
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="c307a-103">Konsolide toplu iş emirleri</span><span class="sxs-lookup"><span data-stu-id="c307a-103">Consolidated batch orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c307a-104">Bu makale konsolide edilen toplu siparişler kavramını açıklar.</span><span class="sxs-lookup"><span data-stu-id="c307a-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="c307a-105">Üretilen toplu ürün, ana ürün olarak değerlendirilirken, paketlenen bir ürün alt ürün olarak değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="c307a-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="c307a-106">Toplu ürün ile paketli ürün arasındaki ilişki bir toplu ürün dönüşümü cinsinden ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="c307a-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="c307a-107">Bu toplu öğe dönüşümü toplu öğenin kendisine tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="c307a-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="c307a-108">Paketlenmiş öğeler tek ünite olarak değerlendirilen, tek bir boyuttan veya birden fazla boyuttan meydana gelen konteynerlerde paketlenir.</span><span class="sxs-lookup"><span data-stu-id="c307a-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="c307a-109">Bir toplu ürün için siparişleri birleştirerek, tüm ilgili toplu siparişleri mutlaka tamamlanması gereken, kalan işin belirlenmesine yardımcı olabilecek, tek bir görünümde görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c307a-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="c307a-110">Birleştirilen bir toplu sipariş şu siparişlerin herhangi bir kombinasyonunu içerebilir:</span><span class="sxs-lookup"><span data-stu-id="c307a-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="c307a-111">Tek bir toplu sipariş ve birden fazla paketli sipariş</span><span class="sxs-lookup"><span data-stu-id="c307a-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="c307a-112">Birden fazla toplu sipariş ve tek bir paketli sipariş</span><span class="sxs-lookup"><span data-stu-id="c307a-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="c307a-113">Birden fazla toplu sipariş ve tek bir paketli sipariş</span><span class="sxs-lookup"><span data-stu-id="c307a-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="c307a-114">Sadece paketli siparişler</span><span class="sxs-lookup"><span data-stu-id="c307a-114">Only packed orders</span></span>





