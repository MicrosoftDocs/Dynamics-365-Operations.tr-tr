---
title: Taşıyıcı grupları
description: Bu konuda, taşıyıcı grupları için veri ayarlama yöntemi açıklanmaktadır.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2570479edac9bc8cc7aa998a8b69f54ffc10cd61
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646446"
---
# <a name="carrier-groups"></a><span data-ttu-id="143c5-103">Taşıyıcı grupları</span><span class="sxs-lookup"><span data-stu-id="143c5-103">Carrier groups</span></span>

<span data-ttu-id="143c5-104">Taşıyıcı grubu, sevkiyat taşıyıcıları ve taşıyıcı hizmetleri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="143c5-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="143c5-105">Her taşıyıcı grubu, kendisine ait olan sevkiyat taşıyıcıları ve taşıyıcı hizmetleri için tercih edilen sırayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="143c5-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="143c5-106">Aynı rota segmenti için birden fazla sevkiyat taşıyıcısı ve taşıyıcı hizmeti olduğunda, rota planı veya rota kılavuzunda belirli bir sevkiyat taşıyıcıyı ve taşıyıcı hizmeti yerine bir taşıyıcı grubu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="143c5-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="143c5-107">Taşıyıcı grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="143c5-107">Create a carrier group</span></span>

1. <span data-ttu-id="143c5-108">**Taşımacılık yönetimi &gt; Kurulum &gt; Taşıyıcılar &gt; Taşıyıcı grupları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="143c5-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="143c5-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="143c5-109">Select **New**.</span></span>
1. <span data-ttu-id="143c5-110">**Taşıyıcı grubu** alanına, grup için benzersiz bir tanımlayıcı (kimlik) girin.</span><span class="sxs-lookup"><span data-stu-id="143c5-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="143c5-111">**Ad** alanına grup için açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="143c5-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="143c5-112">**Ayrıntılar** hızlı sekmesinde, bir satır ekleyin ve bunun için bir sevkiyat taşıyıcısı ve bir taşıyıcı hizmeti seçin.</span><span class="sxs-lookup"><span data-stu-id="143c5-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="143c5-113">Grup için gerek duyduğunuz sayıda taşıyıcı ekleyinceye kadar bu adımı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="143c5-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="143c5-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="143c5-114">Close the page.</span></span>
