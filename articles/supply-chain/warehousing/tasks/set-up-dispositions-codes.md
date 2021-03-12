---
title: Değerlendirme kodlarını ayarlama
description: Bu yordam, iade emri alma işlemi için mobil aygıtta kullanılabilecek bir değerlendirme kodunun kurulumuna odaklanır.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c98526423b28fcb6c4e00a9f2cfd84d5a9119e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977025"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="6ba58-103">Değerlendirme kodlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6ba58-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ba58-104">Bu yordam, iade emri alma işlemi için mobil aygıtta kullanılabilecek bir değerlendirme kodunun kurulumuna odaklanır.</span><span class="sxs-lookup"><span data-stu-id="6ba58-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="6ba58-105">Değerlendirme kodları, maddeler alındığında kullanılabilir kurallar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="6ba58-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="6ba58-106">Örneğin, kullanıcı bir iş kullanıcısı zarar görmüş maddeleri almak için mobil aygıta kullandığında, bozuk öğeler için bir değerlendirme kodu taratmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6ba58-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="6ba58-107">Alınan malların stok durumu, iş şablonu ve yerleşim yönergesi taranan değerlendirme kodundan belirlenebilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6ba58-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="6ba58-108">Satınalma siparişi alma işlemi ve bitirilmiş bir işlem olarak üretim emri raporu için değerlendirme kodu kullanımı isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="6ba58-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="6ba58-109">Maddeler bir taşınabilir aygıt kullanarak kayıt edilmiş ise satış siparişi iade alma işlemi için değerlendirme kodu kullanımı zorunludur.</span><span class="sxs-lookup"><span data-stu-id="6ba58-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="6ba58-110">Bu kılavuz oluşturulurken USMF demo verisi şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="6ba58-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="6ba58-111">Bu yordam ambar yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6ba58-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="6ba58-112">Ambar Yönetimi > Kurulum > Mobil aygıt > Değerlendirme kodları menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="6ba58-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="6ba58-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6ba58-113">Click New.</span></span>
    * <span data-ttu-id="6ba58-114">Müşteri iadelerinde kullanılmak üzere yeni bir değerlendirme kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="6ba58-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="6ba58-115">Değerlendirme kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6ba58-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="6ba58-116">Stok durumu alanında, stok durdurması olan bir stok durumu seçin.</span><span class="sxs-lookup"><span data-stu-id="6ba58-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="6ba58-117">USMF kullanıyorsanız, 'Durdurma'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="6ba58-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="6ba58-118">Sipariş satırlarında varsayılan durumu geçersiz kılmak için değerlendirme koduna bir stok durumu ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6ba58-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="6ba58-119">İş şablonu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6ba58-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="6ba58-120">İsteğe bağlı: bir iade emri ile ilişkilendirilmiş bir iş şablonu kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="6ba58-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="6ba58-121">Hiçbir değer sağlanmamışsa, iş şablonu, sisteminizdeki yapılandırılmış standart kurallar kullanılarak çözümlenir.</span><span class="sxs-lookup"><span data-stu-id="6ba58-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="6ba58-122">İş şablonu seçmek bu değerlendirme kodunun birlikte kullanılabileceği işlemleri sınırlar.</span><span class="sxs-lookup"><span data-stu-id="6ba58-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="6ba58-123">Örneğin bir değerlendirme kodunun, satın alma türünde iş emrine sahip bir çalışma şablonu varsa, bu müşteri tarafından iade edilen maddeleri kayıtta kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="6ba58-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="6ba58-124">İade değerlendirme kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="6ba58-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="6ba58-125">İade değerlendirme kodu, kayıt edilen maddeler için iade siparişi işleminin kalanını belirlemekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6ba58-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="6ba58-126">Bu örnekte, müşteri bir alacak dekontu almalıdır.</span><span class="sxs-lookup"><span data-stu-id="6ba58-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="6ba58-127">Eylem kredisi içeren bir iade değerlendirme kodu ekleyin.</span><span class="sxs-lookup"><span data-stu-id="6ba58-127">Add a returns disposition code that contains an action Credit.</span></span>  

