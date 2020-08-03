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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596286"
---
# <a name="country-of-origin"></a><span data-ttu-id="06a50-105">Menşei ülke</span><span class="sxs-lookup"><span data-stu-id="06a50-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06a50-106">Birçok kuruluş, ürünlerin belirli sertifika standartlarına uygun olmasını sağlamak için satıcılarına sertifika verir.</span><span class="sxs-lookup"><span data-stu-id="06a50-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="06a50-107">Bu sertifikalar genellikle menşei ülkeye bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="06a50-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="06a50-108">Menşei ülke özelliği, bir ürünü kendi menşei ülkesine bağlamanıza ve ürün sertifikalarını izlemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="06a50-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="06a50-109">Kaynak ve hedef ülkeleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="06a50-109">Configure source and destination countries</span></span>

<span data-ttu-id="06a50-110">Bir ürünle ilgili sertifika vermeden önce, ürünü hedef ülkesine ve menşei ülkesine bağlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="06a50-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="06a50-111">**Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Menşei ülke \> Menşei ülke kuralları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="06a50-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="06a50-112">Düzenlemek için mevcut bir ülke kurulumu seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir ülke kurulumu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="06a50-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="06a50-113">Seçili veya yeni ülke için aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="06a50-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="06a50-114">Alan</span><span class="sxs-lookup"><span data-stu-id="06a50-114">Field</span></span> | <span data-ttu-id="06a50-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="06a50-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="06a50-116">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="06a50-116">Item number</span></span> | <span data-ttu-id="06a50-117">Ürünün madde numarasını seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="06a50-118">Hedef ülke</span><span class="sxs-lookup"><span data-stu-id="06a50-118">Destination country</span></span> | <span data-ttu-id="06a50-119">Ürünü göndereceğiniz ülkeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="06a50-120">Menşei ülke</span><span class="sxs-lookup"><span data-stu-id="06a50-120">Origin country</span></span> | <span data-ttu-id="06a50-121">Ürünü göndereceğiniz kaynak ülkeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="06a50-122">Bu kurulumun amacı, menşei ve hedef ülkelerin belirtildiği her bir parça için menşei ülkeyi ekleyebileceğiniz bir ürün reçetesi (BOM) raporu üretmeye yardımcı olmaktır.</span><span class="sxs-lookup"><span data-stu-id="06a50-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="06a50-123">Bu rapor, parçaların nereden geldiğini ve nereye gideceğini bütünsel bir şekilde almanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="06a50-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="06a50-124">Satıcı sertifikalarını izleme</span><span class="sxs-lookup"><span data-stu-id="06a50-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="06a50-125">Satıcılara verdiğiniz sertifikaları izlemek için **Menşei ülke satıcı sertifikaları** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06a50-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="06a50-126">Hangi sertifika belgelerini düzenleyeceğinizi ve bunları müşterilere nasıl bildireceğinize karar vermeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="06a50-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="06a50-127">Bu özellik, sertifikalarınızı izlemenize yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="06a50-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="06a50-128">Ayrıca, ilgili sertifika numaralarının faturalarda, sevk irsaliyelerinde ve/veya sipariş onaylarında görünüp görünmeyeceğini seçmenize de olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="06a50-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="06a50-129">Sertifika bilgilerinizi ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="06a50-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="06a50-130">**Ürün bilgileri yönetimi \> Kurulum \> Ürün uyumluluğu \> Menşei ülke \> Menşei ülke satıcı sertifikaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="06a50-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="06a50-131">Düzenlemek için mevcut bir sertifika kurulumu seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir sertifika kurulumu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="06a50-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="06a50-132">Seçili veya yeni sertifika için aşağıdaki ayarları yapın.</span><span class="sxs-lookup"><span data-stu-id="06a50-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="06a50-133">Alan</span><span class="sxs-lookup"><span data-stu-id="06a50-133">Field</span></span> | <span data-ttu-id="06a50-134">Tanım</span><span class="sxs-lookup"><span data-stu-id="06a50-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="06a50-135">Satıcı hesabı</span><span class="sxs-lookup"><span data-stu-id="06a50-135">Vendor account</span></span> | <span data-ttu-id="06a50-136">Sertifikanın verileceği satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="06a50-137">Madde kodu</span><span class="sxs-lookup"><span data-stu-id="06a50-137">Item number</span></span> | <span data-ttu-id="06a50-138">Sertifikanın verileceği ilgili maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="06a50-139">Ülke/bölge</span><span class="sxs-lookup"><span data-stu-id="06a50-139">Country/region</span></span> | <span data-ttu-id="06a50-140">Bu sertifikayı kullanmanız gereken hedef ülke veya bölge.</span><span class="sxs-lookup"><span data-stu-id="06a50-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="06a50-141">Sertifika numarası</span><span class="sxs-lookup"><span data-stu-id="06a50-141">Certificate number</span></span> | <span data-ttu-id="06a50-142">Düzenlediğiniz sertifikanın kimlik numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="06a50-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="06a50-143">Etkin</span><span class="sxs-lookup"><span data-stu-id="06a50-143">Effective</span></span> | <span data-ttu-id="06a50-144">Geçerli sertifikanın geçerli olduğu ilk tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="06a50-145">Bitiş tarihi</span><span class="sxs-lookup"><span data-stu-id="06a50-145">Expiration</span></span> | <span data-ttu-id="06a50-146">Geçerli sertifikanın geçerli olduğu son tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="06a50-147">Faturaya yazdır</span><span class="sxs-lookup"><span data-stu-id="06a50-147">Print on invoice</span></span> | <span data-ttu-id="06a50-148">Belirtilen tarih aralığında belirtilen ülkeye yönelik faturalara sertifika numarası yazdırmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="06a50-149">Sevk irsaliyesine yazdır</span><span class="sxs-lookup"><span data-stu-id="06a50-149">Print on packing slip</span></span> | <span data-ttu-id="06a50-150">Belirtilen tarih aralığında belirtilen ülkeye yönelik sevk irsaliyelerine sertifika numarası yazdırmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="06a50-151">Satış siparişine yazdır</span><span class="sxs-lookup"><span data-stu-id="06a50-151">Print on sales order</span></span> | <span data-ttu-id="06a50-152">Belirtilen tarih aralığında belirtilen ülkeye yönelik satış siparişlerine sertifika numarası yazdırmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="06a50-153">BOM raporlarında menşei ülke ekleme</span><span class="sxs-lookup"><span data-stu-id="06a50-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="06a50-154">Bir ürün reçetesi raporu oluştururken, kaynak ve hedef ülkeleri belirttiğiniz her bir parça için **Menşei ülke kuralları** sayfasına bulunduğu ülkeyi dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06a50-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="06a50-155">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="06a50-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="06a50-156">**Serbest bırakılan ürün ayrıntıları** sayfasını açmak için bir ürün oluşturun veya açın.</span><span class="sxs-lookup"><span data-stu-id="06a50-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="06a50-157">Eylem Bölmesinde, **Mühendis** sekmesindeki **BOM** gurubunda **Tasarımcı**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="06a50-158">Eylem Bölmesi'nde görüntülenen liste sayfasında **BOM \> Yazdır**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="06a50-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="06a50-159">**Ürün reçetesi satırları** iletişim kutusunda, **Hedef ülke** alanını raporunuzda görüntülemek istediğiniz hedef ülkeye ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="06a50-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="06a50-160">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="06a50-160">Select **OK**.</span></span>

<span data-ttu-id="06a50-161">Her bir parçanın menşei ülkesi hakkında bilgi gösteren bir rapor oluşturulur ve gösterilir.</span><span class="sxs-lookup"><span data-stu-id="06a50-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="06a50-162">Burada rapor için bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="06a50-162">Here is an example of the report.</span></span>

<span data-ttu-id="06a50-163">![Menşei ülke raporu](media/country-of-origin-report.png "Menşei ülke raporu")</span><span class="sxs-lookup"><span data-stu-id="06a50-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
