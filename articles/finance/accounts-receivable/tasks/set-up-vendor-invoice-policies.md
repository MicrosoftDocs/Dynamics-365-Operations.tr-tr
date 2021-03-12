---
title: Satıcı fatura ilkelerini ayarlama
description: Bu konuda, satıcı fatura ilkelerinin nasıl ayarlanacağını açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79cbabba74fdb76d8fcc0553d39e0f140aacf03e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995475"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="8c547-103">Satıcı fatura ilkelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="8c547-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c547-104">Bu konuda, satıcı fatura ilkelerinin nasıl ayarlanacağını açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8c547-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="8c547-105">Satıcı faturası sayfasından bir satıcı faturası naklettiğiniz zaman ve satıcı faturası İlke ihlalleri sayfasını açtığınız zaman satıcı faturası ilkeleri çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="8c547-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="8c547-106">Ayrıca, satıcı faturası iş akışını yapılandırarak, iş akışına her fatura gönderişinizde satıcı faturası ilkelerinin çalıştırılmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8c547-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="8c547-107">Fatura kaydında veya fatura günlüğünde oluşturulmuş faturalara satıcı faturası ilkeleri uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="8c547-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="8c547-108">Fatura eşleştirme doğrulaması satıcı faturası ilkeleri kullanmaz, bunun yerine Borç hesapları parametreleri sayfasında ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="8c547-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="8c547-109">Bu kayıtta USMF demo şirketi kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="8c547-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="8c547-110">Bu adımları borç hesapları yöneticisi veya muhasebe müdürü rolü gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="8c547-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="8c547-111">Başlamadan önce Fatura eşleştirme yapılandırma anahtarının seçildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="8c547-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="8c547-112">Satıcı faturası ilkeleri oluşturmaya hazırlanın</span><span class="sxs-lookup"><span data-stu-id="8c547-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="8c547-113">**Gezinti bölmesi > Modüller > Borç hesapları > Kurulum > Borç hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8c547-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="8c547-114">**Fatura doğrulama** sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8c547-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="8c547-115">**Fatura başlığı durumunu otomatik olarak güncelleştir** onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="8c547-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="8c547-116">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-116">Select **OK**.</span></span>
5. <span data-ttu-id="8c547-117">**Uyuşmazlıkları olan faturayı deftere naklet** alanında bir seçenek belirtin.</span><span class="sxs-lookup"><span data-stu-id="8c547-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="8c547-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8c547-118">Close the page.</span></span>
7. <span data-ttu-id="8c547-119">**Gezinti bölmesi > Modüller > Borç hesapları > Politika ayarı > Satıcı faturası politikaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8c547-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="8c547-120">**Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="8c547-121">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-121">Select **Add**.</span></span>
10. <span data-ttu-id="8c547-122">Ana sayfaya dönmek için sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8c547-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="8c547-123">Satıcı faturaları için ilke kuralı türleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="8c547-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="8c547-124">**Gezinti bölmesi > Modüller > Borç hesapları > Politika ayarı > Satıcı faturası politika kural türleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8c547-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="8c547-125">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-125">Select **New**.</span></span>
3. <span data-ttu-id="8c547-126">**Kural adı** ve **Açıklama** alanlarına değer girin.</span><span class="sxs-lookup"><span data-stu-id="8c547-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="8c547-127">**Sorgu adı** alanında, açılır menü düğmesini seçerek aramayı açın, ardından istenen kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="8c547-128">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-128">Select **Save**.</span></span>
6. <span data-ttu-id="8c547-129">Ana sayfaya dönmek için sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8c547-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="8c547-130">Satıcı faturası ilkesi tanımlayın</span><span class="sxs-lookup"><span data-stu-id="8c547-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="8c547-131">**Gezinti bölmesi > Modüller > Borç hesapları > Politika ayarı > Satıcı faturası politikaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8c547-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="8c547-132">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-132">Select **New**.</span></span>
3. <span data-ttu-id="8c547-133">**Ad** ve **Açıklama** alanlarına değer girin.</span><span class="sxs-lookup"><span data-stu-id="8c547-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="8c547-134">**İlke organizasyonları** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="8c547-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="8c547-135">Ağaçta **Contoso Eğlence Sistemi Türkiye** (Contoso Entertainment System USA) seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="8c547-136">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-136">Select **Add**.</span></span>
7. <span data-ttu-id="8c547-137">**İlke kuralları** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="8c547-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="8c547-138">**İlke kuralı oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="8c547-139">**İlke kuralı açıklaması** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="8c547-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="8c547-140">**Filtre**'yi seç.</span><span class="sxs-lookup"><span data-stu-id="8c547-140">Select **Filter**.</span></span>
11. <span data-ttu-id="8c547-141">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-141">Select **Add**.</span></span> <span data-ttu-id="8c547-142">İstenen kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-142">Select the desired record.</span></span>
12. <span data-ttu-id="8c547-143">**Tablo** , **Türetilmiştablo** ve **Alan** alanlarında, açılır menülerden seçenekler seçin veya girin.</span><span class="sxs-lookup"><span data-stu-id="8c547-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="8c547-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8c547-144">Close the page.</span></span>
14. <span data-ttu-id="8c547-145">**Ölçütler** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8c547-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="8c547-146">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-146">Select **OK**.</span></span>
16. <span data-ttu-id="8c547-147">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8c547-147">Select **OK**.</span></span>
17. <span data-ttu-id="8c547-148">Ana sayfaya dönmek için sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="8c547-148">Close the pages to return to the home page.</span></span>

