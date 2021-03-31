---
title: İş emrini belirli bir tarihte ve saatte zamanlama
description: Bu konu, Varlık Yönetiminde, iş emrinin belirli bir tarih ve saate nasıl planlanacağını açıklamaktadır.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 921e78f2fc7e6254aa27ce70cdbbf0516aad7e11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214998"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="e5bf4-103">İş emrini belirli bir tarihte ve saatte zamanlama</span><span class="sxs-lookup"><span data-stu-id="e5bf4-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e5bf4-104">Bir iş emrinin belirli bir tarih *ve* saatte zamanlanması gerekiyorsa, Varlık Yönetiminde standart planlama sürecini geçersiz kılabilir ve bir iş emri için belirli bir plan oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="e5bf4-105">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e5bf4-106">İş emri listesinde, **İş emri** sütunundaki İş emri koduna tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="e5bf4-107">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-107">Click **Edit**.</span></span>

4. <span data-ttu-id="e5bf4-108">**İş emri başlığı** hızlı sekmesinde, **Beklenen başlangıç** ve **Beklenen bitiş** alanlarına başlangıç ve bitiş tarihlerini ve saatlerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![Şekil 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="e5bf4-110">**Genel** sekmesinde, standart planlama işlemini kullanmak için **Zamanla**'ya tıklayın veya iş emrini belirli bir çalışana atamak istiyorsanız **Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="e5bf4-111">İş emrinin beklenen dönemde zamanlandığından emin olmak amacıyla varolan herhangi bir kapasite rezervasyonunu geçersiz kılmak için **İş emrini planla** iletişim kutusu > **Sınırlı kapasite** bölümünde aşağıdaki şekilde gösterilen seçimleri yapın.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="e5bf4-112">Bu, iş emrinin beklenen başlangıç saatinde başlaması gerektiği için, planlama işleminin varolan kapasite rezervasyonlarını yok sayacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![Şekil 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="e5bf4-114">Planlamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="e5bf4-115">Planlama süreci çift ayırmaya neden olursa, ekranda bir ileti görüntülenir ve ilgili iş emirlerini ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="e5bf4-116">İş emri için bir bakım görevlisi planlamak için bu bakım görevlisinin beklenen başlangıç tarihi ve saatinde uygun olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="e5bf4-117">Çalışanın uygunluk durumu [çalışan takviminde](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md) ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e5bf4-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]