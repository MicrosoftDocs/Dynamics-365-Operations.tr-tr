---
title: Kalite emirlerini ayarlama
description: "Bu prosedürde, size, gelen stoğun varış kaydı yapıldıktan hemen sonra incelenmesi gerektiği durumlarda kalite yönetim işleminin nasıl etkinleştirileceği gösterilmektedir."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: f43c2cb9dca441a796d1ec2ec2e17da063dddaa9
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="ec641-103">Kalite emirlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="ec641-103">Set up quality orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec641-104">Bu prosedürde, size, gelen stoğun varış kaydı yapıldıktan hemen sonra incelenmesi gerektiği durumlarda kalite yönetim işleminin nasıl etkinleştirileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ec641-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="ec641-105">Bu prosedür genellikle bir kalite yöneticisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ec641-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="ec641-106">İşlem, örnek alınacak maddeleri tanımlamak üzere bir kalite grubu oluşturmayı ve kalite grubundaki maddeler üzerinde uygulanacak testleri gruplandırmak üzere bir test grubu oluşturmayı içerir.</span><span class="sxs-lookup"><span data-stu-id="ec641-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="ec641-107">USMF demo veriler şirketinde bu kılavuzu çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec641-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="ec641-108">Kalite yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ec641-108">Enable quality management</span></span>
1. <span data-ttu-id="ec641-109">Stokyönetimi > Kurulum > Stok ve ambar yönetim parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ec641-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="ec641-110">Kalite yönetimi sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="ec641-111">Kalite yönetimini kullan seçeneğini Evet konumuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="ec641-112">Rapor kurulumu'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-112">Click Report setup.</span></span>
    * <span data-ttu-id="ec641-113">USMF'de, kalite yönetimi için rapor kurulumu zaten tanımlıdır.</span><span class="sxs-lookup"><span data-stu-id="ec641-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="ec641-114">Bu yapılmadıysa farklı rapor türleri için buraya yeni satırlar eklemeli ve her bir rapor için kullanılacak belge türünü seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="ec641-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="ec641-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-115">Close the page.</span></span>
6. <span data-ttu-id="ec641-116">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="ec641-117">Test oluşturun</span><span class="sxs-lookup"><span data-stu-id="ec641-117">Create a test</span></span>
1. <span data-ttu-id="ec641-118">Stok yönetimi > Kurulum > Kalite kontrol > Testler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ec641-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="ec641-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-119">Click New.</span></span>
3. <span data-ttu-id="ec641-120">Test türü alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="ec641-121">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ec641-122">Tür alanında, "Seçenek"i seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="ec641-123">Bu örnekte, test sonuçlarını önceden tanımlanmış değerler temel alınarak atamayı olanaklı hale getiren "Seçenek"i seçeceğiz.</span><span class="sxs-lookup"><span data-stu-id="ec641-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="ec641-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-124">Click Save.</span></span>
7. <span data-ttu-id="ec641-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="ec641-126">Test sonuçlarını kaydetme şeklini tanımlamak için Test değişkenleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="ec641-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="ec641-127">Stok yönetimi > Kurulum > Kalite kontrol > Test değişkenleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ec641-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="ec641-128">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-128">Click New.</span></span>
3. <span data-ttu-id="ec641-129">Değişken alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="ec641-130">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ec641-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-131">Click Save.</span></span>
6. <span data-ttu-id="ec641-132">Sonuçlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-132">Click Outcomes.</span></span>
7. <span data-ttu-id="ec641-133">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-133">Click New.</span></span>
8. <span data-ttu-id="ec641-134">Sonuç alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="ec641-135">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="ec641-136">Sonuç alanında, "Başarılı"yı seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="ec641-137">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-137">Click Save.</span></span>
12. <span data-ttu-id="ec641-138">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-138">Click New.</span></span>
13. <span data-ttu-id="ec641-139">Sonuç alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="ec641-140">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="ec641-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-141">Click Save.</span></span>
16. <span data-ttu-id="ec641-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-142">Close the page.</span></span>
17. <span data-ttu-id="ec641-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="ec641-144">Madde örneklemesi ayarlayın</span><span class="sxs-lookup"><span data-stu-id="ec641-144">Set up item sampling</span></span>
1. <span data-ttu-id="ec641-145">Stok yönetimi > Kurulum > Kalite kontrol > Madde örnekleme öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ec641-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="ec641-146">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-146">Click New.</span></span>
3. <span data-ttu-id="ec641-147">Madde örnekleme alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="ec641-148">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ec641-149">Değer alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="ec641-150">Bu değer bitişik alanda seçilen Miktar belirtimiyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="ec641-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="ec641-151">İşlem bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ec641-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="ec641-152">Tam durdurma onay kutusunu işaretleyin veya işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ec641-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="ec641-153">Bu seçeneği belirtirseniz, bir test başarısız olduğu zaman tüm lot veya sipariş satırı miktarı engellenir.</span><span class="sxs-lookup"><span data-stu-id="ec641-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="ec641-154">Seçmezseniz, yalnızca kalite emrindeki maddeler engellenir.</span><span class="sxs-lookup"><span data-stu-id="ec641-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="ec641-155">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-155">Click Save.</span></span>
9. <span data-ttu-id="ec641-156">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="ec641-157">Kalite grubu oluşturun</span><span class="sxs-lookup"><span data-stu-id="ec641-157">Create a quality group</span></span>
1. <span data-ttu-id="ec641-158">Stok yönetimi > Kurulum > Kalite kontrol > Kalite grupları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ec641-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="ec641-159">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-159">Click New.</span></span>
3. <span data-ttu-id="ec641-160">Kalite grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="ec641-161">Grupta hangi tür maddelerin (örnekleme ölçütlerinizin) yer alacağını bilmenize yardımcı olacak açıklayıcı bir ad kullanın.</span><span class="sxs-lookup"><span data-stu-id="ec641-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="ec641-162">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ec641-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-163">Click Save.</span></span>
6. <span data-ttu-id="ec641-164">Madde ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-164">Click Add items.</span></span>
7. <span data-ttu-id="ec641-165">Madde numarası satırını seçin</span><span class="sxs-lookup"><span data-stu-id="ec641-165">Select the Item number row</span></span>
    * <span data-ttu-id="ec641-166">Bu örnekte filtreleme madde numarasına göre yapılacak.</span><span class="sxs-lookup"><span data-stu-id="ec641-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="ec641-167">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ec641-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="ec641-168">Örneğin, T harfiyle başlayan madde numaralarını filtrelemek için T\* yazın.</span><span class="sxs-lookup"><span data-stu-id="ec641-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="ec641-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-169">Click OK.</span></span>
