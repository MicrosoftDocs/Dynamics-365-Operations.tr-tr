---
title: Bir satıcı ödemesi için hesaplanan iskontodan daha fazlasını alma
description: Bu makalede, bir tutar için faturada olan indirimden daha fazla nakit indirimi alınan bir senaryo verilmektedir. Bu senaryo, bir kuruluşun satıcı ile faturadakinden daha az bir miktarı ödeme konusunda anlaşmaya varması durumunda gerçekleşebilir.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f2088ff04a0ef5ffe6ffe47b85f47e6957264d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810258"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="93d3c-104">Bir satıcı ödemesi için hesaplanan iskontodan daha fazlasını alma</span><span class="sxs-lookup"><span data-stu-id="93d3c-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93d3c-105">Bu makalede, bir tutar için faturada olan indirimden daha fazla nakit indirimi alınan bir senaryo verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="93d3c-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="93d3c-106">Bu senaryo, bir kuruluşun satıcı ile faturadakinden daha az bir miktarı ödeme konusunda anlaşmaya varması durumunda gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="93d3c-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="93d3c-107">Satıcı 3051, bir faturanın yedi gün içinde ödenmesi durumunda Fabrikam'a yüzde 4 oranında bir nakit iskontosu veriyor.</span><span class="sxs-lookup"><span data-stu-id="93d3c-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="93d3c-108">29 Haziran tarihinde April, 1.000,00 tutarında bir fatura giriyor.</span><span class="sxs-lookup"><span data-stu-id="93d3c-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="93d3c-109">Satıcı, April'in fatura için kullanılabilecek, 40,00 tutarındaki varsayılan iskonto yerine 60.00 tutarında bir iskonto almasına izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="93d3c-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="93d3c-110">April, Borç hesapları ödeme günlüğünü kullanarak bir tek seferlik ödeme kaydediyor.</span><span class="sxs-lookup"><span data-stu-id="93d3c-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="93d3c-111">Ödeme için satıcı giriyor ve **Hareketleri kapat** sayfasını açıyor.</span><span class="sxs-lookup"><span data-stu-id="93d3c-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="93d3c-112">April, faturayı işaretliyor ve **Nakit iskontosu tutarı** alanındaki değeri **60,00** olarak değiştiriyor.</span><span class="sxs-lookup"><span data-stu-id="93d3c-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="93d3c-113">İşaret</span><span class="sxs-lookup"><span data-stu-id="93d3c-113">Mark</span></span>     | <span data-ttu-id="93d3c-114">Nakit iskontosu kullan</span><span class="sxs-lookup"><span data-stu-id="93d3c-114">Use cash discount</span></span> | <span data-ttu-id="93d3c-115">Fiş</span><span class="sxs-lookup"><span data-stu-id="93d3c-115">Voucher</span></span>   | <span data-ttu-id="93d3c-116">Hesap</span><span class="sxs-lookup"><span data-stu-id="93d3c-116">Account</span></span> | <span data-ttu-id="93d3c-117">Tarih</span><span class="sxs-lookup"><span data-stu-id="93d3c-117">Date</span></span>      | <span data-ttu-id="93d3c-118">Vade tarihi</span><span class="sxs-lookup"><span data-stu-id="93d3c-118">Due date</span></span>  | <span data-ttu-id="93d3c-119">Fatura</span><span class="sxs-lookup"><span data-stu-id="93d3c-119">Invoice</span></span> | <span data-ttu-id="93d3c-120">Hareket para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="93d3c-120">Amount in transaction currency</span></span> | <span data-ttu-id="93d3c-121">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="93d3c-121">Currency</span></span> | <span data-ttu-id="93d3c-122">Kapatılacak tutar</span><span class="sxs-lookup"><span data-stu-id="93d3c-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="93d3c-123">Seçildi</span><span class="sxs-lookup"><span data-stu-id="93d3c-123">Selected</span></span> | <span data-ttu-id="93d3c-124">Normal</span><span class="sxs-lookup"><span data-stu-id="93d3c-124">Normal</span></span>            | <span data-ttu-id="93d3c-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="93d3c-125">Inv-10040</span></span> | <span data-ttu-id="93d3c-126">3051</span><span class="sxs-lookup"><span data-stu-id="93d3c-126">3051</span></span>    | <span data-ttu-id="93d3c-127">29/6/2015</span><span class="sxs-lookup"><span data-stu-id="93d3c-127">6/29/2015</span></span> | <span data-ttu-id="93d3c-128">29/7/2015</span><span class="sxs-lookup"><span data-stu-id="93d3c-128">7/29/2015</span></span> | <span data-ttu-id="93d3c-129">10040</span><span class="sxs-lookup"><span data-stu-id="93d3c-129">10040</span></span>   | <span data-ttu-id="93d3c-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="93d3c-130">1,000.00</span></span>                       | <span data-ttu-id="93d3c-131">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="93d3c-131">USD</span></span>      | <span data-ttu-id="93d3c-132">940,00</span><span class="sxs-lookup"><span data-stu-id="93d3c-132">940.00</span></span>           |

<span data-ttu-id="93d3c-133">İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="93d3c-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

| <span data-ttu-id="93d3c-134">Alan</span><span class="sxs-lookup"><span data-stu-id="93d3c-134">Field</span></span>                        | <span data-ttu-id="93d3c-135">Değer</span><span class="sxs-lookup"><span data-stu-id="93d3c-135">Value</span></span>     |
|------------------------------|-----------|
| <span data-ttu-id="93d3c-136">Nakit iskonto tarihi</span><span class="sxs-lookup"><span data-stu-id="93d3c-136">Cash discount date</span></span>           | <span data-ttu-id="93d3c-137">12/7/2015</span><span class="sxs-lookup"><span data-stu-id="93d3c-137">7/12/2015</span></span> |
| <span data-ttu-id="93d3c-138">Nakit iskontosu tutarı</span><span class="sxs-lookup"><span data-stu-id="93d3c-138">Cash discount amount</span></span>         | <span data-ttu-id="93d3c-139">60.00</span><span class="sxs-lookup"><span data-stu-id="93d3c-139">60.00</span></span>     |
| <span data-ttu-id="93d3c-140">Nakit iskontosu kullan</span><span class="sxs-lookup"><span data-stu-id="93d3c-140">Use cash discount</span></span>            | <span data-ttu-id="93d3c-141">Normal</span><span class="sxs-lookup"><span data-stu-id="93d3c-141">Normal</span></span>    |
| <span data-ttu-id="93d3c-142">Alınan nakit iskontosu</span><span class="sxs-lookup"><span data-stu-id="93d3c-142">Cash discount taken</span></span>          | <span data-ttu-id="93d3c-143">0,00</span><span class="sxs-lookup"><span data-stu-id="93d3c-143">0.00</span></span>      |
| <span data-ttu-id="93d3c-144">Alınacak nakit iskontosu tutarı</span><span class="sxs-lookup"><span data-stu-id="93d3c-144">Cash discount amount to take</span></span> | <span data-ttu-id="93d3c-145">60,00</span><span class="sxs-lookup"><span data-stu-id="93d3c-145">60.00</span></span>     |

<span data-ttu-id="93d3c-146">April sonra ödeme günlüğünü naklediyor.</span><span class="sxs-lookup"><span data-stu-id="93d3c-146">April posts the payment journal.</span></span> <span data-ttu-id="93d3c-147">Fatura, 940,00 tutarında bir ödeme ve 60,00 tutarında bir iskonto kullanılarak tamamen kapatılıyor.</span><span class="sxs-lookup"><span data-stu-id="93d3c-147">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]