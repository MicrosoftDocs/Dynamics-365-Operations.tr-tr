---
title: Yerleşim profili oluşturma
description: Bu konu Dynamics 365 Supply Chain Management'ta yerleşim profili oluşturma işlemi açıklanmaktadır.
author: ShylaThompson
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9be25004452ab0a0e2af0ac552a69f805d301d8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239074"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="326e1-103">Yerleşim profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="326e1-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="326e1-104">Bu konu Dynamics 365 Supply Chain Management'ta yerleşim profili oluşturma işlemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="326e1-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="326e1-105">Ambardaki her konumun, örneğin karma maddelere izin verip vermediği gibi özelliklerini açıklayan, kendisiyle ilişkili bir konum profiline sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="326e1-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="326e1-106">Bu yordamda, plaka kontrolü gerektirmeyen bir konum için bir profil oluşturacağız.</span><span class="sxs-lookup"><span data-stu-id="326e1-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="326e1-107">Karışık maddeleri ve karışık stok durumlarını etkinleştirecek ve döngü sayımına izin vereceğiz.</span><span class="sxs-lookup"><span data-stu-id="326e1-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="326e1-108">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="326e1-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="326e1-109">Gezinti bölmesinde **Modüller > Ambar yönetimi > Kurulum > Ambar > Yerleşim profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="326e1-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="326e1-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="326e1-110">Select **New**.</span></span>
3. <span data-ttu-id="326e1-111">**Konum profili numarası** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="326e1-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="326e1-112">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="326e1-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="326e1-113">**Konum biçimi** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="326e1-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="326e1-114">**Konum türü** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="326e1-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="326e1-115">**Giriş/çıkış noktası yönetimi profili kimliği** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="326e1-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="326e1-116">**Karışık öğelere izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="326e1-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="326e1-117">**Karışık stok durumlarına izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="326e1-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="326e1-118">**Döngü sayımına izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="326e1-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="326e1-119">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="326e1-119">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]