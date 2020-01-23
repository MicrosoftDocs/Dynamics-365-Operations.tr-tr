---
title: Power Apps ve Power Automate ile Talent'i genişletme
description: Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Talent için bazı örnek genişletilebilirlik senaryolarını açıklar.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
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
ms.openlocfilehash: 6c8a583a93c2ceb70d8c3b0e0047e2bf2047b56d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898329"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="995e8-103">Power Apps ve Power Automate ile Talent'i genişletme</span><span class="sxs-lookup"><span data-stu-id="995e8-103">Extend Talent with Power Apps and Power Automate</span></span>

<span data-ttu-id="995e8-104">Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Talent için bazı örnek genişletilebilirlik senaryolarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="995e8-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="995e8-105">Her bir örnek ile ilişkilendirilmiş çözüm paketini Power Apps ortamınıza içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="995e8-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="995e8-106">Daha sonra paketleri kılavuz veya başlangıç noktası olarak kullanarak, kuruluşunuza uygun olan senaryoları gerçekleştirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="995e8-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="995e8-107">Bu konuda açıklanan şablonları ve uygulamayı "olduğu gibi" kullanmak istiyorsanız, uygulamanıza spesifik olan tüm senaryoları kapsadıklarından emin olmak için test ettiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="995e8-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="995e8-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="995e8-108">Prerequisites</span></span>

- <span data-ttu-id="995e8-109">Paketleri almak için kullanıcıların **Ortam Yapıcı** izni olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="995e8-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="995e8-110">Uygulamaları içe veya dışa aktarmak için kullanıcıların bir Power Apps Plan 2 lisansı veya Power Apps Plan 2 deneme lisansına sahip olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="995e8-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="995e8-111">Power Automate – Form Bağlantısı</span><span class="sxs-lookup"><span data-stu-id="995e8-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="995e8-112">**Power Automate – Form Bağlantısı** şablonu, Microsoft Forms'tan veri okumak ve bunları bir Common Data Service varlığı içinde depolamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="995e8-113">Bu şablon, diğer senaryolar için kullanılabilecek şekilde genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="995e8-114">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="995e8-114">Here are some examples:</span></span>

- <span data-ttu-id="995e8-115">Aday değerlendirmeleri yakalama.</span><span class="sxs-lookup"><span data-stu-id="995e8-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="995e8-116">Kurs anketlerinden sonuçları yakala.</span><span class="sxs-lookup"><span data-stu-id="995e8-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="995e8-117">İnsan kaynakları (İK) yöneticileri için bir görüşme soruları kütüphanesi derleyin.</span><span class="sxs-lookup"><span data-stu-id="995e8-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="995e8-118">Bir adayın görüşme sürecini değerlendirmesini yakalayın</span><span class="sxs-lookup"><span data-stu-id="995e8-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="995e8-119">Microsoft Dynamics 365 içinde: Attract, formları Aday portalında görüntülenebilir ve adaylar ayrıntıları doldurabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="995e8-120">Formlar ayrıca bir iş şablonunda etkinlikler olarak katıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="995e8-121">Bir aday bir form gönderdiğinde, Microsoft Power Automate, form gönderimini yakalar, veriyi okur ve Common Data Service varlığı içinde depolar.</span><span class="sxs-lookup"><span data-stu-id="995e8-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="995e8-122">**Power Automate – Form Bağlantısı** şablonunu ve Özel Varlık Yapısını indirmek için Microsoft İndirme Merkezi'nde [Power Automate – Form Bağlantısı](https://go.microsoft.com/fwlink/?linkid=2081988)'na gidin.</span><span class="sxs-lookup"><span data-stu-id="995e8-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a><span data-ttu-id="995e8-123">Power Apps'e aktarılan parametreleri başlat ve ayıkla</span><span class="sxs-lookup"><span data-stu-id="995e8-123">Initiate and Extract Parameters Passed to Power Apps</span></span>

