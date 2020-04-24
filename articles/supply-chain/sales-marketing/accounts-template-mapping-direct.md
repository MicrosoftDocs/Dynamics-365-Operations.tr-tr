---
title: Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme
description: Bu konu, hesapları Dynamics 365 Sales'den Supply Chain Management'a eşitlemek için altta yatan görevleri ve şablonları açıklar.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1146fce7cf620a002231a5bc9246c706b97d478d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210146"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="20f70-103">Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="20f70-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="20f70-104">Aday'dan nakde çözümünü kullanmadan önce [Common Data Service for Apps için veri tümleştirme](https://docs.microsoft.com/powerapps/administrator/data-integrator) hakkında bilgi sahibi olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="20f70-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="20f70-105">Bu konu, hesapları doğrudan Dynamics 365 Sales'den Dynamics 365 Supply Chain Management'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="20f70-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="20f70-106">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="20f70-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="20f70-107">Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="20f70-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="20f70-108">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Supply Chain Management ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="20f70-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="20f70-109">Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="20f70-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="20f70-110">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="20f70-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="20f70-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="20f70-111">Templates and tasks</span></span>

<span data-ttu-id="20f70-112">Kullanılabilir şablonlara erişmek için [Power Apps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="20f70-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="20f70-113">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="20f70-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="20f70-114">Aşağıdaki şablon ve altta yatan görev, hesapları Sales'tan Supply Chain Management'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="20f70-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="20f70-115">**Veri tümleştirmedeki şablonun adı:** Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="20f70-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="20f70-116">**Projedeki görevin adı:** Hesaplar - Müşteriler</span><span class="sxs-lookup"><span data-stu-id="20f70-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="20f70-117">Hesap/Müşteri eşitlemesinin gerçekleşmesi için eşitleme görevleri gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="20f70-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="20f70-118">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="20f70-118">Entity set</span></span>

| <span data-ttu-id="20f70-119">Satışlar</span><span class="sxs-lookup"><span data-stu-id="20f70-119">Sales</span></span>    | <span data-ttu-id="20f70-120">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="20f70-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="20f70-121">Hesaplar</span><span class="sxs-lookup"><span data-stu-id="20f70-121">Accounts</span></span> | <span data-ttu-id="20f70-122">Müşteriler V2</span><span class="sxs-lookup"><span data-stu-id="20f70-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="20f70-123">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="20f70-123">Entity flow</span></span>

<span data-ttu-id="20f70-124">Hesaplar Sales'ta yönetilir ve Supply Chain Management'a müşteriler olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="20f70-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="20f70-125">Bu müşterilerdeki **Harici Olarak Tutulur** özelliği Sales'tan gelen müşterileri izlemek için **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="20f70-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="20f70-126">Faturalama sırasında, bu bilgi Sales'a eşitlenen faturaları filtrelemekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="20f70-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="20f70-127">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="20f70-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="20f70-128">**Hesap numarası** alanı, **Hesap** sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="20f70-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="20f70-129">Tümleştirmeyi desteklemek için doğal ve benzersiz anahtar yapılmıştır.</span><span class="sxs-lookup"><span data-stu-id="20f70-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="20f70-130">Müşteri İlişkileri Yönetimi'nin (CRM) doğal anahtar özelliği, halihazırda **Hesap Numarası** alanını kullanan ancak hesap başına benzersiz **Hesap Numarası** kullanmayan müşterileri etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="20f70-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="20f70-131">Şu anda, tümleştirme çözümü bu durumu desteklemez.</span><span class="sxs-lookup"><span data-stu-id="20f70-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="20f70-132">Yeni bir hesap oluşturulduğunda, bir **Hesap Numarası** değeri zaten mevcut değilse, otomatik olarak bu numara serisini kullanarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="20f70-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="20f70-133">Değer **ACC**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir.</span><span class="sxs-lookup"><span data-stu-id="20f70-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="20f70-134">Aşağıda bir örnek verilmiştir: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="20f70-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="20f70-135">Sales için tümleştirme çözümü uygulandığında, bir güncelleştirme kodu **Hesap Numarası** alanını Sales içindeki mevcut hesaplarda ayarlar.</span><span class="sxs-lookup"><span data-stu-id="20f70-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="20f70-136">**Hesap Numarası** değeri yoksa, daha önce belirtilen numara serisi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="20f70-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="20f70-137">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="20f70-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="20f70-138">**CustomerGroupId** eşlemesi Supply Chain Management içinde geçerli bir değer bulmak için güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="20f70-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="20f70-139">Bir varsayılan değer belirtebilir veya değeri, bir değer haritası kullanarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20f70-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="20f70-140">Varsayılan şablon değeri **10**'dur.</span><span class="sxs-lookup"><span data-stu-id="20f70-140">The default template value is **10**.</span></span>

- <span data-ttu-id="20f70-141">Aşağıdaki eşleşmeleri ekleyerek, Supply Chain Management'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20f70-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="20f70-142">Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="20f70-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="20f70-143">**SiteId** - Supply Chain Management'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir.</span><span class="sxs-lookup"><span data-stu-id="20f70-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="20f70-144">Bir varsayılan site, sipariş başlığında üründen veya müşteriden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="20f70-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="20f70-145">Varsayılan şablon değeri **1**'dur.</span><span class="sxs-lookup"><span data-stu-id="20f70-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="20f70-146">**WarehouseId** - Supply Chain Management'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="20f70-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="20f70-147">Bir varsayılan ambar, Supply Chain Management'ta sipariş başlığında üründen veya müşteriden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="20f70-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="20f70-148">Varsayılan şablon değeri **13**'dur.</span><span class="sxs-lookup"><span data-stu-id="20f70-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="20f70-149">**LanguageId** - Supply Chain Management'ta teklifler ve satış siparişlerini oluşturmak için bir dil gereklidir.</span><span class="sxs-lookup"><span data-stu-id="20f70-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="20f70-150">Varsayılan olarak, müşterinin sipariş başlığındaki dil kullanılır.</span><span class="sxs-lookup"><span data-stu-id="20f70-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="20f70-151">Varsayılan şablon değeri **tr-tr**'dir.</span><span class="sxs-lookup"><span data-stu-id="20f70-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="20f70-152">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="20f70-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="20f70-153">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="20f70-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="20f70-154">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="20f70-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="20f70-155">Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="20f70-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="20f70-156">Eşleme hangi alan bilgilerinin Sales'den Supply Chain Management'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="20f70-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Veri tümleştirmede şablon eşleme](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="20f70-158">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="20f70-158">Related topics</span></span>


[<span data-ttu-id="20f70-159">Aday müşteriden nakde</span><span class="sxs-lookup"><span data-stu-id="20f70-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="20f70-160">Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="20f70-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="20f70-161">Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="20f70-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="20f70-162">Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="20f70-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="20f70-163">Supply Chain Management'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="20f70-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

