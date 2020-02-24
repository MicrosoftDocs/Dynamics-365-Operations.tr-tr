---
title: Perakende satış fiyatı yönetimi
description: Bu konu Dynamics 365 Commerce'de satış fiyatları oluşturma ve yönetme kavramlarını açıklar.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f3f2616fd98b37576625d9586a1cda29ce1b89f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024374"
---
# <a name="retail-sales-price-management"></a>Retail satış fiyatı yönetimi

[!include [banner](includes/banner.md)]

Bu konu Dynamics 365 Commerce içinde satış fiyatlarını oluşturma ve yönetme işlemini açıklar. Bu işlemine dahil olan kavramlara ve satış fiyatlarına ilişkin çeşitli yapılandırma seçeneklerinin etkisine odaklanır.

## <a name="terminology"></a>Terminoloji

Bu konuda şu terimler kullanılmıştır.

| Vade | Tanım, kullanım ve notlar |
|---|---|
| Fiyat | bir satış noktası (POS) istemcisinde veya satış siparişinde ürünün satıldığı tek bir birim tutarı. Bu konuda *fiyat* terimi stok fiyatı veya maliyet fiyatını değil her zaman satış fiyatını belirtir. |
| Taban fiyat | Serbest bırakılan bir üründe **Fiyat** alanında ayarlanan fiyat. |
| Ticari sözleşme fiyatı | **Fiyat (satış)** türünde ticari sözleşme kullanılarak bir ürün veya ürün çeşidi üzerinde ayarlanan fiyat. |
| En iyi fiyat | Bir ürüne birden fazla fiyat veya iskonto uygulanabildiğinde, en küçük satış tutarı ve/veya müşterinin ödemesi gereken olası en düşük net tutarı üreten en büyük iskonto tutarı. Bu konuda en iyi fiyat kavramı her zaman için "en iyi fiyat" olarak geçer Bu en iyi fiyat iskonto eşzamanlılık moduna ilişkin **En iyi fiyat** numaralandırma değerinden farklıdır ve bununla karıştırılmamalıdır. |

## <a name="price-groups"></a>Fiyat grupları

Fiyat grupları Commerce'de fiyat ve iskonto yönetiminin merkezinde yer alır. Fiyat grupları perakende varlıklarına (kanallar, ilişkiler, kataloglar ve bağlılık programları) fiyatlar ve iskontolar atamak için kullanılır. Fiyat grupları tüm fiyat ve iskontolar için kullanıldığından, başlamadan önce bunları nasıl kullanacağınızı planlamak çok önemlidir.

Tek başına bir fiyat grubu yalnızca bir ad, bir açıklama ve isteğe bağlı olarak bir fiyatlandırma önceliğidir. Fiyat grupları hakkında hatırlanması gereken ana nokta fiyatların perakende varlıklar ile birlikte fiyatlar ve iskontoların sahip olduğu çok-çok ilişkileri yönetmek için kullanılmasıdır.

Aşağıdaki örnek fiyat gruplarının nasıl kullanılacağını gösterir. Bu örnekte, "Fiyat grubu"nun tam olarak fiyatlama ve iskonto yönetiminin merkezinde olduğunu unutmayın. Farklı fiyatları ve iskontoları yönetmek için kullanabileceğiniz perakende varlıkları solda ve gerçek fiyat ve iskonto kayıtları sağdadır.

![Fiyat grupları](./media/PriceGroups.png "Fiyat grupları")

Fiyat grupları oluştururken, birden fazla türdeki perakende varlıklar için tek bir fiyat grubu kullanmamanız gerekir. Aksi takdirde, neden belirli bir fiyat veya iskontonun harekete uygulandığını belirlemek zor olabilir.

Örnekteki kırmızı çizgili satırda da gösterildiği gibi, Commerce, Microsoft Dynamics 365'teki doğudan bir müşteriden ayarlanan fiyat grubu işlevini desteklemez. Bununla birlikte, bu durumda, yalnızca satış fiyatı ticari sözleşmelerini alırsınız. Müşteriye özel fiyatları uygulamak isterseniz, doğrudan müşteri üzerinden fiyat grupları ayarlamamanızı öneririz. Bunun yerine, ilişkileri kullanın.

