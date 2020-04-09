---
title: Özel durumları araştırma veya giderme
description: Satıcı faturası sayfasından bir satıcı faturası naklettiğiniz zaman ve satıcı faturası İlke ihlalleri sayfasını açtığınız zaman satıcı faturası ilkeleri çalıştırılır.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 995d68f6224b6dfbb1928c907ad991b86fc47668
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140364"
---
# <a name="research-or-resolve-exceptions"></a><span data-ttu-id="de62a-103">Özel durumları araştırma veya giderme</span><span class="sxs-lookup"><span data-stu-id="de62a-103">Research or resolve exceptions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de62a-104">Satıcı faturası sayfasından bir satıcı faturası naklettiğiniz zaman ve satıcı faturası İlke ihlalleri sayfasını açtığınız zaman satıcı faturası ilkeleri çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="de62a-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="de62a-105">Ayrıca, satıcı faturası iş akışını yapılandırarak, iş akışına her fatura gönderişinizde satıcı faturası ilkelerinin çalıştırılmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="de62a-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="de62a-106">Fatura kaydında veya fatura günlüğünde oluşturulmuş faturalara satıcı faturası ilkeleri uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="de62a-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="de62a-107">Fatura eşleştirme doğrulaması satıcı faturası ilkeleri kullanmaz, bunun yerine Borç hesapları parametreleri sayfasında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="de62a-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="de62a-108">Bu kayıtta USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="de62a-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="de62a-109">Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="de62a-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="de62a-110">Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="de62a-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="de62a-111">Satıcı faturası ilkeleri oluşturmaya hazırlanın</span><span class="sxs-lookup"><span data-stu-id="de62a-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="de62a-112">Borç hesapları > Kurulum > Borç hesapları parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="de62a-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="de62a-113">Fatura doğrulama sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="de62a-114">Fatura başlığı durumunu otomatik olarak güncelleştir onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="de62a-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="de62a-115">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="de62a-115">Click OK.</span></span>
5. <span data-ttu-id="de62a-116">Uyuşmazlıkları olan faturayı deftere naklet alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="de62a-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="de62a-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="de62a-117">Close the page.</span></span>
7. <span data-ttu-id="de62a-118">Borç hesapları > İlke ayarı > Satıcı fatura ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="de62a-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="de62a-119">Parametreler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-119">Click Parameters.</span></span>
9. <span data-ttu-id="de62a-120">Ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-120">Click btnAdd.</span></span>
10. <span data-ttu-id="de62a-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="de62a-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="de62a-122">Satıcı faturaları için ilke kuralı türleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="de62a-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="de62a-123">Borç hesapları > İlke ayarı > Satıcı faturası ilke kuralı türleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="de62a-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="de62a-124">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-124">Click New.</span></span>
3. <span data-ttu-id="de62a-125">Kural adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="de62a-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="de62a-126">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="de62a-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="de62a-127">Sorgu adı alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="de62a-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="de62a-128">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="de62a-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="de62a-129">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="de62a-130">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-130">Click Save.</span></span>
9. <span data-ttu-id="de62a-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="de62a-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="de62a-132">Satıcı faturası ilkesi tanımlayın</span><span class="sxs-lookup"><span data-stu-id="de62a-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="de62a-133">Borç hesapları > İlke ayarı > Satıcı fatura ilkeleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="de62a-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="de62a-134">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-134">Click New.</span></span>
3. <span data-ttu-id="de62a-135">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="de62a-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="de62a-136">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="de62a-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="de62a-137">İlke organizasyonları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="de62a-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="de62a-138">Ağaçta "Contoso Eğlence Sistemi Türkiye"yi (Contoso Entertainment System USA) seçin.</span><span class="sxs-lookup"><span data-stu-id="de62a-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="de62a-139">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="de62a-139">Click Add.</span></span>
8. <span data-ttu-id="de62a-140">İlke kuralları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="de62a-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="de62a-141">İlke kuralı oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="de62a-142">İlke kuralı açıklaması alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="de62a-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="de62a-143">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-143">Click Filter.</span></span>
12. <span data-ttu-id="de62a-144">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="de62a-144">Click Add.</span></span>
13. <span data-ttu-id="de62a-145">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="de62a-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="de62a-146">Tablo alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="de62a-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="de62a-147">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="de62a-148">Türetilen tablo alanında, açılır menü düğmesine tıklayarak açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="de62a-149">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="de62a-150">Alan alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="de62a-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="de62a-151">Alan alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="de62a-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="de62a-152">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="de62a-152">Close the page.</span></span>
21. <span data-ttu-id="de62a-153">Ölçütler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="de62a-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="de62a-154">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-154">Click OK.</span></span>
23. <span data-ttu-id="de62a-155">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="de62a-155">Click OK.</span></span>
24. <span data-ttu-id="de62a-156">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="de62a-156">Close the page.</span></span>
25. <span data-ttu-id="de62a-157">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="de62a-157">Close the page.</span></span>

