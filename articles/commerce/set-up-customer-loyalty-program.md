---
title: Bağlılık programına genel bakış
description: Bu konu, Dynamics 365 Commerce'daki bağlılık özelliklerini ve satıcının bağlılık programına kolayca başlamasına yardımcı olmak için karşılık gelen kurulum adımlarını açıklar.
author: scott-tucker
ms.date: 07/21/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.custom:
- "16201"
- intro-internal
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 57512bbd735e26ba31e00518ca8179f2d9b14bc4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985174"
---
# <a name="loyalty-overview"></a>Bağlılık programına genel bakış

[!include [banner](includes/banner.md)]

Bağlılık programları, müşterileri Retailer markasıyla etkileşimleri için ödüllendirerek müşteri bağlılığını artırmanıza yardımcı olabilir. Dynamics 365 Commerce içinde, herhangi bir ticaret kanalındaki tüzel varlıklarınıza uygulanacak basit veya karmaşık bağlılık programları ayarlayabilirsiniz. Bu konu, Commerce'deki bağlılık özelliklerini ve satıcının bağlılık programına kolayca başlamasına yardımcı olmak için karşılık gelen kurulum adımlarını açıklar.

Aşağıdaki seçenekleri içeren bir bağlılık programı ayarlayabilirsiniz.

- Bağlılık programlarınızda sunduğunuz birden çok ödül türünü ayarlayın ve bağlılık programlarına katılımı izleyin.
- Sunduğunuz farklı ödül teşviklerini temsil eden bağlılık programları ayarlayın. Daha sık alışveriş yapan veya mağazalarda daha fazla para harcayan müşterilere daha büyük teşvikler ve ödüller sunmak için bağlılık programı katmanları ekleyin.
- Bir müşterinin ödülleri kazanması için tamamlaması gereken etkinlikleri tanımlamak üzere kazanç kuralları tanımlayın. Ayrıca, bir müşterinin ödülleri ne zaman ve nasıl kullanabileceğini belirleyen kullanım kuralları da tanımlayabilirsiniz.
- Bağlılık programlarınıza katılan herhangi bir kanalından bağlılık kartları çıkarın ve bağlılık kartlarını, müşterinin katılabileceği bir veya daha fazla bağlılık programına bağlayın. Ayrıca müşteri kaydını bir bağlılık kartına bağlayarak müşterinin birden fazla karttan bağlılık puanları toplayıp kullanabilmesini de sağlayabilirsiniz.
- Bağlılık programı kartlarını el ile ayarlayın ya da bir müşteriyi ödüllendirmek veya ihtiyacını karşılamak için bağlılık ödülleri bakiyesini bir karttan diğerine transfer edin.

## <a name="setting-up-loyalty-programs"></a>Bağlılık programları ayarlama

Commerce'de bağlılık özelliğini etkinleştirmek için çeşitli bileşenleri ayarlamanız gerekir. Aşağıdaki diyagram, bağlılık bileşenlerini ve birbirleriyle ilişkisini gösterir.

![Bağlılık programı ayarlama işlem akışı.](./media/loyaltyprocess.gif "Bağlılık programı bileşenleri ve birbirleriyle ilişkileri")

## <a name="loyalty-components"></a>Bağlılık programı bileşenleri

Aşağıdaki tabloda her bir bileşen ve bağlılık programı ayarlarında nerede kullanıldığı tanımlanmıştır.

