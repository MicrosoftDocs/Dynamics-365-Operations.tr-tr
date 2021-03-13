---
title: Dataverse tabloları
description: Microsoft Dynamics 365 Human Resources, Dataverse genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: 2f075a8e96af55b1363d2d51db377c5b25c38775
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114630"
---
# <a name="dataverse-tables"></a><span data-ttu-id="b5ad9-103">Dataverse tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-103">Dataverse tables</span></span>

<span data-ttu-id="b5ad9-104">Microsoft Dynamics 365 Human Resources, Dataverse genişletilebilirlik ve tümleştirme senaryolarını etkinleştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b5ad9-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="b5ad9-105">Human Resources varlıkları Dataverse tablolarına karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="b5ad9-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="b5ad9-106">Dataverse (önceden Common Data Service) ve terminoloji güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Microsoft Dataverse nedir?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="b5ad9-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="b5ad9-107">Aşağıdaki Dataverse tabloları Human Resources varlıklarına göre kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b5ad9-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="b5ad9-108">Fayda tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-108">Benefit tables</span></span>

| <span data-ttu-id="b5ad9-109">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-109">Name</span></span> | <span data-ttu-id="b5ad9-110">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5ad9-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b5ad9-111">Kazanç Hesaplama Sıklığı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="b5ad9-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="b5ad9-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="b5ad9-113">Kazanç Hesaplama sıklığı ödeme dönemi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="b5ad9-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="b5ad9-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="b5ad9-115">Kazanç hesaplama oranı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="b5ad9-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="b5ad9-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="b5ad9-117">Kazanç hesaplama oranı ayrıntısı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="b5ad9-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="b5ad9-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="b5ad9-119">Kazanç seçeneği</span><span class="sxs-lookup"><span data-stu-id="b5ad9-119">Benefit Option</span></span> | <span data-ttu-id="b5ad9-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="b5ad9-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="b5ad9-121">Kazanç planı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-121">Benefit Plan</span></span> | <span data-ttu-id="b5ad9-122">cdm_benefitplan (özel alan desteği için etkinleştirilmedi)</span><span class="sxs-lookup"><span data-stu-id="b5ad9-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="b5ad9-123">Kazanç Türü</span><span class="sxs-lookup"><span data-stu-id="b5ad9-123">Benefit Type</span></span> | <span data-ttu-id="b5ad9-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="b5ad9-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="b5ad9-125">İş süreci görevleri tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-125">Business process tasks tables</span></span>

| <span data-ttu-id="b5ad9-126">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-126">Name</span></span> | <span data-ttu-id="b5ad9-127">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5ad9-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b5ad9-128">İş Süreci Takvimi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-128">Business Process Calendar</span></span> | <span data-ttu-id="b5ad9-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="b5ad9-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="b5ad9-130">İş Süreci Grup Ataması</span><span class="sxs-lookup"><span data-stu-id="b5ad9-130">Business Process Group Assignment</span></span> | <span data-ttu-id="b5ad9-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="b5ad9-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="b5ad9-132">İş Süreci Kitaplığı Görev Grubu</span><span class="sxs-lookup"><span data-stu-id="b5ad9-132">Business Process Library Task Group</span></span> | <span data-ttu-id="b5ad9-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="b5ad9-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="b5ad9-134">İş Süreci Aşaması</span><span class="sxs-lookup"><span data-stu-id="b5ad9-134">Business Process Stage</span></span> | <span data-ttu-id="b5ad9-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="b5ad9-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="b5ad9-136">Denetim Listesi Şablonu Başlığı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-136">Checklist Template Header</span></span> | <span data-ttu-id="b5ad9-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="b5ad9-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="b5ad9-138">Denetim Listesi Şablonu Görevi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-138">Checklist Template Task</span></span> | <span data-ttu-id="b5ad9-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="b5ad9-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="b5ad9-140">Ücret tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-140">Compensation tables</span></span>

