---
title: Hesaptan ödeme talimatları olan bir müşteri için ödemeler oluşturma
description: Bu yordam, hesaptan ödeme yapılandırması ve ödenecek bir faturası olan müşteriler için bir ISO20022 hesaptan ödeme dosyasının nasıl oluşturulacağını gösterir.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 129c5291a29994f91ef325aa9b9a3b54a0e958d6
ms.sourcegitcommit: 807dec193cd163c9f5d949e744cfde40f2eb24b4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/01/2019
ms.locfileid: "2468967"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="e0387-103">Hesaptan ödeme talimatları olan bir müşteri için ödemeler oluşturma</span><span class="sxs-lookup"><span data-stu-id="e0387-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0387-104">Bu yordam, hesaptan ödeme yapılandırması ve ödenecek bir faturası olan müşteriler için bir ISO20022 hesaptan ödeme dosyasının nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0387-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="e0387-105">Bir faturayı oluşturmak ve deftere nakletmek isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e0387-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="e0387-106">Ödenecek fatura yerine müşteri ön ödeme senaryosunu desteklemek için bir ödeme dosyası oluşturmadan önce günlükte bir talimat seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0387-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="e0387-107">Bu yordamı oluşturmak için kullanılan demo veri şirketi DEMF'dir.</span><span class="sxs-lookup"><span data-stu-id="e0387-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="e0387-108">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın beşincisidir.</span><span class="sxs-lookup"><span data-stu-id="e0387-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="e0387-109">Bu görevi tamamlamadan önce önceki görevleri tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e0387-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="e0387-110">Öncelikle müşteri ödeme elektronik raporlama yapılandırmalarını içe aktarmanız, ödeme yöntemini yapılandırmanız ve şirket ve müşteri bilgilerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e0387-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="e0387-111">Hesaptan ödeme talimatı bilgileri olan bir serbest metin faturasını deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="e0387-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="e0387-112">Alacak hesapları > Faturalar > Tüm serbest metin faturaları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e0387-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="e0387-113">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-113">Click New.</span></span>
3. <span data-ttu-id="e0387-114">Müşteri hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e0387-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="e0387-115">Örneğin, DE-010 öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e0387-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="e0387-116">Ödeme yöntemi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e0387-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="e0387-117">Örneğin,</span><span class="sxs-lookup"><span data-stu-id="e0387-117">For example.</span></span> <span data-ttu-id="e0387-118">Elektronik'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e0387-118">select Electronic.</span></span>  
5. <span data-ttu-id="e0387-119">Hesaptan ödeme talimatı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e0387-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="e0387-120">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-120">Click Add line.</span></span>
7. <span data-ttu-id="e0387-121">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e0387-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="e0387-122">Ana hesap alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0387-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="e0387-123">Birim fiyatı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e0387-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="e0387-124">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-124">Click Post.</span></span>
11. <span data-ttu-id="e0387-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="e0387-126">Ödeme oluşturma</span><span class="sxs-lookup"><span data-stu-id="e0387-126">Create a payment</span></span>
1. <span data-ttu-id="e0387-127">Alacak hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e0387-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="e0387-128">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-128">Click New.</span></span>
3. <span data-ttu-id="e0387-129">Ad alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e0387-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="e0387-130">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-130">Click Lines.</span></span>
5. <span data-ttu-id="e0387-131">Ödeme teklifi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="e0387-132">Ödeme teklifi oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="e0387-133">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e0387-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="e0387-134">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-134">Click Filter.</span></span>
9. <span data-ttu-id="e0387-135">Listede, Müşteri hareketleri tablosu ve Ödeme yöntemi alanı için bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="e0387-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="e0387-136">Ödenecek müşteri hareketlerini seçmek için herhangi bir ölçütü uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e0387-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="e0387-137">Bu örnekte, filtre hareketleri için ödeme yöntemi olarak Elektronik'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="e0387-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="e0387-138">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e0387-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="e0387-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-139">Click OK.</span></span>
12. <span data-ttu-id="e0387-140">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-140">Click OK.</span></span>
13. <span data-ttu-id="e0387-141">Ödemeleri oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e0387-141">Click Create payments.</span></span>
