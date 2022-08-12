---
title: Satın alma siparişi deftere naklediliyor
description: Bu makale, Stok deftere nakil profilleri sayfasının Satınalma siparişi sekmesini açıklar.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 38a9e2740232b18255109ba867fcdddd5b890774
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151047"
---
# <a name="purchase-order-posting"></a>Satın alma siparişi deftere naklediliyor

**Stok deftere nakil profilleri** sayfasındaki **Satınalma siparişi** sekmesi satınalma siparişlerinin genel muhasebeye nasıl nakledileceğini denetlemek için kullanılır. Bir satınalma siparişi için genel muhasebeye iki ana faaliyet nakledilir: 

- Ürün girişi
- Fatura

Fiziksel bir hareketin (ürün girişi) bir satınalma siparişinde genel muhasebeye nakledilmesi için aşağıdaki onay kutularının seçili olması gerekir:

- **Stok ve ambar yönetim parametreleri** sayfasında **Ürün girişini genel muhasebeye naklet** onay kutusu.
- **Madde model grupları** sayfasında **Fiziksel stoğu deftere naklet** ve **Ürün girişinde borcu tahakkuk ettir** onay kutuları.

Ana hesaplar **Stok deftere nakil profili** sayfasında aşağıdaki deftere nakil türleri için belirtilmelidir:

- Stoğa giren satın alınmış malzemelerin maliyeti
- Faturalanmamış satınalma harcaması
- Satınalma, tahakkuk

Mali bir hareketin (fatura) bir satınalma siparişinde genel muhasebeye nakledilmesi için aşağıdaki koşulların karşılanması gerekir:

- Satınalma siparişi satırındaki seçili madde için **Madde model grupları** sayfasındaki **Mali stoğu deftere naklet** onay kutusunun seçilmiş olması gerekir.
- Ana hesaplar **Stok deftere nakil profili** sayfasında aşağıdaki deftere nakil türleri için belirtilmelidir:
  - Faturalanan satın alınmış malzemelerin maliyeti
  - Ürün için satınalma harcaması
  - Gider için satınalma harcaması
  - İskonto (isteğe bağlı)

## <a name="fixed-receipt-price-posting"></a>Sabit giriş fiyatını deftere nakletme

Bir madde için **Madde model grupları** sayfasındaki **Stok modeli** alanında **Standart maliyet** seçeneğini belirlemek yerine bir ürün için standart maliyet olarak sabit giriş fiyatını kullanabilirsiniz. **Sabit giriş fiyatı** kullanıldığında oluşacak temel fark, stok girişi deftere nakledildiğinde madde için geçerli maliyet fiyatının kullanılacak olmasıdır. **Sabit giriş fiyatı için** maliyet yeniden değerleme işlemi yapılmaz; Bir mali güncelleştirme deftere nakledildiğinde, geçerli maliyet fiyatı deftere nakil sırasında kullanılır. Girişte kullanılan maliyet fiyatı ile fatura arasında fark varsa bu fark, sabit giriş fiyatı kar ve zarar hesaplarına nakledilir.

Bir ürün için sabit giriş fiyatı kullanmak üzere aşağıdakileri yapılandırmanız gerekir:

- **Madde model grupları** sayfasında **Fiziksel stoğu deftere naklet** ve **Sabit giriş fiyatı** onay kutularını seçin. 
- **Stok ve ambar yönetimi parametreleri** sayfasında, **Sevk irsaliyesini genel muhasebeye naklet** onay kutusunu seçin.
- **Stok deftere nakil profili** sayfasında, aşağıdaki deftere nakil türleri için ana hesapları belirtin:
  - Sabit giriş fiyatı karı
  - Sabit giriş fiyatı zararı
  - Sabit giriş fiyatı mahsup işlemi

Daha fazla bilgi için [Sabit giriş fiyatı](/supply-chain/cost-management/fixed-receipt-price.md) konusuna gidin.

