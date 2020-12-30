---
title: Power Apps ve Power Automate ile Talent'i genişletme
description: Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Talent - Attract için bazı örnek genişletilebilirlik senaryolarını açıklar.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529646"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a><span data-ttu-id="a3534-103">Power Apps ve Power Automate ile Talent'i genişletme</span><span class="sxs-lookup"><span data-stu-id="a3534-103">Extend Talent with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a3534-104">Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Talent: Attract için bazı örnek genişletilebilirlik senaryolarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="a3534-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Talent: Attract that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="a3534-105">Her bir örnek ile ilişkilendirilmiş çözüm paketini Power Apps ortamınıza içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3534-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="a3534-106">Daha sonra paketleri kılavuz veya başlangıç noktası olarak kullanarak, kuruluşunuza uygun olan senaryoları gerçekleştirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3534-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3534-107">Bu makalede açıklanan şablonları ve uygulamayı "olduğu gibi" kullanmak istiyorsanız, uygulamanıza spesifik olan tüm senaryoları kapsadıklarından emin olmak için test ettiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="a3534-107">If you want to use the templates and app that are described in this article "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="a3534-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="a3534-108">Prerequisites</span></span>

- <span data-ttu-id="a3534-109">Paketleri almak için kullanıcıların **Ortam Yapıcı** izni olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a3534-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="a3534-110">Uygulamaları içe veya dışa aktarmak için kullanıcıların bir Power Apps Plan 2 lisansı veya Power Apps Plan 2 deneme lisansına sahip olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="a3534-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="power-automate--form-connect"></a><span data-ttu-id="a3534-111">Power Automate – Form Bağlantısı</span><span class="sxs-lookup"><span data-stu-id="a3534-111">Power Automate – Form Connect</span></span>

<span data-ttu-id="a3534-112">**Power Automate – Form Bağlantısı** şablonu, Microsoft Forms'tan veri okumak ve bunları bir Common Data Service varlığı içinde depolamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a3534-112">The **Power Automate – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="a3534-113">Bu şablon, diğer senaryolar için kullanılabilecek şekilde genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="a3534-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="a3534-114">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="a3534-114">Here are some examples:</span></span>

- <span data-ttu-id="a3534-115">Aday değerlendirmeleri yakalama.</span><span class="sxs-lookup"><span data-stu-id="a3534-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="a3534-116">Kurs anketlerinden sonuçları yakala.</span><span class="sxs-lookup"><span data-stu-id="a3534-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="a3534-117">İnsan kaynakları (İK) yöneticileri için bir görüşme soruları kütüphanesi derleyin.</span><span class="sxs-lookup"><span data-stu-id="a3534-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="a3534-118">Bir adayın görüşme sürecini değerlendirmesini yakalayın</span><span class="sxs-lookup"><span data-stu-id="a3534-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="a3534-119">Microsoft Dynamics 365: Attract'ta, adayların bilgilerini girdiği aday portalındaki formları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3534-119">In Microsoft Dynamics 365: Attract, you can use forms in the candidate portal, where candidates fill in details.</span></span> <span data-ttu-id="a3534-120">Ayrıca formları bir iş şablonuna etkinlikler olarak da katıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3534-120">You can also embed forms as activities in a job template.</span></span>

<span data-ttu-id="a3534-121">Bir aday bir form gönderdiğinde, Microsoft Power Automate, form gönderimini yakalar, veriyi okur ve Common Data Service varlığı içinde depolar.</span><span class="sxs-lookup"><span data-stu-id="a3534-121">When a candidate submits a form, Microsoft Power Automate captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="a3534-122">**Power Automate – Form Bağlantısı** şablonunu ve Özel Varlık Yapısını indirmek için Microsoft İndirme Merkezi'nde [Power Automate – Form Bağlantısı](https://go.microsoft.com/fwlink/?linkid=2081988)'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a3534-122">To download the **Power Automate – Form Connect** template and Custom Entity Structure, go to [Power Automate – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sharepoint-integration"></a><span data-ttu-id="a3534-123">Power Automate – SharePoint Tümleştirmesi</span><span class="sxs-lookup"><span data-stu-id="a3534-123">Power Automate – SharePoint Integration</span></span>

