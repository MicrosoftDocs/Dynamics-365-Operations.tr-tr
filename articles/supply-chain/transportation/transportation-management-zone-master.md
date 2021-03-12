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
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 6527c4887ccd3085d63dd64c104a94e6354f536b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996481"
---
# <a name="transportation-management-zone-master"></a><span data-ttu-id="9b73c-103">Taşıma yönetimi ana bölgesi</span><span class="sxs-lookup"><span data-stu-id="9b73c-103">Transportation management zone master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b73c-104">Taşıma yönetimi coğrafi konumları bölgelere bölmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9b73c-104">Transport management lets you divide geographic locations into zones.</span></span> <span data-ttu-id="9b73c-105">Konumları bölgelere bölme işlemi, aşağıdakileri yapmanıza yardımcı olabilir:</span><span class="sxs-lookup"><span data-stu-id="9b73c-105">Dividing locations into zones can help to:</span></span>

- <span data-ttu-id="9b73c-106">**Taşıma fiyatlandırmasını basitleştirme**: Bölge bazında fiyatlandırma, özellikle taşıma konumlarının dağınık olduğu durumlarda ayrı ayrı konuma göre fiyatlandırmadan daha basit olabilir.</span><span class="sxs-lookup"><span data-stu-id="9b73c-106">**Simplify transportation pricing** – Zone-wise pricing can be simpler than individual location-based pricing, especially when transportation locations are scattered.</span></span>
- <span data-ttu-id="9b73c-107">**Yük planlamayı iyileştirme**: Yükleri bölgelere göre birleştirmeyi sağlar.</span><span class="sxs-lookup"><span data-stu-id="9b73c-107">**Optimize load planning** – By consolidating loads by zones.</span></span>
- <span data-ttu-id="9b73c-108">**Rota planlamayı iyileştirme**: Belirli bölgelere özel rota planları atamayı sağlar.</span><span class="sxs-lookup"><span data-stu-id="9b73c-108">**Optimize route planning** – By assigning specific route plans to specific zones.</span></span>

<span data-ttu-id="9b73c-109">Bölgeleri, her bölgeyi nitelendirmek için kullanılan meta veri alan değerlerini (ülke/bölge, posta kodu aralığı veya taşıyıcı hizmeti gibi) temel alarak tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="9b73c-109">You define zones based on the metadata field values (such as country, zip code range, or carrier service) that qualify each zone.</span></span> <span data-ttu-id="9b73c-110">Taşımacılık fiyatlarınız bir bölge kavramı kullanmıyorsa bölge tanımları gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="9b73c-110">Zone definitions aren't required if your transportation pricing doesn't employ a zone concept.</span></span>
