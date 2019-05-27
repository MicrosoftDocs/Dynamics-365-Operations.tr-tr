---
title: PowerApps ve Microsoft Flow kullanarak Talent'ı genişletme - Örnek senaryolar
description: Bu konu, Microsoft PowerApps ve Microsoft Flow kullanan Microsoft Dynamics 365 for Talent için bazı örnek genişletilebilirlik senaryolarını açıklar.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519288"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="76e22-103">PowerApps ve Microsoft Flow kullanarak Talent'ı genişletme - Örnek senaryolar</span><span class="sxs-lookup"><span data-stu-id="76e22-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="76e22-104">Bu konu, Microsoft PowerApps ve Microsoft Flow kullanan Microsoft Dynamics 365 for Talent için bazı örnek genişletilebilirlik senaryolarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="76e22-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="76e22-105">Her bir örnek ile ilişkilendirilmiş çözüm paketini PowerApps ortamınıza içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76e22-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="76e22-106">Daha sonra paketleri kılavuz veya başlangıç noktası olarak kullanarak, kuruluşunuza uygun olan senaryoları gerçekleştirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76e22-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76e22-107">Bu konuda açıklanan şablonları ve uygulamayı "olduğu gibi" kullanmak istiyorsanız, uygulamanıza spesifik olan tüm senaryoları kapsadıklarından emin olmak için test ettiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="76e22-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="76e22-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="76e22-108">Prerequisites</span></span>

- <span data-ttu-id="76e22-109">Paketleri almak için kullanıcıların **Ortam Yapıcı** izni olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="76e22-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="76e22-110">Uygulamaları içe veya dışa aktarmak için kullanıcıların bir PowerApps Plan 2 lisansı veya PowerApps Plan 2 deneme lisansına sahip olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="76e22-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="76e22-111">Akış - Form Bağlantısı</span><span class="sxs-lookup"><span data-stu-id="76e22-111">Flow – Form Connect</span></span>

<span data-ttu-id="76e22-112">**Akış - Form Bağlantısı** şablonu, Microsoft Formlarından veri okumak ve bunları bir Common Data Service varlığı içinde depolamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="76e22-113">Bu şablon, diğer senaryolar için kullanılabilecek şekilde genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="76e22-114">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="76e22-114">Here are some examples:</span></span>

- <span data-ttu-id="76e22-115">Aday değerlendirmeleri yakalama.</span><span class="sxs-lookup"><span data-stu-id="76e22-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="76e22-116">Kurs anketlerinden sonuçları yakala.</span><span class="sxs-lookup"><span data-stu-id="76e22-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="76e22-117">İnsan kaynakları (İK) yöneticileri için bir görüşme soruları kütüphanesi derleyin.</span><span class="sxs-lookup"><span data-stu-id="76e22-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="76e22-118">Bir adayın görüşme sürecini değerlendirmesini yakalayın</span><span class="sxs-lookup"><span data-stu-id="76e22-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="76e22-119">Microsoft Dynamics 365 içinde: Attract, formları Aday portalında görüntülenebilir ve adaylar ayrıntıları doldurabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="76e22-120">Formlar ayrıca bir iş şablonunda etkinlikler olarak katıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="76e22-121">Bir aday bir form gönderdiğinde, Microsoft Flow, form gönderimini yakalar, veriyi okur ve Common Data Service varlığı içinde depolar.</span><span class="sxs-lookup"><span data-stu-id="76e22-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="76e22-122">**Akış - Form Bağlantısı** şablonunu ve Özel Varlık Yapısını indirmek için [Akış - Form Bağlantısı](https://go.microsoft.com/fwlink/?linkid=2081988)'na, Microsoft Download Center üzerinden gidin.</span><span class="sxs-lookup"><span data-stu-id="76e22-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="76e22-123">PowerApps'e aktarılan parametreleri başlat ve ayıkla</span><span class="sxs-lookup"><span data-stu-id="76e22-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="76e22-124">**PowerApps'e aktarılan parametreleri başlat ve ayıkla** şablonu Attract'e özel olan PowerApps senaryosuna bir başlangıç noktası olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="76e22-125">Attract'e aktarılan tüm varsayılan parametreleri içerir, örnein **İş Başvurusu**, **Aday Kimlik Kodu** ve **JobID** gibi.</span><span class="sxs-lookup"><span data-stu-id="76e22-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="76e22-126">Bu şablon, aday değerlendirme formunu çağırmak için kullanılabilir, böylece işe alan yönetici adayın doldurduğu değerlendirmeyi görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="76e22-127">PowerApps kullanılarak oluşturulan uygulamalar Attract içindeki bir iş şablonuna katıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="76e22-128">**PowerApps'e aktarılan parametreleri başlat ve ayıkla** şablonu ve Özel Varlık Yapısını indirmek için [PowerApps'e aktarılan parametreleri başlat ve ayıkla](https://go.microsoft.com/fwlink/?linkid=2081991)'ya Microsoft Download  Center üzerinden gidin.</span><span class="sxs-lookup"><span data-stu-id="76e22-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="76e22-129">Office 365'le Tümleştirme</span><span class="sxs-lookup"><span data-stu-id="76e22-129">Integration with Office 365</span></span>

