---
title: Başvuran İzleme Sistemi tümleştirme API'si tanıtımı
description: Bu konuda Dynamics 365 Human Resources Başvuran İzleme Sistemi (ATS) tümleştirme API'si açıklanmaktadır.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c043ac9c19a810d1718f0d4907cd5e9d651d778f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055304"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="e1190-103">Başvuran İzleme Sistemi tümleştirme API'si tanıtımı</span><span class="sxs-lookup"><span data-stu-id="e1190-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e1190-104">Bu konuda Dynamics 365 Human Resources Başvuran İzleme Sistemi (ATS) tümleştirme API'si açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e1190-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="e1190-105">API'nin amacı, Dynamics 365 Human Resources ile iş ortaklığı yapılan ATS'ler arasında kolaylaştırılmış tümleştirmeleri etkinleştirmektir.</span><span class="sxs-lookup"><span data-stu-id="e1190-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS tümleştirme akışı](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="e1190-107">Tümleştirilmiş deneyim, bir işe alma yöneticisi işe alım isteği oluşturduğunda Human Resources'da başlar.</span><span class="sxs-lookup"><span data-stu-id="e1190-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="e1190-108">İstek etkinleştirildiğinde, ATS bir işe alım projesi oluşturma isteği için ayrıntıyı çeker.</span><span class="sxs-lookup"><span data-stu-id="e1190-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="e1190-109">Ardından, pozisyonlar için bir aday seçmek ve işe almak için işe alım ardışık düzenini izler.</span><span class="sxs-lookup"><span data-stu-id="e1190-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="e1190-110">Son olarak, ATS seçilen adayın kaydını Human Resources'a göndererek iki yönlü tümleştirmeyi tamamlar.</span><span class="sxs-lookup"><span data-stu-id="e1190-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="e1190-111">Aday kaydı daha sonra çalışan kaydını oluşturmak için daha fazla ekleme doğrulaması ve iş akışından geçebilir.</span><span class="sxs-lookup"><span data-stu-id="e1190-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="e1190-112">Tümleştirmeyi etkinleştirmek için Human Resources aşağıdaki bileşenleri ekledi:</span><span class="sxs-lookup"><span data-stu-id="e1190-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="e1190-113">İşe alma isteği oluşturma işlevi.</span><span class="sxs-lookup"><span data-stu-id="e1190-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="e1190-114">Genişletilmiş aday profili ve ilgili iş akışları.</span><span class="sxs-lookup"><span data-stu-id="e1190-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="e1190-115">Uygulamaları tümleştirmeye yeni işlevselliği açan bir tümleştirme API'si.</span><span class="sxs-lookup"><span data-stu-id="e1190-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="e1190-116">İşe alma isteğini ve aday işlevselliğini ayarlama ve kullanma hakkında daha fazla bilgi için bkz. [İş adaylarını işe alma](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="e1190-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="e1190-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="e1190-117">Microsoft Dataverse</span></span>

<span data-ttu-id="e1190-118">Bu API, Microsoft Dataverse (eski adıyla Common Data Service) üzerine kuruludur.</span><span class="sxs-lookup"><span data-stu-id="e1190-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="e1190-119">Bu API ile tüm RESTful etkileşimi, OData kullanan Microsoft Dataverse Web API'si üzerinden yapılır.</span><span class="sxs-lookup"><span data-stu-id="e1190-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="e1190-120">Bu API, Dataverse Web API'sinin bir alt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="e1190-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="e1190-121">Dataverse Web API'si; kimlik doğrulama, SLA'lar, toplu iş, eşzamanlılık denetimi ve hata işleme gibi özellikleri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e1190-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="e1190-122">Microsoft Dataverse Web API'si hakkında daha fazla genel bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="e1190-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="e1190-123">Microsoft Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="e1190-123">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="e1190-124">Microsoft Dataverse Web API'sini kullanma</span><span class="sxs-lookup"><span data-stu-id="e1190-124">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="e1190-125">Microsoft Dataverse geliştirici kılavuzu</span><span class="sxs-lookup"><span data-stu-id="e1190-125">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="e1190-126">Yukarıdaki belgeler, [kimlik doğrulamayı yönetme](/powerapps/developer/data-platform/webapi/authenticate-web-api), [işlemleri gerçekleştirme](/powerapps/developer/data-platform/webapi/perform-operations-web-api) , [API ile Postman'i kullanma](/powerapps/developer/data-platform/webapi/use-postman-web-api) ve API ile [değişiklik izleme veya delta belirteçlerini kullanma](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) gibi Dataverse Web API'sini kullanma hakkında ayrıntılar ve geliştirici kılavuzu içerir.</span><span class="sxs-lookup"><span data-stu-id="e1190-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="e1190-127">Seçenek kümeleri</span><span class="sxs-lookup"><span data-stu-id="e1190-127">Option sets</span></span>

