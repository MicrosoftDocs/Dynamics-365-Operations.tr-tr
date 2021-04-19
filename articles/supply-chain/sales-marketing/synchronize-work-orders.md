---
title: Proje içeren iş emirlerini Field Service'ten Supply Chain Management'a eşitleme
description: Bu konu iş emirlerini Dynamics 365 Field Service bir proje numarasına üzerinden Dynamics 365 Supply Chain Management üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.
author: ChristianRytt
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d733bf3256fa1f6c572bd0aa35c228490d409bbc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836506"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="4f8ec-103">Proje içeren iş emirlerini Field Service'ten Supply Chain Management'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="4f8ec-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4f8ec-104">Bu konu iş emirlerini Dynamics 365 Field Service bir proje numarasına üzerinden Dynamics 365 Supply Chain Management üzerine eşitlemekte kullanılan şablonları ve alttaki görevi açıklar.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="4f8ec-105">[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="4f8ec-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="4f8ec-106">Kullanılan **Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a)** şablonu, **İş Emirleri (Field Service'ten Supply Chain Management'a)** şablonuna dayanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="4f8ec-107">Daha fazla bilgi için bkz. [Field Service'teki iş emirlerini Supply Chain Management'taki satış siparişlerine eşitleme](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="4f8ec-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="4f8ec-108">Bu konu, yalnızca iki şablon arasındaki farkı açıklar:</span><span class="sxs-lookup"><span data-stu-id="4f8ec-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="4f8ec-109">**Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a)**</span><span class="sxs-lookup"><span data-stu-id="4f8ec-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="4f8ec-110">**İş Emirleri (Field Service'ten Supply Chain Management'a)**</span><span class="sxs-lookup"><span data-stu-id="4f8ec-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="4f8ec-111">Bu şablonun dahil ettiği ana fark, Field Service'ta İş emrine atanmış proje numarası olmasıdır ve bu, Supply Chain Management'ta oluşturulan Satış siparişlerinin, proje numarasını dahil etmesi gerektiği anlamına gelir ve bu ilgili projede gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="4f8ec-112">Bunun yanı sıra, bu şablon Gelişmiş Sorgu ve Filtreleme kullanır.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4f8ec-113">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="4f8ec-113">Templates and tasks</span></span>

<span data-ttu-id="4f8ec-114">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="4f8ec-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="4f8ec-115">Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="4f8ec-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="4f8ec-116">**Veri tümleştirme projesindeki görevin adı:**</span><span class="sxs-lookup"><span data-stu-id="4f8ec-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="4f8ec-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="4f8ec-117">WorkOrderHeader</span></span>
- <span data-ttu-id="4f8ec-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="4f8ec-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="4f8ec-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="4f8ec-119">WorkOrderProduct</span></span>
- <span data-ttu-id="4f8ec-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="4f8ec-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="4f8ec-121">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="4f8ec-121">Field Service CRM solution</span></span>
<span data-ttu-id="4f8ec-122">**Harici Proje** alanı, İş Emri varlığına eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="4f8ec-123">Bu alan, bir arama ve İş Emrinizi bir proje ile etiketleyerek, Satış Siparişi daha sonra Supply Chain Management içindeki bir Projeye bağlanacaktır.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="4f8ec-124">**Sistem Durumu** Açık – Devam Ediyor'dan (690,970,000) daha yüksek bir duruma geçince **Harici Proje** alanı kilitlenir ve değeri ekleyemez, kaldıramaz veya değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4f8ec-125">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="4f8ec-125">Template mapping in Data integration</span></span>

<span data-ttu-id="4f8ec-126">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f8ec-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="4f8ec-127">Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="4f8ec-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="4f8ec-128">[![Veri tümleştirmede şablon eşleme](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="4f8ec-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="4f8ec-129">Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="4f8ec-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="4f8ec-130">[![Veri tümleştirmede şablon eşleme](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="4f8ec-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="4f8ec-131">Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="4f8ec-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="4f8ec-132">[![Veri tümleştirmede şablon eşleme](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="4f8ec-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="4f8ec-133">Proje İçeren İş Emirleri (Field Service'ten Supply Chain Management'a): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="4f8ec-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="4f8ec-134">[![Veri tümleştirmede şablon eşleme](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="4f8ec-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]