Aşağıdaki bölümler fiyat grupları kullanıldığında ayrı gruplar ayarlamak için kullanabileceğiniz perakende varlıklar hakkında daha fazla bilgi sağlar. Bu varlıklar için fiyatları ve iskontoları yapılandırma iki aşamalı bir işlemdir. Bu adımlar her iki sırayla da yapılabilir. Ancak, bu adım uygulama sırasında bir kez yapılacak bir kurulum olduğundan mantıksal sıra önce varlıklarda fiyat gruplarını ayarlamaktır. Ardından, fiyatlar ve iskontolar oluşturulduğunda, bu fiyatlar ve isontolar üzerinde fiyat gruplarını ayrı ayrı ayarlayabilirsiniz.

### <a name="channels"></a>Kanallar

Perakende sektöründe farklı kanallarda farklı fiyatlar olması çok normaldir. Kanala özel fiyatları etkileyen iki temel faktör maliyetler ve yerel piyasa koşullarıdır.

- **Maliyetler** – Bir kanal ürün kaynağından ne kadar uzaksa, bir ürünü stoklamanın maliyeti o kadar fazla olur. Örneğin, taze ürünlerin sınırlı raf ömrü ve özel üretim gereksinimleri bulunur (örneğin yetişme mevsimi). Kış aylarında taze yeşil salatanın maliyeti kuzey iklimlerde güney iklimlere göre daha yüksek olacaktır. Geniş bir coğrafi alan üzerinde kanallar için fiyatlar ayarlıyorsanız, farklı kanallarda farklı fiyatlar ayarlamak isteyeceksiniz.
- **Yerel piyasa koşulları** – Cadde üzerinde doğrudan rakibi olan bir mağaza yakınlarda doğrudan rakibi olmayan bir mağazaya göre fiyat konusunda çok daha hassas olacaktır.

### <a name="affiliations"></a>İlişkiler

Bir ilişkinin genel tanımı bir grupla bağlantı veya ilişkilendirmedir. Commerce'de, ilişkiler müşteri gruplarıdır. İlişkiler müşteri fiyatlandırma ve iskontolar için temel Microsoft Dynamics 365 müşteri grupları ve iskonto grupları kavramından çok daha esnektir. İlk olarak, bir ilişki hem fiyatlar hem iskontolar için kullanılabilirken, perakende olmayan bir fiyatın her iskonto ve fiyat türü için farklı bir grubu bulunur. Daha sonra, bir müşteri birden fazla ilişkiye ait olabilir ancak her türden yalnızca bir perakende olmayan fiyat grubuna ait olabilir. Son olarak, ilişkiler bir müşteriye bağlı olacak şekilde ayarlanabilmesine karşın böyle olmaları gerekmez. POS'taki anonim müşteriler için geçici bir ilişki kullanılabilir. Anonim ilişki iskontosunun tipik bir örneği bir yönetici veya öğrenci iskontosudur; burada müşteri bir grup üyeliği kartı göstererek iskonto alabilir.

İlişkiler genellikle iskontolarla ilişkilendirilmesine karşın, bunları farklı fiyatlar ayarlamak için de kullanabilirsiniz. Örneğin, bir perakendeci bir çalışana satış yaptığında, normal fiyatın üzerinden iskonto uygulamak yerine satış fiyatını değiştirmek isteyebilir. Başka bir örnek olarak, hem tüketici müşterilere hem de kurumsal müşterilere satış yapan bir perakendeci kurumsal müşterilerine satınalma hacmine göre daha iyi fiyatlar sunabilir. İlişkiler bu her iki senaryoyu da mümkün kılar.

### <a name="loyalty-programs"></a>Bağlılık programları

Fiyatlar ve iskontolarla ilişkili olarak, bağlılık programları temelde özel bir adı olan bir ilişkidir. Hem fiyatlar hem de iskontolar bir bağlılık programı için ayarlanabilir veya bir ilişki için ayarlanabilir. Ancak, müşterilerin bir hareket veya siparişi sırasında bağlılık programı fiyatı alma şekli ilişki fiyatı alma yöntemlerinden farklıdır. Müşteriler bağlılık programı fiyatını yalnızca harekete bir bağlılık programı kartı eklenmesi durumunda alabilirler. Bağlılık programı kartı harekete eklendiğinde, bağlılık programı da eklenir. Bağlılık programı daha sonra özel fiyatlar ve iskontolar etkinleştirir.

Bağlılık programlarında birden çok katman olabilir ve iskontolar farklı katmanlar için farklı olabilir. Bu şekilde, perakendeciler müşterileri el ile özel bir gruba koymak zorunda olmadan müşterilerine sıklıkla daha büyük ödüller verebilir.

Bağlılık programlarında fiyatlar ve iskontoların yanı sıra ek işlevler bulunur. Ancak, fiyat ve iskontolar açısından, bunlar ilişkilerle aynıdır.

