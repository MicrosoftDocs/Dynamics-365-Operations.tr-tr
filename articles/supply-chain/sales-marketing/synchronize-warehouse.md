---
title: Ambarları Supply Chain Management'tan Field Service'e eşitleme
description: Bu konu ambarları Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
author: ChristianRytt
ms.date: 03/13/2019
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
ms.openlocfilehash: f302f780fa8ba3d387a71770024a1bf7ad42c4ef
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910277"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="3a377-103">Ambarları Supply Chain Management'tan Field Service'e eşitleme</span><span class="sxs-lookup"><span data-stu-id="3a377-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3a377-104">Bu konu ambarları Dynamics 365 Supply Chain Management üzerinden Dynamics 365 Field Service üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="3a377-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="3a377-105">[![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="3a377-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3a377-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="3a377-106">Templates and tasks</span></span>
<span data-ttu-id="3a377-107">Aşağıdaki şablon ve temel görevler, ambarların Supply Chain Management'tan Field Service'e eşitlemesini çalıştırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3a377-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="3a377-108">**Veri Tümleştirmesindeki Şablon**</span><span class="sxs-lookup"><span data-stu-id="3a377-108">**Template in Data integration**</span></span>
- <span data-ttu-id="3a377-109">Ambarlar (Supply Chain Management'tan Field Service'e)</span><span class="sxs-lookup"><span data-stu-id="3a377-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="3a377-110">**Veri tümleştirme projesindeki görev**</span><span class="sxs-lookup"><span data-stu-id="3a377-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="3a377-111">Ambar</span><span class="sxs-lookup"><span data-stu-id="3a377-111">Warehouse</span></span>

## <a name="table-set"></a><span data-ttu-id="3a377-112">Tablo kümesi</span><span class="sxs-lookup"><span data-stu-id="3a377-112">Table set</span></span>
| <span data-ttu-id="3a377-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="3a377-113">Field Service</span></span>    | <span data-ttu-id="3a377-114">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3a377-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="3a377-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="3a377-115">msdyn_warehouses</span></span> | <span data-ttu-id="3a377-116">Ambarlar</span><span class="sxs-lookup"><span data-stu-id="3a377-116">Warehouses</span></span>                             |

## <a name="table-flow"></a><span data-ttu-id="3a377-117">Tablo akışı</span><span class="sxs-lookup"><span data-stu-id="3a377-117">Table flow</span></span>
<span data-ttu-id="3a377-118">Supply Chain Management'ta oluşturulan ve korunan ambarlar, Field Service'e bir Microsoft Dataverse Veri tümleştirme projesi aracılığıyla eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="3a377-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="3a377-119">Field Service'a eşitlemek istediğiniz ambarlar, proje üzerinde Gelişmiş sorgu ve filtreleme ile kontrol edilebilirler.</span><span class="sxs-lookup"><span data-stu-id="3a377-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="3a377-120">Supply Chain Management'tan eşitlenen ambarlar, **Harici olarak korunur** sütununun **Evet** olarak ayarlandığı ve kaydın salt okunur olduğu şekilde Field Service'te oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3a377-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** column set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="3a377-121">Field Service CRM çözümü</span><span class="sxs-lookup"><span data-stu-id="3a377-121">Field Service CRM solution</span></span>
<span data-ttu-id="3a377-122">Field Service ile Supply Chain Management arasında tümleştirmeyi desteklemek için, Field Service CRM çözümündeki ek işlev gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3a377-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="3a377-123">Çözümde, **Harici Olarak Korunur** sütunu, **Ambar (msdyn_warehouses)** tablosuna eklendi.</span><span class="sxs-lookup"><span data-stu-id="3a377-123">In the solution, the **Is Maintained Externally** column has been added to the **Warehouse (msdyn_warehouses)** table.</span></span> <span data-ttu-id="3a377-124">Bu sütun, ambarın Supply Chain Management'tan mı yönetildiğini yoksa yalnızca Field Service'te mi var olduğunu belirlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3a377-124">This column helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="3a377-125">Bu sütunun ayarları arasında aşağıdakiler yer alır:</span><span class="sxs-lookup"><span data-stu-id="3a377-125">The settings for this column include:</span></span>
- <span data-ttu-id="3a377-126">**Evet** – Ambar, Supply Chain Management kaynaklıdır ve Sales'te düzenlenemez.</span><span class="sxs-lookup"><span data-stu-id="3a377-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="3a377-127">**Hayır** – Ambar, doğrudan Field Service'a girildi ve burada tutuluyor.</span><span class="sxs-lookup"><span data-stu-id="3a377-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="3a377-128">**Harici Olarak Korunur** sütunu, iş emirlerindeki stok düzeylerinin, ayarlamaların, aktarmaların ve kullanımın eşitlemesini kontrol etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="3a377-128">The **Is Externally Maintained** column helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="3a377-129">Yalnızca **Harici Korunan ambarlar**, **Evet** olarak ayarlanır, diğer sistemdeki aynı ambara doğrudan eşitlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3a377-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="3a377-130">Field Service'ta birden fazla ambar (**Harici Korunan** = Hayır) oluşturmak ve bunları tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür.</span><span class="sxs-lookup"><span data-stu-id="3a377-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="3a377-131">Bu, Field Service'in ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri yalnızca Supply Chain Management'a göndermesini istediğiniz durumlarda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3a377-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="3a377-132">Bu durumda, Field Service, Supply Chain Management'tan stok düzeyi güncelleştirmeleri almayacaktır.</span><span class="sxs-lookup"><span data-stu-id="3a377-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="3a377-133">Daha fazla bilgi için bkz. [Field Service'tan Finance and Operations'a stok ayarlamalarını eşitleme](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ve [Field Service'taki iş emirlerini Finance and Operations'taki projeye bağlantısı olan satış siparişlerine eşitleme](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="3a377-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="3a377-134">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="3a377-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="3a377-135">Veri Tümleştirme projesi</span><span class="sxs-lookup"><span data-stu-id="3a377-135">Data Integration project</span></span>
<span data-ttu-id="3a377-136">Ambarların eşitlenmesinden önce, Gelişmiş sorgu ve filtrelemenin proje üzerinde yalnızca Supply Chain Management'tan Field Service'e getirdiğiniz ambarları dahil ettiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="3a377-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="3a377-137">İş emirleri, ayarlamalar ve aktarmalarda uygulayabilmek için ambara Field Service'ta ihtiyacınız olacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3a377-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="3a377-138">**msdyn_warehouses** için **Tümleştirme anahtarı** bulunduğundan emin olmak için:</span><span class="sxs-lookup"><span data-stu-id="3a377-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="3a377-139">Veri Tümleştirme'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="3a377-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="3a377-140">**Bağlantı Kümesi** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3a377-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="3a377-141">İş emri eşitlemede kullanılacak bağlantı kümesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3a377-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="3a377-142">**Tümleştirme anahtarı** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="3a377-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="3a377-143">msdyn_warehouses öğesini bulun ve **msdyn_name (adı)** anahtarının eklendiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="3a377-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="3a377-144">Görünmüyorsa, **Anahtar ekle**'ye tıklayarak ekleyin ve sonra sayfanın üst kısmındaki **Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a377-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3a377-145">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="3a377-145">Template mapping in Data integration</span></span>

<span data-ttu-id="3a377-146">Aşağıdaki görsel, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a377-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="3a377-147">Ambarlar (Supply Chain Management'tan Field Service'e): Ambar</span><span class="sxs-lookup"><span data-stu-id="3a377-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="3a377-148">[![Veri tümleştirmede şablon eşleme](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="3a377-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]