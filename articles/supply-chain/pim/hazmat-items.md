---
title: Ürün, sipariş, sevkiyat ve yüklerdeki tehlikeli malzemeler
description: Bu konuda serbest bırakılan ürünler için tehlikeli malzeme özelliklerini ayarlama, tehlikeli maddelerle ilgili stok limitlerini belirleme ve tehlikeli malzemeleri satış siparişine, sevkiyata veya yüke ekleme açıklanmaktadır.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 64d31cd86045ff28aa007666a3877271eecf0106
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570717"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Ürün, sipariş, sevkiyat ve yüklerdeki tehlikeli malzemeler

[!include [banner](../includes/banner.md)]

Bu konuda serbest bırakılan ürünler için tehlikeli malzeme özelliklerini ayarlama, tehlikeli maddelerle ilgili stok limitlerini belirleme ve tehlikeli malzemeleri satış siparişine, sevkiyata veya yüke ekleme açıklanmaktadır.

## <a name="set-hazardous-material-specifications-for-products"></a>Ürünlerin tehlikeli malzeme belirtimlerini ayarlama

Tehlikeli malzeme yönetmeliği tanımlayıp [Tehlikeli malzemeleri ayarlama](hazmat-setup.md) bölümünde açıklanan şekilde ilgili referans kodlarını ayarladıktan sonra bu bilgileri serbest bırakılan maddelerle ilişkilendirebilirsiniz. Sevkiyat belgelerindeki sevkiyat metni, serbest bırakılan maddeler için tehlikeli malzeme bilgilerinden çekilir.

Serbest bırakılmış maddeyi tehlikeli malzemeyle ilişkilendirme süreci kapsamında yönetmelik kodunu ve malzemeyi belirtmeniz gerekir. Teslimat şekillerine bağlı olarak bir maddeyle farklı düzenleme kodları ilişkilendirilebilir ve her bir maddeyle birden fazla yönetmelik ve malzeme kodu ilişkilendirebilirsiniz.

Serbest bırakılan ürünü tehlikeli malzeme olarak ayarlamak için aşağıdaki adımları uygulayın:

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Serbest bırakılan ürün ayrıntıları** sayfasını açmak için bir ürün oluşturun veya açın.
1. **Stok yönetimi** hızlı sekmesinde, **Tehlikeli malzeme** seçeneğini **Evet** olarak ayarlayın. Bu ayar, maddeyi tehlikeli malzeme olarak tanımlar ve sevkiyat belgesi yazdırılırken kullanılır.
1. Eylem Bölmesinde, **Stok yönetimi** sekmesindeki **Uyumluluk** grubunda **Madde tehlikeli malzemesi**'ni seçin.
1. Aşağıdaki alt bölümlerde açıklanan alanları kullanarak seçili madde için **Madde tehlikeli malzemeleri** sayfasını doldurun.

### <a name="item-hazardous-materials-header"></a>Madde tehlikeli malzemeleri üst bilgisi

Aşağıdaki tabloda **Madde tehlikeli malzemeleri** sayfasının en üst kısmındaki alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Madde kodu | Üzerinde çalıştığınız serbest bırakılmış ürün. |
| Düzenleme kodu | Ürün için geçerli olan tehlikeli malzeme yönetmeliğini seçin. Yönetmelik, yazdırılan sevkiyat metninin madde ve ilişkili teslimat şekli için nasıl oluşturulduğunu tanımlar. Kod, atandıktan sonra bu sayfada düzenlenemez. Ancak **Yeni**'yi seçerek yeni bir yönetmelik kodu atayabilirsiniz. |
| Malzeme kodu | (İsteğe bağlı) Ürün için geçerli olan tehlikeli malzeme kodunu seçin. Malzeme kodu, bu sayfadaki diğer birçok alan için varsayılan değerleri içeren bir şablon sağlar. Kod seçtiğinizde, tüm tehlikeli malzeme belirtimleri geçerli ürüne kopyalanır. Ancak, sistem ilk olarak madde malzemesi verilerinin malzeme kodundan doldurulması gerektiğini onaylamanızı ister. |
| Grup kodu | (İsteğe bağlı) Ürün için geçerli olan tehlikeli malzeme sınıflandırma grubunu seçin. **Malzeme kodu** alanında kod seçtiğinizde tüm tehlikeli malzeme belirtimleri geçerli ürüne kopyalanır. Ancak, sistem ilk olarak madde sınıf grubu verilerinin grup kodundan doldurulması gerektiğini onaylamanızı ister. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Açıklamalar hızlı sekmesi

