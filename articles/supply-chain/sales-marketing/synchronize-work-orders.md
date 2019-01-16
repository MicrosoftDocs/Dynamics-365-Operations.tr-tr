---
title: "Finance and Operations'tan Field Service'a iş emirleri eşitleme"
description: "Bu konu, proje numaralı iş emirlerini Microsoft Dynamics 365 for Field Service'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: tr-tr
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="157ef-103">Field Service'tan Finance and Operations'a projeli iş emirleri eşitleme</span><span class="sxs-lookup"><span data-stu-id="157ef-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="157ef-104">Bu konu, proje numaralı iş emirlerini Microsoft Dynamics 365 for Field Service'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="157ef-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="157ef-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="157ef-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="157ef-106">Kullanılan **Field Service Ürünleri (Finance and Operations'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Finance and Operations'tan Sales'e) – Doğrudan** şablonunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="157ef-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="157ef-107">Daha fazla bilgi için bkz. [Ürünler (Finance and Operations'tan Sales'e) – Doğrudan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="157ef-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="157ef-108">Bu konu yalnızca **Field Service Ürünleri (Finance and Operations'tan Field Service'a)** ile **Field Service Ürünleri (Finance and Operations'tan Sales'e)** şablonları arasındaki farkları açıklar.</span><span class="sxs-lookup"><span data-stu-id="157ef-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="157ef-109">Bu şablonun dahil ettiği ana fark, Field Service'ta İş emrine atanmış proje numarası olmasıdır ve bu, Finance and Operations'ta oluşturulan Satış siparişlerinin, proje numarasını dahil etmesi gerektiği anlamına gelir ve bu ilgili projede gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="157ef-109">The main difference is that this template include mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="157ef-110">Bunun yanı sıra, bu şablon Gelişmiş Sorgu ve Filtreleme kullanır.</span><span class="sxs-lookup"><span data-stu-id="157ef-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="157ef-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="157ef-111">Templates and tasks</span></span>

<span data-ttu-id="157ef-112">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="157ef-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="157ef-113">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a)</span><span class="sxs-lookup"><span data-stu-id="157ef-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="157ef-114">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="157ef-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="157ef-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="157ef-115">WorkOrderHeader</span></span>
- <span data-ttu-id="157ef-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="157ef-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="157ef-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="157ef-117">WorkOrderProduct</span></span>
- <span data-ttu-id="157ef-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="157ef-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="157ef-119">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="157ef-119">Field Service CRM solution</span></span>
<span data-ttu-id="157ef-120">**Harici Proje** alanı, İş Emri varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="157ef-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="157ef-121">Bu alan, bir arama ve İş Emrinizi bir proje ile etiketleyerek, Satış Siparişi daha sonra Finance and Operations içindeki bir Projeye bağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="157ef-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="157ef-122">**Sistem Durumu** açık'tan değişenler – Sürmekte(690,970,000) daha yüksek bir durum **Harici Proje** alanı kilitlenir ve değeri ekleyemez, kaldıramaz veya değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="157ef-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="157ef-123">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="157ef-123">Template mapping in Data integration</span></span>

<span data-ttu-id="157ef-124">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="157ef-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="157ef-125">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="157ef-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="157ef-126">[![Veri tümleştirmede şablon eşleme](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="157ef-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="157ef-127">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="157ef-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="157ef-128">[![Veri tümleştirmede şablon eşleme](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="157ef-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="157ef-129">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="157ef-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="157ef-130">[![Veri tümleştirmede şablon eşleme](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="157ef-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="157ef-131">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="157ef-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="157ef-132">[![Veri tümleştirmede şablon eşleme](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="157ef-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>

