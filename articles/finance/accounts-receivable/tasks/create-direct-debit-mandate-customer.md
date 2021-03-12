---
title: Müşteri için hesaptan ödeme talimatı oluşturma
description: Bu görev kılavuzunda hesaptan ödeme talimatının nasıl oluşturulacağı ve faturada nasıl kullanılacağı gösterilmektedir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f746da0bcf2b1e0cb09af6b5e2ea61938213c924
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991054"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="a4431-103">Müşteri için hesaptan ödeme talimatı oluşturma</span><span class="sxs-lookup"><span data-stu-id="a4431-103">Create a direct debit mandate for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4431-104">Bu görev kılavuzunda hesaptan ödeme talimatının nasıl oluşturulacağı ve faturada nasıl kullanılacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="a4431-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="a4431-105">Banka hesabı oluşturun</span><span class="sxs-lookup"><span data-stu-id="a4431-105">Create a bank account</span></span>
1. <span data-ttu-id="a4431-106">**Gezinti bölmesinde** **Modüller > Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a4431-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="a4431-107">Listeden bir kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-107">In the list, select a record.</span></span> <span data-ttu-id="a4431-108">Örneğin, TR-001 seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-108">For example, select US-001</span></span>
3. <span data-ttu-id="a4431-109">Eylem Bölmesinde **Müşteri**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="a4431-110">**Banka hesapları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="a4431-111">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-111">Click **New**.</span></span>
6. <span data-ttu-id="a4431-112">**Banka hesabı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="a4431-113">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a4431-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="a4431-114">**IBAN** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="a4431-115">**Para birimi** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a4431-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="a4431-116">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-116">Click **Save**.</span></span>
11. <span data-ttu-id="a4431-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-117">Close the page.</span></span>
12. <span data-ttu-id="a4431-118">**Gezinti bölmesinde** **Modüller > Nakit ve banka yönetimi > Banka hesapları > Banka hesapları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a4431-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="a4431-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a4431-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="a4431-121">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-121">Click **Edit**.</span></span>
16. <span data-ttu-id="a4431-122">**Ek kimlik** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a4431-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="a4431-123">**Otomatik ödeme kodu** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="a4431-124">**IBAN** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="a4431-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-125">Close the page.</span></span>
20. <span data-ttu-id="a4431-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="a4431-127">Elektronik ödeme yöntemini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="a4431-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="a4431-128">**Gezinti bölmesinde** **Modüller > Alacak hesapları > Ödeme ayarı > Ödeme yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a4431-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="a4431-129">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-129">Click **New**.</span></span>
3. <span data-ttu-id="a4431-130">**Ödeme yöntemi** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="a4431-131">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a4431-132">**Ödeme türü** alanına 'Elektronik ödeme' girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="a4431-133">Ödemenin hesaptan ödeme talimatı yönteminin ödeme türü Elektronik ödeme olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a4431-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="a4431-134">**Talimat iste** alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="a4431-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="a4431-136">Müşteriye bir hesaptan ödeme talimatı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="a4431-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="a4431-137">**Gezinti bölmesinde** **Modüller > Alacak hesapları > Müşteriler > Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="a4431-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="a4431-138">Listeden bir kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-138">In the list, select a record.</span></span> <span data-ttu-id="a4431-139">Örneğin, TR-001 seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-139">For example, select US-001</span></span>
3. <span data-ttu-id="a4431-140">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-140">Click **Edit**.</span></span>
4. <span data-ttu-id="a4431-141">**Ödeme varsayılanları** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a4431-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="a4431-142">**Ödeme yöntemi** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="a4431-143">**Ödeme varsayılanları** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a4431-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="a4431-144">**Hesaptan ödeme talimatları** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a4431-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="a4431-145">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-145">Click **Add**.</span></span>
9. <span data-ttu-id="a4431-146">**Banka hesabı** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="a4431-147">**Alacaklı banka hesabı** alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="a4431-148">**Ödeme sıklığı** alanına bu talimat için işleneceğini tahmin ettiğiniz ödeme sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="a4431-149">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-149">Click **OK**.</span></span>
13. <span data-ttu-id="a4431-150">**Yazdır**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-150">Click **Print**.</span></span>
14. <span data-ttu-id="a4431-151">**Talimat raporu**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="a4431-152">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-152">Close the page.</span></span>
16. <span data-ttu-id="a4431-153">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-153">Click **Edit**.</span></span>
17. <span data-ttu-id="a4431-154">**İmza tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="a4431-155">**Evet** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-155">Click **Yes**.</span></span>
19. <span data-ttu-id="a4431-156">Talimatın imzalandığı yeri girin.</span><span class="sxs-lookup"><span data-stu-id="a4431-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="a4431-157">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-157">Click **OK**.</span></span>
21. <span data-ttu-id="a4431-158">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a4431-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="a4431-159">Talimatlı bir serbest metin faturası oluşturun</span><span class="sxs-lookup"><span data-stu-id="a4431-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="a4431-160">**Gezinti bölmesinde** **Modüller > Alacak hesapları > Faturalar > Tüm serbest metin faturaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a4431-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="a4431-161">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a4431-161">Click **New**.</span></span>
3. <span data-ttu-id="a4431-162">Talimatı eklediğiniz müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="a4431-163">**Hesaptan ödeme talimatı kodu** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a4431-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>

