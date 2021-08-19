---
title: Mühendislik sürümleri ve mühendislik ürünü kategorileri
description: Bu konu, mühendislik sürümleri konsepti hakkında bilgi sağlar. Mühendislik sürümleri, bir ürünün farklı durumlarının ve verilerinin güncel ve net tutulmasını ve sistemde görselleştirilebilmesini sağlar.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 18f187ef6805b8d2bfe777aaad54ad2cf0fb0d71a981c5b02932f3cccf2404e9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776422"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Mühendislik sürümleri ve mühendislik ürünü kategorileri

[!include [banner](../includes/banner.md)]

Mühendislik ürünleri birçok nedenden dolayı, kendi ürün yaşam döngüsü sırasında gelişir. Örneğin, ürüne servis uygulanabilirliğini geliştirmek, tedarikçi artık sunamadığı için bileşeni değiştirmek, yeni içgörülere yanıt vermek veya ilk tasarımdaki hataları düzeltmek için değişiklikler yapılabilir. Bu değişikliklerin, önceki verilerin üzerine yazılmaması için devam eden bir ürünün parçası olarak depolanması için birçok neden de vardır. Bu nedenlerden birkaçı şunlardır:

- Önceki yaşam döngüsü durumlarında üretilip müşterilerinize teslim edilen ürünü takip etmek istiyorsunuz.
- Değişiklikleri onaylamadan ve uygulamadan önce sağlama süresine ihtiyacınız var.
- Her değişiklikte bir zaman damgası olmasını ve daha önce üretilmiş ürünleri birbirinden ayrı olarak teslim edilmesini istiyorsunuz.

*Mühendislik sürümleri*, bir ürünün çeşitli durumlarının ve verilerinin güncel ve net tutulmasını ve sistemde görselleştirilebilmesini sağlar. Bu konsept; tutarlılığı korumanıza, üretim için ürün reçetelerini sabitlemenize, değişkenliği ortadan kaldırmanıza ve değişiklikleri kolayca belirlemenize yardımcı olur.

Genel olarak, bir değişikliğin yeni bir ürün, yeni bir sürüm veya var olan bir sürüme güncelleştirme gerektirip gerekmediğini belirlemek için *biçim-uyum-işlev* kuralı uygulanır. Bu kural adındaki üç terimin her biri, mühendislerin parçaları ihtiyaçlara göre eşleştirmesine yardımcı olan bir parçanın belirli bir yönünü ifade eder. Biçim-uyum-işlev kuralı, ürünün biçimi, uyumu ve işlevinin korunması koşuluyla, bir parçayı değiştirmek için minimum belge ve tasarım maliyeti gerektiğinden, tasarım değişikliklerinin esnekliğini artırır.

- **Uyum**, parçanın veya özelliğin bir montajdaki başka bir özelliğe veya parçaya bağlanma, yerleşme veya dahil olma becerisi anlamına gelir. Uyum, parçanın yararlı olabilmesi için gerekli montaj toleranslarını karşılamasını sağlar.
- **Biçim**; dış boyutlar, ağırlık, boyut ve görsel görünüm gibi bir parça veya montajın özelliklerini ifade eder. Biçim, bir mühendisin estetik tercihlerinden en çok etkilenen unsurdur. Bu özellik; muhafaza, şasi ve kontrol panelini içerir ve bunlar ürünün dış "yüzünü" oluşturur.
- **İşlev**, parça belirtilen amacını etkin ve güvenilir bir şekilde gerçekleştirdiğinde karşılanan bir ölçüttür. Örneğin, bir elektronik üründe işlev, kullanılan katı hal bileşenlerine ve yazılıma veya üretici yazılımına bağlı olabilir. Genelde, seçilen muhafaza özelliklerine de bağlı olabilir. Bir muhafazanın işlev ölçütünün başarısız olmasının en yaygın nedenlerinden ikisi, kötü yerleştirilmiş ya da kullanışsız boyutlu bağlantı noktaları ve yanıltıcı ya da eksik etiketlerdir. 

