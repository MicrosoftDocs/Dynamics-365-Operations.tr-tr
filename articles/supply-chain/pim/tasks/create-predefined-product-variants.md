---
title: Önceden tanımlanmış ürün çeşitleri oluşturma
description: Bu prosedürde ürün boyutları kombinasyonları kullanılarak bir ana ürün için ürün seçeneklerinin nasıl oluşturulacağı adım adım açıklanmıştır.
author: t-benebo
ms.date: 08/09/2022
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
ms.openlocfilehash: a26439b8c7346cdce2b4c9804493fea94c29ac31
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335930"
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

*Varyant önerileri sayfası iyileştirmeleri* özelliği, yüksek sayıda ürün boyutu kombinasyonu olan şirketler için performans ve kullanılabilirlik sorunlarını gidermek amacıyla **Varyant önerileri** sayfasını geliştirir. Varyant önerileri oluşturulacak ürün boyut değerlerini seçmeye yönelik gelişmiş süreç, ilgili ürün varyantları kümesini tanımlama ve serbest bırakma işlemini hızlandırır ve kolaylaştırır.

Bu özellikle birlikte aşağıdaki iyileştirmeler sağlanır:

- **Varyant önerilerinin ertelenmiş şekilde oluşturulması:** **Varyant önerileri** sayfası, artık ilk açtığınızda öneriler göstermez. Bunun yerine, gereksinim duyacağınız değerleri seçmeniz ve birleşimleri oluşturmak için **Öner** düğmesini seçmeniz gerekir. Bu, işlemi daha görünür ve etkileşimli hale getirir.
- **Boyut değerleri seçimi:** Birçok boyut değerleriniz olduğunda, genellikle bunlardan yalnızca birkaçını içeren (örneğin, yeni bir renk veya stil kümesi oluştururken) varyant önerileri oluşturmak isteyebilirsiniz. Bu geliştirilmiş tasarım sayesinde, ürün varyantı önerileri oluşturmak istediğiniz boyut değerlerini seçebilirsiniz. Bu, önerilen varyantların ilgi derecesini büyük ölçüde artırır ve hem sistem performansını hem de kullanıcı üretkenliğini artırır.

### <a name="turn-the-variant-suggestions-page-improvements-feature-on-or-off"></a>Varyant önerileri sayfa iyileştirmeleri özelliğini açma veya kapatma

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Supply Chain Management sürüm 10.0.25 itibarıyla özellik varsayılan olarak açıktır. Supply Chain Management sürüm 10.0.29 itibarıyla, özellik zorunludur ve kapatılamaz. 10.0.29 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Çeşit önerileri sayfa geliştirmeleri* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

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