### <a name="catalogs"></a>Kataloglar

Bazı perakendeciler ürünlerini odaklanmış müşteri gruplarına pazarlamak ve fiyatlandırmak için fiziksel veya sanal kataloglar kullanırlar. Katalogla pazarlamayı hedefleme iş modellerinin bir parçası olarak bu perakendeciler çeşitli kataloglar üzerinde farklı fiyatlar ayarlayabilirler. Microsoft Dynamics 365 kataloğa özel iskontolar ve fiyatlar tanımlamanıza olanak tanıyarak bu özelliği destekler; böylece kanala özel veya ilişkiye özel iskontolar tanımlayabilirsiniz. Bir kataloğu düzenlediğinizde, fiyat gruplarını bir kanalla, ilişkiyle veya bağlılık programıyla olduğu gibi katalogla da ilişkilendirebilirsiniz.

### <a name="best-practices-for-price-groups"></a>Fiyat grupları için en iyi uygulamalar

Birden fazla perakende varlık türü için bir fiyat grubu kullanmayın. Bunun yerine, kanallar için bir fiyat grubu kümesi, ilişkiler veya bağlılık programları için farklı bir fiyat grubu kümesi kullanın. Kullandığınız farklı türdeki fiyat gruplarını görsel olarak gruplandırmak için fiyat grubu adında bir önek veya sonek kullanabilirsiniz.

Bir müşteri üzerinde doğrudan fiyat grupları ayarlamaktan kaçının. Bunun yerine, bir ilişki kullanın. Bu şekilde müşterilere yalnızca satış fiyatı ticari sözleşmeleri değil her tür fiyat ve iskontoyu atayabilirsiniz.

## <a name="pricing-priority"></a>Fiyatlandırma önceliği

Tek başına bir fiyatlandırma önceliği bir numara ve açıklamadır. Fiyatlandırma öncelikleri fiyat gruplarına uygulanabilir veya doğrudan iskontolar için uygulanabilir. Fiyatlandırma öncelikleri kullanıldığında, perakendeciye fiyatların ve iskontoların ürünlere uygulanma sırasını denetleyerek en iyi fiyat ilkesini geçersiz kılma olanağı sağlar. Daha büyük bir fiyatlandırma öncelik numarası daha düşük bir fiyat öncelik numarasından önce değerlendirilir. Buna ek olarak, bir fiyat veya iskonto bir öncelik numarasında bulunursa, daha düşük öncelik numaralarına sahip fiyatlar veya iskontolar dikkate alınmaz.

Fiyat ve iskonto iki farklı fiyatlandırma önceliğinden önce gelebilir çünkü fiyatları ve iskontoları bağımsız olarak uygulamak için fiyat öncelikleri geçerli olur.

Fiyatlar için fiyatlandırma önceliği kullanmak için bir fiyat grubuna bir fiyatlandırma önceliği atamanız ve sonra o fiyat grubu için bir satış fiyatı ticari sözleşmesi oluşturmanız gerekir.

Fiyatlandırma önceliği özelliğinin amacı bir perakendecinin belirli mağazalar kümesinde daha yüksek fiyatlar uygulamak istediği senaryoyu desteklemektir. Örneğin, bir perakendeci Amerika Birleşik Devletleri'nin doğu sahili için bölgesel fiyatlar tanımlar ancak bazı ürünler için New York mağazalarında daha yüksek fiyat uygulamak ister çünkü bazı ürünleri şehirde satmak daha maliyetlidir ve/veya yerel pazar daha yüksek bir fiyatı kaldırabilir.

Bu konunun "En iyi fiyat" bölümünde açıklandığı gibi, genellikle perakende fiyatlandırma altyapısı iki fiyattan en düşük olanı seçer. Bu nedenle, perakendecinin genellikle iki fiyattan en yüksek olanı hem Doğu sahili hem de New York fiyat gruplarına sahip bir mağazada kullanmasını engeller. Fiyatlandırma önceliği özelliği kullanılmadan önce bu sorunu çözmek için perakendecinin her ürün için fiyatı iki kez tanımlaması ve her iki fiyat grubuna atamaması gerekir. Alternatif olarak, perakendecinin yüksek fiyatlı ürünleri normal, daha düşük fiyatlı ürünlerden ayırmak için ekstra fiyat grupları oluşturması gerekir.

