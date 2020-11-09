---
title: Ek yerleşim bölgeleri
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'a eklenen yeni bölge bölgelerinin genel görünümünü sağlar .
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 6cf81939989b8faffcda51bbbd5bc6b27aec7eea
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016321"
---
# <a name="additional-location-zones"></a><span data-ttu-id="d9555-103">Ek yerleşim bölgeleri</span><span class="sxs-lookup"><span data-stu-id="d9555-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9555-104">Microsoft Dynamics 365 Supply Chain Management'ta üç yeni bölge alanı vardır.</span><span class="sxs-lookup"><span data-stu-id="d9555-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="d9555-105">Ambar yöneticileri bunları ek ambar kuruluşları veya mizanpajları tanımlamak için kullanabilirler.</span><span class="sxs-lookup"><span data-stu-id="d9555-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="d9555-106">Yeni bölge alanları el ile veya **konum kurulum** Sihirbazı kullanılarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="d9555-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="d9555-107">Bunlar, konumlar tablosunu kullanan herhangi bir sorgu veya filtre uygulama içinde kullanılabilirler.</span><span class="sxs-lookup"><span data-stu-id="d9555-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="d9555-108">Bölge alanlarını kullanmak için ek bir kurulum gerekmez.</span><span class="sxs-lookup"><span data-stu-id="d9555-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="d9555-109">Ek konum dilimi özelliğini aç</span><span class="sxs-lookup"><span data-stu-id="d9555-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="d9555-110">*İlave konum bölgesi* özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d9555-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="d9555-111">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="d9555-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d9555-112">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="d9555-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d9555-113">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="d9555-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d9555-114">**Özellik adı:** *Ek konum bölgesi aç*</span><span class="sxs-lookup"><span data-stu-id="d9555-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="d9555-115">Yerleşim bölgelerini kullan</span><span class="sxs-lookup"><span data-stu-id="d9555-115">Use location zones</span></span>

1. <span data-ttu-id="d9555-116">**Ambar yönetimi \> Kurulum \> Ambar \> Konum kurulum sihirbazı** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="d9555-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="d9555-117">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="d9555-117">Set the following values:</span></span>

    - <span data-ttu-id="d9555-118">**Ambar** alanında _62_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d9555-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="d9555-119">**Bölge kodu** alanında _ZEMİN_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d9555-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="d9555-120">**İlave Bölge 1** alanında _PICKZONE1_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d9555-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="d9555-121">**İlave Bölge 2** alanında _WEBSHOP1_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d9555-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="d9555-122">**Konum profil kimliği** alanında _ZEMİN_ 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d9555-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="d9555-123">**Zemin** satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="d9555-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="d9555-124">**Gönderen numarası** alanına _1_ girin.</span><span class="sxs-lookup"><span data-stu-id="d9555-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="d9555-125">**Kime numarası** alanına _3_ girin.</span><span class="sxs-lookup"><span data-stu-id="d9555-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="d9555-126">**Koridor** satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="d9555-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="d9555-127">**Gönderen numarası** alanına _1_ girin.</span><span class="sxs-lookup"><span data-stu-id="d9555-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="d9555-128">**Kime numarası** alanına _5_ girin.</span><span class="sxs-lookup"><span data-stu-id="d9555-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="d9555-129">**Oluştur** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d9555-129">Select **Create**.</span></span>
8. <span data-ttu-id="d9555-130">Yeni konumların eklendiğini bildiren iletiler alırsınız.</span><span class="sxs-lookup"><span data-stu-id="d9555-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="d9555-131">İletileri görüntülemek için **iletileri göster** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d9555-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="d9555-132">**Ambar yönetimi \> Kurulum \> Ambar \> Konumlar** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d9555-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="d9555-133">Yeni konumlar listede görünür ve tüm bölge alanları (yani, varolan bölge alanı ve yeni ek bölge alanları) kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d9555-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
