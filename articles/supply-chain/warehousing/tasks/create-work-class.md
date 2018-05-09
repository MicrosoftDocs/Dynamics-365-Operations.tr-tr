--- 
title: "İş sınıfı oluşturma"
description: "Bu yordam, iş sınıfı kurmayı göstermektedir."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ae594d55b1a14ab4e832658aaa12165f1be2b303
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-work-class"></a><span data-ttu-id="d8a25-103">İş sınıfı oluşturma</span><span class="sxs-lookup"><span data-stu-id="d8a25-103">Create a work class</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8a25-104">Bu yordam, iş sınıfı kurmayı göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="d8a25-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="d8a25-105">İş sınıfları, ambar çalışanı tarafından bir mobil aygıtta işlenebilecek iş emri satırlarının türünü yönetmek ve/veya sınırlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d8a25-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="d8a25-106">Çalışanın işleyebileceği satırlar, çalışanın erişimi olan mobil cihaz menü öğeleri üzerindeki iş sınıfları ve iş satırı üzerinde belirlenen iş sınıfı tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="d8a25-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that’s specified on the work lines.</span></span> <span data-ttu-id="d8a25-107">İş sınıfları, iş emri satırı için yerine koyma konumunu doğrulamak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d8a25-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="d8a25-108">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8a25-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d8a25-109">Bu yordam ambar yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="d8a25-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="d8a25-110">Ambar yönetimi > Kurulum > İş > İş sınıfları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d8a25-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="d8a25-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8a25-111">Click New.</span></span>
3. <span data-ttu-id="d8a25-112">İş sınıfı kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d8a25-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="d8a25-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d8a25-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d8a25-114">İş siparişi türü alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="d8a25-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="d8a25-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d8a25-115">Click New.</span></span>
7. <span data-ttu-id="d8a25-116">Konum türü alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d8a25-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="d8a25-117">Konum türü seçerseniz, maddelerin çekildikten sonra nereye konulabileceklerine kısıtlama getirir.</span><span class="sxs-lookup"><span data-stu-id="d8a25-117">If you select a location type, this sets a restriction on where items can be put after they’ve been picked.</span></span> <span data-ttu-id="d8a25-118">Bu ayar, konum yönergesi konumu çözümlemeye çalışırken ya da bir ambar çalışanı el ile mobil aygıt menü öğesi için bir konum sağlarken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d8a25-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="d8a25-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d8a25-119">Close the page.</span></span>


