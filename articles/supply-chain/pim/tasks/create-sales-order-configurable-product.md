--- 
title: "Yapılandırılabilir ürün için satış siparişi oluşturma"
description: "Bu yordam bir yapılandırma şablonunun satış siparişindeki bir ürüne nasıl uygulanacağını gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e9b42a7343dacc1bcd995c10a4b90a87998a31ba
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="1ca24-103">Yapılandırılabilir ürün için satış siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ca24-103">Create a sales order for a configurable product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1ca24-104">Bu yordam bir yapılandırma şablonunun satış siparişindeki bir ürüne nasıl uygulanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ca24-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="1ca24-105">Bu örnek, USMF demo veri şirketindeki D0006 hoparlör modelini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1ca24-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="1ca24-106">Genel olarak bu yordamı bir satış siparişi işlemcisi kullanır.</span><span class="sxs-lookup"><span data-stu-id="1ca24-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="1ca24-107">Satış siparişi oluştur</span><span class="sxs-lookup"><span data-stu-id="1ca24-107">Create a sales order</span></span>
1. <span data-ttu-id="1ca24-108">Satış siparişi işleme ve sorgulama'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="1ca24-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-109">Click New.</span></span>
3. <span data-ttu-id="1ca24-110">Satış siparişi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-110">Click Sales order.</span></span>
4. <span data-ttu-id="1ca24-111">Müşteri hesabı alanında US-001'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1ca24-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="1ca24-112">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-112">Click OK.</span></span>
6. <span data-ttu-id="1ca24-113">Madde numarası alanında D0006 seçin.</span><span class="sxs-lookup"><span data-stu-id="1ca24-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="1ca24-114">Bu görev için yapılandırılabilir bir ürün seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="1ca24-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="1ca24-115">Ürün ve tedarik seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-115">Click Product and supply.</span></span>
8. <span data-ttu-id="1ca24-116">Yapılandırma satırı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-116">Click Configure line.</span></span>
    * <span data-ttu-id="1ca24-117">Fiyatın seçilen yapılandırmaya göre değiştiğini ve Kabloyu dahil et alanının şimdi Doğru olarak ayarlandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="1ca24-118">Kablo için seçilen varsayılan fiyatı ve ayarları not alın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="1ca24-119">Şablonu yükle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-119">Click Load template.</span></span>
    * <span data-ttu-id="1ca24-120">Bu örnek, önceden tanımlanmış bir yapılandırmayı seçmek için bir şablonu nasıl uygulayabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ca24-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="1ca24-121">Bu yordamı bir görev kılavuzu olarak kullanıyorsanız ve kullanılabilir diğer öznitelik değerlerini görmek istiyorsanız Kilidi aç düğmesine tıklamalısınız.</span><span class="sxs-lookup"><span data-stu-id="1ca24-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="1ca24-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-122">Click OK.</span></span>
11. <span data-ttu-id="1ca24-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-123">Click OK.</span></span>
12. <span data-ttu-id="1ca24-124">Satır ayrıntıları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1ca24-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="1ca24-125">Ürün sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-125">Click the Product tab.</span></span>
    * <span data-ttu-id="1ca24-126">Madde yapılandırılması artık ürün boyutları altında listelenir.</span><span class="sxs-lookup"><span data-stu-id="1ca24-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="1ca24-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1ca24-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="1ca24-128">Ürün yapılandırmasını seçme</span><span class="sxs-lookup"><span data-stu-id="1ca24-128">Select the product configuration</span></span>


