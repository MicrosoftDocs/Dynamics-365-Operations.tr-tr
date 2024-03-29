---
title: Boyutlar ve ürün çeşitleri için varsayılan sipariş ayarları
description: Varsayılan sipariş ayarları maddelerin bulunduğu veya depolandığı tesisi ve ambarı, ticari veya stok yönetimi için kullanılacak minimum, maksimum, birden fazla ve standart miktarları, sağlama sürelerini, durdurma bayrağını ve sipariş taahhüt hesabını tanımlar.
author: johanhoffmann
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemOrderSetup, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleasedStoppedAllChartPart, UnitTestPartitions
audience: Application User
ms.reviewer: kamaybac
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 106da56ed1de7d9e555cfdd63f19687d7e17599a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862583"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Boyutlar ve ürün çeşitleri için varsayılan sipariş ayarları

[!include [banner](../includes/banner.md)]

Dynamics 365 Supply Chain Management içinde, varsayılan sipariş ayarları maddelerin bulunduğu veya depolandığı tesisi ve ambarı, ticari veya stok yönetimi için kullanılacak minimum, maksimum, birden fazla ve standart miktarları, sağlama sürelerini, durdurma bayrağını ve sipariş taahhüt hesabını tanımlar. Varsayılan sipariş ayarları, satınalma siparişleri, satış siparişleri, transfer emirleri, stok günlükleri oluştururken ve master planlama ile planlı siparişler oluştururken kullanılır. Varsayılan sipariş ayarları maddeye, tesise, ürün çeşidine veya ürün boyutuna özel olabilir.

Bir ürünle ilgili olarak varsayılan sipariş ayarlarını tanımlamak için aşağıdaki adımları izleyin.

1. **Ürün bilgileri yönetimi** &gt; **Ürünler** &gt; **Serbest bırakılmış ürünler**'e gidin.
1. Izgaradan ilgili ürünü seçin.
1. Eylem Bölmesinde, seçilen ürünle ilgili **Varsayılan sipariş ayarları** sayfasını açmak için aşağıdaki adımlardan birini izleyin:

    - **Plan** sekmesinde, **Sipariş ayarları** grubunda, **Varsayılan sipariş ayarları**'nı seçin.
    - **Stoğu yönet** sekmesinde, **Sipariş ayarları** grubunda, **Varsayılan sipariş ayarları**'nı seçin.

1. Ayarları makalenin geri kalanında açıklandığı şekilde yapılandırın.

## <a name="default-order-settings"></a>Varsayılan sipariş ayarları

Satınalma, satış ve stok için üç tür sipariş ayarı bulunur. Satınalmalar için varsayılan sipariş ayarları şunları oluştururken kullanılır:

- Satın alma siparişi satırları
- Satınalma sözleşmesi satırları
- Teklif talebi satırları
- Satınalma talebi satırları
- Konsinye stok yenileme satırları (kısmen desteklenir, nota bakın)
- Planlı satınalma siparişleri

> [!NOTE]
> Konsinye stok yenileme sipariş satırları için uygun olan **Varsayılan sipariş ayarları** sayfasındaki **Satınalma siparişi** hızlı sekmesinden gelen ayarlar yalnızca **Varsayılan tesis** alanı, **Varsayılan ambar** alanı ve **Durdurulmuş** onay kutusudur.

Satışlar için varsayılan sipariş ayarları şunları oluştururken kullanılır:

- Satış siparişi satırları
- Satış sözleşmesi satırları
- Satış teklifi satırları
- Sipariş iade satırları ve madde yenileme satırları
- Talep tahmin satırları

Varsayılan satış siparişi ayarları şunları oluştururken de uygulanır:

- Proje maddesi gereksinimleri
- Servis siparişi madde gereksinimleri

Stok için varsayılan sipariş ayarları şunları oluştururken kullanılır:

- Stok günlükleri
- Transfer emirleri
- Planlı transfer emirleri

Varsayılan stok siparişi ayarları şunları oluştururken de uygulanır:

- Karantina emirleri
- Kalite emirleri
- Üretim emirleri
- Ürün reçetesi satırları
- Planlı üretim emirleri