Bununla birlikte, fiyatlandırma önceliği özelliği perakendeciye bölgesel fiyatlara ilişkin fiyatlandırma önceliğinden daha yüksek olan mağaza fiyatları için bir fiyatlandırma önceliği oluşturma olanağı tanır. Alternatif olarak, perakendeci yalnızca mağaza fiyatları için bir fiyatlandırma önceliği oluşturabilir ve bölgesel fiyatları 0 (sıfır) olan varsayılan fiyatlandırma önceliğinde bırakabilir. Her iki ayar da mağaza fiyatlarının daima bölgesel fiyatlardan önce kullanılmasını sağlamaya yardımcı olur.

### <a name="pricing-priority-example"></a>Fiyatlandırma önceliği örneği

Mağaza fiyatlarının diğer fiyatları geçersiz kıldığı bir örneği inceleyelim.

Ulusal bir perakendeci çoğu fiyatı bölgeye göre ayarlar ve dört bölgesi bulunur: Kuzey doğu, Güney doğu, Orta batı ve batı. Daha yüksek fiyatları destekleyebilecek çeşitli yüksek maliyetli pazarlar tanımlar. Bu pazarlar New York City, Chicago ve San Francisco Körfezi alanındadır.

Bu örnekte, Kuzey doğu bölgesini ayrıntılı inceleyeceğiz. Mağaza 1 Boston'da ve mağaza 2 Manhattan'dadır. Boston mağazası için iki fiyat grubu kanala bağlıdır: Kuzey Doğu ve Mağaza 1. Manhattan mağazası için üç fiyat grubu kanala bağlıdır: Kuzey Doğu, NYC ve Mağaza 2.

Perakendeci iki fiyatlandırma önceliği ayarlar: Yüksek maliyetin öncelik numarası 5 ve Mağaza fiyatlarının öncelik numarası 10'dur. (Varsayılan olarak, fiyatlandırma önceliğinin 0 \[sıfır\] olduğunu ve daha yüksek öncelik numarasına sahip bir fiyat veya iskontonun daha düşük öncelikli olandan önce kullanılacağını unutmayın) Kuzey Doğu fiyat grubu için fiyatlandırma önceliği varsayılan değer olan **0** (sıfır) olarak bırakılır. NYC fiyat grubu için fiyatlandırma önceliği **5** olarak ayarlanır çünkü New York City yüksek maliyetli bir pazardır. Mağaza 1 ve Mağaza 2 fiyat grupları için fiyatlandırma önceliği **10** olarak ayarlanır.

Perakendecinin sattığı iki üründen ürün 1 bir ticari T-shirt ürün 2 ise markaya özel moda bir kot pantolondur.

| Ürün | Kuzey Doğu fiyatı | NYC fiyatı | Mağaza fiyatı |
|---|---|---|---|
| Tişört | $15 | Ayarlanmadı | Ayarlanmadı |
| Moda kot | $50 | $70 | Ayarlanmadı |

Tişört hem Boston hem de Manhattan mağazalarında aynı fiyata ($15) satılır çünkü her iki kanala bağlı olan Kuzey Doğu fiyat grubunda tek bir fiyat ayarlanmıştır. Modaya uygun kot Boston mağazasında $50 fiyatla satılır çünkü bu fiyat bu mağaza için kullanılabilir olan tek fiyattır. Ancak, Manhattan mağazasında iki fiyat kullanılabilir: $50 ve $70. NYC fiyat grubu için fiyatlandırma önceliği 5 uzey Doğu fiyatlandırma grubu fiyatlandırma önceliği olan 0'dan (sıfır) yüksek olduğu için, fiyat POS sisteminde $70 olacaktır.

> [!NOTE]
> Her fiyatlandırma önceliği için, perakende fiyatlandırma altyapısı için mantık aracılığıyla tam geçiş gereklidir. Bu nedenle, fiyat ve iskonto hesaplaması performansını korumaya yardımcı olmak için fiyatlandırma önceliklerini tedbirli şekilde kullanmanız gerekir.

## <a name="types-of-prices"></a>Fiyat türleri

Microsoft Dynamics 365'de bir ürünün fiyatını üç yerde ayarlayabilirsiniz:

- Doğrudan üründe (taban fiyatı)
- Satış fiyatı ticari sözleşmesinde
- Fiyat ayarlamasında

Taban fiyatı ve ticari sözleşme fiyatı Dynamics 365'in temel parçasıdır ve Commerce kullanmasanız bile kullanılabilir. Fiyat ayarlama işlevi yalnızca Commerce'de kullanılabilir. Bir sonraki bölüm fiyatları ayarlamak için bu seçeneklerin her biri hakkında daha fazla bilgi sağlar ve bu seçeneklerin bir arada nasıl çalıştığını açıklar.