| Bileşen                                        | Açıklama | Kullanıldığı yer |
|--------------------------------------------------|-------------|-----------------|
| İskontoları ayarlama (önkoşul)                  | Bağlılık programı müşterilerinize sunduğunuz iskontoları ayarlayın. Örneğin, tüm giyim ürünlerinde yüzde 5 indirim sunabilirsiniz. | İskontolar, fiyat grupları bir bağlılık programına dahil edilmeden önce eklenmelidir. Fiyat grupları, bağlılık programlarına ve bağlılık programı katmanlarına atanır. |
| Fiyat gruplarını ayarlama (önkoşul)               | Fiyat grupları, ürünler için fiyatları ve iskontoları oluşturmak ve yönetmek için kullanılır. Bağlılık programlarınıza uygulanan iskontoları içeren fiyat gruplarını ayarlayın. | Fiyat grupları, bağlılık programlarına ve bağlılık programı katmanlarına atanır. |
| Kanalları ayarlama (önkoşul)                   | Commerce kanalları, bir adreste hizmet veren mağaza, çevrimiçi mağaza veya çağrı merkezi gibi bağlılık programlarınıza katılan mağazalardır. Bunlara bağlılık programları atamadan önce kanallarınızı ayarlamanız gerekir. | Kanalı bağlılık programına katılıyorsa ilgili kanalını bağlılık programına atarsanız. |
| Bağlılık programı ödeme yöntemi ayarlama (önkoşul) | Bağlılık programı puanlarının, fiziksel mağazalar, çevrimiçi mağazalar veya çağrı merkezleri gibi herhangi bir kanalda kullanılabilir olmasını sağlamak için **Kart numaraları** sayfasında bağlılık programı kartları için aralık ayarlamanız gerekir. | Bir bağlılık programı türü ödeme yöntemi ayarlayın, sonra bağlılık programı ödeme yöntemini bağlılık programına katılan kanallarına atayın. |
| Tarih aralıklarını ayarlama                            | Tarih aralıkları, bağlılık programı katmanları için geçerli zaman aralığını ayarlamanın esnek bir yolunu sağlar. Bir müşterinin bir katmanında ne kadar kalacağını veya bir katman için uygun hale gelmesi için bir etkinliği ne kadar sürede tamamlaması gerektiğini belirlemek için tarih aralıklarını kullanın. | Tarih aralıkları yalnızca bağlılık programlarınızda katmanlar kullanıyorsanız geçerlidir. Program katmanlarında geçerli tarih aralığını ve program katmanı kuralları için geçerli tarih aralıklarını seçin. |
| Ödül puanlarını ayarlama                             | Ödül puanları, müşterilerinize sunduğunuz ödül türleridir. Ödül puanları, kullanılabilir veya kullanılamaz özelliktedir. Kullanılabilir ödül puanları ürünlerle takas edilebilir. Kullanılamaz ödül puanları, izleme amaçlarıyla veya bağlılık programındaki bir müşteriyi sonraki katmana ilerletmek için kullanılır. | Ödül puanları, katman kurallarında gösterilir ve bir müşterinin belirli bir katman için uygunluğunu belirlemek üzere kullanılır. Ödül puanları, bağlılık programı planlarında kazanç ve kullanım kurallarında da gösterilir. Kazanç kurallarında, müşterinin belirli bir etkinlik neticesinde kazanabileceği ödülleri belirtirsiniz. Kullanım kurallarında, müşterinin kullanabileceği ödülü belirtirsiniz. |
| Bağlılık programları ayarlama                          | Bağlılık programları, sunduğunuz temel bağlılık öğeleridir. Her bir bağlılık programına atanmış bağlılık programı katmanları vardır. İskontolar ve fiyat grupları, program düzeyinde ya da katman düzeyinde bağlılık programlarına atanır. | Bağlılık programlarınız için bağlılık programı planları oluşturursunuz. Bağlılık programı kartlarını bağlılık programlarınıza atarsınız ve sonra bu kartlar müşterilere atanabilir. Kanalları, bağlılık programı planlarına atanmış olan bağlılık programları katılır. Bağlılık programı kartına sahip tüm müşteriler ilgili karta atanmış bağlılık programlarına katılabilir. |
| Bağlılık programı katmanları ve katman kuralları ayarlama              | Bağlılık katmanları, bağlılık programlarınız için tanımlayabileceğiniz isteğe bağlı düzeylerdir. Bağlılık programına katılan tüm müşteriler için taban fiyat iskontolarının ve ödüllerin yanı sıra, program içinde çeşitli düzeylere ulaşan müşteriler için ek iskontolar ve ödüller de ayarlayabilirsiniz. Tanımladığınız her bir bağlılık programı katmanına yönelik olarak o katmana uygun bir müşteri için kurallar ayarlayabilirsiniz. O katmana ulaştıktan sonra müşterilerin orada ne kadar süreyle kalabileceğini de belirleyebilirsiniz. | Bağlılık programı katmanları ve bağlılık programı katman kuralları bağlılık programları içinde tanımlanır. Hiçbir bağlılık programı katmanı tanımlamazsanız, bağlılık programına katılan tüm müşteriler bağlılık programı fiyat grubunu atadığınız iskontolar için uygun olur. Bağlılık programı katmanları tanımlarsanız, bağlılık programı planındaki bağlılık programları katmanları için kazanç ve kullanım kuralları ayarlayabilirsiniz. |
| Bağlılık programı planları kurma                           | Bağlılık programı planları, seçilen bağlılık programı için geçerli kullanım ve kazanç kurallarını belirtir. Bağlılık programını, kazanç kurallarını ve bir mağaza için geçerli kullanım kurallarını tanımlamak için bir bağlılı programı planına kanalları atarsınız. | Bir bağlılık programı planı, bağlılık programına ve kanallarına atanır. Birden çok bağlılık programı planını aynı bağlılık programına veya çok sayıda kanalına atayabilirsiniz. |
| Bağlılık programı kartları ayarlama                             | Bir bağlılık programı kartı, kart sahibine ilgili karta atanmış bağlılık programlarına katılma yetkisi verir. Bağlılık programı kartları anonim olarak verilebilir ya da belirli bir müşteriye atanabilir. Belirli bir kart için bağlılık programı hareketlerini ve kartta birikmiş bağlılık programı puanlarına yönelik özeti görüntüleyebilirsiniz. Herhangi bir kanalından bağlılık programı kartları verebilirsiniz. Müşteriyi farklı bir katmana yükseltmek, bağlılık programı puanı eklemek veya bağlılık programı puan bakiyesini bir karttan diğerine aktarmak için bir bağlılık programı kartını el ile de ayarlayabilirsiniz. | Bağlılık programlarını bir bağlılık programı kartına atarsınız. |

