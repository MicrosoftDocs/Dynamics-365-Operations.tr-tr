---
title: Satınalma siparişleri için gelen yüklerin ambarda işlenmesi
description: Bu konu, satınalma siparişleri için gelen yüklerle ilgili ambar işleme sürecini açıklamaktadır.
author: Mirzaab
ms.date: 03/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-03-21
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 464d49f4e096fdd4fe47f73efc253c97200f4de3
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778071"
---
# <a name="warehouse-handling-of-inbound-loads-for-purchase-orders"></a>Satınalma siparişleri için gelen yüklerin ambarda işlenmesi

[!include [banner](../includes/banner.md)]

Bu konu, satınalma siparişleri için gelen yüklerle ilgili ambar işleme sürecini açıklamaktadır.

Her gelen yük için, sisteminizde zaten ilgili bir satış siparişi bulunmalıdır ve ayrıca ilgili yük belirtimini ve/veya taşımacılık planını da içerebilir. Gelen yükleri oluşturma ve yönetme hakkında daha fazla bilgi için bkz. [İş süreci: Gelen yükler için taşımayı planlama](/dynamicsax-2012/appuser-itpro/business-process-planning-transportation-for-inbound-loads).

## <a name="overview-how-inbound-loads-are-created-registered-and-received"></a>Genel bakış: Gelen yüklerin oluşturulması, kaydedilmesi ve teslim alınması

Aşağıdaki şekil, ambarınıza ulaştığında satınalma siparişi miktarları içeren gelen yükleri işlemek için kullanılan tipik akışı gösterir.

![Gelen yükü işleme işlemi.](media/inbound-process.png "Gelen yükü işleme işlemi")

1. **Satıcı satınalma siparişini onaylar.**

    İşlem, sisteme bir satınalma siparişi girildiğinde ve daha sonra siparişi onaylayan satıcıya teslim edildiğinde başlar. Bir gelen yük kaydı oluşturabilmeniz için satınalma siparişinin mevcut olması gerekir. Ancak, sipariş onaylanmamış olsa bile gelen yükü oluşturabilirsiniz. Daha fazla bilgi için bkz. [Satınalma siparişlerini onaylama](../procurement/purchase-order-approval-confirmation.md).

1. **Varışı ve içeriğini planlamak için bir gelen yük kaydı oluşturulur.**

    Gelen yük kaydı bir veya daha fazla satınalma siparişinin satıcı sevkiyatını temsil eder. Yükün, ambara bir fiziksel taşıma birimi olarak (örneğin, bir kamyon yükü) gelmesi beklenir. Gelen yük kaydı planlama amacıyla kullanılır ve lojistik düzenleyicisinin satıcıdan alınan yük ilerlemesini izlemesine olanak tanır. Ayrıca, sipariş satırı miktarlarını kaydetmek ve varış ve yerine koyma işi gibi ambar işlemlerindeki ilerlemeyi yönetmek için de kullanılır. Yükler otomatik olarak veya el ile oluşturulabilir ve bir satınalma siparişi ya da satıcıdan gelen ön sevkiyat bildirimini (ÖSB) temel alabilir. Daha fazla bilgi için bkz. [Gelen yük oluşturma veya değiştirme](/dynamicsax-2012/appuser-itpro/create-or-modify-an-inbound-load).

1. **Satıcı yükün gönderilmesini onaylar.**

    Satıcı yükü gönderdiğinde, teslim alan ambardaki lojistik koordinatörü yük sevkiyatını onaylar. Teslim alan şirket **Taşıma Yönetimi** modülünü kullanıyorsa, gelen sevkiyat onayı gelen yüklerle ilişkili diğer yük yönetimi işlemlerini tetikler. Daha fazla bilgi için bkz. [Yükü sevkiyat için onaylama](/dynamicsax-2012/appuser-itpro/confirm-a-load-for-shipping).

