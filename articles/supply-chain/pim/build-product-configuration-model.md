---
title: "Ürün konfigürasyon modeli oluşturun"
description: "Ürünleri özel gereksinimleri karşılamak üzere yapılandırma gerekliliği hem işletmeden işletmeye hem de hem işletme-müşteri ilişkilerinde istisna yerine bir kural haline gelmektedir."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b096f366f13406a4c80d7eccfa8f27d8f8f712e4
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="build-a-product-configuration-model"></a>Ürün konfigürasyon modeli oluşturun

[!include[banner](../includes/banner.md)]


Ürünleri özel gereksinimleri karşılamak üzere yapılandırma gerekliliği hem işletmeden işletmeye hem de hem işletme-müşteri ilişkilerinde istisna yerine bir kural haline gelmektedir.

Sipariş ile yapılandırmak senaryoları destekleyen üretici müşteri gereksinimlerine göre daha dikkatli eğilimindedir için bir fırsat vardır. Ayrıca, Yarı Mamul mallar yerine Bitmiş ürünün genel bileşenleri biçiminde tutularak üretici stoğa bağlı sermayeyi azaltabilir.  

Üretimi hisse senedi kurulumundan yapılandırma siparişi kurulumuna başarılı bir taşıma ürün yapılarının dikkatli analizini, ürün ailelerinin tanımlanması ve bileşenleştirme gerektirir. Bölümlerinin sayısını azaltmak ve Hazırlanmakta olan mal sayısını en aza indirmek için ürün arabirimleri anlamak ve yeniden kullanılabilirlik için tasarım büyük önem taşımaktadır.  

Birkaç ürün yapılandırma modelleme ilkesi vardır, kural tabanlı, boyut tabanlı ve kısıtlama tabanlı modelleme gibi. Çalışmalar karşılaştırıldığında diğer modelleme ilkelerine göre kısıtlama tabanlı Metodoloji modellerinde kod satır sayısını yaklaşık yüzde 50 azaltabilir gösterir. Bu nedenle, bu yöntem toplam maliyetini (TCO) sahipliği azaltabilir. X ++ kodunu temel alan kural tabanlı Kısıtlama tabanlı modelin kısıtlama tabanlı modele taşıyarak, artık ürün modellerini korumak için bir geliştirici lisans gerekli değildir.

## <a name="product-configuration"></a>Ürün yapılandırması
Endüstrileşme dönemi için uygun fiyata yüksek kalitede ve zengin özellikli ürünler üretme içinde harika başarılar neden olmuştur. Ölçek ekonomileri endüstriyelleşmiş dünyada çoğumuzun gündelik yaşamın gerekli bir parçası olduğunu düşündüğü arabalar, TV'ler, ev aletleri ve diğer malları almasını sağlamıştır.  

Birçok ürün ticari mallar duruma geldikçe bunları ayırt etme gereği oluşmuştur. Üreticilerin bu zorluğa hemen yanıtı, müşterilerin alternatifi olacak şekilde her ürünün varyantını oluşturmak olmuştur. Bu strateji, artan tahmin zorlukları ve ayrıca stok maliyeti ve ortadan kalkacak satılmamış ürünlerde artışa neden olmuştur.  

Yapılandırma sipariş felsefesi kabul ederek, üreticilerin azaltma veya eski stok maddeleri ortadan kaldırılması sırasında benzersiz ürünler için Müşteri talebi karşılamak için fırsatı vardır. Üretim-hisse senedi felsefesi yapılandır-sipariş felsefesine kaydığında, ortaya çıkan bir zorluk kısa sağlama sürelerinin düşük stok düzeyleriyle dengeli olması ihtiyacıdır.  

Burada başarı için anahtar ürün yelpazesi dikkatle analiz etmek ve ürün özellikleri ve işlemlerinde modelleri aramaktır. Hedef, aynı ekipmanı tarafından üretilen ve tüm çeşitlerde kullanılan genel bileşenleri tanımlamaktır.  

Yeni ürün yapılandırma özelliği kümesi ürün yapılandırma modeli yapısına görsel genel bakış sağlayan bir kullanıcı arabirimi (UI) ve ayrıca derlenmek zorunda olmayan tanımlayıcı bir kısıtlama sözdizimi içerir. Bu nedenle, bir yapılandırma yöntemi desteklemek isteyen şirketler daha kolay başlayabilir. Aşağıdaki bölümlerde anlatıldığı şekilde bir ürün Tasarımcısı artık ürün yapılandırma modeli oluşturmak, sınamak ve Satış organizasyonunu için yayın için geliştirici desteği gerektirmez.

