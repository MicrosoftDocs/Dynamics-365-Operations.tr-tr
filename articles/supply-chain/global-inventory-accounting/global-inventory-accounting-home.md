---
title: Global Stok Muhasebesi giriş sayfası
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management için Global Stok Muhasebesi Eklentisi'nin giriş sayfasıdır.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f4434afb847104a18a2a2a2f07a7060cf01de816
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273237"
---
# <a name="global-inventory-accounting-home-page"></a><span data-ttu-id="1a90a-103">Global Stok Muhasebesi giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="1a90a-103">Global Inventory Accounting home page</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="1a90a-104">Uluslararası kuruluşlar, yerel ve küresel muhasebe standartlarına uymaları için yetkililerin artan baskısı altındadır.</span><span class="sxs-lookup"><span data-stu-id="1a90a-104">International organizations are under increasing pressure from authorities to comply with local and global accounting standards.</span></span> <span data-ttu-id="1a90a-105">Stok değerlemesi uyumun sağlanmasında önemli bir rol oynar.</span><span class="sxs-lookup"><span data-stu-id="1a90a-105">The valuation of inventory plays a significant role in ensuring compliance.</span></span> <span data-ttu-id="1a90a-106">Microsoft Dynamics 365 Supply Chain Management için Global Stok Muhasebesi Eklentisi, kuruluşların (özellikle uluslararası kuruluşların) stok muhasebesi yapmak için birden çok maliyetli genel muhasebe çözümü kullanmasını sağlayan kapsamlı bir çözüm sağlar.</span><span class="sxs-lookup"><span data-stu-id="1a90a-106">The Global Inventory Accounting Add-in for Microsoft Dynamics 365 Supply Chain Management provides a comprehensive solution that enables organizations (especially international organizations) to use multiple costing ledgers to do inventory accounting.</span></span> <span data-ttu-id="1a90a-107">Bu nedenle, bu kuruluşlar aynı anda birden fazla muhasebe standardına ve dahili yönetim muhasebesiyle aynı anda uyumlu olabilir.</span><span class="sxs-lookup"><span data-stu-id="1a90a-107">Therefore, those organizations can comply with multiple accounting standards and internal management accounting at the same time.</span></span>

<span data-ttu-id="1a90a-108">Global Stok Muhasebesi, uygun değerleme yöntemini (standart maliyet, ortalama veya belirli tanımlama) ve örnek başına seçilen muhasebe para birimini uygulayarak birden çok gösterimde stoğu muhasebeleştirmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="1a90a-108">Global Inventory Accounting lets you account inventory in multiple representations by applying the appropriate valuation method (standard cost, average, or specific identification) and the selected accounting currency per instance.</span></span> <span data-ttu-id="1a90a-109">Global Stok Muhasebesi, kuruluşların stok ekstrelerini ve yardımcı defter muhasebe değerlerini (stok bakiyesi ve satılan malların maliyeti olarak da bilinir) genellikle çift değerleme ve/veya çift para birimi şeklinde raporlamasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="1a90a-109">Global Inventory Accounting enables organizations to report inventory statements and subledger accounting values (also known as the inventory balance and the cost of goods sold) in what is often referred to as dual valuation and/or dual currency.</span></span>

<span data-ttu-id="1a90a-110">Stok muhasebesi tek tek genel muhasebe defterlerinde yapılır.</span><span class="sxs-lookup"><span data-stu-id="1a90a-110">Inventory accounting is done in individual ledgers.</span></span> <span data-ttu-id="1a90a-111">Gerektiğinde, bir kuruluştaki her tüzel kişilik için birkaç Genel Stok Muhasebesi genel defteri oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1a90a-111">Several Global Inventory Accounting ledgers can be created for each legal entity in an organization, as required.</span></span> <span data-ttu-id="1a90a-112">Bu nedenle, birden çok stok gösterimi elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="1a90a-112">Therefore, multiple inventory representations can be obtained.</span></span> <span data-ttu-id="1a90a-113">Bir tüzel kişilikte deftere nakledilen tüm belgeler (satınalma siparişleri, satış siparişleri ve transfer emirleri gibi) bu tüzel kişilikle ilişkili tüm maliyet muhasebelerinde hesaba alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="1a90a-113">All documents that are posted in a legal entity (such as purchase orders, sales orders, and transfer orders) will be accounted in all the costing ledgers that are associated with that legal entity.</span></span>

