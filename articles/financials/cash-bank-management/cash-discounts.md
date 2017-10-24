---
title: "Nakit iskontoları"
description: "Nakit iskontoları Borç hesapları ve Alacak hesapları için ayarlanır ve paylaşılır.  Yapılabilecek nakit iskontosu müşteri faturasında veya satıcı faturasında tanımlanabilir ve fatura, nakit iskontosu tarihi geçmeden ödendiği takdirde alınır."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 668e3ebdd2729efb48e2833fd5beec3cefdb17b0
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="cash-discounts"></a><span data-ttu-id="c6eb8-104">Nakit iskontoları</span><span class="sxs-lookup"><span data-stu-id="c6eb8-104">Cash discounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c6eb8-105">Nakit iskontoları Borç hesapları ve Alacak hesapları için ayarlanır ve paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="c6eb8-106">Yapılabilecek nakit iskontosu müşteri faturasında veya satıcı faturasında tanımlanabilir ve fatura, nakit iskontosu tarihi geçmeden ödendiği takdirde alınır.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

<a name="cash-discounts"></a><span data-ttu-id="c6eb8-107">Nakit iskontoları</span><span class="sxs-lookup"><span data-stu-id="c6eb8-107">Cash discounts</span></span>
--------------

<span data-ttu-id="c6eb8-108">Hem müşteriler veya hem de satıcılar için nakit iskontoları, Nakit iskontoları sayfasında oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="c6eb8-109">Ayrıca, önceki nakit iskontosunun vadesi dolduğunda birbirini izleyecek nakit iskontolarını, Sonraki iskonto kodu alanını kullanarak tanımlayabilirsiniz,</span><span class="sxs-lookup"><span data-stu-id="c6eb8-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="c6eb8-110">Daha fazla bilgi için bu konunun devamındaki "Örnek: Nakit iskontoları serileri" başlığına bakınız.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="c6eb8-111">Eğer bir fatura, iade hareketi (ödeme veya alacak dekontu) veya her ikisi, tüzel kişiliğin hesap para birimini farklı bir para biriminde girilirse, nakit iskontosu, ödeme veya alacak dekontunun döviz kuru kullanılarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="c6eb8-112">Fatura ve iade belgesi farklı tüzel kişiliklere girildiye ve tüzel kişiliklerin muhasebe para birimleri farklıysa, döviz kuru faturanın bir tüzel kişiliğinden kredi belgesine göre alınır.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="c6eb8-113">Daha fazla bilgi için bu konunun devamındaki "Örnek: Nakit için döviz kurları" başlığına bakınız.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>
<span data-ttu-id="c6eb8-114">Nakit iskontosu ana hesabı varsayılan ilkesi</span><span class="sxs-lookup"><span data-stu-id="c6eb8-114">Defaulting order of cash discount main account</span></span>
----------------------------------------------

<span data-ttu-id="c6eb8-115">Bir fatura nakit iskontosu elde etmek için zamanında kapatılmışsa, nakit iskontosu aşağıdaki varsayılan ilkesi önceliğine göre otomatik olarak bir nakit iskontosu ana hesabına nakledilir:</span><span class="sxs-lookup"><span data-stu-id="c6eb8-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="c6eb8-116">Ana hesap, Açık hareketleri kapat sayfası veya Satıcı açık hareketleri kapat sayfasındaki Alternatif nakit iskontosu hesabı alanda belirtilir.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="c6eb8-117">Ana hesap, Faturaya atanan satış vergisi kodunun Genel muhasebe deftere nakletme grubunun, Müşteri nakit iskontosu alanı veya Satıcı satış iskontosu alanında belirtilir.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="c6eb8-118">Genel muhasebe deftere nakil gruplarını, genel muhasebe deftere nakil grupları sayfasında ayarlayın ve onları satış vergisi koduna satış vergisi kodları sayfasından atayın.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="c6eb8-119">Kapatılmış faturadaki nakit iskontosu kodu için, Müşteri iskontoları için ana hesap alanı veya Satıcı iskontoları için ana hesap alan Nakit iskontosu sayfasındadır.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="c6eb8-120">Nakit iskontoları için ana hesap, Otomatik hareketler için hesaplar sayfasında tanımlandığı gibi.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="c6eb8-121"> Örnek: Nakit iskontoları dizisi</span><span class="sxs-lookup"><span data-stu-id="c6eb8-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="c6eb8-122">Aşağıdaki gibi üç nakit iskontosu kodu ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="c6eb8-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="c6eb8-123">Kod 5D10% – Tutar 5 gün içinde ödendiğinde %10 oranında bir nakit iskontosu.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="c6eb8-124">Kod 10D5% – Tutar 10 gün içinde ödendiğinde %5 oranında bir nakit iskontosu.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="c6eb8-125">Kod 14D2% - Tutar 14 gün içinde ödendiğinde %2 oranında bir nakit iskontosu.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="c6eb8-126">Bir sonraki iskonto kodu alanına:</span><span class="sxs-lookup"><span data-stu-id="c6eb8-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="c6eb8-127">5G%1 kodu için 10G%5 seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="c6eb8-128">10G%5 kodu için 14G%2 seçimini yapın.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="c6eb8-129">14D2% kodu için Sonraki iskonto kodu alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="c6eb8-130">Fatura üzerindeki ödeme tarihi, bir önceki nakit indirimi tarihini geçtikçe, üç nakit indirimi bir birini izler.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="c6eb8-131">Fatura ödendiğinde nakit iskontosu sırasınndaki hangi nakit iskonto tarihi uyduğuna bağlı olarak, yalnızca bir nakit iskontosu verilir.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="c6eb8-132"> Örnek: Nakit iskontoları için döviz kurları</span><span class="sxs-lookup"><span data-stu-id="c6eb8-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="c6eb8-133">Tüzel kişiliğinizin muhasebe para birimi EUR'dur ve aşağıdaki döviz kurları USD için belirtilmiştir:</span><span class="sxs-lookup"><span data-stu-id="c6eb8-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="c6eb8-134">1 Şubat = 110</span><span class="sxs-lookup"><span data-stu-id="c6eb8-134">February 1 = 110</span></span>
-   <span data-ttu-id="c6eb8-135">1 Mart = 80</span><span class="sxs-lookup"><span data-stu-id="c6eb8-135">March 1 = 80</span></span>

<span data-ttu-id="c6eb8-136">20D2% nakit iskonto koşullarına sahip 1000 USD'lik bir fatura 15 Şubat'ta nakledilir.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="c6eb8-137">Faturanın muhasebe para birimi tutarı 1100 EUR'dur.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="c6eb8-138">980 USD için bir ödeme, fatura ile 1 Mart'ta kapatılır.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="c6eb8-139">Nakit iskontosu tutarı 20 USD'dir.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="c6eb8-140">Ödemenin muhasebe para birimi tutarı 784 Euro'dur.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="c6eb8-141">Nakit iskontosu hesap para miktarı, 1 Mart itibariyle döviz kuru kullanılarak hesaplanır: 20 \* 80 / 100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>
| <span data-ttu-id="c6eb8-142">**Not**</span><span class="sxs-lookup"><span data-stu-id="c6eb8-142">**Note**</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6eb8-143">Alacak hesapları parametreleri ya da hesapların borç parametreleri sayfaları hesapla nakit iskontoları için kısmi ödeme seçeneği seçili olduğunda her bir kısmi ödeme tarihinde geçerli olan döviz kuru kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c6eb8-143">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> |

 
=

 




