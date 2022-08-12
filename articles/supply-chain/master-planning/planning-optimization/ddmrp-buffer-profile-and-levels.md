---
title: Tampon profili ve düzeyleri
description: Bu makalede her bir ayırma noktası için tutulması gereken minimum ve maksimum stok düzeylerini belirleyen tampon profilleri ve düzeyleri ile ilgili bilgi verilmektedir.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: dd72332abefd31fd391ff66931a5abae0efb08de
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186756"
---
# <a name="buffer-profile-and-levels"></a>Tampon profili ve düzeyleri

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Ayırma noktalarınızı belirledikten sonra (stratejik olarak stokta tuttuğunuz anahtar öğeler) her bir nokta için ne kadar stok (tampon) tutacağınıza karar vermeniz gerekir. Bu görev, Talep Temelli Materyal Kaynak Planlaması'nın (DDMRP) ikinci adımıdır.

## <a name="buffer-levels-and-zones"></a>Tampon düzeyleri ve bölgeleri

DDMRP'de her stok tamponu üç değer kullanılarak tanımlanır. Bunlar; minimum miktar, maksimum miktar ve yeniden sipariş noktasıdır. Bu değerler, aşağıdaki renk kodlarıyla tanımlanan üç fark bölgesi oluşturur:

- **Kırmızı bölge**: Minimum miktarın altında kalan alan. Minimum miktar, "kırmızının üstü" olarak da adlandırılır ve planlama stratejiniz stok düzeylerinizin her zaman bu nokta üzerinde kalmasını sağlamak için tasarlanmalıdır.
- **Sarı bölge**: Minimum miktar ile yeniden sipariş noktası arasında kalan alan. Yeniden sipariş noktasına "sarının üstü" de denir. Bu noktaya ulaşıldığında, sistem yeniden sipariş oluşturmalıdır.
- **Yeşil bölge**: Yeniden sipariş noktası ile maksimum miktar alasında kalan alan. Maksimum miktar, "yeşilin üstü" olarak da adlandırılır. Bu nokta, stoğun yenileneceği maksimum düzeydir.

Aşağıdaki şekilde üç renkli bölge ve bunların minimum miktar, maksimum miktar ve yeniden sipariş noktası ile ilişkisini gösterilmektedir.

![DDMRP tampon bölgeleri ve düzeyleri.](media/ddmrp-buffer-levels.png "DDMRP tampon bölgeleri ve düzeyleri")

## <a name="calculating-the-buffer-zones"></a>Tampon bölgeleri hesaplama

Bu bölümde her bir tampon bölgenin yüksekliğinin nasıl hesaplandığı açıklanmaktadır.

Genelde ilk sarı bölge hesaplanır. Bu bölge, sipariş oluşturduğunuzdan bu siparişin gelişine kadar tükettiğiniz miktarı temsil eder. Başka bir deyişle, stok yenileme sağlama süresi içinde beklenen tüketimi gösterir. Aşağıdaki eşitlik kullanılarak hesaplanır:

- **Sarı bölge** = *Günlük ortalama kullanım (ADU)* × *Ayrılmış sağlama süresi*

*Ayrılmış sağlama süresi*, ayrılmış noktaların her zaman stokta olması durumunda bir öğenin üretilmesi veya alınması için gerekli zamanı belirtir. Genelde master planlamada kullanılan *kümülatif sağlama süresinden* çok daha kısadır. Doğru tampon ayarları, ayrılmış noktaların her zaman stokta olmasını ve stok fazlası olmaması için önemlidir.

Kırmızı bölge, aşağıdaki eşitlik kullanılarak hesaplanır:

- **Kırmızı taban** = *ADU* × *Ayrılmış sağlama süresi* × *Sağlama süresi faktörü*
- **Kırmızı emniyet** = *Kırmızı taban* × *Değişkenlik faktörü*
- **Kırmızı bölge** = *Kırmızı taban* + *Kırmızı emniyet*

Yeşil bölge, aşağıdaki üç eşitlik sonucunda oluşan maksimum sonuç olarak hesaplanır:

- *Minimum sipariş miktarı*
- *ADU* × *Sipariş döngüsü*
- *ADU* × *Ayrılmış salama süresi* × *Sağlama süresi faktörü*

## <a name="calculating-average-daily-usage"></a>Günlük ortalama kullanımı hesaplama

