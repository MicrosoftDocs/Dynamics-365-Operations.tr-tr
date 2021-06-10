---
title: Dataverse tabloları
description: Microsoft Dynamics 365 Human Resources, Dataverse genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 325bd8a9de07e3978ff6c513975a0e8db22854e0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054368"
---
# <a name="dataverse-tables"></a><span data-ttu-id="37669-103">Dataverse tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="37669-104">Microsoft Dynamics 365 Human Resources, Dataverse genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="37669-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="37669-105">Human Resources varlıkları Dataverse tablolarına karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="37669-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="37669-106">Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="37669-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="37669-107">Aşağıdaki Dataverse tabloları Human Resources varlıklarına göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="37669-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="37669-108">Fayda tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-108">Benefit tables</span></span>

| <span data-ttu-id="37669-109">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="37669-109">Name</span></span> | <span data-ttu-id="37669-110">Tablo</span><span class="sxs-lookup"><span data-stu-id="37669-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="37669-111">Kazanç Hesaplama Sıklığı</span><span class="sxs-lookup"><span data-stu-id="37669-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="37669-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="37669-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="37669-113">Kazanç Hesaplama sıklığı ödeme dönemi</span><span class="sxs-lookup"><span data-stu-id="37669-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="37669-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="37669-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="37669-115">Kazanç hesaplama oranı</span><span class="sxs-lookup"><span data-stu-id="37669-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="37669-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="37669-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="37669-117">Kazanç hesaplama oranı ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="37669-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="37669-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="37669-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="37669-119">Kazanç seçeneği</span><span class="sxs-lookup"><span data-stu-id="37669-119">Benefit Option</span></span> | <span data-ttu-id="37669-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="37669-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="37669-121">Kazanç planı</span><span class="sxs-lookup"><span data-stu-id="37669-121">Benefit Plan</span></span> | <span data-ttu-id="37669-122">cdm_benefitplan (özel alan desteği için etkinleştirilmedi)</span><span class="sxs-lookup"><span data-stu-id="37669-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="37669-123">Kazanç Türü</span><span class="sxs-lookup"><span data-stu-id="37669-123">Benefit Type</span></span> | <span data-ttu-id="37669-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="37669-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="37669-125">İş süreci görevleri tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-125">Business process tasks tables</span></span>

| <span data-ttu-id="37669-126">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="37669-126">Name</span></span> | <span data-ttu-id="37669-127">Tablo</span><span class="sxs-lookup"><span data-stu-id="37669-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="37669-128">İş Süreci Takvimi</span><span class="sxs-lookup"><span data-stu-id="37669-128">Business Process Calendar</span></span> | <span data-ttu-id="37669-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="37669-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="37669-130">İş Süreci Grup Ataması</span><span class="sxs-lookup"><span data-stu-id="37669-130">Business Process Group Assignment</span></span> | <span data-ttu-id="37669-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="37669-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="37669-132">İş Süreci Kitaplığı Görev Grubu</span><span class="sxs-lookup"><span data-stu-id="37669-132">Business Process Library Task Group</span></span> | <span data-ttu-id="37669-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="37669-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="37669-134">İş Süreci Aşaması</span><span class="sxs-lookup"><span data-stu-id="37669-134">Business Process Stage</span></span> | <span data-ttu-id="37669-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="37669-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="37669-136">Denetim Listesi Şablonu Başlığı</span><span class="sxs-lookup"><span data-stu-id="37669-136">Checklist Template Header</span></span> | <span data-ttu-id="37669-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="37669-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="37669-138">Denetim Listesi Şablonu Görevi</span><span class="sxs-lookup"><span data-stu-id="37669-138">Checklist Template Task</span></span> | <span data-ttu-id="37669-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="37669-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="37669-140">Ücret tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-140">Compensation tables</span></span>

