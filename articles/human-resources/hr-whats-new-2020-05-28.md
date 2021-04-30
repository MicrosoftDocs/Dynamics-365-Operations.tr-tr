---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (28 Mayız 2020)
description: Bu konuda, 28 Mayıs 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 79026c6047f3a10366ef3b22d74caee13b371b66
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891973"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="94ed2-103">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (28 Mayız 2020)</span><span class="sxs-lookup"><span data-stu-id="94ed2-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="94ed2-104">Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="94ed2-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="94ed2-105">Değişiklikler derleme numarası 8.1.3287 uygulanır.</span><span class="sxs-lookup"><span data-stu-id="94ed2-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="94ed2-106">Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="94ed2-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="94ed2-107">İzin planı başına çoklu türleri etkinleştirdiğinizde LeaveRequest varlığı çalışmıyor (447498)</span><span class="sxs-lookup"><span data-stu-id="94ed2-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="94ed2-108">Bu değişiklikle, **LeaveEnrollmentV2Entity** artık çoklu izin türlerini etkinleştirdiğinizde ortaya çıkan hatayı düzeltebilir şekilde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="94ed2-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="94ed2-109">Toplu çekişme azaltma özelliği (Önizleme) (446619)</span><span class="sxs-lookup"><span data-stu-id="94ed2-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="94ed2-110">Bu özelliği etkinleştirdiğinizde, görevleri ve işleri bitirmede toplu iş çerçevesi tablolarında bloke etmek için bir azaltma bekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94ed2-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="94ed2-111">Çalışanı kaydederken UpdateConflict kişilerde bir kaydın düzenlenmesini engelliyor (427915)</span><span class="sxs-lookup"><span data-stu-id="94ed2-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="94ed2-112">Bu değişiklik, yeni bir çalışan eklerken, adres bilgilerini güncelleştirirken ve Dil tercihini değiştirirken oluşan bir hatayı düzeltir.</span><span class="sxs-lookup"><span data-stu-id="94ed2-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="94ed2-113">Bu benzersiz senaryoda, kaydın güncelleştirilmediği bir hata görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="94ed2-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="94ed2-114">Yeniden göndermek için onaylı bir izin isteğine bir ek eklenememesi (425407)</span><span class="sxs-lookup"><span data-stu-id="94ed2-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="94ed2-115">Bu değişiklik artık eklerin onaylanmış izin isteklerine izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="94ed2-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="94ed2-116">Kullanıcı, başka bir yasal varlık formundaki bir çalışan için maaş girebilir (409529)</span><span class="sxs-lookup"><span data-stu-id="94ed2-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="94ed2-117">Bu değişiklik, yanlış yasal varlık için maaş kayıtlarının yanlışlıkla girilmesini önlemek üzere maaş seçeneklerini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="94ed2-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="94ed2-118">Bir çalışan transfer ettiğinizde ve çalışan pozisyonu atama tarihi pozisyon süresinden önce olduğunda hata (429402)</span><span class="sxs-lookup"><span data-stu-id="94ed2-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="94ed2-119">Bu senaryodaki bir çalışanın aktarılması sırasında hata iletileri sorunu gidermek için gereken değişiklikleri daha iyi açıklayacak şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="94ed2-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="94ed2-120">Çalışan Self Servis kazançları kaydında ek özellikleri</span><span class="sxs-lookup"><span data-stu-id="94ed2-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="94ed2-121">Artık çalışanın kayıt olduğu her plan için sosyal haklar kaydı işlemi sırasında ek ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94ed2-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="94ed2-122">Böylece, **çalışanların kayıtlı kazancı** formundaki ekleri görebilirsiniz .</span><span class="sxs-lookup"><span data-stu-id="94ed2-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="94ed2-123">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="94ed2-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="94ed2-124">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="94ed2-124">Human Resources application in Teams</span></span>