## <a name="full-definition-of-a-released-product"></a>Serbest bırakılan bir ürünün tam tanımı

Bir hareket oluştururken, Supply Chain Management'ın varsayılan sipariş ayarlarını tanımlamaya çalışabilmesi için satırdaki serbest bırakılan bir ürünün tam tanımını belirtmeniz gerekir. Yayımlanan ürünün tam tanımında, madde numarası ve yapılandırma, ebat, stil, sürüm, renk gibi tüm aktif ürün boyutları harekette belirtilir. Örneğin, serbest bırakılan bir ürün çeşidi için el ile bir satın alma siparişi oluşturursanız tesis, ambar, miktar ve sağlama süresi varsayılan olarak sipariş satırında görüntülenmeden önce gerekli tüm ürün boyutlarını belirtmeniz gerekir. 

Sipariş veya yevmiye defteri satırlarını oluştururken varsayılan sipariş ayarları parametrelerinin tamamı uygulanmaz. Miktarlar ve sağlama süreleri yalnızca uygun olduğunda varsayılan olarak görüntülenir. Örneğin, bir yevmiye defteri satırı sayıldığında, sadece site ve ambar bir satır oluşturulduğunda varsayılan olarak görüntülenirler. Bu nedenle, çoklu veya minimumlar üzerinde varsayılan miktar veya denetimler, satırı veya günlüğü deftere naklederken gerçekleştirilmeyecektir. 

Sipariş veya yevmiye defteri satırı oluşturulduğunda sistem her zaman varsayılan tesis ve ambarı bulmayı dener. Tesis, diğer ayarlarda her zaman varsayılan olarak görüntülenmez. Örneğin, satış siparişi veya satınalma siparişi oluştururken sipariş başlığındaki site otomatik olarak sipariş satırlarında kullanılır. Ürün reçetesi satırı oluştururken, ürün reçetesi başlığındaki site kullanılır. Tesis belirlendikten sonra ambar için varsayılan olarak kullanılabilen tesise özgü herhangi bir sipariş ayarını bulmak için kullanılır. 

Varsayılan sipariş türü, satınalma ve stok sağlama süreleri **Madde kapsamı** sayfası üzerindeki madde karşılama kuralları tarafından geçersiz kılınabilir. Varsayılan sipariş ayarları üretim ve transfer sağlama süreleri arasında ayrım yapılmasına izin vermese de, madde kapsam kuralları buna izin verir. Ancak madde kapsama ayarı planlı üretimi ve planlı transfer emirlerini oluştururken yalnızca Master planlama (MRP) tarafından kullanılır ve el ile üretim ve transfer emirleri oluştururken uygulanmaz. 

## <a name="default-order-settings-rules"></a>Varsayılan sipariş ayarları kuralları

Genel varsayılan sipariş ayarlarını ve tesis veya belirli bir ürün boyutu veya ürün boyutları birleşimi gibi yalnızca belirli şartlara uygulanan varsayılan sipariş ayarı kural sayısını tanımlayabilirsiniz. Ambara özgü sipariş ayarlarını tanımlayamazsınız.

### <a name="rank-in-default-order-settings"></a>Varsayılan sipariş ayarlarında derecelendirme

Varsayılan sipariş ayarları kurallarının dereceleri vardır. Derece ne kadar yüksekse kural o kadar önemlidir, bu da yüksek önceliğe sahip olduğu ve daha düşük dereceli kurallardan önce kullanılacağı anlamına gelir. Genel varsayılan sipariş ayarları, değiştirilemeyen sıfır dereceye sahiptir. Sıfır dereceli yalnızca tek bir kural olabilir. Uygulandıkları boyutlar farklı olduğu sürece kurallar aynı dereceye sahip olabilir. Bu, tesise özgü sipariş ayarlarının modellemesi açısından faydalıdır. Varsayılan sipariş ayarları kuralı oluşturulduğunda, sipariş değerleri, durdurma bayrağı vb. gibi değerler sıfır dereceden devralınır ancak geçersiz kılınabilir.

### <a name="default-order-settings-for-released-products"></a>Serbest bırakılan ürünler için varsayılan sipariş ayarları

