---
title: Seyahatleri yönetme
description: Bu konu, seyahatlerle nasıl çalışılacağını açıklamaktadır. Bir seyahat genellikle bir gemiyi temsil eder. Ancak uygulamalarınıza ve prosedürlerinize bağlı olarak bir satıcıyı, satın alma siparişini veya kuruluşunuz için anlamlı olan başka bir maddeyi temsil edebilir.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7d85ef86351f5d6ac662bb72c88d464fba82f561
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696180"
---
# <a name="manage-voyages"></a>Seyahatleri yönetme

[!include [banner](../../includes/banner.md)]

Bir seyahat genellikle bir gemiyi temsil eder. Ancak uygulamalarınıza ve prosedürlerinize bağlı olarak bir satıcıyı, satın alma siparişini veya kuruluşunuz için anlamlı olan başka bir maddeyi temsil edebilir.

**Tüm seyahatler** sayfası seyahat ayrıntıları, teslimat ve maliyet bilgileri ile maddeler, satın alma siparişleri ve transfer emirleri hakkında bilgi sağlar. **Tüm seyahatler** sayfasını açmak için **Varış yeri maliyeti \> Seyahatler \> Tüm seyahatler**'e gidin. Bu sayfa tüm güncel seyahatlerin listesini göstermektedir. Seyahatler oluşturmak, silmek ve seyahatlerle çalışmak için Eylem Bölmesindeki düğmeleri kullanabilirsiniz. Ayrıntılarını görüntülemek için listeden herhangi bir seyahat seçin.

> [!NOTE]
> Sevkiyat konteynerleri ve folyolar bir seyahate bağlıdır. Satın alma satırları bir sevkiyat konteynerine bağlıdır. Sevkiyat konteynerleri ve folyolar kapalıysa doğrudan bir seyahate de bağlanabilirler. Ayrıca, buraya girilen maliyetler tüm eklenmiş satın alma satırlarına tahsis edilir.

## <a name="action-pane"></a>Eylem Bölmesi

**Seyahatler** sayfasının Eylem Bölmesi, seçili bir seyahatle çalışmanıza olanak sağlayan düğmeler sağlar. Her düğme tek bir eylem gerçekleştirir. Eylem Bölmesi, her biri sırayla bir dizi ilgili düğme sağlayan sekmeler de içerir. Belirtilen durumlar dışında, tüm düğmeler ve sekmeler hem **Tüm seyahatler** sayfasının liste görünümünde hem de seçilen tek bir seyahat için ayrıntılı görünümde kullanılabilir.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Doğrudan Eylem Bölmesinde görünen düğmeler

Aşağıdaki tabloda, doğrudan Eylem Bölmesinde bulunan düğmeler açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Yeni | Seyahat oluşturun. <!-- KFM: Link to scenario --> |
| Delete | Geçerli seyahati silin. Yalnızca *Onaylandı* seyahat durumuna sahip seyahatler silinebilir. Bir seyahat limandan ayrıldıktan ve transitteki malları işledikten sonra, artık silinemez. |
| Seyahat düzenleyici | Seyahat için satın alma satırları ekleyebileceğiniz veya kaldırabileceğiniz yeni konteynerler oluşturabileceğiniz ve seyahatin ayrıntılarını değiştirebileceğiniz **Seyahat düzenleyici** sayfasını açın. |
| Seyahat maliyetleri | Seyahatteki tüm malları görüntüleyebileceğiniz ve bunlara seyahat maliyetleri ekleyebileceğiniz **Seyahat maliyetleri** sayfasını açın. Seyahat maliyetleri seyahate el ile eklendiğinde, **Maliyet sorgulama** sayfasına otomatik olarak eklenir ve **Seyahat maliyetleri** sayfasında belirtilen yönteme göre her bir mala tahsis edilir. |

### <a name="buttons-on-the-voyage-tab"></a>Seyahat sekmesindeki düğmeler

Aşağıdaki tabloda, doğrudan Eylem Bölmesinde bulunan **Seyahat** sekmesinde açıklanmaktadır. Bu sekme yalnızca **Tüm seyahatler** sayfasının liste görünümünde çalışırken kullanılabilir.

