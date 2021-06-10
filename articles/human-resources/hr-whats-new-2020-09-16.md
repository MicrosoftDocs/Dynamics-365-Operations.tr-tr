---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (16 Eylül 2020)
description: Bu konuda, 16 Eylül 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fe3ac2393e66a00e070d8cb6862c29625d39b53
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057176"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="5499d-103">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (16 Eylül 2020)</span><span class="sxs-lookup"><span data-stu-id="5499d-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5499d-104">Bu konuda, Dynamics 365 Human Resources'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5499d-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5499d-105">Değişiklikler derleme numarası 8.1.3557 uygulanır.</span><span class="sxs-lookup"><span data-stu-id="5499d-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="5499d-106">Bazı özelliklerin yanında bulunan parantez içindeki numaralar Lifecycle Services (LCS) destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="5499d-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="5499d-107">Bu sürümdeki içerik</span><span class="sxs-lookup"><span data-stu-id="5499d-107">Included in this release</span></span>

-  [<span data-ttu-id="5499d-108">Kayıtlı görünümler - genel kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="5499d-108">Saved views - general availability</span></span>](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="5499d-109">- Daha fazla bilgi için, bkz. [Kayıtlı görünümler](../fin-ops-core/fin-ops/get-started/saved-views.md).</span><span class="sxs-lookup"><span data-stu-id="5499d-109">- For more information, see [Saved views](../fin-ops-core/fin-ops/get-started/saved-views.md).</span></span> 

- <span data-ttu-id="5499d-110">**Pozisyon eylemleri** formunda güncelleştirilmiş bir boyut kılavuzu ve yeni iletişim kutusu (469495) vardır.</span><span class="sxs-lookup"><span data-stu-id="5499d-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="5499d-111">**Human Resources Paylaşılan parametreler**'e **Gelişmiş erişim**'de **Çalışan bilgilerine erişimi kısıtlamak** ayarını evet olarak ayarlarsanız, yan haklar formları artık yalnızca uygun çalışanları gösterir (393384).</span><span class="sxs-lookup"><span data-stu-id="5499d-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="5499d-112">**WorkCalendar** varlığında yeni takvim oluşturma seçenekleri (477055):</span><span class="sxs-lookup"><span data-stu-id="5499d-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="5499d-113">- Varsayılan bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="5499d-113">- Default ending time</span></span><br><span data-ttu-id="5499d-114">- Varsayılan başlangıç zamanı</span><span class="sxs-lookup"><span data-stu-id="5499d-114">-    Default starting time</span></span><br><span data-ttu-id="5499d-115">- Cuma çalışma günüdür</span><span class="sxs-lookup"><span data-stu-id="5499d-115">-  Is Friday working day</span></span><br><span data-ttu-id="5499d-116">- Pazartesi çalışma günüdür</span><span class="sxs-lookup"><span data-stu-id="5499d-116">-  Is Monday working day</span></span><br><span data-ttu-id="5499d-117">- Cumartesi çalışma günüdür</span><span class="sxs-lookup"><span data-stu-id="5499d-117">-  Is Saturday working day</span></span><br><span data-ttu-id="5499d-118">- Pazar çalışma günüdür</span><span class="sxs-lookup"><span data-stu-id="5499d-118">- Is Sunday working day</span></span><br><span data-ttu-id="5499d-119">- Perşembe çalışma günüdür</span><span class="sxs-lookup"><span data-stu-id="5499d-119">- Is Thursday working day</span></span><br><span data-ttu-id="5499d-120">- Salı çalışma günüdür</span><span class="sxs-lookup"><span data-stu-id="5499d-120">- Is Tuesday working day</span></span><br><span data-ttu-id="5499d-121">- Çarşamba çalışma günüdür</span><span class="sxs-lookup"><span data-stu-id="5499d-121">- Is Wednesday working day</span></span><br><span data-ttu-id="5499d-122">- İş Takvimi tatil kodu</span><span class="sxs-lookup"><span data-stu-id="5499d-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="5499d-123">**LeaveBankTransactionV1** varlığı şimdi neden kodunu içerir (477823).</span><span class="sxs-lookup"><span data-stu-id="5499d-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="5499d-124">Artık görev kayıtlarını kaydedebilirsiniz (492923).</span><span class="sxs-lookup"><span data-stu-id="5499d-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="5499d-125">Veriler artık **HCMWorkerContactEntity** öğesinden başarıyla yayımlandı (427620).</span><span class="sxs-lookup"><span data-stu-id="5499d-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="5499d-126">**Ücret** hızlı sekmesi artık yüklenici çalışan türü için **Çalışan eylemleri** formunda görüntülenir (482494).</span><span class="sxs-lookup"><span data-stu-id="5499d-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="5499d-127">Artık **Sabit ücret** ayarladıysanız, **Düzey** ve **Plan** alanları zorunludur.</span><span class="sxs-lookup"><span data-stu-id="5499d-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="5499d-128">Bu alanları boş bırakırsanız hata iletisi görüntülenir (482497).</span><span class="sxs-lookup"><span data-stu-id="5499d-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="5499d-129">**Kazanç** ögesinde **Plan türü** alanı artık bir açılır listedir (488768).</span><span class="sxs-lookup"><span data-stu-id="5499d-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="5499d-130">Human Resources'dan bir özel alan silinirse sistem yöneticileri artık bildirim almaya başlar (481408).</span><span class="sxs-lookup"><span data-stu-id="5499d-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="5499d-131">Çalışanın işine son verme işlemi sırasında, Human Resources beklendiği gibi davranır ve kilitleme olarak görüntülendikten sonra seçili şirketi değiştirmez (479877).</span><span class="sxs-lookup"><span data-stu-id="5499d-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="5499d-132">Yöneticiler artık kişiselleştirme yoluyla bir numara sütunu ekleyemez (485317).</span><span class="sxs-lookup"><span data-stu-id="5499d-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="5499d-133">Yöneticiler, artık süresi dolan kimlik numaralarından veri aralığı filtresini kaldıramazlar (485321).</span><span class="sxs-lookup"><span data-stu-id="5499d-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="5499d-134">**Bağlı olduğu kişi** alanı boş olduğunda pozisyon ayrıntıları pozisyon üzerine imleç getirildiğinde görüntülenmeye devam eder (433328).</span><span class="sxs-lookup"><span data-stu-id="5499d-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="5499d-135">Çalışanlar artık, Employee self service'de kazanç planı bilgilerini görüntüleyebilir (481676).</span><span class="sxs-lookup"><span data-stu-id="5499d-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="5499d-136">Çalışanlar artık tüm kayıtlı kursları görebilir (429048).</span><span class="sxs-lookup"><span data-stu-id="5499d-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="5499d-137">Artık **Profesyonel sertifikalar** sayfası için görüntüleme seçeneklerini kısıtlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5499d-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="5499d-138">Görüntüleme seçeneklerini geçerli yasal varlığa, çalışan durumuna göre ve çalışan türüne göre kısıtlayabilirsiniz (451501).</span><span class="sxs-lookup"><span data-stu-id="5499d-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="5499d-139">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="5499d-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="5499d-140">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="5499d-140">Human Resources app in Teams</span></span>

<span data-ttu-id="5499d-141">Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir .</span><span class="sxs-lookup"><span data-stu-id="5499d-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="5499d-142">İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler.</span><span class="sxs-lookup"><span data-stu-id="5499d-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="5499d-143">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="5499d-143">For more information, see:</span></span>

- <span data-ttu-id="5499d-144">Dynamics 365 2020 sürümü 1. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="5499d-144">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="5499d-145">Human Resources belgelerinde [Teams içinde Human Resources uygulaması](./hr-admin-teams-leave-app.md)</span><span class="sxs-lookup"><span data-stu-id="5499d-145">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="5499d-146">Teams'de Human Resources uygulaması önizleme özellikleri</span><span class="sxs-lookup"><span data-stu-id="5499d-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="5499d-147">**Bildirimler**: Teams'deki Human Resources uygulamasında izin isteklerini gönderen ve onaylayan kişiler bildirim alacak.</span><span class="sxs-lookup"><span data-stu-id="5499d-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="5499d-148">Onaylayanlar, izin isteklerini onaylayabilir veya reddedebilir.</span><span class="sxs-lookup"><span data-stu-id="5499d-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="5499d-149">Göndericiler, istek onaylandıysa veya reddedilmişse bilgilendirilir.</span><span class="sxs-lookup"><span data-stu-id="5499d-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="5499d-150">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="5499d-150">For more information, see:</span></span>
   - <span data-ttu-id="5499d-151">Dynamics 365 2020 sürümü 2. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="5499d-151">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="5499d-152">Human Resources belgelerinde [Teams içinde Human Resources uygulamasına ait bildirimleri etkinleştirme](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)</span><span class="sxs-lookup"><span data-stu-id="5499d-152">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="5499d-153">Human Resources belgelerinde [Tek tek kullanıcılar için Teams bildirimlerini açma veya kapatma](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)</span><span class="sxs-lookup"><span data-stu-id="5499d-153">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="5499d-154">Human Resources belgelerinde [Teams Bildirimleri](./hr-teams-leave-app.md#respond-to-teams-notifications)</span><span class="sxs-lookup"><span data-stu-id="5499d-154">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="5499d-155">Human Resources belgelerinde [Takımınızın takvimini görüntüleme](./hr-teams-leave-app.md#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="5499d-155">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="5499d-156">**Yönetici izin takvimi**: Yöneticiler, doğrudan onlara bağlı çalışanlar için onaylanan ve bekleyen izinleri takvim görünümünde görebilir.</span><span class="sxs-lookup"><span data-stu-id="5499d-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="5499d-157">Bu görünüm, takım üyelerinin izinde olduğu tarihlerin daha kolay anlaşılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="5499d-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="5499d-158">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="5499d-158">For more information, see:</span></span>
   - <span data-ttu-id="5499d-159">Dynamics 365 2020 sürümü 2. dalga planında [Microsoft Teams'de personel izin ve devamsızlık deneyimi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="5499d-159">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="5499d-160">Human Resources belgelerinde [Takımınızın takvimini görüntüleme](./hr-teams-leave-app.md#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="5499d-160">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="5499d-161">Bana atanan iş öğeleri listesini konumlandırmak için yapılandırma seçeneği (477004)</span><span class="sxs-lookup"><span data-stu-id="5499d-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="5499d-162">Panonun sağ sütunundaki **Bana atanan çalışma öğeleri** listesini konumlandırmak için yeni bir seçenek bulunur.</span><span class="sxs-lookup"><span data-stu-id="5499d-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="5499d-163">Bu değişiklikle, tüm çalışma öğeleri ve yapılacak işler listeleri aynı alanda görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="5499d-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="5499d-164">Özellik yönetiminde **Önizleme: İş akışı deneyimi geliştirmeleri** özelliğini etkinleştirerek bu işlevi etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="5499d-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="5499d-165">Önizleme özelliklerini açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="5499d-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="5499d-166">Bu özellik ayrıca, personel eylemleri formlarında görünen iş akışı seçeneklerini de yükseltir.</span><span class="sxs-lookup"><span data-stu-id="5499d-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="5499d-167">Ayrıca, hızlı erişim için eylem hızlı sekmesinin üstünde iş akışı seçenekleri de görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5499d-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="5499d-168">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="5499d-168">For more information, see:</span></span> 

- <span data-ttu-id="5499d-169">Dynamics 365 2020 sürüm dalga 2 planında [Kuruluş ve personel yönetimi iş akışı deneyimi iyileştirmeleri](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)</span><span class="sxs-lookup"><span data-stu-id="5499d-169">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Bana atanan iş öğeleri](./media/hr-workflow-work-items-assigned-to-me.png)

![İş akışı öğelerine hızlı erişim](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="5499d-172">İzin ve devamsızlık takvimi</span><span class="sxs-lookup"><span data-stu-id="5499d-172">Leave and absence calendar</span></span>

<span data-ttu-id="5499d-173">Bu sürüm, izin ve devamsızlık takvimleri için ek takvim seçenekleri içerir.</span><span class="sxs-lookup"><span data-stu-id="5499d-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="5499d-174">Daha fazla bilgi için bkz. [Ekip ve şirket takvimlerini görüntüleyin](./hr-employee-self-service-calendar.md).</span><span class="sxs-lookup"><span data-stu-id="5499d-174">For more information, see [View team and company calendars](./hr-employee-self-service-calendar.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="5499d-175">Çok Yakında</span><span class="sxs-lookup"><span data-stu-id="5499d-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="5499d-176">Dataverse'te bulunan denetim listesi varlıkları</span><span class="sxs-lookup"><span data-stu-id="5499d-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="5499d-177">Ekleme, çıkarma, transferler ve iş süreçleri için denetim listesi varlıkları yakında Dataverse'te kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5499d-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="5499d-178">Yan haklar yönetimi neden kodları</span><span class="sxs-lookup"><span data-stu-id="5499d-178">Benefits management reason codes</span></span>

<span data-ttu-id="5499d-179">Yan haklar yönetimi neden kodları Human Resources içinde var olan neden kodlarıyla yakında birleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="5499d-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="5499d-180">Yan haklar yönetiminde 15 karakterden uzun neden kodları oluşturduysanız, Yan haklar yönetimi **Neden kodları** formunda neden kodunun adını 15 karakter veya daha az olacak şekilde değiştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5499d-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="5499d-181">Adı güncelleştirdiğinizde, neden kodu, Personel yönetimi'nde var olan neden kodu formunun altında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="5499d-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="5499d-182">Bu değişiklik gelecekte kullanılabilir olacaktır ve var olan işlevleri etkilemeyecek.</span><span class="sxs-lookup"><span data-stu-id="5499d-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="5499d-183">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="5499d-183">See also</span></span>

[<span data-ttu-id="5499d-184">Human Resources'daki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="5499d-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="5499d-185">Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış</span><span class="sxs-lookup"><span data-stu-id="5499d-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="5499d-186">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="5499d-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="5499d-187">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="5499d-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
