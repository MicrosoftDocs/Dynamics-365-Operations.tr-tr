---
title: Servis siparişleri için madde gereksinimleri oluşturma
description: Bir servis siparişi için belirli maddeleri rezerve etmeniz gerekiyorsa, bunun için stok madde gereksinimleri oluşturabilirsiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5a730ae945af15c7bd4020c734bac971d8186e2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553427"
---
# <a name="create-item-requirements-for-service-orders"></a><span data-ttu-id="fe4f2-103">Servis siparişleri için madde gereksinimleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe4f2-103">Create item requirements for service orders</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="fe4f2-104">Müşterilerinize sağladığınız hizmetleri yönetmek ve izlemek için servis siparişi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="fe4f2-105">Bir servis siparişi için belirli maddeleri rezerve etmeniz gerekiyorsa, bunun için stok madde gereksinimleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="fe4f2-106">Bir madde gereksinimi hemen stoktan tüketilebilir ya da madde için üretim emri başlatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="fe4f2-107">Madde hareketi yerine madde gereksinimi kullanarak, madde gerçekten kullanılmadan hemen önce teslimat planı yapabilir, bir satın alma siparişi oluşturabilir, maddeyi ticari anlaşma çerçevesine dahil edebilir ve madde gereksinimini üretim planlamasına dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="fe4f2-108">Servis siparişleri için madde gereksinimleri bir proje aracılığıyla işlenir.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="fe4f2-109">Bir servis siparişinde madde gereksinimi oluşturmak için, servis siparişinin bir projeye atanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-109">To create an item requirement on a service order, the service order must be assigned to a project.</span></span> <span data-ttu-id="fe4f2-110">Servis siparişi için madde gereksinimi oluşturduktan sonra madde gereksinimini seçilen projenin **Projeler** formundan görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-110">After you create an item requirement for a service order, you can view the item requirement in the **Projects** form for the selected project.</span></span>

## <a name="create-an-item-requirement-for-a-service-order"></a><span data-ttu-id="fe4f2-111">Servis siparişi için madde gereksinimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe4f2-111">Create an item requirement for a service order</span></span>

1.  <span data-ttu-id="fe4f2-112">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="fe4f2-113">Madde gereksinimi oluşturmak istediğiniz servis siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-113">Select the service order that you want to create an item requirement for.</span></span>

3.  <span data-ttu-id="fe4f2-114">**Eylem Bölmesinde**, **Gönder** sekmesinde **Madde gereksinimi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-114">On the **Action Pane**, on the **Dispatch** tab, click **Item requirement**.</span></span>

4.  <span data-ttu-id="fe4f2-115">**Madde gereksinimleri** formunda, gereken madde için bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-115">In the **Item requirements** form, enter information for the required item.</span></span> <span data-ttu-id="fe4f2-116">Belirli alanlar hakkında daha fazla bilgi için bkz. [Madde gereksinimleri (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span><span class="sxs-lookup"><span data-stu-id="fe4f2-116">For more information about the specific fields, see [Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).</span></span>

## <a name="create-an-item-requirement-for-a-service-agreement"></a><span data-ttu-id="fe4f2-117">Servis sözleşmesi için madde gereksinimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe4f2-117">Create an item requirement for a service agreement</span></span>

1.  <span data-ttu-id="fe4f2-118">**Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-118">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="fe4f2-119">Madde gereksinimi oluşturmak istediğiniz servis sözleşmesini açın.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-119">Open the service agreement for which you want to create an item requirement.</span></span>

3.  <span data-ttu-id="fe4f2-120">**Satırlar** hızlı sekmesinde yeni bir satır oluşturmak için **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-120">On the **Lines** FastTab, click **Add** to create a new line.</span></span>

4.  <span data-ttu-id="fe4f2-121">**Hareket türü** alanında **Madde**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-121">In the **Transaction type** field, select **Item**.</span></span>

5.  <span data-ttu-id="fe4f2-122">**Madde kurulumu** alanında **Madde gereksinimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-122">In the **Item setup** field, select **Item requirement**.</span></span>

6.  <span data-ttu-id="fe4f2-123">**Madde numarası** alanında, servis sözleşmesi için gereken maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-123">In the **Item number** field, select the item that is required for the service agreement.</span></span>

7.  <span data-ttu-id="fe4f2-124">**Satır ayrıntıları** hızlı sekmesinde, **Ürün boyutları** sekmesindeki **Tesis** alanında, madde için stok tesisi seçin.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-124">On the **Line details** FastTab, on the **Product dimensions** tab, in the **Site** field, select the inventory site for the item.</span></span>

8.  <span data-ttu-id="fe4f2-125">Bir sözleşme satırından servis siparişi oluşturmak için **Satırlar** hızlı sekmesinde **Servis siparişleri oluştur**'a tıklayın ve **Servis siparişleri oluştur** formuna ilgili bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-125">To create a service order from the agreement line, on the **Lines** FastTab, click **Create service orders**, and then enter the relevant information in the **Create service orders** form.</span></span> 


## <a name="see-also"></a><span data-ttu-id="fe4f2-126">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="fe4f2-126">See also</span></span>

<span data-ttu-id="fe4f2-127">[Servis siparişlerini otomatik olarak oluşturma](create-service-orders-automatically.md)</span><span class="sxs-lookup"><span data-stu-id="fe4f2-127">[Create service orders automatically](create-service-orders-automatically.md).</span></span>

  


