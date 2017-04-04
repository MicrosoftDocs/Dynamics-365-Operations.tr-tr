---
title: "Yollar ve işlemleri"
description: "Bu konu, yollar ve işlemleri hakkında bilgi sağlar. Bir yol, bir ürün veya ürün çeşit üretme işlemini tanımlar. Üretim süreci ve bu adımları gerçekleştirilmesi gereken sipariş (işlem) her adımı açıklar. Her adım için yol gerekli işlemleri kaynakları gerekli hazırlık süresi ve çalışma süresi ve maliyeti nasıl hesaplanacağını tanımlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Yollar ve işlemleri

Bu konu, yollar ve işlemleri hakkında bilgi sağlar. Bir yol, bir ürün veya ürün çeşit üretme işlemini tanımlar. Üretim süreci ve bu adımları gerçekleştirilmesi gereken sipariş (işlem) her adımı açıklar. Her adım için yol gerekli işlemleri kaynakları gerekli hazırlık süresi ve çalışma süresi ve maliyeti nasıl hesaplanacağını tanımlar.

<a name="overview"></a>Özet
--------

Bir yol, bir ürün veya ürün çeşit üretmek için gereken işlemlerin sırasını açıklar. Her operasyon için yol da ayarlamak ve işlem ve maliyeti nasıl hesaplanacağını gerçekleştirmek için gereken zamanı gereklidir işlem kaynakları tanımlar. Birden fazla ürün üretmek için aynı rotayı kullanabilirsiniz veya her ürün veya ürün çeşit için benzersiz bir yol tanımlayabilirsiniz. Aynı ürün için birden fazla yol bile olabilir. Bu durumda, kullanılan yol, üretilmesi gereken miktar gibi etkenlere bağlı olarak değişir. Bir rotaya operasyonlar için Microsoft Dynamics 365 tanımı, birlikte, üretim sürecini açıklayan dört ayrı öğelerden oluşur:

-   **Yol** – bir rota üretim süreci yapısını tanımlar. Diğer bir deyişle, işlemlerin sırasını tanımlar.
-   **İşlem** – bir işlemi tanımlayan bir yolu, adlandırılmış bir adım gibi **derleme**. Aynı işlem içinde birden çok yol oluşabilir ve farklı operasyon numaraları olabilir.
-   **Operasyon ilişkisi** – operasyon ilişkisi hazırlık süresi ve çalışma süresi, maliyet kategorileri, tüketim parametreleri ve kaynak gereksinimleri bir operasyon, operasyon özelliklerini tanımlar. Operasyon ilişkisi operasyonel işlem içinde kullanılan rota veya üretilmekte ürünleri bağlı olarak değişen bir işlem özelliklerini etkinleştirir.
-   **Rota versiyonu** – bir rota versiyonu, bir ürün veya ürün çeşit üretmek için kullanılan yolu tanımlar. Rota versiyonları ürünler arasında yeniden veya zamanla değişimi için bir yol sağlar. Onlar da aynı ürünü üretmek için kullanılmak üzere farklı yollar sağlar. Bu durumda, kullanılan rota konumu veya üretilmesi gereken miktar gibi etkenlere bağlıdır.

## <a name="routes"></a>Rotalar
Bir yol, bir ürün veya ürün çeşit üretmek için kullanılan işlemlerin sırasını açıklar. Her operasyonun operasyon numarası ve ardıl işlem atanmıştır. Bir veya daha fazla başlangıç noktaları ve tek bir bitiş noktası olan yönlendirilmiş bir grafik tarafından temsil edilebilir bir rota ağındaki işlemlerin sırasını oluşturur. İşlemler için Dynamics 365 içinde yollar yapı türüne göre ayrılırlar. Basit yollar ve yol yollar iki tür olan ağlar. Üretim denetimi parametrelerinde yalnızca basit yollar kullanılıp kullanılamayacağı veya daha karmaşık bir rota ağları kullanılabilir olup olmadığını belirtebilirsiniz.

### <a name="simple-routes"></a>Basit yollar

Basit bir yol sıralı olduğundan ve yol için tek bir başlangıç noktası vardır.  

