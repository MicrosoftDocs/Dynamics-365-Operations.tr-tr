---
title: Stoğu olmayan maddeler ödeme sayfasına yönlendirilebiliyor
description: Bu konu, müşterilerin stoğu olmayan maddeleri alışveriş sepetlerine ekleyebildiği ve ödeme sayfasına ilerleyebildiği durumlarda yardımcı olan sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018470"
---
# <a name="items-without-inventory-can-be-checked-out"></a><span data-ttu-id="27d69-103">Stoğu olmayan maddeler ödeme sayfasına yönlendirilebiliyor</span><span class="sxs-lookup"><span data-stu-id="27d69-103">Items without inventory can be checked out</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="27d69-104">Bu konu, müşterilerin stoğu olmayan maddeleri alışveriş sepetlerine ekleyebildiği ve ödeme sayfasına ilerleyebildiği durumlarda yardımcı olan sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="27d69-104">This topic provides troubleshooting guidance that can help when customers can add out-of-stock items to their cart and proceed to checkout.</span></span>

## <a name="description"></a><span data-ttu-id="27d69-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27d69-105">Description</span></span>

<span data-ttu-id="27d69-106">Kullanıcılar elde stoğu olmayan bir maddeyi sepetine ekleyebiliyor ve ödeme sayfasına ilerleyebiliyor.</span><span class="sxs-lookup"><span data-stu-id="27d69-106">Users can add an item to their cart, even though there is no on-hand inventory in the store, and then proceed to the checkout page.</span></span>

## <a name="resolution"></a><span data-ttu-id="27d69-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="27d69-107">Resolution</span></span>

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a><span data-ttu-id="27d69-108">Commerce Site Builder'da stokta yok hatalarını göster özelliğini etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="27d69-108">Enable the Show Out Of Stock Errors property in Commerce site builder</span></span>

<span data-ttu-id="27d69-109">Commerce Site Builder'da **stokta yok hatalarını göster** özelliğini etkinleştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="27d69-109">To enable the **Show Out Of Stock Errors** property in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="27d69-110">Üzerinde çalıştığınız siteyi seçin.</span><span class="sxs-lookup"><span data-stu-id="27d69-110">Select the site that you're working on.</span></span>
1. <span data-ttu-id="27d69-111">Soldaki gezinti bölmesinde **Sayfalar** seçin.</span><span class="sxs-lookup"><span data-stu-id="27d69-111">In the left navigation, select **Pages**.</span></span>
1. <span data-ttu-id="27d69-112">Açmak için **cartpage**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="27d69-112">Select **CartPage** to open it.</span></span>
1. <span data-ttu-id="27d69-113">**Sepet 1** yuvasını seçin , **Düzenle**'yi seçin ve sonra Özellikler bölmesinde **Stokta yok hatalarını göster** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="27d69-113">Select the **Cart 1** slot, select **Edit**, and then, in the properties pane, select the **Show Out Of Stock Errors** check box.</span></span>
1. <span data-ttu-id="27d69-114">Sayfayı kaydedip yayınlayın.</span><span class="sxs-lookup"><span data-stu-id="27d69-114">Save and publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27d69-115">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="27d69-115">Additional resources</span></span>

[<span data-ttu-id="27d69-116">Stok ayarlarını uygulama</span><span class="sxs-lookup"><span data-stu-id="27d69-116">Apply inventory settings</span></span>](../inventory-settings.md)

[<span data-ttu-id="27d69-117">Perakende kanalları için stok kullanılabilirliğini hesaplama</span><span class="sxs-lookup"><span data-stu-id="27d69-117">Calculate inventory availability for retail channels</span></span>](../calculated-inventory-retail-channels.md)

[<span data-ttu-id="27d69-118">Stok arabellekleri ve stok düzeyleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="27d69-118">Configure inventory buffers and inventory levels</span></span>](../inventory-buffers-levels.md)
