---
title: Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (Haziran 11 2020)
description: Bu konuda, 11 Haziran 2020 için Microsoft Dynamics 365 Human Resources'taki yeni veya değişen özellikler açıklanmaktadır.
author: andreabichsel
manager: tfehr
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8e5fa842739bbc0070f892c7f19e84ac6ac0ceb
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463658"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="94eaa-103">Dynamics 365 Human Resources'taki yenilikler veya değişiklikler (Haziran 11 2020)</span><span class="sxs-lookup"><span data-stu-id="94eaa-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="94eaa-104">Bu makalede Dynamics 365 Human Resources'te yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="94eaa-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="94eaa-105">Değişiklikler derleme numarası 8.1.3316 uygulanır.</span><span class="sxs-lookup"><span data-stu-id="94eaa-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="94eaa-106">Bazı başlıklardaki parantez içindeki numaralar referans için LCS destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="94eaa-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="94eaa-107">Kolaylaştırılmış çalışan formu bazen alt formu kapatma (X) düğmelerinin çalışmayı durdurmasına neden oluyor (442369)</span><span class="sxs-lookup"><span data-stu-id="94eaa-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="94eaa-108">Yeni **Çalışan** formu etkinleştirildiğinde, alt formlardaki kapat (**X**) düğmesi bazen çalışmıyordu.</span><span class="sxs-lookup"><span data-stu-id="94eaa-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="94eaa-109">Bu aralıklı görülen bir sorundu.</span><span class="sxs-lookup"><span data-stu-id="94eaa-109">This problem was intermittent.</span></span> <span data-ttu-id="94eaa-110">Ayrılıp geri döndüğünüzde formu kapatabiliyordunuz.</span><span class="sxs-lookup"><span data-stu-id="94eaa-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="94eaa-111">Örneğin, sol taraftaki bir menü öğesini seçip **Çalışan** formuna geri döndüğünüzde formu kapatabiliyordunuz.</span><span class="sxs-lookup"><span data-stu-id="94eaa-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="94eaa-112">Bu haftanın sürümüyle bu sorunu düzeltildi.</span><span class="sxs-lookup"><span data-stu-id="94eaa-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="94eaa-113">Çalışan kişisel ilgili kişi varlığı, kişisel ilgili kişileri üst ilişki türüyle birlikte dışarı aktarmıyor</span><span class="sxs-lookup"><span data-stu-id="94eaa-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="94eaa-114">Bu sürümde, **Çalışan kişisel ilgili kişi** varlığı tüm ilişki türlerini dışa aktarıyor.</span><span class="sxs-lookup"><span data-stu-id="94eaa-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="94eaa-115">HcmPositionWorkerAssignmentV2Entity, varsayılan olarak Ceridian bordro tümleştirme paketinin parçası olmalıdır (448506)</span><span class="sxs-lookup"><span data-stu-id="94eaa-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="94eaa-116">Bu değişiklikle, **HcmPositionWorkerAssignmentV2Entity** Ceridian Bordro tümleştirme paketine dahil edildi.</span><span class="sxs-lookup"><span data-stu-id="94eaa-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="94eaa-117">Ön izlemede</span><span class="sxs-lookup"><span data-stu-id="94eaa-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="94eaa-118">Veritabanı günlüklerine kaydetme</span><span class="sxs-lookup"><span data-stu-id="94eaa-118">Database logging</span></span>

<span data-ttu-id="94eaa-119">Veritabanı günlükleri özelliği hangi tablo ve alanların izleneceğini belirlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="94eaa-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="94eaa-120">Ayrıca değişiklik izlemeyi tetiklemesi gereken olayları belirlemenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="94eaa-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="94eaa-121">Zaman içinde yapılan bu değişiklikleri görmek için veritabanı günlüğü kaydetme yeteneklerini kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="94eaa-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="94eaa-122">Daha fazla bilgi için, bkz. [Veri tabanı günlüğü kaydetme işlemini yapılandırma ve yönetme](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="94eaa-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="94eaa-123">Teams'de Human Resources uygulaması</span><span class="sxs-lookup"><span data-stu-id="94eaa-123">Human Resources application in Teams</span></span>