Yayımlanan farklı ürünler için genel sipariş ayarlarını veya tesise özel sipariş ayarlarını tanımlayabilirsiniz. Genel sipariş ayarları her zaman sıfır dereceye sahiptir. Yeni satış, satınalma ve stok sipariş ayarlarını aynı anda ayarlarsanız **Varsayılan sipariş ayarları** sayfasında **Ayrıntı görünümü**'nü kullanmanızı öneririz. Ayrıntı görünümünü değiştirmek için **Seçenekler** &gt; **Sayfa seçenekleri** &gt; **Görünümü değiştir** &gt; **Ayrıntı görünümü'ne** gidin.

### <a name="site-specific-order-settings"></a>Tesise özel sipariş ayarları

Tesise özel sipariş ayarları oluşturmak için **Yeni**'yi seçin. **Ayrıntılar görünümünde** **Şunun için geçerli ayarlar** bölümündeki **Tesis** alanına tesisi girin. **Izgara görünümünde** **Tesis** sütununa tesisi girin. Yeni kurala otomatik olarak 0'dan (sıfır) büyük yeni bir derece değeri atanır. İhtiyaç duyduğunuz sayıda tesise özgü kural oluşturabilirsiniz. Eşit derecede önemli olduklarını belirtmek için, tüm tesise özgü kurallara aynı derece değerini atayabilirsiniz.

**Ayrıntı görünümü** içindeyken madde için oluşturulan kuralların özetini alamazsınız. Özet bilgileri görmek için **Listeyi göster/gizle** seçeneğini kullanın. Herhangi bir türde sipariş satırı oluşturulduğunda ve sağlanan bir tesise sahip olmadığında, Supply Chain Management tesise özel olmayan bir kural arar. Bu, sipariş satırında varsayılan bir tesis belirlemeye yardımcı olur. Bu tesis daha sonra varsayılan ambarın ayarlanabildiği tesise özel bir kuralı aramak için kullanılır. Bu ambar, sipariş satırına uygulanır.

### <a name="specific-order-settings-for-product-dimension"></a>Ürün boyutu için özel sipariş ayarları

Sipariş ayarları kurallarını, herhangi bir etkin ürün boyutu veya etkin ürün boyutları birleşimi için tanımlayabilirsiniz. Ürün boyutu alanı boşsa kural ürün boyutunun tüm değerlerine uygulanır. 

Aşağıdaki örnek ürünü değerlendirin.

| Ürün                                                | Değer                                   |
|-----------------------------------------------------|-----------------------------------------|
| **Ürün adı**                                    | Fotoelektrik sensörü                    |
| **Madde numarası**                                     | XW56                                    |
| **Konfigürasyon** (ışık türüne model oluşturmak için kullanılır) | C1-Görünür kırmızı ışık, C2-Kızılötesi ışık |
| **Sürüm** | V1, V2, V3                              |

Bu örnekte, ürünün tedarik edildiğini ve üretilmediğini varsayalım. Ayrıca, C1 konfigürasyonunun daha yaygın kullanıldığını, bu nedenle daha kısa sağlama süresine sahip olduğunu varsayalım. 

Bu senaryoyu modellemek için aşağıdaki varsayılan sipariş ayarlarını oluşturun.

| Derece | Tesis | Konfigürasyon | Sürüm | Satınalma: Varsayılan ayarları geçersiz kıl | Satınalma sağlama süresi | Satınalma: Durduruldu | Satışlar: Varsayılan ayarları geçersiz kıl | Satışlar: Durduruldu |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Evet                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Versiyon veya tesisin yerleştirildiği satırdan bağımsız olarak madde XW56, yapılandırma C1 için bir satınalma sipariş satırı veya planlı bir satınalma siparişi oluşturulduğunda sağlama süresi 2 olarak kabul edilir. V3 dahil tüm sürümlerin durdurulduğunu varsayalım.

Aşağıdaki varsayılan sipariş ayarları kurallarını oluşturabilirsiniz.

