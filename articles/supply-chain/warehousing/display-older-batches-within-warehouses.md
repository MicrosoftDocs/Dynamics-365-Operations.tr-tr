---
title: Bir mobil cihazda ambar içindeki eski toplu işleri görüntülemeyi konfigüre etme
description: Bu konu, bir iş satırının geçerli konumundan daha eski toplu işlere sahip konumların bir listesini görüntüleme için bir mobil cihazı ayarlamayı açıklar.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 946266e73d59bdf383f1f91cdf70dd58f01b995c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569440"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="c1dd1-103">Bir mobil cihazda ambar içindeki eski toplu işleri görüntülemeyi konfigüre etme</span><span class="sxs-lookup"><span data-stu-id="c1dd1-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1dd1-104">**Bu ambar içerisindeki daha eski toplu işleri görüntüle** yapılandırması, iş satırının geçerli konumundakinden eski toplu işlere sahip konumları listelemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="c1dd1-105">Görüntülenen konumların listesi konumdaki eski toplu işler hakkında bilgiyi, her bir toplu işin bitiş tarihi ve fiziksel stokunu içerir.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="c1dd1-106">Yeni bir konumdan çekmeyi veya geçerli konumdan çekmeye devam etmeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="c1dd1-107">Yeni bir konumdan çek - Çekmek için yeni bir konum seçerseniz, geçerli iş satırı yeni konumu kullanmak üzere güncelleştirilir ve iş, yeni konumda her zaman olduğu gibi devam eder.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="c1dd1-108">Yeni konumun geçerli olması için tüm iş satırı için yeterli kullanılabilir miktara sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="c1dd1-109">Gerekli miktar kullanılabilir durumda değilse, iş satıcı güncelleştirilmez ve liste görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="c1dd1-110">Geçerli konumdan çekmeye devam et - Geçerli iş satırı konumuyla devam ederseniz, iş satırı için miktarlar orijinal konumdan çekilmeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="c1dd1-111">Uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="c1dd1-111">Where it applies</span></span>
<span data-ttu-id="c1dd1-112">Ambar içindeki eski toplu işleri görüntüle mobil cihaz menü öğelerinde yapılandırılır ve aşağıdaki toplu iş maddeleri için seçimi etkiler.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="c1dd1-113">Bu ambar içindeki eski toplu işleri görüntülemeyi ayarlama</span><span class="sxs-lookup"><span data-stu-id="c1dd1-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="c1dd1-114">**Bu ambar içindeki eski toplu işleri görüntüle** yapılandırması mobil cihaz menü öğelerinde **En eski toplu işi çek** seçeneği **Uyar** olarak ayarlanmışsa kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="c1dd1-115">**Ambar yönetimi** > **Kurulum** > **Mobil cihaz** > **Mobil cihaz menü öğeleri** altında, **Mevcut işi kullan**'ı menü öğesi için **Evet** olarak ayarlayın ve **En eksiyi çek** altında **Uyar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c1dd1-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 

