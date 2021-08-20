---
title: Transitteki malları işleme
description: Bu konuda, transitteki mal siparişleriyle nasıl çalışılacağı açıklanmaktadır. Transitteki malların işlenmesini kullanmak üzere bir sipariş veya seyahat ayarlandığında, mallar tüketim için ambara alınmadan önce faturalanabilir.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DeliveryTerms, InventLocation, InventPosting, ITMGoodsInTransitOrder, ITMTableListPage, ITMTable, ITMContainersListPage, ITMContainers, ITMFolioTableListPage, ITMFolioTable, ITMGoodsInTransitOrderEditLines, SysOperationTemplateForm, WHSRFMenuItem, WHSLocDirTable, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d4503b6939e3d01ae5bcf1d79c1f85d39348fbb6233cfb7a965f84f3a3b0699a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744810"
---
# <a name="goods-in-transit-processing"></a>Transitteki malları işleme

[!include [banner](../../includes/banner.md)]

Bu konuda, transitteki mal siparişleriyle nasıl çalışılacağı açıklanmaktadır. Bu tür siparişler yalnızca **Varış yeri maliyeti** modülü tarafından kullanılır. Bir sipariş veya seyahat, transitteki malları işlemek üzere ayarlandığında, malları faturalamadan önce ambara alınana kadar beklemeniz gerekmemektedir. Bunun yerine, mallar satıcının ambarı veya çıkış limanından ayrıldığında faturalanır ve seyahat başladığında mali maliyetler tanınır. Bu işlevsellik, malların sevkiyat limanından ayrıldığında genellikle kuruluşunuzun malı haline gelmesi nedeniyle stokun sahipliğini doğru bir şekilde almanızı sağlar.

Transitteki mal siparişleri kullanıldığında, mali olarak güncelleştirilmiş maddeler, transitteki mal ambarı olarak bilinen geçici bir ambara alınır. Mallar daha sonra son hedef ambara (diğer bir deyişle, satın alma satırında tanımlanan ambar) alınana kadar bu ambarda kalır. Bunlar el ile kaldırılamaz.

Maddeler transitte olduğu sürece stokta kullanılamaz ve teslimat için stoktan seçilemez. Ancak transitteki malları görüntüleyebilirsiniz. Malları master planlama için de kullanabilirsiniz. Bu durumda, stokun tüketim için kullanılabilir olacağı beklenen tarih olarak satın alma siparişi satırındaki onaylanmış teslimat tarihini kullanın.

Aşağıdaki bölümlerde, transitteki mal konseptini ve işlevselliğini kullanarak stok ve seyahatleri işlemek için gereken kurulum açıklanmaktadır.

## <a name="terms-of-delivery"></a>Teslimat koşulları

**Varış yeri maliyeti** modülünü etkinleştirdiğinizde, standart *teslimat şartları*, transitteki mal özelliğini destekleyecek şekilde geliştirilmiştir.

Geçerli teslimat şartları kaydı için **Transitteki mal yönetimi** seçeneği *Evet* olarak ayarlandığında, mallar transitteki mal ambarına konur. Bu eylem yalnızca bir fatura işlenmeden önce stok girişi işlenmezse tetiklenir. Bir siparişin teslimat şartları transitteki malları kullanacak şekilde ayarlandığında, kullanıcılar artık satın alma siparişi için bir ürün girişini deftere nakledemez. Denerlerse bir hata oluşur. Hata iletisi, devam etmek için transitteki mallar işlevini kullanmaları gerektiğini belirtir.

Transitteki malların teslimat şartları bilgileriyle çalışmak için **Satın Alma ve Tedarik \> Kurulum \> Dağıtım \> Teslimat Şartları**'na gidin. Aşağıdaki tabloda, transitteki mallar işlevselliğini desteklemek için **Varış yeri maliyeti** modülünün **Teslimat Şartları** sayfasına eklediği alanlar açıklanmaktadır. Her iki alan da **Genel** hızlı sekmesindedir. Bu sayfadaki diğer alanlar hakkında daha fazla bilgi için bkz. [Teslimat şartları (form)](/dynamicsax-2012//terms-of-delivery-form).

| Alan | Tanım |
|---|---|
| Sevkiyat limanı zorunlu | Teslimat şartları geçerli olduğunda sevkiyat limanı zorunluysa bu seçeneği *Evet* olarak ayarlayın. |
| Transitteki malların yönetimi | Teslimat şartları geçerli olduğunda transitteki mal yönetimini kullanmak için bu seçeneği *Evet* olarak ayarlayın. |

## <a name="warehouses-for-goods-in-transit-and-under-delivery"></a>Transitteki ve eksik teslimattaki mallar için depolar