1. **Yük ambara ulaşır ve çalışanlar miktarları kaydeder.**

    Ambar teslim alma limanına bir kamyon yükü ulaştığında, ambar çalışanları yük miktarlarını kaydeder. **Ambar yönetimi** modülü kullanıldığında, çalışanlar kaydı mobil cihazlar kullanarak yapar. Daha fazla bilgi için bkz. [Satınalma siparişlerine karşı ürün girişi - kayıt](../procurement/product-receipt-against-purchase-orders.md#registration) ve [Gelen yüke ulaşan madde miktarlarını kaydetme](#register-item-quantities-arriving).

1. **Kaydedilen yük miktarları satınalma siparişlerine göre deftere nakledilir.**

    Yük miktarları ulaştı olarak kaydedildikten sonra, fiziksel stok artışını kaydetmek için bu miktarların şirket genel muhasebe defterine ürün girişiyle nakledilmesi gerekir. Daha fazla bilgi için bkz. [Satınalma siparişlerine göre ürün girişi - ürün girişi](../procurement/product-receipt-against-purchase-orders.md#product-receipt) ve [Kayıtlı ürün miktarılarını satınalma siparişlerine göre deftere nakletme](#post-registered-quantities).

## <a name="register-item-quantities-that-arrive-on-an-inbound-load"></a><a name="register-item-quantities-arriving"></a>Gelen madde miktarlarını gelen yüke kaydetme

Microsoft Dynamics 365 Supply Chain Management, sipariş edilen ürünlerin gelişini kaydetmek için birçok işlemsel yaklaşımı destekler. Bu nedenle, sistemi belirli iş gereksinimlerinize uyacak şekilde konfigüre edebilirsiniz. Bu bölümde, sistemde Gelişmiş ambar yönetimi açık olduğunda, bir mobil cihaz kullanılarak gelen madde miktarlarının nasıl kaydedileceği açıklanır. Ancak, mobil cihaz yerine, madde varış günlüğünü kullanmayı temel alan alternatif bir akış vardır. Bu akış hakkında daha fazla bilgi için bkz. [Gelişmiş ambar işlemleri etkinleştirilmiş madde için madde varış günlüğü kullanarak maddeleri kaydetme](tasks/register-items-advanced-warehousing.md).

Bir gelen yük ambara ilk kez ulaştığında, ambar çalışanları sevkiyata dahil edilen madde miktarlarını kaydetmelidir. Normal olarak, el tarayıcılarını kullanırlar. Bu iş akışı yalnızca sistemde aşağıdaki öğeler varsa kullanılabilir:

- **Sevkiyatta beklenen madde miktarlarını açıklayan bir gelen yük kaydı**

    Genel olarak, satıcı sevkiyat ambara ulaşmadan önce gelen yük kaydını onaylar. Bu nedenle, yükün  _Sevkedildi_ durumundadır. Ancak, ambar çalışanları durumu _Açık_ veya _Teslim alındı_ olan yüklemeler için de madde miktarlarını kaydedebilir.

- **Yük alımını destekleyecek şekilde yapılandırılmış mobil cihaz menüsü**

    Mobil cihazlar için [Ambar Yönetimi mobil uygulaması](../warehousing/install-configure-warehouse-management-app.md) aşağıdaki iş oluşturma işlemlerini destekler:

    - Yük maddesi teslim alma
    - Yük maddesi teslim alma ve yerine koyma
    - Mobil cihaz mesü öğesi için **Kaynak belge satırı tanımlama yöntemi** alanının  _Yük maddesi teslim alma_ olarak ayarlandığı karma plaka teslim alma. Daha fazla bilgi için bkz. [Karma plaka teslim alma](mixed-license-plate-receiving.md).
    - Mobil cihaz mesü öğesi için **Kaynak belge satırı tanımlama yöntemi** alanının  _Yük maddesi teslim alma_ olarak ayarlandığı karma plaka teslim alma ve yerine koyma. Daha fazla bilgi için bkz. [Karma plaka teslim alma](mixed-license-plate-receiving.md).

    > [!NOTE]
    > İşlemden bağımsız olarak, sistem teslim alma konumunda kayıtlı miktarları alacak ve bunları normal depolama konumuna yerleştirecek işi oluşturur. _Yük maddesi teslim alma ve yerine koyma_ veya _Karışık plaka teslim alma ve yerine koyma_ işlemi kullanıldığında, cihaz tarafından yükleme miktarını kaydeden çalışandan, kayıt görevinin bir parçası olarak yerine koyma işini de gerçekleştirmesi istenir. Bunun aksine _Yük maddesi teslim alma_ ve _Karışık plaka teslim alma_ işlemleri için varsayım, yerine koyma işinin kayıt görevinden ayrı olarak yapılmasıdır.

- **Gelen yükler için çekme ve yerine koyma işini tanımlayan bir iş şablonu**

    Bu madde önceki maddelerle ilgilidir. _Satınalma siparişi_ iş emri türü için en az bir iş şablonunuz olmalıdır ve bu şablon bir çekme/yerine koyma iş türü kümesi içermelidir.

Mobil cihaz, yük miktarı kaydı için akış aracılığıyla ambar teslim alma memuruna yol gösterir. En azından bu akış, her yük kodu için aşağıdaki adımları içerir:

1. Yük kodunu girin.
2. Teslim alınan madde için madde numarasını girin.
3. Teslim alınan bu madde numarasının miktarını girin.
4. Sistem bu numarayı otomatik olarak oluşturmak üzere ayarlanmamışsa, maddenin ilk yerleşimi için plaka numarasını girin.
5. **Tamam**'a dokunun.

Çalışan bu adımları tamamladıktan sonra sistem, satınalma siparişi satır miktarının bir yükte geldiği ve tüm yük miktarlarının kayıtlı olması koşuluyla, uygun varlıklarda aşağıdaki güncelleştirmeleri yapar:

| Varlık | Güncelleştirmeler | Not |
|---|---|---|
| Yükle | Yük satırındaki **İş oluşturulan miktar** alanı kayıtlı miktarı gösterecek şekilde güncelleştirilir. | Yük için herhangi bir sevkiyat onayı çalıştırılmamışsa, **Yük durumu** değeri _Sevk edildi_ veya _Açık_ olarak kalır. En az bir yerine koyma çalışması satırı başlatılmışsa, durum _İşleniyor_ olarak değiştirilir. |
| İlişkili yük miktarları kaydedilen bir satınalma siparişinin stok hareketi |<p>Aşağıdaki alanlar güncelleştirilir:</p><ul><li><b>Giriş</b> alanı <i>Kaydedildi</i> olarak ayarlanır.</li><li><b>Yerleşim</b> alanı, teslim alma noktasının yerleşim koduyla güncelleştirilir. (Bu kod, her ambar için <b>Varsayılan giriş yerleşimi</b> alanında belirtilmiştir.)</li><li><b>Plaka</b> alanı, kayıt sırasında girilen veya oluşturulan plaka numarasıyla güncelleştirilir.</li><li><b>Yük kodu</b> alanı, miktarın kaydedildiği yükün numarasıyla güncelleştirilir. (Nota bakın.)</li></ul> | Satınalma siparişi stok hareketi ile yüke göre kaydedilen miktarlar arasında bağlantı kurma olanağı 10.0.9 sürümünde isteğe bağlı bir özellik olarak sunulmuş ve _Satınalma siparişi stok hareketlerini yükle ilişkilendir_ olarak adlandırılmıştır. Bu özellik özellikle satın alınan mallara ilişkin tek bir siparişin birden fazla yük olarak teslim edildiği veya bir yükün birden çok satınalma siparişi için miktar içerdiği iş akışları için yararlıdır. |
| Ambarda yerine koyma | Çalışanın, kayıtlı miktarları teslim alma yerleşiminden normal bir depolama konumuna taşımasını yönlendirmek için çalışma şablonu temel alınarak iş oluşturulur. | Depolama konumu seçimi Yerine koyma yerleşimi yönergesi tarafından kontrol edilir. Herhangi bir konum yönergesi tanımlanmamışsa, iş üzerindeki yerine koyma konumu boştur. |

Ambar çalışanlarının _Yük maddesi teslim alma_ işlemini kullanmadan bir veya daha fazla ilişkilendirilmiş yük içeren bir satınalma siparişi girişini kaydedebileceğini göz önünde bulundurun. Aşağıdaki yöntemler kullanılabilir:

- **Mobil cihazda:** _Satınalma siparişi satırı teslim alma_  ve  _Satınalma sipariş satırı teslim alma ve yerine koyma_ işlemlerini kullanın. (Satınalma siparişi satır miktarı için birden fazla yük varsa, çalışan _Satınalma siparişi satırı teslim alma_ işlemini kullanamaz. Bunun yerine çalışandan,  _Yük maddesi teslim alma_ işlemiyle ilişkilendirilmiş olan cihaz eylemini kullanması istenir.)
- **İstemci üzerinde:** Madde varış günlüğünü kullanın.
- **İstemci üzerinde:** Satınalma siparişi satırından erişilebilen **Kayıt** eylemini kullanın.

> [!NOTE]
> Satınalma siparişi girişi önceki yöntemlerden herhangi biri kullanılarak kaydedilirse, satınalma sipariş stok hareketi ve yük arasında, _Satınalma siparişi stok hareketlerini yükle ilişkilendir_ özelliği açık olsa bile hiçbir bağlantı oluşturulmaz. Bu kuraldaki tek istisna, **Satınalma siparişi satırı teslim alma** seçeneğini kullanmanız ve sipariş satırı için yalnızca bir yükün _Teslim alındı_ durumu dışında bir durumu olmasıdır.

### <a name="handle-discrepancies-during-registration-of-inbound-load-quantities"></a>Gelen yük miktarlarının kaydı sırasında tutarsızlıkları işleme

Ambar çalışanları kısmi yük miktarı girişi kaydı yapabilir. Her kısmi yük miktarı girişi, kayıtlı miktar için _Kayıtlı_ giriş durumu olan ayrı bir stok hareketi oluşturur ve lot kodu kaynak satınalma sipariş satırına başvurur.

#### <a name="load-under-receiving"></a>Eksik yük teslim alma

Bir yük geldiğinde, madde miktarları yükleme kaydında belirtilen miktardan daha azsa, ambar teslim alma çalışanları, gelen ve kaydedilen gerçek miktarla eşleşmesi için yükleme satırındaki miktarı azaltarak bu tutarsızlığı onaylamak üzere doğrudan istemcide çalışabilir.

#### <a name="load-over-receiving"></a><a name="load-over-receiving"></a>Fazla yük teslim alma

Fazla teslim alma, bir yük geldiğinde ve madde miktarları beklenen yük satırı miktarını aştığında gerçekleşir. Yük kaydı sırasında, fazla teslim almaya izin verilip verilmeyeceğini ve ne seviyede izin verileceğini kontrol edebilirsiniz.

Bir ambar çalışanı fazla teslimat kaydı yapmayı denediğinde ne olacağını kontrol etmek için ilgili mobil cihaz menü öğelerinin **Yük fazla teslim alındı** alanını kullanın. Bu alan, aşağıdaki iş oluşturma işlemi türlerini kullanan mobil cihaz menü öğeleri için kullanılabilir:

- Yük maddesi teslim alma
- Yük maddesi teslim alma ve yerine koyma
- Karışık plaka teslim alma (**Kaynak belge satırı tanımlama yöntemi** alanı _Yük maddesi teslim alma_ olarak ayarlandığında)
- Karışık plaka teslim alma ve yerine koyma (**Kaynak belge satırı tanımlama yöntemi** alanı _Yük maddesi teslim alma_ olarak ayarlandığında)

Aşağıdaki tablo, **Yük fazla teslim alındı** alanı için kullanabileceğiniz seçenekleri açıklar.

| Değer | Tanım |
|---|---|
| İzin ver | Çalışanlar seçili bir yük için kalan kayıtlı olmayan miktarı aşan miktarların kaydını yapabilir, ancak yalnızca toplam kayıtlı miktar yükleme ile ilişkili satınalma siparişi satırı miktarını (fazla teslimat yüzdesi için düzeltmeden sonra) geçemez. |
| Engelle | <p>Çalışanlar seçili bir yük için kalan kayıtlı olmayan miktardan daha fazla miktar girişi kaydedemez (fazla teslimat yüzdesi ayarlandıktan sonra). Girişleri kaydetmek isteyen bir çalışan bir hata alır ve kalan kayıtlı olmayan yük miktarına eşit veya bundan daha az bir miktar kaydetinceye kadar devam edemez.</p><p>Varsayılan olarak, bir yükleme satırındaki fazla teslimat yüzdesinin değeri, ilişkili satınalma sipariş satırından kopyalanır. <b>Fazla teslim alınan yük</b> alanı <i>Engelle</i> olarak ayarlandığında sistem, bir yükleme satırı için kaydedilebilecek toplam miktarı hesaplamak için fazla teslimat yüzdesi değerini kullanır. Ancak, gerektiğinde her bir yük için bu değerin üzerine yazılabilir. Bu davranış, sipariş satırı fazla teslimat yüzdesini temsil eden fazla miktarın bir kısmının veya tümünün birden çok yük arasında orantılı olarak dağıtılmasını sağlayan teslim alma akışlarında geçerli duruma gelir. Aşağıda bir örnek senaryo verilmiştir:</p><ul><li>Tek bir satınalma siparişi satırı için birden çok yük vardır.</li><li>Satınalma siparişi satırı 0'dan (sıfır) büyük bir fazladan teslimat yüzdesine sahiptir.</li><li>Miktarlar, fazla teslimat yüzdesi dikkate alınmadan bir veya daha fazla yüke göre zaten kaydedilmiştir.</li><li>Fazla teslimat miktarı son yükte gelir.</li></ul><p>Bu senaryoda, yalnızca ambar Yöneticisi ilgili yükleme satırına ait fazla teslimat yüzdesini varsayılan değerden yeterince geniş bir değere artırırsa bir mobil cihaz son yük için fazla miktarı kaydetmek üzere kullanılabilir ve böylece tüm fazladan teslimar son yükle birlikte kaydedilebilir.</p> |
| Yalnızca kapalı yükler için engelle | Çalışanlar açık yükler için fazla yük satırı miktarları alabilir, ancak _Alındı_ durumunda olan yüklemeler için bunu yapamaz. |

> [!NOTE]
> **Yük fazla teslim alındı** alanının varsayılan değeri _İzin ver_'dir. Bu değer kullanıldığında, davranış 10.0.11 sürümünde sunulan _Yük miktarlarının fazladan teslim alınması_ özelliğinden önceki standart davranışla eşleşir.

### <a name="put-away-the-registered-quantities"></a>Kayıtlı miktarları yerine koyma

Mobil cihazda kayıt tamamlandığında, _Miktar giriş kaydı_ eylemi, miktarların şimdi teslim alma yerleşimi konumunda olduğunu ve rezervasyon için kullanılabileceğini belirtmek üzere stok ve ambar kayıtlarını güncelleştirir. Ancak, şirketin ambar operasyonları tipik olarak miktarların teslim alma noktasından normal ambar depolama alanına taşınmasını gerektirir, böylece sonraki malzeme çekme işlemleri yapılabilir. Yerine koyma yönergeleri, gelen yük teslim alındı olarak kaydedildiğinde otomatik olarak oluşturulan yerine koyma işinde yakalanır.

Ambar çalışanı yerine koyma işini tamamladığında, aşağıdaki tabloda özetlendiği şekilde, sistem bazı varlıkların güncelleştirmelerini güncelleştirerek sonucu kaydeder ve izler.

| Varlık | Güncelleştirmeler | Not |
|---|---|---|
| Yükle | <p>Aşağıdaki alanlar güncelleştirilir:</p><ul><li><b>Yük durumu</b> değeri <i>İşlemde</i> olarak değiştirilir.</li><li><b>İş durumu</b> değeri <i>İş %100,00 tamamlandı</i> olarak değiştirilir.</li></ul> | Çalışan en az bir yerine koyma işi satırı için yerine koyma görevini başlattığında, **Yük durumu** değeri _İşlemde_ olarak değiştirilir. |
| İlişkili miktarların yerine koyulduğu işin stok hareketleri | **Giriş** ve **Yerleşim** alanları ve diğer ilgili alanlar, teslim alma yerleşiminden depolama konumuna kadar hareketi yansıtacak şekilde güncelleştirilir. | Satınalma siparişi stok hareketinin **Giriş durumu** değeri _Kayıtlı_ olarak kalır. |
| Ambarda yerine koyma | **İş durumu** değeri  _Kapalı_ olarak değiştirilir. | |

## <a name="post-registered-product-quantities-against-purchase-orders"></a><a name="post-registered-quantities"></a>Kayıtlı ürün miktarlarını satınalma siparişlerine göre deftere nakletme

Gelen ürün miktarları sistemde kaydedildikten sonra, satışlarla ve diğer giden ve dahili işlemlerle bağlantılı olarak rezervasyon için kullanılabilir olurlar. Ancak, sistem henüz stok (geçiş) hesaplarını güncelleştirmez. Bu güncelleştirme yalnızca, operasyon ekibi kayıtlı ürün girişlerini deftere naklettiğinde gerçekleşebilir.

Ürün girişini deftere nakledebilecekleri bir sayfa açmak için, operasyon takımının üyeleri aşağıdaki adımlardan herhangi _birini_ izleyebilir:

- İlgili yük kaydını açın ve **Ürün girişi** eylemini seçin.
- **Ambar yönetimi \> Periyodik görevler \> Ürün girişlerini güncelleştir**'e gidin ve ardından **Yük kodu** alanında deftere nakledilecek yüklemeyi belirtin.
- İlgili satınalma siparişini açın ve **Ürün girişi** eylemini seçin.
- **Tedarik ve kaynak atama \> Satınalma siparişleri \> Ürünleri teslim alma \> Ürün girişi işini deftere nakletme**'ye gidin.

**Yük** sayfasında bulunan (ve güncelleştirme işi için eşdeğer sayfa olan **Ürün girişlerini güncelleştir** sayfasında) bulunan **Ürün girişi** eylemi, ürün giriş miktarlarını yalnızca _Kayıtlı_ durumundaki satınalma siparişi miktarlarında güncelleştirebilir. Ancak,**Satınalma siparişi** sayfasında bulunan **ürün girişi** eylemi her iki işleme durumundaki (_Sipariş edildi_ ve _Kaydedildi_) miktarları içerebilir. Ayrıca _Şimdi teslim alma miktarı_ ve _Kayıtlı miktar ve hizmetler_ gibi ek parametreler aracılığıyla ürün girişi deftere nakil kapsamını da denetleyebilir.

Yalnızca _Onaylandı_ durumda olan siparişler ürün girişiyle deftere nakledilebilir. Onaylanmamış satınalma siparişlerinde, **Ürün girişi** eylemi kullanılamaz olarak görünür.

### <a name="post-registered-quantities-from-the-load-page"></a>Yük sayfasından kayıtlı miktarları deftere nakletme

**Yük** sayfasından ürün girişiyle deftere nakledilen kayıtlı miktarlar için aşağıdaki önkoşulların karşılanması gerekir:

- Yük, _Kaydedildi_ durumunda olan en az bir miktar birimine sahip olmalıdır.
- Yük durumu _Sevk edildi_ olmalıdır.
- Yük ile ilişkilendirilen satınalma siparişinin durumu _Onaylandı_ olmalıdır.

> [!NOTE]
> Yük durumu _Sevk edildi_ olarak ayarlanmamışsa sistem, ürün girişi güncelleştirmesini çalıştırmadan önce, yükü otomatik olarak onaylar. (Bir kullanıcı, yükün gelen sevkiyatını kaydettiğinde yük durumu _Sevk edildi_ olarak ayarlanır.)

Seçili bir yük ile ilişkili varış kayıtlarını ürün girişiyle deftere nakletmek için çalışan **Yük** sayfasındaki **Ürün girişi** eylemini seçer. Açılan sayfada aşağıdaki temel ayrıntılar vardır:

- **Ayarlar** sekmesinin **Parametreler** bölümündeki **Miktar** _kayıtlı miktarı_ gösterir. Burada başka seçenek yoktur.
- **Genel bakış** hızlı sekmesindeki kılavuz, seçili yükün içerdiği tüm satınalma siparişlerini listeler.
- **Satırlar** hızlı sekmesindeki kılavuz, kayıtlı miktarı olan tüm sipariş satırlarını listeler.

> [!NOTE]
> **Satır** sekmesinde görüntülenen sipariş satırı miktarları _Yük başına birden fazla ürün girişine izin ver_ özelliğinin Supply Chain Management sürümünüzde kullanılabilir ve etkinleştirilmiş olup olmamasına bağlı olarak farklı şekilde hesaplanır.
>
> | Sürüm | Hesaplama |
> |---|---|
> | 10.0.10 sürümünden önceki sürümler ve  _Yük başına birden fazla ürün girişine izin ver_ seçeneğinin açık olmadığı daha yeni sürümler | Satır miktarı, kaydın birden çok yükleme üzerinden mi, yükten bağımsız olarak mı, bir mobil cihaz veya istemciden mi gerçekleştirildiğinden bağımsız olarak _söz konusu satınalma sipariş satırı için_ kaydedilen tüm miktarların toplamıdır. |
> | _Yük başına birden fazla ürün girişine izin ver_ seçeneğinin açık olduğu 10.0.10 sürümü ve sonrası | Satır miktarı, **Ürün girişi deftere nakil** eyleminin başlatıldığı _yük kaydı_ için tüm kayıtlı miktarların toplamıdır. |

Kullanıcı, ürün girişini deftere nakil işlemini onaylamak için **Tamam**'ı seçtiğinde, sistem uygun varlıklarda aşağıdaki anahtar güncelleştirmeleri yapar.

| Varlık | Güncelleştirmeler |
|---|---|
| Deftere nakil kapsamına dahil edilen satır miktarlarının bulunduğu satınalma siparişinin stok hareketi | <p>Aşağıdaki alanlar güncelleştirilir (ancak, birden fazla başka güncelleştirme de vardır):</p><ul><li><b>Giriş</b> alanı <i>Teslim alındı</i> olarak ayarlanır.</li><li><b>Fiziksel tarih</b> alanı deftere nakil tarihiyle güncelleştirilir.</li></ul> |
| Kullanıcının, ürün girişini deftere naklettiği yük | Yüklerde yapılan güncelleştirmeler kullanılan sürüme ve **Yükleme başına birden çok ürün girişine izin ver** alanının ayarına bağlıdır. Kurallar, bu bölümün ilerisinde yer alan tabloda açıklanmaktadır. |

**Yük başına birden fazla ürün girişine izin ver** alanı şirketlerin gelen yük teslim alma ilkesi seçmesine olanak tanır. Operasyonel akışlarına bağlı olarak, şirketler aynı yük için birden çok ürün giriş deftere nakil işlemine izni vermeyi veya vermemeyi seçebilirler. Lojistik yöneticisinin **Yük başına birden fazla ürün girişine izin ver** alanını aşağıdaki değerlerden birine ayarlamasını öneririz:

- **Hayır** – Ambar teslim alma görevlileri her zaman belirlenen bir zaman dilimi içinde her bir yük ile gelen sipariş miktarlarını kaydediyorlarsa bu değeri seçin. Herhangi bir yük miktarı kayıtlı değilse, sistem miktarın gelmemiş olduğunu veya yükte bulunmadığını ve bu nedenle yükün bir parçası olarak kabul edilmemesi gerektiğini varsayar. Bir yükten çalıştırılan ürün girişi deftere nakli işlemi aynı varsayımı kullanır. Ürün girişyile tüm kayıtlı miktarları güncelleştirmenin (kendi ana işlevini) yanı sıra yükün tamamlandığını ve ek işleme için kapatıldığını da bildirir. Bu durumda, tüm yük satırı miktarları otomatik olarak kayıtlı miktarlarla güncelleştirilir, kayıtlı miktarı olmayan yükleme satırları silinir ve yük durumu _Teslim alındı_ olarak değişir.
- **Evet** – Ambar teslim alma görevlileri için gelen yükte bulunan tüm miktarları kaydetmek için daha fazla zaman gerekiyorsa, ancak bu sırada daha önceden kaydedilen miktarları ürün girişiyle deftere nakletmeniz gerekiyorsa bu değeri seçin. Bu durumda, lojistik yöneticisi, ürün girişi deftere nakil işi çalıştırıldıktan sonra bile bir yükü açık tutmak isteyecek ve böylece kalan yük miktarları genel muhasebe defterine sürekli olarak ürün girişiyle kaydedilecek ve güncelleştirilecektir.
- **Sor** – Yük teslim alma yöntemleriniz karışıksa ve ürün girişi deftere nakil işlemi her çalıştırıldığında karar vermeniz gerekiyorsa bu değeri seçin.

Aşağıdaki tabloda, **Yük başına birden fazla ürün girişine izin ver** ayarının etkileri özetlenmektedir.

| Yük başına birden fazla ürün girişine izin ver | Yük miktarı | Yük durumu | Not |
|---|---|---|---|
| Bu alan kullanılamıyorsa (10.0.10 öncesi sürümler) | <p>Yük miktarı, kayıtlı miktara eşit olacak şekilde ayarlanır.</p><p>Yük miktarının 0 (sıfır) olarak güncelleştirilmesi, kayıt yapılmadığı anlamına gelir, yük satırı silinir.</p><p>Yükte herhangi bir yük satırı yoksa, yük silinir.</p> | _Alınan_ | Sipariş satırının kayıtlı miktarı için birden çok yük varsa, yalnızca girişin deftere nakledildiği yükün durumu _Teslim alındı_ olarak güncelleştirilir. |
| Hayır | <p>Yük miktarı, yük koduyla ilişkilendirilmiş kayıtlı miktara eşit olacak şekilde ayarlanır.</p><p>Stok hareketi için bir yük kodu kaydedilmezse, davranış 10.0.10 önceki sürümlerdeki davranışla eşleşir.</p> | _Alınan_ | |
| Evet | Güncelleştirme yok | _Teslim alındı_, toplam kayıtlı yük miktarı yük miktarına eşit veya daha fazlaysa | |
| Evet | Güncelleştirme yok | _Sevk edildi_ veya _İşlemde_, toplam kayıtlı yük miktarı yük miktarından azsa | |

**Yük durumu** alanı _Teslim alındı_ olarak ayarlandıktan sonra, bu yük için daha fazla ürün girişi deftere nakli yapılamaz. Ancak, çalışan kalan sipariş miktarını aşağıdaki koşullarda alınan yüklemeye karşı kaydedebilir. (Daha fazla bilgi için bu konunun önceki bölümündeki [Fazla yük teslim alma](#load-over-receiving) konusuna bakın.)

- Supply Chain Management sürümü 10.0.11 sürümünden daha eski.
- _Yük miktarlarını fazladan teslim alma_ özelliği açıktır ve yük maddesi teslim alma eylemine ait mobil cihaz menü öğesindeki **Fazla teslim alınan yük satırı miktarı** alanı _İzin ver_ olarak ayarlanır.

Ek kayıtlı yük miktarlarını durumu _Teslim alındı_ olan bir yüke karşı ürün girişiyle deftere nakletmek için kullanıcının ilişkili satınalma siparişinden deftere nakil eylemini çalıştırması gerekir.

### <a name="post-registered-quantities-from-the-purchase-order-page"></a>Satınalma siparişi sayfasından kayıtlı miktarları deftere nakletme

Kayıtlı miktarları **Satınalma siparişi** sayfasından ürün girişiyle deftere nakletmek için kullanıcı **Ürün girişi** eylemini seçmeden önce aşağıdaki görevleri tamamlar:

- **Ayarlar** sekmesinin **Parametreler** bölümündeki **Miktar** sekmesini  _Kayıtlı miktarı_ olarak ayarlayın.
- **Ürün girişi** alanında, deftere nakil işlemine dahil edilen satınalma siparişlerinin numaralarını girin.

> [!NOTE]
> Deftere nakil kapsamına eklenecek satır miktarı, kaydın birden çok yükleme üzerinden mi, yükten bağımsız olarak mı, bir mobil cihaz veya istemciden mi gerçekleştirildiğinden bağımsız olarak söz konusu sipariş satırı için kaydedilen tüm miktarların toplamıdır. Aynı kural, **Yük başına birden fazla ürün girişine izin ver** alanı kullanılabilir veya etkin olmadığında gerçekleştirilmiş olması durumunda, ürün girişi deftere nakil işlemi yükten çalıştırıldığında da geçerlidir.

Kullanıcı, ürün girişini deftere nakil işlemini onaylamak için **Tamam**'ı seçtiğinde, sistem uygun varlıklarda aşağıdaki anahtar güncelleştirmeleri yapar.

| Varlık | Güncelleştirmeler |
|---|---|
| Deftere nakil kapsamına dahil edilen satır miktarlarının bulunduğu satınalma siparişinin stok hareketi | <p>Aşağıdaki alanlar güncelleştirilir (ancak, birden fazla başka güncelleştirme de vardır):</p><ul><li><b>Giriş</b> alanı <i>Teslim alındı</i> olarak ayarlanır.</li><li><b>Fiziksel tarih</b> alanı ürün girişi deftere nakil eyleminin tarihiyle güncelleştirilir.</li></ul> |
| Yükle | Yük güncelleştirmeleri, **Yük başına birden fazla ürün girişine izin ver** alanının kullanılabilir ve etkin olmasına bağlıdır. Kurallar sonraki tabloda açıklanmaktadır. |

Aşağıdaki tabloda, **Yük başına birden fazla ürün girişine izin ver** ayarının etkileri özetlenmektedir.

| Yük başına birden fazla ürün girişine izin ver | Yük miktarı | Yük durumu | Not |
|---|---|---|---|
| Bu alan devre dışı bırakıldığında veya kullanılamıyorsa (10.0.10 önceki sürümlerde) | Güncelleştirme yok | Hiçbir güncelleştirme yapılmaz. (Durum _Açık_, _Sevk edildi_ veya  _İşlemde_ olarak kalır.) | Ürün girişi deftere nakil işlemi bir satınalma siparişinden başlatıldığından, güncelleştirme mantığı, kapsamı içindeki kayıtlı miktarlar ile kaydın kaydedildiği yük arasındaki ilişki hakkında bilgi sahibi değildir. Bu nedenle, durum güncelleştirmesi için yükü seçemez. |
| Etkinleştirildi | Güncelleştirme yok | <p>Aşağıdaki eylemlerden biri gerçekleşir:</p><ul><li>Satınalma siparişi stok hareketlerinin toplam teslim alınan ve satın alınan miktarları ilişkili oldukları yükün miktarıyla eşit veya bu miktardan fazlaysa durum <i>Teslim alındı</i> olarak değişir.</li><li>Yüklerdeki tüm satırlar için önceki koşul karşılanmazsa durum <i>Açık</i>, <i>Sevk edildi</i> veya <i>İşlemde</i>  olarak kalır.</li></ul> | |

### <a name="select-the-appropriate-product-receipt-posting-option-for-your-logistics-operations"></a>Lojistik işlemleriniz için uygun ürün girişi deftere nakil seçeneğini seçin

Daha önce anlatıldığı gibi, sistem iki ürün girişi deftere nakil seçeneği sunar. Bu seçeneklere aşağıdaki konumlardan erişilebilir:

- **Yük** sayfasında veya **Ambar yönetimi \> Periyodik görevler** menüsünden güncelleştirme işi olarak
- **Satınalma siparişi** sayfasında veya **Tedarik ve kaynak atama \> Satınalma siparişleri \> Ürünleri teslim alma** menüsünden güncelleştirme işi olarak

Gelen siparişlerinin taşıma ve ambar işlemlerini planlamak ve yönetmek için yükleri kullanan şirketlerin, yüklerle çalışmak üzere tasarlanmış olan aşağıdaki işlevleri kullanması önerilir:

- Ürün miktarı gelişini yüke karşı kaydetmek için ambar mobil cihazlarındaki **Yük maddesi teslim alma** eylemleri
- Stok genel muhasebesini güncelleştirmek için bir yükten başlatılan **Ürün girişi deftere nakil** eylemleri

> [!NOTE]
> Diğer miktar kaydı ve ürün girişi deftere nakil işlevleri ilgili gelen operasyonel işlemleri desteklemek için kullanılabilir. Ancak, bunları adanmış yük odaklı işlevler yerine veya bunlarla birlikte kullanırsanız, yük kayıtlarının veri doğruluğunu tehlikeye atabilir ve bu nedenle yük yönetimi akışlarının sorunsuzluğunu bozabilirsiniz.

## <a name="example-scenarios"></a>Örnek senaryolar

### <a name="prepare-your-system-to-run-the-sample-scenarios"></a>Sisteminizi örnek senaryoları çalıştırmak üzere hazırlayın

Bu bölümde açıklanan örnek senaryolar aracılığıyla çalışabilmek için, öncelikle gerekli tüm özelliklerin sisteminizde açık olduğundan emin olmanız gerekir. Gerekli demo verileri de sistemde bulunmalıdır.

#### <a name="turn-on-the-required-features"></a>Gerekli özellikleri açma

Bu senaryolar, _Yük başına birden fazla ürün girişine izin ver_ özelliğini ve bunun önkoşul özelliğini gerektirir. Yöneticiler bu özellikleri, bu adımları izleyerek açabilir.

1. **Özellik yönetimi** çalışma alanını açın. (Bu çalışma alanının nasıl bulunacağı ve kullanılacağı hakkında tüm ayrıntılar için bkz. [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)

1. _Satınalma siparişi stok hareketlerini yükle ilişkilendir_ özelliğinin açık olduğundan emin olun. Supply Chain Management sürüm 10.0.21 itibariyle bu özellik zorunludur; bu nedenle varsayılan olarak açıktır ve yeniden kapatılamaz. Ancak, özellik hâlâ [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'nde aşağıdaki şekilde listelenir:

    - **Modül:** _Ambar yönetimi_
    - **Özellik adı:** _Satınalma siparişi stok hareketlerini yükle ilişkilendir_

1. Listelenen _Yük başına birden fazla ürün girişine izin ver_ özelliğini aşağıdaki şekilde açın:

    - **Modül:** _Ambar yönetimi_
    - **Özellik adı:**_Yük başına birden fazla ürün girişine izin ver_

#### <a name="enable-sample-data"></a>Örnek verileri etkinleştirme

Belirtilen örnek kayıtları ve değerleri kullanarak bu senaryolar arasında çalışmak için, standart demo verisinin yüklenmiş olduğu bir sistem kullanmanız gerekir. Ayrıca başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

#### <a name="add-a-menu-item-for-receiving-load-items-when-a-mobile-device-is-used"></a>Mobil cihaz kullanıldığında yük maddelerini teslim almak için bir menü öğesi ekleme

Ambar teslim alma görevlilerinin bir yük ile bağlantılı gelen stoğu kaydetmek için bir mobil cihaz kullanabilmesi için, o amaca yönelik bir mobil cihaz menü öğesi oluşturmanız gerekir.

Bu bölümde, bir mobil cihaz menü öğesi oluşturacak ve bunu varolan bir menüye ekleyeceksiniz. Ambar çalışanı böylece Ambar Yönetimi mobil uygulaması içindeki menü öğesini seçebilir.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menü öğeleri**'ne gidin ve mobil cihaz menünüzde aşağıdaki ayarlara sahip bir menü öğesi bulunduğundan emin olun:

    - **Mod:**_İş_
    - **İş oluşturma işlemi:**_Yük maddesi teslim alma_
    - **Plaka oluştur:** _Evet_

    Diğer tüm ayarları varsayılan değerleriyle bırakabilirsiniz.

    ![Mobil cihaz menü öğesi ayarları.](media/inbound-mobile-menu-items.png "Mobil cihaz menü öğesi ayarları")

    Mobil cihaz menü öğeleri ayarlama hakkında daha fazla bilgi için bkz. [Ambar işi için mobil cihazları ayarlama](configure-mobile-devices-warehouse.md).

2. Menü öğesini ayarlamayı bitirdikten sonra **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menü öğeleri**'ne gidin ve mobil cihazınızın menü yapısına ekleyin.

### <a name="example-scenario-1-register-a-load-where-some-items-are-missing"></a>Örnek senaryo 1: Bazı maddelerin eksik olduğu bir yükü kaydedin

Bu senaryo, tüm beklenen miktarların mevcut olmadığı bir giriş yükü için miktarların nasıl kaydedileceğini gösterir. Daha sonra satınalma siparişi için ürün girişinin nasıl deftere nakledileceği gösterilir.

#### <a name="create-a-load-to-plan-receipt-of-a-purchase-order"></a>Bir satınalma siparişinin girişini planlamak için yük oluşturma

Bu yordamda, el ile bir satınalma siparişi ve ilişkili bir yük oluşturacaksınız. Sonra, satıcıdan sevk edildiği (yük durumunu güncelleştirir) benzetimi yapmak için yükü güncelleştireceksiniz. Böylece, ambar planlayıcıları, beklenen gelen yükleri bulmak için yükleri **Yük durumu** ile filtreleyebilir.

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Satınalma siparişi oluştur** iletişim kutusunda, **Satıcı hesabı** alanını  _1001_ olarak ayarlayın.
1. İletişim kutusunu kapatmak için **Tamam**'ı seçin ve satınalma siparişini oluşturun.
1. Yeni satınalma siparişi zaten **Satınalma siparişi satırları** altında bir satır içerir. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** _A0001_
    - **Ambar:** _24_
    - **Miktar:** _10_

1. Eylem Bölmesinde, **Satınalma** sekmesinde, **Eylemler \> Onayla**'yı seçin. Sipariş durumu artık _Onaylandı_ olur.
1. Eylem Bölmesinde, **Ambar** sekmesinde, **Eylemler \> Yük planlama workbench**'ini seçin.
1. **Yük planlama workbench'i** sayfasında, Eylem Bölmesinde **Tedarik ve talep** sekmesinde, **Ekle \> Yeni yüke**'yi seçin.
1. **Yük şablonu ataması** iletişim kutusunda **Yük şablonu kodunu** _20' Konteyner_ olarak ayarlayın.
1. İletişim kutusunu kapatıp workbench'e dönmek için **Tamam**'ı seçin.
1. **Yükler** bölümünde, yeni oluşturulan yükü açmak için **Yük kodu**'nu seçin.
1. Yük başlığını ve satır ayrıntılarını gözden geçirin ve aşağıdaki noktalara dikkat edin:

    - **Yük** hızlı sekmesinde, **Yük durumu** alanı _Açık_ olarak ayarlanır.
    - **Yük satırları** bölümünde, **Miktar** alanının _10_ olarak ayarlandığı ve **İş oluşturulan miktar** alanının  _0_ (sıfır) olarak ayarlandığı tek bir satır vardır.

    ![Yük ayrıntıları.](media/inbound-load-details.png "Yük ayrıntıları")

1. Eylem Bölmesinde **Sevk ve teslim alma** sekmesinde **Onayla\> Gelen sevkiyat**'ı seçin. **Yük durumunun** _Sevk edildi_ olarak değiştiğini unutmayın.
1. Bir sonraki yordamda kullanabilmeniz için **Yük kodu** değerini not edin.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-load"></a>Yük üzerinde gelen miktarların girişini kaydetme

Yük ambar teslim alma limanına ulaştığında, bir teslim alma memuru yük miktarlarını bir mobil cihaza kaydeder.

1. Ambar 24'te oturum açmak için mobil cihazınızı kullanın. (Standart demo verilerinde, kullanıcı kimliği _24_ ve parola olarak _1_'i kullanarak oturum açın.)
1. Bu senaryo için oluşturduğunuz _Yük maddesi teslim alma_ menü öğesini seçin.
1. Aşağıdaki değerleri girmek için ekrandaki veri girişi yönergelerini izleyin. (Sipariş, kullanmakta olduğunuz mobil cihaza veya emülatöre göre değişebilir.)

    - **Yük** – Önceki yordamda oluşturduğunuz yük kodunu girin.
    - **Madde** – Bu yük için beklenen madde olan _A0001_ girin.
    - **Miktar** – Yükte bulunan fiili miktar olarak _9_ girin. Bu miktarın beklenen miktardan az olduğunu unutmayın.

1. Cihazınız işin tamamlandığını bildirene kadar, diğer tüm alanları boş bırakarak veya varsayılan değerlerine ayarlayarak iş akışı üzerinden gitmeye devam edin.

Yük teslim alma görevi tamamlanır ve teslim alma görevlisi bir sonraki görevine hareket edebilir. Bununla birlikte, ambar teslim alma personeli sonuç olarak yükleme kaydını gözden geçirecek ve alınan miktarın beklenen miktardan az olduğunu görebilecektir. Daha sonra, web istemcisini kullanarak aşağıdaki yordamı tamamlayacaktır.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Listede, yeni teslim aldığınız yüklemeyi bulun. ( **Sevk edildi** yük durumuna sahip gelen yükleri dahil etmek için _Kapalı olanı göster_ onay kutusunu seçmeniz gerekebilir.) Sonra yükü açmak için **Yük kodu** sütunundaki bağlantıyı seçin.
1. Yük kaydında, **Yük durumu** değerinin _Sevk edildi_ olarak kaldığını ancak yük satırındaki **İş oluşturulan miktar** değerinin _9_ olarak değiştiğini dikkate alın.
1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Listede, yeni teslim aldığınız satınalmayı bulun ve siparişi açmak için **Satınalma siparişi** sütunundan bağlantıyı seçin.
\
1. **Satınalma siparişi satırları** hızlı sekmesinde, **Stok \> Görünüm \> Hareketler**'i seçin.
1. İki satınalma siparişi hareketinin ayrıntılarını gözden geçirin. ( **Yük kodu** alanını kılavuza görebilmek için **Stok hareketleri** sayfasını kişiselleştirmek zorunda kalabilirsiniz.) İki hareket görmelisiniz:

    - _Kayıt edildi_ durumunda girişi olan hareket, mobil cihaz kullanılarak belirli bir yük için çalıştırılan _9_ kayıt miktarını gösterir. **Yük kodu**, söz konusu hareketle ilişkilidir.
    - _Sipariş edildi_ durumunda girişi olan hareket, kalan kayıtlı olmayan sipariş satırı miktarı olan _1_'i gösterir.

#### <a name="product-receiptpost-the-registered-load-quantities-against-purchase-orders"></a>Kayıtlı ürün miktarlarını satınalma siparişlerine göre ürün girişiyle deftere nakletme

Bu yordamda, bir yük için kaydettiğiniz stoğu ürün girişiyle deftere nakledersiniz. Sonuç olarak, teslim alınan stok ve ilgili maliyetleri şirketin genel muhasebesine eklenecektir.

1. **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Listede, teslim aldığınız yüklemeyi bulun. ( **Sevk edildi** yük durumuna sahip gelen yükleri dahil etmek için _Kapalı olanı göster_ onay kutusunu seçmeniz gerekebilir.) Sonra yükü açmak için **Yük kodu** sütunundaki bağlantıyı seçin.
1. Eylem Bölmesinde **Sevk ve teslim alma** sekmesinde **Teslim al\> Ürün girişi**'ni seçin. Eylemi onaylamanız istendiğinde, **Evet**'i seçin.
1. **Ürün girişinin deftere nakli** iletişim kutusunda, **Satırlar** hızlı sekmesinde, kılavuzu denetleyin. Seçili yüke göre miktarın kaydedildiği satınalma siparişi satırını görmelisiniz.

    > [!NOTE]
    > _Yük başına birden fazla ürün girişine izin ver_ özelliğinin kullanılamadığı veya etkinleştirilmediği sürümlerde, **Yük satırları** kılavuzunda gösterilen varsayılan miktar satınalma siparişi satırıyla ilişkili tüm yüklerde kaydedilen toplam miktar olacaktır.

1. **Genel bakış** hızlı sekmesinde kılavuzdaki **Ürün girişi** alanını denetleyin. Seçili yükün kimliğini içeren bir sayıya ayarlandığına dikkat edin.
1. Ürün girişini deftere nakletmek için **Tamam**'ı seçin ve **Ürün girişini deftere nakletme** iletişim kutusunu kapatın.
1. Yükleme ayrıntılarına geri dönersiniz. Aşağıdaki noktalara dikkat edin:

    - **Yük durumu** alanı şimdi  _Teslim alındı_ olarak ayarlandı.
    - Yük satırında, yükün **Miktar** değeri, kaydedilen miktarla eşleşmesi için  _10_  yerine _9_ olarak değiştirilmiştir, ancak **İş oluşturulan miktar** değeri _9_ olarak kalır.

Satınalma takımı satıcının kalan sipariş miktarı olan 1'i teslim etmesini beklemiyorsa, satırın teslim kalanını _0_ olarak güncelleştirerek siparişi kapatabilir. Bununla birlikte, özgün yüklemede eksik parçanın geldiğini öğrendikten sonra ambar personeli aşağıdaki eylemlerden birini gerçekleştirebilir:

- Miktarı aynı yüke göre kaydedin. Bu durumda, **Yük durumu** alanı _Sevk edildi_ olarak sıfırlanacak ve **İş oluşturulan miktar** değeri _10_ olarak güncelleştirilecektir. Bu seçenek yalnızca aşağıdaki durumlarda kullanılabilir:

    - _Yük miktarlarını fazladan teslim alma_ özelliği kullanılamaz veya etkin değildir.
    - _Yük miktarlarını fazladan teslim alma_ özelliği kullanılabilir ve etkindir ve **Fazla teslim alınan yük satırı miktarı** alanı _İzin ver_ olarak ayarlanır.

- Miktarı yeni veya varolan bir yüke ekleyin ve her zamanki şekilde işleyin.
- Miktarı yük işlemeyi içermeyen bir şekilde kaydedin ve/veya teslim alın.

### <a name="example-scenario-2-register-quantities-that-arrive-on-multiple-inbound-loads-where-some-items-are-missing"></a>Örnek senaryo 2: Bazı maddelerin eksik olduğu birden fazla yükle gelen miktarları kaydedin

Bu senaryoda, tek bir satınalma sipariş satırıyla ilişkili olan bir gelen sevkiyat iki yüke bölünecektir. Örneğin, bir satınalma siparişi satırı ağırlık ve/veya hacimdeki fiziksel yük sınırlamaları nedeniyle birden fazla yüke bölünebilir.

Bu senaryo aynı yük için birden çok ürün giriş deftere nakil işleminin nasıl işleneceğinide gösterir. Birden fazla gelen yükle gelen miktarları kaydedersiniz ancak miktarlar beklenen miktarlarla eşleşmeyecektir. Ürün girişi deftere nakli aracılığıyla gerçekleşen maliyet güncelleştirmeleri aynı yük için birden fazla kez yapılır.

#### <a name="set-up-load-receiving-policies"></a>Yük teslim alma ilkeleri ayarlama

Bu yordamda, aynı yükten birden çok ürün girişi deftere nakil işlemini etkinleştireceksiniz.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Yükler** sekmesinde, **Yük başına birden fazla ürün girişine izin ver** alanını _Evet_ olarak ayarlayın.

#### <a name="create-two-loads-to-plan-receipt-of-a-purchase-order"></a>Bir satınalma siparişinin girişini planlamak için iki yük oluşturma

Bu yordamda, bir satınalma siparişi ve iki yük oluşturacaksınız. Sonra, satıcı tarafından sevk edildiği (yük durumunu güncelleştirir) benzetimi yapmak için her yükü el ile güncelleştireceksiniz. Böylece, ambar planlayıcıları, beklenen gelen yükleri bulmak için yükleri **Yük durumu** ile filtreleyebilir.

Ayrıca, satır için belirtilen miktardan yüzde 20 oranında fazla bir miktar teslim alabileceğiniz satınalma siparişi satırını nasıl ayarlayacağınızı öğreneceksiniz.

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Satıcı** hızlı sekmesinde **Satıcı hesabı** alanını _1001_ olarak ayarlayın ve **Tamam**'ı seçin.
1. Yeni satınalma siparişiniz açılır ve **Satınalma siparişi satırları** kılavuzuna boş bir satır dahil edilir. Bu sipariş satırı için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** _A0001_
    - **Ambar:** _24_
    - **Miktar:** _10_

1. **Satır ayrıntıları** hızlı sekmesinde **Teslimat** sekmesinde, **Fazla teslimat** alanını _20_ olarak ayarlayın.
1. Eylem Bölmesinde, **Satınalma** sekmesinde, **Eylemler \> Onayla**'yı seçin. Sipariş durumu artık _Onaylandı_ olur.
1. Eylem Bölmesinde, **Ambar** sekmesinde, **Eylemler \> Yük planlama workbench**'ini seçin.
1. **Yük planlama workbench'i** sayfasında, Eylem Bölmesinde **Tedarik ve talep** sekmesinde, **Ekle \> Yeni yüke**'yi seçin.
1. **Yük şablonu ataması** iletişim kutusunda **Yük şablonu kodunu** _20' Konteyner_ olarak ayarlayın. **Ayrıntılar** sekmesinde, satınalma siparişi satırı miktarını kısmi olarak eklemek için **Miktar** değerini _10_ yerine _5_ olarak ayarlayın.
1. Ayarlarınızı uygulayıp iletişi kutusunu kapatmak için **Tamam**'ı seçin.
1. İkinci bir yük oluşturmak için 8 ile 10 arasındaki adımları yineleyin. Bu kez, **Miktar** alanı zaten _5_ ayarlanmış olmalıdır.
1. **Yükleme planlama workbenchi** sayfasında, **Yükler** kılavuzunda, oluşturduğunuz ilk yükün **Yük kodu** değerini seçin. **Yük ayrıntıları** sayfası görüntülenir ve seçili yükü gösterir. Aşağıdaki adımları izleyin:

    1. Eylem Bölmesinde **Sevk ve teslim alma** sekmesinde **Onayla\> Gelen sevkiyat**'ı seçin.
    1. **Yük durumu** değerinin _Sevk edildi_ olarak değiştiğini unutmayın.
    1. **Yük planlama workbenchi**'ne dönmek için Kapat düğmesini seçin.

1. Oluşturduğunuz ikinci yük için önceki adımı yineleyin.
1. **Yük** kılavuzunda görünen iki **Yük kodu** değerini not edin.

#### <a name="register-partial-receipt-of-the-quantities-that-arrived-on-the-first-load-and-post-the-registered-load-quantities"></a>İlk yükte gelen miktarların kısmi girişini kaydedin ve kaydedilen yük miktarlarını deftere nakledin

Yükler ambar teslim alma limanına ulaştığında, bir teslim alma memuru yük miktarlarını bir mobil cihaza kaydeder. Bir yükle bağlantılı olan kayıtlı stok, yükü temel alarak, satınalma siparişi ürün girişini deftere naklederek şirketin genel muhasebe defterindeki maliyet güncelleştirilir.

Bu yordamda, bir teslim alma memurunun bir mobil cihaza yük miktarlarını nasıl kaydedeceği gösterilir.

1. Ambar 24'te oturum açmak için mobil cihazınızı kullanın. (Standart demo verilerinde, kullanıcı kimliği _24_ ve parola olarak _1_'i kullanarak oturum açın.)
1. Bu senaryo için oluşturduğunuz _Yük maddesi teslim alma_ menü öğesini seçin.
1. Aşağıdaki değerleri girmek için ekrandaki veri girişi yönergelerini izleyin. (Sipariş, kullanmakta olduğunuz mobil cihaza veya emülatöre göre değişebilir.)

    - **Yük** – Önceki yordamda oluşturduğunuz ilk yük kodunu girin.
    - **Madde** – Bu yük için beklenen madde olan _A0001_ girin.
    - **Miktar** – _3_ girin. Bu miktarın beklenen miktardan az olduğunu unutmayın. Bu senaryoda, alıcı memuru olarak, bu yükle ilgili tüm miktarları kaydetmek için zamanınız olmadığını düşünün. Bu yordamın ilerleyen kısımlarında, bu adımı tekrarlayarak ve **Miktar** alanını _2_ olarak ayarlayarak kalan parçaları kaydedeceksiniz.

1. Cihazınız işin tamamlandığını bildirene kadar, diğer tüm alanları boş bırakarak veya varsayılan değerlerine ayarlayarak iş akışı üzerinden gitmeye devam edin.
1. Web istemcisinde **Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.
1. Listede, yeni teslim aldığınız yükü bulun ve yükü açmak için **Yük kodu** değerini seçin. **Yük durumu** değerinin _Sevk edildi_ olarak kaldığını ancak yük satırındaki **İş oluşturulan miktar** değerinin _3_ olarak değiştiğini dikkate alın.
1. Eylem Bölmesinde **Sevk ve teslim alma** sekmesinde **Teslim al\> Ürün girişi**'ni seçin. Eylemi onaylamanız istendiğinde, **Evet**'i seçin.
1. **Ürün girişini deftere nakletme** iletişim kutusunda gösterilen değerleri gözden geçirin ancak değiştirmeyin ve **Tamam**'ı seçin.
1. Seçili yükünüz için **Yük ayrıntıları** sayfasına geri dönersiniz. Aşağıdaki noktalara dikkat edin:

    - **Yük durumu** alanı  _Teslim alındı_ değerine ayarlanmış olarak kalır.
    - Yük satırında, yük için **Miktar** değeri _5_ parça olarak kalır (bu orijinal yük miktarıdır) ve **İş oluşturulan miktar** değeri _3_ olarak kalır.

1. Bu yordamı yineleyerek, bu yükte kalan miktarın kaydını tamamlayın. Ancak, adım 3'te **Miktar** alanını _2_ olarak ayarlayın.

İlk yük için teslim alma görevi şimdi tamamlandı. İki ürün giriş günlüğü oluşturuldu: çalıştırdığınız iki ürün girişi güncelleştirmesinin her biri için bir tane olacak şekilde.

#### <a name="register-receipt-of-the-quantities-that-arrived-on-the-second-load-and-account-for-the-overdelivered-quantity"></a>Fazla teslim edilen miktar için ikinci yükte ve hesapta ulaşan miktarların girişini kaydedin

Bu senaryoda, teslim alma memuru, yükte var olan miktarı aşan miktarı gelen olarak kaydedecektir. Sistem fazla teslimata izin verecek şekilde ayarlandığından, fazla teslim almaya izin verilir.

1. Ambar 24'te oturum açmak için mobil cihazınızı kullanın. (Standart demo verilerinde, kullanıcı kimliği _24_ ve parola olarak _1_'i kullanarak oturum açın.)
1. Bu senaryo için oluşturduğunuz _Yük maddesi teslim alma_ menü öğesini seçin.
1. Aşağıdaki değerleri girmek için ekrandaki veri girişi yönergelerini izleyin. (Sipariş, kullanmakta olduğunuz mobil cihaza veya emülatöre göre değişebilir.)

    - **Yük** – Daha önce oluşturduğunuz ikinci yük kodunu girin.
    - **Madde** – Bu yük için beklenen madde olan _A0001_ girin.
    - **Miktar** – Satıcının 12 olan toplam satınalma siparişi miktarının parçası olarak teslim etme iznine sahip olduğu kalan miktar olan _7_ değerini girin (orijinal sipariş miktarı 10'dur ve 2 yüzde 20'lik izin verilen fazla teslimat miktarıdır). 5 parçanın ilk yük için kaydedilmiş olduğunu unutmayın.

İkinci yük şimdi 7 miktarıyla güncelleştirilir ve bu miktara göre ürün girişiyle güncelleştirilebilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]