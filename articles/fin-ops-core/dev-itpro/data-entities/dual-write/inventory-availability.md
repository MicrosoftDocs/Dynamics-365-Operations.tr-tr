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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997904"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="2d614-103">Çift yazılarda stok kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="2d614-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2d614-104">Stok kullanılabilirliğini kullanarak, bir ürünü Microsoft Dynamics 365 Sales'te model temelli uygulamalardaki **Teklifler** , **Siparişler** veya **Faturalar** sayfasına eklemeden önce Stoğunuzu kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d614-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations** , **Orders** , or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="2d614-105">Örneğin, stok denetimi ve karşılama tarihi belirleme [aday müşteriden nakde](dual-write-prospect-to-cash.md) işlemindeki anahtar görevdir.</span><span class="sxs-lookup"><span data-stu-id="2d614-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="2d614-106">Yeterli stoğa sahip değilseniz, tahmini stok alış girişlerine ve çıkışlarına göre bir teslimat tarihi tahmin edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d614-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="2d614-107">Ayrıca, ATP miktarını önceden tanımlanmış zaman diliminden bulabileceğiniz, maddenin taahhüt edilebilir (ATP) bilgilerini de denetleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d614-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="2d614-108">Eldeki stok</span><span class="sxs-lookup"><span data-stu-id="2d614-108">On-hand inventory</span></span>

<span data-ttu-id="2d614-109">Dynamics 365 Sales'te **Teklifler** , **Siparişler** ve **Fatura** sayfalarının başlığına yen bir **Eldeki stok** düğmesi eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="2d614-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="2d614-110">Bu düğmeyi seçtiğinizde, bir iletişim kutusu görüntülenir ve eldeki stoğu denetlemek istediğiniz şirketi ve ürünü burada belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d614-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="2d614-111">Bu iletişim kutusu [Eldeki stok](../../../../supply-chain/inventory/tasks/check-availability-stock.md) ile aynı bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d614-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="2d614-112">İletişim kutusu Dynamics 365 Supply Chain Management'tan stok bilgilerini getirir.</span><span class="sxs-lookup"><span data-stu-id="2d614-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="2d614-113">Bilgiler aşağıdaki miktarları içerir:</span><span class="sxs-lookup"><span data-stu-id="2d614-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="2d614-114">Eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="2d614-114">On-hand quantity</span></span>
- <span data-ttu-id="2d614-115">Tersine çevrilen eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="2d614-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="2d614-116">Kullanılabilir eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="2d614-116">Available on-hand quantity</span></span>
- <span data-ttu-id="2d614-117">Sipariş miktarı</span><span class="sxs-lookup"><span data-stu-id="2d614-117">Ordered quantity</span></span>
- <span data-ttu-id="2d614-118">Siparişteki miktar</span><span class="sxs-lookup"><span data-stu-id="2d614-118">On-order quantity</span></span>
- <span data-ttu-id="2d614-119">Ayrılan sipariş edilen miktar</span><span class="sxs-lookup"><span data-stu-id="2d614-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="2d614-120">Toplam kullanılabilir miktar</span><span class="sxs-lookup"><span data-stu-id="2d614-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="2d614-121">KM bilgileri</span><span class="sxs-lookup"><span data-stu-id="2d614-121">ATP information</span></span>

<span data-ttu-id="2d614-122">Sales'te **Teklifler** , **Siparişler** ve **Faturalar** sayfalarındaki satır öğelerine yeni bir **ATP Bilgileri** düğmesi eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="2d614-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="2d614-123">Bu düğmeyi seçtiğinizde, bir iletişim kutusu görüntülenir ve şirketi, stok tesisini, stok ambarını ve sipariş miktarını burada belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2d614-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="2d614-124">Bu iletişim kutusu, [Sipariş taahhüdü](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) bölümünde açıklananlarla aynı ayarlara sahiptir.</span><span class="sxs-lookup"><span data-stu-id="2d614-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="2d614-125">İletişim kutusu, Supply Chain Management'taki ATP bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2d614-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="2d614-126">Bilgiler aşağıdaki miktarları içerir:</span><span class="sxs-lookup"><span data-stu-id="2d614-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="2d614-127">KM miktarı</span><span class="sxs-lookup"><span data-stu-id="2d614-127">ATP quantity</span></span>
- <span data-ttu-id="2d614-128">Giriş  miktarı</span><span class="sxs-lookup"><span data-stu-id="2d614-128">Receipt quantity</span></span>
- <span data-ttu-id="2d614-129">Çıkış miktarı</span><span class="sxs-lookup"><span data-stu-id="2d614-129">Issue quantity</span></span>
- <span data-ttu-id="2d614-130">Eldeki miktar</span><span class="sxs-lookup"><span data-stu-id="2d614-130">On-hand quantity</span></span>