## <a name="building-a-product-configuration-model"></a>Ürün konfigürasyon modeli oluşturma
Bir kullanıcı bir ürün yapılandırma modeli oluşturmak için gerçekleştirebileceği çeşitli yaklaşımlar vardır. Bir seçenek tüm başvuru verilerini, ürün yöneticileri, farklı ürünler ve operasyonel kaynaklar gibi ilk oluşturarak ve sonra bunları bileşen, ürün reçetesi (BOM) satırlarını rota operasyonları ve diğer ürün yapılandırma modeli öğeleri olarak dahil ederek bir Sıralı Akış izlemektir. Alternatif olarak, önce model oluşturma ve daha sonra gerektiğinde başvuru veri ekleyerek daha yinelemeli bir yaklaşım seçebilirsiniz.

### <a name="components"></a>Bileşenler

Ürün yapılandırma modeli alt bileşen ilişkileri birbirine bağlı bir veya daha fazla bileşenden oluşur. Bileşenleri bir kez tanımlanır ve sonra bir veya daha fazla ürün yapılandırma modellerinde birçok kez kullanılabilir. Ürün yapılandırma modelinin ana yapı taşları bileşenlerdir ve modeli hakkında bilgi neredeyse tüm bunlarla ilgilidir.

### <a name="attributes"></a>Öznitelikler

Her bileşen özelliklerini tanımlayan bir veya daha fazla özniteliklere sahiptir. Öznitelikler yapılandırma işlemi sırasında kullanıcının seçtikleridir. Öznitelikler sınırlamaları veya hesaplamalarda eklemeler sayesinde bileşen arası ve bileşen içi ilişkilerini kontrol eder. Ürün reçetesi satırları için uygulanan koşullar aracılığıyla öznitelikler yapılandırılan ürünün hangi fiziksel bölümleri içereceğini belirlemek için kullanılabilir. Ayrıca, bir öznitelik bir eşleme mekanizması aracılığıyla bir ürün reçetesi satırının özelliğini denetleyebilir. Ekleme ve özellik ayarlarıyla ilgili rota operasyonları için benzer işlevsellik vardır.

### <a name="expression-constraints"></a>İfade kısıtlamaları

Kısıtlama tabanlı ürün yapılandırma model kullanımı kullanıcı çeşitli öznitelikler için değerler seçtiğinde bazı sınırlamalar var anlamına gelir. En iyi duruma getirme Modelleme Dili (OML) kullanarak deyim kısıtlamaları olarak bu tür sınırlamalar uygulanabilir. Alternatif olarak, bir kısıtlama bir tablo kısıtlaması şeklinde uygulanabilir.

### <a name="table-constraints"></a>Tablo sınırlamaları

Tablo kısıtlamaları kullanıcı veya sistem tanımlı olabilir.  

Bir kullanıcı tanımlı tablo kısıtlaması kullanıcı tarafından üretilmiştir. Kullanıcı tablonun sütunları göstermek için öznitelik türleri birleşimini seçer ve sonra satır içinde tablo kısıtlaması oluşturmak için seçili öznitelik türlerinin etki alanlarındaki değerleri girer.  

Bir sistem tanımlı tablo kısıtlaması hangi Microsoft Dynamics 365 for Finance and Operations tablosunun başvuru olarak kullanılacağını seçerek ve sonra kısıtlamada sütunlar oluşturmak için bu tablodan alanları seçerek tanımlanır. Tablo kısıtlaması satırları, yapılandırma sırasında mevcut Finance and Operations tablosu satırlarıdır.  

Bir tablo kısıtlaması tablo kısıtlaması tanımına referans vererek ve modelde ilgili öznitelikleri tablo kısıtlamasındaki sütunlara eşleyerek bir ürün yapılandırma modeline dahil edilir.

### <a name="calculations"></a>Hesaplamalar

