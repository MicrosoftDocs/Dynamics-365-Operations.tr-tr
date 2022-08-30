---
title: Öncelik tabanlı planlama
description: Bu makalede, Microsoft Dynamics 365 Supply Chain Management'ın öncelik tabanlı planlama özelliği açıklanmaktadır.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e17e45f1d4e9f7c62317eac6f3ea1be84017b562
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335300"
---
# <a name="priority-based-planning"></a>Öncelik tabanlı planlama

[!include [banner](../../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Supply Chain Management'ın öncelik tabanlı planlama özelliği açıklanmaktadır. Özellik, [Talep Temelli Malzeme Gereksinimleri Planlaması (DDMRP)](ddmrp-overview.md) adımı olan talep temelli planlamaya destek ekler. Önceliğe dayalı planlama, Planlama Optimizasyonu için, gereksinim tarihleri yerine öncelikler planlama ile çalışan planlı siparişler oluşturma olanağı sağlar.

Önceliğe dayalı planlama, acil talebin, daha az önemli talebe göre öncelik uygulandığından emin olmak için stok yenileme emirlerinin önceliğini belirlemenizi sağlar. Örneğin, bir stok bitimi yenileme siparişinin standart bir dolum stok yenileme siparişi üzerinden öncelikli olması gerekir. Sistem, daha büyük siparişleri otomatik olarak sipariş satırlarının önceliğine göre gruplandırıldığında farklı küçük siparişlere bölebilir. Daha sonra, tüm yüksek öncelikli siparişleri önce işleyebilir.

Bu özelliğe hızlı bir genel bakış için, şu videoya bakın: [Dynamics 365 Supply Chain Management'ta öncelik temelli planlama için en planlama optimizasyonu desteği](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Sisteminizde önceliğe dayalı planlamayı açın

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Master planlama*
- **Özellik adı:** *Planlama Optimizasyonu için önceliği temel alan MRP desteği*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Planlama önceliklerinin nerede ve nasıl atandığı

Tedarik ve talebe ilişkin *planlama öncelik* bilgileri, öncelik tabanlı planlamanın omurgasıdır. Planlama önceliği, bir talep veya tedarik satırının önemini tanımlar. Planlama Optimizasyonu, **Karşılama kodu** alanı *Öncelik* olarak ayarlandığında bunu kullanır.

Planlama önceliği genellikle 0 (sıfır) ile 100 arasında bir sayıdır (burada 0, en yüksek önemi temsil eder). Bu, **Planlama önceliği** alanında görüntülenir ve ayarlanır. Bu alanı, aşağıdaki sayfalarda bulabilirsiniz: **Talep tahmin satırları**, **Satış siparişi ayrıntıları**, **Satınalma siparişi detayları**, **Transfer emri detayları** ve **Planlı sipariş ayrıntıları**.

İlgili madde veya karşılama grubunun **Karşılama kodu** alanı *Öncelik* olarak ayarlandığında, Planlama Optimizasyonu planlama önceliğini hesaplarken talebe göre tedariki desteklemek için talep temelli bir yaklaşım kullanır ve her serbest bırakılan ürün için **Madde karşılama** sayfasındaki **Minimum**, **Yeniden sipariş noktası** ve **Maksimum** alanları için belirlenen değerleri göz önünde bulundurur.

> [!NOTE]
> *Öncelik* değeri yalnızca, Planlama Optimizasyonu etkinleştirildiğinde **Karşılama kodu** alanı için kullanılabilir.

İlgili *planlama önceliği modelleri* planlama önceliğini denetler ve planlı siparişleri öncelik aralığına göre böler. Bunlar aynı zamanda, her tedarik veya talep türü için varsayılan planlama öncelik değerlerini ayarlamanıza ve öncelik hesaplama yöntemini tanımlamanıza olanak sağlarlar.

## <a name="types-of-priority-calculation-methods"></a>Öncelik hesaplama yöntemi türleri

Her planlama önceliği modelinde, master planlamanın planlı siparişlere öncelik nasıl uygulayacağını kontrol eden bir **Öncelik hesaplama yöntemi** ayarı vardır. Kullanılabilir değerler *Maksimum stok miktarı yüzdesi* ve *Öncelik aralıkları*'dır. *Öncelik aralıkları*, *Maksimum stok miktarı yüzdesi* yöntemi olan daha gelişmiş bir sürümü temsil eder.

### <a name="percent-of-maximum-inventory-quantity"></a>Maksimum stok miktarının yüzdesi

*Maksimum stok miktarı yüzdesi* hesaplama yönteminde, tedarik önceliği hesaplaması bir madde için ayarlanan **Maksimum stok miktarı** değerinin yüzdesi olarak geçerli *toplam kullanılabilir stoğu* (net akış) bulur. Böylece her madde ve satıcı için tek bir planlı sipariş oluşturulur (maksimum sipariş miktarı, bir bölünmeye zorlamak için kullanılmaz). Siparişin planlama önceliği maksimum bir yüzde olarak hesaplanır.

Aşağıdaki formül kullanılır:

*Maksimum yüzde* = (*Net akış konumu* × 100) ÷ *Madde karşılamasının maksimum stok miktarı değeri*

Bu formülde, *Net akış konumu* aşağıdaki şekilde hesaplanır:

*Net akış pozisyonu* = *Eldeki* + *Siparişteki* – *Nitelikli talep*

- *Siparişteki*, beklenen tedariktir.
- *Nitelikli talep*, planlama zaman dilimi içinde gereksinim tarihine sahip net gereksinimleri gösterir.

Master planlama çalışması sırasında, yeni planlı siparişler, net akış konumu bir maddenin yeniden sipariş noktası miktarından az olduğunda oluşturulur. Planlı sipariş miktarı, madde düzeyinde ve net akış konumunda ayarlanan **Maksimum stok miktarı** değeri arasındaki farktır. Planlı sipariş önceliği, **Maksimum stok miktarı** değerinin *net akış pozisyonu* yüzdesi olarak hesaplanır.

> [!NOTE]
> Talep toplam tedariği aşıyorsa bile hesaplanan öncelik negatif olamaz. Talep, toplam tedariği aşıyorsa, hesaplanan öncelik 0 (sıfır) olarak ayarlanır.

### <a name="priority-ranges"></a>Öncelik aralıkları

*Öncelik aralıkları* hesaplama yöntemi, *Maksimum stok miktarı yüzdesi* değerinden daha ileri düzeyde olup planlama önceliği modeli düzeyinde konfigüre edilir. Her madde için talebi karşılamak üzere birçok yeni planlı tedarik emri oluşturulabilir. Planlanan tedarikin öncelikleri, **Planlama önceliği modelleri** sayfasındaki **Planlama öncelik aralıkları** kılavuzunda tanımlanan değerleri izler.

**Öncelik hesaplama yöntemi** alanı, *Öncelik aralıklarına* ayarlandığında aşağıdaki ek kurallar etkili olur:

- Planlanan öncelik modeli için **Talep önceliğini dikkate al** seçeneği *Evet* olarak ayarlanmışsa, her bir talep satırında ayarlanan öncelik, öncelik aralığı aralığını sınırlar. Tedarik için yeni bir planlı siparişin önceliği talebin önceliğinden düşük olmaz. Aralığın üst değeri, talebin öncelik değerinin karşılaştırıldığı bir eşik olarak kabul edilir. Talebin önceliği iki aralığın üst eşik değerleri arasında tam olarak ortasındaysa, en yüksek önceliğe (yani en düşük öncelik değerine) sahip aralık seçilir.
- Planlanan öncelik modeliyle ilgili **Planlı sipariş oluşturma** alanı, *En önemli önceliğe sahip tek bir tedarik* olarak ayarlanmışsa, en fazla tüm şekilde maksimum bir şekilde karşılamak için yalnızca bir tedarik oluşturulur. Öncelik, bir tedariği tetikleyecek ilk aralığın önceliğinde ayarlanacaktır.
- Eldeki stok için tedarik yok ve talep yok ise, **İlk miktar** alanının *Sıfıra* ayarlandığı **Planlama önceliği aralıkları** ızgarasında bir satır kullanılır.
- Talep varsa ancak eldeki stok veya beklenen tedarik yok ise, **İlk miktar** alanının *Sıfır veya daha aza* ayarlandığı **Planlama önceliği aralıkları** ızgarasında bir satır kullanılır.
- Talebin parçası olduğu aralık değerlendirildiğinde sonra **Talep önceliğini dikkate al** seçeneğinin ayarı hala bir etkiye sahip olacaktır.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Geleneksel zaman çizelgesi hesaplamaları ile öncelik tabanlı planlama arasındaki farklar

Öncelik tabanlı planlama, geleneksel zaman çizelgesi hesaplamalardan aşağıdaki yollarla farklılık gösterir:

- Tüm normal ön plan işlemcileri hala etkili. Bu ön işlemciler satış talebine, satınalma talebi eşlemeye ve rezervasyon mantığına karşılık gelen onaylanmış planlı siparişlerin bir kopyasını içerir. Yalnızca bu işlemciler tarafından yerine getirilmemiş talep işlenir.
- İlişkilendirme sırasında, önceliği ne olursa olsun tüm tedarik dikkate alınır. Bu tedarik, eldeki stoğu, serbest bırakılmış tedariki ve onaylı planlı siparişlerin ilişkili olmayan bölümünü içerir.
- Tüm karşılama süresi boyunca tedarikte ilişkili "negatif gün" olarak talep yapılamaz.
- Tedarik, talebe karşı ilişkilendirildiğinde, en yüksek önceliğe sahip olan tedarik (en düşük öncelik değeri) önce kullanılır. Eldeki tedarikin öncelik değeri 0 (sıfır) olarak kabul edilir. Bu nedenle, ilk kaynak olarak kullanılır.
- En düşük sipariş boyutu, maksimum sipariş boyutu, miktar çokluğu gibi normal kurallara göre yeni planlı tedarik satırları oluşturulur.

## <a name="planning-priority-models"></a>Planlama önceliği modelleri

*Planlama öncelik modelleri*, karşılama gruplarına atanır ve planlı siparişler için planlama önceliğini denetler. Bunlar planlı her sipariş için planlama öncelik değerinin nasıl hesaplandığını ve planlı siparişlere, tedarik satırlarına ve talep satırlarına nasıl atanacağını belirleyen mantığı tanımlar.

Planlama öncelik modelleriyle çalışmak için **Master planlama \> Kurulum \> Planlama öncelik modelleri**'ne gidin. Daha önce anlatıldığı gibi, bir modelin en önemli ayarlarından biri **Öncelik hesaplama yöntemi** değeridir. Bu ayar, master planlama planlı siparişlere bir öncelik değeri atarken kullanılan hesaplama yöntemini denetler.

> [!NOTE]
> Planlama öncelik modelleri, tüm yasal varlıklar arasında organizasyon çapında geçerlidir.

### <a name="coverage-group"></a>Kapsam grubu

[Maddeler için kapsam kuralları tanımlama](../tasks/define-coverage-rules-items.md)'da açıklandığı üzere, öncelik tabanlı planlama için kullanmayı planladığınız yeni bir karşılama grubu ayarlayın. Karşılama grubunu oluşturduktan sonra, aşağıdaki ek alanları ayarlayın:

- **Karşılama kodu** – Karşılama grubunun öncelik tabanlı planlamayı kullanması durumunda *Öncelik*'i seçin.
- **Planlama öncelik modeli** – Tüm organizasyon çapında planlama öncelik modelini seçin.

### <a name="item-coverage"></a>Madde karşılama

Madde karşılama ayarlarını, [Karşılama ayarlarında](../coverage-settings.md) açıklandığı şekilde ayarlayın. Karşılama grubu için seçilen **Karşılama kodu** değeri varsayılan olarak madde karşılama ayarlarına kopyalanır. Ancak, varsayılan değeri istediğiniz gibi geçersiz kılabilirsiniz. Bazı durumlarda, madde karşılama kaydına ait **Karşılama kodu** alanı *Planlama* olarak ayarlanır, ancak ilgili kapsam grubu için planlama öncelik modeli tanımlanmamıştır. Bu durumlarda, **Öncelik hesaplama yöntemi** alanının *Maksimum stok miktarının yüzdesi* olarak ayarlandığı ve **Planlı sipariş oluşturma** alanının *En önemli önceliğe sahip tek bir tedarik olarak* ayarlandığı tüm modeller varsayılan olarak uygulanacaktır.

Madde karşılama ayarlarındaki **Yeniden sipariş noktası** alanını kullanılabilir yapmak için **Karşılama kodu** alanını *Öncelik* olarak ayarlayın. Bu alana, **Karşılama kodu** değeri *Öncelik* olan planlı siparişlerin ne zaman yerleştirileceğini belirlerken, sistemin kullanması gereken yeniden sipariş noktası miktarını girin.

Yeniden sipariş noktası miktarı genellikle talep olarak sağlama süresi artı bir minimum değer (emniyet stoğu) sırasında hesaplanır. **Minimum** ve **Maksimum** değerler arasında bir değer olmalıdır.

Örneğin, alanları aşağıdaki şekilde ayarlayabilirsiniz:

- **Minimum:** *10*
- **Sipariş yenileme noktası:** *45*
- **Maksimum:** *60*

Bu örnekte, yeniden sipariş noktası miktarı, yedi günlük bir sağlama süresine ve ortalama günlük kullanım süresi 5'i temel alır. Bu nedenle, sağlama süresi içindeki talep 35'tir. Daha sonra 45 yeniden sipariş noktası almak için minimum 10 değerine (emniyet stoğu) eklenir. Bu kurulum kullanıldığında, öngörülen eldeki düzey 45'in altında olduğunda tedarik önerilir. Sipariş önceliği, planlama önceliği kurulumunu temel alır.

### <a name="manage-planning-priority-models"></a>Planlama önceliği modellerini yönetme

Planlama öncelik modellerinizde çalışmak için. aşağıdaki adımları izleyin.

1. **Master planlama \> Kurulum \> Planlama öncelik modelleri**'ne gidin.
1. Liste bölmesinden mevcut bir model seçin veya Eylem Bölmesinde **Yeni**'yi seçerek yeni bir model oluşturun.
1. Kaydın üst bilgisinde aşağıdaki alanları ayarlayın:

    - **Ad**: Model için bir ad girin. Ad, kuruluşunuzdaki tüm yasal varlıklar arasında benzersiz olmalıdır.
    - **Açıklama**: Modelin açıklamasını girin.
    - **Öncelik hesaplama yöntemi** – Aşağıdaki değerlerden birini seçin:

        - *Öncelik aralıkları* – Bu değeri seçtiğinizde, **Planlama önceliği aralıkları** grubu kullanılabilir duruma gelir. Burada, planlama öncelik değerini tanımlamak için birkaç öncelik aralığı oluşturmanız gerekir.
        - *Maksimum stok miktarının yüzdesi* – Maksimum stok miktarıyla ilgili tahmini stok düzeyini temel alarak planlama önceliği değerini yüzde olarak hesaplayın.

    - **Planlı sipariş oluşturma** – Bu alan, **Öncelik hesaplama yöntemi** alanı *Öncelik aralıklarına* ayarlandığında kullanılabilir. Aşağıdaki değerlerden birini seçin:

        - *En önemli önceliğe sahip tek tedarik* – Planlı siparişleri öncelik aralığına göre bölmeyin. Planlı bir siparişin planlama önceliği en önemli öncelik aralığına (en düşük planlama önceliği değeri) dayanır.
        - *Öncelik aralıklarına göre ayır* – Planlama öncelik aralıklarını temel alarak talebi birden fazla planlı siparişe bölün. Her planlı sipariş için planlama önceliği, ilgili planlama öncelik aralığının planlama önceliğiyle tanımlanır.

    - **Talep önceliğini dikkate al** – Tedarik için oluşturulan yeni planlı siparişin önceliğini sınırlandırmak için bu seçeneği *Evet* olarak ayarlayın. (Öncelik, ilgili talebin önceliğinde düşük olmayacak.) Bu seçeneği *Hayır* olarak ayarlarsanız , tedarik emrinin önceliği hesaplanırken talep siparişinin önceliği dikkate alınmayacak.

1. **Öncelik hesaplama yöntemi** alanını *Öncelik aralıkları* olarak ayarladıysanız, gerektiği şekilde öncelik aralığı satırları eklemek veya kaldırmak için **Planlı öncelik aralıkları** hızlı sekmesindeki **Ekle** ve **Kaldır** düğmelerini kullanın. Birden fazla satır varsa ve yeni bir satır eklerseniz, planlama önceliği otomatik olarak seçili satırın ortalaması ve üstündeki satır olarak ayarlanır. Her satır için aşağıdaki alanları ayarlayın:

    - **Planlama önceliği** – 0,00 ve 100,00 arasında herhangi bir değer girin. Bu değer, satır için kullanılan planlama önceliğini gösterir. En düşük öncelik değeri, en yüksek önceliği temsil eder. Varsayılan bir değer atanır, ancak bunu gereksinim duyduğunuz gibi değiştirebilirsiniz. Aynı **Planlama önceliği** modelinde birden fazla planlama öncelik aralığı için aynı planlama öncelik değeri kullanılamaz.
    - **Açıklama** – Planlama öncelik aralığının açıklamasını girin ( *Yeniden sipariş noktası: Maksimum* gibi).
    - **Başlangıç miktarı** – Planlama öncelik aralığının alt sınırı. Bu değer salt okunurdur ve önceki planlama öncelik aralığı için **Son miktara** ve **Son miktar değerlerinin yüzdesine** dayanır.
    - **Son miktar** - Aralığın üst limitini tanımlamak için kullanılacak madde karşılamasının alanını seçin. Aşağıdaki değerler desteklenir ve sonraki aralığın **Başlangıç miktarı** değerini etkiler:

        - *Sıfır* – Bu değer negatif ile sıfır (*Sıfır veya daha az*'dan *Sıfır*'a) aralığı temsil eder. Bu değerin seçildiği satırlar için, **Son miktar yüzdesi** alanı salt okunurdur ve her zaman yüzde *100* olarak ayarlanır.
        - *Minimum stok miktarı* – Bu değer **Madde karşılama** sayfasındaki bir madde için **Minimum** değeri temsil eder. Bu değerin seçildiği satırlar için, **Son miktar yüzdesi** alanı düzenlenebilir ve sonraki aralığın **İlk miktar** değerini ayarlamak için kullanılır (örneğin, *Minimum stok miktarının %80'ine kadar*).
        - *Yeniden sipariş noktası* – Bu değer **Madde karşılama** sayfasındaki bir madde için **Yeniden sipariş noktası** değeri temsil eder. Bu değerin seçildiği satırlar için, **Son miktar yüzdesi** alanı düzenlenebilir ve sonraki aralığın **İlk miktar** değerini ayarlamak için kullanılır (örneğin, *Yeniden sipariş noktasının %80'ine kadar*).
        - *Maksimum stok miktarı* – Bu değer **Madde karşılama** sayfasındaki bir madde için **Maksimum** değeri temsil eder. Bu değerin seçildiği satırlar için, **Son miktar yüzdesi** alanı düzenlenebilir ve sonraki aralığın **İlk miktar**'ını ayarlamak için kullanılır (örneğin, *Minimum stok miktarının %80'ine kadar*).
        - *Sonsuz* – Bu değer, aralığın sonsuz üst düzeyini (*Sonsuz veya daha az*'dan *Sonsuz*'a) temsil eder. Bu değerin seçildiği satırlar için, **Son miktar yüzdesi** alanı salt okunurdur ve her zaman yüzde *100* olarak ayarlanır.

    - **Son miktarın yüzdesi** – **Son miktar** alanında seçilen değere göre, planlama öncelik aralığının üst limitini hesaplamak için kullanılan bir yüzde değeri girin. Örneğin, **Son miktar** alanı *Minimum stok miktarı* ve **Son miktar yüzdesi** alanı da *50* olarak ayarlanmışsa, üst sınır ilgili madde karşılamasının minimum stok miktarının yüzde 50 olur.

1. **Planlama önceliği varsayılanları** hızlı sekmesinde, her bir tedarik veya talep satırı türü (satış siparişi, satınalma siparişi, transfer emri veya talep tahmini) için varsayılan planlama öncelikleri tanımlamak üzere alanları ayarlayın. Yalnızca pozitif değerler girilebilir.

## <a name="view-and-maintain-planning-priority"></a>Planlama önceliği görüntüleme ve koruma

Planlama önceliği, **Planlama önceliği** alanında görüntülenir ve ayarlanır. Bu alanı, aşağıdaki tabloda listelenen sayfalarda bulabilirsiniz. Öncelik 0 (sıfır) ile 100 arasında bir sayıdır (burada 0, en yüksek önemi temsil eder).

| Sayfa | Alan konumu | Değer kaynağı |
|---|---|---|
| Talep tahmin satırları | <p>**Madde** sekmesi</p><p>(Üst bölümde bir satır seçin ve sonra **Madde** sekmesini seçin.)</p> | Varsayılan değer veya el ile ayarlanan değer |
| Satış siparişi ayrıntıları | <p>**Satır ayrıntıları** hızlı sekmesinde, **Teslimat** sekmesi</p><p>(**Satış siparişi satırları** hızlı sekmesinde bir satır seçin ve sonra **Satır ayrıntıları** hızlı sekmesinde **Teslimat** sekmesini seçin.)</p> | Varsayılan değer, şirketlerarasından değer veya el ile ayarlanan değer |
| Satın alma siparişi ayrıntıları | <p>**Satır ayrıntıları** hızlı sekmesinde, **Teslimat** sekmesi</p><p>(**Satınalma siparişi satırları** hızlı sekmesinde bir satır seçin ve sonra **Satır ayrıntıları** hızlı sekmesinde **Teslimat** sekmesini seçin.)</p> | Değer, planlı siparişler, şirketlerarasından değer veya elle ayarlanan değerden kesinleştirme sırasında ayarlanır |
| Transfer emri ayrıntıları | <p>**Satır ayrıntıları** hızlı sekmesinde, **Teslimat** sekmesi</p><p>(**Transfer siparişi satırları** hızlı sekmesinde bir satır seçin ve sonra **Satır ayrıntıları** hızlı sekmesinde **Teslimat** sekmesini seçin.)</p> | Değer, planlı siparişler veya elle ayarlanan değerden kesinleştirme sırasında ayarlanır |
| Planlı sipariş detayları | **Genel** hızlı sekmesi | Master planlama sırasında veya el ile ayarlanan değer olarak hesaplanan değer |

### <a name="intercompany-trade"></a>Şirketlerarası ticaret

Şirketlerarası tedarik ve talep satırlarındaki **Planlama önceliği** değeri, bağlantılı varlıklar arasında paylaşılır. Her iki taraftaki değişiklik ise bağlantılı sipariş satırına yansıtılır.

Burada bazı örnekler verilmiştir:

- Bir kullanıcı, şirketlerarası satış siparişi satırı için planlama önceliğini 20'den 30'a değiştirir. Bu değişiklik, bağlantılı şirketlerarası satınalma siparişi satırına yansıtılır.
- Bir kullanıcı, şirketlerarası satınalma siparişi satırı için planlama önceliğini 40'dan 50'ye değiştirir. Bu değişiklik, bağlantılı şirketlerarası satış siparişi satırına yansıtılır.
