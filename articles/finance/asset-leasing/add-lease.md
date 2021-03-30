---
title: Kiralama ekleme veya kopyalama (Önizleme)
description: Bu konuda, Varlık kiralamada kiralamaya ilişkin bilgi girerek veya mevcut bir kiralamadaki bilgileri kopyalayarak yeni bir kiralama oluşturma açıklanmaktadır.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 325a1b7948f3cb8033fa93b7c36f1f1f6b7dbb27
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220023"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="46ad5-103">Kiralama ekleme veya kopyalama (Önizleme)</span><span class="sxs-lookup"><span data-stu-id="46ad5-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46ad5-104">Bu konuda, Varlık kiralamada sıfırdan kiralama oluşturma ve mevcut bir kiralamayı kopyalayarak kiralama oluşturma yöntemleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="46ad5-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="46ad5-105">Sıfırdan kiralama oluşturma işlemi, yeni kiralamaya ilişkin bilgilerin girilmesini ve sonra bir kiralama planlamasının oluşturulmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="46ad5-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="46ad5-106">En az bir kiralama ayarladıktan sonra, bilgileri mevcut bir kiralamadan kopyalayıp daha sonra yeni bir kiralama oluşturmak için bu bilgileri düzenlemeniz daha kolay olabilir.</span><span class="sxs-lookup"><span data-stu-id="46ad5-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="46ad5-107">Kiralama oluşturma</span><span class="sxs-lookup"><span data-stu-id="46ad5-107">Create a lease</span></span>

<span data-ttu-id="46ad5-108">Varlık kiralamada kiralama oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="46ad5-109">**Kiralama özeti** sayfasındaki Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="46ad5-110">Kiralama bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-110">Enter the lease information.</span></span> <span data-ttu-id="46ad5-111">Gerekli alanların kırmızı kenarlıkları vardır.</span><span class="sxs-lookup"><span data-stu-id="46ad5-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="46ad5-112">Kiralama planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="46ad5-112">Create a lease schedule</span></span>

<span data-ttu-id="46ad5-113">Kiralamaya ilişkin bilgileri girmeyi tamamladıktan sonra, kiralama planı oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="46ad5-114">Mali boyutlar özel mali boyutlara göre değişebilir.</span><span class="sxs-lookup"><span data-stu-id="46ad5-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="46ad5-115">Kiralama defterleri oluşturmak için **Planlama oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="46ad5-116">Kiralama defterleri arasında ödeme, itfa, amortisman ve gider planlamaları yer alır.</span><span class="sxs-lookup"><span data-stu-id="46ad5-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="46ad5-117">Kiralama defterlerine erişmek ve yeni oluşturulan planlamaları görüntülemek için **Defterler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="46ad5-118">**Defter ayrıntıları** sayfası, kiralamaya tahsis edilmiş olan defterlerde kiralamanın nasıl hesaplandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46ad5-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="46ad5-119">Buradan, kira planlamalarını görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46ad5-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="46ad5-120">Ödeme planı, **Kiralama ekle** sayfasındaki **Ödeme planı satırları** sekmesinden alınan girişleri içerir.</span><span class="sxs-lookup"><span data-stu-id="46ad5-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="46ad5-121">Her ödeme tutarını ve değişken ödemeyi değiştirmeye devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46ad5-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="46ad5-122">Kiralama yükümlülüğü değiştirilen ödeme planına göre hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="46ad5-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="46ad5-123">Ödeme planını incelemeyi tamamladıktan sonra **Planlamayı onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="46ad5-124">Planlama onaylandıktan sonra kiralama, artık düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="46ad5-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46ad5-125">Sistem, kiralama süresini **Kiralama ekle** sayfasındaki ödeme planı satırlarından otomatik olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="46ad5-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="46ad5-126">Kiralama süresini aylık olarak hesaplamak için sistem, belirli bir ödeme planı satırında başlangıç tarihi ile bitiş tarihi arasındaki farkı bulur.</span><span class="sxs-lookup"><span data-stu-id="46ad5-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="46ad5-127">Ardından, sonraki ödeme planı satırına gider ve farkı tekrar bulur.</span><span class="sxs-lookup"><span data-stu-id="46ad5-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="46ad5-128">Son olarak, sistem kiralama süresini aylık olarak belirlemek için tüm tutarları toplar.</span><span class="sxs-lookup"><span data-stu-id="46ad5-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="46ad5-129">Hesaplanan dönem içi faiz giderlerini görüntülemek için **Kira yükümlülüğü amortisman planlaması** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="46ad5-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="46ad5-130">Hesaplanan sabit amortismanı görüntülemek için **Varlık amortisman planlaması** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="46ad5-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="46ad5-131">Hesaplanan tutarı incelemeyi tamamladıktan sonra **İlk kabul** sayfasında ilk kabul günlüğü girişinizi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46ad5-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="46ad5-132">Günlüğün oluşturulduğunu bildiren bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="46ad5-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46ad5-133">Girişi el ile deftere nakledene kadar günlük girişi Genel muhasebeye nakledilmez.</span><span class="sxs-lookup"><span data-stu-id="46ad5-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="46ad5-134">Önerilen ilk kabul girişini deftere nakletmeden önce gözden geçirmek için **Varlık kiralama günlükleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46ad5-135">Varlık kiralama günlüğü el ile oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="46ad5-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="46ad5-136">Kiralama planları oluşturulduğunda otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="46ad5-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="46ad5-137">İlk kabul günlüğü girişini gözden geçirmeyi bitirdiğinizde ve deftere nakletmeye hazır olduğunuzda, kullanım hakkı (ROU) varlığını ve kiralama yükümlülüğünü Genel muhasebede tanımak için **Deftere nakil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="46ad5-138">Kiralamayı kopyalama</span><span class="sxs-lookup"><span data-stu-id="46ad5-138">Copy a lease</span></span>

