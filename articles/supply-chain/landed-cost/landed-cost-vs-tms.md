---
title: Varış yeri maliyeti ve Taşıma yönetimi karşılaştırması
description: Microsoft Dynamics 365 Supply Chain Management, taşıma ile çalışmak için Taşıma yönetimi (TMS) ve Varış yeri maliyeti olmak üzere iki farklı modül sağlar. Bu konu, iki modülün ortak işlevselliğini özetler ve aralarındaki farkları vurgular.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ba745048d1d9f28300f03ed0bc98142d80aa5a26
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569829"
---
# <a name="landed-cost-vs-transportation-management"></a>Varış yeri maliyeti ve Taşıma yönetimi karşılaştırması

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management, taşıma ile çalışmak için iki farklı modül sağlar: **Taşıma yönetimi** (TMS) ve **Varış yeri maliyeti**. Bu konu, iki modülün ortak işlevselliğini özetler ve aralarındaki farkları vurgular. Hangi modülün iş uygulamalarınıza en uygun olduğuna karar vermek için bu bilgileri kullanabilirsiniz. Bazı iş uygulamalarının TMS ile daha iyi çalıştığını, diğerlerinin ise Varış yeri maliyetiyle en iyi şekilde çalıştığını görebilirsiniz. Ardından, iş gereksinimlerinize bağlı olarak yalnızca bir modül kullanmayı seçebilir veya iki modülü birleştirebilirsiniz.

Bu konu, her iki modülün tüm özelliklerinin kapsamlı bir incelemesi değildir. Bunun yerine, malların satıcıdan tüketilebileceği yer olan işletmenizin ambarına taşınmasıyla ilgili olarak kullanılabilir işlevselliği vurgular.

## <a name="terminology-reference-data-and-reporting-differences"></a>Terminoloji, referans veriler ve raporlama farklılıkları

### <a name="terminology-comparison"></a>Terminoloji karşılaştırması

TMS ve Varış yeri maliyeti benzer kavramlar için farklı terimler kullanır. Aşağıdaki tabloda bu terimler ve bunların iki modüldeki kullanımı özetlenmiştir.

| TMS terimi | Varış yeri maliyeti terimi | Notlar |
|----------|------------------|-------|
| **Yükle**<p>*Yük*, aynı taşıma biriminde (kamyon veya gemi gibi) aynı anda taşınan sevkiyatların bir koleksiyonudur. Yükler gelen veya giden olabilir.</p> | **Seyahat**<p>Tipik olarak, bir *seyahat* tek bir *yolculuk* boyunca seyahat eden tek bir araçtır. Bir seyahat birden fazla *sevkiyat konteyneri* içerebilir ve kuruluşunuzun farklı tüzel kişiliklerinden gelen siparişleri de içerebilir. Seyahatler sadece gelen olabilir.</p> | TMS ayrıca, tanımlayıcı girebileceğiniz bir bilgi alanını ifade eden *seyahat numarası* terimini de kullanır. Ancak hiçbir işlevsellik TMS alanıyla ilişkili değildir ve Varış yeri maliyetindeki *seyahat* konseptiyle ilgisi yoktur. |
| **Rota**<p>*Rota*, kaynaktan hedefe taşımanın fiziksel yoludur.</p> | **Yolculuk**<p>*Yolculuk* kaynaktan hedefe bir taşımanın fiziksel yoludur. Her seyahat bir yolculuğa atanmalıdır.</p> | |
| **Rota segmentleri**<p>Bir rota, her biri yolculuğun bir adımını temsil eden birden çok *rota parçasına* sahip olabilir. Bir rota, her biri bir rota segmenti olarak kabul edilen birden fazla taşıyıcı veya hizmet içerebilir.</p> | **Duraklar**<p>Her yolculuğun birden fazla *durağı* olabilir ve her biri yolculuğun bir adımını temsil eder. Bir durak; taşıma, görev işleme veya başka bir faaliyetin bir parçası olabilir.</p> | |
| **Konteynerler**<p>Bir *konteyner,* TMS tarafından kullanılan her türlü paket veya ambalaj olabilir.</p> | **Sevkiyat konteynerleri**<p>*Sevkiyat konteyneri*, konteyner gemilerinden bilindiği gibi gerçek, fiziksel bir sevkiyat konteyneridir.</p> | |
| **Emtia kodları**<p>TMS'de (ve Supply Chain Management'taki diğer yerlerde), *emtia kodları* emtia türlerini tanımlar. Tarifeleri, tehlikeli maddelerin işlenmesini vb. etkileyebilirler.</p> | **Emtia kodları**<p>Varış yeri maliyetinde, *emtia kodları* tüzel kişilik düzeyinde belirlenir. Çoğunlukla raporlama için kullanılırlar.</p> | Varış yeri maliyeti, TMS ve Supply Chain Management'taki diğer yerler için kullanılan emtia kodlarını da kullanabilir. Ancak, Varış yeri maliyeti emtia kodları yalnızca Varış yeri maliyeti tarafından kullanılır. |