| <span data-ttu-id="b5ad9-141">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-141">Name</span></span> | <span data-ttu-id="b5ad9-142">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5ad9-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b5ad9-143">Ücret Sabit Planı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="b5ad9-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="b5ad9-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="b5ad9-145">Ücret Izgarası</span><span class="sxs-lookup"><span data-stu-id="b5ad9-145">Compensation Grid</span></span> | <span data-ttu-id="b5ad9-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="b5ad9-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="b5ad9-147">Ücret Düzeyi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-147">Compensation Level</span></span> | <span data-ttu-id="b5ad9-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="b5ad9-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="b5ad9-149">Maaş ödeme sıklığı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="b5ad9-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="b5ad9-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="b5ad9-151">Ücret referans noktası ayarı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="b5ad9-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="b5ad9-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="b5ad9-153">Ücret referans noktalarını ayar çizgisi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="b5ad9-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="b5ad9-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="b5ad9-155">Ücret Bölgesi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-155">Compensation Region</span></span> | <span data-ttu-id="b5ad9-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="b5ad9-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="b5ad9-157">Maaş yapısı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-157">Compensation Structure</span></span> | <span data-ttu-id="b5ad9-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="b5ad9-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="b5ad9-159">Değişken Ücret Planı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-159">Compensation Variable Plan</span></span> | <span data-ttu-id="b5ad9-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="b5ad9-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="b5ad9-161">Değişken Ücret Planı Düzeyi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="b5ad9-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="b5ad9-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="b5ad9-163">Değişken Ücret Planı Türü</span><span class="sxs-lookup"><span data-stu-id="b5ad9-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="b5ad9-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="b5ad9-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="b5ad9-165">Sabit Ücret Etkinliği</span><span class="sxs-lookup"><span data-stu-id="b5ad9-165">Fixed Compensation Event</span></span> | <span data-ttu-id="b5ad9-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="b5ad9-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="b5ad9-167">Hakediş Ödeme Kuralı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-167">Vesting Rule</span></span> | <span data-ttu-id="b5ad9-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="b5ad9-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="b5ad9-169">Çalışan Sabit Ücreti</span><span class="sxs-lookup"><span data-stu-id="b5ad9-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="b5ad9-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="b5ad9-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="b5ad9-171">Kuruluş tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-171">Organization tables</span></span>

| <span data-ttu-id="b5ad9-172">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-172">Name</span></span> | <span data-ttu-id="b5ad9-173">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5ad9-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b5ad9-174">Departman</span><span class="sxs-lookup"><span data-stu-id="b5ad9-174">Department</span></span> | <span data-ttu-id="b5ad9-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="b5ad9-175">cdm_department</span></span> |
| <span data-ttu-id="b5ad9-176">İstihdam</span><span class="sxs-lookup"><span data-stu-id="b5ad9-176">Employment</span></span> | <span data-ttu-id="b5ad9-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="b5ad9-177">cdm_employment</span></span> |
| <span data-ttu-id="b5ad9-178">Şirket</span><span class="sxs-lookup"><span data-stu-id="b5ad9-178">Company</span></span> | <span data-ttu-id="b5ad9-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="b5ad9-179">cdm_company</span></span> |
| <span data-ttu-id="b5ad9-180">Görev</span><span class="sxs-lookup"><span data-stu-id="b5ad9-180">Job</span></span> | <span data-ttu-id="b5ad9-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="b5ad9-181">cdm_job</span></span> |
| <span data-ttu-id="b5ad9-182">İş İşlevi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-182">Job Function</span></span> | <span data-ttu-id="b5ad9-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="b5ad9-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="b5ad9-184">İş Pozisyonu</span><span class="sxs-lookup"><span data-stu-id="b5ad9-184">Job Position</span></span> | <span data-ttu-id="b5ad9-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="b5ad9-185">cdm_jobposition</span></span> |
| <span data-ttu-id="b5ad9-186">Pozisyon türü</span><span class="sxs-lookup"><span data-stu-id="b5ad9-186">Position Type</span></span> | <span data-ttu-id="b5ad9-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="b5ad9-187">cdm_positiontype</span></span> |
| <span data-ttu-id="b5ad9-188">Pozisyon Çalışan Ataması</span><span class="sxs-lookup"><span data-stu-id="b5ad9-188">Position Worker Assignment</span></span> | <span data-ttu-id="b5ad9-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="b5ad9-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="b5ad9-190">İş Pozisyonu Boyutu</span><span class="sxs-lookup"><span data-stu-id="b5ad9-190">Job Position Dimension</span></span> | <span data-ttu-id="b5ad9-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="b5ad9-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="b5ad9-192">İş Türü</span><span class="sxs-lookup"><span data-stu-id="b5ad9-192">Job Type</span></span> | <span data-ttu-id="b5ad9-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="b5ad9-193">cdm_jobtype</span></span> |
| <span data-ttu-id="b5ad9-194">Dil</span><span class="sxs-lookup"><span data-stu-id="b5ad9-194">Language</span></span> | <span data-ttu-id="b5ad9-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="b5ad9-195">cdm_language</span></span> |
| <span data-ttu-id="b5ad9-196">Ünvan</span><span class="sxs-lookup"><span data-stu-id="b5ad9-196">Title</span></span> | <span data-ttu-id="b5ad9-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="b5ad9-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="b5ad9-198">**Pozisyon türü**, **çalışan ataması pozisyon** ve **istihdam** için mali boyutlar Dataverse'e tek-yön tümleştirmesi sağlar.</span><span class="sxs-lookup"><span data-stu-id="b5ad9-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="b5ad9-199">Mali boyut güncelleştirmeleri şu an için Dataverse'tan Human Resources ile eşitlenmez.</span><span class="sxs-lookup"><span data-stu-id="b5ad9-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="b5ad9-200">İzin ve devamsızlık tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-200">Leave and absence tables</span></span>

