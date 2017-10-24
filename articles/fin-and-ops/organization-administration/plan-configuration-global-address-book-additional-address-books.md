---
title: "Genel adres defteri ve diğer adres defterlerini yapılandırmayı planlama"
description: "Bu makalede, Microsoft Dynamics 365 for Finance and Operations'da genel adres defteri ve diğer ek adres defterlerini kurup yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır. Kararlardan bazılarında, üretimin diğer alanları için verilen kararları (örneğin organizasyon hiyerarşisini) onaylamanız gerekir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a><span data-ttu-id="ba295-104">Genel adres defteri ve diğer adres defterlerini yapılandırmayı planlama</span><span class="sxs-lookup"><span data-stu-id="ba295-104">Plan how to configure the global address book and additional address books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ba295-105">Bu makalede, Microsoft Dynamics 365 for Finance and Operations'da genel adres defteri ve diğer ek adres defterlerini kurup yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ba295-105">This article describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ba295-106">Kararlardan bazılarında, üretimin diğer alanları için verilen kararları (örneğin organizasyon hiyerarşisini) onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ba295-106">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

<a name="global-address-book"></a><span data-ttu-id="ba295-107">Genel adres defteri</span><span class="sxs-lookup"><span data-stu-id="ba295-107">Global address book</span></span>
-------------------

<span data-ttu-id="ba295-108">Genel Adres Defteri ile çalışmaya başlamadan önce onun için varsayılan değerleri belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ba295-108">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="ba295-109">Bu varsayılan değerler, daha sonra oluşturacağınız tüm ek adres defterleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ba295-109">These default values are then used for any additional address books that you create.</span></span> 

<span data-ttu-id="ba295-110">**Kararlar:**</span><span class="sxs-lookup"><span data-stu-id="ba295-110">**Decisions:**</span></span>

-   <span data-ttu-id="ba295-111">**Kişi** türü için tarafların kayıtları hangi sıralama ile görüntülenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ba295-111">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="ba295-112">Örneğin bir sıralama, soyad, ikinci ad ve isimden oluşur.</span><span class="sxs-lookup"><span data-stu-id="ba295-112">For example, one sequence is last name, middle name, first name.</span></span>
-   <span data-ttu-id="ba295-113">Taraf kayıtları adres defterinden, rol kayıtları silindiğinde silinmeli midir?</span><span class="sxs-lookup"><span data-stu-id="ba295-113">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="ba295-114">Örneğin, bir müşteri kaydı silinirse, taraf kaydı da silinmelidir?</span><span class="sxs-lookup"><span data-stu-id="ba295-114">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
-   <span data-ttu-id="ba295-115">Yeni bir kayıt oluşturulduğunda, genel adres defteri içinde yinelenen bir kayıt bulunursa, kullanıcılara bildirisin mi?</span><span class="sxs-lookup"><span data-stu-id="ba295-115">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
-   <span data-ttu-id="ba295-116">Veri evrensel numaralandırma sistemi (DUNS) numarası bir taraf kaydının bilgilerine dahil edilsin mi?</span><span class="sxs-lookup"><span data-stu-id="ba295-116">Should the Data Universal Numbering System (DUNS) number be included in a party record’s information?</span></span>
-   <span data-ttu-id="ba295-117">Eğer DUNS numarası taraf kaydına dahil edildiyse, numaranın benzersiz olması kontrol edilmeli midir?</span><span class="sxs-lookup"><span data-stu-id="ba295-117">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
-   <span data-ttu-id="ba295-118">Genel Adres Defteri içinde bir taraf kayıt oluşturulduğunda, varsayılan taraf türü, kişi veya kuruluş olmasını istiyor musunuz?</span><span class="sxs-lookup"><span data-stu-id="ba295-118">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
-   <span data-ttu-id="ba295-119">Hangi kullanıcı rolleri, özel adreslere ve parti kayıtlarının iletişim bilgilerine erişebilir?</span><span class="sxs-lookup"><span data-stu-id="ba295-119">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="ba295-120">Ek adres defterleri</span><span class="sxs-lookup"><span data-stu-id="ba295-120">Additional address books</span></span>
<span data-ttu-id="ba295-121">Genel Adres Defteri'ni oluşturduktan sonra her iş kolu veya kuruluşunuzdaki her şirket için bir ayrı bir adres defterini, gerektiği gibi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba295-121">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="ba295-122">Örneğin, Fabrikam birden fazla şirket ve birden çok iş kolları olan uluslararası bir kuruluştur.</span><span class="sxs-lookup"><span data-stu-id="ba295-122">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="ba295-123">Fabrikam, her iş kolu için bir adres defteri oluşturmayı planlar.</span><span class="sxs-lookup"><span data-stu-id="ba295-123">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="ba295-124">Pnömatik Araçlar iş gibi birden fazla yerde ortaya çıkan iş kolları için Fabrikam her konum için bir adres defteri oluşturma planı yapar.</span><span class="sxs-lookup"><span data-stu-id="ba295-124">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="ba295-125">Chris, Fabrikam'ın BT yöneticisi, aşağıdaki gerekli olan adres defterleri listesini oluşturmuştur.</span><span class="sxs-lookup"><span data-stu-id="ba295-125">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="ba295-126">Bu liste aynı zamanda da her adres defterinin içermesi gereken taraf kayıtlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="ba295-126">This list also also describes the party records that each address book must include.</span></span>

