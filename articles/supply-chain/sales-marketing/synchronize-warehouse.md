---
title: "Finance and Operations'tan Field Service'a ambarları eşitleme"
description: "Bu konu, ambarları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevlerini ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
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
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: tr-tr
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="e8f72-103">Finance and Operations'tan Field Service'a ambarları eşitleme</span><span class="sxs-lookup"><span data-stu-id="e8f72-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e8f72-104">Bu konu, ambarları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemek için altta yatan görevlerini ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="e8f72-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e8f72-105">[![Finance and Operations ile Field Service arasında iş süreçlerini eşitleme](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="e8f72-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e8f72-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="e8f72-106">Templates and tasks</span></span>
<span data-ttu-id="e8f72-107">Aşağıdaki şablon ve görevleri, ambarları Microsoft Dynamics 365 for Finance and Operations'tan Microsoft Dynamics 365 for Field Service'a eşitlemeyi açıklar.</span><span class="sxs-lookup"><span data-stu-id="e8f72-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="e8f72-108">**Veri tümleştirmesindeki şablonun adı:**</span><span class="sxs-lookup"><span data-stu-id="e8f72-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="e8f72-109">Ambarlar (Finance and Operations'tan Field Service'a)</span><span class="sxs-lookup"><span data-stu-id="e8f72-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="e8f72-110">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="e8f72-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="e8f72-111">Ambar</span><span class="sxs-lookup"><span data-stu-id="e8f72-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="e8f72-112">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="e8f72-112">Entity set</span></span>
| <span data-ttu-id="e8f72-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="e8f72-113">Field Service</span></span>    | <span data-ttu-id="e8f72-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e8f72-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="e8f72-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="e8f72-115">msdyn_warehouses</span></span> | <span data-ttu-id="e8f72-116">Ambarlar</span><span class="sxs-lookup"><span data-stu-id="e8f72-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="e8f72-117">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="e8f72-117">Entity flow</span></span>
<span data-ttu-id="e8f72-118">Finance and Operations'taki oluşturulan ve korunan ambarlar Field Service'a br Common Data Service (CDS) Veri tümleştirme projesi aracılığıyla Finance and Operations ile eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="e8f72-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="e8f72-119">Field Service'a eşitlenen istenen ambarlar, proje üzerinde Gelişmiş sorgu ve filtreleme ile kontrol edilebilirler.</span><span class="sxs-lookup"><span data-stu-id="e8f72-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="e8f72-120">Finance and Operations'tan eşitlenen ambarlar, Harici olarak korunuyor alanının Evet olarak ayarlandığı ve kaydın salt okunur olduğu şekilde Field Service için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e8f72-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="e8f72-121">Field Service CRM çözümü Field Service ile Finance and Operations arasında tümleştirmeyi desteklemek için, Field Service CRM çözümündeki ek işlev gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e8f72-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="e8f72-122">Çözüm aşağıdaki değişiklikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="e8f72-122">The solution includes the following changes.</span></span>
<span data-ttu-id="e8f72-123">**Harici Korunuyor** alanı, **Ambar (msdyn_warehouses)** varlığına eklendi.</span><span class="sxs-lookup"><span data-stu-id="e8f72-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="e8f72-124">Bu alan, Ambarın Operations'tan mı yönetildiğini yoksa yalnızca Field Service'ta mı mevcut olduğunu tanımlamaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e8f72-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="e8f72-125">Evet – Ambar, Finance and Operations'tan gelir ve Sales'ta düzenlenebilir olmaz.</span><span class="sxs-lookup"><span data-stu-id="e8f72-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="e8f72-126">Hayır – Ambar, doğrudan Field Service'a girildi ve burada tutuluyor.</span><span class="sxs-lookup"><span data-stu-id="e8f72-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="e8f72-127">**Harici Korunuyor** alanı, iş emirlerindeki stok düzeylerinin, ayarlamaların, aktarmaların ve kullanımın eşitlemesini kontrol etmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e8f72-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="e8f72-128">Yalnızca **Harici Korunan** ambarlar = Evet, diğer sistemdeki aynı ambara doğrudan eşitlemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e8f72-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="e8f72-129">Not: Field Service'ta birden fazla ambar (**Harici Korunan** = Hayır) oluşturmak ve bunları Finance and Operations içinde tek bir ambara eşleştirmek Gelişmiş sorgu ve filtreleme özelliği ile mümkündür.</span><span class="sxs-lookup"><span data-stu-id="e8f72-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="e8f72-130">Bu, Field Service'ın ayrıntılı stok düzeylerini üstlenmesi ve sadece güncelleştirmeleri Finance and Operations'a göndermesini istediğiniz durumlarda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e8f72-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="e8f72-131">Bu durumda Field Service, Finance and Operations'tan stok düzeyi güncelleştirmeleri almayacaktır.</span><span class="sxs-lookup"><span data-stu-id="e8f72-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="e8f72-132">Field Service'tan Finance and Operations'a stok ayarlamalarını eşitlemede ve Finance and Operations içinde projelere bağlantılı satış siparişlerini Field Service iş emirlerine eşitlemek istiyorsanız ek bilgiye bakın.</span><span class="sxs-lookup"><span data-stu-id="e8f72-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e8f72-133">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="e8f72-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="e8f72-134">Veri Tümleştirme projesinde</span><span class="sxs-lookup"><span data-stu-id="e8f72-134">In the Data Integration project</span></span>
<span data-ttu-id="e8f72-135">Ambarların eşitlenmesinden önce, Gelişmiş sorgu ve filtrelemenin proje üzerinde yalnızca Finance and Operations'tan Field Service'a getirdiğiniz ambarları dahil ettiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="e8f72-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="e8f72-136">İş emirleri, ayarlamalar ve aktarmalarda uygulayabilmek için ambara Field Service'ta ihtiyacınız olacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="e8f72-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="e8f72-137">**msdyn_warehouses** için **Tümleştirme anahtarı** bulunduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="e8f72-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="e8f72-138">Veri Tümleştirme'ye gidin</span><span class="sxs-lookup"><span data-stu-id="e8f72-138">Go to Data Integration</span></span>
2. <span data-ttu-id="e8f72-139">**Bağlantı Kümesi** sekmesini seçin</span><span class="sxs-lookup"><span data-stu-id="e8f72-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="e8f72-140">İş emri eşitlemede kullanılacak Bağlantı kümesini seçin</span><span class="sxs-lookup"><span data-stu-id="e8f72-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="e8f72-141">**Tümleştirme anahtarı** sekmesini seçin</span><span class="sxs-lookup"><span data-stu-id="e8f72-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="e8f72-142">msdyn_warehouses öğesini bulun ve **msdyn_name (adı)** anahtarının eklendiğini kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="e8f72-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="e8f72-143">Görünmüyorsa, **Anahtar ekle**'ye tıklayarak ekleyin sayfanın üst kısmındaki **Kaydet**'e tıklayın</span><span class="sxs-lookup"><span data-stu-id="e8f72-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e8f72-144">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="e8f72-144">Template mapping in Data integration</span></span>

<span data-ttu-id="e8f72-145">Aşağıdaki görseller, Veri tümleştirmede şablon eşlemeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8f72-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="e8f72-146">Ambarlar (Finance and Operations'tan Field Service'a): Ambar</span><span class="sxs-lookup"><span data-stu-id="e8f72-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="e8f72-147">[![Veri tümleştirmede şablon eşleme](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="e8f72-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

