---
title: Biçim oluşturduğunuzda veri modeli tanımlarını seçme
description: Bu yordamdaki adımları tamamlamak için öncelikle "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamını tamamlamanız gerekir.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66b9636f6d9da06f0ea65ab311dd9308ff6ae020
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184727"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="53070-103">Biçim oluşturduğunuzda veri modeli tanımlarını seçme</span><span class="sxs-lookup"><span data-stu-id="53070-103">Select data model definitions when you create formats</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="53070-104">Bu yordamdaki adımları tamamlamak için öncelikle "ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="53070-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="53070-105">Bu yordam, elektronik belgeler oluşturmak için tasarlanmış bir Elektronik raporlama (ER) biçimi yapılandırması olarak nasıl bir modeli kök öğesinin bir veri modeli tanımı olarak nasıl seçilebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="53070-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="53070-106">Bu yordamda, 'Litware, Inc.' örnek şirketi için bir ER biçim yapılandırması ekleyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="53070-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="53070-107">Bu yordam Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar içindir.</span><span class="sxs-lookup"><span data-stu-id="53070-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="53070-108">Adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir.</span><span class="sxs-lookup"><span data-stu-id="53070-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="53070-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="53070-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="53070-110">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve etkin olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="53070-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="53070-111">Bu yapılandırma sağlayıcısını göremiyorsanız "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="53070-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="53070-112">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="53070-113">Yeni bir ER veri modeli yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="53070-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="53070-114">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="53070-115">ER raporları oluşturma için bir veri modeli olarak kullanılacak bir veri modeli içeren yeni bir ER model yapılandırması ekliyoruz.</span><span class="sxs-lookup"><span data-stu-id="53070-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="53070-116">İsim alanında, 'Ödeme modeli (hayali)' yazın.</span><span class="sxs-lookup"><span data-stu-id="53070-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="53070-117">Ödeme modeli (hayali)</span><span class="sxs-lookup"><span data-stu-id="53070-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="53070-118">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="53070-118">Click Create configuration.</span></span>
4. <span data-ttu-id="53070-119">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="53070-119">Click Designer.</span></span>
    * <span data-ttu-id="53070-120">Bu yapılandırmanın veri modelinin yapısını belirtmek için ER tasarımcısını açın.</span><span class="sxs-lookup"><span data-stu-id="53070-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="53070-121">2 ödeme yöntemini desteklemek için iş etki alanı için veri modelini tasarladığımızı varsayalım – alacak transferi ve otomatik ödemeler.</span><span class="sxs-lookup"><span data-stu-id="53070-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="53070-122">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="53070-123">İsim alanında 'Ödemeler – alacak transferi' yazın.</span><span class="sxs-lookup"><span data-stu-id="53070-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="53070-124">Ödemeler – kredi transferi</span><span class="sxs-lookup"><span data-stu-id="53070-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="53070-125">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="53070-125">Click Add.</span></span>
8. <span data-ttu-id="53070-126">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="53070-127">Yeni düğüm biçimi alanına "Model kökü" girin.</span><span class="sxs-lookup"><span data-stu-id="53070-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="53070-128">İsim alanında 'Ödemeler – hesaptan ödeme' yazın.</span><span class="sxs-lookup"><span data-stu-id="53070-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="53070-129">Ödemeler – otomatik ödeme</span><span class="sxs-lookup"><span data-stu-id="53070-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="53070-130">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="53070-130">Click Add.</span></span>
12. <span data-ttu-id="53070-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-131">Click Save.</span></span>
13. <span data-ttu-id="53070-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="53070-132">Close the page.</span></span>
14. <span data-ttu-id="53070-133">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-133">Click Change status.</span></span>
    * <span data-ttu-id="53070-134">Yeni model eşlemeleri ve biçimlerinde kullanılabilir hale getirmek için modelin taslak sürümünü tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="53070-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="53070-135">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-135">Click Complete.</span></span>