| Düğme | Tanım |
|---|---|
| Sevkiyat konteyneri | Seçili seyahatle ilişkili tüm sevkiyat konteynerlerini gösteren bir sayfa açın. Bir konteyner veya çok sayıda konteyner olabilir. |
| Folyo | Seçili seyahatle ilişkili tüm folyoları gösteren bir sayfa açın. Bir folyo ya da birçok folyo olabilir. |

### <a name="buttons-on-the-manage-tab"></a>Yönet sekmesindeki düğmeler

Aşağıdaki tabloda, doğrudan Eylem Bölmesinde bulunan **Yönet** sekmesindeki eylemler açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Belgeler alındı | **Alınan Belgeler** seçeneğinin *Evet* olarak ayarlanması için seyahati güncelleştirin. Daha fazla güncelleştirilmemesi için maddeyi ve/veya satın alma satırını kilitlemek için bu düğmeyi kullanabilirsiniz. |
| Transitte | **Seyahat durumu** alanını, **[Varış yeri maliyeti parametreleri](landed-cost-parameters.md)** sayfasında oluşturulan transit durumuna güncelleştirin. Bu işlemde başka bir mantık yoktur. Bir seyahat, [İzleme denetimi merkezindeki](delivery-information-setup.md) ayarlara bağlı olarak transit durumuna otomatik olarak güncelleştirilebilir.
| Maliyetlendirmeye hazır | **Seyahat durumu** alanını, **[ Varış yeri maliyeti parametreleri](landed-cost-parameters.md)** sayfasında oluşturulan maliyetlendirmeye hazır durumuna güncelleştirin. Tüm faturalar işlendiğinde (hem stok faturaları hem de seyahat maliyeti faturaları) ve mallar alındığında bir seyahat maliyetlendirilebilir. Bir seyahatle ilişkili tahmini maliyetler maliyetlendirilmemişse bir seyahatin maliyetini işlemeye çalıştığınızda hata oluşur. |
| Maliyetlendirildi | Tüm satın alma siparişleri ve seyahat maliyetleri için bir fatura oluştuktan sonra maliyetlendirme düzensizliklerini temizleyin. Bu düğmeyi seçtiğinizde, **Seyahat güncelleştirmesi - Maliyetlendirilmiş** iletişim kutusu görüntülenir. Burada, standart mali tarihte deftere nakletmeyi veya bir deftere nakil tarihi belirtmeyi seçebilir ve ardından eylemi çalıştırabilirsiniz. Eylemi istediğiniz kadar yeniden çalıştırabilirsiniz. **Seyahat güncelleştirmesi - Maliyetlendirilmiş** iletişim kutusunu, eylemi periyodik görev (toplu işlem) olarak çalıştıracak bir zamanlama oluşturmak için de kullanabilirsiniz. Eylemi toplu işlem olarak ayarlayarak düzenli olarak çalıştırmanızı öneririz. |
| Girişler listesini deftere naklet | Seyahatteki tüm satın alma siparişi satırları için bir giriş listesini deftere nakledin.  |
| Ürün girişini deftere naklet | Seyahatteki tüm satın alma siparişi satırları için bir ürün girişini deftere nakledin. Bir seyahatle ilişkili satın alma siparişi satırları için ürün girişi işlemi, yalnızca mallar transitteki mal işlemeden **geçmeyecekse** kullanılır. Mallar transitteki malların işlenmesinden geçecekse bir satın alma siparişi satırı için ürün girişini deftere nakletmeye çalıştığınızda hata alırsınız.  |
| Faturayı deftere naklet | Seyahatteki tüm satın alma siparişi satırları için bir faturayı deftere nakledin. Seyahatteki mallar sevkiyattaki malların işlenmesinden geçecekse satın alma siparişi satırları teslim alma işlemi yapılmadan önce faturalanır. Orijinal satın alma siparişi faturalandığında, orijinal satın alma siparişi satırlarıyla ilişkili transitteki mal siparişleri oluşturulur. Bu siparişler daha sonra ambar tarafından teslim alınabilir.  |
| Sevk transfer emri | Seyahatteki tüm transfer emri satırları için bir transfer emri seyahatini deftere nakledin. Bu düğme seçildiğinde, güncelleştirme için yalnızca transfer emirleri kullanılabilir. |
| Transfer emrini al | Seyahatteki tüm transfer emri satırları için transfer emri girişini deftere nakledin. |
| Transitteki malları al | Seyahatteki transitteki tüm sipariş satırlarını alın. Bu düğme, bir seyahatte transitteki malları almak için kullanılabilen üç seçenekten biridir. (Diğer iki seçenek, bu tablonun ilerleyen bölümlerinde açıklanan **Varış günlüğü oluştur** düğmesi ve Ambar Yönetimi mobil uygulamasıdır.) Bu seçenek en basit seçenektir ve transitteki malları transit ambarından nihai hedef ambara işler. İşlem üzerinde daha fazla kontrol isterseniz malların alımını işlemek için varış günlüğü veya mobil cihaz kullanın. |
| Otomatik maliyetleri bul | İlgili seyahat maliyetlerini bulun. Bu maliyetler zaten bulunduysa veya güncelleştirildiyse aşağıdaki iletiyi alırsınız: "Faturalanmamış maliyet satırları mevcut. Üzerine yazılmasını ister misiniz?" Oluşturma anında seyahatle ilişkili olmayan tüm maliyetler bulunacaktır. Bir seyahate bağlı olan ve faturalanan seyahat maliyetlerinin üzerine yazılmaz. |
| Varış günlüğü oluştur | <p>Konum belirten bir varış günlüğü oluşturabileceğiniz **Varış günlüğü oluştur** iletişim kutusunu açın. İletişim kutusu, aşağıdaki seçenekleri sağlar:</p><ul><li>**Transitteki mallardan oluştur** veya **Transfer emrinden oluştur**: Bu seçeneğin etiketi, transitteki malları kullanıp kullanmadığınıza bağlı olarak değişir. Seyahatle ilişkili transitteki mallar için standart bir varış günlüğü işlemenizi sağlayan bir varış günlüğü sayfası açmak için *Evet* olarak ayarlayın. Madde son hedef ambarda zaten teslim alınmışsa varış günlüğü satırlarına eklenmez.</li><li>**Miktarı başlat**: Seyahat satırında belirtilen mal miktarına bağlı olarak teslim alınacak miktarı başlatmak için bu seçeneği *Evet* olarak ayarlayın. Seyahat satırı kısmen alınmışsa bu miktar kalan miktar olacaktır. Bu seçeneği *Evet* olarak ayarlamanızı öneririz.</li><li>**Sipariş satırlarından oluştur**: Değeri sipariş satırlarından almak için bu seçeneği *Evet* olarak ayarlayın.</li></ul><p>Bu düğme, bir seyahatteki malları almak için kullanılabilen üç seçenekten biridir. (Diğer seçenekler, bu tabloda daha önce açıklanan **Transitteki malları al** düğmesi ve Ambar Yönetimi mobil uygulamasıdır.)</p> |
| Tahakkuk eden maliyetler | Maliyet türünün borç için belirtilen bir genel muhasebe hesabına sahip olduğu maliyetleri tahakkuk ettirebilirsiniz. Bu düğme genellikle stok transitteyken veya mallar teslim alındığında ve faturalandığında kullanılır. |
| Maliyetleri topla | Maliyetleri sevkiyat konteyneri seviyesinden seyahat seviyesine taşıyın. Bu düğmeyi, birden çok varlığın bir sevkiyat konteyneri veya karton alanı paylaştığı bir hizmet/sevkiyat senaryosunda kullanabilirsiniz. Örneğin, seyahat 12 metrelik bir sevkiyat konteynerine ve 6 metrelik bir sevkiyat konteynerine sahiptir ve tahsisi hacme göre yapılır. Bu durumda, 6 metrelik sevkiyat konteynerinde alanı paylaşan veya kullanan mallar/varlıklar cezalandırılabilir. Maliyetleri adil bir şekilde dağıtmak için bazı kuruluşlar maliyetleri seyahate transfer etmek ve seyahat düzeyinde tahsis yöntemine göre dağıtmak isteyebilir. |
| Seyahat şablonunu değiştir | Yolculuk şablonunu değiştirebileceğiniz bir iletişim kutusu açın. Şablonu değiştirdikten sonra seyahat maliyetleri silinir. Bu nedenle, **Otomatik maliyetleri bul**'u seçmeniz (bu tablonun önceki açıklamasına bakın) veya maliyetleri el ile yeniden eklemeniz gerekebilir. |

