---
title: "Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme"
description: "Bu konu, İlgili Kişiler (İlgili Kişiler) ve İlgili Kişiler (Müşteriler) varlıklarını Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 95b7d5be86676a1442df1c71308cb978b854d2c8
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="30da0-103">Sales'teki ilgili kişileri doğrudan Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="30da0-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="30da0-104">Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="30da0-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="30da0-105">Bu konu, İlgili Kişiler (İlgili Kişiler) ve İlgili Kişiler (Müşteriler) varlıklarını doğrudan Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations'a eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="30da0-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="30da0-106">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="30da0-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="30da0-107">Aday müşteriden nakde çözümü Finance and Operations ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="30da0-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="30da0-108">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Finance and Operations ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="30da0-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="30da0-109">Finance and Operations ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="30da0-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="30da0-110">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="30da0-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="30da0-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="30da0-111">Templates and tasks</span></span>

<span data-ttu-id="30da0-112">Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="30da0-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="30da0-113">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="30da0-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="30da0-114">Aşağıdaki şablonlar ve altta yatan görevler, İlgili Kişi (Kişiler) varlıklarını Sales'tan Finance to Operations'daki İlgili Kişi (Müşteriler) varlıklarına eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="30da0-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="30da0-115">**Veri tümleştirmesindeki şablonların adları:**</span><span class="sxs-lookup"><span data-stu-id="30da0-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="30da0-116">İlgili Kişiler (Sales'tan Fin and Ops'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="30da0-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="30da0-117">İlgili Kişilerden Müşteriye (Sales'tan Fin and Ops'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="30da0-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="30da0-118">**Veri tümleştirme projesindeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="30da0-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="30da0-119">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="30da0-119">Contacts</span></span>
    - <span data-ttu-id="30da0-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="30da0-120">ContactToCustomer</span></span>

<span data-ttu-id="30da0-121">Aşağıdaki eşitleme görevi ilgili kişi eşitlemesi gerçekleşemeden önce gereklidir: Hesaplar (Sales'tan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="30da0-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="30da0-122">Varlık kümeleri</span><span class="sxs-lookup"><span data-stu-id="30da0-122">Entity sets</span></span>

| <span data-ttu-id="30da0-123">Satış</span><span class="sxs-lookup"><span data-stu-id="30da0-123">Sales</span></span>    | <span data-ttu-id="30da0-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="30da0-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="30da0-125">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="30da0-125">Contacts</span></span> | <span data-ttu-id="30da0-126">CDS İlgili Kişileri</span><span class="sxs-lookup"><span data-stu-id="30da0-126">CDS Contacts</span></span>           |
| <span data-ttu-id="30da0-127">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="30da0-127">Contacts</span></span> | <span data-ttu-id="30da0-128">Müşteriler V2</span><span class="sxs-lookup"><span data-stu-id="30da0-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="30da0-129">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="30da0-129">Entity flow</span></span>

<span data-ttu-id="30da0-130">İlgili kişiler Sales içinde yönetilir ve Finance and Operations'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="30da0-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="30da0-131">Sales'daki bir ilgili kişi, Finance and Operations'taki bir ilgili kişi veya müşteri olabilir.</span><span class="sxs-lookup"><span data-stu-id="30da0-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="30da0-132">Sales'deki bir ilgili kişinin Finance and Operations'a bir ilgili kişi veya müşteri olarak eşitlenip eşitlenmeyeceğini belirlemek için sistem Sales'de ilgili kişinin aşağıdaki özelliklerine bakar:</span><span class="sxs-lookup"><span data-stu-id="30da0-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="30da0-133">**Finance and Operations içinde bir müşteriye eşitleme:** **Etkin Müşteri** seçeneğinin **Evet** olarak ayarlandığı ilgili kişiler</span><span class="sxs-lookup"><span data-stu-id="30da0-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="30da0-134">**Finance and Operations'da bir ilgili kişiye eşitleme:** **Etkin Müşteri**'nin **Hayır** olarak ayarlandığı ve **Şirket**'in (Ana Firma/İlgili Kişi) bir hesaba (bir İlgili Kişiye değil) işaret ettiği İlgili Kişiler</span><span class="sxs-lookup"><span data-stu-id="30da0-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="30da0-135">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="30da0-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="30da0-136">Yeni bir **Etkin Müşteri** alanı ilgili kişiye eklendi.</span><span class="sxs-lookup"><span data-stu-id="30da0-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="30da0-137">Bu alan satış etkinliğine sahip ilgili kişileri ve satış etkinliğine sahip olmayan ilgili kişileri ayırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30da0-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="30da0-138">**Etkin müşteri**, yalnızca ilgili tekliflere, siparişlere veya faturalara sahip ilgili kişiler için **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="30da0-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="30da0-139">Yalnızca bu ilgili kişiler Finance and Operations'ta müşteriler olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="30da0-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="30da0-140">Yeni bir **IsCompanyAnAccount** alanı ilgili kişiye eklendi.</span><span class="sxs-lookup"><span data-stu-id="30da0-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="30da0-141">Bu alan, bir ilgili kişinin bir **Hesap** türündeki şirkete (ana hesap/ilgili kişi) bağlı olup olmadığını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30da0-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="30da0-142">Bu bilgi Finance and Operations'a ilgili kişiler olarak eşitlenecek ilgili kişileri belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30da0-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="30da0-143">**İlgili Kişi Numarası** alanı, tümleştirme için doğal ve benzersiz anahtarın ilgili kişiye eklendiğinden emin olmak için eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="30da0-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="30da0-144">Yeni bir ilgili kişi oluşturulduğunda bir **İlgili Kişi Numarası** değeri otomatik olarak bir numara serisi kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="30da0-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="30da0-145">Değer **CON**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir.</span><span class="sxs-lookup"><span data-stu-id="30da0-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="30da0-146">Aşağıda bir örnek verilmiştir: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="30da0-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="30da0-147">Sales için tümleştirme çözümü uygulandığında, bir yükseltme komut dosyası **İlgili Kişi Numarası** alanını tüm mevcut ilgili kişiler için daha önce belirtilen numara serisini kullanarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="30da0-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="30da0-148">Bir güncelleştirme kodu ayrıca **Etkin Müşteri** alanını, satış etkinliğine sahip tüm ilgili kişiler için **Evet** olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="30da0-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="30da0-149">Finance and Operations'ta</span><span class="sxs-lookup"><span data-stu-id="30da0-149">In Finance and Operations</span></span>

<span data-ttu-id="30da0-150">İlgili Kişiler **IsContactPersonExternallyMaintained** özelliğini kullanarak etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="30da0-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="30da0-151">Bu özellik, belirli bir ilgili kişinin dışarıda tutulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="30da0-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="30da0-152">Bu durumda, dışarıda tutulan ilgili kişiler, Sales içerisinde tutulur.</span><span class="sxs-lookup"><span data-stu-id="30da0-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="30da0-153">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="30da0-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="30da0-154">İlgili kişiden müşteriye</span><span class="sxs-lookup"><span data-stu-id="30da0-154">Contact to customer</span></span>

- <span data-ttu-id="30da0-155">**CustomerGroup**, Finance and Operations içerisinde gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30da0-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="30da0-156">Eşitleme hatalarının önüne geçmek için, eşlemede bir varsayılan değer belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30da0-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="30da0-157">Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="30da0-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="30da0-158">Varsayılan şablon değeri **10**'dur.</span><span class="sxs-lookup"><span data-stu-id="30da0-158">The default template value is **10**.</span></span>

- <span data-ttu-id="30da0-159">Aşağıdaki eşleşmeleri ekleyerek, Finance and Operations'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30da0-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="30da0-160">Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="30da0-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="30da0-161">**SiteId** – Bir varsayılan site, Finance and Operations'taki ürünlerde de tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="30da0-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="30da0-162">Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir site gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30da0-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="30da0-163">**SiteId** için bir şablon değeri tanımlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="30da0-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="30da0-164">**WarehouseId** – Bir varsayılan ambar, Finance and Operations'taki ürünlerde de tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="30da0-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="30da0-165">Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir ambar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30da0-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="30da0-166">**WarehouseId** için bir şablon değeri tanımlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="30da0-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="30da0-167">**LanguageId** – Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir dil gereklidir.</span><span class="sxs-lookup"><span data-stu-id="30da0-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="30da0-168">Varsayılan şablon değeri **tr-tr**'dir.</span><span class="sxs-lookup"><span data-stu-id="30da0-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="30da0-169">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="30da0-169">Template mapping in Data integration</span></span>

<span data-ttu-id="30da0-170">Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="30da0-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="30da0-171">Eşleme hangi alan bilgilerinin Sales'den Finance and Operations'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="30da0-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="30da0-172">İlgili kişiden ilgili kişiye</span><span class="sxs-lookup"><span data-stu-id="30da0-172">Contact to contact</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="30da0-174">İlgili kişiden müşteriye</span><span class="sxs-lookup"><span data-stu-id="30da0-174">Contact to customer</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="30da0-176">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="30da0-176">Related topics</span></span>

[<span data-ttu-id="30da0-177">Müşteri adayından nakde</span><span class="sxs-lookup"><span data-stu-id="30da0-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="30da0-178">Hesapları doğrudan Sales'tan Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="30da0-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="30da0-179">Finance and Operations'taki ürünleri doğrudan Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="30da0-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="30da0-180">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="30da0-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="30da0-181">Finance and Operations'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="30da0-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



