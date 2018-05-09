--- 
title: "Elektronik raporlama (ER) için oluşturulan biçimin bileşenlerini veri modeli öğelerine eşleme"
description: "Aşağıdaki yordam, Sistem yöneticisi veya Elektronik raporlama geliştirici rolüne sahip bir kullanıcının, veri modeli öğelerini ödemeler iş etki alanı için bir elektronik dosya biçimini tanımlayan, oluşturulmuş Elektronik raporlama (ER) yapılandırmasının bileşenlerine nasıl eşleyebileceğini gösterir."
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 921e00051e8d9647f16b1e29dfbda8821f28c7e5
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="map-components-of-the-created-format-to-data-model-elements-for-electronic-reporting-er"></a><span data-ttu-id="1c546-103">Elektronik raporlama (ER) için oluşturulan biçimin bileşenlerini veri modeli öğelerine eşleme</span><span class="sxs-lookup"><span data-stu-id="1c546-103">Map components of the created format to data model elements for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c546-104">Aşağıdaki yordam, Sistem yöneticisi veya Elektronik raporlama geliştirici rolüne sahip bir kullanıcının, veri modeli öğelerini ödemeler iş etki alanı için bir elektronik dosya biçimini tanımlayan, oluşturulmuş Elektronik raporlama (ER) yapılandırmasının bileşenlerine nasıl eşleyebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c546-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="1c546-105">Bu biçim daha sonra ödeme işlemleri için elektronik belgeler oluşturmak üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1c546-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="1c546-106">Bu örnekte, 'Litware, Inc.' örnek şirketi için bir biçim yapılandırması oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="1c546-106">In this example, you will create a format configuration for the sample company, ‘Litware, Inc.’.</span></span> <span data-ttu-id="1c546-107">Bu adımlar, ER yapılandırmaları tüm şirketlerde paylaşıldığı için herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="1c546-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="1c546-108">Bu adımları tamamlamak için öncelikle "Bir biçim yapılandırması oluşturma" görev kılavuzundaki adımları tamamlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="1c546-108">To complete these steps, you must first complete the steps in the “Create a format configuration” task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="1c546-109">Biçim yapılandırması seçme</span><span class="sxs-lookup"><span data-stu-id="1c546-109">Select a format configuration</span></span>
1. <span data-ttu-id="1c546-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="1c546-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1c546-111">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1c546-112">Ağaçta, 'Ödemeler (Basitleştirilmiş model)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="1c546-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="1c546-113">Ağaçta 'Payments (simplified model)\BACS (UK fictitious)' seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="1c546-114">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c546-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="1c546-115">Format bileşenlerini veri modeli öğelerine eşleyin</span><span class="sxs-lookup"><span data-stu-id="1c546-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="1c546-116">Genişlet/daralt'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="1c546-117">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="1c546-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="1c546-118">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="1c546-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="1c546-119">Ağaçta, "Xml\İleti\ProcessingDate\DateTime" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="1c546-120">Ağaçta, "model\ProcessingDateTime" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="1c546-121">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-121">Click Bind.</span></span>
7. <span data-ttu-id="1c546-122">Ağaçta, "Xml\İleti\MessageId\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="1c546-123">Ağaçta, "model\MessageIdentification" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="1c546-124">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-124">Click Bind.</span></span>
10. <span data-ttu-id="1c546-125">Ağaçta genişletin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="1c546-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="1c546-126">Ağaçta, "Xml\İleti\Ödemeler\Madde\Tutar\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="1c546-127">Ağaçta, "model\Ödemeler\InstructedAmount" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="1c546-128">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-128">Click Bind.</span></span>
14. <span data-ttu-id="1c546-129">Ağaçta, "Xml\İleti\Ödemeler\Madde\TransDate\DateTime" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="1c546-130">Ağaçta, "model\Ödemeler\TransactionDate" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="1c546-131">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-131">Click Bind.</span></span>
17. <span data-ttu-id="1c546-132">Ağaçta, "Xml\İleti\Ödemeler\Madde\Açıklama\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="1c546-133">Ağaçta seçin 'model\Payments\Description'.</span><span class="sxs-lookup"><span data-stu-id="1c546-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="1c546-134">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-134">Click Bind.</span></span>
20. <span data-ttu-id="1c546-135">Ağaçta, "Xml\İleti\Ödemeler\Madde\Para Birimi\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="1c546-136">Ağaçta seçin 'model\Payments\Currency'.</span><span class="sxs-lookup"><span data-stu-id="1c546-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="1c546-137">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-137">Click Bind.</span></span>
23. <span data-ttu-id="1c546-138">Ağaçta, "Xml\İleti\Ödemeler\Madde\Kimlik" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="1c546-139">Ağaçta, "model\Ödemeler\End2EndID" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="1c546-140">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-140">Click Bind.</span></span>
26. <span data-ttu-id="1c546-141">Ağaçta genişletin 'model\Payments\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="1c546-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="1c546-142">Ağaçta genişletin 'model\Payments\Creditor\Account'.</span><span class="sxs-lookup"><span data-stu-id="1c546-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="1c546-143">Ağaçta genişletin 'model\Payments\Creditor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="1c546-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="1c546-144">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Ad\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="1c546-145">Ağaçta seçin 'model\Payments\Creditor\Name'.</span><span class="sxs-lookup"><span data-stu-id="1c546-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="1c546-146">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-146">Click Bind.</span></span>
32. <span data-ttu-id="1c546-147">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\RoutingNumber\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="1c546-148">Ağaçta, "model\Ödemeler\Alacaklı\Temsilci\RoutingNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="1c546-149">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-149">Click Bind.</span></span>
35. <span data-ttu-id="1c546-150">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\AccountNumber\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="1c546-151">Ağaçta seçin 'model\Payments\Creditor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="1c546-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="1c546-152">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-152">Click Bind.</span></span>
38. <span data-ttu-id="1c546-153">Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Ad\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="1c546-154">Ağaçta genişletin 'model\Payments\Debtor'.</span><span class="sxs-lookup"><span data-stu-id="1c546-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="1c546-155">Ağaçta genişletin 'model\Payments\Debtor\Account'.</span><span class="sxs-lookup"><span data-stu-id="1c546-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="1c546-156">Ağaçta genişletin 'model\Payments\Debtor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="1c546-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="1c546-157">Ağaçta seçin 'model\Payments\Debtor\Name'.</span><span class="sxs-lookup"><span data-stu-id="1c546-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="1c546-158">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-158">Click Bind.</span></span>
44. <span data-ttu-id="1c546-159">Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\RoutingNumber\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="1c546-160">Ağaçta, "model\Ödemeler\Borçlu\Temsilci\RoutingNumber" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="1c546-161">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-161">Click Bind.</span></span>
47. <span data-ttu-id="1c546-162">Ağaçta, "Xml\İleti\Ödemeler\Madde\Ödeyen\Banka\AccountNumber\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="1c546-163">Ağaçta seçin 'model\Payments\Debtor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="1c546-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="1c546-164">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-164">Click Bind.</span></span>
50. <span data-ttu-id="1c546-165">Ağaçta, "Xml\İleti\Ödemeler\Madde" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="1c546-166">Ağaçta seçin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="1c546-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="1c546-167">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-167">Click Bind.</span></span>
53. <span data-ttu-id="1c546-168">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="1c546-169">Biçim eşlemesini doğrulama</span><span class="sxs-lookup"><span data-stu-id="1c546-169">Validate format mapping</span></span>
1. <span data-ttu-id="1c546-170">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-170">Click Validate.</span></span>
    * <span data-ttu-id="1c546-171">Tüm bağlamaların doğru yapıldığından emin olmak için yeni eşlemeyi doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="1c546-172">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c546-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="1c546-173">Biçim yapılandırmasının geçerli sürümünün durumunu değiştirin</span><span class="sxs-lookup"><span data-stu-id="1c546-173">Change status of the current version of format configuration</span></span>
    * <span data-ttu-id="1c546-174">Sonraki adımlarda, biçim yapılandırmasının durumunu Taslak yerine Tamamlandı olarak değiştirerek ödeme belgesi oluşturmada kullanılabilir hale getirin.</span><span class="sxs-lookup"><span data-stu-id="1c546-174">In the next steps, you’ll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="1c546-175">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-175">Click Change status.</span></span>