<span data-ttu-id="94eaa-124">Çalışanlar, Microsoft Teams içinde işten geçen zamanı görüntüleyebilir ve talep edebilir .</span><span class="sxs-lookup"><span data-stu-id="94eaa-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="94eaa-125">İzin istekleri oluşturmak için bir bot ile etkileşime girebilirler.</span><span class="sxs-lookup"><span data-stu-id="94eaa-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="94eaa-126">Daha fazla bilgi için bkz: [Teams'te insan kaynakları uygulama](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="94eaa-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="94eaa-127">Sosyal haklar yönetimi için veri yönetimi çerçevesi (DMF) varlıkları</span><span class="sxs-lookup"><span data-stu-id="94eaa-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="94eaa-128">Kazançlar yönetimi varlıkları serbest bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="94eaa-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="94eaa-129">DMF varlıkları, kazanç yönetimini kolayca yapılandırmak için verilerin içe ve dışa aktarılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="94eaa-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="94eaa-130">Verileri taşımak için bir Kazanç yönetimi şablonu kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="94eaa-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="94eaa-131">Şablon veri bağımlılıklarını dikkate almak için verileri dışa aktarır ve sıralı şekilde içe aktarır.</span><span class="sxs-lookup"><span data-stu-id="94eaa-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="94eaa-132">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="94eaa-132">Buy and sell leave</span></span> 

<span data-ttu-id="94eaa-133">Bazı kuruluşlar, çalışanların izin satın alma veya satma olanağı sağlayan bir yarar sağlar.</span><span class="sxs-lookup"><span data-stu-id="94eaa-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="94eaa-134">Bu işlem genellikle el ile yönetilir.</span><span class="sxs-lookup"><span data-stu-id="94eaa-134">This process is often managed manually.</span></span> <span data-ttu-id="94eaa-135">Bu özellik, İK departmanı ile ilgili ilkelerin ve isteklerin yönetilmesini otomatikleştirir.</span><span class="sxs-lookup"><span data-stu-id="94eaa-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="94eaa-136">İzin yönetimi işlemini kolaylaştırır ve hataları gidermek için yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="94eaa-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="94eaa-137">Daha fazla bilgi için bkz:</span><span class="sxs-lookup"><span data-stu-id="94eaa-137">For more information, see:</span></span>

- [<span data-ttu-id="94eaa-138">İzin satın alma ve satma ilkelerini yönetme</span><span class="sxs-lookup"><span data-stu-id="94eaa-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="94eaa-139">İzin satın alma ve satma</span><span class="sxs-lookup"><span data-stu-id="94eaa-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="94eaa-140">Tek bir şirket veya tek bir plan için izin tahakkuku</span><span class="sxs-lookup"><span data-stu-id="94eaa-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="94eaa-141">Müşteriler tek bir şirket veya tek bir izin ve devamsızlık planı için tahakkukları işleyebilir.</span><span class="sxs-lookup"><span data-stu-id="94eaa-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="94eaa-142">Bu özellik, farklı izin yılı veya izin tahakkuk ilkeleri olan müşteriler için tahakkuk işlemine açıklık sağlar.</span><span class="sxs-lookup"><span data-stu-id="94eaa-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="94eaa-143">Daha fazla bilgi için bkz. [Şirket veya izin planı başına izin tahakkuku](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="94eaa-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="94eaa-144">İzin isteklerine ekler ekleme</span><span class="sxs-lookup"><span data-stu-id="94eaa-144">Add attachments to time off requests</span></span>

<span data-ttu-id="94eaa-145">Onaylanmış izin isteklerine ek ekleme yeteneği, geçerli COVID-19 ortamında kritik öneme sahip.</span><span class="sxs-lookup"><span data-stu-id="94eaa-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="94eaa-146">Çalışanlar şimdi bu ekleri ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="94eaa-146">Employees can now add these attachments.</span></span> <span data-ttu-id="94eaa-147">Ayrıca, izin isteklerinde güncelleştirmelerin nasıl yapıldığıyla ilgili daha fazla öngörüye shaip olabilirler.</span><span class="sxs-lookup"><span data-stu-id="94eaa-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="94eaa-148">Daha fazla bilgi için, bkz. [Mevcut bir isteğe ek ekleme](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="94eaa-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="94eaa-149">Tahakkuk askıya almalara neden kodu ekleme</span><span class="sxs-lookup"><span data-stu-id="94eaa-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="94eaa-150">Neden kodları tahakkuk askıya almaya eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="94eaa-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="94eaa-151">Devretme kuralları</span><span class="sxs-lookup"><span data-stu-id="94eaa-151">Carry forward rules</span></span> 

<span data-ttu-id="94eaa-152">Örneğin, devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94eaa-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="94eaa-153">Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94eaa-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="94eaa-154">Daha fazla bilgi için bkz. [İzin ve devamsızlık türleri yapılandırma](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="94eaa-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="94eaa-155">Belirtilen izin türleri için izin tahakkunu askıya alma</span><span class="sxs-lookup"><span data-stu-id="94eaa-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="94eaa-156">Ücretsiz izin için girilen izin istekleri bulunan çalışanlar için izin tahakkuklarını askıya alma kuralı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94eaa-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="94eaa-157">Ücretsiz izin bir tür olabilir, ancak böyle olması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="94eaa-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="94eaa-158">Başka bir izin türünü temel alarak herhangi bir izni askıya alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94eaa-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="94eaa-159">Tahakkuk askıya almaları için DMF varlığı kullanılabilir</span><span class="sxs-lookup"><span data-stu-id="94eaa-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="94eaa-160">DMF varlığı artık tahakkuk askıya almalar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="94eaa-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="94eaa-161">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="94eaa-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="94eaa-162">Yeni platform yetenekleri</span><span class="sxs-lookup"><span data-stu-id="94eaa-162">New platform capabilities</span></span> 

<span data-ttu-id="94eaa-163">Kişiselleştirmeyi kullanarak alanları zorunlu hale getirebileceksiniz.</span><span class="sxs-lookup"><span data-stu-id="94eaa-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="94eaa-164">Bu özellik, **Kaydedilmiş görünümleri** etkinleştirmenizi gerektirir.</span><span class="sxs-lookup"><span data-stu-id="94eaa-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="94eaa-165">Personel self servisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="94eaa-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="94eaa-166">Personel self servis çalışma alanının adını Self servis olarak güncelleştirmek için Human Resources parametrelerinde yeni bir seçenek kullanılabilir olacaktır.</span><span class="sxs-lookup"><span data-stu-id="94eaa-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="94eaa-167">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="94eaa-167">See also</span></span>

[<span data-ttu-id="94eaa-168">Human Resources'taki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="94eaa-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="94eaa-169">Dynamics 365 Human Resources 2019 sürüm 2'ye genel bakış</span><span class="sxs-lookup"><span data-stu-id="94eaa-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="94eaa-170">Güncelleştirme işlemi</span><span class="sxs-lookup"><span data-stu-id="94eaa-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="94eaa-171">Özellikleri yönetme</span><span class="sxs-lookup"><span data-stu-id="94eaa-171">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]