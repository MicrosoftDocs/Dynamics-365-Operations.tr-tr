---
title: Proje listesini Supply Chain Management'tan Field Service'e eşitleme
description: Bu konu projeleri Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3d17b226cabd0668bcdb52e9a7fdfc5973fe49b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243069"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="dab12-103">Proje listesini Supply Chain Management'tan Field Service'e eşitleme</span><span class="sxs-lookup"><span data-stu-id="dab12-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dab12-104">Bu konu projeleri Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="dab12-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="dab12-105">[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="dab12-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="dab12-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="dab12-106">Templates and tasks</span></span>
<span data-ttu-id="dab12-107">Aşağıdaki şablon ve temel görevler, projelerin Supply Chain Management'tan Field Service'e eşitlemesini çalıştırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dab12-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="dab12-108">**Veri Tümleştirmesindeki Şablon**</span><span class="sxs-lookup"><span data-stu-id="dab12-108">**Template in Data integration**</span></span>
- <span data-ttu-id="dab12-109">Projeler (Supply Chain Management'tan Field Service'e)</span><span class="sxs-lookup"><span data-stu-id="dab12-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="dab12-110">**Veri tümleştirme projesindeki görev**</span><span class="sxs-lookup"><span data-stu-id="dab12-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="dab12-111">Projeler</span><span class="sxs-lookup"><span data-stu-id="dab12-111">Projects</span></span>

<span data-ttu-id="dab12-112">Aşağıdaki eşitleme görevlerinin, proje listesinin eşitlemesinin gerçekleştirilebilmesi için gereklidir:</span><span class="sxs-lookup"><span data-stu-id="dab12-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="dab12-113">Hesaplar (Sales'den Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="dab12-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="dab12-114">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="dab12-114">Entity set</span></span>
| <span data-ttu-id="dab12-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="dab12-115">Field Service</span></span>           | <span data-ttu-id="dab12-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dab12-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="dab12-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="dab12-117">msdynce_externalprojects</span></span> | <span data-ttu-id="dab12-118">Projeler</span><span class="sxs-lookup"><span data-stu-id="dab12-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="dab12-119">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="dab12-119">Entity flow</span></span>
<span data-ttu-id="dab12-120">Projeler Supply Chain Management'ta oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dab12-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="dab12-121">**Proje türü**, **Zaman ve malzeme**'ye ayarlanır ve **Proje aşaması**, **İşlevde olan** projelere ayarlanır, Field Service'ta **Harici Proje** varlığına eşitlenir, Proje numarası, Proje adı, Proje aşaması ve Müşteri hesap bilgisi de dahil.</span><span class="sxs-lookup"><span data-stu-id="dab12-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="dab12-122">**Harici Proje** listesi, Field Service iş emirlerini Supply Chain Management projeleriyle eşleştirmede kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dab12-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="dab12-123">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="dab12-123">Field Service CRM solution</span></span>
<span data-ttu-id="dab12-124">**Harici Proje** varlığı, tüm projeleri Supply Chain Management'tan alır.</span><span class="sxs-lookup"><span data-stu-id="dab12-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="dab12-125">**Harici Proje** alanı, **İş Emri** varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="dab12-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="dab12-126">Bu bir arama alanıdır ve bu yüzden, iş emrinizi bir proje ile etiketleyerek, satış siparişi Supply Chain Management içindeki bir projeye bağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="dab12-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="dab12-127">**Sistem Durumu**, **Açık – Sürmekte(690,970,000)** daha yüksek bir duruma değiştikten sonra, **Harici Proje** alanı kilitlenir ve değeri artık ekleyemez, kaldıramaz veya değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="dab12-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="dab12-128">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="dab12-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="dab12-129">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dab12-129">Supply Chain Management</span></span>
<span data-ttu-id="dab12-130">Veri varlığı projeleri için izlemeyi etkinleştir</span><span class="sxs-lookup"><span data-stu-id="dab12-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dab12-131">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="dab12-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="dab12-132">Projeler (Supply Chain Management'tan Field Service'e): Projeler</span><span class="sxs-lookup"><span data-stu-id="dab12-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="dab12-133">[![Veri tümleştirmede şablon eşleme](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="dab12-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]