<span data-ttu-id="a3534-124">**Power Automate – SharePoint Tümleştirmesi** şablonu, Microsoft SharePoint listesinden veri okumak, listeleri herhangi bir Common Data Service varlığı için alan değerleriyle karşılaştırmak ve karşılaştırmanın sonuçlarını bir bildirim e-postası olarak göndermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a3534-124">The **Power Automate – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="a3534-125">Bir kuruluş, acil olarak ihtiyaç duydukları bir yetenek kümesine sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="a3534-125">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="a3534-126">Bu yetenekler, SharePoint içinde bir SharePoint listesi olarak depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="a3534-126">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="a3534-127">Bir aday, bir gerekli yetenekler kümesinin listelendiği herhangi bir işe başvurduğunda, adayın yetenekleri ve SharePoint içinde depolanmış yetenekler arasında önemli bir eşleşme varsa bir e-posta bildirimi gönderilir.</span><span class="sxs-lookup"><span data-stu-id="a3534-127">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="a3534-128">Bu, acil olarak ihtiyaç duyulan pozisyonların daha hızlı doldurulmasına yardımcı olur çünkü bildirimler işe alanların kuruluş içinden adaylara ulaşmalarına yardım eder.</span><span class="sxs-lookup"><span data-stu-id="a3534-128">This helps fill positions that are urgently required faster, because the notifications help recruiters cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="a3534-129">Bu şablon, SharePoint tümleştirmesi içeren herhangi bir senaryoda kullanılmak üzere genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="a3534-129">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="a3534-130">**Power Automate – SharePoint Tümleştirmesi** şablonunu indirmek için Microsoft İndirme Merkezi'nde [Power Automate – SharePoint Tümleştirmesi](https://go.microsoft.com/fwlink/?linkid=2082109) bağlantısına gidin.</span><span class="sxs-lookup"><span data-stu-id="a3534-130">To download the **Power Automate – SharePoint Integration** template, go to [Power Automate – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="referral-app"></a><span data-ttu-id="a3534-131">Başvuru Uygulaması</span><span class="sxs-lookup"><span data-stu-id="a3534-131">Referral App</span></span>

<span data-ttu-id="a3534-132">Paylaşılan bir yetenek havuzuna aday eklemek için referans uygulamasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3534-132">You can use the Referral App to add candidates to a shared talent pool.</span></span> <span data-ttu-id="a3534-133">Başvuran, adayı gönderirken **FirstName**, **LastName**, **Email** ve **Linkedln URL** girebilir.</span><span class="sxs-lookup"><span data-stu-id="a3534-133">The referrer can enter **Firstname**, **Lastname**, **Email**, and **LinkedIn URL** when submitting a candidate.</span></span> <span data-ttu-id="a3534-134">Aday kaynak meta verileri daha sonra başvuran bilgileri ile doldurulur.</span><span class="sxs-lookup"><span data-stu-id="a3534-134">The candidate source metadata is then populated with the referrer’s information.</span></span>

<span data-ttu-id="a3534-135">Bu uygulamayı, referanslar göndermek için çalışan self servisi'ne (ESS) katıştırabilir veya bunu şirket portalında köprü olarak kullanıp tek başına çalışan bir uygulama olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3534-135">You can embed this app in Employee self service for submitting referrals, or you can use it as a hyperlink in the corporate portal and run it as a stand-alone app.</span></span>

<span data-ttu-id="a3534-136">**Referans uygulamasını** karşıdan yüklemek için Microsoft İndirme Merkezi'nde [Dynamics 365 Talent genişletilebilirlik çözümü: Referans Uygulaması](https://www.microsoft.com/download/details.aspx?id=58497) bağlantısına gidin.</span><span class="sxs-lookup"><span data-stu-id="a3534-136">To download **Referral App**, go to [Dynamics 365 Talent extensibility solution: Referral App](https://www.microsoft.com/download/details.aspx?id=58497) on the Microsoft Download Center.</span></span> <span data-ttu-id="a3534-137">Bu uygulamayı içe aktarabilir ve başka işlevler eklemek için özelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3534-137">You can import this app and customize it to add additional functionality.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3534-138">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a3534-138">Additional resources</span></span>

[<span data-ttu-id="a3534-139">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="a3534-139">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[<span data-ttu-id="a3534-140">Kiracılar ve ortamlar arasında uygulamaları geçirmek</span><span class="sxs-lookup"><span data-stu-id="a3534-140">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