### <a name="buttons-on-the-general-tab"></a>Genel sekmesindeki düğmeler

Aşağıdaki tabloda, doğrudan Eylem Bölmesinde bulunan **Genel** sekmesinde açıklanmaktadır.

| Düğme | Tanım |
|---|---|
| Giriş listesi | Seyahatteki tüm satın alma siparişi satırları için ürün girişi listesini açın.  Ürün giriş listeleri işlenmediyse bu düğme kullanılamaz. |
| Ürün girişi | Ürün girişi kaydı kullanılıyorsa seyahatle ilişkili satın alma siparişi satırları için bu kaydı açın. Deftere nakledilmiş ürün girişi yoksa bu düğme kullanılamaz. Transitteki malları kullanıyorsanız ürün girişi işlemi kullanılmaz. |
| Madde varışı | Kullanılıyorsa madde varış günlüğünü açın. |
| İzleme | Bir sevkiyat konteyneri ve bir yolculuktaki malların beklenen varış tarihini güncelleştirebileceğiniz **Geliş izleme** sayfasını açın ve daha sonra satın alma siparişi satırlarının beklenen teslimat tarihlerini güncelleştirin. |
| Maliyetlerin sorgusu | <p>Bir seyahatin tüm maliyetlerini gösteren **Maliyet sorgulama** sayfasını açın.</p><p>Görünümü ayarlamak için Eylem Bölmesinde **Görünüm**'ü seçin. Düzeylerden herhangi birini, maddeyi ve maliyet türü kodunu görüntüleyebilirsiniz.</p><p>**Maliyet sorgulama** sayfasında yalnızca stok hareketleriyle doğrudan ilişkili maliyet türü kodları görünür. Maliyet türü kodlarını kaldırarak maliyetleri gruplandırıp sayfayı ayarlayabilirsiniz. Boyut ve renk kullanıyorsanız bu özellik yararlı olabilir.</p><p>**Maliyet sorgulama** sayfasında, **yalnızca Borç** alanının *Madde* olarak ayarlandığı maliyet türü kodları gösterilir.</p> |
| Transitteki mal siparişleri | Yalnızca seçili seyahat için transitteki malların kayıtlarını gösteren **Transitteki Mallar siparişleri** sayfasını açın. |

