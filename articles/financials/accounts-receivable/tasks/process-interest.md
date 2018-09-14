--- 
title: "Faiz işleme"
description: "Bu prosedürde, vade farkı dekontlarının nasıl oluşturulacağı, yazdırılacağı ve deftere nakledileceği gösterilmektedir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: c5652a38684061914f895d7f8b82999c9840fd63
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="process-interest"></a><span data-ttu-id="258c4-103">Faiz işleme</span><span class="sxs-lookup"><span data-stu-id="258c4-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="258c4-104">Bu prosedürde, vade farkı dekontlarının nasıl oluşturulacağı, yazdırılacağı ve deftere nakledileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="258c4-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="258c4-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="258c4-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="258c4-106">Deftere nakil profilinde faiz ayarlayın</span><span class="sxs-lookup"><span data-stu-id="258c4-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="258c4-107">Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="258c4-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="258c4-108">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="258c4-108">Click Edit.</span></span>
    * <span data-ttu-id="258c4-109">Açılır listeden bir faiz kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="258c4-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="258c4-110">Bu deftere nakil profilini kullanarak hareketler için faiz hesaplanmasını istemiyorsanız alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="258c4-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="258c4-111">Tablo kısıtlaması sekmesi, faiz işleme biçimini değiştirmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="258c4-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="258c4-112">Bu alan Evet olarak ayarlanırsa, bu deftere nakil profili için faiz hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="258c4-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="258c4-113">Vade farkını hesapla</span><span class="sxs-lookup"><span data-stu-id="258c4-113">Calculate interest</span></span>
1. <span data-ttu-id="258c4-114">Alacak ve tahsilatlar > Faiz > Vade farkı dekontları oluştur'a gidin.</span><span class="sxs-lookup"><span data-stu-id="258c4-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="258c4-115">Faizini hesaplayacağınız hareket türlerini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="258c4-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="258c4-116">Bu türlerdeki açık hareketlerin tümü hesaplamaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="258c4-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="258c4-117">Faiz'i seçerseniz, faizin faizini hesaplarsınız.</span><span class="sxs-lookup"><span data-stu-id="258c4-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="258c4-118">Bu hareketleri dahil etmeden önce faizin faizini hesaplamayı kontrol eden yasaları incelemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="258c4-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="258c4-119">Faiz, bu tarihten "Bitiş tarihi"ne kadar olan dönem üzerinden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="258c4-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="258c4-120">Bir "Başlangıç tarihi" belirtmezseniz, deftere nakledilmemiş tüm vade farkı dekontları iptal edilir ve faiz hareket tarihinden yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="258c4-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="258c4-121">Vade farkı dekontunun tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="258c4-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="258c4-122">Üç deftere nakil profili seçeneği vardır:   Hesap – Her bir vade farkı dekontunun müşteri hesabına atanan deftere nakil profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="258c4-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="258c4-123">Seçim – Deftere nakil profili alanında seçtiğiniz deftere nakil profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="258c4-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="258c4-124">Hareket – Her bir vade farkı dekontu için faizin hesaplandığı hareketlerdeki bağımsız deftere nakil profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="258c4-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="258c4-125">Atanmış deftere nakil profili olmayan hareketlerde, Alacak hesapları parametreleri formundaki Genel muhasebe ve satış vergisi alanında belirtilen deftere nakil profili kullanılır.</span><span class="sxs-lookup"><span data-stu-id="258c4-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="258c4-126">"Kullanılacak deftere nakil profili" ayarını "Seç" olarak değiştirdiyseniz, burada bir deftere nakil profili seçin.</span><span class="sxs-lookup"><span data-stu-id="258c4-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="258c4-127">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="258c4-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="258c4-128">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="258c4-128">Click Filter.</span></span>
5. <span data-ttu-id="258c4-129">Ölçütler alanına bir Müşteri kodu girin.</span><span class="sxs-lookup"><span data-stu-id="258c4-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="258c4-130">Örneğin, TR-001 girin.</span><span class="sxs-lookup"><span data-stu-id="258c4-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="258c4-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="258c4-131">Click OK.</span></span>
7. <span data-ttu-id="258c4-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="258c4-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="258c4-133">Vade farkı dekontlarını yazdır</span><span class="sxs-lookup"><span data-stu-id="258c4-133">Print interest notes</span></span>
1. <span data-ttu-id="258c4-134">Alacak ve tahsilatlar > Faiz > Vade farkı dekontlarını gözden geçir ve işle'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="258c4-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="258c4-135">Durum alanında, "Oluşturuldu"yu seçin.</span><span class="sxs-lookup"><span data-stu-id="258c4-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="258c4-136">Yazdırıldı alanında, "Yazdırılmadı"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="258c4-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="258c4-137">Yazdır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="258c4-137">Click Print.</span></span>
5. <span data-ttu-id="258c4-138">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="258c4-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="258c4-139">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="258c4-139">Click OK.</span></span>
7. <span data-ttu-id="258c4-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="258c4-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="258c4-141">Vade farkı dekontunu deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="258c4-141">Post the interest note</span></span>
1. <span data-ttu-id="258c4-142">Deftere nakil için hazır bir vade farkı dekontu seçin (durumu Oluşturuldu'dur).</span><span class="sxs-lookup"><span data-stu-id="258c4-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="258c4-143">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="258c4-143">Click Post.</span></span>
3. <span data-ttu-id="258c4-144">Vade farkı dekontu için deftere nakil tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="258c4-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="258c4-145">Her bir vade farkı dekontu için bir genel muhasebe hareketi oluşturmak üzere Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="258c4-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="258c4-146">Evet'i seçmezseniz, müşteriye gidecek tüm vade farkı dekontlarındaki faizler toplanır ve tek harekette genel muhasebeye nakledilir.</span><span class="sxs-lookup"><span data-stu-id="258c4-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="258c4-147">Eklenecek kayıtlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="258c4-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="258c4-148">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="258c4-148">Click OK.</span></span>
6. <span data-ttu-id="258c4-149">Durum alanında, "Deftere nakledildi"yi seçin.</span><span class="sxs-lookup"><span data-stu-id="258c4-149">In the Status field, select 'Posted'.</span></span>


