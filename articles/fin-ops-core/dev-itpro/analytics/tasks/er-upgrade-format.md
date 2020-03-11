---
title: ER Biçiminizi, o biçimin yeni bir temel sürümünü benimseyerek yükseltin.
description: Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir Elektronik raporlama (ER) biçim yapılandırmasını nasıl sürdürebileceğini gösterir.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b4ad9fb7a3d768acb0af73dcbe3d87b323de727
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042816"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="42374-103">ER Biçiminizi, o biçimin yeni bir temel sürümünü benimseyerek yükseltin.</span><span class="sxs-lookup"><span data-stu-id="42374-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42374-104">Aşağıdaki yordam, Sistem Yöneticisi veya Elektronik Raporlama geliştiricisi rolündeki bir kullanıcının, bir Elektronik raporlama (ER) biçim yapılandırmasını nasıl sürdürebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="42374-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="42374-105">Bu yordam, bir yapılandırma sağlayıcısından (CP) alınan biçime dayalı olarak bir biçimin özel bir sürümünün nasıl oluşturulabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="42374-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="42374-106">Ayrıca, bu biçimin yeni bir temel sürümünün nasıl benimseneceğini de açıklar.</span><span class="sxs-lookup"><span data-stu-id="42374-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="42374-107">Bu adımları tamamlamak için önce "yapılandırma sağlayıcı oluşturmak ve etkin olarak işaretleme" ve "Kullanım biçimi ödemeler için elektronik belgeleri oluşturmak için oluşturulan" yordamlarındaki adımları tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="42374-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” and “Use created format to generate electronic documents for payments” procedures.</span></span> <span data-ttu-id="42374-108">Bu adımlar GBSI şirketinde gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="42374-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="42374-109">Özelleştirme için yapılandırma biçimi seçin</span><span class="sxs-lookup"><span data-stu-id="42374-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="42374-110">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="42374-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="42374-111">Bu örnekte örnek şirket Litware, Inc. (https://www.litware.com) belirli bir ülke için elektronik ödemeleri destekleyen bir biçim yapılandırma sağlayıcısı görevi görecektir.</span><span class="sxs-lookup"><span data-stu-id="42374-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="42374-112">Örnek şirket Proseware, Inc. (http://www.proseware.com) Litware, Inc. tarafından sağlanan biçim yapılandırmasının tüketicisi görevi görecektir.</span><span class="sxs-lookup"><span data-stu-id="42374-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="42374-113">Proseware, Inc. bu ülkenin belirli bölgelerdeki biçimleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="42374-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="42374-114">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="42374-115">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-115">Click Show filters.</span></span>
4. <span data-ttu-id="42374-116">Şu filtreleri uygulayın: "ile başlar" filtre işlecini kullanarak "Ad" alanında "BACS (Birleşik Krallık hayali)" için bir filtre değeri girin.</span><span class="sxs-lookup"><span data-stu-id="42374-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="42374-117">Seçili biçim yapılandırması BACS'nin (Birleşik Krallık hayali) sahibi, sağlayıcı Litware, Inc.'dir.</span><span class="sxs-lookup"><span data-stu-id="42374-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="42374-118">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-118">Click Show filters.</span></span>
6. <span data-ttu-id="42374-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="42374-120">Tamamlandı durumunda olan biçim sürümü, Proseware, Inc. özelleştirme için.</span><span class="sxs-lookup"><span data-stu-id="42374-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="42374-121">Elektronik belgenin özel bir biçim için yeni bir konfigürasyonunu oluşturma</span><span class="sxs-lookup"><span data-stu-id="42374-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="42374-122">Proseware, Inc. BACS (UK hayali) yapılandırmasının, hizmet aboneliklerine uygun olarak Litware, Inc.'den ödeme belgeleri oluşturmak için gerekli biçimi içeren, alınan sürüm 1.1.</span><span class="sxs-lookup"><span data-stu-id="42374-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="42374-123">Proseware, Inc. kendi ülkesi için bunu bir standart olarak kullanmak istiyor fakat çeşitli bölgesel gereklilikleri desteklemek için bazı özelleştirmeler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="42374-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="42374-124">Proseware, Inc. ayrıca, özelleştirilmiş bir biçimden Litware Inc. tarafından (yeni ülke gereksinimlerini destekleyen) gelen yeni sürüme hızlı bir biçimde geçiş yapmak için yükseltme kabiliyetini de tutmak istiyor ve bu yükseltmeyi en düşük maliyetle gerçekleştirmek istiyor.</span><span class="sxs-lookup"><span data-stu-id="42374-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="42374-125">Bunu yapmak için Proseware, Inc'nin Litware, Inc. yapılandırması BACS'yi (Birleşik Krallık hayali) taban olarak kullanan bir yapılandırma oluşturması gerekir.</span><span class="sxs-lookup"><span data-stu-id="42374-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="42374-126">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="42374-126">Close the page.</span></span>
2. <span data-ttu-id="42374-127">Etkin bir sağlayıcı yapmak için Proseware, Inc.'i seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="42374-128">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-128">Click Set active.</span></span>
4. <span data-ttu-id="42374-129">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="42374-130">Ağaçta, 'Ödemeler (Basitleştirilmiş model)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="42374-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="42374-131">Ağaçta 'Payments (simplified model)\BACS (UK fictitious)' seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="42374-132">Litware, Inc.'den BACS (Birleşik Krallık hayali) yapılandırmasını seçin. Proseware, Inc. sürüm 1.1'i özel sürümün tabanı olarak kullanacaktır.</span><span class="sxs-lookup"><span data-stu-id="42374-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="42374-133">İletişim kutusu formunu açmak için Yapılandırma oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="42374-134">Bu, özel bir ödeme biçimi için yeni bir yapılandırma oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="42374-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="42374-135">Yeni alanında, 'İsimden Türet: BACS (UK hayali), Litware, Inc.' girin.</span><span class="sxs-lookup"><span data-stu-id="42374-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="42374-136">Özel sürümü oluşturma için temel olarak BACS (UK hayali) kullanımını onaylamak için Türet seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="42374-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="42374-137">İsim alanına, 'BACS (UK hayali özel)' yazın.</span><span class="sxs-lookup"><span data-stu-id="42374-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="42374-138">Açıklama alanına, "BACS satıcı ödemesi (Birleşik Krallık özel)" yazın.</span><span class="sxs-lookup"><span data-stu-id="42374-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="42374-139">Etkin yapılandırma sağlayıcısı (Proseware, Inc.) otomatik olarak buraya girilir.</span><span class="sxs-lookup"><span data-stu-id="42374-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="42374-140">Bu sağlayıcının, bu yapılandırmayı sürdürmesi mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="42374-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="42374-141">Diğer sağlayıcılar bu yapılandırmayı kullanabilir, ancak onu sürdüremezler.</span><span class="sxs-lookup"><span data-stu-id="42374-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="42374-142">Konfigürasyon oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="42374-143">Elektronik belge için biçiminizi özelleştirme</span><span class="sxs-lookup"><span data-stu-id="42374-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="42374-144">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-144">Click Designer.</span></span>
2. <span data-ttu-id="42374-145">Genişlet/daralt'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="42374-146">Genişlet/daralt'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="42374-147">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="42374-148">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="42374-149">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="42374-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="42374-150">İsim alanına 'IBAN' yazın.</span><span class="sxs-lookup"><span data-stu-id="42374-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="42374-151">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-151">Click OK.</span></span>
9. <span data-ttu-id="42374-152">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\IBAN" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="42374-153">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="42374-154">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="42374-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="42374-155">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-155">Click OK.</span></span>
13. <span data-ttu-id="42374-156">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Ad\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="42374-157">Maksimum uzunluk alanında 60 girin.</span><span class="sxs-lookup"><span data-stu-id="42374-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="42374-158">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="42374-159">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="42374-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="42374-160">Ağaçta genişletin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="42374-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="42374-161">Ağaçta genişletin 'model\Payments\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="42374-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="42374-162">Ağaçta genişletin 'model\Payments\Creditor\Account'.</span><span class="sxs-lookup"><span data-stu-id="42374-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="42374-163">Ağaçta, "model\Ödemeler\Alacaklı\Hesap\IBAN" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="42374-164">Ağaçta, "Xml\İleti\Ödemeler\Madde =  model.Payments\Satıcı\Banka\IBAN\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="42374-165">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-165">Click Bind.</span></span>
23. <span data-ttu-id="42374-166">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="42374-167">Özelleştirilmiş biçimi doğrulama</span><span class="sxs-lookup"><span data-stu-id="42374-167">Validate the customized format</span></span>
1. <span data-ttu-id="42374-168">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-168">Click Validate.</span></span>

    <span data-ttu-id="42374-169">Tüm bağlamaların sorunsuz olduğundan emin olmak için özelleştirilmiş biçimi düzeninin ve veri eşlemesi değişikliklerini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="42374-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="42374-170">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="42374-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="42374-171">Özel biçim yapılandırmasının geçerli sürümünün durumunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="42374-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="42374-172">Ödeme belgesi oluşturulmasında kullanılabilir duruma getirmek için tasarlanan biçim yapılandırmasının durumunu Taslak'tan Tamamlandı'ya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="42374-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="42374-173">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-173">Click Change status.</span></span>

    <span data-ttu-id="42374-174">Seçili yapılandırmanın geçerli sürümünün Taslak durumunda olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="42374-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="42374-175">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-175">Click Complete.</span></span>
3. <span data-ttu-id="42374-176">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="42374-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="42374-177">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-177">Click OK.</span></span>
5. <span data-ttu-id="42374-178">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="42374-179">Oluşturulan yapılandırmanın tamamlanmış sürüm 1.1.1 olarak kaydedildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="42374-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="42374-180">Bu, BACS (Birleşik Krallık, hayali özel) biçiminin, Ödemeler (basitleştirilmiş model) veri modelinin 1. sürümüne dayalı olan BACS (Birleşik Krallık hayali) biçiminin 1. sürümüne dayalı olduğu anlamına gelmektedir.</span><span class="sxs-lookup"><span data-stu-id="42374-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="42374-181">Ödeme dosyaları oluşturmak için özelleştirilmiş biçimi test et</span><span class="sxs-lookup"><span data-stu-id="42374-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="42374-182">Paralel Finance and Operations oturumunda "Ödemeler için elektronik belgeleri oluşturmak için oluşturulan biçimi kullan" yordamındaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="42374-182">Complete the steps in the “Use created format to generate electronic documents for payments” procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="42374-183">Elektronik Ödeme yöntemi parametrelerinde BACS (UK hayali özel) biçimi seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="42374-184">Oluşturulan ödeme dosyasında son sunulan XML düğümünün, bölgesel gereksinimleri uygun IBAN kodu sunma içerdiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="42374-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="42374-185">Ülkeye özgü varolan yapılandırmayı güncelleştirmek</span><span class="sxs-lookup"><span data-stu-id="42374-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="42374-186">Litware, Inc. BACS (UK hayali) yapılandırmasını güncelleştirmek ve elektronik belge biçimini yönetmek için yeni ülke gereksinimleri benimsemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="42374-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="42374-187">Daha sonra, bu yeni sürümünde Proseware, Inc. dahil olmak üzere hizmet aboneleri için sunulan bu yapılandırma içine alınacaktır.</span><span class="sxs-lookup"><span data-stu-id="42374-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="42374-188">Gerçek servis sağlama ile ilgili işlemlerde, her yeni BACS (UK hayali) sürümü Proseware, Inc. tarafından Litware, Inc.'nin yapılandırmalarının LCS havuzundan alınabilir.</span><span class="sxs-lookup"><span data-stu-id="42374-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations’ LCS repository.</span></span> <span data-ttu-id="42374-189">Bu yordamda biz bu servis sağlayıcı adına BACS (UK hayali) güncelleştirmenin benzetimini yapacağız.</span><span class="sxs-lookup"><span data-stu-id="42374-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="42374-190">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="42374-190">Close the page.</span></span>
2. <span data-ttu-id="42374-191">Litware, inc. sağlayıcısı seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="42374-192">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-192">Click Set active.</span></span>
4. <span data-ttu-id="42374-193">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="42374-194">Ağaçta, 'Ödemeler (Basitleştirilmiş model)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="42374-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="42374-195">Ağaçta 'Payments (simplified model)\BACS (UK fictitious)' seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="42374-196">Taslak sürümü Litware, Inc. şirketine aittir. sağlayıcı BACS (UK hayali), ülkeye özgü yeni gereksinimlerini desteklemek için değişiklikleri getirmek üzere seçilir.</span><span class="sxs-lookup"><span data-stu-id="42374-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="42374-197">Elektronik belge temel biçimini yerelleştirme.</span><span class="sxs-lookup"><span data-stu-id="42374-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="42374-198">Ülkeye özel yeni gereksinimlerin Litware Inc. tarafından destekleneceğini varsayalım:</span><span class="sxs-lookup"><span data-stu-id="42374-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="42374-199">Her ödeme hareketi için alacaklı banka SWIFT kodu için bir değer.</span><span class="sxs-lookup"><span data-stu-id="42374-199">A value for the creditor’s bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="42374-200">Oluşturma dosyasında satıcının adı için 100 karakter metin uzunluğu sınırı.</span><span class="sxs-lookup"><span data-stu-id="42374-200">A limit of 100 characters for the length of text for the vendor’s name in a generating file.</span></span>  
- <span data-ttu-id="42374-201">Yeni ülkeye özgü gereksinimler</span><span class="sxs-lookup"><span data-stu-id="42374-201">New country-specific requirements</span></span>  
- <span data-ttu-id="42374-202">Gerekli değişiklikleri tanıtmak için istenen yapılandırmanın taslak sürümünü seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="42374-203">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-203">Click Designer.</span></span>
2. <span data-ttu-id="42374-204">Genişlet/daralt'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="42374-205">Genişlet/daralt'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="42374-206">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="42374-207">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="42374-208">Ağaçta seçin 'XML\Element'.</span><span class="sxs-lookup"><span data-stu-id="42374-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="42374-209">İsim alanına 'SWIFT' yazın.</span><span class="sxs-lookup"><span data-stu-id="42374-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="42374-210">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-210">Click OK.</span></span>
9. <span data-ttu-id="42374-211">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Banka\SWIFT" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="42374-212">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="42374-213">Ağaçta seçin 'Text\String'.</span><span class="sxs-lookup"><span data-stu-id="42374-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="42374-214">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-214">Click OK.</span></span>
13. <span data-ttu-id="42374-215">Ağaçta, "Xml\İleti\Ödemeler\Madde\Satıcı\Ad\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="42374-216">Maksimum uzunluk alanında 100 girin.</span><span class="sxs-lookup"><span data-stu-id="42374-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="42374-217">Eşleme sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="42374-218">Ağaçta, 'model'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="42374-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="42374-219">Ağaçta genişletin 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="42374-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="42374-220">Ağaçta genişletin 'model\Payments\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="42374-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="42374-221">Ağaçta genişletin 'model\Payments\Creditor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="42374-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="42374-222">Ağaçta, "model\Ödemeler\Alacaklı\Temsilci\SWIFT" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="42374-223">Ağaçta, "Xml\İleti\Ödemeler\Madde =  model.Payments\Satıcı\Banka\SWIFT\Dize" öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="42374-224">Bağla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-224">Click Bind.</span></span>
23. <span data-ttu-id="42374-225">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="42374-226">Yerelleştirilmiş biçimi doğrulama</span><span class="sxs-lookup"><span data-stu-id="42374-226">Validate the localized format</span></span>
1. <span data-ttu-id="42374-227">Doğrula'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-227">Click Validate.</span></span>
2. <span data-ttu-id="42374-228">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="42374-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="42374-229">Temel biçim yapılandırmasının geçerli sürümünün durumunu değiştirin</span><span class="sxs-lookup"><span data-stu-id="42374-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="42374-230">Güncelleştirilen temel biçim yapılandırmasının durumunu, ödeme belgeleri ve bundan türetilen biçim yapılandırmalarının oluşturulmasında kullanılabilmesi için, Taslak'tan Tamamlandı'ya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="42374-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="42374-231">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-231">Click Change status.</span></span>

    <span data-ttu-id="42374-232">Seçili yapılandırmanın geçerli sürümünün Taslak durumunda olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="42374-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="42374-233">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-233">Click Complete.</span></span>
3. <span data-ttu-id="42374-234">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="42374-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="42374-235">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-235">Click OK.</span></span>
5. <span data-ttu-id="42374-236">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="42374-237">Özel biçim yapılandırması için temel sürümü değiştir</span><span class="sxs-lookup"><span data-stu-id="42374-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="42374-238">Proseware, Inc.'nin BACS (UK hayali) yapılandırmasının yeni sürümü 1.2'nin yakın zaman önce duyurulan ülkeye özgü gereksinimleri uygun elektronik ödeme belgeleri oluşturmak kullanılabilir olduğunu bilgisi verilir.</span><span class="sxs-lookup"><span data-stu-id="42374-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="42374-239">Proseware, Inc. bu ülke için bir standart olarak bunu kullanmaya başlamak istiyor.</span><span class="sxs-lookup"><span data-stu-id="42374-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="42374-240">Proseware, Inc'nin bunu yapmak için temel yapılandırma sürümünü, BACS (UK hayali özel) özel yapılandırma sürümü için değiştirmesi gerekiyor.</span><span class="sxs-lookup"><span data-stu-id="42374-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="42374-241">BACS (UK hayali) 1.1 sürümü yerine yeni sürüm 1.2 kullanın.</span><span class="sxs-lookup"><span data-stu-id="42374-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="42374-242">Organizasyon yönetimi > Çalışma alanları > Elektronik raporlama'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="42374-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="42374-243">Etkin olarak işaretlemek için Proseware, Inc. sağlayıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="42374-244">Etkin olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-244">Click Set active.</span></span>
4. <span data-ttu-id="42374-245">Raporlama konfigürasyonları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="42374-246">Ağaçta, 'Ödemeler (Basitleştirilmiş model)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="42374-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="42374-247">Ağaçta 'Payments (simplified model)\BACS (UK fictitious)' genişletin.</span><span class="sxs-lookup"><span data-stu-id="42374-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="42374-248">Ağaçta 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)' seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="42374-249">Proseware, Inc. şirketine ait olan BACS (Birleşik Krallık, hayali özel) yapılandırmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="42374-250">Gerekli değişiklikleri tanıtmak için seçili yapılandırmanın taslak sürümünü kullanın.</span><span class="sxs-lookup"><span data-stu-id="42374-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="42374-251">Rebase'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-251">Click Rebase.</span></span>

    <span data-ttu-id="42374-252">Yapılandırmayı güncelleştirmek için yeni bir temel olarak uygulanması için yeni sürüm 1.2'yi temel yapılandırma olarak seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="42374-253">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-253">Click OK.</span></span>

    <span data-ttu-id="42374-254">Otomatik olarak birleştirilemeyen bazı biçim değişikliklerini temsil eden, yeni temel sürüm ile özel sürümün birleştirilmesi sırasında bazı çakışmaların ortaya çıktığını göz önünde tutun.</span><span class="sxs-lookup"><span data-stu-id="42374-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can’t be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="42374-255">Rebase çakışmalarını çözümle</span><span class="sxs-lookup"><span data-stu-id="42374-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="42374-256">Tasarımcı'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-256">Click Designer.</span></span>
    
    <span data-ttu-id="42374-257">Satıcının adı metin uzunluğu sınırına yapılan değişikliğin otomatik olarak çözümlenme uygulanamadığını göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="42374-257">Note that changes to the vendor’s name text length limit couldn’t be resolved automatically.</span></span> <span data-ttu-id="42374-258">Bu nedenle, bu çakışmalar listesinde görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="42374-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="42374-259">Her Güncelleştirme türü çakışma için, aşağıdaki seçenekler mevcuttur:  - Önceki taban sürüm değerini (bu durumda 0 olan) getirmek için, daha önceki bir taban değeri uygula (ızgaranın üstündeki düğme).</span><span class="sxs-lookup"><span data-stu-id="42374-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="42374-260">- Yeni temel sürüm değerini (bu durumda 100) getirmek için temel bir değer uygula. (ızgara üzerindeki düğme).</span><span class="sxs-lookup"><span data-stu-id="42374-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="42374-261">- Kendi (özel) değerinizi tutun (bizim durumumuzda 60).</span><span class="sxs-lookup"><span data-stu-id="42374-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="42374-262">Satıcı adı uzunluğu için bir ülkeye özgü temel sınır olan 100 karakter limitini uygulamak için Uygula'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor’s name text length.</span></span>  

    <span data-ttu-id="42374-263">Proseware, Inc. şirketinin ve Litware, Inc.'in yönetim biçiminde ilgili bileşenlerin otomatik olarak birleştirildiği, IBAN ve SWIFT kodları kullanarak bu biçim için özel ve yerel sürümlerinin olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="42374-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="42374-264">Taban değeri uygula'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-264">Click Apply base value.</span></span>

    <span data-ttu-id="42374-265">Satıcı adlarına ülkeye özgü temel sınır olan 100 karakter limitini uygulamak için Uygula'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="42374-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="42374-266">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-266">Click Save.</span></span>

    <span data-ttu-id="42374-267">Biçimi kaydetmek, çözümlenen çakışmaları çakışmalar listesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42374-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="42374-268">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="42374-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="42374-269">Özel biçim yapılandırmasının geçerli sürümünün durumunu değiştirin</span><span class="sxs-lookup"><span data-stu-id="42374-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="42374-270">Durumu değiştir öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-270">Click Change status.</span></span>

    <span data-ttu-id="42374-271">Güncelleştirilen, özel biçim yapılandırmasının durumunu Taslak'tan, Tamamlandı'ya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="42374-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="42374-272">Bu, ödeme belgeleri oluşturmak için biçim yapılandırmasını kullanılabilir hale getirir.</span><span class="sxs-lookup"><span data-stu-id="42374-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="42374-273">Seçili yapılandırmanın geçerli sürümünün Taslak durumunda olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="42374-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="42374-274">Tamamla öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-274">Click Complete.</span></span>
3. <span data-ttu-id="42374-275">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="42374-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="42374-276">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="42374-276">Click OK.</span></span>

    <span data-ttu-id="42374-277">Oluşturulan yapılandırmanın tamamlanmış sürüm 1.2.2: taban BACS (UK hayali özel) biçiminin 2. sürümü, yani temel BACS (UK hayali) biçiminin 2. sürümüne dayalı, bu da Ödemeler (basitleştirilmiş model) veri modelinin 1. sürümüne dayalı olan sürüm olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="42374-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="42374-278">Ödeme dosyaları oluşturması için özelleştirilmiş biçimi test et</span><span class="sxs-lookup"><span data-stu-id="42374-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="42374-279">Paralel Finance and Operations oturumunda "Ödemeler için elektronik belgeleri oluşturmak için oluşturulan biçimi kullan" yordamındaki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="42374-279">Complete the steps in the “Use created format to generate electronic documents for payments” procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="42374-280">Elektronik Ödeme yöntemi parametrelerinde oluşturulan 'BACS (UK hayali özel)' biçimi seçin.</span><span class="sxs-lookup"><span data-stu-id="42374-280">Select the created ‘BACS (UK fictitious custom)’ format in electronic payment method parameters.</span></span> <span data-ttu-id="42374-281">Oluşturulan ödeme dosyasında Proseware, Inc. tarafından son sunulan XML düğümünün, bölgesel gereksinimleri uygun IBAN hesap kodu sunma içerdiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="42374-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="42374-282">Dosya ayrıca Litware, Inc. tarafından yakın zaman önce sunulan XML düğün sunum SWIFT banka kodunu ülke gereksinimlerine göre içermelidir.</span><span class="sxs-lookup"><span data-stu-id="42374-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  

