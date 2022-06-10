---
title: Satış noktasında (POS) ürün arama ve müşteri arama
description: Bu konu Dynamics 365 Commerce içinde ürün ve müşteri arama özelliğinde yapılmış olan iyileştirmeler hakkında genel bakış sağlar.
author: ShalabhjainMSFT
ms.date: 05/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 460c7d3b00421ba43414f7343887edf9b8adad9c
ms.sourcegitcommit: 9dd2d32fc303023a509d58ec7b5935f89d1e9c6d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/26/2022
ms.locfileid: "8806440"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Satış noktasında (POS) ürün arama ve müşteri arama

[!include [banner](includes/banner.md)]

Modern Point of Sale (MPOS) ve Cloud Point of Sale (CPOS), ürünler ve müşteriler için kolay kullanımlı arama işlevi sağlar. Arama çubuğu her zaman MPOS ve CPOS pencerelerinin üstünde olduğundan çalışanlar ürünleri ve müşterileri hızla arayabilir.

Çalışanlar geçerli mağazayla ilişkilendirilmiş ürün çeşitleri ve kataloglardaki ürünleri arayabilir. Ayrıca, çalışanlar şirketteki başka bir mağazayla ilişkilendirilmiş ürün çeşitleri ve kataloglardaki ürünleri arayabilir. Bu nedenle, kasiyerler mağaza sınıflandırması dışındaki ürünleri satabilir ve iade alabilir. Benzer şekilde, çalışanlar geçerli mağaza veya şirketle ilişkili herhangi başka bir mağaza ile ilişkili müşterileri arayabilir. Ek olarak, çalışanlar, üst kuruluştaki başka bir şirketle ilişkilendirilmiş müşterileri arayabilirler.

## <a name="product-search"></a>Ürün arama

Varsayılan olarak, ürün aramaları mağaza ürün çeşitlerinde yapılır. Bu arama türü *yerel ürün arama* olarak bilinir. Ancak, çalışanlar geçerli mağaza ile ilişkilendirilen herhangi bir kataloğa kolayca geçiş yapabilir veya farklı bir mağazada arama yapabilirler. Bu arama türü *uzak ürün arama* olarak bilinir. Kataloğu değiştirmek için sayfanın sol tarafındaki **Kategoriler** düğmesini seçin. Beliren bölmenin üstünde, **Kataloğu değiştir** düğmesini seçin ve sonra taramak için kullanılabilir kataloglardan birini seçin. Sistem ürünleri seçilen katalogda arar.

**Kataloğu değiştir** sayfasında, çalışanlar kolayca herhangi bir mağazayı seçebilir veya tüm mağazalar arasındaki ürünler arasından arama yapabilir.

![Katalog değiştirme.](./media/Changecatalog.png "Katalog değiştirme")

Bir yerel ürün arama, aşağıdaki ürün özellikleri içerisinde arar:

- Ürün numarası
- Ürün adı
- Tanım
- Boyutlar
- Barkod
- Ad ara

### <a name="additional-local-product-search-capabilities-conventional-sql-full-text-search"></a>Ek yerel ürün arama yetenekleri (geleneksel SQL tam metin araması) 

- Çoklu anahtar sözcük aramaları için (yani, arama terimleri kullanan aramalar için) perakendeciler aramanın *herhangi bir* arama terimi ile mi eşleşen yoksa yalnızca *tüm* arama terimleriyle mi eşleşen sonuçları dahil edeceğini yapılandırabilir. Bu işlev için ayar, POS işlevi profilinde, **Ürün arama** olarak adlandırılan yeni bir grupta kullanılabilir. Varsayılan ayar **Herhangi bir arama terimi ile eşleş**'tir. Bu ayar aynı zamanda önerilen ayardır. **Herhangi bir arama terimiyle eşleştir** ayarı kullanıldığında, tamamen veya kısmen bir veya daha fazla arama sözcüğüne uyan tüm ürünler sonuç olarak döndürülür. Bu sonuçlar, en çok eşleşen anahtar kelimeye sahip ürünlere göre (tam veya kısmi) artan düzende sıralanır.

    **Tüm arama terimleriyle eşleş** ayarı, yalnızca tüm arama terimleriyle (kısmi veya tam) olarak eşleşen ürünleri döndürür. Bu ayar, ürün adları uzunsa ve çalışanlar arama sonuçlarında yalnızca sınırlı ürünleri görmek istiyorlarsa kullanışlıdır. Ancak, bu tür aramanın iki sınırlaması vardır:

    - Arama yalnızca tek tek ürün özellikleri üzerinde yapılır. Örneğin, en az bir ürün özelliğinde, yalnızca tüm aranan kelimeleri içeren ürünler döndürülür.
    - Boyutlar aranmaz.
