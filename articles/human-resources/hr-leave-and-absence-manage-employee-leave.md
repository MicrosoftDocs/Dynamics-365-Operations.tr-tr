---
title: Personel iznini yönetme
description: Dynamics 365 Human Resources'ta personel iznini yönetme
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 33080fc5ca43f3d83ee9d17565f4c229ced7b94f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055640"
---
# <a name="manage-employee-leave"></a><span data-ttu-id="f3469-103">Personel iznini yönetme</span><span class="sxs-lookup"><span data-stu-id="f3469-103">Manage employee leave</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f3469-104">Bir çalışanın iznini izin türü ile yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3469-104">You can manage an employee's leave by leave type.</span></span> <span data-ttu-id="f3469-105">Buna, izin kaydı süresini sona erdirme ve izin türü bakiyelerini ayarlama da dahildir.</span><span class="sxs-lookup"><span data-stu-id="f3469-105">This includes expiring leave enrollment and adjusting leave type balances.</span></span> 

## <a name="adjust-leave-balances"></a><span data-ttu-id="f3469-106">İzin bakiyelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f3469-106">Adjust leave balances</span></span>

1. <span data-ttu-id="f3469-107">Çalışanın kaydında, **izin** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f3469-107">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="f3469-108">**İzin ve devamsızlık ayarı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3469-108">Select **Leave and absence setup**.</span></span>

3. <span data-ttu-id="f3469-109">**Bakiye ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3469-109">Select **Adjust balance**.</span></span>

4. <span data-ttu-id="f3469-110">**İzin türü**'nü seçin.</span><span class="sxs-lookup"><span data-stu-id="f3469-110">Select the **Leave type**.</span></span>

5. <span data-ttu-id="f3469-111">**Ayarlama tutarı** girin.</span><span class="sxs-lookup"><span data-stu-id="f3469-111">Enter an **Adjustment amount**.</span></span> 

6. <span data-ttu-id="f3469-112">İsteğe bağlı olarak, bir **Tarih** seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3469-112">Optionally, you can select a **Date**.</span></span> 

<span data-ttu-id="f3469-113">Bir çalışanın izin bakiyesini ayarlarken bir neden kodu ve açıklama ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3469-113">You can include a reason code and comment when adjusting an employee's leave balance.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="f3469-114">Bakiyelerdeki bakiye ile ilgili ek bilgileri görüntülemek önizlemede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="f3469-114">Viewing additional information about leave balances is in preview.</span></span> <span data-ttu-id="f3469-115">Bunu **korumalı alan** ortamınızda etkinleştirmeniz gerekir .</span><span class="sxs-lookup"><span data-stu-id="f3469-115">You'll need to enable it in your **Sandbox** environment.</span></span> <span data-ttu-id="f3469-116">Önizleme özelliklerini etkinleştirme hakkında daha fazla bilgi edinmek için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="f3469-116">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br>
><span data-ttu-id="f3469-117">Herhangi bir bırakma bakiyesinin üzerine getirildiğinde şu şekilde görüntülenir:</span><span class="sxs-lookup"><span data-stu-id="f3469-117">When hovering over any leave balance, you will now see:</span></span><br>
>- <span data-ttu-id="f3469-118">**Kullanılabilir**: Bu yılki toplam-bu yılı al</span><span class="sxs-lookup"><span data-stu-id="f3469-118">**Available**: Total this year - Take this year</span></span>
>- <span data-ttu-id="f3469-119">**Bu yılın toplamı**: Tüm tahakkukları, ayarlamalar ve bu yıl için ileriye doğru Yürüt</span><span class="sxs-lookup"><span data-stu-id="f3469-119">**Total this year**: All accruals, adjustments, and carry forward for the year</span></span>
>- <span data-ttu-id="f3469-120">**Bu yıl uygulanan**: tüm onaylanan zaman kapalı</span><span class="sxs-lookup"><span data-stu-id="f3469-120">**Taken this year**: All approved time off</span></span>

## <a name="see-also"></a><span data-ttu-id="f3469-121">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="f3469-121">See also</span></span>

- [<span data-ttu-id="f3469-122">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="f3469-122">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="f3469-123">İzin ve devamsızlık isteklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="f3469-123">Manage leave and absence requests</span></span>](hr-employee-self-service-manage-requests.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]