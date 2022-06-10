---
title: Stok deftere nakil profilleri
description: Bu konu, stok deftere nakil profillerine genel bakış sağlamaktadır.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28e3a3051978f921e01a929496e96909e6c32429
ms.sourcegitcommit: 00b39900d3cbdbc9ca1ab3145265007f5dc98a3f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/25/2022
ms.locfileid: "8806383"
---
# <a name="inventory-posting-profiles"></a>Stok deftere nakil profilleri

[!include [banner](../includes/banner.md)]

Stok deftere nakil profilleri, stok yardımcı defteri hareketlerinin genel muhasebe defterine naklini kontrol eder. Stok yardımcı defteri hareketleri **Satış ve pazarlama**, **Tedarik ve kaynak atama** ve **Üretim denetimi** gibi birçok modül kullanılarak oluşturulabilir. Bir maddenin satış siparişinde veya satınalma siparişinde kullanıldığı her seferde stok yardımcı defteri hareketleri nakledilebilir. 

Ek stok yardımcı defteri hareketleri aşağıdaki durumlarda deftere nakledilebilir:
- Belge her güncelleştirildiğinde.
- Bir satış siparişi sevk irsaliyesi veya faturası deftere nakledildiğinde.
- Bir satınalma siparişi ürün girişi veya faturası oluşturulduğunda.

Daha fazla bilgi için Stok yardımcı defteri hareketleri konusuna gidin.

## <a name="inventory-transaction-overview"></a>Stok hareketine genel bakış

Her stok yardımcı defteri hareketi şunları içerir:
 - Miktar 
 - Fiyat 
 - Site 
 - Ambar 
 - Konum 

Stok yardımcı defteri hareketleri, fiziksel deftere nakil ve mali deftere nakil aracılığıyla genel muhasebe defterinde iki giriş oluşturur. Daha fazla bilgi için [Fiziksel ve mali güncelleştirmeler](/supply-chain/cost-management/physical-financial-updates.md) konusuna gidin.
Aşağıdaki örnek, üç satırlık bir satınalma siparişine aittir. Bu örnekte, tüm siparişin tek bir tesis ve ambar için olduğunu varsayın. Her satınalma siparişi satırında tek bir ilgili InventTrans kaydı (diğer adıyla, stok hareketi) vardır ve her satırda belirtilen miktar 10'dur. Aşağıdaki diyagramda, bir satınalma siparişi üst bilgisiyle her biri bir InventTrans kaydına sahip olan üç satınalma siparişi satırının ilişkisi gösterilmiştir.

![Her biri InventTrans kaydına sahip olan üç satırlık bir satınalma siparişi için ilişki diyagramı.](./media/InventTransRelationship.PNG)

Birinci satınalma siparişi satırında miktar olarak 5 adet madde alınmıştır. Satın alma siparişinin ikinci satırında tam miktar alınmış, üçüncü satırında ise miktar alınmamıştır. Artık ilk satınalma siparişi satırıyla ilgili olan ikinci bir stok hareketi vardır. İkinci satınalma siparişi satırının hareketi **Alındı** olarak güncelleştirilir ve üçüncü hareket aynı kalır. Aşağıdaki diyagramda, satınalma sipariş satırı 1 için ek InventTrans kaydıyla ilişki gösterilmektedir.

![Üç satırlık bir satınalma siparişi için ilişki diyagramı. Satırlardan biri kısmen alındı durumundadır ve iki InventTrans kaydı gösterilmektedir.](./media/InventTransRelationshipPartialReceipt.PNG)

Bu örnekte, genel muhasebe defterine bir fiş nakledilir. Bu fiziksel fiştir. Madde modeli grubu fiziksel stoğu deftere nakledecek şekilde yapılandırılır ve tüm maddeler aynı madde modeli grubunu kullanır. Stok deftere nakil profili tek bir ana hesap kümesi kullanıyor. Tek bir fiş oluşturulur ve InventTrans kaydı hem InventTrans 1, hem de InventTrans 2 öğesini aynı fişe bağlar.

Ardından, 1. ve 2. satırlarda alınan miktar için bir fatura alınır. Genel muhasebe defterinde başka bir fiş oluşturulur; bu mali fiştir. Madde model grubu, mali stoğu deftere nakledecek şekilde yapılandırılır. Yeni ikinci fiş, InventTrans 1 ve InventTrans 2 ile ilgilidir.