Aşağıdaki tabloda, **Açıklamalar** hızlı sekmesinde kullanılabilecek alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Uygun sevkiyat adı | Geçerli yönetmelikte belirtildiği şekilde malzemenin standart açıklamasını girin. Bir sonraki bölümde açıklanan şekilde **Madde sevkiyat metni çevirisi** hızlı sekmesinde bu değer için çeviriler sağlayabilirsiniz. |
| Teknik ad | Malzemenin yaygın olarak kullanılan veya genel adını seçin. Bu ad, şirketinizin malzeme için şirket içinde kullandığı bir ad olabilir. |
| N.O.S. | **Uygun sevkiyat adı** değerinin, maddenin başka türlü adlandırılmayan (N.O.S.) sevkiyat adı olduğunu belirtmek için bu onay kutusunu seçin. N.O.S. sevkiyat adları, belirli son kullanımları olan ancak belirli bir yönetmelikteki tehlikeli malzeme tablosunda adıyla listelenmemiş olabilecek benzer kimyasal ve malzeme grupları için kullanılır. |

### <a name="item-ship-text-translation-fasttab"></a>Madde sevkiyat metni çevirisi hızlı sekmesi

**Madde sevkiyat metni çevirisi** hızlı sekmesi, **Açıklamalar** hızlı sekmesindeki birincil dil için tanımlı **Uygun sevkiyat adı** değerlerinin çevirilerini gösteren bir ızgara içerir. Bu çeviriler, bir veya daha fazla ek dilde sevkiyat yazılı metni için kullanılabilir.

Aşağıdaki tabloda, **Madde sevkiyat metni çevirisi** hızlı sekmesinde kullanılabilecek alanlar açıklanmaktadır.


| Alan | Tanım |
|---|---|
| Dil | Satırda kullanılan dil kodu. Örneğin, **pt-br** Brezilya Portekizcesi anlamına gelir. |
| Sevkiyat yazdırma metni | Satırda kullanılan dilde çevrilmiş **Uygun sevkiyat adı** değeri. |

Çeviri eklemek veya düzenlemek için ızgaranın üstündeki **Çeviriler**'i seçerek **Metin çevirileri** sayfasını açın. Ardından şu adımlardan birini izleyin:

- Yeni çeviri eklemek için Eylem Bölmesinde **Ekle**'yi seçin. Eklenecek dili seçin ve ardından **Çevrilmiş metin** alanına çevrilmiş metni girin.
- Mevcut bir çeviriyi düzenlemek için, **Dil** alanında bir hedef dil seçip çevrilmiş metni **Çevrilmiş metin** alanında gerektiği şekilde düzenleyin.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Malzeme yönetimi hızlı sekmesi

