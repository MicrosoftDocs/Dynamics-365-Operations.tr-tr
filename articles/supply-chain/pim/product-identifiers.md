---
title: Ürün tanımlayıcıları
description: Bu konu çeşitli ürün tanımlayıcısı türleri hakkında bilgi sağlar ve ürün tanımlayıcılarını ürün verilerine nasıl ekleyebileceğinizi açıklar.
author: cvocph
manager: AnnBe
ms.date: 03/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 58a32bd7f857e8173996cd4eb21f176bae508587
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546237"
---
# <a name="product-identifiers"></a>Ürün tanımlayıcıları 

[!include [banner](../includes/banner.md)]

Bu konu çeşitli ürün tanımlayıcısı türleri hakkında bilgi sağlar ve ürün tanımlayıcılarını ürün verilerine nasıl ekleyebileceğinizi açıklar.

Microsoft Dynamics ERP veya Microsoft Dynamics CRM'de atölyedeki veya ambardaki ürünlerle çalıştığınızda, bu ürünleri ve ürün çeşitlerini tanımlamak için iyi bir stratejiniz olması gerekir.

## <a name="unique-product-numberproduct-id"></a>Benzersiz ürün numarası/ürün kodu

Microsoft Dynamics 365 for Finance and Operations içinde, bir ürün için birincil kimlik tanımlayıcı, ürün numarasıdır (yani, benzersiz ürün Kimliğidir). Bu numara bir numara serisi tarafından otomatik olarak oluşturulabilir veya bir ürünle el ile ilişkilendirilebilir. Ürün çeşitleri için, numaralar ürün terminolojisi şablonu aracılığıyla tanımlanabilir.

Çoğu durumda, ürün numarası en başta Finance and Operations'ta oluşturulmaz. Bunun yerine, bir ürün yaşam döngüsü yönetimi (PLM) sistemi veya ürün veri yönetimi (PDM) sistemindeki bir ürünle ilişkilendirilir. Bu durumda, ürünleri ve ürün çeşitlerini içe aktarmak için veri varlıklarını kullanırsınız. Finance and Operations numaraları tüm işlemlerde kullanır.

Finance and Operations'ı uyguladığınızda, ürün numaralarıyla ilgili stratejinize özel bir önem vermeniz gerekir. İyi bir numaralandırma sistemi lojistik akışları geliştirir ve hataları engellemeye yardımcı olur. İyi bir ürün tanımlayıcısı en çok 15 karakter uzunluğundadır. İdeal olarak, 10 karakterden daha kısa olur ve en fazla beş sınıflandırma karakteri içerir. Ayrıca, hızlı aramalar sağlamak için arama adlarını da kullanabilirsiniz. Bir arama adı bir ürünün sınıflandırmalarını temsil eden ek bir addır.

Common Data Service (CDS) kullandığınızda, Finance and Operations'taki ürün numarası aynı zamanda CDS'deki ürün numarasıdır. Ürün çeşitleri CDS ile ayrı ürünler olarak eşitlenir.

## <a name="item-number-and-product-dimensions"></a>Madde numarası ve ürün boyutları

Madde numarası, belirli bir tüzel kişilik tarafından kullanılan ürün tanımlayıcısıdır. İdeal olarak, madde numarası ürün numarası ile aynı olmalıdır. Terminoloji her tüzel kişilik için farklıysa, bir ürünü tedarik zinciri boyunca izlemek zorlaşır ve zahmetli yeniden etiketleme ve referans verme işlemleri ile karşılaşılır. Önceki sürümlerle (diğer bir deyişle, Microsoft Dynamics AX 2009 ve öncesi ile) uyumluluk için bu modeli sakladık. Ancak, tüzel kişiliklere özgü olan tanımlayıcıları mümkün olduğunca elemenizi ve bunun yerine birincil tanımlayıcı olarak benzersiz ürün numarası kullanmanızı öneririz.

Ayrıca, bir ürün çeşidi bir madde numarası ile benzersiz olarak tanımlanamaz. Her zaman bir madde numarası ile ana üründe tanımlanan tüm ürün boyutlarının birleşimini gerektirir. Bu gereksinim zahmetli olabilir ve tanımlama süreçlerini yavaşlatabilir. Bu nedenle de, mümkün olduğunda madde numarası yerine benzersiz ürün numarası kullanmanızı öneririz.

