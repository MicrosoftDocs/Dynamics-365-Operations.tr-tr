---
title: Çağrı merkezi kanalları oluşturma ve kanal özniteliklerini tanımlama
description: Bu yordam yeni bir perakende kanalı oluşturma ve kanal özniteliklerini tanımlamayla ilgilidir.
author: mugunthanm
manager: AnnBe
ms.date: 05/22/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ef094535214ecf4c65f95c36a93455446d7e388
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "346767"
---
# <a name="create-call-center-channels-and-define-channel-attributes"></a><span data-ttu-id="3a11b-103">Çağrı merkezi kanalları oluşturma ve kanal özniteliklerini tanımlama</span><span class="sxs-lookup"><span data-stu-id="3a11b-103">Create call center channels and define channel attributes</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3a11b-104">Bu yordam yeni bir perakende kanalı oluşturma ve kanal özniteliklerini tanımlamayla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="3a11b-104">This procedure walks through creating a new retail channel and defining channel attributes.</span></span> <span data-ttu-id="3a11b-105">Bu görevi oluşturmak için kullanılan demo verisi şirketi USRT'dir.</span><span class="sxs-lookup"><span data-stu-id="3a11b-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="3a11b-106">Bu yordam Perakende BT rolü için hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="3a11b-106">This procedure is intended for the Retail IT role.</span></span>


## <a name="create-new-store"></a><span data-ttu-id="3a11b-107">Yeni mağaza oluştur</span><span class="sxs-lookup"><span data-stu-id="3a11b-107">Create new store</span></span>
1. <span data-ttu-id="3a11b-108">Tüm çalışma alanları > Kanal dağıtımı öğelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-108">Go to All workspaces > Channel deployment.</span></span>
2. <span data-ttu-id="3a11b-109">Yeni kanal'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-109">Click New channel.</span></span>
3. <span data-ttu-id="3a11b-110">Mağaza'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-110">Click Store.</span></span>
4. <span data-ttu-id="3a11b-111">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3a11b-112">Mağaza numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-112">In the Store number field, type a value.</span></span>
6. <span data-ttu-id="3a11b-113">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-113">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3a11b-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="3a11b-115">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3a11b-116">Mağaza saat dilimi alanında bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-116">In the Store time zone field, select an option.</span></span>
10. <span data-ttu-id="3a11b-117">Kanal profili alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-117">In the Channel profile field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="3a11b-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="3a11b-119">Dil alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-119">In the Language field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="3a11b-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="3a11b-121">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-121">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="3a11b-122">Satış vergisi grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-122">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="3a11b-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-123">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="3a11b-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="3a11b-125">Müşteri adres defteri alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-125">In the Customer address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3a11b-126">Müşterileri bu mağazaya bağlamak için kullanılan adresi defterini seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-126">Select the address book used to link customers to this store.</span></span>  
19. <span data-ttu-id="3a11b-127">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-127">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="3a11b-128">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-128">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="3a11b-129">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-129">Click Select.</span></span>
22. <span data-ttu-id="3a11b-130">Çalışan adres defteri alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-130">In the Employee address book field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3a11b-131">Veznedarları bu kanala bağlamak için kullanılan adresi defterini seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-131">Select the address book used to link cashiers to this channel.</span></span>  
23. <span data-ttu-id="3a11b-132">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-132">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="3a11b-133">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-133">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="3a11b-134">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-134">Click Select.</span></span>
26. <span data-ttu-id="3a11b-135">Varsayılan müşteri alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-135">In the Default customer field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="3a11b-136">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-136">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="3a11b-137">Ekran düzeni bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-137">Expand or collapse the Screen layout section.</span></span>
29. <span data-ttu-id="3a11b-138">Ekran düzeni kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-138">In the Screen layout ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3a11b-139">Bu mağaza için varsayılan POS ekranı düzenini seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-139">Select the default POS screen layout for this store.</span></span>  
30. <span data-ttu-id="3a11b-140">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-140">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="3a11b-141">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="3a11b-142">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-142">On the Action Pane, click Set up.</span></span>
33. <span data-ttu-id="3a11b-143">Kanal öznitelikleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-143">Click Channel attributes.</span></span>
34. <span data-ttu-id="3a11b-144">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-144">Click New.</span></span>
35. <span data-ttu-id="3a11b-145">Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-145">In the Name field, click the drop-down button to open the lookup.</span></span>
36. <span data-ttu-id="3a11b-146">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-146">In the list, find and select the desired record.</span></span>
37. <span data-ttu-id="3a11b-147">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-147">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="3a11b-148">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-148">Click Save.</span></span>
39. <span data-ttu-id="3a11b-149">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-149">Close the page.</span></span>
40. <span data-ttu-id="3a11b-150">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-150">On the Action Pane, click Set up.</span></span>
41. <span data-ttu-id="3a11b-151">Ödeme yöntemleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-151">Click Payment methods.</span></span>
42. <span data-ttu-id="3a11b-152">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-152">Click New.</span></span>
43. <span data-ttu-id="3a11b-153">Ödeme yöntemi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-153">In the Payment method field, click the drop-down button to open the lookup.</span></span>
44. <span data-ttu-id="3a11b-154">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-154">In the list, click the link in the selected row.</span></span>
45. <span data-ttu-id="3a11b-155">Nakil bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-155">Expand or collapse the Posting section.</span></span>
46. <span data-ttu-id="3a11b-156">Hesap numarası alanında istediğiniz değerleri belirtin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-156">In the Account number field, specify the desired values.</span></span>
47. <span data-ttu-id="3a11b-157">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-157">Click Save.</span></span>
48. <span data-ttu-id="3a11b-158">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-158">Close the page.</span></span>
49. <span data-ttu-id="3a11b-159">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-159">On the Action Pane, click Set up.</span></span>
50. <span data-ttu-id="3a11b-160">Kasa bildirimi'ni tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-160">Click Cash declaration.</span></span>
51. <span data-ttu-id="3a11b-161">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-161">Click New.</span></span>
52. <span data-ttu-id="3a11b-162">Para birimi hareket miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-162">In the Amount in transaction currency field, enter a number.</span></span>
53. <span data-ttu-id="3a11b-163">Para birimi alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-163">In the Currency field, click the drop-down button to open the lookup.</span></span>
54. <span data-ttu-id="3a11b-164">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-164">In the list, find and select the desired record.</span></span>
55. <span data-ttu-id="3a11b-165">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-165">In the list, click the link in the selected row.</span></span>
56. <span data-ttu-id="3a11b-166">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-166">Click Save.</span></span>
57. <span data-ttu-id="3a11b-167">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-167">Close the page.</span></span>
58. <span data-ttu-id="3a11b-168">Eylem Bölmesinde Kurulum'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-168">On the Action Pane, click Set up.</span></span>
59. <span data-ttu-id="3a11b-169">Mağaza bulucu grup ataması'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-169">Click Store locator group assignment.</span></span>
60. <span data-ttu-id="3a11b-170">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-170">Click New.</span></span>
61. <span data-ttu-id="3a11b-171">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-171">In the list, mark the selected row.</span></span>
62. <span data-ttu-id="3a11b-172">Bulucu grubu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-172">In the Locator group field, click the drop-down button to open the lookup.</span></span>
63. <span data-ttu-id="3a11b-173">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a11b-173">In the list, find and select the desired record.</span></span>
64. <span data-ttu-id="3a11b-174">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-174">In the list, click the link in the selected row.</span></span>
65. <span data-ttu-id="3a11b-175">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-175">Click Save.</span></span>
66. <span data-ttu-id="3a11b-176">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3a11b-176">Close the page.</span></span>

