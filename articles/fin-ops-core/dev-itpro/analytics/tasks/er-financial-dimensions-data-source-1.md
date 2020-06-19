---
title: ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 1 - Veri modeli tasarlama)
description: Aşağıdaki adımlar, bir sistem yöneticisinin veya elektronik raporlama geliştiricisinin bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
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
ms.openlocfilehash: b951c9074c68a9f7592c17e0688498880397b223
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406555"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="524b1-103">ER Mali boyutları bir veri kaynağı olarak kullanma (Bölüm 1 - Veri modeli tasarlama)</span><span class="sxs-lookup"><span data-stu-id="524b1-103">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="524b1-104">Aşağıdaki adımlar, bir sistem yöneticisinin veya elektronik raporlama geliştiricisinin bir Elektronik raporlama (ER) modelini ER raporları için veri kaynağı olarak mali boyutları kullanacak şekilde nasıl yapılandıracağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="524b1-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="524b1-105">Bu adımlar tüm şirketlerde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="524b1-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="524b1-106">Bu adımları tamamlamak için öncelikle "Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme" yordamındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="524b1-106">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="524b1-107">Yeni bir veri modeli oluşturma</span><span class="sxs-lookup"><span data-stu-id="524b1-107">Create a new data model</span></span>
1. <span data-ttu-id="524b1-108">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="524b1-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="524b1-109">"Litware, Inc." emin olun</span><span class="sxs-lookup"><span data-stu-id="524b1-109">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="524b1-110">sağlayıcısının kullanılabilir ve etkin olarak işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="524b1-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="524b1-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="524b1-112">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="524b1-113">Ad alanına 'Mali boyutlar örnek modeli' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="524b1-114">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-114">Click Create configuration.</span></span>
6. <span data-ttu-id="524b1-115">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-115">Click Designer.</span></span>
7. <span data-ttu-id="524b1-116">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="524b1-117">Ad alanına 'Giriş' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="524b1-118">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-118">Click Add.</span></span>
10. <span data-ttu-id="524b1-119">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="524b1-120">İsim alanına 'Şirket' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="524b1-121">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-121">Click Add.</span></span>
    * <span data-ttu-id="524b1-122">Modelimize yeni bir kayıt listesi ekleyeceğiz.</span><span class="sxs-lookup"><span data-stu-id="524b1-122">We will add to our model a new record list.</span></span> <span data-ttu-id="524b1-123">Bu liste (bu modeli veri kaynağı olarak kullanan tüm ER raporları için) seçili mali boyutların ayarlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="524b1-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="524b1-124">Tüm mali boyutlar bu listede boyutun ayarını temsil eden uygun alanlarla birlikte bir kayıt olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="524b1-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="524b1-125">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="524b1-126">Ad alanına 'Boyutlar ayarı' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="524b1-127">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="524b1-128">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-128">Click Add.</span></span>
17. <span data-ttu-id="524b1-129">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="524b1-130">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="524b1-131">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="524b1-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-132">Click Add.</span></span>
21. <span data-ttu-id="524b1-133">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="524b1-134">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="524b1-135">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-135">Click Add.</span></span>
24. <span data-ttu-id="524b1-136">Ağaçta, 'Giriş'i seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="524b1-137">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="524b1-138">Ad alanına 'Günlük' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="524b1-139">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="524b1-140">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-140">Click Add.</span></span>
29. <span data-ttu-id="524b1-141">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="524b1-142">Ad alanına, 'Toplu İş' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="524b1-143">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="524b1-144">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-144">Click Add.</span></span>
33. <span data-ttu-id="524b1-145">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="524b1-146">Ad alanına 'Hareket' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="524b1-147">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="524b1-148">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-148">Click Add.</span></span>
37. <span data-ttu-id="524b1-149">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="524b1-150">Ad alanına 'Tarih' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="524b1-151">Madde türü alanında 'Tarih' seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="524b1-152">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-152">Click Add.</span></span>
41. <span data-ttu-id="524b1-153">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="524b1-154">Ad alanına 'Borç' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="524b1-155">Madde türü alanında 'Gerçek' seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="524b1-156">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-156">Click Add.</span></span>
45. <span data-ttu-id="524b1-157">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="524b1-158">Ad alanına 'Alacak' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="524b1-159">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-159">Click Add.</span></span>
48. <span data-ttu-id="524b1-160">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="524b1-161">İsim alanına 'Para birimi' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="524b1-162">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="524b1-163">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-163">Click Add.</span></span>
52. <span data-ttu-id="524b1-164">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="524b1-165">Ad alanına 'Fiş' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="524b1-166">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-166">Click Add.</span></span>
55. <span data-ttu-id="524b1-167">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="524b1-168">Ad alanına 'Boyut verileri' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="524b1-169">Madde türü alanında 'Kayıt listesi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="524b1-170">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-170">Click Add.</span></span>
    * <span data-ttu-id="524b1-171">Modelimize yeni bir kayıt listesi ekledik.</span><span class="sxs-lookup"><span data-stu-id="524b1-171">We added to our model a new record list.</span></span> <span data-ttu-id="524b1-172">Bu liste (bu modeli veri kaynağı olarak kullanan tüm ER raporları için) seçili mali boyutların değerlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="524b1-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="524b1-173">Tüm mali boyutlar bu listede boyutun değerlerini temsil eden uygun alanlarla birlikte bir kayıt olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="524b1-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="524b1-174">Boyut adı da bu kayıtta gerekirse seçim amacıyla kullanılmak üzere bir alan olarak sunulur.</span><span class="sxs-lookup"><span data-stu-id="524b1-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="524b1-175">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="524b1-176">Ad alanına 'Kod' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="524b1-177">Madde türü alanında 'Dize' seçin.</span><span class="sxs-lookup"><span data-stu-id="524b1-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="524b1-178">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-178">Click Add.</span></span>
63. <span data-ttu-id="524b1-179">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="524b1-180">İsim alanına 'Açıklama' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="524b1-181">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-181">Click Add.</span></span>
66. <span data-ttu-id="524b1-182">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="524b1-183">İsim alanında 'İsim' yazın.</span><span class="sxs-lookup"><span data-stu-id="524b1-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="524b1-184">Ekle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="524b1-184">Click Add.</span></span>
69. <span data-ttu-id="524b1-185">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-185">Click Save.</span></span>
70. <span data-ttu-id="524b1-186">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="524b1-186">Close the page.</span></span>

![ER veri modeli tasarımcısı sayfası](../media/er-financial-dimensions-guides-data-model.png)

