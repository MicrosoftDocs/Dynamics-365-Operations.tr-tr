---
title: Mobil cihazda en eski toplu işi seçme
description: Bu konu bir mobil cihazdan en eski toplu işi seçme seçeneklerinin nasıl ayarlanacağını ve uygulanacağını açıklamaktadır.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f235c34d6369c6f0584a7bac1c1be75f3d84c9c0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215643"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="23d3e-103">Mobil cihazda en eski toplu işi seçme</span><span class="sxs-lookup"><span data-stu-id="23d3e-103">Pick oldest batch on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23d3e-104">**En eski toplu işi seç** konfigürasyonuna mobil cihaz menüsünden erişebilirsiniz ve bu konfigürasyon ambar çalışanlarını bulundukları yerleşimde en eski toplu işi seçme konusunda zorlamanızı veya uyarmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="23d3e-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="23d3e-105">Uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="23d3e-105">Where it applies</span></span>
<span data-ttu-id="23d3e-106">En eski işi seçme mobil cihaz menü öğelerinde yapılandırılır ve aşağıdaki toplu iş maddeleri için seçimi etkiler.</span><span class="sxs-lookup"><span data-stu-id="23d3e-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="23d3e-107">En eski toplu işi seçme için konfigürasyonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="23d3e-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="23d3e-108">Varolan işi kullanmak üzere ayarlanan maddeler için **En eski toplu işi seç** mobil cihaz menüsünden **Hiçbiri**, **Uyar** veya **Zorla** olarak ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="23d3e-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="23d3e-109">**Hiçbiri**: Çalışanlar herhangi bir ileti almaz ve bulundukları yerleşimde herhangi bir toplu işi seçmelerine izin verilir.</span><span class="sxs-lookup"><span data-stu-id="23d3e-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="23d3e-110">**Uyar** ve **Zorla**: Çalışan bir toplu iş seçerken toplu iş denetiminin üstünde en eski bitiş tarihine sahip olan toplu işlerin listesi görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="23d3e-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="23d3e-111">Konum plaka denetimli ise, en eski toplu işe sahip plakaların listesi plaka denetiminin üst kısmında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="23d3e-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="23d3e-112">**Uyar**: Çalışan gösterilen listede olmayan bir plaka veya toplu iş seçerse, denetim boş bırakılacak ve seçilmek üzere daha eski bir toplu iş bulunduğunu belirten bir uyarı görüntülenecektir.</span><span class="sxs-lookup"><span data-stu-id="23d3e-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="23d3e-113">Çalışmaya devam etmek için, çalışan aynı toplu işi veya plakayı yeniden seçebilir.</span><span class="sxs-lookup"><span data-stu-id="23d3e-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="23d3e-114">**Zorla**: Çalışanlar seçmek için daha eski bir toplu iş olduğunu gösteren iletiyi almaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="23d3e-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>
