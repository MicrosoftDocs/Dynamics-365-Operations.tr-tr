---
title: Mağazalar için sipariş karşılamayı ayarlama
description: Bu konu, Mağaza sipariş karşılamanın nasıl ayarlanacağı konusuna genel bir bakış sağlar.
author: rubencdelgado
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: rubencdelgado
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 65a6e1c3e361870dde71bb4f848867b7e5e296d1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024274"
---
# <a name="set-up-order-fulfillment-for-stores"></a>Mağazalar için sipariş karşılamayı ayarlama

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Özet

Birçok satıcı, mağazaların siparişleri karşılamasını sağlayarak sipariş karşılama yeteneğini en iyi duruma getirmek istemektedir. Mağaza seviyesinde sipariş karşılama belirli bir mağazayla ilgili aşırı stok senaryolarını kolay hale getirmeye yardımcı olabilir ve bir mağazanın ekstra kapasitesi olması veya müşteriye daha yakın bir sevkiyat mesafesinde yer alması durumunda lojistik açıdan gerekli olabilir. Bu ihtiyacı karşılamak için, satış noktasında birleştirilmiş sipariş karşılama işlemi bulunmaktadır.

Belirli bir mağaza tarafından karşılanması gereken siparişlerde siparişin başlığında veya satırlarında atanan mağazanın deposu yer alır.

Satış noktasındaki sipariş karşılama işlemi, satış noktasında siparişleri işlemek için kullanılabilecek tek bir çalışma alanı sağlar. Bu siparişin kabul edilmesinden sevk edildi olarak işaretlenmesine veya mağazadan çekme işleminin başlatılmasına kadar tüm aşamaları içerir.

## <a name="set-up-the-order-fulfillment-operation"></a>Sipariş karşılama işlemini ayarlama

Siparişin karşılama, [928 işlem kodu](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-operations), satış noktasında mağaza sipariş karşılama çalışma alanına erişmek için kullanılabilir.

Satış noktasında sipariş karşılamayı çağırmak için hangi parametrenin kullanılacağını belirlemek üzere [Düğme grubuna bir işlem ekleme](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-screen-layouts) bölümündeki adımları izleyin. Varsayılan olarak sipariş karşılama işlemleri belirtildikten sonra **Tüm siparişler** seçeneği seçilir. Bu parametre ile yapılandırıldığında, işlem geçerli mağazadaki karşılanacak tüm sipariş satırlarını listeler. Ayrıca, bir düğmeye atanıp yalnızca kullanıcı mağazadan sev edilecek siparişleri görmek istediği zaman kullanılabilecek **Sevk edilecek siparişler** seçeneği de bulunmaktadır. Son olarak **Çekilecek siparişler** seçeneği bulunur. Satış noktasında çağrıldığında, yalnızca mağazadan çekilecek olan siparişleri listeler. Farklı parametreler, kullanıcıya sipariş karşılamanın farklı yollarını sağlamak üzere farklı düğmelere atanabilir.

### <a name="enable-users-to-access-order-fulfillment-at-the-point-of-sale"></a>Kullanıcıların satış noktasında sipariş karşılamaya erişmesine olanak tanır

Sipariş karşılama işleminin kullanıma hazır kendi izni bulunmamaktadır ancak kullanıcıların gelecekte işlemi satış noktasından çağırmak için **Sipariş almaya izin ver** iznini kullanması gerekli olabilir.

Mağaza seviyesinde, bir sipariş satırının satış noktası içinden el ile kabul edilip edilmemesi gerektiğini belirlemek için kullanılan bir yapılandırma ayarı bulunur. Bu yapılandırma seçeneği ayarlanmazsa, sipariş satırları varsayılan olarak kabul edilir. Bu yapılandırma seçeneği etkinleştirilse, satış noktasındaki kullanıcıların siparişleri satış noktası içinden kabul etmek için **Siparişi kabul etmeye izin ver** iznine sahip olması gerekir.

### <a name="enable-manual-order-acceptance"></a>El ile sipariş kabulünü etkinleştirme

Varsayılan olarak, bir mağazaya atanan sipariş satırları **Kabul edildi** olarak işaretlenir. Bu, siparişlerin atandıkları mağaza tarafından karşılanacaklarının ve başka bir atama olmayacağının varsayıldığı anlamına gelir. Belirli durumlarda, perakendeciler karşılanmadan önce siparişleri el ile kabul etmek isteyebilir. Örneğin, mağazada personel sayısı kısıtlıysa ve mağaza siparişi karşılayamayacaksa, mağaza yöneticisi yalnızca belirtilen tarihte uygun şekilde işleme alınabileceğini düşündüğü sayıdaki siparişi işlemek üzere kabul edebilir. Sipariş kabul edilinceye kadar, arka ofis tarafından farklı bir mağazaya atanabilir. Bu şekilde, sipariş kabulü de bir siparişin bir mağaza tarafından onaylandığını ve karşılanacağını belirtmek üzere kullanılabilir.

Mağazadan çekilecek sipariş satırları **Beklemede** olarak işaretlenir ve kabul etme işlemine tabi değildir.

