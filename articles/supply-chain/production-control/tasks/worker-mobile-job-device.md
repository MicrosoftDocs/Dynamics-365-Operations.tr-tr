--- 
title: "Mobil iş cihazını kullanarak çalışanı yapılandırma"
description: "Bu yordam, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: f9de2f79c68fead5ede714ff05bba97118874aad
ms.contentlocale: tr-tr
ms.lasthandoff: 02/06/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="93cfe-103">Mobil iş cihazını kullanarak çalışanı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="93cfe-103">Configure a worker using the mobile job device</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93cfe-104">Bu yordam, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="93cfe-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="93cfe-105">Kullanıcı hesabına roller atama</span><span class="sxs-lookup"><span data-stu-id="93cfe-105">Assign roles to user account</span></span>
1. <span data-ttu-id="93cfe-106">Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.</span><span class="sxs-lookup"><span data-stu-id="93cfe-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="93cfe-107">Kullanıcı hesabının makine operatörü rolüyle ilişkili olduğu çalışanın adına filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="93cfe-108">Örnek verilerde çalışanın adı Shannon olacaktır.</span><span class="sxs-lookup"><span data-stu-id="93cfe-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="93cfe-109">Kullanıcı hesabı kaydını vurgulayın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="93cfe-110">Listede, kullanıcı hesabının ayrıntılarını görüntülemek için seçili satırdaki "Ad" bağlantısını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="93cfe-111">Ağaçta, 'Roller\Makine operatörü' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="93cfe-112">Kullanıcı hesabı ayrıntıları sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-112">Close the user account details page.</span></span>
7. <span data-ttu-id="93cfe-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="93cfe-114">Çalışan hesabını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-114">Configure worker account.</span></span>
1. <span data-ttu-id="93cfe-115">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="93cfe-116">Kullanıcı hesabının makine operatörü rolüyle ilişkili olduğu çalışanın adına filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="93cfe-117">Örnek verilerde çalışanın adı Shannon olacaktır.</span><span class="sxs-lookup"><span data-stu-id="93cfe-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="93cfe-118">Kullanıcı hesabı kaydını vurgulayın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="93cfe-119">Listede, kullanıcı hesabının ayrıntılarını görüntülemek için seçili satırdaki "Ad" bağlantısını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="93cfe-120">İstihdam sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="93cfe-121">Saat kayıt FastTab'ini genişletin ve kayıt terminallerinde etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="93cfe-122">Kayıt terminallerinde etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="93cfe-123">Hesaplama grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="93cfe-124">Varsayılan hesaplama grubu alanında +bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="93cfe-125">Onay grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="93cfe-126">Standart profil alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="93cfe-127">Profil grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="93cfe-128">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-128">Click OK.</span></span>
14. <span data-ttu-id="93cfe-129">Yeni zaman kayıt çalışanı için bir rozet numarası girmek için Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="93cfe-130">Rozet Kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="93cfe-131">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-131">Click Save.</span></span>
17. <span data-ttu-id="93cfe-132">SaveRecord kısayolunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="93cfe-133">Çalışan ayrıntıları sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-133">Close the worker details page.</span></span>
19. <span data-ttu-id="93cfe-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="93cfe-135">Cihaz grubuna çalışan atayın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="93cfe-136">Üretim denetimi > Ayarlar > Üretim yürütme > Cihazlar için iş kartını konfigüre et'e gidin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="93cfe-137">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-137">Click Add.</span></span>
3. <span data-ttu-id="93cfe-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="93cfe-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="93cfe-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-139">Click OK.</span></span>
5. <span data-ttu-id="93cfe-140">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-140">Click Edit.</span></span>
6. <span data-ttu-id="93cfe-141">Üretim birimi alanında çalışanın varsayılan filtresini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93cfe-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="93cfe-142">Bu, çalışan bu cihazda oturum açtığında yalnızca seçili üretim biriminin üretim işlerinin gösterilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="93cfe-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="93cfe-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="93cfe-143">Close the page.</span></span>

