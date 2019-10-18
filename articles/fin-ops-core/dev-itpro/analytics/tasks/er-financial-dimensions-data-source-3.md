---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3 - Raporu tasarlama)
description: Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 29dcf008f342603615241ab75860893cadc2b69e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182451"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a><span data-ttu-id="36018-103">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 3: Raporu tasarlama)</span><span class="sxs-lookup"><span data-stu-id="36018-103">ER Use financial dimensions as a data source (Part 3: Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36018-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="36018-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="36018-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="36018-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="36018-106">Bu adımları tamamlamak için öncelikle "ER Mali boyutları veri kaynağı olarak kullanma (Bölüm 2: Model eşleme)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="36018-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="36018-107">Mali boyutları sunmak üzere bir rapor tasarlama</span><span class="sxs-lookup"><span data-stu-id="36018-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="36018-108">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="36018-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="36018-109">Ağaçta, 'Mali boyutlar örnek modeli' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="36018-110">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="36018-111">Yeni alanına, 'Mali boyutlar örnek modeli veri modeline dayalı biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="36018-112">Önceden oluşturulan modeli, yeni raporunuz için veri kaynağı olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="36018-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="36018-113">Ad alanına, 'Genel muhasebe günlüğü raporu' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="36018-114">Veri modeli tanımı alanında Giriş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="36018-115">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-115">Click Create configuration.</span></span>
8. <span data-ttu-id="36018-116">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-116">Click Designer.</span></span>
9. <span data-ttu-id="36018-117">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="36018-118">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="36018-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="36018-119">Ad alanına 'Kök' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="36018-120">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-120">Click OK.</span></span>
13. <span data-ttu-id="36018-121">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="36018-122">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="36018-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="36018-123">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="36018-124">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-124">Click OK.</span></span>
17. <span data-ttu-id="36018-125">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="36018-126">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="36018-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="36018-127">Ad alanına 'Günlük' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="36018-128">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-128">Click OK.</span></span>
21. <span data-ttu-id="36018-129">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="36018-130">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="36018-131">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="36018-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="36018-132">Ad alanına, 'Toplu İş' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="36018-133">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-133">Click OK.</span></span>
26. <span data-ttu-id="36018-134">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="36018-135">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="36018-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="36018-136">Ad alanına 'Hareket' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="36018-137">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-137">Click OK.</span></span>
30. <span data-ttu-id="36018-138">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="36018-139">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="36018-140">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="36018-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="36018-141">Ad alanına 'Fiş' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="36018-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-142">Click OK.</span></span>
35. <span data-ttu-id="36018-143">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="36018-144">Ad alanına 'Tarih' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="36018-145">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-145">Click OK.</span></span>
38. <span data-ttu-id="36018-146">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="36018-147">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="36018-148">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-148">Click OK.</span></span>
41. <span data-ttu-id="36018-149">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="36018-150">Ad alanına, 'Borç' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="36018-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-151">Click OK.</span></span>
44. <span data-ttu-id="36018-152">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="36018-153">Ad alanına, 'Alacak' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="36018-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-154">Click OK.</span></span>
47. <span data-ttu-id="36018-155">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="36018-156">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="36018-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="36018-157">Ad alanına, 'Boyutlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="36018-158">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-158">Click OK.</span></span>
51. <span data-ttu-id="36018-159">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="36018-160">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="36018-161">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="36018-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="36018-162">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="36018-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-163">Click OK.</span></span>
56. <span data-ttu-id="36018-164">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="36018-165">Ad alanına, 'Değer' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="36018-166">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-166">Click OK.</span></span>
59. <span data-ttu-id="36018-167">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="36018-168">Ad alanına, 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="36018-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="36018-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="36018-170">Rapor öğelerini veri kaynakları ile eşleme</span><span class="sxs-lookup"><span data-stu-id="36018-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="36018-171">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="36018-172">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli' öğesini genişletin</span><span class="sxs-lookup"><span data-stu-id="36018-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="36018-173">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="36018-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="36018-174">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="36018-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="36018-175">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="36018-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="36018-176">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Açıklama: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="36018-177">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kaynak listesi\Açıklama: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="36018-178">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-178">Click Bind.</span></span>
9. <span data-ttu-id="36018-179">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Değer: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="36018-180">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Kod: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="36018-181">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-181">Click Bind.</span></span>
12. <span data-ttu-id="36018-182">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Kod: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="36018-183">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Ad: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="36018-184">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-184">Click Bind.</span></span>
15. <span data-ttu-id="36018-185">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="36018-186">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="36018-187">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-187">Click Bind.</span></span>
18. <span data-ttu-id="36018-188">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Alacak: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="36018-189">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Alacak: Gerçek' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="36018-190">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-190">Click Bind.</span></span>
21. <span data-ttu-id="36018-191">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Borç: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="36018-192">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Borç: Gerçek' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="36018-193">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-193">Click Bind.</span></span>
24. <span data-ttu-id="36018-194">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Para Birimi: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="36018-195">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Para Birimi: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="36018-196">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-196">Click Bind.</span></span>
27. <span data-ttu-id="36018-197">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Tarih: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="36018-198">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Tarih: Tarih' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="36018-199">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-199">Click Bind.</span></span>
30. <span data-ttu-id="36018-200">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Fiş: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="36018-201">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Fiş: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="36018-202">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-202">Click Bind.</span></span>
33. <span data-ttu-id="36018-203">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="36018-204">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="36018-205">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-205">Click Bind.</span></span>
36. <span data-ttu-id="36018-206">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Toplu İş: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="36018-207">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Toplu İş: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="36018-208">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-208">Click Bind.</span></span>
39. <span data-ttu-id="36018-209">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="36018-210">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="36018-211">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="36018-211">Click Bind.</span></span>
42. <span data-ttu-id="36018-212">Ağaçta, 'Kök: XML Öğesi\Şirket: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="36018-213">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Şirket: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="36018-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="36018-214">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-214">Click Bind.</span></span>
45. <span data-ttu-id="36018-215">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="36018-215">Click Save.</span></span>
46. <span data-ttu-id="36018-216">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="36018-216">Close the page.</span></span>

