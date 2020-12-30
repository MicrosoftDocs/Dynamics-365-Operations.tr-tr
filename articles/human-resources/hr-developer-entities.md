---
title: Common Data Service varlıkları
description: Microsoft Dynamics 365 Human Resources, Common Data Service genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530018"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="375b5-103">Common Data Service varlıkları</span><span class="sxs-lookup"><span data-stu-id="375b5-103">Common Data Service entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="375b5-104">Microsoft Dynamics 365 Human Resources, Common Data Service genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="375b5-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="375b5-105">Common Data Service hakkında daha fazla bilgi için bkz. [Common Data Service nedir?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="375b5-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="375b5-106">Aşağıdaki İnsan Kaynakları varlıkları Common Data Service'de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="375b5-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="375b5-107">Yarar varlıkları</span><span class="sxs-lookup"><span data-stu-id="375b5-107">Benefit entities</span></span>

| <span data-ttu-id="375b5-108">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="375b5-108">Name</span></span> | <span data-ttu-id="375b5-109">Varlık</span><span class="sxs-lookup"><span data-stu-id="375b5-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="375b5-110">Kazanç Hesaplama Sıklığı</span><span class="sxs-lookup"><span data-stu-id="375b5-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="375b5-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="375b5-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="375b5-112">Kazanç Hesaplama sıklığı ödeme dönemi</span><span class="sxs-lookup"><span data-stu-id="375b5-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="375b5-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="375b5-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="375b5-114">Kazanç hesaplama oranı</span><span class="sxs-lookup"><span data-stu-id="375b5-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="375b5-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="375b5-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="375b5-116">Kazanç hesaplama oranı ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="375b5-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="375b5-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="375b5-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="375b5-118">Kazanç seçeneği</span><span class="sxs-lookup"><span data-stu-id="375b5-118">Benefit Option</span></span> | <span data-ttu-id="375b5-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="375b5-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="375b5-120">Kazanç planı</span><span class="sxs-lookup"><span data-stu-id="375b5-120">Benefit Plan</span></span> | <span data-ttu-id="375b5-121">cdm_benefitplan (özel alan desteği için etkinleştirilmedi)</span><span class="sxs-lookup"><span data-stu-id="375b5-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="375b5-122">Kazanç Türü</span><span class="sxs-lookup"><span data-stu-id="375b5-122">Benefit Type</span></span> | <span data-ttu-id="375b5-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="375b5-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="375b5-124">İş işlemi görevleri varlıkları</span><span class="sxs-lookup"><span data-stu-id="375b5-124">Business process tasks entities</span></span>

| <span data-ttu-id="375b5-125">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="375b5-125">Name</span></span> | <span data-ttu-id="375b5-126">Varlık</span><span class="sxs-lookup"><span data-stu-id="375b5-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="375b5-127">İş Süreci Takvimi</span><span class="sxs-lookup"><span data-stu-id="375b5-127">Business Process Calendar</span></span> | <span data-ttu-id="375b5-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="375b5-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="375b5-129">İş Süreci Grup Ataması</span><span class="sxs-lookup"><span data-stu-id="375b5-129">Business Process Group Assignment</span></span> | <span data-ttu-id="375b5-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="375b5-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="375b5-131">İş Süreci Kitaplığı Görev Grubu</span><span class="sxs-lookup"><span data-stu-id="375b5-131">Business Process Library Task Group</span></span> | <span data-ttu-id="375b5-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="375b5-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="375b5-133">İş Süreci Aşaması</span><span class="sxs-lookup"><span data-stu-id="375b5-133">Business Process Stage</span></span> | <span data-ttu-id="375b5-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="375b5-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="375b5-135">Denetim Listesi Şablonu Başlığı</span><span class="sxs-lookup"><span data-stu-id="375b5-135">Checklist Template Header</span></span> | <span data-ttu-id="375b5-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="375b5-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="375b5-137">Denetim Listesi Şablonu Görevi</span><span class="sxs-lookup"><span data-stu-id="375b5-137">Checklist Template Task</span></span> | <span data-ttu-id="375b5-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="375b5-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="375b5-139">Ücret varlıkları</span><span class="sxs-lookup"><span data-stu-id="375b5-139">Compensation entities</span></span>

| <span data-ttu-id="375b5-140">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="375b5-140">Name</span></span> | <span data-ttu-id="375b5-141">Varlık</span><span class="sxs-lookup"><span data-stu-id="375b5-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="375b5-142">Sabit ücret planı</span><span class="sxs-lookup"><span data-stu-id="375b5-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="375b5-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="375b5-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="375b5-144">Ücret Izgarası</span><span class="sxs-lookup"><span data-stu-id="375b5-144">Compensation Grid</span></span> | <span data-ttu-id="375b5-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="375b5-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="375b5-146">Ücret Düzeyi</span><span class="sxs-lookup"><span data-stu-id="375b5-146">Compensation Level</span></span> | <span data-ttu-id="375b5-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="375b5-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="375b5-148">Maaş ödeme sıklığı</span><span class="sxs-lookup"><span data-stu-id="375b5-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="375b5-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="375b5-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="375b5-150">Ücret referans noktası ayarı</span><span class="sxs-lookup"><span data-stu-id="375b5-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="375b5-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="375b5-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="375b5-152">Ücret referans noktalarını ayar çizgisi</span><span class="sxs-lookup"><span data-stu-id="375b5-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="375b5-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="375b5-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="375b5-154">Ücret Bölgesi</span><span class="sxs-lookup"><span data-stu-id="375b5-154">Compensation Region</span></span> | <span data-ttu-id="375b5-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="375b5-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="375b5-156">Maaş yapısı</span><span class="sxs-lookup"><span data-stu-id="375b5-156">Compensation Structure</span></span> | <span data-ttu-id="375b5-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="375b5-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="375b5-158">Değişken Ücret Planı</span><span class="sxs-lookup"><span data-stu-id="375b5-158">Compensation Variable Plan</span></span> | <span data-ttu-id="375b5-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="375b5-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="375b5-160">Değişken Ücret Planı Düzeyi</span><span class="sxs-lookup"><span data-stu-id="375b5-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="375b5-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="375b5-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="375b5-162">Değişken Ücret Planı Türü</span><span class="sxs-lookup"><span data-stu-id="375b5-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="375b5-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="375b5-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="375b5-164">Sabit Ücret Etkinliği</span><span class="sxs-lookup"><span data-stu-id="375b5-164">Fixed Compensation Event</span></span> | <span data-ttu-id="375b5-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="375b5-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="375b5-166">Hakediş Ödeme Kuralı</span><span class="sxs-lookup"><span data-stu-id="375b5-166">Vesting Rule</span></span> | <span data-ttu-id="375b5-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="375b5-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="375b5-168">Çalışan ücreti sabit</span><span class="sxs-lookup"><span data-stu-id="375b5-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="375b5-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="375b5-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="375b5-170">Kuruluş varlıkları</span><span class="sxs-lookup"><span data-stu-id="375b5-170">Organization entities</span></span>

| <span data-ttu-id="375b5-171">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="375b5-171">Name</span></span> | <span data-ttu-id="375b5-172">Varlık</span><span class="sxs-lookup"><span data-stu-id="375b5-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="375b5-173">Departman</span><span class="sxs-lookup"><span data-stu-id="375b5-173">Department</span></span> | <span data-ttu-id="375b5-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="375b5-174">cdm_department</span></span> |
| <span data-ttu-id="375b5-175">İstihdam</span><span class="sxs-lookup"><span data-stu-id="375b5-175">Employment</span></span> | <span data-ttu-id="375b5-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="375b5-176">cdm_employment</span></span> |
| <span data-ttu-id="375b5-177">Şirket</span><span class="sxs-lookup"><span data-stu-id="375b5-177">Company</span></span> | <span data-ttu-id="375b5-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="375b5-178">cdm_company</span></span> |
| <span data-ttu-id="375b5-179">Görev</span><span class="sxs-lookup"><span data-stu-id="375b5-179">Job</span></span> | <span data-ttu-id="375b5-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="375b5-180">cdm_job</span></span> |
| <span data-ttu-id="375b5-181">İş İşlevi</span><span class="sxs-lookup"><span data-stu-id="375b5-181">Job Function</span></span> | <span data-ttu-id="375b5-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="375b5-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="375b5-183">İş Pozisyonu</span><span class="sxs-lookup"><span data-stu-id="375b5-183">Job Position</span></span> | <span data-ttu-id="375b5-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="375b5-184">cdm_jobposition</span></span> |
| <span data-ttu-id="375b5-185">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="375b5-185">Position Type</span></span> | <span data-ttu-id="375b5-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="375b5-186">cdm_positiontype</span></span> |
| <span data-ttu-id="375b5-187">Pozisyon Çalışan Ataması</span><span class="sxs-lookup"><span data-stu-id="375b5-187">Position Worker Assignment</span></span> | <span data-ttu-id="375b5-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="375b5-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="375b5-189">İş Pozisyonu Boyutu</span><span class="sxs-lookup"><span data-stu-id="375b5-189">Job Position Dimension</span></span> | <span data-ttu-id="375b5-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="375b5-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="375b5-191">İş Türü</span><span class="sxs-lookup"><span data-stu-id="375b5-191">Job Type</span></span> | <span data-ttu-id="375b5-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="375b5-192">cdm_jobtype</span></span> |
| <span data-ttu-id="375b5-193">Dil</span><span class="sxs-lookup"><span data-stu-id="375b5-193">Language</span></span> | <span data-ttu-id="375b5-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="375b5-194">cdm_language</span></span> |
| <span data-ttu-id="375b5-195">Ünvan</span><span class="sxs-lookup"><span data-stu-id="375b5-195">Title</span></span> | <span data-ttu-id="375b5-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="375b5-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="375b5-197">**Pozisyon türü**, **çalışan ataması pozisyon** ve **istihdam** için mali boyutlar Common Data Service'e tek-yön tümleştirmesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="375b5-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="375b5-198">Mali boyut güncelleştirmeleri şu an için Common Data Service'tan Human Resources ile eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="375b5-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="375b5-199">İzin ve devamsızlık varlıkları</span><span class="sxs-lookup"><span data-stu-id="375b5-199">Leave and absence entities</span></span>

| <span data-ttu-id="375b5-200">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="375b5-200">Name</span></span> | <span data-ttu-id="375b5-201">Varlık</span><span class="sxs-lookup"><span data-stu-id="375b5-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="375b5-202">İzin Bankası Hareketi</span><span class="sxs-lookup"><span data-stu-id="375b5-202">Leave Bank Transaction</span></span> | <span data-ttu-id="375b5-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="375b5-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="375b5-204">Ayrılma Kaydı</span><span class="sxs-lookup"><span data-stu-id="375b5-204">Leave Enrollment</span></span> | <span data-ttu-id="375b5-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="375b5-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="375b5-206">İzin Planı</span><span class="sxs-lookup"><span data-stu-id="375b5-206">Leave Plan</span></span> | <span data-ttu-id="375b5-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="375b5-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="375b5-208">İzin İsteği</span><span class="sxs-lookup"><span data-stu-id="375b5-208">Leave Request</span></span> | <span data-ttu-id="375b5-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="375b5-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="375b5-210">Ayrılma talebi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="375b5-210">Leave Request Detail</span></span> | <span data-ttu-id="375b5-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="375b5-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="375b5-212">İzin Türü</span><span class="sxs-lookup"><span data-stu-id="375b5-212">Leave Type</span></span> | <span data-ttu-id="375b5-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="375b5-213">cdm_leavetype</span></span> |
| <span data-ttu-id="375b5-214">İzin Türü Neden Kodu</span><span class="sxs-lookup"><span data-stu-id="375b5-214">Leave Type Reason Code</span></span> | <span data-ttu-id="375b5-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="375b5-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="375b5-216">Bordro varlıkları</span><span class="sxs-lookup"><span data-stu-id="375b5-216">Payroll entities</span></span>

| <span data-ttu-id="375b5-217">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="375b5-217">Name</span></span> | <span data-ttu-id="375b5-218">Varlık</span><span class="sxs-lookup"><span data-stu-id="375b5-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="375b5-219">Ödeme Döngüsü</span><span class="sxs-lookup"><span data-stu-id="375b5-219">Pay Cycle</span></span> | <span data-ttu-id="375b5-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="375b5-220">cdm_paycycle</span></span> |
| <span data-ttu-id="375b5-221">Ödeme Dönemi</span><span class="sxs-lookup"><span data-stu-id="375b5-221">Pay Period</span></span> | <span data-ttu-id="375b5-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="375b5-222">cdm_payperiod</span></span> |
| <span data-ttu-id="375b5-223">Bordro kazanç kodu</span><span class="sxs-lookup"><span data-stu-id="375b5-223">Payroll Earning Code</span></span> | <span data-ttu-id="375b5-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="375b5-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="375b5-225">Banka hesabı ödemeleri</span><span class="sxs-lookup"><span data-stu-id="375b5-225">Bank Account Disbursement</span></span> | <span data-ttu-id="375b5-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="375b5-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="375b5-227">Vergi bölgesi</span><span class="sxs-lookup"><span data-stu-id="375b5-227">Tax Region</span></span> | <span data-ttu-id="375b5-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="375b5-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="375b5-229">Çalışan kişilikler</span><span class="sxs-lookup"><span data-stu-id="375b5-229">Worker entities</span></span>

| <span data-ttu-id="375b5-230">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="375b5-230">Name</span></span> | <span data-ttu-id="375b5-231">Varlık</span><span class="sxs-lookup"><span data-stu-id="375b5-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="375b5-232">Çalışan</span><span class="sxs-lookup"><span data-stu-id="375b5-232">Worker</span></span> | <span data-ttu-id="375b5-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="375b5-233">cdm_worker</span></span> |
| <span data-ttu-id="375b5-234">Çalışan Adresi</span><span class="sxs-lookup"><span data-stu-id="375b5-234">Worker Address</span></span> | <span data-ttu-id="375b5-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="375b5-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="375b5-236">Çalışan Kişisel Ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="375b5-236">Worker Personal Detail</span></span> | <span data-ttu-id="375b5-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="375b5-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="375b5-238">Çalışan Kişi Tanımlama Numarası</span><span class="sxs-lookup"><span data-stu-id="375b5-238">Worker Person Identification Number</span></span> | <span data-ttu-id="375b5-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="375b5-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="375b5-240">Çalışan Kişi Tanımlama Türü</span><span class="sxs-lookup"><span data-stu-id="375b5-240">Worker Person Identification Type</span></span> | <span data-ttu-id="375b5-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="375b5-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="375b5-242">İş Takvimi</span><span class="sxs-lookup"><span data-stu-id="375b5-242">Work Calendar</span></span> | <span data-ttu-id="375b5-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="375b5-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="375b5-244">İş Takvimi Gün</span><span class="sxs-lookup"><span data-stu-id="375b5-244">Work Calendar Day</span></span> | <span data-ttu-id="375b5-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="375b5-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="375b5-246">İş Takvimi Tatili</span><span class="sxs-lookup"><span data-stu-id="375b5-246">Work Calendar Holiday</span></span> |<span data-ttu-id="375b5-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="375b5-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="375b5-248">Çalışma takvimi tatil satırı</span><span class="sxs-lookup"><span data-stu-id="375b5-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="375b5-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="375b5-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="375b5-250">Çalışma Takvimi Zaman Aralığı</span><span class="sxs-lookup"><span data-stu-id="375b5-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="375b5-251">cdm_workcalendartimeinterval (özel alan desteği için etkinleştirilmedi)</span><span class="sxs-lookup"><span data-stu-id="375b5-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="375b5-252">Çalışan banka hesabı</span><span class="sxs-lookup"><span data-stu-id="375b5-252">Worker Bank Account</span></span> | <span data-ttu-id="375b5-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="375b5-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="375b5-254">Çalışan kurulum varlıkları</span><span class="sxs-lookup"><span data-stu-id="375b5-254">Worker setup entities</span></span>

| <span data-ttu-id="375b5-255">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="375b5-255">Name</span></span> | <span data-ttu-id="375b5-256">Varlık</span><span class="sxs-lookup"><span data-stu-id="375b5-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="375b5-257">Gazilik Durumu</span><span class="sxs-lookup"><span data-stu-id="375b5-257">Veteran Status</span></span> | <span data-ttu-id="375b5-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="375b5-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="375b5-259">Etnik Kökeni</span><span class="sxs-lookup"><span data-stu-id="375b5-259">Ethnic Origin</span></span> | <span data-ttu-id="375b5-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="375b5-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="375b5-261">Neden Kodu</span><span class="sxs-lookup"><span data-stu-id="375b5-261">Reason Code</span></span> | <span data-ttu-id="375b5-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="375b5-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="375b5-263">Kişi kimliği veren acentesi</span><span class="sxs-lookup"><span data-stu-id="375b5-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="375b5-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="375b5-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="375b5-265">Yetki tüzel kişilikler</span><span class="sxs-lookup"><span data-stu-id="375b5-265">Competency entities</span></span>

| <span data-ttu-id="375b5-266">Dosya Adı</span><span class="sxs-lookup"><span data-stu-id="375b5-266">Name</span></span> | <span data-ttu-id="375b5-267">Varlık</span><span class="sxs-lookup"><span data-stu-id="375b5-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="375b5-268">Yetenek türü</span><span class="sxs-lookup"><span data-stu-id="375b5-268">Skill Type</span></span> | <span data-ttu-id="375b5-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="375b5-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="375b5-270">Varlık ilişki modelleri</span><span class="sxs-lookup"><span data-stu-id="375b5-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="375b5-271">Çalışan</span><span class="sxs-lookup"><span data-stu-id="375b5-271">Worker</span></span>

![Çalışan](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="375b5-273">İş ve Iş pozisyonu</span><span class="sxs-lookup"><span data-stu-id="375b5-273">Job and Job Position</span></span>

![İş ve Iş pozisyonu](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="375b5-275">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="375b5-275">Benefits</span></span>

![Kazançlar](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="375b5-277">Ücret</span><span class="sxs-lookup"><span data-stu-id="375b5-277">Compensation</span></span>

![Ücret](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="375b5-279">Bırak</span><span class="sxs-lookup"><span data-stu-id="375b5-279">Leave</span></span>

![Bırak](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="375b5-281">İş Takvimi</span><span class="sxs-lookup"><span data-stu-id="375b5-281">Work Calendar</span></span>

![İş Takvimi](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="375b5-283">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="375b5-283">See also</span></span>

[<span data-ttu-id="375b5-284">Veri tümleştirme teknolojisi seçme</span><span class="sxs-lookup"><span data-stu-id="375b5-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="375b5-285">Common Data Service tümleştirmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="375b5-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