<span data-ttu-id="46ad5-139">Varlık kiralama, aynı bilgilere sahip olan yeni bir kiralama oluşturmak için kira ayrıntılarını kopyalamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="46ad5-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="46ad5-140">Daha sonra, kopyalanan kiralama için plan oluşturmadan önce kiralama alanlarını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46ad5-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="46ad5-141">**Kiralama özeti** sayfasında, kopyalanacak kirayı seçin ve sonra Eylem bölmesinde **Kiralamayı kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="46ad5-142">Kiralama kodlarının numara sırası için **El ile** parametresi kapatılmışsa, dizideki bir sonraki numara otomatik olarak kopyalanan kiralamanın kiralama kodu olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="46ad5-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="46ad5-143">**El ile** parametresi açıksa kiralamayı kopyalama işlemine devam etmeden önce kiralama kodunu girmenizi isteyen bir ileti alırsınız.</span><span class="sxs-lookup"><span data-stu-id="46ad5-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="46ad5-144">**Kopyala** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="46ad5-144">Select **Copy**.</span></span> <span data-ttu-id="46ad5-145">Seçili kiralamadan alınan kiralama ayrıntıları yeni kiralamaya kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="46ad5-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="46ad5-146">Ardından, kaydetmeden önce yeni kiralamanın ayrıntılarını düzenleyebilir ve kira planlarını oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46ad5-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="46ad5-147">Varlık kiralama günlüğü</span><span class="sxs-lookup"><span data-stu-id="46ad5-147">Asset leasing journal</span></span>

<span data-ttu-id="46ad5-148">Varlık kiralamada oluşturulan tüm günlük girişleri, Varlık kiralama günlüğünde yer alır.</span><span class="sxs-lookup"><span data-stu-id="46ad5-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="46ad5-149">**Varlık kiralama günlüğü** sayfasında (**Varlık kiralama \> Günlük girişleri \> Varlık kiralama günlüğü**), deftere nakil durumuna göre filtre uygulayabilir, belirli günlük girişlerini ve fişleri görüntüleyebilir ve deftere nakledilmemiş günlük girişlerini deftere nakledebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="46ad5-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="46ad5-150">Varlık kiralama günlüğü el ile oluşturulamaz.</span><span class="sxs-lookup"><span data-stu-id="46ad5-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="46ad5-151">Kiralama planları oluşturulduğunda otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="46ad5-151">It's automatically created when lease schedules are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]