<span data-ttu-id="e1190-128">Bu belgede açıklanan ATS tümleştirme API'sinin veri modeli, varlık özellikleriyle ilişkili numaralandırılmış değerler sağlayan seçenek kümelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="e1190-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="e1190-129">Dataverse Web API'sinde seçenek kümeleriyle çalışma hakkında ayrıntılı bilgi için bkz. [Web API'sini kullanarak seçenek kümeleri oluşturma ve güncelleştirme](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="e1190-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="e1190-130">Seçenek kümeleri her Dataverse ortamı için tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="e1190-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="e1190-131">Dataverse'te Human Resources için sanal tablolar</span><span class="sxs-lookup"><span data-stu-id="e1190-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="e1190-132">ATS tümleştirme API'sinin uç noktaları , Microsoft Dataverse'ün sanal tablo platformu yeteneklerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e1190-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="e1190-133">Varsayılan olarak, sanal tablolar ve ilişkili API uç noktaları Human Resources ortamları için dağıtılmamıştır ve kuruluşların ortam için hangi OData uç noktalarının kullanıma sunulacağını belirlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e1190-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="e1190-134">API'yi kullanmak istiyorsanız ortam için Human Resources varlıklarına yönelik sanal tablolar oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e1190-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="e1190-135">API'ye yönelik sanal tablolar oluşturma hakkında bilgi için bkz. [Dataverse sanal tablolarını yapılandırma](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="e1190-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="e1190-136">Veri modeli</span><span class="sxs-lookup"><span data-stu-id="e1190-136">Data model</span></span>

<span data-ttu-id="e1190-137">Veri modeli iki ana varlığa odaklanır:</span><span class="sxs-lookup"><span data-stu-id="e1190-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="e1190-138">**RecruitingRequest,** bir ATS'ye bir veya daha fazla açık pozisyon için gönderilen işe alma isteğini temsil eder. Örnek bir sorgu için bkz. [İşe alma isteği için sorgu örneği](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="e1190-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="e1190-139">**CandidateToHire**, bir pozisyon için teklifi kabul eden bir adayın ayrıntılarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="e1190-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="e1190-140">**Kişi**, aday olan kişiyi temsil eder.</span><span class="sxs-lookup"><span data-stu-id="e1190-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="e1190-141">Bir kişinin şirkette aday, işçi, çalışan veya yüklenici gibi birden fazla rolü alabilir.</span><span class="sxs-lookup"><span data-stu-id="e1190-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="e1190-142">Örnek bir sorgu için, bkz. [İşe alınacak aday için sorgu örneği](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="e1190-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="e1190-143">Aşağıdaki diyagramda API içindeki ilişkiler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e1190-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="e1190-144">Çeşitli türlerin, Human Resources'da önceden var olan ve burada belirtilmeyen diğer varlıkların yabancı anahtarları vardır.</span><span class="sxs-lookup"><span data-stu-id="e1190-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="e1190-145">Bu belge, işe alma tümleştirme senaryolarına özgü varlıklar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e1190-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="e1190-146">Ancak Dynamics 365 Human Resources için Dataverse Web API'sinde tümleştirmenizle de ilgili olabilecek birçok başka varlık vardır.</span><span class="sxs-lookup"><span data-stu-id="e1190-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="e1190-147">Örneğin, burada tanımlanmayan çalışanlar, işler, pozisyonlar veya diğer varlıklar için de ayrıntıya ihtiyacınız olabilir.</span><span class="sxs-lookup"><span data-stu-id="e1190-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="e1190-148">Bu varlıkların çoğuna yabancı anahtar ilişkilerinde veya gezinti özelliklerinde referans verilir.</span><span class="sxs-lookup"><span data-stu-id="e1190-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS Tümleştirme API'si veri modeli](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="e1190-150">İşe alma isteği ve ilgili varlıklar ve seçenek kümeleri</span><span class="sxs-lookup"><span data-stu-id="e1190-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="e1190-151">Örnek sorgu:</span><span class="sxs-lookup"><span data-stu-id="e1190-151">Example query:</span></span> 

- [<span data-ttu-id="e1190-152">Işe alma isteği için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="e1190-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="e1190-153">Varlıklar:</span><span class="sxs-lookup"><span data-stu-id="e1190-153">Entities:</span></span>

- [<span data-ttu-id="e1190-154">İşe alma isteği</span><span class="sxs-lookup"><span data-stu-id="e1190-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="e1190-155">İşe alma isteği pozisyonu</span><span class="sxs-lookup"><span data-stu-id="e1190-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="e1190-156">İşe alma isteği becerisi</span><span class="sxs-lookup"><span data-stu-id="e1190-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="e1190-157">İşe alma isteği eğitimi</span><span class="sxs-lookup"><span data-stu-id="e1190-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="e1190-158">İşe alma isteği konumu</span><span class="sxs-lookup"><span data-stu-id="e1190-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="e1190-159">Seçenek kümeleri:</span><span class="sxs-lookup"><span data-stu-id="e1190-159">Option sets:</span></span>

- [<span data-ttu-id="e1190-160">İş muafiyet durumu</span><span class="sxs-lookup"><span data-stu-id="e1190-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="e1190-161">İşe alma isteği pozisyon durumu</span><span class="sxs-lookup"><span data-stu-id="e1190-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="e1190-162">İşe alma isteği durumu</span><span class="sxs-lookup"><span data-stu-id="e1190-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="e1190-163">Mevzuat iş kategorisi</span><span class="sxs-lookup"><span data-stu-id="e1190-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="e1190-164">İşe alınacak aday ve ilgili varlıklar ve seçenek kümeleri</span><span class="sxs-lookup"><span data-stu-id="e1190-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="e1190-165">Örnek sorgu:</span><span class="sxs-lookup"><span data-stu-id="e1190-165">Example query:</span></span>

- [<span data-ttu-id="e1190-166">İşe alınacak aday için sorgu örneği</span><span class="sxs-lookup"><span data-stu-id="e1190-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="e1190-167">Varlıklar:</span><span class="sxs-lookup"><span data-stu-id="e1190-167">Entities:</span></span>

- [<span data-ttu-id="e1190-168">İşe alınacak aday</span><span class="sxs-lookup"><span data-stu-id="e1190-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="e1190-169">Kişi</span><span class="sxs-lookup"><span data-stu-id="e1190-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="e1190-170">Kişi eğitimi</span><span class="sxs-lookup"><span data-stu-id="e1190-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="e1190-171">Kişi profesyonel deneyimi</span><span class="sxs-lookup"><span data-stu-id="e1190-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="e1190-172">Kişi adresi</span><span class="sxs-lookup"><span data-stu-id="e1190-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="e1190-173">Taraf ilgili kişisi</span><span class="sxs-lookup"><span data-stu-id="e1190-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="e1190-174">Kişi yeteneği</span><span class="sxs-lookup"><span data-stu-id="e1190-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="e1190-175">Değerlendirme düzeyi</span><span class="sxs-lookup"><span data-stu-id="e1190-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="e1190-176">Kişi sertifikası</span><span class="sxs-lookup"><span data-stu-id="e1190-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="e1190-177">Sertifika türü</span><span class="sxs-lookup"><span data-stu-id="e1190-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="e1190-178">Kişi filtreleme</span><span class="sxs-lookup"><span data-stu-id="e1190-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="e1190-179">Filtreleme türleri</span><span class="sxs-lookup"><span data-stu-id="e1190-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="e1190-180">Kişi kimlik numarası</span><span class="sxs-lookup"><span data-stu-id="e1190-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="e1190-181">Seçenek kümeleri:</span><span class="sxs-lookup"><span data-stu-id="e1190-181">Option sets:</span></span>

- [<span data-ttu-id="e1190-182">Başvuran tümleştirmesi sonucu</span><span class="sxs-lookup"><span data-stu-id="e1190-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="e1190-183">Boş Evet Hayır</span><span class="sxs-lookup"><span data-stu-id="e1190-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="e1190-184">Tamamlanma durumu</span><span class="sxs-lookup"><span data-stu-id="e1190-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="e1190-185">İlgili kişi türü</span><span class="sxs-lookup"><span data-stu-id="e1190-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="e1190-186">Eğitim kredisi esası</span><span class="sxs-lookup"><span data-stu-id="e1190-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="e1190-187">Cinsiyet</span><span class="sxs-lookup"><span data-stu-id="e1190-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="e1190-188">Medeni durum</span><span class="sxs-lookup"><span data-stu-id="e1190-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="e1190-189">Yılın ayları</span><span class="sxs-lookup"><span data-stu-id="e1190-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="e1190-190">Hayır Evet</span><span class="sxs-lookup"><span data-stu-id="e1190-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="e1190-191">Dönem birimi</span><span class="sxs-lookup"><span data-stu-id="e1190-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="e1190-192">Filtreleme sıklığı</span><span class="sxs-lookup"><span data-stu-id="e1190-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="e1190-193">Filtreleme sıklığı oluşturma kaynağı</span><span class="sxs-lookup"><span data-stu-id="e1190-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="e1190-194">Yetenek düzeyi türü</span><span class="sxs-lookup"><span data-stu-id="e1190-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="e1190-195">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="e1190-195">See also</span></span>

[<span data-ttu-id="e1190-196">İş adaylarını işe alma</span><span class="sxs-lookup"><span data-stu-id="e1190-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="e1190-197">Microsoft Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="e1190-197">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="e1190-198">Microsoft Dataverse Web API'sini kullanma</span><span class="sxs-lookup"><span data-stu-id="e1190-198">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="e1190-199">Web API'sini kullanarak seçenek kümeleri oluşturma ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e1190-199">Create and update option sets using the Web API</span></span>](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]