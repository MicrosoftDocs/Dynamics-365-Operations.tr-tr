---
title: "Sabit kıymet hareket seçenekleri"
description: "Bu makalede, sabit kıymet hareketleri oluşturmak için kullanılabilecek çeşitli yöntemler açıklanmaktadır."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9be300652e3de23554e1e61e32f1b0070e08099b
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---

# <a name="fixed-asset-transaction-options"></a><span data-ttu-id="95dd9-103">Sabit kıymet hareket seçenekleri</span><span class="sxs-lookup"><span data-stu-id="95dd9-103">Fixed asset transaction options</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95dd9-104">Bu makalede, sabit kıymet hareketleri oluşturmak için kullanılabilecek çeşitli yöntemler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="95dd9-104">This article describes the different methods available to create fixed asset transactions.</span></span>

<span data-ttu-id="95dd9-105">Sabit kıymetleri Borç hesapları, Alacak hesapları, Tedarik ve kaynak atama ve Genel muhasebeye bağlanacak şekilde ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95dd9-105">You can set up Fixed assets for integration with Accounts payable, Accounts receivable, Procurement and sourcing, and General ledger.</span></span> <span data-ttu-id="95dd9-106">Ayrıca, bu maddeleri dahili olarak kullanmak üzere Stok yönetimindeki maddeleri Sabit kıymetlere de aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95dd9-106">You can also transfer items in Inventory management to Fixed assets if you want to use those items internally.</span></span>

## <a name="accounts-payable"></a><span data-ttu-id="95dd9-107">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="95dd9-107">Accounts payable</span></span>
<span data-ttu-id="95dd9-108">Sabit kıymet hareketlerini günlük fişi sayfasına girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95dd9-108">You can enter Fixed assets transactions in the Journal voucher page.</span></span> <span data-ttu-id="95dd9-109">Bu sayfa, Fatura günlüğü sayfasından açılabilir.</span><span class="sxs-lookup"><span data-stu-id="95dd9-109">This page can be opened from the Invoice journal page.</span></span> <span data-ttu-id="95dd9-110">Günlük fişi sayfasını Fatura onay günlüğü sayfasından da açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95dd9-110">You can also open the Journal voucher page from the Invoice approval journal page.</span></span> <span data-ttu-id="95dd9-111">Mahsup hesabı türü alanında, Sabit kıymetleri seçin.</span><span class="sxs-lookup"><span data-stu-id="95dd9-111">In the Offset account type field, select Fixed assets.</span></span> <span data-ttu-id="95dd9-112">Sonra, Mahsup hesap alanında bir sabit kıymet numarası seçin.</span><span class="sxs-lookup"><span data-stu-id="95dd9-112">Then, in the Offset account field, select a fixed asset number.</span></span> <span data-ttu-id="95dd9-113">Sabit kıymetler sekmesinde, Hareket türü ve Değerler alanlarında değerleri girin.</span><span class="sxs-lookup"><span data-stu-id="95dd9-113">On the Fixed assets tab, enter values in the Transaction type and Book fields.</span></span>

## <a name="accounts-receivable"></a><span data-ttu-id="95dd9-114">Alacak hesapları</span><span class="sxs-lookup"><span data-stu-id="95dd9-114">Accounts receivable</span></span>
<span data-ttu-id="95dd9-115">Sabit kıymet hareketlerini Serbest metin faturası sayfasına girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95dd9-115">You can enter Fixed assets transactions in the Free text invoice page.</span></span>  <span data-ttu-id="95dd9-116">Serbest metin faturası sayfasında, fatura satırları kılavuzunda bir satır öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="95dd9-116">In the Free text invoice page, in the Invoice lines grid, select a line item.</span></span> <span data-ttu-id="95dd9-117">Satır ayrıntıları Hızlı Sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95dd9-117">Click the Line details FastTab.</span></span> <span data-ttu-id="95dd9-118">Elden çıkarma hareketi için sabit kıymet numarasını ve defteri girin.</span><span class="sxs-lookup"><span data-stu-id="95dd9-118">Enter the fixed asset number and book for the disposal transaction.</span></span> <span data-ttu-id="95dd9-119">Serbest metin faturaları için, sabit kıymet hareket türü her zaman Satış çıkışıdır.</span><span class="sxs-lookup"><span data-stu-id="95dd9-119">For free text invoices, the fixed asset transaction type is always Disposal - sale.</span></span>