Maliyetlendirme modeline bağlı olarak, stok kapanışı ve kapatma işlemleriyle ilgili stok yardımcı defteri hareketleriniz için üçüncü bir genel muhasebe defterine nakil olabilir. Daha fazla bilgi için [Stok kapatma](/supply-chain/cost-management/inventory-close.md) konusuna gidin. **Stok yönetimi** > **Sorgular ve raporlar** > **Hareketler** bölümüne giderek tüm stok hareketlerinizin ayrıntılarını görebilirsiniz.

>[!Important]
> Stok hareketleri, her bir ayrı stok boyutu birleşimi ve her kısmi güncelleştirme için bölünür. Bu, önceki örnekte kısmi güncelleştirmeler için gösterilmiştir.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Stok boyutuna göre stoğu bölme örneği

Örnekteki satınalma siparişi satırı 3 seri hale getirilmiş bir maddedir. Alma işlemi sırasında satınalma siparişi için on seri numarası kaydedilir. Stok hareketi 10 stok hareketine bölünür. Aşağıdaki diyagramda, ilişki ve her biri satınalma sipariş satırı 3 ile ilişkili kendi seri numarasına sahip olan ek stok hareketleri gösterilmektedir.

![Üç satırlık bir satınalma siparişi için ilişki diyagramı. Satırlardan biri seri hale getirilmiştir ve ek InventTrans kayıtları gösterilmektedir](./media/InventTransRelationshipSerialNumber.PNG)

Yukarıdaki örnekte, her bir seri numarası tek bir ürün girişinde alınırsa, ek bir fiş oluşturulur. Fiziksel fiş alanı her bir seri numarasına bağlanır. Aynı durum, satınalma siparişini faturalandırdığınızda mali güncelleştirme için de geçerlidir.

## <a name="inventory-transactions"></a>Stok hareketleri

**Stok hareketleri** sayfasındaki **Stok ve ambar yönetimi** ya da **Maliyet yönetimi**'nin altında stok hareketlerini görebilirsiniz. Ayrıca, belirli bir kaynak belge satırı (ör. satınalma siparişi satırı veya satış siparişi satırı) ilgili stok hareketlerini **Stok**'u ve ardından **Hareketler**'i seçerek görebilirsiniz. 

**Stok hareketleri** sayfası aşağıdaki alanları içerir.

| Alan            | Açıklama                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Madde numarası      | Hareketle ilişkili madde numarası.                                                                  |
| Fiili tarih    | Stoğun ambara ulaştığı, ambardan ayrıldığı, üretimde tüketildiği veya üretildiği tarih. Örneğin, satış siparişi için
sevk irsaliyesi deftere nakil tarihi veya satınalma siparişi için ürün girişi deftere nakil tarihi.                             |
| Mali tarih   | Stok hareketinin kapatıldığı ve maliyetin genel muhasebe defterine kaydedildiği tarih. Örneğin, satış veya satınalma siparişi için 
fatura oluşturma deftere nakil tarihi. Mali tarih doldurulduktan sonra başvuru belgesinde güncelleştirme yapılmasına izin verilmez. |
| Referans        | Hareketin kaynağını ve **Numara** alanında görüntülenen belge türünü gösterir. Örneğin; satış siparişi, satınalma siparişi veya transfer emri girişi.                                                 |
| Sayı           | Hareketin başvuru kimliğini gösterir. Örneğin, **Başvuru** alanı satış siparişini gösteriyorsa, **Numara** alanı satış siparişi numarasını belirtir.                                                       |
| Giriş (durum) | Giriş olan stok hareketleri için bu alan girişin durumunu gösterir. Örneğin, satınalma siparişi bir giriştir ve durumu **Sipariş Edildi** veya **Satın Alındı** olabilir.                                                            |
| Çıkış (durum)   | Çıkış olan stok hareketleri için bu alan çıkışın durumunu gösterir. Örneğin, satış siparişi bir çıkıştır ve durumu **Siparişte** veya **Satıldı** olabilir.                         |
| Miktar         | Stok hareketinin miktarı. Pozitif sayılar, stok girişleri için kullanılırken negatif sayılar stoktan çıkışlar için kullanılır.                                                                                                                          |
| Birim             | Miktarın ifade edildiği ölçü birimi.                                                                                   |
| FA miktarı      | Hareketin fiili ağırlık miktarı. Daha fazla bilgi için [Fiili ağırlık maddeleri hakkında](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.) bölümüne gidin.       |
| FA birimi          | Fiili ağırlık miktarının ifade edildiği fiili ağırlık ölçü birimi.                                                         |
| Maliyet tutarı      | Stok hareketinin nihai maliyeti. Bir hareket mali olarak güncelleştirildiğinde bu alan doldurulur. Maliyetlendirme yönteminize bağlı olarak, Stok kapatma ve düzeltme işlemi bu alanı güncelleştirebilir.                            |