## <a name="loyalty-processes"></a>Bağlılık programı işlemleri

Aşağıdaki tabloda, bağlılık programı yapılandırmaları ile verilerini mağazalarınıza göndermek ve mağazalarınızdan bağlılık programı hareketlerini almak için çalıştırılması gereken işlemler açıklanır.

| İşlem adı                         | Açıklama | Sayfa adı |
|--------------------------------------|-------------|-----------|
| 1050 (bağlılık programı bilgileri)           | Bağlılık programı verilerini Commerce'den perakende mağazalara göndermek için bu işlemi çalıştırın. Bağlılık programı verilerinin tüm mağazalara aktarılabilmesi için bu işlemi sık çalışacak şekilde zamanlamak iyi bir fikirdir. | Dağıtım planı |
| Bağlılık şemalarını işle              | Bağlılık programı planlarını bağlılık programı planının atandığı kanallarıyla ilişkilendirmek için bu işlemi çalıştırın. Bu işlem, toplu işlem olarak çalışacak şekilde zamanlanabilir. Bağlılık programı planları, bağlılık programları veya bağlılık programı ödül puanları gibi bağlılık programı yapılandırma verilerini değiştirirseniz bu işlemi çalıştırmanız gerekir. | Bağlılık şemalarını işle |
| Kazanılan bağlılık puanlarını toplu olarak deftere naklet | Çevrimdışı işlenen hareketlerin bağlılık programı kartlarına dahil edilebilmesi amacıyla bu kartları güncellemek için bu işlemi çalıştırın. Bu işlem yalnızca **Paylaşılan Commerce parametreleri** sayfasında **Kazanılan puanları toplu olarak deftere naklet** onay kutusu işaretlendiğinde geçerlidir, böylece ödüller çevrimdışıyken kazanılabilir. | Kazanılan bağlılık puanlarını toplu olarak deftere naklet |
| Bağlılık programı kartı katmanlarını güncelle            | Müşterinin kazanç etkinliğini bir bağlılık programının katman kurallarına göre değerlendirmek ve müşterinin katman durumunu güncelleştirmek için bu işlemi çalıştırın. Bu işlem yalnızca bağlılık programlarındaki katman kurallarını değiştirmek ve güncel kuralların önceden verilmiş bağlılık programı kartları için geriye dönük olarak geçerli olmasını istiyorsanız gereklidir. Bu işlem, toplu bir şeklinde veya tek tek kartlar için çalıştırılabilir. | Bağlılık programı kartı katmanlarını güncelle |

