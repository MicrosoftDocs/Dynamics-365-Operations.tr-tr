---
title: Dağıtılmış sipariş yönetimi (DOM)
description: Bu konuda, Dynamics 365 Commerce'da dağıtılmış sipariş yönetimi (DOM) işlevleri açıklanmaktadır.
author: josaw1
ms.date: 01/08/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 52d8b1055517bc544eea6a8e405a8b6d5c0eee0a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356866"
---
# <a name="distributed-order-management-dom"></a>Dağıtılmış sipariş yönetimi (DOM)

[!include [banner](includes/banner.md)]

Ticaret operasyonlarındaki yeni paradigmada, perakendeciler kişiselleştirilmiş müşteri katılımı, çok kanallı deneyimler ve sürtüşmesiz etkileşimler sağlamak için uğraşmaktadır. Çok sayıda seçenek bulunduğundan, tüketiciler en çok istedikleri deneyimi nerede alabileceklerse oradan alışveriş yapacaktır. Çoğu durumda, fiyatlar ve ürünler artık tüketiciler için en önemli karar verme etkenleri değildir.

Perakendeciler, müşteri deneyimini geliştirmek için tüm kanallarında stoklarını gerçek zamanlı olarak görebilmelidir. Tüm stoğa ilişkin tek, bütünsel bir görünüm siparişin yerine getirilmesini iyileştirmeye, tahsisata ve dağıtıma yardımcı olabilir. Bu nedenle, bir dağıtılmış sipariş yönetimi (DOM) sisteminin benimsenip uygulanması, perakendeciler için giderek zorunlu hale gelmektedir.

DOM siparişin yerine getirilmesini, karmaşık bir sistem ve işlem ağında en iyi duruma getirir. Doğru ve daha uygun maliyetli biçimde yerine getirilmeleri için siparişleri akıllıca yönetmek amacıyla tüm kurumda stoğa ilişkin tek, genel bir görünümü esas alır. DOM, perakendecinin tedarik zincirinin verimliliğini iyileştirerek müşteri beklentilerini daha iyi karşılamasına yardımcı olur.

Aşağıdaki resimde bir DOM sistemindeki bir satış siparişinin yaşam döngüsü gösterilmektedir.

![DOM bağlamında satış siparişi yaşam döngüsü.](./media/flow.png "DOM bağlamında satış siparişi yaşam döngüsü")

## <a name="set-up-dom"></a>DOM'u ayarlama