## <a name="purchase-charges-and-stock-variation-posting"></a>Satınalma masrafları ve stok varyasyonu deftere nakli

Satın alma masrafları ve stok varyasyonlarını hesaba katmayı planlıyorsanız aşağıdakileri yapın:

- **Fatura** sekmesindeki **Borç hesapları parametreleri** sayfasında, **Genel muhasebedeki gider hesabına naklet** onay kutusunu seçin.
- Satınalma siparişi satırında seçili maddenin **Madde model grupları** sayfasında, **Fiziksel stoğu deftere naklet**, **Mali stoğu deftere naklet** ve **Ürün girişinde borcu tahakkuk ettir** onay kutularını seçin.
- **Tedarik ve kaynak atama parametreleri** sayfasında, **Ürün girişinde masraf oluştur** onay kutusunu seçin.
- **Stok ve ambar yönetimi parametreleri** sayfasında, **Sevk irsaliyesini genel muhasebeye naklet** onay kutusunu seçin.

**Stok deftere nakil profili** sayfasında, aşağıdaki deftere nakil türleri için ana hesapları belirtmelisiniz:

- Faturalanmamış satınalma harcaması
- Ürün için satınalma harcaması
- Stok değişimi

> [!NOTE]
> **Genel muhasebedeki gider hesabına naklet** parametresi seçildiğinde **Masraf** deftere nakil türü kullanılamaz.

Daha fazla bilgi için [Gider hesabına naklet muhasebe ilkesi](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md) konusuna gidin.

## <a name="sample-posting-profile-configuration"></a>Örnek deftere nakil profili yapılandırması

Aşağıdaki tabloda örnek ana hesapları ve açıklamaları olan varsayılan deftere nakil türleri örnekleri gösterilmiştir:

- **Temizleme hesabı** sütunu, deftere nakil türünün bir temizleme hesabı olduğunu belirtir. Sonraki bir hareket deftere nakledildiğinde, bu hesapta deftere nakledilen tutar için otomatik olarak ters işlem uygulanır. 
- **P/F** sütunu fiziksel deftere nakil için **P** ve mali deftere nakil için **F**'yi belirtir. 
- **İzle** sütunu, belirli bir deftere nakil türü ana hesabının genellikle başka bir deftere nakil türüyle aynı olup olmadığını gösterir. Sütundaki değer genellikle kullanılan deftere nakil türünü gösterir.

> [!NOTE]
> Ana hesaplar ve ana hesap adları yalnızca önerilerdir. İş gereksinimleriniz için<!--note from editor: Via Writing Style Guide.--> en iyi yapılandırmayı belirlemek amacıyla muhasebeciniz ile çalışmanızı öneririz.