<span data-ttu-id="76e22-130">**Office 365 ile tümleştirme** uygulaması, Microsoft Office 365 üzerinden oturum açmış kullanıcılar için takım bilgisini ayıklamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="76e22-131">Talent içindeki çalışanların işe başlama ve işten çıkma ayrıntılarını ve istisna kayıtlarına referans gösterir.</span><span class="sxs-lookup"><span data-stu-id="76e22-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="76e22-132">İşe başlama ve işten çıkma ayrıntıları özel Common Data Service varlıklarında depolanır.</span><span class="sxs-lookup"><span data-stu-id="76e22-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="76e22-133">Varsayım, bu ayrıntıların bir üçüncü parti sistemden tümleştirme aracılığıyla doldurulduğudur.</span><span class="sxs-lookup"><span data-stu-id="76e22-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="76e22-134">Bu uygulama, diğer senaryolar için kullanılabilecek şekilde genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="76e22-135">Örneğin, ekip tatil bilgisini, takvim etkinlikleri ve ekibe özel etkinlikleri göstermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="76e22-136">**Office 365 ile tümleştirme** uygulamasını ve Özel Varlık Yapısını indirmek için [Office 365 ile tümleştirme'ye](https://go.microsoft.com/fwlink/?linkid=2081787) Microsoft Download Center'a gidin.</span><span class="sxs-lookup"><span data-stu-id="76e22-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="76e22-137">Akış - E-posta Bildirimi</span><span class="sxs-lookup"><span data-stu-id="76e22-137">Flow – Email Notification</span></span>