### <a name="some-reference-data-isnt-shared"></a>Paylaşılmayan bazı referans verileri

TMS ve Varış yeri maliyeti; maliyet kurulumu, yolculuklar ve duraklar gibi varlıklar için referans verilerini paylaşmaz. Her iki modülü de kullanırsanız paylaşılmayan referans verilerini yeniden oluşturmanız gerekir.

### <a name="intercompany-reports-dont-work-with-goods-in-transit"></a><a name="intercompany-reports"></a>Şirketlerarası raporlar transitteki mallarla çalışmaz

Aşağıdaki raporlar, Varış yeri maliyetinin sağladığı transitteki mallar özelliğiyle çalışmaz:

- [Şirketlerarası transitteki mallar toplamı raporu](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)
- [Şirketlerarası transitteki mallar toplamı raporu](/dynamicsax-2012/appuser-itpro/intercompany-goods-in-transit-totals-report-intercompanygoodsintransittotals)

Bu raporlar, bir satış sevk irsaliyesi düzenlediğiniz anda malların transite alındığını ve teslim alındıktan sonra transitten stoka alındığını varsayar. Ancak, transitteki mallar bu şekilde işlenmez. Bu nedenle, transitteki mallar ve şirketlerarası özelliklerini birlikte kullanırsanız bu raporların her ikisinin sonuçları da yanlış olacaktır.

## <a name="using-the-two-modules-together"></a>İki modülü birlikte kullanma

TMS'yi hem gelen hem de giden işlemleri için kullanabilirsiniz. Varış yeri maliyeti, gelen işlemler için TMS ile aynı temel işlevselliğin çoğunu sağlasa da, bazı işlevler de ekler. Bu nedenle, giden işlemler için TMS'yi ve gelen işlemler için Varış yeri maliyetini kullanmayı düşünebilirsiniz.

Genel olarak, gelen işlemler için her iki modülü birlikte kullanmanızı önermiyoruz. Gereksinimlerinizi en iyi karşılayan modülü kullanmalısınız. İki modülü birlikte kullanırsanız kaynak belgeleri aralarında paylaşmamalısınız. Örneğin, hem TMS'deki bir yük hem de Varış yeri maliyetindeki bir seyahat için aynı satın alma siparişini kullanmayın. Özellikle, sistemi otomatik olarak gelen yükler oluşturacak şekilde ayarlamadığınızdan emin olmalısınız. Satın alma siparişlerindeki maddeler bir seyahate dahil edilirse bunlar bir yükün parçası olarak işlenemez.

## <a name="goods-in-transit"></a>Transitteki mallar

Varış yeri maliyetinin birincil özelliklerinden biri, transitteki malları işleme özelliğidir. Transitteki malları işleme özelliği, sevk edilen maddelerin mali mülkiyetini hedef ambarda fiziksel olarak alınmadan önce almanızı sağlar. Transitteki malları işleme özelliği, genellikle uluslararası ticaret için gereklidir.

### <a name="tms-goods-in-transit-features"></a>TMS'de transitteki mallar özellikleri

TMS şu anda transitteki malları işleme özelliğini desteklememektedir.

### <a name="landed-cost-goods-in-transit-features"></a>Varış yeri maliyetinde transitteki mallar özellikleri