Birçok sayfada hala birincil tanımlayıcılar olarak madde numarası ve ürün boyutları bulunmaktadır. Ancak, ürün numaraları aramalar için kullanılabilir. **Satış ve pazarlama** &gt; **Kurulum** &gt; **Arama** &gt; **Arama parametreleri**'nde, aramayı birincil arama stratejisi olarak madde numaraları yerine ürün numaralarını kullanacak şekilde değiştirebilirsiniz. **Aramayı ürün araması için etkinleştir** seçeneğini **Evet** olarak ayarlarsanız, arama yalnızca ana ürünleri değil ürün çeşitlerini de gösterir. Daha fazla bilgi için bkz. [Sipariş girişi sırasında ürünleri ve ürün çeşitlerini arama](search-products-product-variants.md).

Ayrıca, ürün numarasını, ürün adını ve açıklamasını ve ürün çeşidinin ürün boyutu kodlarını arayabilir ve filtreleyebilirsiniz. Bir ürün çeşidi seçtiğinizde, ilgili madde numarası ve tüm ürün boyutu kodları seçilir. Bu nedenle, doğru ürün çeşidini kolayca bulabilir ve seçebilirsiniz. Ürünler için birincil tanımlayıcılar olarak ürün çeşitlerini ve benzersiz bir ürün numarasını kullanıyorsanız bu ayar önemle önerilir. Tek özel durum iş süreçlerinin genellikle bir ürün çeşidi seçmeden önce ana ürün seçmenizi gerektirdiği moda sektörü olabilir. Numaralama sistemini uygulamadan önce bu seçeneği dikkatli şekilde değerlendirmeniz gerekir.

## <a name="product-name-and-description"></a>Ürün adı ve açıklaması

Ürün adı ve açıklaması, bir ürünün insanlar tarafından okunan tanımlayıcılarıdır ve birçok dilde olabilir. Varsayılan olarak, Finance and Operations istemcisi tüm ürün bilgilerini kullanıcının dilinde değil şirketin varsayılan dilinde gösterir. Ancak, çevrilmiş ürün adları ve açıklamaları müşteriler ve satıcılarla yapılan tüm iletişimlerde kullanılır. Çeviriler müşteri ve satıcı hesaplarının dil kodunu temel alır.

Ürün çeşitleri için, ürün adı ürün terminolojisi şablonu aracılığıyla oluşturulabilir. Ürün adlarının benzersiz olmasına ilişkin bir gereksinim olmadığından, aynı ada sahip birden fazla ürün olduğunu görebilirsiniz.

## <a name="product-and-item-search-names"></a>Ürün ve madde arama adları

Finance and Operations ürünler ve maddeler (serbest bırakılan ürünler) için ikincil bir arama adı sağlar. Bu arama adı benzersiz olmak zorunda değildir ve bir ürün veya ürün çeşidi oluşturulduktan sonra değiştirilebilir. Ürünleri kategorilere göre aramak için arama adı kullanmanızı öneririz. Arama adları özellikle satış ve satınalma işlemlerinde hızlı aramalar yapılmasını sağlar.

Bir arama adı bir müşteri ve satıcı ürünü kodunu veya harici kodun ürün için birincil arama ölçütü olması durumunda başka bir harici ürün kodunu da içerebilir.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Harici ürün tanımlayıcıları (Müşteri ve satıcı tanımlayıcıları)

Serbest bırakılan ürünler için müşteri veya satıcının kullandığı madde numaralarını, madde adlarını ve madde açıklamalarını kullanabilirsiniz. Referanslar satış siparişleri, satınalma siparişleri, sevk irsaliyeleri ve faturalar gibi harici belgelerde gösterilir. Finance and Operations'ın geçerli sürümünde, harici referanslar temel işlem sayfalarında gösterilmez. Tek özel durum satıcı madde numarasıdır. Bu numara, serbest bırakılan ürün için varsayılan bir satıcı tanımlanmış olması durumunda **Ürün bilgisi** iletişim kutusunda gösterilir.

Harici ürün tanımlayıcıları serbest bırakılan ürün, serbest bırakılan ürün çeşidi, müşteri veya müşteri grubu veya satıcı veya satıcı grubuna göre sağlayabilirsiniz.

**Serbest bırakılan ürünler** sayfasında, aşağıdaki adımlardan birini izleyin.

