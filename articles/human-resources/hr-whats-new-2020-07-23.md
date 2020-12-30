---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (23 Temmuz 2020)
description: Bu konuda, 23 Temmuz 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d0672e3039f54a4591db49eee00d69bf5e4278fd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528461"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="d2da7-103">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (23 Temmuz 2020)</span><span class="sxs-lookup"><span data-stu-id="d2da7-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d2da7-104">Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d2da7-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d2da7-105">Değişiklikler derleme numarası 8.1.3416 uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d2da7-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="d2da7-106">Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="d2da7-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="d2da7-107">Bir Pozisyonda Mali Boyutları silmek beklenen şekilde çalışmıyor (445476)</span><span class="sxs-lookup"><span data-stu-id="d2da7-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="d2da7-108">Bir pozisyondan boyutları kaldırmak, artık aynı pozisyonları Common Data Service'ten de kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2da7-108">Removing dimensions from a position now removes those same positions from Common Data Service.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="d2da7-109">Hiyerarşide bulunmayan pozisyonlar etkin olmayan pozisyonları gösteriyor (397257)</span><span class="sxs-lookup"><span data-stu-id="d2da7-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="d2da7-110">Etkin olmayan (süresi dolmuş) pozisyonlar, artık **Hiyerarşide bulunmayan pozisyonlar** olarak pozisyon hiyerarşisinde görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="d2da7-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="d2da7-111">Data Management Framework (DMF) üzerinde LeaveEnrollmentEntity ve HcmWorkerEntity arasında gerçekleştirilen doğrulama, yavaş veri yükleri oluşmasına neden oluyor (442324)</span><span class="sxs-lookup"><span data-stu-id="d2da7-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="d2da7-112">Bu sürümdeki değişiklikler **LeaveEnrollmentEntity** performansını artırır.</span><span class="sxs-lookup"><span data-stu-id="d2da7-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="d2da7-113">Kuruluş yönetimi kişiselleştirilemiyor (447490)</span><span class="sxs-lookup"><span data-stu-id="d2da7-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="d2da7-114">Bu değişiklikle, artık **Kuruluş yönetimi** içindeki bağlantıları kişiselleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2da7-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d2da7-115">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="d2da7-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="d2da7-116">Zorunlu alanlar</span><span class="sxs-lookup"><span data-stu-id="d2da7-116">Mandatory fields</span></span> 

<span data-ttu-id="d2da7-117">Artık İnsan Kaynakları kişiselleştirme yetenekleri kullanarak alan zorunlu hale getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2da7-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="d2da7-118">Bu özellik için **Kaydedilmiş görünümler** gereklidir .</span><span class="sxs-lookup"><span data-stu-id="d2da7-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="d2da7-119">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="d2da7-119">Human Resources application in Teams</span></span>