Transitteki malları işleme özelliği, Varış yeri maliyetinin birincil özelliğiklerinden biridir ve aşağıdaki işlevleri sağlar:

- **Transitteki mal ambarları**: Transitteki mal ambarları, Supply Chain Management'ta her ambarla ilişkilendirilebilir. Mallar, orijinal satın alma siparişi fatura edildikten sonra transitteki mal ambarlarına transfer edilir. Bu konumlarda fiziksel olarak rezerve edilen maddeler, fiziksel ambarlarda teslim alınana kadar tüketim için kullanılamaz hale gelir. Bu nedenle, satın alma siparişini faturalayarak malların mali mülkiyetini alabilirsiniz.
- **Transitteki mallar genel muhasebe hesabı**: Varış yeri maliyeti, transitteki malları işlemek için satın alma siparişi deftere nakil profiline belirli bir genel muhasebe deftere nakil hesabı ekler. Transitteki mallar genel muhasebe hesabı, "teslim alınmamış faturalanan mallar" türünde bir hesap görevi görür. Orijinal satın alma siparişi faturalandığında ve transitteki mallar siparişi oluşturulduğunda, doğrudan satın alma siparişi maliyeti, mallar son fiziksel konumlarında teslim alınana kadar transitteki mallar genel muhasebe hesabına nakledilir.
- **İzleme denetimi güncelleştirmeleri**: Transitteki mallar siparişleri, Varış yeri maliyetinde izleme denetimi işlevselliğini destekler. İzleme denetimi, malların sevkiyat halindeyken beklenen varış tarihini güncelleştirmenizi sağlar. İzleme denetimi daha sonra seyahati ve ilişkili satın alma siparişi satırlarını güncelleştirir. Beklenen teslimat tarihi daha sonra master planlama ve lojistik için kullanılabilir.
- **Fazla/eksik teslima hareketlerini tetikleme**: Bir seyahat satırındaki beklenen mallar ile ambarda teslim alınan gerçek mallar arasında bir fark oluşursa Varış yeri maliyeti, fazla ve/veya eksik teslimat hareketleri oluşturarak bunu çözer. Daha sonra, bu hareketleri bir satın alma siparişi veya taşıma günlüğü aracılığıyla işlemek istediğiniz şekilde yönetebilirsiniz. Fazla ve eksik teslimat hareketleri, seyahate, orijinal satın alma siparişine ve fark için yeni hareket günlüğüne veya satın alma siparişine bir bağlantı sağlar.
- **Transitteki mallar siparişleri**: Varış yeri maliyeti, *transitteki mallar siparişi* olarak bilinen yeni bir kaynak belge sunar. Transitteki mallar siparişi, maddelerin mali mülkiyetini almak için orijinal satın alma siparişini faturalamanızı sağlar. Satın alma siparişi faturalandığında, stok boyutları kombinasyonuna sahip her satın alma siparişi satırı için yeni kaynak belge oluşturulur. Mallar daha sonra fiziksel olarak bir transitteki mal ambarına taşınır ve burada transitteki mallar siparişiyle karşılaştırılarak fiziksel olarak rezerve edilir ve transitteki mallar siparişi alınmadığı sürece tüketilemez.

## <a name="miscellaneous-charges-and-shipment-costs"></a>Sair giderler ve sevkiyat maliyetleri

Mallar için sevkiyat ve sevkiyat yönetiminin en önemli yönlerinden biri, sevkiyatlarla ilişkili genel gider maliyetlerinin tanınmasıdır. Bu genel gider maliyetleri, bir satın alma siparişi ve sevkiyat ya da seyahatle ilişkili doğrudan stok maliyetleri değildir. Bunun yerine, malların satıcıdan kuruluşunuza hareketinin doğası gereği ortaya çıkan ek maliyetlerdir. Bu maliyetler, bir fiziksel konumdan diğerine mal sevkiyatıyla ilişkili navlun maliyetlerini veya yabancı bir satıcıdan mal ithalatıyla ilişkili vergi maliyetlerini içerebilir.