<span data-ttu-id="76e22-138">**Akış - E-posta Bildirimi** şablonu, e-posta bildirimi senaryoları için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="76e22-139">İşe alma sürecinin herhangi bir aşamasında işe alma ekibinin reddettiği adaylara bildirim e-postaları gönderilmesini tetiklemekte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="76e22-140">Bu şablon, adaylık aşamasında işe alma süreci boyunca değişiklikleri takip etmek için ve işe alma ekibi ve adaya bildirimler göndermek için genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="76e22-141">Genel olarak, Common Data Service içinde depolanan varlıklar, akışlar Core HR veya Dynamics 365 Talent: Onboard içinde gerçekleşen etkinlikler için bildirimler göndermek üzere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="76e22-142">**Akış - E-posta Bildirimi** şablonunu indirmek için [Akış - E-posta bildirimi](https://go.microsoft.com/fwlink/?linkid=2082103)'ne Microsoft Download Center'dan gidin.</span><span class="sxs-lookup"><span data-stu-id="76e22-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="76e22-143">Akış - SQL Bağlan ve yürüt</span><span class="sxs-lookup"><span data-stu-id="76e22-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="76e22-144">**Akış - SQL Bağlan ve yürüt** şablonu, Microsoft SQL Server'e bağlanır ve SQL sorgularının yürütülmesini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="76e22-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="76e22-145">Bu şablon, SQL tablolarını okumak ve güncelleştirmek üzere tasarlanmış olsa da, diğer senaryolar için kullanılmak üzere genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="76e22-146">Örneğin, Common Data Service içinde bir hazırlama tablosunu SQL Server'dan doldurmak ve hazırlama tablosunu SQL Server'dan kademeli şekilde eşitlemek üzere kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="76e22-147">**Akış - SQL Bağlan ve yürüt** şablonunu indirmek için [Akış - SQL Bağlan ve yürüt](https://go.microsoft.com/fwlink/?linkid=2081789)'na, Microsoft Download Center üzerinden gidin.</span><span class="sxs-lookup"><span data-stu-id="76e22-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="76e22-148">Akış - SharePoint Tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="76e22-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="76e22-149">**Akış - SharePoint Tümleştirmesi** şablonu, Microsoft SharePoint listesinden veri okumak, listeleri herhangi bir Common Data Service varlığı için alan değerleriyle karşılaştırmak ve karşılaştırmanın sonuçlarını bir bildirim e-postası olarak gönderir.</span><span class="sxs-lookup"><span data-stu-id="76e22-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="76e22-150">Bir kuruluş, acil olarak ihtiyaç duydukları bir yetenek kümesine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="76e22-151">Bu yetenekler, SharePoint içinde bir SharePoint listesi olarak depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="76e22-152">Bir aday, bir gerekli yetenekler kümesinin listelendiği herhangi bir işe başvurduğunda, adayın yetenekleri ve SharePoint içinde depolanmış yetenekler arasında önemli bir eşleşme varsa bir e-posta bildirimi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="76e22-153">Bu şekilde, acil olarak ihtiyaç duyulan pozisyonlar daha hızlı doldurulur çünkü bildirimler işe alanların adaylara kuruluş içinden ulaşmasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="76e22-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="76e22-154">Bu şablon, SharePoint tümleştirmesi içeren herhangi bir senaryoda kullanılmak üzere genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="76e22-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="76e22-155">**Akış - SharePoint Tümleştirmesi** şablonunu indirmek için [Akış - SharePoint Tümleştirmesi](https://go.microsoft.com/fwlink/?linkid=2082109)'ne Microsoft Download Center'dan gidin.</span><span class="sxs-lookup"><span data-stu-id="76e22-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="76e22-156">Yetenek havuzlarını yönetmek için yönetici konsolu</span><span class="sxs-lookup"><span data-stu-id="76e22-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="76e22-157">LinkedIn ile tümleştirmeyi etkinleştirdiğinizde, Attract otomatik olarak LinkedIn'de bir yetenek havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="76e22-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="76e22-158">Bir işe alım görevlisi işe alınan kişiyle LinkedIn üzerinden InMail ile e-posta alış verişi yaptığında Attract işe alınan kişi için bir profil oluşturur ve yeni işe alınan LinkedIn yetenek havuzunun üyesi olur.</span><span class="sxs-lookup"><span data-stu-id="76e22-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="76e22-159">Bu PowerApps uygulaması, yeteneğe dayalı olarak yetenek havuzlarındaki adayları yeniden düzenleme için yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="76e22-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="76e22-160">Aşağıdaki görevleri gerçekleştirmek için bu PowerApps uygulamasını yönetici konsolu olarak çalıştırın:</span><span class="sxs-lookup"><span data-stu-id="76e22-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="76e22-161">Yetenek havuzunda adayları listeleme</span><span class="sxs-lookup"><span data-stu-id="76e22-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="76e22-162">Yetenek havuzun aday ekleme veya kaldırma</span><span class="sxs-lookup"><span data-stu-id="76e22-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="76e22-163">Adayları bir yetenek havuzundan başka bir tanesine taşıma</span><span class="sxs-lookup"><span data-stu-id="76e22-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="76e22-164">Adayların taşımadan önce zaten bir yetenek havuzunun parçası olup olmadığını belirleme</span><span class="sxs-lookup"><span data-stu-id="76e22-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="76e22-165">Adayları diğer yetenek havuzlarına taşımadan önce niteliklerini denetleme</span><span class="sxs-lookup"><span data-stu-id="76e22-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="76e22-166">Bu PowerApps uygulaması çok-çok ilişkilerin kullanır, böylece çok-çok ilişkisi olan kayıtları çıkarmanız gereken diğer senaryolar için şablon olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="76e22-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="76e22-167">**Yetenek havuzlarını yönetmek için yönetici konsolu** şablonunu indirmek için Microsoft İndirme Merkezinde [Yetenek havuzlarını yönetmek için yönetici konsolu](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469)'na gidin.</span><span class="sxs-lookup"><span data-stu-id="76e22-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76e22-168">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="76e22-168">Additional resources</span></span>

[<span data-ttu-id="76e22-169">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="76e22-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="76e22-170">Kiracılar ve ortamlar arasında uygulamaları geçirmek</span><span class="sxs-lookup"><span data-stu-id="76e22-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