- Müşteriler için, **Satış** sekmesindeki **İlgili bilgiler** grubunda **Harici madde açıklaması**'nı seçin.
- Satıcılar için, **Satınalma** sekmesindeki **İlgili bilgiler** grubunda **Harici madde açıklaması**'nı seçin.

**Harici madde açıklamaları** sayfasında, müşteri veya satıcının madde numarasını serbest bırakılan bir ürünle ilişkilendirebilirsiniz. Bu ilişki her tüzel kişilik için yapılmalıdır. Aşağıdaki bilgiler alınabilir. Ne yazık ki, Finance and Operations'ın geçerli sürümünde etiketler biraz yanıltıcıdır. Bununla birlikte, bu etiketler gelecekteki bir sürümde değiştirilebilir.

| Alan | İlgili müşteri bilgileri | İlgili satıcı bilgileri |
|-------|------------------------------------|----------------------------------|
| Harici madde numarası | Müşterinin madde numarası | Satıcının madde numarası |
| Tanım | Müşterinin maddeyle ilişkilendirdiği ad | Satıcının maddeyle ilişkilendirdiği ad |
| Harici madde metni | Müşterinin madde açıklaması | Satıcının madde açıklaması |

Birçok müşteri veya satıcı aynı madde numaralarını kullanıyorsa (örneğin satınalma ilişkisi veya perakende grubunda olduğu gibi), harici ürün bilgilerinin bakımını basitleştirmek için müşteri veya satıcı grupları oluşturabilirsiniz.

- Müşteri grupları için **Satış** &gt; **Kurulum** &gt; **Maddeler** &gt; **Harici madde açıklaması**'na giderek grupları ve ilgili madde numaralarını oluşturun ve sağlayın. Müşterileri bir grupla ilişkilendirmek için **Alacak hesapları** &gt; **Müşteriler** &gt; **Tüm müşteriler**'e gidin ve daha sonra **Satış siparişi varsayılanları** hızlı sekmesindeki **Madde - müşteri grubu** alanında bir değer belirtin.
- Satıcı grupları için **Tedarik ve kaynak atama** &gt; **Kurulum** &gt; **Harici madde açıklaması grubu**'na giderek grupları ve ilgili madde numaralarını oluşturun ve sağlayın. Satıcıları bir grupla ilişkilendirmek için **Borç hesapları** &gt; **Satıcılar** &gt; **Tüm satıcılar**'a gidin ve daha sonra **Satınalma siparişi varsayılanları** hızlı sekmesindeki **Madde - satıcı grubu** alanında bir değer belirtin.
 
## <a name="bar-codes"></a>Barkodlar

Ürünleri tanımlamak için bir barkod tarayıcısı kullanmak istiyorsanız, ürün tanımlayıcısının kullanılan barkod standardı gereksinimlerini karşılaması gerekir. Bu nedenle, bar kodlar genellikle ham ürün numarasını içerir ancak numara seçili barkodun teknolojisi için özel olarak oluşturulan bir numaradır. Barkod türüne göre birden fazla barkod sağlayabilirsiniz. Birden fazla ürünü aynı barkod ile ilişkilendirebilir ve ardından bir barkodu tararken gerçek etkin ilişkilendirmeyi seçebilirsiniz.

Barkodları tanımlamadan önce bir veya daha fazla barkod kurulumu tanımlayabilirsiniz. Barkod kurulumları, barkodların gerekli yönergeleri izlediğini ve böylece etkin şekilde yazdırılabileceğini ve taranabileceğini doğrulamaya yardımcı olur. Belirli ürün miktarları için özel barkodlar da sağlayabilirsiniz.

Uluslararası Madde Numarası (EAN) veya Global Ticaret Madde Numarası (GTIN) kodları sağlamak için barkod kurulumunu kullanmanızı öneririz.

Barkodlar sağlamak için **Serbest bırakılan ürünler** sayfasında, **Stoğu yönet** sekmesindeki **Ambar** grubunda **Barkodlar**'ı seçin.

## <a name="gtin-codes"></a>GTIN kodları

