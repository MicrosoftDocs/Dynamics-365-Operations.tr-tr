---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (14 Mayız 2020)
description: Bu konuda, 14 Mayıs 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
manager: tfehr
ms.date: 05/14/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8d65236d316035722451a871afabedc6ab73f7a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127861"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a><span data-ttu-id="b0927-103">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (14 Mayız 2020)</span><span class="sxs-lookup"><span data-stu-id="b0927-103">What's new or changed in Dynamics 365 Human Resources (May 14, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b0927-104">Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b0927-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b0927-105">Değişiklikler derleme numarası 8.1.3244 uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b0927-105">Changes apply to build number 8.1.3244.</span></span> <span data-ttu-id="b0927-106">Bazı başlıklardaki parantez içindeki numaralar  Lifecycle Services (LCS) destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="b0927-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="b0927-107">Platform değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="b0927-107">Platform changes</span></span>

<span data-ttu-id="b0927-108">Platform değişiklikleri, bu haftaki sürüme dahil edildi.</span><span class="sxs-lookup"><span data-stu-id="b0927-108">Platform changes are included in this week's release.</span></span> <span data-ttu-id="b0927-109">Daha fazla bilgi için bkz. [Finance and Operations uygulamalarının 10.0.10 sürümü için platform güncelleştirmeleri (Mayıs 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span><span class="sxs-lookup"><span data-stu-id="b0927-109">For more information, see [Platform updates for version 10.0.10 of Finance and Operations apps (May 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span></span> <span data-ttu-id="b0927-110">Bu sürümde, hata düzeltmeleri ve kaydedilmiş görünümlerde değişiklikler bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b0927-110">This release includes bug fixes and changes to saved views.</span></span>
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a><span data-ttu-id="b0927-111">Dataverse seçim listelerinin İzin sabit listeleriyle tutarlı olduğundan emin olma (436343)</span><span class="sxs-lookup"><span data-stu-id="b0927-111">Ensure Dataverse picklists are consistent with Leave enums (436343)</span></span>

<span data-ttu-id="b0927-112">Dataverse seçim listeleri artık İzin sabit listeleriyle tutarlı.</span><span class="sxs-lookup"><span data-stu-id="b0927-112">Dataverse picklists are now consistent with Leave enums.</span></span>

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a><span data-ttu-id="b0927-113">İzin isteği iş akışını, istek miktarına göre kullanıcıların yapılandırmasına izin verme (300044)</span><span class="sxs-lookup"><span data-stu-id="b0927-113">Allow users to configure leave request workflow based on the request amount (300044)</span></span>

<span data-ttu-id="b0927-114">Kullanıcılar, izin istekleri iş akışlarını istek miktarına göre yapılandırabilir.</span><span class="sxs-lookup"><span data-stu-id="b0927-114">Users can configure leave requests workflows based on request amounts.</span></span>
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a><span data-ttu-id="b0927-115">Yeni çalışan formunun, gelişmiş güvenlik etkinleştirildiğinde Görünüm menüsü aracılığıyla verileri göstermesi (403185)</span><span class="sxs-lookup"><span data-stu-id="b0927-115">New worker form exposes data through the View menu when advanced security is enabled (403185)</span></span>

<span data-ttu-id="b0927-116">Bu sürüm, gelişmiş erişim etkinleştirildiğinde ve diğer şirketlerdeki çalışanlar erişilebilir olduğunda çalışanların görüntülenme sorunlarını tüzel varlıklar işlevleriyle düzeltir.</span><span class="sxs-lookup"><span data-stu-id="b0927-116">This release corrects how viewing workers across legal entities functions when advanced access is enabled and workers in other companies are accessible.</span></span>

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a><span data-ttu-id="b0927-117">Tek bir plan veya tek bir şirket için izin tahakkuklarının çalışmasına izin verme (318844)</span><span class="sxs-lookup"><span data-stu-id="b0927-117">Allow running leave accruals for a single plan or a single company (318844)</span></span>

<span data-ttu-id="b0927-118">Bu değişiklikle, bir şirket veya plan için tahakkukları çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0927-118">With this change, you can run accruals for a company or a plan.</span></span>
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a><span data-ttu-id="b0927-119">Pozisyonun tam zamanlı eşdeğerini (FTE) Kayıtlı işçi formunda gösterme (414658)</span><span class="sxs-lookup"><span data-stu-id="b0927-119">Show the position's full-time equivalent (FTE) in the Enrolled workers form (414658)</span></span>

