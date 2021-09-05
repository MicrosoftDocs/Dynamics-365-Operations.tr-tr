---
title: Stok Görünürlüğü uygulaması
description: Bu konuda, Stok Görünürlüğü uygulamasının nasıl kullanılacağı açıklanmaktadır.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: cc09dd82547ec42041889e9a96662cd17549a3ea
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345014"
---
# <a name="inventory-visibility-app"></a>Stok Görünürlüğü uygulaması

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Bu konuda, Stok Görünürlüğü uygulamasının nasıl kullanılacağı açıklanmaktadır.

Stok görünürlüğü, görselleştirme için bir model temelli uygulama sağlar. Uygulama üç sayfa içerir: **Yapılandırma**, **Operasyonel görünürlük** ve **Stok özeti**. Aşağıdaki özelliklere sahiptir:

- Eldeki yapılandırma ve geçici rezervasyon yapılandırması için bir kullanıcı arabirimi (UI) sağlar.
- Çeşitli boyut birleşimlerinde gerçek zamanlı eldeki stok sorgularını destekler.
- Rezervasyon taleplerini deftere nakletmek için bir kullanıcı arabirimi sağlar.
- Tüm boyutlarla birlikte ürünler için eldeki stokların özelleştirilmiş görünümünü sağlar

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce, Stok Görünürlüğü Eklentisini [Stok Görünürlüğü'nü ayarlama](inventory-visibility-setup.md) bölümünde açıklandığı gibi yükleyin ve ayarlayın.

## <a name="configuration"></a><a name="configuration"></a>Konfigürasyon

**Yapılandırma** sayfası eldeki yapılandırmayı ve geçici rezervasyon yapılandırmasını ayarlamanıza yardımcı olur. Eklenti yüklendikten sonra varsayılan yapılandırma, Microsoft Dynamics 365 Supply Chain Management'tan (`fno` veri kaynağı) alınan değeri içerir. Varsayılan ayarı inceleyebilirsiniz. Ek olarak, iş gereksinimlerinize ve harici sisteminizin stok deftere nakil gereksinimlerine göre yapılandırmayı, [Dataverse](/powerapps/maker/common-data-service/data-platform-intro) stok değişikliklerinin çoklu sistemler arasında deftere nakledilme, düzenlenme ve sorgulanma şeklini standartlaştırmak için değiştirebilirsiniz.

### <a name="define-data-sources"></a>Veri kaynaklarını tanımlama

Stok Görünürlüğüyle entegre etmek istediğiniz her bir *veri kaynağını* tanımlarsınız. Stok Görünürlüğü, satış noktası (POS) sisteminiz, Supply Chain Management ve diğer harici sistemler gibi çeşitli veri kaynaklarıyla tümleştirmeyi destekler. Varsayılan olarak Supply Chain Management, Stok Görünürlüğü'nde varsayılan veri kaynağı (`fno`) olarak ayarlanır.

Veri kaynağı eklemek için şu adımları izleyin.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Veri Kaynağı** sekmesinde, bir veri kaynağı eklemek için **Yeni Veri Kaynağı**'nı seçin.

> [!NOTE]
> Bir veri kaynağı eklediğinizde, Stok Görünürlüğü hizmetinin yapılandırmasını güncelleştirmeden önce veri kaynağı adınızı, fiziksel ölçüleri ve boyut eşlemelerini doğrulamaya dikkat edin. **Yapılandırmayı Güncelleştirme**'yi seçtikten sonra bu ayarları değiştiremezsiniz.

### <a name="set-up-dimension-mappings"></a>Boyut eşlemelerini ayarlama

Stok Görünürlüğü, veri kaynağınızın boyutlarından eşlenebilir temel boyutların listesini sağlar. Eşleme için otuz üç boyut kullanılabilir.

- Varsayılan olarak, veri kaynaklarınızdan biri olarak Supply Chain Management kullanıyorsanız 13 boyut, Supply Chain Management standart boyutlarıyla eşlenir. Diğer on iki boyut (`inventDimension1` aracılığıyla `inventDimension12`) Supply Chain Management'ta özel boyutlara eşlenir. Kalan sekiz boyut, harici veri kaynaklarıyla eşleyebileceğiniz genişletilmiş boyutlardır.
- Supply Chain Management'ı veri kaynaklarınızdan biri olarak kullanmıyorsanız boyutları serbestçe eşleyebilirsiniz. Aşağıdaki tabloda, kullanılabilir boyutların tam listesi gösterilmektedir.

> [!NOTE]
> Boyutunuz varsayılan boyut listesinde değilse ve harici bir veri kaynağı kullanıyorsanız eşlemeyi yapmak için `ExtendedDimension1` aracılığıyla `ExtendedDimension8` kullanmanızı öneririz.

| Boyut türü | Boyut adı |
|---|---|
| Ürün | `ColorId` |
| Ürün | `SizeId` |
| Ürün | `StyleId` |
| Ürün | `ConfigId` |
| İzleme | `BatchId` |
| İzleme | `SerialId` |
| Yer | `LocationId` |
| Yer | `SiteId` |
| Stok Durumu | `StatusId` |
| Ambara Özel | `WMSLocationId` |
| Ambara Özel | `WMSPalletId` |
| Ambara Özel | `LicensePlateId` |
| Diğer | `VersionId` |
| Stok (Özel) | `InventDimension1` - `InventDimension12` |
| Diğer | `ExtendedDimension1` - `ExtendedDimension8` |

Boyut eşlemeleri eklemek için şu adımları izleyin.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Veri Kaynağı** sekmesinde, **Boyut Eşlemeleri** bölümünde, boyut eşlemeleri eklemek için **Ekle**'yi seçin.
1. **Boyut Adı** alanında, kaynak boyutunu belirtin.
1. **Temel Boyuta** alanında, Stok Görünürlüğü'nde eşleştirmek istediğiniz boyutu seçin.
1. **Kaydet**'i seçin.

![Boyut eşlemeleri ekleme](media/inventory-visibility-dimension-mapping.png "Boyut eşlemeleri ekleme")

Örneğin, veri kaynağınız bir ürün rengi boyutu içeriyorsa bunu `exterchannel` veri kaynağına bir `ProductColor` özel boyutu eklemek için `ColorId` temel boyutuyla eşleyebilirsiniz. Ardından `ColorId` temel boyutuyla eşlenir.

## <a name="create-a-physical-measure"></a>Fiziksel ölçü oluşturma

Veri kaynağı, Stok Görünürlüğü'ne bir stok değişikliğini naklettiğinde bu değişikliği *fiziksel ölçüler* kullanarak nakleder. Fiziksel ölçüler, özetlenen stok işlem durumlarını yansıtan değiştiricilerdir. Sorgular fiziksel ölçülere göre olabilir.

Stok Görünürlüğü'nde, varsayılan fiziksel ölçülerin listesi vardır. Bu varsayılan fiziksel ölçüler, Supply Chain Management'taki **Eldekilerin listesi** sayfasındaki stok hareket durumlarından alınır (**Stok yönetimi \> Sorgular ve Raporlar \> Eldekilerin listesi**).

| Değiştirici | Kuruluş adı |
|---|---|
| `PhysicalInvent` | Fiziksel Stok |
| `ReservPhysical` | Fiziksel Olarak Rezerve Edilmiş Miktar |
| `AvailPhysical` | Kullanılabilir Fiziksel Miktar |
| `ReservOrdered` | Sipariş Edilen Rezerve Miktar |
| `PostedQty` | Deftere Nakledilen Miktar |
| `Deducted` | Düşülen |
| `Picked` | Çekildi |
| `Received` | Teslim alındı |
| `Registered` | Kayıtlı |
| `Arrived` | Gelen |
| `Ordered` | Sipariş edilen |
| `OnOrder` | Siparişte |
| `QuotationReceipt` | Teklif Girişi |
| `QuotationIssue` | Teklif Çıkışı |

Veri kaynağı, Supply Chain Management ise varsayılan fiziksel ölçüleri yeniden oluşturmanız gerekmez. Ancak, harici veri kaynakları için aşağıdaki adımları izleyerek yeni fiziksel ölçüler oluşturabilirsiniz.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Veri kaynağı** sekmesinde, **Fiziksel ölçüler** bölümünde **Ekle**'yi seçin, bir kaynak ölçüsü adı belirtin ve değişikliklerinizi kaydedin.

## <a name="define-the-product-hierarchy-index"></a>Ürün hiyerarşi dizinini tanımlama

Toplu boyut gruplarını ayarlayarak, eldeki stok durumunu sorgulamak için Stok Görünürlüğü'nü kullanabilirsiniz. Stok Görünürlüğü'nde, her boyut grubu bir *dizin* olarak bilinir. Her dizin bir küme numarasına karşılık gelir. Stok Görünürlüğü'nün sorgulanma şeklini temel alarak, dizinleme ayarlamak için hangi boyutları kullanılacağınıza karar verebilirsiniz.

Ürün hiyerarşi dizininizi ayarlamak için şu adımları izleyin.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Ürün Hiyerarşi Dizini** sekmesinde, **Boyut Eşlemeleri** bölümünde, boyut eşlemeleri eklemek için **Ekle**'yi seçin.
1. Varsayılan olarak, dizinlerin bir listesi sağlanır. Var olan bir dizini değiştirmek için ilgili dizin bölümünde **Düzenle** veya **Ekle**'yi seçin. Yeni bir dizin kümesi oluşturmak için **Yeni dizin kümesi**'ni seçin. Her dizin kümesindeki her bir satır için **Boyut** alanında, temel boyutlar listesinden seçim yapın. Aşağıdaki alanlar için değerler otomatik olarak oluşturulur:

    - **Küme numarası**: Aynı kümeye (dizin) ait boyutlar birlikte gruplanır ve bunlara aynı küme numarası atanır.
    - **Hiyerarşi**: Hiyerarşi, bir boyut grubunda (dizin) sorgulanabilen desteklenen boyut birleşimlerini tanımlamak için kullanılır. Örneğin, *Stil*, *Renk* ve *Boyut* hiyerarşi sırasına sahip bir boyut grubu ayarlarsanız sistem üç sorgu grubunun sonucunu destekler. İlk grup sadece stildir. İkinci grup stil ve renk birleşimidir. Üçüncü grup stil, renk ve boyutun bir birleşimidir. Diğer birleşimler desteklenmez.

Daha fazla bilgi için bkz. [Ürün dizini hiyerarşi yapılandırması](inventory-visibility-configuration.md#index-configuration).

### <a name="example"></a>Örnek

Bu bölüm, hiyerarşinin nasıl çalıştığını gösteren bir örnek sağlar. Aşağıdaki tabloda, bu örnek için kullanılabilir stokun bir listesi verilmiştir.

| Ürün | Stil | Renk | Boyut | Miktar |
|---|---|---|---|---|
| I0001 | Geniş | Siyah | Küçük | 1 |
| I0001 | Geniş | Siyah | Büyük | 2 |
| I0001 | Geniş | Kırmızı | Küçük | 3 |
| I0001 | Normal | Siyah | Küçük | 4 |
| I0001 | Normal | Siyah | Büyük | 5 |
| I0001 | Normal | Kırmızı | Küçük | 6 |
| I0001 | Normal | Kırmızı | Büyük | 7 |

Aşağıdaki tabloda, dizin hiyerarşisinin nasıl ayarlanacağı gösterilmektedir.

| Anahtar | Küme numarası | Hiyerarşi |
|---|---|---|
| `StyleId` | 1 | 1 |
| `ColorId` | 1 | 2 |
| `SizeId` | 1 | 3 |

Önceki ayarlara bağlı olarak, Stok Görünürlüğü sorgusu için boyut birleşimi *Stil*, *Renk* ve *Boyut*'tur. Hiyerarşi kurulumu, harici sistemlerin eldeki stoku aşağıdaki yollarla sorgulamasına olanak tanır:

- `()`: Tümüne göre gruplandırılmıştır. Çıktı aşağıdaki gibidir:

    - I0001, 28

- `(StyleId)`: Stile göre gruplandır. Çıktı aşağıdaki gibidir:

    - I0001, Geniş, 6
    - I0001, Normal, 22

- `(StyleId, ColorId)`: Stil ve renk birleşimine göre gruplandırılmıştır. Çıktı aşağıdaki gibidir:

    - I0001, Geniş, Siyah, 3
    - I0001, Geniş, Kırmızı, 3
    - I0001, Normal, Siyah, 9
    - I0001, Normal, Kırmızı, 13

- `(StyleId, ColorId, SizeId)`: Stil ve renk birleşimine göre gruplandırılmıştır. Çıktı aşağıdaki gibidir:

    - I0001, Geniş, Siyah, Küçük, 1
    - I0001, Geniş, Siyah, Büyük, 2
    - I0001, Geniş, Kırmızı, Küçük, 3
    - I0001, Normal, Siyah, Küçük, 4
    - I0001, Normal, Siyah, Büyük, 5
    - I0001, Normal, Kırmızı, Küçük, 6
    - I0001, Normal, Kırmızı, Büyük, 7

## <a name="set-up-a-custom-calculated-measure"></a>Özel hesaplanmış bir ölçü ayarlama

Hem stok fiziksel ölçülerini hem de *özel hesaplanmış ölçüleri* sorgulamak için Stok Görünürlüğü'nü kullanabilirsiniz.

Yapılandırma, toplam toplu çıkış miktarını elde etmek için eklenen veya çıkartılan bir dizi değiştirici tanımlamanızı sağlar.

1. Power Apps ortamınızda oturum açın ve **Stok Görünürlüğü**'nü açın.
1. **Yapılandırma** sayfasını açın.
1. **Hesaplanan Ölçü** sekmesinde, hesaplanmış bir ölçü eklemek için **Yeni Hesaplanmış Ölçü**'yü seçin. Ardından, alanları aşağıdaki tabloda açıklandığı gibi ayarlayın.

    | Alan | Değer |
    |---|---|
    | Yeni hesaplanan ölçü adı | Hesaplanan ölçünün adını girin. |
    | Veri kaynağı | Sorgulama sistemi bir veri kaynağıdır. |
    | Değiştirici veri kaynağı | Değiştiricinin veri kaynağını girin. |
    | Değiştirici | Değiştirici adını girin. |
    | Değiştirici türü | Değiştirici türünü seçin (*Toplama* veya *Çıkarma*). |

Aşağıdaki tabloda, `MyCustomAvailableforReservation` özel hesaplanmış ölçüye bir örnek gösterilmiştir. Bu örnek hakkında daha fazla bilgi için bkz. [Veri kaynağı yapılandırması](inventory-visibility-configuration.md#data-source-configuration).

| Hesaplanan ölçü veri kaynağı | Hesaplanan ölçü | Değiştirici veri kaynağı | Değiştirici | Değiştirici türü |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `Outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `Exteexterchannelrchannel` | `reserved` | `Subtraction` |

### <a name="set-up-a-soft-reservation-mapping"></a><a name="setup-reservation-mapping"></a>Geçici rezervasyon eşlemesi ayarlama

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

**Geçici Rezervasyon Eşlemesi** sekmesini düzenleyebilmeniz için **Özellik Yönetimi** sekmesinde *OnHandReservation* özelliğini açmalısınız.

Fiziksel ölçüden hesaplanan ölçüye eşlemeyi ayarlayarak, Stok Görünürlüğü hizmetinin fiziksel ölçüye göre rezervasyon kullanılabilirliğini otomatik olarak doğrulamasını sağlarsınız.

Bu eşlemeyi ayarlamadan önce, fiziksel ölçüler, hesaplanmış ölçüler ve bunların veri kaynakları, Power Apps'te (bu konuda daha önce açıklandığı gibi) **Yapılandırma** sayfasının **Veri kaynağı** ve **Hesaplanan ölçü** sekmelerinde tanımlanmalıdır.

Geçici rezervasyon eşlemesini tanımlamak için şu adımları izleyin.

1. Geçici rezervasyon ölçüsü olarak hizmet eden fiziksel ölçüyü tanımlayın (örneğin, `softreservordered`).
1. **Yapılandırma** sayfasının **Hesaplanan ölçü** sekmesinde, fiziksel ölçüyle eşlemek istediğiniz AFR hesaplama formülünü içeren *rezerve edilebilir* (AFR) hesaplanmış ölçüyü tanımlayın. Örneğin, `availforreserv`'i (rezerve edilebilir) önceden tanımlanmış `softreservordered` fiziksel ölçüsüyle eşlenecek şekilde ayarlayabilirsiniz. Bu şekilde, `softreservordered` stok durumuna sahip olan hangi miktarların rezerve edilebileceğini bulabilirsiniz. Aşağıdaki tabloda, AFR hesaplama formülü gösterilmektedir.

    | Değiştirici | Veri kaynağı | Ölçü |
    |---|---|---|
    | `Addition` | `fno` | `availphysical` |
    | `Addition` | `pos` | `inbound` |
    | `Subtraction` | `pos` | `outbound` |
    | `Subtraction` | `iv` | `softreservordered` |

1. **Yapılandırma** sayfasını açın.
1. **Geçici rezervasyon eşlemesi** sekmesinde, fiziksel ölçüden hesaplanan ölçüye eşlemeyi ayarlayın. Önceki örnek için `availforreserv`'i önceden tanımlanmış `softreservordered` fiziksel ölçüsüyle eşleştirmek için aşağıdaki ayarları kullanabilirsiniz.

    | Fiziksel ölçü veri kaynağı | Fiziksel ölçü | Rezerve edilebilir veri kaynağı | Rezerve edilebilir hesaplanan ölçü |
    |---|---|---|---|
    | `iv` | `softreservordered` | `iv` | `availforreserv` |

### <a name="set-up-a-soft-reservation-hierarchy"></a><a name="setup-reservation-hierarchy"></a>Geçici rezervasyon hiyerarşisi ayarlama

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

**Geçici Rezervasyon Hiyerarşisi** sekmesini düzenleyebilmeniz için **Özellik Yönetimi** sekmesinde *OnHandReservation* özelliğini açmalısınız.

Rezervasyon hiyerarşisi, rezervasyonlar yapıldığında belirtilmesi gereken boyutların sırasını açıklar. Ürün dizini hiyerarşisinin eldeki sorgular için çalıştığı şekilde çalışır.

Rezervasyon hiyerarşisi, eldeki dizin hiyerarşisinden farklı olabilir. Bu bağımsızlık, kullanıcıların daha hassas rezervasyonlar yapmak için gereksinimleri belirtmek üzere boyutları bölebilecekleri kategori yönetimi uygulamalarına olanak tanır.

#### <a name="example"></a>Örnek

Sisteminizde aşağıdaki rezervasyon hiyerarşisi ayarlandı.

| Boyut | Hiyerarşi |
|---|---|
| `ColorId` | 1 |
| `SizeId ` | 2 |
| `StyleId` | 3 |

Bu rezervasyon hiyerarşisi verildiğinde, rezervasyonu aşağıdaki boyut sıralarında yapabilirsiniz:

- `()`: Hiçbir boyut verilmedi.
- `(ColorId)`
- `(ColorId, SizeId)`
- `(ColorId, SizeId, StyleId)`

Boyut sırası, rezervasyon hiyerarşi sırasını ve boyuta göre boyutu kesin olarak izlemelidir. Örneğin, `(ColorId, StyleId)` olan rezervasyonlara bu örnekte izin verilmeyecektir çünkü bu sıra, rezervasyon hiyerarşisinde tanımlanmamıştır.

### <a name="control-feature-management"></a><a name="feature-switch"></a>Özellik yönetimi denetimi

Stok Görünürlüğü Eklentisi, *OnHandReservation* ve *OnHandMostSpecificBackgroundService* gibi özellikler sağlar. Varsayılan olarak, bu özellikler kapalıdır. Bunları kullanmak için Power Apps'te **Yapılandırma** sayfasını açın ve ardından **Özellik yönetimi** sekmesinde bunları açın.

### <a name="complete-and-update-the-configuration"></a>Yapılandırmayı tamamlama ve güncelleştirme

Yapılandırmayı tamamladıktan sonra, Stok Görünürlüğü'nde tüm değişiklikleri uygulamalısınız. Değişiklikleri kaydetmek için Power Apps'te **Yapılandırma** sayfasının sağ üst köşesinde **Yapılandırmayı Güncelleştirme**'yi seçin.

**Yapılandırmayı Güncelleştirme**'yi ilk kez seçtiğinizde sistem, kimlik bilgilerinizi ister.

- **İstemci Kimliği**: Stok Görünürlüğü için oluşturduğunuz Azure uygulaması kimliği.
- **Kiracı kimliği**: Azure kiracısı kimliğiniz.
- **İstemci Gizli Anahtarı**: Stok Görünürlüğü için oluşturduğunuz Azure uygulaması kimliği.

Oturum açtıktan sonra, Stok Görünürlüğü hizmetinde yapılandırma güncelleştirilir.

> [!NOTE]
> Stok Görünürlüğü hizmetinin yapılandırmasını güncelleştirmeden önce veri kaynağı adınızı, fiziksel ölçülerinizi ve boyut eşlemelerinizi doğruladığınızdan emin olun. **Yapılandırmayı Güncelleştirme**'yi seçtikten sonra bu ayarları değiştiremezsiniz.

### <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Hizmet uç noktasını bulma

Doğru Stok Görünürlüğü hizmeti uç noktasını bilmiyorsanız Power Apps'te **Yapılandırma** sayfasını açın ve ardından sağ üst köşedeki **Hizmet Uç Noktasını Göster**'i seçin. Sayfa doğru hizmet uç noktasını gösterir.

## <a name="operational-visibility"></a>Operasyonel görünürlük

**Operasyonel Görünürlük** sayfası, çeşitli boyut birleşimlerine göre gerçek zamanlı eldeki stok sorgusunun sonuçlarını sağlar. *OnHandReservation* özelliği açıldığında, **Operasyonel Görünürlük** sayfasından da rezervasyon isteklerini deftere nakledebilirsiniz.

### <a name="on-hand-query"></a>Eldeki sorgu

**Eldeki Sorgu** sekmesi, gerçek zamanlı eldeki stok sorgusunun sonuçlarını gösterir.

**Eldeki Sorgu** sekmesini seçtiğinizde sistem, Stok Görünürlüğü hizmetini sorgulamak için gereken taşıyıcı belirteci alabilmesi için kimlik bilgilerinizi ister. Taşıyıcı belirtecini, **BearerToken** alanına yapıştırabilir ve iletişim kutusunu kapatabilirsiniz. Ardından, eldeki sorgu isteğini deftere nakledebilirsiniz.

Taşıyıcı belirteci geçerli değilse veya süresi dolmuşsa **BearerToken** alanına yeni bir tane yapıştırmanız gerekir. **İstemci Kimliği**, **Kiracı Kimliği**, **İstemci Gizli Anahtarı**'nın doğru değerlerini girin ve ardından **Yenile**'yi seçin. Sistem otomatik olarak yeni ve geçerli bir taşıyıcı belirteci alır.

Eldeki sorgusunu deftere nakletmek için sorguyu istek gövdesine girin. [Nakletme yöntemini kullanarak sorgulama](inventory-visibility-api.md#query-with-post-method) içinde açıklanan modeli kullanın.

![Eldeki sorgu ayarları](media/inventory-visibility-query-settings.png "Eldeki sorgu ayarları")

### <a name="reservation-posting"></a>Rezervasyonun deftere nakli

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Rezervasyon isteğini deftere nakletmek için **Rezervasyonun Deftere Nakli** sekmesini kullanın. Rezervasyon isteğini deftere nakletmeden önce *OnHandReservation* özelliğini açmalısınız. Bu özellik hakkında daha fazla bilgi için bkz. [Stok Görünürlüğü rezervasyonları](inventory-visibility-reservations.md).

Rezervasyon isteğini deftere nakletmek için talep gövdesine bir değer girmelisiniz. [Rezervasyon olayı oluşturma](inventory-visibility-api.md#create-one-reservation-event) bölümünde açıklanan modeli kullanın. Ardından **Deftere Naklet**'i seçin. İstek yanıtı ayrıntılarını görüntülemek için **Ayrıntıları Göster**'i seçin. Ayrıca yanıt ayrıntılarından **reservationId** değerini de alabilirsiniz.

## <a name="inventory-summary"></a>Stok özeti

**Stok özeti**, *Eldeki Stok Toplamı Varlığı* için özelleştirilmiş bir görünümdür. Tüm boyutlarla birlikte ürünler için bir stok özeti sağlar. Dataverse'in sağladığı **Gelişmiş Filtre**'yi kullanarak, sizin için önemli olan satırları gösteren kişisel bir görünüm oluşturabilirsiniz. Gelişmiş filtre seçenekleri, basitten karmaşığa doğru geniş aralıklı görünümler oluşturmanıza olanak tanır. Ayrıca filtrelere gruplanmış ve iç içe koşullar eklemenize de olanak tanır.

**Gelişmiş Filtre**'nin nasıl kullanılacağı hakkında daha fazla bilgi edinmek için bkz. [Gelişmiş ızgara filtrelerini kullanarak kişisel görünümleri düzenleme veya oluşturma](/powerapps/user/grid-filters-advanced)

Özelleştirilmiş görünümün üst kısmında üç alan bulunur: **Varsayılan Boyut**, **Özel Boyut** ve **Ölçü**. Hangi sütunların görünür olduğunu denetlemek için bu alanları kullanabilirsiniz.

Geçerli sonucu filtrelemek veya sıralamak için sütun başlığını seçebilirsiniz.

Özelleştirilmiş görünümün alt kısmında "50 kayıt (29 seçili)" veya "50 kayıt" gibi bilgiler gösterilir. Bu bilgi, **Gelişmiş Filtre** sonucundan şu anda yüklenen kayıtları ifade eder. "29 seçili" metni, yüklenen kayıtlar için sütun başlığı filtresi kullanılarak seçilen kayıtların sayısını ifade eder.

Görünümün altında, Dataverse'ten daha fazla kayıt yüklemek için kullanabileceğiniz bir **Daha fazla yükle** düğmesi vardır. Yüklenen varsayılan kayıt sayısı 50'dir. **Daha fazla yükle**'yi seçtiğinizde, sonraki 1.000 kullanılabilir kayıt görünüme yüklenir. **Daha Fazlasını Yükle** düğmesindeki sayı, o anda yüklü olan kayıtları ve **Gelişmiş Filtre** sonucu için toplam kayıt sayısını gösterir.

![Stok Özeti](media/inventory-visibility-onhand-list.png "Stok Özeti")