Aşağıdaki tabloda, **Malzeme yönetimi** hızlı sekmesinde kullanılabilecek alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Sınıf | Uyduğunuz yönetmelik tarafından tanımlanan şekilde, ürünün ait olduğu tehlikeli malzeme sınıfını seçin. Tehlikeli malzeme içeren tüm ürünlere hem bölüm hem de sınıf atamanız gerekir. |
| Tanım | **Sınıf** alanında seçilen sınıf için tanımlanan açıklama. Bu alan salt okunurdur. |
| Bölüm | Uyduğunuz yönetmelik tarafından tanımlanan şekilde, ürünün ait olduğu tehlikeli malzeme bölümünü seçin. Bölüm, sınıfın bir alt kümesidir. Tehlikeli malzeme içeren tüm ürünlere hem bölüm hem de sınıf atamanız gerekir. |
| Kimlik | Tehlikeli malzeme kimlik kodunu seçin. Genellikle, bu kod Birleşmiş Milletler (BM) standardını temel alır. |
| Ambalaj grubu | Geçerli madde için uygun ambalaj grubunu seçin. |
| Tanım | **Ambalaj grubu** alanında seçilen grup için tanımlanan açıklama. Bu alan salt okunurdur. |
| Ambalaj Açıklamaları | Geçerli ambalaj açıklama kodunu seçin. Bu kod, ürünün nasıl paketlenmesi gerektiğini gösteren açıklamanın başvurur. |
| Tehlikeli malzeme etiketleri | Ürüne uygulanması gereken geçerli tehlikeli mallar etiketine başvuran bir kod seçin. |
| Sınırlı garanti | Her bir yüke ve yük satırına dahil edilen toplam ürün ağırlığını raporlamak için bu seçeneği **Evet** olarak ayarlayın. |
| Miktar | Üründeki tehlikeli malzeme miktarını belirtilen birimde girin. Bu değer, ürünü içeren yüklerin ve sevkiyatların toplam tehlikeli malzeme puanı hesaplamasında kullanılacaktır. |
| Çarpan | Ürünü içeren her yük satırı için tehlikeli malzeme puanı hesaplanırken uygulanacak çarpanı girin. Bu değer, üründe bulunan tehlikeli malzeme türüne göre geçerli yönetmelikte belirtilir. |
| Birim | **Miktar** alanında belirtilen şekilde, üründeki tehlikeli malzemenin miktarına uygulanan ölçü birimini seçin. Bu değer, ürünü içeren yüklerin ve sevkiyatların toplam tehlikeli malzeme puanı hesaplamasında kullanılacaktır. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Tehlikeli malzeme puanının hesaplanması

**Malzeme yönetimi** hızlı sekmesinde ürün için belirtilen birçok değer, söz konusu ürünü içeren her yük satırı için *tehlikeli malzeme puanını* hesaplamak amacıyla kullanılır. Puan aşağıdaki formül kullanılarak hesaplanır:

Tehlikeli malzeme puanı = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

Formül anahtarı aşağıdaki gibidir:

- *&lt;LineQty&gt;*, yük satırı için belirtilen ürün miktarıdır.
- *&lt;HazmatQty&gt;*, **Malzeme yönetimi** hızlı sekmesindeki **Miktar** alanında ürün için belirtilen tehlikeli malzeme miktarıdır.
- *&lt;UnitConversion&gt;*, yük satırı miktarı için kullanılan birim ile **Malzeme yönetimi** hızlı sekmesindeki **Birim** alanında ürün için belirtilen birim arasında dönüşüm yapmak amacıyla kullanılan dönüştürme faktörüdür.
- *&lt;Multiplier&gt;*, **Malzeme yönetimi** hızlı sekmesindeki **Çarpan** alanında ürün için belirtilen çarpandır.