Sistem, günlük olarak kullandığınız miktarı hesaplamak için üç yaklaşımdan birini kullanır:

- **Günlük ortalama kullanım (geçmiş)**: Bu yaklaşım, gerçek geçmiş tüketimi temel alır.
- **Günlük ortalama kullanım (ileri)**: Bu yaklaşım, gelecekteki tahmini tüketimi temel alır.
- **Ortalama günlük kullanım (karma)**: Bu yaklaşım, geçmiş ve tahmini tüketimin ağırlıklı karışımını temel alır.

### <a name="average-daily-usage-past"></a>Günlük ortalama kullanım (geçmiş)

Son ADU, belirli sayıda geçmiş gün boyunca her gün kullanılan miktarların toplanıp gün sayısına bölünerek ortalamasının alınması ile hesaplanır. Aşağıdaki çizimde geçmiş üç güne bakılarak hesaplama yapıldığında yaklaşımın nasıl çalıştığı gösterilmektedir.

![Günlü ortalama kullanım (geçmiş) grafiği.](media/ddmrp-adu-past.png "Ortalama günlük kullanım (geçmiş) grafiği")

Önceki çizimde bugün 11 Haziran ise geçmiş üç günün (8, 9 ve 10 Haziran) ADU'su 21 olarak hesaplanır.

- **ADU (geçmiş)** = (29 + 11 + 23) ÷ 3 = 21

### <a name="average-daily-usage-forward"></a>Günlük ortalama kullanım (ileri)

Yeni bir ürünle ilgili geçmiş kullanım veriniz bulunmayabilir. Bu nedenle, ileriye dönük tahmini ADU'yu (örneğin, tahmini talebe göre) kullanabilirsiniz. Aşağıdaki çizimde ileriye dönük üç güne (bugün dahil) bakılarak hesaplama yapıldığında yaklaşımın nasıl çalıştığı gösterilmektedir.

![Ortalama günlük kullanım (ileri) grafiği.](media/ddmrp-adu-forward.png "Ortalama günlük kullanım (ileri) grafiği")

Önceki çizimde bugün 11 Haziran ise önümüzdeki üç günün (11, 12 ve 13 Haziran) ADU'su 21,66 olarak hesaplanır.

- **ADU (ileri)** = (18 + 18 + 29) ÷ 3 = 21,66

### <a name="average-daily-usage-blended"></a>Ortalama günlük kullanım (karma)

Aşağıdaki çizimde gösterildiği gibi karma ADU ortalama eski kullanımı ve ortalama ileriye dönük kullanımı birleştirir.

![Ortalama günlük kullanım (karma) grafiği.](media/ddmrp-adu-blended.png "Ortalama günlük kullanım (karışık) grafiği")

Önceki çizimde bugün 11 Haziran ise geçmiş ve önümüzdeki üç günün (8-13 Haziran) karma ADU'su 21,33 olarak hesaplanır.