<span data-ttu-id="b0927-120">FTE değeri, izin türünde FTE seçeneği etkinleştirilmişse işçinin tahakkuk oranını işçinin bulunduğu konumdan belirler.</span><span class="sxs-lookup"><span data-stu-id="b0927-120">The FTE value from a worker's position determines a worker's accrual rate when the FTE option is enabled on the leave type.</span></span> <span data-ttu-id="b0927-121">Bu alan artık **Kayıtlı işçiler** formuna ve **Toplu kayıt** iletişim kutusuna dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b0927-121">This field is now included in **Enrolled workers** form and the **Mass enrollment** dialog.</span></span>

## <a name="add-leave-balance-expiration-batch-job-431266"></a><span data-ttu-id="b0927-122">İzin bakiyesi geçerlilik bitiş tarihleri, toplu işi ekleme (431266)</span><span class="sxs-lookup"><span data-stu-id="b0927-122">Add leave balance expiration batch job (431266)</span></span>

<span data-ttu-id="b0927-123">Artık her gün çalışan yeni bir toplu iş kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b0927-123">A new batch job is now available that runs daily.</span></span> <span data-ttu-id="b0927-124">Geçerlilik bitiş tarihleri geldiğinde kalan izin bakiyesini azaltır.</span><span class="sxs-lookup"><span data-stu-id="b0927-124">It decreases the remaining leave balance when expiration dates become current.</span></span>

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a><span data-ttu-id="b0927-125">Çalışanın kişisel ilgili kişi varlığını kullanarak bir çalışan için kişisel ilgili kişileri dışa aktarma işlevinin Ana ilişki türündeki kişisel ilgili kişileri dışa aktarmaması (345893)</span><span class="sxs-lookup"><span data-stu-id="b0927-125">Exporting personal contacts for an employee using the Worker personal contact person entity doesn't export personal contacts with the Parent relationship type (345893)</span></span>

<span data-ttu-id="b0927-126">**Çalışanın kişisel ilgili kişi** veri varlığı (DMF'de **HcmPersonalContactPersonEntity** ve OData'da **PersonalContactPerson**), **Ana** ilişki türüne sahip kişisel ilgili kişileri dışarı aktaramaz.</span><span class="sxs-lookup"><span data-stu-id="b0927-126">The **Worker personal contact person** data entity (**HcmPersonalContactPersonEntity** in DMF and **PersonalContactPerson** in OData) couldn't export personal contacts that have a relationship type of **Parent**.</span></span> <span data-ttu-id="b0927-127">Bu sorun, bu değişiklikten sonra oluşturulan kişisel ilgili kişiler için düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="b0927-127">This issue is fixed for personal contacts that are created after this change.</span></span> <span data-ttu-id="b0927-128">**Ana** türündeki var olan kişisel ilgili kişiler, daha sonraki bir sürümde düzeltilecektir.</span><span class="sxs-lookup"><span data-stu-id="b0927-128">Existing personal contacts of type **Parent** will be fixed in a later release.</span></span>

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a><span data-ttu-id="b0927-129">Neden kodlarının, İzin ve devamsızlık olarak işaretlendiklerinde ve akıcı çalışan formu etkinleştirildiğinde farklı senaryolarda görüntülenmesi (434163)</span><span class="sxs-lookup"><span data-stu-id="b0927-129">Reason codes display across different scenarios when they're marked as Leave and absence and the streamlined employee form is enabled (434163)</span></span>

<span data-ttu-id="b0927-130">Bu değişiklik, akıcı çalışan girişini etkinleştirdiğinizde neden kodlarının yalnızca İzin ve devamsızlık kodlarıyla sınırlandırılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0927-130">This change restricts the reason codes to only Leave and absence codes when you enable streamlined employee entry.</span></span>

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a><span data-ttu-id="b0927-131">Gelecek dönem için çalışanlara izin planı atama önizleme özelliğinin hata göstermesi (433555)</span><span class="sxs-lookup"><span data-stu-id="b0927-131">The preview feature Assign a leave plan to employees in the future displays error (433555)</span></span>

<span data-ttu-id="b0927-132">Bu değişiklik, izin planına iki izin türünün atandığı ancak bir çalışan atamaya çalıştığınız durumlarda oluşan hatayı düzeltir.</span><span class="sxs-lookup"><span data-stu-id="b0927-132">This change corrects an error when a leave plan has two leave types assigned and you attempt to assign an employee.</span></span>

## <a name="getting-started-banner-appears-for-all-users-441731"></a><span data-ttu-id="b0927-133">Başlarken başlığının tüm kullanıcılar için görüntülenmesi (441731)</span><span class="sxs-lookup"><span data-stu-id="b0927-133">Getting started banner appears for all users (441731)</span></span>