**Varış yeri maliyeti** modülünü etkinleştirdiğinizde, standart *ambarlar* varlığı, mallar bir transitteki mal ambarındayken satın alma siparişlerinin faturalanmasını sağlayacak şekilde geliştirilmiştir.

Varış yeri maliyeti iki yeni ambar türü ekler: *transitteki mallar* ve *eksik teslimat*. Her iki türde ambarlar varsayılan ambarlar olarak seçilebilir. Transitteki mal siparişlerinin başarılı bir şekilde işlenmesi, hem transitteki mal ambarının hem de eksik teslimat ambarının **Ambarlar** sayfasında yapılandırılmasını gerektirir. Daha sonra, Varış yeri maliyeti ve transitteki mallarla kullanılacak her varsayılan ambar için her türdeki kullanılabilir ambar için transitteki mal ambarı ve eksik teslimat ambarı seçilmelidir.

*Transitteki mal* ambarı türü, transitteki mal ambarınızla ilişkilendirilir ve bu ambar, mallar son varış ambarında teslim alınmadan önce transit siparişlerdeki malları işlemek için kullanılır. Genel olarak, stok yönetimi için kullanılan tek stok boyutları Tesis ve Ambar ise her tesis için bir adet transitteki mal ambarı yeterlidir. Konum stok boyutu da kullanılıyorsa varsayılan konumun da belirtilebilmesi için bir tesis ve ambarın her kombinasyonu için bir transitteki mal ambarı ayarlanmalıdır.

Ambarlarınıza yönelik transitteki mal ayarlarıyla çalışmak için **Stok yönetimi \> Kurulum \> Stok dökümü \> Ambarlar**'a gidin. Aşağıdaki tabloda, **Varış yeri maliyeti** modülünün transitteki mal işlevselliğini desteklemek için **Ambarlar** sayfasına eklediği alanlar açıklanmaktadır. Her iki alan da **Genel** hızlı sekmesinde görünür. Sayfadaki diğer alanlar hakkında bilgi için bkz. [Ambarlar (form)](/dynamicsax-2012//warehouses-form).

| Alan | Tanım |
|---|---|
| Transitteki mal ambarı | Ana ambarla ilgili transitteki mal ambarını tanımlayın. |
| Eksik teslimat ambarı | Ana ambarla ilgili eksik teslimat ambarını tanımlayın. |

## <a name="posting-rules-for-landed-cost"></a>Varış yeri maliyeti için deftere nakil kuralları

Varış yeri maliyeti, yapılandırabileceğiniz iki yeni deftere nakil kuralı ekler. Bu deftere nakil kuralları, çıkış noktasından ayrıldıklarında malların sahipliğini tanımlamak için doğrudan satın alma siparişi fatura tutarlarını mali olarak deftere nakletmek için kullanılır. Bu işlem, *faturalanmamış mallar* kavramının yerini alır çünkü mallar alınmadan önce faturalanır. <!-- KFM: Add a link to the related scenario when available. -->

Deftere nakil profilleriyle çalışmak için **Stok yönetimi \> Kurulum \> Deftere Nakil \> Deftere Nakil**'e gidin. **Satın Alma Siparişi** sekmesinde, aşağıdaki yeni deftere nakil kuralları bulunur:

- **Varış yeri maliyeti, transitteki mallar**: Transitteki mal yönetimi için deftere nakil kurallarını belirtin.
- **Varış yeri maliyeti, maliyet gideri tahakkuku**: Masraf hesabı tahakkuku için deftere nakil kurallarını belirtin.

## <a name="goods-in-transit-orders"></a>Transitteki mal siparişleri

Transitteki mal siparişlerini doğrudan **Varış yeri maliyeti** modülünde inceleyebilir ve yönetebilirsiniz. Transitteki mal siparişlerdeki malları doğrudan **Transitteki mal siparişleri** sayfasından işleyebilirsiniz. Alternatif olarak, transitteki mal siparişleriyle ilişkili seyahate gidebilir ve tüm seyahati, sevkiyat konteynerini veya folyoyu işleyebilirsiniz. Bir yolculuğu faturaladığınızda ve transitteki mal siparişlerindeki malları oluşturduğunuzda, satın alma siparişi satırıyla ilişkili stok ve stok boyutlarının her kombinasyonu için yeni bir transitteki mal siparişi oluşturulur.

Transitteki malları yönetmek için Varış yeri maliyeti iki adımlı bir prosedür kullanır:

1. Bir stok faturası işlendiğinde ve *Transitte* durumu atandığında bir madde alınır.
1. Transitteki mal siparişi, **Transitteki mal siparişleri** sayfasında işlenir ve daha sonra satın alma siparişinde belirtilen ambarda teslim alınır. Bu noktada, durum *Alındı* olarak değiştirilir.

