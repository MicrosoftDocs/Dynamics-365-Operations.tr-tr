---
title: Varyant ağırlıkları kullanarak satınalma siparişlerine çeşitli ürünler ekleme
description: Bu yordam, her ürün varyantı için satınalma siparişi satırlarını otomatik olarak doldurmak üzere varyant ağırlıklarının kullanılmasıyla ilgili açıklamalar içerir.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c099daf888cb2a1740dda3e860b37f88089c5ca
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986467"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="dec70-103">Varyant ağırlıkları kullanarak satınalma siparişlerine çeşitli ürünler ekleme</span><span class="sxs-lookup"><span data-stu-id="dec70-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dec70-104">Bu yordam, her ürün varyantı için satınalma siparişi satırlarını otomatik olarak doldurmak üzere varyant ağırlıklarının kullanılmasıyla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="dec70-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="dec70-105">Satın almak istediğiniz ürün miktarını seçtiğinizde, satınalma siparişi satırları ürün varyantlarında yapılandırılan ağırlıklar teme alınarak tüm ürün varyantları için önerilen miktarlarla oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="dec70-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="dec70-106">Bu yordam, ürün boyutları ve ürün çeşitlerinde ağırlık değerleri yapılandırma adımlarını içermez.</span><span class="sxs-lookup"><span data-stu-id="dec70-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="dec70-107">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="dec70-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="dec70-108">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="dec70-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="dec70-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dec70-109">Click New.</span></span>
3. <span data-ttu-id="dec70-110">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="dec70-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dec70-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dec70-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="dec70-112">Genel bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="dec70-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="dec70-113">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dec70-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="dec70-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dec70-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="dec70-115">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="dec70-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="dec70-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dec70-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="dec70-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dec70-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="dec70-118">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dec70-118">Click OK.</span></span>
12. <span data-ttu-id="dec70-119">Satır ayrıntıları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="dec70-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="dec70-120">Varyantlar sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dec70-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="dec70-121">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dec70-121">Click Add line.</span></span>
15. <span data-ttu-id="dec70-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dec70-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="dec70-123">Madde numarası alanına '0140' yazın.</span><span class="sxs-lookup"><span data-stu-id="dec70-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="dec70-124">Miktarı '1000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dec70-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="dec70-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dec70-125">Click Save.</span></span>

