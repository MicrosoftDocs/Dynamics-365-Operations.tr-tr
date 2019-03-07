---
title: Varyant ağırlıkları kullanarak satınalma siparişlerine çeşitli ürünler ekleme
description: Bu yordam, her ürün varyantı için satınalma siparişi satırlarını otomatik olarak doldurmak üzere varyant ağırlıklarının kullanılmasıyla ilgili açıklamalar içerir.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 446260a09bd5177877637ac8a288ad584dfa2b2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "345502"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="0a006-103">Varyant ağırlıkları kullanarak satınalma siparişlerine çeşitli ürünler ekleme</span><span class="sxs-lookup"><span data-stu-id="0a006-103">Add variant products to purchase orders using variant weights</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a006-104">Bu yordam, her ürün varyantı için satınalma siparişi satırlarını otomatik olarak doldurmak üzere varyant ağırlıklarının kullanılmasıyla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="0a006-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="0a006-105">Satın almak istediğiniz ürün miktarını seçtiğinizde, satınalma siparişi satırları ürün varyantlarında yapılandırılan ağırlıklar teme alınarak tüm ürün varyantları için önerilen miktarlarla oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0a006-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="0a006-106">Bu yordam, ürün boyutları ve ürün çeşitlerinde ağırlık değerleri yapılandırma adımlarını içermez.</span><span class="sxs-lookup"><span data-stu-id="0a006-106">This procedure doesn’t include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="0a006-107">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0a006-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="0a006-108">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="0a006-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="0a006-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a006-109">Click New.</span></span>
3. <span data-ttu-id="0a006-110">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="0a006-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0a006-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a006-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0a006-112">Genel bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="0a006-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="0a006-113">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a006-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0a006-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a006-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="0a006-115">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="0a006-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0a006-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="0a006-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="0a006-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a006-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="0a006-118">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="0a006-118">Click OK.</span></span>
12. <span data-ttu-id="0a006-119">Satır ayrıntıları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="0a006-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="0a006-120">Varyantlar sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a006-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="0a006-121">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a006-121">Click Add line.</span></span>
15. <span data-ttu-id="0a006-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="0a006-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="0a006-123">Madde numarası alanına '0140' yazın.</span><span class="sxs-lookup"><span data-stu-id="0a006-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="0a006-124">Miktarı '1000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0a006-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="0a006-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a006-125">Click Save.</span></span>

