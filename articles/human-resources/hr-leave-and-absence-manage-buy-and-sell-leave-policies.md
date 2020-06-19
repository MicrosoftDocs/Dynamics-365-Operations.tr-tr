---
title: İzin satın alma ve satma ilkelerini yönetme
description: Dynamics 365 Human Resources'ta çalışanların izin satın alma ve satma olanağı sağlayabilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429025"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="1fa97-103">İzin satın alma ve satma ilkelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="1fa97-103">Manage buy and sell leave policies</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1fa97-104">Çalışanların bir izin satınalma ilkesi oluşturarak izin satın alması için bunu etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1fa97-104">You can enable employees to buy leave by creating a buy leave policy.</span></span>  

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="1fa97-105">Çalışanların izin satın alma ve satma olanağını etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="1fa97-105">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="1fa97-106">**İzin ve devamsızlık parametreleri** sayfasında, **çalışanların izin satın almasına izin vermek** için **Evet** 'i seçin .</span><span class="sxs-lookup"><span data-stu-id="1fa97-106">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave**.</span></span> 

## <a name="create-a-buy-leave-policy"></a><span data-ttu-id="1fa97-107">İzin satınalma İlkesi Oluştur</span><span class="sxs-lookup"><span data-stu-id="1fa97-107">Create a buy leave policy</span></span>

1. <span data-ttu-id="1fa97-108">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-108">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="1fa97-109">**İzin satın alma ve satma ilkesi** seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-109">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="1fa97-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-110">Select **New**.</span></span>

4. <span data-ttu-id="1fa97-111">İlke için**İzin Satınalma ve satma ilkesi** altındaki bir **ad** ve **açıklama** girin .</span><span class="sxs-lookup"><span data-stu-id="1fa97-111">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="1fa97-112">Bir **İlke türü** seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-112">Select a **Policy type**.</span></span> 

   <span data-ttu-id="1fa97-113">Kullanılabilir ilke türleri haftalık **tutar** ve **saat sayısı**.</span><span class="sxs-lookup"><span data-stu-id="1fa97-113">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="1fa97-114">Çalışanların satın alabileceği ve satılabilecek maksimum tutarlar için **sabit bir tutar** girmek üzere **tutar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-114">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="1fa97-115">**Haftalık saatleri** seçerseniz , çalışanın atadığı çalışma tarihi takviminde tanımlanan çalışma zamanı, ilkenin maksimum tutarını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1fa97-115">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="1fa97-116">İlke için **başlangıç tarihi** ve **Bitiş tarihi** seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-116">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="1fa97-117">İzin satın alma veya satma istekleri yalnızca bu zaman dilimi boyunca gönderme için kullanılabilir olacak.</span><span class="sxs-lookup"><span data-stu-id="1fa97-117">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="1fa97-118">**İlke satın alma** altında , çalışanın pozisyonunda tanımlanan fmaya bağlı olarak maksimum tutarı aktarmak için **tam zaman eşdeğerliliği** (FTE) öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-118">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="1fa97-119">İlke türü **tutar** ise **Maksimum sabit bir tutar** girin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-119">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

8. <span data-ttu-id="1fa97-120">İzin satın almak üzere çalışanlar için izin tiplerini eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-120">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="1fa97-121">İlkeye birden fazla izin türü ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1fa97-121">You can add multiple leave types to the policy.</span></span> 

9. <span data-ttu-id="1fa97-122">Bir çalışanın satın alabileceği maksimum tutarı belirlemek için, farklı servis ayları etkinleştirmek üzere izin türüne ait **servis ayları** girin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-122">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

10. <span data-ttu-id="1fa97-123">İzin türü için **maksimum tutarı** girin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-123">Enter the **Maximum amount** for the leave type.</span></span> 

11. <span data-ttu-id="1fa97-124">Çalışanın izin verilecek **oranı** girin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-124">Enter the **Rate** at which the employee will buy the leave.</span></span> 

12. <span data-ttu-id="1fa97-125">İsteğe bağlı olarak alma için kullanılacak **kazanç kodunu** girin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-125">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

13. <span data-ttu-id="1fa97-126">İsteğe bağlı olarak, izin türü için maksimum tutarı belirlemek üzere FTE'nin kullanılması gerekip belirlenir.</span><span class="sxs-lookup"><span data-stu-id="1fa97-126">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="1fa97-127">Bir izin ve devamsızlık planına izin satınalma ve satış ilkesini ekleyin</span><span class="sxs-lookup"><span data-stu-id="1fa97-127">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="1fa97-128">**İzin ve devamsızlık** sayfasında, bir izin ve devamsızlık planı seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-128">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="1fa97-129">**Kurallar** altında **İzin satın alma ve satma ilkesi** seçin.</span><span class="sxs-lookup"><span data-stu-id="1fa97-129">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fa97-130">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1fa97-130">See also</span></span>

[<span data-ttu-id="1fa97-131">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="1fa97-131">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="1fa97-132">İzin ve devamsızlık türlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1fa97-132">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="1fa97-133">İzin ve devamsızlık planları tahakkuk ettirme</span><span class="sxs-lookup"><span data-stu-id="1fa97-133">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="1fa97-134">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="1fa97-134">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