Hesaplamalar bir yapılandırma modelinde aritmetik işlemleri gerçekleştirmek için bir mekanizmayı temsil eder. Örneğin, bir hesaplama belirli bir hammadde parçasının uzunluğunu veya polishing bir operasyon için işlem süresini belirleyebilir. Hesaplamalar zorunludur ve hesaplama ifadesine dahil edilen tüm öznitelik değerleri kullanılabilir olduktan sonra hedef öznitelik için değer belirler.

### <a name="subcomponents"></a>Alt bileşenler

Alt bileşenler ürün yapılandırma modeli yapısındaki düğümleri temsil eder. Her alt bileşen ilişkisi için, referans kısıtlama tabanlı yapılandırmaya ayarlanan varyant yapılandırma teknolojisine sahip bir ana ürün belirtilmelidir.

### <a name="user-requirements"></a>Kullanıcı gereksinimleri

Bir kullanıcı gereksinimin tüm alt bileşen oluşturucuları vardır. Tek fark, kullanıcı gereksiniminin bir ana ürüne bağlı olmamasıdır. Bu farkın pratik etkisi tüm ürün reçetesi satırlarını veya kullanıcı gereksinimi bağlamında tanımlanan rota operasyonunu ana bileşen ürün reçetesi yapısı veya rotasına daraltmasıdır. Bu davranış, bir hayali ürün reçetesi davranışına benzer.

### <a name="bom-lines"></a>Ürün reçetesi satırları

Ürün reçetesi satırları her bileşen için ürün reçetesi üretimini tanımlamak için dahil edilmiştir. Bir ürün reçetesi satırı bir öğeye referans vermelidir ve tüm öğe özellikleri sabit bir değere ayarlanabilir veya bir özniteliğe eşleştirilebilir.

### <a name="route-operations"></a>Rota işlemleri

Üretim rotası tanımlamak için rota operasyonları eklenmiştir. Rota operasyonu tanımlanan bir işleme referans vermelidir ve tüm işlem özellikleri sabit bir değere ayarlanabilir. Kaynak gereksinimleri hariç tüm özellikler bir değer yerine bir özniteliğe eşlenebilir.

## <a name="validating-and-testing-a-product-configuration-model"></a>Ürün yapılandırma model doğrulama ve test etme
Ürün yapılandırma modelinin doğrulaması modelin birkaç düzeyinde oluşabilir ve bu nedenle çeşitli kapsamları kapsayabilir. En düşük düzeyi için bir tek ifade kısıtlaması içindir. Bu durumda, doğrulama ifade sözdiziminin doğru olduğunu doğrulamak için genellikle ürün tasarımcısı tarafından gerçekleştirilir.  

Benzer şekilde, bir ürün reçetesi satırı veya Rota operasyonu için bir koşul yalıtım modunda doğrulanabilir.  

Doğrulama bir kullanıcı tanımlı tablo kısıtlaması tanımı için de yapılabilir. Bu durumda, kullanıcı her alan için girilen değerlerin ilgili öznitelik türlerinin etki alanı içinde olduğunu doğrulayabilir.  

Son olarak, bir tam ürün yapılandırma modeli için tam sözdizimi doğru olduğunu ve tüm adlandırma ve modelleme kuralları dikkate gerektiğini doğrulamak için doğrulama yapılabilir.

### <a name="testing"></a>Test etme

Bir modeli test etmek, gerçek bir yapılandırma oturumuna benzerlik taşır. Kullanıcı, yapılandırma sayfaları arasında gezinebilir ve model yapısının, yapılandırma işlemini desteklediğini doğrulayabilir. Kullanıcı, öznitelik değerlerinin doğru olduğunu ve öznitelik tanımlarının kullanıcının doğru değerleri seçmesine yol gösterdiğini doğrulayabilir. Son olarak, bir test oturumu tamamlandıktan sonra sistem ürün reçetesi ve seçilen öznitelik değerlerine karşılık gelen rotayı oluşturmaya çalışır ve herhangi bir hata oluşursa hata iletisi sunar.

### <a name="the-configuration-page"></a>Yapılandırma sayfası

Bileşenler arasında gezinmek için **İleri**'yi ya da odak ayarlamak için ürün yapılandırma model ağacındaki bir bileşeni tıklatın.

