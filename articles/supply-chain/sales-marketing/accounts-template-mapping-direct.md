---
title: "Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme"
description: "Bu konu, hesapları Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için temel görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 16bbca2d9eb8c3d9c33752404ebecbe4415517a2
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="dd3e2-103">Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="dd3e2-103">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="dd3e2-104">Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="dd3e2-105">Bu konu, hesapları doğrudan Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için temel görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="dd3e2-106">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="dd3e2-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="dd3e2-107">Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span>  <span data-ttu-id="dd3e2-108">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="dd3e2-109">Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="dd3e2-110">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="dd3e2-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="dd3e2-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="dd3e2-111">Templates and tasks</span></span>

<span data-ttu-id="dd3e2-112">Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="dd3e2-113">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="dd3e2-114">Aşağıdaki şablon ve altta yatan görev, hesapları Sales'tan Finance to Operations'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="dd3e2-114">The following template and underlying task are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="dd3e2-115">**Veri tümleştirmedeki şablonun adı:** Hesaplar (Sales'tan Fin and Ops'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="dd3e2-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="dd3e2-116">**Projedeki görevin adı:** Hesaplar - Müşteriler</span><span class="sxs-lookup"><span data-stu-id="dd3e2-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="dd3e2-117">Hesap/Müşteri eşitlemesinin gerçekleşmesi için eşitleme görevleri gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="dd3e2-118">Varlık kümesi</span><span class="sxs-lookup"><span data-stu-id="dd3e2-118">Entity set</span></span>

| <span data-ttu-id="dd3e2-119">Satış</span><span class="sxs-lookup"><span data-stu-id="dd3e2-119">Sales</span></span>    | <span data-ttu-id="dd3e2-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="dd3e2-120">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="dd3e2-121">Hesaplar</span><span class="sxs-lookup"><span data-stu-id="dd3e2-121">Accounts</span></span> | <span data-ttu-id="dd3e2-122">Müşteriler V2</span><span class="sxs-lookup"><span data-stu-id="dd3e2-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="dd3e2-123">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="dd3e2-123">Entity flow</span></span>

<span data-ttu-id="dd3e2-124">Hesaplar Sales'ta yönetilir ve Finance and Operations'a müşteriler olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-124">Accounts are managed in Sales and synchronized to Finance and Operations as customers.</span></span> <span data-ttu-id="dd3e2-125">Bu müşterilerdeki **Harici Olarak Tutulur** özelliği Sales'tan gelen müşterileri izlemek için **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="dd3e2-126">Faturalama sırasında, bu bilgi Sales'a eşitlenen faturaları filtrelemekte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="dd3e2-127">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="dd3e2-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="dd3e2-128">**Hesap numarası** alanı, **Hesap** sayfasında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="dd3e2-129">Tümleştirmeyi desteklemek için doğal ve benzersiz anahtar yapılmıştır.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="dd3e2-130">Müşteri İlişkileri Yönetimi'nin (CRM) doğal anahtar özelliği, halihazırda **Hesap Numarası** alanını kullanan ancak hesap başına benzersiz **Hesap Numarası** kullanmayan müşterileri etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="dd3e2-131">Şu anda, tümleştirme çözümü bu durumu desteklemez.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="dd3e2-132">Yeni bir hesap oluşturulduğunda, bir **Hesap Numarası** değeri zaten mevcut değilse, otomatik olarak bu numara serisini kullanarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="dd3e2-133">Değer **ACC**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="dd3e2-134">Aşağıda bir örnek verilmiştir: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="dd3e2-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="dd3e2-135">Sales için tümleştirme çözümü uygulandığında, bir güncelleştirme kodu **Hesap Numarası** alanını Sales içindeki mevcut hesaplarda ayarlar.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="dd3e2-136">**Hesap Numarası** değeri yoksa, daha önce belirtilen numara serisi kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="dd3e2-137">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="dd3e2-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="dd3e2-138">**CustomerGroupId** eşlemesi Finance and Operations içinde geçerli bir değer bulmak için güncelleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-138">The **CustomerGroupId** mapping must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="dd3e2-139">Bir varsayılan değer belirtebilir veya değeri, bir değer haritası kullanarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="dd3e2-140">Varsayılan şablon değeri **10**'dur.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-140">The default template value is **10**.</span></span>

- <span data-ttu-id="dd3e2-141">Aşağıdaki eşleşmeleri ekleyerek, Finance and Operations'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="dd3e2-142">Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="dd3e2-143">**SiteId** - Finance and Operations'ta teklifler ve satış siparişi satırlarını oluşturmak için bir site gereklidir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="dd3e2-144">Bir varsayılan site, sipariş başlığında üründen veya müşteriden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="dd3e2-145">Varsayılan şablon değeri **1**'dur.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="dd3e2-146">**WarehouseId** - Finance and Operations'ta teklifleri ve satış siparişi satırlarını işlemek için bir ambar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="dd3e2-147">Bir varsayılan ambar, Finance and Operations'ta sipariş başlığında üründen veya müşteriden alınabilir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span>

        <span data-ttu-id="dd3e2-148">Varsayılan şablon değeri **13**'dur.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="dd3e2-149">**LanguageId** – Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir dil gereklidir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="dd3e2-150">Varsayılan olarak, müşterinin sipariş başlığındaki dil kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="dd3e2-151">Varsayılan şablon değeri **tr-tr**'dir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="dd3e2-152">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="dd3e2-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="dd3e2-153">**Ödeme koşulları**, **Navlun koşulları**, **Teslimat koşulları**, **Sevkiyat yöntemi** ve **Teslimat şekli** alanları varsayılan eşlemelerine dahil değildir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="dd3e2-154">Bu alanları eşleştirmek için, varlığın aralarında eşleştirildiği kuruluşlar içinde veriye özel bir değer eşleştirmesi ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="dd3e2-155">Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="dd3e2-156">Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd3e2-156">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Veri tümleştirmede şablon eşleme](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="dd3e2-158">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="dd3e2-158">Related topics</span></span>


[<span data-ttu-id="dd3e2-159">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="dd3e2-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="dd3e2-160">Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="dd3e2-160">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="dd3e2-161">Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="dd3e2-161">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="dd3e2-162">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="dd3e2-162">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="dd3e2-163">Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="dd3e2-163">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

