---
title: Field Service'tan Finance and Operations'a projeli iş emirleri eşitleme
description: Bu konu iş emirlerini Microsoft Dynamics 365 for Field Service bir proje numarasına üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843421"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="337e2-103">Field Service'tan Finance and Operations'a projeli iş emirleri eşitleme</span><span class="sxs-lookup"><span data-stu-id="337e2-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="337e2-104">Bu konu iş emirlerini Microsoft Dynamics 365 for Field Service bir proje numarasına üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.</span><span class="sxs-lookup"><span data-stu-id="337e2-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="337e2-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="337e2-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="337e2-106">Kullanılan **İş Emirleri Proje ile (Field Service'ten Fin and Ops'a)** şablonu, **İş Emirleri (Field Service to Fin and Ops)** şablonuna dayanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="337e2-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="337e2-107">Dah af azla bilgi için bkz. [Field Service'daki iş emirlerini Finance and Operations'taki satış siparişleriyle eşitleme](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="337e2-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="337e2-108">Bu konu, yalnızca iki şablon arasındaki farkı açıklar:</span><span class="sxs-lookup"><span data-stu-id="337e2-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="337e2-109">**Proje İle İş Emirleri (Field Service'tan Fin and Ops'a)**</span><span class="sxs-lookup"><span data-stu-id="337e2-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="337e2-110">**Proje Emirleri (Field Service'tan Fin and Ops'a)**</span><span class="sxs-lookup"><span data-stu-id="337e2-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="337e2-111">Bu şablonun dahil ettiği ana fark, Field Service'ta İş emrine atanmış proje numarası olmasıdır ve bu, Finance and Operations'ta oluşturulan Satış siparişlerinin, proje numarasını dahil etmesi gerektiği anlamına gelir ve bu ilgili projede gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="337e2-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="337e2-112">Bunun yanı sıra, bu şablon Gelişmiş Sorgu ve Filtreleme kullanır.</span><span class="sxs-lookup"><span data-stu-id="337e2-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="337e2-113">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="337e2-113">Templates and tasks</span></span>

<span data-ttu-id="337e2-114">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="337e2-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="337e2-115">Proje İle İş Emirleri (Field Service'tan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="337e2-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="337e2-116">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="337e2-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="337e2-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="337e2-117">WorkOrderHeader</span></span>
- <span data-ttu-id="337e2-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="337e2-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="337e2-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="337e2-119">WorkOrderProduct</span></span>
- <span data-ttu-id="337e2-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="337e2-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="337e2-121">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="337e2-121">Field Service CRM solution</span></span>
<span data-ttu-id="337e2-122">**Harici Proje** alanı, İş Emri varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="337e2-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="337e2-123">Bu alan, bir arama ve İş Emrinizi bir proje ile etiketleyerek, Satış Siparişi daha sonra Finance and Operations içindeki bir Projeye bağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="337e2-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="337e2-124">**Sistem Durumu** açık'tan değişenler – Sürmekte(690,970,000) daha yüksek bir durum **Harici Proje** alanı kilitlenir ve değeri ekleyemez, kaldıramaz veya değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="337e2-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="337e2-125">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="337e2-125">Template mapping in Data integration</span></span>

<span data-ttu-id="337e2-126">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="337e2-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="337e2-127">Proje İle İş Emirleri (Field Service'tan Fin and Ops'a): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="337e2-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="337e2-128">[![Veri tümleştirmede şablon eşleme](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="337e2-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="337e2-129">Proje İle İş Emirleri (Field Service'tan Fin and Ops'a): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="337e2-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="337e2-130">[![Veri tümleştirmede şablon eşleme](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="337e2-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="337e2-131">Proje İle İş Emirleri (Field Service'tan Fin and Ops'a): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="337e2-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="337e2-132">[![Veri tümleştirmede şablon eşleme](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="337e2-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="337e2-133">Proje İle İş Emirleri (Field Service'tan Fin and Ops'a): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="337e2-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="337e2-134">[![Veri tümleştirmede şablon eşleme](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="337e2-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