## <a name="procurement-and-sourcing"></a><span data-ttu-id="95dd9-120">Tedarik ve kaynak atama</span><span class="sxs-lookup"><span data-stu-id="95dd9-120">Procurement and sourcing</span></span>
<span data-ttu-id="95dd9-121">Sabit kıymet hareketlerini Satınalma siparişi sayfasına girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95dd9-121">You can enter Fixed assets transactions in the Purchase order page.</span></span> <span data-ttu-id="95dd9-122">Bir satınalma siparişi oluşturmak için gereken bilgileri girin ve Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95dd9-122">Enter the required information to create a purchase order, and then click OK.</span></span> <span data-ttu-id="95dd9-123">Satınalma sipariş sayfasında, Satır ayrıntıları Hızlı Sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="95dd9-123">In the Purchase order page, click the Line details FastTab.</span></span> <span data-ttu-id="95dd9-124">Ardından, Sabit kıymetler sekmesinde, sabit kıymet hakkındaki bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="95dd9-124">Then, on the Fixed assets tab, enter information about the fixed asset.</span></span> 

<span data-ttu-id="95dd9-125">Mevcut bir sabit kıymet için alım hareketi nakletmek için sabit kıymet numarasını, defteri ve hareket türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="95dd9-125">To post an acquisition transaction for an existing fixed asset, specify the fixed asset number, book, and transaction type.</span></span> <span data-ttu-id="95dd9-126">Bu bilgiler eksik ise sabit kıymet deftere nakledilemez.</span><span class="sxs-lookup"><span data-stu-id="95dd9-126">The fixed asset cannot be posted if any of this information is missing.</span></span> <span data-ttu-id="95dd9-127">Yeni bir sabit kıymet için alım hareketi nakletmek için, Yeni sabit kıymet seçeneğini seçin ve ardından yeni kıymeti atamak için sabit kıymet grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="95dd9-127">To post an acquisition transaction for a new fixed asset, select the New fixed asset? option, and then select the fixed asset group to assign the new asset to.</span></span> <span data-ttu-id="95dd9-128">Ancak madde standart bir maliyet stok modeli kullanan bir stok modeli grubundaysa, bir satır için hiçbir sabit kıymet alanı mevcut değildir.</span><span class="sxs-lookup"><span data-stu-id="95dd9-128">However, no fixed asset fields are available for a line if the item is in an inventory model group that uses a standard cost inventory model.</span></span> <span data-ttu-id="95dd9-129">Ayrıca, Sabit kıymetler parametreleri sayfasında tanımlanan seçenekler satın alma modüllerinden alım hareketlerini nakledip nakledemeyeceğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="95dd9-129">Additionally, the options that are defined in the Fixed assets parameters page determine whether you can post acquisition transactions from the purchasing modules.</span></span> 

<span data-ttu-id="95dd9-130">Sabit kıymet alımı için bir satınalma siparişi veya Stoktan sabit kıymetlere günlüğü kullanıldığında, stok değeri etkilenir.</span><span class="sxs-lookup"><span data-stu-id="95dd9-130">When a purchase order or the Inventory to fixed assets journal is used to acquire fixed assets, the inventory value is affected.</span></span>

## <a name="general-ledger"></a><span data-ttu-id="95dd9-131">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="95dd9-131">General ledger</span></span>
<span data-ttu-id="95dd9-132">Tüm sabit kıymet hareket türleri Genel günlük sayfasına nakledilebilir.</span><span class="sxs-lookup"><span data-stu-id="95dd9-132">Any fixed asset transaction type can be posted in the General journal page.</span></span> <span data-ttu-id="95dd9-133">Ayrıca, sabit kıymet hareketlerini deftere nakletmek için Sabit kıymetlerdeki günlükleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95dd9-133">You can also use journals in Fixed assets to post fixed asset transactions.</span></span>

## <a name="options-for-entering-fixed-asset-transaction-types"></a><span data-ttu-id="95dd9-134">Sabit kıymet hareketleri tiplerini girme seçenekleri</span><span class="sxs-lookup"><span data-stu-id="95dd9-134">Options for entering fixed asset transaction types</span></span>


