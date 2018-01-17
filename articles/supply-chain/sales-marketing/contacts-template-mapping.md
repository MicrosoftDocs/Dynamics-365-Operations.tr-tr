---
title: "Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme"
description: "Bu konu, İlgili Kişileri (İlgili Kişiler) ve İlgili Kişileri (Müşteriler) Microsoft Dynamics 365 for Sales'tan Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a eşitlemek için altta yatan görevleri ve şablonları açıklar."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 2982c0d6f04f9f7b639a73ed5f68a082f05b17be
ms.contentlocale: tr-tr
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="2ed7b-103">Sales'teki ilgili kişileri Finance and Operations'taki ilgili kişilerle veya müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="2ed7b-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="2ed7b-104">Müşteri adayından nakde çözümünü kullanmadan önce [Dynamics 365 Veri Tümleştirme](/common-data-service/entity-reference/dynamics-365-integration) hakkında bilgi sahibi olun.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="2ed7b-105">Bu konu, İlgili Kişi (İlgili Kişiler) ve İlgili Kişi (Müşteriler) Microsoft Dynamics 365 for Sales'tan (Satış) Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'a (Finance and Operations) eşitlemek için altta yatan görevleri ve şablonları açıklar.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="2ed7b-106">Şablonlar ve görevler</span><span class="sxs-lookup"><span data-stu-id="2ed7b-106">Templates and tasks</span></span>

<span data-ttu-id="2ed7b-107">Aşağıdaki şablonlar ve altta yatan görevler, İlgili Kişi (Kişiler) ve İlgili Kişiyi (Müşterileri) Sales'tan Finance to Operations'a eşitlemekte kullanılır:</span><span class="sxs-lookup"><span data-stu-id="2ed7b-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="2ed7b-108">**Şablonların adları:**</span><span class="sxs-lookup"><span data-stu-id="2ed7b-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="2ed7b-109">İlgili Kişiler (Sales'tan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="2ed7b-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="2ed7b-110">İlgili kişiden Müşteriye (Sales'tan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="2ed7b-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="2ed7b-111">**Projedeki görevlerin adları:**</span><span class="sxs-lookup"><span data-stu-id="2ed7b-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="2ed7b-112">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="2ed7b-112">Contacts</span></span>
    - <span data-ttu-id="2ed7b-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="2ed7b-113">ContactToCustomer</span></span>

<span data-ttu-id="2ed7b-114">Aşağıdaki eşitleme görevi İlgili kişi eşitlemesinden önce gereklidir: Hesaplar (Sales'tan Fin and Ops'a)</span><span class="sxs-lookup"><span data-stu-id="2ed7b-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="2ed7b-115">Varlık kümeleri</span><span class="sxs-lookup"><span data-stu-id="2ed7b-115">Entity sets</span></span>

| <span data-ttu-id="2ed7b-116">Satış</span><span class="sxs-lookup"><span data-stu-id="2ed7b-116">Sales</span></span>    | <span data-ttu-id="2ed7b-117">CDS</span><span class="sxs-lookup"><span data-stu-id="2ed7b-117">CDS</span></span>     | <span data-ttu-id="2ed7b-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="2ed7b-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="2ed7b-119">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="2ed7b-119">Contacts</span></span> | <span data-ttu-id="2ed7b-120">Başvur</span><span class="sxs-lookup"><span data-stu-id="2ed7b-120">Contact</span></span> | <span data-ttu-id="2ed7b-121">CDS İlgili Kişileri</span><span class="sxs-lookup"><span data-stu-id="2ed7b-121">CDS Contacts</span></span>           |
| <span data-ttu-id="2ed7b-122">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="2ed7b-122">Contacts</span></span> | <span data-ttu-id="2ed7b-123">Hesap</span><span class="sxs-lookup"><span data-stu-id="2ed7b-123">Account</span></span> | <span data-ttu-id="2ed7b-124">Müşteriler V2</span><span class="sxs-lookup"><span data-stu-id="2ed7b-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="2ed7b-125">Varlık akışı</span><span class="sxs-lookup"><span data-stu-id="2ed7b-125">Entity flow</span></span>

<span data-ttu-id="2ed7b-126">İlgili kişiler Sales'ta yönetilir ve Ortak Veri Hizmeti (CDS) ve Finance and Operations'a eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="2ed7b-127">Sales'daki bir İlgili Kişi, CDS ve Finance and Operations'taki bir İlgili Kişi olabilir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="2ed7b-128">Alternatif olarak, CDS içerisinde bir Hesap ve Finance and Operations'ta bir Müşteri olabilir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-129">Bir ilgili kişinin Sales içinde CDS'ye ve Finance and Operations'a eşitlenmek üzere seçilip seçilmeyeceğini belirlemek için (örneğin, Sales'daki İlgili Kişiler &gt; CDS'de İlgili Kişi &gt; Finance and Operations'daki İlgili Kişiler) sistem Sales'daki İlgili Kişilerde aşağıdaki özelliklere bakar:</span><span class="sxs-lookup"><span data-stu-id="2ed7b-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="2ed7b-130">**CDS içinde Hesap'a ve Finance and Operations içinde Müşteri'ye eşitle:** **Etkin Müşteri** **Evet** olarak ayarlandığı İlgili Kişileri</span><span class="sxs-lookup"><span data-stu-id="2ed7b-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="2ed7b-131">**CDS içinde İlgili Kişiye ve Finance and Operations'da İlgili Kişiye eşitle:** **Etkin Müşteri**'nin **Hayır** ve **Şirket**'in (Ana Firma/İlgili Kişi) noktalarının bir hesaba (bir İlgili Kişiye değil) işaret ettiği İlgili Kişiler</span><span class="sxs-lookup"><span data-stu-id="2ed7b-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2ed7b-132">Sales için Aday müşteriden nakde çözümü</span><span class="sxs-lookup"><span data-stu-id="2ed7b-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="2ed7b-133">Yeni bir **Etkin Müşteri** alanı İlgili Kişiye eklendi.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="2ed7b-134">Bu alan satış etkinliğine sahip İlgili Kişileri ve satış etkinliğine sahip olmayan İlgili Kişileri ayırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="2ed7b-135">**Etkin müşteri**, yalnızca ilgili tekliflere, siparişlere veya faturalara sahip İlgili Kişiler için **Evet** olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="2ed7b-136">Yalnızca bu İlgili Kişiler Finance and Operations'ta Müşteriler olarak eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="2ed7b-137">Yeni bir **IsCompanyAnAccount** alanı İlgili Kişiye eklendi.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="2ed7b-138">Bu alan, bir İlgili Kişinin bir **Hesap** türündeki Şirkete (Ana Firma/İlgili Kişi) bağlı olup olmadığını belirtmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="2ed7b-139">Bu bilgi Finance and Operations'a İlgili Kişiler olarak eşitlenecek İlgili Kişileri belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="2ed7b-140">**İlgili Kişi Numarası** alanı, tümleştirme için doğal ve benzersiz anahtarın İlgili Kişiye eklendiğinden emin olmak için eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="2ed7b-141">Yeni bir İlgili Kişi oluşturulduğunda bir **İlgili Kişi Numarası** değeri otomatik olarak bir numara serisi kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="2ed7b-142">Değer **CON**'dan oluşur ve artan bir numara serisi ve daha sonra altı karakterlik bir sonek tarafından izlenir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="2ed7b-143">Aşağıda bir örnek verilmiştir: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="2ed7b-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="2ed7b-144">Sales için tümleştirme çözümü Sales'a eklendiğinde, bir güncelleştirme komut dosyası **İlgili Kişi Numarası** alanını tüm mevcut İlgili Kişiler için daha önce belirtilen numara serisini kullanarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="2ed7b-145">Bir güncelleştirme kodu ayrıca **Etkin Müşteri** alanını, satış etkinliğine sahip tüm İlgili Kişiler için **Evet** olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="2ed7b-146">Finance and Operations'ta</span><span class="sxs-lookup"><span data-stu-id="2ed7b-146">In Finance and Operations</span></span> 

