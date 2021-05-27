---
title: Otomatik maliyet kurulumu
description: Bu konuda, çeşitli gelen seyahat düzeyleri için maliyet kurallarının nasıl ayarlanacağı açıklanmaktadır. Bu kurallara dayanarak sistem maliyetleri hesaplar ve otomatik olarak ekler. Bu nedenle, kullanıcıların maliyetleri el ile eklemesi gerekmez.
author: sherry-zheng
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d057522afbf6a6d706c51f7c9e69b656483c7eb1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021672"
---
# <a name="auto-costs-setup"></a>Otomatik maliyet kurulumu

[!include [banner](../../includes/banner.md)]

Çeşitli maliyet alanları (seyahatler, sevkiyat konteynerleri, folyolar, satın alma siparişleri, maddeler veya transfer emri satırları gibi) için maliyet kuralları ayarlamak üzere **Otomatik maliyetler** sayfasını kullanabilirsiniz. Kurallara ve kullanıcıların maliyet alanlarından biri için kayıt oluştururken seçtikleri alanlara bağlı olarak sistem maliyetleri hesaplar ve bunları otomatik olarak ekler. Bu nedenle, kullanıcıların maliyetleri el ile eklemesi gerekmez.

Otomatik maliyetlerle çalışmak için **Varış yeri maliyeti \> Maliyet kurulumu \> Otomatik maliyetler**'e gidin. Ardından, bu konunun geri kalanında açıklandığı gibi otomatik maliyet kurallarınızı ayarlayın.

## <a name="work-with-cost-areas"></a>Maliyet alanlarıyla çalışma

Otomatik maliyetler, ticari anlaşmalar veya otomatik sair giderler gibi çalışır. Her otomatik maliyet kaydı belirli bir maliyet düzeyine aittir. Çalışmak istediğiniz maliyet alanını seçmek için **Otomatik maliyetler** sayfasının liste bölmesindeki **Maliyet alanı** alanını kullanın. Liste bölmesinde yalnızca seçili maliyet alanına ait otomatik maliyetler gösterilir. Oluşturduğunuz tüm otomatik maliyetler, seçili maliyet alanına ait olacaktır.

Maliyet alanları, sistemin bir maliyet alanındaki satın alma siparişi satırlarındaki maliyetleri değerlendirmesini sağlar. Örneğin, bir sevkiyat konteyneri için bir maliyet, bu sevkiyat konteynerindeki tüm ürünlerin değerini alacaktır. İki veya daha fazla sevkiyat konteyneri varsa her sevkiyat konteyneri için aynı maliyet türü belirtilebilir. Bu nedenle, konteyner türü doğru otomatik maliyeti bulmak için kullanılabilir.

## <a name="buttons-on-the-action-pane"></a>Eylem Bölmesindeki düğmeler

Aşağıdaki tabloda, **Otomatik maliyetler** hızlı sekmesindeki araç çubuğunda yer alan düğmeler açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Düzenle | Var olan bir otomatik maliyeti düzenleyin. |
| Yeni | Bir otomatik maliyet oluşturun. |
| Delete | Otomatik maliyeti silin. |
| Kopyalama kaynağı | Var olan bir kaydı temel alan yeni bir otomatik maliyet kaydı oluşturun. Daha sonra yeni kaydı serbestçe düzenleyebilirsiniz. Bu düğme hızlı bir şekilde yeni otomatik maliyetler oluşturmanıza yardımcı olur. |
| Boyutları görüntüle | Görüntülediğiniz maliyet hareketleri için gösterilen stok boyutlarını seçebileceğiniz bir iletişim kutusu açın. Onay kutularını temizlerseniz, maliyet hareketleri için daha az stok boyutu gösterilir. Bu nedenle, hareket için daha az ayrıntı gösterilecektir. Bir otomatik maliyet için stok boyutu belirtilmişse otomatik maliyet yalnızca bir yolculuktaki madde için belirtilen stok boyutu kullanıldığında uygulanır. |

## <a name="settings-on-the-header"></a>Başlıktaki ayarlar

