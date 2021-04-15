---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 1 - Veri modeli tasarlama)
description: Bu konuda, ER raporları için veri kaynağı olarak mali boyutları kullanmak üzere Elektronik raporlama (ER) modelinin nasıl yapılandırılacağı açıklanmaktadır. (1. Bölüm)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92b44532dfae70f03d6686ca1d2f8b6f74345ee6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752472"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="b4082-104">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 1 - Veri modeli tasarlama)</span><span class="sxs-lookup"><span data-stu-id="b4082-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4082-105">Aşağıdaki adımlar, bir sistem yöneticisinin veya elektronik raporlama geliştiricisinin bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="b4082-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="b4082-106">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="b4082-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="b4082-107">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4082-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="b4082-108">Yeni bir veri modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4082-108">Create a new data model</span></span>
1. <span data-ttu-id="b4082-109">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b4082-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="b4082-110">"Litware, Inc." emin olun</span><span class="sxs-lookup"><span data-stu-id="b4082-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="b4082-111">sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="b4082-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="b4082-112">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b4082-113">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="b4082-114">Ad alanına 'Mali boyutlar örnek modeli' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="b4082-115">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-115">Click Create configuration.</span></span>
6. <span data-ttu-id="b4082-116">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-116">Click Designer.</span></span>
7. <span data-ttu-id="b4082-117">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b4082-118">Ad alanına 'Giriş' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="b4082-119">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-119">Click Add.</span></span>
10. <span data-ttu-id="b4082-120">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="b4082-121">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="b4082-122">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-122">Click Add.</span></span>
    * <span data-ttu-id="b4082-123">Modelimize yeni bir kayıt listesi ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="b4082-123">We will add to our model a new record list.</span></span> <span data-ttu-id="b4082-124">Bu liste (bu modeli veri kaynağı olarak kullanan tüm ER raporları için) seçili mali boyutların ayarlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4082-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="b4082-125">Tüm mali boyutlar bu listede boyutun ayarını temsil eden uygun alanlarla birlikte bir kayıt olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="b4082-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="b4082-126">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="b4082-127">Ad alanına 'Boyutlar ayarı' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="b4082-128">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="b4082-129">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-129">Click Add.</span></span>
17. <span data-ttu-id="b4082-130">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="b4082-131">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="b4082-132">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="b4082-133">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-133">Click Add.</span></span>
21. <span data-ttu-id="b4082-134">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="b4082-135">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="b4082-136">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-136">Click Add.</span></span>
24. <span data-ttu-id="b4082-137">Ağaçta, 'Giriş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="b4082-138">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="b4082-139">Ad alanına 'Günlük' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="b4082-140">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="b4082-141">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-141">Click Add.</span></span>
29. <span data-ttu-id="b4082-142">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="b4082-143">Ad alanına, 'Toplu İş' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="b4082-144">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="b4082-145">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-145">Click Add.</span></span>
33. <span data-ttu-id="b4082-146">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="b4082-147">Ad alanına 'Hareket' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="b4082-148">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="b4082-149">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-149">Click Add.</span></span>
37. <span data-ttu-id="b4082-150">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="b4082-151">Ad alanına 'Tarih' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="b4082-152">Madde türü alanında 'Tarih' seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="b4082-153">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-153">Click Add.</span></span>
41. <span data-ttu-id="b4082-154">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="b4082-155">Ad alanına 'Borç' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="b4082-156">Madde türü alanında 'Gerçek' seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="b4082-157">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-157">Click Add.</span></span>
45. <span data-ttu-id="b4082-158">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="b4082-159">Ad alanına 'Alacak' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="b4082-160">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-160">Click Add.</span></span>
48. <span data-ttu-id="b4082-161">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="b4082-162">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="b4082-163">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="b4082-164">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-164">Click Add.</span></span>
52. <span data-ttu-id="b4082-165">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="b4082-166">Ad alanına 'Fiş' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="b4082-167">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-167">Click Add.</span></span>
55. <span data-ttu-id="b4082-168">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="b4082-169">Ad alanına 'Boyut verileri' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="b4082-170">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="b4082-171">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-171">Click Add.</span></span>
    * <span data-ttu-id="b4082-172">Modelimize yeni bir kayıt listesi ekledik.</span><span class="sxs-lookup"><span data-stu-id="b4082-172">We added to our model a new record list.</span></span> <span data-ttu-id="b4082-173">Bu liste (bu modeli veri kaynağı olarak kullanan tüm ER raporları için) seçili mali boyutların değerlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4082-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="b4082-174">Tüm mali boyutlar bu listede boyutun değerlerini temsil eden uygun alanlarla birlikte bir kayıt olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="b4082-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="b4082-175">Boyut adı da bu kayıtta gerekirse seçim amacıyla kullanılmak üzere bir alan olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="b4082-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="b4082-176">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="b4082-177">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="b4082-178">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="b4082-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="b4082-179">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-179">Click Add.</span></span>
63. <span data-ttu-id="b4082-180">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="b4082-181">İsim alanına 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="b4082-182">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-182">Click Add.</span></span>
66. <span data-ttu-id="b4082-183">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="b4082-184">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="b4082-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="b4082-185">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="b4082-185">Click Add.</span></span>
69. <span data-ttu-id="b4082-186">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-186">Click Save.</span></span>
70. <span data-ttu-id="b4082-187">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="b4082-187">Close the page.</span></span>

![ER veri modeli tasarımcısı sayfası](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]