<span data-ttu-id="94ed2-125">Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir .</span><span class="sxs-lookup"><span data-stu-id="94ed2-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="94ed2-126">İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler.</span><span class="sxs-lookup"><span data-stu-id="94ed2-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="94ed2-127">Daha fazla bilgi için bkz: [Teams'te insan kaynakları uygulama](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="94ed2-127">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="94ed2-128">İzni askıya alma</span><span class="sxs-lookup"><span data-stu-id="94ed2-128">Leave suspension</span></span>

<span data-ttu-id="94ed2-129">Human Resources'ta bir çalışan için izin ve devamsızlığı askıya alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94ed2-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="94ed2-130">İzni askıya alma, seçili izin türleri için izin tahakkuklarını durdurur.</span><span class="sxs-lookup"><span data-stu-id="94ed2-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="94ed2-131">Askıya alma bir tahakkuk işleminden sonra gerçekleştiyse, askıya alınan izin çalışanın izin bakiyesinde eşit dağıtılmış bir ayarlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="94ed2-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="94ed2-132">Daha fazla bilgi için bkz. [İzni askıya alma](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="94ed2-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="94ed2-133">Tahakkukun askıya alınmış olduğunu belirtmek için kullanıcı deneyimini güncelleştirme (429550)</span><span class="sxs-lookup"><span data-stu-id="94ed2-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="94ed2-134">Kullanıcı deneyimi şimdi tahakkukun bir plan için askıya alınmış olduğunu gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="94ed2-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="94ed2-135">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="94ed2-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="94ed2-136">Veritabanı günlükleri (Haziran 'da önizlemede)</span><span class="sxs-lookup"><span data-stu-id="94ed2-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="94ed2-137">Veritabanı günlükleri özelliği hangi tablo ve alanların izleneceğini belirlemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="94ed2-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="94ed2-138">Ayrıca değişiklik izlemeyi tetiklemesi gereken olayları belirlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="94ed2-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="94ed2-139">Bu değişiklikleri zaman içinde görmek için sorgulama özellikleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="94ed2-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="94ed2-140">İzin satın alma ve satma (önizlemede 1 Haziran 'ta)</span><span class="sxs-lookup"><span data-stu-id="94ed2-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="94ed2-141">Bazı kuruluşlar, çalışanların izin satın alma veya satma olanağı sağlayan bir yarar sağlar.</span><span class="sxs-lookup"><span data-stu-id="94ed2-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="94ed2-142">Bu işlem genellikle el ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="94ed2-142">This process is often managed manually.</span></span> <span data-ttu-id="94ed2-143">Bu özellik, HR departmanı için ilkeleri ve istekleri yönetmenin daha otomatikleştirilmiş bir yolunu sağlar ve yönetim sürecini korurken hataları ortadan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="94ed2-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="94ed2-144">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="94ed2-144">For more information, see:</span></span>

- [<span data-ttu-id="94ed2-145">İzin satın alma ve satma ilkelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="94ed2-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="94ed2-146">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="94ed2-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="94ed2-147">Sosyal haklar yönetimi için veri yönetimi çerçevesi (DMF) varlıkları</span><span class="sxs-lookup"><span data-stu-id="94ed2-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="94ed2-148">Kazançlar yönetimi varlıkları serbest bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="94ed2-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="94ed2-149">DMF varlıkları, sosyal haklar yönetimini kolayca konfigüre etmek için verilerin içe aktarılması ve verilmesi</span><span class="sxs-lookup"><span data-stu-id="94ed2-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="94ed2-150">Veri taşımak için bir sosyal haklar yönetimi şablonu da kullanılabilecek.</span><span class="sxs-lookup"><span data-stu-id="94ed2-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="94ed2-151">Şablon veri bağımlılıklarını dikkate almak için verileri dışa aktarır ve sıralı şekilde içe aktarır.</span><span class="sxs-lookup"><span data-stu-id="94ed2-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="94ed2-152">Tahakkuk askıya almalara neden kodu ekleme (1 Haziran)</span><span class="sxs-lookup"><span data-stu-id="94ed2-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="94ed2-153">Neden kodları tahakkuk askıya almaya eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="94ed2-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="94ed2-154">Devretme kuralları (1 Haziran)</span><span class="sxs-lookup"><span data-stu-id="94ed2-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="94ed2-155">Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94ed2-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="94ed2-156">Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94ed2-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="94ed2-157">Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="94ed2-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="94ed2-158">Belirtilen izin türleri için izin tahakkunu askıya alma (1 Haziran)</span><span class="sxs-lookup"><span data-stu-id="94ed2-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="94ed2-159">Bu sürümde İK, ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="94ed2-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="94ed2-160">Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="94ed2-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="94ed2-161">Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94ed2-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="94ed2-162">Tahakkuk askıya almaları için DMF varlığı kullanılabilir (1 Haziran)</span><span class="sxs-lookup"><span data-stu-id="94ed2-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="94ed2-163">DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="94ed2-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="94ed2-164">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="94ed2-164">See also</span></span>

[<span data-ttu-id="94ed2-165">Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="94ed2-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="94ed2-166">Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış</span><span class="sxs-lookup"><span data-stu-id="94ed2-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="94ed2-167">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="94ed2-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="94ed2-168">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="94ed2-168">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]