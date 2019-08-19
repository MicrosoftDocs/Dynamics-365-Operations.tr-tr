---
title: Yerleşim profili oluşturma
description: Ambardaki her konumun, örneğin karma maddelere izin verip vermediği gibi özelliklerini açıklayan, kendisiyle ilişkili bir konum profiline sahip olması gerekir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9e1217a1105e1d53fc937f927e066e392f1ef14
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847339"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="4661f-103">Yerleşim profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="4661f-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4661f-104">Ambardaki her konumun, örneğin karma maddelere izin verip vermediği gibi özelliklerini açıklayan, kendisiyle ilişkili bir konum profiline sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="4661f-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="4661f-105">Bu yordamda, plaka kontrolü gerektirmeyen bir konum için bir profil oluşturacağız.</span><span class="sxs-lookup"><span data-stu-id="4661f-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="4661f-106">Karışık maddeleri ve karışık stok durumlarını etkinleştirecek ve döngü sayımına izin vereceğiz.</span><span class="sxs-lookup"><span data-stu-id="4661f-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="4661f-107">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4661f-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="4661f-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4661f-108">Click New.</span></span>
2. <span data-ttu-id="4661f-109">Konum profili numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4661f-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="4661f-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="4661f-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4661f-111">Konum biçimi alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="4661f-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="4661f-112">Konum türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="4661f-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="4661f-113">Giriş/çıkış noktası yönetimi profili kimliği alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="4661f-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="4661f-114">Karışık öğelere izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4661f-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="4661f-115">Karışık stok durumlarına izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4661f-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="4661f-116">Döngü sayımına izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4661f-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="4661f-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4661f-117">Click Save.</span></span>
11. <span data-ttu-id="4661f-118">Ambar yönetimi > Kurulum > Ambar > Konum profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="4661f-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