Varış yeri maliyeti, *otomatik maliyetler* olarak bilinen yeni bir maliyet yapısı türü oluşturarak bu maliyetleri işler. TMS, sair gider işlevselliğini kullanarak bu maliyetleri işler.

### <a name="tms-charge-and-cost-features"></a>TMS ücret ve maliyet özellikleri

TMS, ilgili kaynak belge satırlarına tahsis edilen yüklerin ek maliyetlerini yönetmek için sair giderleri kullanır. Bu sair giderler satın alma siparişi satırı veya satın alma siparişi başlığı düzeyinde ayarlanabilir.

TMS'de sair giderler stokun ağırlığına, hacmine veya miktarına göre eklenebilir veya bölünebilir. Ücretler navlun veya ilave ücretlere bölünebilir. TMS'de ek tahsis yöntemlerinin kullanılması için daha fazla geliştirme yapılması gerekecektir.

### <a name="landed-cost-charge-and-cost-features"></a>Varış yeri maliyeti ücret ve maliyet özellikleri

Varış yeri maliyeti, malların sevkiyatıyla ilişkili ek maliyetleri işleyen bir maliyet işlevleri kümesi sağlar. Bu maliyetler otomatik maliyetler olarak bilinir ve tahmini maliyet tutarı kullanılarak ilk sevkiyat faturalama anında uygulanır. Her maliyet türü kendi deftere naklinde yönetilir. Genel gider maliyetleri için gerçek faturalar deftere nakledildikten sonra, tahmini maliyetler fiili maliyetleri yansıtacak şekilde otomatik olarak güncelleştirilir.

Ayrıca, malların sevkiyatı ile ilişkili genel gider maliyetleri, çıkış limanından seyahat sırasında veya mallar teslim alındıktan sonra herhangi bir zamanda faturalandırılabilir. Bu özellik, malların tüketimi için daha fazla esneklik sağlar.

Aşağıdaki listede, Varış yeri maliyetindeki ücret ve maliyet özelliklerine ilişkin bazı kavramlar özetlenmiştir:

- **Maliyet alanı**: Maliyetler ve masraflar bir yolculukta farklı seviyelere veya *maliyet alanlarına* atanabilir. Maliyet seyahat seviyesinde uygulanabilir ve seyahatteki her öğeye bölünebilir. Ayrıca, maliyetler konteyner, satın alma siparişi, madde veya transfer emri düzeyinde uygulanabilir. Her maliyet gideri çeşitli alanlarda ayrı ayrı yönetilebilir ve madde başına maliyete bölünür.
- **Paylaştırma yöntemleri**: Varış yeri maliyetinde çeşitli tahsis yöntemleri mevcuttur. Maliyet giderleri miktara, dolar tutarına, değere, ağırlığa, hacme, ölçüme veya kullanıcı tanımlı hacimsel ölçüye göre eklenebilir.
- **Temizleme/fark denetimi**: Maliyet giderleri, Varış yeri maliyetinde kendi maliyet kodu türü olarak ayarlanır. Her maliyet kodu türü, tahmini maliyet giderleri için bir kliring hesabı ve ayrıca tahmini maliyetlerdeki farklar için tahakkuk ve satın alma fiyatı farkı hesapları tanımlamanıza olanak tanır. Tahmini maliyetler başlangıçta deftere nakledildiğinde, kliring hesabında bir alacak olur. Gerçek faturalar deftere nakledildikten sonra, fiili maliyet giderleri deftere nakledilir ve tahmini maliyetler kliring hesabından borçlandırılır.

## <a name="matching-freight-bills-and-invoices"></a>Navlun faturaları ile faturaları eşleştirme

### <a name="tms-bill-and-invoice-matching-features"></a>TMS faturası ve fatura eşleştirme özellikleri

TMS, tahmini maliyetler ve faturalar içeren navlun faturalarını navlun fiili maliyetiyle eşleştirebilir. Faturalar elektronik veya basılı olarak alınabilir. Tahmini maliyet ile fiili maliyet arasındaki farkın eşleşmesi stok değerlemesini etkilemez.

Daha fazla bilgi için bkz. [Taşımacılık yönetiminde mutabakat sağlama](../transportation/reconcile-freight-transportation-management.md).

