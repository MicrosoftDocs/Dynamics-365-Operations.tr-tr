---
title: Finance and Operations'tan Field Service'a ambarları eşitleme
description: Bu konu ambarları Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 7e6d7626c00b9d7d98ce872652653c36ce7bc975
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "842545"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="afdd6-103">Ambarları Finance and Operations'dan Field Service'a eşitleme</span><span class="sxs-lookup"><span data-stu-id="afdd6-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="afdd6-104">Bu konu ambarları Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="afdd6-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="afdd6-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="afdd6-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="afdd6-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="afdd6-106">Templates and tasks</span></span>
<span data-ttu-id="afdd6-107">Aşağıdaki şablon ve görevler, Microsoft Dynamics 365 for Finance and Operations üzerinden Microsoft Dynamics 365 for Field Service üzerine ambarların eşitlenmesinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="afdd6-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="afdd6-108">**Veri Tümleştirmesindeki Şablon**</span><span class="sxs-lookup"><span data-stu-id="afdd6-108">**Template in Data integration**</span></span>
- <span data-ttu-id="afdd6-109">Ambarlar (Fin and Ops'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="afdd6-109">Warehouses (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="afdd6-110">**Veri tümleştirme projesindeki görev**</span><span class="sxs-lookup"><span data-stu-id="afdd6-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="afdd6-111">Ambar</span><span class="sxs-lookup"><span data-stu-id="afdd6-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="afdd6-112">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="afdd6-112">Entity set</span></span>
| <span data-ttu-id="afdd6-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="afdd6-113">Field Service</span></span>    | <span data-ttu-id="afdd6-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="afdd6-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="afdd6-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="afdd6-115">msdyn_warehouses</span></span> | <span data-ttu-id="afdd6-116">Ambarlar</span><span class="sxs-lookup"><span data-stu-id="afdd6-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="afdd6-117">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="afdd6-117">Entity flow</span></span>
<span data-ttu-id="afdd6-118">Finance and Operations'taki oluşturulan ve korunan ambarlar Field Service'a br Common Data Service (CDS) Veri tümleştirme projesi aracılığıyla Finance and Operations ile eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="afdd6-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="afdd6-119">Field Service'a eşitlemek istediğiniz ambarlar, proje üzerinde Gelişmiş sorgu ve filtreleme ile kontrol edilebilirler.</span><span class="sxs-lookup"><span data-stu-id="afdd6-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="afdd6-120">Finance and Operations'tan eşitlenen ambarlar, **Harici olarak korunuyor** alanının **Evet** olarak ayarlandığı ve kaydın salt okunur olduğu şekilde Field Service için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="afdd6-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="afdd6-121">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="afdd6-121">Field Service CRM solution</span></span>
<span data-ttu-id="afdd6-122">Field Service ile Finance and Operations arasında tümleştirmeyi desteklemek için, Field Service CRM çözümündeki ek işlev gereklidir.</span><span class="sxs-lookup"><span data-stu-id="afdd6-122">To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="afdd6-123">Çözümde, **Harici Korunuyor** alanı, **Ambar (msdyn_warehouses)** varlığına eklendi.</span><span class="sxs-lookup"><span data-stu-id="afdd6-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="afdd6-124">Bu alan, ambarın Finance and Operations'tan mı yönetildiğini yoksa yalnızca Field Service'ta mı mevcut olduğunu tanımlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="afdd6-124">This field helps to identify if the warehouse is handled from Finance and Operations or if it only exists in Field Service.</span></span> <span data-ttu-id="afdd6-125">Bu alan için ayarlara şunlar dahildir:</span><span class="sxs-lookup"><span data-stu-id="afdd6-125">The settings for this field include:</span></span>
- <span data-ttu-id="afdd6-126">**Evet** – Ambar, Finance and Operations'tan gelir ve Sales'ta düzenlenebilir olmaz.</span><span class="sxs-lookup"><span data-stu-id="afdd6-126">**Yes** – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="afdd6-127">**Hayır** – Ambar, doğrudan Field Service'a girildi ve burada tutuluyor.</span><span class="sxs-lookup"><span data-stu-id="afdd6-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="afdd6-128">**Harici Korunuyor** alanı, iş emirlerindeki stok düzeylerinin, ayarlamaların, aktarmaların ve kullanımın eşitlemesini kontrol etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="afdd6-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="afdd6-129">Yalnızca **Harici Korunan ambarlar**, **Evet** olarak ayarlanır, diğer sistemdeki aynı ambara doğrudan eşitlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="afdd6-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="afdd6-130">Field Service'ta birden fazla ambar (**Harici Korunan** = Hayır) oluşturmak ve bunları Finance and Operations içinde tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür.</span><span class="sxs-lookup"><span data-stu-id="afdd6-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="afdd6-131">Bu, Field Service'ın ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri Finance and Operations'a göndermesini istediğiniz durumlarda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="afdd6-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="afdd6-132">Bu durumda, Field Service, Finance and Operations'tan stok düzeyi güncelleştirmeleri almayacaktır.</span><span class="sxs-lookup"><span data-stu-id="afdd6-132">In this case, Field Service will not receive inventory-level updates from Finance and Operations.</span></span> <span data-ttu-id="afdd6-133">Daha fazla bilgi için bkz. [Field Service'tan Finance and Operations'a stok ayarlamalarını eşitlemede](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ve [Finance and Operations içinde projelere bağlantılı satış siparişlerini Field Service iş emirlerine eşitlemek](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="afdd6-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="afdd6-134">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="afdd6-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="afdd6-135">Veri Tümleştirme projesi</span><span class="sxs-lookup"><span data-stu-id="afdd6-135">Data Integration project</span></span>
<span data-ttu-id="afdd6-136">Ambarların eşitlenmesinden önce, Gelişmiş sorgu ve filtrelemenin proje üzerinde yalnızca Finance and Operations'tan Field Service'a getirdiğiniz ambarları dahil ettiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="afdd6-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="afdd6-137">İş emirleri, ayarlamalar ve aktarmalarda uygulayabilmek için ambara Field Service'ta ihtiyacınız olacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="afdd6-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="afdd6-138">**msdyn_warehouses** için **Tümleştirme anahtarı** bulunduğundan emin olmak için:</span><span class="sxs-lookup"><span data-stu-id="afdd6-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="afdd6-139">Veri Tümleştirme'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="afdd6-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="afdd6-140">**Bağlantı Kümesi** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="afdd6-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="afdd6-141">İş emri eşitlemede kullanılacak bağlantı kümesini seçin.</span><span class="sxs-lookup"><span data-stu-id="afdd6-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="afdd6-142">**Tümleştirme anahtarı** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="afdd6-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="afdd6-143">msdyn_warehouses öğesini bulun ve **msdyn_name (adı)** anahtarının eklendiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="afdd6-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="afdd6-144">Görünmüyorsa, **Anahtar ekle**'ye tıklayarak ekleyin ve sonra sayfanın üst kısmındaki **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="afdd6-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="afdd6-145">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="afdd6-145">Template mapping in Data integration</span></span>

<span data-ttu-id="afdd6-146">Aşağıdaki görsel, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="afdd6-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a><span data-ttu-id="afdd6-147">Ambarlar (Fin and Ops'tan Field Service'a): Ambar</span><span class="sxs-lookup"><span data-stu-id="afdd6-147">Warehouses (Fin and Ops to Field Service): Warehouse</span></span>

<span data-ttu-id="afdd6-148">[![Veri tümleştirmede şablon eşleme](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="afdd6-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