## <a name="loyalty-capabilities"></a>Bağlılık programı olanakları

- Satıcılar bağlılık programıyla ve bağlılık programı katmanlarıyla ilişkilendirilmiş fiyat gruplarını kullanarak, bağlılık programı üyeleri için kolayca özel fiyatlar ve indirimler oluşturabilirler.

- Bağlılık programı planının parçası olarak satıcılar, farklı katmanlardaki müşterilerin ödüllerini ayırmak için katmanlara göre farklı kazanç ve kullanım kuralları oluşturabilir. Belirli bir müşteri grubu mevcut katmanların parçası olabilsin ancak yine de farklı bir şekilde ödüllendirilebilsin diye satıcılar kazanma ve kullanma kurallarının bir parçası olarak "ilişkileri" de dahil edebilir. Bu, ek katmanları oluşturma gereksinimini engeller.
    
    > [!NOTE]
    > Bir bağlılık programı planı içinde kazanç kuralları ilavedir. Örneğin, her ABD doları için altın katman üyesine 10 puan verecek bir kural oluşturursanız ve aynı zamanda her ABD Doları için 5 puan kazanacak "gazi" ilişkisiyle bir kural oluşturursanız altın katman üyesi olan bir gazi, iki satır için de nitelikli olduğundan 1 ABD Doları için 15 puan kazanır. Ancak gazi müşteri altın katmanı üyesi değilse her dolar için 5 puan kazanır. Kanallarda değişiklikleri yansıtmak için **Bağlılık şemalarını işle** ve **1050** (bağlılık programı bilgileri) işlerini çalıştırın.
    
    ![İlişki tabanlı kazanç.](./media/Affiliation-based-earning.png "Bağlantı tabanlı katılım")

- Satıcılar genelde bağlılık programları uygulanmasını istemeyen belirli bir grup müşteri için özel fiyatlara sahiptir. Örneğin, özel fiyatlandırma alan ancak bağlılık puanı almayan toptancı veya personel. Genellikle, "ilişkiler" böyle müşteri gruplarına özel fiyat sağlamak için kullanılır. Müşterilerden belirli bir grubun bağlılık programı puanı kazanmasını sınırlamak için satıcı, bağlılık planının **Dışarıda bırakılan ilişkiler** bölümünde bir veya daha fazla ilişki belirtebilir. Bu şekilde, dışarıda bırakılan ilişkilere ait olan müşteriler bağlılık programı üyeleri olduğunda satın alımları için bağlılık puanı kazanamaz. Kanallarda değişiklikleri yansıtmak için **Bağlılık şemalarını işle** ve **1050** (bağlılık programı bilgileri) işlerini çalıştırın.

    ![Dışarıda bırakılan ilişkiler.](./media/Excluded-affiliations.png "İlişkileri bağlılık puanı kazanma dışında bırak")
    
- Satış noktası, satıcılar için fiziksel bağlılık programı kartlarını kullanma veya otomatik olarak benzersiz bağlılık programı kart numarası oluşturma esnekliği sağlar. Mağazalarında bağlılık programı kartlarının otomatik oluşturulmasını etkinleştirmek için mağazayla ilişkilendirilmiş işlev profilinde **Bağlılık programı kart numarası oluştur**'u açın. Çevrimiçi kanallar için satıcılar, müşterilerine bağlılık programı kartları yayınlamak üzere IssueLoyaltyCard API kullanabilir. Satıcılar, bu API'ya bağlılık programı kartı oluşturmak için kullanılacak olan bağlılık programı kart numarası sağlayabilir veya sistem, Commerce'de ayarlanan bağlılık programı kart numarası sıralamasını kullanır. Bununla birlikte, numara serisi yoksa ve satıcı API'yı çağırırken bir bağlılık programı kart numarası sağlamazsa bir hata görüntülenir.

    ![Bağlılık programı kartı oluşturma.](./media/Generate-loyalty-card.png "Otomatik bağlılık programı kart numarası oluştur")