[![Basit yol](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Üretim kontrol parametreleri yalnızca basit yollar etkinleştirirseniz, Dynamics 365 işlemleri için operasyon numaralarını otomatik olarak oluşturur (10, 20, 30 vb.) yol tanımladığınızda.

### <a name="route-networks"></a>Rota ağları

Daha karmaşık bir rota ağları üretim denetimi parametrelerinde etkinleştirirseniz, birden çok başlangıç noktaları ve paralel olarak çalışan işlemleri yolları tanımlayabilirsiniz.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Notlar:**

-   Her operasyonun tek bir ardıl işlem olabilir ve tek bir işlemle tüm rota bitmelidir.
-   Aynı ardıl işlem (örneğin, 30 ve 40 önceki çizimde işlem) sahip birden çok işlemleri gerçekten paralel olarak çalıştıracağı garantisi yoktur. Kullanılabilirlik ve kaynakların kapasitesini operasyonlar planlanır yolu üzerinde kısıtlamalar koyabilirsiniz.
-   Operasyon numarası olarak 0 (sıfır) kullanamazsınız. O numarayı ayrılmıştır ve hiçbir ardıl operasyonun rotadaki son operasyon olduğunu belirtmek için kullanılır.

### <a name="parallel-operations"></a>Paralel operasyonlar

Bazı durumlarda, farklı özelliklere sahip birden çok işlem kaynaklarının birleşimi bir işlemi gerçekleştirmek için gereklidir. Örneğin, derleme işlemi bir makine, araç ve her iki makine için bir alt işlem denetleyecek gerektirebilir. Bu örnek, burada bir operasyonun birincil operasyon belirlenmiş ve diğer ikincil paralel işlemleri kullanarak modellenebilir.  

[![Birincil ve ikincil operasyonlar sahip rotayı](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Genellikle birincil operasyon darboğaz kaynağı temsil eder ve ikincil operasyonlar için çalışma süresi belirler. Ancak, sınırlı kapasite gerektirir planlama sırasında operasyon birincil ve ikincil operasyonlar için zamanlanmış kaynaklar kullanılabilir ve aynı zamanda ücretsiz kapasitesine sahip.  

Birincil operasyon hem de ikincil operasyonlar aynı operasyon numarası (30 önceki çizimde) olması gerekir.  

İkincil operasyonlar (30' ve 30'') için kaynak gereksinimleri araç ve işçi ise yukarıdaki örnekte, kaynak (30) birincil operasyon için makine gereksinimdir. Yüzde elli - yük zamanlanan alt aynı anda iki makine denetleyecek olduğunu garanti yardımcı olur.

### <a name="approval-of-routes"></a>Rotaların onaylanması

Bir rota planlama veya üretim işleminde kullanılmadan önce onaylanmalıdır. Onay yolu tasarım tamamlandığını gösterir. Aynı ürünün piyasaya veya yayımlanan ürün çeşit birden fazla onaylanmış yollar sağlayabilirsiniz. Genellikle ilk ilgili rota versiyonu onaylandığında bir rotanın onaylanması gerçekleşir. Ancak, bazı senaryolarda, rota ve rota versiyonunun onaylanması farklı işlem sahiplerinin gerektirebilir ayrı faaliyetler vardır.  

Her rota onaylanmış veya onaylanmamış ayrı ayrı olabilir. Ancak, onaylanmamış bir rota olduğunda, tüm ilgili rota versiyonları da onaylanmamış olduğunu unutmayın. Üretim denetimi parametrelerinde yollar onaylanmamış olabilir ve onaylı rotalar değişip olup olmadığını belirtebilirsiniz.  

Her yol onaylayan kaydeden bir günlük tutmak, elektronik imza için Rota onayı gerektirebilir. Kullanıcıların kullanarak kimliklerini onaylamak sahip olur bir [elektronik imza](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>İşlemler
Üretim sürecindeki bir adım bir işlemdir. İşlemleri için Dynamics 365 içinde her işlem ID'si ve basit bir açıklama var. Aşağıdaki tablolarda, bir makine Atölye işlemlerinden tipik örnekleri gösterir.

| Operasyon  | Açıklama        |
|------------|--------------------|
| PipeCut    | Boru kesme       |
| TIGweld    | TIG kaynak        |
| JigAssy    | Jig derleme       |
| Denetleme | Kalite incelemesi |

Makine Hazırlık süresi ve çalışma süresi, kaynak gereksinimleri, maliyet bilgileri ve Tüketim hesaplaması, operasyon, operasyon özelliklerini operasyon ilişkisi üzerinde belirtilir. (Operasyon ilişkileri hakkında daha fazla bilgi için sonraki bölüme bakın.)

## <a name="operation-relations"></a>Operasyon ilişkileri
Operasyon ilişkisi üzerinde işlem aşağıdaki kullanım özelliklerini tutulur:

-   Maliyet kategorileri
-   Tüketim parametreleri
-   İşlem süreleri
-   İşlem miktarları
-   Kaynak gereksinimleri
-   Notlar ve yönergeler

Aynı işlem için birden fazla operasyon ilişkileri tanımlayabilirsiniz. Ancak, her operasyon ilişkisi belirli bir operasyona ve belirli bir yol, yayımlanmış bir ürün veya bir madde grubuyla ilgili serbest bırakılan ürün kümesi özelliklerini saklar. Bu nedenle, aynı işlem içinde farklı kullanım özelliklerine sahip birden çok yol kullanılabilir. Ayrıca, kullanılan rota ve üretilen ürün ne olursa olsun aynı kullanım özelliklerine sahip standart operasyonlar kullanırsanız daha kolay ana verilerinizi koruyabilirsiniz. Operasyon ilişkisi kapsamı ile tanımlanan **madde kodu**, **Madde ilişkisi**, **rota kodu** ve **Rota ilişkisi** aşağıdaki tabloda gösterildiği gibi özellikler.

| Madde kodu | Madde ilişkisi         | Rota kodu | Rota ilişkisi   | Operasyon ilişkisinin kapsamı                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tablo     | &lt;Madde Kodu&gt;       | Rota      | &lt;Rota kodu&gt; | Operasyon rotasında kullanıldığında, işlem özelliklerini burada **rota numarası**=&lt;kimliği yönlendirmek&gt; yayınlanan ürün üretmek için burada **madde numarası**=&lt;kimliği madde&gt;.                                                                                                                        |
| Tablo     | &lt;Madde Kodu&gt;       | Tümü        |                  | Yayımlanan ürün üretmek için kullanıldığında, işlem varsayılan çalışma özelliklerini burada **madde numarası**=&lt;kimliği madde&gt;. Diğer bir deyişle, serbest bırakılan ürün için hiçbir özel rota operasyon ilişkisi olduğunda bu işlem özellikleri uygulayın.                                     |
| Grup     | &lt;Madde grubu kodu&gt; | Rota      | &lt;Rota kodu&gt; | Operasyon rotasında kullanıldığında, işlem özelliklerini burada **rota numarası**=&lt;yol kimliği&gt; madde grubu ile ilişkili yayımlanmış ürünler üretmek için &lt;grup kodunu madde&gt;, serbest bırakılan ürün için bir yol özel operasyon ilişkisi olmadığı sürece.                         |
| Grup     | &lt;Madde grubu kodu&gt; | Tümü        |                  | Madde grubu ile ilişkili yayımlanmış ürünler üretmek için kullanıldığında, işlem varsayılan çalışma özelliklerini &lt;Grup Kimliği madde&gt;, daha özel bir operasyon ilişkisi yoksa.                                                                                                  |
| Tümü       |                       | Rota      | &lt;Rota kodu&gt; | Rotada kullanıldığında, işlem varsayılan çalışma özelliklerini burada **rota numarası**=&lt;kimliği yol&gt;. Diğer bir deyişle, bu kullanım özellikleri yayımlanan ürün ya da belirli bu yolu hiç operasyon ilişkisi olduğunda veya madde grubu ilişkilendirilmiş uygulayın. |
| Tümü       |                       | Tümü        |                  | Varsayılan işlem işlem özelliklerini. Daha özel bir operasyon ilişkisi yok, bu kullanım özellikleri uygular.                                                                                                                                                                |

Operasyon ilişkisi belirli bir siteye de belirtebilirsiniz. Bu şekilde, işlemsel özelliklerin bir işlemin, işlemin gerçekleştirildiği konumuna göre (site) değişebilir. Yapılandırılmış ürünler için her ürün konfigürasyonu için farklı kullanım özelliklerini de belirtebilirsiniz.  

Operasyon ilişkilerini, yollar tanımladığınızda çok fazla esneklik verir. Ayrıca, varsayılan özelliklerini tanımlama yeteneği sürdürmesi gereken ana veri miktarını azaltmaya yardımcı olur. Ancak, bu esneklik de bir operasyon ilişkisi içinde değiştirmek içeriğinin farkında olmalıdır anlamına gelir.  

**Not:** aynı işlemi (örneğin, derleme) tüm tekrarlamalarını işlemsel özelliklerin operasyona göre rota operasyon ilişkilerini saklandığından, aynı makine hazırlık süresi, çalışma süresi, kaynak gereksinimlerini ve benzeri vardır. Bu nedenle, bir işlem iki oluşumu aynı rotada gerçekleşir ancak farklı çalışma süreleri olması, Assembly1 ve Assembly2 gibi iki farklı işlemler oluşturmalısınız.

### <a name="modifying-product-specific-routes"></a>Ürüne özgü yollar değiştirme

Açtığınızda **yol** gelen sayfa **Ürün Ayrıntıları Serbest** sayfasında, seçilen yayınlanan ürünüyle ilişkili rota versiyonları gösterilir. Bu bağlamda, her işlem için en iyi rota sürümü ile eşleşen işlemleri için Dynamics 365 operasyon ilişkisi kullanım özelliklerinden gösterir. İşlemlerin listesini içerdiğini görürsünüz **madde kodu** ve **rota kodu** operasyon ilişkisi özelliklerinden. Bu nedenle, hangi operasyon ilişkisi gösterilen belirleyebilirsiniz.  

Üzerinde **yol** sayfası, çalışma zamanı veya maliyet kategorilerini operasyon, operasyon özelliklerini değiştirebilirsiniz. Rota ve geçerli rota versiyonunu başvurulan yayımlanan ürün özgü operasyon ilişkisi üzerinde yaptığınız değişiklikler depolanır. Operasyon ilişkisi gösterilen yol ve serbest bırakılan ürün için özel değilse, değişikliklerinizi depolanmadan önce Sistem operasyon ilişkisi bir kopyasını oluşturur. Bu kopya *olan* belirli rota ve serbest bırakılan ürün için. Bu nedenle, yaptığınız değişiklikler diğer yollar etkilemez veya ürünleri serbest. Hangi operasyon ilişkisi üzerinde değiştirilmekte olan doğrulamak için **yol** sayfasında, bakmak **madde kodu** ve **rota kodu** alanlar.  

Kullanarak bir yol ve serbest bırakılan ürün için belirli bir işlemi el ile de oluşturabilirsiniz **kopya ve ilişki düzenleme** işlev.  

**Not:** üzerinde yeni bir operasyon rota eklemek isterseniz **yol** sayfa, operasyon ilişkisi yalnızca geçerli serbest bırakılan ürün için oluşturulur. Bu nedenle, yol da yayınlanan diğer ürünleri üretmek için kullanılan bu yayımlanmış ürünler için hiçbir ilgili operasyon ilişkisi vardır ve rota bu yayımlanmış ürünler için artık kullanılabilir.

### <a name="maintaining-operation-relations-per-route"></a>Her rota operasyon ilişkilerini sürdürme

Açtığınızda **rota ayrıntıları** gelen sayfa **yolları** listesi sayfası uygulamak için seçili rota operasyon ilişkilerini listesi gösterilir. Bu nedenle, hangi işlemsel özelliklerin hangi ürünler için kullanılan kolayca doğrulayabilirsiniz. Varsayılan özellik değerleri hem ürüne özgü özellik değerlerini değiştirebilirsiniz.  

Yeni bir operasyon ilişkisi eklerseniz **rota ayrıntıları** sayfası, **rota kodu** otomatik olarak ayarlanırsa **yol**ve **Rota ilişkisi** geçerli rota için rota numarası alanında ayarlanır.

### <a name="maintaining-operation-relations-per-operation"></a>Her operasyon operasyon ilişkilerini sürdürme

Gelen **işlemleri** sayfa açabilir **operasyon ilişkilerini** sayfa. Bu sayfada, belirli bir işlem için tüm operasyon ilişkilerini değiştirebilirsiniz. Varsayılan değerler içeren operasyon ilişkileri bile değiştirebilirsiniz.  

Standart operasyonlar kullanılıyorsa ve tüm ürünleri ve süreçleri, işletim parametrelerini aynı olması durumunda **operasyon ilişkilerini** sayfası, bu işlemlerin varsayılan çalışma Özellikleri korumak için kullanışlı bir yol sağlar.

### <a name="applying-operation-relations"></a>Operasyon ilişkilerini uygulanıyor

Bazı durumlarda, bir operasyon için işlemsel özelliklerin işlemleri için Dynamics 365 bulmanız gerekir. Satınalma siparişi oluşturulduğunda, örneğin, işlemsel özelliklerin her operasyonun üretim rotası için operasyon ilişkilerini kopyalanmalıdır. Bu gibi durumlarda, Dynamics 365 işlemleri için en özel birleşimini az belirli birleşimi için ilgili operasyon ilişkilerini arar.  

Bir operasyon ilişkisi üzerinde eşleşme madde grubu kimliği tercih edilen Dynamics 365 işlemleri aramak için en uygun operasyon ilişkisi için yayımlanmış bir ürün, serbest bırakılan ürün madde Kimliğini eşleşen bir operasyon ilişkisi olduğunda Buna karşılık, madde grubu kimliği ile eşleşen bir operasyon ilişkisi varsayılan iş ilişkisi tercih edilir. Arama aşağıdaki sıraya göre yapılır:

1.  **Madde kodu**=**tablo** ve **Madde ilişkisi**=&lt;öğesi kimliği&gt;
2.  **Madde kodu**=**grup** ve **Madde ilişkisi**=&lt;madde grubu kodu&gt;
3.  **Madde kodu**=**tüm**
4.  **Rota kodu**=**yol** ve **Rota ilişkisi**=&lt;yol kimliği&gt;
5.  **Rota kodu**=**tüm**
6.  **Yapılandırma**=&lt;konfigürasyon kimliği&gt;
7.  **Configuration**=
8.  **Site**=&lt;site kimliği&gt;
9.  **Site**=

Bu nedenle, bir işlemi her rota için yalnızca bir kez kullanılmalıdır. İşlem aynı Rotadaki birden çok kez oluşursa, bu işlem tüm tekrarlamalarını aynı operasyon ilişkisi vardır ve her örneği için (örneğin, çalışma zamanları) farklı özelliklere sahip olmayacaktır.

## <a name="route-versions"></a>Rota sürümleri
Rota versiyonları ürünlerin üretimini çeşitlemelerine uyum ya da üretim işlemi üzerinde daha fazla denetim sağlamak için kullanılır. Belirli bir ürünün piyasaya hangi yol kullanılmalıdır tanımlarlar veya yayımlanan ürün çeşit üretilir. Aşağıdaki kısıtlamalar, yayımlanmış bir ürün için hangi yol kullanılır tanımlamak için kullanabilirsiniz:

-   Ürün boyutları (boyut, renk, stil veya yapılandırma)
-   Üretim miktarı
-   Üretim tesisi
-   Üretim tarihi

Zaman içinde belirli bir miktar, belirli bir sitede ürün üreten veya belirli bir dönemde, özel bir rota versiyonu varsayılan rota versiyonu belirleyebilirsiniz. Ancak, bu yalnızca bir etkin rota verilen yayımlanmış bir ürün ve belirli kısıtlamalar kümesi için izin unutmayın.  

Üretim denetimi parametrelerinde bir rota versiyonu geçerlilik süresi her zaman belirtilmesi gerekir.

### <a name="approval-of-route-versions"></a>Rota versiyonlarının onayı

Planlama veya üretim süreci içinde bir rota versiyonu kullanılmadan önce onaylanmalıdır. İlgili rota, rota versiyonunu onayladığınızda, ayrıca onaylayabilirsiniz. Ancak, yalnızca ilgili rota da onaylanırsa bir rota versiyonu onaylanabilir unutmayın.

### <a name="activating-the-default-route-version"></a>Varsayılan rota versiyon etkinleştirme

Bir rota versiyonu etkinleştirdiğinizde, master planlama varsayılan rota versiyonu kullanır veya üretim emirleri oluşturmak için kullanılacak şekilde belirleyin. Kısıtlamalar (örneğin, dönem, site veya miktar) belirli bir kümesi için yalnızca bir etkin rota sürümü olabilir. Bir sürüm çakışmaları etkinleştirmeye çalıştığınız sürüm, zaten etkinse, bir hata iletisi alırsınız. Belirsiz bir etkinleştirme önlemek için daha sonra ya da çakışan versiyonun veya kısıtlamalar (genellikle dönem) rota versiyonunun değiştirmeniz gerekir.

### <a name="electronic-signatures"></a>Elektronik imza

Kim onaylar ve her bir rota versiyonu etkinleştirir kaydeden bir günlük tutmak, bu görevler için elektronik imza gerektirebilir. Onayla ve rota versiyonları etkinleştirmek kullanıcıların kullanarak kimliklerini onaylamak sahip olur bir [elektronik imza](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Servis talebi yönetimi kullanan Ürün değişikliği

Ürün onayı için Harf Değiştir ve yeni veya değiştirilmiş yollar ve rota versiyonlarının etkinleştirme rota sürümü kısıtlamaları özetini görmek için kolay bir yol sağlar. Onayla ve Ürün değişikliği durumunda sonuçları belge ve belirli bir değişikliği tek bir işlemde ilgili tüm yolları etkinleştir.

## <a name="maintaining-routes"></a>Yolların bakımını yapma
İş gereksinimlerinize bağlı olarak, işlem tanımları sağlamak için gerekli çabayı azaltmak mümkün olabilir.

### <a name="making-routes-independent-of-resources"></a>Yol kaynaklarının bağımsız yapma

Birçok sisteminde rotadaki işlemleri kaynak veya bir işlem gerçekleştirmesi gereken kaynak grubu belirtilmelidir. Ancak, operasyonlar için Dynamics 365 içinde işlemleri kaynak işlemi için uygun olması için yerine getirmesi gereken gereksinimler kümesi tanımlayabilirsiniz. Bu nedenle, belirli işlemleri kaynak veya kullanılması gereken kaynak grubu işlem aslında zamanlandığı süreye kadar belirlenecek yok. Birçok çalışanlar veya aynı işlemi gerçekleştiren makineler varsa, bu işlev özellikle yararlıdır.  

Örneğin, bir işlem, bir işlem kaynağı gerektirdiğini belirtmek **makine** olan bir tür bir **Stamping** 20 ton yeteneğini. İşlem planlandığında zamanlama motoru belirli işlemleri kaynak veya kaynak grubu için daha sonra bu gereksinimleri çözer. Yalnızca belirli bir makine bağlama işlemi yerine bu gereksinimleri belirleyebilirsiniz olduğundan çok daha fazla esnekliğe sahip olursunuz. Ayrıca, bakım kaynaklar taşınır ve yeni kaynaklar eklenmeden kolay olur.  

Çeşitli kaynak gereksinimlerini ve nasıl kullanılacakları hakkında daha fazla bilgi için bkz: işlem kaynak gereksinimleri ve [kaynak yetenekleri](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Siteler arasında yollar paylaşımı

Aynı ürünün birden fazla üretim sitesinde üretmek ve ürün üretmek için tüm siteler aynı adımlardır, genellikle tüm üretim siteler arasında kullanılan paylaşılan bir yol tasarlayabilirsiniz. Paylaşılan bir yol oluşturmak için bir site rotasında belirtmeyin. Ancak, hala, ürünün her sitede paylaşılan rota ilişkilendiren bir rota versiyonunu oluşturmanız gerekir.  

Ayrıca rotasındaki her operasyon için kaynak gereksinimleri belirli işlemleri kaynaklar veya kaynak grupları için arama yok, ancak bunun yerine gerekli kaynakları açısından özelliklerini ifade edilir emin olmanız gerekir. Zamanlama altyapısı sonra üretim üzerinde zamanlanmış sitesinden uygun işlem kaynakları atamak mümkün olacaktır. Örneğin, çalışma süresi içinde küçük farklılıklar varsa veya belirli bir operasyon için ayar süresini siteye ise, bu site için bir ek operasyon ilişkisi ekleyerek bu bilgileri belirtebilirsiniz.  

Paylaşılan yollar yararlarını tam olarak yararlanabilmek için kaynak tüketimi de ilgili ürün reçetesini (BOM) kullanmanız gerekir. Ürün reçetesi satırı için kaynak tüketimi bayrağını ayarladığınızda, Hammadde tüketilen yeri ve ambar sözcüğünden çıkarıldığında işlemi üzerinde zamanlanmış işlemleri kaynak. Bu nedenle, yeri ve ambar üretim gerçekten zamanlandığı süreye kadar belirlenmesi gerekmez. Bu yolla, hem bir BOM ve rota ürün burada üretilen fiziksel konumunu bağımsız duruma getirebilirsiniz.

### <a name="standard-operation-relations"></a>Standart operasyon ilişkileri

İşinizi standart işlem üretim boyunca kullanıyorsa ve makine hazırlık süresini çok az veya hiç Değişim ise, çalışma süresi, Tüketim hesaplaması, maliyet hesaplaması, ve vb., varsayılan tüm işlemler için operasyon ilişkilerini oluşturmaktan yarar. Bu durumda, belirli herhangi bir yol veya ürünün piyasaya operasyon ilişkilerini oluşturmaktan kaçının.  

Ayrıca kaynak gereksinimleri beceri ve yetenekleri açısından express ve site bağımsız, yollar yapmak, İş süreçlerinizi devam eden bakımının minimumda tutabilirsiniz yardımcı olabilir.  

Bu yaklaşımı kullanırsanız, **operasyon ilişkilerini** sayfa Çalıştırma süreleri ve diğer özellikleri korumak için birincil hedefi haline gelir.

### <a name="resource-specific-process-times"></a>Kaynak özel işlem süreleri

Bir operasyon için kaynak gereksinimleri bir parçası olarak bir işlem kaynağı veya kaynak grubunu belirtmezseniz, ilgili kaynaklara farklı hızlarda çalışmıyor olabilir. Bu nedenle, bir işlemi yürütmek için gereken süre değişebilir. Bu sorunu gidermek için kullanabileceğiniz **formül** işlem süresinin nasıl hesaplanacağını belirtmek için Operasyon ilişkisi alanını. Aşağıdaki seçenekler bulunur:

-   **Standart** – (varsayılan seçenek) hesaplama yalnızca operasyon ilişkisi alanları kullanır ve belirtilen çalışma zamanı tarafından sipariş miktarı çarpar.
-   **Kapasite** – hesaplama içerir **kapasite** işlemleri kaynaktan alan. Bu nedenle, kaynak bağımlı zamanı gelmiştir. İşlemleri kaynakta belirtilen saat başına kapasite değerdir. Bu değer Sipariş miktarla çarpılır ve **faktör** operasyon ilişkisi değer.
-   **Toplu** – operasyon ilişkisi bilgilerini kullanarak toplu kapasite hesaplanır. Toplu işlemleri ve bu nedenle, işlem süresi sayısı sonra göre sipariş miktarı hesaplanabilir.
-   **Kaynak toplu** – bu seçenek temelde aynı olan **toplu** seçeneği. Bununla birlikte, hesaplama içerir **toplu kapasite** işlemleri kaynaktan alan. Bu nedenle, kaynak bağımlı zamanı gelmiştir.


<a name="see-also"></a>Ayrıca bkz.
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


