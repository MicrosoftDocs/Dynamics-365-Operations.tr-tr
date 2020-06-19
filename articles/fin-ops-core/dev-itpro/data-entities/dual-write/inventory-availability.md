---
title: Çift yazılarda stok kullanılabilirliği
description: Bu konu, çift yazmada envanter kullanılabilirliğini kontrol etme hakkında bilgi sağlar.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426994"
---
# <a name="inventory-availability"></a><span data-ttu-id="0e8c8-103">Stok kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="0e8c8-103">Inventory availability</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0e8c8-104">Stok kullanılabilirliğini kullanarak, Dynamics 365 ' te model odaklı uygulamalardaki bir ürünü **tekliflere**, **siparişlere** veya **faturalara** eklemek için Stoğunuzu kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e8c8-104">Using inventory availability, you can check your inventory before you add a product into the **Quotes**, **Orders**, or **Invoices** forms in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="0e8c8-105">Örneğin, stok denetimi ve tam bir tarihi belirleme [aday müşteri nakit](dual-write-prospect-to-cash.md) işlemindeki anahtar görevdir .</span><span class="sxs-lookup"><span data-stu-id="0e8c8-105">For example, checking inventory and determining a fulfullment date is a key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span> <span data-ttu-id="0e8c8-106">Yeterli stoğa sahip değilseniz, tahmini stok alış irsaliyelerine ve çıkışlarına göre bir teslimat tarihi tahmin edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e8c8-106">If you don't have enough inventory, you can estimate a delivery date based on projected inventory receipts and issues.</span></span> <span data-ttu-id="0e8c8-107">Ayrıca, ATP miktarını önceden tanımlanmış zaman diliminden bulabileceğiniz, maddenin taahhüt edilebilir (ATP) bilgilerini de denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e8c8-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the pre-defined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="0e8c8-108">Eldeki Stok</span><span class="sxs-lookup"><span data-stu-id="0e8c8-108">On-hand Inventory</span></span> 

<span data-ttu-id="0e8c8-109">Dynamics 365 Sales içindeki **teklif**, **sipariş** veya **fatura** formlarının üstbilgisinde Yeni bir düğme **Eldeki stok** eklenir.</span><span class="sxs-lookup"><span data-stu-id="0e8c8-109">In the header of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **On-hand Inventory** is added.</span></span> <span data-ttu-id="0e8c8-110">Düğmeyi tıklattığınızda, bir iletişim kutusu görüntülenir ve eldeki stoğu denetlemek istediğiniz şirketi ve ürünü belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e8c8-110">When you click the button, a dialog box appears and you can specify the company and the product for which you want to check the on-hand inventory.</span></span> <span data-ttu-id="0e8c8-111">Stok bilgilerini Dynamics 365 Supply Chain Management'den döndürür ve [eldeki stokla](../../../../supply-chain/inventory/tasks/check-availability-stock.md) aynı bilgileri gösterir .</span><span class="sxs-lookup"><span data-stu-id="0e8c8-111">It returns the inventory information from Dynamics 365 Supply Chain Management, and shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span> <span data-ttu-id="0e8c8-112">Bilgiler şu miktarları içerir:</span><span class="sxs-lookup"><span data-stu-id="0e8c8-112">The information includes these quantities:</span></span>

- <span data-ttu-id="0e8c8-113">**Eldeki Miktar**</span><span class="sxs-lookup"><span data-stu-id="0e8c8-113">**On-hand Quantity**</span></span>
- <span data-ttu-id="0e8c8-114">**Kaydedilen Eldeki Miktar**</span><span class="sxs-lookup"><span data-stu-id="0e8c8-114">**Reserved On-hand Quantity**</span></span>
- <span data-ttu-id="0e8c8-115">**Kullanılabilir Eldeki Miktar**</span><span class="sxs-lookup"><span data-stu-id="0e8c8-115">**Available On-hand Quantity**</span></span>
- <span data-ttu-id="0e8c8-116">**Sipariş verilen miktarı**</span><span class="sxs-lookup"><span data-stu-id="0e8c8-116">**Orderd Quantity**</span></span>
- <span data-ttu-id="0e8c8-117">**Siparişteki Miktar**</span><span class="sxs-lookup"><span data-stu-id="0e8c8-117">**On-order Quantity**</span></span>
- <span data-ttu-id="0e8c8-118">**Ayrılan sipariş edilen miktar**</span><span class="sxs-lookup"><span data-stu-id="0e8c8-118">**Reserved Ordered Quantity**</span></span>
- <span data-ttu-id="0e8c8-119">**Toplam kullanılabilir miktar**</span><span class="sxs-lookup"><span data-stu-id="0e8c8-119">**Total Available Quantity**</span></span>

## <a name="atp-information"></a><span data-ttu-id="0e8c8-120">KM bilgileri</span><span class="sxs-lookup"><span data-stu-id="0e8c8-120">ATP information</span></span>

<span data-ttu-id="0e8c8-121">Dynamics 365 Sales içindeki **teklif**, **sipariş** veya **fatura** formlarının üstbilgisinde Yeni bir düğme **ATP bilgileri** eklenir.</span><span class="sxs-lookup"><span data-stu-id="0e8c8-121">On line items of the **Quotes**, **Orders**, or **Invoices** forms in Dynamics 365 Sales, a new button **ATP Information** is added.</span></span> <span data-ttu-id="0e8c8-122">Düğmeyi tıklattığınızda, bir iletişim kutusu görüntülenir ve şirketi, envanter sahasını, envanter deposunu ve sipariş miktarını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e8c8-122">When you click the button, a dialog box appears and you can specify the company, product, inventory Site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="0e8c8-123">Supply Chain Management'tan **ATP bilgileri** iade edin ve [sipariş taahhüdünden](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) alınan ayarları gösterir .</span><span class="sxs-lookup"><span data-stu-id="0e8c8-123">It returns the **ATP Information** from Supply Chain Management and shows the settings descrbed in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span> <span data-ttu-id="0e8c8-124">Bu bilgiler **ATP miktarını**, **giriş miktarını**, **Stok çıkış miktarını** ve **Eldeki miktarı** içerir.</span><span class="sxs-lookup"><span data-stu-id="0e8c8-124">The information includes **ATP quantity**, **Receipt quantity**, **Issue quantity**, and **On-hand quantity**.</span></span>
