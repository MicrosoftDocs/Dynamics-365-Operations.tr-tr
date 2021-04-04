---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3 - Raporu tasarlama)
description: Bu konuda, ER raporları için veri kaynağı olarak mali boyutları kullanmak üzere Elektronik raporlama (ER) modelinin nasıl yapılandırılacağı açıklanmaktadır. (3. Bölüm)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565250"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="4b20b-104">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3 - Raporu tasarlama)</span><span class="sxs-lookup"><span data-stu-id="4b20b-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b20b-105">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="4b20b-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="4b20b-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="4b20b-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="4b20b-107">Bu adımları tamamlamak için öncelikle "ER Mali boyutları veri kaynağı olarak kullanma (Bölüm 2: Model eşleme)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4b20b-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="4b20b-108">Mali boyutları sunmak üzere bir rapor tasarlama</span><span class="sxs-lookup"><span data-stu-id="4b20b-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="4b20b-109">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="4b20b-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4b20b-110">Ağaçta, 'Mali boyutlar örnek modeli' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="4b20b-111">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="4b20b-112">Yeni alanına, 'Mali boyutlar örnek modeli veri modeline dayalı biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="4b20b-113">Önceden oluşturulan modeli, yeni raporunuz için veri kaynağı olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="4b20b-114">Ad alanına, 'Genel muhasebe günlüğü raporu' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="4b20b-115">Veri modeli tanımı alanında Giriş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="4b20b-116">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-116">Click Create configuration.</span></span>
8. <span data-ttu-id="4b20b-117">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-117">Click Designer.</span></span>
9. <span data-ttu-id="4b20b-118">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="4b20b-119">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="4b20b-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="4b20b-120">Ad alanına 'Kök' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="4b20b-121">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-121">Click OK.</span></span>
13. <span data-ttu-id="4b20b-122">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="4b20b-123">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="4b20b-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="4b20b-124">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="4b20b-125">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-125">Click OK.</span></span>
17. <span data-ttu-id="4b20b-126">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="4b20b-127">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="4b20b-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="4b20b-128">Ad alanına 'Günlük' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="4b20b-129">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-129">Click OK.</span></span>
21. <span data-ttu-id="4b20b-130">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="4b20b-131">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="4b20b-132">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="4b20b-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="4b20b-133">Ad alanına, 'Toplu İş' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="4b20b-134">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-134">Click OK.</span></span>
26. <span data-ttu-id="4b20b-135">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="4b20b-136">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="4b20b-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="4b20b-137">Ad alanına 'Hareket' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="4b20b-138">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-138">Click OK.</span></span>
30. <span data-ttu-id="4b20b-139">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="4b20b-140">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="4b20b-141">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="4b20b-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="4b20b-142">Ad alanına 'Fiş' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="4b20b-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-143">Click OK.</span></span>
35. <span data-ttu-id="4b20b-144">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="4b20b-145">Ad alanına 'Tarih' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="4b20b-146">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-146">Click OK.</span></span>
38. <span data-ttu-id="4b20b-147">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="4b20b-148">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="4b20b-149">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-149">Click OK.</span></span>
41. <span data-ttu-id="4b20b-150">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="4b20b-151">Ad alanına, 'Borç' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="4b20b-152">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-152">Click OK.</span></span>
44. <span data-ttu-id="4b20b-153">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="4b20b-154">Ad alanına, 'Alacak' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="4b20b-155">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-155">Click OK.</span></span>
47. <span data-ttu-id="4b20b-156">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="4b20b-157">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="4b20b-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="4b20b-158">Ad alanına, 'Boyutlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="4b20b-159">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-159">Click OK.</span></span>
51. <span data-ttu-id="4b20b-160">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="4b20b-161">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="4b20b-162">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="4b20b-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="4b20b-163">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="4b20b-164">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-164">Click OK.</span></span>
56. <span data-ttu-id="4b20b-165">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="4b20b-166">Ad alanına, 'Değer' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="4b20b-167">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-167">Click OK.</span></span>
59. <span data-ttu-id="4b20b-168">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="4b20b-169">Ad alanına, 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="4b20b-170">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-170">Click OK.</span></span>
<span data-ttu-id="4b20b-171">![ER İşlem tasarımcısı sayfası](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="4b20b-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="4b20b-172">Rapor öğelerini veri kaynakları ile eşleme</span><span class="sxs-lookup"><span data-stu-id="4b20b-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="4b20b-173">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="4b20b-174">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli' öğesini genişletin</span><span class="sxs-lookup"><span data-stu-id="4b20b-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="4b20b-175">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="4b20b-176">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="4b20b-177">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="4b20b-178">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Açıklama: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="4b20b-179">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kaynak listesi\Açıklama: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="4b20b-180">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-180">Click Bind.</span></span>
9. <span data-ttu-id="4b20b-181">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Değer: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="4b20b-182">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Kod: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="4b20b-183">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-183">Click Bind.</span></span>
12. <span data-ttu-id="4b20b-184">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Kod: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="4b20b-185">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Ad: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="4b20b-186">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-186">Click Bind.</span></span>
15. <span data-ttu-id="4b20b-187">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="4b20b-188">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="4b20b-189">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-189">Click Bind.</span></span>
18. <span data-ttu-id="4b20b-190">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Alacak: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="4b20b-191">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Alacak: Gerçek' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="4b20b-192">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-192">Click Bind.</span></span>
21. <span data-ttu-id="4b20b-193">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Borç: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="4b20b-194">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Borç: Gerçek' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="4b20b-195">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-195">Click Bind.</span></span>
24. <span data-ttu-id="4b20b-196">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Para Birimi: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="4b20b-197">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Para Birimi: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="4b20b-198">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-198">Click Bind.</span></span>
27. <span data-ttu-id="4b20b-199">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Tarih: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="4b20b-200">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Tarih: Tarih' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="4b20b-201">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-201">Click Bind.</span></span>
30. <span data-ttu-id="4b20b-202">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Fiş: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="4b20b-203">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Fiş: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="4b20b-204">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-204">Click Bind.</span></span>
33. <span data-ttu-id="4b20b-205">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="4b20b-206">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="4b20b-207">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-207">Click Bind.</span></span>
36. <span data-ttu-id="4b20b-208">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Toplu İş: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="4b20b-209">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Toplu İş: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="4b20b-210">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-210">Click Bind.</span></span>
39. <span data-ttu-id="4b20b-211">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="4b20b-212">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="4b20b-213">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-213">Click Bind.</span></span>
42. <span data-ttu-id="4b20b-214">Ağaçta, 'Kök: XML Öğesi\Şirket: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="4b20b-215">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Şirket: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4b20b-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="4b20b-216">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-216">Click Bind.</span></span>
45. <span data-ttu-id="4b20b-217">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-217">Click Save.</span></span>
46. <span data-ttu-id="4b20b-218">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4b20b-218">Close the page.</span></span>
<span data-ttu-id="4b20b-219">![ER İşlem tasarımcısı sayfası](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="4b20b-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]