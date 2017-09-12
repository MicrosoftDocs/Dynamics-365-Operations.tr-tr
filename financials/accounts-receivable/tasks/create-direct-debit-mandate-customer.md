--- 
title: "Müşteri için hesaptan ödeme talimatı oluşturma"
description: "Bu görev kılavuzunda hesaptan ödeme talimatının nasıl oluşturulacağı ve faturada nasıl kullanılacağı gösterilmektedir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d01c7c19925a3c7064ab3f845b92b610b162066c
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="84c43-103">Müşteri için hesaptan ödeme talimatı oluşturma</span><span class="sxs-lookup"><span data-stu-id="84c43-103">Create a direct debit mandate for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84c43-104">Bu görev kılavuzunda hesaptan ödeme talimatının nasıl oluşturulacağı ve faturada nasıl kullanılacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="84c43-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="84c43-105">Banka hesabı oluşturun</span><span class="sxs-lookup"><span data-stu-id="84c43-105">Create a bank account</span></span>
1. <span data-ttu-id="84c43-106">Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="84c43-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="84c43-107">Örneğin, TR-001 seçin.</span><span class="sxs-lookup"><span data-stu-id="84c43-107">For example, select US-001</span></span>
3. <span data-ttu-id="84c43-108">Eylem Bölmesinde, Müşteri'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="84c43-109">Banka hesapları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="84c43-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-110">Click New.</span></span>
6. <span data-ttu-id="84c43-111">Banka hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="84c43-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="84c43-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="84c43-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="84c43-113">IBAN alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="84c43-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="84c43-114">Para birimi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="84c43-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="84c43-115">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-115">Click Save.</span></span>
11. <span data-ttu-id="84c43-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84c43-116">Close the page.</span></span>
12. <span data-ttu-id="84c43-117">Nakit ve banka yönetimi > Banka hesapları > Banka hesapları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="84c43-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="84c43-118">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="84c43-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="84c43-119">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="84c43-120">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-120">Click Edit.</span></span>
16. <span data-ttu-id="84c43-121">Ek kimlik bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="84c43-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="84c43-122">Otomatik ödeme kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="84c43-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="84c43-123">IBAN alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="84c43-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="84c43-124">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84c43-124">Close the page.</span></span>
20. <span data-ttu-id="84c43-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84c43-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="84c43-126">Elektronik ödeme yöntemini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="84c43-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="84c43-127">Alacak hesapları > Ödeme kurulumu > Ödeme yöntemi'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="84c43-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="84c43-128">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-128">Click New.</span></span>
3. <span data-ttu-id="84c43-129">Ödeme yöntemi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="84c43-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="84c43-130">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="84c43-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="84c43-131">Ödemenin hesaptan ödeme talimatı yönteminin ödeme türü Elektronik ödeme olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="84c43-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="84c43-132">Talimat iste alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="84c43-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="84c43-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84c43-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="84c43-134">Müşteriye bir hesaptan ödeme talimatı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="84c43-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="84c43-135">Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="84c43-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="84c43-136">Örneğin, TR-001 seçin.</span><span class="sxs-lookup"><span data-stu-id="84c43-136">For example, select US-001</span></span>
3. <span data-ttu-id="84c43-137">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-137">Click Edit.</span></span>
4. <span data-ttu-id="84c43-138">Ödeme varsayılanları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="84c43-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="84c43-139">Ödeme yöntemi alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="84c43-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="84c43-140">Ödeme varsayılanları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="84c43-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="84c43-141">Hesaptan ödeme talimatları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="84c43-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="84c43-142">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84c43-142">Click Add.</span></span>
9. <span data-ttu-id="84c43-143">Banka hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="84c43-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="84c43-144">Alacaklı banka hesabı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="84c43-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="84c43-145">Bu talimat için işleneceğini tahmin ettiğiniz ödeme sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="84c43-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="84c43-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-146">Click OK.</span></span>
13. <span data-ttu-id="84c43-147">Yazdır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84c43-147">Click Print.</span></span>
14. <span data-ttu-id="84c43-148">Talimat raporu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-148">Click Mandate report.</span></span>
15. <span data-ttu-id="84c43-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84c43-149">Close the page.</span></span>
16. <span data-ttu-id="84c43-150">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-150">Click Edit.</span></span>
17. <span data-ttu-id="84c43-151">İmza tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="84c43-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="84c43-152">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="84c43-152">Click Yes.</span></span>
19. <span data-ttu-id="84c43-153">Talimatın imzalandığı yeri girin.</span><span class="sxs-lookup"><span data-stu-id="84c43-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="84c43-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-154">Click OK.</span></span>
21. <span data-ttu-id="84c43-155">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="84c43-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="84c43-156">Talimatlı bir serbest metin faturası oluşturun</span><span class="sxs-lookup"><span data-stu-id="84c43-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="84c43-157">Alacak hesapları > Faturalar > Tüm serbest metin faturaları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="84c43-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="84c43-158">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="84c43-158">Click New.</span></span>
3. <span data-ttu-id="84c43-159">Talimatı eklediğiniz müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="84c43-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="84c43-160">Hesaptan ödeme talimatı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="84c43-160">In the Direct debit mandate ID field, enter or select a value.</span></span>