- Kazanılan ve kullanılan bağlılık programı puanları, tam veya kısmi geri ödemelerde aynı miktarın verilmesi veya geri alınması için satış hattındaki her hareket ve satış emri için kaydedilebilir. Ayrıca, puanların satış satırı düzeyinde görünürlüğü arama merkezi kullanıcılarının, müşterilerin her satır için ne kadar puan kazandığı veya kullandığı sorularını yanıtlayabilme becerisi sağlar. Bu değişiklikten önce, ödül puanları iadelerde her zaman yeniden hesaplanırdı; bu da kazanma veya kullanma kuralları değiştirilirse orijinalden farklı bir tutara neden olurdu ve arama merkezi kullanıcıları puan dağılımını göremezdi. Puanlar her bağlılık programı kartı için **Kart hareketleri** formu altında görülür. Bu özelliği etkinleştirmek için S **atış hattı başına bağlılık programı puanları aktar** yapılandırmasını, **Commerce paylaşılan parametreler** \> **Genel** sekmesinde açın.

    > [!NOTE]
    > İadeler olması durumunda, doğru miktarda puan müşteriye verilmesi veya müşteriden alınmasını sağlamak için bu özelliğin açılması şiddetle tavsiye edilir.

- Satıcılar, artık her ödül puanı için hakediş ödeme dönemini tanımlayabilir. Hakediş ödeme dönemi yapılandırması, kazanma tarihinden sonra, ödül puanları müşteriler için kullanılabilir olduktan sonra süreyi tanımlar. Hak kazanılmamış puanlar **Bağlılık programı kartları** sayfasındaki **Hak kazanılmamış puanlar** sütununda görünebilir. Müşteriler bağlılık programı puanlarının kazanıldığı bazı ürünleri iade ettiğinde, varsayılan olarak, sistem ilk olarak hak kazanılmamış puanları alır ve ardından kullanılabilir puanlardan bakiyeyi düşer. Ancak, hak edilmemiş puanlar yerine yalnızca kullanılabilir puanlardan kesinti yapılmasını konfigüre edebilirsiniz.

Ayrıca, satıcılar bağlılık programı kartı başına maksimum bağlılık programı ödül puanı sınırı tanımlayabilir. Bu alan, bağlılık programı dolandırıcılığı etkisini azaltmak için kullanılabilir. Maksimum ödül puanına ulaşıldığında, kullanıcı daha fazla puan kazanamaz. Satıcı, bu tür krtları olası bir dolandırıcılı için araştırılana kadar engellemeyi seçebilir. Satıcı dolandırıcılık olduğuna karar verirse hem müşterinin bağlılık programı kartını hem de müşteriyi engelleyebilir. Bunu yapmak için **Müşterinin bağlılık programına kaydını engelle** özelliğini **Evet** olarak (**Commerce** hızlı sekmesindeki **Tüm müşteriler** altında) ayarlayın. Bloke müşteriler kanalları herhangi birinde bağlılık programı kartı yayınlayamaz.

   ![Hakediş ve maksimum ödül puanları.](./media/Vesting-and-maximum-reward-points.png "Temlik ve maksimum ödül puanlarını tanımalama")

- İlişkiler, özel fiyat ve indirimler sağlasa da, satıcıların müşterilerin görmesini istemediği bazı ilişkiler olabilir. Örneğin, "Yüksek harcamalı müşteri" başlıklı bir ilişki bazı müşteriler tarafından hoş karşılanmaz. Ayrıca, mağazada yönetilmemesi gereken bazı ilişkiler de vardır. Örneğin, personeller. Çünkü kasiyerlerin kimin personel olduğuna karar vermesini ve bu nedenle personel temelli indirimler sağlamasını istemezsiniz. Satıcılar şimdi kanallarında gizli olması gereken ilişkiler seçebilir. **Kanallarda gizle** olarak işaretli ilişkiler POS'ta görüntülenemez, eklenemez veya kaldırılamaz. Ancak, ilişkiyle ilgili olan fiyatlandırma ve indirimler hala ürünlere uygulanır.

    ![İlişkileri gizle.](./media/Hide-affiliations.png "Kanallarda ilişkileri gizle")
    
