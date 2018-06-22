---
title: "Project Service Automation tümleştirme parametreleri"
description: "Project Service Automation'ı Dynamics 365 for Finance and Operations'la tümleştirirken verilerin nasıl varsayılan kılınacağını yapılandırabilirsiniz."
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: tr-tr
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a><span data-ttu-id="fe825-103">Project Service Automation tümleştirme parametreleri</span><span class="sxs-lookup"><span data-stu-id="fe825-103">Project Service Automation integration parameters</span></span>

<span data-ttu-id="fe825-104">**Project Service Automation tümleştirme parametreleri** sayfasında, Project Service Automation'ı Finance and Operations'la tümleştirirken verilerin nasıl varsayılan kılınacağını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe825-104">On the **Project Service Automation integration parameters** page, you can configure how data should default when integrating Project Service Automation with Finance and Operations.</span></span> <span data-ttu-id="fe825-105">Project Service Automation'daki projelerin Finance and Operations'ta başarıyla eşitlenebilmesi için aşağıdakilerin ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe825-105">The following must be set up for projects to be successfully synchronized from Project Service Automation in Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="fe825-106">Proje görevleri tümleştirmesi, gider hareketi kategorileri, saat tahminleri, gider tahminleri ve işlev kilitleme, Dynamics 365 for Finance and Operations sürüm 8.0'da mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="fe825-106">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>




