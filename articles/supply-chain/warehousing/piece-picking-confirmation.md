---
title: "Parça çekme onayı"
description: "Bu konu bir mobil cihazdan parça çekme onayının nasıl ayarlanacağını ve uygulanacağını açıklamaktadır."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 31b285f06ea8b7951f2439637a4fccb83db31578
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="piece-picking-confirmation"></a><span data-ttu-id="4c666-103">Parça çekme onayı</span><span class="sxs-lookup"><span data-stu-id="4c666-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c666-104">Parça çekme, bir mobil cihazda çekme veya sayım işi aracılığıyla stoktaki her parçayı onaylamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4c666-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="4c666-105">Çekme işleri için, işte çekim için belirtilen miktara kadar olan miktarda işi onaylayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c666-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="4c666-106">Sayım işi için, saydığınız stoğu tarayabilir ve toplam tutarı izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c666-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="4c666-107">Parça çekmeyi etkinleştirdiğinizde, ürün onayı otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="4c666-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="4c666-108">İş türü çekmeler için, maksimum parça sayısı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4c666-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="4c666-109">Bu, parça sayısı için iş işlenirken onaylanması gereken maksimum değeri ayarlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="4c666-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="4c666-110">Maksimum miktar işlenmekte olan geçerli iş birimini temel alır.</span><span class="sxs-lookup"><span data-stu-id="4c666-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="4c666-111">Sayım iş türü maksimum ayarlanmasına izin vermez.</span><span class="sxs-lookup"><span data-stu-id="4c666-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="4c666-112">Taranan bir barkodla ilişkili olan miktarı ve ölçü birimini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c666-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="4c666-113">Karma plaka alma, satınalma siparişi maddesi, transfer emri maddesi ve yük maddesi de dahil olmak üzere gelen akışlar üzerinde alma için işe yarar.</span><span class="sxs-lookup"><span data-stu-id="4c666-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="4c666-114">Ayrıca, barkod tarama işleminin miktarı onaylanan toplam parça sayısına barkod ile iş birimi üzerindeki ölçü birimine göre dönüştürme yaparak eklediği parça çekme işleminde de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c666-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="4c666-115">Barkod üzerindeki ölçü birimi sayımı yapılırken, miktarın sıra grubunda sayımına izin verildiği onaylanırsa, miktar toplam sayıma eklenir.</span><span class="sxs-lookup"><span data-stu-id="4c666-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="4c666-116">Uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="4c666-116">Where it applies</span></span>

<span data-ttu-id="4c666-117">Parça çekme tüm sayım işlemleri ve herhangi bir iş türü için ilk çekme işleminde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4c666-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="4c666-118">Parça çekme, madde seri numaraları tarafından denetleniyorsa veya bir plaka konumundan yapılan bir kanban veya üretim çekme işlemiyse ve madde aşamalandırma için ayarlandıysa kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="4c666-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="4c666-119">Parça çekme işlemini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4c666-119">Set up piece picking</span></span>

1.  <span data-ttu-id="4c666-120">Mobil cihaz menü öğesinden iş onayı için kurulum formunu açın: Ambar yönetimi > **Ambar yönetimi** > **Kurulum** > **Mobil cihaz** > **Mobil cihaz menü öğeleri**.</span><span class="sxs-lookup"><span data-stu-id="4c666-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="4c666-121">Mobil cihaz menü öğesinden İş onayı ayarını açın.</span><span class="sxs-lookup"><span data-stu-id="4c666-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="4c666-122">İş türü çekme veya sayım olduğunda aşağıdaki seçenekler seçim için kullanılabilir hale gelir.</span><span class="sxs-lookup"><span data-stu-id="4c666-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="4c666-123">Seçenek</span><span class="sxs-lookup"><span data-stu-id="4c666-123">Option</span></span>           |                                                                            <span data-ttu-id="4c666-124">Açıklama</span><span class="sxs-lookup"><span data-stu-id="4c666-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c666-125">Parça çekme onayı</span><span class="sxs-lookup"><span data-stu-id="4c666-125">Piece picking confirmation</span></span> | <span data-ttu-id="4c666-126">Çekme ve sayım iş türleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c666-126">Available for pick and counting work types.</span></span> <span data-ttu-id="4c666-127">Ürün onayı otomatik olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="4c666-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="4c666-128">Her stok parçasını mobil cihazınızdan onaylamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4c666-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="4c666-129">Maksimum parça sayısı</span><span class="sxs-lookup"><span data-stu-id="4c666-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="4c666-130">Parça çekme onayı etkinleştirilmişse, çekme işi için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4c666-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="4c666-131">Onaylamak zorunda olduğunuz parça sayısı için bir sınır ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c666-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |


