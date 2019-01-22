--- 
title: "Tahsilat mektuplarını işleme"
description: "Bu yordam, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 18eaadf417ce6d0aacf0b13b3e4f857e06031e66
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.contentlocale: tr-tr
ms.lasthandoff: 01/22/2019

---
# <a name="process-collection-letters"></a><span data-ttu-id="579a3-103">Tahsilat mektuplarını işleme</span><span class="sxs-lookup"><span data-stu-id="579a3-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="579a3-104">Bu yordam, tahsilat mektuplarının nasıl oluşturulacağını, yazdırılacağını ve deftere nakledileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="579a3-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="579a3-105">Bu görevde USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="579a3-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="579a3-106">Deftere nakil profilinde bir tahsilat mektubu sırası ayarlama</span><span class="sxs-lookup"><span data-stu-id="579a3-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="579a3-107">**Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="579a3-107">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="579a3-108">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="579a3-108">Click **Edit**.</span></span>
3. <span data-ttu-id="579a3-109">Açılan listeden bir tahsilat mektubu sırası seçin.</span><span class="sxs-lookup"><span data-stu-id="579a3-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="579a3-110">Bu deftere nakil profilini kullanarak hareketler için tahsilat mektupları oluşturmak istemiyorsanız ilgili alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="579a3-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="579a3-111">Tablo kısıtlaması sekmesini genişletin, tahsilat mektuplarını işleme biçimini değiştirmek için.</span><span class="sxs-lookup"><span data-stu-id="579a3-111">Expand the table restriction tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="579a3-112">Bu alan **Evet** olarak ayarlanırsa, bu deftere nakil profili için tahsilat mektupları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="579a3-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="579a3-113">Tahsilat mektupları oluştur</span><span class="sxs-lookup"><span data-stu-id="579a3-113">Create collection letters</span></span>
1. <span data-ttu-id="579a3-114">**Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektupları oluştur**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="579a3-114">Go to **Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="579a3-115">Tahsilat mektuplarının hareket türlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="579a3-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="579a3-116">Bu türlerdeki açık hareketlerin tümü hesaplamaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="579a3-116">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="579a3-117">**Tahsilat mektubu** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="579a3-117">In the **Collection letter** field, select an option.</span></span>
3. <span data-ttu-id="579a3-118">Tahsilat mektubunun tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="579a3-118">Enter the date of the collection letter.</span></span>
4. <span data-ttu-id="579a3-119">**Kullanılacak deftere nakil profili:** seçeneğini **Seç** olarak değiştirdiyseniz, bir deftere nakil profili seçin.</span><span class="sxs-lookup"><span data-stu-id="579a3-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="579a3-120">İki deftere nakletme profili seçeneği vardır:</span><span class="sxs-lookup"><span data-stu-id="579a3-120">There are two posting profile options:</span></span>   
   - <span data-ttu-id="579a3-121">**Hesap** – Her vade farkı dekontu için müşteri hesabına atanmış deftere nakil profilini kullan.</span><span class="sxs-lookup"><span data-stu-id="579a3-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="579a3-122">**Seçim** – **Deftere nakil profili** alanında seçtiğiniz deftere nakil profilini kullanın.</span><span class="sxs-lookup"><span data-stu-id="579a3-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  
