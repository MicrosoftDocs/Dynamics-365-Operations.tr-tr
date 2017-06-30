---
title: "Ürün reçeteleri ve formüller"
description: "Bu makale, ürün ve ürün çeşitleri tanımlarının merkezi bir parçası olan ürün reçeteleri (BOM'lar) ve formüller hakkında bilgi sağlar. BOM'lar ve formüller, belirli bir ürünün ihtiyaç duyulan malzemelerini veya içerikleri belirtir. Formüller ayrıca belirli üretim bağlamında alınan yan ürünleri ve ortak ürünleri de belirtir."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5a23acfa95bb93dbc5990bf3839bbc629f15cc2f
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="bills-of-materials-and-formulas"></a>Ürün reçeteleri ve formüller

[!include[banner](../includes/banner.md)]


Bu makale, ürün ve ürün çeşitleri tanımlarının merkezi bir parçası olan ürün reçeteleri (BOM'lar) ve formüller hakkında bilgi sağlar. BOM'lar ve formüller, belirli bir ürünün ihtiyaç duyulan malzemelerini veya içerikleri belirtir. Formüller ayrıca belirli üretim bağlamında alınan yan ürünleri ve ortak ürünleri de belirtir. 

<a name="bills-of-materials"></a>Ürün reçeteleri
------------------

Ürün reçetesi (BOM), bir ürünü üretmek için gereken bileşenleri tanımlar. Bileşenler hammadde, yarı mamul ürünler ve malzemeleri olabilir. Bazı durumlarda, bir ürün reçetesinde hizmetlere gönderme yapılabilir. Ancak, ürün reçeteleri genellikle gerekli *malzeme kaynaklarını* açıklar.  

Ürün oluşturmak için gereken operasyon ve kaynakları açıklayan bir rota veya üretim akışıyla birlikte kullanıldığında, ürün reçetesi, ürünün tahmini maliyetini hesaplama temelini oluşturur.  

Bir ürün reçetesi aşağıdaki bilgilerle açıklanan bağımsız bir varlıktır:

-   Ürün Reçetesi Kodu
-   Ürün reçetesi adı
-   Bileşenleri ve malzemeleri açıklayan ürün reçetesi satırları
-   Ürünü ve ürün reçetesinin kullanılabileceği dönemi tanımlayan ürün reçetesi sürümleri

Tek bir ürün reçetesi, benzersiz bir kodla tanımlanmış tek bir düzeyi açıklar. Bileşenlerde, ürün reçetesi sürümlerinin başvurduğu kendi ürün reçeteleri olabilir. Ürün reçetesi tasarımcısında, belirli bir ürün için tüm ürün reçeteleri hiyerarşisini görüntüleyebilir ve düzenleyebilirsiniz.

### <a name="formulas-co-products-and-by-products"></a>Formüller, ortak ürünler ve yan ürünler

Formül, genellikle proses üretimi için kullanılan bir ürün reçetesi alt türüdür. Bileşenlere ve malzemelere ek olarak, formül, ortak ürünleri ve yan ürünleri açıklar. Gerçek sürümde, yan ürünlerin ve ortak ürünlerin formüller için tanımı, formül sürümünü gerektirir. Bir formül, genellikle formül sürümünde tanımlanmış, belirli bir tamamlanmış ürün için belirlenir (bir formül veya planlama maddesi).

### <a name="boms-in-the-product-lifecycle"></a>Ürün yaşam döngüsündeki ürün reçeteleri

Ürün yaşam döngüsünde çeşitli nedenlerle birçok türde ürün reçetesi oluşturulabilir:

-   **Taslak ürün reçetesi** – Bu ürün reçetesi, tasarımın erken bir aşamasındayken gerekli malzemelerin taslak halinde bir tahminini verir ve kabaca bir maliyet ve ürün öznitelikleri tahmini çıkarmanıza yardımcı olur. Bu ürün reçetesi kurumsal kaynak planlamada (ERP) sık kullanılmaz.
-   **Mühendislik ürün reçetesi** – Bu ürün reçetesi, genellikle, varolan ürün portföylerine dayalı ürünler tasarladığınız zaman genellikle kullanılır. Mühendislik ürün reçeteleri, tasarım sürecini basitleştirmek ve karmaşık ürünleri mühendislik modülleri halinde gruplandırmak için yapılandırılmıştır. Basit ürünler için, gerçek üretim işleminde mühendislik ürün reçeteleri kullanılabilir. Ancak, diğer ürünler için, mühendislik ürün reçetesinin bir gerçek üretim ürün reçetesine dönüştürülmelidir. Mühendislik ürün reçeteleri, ürün reçetesi hiyerarşisinde genellikle hayali ürün reçeteleriyle temsil edilir. Mühendislik ürün reçeteleri üretim operasyonlarının planlanmasında ve yürütülmesinde kullanılabilmesine karşın, bu yaklaşım, özellikle çok sayıda siparişin oluşturulduğu yinelenen operasyonlarda verimsizliğe yol açabilir.
-   **Planlama ürün reçetesi** – Bu ürün reçetesi, malzeme gereksinimleri planlaması yapmak için kullanılır. Bileşen ve malzeme talebi, mamul ürün talebine göre hesaplanır. Maliyetlendirme ürün reçeteleri gibi, planlama ürün reçeteleri belirli bir dönem içinde kullanılan belirli bir malzeme karışımını temsil edebilir.
-   **Üretim ürün reçetesi** – Belirli bir üretim için kullanılan gerçek ürün reçetesidir. Üretim ürün reçetesinde, ürünü üretmek için kullanılan fiili kaynaklar hesaba katılmalıdır. Üretim emri, toplu iş emri veya kanban oluşturulduğunda, hayali ürün reçeteleriyle temsil edilen birden fazla ürün reçetesi bir düzeye daraltılır ve sipariş için operasyonlara dağıtılır.
-   **Maliyetlendirme ürün reçetesi** – Bu ürün reçetesi, bir ürünün tahmini maliyetini hesaplamak için kullanılır. Örneğin, standart maliyet kullanılırken veya belirli bir ürün için tahmini planlanan maliyet hesaplanırken bir maliyetlendirme ürün reçetesi kullanabilirsiniz. Maliyetlendirme ürün reçeteleri, kullanılması beklenen belirli malzeme ve kaynak karışımına başvurabilir. Bu nedenle, bir dönem için temsili bir tahmini maliyet oluşturmak ve zamanla oluşabilecek sapmaları önlemek için maliyetlendirme ürün reçetesini kullanabilirsiniz.

Uygulamada fiilen kullanılan ürün reçetesi türleri, o uygulamaya, iş senaryolarına ve gereksinimlere bağlıdır. Basit uygulamalarda, planlama ürün reçetesi, üretim ürün reçetesi ve maliyetlendirme ürün reçetesi tek bir ürün reçetesi olarak modellenebilir. Sık sık mühendislik değişiklikleri ve birden fazla alternatif rotalar olan ortamlarda, büyük olasılıkla daha büyük ürün reçetesi türü grubu gerekecektir.

### <a name="approval-of-boms-and-formulas"></a>Ürün reçetelerinin ve formüllerin onayı

Her ürün reçetesi ve formül ayrı ayrı onaylanabilir veya onayları kaldırılabilir. Bir ürün reçetesi veya formül onayı genellikle ilgili ilk ürün reçetesi sürümü onaylandığında oluşur. Ancak bazı iş senaryolarında bu onaylar işlemde farklı adımlar olabilir ve farklı işlem sahiplerini kapsayabilir.  

Bir ürün reçetesinin onayı kaldırılırsa, ilgili tüm ürün reçetesi sürümlerinin de onayının kaldırılacağını unutmayın.

## <a name="bom-and-formula-versions"></a>Ürün reçetesi ve formül sürümleri
Belirli bir ürün reçetesini veya formülü, üretilebilecek bir ürün çeşidiyle ilişkilendirmek için bir ürün reçetesi sürümü veya formül sürümü oluşturmanız gerekir. Ürün reçetesi sürümlerinin ve formül sürümlerinin geçerliliği dönem, miktar, teis, belirli ürün boyutları ve benzeri ölçütlerle kısıtlanabilir. Formül sürümlerinin verim, ortak ürün ve yan ürün tanımları ve formül için maliyet dağılım yönergeleri gibi önemli ek öznitelikleri vardır.

### <a name="approval-of-bom-and-formula-versions"></a>Ürün reçetesi ve formül sürümlerinin onayı

Planlama veya üretim sürecinde bir ürün reçetesi sürümünün kullanılabilmesi için onaylanması gerekir. Bir ürün reçetesi sürümü onaylandığında, kullanıcının seçim ve kimlik doğrulama haklarına bağlı olarak ilgili ürün reçetesi de onaylanabilir. Bir ürün reçetesi sürümünün ancak ilgili ürün reçetesi onayladığı zaman onaylanabileceğini unutmayın.

### <a name="activation-of-the-default-bom-or-formula-version"></a>Varsayılan ürün reçetesi veya formül sürümünün etkinleştirilmesi

Belirli bir ürün reçetesini veya formülü, master planlamayla veya üretim emirleri oluşturmada kullanılacak varsayılan ürün reçetesi sürümü veya formül sürümü yapmak için, o sürümü etkinleştirmeniz gerekir. Bir sürüm etkinleştirildiğinde, belirtilen sınırlar içerisinde sürümün benzersizliğini (örneğin, dönem, site veya miktar) doğrulanır. Etkinleştirmeye çalıştığınız sürüm, halihazırda etkin bir sürümle çakışıyorsa, bir hata iletisi alırsınız. Bu durumda, belirsiz bir etkinleştirmeyi önlemek için ya çakışan sürümü devre dışı bırakmanız veya sürüm kısıtlamalarında (genellikle dönem) değişiklik yapmanız gerekir.

### <a name="product-change-with-case-management"></a>Servis talebi yönetimiyle ürün değişikliği

Yeni veya değiştirilmiş ürün reçetelerini ve ürün reçetesi sürümlerini onaylamak ve etkinleştirmek için yapılan ürün değişikliği servis talebi, ürün reçetesi sürüm kısıtlamalarını genel bir açıdan görmenin kolay bir yoludur. Ayrıca, bir etkinleştirme tarihi için belirli bir değişiklikle ilgili tüm ürün reçetelerini ve formülleri onaylayabilir ve etkinleştirebilirsiniz.

### <a name="alternative-bom-versions"></a>Alternatif ürün reçetesi sürümleri

Bazı durumlarda, etkin ürün reçetesi veya formül sürümü tahminlerde, satışta veya bir üst üründe kullanılmamalıdır. Bu durumda, alternatif ürün reçetesi veya formül için onaylı bir ürün reçetesi sürümü veya formül sürümü varsa, gerekliliğin (tahmin satırı, satış satırı veya ürün reçetesi satırı) bir parçası olarak belirli bir onaylı ürün reçetesi seçebilirsiniz.  

Planlı siparişler, üretim emirleri veya kanbanlar oluşturulurken, planlayıcı veya atölye gözetmeni, belirli bir ürünü planlamak veya üretmek için istenen planlanmış üretim tarihinde geçerli bir onaylı ürün reçetesi sürümü kullanabilir. Kullanılan ürün reçetesi sürümünün, varsayılan ürün reçetesi sürümü olarak etkinleştirilmesi gerekmez.

## <a name="bom-and-formula-lines"></a>Ürün reçetesi ve formül satırları
Her malzeme, hizmet veya malzeme içeriği için bir ürün reçetesi satırı oluşturulur. Satır, belirtilen ürün çeşidinin planlı tüketimini ve planlanan tüketimle ilgili çeşitli öznitelikleri tanımlar.  

Ürün reçetesi satırları aşağıdaki satır türlerinde olabilir: **Madde**, **Hayali**, **İlişkilendirilmiş tedarik**, **Satıcı**.

### <a name="item"></a>Madde

Doğrudan tüketilen ve açılım ya da ilişkilendirilmiş tedarik gerektirmeyen hizmetler veya malzemeler için **Madde** satır türünü seçin.

### <a name="phantom"></a>Hayali

Ürün reçetesi satırında bulunan daha alt düzeydeki ürün reçetesi maddelerini açmak istediğinizde **Hayali** satır türünü seçin. Master planlamada, planlanan maliyet hesaplamasında veya **Hayali** türde ürün reçetesi satırları kullanan bir üretim emri tahmininde, hayali ürün reçetesi olan bir ürün çeşidine başvuruda bulunulan ana ürün reçetesi satırı, o ürün çeşidinin ilgili etkin ürün reçetesi sürümüyle belirlendiği şekilde, o ürün reçetesinde ürün reçetesi satırları olarak listelenen bileşen maddelerle değiştirilir. Ürün çeşidinin ilgili bir etkin rotası varsa, o rotadaki operasyonlar üst rotada birleştirilir.  

Hayali ürün reçetelerinin genellikle mühendislik işlemini basitleştirmek için kullanıldığını unutmayın. Hayali ürün reçetelerinin birçok düzeyde yaygın kullanımının performans üzerinde, özellikle yüksek yinelemeli üretim senaryolarında etkisi vardır. Performansı artırmak için hayali ürün reçetesi derin hiyerarşileri kullanmaktan kaçınmalısınız. Bunun yerine, önceden açılmış üretim ürün reçeteleri ve rotaları kullanın.

### <a name="pegged-supply"></a>İlişkilendirilmiş tedarik

Bir alt üretim, bir ürün reçetesi satırı, etkinlik kanbanı veya ürün reçetesi satırının başvuruda bulunduğu herhangi bir ürün çeşidi için bir doğrudan satınalma siparişi oluşturmak istiyorsanız **İlişkilendirilmiş tedarik** satır türünü seçin. Üretim emrini tahmin ettiğiniz zaman alt üretim, etkinlik kanbanı veya satınalma siparişi oluşturulur. Üretim emrini tüketmek için gereken madde miktarları otomatik olarak rezerve edilir.

### <a name="vendor"></a>Satıcı

Üretim süreci bir alt yüklenici kullanıyorsa ve alt yüklenici için otomatik olarak bir alt üretim veya satınalma siparişi oluşturmak istiyorsanız **Satıcı** satır türünü seçin.  

**Ürün reçetesinde alt sözleşmeli operasyonlar hakkında not:** Alt yüklenicinin verdiği hizmet veya çalıştığı iş, stokta izlenen bir servis maddesi olarak oluşturulmalıdır. Servis maddesini ana maddeye bir ürün reçetesi satırı olarak iliştirmeniz gerekir. Rota, alt yüklenicinin operasyon kaynağına tahsis edilen bir operasyon içermelidir.




