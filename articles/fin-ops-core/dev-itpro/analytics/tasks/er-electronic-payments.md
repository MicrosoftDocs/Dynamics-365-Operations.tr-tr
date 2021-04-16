---
title: ER Biçim yapılandırmayı kullanarak ödemeler için elektronik belgeler oluşturma
description: Bu konuda, ödemeleri işlemek üzere elektronik belgeler oluşturmak için yeni bir Elektronik raporlama (ER) biçimi yapılandırmasının nasıl kullanılacağı açıklanmaktadır.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f62d7cd690406647886f9d6d1cb1491b691d4159
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752496"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="17973-103">ER Biçim yapılandırmayı kullanarak ödemeler için elektronik belgeler oluşturma</span><span class="sxs-lookup"><span data-stu-id="17973-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17973-104">Aşağıdaki yordamlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının yeni bir Elektronik Raporlama (ER) biçim yapılandırmasını kullanarak, ödemeleri işlemek için elektronik belgeleri nasıl oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="17973-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="17973-105">Bu adımlar GBSI örnek şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="17973-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="17973-106">Bu adımları tamamlamak için, öncelikle "Ödeme belgesi biçimi ile bir yapılandırma oluşturun" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="17973-106">To complete these steps, you must first complete the steps in the "Create a configuration with format of payment document" procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="17973-107">Elektronik ödeme yönteminin yapılandırmasını değiştirin</span><span class="sxs-lookup"><span data-stu-id="17973-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="17973-108">Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="17973-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="17973-109">Gerekirse, genişletmek için Dosya biçimi bölümünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="17973-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="17973-110">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="17973-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="17973-111">Örneğin, Ödeme yöntemi alanına 'Elektronik' değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="17973-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="17973-112">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-112">Click Edit.</span></span>
5. <span data-ttu-id="17973-113">Genel elektronik raporlama alanını Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="17973-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="17973-114">Ödeme dosyaları oluşturmak için genel elektronik raporlama deseni kullanmak için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="17973-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="17973-115">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="17973-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="17973-116">BACS (UK hayali) yapılandırma biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="17973-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="17973-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-117">Click Save.</span></span>
9. <span data-ttu-id="17973-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="17973-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="17973-119">Oluşturulan ödeme dosyalarının biçimini sınayın</span><span class="sxs-lookup"><span data-stu-id="17973-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="17973-120">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="17973-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="17973-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-121">Click New.</span></span>
3. <span data-ttu-id="17973-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="17973-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="17973-123">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="17973-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="17973-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="17973-125">VendPay seçin.</span><span class="sxs-lookup"><span data-stu-id="17973-125">Select VendPay.</span></span>  
6. <span data-ttu-id="17973-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-126">Click Save.</span></span>
7. <span data-ttu-id="17973-127">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-127">Click Lines.</span></span>
8. <span data-ttu-id="17973-128">Şirket alanına 'DEMF' yazın.</span><span class="sxs-lookup"><span data-stu-id="17973-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="17973-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="17973-129">DEMF</span></span>  
9. <span data-ttu-id="17973-130">Hesap alanında, 'DE-01001' değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="17973-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="17973-131">DE-01001</span><span class="sxs-lookup"><span data-stu-id="17973-131">DE-01001</span></span>  
10. <span data-ttu-id="17973-132">Tanım alanına 'Ödeme' yazın.</span><span class="sxs-lookup"><span data-stu-id="17973-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="17973-133">Ödeme</span><span class="sxs-lookup"><span data-stu-id="17973-133">Payment</span></span>  
11. <span data-ttu-id="17973-134">Borç alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="17973-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="17973-135">1000</span><span class="sxs-lookup"><span data-stu-id="17973-135">1000</span></span>  
12. <span data-ttu-id="17973-136">Ödeme sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="17973-137">Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="17973-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="17973-138">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="17973-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="17973-139">Elektronik değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="17973-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="17973-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="17973-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-141">Click Save.</span></span>
17. <span data-ttu-id="17973-142">Ödemeler oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="17973-142">Click Generate payments.</span></span>
18. <span data-ttu-id="17973-143">Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="17973-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="17973-144">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="17973-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="17973-145">Elektronik değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="17973-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="17973-146">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="17973-147">Elektronik değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="17973-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="17973-148">Dosya adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="17973-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="17973-149">Örneğin 'ödemeler' yazın.</span><span class="sxs-lookup"><span data-stu-id="17973-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="17973-150">Banka hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="17973-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="17973-151">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="17973-152">GBSI OPER değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="17973-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="17973-153">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-153">Click OK.</span></span>
25. <span data-ttu-id="17973-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17973-154">Click OK.</span></span>
    * <span data-ttu-id="17973-155">XML biçiminde oluşturulan ödeme dosyasının çözümleyin.</span><span class="sxs-lookup"><span data-stu-id="17973-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="17973-156">Bunu, tasarlanmış belge düzeni ve tanımlanan ödeme işlem özniteliklerini ile karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="17973-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]