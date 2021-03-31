---
title: Karma plaka alımı
description: Bu konu, bir mobil cihaz ile çoklu öğe için iş oluşturma ve kaydetme amacıyla karma plaka alma kullanmayı açıklar.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 948942f137b75c83cc337c5b05300ed8b8857ab8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227734"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="1c372-103">Karma plaka alımı</span><span class="sxs-lookup"><span data-stu-id="1c372-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c372-104">Karma plaka almak, yerine koyma işlemi oluşturmadan önce çoklu öğelerden oluşan bir plaka oluşturmanıza izin verir.</span><span class="sxs-lookup"><span data-stu-id="1c372-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="1c372-105">Birden fazla öğeden oluşan bir plakanın, sizin her bir öğeyi kaydetmeniz için teslim alma noktasında bölünmesi gerekmez.</span><span class="sxs-lookup"><span data-stu-id="1c372-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="1c372-106">Belge satırlarının kaynağını belirlemek için maddeye bağlı akış kullanırken, madde denetimi üzerindeki barkodları taratabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c372-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="1c372-107">Barkodun üzerinde miktar ve bir ölçüm birimi (UOM) yapılandırılmışsa, madde ve miktar otomatik olarak karma plaka eklenir ve başka bir madde taramak için ekrana döndürülürsünüz.</span><span class="sxs-lookup"><span data-stu-id="1c372-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="1c372-108">Bu da tüm maddeleri, her adımda bir onay vermek zorunda kalmadan hızlıca taramanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="1c372-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="1c372-109">Karma plaka alma akışı içerisinde, plakaya taranmış olan maddelerin listesini görüntüleyebilir ve buradan bir maddeyi değiştirebilir veya miktarını düzeltebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c372-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="1c372-110">Uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="1c372-110">Where it applies</span></span>

<span data-ttu-id="1c372-111">Karma plaka alma, çoklu satır/madde için aynı anda kayıt ve iş oluşturma sağlayan bir mobil cihaz alma akışıdır.</span><span class="sxs-lookup"><span data-stu-id="1c372-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="1c372-112">Bu, birden çok öğe içeren gelen plakalar alıyorsanız yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="1c372-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="1c372-113">Karma plaka almanın ayarlanması</span><span class="sxs-lookup"><span data-stu-id="1c372-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="1c372-114">Karma plaka alma, bir mobil cihaz menü öğesi olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="1c372-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="1c372-115">Mevcut işi kullanmayan ve aşağıdaki yöntemlerden birini kullanan, iş moduna sahip yeni bir menü öğesi oluşturmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="1c372-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="1c372-116">Karma plaka alımı</span><span class="sxs-lookup"><span data-stu-id="1c372-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="1c372-117">Karma plaka alımı ve yerine koyma işlemi</span><span class="sxs-lookup"><span data-stu-id="1c372-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="1c372-118">Kaynak belge satırlarını belirlemek için seçenekler şunlardır: satınalma siparişi maddesi, satınalma siparişi satırı, iade siparişi, transfer sipariş maddesi ve transfer emri satırı.</span><span class="sxs-lookup"><span data-stu-id="1c372-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="1c372-119">Bu seçenekler, tek bir plaka üzerindeki alma sırasını değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="1c372-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="1c372-120">Son seçenek yük maddesine göredir.</span><span class="sxs-lookup"><span data-stu-id="1c372-120">The last option is by load item.</span></span> <span data-ttu-id="1c372-121">Birden fazla maddeyi bir plakaya ekleyebilirsiniz ancak çoklu yükler arasında geçiş yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="1c372-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]