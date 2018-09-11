--- 
title: " POS izin grupları oluşturma"
description: "Bu yordam bir POS izni grubunun nasıl oluşturulacağını gösterir."
author: scott-tucker
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c5bb77b0cc4d81e2cceb8c17760fe0b84d2c575d
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="b1256-103"> POS izin grupları oluşturma</span><span class="sxs-lookup"><span data-stu-id="b1256-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b1256-104">Bu yordam bir POS izni grubunun nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1256-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="b1256-105">Bu görevi oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="b1256-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="b1256-106">Bu görev, Perakende operasyonları yöneticisi rolü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b1256-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="b1256-107">İzin gruplarına gidin.</span><span class="sxs-lookup"><span data-stu-id="b1256-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="b1256-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1256-108">Click New.</span></span>
3. <span data-ttu-id="b1256-109">POS izin grubu kimliği alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b1256-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="b1256-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b1256-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b1256-111">Saat girişlerini gör alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b1256-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="b1256-112">Artık POS İzin grubunuz için çeşitli izinleri etkinleştirebilir veya devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1256-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="b1256-113">Bazı izinler için POS kullanıcısının eylemi gerçekleştirip gerçekleştiremeyeceğini değerlendirmek amacıyla kullanılacak bir değer ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1256-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="b1256-114">Bu görev kılavuzu bir kasiyere verilebilecek bazı izinleri etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="b1256-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="b1256-115">Sipariş oluşturmaya izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b1256-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="b1256-116">Siparişi düzenlemeye izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b1256-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="b1256-117">Sipariş almaya izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b1256-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="b1256-118">Parola değiştirmeye izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b1256-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="b1256-119">Tamamen kapatmaya izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b1256-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="b1256-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1256-120">Click Save.</span></span>
    * <span data-ttu-id="b1256-121">Değişiklikleriniz kaydedildikten sonra, değişiklikleri perakende kanallarına itmek için Personel dağıtım planlamasını çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b1256-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="b1256-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b1256-122">Close the page.</span></span>
13. <span data-ttu-id="b1256-123">İşlere gidin.</span><span class="sxs-lookup"><span data-stu-id="b1256-123">Go to Jobs.</span></span>
    * <span data-ttu-id="b1256-124">Daha sonra, POS izin grubunu bir İşe atarız.</span><span class="sxs-lookup"><span data-stu-id="b1256-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="b1256-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b1256-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b1256-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1256-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b1256-127">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b1256-127">Click Edit.</span></span>
17. <span data-ttu-id="b1256-128">İş sınıflandırma bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b1256-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="b1256-129">POS izin grubu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b1256-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="b1256-130">Bu İşle ilgili Konumlarda bulunan tüm Çalışanlar, çalışanların POS izinleri Konum düzeylerinde geçersiz kılınmadığı sürece bu POS izin grubu ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="b1256-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="b1256-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b1256-131">Click Save.</span></span>
    * <span data-ttu-id="b1256-132">Değişiklikleriniz kaydedildikten sonra, değişiklikleri perakende kanallarına itmek için Personel dağıtım planlamasını çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b1256-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


