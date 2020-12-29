---
title: Konsolide toplu iş emirleri
description: Bu makale konsolide edilen toplu siparişler kavramını açıklar.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faeb90aa3366a58b746c0b397dd950bfb8c9024f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439466"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="ae930-103">Konsolide toplu iş emirleri</span><span class="sxs-lookup"><span data-stu-id="ae930-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae930-104">Bu makale konsolide edilen toplu siparişler kavramını açıklar.</span><span class="sxs-lookup"><span data-stu-id="ae930-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="ae930-105">Üretilen toplu ürün, ana ürün olarak değerlendirilirken, paketlenen bir ürün alt ürün olarak değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="ae930-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="ae930-106">Toplu ürün ile paketli ürün arasındaki ilişki bir toplu ürün dönüşümü cinsinden ifade edilir.</span><span class="sxs-lookup"><span data-stu-id="ae930-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="ae930-107">Bu toplu öğe dönüşümü toplu öğenin kendisine tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="ae930-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="ae930-108">Paketlenmiş öğeler tek ünite olarak değerlendirilen, tek bir boyuttan veya birden fazla boyuttan meydana gelen konteynerlerde paketlenir.</span><span class="sxs-lookup"><span data-stu-id="ae930-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="ae930-109">Bir toplu ürün için siparişleri birleştirerek, tüm ilgili toplu siparişleri mutlaka tamamlanması gereken, kalan işin belirlenmesine yardımcı olabilecek, tek bir görünümde görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae930-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="ae930-110">Birleştirilen bir toplu sipariş şu siparişlerin herhangi bir kombinasyonunu içerebilir:</span><span class="sxs-lookup"><span data-stu-id="ae930-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="ae930-111">Tek bir toplu sipariş ve birden fazla paketli sipariş</span><span class="sxs-lookup"><span data-stu-id="ae930-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="ae930-112">Birden fazla toplu sipariş ve tek bir paketli sipariş</span><span class="sxs-lookup"><span data-stu-id="ae930-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="ae930-113">Birden fazla toplu sipariş ve tek bir paketli sipariş</span><span class="sxs-lookup"><span data-stu-id="ae930-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="ae930-114">Sadece paketli siparişler</span><span class="sxs-lookup"><span data-stu-id="ae930-114">Only packed orders</span></span>




