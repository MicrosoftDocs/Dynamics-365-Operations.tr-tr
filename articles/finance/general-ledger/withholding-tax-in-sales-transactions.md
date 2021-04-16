---
title: Satış hareketlerinde stopaj vergisi
description: Bu konuda, seçili müşteriler için stopaj vergisinin hesaplanmasından kaçınma adımları listelenir. Size ödemelerinde stopaj vergisi belirten müşteriler için varsayılan stopaj vergisi grubunu atayabilirsiniz.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842356"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="b3ca4-104">Satış hareketlerinde stopaj vergisi</span><span class="sxs-lookup"><span data-stu-id="b3ca4-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="b3ca4-105">Bu konuda, seçili müşteriler için stopaj vergisinin hesaplanmasından kaçınma adımları listelenir.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="b3ca4-106">Size ödemelerinde stopaj vergisi belirten müşteriler için **Müşteriler** sayfasında varsayılan **Stopaj vergisi grubu**'nu atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="b3ca4-107">**Gezinti bölmesi > Modüller > Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="b3ca4-108">İlgili müşteri hesabına tıklayın, **Düzenle**'yi tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="b3ca4-109">**Fatura ve teslimat** sekmesinde, **Stopaj vergisini hesapla** alanını **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="b3ca4-110">Master verilerde bu müşteri için **Stopaj vergisini hesapla** açık değilse stopaj vergisi hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="b3ca4-111">Stopaj vergisi grubundan bir **Stopaj vergisi grubu** seçin.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="b3ca4-112">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-112">Click **Save**.</span></span>

<span data-ttu-id="b3ca4-113">Stopaj vergisine tabi kelamler/hizmetler için **Serbest Bırakılan Ürünler**'de varsayılan **Kalem stopaj vergisi grubu**'nu atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="b3ca4-114">**Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="b3ca4-115">İlgili Madde numarasına tıklayın, **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="b3ca4-116">**Satış** sekmesinde **Stopaj vergisini hesapla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="b3ca4-117">**Serbest Bırakılan Ürün** sayfasındaki **Satış** sekmesindeki bu madde için **Stopaj Vergisini Hesapla** **Evet** olarak ayarlanmazsa stopaj vergisi hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="b3ca4-118">**Madde stopaj vergisi grubu** listesinden bir madde stopaj vergisi grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="b3ca4-119">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-119">Click **Save**.</span></span>

<span data-ttu-id="b3ca4-120">Stopaj vergisi grupları ve madde stopaj vergisi grupları **Satış siparişi** sayfası kullanılarak atanabilir.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="b3ca4-121">Yeni bir satış siparişi oluşturduğunuzda, varsayılan Stopaj vergisi grubu ve Madde stopaj vergisi grubu satış siparişi satırlarında varsayılan girişler olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="b3ca4-122">Stopaj vergisi hesaplanır ve **Müşteri ödeme günlüğü**'ne nakledilir.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="b3ca4-123">İlgili stopaj vergisi kodunu ve gerçek stopaj vergisi tutarını, **Hareketleri kapat** sayfasındaki **Stopaj vergisi** sekmesinde el ile ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="b3ca4-124">Hesaplanan stopaj vergisi tutarı müşteri ödemesinden düşülür ve ilgili bir fişteki **Stopaj vergisi mahsubu** hesabına nakledilir.</span><span class="sxs-lookup"><span data-stu-id="b3ca4-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]