## <a name="inventory-status"></a>Stok durumu

Her stok hareketi, **Giriş** veya **Çıkış** alanında gösterilen bir duruma sahiptir. Kullanılan alan, stok hareketlerinin türüne bağlıdır. Girişler stoğu artıran hareketlerdir. Örneğin, pozitif miktara sahip bir satınalma siparişi veya negatif miktara sahip bir satış siparişi iadesi. Çıkışlar, stoğu azaltan stok hareketleridir. Örneğin, pozitif miktara sahip bir satış siparişi veya negatif miktara sahip satınalma siparişi iadesi.

### <a name="receipt-status"></a>Giriş  durumu

Aşağıdaki tabloda, **Giriş** durumu açıklanmaktadır.

| **Giriş  durumu** | **Tanım**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Sipariş edilen            | Bir girişi temsil eden tüm stok hareketlerinin başlangıç durumu. Buna, pozitif miktara sahip satın alma siparişleri, üretim emirleri veya negatif miktara sahip satış siparişi iadeleri dahildir.                                                   |
| Kayıtlı         | Bu durum, iki aşamalı bir alma işlemi gerçekleşirken veya madde varışının ürünün vardığını göstermek için kullanıldığı durumlarda kullanılır. Bu, parti veya seri numaraları "tahsis edildiğinde" veya siparişe kaydedildiğinde kullanılır. Madde varışı hakkında daha fazla bilgi için [Varışa genel bakış](/supply-chain/inventory/arrival-overview.md) konusuna gidin. |
| Teslim Alındı           | Bu durum, hareket fiziksel olarak güncelleştirildiğinde kullanılır. Satınalma siparişi için bu durum, ürün girişi deftere nakledildiğinde gerçekleşir. Satış siparişi iadesi için bu durum, sevk irsaliyse deftere nakledildiğinde gerçekleşir.                                                                            |
| Satın alındı          | Bu durum, hareket mali olarak güncelleştirildiğinde kullanılır. Satınalma siparişi veya satış siparişi iadesi için bu durum, fatura oluşturulduğunda gerçekleşir.                                                                                             |

### <a name="issue-status"></a>Çıkış durumu

Aşağıdaki tabloda, **Çıkış** durumu açıklanmaktadır.

| **Çıkış durumu**  | **Tanım**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| Siparişte          | Bir çıkışı temsil eden tüm stok hareketlerinin başlangıç durumu. Buna, pozitif miktara sahip satış siparişleri, üretim emirleri, BOM veya formül satırları ya da negatif miktara sahip satınalma siparişi iadeleri dahildir.                                             |
| Siparişli rezerve miktar  | Bu stok durumu, stoğun oluşturulmuş bir sipariş ile ilgili olarak rezerve edildiğini ancak henüz stokta fiziksel olarak teslim alınmadığını gösterir. Stok alındığında, durum otomatik olarak **Fiziksel rezerve miktar** olarak güncelleştirilir. Rezervasyonlar hakkında daha fazla bilgi için [Stok miktarlarını rezerve etme](/supply-chain/inventory/reserve-inventory-quantities.md) bölümüne gidin. |
| Fiziksel rezerve miktar | Bu durum, stoğun belirli bir sipariş için ayrıldığını veya rezerve edildiğini gösterir. Stok rezerve edildiğinde fiziksel olarak diğer siparişlerde kullanılamaz.                                 |
| Malzeme çekildi         | Bu, stoğun ambardan çekildiği anlamına gelir. Stok hala fiziksel olarak ambardadır, kaldırılmamıştır ancak diğer siparişler için kullanılamaz.  |
| Düşülen          | Bu durum, hareket fiziksel olarak güncelleştirildiğinde kullanılır. Satış siparişi için bu, sevk irsaliyesinin deftere nakledildiği durumdur; Satınalma siparişi iadesi için bu, ürün girişinin deftere nakledildiği durumdur.                                                                      |
| Satılan              | Bu, hareket mali olarak güncelleştirildiğinde kullanılan durumdur. Satınalma siparişi veya satış siparişi için bu durum, fatura oluşturulduğunda gerçekleşir.|