E-ticarette, tüm tarafların ortak bir dili konuşması ve ürünlere ortak bir tanımlayıcılar kümesi kullanarak referans vermesi önemlidir. Bu nedenle bazı sektörler, GS1 tarafından sağlanan global madde numarası sistemi olan [GTIN](https://www.gs1.org/id-keys/gtin)'e güvenir.

Finance and Operations'da, barkod olarak GTIN sağlamanızı öneririz. Ancak, **Madde - GTIN** sayfasından da sağlayabilirsiniz. Bu sayfayı açmak için, **Serbest bırakılan ürünler** sayfasında, **Stoğu yönet** sekmesindeki **Ambar** grubunda **GTIN kodları**'nı seçin. GTIN kodunun global numara olarak sağlanmayacağını unutmayın. Bunun yerine, bu tüzel kişiliğe göre sağlanır.

Finance and Operations'da, belirli ölçü birimleri tanımlayarak ambar işlemlerinde paketleme değişkenlerini tanımlarsınız. Örneğin, bir madde parçalar, altılı paketler, 18'lik tepsiler veya tam paletler halinde depolanabilir. Bu paketleme değişkenlerinin her biri için belirli bir ölçü birimi tanımlanır. GTIN genellikle bir ürünün paketleme birimiyle ilgili olduğundan **Madde - GTIN** sayfası ürün ve ölçü birimi başına çoklu GTIN kodları sağlamanıza olanak tanır. Ancak, aynı GTIN kodunu bir tüzel kişilikteki farklı maddeler veya ürün çeşitleri için bir kereden fazla kullanamazsınız.

**GTIN kodlarını** sağlamak için **Serbest bırakılan ürünler** sayfasında, **Stoğu yönet** sekmesindeki **Ambar** grubunda **GTIN**'yi seçin.

## <a name="external-codes"></a>Harici kodlar

Finance and Operations'da harici kodlar birçok varlık için tanımlanabilir. Örneğin, ürünleri ve serbest bırakılan ürünleri tanımlamak için harici kodlar tanımlayabilirsiniz. Bu harici kodlar istatistiksel kodları ya da vergi kodlarını serbest bırakılan ürünler ve serbest bırakılan ürün çeşitleriyle ilişkilendirmek için kullanılabilir. Harici kodlar tüzel kişilik ve kod türü ile tanımlanır. Tüzel kişilik, kod türü ve tablo referansı için benzersiz olmaları gerekir.

Ne yazık ki, harici kodlara göre ürünleri aramanızı sağlayan standart bir işlev yoktur.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Ürün tanımlayıcılarını içe ve dışa aktarmak için kullanılan veri varlıkları

| Varlık adı | Tanımlayıcıları içe aktarma | Tanımlayıcıları dışa aktarma | Yorumlar |
|-------------|--------------------|--------------------|----------|
| Ürünler V2 | Ürün numarası, ürün arama adı, ürün adı, ürün açıklaması | Ürün numarası, ürün arama adı, ürün adı, ürün açıklaması | Ürün numarası için numara serisi ve varlık ayarlarına bağlı olarak ürün numarası içe aktarma sırasında otomatik olarak oluşturulabilir. |
| Ürün çeşitleri | Ürün numarası, ürün arama adı, ürün adı, ürün açıklaması | Ürün numarası, ürün arama adı, ürün adı, ürün açıklaması | Ürün terminolojisi şablonuna bağlı olarak ürün numarası, içe aktarma sırasında otomatik olarak oluşturulabilir. Bununla birlikte, tüm benzersiz bir ürün numaralarını içe aktarabilirsiniz ve ürün numarasının ürün terminolojisi şablonlarının yapısını izlemesi gerekmez. |
| Ürün çevirileri | Ürün adı, ürün açıklaması | Ürün adı, ürün açıklaması | Bu varlık herhangi bir dil üzerine yazılır. Bir tüzel kişiliğinin adının veya açıklamasının birincil dili üzerine yazıldığında, ürünün adı ve açıklaması değişir. |
| Serbest bırakılan ürünler V2 | Madde numarası, ürün numarası, madde arama adı| Madde numarası, ürün numarası, madde arama adı, ürün arama adı, ürün adı | Numara serileri yeni serbest bırakılan ürünler oluşturulurken kullanıldığında, bu varlıkla ilgili zorluklarla karşılaşılabilir. Hem **Madde numarası** numara serisinin hem de **Ürün numarası** numara serisinin bir etkisi vardır. Bununla birlikte, **Madde numarası** numara serisi tüzel kişiliğe göredir ve **Ürün numarası** numara serisi geneldir. Bu nedenle, yeni serbest bırakılan ürünler dağıtırken **Madde numarası** numara serisini kullanmanızı önermeyiz. Açıkça, varlık varolan bir ürünü serbest bırakmak için kullanıldığında, ürün numarasının varlıkta verilmesi gerekir. Daha fazla bilgi için bu konudaki "Ürün ve madde numarası serileri" bölümüne bakın. |
| Serbest bırakılan ürün çeşitleri | Madde numarası, ürün boyutları, ürün numarası | Ürün numarası, ürün arama adı, ürün adı, ürün açıklaması, ürün boyutları | **Ürün çeşitleri** varlığı gibi, bu varlık da ürün terminolojisi şablonunu izleyen veya ürün çeşidi için kendi ürün numaralarını kullanan yeni ürünler oluşturmak için kullanılabilir. |
| Müşteriler için harici madde açıklaması | Müşteri madde numarası, müşteri madde adı, müşteri açıklaması, müşteri hesabı | Müşteri madde numarası, müşteri madde adı, müşteri açıklaması, müşteri hesabı | Bir grup müşteri (örneğin, alıcı ilişkilendirmesi) **Harici madde açıklaması müşteri grupları** varlığı kullanılarak tek bir grupta toplanabilir. |
| Satıcılar için harici madde açıklaması | Satıcı madde numarası, satıcı madde adı, satıcı açıklaması, satıcı hesabı | Satıcı madde numarası, satıcı madde adı, satıcı açıklaması, satıcı hesabı | Bir grup satıcı (örneğin, satış ilişkilendirmesi ve sektör organizasyonu) **Harici madde açıklaması satıcı grupları** varlığı kullanılarak tek bir grupta toplanabilir. |
| Madde Barkod | Barkod | Barkod | İçe aktarma sırasında, hedef sistemde tanımlanan bir barkod kurulumuna başvurmanız gerektiğini unutmayın. İçe aktarılan barkod referansları, barkod kurulumuna karşı doğrulanır ve barkodlar baroda kurulumunda tanımlanan gereksinimlerle eşleşmiyorsa reddedilir. |
| Serbest bırakılan ürünler için harici kodlar | Harici kod | Harici kod, harici kod sınıfları, madde numarası | Harici kodlar tüzel kişiliğe göredir. İçe aktarma için tanımlanmış bir kod sınıfına başvurulması gerekir. **Serbest bırakılan ürünler için harici kod sınıfları** varlığını kullanarak kod sınıflarını içe aktarın. |
| Serbest bırakılan ürün çeşitleri için harici kodlar | Harici kod | Harici kod, harici kod sınıfları, madde numarası, ürün boyutları | Harici kodlar tüzel kişiliğe göredir. İçe aktarma için tanımlanmış bir kod sınıfına başvurulması gerekir. **Serbest bırakılan ürünler için harici kod sınıfları** varlığını kullanarak kod sınıflarını içe aktarın. Bu varlık madde numarası ve ürün boyutlarına göre ürün çeşitlerine başvurur. |
| Ürün numarası tanımlayıcısına göre serbest bırakılan ürün çeşitleri için harici kodlar | Harici kod | Harici kod, harici kod sınıfları, ürün numarası | Harici kodlar tüzel kişiliğe göredir. İçe aktarma için tanımlanmış bir kod sınıfına başvurulması gerekir. **Serbest bırakılan ürünler için harici kod sınıfları** varlığını kullanarak kod sınıflarını içe aktarın. Bu varlık ürün çeşidinin ürün numarasına göre ürün çeşitlerine başvurur. (Sonraki ana sürümden itibaren) |
| GTIN | Uygulanamaz | Uygulanamaz | Şu anda GTIN kodlarını içe ve dışa aktarmak için kullanılan özel varlık yoktur. Bunun yerine **Madde Barkod** varlığını kullanmanızı öneririz. |
| Ürün varlığı common data service tanımlayıcısı varlığı | Uygulanamaz | Madde numarası, madde arama adı, ürün arama adı, satıcı madde numarası, müşteri madde numarası, harici kodlar, GTIN kodları, barkodlar | Bu varlık tüm tanımlayıcıları tek bir veri modelinde birleştirir böylece tüm tanımlayıcıları ve ilgili türlerini dışa aktarmak için tek bir arayüz kullanılabilir. Tanımlayıcı kodlarını ve açıklamalarını dışa aktarmak için **Ürün varlığı tanımlayıcı kodu** varlığını kullanın. Bir tanımlayıcıya taraf, varlık, miktar veya birim gibi ek kapsam bilgilerini aktarmak için **Ürün varlığı tanımlayıcısı kapsamı** varlığını kullanın. |

### <a name="product-and-item-number-sequences"></a>Ürün ve madde numarası serileri

Finance and Operations'da, iki farklı numara serisi tanımlayabilirsiniz:

- Global ürün numarası için **Ürün numarası** numara serisi
- Tüzel kişiliğe göre madde numarası için **Madde numarası** numara serisi

> [!NOTE]
> Yalnızca farklı numaralandırma sistemleri olan farklı kaynaklardaki farklı tüzel kişilikleri taşırken madde numarasını ayrı bir tanımlayıcı olarak kullanmanız gerekir. Tüm tüzel kişilikler arasında benzersiz olan bir ürün tanımlayıcısı kullanmaya çalışmanız gerekir. Bu nedenle, **Madde numarası** numara serisi için **El ile** seçeneğini **Evet** olarak ayarlamanız gerekir. Bu şekilde, madde numarası oluşturma sırasındaki ürün numarasını izler. Finance and Operations yeni ürün numaraları için önde gelen sistem değilse, **El ile** seçeneğini hem **Madde numarası** hem de **Ürün numarası** numara serileri için **Evet** olarak ayarlamanız gerekir.

Ürünleri oluşturmak için **Serbest bırakılan ürün V2** kullandığınızda, ürün numarası ve madde numarası oluşturmak için numara serilerinin nasıl kullanılacağı birden fazla ayar tarafından etkilenebilir.

- **Ürün numarası** numara serisi ayarları
- **Madde numarası** numara serisi ayarları
- Madde numarasının eşlenmesi 
- Ürün numarasının eşlenmesi

Aşağıdaki tablo, belirli numara serisi ve alan eşleme ayarları birleşimlerinde içe aktarma ve el ile oluşturma sonuçlarına ilişkin genel bir görünümün sağlar.

| Ürün numarası numara serisi | Madde numarası numara serisi | Madde numarasının eşlenmesi | Ürün numarasının eşlenmesi | Varlık içe aktarmanın sonucu | El ile oluşturmanın sonucu | Sonuç |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| El ile = Hayır | El ile = Hayır | Eşleme yok | Eşleme yok | Ürün numaraları **Ürün numarası** numara serisini kullanır. Madde numaraları **Madde numarası** numara serisini kullanır. | Ürün numaraları **Ürün numarası** numara serisini kullanır. Madde numaraları **Madde numarası** numara serisini kullanır. | Bu ayarlar, ürünler ve maddeler için farklı numara gerekli olduğunda kullanılabilir. Bununla birlikte, maddeler ve ürünler için farklı numaralar kullanmanızı önermeyiz. |
| El ile = Hayır | El ile = Evet | Otomatik oluştur | Eşleme yok | Hem ürün numaraları hem de madde numaraları **Madde numarası** numara serisini kullanır. | Hem ürün numaraları hem de madde numaraları **Ürün numarası** numara serisini kullanır. | Bu ayarlar önerilmez. İçe aktarma ve el ile oluşturma farklı çalışır. |
| El ile = Hayır | El ile = Evet | Eşleme yok | Eşleme yok | Hem ürün numaraları hem de madde numaraları **Ürün numarası** numara serisini kullanır. | Hem ürün numaraları hem de madde numaraları **Ürün numarası** numara serisini kullanır. | Bu ayarlar, içe aktarma veya el ile oluşturma kullanılıp kullanılmadığından bağımsız olarak, ürünlerin tutarlı otomatik numaralamaya sahip olması gerektiğinde önerilir. |
| El ile = Evet | Uygulanamaz | Uygulanamaz | Otomatik oluştur | Aşağıdaki hata iletisini alırsınız: "Numara serisi algılanamadı" | **Madde numarası** numara serisine göre | Bu ayar içe aktarma için desteklenmez. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Ürün varlığı tanımlayıcısı (Tüm ürün tanımlayıcılarını dışa aktarma)

Ürün varlığı tanımlayıcısı modeli, CDS 1.0 sürümünün ürüne başvurmak için kullanılan tüm tanımlayıcılarla birlikte sağlanabilmesine olanak tanımak için oluşturuldu. Bu görevi basitleştirmek için tüm tanımlayıcılar tek bir genel tanımlayıcı tablosunda toplanır ve böylece tek bir model olarak dışa aktarılabilir. CDS'nin bu sürümünün ürün tanımlayıcıları modelini kullanmadığını unutmayın. Bu nedenle, **Ürün varlığı common data service tanımlayıcı varlığı** varlığı ve bu işlemin kullanımı sınırlıdır ve gelecek sürümlerde değiştirilebilir.

Ürün tanımlayıcısı tablosu, yinelenen toplu iş işiyle Ana tüzel kişiliğin tüm referans tablolarından doldurulan genel bir tablodur. Genel ana ürün kapsamı tanımı olarak bir tüzel kişilik ve bir ürün kategori hiyerarşisi seçmeniz gerekir. Genel ürün tanımlayıcısı tablosu oluşturma, seçili tüzel kişiliğe serbest bırakılan ürünler ve ürün kategori hiyerarşisinde **Common data service** rolü için seçilen ürün hiyerarşisinin üyesi olan ürünlerle sınırlandırılmıştır.

Bu işlem ana ürün verilerinin öncelikle bir merkezi tüzel kişilikte tutulduğunu kabul eder. (Ancak, bu tüzel kişilik yalnızca genel ana verileri korumak için kullanılan sanal bir tüzel kişilik olabilir.)

Ortamı yapılandırmak için şu adımları izleyin.

1. CDS için kategori hiyerarşisini seçin. **Kategori hiyerarşisi rol ilişkileri** sayfasında, **Common data service** rolüyle ilişkilendirilmiş hiyerarşi yoksa, yeni bir ilişki oluşturmanız gerekir. **Common data service** rolünü seçin ve CDS ile eşitlenmesi gereken ürün portföyünü temsil eden kategori hiyerarşisini ilişkilendirin.
2. Genel ana ürün verileri için tüzel kişiliği seçin. **Ürün bilgileri yönetimi parametreleri** sayfasında **Ürün öznitelikleri** sekmesinde, ürünün ve madde tanımlayıcıların birincil olarak tutulacağı ana şirketi seçin.
3. Tanımlayıcı kod türlerini ve dışa aktarılması gereken kodları tanımlayın. **Ürün yönetimi bilgileri** &gt; **Kurulum** &gt; **Ürün tanımlayıcısı kodları**'na gidin. Tanımlayıcı kod türlerini oluşturmak için **Kodlar oluştur**'u seçin. Seçilen tüzel kişilikte bulunan her tanımlayıcı türü için bir kod türü girişi oluşturulur.

    Barkodlar için, her barkod kurulumunda bir kod türü oluşturulduğunu unutmayın. Harici kodlar için, her harici kod sınıfı için bir kod türü oluşturulur.

    Şimdi kod türlerinin listesini sağlayabilirsiniz. Kodu, adı ve açıklamayı değiştirebilirsiniz. Aynı zamanda kod türlerini de silebilirsiniz. Sildiğiniz kod türleri, genel ürün varlığı tanımlayıcı tablolarını doldurmak için kullanılmaz.

4. Ürün tanımlayıcı kod türlerini tanımlamayı bitirdiğinizde, tanımlayıcıları genel tabloda **Ürün varlık tanımlayıcısı kodları** sayfasındaki **Ürün varlık tanımlayıcıları oluştur** işini başlatarak oluşturabilirsiniz. Bu işi bir toplu işte çalıştırmanız gerekir. Tablonun yeni girişlere göre doldurulabilmesi için işin periyodik bir toplu iş olarak ayarlanması gerekir.

Artık herhangi bir hedef sistem için tanımlayıcıları dışa aktarmak için **Ürün varlığı common data service tanımlayıcısı varlığı**, **Ürün varlık tanımlayıcısı kodu** ve **Ürün varlık tanımlayıcısı kapsamı** veri varlıklarını kullanabilirsiniz.

## <a name="related-topic"></a>İlgili konu

[Sipariş girişi sırasında ürünleri ve ürün çeşitlerini arama](search-products-product-variants.md)
