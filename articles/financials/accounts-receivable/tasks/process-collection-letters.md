--- 
title: "Tahsilat mektuplarını işleme"
description: "Bu yordam, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir."
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
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="process-collection-letters"></a><span data-ttu-id="a626d-103">Tahsilat mektuplarını işleme</span><span class="sxs-lookup"><span data-stu-id="a626d-103">Process collection letters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a626d-104">Bu yordam, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a626d-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="a626d-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a626d-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="a626d-106">Deftere nakil profilinde bir tahsilat mektubu sırası ayarlama</span><span class="sxs-lookup"><span data-stu-id="a626d-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="a626d-107">Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="a626d-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="a626d-108">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a626d-108">Click Edit.</span></span>
    * <span data-ttu-id="a626d-109">Açılan listeden bir tahsilat mektubu sırası seçin.</span><span class="sxs-lookup"><span data-stu-id="a626d-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="a626d-110">Bu deftere nakil profilini kullanarak hareketler için tahsilat mektupları oluşturmak istemiyorsanız ilgili alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="a626d-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="a626d-111">Tablo kısıtlaması sekmesi, tahsilat mektuplarını işleme biçimini değiştirmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="a626d-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="a626d-112">Bu alan Evet olarak ayarlanırsa, bu deftere nakil profili için tahsilat mektupları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a626d-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="a626d-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a626d-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="a626d-114">Tahsilat mektupları oluştur</span><span class="sxs-lookup"><span data-stu-id="a626d-114">Create collection letters</span></span>
1. <span data-ttu-id="a626d-115">Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektupları oluştur'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a626d-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="a626d-116">Tahsilat mektuplarının hareket türlerini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a626d-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="a626d-117">Bu türlerdeki açık hareketlerin tümü hesaplamaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="a626d-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="a626d-118">Tahsilat mektubu alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a626d-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="a626d-119">Tahsilat mektubunun tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="a626d-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="a626d-120">İki deftere nakil profili seçeneği vardır:   Hesap – Her bir vade farkı dekontunun müşteri hesabına atanan deftere nakil profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a626d-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="a626d-121">Seçim – Deftere nakil profili alanında seçtiğiniz deftere nakil profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a626d-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="a626d-122">"Kullanılacak deftere nakil profili:" seçeneğini "Seç" olarak değiştirdiyseniz, bir deftere nakil profili seçin.</span><span class="sxs-lookup"><span data-stu-id="a626d-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="a626d-123">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a626d-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="a626d-124">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a626d-124">Click Filter.</span></span>
6. <span data-ttu-id="a626d-125">Ölçüt alanında, bir Müşteri Kodu girin.</span><span class="sxs-lookup"><span data-stu-id="a626d-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="a626d-126">Örneğin, TR-001 girin.</span><span class="sxs-lookup"><span data-stu-id="a626d-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="a626d-127">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a626d-127">Click OK.</span></span>
8. <span data-ttu-id="a626d-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a626d-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="a626d-129">Tahsilat mektuplarını yazdırma</span><span class="sxs-lookup"><span data-stu-id="a626d-129">Print collection letters</span></span>
1. <span data-ttu-id="a626d-130">Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektuplarını gözden geçir ve işle'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="a626d-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="a626d-131">Durum alanında, "Oluşturuldu"yu seçin.</span><span class="sxs-lookup"><span data-stu-id="a626d-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="a626d-132">Yazdırıldı alanında, "Yazdırılmadı"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a626d-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="a626d-133">Yazdır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a626d-133">Click Print.</span></span>
5. <span data-ttu-id="a626d-134">Tahsilat mektubu dekontu'nu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a626d-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="a626d-135">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a626d-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="a626d-136">Deftere nakiller için bir fatura kesme tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="a626d-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="a626d-137">Tahsilat mektubunu yazdırmak için Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a626d-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="a626d-138">Tahsilat mektubunu deftere nakletme</span><span class="sxs-lookup"><span data-stu-id="a626d-138">Post the collection letter</span></span>
1. <span data-ttu-id="a626d-139">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a626d-139">Click Post.</span></span>
2. <span data-ttu-id="a626d-140">Tahsilat mektubu için deftere nakil tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="a626d-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="a626d-141">Eklenecek kayıtlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="a626d-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="a626d-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a626d-142">Click OK.</span></span>
5. <span data-ttu-id="a626d-143">Durum alanında, "Deftere nakledildi"yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a626d-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="a626d-144">Yazdırılan alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a626d-144">In the Printed field, select an option.</span></span>


