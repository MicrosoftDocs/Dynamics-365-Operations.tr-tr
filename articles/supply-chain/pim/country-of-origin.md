---
title: Menşei ülke
description: Birçok kuruluş, ürünlerin belirli sertifika standartlarına uygun olmasını sağlamak için satıcılarına sertifika verir. Bu sertifikalar genellikle menşei ülkeye bağlıdır. Bu konu, bir ürünü kendi menşei ülkesine bağlamanıza ve ürün sertifikalarını izlemenize olanak sağlayan, menşei ülke özelliği hakkında bilgi sağlar.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 2eaf0057123cd2cbcad00f95038627291dada517
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007827"
---
# <a name="country-of-origin"></a><span data-ttu-id="1f13b-105">Menşei ülke</span><span class="sxs-lookup"><span data-stu-id="1f13b-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1f13b-106">Birçok kuruluş, ürünlerin belirli sertifika standartlarına uygun olmasını sağlamak için satıcılarına sertifika verir.</span><span class="sxs-lookup"><span data-stu-id="1f13b-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="1f13b-107">Bu sertifikalar genellikle menşei ülkeye bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1f13b-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="1f13b-108">Menşei ülke özelliği, bir ürünü kendi menşei ülkesine bağlamanıza ve ürün sertifikalarını izlemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="1f13b-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="1f13b-109">Menşei ülke özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="1f13b-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="1f13b-110">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1f13b-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="1f13b-111">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="1f13b-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="1f13b-112">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="1f13b-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1f13b-113">**Modül:** *Ürün bilgileri yönetimi*</span><span class="sxs-lookup"><span data-stu-id="1f13b-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="1f13b-114">**Özellik adı:** *menşei ülke yönetim özelliği*</span><span class="sxs-lookup"><span data-stu-id="1f13b-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="1f13b-115">Kaynak ve hedef ülkeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1f13b-115">Configure source and destination countries</span></span>