| Deftere nakil türü | Temel hesap örneği | Temel hesap adı örneği | Hesap türü | Borç/Alacak? | Kliring hesabı | P/F | İzle | Açıklama |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| Stoğa giren satın alınmış malzemelerin maliyeti | 140100</br>140101 | Malzeme stoğu</br>Sevk edilip faturalanmayan malzemeler | Varlık | Borç | Evet | P | Faturalanan satın alınmış malzemelerin maliyeti | Bir satınalma siparişi ürün girişi deftere nakledildiğinde ve hesaba mahsup, faturalanmayan Satınalma harcaması olduğunda kullanılır. Bir satınalma siparişi faturası deftere nakledildiğinde, bu hesaptaki tutar için ters işlem uygulanır. |
| Faturalanmamış satınalma harcaması | 600180 | Malzeme girişleri | Gider | Borç | Evet | P | |Satınalma siparişi deftere nakledildiğinde kullanılır. Standart maliyet kullanıldığında satınalma fiyatı farklarını takip etmek için iki fiş oluşturulur. İlk fişteki hesabın mahsubu, Satınalma tahakkuk hesabıdır. İkinci fişteki mahsup, Stoğa giren satın alınmış malzemelerin maliyeti ve Satın alma fiyat farkı hesaplarının toplamıdır. Bir satınalma siparişi faturası deftere nakledildiğinde bu hesaba nakledilen tutarlara ters işlem uygulanır. |
| Faturalanan satın alınmış malzemelerin maliyeti | 140100 | Malzeme stoğu | Varlık | Borç | No. | C  |Stoğa giren satın alınmış malzemelerin maliyeti | Bir satınalma siparişi faturası deftere nakledildiğinde kullanılır. Bu hesaba mahsup, Ürün için satınalma harcaması hesabıdır. Bu hesap bilançonuzdaki stoğu temsil eder. Kullanılan hesap, genellik satış siparişinde Birimlerin maliyeti, teslim edilen ve Birimlerin maliyeti, faturalanan için kullanılan hesapla aynıdır. |
| Ürün için satınalma harcaması | 600180 | Malzeme girişi | Gider | Kredi | Evet | C  | |Bir satınalma siparişi faturası deftere nakledildiğinde kullanılır. Standart maliyet kullanıldığında satınalma fiyatı farklarını takip etmek üzere fatura için iki fiş oluşturulur. Bu hesaba mahsup, giriş deftere naklinde kullanılan ve fatura deftere nakli sırasında tersine çevrilen faturalanmayan Satınalma harcaması hesabıdır. Faturalama sırasında satın alınan ve bilançodaki stok hesabına yansıtılmayan stok maliyetlerini temsil eder. Bu, standart maliyet maddesi satınalma işlemlerinde sıklıkla görülen satınalma fiyatı farkı için kâr ve zarar deftere naklidir.|
| Sabit giriş fiyatı karı (Satınalma, sabit giriş fiyatı karı*) | 510310 | Satın alma fiyat farkı | Gider | Kredi | No. | C | Sabit giriş fiyatı zararı | Bir satınalma siparişi faturası deftere nakledildiğinde ve maddenin faturalanan fiyatıyla varsayılan maliyeti arasında fark olduğunda kullanılır. Fark daha yüksek olduğunda bu hesap kullanılır. Bu hesaba mahsup, Sabit giriş fiyatı mahsup işlemidir. |
| Sabit giriş fiyatı zararı (Satınalma, sabit giriş fiyatı zararı*) | 510310 | Satın alma fiyat farkı | Gider | Borç | No. | C | Sabit giriş fiyatı karı | Bir satınalma siparişi faturası deftere nakledildiğinde ve maddenin faturalanan fiyatıyla varsayılan maliyeti arasında fark olduğunda kullanılır. Fark daha düşük olduğunda bu hesap kullanılır. Bu hesaba mahsup, Sabit giriş fiyatı mahsup işlemidir. |
| Sabit giriş fiyatı mahsup işlemi (Satınalma, sabit giriş fiyatı mahsup işlemi*) | 140900 | Stok değişimi | Varlık | İkisi birden | No. | C  | |Bir satınalma siparişi faturası deftere nakledildiğinde ve maddenin faturalanan fiyatıyla varsayılan maliyeti arasında fark olduğunda kullanılır. Bu hesap, Sabit giriş fiyatı kar ve zarar hesaplarının mahsup hesabıdır. |
| Ücret | Yok | Yok | Yok | Yok | Yok | Yok | Yok | Bu hesap artık kullanılmamaktadır. Bunun yerine Stok varyasyonunu kullanın. |
| Stok değişimi | 600170 | Stok değişimi | Gider | Kredi | No. | İkisi birden | | Bu hesap şu durumlarda kullanılır: <ul><li>Ürün girişi ve fatura arasındaki birim fiyatlarda fark vardır.</li><li>Masraflar maddeye nakledilir.</li><li>Dolaylı maliyetler<!--note from editor: Edit okay?--> satın alınan maddelere eklenmiştir. </li><li>Bu hesaba mahsup, Faturalanmamış satınalma harcaması hesabıdır.</li></ul> |
| Satınalma, tahakkuk | 200140 | Tahakkuk Eden Satın Almalar | Pasif | Kredi | Y | P | |Bir satınalma siparişi ürün girişi nakledildiğinde ve satınalma tutarlarını tahakkuk ettir seçeneği etkin olduğunda kullanılır. |
| Girişte tahakkuk eden satış vergisi | 250500 | Tahakkuk Eden Satış Vergisi | Pasif | Kredi | Y | İkisi birden  | |Bu hesap, **Stok ve ambar yönetim parametreleri**'nde **Fiziksel vergisi deftere naklet** seçeneğini belirlediğinizde ve vergi içeren bir satınalma siparişiniz olduğunda kullanılır. Satınalma siparişini fiziksel olarak (ürün girişi) güncelleştirdiğinizde tutar nakledilir, satınalma siparişini mali olarak (fatura)deftere naklettiğinizde ters işlem uygulanır. |
| Sabit kıymet girişi (Sabit kıymet borcu *) | 180100 | Maddi sabit kıymetler | Varlık | Borç | N | İkisi birden | İkisi birden | Bu hesap, Sabit kıymetler için satınalma siparişi satırında ilgili seçeneği belirlediğinizde kullanılır. Satınalma siparişi tümleştirmesi, ürün girişi veya faturasının ardından sabit kıymeti alacak şekilde yapılandırılmıştır. Sabit kıymet satın alma siparişi tümleştirmesi hakkında daha fazla bilgi için [Kıymetleri tedarik yoluyla alma](/fixed-assets/acquire-assets-procurement) konusuna gidin. |
| Gider için satınalma harcaması | 618900 | Sair gider | Gider | Borç | N | İkisi birden | |Maddelerin stoğunun tutulmadığı ve tedarik kategorisinin kullanıldığı bir satınalma siparişi için ürün girişi veya faturayı deftere naklederken kullanılır. |
| Ön ödeme | 132190 | Peşin ödenmiş gider | Varlık | Borç | N | İkisi birden | | Satınalma siparişinde bir ön ödeme faturası işlenirken kullanılır. |


