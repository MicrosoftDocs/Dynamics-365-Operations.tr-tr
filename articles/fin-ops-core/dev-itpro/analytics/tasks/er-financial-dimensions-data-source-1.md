---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 1 - Veri modeli tasarlama)
description: Aşağıdaki adımlar, bir sistem yöneticisinin veya elektronik raporlama geliştiricisinin bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b02496ebb06e0c2eb644fc7ef3280ca4eca05923
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142052"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="e059b-103">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 1 - Veri modeli tasarlama)</span><span class="sxs-lookup"><span data-stu-id="e059b-103">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e059b-104">Aşağıdaki adımlar, bir sistem yöneticisinin veya elektronik raporlama geliştiricisinin bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="e059b-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="e059b-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="e059b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="e059b-106">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e059b-106">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="e059b-107">Yeni bir veri modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="e059b-107">Create a new data model</span></span>
1. <span data-ttu-id="e059b-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="e059b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e059b-109">"Litware, Inc." emin olun</span><span class="sxs-lookup"><span data-stu-id="e059b-109">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="e059b-110">sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="e059b-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="e059b-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e059b-112">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="e059b-113">Ad alanına 'Mali boyutlar örnek modeli' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="e059b-114">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-114">Click Create configuration.</span></span>
6. <span data-ttu-id="e059b-115">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-115">Click Designer.</span></span>
7. <span data-ttu-id="e059b-116">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e059b-117">Ad alanına 'Giriş' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="e059b-118">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-118">Click Add.</span></span>
10. <span data-ttu-id="e059b-119">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="e059b-120">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="e059b-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-121">Click Add.</span></span>
    * <span data-ttu-id="e059b-122">Modelimize yeni bir kayıt listesi ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="e059b-122">We will add to our model a new record list.</span></span> <span data-ttu-id="e059b-123">Bu liste (bu modeli veri kaynağı olarak kullanan tüm ER raporları için) seçili mali boyutların ayarlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e059b-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="e059b-124">Tüm mali boyutlar bu listede boyutun ayarını temsil eden uygun alanlarla birlikte bir kayıt olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="e059b-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="e059b-125">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="e059b-126">Ad alanına 'Boyutlar ayarı' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="e059b-127">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="e059b-128">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-128">Click Add.</span></span>
17. <span data-ttu-id="e059b-129">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="e059b-130">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="e059b-131">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="e059b-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-132">Click Add.</span></span>
21. <span data-ttu-id="e059b-133">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="e059b-134">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="e059b-135">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-135">Click Add.</span></span>
24. <span data-ttu-id="e059b-136">Ağaçta, 'Giriş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="e059b-137">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="e059b-138">Ad alanına 'Günlük' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="e059b-139">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="e059b-140">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-140">Click Add.</span></span>
29. <span data-ttu-id="e059b-141">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="e059b-142">Ad alanına, 'Toplu İş' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="e059b-143">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="e059b-144">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-144">Click Add.</span></span>
33. <span data-ttu-id="e059b-145">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="e059b-146">Ad alanına 'Hareket' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="e059b-147">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="e059b-148">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-148">Click Add.</span></span>
37. <span data-ttu-id="e059b-149">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="e059b-150">Ad alanına 'Tarih' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="e059b-151">Madde türü alanında 'Tarih' seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="e059b-152">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-152">Click Add.</span></span>
41. <span data-ttu-id="e059b-153">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="e059b-154">Ad alanına 'Borç' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="e059b-155">Madde türü alanında 'Gerçek' seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="e059b-156">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-156">Click Add.</span></span>
45. <span data-ttu-id="e059b-157">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="e059b-158">Ad alanına 'Alacak' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="e059b-159">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-159">Click Add.</span></span>
48. <span data-ttu-id="e059b-160">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="e059b-161">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="e059b-162">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="e059b-163">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-163">Click Add.</span></span>
52. <span data-ttu-id="e059b-164">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="e059b-165">Ad alanına 'Fiş' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="e059b-166">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-166">Click Add.</span></span>
55. <span data-ttu-id="e059b-167">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="e059b-168">Ad alanına 'Boyut verileri' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="e059b-169">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="e059b-170">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-170">Click Add.</span></span>
    * <span data-ttu-id="e059b-171">Modelimize yeni bir kayıt listesi ekledik.</span><span class="sxs-lookup"><span data-stu-id="e059b-171">We added to our model a new record list.</span></span> <span data-ttu-id="e059b-172">Bu liste (bu modeli veri kaynağı olarak kullanan tüm ER raporları için) seçili mali boyutların değerlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e059b-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="e059b-173">Tüm mali boyutlar bu listede boyutun değerlerini temsil eden uygun alanlarla birlikte bir kayıt olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="e059b-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="e059b-174">Boyut adı da bu kayıtta gerekirse seçim amacıyla kullanılmak üzere bir alan olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="e059b-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="e059b-175">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="e059b-176">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="e059b-177">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="e059b-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="e059b-178">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-178">Click Add.</span></span>
63. <span data-ttu-id="e059b-179">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="e059b-180">İsim alanına 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="e059b-181">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-181">Click Add.</span></span>
66. <span data-ttu-id="e059b-182">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="e059b-183">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="e059b-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="e059b-184">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-184">Click Add.</span></span>
69. <span data-ttu-id="e059b-185">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e059b-185">Click Save.</span></span>
70. <span data-ttu-id="e059b-186">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e059b-186">Close the page.</span></span>