| <span data-ttu-id="b5ad9-201">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-201">Name</span></span> | <span data-ttu-id="b5ad9-202">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5ad9-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b5ad9-203">İzin Bankası Hareketi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-203">Leave Bank Transaction</span></span> | <span data-ttu-id="b5ad9-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="b5ad9-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="b5ad9-205">İzin Kaydı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-205">Leave Enrollment</span></span> | <span data-ttu-id="b5ad9-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="b5ad9-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="b5ad9-207">İzin Planı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-207">Leave Plan</span></span> | <span data-ttu-id="b5ad9-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="b5ad9-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="b5ad9-209">İzin İsteği</span><span class="sxs-lookup"><span data-stu-id="b5ad9-209">Leave Request</span></span> | <span data-ttu-id="b5ad9-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="b5ad9-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="b5ad9-211">Ayrılma talebi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-211">Leave Request Detail</span></span> | <span data-ttu-id="b5ad9-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="b5ad9-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="b5ad9-213">İzin Türü</span><span class="sxs-lookup"><span data-stu-id="b5ad9-213">Leave Type</span></span> | <span data-ttu-id="b5ad9-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="b5ad9-214">cdm_leavetype</span></span> |
| <span data-ttu-id="b5ad9-215">İzin Türü Neden Kodu</span><span class="sxs-lookup"><span data-stu-id="b5ad9-215">Leave Type Reason Code</span></span> | <span data-ttu-id="b5ad9-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="b5ad9-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="b5ad9-217">Bordro tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-217">Payroll tables</span></span>

| <span data-ttu-id="b5ad9-218">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-218">Name</span></span> | <span data-ttu-id="b5ad9-219">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5ad9-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b5ad9-220">Ödeme Döngüsü</span><span class="sxs-lookup"><span data-stu-id="b5ad9-220">Pay Cycle</span></span> | <span data-ttu-id="b5ad9-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="b5ad9-221">cdm_paycycle</span></span> |
| <span data-ttu-id="b5ad9-222">Ödeme Dönemi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-222">Pay Period</span></span> | <span data-ttu-id="b5ad9-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="b5ad9-223">cdm_payperiod</span></span> |
| <span data-ttu-id="b5ad9-224">Bordro Kazanç Kodu</span><span class="sxs-lookup"><span data-stu-id="b5ad9-224">Payroll Earning Code</span></span> | <span data-ttu-id="b5ad9-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="b5ad9-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="b5ad9-226">Banka hesabı ödemeleri</span><span class="sxs-lookup"><span data-stu-id="b5ad9-226">Bank Account Disbursement</span></span> | <span data-ttu-id="b5ad9-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="b5ad9-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="b5ad9-228">Vergi Bölgesi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-228">Tax Region</span></span> | <span data-ttu-id="b5ad9-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="b5ad9-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="b5ad9-230">Çalışan tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-230">Worker tables</span></span>

| <span data-ttu-id="b5ad9-231">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-231">Name</span></span> | <span data-ttu-id="b5ad9-232">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5ad9-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b5ad9-233">Çalışan</span><span class="sxs-lookup"><span data-stu-id="b5ad9-233">Worker</span></span> | <span data-ttu-id="b5ad9-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="b5ad9-234">cdm_worker</span></span> |
| <span data-ttu-id="b5ad9-235">Çalışan Adresi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-235">Worker Address</span></span> | <span data-ttu-id="b5ad9-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="b5ad9-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="b5ad9-237">Çalışan Kişisel Bilgisi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-237">Worker Personal Detail</span></span> | <span data-ttu-id="b5ad9-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="b5ad9-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="b5ad9-239">Çalışan Kişi Tanımlama Numarası</span><span class="sxs-lookup"><span data-stu-id="b5ad9-239">Worker Person Identification Number</span></span> | <span data-ttu-id="b5ad9-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="b5ad9-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="b5ad9-241">Çalışan Kişi Tanımlama Türü</span><span class="sxs-lookup"><span data-stu-id="b5ad9-241">Worker Person Identification Type</span></span> | <span data-ttu-id="b5ad9-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="b5ad9-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="b5ad9-243">İş Takvimi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-243">Work Calendar</span></span> | <span data-ttu-id="b5ad9-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="b5ad9-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="b5ad9-245">İş Takvimi Gün</span><span class="sxs-lookup"><span data-stu-id="b5ad9-245">Work Calendar Day</span></span> | <span data-ttu-id="b5ad9-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="b5ad9-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="b5ad9-247">İş Takvimi Tatili</span><span class="sxs-lookup"><span data-stu-id="b5ad9-247">Work Calendar Holiday</span></span> |<span data-ttu-id="b5ad9-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="b5ad9-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="b5ad9-249">Çalışma takvimi tatil satırı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="b5ad9-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="b5ad9-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="b5ad9-251">Çalışma Takvimi Zaman Aralığı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="b5ad9-252">cdm_workcalendartimeinterval (özel alan desteği için etkinleştirilmedi)</span><span class="sxs-lookup"><span data-stu-id="b5ad9-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="b5ad9-253">Çalışan Banka Hesabı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-253">Worker Bank Account</span></span> | <span data-ttu-id="b5ad9-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="b5ad9-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="b5ad9-255">Çalışan kurulum tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-255">Worker setup tables</span></span>

