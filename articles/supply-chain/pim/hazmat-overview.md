---
title: Tehlikeli malzemelere genel bakış
description: Bu konuda, ürün bilgileri yönetimi ve ambar yönetimi sırasında tehlikeli malzemelerin işlenmesi ve belgelenmesi ile ilgili özelliklere genel bir bakış sağlanır.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 34c0a19308bb5159faa9a4ab06bf65e58da0deb1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439051"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="b6a46-103">Tehlikeli malzemelere genel bakış</span><span class="sxs-lookup"><span data-stu-id="b6a46-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="b6a46-104">Sevkiyat ve taşıma yönetmeliklerine uyumluluğu korumak için tehlikeli mal olarak sınıflandırılmış malzemeler sevk eden kuruluşların, sevkiyatlarına ek belgeler eklemeleri gerekir.</span><span class="sxs-lookup"><span data-stu-id="b6a46-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="b6a46-105">Tehlikeli malzemeler özelliği, müşterilerin serbest bırakılmış maddelerle ilgili bilgileri depolamasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="b6a46-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="b6a46-106">Bu bilgiler daha sonra sevkiyat belgelerinin hazırlanmasına yardımcı olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b6a46-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="b6a46-107">Tehlikeli mal sevk eden bir kuruluşun, sevkiyat sürecini yönetmeye yönelik kendi süreçleri ve yordamları olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b6a46-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="b6a46-108">Microsoft Dynamics 365 Supply Chain Management, yalnızca gerekli belgelerin oluşturulmasına yardımcı olabilecek bir araçtır.</span><span class="sxs-lookup"><span data-stu-id="b6a46-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="b6a46-109">Aşağıdaki diyagramda, tehlikeli malzeme özelliğini ayarlamak ve kullanmak için gerekli adımlar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b6a46-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="b6a46-110">![Tehlikeli malzeme özelliğinin ayarlanması ve kullanımı](media/hazmat-overview.png "Tehlikeli malzeme özelliğinin ayarlanması ve kullanımı")</span><span class="sxs-lookup"><span data-stu-id="b6a46-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="b6a46-111">Tehlikeli malzemeler özelliği, Ürün bilgileri yönetiminde ayarlanır ve Ambar yönetimi üzerinden yazdırılabilen belgeler sağlar.</span><span class="sxs-lookup"><span data-stu-id="b6a46-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="b6a46-112">Bu nedenle, genel anlamda bu özelliğin işlevini inceleyeceğiniz, ayarlayacağınız ve kullanacağınız iki ana alan bunlardır.</span><span class="sxs-lookup"><span data-stu-id="b6a46-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="b6a46-113">**Ürün bilgileri yönetimi:** Serbest bırakılan ürüne uygulanacak kodları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b6a46-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="b6a46-114">**Ambar yönetimi**: Sevkiyatlar için yazdırılacak ek sevkiyat belgeleri üzerinde çalışın.</span><span class="sxs-lookup"><span data-stu-id="b6a46-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6a46-115">Supply Chain Management'daki tehlikeli malzeme özellikleri, tehlikeli ürünlerinizle ilgili bilgileri kaydetmenize ve bu bilgilere başvurmanıza yardımcı olabilecek kullanışlı ürün bilgisi alanları ve ilgili işlevler koleksiyonu sağlar.</span><span class="sxs-lookup"><span data-stu-id="b6a46-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="b6a46-116">Bu özellikler, sevk ettiğiniz tehlikeli malzemeler hakkındaki bilgilerin aynısını içeren sevkiyat belgelerini tasarlamanıza ve yazdırmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="b6a46-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="b6a46-117">Ancak, sistem ülkenizdeki veya bölgenizdeki geçerli tüm yönetmeliklerle otomatik olarak uyumlu hale gelmez.</span><span class="sxs-lookup"><span data-stu-id="b6a46-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="b6a46-118">Bu araçlar ortak yönetmeliklere uymanıza yardımcı olacak şekilde tasarlanmış olsa da kendi başlarına yeterli değillerdir ve bununla ilgili bir garanti sunulmaz.</span><span class="sxs-lookup"><span data-stu-id="b6a46-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="b6a46-119">Geçerli tüm yönetmelikleri bilmek ve bunlara uymak için gerekli tüm adımları atmaktan kuruluşunuz sorumludur.</span><span class="sxs-lookup"><span data-stu-id="b6a46-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="b6a46-120">Ürün bilgileri yönetimi</span><span class="sxs-lookup"><span data-stu-id="b6a46-120">Product information management</span></span>

<span data-ttu-id="b6a46-121">Ürün bilgileri yönetiminde, kara, hava ve deniz yoluyla taşıma için çeşitli tehlikeli mallar listelerinde sağlanan referans bilgilerini girebileceğiniz bir dizi kurulum tablosu bulunur.</span><span class="sxs-lookup"><span data-stu-id="b6a46-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="b6a46-122">Bu işlevin geliştirilmesi sırasında aşağıdaki ortak yönetmeliklere başvurulmuştur:</span><span class="sxs-lookup"><span data-stu-id="b6a46-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="b6a46-123">**ADR** – Tehlikeli malların uluslararası karayollarında taşınmasıyla ilgili düzenlemeler</span><span class="sxs-lookup"><span data-stu-id="b6a46-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="b6a46-124">**CFR 49** – ABD'de tehlikeli malların taşınmasına yönelik düzenlemeler</span><span class="sxs-lookup"><span data-stu-id="b6a46-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="b6a46-125">**IMDG** – Uluslararası Denizcilik Tehlikeli Maddeler (IMDG) kodu</span><span class="sxs-lookup"><span data-stu-id="b6a46-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="b6a46-126">**IATA** – Uluslararası Hava Taşımacılığı Birliği (IATA) tehlikeli mal düzenlemeleri</span><span class="sxs-lookup"><span data-stu-id="b6a46-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="b6a46-127">Her yönetmelik kümesi, tehlikeli malların ve referans kodlarının standart listelerini sağlar.</span><span class="sxs-lookup"><span data-stu-id="b6a46-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="b6a46-128">Bu nedenle, Supply Chain Management bu listelerdeki ortak kodlar için bir başvuru tablosu sunar.</span><span class="sxs-lookup"><span data-stu-id="b6a46-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="b6a46-129">Her listede, tanımlayabileceğiniz bazı benzersiz kodlar da vardır.</span><span class="sxs-lookup"><span data-stu-id="b6a46-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="b6a46-130">Tehlikeli malzemelerle ilgili yönetmeliklerin ve değerlerin nasıl ayarlanacağı ve değerlerin ilgili ürünlere nasıl atanacağı hakkında daha fazla bilgi için aşağıdaki konulara bakın:</span><span class="sxs-lookup"><span data-stu-id="b6a46-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="b6a46-131">Tehlikeli malzemeleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6a46-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="b6a46-132">Ürün, sipariş, sevkiyat ve yüklerdeki tehlikeli malzemeler</span><span class="sxs-lookup"><span data-stu-id="b6a46-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="b6a46-133">Ambar yönetimi</span><span class="sxs-lookup"><span data-stu-id="b6a46-133">Warehouse management</span></span>

<span data-ttu-id="b6a46-134">Ambar yönetiminde sevkiyat hazırlarken, Ürün bilgileri yönetiminde ayarladığınız bilgileri kullanan bazı yeni raporlar yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b6a46-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="b6a46-135">Kullanılabilir raporlar ve bunların nasıl kullanılacağı hakkında daha fazla bilgi için bkz. [Tehlikeli malzeme sorguları ve raporları](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="b6a46-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>
