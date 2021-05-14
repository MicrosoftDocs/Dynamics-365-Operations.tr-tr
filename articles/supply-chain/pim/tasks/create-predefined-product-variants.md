---
title: Önceden tanımlanmış ürün çeşitleri oluşturma
description: Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır.
author: t-benebo
manager: tfehr
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acd2e3f1464dfed09ee24764270b06970b747d7c
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938214"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="774ca-103">Önceden tanımlanmış ürün varyantları</span><span class="sxs-lookup"><span data-stu-id="774ca-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="774ca-104">Örnek senaryo: Önceden tanımlanmış ürün varyantları oluşturma</span><span class="sxs-lookup"><span data-stu-id="774ca-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="774ca-105">Bu örnek senaryo, ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün varyantlarının nasıl oluşturulacağını adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="774ca-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="774ca-106">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="774ca-106">Make demo data available</span></span>

<span data-ttu-id="774ca-107">Bu senaryoyu izlemek için, burada önerilen değerleri kullanarak demo verilerinin yüklenmiş olması ve *USMF* tüzel kişiliğini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="774ca-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="774ca-108">1. Adım: Ana ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="774ca-108">Step 1: Create a product master</span></span>

<span data-ttu-id="774ca-109">Ana ürün oluşturmak için:</span><span class="sxs-lookup"><span data-stu-id="774ca-109">To create a product master:</span></span>

1. <span data-ttu-id="774ca-110">**Ürün bilgi yönetimi > Ürünler > Ana ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="774ca-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="774ca-111">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-111">Select **New**.</span></span>
1. <span data-ttu-id="774ca-112">**Ürün numarası** alanında zaten bir numara yoksa bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="774ca-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="774ca-113">Bu, yalnızca bu alan için numara sırası ayarlanmadıysa gereklidir.</span><span class="sxs-lookup"><span data-stu-id="774ca-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="774ca-114">**Ürün adı** alanına bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="774ca-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="774ca-115">**Ürün boyut grubu** alanında, ürün boyut grubu *SizeCol* (Boyut ve Renk) seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="774ca-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="774ca-116">Yeni ürün yöneticisi oluşturmak ve açmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="774ca-117">2. Adım: Ürün boyutları ekleme</span><span class="sxs-lookup"><span data-stu-id="774ca-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="774ca-118">Bu örnekte ürün boyutlarının nasıl el ile girileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="774ca-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="774ca-119">Ayrıca, kullanmak istediğiniz ürün boyutu değerlerini içeren boyut, renk veya tarz grubunu da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="774ca-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="774ca-120">Ürün boyutları eklemek için:</span><span class="sxs-lookup"><span data-stu-id="774ca-120">To add product dimensions:</span></span>

1. <span data-ttu-id="774ca-121">Yeni ana ürününüz hâlâ açıkken Eylem Bölmesi'nde **Ürün boyutları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="774ca-122">Izgaraya satır eklemek için **Boyut** sekmesini açın ve araç çubuğunda **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="774ca-123">Yeni satır için aşağıdaki ayarları yapın:</span><span class="sxs-lookup"><span data-stu-id="774ca-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="774ca-124">**Boyut**: Bir boyut değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="774ca-125">**Ad**: Boyut için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="774ca-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="774ca-126">Araç çubuğunda **Yeni**'yi seçin ve yeni bir **Boyut** ve **Ad** kullanarak ızgaraya ikinci bir boyut ekleyin.</span><span class="sxs-lookup"><span data-stu-id="774ca-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="774ca-127">Izgaraya satır eklemek için **Renk** sekmesini açın ve araç çubuğunda **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="774ca-128">Yeni satır için aşağıdaki ayarları yapın:</span><span class="sxs-lookup"><span data-stu-id="774ca-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="774ca-129">**Renk:** Bir renk değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="774ca-130">**Ad**: Renk için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="774ca-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="774ca-131">Araç çubuğunda **Yeni**'yi seçin ve yeni bir **Renk** ve **Ad** kullanarak ızgaraya ikinci bir renk ekleyin.</span><span class="sxs-lookup"><span data-stu-id="774ca-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="774ca-132">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-132">Select **Save**.</span></span>
1. <span data-ttu-id="774ca-133">Sayfayı kapatın ve yeni ana ürününüze dönün.</span><span class="sxs-lookup"><span data-stu-id="774ca-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="774ca-134">3. Adım: Ürün varyantları oluşturma</span><span class="sxs-lookup"><span data-stu-id="774ca-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="774ca-135">Bu bölümde, *Varyant önerileri sayfası geliştirmeleri* özelliği etkin olmadığında ürün varyantlarını nasıl oluşturacağınız anlatılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="774ca-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="774ca-136">Bu özellik kullanılabilir olduğunda ürün varyantlarının nasıl oluşturulacağı ile ilgili ayrıntılar için sonraki bölüme bakın.</span><span class="sxs-lookup"><span data-stu-id="774ca-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="774ca-137">Ürün varyantları oluşturmak için:</span><span class="sxs-lookup"><span data-stu-id="774ca-137">To generate product variants:</span></span>

