---
title: Power Apps ve Power Automate ile Talent'i genişletme
description: Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Human Resources için bazı örnek genişletilebilirlik senaryolarını açıklar.
author: negudava
manager: tfehr
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6885c67f42ead34b5e10cc1b1a80a88fd2d59b9
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115378"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="68f6c-103">Power Apps ve Power Automate ile genişletme</span><span class="sxs-lookup"><span data-stu-id="68f6c-103">Extend with Power Apps and Power Automate</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="68f6c-104">Bu konu, Microsoft Power Apps ve Microsoft Power Automate kullanan Microsoft Dynamics 365 Human Resources için bazı örnek genişletilebilirlik senaryolarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="68f6c-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="68f6c-105">Her bir örnek ile ilişkilendirilmiş çözüm paketini Power Apps ortamınıza içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68f6c-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="68f6c-106">Daha sonra paketleri kılavuz veya başlangıç noktası olarak kullanarak, kuruluşunuza uygun olan senaryoları gerçekleştirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68f6c-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68f6c-107">Bu konuda açıklanan şablonları ve uygulamayı "olduğu gibi" kullanmak istiyorsanız, uygulamanıza spesifik olan tüm senaryoları kapsadıklarından emin olmak için test ettiğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="68f6c-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="68f6c-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="68f6c-108">Prerequisites</span></span>

- <span data-ttu-id="68f6c-109">Paketleri almak için kullanıcıların **Ortam Yapıcı** izni olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="68f6c-110">Uygulamaları içe veya dışa aktarmak için kullanıcıların bir Power Apps Plan 2 lisansı veya Power Apps Plan 2 deneme lisansına sahip olmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="68f6c-111">Microsoft 365, Power Automate ile tümleştirme</span><span class="sxs-lookup"><span data-stu-id="68f6c-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="68f6c-112">**Microsoft 365 ile tümleştirme** uygulaması, Microsoft 365 üzerinden oturum açmış kullanıcılar için takım bilgisini ayıklamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="68f6c-113">Çalışanların kimlik tiplerini çıkarmak için İnsan Kaynakları çalışanlara başvurur.</span><span class="sxs-lookup"><span data-stu-id="68f6c-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="68f6c-114">Yöneticiler, çalışan kimlik tiplerinin sona erme tarihlerini denetleyebilir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="68f6c-115">Çalışan numarası tipi sona ertiğinde, bunlar da e-posta anımsatıcısı gönderebilirler.</span><span class="sxs-lookup"><span data-stu-id="68f6c-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="68f6c-116">Power Automate, bu anımsatıcıyı göndermek için Power Apps ile birleşir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="68f6c-117">Anımsatıcı gönderildiğinde, onay Power Automate'tan Power Apps'e geri gönderilir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="68f6c-118">Tanımlama türleri, sürücünün lisansını, Passport 'unu ve kabul edilen diğer kod biçimlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="68f6c-119">Bu uygulamayı diğer senaryolar için genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68f6c-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="68f6c-120">Örneğin, ekip tatil bilgisini, takvim etkinlikleri ve ekibe özel etkinlikleri göstermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="68f6c-121">**Microsoft 365, Power Automate ile Tümleştirme** uygulamasını indirmek için Microsoft İndirme Merkezi'nde [Microsoft 365 ile Tümleştirme bağlantısına](https://go.microsoft.com/fwlink/?linkid=2081787) gidin.</span><span class="sxs-lookup"><span data-stu-id="68f6c-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="68f6c-122">Power Automate – SQL Bağlan ve yürüt</span><span class="sxs-lookup"><span data-stu-id="68f6c-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="68f6c-123">**Power Automate – SQL Bağlan ve yürüt** şablonu, Microsoft SQL Server'a bağlanır ve SQL sorgularının çalıştırılmasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="68f6c-124">Bu şablon SQL tablolarını okuyup güncelleştirse de, genişletebilir ve diğer senaryolar için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="68f6c-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="68f6c-125">Örneğin, Dataverse içinde bir hazırlama tablosunu SQL Server'dan doldurmak ve hazırlama tablosunu SQL Server'dan kademeli şekilde eşitlemek üzere kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="68f6c-126">Veri dönüşümü ve artımlı gönderimi etkinleştirmek için Gelişmiş sorgu akış ile tümleşiktir.</span><span class="sxs-lookup"><span data-stu-id="68f6c-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="68f6c-127">**Power Automate – SQL Bağlan ve yürüt** şablonunu indirmek için Microsoft İndirme Merkezi'nde [Power Automate – SQL Bağlan ve yürüt](https://go.microsoft.com/fwlink/?linkid=2081789) bağlantısına gidin.</span><span class="sxs-lookup"><span data-stu-id="68f6c-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68f6c-128">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="68f6c-128">Additional resources</span></span>

[<span data-ttu-id="68f6c-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="68f6c-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>