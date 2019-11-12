---
title: Boyutlar ve ürün çeşitleri için varsayılan sipariş ayarları
description: Varsayılan sipariş ayarları maddelerin bulunduğu veya depolandığı tesisi ve ambarı, ticari veya stok yönetimi için kullanılacak minimum, maksimum, birden fazla ve standart miktarları, sağlama sürelerini, durdurma bayrağını ve sipariş taahhüt hesabını tanımlar.
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d13aabfb36e8af4a32de8bc8949e8b164075532a
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570714"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Boyutlar ve ürün çeşitleri için varsayılan sipariş ayarları

[!include [banner](../includes/banner.md)]

Dynamics 365 Supply Chain Management içinde, varsayılan sipariş ayarları maddelerin bulunduğu veya depolandığı tesisi ve ambarı, ticari veya stok yönetimi için kullanılacak minimum, maksimum, birden fazla ve standart miktarları, sağlama sürelerini, durdurma bayrağını ve sipariş taahhüt hesabını tanımlar. Varsayılan sipariş ayarları, satınalma siparişleri, satış siparişleri, transfer emirleri, stok günlükleri oluştururken ve master planlama ile planlı siparişler oluştururken kullanılır. Varsayılan sipariş ayarları maddeye, tesise, ürün çeşidine veya ürün boyutuna özel olabilir.

Varsayılan sipariş ayarlarını **Varsayılan sipariş ayarları** sayfasında tanımlayabilirsiniz. Bu sayfayı açmak için **Ürün bilgileri yönetimi** &gt; **Ürünler** &gt; **Serbest bırakılan ürünler** &gt; **Serbest bırakılan bir ürün seçin** &gt; **Planlama** veya **Stok yönetimi** Eylem Bölmesi &gt; **Sipariş ayarları** &gt; **Varsayılan sipariş ayarları**'na gidin.

## <a name="default-order-settings"></a>Varsayılan sipariş ayarları
Satınalma, satış ve stok için üç tür sipariş ayarı bulunur. Satınalmalar için varsayılan sipariş ayarları şunları oluştururken kullanılır:

-   Satın alma siparişi satırları
-   Satınalma sözleşmesi satırları
-   Teklif talebi satırları
-   Satınalma talebi satırları
-   Konsinye stok yenileme satırları
-   Planlı satınalma siparişleri

Satışlar için varsayılan sipariş ayarları şunları oluştururken kullanılır:

-   Satış siparişi satırları
-   Satış sözleşmesi satırları
-   Satış teklifi satırları
-   Sipariş iade satırları ve madde yenileme satırları
-   Talep tahmin satırları

Varsayılan satış siparişi ayarları şunları oluştururken de uygulanır:

-   Proje maddesi gereksinimleri
-   Servis siparişi madde gereksinimleri

Stok için varsayılan sipariş ayarları şunları oluştururken kullanılır:

-   Stok günlükleri
-   Transfer emirleri
-   Planlı transfer emirleri

Varsayılan stok siparişi ayarları şunları oluştururken de uygulanır:

-   Karantina emirleri
-   Kalite emirleri
-   Üretim emirleri
-   Ürün reçetesi satırları
-   Planlı üretim emirleri

## <a name="full-definition-of-a-released-product"></a>Serbest bırakılan bir ürünün tam tanımı
Bir hareket oluştururken, Supply Chain Management'ın varsayılan sipariş ayarlarını tanımlamaya çalışması için satırdaki serbest bırakılan bir ürünün tam tanımını belirtmeniz gerekir. Yayımlanan ürünün tam tanımı, madde numarası ve yapılandırma, ebat, stil, renk gibi tüm aktif ürün boyutlarının hareket üzerinde belirtildiği anlamına gelir. Örneğin, serbest bırakılan bir ürün çeşidi için el ile bir satın alma siparişi oluşturursanız tesis, ambar, miktar ve sağlama süresi varsayılan olarak sipariş satırında görüntülenmeden önce gerekli tüm ürün boyutlarını belirtmeniz gerekir. 

