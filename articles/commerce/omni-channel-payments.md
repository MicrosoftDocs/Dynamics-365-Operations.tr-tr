---
title: Çoklu kanal ödemeleri genel bakışı
description: Bu makale, Dynamics 365 Commerce Omni-Channel ödemelerinin genel görünümünü sağlar.
author: BrianShook
ms.date: 09/17/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom:
- "141393"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 8.1.3
ms.openlocfilehash: d850e532a764d22bc926f5649f4ad2907b49d1a0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881721"
---
# <a name="omni-channel-payments-overview"></a>Çoklu kanal ödemeleri genel bakışı

[!include [banner](../includes/banner.md)]

Bu makale, Dynamics 365 Commerce Omni-Channel ödemelerinin genel görünümünü sağlar. Desteklenen senaryoların kapsamlı bir listesini, işlevleri, kurulumu ve sorun giderme bilgilerini ve bazı tipik sorunların açıklamalarını içerir.

## <a name="key-terms"></a>Önemli terimler

| Vade | Tanım |
|---|---|
| Belirteç | Ödeme işlemcisinin referans olarak sağladığı bir veri dizesi. Belirteçler, ödeme kartı numaralarını, ödeme yetkilerini ve önceki ödeme yakalamalarını temsil edebilir. Belirteçler, önemli verilerin satış noktasından (POS) oluşan sistemden dışarı kalmasına yardımcı olacağından önemlidir. Bunlar bazen *başvurular* olarak da adlandırılır. |
| Kart belirteci | Bir ödeme işlemcisinin, POS sistemindeki depolama için sağladığı belirteç. Bir kart belirteci yalnızca bunu alan satıcı tarafından kullanılabilir. Kart belirteçleri bazen *kart başvuruları* olarak da adlandırılır. |
| Yetkilendirme (auth) belirteci | Bir ödeme işleminin, POS sistemi bir yetkilendirme isteği yaptıktan sonra bir POS sistemine gönderdiği yanıtın parçası olarak sağladığı benzersiz kod. Daha sonra, işlemci çağrıldığında yetkilendirmeyi ters çevirme veya geçersiz kılma gibi eylemleri gerçekleştirecek şekilde çağrılırsa bir yetkilendirme belirteci kullanılabilir. Ancak, genellikle bir sipariş yerine getirildiyse veya bir hareket sonlandırıldığında fonların yakalanması için kullanılır. Yetkilendirme belirteçleri bazen *Yetkilendirme başvuruları* olarak da adlandırılır. |
| Yakalama belirteci | Bir ödeme sonlandırıldığında veya yakalandıktan sonra bir POS sistemi için ödeme işlemcisinin sağladığı referans. Böylece, yakalama belirteci sonraki operasyonlardaki ödeme yakalamaya (iade istekleri gibi) başvuruda bulunmak için kullanılabilir. | 
| Kart mevcut değil | Fiziksel bir kartın sunulmadığı ödeme hareketlerine belirten bir terimdir. Örneğin, bu hareketler e-ticaret veya çağrı merkezi senaryolarında ortaya çıkabilir. Bu hareketler için ödeme ile ilgili bilgiler bir e-ticaret web sitesine, bir arama merkezi akışına veya POS veya ödeme terminali üzerine el ile girilir. |
| Kart mevcut | Fiziksel bir kartın sunulduğu ve Microsoft Dynamics 365 POS sistemine bağlanan bir ödeme terminalinde kullanıldığı ödeme hareketlerine başvuran bir terim. |

## <a name="overview"></a>Genel bakış

Genel olarak, *omni-kanal ödemeleri* terimi bir kanalda bir sipariş oluşturma ve bunu başka bir kanalda yerine getirebilme olanağını açıklamaktadır. Omni-Channel ödeme desteği arasında ödeme ayrıntıları geri kalan sipariş ayrıntılarının ile birlikte korunur ve sipariş tekrar çekilir veya başka bir kanalda işlenirken bu ödeme detayları kullanılır. Klasik örnek, "Çevrimiçi satın al, mağazada teslim al" senaryosudur. Bu senaryoda, sipariş çevrimiçi oluşturulduğunda ödeme ayrıntıları eklenir. Bunlar, daha sonra POS'ta, malzeme çekme sırasında müşterinin ödeme kartının borçlandırılabilmesi için geri çekilir. 