| <span data-ttu-id="95dd9-135">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="95dd9-135">Transaction type</span></span>                    | <span data-ttu-id="95dd9-136">Modül</span><span class="sxs-lookup"><span data-stu-id="95dd9-136">Module</span></span>                   | <span data-ttu-id="95dd9-137">Seçenekler</span><span class="sxs-lookup"><span data-stu-id="95dd9-137">Options</span></span>                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| <span data-ttu-id="95dd9-138">Alım, Alım düzeltmesi</span><span class="sxs-lookup"><span data-stu-id="95dd9-138">Acquisition, Acquisition adjustment</span></span> | <span data-ttu-id="95dd9-139">Sabit kıymetler</span><span class="sxs-lookup"><span data-stu-id="95dd9-139">Fixed assets</span></span>             | <span data-ttu-id="95dd9-140">Sabit kıymetler, Stoktan sabit kıymetlere</span><span class="sxs-lookup"><span data-stu-id="95dd9-140">Fixed assets, Inventory to fixed assets</span></span>   |
|                                     | <span data-ttu-id="95dd9-141">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="95dd9-141">General ledger</span></span>           | <span data-ttu-id="95dd9-142">Genel günlük</span><span class="sxs-lookup"><span data-stu-id="95dd9-142">General journal</span></span>                           |
|                                     | <span data-ttu-id="95dd9-143">Borç hesapları</span><span class="sxs-lookup"><span data-stu-id="95dd9-143">Accounts payable</span></span>         | <span data-ttu-id="95dd9-144">Fatura günlüğü, Fatura onay günlüğü</span><span class="sxs-lookup"><span data-stu-id="95dd9-144">Invoice journal, Invoice approval journal</span></span> |
|                                     | <span data-ttu-id="95dd9-145">Tedarik ve kaynak atama</span><span class="sxs-lookup"><span data-stu-id="95dd9-145">Procurement and sourcing</span></span> | <span data-ttu-id="95dd9-146">Satın alma siparişi</span><span class="sxs-lookup"><span data-stu-id="95dd9-146">Purchase order</span></span>                            |
| <span data-ttu-id="95dd9-147">Amortisman</span><span class="sxs-lookup"><span data-stu-id="95dd9-147">Depreciation</span></span>                        | <span data-ttu-id="95dd9-148">Sabit kıymetler</span><span class="sxs-lookup"><span data-stu-id="95dd9-148">Fixed assets</span></span>             | <span data-ttu-id="95dd9-149">Sabit kıymetler</span><span class="sxs-lookup"><span data-stu-id="95dd9-149">Fixed assets</span></span>                              |
|                                     | <span data-ttu-id="95dd9-150">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="95dd9-150">General ledger</span></span>           | <span data-ttu-id="95dd9-151">Yevmiye fişi</span><span class="sxs-lookup"><span data-stu-id="95dd9-151">General journal</span></span>                           |
| <span data-ttu-id="95dd9-152">Elden çıkarma</span><span class="sxs-lookup"><span data-stu-id="95dd9-152">Disposal</span></span>                            | <span data-ttu-id="95dd9-153">Sabit kıymetler</span><span class="sxs-lookup"><span data-stu-id="95dd9-153">Fixed assets</span></span>             | <span data-ttu-id="95dd9-154">Sabit kıymetler</span><span class="sxs-lookup"><span data-stu-id="95dd9-154">Fixed assets</span></span>                              |
| <span data-ttu-id="95dd9-155">** **</span><span class="sxs-lookup"><span data-stu-id="95dd9-155">** **</span></span>                               | <span data-ttu-id="95dd9-156">Genel muhasebe</span><span class="sxs-lookup"><span data-stu-id="95dd9-156">General ledger</span></span>           | <span data-ttu-id="95dd9-157">Yevmiye fişi</span><span class="sxs-lookup"><span data-stu-id="95dd9-157">General journal</span></span>                           |
| <span data-ttu-id="95dd9-158">** **</span><span class="sxs-lookup"><span data-stu-id="95dd9-158">** **</span></span>                               | <span data-ttu-id="95dd9-159">Alacak hesapları</span><span class="sxs-lookup"><span data-stu-id="95dd9-159">Accounts receivable</span></span>      | <span data-ttu-id="95dd9-160">Dekont / Serbest metin faturası</span><span class="sxs-lookup"><span data-stu-id="95dd9-160">Free text invoice</span></span>                         |



<span data-ttu-id="95dd9-161">Daha fazla bilgi için bkz: [Sabit kıymet tümleştirmesi](fixed-asset-integration.md).</span><span class="sxs-lookup"><span data-stu-id="95dd9-161">For more information, see [Fixed assets integration](fixed-asset-integration.md).</span></span>




