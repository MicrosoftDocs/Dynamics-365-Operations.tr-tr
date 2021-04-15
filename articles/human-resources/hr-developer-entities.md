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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e316cda9b9c5361c0a2837e7ed6c050e76cc39b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793621"
---
# <a name="dataverse-tables"></a><span data-ttu-id="26a98-103">Dataverse tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="26a98-104">Microsoft Dynamics 365 Human Resources, Dataverse genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="26a98-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="26a98-105">Human Resources varlıkları Dataverse tablolarına karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="26a98-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="26a98-106">Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="26a98-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="26a98-107">Aşağıdaki Dataverse tabloları Human Resources varlıklarına göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="26a98-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="26a98-108">Fayda tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-108">Benefit tables</span></span>

| <span data-ttu-id="26a98-109">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="26a98-109">Name</span></span> | <span data-ttu-id="26a98-110">Tablo</span><span class="sxs-lookup"><span data-stu-id="26a98-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26a98-111">Kazanç Hesaplama Sıklığı</span><span class="sxs-lookup"><span data-stu-id="26a98-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="26a98-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="26a98-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="26a98-113">Kazanç Hesaplama sıklığı ödeme dönemi</span><span class="sxs-lookup"><span data-stu-id="26a98-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="26a98-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="26a98-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="26a98-115">Kazanç hesaplama oranı</span><span class="sxs-lookup"><span data-stu-id="26a98-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="26a98-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="26a98-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="26a98-117">Kazanç hesaplama oranı ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="26a98-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="26a98-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="26a98-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="26a98-119">Kazanç seçeneği</span><span class="sxs-lookup"><span data-stu-id="26a98-119">Benefit Option</span></span> | <span data-ttu-id="26a98-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="26a98-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="26a98-121">Kazanç planı</span><span class="sxs-lookup"><span data-stu-id="26a98-121">Benefit Plan</span></span> | <span data-ttu-id="26a98-122">cdm_benefitplan (özel alan desteği için etkinleştirilmedi)</span><span class="sxs-lookup"><span data-stu-id="26a98-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="26a98-123">Kazanç Türü</span><span class="sxs-lookup"><span data-stu-id="26a98-123">Benefit Type</span></span> | <span data-ttu-id="26a98-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="26a98-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="26a98-125">İş süreci görevleri tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-125">Business process tasks tables</span></span>

| <span data-ttu-id="26a98-126">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="26a98-126">Name</span></span> | <span data-ttu-id="26a98-127">Tablo</span><span class="sxs-lookup"><span data-stu-id="26a98-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26a98-128">İş Süreci Takvimi</span><span class="sxs-lookup"><span data-stu-id="26a98-128">Business Process Calendar</span></span> | <span data-ttu-id="26a98-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="26a98-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="26a98-130">İş Süreci Grup Ataması</span><span class="sxs-lookup"><span data-stu-id="26a98-130">Business Process Group Assignment</span></span> | <span data-ttu-id="26a98-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="26a98-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="26a98-132">İş Süreci Kitaplığı Görev Grubu</span><span class="sxs-lookup"><span data-stu-id="26a98-132">Business Process Library Task Group</span></span> | <span data-ttu-id="26a98-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="26a98-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="26a98-134">İş Süreci Aşaması</span><span class="sxs-lookup"><span data-stu-id="26a98-134">Business Process Stage</span></span> | <span data-ttu-id="26a98-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="26a98-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="26a98-136">Denetim Listesi Şablonu Başlığı</span><span class="sxs-lookup"><span data-stu-id="26a98-136">Checklist Template Header</span></span> | <span data-ttu-id="26a98-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="26a98-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="26a98-138">Denetim Listesi Şablonu Görevi</span><span class="sxs-lookup"><span data-stu-id="26a98-138">Checklist Template Task</span></span> | <span data-ttu-id="26a98-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="26a98-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="26a98-140">Ücret tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-140">Compensation tables</span></span>