10. <span data-ttu-id="ec641-170">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-170">Click OK.</span></span>
11. <span data-ttu-id="ec641-171">Madde kalite gruplarına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="ec641-172">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-172">Close the page.</span></span>
13. <span data-ttu-id="ec641-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="ec641-174">Test grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ec641-174">Create a test group</span></span>
1. <span data-ttu-id="ec641-175">Stok yönetimi > Kurulum > Kalite kontrol > Test grupları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ec641-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="ec641-176">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-176">Click New.</span></span>
3. <span data-ttu-id="ec641-177">Test grubu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="ec641-178">Test grubuna, ne tür testlerin çalıştırılmakta olduğunu ve grubun hangi kalite grubuyla ilişkilendirileceğini hatırlamanıza yardımcı olacak bir ad verin.</span><span class="sxs-lookup"><span data-stu-id="ec641-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="ec641-179">Örneğin "T" harfiyle başlayan maddeleri seçen bir kalite grubuyla kullanılacaksa, gruba "T-madde testleri" adı verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec641-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="ec641-180">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ec641-181">Madde örnekleme alanında, önceden oluşturduğunuz madde örnekleme satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="ec641-182">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ec641-183">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-183">Click Add.</span></span>
8. <span data-ttu-id="ec641-184">Sıra numarası alanına bir numara girin.</span><span class="sxs-lookup"><span data-stu-id="ec641-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="ec641-185">Test alanında, daha önce oluşturduğunuz testi seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="ec641-186">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="ec641-187">Test sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-187">Click the Test tab.</span></span>
12. <span data-ttu-id="ec641-188">Değişken alanında, daha önce oluşturduğunuz test değişkenini seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="ec641-189">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="ec641-190">Varsayılan sonuç alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ec641-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="ec641-191">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="ec641-192">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-192">Click Save.</span></span>
17. <span data-ttu-id="ec641-193">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="ec641-194">Kalite emirlerinin ne zaman oluşturulacağını tanımlayın</span><span class="sxs-lookup"><span data-stu-id="ec641-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="ec641-195">Stok yönetimi > Kurulum > Kalite kontrol > Kalite ilişkileri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ec641-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="ec641-196">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-196">Click New.</span></span>
3. <span data-ttu-id="ec641-197">Referans türü alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="ec641-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="ec641-198">Madde kodu alanında, "Grup"u seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="ec641-199">Bu örnekte, "Grup"u seçeceğiz ve daha önce oluşturduğumuz kalite grubunu kullanacağız.</span><span class="sxs-lookup"><span data-stu-id="ec641-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="ec641-200">Ayrıca, maddeleri el ile belirtmek için ayarını "Tablo" yapabilir veya kalite emrine tüm maddeleri eklemek için "Tümü"nü seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec641-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="ec641-201">Madde alanında, önceden oluşturduğunuz kalite grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="ec641-202">Madde alanındaki kullanılabilir seçenekler, Madde kodu alanındaki ayarlarınıza bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ec641-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="ec641-203">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ec641-204">İşlem bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ec641-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="ec641-205">Olay türü alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="ec641-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="ec641-206">Bu, testi tetikleyen olaydır.</span><span class="sxs-lookup"><span data-stu-id="ec641-206">This is the event that triggers the test.</span></span> <span data-ttu-id="ec641-207">Buradaki kullanılabilir seçenekler Başvuru türü alanında seçtiğiniz işleme bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ec641-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="ec641-208">Yürütme alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="ec641-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="ec641-209">Kalite emri işlemi bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ec641-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="ec641-210">Olay durdurma alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ec641-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ec641-211">Bu alanda, kalite emri hala açıksa, engellenebilecek işlemlerin listesi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ec641-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="ec641-212">Seçenekler, Olay türü alanındaki seçimlerinize bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ec641-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="ec641-213">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ec641-214">Bu, önceden seçtiğiniz değerlere bağlı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ec641-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="ec641-215">Bir kaynak belge satırıyla bağlantılı açık kalite emirleri varken, izleyen işlemlerin engellenip engellenmemesi gerektiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ec641-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="ec641-216">Belirtimler bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ec641-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="ec641-217">Test grubu alanında, daha önce oluşturduğunuz test grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="ec641-218">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec641-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="ec641-219">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec641-219">Click Save.</span></span>
17. <span data-ttu-id="ec641-220">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec641-220">Close the page.</span></span>

