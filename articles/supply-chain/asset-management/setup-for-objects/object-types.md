---
title: Varlık türleri
description: Bu konuda Varlık Yönetimi'nde varlık türleri oluşturma işlemi açıklanmaktadır. Ayrıca, varlık türlerine ilişkin öğeler de açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783662"
---
# <a name="asset-types"></a>Varlık türleri

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Bu konu varlık türlerinin nasıl oluşturulacağını açıklar. Ayrıca, varlık türlerine ilişkin öğeler de açıklanmaktadır. Varlık türleri varlıklar için genel kategoriler olarak kullanılır. Örnekler arasında CNC makineleri, ölçüm ekipmanları ve kamyonlar bulunmaktadır. Varlık türleri bir varlık için seçilebilecek iş türlerini (bakım görevleri), varlık yaşam döngüsü durumlarını, varlık ölçümlerini, varlık özniteliklerini, koşul değerlendirme şablonlarını ve varlık modellerini yönetmek için kullanılır. Bir varlık oluşturduğunuzda varlık türünü belirtmeniz gerekir.

Her varlık türü için, varlık türü kurulumu varyasyonları oluşturulabilir. Örneğin, **Kamyonlar**adlı bir varlık türünüz varsa, bu varlık türünün farklı varlık üreticileri ve varlık modelleri için varyasyonlarını oluşturabilirsiniz. Her varlık türü kurulumuna gerekli yedek parçaları ve bakım planlarını ekleyebilirsiniz.

İlk olarak, gerekli varlık türlerini ayarlayın. Ardından, varlık türleriyle ilişkilendirilmesi gereken varlık modellerini oluşturun. Son olarak, **Varlık türü varsayılanları** sayfasında, ekipmanınız için gerekli olan tüm varlık türleri varyasyonlarını oluşturun.

## <a name="create-an-asset-type"></a>Varlık türü oluşturma

1. **Varlık yönetimi** \> **Kurulum** \> **Varlık türleri** \> **Varlık türleri**'ni seçin.
2. Bir varlık türü oluşturmak için **Yeni**'yi seçin.
3. **Varlık türü** alanına bir varlık türü kodu girin.
4. **Ad** alanına, bir ad girin.
5. **Varlık yaşam döngüsü modeli** alanında bir varlık yaşam döngüsü modeli seçin. Varlık yaşam döngüsü durumları ve varlık yaşam döngüsü modelleri hakkında daha fazla bilgi için bkz. [Varlık yaşam döngüsü durumları](object-stages.md).
6. Özetlenen temel performans göstergesi (KPI) değerlerinin bu varlık türüne sahip varlıklar için hesaplanması gerekiyorsa **Toplam** seçeneğini **Evet** olarak ayarlayın.
7. **Kaydet**'i seçin.
8. **İş türleri** hızlı sekmesinde, varlık türüyle ilişkili olması gereken iş türlerini seçin:

    - Bir iş türü seçmek için türü **Kalan iş türleri** alanında seçin ve daha sonra sağ ok düğmesini ![Sağ ok düğmesi](media/29-setup-for-objects.png) seçerek **Seçili iş türleri** bölümüne taşıyın.
    - Tüm kullanılabilir iş türlerini seçmek için ![Tüm okları ilerlet](media/30-setup-for-objects.png) düğmesini seçin. Tüm iş türleri **Kalan iş türleri** alanından **Seçili iş türleri** alanına aktarılır.
    - İş türü seçimini iptal etmek için türü **Seçili iş türleri** alanında seçin ve daha sonra sol ok düğmesini ![Sol ok düğmesi](media/31-setup-for-objects.png) seçerek **Kalan iş türleri** bölümüne taşıyın.

9. Ayrıca, varlık türüyle ilişkilendirilmesi gereken varlık ölçülerini de seçebilirsiniz. **Varlık ölçüleri** hızlı sekmesinde, adım 8'de iş türleri için açıklanan yöntemleri kullanarak seçimlerinizi yapın. Varlık ölçüleri kurulumu hakkında daha fazla bilgi için bkz. [Bakım yapılan varlık ölçümü](counters.md)
10. Ayrıca, varlık türüyle ilişkilendirilmesi gereken öznitelik türlerini de seçebilirsiniz. **Öznitelik türleri** hızlı sekmesinde, adım 8'de iş türleri için açıklanan yöntemleri kullanarak seçimlerinizi yapın. Ardından, tercih edilen öznitelik türleri sırasını oluşturmak için **Seçili öznitelik türleri** alanında bir öznitelik türü seçin ve bunu taşımak için yukarı ok ve aşağı ok düğmelerini kullanın. Öznitelik türleri sırası bu varlık türünü kullanan varlıklarda gösterilir. Varlık öznitelikleri hakkında daha fazla bilgi için bkz. [Bakım öznitelik türleri](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > **Öznitelik türleri** hızlı sekmesinde yeni öznitelik türleri eklediğinizde, varolan varlıklar otomatik olarak bu bilgilerle güncelleştirilir.

