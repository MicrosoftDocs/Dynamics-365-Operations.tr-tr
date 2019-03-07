---
title: Field Service'tan Finance and Operations'a projeli iş emirleri eşitleme
description: Bu konu iş emirlerini Microsoft Dynamics 365 for Field Service bir proje numarasına üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "329862"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="baf2c-103">Field Service'tan Finance and Operations'a projeli iş emirleri eşitleme</span><span class="sxs-lookup"><span data-stu-id="baf2c-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="baf2c-104">Bu konu iş emirlerini Microsoft Dynamics 365 for Field Service bir proje numarasına üzerinden Microsoft Dynamics 365 for Finance and Operations üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.</span><span class="sxs-lookup"><span data-stu-id="baf2c-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="baf2c-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="baf2c-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="baf2c-106">Kullanılan **Field Service Ürünleri (Finance and Operations'tan Field Service'a)** şablonu Müşteri Adayından Nakde'deki **Ürünler (Finance and Operations'tan Sales'e) – Doğrudan** şablonunu temel alır.</span><span class="sxs-lookup"><span data-stu-id="baf2c-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="baf2c-107">Daha fazla bilgi için bkz. [Ürünler (Finance and Operations'tan Sales'e) – Doğrudan](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="baf2c-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="baf2c-108">Bu konu yalnızca **Field Service Ürünleri (Finance and Operations'tan Field Service'a)** ile **Field Service Ürünleri (Finance and Operations'tan Sales'e)** şablonları arasındaki farkları açıklar.</span><span class="sxs-lookup"><span data-stu-id="baf2c-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="baf2c-109">Bu şablonun dahil ettiği ana fark, Field Service'ta İş emrine atanmış proje numarası olmasıdır ve bu, Finance and Operations'ta oluşturulan Satış siparişlerinin, proje numarasını dahil etmesi gerektiği anlamına gelir ve bu ilgili projede gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="baf2c-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="baf2c-110">Bunun yanı sıra, bu şablon Gelişmiş Sorgu ve Filtreleme kullanır.</span><span class="sxs-lookup"><span data-stu-id="baf2c-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="baf2c-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="baf2c-111">Templates and tasks</span></span>

<span data-ttu-id="baf2c-112">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="baf2c-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="baf2c-113">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a)</span><span class="sxs-lookup"><span data-stu-id="baf2c-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="baf2c-114">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="baf2c-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="baf2c-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="baf2c-115">WorkOrderHeader</span></span>
- <span data-ttu-id="baf2c-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="baf2c-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="baf2c-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="baf2c-117">WorkOrderProduct</span></span>
- <span data-ttu-id="baf2c-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="baf2c-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="baf2c-119">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="baf2c-119">Field Service CRM solution</span></span>
<span data-ttu-id="baf2c-120">**Harici Proje** alanı, İş Emri varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="baf2c-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="baf2c-121">Bu alan, bir arama ve İş Emrinizi bir proje ile etiketleyerek, Satış Siparişi daha sonra Finance and Operations içindeki bir Projeye bağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="baf2c-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="baf2c-122">**Sistem Durumu** açık'tan değişenler – Sürmekte(690,970,000) daha yüksek bir durum **Harici Proje** alanı kilitlenir ve değeri ekleyemez, kaldıramaz veya değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="baf2c-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="baf2c-123">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="baf2c-123">Template mapping in Data integration</span></span>

<span data-ttu-id="baf2c-124">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="baf2c-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="baf2c-125">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="baf2c-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="baf2c-126">[![Veri tümleştirmede şablon eşleme](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="baf2c-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="baf2c-127">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="baf2c-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="baf2c-128">[![Veri tümleştirmede şablon eşleme](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="baf2c-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="baf2c-129">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="baf2c-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="baf2c-130">[![Veri tümleştirmede şablon eşleme](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="baf2c-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="baf2c-131">Proje İle İş Emirleri (Field Service'tan Finance and Operations'a): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="baf2c-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="baf2c-132">[![Veri tümleştirmede şablon eşleme](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="baf2c-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
