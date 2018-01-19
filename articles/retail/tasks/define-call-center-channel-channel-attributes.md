--- 
title: " Çağrı merkezi kanalı ve kanal özniteliklerini tanımlama"
description: "Bu yordam yeni bir perakende kanalı oluşturma ve kanal özniteliklerini tanımlamayla ilgilidir."
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: af77aea3ae1310390bd9ce060d78c8b915724263
ms.contentlocale: tr-tr
ms.lasthandoff: 01/19/2018

---
# <a name="define-call-center-channel-and-channel-attributes"></a><span data-ttu-id="ec4f0-103"> Çağrı merkezi kanalı ve kanal özniteliklerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="ec4f0-103">Define call center channel and channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ec4f0-104">Bu yordam yeni bir perakende kanalı oluşturma ve kanal özniteliklerini tanımlamayla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="ec4f0-105">Bu görevi oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="ec4f0-106">Bu yordam Perakende BT rolü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="ec4f0-107">Yeni mağaza oluştur</span><span class="sxs-lookup"><span data-stu-id="ec4f0-107">Create new store</span></span>
1. <span data-ttu-id="ec4f0-108">Tüm çalışma alanları > Kanal dağıtımı öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="ec4f0-109">Yeni kanal'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-109">Click New channel.</span></span>
3. <span data-ttu-id="ec4f0-110">Mağaza'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-110">Click Store.</span></span>
4. <span data-ttu-id="ec4f0-111">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ec4f0-112">Mağaza numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="ec4f0-113">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ec4f0-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ec4f0-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ec4f0-116">Mağaza saat dilimi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="ec4f0-117">Kanal profili alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ec4f0-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ec4f0-119">Dil alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="ec4f0-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="ec4f0-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="ec4f0-122">Satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="ec4f0-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ec4f0-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="ec4f0-125">Müşteri adres defteri alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ec4f0-126">Müşterileri bu mağazaya bağlamak için kullanılan adresi defterini seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="ec4f0-127">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="ec4f0-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="ec4f0-129">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-129">Click Select.</span></span>
22. <span data-ttu-id="ec4f0-130">Çalışan adres defteri alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ec4f0-131">Veznedarları bu kanala bağlamak için kullanılan adresi defterini seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="ec4f0-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="ec4f0-133">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="ec4f0-134">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-134">Click Select.</span></span>
26. <span data-ttu-id="ec4f0-135">Varsayılan müşteri alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="ec4f0-136">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="ec4f0-137">Ekran düzeni bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="ec4f0-138">Ekran düzeni kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ec4f0-139">Bu mağaza için varsayılan POS ekranı düzenini seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="ec4f0-140">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="ec4f0-141">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="ec4f0-142">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="ec4f0-143">Kanal öznitelikleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="ec4f0-144">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-144">Click New.</span></span>
35. <span data-ttu-id="ec4f0-145">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="ec4f0-146">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="ec4f0-147">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="ec4f0-148">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-148">Click Save.</span></span>
39. <span data-ttu-id="ec4f0-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-149">Close the page.</span></span>
40. <span data-ttu-id="ec4f0-150">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="ec4f0-151">Ödeme yöntemleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-151">Click Payment methods.</span></span>
42. <span data-ttu-id="ec4f0-152">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-152">Click New.</span></span>
43. <span data-ttu-id="ec4f0-153">Ödeme yöntemi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="ec4f0-154">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="ec4f0-155">Nakil bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="ec4f0-156">Hesap numarası alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="ec4f0-157">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-157">Click Save.</span></span>
48. <span data-ttu-id="ec4f0-158">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-158">Close the page.</span></span>
49. <span data-ttu-id="ec4f0-159">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="ec4f0-160">Kasa bildirimi'ni tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="ec4f0-161">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-161">Click New.</span></span>
52. <span data-ttu-id="ec4f0-162">Para birimi hareket miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="ec4f0-163">Para birimi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="ec4f0-164">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="ec4f0-165">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="ec4f0-166">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-166">Click Save.</span></span>
57. <span data-ttu-id="ec4f0-167">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-167">Close the page.</span></span>
58. <span data-ttu-id="ec4f0-168">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="ec4f0-169">Mağaza bulucu grup ataması'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="ec4f0-170">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-170">Click New.</span></span>
61. <span data-ttu-id="ec4f0-171">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="ec4f0-172">Bulucu grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="ec4f0-173">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="ec4f0-174">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="ec4f0-175">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-175">Click Save.</span></span>
66. <span data-ttu-id="ec4f0-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec4f0-176">Close the page.</span></span>