Bu puan, bu değerlerin belirtildiği bir ürün içeren her yük satırı için raporlanır. Daha fazla bilgi için bu konudaki [Tehlikeli malzeme içeren sevkiyatlar](#hazmat-shipments) ve [Tehlikeli malzeme içeren yükler](#hazmat-loads) bölümlerine bakın.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Tehlikeli malzeme ağırlığının hesaplanması

Bu konudaki [Tehlikeli malzeme içeren sevkiyatlar](#hazmat-shipments) ve [Tehlikeli malzeme içeren yükler](#hazmat-loads) bölümlerinde açıklanan şekilde, **Malzeme yönetimi** hızlı sekmesinde **Sınırlı miktar** seçeneği **Evet** olarak ayarlanmış ürünler içeren yükler ve yük satırları toplam tehlikeli malzeme ağırlığını gösterir. Tehlikeli malzeme ağırlığı aşağıdaki formül kullanılarak hesaplanır:

Tehlikeli malzeme ağırlığı = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

Formül anahtarı aşağıdaki gibidir:

- *&lt;LineQty&gt;*, yük satırı için belirtilen ürün miktarıdır.
- *&lt;ProductWeight&gt;*, ürün için belirtilen stok biriminde ürün için belirtilen net ağırlıktır.
- *&lt;UnitConversion&gt;*, yük satırı miktarı için kullanılan birim ile *&lt;ProductWeight&gt;* için kullanılan stok birimi arasında dönüşüm yapmak için kullanılan dönüştürme faktörüdür.

### <a name="transport-information-fasttab"></a>Taşıma bilgileri hızlı sekmesi

Aşağıdaki tabloda, **Taşıma bilgileri** hızlı sekmesinde kullanılabilecek alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Taşıma kategorisi | İlgili taşıma kategorisini seçin. |
| Tünel Kodu | Madde için ilgili tünel sınırlama kodunu seçin. |
| Tehlikeli madde istiflemesi | Maddenin deniz taşımacılığıyla sevk edilmesi durumunda deniz taşımacılığı istifleme yönetimi için kullanılan başvuru kodunu seçin. |
| Uçak türü | Maddenin hava taşımacılığıyla sevk edilmesi durumunda uygulanacak hava taşıtı sınırlamasını seçin. |
| Paketleme - yalnızca kargo uçağı | **Hava taşıtı türü** alanında seçilen değere bağlı olarak ürünün yalnızca yük uçağıyla sevk edilebileceği durumlarda geçerli olan ambalaj talimatları kodunu seçin. |
| Paketleme - yolcu ve kargo uçağı | **Hava taşıtı türü** alanında seçilen değere bağlı olarak, ürünün yük uçağı veya yolcu uçağıyla sevk edilebileceği durumlarda geçerli olan ambalaj talimatları kodunu seçin. |
| IATA Star | Bu hızlı sekmede girilen hava taşımacılığı belirtimlerinin Hava Taşımacılığı Birliği (IATA) tehlikeli mal standardıyla ilgili olduğunu göstermek için bu seçeneği **Evet** olarak ayarlayın. Bu alan yalnızca bilgi amaçlıdır. |
| Acil durum müdahalesi | Acil durumda malzemenin kontrol altına alınmasıyla ilgili talimatların başvurusunu içeren kodu seçin. |

### <a name="environmental-information-fasttab"></a>Çevre bilgileri hızlı sekmesi

Aşağıdaki tabloda, **Çevre bilgileri** hızlı sekmesinde kullanılabilecek alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Çevre açısından tehlikeli | Ürünün çevreye zararlı olduğunu belirtmek için bu seçeneği **Evet** olarak ayarlayın. Bu alanı, kendi raporlama amaçlarınız için kullanın. |
| Denizi kirleten madde | Ürünün deniz kirletici bir madde olduğunu belirtmek için bu seçeneği **Evet** olarak ayarlayın. Bu alanı, kendi raporlama amaçlarınız için kullanın. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Tehlikeli ürünler için stok limitleri ayarlama

Güvenlik nedenleriyle, belirli bir ürünün tek bir konumda stoklanabilecek toplam miktarını sınırlamanız gerekebilir. Serbest bırakılan bir ürünle ilgili stok limitlerini ayarlamak için aşağıdaki adımları uygulayın.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Serbest bırakılan ürün ayrıntıları** sayfasını açmak için bir ürün seçin.
1. Eylem Bölmesinde, **Stok yönetimi** sekmesindeki **Uyumluluk** grubunda **Raporlama ayrıntıları**'nı seçin.
1. **Tehlikeli stok limiti** ve **Tehlike uyarı limiti** alanlarında, seçili ürün için uygun değerleri ayarlayın.

**Tehlikeli malzeme stok limiti** raporu, depolarınızdaki tehlikeli malzeme stok düzeylerinin burada belirlenen güvenli limitlerin altında kalması için bu düzeyleri izlemenize olanak sağlar. Daha fazla bilgi için [Tehlikeli malzeme stok limiti raporu](hazmat-reports.md#stock-limit-report) konusuna bakın.

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Tehlikeli malzeme içeren satış siparişi hareketleri

Satış siparişine tehlikeli malzeme olarak sınıflandırılmış bir ürünü dahil etmek için, ilgili sevkiyat taşıyıcısını satış siparişiyle ilişkilendirmeniz gerekir. Satış siparişini açın ve **Teslimat** hızlı sekmesinde, **Sevkiyat taşıyıcısı** ile **Taşıyıcı hizmeti** alanlarını gerektiği gibi ayarlayın.

Sevkiyat taşıyıcısı, taşıma şekliyle de ilişkilidir. Bu nedenle, bu bilginin tehlikeli malzeme yönetmeliğine uygun olduğundan emin olmalısınız. Diğer bir ifadeyle, tehlikeli malzeme yönetmeliğinde belirtilen teslimat şekli satış siparişi üst bilgisindeki belirtimlerle aynı olmalıdır. Bu sayede yönetmelik, sevkiyat taşıyıcısı ve hizmet ile satış siparişinde kullanılan sevkiyat satırları arasında bağlantı kurulur.

Satış siparişi sonlandırılıp sevk edilmeye hazır olduktan sonra, ambar ve depo operasyonları arasındaki aktarımı belirtmek için ambara serbest bırakılabilir.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Tehlikeli malzeme içeren sevkiyatlar

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Her sevkiyat satırı için tehlikeli malzeme puanlarını görüntüleme

Sevkiyatın **Sevkiyat ayrıntıları** sayfasında, toplam tehlikeli malzeme ağırlığı ve ilgili sevkiyata dahil edilen her yük satırı için hesaplanan puan değerleri gösterilir. Puanları ve ağırlıkları görüntülemek için aşağıdaki adımları uygulayın.

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.
1. **Sevkiyat ayrıntıları** sayfasını açmak için bir sevkiyat seçin.
1. **Yük satırları** hızlı sekmesinde satırları denetleyin. Her satır için, aşağıdaki alanlarda tehlikeli malzeme hesaplamalarını görürsünüz:

    - **Tehlikeli malzeme puanları**: Bu alanda, yük satırının tehlikeli malzeme puanı gösterilir. Değer, ilgili yönetmelik ve serbest bırakılan ürün ayarlarında belirlenen kural ve değerlere göre hesaplanır. Hesaplama için yük satırındaki miktar alınır ve serbest bırakılan ürünün [malzeme yönetimi ayarındaki](#material-management) çarpana başvurulur.
    - **Sınırlı miktar net ağırlığı**: Bu alan, tehlikeli malzeme içermesi nedeniyle sınırlı miktar uygulanan ürünler olarak işaretlenmiş ürünler için yük satırına eklenen tehlikeli içeriğin toplam net ağırlığını gösterir. Hesaplama, serbest bırakılan ürün ayarında tehlikeli malzeme olarak işaretlenmiş ürünleri temel alır. Bir madde sınırlı miktar uygulanan madde olarak işaretlenmişse hesaplamada, her yük satırındaki miktar alınır ve serbest bırakılan ürün için [malzeme yönetimi ayarındaki](#material-management) ağırlığa başvurulur.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Sevkiyata dahil edilen tehlikeli malzemeler arasındaki uyumluluğu denetleme

Sistem, sevkiyata dahil edilen tüm tehlikeli malzemelerin birlikte sevk edilmeye uygun olup olmadığını değerlendirebilir. Sistem, uyumluluğu değerlendirmek için sevkiyata dahil edilen her bir ürüne atanmış uyumluluk grubunu denetler. Daha fazla bilgi için [Tehlikeli malzeme uyumluluk grupları](hazmat-setup.md#compatibility-groups) konusuna bakın.

Uyumluluk denetlemesini çalıştırmak için aşağıdaki adımları uygulayın.

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.
1. **Sevkiyat ayrıntıları** sayfasını açmak için bir sevkiyat seçin.
1. Eylem Bölmesinde, **Sevkiyatlar** sekmesindeki **Eylemler** grubunda **Uyumluluk denetimi**'ni seçin.

Denetimin sonuçlarını bildiren bir ileti alırsınız.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Tehlikeli malzeme içeren yükler

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Her yük satırı için tehlikeli malzeme puanlarını görüntüleme

Yükün **Yük ayrıntıları** sayfasında, toplam tehlikeli malzeme ağırlığı ile ilgili yük ve her bir yük satırı için hesaplanan puan değerleri gösterilir. Puanları ve ağırlıkları görüntülemek için aşağıdaki adımları uygulayın.

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm yükler**'e gidin.
1. **Yük ayrıntıları** sayfasını açmak için bir yük seçin. (Ayrıca, yük ayrıntılarını açmak için ilgili sevkiyattan bir bağlantı da seçebilirsiniz.)
1. **Yük** hızlı sekmesinde, aşağıdaki alanları inceleyerek tüm yükün toplam tehlikeli malzeme puanlarını ve ağırlıklarını inceleyebilirsiniz:

    - **Tehlikeli malzeme puanları**: Bu alanda, yükün tehlikeli malzeme puanı gösterilir. Değer, ilgili yönetmelik ve serbest bırakılan ürün ayarlarında belirlenen kural ve değerlere göre hesaplanır. Hesaplama için yüke dahil edilen miktar alınır ve serbest bırakılan ürünün [malzeme yönetimi ayarındaki](#material-management) çarpana başvurulur.
    - **Sınırlı miktar net ağırlığı**: Bu alan, tehlikeli malzeme içermesi nedeniyle sınırlı miktar uygulanan ürünler olarak işaretlenmiş ürünler için yüke dahil edilen tehlikeli içeriğin toplam net ağırlığını gösterir. Hesaplama, serbest bırakılan ürün ayarında tehlikeli malzeme olarak işaretlenmiş ürünleri temel alır. Bir madde sınırlı miktar uygulanan madde olarak işaretlenmişse hesaplamada, her yükteki miktar alınır ve serbest bırakılan ürün için [malzeme yönetimi ayarındaki](#material-management) ağırlığa başvurulur.

1. Satırların puanlarını ve ağırlıklarını ayrı ayrı gözden geçirmek için **Yük satırları** hızlı sekmesini seçin. Her satır için sağlanan değerler, önceki adımda açıklandığı gibi, tüm yük için sağlanan değerlere benzer.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Yüke dahil edilen tehlikeli malzemeler arasındaki uyumluluğu denetleme

Sistem, yüke dahil edilen tüm tehlikeli malzemelerin birlikte sevk edilmeye uygun olup olmadığını değerlendirebilir. Sistem, uyumluluğu değerlendirmek için yüke dahil edilen her bir ürüne atanmış uyumluluk grubunu denetler. Daha fazla bilgi için [Tehlikeli malzeme uyumluluk grupları](hazmat-setup.md#compatibility-groups) konusuna bakın.

Uyumluluk denetlemesini çalıştırmak için aşağıdaki adımları uygulayın.

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm yükler**'e gidin.
1. **Yük ayrıntıları** sayfasını açmak için bir sevkiyat seçin. (Ayrıca, yük ayrıntılarını açmak için ilgili sevkiyattan bir bağlantı da seçebilirsiniz.)
1. Eylem Bölmesinde, **Yükler** sekmesindeki **Eylemler** grubunda **Uyumluluk denetimi**'ni seçin.

Denetimin sonuçlarını bildiren bir ileti alırsınız.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]