Sipariş veya günlük satırlarını oluştururken varsayılan sipariş ayarları parametrelerinin tamamı uygulanmaz. Miktarlar ve sağlama süreleri yalnızca uygun olduğunda varsayılan olarak görüntülenir. Örneğin, bir günlük satırı sayıldığında, sadece site ve ambar bir satır oluşturulduğunda varsayılan olarak görüntülenirler. Çoklu veya minimumlar üzerinde miktar varsayılanı veya kontrolleri elbette satırı veya günlüğü deftere naklederken gerçekleştirilmeyecektir. 

Sipariş veya günlük satırı oluşturulduğunda sistem her zaman varsayılan tesis ve ambarı bulmayı dener. Tesis, diğer ayarlarda her zaman varsayılan olarak görüntülenmez. Örneğin, satış siparişi veya satınalma siparişi oluştururken sipariş başlığındaki site otomatik olarak sipariş satırlarında kullanılır. Ürün reçetesi satırı oluştururken, ürün reçetesi başlığındaki site kullanılır. Tesis belirlendikten sonra ambar için varsayılan olarak kullanılabilen tesise özgü herhangi bir sipariş ayarını bulmak için kullanılır. 

Varsayılan sipariş türü, satınalma ve stok sağlama süreleri **Madde kapsamı** sayfası üzerindeki madde karşılama kuralları tarafından geçersiz kılınabilir. Varsayılan sipariş ayarları üretim ve transfer sağlama süreleri arasında ayrım yapılmasına izin vermese de, madde kapsam kuralları buna izin verir. Ancak madde kapsama ayarı planlı üretimi ve planlı transfer emirlerini oluştururken yalnızca MRP tarafından kullanılır ve el ile üretim ve transfer emirleri oluştururken uygulanmaz. 

## <a name="default-order-settings-rules"></a>Varsayılan sipariş ayarları kuralları
Genel varsayılan sipariş ayarlarını ve tesis veya belirli bir ürün boyutu veya ürün boyutları birleşimi gibi yalnızca belirli şartlara uygulanan varsayılan sipariş ayarı kural sayısını tanımlayabilirsiniz. Ambara özel sipariş ayarlarını tanımlayamazsınız.

### <a name="rank-in-default-order-settings"></a>Varsayılan sipariş ayarlarında derecelendirme

Varsayılan sipariş ayarları kurallarının dereceleri vardır. Derece ne kadar yüksekse kural o kadar önemlidir, bu da yüksek önceliğe sahip olduğu ve daha düşük dereceli kurallardan önce kullanılacağı anlamına gelir. Genel varsayılan sipariş ayarları, değiştirilemeyen sıfır dereceye sahiptir. Sıfır dereceli yalnızca tek bir kural olabilir. Uygulandıkları boyutlar farklı olduğu sürece kurallar aynı dereceye sahip olabilir. Bu, tesise özgü sipariş ayarlarının modellemesi açısından faydalıdır. Varsayılan sipariş ayarları kuralı oluşturulduğunda, sipariş değerleri, durdurma bayrağı vb. gibi değerler sıfır dereceden devralınır ancak geçersiz kılınabilir.

### <a name="default-order-settings-for-released-products"></a>Serbest bırakılan ürünler için varsayılan sipariş ayarları

Serbest bırakılan farklı ürünler için genel sipariş ayarlarını veya tesise özel sipariş ayarlarını tanımlayabilirsiniz. Genel sipariş ayarları her zaman sıfır dereceye sahiptir. Yeni satış, satınalma ve stok sipariş ayarlarını aynı anda birlikte ayarlarsanız **Varsayılan sipariş ayarları** sayfasında **Ayrıntı görünümü**'nü kullanmanızı öneririz. Ayrıntı görünümünü değiştirmek için **Seçenekler** Eylem Bölmesi &gt; **Sayfa seçenekleri** &gt; **Görünümü değiştir** &gt; **Ayrıntı görünümü'ne** gidin.

### <a name="site-specific-order-settings"></a>Tesise özgü sipariş ayarları

Tesise özel sipariş ayarları oluşturmak için **Yeni**'ye tıklayın. **Ayrıntı görünümü** içinde **Şunun için geçerli ayarlar**: &gt; **Tesis** alanındaki tesisi doldurun. **Izgara görünümü** içinde **Tesis** sütununda tesisi doldurun. Yeni kural otomatik olarak sıfırdan daha yüksek yeni bir derece değeri alır. İstediğiniz kadar tesise özel kural oluşturabilirsiniz ve model oluşturmak için tesise özel tüm kuralları eşit öneme sahip aynı dereceye atayabilirsiniz. 