### <a name="landed-cost-bill-and-invoice-matching-features"></a>Varış yeri maliyeti faturası ve fatura eşleştirme özellikleri

Varış yeri maliyeti, navlun faturalarını tahmini maliyet ücretleriyle eşleştirebilir ve gerçek maliyet giderlerini tahmini maliyetlerle faturalayabilir. Faturalama anında, navlun ücretleri bir fatura günlüğündedir ve tahmini maliyetler kliring hesabından temizlenir. Ayrıca, gerçek maliyet giderleri, tahmini masraflar ve gerçek masraflar arasındaki farklarla birlikte madde için satılan malların maliyetine göre deftere nakledilir. Bu davranış, faturalama işleminde esneklik sağlar.

## <a name="tracking"></a>İzleme

Hem TMS hem de Varış yeri maliyetinin önemli bir özelliği, malları izleme ve çıkış noktasından nihai hedef ambara yolculuğunun neresinde olduğunu belirleme özelliğidir. İzleme, malların nerede bulunduğunu ve tüketim için ambara ne zaman ulaşmasının beklendiğini takip etmenizi ve güncelleştirme yapmanızı sağlar. Yolculukları sırasında malların durumuna ek olarak Varış yeri maliyeti yolculuğun her adımı için beklenen ve gerçek tarihler sağlar.

### <a name="tms-tracking-features"></a>TMS izleme özellikleri

TMS, gelen yükleri izlemek için sınırlı özellikler sağlar. Tarihleri gösterir ve tam konumu bulmak için bir tümleştirmenin (örneğin, **Taşıma durumu** sayfasında) oluşturulmasını sağlar.

Her rota segmenti için tahmini zamanlamaları ve varış saatlerini girebilirsiniz.

### <a name="landed-cost-tracking-features"></a>Varış yeri maliyeti izleme özellikleri

Varış yeri maliyeti, çıkış limanından son varış noktasına kadar her seyahat için izleme denetimi sağlayabilir. İzleme denetimi seyahatin durumunu ayarlar. Durum, seyahatin seyir halinde mi, gümrükte mi yoksa nihai ambara teslimat için yerel teslimatta mı olduğunu gösterir. Durum, satın alma siparişi satırı, konteyner ve seyahat başlığı düzeyinde ayarlanabilir. Böylece, daha ayrıntılı denetime sahip olursunuz.

Ayrıca, belirtilen sağlama sürelerini temel alan onaylanmış bir beklenen tarih, bir yolculuğun her adımıyla ilişkilendirilir. Onaylanan ve beklenen teslimat tarihleri, satın alma siparişi satırına ve transitteki mal siparişlerine eklenir ve master planlama ile lojistik için kullanılabilir. Beklenen tarihlere ek olarak, gerçek tarihler de güncelleştirilebilir. Bir yolculuktaki sonraki adımlar buna göre güncelleştirilir.

## <a name="multi-leg-journeys"></a>Çok duraklı yolculuklar

Yolculuk kavramı, malların sürecin neresinde olduğunu belirler ve taşıma sırasında malların durumunu kontrol eder. Mallar bir yolculuğun birkaç durağından geçebilir ve çeşitli maliyetleri belirli bir durakla ilişkilendirebilirsiniz. Örnekler arasında bir aracın seyri ile ilgili navlun maliyeti ve malların limandan varış noktasına taşınmasındaki yerel sevkiyat maliyetleri sayılabilir.

### <a name="tms-multi-leg-journey-features"></a>TMS çok duraklı yolculuk özellikleri

TMS'de rotalar, çok duraklı yolculukları temsil etmek için rota segmentlerine ayrılabilir. TMS, spot oranları ve ilave ücretleri tek tek rota segmentlerine tahsis edebilir.

Daha fazla bilgi için bkz. [Çok duraklı navlun taşıma rotaları planlama](../transportation/plan-freight-transportation-routes-multiple-stops.md).

### <a name="landed-cost-multi-leg-journey-features"></a>Varış yeri maliyeti çok duraklı yolculuk özellikleri

