---
title: ISO20022 hesaptan ödemeleri için müşterileri ve müşteri banka hesaplarını ayarlama
description: Bu görev, ISO20022 hesaptan ödeme gibi müşteri ödeme dosyası oluşturmak için gereken bir müşteri banka hesabı ve bir müşteri hesaptan ödeme talimatı ayarlamada size yol gösterir.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78523e6f221973194560466e006639f4bb53614b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819518"
---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="361a6-103">ISO20022 hesaptan ödemeleri için müşterileri ve müşteri banka hesaplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="361a6-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="361a6-104">Bu görev, ISO20022 hesaptan ödeme gibi müşteri ödeme dosyası oluşturmak için gereken bir müşteri banka hesabı ve bir müşteri hesaptan ödeme talimatı ayarlamada size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="361a6-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="361a6-105">Ayarlanan müşteri ödeme biçimlerine bağlı olarak bir müşteri veya müşteri banka hesabı için bu yordamda incelenmeyen ek bilgiler gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="361a6-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="361a6-106">Bu görev, tüzel kişilik birincil adresi Almanya'da olan demo veri şirketi DEMF'yi kullanarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="361a6-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="361a6-107">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın dördüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="361a6-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="361a6-108">Bir müşteri banka hesabı ayarlayın</span><span class="sxs-lookup"><span data-stu-id="361a6-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="361a6-109">Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="361a6-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="361a6-110">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="361a6-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="361a6-111">Örneğin, Hesap alanına "DE-010" değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="361a6-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="361a6-113">Eylem Bölmesinde, Müşteri'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="361a6-114">Banka hesapları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="361a6-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-115">Click New.</span></span>
7. <span data-ttu-id="361a6-116">Banka hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="361a6-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="361a6-117">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="361a6-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="361a6-118">Örneğin, "EUR bankası" girin.</span><span class="sxs-lookup"><span data-stu-id="361a6-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="361a6-119">Banka grupları alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="361a6-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="361a6-120">IBAN alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="361a6-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="361a6-121">Örneğin, "DE36200400000628808808" girin.</span><span class="sxs-lookup"><span data-stu-id="361a6-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="361a6-122">SWIFT kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="361a6-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="361a6-123">Örneğin: "COBADEFFXXX" girin.</span><span class="sxs-lookup"><span data-stu-id="361a6-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="361a6-124">Birçok ödeme biçimi için SWIFT \ BIC zorunlu değildir ancak yine de bir banka hesabı için kayıtlı bulunması önerilir.</span><span class="sxs-lookup"><span data-stu-id="361a6-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="361a6-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-125">Click Save.</span></span>
13. <span data-ttu-id="361a6-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="361a6-126">Close the page.</span></span>
14. <span data-ttu-id="361a6-127">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-127">Click Edit.</span></span>
15. <span data-ttu-id="361a6-128">Ödeme varsayılanları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="361a6-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="361a6-129">Banka hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="361a6-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="361a6-130">Hesaptan ödeme talimatı ekleyin</span><span class="sxs-lookup"><span data-stu-id="361a6-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="361a6-131">Hesaptan ödeme talimatları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="361a6-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="361a6-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="361a6-132">Click Add.</span></span>
3. <span data-ttu-id="361a6-133">Alacaklı banka hesabı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="361a6-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="361a6-134">Örneğin, DEMF OPER'i seçin.</span><span class="sxs-lookup"><span data-stu-id="361a6-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="361a6-135">İmza tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="361a6-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="361a6-136">Tarih güncelleştirmesini onaylamak için Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="361a6-137">İmza konumu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="361a6-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="361a6-138">Beklenen ödeme sayısı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="361a6-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="361a6-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-139">Click OK.</span></span>
9. <span data-ttu-id="361a6-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="361a6-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]