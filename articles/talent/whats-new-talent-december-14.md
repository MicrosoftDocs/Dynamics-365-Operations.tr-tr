---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (14 Aralık 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
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
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/12/2019
ms.locfileid: "949863"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="04a0e-103">Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (14 Aralık 2018)</span><span class="sxs-lookup"><span data-stu-id="04a0e-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="04a0e-104">**Derleme 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="04a0e-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="04a0e-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="04a0e-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="04a0e-106">Değişiklikler</span><span class="sxs-lookup"><span data-stu-id="04a0e-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="04a0e-107">US - ACA (uygun eylemi yasası) vergi yılı 2018 1095-B ve C-1095 formlar için desteği</span><span class="sxs-lookup"><span data-stu-id="04a0e-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="04a0e-108">Her yıl, Applicable Large Employers (ALE'ler), her bir tam zamanlı çalışanlarına bir 1095-C sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="04a0e-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="04a0e-109">Ayrıca, İşveren kendini Sigortalı tedarik sağlıyorsa, (bir ALE farklıysa) 1095 C belirtmeniz gerekir ve bir 1095-(küçük bir İşveren farklıysa) B çalışanlara, tam zamanlı veya yarı zamanlı, sunulan durumu planları birinde.</span><span class="sxs-lookup"><span data-stu-id="04a0e-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="04a0e-110">Bu özellik hem 1095-C ve b-1095 için yazdırılabilir formlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="04a0e-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="04a0e-111">İçe aktarma sırasında HcmPerfJournalEntity üzerinde SubmittedByPersonId alanı yoksayılır</span><span class="sxs-lookup"><span data-stu-id="04a0e-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="04a0e-112">Performans günlük girişlerinde, alma/verme sırasında **Tarafından gönderilen** alanı dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="04a0e-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="04a0e-113">Bu değişiklik ile, değer **İçe/dışa aktarılan** alma sistemi içe aktarma dosyasında sağlanan değer güncelleştirilir, dışa aktarma sırasında tablo değeri gösterir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="04a0e-114">'İzin ve devamsızlık' çalışma alanı üzerindeki analiz sekmesi "OpenConnectionError" hatasını sistem Yöneticisi olmayan roller için gösterir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="04a0e-115">Bu güncelleştirme ile **Analitik** sekmesini **İzin ve Devamsızlık** çalışma alanında açarken hata verilmez.</span><span class="sxs-lookup"><span data-stu-id="04a0e-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="04a0e-116">Çalışan Self-Servis, Konum hiyerarşisini açılan kutusundan ana düğüm alamıyor</span><span class="sxs-lookup"><span data-stu-id="04a0e-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="04a0e-117">"Alma üst düğüm hatası"nı düzeltmek için ne zaman varolan bir çalışma alanında görüntülenecek konumu hiyerarşi kişiselleştirilmiş ve hiyerarşide bir konumda değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="04a0e-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="04a0e-118">Konum sayfasında Bordro sekmesini görmek için Sistem Yöneticisi olmak gerekir</span><span class="sxs-lookup"><span data-stu-id="04a0e-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="04a0e-119">Mevcut ayrıcalıkta doğru güvenlik öğelerini dahil etmek için bir değişiklik yapıldı: "Bordro çalışanı ve konum ayrıntısını koru".</span><span class="sxs-lookup"><span data-stu-id="04a0e-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="04a0e-120">Bu değişikliğe göre varsayılan olarak, Bordro Yöneticisi, Bordro konumu sayfa alanlarına erişebilir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="04a0e-121">Performans gözden geçirmesini yöneticiye gönderirken hata ve %Reviews.PerfPeriod% yer tutucusu, Gönderme talimatlarında kullanılır</span><span class="sxs-lookup"><span data-stu-id="04a0e-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="04a0e-122">%Reviews.PerfPeriod% yer tutucusunu Gönderme talimatlarında kullanırken oluşan "Null Reference" hatasını düzeltmek için bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="04a0e-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="04a0e-123">Workforce Power BI raporu, çalışan kıdem tarihi bir artık gün olduğunda hata gösteriyor</span><span class="sxs-lookup"><span data-stu-id="04a0e-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="04a0e-124">Bu değişikliğe göre artık gün için Power BI artık desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="04a0e-125">Core HR ve Attract arasında tümleştirme</span><span class="sxs-lookup"><span data-stu-id="04a0e-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="04a0e-126">İlgili adayların işe alınması için Core HR ve Attract arasındaki tümleştirmeyi güncelleştirmek için bir değişiklik yapıldı.</span><span class="sxs-lookup"><span data-stu-id="04a0e-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="04a0e-127">İşe alınacak adayların **Personel Yönetimi** çalışma alanında görüntülenebilir olması için aşağıdaki Common Data Service varlıklarının kullanılır.</span><span class="sxs-lookup"><span data-stu-id="04a0e-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="04a0e-128">İş Başvurusu</span><span class="sxs-lookup"><span data-stu-id="04a0e-128">Job Application</span></span>
- <span data-ttu-id="04a0e-129">Durum Sebebinin, Teklif Kabul Edildi olarak ayarlanması gerekir</span><span class="sxs-lookup"><span data-stu-id="04a0e-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="04a0e-130">Aday ve Açık Pozisyon sağlar</span><span class="sxs-lookup"><span data-stu-id="04a0e-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="04a0e-131">Aday</span><span class="sxs-lookup"><span data-stu-id="04a0e-131">Candidate</span></span>
-   <span data-ttu-id="04a0e-132">Aday bilgileri sağlar</span><span class="sxs-lookup"><span data-stu-id="04a0e-132">Provides Candidate information</span></span>

<span data-ttu-id="04a0e-133">Açık Pozisyon</span><span class="sxs-lookup"><span data-stu-id="04a0e-133">Job Opening</span></span>
-   <span data-ttu-id="04a0e-134">Açık Pozisyon Kimliği ve Açık Pozisyon Katılımcıları sağlar</span><span class="sxs-lookup"><span data-stu-id="04a0e-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="04a0e-135">Açık Pozisyon Katılımcıları</span><span class="sxs-lookup"><span data-stu-id="04a0e-135">Job Opening Participants</span></span>
-   <span data-ttu-id="04a0e-136">İşe Alım Müdürü sağlar</span><span class="sxs-lookup"><span data-stu-id="04a0e-136">Provides Hiring Manager</span></span>

<span data-ttu-id="04a0e-137">Bir aday Personel Yönetimine eklendiğinde, aday artık aday kartında bulunan yeni seçenek kullanılarak da çıkartılabilir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="04a0e-138">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="04a0e-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="04a0e-139">İzin ve devamsızlık: Gelecekteki izin ve devamsızlık tahmini bakiyeleri</span><span class="sxs-lookup"><span data-stu-id="04a0e-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="04a0e-140">Personellerin günce izin bakiyelerini etkilemeden izin ve gelecekteki izin taleplerini tahmin etmesine olanak sağlayan değişiklikler ile görüntülenen izin bakiyeleri de değişir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="04a0e-141">Şu anda görüntülenen kullanılabilir bakiye tahakkukları Bugün ve onaylanan tüm ile birlikte istekleri isteklerini bırakma süresi sonuna kadar kullanılabilir kapalı süreyi aranır.</span><span class="sxs-lookup"><span data-stu-id="04a0e-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="04a0e-142">Tahmin olanağı serbest bırakıldığı zaman, bakiye, bugünkü tahakkuklar da dahil geçerli izin bakiyesine ve bugün üzerinden taleplere değişir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="04a0e-143">Personeller ve yöneticiler bu güncelleştirilen bakiyeleri personel ve yönetici self servisinde, **İzin** kartında ve **İzin bakiyeleri** penceresinde görebilirler.</span><span class="sxs-lookup"><span data-stu-id="04a0e-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="04a0e-144">İK yöneticileri, bu güncelleştirilmiş bakiyeleri **Kişiler** çalışma alanında ve personelin **Atanmış izin planları** penceresinde görebilirler.</span><span class="sxs-lookup"><span data-stu-id="04a0e-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="04a0e-145">Bilinen sorun</span><span class="sxs-lookup"><span data-stu-id="04a0e-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="04a0e-146">Finance and Operations ile tümleştirmede eşleşme hataları</span><span class="sxs-lookup"><span data-stu-id="04a0e-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="04a0e-147">Talent'ın Dynamics 365 for Finance and Operations ile tümleştirilmesinde geçerli şablonda aşağıdaki sorunlar belirlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="04a0e-148">Yeni bir şablon hemen yayımlanır ve oluşturulan tüm yeni tümleştirme projelerine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="04a0e-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="04a0e-149">Varolan tümleştirme projeleri için görev eşleştirmeleri güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="04a0e-150">Güncelleştirilmiş eşleşmeler için aşağıdaki tabloya bakın.</span><span class="sxs-lookup"><span data-stu-id="04a0e-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="04a0e-151">İş Pozisyonları ve Pozisyonlar Ana İş Atama görevi, veri tümleştirmez.</span><span class="sxs-lookup"><span data-stu-id="04a0e-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="04a0e-152">Bunun şu anda araştırması yapılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="04a0e-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="04a0e-153">Geçerli eşleme içinde geçici çözüm yoktur.</span><span class="sxs-lookup"><span data-stu-id="04a0e-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="04a0e-154">İşletim birimine Departmanlar görevinin aşağıdaki eşleşmeleri güncelleştirmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="04a0e-155">Varolan kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="04a0e-155">Existing source field</span></span>          | <span data-ttu-id="04a0e-156">Yeni kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="04a0e-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="04a0e-157">cdm_description (Tanım)</span><span class="sxs-lookup"><span data-stu-id="04a0e-157">cdm_description (Description)</span></span>  | <span data-ttu-id="04a0e-158">cdm_name (Adı)</span><span class="sxs-lookup"><span data-stu-id="04a0e-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="04a0e-159">Ek bir eşleşmenin de eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="04a0e-160">Aşağıdaki eşleşmeye eklemek için son **Hiçbiri** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="04a0e-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="04a0e-161">Kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="04a0e-161">Source field</span></span>                   | <span data-ttu-id="04a0e-162">Hedef alan</span><span class="sxs-lookup"><span data-stu-id="04a0e-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="04a0e-163">cdm_description (Tanım)</span><span class="sxs-lookup"><span data-stu-id="04a0e-163">cdm_description (Description)</span></span>  | <span data-ttu-id="04a0e-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="04a0e-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="04a0e-165">Güncelleştirilmiş eşlemeler aşağıdaki resimdeki gibi görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-165">The updated mappings should look like the following image.</span></span>

![İşletim birimlerine Departmanlar görevi](./media/DepartmentMapping.png)


<span data-ttu-id="04a0e-167">İş Ayrıntısına İşler görevinin aşağıdaki eşleşmeleri güncelleştirmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="04a0e-168">Varolan kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="04a0e-168">Existing source field</span></span>          | <span data-ttu-id="04a0e-169">Yeni kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="04a0e-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="04a0e-170">cdm_name (Adı)</span><span class="sxs-lookup"><span data-stu-id="04a0e-170">cdm_name (Name)</span></span>                | <span data-ttu-id="04a0e-171">cdm_description (Tanım)</span><span class="sxs-lookup"><span data-stu-id="04a0e-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="04a0e-172">cdm_name (Tanım)</span><span class="sxs-lookup"><span data-stu-id="04a0e-172">cdm_name (Description)</span></span>         | <span data-ttu-id="04a0e-173">cdm_jobdescription(İş Tanımı)</span><span class="sxs-lookup"><span data-stu-id="04a0e-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="04a0e-174">Güncelleştirilmiş eşlemeler aşağıdaki resimdeki gibi görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-174">The updated mappings should look like the image below.</span></span>

![İş Ayrıntılarına İşler görevi](./media/JobMapping.png)

<span data-ttu-id="04a0e-176">İşe Çalışanlar görevinin aşağıdaki eşleşmeleri güncelleştirmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="04a0e-177">Varolan kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="04a0e-177">Existing source field</span></span>                 | <span data-ttu-id="04a0e-178">Yeni kaynak alanı</span><span class="sxs-lookup"><span data-stu-id="04a0e-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="04a0e-179">cdm_emailaddress1 (E-posta Adresi 1)</span><span class="sxs-lookup"><span data-stu-id="04a0e-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="04a0e-180">cdm_primaryemailaddress (Birincil E-posta Adresi)</span><span class="sxs-lookup"><span data-stu-id="04a0e-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="04a0e-181">cdm_telephone1 (Telefon 1)</span><span class="sxs-lookup"><span data-stu-id="04a0e-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="04a0e-182">cdm_primarytelephone (Birincil telefon)</span><span class="sxs-lookup"><span data-stu-id="04a0e-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="04a0e-183">Cinsiyet alanı dönüştürmenin de güncelleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="04a0e-184">**fn** (fonksiyon) eşleşme türünü Cinsiyet için seçin ve aşağıdaki değer eşleştirmelerini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="04a0e-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="04a0e-185">Common Data Service değeri</span><span class="sxs-lookup"><span data-stu-id="04a0e-185">Common Data Service value</span></span>                   | <span data-ttu-id="04a0e-186">Finance and Operations değeri</span><span class="sxs-lookup"><span data-stu-id="04a0e-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="04a0e-187">75440000</span><span class="sxs-lookup"><span data-stu-id="04a0e-187">75440000</span></span>                    | <span data-ttu-id="04a0e-188">Erkek</span><span class="sxs-lookup"><span data-stu-id="04a0e-188">Male</span></span>                                             |
| <span data-ttu-id="04a0e-189">75440001</span><span class="sxs-lookup"><span data-stu-id="04a0e-189">75440001</span></span>                    | <span data-ttu-id="04a0e-190">Kadın</span><span class="sxs-lookup"><span data-stu-id="04a0e-190">Female</span></span>                                           |
| <span data-ttu-id="04a0e-191">75440002</span><span class="sxs-lookup"><span data-stu-id="04a0e-191">75440002</span></span>                    | <span data-ttu-id="04a0e-192">Hiçbiri</span><span class="sxs-lookup"><span data-stu-id="04a0e-192">None</span></span>                                             | 
| <span data-ttu-id="04a0e-193">75440003</span><span class="sxs-lookup"><span data-stu-id="04a0e-193">75440003</span></span>                    | <span data-ttu-id="04a0e-194">NonSpecific</span><span class="sxs-lookup"><span data-stu-id="04a0e-194">NonSpecific</span></span>                                      |

<span data-ttu-id="04a0e-195">Güncelleştirilmiş eşlemeler aşağıdaki resimlerdeki gibi görünmelidir.</span><span class="sxs-lookup"><span data-stu-id="04a0e-195">The updated mappings should look like the following images.</span></span>

![Çalışana Çalışanlar görevi](./media/WorkerMapping.png)

![Cinsiyet alanı dönüştürme](./media/WorkerTransform.png)