Stok hareketleri hakkında daha fazla bilgi için [Stok hareketleri ayrıntısı](/supply-chain/inventory/inventory-transactions-details.md) konusuna gidin.

## <a name="configure-an-inventory-posting-profile"></a>Stok deftere nakil profili yapılandırma

Stok deftere nakil profili yapılandırmak için aşağıdaki adımları izleyin:

1.  **Stok yönetimi** > **Ayarlama** > **Deftere nakil** > **Deftere nakil**'i açın.
2.  Hareket türüne uygun sekmeyi seçin. Örneğin, **Satınalma siparişi**'ni seçin.
3.  Deftere nakil türü için radyo düğmesini seçin. Örneğin, **Gider için satınalma harcaması**'nı seçin.
4.  **Yeni**'yi seçin.
5.  **Madde kodu** alanında **Tablo**, **Grup**, **Tümü** veya **Kategori** için bir seçenek belirleyin. Örneğin, belirli bir madde grubuyla ilgili deftere nakil profilini yapılandırmak için **Grup**'u seçin.
     - 5. adımda **Tablo**'yu seçtiyseniz, **Madde ilişkisi** alanında deftere nakil profili için belirli Madde numarası'nı seçin.
     - 5. adımda **Grup** öğesini seçtiyseniz, **Madde ilişkisi** alanında deftere nakil profili için **Madde grubu**'nu seçin.
     - 5. adımda **Tümü** seçeneğini belirlediyseniz, **Madde ilişkisi** alanı boş bırakılır.
     - 5. adımda **Kategori** seçeneğini belirlediyseniz, **Madde ilişkisi** alanı boş bırakılır. **Kategori ilişkisi** alanını kullanarak deftere nakil profilinin uygulanacağı kategoriyi seçin.

6.  **Hesap kodu** alanında **Tablo**, **Grup** veya **Tümü** için bir seçenek belirleyin. Örneğin, deftere nakil profilini tüm satıcılara uygulamak için **Tümü** seçeneğini belirleyin.
     - 5. adımda **Tablo**'yu seçtiyseniz, **Hesap ilişkisi** alanında deftere nakil profili için belirli bir satıcı numarasını seçin.
     - 5. adımda **Grup** öğesini seçtiyseniz, **Hesap ilişkisi** alanında deftere nakil profili için satıcı grubunu seçin.
     - 5. adımda **Tümü** seçeneğini belirlediyseniz, **Hesap ilişkisi** alanı boş olur.

7.  Seçili nakil türündeki belirli bir vergi grubunu ilişkilendirmek üzere bir **Satış vergisi grubu** seçin. Bu alan boşsa deftere nakil türleri, mevcut tüm vergi gruplarına uygulanır. Vergi grupları için belirtilen deftere nakil, yalnızca, satış ve satın alma hareketlerine uygulanır.
8.  Hesap türünü **Ana hesap** alanına nakletmek için hesap numarasını belirtin. Hesap türü olarak kullanmak üzere henüz bir hesap numarası oluşturulmadıysa yeni bir hesap kullanabilirsiniz. Genel muhasebedeki **Ana hesap ayrıntıları** sayfasında yeni bir hesap oluşturun.

## <a name="additional-resources"></a>Ek kaynaklar

**Stok deftere nakil profili** sayfasındaki her bir sekme, Dynamics 365 Supply Chain Management'taki bir yardımcı defter ile ilişkilidir. Daha fazla bilgi için aşağıdakileri inceleyin:
-   [Satış siparişi deftere nakli](sales-order-posting.md)
-   [Satın alma siparişi deftere naklediliyor](purchase-order-posting.md)
-   [Stok deftere nakil işlemi](inventory-posting.md)
-   [Üretim denetimini deftere nakletme](production-posting.md)
-   [Standart maliyet farkını deftere nakletme](standard-cost-variance-posting.md)