16. <span data-ttu-id="53070-136">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="53070-137">Yeni bir ER biçimi yapılandırması girmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="53070-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="53070-138">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="53070-139">Yeni alanına, 'Ödemeler modeli (hayali) veri modelini temel alan biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="53070-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="53070-140">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="53070-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="53070-141">Seçilen veri modelinin tüm kök maddelerinin bir veri modeli tanımı olarak şu anda kullanılabilir olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="53070-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="53070-142">Biçiminizi, veri modelinin gereken maddelerinin herhangi birini kullanarak tasarlamaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53070-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="53070-143">Seçilen kök maddesi için eksik bir model eşlemesi, çalışmaya devam etmenizi engellemez.</span><span class="sxs-lookup"><span data-stu-id="53070-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="53070-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="53070-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="53070-145">Yeni bir ER modeli eşleme yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="53070-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="53070-146">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="53070-147">Yeni alanına, 'Ödemeler modeli (hayali) veri modelini temel alan Model Eşleme' yazın.</span><span class="sxs-lookup"><span data-stu-id="53070-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="53070-148">İsim alanında, 'Ödeme modeli eşlemeleri (hayali)' yazın.</span><span class="sxs-lookup"><span data-stu-id="53070-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="53070-149">Ödeme modeli eşlemeleri (hayali)</span><span class="sxs-lookup"><span data-stu-id="53070-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="53070-150">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="53070-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="53070-151">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="53070-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="53070-152">ER model eşlemeleri tasarlayın</span><span class="sxs-lookup"><span data-stu-id="53070-152">Design ER model mappings</span></span>
1. <span data-ttu-id="53070-153">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="53070-153">Click Designer.</span></span>
    * <span data-ttu-id="53070-154">Gerekli kök maddeleri için model eşlemelerini belirtmek için ER tasarımcısını kullanın.</span><span class="sxs-lookup"><span data-stu-id="53070-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="53070-155">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="53070-155">Click Designer.</span></span>
    * <span data-ttu-id="53070-156">Seçilen modelin kök maddesi için seçilen model eşlemesinin ayarının benzetimini yapın.</span><span class="sxs-lookup"><span data-stu-id="53070-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="53070-157">Ağaçta, 'Dynamics 365 for Operations\Tablo kayıtları' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="53070-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="53070-158">Kök ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-158">Click Add root.</span></span>
5. <span data-ttu-id="53070-159">Ad alanına 'Genel muhasebe defteri' yazın.</span><span class="sxs-lookup"><span data-stu-id="53070-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="53070-160">Tablo alanına 'LedgerJournalTrans' yazın.</span><span class="sxs-lookup"><span data-stu-id="53070-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="53070-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="53070-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="53070-162">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-162">Click OK.</span></span>
8. <span data-ttu-id="53070-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-163">Click Save.</span></span>
9. <span data-ttu-id="53070-164">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="53070-164">Close the page.</span></span>
10. <span data-ttu-id="53070-165">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="53070-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="53070-166">Başka bir ER biçimi yapılandırması girmeye başlayın</span><span class="sxs-lookup"><span data-stu-id="53070-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="53070-167">Ağaçta 'Ödeme modeli (hayali)' seçin.</span><span class="sxs-lookup"><span data-stu-id="53070-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="53070-168">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53070-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="53070-169">Yeni alanına, 'Ödemeler modeli (hayali) veri modelini temel alan biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="53070-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="53070-170">Veri modeli tanımı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="53070-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="53070-171">Şimdi uygulama veri kaynaklarına yalnızca bir kök maddenin kullanılabilir olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="53070-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="53070-172">En az bir model eşlemesi eklendiğinde, yalnızca uygulama veri kaynaklarına eşleşmiş olan modelin kök maddelerinin bir ER biçimi eklendiğinde bir model tanımı olarak seçilebileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="53070-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="53070-173">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="53070-173">Close the page.</span></span>