Transitteki mal siparişlerindeki mallarla çalışmak için **Varış yeri maliyeti \> Periyodik görevler \> Transitteki mal siparişleri**'ne gidin.

## <a name="receiving-stock-from-the-goods-in-transit-warehouse"></a>Transitteki mal ambarından stok alma

Sisteminizin kurulumuna bağlı olarak transitteki mal siparişindeki bir maldan birçok şekilde mal alabilirsiniz.

### <a name="in-transit-receiving"></a>Transitteki mal alımı

Aşağıdaki sayfaların tümünde transitteki mal alımı yapabilirsiniz:

- **Transitteki mal siparişleri** sayfasında, satırı seçin ve sonra Eylem Bölmesinde **Al**'ı seçin.
- **Tüm seyahatler** sayfasında bir seyahat seçin veya açın. Eylem Bölmesinde, **Yönet** sekmesinde, **Transitteki mallar** grubundan, **Transitteki malları al**'ı seçin.
- **Tüm sevkiyat konteynerleri** sayfasında bir sevkiyat konteyneri seçin veya açın. Eylem Bölmesinde, **Yönet** sekmesinde, **Transitteki mallar** grubundan, **Transitteki malları al**'ı seçin.
- **Tüm folyolar** sayfasından bir folyo seçin veya açın. Eylem Bölmesinde, **Yönet** sekmesinde, **Transitteki mallar** grubundan, **Transitteki malları al**'ı seçin.

> [!NOTE]
> Transitteki mal alımı genellikle konumların ve toplu/seri izlemenin kullanılmadığı durumlarda kullanılır.

### <a name="arrival-journal"></a>Varış günlüğü

Varış günlüğü oluşturarak da mal alabilirsiniz. Doğrudan seyahat sayfasından bir varış günlüğü oluşturabilirsiniz. Kuruluşunuzun oluşturduğu en iyi uygulamalar, varış günlüğünün mal almak için kullanılıp kullanılmadığını belirler.

1. Seyahati, konteyneri veya folyoyu açın.
1. Eylem Bölmesinde **Yönet** sekmesinde **İşlevler** grubunda **Varış günlüğü oluştur**'u seçin.
1. **Varış günlüğü oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Miktarı başlat**: Transitteki miktardan miktarı ayarlamak için bu seçeneği *Evet* olarak ayarlayın. Bu seçenek *Hayır* olarak ayarlanırsa transitteki mallardan hiçbir varsayılan miktar ayarlanmaz.
    - **Transitteki mallardan oluştur**: Seçili seyahat, konteyner veya folyo için seçili transitteki mal transit satırlarından miktar almak üzere bu seçeneği *Evet* olarak ayarlayın.
    - **Sipariş satırlarından oluştur**: Satın alma siparişi satırlarından varış günlüğündeki varsayılan miktarı ayarlamak için bu seçeneği *Evet* olarak ayarlayın. Varış günlüğündeki varsayılan miktar, yalnızca satın alma siparişi satırındaki miktar transitteki mal siparişteki miktarla eşleşiyorsa bu şekilde ayarlanabilir.

1. Varış günlüğünü, [Madde girişlerini bir madde varış günlüğüyle kaydet](/dynamicsax-2012/appuser-itpro/register-item-receipts-with-an-item-arrival-journal) bölümünde açıklandığı gibi işleyin.

> [!NOTE]
> Varış günlüğü genellikle konumların ve toplu iş/seri izlemenin kullanıldığı durumlarda kullanılır ancak ambar yönetimi kullanılmaz.
>
> Varış günlüğünde bir yerine koyma konumu belirtilecekse sipariş satırlarında varsayılan giriş konumları belirtilmemelidir.

## <a name="warehouse-management"></a>Ambar yönetimi

**Varış yeri maliyeti** modülünü etkinleştirdiğinizde, sipariş işlemenin (özellikle, transitteki malları işleme) **Varış yeri maliyeti** modülü aracılığıyla yapılabilmesi için **Ambar yönetimi** modülündeki birkaç sayfa değiştirilir. Bu bölümde, **Ambar yönetimi** modülüne eklenen alanlar ve işlemler özetlenmektedir.

### <a name="mobile-device-menu-items"></a>Mobil cihaz menü öğeleri

Mobil cihaz menüsü ve **Ambar yönetimi** modülünün transitteki bir mal siparişindeki malları almak üzere ayarlanmış olması koşuluyla, bir mobil cihaz kullanılarak mallar teslim alınabilir. Bu bölümde, transitteki mal teslim almayla ilişkili kurulum açıklanmaktadır.

