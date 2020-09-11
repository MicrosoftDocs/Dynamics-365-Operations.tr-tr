---
title: İzin satın alma ve satma ilkelerini yönetme
description: Dynamics 365 Human Resources'ta çalışanların izin satın alma ve satma olanağı sağlayabilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
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
ms.openlocfilehash: 55d29c42cc1b2d69517e2fcd458ee6a1bdf5277f
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712137"
---
# <a name="manage-buy-and-sell-leave-policies"></a><span data-ttu-id="1f8ef-103">İzin satın alma ve satma ilkelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="1f8ef-103">Manage buy and sell leave policies</span></span>

<span data-ttu-id="1f8ef-104">İzin satın alma ve satma ilkesi oluşturarak personelin izin satın almasını ve satmasını etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-104">You can enable employees to buy and sell leave by creating a buy and sell leave policy.</span></span> <span data-ttu-id="1f8ef-105">Onaylar için iş akışını kullanmak, maksimum tutar ve ücret belirlemek ve satın alma ile satma için ücret ayarlamak için bu ilkeleri yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-105">You can configure these policies to use workflow for approvals, set maximum amounts and rates, and set rates for buying and selling.</span></span> 

## <a name="enable-employees-to-buy-and-sell-leave"></a><span data-ttu-id="1f8ef-106">Çalışanların izin satın alma ve satma olanağını etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="1f8ef-106">Enable employees to buy and sell leave</span></span>

1. <span data-ttu-id="1f8ef-107">**İzin ve devamsızlık parametreleri** sayfasında, **Personelin izin satın almasına izin ver** ve **Personelin izin satmasına izin ver** için **Evet**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-107">On the **Leave and absence parameters** page, select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span>

## <a name="create-a-buy-and-sell-leave-policy"></a><span data-ttu-id="1f8ef-108">İzin satın alma ve satma ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1f8ef-108">Create a buy and sell leave policy</span></span>

1. <span data-ttu-id="1f8ef-109">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-109">On the **Leave and absence** page, select the **Links** tab.</span></span> 

2. <span data-ttu-id="1f8ef-110">**İzin satın alma ve satma ilkesi** seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-110">Select **Buy and sell leave policy**.</span></span>

3. <span data-ttu-id="1f8ef-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-111">Select **New**.</span></span>

4. <span data-ttu-id="1f8ef-112">İlke için**İzin Satınalma ve satma ilkesi** altındaki bir **ad** ve **açıklama** girin .</span><span class="sxs-lookup"><span data-stu-id="1f8ef-112">Enter a **Name** and **Description** for the policy under **Buy and sell leave policy**.</span></span> 

5. <span data-ttu-id="1f8ef-113">Bir **İlke türü** seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-113">Select a **Policy type**.</span></span> 

   <span data-ttu-id="1f8ef-114">Kullanılabilir ilke türleri haftalık **tutar** ve **saat sayısı**.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-114">The available policy types are **Amount** and **Hours per week**.</span></span> <span data-ttu-id="1f8ef-115">Çalışanların satın alabileceği ve satılabilecek maksimum tutarlar için **sabit bir tutar** girmek üzere **tutar** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-115">Select **Amount** to enter a **Fixed amount** for the maximum amounts employees can buy and sell.</span></span> <span data-ttu-id="1f8ef-116">**Haftalık saatleri** seçerseniz , çalışanın atadığı çalışma tarihi takviminde tanımlanan çalışma zamanı, ilkenin maksimum tutarını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-116">If you select **Hours per week**, the working time defined in the employee's assigned working time calendar is used to determine the maximum amount of the policy.</span></span> 

6. <span data-ttu-id="1f8ef-117">İlke için **başlangıç tarihi** ve **Bitiş tarihi** seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-117">Select a **Start date** and **End date** for the policy.</span></span> <span data-ttu-id="1f8ef-118">İzin satın alma veya satma istekleri yalnızca bu zaman dilimi boyunca gönderme için kullanılabilir olacak.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-118">Requests to buy or sell leave will only be available for submission during this time frame.</span></span> 