<span data-ttu-id="1f13b-116">Bir ürünle ilgili sertifika vermeden önce, ürünü hedef ülkesine ve menşei ülkesine bağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="1f13b-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="1f13b-117">**Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Menşei ülke \> Menşei ülke kuralları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="1f13b-118">Düzenlemek için mevcut bir ülke kurulumu seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir ülke kurulumu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1f13b-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="1f13b-119">Seçili veya yeni ülke için aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1f13b-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="1f13b-120">Alan</span><span class="sxs-lookup"><span data-stu-id="1f13b-120">Field</span></span> | <span data-ttu-id="1f13b-121">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f13b-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="1f13b-122">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="1f13b-122">Item number</span></span> | <span data-ttu-id="1f13b-123">Ürünün madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="1f13b-124">Hedef ülke</span><span class="sxs-lookup"><span data-stu-id="1f13b-124">Destination country</span></span> | <span data-ttu-id="1f13b-125">Ürünü göndereceğiniz ülkeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="1f13b-126">Menşei ülke</span><span class="sxs-lookup"><span data-stu-id="1f13b-126">Origin country</span></span> | <span data-ttu-id="1f13b-127">Ürünü göndereceğiniz kaynak ülkeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="1f13b-128">Bu kurulumun amacı, menşei ve hedef ülkelerin belirtildiği her bir parça için menşei ülkeyi ekleyebileceğiniz bir ürün reçetesi (BOM) raporu üretmeye yardımcı olmaktır.</span><span class="sxs-lookup"><span data-stu-id="1f13b-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="1f13b-129">Bu rapor, parçaların nereden geldiğini ve nereye gideceğini bütünsel bir şekilde almanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1f13b-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="1f13b-130">Satıcı sertifikalarını izleme</span><span class="sxs-lookup"><span data-stu-id="1f13b-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="1f13b-131">Satıcılara verdiğiniz sertifikaları izlemek için **Menşei ülke satıcı sertifikaları** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f13b-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="1f13b-132">Hangi sertifika belgelerini düzenleyeceğinizi ve bunları müşterilere nasıl bildireceğinize karar vermeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1f13b-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="1f13b-133">Bu özellik, sertifikalarınızı izlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="1f13b-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="1f13b-134">Ayrıca, ilgili sertifika numaralarının faturalarda, sevk irsaliyelerinde ve/veya sipariş onaylarında görünüp görünmeyeceğini seçmenize de olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="1f13b-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="1f13b-135">Sertifika bilgilerinizi ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="1f13b-136">**Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Menşei ülke \> Menşei ülke satıcı sertifikaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="1f13b-137">Düzenlemek için mevcut bir sertifika kurulumu seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir sertifika kurulumu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="1f13b-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="1f13b-138">Seçili veya yeni sertifika için aşağıdaki ayarları yapın.</span><span class="sxs-lookup"><span data-stu-id="1f13b-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="1f13b-139">Alan</span><span class="sxs-lookup"><span data-stu-id="1f13b-139">Field</span></span> | <span data-ttu-id="1f13b-140">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f13b-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="1f13b-141">Satıcı hesabı</span><span class="sxs-lookup"><span data-stu-id="1f13b-141">Vendor account</span></span> | <span data-ttu-id="1f13b-142">Sertifikanın verileceği satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="1f13b-143">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="1f13b-143">Item number</span></span> | <span data-ttu-id="1f13b-144">Sertifikanın verileceği ilgili maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="1f13b-145">Ülke/bölge</span><span class="sxs-lookup"><span data-stu-id="1f13b-145">Country/region</span></span> | <span data-ttu-id="1f13b-146">Bu sertifikayı kullanmanız gereken hedef ülke veya bölge.</span><span class="sxs-lookup"><span data-stu-id="1f13b-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="1f13b-147">Sertifika numarası</span><span class="sxs-lookup"><span data-stu-id="1f13b-147">Certificate number</span></span> | <span data-ttu-id="1f13b-148">Düzenlediğiniz sertifikanın kimlik numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="1f13b-149">Etkin</span><span class="sxs-lookup"><span data-stu-id="1f13b-149">Effective</span></span> | <span data-ttu-id="1f13b-150">Geçerli sertifikanın geçerli olduğu ilk tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="1f13b-151">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="1f13b-151">Expiration</span></span> | <span data-ttu-id="1f13b-152">Geçerli sertifikanın geçerli olduğu son tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="1f13b-153">Faturaya yazdır</span><span class="sxs-lookup"><span data-stu-id="1f13b-153">Print on invoice</span></span> | <span data-ttu-id="1f13b-154">Belirtilen tarih aralığında belirtilen ülkeye yönelik faturalara sertifika numarası yazdırmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="1f13b-155">Sevk irsaliyesine yazdır</span><span class="sxs-lookup"><span data-stu-id="1f13b-155">Print on packing slip</span></span> | <span data-ttu-id="1f13b-156">Belirtilen tarih aralığında belirtilen ülkeye yönelik sevk irsaliyelerine sertifika numarası yazdırmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="1f13b-157">Satış siparişine yazdır</span><span class="sxs-lookup"><span data-stu-id="1f13b-157">Print on sales order</span></span> | <span data-ttu-id="1f13b-158">Belirtilen tarih aralığında belirtilen ülkeye yönelik satış siparişlerine sertifika numarası yazdırmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="1f13b-159">BOM raporlarında menşei ülke ekleme</span><span class="sxs-lookup"><span data-stu-id="1f13b-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="1f13b-160">Bir ürün reçetesi raporu oluştururken, kaynak ve hedef ülkeleri belirttiğiniz her bir parça için **Menşei ülke kuralları** sayfasına bulunduğu ülkeyi dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f13b-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="1f13b-161">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1f13b-162">**Serbest bırakılan ürün ayrıntıları** sayfasını açmak için bir ürün oluşturun veya açın.</span><span class="sxs-lookup"><span data-stu-id="1f13b-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="1f13b-163">Eylem Bölmesinde, **Mühendis** sekmesindeki **BOM** gurubunda **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="1f13b-164">Eylem Bölmesi'nde görüntülenen liste sayfasında **BOM \> Yazdır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1f13b-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="1f13b-165">**Ürün reçetesi satırları** iletişim kutusunda, **Hedef ülke** alanını raporunuzda görüntülemek istediğiniz hedef ülkeye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1f13b-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="1f13b-166">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1f13b-166">Select **OK**.</span></span>

<span data-ttu-id="1f13b-167">Her bir parçanın menşei ülkesi hakkında bilgi gösteren bir rapor oluşturulur ve gösterilir.</span><span class="sxs-lookup"><span data-stu-id="1f13b-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="1f13b-168">Burada rapor için bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1f13b-168">Here is an example of the report.</span></span>

<span data-ttu-id="1f13b-169">![Menşei ülke raporu](media/country-of-origin-report.png "Menşei ülke raporu")</span><span class="sxs-lookup"><span data-stu-id="1f13b-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