## <a name="lines-view"></a>Satırlar görünümü

**Satırlar** görünümünü açmak için bir seyahat açın ve ardından seyahat başlığının sağ üst sekmesindeki **Satırlar** sekmesini seçin.

### <a name="information-on-the-voyage-header-fasttab"></a>Seyahat başlığı hızlı sekmesi hakkında bilgi

Bir **Satırlar** görünümündeki **Seyahat başlığı** hızlı sekmesi, seyahati açıklayan temel bilgileri içerir. Bu hızlı sekmede görünen alanların çoğu, bu konuda daha sonra açıklandığı gibi **Başlık** görünümünde de görünür.

### <a name="information-on-the-voyage-lines-fasttab"></a>Seyahat satırları hızlı sekmesi hakkında bilgi

Bir seyahatin **Satırlar** görünümündeki **Seyahat satırları** hızlı sekmesi, seyahat ayrıntıları ve seyahat düzeyinde geçerli olan maliyet bilgileriyle ilgilidir. Burada, seyahate bağlı sevkiyat konteynerlerini, folyoları ve öğeleri inceleyebilirsiniz. Seyahatteki maddelerin fiyatı ve miktarı da gösterilir. İlgili bağlantıyı seçerek listelenen herhangi bir sevkiyat konteynerini veya folyoyu görüntüleyebilirsiniz.

### <a name="information-on-the-line-details-fasttab"></a>Satır ayrıntıları hızlı sekmesi hakkında bilgi

