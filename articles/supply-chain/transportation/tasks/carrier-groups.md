---
title: Taşıyıcı grupları
description: Bu konuda, taşıyıcı grupları için veri ayarlama yöntemi açıklanmaktadır.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9fe95ee9a0b6d69544f35ac6bc9cdf3dd00db291
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809074"
---
# <a name="carrier-groups"></a><span data-ttu-id="3d40e-103">Taşıyıcı grupları</span><span class="sxs-lookup"><span data-stu-id="3d40e-103">Carrier groups</span></span>

<span data-ttu-id="3d40e-104">Taşıyıcı grubu, sevkiyat taşıyıcıları ve taşıyıcı hizmetleri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="3d40e-104">A carrier group is a collection of shipping carriers and carrier services.</span></span> <span data-ttu-id="3d40e-105">Her taşıyıcı grubu, kendisine ait olan sevkiyat taşıyıcıları ve taşıyıcı hizmetleri için tercih edilen sırayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d40e-105">Each carrier group specifies the preferred sequence for the shipping carriers and carrier services that belong to it.</span></span>

<span data-ttu-id="3d40e-106">Aynı rota segmenti için birden fazla sevkiyat taşıyıcısı ve taşıyıcı hizmeti olduğunda, rota planı veya rota kılavuzunda belirli bir sevkiyat taşıyıcıyı ve taşıyıcı hizmeti yerine bir taşıyıcı grubu belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d40e-106">When multiple shipping carriers and carrier services exist for the same route segment, you can specify a carrier group instead of a specific shipping carrier and carrier service in the route plan or route guide.</span></span>

## <a name="create-a-carrier-group"></a><span data-ttu-id="3d40e-107">Taşıyıcı grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="3d40e-107">Create a carrier group</span></span>

1. <span data-ttu-id="3d40e-108">**Taşımacılık yönetimi &gt; Kurulum &gt; Taşıyıcılar &gt; Taşıyıcı grupları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="3d40e-108">Go to **Transportation management &gt; Setup &gt; Carriers &gt; Carrier group**.</span></span>
1. <span data-ttu-id="3d40e-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3d40e-109">Select **New**.</span></span>
1. <span data-ttu-id="3d40e-110">**Taşıyıcı grubu** alanına, grup için benzersiz bir tanımlayıcı (kimlik) girin.</span><span class="sxs-lookup"><span data-stu-id="3d40e-110">In the **Carrier group** field, enter a unique identifier (ID) for the group.</span></span>
1. <span data-ttu-id="3d40e-111">**Ad** alanına grup için açıklayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="3d40e-111">In the **Name** field, enter a descriptive name for the group.</span></span>
1. <span data-ttu-id="3d40e-112">**Ayrıntılar** hızlı sekmesinde, bir satır ekleyin ve bunun için bir sevkiyat taşıyıcısı ve bir taşıyıcı hizmeti seçin.</span><span class="sxs-lookup"><span data-stu-id="3d40e-112">On the **Details** FastTab, add a row, and select a shipping carrier and a carrier service for it.</span></span> <span data-ttu-id="3d40e-113">Grup için gerek duyduğunuz sayıda taşıyıcı ekleyinceye kadar bu adımı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="3d40e-113">Repeat this step until you've added as many carriers as you require for the group.</span></span>
1. <span data-ttu-id="3d40e-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3d40e-114">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]