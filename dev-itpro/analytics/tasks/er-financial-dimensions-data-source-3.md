--- 
title: "Elektronik raporlama (ER) için mali boyutları veri kaynağı olarak kullanmak üzere bir rapor tasarlama"
description: "Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 02787c96077e8bae54d8073e8d0770613ea2b49a
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="56a1e-103">Elektronik raporlama (ER) için mali boyutları veri kaynağı olarak kullanmak üzere bir rapor tasarlama</span><span class="sxs-lookup"><span data-stu-id="56a1e-103">Design a report to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56a1e-104">Aşağıdaki adımlar, bir sistem yöneticisi veya elektronik raporlama geliştiricisi rolü atanan bir kullanıcının bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="56a1e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="56a1e-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="56a1e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="56a1e-106">Bu adımları tamamlamak için öncelikle "ER Mali boyutları veri kaynağı olarak kullanma (Bölüm 2: Model eşleme)" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="56a1e-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="56a1e-107">Mali boyutları sunmak üzere bir rapor tasarlama</span><span class="sxs-lookup"><span data-stu-id="56a1e-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="56a1e-108">Kuruluş yönetimi > Elektronik raporlama > Yapılandırmalar seçeneğine git.</span><span class="sxs-lookup"><span data-stu-id="56a1e-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="56a1e-109">Ağaçta, 'Mali boyutlar örnek modeli' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="56a1e-110">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="56a1e-111">Yeni alanına, 'Mali boyutlar örnek modeli veri modeline dayalı biçim' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="56a1e-112">Önceden oluşturulan modeli, yeni raporunuz için veri kaynağı olarak kullanın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="56a1e-113">Ad alanına, 'Genel muhasebe günlüğü raporu' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="56a1e-114">Veri modeli tanımı alanında Giriş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="56a1e-115">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-115">Click Create configuration.</span></span>
8. <span data-ttu-id="56a1e-116">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-116">Click Designer.</span></span>
9. <span data-ttu-id="56a1e-117">İletişim kutusunu açmak için Kök ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="56a1e-118">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="56a1e-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="56a1e-119">Ad alanına 'Kök' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="56a1e-120">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-120">Click OK.</span></span>
13. <span data-ttu-id="56a1e-121">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="56a1e-122">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="56a1e-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="56a1e-123">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="56a1e-124">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-124">Click OK.</span></span>
17. <span data-ttu-id="56a1e-125">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="56a1e-126">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="56a1e-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="56a1e-127">Ad alanına 'Günlük' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="56a1e-128">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-128">Click OK.</span></span>
21. <span data-ttu-id="56a1e-129">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="56a1e-130">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="56a1e-131">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="56a1e-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="56a1e-132">Ad alanına, 'Toplu İş' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="56a1e-133">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-133">Click OK.</span></span>
26. <span data-ttu-id="56a1e-134">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="56a1e-135">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="56a1e-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="56a1e-136">Ad alanına 'Hareket' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="56a1e-137">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-137">Click OK.</span></span>
30. <span data-ttu-id="56a1e-138">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="56a1e-139">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="56a1e-140">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="56a1e-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="56a1e-141">Ad alanına 'Fiş' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="56a1e-142">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-142">Click OK.</span></span>
35. <span data-ttu-id="56a1e-143">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="56a1e-144">Ad alanına 'Tarih' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="56a1e-145">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-145">Click OK.</span></span>
38. <span data-ttu-id="56a1e-146">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="56a1e-147">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="56a1e-148">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-148">Click OK.</span></span>
41. <span data-ttu-id="56a1e-149">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="56a1e-150">Ad alanına, 'Borç' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="56a1e-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-151">Click OK.</span></span>
44. <span data-ttu-id="56a1e-152">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="56a1e-153">Ad alanına, 'Alacak' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="56a1e-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-154">Click OK.</span></span>
47. <span data-ttu-id="56a1e-155">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="56a1e-156">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="56a1e-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="56a1e-157">Ad alanına, 'Boyutlar' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="56a1e-158">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-158">Click OK.</span></span>
51. <span data-ttu-id="56a1e-159">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="56a1e-160">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="56a1e-161">Ağaçta seçin 'XML\Attribute'.</span><span class="sxs-lookup"><span data-stu-id="56a1e-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="56a1e-162">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="56a1e-163">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-163">Click OK.</span></span>
56. <span data-ttu-id="56a1e-164">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="56a1e-165">Ad alanına, 'Değer' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="56a1e-166">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-166">Click OK.</span></span>
59. <span data-ttu-id="56a1e-167">Öznitelik Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="56a1e-168">Ad alanına, 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="56a1e-169">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="56a1e-170">Rapor öğelerini veri kaynakları ile eşleme</span><span class="sxs-lookup"><span data-stu-id="56a1e-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="56a1e-171">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="56a1e-172">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli' öğesini genişletin</span><span class="sxs-lookup"><span data-stu-id="56a1e-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="56a1e-173">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="56a1e-174">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="56a1e-175">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="56a1e-176">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Açıklama: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="56a1e-177">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kaynak listesi\Açıklama: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="56a1e-178">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-178">Click Bind.</span></span>
9. <span data-ttu-id="56a1e-179">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Değer: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="56a1e-180">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Kod: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="56a1e-181">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-181">Click Bind.</span></span>
12. <span data-ttu-id="56a1e-182">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi\Kod: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="56a1e-183">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi\Ad: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="56a1e-184">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-184">Click Bind.</span></span>
15. <span data-ttu-id="56a1e-185">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Boyut verileri: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="56a1e-186">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Boyutlar: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="56a1e-187">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-187">Click Bind.</span></span>
18. <span data-ttu-id="56a1e-188">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Alacak: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="56a1e-189">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Alacak: Gerçek' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="56a1e-190">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-190">Click Bind.</span></span>
21. <span data-ttu-id="56a1e-191">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Borç: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="56a1e-192">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Borç: Gerçek' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="56a1e-193">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-193">Click Bind.</span></span>
24. <span data-ttu-id="56a1e-194">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Para Birimi: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="56a1e-195">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Para Birimi: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="56a1e-196">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-196">Click Bind.</span></span>
27. <span data-ttu-id="56a1e-197">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Tarih: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="56a1e-198">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Tarih: Tarih' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="56a1e-199">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-199">Click Bind.</span></span>
30. <span data-ttu-id="56a1e-200">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi\Fiş: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="56a1e-201">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi\Fiş: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="56a1e-202">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-202">Click Bind.</span></span>
33. <span data-ttu-id="56a1e-203">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Hareket: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="56a1e-204">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Hareket: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="56a1e-205">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-205">Click Bind.</span></span>
36. <span data-ttu-id="56a1e-206">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi\Toplu İş: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="56a1e-207">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi\Toplu İş: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="56a1e-208">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-208">Click Bind.</span></span>
39. <span data-ttu-id="56a1e-209">Ağaçta, 'Kök: XML Öğesi\Günlük: XML Öğesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="56a1e-210">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Günlük: Kayıt listesi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="56a1e-211">Bağla'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-211">Click Bind.</span></span>
42. <span data-ttu-id="56a1e-212">Ağaçta, 'Kök: XML Öğesi\Şirket: XML Özniteliği' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="56a1e-213">Ağaçta, 'model: Veri modeli Mali boyutlar örnek modeli\Şirket: Dize' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="56a1e-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="56a1e-214">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-214">Click Bind.</span></span>
45. <span data-ttu-id="56a1e-215">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-215">Click Save.</span></span>
46. <span data-ttu-id="56a1e-216">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="56a1e-216">Close the page.</span></span>


