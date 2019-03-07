---
title: Mobil iş cihazını kullanarak çalışanı yapılandırma
description: Bu yordam, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "327401"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="e29a2-103">Mobil iş cihazını kullanarak çalışanı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e29a2-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e29a2-104">Bu yordam, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e29a2-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="e29a2-105">Kullanıcı hesabına roller atama</span><span class="sxs-lookup"><span data-stu-id="e29a2-105">Assign roles to user account</span></span>
1. <span data-ttu-id="e29a2-106">Sistem Yönetimi > Kullanıcılar > Kullanıcılar'a git.</span><span class="sxs-lookup"><span data-stu-id="e29a2-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="e29a2-107">Kullanıcı hesabının makine operatörü rolüyle ilişkili olduğu çalışanın adına filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="e29a2-108">Örnek verilerde çalışanın adı Shannon olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e29a2-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="e29a2-109">Kullanıcı hesabı kaydını vurgulayın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="e29a2-110">Listede, kullanıcı hesabının ayrıntılarını görüntülemek için seçili satırdaki "Ad" bağlantısını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="e29a2-111">Ağaçta, 'Roller\Makine operatörü' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="e29a2-112">Kullanıcı hesabı ayrıntıları sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-112">Close the user account details page.</span></span>
7. <span data-ttu-id="e29a2-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="e29a2-114">Çalışan hesabını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-114">Configure worker account.</span></span>
1. <span data-ttu-id="e29a2-115">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="e29a2-116">Kullanıcı hesabının makine operatörü rolüyle ilişkili olduğu çalışanın adına filtre uygulamak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="e29a2-117">Örnek verilerde çalışanın adı Shannon olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e29a2-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="e29a2-118">Kullanıcı hesabı kaydını vurgulayın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="e29a2-119">Listede, kullanıcı hesabının ayrıntılarını görüntülemek için seçili satırdaki "Ad" bağlantısını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="e29a2-120">İstihdam sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="e29a2-121">Saat kayıt FastTab'ini genişletin ve kayıt terminallerinde etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="e29a2-122">Kayıt terminallerinde etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="e29a2-123">Hesaplama grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="e29a2-124">Varsayılan hesaplama grubu alanında +bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="e29a2-125">Onay grubu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="e29a2-126">Standart profil alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="e29a2-127">Profil grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="e29a2-128">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-128">Click OK.</span></span>
14. <span data-ttu-id="e29a2-129">Yeni zaman kayıt çalışanı için bir rozet numarası girmek için Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="e29a2-130">Rozet Kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="e29a2-131">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-131">Click Save.</span></span>
17. <span data-ttu-id="e29a2-132">SaveRecord kısayolunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="e29a2-133">Çalışan ayrıntıları sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-133">Close the worker details page.</span></span>
19. <span data-ttu-id="e29a2-134">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="e29a2-135">Cihaz grubuna çalışan atayın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="e29a2-136">Üretim denetimi > Ayarlar > Üretim yürütme > Cihazlar için iş kartını konfigüre et'e gidin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="e29a2-137">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-137">Click Add.</span></span>
3. <span data-ttu-id="e29a2-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e29a2-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e29a2-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-139">Click OK.</span></span>
5. <span data-ttu-id="e29a2-140">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-140">Click Edit.</span></span>
6. <span data-ttu-id="e29a2-141">Üretim birimi alanında çalışanın varsayılan filtresini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e29a2-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="e29a2-142">Bu, çalışan bu cihazda oturum açtığında yalnızca seçili üretim biriminin üretim işlerinin gösterilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="e29a2-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="e29a2-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e29a2-143">Close the page.</span></span>