<span data-ttu-id="995e8-124">**Power Apps'e aktarılan parametreleri başlat ve ayıkla** şablonu Attract'e özel olan tüm Power Apps senaryoları için bir başlangıç noktası olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-124">The **Initiate and Extract Parameters Passed to Power Apps** template can be used as a starting point for any Power Apps scenario that is specific to Attract.</span></span> <span data-ttu-id="995e8-125">Attract'e aktarılan tüm varsayılan parametreleri içerir, örnein **İş Başvurusu**, **Aday Kimlik Kodu** ve **JobID** gibi.</span><span class="sxs-lookup"><span data-stu-id="995e8-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="995e8-126">Bu şablon, aday değerlendirme formunu çağırmak için kullanılabilir, böylece işe alan yönetici adayın doldurduğu değerlendirmeyi görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="995e8-127">Power Apps kullanılarak oluşturulan uygulamalar Attract içindeki bir iş şablonuna katıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-127">Apps that are created by using Power Apps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="995e8-128">**Power Apps'e aktarılan parametreleri başlat ve ayıkla** şablonunu ve Özel Varlık Yapısını indirmek için Microsoft İndirme Merkezi'nde [Power Apps'e aktarılan parametreleri başlat ve ayıkla](https://go.microsoft.com/fwlink/?linkid=2081991) bağlantısına gidin.</span><span class="sxs-lookup"><span data-stu-id="995e8-128">To download the **Initiate and Extract Parameters Passed to Power Apps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Power Apps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="995e8-129">Office 365'le Tümleştirme</span><span class="sxs-lookup"><span data-stu-id="995e8-129">Integration with Office 365</span></span>

<span data-ttu-id="995e8-130">**Office 365 ile tümleştirme** uygulaması, Microsoft Office 365 üzerinden oturum açmış kullanıcılar için takım bilgisini ayıklamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="995e8-131">Talent içindeki çalışanların işe başlama ve işten çıkma ayrıntılarını ve istisna kayıtlarına referans gösterir.</span><span class="sxs-lookup"><span data-stu-id="995e8-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="995e8-132">İşe başlama ve işten çıkma ayrıntıları özel Common Data Service varlıklarında depolanır.</span><span class="sxs-lookup"><span data-stu-id="995e8-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="995e8-133">Varsayım, bu ayrıntıların bir üçüncü parti sistemden tümleştirme aracılığıyla doldurulduğudur.</span><span class="sxs-lookup"><span data-stu-id="995e8-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="995e8-134">Bu uygulama, diğer senaryolar için kullanılabilecek şekilde genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="995e8-135">Örneğin, ekip tatil bilgisini, takvim etkinlikleri ve ekibe özel etkinlikleri göstermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="995e8-136">**Office 365 ile tümleştirme** uygulamasını ve Özel Varlık Yapısını indirmek için Microsoft İndirme Merkezi'nde [Office 365 ile tümleştirme](https://go.microsoft.com/fwlink/?linkid=2081787)'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="995e8-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--email-notification"></a><span data-ttu-id="995e8-137">Power Automate – E-posta Bildirimi</span><span class="sxs-lookup"><span data-stu-id="995e8-137">Power Automate – Email Notification</span></span>

<span data-ttu-id="995e8-138">**Power Automate – E-posta Bildirimi** şablonu, e-posta bildirimi senaryoları için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-138">The **Power Automate – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="995e8-139">İşe alma sürecinin herhangi bir aşamasında işe alma ekibinin reddettiği adaylara bildirim e-postaları gönderilmesini tetiklemekte kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="995e8-140">Bu şablon, adaylık aşamasında işe alma süreci boyunca değişiklikleri takip etmek için ve işe alma ekibi ve adaya bildirimler göndermek için genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="995e8-141">Genel olarak, Common Data Service içinde depolanan varlıklar, akışlar Core HR, Attract veya Onboard içinde gerçekleşen etkinlikler için bildirimler göndermek üzere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Onboard.</span></span>