Bu makalede açıklanan tüm senaryolar Commerce ile birlikte sağlanan standart ödeme yazılımı geliştirme seti (SDK) kullanılarak uygulanabilir. [Dynamics 365 Payment Connector for Adyen](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3), burada tanımlanan her senaryo için kullanıma hazır uygulama sağlar. 

### <a name="prerequisites"></a>Ön Koşullar

Bu makalede anlatılan her senaryo, Omni-channel ödemelerini destekleyen bir ödeme bağlayıcısı gerektirir. Kullanıma hazır Adyen bağlayıcısı da kullanılabilir çünkü Ödemeler SDK'sı ile sağlanan senaryoları desteklemektedir. Ödeme bağlayıcılarının nasıl uygulanacağı ve genel olarak Retail SDK hakkında daha fazla bilgi için, [Perakende BT profesyonelleri ve geliştiricileri ana sayfasını](/dynamics365/unified-operations/retail/dev-itpro/dev-retail-home-page#payment-connectors) ziyaret edin.

#### <a name="supported-versions"></a>Desteklenen sürümler

Bu makalede açıklanan Omni-channel ödeme özellikleri Microsoft Dynamics 365 for Retail 8.1.3 sürümünün bir parçası olarak yayımlanmıştır. 

#### <a name="card-present-and-card-not-present-connectors"></a>"Kart mevcut" ve "kart mevcut değil" bağlayıcıları

Ödemeler SDK'sı, ödemeler için iki uygulama programlama arabirimi (API) kümesine dayanır. İlk API kümesi **iPaymentProcessor** olarak adlandırılır. Çağrı merkezlerinde ve Microsoft Dynamics e-ticaret platformlarında kullanılabilen "kart yok" ödeme bağlayıcıları uygulamak için kullanılır. **iPaymentProcessor** arabirimi hakkında daha fazla bilgi için bkz. [Bir ödeme bağlayıcısı ve bir ödeme cihazı uygula](https://download.microsoft.com/download/e/2/7/e2735c65-1e66-4b8d-8a3c-e6ef3a319137/The%20Guide%20to%20Implementing%20Payment%20Connector%20and%20Payment%20Device_update.pdf) teknik incelemesine bakın, bu ödemeleri de kapsamaktadır. 

İkinci API kümesi **iNamedRequestHandler** olarak adlandırılır. Ödeme terminali kullanan "kart mevcut" ödeme tümleştirmelerini destekler. **iNamedRequestHandler** arabirimi hakkında daha fazla bilgi için, bkz [Bir ödeme terminali için bir ödeme tümleştirmesi oluşturma](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension). 

### <a name="setup-and-configuration"></a>Kurulum ve yapılandırma

Aşağıdaki bileşenler ve kurulum adımları gereklidir:

- **eCommerce entegrasyonu:** bir siparişin çevrimiçi mağazada bulunduğu senaryoları desteklemek için bir Commerce ile bütünleşme gereklidir. Perakende e-ticaret SDK hakkında daha fazla bilgi için, bkz [e-ticaret platformu yazılım geliştirme kiti (SDK)](/dynamics365/unified-operations/retail/dev-itpro/ecommerce-platform-sdk). Bir demo ortamında, başvuru mağazası, Omni-Channel ödeme senaryolarını desteklemektedir. 
- **Çevrimiçi ödemeler yapılandırması:** çevrimiçi kanalın kurulumu, Omni-Channel ödemelerini desteklemek için güncelleştirilmiş bir ödeme bağlayıcısı içermelidir. Alternatif olarak, kutu dışı ödeme bağlayıcısı kullanılabilir. Adyen ödeme bağlayıcısını çevrimiçi mağazalar için konfigüre etme hakkında bilgi için, bkz: [Adyen ödeme konnektörü.](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#e-commerce) Bu makalede açıklanan eCommerce Kurulum adımlarının yanı sıra, Adyen Bağlayıcısı ayarlarında **e-ticaret parametresinde ödeme bilgilerinin kaydedilmesine izin ver** parametresi **doğru** olarak ayarlanmalıdır. 
- **Omni-Channel ödemeler konfigürasyonu:** arka ofiste, **Retail ve Commerce \> Merkez kurulumu \> Parametreler \> Commerce paylaşımı parametreleri**. **Omni kanal ödemeleri** sekmesinde, **Omin-channel ödemeleri kullan** seçeneğini **Evet** olarak ayarlayın. Commerce 10.0.12 ve sonraki sürümlerde bu ayar **Özellik Yönetimi** çalışma alanında yer alınır. **Çok yönlü kanal ödemeleri** özelliğini seçin ve **Şimdi etkinleştir**'e tıklayın. 
- **Ödeme hizmetleri:** Çağrı merkezi ödemeleri işlemek için **Ödeme hizmetleri** sayfasındaki varsayılan ödeme bağlayıcısını kullanır. "Arama merkezinde satın al, mağazada teslim al" gibi senaryoları desteklemek için, bu varsayılan ödeme bağlayıcının, bir Adyen ödeme Bağlayıcısı veya Omni-Channel ödemeleri için olan uygulama gereksinimlerini karşılayan bir ödeme bağlayıcısı olması gerekir.
- **EFT servisi:** donanım profilinin **EFT servis** hızlı sekmesinde bir ödeme terminali ile yapılan ödemeler ayarlanmalıdır. Adyen konektörü, kullanıma hazır, Omni-Channel ödemeler senaryolarını destekler. **iNamedRequestHandler** arabirimini destekleyen diğer ödeme bağlayıcıları , Omni-kanal ödemelerini destekliyorsa da kullanılabilir.
- **Ödeme bağlayıcısı kullanılabilirliği:** bir sipariş geri alınırken, sipariş ile birlikte geri çekilmiş ödeme satırları o siparişle ilişkilendirilmiş yetkilendirmeleri oluşturmak için kullanılan ödeme bağlayıcısının adını içerir. Sipariş yerine getirilirse, ödemeler SDK'sı, özgün yetkilendirmeyi oluşturmak için kullanılan aynı bağlayıcıyı kullanmaya çalışır. Bu nedenle, aynı ticari özelliklere sahip bir ödeme bağlayıcının yakalama için kullanılabilir olması gerekir. 
- **Kart tipleri:** Omni-channel senaryolarının doğru çalışması için, her kanalın Omni-Channel için kullanılabilecek ödeme tipleri için aynı kuruluma sahip olması gerekir. Bu kurulum ödeme yöntemi kodları ve kart türü kodları içeriyor. Örneğin, **Kart** ödeme tipi çevrimiçi mağaza kurulumunda **2** koduna sahipse, perakende mağaza kurulumunda aynı kimliğe sahip olmalıdır. Aynı gereksinim kart türü kodları için geçerlidir. Kart numarası **12**, çevrimiçi mağazada **VISA** olarak ayarlanmışsa, perakende mağaza için aynı kod ayarlanmalıdır. 
- Windows veya Android için yerleşik donanım istasyonlu Retail Modern POS -veya-
- iOS veya Cloud POS için bağlı paylaşılan donanım istasyonlu Modern POS. 

### <a name="basic-principle-supporting-omni-channel-payments"></a>Omni-channel ödemelerini destekleyen temel prensibi

Ödeme bağlayıcıları ve ödeme işlemcileri, kart ödemeleriyle ilgili etkileşimleri referans vermek için belirteçleri veya referansları kullanır. Örneğin, ödeme yetkilendirmesi istendiğinde, o yetkilere yönelik bir referans sağlanır. Bu nedenle, karşılama sırasında fonlar yakalandıktan sonra da yetkilendirmeye başvurulabilir. Bu yetkilendirme ticari, ödeme bağlayıcısı ve işlemci için benzersizdir. 

Çevrimiçi olarak oluşturulan bir sipariş mağazadan teslim alınıyorsa, o siparişle ilgili aynı ödeme ayrıntılarının geri çekilmesi ve kullanılması gerekir. Orijinal yetkilere karşı bir ödeme yakalama talebinin bir parçası olarak başlangıçtaki Ayrıntılar sağlandığında, ödeme işlemcisi talebi işleyebilir ve ödemeyi yakalayabilir. 

Çevrimiçi siparişe doğru başvurmak için, aynı işlemciyi destekleyen "kart mevcut değil" ödeme bağlayıcısı da kullanılabilir olmalıdır. Bu şekilde, POS sistemi "kart mevcut" ödemeleri için bir işlemciye sahip olabilir, ancak başka ödeme işlemcileri kullanarak başka kanallarda oluşturulan siparişleri yerine getirebilmesi için, bu bir işlemci bağlayıcılarına da erişim sağlayabilirsiniz. 

## <a name="supported-scenarios"></a>Desteklenen senaryolar

Aşağıdaki Omni-Channel ödeme senaryoları desteklenir:

- Çevrimiçi sipariş et mağazadan teslim al
- Çağrı merkezinde satın al ve mağazadan teslim al
- Mağaza A'dan satın al ve mağazadan B teslim al
- Mağaza A'da satın al, sevkiyat müşterisi

    > [!NOTE]
    > Çağrı merkezinde yapılmış, "Normal" ödeme işleviyle eşlenen ödemeler, POS 'ta sipariş geri çağırıldığında kalan tutara yansıtılacak **Ön ödeme** = **Evet** olarak işaretlenmelidir. "Normal" tipindeki ön ödeme olmayan ödemeler, sipariş POS'ta geri çağırıldığı sırada tanınmaz. 

Bu senaryoların varyasyonları da desteklenmektedir. Örneğin, bir çevrimiçi siparişte hem müşteriye sevk edilecek satırlar, hem de bir mağazada çekilecek satırlar bulunabilir. Tüm sipariş karşılama seçenekleri, Omni-kanal ödemeleri ile desteklenir. 

Aşağıdaki bölümler, her senaryoya ilişkin adımları açıklar ve demo verilerini kullanarak senaryonun nasıl çalıştırılacağını gösterir. 

### <a name="buy-online-pick-up-in-store"></a>Çevrimiçi sipariş et mağazadan teslim al

Başlamadan önce, aşağıdaki önkoşulların karşılandığından emin olmanız gerekir:

- Adyen bağlayıcının konfigüre edildiği bir mağaza referansınız var.
- **Commerce paylaşılan parametreleri** üzerindeki **Omni-channel ödemeleri** seçeneği **Doğru** olarak ayarlanmıştır. Sonraki sürümlerde, bu ayar **Çoklu kanal ödemeleri** özelliğini seçebileceğiniz ve **Şimdi etkinleştir**'e tıklayabileceğiniz **Özellik Yönetimi** çalışma alanına taşınmıştır. 
- Adyen ödeme konektörü Houston POS kaydı için konfigüre edilir.
- Windows veya Android için yerleşik donanım istasyonlu Retail Modern POS -veya-
- iOS veya Cloud POS için bağlı paylaşılan donanım istasyonlu Modern POS. 

Senaryoyu çalıştırmak için şu adımları izleyin.

1. Referans mağazasında, mağaza için teslim için bir sipariş oluşturun. **Houston** mağazasını seçtiğinizden emin olun. 
2. Kullanıma alma adımlarınız arasında ilerleyin ve bir test kredi kartı numarası kullanarak ödeme yapın. Bir test kredi kartı numaralarını, [Adyen test kartı numaraları sayfasında](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description) bulabilirsiniz.
3. Commerce içinde **Siparişleri senkronize et** toplu işini ve **P-001** dağıtım zamanlamasını kullanarak arka ofiste siparişleri oluşturun.
4. POS'ta, mağaza için malzeme çekme ile ilgili siparişleri görmek **Teslim alınacak siparişler** sayfasında, malzeme çekme işlemi yapılacak siparişleri seçin. 
5. Referans mağazasında oluşturulan siparişten bir veya daha fazla satırı seçin ve sonra **Teslim al**'ı seçin.

    Sipariş, arka ofisten alınır. 

6. Sipariş satırı ayrıntıları arka ofisten alındığında ve Omni-Channel için kullanılabilecek bir kart ödemesi algılanırsa, ödeme yöntemi kullanılabilir olduğunda size bildirilir.
7. Referansı, referans storefront girilen kart ayrıntılarını kullanarak tamamlamak için, **kullanılabilir ödeme yöntemini kullan**'ı seçin.

    Sipariş satırları işlem sayfasında yüklenir ve bakiye 0'dır (sıfır). 

8. Çevrimiçi siparişten çekilen ödeme satırını görüntülemek için **Ödemeler** sekmesini seçin. 
9. Hareketi tamamlamak için herhangi bir ödeme yöntemi seçin. 

### <a name="buy-in-call-center-pick-up-in-store"></a>Çağrı merkezinde satın al ve mağazadan teslim al

1. Commerce'de, **Müşteri Hizmetleri** sayfasında, arama çubuğuna Karen **Karen Berg** girin ve **ara**'yı seçin. 
3. Arama sonuçlarında **Karen Berg**'i seçin.
4. Karen **Müşteri Hizmetleri** sayfasına yüklendikten sonra **yeni satış siparişi** seçeneğini belirleyin.
5. Yeni satış siparişi sayfasında, sipariş başlığını görmek için **başlık**'ı seçin. 
6. **Sipariş başlığı** sayfasında, siteyi **Merkezi** olarak ve **Houston** olarak ayarlayın.
7. **Teslim et** sekmesinde, müşteri malzeme çekme için **teslimat modunu** alanını **60** olarak ayarlayın.
8. **Satırları** seçin ve siparişe bir veya daha fazla satır ekleyin. 
9. Sipariş tamamlama akışını girmek için **Tamam**'ı seçin.
10. Ödemeler bölümünde aşağı doğru ilerleyin, **Ekle**'yi seçin ve ödeme yöntemi türünün **kartlar** olarak ayarlandığı bir satır seçin. 
11. Bir kart ödemesi eklemek için artı (**+**) işaretini seçin. 
12. [Adyen test kartı numaraları sayfasında](https://docs.adyen.com/development-resources/test-cards/test-card-numbers/#description) bulduğunuz bir sınama kredi kartı numarası için ayrıntılar girin ve **Tamam**'ı seçin.

    > [!NOTE]
    > Girdiğiniz kart numarası, ödeme başlatıldığı sırada seçilmiş olan markalardan farklıysa, ödeme devam eder. Ancak, 10. adımda seçtiğiniz kart markasının eşlendiği hesaplara nakledilir.

12. Sipariş **ödemeleri tamamla iletişim kutusunu** kapatmak için yeniden **Tamam**'ı seçin.
13. **Satış siparişi özeti** sayfasında, **Gönder**'i seçin.
14. POS'ta, mağaza için malzeme çekme ile ilgili siparişleri görmek **Teslim alınacak siparişler** sayfasında, malzeme çekme işlemi yapılacak siparişleri seçin. 
15. Referans mağazasında oluşturulan siparişten bir veya daha fazla satırı seçin ve sonra **Teslim al**'ı seçin.

    Sipariş, arka ofisten alınır. 

16. Sipariş satırı ayrıntıları arka ofisten alındığında ve Omni-Channel için kullanılabilecek bir kart ödemesi algılanırsa, ödeme yöntemi kullanılabilir olduğunda size bildirilir.
17. Referansı, referans storefront girilen kart ayrıntılarını kullanarak tamamlamak için, **kullanılabilir ödeme yöntemini kullan**'ı seçin.

    Sipariş satırları işlem sayfasında yüklenir ve bakiye 0'dır (sıfır).

18. Çevrimiçi siparişten çekilen ödeme satırını görüntülemek için **Ödemeler** sekmesini seçin. 
19. Hareketi tamamlamak için herhangi bir ödeme yöntemi seçin. 

### <a name="buy-in-store-a-pick-up-in-store-b"></a>Mağaza A'dan satın al ve mağazadan B teslim al

1. POS'un Houston deposunu başlatın.
2. **Hareket** sayfasında, **2001** girmek için sayı panelini kullanarak hareketi harekete bir şekilde ekleyin.
3. Harekete bir veya birden fazla satır ekle.
4. Sipariş seçeneklerini görmek için **Siparişler**'i seçin.
5. **Tümünü çek**'i seçin ve istendiğinde **müşteri siparişi**'ni seçin.
6. Aramaya **Seattle** girin ve malzeme çekme için **Seattle** deposunu seçin. 
7. Malzeme çekme tarihi olarak geçerli tarihi kabul etmek için **Tamam**'ı seçin.
9. Ödemeyi başlatmak için **Ödeme kartı**'nı seçin.
10. Kart ödemesini, ödem için gerekli olan tutar için yapın. 
11. Ödeme terminalinde havale ödemesini tamamlayın. 
12. Depozito ödendikten sonra, karşılama için aynı kartı kullanma seçeneğini belirleyin ve siparişin tamamlanmasını bekleyin. 
13. POS'un Seattle deposunu başlatın.
14. POS'ta, mağaza için malzeme çekme ile ilgili siparişleri görmek **Teslim alınacak siparişler** sayfasında, malzeme çekme işlemi yapılacak siparişleri seçin. 
15. Referans mağazasında oluşturulan siparişten bir veya daha fazla satırı seçin ve sonra **Teslim al**'ı seçin.

    Sipariş, arka ofisten alınır. 

16. Sipariş satırı ayrıntıları arka ofisten alındığında ve Omni-Channel için kullanılabilecek bir kart ödemesi algılanırsa, ödeme yöntemi kullanılabilir olduğunda size bildirilir.
17. Referansı, referans storefront girilen kart ayrıntılarını kullanarak tamamlamak için, **kullanılabilir ödeme yöntemini kullan**'ı seçin.

    Sipariş satırları işlem sayfasında yüklenir ve bakiye 0'dır (sıfır).

18. Çevrimiçi siparişten çekilen ödeme satırını görüntülemek için **Ödemeler** sekmesini seçin. 
19. Hareketi tamamlamak için herhangi bir ödeme yöntemi seçin. 

### <a name="buy-in-store-a-ship-to-customer"></a>Mağaza A'da satın al, sevkiyat müşterisi

1. POS'un Houston deposunu başlatın.
2. **Hareket** sayfasında, **2001** girmek için sayı panelini kullanarak hareketi harekete bir şekilde ekleyin.
3. Harekete bir veya birden fazla satır ekle.
4. Sipariş seçeneklerini görmek için **Siparişler**'i seçin.
5. **Tümünü sevk et**'i seçin ve istendiğinde **Müşteri siparişi**'ni seçin.
6. Sevkiyat yöntemi sayfasında, **Standart ertesi gün** ögesini seçin ve sevkiyat tarihi olarak bugünün tarihini kabul etmek için **Tamam**'ı seçin. 
7. Malzeme çekme tarihi olarak geçerli tarihi kabul etmek için **Tamam**'ı seçin.
8. Ödemeyi başlatmak için **Ödeme kartı**'nı seçin.
9. Kart ödemesini, ödem için gerekli olan tutar için yapın. 
10. Ödeme terminalinde havale ödemesini tamamlayın. 
11. Depozito ödendikten sonra, karşılama için aynı kartı kullanma seçeneğini belirleyin ve siparişin tamamlanmasını bekleyin.

Sipariş arka ofis içinde çekildiğinde, paketlenebiliyorsa ve faturalandığı zaman, POS 'ta sağlanan ödeme detayları müşteriye sevk edilen malların fonlarının yakalanması için kullanılacaktır. 

## <a name="scenario-details"></a>Senaryo ayrıntıları

Yalnızca açıklanan temel senaryolara ek olarak, çoklu kanal ödemelerini destekleyen ödemeler SDK'sında çeşitli geliştirmeler yapılmıştır. 

### <a name="pos"></a>POS

#### <a name="single-swipedip-for-customer-orders"></a>Müşteri siparişleri için tek çekme/dip

Omni-Channel ödemeler özelliği uygulanmadan önce, müşteri siparişleri dahil edilen havalelerin POS'ta oluşturulduğu sırada müşteriler, kartını iki kez alacak (veya dip) yapması gerekiyordu: depozito ve bir kez kartı izleyen sipariş karşılama. Omni-Channel tokenleştirme özelliği açık olduğunda, müşteriler depozito ödemek ve daha sonra yerine getirilecektir olan malların vadesi gelmiş olduğu tutarı yetkilendirmek için kartlarını yalnızca bir kez alacak şekilde çek etmelidir. Karşılama sırasında, yetkili fonlar yakalanır. Omni-Channel belirteç seçme özelliği uygulanmadan önce, sonraki sipariş karşılama için yalnızca bir yinelenen kart belirteci oluşturuldu. Bu nedenle, bekleyen karşılama için fonlar yetkilendirilmemiştir ve fonların söz konusu satın alma işlemi için tutulmadığından, daha sonra yakalanmaları ihtimali daha düşük olacaktır.

> [!NOTE]
> Retail sürüm 8.1.3 tek çekme desteklenmez. 8.1.3 sürümündeki müşteri siparişleri, Omni-Channel tokenleştirme özelliği uygulanmadan önce kullanılan akışı kullanır. 

### <a name="cards-that-cant-issue-recurring-card-tokens"></a>Yinelenen kart belirteçleri veremeyen kartlar

Bazı kartlar, Omni-channel ödemeler için kullanılamaz, çünkü bunlar yinelenen kart belirteçleri vermeyi desteklemezler. POS'ta bir sipariş oluşturulduğunda, depozito yinelenen kart belirteçlerini desteklemeyen bir kart kullanılarak ödeniyorsa, önceki kart tokenleştirme akışı kullanılır. Bu nedenle, sonraki sipariş karşılama için kullanılacak bir ödeme sağlamak isteyen bir müşterinin ikinci bir kart sunması gerekir. İkinci kart tekrarlanan kart belirteçlerini desteklemiyorsa, tokenleştirme eylemi reddedilir ve müşterinin kasiyere farklı bir kart vermesini istenir. 

### <a name="using-a-different-card"></a>Farklı bir kart kullanma

Sipariş malzeme çekme için mağazaya gelen bir müşteri farklı bir kart kullanma seçeneğine sahiptir. Kasiyer sipariş alma sırasında **Kullanılabilir ödeme yöntemini** kullan istemini aldığında, kasiyer müşterinin aynı kartı kullanmak isteyip istemediğini sorabilir. Müşteri siparişi oluşturmak için kullanılan kartı kaybetmesi durumunda ve farklı bir kart kullanarak sipariş için ödeme yapmak istiyorsa, kasiyer **farklı bir ödeme yöntemi** kullan seçeneğini belirleyebilirsiniz. Müşteri daha sonra aynı sipariş için daha fazla madde çekmek üzere geri gelirse, orijinal kart yetkilendirmesi hala geçerliyse, kasiyer müşterinin o kartı kullanmak isteyip istemediğini da sorabilir.

### <a name="invalid-authorizations"></a>Geçersiz yetkilendirmeler

Sipariş oluşturmak için kullanılan kart artık geçerli değilse, malzeme çekme için seçildiğinde ödeme yakalama talebi başarısız olur. POS ödeme bağlayıcısı, aynı kart ayrıntılarını kullanarak yeni bir yetkilendirme oluşturmaya ve yakalamayı deneyecek. Yeni yetkilendirme veya yakalama başarısız olursa, kasiyer ödemenin işlenmediği konusunda bilgilendirilirler. Kasiyerin bundan sonra müşteriden yeni bir ödeme alması gerekir. 

### <a name="multiple-available-payments"></a>Çoklu kullanılabilir ödeme

Birden çok ilgili ve birden çok satırı bulunan bir sipariş çekildiğinde, kasiyer önce **Kullanılabilir ödeme yöntemini kullan** istemini alır. Birden fazla kart varsa, kasiyer **kullanılabilir ödeme yöntemini kullan** seçtiğinde, mevcut kart ödeme satırları, şu anda çekilmiş mallar için bakiye karşılanana kadar yakalanır. Kasiyerin, çekilmiş mallar için kullanılması gereken kartı seçme seçeneği yoktur. 

## <a name="related-articles"></a>İlgili makaleler

- [Ödemeler ile ilgili SSS](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)
- [Adyen için Dynamics 365 Ödeme Bağlayıcısı](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3)
- [Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma](./cpe-bopis.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]