Bir seyahatin **Satırlar** görünümündeki **Satır ayrıntıları** hızlı sekmesi, **Seyahat satırları** hızlı sekmesinde halihazırda seçili olan satır hakkında daha fazla bilgi sağlar. Bu hızlı sekmenin, her satırın konteynerde kapladığı konum ve bildirilen miktarı hakkında ayrıntılar içerdiğini unutmayın.

## <a name="header-view"></a>Başlık görünümü

**Başlık** görünümünü açmak için bir seyahat açın ve seyahat başlığının sağ üst sekmesindeki **Başlık** sekmesini seçin.

### <a name="settings-on-the-general-fasttab"></a>Genel hızlı sekmesindeki ayarlar

Aşağıdaki tabloda, seyahatin **Başlık** görünümünün **Genel** hızlı sekmesinde bulunan alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Seyahat | Seyahat veya uçuş numarasını girin. |
| Defter tutma referansı | Göndericiniz veya sevkiyat merkeziniz seyahati tanımlamak için bir referans numarası (yani, göndericinin veya sevkiyat merkezinin dahili referansı) sağlıyorsa buraya girin. |
| Tekne | Gemiyi girin veya seçin. Gemi bir değer olarak listelenmiyorsa, gemi kimliğini serbest metin olarak girebilirsiniz. Bu durumda, ana tablo güncelleştirilmez, böylece gemi kimliği daha sonra bu alanda seçilebilir. |
| Seyahat harici kimliği | Seyahatin herkese açık kimliğini (uçuş numarası gibi) girin. |
| Ana hava yolu irsaliyesi/Konşimento | Ana hava yolu irsaliyesi veya konşimento numarasını girin. Bu değeri, hava yoluyla sevkiyat yaptığınızda belirtebilirsiniz. |
| Ara irsaliye/Konşimento | Sevkiyat konteyneri için ara irsaliye veya konşimento girin. |
| Kiralık | Konteynerin iade edilmesi gereken bir kiralık konteyner olduğunu belirtmek için bu onay kutusunu işaretleyin. |
| Tanım | Tanımayı kolaylaştırmak için seyahatin açıklamasını girin. |
| Seyahat durumu | Seyahatin durumu. Değerler arasında *Oluşturuldu*, *Transitte*, *Belgeler alındı* ve *Maliyetlendirildi* bulunur. Bu alan mantığa göre hesaplanmaz. Yalnızca deftere nakil eylemiyle güncelleştirilir. *Maliyetlendirildi* değeri, stok ve tüm seyahat maliyetleri için bir faturanın alındığını gösterir. Fatura alınmadığı sürece, bir seyahat *Maliyetlendirildi* durumuna ulaşamaz. |
| Satın alma siparişi durumu | Seyahatle ilişkili tüm satın alma siparişleri arasında ulaşılan en yüksek durum. |
| Belgeler alındı | Şirketinizin seyahatle ilişkili tüm belgeleri alıp almadığını gösteren bir değer. Değeri değiştirmek için Eylem Bölmesinin **Yönet** sekmesindeki **Seyahat güncelleştirmesi** grubunda **Belgeler alındı**'yı seçin. |
| Sevkiyat şirketi | Bu seyahat için sevkiyat şirketini seçin. Bu alan, otomatik maliyetleri belirlemek için kullanılabilir. |
| Kuruluş adı | **Sevkiyat şirketi** alanında seçilen şirketin adı. |
| Ölçüm | Bu alan, ölçümün otomatik maliyette belirtilmesini sağlar. Ölçümler genellikle malların tek tek hacmini veya ağırlığını bilmeyen ancak tutarın veya miktarın sağladığından daha doğru bir onay gerektiren kuruluşlar tarafından kullanılır. Navlun ileticisi ağırlık veya kübik ölçümü sağlar ve bunu bir madde veya satın alma siparişi düzeyine yerleştirebilirsiniz. Parametre seçilirse veya el ile girilirse otomatik olarak güncelleştirilebilir. |
| Ölçüm birimi | **Ölçüm** alanındaki sayı için geçerli ölçü birimi. |
| Palet sayısı | Seyahat satırındaki palet sayısını belirtin. **Varış yeri maliyeti parametreleri** sayfasının **Genel** sekmesinde **Karton sayısını otomatik olarak güncelleştir** seçeneği *Evet* olarak ayarlanırsa bu alan otomatik olarak güncelleştirilir. |