| <span data-ttu-id="26a98-141">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="26a98-141">Name</span></span> | <span data-ttu-id="26a98-142">Tablo</span><span class="sxs-lookup"><span data-stu-id="26a98-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26a98-143">Ücret Sabit Planı</span><span class="sxs-lookup"><span data-stu-id="26a98-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="26a98-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="26a98-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="26a98-145">Ücret Izgarası</span><span class="sxs-lookup"><span data-stu-id="26a98-145">Compensation Grid</span></span> | <span data-ttu-id="26a98-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="26a98-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="26a98-147">Ücret Düzeyi</span><span class="sxs-lookup"><span data-stu-id="26a98-147">Compensation Level</span></span> | <span data-ttu-id="26a98-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="26a98-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="26a98-149">Maaş ödeme sıklığı</span><span class="sxs-lookup"><span data-stu-id="26a98-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="26a98-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="26a98-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="26a98-151">Ücret referans noktası ayarı</span><span class="sxs-lookup"><span data-stu-id="26a98-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="26a98-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="26a98-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="26a98-153">Ücret referans noktalarını ayar çizgisi</span><span class="sxs-lookup"><span data-stu-id="26a98-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="26a98-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="26a98-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="26a98-155">Ücret Bölgesi</span><span class="sxs-lookup"><span data-stu-id="26a98-155">Compensation Region</span></span> | <span data-ttu-id="26a98-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="26a98-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="26a98-157">Maaş yapısı</span><span class="sxs-lookup"><span data-stu-id="26a98-157">Compensation Structure</span></span> | <span data-ttu-id="26a98-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="26a98-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="26a98-159">Değişken Ücret Planı</span><span class="sxs-lookup"><span data-stu-id="26a98-159">Compensation Variable Plan</span></span> | <span data-ttu-id="26a98-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="26a98-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="26a98-161">Değişken Ücret Planı Düzeyi</span><span class="sxs-lookup"><span data-stu-id="26a98-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="26a98-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="26a98-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="26a98-163">Değişken Ücret Planı Türü</span><span class="sxs-lookup"><span data-stu-id="26a98-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="26a98-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="26a98-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="26a98-165">Sabit Ücret Etkinliği</span><span class="sxs-lookup"><span data-stu-id="26a98-165">Fixed Compensation Event</span></span> | <span data-ttu-id="26a98-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="26a98-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="26a98-167">Hakediş Ödeme Kuralı</span><span class="sxs-lookup"><span data-stu-id="26a98-167">Vesting Rule</span></span> | <span data-ttu-id="26a98-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="26a98-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="26a98-169">Çalışan Sabit Ücreti</span><span class="sxs-lookup"><span data-stu-id="26a98-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="26a98-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="26a98-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="26a98-171">Kuruluş tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-171">Organization tables</span></span>

| <span data-ttu-id="26a98-172">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="26a98-172">Name</span></span> | <span data-ttu-id="26a98-173">Tablo</span><span class="sxs-lookup"><span data-stu-id="26a98-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26a98-174">Departman</span><span class="sxs-lookup"><span data-stu-id="26a98-174">Department</span></span> | <span data-ttu-id="26a98-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="26a98-175">cdm_department</span></span> |
| <span data-ttu-id="26a98-176">İstihdam</span><span class="sxs-lookup"><span data-stu-id="26a98-176">Employment</span></span> | <span data-ttu-id="26a98-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="26a98-177">cdm_employment</span></span> |
| <span data-ttu-id="26a98-178">Şirket</span><span class="sxs-lookup"><span data-stu-id="26a98-178">Company</span></span> | <span data-ttu-id="26a98-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="26a98-179">cdm_company</span></span> |
| <span data-ttu-id="26a98-180">Görev</span><span class="sxs-lookup"><span data-stu-id="26a98-180">Job</span></span> | <span data-ttu-id="26a98-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="26a98-181">cdm_job</span></span> |
| <span data-ttu-id="26a98-182">İş İşlevi</span><span class="sxs-lookup"><span data-stu-id="26a98-182">Job Function</span></span> | <span data-ttu-id="26a98-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="26a98-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="26a98-184">İş Pozisyonu</span><span class="sxs-lookup"><span data-stu-id="26a98-184">Job Position</span></span> | <span data-ttu-id="26a98-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="26a98-185">cdm_jobposition</span></span> |
| <span data-ttu-id="26a98-186">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="26a98-186">Position Type</span></span> | <span data-ttu-id="26a98-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="26a98-187">cdm_positiontype</span></span> |
| <span data-ttu-id="26a98-188">Pozisyon Çalışan Ataması</span><span class="sxs-lookup"><span data-stu-id="26a98-188">Position Worker Assignment</span></span> | <span data-ttu-id="26a98-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="26a98-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="26a98-190">İş Pozisyonu Boyutu</span><span class="sxs-lookup"><span data-stu-id="26a98-190">Job Position Dimension</span></span> | <span data-ttu-id="26a98-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="26a98-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="26a98-192">İş Türü</span><span class="sxs-lookup"><span data-stu-id="26a98-192">Job Type</span></span> | <span data-ttu-id="26a98-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="26a98-193">cdm_jobtype</span></span> |
| <span data-ttu-id="26a98-194">Dil</span><span class="sxs-lookup"><span data-stu-id="26a98-194">Language</span></span> | <span data-ttu-id="26a98-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="26a98-195">cdm_language</span></span> |
| <span data-ttu-id="26a98-196">Ünvan</span><span class="sxs-lookup"><span data-stu-id="26a98-196">Title</span></span> | <span data-ttu-id="26a98-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="26a98-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="26a98-198">**Pozisyon türü**, **çalışan ataması pozisyon** ve **istihdam** için mali boyutlar Dataverse'e tek-yön tümleştirmesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="26a98-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="26a98-199">Mali boyut güncelleştirmeleri şu an için Dataverse'tan Human Resources ile eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="26a98-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="26a98-200">İzin ve devamsızlık tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-200">Leave and absence tables</span></span>

