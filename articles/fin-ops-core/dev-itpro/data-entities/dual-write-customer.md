---
title: Tümleşik müşteri aslı
description: Bu konu Finance and Operations ile Common Data Service arasında müşteri verisi tümleştirmesini açıklar.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769695"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="2d782-103">Tümleşik müşteri aslı</span><span class="sxs-lookup"><span data-stu-id="2d782-103">Integrated customer master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d782-104">Müşteri kayıtlarının birden fazla uygulamada hakim olmasına yönelik tipik bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="2d782-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="2d782-105">Örneğin, satış etkinliği Sales uygulaması üzerinden ticari müşteri kayıtlarını getirebilir ve e-Ticaret veya perakende satışlar Finance and Operations uygulaması aracılığıyla müşteri kayıtlarını getirebilir.</span><span class="sxs-lookup"><span data-stu-id="2d782-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="2d782-106">Müşteri kaydının kaynağından bağımsız olarak, uygulama sınırları ve altyapı farklılıklarının sahne arkasına entegre edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="2d782-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="2d782-107">Tümleşik müşteri hakimiyeti çoklu hakimiyet senaryolarını işlemeye yardımcı olur ve Dynamics 365 uygulama paketine kapsamlı bir müşteri görünümü sağlar.</span><span class="sxs-lookup"><span data-stu-id="2d782-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="2d782-108">Müşteri veri akışı</span><span class="sxs-lookup"><span data-stu-id="2d782-108">Customer data flow</span></span>

<span data-ttu-id="2d782-109">*Müşteri*, uygulamalarda iyi tanımlanmış bir kavramdır.</span><span class="sxs-lookup"><span data-stu-id="2d782-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="2d782-110">Bu nedenle, müşteri verileri tümleştirmesi yalnızca iki uygulama arasındaki müşteri kavramını uyumlu hale getirmeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="2d782-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="2d782-111">Aşağıdaki örnekte, müşteri verisi akışı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2d782-111">The following illustration shows the customer data flow.</span></span>

![Müşteri veri akışı](media/dual-write-customer-data-flow.png)

<span data-ttu-id="2d782-113">Müşteriler, geniş anlamda iki türde sınıflandırılabilir: ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar.</span><span class="sxs-lookup"><span data-stu-id="2d782-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="2d782-114">Bu iki tür müşteri Finance and Operations ve Common Data Service uygulamasında 'da farklı şekilde saklanır ve işlenir.</span><span class="sxs-lookup"><span data-stu-id="2d782-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="2d782-115">Finance and Operations'ta, ticari/kuruluş müşterileri ve tüketiciler/son kullanıcılar **CustTable** (CustomerCustomerV3Entity) adlı tek bir tabloda yönetilir ve **Tür** özniteliğine göre sınıflandırılır.</span><span class="sxs-lookup"><span data-stu-id="2d782-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="2d782-116">( **Tür** **Kuruluş** olarak ayarlanırsa, müşteri ticari/kuruluş müşterisidir; **Tür** **Kişi** olarak ayarlanırsa, müşteri bir tüketici/son kullanıcıdır.) Birincil ilgili kişi bilgileri SMMContactPersonEntity varlığı aracılığıyla işlenir.</span><span class="sxs-lookup"><span data-stu-id="2d782-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="2d782-117">Common Data Service'ta, ticari/kuruluş müşterileri Hesap varlığında yönetilir ve **RelationshipType** özniteliği **Müşteri** olarak ayarlandığında, müşteri olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="2d782-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="2d782-118">Hem tüketiciler/son kullanıcılar hem de ilgili kişi, İlgili Kişi varlığı ile temsil edilir.</span><span class="sxs-lookup"><span data-stu-id="2d782-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="2d782-119">Bir tüketici/son Kullanıcı ve bir ilgili kişi arasında net bir ayrım sağlamak için **İlgili Kişi** varlığında **satış yapılabilir** adlı bir Boole bayrağı bulunur.</span><span class="sxs-lookup"><span data-stu-id="2d782-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="2d782-120">**Satış yapılabilir** için değer **Doğru** olduğunda, ilgili kişi bir tüketici/son kullanıcıdır ve bu ilgili kişi için teklifler ve siparişler oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="2d782-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="2d782-121">**Satış yapılabilir** için değer **Yanlış** olduğunda, ilgili kişi yalnızca bir müşterinin birincil ilgili kişisidir.</span><span class="sxs-lookup"><span data-stu-id="2d782-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="2d782-122">Satış yapılabilir olmayan bir ilgili kişi bir teklif veya sipariş sürecine katıldığında,  **Satış yapılabilir** alanı ilgili kişiyi satış yapılabilir kişi olarak işaretlemek üzere **Doğru** değerine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="2d782-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="2d782-123">Satış yapılabilir ilgili kişi haline gelen bir ilgili kişi satış yapılabilir ilgili kişi olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="2d782-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="2d782-124">Şablonlar</span><span class="sxs-lookup"><span data-stu-id="2d782-124">Templates</span></span>