2. <span data-ttu-id="1c546-176">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-176">Click Complete.</span></span>
3. <span data-ttu-id="1c546-177">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="1c546-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="1c546-178">Örneğin, "sürüm 1".</span><span class="sxs-lookup"><span data-stu-id="1c546-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="1c546-179">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c546-179">Click OK.</span></span>
5. <span data-ttu-id="1c546-180">Geçerli yapılandırmanın tamamlanan sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="1c546-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="1c546-181">Yapılandırmanın, tamamlanan sürüm 1.1 (veri modelinin sürüm 1'ini temel alan biçimin sürüm 1'i) olarak kaydedildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="1c546-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="1c546-182">Tamamlanan biçiminin sürümü için yürürlük tarihi tanımla</span><span class="sxs-lookup"><span data-stu-id="1c546-182">Define effective date for completed version of format</span></span>
    * <span data-ttu-id="1c546-183">Her biçimi sürümü belirli bir tarihten itibaren kullanılabilecek şekilde yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="1c546-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="1c546-184">Belirli bir tarihte birden fazla biçim sürümü etkin olduğunda, kullanım için en son biçim (sürüm numarasına bağlı olarak) seçilir.</span><span class="sxs-lookup"><span data-stu-id="1c546-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="1c546-185">Uygun sürüm seçimi için oturum tarihi değeri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1c546-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="1c546-186">Oluşturulan biçime şirketlerden erişimi kısıtlama</span><span class="sxs-lookup"><span data-stu-id="1c546-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="1c546-187">ISO Ülke/bölge kodları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="1c546-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="1c546-188">Her biçim erişimi, biçimin geçerli olacağı ülke/bölgeleri tanımlayarak kısıtlanabilir.</span><span class="sxs-lookup"><span data-stu-id="1c546-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="1c546-189">Belirli biçim için ülkeler/bölgeler listesi boş olduğunda, bu biçim herhangi bir şirkette kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1c546-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="1c546-190">Bazı ISO ülke/bölge kodları ülkeler/bölgeler listesine eklendiğinde, bu biçim yalnızca birincil adresi ülke/bölge listesinde olan şirketlerde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1c546-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  