<span data-ttu-id="2ed7b-147">İlgili Kişiler **IsContactPersonExternallyMaintained** özelliğini kullanarak etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="2ed7b-148">Bu özellik, belirli bir İlgili Kişinin dışarıda tutulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="2ed7b-149">Bu durumda, dışarıda tutulan İlgili Kişiler, Sales içerisinde tutulur.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2ed7b-150">Önkoşullar ve eşleme kurulumu</span><span class="sxs-lookup"><span data-stu-id="2ed7b-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="2ed7b-151">İlgili Kişi'den İlgili Kişi'ye</span><span class="sxs-lookup"><span data-stu-id="2ed7b-151">Contact to Contact</span></span>

- <span data-ttu-id="2ed7b-152">**Kaynak &gt; CDS** eşlemesi içindeki **CDS Kuruluş Kodu**'nu güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="2ed7b-153">**Organization_OrganizationId [Organization ID]** için varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="2ed7b-154">**PrimaryAccount_Organization_OrganizationId [Organization ID]** için varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="2ed7b-155">**Adres Ülke bölge kodu** alanı Finance and Operations'ta gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-156">Eşitleme hatalarının önüne geçmek için, bir varsayılan değeri **CDS &gt; İşlemler** eşlemesinde belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="2ed7b-157">Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="2ed7b-158">**PrimaryAddressCountryRegionISOCode** için varsayılan bir şablon değeri **ABD**'dir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="2ed7b-159">Aşağıdaki alanlar için bir değerin Finance and Operations'ta bulunduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-160">Bilgi Finance and Operations içinde gerekli değilse, eşlemeyi **CDS &gt; Hedef** eşlemesinden kaldırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="2ed7b-161">**Finance and Operations içinde alan adı** Karar</span><span class="sxs-lookup"><span data-stu-id="2ed7b-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="2ed7b-162">**Eşleme:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="2ed7b-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="2ed7b-163">İlgili Kişi'den Müşteri'ye</span><span class="sxs-lookup"><span data-stu-id="2ed7b-163">Contact to Customer</span></span>

