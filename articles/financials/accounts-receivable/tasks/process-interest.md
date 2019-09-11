---
title: Faiz işleme
description: Bu prosedürde, vade farkı dekontlarının nasıl oluşturulacağı, yazdırılacağı ve deftere nakledileceği gösterilmektedir.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7170a7a14237058064ed3091e9437cae312e6bd5
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916288"
---
# <a name="process-interest"></a><span data-ttu-id="3e0fb-103">Faiz işleme</span><span class="sxs-lookup"><span data-stu-id="3e0fb-103">Process interest</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e0fb-104">Bu prosedürde, vade farkı dekontlarının nasıl oluşturulacağı, yazdırılacağı ve deftere nakledileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="3e0fb-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="3e0fb-106">Deftere nakil profilinde faiz ayarlayın</span><span class="sxs-lookup"><span data-stu-id="3e0fb-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="3e0fb-107">**Gezinti bölmesinde** **Modüller > Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="3e0fb-108">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-108">Click **Edit**.</span></span>
3. <span data-ttu-id="3e0fb-109">**Kurulum hızlı sekmesinde**, **Faiz kodu** alanında, açılan listeden bir faiz kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="3e0fb-110">Bu deftere nakil profilini kullanarak hareketler için faiz hesaplanmasını istemiyorsanız alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="3e0fb-111">**Tablo kısıtlaması** hızlı sekmesi, faiz işleme biçimini değiştirmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="3e0fb-112">Bu alan Evet olarak ayarlanırsa, bu deftere nakil profili için faiz hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="3e0fb-113">Vade farkını hesapla</span><span class="sxs-lookup"><span data-stu-id="3e0fb-113">Calculate interest</span></span>
1. <span data-ttu-id="3e0fb-114">**Gezinti bölmesinde** **Modüller > Alacak ve tahsilatlar > Faiz > Vade farkı dekontları oluştur**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="3e0fb-115">Faizini hesaplayacağınız hareket türlerini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="3e0fb-116">Bu türlerdeki açık hareketlerin tümü hesaplamaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="3e0fb-117">**Faiz**'i 'Evet' olarak ayarlarsanız faizin faizini hesaplarsınız.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="3e0fb-118">Bu hareketleri dahil etmeden önce faizin faizini hesaplamayı kontrol eden yasaları incelemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="3e0fb-119">**Başlangıç tarihi** alanına bu faiz hesaplamasının başlayacağı tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="3e0fb-120">Bir **Başlangıç tarihi** belirtmezseniz, deftere nakledilmemiş tüm vade farkı dekontları iptal edilir ve faiz hareket tarihinden yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="3e0fb-121">**Bitiş tarihi** alanına bu faiz hesaplamasının biteceği tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="3e0fb-122">**Şuradan alınan değerleri kullan** alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="3e0fb-123">Üç deftere nakil profili seçeneği vardır:</span><span class="sxs-lookup"><span data-stu-id="3e0fb-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="3e0fb-124">Hesap – Her vade farkı dekontu için müşteri hesabına atanmış deftere nakil profilini kullan.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="3e0fb-125">Seçim – Deftere nakil profili alanında seçtiğiniz deftere nakil profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="3e0fb-126">Hareket – Her bir vade farkı dekontu için faizin hesaplandığı hareketlerdeki bağımsız deftere nakil profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="3e0fb-127">Atanmış deftere nakil profili olmayan hareketlerde, Alacak hesapları parametreleri formundaki Genel muhasebe ve satış vergisi alanında belirtilen deftere nakil profili kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="3e0fb-128">**Eklenecek kayıtlar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="3e0fb-129">**Filtrele** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-129">Click **Filter**.</span></span>
9. <span data-ttu-id="3e0fb-130">**Ölçütler** alanına bir Müşteri kodu girin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="3e0fb-131">Örneğin, 'TR-001' girin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="3e0fb-132">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-132">Click **OK**.</span></span>
7. <span data-ttu-id="3e0fb-133">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="3e0fb-134">Vade farkı dekontlarını yazdır</span><span class="sxs-lookup"><span data-stu-id="3e0fb-134">Print interest notes</span></span>
1. <span data-ttu-id="3e0fb-135">**Gezinti bölmesinde** **Modüller > Alacak ve tahsilatlar > Faiz > Vade farkı dekontlarını incele ve işle**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="3e0fb-136">**Durum** alanında, "Oluşturuldu"yu seçin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="3e0fb-137">**Yazdırıldı** alanında, "Yazdırılmadı"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="3e0fb-138">**Yazdır**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-138">Click **Print**.</span></span>
5. <span data-ttu-id="3e0fb-139">**Eklenecek kayıtlar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="3e0fb-140">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-140">Click **OK**.</span></span>
7. <span data-ttu-id="3e0fb-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="3e0fb-142">Vade farkı dekontunu deftere nakledin</span><span class="sxs-lookup"><span data-stu-id="3e0fb-142">Post the interest note</span></span>
1. <span data-ttu-id="3e0fb-143">Deftere nakil için hazır bir vade farkı dekontu seçin (durumu Oluşturuldu'dur).</span><span class="sxs-lookup"><span data-stu-id="3e0fb-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="3e0fb-144">**Naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-144">Click **Post**.</span></span>
3. <span data-ttu-id="3e0fb-145">Vade farkı dekontu için deftere nakil tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="3e0fb-146">Her bir vade farkı dekontu için bir genel muhasebe hareketi oluşturmak üzere Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="3e0fb-147">Evet'i seçmezseniz, müşteriye gidecek tüm vade farkı dekontlarındaki faizler toplanır ve tek harekette genel muhasebeye nakledilir.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="3e0fb-148">**Eklenecek kayıtlar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="3e0fb-149">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-149">Click **OK**.</span></span>
6. <span data-ttu-id="3e0fb-150">**Durum** alanında, "Deftere nakledildi"yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3e0fb-150">In the **Status** field, select 'Posted'.</span></span>