## <a name="setting-prices"></a>Fiyatları ayarlama

### <a name="base-price"></a>Taban fiyat

Bir ürün için fiyat ayarlamasının en kolay yapıldığı yer doğrudan üründür. Doğrudan bir üründe ayarladığınız değer genellikle ürünün temel fiyatı olarak adlandırılır. Taban fiyatı **Serbest bırakılan ürün ayrıntıları** sayfasının **Satış** sekmesindeki **Fiyat** alanında ayarlarsınız. Girdiğiniz değer şirket para birimi cinsindendir. Varsayılan olarak fiyat **Satış** sekmesinin **Birim** alanında ayarlanan ölçü birimi (UoM) cinsinden 1 miktar içindir. Bir ürünün gerçek birim başına fiyatı UoM'u, fiyat miktarını ve para birimini temel alır.

Bir ürünün herkes için tek bir fiyatı varsa, taban fiyat bu ürünün fiyatını yönetmek için en etkili yoldur. Fiyatları ayarlamak için ticari sözleşmeleri kullansanız bile, bir üründe taban fiyat da ayarlayabilirsiniz. Daha sonra **Tüm** ticari sözleşmeyi kullanmasanız bile, uygulanan ticari sözleşme olmadığında kullanılan bir geri dönüş fiyatınız olur.

Bir perakende kanal para birimi şirket para biriminden farklıysa, bu kanaldaki temel fiyat üründe ayarlanan fiyat üzerinde para birimi dönüştürme kullanılarak belirlenir.

Fiyat birimi genel bir senaryosu olmamasına karşın, fiyatlandırma altyapısı tarafından desteklenir. Fiyat birimi **0** (sıfır) dışında bir değere ayarlanırsa, birim başına fiyat Fiyat ÷ Fiyat birimine eşit olur. Örneğin, bir ürünün fiyatı $10,00 ve fiyat birimi 50 ise, 1 miktar için fiyat $0,20 (= $10.00 ÷ 50) olur.

### <a name="sales-price-trade-agreement"></a>Satış fiyatı ticari sözleşmesi

Ticari sözleşme günlüğü kullanarak, her ürün için satış fiyatı ticari sözleşmeleri oluşturabilirsiniz. Microsoft Dynamics 365'de satış fiyatı ticari sözleşmeleri için üç müşteri kapsamı vardır: **Tablo**, **Grup** ve **Tümü**. Müşteri kapsam belirli bir satış fiyatı ticari sözleşmesinin uygulandığı müşterileri belirler.

**Tablo** satış fiyatı ticari sözleşmesi doğrudan ticari sözleşmede ayarlanan tek bir müşteri içindir. Bu senaryo tipik bir perakende işletmeden kullanıcıya (B2C) senaryosu değildir. Ancak, bu durum oluşursa, fiyatlandırma altyapısı fiyatı belirlerken **Tablo** ticari sözleşmesini kullanır.

**Grup** satış fiyatı ticari sözleşmesi perakende işleviyle birlikte en çok kullanılan türdür. Commerce dışında **Grup** satış fiyatı ticari sözleşmeleri basit müşteri grubu içindir. Bununla birlikte, Commerce'de, müşteri grubu kavramı daha genel bir fiyat grubu olacak şekilde genişletilmiştir. Bir fiyat grubu bir kanala, ilişkiye, bağlılık programına veya kataloğa bağlanabilir. Fiyat grupları hakkında ayrıntılı bilgi için bu konudaki "Fiyat grupları" bölümüne bakın.

> [!NOTE]
> Ticari sözleşme fiyatı her zaman taban fiyattan önce kullanılır.

### <a name="price-adjustment"></a>Fiyat ayarlaması

Adından da anlaşılacağı gibi bir fiyat ayarlaması doğrudan ürün üzerinde veya bir ticari sözleşme kullanılarak ayarlanan fiyatı değiştirmek için kullanılır. Bir fiyat ayarlaması yalnızca fiyatı düşürmek için kullanılabilir, yükseltmek için kullanılamaz. Bir fiyat ayarlaması perakendecilerin zaman içinde ürünleri için fiyat indirimleri oluşturma, izleme ve yönetmesi için önerilen bir yoldur.

Üç tür fiyat ayarlaması vardır: yüzde, tutar ve fiyat. Yüzde veya tutar türündeki fiyat ayarlaması daima satış hareketine uygulanır. Ancak, fiyat türündeki bir fiyat ayarlaması yalnızca ayarlanan fiyat taban fiyat veya ticari sözleşme fiyatı kullanılarak ayarlanan fiyattan düşükse uygulanır. Bu nedenle, fiyat ayarlamasında ayarlanan fiyat ayarlanmayan fiyattan fazlaysa, fiyat ayarlaması kullanılmaz.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Bir hareketteki bir ürün için fiyat belirleme

