---
title: Servise almayla ilgili SSS
description: Bu konu, bir Dynamics 365 Human Resources uygulama projesiyle uygulamaya geçme ile ilgili sık sorulan soruları listeler.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
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
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cbf00f7428c9b1852a5bf54fd7e30a3bddc1a31e
ms.sourcegitcommit: 0e60df840688932795b9c8f8fd45d98f5ab6ba8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2020
ms.locfileid: "4668957"
---
# <a name="go-live-faq"></a><span data-ttu-id="bb28f-103">Servise almayla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="bb28f-103">Go-live FAQ</span></span> 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bb28f-104">Bu konu, bir Dynamics 365 Human Resources uygulama projesiyle uygulamaya geçme ile ilgili sık sorulan soruları listeler.</span><span class="sxs-lookup"><span data-stu-id="bb28f-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="bb28f-105">Üretim ortamımı ne zaman konfigüre edebilir ve isteyebilirim?</span><span class="sxs-lookup"><span data-stu-id="bb28f-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="bb28f-106">Tipik olarak, üretim ortamı aşağıdaki ölçütler karşılandıktan sonra dağıtılır:</span><span class="sxs-lookup"><span data-stu-id="bb28f-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="bb28f-107">Tüm özelleştirmelerin kodları tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bb28f-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="bb28f-108">Kullanıcı kabul sınamaları (UAT) tamamlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="bb28f-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="bb28f-109">Müşteri, çözümü onaylamıştır.</span><span class="sxs-lookup"><span data-stu-id="bb28f-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="bb28f-110">Uygulamaya geçmeyi engelleyici bir sorun yoktur.</span><span class="sxs-lookup"><span data-stu-id="bb28f-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="bb28f-111">Uygun müşteriler bu aşamada olduğunda, Microsoft FastTrack ekibi, proje ekibiyle birlikte bir uygulamaya geçme değerlendirmesi yapacaktır.</span><span class="sxs-lookup"><span data-stu-id="bb28f-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="bb28f-112">Üretim ortamını dağıtma önkoşulları nelerdir?</span><span class="sxs-lookup"><span data-stu-id="bb28f-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="bb28f-113">Önkoşulların listesi için, bkz  [Uygulamaya geçmeye hazırlık](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="bb28f-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="bb28f-114">Uygulamaya geçme değerlendirmesi nedir?</span><span class="sxs-lookup"><span data-stu-id="bb28f-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="bb28f-115">Uygulamaya geçme değerlendirmesi,  [Microsoft FastTrack programının](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview) bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="bb28f-115">The go-live assessment is part of the [Microsoft FastTrack program](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview).</span></span> <span data-ttu-id="bb28f-116">Bu İnceleme sırasında, bir çözüm mimarı uygulama projesinin başarılı bir kesin bitiş ve uygulamaya geçme için hazır olup olmadığını değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="bb28f-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="bb28f-117">Üretim ortamında uygulamaya geçmeyi isteyebilmeniz için, bu inceleme her uygulama projesi için zorunludur.</span><span class="sxs-lookup"><span data-stu-id="bb28f-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="bb28f-118">Korumalı alan ortamlarımız Orta ABD veri merkezinde dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="bb28f-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="bb28f-119">Üretim ortamlarımızın Batı ABD veri merkezi'nde dağıtılmasını istiyoruz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="bb28f-120">Üretim konfigürasyonumda veri merkezi olarak Batı ABD'yi seçebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="bb28f-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="bb28f-121">LCS, İnsan Kaynakları ortamı dağıttığınızda farklı bir veri merkezi seçmenizi engellemez, ancak farklı bir veri merkezini seçmemenizi önemle öneririz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="bb28f-122">Üretim ortamınızın Batı ABD veri merkezinde olmasını istiyorsanız, önce korumalı alan ortamlarınızı Batı ABD veri merkezine yeniden dağıtmanız, test etmeniz ve onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb28f-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="bb28f-123">Doğru veri merkezini seçme hakkında bilgi için bkz. [ağ gereksinimleri](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="bb28f-123">For information about selecting the correct datacenter, see [Network requirements](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="bb28f-124">İnsan Kaynakları ortamlarım için Azure kaynaklarına hangi düzeyde erişime sahibim?</span><span class="sxs-lookup"><span data-stu-id="bb28f-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="bb28f-125">İnsan Kaynakları ortamlara erişim sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="bb28f-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="bb28f-126">Sanal makineye (VM) veya Microsoft Internet Information Services'a (IIS) erişemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="bb28f-127">Ayrıca, veritabanına Microsoft SQL Server Management Studio üzerinden erişemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="bb28f-128">Azure kaynaklarınıza veya Dynamics 365 Human Resources ortamınıza doğrudan erişemeseniz de verilerinize erişmek için kullanabileceğiniz ek özellikler vardır:</span><span class="sxs-lookup"><span data-stu-id="bb28f-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="bb28f-129">Azure SQL veritabanını kendi Azure kiracınıza dağıtabilir ve verileri eşitlemek için kendi veritabanınızı getirin (BYOD) özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="bb28f-130">Daha fazla bilgi için bkz. [Kendi veritabanınızı getirme (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="bb28f-130">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span>