| Derece | Tesis | Konfigürasyon | Sürüm | Satınalma: Varsayılan ayarları geçersiz kıl | Satınalma sağlama süresi | Satınalma: Durduruldu | Satışlar: Varsayılan ayarları geçersiz kıl | Satışlar: Durduruldu |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Evet                                  |                    | Evet                | Evet                               | Evet             |
| 20   |      |               | V1    | Evet                                  |                    | Evet                | Evet                               | Evet             |
| 10   |      | C1            |       | Evet                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Eski sürümleri durdurmaya ilişkin iki kural aynı dereceye sahiptir. Bu nedenle, bunlar aynı derecede önemlidir. Her iki kural da C1 yapılandırması kuralından daha yüksek bir dereceye olduğundan, bu kuralla C1 yapılandırması kuralına göre öncelik kazanır. 

Bu örnek, derece gereksinimini açıklar. Derece kullanılmazsa, C1 yapılandırması ve V2 sürümü için satınalam siparişi oluşturulduğunda, V2 ve C1 için tanımlanan iki kural belirsiz olur. Bu belirsizliği gidermek için Supply Chain Management azalan derece sırasına göre kuralları arar ve ilk geçerli kuralı uygular. Bu örnekte C1 yapılandırması ve V2 sürümü için bir satınalma siparişi satırı oluşturulduğunda, kullanıcı maddenin beklemede olduğu ve buna sürümü değerinin neden olduğuna dair bir uyarı iletisi alır. Yapılandırma kuralı sürüm kuralından daha yüksek bir dereceye sahipse, C1 yapılandırması ve V2 sürümü için bir satınalma siparişi satırı başarılı şekilde oluşturulur ve kullanıcı "madde beklemede" iletisini almaz. 

Aşağıdaki varsayılan sipariş ayarı kurallarını değerlendirin.

| Derece | Tesis | Konfigürasyon | Sürüm | Varsayılan tesis | Varsayılan ambar | Satınalma: Varsayılan depolama boyutlarını geçersiz kıl | Satınalma ambarı |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Evet                                            | 22                 |
| 10   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Sistem, tesis ve ambarı belirlemek için kural ayarından iki kez çapraz geçiş yapar. Yapılandırma C1, sürüm V2 için bir satınalma siparişi satırı oluşturulduğunda, tesis 10 derecesine sahip kurala dayalı olarak belirlenir. Sistem daha sonra tesis 2 için bir kuralı, ambarı belirlemek için arar. Kural 20 bulunur ve daha yüksek dereceye sahip olduğundan satınalma siparişi satırındaki ambar 21 değil 22 olur.

Genel kural olarak, özel kurallar ve diğer boyutlardan daha önemli olan kurallar, daha yüksek dereceler alırken daha genel kurallar daha düşük dereceler alır. 

Derecesi sıfır olan kural bir güvenlik ağı olarak hizmet verir. Başka kural eklenmemişse sıfır dereceli kuraldaki varsayılan sipariş ayarları kullanılır. 

Derece sayısı önemli olduğundan **Varsayılan sipariş ayarları** Eylem Bölmesi'nde kuralı yukarı veya aşağı taşıyan ve kuralı her zaman 10'un katları olacak şekilde yeniden numaralandıran işlevler bulunur. 

Serbest bırakılmış ürün için oluşturulan kural sayısı fazla olabilir. Her bir kuralın geçersiz kılınması mantığını ve bunun neden gerekli olduğunu daha iyi anlamak için **Varsayılan sipariş ayarları** sayfasında **Kılavuz görünümü**'nü kullanmanızı öneririz. **Seçenekler** &gt; **Sayfa seçenekleri** &gt; **Görünümü değiştir** &gt; **Kılavuz görünümü**'ne giderek kılavuz görünümünü etkinleştirebilirsiniz. Kılavuzda görüntülenen sütun sayısı, özellikle satışlar ve stok sekmeleri için oldukça belirleyici olabilir. Kılavuzda gösterilen sütun sayısını sınırlandırmak için sütun grupları **Varsayılan sipariş ayarları** &gt; **Sütun görüntüsü** menüsündeki düğmeler kullanılarak gizlenebilir veya görüntülenebilir.

### <a name="specific-order-settings-for-released-product-variant"></a>Serbest bırakılan ürün çeşidi için özel sipariş ayarları

