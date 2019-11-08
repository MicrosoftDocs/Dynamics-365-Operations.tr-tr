---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (11 Ocak 2019)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4bf106507800f53be80af1733667bfec3023b56f
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551853"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a><span data-ttu-id="ff801-103">Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (11 Ocak 2019)</span><span class="sxs-lookup"><span data-stu-id="ff801-103">What's new or changed in Dynamics 365 Talent - Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ff801-104">**Derleme 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="ff801-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="ff801-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ff801-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="ff801-106">Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="ff801-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="ff801-107">Bırakma taleplerini kullanılabilir bakiye tahminine göre doğrula</span><span class="sxs-lookup"><span data-stu-id="ff801-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="ff801-108">Bu sürümde yapılan değişiklikleri, çalışanların gelecekteki izin sürelerini mevcut bakiyelerinden çıkartmadan talep etmelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ff801-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="ff801-109">Standart iş akışları gelecekte yapılacak istekler için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="ff801-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="ff801-110">Daha fazla bilgi için [Çalışılan saatlere dayanarak zaman tahakkuk](leave-accrue-hours-worked.md) okuyun.</span><span class="sxs-lookup"><span data-stu-id="ff801-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="ff801-111">ESS ve Kişiler içinde tahmin edilen izin bakiyesini görüntüleyin</span><span class="sxs-lookup"><span data-stu-id="ff801-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="ff801-112">Bu özellik, gelecekteki izin bakiyelerinin İK, yöneticiler ve çalışanlar tarafından görüntülenmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="ff801-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="ff801-113">Çalışanlar, gelecekteki bakiyelere **Çalışan Self Servis** çalışma alanında görebilirler ve İK aynı bilgiye **Kişiler** çalışma alanından sahiptir.</span><span class="sxs-lookup"><span data-stu-id="ff801-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="ff801-114">İzin bakiyelerini değiştirmek için bildirimler</span><span class="sxs-lookup"><span data-stu-id="ff801-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="ff801-115">İzin bakiyeleri çalışanın geçerli bakiyesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="ff801-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="ff801-116">Gelecekteki bakiyeler, **Çalışan Self Servisi** ve **Kişiler** çalışma alanında, tahmin edilen bakiyeyi hesaplamak için bir "başlangıç tarihi" girilerek kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ff801-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="ff801-117">Aşağıdaki alanlarda tahmin edilen bakiyeleri görüntülemek için gezinti eklendi:</span><span class="sxs-lookup"><span data-stu-id="ff801-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="ff801-118">**Çalışan Self Servisi** çalışma alanında **İzin süresi** kartı.</span><span class="sxs-lookup"><span data-stu-id="ff801-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="ff801-119">**İzin ve devamsızlık** kartında, **Yönetici Self Servisi** çalışma alanında.</span><span class="sxs-lookup"><span data-stu-id="ff801-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="ff801-120">**Kişiler** çalışma alanında **İzin ve devamsızlık**.</span><span class="sxs-lookup"><span data-stu-id="ff801-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="ff801-121">Değişken ücret planları için ondalıklara izin ver (Nakit planları)</span><span class="sxs-lookup"><span data-stu-id="ff801-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="ff801-122">Değişken nakit ödülleri ve planları şimdi ondalık tutarlar ve geçersiz kılmalar için ek esnekliğe sahiptir.</span><span class="sxs-lookup"><span data-stu-id="ff801-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="ff801-123">Değişken ücret kayıtları üzerindeki tarihler, plan kaydedildikten sonra değiştirilemiyor</span><span class="sxs-lookup"><span data-stu-id="ff801-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="ff801-124">Bu değişiklik, plan kaydedildikten sonra planın bitiş tarihinin güncelleştirilmesine izin verir (genişletilmiş veya süresi dolmuş).</span><span class="sxs-lookup"><span data-stu-id="ff801-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="ff801-125">Planları başlangıç ve bitiş tarihlerinden bağımsız olarak hala etkinleştirebilir veya devre dışı bırakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff801-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="ff801-126">Bordro bilgisi Bordro yöneticisi güvenlik rolü atandığında kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="ff801-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="ff801-127">Bordro Yöneticisi rolü, talep işlemi sırasında bordro bilgisine erişim sahibi olmak üzere güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="ff801-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="ff801-128">Çalışan Self-Servis | Konum hiyerarşisini açılan kutusundan ana düğüm alamıyor</span><span class="sxs-lookup"><span data-stu-id="ff801-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="ff801-129">Pozisyon hiyerarşisini yeni bir çalışma alanına eklerken ve kuruluş yapısı içinde gezinirken ortaya çıkan bir hatayı gidermek için değişiklikler yapıldı.</span><span class="sxs-lookup"><span data-stu-id="ff801-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="ff801-130">Personel numara serisi kullanımda olduğunda yeni doğrulama iletisi</span><span class="sxs-lookup"><span data-stu-id="ff801-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="ff801-131">Bir çalışanı işe aldığınızda ve bir sonraki personel numarası kullanımda olduğunda sorunu açıklığa kavuşturmak için bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="ff801-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="ff801-132">Çalışan Self Servisi çalışma başlangıç sayfası olarak seçili</span><span class="sxs-lookup"><span data-stu-id="ff801-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="ff801-133">**Çalışan self servisi** çalışma alanı, bir kullanıcı için başlangıç sayfası olarak seçildi ve bu kullanıcı bir çalışan rolüne atanmış olmadığında, sistem varsayılan panoya yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="ff801-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="ff801-134">İşten çıkarma kodu, pozisyon atama kaydını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="ff801-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="ff801-135">Sonlandırma neden kodu şimdi pozisyon atamasını, bir çalışanı işten çıkarırken ve pozisyonu sonlandırırken güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ff801-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
