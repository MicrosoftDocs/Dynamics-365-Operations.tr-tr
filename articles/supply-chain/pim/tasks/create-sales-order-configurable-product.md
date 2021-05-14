---
title: Yapılandırılabilir ürün için satış siparişi oluşturma
description: Bu yordam bir yapılandırma şablonunun satış siparişindeki bir ürüne nasıl uygulanacağını gösterir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921301"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="f6a02-103">Yapılandırılabilir ürün için satış siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f6a02-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6a02-104">Bu yordam bir yapılandırma şablonunun satış siparişindeki bir ürüne nasıl uygulanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6a02-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="f6a02-105">Bu örnek, USMF demo veri şirketindeki D0006 hoparlör modelini kullanır.</span><span class="sxs-lookup"><span data-stu-id="f6a02-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="f6a02-106">Genel olarak bu yordamı bir satış siparişi işlemcisi kullanır.</span><span class="sxs-lookup"><span data-stu-id="f6a02-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="f6a02-107">Satış siparişi oluştur</span><span class="sxs-lookup"><span data-stu-id="f6a02-107">Create a sales order</span></span>

1. <span data-ttu-id="f6a02-108">**Satış ve pazarlama \> Çalışma alanları \> Satış siparişi işleme ve sorgulama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="f6a02-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-109">Select **New**.</span></span>
1. <span data-ttu-id="f6a02-110">**Satış siparişi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="f6a02-111">**Müşteri hesabı** alanında *US-001*'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="f6a02-112">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-112">Select **OK**.</span></span>
1. <span data-ttu-id="f6a02-113">**Öğe numarası** alanında, *D0006*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="f6a02-114">Bu görev için yapılandırılabilir bir ürün seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f6a02-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="f6a02-115">**Ürün ve tedarik**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="f6a02-116">**Satırı yapılandır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="f6a02-117">Fiyatın seçilen yapılandırmaya göre değiştiğini ve **Kabloyu dahil et** alanının şimdi *Doğru* olarak ayarlandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f6a02-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="f6a02-118">Kablo için seçilen varsayılan fiyatı ve ayarları not alın.</span><span class="sxs-lookup"><span data-stu-id="f6a02-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="f6a02-119">**Şablon yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-119">Select **Load template**.</span></span>
    * <span data-ttu-id="f6a02-120">Bu örnek, önceden tanımlanmış bir yapılandırmayı seçmek için bir şablonu nasıl uygulayabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6a02-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="f6a02-121">Bu yordamı bir görev kılavuzu olarak kullanıyorsanız ve kullanılabilir diğer öznitelik değerlerini görmek istiyorsanız **Kilidi aç** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="f6a02-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-122">Select **OK**.</span></span>
1. <span data-ttu-id="f6a02-123">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-123">Select **OK**.</span></span>
1. <span data-ttu-id="f6a02-124">**Satır ayrıntıları** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="f6a02-125">**Ürün** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="f6a02-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="f6a02-126">Madde yapılandırılması artık ürün boyutları altında listelenir.</span><span class="sxs-lookup"><span data-stu-id="f6a02-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="f6a02-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f6a02-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]