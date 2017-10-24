--- 
title: "Elektronik raporlama (ER) için biçim yapılandırması kullanarak ödemelere ilişkin elektronik belgeler oluşturma"
description: "Aşağıdaki yordamlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının yeni bir Elektronik Raporlama (ER) biçim yapılandırmasını kullanarak, ödemeleri işlemek için elektronik belgeleri nasıl oluşturabileceğini açıklar."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a5d958d3b55bfa76f3cfbb3c1a289e4e89c49146
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="90c9c-103">Elektronik raporlama (ER) için biçim yapılandırması kullanarak ödemelere ilişkin elektronik belgeler oluşturma</span><span class="sxs-lookup"><span data-stu-id="90c9c-103">Generate electronic documents for payments using a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90c9c-104">Aşağıdaki yordamlar Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının yeni bir Elektronik Raporlama (ER) biçim yapılandırmasını kullanarak, ödemeleri işlemek için elektronik belgeleri nasıl oluşturabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="90c9c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="90c9c-105">Bu adımlar GBSI örnek şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="90c9c-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="90c9c-106">Bu adımları tamamlamak için, öncelikle "Ödeme belgesi biçimi ile bir yapılandırma oluşturun" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="90c9c-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="90c9c-107">Elektronik ödeme yönteminin yapılandırmasını değiştirin</span><span class="sxs-lookup"><span data-stu-id="90c9c-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="90c9c-108">Borç hesapları > Ödeme kurulumu > Ödeme yöntemleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="90c9c-109">Gerekirse, genişletmek için Dosya biçimi bölümünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="90c9c-110">Kayıtları bulmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="90c9c-111">Örneğin, Ödeme yöntemi alanına 'Elektronik' değeriyle filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="90c9c-112">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-112">Click Edit.</span></span>
5. <span data-ttu-id="90c9c-113">Genel elektronik raporlama alanını Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="90c9c-114">Ödeme dosyaları oluşturmak için genel elektronik raporlama deseni kullanmak için Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="90c9c-115">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="90c9c-116">BACS (UK hayali) yapılandırma biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="90c9c-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-117">Click Save.</span></span>
9. <span data-ttu-id="90c9c-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="90c9c-119">Oluşturulan ödeme dosyalarının biçimini sınayın</span><span class="sxs-lookup"><span data-stu-id="90c9c-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="90c9c-120">Borç hesapları > Ödemeler > Ödeme günlüğü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="90c9c-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-121">Click New.</span></span>
3. <span data-ttu-id="90c9c-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="90c9c-123">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="90c9c-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="90c9c-125">VendPay seçin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-125">Select VendPay.</span></span>  
6. <span data-ttu-id="90c9c-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-126">Click Save.</span></span>
7. <span data-ttu-id="90c9c-127">Satırlar seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-127">Click Lines.</span></span>
8. <span data-ttu-id="90c9c-128">Şirket alanına 'DEMF' yazın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="90c9c-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="90c9c-129">DEMF</span></span>  
9. <span data-ttu-id="90c9c-130">Hesap alanında, 'DE-01001' değerlerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="90c9c-131">DE-01001</span><span class="sxs-lookup"><span data-stu-id="90c9c-131">DE-01001</span></span>  
10. <span data-ttu-id="90c9c-132">Tanım alanına 'Ödeme' yazın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="90c9c-133">Ödeme</span><span class="sxs-lookup"><span data-stu-id="90c9c-133">Payment</span></span>  
11. <span data-ttu-id="90c9c-134">Borç alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="90c9c-135">1000</span><span class="sxs-lookup"><span data-stu-id="90c9c-135">1000</span></span>  
12. <span data-ttu-id="90c9c-136">Ödeme sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="90c9c-137">Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="90c9c-138">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="90c9c-139">Elektronik değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="90c9c-140">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="90c9c-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-141">Click Save.</span></span>
17. <span data-ttu-id="90c9c-142">Ödemeler oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-142">Click Generate payments.</span></span>
18. <span data-ttu-id="90c9c-143">Ödeme yöntemi alanında açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="90c9c-144">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="90c9c-145">Elektronik değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="90c9c-146">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="90c9c-147">Elektronik değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="90c9c-148">Dosya adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="90c9c-149">Örneğin 'ödemeler' yazın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="90c9c-150">Banka hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="90c9c-151">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="90c9c-152">GBSI OPER değerini seçin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="90c9c-153">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-153">Click OK.</span></span>
25. <span data-ttu-id="90c9c-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-154">Click OK.</span></span>
    * <span data-ttu-id="90c9c-155">XML biçiminde oluşturulan ödeme dosyasının çözümleyin.</span><span class="sxs-lookup"><span data-stu-id="90c9c-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="90c9c-156">Bunu, tasarlanmış belge düzeni ve tanımlanan ödeme işlem özniteliklerini ile karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="90c9c-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  