Başlık bölümündeki ayarların kombinasyonu, belirli bir otomatik maliyetin bir seyahate ne zaman ve nasıl ekleniyor olduğunu belirler. Bir otomatik maliyet, yalnızca otomatik maliyetin ayrıntıları bu maliyet alanının başlığındaki ayrıntılarla eşleştiğinde bir seyahate, sevkiyat konteynerine veya folyoya uygulanır. Eşleşen tüm otomatik maliyetlerin toplamı, bir yolculuğun tahmini varış yeri maliyetini belirler. Bu maliyet, gemi veya seyahatteki tüm maddelere paylaştırılır.

Aşağıdaki tabloda, başlık bölümünde görünebilecek tüm alanlar açıklanmaktadır. Ancak kullanılabilir olan belirli alanlar, maliyet alanına ve seçili olan görüntüleme boyutlarına bağlı olarak değişir.

| Alan | Tanım |
|---|---|
| **Hesap kodu** | <p>Aşağıdaki değerlerden birini seçin:</p><ul><li>**Tablo**: Maliyet kuralı yalnızca belirli bir satıcı için geçerlidir.</li><li>**Grup**: Maliyet kuralı bir satıcı grubu geçerlidir. Sistem, satıcı kaydıyla ilişkili [satıcı maliyet türü grubunu](costing-parameters-setup.md) arar.</li><li>**Tümü**: Maliyet kuralı tüm satıcılar için geçerlidir. |
| **Sevkiyat şirketi** | Maliyet kuralının geçerli olduğu satıcı veya satıcı grubunu seçin. Bu alan yalnızca **Hesap kodu** alanında *Tablo* veya *Grup*'u seçerseniz kullanılabilir. |
| **Gümrük müşaviri** | Maliyet kuralının geçerli olduğu satıcı veya satıcı grubunu seçin. Bu alan yalnızca **Hesap kodu** alanında *Tablo* veya *Grup*'u seçerseniz kullanılabilir. |
| **Madde kodu** | <p>Aşağıdaki değerlerden birini seçin:</p><ul><li>**Tablo**: Maliyet kuralı yalnızca belirli bir madde için geçerlidir.</li><li>**Grup**: Maliyet kuralı bir madde grubu geçerlidir. Sistem, madde kaydıyla ilişkili [madde maliyet türü grubunu](costing-parameters-setup.md) arar.</li><li>**Tümü**: Maliyet kuralı tüm maddeler için geçerlidir.|
| **Madde ilişkisi** | Maliyet kuralının geçerli olduğu madde veya madde grubunu seçin. Bu alan yalnızca **Madde kodu** alanında *Tablo* veya *Grup*'u seçerseniz kullanılabilir. |
| **Teslimat şekli** | Maliyet kuralının geçerli olduğu teslimat modunu (hava veya deniz gibi) seçin. |
| **Konteyner türü** | Malların sevk edileceği sevkiyat konteyneri türü. Otomatik maliyet, yalnızca otomatik maliyet kurulumundaki konteyner türü seyahat konteyner türüyle eşleşiyorsa bir seyahate uygulanabilir. |
| **Çıkış limanı** ve **Varış limanı** | Seyahatin kaynak ("çıkış") limanı ve varış noktası ("varış") limanı. (Bazı sevkiyat konteynerlerinin farklı "varış" limanı olabilir çünkü seyahat birden çok limanda durabilir.) Otomatik maliyet, yalnızca otomatik maliyet kurulumundaki "çıkış" ve "varış" limanları seyahatin "çıkış" ve "varış" limanlarıyla eşleşiyorsa bir seyahate uygulanabilir. |
| **Otomatik maliyet numarası** | Otomatik maliyet kuralının benzersiz tanımlayıcısı. Bu alanın değeri, **Varış yeri maliyeti parametreleri** sayfasında ayarlanan numara serisine göre otomatik olarak oluşturulur. |
| **Stok boyutları** | Bazı maliyet alanları, başlıkta bir veya daha fazla madde boyutu (boyut, renk, ambar ve toplu iş numarası gibi) eklemenize olanak tanır. Dahil edilmesi gereken boyutları seçmek için Eylem Bölmesinde **Görüntüleme boyutları**'nı seçin. |