> [!NOTE]
> POS işlevselliği profillerindeki aşağıdaki **Herhangi arama terimini eşleştir**/**Tüm arama terimlerini eşleştir** yapılandırmaları, yalnızca **yerel** ürün aramaları (geleneksel SQL tüm metin arama) deneyimleri için geçerlidir. Bu yapılandırmanın, bulut destekli arama deneyimleri üzerinde etkisi yoktur. Yeni arama motoru, ürün arama sonuçlarıyla ilgili arama sonucunu destekleyen kendi gelişmiş algoritmasıdır. 

- Perakendeciler ürün aramayı, kullanıcılar ürün adlarını yazarken arama sonuçlarını gösterecek şekilde yapılandırabilir. Bu işlev için yeni bir ayar, POS işlevi profilinde, **Ürün arama** olarak adlandırılan bir grupta kullanılabilir. Bu ayarın adı **Yazarken arama önerilerini göster**'dir. Bu işlev, çalışanların aradıkları ürünü hızlıca bulmalarına yardımcı olabilir çünkü tam adını yazmalarına gerek kalmaz.
- Ürün arama algoritması şimdi ayrıca aranan terimleri ürünün **Arama adı** özelliğinde de arar.

![Ürün önerileri.](./media/Productsuggestions.png "Ürün önerileri")

## <a name="customer-search"></a>Müşteri araması

Müşteri arama, çeşitli amaçlarla müşterileri bulmak için kullanılır. Örneğin, kasiyer bir müşterinin istek listesini veya satın alma geçmişini görüntülemek veya müşteriyi bir harekete eklemek isteyebilir. Arama algoritması arama terimlerini aşağıdaki müşteri özelliklerinde bulunan değerlerle eşleştirir:

- Dosya Adı
- E-posta adresi
- Telefon numarası
- Bağlılık programı kart numarası
- Adres
- Hesap numarası

Bu özellikler arasında, ad birden çok anahtar sözcükle arama esnekliği sağlar, çünkü algoritma herhangi bir arama anahtar sözcüğü ile eşleşen tüm müşterileri getirir. Ancak, daha fazla anahtar kelime ile eşleşen müşteriler sonuçların üst kısmında görüntülenir. Bu davanış, kasiyerlerin tam isim aradıkları, ancak soyadının ve adın ilk veri girişinde yer değiştirdiği durumlarda yardımcı olur. Ancak, performans sebebiyle, diğer tüm özellikler arama anahtar kelimeleri sırasını korur. Bu nedenle, arama anahtar sözcüklerinin sırası verilerin depolandığı sırayla eşleşmezse hiçbir sonuç döndürülmez.

Varsayılan olarak, müşteri arama mağazayla ilişkilendirilmiş olan müşteri adres defterleri üzerinden yapılır. Bu arama türü *yerel müşteri arama* olarak bilinir. Bununla birlikte, çalışanlar müşteriler için genel arama da yapabilir. Başka bir deyişle, şirketin mağazaları ve tüm diğer tüzel kişiler arasında arama yapabilirler. Bu arama türü *uzak müşteri arama* olarak bilinir.

Genel olarak aramak için, çalışanlar sayfanın altında bulunan **Sonuçları filtrele** düğmesini seçebilir ve sonra **Tüm mağazaları ara** seçeneğini, aşağıdaki şekilde gösterildiği gibi işaretleyebilir. Bu durumda, yalnızca müşteriler döndürülmez. Merkezdeki herhangi bir adres defterinin parçası olan tüm taraflar da döndürülür. Bu taraflar arasında çalışanlar, satıcılar, ilgili kişiler ve rakipler de vardır.

> [!NOTE]
> Bir uzak müşteri aramasının sonuç döndürmesi için en az dört karakter girilmesi gerekir.

Diğer tüzel varlıklardan sorgulanan müşteriler için müşteri kimliği gösterilmez, çünkü geçerli şirkette bu müşteriler için bir müşteri kimliği oluşturulmamıştır. Ancak, bir çalışan müşteri ayrıntıları sayfasını açarsa, sistem otomatik olarak bu taraf için bir müşteri kimliği oluşturur ve mağazanın müşteri adres defterini müşteri ile ilişkilendirir. Bu nedenle, müşteri daha sonra yapılan yerel mağaza aramalarında da görünür.

![Global müşteri araması.](./media/Globalcustomersearch.png "Global müşteri araması")

### <a name="additional-local-customer-search-capabilities"></a>Ek yerel müşteri arama yetenekleri

Kullanıcı bir telefon numarası aradığında sistem müşteri oluşturulurken eklenmiş olabilecek parantez, tire, boşluk gibi özel karakterleri yok sayar. Bu nedenle, kasiyelerin arama yaparken telefon numarası biçimi hakkında endişelenmesi gerekmez. Örneğin, bir müşterinin telefon numarası **123-456-7890** olarak girilmişse, bir kasiyer müşteriyi **1234567890** veya telefon numarasının ilk birkaç rakamını girerek arayabilir.

> [!NOTE]
> Bir müşterinin birden fazla telefon numarası ve birden çok e-postası olabilir. Müşteri arama algoritması bu ikincil e-postaları ve telefon numaralarını da arar ancak müşteri arama sonuçları sayfası yalnızca birincil e-posta ve telefon numarasını görüntüler. Bu durum, döndürülen müşteri sonuçları aranan e-posta veya telefon numarasını göstermediğinde, bazı karışıklıklara neden olabilir. Gelecekteki bir sürümde, müşteri arama sonuçları ekranını bu bilgileri gösterecek şekilde geliştirmeye yönelik bir plan yapılmıştır.

Geleneksel müşteri arama birden çok alanda arama yaptığından zaman alabilir. Bunun yerine, kasiyerler adı, e-posta adresi veya telefon numarası gibi tek bir müşteri özelliği için arama yapabilir. Müşteri arama algoritmasının kullandığı özellikler topluca *müşteri arama ölçütü* olarak bilinir. Sistem Yöneticisi bir veya daha fazla ölçütü POS'ta görüntülenecek kısayol olarak kolayca yapılandırabilir. Arama tek bir ölçütle sınırlı olduğundan, yalnızca ilgili arama sonuçları gösterilir ve standart müşteri arama performansına göre çok daha iyi performans elde edilir. Aşağıda POS'taki müşteri arama kısayolları gösterilmektedir.

![Müşteri araması kısayolları.](./media/SearchShortcutsPOS.png "Müşteri araması kısayolları")

Arama ölçütlerini kısayol olarak belirlemek için yöneticinin Commerce'da **Ticaret parametreleri** sayfasını açması ve **POS arama ölçütü** sekmesinde kısayol olarak gösterilecek tüm ölçütleri seçmesi gerekir.

![Arama kısayollarını yapılandırma.](./media/ConfigureShortcutsAX.png "Arama kısayollarını yapılandırma")

> [!NOTE]
> Çok sayıda kısayol eklerseniz, POS arama çubuğundaki açılan menü kalabalık olur ve çalışanın arama deneyimini etkileyebilir. Yalnızca gerektiği kadar kısayol eklemenizi öneririz.

**Görüntüleme sırası** alanı kısayolların POS'ta gösterileceği sırayı belirler. Gösterilen ölçütler müşteri arama algoritmasının müşterileri aramak için kullandığı kullanıma hazır özelliklerdir. Bununla birlikte, iş ortakları arama kısayolu olarak özel özellikleri ekleyebilir. Arama kısayolu olarak özel özellikler eklemek için sistem yöneticisinin müşteri arama ölçütleri için kullanılan genişletilebilir numaralandırmayı (enum) genişletmesi ve ardından iş ortağının özel özelliklerini kısayol olarak işaretlemesi gerekir. İş ortakları kendi özel kısayollarını aramalar için kullanıldığında, sonuçları bulmak için kod yazmaktan sorumludur.

POS'ta kısayolların işlenmesini istiyorsanız, kısayol çevirileri gereklidir. Kanal diliniz sistem varsayılan dilinden farklıysa, her kısayolun çevirisini beklenen dilde tanımlamanız gerekir. Her kısayol için **Çevir**'i seçerek çevirileri tanımlayabilirsiniz. 

> [!NOTE]
> Enuma eklenen özel bir özellik standart müşteri arama algoritmasını etkilemez. Başka bir deyişle, müşteri arama algoritması özel özellikte arama yapmaz. Kullanıcılar yalnızca o özel özellik kısayol olarak eklenirse veya varsayılan arama algoritması geçersiz kılınırsa aramalar için özel bir özellik kullanabilir.

Perakendeciler, POS'ta varsayılan müşteri arama modunu **Tüm mağazalarda ara** olarak da ayarlayabilir. Bu yapılandırma, POS dışında oluşturulan müşterilerin hemen aranması (örneğin, dağıtım işi çalıştırılmadan önce) için doğrudan arama yapılması gereken senaryolarda yardımcı olabilir. Bunu yapmak için, perakendeci POS işlevsellik profilindeki **varsayılan müşteri arama modu** seçeneğini etkinleştirmelidir. **Evet** olarak ayarlandığında her müşteri arama denemesinde, yönetim merkezine gerçek zamanlı bir çağrı yapılır.

Beklenmedik performans sorunlarının engellenmesine yardımcı olmak için, bu yapılandırma **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING** adında bir deneme bayrağı arkasında gizlenir. Bu nedenle, kullanıcı arayüzünü (UI) ayarlayarak **Varsayılan müşteri arama modu**'nu göstermek için, satıcı kullanıcı kabul testi (UAT) ve üretim ortamları için bir destek bileti oluşturmalıdır. Bilet alındıktan sonra, mühendislik ekibi, perakendecinin, performansı değerlendirmek ve gereken tüm değerlendirmeleri uygulamak için üretim dışı ortamlarında test yapmasını sağlamak üzere perakendeciyle birlikte çalışacaktır.

## <a name="cloud-powered-customer-search"></a>Bulut destekli müşteri arama

Azure Cognitive Search hizmeti kullanılarak yapılan müşteri arama yeteneğinin genel önizlemesi Commerce 10.0.18 sürümünün bir parçası olarak sunuldu. Performans iyileştirmelerine ek olarak, hizmetin kullanıcıları da zengin iyileştirme ve iyileştirilmiş yakınlık yeteneklerinden faydalanır. Performans iyileştirmeleri özellikle, POS'un genel arama özelliği ("tüm mağazalarda ara") kullanıldığında belirgindir. Bunun nedeni, arama sonuçlarının Commerce headquarters'taki verilerden sorgulanarak değil Azure arama dizininden getirilmesidir. 

### <a name="enable-the-cloud-powered-search-feature"></a>Bulut destekli arama özelliğini etkinleştirme

> [!NOTE]
> Hem Commerce headquarters'ın hem de Commerce Scale Unit'in sürüm 10.0.18'e güncelleştirilmesi gereklidir. POS'un güncelleştirilmesine gerek yoktur.

Commerce Headquarters'da bulut destekli arama özelliğini etkinleştirmek için, aşağıdaki adımları izleyin.

1. **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
1. **(Önizleme) Bulut destekli müşteri arama** özelliğini bulup seçin ve **Şimdi etkinleştir**'i seçin.
1. **Retail ve Commerce > Headquarters kurulumu > Commerce scheduler > Commerce scheduler'ı başlat**'a gidin ve **Dağıtım planı** formunda yeni **1010_CustomerSearch** işini görüntülemek için **Tamam**'ı seçin.
1. **Retail ve Commerce > Retail ve Commerce IT > Dağıtım planı**'na gidin.
1. **1010_CustomerSearch** işini çalıştırın. Bu iş, tarihi Azure Search dizinine yayımlar. Dizinin yayımlanması tamamlandığında, işin durumu **uygulandı** olarak ayarlanır.
1. **1010_CustomerSearch** iş durumu **uygulandı** olarak ayarlandığında, **özellik yönetiminde** yeni etkinleştirilen özelliğin POS kanallarını güncelleştirmek için **1110-Global yapılandırma** işini çalıştırın.
1. Daha sonra, Müşteri güncelleştirmelerini arama dizinine göndermek için, **1010_CustomerSearch** işini düzenli aralıklarla çalıştırın.

> [!NOTE]
> İlk dizin yayımlama için, **1010_CustomerSearch** işi tüm müşteri kayıtlarını Azure search dizinine göndereceği için tamamlanması birkaç saat sürebilir. Sonraki güncelleştirmeler birkaç dakika sürer. Bulut destekli arama özelliğinin etkinleştirildiği, ancak dizin yayımlamanın henüz tamamlanmadığı dönemde, POS'tan alınan müşteri araması varsayılan olarak varolan SQL tabanlı aramaya göre yapılır. Bu işlem, mağaza operasyonlarında kesintiler olmamasını sağlar.

### <a name="functional-differences-from-the-existing-search"></a>Varolan aramadan işlevsel farklılıklar

Aşağıdaki listede, bulut destekli müşteri arama işlevinin varolan arama işlevinden nasıl farklı olduğu gösterilmektedir. 

- Commerce Headquarters'da oluşturulan ve düzenlenen müşteriler **1010_CustomerSearch** işi çalıştırıldığında Azure search dizinine gönderilir. Bu güncelleştirmelerin, dizini güncelleştirmesi en az 15 ila 20 dakika sürer. POS kullanıcıları Commerce Headquarters'da güncelleştirmeler yapıldıktan yaklaşık 15-20 dakika sonra yeni müşterileri arayabilir (veya güncelleştirilmiş bilgileri temel alarak arama yapabilir). İş süreciniz, Commerce Headquarters'da oluşturulan müşterilerin POS'ta hemen aranabilir olmasını gerektiriyorsa, bu sizin için doğru servis olmayabilir.
- POS'ta oluşturulan yeni müşteriler Commerce Scale Unit'ten Azure search dizinine gönderilir ve tüm mağazalarda hemen aranabilir hale gelir. Ancak, zaman uyumsuz müşteri oluşturma özelliği açıksa, yeni müşteri kayıtları Commerce Scale Unit'ten Azure search dizinine yayımlanmaz ve müşteri bilgileri Commerce Headquarters ile eşitleninceye ve zaman uyumsuz müşteriler için müşteri kodları oluşturuluncaya kadar POS'ta aranamaz. **1010_CustomerSearch** işi zaman uyumsuz müşteri kayıtlarını Azure search dizinine gönderebilir. Ortalama olarak, 30 dakika sonra yeni oluşturulan zaman uyumsuz müşteriler POS'ta aranabilir. Bu tahmin, **1010_CustomerSearch**, **P-job** ve **müşterileri ve iş ortaklarını zaman uyumsuz modden eşitle** işlerinin her 15 dakikada bir çalışacak şekilde zamanlandığını varsayar.
- Bulut destekli arama, müşterilerin ikincil e-postalarını ve telefon numaralarını da arar, ancak müşteri arama sonuçları, müşterilerin birincil telefon numarasını ve birincil e-posta adresini görüntüler. İlk bakışta, ilgisiz arama sonuçları döndürülmüş gibi görünebilir, ancak arama sonuçlarında bir müşterinin ikincil e-posta adresini ve telefon numarasını denetlemek, anahtar sözcük aramanın bir müşteri eşleşmesiyle sonuçlandığını doğrulamaya yardımcı olabilir. Bu karışıklığı önlemek için, kullanıcıların arama sonucunun neden döndürüldüğünü anlamasına yardımcı olmak üzere arama sonuçları sayfasını iyileştirme planları vardır.
- Genel aramada ("tüm mağazalarda ara") en az 4 karakter kullanarak arama gereksinimi Bu hizmet için geçerli değildir.

> [!NOTE]
> Azure Cognitive search hizmetini kullanan müşteri arama yeteneği, önizleme için sınırlı bölgelerde kullanılabilir. Müşteri arama özelliği aşağıdaki bölgelerde *kullanılamaz*:
> - Brezilya
> - Hindistan

[!INCLUDE[footer-include](../includes/footer-banner.md)]
