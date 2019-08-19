---
title: Finance and Operations'tan Field Service'a proje listelerini eşitleme
description: Bu konu projeleri Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843565"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="4aa96-103">Proje listesini Finance and Operations'dan Field Service'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="4aa96-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4aa96-104">Bu konu projeleri Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="4aa96-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="4aa96-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="4aa96-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4aa96-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="4aa96-106">Templates and tasks</span></span>
<span data-ttu-id="4aa96-107">Aşağıdaki şablon ve görevler, Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine projelerin eşitlenmesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4aa96-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="4aa96-108">**Veri Tümleştirmesindeki Şablon**</span><span class="sxs-lookup"><span data-stu-id="4aa96-108">**Template in Data integration**</span></span>
- <span data-ttu-id="4aa96-109">Projeler (Fin and Ops'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="4aa96-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="4aa96-110">**Veri tümleştirme projesindeki görev**</span><span class="sxs-lookup"><span data-stu-id="4aa96-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="4aa96-111">Projeler</span><span class="sxs-lookup"><span data-stu-id="4aa96-111">Projects</span></span>

<span data-ttu-id="4aa96-112">Aşağıdaki eşitleme görevlerinin, proje listesinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="4aa96-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="4aa96-113">Hesaplar (Sales'ten Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="4aa96-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="4aa96-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="4aa96-114">Entity set</span></span>
| <span data-ttu-id="4aa96-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="4aa96-115">Field Service</span></span>           | <span data-ttu-id="4aa96-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4aa96-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="4aa96-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="4aa96-117">msdynce_externalprojects</span></span> | <span data-ttu-id="4aa96-118">Projeler</span><span class="sxs-lookup"><span data-stu-id="4aa96-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="4aa96-119">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="4aa96-119">Entity flow</span></span>
<span data-ttu-id="4aa96-120">Finance and Operations'ta oluşturulan projeler.</span><span class="sxs-lookup"><span data-stu-id="4aa96-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="4aa96-121">**Proje türü**, **Zaman ve malzeme**'ye ayarlanır ve **Proje aşaması**, **İşlevde olan** projelere ayarlanır, Field Service'ta **Harici Proje** varlığına eşitlenir, Proje numarası, Proje adı, Proje aşaması ve Müşteri hesap bilgisi de dahil.</span><span class="sxs-lookup"><span data-stu-id="4aa96-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="4aa96-122">**Harici Proje** listesi, Field Service iş emirlerini, Finance and Operations projeleriyle eşleştirmekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4aa96-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="4aa96-123">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="4aa96-123">Field Service CRM solution</span></span>
<span data-ttu-id="4aa96-124">**Harici Proje** varlığı, tüm projeleri Finance and Operations'tan alır.</span><span class="sxs-lookup"><span data-stu-id="4aa96-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="4aa96-125">**Harici Proje** alanı, **İş Emri** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="4aa96-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="4aa96-126">Bu bir arama alanıdır, iş amirlerinizi bir proje ile etiketlediğinizde, satış siparişi Finance and Operations içindeki bir projeye bağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="4aa96-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="4aa96-127">**Sistem Durumu**, **Açık – Sürmekte(690,970,000)** daha yüksek bir duruma değiştikten sonra, **Harici Proje** alanı kilitlenir ve değeri artık ekleyemez, kaldıramaz veya değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4aa96-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="4aa96-128">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="4aa96-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="4aa96-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4aa96-129">Finance and Operations</span></span>
<span data-ttu-id="4aa96-130">Veri varlığı projeleri için izlemeyi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="4aa96-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4aa96-131">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="4aa96-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="4aa96-132">Projeler (Fin and Ops'tan Field Service'a): Projeler</span><span class="sxs-lookup"><span data-stu-id="4aa96-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="4aa96-133">[![Veri tümleştirmede şablon eşleme](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="4aa96-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