- <span data-ttu-id="2ed7b-164">**Kaynak &gt; CDS** eşlemesi içindeki **CDS Kuruluş Kodu**'nu güncelleştir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="2ed7b-165">**Organization_OrganizationId [Organization ID]** için varsayılan şablon değeri **ORG001**'dir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="2ed7b-166">**Adres Ülke bölge kodu** alanı Finance and Operations'ta gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-167">Eşitleme hatalarının önüne geçmek için, bir varsayılan değeri **CDS &gt; Hedef** eşlemesinde belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="2ed7b-168">Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="2ed7b-169">**PrimaryAddressCountryRegionISOCode** için varsayılan bir şablon değeri **ABD**'dir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="2ed7b-170">**CustomerGroup**, Finance and Operations içerisinde gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-171">Eşitleme hatalarının önüne geçmek için, bir varsayılan değeri **CDS &gt; Hedef** eşlemesinde belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="2ed7b-172">Varsayılan değer daha sonra bu alan Sales'ta boş kalırsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="2ed7b-173">**CustomerGroupId** için varsayılan bir şablon değeri **10**'dur.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="2ed7b-174">Aşağıdaki eşleşmeleri **CDS &gt; Hedef**'ten ekleyerek, Finance and Operations'daki el ile güncelleştirmelerin sayısını azaltmaya yardımcı olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-175">Bir varsayılan değeri veya değer eşlemesini, örneğin **Ülke/Bölge** veya **Şehir**'den kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="2ed7b-176">**SiteId** - Bir varsayılan site, Finance and Operations'taki ürünlerde de tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-177">Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir site gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-178">**SiteId** için bir şablon değeri tanımlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="2ed7b-179">**WarehouseId** - Bir varsayılan ambar, Finance and Operations'taki ürünlerde de tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-180">Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir ambar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-181">**WarehouseId** için bir şablon değeri tanımlanmamıştır.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="2ed7b-182">**LanguageId** - Finance and Operations'ta teklifler ve satış siparişleri oluşturmak için bir dil gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="2ed7b-183">**LanguageId** için varsayılan şablon değeri **en-us** olur.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="2ed7b-184">Veri entegratörü içerisindeki şablon eşleme</span><span class="sxs-lookup"><span data-stu-id="2ed7b-184">Template mapping in data integrator</span></span>

<span data-ttu-id="2ed7b-185">Aşağıdaki görseller, veri tümleştircisinde bir şablon eşleme örneği gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ed7b-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="2ed7b-186">İlgili Kişi'den İlgili Kişi'ye</span><span class="sxs-lookup"><span data-stu-id="2ed7b-186">Contact to Contact</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-template-mapping-data-integrator-1.png)

![Veri entegratörü içerisindeki İlgili Kişiler için şablon eşleme](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="2ed7b-189">İlgili Kişi'den Müşteri'ye</span><span class="sxs-lookup"><span data-stu-id="2ed7b-189">Contact to Customer</span></span>

![Veri entegratörü içerisindeki şablon eşleme](./media/contacts-template-mapping-data-integrator-3.png)

![Veri entegratörü içerisindeki İlgili Kişiler için şablon eşleme](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="2ed7b-192">İlgili konular</span><span class="sxs-lookup"><span data-stu-id="2ed7b-192">Related topics</span></span>

[<span data-ttu-id="2ed7b-193">Finance and Operations'taki ürünleri Sales'teki ürünlerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="2ed7b-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="2ed7b-194">Sales'teki firmaları Finance and Operations'taki müşterilerle eşitleme</span><span class="sxs-lookup"><span data-stu-id="2ed7b-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="2ed7b-195">Sales'deki satış teklifi başlıklarını ve satırlarını Finance and Operations'la eşitleme</span><span class="sxs-lookup"><span data-stu-id="2ed7b-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="2ed7b-196">Finance and Operations'daki satış siparişi başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="2ed7b-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="2ed7b-197">Finance and Operations'daki satış faturası başlıklarını ve satırlarını Sales ile eşitleme</span><span class="sxs-lookup"><span data-stu-id="2ed7b-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

