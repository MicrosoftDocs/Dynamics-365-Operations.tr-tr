---
title: Genel muhasebe takvimini değiştirme veya yeniden atama
description: Bu konuda, genel muhasebeye atanmış olan takvimin nasıl değiştirileceği ve yeni bir takvimin genel muhasebeye nasıl atanacağı açıklanmaktadır.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039962"
---
# <a name="change-or-reassign-a-ledger-calendar"></a><span data-ttu-id="402a8-103">Genel muhasebe takvimini değiştirme veya yeniden atama</span><span class="sxs-lookup"><span data-stu-id="402a8-103">Change or reassign a ledger calendar</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="402a8-104">Bu konuda, genel muhasebeye atanmış olan takvimin nasıl değiştirileceği ve yeni bir takvimin genel muhasebeye nasıl atanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="402a8-104">This topic explains how to change the calendar that is currently assigned to a ledger, and how to assign a new calendar to the ledger.</span></span>

## <a name="issue"></a><span data-ttu-id="402a8-105">Sorun</span><span class="sxs-lookup"><span data-stu-id="402a8-105">Issue</span></span>

<span data-ttu-id="402a8-106">Zaman zaman şirketlerin genel muhasebeye atanan mevcut takvimi değiştirmesi veya yeni bir takvim ataması gerekir.</span><span class="sxs-lookup"><span data-stu-id="402a8-106">Sometime, companies must either change the existing calendar that is assigned to a ledger or assign a new calendar.</span></span>

## <a name="resolution"></a><span data-ttu-id="402a8-107">Çözüm</span><span class="sxs-lookup"><span data-stu-id="402a8-107">Resolution</span></span>

<span data-ttu-id="402a8-108">Genel muhasebe takvimini değiştirmeye veya yeniden atamaya yönelik iki senaryo vardır.</span><span class="sxs-lookup"><span data-stu-id="402a8-108">There are two scenarios for changing or reassigning a ledger calendar.</span></span> <span data-ttu-id="402a8-109">İlk senaryo, önceden genel muhasebeye atanmış mevcut bir takvimi değiştirmeyi kapsar.</span><span class="sxs-lookup"><span data-stu-id="402a8-109">The first scenario involves changing an existing calendar that is already assigned to the ledger.</span></span> <span data-ttu-id="402a8-110">İkinci senaryo yeni bir takvim oluşturmayı ve bunu genel muhasebeye atamayı kapsar.</span><span class="sxs-lookup"><span data-stu-id="402a8-110">The second scenario involves creating a new calendar and assigning it to the ledger.</span></span> <span data-ttu-id="402a8-111">Her iki değişiklik de işlemler genel muhasebeye nakledildikten sonra bile herhangi bir zamanda yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="402a8-111">Both changes can be done at any time, even after transactions have been posted to the ledger.</span></span>

### <a name="change-an-existing-fiscal-calendar"></a><span data-ttu-id="402a8-112">Mevcut mali takvimi değiştirme</span><span class="sxs-lookup"><span data-stu-id="402a8-112">Change an existing fiscal calendar</span></span>

<span data-ttu-id="402a8-113">Genel muhasebenize atanan mevcut bir takvimi değiştirmek için **Genel muhasebe \>Genel muhasebe kurulumu \> Muhasebe**'ye gidin ve **Genel muhasebe takvimleri** sayfasını açmak için mali takvimin bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="402a8-113">To change an existing calendar that is assigned to your ledger, go to **General ledger \> Ledger setup \> Ledger**, and select the link for the fiscal calendar to open the **Ledger calendars** page.</span></span>

<span data-ttu-id="402a8-114">Takvimde yapılabilecek değişikliklerle ilgili sınırlar vardır.</span><span class="sxs-lookup"><span data-stu-id="402a8-114">There are limits to the changes that can be made to a calendar.</span></span> <span data-ttu-id="402a8-115">Örneğin, bir yıldaki *dönemlerin* başlangıç ve bitiş tarihlerini değiştirebilirsiniz ancak takvimdeki bir *yılın* başlangıç ve bitiş tarihlerini değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="402a8-115">For example, you can change the start and end dates of the *periods* in a year, but you can't change the start and end dates of a *year* in the calendar.</span></span>

<span data-ttu-id="402a8-116">Bir yıldaki dönemleri değiştirmek için uygun takvimi ve yılı seçin.</span><span class="sxs-lookup"><span data-stu-id="402a8-116">To change the periods in a year, select the appropriate calendar and year.</span></span> <span data-ttu-id="402a8-117">İlk olarak, mevcut çalışma dönemlerinin bir kısmını veya tamamını silmek için **Dönemi sil** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="402a8-117">First, use the use the **Delete period** button to delete some or all of the existing operating periods.</span></span> <span data-ttu-id="402a8-118">İlki dışında tüm çalışma dönemleri silinebilir.</span><span class="sxs-lookup"><span data-stu-id="402a8-118">All operating periods except the first can be deleted.</span></span> <span data-ttu-id="402a8-119">Ardından, sonraki dönem için uygun bir başlangıç tarihi girerek kalan dönemi veya dönemleri yeni dönemlere bölmek için **Dönemi böl** düğmesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="402a8-119">Then use the **Divide period** button to divide the remaining period or periods into new periods by entering an appropriate start date for the next period.</span></span>

