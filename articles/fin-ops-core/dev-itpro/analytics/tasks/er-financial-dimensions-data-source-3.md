---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3 - Raporu tasarlama)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a12f88f1e8b5e451bc8a5c5486d820da61bf3ad0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684799"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="c95d8-103">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3 - Raporu tasarlama)</span><span class="sxs-lookup"><span data-stu-id="c95d8-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c95d8-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="c95d8-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="c95d8-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c95d8-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="c95d8-106">Bu adımları tamamlamak için öncelikle "ER Mali boyutları veri kaynağı olarak kullanma (Bölüm 2: Model eşleme)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c95d8-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="c95d8-107">Mali boyutları sunmak üzere bir rapor tasarlama</span><span class="sxs-lookup"><span data-stu-id="c95d8-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="c95d8-108">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="c95d8-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="c95d8-109">Ağaçta, 'Mali boyutlar örnek modeli' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c95d8-110">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="c95d8-111">Yeni alanına, 'Mali boyutlar örnek modeli veri modeline dayalı biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="c95d8-112">Önceden oluşturulan modeli, yeni raporunuz için veri kaynağı olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="c95d8-113">Ad alanına, 'Genel muhasebe günlüğü raporu' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="c95d8-114">Veri modeli tanımı alanında Giriş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="c95d8-115">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-115">Click Create configuration.</span></span>
8. <span data-ttu-id="c95d8-116">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-116">Click Designer.</span></span>
9. <span data-ttu-id="c95d8-117">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="c95d8-118">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="c95d8-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="c95d8-119">Ad alanına 'Kök' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="c95d8-120">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-120">Click OK.</span></span>
13. <span data-ttu-id="c95d8-121">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="c95d8-122">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="c95d8-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="c95d8-123">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="c95d8-124">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-124">Click OK.</span></span>
17. <span data-ttu-id="c95d8-125">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="c95d8-126">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="c95d8-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="c95d8-127">Ad alanına 'Günlük' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="c95d8-128">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-128">Click OK.</span></span>
21. <span data-ttu-id="c95d8-129">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="c95d8-130">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="c95d8-131">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="c95d8-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="c95d8-132">Ad alanına, 'Toplu İş' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="c95d8-133">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-133">Click OK.</span></span>
26. <span data-ttu-id="c95d8-134">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="c95d8-135">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="c95d8-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="c95d8-136">Ad alanına 'Hareket' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="c95d8-137">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-137">Click OK.</span></span>
30. <span data-ttu-id="c95d8-138">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="c95d8-139">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="c95d8-140">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="c95d8-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="c95d8-141">Ad alanına 'Fiş' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="c95d8-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-142">Click OK.</span></span>
35. <span data-ttu-id="c95d8-143">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="c95d8-144">Ad alanına 'Tarih' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="c95d8-145">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-145">Click OK.</span></span>
38. <span data-ttu-id="c95d8-146">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="c95d8-147">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="c95d8-148">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-148">Click OK.</span></span>
41. <span data-ttu-id="c95d8-149">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="c95d8-150">Ad alanına, 'Borç' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="c95d8-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-151">Click OK.</span></span>
44. <span data-ttu-id="c95d8-152">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="c95d8-153">Ad alanına, 'Alacak' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="c95d8-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-154">Click OK.</span></span>
47. <span data-ttu-id="c95d8-155">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="c95d8-156">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="c95d8-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="c95d8-157">Ad alanına, 'Boyutlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="c95d8-158">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-158">Click OK.</span></span>
51. <span data-ttu-id="c95d8-159">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="c95d8-160">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="c95d8-161">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="c95d8-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="c95d8-162">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="c95d8-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-163">Click OK.</span></span>
56. <span data-ttu-id="c95d8-164">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="c95d8-165">Ad alanına, 'Değer' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="c95d8-166">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-166">Click OK.</span></span>
59. <span data-ttu-id="c95d8-167">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="c95d8-168">Ad alanına, 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="c95d8-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-169">Click OK.</span></span>
<span data-ttu-id="c95d8-170">![ER İşlem tasarımcısı sayfası](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="c95d8-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="c95d8-171">Rapor öğelerini veri kaynakları ile eşleme</span><span class="sxs-lookup"><span data-stu-id="c95d8-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="c95d8-172">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="c95d8-173">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli' öğesini genişletin</span><span class="sxs-lookup"><span data-stu-id="c95d8-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="c95d8-174">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="c95d8-175">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="c95d8-176">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="c95d8-177">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Açıklama: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="c95d8-178">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kaynak listesi\Açıklama: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="c95d8-179">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-179">Click Bind.</span></span>
9. <span data-ttu-id="c95d8-180">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Değer: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="c95d8-181">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Kod: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="c95d8-182">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-182">Click Bind.</span></span>
12. <span data-ttu-id="c95d8-183">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Kod: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="c95d8-184">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Ad: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="c95d8-185">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-185">Click Bind.</span></span>
15. <span data-ttu-id="c95d8-186">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="c95d8-187">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="c95d8-188">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-188">Click Bind.</span></span>
18. <span data-ttu-id="c95d8-189">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Alacak: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="c95d8-190">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Alacak: Gerçek' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="c95d8-191">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-191">Click Bind.</span></span>
21. <span data-ttu-id="c95d8-192">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Borç: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="c95d8-193">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Borç: Gerçek' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="c95d8-194">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-194">Click Bind.</span></span>
24. <span data-ttu-id="c95d8-195">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Para Birimi: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="c95d8-196">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Para Birimi: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="c95d8-197">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-197">Click Bind.</span></span>
27. <span data-ttu-id="c95d8-198">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Tarih: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="c95d8-199">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Tarih: Tarih' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="c95d8-200">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-200">Click Bind.</span></span>
30. <span data-ttu-id="c95d8-201">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Fiş: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="c95d8-202">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Fiş: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="c95d8-203">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-203">Click Bind.</span></span>
33. <span data-ttu-id="c95d8-204">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="c95d8-205">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="c95d8-206">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-206">Click Bind.</span></span>
36. <span data-ttu-id="c95d8-207">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Toplu İş: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="c95d8-208">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Toplu İş: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="c95d8-209">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-209">Click Bind.</span></span>
39. <span data-ttu-id="c95d8-210">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="c95d8-211">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="c95d8-212">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-212">Click Bind.</span></span>
42. <span data-ttu-id="c95d8-213">Ağaçta, 'Kök: XML Öğesi\Şirket: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="c95d8-214">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Şirket: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="c95d8-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="c95d8-215">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-215">Click Bind.</span></span>
45. <span data-ttu-id="c95d8-216">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-216">Click Save.</span></span>
46. <span data-ttu-id="c95d8-217">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c95d8-217">Close the page.</span></span>
<span data-ttu-id="c95d8-218">![ER İşlem tasarımcısı sayfası](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="c95d8-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