| <span data-ttu-id="26a98-201">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="26a98-201">Name</span></span> | <span data-ttu-id="26a98-202">Tablo</span><span class="sxs-lookup"><span data-stu-id="26a98-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26a98-203">İzin Bankası Hareketi</span><span class="sxs-lookup"><span data-stu-id="26a98-203">Leave Bank Transaction</span></span> | <span data-ttu-id="26a98-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="26a98-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="26a98-205">İzin Kaydı</span><span class="sxs-lookup"><span data-stu-id="26a98-205">Leave Enrollment</span></span> | <span data-ttu-id="26a98-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="26a98-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="26a98-207">İzin Planı</span><span class="sxs-lookup"><span data-stu-id="26a98-207">Leave Plan</span></span> | <span data-ttu-id="26a98-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="26a98-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="26a98-209">İzin İsteği</span><span class="sxs-lookup"><span data-stu-id="26a98-209">Leave Request</span></span> | <span data-ttu-id="26a98-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="26a98-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="26a98-211">Ayrılma talebi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="26a98-211">Leave Request Detail</span></span> | <span data-ttu-id="26a98-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="26a98-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="26a98-213">İzin Türü</span><span class="sxs-lookup"><span data-stu-id="26a98-213">Leave Type</span></span> | <span data-ttu-id="26a98-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="26a98-214">cdm_leavetype</span></span> |
| <span data-ttu-id="26a98-215">İzin Türü Neden Kodu</span><span class="sxs-lookup"><span data-stu-id="26a98-215">Leave Type Reason Code</span></span> | <span data-ttu-id="26a98-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="26a98-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="26a98-217">Bordro tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-217">Payroll tables</span></span>

| <span data-ttu-id="26a98-218">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="26a98-218">Name</span></span> | <span data-ttu-id="26a98-219">Tablo</span><span class="sxs-lookup"><span data-stu-id="26a98-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26a98-220">Ödeme Döngüsü</span><span class="sxs-lookup"><span data-stu-id="26a98-220">Pay Cycle</span></span> | <span data-ttu-id="26a98-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="26a98-221">cdm_paycycle</span></span> |
| <span data-ttu-id="26a98-222">Ödeme Dönemi</span><span class="sxs-lookup"><span data-stu-id="26a98-222">Pay Period</span></span> | <span data-ttu-id="26a98-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="26a98-223">cdm_payperiod</span></span> |
| <span data-ttu-id="26a98-224">Bordro Kazanç Kodu</span><span class="sxs-lookup"><span data-stu-id="26a98-224">Payroll Earning Code</span></span> | <span data-ttu-id="26a98-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="26a98-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="26a98-226">Banka hesabı ödemeleri</span><span class="sxs-lookup"><span data-stu-id="26a98-226">Bank Account Disbursement</span></span> | <span data-ttu-id="26a98-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="26a98-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="26a98-228">Vergi Bölgesi</span><span class="sxs-lookup"><span data-stu-id="26a98-228">Tax Region</span></span> | <span data-ttu-id="26a98-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="26a98-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="26a98-230">Çalışan tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-230">Worker tables</span></span>