<span data-ttu-id="b0927-134">Bu değişiklikle birlikte Başlarken başlığı, Sistem yöneticisi veya Veri yönetimi yöneticisi olmayan kullanıcılar için gizlenir.</span><span class="sxs-lookup"><span data-stu-id="b0927-134">With this change, the Getting started banner is hidden for users that aren't System administrators or Data management administrators.</span></span> 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a><span data-ttu-id="b0927-135">Dataverse Çalışan Adresi varlığının Human Resources'taki tarih saat bilgilerinin geçerli olduğu tarihler açısından farklı çalışması (425071)</span><span class="sxs-lookup"><span data-stu-id="b0927-135">The Dataverse Worker Address entity works differently in terms of date time effective dates in Human Resources (425071)</span></span>

<span data-ttu-id="b0927-136">Bu değişiklik, adres bilgilerini adres tarihlerine göre belirli senaryolarda hizalanmış halde tutar.</span><span class="sxs-lookup"><span data-stu-id="b0927-136">This change keeps address information aligned in certain scenarios, based on the dates of the address.</span></span>

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a><span data-ttu-id="b0927-137">Onaylı bir izin isteğine bir ek eklenememesi (425407)</span><span class="sxs-lookup"><span data-stu-id="b0927-137">Unable to add an attachment to an approved leave request (425407)</span></span>

<span data-ttu-id="b0927-138">Bu hafta yayımlanan sürümle, izin isteklerini değiştirmeden onaylı izin isteklerine ek ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0927-138">With this week's release, you can add attachments to approved leave requests without changing the leave request.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b0927-139">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="b0927-139">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="b0927-140">İzni askıya alma</span><span class="sxs-lookup"><span data-stu-id="b0927-140">Leave suspension</span></span>

<span data-ttu-id="b0927-141">Human Resources'ta bir çalışan için izin ve devamsızlığı askıya alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0927-141">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="b0927-142">İzni askıya alma, seçili izin türleri için izin tahakkuklarını durdurur.</span><span class="sxs-lookup"><span data-stu-id="b0927-142">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="b0927-143">Askıya alma bir tahakkuk işleminden sonra gerçekleştiyse, askıya alınan izin çalışanın izin bakiyesinde eşit dağıtılmış bir ayarlama oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b0927-143">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="b0927-144">Daha fazla bilgi için bkz. [İzni askıya alma](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="b0927-144">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="b0927-145">Tahakkukun askıya alınmış olduğunu belirtmek için kullanıcı deneyimini güncelleştirme (429550)</span><span class="sxs-lookup"><span data-stu-id="b0927-145">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="b0927-146">Kullanıcı deneyimi şimdi tahakkukun bir plan için askıya alınmış olduğunu gösteriyor.</span><span class="sxs-lookup"><span data-stu-id="b0927-146">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="b0927-147">Belirtilen izin türleri için izin tahakkunu askıya alma (272447)</span><span class="sxs-lookup"><span data-stu-id="b0927-147">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="b0927-148">Bu sürümde İK, ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="b0927-148">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="b0927-149">Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="b0927-149">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="b0927-150">Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0927-150">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="b0927-151">Tahakkuk askıya almaları için DMF varlığı kullanılabilir (429549)</span><span class="sxs-lookup"><span data-stu-id="b0927-151">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="b0927-152">DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b0927-152">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="b0927-153">Tahakkuk askıya almalara neden kodu ekleme (429547)</span><span class="sxs-lookup"><span data-stu-id="b0927-153">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="b0927-154">Neden kodları tahakkuk askıya almaya eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="b0927-154">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="b0927-155">İnsan Kaynakları parametrelerinden izin ve devamsızlık parametrelerine geçişi başlat</span><span class="sxs-lookup"><span data-stu-id="b0927-155">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="b0927-156">Bu sürüm İnsan Kaynakları parametrelerini İzin ve devamsızlık parametreleriyle birleştirmeye başlar.</span><span class="sxs-lookup"><span data-stu-id="b0927-156">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="b0927-157">Devretme kuralları</span><span class="sxs-lookup"><span data-stu-id="b0927-157">Carry forward rules</span></span>

<span data-ttu-id="b0927-158">Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0927-158">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="b0927-159">Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0927-159">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="b0927-160">Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="b0927-160">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b0927-161">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b0927-161">See also</span></span>

[<span data-ttu-id="b0927-162">Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="b0927-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="b0927-163">Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış</span><span class="sxs-lookup"><span data-stu-id="b0927-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="b0927-164">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="b0927-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="b0927-165">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="b0927-165">Manage features</span></span>](hr-admin-manage-features.md)