---
title: Bordro tümleştirme API'sına giriş
description: Bu konuda, Dynamics 365 Human Resources Bordro tümleştirme API'sı açıklanmaktadır.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6d8a1cb9619a863184460a74e472af3f06934b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058572"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="315f2-103">Bordro tümleştirme API'sına giriş</span><span class="sxs-lookup"><span data-stu-id="315f2-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="315f2-104">Bu belgede, Dynamics 365 Human Resources Bordro tümleştirme API'sı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="315f2-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="315f2-105">API, Human Resources ve iş ortağı bordro sistemleri arasında uçtan uca sorunsuz tümleştirmeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="315f2-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="315f2-106">Tümleşik deneyim Human Resources'ta personel profili, maaş ve kesinti ve katkı bilgileri ile başlar.</span><span class="sxs-lookup"><span data-stu-id="315f2-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="315f2-107">Bir çalışanı işe alıp gerekli profili ve ödeme bilgilerini Human Resources'a girdiğinizde bordro sistemi, bordroyu işlerken kullanmak için bu bilgileri çeker.</span><span class="sxs-lookup"><span data-stu-id="315f2-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="315f2-108">Çalışan veya ödeme bilgilerinde yapılan tüm güncelleştirmeler de sonraki ödeme çalıştırmasında kullanılmak üzere çekilir.</span><span class="sxs-lookup"><span data-stu-id="315f2-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Bordro tümleştirme akışı](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="315f2-110">Tümleştirmeyi etkinleştirmek için Human Resources'ta aşağıdaki bileşenler bulunur:</span><span class="sxs-lookup"><span data-stu-id="315f2-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="315f2-111">Bir çalışanı ödeme için hazır olarak işaretleme işlevi</span><span class="sxs-lookup"><span data-stu-id="315f2-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="315f2-112">Uygulamaları tümleştirmeye yeni işlevsellik açan bir tümleştirme API'sı</span><span class="sxs-lookup"><span data-stu-id="315f2-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="315f2-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="315f2-113">Microsoft Dataverse</span></span>

<span data-ttu-id="315f2-114">Bu API, Microsoft Dataverse (eski adıyla Common Data Service) üzerine kuruludur.</span><span class="sxs-lookup"><span data-stu-id="315f2-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="315f2-115">Bu API ile tüm RESTful etkileşimi, OData kullanan Microsoft Dataverse Web API'si üzerinden yapılır.</span><span class="sxs-lookup"><span data-stu-id="315f2-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="315f2-116">Bu API, Dataverse Web API'sinin bir alt kümesidir.</span><span class="sxs-lookup"><span data-stu-id="315f2-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="315f2-117">Dataverse Web API'si; kimlik doğrulama, SLA'lar, toplu iş, eşzamanlılık denetimi ve hata işleme gibi özellikleri tanımlar.</span><span class="sxs-lookup"><span data-stu-id="315f2-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="315f2-118">Microsoft Dataverse Web API'si hakkında daha fazla genel bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="315f2-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="315f2-119">Microsoft Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="315f2-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="315f2-120">Microsoft Dataverse Web API'sini kullanma</span><span class="sxs-lookup"><span data-stu-id="315f2-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="315f2-121">Microsoft Dataverse geliştirici kılavuzu</span><span class="sxs-lookup"><span data-stu-id="315f2-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="315f2-122">Bu belge, aşağıdaki konular dahil olmak üzere Dataverse Web API'sını kullanmayla ilgili ayrıntıları ve geliştirici kılavuzunu içerir:</span><span class="sxs-lookup"><span data-stu-id="315f2-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="315f2-123">Web API'sı ile Microsoft Dataverse'te kimlik doğrulaması yapma</span><span class="sxs-lookup"><span data-stu-id="315f2-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="315f2-124">Web API'sını kullanarak işlem gerçekleştirme</span><span class="sxs-lookup"><span data-stu-id="315f2-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="315f2-125">Web API'sı ile Postman kullanma</span><span class="sxs-lookup"><span data-stu-id="315f2-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="315f2-126">Verileri harici sistemlerle eşitlemek için değişiklik izlemeyi kullanma</span><span class="sxs-lookup"><span data-stu-id="315f2-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="315f2-127">Dataverse'te Human Resources için sanal tablolar</span><span class="sxs-lookup"><span data-stu-id="315f2-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="315f2-128">Bordro tümleştirme API'sının uç noktaları, Microsoft Dataverse'ün sanal tablo platformu yeteneklerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="315f2-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="315f2-129">Varsayılan olarak, sanal tablolar ve ilişkili API uç noktaları Human Resources ortamları için dağıtılmamıştır ve kuruluşların ortam için hangi OData uç noktalarının kullanıma sunulacağını belirlemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="315f2-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="315f2-130">API'yi kullanmak istiyorsanız ortam için Human Resources varlıklarına yönelik sanal tablolar oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="315f2-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="315f2-131">API'ye yönelik sanal tablolar oluşturma hakkında bilgi için bkz. [Dataverse sanal tablolarını yapılandırma](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="315f2-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="315f2-132">Veri modeli</span><span class="sxs-lookup"><span data-stu-id="315f2-132">Data model</span></span>

<span data-ttu-id="315f2-133">Aşağıdaki diyagramda API içindeki ilişkiler gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="315f2-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="315f2-134">Çeşitli türlerin, Human Resources'da önceden var olan ve burada belirtilmeyen diğer varlıkların yabancı anahtarları vardır.</span><span class="sxs-lookup"><span data-stu-id="315f2-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="315f2-135">Bu belge, bordro tümleştirme senaryolarına özgü varlıklar hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="315f2-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="315f2-136">Ancak Human Resources için Dataverse Web API'sında tümleştirmenizle de ilgili olabilecek birçok başka varlık vardır.</span><span class="sxs-lookup"><span data-stu-id="315f2-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="315f2-137">Bu varlıkların bazılarına yabancı anahtar ilişkilerinde veya gezinti özelliklerinde referans verilir.</span><span class="sxs-lookup"><span data-stu-id="315f2-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Bordro Tümleştirme API'sı veri modeli](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="315f2-139">Bordrolu personel ve ilgili varlıklar</span><span class="sxs-lookup"><span data-stu-id="315f2-139">Payroll employee and related entities</span></span>

<span data-ttu-id="315f2-140">Varlıklar:</span><span class="sxs-lookup"><span data-stu-id="315f2-140">Entities:</span></span>

- [<span data-ttu-id="315f2-141">Bordrolu personel</span><span class="sxs-lookup"><span data-stu-id="315f2-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="315f2-142">Bordrolu çalışanın adresi</span><span class="sxs-lookup"><span data-stu-id="315f2-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="315f2-143">Bordro sabit ücret planı</span><span class="sxs-lookup"><span data-stu-id="315f2-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="315f2-144">Bordrolu pozisyon işi</span><span class="sxs-lookup"><span data-stu-id="315f2-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="315f2-145">Bordrolu pozisyon</span><span class="sxs-lookup"><span data-stu-id="315f2-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="315f2-146">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="315f2-146">See also</span></span>

[<span data-ttu-id="315f2-147">Bordro varlıkları oluşturma ve gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="315f2-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="315f2-148">Human Resources parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="315f2-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="315f2-149">Human Resources paylaşılan parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="315f2-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="315f2-150">Microsoft Dataverse nedir?</span><span class="sxs-lookup"><span data-stu-id="315f2-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="315f2-151">Microsoft Dataverse Web API'sini kullanma</span><span class="sxs-lookup"><span data-stu-id="315f2-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]