5. <span data-ttu-id="579a3-123">**Eklenecek kayıtlar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="579a3-123">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="579a3-124">**Filtrele** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="579a3-124">Click **Filter**.</span></span>
7. <span data-ttu-id="579a3-125">**Ölçütler** alanına bir Müşteri kodu girin.</span><span class="sxs-lookup"><span data-stu-id="579a3-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="579a3-126">Örneğin, 'TR-001' girin.</span><span class="sxs-lookup"><span data-stu-id="579a3-126">For example, enter 'US-001'.</span></span>
8. <span data-ttu-id="579a3-127">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="579a3-127">Click **OK**.</span></span>
9. <span data-ttu-id="579a3-128">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="579a3-128">Click **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="579a3-129">Tahsilat mektuplarını yazdırma</span><span class="sxs-lookup"><span data-stu-id="579a3-129">Print collection letters</span></span>
1. <span data-ttu-id="579a3-130">**Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektuplarını gözden geçir ve işle**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="579a3-130">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="579a3-131">**Durum** alanında, **Oluşturuldu**yu seçin.</span><span class="sxs-lookup"><span data-stu-id="579a3-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="579a3-132">**Yazdırıldı** alanında, **Yazdırılmadı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="579a3-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="579a3-133">**Yazdır**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="579a3-133">Click **Print**.</span></span>
5. <span data-ttu-id="579a3-134">**Tahsilat mektubu dekontu**'nu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="579a3-134">Click **Collection letter note**.</span></span>
6. <span data-ttu-id="579a3-135">**Eklenecek kayıtlar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="579a3-135">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="579a3-136">Deftere nakiller için bir fatura kesme tarihi girin.</span><span class="sxs-lookup"><span data-stu-id="579a3-136">Enter the cutoff date for postings.</span></span>
8. <span data-ttu-id="579a3-137">Tahsilat mektubunu yazdırmak için **Tamam**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="579a3-137">Click **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="579a3-138">Tahsilat mektubunu deftere nakletme.</span><span class="sxs-lookup"><span data-stu-id="579a3-138">Post the collection letter.</span></span>
   1. <span data-ttu-id="579a3-139">**Naklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="579a3-139">Click **Post**.</span></span>
   2. <span data-ttu-id="579a3-140">Tahsilat mektubu için deftere nakil tarihini girin.</span><span class="sxs-lookup"><span data-stu-id="579a3-140">Enter the posting date for the collection letter.</span></span>
   3. <span data-ttu-id="579a3-141">**Eklenecek kayıtlar** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="579a3-141">Expand the **Records to include** section.</span></span>
   4. <span data-ttu-id="579a3-142">**Tamam** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="579a3-142">Click **OK**.</span></span>
   5. <span data-ttu-id="579a3-143">**Durum** alanında, **Deftere nakledildi**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="579a3-143">In the **Status** field, select **Posted**.</span></span>
   6. <span data-ttu-id="579a3-144">**Yazdırılan** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="579a3-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="579a3-145">Müşteri düzeyinde tahsilat mektuplarını denetleyin</span><span class="sxs-lookup"><span data-stu-id="579a3-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="579a3-146">Her bir hareket için tahsilat mektup kodunun izlenmesi için tahsilat mektuplarını ayarlayabilirsiniz, ancak tahsilat mektubu işleme, müşteri için kaydedilmiş tek bir tahsilat mektubu düzeyine dayanacaktır.</span><span class="sxs-lookup"><span data-stu-id="579a3-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="579a3-147">Tek bir tahsilat mektubu, müşteri için tarihi geçmiş olan tüm hareketleri içerir.</span><span class="sxs-lookup"><span data-stu-id="579a3-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="579a3-148">Mehil gün sayısı müşteri düzeyinde şimdi izlendiği için sıradaki bir sonraki tahsilat mektubunun vade erteleme gün sayısı geçene kadar sonra son tahsilat mektubu hareketleri süresi sona erene olsa da bir sonraki tahsilat mektubu gönderilmeyecek gönderildi.</span><span class="sxs-lookup"><span data-stu-id="579a3-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="579a3-149">Bu seçenek, müşteri başına gönderilecek tahsilat mektuplarının sayısını azaltır.</span><span class="sxs-lookup"><span data-stu-id="579a3-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="579a3-150">Tahsilat mektuplarının kontrol edileceği müşteriyi müşteri düzeyinde ayarlayın</span><span class="sxs-lookup"><span data-stu-id="579a3-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="579a3-151">**Kredi ve tahsilatlar > Kurulum > Alacak hesabı parametreleri**'ne gidin ve **Tahsilatlar** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="579a3-151">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2.  <span data-ttu-id="579a3-152">**Her seferinde tahsilat mektubu oluştur**'u **Müşteri**'ye değiştirin.</span><span class="sxs-lookup"><span data-stu-id="579a3-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="579a3-153">**Alacak ve Tahsilatlar > Tahsilat mektubu > Tahsilat mektuplarını gözden geçir ve işle**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="579a3-153">Go to **Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="579a3-154">Bir müşteri için tüm tarihi geçmiş hareketler içeren tek bir tahsilat mektubu oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="579a3-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="579a3-155">Tahsilat mektubu kodunu hesaplarken için ödemeleri ve alacak faturalarını yoksay</span><span class="sxs-lookup"><span data-stu-id="579a3-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="579a3-156">Tahsilat mektuplarına dahil edilecek hareketlerde ödemeler ve alacak notu dahil ederseniz, bir tahsilat mektubunu tetikleyebilecek ödemeler veya alacak notlarına sahip olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="579a3-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="579a3-157">Ödemeler ve alacak notlarının tahsilat mektubu kodunu nasıl kontrol edebileceğini, **Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay** parametresinin değerini değiştirerek kontrol edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="579a3-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="579a3-158">Tahsilat mektubu kodunu hesaplarken için ödemeleri ve alacak faturalarını yoksaymak için şunu yapın.</span><span class="sxs-lookup"><span data-stu-id="579a3-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>
1. <span data-ttu-id="579a3-159">**Kredi ve tahsilatlar > Kurulum > Alacak hesabı parametreleri**'ne gidin ve **Tahsilatlar** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="579a3-159">Go to **Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="579a3-160">**Tahsilat mektubu kodunu hesaplarken ödemeler ve alacak notlarını yoksay**'ın değerini **Evet** olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="579a3-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>

