---
title: "Tahakkuklara genel bakış"
description: "Bu makalede tahakkuklar açıklanmakta, tahakkukları nasıl ayarlayacağınız ve hareketleri nasıl oluşturacağınız hakkında bilgiler verilmektedir."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b3f989b1e442c35b5bed3c34c9cc6e31de5c4c9e
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="accruals-overview"></a><span data-ttu-id="ff9ee-103">Tahakkuklara genel bakış</span><span class="sxs-lookup"><span data-stu-id="ff9ee-103">Accruals overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff9ee-104">Bu makalede tahakkuklar açıklanmakta, tahakkukları nasıl ayarlayacağınız ve hareketleri nasıl oluşturacağınız hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="ff9ee-105">Tahakkuklar, tahakkuk muhasebesinde ödeme alındığında değil de kazanılan dönemde elde edilen geliri takip etmek ve ödeme yapıldığında değil de meydana geldiğinde anda giderleri (maliyetleri) takip etmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="ff9ee-106">Tahakkuk planları</span><span class="sxs-lookup"><span data-stu-id="ff9ee-106">Accrual schemes</span></span>
<span data-ttu-id="ff9ee-107">Tahakkuk planları, ertelenmiş gelir ve maliyetleri oluşturmak için kullanılır ve aynı tahakkuk planı hem gelir hem maliyetler için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="ff9ee-108">Genel muhasebe tahakkukları, bir günlük satırının maliyetleri ve gelirlerini uygun dönemlerde tanınacak şekilde yeniden dağıtır.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="ff9ee-109">**Tahakkuk planı** sayfasında, tahakkuk planı uygulandığında kullanılacak borç ve alacak hesaplarını belirtirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="ff9ee-110">**Borç** – Tanımladığınız ana hesap, günlük fişinde borç ana hesabının yerini alacaktır.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="ff9ee-111">Bu hesap ayrıca genel muhasebe tahakkuk hareketlerine dayalı olarak ertelemenin ters çevrilmesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="ff9ee-112">**Alacak** – tanımladığınız ana hesap, günlük fişinde alacak ana hesabının yerini alacaktır.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="ff9ee-113">Bu hesap ayrıca genel muhasebe tahakkuk hareketlerine dayalı olarak ertelemenin ters çevrilmesi için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="ff9ee-114">Hangi hesapların kullanılacağını belirledikten sonra tahakkuk hareketleri oluşturulduğunda fiş numarasının nasıl oluşturulacağını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="ff9ee-115">Hareketlerin ne sıklıkla gerçekleştirileceğini, hareketlerin gerçekleşme sayısını ve hareketlerin ne zaman nakledileceğini de belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="ff9ee-116">Tahakkuk planı oluşturduktan sonra Genel muhasebe tahakkukları işlevini kullanarak bu planı bazı günlüklerde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="ff9ee-117">Genel muhasebe tahakkukları</span><span class="sxs-lookup"><span data-stu-id="ff9ee-117">Ledger accruals</span></span>
<span data-ttu-id="ff9ee-118">Bir günlük girdiğinizde **İşlevler** menüsündeki **Genel muhasebe tahakkukları** öğesini tıklayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="ff9ee-119">Ardından, tahakkuk planını seçtiğinizde, günlükteki taban tutarını tahakkuk planında belirlendiği şekilde döneme dağılmış şekilde görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="ff9ee-120">Örneğin, bir çalışanın tüm yıla ait sigortasını Ocak ayındaki ödüyorsanız ve tutar 12.000 ise, bu gideri her ay kabul etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="ff9ee-121">Başlangıç tarihini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-121">You can select the start date.</span></span> <span data-ttu-id="ff9ee-122">Tahakkuk eden tutarın hesaba mı, yoksa mahsup hesaba mı dayalı olacağını da belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="ff9ee-123">Bu seçimleri yaptıktan sonra tahakkuk düzenine dayanarak oluşturulan tüm hareketleri görmek için **Hareketler**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="ff9ee-124">Örneğin, 12.000 tutarındaki sigorta masraflarını yıla yayarsanız, her ay 1.000 görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="ff9ee-125">Günlüğü deftere naklettikten sonra, **Fiş hareketleri** sorgulama sayfasını kullanarak hareketleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="ff9ee-126">Bir tahakkuk düzeni uygulanamıyorsa (örneğin, bir satış siparişi faturası veya satınalma emri faturası söz konusuysa), önceden ödenmiş tutarı alacaklandırabilir ve gider tutarını borçlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="ff9ee-127">Tahakkuk planını uygularken **Mahsup** seçimini yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff9ee-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="ff9ee-128">Daha fazla bilgi için bkz. [Tahakkuk planları oluşturma](tasks/create-accrual-schemes.md) ve [Genel muhasebe tahakkuk hareketleri oluşturma](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="ff9ee-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>