<span data-ttu-id="995e8-142">**Power Automate – E-posta Bildirimi** şablonunu indirmek için Microsoft İndirme Merkezi'nde [Power Automate – E-posta Bildirimi](https://go.microsoft.com/fwlink/?linkid=2082103) bağlantısına gidin.</span><span class="sxs-lookup"><span data-stu-id="995e8-142">To download the **Power Automate – Email Notification** template, go to [Power Automate – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="995e8-143">Power Automate – SQL Bağlan ve yürüt</span><span class="sxs-lookup"><span data-stu-id="995e8-143">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="995e8-144">**Power Automate – SQL Bağlan ve yürüt** şablonu, Microsoft SQL Server'a bağlanır ve SQL sorgularının çalıştırılmasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="995e8-144">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="995e8-145">Bu şablon, SQL tablolarını okumak ve güncelleştirmek üzere tasarlanmış olsa da, diğer senaryolar için kullanılmak üzere genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="995e8-146">Örneğin, Common Data Service içinde bir hazırlama tablosunu SQL Server'dan doldurmak ve hazırlama tablosunu SQL Server'dan kademeli şekilde eşitlemek üzere kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="995e8-147">**Power Automate – SQL Bağlan ve yürüt** şablonunu indirmek için Microsoft İndirme Merkezi'nde [Power Automate – SQL Bağlan ve yürüt](https://go.microsoft.com/fwlink/?linkid=2081789) bağlantısına gidin.</span><span class="sxs-lookup"><span data-stu-id="995e8-147">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="995e8-148">Power Automate – SharePoint Tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="995e8-148">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="995e8-149">**Power Automate – SharePoint Tümleştirmesi** şablonu, Microsoft SharePoint listesinden veri okumak, listeleri herhangi bir Common Data Service varlığı için alan değerleriyle karşılaştırmak ve karşılaştırmanın sonuçlarını bir bildirim e-postası olarak göndermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-149">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="995e8-150">Bir kuruluş, acil olarak ihtiyaç duydukları bir yetenek kümesine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="995e8-151">Bu yetenekler, SharePoint içinde bir SharePoint listesi olarak depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="995e8-152">Bir aday, bir gerekli yetenekler kümesinin listelendiği herhangi bir işe başvurduğunda, adayın yetenekleri ve SharePoint içinde depolanmış yetenekler arasında önemli bir eşleşme varsa bir e-posta bildirimi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="995e8-153">Bu şekilde, acil olarak ihtiyaç duyulan pozisyonlar daha hızlı doldurulur çünkü bildirimler işe alanların adaylara kuruluş içinden ulaşmasına olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="995e8-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="995e8-154">Bu şablon, SharePoint tümleştirmesi içeren herhangi bir senaryoda kullanılmak üzere genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="995e8-155">**Power Automate – SharePoint Tümleştirmesi** şablonunu indirmek için Microsoft İndirme Merkezi'nde [Power Automate – SharePoint Tümleştirmesi](https://go.microsoft.com/fwlink/?linkid=2082109) bağlantısına gidin.</span><span class="sxs-lookup"><span data-stu-id="995e8-155">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="995e8-156">Başvuru Uygulaması</span><span class="sxs-lookup"><span data-stu-id="995e8-156">Referral App</span></span>
<span data-ttu-id="995e8-157">Paylaşılan bir yetenek havuzuna aday eklemek için referans uygulamasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="995e8-157">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="995e8-158">Başvuran, adayı gönderirken **FirstName**, **LastName**, **Email** ve **Linkedln URL'sini** girebilir.</span><span class="sxs-lookup"><span data-stu-id="995e8-158">The referrer can enter **Firstname**, **Lastname**, **Email**, and **Linkedln URL** when submitting a candidate.</span></span> <span data-ttu-id="995e8-159">Aday kaynak meta verileri daha sonra başvuran bilgileri ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="995e8-159">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="995e8-160">Bu uygulamayı, referanslar göndermek için çalışan self servisi'ne (ESS) katıştırabilir veya bunu şirket portalında köprü olarak kullanıp tek başına çalışan bir uygulama olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="995e8-160">You can embed this app in Employee self-service (ESS) for submitting referrals, or you can be use it as a hyperlink in the Corporate Portal and run as a stand-alone app.</span></span>

<span data-ttu-id="995e8-161">**Referans uygulamasını** karşıdan yüklemek için Microsoft İndirme Merkezi'nde [Dynamics 365 Talent genişletilebilirlik çözümü: Referans Uygulaması](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) bağlantısına gidin.</span><span class="sxs-lookup"><span data-stu-id="995e8-161">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d) on the Microsoft Download Center.</span></span> <span data-ttu-id="995e8-162">Bu uygulamayı içe aktarabilir ve başka işlevler eklemek için özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="995e8-162">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="995e8-163">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="995e8-163">Additional resources</span></span>

[<span data-ttu-id="995e8-164">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="995e8-164">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="995e8-165">Kiracılar ve ortamlar arasında uygulamaları geçirmek</span><span class="sxs-lookup"><span data-stu-id="995e8-165">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