- Arama merkezi kullanıcıları artık müşterinin bağlılık programı kartı bilgilerini kullanarak müşteriyi kolayca arayabilir ve müşterinin bağlılık programı kartı ve bağlılık programı kartı hareket sayfalarına **Müşteri Hizmetleri** sayfasından gidebilir.

    ![Müşteri hizmetleri.](./media/Customer-service.png "Müşteri için bağlılık programı bilgisi bul")
    
- Bağlılık programı kartı güvenliği aşılırsa, yeni bir kart üretilmesi gerekir ve yeni kartına varolan puanlar aktarılır. Yeni kart akışı bu sürümde basitleştirilmiştir. Ayrıca, müşteriler bazı bağlılık programı puanlarını arkadaşlarına ve ailesine hediye edebilir. Puan aktarıldığında her bağlılık programı kartı için puan düzeltme girişleri oluşturulur. Yedek kart ve bakiye aktarma işlevine **Bağlılık programı kartları** sayfasından erişilebilir.

    ![Değiştirme ve puanları aktarma.](./media/Replace-and-transfer-points.png "Bağlılık programı kartı veya transfer bakiyesini Değiştir")
    
- Satıcılar, müşterileri bağlılık programına kaydetmek için belirli bir kanalın etkisini yakalamak isteyebilir. Bağlılık programı kartlarının kayıt kaynağı artık kaydedilir, böylece satıcılar bu veriler üzerinde raporları çalıştırabilir. Kayıtlar kaynağı, MPOS/CPOS veya e-ticaret kanallarından yayınlanan tüm bağlılık programı kartları için otomatik olarak yakalanır. Arka ofis uygulamasından yayınlanan bağlılık programı kartları için arama merkezi kullanıcısı uygun kanal seçebilir.
- Önceki sürümlerde, satıcılar müşterilerin bir mağazada bağlılık programı puanlarını kullanabilmesi için MPOS/CPOS kullanırdı. Ancak o sürümlerde, bağlılık programı bakiyesi bağlılık programı puanları olarak gösterildiğinden kasiyer, geçerli harekete uygulanacak para birimi değerinde miktarı görüntüleyemiyordu. Kasiyerin, bağlılık programı puanlarına göre ödeme yapmadan önce puanları para birimine dönüştürmesi gerekirdi. Mevcut sürümde, harekete satırları eklendikten sonra kasiyer, bağlılık programı puanlarının geçerli hareketi karşılayıp karşılamadığını görebilir; bu da hareketi bazı veya tüm bağlılık programı puanlarını uygulamayı kolaylaştırır. Ayrıca, kasiyer sonraki 30 gün içinde süresi dolacak puanları görebilir, böylece o harekette süresi dolacak puanların kullanılması adına müşteriyi motive ederek fazla satış veya çapraz satış yapabilir.

    ![Bağlılık bakiyesi kapsamındaki tutar.](./media/Points-covered-by-loyalty-balance.png "Bağlılık bakiyesi kapsamındaki tutar")

    ![Süresi dolmak üzere olan puanlar.](./media/Expiring-points.png "Süresi dolan puanları görüntüle")

- 8.1.3 sürümüyle, çağrı merkezi kanalında "bağlılık ile ödeme" seçeneğini etkinleştirdik. Bu seçeneği etkinleştirmek için bir bağlılık ödeme türü oluşturun ve bunu çağrı merkezi ile ilişkilendirin. 

    > [!NOTE]
    > Bağlılık ödemeleri kart ödemeleri olarak ayarlandığı için bir kartı **Kart kurulumu** sayfasından seçmeniz gerekir. 

    ![Bağlılık kartı kurulumu.](./media/LoyaltyCardSetup.png "Bağlılık kartı kurulumu")

    Bu ayardan sonra, müşteriler bağlılık puanlarını çağrı merkezinden kullanabilirler. Ek olarak, kullanıcı deneyimini "Bağlılık puanı tarafından karşılanan tutar"ı göstermek üzere geliştiriyoruz, böylece çağrı merkezi kullanıcılarının bağlılık puanı bakiyesini görmek için başka bir ekrana gitmelerine gerek kalmaz.

