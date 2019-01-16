---
title: "Finance and Operations'tan Field Service'a proje listelerini eşitleme"
description: "Bu konu, projeleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: tr-tr
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="9713a-103">Finance and Operations'tan Field Service'a proje listelerini eşitleme</span><span class="sxs-lookup"><span data-stu-id="9713a-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9713a-104">Bu konu, projeleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="9713a-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="9713a-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="9713a-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9713a-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="9713a-106">Templates and tasks</span></span>
<span data-ttu-id="9713a-107">Aşağıdaki şablon ve görevleri, projeleri Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="9713a-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="9713a-108">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="9713a-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="9713a-109">Projeler (Finance and Operations'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="9713a-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="9713a-110">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="9713a-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="9713a-111">Projeler</span><span class="sxs-lookup"><span data-stu-id="9713a-111">Projects</span></span>

<span data-ttu-id="9713a-112">Aşağıdaki eşitleme görevlerinin, proje listesinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="9713a-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="9713a-113">Hesaplar (Sales'tan Finance and Operations'a)</span><span class="sxs-lookup"><span data-stu-id="9713a-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="9713a-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="9713a-114">Entity set</span></span>
<span data-ttu-id="9713a-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9713a-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="9713a-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="9713a-116">Field Service</span></span>           | <span data-ttu-id="9713a-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9713a-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="9713a-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="9713a-118">msdynce_externalprojects</span></span> | <span data-ttu-id="9713a-119">Projeler</span><span class="sxs-lookup"><span data-stu-id="9713a-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="9713a-120">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="9713a-120">Entity flow</span></span>
<span data-ttu-id="9713a-121">Finance and Operations'ta oluşturulan projeler.</span><span class="sxs-lookup"><span data-stu-id="9713a-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="9713a-122">**Proje türü** Zaman ve malzeme ve **Proje aşaması** işlevde olan projeler, Field Service'ta **Harici Proje** varlığına eşitlenir, Proje numarası, Proje adı, Proje aşaması ve Müşteri hesap bilgisi de dahil.</span><span class="sxs-lookup"><span data-stu-id="9713a-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="9713a-123">**Harici Proje** listesi, Field Service İş Emirlerini, Finance and Operations projeleriyle eşleştirmekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9713a-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="9713a-124">Field Service CRM çözümü Harici Proje, Operations'tan tüm Projeleri alan yeni bir varlıktır.</span><span class="sxs-lookup"><span data-stu-id="9713a-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="9713a-125">Harici Proje alanı, İş Emri varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="9713a-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="9713a-126">Bu alan, bir arama ve İş Emrinizi bir proje ile etiketleyerek, Satış Siparişi daha sonra Operations içindeki bir Projeye bağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="9713a-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="9713a-127">Sistem Durumu Açık olarak değişenler – Sürmekte(690,970,000) daha yüksek bir durum Harici Proje alanı kilitlenir ve değeri ekleyemez, kaldıramaz veya değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="9713a-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9713a-128">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="9713a-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="9713a-129">Finance and Operations'ta</span><span class="sxs-lookup"><span data-stu-id="9713a-129">In Finance and Operations</span></span>
<span data-ttu-id="9713a-130">Veri varlığı Projeleri için izlemeyi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="9713a-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9713a-131">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="9713a-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="9713a-132">Projeler (Finance and Operations'tan Field Service'a): Projeler</span><span class="sxs-lookup"><span data-stu-id="9713a-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="9713a-133">[![Veri tümleştirmede şablon eşleme](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="9713a-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

