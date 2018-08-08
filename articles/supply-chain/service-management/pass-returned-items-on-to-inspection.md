---
title: "İade edilen maddeleri incelemeye iletme"
description: "İade edilen bir maddeyi kaydederken, bir maddenin stoka iade edilmeden veya başka bir yöntemle elden çıkarılmadan önce denetlemeye gönderilmesini belirtebilirsiniz."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 70aafb752b2c847d5d48236fd5d201a73e088c24
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---


# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="5012b-103">İade edilen maddeleri incelemeye iletme</span><span class="sxs-lookup"><span data-stu-id="5012b-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="5012b-104">İade edilen bir maddeyi kaydederken, bir maddenin stoka iade edilmeden veya başka bir yöntemle elden çıkarılmadan önce denetlemeye gönderilmesini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5012b-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="5012b-105">**Stok Yönetimi** \> **Günlükler** \> **Madde varışı** \> **Madde varışı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="5012b-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="5012b-106">\-veya-</span><span class="sxs-lookup"><span data-stu-id="5012b-106">\-or-</span></span>
    
    <span data-ttu-id="5012b-107">**Stok Yönetimi** \> **Günlükler** \> **Madde varışı** \> **Üretim girişi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5012b-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="5012b-108">**Konum günlüğü** formunda bir maddenin teslim alınmasını her zamanki gibi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="5012b-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="5012b-109">İade edilen maddelerin girişini kaydetme hakkında bilgi için bkz. <A href="register-the-receipt-of-returned-items.md">İade edilen maddelerin girişini kaydetme</A></span><span class="sxs-lookup"><span data-stu-id="5012b-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="5012b-110">**Varsayılan değerler** sekmesinde, **İşleme modu** alanında, **Karantina yönetimi** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="5012b-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="5012b-111">Bu seçimle sisteme bir karantina emri oluşturma isteği gönderilir ve denetimleri gerçekleştiren kişi veya departman **Karantina emri** formunu kullanarak bu emre yanıt verir.</span><span class="sxs-lookup"><span data-stu-id="5012b-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="5012b-112">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="5012b-112">See also</span></span>

[<span data-ttu-id="5012b-113">İade edilen maddeleri inceleme yoluyla alma</span><span class="sxs-lookup"><span data-stu-id="5012b-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="5012b-114">İade edilen maddelerin nasıl elden çıkarılacağını belirtme</span><span class="sxs-lookup"><span data-stu-id="5012b-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)