11. Ayrıca, varlık türüyle ilişkilendirilmesi gereken koşul değerlendirmesi şablonlarını da seçebilirsiniz. **Koşul değerlendirmeleri** hızlı sekmesinde, adım 8'de iş türleri için açıklanan yöntemleri kullanarak seçimlerinizi yapın. Koşul değerlendirme şablonları ve kayıtları hakkında daha fazla bilgi için bkz. [Koşul değerlendirmesi](../setup-for-objects/condition-assessment.md).
12. **Varlık modeli** hızlı sekmesi, seçili varlık türünde ayarlanan tüm varlık üreticileri ve modelleri kombinasyonlarını gösterir. Kombinasyonları üreticiye göre bölünmüş olarak görmek için **Varlık modeli**'ni seçerek **Varlık modeli** sayfasını açın.

    **Varlık modeli** sayfasında, varlık modeli - varlık türü ilişkileri ekleyebilirsiniz. Ayrıca, **Varlık türleri** sayfasında, varlık üreticisi – varlık modeli ilişkilerini doğrudan bir varlık türüne ekleyebilirsiniz. Son olarak **Varlık modeli** sayfasında (**Varlık yönetimi** \> **Kurulum** \> **Varlıklar** \> **Varlık modeli**), yeni varlık üreticisi - varlık modeli – varlık türü ilişkileri oluşturabilirsiniz. Bu nedenle, varlık üreticisi – varlık modeli – varlık türü ilişkilerini ayarlamanın ve düzenlemenin üç yolu vardır. Kullanılabilir tüm kombinasyonlar farklı perspektiflerden gösterilir ve kurulum ile çalışırken tercih ettiğiniz giriş noktasını seçebilirsiniz.

> [!NOTE]
> - Bir varlık türünde varlık ölçümlerini seçerseniz, seçimler **Varlık ölçümleri** sayfasında otomatik olarak güncelleştirilir (**Varlık yönetimi** \> **Kurulum** \> **Varlıklar** \> **Varlık türleri** \> **Varlık ölçümleri**).
> - **Genel** hızlı sekmesindeki **Ayrıntılar** bölümündeki alanlar, seçili varlık türünde ayarlanan iş türleri, varlık ölçümleri, öznitelikler vb. sayısını gösterir.

Genellikle, el ile oluşturulan iş emirleri düzeltici bakım ile ilgiliyken otomatik olarak oluşturulan iş emirleri önleyici bakımla ilişkilidir. El ile iş emirleri oluşturduğunuzda, yalnızca **Varlık türleri** sayfasının **İş türleri** hızlı sekmesinde seçilen iş türleri kullanılabilir. Ancak, otomatik olarak oluşturulan iş emirleri **İş türleri** sayfasında oluşturduğunuz tüm iş türlerini kullanabilir (**Varlık yönetimi** \> **Kurulum** \> **İşler** \> **İş türleri**).

## <a name="create-asset-type-setup-lines"></a>Varlık türü kurulum satırları oluşturma

1. **Varlık yönetimi** \> **Kurulum** \> **Varlıklar** \> **Varlık türleri** \> **Varlık türleri kurulumu**'nu seçin. Alternatif olarak **Varlık yönetimi** \> **Kurulum** \> **Varlıklar** \> **Varlık türleri** \> **Varlık türleri**'ni seçin, bir varlık türü seçin ve ardından **Varlık türü kurulumu**'nu seçin.
2. **Varlık türü kurulumu** sayfasını ilk kez kullandığınızda, **Kombinasyonlar oluştur** düğmesinin yararlı olduğunu görebilirsiniz. Bu düğmeyi, bir varlık türünde bir varlık modelinin tüm kombinasyonlarını hızla oluşturmak için kullanabilirsiniz. **Kombinasyonlar oluştur**'u seçin, kombinasyonları oluşturulacak varlık türünü seçin ve ardından **Tamam**'ı seçin.

    > [!NOTE]
    > Otomatik olarak oluşturulan tüm varlık türü kurulum kombinasyonlarını kullanmayacaksanız, kurulumu ve ardından **Sil**'i seçerek kurulumu silebilirsiniz.