## <a name="settings-on-the-lines-fasttab"></a>Satırlar hızlı sekmesindeki ayarlar

**Satırlar** hızlı sekmesinde, maliyet bir seyahatteki satın alma siparişi satırına uygulandığında kullanılabilecek her para birimi için bir satır ekleyin. 

Maddeler ve satın alma siparişleri için sistem her satın alma siparişi satırının para birimini **Satırlar** hızlı sekmesinde belirtilen para birimleriyle eşleştirecektir. Yalnızca eşleşen satır veya madde için ayarlanan maliyet değerini uygular. Satırın veya maddenin para birimi için bir satır ayarlanmazsa otomatik maliyet bu satıra veya maddeye uygulanmaz.

Diğer maliyet alanları için Satırlar hızlı sekmesindeki tüm **Satırlar** başlıkta oluşturulan değerlerle eşleşen her seyahat, sevkiyat konteyneri, folyo veya transfer emri satırı için geçerli olur.

Aşağıdaki tabloda, her satırda görünebilecek tüm alanlar açıklanmaktadır. Ancak kullanılabilir belirli alanlar, seçili olan maliyet alanına bağlı olarak değişir.

| Alan | Tanım |
|---|---|
| **Para Birimi** | Satırın geçerli olduğu para birimini seçin. Bu para birimi satın alma siparişiyle ilgilidir. Sistem bir seyahate ve seyahat satırlarına uygulanması gereken otomatik maliyetleri bulmaya çalışırken, satın alma siparişiyle aynı para birimine sahip satırı seçer. Bu alan yalnızca **Maliyet alanı** alanı *Satın alma siparişi* veya *Madde* olarak ayarlandığında kullanılabilir. |
| **Maliyet türü kodu** | Maliyet türü. |
| **Paylaştırma yöntemi** | <p>Maliyetleri satırlara dağıtmak için kullanılan yöntem. Aşağıdaki seçenekler bulunur:</p><ul><li><p>**Yüzde**: **Maliyet değeri** alanının değeri, malların toplam değeri için geçerli bir yüzdedir.</p><p>Örneğin, **Maliyet değeri** alanı *10* olarak ayarlanmışsa ve malların toplam değeri 800 TL ise maliyet değeri 80 TL'dir (= 800 TL × yüzde 10).</p></li><li>**Miktar**: Maliyet, mal miktarına göre paylaştırılır.</li><li>**Tutar**: Maliyet, malların değerine göre paylaştırılır.</li><li>**Hacim**: Maliyet, mal hacmine göre paylaştırılır. Birim, madde yöneticisinde belirtilir.</li><li>**Ağırlık**: Maliyet, malların ağırlığına göre paylaştırılır. Ağırlık ana maddede belirtilir.</li><li>**Hacimsel**: Maliyet malların hacimsel ölçümüne göre paylaştırılacaktır.</li><li><p>**Ölçüm**: Bu seçenek, bir ölçümün **Varış yeri maliyeti** modülünde belirtilmesini sağlar. Genellikle malların ayrı ayrı hacmini veya ağırlığını bilmeyen ancak **Tutar** ve **Miktar** seçeneklerinin izin verdiğinden daha doğru bir değerlendirme gerektiren kuruluşlar tarafından kullanılır. Navlun ileticisi veya aracısı, kuruluşa madde düzeyinde veya satın alma siparişi düzeyinde ağırlık veya kübik ölçüm sağlar.</p><p>Örneğin, deniz navlunu 900 TL'ye eşittir. A maddesi 800 kilogram (kg) ağırlığa ve 2 metreküp (m³) hacme sahiptir. B maddesi 100 kg ağırlığa ve 1 m³ hacme sahiptir. Maliyetler ağırlığa göre değerlendiğinde elde edilen sonuçlar şunlardır:</p><ul><li>Madde A = 800 TL</li><li>Madde B = 100 TL</li></ul><p>Maliyetler hacme göre değerlendiğinde elde edilen sonuçlar şunlardır:</p><ul><li>Madde A = 600 TL</li><li>Madde B = 300 TL</li></ul><p>**Not:** **Paylaştırma yöntemi** alanı *Ölçüm* olarak ayarlandığında, sistem hem maliyet alanı (sevkiyat konteyneri) hem de satırlar için girilen ölçümleri kullanır. Bu ölçümlerin beklenen toplam kadar eklenmesi gerekmez. Ancak, beklenen toplam kadar toplamalarını istiyorsanız toplam ölçümü gözden geçirmek için istatistikleri kullanarak bir kontrol yapabilirsiniz. Ölçüm istemi ayarı ve ölçümün sevkiyat veya konteyner düzeyinde otomatik olarak güncelleştirilmesi seyahat başlığında ayarlanır.</p></li></ul> |
| **Başlangıç tarihi** | Bir tarih aralığı varsa maliyetlendirme için tarih aralığının başlangıcını belirtin. Bu tarih, otomatik maliyetin uygulanacağı ilk tarihtir. |
| **Bitiş tarihi** | Bir tarih aralığı varsa maliyetlendirme için tarih aralığının sonunu belirtin. Bu tarih, otomatik maliyetin uygulanacağı son tarihtir. |
| **Kategori** | <p>Maliyeti hesaplamak için kullanılması gereken yöntemi seçin. Aşağıdaki seçenekler bulunur:</p><ul><li>**Düzeltildi**: Maliyet, değerlendirme yöntemine göre tahsis edilecektir.</li><li>**Parçalar**: Maliyet parça başına tahsis edilecektir. Bu nedenle, paylaştırma yöntemi kullanılmaz.</li><li>**Yüzde**: Malların değerinin bir yüzdesi eklenecektir. Bu nedenle, paylaştırma yöntemi kullanılmaz.</li><li>**Oran**: Miktar kırılımları varsa bu seçeneği belirleyin. Satırın **Paylaştırma yöntemi** alanı *Ölçüm* olarak ayarlanmalıdır.</li><ul> |
| **Miktara göre döküm** | <p>**Satırlar** hızlı sekmesinde **Miktar sonları** düğmesini kullanılabilir hale getirmek için bu onay kutusunu işaretleyin. Miktar sonları, seyahatin satın alma siparişi satırındaki miktara bağlı olarak maliyetin dökümünün alınmasını ve farklı maliyetlerin değişiklik göstermesini sağlar. Bu işlevsellik genellikle teslimat modu hava olduğunda kullanılır. Satırın **Kategori** alanı *Oran* olarak ayarlanmalıdır.</p><p>Miktar, **Paylaştırma yöntemi** alanında seçilen seçenekle ilgilidir. Maliyet değeri, **Maliyet değeri** alanına girilen miktara kadar olur.<p>Örneğin, 45-100 kg'lık miktarlar ölçüm başına (kg/m³ gibi) 6,00 TL ücret üretir. 100 kg'ı aşan miktarlar ölçüm başına (kg/m³ gibi) 5,50 TL ücret üretir.</p> |
| **Maliyet değeri** | Maliyet değerini girin. |
| **Maliyet para birimi kodu** | Maliyetin para birimini seçin. |
| **Madde satış vergisi grubu** | Maliyetin vergi kodunu seçin. |
| **Minimum maliyet** | <p>Bu alan yalnızca **Miktara göre döküm** onay kutusu seçiliyse uygulanır. Ölçüm bu değere ulaşmazsa **Miktar sonları** sayfasında belirtilen maliyetlerden bağımsız olarak minimum değer seçilir.<p>Örneğin, 0-45 kg'lık miktarlar ölçüm başına (kg/m³ gibi) 6 TL ücret üretir. 46-100 kg'lık miktarlar ölçüm başına (kg / m³) 5,50 TL ücret üretir. 2 kg sevk edilirse miktar sonu 12 TL maliyet değeri oluşturur. Ancak, **Minimum maliyet** alanı *100 TL* olarak ayarlanırsa son maliyet 100 TL olur.</p> |
| **Topla** | Kullanıcıların bu maliyeti sevkiyat konteyneri düzeyinden seyahat düzeyine taşımasına izin vermek için bu onay kutusunu işaretleyin. Bu durumda, maliyetler otomatik olarak sevkiyat konteyneri düzeyinde hesaplanabilir. Bununla birlikte, tek tek sevkiyat konteynerlerindeki tüm maddeler yerine, bir seyahatteki tüm konteynerlerdeki tüm maddeler birleştirilebilir ve paylaştırılabilir. |
| **Bağlı maliyet türü** | <p>Bağlamak istediğiniz satırın **Maliyet türü kodu** değerini belirterek geçerli satırı aynı otomatik maliyet kaydındaki başka bir satıra bağlayın. Bu işlevsellik yalnızca geçerli satırın **Kategori** alanı *Yüzde* olarak ayarlandığında kullanılabilir. Geçerli satır başka bir satıra bağlandığında, geçerli satırın maliyeti diğer satırın maliyetini temel alacaktır.</p><p>Örneğin, navlun 1000 TL ve yakıt ek ücretinin navlun maliyetinin yüzde 10'u olmasını istiyorsunuz. Bu durumda, satırın **Kategori** değeri *Yüzde*, **Maliyet değeri** değeri *%10* ve **Bağlantılı maliyet türü** değeri *Navlun* olmalıdır.</p> |
| **Değer düzeltmesi** ve **Düzeltme tutarı** | <p>Çeşitli yüzde değerlerinin değerini ve tutarını ayarlamak için bu alanları kullanın. Bunlar yalnızca **Maliyet alanı** alanı *Madde* olarak ayarlandığında kullanılabilir.</p><p>Bir maddenin farklı bileşenleri için farklı maliyetlendirme ayarlanabilir. Bir maddenin bir bileşeni, o maddenin diğer bileşenlerinden farklı bir maliyet yüzdesine sahip olabilir. Bu yaklaşım, bazen malların belirli bir kısmına farklı oranlarda değer vermek için gereklidir.</p><p>Örneğin, bir saat için görev iki oranda hesaplanır: saatin bir bileşeni yüzde 10, ikinci bileşeni ise yüzde 2'lik bir görev oranına sahiptir. Bu durumda, maliyetlendirme iki bileşen arasında bölünür.</p><p>Maliyet madde için hesaplanır ancak maliyet değeri farklı maliyet kategorisine sahip bileşenlerin değerine göre ayarlanır. Kalan bileşenlerin maliyeti daha sonra önceki hesaplamanın ayarlanan tutarı kullanılarak hesaplanabilir.</p><p>Örneğin, saatin A bileşeni 9,50 TL ve vergisi yüzde 10, B bileşeninin maliyeti ise 0,50 TL ve vergisi yüzde 2'dir. Bu nedenle, toplam maliyet 10,00 TL'dir. İlk giriş yüzde 10 satırı içindir. Aşağıdaki değerler kullanılır:</p><ul><li>**Kategori:** *Yüzde*</li><li>**Maliyet değeri:** *10*</li><li>**Değer düzeltildi:** *Şuna göre düzelt*</li><li>**Düzeltilen değer:** *-0,50*</li></ul><p>Bu düzen, yüzde 10'luk bir vergi gideri hesaplanmadan önce maddenin maliyetinin (10 TL) 0,50 TL (bileşen B fiyatı) düşürülmesi gerektiğini belirtir. Bu nedenle, 9,50 TL'ye yüzde 10 uygulanır.</p><p>İkinci giriş yüzde 2'lik satır içindir (önceki girişin düzeltildiği 0,50 TL). Aşağıdaki değerler kullanılır:</p><ul><li>**Kategori:** *Yüzde*</li><li>**Maliyet değeri:** *2*</li><li>**Değer düzeltildi:** *Kullan*</li><li>**Düzeltme:** *0,50*</li></ul><p>Bu düzen, B bileşeni için ödenecek kalan vergiyi hesaplar.</p> |