**Ayrıntı görünümü** içindeyken madde için oluşturulan kuralların özetini alamazsınız. Özet bilgileri görmek için **Listeyi göster/gizle** düğmesini değiştirin. Herhangi bir türde sipariş satırı oluşturulduğunda ve sağlanan bir tesise sahip olmadığında, Supply Chain Management tesise özel olmayan bir kural arar. Bu, sipariş satırında varsayılan bir tesis belirlemeye yardımcı olabilir. Bu tesis daha sonra varsayılan ambarın ayarlanabildiği tesise özel bir kuralı aramak için kullanılır. Bu ambar, sipariş satırına uygulanır.

### <a name="specific-order-settings-for-product-dimension"></a>Ürün boyutu için özel sipariş ayarları

Sipariş ayarları kurallarını, herhangi bir etkin ürün boyutu veya etkin ürün boyutları birleşimi için tanımlayabilirsiniz. Ürün boyutu alanı boş bırakılırsa kural ürün boyutunun tüm değerlerine uygulanır. 

Aşağıdaki örnek ürünü değerlendirin.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Ürün adı**                                    | Fotoelektrik sensörü                    |
| **Madde numarası**                                     | XW56                                    |
| **Konfigürasyon** (ışık türüne model oluşturmak için kullanılır) | C1-Görünür kırmızı ışık, C2-Kızılötesi ışık |
| **Stil** (mühendislik revizyonuna model oluşturmak için kullanılır)  | R1, R2, R3                              |

Bu örnekte, ürünün tedarik edildiğini ve üretilmediğini varsayalım. Ayrıca, C1 konfigürasyonunun daha yaygın kullanıldığını, bu nedenle daha kısa sağlama süresine sahip olduğunu varsayalım. 

Bu senaryoyu modellemek için aşağıdaki varsayılan sipariş ayarlarını oluşturun.

| Derece | Tesis | Yapılandırma | Stil | Satınalma: Varsayılan ayarları geçersiz kıl | Satınalma sağlama süresi | Satınalma: Durduruldu | Satışlar: Varsayılan ayarları geçersiz kıl | Satışlar: Durduruldu |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Evet                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Revizyon veya tesisin yerleştirildiği satırdan bağımsız olarak XW56, Yapılandırma C1 için bir satınalma sipariş satırı veya planlı bir satınalma siparişi oluşturulduğunda sağlama süresi 2 olarak kabul edilir. R3 dahil tüm revizyonların durdurulduğunu varsayalım.

Aşağıdaki varsayılan sipariş ayarları kurallarını oluşturabilirsiniz.

| Derece | Tesis | Yapılandırma | Stil | Satınalma: Varsayılan ayarları geçersiz kıl | Satınalma sağlama süresi | Satınalma: Durduruldu | Satışlar: Varsayılan ayarları geçersiz kıl | Satışlar: Durduruldu |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Evet                                  |                    | Evet                | Evet                               | Evet             |
| 20   |      |               | R1    | Evet                                  |                    | Evet                | Evet                               | Evet             |
| 10   |      | C1            |       | Evet                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Eski revizyonları durduran iki kural aynı derecelendirmeye sahiptir. Bu, eşit olarak önemli oldukları anlamına gelir. Her ikisi de C1 konfigürasyon kuralından daha yüksek bir dereceye sahiptir. Bu, C1 konfigürasyon kuralına göre öncelik kazandıkları anlamına gelir. 

Bu örnek, derece gereksinimini açıklar. Satınalma siparişi, derece olmaksızın C1 konfigürasyonu ve R2 revizyonu için oluşturulursa R2 ve C1 için tanımlanan iki kural belirsiz olur. Bu belirsizliği gidermek için Supply Chain Management azalan derece sırasına göre kuralları arar ve ilk geçerli kuralı uygular. Bu örnekte C1 konfigürasyonu ve R2 revizyonu için bir satınalma sipariş satırı oluşturulduğunda, kullanıcı maddenin beklemede olduğu ve buna revizyon değerinin neden olduğuna dair bir uyarı iletisi alır. Konfigürasyon kuralı revizyon kuralından daha yüksek bir dereceye sahipse C1 konfigürasyonu ve R2 revizyonu için bir satınalma siparişi satırının oluşturulması başarılı olur ve kullanıcı "madde beklemede" iletisini almaz. 

