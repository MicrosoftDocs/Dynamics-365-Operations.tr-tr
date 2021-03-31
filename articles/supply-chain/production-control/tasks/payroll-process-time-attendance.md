---
title: Personel saat ve işe devam için bordro işlemini etkinleştirme
description: Bu yordamda, saat ve işe devam için bordro işleminin nasıl etkinleştirileceği gösterilir.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72b925feb8f784c257656dd93b48c9c0cc66da5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214926"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="88ae9-103">Personel saat ve işe devam için bordro işlemini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="88ae9-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88ae9-104">Bu yordamda, saat ve işe devam için bordro işleminin nasıl etkinleştirileceği gösterilir.</span><span class="sxs-lookup"><span data-stu-id="88ae9-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="88ae9-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="88ae9-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="88ae9-106">İlgili ödeme oranıyla ödeme türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ae9-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="88ae9-107">Saat ve işe devam > Kurulum > Bordro > Ödeme türleri</span><span class="sxs-lookup"><span data-stu-id="88ae9-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="88ae9-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-108">Click New.</span></span>
3. <span data-ttu-id="88ae9-109">Ödeme türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="88ae9-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="88ae9-111">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-111">Click Save.</span></span>
6. <span data-ttu-id="88ae9-112">Oranlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-112">Click Rates.</span></span>
    * <span data-ttu-id="88ae9-113">Ödeme türleri için oranlar belirli zaman aralıkları için ayarlanır ve çalışanlar için bireysel oranlar oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="88ae9-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="88ae9-114">Saat ve işe devamdaki ödeme türleri için oran oluşturmak her zaman gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="88ae9-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="88ae9-115">Bu bilgi, ücretleri oluşturmak için kullanılan bordro sisteminde bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="88ae9-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="88ae9-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-116">Click New.</span></span>
8. <span data-ttu-id="88ae9-117">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="88ae9-118">Oran alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="88ae9-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="88ae9-120">Ödeme anlaşması oluşturma</span><span class="sxs-lookup"><span data-stu-id="88ae9-120">Create a pay agreement</span></span>
1. <span data-ttu-id="88ae9-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-121">Close the page.</span></span>
2. <span data-ttu-id="88ae9-122">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-122">Close the page.</span></span>
3. <span data-ttu-id="88ae9-123">Ödeme anlaşmalarına gidin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="88ae9-124">Saat ve işe devam > Kurulum > Ödeme anlaşmaları</span><span class="sxs-lookup"><span data-stu-id="88ae9-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="88ae9-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-125">Click New.</span></span>
5. <span data-ttu-id="88ae9-126">Ödeme anlaşması alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="88ae9-127">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="88ae9-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-128">Click Save.</span></span>
8. <span data-ttu-id="88ae9-129">Anlaşma satırlarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="88ae9-130">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-130">Click New.</span></span>
10. <span data-ttu-id="88ae9-131">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="88ae9-132">Profil türü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="88ae9-133">Ödeme türü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="88ae9-134">Süre ve kayıtlı çalışan için ödeme anlaşması ayarlama</span><span class="sxs-lookup"><span data-stu-id="88ae9-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="88ae9-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-135">Close the page.</span></span>
2. <span data-ttu-id="88ae9-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-136">Close the page.</span></span>
3. <span data-ttu-id="88ae9-137">Zaman kayıtlı çalışanlar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="88ae9-138">Saat ve işe devam > Kurulum > Zaman kayıtlı çalışanlar</span><span class="sxs-lookup"><span data-stu-id="88ae9-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="88ae9-139">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="88ae9-140">İstihdam sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="88ae9-141">Zaman kaydı bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="88ae9-142">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="88ae9-142">Click Edit.</span></span>
8. <span data-ttu-id="88ae9-143">Ödeme anlaşması alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="88ae9-143">In the Pay agreement field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]