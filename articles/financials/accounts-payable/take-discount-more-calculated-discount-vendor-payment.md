---
title: Bir satıcı ödemesi için hesaplanan iskontodan daha fazla iskonto alma
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
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84b3d6ef1a86d8174823345a5ee9181c701c151
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843277"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="a792f-104">Bir satıcı ödemesi için hesaplanan iskontodan daha fazla iskonto alma</span><span class="sxs-lookup"><span data-stu-id="a792f-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a792f-105">Bu makalede, bir tutar için faturada olan indirimden daha fazla nakit indirimi alınan bir senaryo verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a792f-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="a792f-106">Bu senaryo, bir kuruluşun satıcı ile faturadakinden daha az bir miktarı ödeme konusunda anlaşmaya varması durumunda gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="a792f-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="a792f-107">Satıcı 3051, bir faturanın yedi gün içinde ödenmesi durumunda Fabrikam'a yüzde 4 oranında bir nakit iskontosu veriyor.</span><span class="sxs-lookup"><span data-stu-id="a792f-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="a792f-108">29 Haziran tarihinde April, 1.000,00 tutarında bir fatura giriyor.</span><span class="sxs-lookup"><span data-stu-id="a792f-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="a792f-109">Satıcı, April'in fatura için kullanılabilecek, 40,00 tutarındaki varsayılan iskonto yerine 60.00 tutarında bir iskonto almasına izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="a792f-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="a792f-110">April, Borç hesapları ödeme günlüğünü kullanarak bir tek seferlik ödeme kaydediyor.</span><span class="sxs-lookup"><span data-stu-id="a792f-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="a792f-111">Ödeme için satıcı giriyor ve **Hareketleri kapat** sayfasını açıyor.</span><span class="sxs-lookup"><span data-stu-id="a792f-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="a792f-112">April, faturayı işaretliyor ve **Nakit iskontosu tutarı** alanındaki değeri **60,00** olarak değiştiriyor.</span><span class="sxs-lookup"><span data-stu-id="a792f-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="a792f-113">İşaret</span><span class="sxs-lookup"><span data-stu-id="a792f-113">Mark</span></span>     | <span data-ttu-id="a792f-114">Nakit iskontosu kullan</span><span class="sxs-lookup"><span data-stu-id="a792f-114">Use cash discount</span></span> | <span data-ttu-id="a792f-115">Fiş</span><span class="sxs-lookup"><span data-stu-id="a792f-115">Voucher</span></span>   | <span data-ttu-id="a792f-116">Hesap</span><span class="sxs-lookup"><span data-stu-id="a792f-116">Account</span></span> | <span data-ttu-id="a792f-117">Tarih</span><span class="sxs-lookup"><span data-stu-id="a792f-117">Date</span></span>      | <span data-ttu-id="a792f-118">Vade tarihi</span><span class="sxs-lookup"><span data-stu-id="a792f-118">Due date</span></span>  | <span data-ttu-id="a792f-119">Fatura</span><span class="sxs-lookup"><span data-stu-id="a792f-119">Invoice</span></span> | <span data-ttu-id="a792f-120">Hareket para birimi cinsinden tutar</span><span class="sxs-lookup"><span data-stu-id="a792f-120">Amount in transaction currency</span></span> | <span data-ttu-id="a792f-121">Para Birimi</span><span class="sxs-lookup"><span data-stu-id="a792f-121">Currency</span></span> | <span data-ttu-id="a792f-122">Kapatılacak tutar</span><span class="sxs-lookup"><span data-stu-id="a792f-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="a792f-123">Seçildi</span><span class="sxs-lookup"><span data-stu-id="a792f-123">Selected</span></span> | <span data-ttu-id="a792f-124">Normal</span><span class="sxs-lookup"><span data-stu-id="a792f-124">Normal</span></span>            | <span data-ttu-id="a792f-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="a792f-125">Inv-10040</span></span> | <span data-ttu-id="a792f-126">3051</span><span class="sxs-lookup"><span data-stu-id="a792f-126">3051</span></span>    | <span data-ttu-id="a792f-127">29/6/2015</span><span class="sxs-lookup"><span data-stu-id="a792f-127">6/29/2015</span></span> | <span data-ttu-id="a792f-128">29/7/2015</span><span class="sxs-lookup"><span data-stu-id="a792f-128">7/29/2015</span></span> | <span data-ttu-id="a792f-129">10040</span><span class="sxs-lookup"><span data-stu-id="a792f-129">10040</span></span>   | <span data-ttu-id="a792f-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="a792f-130">1,000.00</span></span>                       | <span data-ttu-id="a792f-131">ABD Doları</span><span class="sxs-lookup"><span data-stu-id="a792f-131">USD</span></span>      | <span data-ttu-id="a792f-132">940,00</span><span class="sxs-lookup"><span data-stu-id="a792f-132">940.00</span></span>           |

<span data-ttu-id="a792f-133">İskonto bilgileri **Hareketleri kapat** sayfasının altında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="a792f-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="a792f-134">Nakit iskontosu tarihi</span><span class="sxs-lookup"><span data-stu-id="a792f-134">Cash discount date</span></span>           | <span data-ttu-id="a792f-135">12/7/2015</span><span class="sxs-lookup"><span data-stu-id="a792f-135">7/12/2015</span></span> |
| <span data-ttu-id="a792f-136">Nakit iskontosu tutarı</span><span class="sxs-lookup"><span data-stu-id="a792f-136">Cash discount amount</span></span>         | <span data-ttu-id="a792f-137">60,00</span><span class="sxs-lookup"><span data-stu-id="a792f-137">60.00</span></span>     |
| <span data-ttu-id="a792f-138">Nakit iskontosu kullan</span><span class="sxs-lookup"><span data-stu-id="a792f-138">Use cash discount</span></span>            | <span data-ttu-id="a792f-139">Normal</span><span class="sxs-lookup"><span data-stu-id="a792f-139">Normal</span></span>    |
| <span data-ttu-id="a792f-140">Alınan nakit iskontosu</span><span class="sxs-lookup"><span data-stu-id="a792f-140">Cash discount taken</span></span>          | <span data-ttu-id="a792f-141">0,00</span><span class="sxs-lookup"><span data-stu-id="a792f-141">0.00</span></span>      |
| <span data-ttu-id="a792f-142">Alınacak nakit iskontosu tutarı</span><span class="sxs-lookup"><span data-stu-id="a792f-142">Cash discount amount to take</span></span> | <span data-ttu-id="a792f-143">60,00</span><span class="sxs-lookup"><span data-stu-id="a792f-143">60.00</span></span>     |

<span data-ttu-id="a792f-144">April sonra ödeme günlüğünü naklediyor.</span><span class="sxs-lookup"><span data-stu-id="a792f-144">April posts the payment journal.</span></span> <span data-ttu-id="a792f-145">Fatura, 940,00 tutarında bir ödeme ve 60,00 tutarında bir iskonto kullanılarak tamamen kapatılıyor.</span><span class="sxs-lookup"><span data-stu-id="a792f-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



