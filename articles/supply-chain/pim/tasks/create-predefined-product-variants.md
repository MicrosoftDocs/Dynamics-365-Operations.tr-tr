---
title: Önceden tanımlanmış ürün çeşitleri oluşturma
description: Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır.
author: t-benebo
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
ms.openlocfilehash: 6f78441445baecba279f96eb3935d9ebbb4ff03f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021920"
---
# <a name="predefined-product-variants"></a>Önceden tanımlanmış ürün varyantları

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Örnek senaryo: Önceden tanımlanmış ürün varyantları oluşturma

Bu örnek senaryo, ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün varyantlarının nasıl oluşturulacağını adım adım açıklar.

### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu senaryoyu izlemek için, burada önerilen değerleri kullanarak demo verilerinin yüklenmiş olması ve *USMF* tüzel kişiliğini kullanmanız gerekir.

### <a name="step-1-create-a-product-master"></a>1. Adım: Ana ürün oluşturma

Ana ürün oluşturmak için:

1. **Ürün bilgi yönetimi > Ürünler > Ana ürünler**'e gidin.
1. **Yeni**'yi seçin.
1. **Ürün numarası** alanında zaten bir numara yoksa bir değer girin. Bu, yalnızca bu alan için numara sırası ayarlanmadıysa gereklidir.
1. **Ürün adı** alanına bir ad girin.
1. **Ürün boyut grubu** alanında, ürün boyut grubu *SizeCol* (Boyut ve Renk) seçeneğini belirleyin.
1. Yeni ürün yöneticisi oluşturmak ve açmak için **Tamam**'ı seçin.

### <a name="step-2-add-product-dimensions"></a>2. Adım: Ürün boyutları ekleme

Bu örnekte ürün boyutlarının nasıl el ile girileceği gösterilmiştir. Ayrıca, kullanmak istediğiniz ürün boyutu değerlerini içeren boyut, renk veya tarz grubunu da seçebilirsiniz.

Ürün boyutları eklemek için:

1. Yeni ana ürününüz hâlâ açıkken Eylem Bölmesi'nde **Ürün boyutları**'nı seçin.
1. Izgaraya satır eklemek için **Boyut** sekmesini açın ve araç çubuğunda **Yeni**'yi seçin. Yeni satır için aşağıdaki ayarları yapın:
    - **Boyut**: Bir boyut değeri seçin.
    - **Ad**: Boyut için bir ad girin.
1. Araç çubuğunda **Yeni**'yi seçin ve yeni bir **Boyut** ve **Ad** kullanarak ızgaraya ikinci bir boyut ekleyin.
1. Izgaraya satır eklemek için **Renk** sekmesini açın ve araç çubuğunda **Yeni**'yi seçin. Yeni satır için aşağıdaki ayarları yapın:
    - **Renk:** Bir renk değeri seçin.
    - **Ad**: Renk için bir ad girin.
1. Araç çubuğunda **Yeni**'yi seçin ve yeni bir **Renk** ve **Ad** kullanarak ızgaraya ikinci bir renk ekleyin.
1. **Kaydet**'i seçin.
1. Sayfayı kapatın ve yeni ana ürününüze dönün.

### <a name="step-3-generate-product-variants"></a>3. Adım: Ürün varyantları oluşturma

> [!NOTE]
> Bu bölümde, *Varyant önerileri sayfası geliştirmeleri* özelliği etkin olmadığında ürün varyantlarını nasıl oluşturacağınız anlatılmaktadır. Bu özellik kullanılabilir olduğunda ürün varyantlarının nasıl oluşturulacağı ile ilgili ayrıntılar için sonraki bölüme bakın.

Ürün varyantları oluşturmak için:

1. Yeni ana ürününüz hâlâ açıkken Eylem Bölmesi'nde **Ürün varyantları**'nı seçin.
1. Eylem Bölmesi'nde **Varyant önerileri**'ni seçin.
1. Sistem, ürün için tanımladığınız boyutların ve renklerin tüm olası birleşimlerine sahip bir liste oluşturur. Araç çubuğundan **Tümünü Seç**'i seçin.
    - Bu örnekte, olası tüm varyantları seçin. Yalnızca olası ürün boyut birleşimlerinin bir alt kümesini kullanmak istiyorsanız yalnızca dilediğiniz onay kutularını gerektiği şekilde seçin.  
1. **Oluştur**'u seçin.
1. **Kaydet**'i seçin.

## <a name="improved-variant-suggestions"></a>Geliştirilmiş varyant önerileri

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

*Varyant önerileri sayfası iyileştirmeleri* özelliği, yüksek sayıda ürün boyutu kombinasyonu olan şirketler için performans ve kullanılabilirlik sorunlarını gidermek amacıyla **Varyant önerileri** sayfasını geliştirir. Varyant önerileri oluşturulacak ürün boyut değerlerini seçmeye yönelik gelişmiş süreç, ilgili ürün varyantları kümesini tanımlama ve serbest bırakma işlemini hızlandırır ve kolaylaştırır.

Bu özellikle birlikte aşağıdaki iyileştirmeler sağlanır:

- **Varyant önerilerinin ertelenmiş şekilde oluşturulması:** **Varyant önerileri** sayfası, artık ilk açtığınızda öneriler göstermez. Bunun yerine, gereksinim duyacağınız değerleri seçmeniz ve birleşimleri oluşturmak için **Öner** düğmesini seçmeniz gerekir. Bu, işlemi daha görünür ve etkileşimli hale getirir.
- **Boyut değerleri seçimi:** Birçok boyut değerleriniz olduğunda, genellikle bunlardan yalnızca birkaçını içeren (örneğin, yeni bir renk veya stil kümesi oluştururken) varyant önerileri oluşturmak isteyebilirsiniz. Bu geliştirilmiş tasarım sayesinde, ürün varyantı önerileri oluşturmak istediğiniz boyut değerlerini seçebilirsiniz. Bu, önerilen varyantların ilgi derecesini büyük ölçüde artırır ve hem sistem performansını hem de kullanıcı üretkenliğini artırır.

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a>Varyant önerileri sayfa iyileştirmeleri özelliğini etkinleştirme

*Varyant önerileri sayfa iyileştirmeleri* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ürün bilgileri yönetimi*
- **Özellik adı**: *Varyant önerileri sayfa iyileştirmeleri*

### <a name="work-with-the-improved-variant-suggestions"></a>İyileştirilmiş varyant önerileriyle çalışma

*Varyant önerileri sayfası geliştirmeleri* özelliği etkin olduğunda ürün varyantlarını oluşturmak için:

1. Bir ana ürün açın veya oluşturun ve önceki bölümde açıklandığı gibi bu ana ürüne gerekli ürün boyutlarını ekleyin.
1. Ana ürününüz açıkken Eylem Bölmesi'nde **Ürün varyantları**'nı seçin.
1. Eylem Bölmesi'nde **Varyant önerileri**'ni seçin.
1. Her bir boyut için kullanmak istediğiniz değerleri seçin.
1. Üst araç çubuğunda, **Öner**'i seçin.
1. Sistem, seçtiğiniz boyutların ve renklerin tüm olası birleşimlerine sahip bir liste oluşturur. **Önerilen varyantlar** hızlı sekmesinde, kullanmak istediğiniz her ürün boyutu birleşiminin onay kutusunu işaretleyin veya tümünü seçmek için araç çubuğundan **Tümünü Seç**'i seçin.  
1. Varyantları geçerli ana ürüne eklemek için **Oluştur** seçeneğini belirleyin.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