<span data-ttu-id="d2da7-120">Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir .</span><span class="sxs-lookup"><span data-stu-id="d2da7-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="d2da7-121">İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler.</span><span class="sxs-lookup"><span data-stu-id="d2da7-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="d2da7-122">Daha fazla bilgi için bkz: [Teams'te insan kaynakları uygulama](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="d2da7-122">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="d2da7-123">Sosyal haklar yönetimi için veri yönetimi çerçevesi (DMF) varlıkları</span><span class="sxs-lookup"><span data-stu-id="d2da7-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="d2da7-124">Kazançlar yönetimi varlıkları serbest bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="d2da7-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="d2da7-125">DMF varlıkları, kazanç yönetimini kolayca yapılandırmak için verilerin içe ve dışa aktarılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="d2da7-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="d2da7-126">Verileri taşımak için bir Kazanç yönetimi şablonu kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="d2da7-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="d2da7-127">Şablon veri bağımlılıklarını dikkate almak için verileri dışa aktarır ve sıralı şekilde içe aktarır.</span><span class="sxs-lookup"><span data-stu-id="d2da7-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="d2da7-128">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="d2da7-128">Buy and sell leave</span></span> 

<span data-ttu-id="d2da7-129">Bazı kuruluşlar, çalışanların izin satın alma veya satma olanağı sağlayan bir yarar sağlar.</span><span class="sxs-lookup"><span data-stu-id="d2da7-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="d2da7-130">Bu işlem genellikle el ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="d2da7-130">This process is often managed manually.</span></span> <span data-ttu-id="d2da7-131">Bu özellik, İK departmanı ile ilgili ilkelerin ve isteklerin yönetilmesini otomatikleştirir.</span><span class="sxs-lookup"><span data-stu-id="d2da7-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="d2da7-132">İzin yönetimi işlemini kolaylaştırır ve hataları gidermek için yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="d2da7-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="d2da7-133">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="d2da7-133">For more information, see:</span></span>

- [<span data-ttu-id="d2da7-134">İzin satın alma ve satma ilkelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="d2da7-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="d2da7-135">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="d2da7-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="d2da7-136">Tek bir şirket veya tek bir plan için izin tahakkuku</span><span class="sxs-lookup"><span data-stu-id="d2da7-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="d2da7-137">Müşteriler tek bir şirket veya tek bir izin ve devamsızlık planı için tahakkukları işleyebilir.</span><span class="sxs-lookup"><span data-stu-id="d2da7-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="d2da7-138">Bu özellik, farklı izin yılı veya izin tahakkuk ilkeleri olan müşteriler için tahakkuk işlemine açıklık sağlar.</span><span class="sxs-lookup"><span data-stu-id="d2da7-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="d2da7-139">Daha fazla bilgi için bkz. [Şirket veya izin planı başına izin tahakkuku](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="d2da7-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="d2da7-140">İzin isteklerine ekler ekleme</span><span class="sxs-lookup"><span data-stu-id="d2da7-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="d2da7-141">Onaylanmış izin isteklerine ek ekleme yeteneği, geçerli COVID-19 ortamında kritik öneme sahip.</span><span class="sxs-lookup"><span data-stu-id="d2da7-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="d2da7-142">Çalışanlar şimdi bu ekleri ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="d2da7-142">Employees can now add these attachments.</span></span> <span data-ttu-id="d2da7-143">Ayrıca, izin isteklerinde güncelleştirmelerin nasıl yapıldığıyla ilgili daha fazla öngörüye shaip olabilirler.</span><span class="sxs-lookup"><span data-stu-id="d2da7-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="d2da7-144">Daha fazla bilgi için, bkz. [Mevcut bir isteğe ek ekleme](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="d2da7-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="d2da7-145">Tahakkuk askıya almalara neden kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="d2da7-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="d2da7-146">Neden kodları tahakkuk askıya almaya eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="d2da7-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="d2da7-147">Devretme kuralları</span><span class="sxs-lookup"><span data-stu-id="d2da7-147">Carry forward rules</span></span> 

<span data-ttu-id="d2da7-148">Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2da7-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="d2da7-149">Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2da7-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="d2da7-150">Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="d2da7-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="d2da7-151">Belirtilen izin türleri için izin tahakkunu askıya alma</span><span class="sxs-lookup"><span data-stu-id="d2da7-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="d2da7-152">Ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2da7-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="d2da7-153">Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="d2da7-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="d2da7-154">Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d2da7-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="d2da7-155">Tahakkuk askıya almaları için DMF varlığı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="d2da7-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="d2da7-156">DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d2da7-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="d2da7-157">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="d2da7-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="d2da7-158">Common Data Service'te bulunan denetim listesi varlıkları</span><span class="sxs-lookup"><span data-stu-id="d2da7-158">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="d2da7-159">Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Common Data Service'te kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d2da7-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="d2da7-160">Platform değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="d2da7-160">Platform changes</span></span>

<span data-ttu-id="d2da7-161">Platform güncelleştirmesi 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="d2da7-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="d2da7-162">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="d2da7-162">See also</span></span>

[<span data-ttu-id="d2da7-163">Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="d2da7-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d2da7-164">Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış</span><span class="sxs-lookup"><span data-stu-id="d2da7-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="d2da7-165">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="d2da7-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="d2da7-166">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="d2da7-166">Manage features</span></span>](hr-admin-manage-features.md)
