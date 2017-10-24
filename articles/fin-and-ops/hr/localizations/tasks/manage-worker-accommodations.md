--- 
title: "Çalışan konaklamalarını yönetme"
description: "Bu yordam ergonomik sandalyeler veya düzenli molalar gibi çalışma ortamı konaklama türlerini ayarlamayı adım adım anlatmaktadır."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 10d34d0b2eca95034d1f67931ff72a035be9a6b8
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="manage-worker-accommodations"></a><span data-ttu-id="cf9a1-103">Çalışan konaklamalarını yönetme</span><span class="sxs-lookup"><span data-stu-id="cf9a1-103">Manage worker accommodations</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="cf9a1-104">Bu yordam ergonomik sandalyeler veya düzenli molalar gibi çalışma ortamı konaklama türlerini ayarlamayı adım adım anlatmaktadır.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-104">This procedure walks through the steps for setting up work environment accommodation types, such as ergonomic chairs or periodic breaks.</span></span> <span data-ttu-id="cf9a1-105">Ayrıca bu konaklama türlerinin çalışana nasıl atanacağını ve konaklama türünü onaylamayı veya reddetmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-105">It also shows how to assign these accommodation types to a worker, and either approve or deny the accommodation type.</span></span> <span data-ttu-id="cf9a1-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="setup-accommodations"></a><span data-ttu-id="cf9a1-107">Konaklamaları ayarla</span><span class="sxs-lookup"><span data-stu-id="cf9a1-107">Setup accommodations</span></span>
1. <span data-ttu-id="cf9a1-108">İnsan Kaynakları > Kurulum > Konaklama türleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-108">Go to Human resources > Setup > Accommodation types.</span></span>
2. <span data-ttu-id="cf9a1-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-109">Click New.</span></span>
3. <span data-ttu-id="cf9a1-110">Konaklama türü alanına konaklama için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-110">In the Accommodation type field, enter a name for the accommodation.</span></span> <span data-ttu-id="cf9a1-111">Örnek: Klavye.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-111">Example: Keyboard.</span></span>
4. <span data-ttu-id="cf9a1-112">Açıklama alanına konaklama tipi için bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-112">In the Description field, enter a description for the accommodation.</span></span> <span data-ttu-id="cf9a1-113">Örnek: Ergonomik Klavye.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-113">Example: Ergonomic Keyboard.</span></span>
5. <span data-ttu-id="cf9a1-114">Not alanına konaklamayı netleştirmek için yardımcı olacak tüm bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-114">In the Note field, enter any information that helps to clarify the accommodation.</span></span>
6. <span data-ttu-id="cf9a1-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-115">Click Save.</span></span>
7. <span data-ttu-id="cf9a1-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-116">Close the page.</span></span>

## <a name="assign-accommodations"></a><span data-ttu-id="cf9a1-117">Konaklamaları atayın</span><span class="sxs-lookup"><span data-stu-id="cf9a1-117">Assign accommodations</span></span>
1. <span data-ttu-id="cf9a1-118">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-118">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="cf9a1-119">Listeden bir personel seçin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-119">From the list, select an employee.</span></span>
3. <span data-ttu-id="cf9a1-120">Konaklamayı talep eden personelin adına tıklayarak, çalışanın kim olduğuna dair detayları görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-120">Click the employee's name to view details about the employee who is requesting the accommodation.</span></span>
4. <span data-ttu-id="cf9a1-121">Kişisel bilgiler Hızlı Sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-121">Expand the Personal information FastTab.</span></span>
5. <span data-ttu-id="cf9a1-122">Konaklamalar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-122">Click Accommodations.</span></span>
6. <span data-ttu-id="cf9a1-123">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-123">Click New.</span></span>
7. <span data-ttu-id="cf9a1-124">Konaklama türü alanında uygun konaklamayı seçin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-124">In the Accommodation type field, select the appropriate accommodation.</span></span> <span data-ttu-id="cf9a1-125">Örnek: Klavye</span><span class="sxs-lookup"><span data-stu-id="cf9a1-125">Example: Keyboard</span></span>
8. <span data-ttu-id="cf9a1-126">İş görevi alanında, konaklamayı gerektiren iş görevini girin</span><span class="sxs-lookup"><span data-stu-id="cf9a1-126">In the Job task field, enter the work task that requires the accommodation.</span></span>
9. <span data-ttu-id="cf9a1-127">Durum alanında uygun durumu girin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-127">In the Status field, enter the appropriate status.</span></span> <span data-ttu-id="cf9a1-128">Örnek: Makul</span><span class="sxs-lookup"><span data-stu-id="cf9a1-128">Example: Reasonable</span></span>
    * <span data-ttu-id="cf9a1-129">Aşağıdaki durumlar mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-129">The following statuses are available.</span></span> <span data-ttu-id="cf9a1-130">Talep, konaklamanın oluşturulduğunu fakat henüz incelenmediğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-130">Requested indicates that the accommodation has been created but not yet reviewed.</span></span> <span data-ttu-id="cf9a1-131">Uygun, konaklamanın uygun olduğunu ve izin verileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-131">Reasonable indicates that the accommodation is reasonable and will be granted.</span></span> <span data-ttu-id="cf9a1-132">Aşırı güçlük, konaklamanın işveren üzerinde aşırı yük oluşturacağını ve reddedildiğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-132">Undue hardship indicates that the accommodation will place an unreasonable burden on the employer, and has been denied.</span></span> <span data-ttu-id="cf9a1-133">Bu örnekte, konaklama talebi en azda olduğu için istek hemen kabul edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-133">In this example, the request was approved immediately because the accommodation request was minimal.</span></span>  
10. <span data-ttu-id="cf9a1-134">Onaylanan alanında, konaklama talebini kimin onaylandığını seçin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-134">In the Accepted field, select the person who accepted the accommodation request.</span></span>
11. <span data-ttu-id="cf9a1-135">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-135">Click Select.</span></span>
12. <span data-ttu-id="cf9a1-136">Kabul tarihi alanında, konaklama talebinin kabul edildiği tarih ve saati girin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-136">In the Accepted date field, enter the date and time when the accommodation request was accepted.</span></span>
13. <span data-ttu-id="cf9a1-137">Not bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-137">Expand the Note section.</span></span>
14. <span data-ttu-id="cf9a1-138">Mali alanda, konaklamanın etkisini açıklamaya yardımcı olacak tüm bilgileri veya kaynak maliyetlerini girin.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-138">In the Financial field, enter any information or resource costs that helps to clarify the impact of the accommodation.</span></span>
    * <span data-ttu-id="cf9a1-139">Eğer konaklama reddedildiyse, Yanıt alanı talebin neden reddedildiğini göstermekte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-139">If the accommodation has been denied, the Reply field can be used to indicate why a request was denied.</span></span>  
15. <span data-ttu-id="cf9a1-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cf9a1-140">Click Save.</span></span>