Varsayılan sipariş ayarları için kural sisteminde sorun yaşanıyorsa her bir ürün çeşidi için varsayılan sipariş ayarlarını tanımlama seçeneği vardır. Aşağıdaki örnek, bunun yukarıda tanımlanan üründe ve durumlarda nasıl kullanılacağını gösterir.

| Derece | Tesis | Konfigürasyon | Sürüm | Satınalma: Varsayılan ayarları geçersiz kıl | Satınalma sağlama süresi | Satınalma: Durduruldu | Satışlar: Varsayılan ayarları geçersiz kıl | Satışlar: Durduruldu |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | V3    | Evet                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | V2    | Evet                                  | 5                  | Evet                | Evet                               | Evet             |
| 10   |      | C2            | V1    | Evet                                  | 5                  | Evet                | Evet                               | Evet             |
| 10   |      | C1            | V3    | Evet                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | V2    | Evet                                  | 2                  | Evet                | Evet                               | Evet             |
| 10   |      | C1            | V1    | Evet                                  | 2                  | Evet                | Evet                               | Evet             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Bu durumda derecenin bir önemi yoktur, bu nedenle onu gizlemeyi seçebilirsiniz. Bu çözüm, bakım sorunlarına neden olma potansiyeline sahiptir. Ancak, Ürün Yaşam Döngüsü Yönetimi (PLM) sistemleri ile tümleştirmeyi düşünüyorsanız bu ayarı kullanmayı düşünmek isteyebilirsiniz.

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Varsayılan sipariş miktarlarında katı veya standart doğrulamayı kullanma

Bir ürünle ilgili olarak **Varsayılan sipariş ayarları**'na girilen miktarları doğrularken sistemin ne kadar katı olacağını belirleyebilirsiniz. Yeni katı seçeneğini kullandığınızda, **Standart sipariş miktarı** her zaman satın alma siparişleri, stok ve satış siparişleri için belirtilen **Çoklu** değerin bir katı olmalıdır. Katı doğrulama kullanıyorsanız, bu gereksinimi karşılamayan varsayılan sipariş ayarlarını kaydedemezsiniz (ve ileti çubuğunda bir hata gösterilir). 

Katı doğrulama, **Varsayılan sipariş ayarları** sayfasının **Satın alma siparişi**, **Stok** ve **Satış siparişi** hızlı sekmelerinde belirtilen **Standart sipariş miktarı** değerleri için geçerlidir. Her hızlı sekmenin o hızlı sekme için belirtilen **Standart sipariş miktarı** değerini doğrulamak için kullanılan, kendi **Çoklu** ayarı vardır.

### <a name="turn-the-strict-validation-option-on-or-off"></a>Kesin doğrulama seçeneğini açma veya kapatma

Kesin doğrulama kullanmak için *Varsayılan sipariş miktarlarında kesin doğrulama* özelliğinin sisteminizde açık olması gerekir. Supply Chain Management sürüm 10.0.21 itibariyle, bu özellik varsayılan olarak açıktır. Supply Chain Management 10.0.25 itibarıyla, bu özellik zorunludur ve kapatılamaz. 10.0.25 sürümünden daha eski bir sürümü çalıştırıyorsanız, [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanına gidip *Varsayılan sipariş miktarlarında kesin doğrulama* özelliğini bularak bu işlevi açabilir veya kapatabilirsiniz.

### <a name="set-the-validation-option"></a>Doğrulama seçeneğini ayarlama

Doğrulama seçeneğini ayarlamak için:

1. **Ürün bilgileri yönetimi \>Kurulum \> Ürün bilgileri yönetimi parametreleri** bölümüne gidin.
1. **Genel** sekmesinde, **Varsayılan sipariş miktarları doğrulaması** öğesini aşağıdaki değerlerden biriyle ayarlayın:
    - **Katı** - Tüm **Standart sipariş miktarı** değerlerinin her hızlı sekmede (**Satın alma siparişi** , **Stok** ve **Satış siparişi**) **Çoklu** değerinin bir katı olmasını sağlamak için bu seçeneği işaretleyin.
    - **Standart** - Standart doğrulamayı kullanmak için bu seçeneği belirleyin (bu özellik etkinleştirilmediğinde aynı şekilde çalışır).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]