---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (Haziran 25 2020)
description: Bu konuda, 23 Haziran 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9787df5f36c1f08ade40e3e8fc5d5189e3bd5b0
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711952"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="1f518-103">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (Haziran 23 2020)</span><span class="sxs-lookup"><span data-stu-id="1f518-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

<span data-ttu-id="1f518-104">Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1f518-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1f518-105">Değişiklikler derleme numarası 8.1.3347 uygulanır.</span><span class="sxs-lookup"><span data-stu-id="1f518-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="1f518-106">Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="1f518-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="1f518-107">İşten çıkarılan bir çalışan için bir kayıt sona erdiğinde, kayıt türü, bakiye ve tutarın tümü kaydı bırak formunda temizlenir (444867)</span><span class="sxs-lookup"><span data-stu-id="1f518-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="1f518-108">Bu seçim yapıldığında, **izin türü**, **Bakiye** ve **tutar** değerlerinin artık temizlenmesi yerine bu değerler korunur.</span><span class="sxs-lookup"><span data-stu-id="1f518-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="1f518-109">Yeni Özellik (tek bir şirket veya tek bir plan için tahakkuku bırak) etkinleştirildiğinde tahmin edilen bakiye yanlış (456553)</span><span class="sxs-lookup"><span data-stu-id="1f518-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="1f518-110">Doğru tahmin edilen bakiye artık tek bir kurum veya tek bir plan için izin tahakkuku etkinleştirildiğinde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1f518-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="1f518-111">Yinelenen gezinme özelliklerine neden olan ilişkileri olan varlıklar (456486)</span><span class="sxs-lookup"><span data-stu-id="1f518-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="1f518-112">Bu sürüm, birden çok varlığın gezinme özellikleriyle ilgili bir sorunu düzeltir.</span><span class="sxs-lookup"><span data-stu-id="1f518-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="1f518-113">Tekrarlanan ilişkiler algılandı.</span><span class="sxs-lookup"><span data-stu-id="1f518-113">Duplicate relations are detected.</span></span> <span data-ttu-id="1f518-114">Bu senaryoların hepsi düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="1f518-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="1f518-115">Performans incelemesi ile ilgili şirketler arası açıklamalar (455536)</span><span class="sxs-lookup"><span data-stu-id="1f518-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="1f518-116">Şirketler arası Yorumlar, bu düzeltmeyle ilgili performans incelemelerde artık görünür.</span><span class="sxs-lookup"><span data-stu-id="1f518-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="1f518-117">Bu değişiklik, aynı performans incelemesi için farklı şirketlerde girilen gözden geçirici açıklamalarının görünümünü düzeltir.</span><span class="sxs-lookup"><span data-stu-id="1f518-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="1f518-118">Maaş yönetimi verilerini gösteren tutarsızlık (432562)</span><span class="sxs-lookup"><span data-stu-id="1f518-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="1f518-119">Dağıtım verilerinin tutarlı bir görünümü artık yönetici self servis 'de tutulur.</span><span class="sxs-lookup"><span data-stu-id="1f518-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="1f518-120">Çalışanın **maaş ayrıntılarına** nasıl gittiğinize bağlı olarak maaş verileri artık sürekli olarak yöneticilere göre görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="1f518-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="1f518-121">Sabit maaş planının geçerlilik tarihi varsayılan olarak bugünün tarihine (411994)</span><span class="sxs-lookup"><span data-stu-id="1f518-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="1f518-122">Maaş başlangıç tarihi şimdi çalışana atanan pozisyonun başlangıç tarihine göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="1f518-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="1f518-123">Bırak ve devamsızlık formu bu form açıldığında yarım gün tanımını etkinleştir devre dışı bırakıldı (452607)</span><span class="sxs-lookup"><span data-stu-id="1f518-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="1f518-124">Bu değişiklikle, Yeni bırakma hareketleri olana kadar **yarım gün açıklamasını etkinleştir** özelliği etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1f518-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="1f518-125">Excel üzerinden HcmDiscussionEntity yayımlanamıyor; TotalRatingScore alanı hatası (453899)</span><span class="sxs-lookup"><span data-stu-id="1f518-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="1f518-126">Şimdi, Excel çalışma kitabı tasarımcısında **HCMDiscussionEntity** kullanarak **TotalRatingScore** alanını güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f518-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="1f518-127">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="1f518-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="1f518-128">Veritabanı günlüklerine kaydetme</span><span class="sxs-lookup"><span data-stu-id="1f518-128">Database logging</span></span>

<span data-ttu-id="1f518-129">Veritabanı günlükleri hangi tablo ve alanların izleneceğini belirlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1f518-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="1f518-130">Ayrıca değişiklik izlemeyi tetiklemesi gereken olayları belirlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1f518-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="1f518-131">Zaman içinde yapılan bu değişiklikleri görmek için veritabanı günlüğü kaydetme yeteneklerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="1f518-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="1f518-132">Daha fazla bilgi için, bkz. [Veri tabanı günlüğü kaydetme işlemini yapılandırma ve yönetme](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="1f518-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="1f518-133">Zorunlu alanlar</span><span class="sxs-lookup"><span data-stu-id="1f518-133">Mandatory fields</span></span> 

