---
title: Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (20 Ağustos 2020)
description: Bu konuda, 20 Ağustos 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d964f9a532582b18471550a68032d00e19a065c4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467277"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a><span data-ttu-id="b8bcc-103">Dynamics 365 Human Resources'deki yenilikler veya değişiklikler (20 Ağustos 2020)</span><span class="sxs-lookup"><span data-stu-id="b8bcc-103">What's new or changed in Dynamics 365 Human Resources (August 20, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b8bcc-104">Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b8bcc-105">Değişiklikler derleme numarası 8.1.3478 uygulanır.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-105">Changes apply to build number 8.1.3478.</span></span> <span data-ttu-id="b8bcc-106">Bazı başlıklardaki parantez içindeki numaralar  Lifecycle Services (LCS) destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a><span data-ttu-id="b8bcc-107">Kişi çalışma alanındaki kartlarda yaklaşan ve bekleyen izin bilgilerini gösterme</span><span class="sxs-lookup"><span data-stu-id="b8bcc-107">Show upcoming and pending leave of absence information to cards in People workspace</span></span>

<span data-ttu-id="b8bcc-108">Artık **Kişi** çalışma alanındaki İzin ve devamsızlık kartlarında bekleyen ve yaklaşan izin isteği seçenekleri bulunur.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-108">Pending and upcoming leave request options are now available on the Leave and absence cards in the **People** workspace.</span></span>

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a><span data-ttu-id="b8bcc-109">Personel self servisi'deki Personel rolü için özel alan varsayılan olarak Evet değil (477106)</span><span class="sxs-lookup"><span data-stu-id="b8bcc-109">Private field isn't Yes by default for Employee role in Employee self service (477106)</span></span>

<span data-ttu-id="b8bcc-110">Artık **Özel** alan, personeller Personel self servisi'ndeki **Kişisel bilgiler** sayfası üzerinden yeni adres kayıtları eklediğinde varsayılan olarak **Evet** olur.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-110">The **Private** field now defaults to **Yes** when employees add new address records through the **Personal information** page in Employee self service.</span></span> 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a><span data-ttu-id="b8bcc-111">Personel yönetimindeki İşe alınacak adaylar hızlı sekmesinde hatalı aday sayısı gösteriliyor (470110)</span><span class="sxs-lookup"><span data-stu-id="b8bcc-111">Candidates to hire FastTab in Personnel management shows an incorrect count of candidates (470110)</span></span>

<span data-ttu-id="b8bcc-112">Artık, **Personel yönetimi** sayfası işe alınacak aday sayısını doğru şekilde görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-112">The **Personnel management** page now accurately displays the number of candidates to hire.</span></span> 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a><span data-ttu-id="b8bcc-113">Tahakkuk sıfır olarak ayarlandığında işten çıkarılan personel için hastalık izni girilemiyor (446195)</span><span class="sxs-lookup"><span data-stu-id="b8bcc-113">Can’t enter sickness for terminated employee when accrual is set to zero (446195)</span></span>

<span data-ttu-id="b8bcc-114">Gelecekte işten çıkarılacak ve tahakkuku sıfıra ayarlanmış personeller için artık izin işlemleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-114">Leave transactions are now allowed for employees that have been terminated in the future and the accrual is set to zero.</span></span> <span data-ttu-id="b8bcc-115">İzin işlemleri, personelin işten çıkarılma tarihine kadar girilebilir.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-115">Leave transactions can be entered up to the termination date of the employee.</span></span> 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a><span data-ttu-id="b8bcc-116">Yeni Çalışan formuna özel alanlar eklemek İzin yönetme eylem bölmesindeki alanları devre dışı bırakıyor (473314)</span><span class="sxs-lookup"><span data-stu-id="b8bcc-116">Adding custom fields to the new Worker form disables the fields in the action pane for Manage leave (473314)</span></span>

<span data-ttu-id="b8bcc-117">Yeni **Çalışan** formuna özel alanlar eklendiğinde **İzni yönet**'teki yeni **Çalışan** formunda yer alan eylem bölmesi seçenekleri devre dışı bırakılmayacak.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-117">Action pane options on the new **Worker** form in **Manage leave** will no longer be disabled if custom fields have been added to the new **Worker** form.</span></span>

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a><span data-ttu-id="b8bcc-118">Yorum yaz alanını zorunlu hale getirme özelliği, izin isteğinin yorum girilmeden gönderilmesine izin veriyor (473543)</span><span class="sxs-lookup"><span data-stu-id="b8bcc-118">Making the Leave comment field mandatory allows a leave request to be submitted when no comment is entered (473543)</span></span>

<span data-ttu-id="b8bcc-119">Yorum alanları artık zorunlu olabilir ve izin istekleri de bu ayara uyar.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-119">Comment fields can now be mandatory, and leave requests honor this setting.</span></span> <span data-ttu-id="b8bcc-120">Zorunlu alanlar önizleme özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-120">Mandatory fields is a preview feature.</span></span>