<span data-ttu-id="402a8-120">Takvimdeki dönemleri değiştirdikten sonra takvimin atandığı her tüzel kişilikte (şirkette) **Genel muhasebe dönemlerini yeniden hesapla** işlemini çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="402a8-120">After you change the periods in a calendar, you must run the **Recalculate ledger periods** process in every legal entity (company) that the calendar is assigned to.</span></span> <span data-ttu-id="402a8-121">Hiçbir uyarı iletisi size bu adımı tamamlamanızı hatırlatmasa da Genel muhasebede deftere nakledilmiş işlemlere atanan dönemi güncelleştirmek için yeniden hesaplama işlemi gerekir.</span><span class="sxs-lookup"><span data-stu-id="402a8-121">Although no warning message reminds you to complete this step, the recalculation process is required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="402a8-122">Yeniden hesaplama işlemini çalıştırmak için her şirkette **Genel muhasebe kurulumu** sayfasında **Genel muhasebe dönemlerini yeniden hesapla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="402a8-122">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page in each company.</span></span>

<span data-ttu-id="402a8-123">Yeniden hesaplama işlemi çalıştırılmazsa bir mizandaki veya mali tablolardaki işlem bakiyeleri dönemlere yanlış şekilde eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="402a8-123">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="402a8-124">Bu durumda, yeniden hesaplama işlemini çalıştırarak istediğiniz zaman bakiyeleri düzeltebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="402a8-124">In this case, you can correct the balances at any time by running the recalculation process.</span></span>

### <a name="assign-a-new-fiscal-calendar"></a><span data-ttu-id="402a8-125">Yeni bir mali takvim atama</span><span class="sxs-lookup"><span data-stu-id="402a8-125">Assign a new fiscal calendar</span></span>

<span data-ttu-id="402a8-126">Yeni bir mali takvim atamak için **Genel muhasebe \> Genel muhasebe kurulumu \> Muhasebe**'ye gidin ve **Düzenle**'yi seçerek **Genel muhasebe** sayfasını düzenleme moduna getirin.</span><span class="sxs-lookup"><span data-stu-id="402a8-126">To assign a new fiscal calendar, go to **General ledger \> Ledger setup \> Ledger**, and select **Edit** to put the **Ledger** page into edit mode.</span></span> <span data-ttu-id="402a8-127">Ardından **Mali takvim** alanında, yeni bir mali takvim seçin.</span><span class="sxs-lookup"><span data-stu-id="402a8-127">Then, in the **Fiscal calendar** field, select a new fiscal calendar.</span></span>

<span data-ttu-id="402a8-128">Genel muhasebe için mali takvimi değiştirdikten sonra **Genel muhasebe dönemlerini yeniden hesapla** işlemini çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="402a8-128">After you change the fiscal calendar for a ledger, you must run the **Recalculate ledger periods**.</span></span> <span data-ttu-id="402a8-129">Genel muhasebeye yeni bir mali takvim atadığınızda bir ileti size bu adımı tamamlamanız gerektiğini anımsatır.</span><span class="sxs-lookup"><span data-stu-id="402a8-129">When you assign a new fiscal calendar to a ledger, a message reminds you to complete this step.</span></span> <span data-ttu-id="402a8-130">İleti, yeniden hesaplama işleminin isteğe bağlı olduğunu belirtiyor gibi görünse de böyle bir durum yoktur.</span><span class="sxs-lookup"><span data-stu-id="402a8-130">Although the message might seem to indicate that the recalculation process is optional, it isn't.</span></span> <span data-ttu-id="402a8-131">Genel muhasebede deftere nakledilmiş işlemlere atanan dönemi güncelleştirmek için gereklidir.</span><span class="sxs-lookup"><span data-stu-id="402a8-131">It's required to update the period that is assigned to each posted transaction in General ledger.</span></span> <span data-ttu-id="402a8-132">Yeniden hesaplama işlemini çalıştırmak için **Genel muhasebe kurulumu** sayfasında **Genel muhasebe dönemlerini yeniden hesapla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="402a8-132">To run the recalculation process, select **Recalculate ledger periods** on the **Ledger setup** page.</span></span>

<span data-ttu-id="402a8-133">Yeniden hesaplama işlemi çalıştırılmazsa bir mizandaki veya mali tablolardaki işlem bakiyeleri dönemlere yanlış şekilde eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="402a8-133">If the recalculation process isn't run, transaction balances on a trial balance or on financial statements might be incorrectly included in periods.</span></span> <span data-ttu-id="402a8-134">Bu durumda, yeniden hesaplama işlemini çalıştırarak istediğiniz zaman bakiyeleri düzeltebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="402a8-134">In this case, you can correct the balances at any time by running the recalculation process.</span></span>