## <a name="engineering-versions"></a>Mühendislik sürümleri

Mühendislik ürünlerini kullandığınızda, her ürünün en az bir mühendislik sürümü vardır. Bir mühendislik ürünü oluşturduğunuzda ilk mühendislik sürümü otomatik olarak oluşturulur. Her mühendislik sürümü, bu sürüme özgü mühendislikle ilgili verileri depolar. Bu verilerin bazı örnekleri aşağıda verilmiştir:

- Sürüm numarası ve önceki sürüm numarası (varsa)
- Geçerlilik başlangıç ve geçerlilik bitiş tarihleri
- Sürümün serbest bırakılıp bırakılmayacağını ve hareketlerde kullanılıp kullanılamayacağını gösteren ürün sürümü etkin durumu (Daha fazla bilgi için bkz. [Ürüne hazır olma durumu](product-readiness.md).)
- Ürünü oluşturan ve ürünün sahibi olan mühendislik şirketi (Daha fazla bilgi için bkz. [Mühendislik şirketleri ve veri sahipliği kuralları](engineering-org-data-ownership-rules.md).)
- Montaj kılavuzu, kullanım talimatları, resimler ve bağlantılar gibi ilgili mühendislik belgeleri
- Mühendislik öznitelikleri (Daha fazla bilgi için bkz. [Mühendislik öznitelikleri ve mühendislik özniteliği araması](engineering-attributes-and-search.md).)
- Mühendislik ürünleri için ürün reçetesi (BOM)
- Süreç üretimi ürünleri için formüller
- Mühendislik rotaları

Bu verileri var olan bir sürümde güncelleştirebilir veya bir *mühendislik değişikliği emri* kullanarak yeni bir sürüm oluşturabilirsiniz. (Daha fazla bilgi için bkz. [Mühendislik ürünlerindeki değişiklikleri yönetme](engineering-change-management.md).) Bir ürünün yeni bir sürümünü oluşturursanız sistem mühendislikle ilgili tüm verileri bu yeni sürüme kopyalar. Daha sonra bu yeni sürümün verilerini değiştirebilirsiniz. Bu şekilde, ardışık her sürüm için belirli verileri izleyebilirsiniz. Ardışık mühendislik sürümleri arasındaki farkları karşılaştırmak için tüm değişiklikleri gösteren değişiklik türlerini içeren mühendislik değişikliği emrini inceleyin.

Belirtildiği gibi, bir mühendislik ürünü oluşturduğunuzda ilk mühendislik sürümü otomatik olarak oluşturulur. Bu sürümün sürüm numarası, ürünün mühendislik kategorisinde tanımlanan sürüm numarası kuralını izler. Sonraki sürüme geçiş yapmak için ürünü bir satır olarak mühendislik değişikliği emrine eklemeniz ve **Etki** alanını *Yeni sürüm* olarak ayarlamanız gerekir. Mühendislik değişikliği emri, geçerli sürümden bir sonraki sürüme yapılan değişikliğin ayrıntılarını içerir.

Bir mühendislik ürününün aynı anda yalnızca bir mühendislik değişikliği emrinde olabileceğini unutmayın. Bu kısıtlama, veri doğruluğunu sağlar ve üründe çakışan veya çelişkili değişikliklerin önlenmesine yardımcı olur. Ayrıca, mühendislik değişikliği emrinin **Üst bilgi** görünümündeki **Mühendis** alanının, değişiklik emrinden sorumlu olan mühendisi gösterdiğini de unutmayın. Mühendis sistemde tanımlı bir takıma aitse **Sorumlu** alanı, o takımın liderini gösterir.

## <a name="track-versions-in-transactions"></a>Hareketlerde sürümleri izleme

