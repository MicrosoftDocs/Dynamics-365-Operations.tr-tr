---
title: Genel adres defteri ve diğer adres defterleri için planlama
description: Bu konuda, genel adres defteri ve diğer ek adres defterlerini kurup yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c6e71e5f537f0f9309eca1025c8e74cdce6716
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2019
ms.locfileid: "2883423"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="af622-103">Genel adres defteri ve diğer adres defterleri için planlama</span><span class="sxs-lookup"><span data-stu-id="af622-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af622-104">Bu konuda, genel adres defteri ve diğer ek adres defterlerini kurup yapılandırmadan önce planlama sürecinde değerlendirmeniz gereken noktalar ve almanız gereken kararlar açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="af622-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="af622-105">Kararlardan bazılarında, üretimin diğer alanları için verilen kararları (örneğin organizasyon hiyerarşisini) onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="af622-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="af622-106">Genel adres defteri</span><span class="sxs-lookup"><span data-stu-id="af622-106">Global address book</span></span>

<span data-ttu-id="af622-107">Genel Adres Defteri ile çalışmaya başlamadan önce onun için varsayılan değerleri belirlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="af622-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="af622-108">Bu varsayılan değerler, daha sonra oluşturacağınız tüm ek adres defterleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="af622-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="af622-109">**Kararlar**</span><span class="sxs-lookup"><span data-stu-id="af622-109">**Decisions**</span></span>

- <span data-ttu-id="af622-110">**Kişi** türü için tarafların kayıtları hangi sıralama ile görüntülenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="af622-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="af622-111">Örneğin bir sıralama, soyad, ikinci ad ve isimden oluşur.</span><span class="sxs-lookup"><span data-stu-id="af622-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="af622-112">Taraf kayıtları adres defterinden, rol kayıtları silindiğinde silinmeli midir?</span><span class="sxs-lookup"><span data-stu-id="af622-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="af622-113">Örneğin, bir müşteri kaydı silinirse, taraf kaydı da silinmelidir?</span><span class="sxs-lookup"><span data-stu-id="af622-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="af622-114">Yeni bir kayıt oluşturulduğunda, genel adres defteri içinde yinelenen bir kayıt bulunursa, kullanıcılara bildirisin mi?</span><span class="sxs-lookup"><span data-stu-id="af622-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="af622-115">Veri evrensel numaralandırma sistemi (DUNS) numarası bir taraf kaydının bilgilerine dahil edilsin mi?</span><span class="sxs-lookup"><span data-stu-id="af622-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="af622-116">Eğer DUNS numarası taraf kaydına dahil edildiyse, numaranın benzersiz olması kontrol edilmeli midir?</span><span class="sxs-lookup"><span data-stu-id="af622-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="af622-117">Genel Adres Defteri içinde bir taraf kayıt oluşturulduğunda, varsayılan taraf türü, kişi veya kuruluş olmasını istiyor musunuz?</span><span class="sxs-lookup"><span data-stu-id="af622-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="af622-118">Hangi kullanıcı rolleri, özel adreslere ve parti kayıtlarının iletişim bilgilerine erişebilir?</span><span class="sxs-lookup"><span data-stu-id="af622-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="af622-119">Ek adres defterleri</span><span class="sxs-lookup"><span data-stu-id="af622-119">Additional address books</span></span>

<span data-ttu-id="af622-120">Genel Adres Defteri'ni oluşturduktan sonra her iş kolu veya kuruluşunuzdaki her şirket için bir ayrı bir adres defterini, gerektiği gibi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af622-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="af622-121">Örneğin, Fabrikam birden fazla şirket ve birden çok iş kolları olan uluslararası bir kuruluştur.</span><span class="sxs-lookup"><span data-stu-id="af622-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="af622-122">Fabrikam, her iş kolu için bir adres defteri oluşturmayı planlar.</span><span class="sxs-lookup"><span data-stu-id="af622-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="af622-123">Pnömatik Araçlar iş gibi birden fazla yerde ortaya çıkan iş kolları için Fabrikam her konum için bir adres defteri oluşturma planı yapar.</span><span class="sxs-lookup"><span data-stu-id="af622-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="af622-124">Chris, Fabrikam'ın BT yöneticisi, aşağıdaki gerekli olan adres defterleri listesini oluşturmuştur.</span><span class="sxs-lookup"><span data-stu-id="af622-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="af622-125">Bu liste aynı zamanda da her adres defterinin içermesi gereken taraf kayıtlarını açıklar.</span><span class="sxs-lookup"><span data-stu-id="af622-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="af622-126">**Kamu sektörü sözleşmeleri (PubSC)** – Fabrikam'ın elinde bulunan kamu sektörü sözleşmelere dahil tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="af622-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="af622-127">**Özel sektör sözleşmeleri (PriSC)** – Fabrikam'ın elinde bulunan özel sektör sözleşmelerine dahil tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="af622-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="af622-128">**Elektronik Araçlar (ET)** – Elektronik araçların veya başka şekilde Fabrikam için Fabrikam-Japonya şirketinden sağlanan veya satın alınanlarla etkileşime giren, alımına veya satımına dahil olan tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="af622-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="af622-129">**Pnömatik Araçlar (PTJPN)** – Pnömatik araçların veya başka şekilde Fabrikam için Fabrikam-Japonya şirketinden sağlanan veya satın alınanlarla etkileşime giren, alımına veya satımına dahil olan tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="af622-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="af622-130">**Pnömatik Araçlar (PTUSA)** – Pnömatik araçların veya başka şekilde Fabrikam için Fabrikam-ABD şirketinden sağlanan veya satın alınanlarla etkileşime giren, alımına veya satımına dahil olan tüm taraflar için taraf kayıtları.</span><span class="sxs-lookup"><span data-stu-id="af622-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="af622-131">**Karar:**</span><span class="sxs-lookup"><span data-stu-id="af622-131">**Decision:**</span></span>

- <span data-ttu-id="af622-132">Kaç tane ek adres defteri oluşturacaksınız?</span><span class="sxs-lookup"><span data-stu-id="af622-132">How many additional address books will you create?</span></span>