Transitteki malların işlenmesi için mobil cihazları ayarlamak üzere **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menü öğeleri**'ne gidin.

Varış yeri maliyeti, transitteki malların işlenmesini desteklemek için mobil cihaz menü öğelerine aşağıdaki iş oluşturma işlemlerini ekler:

- Transitteki mallar için madde teslim alma
- Transitteki mallar için madde teslim alma ve yerine koyma

Bu işlemlerin yapılandırma ayarları, [satın alma siparişi alma ve yerine koyma işi oluşturma işlemleri](/dynamicsax-2012/appuser-itpro/configure-mobile-devices-for-warehouse-work) ayarlarına benzerdir. Ancak *Transitteki mal madde teslim alma ve yerine koyma* işlemi, aşağıdaki alanı da ekler.

- **Sevkiyat konteynerini etkinleştirme tamamlandı**: Bu seçenek *Evet* olarak ayarlanırsa yerine koyma işi tamamlandığında, Ambar Yönetimi mobil uygulaması **Sevkiyat konteyneri tamamlandı** olarak adlandırılan ek bir seçenek sağlar. Bu seçenek belirlendiğinde, çalışandan konteynerin tamamlandığını onaylaması istenir. Bu noktada, tüm kısa girişler bir eksik işlem olarak işlenir.

### <a name="location-directives"></a>Konum yönergeleri

Varış yeri maliyeti, **Konum yönergeleri** sayfasına *Transitteki mallar* adlı yeni bir iş emri türü ekler. Bu iş emri türü, [satın alma siparişi iş emri türleriyle](/dynamicsax-2012/appuser-itpro/create-a-work-template)aynı şekilde yapılandırılmalıdır.

### <a name="work-templates"></a>İş şablonları

Bu bölümde, **Son teslim alma maliyeti** modülünün iş şablonlarına eklediği özellikler açıklanmaktadır.

#### <a name="goods-in-transit-work-order-type"></a>Transitteki mallar iş emri türü

Varış yeri maliyeti, **İş şablonları** sayfasına *Transitteki mallar* adlı yeni bir iş emri türü ekler. Bu iş emri türü, [satın alma siparişi iş şablonlarıyla](/dynamicsax-2012/appuser-itpro/create-a-work-template)aynı şekilde yapılandırılmalıdır.

#### <a name="work-header-breaks"></a>İş başlığı molaları

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

*Transitteki mallar* iş emri türüne sahip iş şablonları iş başlıklarını bölecek şekilde yapılandırılabilir. **İş şablonları** sayfasında, aşağıdaki adımlardan birini izleyin:

- Şablonun **Genel** sekmesinde, iş başlığının maksimum değerlerini ayarlayın. Bu maksimum değerler, satınalma siparişi iş şablonlarıyla aynı şekilde çalışırlar. (Daha fazla bilgi için bkz. [satınalma siparişi iş şablonları](/dynamicsax-2012/appuser-itpro/create-a-work-template).)
- Sıralama için kullanılan alanlara göre sistemin ne zaman yeni iş başlıkları oluşturması gerektiğini tanımlamak için **İş başlığı sonları** düğmesini kullanın. Örneğin, her kapsayıcı kimliği için bir iş başlığı oluşturmak amacıyla, Eylem Bölmesi'nde **Sorguyu düzenle**'yi seçin ve ardından **Kapsayıcı Kimliği** alanını sorgu düzenleyicisinin **Sıralama** sekmesine ekleyin. **Sıralama** sekmesine eklenen alanlar *gruplandırma alanları* olarak seçilebilir. Gruplandırma alanlarını ayarlamak için Eylem Bölmesi'nde **İş başlığı sonları**'nı seçin ve ardından gruplandırma alanı olarak kullanmak istediğiniz her alan için **Bu alana göre gruplandır** sütununun onay kutusunu işaretleyin.

Kayıtlı miktar orijinal sipariş miktarını aşarsa son teslim alma maliyeti [fazla bir hareket oluşturur](over-under-transactions.md). İş başlığı tamamlandığında sistem, ana sipariş miktarı için stok hareketlerinin durumunu güncelleştirir. Ancak birincil olan tamamen satın alındıktan sonra öncelikle fazla harekete bağlı olan miktarı güncelleştirir.

Halihazırda kaydedilmiş olan fazla hareket için bir iş başlığını iptal ederseniz fazla hareket, öncelikle iptal edilen miktar kadar azaltılır. Fazla hareket miktarı 0'a (sıfır) indirildikten sonra kayıt kaldırılır ve ek miktarlar birincil sipariş miktarına karşı kayıttan çıkarılır.