| <span data-ttu-id="37669-141">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="37669-141">Name</span></span> | <span data-ttu-id="37669-142">Tablo</span><span class="sxs-lookup"><span data-stu-id="37669-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="37669-143">Ücret Sabit Planı</span><span class="sxs-lookup"><span data-stu-id="37669-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="37669-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="37669-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="37669-145">Ücret Izgarası</span><span class="sxs-lookup"><span data-stu-id="37669-145">Compensation Grid</span></span> | <span data-ttu-id="37669-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="37669-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="37669-147">Ücret Düzeyi</span><span class="sxs-lookup"><span data-stu-id="37669-147">Compensation Level</span></span> | <span data-ttu-id="37669-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="37669-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="37669-149">Maaş ödeme sıklığı</span><span class="sxs-lookup"><span data-stu-id="37669-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="37669-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="37669-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="37669-151">Ücret referans noktası ayarı</span><span class="sxs-lookup"><span data-stu-id="37669-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="37669-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="37669-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="37669-153">Ücret referans noktalarını ayar çizgisi</span><span class="sxs-lookup"><span data-stu-id="37669-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="37669-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="37669-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="37669-155">Ücret Bölgesi</span><span class="sxs-lookup"><span data-stu-id="37669-155">Compensation Region</span></span> | <span data-ttu-id="37669-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="37669-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="37669-157">Maaş yapısı</span><span class="sxs-lookup"><span data-stu-id="37669-157">Compensation Structure</span></span> | <span data-ttu-id="37669-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="37669-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="37669-159">Değişken Ücret Planı</span><span class="sxs-lookup"><span data-stu-id="37669-159">Compensation Variable Plan</span></span> | <span data-ttu-id="37669-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="37669-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="37669-161">Değişken Ücret Planı Düzeyi</span><span class="sxs-lookup"><span data-stu-id="37669-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="37669-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="37669-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="37669-163">Değişken Ücret Planı Türü</span><span class="sxs-lookup"><span data-stu-id="37669-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="37669-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="37669-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="37669-165">Sabit Ücret Etkinliği</span><span class="sxs-lookup"><span data-stu-id="37669-165">Fixed Compensation Event</span></span> | <span data-ttu-id="37669-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="37669-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="37669-167">Hakediş Ödeme Kuralı</span><span class="sxs-lookup"><span data-stu-id="37669-167">Vesting Rule</span></span> | <span data-ttu-id="37669-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="37669-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="37669-169">Çalışan Sabit Ücreti</span><span class="sxs-lookup"><span data-stu-id="37669-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="37669-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="37669-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="37669-171">Kuruluş tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-171">Organization tables</span></span>

| <span data-ttu-id="37669-172">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="37669-172">Name</span></span> | <span data-ttu-id="37669-173">Tablo</span><span class="sxs-lookup"><span data-stu-id="37669-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="37669-174">Departman</span><span class="sxs-lookup"><span data-stu-id="37669-174">Department</span></span> | <span data-ttu-id="37669-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="37669-175">cdm_department</span></span> |
| <span data-ttu-id="37669-176">İstihdam</span><span class="sxs-lookup"><span data-stu-id="37669-176">Employment</span></span> | <span data-ttu-id="37669-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="37669-177">cdm_employment</span></span> |
| <span data-ttu-id="37669-178">Şirket</span><span class="sxs-lookup"><span data-stu-id="37669-178">Company</span></span> | <span data-ttu-id="37669-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="37669-179">cdm_company</span></span> |
| <span data-ttu-id="37669-180">Görev</span><span class="sxs-lookup"><span data-stu-id="37669-180">Job</span></span> | <span data-ttu-id="37669-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="37669-181">cdm_job</span></span> |
| <span data-ttu-id="37669-182">İş İşlevi</span><span class="sxs-lookup"><span data-stu-id="37669-182">Job Function</span></span> | <span data-ttu-id="37669-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="37669-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="37669-184">İş Pozisyonu</span><span class="sxs-lookup"><span data-stu-id="37669-184">Job Position</span></span> | <span data-ttu-id="37669-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="37669-185">cdm_jobposition</span></span> |
| <span data-ttu-id="37669-186">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="37669-186">Position Type</span></span> | <span data-ttu-id="37669-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="37669-187">cdm_positiontype</span></span> |
| <span data-ttu-id="37669-188">Pozisyon Çalışan Ataması</span><span class="sxs-lookup"><span data-stu-id="37669-188">Position Worker Assignment</span></span> | <span data-ttu-id="37669-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="37669-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="37669-190">İş Pozisyonu Boyutu</span><span class="sxs-lookup"><span data-stu-id="37669-190">Job Position Dimension</span></span> | <span data-ttu-id="37669-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="37669-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="37669-192">İş Türü</span><span class="sxs-lookup"><span data-stu-id="37669-192">Job Type</span></span> | <span data-ttu-id="37669-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="37669-193">cdm_jobtype</span></span> |
| <span data-ttu-id="37669-194">Dil</span><span class="sxs-lookup"><span data-stu-id="37669-194">Language</span></span> | <span data-ttu-id="37669-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="37669-195">cdm_language</span></span> |
| <span data-ttu-id="37669-196">Ünvan</span><span class="sxs-lookup"><span data-stu-id="37669-196">Title</span></span> | <span data-ttu-id="37669-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="37669-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="37669-198">**Pozisyon türü**, **çalışan ataması pozisyon** ve **istihdam** için mali boyutlar Dataverse'e tek-yön tümleştirmesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="37669-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="37669-199">Mali boyut güncelleştirmeleri şu an için Dataverse'tan Human Resources ile eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="37669-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="37669-200">İzin ve devamsızlık tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-200">Leave and absence tables</span></span>

