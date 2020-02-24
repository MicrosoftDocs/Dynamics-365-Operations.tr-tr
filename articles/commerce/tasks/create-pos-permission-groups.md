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
ms.openlocfilehash: e6f9f8f970f336a0cce6bcac78e32a1b7fe0a252
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024324"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="b455b-103">POS izin grupları oluşturma</span><span class="sxs-lookup"><span data-stu-id="b455b-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b455b-104">Bu konu POS izin grubunun nasıl oluşturulacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="b455b-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="b455b-105">Bu görevi oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="b455b-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="b455b-106">Bu görev, Commerce operasyonları yöneticisi rolü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b455b-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="b455b-107">Gezinti bölmesinde **Modüller > Retail and Commerce > Personel > İzin grupları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="b455b-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="b455b-108">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-108">Select **New**.</span></span>
3. <span data-ttu-id="b455b-109">**POS izin grubu kimliği** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="b455b-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="b455b-110">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="b455b-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="b455b-111">**Saat girişlerini gör** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="b455b-112">Artık POS İzin grubunuz için çeşitli izinleri etkinleştirebilir veya devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b455b-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="b455b-113">Bazı izinler için POS kullanıcısının eylemi gerçekleştirip gerçekleştiremeyeceğini değerlendirmek amacıyla kullanılacak bir değer ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b455b-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="b455b-114">Bu görev kılavuzu bir kasiyere verilebilecek bazı izinleri etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="b455b-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="b455b-115">**Sipariş oluşturmaya izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="b455b-116">**Siparişi düzenlemeye izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="b455b-117">**Sipariş almaya izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="b455b-118">**Parola değiştirmeye izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="b455b-119">**Tamamen kapatmaya izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="b455b-120">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-120">Select **Save**.</span></span> <span data-ttu-id="b455b-121">Değişiklikleriniz kaydedildikten sonra, değişiklikleri Commerce kanallarına iletmek için Personel dağıtım planlamasını çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b455b-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="b455b-122">Gezinti bölmesinde **Modüller > İnsan kaynakları > İşler > İşler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b455b-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="b455b-123">Daha sonra, POS izin grubunu bir İşe atarız.</span><span class="sxs-lookup"><span data-stu-id="b455b-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="b455b-124">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b455b-125">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-125">Select **Edit**.</span></span>
15. <span data-ttu-id="b455b-126">**İş sınıflandırma** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="b455b-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="b455b-127">POS izin grubu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="b455b-128">Bu İşle ilgili Konumlarda bulunan tüm Çalışanlar, çalışanların POS izinleri Konum düzeylerinde geçersiz kılınmadığı sürece bu POS izin grubu ayarlarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="b455b-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="b455b-129">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b455b-129">Select **Save**.</span></span> <span data-ttu-id="b455b-130">Değişiklikleriniz kaydedildikten sonra, değişiklikleri kanallara iletmek için Personel dağıtım planlamasını çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b455b-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  