| <span data-ttu-id="fe825-107">**Sekme**</span><span class="sxs-lookup"><span data-stu-id="fe825-107">**Tab**</span></span>                      | <span data-ttu-id="fe825-108">**Alan**</span><span class="sxs-lookup"><span data-stu-id="fe825-108">**Field**</span></span>                          | <span data-ttu-id="fe825-109">**Açıklama**</span><span class="sxs-lookup"><span data-stu-id="fe825-109">**Description**</span></span>                    |
|------------------------------|------------------------------------|--------------------------------|
| <span data-ttu-id="fe825-110">**Genel**</span><span class="sxs-lookup"><span data-stu-id="fe825-110">**General**</span></span>                  | <span data-ttu-id="fe825-111">**Varsayılan proje türü**</span><span class="sxs-lookup"><span data-stu-id="fe825-111">**Default project type**</span></span>               | <span data-ttu-id="fe825-112">Tümleştirme şablonunda bir varsayılan değer belirtmediyseniz, projeler Project Service Automation'dan eşitlenirken **Proje türü** için varsayılan değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="fe825-112">Select the default for **Project type**, which is when projects are synchronized from Project Service Automation if you have not provided a default value in the integration template.</span></span> <span data-ttu-id="fe825-113">Eşitleme sırasında yeni projelerin **Proje türü** bu değere ayarlı olacaktır ve bu değer, proje sözleşme satırları Project Service Automation'dan eşitlenirken güncellenebilir.</span><span class="sxs-lookup"><span data-stu-id="fe825-113">During synchronization, new projects will have the **Project type** set to this value and may be updated when the project contract lines are synchronized from Project Service Automation.</span></span>               |
| <span data-ttu-id="fe825-114">**Genel**</span><span class="sxs-lookup"><span data-stu-id="fe825-114">**General**</span></span>                  | <span data-ttu-id="fe825-115">**Süre kategorisi**</span><span class="sxs-lookup"><span data-stu-id="fe825-115">**Time category**</span></span>                      | <span data-ttu-id="fe825-116">Project Service Automation'dan saat tahminleri eşitlenirken **Zaman kategorisi** için varsayılan değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="fe825-116">Select the default for **Time category**, which is when hour estimates are synchronized from Project Service Automation.</span></span> <span data-ttu-id="fe825-117">Eşitleme sırasında, saat tahminleri ve saat gerçek değerleri Project Service Automation'dan eşitlenirken Finance and Operations'taki yeni proje saat tahminlerinin **Kategori** ayarı bu değeri alacaktır.</span><span class="sxs-lookup"><span data-stu-id="fe825-117">During synchronization, new project hour forecasts in Finance and Operations will have the **Category** set to this value when the hour estimates and hour actuals are synchronized from Project Service Automation.</span></span>   |
| <span data-ttu-id="fe825-118">**Genel**</span><span class="sxs-lookup"><span data-stu-id="fe825-118">**General**</span></span>                  | <span data-ttu-id="fe825-119">**Ücret kategorisi**</span><span class="sxs-lookup"><span data-stu-id="fe825-119">**Fee category**</span></span>                       | <span data-ttu-id="fe825-120">Project Service Automation'dan ücret gerçek değerleri eşitlenirken **Ücret kategorisi** için varsayılan değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="fe825-120">Select the default for **Fee category**, which is when fee actuals are synchronized from Project Service Automation.</span></span> <span data-ttu-id="fe825-121">Eşitleme sırasında, ücret gerçek değerleri Project Service Automation'dan eşitlenirken Finance and Operations'taki yeni ücret hareketlerinin **Kategori** ayarı bu değeri alacaktır.</span><span class="sxs-lookup"><span data-stu-id="fe825-121">During synchronization, new fee transactions in Finance and Operations will have the **Category** set to this value when the fee actuals are synchronized from Project Service Automation.</span></span>          |
| <span data-ttu-id="fe825-122">**Proje grubu varsayılanları**</span><span class="sxs-lookup"><span data-stu-id="fe825-122">**Project group defaults**</span></span>   | <span data-ttu-id="fe825-123">**Proje türü**</span><span class="sxs-lookup"><span data-stu-id="fe825-123">**Project type**</span></span> | <span data-ttu-id="fe825-124">Varsayılan proje grubu ayarlanacak proje türünü seçebileceğiniz bir satır eklemek için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe825-124">Click **New** to add a row where you can select the project type for which to set the default project group.</span></span> <span data-ttu-id="fe825-125">Yapılandırmada belirli bir proje türü yalnızca bir kez seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="fe825-125">A specific project type can be selected only once in the configuration.</span></span>              
|                              | <span data-ttu-id="fe825-126">**Proje Grubu**</span><span class="sxs-lookup"><span data-stu-id="fe825-126">**Project group**</span></span>          | <span data-ttu-id="fe825-127">Belirtilen proje türü için varsayılan proje grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="fe825-127">Select the default project group for the specified project type.</span></span> <span data-ttu-id="fe825-128">Tümleştirme şablonunda bir varsayılan değer belirtmediyseniz, Project Service Automation'dan yeni projeler eşitlenirken, **Proje grubu**, proje türüne göre varsayılan olacaktır.</span><span class="sxs-lookup"><span data-stu-id="fe825-128">When new projects are synced from Project Service Automation, the **Project group** will be the default based on the project type if you have not provided a default value in the integration template.</span></span>  |
| <span data-ttu-id="fe825-129">**Faturalama türü varsayılanları**</span><span class="sxs-lookup"><span data-stu-id="fe825-129">**Billing type defaults**</span></span>    | <span data-ttu-id="fe825-130">**Faturalama türü**</span><span class="sxs-lookup"><span data-stu-id="fe825-130">**Billing type**</span></span> | <span data-ttu-id="fe825-131">Varsayılan satır özelliği ayarlanacak faturalama türünü seçebileceğiniz bir satır eklemek için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe825-131">Click **New** to add a row where you can select the billing type for which to set the default line property.</span></span> <span data-ttu-id="fe825-132">Yapılandırmada belirli bir faturalama türü yalnızca bir kez seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="fe825-132">A specific billing type can be selected only once in the configuration.</span></span>          |
|                              | <span data-ttu-id="fe825-133">**Satır özelliği**</span><span class="sxs-lookup"><span data-stu-id="fe825-133">**Line property**</span></span>| <span data-ttu-id="fe825-134">Belirtilen faturalama türü için varsayılan satır özelliğini seçin.</span><span class="sxs-lookup"><span data-stu-id="fe825-134">Select the default line property for the specified billing type.</span></span> <span data-ttu-id="fe825-135">Project Service Automation'dan yeni saat tahminleri, yeni gider tahminleri veya yeni gerçek değerler eşitlenirken, **Satır özelliği**, faturalama türüne göre varsayılan olacaktır.</span><span class="sxs-lookup"><span data-stu-id="fe825-135">When new hour estimates, new expense estimates, or new actuals are synced from Project Service Automation, the **Line property** will be the default based on the billing type.</span></span>          |
| <span data-ttu-id="fe825-136">**İşlev kilitleme**</span><span class="sxs-lookup"><span data-stu-id="fe825-136">**Functionality locking**</span></span>    |                   | <span data-ttu-id="fe825-137">Project Service Automation kaynaklı projeler ve sözleşmeler için Finance and Operations'ta devre dışı bırakılacak işlevselliği seçin.</span><span class="sxs-lookup"><span data-stu-id="fe825-137">Select the functionality to disable in Finance and Operations for projects and contracts that originated from Project Service Automation.</span></span> <span data-ttu-id="fe825-138">Örneğin Finance and Operations'ta sözleşme ve proje düzenleme, iş kırılım yapıları oluşturma ve zaman çizelgeleri girme yeteneklerini devre dışı bırakmayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe825-138">For example, you can choose to turn off the ability to edit contracts and projects, create work breakdown structures, and enter timesheets in Finance and Operations.</span></span> <span data-ttu-id="fe825-139">Muhasebeyle ilgili alanlar parametre ayarıyla kullanılamaz yapılsa bile, etkin olmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="fe825-139">Accounting-related fields will continue to be enabled, even if they are made unavailable by the parameter setting.</span></span> <span data-ttu-id="fe825-140">Varsayılan olarak, tüm işlevsellik etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="fe825-140">By default, all functionality will be enabled.</span></span>           |