| <span data-ttu-id="37669-201">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="37669-201">Name</span></span> | <span data-ttu-id="37669-202">Tablo</span><span class="sxs-lookup"><span data-stu-id="37669-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="37669-203">İzin Bankası Hareketi</span><span class="sxs-lookup"><span data-stu-id="37669-203">Leave Bank Transaction</span></span> | <span data-ttu-id="37669-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="37669-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="37669-205">İzin Kaydı</span><span class="sxs-lookup"><span data-stu-id="37669-205">Leave Enrollment</span></span> | <span data-ttu-id="37669-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="37669-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="37669-207">İzin Planı</span><span class="sxs-lookup"><span data-stu-id="37669-207">Leave Plan</span></span> | <span data-ttu-id="37669-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="37669-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="37669-209">İzin İsteği</span><span class="sxs-lookup"><span data-stu-id="37669-209">Leave Request</span></span> | <span data-ttu-id="37669-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="37669-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="37669-211">Ayrılma talebi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="37669-211">Leave Request Detail</span></span> | <span data-ttu-id="37669-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="37669-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="37669-213">İzin Türü</span><span class="sxs-lookup"><span data-stu-id="37669-213">Leave Type</span></span> | <span data-ttu-id="37669-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="37669-214">cdm_leavetype</span></span> |
| <span data-ttu-id="37669-215">İzin Türü Neden Kodu</span><span class="sxs-lookup"><span data-stu-id="37669-215">Leave Type Reason Code</span></span> | <span data-ttu-id="37669-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="37669-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="37669-217">Bordro tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-217">Payroll tables</span></span>

| <span data-ttu-id="37669-218">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="37669-218">Name</span></span> | <span data-ttu-id="37669-219">Tablo</span><span class="sxs-lookup"><span data-stu-id="37669-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="37669-220">Ödeme Döngüsü</span><span class="sxs-lookup"><span data-stu-id="37669-220">Pay Cycle</span></span> | <span data-ttu-id="37669-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="37669-221">cdm_paycycle</span></span> |
| <span data-ttu-id="37669-222">Ödeme Dönemi</span><span class="sxs-lookup"><span data-stu-id="37669-222">Pay Period</span></span> | <span data-ttu-id="37669-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="37669-223">cdm_payperiod</span></span> |
| <span data-ttu-id="37669-224">Bordro Kazanç Kodu</span><span class="sxs-lookup"><span data-stu-id="37669-224">Payroll Earning Code</span></span> | <span data-ttu-id="37669-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="37669-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="37669-226">Banka hesabı ödemeleri</span><span class="sxs-lookup"><span data-stu-id="37669-226">Bank Account Disbursement</span></span> | <span data-ttu-id="37669-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="37669-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="37669-228">Vergi Bölgesi</span><span class="sxs-lookup"><span data-stu-id="37669-228">Tax Region</span></span> | <span data-ttu-id="37669-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="37669-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="37669-230">Çalışan tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-230">Worker tables</span></span>