<span data-ttu-id="1f518-134">Artık İnsan Kaynakları kişiselleştirme yetenekleri kullanarak alan zorunlu hale getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f518-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="1f518-135">Bu özellik için **Kaydedilmiş görünümler** gereklidir .</span><span class="sxs-lookup"><span data-stu-id="1f518-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="1f518-136">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="1f518-136">Human Resources application in Teams</span></span>

<span data-ttu-id="1f518-137">Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir .</span><span class="sxs-lookup"><span data-stu-id="1f518-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="1f518-138">İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler.</span><span class="sxs-lookup"><span data-stu-id="1f518-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="1f518-139">Daha fazla bilgi için bkz: [Teams'te insan kaynakları uygulama](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="1f518-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="1f518-140">Sosyal haklar yönetimi için veri yönetimi çerçevesi (DMF) varlıkları</span><span class="sxs-lookup"><span data-stu-id="1f518-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="1f518-141">Kazançlar yönetimi varlıkları serbest bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="1f518-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="1f518-142">DMF varlıkları, kazanç yönetimini kolayca yapılandırmak için verilerin içe ve dışa aktarılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1f518-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="1f518-143">Verileri taşımak için bir Kazanç yönetimi şablonu kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="1f518-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="1f518-144">Şablon veri bağımlılıklarını dikkate almak için verileri dışa aktarır ve sıralı şekilde içe aktarır.</span><span class="sxs-lookup"><span data-stu-id="1f518-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="1f518-145">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="1f518-145">Buy and sell leave</span></span> 

<span data-ttu-id="1f518-146">Bazı kuruluşlar, çalışanların izin satın alma veya satma olanağı sağlayan bir yarar sağlar.</span><span class="sxs-lookup"><span data-stu-id="1f518-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="1f518-147">Bu işlem genellikle el ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="1f518-147">This process is often managed manually.</span></span> <span data-ttu-id="1f518-148">Bu özellik, İK departmanı ile ilgili ilkelerin ve isteklerin yönetilmesini otomatikleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f518-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="1f518-149">İzin yönetimi işlemini kolaylaştırır ve hataları gidermek için yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1f518-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="1f518-150">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="1f518-150">For more information, see:</span></span>

- [<span data-ttu-id="1f518-151">İzin satın alma ve satma ilkelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="1f518-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="1f518-152">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="1f518-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="1f518-153">Tek bir şirket veya tek bir plan için izin tahakkuku</span><span class="sxs-lookup"><span data-stu-id="1f518-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="1f518-154">Müşteriler tek bir şirket veya tek bir izin ve devamsızlık planı için tahakkukları işleyebilir.</span><span class="sxs-lookup"><span data-stu-id="1f518-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="1f518-155">Bu özellik, farklı izin yılı veya izin tahakkuk ilkeleri olan müşteriler için tahakkuk işlemine açıklık sağlar.</span><span class="sxs-lookup"><span data-stu-id="1f518-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="1f518-156">Daha fazla bilgi için bkz. [Şirket veya izin planı başına izin tahakkuku](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="1f518-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="1f518-157">İzin isteklerine ekler ekleme</span><span class="sxs-lookup"><span data-stu-id="1f518-157">Add attachments to time off requests</span></span>

<span data-ttu-id="1f518-158">Onaylanmış izin isteklerine ek ekleme yeteneği, geçerli COVID-19 ortamında kritik öneme sahip.</span><span class="sxs-lookup"><span data-stu-id="1f518-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="1f518-159">Çalışanlar şimdi bu ekleri ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="1f518-159">Employees can now add these attachments.</span></span> <span data-ttu-id="1f518-160">Ayrıca, izin isteklerinde güncelleştirmelerin nasıl yapıldığıyla ilgili daha fazla öngörüye shaip olabilirler.</span><span class="sxs-lookup"><span data-stu-id="1f518-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="1f518-161">Daha fazla bilgi için, bkz. [Mevcut bir isteğe ek ekleme](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="1f518-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="1f518-162">Tahakkuk askıya almalara neden kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="1f518-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="1f518-163">Neden kodları tahakkuk askıya almaya eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="1f518-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="1f518-164">Devretme kuralları</span><span class="sxs-lookup"><span data-stu-id="1f518-164">Carry forward rules</span></span> 

<span data-ttu-id="1f518-165">Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f518-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="1f518-166">Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f518-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="1f518-167">Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="1f518-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="1f518-168">Belirtilen izin türleri için izin tahakkunu askıya alma</span><span class="sxs-lookup"><span data-stu-id="1f518-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="1f518-169">Ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f518-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="1f518-170">Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="1f518-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="1f518-171">Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f518-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="1f518-172">Tahakkuk askıya almaları için DMF varlığı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="1f518-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="1f518-173">DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1f518-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="1f518-174">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="1f518-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="1f518-175">Personel self servisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1f518-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="1f518-176">Personel self servis çalışma alanının adını Self servis olarak güncelleştirmek için **Human Resources parametrelerinde** yeni bir seçenek kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1f518-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="1f518-177">Common Data Service'te bulunan denetim listesi varlıkları</span><span class="sxs-lookup"><span data-stu-id="1f518-177">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="1f518-178">Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Common Data Service'te kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="1f518-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f518-179">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="1f518-179">See also</span></span>

[<span data-ttu-id="1f518-180">Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="1f518-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="1f518-181">Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış</span><span class="sxs-lookup"><span data-stu-id="1f518-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="1f518-182">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="1f518-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="1f518-183">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="1f518-183">Manage features</span></span>](hr-admin-manage-features.md)