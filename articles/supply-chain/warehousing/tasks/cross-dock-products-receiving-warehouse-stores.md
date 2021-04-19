---
title: Ürünleri teslim alan ambardan mağazalara çapraz sevk etme
description: Bu yordam, ürünleri satınalma siparişinin alma konumundan bir veya daha fazla mağazaya dağıtmak için Çapraz sevk oluşturma ve işleme konusunda kılavuzluk sağlar.
author: ShylaThompson
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailBuyersPushPerPackage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7caec5329774baaa03c72f9236f8e3192399089
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810402"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="f392e-103">Ürünleri teslim alan ambardan mağazalara çapraz sevk etme</span><span class="sxs-lookup"><span data-stu-id="f392e-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f392e-104">Bu yordam, ürünleri satınalma siparişinin alma konumundan bir veya daha fazla mağazaya dağıtmak için Çapraz sevk oluşturma ve işleme konusunda kılavuzluk sağlar.</span><span class="sxs-lookup"><span data-stu-id="f392e-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="f392e-105">Kullanıcı birden çok yapılandırmalar tanımlayabilir ve ürünlerin nasıl dağıtılacağını sistemin önermesini isteyebilir ya da ürünlerin nereye dağıtılacağını ve her mağazaya ne kadar dağıtım yapılacağını el ile girebilir.</span><span class="sxs-lookup"><span data-stu-id="f392e-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="f392e-106">Yordam Çapraz sevkte kullanılabilecek stok yenileme kuralları, kuruluş hiyerarşileri ve mağaza ağırlıkları gibi verilerin ayarlanmasını kapsamaz.</span><span class="sxs-lookup"><span data-stu-id="f392e-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="f392e-107">Yordam, USRT demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f392e-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="f392e-108">Tüm satınalma siparişleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f392e-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="f392e-109">Listeden bir satınalma siparişi seçin ve siparişi açmak için bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f392e-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="f392e-110">Eylem bölmesinde Retail and Commerce'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f392e-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="f392e-111">Çapraz sevki tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f392e-111">Click Cross docking.</span></span>
5. <span data-ttu-id="f392e-112">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f392e-112">Click Edit.</span></span>
    * <span data-ttu-id="f392e-113">Kategori Satırlar bölümündeki maddeleri filtrelemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f392e-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="f392e-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f392e-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f392e-115">Çapraz sevk miktarı alanına, seçilen üründen satın alınan ne kadar miktarın dağıtılacağını belirtmek için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f392e-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="f392e-116">Ek çapraz sevk miktarı alanına, satın alınan kullanılabilir ürünler için dağıtılacak miktarları belirtmek için bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f392e-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="f392e-117">Dağıtım alanına 'Yerleşim ağırlığı' girin.</span><span class="sxs-lookup"><span data-stu-id="f392e-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="f392e-118">Dağıtım için farklı kurallar kullanmak üzere diğer türleri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f392e-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="f392e-119">Atok yenileme hiyerarşisi alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f392e-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="f392e-120">Ürün çeşitlerini dikkate al alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f392e-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="f392e-121">Miktarları hesapla'yı tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f392e-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="f392e-122">Sipariş oluştur'u tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f392e-122">Click Create order.</span></span>
14. <span data-ttu-id="f392e-123">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f392e-123">Click Yes.</span></span>
15. <span data-ttu-id="f392e-124">Listede ürünlerin teslim alındığı ambarı bulup seçin</span><span class="sxs-lookup"><span data-stu-id="f392e-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="f392e-125">Seçilen ambar için oluşturulan siparişleri görüntülemek için Sipariş'i tıklayın</span><span class="sxs-lookup"><span data-stu-id="f392e-125">Click Order to view the orders that got created for the selected warehouse</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]