Sipariş satırları için el ile kabul etmeyi açmak için **Perakende ve Ticaret** \> **Kanallar** \> **Mağazalar** \> **Tüm perakende mağazalar**'a gidin. Mağazayı seçin ve mağaza ayrıntılarını görmek için mağaza koduna tıklayın. **Düzenle**'yi tıklatın. **Genel** hızlı sekmesinde **Sipariş karşılama** alt başlığını bulun ve **El ile kabul et** seçeneğini **Hayır** yerine **Evet** olarak ayarlayın.

### <a name="enable-reject-order-line-capability"></a>Sipariş satırını reddet özelliğini etkinleştirme

Ayrıca sipariş satırları satış noktasından reddedilebilir. Bir sipariş satırının reddedilmesi, bu satırın mağazada karşılanmayacağı anlamına gelir ve satış satırı başka bir mağazaya veya ambara atanmak üzere geri gönderilir. Sipariş satırını reddetme izni çalışanla ilişkili POS izin grubundaki **Siparişi reddetmeye izin ver** izniyle sağlanır. Perakendeciler bir satırı reddederken çalışanlarının reddetmeyle ilgili bir açıklama girmesini zorunlu kılabilir. Bu, **Siparişin karşılama** türündeki **Bilgi kodu etkinliği** bilgi kodları kullanılarak ve bilgi kodu kanalla ilişkilendirilen işlev profilindeki **Sipariş satırını reddet**'e atanarak gerçekleştirilebilir.

> [!NOTE]
> Yalnızca **Sipariş karşılama** türündeki **Bilgi kodu etkinliği** bilgi kodları **Sipariş satırını reddet** eylemine atanabilir.

### <a name="synchronize-changes-to-the-channel-database"></a>Değişiklikleri kanal veritabanıyla eşleştirme

İşlem bir düğme grubuna atandıktan sonra, ilgili izinler atanıp kanal yapılandırılır. Değişikliklerin kanal veritabanıyla eşitlenmesi gerekir. Bunu yapmak için, **Retail ve Commerce** \> **Retail ve Commerce BT** \> **Dağıtım planı**'na gidin. Düğme grubu değişikliklerini eşitlemek için "1090-Kayıtlar" planını seçin ve ardından **Şimdi çalıştır**'a tıklayın. Daha sonra "1060-Personel"i seçerek izin değişikliklerini eşitleyin ve ardından **Şimdi çalıştır**'a tıklayın. Daha sonra "1070-Kanal yapılandırması"nı seçerek kanal değişikliklerini eşitleyin ve ardından **Şimdi çalıştır**'a tıklayın. Son olarak, reddetme nedeni için yeni oluşturulan bilgi kodunu "1110-Genel yapılandırma"yı seçerek eşitleyin ve **Şimdi çalıştır**'a tıklayın.

## <a name="use-order-fulfillment-at-the-point-of-sale"></a>Satış noktasında sipariş karşılamayı kullanma

Satış noktasını açın ve sipariş karşılama işlemini seçin. Nasıl yapılandırıldığına bağlı olarak tüm satırlar, malzeme çekme için sipariş satırları veya sev edilecek sipariş satırları listede görüntülenir.

### <a name="order-fulfillment-view"></a>Sipariş karşılama görünümü

Sipariş karşılama görünümü, mağazada karşılanacak sipariş satırlarını listeler ve aşağıdaki sütunları içerir:

- Sipariş numarası
- Ürün numarası
- Tanım
- Sipariş edilen miktar
- İstenen teslim tarihi
- Müşteri adı
- Karşılama durumu

Belirli bir sipariş satırıyla ilgili ek bilgiler sipariş satırı seçilip satış noktası başlığında gösterilen oturum açan kullanıcı/vardiya bilgisinin hemen altında bulunan açılır menü açılarak görüntülenebilir. Bu menüde 2 sekme vardır: biri satır ayrıntılarıyla, diğeri sipariş ayrıntılarıyla ilgilidir. Satır ayrıntıları sekmesi aşağıdaki bilgileri içerir:

- Sipariş edilen miktar
- Sevk edilecek/çekilecek kalan miktar
- Çekilen miktar
- Paketlenen miktar
- Faturalanan miktar (zaten çekilen ya da sevk edilen)
- Teslimat şekli
- Teslimat adresi

Ayrıntılar açılır menüsünde ayrıca aşağıdakiler dahil sipariş düzeyinde daha fazla ayrıntı sağlayan bir sekme bulunur:

- Müşteri adı
- Müşteri kodu
- Sipariş numarası
- Sipariş toplamı
- Sipariş bakiyesi

Sipariş karşılama görünümünün altında bir Eylem Bölmesi bulunur. Bu bölme, bir sipariş satırıyla ilgili gerçekleştirilebilecek tüm eylemleri içerir. Bir satırın durumuna bağlı olarak bir eylem kullanılamıyorsa, bu eylem kullanılamaz durumda olur.

