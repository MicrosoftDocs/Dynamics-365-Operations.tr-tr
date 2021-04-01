---
title: Satın alma hareketlerinde stopaj vergisi
description: Stopaj vergisi yükümlülüğü olan satıcılar için **Tüm satıcılar** sayfasında varsayılan **Stopaj vergisi grubunu** atayabilirsiniz.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 06c18e6b0779539a6da7ae7afbe000c4cfc78d9e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256679"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="1578c-103">Satın alma hareketlerinde stopaj vergisi</span><span class="sxs-lookup"><span data-stu-id="1578c-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="1578c-104">Stopaj vergisi yükümlülüğü olan satıcılar için **Tüm satıcılar** sayfasında varsayılan **Stopaj vergisi grubunu** atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1578c-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="1578c-105">**Gezinti bölmesi > Modüller > Borç hesapları > Satıcılar > Tüm satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="1578c-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="1578c-106">İlgili Satıcı hesabına tıklayın, **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1578c-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="1578c-107">**Fatura ve teslimat** sekmesinde, **Stopaj vergisini hesapla** alanını **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1578c-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="1578c-108">Verilerde bu satıcı için **Stopaj vergisini hesapla** açık değilse stopaj vergisi hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="1578c-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="1578c-109">Stopaj vergisi grubundan bir **Stopaj vergisi grubu** seçin.</span><span class="sxs-lookup"><span data-stu-id="1578c-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="1578c-110">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1578c-110">Click **Save**.</span></span>

<span data-ttu-id="1578c-111">Stopaj vergisine tabi kelamler/hizmetler için **Serbest Bırakılan Ürünler**'de varsayılan **Kalem stopaj vergisi grubu**'nu atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1578c-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="1578c-112">**Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1578c-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="1578c-113">İlgili Madde numarasına tıklayın, **Düzenle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1578c-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="1578c-114">**Satın alma** sekmesinde **Stopaj vergisini hesapla**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1578c-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="1578c-115">**Serbest Bırakılan Ürün** sayfasındaki **Satın Alma** sekmesindeki bu madde için **Stopaj Vergisini Hesapla** **Evet** olarak ayarlanmazsa stopaj vergisi hesaplanmaz.</span><span class="sxs-lookup"><span data-stu-id="1578c-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="1578c-116">**Madde stopaj vergisi grubu** listesinden bir madde stopaj vergisi grubu seçin.</span><span class="sxs-lookup"><span data-stu-id="1578c-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="1578c-117">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1578c-117">Click **Save**.</span></span>

<span data-ttu-id="1578c-118">Stopaj vergisi grupları ve Madde stopaj vergisi grupları şu sayfalarda atanabilir:</span><span class="sxs-lookup"><span data-stu-id="1578c-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="1578c-119">**Satın alma siparişi**</span><span class="sxs-lookup"><span data-stu-id="1578c-119">**Purchase order**</span></span>
- <span data-ttu-id="1578c-120">**Satıcı faturası**</span><span class="sxs-lookup"><span data-stu-id="1578c-120">**Vendor invoice**</span></span>
- <span data-ttu-id="1578c-121">**Fatura günlüğü**</span><span class="sxs-lookup"><span data-stu-id="1578c-121">**Invoice journal**</span></span>

<span data-ttu-id="1578c-122">**Satın alma siparişleri** ve/veya **Bekleyen Satıcı faturaları** oluşturulurken, varsayılan Stopaj vergisi grubu ve Madde stopaj vergisi grubu satırlara aktarılır.</span><span class="sxs-lookup"><span data-stu-id="1578c-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="1578c-123">**Satıcı fatura günlüğü** için, **Stopaj vergisini hesapla**'yı açabilir ve günlükteki **Genel** sekmesinde **Madde stopaj vergisi grubu**'nu seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1578c-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="1578c-124">Geçici stopaj vergisi tutarı, **Satın alma siparişi** sayfasındaki **Toplamlar** sekmesinin **Ayarlanmış stopaj vergisi** alanında bulunur.</span><span class="sxs-lookup"><span data-stu-id="1578c-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Stopaj vergisi satın alma siparişine dahildir](media/withholding-tax-adjusted.png)

<span data-ttu-id="1578c-126">Stopaj vergisi, **Satıcı ödeme günlüğünde** hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="1578c-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="1578c-127">İlgili stopaj vergisi kodlarını ve gerçek stopaj vergisi tutarlarını, **Hareketleri kapat** sayfasındaki **Stopaj vergisi** sekmesinde el ile ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1578c-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Stopaj, Hareketleri kapat sayfasında el ile ayarlanabilir](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="1578c-129">Türetilen stopaj vergisi tutarı satıcı ödemesinden düşülür ve ilgili bir fişteki **Stopaj vergisi hesabına** nakledilir.</span><span class="sxs-lookup"><span data-stu-id="1578c-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![İlgili fişi gösteren stopaj vergisi hesabı](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]