---
title: "Servis siparişi madde gereksinimleri"
description: "Bir servis siparişi için belirli maddeleri rezerve etmeniz gerekiyorsa, bunun için stok madde gereksinimleri oluşturabilirsiniz."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 880d41a5b3d8c9200a0a1f4b13af2d6d24d30766
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-item-requirements"></a><span data-ttu-id="ca4d8-103">Servis siparişi madde gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="ca4d8-103">Service order item requirements</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ca4d8-104">Müşterilerinize sağladığınız hizmetleri yönetmek ve izlemek için servis siparişi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-104">You can create a service order to track and manage services that you provide to your customers.</span></span> <span data-ttu-id="ca4d8-105">Bir servis siparişi için belirli maddeleri rezerve etmeniz gerekiyorsa, bunun için stok madde gereksinimleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-105">If you need to reserve specific items for a service order, you can create inventory item requirements for it.</span></span> <span data-ttu-id="ca4d8-106">Bir madde gereksinimi hemen stoktan tüketilebilir ya da madde için üretim emri başlatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-106">An item requirement can be immediately consumed from inventory, or it can initiate a production order for the item.</span></span>

<span data-ttu-id="ca4d8-107">Madde hareketi yerine madde gereksinimi kullanarak, madde gerçekten kullanılmadan hemen önce teslimat planı yapabilir, bir satın alma siparişi oluşturabilir, maddeyi ticari anlaşma çerçevesine dahil edebilir ve madde gereksinimini üretim planlamasına dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-107">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span>

<span data-ttu-id="ca4d8-108">Servis siparişleri için madde gereksinimleri bir proje aracılığıyla işlenir.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-108">Item requirements for service orders are processed through a project.</span></span> <span data-ttu-id="ca4d8-109">Bir servis siparişinde madde gereksinimi oluşturmak için, servis siparişinin bir projeye eklenmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-109">To create an item requirement on a service order, the service order must be attached to a project.</span></span>

<span data-ttu-id="ca4d8-110">Bir servis siparişi için bir madde gereksinimi oluşturulur oluşturulmaz, bireysel servis siparişindeki **Proje**'den veya **Satış siparişi** formu üzerinden görüntülenebilir.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-110">As soon as an item requirement is created for a service order, it can be viewed from **Project** in the individual service order or through the **Sales order** form.</span></span>

## <a name="view-an-item-requirement-from-a-service-order"></a><span data-ttu-id="ca4d8-111">Bir servis siparişinden madde gereksinimi görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ca4d8-111">View an item requirement from a service order</span></span>

1.  <span data-ttu-id="ca4d8-112">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-112">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ca4d8-113">**Gönder**'e ve ardından **Madde gereksinimi**'ne tıklayarak **Madde gereksinimleri** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-113">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span>

3.  <span data-ttu-id="ca4d8-114">Madde gereksiniminin servis siparişlerini görmek için, **Proje** sekmesini tıklatın ve **Servis siparişi** alanını işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-114">Click the **Project** tab, and check the **Service order** field to see the service orders of the item requirement.</span></span>

## <a name="delete-service-orders-with-item-requirements"></a><span data-ttu-id="ca4d8-115">Madde gereksinimi olan servis siparişlerini silme</span><span class="sxs-lookup"><span data-stu-id="ca4d8-115">Delete service orders with item requirements</span></span>

<span data-ttu-id="ca4d8-116">Bir servis siparişinde bir madde gereksinimi oluşturulmuşsa, servis siparişini silemezsini.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-116">If an item requirement is created on a service order, you cannot delete the service order.</span></span> <span data-ttu-id="ca4d8-117">Servis siparişini silebilmeniz için madde gereksinimini silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-117">You must delete the item requirement before you can delete the service order.</span></span>

1.  <span data-ttu-id="ca4d8-118">**Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-118">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="ca4d8-119">**Gönder**'e ve ardından **Madde gereksinimi**'ne tıklayarak **Madde gereksinimleri** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-119">Click **Dispatch**, and then click **Item requirement** to open the **Item requirements** form.</span></span> <span data-ttu-id="ca4d8-120">Bu form servis siparişinde oluşturulan tüm madde gereksinimlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-120">This form lists the item requirements that are created on the service order.</span></span>

3.  <span data-ttu-id="ca4d8-121">Silinecek madde gereksinimini seçin ve ardından **Sil** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-121">Select the item requirement to delete, and then click **Delete**.</span></span>

<span data-ttu-id="ca4d8-122">veya</span><span class="sxs-lookup"><span data-stu-id="ca4d8-122">–or–</span></span>

1.  <span data-ttu-id="ca4d8-123">**Proje yönetimi ve muhasebe** \> **Genel** \> **Projeler** \> **Tüm projeler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-123">Click **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="ca4d8-124">Bir madde gereksiniminin oluşturulduğu servis siparişine sahip projeyi açın.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-124">Open the project that has the service order in which an item requirement is created.</span></span>

3.  <span data-ttu-id="ca4d8-125">**Projeler** formunda sağ bölmede **Madde gereksinimleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-125">In the **Projects** form, in the right pane, click **Item requirements**.</span></span> <span data-ttu-id="ca4d8-126">**Madde gereksinimleri** formu seçili projeyle ilişkili madde gereksinimlerini listeler.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-126">The **Item requirements** form lists the item requirements that are associated with the selected project.</span></span>

4.  <span data-ttu-id="ca4d8-127">Silinecek madde gereksinimini seçin ve ardından **Sil** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-127">Select the item requirement to delete, and then click **Delete**.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca4d8-128">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="ca4d8-128">See also</span></span>

<span data-ttu-id="ca4d8-129">[Madde gereksinimleri (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="ca4d8-129">[Item requirements (form)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\))</span></span>