| <span data-ttu-id="b5ad9-256">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-256">Name</span></span> | <span data-ttu-id="b5ad9-257">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5ad9-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b5ad9-258">Gazilik Durumu</span><span class="sxs-lookup"><span data-stu-id="b5ad9-258">Veteran Status</span></span> | <span data-ttu-id="b5ad9-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="b5ad9-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="b5ad9-260">Etnik Köken</span><span class="sxs-lookup"><span data-stu-id="b5ad9-260">Ethnic Origin</span></span> | <span data-ttu-id="b5ad9-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="b5ad9-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="b5ad9-262">Neden Kodu</span><span class="sxs-lookup"><span data-stu-id="b5ad9-262">Reason Code</span></span> | <span data-ttu-id="b5ad9-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="b5ad9-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="b5ad9-264">Kişi Kimliğini Düzenleyen Kurum</span><span class="sxs-lookup"><span data-stu-id="b5ad9-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="b5ad9-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="b5ad9-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="b5ad9-266">Yetkinlik tabloları</span><span class="sxs-lookup"><span data-stu-id="b5ad9-266">Competency tables</span></span>

| <span data-ttu-id="b5ad9-267">Kuruluş adı</span><span class="sxs-lookup"><span data-stu-id="b5ad9-267">Name</span></span> | <span data-ttu-id="b5ad9-268">Tablo</span><span class="sxs-lookup"><span data-stu-id="b5ad9-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b5ad9-269">Yetenek Türü</span><span class="sxs-lookup"><span data-stu-id="b5ad9-269">Skill Type</span></span> | <span data-ttu-id="b5ad9-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="b5ad9-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="b5ad9-271">Tablo ilişkisi modelleri</span><span class="sxs-lookup"><span data-stu-id="b5ad9-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="b5ad9-272">Çalışan</span><span class="sxs-lookup"><span data-stu-id="b5ad9-272">Worker</span></span>

![Çalışan](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="b5ad9-274">İş ve Iş pozisyonu</span><span class="sxs-lookup"><span data-stu-id="b5ad9-274">Job and Job Position</span></span>

![İş ve Iş pozisyonu](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="b5ad9-276">Kazançlar</span><span class="sxs-lookup"><span data-stu-id="b5ad9-276">Benefits</span></span>

![Kazançlar](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="b5ad9-278">Ücret</span><span class="sxs-lookup"><span data-stu-id="b5ad9-278">Compensation</span></span>

![Ücret](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="b5ad9-280">Bırak</span><span class="sxs-lookup"><span data-stu-id="b5ad9-280">Leave</span></span>

![Bırak](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="b5ad9-282">İş Takvimi</span><span class="sxs-lookup"><span data-stu-id="b5ad9-282">Work Calendar</span></span>

![İş Takvimi](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="b5ad9-284">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="b5ad9-284">See also</span></span>

[<span data-ttu-id="b5ad9-285">Veri tümleştirme teknolojisi seçme</span><span class="sxs-lookup"><span data-stu-id="b5ad9-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="b5ad9-286">Dataverse tümleştirmesini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b5ad9-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="b5ad9-287">Dataverse sanal tablolarını yapılandırma</span><span class="sxs-lookup"><span data-stu-id="b5ad9-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="b5ad9-288">Human Resources sanal tablolarıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="b5ad9-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="b5ad9-289">Microsoft Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="b5ad9-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="b5ad9-290">Terminoloji güncelleştirmeleri</span><span class="sxs-lookup"><span data-stu-id="b5ad9-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