7. <span data-ttu-id="1f8ef-119">İlke için **İş Akışı Kimliği** seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-119">Select a **Workflow ID** for the policy.</span></span> <span data-ttu-id="1f8ef-120">Tüm satın alma ve satma istekleri, inceleme ve onay için bu iş akışını kullanır.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-120">Any buy and sell requests will use this workflow for review and approval.</span></span> 

8. <span data-ttu-id="1f8ef-121">**İlke satın alma** altında , çalışanın pozisyonunda tanımlanan fmaya bağlı olarak maksimum tutarı aktarmak için **tam zaman eşdeğerliliği** (FTE) öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-121">Under **Buy policy**, select **Full time equivalency** (FTE) to prorate the maximum amount based on the FTE defined on the employee's position.</span></span> <span data-ttu-id="1f8ef-122">İlke türü **tutar** ise **Maksimum sabit bir tutar** girin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-122">If the policy type is **Amount**, enter a **Maximum fixed amount**.</span></span> 

9. <span data-ttu-id="1f8ef-123">İzin satın almak üzere çalışanlar için izin tiplerini eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-123">Select **Add** to add the leave types for employees to buy leave.</span></span> <span data-ttu-id="1f8ef-124">İlkeye birden fazla izin türü ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-124">You can add multiple leave types to the policy.</span></span> 

10. <span data-ttu-id="1f8ef-125">Bir çalışanın satın alabileceği maksimum tutarı belirlemek için, farklı servis ayları etkinleştirmek üzere izin türüne ait **servis ayları** girin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-125">Enter the **Months of service** for the leave type to enable different months of service to determine the maximum amount an employee can buy.</span></span> 

11. <span data-ttu-id="1f8ef-126">İzin türü için **maksimum tutarı** girin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-126">Enter the **Maximum amount** for the leave type.</span></span> 

12. <span data-ttu-id="1f8ef-127">Çalışanın izin verilecek **oranı** girin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-127">Enter the **Rate** at which the employee will buy the leave.</span></span> 

13. <span data-ttu-id="1f8ef-128">İsteğe bağlı olarak alma için kullanılacak **kazanç kodunu** girin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-128">Optionally enter the **Earning code** to be used for buying leave.</span></span> 

14. <span data-ttu-id="1f8ef-129">İsteğe bağlı olarak, izin türü için maksimum tutarı belirlemek üzere FTE'nin kullanılması gerekip belirlenir.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-129">Optionally set whether to use FTE to determine the maximum amount for the leave type.</span></span> 

15. <span data-ttu-id="1f8ef-130">Bir satış ilkesi oluşturmak için **Satış ilkesi** bölümündeki 8 ile 14. adımlar arasındaki işlemleri uygulayın.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-130">To create a sell policy, follow steps 8 through 14 under **Sell policy**.</span></span> 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a><span data-ttu-id="1f8ef-131">Bir izin ve devamsızlık planına izin satınalma ve satış ilkesini ekleyin</span><span class="sxs-lookup"><span data-stu-id="1f8ef-131">Add the buy and sell leave policy to a leave and absence plan</span></span>

1. <span data-ttu-id="1f8ef-132">**İzin ve devamsızlık** sayfasında, bir izin ve devamsızlık planı seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-132">On the **Leave and absence** page, select a leave and absence plan.</span></span>

2. <span data-ttu-id="1f8ef-133">**Kurallar** altında **İzin satın alma ve satma ilkesi** seçin.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-133">Under **Rules**, select **Buy and sell leave policy**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f8ef-134">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1f8ef-134">See also</span></span>

[<span data-ttu-id="1f8ef-135">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="1f8ef-135">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="1f8ef-136">İzin ve devamsızlık türlerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1f8ef-136">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)</br>
[<span data-ttu-id="1f8ef-137">İzin ve devamsızlık planları tahakkuk ettirme</span><span class="sxs-lookup"><span data-stu-id="1f8ef-137">Accrue leave and absence plans</span></span>](hr-leave-and-absence-accrue.md)</br>
[<span data-ttu-id="1f8ef-138">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="1f8ef-138">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

