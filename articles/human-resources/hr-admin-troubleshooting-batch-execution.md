---
title: Takılmış toplu işleri sıfırlama
description: Bu konu, takılan toplu işlerle ilgili sorunların nasıl giderileceğini açıklamaktadır.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d0b12908993070a41d21ac57d6fb504fc6e3b06a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053527"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="67aa6-103">Takılmış toplu işleri sıfırlama</span><span class="sxs-lookup"><span data-stu-id="67aa6-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="67aa6-104">Çıkış</span><span class="sxs-lookup"><span data-stu-id="67aa6-104">Issue</span></span>

<span data-ttu-id="67aa6-105">Microsoft Dynamics 365 Human Resources, **çalıştırılıyor** veya **iptal ediliyor** durumunda takılı kalan ve tamamlanmayan toplu işlerle ilgili sorunlar yaşayabilir.</span><span class="sxs-lookup"><span data-stu-id="67aa6-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="67aa6-106">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="67aa6-106">Resolution</span></span>

<span data-ttu-id="67aa6-107">Toplu iş, **çalıştırılıyor** veya **iptal ediliyor** durumunda takılı kaldığında işin iptal edilmesini zorlayarak durumu sıfırlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="67aa6-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="67aa6-108">Bunu iptal ettikten sonra, toplu işi **bekliyor** durumuna ayarlayarak sıfırlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="67aa6-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="67aa6-109">Daha sonra, zamanlanan bir sonraki toplu işte yürütülmek üzere yeniden alınır.</span><span class="sxs-lookup"><span data-stu-id="67aa6-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="67aa6-110">**Sistem Yönetimi** çalışma alanında, **Bağlantılar** sayfasını seçin ve **toplu işler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="67aa6-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="67aa6-111">**Toplu iş** liste sayfasında, sıfırlanması gereken işi seçin.</span><span class="sxs-lookup"><span data-stu-id="67aa6-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="67aa6-112">Eylem şeridinde, **iptal etmeye zorla**'yı seçin ve eylemi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="67aa6-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="67aa6-113">**İptal etmeye zorla** eylemi, yalnızca seçilen toplu işin durumu **çalıştırılıyor** veya **iptal ediliyor** olduğunda ve iş için hiçbir toplu yürütme veya iptal işlemi çalıştırılmazken kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="67aa6-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="67aa6-114">Eylem şeridinde **Durumu değiştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="67aa6-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="67aa6-115">**Yeni durum Seç** sayfasında, **bekliyor**'u seçin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="67aa6-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Yeni bir toplu iş durumu seç](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="67aa6-117">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="67aa6-117">See also</span></span>

[<span data-ttu-id="67aa6-118">Toplu işleri çalışma saatleri dışına planlayarak performansını en iyi duruma getirme</span><span class="sxs-lookup"><span data-stu-id="67aa6-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="67aa6-119">Otomatik temizleme görevleriyle performansı en iyi duruma getirme</span><span class="sxs-lookup"><span data-stu-id="67aa6-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