- <span data-ttu-id="bb28f-131">Belirli varlıkları Common Data Service veritabanıyla senkronize etmek için Common Data Service tümleştirmesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-131">You can use Common Data Service integration to synchronize select entities into the Common Data Service database.</span></span> <span data-ttu-id="bb28f-132">Daha fazla bilgi için bkz. [Common Data Service varlıkları](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="bb28f-132">For more information, see [Common Data Service entities](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="bb28f-133">Üretim veritabanı ne sıklıkta yedeklenir?</span><span class="sxs-lookup"><span data-stu-id="bb28f-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="bb28f-134">Veritabanları otomatik yedeklemeler tarafından aşağıdaki sıklıklarda korunur:</span><span class="sxs-lookup"><span data-stu-id="bb28f-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="bb28f-135">Yedekleme türü</span><span class="sxs-lookup"><span data-stu-id="bb28f-135">Type of backup</span></span> | <span data-ttu-id="bb28f-136">Sıklık</span><span class="sxs-lookup"><span data-stu-id="bb28f-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="bb28f-137">Tam veritabanı yedekleme</span><span class="sxs-lookup"><span data-stu-id="bb28f-137">Full database backup</span></span> | <span data-ttu-id="bb28f-138">Weekly</span><span class="sxs-lookup"><span data-stu-id="bb28f-138">Weekly</span></span> |
| <span data-ttu-id="bb28f-139">Farklı veritabanı yedekleme</span><span class="sxs-lookup"><span data-stu-id="bb28f-139">Differential database backup</span></span> | <span data-ttu-id="bb28f-140">Her 12-24 saatte bir</span><span class="sxs-lookup"><span data-stu-id="bb28f-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="bb28f-141">İşlem günlüğü yedeklemesi</span><span class="sxs-lookup"><span data-stu-id="bb28f-141">Transaction log backup</span></span> | <span data-ttu-id="bb28f-142">Her 5-10 dakikada bir</span><span class="sxs-lookup"><span data-stu-id="bb28f-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="bb28f-143">Microsoft, son 14 gün içinde belirli bir noktaya geri yüklemeye (PITR) izin vermek için yeterli yedeği saklar.</span><span class="sxs-lookup"><span data-stu-id="bb28f-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="bb28f-144">Daha fazla bilgi için bkz.  [Otomatik SQL Veritabanı yedeklemeleri hakkında daha fazla bilgi alın](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="bb28f-144">For more information, see [Learn about automatic SQL Database backups](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="bb28f-145">Üretim veritabanımın yedeğinin bir kopyasını isteyebilir miyim?</span><span class="sxs-lookup"><span data-stu-id="bb28f-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="bb28f-146">Hayır.</span><span class="sxs-lookup"><span data-stu-id="bb28f-146">No.</span></span> <span data-ttu-id="bb28f-147">Ancak üretim ortamınızı korumalı alan ortamınıza kopyalamak için veritabanı yenileme hizmeti isteği gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="bb28f-148">Azure SQL veritabanını kendi Azure kiracınıza dağıtabilir ve üretim ortamınızdan verileri eşitlemek için BYOD özelliğini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="bb28f-149">Daha fazla bilgi için bkz. [Kendi veritabanınızı getirme (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span><span class="sxs-lookup"><span data-stu-id="bb28f-149">For more information, see [Bring your own database (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="bb28f-150">Korumalı alan ortamımı uygulamaya geçirmek üzere üretime nasıl taşıyabilirim?</span><span class="sxs-lookup"><span data-stu-id="bb28f-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="bb28f-151">Ortamınızı bir korumalı alan ortamından üretim ortamına taşımak için kullanılabilecek bir kopya özelliği olmadığından, verileri üretim ortamınıza taşımak için veri paketlerini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb28f-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="bb28f-152">Proje boyunca korumalı alanda yapılandırılmış varlıkların açık bir listesini tutmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="bb28f-153">Daha sonra, uygulamaya geçirme işleminiz için gereken tüm veri paketlerinin kesin bitiş ve geçiş işlemlerini sınayın.</span><span class="sxs-lookup"><span data-stu-id="bb28f-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="bb28f-154">Uygulamaya geçmeye hazır olduğunuzda, tüm veri paketlerini üretim ortamına el ile taşımanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb28f-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="bb28f-155">Üretim ortamım arızalıyla ne yapmam gerekir?</span><span class="sxs-lookup"><span data-stu-id="bb28f-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="bb28f-156">Üretim kesintisi bildirmek için,  [üretim kesintisi bildir](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage) bölümünde açıklanan süreci izleyin.</span><span class="sxs-lookup"><span data-stu-id="bb28f-156">To report a Production outage, follow the process described in [Report a production outage](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="bb28f-157">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="bb28f-157">See also</span></span>

 [<span data-ttu-id="bb28f-158">Servise almak için hazırlama</span><span class="sxs-lookup"><span data-stu-id="bb28f-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)