-   <span data-ttu-id="ba295-127">**Kamu sektörü sözleşmeleri (PubSC)** – Fabrikam'ın elinde bulunan kamu sektörü sözleşmelere dahil tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="ba295-127">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="ba295-128">**Özel sektör sözleşmeleri (PriSC)** – Fabrikam'ın elinde bulunan özel sektör sözleşmelerine dahil tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="ba295-128">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="ba295-129">**Elektronik Araçlar (ET)** – Elektronik araçların veya başka şekilde Fabrikam için Fabrikam-Japonya şirketinden sağlanan veya satın alınanlarla etkileşime giren, alımına veya satımına dahil olan tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="ba295-129">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="ba295-130">**Pnömatik Araçlar (PTJPN)** – Pnömatik araçların veya başka şekilde Fabrikam için Fabrikam-Japonya şirketinden sağlanan veya satın alınanlarla etkileşime giren, alımına veya satımına dahil olan tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="ba295-130">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="ba295-131">**Pnömatik Araçlar (PTUSA)** – Pnömatik araçların veya başka şekilde Fabrikam için Fabrikam-ABD şirketinden sağlanan veya satın alınanlarla etkileşime giren, alımına veya satımına dahil olan tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="ba295-131">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="ba295-132">**Karar:**</span><span class="sxs-lookup"><span data-stu-id="ba295-132">**Decision:**</span></span>

-   <span data-ttu-id="ba295-133">Kaç tane ek adres defteri oluşturacaksınız?</span><span class="sxs-lookup"><span data-stu-id="ba295-133">How many additional address books will you create?</span></span>

### <a name="address-book-security"></a><span data-ttu-id="ba295-134">Adres defteri güveniği</span><span class="sxs-lookup"><span data-stu-id="ba295-134">Address book security</span></span>

<span data-ttu-id="ba295-135">Herhangi bir anda adres defterleri oluşturabilirsiniz ve herhangi bir zamanda da adres defterleri için güvenlik parametreleri ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba295-135">You can create address books at any time, and you can also set security parameters for the address books at any time.</span></span> <span data-ttu-id="ba295-136">Adres defteri için güvenlik ayrıcalıklarını ayarlamak zorunda değilsiniz, ancak bunu yapmazsanız, kuruluşunuzdaki tüm çalışanlar bu adres defterindeki tüm taraf kayıtlarını görüntüleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="ba295-136">You aren't required to set security privileges for an address book, but if you don't, all workers in your organization can view all party records in that address book.</span></span> <span data-ttu-id="ba295-137">Taraf kayıtlarına güvenlik ayrıcalıklarını adres defterlerinden ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba295-137">You can set security privileges to party records through address books.</span></span> <span data-ttu-id="ba295-138">Güvenlik ayrıcalıkları takımları temel alır.</span><span class="sxs-lookup"><span data-stu-id="ba295-138">Security privileges are based on teams.</span></span> <span data-ttu-id="ba295-139">Bu yaklaşım, sadece bir adres defterine erişimi olan bir takıma atanmış olan çalışanların bu Adres Defteri'ndeki taraf kayıtlarını görüntüleyebileceklerini garanti eder.</span><span class="sxs-lookup"><span data-stu-id="ba295-139">This approach guarantees that only workers who are assigned to a team that has access to an address book can view the party records in that address book.</span></span> <span data-ttu-id="ba295-140">Her bir adres defterine erişimi olan takımları seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ba295-140">You must select the teams that have access to each address book.</span></span> <span data-ttu-id="ba295-141">Her adres defteri için belirli takımlara erişim izni veren veya reddeden güvenlik ayrıcalıkları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba295-141">For each address book, you can set security privileges that allow or deny access to specific teams.</span></span> <span data-ttu-id="ba295-142">Eğer bir ekibe adres defterine erişim ayrıcalığı verirseniz, o ekibin tüm üyeleri o adres defterindeki kayıtları görebilirler.</span><span class="sxs-lookup"><span data-stu-id="ba295-142">If you grant a team privileges to an address book, all members of that team can view the records in the address book.</span></span> <span data-ttu-id="ba295-143">Eğer bir ekibe adres defterine erişim vermezseniz, o ekibin üyeleri o adres defterindeki kayıtları veya içeriklerini göremezler.</span><span class="sxs-lookup"><span data-stu-id="ba295-143">If you don't grant a team access to an address book, the members of that team can't view the address book or its contents.</span></span> 

<span data-ttu-id="ba295-144">**Karar:**</span><span class="sxs-lookup"><span data-stu-id="ba295-144">**Decision:**</span></span>

-   <span data-ttu-id="ba295-145">Hangi takımların oluşturduğunuz her yeni adres defterine erişimi olmalıdır?</span><span class="sxs-lookup"><span data-stu-id="ba295-145">Which teams should have access to each new address book that you will create?</span></span>





