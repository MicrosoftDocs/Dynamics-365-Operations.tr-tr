---
title: Mobil iş cihazını kullanarak çalışanı yapılandırma
description: Bu konu, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6e45ea8fdbe30436badd88d4972fda970755275
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835799"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="aa1d8-103">Mobil iş cihazını kullanarak çalışanı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="aa1d8-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa1d8-104">Bu konu, çalışanın kullanıcı hesabına doğru rollerin nasıl atanacağını ve atölye kayıtları yapacak çalışanın nasıl etkinleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="aa1d8-105">Bir çalışanın belirli bir role atanmasını doğrulayın</span><span class="sxs-lookup"><span data-stu-id="aa1d8-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="aa1d8-106">Bu örnekte, çalışan hesabı yapılandırmadan önce "SHANNON" kullanıcısının makine operatörü rolüne atanacağını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="aa1d8-107">**Gezinti bölmesi > Modüller > Sistem yönetimi > Kullanıcılar > Kullanıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="aa1d8-108">Hızlı filtrede bir kullanıcı arayın.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="aa1d8-109">Bu örnek için, `shannon` girin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="aa1d8-110">Görüntülenen kullanıcı hesabının **Kullanıcı kimliği** sütununda bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="aa1d8-111">**Kullanıcı rolleri** ağacında **Roller > Makine operatörü** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="aa1d8-112">Giriş sayfasına dönmek için **Kullanıcı ayrıntıları** ve **kullanıcılar** sayfalarını kapatın.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="aa1d8-113">Çalışan hesabını yapılandırın</span><span class="sxs-lookup"><span data-stu-id="aa1d8-113">Configure worker account</span></span>
1. <span data-ttu-id="aa1d8-114">**Gezinti bölmesi > Modüller > İnsan kaynakları > İşçiler > İşçiler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="aa1d8-115">Hızlı filtrede bir kullanıcı arayın.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="aa1d8-116">Bu örnek için, `shannon` girin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="aa1d8-117">Görüntülenen kullanıcı hesabının **Ad** sütununda bağlantıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="aa1d8-118">**Saat kaydı** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="aa1d8-119">**Kayıt terminallerinde etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="aa1d8-120">Aşağıdaki alanlara değerleri girin vey seçin:</span><span class="sxs-lookup"><span data-stu-id="aa1d8-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="aa1d8-121">**Hesaplama grubu**</span><span class="sxs-lookup"><span data-stu-id="aa1d8-121">**Calculation group**</span></span>  
    - <span data-ttu-id="aa1d8-122">**Varsayılan hesaplama grubu**</span><span class="sxs-lookup"><span data-stu-id="aa1d8-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="aa1d8-123">**Onay grubu**</span><span class="sxs-lookup"><span data-stu-id="aa1d8-123">**Approval group**</span></span>  
    - <span data-ttu-id="aa1d8-124">**Standart profil**</span><span class="sxs-lookup"><span data-stu-id="aa1d8-124">**Standard profile**</span></span>  
    - <span data-ttu-id="aa1d8-125">**Profil grubu**</span><span class="sxs-lookup"><span data-stu-id="aa1d8-125">**Profile group**</span></span>  

7. <span data-ttu-id="aa1d8-126">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-126">Select **OK**.</span></span>
8. <span data-ttu-id="aa1d8-127">Yeni zaman kayıt çalışanı için bir rozet numarası girmek için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="aa1d8-128">**Rozet kodu** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="aa1d8-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-129">Select **Save**.</span></span>
10. <span data-ttu-id="aa1d8-130">**Çalışan ayrıntıları** ve **İşçiler** sayfalarını kapatın.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="aa1d8-131">Cihaz grubuna çalışan atayın</span><span class="sxs-lookup"><span data-stu-id="aa1d8-131">Assign worker to device group</span></span>
1. <span data-ttu-id="aa1d8-132">**Üretim denetimi > Ayarlar > Üretim yürütme > Cihazlar için iş kartını konfigüre et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="aa1d8-133">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-133">Select **Add**.</span></span>
3. <span data-ttu-id="aa1d8-134">Listede, istediğiniz çalışanı seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-134">In the list, select the desired worker.</span></span> <span data-ttu-id="aa1d8-135">Bu örnek için **SHANNON** seçeneğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="aa1d8-136">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-136">Select **OK**.</span></span>
5. <span data-ttu-id="aa1d8-137">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-137">Select **Edit**.</span></span>
6. <span data-ttu-id="aa1d8-138">**Üretim birimi** alanında çalışanın varsayılan filtresini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="aa1d8-139">Bu, çalışan bu cihazda oturum açtığında yalnızca seçili üretim biriminin üretim işlerinin gösterilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="aa1d8-140">İstenen değeri girin.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-140">Enter the desired value.</span></span>
7. <span data-ttu-id="aa1d8-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aa1d8-141">Close the page.</span></span>