- Birçok satıcı, yalnızca satış hareketlerine bağlı olarak bağlılık programı puanları ödülü verebilir ancak daha müşteri merkezli satıcılar, müşterilerin markasıyla olan her etkileşimini ödüllendirir. Örneğin, çevrimiçi bir anket tamamlama, mağaza ziyareti, Facebook'ta satıcıları beğen, satıcı hakkında Twitter'a yazma ve daha fazlası için ödül vermek ister. Bunu yapmak için satıcı istediği sayıda "Diğer faaliyet türü"nü ve bu etkinliklere karşılık gelen kazanç kurallarını tanımlayabilir. Ayrıca, açık bir Commerce Scale Unit'i "PostNonTransactionalActivityLoyaltyPoints" vardır ve bu, müşteriye bağlılık puanı kazandıracak bir etkinlik belirlendiğinde çağrılabilir. Bu API, Bağlılık kartı kimliği, kanal kimliği ve diğer etkinlik tipi kimliği bekler, böylece puan alacak müşteri tespit edilebilir ve etkinlik için kazanma kuralı tespit edilebilir. 

    Hareket tipi olmayan etkinlikler için puan kazandırmanın iki önemli adımı vardır:

    - Bir etkinliğin gerçekleştiğini ve ödüllendirilmesi gerektiğini tespit etmek.
    - Uygun puanları kazandırmak.

    Bu adım Commerce için haricidir, örneğin marka hakkında tweet yazmak veya markayı Facebook'ta beğenmek gibi. Bu etkinlik tanımlandıktan sonra, perakendeciler yukarıda bahsedilen Commerce Scale Unit API'sini çağırabilir ve bağlılık puanlarını gerçek zamanlı olarak verebilirler. Bu tür senaryolarda, bir gözden geçirme adımına gerek yoktur çünkü etkinlikler gerçekleşmiştir ve karşılık gelen puanlar verilir. Ancak, perakendecinin kayıtları puanları vermeden önce gözden geçirmek isteyeceği bazı senaryolar vardır. Örneğin, perakendeci mağazada bir workshop açmıştır ve müşterilerin etkinlik kaydı başvurusu yapmaları için e-ticaret sitesinde kayıt olmaları gerekir. Ancak, yalnızca katılım gösteren müşteriler ödül kazanacaktır. Bu tür senaryolar için 10.0 sürümünde **Perakende bağlılık diğer etkinlik türü satırlar** adlı bir veri varlığı oluşturduk. Bu veri varlığı, perakendecilerin Veri İçe Aktarma/Dışa Aktarma Çerçevesini (DIXF) veya OData API kullanarak, müşterilere bağlılık puanı kazandırması gereken etkinlikleri kaydetmesine olanak sağlar. Veri varlığı, etkinlikleri **Diğer etkinlikler için bağlılık satırları** adlı bir günlükte depolar, bu da gözden geçirme ve değiştirme amacıyla kullanılabilir. Veri gözden geçirildikten sonra, IT kullanıcısı etkinlik satırlarını el ile deftere nakledebilir veya **Bağlılık satırları için diğer etkinlik** adlı bir işi çalıştırabilir, bu da deftere nakledilmemiş tüm etkinlik satırlarını deftere nakleder ve puanları geçerli kazanç kurallarına dayanarak müşterilere kazandırır. Yukarıdaki senaryoda, etkinlik kaydı uygulaması OData API'sini müşteri bilgisini Commerce'a göndermek için çağırır. Ancak, BT kullanıcısı yalnızca atölyeye katılan müşteriler için etkinlik satırlarını deftere nakledebilir ve diğer müşteriler için etkinlik satırlarını silebilir. 

    > [!NOTE]
    > Şu anda, sistem kullanıcıların "diğer etkinlik türleri" için bir numara serisi oluşturmaya zorlar ancak bu gelecekteki sürümler için gerekli bir adım olmayacaktır. Bir numara serisini ayarlamak için **Commerce paylaşılan parametreler** \> **Numara serileri**'ne gidin ve **Bağlılık diğer etkinlik türü kimliği** için bir numara serisi seçin.

