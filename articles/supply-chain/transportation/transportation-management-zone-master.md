---
title: Taşıma yönetimi ana bölgesi
description: Bu konuda, taşıma yönetiminin coğrafi konumları bölgelere bölmenize nasıl olanak verdiği açıklanmaktadır.
author: Henrikan
manager: ''
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSZoneMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2112e7131281cd485b580fd71536981c1ba4aefd
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/29/2020
ms.locfileid: "4439765"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="29bb1-103">Taşıma yönetimi ana bölgesi</span><span class="sxs-lookup"><span data-stu-id="29bb1-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29bb1-104">Taşıma yönetimi coğrafi konumları bölgelere bölmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="29bb1-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="29bb1-105">Konumları bölgelere bölme işlemi, aşağıdakileri yapmanıza yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="29bb1-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="29bb1-106">**Taşıma fiyatlandırmasını basitleştirme**: Bölge bazında fiyatlandırma, özellikle taşıma konumlarının dağınık olduğu durumlarda ayrı ayrı konuma göre fiyatlandırmadan daha basit olabilir.</span><span class="sxs-lookup"><span data-stu-id="29bb1-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="29bb1-107">**Yük planlamayı iyileştirme**: Yükleri bölgelere göre birleştirmeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="29bb1-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="29bb1-108">**Rota planlamayı iyileştirme**: Belirli bölgelere özel rota planları atamayı sağlar.</span><span class="sxs-lookup"><span data-stu-id="29bb1-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="29bb1-109">Bölgeleri, her bölgeyi nitelendirmek için kullanılan meta veri alan değerlerini (ülke/bölge, posta kodu aralığı veya taşıyıcı hizmeti gibi) temel alarak tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="29bb1-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="29bb1-110">Taşımacılık fiyatlarınız bir bölge kavramı kullanmıyorsa bölge tanımları gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="29bb1-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>
