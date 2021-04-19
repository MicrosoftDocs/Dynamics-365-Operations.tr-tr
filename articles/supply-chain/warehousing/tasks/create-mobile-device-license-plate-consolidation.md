---
title: Plaka birleştirme işlemi için bir mobil cihaz menü öğesi oluşturma
description: Bu yordam, plaka birleştirme işi için mobil cihaz menüsü öğesi oluşturmayı gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1dfb0bb2db5690a966d70f96a3bba2d60833abd4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831014"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="57ce5-103">Plaka birleştirme işlemi için bir mobil cihaz menü öğesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="57ce5-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57ce5-104">Bu yordam, plaka birleştirme işi için mobil cihaz menüsü öğesi oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="57ce5-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="57ce5-105">Bu, ambar çalışanlarının bir plakadaki maddeleri aynı konumda bulunan farklı bir plakadaki maddelerde birleştirmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="57ce5-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="57ce5-106">Örneğin, sonraki aşamalandırma adımları her iki iş emrinde de aynı olduğunda çalışanlar bu özelliği kullanabilir ve işin birleştirilmiş maddeler için yalnızca bir kere uygulanmasını sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="57ce5-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="57ce5-107">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57ce5-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="57ce5-108">Görev genellikle ambar yöneticisi tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="57ce5-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="57ce5-109">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="57ce5-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="57ce5-110">Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğeleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="57ce5-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="57ce5-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="57ce5-111">Click New.</span></span>
3. <span data-ttu-id="57ce5-112">Menü öğesi adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="57ce5-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="57ce5-113">Başlık alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="57ce5-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="57ce5-114">Mod alanında, 'Dolaylı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="57ce5-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="57ce5-115">Faaliyet kodu alanında 'Plakaları birleştir'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57ce5-115">In the Activity code field, select 'Consolidate license plates'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]