Aşağıdaki varsayılan sipariş ayarı kurallarını değerlendirin.

| Derece | Tesis | Yapılandırma | Stil | Varsayılan tesis | Varsayılan ambar | Satınalma: Varsayılan depolama boyutlarını geçersiz kıl | Satınalma ambarı |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Evet                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Sistem, tesis ve ambarı belirlemek için kural ayarından iki kez çapraz geçiş yapar. Yapılandırma C1, stil R2 için bir sipariş emri satırı oluşturulduğunda, site rank 10 kuralına dayalı olarak belirlenir. Sistem daha sonra site 2 için bir kuralı, ambarı belirlemek için arar. Kural 20 bulunur ve daha yüksek dereceye sahip olduğundan satınalma siparişi satırındaki ambar 21 değil 22 olur. 

Genel bir kural olarak, özel kurallar ve diğer boyutlardan daha önemli olan kurallar, daha yüksek dereceler alırken daha genel kurallar daha düşük dereceler alır. 

Derecesi sıfır olan kural bir güvenlik ağı olarak hizmet verir. Başka kural eklenmemişse sıfır dereceli kuraldaki varsayılan sipariş ayarları kullanılır. 

Derece sayısı çok önemli olduğundan **Varsayılan sipariş ayarları** Eylem Bölmesi'nde kuralı yukarı veya aşağı taşıyan ve kuralı her zaman 10'un katları olacak şekilde yeniden numaralandıran işlevler bulunur. 

Serbest bırakılmış ürün için oluşturulan kural sayısı fazla olabilir. Her bir kuralın geçersiz kılınması mantığını ve bunun neden gerekli olduğunu daha iyi anlamak için **Varsayılan sipariş ayarları** sayfasında **Izgara görünümü**'nü kullanmanızı öneririz. **Seçenekler** Eylem Bölmesi &gt; **Sayfa seçenekleri** &gt; **Görünümü değiştir** &gt; **Kılavuz görünümü**'ne giderek kılavuz görünümünü etkinleştirebilirsiniz. Kılavuzda görüntülenen sütun sayısı, özellikle satışlar ve stok sekmeleri için oldukça belirleyici olabilir. Kılavuzda gösterilen sütun sayısını sınırlandırmak için sütun grupları **Varsayılan sipariş ayarları** &gt; **Sütun görüntüsü** menüsündeki düğmeler kullanılarak gizlenebilir veya görüntülenebilir.

### <a name="specific-order-settings-for-released-product-variant"></a>Serbest bırakılan ürün çeşidi için özel sipariş ayarları

Varsayılan sipariş ayarları için kural sisteminde sorun yaşanıyorsa her bir ürün çeşidi için varsayılan sipariş ayarlarını tanımlama seçeneği vardır. Aşağıdaki örnekler, bunun yukarıda tanımlanan üründe ve durumlarda nasıl kullanılacağını gösterir.

| Derece | Tesis | Yapılandırma | Stil | Satınalma: Varsayılan ayarları geçersiz kıl | Satınalma sağlama süresi | Satınalma: Durduruldu | Satışlar: Varsayılan ayarları geçersiz kıl | Satışlar: Durduruldu |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Evet                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Evet                                  | 5                  | Evet                | Evet                               | Evet             |
| 10   |      | C2            | R1    | Evet                                  | 5                  | Evet                | Evet                               | Evet             |
| 10   |      | C1            | R3    | Evet                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Evet                                  | 2                  | Evet                | Evet                               | Evet             |
| 10   |      | C1            | R1    | Evet                                  | 2                  | Evet                | Evet                               | Evet             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Bu durumda derecenin bir önemi yoktur, bu nedenle onu gizlemeyi seçebilirsiniz. Bu çözüm, bakım sorunlarına neden olma potansiyeline sahiptir. Ancak, Ürün Yaşam Döngüsü Yönetimi (PLM) sistemleri ile tümleştirmeyi düşünüyorsanız bu ayarı kullanmayı düşünmek isteyebilirsiniz.



