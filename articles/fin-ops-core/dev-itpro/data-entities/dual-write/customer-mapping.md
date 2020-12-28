---
title: Tümleşik müşteri aslı
description: Bu konu, Finance and Operations ve Dataverse arasındaki müşteri verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 801538e320ca78b0cc55bb4e4b8a80d38b9b48d6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685651"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="35ad3-103">Tümleşik müşteri aslı</span><span class="sxs-lookup"><span data-stu-id="35ad3-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="35ad3-104">Müşteri verileri birden fazla Dynamics 365 uygulamasında ana kopyalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="35ad3-105">Örneğin, bir müşteri satırının kaynağı Dynamics 365 Sales (Dynamics 365'te model temelli uygulama) içindeki satış faaliyetleri olabilir veya satırın kaynağı Dynamics 365 Commerce (bir Finance and Operations uygulaması) içindeki perakende faaliyeti olabilir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="35ad3-106">Müşteri verilerinin kaynaklandığı yerden bağımsız olarak, arka planda tümleştirilir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="35ad3-107">Tümleşik Müşteri Yöneticisi, herhangi bir Dynamics 365 uygulamasındaki ana müşteri verilerine esneklik sağlar ve Dynamics 365 uygulama paketi arasında müşterinin kapsamlı bir görünümünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="35ad3-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="35ad3-108">Müşteri veri akışı</span><span class="sxs-lookup"><span data-stu-id="35ad3-108">Customer data flow</span></span>

<span data-ttu-id="35ad3-109">*Müşteri*, uygulamalarda iyi tanımlanmış bir kavramdır.</span><span class="sxs-lookup"><span data-stu-id="35ad3-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="35ad3-110">Bu nedenle, müşteri verileri tümleştirmesi yalnızca iki uygulama arasındaki müşteri kavramını uyumlu hale getirmeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="35ad3-111">Aşağıdaki örnekte, müşteri verisi akışı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-111">The following illustration shows the customer data flow.</span></span>

![Müşteri veri akışı](media/dual-write-customer-data-flow.png)

<span data-ttu-id="35ad3-113">Müşteriler, geniş anlamda iki türde sınıflandırılabilir: ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar.</span><span class="sxs-lookup"><span data-stu-id="35ad3-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="35ad3-114">Bu iki tür müşteri Finance and Operations ve Dataverse uygulamasında farklı şekilde saklanır ve işlenir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="35ad3-115">Finance and Operations uygulamasında, ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar **CustTable** (CustomerCustomerV3Entity) adlı tek bir tabloda yönetilir ve **Tür** özniteliğine göre sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="35ad3-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="35ad3-116">( **Tür** **Kuruluş** olarak ayarlanırsa, müşteri ticari/kuruluş müşterisidir; **Tür** **Kişi** olarak ayarlanırsa, müşteri bir tüketici/son kullanıcıdır.) Birincil ilgili kişi bilgileri SMMContactPersonEntity varlığı aracılığıyla işlenir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="35ad3-117">Dataverse'ta, ticari/kuruluş müşterileri Hesap varlığında yönetilir ve **RelationshipType** özniteliği **Müşteri** olarak ayarlandığında, müşteri olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="35ad3-117">In Dataverse, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="35ad3-118">Hem tüketiciler/son kullanıcılar hem de ilgili kişi, İlgili Kişi varlığı ile temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="35ad3-119">Bir tüketici/son Kullanıcı ve bir ilgili kişi arasında net bir ayrım sağlamak için **İlgili Kişi** varlığında **satış yapılabilir** adlı bir Boole bayrağı bulunur.</span><span class="sxs-lookup"><span data-stu-id="35ad3-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="35ad3-120">**Satış yapılabilir** için değer **Doğru** olduğunda, ilgili kişi bir tüketici/son kullanıcıdır ve bu ilgili kişi için teklifler ve siparişler oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="35ad3-121">**Satış yapılabilir** için değer **Yanlış** olduğunda, ilgili kişi yalnızca bir müşterinin birincil ilgili kişisidir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="35ad3-122">Satış yapılabilir olmayan bir ilgili kişi bir teklif veya sipariş sürecine katıldığında,  **Satış yapılabilir** alanı ilgili kişiyi satış yapılabilir kişi olarak işaretlemek üzere **Doğru** değerine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="35ad3-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="35ad3-123">Satış yapılabilir ilgili kişi haline gelen bir ilgili kişi satış yapılabilir ilgili kişi olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="35ad3-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="35ad3-124">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="35ad3-124">Templates</span></span>

<span data-ttu-id="35ad3-125">Müşteri verileri, müşteriyle ilgili müşteri grubu, adresler, iletişim bilgileri, ödeme profili, fatura profili ve bağlılık durumu gibi tüm bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="35ad3-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="35ad3-126">Tablo eşlemeleri koleksiyonu, aşağıdaki tabloda gösterildiği gibi, müşteri veri etkileşimi sırasında birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="35ad3-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="35ad3-127">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="35ad3-127">Finance and Operations apps</span></span> | <span data-ttu-id="35ad3-128">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="35ad3-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="35ad3-129">Tanım</span><span class="sxs-lookup"><span data-stu-id="35ad3-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="35ad3-130">CDS İlgili Kişileri V2</span><span class="sxs-lookup"><span data-stu-id="35ad3-130">CDS Contacts V2</span></span>             | <span data-ttu-id="35ad3-131">ilgili kişiler</span><span class="sxs-lookup"><span data-stu-id="35ad3-131">contacts</span></span>                        | <span data-ttu-id="35ad3-132">Bu şablon, müşterilerin ve satıcıların tüm birincil, ikincil ve üçüncül ilgili kişi bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="35ad3-133">Müşteri grupları</span><span class="sxs-lookup"><span data-stu-id="35ad3-133">Customer groups</span></span>             | <span data-ttu-id="35ad3-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="35ad3-134">msdyn_customergroups</span></span>            | <span data-ttu-id="35ad3-135">Bu şablon müşteri grubu bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="35ad3-136">Müşteri ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="35ad3-136">Customer payment method</span></span>     | <span data-ttu-id="35ad3-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="35ad3-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="35ad3-138">Bu şablon, müşteri ödeme yöntemi bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="35ad3-139">Müşteriler V3</span><span class="sxs-lookup"><span data-stu-id="35ad3-139">Customers V3</span></span>                | <span data-ttu-id="35ad3-140">hesaplar</span><span class="sxs-lookup"><span data-stu-id="35ad3-140">accounts</span></span>                        | <span data-ttu-id="35ad3-141">Bu şablon, ticari ve kurumsal müşterilere ilişkin müşteri ana bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="35ad3-142">Müşteriler V3</span><span class="sxs-lookup"><span data-stu-id="35ad3-142">Customers V3</span></span>                | <span data-ttu-id="35ad3-143">ilgili kişiler</span><span class="sxs-lookup"><span data-stu-id="35ad3-143">contacts</span></span>                        | <span data-ttu-id="35ad3-144">Bu şablon tüketicilere ve son kullanıcılara ilişkin müşteri ana verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="35ad3-145">Ad ekleri</span><span class="sxs-lookup"><span data-stu-id="35ad3-145">Name affixes</span></span>                | <span data-ttu-id="35ad3-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="35ad3-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="35ad3-147">Bu şablon, müşterilerin ve satıcıların ad ekleri referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="35ad3-148">Ödeme günü satırları CDS V2</span><span class="sxs-lookup"><span data-stu-id="35ad3-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="35ad3-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="35ad3-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="35ad3-150">Bu şablon, müşterilerin ve satıcıların ödeme günü satırları referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="35ad3-151">Ödeme günleri CDS</span><span class="sxs-lookup"><span data-stu-id="35ad3-151">Payment days CDS</span></span>            | <span data-ttu-id="35ad3-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="35ad3-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="35ad3-153">Bu şablon, müşterilerin ve satıcıların ödeme günleri referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="35ad3-154">Ödeme planı satırları</span><span class="sxs-lookup"><span data-stu-id="35ad3-154">Payment schedule lines</span></span>      | <span data-ttu-id="35ad3-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="35ad3-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="35ad3-156">Müşterilerin ve satıcıların ödeme planı satırları referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="35ad3-157">Ödeme planı</span><span class="sxs-lookup"><span data-stu-id="35ad3-157">Payment schedule</span></span>            | <span data-ttu-id="35ad3-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="35ad3-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="35ad3-159">Bu şablon, müşterilerin ve satıcıların ödeme planı referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="35ad3-160">Ödeme koşulları</span><span class="sxs-lookup"><span data-stu-id="35ad3-160">Terms of payment</span></span>            | <span data-ttu-id="35ad3-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="35ad3-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="35ad3-162">Bu şablon, müşterilerin ve satıcıların ödeme koşulları (ödeme koşulları) referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="35ad3-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
