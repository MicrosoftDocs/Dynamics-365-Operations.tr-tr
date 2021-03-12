---
title: Bir satıcı ödemesi için hesaplanan iskontodan daha fazlasını alma
description: Bu makalede, bir tutar için faturada olan indirimden daha fazla nakit indirimi alınan bir senaryo verilmektedir. Bu senaryo, bir kuruluşun satıcı ile faturadakinden daha az bir miktarı ödeme konusunda anlaşmaya varması durumunda gerçekleşebilir.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: c7ee74bad071d546724f6ffe336bbe3bdf47e2a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971915"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="b500e-104">Bir satıcı ödemesi için hesaplanan iskontodan daha fazlasını alma</span><span class="sxs-lookup"><span data-stu-id="b500e-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b500e-105">Bu makalede, bir tutar için faturada olan indirimden daha fazla nakit indirimi alınan bir senaryo verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="b500e-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="b500e-106">Bu senaryo, bir kuruluşun satıcı ile faturadakinden daha az bir miktarı ödeme konusunda anlaşmaya varması durumunda gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="b500e-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="b500e-107">Satıcı 3051, bir faturanın yedi gün içinde ödenmesi durumunda Fabrikam'a yüzde 4 oranında bir nakit iskontosu veriyor.</span><span class="sxs-lookup"><span data-stu-id="b500e-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="b500e-108">29 Haziran tarihinde April, 1.000,00 tutarında bir fatura giriyor.</span><span class="sxs-lookup"><span data-stu-id="b500e-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="b500e-109">Satıcı, April'in fatura için kullanılabilecek, 40,00 tutarındaki varsayılan iskonto yerine 60.00 tutarında bir iskonto almasına izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="b500e-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="b500e-110">April, Borç hesapları ödeme günlüğünü kullanarak bir tek seferlik ödeme kaydediyor.</span><span class="sxs-lookup"><span data-stu-id="b500e-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="b500e-111">Ödeme için satıcı giriyor ve **Hareketleri kapat** sayfasını açıyor.</span><span class="sxs-lookup"><span data-stu-id="b500e-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="b500e-112">April, faturayı işaretliyor ve **Nakit iskontosu tutarı** alanındaki değeri **60,00** olarak değiştiriyor.</span><span class="sxs-lookup"><span data-stu-id="b500e-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="b500e-113">İşaret</span><span class="sxs-lookup"><span data-stu-id="b500e-113">Mark</span></span>     | <span data-ttu-id="b500e-114">Nakit iskontosu kullan</span><span class="sxs-lookup"><span data-stu-id="b500e-114">Use cash discount</span></span> | <span data-ttu-id="b500e-115">Fiş</span><span class="sxs-lookup"><span data-stu-id="b500e-115">Voucher</span></span>   | <span data-ttu-id="b500e-116">Hesap</span><span class="sxs-lookup"><span data-stu-id="b500e-116">Account</span></span> | <span data-ttu-id="b500e-117">Tarih</span><span class="sxs-lookup"><span data-stu-id="b500e-117">Date</span></span>      | <span data-ttu-id="b500e-118">Vade tarihi</span><span class="sxs-lookup"><span data-stu-id="b500e-118">Due date</span></span>  | <span data-ttu-id="b500e-119">Fatura</span><span class="sxs-lookup"><span data-stu-id="b500e-119">Invoice</span></span> | <span data-ttu-id="b500e-120">Hareket para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="b500e-120">Amount in transaction currency</span></span> | <span data-ttu-id="b500e-121">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="b500e-121">Currency</span></span> | <span data-ttu-id="b500e-122">Kapatılacak tutar</span><span class="sxs-lookup"><span data-stu-id="b500e-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="b500e-123">Seçildi</span><span class="sxs-lookup"><span data-stu-id="b500e-123">Selected</span></span> | <span data-ttu-id="b500e-124">Normal</span><span class="sxs-lookup"><span data-stu-id="b500e-124">Normal</span></span>            | <span data-ttu-id="b500e-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="b500e-125">Inv-10040</span></span> | <span data-ttu-id="b500e-126">3051</span><span class="sxs-lookup"><span data-stu-id="b500e-126">3051</span></span>    | <span data-ttu-id="b500e-127">29/6/2015</span><span class="sxs-lookup"><span data-stu-id="b500e-127">6/29/2015</span></span> | <span data-ttu-id="b500e-128">29/7/2015</span><span class="sxs-lookup"><span data-stu-id="b500e-128">7/29/2015</span></span> | <span data-ttu-id="b500e-129">10040</span><span class="sxs-lookup"><span data-stu-id="b500e-129">10040</span></span>   | <span data-ttu-id="b500e-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="b500e-130">1,000.00</span></span>                       | <span data-ttu-id="b500e-131">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="b500e-131">USD</span></span>      | <span data-ttu-id="b500e-132">940,00</span><span class="sxs-lookup"><span data-stu-id="b500e-132">940.00</span></span>           |

<span data-ttu-id="b500e-133">İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="b500e-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="b500e-134">Nakit iskontosu tarihi</span><span class="sxs-lookup"><span data-stu-id="b500e-134">Cash discount date</span></span>           | <span data-ttu-id="b500e-135">12/7/2015</span><span class="sxs-lookup"><span data-stu-id="b500e-135">7/12/2015</span></span> |
| <span data-ttu-id="b500e-136">Nakit iskontosu tutarı</span><span class="sxs-lookup"><span data-stu-id="b500e-136">Cash discount amount</span></span>         | <span data-ttu-id="b500e-137">60,00</span><span class="sxs-lookup"><span data-stu-id="b500e-137">60.00</span></span>     |
| <span data-ttu-id="b500e-138">Nakit iskontosu kullan</span><span class="sxs-lookup"><span data-stu-id="b500e-138">Use cash discount</span></span>            | <span data-ttu-id="b500e-139">Normal</span><span class="sxs-lookup"><span data-stu-id="b500e-139">Normal</span></span>    |
| <span data-ttu-id="b500e-140">Alınan nakit iskontosu</span><span class="sxs-lookup"><span data-stu-id="b500e-140">Cash discount taken</span></span>          | <span data-ttu-id="b500e-141">0,00</span><span class="sxs-lookup"><span data-stu-id="b500e-141">0.00</span></span>      |
| <span data-ttu-id="b500e-142">Alınacak nakit iskontosu tutarı</span><span class="sxs-lookup"><span data-stu-id="b500e-142">Cash discount amount to take</span></span> | <span data-ttu-id="b500e-143">60,00</span><span class="sxs-lookup"><span data-stu-id="b500e-143">60.00</span></span>     |

<span data-ttu-id="b500e-144">April sonra ödeme günlüğünü naklediyor.</span><span class="sxs-lookup"><span data-stu-id="b500e-144">April posts the payment journal.</span></span> <span data-ttu-id="b500e-145">Fatura, 940,00 tutarında bir ödeme ve 60,00 tutarında bir iskonto kullanılarak tamamen kapatılıyor.</span><span class="sxs-lookup"><span data-stu-id="b500e-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



