---
title: Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme
description: Bu konu, Kişiler (Kişiler) ve Kişiler (Müşteriler) varlıklarını Dynamics 365 Sales üzerinden Dynamics 365 Supply Chain Management üzerine eşitlemekte kullanılan şablonları ve alttaki görevleri açıklar.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: d0e3b8b2087547ea93a16cd3eb43b2126e0e787b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215805"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="5ad26-103">Sales'teki ilgili kişileri doğrudan Supply Chain Management'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="5ad26-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="5ad26-104">Aday'dan nakde çözümünü kullanmadan önce [Microsoft Dataverse for Apps için veri tümleştirme](https://docs.microsoft.com/powerapps/administrator/data-integrator) hakkında bilgi sahibi olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="5ad26-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="5ad26-105">Bu konuda, İlgili Kişi (Kişiler) ve İlgili Kişi (Müşteriler) tablolarını doğrudan Dynamics 365 Sales'den Dynamics 365 Supply Chain Management'a eşitlemekte kullanılan şablonlar ve temel görevler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="5ad26-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) tables directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5ad26-106">Aday müşteriden nakde çözümünde veri akışı</span><span class="sxs-lookup"><span data-stu-id="5ad26-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5ad26-107">Aday müşteriden nakde çözümü Supply Chain Management ve Sales örnekleri arasında verileri eşitlemek için Veri tümleştirme özelliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5ad26-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="5ad26-108">Veri Tümleştirme özelliği içindeki Aday müşteriden nakde şablonları, hesaplar, ilgili kişiler, ürünler ve satış teklifleri, satış siparişleri ve satış faturalarının Supply Chain Management ve Sales arasında veri akışını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="5ad26-109">Supply Chain Management ve Sales arasında verilerin nasıl eşitleneceği aşağıda gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="5ad26-110">[![Aday müşteriden nakde çözümünde veri akışı](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5ad26-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5ad26-111">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="5ad26-111">Templates and tasks</span></span>

