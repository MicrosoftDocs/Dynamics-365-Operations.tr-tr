--- 
title: "ISO20022 hesaptan ödemeleri için müşterileri ve müşteri banka hesaplarını ayarlama"
description: "Bu görev, ISO20022 hesaptan ödeme gibi müşteri ödeme dosyası oluşturmak için gereken bir müşteri banka hesabı ve bir müşteri hesaptan ödeme talimatı ayarlamada size yol gösterir."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 52970c54849e91c5052ad61ffc6458e646cbb262
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a><span data-ttu-id="aadf5-103">ISO20022 hesaptan ödemeleri için müşterileri ve müşteri banka hesaplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="aadf5-103">Set up customers and customer bank accounts for ISO20022 direct debits</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aadf5-104">Bu görev, ISO20022 hesaptan ödeme gibi müşteri ödeme dosyası oluşturmak için gereken bir müşteri banka hesabı ve bir müşteri hesaptan ödeme talimatı ayarlamada size yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="aadf5-104">This task walks you through setting up a customer bank account and a customer direct debit mandate which are required to generate the customer payment file like ISO20022 direct debit.</span></span> <span data-ttu-id="aadf5-105">Ayarlanan müşteri ödeme biçimlerine bağlı olarak bir müşteri veya müşteri banka hesabı için bu yordamda incelenmeyen ek bilgiler gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="aadf5-105">Depending on the customer payment formats tha are set up, additional information, not covered in this procedure, might be required for a customer or a customer bank account.</span></span> 

<span data-ttu-id="aadf5-106">Bu görev, tüzel kişilik birincil adresi Almanya'da olan demo veri şirketi DEMF'yi kullanarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="aadf5-106">This task was created using the demo data company DEMF with a legal entity primary address in Germany.</span></span>



<span data-ttu-id="aadf5-107">Bu, birlikte elektronik raporlama yapılandırmalarını kullanarak müşteri ödemesi işlemini gösteren beş yordamın dördüncüsüdür.</span><span class="sxs-lookup"><span data-stu-id="aadf5-107">This is the fourth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>


## <a name="set-up-a-customer-bank-account"></a><span data-ttu-id="aadf5-108">Bir müşteri banka hesabı ayarlayın</span><span class="sxs-lookup"><span data-stu-id="aadf5-108">Set up a customer bank account</span></span>
1. <span data-ttu-id="aadf5-109">Alacak hesapları > Müşteriler > Tüm müşteriler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-109">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="aadf5-110">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="aadf5-111">Örneğin, Hesap alanına "DE-010" değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-111">For example, filter on the Account field with a value of 'DE-010 '.</span></span>
3. <span data-ttu-id="aadf5-112">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="aadf5-113">Eylem Bölmesinde, Müşteri'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-113">On the Action Pane, click Customer.</span></span>
5. <span data-ttu-id="aadf5-114">Banka hesapları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="aadf5-115">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-115">Click New.</span></span>
7. <span data-ttu-id="aadf5-116">Banka hesabı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-116">In the Bank account field, type a value.</span></span>
8. <span data-ttu-id="aadf5-117">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-117">In the Name field, type a value.</span></span>
    * <span data-ttu-id="aadf5-118">Örneğin, "EUR bankası" girin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-118">For example, enter 'EUR bank'.</span></span>  
9. <span data-ttu-id="aadf5-119">Banka grupları alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-119">In the Bank groups field, enter or select a value.</span></span>
10. <span data-ttu-id="aadf5-120">IBAN alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-120">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="aadf5-121">Örneğin, "DE36200400000628808808" girin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-121">For example, enter 'DE36200400000628808808'.</span></span>  
11. <span data-ttu-id="aadf5-122">SWIFT kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-122">In the SWIFT code field, type a value.</span></span>
    * <span data-ttu-id="aadf5-123">Örneğin: "COBADEFFXXX" girin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-123">For example: Enter 'COBADEFFXXX'.</span></span>  <span data-ttu-id="aadf5-124">Birçok ödeme biçimi için SWIFT \ BIC zorunlu değildir ancak yine de bir banka hesabı için kayıtlı bulunması önerilir.</span><span class="sxs-lookup"><span data-stu-id="aadf5-124">Please note that SWIFT \ BIC is not mandatory for many payment formats however it is recommended to have it registered for a bank account.</span></span>  
12. <span data-ttu-id="aadf5-125">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-125">Click Save.</span></span>
13. <span data-ttu-id="aadf5-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-126">Close the page.</span></span>
14. <span data-ttu-id="aadf5-127">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-127">Click Edit.</span></span>
15. <span data-ttu-id="aadf5-128">Ödeme varsayılanları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-128">Expand the Payment defaults section.</span></span>
16. <span data-ttu-id="aadf5-129">Banka hesabı alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-129">In the Bank account field, enter or select a value.</span></span>

## <a name="add-a-direct-debit-mandate"></a><span data-ttu-id="aadf5-130">Hesaptan ödeme talimatı ekleyin</span><span class="sxs-lookup"><span data-stu-id="aadf5-130">Add a direct debit mandate</span></span>
1. <span data-ttu-id="aadf5-131">Hesaptan ödeme talimatları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-131">Expand the Direct debit mandates section.</span></span>
2. <span data-ttu-id="aadf5-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-132">Click Add.</span></span>
3. <span data-ttu-id="aadf5-133">Alacaklı banka hesabı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-133">In the Creditor bank account field, enter or select a value.</span></span>
    * <span data-ttu-id="aadf5-134">Örneğin, DEMF OPER'i seçin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-134">For example, select DEMF OPER.</span></span>  
4. <span data-ttu-id="aadf5-135">İmza tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-135">In the Signature date field, enter a date.</span></span>
5. <span data-ttu-id="aadf5-136">Tarih güncelleştirmesini onaylamak için Evet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-136">Click Yes to confirm the date update.</span></span>
6. <span data-ttu-id="aadf5-137">İmza konumu alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-137">In the Signature location field, enter or select a value.</span></span>
7. <span data-ttu-id="aadf5-138">Beklenen ödeme sayısı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="aadf5-138">In the Expected number of payments field, enter a number.</span></span>
8. <span data-ttu-id="aadf5-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-139">Click OK.</span></span>
9. <span data-ttu-id="aadf5-140">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="aadf5-140">Click Save.</span></span>