Bir hareketteki fiyat ve iskonto hesaplaması müşteri için en iyi fiyatı bulma ilkesini kullanır. Bu ilkeye göre birden fazla fiyat bulunursa en düşük fiyat kullanılır. Ayrıca, tüm işlem için en büyük indirim tutarını oluşturan iskontolar birleşimi kullanılır. Bazı durumlarda, tek bir üründe daha küçük iskonto kullanılması gerekir; böylece hareketteki diğer ürünlere ek iskontolar uygulanabilir.

Müşteri için en iyi fiyatı bulma ilkesinin tek istisnası en az pahalı iskontoları karıştır ve eşleştir seçeneğidir. Bu seçenek, perakendecinin ürünleri seçip gruplandırırken belirlediği en az pahalı iskontoları etkinleştirir. Bu nedenle, bir hareket en az pahalı iskontoyu belirlemek için gerekenden daha fazla ürün içerirse, fiyatlandırma altyapısı müşteri için olası en küçük iskonto tutarını üreten ürünleri seçer.

Fiyatlandırma altyapısı her ürün için üç fiyat döndürür: taban fiyat, ticari sözleşme fiyatı ve etkin fiyat.

Taban fiyatı yalnızca üründeki özelliktir ve herkes için aynıdır.

Satış fiyatı ticari sözleşmesinde **Sonrakini Bul** seçeneği **Evet** olarak ayarlanmışsa, uygulanabilir satış fiyatı ticari sözleşmeleri için en düşük fiyat ticari sözleşme fiyatı olarak kullanılır. Ticari sözleşmeler fiyat grupları veya **TÜM** hesap kodu kullanılarak bulunabilir. Alternatif olarak, ticari sözleşmeleri doğrudan müşteriye atayabilirsiniz. **Sonrakini Bul** seçeneği **Hayır** olarak ayarlanmışsa, bulunan ilk ticari sözleşme fiyatı kullanılır. Hiçbir satış fiyatı ticari sözleşmesi bulunamazsa, ticari sözleşme fiyatı tabana fiyat eşit olarak ayarlanır.

Etkin fiyat ticari sözleşme fiyatını alınıp ürüne uygulanan en büyük fiyat ayarlaması uygulanarak hesaplanır. Hiçbir fiyat ayarlaması bulunamazsa veya hesaplanan etkin fiyat ticari sözleşme fiyatından yüksekse, etkin fiyat ticari sözleşme fiyatına eşit olarak ayarlanır. Bir fiyat ayarlaması kullanarak bir ürünün fiyatını yükseltemeyeceğinizi unutmayın. Uygulanabilir fiyat ayarlamaları yalnızca bir kanala, kataloğa, ilişkiye veya bağlılık programına atanan fiyat grupları kullanılarak bulunabilir.

## <a name="category-price-rules"></a>Kategori fiyatı kuralları

Commerce'de kategori fiyatı kuralları özelliği, bir kategorideki tüm ürünler için yeni ticari sözleşmeler oluşturmak için kolay bir yol sağlar. Bu özellik ayrıca kategorideki ürünler için mevcut ticari sözleşmeleri otomatik olarak bulmanıza ve sonlandırmanıza olanak tanır.

Mevcut ticari sözleşmeleri sonlandırma seçeneğini seçtiğinizde, sistem etkin ticari sözleşmesi bulunan kategorideki ürünler için yeni bir ticari sözleşme günlüğü oluşturur. Bununla birlikte, günlüğü el ile deftere nakletmeniz gerekir. Ayrıca, kategori fiyatı kuralları yalnızca aynı fiyat kuralını kullanıyor olmanız durumunda mevcut ticari sözleşmeleri bulabilir (yani, öncekiyle aynı kategoriyi kullanan yeni bir fiyat kuralı oluşturursanız). Aynı fiyat kuralını kullanmıyorsanız, mevcut ticari sözleşmeler sonlandırılmaz.

Fiyatlar kategori fiyat kurallarının **Fiyat kuralı** ve **Fiyat tabanı** alanı kullanılarak artırılabilir veya azaltılabilir.