1. **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.
2. **Yapılandırma anahtarları** sekmesinde **Commerce** düğümünü genişletin ve ardından **Dağıtılmış Sipariş Yönetimi** onay kutusunu seçin.
3. **Retail ve Commerce \> Dağıtılmış sipariş yönetimi \> Ayarlar \> DOM parametreleri** bölümüne gidin.
4. **Genel** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Dağıtılmış sipariş yönetimine izin ver**: Bu seçeneği **Evet** olarak ayarlayın.
    - **DOM için Bing Haritalar kullanımını onayla**: Bu seçeneği **Evet** olarak ayarlayın.


        > [!NOTE]
        > Bu seçeneği yalnızca **Commerce'te paylaşılan parametreler** sayfasının (**Retail ve Commerce \> Genel merkez ayarı \> Parametreler \> Commerce'te paylaşılan parametreler**) **Bing Haritalar** sekmesindeki **Bing Haritalar'ı etkinleştir** seçeneği de **Evet** olarak ayarlıysa ve **Bing Haritalar anahtarı** alanına geçerli bir anahtar girildiyse **Evet** olarak ayarlayabilirsiniz.
        >
        > [Bing Haritalar Geliştirme Merkezi](https://www.bingmapsportal.com/) portalı, Bing Haritalar API anahtarlarınızda erişimi, belirttiğiniz bir etki alanı kümesiyle kısıtlamanıza olanak tanır. Bu özellik sayesinde müşteriler, anahtarın doğrulanacağı bir dizi başvuran değeri veya IP adresi aralığı tanımlayabilir. İzin verilenler listenizden gelen istekler normal şekilde işlenirken, listenizin dışından gelen istekler "erişim engellendi" yanıtı döndürür. API anahtarınıza etki alanı güvenliği eklenmesi isteğe bağlıdır ve olduğu gibi bırakılan anahtarlar çalışmaya devam eder. Bir anahtarın izin verilenler listesi, diğer anahtarlarınızın tümünden bağımsızdır ve her anahtarınız için ayrı kurallarınızın olmasını sağlar. Dağıtılmış Sipariş Yönetimi, etki alanı tarafından başvurulan özelliklerin ayarlanmasını desteklemez.


    - **Gün olarak tutma süresi**: DOM çalıştırma işlemlerinin oluşturduğu karşılama planlarının sistemde ne kadar süreyle tutulacağını belirtin. **DOM yerine getirme verileri silme işi ayarı** toplu işi burada belirttiğiniz gün sayısından daha eski olan tüm karşılama planlarını siler.
    - **Reddetme süresi (gün olarak)**: Reddedilen bir sipariş satırının aynı konuma atanabilmesi için ne kadar süre geçmesi gerektiğini belirtin.

5. **Çözücü** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Maks. otomatik karşılama girişimi sayısı**: DOM altyapısının kaç kez bir sipariş satırını bir konuma satmaya çalışacağını belirtin. DOM altyapısı, bir sipariş satırını bir konuma belirtilen girişim sayısı içinde satamazsa sipariş satırını özel durum olarak işaretler. Böylece gelecekteki çalıştırma işlemlerinde durum el ile sıfırlanana kadar bu satırı atlar.
    - **Yerel mağaza bölgesi yarıçapı**: Bir değer girin. Bu alan, konumların nasıl gruplandırılacağını ve uzaklık bakımından nasıl eşit sayılacaklarını belirlemeye yardımcı olur. Örneğin **100** değerini girerseniz karşılama adresinin 100 millik yarıçapı içinde kalan her mağaza veya dağıtım merkezi uzaklık bakımından eşit kabul edilir.
    - **Çözücü türü**: Bir değer seçin. Commerce ile birlikte şu iki çözücü türü kullanıma sunulmuştur: **Üretim Çözücü** ve **Basitleştirilmiş Çözücü**. DOM'un çalıştırılacağı tüm makinelerde (yani DOMBatch grubunun parçası olan tüm sunucularda), **Üretim Çözücü** seçilmelidir. Üretim Çözücü için varsayılan olarak üretim ortamlarında lisanslanıp dağıtılan özel lisans anahtarı gereklidir. Bu lisans anahtarı, üretim dışı ortamlarda el ile dağıtılmalıdır. Lisans anahtarını el ile kurmak için şu adımları izleyin:

        1. Microsoft Dynamics Lifecycle Services'ta Paylaşılan varlık kitaplığını açıp varlık türü olarak **Model**'i seçin ve **DOM lisansı** dosyasını indirin.
        1. Microsoft Internet Information Services (IIS) Yöneticisi'ni başlatın, **AOSService web sitesi**'ne sağ tıklayın ve ardından **Keşfet**'i seçin. **\<AOS service root\>\\ webroot**'ta bir Windows Gezgini penceresi açılır. Sonraki adımda kullanacağınızdan \<AOS Service root\> yolunu not edin.
        1. **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin** dizinindeki yapılandırma dosyasını kopyalayın.
        1. Genel Merkez istemcisine gidin ve **DOM parametreleri** sayfasını açın. **Çözücü** sekmesinde, **Çözücü türü** alanında, **Üretim çözücü**' seçeneğini belirleyin ve hiçbir hata iletisi görünmediğinden emin olun.


        > [!NOTE]
        > Basitleştirilmiş Çözücü, perakendecilerin özel lisans kurmak zorunda kalmadan DOM özelliğini deneyebilmeleri için sunulmuştur. Kurumlar Basitleştirilmiş Çözücüyü üretim ortamlarında kullanmamalıdır.
        >
        > Üretim Çözücü performansı (bir çalıştırma işleminde işlenebilecek sipariş ve sipariş satırı sayısı gibi) ve sonuçların yakınsaması (bazı senaryolarda bir sipariş toplu işi en iyi sonuçları vermeyebileceği için) artırır. **Kısmi siparişler** kuralı ve **Maksimum konum sayısı** kuralı gibi bazı kurallar Üretim Çözücü gerektirir.
     
6. **Retail ve Commerce \> Dağıtılmış sipariş yönetimi \> Ayarlar \> DOM parametreleri** bölümüne dönün.
7. **Numara serileri** sekmesinde, gerekli numara serilerini çeşitli DOM varlıklarına atayın.

    > [!NOTE]
    > Numara serilerinin varlıklara atanabilmesi için, bu seriler **Numara serileri** sayfasında (**Kurum yönetimi \> Numara serileri \> Numara serileri**) tanımlanmalıdır.

8. DOM özelliği çeşitli DOM kuralları türlerinin tanımlanmasını destekler ve kurumlar iş ihtiyaçlarına bağlı olarak birden fazla kural yapılandırabilir. DOM kuralları, bir konum grubu veya tek konum ve belirli bir ürün, kategori veya çeşit için tanımlanabilir. DOM kuralları için kullanılması gereken konumların gruplandırmasını oluşturmak isterseniz şu adımları izleyin:

    1. **Retail ve Commerce \> Kanal kurulumu \> Karşılama grupları**'na gidin.
    2. **Yeni**'yi seçin ve yeni grup için bir ad ve açıklama girin.
    3. **Kaydet**'i seçin.
    4. Gruba tek bir yerleşim eklemek için **Satır ekle**'yi seçin. Alternatif olarak, birden fazla yerleşim eklemek için **Satırlar ekle**'yi seçin.
    
    > [!NOTE]
    > Commerce 10.0.12 ve üstü sürümlerde, **Karşılama grubunda yerleşimleri 'Sevkiyat' veya 'Malzeme çekme' etkin olarak belirtme özelliği**, **Özellik Yönetimi** çalışma alanında etkinleştirilmelidir.
    >
    > Bu özellik, **Karşılama grubu** sayfasına yeni yapılandırmalar ekleyerek, ambarın sevkiyat için kullanılıp kullanılamayacağını veya ambar/mağaza birleşiminin sevkiyat, malzeme çekme veya her ikisi için kullanılıp kullanılamayacağını tanımlamanızı sağlar. 
    >
    > Özelliği etkinleştirirseniz, POS'ta malzeme çekme veya sevkiyat emirleri oluşturduğunuzda yerleşim seçimi için kullanılabilir olan seçenekler güncelleştirilir.
    >
    > Ayrıca, bu özelliğin "tümünü sevk et" veya "seçileni sevk et" işlemleri seçildiğinde etkinleştirilmesi, POS'taki sayfaların güncelleştirilmesine neden olur.

9. Kuralları tanımlamak için **Retail ve Commerce \> Dağıtılmış sipariş yönetimi \> Ayarlar \> Kuralları yönet**'e gidin. Şu anda aşağıdaki DOM kuralları desteklenmektedir:

    - **Minimum stok kuralı**: Bu kural türü, kurumların bir ürünün belirli bir miktarını sipariş karşılama dışındaki amaçlar için "korumasını" sağlar. Örneğin, kurumlar DOM'nin bir mağazada bulunan tüm stoğu sipariş karşılama için dikkate almasını istemeyebilir. Bunun yerine, kapı müşterileri için biraz stok ayırmak isteyebilirler. Bu kural türü kullanıldığında, bir ürün kategorisi, tek bir ürün ya da konuma veya konum grubuna göre bir ürün çeşidi için tutulacak minimum stoğu tanımlayabilirsiniz.
    - **Karşılama konumu önceliği kuralı**: Bu kural türü, kurumların DOM altyapısının belirli ürünler için karşılama konumları tanımlamaya çalışırken dikkate aldığı önceliği belirlemek için bir konum hiyerarşisi belirlemelerini sağlar. Geçerli öncelik aralığı 1-10'dur. Burada 1 en yüksek, 10 ise en düşük önceliktir. Daha yüksek önceliğe sahip konumlar daha düşük önceliğe sahip önce konumlardan önce dikkate alınır. Kural, sabit bir kısıtlama kuralı olarak tanımlanırsa siparişler yalnızca önceliklerin tanımlandığı konumlara satılır.
    - **Kısmi siparişler kuralı**: Bu kural, kurumların siparişin mi yoksa sipariş satırlarının mı kısmen karşılanabileceğini belirlemelerine olanak tanır. Aşağıdaki parametreler kullanılabilir:

        - **Kısmi siparişler karşılansın mı?** – Bu seçenek **Evet** olarak ayarlanırsa DOM yalnızca bir sipariş satırındaki miktarın bir kısmını karşılayabilir. Bu kısmi karşılama, sipariş satırı bölünerek sağlanır.
        - **Kısmi satırlar karşılansın mı?** – Bu seçenek **Evet** olarak ayarlanırsa DOM sipariş satırlarının kısmi bir miktarını karşılayabilir. Bu kısmi karşılama, sipariş satırı bölünerek sağlanır.
        - **Siparişi yalnızca bir konumdan karşıla**: Bu seçenek **Evet** olarak ayarlanırsa DOM, bir siparişteki tüm satırların tek bir konumdan karşılanmasını sağlar.


        Aşağıdaki tabloda, bu parametrelerin bir birleşimi tanımlandığında görülen davranış açıklanmaktadır.

        | Birleşim numarası | Kısmi siparişleri karşıla | Kısmi satırları karşıla | Siparişi tek bir konumdan karşıla | Tanım |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | Evet                    | Evet                   | Evet                                  | Siparişin birkaç satırı karşılanabilir ve tek satırlar kısmen karşılanabilir, ancak DOM çalıştırma işleminin bir örneğinde tüm satırlar aynı konuma ait olmalıdır. (Bu birleşim şu anda desteklenmemektedir.) |
        | 2    | Evet                    | Hayır                    | Evet                                  | Siparişin birkaç satırı karşılanabilir, ancak tek satırlar kısmen karşılanamaz ve DOM çalıştırma işleminin bir örneğinde karşılanan tüm satırlar aynı konuma ait olmalıdır. (Bu birleşim şu anda desteklenmemektedir.) |
        | 3    | Evet                    | Evet                   | Hayır                                   | Siparişin birkaç satırı karşılanabilir, tek satırlar kısmen karşılanabilir ve her satır, DOM çalıştırma işleminin bir örneğindeki bir konumdan karşılanabilir. |
        | 4\*  | Hayır                     | Uygulanamaz        | Hayır                                   | Tüm sipariş satırları karşılanmalıdır, tek satırlar kısmen karşılanamaz ve her sipariş satırı farklı bir konumdan karşılanabilir. |
        | 5\*  | Hayır                     | Uygulanamaz        | Evet                                  | Tüm sipariş satırları karşılanmalıdır, tek satırlar kısmen karşılanamaz ve tüm sipariş satırları yalnızca bir konumdan sağlanabilir. |
        | 6\*  | Hayır                     | Uygulanamaz        | Hayır                                   | Bu kombinasyon, kombinasyon 4 gibi çalışır, çünkü **Kısmi satırları karşıla**, **Kısmi siparişleri karşıla** **Hayır** olarak ayarlıyken **Evet** olarak ayarlanamaz. |
        | 7\*  | Hayır                     | Uygulanamaz        | Evet                                  | Bu kombinasyon, kombinasyon 5 gibi çalışır, çünkü **Kısmi satırları karşıla**, **Kısmi siparişleri karşıla** **Hayır**'ken **Evet** olamaz. |
        | 8    | Evet                    | Hayır                    | Hayır                                   | Siparişin birkaç satırı karşılanabilir, ancak tek satırlar kısmen karşılanamaz ve çeşitli sipariş satırları, DOM çalıştırma işleminin bir örneğindeki bir konumdan karşılanabilir. |
        | 9\*  | Hayır                     | Uygulanamaz        | Evet                                  | Tüm sipariş satırları karşılanmalı ve tüm sipariş satırları yalnızca tek bir konumdan karşılanmalıdır. |

        \* **Kısmi siparişleri karşıla** **Hayır** olarak ayarlıysa **Kısmi satırları karşıla**, aslında nasıl ayarlandığından bağımsız olarak her zaman **Hayır**'a ayarlı olarak kabul edilir.

        > [!NOTE]
        > Retail 10.0.5 sürümünde, **Siparişi yalnızca bir yerleşimden karşıla** parametresi **Maksimum karşılama yerleşimleri** olarak değiştirildi. Kullanıcılar siparişlerin yalnızca bir konumdan mı, yoksa mümkün olduğunca çok sayıda konumdan mı karşılanacağını yapılandırma olanağını kullanmak yerine artık karşılamanın belirli bir konum kümesinden mi (en fazla 5) yoksa mümkün olduğunca çok sayıda konumdan mı karşılanacağını belirtebilir. Bu özellik, siparişin karşılanabileceği konum sayısı açısından daha fazla esneklik sunar. Bu kural yalnızca Üretim Çözücü ile çalışır. 

   - **Çevrimdışı karşılama konumu kuralı**: Bu kural, kurumların bir konumu veya konum grubunu çevrim dışı ya da DOM için kullanılamaz olarak belirtmelerini sağlar, böylece siparişler karşılama için bu konumlara atanamaz.
    - **Maksimum reddetme sayısı kuralı**: Bu kural, kurumların reddetme işlemleri için bir eşik tanımlamasını sağlar. Eşiğe ulaşıldığında, DOM işlemcisi bir siparişi veya sipariş satırını özel durum olarak işaretler ve diğer işlemlerde hariç tutar.

        Sipariş satırları bir konuma atandıktan sonra, konum atanan bir sipariş satırını reddedebilir, çünkü bazı nedenlerle söz konusu satırı karşılayamıyor olabilir. Reddedilen satırlar özel durum olarak işaretlenir ve sonraki çalıştırmada işlenmeleri için yeniden havuza eklenir. DOM, sonraki çalışma sırasında reddedilen satırı farklı bir konuma atamayı dener. Yeni konum da atanan sipariş satırını reddedebilir. Bu atama ve reddetme çevrimi birkaç kez meydana gelebilir. Reddetme sayısı tanımlanan eşiğe ulaştığında, DOM sipariş satırını kalıcı özel durum olarak işaretler ve satırı yeniden atama için seçmez. DOM, sipariş satırını yalnızca bir kullanıcı sipariş satırının durumunu sıfırlarsa yeniden atama için dikkate alır.

   - **Maksimum mesafe kuralı**: Bu kural, kurumların bir konumun veya konum grubunun siparişi karşılamak için bulunabileceği maksimum uzaklığı tanımlamasını sağlar. Bir konum için çakışan maksimum uzaklık kuralları tanımlandıysa DOM söz konusu konum için tanımlanan en düşük maksimum uzaklığı uygular.
    - **Maksimum siparişler kuralı**: Bu kural, kurumların bir konumun veya konum grubunun bir takvim günü boyunca işleyebileceği maksimum sipariş sayısını tanımlamasını sağlar. Bir konuma tek bir günde maksimum sipariş sayısı atandıysa DOM, takvim gününün kalanı boyunca söz konusu konuma başka sipariş atamaz.

   Tüm önceki kural türleri için tanımlanabilecek ortak özniteliklerin bazıları aşağıdadır:

   - **Başlangıç tarihi** ve **Bitiş tarihi**: Her kural bu alanlar kullanılarak tarih açısından etkin hale getirilebilir.
   - **Devre Dışı**: Bir DOM çalıştırma işleminde bu alan için yalnızca **Hayır** değerine sahip kurallar dikkate alınır.
   - **Sabit sınırlama**: Bir kural, sabit kısıtlama veya sabit kısıtlama değil olarak tanımlanabilir. Her DOM çalıştırma işlemi, iki kez tekrarlanır. İlk tekrarda, her kurala bu alanın ayarından bağımsız olarak sabit kısıtlama olarak işlem yapılır. Başka bir deyişle, her kural uygulanır. Tek özel durum, **Konumu önceliği** kuralıdır. İkinci tekrarda, sabit kısıtlama olarak tanımlanmayan kurallar kaldırılır ve tüm kurallar uygulandığında konumlara atanmayan sipariş veya sipariş satırları konumlara atanır.

10. Karşılama profilleri bir kural, tüzel kişilik, satış siparişi menşeleri ve teslimat şekilleri koleksiyonunu gruplandırmak için kullanılır. Her DOM çalıştırma işlemi, belirli bir karşılama profiline yöneliktir. Kurumlar, bu şekilde belirli satış siparişi menşeleri ve teslimat şekillerine sahip siparişlerde bir tüzel kişilik kümesi için bir dizi kural tanımlayıp çalıştırabilir. Bu nedenle, farklı satış siparişi menşeleri ve teslimat şekilleri kümeleri için farklı kural dizileri çalıştırılması gerekiyorsa karşılama profilleri buna göre tanımlanabilir. Karşılama profillerini ayarlamak için aşağıdaki adımları takip edin:  

    1. **Retail ve Commerce \> Dağıtılmış sipariş yönetimi \> Ayarlar \> Karşılama profilleri** bölümüne gidin.
    2. **Yeni**'yi seçin.
    3. **Profil** ve **Açıklama** alanlarına değer girin.
    4. **Sonucu otomatik olarak uygula** seçeneğini ayarlayın. Bu seçeneği **Evet** olarak ayarlarsanız profil için DOM çalıştırma işleminin sonuçları otomatik olarak satış siparişi satırlarına uygulanır. Bunu **Hayır** olarak ayarlarsanız sonuçlar yalnızca karşılama planında görüntülenebilir. Satış siparişi satırlarına uygulanmaz.
    5. DOM profilinin, satış siparişi menşeinin tanımlı olmadığı siparişler dahil her satış siparişi menşeine sahip siparişler için çalıştırılmasını istiyorsanız **Boş satış menşeine sahip siparişleri işle** seçeneğini **Evet** olarak ayarlayın. Profili yalnızca birkaç satış siparişi menşei için çalıştırmak isterseniz, bunları daha sonra açıklandığı gibi **Satış menşeleri** sayfasında tanımlayabilirsiniz.

    > [!NOTE]
    > Commerce 10.0.12 ve üstü sürümlerde, **Karşılama Profiline Karşılama grubu atama özelliği** **Özellik Yönetimi** çalışma alanında etkinleştirilmelidir. 
    >
    > Bu özellik, **Karşılama profili** sayfasına, tek bir karşılama grubuyla ilişkilendirilebilecek yeni bir yapılandırma ekler. 
    >
    > Karşılama grubunu seçerseniz, bu karşılama profilinin DOM kuralları, karşılama grubuna dahil edilen "sevkiyat" ambarları için etkili şekilde çalışacaktır. 
    > 
    > Bu özelliği etkin şekilde kullanmak için, tüm sevkiyat ambarlarını içeren tek bir karşılama grubu olduğundan emin olun ve sonra bu karşılama grubunu karşılama profiliyle ilişkilendirin.
    
    6. **Tüzel kişilikler** hızlı sekmesinde, **Ekle**'yi seçin ve ardından bir tüzel kişilik seçin.
    7. **Kurallar** hızlı sekmesinde, **Ekle**'yi seçin ve ardından profille ilişkilendirilecek kuralı seçin.
    8. Tüm gerekli kurallar profille ilişkilendirilene kadar önceki iki adımı yineleyin.
    9. **Kaydet**'i seçin.
    10. Eylem Bölmesi'ndeki **Ayar** sekmesinde, **Teslimat şekilleri**'ni seçin.
    11. **Teslimat şekilleri** sayfasında, **Yeni**'yi seçin.
    12. **Şirket** alanında, tüzel kişiliği seçin. Şirket listesi daha önce eklediğiniz tüzel kişiliklerle sınırlıdır.
    13. **Teslimat şekli** alanında, bu profille ilişkilendirilecek teslimat şeklini seçin. Bir teslimat şekli, birden fazla etkin profille ilişkilendirilemez.
    14. Tüm gerekli teslimat şekilleri profille ilişkilendirilene kadar önceki iki adımı yineleyin.
    15. **Teslimat şekilleri** sayfasını kapatın.
    16. Eylem Bölmesi'ndeki **Ayar** sekmesinde, **Satış siparişi menşeleri**'ni seçin.
    17. **Satış menşeleri** sayfasında, **Yeni**'yi seçin.
    18. **Şirket** alanında, tüzel kişiliği seçin. Şirket listesi daha önce eklediğiniz tüzel kişiliklerle sınırlıdır.
    19. **Satış menşesi** alanında, bu profille ilişkilendirilecek satış menşesini seçin. Bir satış menşesi, birden fazla etkin profille ilişkilendirilemez.
    20. Tüm gerekli satış menşeleri profille ilişkilendirilene kadar önceki iki adımı yineleyin.
    21. **Satış menşeleri** sayfasını kapatın.
    22. **Profili etkinleştir** seçeneğini **Evet** olarak ayarlayın. Ayarda hata varsa bir uyarı iletisi alırsınız.

## <a name="dom-processing"></a>DOM işleme

DOM yalnızca bir toplu işte çalışır. DOM çalıştırma işlemleri için toplu işi yapılandırmak üzere bu adımları izleyin.

1. **Retail ve Commerce \> Dağıtılmış sipariş yönetimi \> Toplu işleme \> DOM işlemcisi iş ayarı**'na gidin.
1. **Parametreler** hızlı sekmesindeki **Karşılama profili** alanında, DOM'nin çalıştırılması gereken bir profil seçin.
1. **Arka planda çalıştır** hızlı sekmesindeki **Toplu iş grubu** alanında, yapılandırılmış bir toplu iş grubu seçin.
1. **Görev açıklaması** alanında, toplu iş için bir ad girin.
1. **Yinelenme**'yi seçin ve toplu işin yinelenmesini tanımlayın.
1. **Tamam**'ı seçin.

DOM, işleme anında sipariş ve sipariş satırlarını burada açıklandığı gibi dikkate alır:

- DOM profilinde tanımlandığı gibi satış siparişi menşeleri, teslimat şekilleri, tüzel kişilik için ölçütleri ve aynı zamanda aşağıdaki ölçütlerden herhangi birini karşılayan sipariş satırları:

    - Ticari kanallardan oluşturulurlar.
    - Asla DOM tarafından satılmamışlardır.
    - Daha önce DOM tarafından satılmamışlardır, ancak özel durum olarak işaretlenmişlerdir ve maksimum girişim eşiğinin altındadırlar.
    - Teslimat şekli, teslim alma veya elektronik teslimat değildir.
    - Teslimat için işaretlenmemişlerdir.
    - El ile hariç tutulmamışlardır.

- Beklemede olmayan siparişler

DOM kuralları, stok kısıtlamalarını ve iyileştirmeleri uyguladıktan sonra müşterinin teslimat adresine en yakın konumu seçer.

![Satış siparişi ölçütü.](./media/ordercriteria.png "Satış siparişi ölçütü")

## <a name="results-of-dom-runs"></a>DOM çalıştırma işlemlerinin sonuçları

Karşılama profili **Otomatik olarak uygula** şeklinde ayarlandığında, çalıştırma işleminin sonuçları otomatik olarak satış siparişi satırlarına uygulanır ve karşılama planı ayrı olarak görüntülenebilir. Bununla birlikte, karşılama profili **Otomatik olarak uygula** şeklinde ayarlanmamışsa çalıştırma işleminin sonuçları yalnızca karşılama planı görünümden görülebilir. 

Oluşturulan tüm karşılama planlarını görüntülemek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Dağıtılmış sipariş yönetimi \> Dağıtılmış sipariş yönetimi** bölümüne gidin.
2. **Dağıtılmış sipariş yönetimi** çalışma alanında, **Karşılama Planları** kutucuğunu seçin.
3. Karşılama planını görüntülemek için ilgili sipariş karşılama planının kimliğini seçin.

    Karşılama planının sipariş ayrıntıları bölümü çalıştırma işleminin parçası olan orijinal satış siparişi satırlarını gösterir. Sipariş ayrıntıları bölümü, standart satış siparişi satırı alanının yanı sıra aşağıdaki DOM ile ilgili üç alanı da içerir:

    - **Karşılama türü**: Bu alan satış siparişi satırının tam olarak satıldığını, kısmen kullanıldığını veya bir konuma hiç satılmadığını gösterir.
    - **Böl**: Bu alan, bir adet satış satırının bölünerek farklı konumlara satılıp satılmadığı gösterir.
    - **Karşılama konumu sayısı**: Bu alan, bir adet satış siparişi satırı için kaç karşılama satırı oluşturulduğunu (özgün satış siparişinin satıldığı konumların sayısına göre) gösterir.

    Sipariş karşılama ayrıntıları bölümü, orijinal satış siparişi satırlarının miktarlarıyla birlikte farklı konumlara atanmasını gösterir.

## <a name="order-line-actions-and-statuses"></a>Sipariş satırı eylemleri ve durumları

Aşağıda, sipariş satırındaki ayarlar açıklanmaktadır. Sipariş satırını açmak için **Retail ve Commerce \> Müşteriler \> Tüm satış siparişleri** bölümüne gidin.
- Satış siparişi satırının **Genel** sekmesindeki **DOM işlemlerinden hariç tut** seçeneğini **Evet** olarak ayarlarsanız sipariş veya sipariş satırı DOM işlemlerinde hariç tutulur.
- Satış siparişi satırının **Genel** sekmesindeki **DOM durumu** alanı aşağıdaki değerlerden birine ayarlanabilir:

    - **Hiçbiri**: Sipariş satırı hiçbir zaman satılmamıştır.
    - **Tam**: Sipariş satırı başarıyla satılarak bir konuma atanmıştır.
    - **Özel durum**: Sipariş satırı başarıyla satılmış ancak bir konuma atanamamaktadır. Özel durumların DOM çalışma alanından görüntülenebilen birden fazla alt türü vardır:

        - **Kullanılabilir miktar yok**: Siparişi konumlara atamak için kullanılabilir stok yoktur.
        - **Maksimum reddetme sayısı**: Sipariş satırı, maksimum reddi sayısı eşiğine ulaşmıştır.
        - **Veri değişikliği çakışması**: Satış siparişi satırı, sipariş satıldıktan sonra değiştirilmiştir. Bu nedenle, karşılama planı siparişe uygulanamaz.
        - **Sipariş satırına özgü özel durum**: Sipariş satırında birden çok özel durum vardır.

- Satış sipariş girişi sırasında DOM etkileşimli bir modda çalışır. Ürün ve miktarı belirttikten sonra bir sipariş satırı olarak girerken **Satırı güncelleştir**'i ve ardından **DOM**'nin altından **Karşılama konumu öner**'i seçin. Daha sonra sipariş satırında miktarı gerçekleştirebilecek DOM kurallarını temel alan konumların listesini görebilirsiniz. Bu liste uzaklığa göre sıralanır. Satış siparişi satırında ilgili tesisi ve ambarı ayarlamak için bir konum seçin. Bu işlevin çalışması için, satış satırında satış menşesi ve teslimat şekliyle eşleşen var olan, etkin bir karşılama profili olmalıdır.
- Bir satış siparişi satırı için DOM çalıştırma günlüklerini görüntülemek amacıyla **Satış siparişi satırı**'nı seçin ve ardından **DOM**'nin altından **DOM Günlüklerini Görüntüle**'yi seçin. DOM günlükleri, DOM çalıştırma işlemi tarafından oluşturulan tüm olayları ve günlükleri gösterir. Günlükler, belirli bir konumun sipariş satırına neden atandığını ve hangi kısıtlamaları ile kuralların atamanın parçası olarak dikkate alındığını anlamanıza yardımcı olabilir. **Yönet** sekmesinde, DOM günlükleri de satış siparişi başlığı düzeyinde kullanılabilir.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>DOM karşılama planları için bir temizleme işi çalıştırma

DOM işlemi çalıştırılırken, karşılama planları oluşturulur. Sistem, zaman içinde çok sayıda karşılama planını saklar. Sistemin sakladığı karşılama planı sayısını yönetmek için **Gün olarak tutma dönemi** değerine göre eski karşılama planlarını silen bir toplu iş yapılandırabilirsiniz.

1. **Retail ve Commerce \> Dağıtılmış sipariş yönetimi \> Toplu işleme \> DOM karşılama verilerini silme işi ayarı** bölümüne gidin. 
1. **Toplu iş grubu** alanında, yapılandırılmış bir toplu iş grubu seçin.
1. **Yinelenme**'yi seçin ve toplu işin yinelenmesini tanımlayın.
1. **Tamam**'ı seçin.

## <a name="more-information"></a>Daha fazla bilgi

DOM özelliğini kullanırken dikkate almanız gereken bazı noktalar aşağıda belirtilmiştir:

- DOM şu anda yalnızca ticari kanallardan oluşturulan siparişlere bakmaktadır. Satış siparişleri, **Ticari satış** seçeneği **Evet** olarak ayarlandığında ticari satış siparişleri olarak tanımlanır.
- Microsoft, DOM'yi ileri düzey ambar yönetimi özellikleriyle test etmemiştir. Müşteriler ve iş ortakları, DOM'nin ileri düzey ambar yönetimi özellikleri ve bunlara ilgili işlemlerle uyumlu olup olmadığını belirlemek için dikkatli olmalıdır.
- DOM, yalnızca Commerce'in bulut sürümünde kullanılabilir. Şirket içi dağıtımlarda desteklenmez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]