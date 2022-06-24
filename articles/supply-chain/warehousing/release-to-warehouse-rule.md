---
title: Ambara serbest bırakma kuralı
description: Bu makale, ambara serbest bırakma sırasında esneklik sağlayan Ambara serbest bırakma kuralı özelliği hakkında bilgi sağlamaktadır. Bu özellik, sistemin kısmen rezerve edilmiş sipariş satırlarının serbest bırakılmasına izin verip vermeyeceğini denetleyen bir yapılandırma seçeneği ekler.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: c011938438be32e8a3169d90561ab329da32e32a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895481"
---
# <a name="release-to-warehouse-rule"></a>Ambara serbest bırakma kuralı

[!include [banner](../includes/banner.md)]

*Ambara serbest bırakma kuralı* özelliği, ambara serbest bırakma sırasında esneklik sağlar. Her ambar için bir yapılandırma seçeneği ekler. Ambar için kısmi olarak rezerve edilmiş sipariş satırlarının serbest bırakılıp bırakılamayacağını belirtmek için bu seçeneği kullanabilirsiniz. Özellik, bir tedarik kaynağına karşı sipariş satırı miktarının bir kısmının işaretlenmiş olduğu durumlarda ileri düzey çapraz sevk işlevselliğiyle birlikte çalışır ancak geri kalan kısım ambarda işlenebilir. Bu nedenle, satır, kullanılabilir stok miktarının ambar işleminin devam edebilmesi için serbest bırakılabilir.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Ambara serbest bırakma kuralı özelliğini açma ve başlatma

### <a name="turn-on-the-feature"></a>Özelliği etkinleştirme

*Ambara serbest bırakma kuralı* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Ambara serbest bırakma kuralı*

### <a name="initialize-the-feature"></a>Özelliği başlatma

Özellik sisteminizde etkinleştirildikten sonra, kuralı tüm ambarlarda doğru başlangıç durumuna ayarlamak için bu özelliği başlatmanız gerekir.

- Ambar yönetimi etkinleştirilmemiş ambarlar için, kural başlangıçta **Uygulanamaz** olarak ayarlanır.
- Ambar yönetimi etkinleştirilmiş ambarlar için, kural başlangıçta **Kısmi rezervasyona izin ver** olarak ayarlanır.

Özelliği başlatmak ve serbest bırakma kuralını tüm ambarlara yönelik olarak ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Ambar yönetimi parametreleri** sayfasında, **Genel** sekmesinde, **Şirket bilgileri** bölümünde **Ambara serbest bırakma kuralını başlat** için bağlantıyı seçin. (Bu bağlantı görünmüyorsa ya özellik açık değildir veya önceden başlatılmıştır.)
1. Eylemi onaylamanız istendiğinde **Evet**'i seçerek özelliği başlatın.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Ambara serbest bırakma kuralını her bir ambar için ayarlama

Özellik açılıp başlatıldıktan sonra, önceki bölümde açıklandığı gibi tüm ambarlarınızın bir başlangıç ayarı olacaktır. Bu adımları izleyerek, bu ayarı tek tek ambarlar için değiştirebilirsiniz.

1. **Ambar yönetimi \> Kurulum \> Ambar  \> Ambarlar**'a gidin.
1. Yapılandırılacak ambarı seçin.
1. Sayfayı düzenleme moduna sokmak için **Düzenle**'yi seçin.
1. **Ambar** hızlı sekmesinde, **Rezervasyonlar** bölümünde, **Stok rezervasyonu için gereksinim** alanı, siparişlerin kısmi serbest bırakılmasına izin verilip verilmeyeceğini denetler. Aşağıdaki değerlerden birini seçin:

    - **Uygulanamaz** – Özellik ilk açılıp başlatıldığında, ambar yönetimi etkinleştirilmemiş tüm ambarlara otomatik olarak bu değer atanır. Bu değer değiştirilemez. Bu değer ambar yönetimi etkinleştirilmiş ambarlarda kullanılamaz.
    - **Kısmi rezervasyona izin ver** – Herhangi bir miktar rezerve edildiğinde siparişler serbest bırakılabilir. Sistem, rezerve edilmemiş miktarın ileri düzey çapraz sevk için işaretlenip işaretlenmeyeceğini değerlendirir ve bu miktarı gerekli olarak işaretler. İşaret yoksa, sistem yalnızca rezerve edilen miktar için iş oluşturur. Özellik ilk açılıp başlatıldığında, ambar yönetimi etkinleştirilmiş tüm ambarlara otomatik olarak bu değer atanır. Bu değer ambar yönetimi etkinleştirilmemiş ambarlarda kullanılamaz.
    - **Tam rezervasyon gerekli** – Siparişler yalnızca tam miktar rezerve edilmişse serbest bırakılabilir. Toplam miktar fiziksel olarak rezerve edilmişse veya çapraz sevk için planlanmışsa, siparişler serbest bırakılamaz. Bu değer ambar yönetimi etkinleştirilmemiş ambarlarda kullanılamaz.

1. **Kaydet**'i seçin.