- **Fiyat kuralı** alanında, kullanılacak fiyat değişikliği türünü seçin:

    - **Kar marjı** – Satış fiyatını hesaplamak için fiyat tabanının yüzdesi kullanılır. Örneğin, maliyeti 10,00 ve satış fiyatı 15,00 olan bir ürünün kar marjı yüzde 50'dir.
    - **Marj** – Satış fiyatının yüzdesi kar tutarını hesaplamak için kullanılır. Örneğin, maliyeti 10,00 ve satış fiyatı 15,00 olan bir ürünün marjı yüzde 33,3'tür.
    - **Sabit tutar** – Fiyat tabanına eklenen ve satış fiyatını hesaplamak için kullanılan tutar. Örneğin, maliyeti 10,00 ve satış fiyatı 15,00 olan bir ürünün sabit tutarı 5,00'dır.

- **Fiyat tabanı** alanında, değiştirilecek fiyat türünü seçin:

    - **Temel maliyet** – Perakendecinin tedarikçiye ödediği tutar.
    - **Taban fiyat** – Ticari sözleşmeler ve fiyat ayarlamaları uygulanmadan önceki satış fiyatı.
    - **Geçerli fiyat** – Ticari sözleşmeler ve fiyat ayarlamaları uygulandıktan sonraki satış fiyatı.

Kolayca farklı ürün kategorilerindeki çeşitli ürünlerin fiyatlarını güncelleştirmek için ek ürün kategorilerini kategori fiyatı kuralları ile birlikte kullanabilirsiniz.

## <a name="best-practices"></a>Önerilen yöntemler

Microsoft SQL Server Express, maliyeti nedeniyle (ücretsiz) genellikle kanal veritabanı için kullanılır. SQL Server Express'in donanım kısıtlamaları ve veri boyutu sınırları olduğunu unutmayın. Doğru şekilde planlamazsanız, SQL Server Express veri boyutunun sınırına hızlı bir şekilde ulaşabilirsiniz. Bu yalnızca fiyatlandırmayı değil ürünün diğer alanlarını da etkiler. Verilerinizin boyutunu düşürmeye yardımcı olabilecek birkaç en iyi yöntem aşağıda belirtilmiştir:

- Ticari sözleşmeleri kullanıyorsanız ve fiyatları değiştirirseniz, eski ticari sözleşmeleri bir bitiş tarihi ayarlayarak sonlandırmanız gerekir. Zaman içinde bu yaklaşım kanal veritabanlarında tutulan ticari sözleşmelerin azaltılmasına yardımcı olur. Aynı zamanda fiyat hesaplama algoritmasının üzerinde çalışması gereken veri miktarını azaltmaya yardımcı olur.
- Fiyatlarınız ürün çeşidine göre değişiyorsa, ürün temel fiyatını en sık kullanılan ürün çeşidinin fiyatı olarak kullanmayı düşünün. Sonra da ticari sözleşmeleri yalnızca özel durumlar olan ürün çeşidi fiyatları için kullanın. Bu yaklaşım ticari sözleşme kayıt sayısını düşürmenize yardımcı olur. Microsoft Dynamics 365'e veri aktarmak kolay olduğundan, her ürünün her çeşidi için bir ticaret sözleşmeyi içe aktarmak isteyebilirsiniz. Ancak, bu yaklaşım aynı değere sahip birçok ticari sözleşme oluşturabilir. Bu nedenle, verilerinizin boyutunu gereksiz düzeyde artırabilir.
- Commerce ürün çeşidine özel fiyatları en özel olandan en az özel alana doğru bir sırayla işler. Bir ürün boyutu fiyatı etkilemezse, bunun için ticari sözleşme tanımlamanıza gerek yoktur. Örneğin, bir ürün üç renk ve dört faklı bedende vardır ancak fiyat sadece bedene göre değişir. Her ürün çeşidi için bir ticari sözleşme tanımlarsanız, 12 kayıt oluşturursunuz. Bunun yerine, yalnızca her beden için bir ticari sözleşme belirleyip Renk boyutunu boş bırakabilirsiniz. Bu durumda, yalnızca dört kayıt oluşturursunuz.

    Alternatif olarak, boyutun her bir değeri farklı bir fiyat oluşturmazsa, ana ürün için bir ticari sözleşme oluşturup tüm ürün boyutlarını boş bırakabilirsiniz. Daha sonra farklı bir fiyat oluşturan her boyut değeri için ayrı bir ticari sözleşme tanımlarsınız. Örneğin, XXL bedeninin fiyatı daha yüksekse ancak diğer tüm bedenlerin fiyatı aynıysa, yalnızca iki ticari sözleşme gerekir: bir adet ana ürün için ve bir adet XXL bedeni için.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Veri dahil fiyatlar ile vergi hariç fiyatlar karşılaştırması