Varsayılan olarak, siparişlerin durumu **Kabul edildi** olur. Sipariş durumu sipariş satırları listesinde bir sütun olarak görüntülenebilir. Kanal düzeyinde **El ile kabul** yapılandırılmışsa, sevk edilecek tüm satırlar **Beklemede** olarak gösterilir ve bunların karşılanmadan önce kabul edilmesi gerekir. Mağazadan çekilecek siparişler varsayılan olarak **Beklemede** durumundadır ve kabul edilmeleri gerekmez.

### <a name="order-fulfillment-line-actions"></a>Sipariş karşılama satırı eylemleri

- **Düzenle** – durumu Beklemede olduğunda, satış noktasında düzenlenebilir. Zaten kısmen çekilmiş, paketlenmiş veya faturalanmış olan siparişler sipariş karşılama görünümünden düzenlenemez.
- **Kabul et** – **El ile kabul et** kanal düzeyinde yapılandırılmışsa, satırların sipariş karşılama işlemine geçebilmesi için öncelikle kabul edilmesi gerekir.
- **Çek** – Çekme seçeneği birçok eylemi destekler. Öncelikle, **Çekme** sipariş satırının durumunu güncelleştirir, böylece mağazadaki diğer kişiler aynı satır için çekme işlemi gerçekleştirmeye çalışmaz. Ardından, **Malzeme çekme listesini yazdır** seçeneği seçilen satır veya satırlar için malzeme çekme listesini yazdırır ve durumlarını **Çekme** olarak güncelleştirir. Malzeme çekme listesi biçimleri makbuz biçimlerinin bir parçası olarak denetlenir. Makbuz biçimleri ayarlama hakkında daha fazla bilgi için bkz. [Makbuz şablonları ve yazdırma](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing). Son olarak, **Çekildi olarak işaretle** satırı çekilmiş gösterir. **Çekildi olarak işaretle**, arka ofiste ilgili stok hareketlerini başlatır. Çekme eylemleri, siparişlerdeki birden fazla sipariş satırı ve tüm teslimat şekilleri için aynı anda gerçekleştirilebilir.
- **Reddet** – Satırlar veya kısmi satırlar reddedilebilir. Bu, satırların arka ofisten başka bir mağazaya veya ambara atanmasına olanak tanır. Satırlar yalnızca henüz çekilmemiş veya paketlenmemiş olması durumunda reddedilebilir. Çekilmiş veya paketlenmiş olan bir satırı reddetmek için, arka ofis tarafından bu satırdaki çekme veya paketleme işleminin geri alınması gerekir.
- **Paketle** – Paketle seçeneği iki eylemi destekler: **Sevk irsaliyesi yazdır** seçeneği seçili satırlar için sevk irsaliyesi yazdırır ve **Paketlendi olarak işaretle** seçeneği satırları paketlendi olarak işaretler ve satırlar arka ofiste teslim edildi olarak işaretlenir. Yalnızca aynı siparişe ait olan ve aynı teslimat şekline sahip olan sipariş satırları aynı anda paketlenebilir. Sevk irsaliyesi biçimleri makbuz biçimlerinin bir parçası olarak denetlenir. Makbuz biçimleri ayarlama hakkında daha fazla bilgi için bkz. [Makbuz şablonları ve yazdırma](https://docs.microsoft.com/dynamics365/unified-operations/retail/receipt-templates-printing).
- **Sevk et** – Sevk etme eylemi seçili satırları arka ofiste **Teslim edildi** olarak işaretler. Bir satır tam olarak sevk edildikten sonra, artık sipariş karşılama görünümünde görüntülenmez.
- **Malzeme çekme** – Malzeme çekme eylemi çekme için satırları hareket görünümüne ekler. Siparişte henüz çekilmemiş başka satırlar olması durumunda, bu satırlar hareket görünümüne sıfır miktarıyla eklenir. Bir satır tam olarak çekildikten sonra, artık sipariş karşılama görünümünde görüntülenmez.

### <a name="order-fulfillment-filtering"></a>Sipariş karşılama filtreleme

Satış noktasında sipariş karşılama, kullanıcının ihtiyacı olanı bulmasına yardımcı olmak amacıyla filtreleme özelliği içerir. Filtreler, **Satış noktası** ekranının alt kısmındaki Eylem Bölmesinden değiştirilebilir. Varsayılan olarak, işlemin nasıl ayarlandığına bağlı olarak, **Teslimat türü** filtresi uygulanır. İşlem **Tüm siparişler** parametresiyle ayarlanmışsa, bu filtre sipariş karşılamaya erişildiğinde uygulanır. Aynı durum **Mağazadan çekme** ve **Mağazadan sevkiyat** parametreleri için de geçerlidir. Sipariş karşılama görünümüne uygulanabilecek filtreler şunlardır:

- Müşteri numarası
- Müşteri adı
- Müşteri e-postası
- Sipariş numarası
- Teslimat şekli
- Makbuz numarası
- Kanal Referansı Kodu
- Kaynak mağaza numarası
- Satır durumu
- Oluşturulma tarihi
- Teslimat tarihi
- Giriş tarihi