## <a name="finalizing-a-model-for-configuration"></a>Bir modelin yapılandırma için tamamlanması
Ürün yapılandırma modeli sipariş ile yapılandırma senaryolarında kullanılmaya hazır olduğunda, bir sürüm oluşturulmalıdır. Ancak, model oluşturma deneyimini geliştirmek çeşitli seçenekler vardır.

### <a name="user-interface"></a>Kullanıcı arabirimi

Yapılandırma arabirimi bir veya daha fazla alt bileşenleri içindeki öznitelik gruplarını sunarak değiştirilebilir. Bu tür bir gruplandırma, belirli öznitelikleri arasındaki ilişkileri vurgulayabilir ve yapılandırma kullanıcısının o an odakta ürün alanını tanımlamasına yardım eder.

### <a name="templates"></a>Şablonlar

Yapılandırma işlemini hızlandırmak için bir veya daha fazla yapılandırma şablonları oluşturulabilir. Alternatif olarak, bir satış kampanyasının ne zaman belirli bir ürün özellikleri kümesi üzerinde odaklanacağı gibi belirli öznitelik birleşimleri tanıtmak için şablonlar oluşturulabilir.

### <a name="translations"></a>Çeviriler

Ürün farklı ülkelerde/bölgelerde satılıyorsa, yapılandırma arabiriminde görüntülenen tüm metinler için çeviriler oluşturulabilir. Bu metin yalnızca ad ve açıklama alanlarını değil, aynı zamanda öznitelik metin değerlerini içerir.

### <a name="versions"></a>Sürümler

Sonlandırılma işleminde son ve en önemli adım bir ürün yapılandırma modeli için sürüm oluşturmaktır. Sürüm bir sipariş veya teklif satırındaki yapılandırma için seçilebilecek ürün yöneticisi ve ürün modeli yapılandırması arasındaki ilişkiyi temsil eder. Yapılandırma oturumunda kullanılmadan önce, sürümün onaylanması ve etkinleştirilmesi gerekir.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Ürün yapılandırma modeli API aracılığıyla genişletme
İş ortakları ve geliştirici lisansına sahip diğerleri bir ürün yapılandırma modeli yeteneklerini genişletebilecek şekilde, özel uygulama programlama arabirimi (API) kullanılmıştır. Ana hedef, ortakların ve mevcut Ürün Oluşturucu kullanan müşterilerin Ürün Oluşturucu modellerine yerleşik kodu API'ye geçiş yapmasını sağlayan bir mekanizma kurmaktır. Bu şekilde, onlar modellerini Ürün Oluşturucusu'ndan bir ürün yapılandırmaya geçirebilir. Ancak, yeni ortaklar ve müşteriler de yeni ürün yapılandırma modellerini genişletmek için API kullanarak yararlanabilir.

### <a name="pcadaptor-class"></a>PCAdaptor sınıfı

API ürün yapılandırma modellerinin veri yapısını sergileyen **PCAdaptor** sınıfları kümesini kullanarak uygulanır. **PCAdaptor** sınıfının bir örneği, genişletilecek her model için oluşturulmalıdır. Bir yapılandırma oturumu tamamlandıktan sonra, sistem bu sınıfın bir örneğini denetler ve bulursa onu çalıştırır.  

Aşağıdaki akış diyagramı işlemi özetlenmektedir.  

[![Akış diyagramı](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

Ürün yapılandırma API akış diyagramı

## <a name="product-configuration"></a>Ürün yapılandırması
Ürün yapılandırma aşağıdaki yerlerden gerçekleştirilebilir:

-   Satış siparişi satırı
-   Satış teklifi satırı
-   Satın alma siparişi satırı
-   Üretim emri satırı
-   Madde gereksinim satırı (proje)

Müşterinin gereksinimini karşılayan ürünün ayrı bir değişkenini oluşturmak yapılandırmanın amacıdır. Her yeni yapılandırma için bir benzersiz yapılandırma kimliği oluşturulur. Bu kimlik stok aracılığıyla izleme sağlar.

### <a name="multiple-sites-and-intercompany"></a>Birden çok site ve şirketler arası

Yapılandırma üretim gerçekleşeceği site veya şirketten ayrı bir site veya bir şirkette bile yapılır, ürün reçetesi ve rota oluşturulur ve tedarik şirketindeki tedarikçi sitesine yerleştirilir. Ürün çeşidi tedarik zincirinde yer alan tüm şirketlerde yayımlanacaktır.