\*Parantez içinde gösterilen değerler, **Fiş hareketleri** sayfasındaki **Deftere nakil türü** alanında kullanılan değeri temsil eder. **Deftere nakil türü**'nü, **Fiş hareketleri** sayfasının **Genel** sekmesinde görüntüleyebilirsiniz.

## <a name="fixed-asset-posting-with-purchase-orders"></a>Satınalma siparişleriyle sabit kıymeti deftere nakletme

**Sabit kıymetler** modülünü kullanıyor ve satınalma siparişleri aracılığıyla sabit kıymet satın almayı planlıyorsanız, **Stok deftere nakil profili** sayfasının **Satınalma siparişi** sekmesindeki **Sabit kıymet girişi** deftere nakil türünü yapılandırmanız gerekir. Daha fazla bilgi için [Sabit kıymetler tümleştirmesi](/fixed-assets/fixed-asset-integration.md) ve [Borç hesaplarından kıymetler oluşturma ve alma](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md) konularına bakın.

## <a name="prepayment-purchase-order-invoice-posting"></a>Ön ödemeli satın alma siparişi faturasını deftere nakletme

Satınalma siparişleri için **Ön ödeme faturası** özelliğini kullanmayı planlıyorsanız, **Stok deftere nakil profili** sayfasının **Satınalma siparişi** sekmesinde **Ön ödeme** deftere nakil türü seçilmelidir. Daha fazla bilgi için [Ön ödeme faturaları ve ön ödemeler karşılaştırması](/accounts-payable/prepayments-invoices-vs-prepayments.md) konusuna gidin.

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>Satınalma talebi ve satınalma sipariş onayını deftere nakletme

Satınalma talepleri ve satınalma siparişi onayları, genel muhasebe defterine ön yükümlülükler ve yükümlülükler nakletmek için de yapılandırılabilir. Bu deftere nakiller, deftere nakil tanımı tarafından denetlenir. Daha fazla bilgi için [Satınalma siparişi yükümlülükleri hakkında](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances) konusuna gidin.