Mühendislik değişikliği yönetimini kullandığınızda, ürün ana verileriniz her zaman bir veya daha fazla mühendislik sürümü içerir. Mühendislik ürünleri kurulumunuzda, mühendislik sürümünün de *lojistik hareketlerin* bir parçası olup olmadığını seçebilirsiniz. (Daha fazla bilgi için bu konuda daha önce ele alınan [Mühendislik ürünü kategorilerini ayarlama](#product-category) bölümüne bakın.) Lojistik etki alakalıysa, ürüne ve şirkete göre farklılık gösterir. Bazen, bir ürünün yalnızca en son sürümü kullanılır. Bu nedenle, yeni bir sürüm tanıttığınızda, önceki sürüm artık kullanılamaz. Diğer durumlarda, aşağıdaki zorlukların üstesinden gelmek için lojistik hareketlerde önceki sürüm gereklidir:

- Lojistik departmanı bir ürünün iki parçasını müşteriye göndermeli. Bu durumda, iki farklı sürümün gönderilmesini isteyip istemediğinize veya buna izin verip vermeyeceğinize karar vermeniz gerekir.
- Daha sonra bir sorun oluştuğu ve sorunun belirli bir değişiklikle ilişkili olduğu keşfedilir. Bu durumda, her siparişte tam olarak hangi sürümün sevk edildiğini belirlemek yararlı olabilir.
- Şirketler genellikle stoğu aşamalı olarak tüketmek için önce eski sürümleri sevk etmek ister. Özellikle düşük hacimli ürünlerde, bu yaklaşım genellikle eski sürümün stoğunun ne zaman tükeneceğine ilişkin tahminlerle ilgili olarak yeni sürümün geçerlilik tarihleri belirlenerek yönetilebilir. Ancak, bazen bu karşılaştırmayı yapmak mümkün olmayabilir ya da stok düzeyi tahminleri belirsizliğinin çok yüksek olduğunu düşünebilirsiniz.

Sürümlerin stokta görünür hale getirilip getirilmeyeceğine ilişkin karar, daha önce bahsedilen etkenler gibi faktörlere, şirket uygulamalarına ve her şirkete özgü diğer hususlara bağlıdır. *Mühendislik ürünü kategorisi* için davranışı belirtebilirsiniz. Daha sonra, ürünün serbest bırakılduğu tüm şirketler için bu kategoriden oluşturulan tüm ürünler için geçerli olacaktır.

Lojistik etkiye sahip olacak şekilde ayarlanmış ürünlerde her harekette mühendislik sürümü belirtilmelidir. Sistem *en son etkin sürümü* önerecek olsa da, şirket için kullanılabilir tüm etkin sürümler arasından seçebilirsiniz. Lojistik etkiye sahip olmayacak şekilde ayarlanmış ürünlerde, mühendislik sürümü hareketlerde belirtilmez. Ancak, sistem en son etkin sürümü kullanır. Örneğin, bir ürünü bir üretim ürün reçetesine eklediğinizde, en son sürüm kullanılır ve master planlamayı çalıştırdığınızda, en son sürüm kabul edilir.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Mühendislik ürünü kategorilerini ayarlama

Mühendislik ürünü kategorisi, belirli bir mühendislik ürünü oluşturmak için temel sağlar. Her kategori varsayılan değerler ve ilkeler kümesi belirler. Bu nedenle, bir mühendislik ürünü oluşturduğunuzda, ilk olarak ürünün oluşturulacağı kategoriyi seçersiniz.

Yeni bir kategori hiyerarşisi türünün (*mühendislik ürünü hiyerarşisi)* sizin için otomatik olarak ayarladığını unutmayın. **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik ürünü kategorisi ayrıntıları**'na giderek kategorileri el ile oluşturabilirsiniz.

Her mühendislik ürünü kategorisi, ilgili kategoriye dayalı olarak oluşturulan mühendislik ürünlerinin varsayılan davranışını belirler. Bir mühendislik ürünü oluşturduktan sonra, mühendislik ürünü kategorisini değiştiremezsiniz. Ancak, yanlış kategoriyi seçerseniz ürünü silebilir ve sonra yeniden oluşturabilirsiniz.

Bir mühendislik ürünü kategorisi oluşturulduğunda, aşağıdaki ayarları değiştirmeniz engellenir:

- Mühendislik şirketi
- Ürün türü
- Ürün alt türü
- Ürün boyut grubu
- Yapılandırma teknolojisi
- Sürüm numarası kuralı

Diğer ayarlar, mühendislik ürünü kategorisi için ayarlanan varsayılan değerleri devralabilir. Ancak sistem kurallarına göre, bu değerler değiştirilebilir.

Mühendislik ürünü kategorileriyle çalışmak için **Mühendislik değişikliği yönetimi \> Kurulum \> Mühendislik ürünü kategorisi ayrıntıları**'na gidin. Ardından şu adımlardan birini izleyin.

- Yeni kategori oluşturmak için Eylem bölmesinden **Yeni**'yi seçin ve sonra alanları aşağıdaki alt bölümlerde açıklandığı gibi ayarlayın.
- Mevcut kategoriyi düzenlemek için liste bölmesinden ilkeyi seçin ve Eylem bölmesinden **Düzenle**'yi seçin ve sonra alanları aşağıdaki alt kısımlarda açıklandığı gibi ayarlayın.
- Var olan bir kategoriyi silmek için bunu liste bölmesinden seçin ve sonra Eylem bölmesinden **Sil**'i seçin.

### <a name="header"></a>Üst bilgi

Mühendislik ürünü kategorisinin üst bilgisinde aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| Kuruluş adı | Mühendislik ürünü kategorisi için bir ad girin. |
| Mühendislik şirketi | Bu mühendislik ürünü kategorisindeki ürünlerin oluşturulabileceği ve bunların tutulacağı mühendislik şirketini seçin. |

### <a name="details-fasttab"></a>Ayrıntılar hızlı sekmesi

Mühendislik ürünü kategorisinin **Ayrıntılar** hızlı sekmesinde aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| Ürün türü | Kategorinin ürünler veya hizmetler için geçerli olup olmadığını seçin. |
| Üretim türü | Bu alan yalnızca sisteminizde [formül değişikliği yönetimini](manage-formula-changes.md) etkinleştirdiğinizde görünür. Bu mühendislik ürün kategorisinin geçerli olduğu üretim türünü seçin:<ul><li>**Planlama maddesi** – Planlama maddeleri için formül değişikliği yönetimi yapmak üzere bu mühendislik kategorisini kullanın. Planlama maddeleri formüller kullanır. Formül öğelerine benzerler, ancak bitmiş ürünler değil, yalnızca ortak ürünler ve yan ürünler üretmek için kullanılırlar. Formüller proses üretimi sırasında kullanılır.</li><li>**Ürün reçetesi** – Formül kullanmayan ve genellikle (ancak zorunlu değil) ürün reçetelerini içermeyen mühendislik ürünlerini yönetmek için bu mühendislik kategorisini kullanın.</li><li>**Formül** – Bitmiş ürünler için formül değişikliği yönetimi yapmak üzere bu mühendislik kategorisini kullanın. Bu maddelerin bir formülü olacak, ancak ürün reçetesi olmayacak. Formüller proses üretimi sırasında kullanılır.</li></ul> |
| Fiili ağırlık | Bu seçenek yalnızca sisteminizde [formül değişikliği yönetimini](manage-formula-changes.md) etkinleştirdiğinizde görünür. Yalnızca **Üretim türü** alanı *Planlama maddesi* veya *Formül* olarak ayarlandığında kullanılabilir. Ağırlık desteği gerektiren öğeleri yönetmek için bu mühendislik kategorisini kullanacaksanız, bu seçeneği *Evet* olarak ayarlayın. |
| Hareketlerde sürümleri izleme | Ürünün sürümünün tüm hareketlere damgalanıp damgalanmayacağını (lojistik etki) seçin. Örneğin, hareketlerde sürümü izliyorsanız her satış siparişi, belirli bir satış siparişinde ürünün hangi sürümünün satıldığını gösterir. Hareketlerde sürümü izlemiyorsanız satış siparişleri hangi sürümün satıldığını göstermez. Bunun yerine, her zaman en son sürümünü gösterirler.<ul><li>Bu seçenek *Evet* olarak ayarlanırsa ürün için bir ana ürün oluşturulur ve ürünün her sürümü *sürüm* ürün boyutunu kullanan bir varyant olur. **Ürün alt türü** alanı otomatik olarak *Ana ürün* olarak ayarlanır ve **Ürün boyutu grubu** alanında sürüm boyutunun *etkin* olduğu bir ürün boyutu grubu seçmeniz gerekir. Yalnızca *sürümün* etkin bir boyut olduğu ürün boyutu grupları gösterilir. **Düzenle** düğmesini (kalem simgesi) seçerek yeni ürün boyutu grupları oluşturabilirsiniz.</li><li>Bu seçenek *Hayır* olarak ayarlıysa *sürüm* ürün boyutu kullanılmaz. Daha sonra, bir ürün mü yoksa diğer boyutları kullanan bir ana ürün mü oluşturup oluşturmayacağınızı seçebilirsiniz.</li></ul><p>Bu seçenek genellikle sürümler arasında maliyet farkı olan ürünler veya müşteriyle ilgili olarak farklı koşulların geçerli olduğu ürünler için kullanılır. Bu nedenle, her harekette hangi sürümün kullanıldığını belirtmek önemlidir.</p> |
| Ürün alt türü | Kategorinin ürün veya ana ürünleri barındırıp barındırmayacağını seçin. Ana ürünler için ürün boyutları kullanılacaktır.
| Ürün boyut grubu | **Hareketlerde sürümleri izle** ayarı, ürün boyut grubunu seçmenize yardımcı olur. Hareketlerde sürümü izlemek istediğinizi belirtirseniz *sürüm* boyutunun kullanıldığı ürün boyutu grupları gösterilir. Aksi takdirde, yalnızca *sürüm* boyutunun kullanılmadığı ürün boyutu grupları gösterilir. |
| Oluşturma aşamasında ürün yaşam döngüsü durumu | Bir mühendislik ürününün ilk oluşturulduğu zaman sahip olması gereken varsayılan ürün yaşam döngüsü durumunu ayarlayın. Daha fazla bilgi için bkz. [Ürün yaşam döngüsü durumları ve hareketler](product-lifecycle-state-transactions.md). |
| Sürüm numarası kuralı | Kategori için geçerli olan sürüm numarası kuralını seçin:<ul><li>**El ile**: Her yeni sürüm için sürüm numarasını seçersiniz.</li><li>**Otomatik**: Sistem, tanımladığınız bir biçime göre sürüm numarasını ayarlar. Biçimi ayarlarken, bir rakamı temsil etmek için sayı işaretini (\#) ve sabit bir değeri temsil etmek için herhangi başka bir karakteri kullanın. Örneğin, biçimi *V-\#\#* olarak tanımlarsanız ilk sürüm "V-01" olur, ikinci sürüm "V-02" ve benzeri olacaktır.</li><li>**Liste**: Sistem, tanımladığınız özel değerler listesinden bir sonraki sayıyı alır.</li></ul> |
| Geçerliliği zorla | Mühendislik sürümlerinin geçerlilik tarihlerinin bitişik olması mı gerektiğini veya boşluklar ve çakışmalar olup olmayacağını seçin. Bu ayar, kategorinin uygulandığı her mühendislik sürümü için **Geçerlilik başlangıç tarihi** ve **Geçerlilik bitiş tarihi** alanlarını kullanma biçimini etkiler.<ul><li>Bu seçenek *Evet* olarak ayarlanmışsa her sürüm için **Geçerlilik başlangıç tarihi** değeri belirtilmelidir ve sürümler arasında ne çakışmalara ne de boşluklara izin verilir. Her mühendislik sürümü için tarih aralığı, varsa, doğrudan önceki ve sonraki mühendislik sürümlerine bağlanır. Bu senaryoda, her zaman en yeni sürüm kullanılır ve eski sürümler artık kullanılmaz.</li><li>Bu seçenek **Hayır** olarak ayarlanırsa, mühendislik sürümleri için geçerlilik tarihi alanlarında herhangi bir kısıtlama yoktur ve hem çakışmalara hem de boşluklara izin verilir. Bu senaryoda, birden çok sürüm aynı anda etkin olabilir ve herhangi bir etkin sürümle çalışabilirsiniz.</li></ul><p>Bu seçenek, ürün sürümüne bağlı ürün ve rotaları da etkiler. Daha fazla bilgi için bu konunun devamında yer alan [Ürün reçetelerini ve rotaları mühendislik sürümlerine bağlana](#boms-routes) bölümüne bakın.</p> |
| Numara kuralı terminolojisini kullan | Sayı dizilerini, mühendislik özniteliği adlarını ve değerlerini ve metin sabitlerini segment olarak kullanarak bir ürün numarası tanımlamaya yönelik kuralları etkinleştirmek için bu seçeneği *Evet* olarak ayarlayın. Kural oluşturmak veya düzenlemek için **Düzenle** düğmesini seçin. |
| Ad kuralı terminolojisini kullan | Mühendislik özniteliği adlarını, mühendislik özniteliği değerlerini ve metin sabitlerini segment olarak kullanarak ad tanımlama kurallarını etkinleştirmek için bu seçeneği *Evet* olarak ayarlayın. Kural oluşturmak veya düzenlemek için **Düzenle** düğmesini seçin. |
| Açıklama kuralı terminolojisini kullan | Mühendislik öznitelik adlarını, mühendislik öznitelik değerlerini ve metin sabitlerini segment olarak kullanarak açıklama tanımlama kurallarını etkinleştirmek için bu seçeneği *Evet* olarak ayarlayın. Kural oluşturmak veya düzenlemek için **Düzenle** düğmesini seçin. |

### <a name="attributes-fasttab"></a>Öznitelikler hızlı sekmesi

Bu kategoriye ait ürünler için geçerli olan mühendislik özniteliklerini ayarlamak için **Öznitelikler** hızlı sekmesindeki kılavuzu kullanın. Mühendislik öznitelikleri oluşturma hakkında daha fazla bilgi için bkz. [Mühendislik öznitelikleri ve mühendislik özniteliği araması](engineering-attributes-and-search.md).

Kılavuzda öznitelikleri eklemek, kaldırmak ve düzenlemek için **Öznitelikler** hızlı sekmesindeki düğmeleri kullanın.

Bir mühendislik kategorisi için özniteliklerin seçimini değiştirirseniz ve bu kategoriye dayalı ürünler zaten varsa, değişikliklerinizi bu ürünlere uygulayıp uygulamayacağınıza karar vermeniz gerekir. Var olan ürünlerin değişiklikleri yansıtmasını istiyorsanız **Öznitelikler** hızlı sekmesinde **Var olan ürünleri güncelleştir**'i seçin.

Kılavuza eklediğiniz her satır için aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| Kuruluş adı | Eklenecek özniteliği seçin. |
| Değer | Öznitelik için varsayılan değeri seçin. |
| Zorunlu | *Boole* türündeki öznitelikler için bu seçenek *Evet* olarak ayarlanmışsa kullanıcıların özniteliği *Evet* olarak ayarlamaları gerekir. Bu seçenek *Hayır* olarak ayarlanırsa, kullanıcılar özniteliği *Evet* veya *Hayır* olarak ayarlayabilir. Diğer veri türleri için bu seçeneğin ayarı yalnızca bilgilendirme amaçlıdır. |
| Toplu iş özniteliği | Özniteliğin toplu işlem işleviyle doldurulup doldurulmayacağını seçin. |

### <a name="readiness-policy-fasttab"></a>Hazırlık ilkesi hızlı sekmesi

Bu mühendislik kategorisine bağlı olarak oluşturulan ürünler için geçerli olması gereken hazırlık ilkesini seçmek için **Ürün hazırlık ilkesi** alanını kullanın. Daha fazla bilgi için bkz. [Ürün hazırlığı](product-readiness.md).

> [!NOTE]
> Sisteminizdeki **Ürün hazırlık denetimleri** özelliğini açtıysanız *Ürün hazırlık politikası* alanı biraz farklı çalışır. (Bu özellik, standart \[mühendislik dışı\] ürünlere hazırlık ilkeleri uygulamanızı sağlar). Daha fazla bilgi için, bkz. [Standart ve mühendislik ürünlerine hazırlık politikaları atama](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Serbest bırakma ilkesi hızlı sekmesi

Bu kategoriye ait ürünlerde geçerli olan serbest bırakma ilkesini seçmek için **Ürün serbest bırakma ilkesi** alanını kullanın. Daha fazla bilgi için bkz. [Ürün yapılarını serbest bırakma](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Ürün reçetelerini ve rotaları mühendislik sürümlerine bağlama

**Geçerliliği zorla** seçeneğinin ayarı, ürün reçeteleri ve rotaların her mühendislik sürümüne bağlanması açısından önemlidir. Yalnızca aşağıdaki ayarlardan herhangi birinde bir fark varsa ürün başına birden çok ürün reçetesi veya rotayı etkinleştirebilirsiniz:

- Ürün boyutu
- Miktar
- Tesis
- Geçerlilik tarihleri

Mühendislik ürün reçeteleri ve rotaları, geçerli oldukları mühendislik sürümünden oluşturulur. **Mühendislik denetimli** onay kutusundaki onay işaretiyle tanınabilirler. Mühendislik ürün reçeteleri ve rotaları ile çalışırken, bunları genellikle farklı miktarlar kullanarak tasarlamazsınız. Ayrıca genellikle tesis başına farklı ürün reçeteleri tasarlamazsınız. Ayrıca, mühendislik ürün reçeteleri ve rotaları için, geçerlilik tarihleri her zaman mühendislik sürümünden alınır. Bu nedenle, bir mühendislik sürümü, ürün reçetesi ve rotası, aynı geçerlilik tarihlerine sahiptir.

*Sürüm* ürün boyutunu kullandığınız ürünlerde (hareketler üzerindeki lojistik etki vardır), sürüm ürün ve rotalara da eklenir. Bu davranış, **Geçerliliği zorla** ayarından bağımsız olarak, ardışık sürümlerin ürün reçetelerini ve rotalarını ayırt etmeye yardımcı olur.

*Sürüm* ürün boyutunu kullanmadığınız ürünlerde (hareketler üzerinde lojistik etki olmadan), sürüm ürün reçetelerine ve rotalara eklenmez. Bu nedenle, ardışık sürümlerin ürün reçeteleri ile rotaları arasında hiçbir fark olmayacaktır. Bu durumda, **Geçerliliği zorla** seçeneğini *Evet* olarak ayarlamanızı öneririz. Bu sayede, mühendislik sürümlerinin çakışmasını önlemeye yardımcı olur ve önceki sürümün ürün reçetesini ve rotasını devre dışı bırakmak zorunda kalmadan daha yeni bir sürümün ürün reçetesi ve rotasını etkinleştirebilirsiniz. Bu durumda **Geçerliliği zorla** seçeneğini *Evet* olarak ayarlarsanız en son sürümü etkinleştirmeden önce eski sürümlerin ürün reçetelerini ve rotalarını el ile devre dışı bırakmanız gerekir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
