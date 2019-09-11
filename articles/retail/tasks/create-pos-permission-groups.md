---
title: POS izin grupları oluşturma
description: Bu konu POS izin grubunun nasıl oluşturulacağını açıklar.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914847"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="934cd-103">POS izin grupları oluşturma</span><span class="sxs-lookup"><span data-stu-id="934cd-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="934cd-104">Bu konu POS izin grubunun nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="934cd-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="934cd-105">Bu görevi oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="934cd-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="934cd-106">Bu görev, Perakende operasyonları yöneticisi rolü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="934cd-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="934cd-107">Gezinti bölmesinde **Modüller > Perakende > Personel > İzin grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="934cd-107">In the navigation pane, go to **Modules > Retail > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="934cd-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-108">Select **New**.</span></span>
3. <span data-ttu-id="934cd-109">**POS izin grubu kimliği** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="934cd-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="934cd-110">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="934cd-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="934cd-111">**Saat girişlerini gör** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="934cd-112">Artık POS İzin grubunuz için çeşitli izinleri etkinleştirebilir veya devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="934cd-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="934cd-113">Bazı izinler için POS kullanıcısının eylemi gerçekleştirip gerçekleştiremeyeceğini değerlendirmek amacıyla kullanılacak bir değer ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="934cd-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="934cd-114">Bu görev kılavuzu bir kasiyere verilebilecek bazı izinleri etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="934cd-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="934cd-115">**Sipariş oluşturmaya izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="934cd-116">**Siparişi düzenlemeye izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="934cd-117">**Sipariş almaya izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="934cd-118">**Parola değiştirmeye izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="934cd-119">**Tamamen kapatmaya izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="934cd-120">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-120">Select **Save**.</span></span> <span data-ttu-id="934cd-121">Değişiklikleriniz kaydedildikten sonra, değişiklikleri perakende kanallarına itmek için Personel dağıtım planlamasını çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="934cd-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span> 
12. <span data-ttu-id="934cd-122">Gezinti bölmesinde **Modüller > İnsan kaynakları > İşler > İşler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="934cd-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="934cd-123">Daha sonra, POS izin grubunu bir İşe atarız.</span><span class="sxs-lookup"><span data-stu-id="934cd-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="934cd-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="934cd-125">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-125">Select **Edit**.</span></span>
15. <span data-ttu-id="934cd-126">**İş sınıflandırma** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="934cd-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="934cd-127">POS izin grubu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="934cd-128">Bu İşle ilgili Konumlarda bulunan tüm Çalışanlar, çalışanların POS izinleri Konum düzeylerinde geçersiz kılınmadığı sürece bu POS izin grubu ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="934cd-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="934cd-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="934cd-129">Select **Save**.</span></span> <span data-ttu-id="934cd-130">Değişiklikleriniz kaydedildikten sonra, değişiklikleri perakende kanallarına itmek için Personel dağıtım planlamasını çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="934cd-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  

