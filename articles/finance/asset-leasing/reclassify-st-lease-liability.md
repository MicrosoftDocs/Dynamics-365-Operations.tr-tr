---
title: Kiralama yükümlülüğünün kısa vadeli bölümünü yeniden sınıflandırma
description: Bu konu, kiralama yükümlülüğünün bir bölümünü kısa süreli olarak yeniden sınıflandırmak için aylık günlük girdisinin nasıl oluşturulacağını açıklamaktadır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ae5aebab507479775626579e8b08d68001326a06
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881578"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="2d98a-103">Kiralama yükümlülüğünün kısa süreli bölümünü yeniden sınıflandırma</span><span class="sxs-lookup"><span data-stu-id="2d98a-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d98a-104">Bu konu, kiralama yükümlülüğünün bir bölümünü kısa süreli olarak yeniden sınıflandırmak için aylık günlük girdisinin nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2d98a-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="2d98a-105">Toplu iş işleminde seçilen plan **Kısa süreli kira yükümlülüğü yeniden sınıflandırma** olduğunda bir günlük girişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2d98a-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="2d98a-106">Bu giriş, ayın son gününe kiralama yükümlülüğünün geçerli bölümünü deftere nakletmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2d98a-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="2d98a-107">Aynı zamanda, sonraki ayın ilk günü itibarıyla ters kayıt girişi de deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="2d98a-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="2d98a-108">Kiralama yükümlülüğünün kısa süreli kısmı, yükümlülük amortisman planında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="2d98a-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="2d98a-109">Günlük girişi deftere nakledildiğinde, **Yükümlülük yeniden sınıflama günlüğü oluşturuldu** sütunu kullanılabilir duruma gelir ve günlük kimliği de plana göre doldurulur.</span><span class="sxs-lookup"><span data-stu-id="2d98a-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="2d98a-110">Kısa süreli yükümlülük yeniden sınıflama günlüğü girişi oluşturmak ve deftere nakletmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2d98a-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="2d98a-111">**Varlık kiralama \> Periyodik \> Toplu iş günlük oluşturma** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="2d98a-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="2d98a-112">**Toplu iş günlük oluşturma** iletişim kutusundaki **Plan seçin** alanında **Kısa süreli kiralama yükümlülüğünü yeniden sınıflandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="2d98a-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="2d98a-113">**Kiralama grubu** alanında bir kiralama grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="2d98a-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="2d98a-114">Bunun yerine, **Defter Kimliği** alanında defter kimliğini de seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d98a-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="2d98a-115">**Deftere naklet** parametresini açın.</span><span class="sxs-lookup"><span data-stu-id="2d98a-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="2d98a-116">Girişin oluşturulması ancak deftere nakledilmemesi gerekiyorsa bunun yerine parametreyi kapalı bırakın.</span><span class="sxs-lookup"><span data-stu-id="2d98a-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="2d98a-117">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2d98a-117">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
