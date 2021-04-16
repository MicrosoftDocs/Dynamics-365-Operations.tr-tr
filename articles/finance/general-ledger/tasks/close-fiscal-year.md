---
title: Mali yılı kapatma
description: Bu yordam, bakiyeleri yeni bir mali yıla aktaran yıl sonu kapanış işlemini adım adım açıklar.
author: aprilolson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f17b7fefb9251a28bfba9d0e93b9ad171ef7b9c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815200"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="ec19f-103">Mali yılı kapatma</span><span class="sxs-lookup"><span data-stu-id="ec19f-103">Close the fiscal year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec19f-104">Bu yordam, bakiyeleri yeni bir mali yıla aktaran yıl sonu kapanış işlemini adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="ec19f-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="ec19f-105">Yıl sonu kapatma parametrelerini doğrulama</span><span class="sxs-lookup"><span data-stu-id="ec19f-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="ec19f-106">**Gezinti bölmesi > Modüller > Genel muhasebe > Genel muhasebe ayarı > Genel muhasebe parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="ec19f-107">**Mali yıl kapanışı** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="ec19f-108">Aktarmadan sonra **Yıl kapanışı hareketlerini sil** seçeneği için 'Evet' veya 'Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="ec19f-109">Mali yıl zaten kapanmışsa ve yıl sonu kapanışı tekrar çalıştırılıyorsa bu ayar önemlidir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="ec19f-110">Evet olarak ayarlanırsa, önceki yıl sonu kapanışına ait fiş silinecek ve tüm hesap başlangıç bakiyeleri için yeni bir fiş oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="ec19f-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="ec19f-111">Hayır olarak ayarlanırsa, önceki fiş kalacak ve yeni fiş yalnızca son yıl sonu kapanışından sonra nakledilmiş ayarlama girişleri için oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="ec19f-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="ec19f-112">**Aktarma sırasında kapanış hareketleri oluştur** seçeneği için 'Evet'i veya 'Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="ec19f-113">Evet olarak ayarlanırsa, iki hareket oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ec19f-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="ec19f-114">İlk fiş P&L genel muhasebe hareketlerini sıfıra getirmek için kapatılan mali yılda oluşturulur, ikinci fiş ise başlangıç bakiyeleri için bir sonraki mali yılda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ec19f-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="ec19f-115">Hayır olarak ayarlanırsa başlangıç bakiyeleri için bir sonraki mali yılda tek bir fiş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ec19f-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="ec19f-116">**Mali yıl durumunu kalıcı olarak kapatıldı** olarak ayarla için Evet'i veya Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="ec19f-117">Evet olarak ayarlanırsa mali yıl durumu Kalıcı olarak kapatıldı olarak belirlenir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="ec19f-118">Kalıcı olarak kapatılan bir yıl yeniden açılamadığından en iyi uygulama bu seçeneği Hayır olarak ayarlamak olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ec19f-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="ec19f-119">**Yıl sonu kapanışı sırasında Fiş numarası doldurulmalıdır** seçeneği için Evet'i veya Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="ec19f-120">Evet olarak ayarlanırsa, fiş numarası yıl sonu kapanış işlemi sırasında el ile girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="ec19f-121">Bu fiş numarasını oluşturmak için bir numara serisi kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="ec19f-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="ec19f-122">En iyi uygulama bunu Evet olarak ayarlamaktır.</span><span class="sxs-lookup"><span data-stu-id="ec19f-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="ec19f-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-123">Close the page.</span></span>
8. <span data-ttu-id="ec19f-124">**Genel muhasebe > Yakın dönem > Yıl sonu kapanışı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="ec19f-125">Yıl sonu kapanış şablonu oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="ec19f-126">Yıl sonu kapanışını çalıştırmak amacıyla tüzel kişilikler grubu için bir şablon oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="ec19f-127">Bu şablon yıldan yıla yeniden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="ec19f-128">**Grup adı** alanında yıl sonu kapanış şablonunun adını girin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="ec19f-129">**Mali takvim** alanında, şablonun oluşturulacağı mali yılı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="ec19f-130">Yıl sonu kapanış şablonunda yalnızca aynı mali yılı kullanan tüzel kişilikler bir arada gruplandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="ec19f-131">Bunun nedeni yıl sonu kapanışının tarih yerine mali yılın seçilmesiyle gerçekleştirilmesidir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="ec19f-132">**Eylem Bölmesi**'nde, **Kaydet** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="ec19f-133">**Tüzel kişilikler** bölmesinde, bu şablon için tüzel kişileri seçmek üzere **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="ec19f-134">Tüzel kişilikler, tüzel kişilikleri seçerek veya bir kurumsal hiyerarşi seçerek eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="ec19f-135">Yalnızca aynı mali takvime sahip kurumsal hiyerarşi ile seçilen tüzel kişilikler eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="ec19f-136">Tüzel kişilikleri veya kurumsal hiyerarşiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="ec19f-137">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-137">Click **OK**.</span></span>
16. <span data-ttu-id="ec19f-138">**Bilanço boyutlarını aktar** öğesinde 'Evet' ya da 'Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="ec19f-139">En iyi uygulama bu seçeneği Bilanço hesapları için Evet olarak ayarlamaktır.</span><span class="sxs-lookup"><span data-stu-id="ec19f-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="ec19f-140">Bu, bilanço hesapları için başlangıç bakiyeleri oluşturulurken deftere nakledilmiş hareketler üzerinden mali boyutları günceller.</span><span class="sxs-lookup"><span data-stu-id="ec19f-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="ec19f-141">Kar ve zarar hesapları için bilançolar Yedek akçelere taşındığında mali boyutları güncelleştirmeyi seçebilirsiniz (Tümünü kapat) veya mali boyutları farklı bir boyut değeri ile değiştirmeyi seçebilirsiniz (Tek kapat).</span><span class="sxs-lookup"><span data-stu-id="ec19f-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="ec19f-142">Tek Kapat'ı seçerseniz, her boyut için belirli bir boyut değeri tanımlayabilir veya boş bırakmayı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec19f-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="ec19f-143">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-143">Click **Save**.</span></span>
18. <span data-ttu-id="ec19f-144">**Eylem Bölmesi**'nde **Mali kapanışı çalıştır**'ı seçerek yıl sonu kapanışını başlatın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="ec19f-145">Yıl sonu kapanışı seçilen şablon için çalıştırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="ec19f-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="ec19f-146">Yıl sonu kapanışını çalıştırmak için şablondan tüzel kişiliklerin tamamını veya alt kümesini seçin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="ec19f-147">İlk önce yıl sonu kapanışı çalıştırıldığında çoğu kuruluş başlangıç bakiyelerini almak için şablon dahilindeki tüm tüzel kişilikler için yıl sonu kapanışını çalıştırmayı tercih edebilir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="ec19f-148">Ayarlama girişleri bundan sonra yapılırsa yalnızca ayarları yapılan tüzel kişilikler için yıl sonu kapanışını çalıştırmayı tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec19f-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="ec19f-149">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-149">Click **OK**.</span></span>
21. <span data-ttu-id="ec19f-150">Yıl sonu kapanışının çalıştırılacağı mali yılı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec19f-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="ec19f-151">**Fiş alanı**'na bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="ec19f-152">Oluşturulan yıl sonu kapanış fişinin bulunmasını kolaylaştırmak için en iyi uygulama mali yılı fiş numarasına dahil etmektir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="ec19f-153">Toplu iş modunda çalıştırmak için yıl sonu kapanışı varsayılanları.</span><span class="sxs-lookup"><span data-stu-id="ec19f-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="ec19f-154">Uzun süreli işlemler için en iyi uygulama toplu iş modunda çalıştırmaktır.</span><span class="sxs-lookup"><span data-stu-id="ec19f-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="ec19f-155">Bu, genel olarak varsayılanın iş modunda kullanılma sebebi olan süreçlerden biridir.</span><span class="sxs-lookup"><span data-stu-id="ec19f-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="ec19f-156">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec19f-156">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]