<span data-ttu-id="5ad26-112">Kullanılabilir şablonlara erişmek için [PowerApps Yönetim Merkezi](https://preview.admin.powerapps.com/dataintegration)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="5ad26-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5ad26-113">**Projeler**'i seçin ve ardından genel şablonları seçmek için sağ üst köşeden **Yeni proje**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5ad26-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5ad26-114">Aşağıdaki şablonlar ve temel görevler, İlgili Kişi (Kişiler) tablolarını Sales'dan Supply Chain Management'taki İlgili Kişi (Müşteriler) tablolarına eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="5ad26-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) tables in Sales to Contact (Customers) tables in Supply Chain Management.</span></span>

- <span data-ttu-id="5ad26-115">**Veri tümleştirmesindeki şablonların adları:**</span><span class="sxs-lookup"><span data-stu-id="5ad26-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="5ad26-116">İlgili kişiler (Sales'ten Supply Chain Management'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="5ad26-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="5ad26-117">İlgili kişilerden Müşteriye (Sales'ten Supply Chain Management'a) - Doğrudan</span><span class="sxs-lookup"><span data-stu-id="5ad26-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="5ad26-118">**Veri tümleştirme projesindeki görevlerin adları**</span><span class="sxs-lookup"><span data-stu-id="5ad26-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="5ad26-119">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="5ad26-119">Contacts</span></span>
    - <span data-ttu-id="5ad26-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="5ad26-120">ContactToCustomer</span></span>

<span data-ttu-id="5ad26-121">Aşağıdaki eşitleme görevi ilgili kişi eşitlemesi gerçekleşemeden önce gereklidir: Hesaplar (Sales'tan Supply Chain Management'a)</span><span class="sxs-lookup"><span data-stu-id="5ad26-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="5ad26-122">Varlık kümeleri</span><span class="sxs-lookup"><span data-stu-id="5ad26-122">Entity sets</span></span>

| <span data-ttu-id="5ad26-123">Satışlar</span><span class="sxs-lookup"><span data-stu-id="5ad26-123">Sales</span></span>    | <span data-ttu-id="5ad26-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5ad26-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="5ad26-125">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="5ad26-125">Contacts</span></span> | <span data-ttu-id="5ad26-126">Dataverse İlgili Kişileri</span><span class="sxs-lookup"><span data-stu-id="5ad26-126">Dataverse Contacts</span></span>           |
| <span data-ttu-id="5ad26-127">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="5ad26-127">Contacts</span></span> | <span data-ttu-id="5ad26-128">Müşteriler V2</span><span class="sxs-lookup"><span data-stu-id="5ad26-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="5ad26-129">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="5ad26-129">Entity flow</span></span>

<span data-ttu-id="5ad26-130">İlgili Kişiler Sales'ta yönetilir ve Supply Chain Management'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="5ad26-131">Sales'daki bir ilgili kişi, Supply Chain Management'taki bir ilgili kişi veya müşteri olabilir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="5ad26-132">Sales'deki bir ilgili kişinin Supply Chain Management'a bir ilgili kişi veya müşteri olarak eşitlenip eşitlenmeyeceğini belirlemek için sistem Sales'de ilgili kişinin aşağıdaki özelliklerine bakar:</span><span class="sxs-lookup"><span data-stu-id="5ad26-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="5ad26-133">**Supply Chain Management içinde bir müşteriye eşitleme:** **Etkin Müşteri** seçeneğinin **Evet** olarak ayarlandığı ilgili kişiler</span><span class="sxs-lookup"><span data-stu-id="5ad26-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="5ad26-134">**Supply Chain Management'da bir ilgili kişiye eşitleme:** **Etkin Müşteri**'nin **Hayır** olarak ayarlandığı ve **Şirket**'in (Ana Firma/İlgili Kişi) bir hesaba (bir İlgili Kişiye değil) işaret ettiği İlgili Kişiler</span><span class="sxs-lookup"><span data-stu-id="5ad26-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5ad26-135">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="5ad26-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5ad26-136">Yeni bir **Etkin Müşteri** sütunu ilgili kişiye eklendi.</span><span class="sxs-lookup"><span data-stu-id="5ad26-136">A new **Is Active Customer** column has been added to the contact.</span></span> <span data-ttu-id="5ad26-137">Bu sütun satış etkinliğine sahip ilgili kişileri ve satış etkinliğine sahip olmayan ilgili kişileri ayırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ad26-137">This column is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="5ad26-138">**Etkin müşteri**, yalnızca ilgili tekliflere, siparişlere veya faturalara sahip ilgili kişiler için **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5ad26-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="5ad26-139">Yalnızca bu ilgili kişiler Supply Chain Management'ta müşteriler olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="5ad26-140">Yeni bir **IsCompanyAnAccount** sütunu ilgili kişiye eklendi.</span><span class="sxs-lookup"><span data-stu-id="5ad26-140">A new **IsCompanyAnAccount** column has been added to the contact.</span></span> <span data-ttu-id="5ad26-141">Bu sütun, ilgili kişinin bir **Hesap** türündeki şirkete (ana hesap/ilgili kişi) bağlı olup olmadığını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ad26-141">This column indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="5ad26-142">Bu bilgi Supply Chain Management'a ilgili kişiler olarak eşitlenecek ilgili kişileri belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ad26-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="5ad26-143">**İlgili Kişi Numarası** sütunu, tümleştirme için doğal ve benzersiz anahtarın ilgili kişiye eklendiğinden emin olmak için eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-143">A new **Contact Number** column has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="5ad26-144">Yeni bir ilgili kişi oluşturulduğunda bir **İlgili Kişi Numarası** değeri otomatik olarak bir numara serisi kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ad26-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="5ad26-145">Değer **CON**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="5ad26-146">Aşağıda bir örnek verilmiştir: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="5ad26-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="5ad26-147">Sales için tümleştirme çözümü uygulandığında, bir yükseltme komut dosyası **İlgili Kişi Numarası** sütununu tüm mevcut ilgili kişiler için daha önce belirtilen numara serisini kullanarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5ad26-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** column for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="5ad26-148">Bir güncelleştirme kodu ayrıca **Etkin Müşteri** sütununu, satış etkinliğine sahip tüm ilgili kişiler için **Evet** olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5ad26-148">The upgrade script also sets the **Is Active Customer** column to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="5ad26-149">Supply Chain Management'ta</span><span class="sxs-lookup"><span data-stu-id="5ad26-149">In Supply Chain Management</span></span>

<span data-ttu-id="5ad26-150">İlgili Kişiler **IsContactPersonExternallyMaintained** özelliğini kullanarak etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="5ad26-151">Bu özellik, belirli bir ilgili kişinin dışarıda tutulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="5ad26-152">Bu durumda, dışarıda tutulan ilgili kişiler, Sales içerisinde tutulur.</span><span class="sxs-lookup"><span data-stu-id="5ad26-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5ad26-153">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="5ad26-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="5ad26-154">İlgili kişiden müşteriye</span><span class="sxs-lookup"><span data-stu-id="5ad26-154">Contact to customer</span></span>

- <span data-ttu-id="5ad26-155">**CustomerGroup** Supply Chain Management'ta gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="5ad26-156">Eşitleme hatalarının önüne geçmek için, eşlemede bir varsayılan değer belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad26-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="5ad26-157">Varsayılan değer daha sonra bu sütun Sales'da boş kalırsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ad26-157">That default value is then used if the column is left blank in Sales.</span></span>

    <span data-ttu-id="5ad26-158">Varsayılan şablon değeri **10**'dur.</span><span class="sxs-lookup"><span data-stu-id="5ad26-158">The default template value is **10**.</span></span>

- <span data-ttu-id="5ad26-159">Aşağıdaki eşleşmeleri ekleyerek, Supply Chain Management'da gereken el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad26-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="5ad26-160">Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ad26-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="5ad26-161">**SiteId** – Bir varsayılan site, Supply Chain Management'taki ürünlerde de tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="5ad26-162">Supply Chain Management'ta teklifler ve satış siparişleri oluşturmak için bir site gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="5ad26-163">**SiteId** için bir şablon değeri tanımlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="5ad26-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="5ad26-164">**WarehouseId** – Bir varsayılan ambar, Supply Chain Management'taki ürünlerde de tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="5ad26-165">Supply Chain Management'ta teklifler ve satış siparişleri oluşturmak için bir ambar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="5ad26-166">**WarehouseId** için bir şablon değeri tanımlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="5ad26-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="5ad26-167">**LanguageId** - Supply Chain Management'ta teklifler ve satış siparişlerini oluşturmak için bir dil gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="5ad26-168">Varsayılan şablon değeri **tr-tr**'dir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5ad26-169">Veri tümleştirmede şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="5ad26-169">Template mapping in Data integration</span></span>

<span data-ttu-id="5ad26-170">Aşağıdaki görseller, veri tümleştirmede bir şablon eşleme örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5ad26-171">Eşleme hangi sütun bilgilerinin Sales'den Supply Chain Management'a eşitleneceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ad26-171">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="5ad26-172">İlgili kişiden ilgili kişiye</span><span class="sxs-lookup"><span data-stu-id="5ad26-172">Contact to contact</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="5ad26-174">İlgili kişiden müşteriye</span><span class="sxs-lookup"><span data-stu-id="5ad26-174">Contact to customer</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="5ad26-176">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="5ad26-176">Related topics</span></span>

[<span data-ttu-id="5ad26-177">Aday müşteriden nakde</span><span class="sxs-lookup"><span data-stu-id="5ad26-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5ad26-178">Sales'deki hesapları doğrudan Supply Chain Management'daki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="5ad26-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5ad26-179">Supply Chain Management'daki ürünleri doğrudan Sales'deki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="5ad26-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="5ad26-180">Sales ve Supply Chain Management arasında satış siparişlerini doğrudan eşitleme</span><span class="sxs-lookup"><span data-stu-id="5ad26-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="5ad26-181">Supply Chain Management'daki satış faturası başlıklarını ve satırlarını doğrudan Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="5ad26-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]