| <span data-ttu-id="26a98-231">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="26a98-231">Name</span></span> | <span data-ttu-id="26a98-232">Tablo</span><span class="sxs-lookup"><span data-stu-id="26a98-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26a98-233">Çalışan</span><span class="sxs-lookup"><span data-stu-id="26a98-233">Worker</span></span> | <span data-ttu-id="26a98-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="26a98-234">cdm_worker</span></span> |
| <span data-ttu-id="26a98-235">Çalışan Adresi</span><span class="sxs-lookup"><span data-stu-id="26a98-235">Worker Address</span></span> | <span data-ttu-id="26a98-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="26a98-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="26a98-237">Çalışan Kişisel Bilgisi</span><span class="sxs-lookup"><span data-stu-id="26a98-237">Worker Personal Detail</span></span> | <span data-ttu-id="26a98-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="26a98-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="26a98-239">Çalışan Kişi Tanımlama Numarası</span><span class="sxs-lookup"><span data-stu-id="26a98-239">Worker Person Identification Number</span></span> | <span data-ttu-id="26a98-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="26a98-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="26a98-241">Çalışan Kişi Tanımlama Türü</span><span class="sxs-lookup"><span data-stu-id="26a98-241">Worker Person Identification Type</span></span> | <span data-ttu-id="26a98-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="26a98-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="26a98-243">İş Takvimi</span><span class="sxs-lookup"><span data-stu-id="26a98-243">Work Calendar</span></span> | <span data-ttu-id="26a98-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="26a98-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="26a98-245">İş Takvimi Gün</span><span class="sxs-lookup"><span data-stu-id="26a98-245">Work Calendar Day</span></span> | <span data-ttu-id="26a98-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="26a98-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="26a98-247">İş Takvimi Tatili</span><span class="sxs-lookup"><span data-stu-id="26a98-247">Work Calendar Holiday</span></span> |<span data-ttu-id="26a98-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="26a98-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="26a98-249">Çalışma takvimi tatil satırı</span><span class="sxs-lookup"><span data-stu-id="26a98-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="26a98-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="26a98-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="26a98-251">Çalışma Takvimi Zaman Aralığı</span><span class="sxs-lookup"><span data-stu-id="26a98-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="26a98-252">cdm_workcalendartimeinterval (özel alan desteği için etkinleştirilmedi)</span><span class="sxs-lookup"><span data-stu-id="26a98-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="26a98-253">Çalışan Banka Hesabı</span><span class="sxs-lookup"><span data-stu-id="26a98-253">Worker Bank Account</span></span> | <span data-ttu-id="26a98-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="26a98-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="26a98-255">Çalışan kurulum tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-255">Worker setup tables</span></span>

| <span data-ttu-id="26a98-256">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="26a98-256">Name</span></span> | <span data-ttu-id="26a98-257">Tablo</span><span class="sxs-lookup"><span data-stu-id="26a98-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26a98-258">Gazilik Durumu</span><span class="sxs-lookup"><span data-stu-id="26a98-258">Veteran Status</span></span> | <span data-ttu-id="26a98-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="26a98-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="26a98-260">Etnik Köken</span><span class="sxs-lookup"><span data-stu-id="26a98-260">Ethnic Origin</span></span> | <span data-ttu-id="26a98-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="26a98-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="26a98-262">Neden Kodu</span><span class="sxs-lookup"><span data-stu-id="26a98-262">Reason Code</span></span> | <span data-ttu-id="26a98-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="26a98-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="26a98-264">Kişi Kimliğini Düzenleyen Kurum</span><span class="sxs-lookup"><span data-stu-id="26a98-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="26a98-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="26a98-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="26a98-266">Yetkinlik tabloları</span><span class="sxs-lookup"><span data-stu-id="26a98-266">Competency tables</span></span>

| <span data-ttu-id="26a98-267">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="26a98-267">Name</span></span> | <span data-ttu-id="26a98-268">Tablo</span><span class="sxs-lookup"><span data-stu-id="26a98-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26a98-269">Yetenek Türü</span><span class="sxs-lookup"><span data-stu-id="26a98-269">Skill Type</span></span> | <span data-ttu-id="26a98-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="26a98-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="26a98-271">Tablo ilişkisi modelleri</span><span class="sxs-lookup"><span data-stu-id="26a98-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="26a98-272">Çalışan</span><span class="sxs-lookup"><span data-stu-id="26a98-272">Worker</span></span>

![Çalışan](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="26a98-274">İş ve Iş pozisyonu</span><span class="sxs-lookup"><span data-stu-id="26a98-274">Job and Job Position</span></span>

![İş ve Iş pozisyonu](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="26a98-276">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="26a98-276">Benefits</span></span>

![Kazançlar](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="26a98-278">Ücret</span><span class="sxs-lookup"><span data-stu-id="26a98-278">Compensation</span></span>

![Ücret](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="26a98-280">Bırak</span><span class="sxs-lookup"><span data-stu-id="26a98-280">Leave</span></span>

![Bırak](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="26a98-282">İş Takvimi</span><span class="sxs-lookup"><span data-stu-id="26a98-282">Work Calendar</span></span>

![İş Takvimi](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="26a98-284">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="26a98-284">See also</span></span>

[<span data-ttu-id="26a98-285">Veri tümleştirme teknolojisi seçme</span><span class="sxs-lookup"><span data-stu-id="26a98-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="26a98-286">Dataverse tümleştirmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="26a98-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="26a98-287">Dataverse sanal tablolarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="26a98-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="26a98-288">Human Resources sanal tablolarıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="26a98-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="26a98-289">Microsoft Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="26a98-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="26a98-290">Terminoloji güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="26a98-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]