- İyi müşteri hizmeti sağlamak ve müşteri profillerini etkin biçimde sorgulamak için kasiyerlerin eksiksiz müşteri profiline tam erişimlerinin olması önemlidr. 10.0 sürümü ile, kasiyerler bağlılık geçmiş ayrıntılarını, ilişkili bağlılık programı ve POS üzerindeki katman bilgisi ile görebileceklerdir.
- Ücretsiz veya indirimli sevkiyat, müşterilerin çevrimiçi satın alması için son derece motive edici temel faktörlerden biridir. Perakendecilerin sevkiyat promosyonlarını ayarlamaları için 10.0 sürümü ile "Sevkiyat eşik indirimi" adlı yeni bir promosyon türü devreye soktuk, burada perakendeci eşikleri tanımlayabilir, bunlara ulaşıldığında, müşterilerin ücretsiz sevkiyat için iskonto verilmesine olanak sağlanır. Örneğin, ücretsiz 'İki günde sevkiyat' için 35$ harcayın veya tüm bağlılık müşterileri için 'İki günde sevkiyat'. Bu özellik, yeni Gelişmiş otomatik masraf yeteneklerini kullanır. [Gelişmiş otomatik masraflar hakkındaki belgeye](/dynamics365/unified-operations/retail/omni-auto-charges) başvurun. Bu gelişmiş otomatik masrafların çalışması için sevkiyat promosyonu için etkinleştirilmesi gerekir. Bunlar, **Müşteri siparişleri** sekmesinden, **Commerce parametreleri** sayfasında etkinleştirilebilir ve "Gelişmiş otomatik masraflar" yapılandırmasını etkinleştirir. Ek olarak, bir perakendeci birden fazla türde gider ayarlayabildiği için örneğin işleme veya kurulum gibi, perakendecinin hangi giderin sevkiyat giderinin olduğunu belirtmesi gerekir. Sevkiyat iskontoları yalnızca sevkiyat masraflarına uygulanır. Masrafı Sevkiyat masrafı olarak belirtmek için **Masraf kodları** formuna gidin, bu **Retail ve Commerce** \> **Retail ve Commerce IT**\> **Kanal kurulumu** \> **Masraflar** altında bulunur ve sonra istenilen masraflar için "Sevkiyat masrafı" onay kutusunu açın. Şimdi **Sevkiyat eşiği iskontosu** formuna gidin ve iskontoyu ayarlayın.

    Ürün iskontolarında olduğu gibi bu iskonto, tüm mevcut standart iskonto yeterliliklerini yerine getirir, örneğin perakendecinin bu iskontoları yalnızca kupona sahip müşterilerin sahip olmasına izin vermek gibi. Ayrıca, bu iskontolar bu tür iskontoların uygunluğunu belirlemek için Fiyat grupları yeterliliğini de kullanır. Örneğin, perakendeci, bu promosyonları yalnızca çevrimiçi kanallarda ve/veya bağlılık müşterileri gibi çeşitli müşteri grupları içinde yürütmeyi seçebilir. Sipariş satırları, belirtilen teslim modu ile belirtilen eşiği karşıladığında, sevkiyat iskontosu uygulanır ve iskonto kuruluma dayalı olarak iskonto giderini azaltır. 

    > [!NOTE]
    > Miktar, basit, karıştır ve eşleştir gibi diğer periyodik iskontoların aksine, sevkiyat iskontosu iskonto satıralrı oluşturmaz, sevkiyat giderlerindeki düzeltmelerin doğrudandır ve iskontonun adını masraf açıklamasına ekler.


[!INCLUDE[footer-include](../includes/footer-banner.md)]