## <a name="scenarios"></a>Senaryolar

Bu bölüm, özelliğin ne yaptığını ve nasıl kullanılacağını öğrenmek için kullanabileceğiniz iki senaryo sunmaktadır.

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak bu senaryolar üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

Bu senaryoları, üretim sisteminde çalışırken özelliğe ilişkin bir kılavuz olarak da kullanabilirsiniz. Ancak, bu durumda kendi değerlerinizi değiştirmeniz gerekir ve standart tanıtım verilerinin sağladığı bazı gerekli kayıt türleri kaybolabilir.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>Senaryo 1: Tam sürüm gerekli (planlı çapraz sevk yok)

Bu senaryo, özelliğin **Tam rezervasyon gerekli** şeklinde ayarlanmış ambarlar için nasıl çalıştığını gösterir.

1. **Ambar yönetimi \> Kurulum \> Ambar  \> Ambarlar**'a gidin.
1. _62_ kodlu ambar için, bu makalede daha önce ele alınan [Ambara serbest bırakma kuralını her bir ambar için ayarlama](#set-option-warehouse) bölümünde açıklandığı gibi, **Stok rezervasyonu için gereksinim** alanının ayarını **Tam rezervasyon gerekli** yapın.
1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Satış siparişi oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri** hızlı sekmesinde, **Müşteri hesabı** alanını _ABD-004_ olarak ayarlayın.
    - **Genel** hızlı sekmesinde, **Ambar** alanının ayarını _62_ yapın.

1. Yeni satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişiniz açılır. **Satış siparişi satırları** bölümündeki kılavuzda boş bir satırı bulunur. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *2*

1. **Satır ekle**'yi seçerek yeni bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0002*
    - **Miktar:** *2*

1. İlk sipariş satırını seçin ve ardından kılavuzun yukarısındaki **Stok** menüsünde **Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. İkinci sipariş satırını rezerve etmeyin.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.
1. Şu hata iletisini aldığınıza dikkat edin: "Tam miktar fiziksel olarak rezerve edilmiş olmalıdır." Bu nedenle, sistem sipariş için herhangi bir iş, sevkiyat veya yük oluşturmaz.

    > [!NOTE]
    > İkinci satırı kısmi olarak rezerve ederseniz aynı hata iletisini alırsınız.

### <a name="scenario-2-allow-partial-release"></a>Senaryo 2: Kısmi serbest bırakmaya izin ver

Bu senaryo, özelliğin **Kısmi serbest bırakmaya izin ver** şeklinde ayarlanmış ambarlar için nasıl çalıştığını gösterir.

1. **Ambar yönetimi \> Kurulum \> Ambar  \> Ambarlar**'a gidin.
1. _62_ kodlu ambar için, bu makalede daha önce ele alınan [Ambara serbest bırakma kuralını her bir ambar için ayarlama](#set-option-warehouse) bölümünde açıklandığı gibi, **Stok rezervasyonu için gereksinim** alanının ayarını **Kısmi rezervasyona izin ver** yapın.
1. [Önceki senaryoda](#scenario1) yaptığınız gibi, **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin ve _62_ kodlu ambardaki müşteri hesabı _ABD-004_ için bir satış siparişi oluşturun. Aşağıdaki iki sipariş satırını ekleyin:

    - **Satır 1:** **Madde numarası** alanını _A0001_ olarak, **Miktar** alanını _2_ olarak ve **Birim** alanını _Prç_ olarak ayarlayın.
    - **Satır 2:** **Madde numarası** alanını _A0002_ olarak, **Miktar** alanını _2_ olarak ve **Birim** alanını _Prç_ olarak ayarlayın.

1. [Önceki senaryoda](#scenario1) yaptığınız gibi, sipariş satırı 1 için tüm miktarı rezerve edin ancak sipariş satırı 2'yi rezerve etmeyin.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.
1. Bu kez bir hata iletisi almadığınıza dikkat edin. Bunun yerine, sistem iş, sevkiyat ve yükleri gerektiği gibi oluşturur ve sonuçları gösterir.
1. Sevkiyat, yükleme ve iş bilgilerini görüntülemek için kılavuzun yukarısındaki **Ambar** menüsünün seçeneklerini kullanın:

    - **Satır 1:** Üç seçenek mevcuttur: **Sevkiyat ayrıntıları**, **Yükleme ayrıntıları** ve **İş ayrıntıları**. Sipariş ambara serbest bırakıldığında oluşturulan sevkiyat, yükleme ve iş ayrıntılarını görüntülemek için her bir seçeneği belirleyin.
    - **Satır 2:** Yalnızca **İş ayrıntıları** seçeneği kullanılabilir. Bunu seçin ve stok rezerve edilmediği için iş oluşturulmadığına dikkat edin. Bu nedenle, sevkiyat veya yük oluşturulmamıştır.

> [!NOTE]
> İkinci satır kısmen rezerve edildiğinde aynı sonuç beklenir. Bu durumda, rezerve edilmiş satır miktarı için iş oluşturulur ancak rezerve edilmemiş miktar için oluşturulmaz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]