Varış yeri maliyeti, malların bir yolculuktaki duraklar veya adımlar olan bir dizi durak aracılığıyla varış noktasından hedefe taşınması için bir çerçeve sağlar. Duraklar, malların satıcıdan kuruluşunuza nasıl taşınacağını tanımlayan yolculuk şablonları oluşturmak için birleştirilir.

Bir yolculuğun her durağında, her satın alma siparişi satırının durumunu ve onunla ilişkili sağlama sürelerini daha ayrıntılı tanımlayabilirsiniz. Tüm duraklar için birleşik teslim süresi, tahmini teslimat tarihini tanımlamak için kullanılır. Ancak, çok duraklı yolculukların uygulanabileceği transitteki mal işlemesi gerekir. Bir yolculukta malların yolculuğu, Varış yeri maliyetine özgü bir tabloda yönetilir.

## <a name="receiving-by-container"></a>Konteynere göre teslim alma

Malların bir gemide nasıl bölünüp depolandığını yönetmek önemli olabilir. Bir araçta, mallar bir veya birden fazla konteynerde tutulabilir. Mallar teslim alındığında, konteynerlerde alınır ve bir seyahatteki farklı konteynerler farklı zamanlarda veya farklı tarihlerde alınabilir.

Hem TMS hem de Varış yeri maliyeti, bir konteynerdeki malların teslim alımını yönetme işlevi sağlar. TMS, bir sevkiyat konteyneriyle ilişkili malları, satın alma siparişlerini ve transfer emirlerini yönetmek için yük kavramını kullanır. TMS, önceden sevkiyat bildirimi (ASN) yoluyla teslim alınan bir ambalaj yapısı temelinde teslim almayı destekler. Varış yeri maliyeti, satın alma siparişlerini işlemek ve bir gemideki bir konteynerle ilişkili genel gider maliyetlerini kontrol etmek için sevkiyat konteynerleri kavramını kullanır.

### <a name="tms-receiving-by-container-features"></a>Konteyner özelliklerine göre TMS teslim alma

TMS, gelen ASN'leri, Ambar Yönetimi mobil uygulaması üzerinden teslim almanın tüm çeşitlerini ve Supply Chain Management istemcisi aracılığıyla teslim almanın tüm yöntemlerini destekler.

### <a name="landed-cost-receiving-by-container-features"></a>Konteyner özelliklerine göre varış yeri maliyeti alma

Konteynere göre teslim almayı desteklemek için Varış yeri maliyeti sevkiyat konteyneri kayıtları oluşturur ve satın alma siparişlerini konteyner kimliği kullanılarak belirli bir sevkiyat konteyneriyle ilişkilendirir. Ek yük maliyetleri daha sonra bu sevkiyat konteynerine uygulanabilir ve ilgili satın alma siparişleriyle ilişkilendirilecek şekilde bölünebilir.

Varış yeri maliyetindeki konteynerler, *transitteki mallar girişi* olarak bilinen yeni bir giriş türü üzerinden, varış günlükleriyle veya mobil cihaz teslim alma yoluyla teslim alınabilir. Varış günlükleri kullanıldığında, miktarlar transitteki mal siparişinden veya konteynerdeki orijinal satın alma siparişi satırlarından başlatılabilir. Varış yeri maliyeti, Ambar Yönetimi mobil uygulaması üzerinden alınacak iki iş türü sağlar.

Varış yeri maliyeti, malların elektronik olarak alınması için bir ASN sağlamaz. Ayrıca, yük teslim alma, plaka alma veya karışık plaka alma işlemlerini işleyen Ambar Yönetimi mobil uygulaması akışlarını desteklemez.

## <a name="rate-shopping-by-vendor"></a>Satıcıya göre alışveriş derecelendirme

Oran değişimi, bir şirketin en düşük fiyata, en hızlı rotaya veya her iki hususun kombinasyonuna göre bir sevkiyat satıcısı seçmesini sağlar.

### <a name="tms-rate-shopping-features"></a>TMS alışveriş derecelendirme özellikleri

TMS, gelen ve giden siparişler için satıcı ve üretim akışı çözümlerini tanımlamanıza olanak tanır. Örneğin bir sevkiyat için en hızlı yolu veya en ucuz oranı tanımlayabilirsiniz.