1. <span data-ttu-id="774ca-138">Yeni ana ürününüz hâlâ açıkken Eylem Bölmesi'nde **Ürün varyantları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="774ca-139">Eylem Bölmesi'nde **Varyant önerileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="774ca-140">Sistem, ürün için tanımladığınız boyutların ve renklerin tüm olası birleşimlerine sahip bir liste oluşturur.</span><span class="sxs-lookup"><span data-stu-id="774ca-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="774ca-141">Araç çubuğundan **Tümünü Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="774ca-142">Bu örnekte, olası tüm varyantları seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="774ca-143">Yalnızca olası ürün boyut birleşimlerinin bir alt kümesini kullanmak istiyorsanız yalnızca dilediğiniz onay kutularını gerektiği şekilde seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="774ca-144">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-144">Select **Create**.</span></span>
1. <span data-ttu-id="774ca-145">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="774ca-146">Geliştirilmiş varyant önerileri</span><span class="sxs-lookup"><span data-stu-id="774ca-146">Improved variant suggestions</span></span>

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

<span data-ttu-id="774ca-147">*Varyant önerileri sayfası iyileştirmeleri* özelliği, yüksek sayıda ürün boyutu kombinasyonu olan şirketler için performans ve kullanılabilirlik sorunlarını gidermek amacıyla **Varyant önerileri** sayfasını geliştirir.</span><span class="sxs-lookup"><span data-stu-id="774ca-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="774ca-148">Varyant önerileri oluşturulacak ürün boyut değerlerini seçmeye yönelik gelişmiş süreç, ilgili ürün varyantları kümesini tanımlama ve serbest bırakma işlemini hızlandırır ve kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="774ca-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="774ca-149">Bu özellikle birlikte aşağıdaki iyileştirmeler sağlanır:</span><span class="sxs-lookup"><span data-stu-id="774ca-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="774ca-150">**Varyant önerilerinin ertelenmiş şekilde oluşturulması:** **Varyant önerileri** sayfası, artık ilk açtığınızda öneriler göstermez.</span><span class="sxs-lookup"><span data-stu-id="774ca-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="774ca-151">Bunun yerine, gereksinim duyacağınız değerleri seçmeniz ve birleşimleri oluşturmak için **Öner** düğmesini seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="774ca-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="774ca-152">Bu, işlemi daha görünür ve etkileşimli hale getirir.</span><span class="sxs-lookup"><span data-stu-id="774ca-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="774ca-153">**Boyut değerleri seçimi:** Birçok boyut değerleriniz olduğunda, genellikle bunlardan yalnızca birkaçını içeren (örneğin, yeni bir renk veya stil kümesi oluştururken) varyant önerileri oluşturmak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="774ca-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="774ca-154">Bu geliştirilmiş tasarım sayesinde, ürün varyantı önerileri oluşturmak istediğiniz boyut değerlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="774ca-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="774ca-155">Bu, önerilen varyantların ilgi derecesini büyük ölçüde artırır ve hem sistem performansını hem de kullanıcı üretkenliğini artırır.</span><span class="sxs-lookup"><span data-stu-id="774ca-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="774ca-156">Varyant önerileri sayfa iyileştirmeleri özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="774ca-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="774ca-157">*Varyant önerileri sayfa iyileştirmeleri* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="774ca-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="774ca-158">Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="774ca-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="774ca-159">**Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:</span><span class="sxs-lookup"><span data-stu-id="774ca-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="774ca-160">**Modül:** *Ürün bilgileri yönetimi*</span><span class="sxs-lookup"><span data-stu-id="774ca-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="774ca-161">**Özellik adı**: *Varyant önerileri sayfa iyileştirmeleri*</span><span class="sxs-lookup"><span data-stu-id="774ca-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="774ca-162">İyileştirilmiş varyant önerileriyle çalışma</span><span class="sxs-lookup"><span data-stu-id="774ca-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="774ca-163">*Varyant önerileri sayfası geliştirmeleri* özelliği etkin olduğunda ürün varyantlarını oluşturmak için:</span><span class="sxs-lookup"><span data-stu-id="774ca-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="774ca-164">Bir ana ürün açın veya oluşturun ve önceki bölümde açıklandığı gibi bu ana ürüne gerekli ürün boyutlarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="774ca-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="774ca-165">Ana ürününüz açıkken Eylem Bölmesi'nde **Ürün varyantları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="774ca-166">Eylem Bölmesi'nde **Varyant önerileri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="774ca-167">Her bir boyut için kullanmak istediğiniz değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="774ca-168">Üst araç çubuğunda, **Öner**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="774ca-169">Sistem, seçtiğiniz boyutların ve renklerin tüm olası birleşimlerine sahip bir liste oluşturur.</span><span class="sxs-lookup"><span data-stu-id="774ca-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="774ca-170">**Önerilen varyantlar** hızlı sekmesinde, kullanmak istediğiniz her ürün boyutu birleşiminin onay kutusunu işaretleyin veya tümünü seçmek için araç çubuğundan **Tümünü Seç**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="774ca-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="774ca-171">Varyantları geçerli ana ürüne eklemek için **Oluştur** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="774ca-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