<span data-ttu-id="1a90a-114">Genel Stok Muhasebesi genel defteri, aşağıdaki öğelerin birleşimiyle tanımlanır:</span><span class="sxs-lookup"><span data-stu-id="1a90a-114">A Global Inventory Accounting ledger is defined by a combination of the following elements:</span></span>

- <span data-ttu-id="1a90a-115">Takvim</span><span class="sxs-lookup"><span data-stu-id="1a90a-115">Calendar</span></span>
- <span data-ttu-id="1a90a-116">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="1a90a-116">Currency</span></span>
- <span data-ttu-id="1a90a-117">Döviz kuru tablosu</span><span class="sxs-lookup"><span data-stu-id="1a90a-117">Exchange rate table</span></span>
- <span data-ttu-id="1a90a-118">Kural</span><span class="sxs-lookup"><span data-stu-id="1a90a-118">Convention</span></span>

<span data-ttu-id="1a90a-119">Kural, bir veya daha fazla genel muhasebeyle ilişkilendirilebilen stok muhasebesi ilkeleri topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="1a90a-119">A convention is a collection of inventory accounting policies that can be associated with one or more ledgers.</span></span> <span data-ttu-id="1a90a-120">Kurallar, kuruluşunuzdaki ortak bir ilkeler kümesini paylaşmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1a90a-120">Conventions let you share a common set of policies within your organization.</span></span>

## <a name="availability"></a><span data-ttu-id="1a90a-121">Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="1a90a-121">Availability</span></span>

<span data-ttu-id="1a90a-122">Global Stok Muhasebesi şu anda aşağıdaki Azure coğrafi bölgelerinde kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="1a90a-122">Global Inventory Accounting is currently available in the following Azure geographic regions:</span></span>

- <span data-ttu-id="1a90a-123">Amerika Birleşik Devletleri</span><span class="sxs-lookup"><span data-stu-id="1a90a-123">United States</span></span>
- <span data-ttu-id="1a90a-124">Avrupa</span><span class="sxs-lookup"><span data-stu-id="1a90a-124">Europe</span></span>
- <span data-ttu-id="1a90a-125">Birleşik Krallık</span><span class="sxs-lookup"><span data-stu-id="1a90a-125">United Kingdom</span></span>
- <span data-ttu-id="1a90a-126">Avustralya</span><span class="sxs-lookup"><span data-stu-id="1a90a-126">Australia</span></span>
- <span data-ttu-id="1a90a-127">Kanada</span><span class="sxs-lookup"><span data-stu-id="1a90a-127">Canada</span></span>

<span data-ttu-id="1a90a-128">Eklentiyi başka bir coğrafi bölgeden yüklemeye çalışırsanız, Microsoft Dynamics Lifecycle Services (LCS) coğrafi bölgenizin desteklenmediğini belirten bir ileti gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a90a-128">If you try to install the add-in from another geographic region, Microsoft Dynamics Lifecycle Services (LCS) will show a message that your geographic region isn't supported.</span></span> <span data-ttu-id="1a90a-129">Global Stok Muhasebesi, Supply Chain Management'ın şirket içi dağıtımlarını desteklemez.</span><span class="sxs-lookup"><span data-stu-id="1a90a-129">Global Inventory Accounting doesn't support on-premises deployments of Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="1a90a-130">Lisans</span><span class="sxs-lookup"><span data-stu-id="1a90a-130">Licensing</span></span>

<span data-ttu-id="1a90a-131">Global Stok Muhasebesi, Supply Chain Management için kullanılabilir olan standart maliyet yönetimi özellikleri ile birlikte lisanslanır.</span><span class="sxs-lookup"><span data-stu-id="1a90a-131">Global Inventory Accounting is licensed together with the standard cost management features available for Supply Chain Management.</span></span> <span data-ttu-id="1a90a-132">Global Stok Muhasebesini kullanmak için ek lisans satın almanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="1a90a-132">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>