- **Karma ADU** = (*Geçmiş ADU* + *ileriye dönük ADU*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Tampon hesaplama faktörleri

Her bir öğe için kırmızı ve yeşil bölgelerin ne kadar büyük olması gerektiğini ayarlamak üzere iki faktör tanımlayabilirsiniz. Bu şekilde, beklenen sağlama süresi ile talep çeşitliliğini denkleştirebilirsiniz.

![Sağlama süresi ve değişkenlik faktörleri.](media/ddmrp-zone-factors.png "Sağlama süresi ve değişkenlik faktörleri")

İlk faktör, *sağlama süresi faktörüdür*. 0-1 arasında ondalık bir değer alır. Sağlama süresi ne kadar uzunsa değer o kadar küçük olur. Talebe Dayalı Enstitü, aşağıdaki aralıkları önerir:

- **Uzun sağlama süresi:** 0,20–0,40
- **Orta sağlama süresi:** 0,41 – 0,60
- **Kısa sağlama süresi:** 0,61 – 1,00

İkinci faktör ise *değişkenlik faktörüdür*. 0-1 arasında ondalık bir değer alır. Değişkenlik faktörü ne kadar büyük olursa değer o kadar küçük olur. Talebe Dayalı Enstitü, aşağıdaki aralıkları önerir:

- **Düşük değişkenlik:** 0,20 – 0,40
- **Orta değişkenlik:** 0,41 – 0,60
- **Yüksek değişkenlik:** 0,61 – 1,00

## <a name="buffer-calculation-examples"></a>Tampon hesaplama örnekleri

Bu örnek, [stok konumlandırma](ddmrp-inventory-positioning.md) verilen yastık üretim örneğinin devamı niteliğindedir. Belirtilen örnekte, aşağıdaki çizimde de gösterildiği üzere sağlama süresini 21 günden beş güne düşüren ayırma noktalarını seçmiştiniz.

![Ayrılmış sağlama süresi örneği.](media/ddmrp-bom-decoupled-lead-time-example.png "Ayrılmış sağlama süresi örneği")

Bu örnekte, ADU'nun önceki çizimde gösterildiği gibi 23 parça olarak hesaplandığını ve ayrılmış sağlama süresinin beş gün olduğunu varsayın. Bu değerleri temel alarak ve aşağıdaki eşitliği kullanarak sarı bölgeyi hesaplayabilirsiniz:

- **Sarı bölge** = *ADU* × *Ayrılmış sağlama süresi* = 115

![Sarı bölge hesaplaması örneği.](media/ddmrp-example-calc-yellow.png "Sarı bölge hesaplaması örneği")

Kırmızı bölge hesaplaması sarı bölge hesaplamasına benzer, ancak değişkenlik ve sağlama süresi de eklenir. Bu örnekte orta sağlama süresi (faktör = 0,50) ve yüksek talep değişkenliği (faktör = 0,8) gözlemlediğinizi varsayın. Bu değerler ile sarı bölge eşitliğinden gelen bileşenleri bir araya getirip aşağıdaki eşitlikleri kullanarak kırmızı bölgeyi hesaplayabilirsiniz:

- **Kırmızı taban** = *ADU* × *Ayrılmış sağlama süresi* × *Sağlama süresi faktörü* = 57,5
- **Kırmızı emniyet** = *Kırmızı taban* × *Değişkenlik faktörü* = 46
- **Kırmızı bölge** = *Kırmızı taban* + *Kırmızı emniyet* = 103,5

Parçalar tam sayı olarak sayıldığından sistem, kırmızı bölgeyi 104 parçaya (beher) yuvarlar.

![Kırmızı bölge hesaplaması örneği.](media/ddmrp-example-calc-red.png "Kırmızı bölge hesaplaması örneği")

Yeşil bölge hesaplaması da sarı bölge eşitliğinde bulunan bileşenleri içerir, ancak minimum sipariş miktarı, sipariş döngüsü ve sağlama süresi faktörünü de hesaba katar. Bu örnekte, sipariş döngüsü olmadığını (yani, sipariş sıklığı ile ilgili bir zaman kısıtlaması yok) ve minimum sipariş miktarının 10 parça olduğunu varsayın. Yeşil bölge, aşağıdaki üç eşitlikten elde edilen maksimum sonuç olarak hesaplanır:

- *Minimum sipariş miktarı* = 10
- *ADU* × *Sipariş döngüsü* = 0
- *ADU* × *Ayrılmış sağlama süresi* × *Sağlama süresi faktörü* = 57,5

Parçalar, tam sayı olarak sayıldığından sistem, yeşil bölgeyi 58 parçaya (beher) yuvarlar.

![Yeşil bölge hesaplaması örneği.](media/ddmrp-example-calc-green.png "Yeşil bölge hesaplaması örneği")

Aşağıdaki çizimde bölge hesaplama sonuçları, DDMRP'de sıklıkla kullanılan huni grafikleri ile özetlenmiştir.

![Bölge hesaplama sonuçları özeti.](media/ddmrp-example-calc-summary.png "Bölge hesaplama sonuçları özeti")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a>Dinamik düzeltmeler

Dinamik düzeltmeler, yüksek veya düşük talep dönemlerinde *talep düzeltme faktörü* uygulamanıza olanak tanır. Bu faktör, seçili dönem için tüm hesaplamalarda ADU değerini çarpar. Sonrasında, tampon bölgeler sırayla değiştirilir. Bu faktör, genellikle ilk tampon değerler oluşturulduktan sonra uygulanır. Böylelikle, bu değerleri zaman içinde ve değişen koşullara göre ayarlayabilirsiniz. Bu görev, DDMRP'nin üçüncü adımıdır.

Örneğin, Ağustos ayında tatil dönemi olması nedeniyle belirli bir yastık ürününe talep artabilir. Bu nedenle, satışların daha yüksek olması beklenir. Bu durumda, ürünün **Talep düzeltme faktörünü** Ağustos ayının tüm haftaları için *1,5* olarak değiştirebilirsiniz.

Bu şekilde, zaman içinde tampon değerleri hesaplayabilir ve sonra bu değerleri yalnızca sistemdeki bilgilerle yetinmeden ayarlayabilirsiniz. Tam bir DDMRP uygulamasında toplu iş yoluyla tampon değerleri her gün hesaplar ve bu değerleri kabul edersiniz. Sonrasında tamponları yeniden doldurmak için toplu iş olarak planlamayı çalıştırır ve planlanan siparişleri gözden geçirirsiniz.

## <a name="implement-buffers-in-supply-chain-management"></a>Tamponları Supply Chain Management'ta uygulama

Bu bölümde, tampon bölge stratejinizin Microsoft Dynamics 365 Supply Chain Management'ta nasıl uygulanacağı açıklanmaktadır. Makalenin ilk yarısında açıklanan analiz ve hesaplamaları yaptığınız varsayılmaktadır.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a>Ayırma noktası öğesi için tamponları ayarlama

Ayırma noktası için tampon değerleri ayarlamak için bu adımları izleyin.

1. Sırasıyla **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Ayırma noktası olarak ayarlanan serbest bırakılmış bir öğeyi seçin. (Daha fazla bilgi için bkz. [Stok konumlandırma](ddmrp-inventory-positioning.md).)
1. Eylem Bölmesi'nin **Plan** sekmesinde **Öğe kapsamı**'nı seçin.
1. **Öğe kapsamı** sayfasında ayırma noktası oluşturan bir öğe kapsam kaydı seçin. (Bu kayıt, ayırma noktaları oluşturmak üzere ayarlanmış bir kapsam grubunun adını gösterir.)
1. **Genel** sekmesini seçin.
1. Sistemin satış geçmişi, tahminler ve kapsam grubu ayarlarınıza bağlı olarak tampon değerlerinizi günlük olarak yeniden hesaplamasını istiyorsanız aşağıdaki adımları izleyin:

    1. **Zaman içinde tampon değerler** seçeneğini *Evet* olarak ayarlayın.
    1. Devam etmeniz halinde el ile ayarlanmış tampon ayarlarınızın (**Minimum**, **Yeniden sipariş noktası** ve **Maksimum**) sıfırlanacağı ile ilgili bir ileti kutusu görüntülenir. Yeni ayarı tutmak için **Evet**'i seçin.

    Alternatif olarak tampon ayarlarınızı yalnızca bir kez hesaplamayı veya girmeyi tercih ederseniz şu adımları izleyin:

    1. **Zaman içinde tampon değerler** seçeneğini *Hayır* olarak ayarlayın.
    1. **Minimum**, **Yeniden sipariş noktası** ve **Maksimum** alanlarını, makalede daha önce açıklandığı şekilde öğe için hesapladığınız tampon değerlerine ayarlayın.

1. Öğeye ait DDMRP hesaplamalarını ayarlamayı bitirmek için aşağıdaki alanları ayarlayın:

    - **Sipariş döngüsü**: Öğenin satınalma siparişleri arasında geçmesi gereken gün sayısını belirtin. Herhangi bir sipariş kısıtlaması yoksa değeri *0* (sıfır) olarak ayarlayın. Bu alan, makalede daha önce belirtildiği üzere maksimum miktar tampon değerini etkiler.
    - **Günlük ortalama kullanım**: Öğe için isteğe bağlı olarak tahmini bir ADU değeri girebilirsiniz. Bu alan yalnızca bilgi amaçlıdır. Bu değer, genellikle tampon hesaplamalarının bir parçası olarak otomatik olarak hesaplanır.
    - **Sipariş ani artış eşiği**: Öğenin ani sipariş artışı (olağandışı yüksek talep) olarak nitelendirilen günlük satış miktarını belirtin. Sistem bu alanı, yüksek talep dönemlerinde planlı siparişlerin yeniden sipariş miktarını artırmak için kullanır. Daha fazla bilgi için bkz. [Talebe dayalı planlama](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a>Ayrılmış sağlama sürelerini hesaplama veya girme

Sistemin [Tampon bölgelerinizi otomatik olarak hesaplamasını](#set-up-buffers) seçtiğiniz öğelerde ayrılma noktası öğesinin ayrılmış sağlama sürelerini hesaplamak veya girmek için aşağıdaki adımları izleyin.

1. Ayrılma noktası öğesinin **Öğe kapsamı** sayfasını açın. (Daha fazla bilgi için bkz. [Ayrılma noktası öğesi için tampon değerleri ayarlama](#set-up-buffers).)
1. Ayrılma noktası oluşturan öğenin kapsam kaydını seçin.
1. **Tampon değerler** sekmesini seçin.
1. Kılavuzda dönem gösterilmiyorsa Eylem Bölmesinde **Tampon değerler** sekmesinde **Dönem ekle** seçeneğini belirleyin. [Kapsam grubu](ddmrp-inventory-positioning.md) için **Minimum, maksimum ve yeniden sipariş noktası** alanlarının *Günlük* veya *Haftalık* şeklinde ayarlanmasına bağlı olarak sistem, günlük veya haftalık dönem şeklinde kılavuzu doldurur. Sistem, öğeye atanan kapsam grubu için belirtilen zaman dilimine erişmek üzere yeterli sayıda satır ekler.
1. Ayrılmış sağlama süresini hesaplamak istediğiniz zaman dilimini seçin. (Bu zaman dilimi, genellikle bugünün tarihini içeren dönemdir.)
1. Eylem Bölmesi'nin **Tampon değerler** sekmesinde **Ayrılmış sağlama süresini hesapla**'yı seçin.
1. **Ayrılmış sağlama süresini hesapla** iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Ürün reçetesi**: Hesaplamayı çalıştırmak istediğiniz ürün reçetesini (BOM) seçin.
    - **Tarih**: Hesaplamayı çalıştırmak istediğiniz tarihi seçin. Kullanılabilir ürün reçeteleri kümesi, yalnızca seçilen tarihte etkin olan ürün reçetelerini gösterecek şekilde filtrelenir.
    - **Miktar**: Hesaplamayı çalıştırmak istediğiniz miktarı girin. Kullanılabilir ürün reçeteleri kümesi, yalnızca seçilen miktara uygulanan ürün reçetelerini gösterecek şekilde filtrelenir.

1. Hesaplamayı çalıştırmak ve **Ayrılmış sağlama süresini hesapla** iletişim kutusunu kapatmak için **Tamam**'ı seçin. Artık, seçili zaman diliminin **Ayrılmış sağlama süresi** sütunu, hesaplanmış değeri gösterir.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a>Günlük ortalama kullanımı hesaplama veya girme

Sistemin [Tampon bölgelerinizi otomatik olarak hesaplamasını](#set-up-buffers) seçtiğiniz öğelerde ayrılma noktası öğesinin ADU'sunu hesaplamak veya girmek için aşağıdaki adımları izleyin.

1. Ayrılma noktası öğesinin **Öğe kapsamı** sayfasını açın. (Daha fazla bilgi için bkz. [Ayrılma noktası öğesi için tampon değerleri ayarlama](#set-up-buffers).)
1. Ayrılma noktası oluşturan öğenin kapsam kaydını seçin.
1. **Tampon değerler** sekmesini seçin.
1. Kılavuzda dönem gösterilmiyorsa Eylem Bölmesinde **Tampon değerler** sekmesinde **Dönem ekle** seçeneğini belirleyin. [Kapsam grubu](ddmrp-inventory-positioning.md) için **Minimum, maksimum ve yeniden sipariş noktası** alanlarının *Günlük* veya *Haftalık* şeklinde ayarlanmasına bağlı olarak sistem, günlük veya haftalık dönem şeklinde kılavuzu doldurur. Ayrıca, **Sağlama süresi faktörü** ve **Değişkenlik faktörü** alanları, kapsam grubundan alınır. Her satır için bu değerleri gerektiği gibi düzenleyebilirsiniz.
1. ADU değerini hesaplamak istediğiniz bir zaman dilimi seçin.
1. Eylem Bölmesi'nin **Tampon değerler** sekmesinde **Günlük ortalama kullanımı hesapla**'yı seçin. Sistem, [kapsam grubu](ddmrp-inventory-positioning.md) için tanımlandığı gibi ADU hesaplaması için gerekli verileri toplamaya çalışır.
1. Şu adımlardan birini izleyin:

    - Gerekli veriler mevcut ise hesaplama sonuçları, **Günlük ortalama kullanım** sütununa eklenir. Bu durumda, herhangi bir eylem gerekmez.
    - Gerekli veriler mevcut değilse hiçbir değer otomatik olarak eklenmez. Bu durumda, tampon değerleri hesaplamayı düşündüğünüz her bir satır için tahmini değerleri el ile girin.

### <a name="calculate-and-apply-buffer-values"></a>Tampon değerleri hesaplama ve uygulama

Sistemin [tampon bölgelerinizi otomatik olarak hesaplamasını](#set-up-buffers) seçtiğiniz öğelerde aşağıdaki adımları izleyerek tampon değerlerin hesaplanmasını el ile tetikleyebilirsiniz.

1. İlgili ayrılma noktası öğesi için bu makalede daha önce açıklandığı gibi [tampon hesaplamasın konfigüre edin](#set-up-buffers), [ayrılmış sağlama sürelerini hesaplayın veya girin](#calc-lead-time) ve ilgili tüm dönemlere ilişkin [ortalama günlük kullanımı hesaplayın veya girin](#calc-adu).
1. Ayrılma noktası öğesinin **Öğe kapsamı** sayfasını açın.
1. Zaman dilimi listesini gösteren **Tampon değerler** sekmesini seçin.
1. Tampon değerlerini hesaplamak istediğiniz zaman dilimini seçin. (Bu zaman dilimi, genellikle bugünü içine alan dönem olur.) Seçtiğiniz satırın **Günlük ortalama kullanım** ve **Ayrılmış sağlama süresi** sütunlarında sıfır dışında bir değer olmalıdır.
1. Bir veya daha fazla satır için **Talep düzeltme faktörü** alanını gerektiği gibi düzenleyin. Sistem, bu faktörü bu değerin kullanıldığı tüm tampon hesaplamalarında **Günlük ortalama kullanım** değerine uygular. Bu faktör, talebin tarihe göre nasıl dalgalanacağını ayarlamanıza olanak sağlar (örneğin, tatiller veya sezonluk öğeler için).
1. Eylem Bölmesi'nin **Tampon değerler** sekmesinde **Minimum, maksimum ve yeniden sipariş noktası miktarlarını hesapla** seçeneğini belirleyin. Sistem, hesaplama yapar ve **Öğe kapsamı** sayfasındaki kılavuzda bulunan **Hesaplanan minimum**, **Hesaplanan yeniden sipariş noktası** ve **Hesaplanan maksimum** sütunlarını doldurur.
1. Hesaplanan değerleri incelemeyi bitirdiğinizde bu değerleri uygulamalısınız. Aksi takdirde, hiçbir etkisi olmayacaktır. Bir veya daha fazla satır için hesaplama yaptığınızda **Hesaplanan minimum**, **Hesaplanan yeniden sipariş** ve **Hesaplanan maksimum** değerleri, sırasıyla **Minimum**, **Yeniden sipariş noktası** ve **Maksimum** sütunlarına kopyalanır. Eylem Bölmesi'nin **Tampon değerler** sekmesinde, **Eylem gerçekleştir** grubunda aşağıdaki düğmelerden birini seçin:

    - **Tüm hesaplamaları kabul et**: Hesaplanan tüm değerleri kılavuzda uygula.
    - **Seçili satırlar için hesaplamaları kabul et**: Hesaplanmış değerleri yalnızca seçili satırlar için uygular.
    - **Tüm hesaplamaları kaldır**: Kılavuzdaki minimum miktarlar, maksimum miktarlar ve yeniden sipariş noktaları için hesaplanmış tüm değerleri kaldırır.
    - **Seçili satırlar için tüm hesaplamaları kaldır**: Seçili satırlar için minimum miktarlar, maksimum miktarlar ve yeniden sipariş noktaları için hesaplanmış tüm değerleri kaldırır.

### <a name="schedule-automatic-buffer-value-calculations"></a>Otomatik tampon değer hesaplamalarını zamanla

DDMRP ayarlarınızı tam olarak ayarladıktan ve beklendiği gibi çalıştığını doğruladıktan sonra ADU ve ilgili tampon değerlerini fiili tüketim verileri ve/veya güncelleştirilmiş tahminlere dayalı olarak düzenli aralıklarla yeniden hesaplamak amacıyla toplu bir iş ayarlamak isteyeceksiniz. Bu işlem, yalnızca sistemin [tampon bölgelerinizi otomatik olarak hesaplamasına](#set-up-buffers) izin verdiğiniz öğeler için uygulanır.

Otomatik tampon değeri hesaplamalarını zamanlamak için bu adımları izleyin.

1. **Master planlama \> Master planlama \> DDMRP \> Tampon değerleri hesapla**'ya gidin.
1. **Tampon değerleri hesapla** iletişim kutusunda aşağıdaki alanları ayarlayın:

    - **Günlük ortalama kullanımı hesapla**: İş her çalıştığında ayrılma noktası öğelerinin ADU değerlerinin yeniden hesaplanması için bu seçeneği *Evet* olarak ayarlayın. Bu hesaplamayı atlamak için *Hayır* olarak ayarlayın. Bu seçeneği, mümkün olduğunca *Evet* olarak ayarlamanız gerekir.
    - **Ayrılmış sağlama süresini hesapla**: İş her çalıştığında ayrılmış sağlama sürelerinin yeniden hesaplanması için bu seçeneği *Evet* olarak ayarlayın. Bu hesaplamayı atlamak için *Hayır* olarak ayarlayın. Bu seçeneği, mümkün olduğunca *Evet* olarak ayarlamanız gerekir.
    - **Tampon değerleri hesapla**: İş her çalıştığında tampon değerlerin yeniden hesaplanması için bu seçeneği *Evet* olarak ayarlayın. Bu hesaplamayı atlamak için *Hayır* olarak ayarlayın. Bu seçeneği, mümkün olduğunca *Evet* olarak ayarlamanız gerekir.
    - **Minimum, maksimum ve yeniden sipariş noktası hesaplamalarını kabul et**: İş her çalıştığında yeniden hesaplanan tampon değerleri otomatik olarak onaylamak ve uygulamak için bu seçeneği *Evet* olarak ayarlayın. Yeniden hesaplanan değerleri uygulanmamış olarak bırakmak için *Hayır* olarak ayarlayın. Bu durumda, yeniden hesaplanan değerler, her bir ürünün **Öğe kapsamı** sayfasından el ile uygulanmadıkça etkili olmayacaktır. Bu seçeneği, mümkün olduğunca *Evet* olarak ayarlamanız gerekir.
    - **Master plan**: Hesaplamadan etkilenecek öğeleri içeren bir master plan seçin. Hesaplama, bu iletişim kutusundaki **Filtre** ayarlarıyla daha da sınırlı olacak plan filtresinde bulunan tüm öğeler için geçerli olacaktır.

1. Bu toplu işin üzerinde çalışması gereken kayıt kümesini sınırlandırmak için **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçerek **Sorgu** iletişim kutusunu açın. Bu iletişim kutusu, Supply Chain Management'ta bulunan diğer [arka plan işlerinde](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) çalıştığı gibi çalışır.
1. **Arka planda çalıştır** hızlı sekmesinden seçili öğeler için seçili hesaplamaların nasıl, ne zaman ve hangi sıklıkta yapılacağını belirtin. Alanlar, Supply Chain Management'ta bulunan diğer [arka plan işleri](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) için çalıştıkları gibi çalışır.
1. Yürütme için yeni işi toplu iş kuyruğuna eklemek için **Tamam**'ı seçin.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Tüm öğeler için ayrılmış sağlama sürelerini gözden geçirme ve yeniden hesaplama

Tüzel kişiliğiniz (şirket) içinde bulunan tüm ayrılmış sağlama sürelerini gözden geçirmek ve yeniden hesaplamak için aşağıdaki adımları izleyin.

1. **Master planlama \> Master planlama \> DDMRP \> Ayrılmış sağlama süresi**'ne gidin.
1. **Ayrılmış sağlama süresi** sayfasında aradığınız bilgileri bulmak için listeye göz atın ve filtre uygulayın. Öğelerle ilgili daha fazla bilgi görüntülemek için **Öğe numarası** sütunundaki bağlantıyı seçin.
1. Herhangi bir öğe için ayrılmış sağlama süresini yeniden hesaplamak isterseniz öğeyi seçin ve sonrasında Eylem Bölmesi'nde **Ayrılmış sağlama süresini hesapla** seçeneğini belirleyin. **Ayrılmış sağlama süresini hesapla** iletişim kutusu görüntülenir. Bu iletişim kutusu, aynı öğe için **Öğe kapsamı** sayfasında [ayrılmış sağlama süresini hesapladığınızdaki](#calc-lead-time) gibi çalışır.