3. Bir varlık türü kurulumunu el ile oluşturmak için **Yeni**'yi seçin.
4. Varlık türü kurulumunun ne kadar özel olması gerektiğine bağlı olarak **Varlık türü**, **Üretici** ve **Model** alanlarındaki seçimleri yapın.
5. Bir garanti sözleşmesi varlık türüyle ilişkiliyse, **Satıcı garantisi** ve **Müşteri garantisi** alanlarındaki sözleşmeyi seçin. 
6. **Yedek parçalar** hızlı sekmesinde, seçili varlık türü kurulumuna yedek parça eklemek için **Ekle**'yi seçin.
7. Yedek parçayı onaylamak için yedek parça satırını ve ardından **Onayla**'yı seçin. Onay için birden çok satır seçebilirsiniz.
8. Bir yedek parçanın Varlık yönetiminde başka bir yerde kullanılıp kullanılmadığını görmek için (örneğin, varlıklar ve iş emirleriyle ilgili olarak) yedek parça satırını seçin ve ardından **Maddenin kullanıldığı yer** sayfasını açmak için **Maddenin kullanıldığı yer**'i seçin. Listedeki tüm etkin yedek parçaları görmek için **Etkin** onay kutusunu seçin. Yalnızca onaylı yedek parçaları görmek için **Onaylı** onay kutusunu seçin.
9. **Bakım planları** hızlı sekmesinde, seçili varlık türü kurulumuna bakım planları eklemek için **Ekle**'yi seçin.
10. Bir varlık türü kurulumunu başka bir kuruluma kopyalamak için Kopyala işlevini kullanabilirsiniz. Bir kurulumu kopyalamak için varlık türü kurulumunu seçin, **Kurulumu kopyala**'yı seçin ve kurulumun kopyalanacağı varlık türü kurulumunu seçin. Çeşitli seçeneklerin ayarları ne kadar bilgi ekleneceğini belirler. Bitirdiğinizde, Kurulumu kopyalamak için **Tamam**'ı seçin.

> [!NOTE]
> Yeniden kullanacağınız çok sayıda yedek parça satırı ve bakım planı satırı varsa, Kopyala işlevi birçok varlık türü kurulum kombinasyonu için hızlı ve kolay bir şekilde veri ayarlamanızı sağlar.

## <a name="spare-parts-on-the-asset-type-setup"></a>Varlık türü kurulumunda yedek parçalar

"Varlık türü kurulum satırları oluşturma" bölümünde açıklandığı gibi, yedek parçalar **Varlık türü kurulumu** sayfasındaki varlık modellerinde ayarlanır. Bu nedenle, **Varlık türü kurulumu** sayfasını açtığınızda yalnızca varlık türü, varlık üreticisi ve varlık modelinin seçili kombinasyonuyla ile ilgili yedek parçaları görürsünüz. Tüm yedek parça kayıtlarının listesini görmek için **Yedek parçalar** sayfasını (**Varlık yönetimi** \> **Sorgular** \> **Yedek parçalar**) açın.

**Yedek parçalar** sayfasında varlık türü, varlık üreticisi ve varlık modelinin mevcut kombinasyonları için yeni yedek parçalar da oluşturabilirsiniz. **Varlık türü kurulumu** sayfasında veya **Yedek parçalar** sayfasında yedek parça kayıtları oluşturmayı isteyip istemediğinize karar verebilirsiniz. **Varlık türü kurulumu** sayfası  varlık türü, varlık üreticisi ve varlık modelinin seçili kombinasyonundaki verilere genel bir bakış sağlarken **Yedek parçalar** sayfası tüm varlık türü kurulum satırlarına tam bir genel bakış sağlar. **Yedek parçalar** sayfası çok sayıda kayıt içeriyorsa, **Varlık türü kurulumu** sayfası size daha iyi bir genel bakış sağlayabilir.

Seçili satırdaki yedek parçanın Varlık Yönetiminde herhangi bir yerde kullanılıp kullanılmadığını görmek için (örneğin varlıklar ve iş emirleriyle ilgili olarak) **Maddenin kullanıldığı yer**'i seçerek **Maddenin kullanıldığı yer** sayfasını açın. 