## <a name="procurement-category-posting"></a>Tedarik kategorisini deftere nakletme

Stok deftere naklini tüm maddeler, bir madde grubu veya tek bir madde için ayarlamaya alternatif olarak, kategorileri ayarlayabilir ve tedarik kategorilerine göre genel muhasebe defterine naklini denetleyebilirsiniz. Kategorileri ayarlama ve bunları ürünlere atama hakkında daha fazla bilgi için bu makalenin önceki kısımlarında yer alan [Örnek deftere nakil profili yapılandırması](#sample-posting-profile-configuration) bölümüne gidin.

Satınalma siparişleri veya satıcı faturalarıyla kategorileri kullanırken, kategori hiyerarşisinin **Kategori hiyerarşisi rol atamaları** sayfasında **Tedarik kategorisi hiyerarşisi** türüne atanması gerekir.

### <a name="vendor-invoices-with-procurement-categories"></a>Tedarik kategorileri içeren satıcı faturaları

Kuruluşunuz, satınalma siparişlerini belirli satın alma işlemlerinde kullanıyor belirli işlemlerde kullanmıyorsa satınalma siparişiyle ilişkili olmayan faturaları çeşitli yöntemlerle işleyebilirsiniz. Buna, **Borç hesaplarında** günlükleri kullanmak veya satınalma siparişleri için fatura oluşturmak amacıyla kullanılan **Bekleyen satıcı faturaları** sayfası dahildir. Satınalma siparişiyle ilişkili olmayan faturalar oluştururken her gider türü için tedarik kategorileri oluşturmanız gerekir. Kategoriyi **Stok deftere nakil profilleri** sayfasındaki doğru gider hesabıyla eşleştirmeniz gerekir.

Tam kategori sayısı, faturalarınızı deftere nakletmek için kullandığınız gider hesaplarının sayısına göre değişir. Satınalma siparişiyle ilişkili olmayan faturaları giderleştirdiğiniz her ana hesap için en az bir tedarik kategorisi gereklidir. Tek bir ana hesap için birçok kategori kullanılabilir. Bu, kullanışlılık, kolay arama ve kullandığınız masraf türlerini raporlama açısından yararlı olabilir.

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>Satıcı faturaları için tedarik kategorilerini kullanmanın yararları

Satıcı faturaları için tedarik kategorilerini kullanmanın yararlarından bazıları şunlardır:

- Tutarlı kullanıcı deneyimi: Satınalma siparişiyle ilişkili olmayan giderler için tedarik kategorileri yapılandırdığınızda kullanıcılar, **Bekleyen satıcı faturaları** sayfasını kullanarak faturalandırma için tek bir işlemle ilgili eğitim alır.
- İyileştirilmiş raporlama deneyimi: Tüm maddeler ve satınalma siparişiyle ilişkili olmayan tüm giderler için tedarik kategorileri yapılandırdığınızda, tedarik harcamaları raporu harcamaları satıcı, kategori ve diğer ölçütlere göre analiz eder.
- Tutarlı iş akışı: Tüm faturaları işlemek için **Bekleyen satıcı faturaları**'nı kullandığınızda, tek bir iş akışı kullanarak tutarlı bir iş akışı ve onay işlemi oluşturabilirsiniz.

## <a name="consignment-inventory-posting"></a>Konsinye stoğu deftere nakletme

Konsinye stok, diğer satın alınan maddelerle aynı genel muhasebe defterine nakil işlemini kullanır. Başlıca fark, stok alındığında genel muhasebe hareketlerinin kaydedilmemesidir. **Stok sahipliği değişikliği** günlüğü nakledildiğinde sahipliği kuruluşa aktarmak için, maddenin maliyetini kaydetmek üzere bir fiş oluşturulur. Daha fazla bilgi için [Konsinye ayarlama](/supply-chain/inventory/consignment.md) konusuna gidin.