### <a name="settings-on-the-delivery-fasttab"></a>Teslimat hızlı sekmesindeki Ayarlar

Aşağıdaki tabloda, seyahatin **Başlık** görünümünün **Teslimat** hızlı sekmesinde bulunan alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Oluşturulma tarihi ve saati | Seyahat kaydının oluşturulduğu tarih ve saat. |
| Fabrikadan çıkış tarihi | Bu alan, seyahate bağlı satın alma siparişleri arasından en erken eski fabrika tarihini seçer. Eski fabrika tarihi satın alma siparişi başlığında kullanılabilir ve izleme denetimi özelliği kullanılarak güncelleştirilir. |
| Sevk tarihi | Uçağın veya geminin çıkış noktasından ayrıldığı tahmini tarih. |
| Yola çıkış tarihi | Yola çıkış tarihi genellikle uçağın veya geminin denizaşırı limandan ayrıldığı tarihtir. Sevk tarihi ve yola çıkış tarihi eşleşmek zorunda değildir. **Yola çıkış tarihi** alanı yalnızca bilgilendirme amaçlıdır. Beklenen teslimat tarihini tahmin etmek için kullanılmaz. İzleme denetimi özelliği beklenen teslim tarihini tahmin etmek için kullanılır ve bu alan izleme denetimi özelliği tarafından otomatik olarak doldurulacak şekilde ayarlanabilir. |
| Depoya giriş tarihi | Bu alan, seyahate bağlı satın alma siparişlerindeki malların satışa sunulacağı en erken tarihi seçer. |
| Tahmini teslim tarihi | Tahmini teslimat tarihi genellikle malların ambara ulaşması gereken tarihtir. Bu alan yalnızca bilgi amaçlıdır. Mallara yönelik master planlama için kullanılmaz. Satın alma siparişi satırındaki beklenen teslimat tarihi, bir seyahatteki mallara yönelik master planlama için kullanılır ve izleme denetimi özelliği kullanılarak güncelleştirilir. Bu alan, izleme denetimi özelliği tarafından doldurulacak şekilde ayarlanabilir. |
| Gerçek teslim tarihi | Seyahate bağlı mallara göre en erken teslimat tarihi. |
| Sevkiyat limanındaki ETA | Sevkiyat acenteniz tarafından sağlanan bilgilere bağlı olarak seyahatin sevkiyat limanına ulaşmasını beklediğiniz tarihi girin. |
| Alınan orijinal belgeler | Orijinal belgelerin alındığı tarihi girin. |
| Aracı tarafından önerilir | Aracının tavsiye edildiği tarihi girin. |
| Gönderilen orijinal konşimento | Orijinal konşimentonun gönderildiği tarihi girin. |
| Piyasaya sürülen mallar | Malların gümrükten çıktığı tarihi girin. |
| Müşteri randevusu | Müşterinin malların sahipliğini almasını beklediğiniz tarih olan müşteri randevu tarihini girin. |
| Ambara teslim edildi | Malların ambara teslim edildiği tarihi girin. |
| Doğrulama tarihi | Doğrulama tarihini girin. |
| Teslimat talimatları | Teslimat talimatlarının alındığı tarihi girin. |
| Teslimat şekli | Bu alan, seyahati teslim etmek için kullanılan yöntem ve bu teslimat yöntemiyle ilişkili otomatik maliyetlerin maliyet seçimi hakkında bilgi sağlar. |
| Çıkış limanı | Seyahatin çıkış yaptığı sevkiyat limanı. |
| Varış limanı | Seyahatin vardığı sevkiyat limanı. Sevkiyat konteynerleri farklı limanlara sahip olabilir çünkü gemi birden fazla limanda durabilir. Sevkiyat konteyneri düzeyinde "varış" limanını doğrulayarak bir seyahatteki her sevkiyat konteyneri için doğru liman ayrıntıları sağlarsınız. Navlunla ilişkili otomatik maliyet, sevkiyat konteyneri türü, "varış" limanı ve "çıkış" limanı kombinasyonuna göre belirlenir. |
| Yerel aracı | Bu alan yalnızca bilgi amaçlıdır. Yerel iletici satıcı tablosundan seçilebilir olmalıdır. |
| Yerel taşıma tarihi | Yerel taşımanın rezerve edildiği tarih. Bu alan, ambarın planlamasını yapmasına yardımcı olabilir. |
| Yerel taşıma saati | Yerel taşımanın rezerve edildiği saat ve süre. Bu alan, ambarın planlamasını yapmasına yardımcı olabilir. |
| Yolculuk şablonu | Seyahat için belirtilen yolculuk şablonu. Seyahat şablonu, sevkiyat konteyneri ve yolculuğunun "varış" limanını ve "çıkış" limanını girmek için kullanılır. Bu değerler, sırayla, seyahatle ilişkili otomatik maliyetleri tanımlamaya yardımcı olur. |

