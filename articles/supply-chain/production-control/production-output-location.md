---
title: Üretim çıkış yeri
description: Bu konu, üretim çıkış konumunun kimliğini belirlemekte kullanılacak hiyerarşiyi açıklar.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d8d28b9670d8752c1039684551d56b1779a10b20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001611"
---
# <a name="production-output-location"></a><span data-ttu-id="8a034-103">Üretim çıkış yeri</span><span class="sxs-lookup"><span data-stu-id="8a034-103">Production output location</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a034-104">Bu konu, üretim çıkış konumunun kimliğini belirlemekte kullanılacak hiyerarşiyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="8a034-104">This topic describes the hierarchy that is used to identify the production output location.</span></span>

<span data-ttu-id="8a034-105">Üretim çıkış konumu, tamamlanmış malın üretildikten sonra ilk depolandığı konumdur.</span><span class="sxs-lookup"><span data-stu-id="8a034-105">The production output location is the location where a finished good is first stored after it's produced.</span></span> <span data-ttu-id="8a034-106">Bu, konum genellikle, tamamlanmış ürünü üreten üretim merkezine yakındır.</span><span class="sxs-lookup"><span data-stu-id="8a034-106">Usually, this location is close to the production process that produces the finished good.</span></span> <span data-ttu-id="8a034-107">Üretim çıkış konumu, malzemenin sevkiyat alanına, bir depolama konumuna, üretime devam etme işlemi için bir üretim giriş konumuna ve benzerlerine taşınmadan önceki bir ara depolamadır.</span><span class="sxs-lookup"><span data-stu-id="8a034-107">The production output location is used as intermediate storage for the material before it's moved on to the shipment area, a storage location, a production input location for a downstream production process, and so on.</span></span> 

<span data-ttu-id="8a034-108">Bir varsayılan üretim çıkış konumu, tamamlanmış mallar bir üretim siparişi veya toplu iş siparişinde raporlandığında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8a034-108">A default production output location is set when finished goods are reported on a production order or batch order.</span></span> <span data-ttu-id="8a034-109">Aşağıdaki hiyerarşi bu çıkış konumunu tanımlamakta kullanılır:</span><span class="sxs-lookup"><span data-stu-id="8a034-109">The following hierarchy is used to identify this output location:</span></span>

1. <span data-ttu-id="8a034-110">Üretim emri veya toplu iş siparişi başlığında tanımlanan çıkış konumunu kullan.</span><span class="sxs-lookup"><span data-stu-id="8a034-110">Use the output location that is defined on the production order or batch order header.</span></span>
2. <span data-ttu-id="8a034-111">Burada konum bulunamıyorsa, kaynak üzerinde üretim rotasında tanımlanmış son operasyonda tanımlanmış olan çıkış konumunu kullan.</span><span class="sxs-lookup"><span data-stu-id="8a034-111">If no location is found there, use the output location that is defined on the resource that is used by the last operation that is defined in the production route.</span></span>
3. <span data-ttu-id="8a034-112">Burada konum bulunamıyorsa, kaynak grubu üzerinde üretim rotasında tanımlanmış son operasyon için tanımlanmış olan çıkış konumunu kullan.</span><span class="sxs-lookup"><span data-stu-id="8a034-112">If no location is found there, use the output location that is defined on the resource group that is used by the resource for the last operation that is defined in the production route.</span></span>
4. <span data-ttu-id="8a034-113">Burada konum bulunmazsa, üretim emri için tanımlanmış ambardaki çıkış konumunu kullan.</span><span class="sxs-lookup"><span data-stu-id="8a034-113">If no location is found there, use the output location that is defined on the warehouse that is defined for the production order.</span></span>

<span data-ttu-id="8a034-114">Bir varsayılan üretim çıkış konumu, yalnızca gelişmiş ambar işlemleri kullanan ürünler için ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="8a034-114">A default production output location is set only for products that are set up by using advanced warehouse processes.</span></span> <span data-ttu-id="8a034-115">Bu türde bir madde tamamlanmış olarak raporlandığında, **Tamamlanmış mal koyma** veya **Ortak ürün ve yan ürün koyma** türünde bir ambar işi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="8a034-115">When this type of item is reported as finished, warehouse work of the **Finished goods put away** or **Co-product and by-product put away** type is created.</span></span> <span data-ttu-id="8a034-116">Bu türde iş, üretim çıkış konumunu çekme konumu olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="8a034-116">This type of work uses the production output location as the pick location.</span></span> <span data-ttu-id="8a034-117">Yerine koyma konumu, konum yönergeleri tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="8a034-117">The put-away location is determined by the location directives.</span></span>