<span data-ttu-id="2d782-125">Müşteri verileri, müşteriyle ilgili müşteri grubu, adresler, iletişim bilgileri, ödeme profili, fatura profili ve bağlılık durumu gibi tüm bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="2d782-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="2d782-126">Varlık eşlemeleri topluluğu, aşağıdaki tabloda gösterildiği gibi, müşteri veri etkileşimi sırasında birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="2d782-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="2d782-127">Finance and Operations uygulamaları</span><span class="sxs-lookup"><span data-stu-id="2d782-127">Finance and Operations apps</span></span> | <span data-ttu-id="2d782-128">Diğer Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="2d782-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="2d782-129">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d782-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="2d782-130">CDS İlgili Kişileri V2</span><span class="sxs-lookup"><span data-stu-id="2d782-130">CDS Contacts V2</span></span>             | <span data-ttu-id="2d782-131">ilgili kişiler</span><span class="sxs-lookup"><span data-stu-id="2d782-131">contacts</span></span>                        | <span data-ttu-id="2d782-132">Bu şablon, müşterilerin ve satıcıların tüm birincil, ikincil ve üçüncül ilgili kişi bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="2d782-133">Müşteri grupları</span><span class="sxs-lookup"><span data-stu-id="2d782-133">Customer groups</span></span>             | <span data-ttu-id="2d782-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="2d782-134">msdyn_customergroups</span></span>            | <span data-ttu-id="2d782-135">Bu şablon müşteri grubu bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="2d782-136">Müşteri ödeme yöntemi</span><span class="sxs-lookup"><span data-stu-id="2d782-136">Customer payment method</span></span>     | <span data-ttu-id="2d782-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="2d782-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="2d782-138">Bu şablon, müşteri ödeme yöntemi bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="2d782-139">Müşteriler V3</span><span class="sxs-lookup"><span data-stu-id="2d782-139">Customers V3</span></span>                | <span data-ttu-id="2d782-140">hesaplar</span><span class="sxs-lookup"><span data-stu-id="2d782-140">accounts</span></span>                        | <span data-ttu-id="2d782-141">Bu şablon, ticari ve kurumsal müşterilere ilişkin müşteri ana bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="2d782-142">Müşteriler V3</span><span class="sxs-lookup"><span data-stu-id="2d782-142">Customers V3</span></span>                | <span data-ttu-id="2d782-143">ilgili kişiler</span><span class="sxs-lookup"><span data-stu-id="2d782-143">contacts</span></span>                        | <span data-ttu-id="2d782-144">Bu şablon tüketicilere ve son kullanıcılara ilişkin müşteri ana verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="2d782-145">Bağlılık programı kartı</span><span class="sxs-lookup"><span data-stu-id="2d782-145">Loyalty card</span></span>                | <span data-ttu-id="2d782-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="2d782-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="2d782-147">Bu şablon müşteri bağlılık programı kartı bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="2d782-148">Ad ekleri</span><span class="sxs-lookup"><span data-stu-id="2d782-148">Name affixes</span></span>                | <span data-ttu-id="2d782-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="2d782-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="2d782-150">Bu şablon, müşterilerin ve satıcıların ad ekleri referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2d782-151">Ödeme günü satırları CDS V2</span><span class="sxs-lookup"><span data-stu-id="2d782-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="2d782-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="2d782-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="2d782-153">Bu şablon, müşterilerin ve satıcıların ödeme günü satırları referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2d782-154">Ödeme günleri CDS</span><span class="sxs-lookup"><span data-stu-id="2d782-154">Payment days CDS</span></span>            | <span data-ttu-id="2d782-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="2d782-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="2d782-156">Bu şablon, müşterilerin ve satıcıların ödeme günleri referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2d782-157">Ödeme planı satırları</span><span class="sxs-lookup"><span data-stu-id="2d782-157">Payment schedule lines</span></span>      | <span data-ttu-id="2d782-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="2d782-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="2d782-159">Müşterilerin ve satıcıların ödeme planı satırları referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2d782-160">Ödeme planı</span><span class="sxs-lookup"><span data-stu-id="2d782-160">Payment schedule</span></span>            | <span data-ttu-id="2d782-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="2d782-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="2d782-162">Bu şablon, müşterilerin ve satıcıların ödeme planı referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2d782-163">Ödeme koşulları</span><span class="sxs-lookup"><span data-stu-id="2d782-163">Terms of payment</span></span>            | <span data-ttu-id="2d782-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="2d782-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="2d782-165">Bu şablon, müşterilerin ve satıcıların ödeme koşulları (ödeme koşulları) referans verilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="2d782-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