| <span data-ttu-id="37669-231">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="37669-231">Name</span></span> | <span data-ttu-id="37669-232">Tablo</span><span class="sxs-lookup"><span data-stu-id="37669-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="37669-233">Çalışan</span><span class="sxs-lookup"><span data-stu-id="37669-233">Worker</span></span> | <span data-ttu-id="37669-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="37669-234">cdm_worker</span></span> |
| <span data-ttu-id="37669-235">Çalışan Adresi</span><span class="sxs-lookup"><span data-stu-id="37669-235">Worker Address</span></span> | <span data-ttu-id="37669-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="37669-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="37669-237">Çalışan Kişisel Bilgisi</span><span class="sxs-lookup"><span data-stu-id="37669-237">Worker Personal Detail</span></span> | <span data-ttu-id="37669-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="37669-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="37669-239">Çalışan Kişi Tanımlama Numarası</span><span class="sxs-lookup"><span data-stu-id="37669-239">Worker Person Identification Number</span></span> | <span data-ttu-id="37669-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="37669-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="37669-241">Çalışan Kişi Tanımlama Türü</span><span class="sxs-lookup"><span data-stu-id="37669-241">Worker Person Identification Type</span></span> | <span data-ttu-id="37669-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="37669-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="37669-243">İş Takvimi</span><span class="sxs-lookup"><span data-stu-id="37669-243">Work Calendar</span></span> | <span data-ttu-id="37669-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="37669-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="37669-245">İş Takvimi Gün</span><span class="sxs-lookup"><span data-stu-id="37669-245">Work Calendar Day</span></span> | <span data-ttu-id="37669-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="37669-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="37669-247">İş Takvimi Tatili</span><span class="sxs-lookup"><span data-stu-id="37669-247">Work Calendar Holiday</span></span> |<span data-ttu-id="37669-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="37669-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="37669-249">Çalışma takvimi tatil satırı</span><span class="sxs-lookup"><span data-stu-id="37669-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="37669-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="37669-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="37669-251">Çalışma Takvimi Zaman Aralığı</span><span class="sxs-lookup"><span data-stu-id="37669-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="37669-252">cdm_workcalendartimeinterval (özel alan desteği için etkinleştirilmedi)</span><span class="sxs-lookup"><span data-stu-id="37669-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="37669-253">Çalışan Banka Hesabı</span><span class="sxs-lookup"><span data-stu-id="37669-253">Worker Bank Account</span></span> | <span data-ttu-id="37669-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="37669-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="37669-255">Çalışan kurulum tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-255">Worker setup tables</span></span>

| <span data-ttu-id="37669-256">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="37669-256">Name</span></span> | <span data-ttu-id="37669-257">Tablo</span><span class="sxs-lookup"><span data-stu-id="37669-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="37669-258">Gazilik Durumu</span><span class="sxs-lookup"><span data-stu-id="37669-258">Veteran Status</span></span> | <span data-ttu-id="37669-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="37669-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="37669-260">Etnik Köken</span><span class="sxs-lookup"><span data-stu-id="37669-260">Ethnic Origin</span></span> | <span data-ttu-id="37669-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="37669-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="37669-262">Neden Kodu</span><span class="sxs-lookup"><span data-stu-id="37669-262">Reason Code</span></span> | <span data-ttu-id="37669-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="37669-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="37669-264">Kişi Kimliğini Düzenleyen Kurum</span><span class="sxs-lookup"><span data-stu-id="37669-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="37669-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="37669-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="37669-266">Yetkinlik tabloları</span><span class="sxs-lookup"><span data-stu-id="37669-266">Competency tables</span></span>

| <span data-ttu-id="37669-267">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="37669-267">Name</span></span> | <span data-ttu-id="37669-268">Tablo</span><span class="sxs-lookup"><span data-stu-id="37669-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="37669-269">Yetenek Türü</span><span class="sxs-lookup"><span data-stu-id="37669-269">Skill Type</span></span> | <span data-ttu-id="37669-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="37669-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="37669-271">Tablo ilişkisi modelleri</span><span class="sxs-lookup"><span data-stu-id="37669-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="37669-272">Çalışan</span><span class="sxs-lookup"><span data-stu-id="37669-272">Worker</span></span>

![Çalışan](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="37669-274">İş ve Iş pozisyonu</span><span class="sxs-lookup"><span data-stu-id="37669-274">Job and Job Position</span></span>

![İş ve Iş pozisyonu](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="37669-276">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="37669-276">Benefits</span></span>

![Kazançlar](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="37669-278">Ücret</span><span class="sxs-lookup"><span data-stu-id="37669-278">Compensation</span></span>

![Ücret](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="37669-280">Bırak</span><span class="sxs-lookup"><span data-stu-id="37669-280">Leave</span></span>

![Bırak](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="37669-282">İş Takvimi</span><span class="sxs-lookup"><span data-stu-id="37669-282">Work Calendar</span></span>

![İş Takvimi](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="37669-284">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="37669-284">See also</span></span>

[<span data-ttu-id="37669-285">Veri tümleştirme teknolojisi seçme</span><span class="sxs-lookup"><span data-stu-id="37669-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="37669-286">Dataverse tümleştirmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="37669-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="37669-287">Dataverse sanal tablolarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="37669-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="37669-288">Human Resources sanal tablolarıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="37669-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="37669-289">Microsoft Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="37669-289">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="37669-290">Terminoloji güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="37669-290">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]