### <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="b8bcc-121">Tahakkuk askıya almaları için DMF varlığı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="b8bcc-121">DMF entity available for accrual suspensions</span></span>

<span data-ttu-id="b8bcc-122">DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-122">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b8bcc-123">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="b8bcc-123">In preview</span></span>

### <a name="mandatory-fields"></a><span data-ttu-id="b8bcc-124">Zorunlu alanlar</span><span class="sxs-lookup"><span data-stu-id="b8bcc-124">Mandatory fields</span></span>

<span data-ttu-id="b8bcc-125">İnsan Kaynakları kişiselleştirme yeteneklerini kullanarak alanları zorunlu hale getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-125">You can make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="b8bcc-126">Bu özellik için **Kaydedilmiş görünümler** gereklidir .</span><span class="sxs-lookup"><span data-stu-id="b8bcc-126">This feature requires **Saved views**.</span></span> <span data-ttu-id="b8bcc-127">Kayıtlı görünümler hakkında daha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-127">For more information about saved views, see:</span></span>

- <span data-ttu-id="b8bcc-128">Dynamics 365 2020 sürümü 2. dalga planında [Kayıtlı görünümler - genel kullanılabilirlik](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)</span><span class="sxs-lookup"><span data-stu-id="b8bcc-128">[Saved views - general availability](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="b8bcc-129">Kayıtlı görünümleri tamamen kullanan formlar oluşturma</span><span class="sxs-lookup"><span data-stu-id="b8bcc-129">Build forms that fully utilize saved views</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="b8bcc-130">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="b8bcc-130">Human Resources application in Teams</span></span>

<span data-ttu-id="b8bcc-131">Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir .</span><span class="sxs-lookup"><span data-stu-id="b8bcc-131">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="b8bcc-132">İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-132">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="b8bcc-133">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="b8bcc-133">For more information, see:</span></span>

- <span data-ttu-id="b8bcc-134">Dynamics 365 2020 sürümü 1. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="b8bcc-134">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="b8bcc-135">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="b8bcc-135">Human Resources app in Teams</span></span>](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a><span data-ttu-id="b8bcc-136">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="b8bcc-136">Coming soon</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="b8bcc-137">Teams'de Human Resources uygulaması önizleme özellikleri</span><span class="sxs-lookup"><span data-stu-id="b8bcc-137">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="b8bcc-138">**Bildirimler**: Teams'deki Human Resources uygulamasında izin isteklerini gönderen ve onaylayan kişiler bildirim alacak.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-138">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="b8bcc-139">Onaylayan kişiler, izin isteklerini onaylayabilecek veya reddedebilecek; gönderen kişiler ise istek onaylandığında veya reddedildiğinde bildirim alacak.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-139">Approvers will be able to approve or deny time-off requests, and submitters will be notified if the request was approved or denied.</span></span>
 
- <span data-ttu-id="b8bcc-140">**Yönetici izin takvimi**: Yöneticiler, doğrudan onlara bağlı çalışanlar için onaylanan ve bekleyen izinleri takvim görünümünde görebilecek.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-140">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="b8bcc-141">Bu görünüm, takım üyelerinin izinde olduğu tarihlerin daha kolay anlaşılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-141">This view provides an easy understanding of when their team members are away from work.</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="b8bcc-142">Dataverse'te bulunan denetim listesi varlıkları</span><span class="sxs-lookup"><span data-stu-id="b8bcc-142">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="b8bcc-143">Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Dataverse'te kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-143">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="known-issues"></a><span data-ttu-id="b8bcc-144">Bilinen sorunlar</span><span class="sxs-lookup"><span data-stu-id="b8bcc-144">Known issues</span></span>

<span data-ttu-id="b8bcc-145">**Özellik yönetimi** çalışma alanı, genel kullanıma sunulduklarında önizleme özellikleri olarak devre dışı bırakılan özellikleri görüntülüyor olabilir.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-145">The **Feature management** workspace may be displaying features that are disabled as preview features when they are generally available.</span></span> <span data-ttu-id="b8bcc-146">Aşağıda, yanlış durum gösteren genel kullanıma sunulmuş özelliklerin listesi verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-146">Below is a list of generally available features that show an incorrect status.</span></span> 

- <span data-ttu-id="b8bcc-147">Kazanç yönetimi</span><span class="sxs-lookup"><span data-stu-id="b8bcc-147">Benefits management</span></span>
- <span data-ttu-id="b8bcc-148">Servis talebi yönetimi</span><span class="sxs-lookup"><span data-stu-id="b8bcc-148">Case management</span></span>
- <span data-ttu-id="b8bcc-149">Veritabanı Günlük Kaydı (Denetleme)</span><span class="sxs-lookup"><span data-stu-id="b8bcc-149">Database logging (Auditing)</span></span>
- <span data-ttu-id="b8bcc-150">Tek bir şirket veya tek bir plan için izin tahakkuku</span><span class="sxs-lookup"><span data-stu-id="b8bcc-150">Leave accrual for a single company or a single plan</span></span>
- <span data-ttu-id="b8bcc-151">İzin ve devamsızlık tahakkuku askıya alma</span><span class="sxs-lookup"><span data-stu-id="b8bcc-151">Leave and absence accrual suspension</span></span>
- <span data-ttu-id="b8bcc-152">Bakiye ayarlama neden kodu ve açıklaması</span><span class="sxs-lookup"><span data-stu-id="b8bcc-152">Balance adjustment reason code and comment</span></span>
- <span data-ttu-id="b8bcc-153">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="b8bcc-153">Buy and sell leave</span></span>
- <span data-ttu-id="b8bcc-154">İzin ve devamsızlık takvimi</span><span class="sxs-lookup"><span data-stu-id="b8bcc-154">Leave and absence calendar</span></span>
- <span data-ttu-id="b8bcc-155">İzin ileri taşıma kuralları</span><span class="sxs-lookup"><span data-stu-id="b8bcc-155">Leave carry-forward rules</span></span>
- <span data-ttu-id="b8bcc-156">İzin tahakkuku denetleme</span><span class="sxs-lookup"><span data-stu-id="b8bcc-156">Leave accrual auditing</span></span>
- <span data-ttu-id="b8bcc-157">İzin tahakkuku silme işlemi</span><span class="sxs-lookup"><span data-stu-id="b8bcc-157">Leave accrual deletion</span></span>
- <span data-ttu-id="b8bcc-158">İzin tahakkuku yuvarlama</span><span class="sxs-lookup"><span data-stu-id="b8bcc-158">Leave accrual rounding</span></span>
- <span data-ttu-id="b8bcc-159">Tek bir izin planında birden fazla izin türü yapılandır</span><span class="sxs-lookup"><span data-stu-id="b8bcc-159">Configure multiple leave types on a single leave plan</span></span>
- <span data-ttu-id="b8bcc-160">İzin iyileştirmelerini güncelleştir</span><span class="sxs-lookup"><span data-stu-id="b8bcc-160">Update time-off enhancements</span></span>
- <span data-ttu-id="b8bcc-161">Tahakkuklar için personelin tam zamanlı eşdeğerini kullan</span><span class="sxs-lookup"><span data-stu-id="b8bcc-161">Use an employee's FTE for accruals</span></span>
- <span data-ttu-id="b8bcc-162">Şirketler arası ücret görünümü</span><span class="sxs-lookup"><span data-stu-id="b8bcc-162">Cross company compensation view</span></span>
- <span data-ttu-id="b8bcc-163">Performans incelemelerini yazdırma</span><span class="sxs-lookup"><span data-stu-id="b8bcc-163">Print performance reviews</span></span>
- <span data-ttu-id="b8bcc-164">İzin tahakkuku tatil düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="b8bcc-164">Leave accrual holiday corrections</span></span>

### <a name="benefit-plan-employee-entity"></a><span data-ttu-id="b8bcc-165">Kazanç planı personel varlığı</span><span class="sxs-lookup"><span data-stu-id="b8bcc-165">Benefit plan employee entity</span></span> 

<span data-ttu-id="b8bcc-166">Yakın zamanda, **BenefitsPlanEmployee** varlığıyla ilgili iki sorun tespit ettik.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-166">We have recently discovered two issues regarding the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="b8bcc-167">Çalışan kayıt anlaşmaları içeri aktarılırken **Kapsam kodu** ve **Plan türü kodu** hatalı ayarlanıyor.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-167">When importing worker enrollments, the **Coverage code** and the **Plan type code** are being set incorrectly.</span></span> <span data-ttu-id="b8bcc-168">Bu sorun, personel kazanç planlarının Personel self servisi'ndeki **Çalışan kazanç planları** formunda ve **Açık kayıt anlaşması** formunda yanlış gösterilmesine neden oluyor.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-168">This issue causes employee benefit plans to display incorrectly in the **Worker benefits plan** form and in the **Open enrollment** form in Employee self service.</span></span> <span data-ttu-id="b8bcc-169">Bu sorun, personelin Personel self servisi'nde plan seçme özelliğini de etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-169">This issue can also impact the employee's ability to select plans in Employee self service.</span></span> <span data-ttu-id="b8bcc-170">Şu anda geçici çözüm yok.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-170">Currently there isn't a workaround.</span></span> <span data-ttu-id="b8bcc-171">Bunu yüksek öncelikli bir düzeltme olarak ele alıyoruz ve bir sonraki sürümde düzeltmeyi sunacağız.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-171">We're treating this as a high-priority fix and will roll out the fix with our next release.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8bcc-172">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b8bcc-172">See also</span></span>

[<span data-ttu-id="b8bcc-173">Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="b8bcc-173">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="b8bcc-174">Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış</span><span class="sxs-lookup"><span data-stu-id="b8bcc-174">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="b8bcc-175">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="b8bcc-175">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="b8bcc-176">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="b8bcc-176">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]