Dynamics 365'te satış fiyatlarını ayarlarken, ayarladığınız fiyat değerinin vergi dahil mi hariç mi olduğunu belirtmezsiniz. Değer sadece fiyattır. Bununla birlikte, perakende kanallarındaki **Vergi dahil fiyatlar** ayarı kanallarını vergiyi fiyata dahil edecek veya hariç tutacak şekilde yapılandırmanıza olanak tanır. Bu ayar kanalda ayarlanır ve tek bir şirket içinde bile değişebilir.

Hem vergi dahil hem de vergi hariç türleriyle çalışıyorsanız, fiyatları düzgün şekilde ayarlamanız çok önemlidir çünkü kanaldaki **Satış vergisi dahil fiyat** değiştirilirse müşterinin ödeyeceği toplam fiyat değişecektir.

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Perakende satış fiyatı ve perakende olmayan satış fiyatı arasındaki farklar

Tüm kanallarda fiyatlarını hesaplamak için tek bir fiyatlandırma altyapısı kullanılır: Çağrı merkezi, Perakende mağazalar ve Çevrimiçi mağazalar. Bu, birleşik ticaret senaryolarının etkinleştirilmesine yardımcı olur.

Perakende fiyatlandırması perakende dışı varlıklar yerine perakende varlıklarla çalışmak üzere tasarlanmıştır. Özellikle, fiyatları ambara göre değil mağazaya göre ayarlamak üzere tasarlanmıştır.

Perakende fiyatlandırma altyapısı şu fiyatlandırma özelliklerini **desteklemez**:

- Tesis veya tesis ile ambar depolama boyutlarının fiyatlarını ayarlama desteklenmez. Ticari sözleşmeler üzerinde yalnızca tesis boyutunu belirtirseniz, perakende fiyatlandırması tesisi dikkate almaz ve tüm sitelere ticari anlaşmayı uygular. Hem tesisi, hem de ambarı belirtirseniz, satıcıların her mağaza/ambar için fiyatları kontrol etmek üzere mağaza fiyat gruplarını kullanması beklendiğinden, tanımsız/sınanmadı.
- Öznitelik temelli fiyatlandırma desteklenmiyor.
- Satıcı iskontosu geçişi desteklenmiyor.

Ayrıca, **yalnızca** perakende fiyatlandırma altyapısı şu fiyatlandırma özelliklerini destekler:

- Fiyat, ana ürün fiyatına doğru en belirgin ürün çeşidi fiyatından en az belirgin ürün çeşidi fiyatına giden sırayla, ürün boyutlarını temel alır. İki ürün boyutu (örneğin, renk ve boyut) kullanılarak ayarlanan fiyat yalnızca bir ürün boyutu (örneğin boyut) kullanılarak ayarlanan fiyattan önce kullanılır.
- Aynı fiyat grubu, fiyat ve iskontoları denetlemek için kullanılabilir.

## <a name="pricing-api-enhancements"></a>Fiyatlandırma API geliştirmeleri

Fiyat, birçok müşterinin satın alma kararlarını kontrol eden en önemli etkilerinden biridir ve birçok müşteri satın almadan önce çeşitli sitelerdeki fiyatları karşılaştırır. Perakendeciler, rekabetçi fiyatları sağlamalarının sağlanmasına yardımcı olmak için, rakiplerini gözlemler ve genellikle promosyonlar yapar. Bu perakendecilere müşteriler çekmenize yardımcı olmak amacıyla ürün aramasının, Gözat özelliğinin, listelerin ve Ürün Ayrıntıları sayfasının en doğru fiyatları göstermesi çok önemlidir.

Commerce satış sürümünde, **GetActivePrices** uygulama programlama arabirimi (API), basit iskontolar (örneğin, sepetteki diğer maddelere bağımlı olmayan tek satırlı iskontolar) içeren fiyatları döndürür. Bu şekilde, gösterilen fiyatlar müşterilerin maddeler için ödeyeceği gerçek tutara yakın bir yöntemdir. Bu API, tüm basit iskonto türlerini içerir: bağlantı tabanlı, bağlılık programı tabanlı, katalog tabanlı ve kanal tabanlı indirimler. Ek olarak, satıcılar, uygulanan indirimlerle ilgili adları ve geçerlilik bilgilerini döndürür ve böylece perakendeciler fiyat için daha ayrıntılı bir açıklama sağlayabilir ve iskontonun geçerliliği yakında sona erdiğinde acilinin bir fikir yaratmasını sağlar.