TMS, fiyat rotası çalışma düzeni üzerinden tam fiyat derecelendirme ve navlun optimizasyonu, derecelendirme altyapısı üzerinden esnek derecelendirme seçenekleri, harici taraflarla tümleştirme için bir derecelendirme altyapısı API'si ve hacimsel ağırlık desteği sağlar.

Daha fazla bilgi için bkz. [Taşıma yönetimi altyapıları](../transportation/transportation-management-engines.md).

### <a name="landed-cost-rate-shopping-features"></a>Varış yeri maliyeti alışveriş oranı özellikleri

Varış yeri maliyeti, satıcıya göre alışveriş oranı için yalnızca sınırlı destek sağlar. Navlun iletici değerlerini girebilmenize rağmen, Varış yeri maliyeti bunları birden çok satıcı arasında karşılaştırmaz.

## <a name="driver-check-incheck-out-with-appointment-scheduling"></a>Randevu zamanlaması ile sürücü giriş/çıkışı

Sürücü giriş/çıkış özellikleri, sistemin varışları izlemesini ve yükleme noktalarındaki tıkanıklığı önlemesini sağlar.

### <a name="tms-driver-check-incheck-out-features"></a>TMS sürücü giriş/çıkış özellikleri

TMS, *randevu* oluşturmanıza olanak tanır. Randevu, bir satın alma siparişi almak, satış siparişini sevk etmek veya belirli bir tarihte ve belirli bir zamanda gelen veya giden yükü işlemek için bir yükleme/boşaltma noktasında meydana gelen olayları temsil eder. Randevular, yükleme/boşaltma noktalarının malları yüklemek ve boşaltmak için kullanılabilir olmasını sağlar ve birden fazla taşıyıcının aynı anda bir konuma ulaştığı durumları önlemeye yardımcı olur.

Sistem, sürücülerin belirli bir yükleme/boşaltma noktasında giriş yapmasına izin vermeyi destekler.

### <a name="landed-cost-driver-check-incheck-out-features"></a>Varış yeri maliyeti sürücü giriş/çıkış özellikleri

Varış yeri maliyeti, bir konteynerin teslim edileceğinin tarih ve saatiyle ilgili tahminleri depolayabilir.

## <a name="transfer-orders-and-additional-costs"></a>Transfer emirleri ve ek maliyetler

Genellikle, işletmeler ambarlar arasında mal transfer edebilmelidir. Bu tür bir transfer gerçekleştiğinde, maliyetler bununla ilişkilendirilir ve bu maliyetleri tanımak isteyebilirsiniz. Varış yeri maliyetinde, malların bir ambardan veya tesisten diğerine hareketini izlemek, teslimat süresini ve beklenen teslimat tarihini tahmin etmek ve malların transferine genel gider maliyetleri eklemek için bir seyahate veya gemiye transfer emirleri eklenebilir.

### <a name="tms-transfer-order-cost-features"></a>TMS transfer emri maliyet özellikleri

TMS, transferlere bağlı navlun ücretlerinin oluşturulmasını destekler. Bu ücretler transfer emrinden görüntülenebilse de, alınan maliyet madde maliyetine eklenmez. Navlun mutabakatı, bu masraflara dayalı bir navlun faturası oluşturularak desteklenir. Bu navlun faturası daha sonra bir satıcı navlun faturasıyla eşleştirilir.

### <a name="landed-cost-transfer-order-cost-features"></a>Varış yeri maliyeti transfer emri maliyet özellikleri

Varış yeri maliyeti, bir gemiye veya seyahate transfer emirleri eklemenizi sağlar. Bu şekilde, transfer emrinin alındığı anda stok kapatmaları olarak seyahate sevkiyat maliyetleri ekleyebilirsiniz. Genel gider maliyetleri gerçek maliyetler için faturalandırılabilir ve satılan malların maliyetini güncelleştirmek için bir seyahatle karşılaştırılarak izlenebilir. Transfer emirleri standart sürümde transitteki mal işlemesinde kullanmasa da, seyahatlere eklenebilir. Varış yeri maliyeti, her maddenin toplam maliyetine eklenir.