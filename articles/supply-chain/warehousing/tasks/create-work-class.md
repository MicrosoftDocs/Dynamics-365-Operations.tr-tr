---
title: İş sınıfı oluşturma
description: Bu yordam, iş sınıfı kurmayı göstermektedir.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed9b72d891df4d40213d4854da6b09bd9876effa
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439656"
---
# <a name="create-a-work-class"></a><span data-ttu-id="312f2-103">İş sınıfı oluşturma</span><span class="sxs-lookup"><span data-stu-id="312f2-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="312f2-104">Bu yordam, iş sınıfı kurmayı göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="312f2-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="312f2-105">İş sınıfları, ambar çalışanı tarafından bir mobil aygıtta işlenebilecek iş emri satırlarının türünü yönetmek ve/veya sınırlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="312f2-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="312f2-106">Çalışanın işleyebileceği satırlar, çalışanın erişimi olan mobil cihaz menü öğeleri üzerindeki iş sınıfları ve iş satırı üzerinde belirlenen iş sınıfı tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="312f2-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="312f2-107">İş sınıfları, iş emri satırı için yerine koyma konumunu doğrulamak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="312f2-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="312f2-108">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="312f2-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="312f2-109">Bu yordam ambar yöneticisi için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="312f2-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="312f2-110">Ambar yönetimi > Kurulum > İş > İş sınıfları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="312f2-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="312f2-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="312f2-111">Click New.</span></span>
3. <span data-ttu-id="312f2-112">İş sınıfı kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="312f2-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="312f2-113">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="312f2-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="312f2-114">İş siparişi türü alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="312f2-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="312f2-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="312f2-115">Click New.</span></span>
7. <span data-ttu-id="312f2-116">Konum türü alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="312f2-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="312f2-117">Konum türü seçerseniz, maddelerin çekildikten sonra nereye konulabileceklerine kısıtlama getirir.</span><span class="sxs-lookup"><span data-stu-id="312f2-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="312f2-118">Bu ayar, konum yönergesi konumu çözümlemeye çalışırken ya da bir ambar çalışanı el ile mobil aygıt menü öğesi için bir konum sağlarken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="312f2-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="312f2-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="312f2-119">Close the page.</span></span>