### <a name="settings-on-the-other-fasttab"></a>Diğer hızlı sekmedeki ayarlar

Aşağıdaki tabloda, seyahatin **Başlık** görünümünün **Diğer** hızlı sekmesinde bulunan alanlar açıklanmaktadır.

| Alan | Tanım |
|---|---|
| Açıklamalar | Seyahatle ilgili ek bilgileri girin. |
| Değerleme tarihi | Seyahate bağlı satın alma siparişleri için en erken eski fabrika tarihini seçin. |
| Bekleyen seyahat | Bunu, sevkiyatınızın veya seyahatinizin henüz ayrılıp ayrılmadığını belirtmek için kullanabilirsiniz. Bu, yalnızca bilgi amaçlıdır.  |
| Sevkiyat konteynerlerini yeniden adlandırma | Birden fazla konteyneri olan seyahatlerde, henüz alınmamış konteyner sayısı. |

## <a name="voyage-update-periodic-tasks"></a>Seyahat periyodik görevlerini güncelleştirme

**Varış yeri maliyeti** modülü, seyahatlerin çeşitli yönlerini toplu olarak güncelleştirebilen seyahatle ilgili birkaç periyodik görev içerir. Bu periyodik görevleri çalıştırmak veya zamanlamak için **Varış yeri maliyeti \> Periyodik görevler \> Seyahat güncelleştirmeleri**'ne gidin ve aşağıdaki görev türlerinden birini seçin:

- **Belgeler alındı**: Bu görev, aynı anda birkaç seyahat için **Belgeler alındı** seçeneğini *Evet* olarak ayarlamanıza olanak tanır. Güncelleştirmek istediğiniz seyahat kümesini tanımlamak için **Filtre** ayarlarını kullanın.
- **Transitte**: Bu görev, **Seyahat durumu** alanını aynı anda birkaç seyahat için **[Varış yeri maliyeti parametreleri](landed-cost-parameters.md)** sayfasında belirtilen transitte durumuna ayarlamanıza olanak tanır. Güncelleştirmek istediğiniz seyahat kümesini tanımlamak için **Filtre** ayarlarını kullanın.
- **Maliyetlendirilmeye hazır**: Bu görev, **Seyahat durumu** alanını aynı anda birkaç seyahat için **[Varış yeri maliyeti parametreleri](landed-cost-parameters.md)** sayfasında belirlenen maliyetlendirilmeye hazır olarak ayarlamanıza olanak tanır. Genellikle bu görevi normal bir zamanlamaya göre çalışacak şekilde ayarlarsınız.
- **Maliyetlendirildi**: Bu görev, **Seyahat durumu** alanını, maliyetlendirilmiş ancak seyahatte henüz güncelleştirilmemiş olmaları koşuluyla, aynı anda birkaç seyahat için **[Varış yeri maliyet parametreleri](landed-cost-parameters.md)** sayfasında belirlenen maliyetlendirildi durumuna ayarlamanıza olanak tanır. Genellikle bu görevi normal bir zamanlamaya göre çalışacak şekilde ayarlarsınız.
