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
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0cb0a99b926e1e129c5f7a174cac18e3b93aafa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967017"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="e39f8-103">Varyant ağırlıkları kullanarak satınalma siparişlerine çeşitli ürünler ekleme</span><span class="sxs-lookup"><span data-stu-id="e39f8-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e39f8-104">Bu yordam, her ürün varyantı için satınalma siparişi satırlarını otomatik olarak doldurmak üzere varyant ağırlıklarının kullanılmasıyla ilgili açıklamalar içerir.</span><span class="sxs-lookup"><span data-stu-id="e39f8-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="e39f8-105">Satın almak istediğiniz ürün miktarını seçtiğinizde, satınalma siparişi satırları ürün varyantlarında yapılandırılan ağırlıklar teme alınarak tüm ürün varyantları için önerilen miktarlarla oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e39f8-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="e39f8-106">Bu yordam, ürün boyutları ve ürün çeşitlerinde ağırlık değerleri yapılandırma adımlarını içermez.</span><span class="sxs-lookup"><span data-stu-id="e39f8-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="e39f8-107">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="e39f8-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e39f8-108">Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="e39f8-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="e39f8-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-109">Click New.</span></span>
3. <span data-ttu-id="e39f8-110">Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e39f8-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e39f8-112">Genel bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="e39f8-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="e39f8-113">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e39f8-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e39f8-115">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e39f8-116">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="e39f8-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e39f8-117">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="e39f8-118">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-118">Click OK.</span></span>
12. <span data-ttu-id="e39f8-119">Satır ayrıntıları bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="e39f8-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="e39f8-120">Varyantlar sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="e39f8-121">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-121">Click Add line.</span></span>
15. <span data-ttu-id="e39f8-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e39f8-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="e39f8-123">Madde numarası alanına '0140' yazın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="e39f8-124">Miktarı '1000' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="e39f8-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e39f8-125">Click Save.</span></span>

