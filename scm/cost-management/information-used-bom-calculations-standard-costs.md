---
title: "Standart maliyetlere sahip ürün reçetesi hesaplamaları."
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a81bb51eef089152915d19170736a06d527191da
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="bom-calculations-with-standard-costs"></a>Standart maliyetlere sahip ürün reçetesi hesaplamaları.

[!include[banner](../includes/banner.md)]




Standart maliyet ürün reçetesi hesaplamasında kullanılan satın alınan madde bilgileri aşağıdakileri içerir:
-   Maliyet − Satınalınan bir maddenin maliyetleri, standart maliyetlere ilişkin maliyet versiyonunda tesise özel maliyet kayıtları olarak tutulur. Her maliyet kaydının etkin olduğu bir tarih vardır ve ürün reçetesi hesaplama tarihi hangi maliyet kaydının kullanılacağını belirler. Örneğin gelecekteki bir hesaplama tarihine sahip bir ürün reçetesi hesaplaması, bekleme durumunda ve gelecekte etkin olacak bir tarihe sahip bir maliyet kaydı kullanabilir.
-   Maliyet grubu − Satın alınan bir maddeye atanan maliyet grubu, üretilmiş bir maddenin hesaplanan maliyetlerindeki maliyet segmentasyonu için temel sağlar.
-   Madde ürün reçetesi hesaplama grubunda gömülü uyarı koşulları olası sorunları belirlemek ürün reçetesi hesaplaması etkinleştirin. Satın alınan ürünün maliyeti sıfır olduğunda, bir ürün reçetesinde sıfır maliyet veya tarihi geçmiş bir maliyet kaydı olduğunda bu gerçekleşebilir. Uygulanabilir uyarı koşulları, ürün reçetesi hesaplamasını başlatırken geçersiz kılınabilir.

Standart maliyet ürün reçetesi hesaplamasında kullanılan üretilmiş madde bilgileri aşağıdakileri içerir:
-   Stok için standart sipariş miktarı − Maddenin standart sipariş miktarı (stok için) bir ürün reçetesi hesaplamasındaki sabit maliyetleri itfa etmek için varsayılan muhasebe lot boyutu olarak işlev görür. Muhasebe lot boyutu ayrıca belirtilmişse sipariş miktarı çarpanını yansıtır.
-   Madde ürün reçetesi hesaplama grubunda gömülü uyarı koşulları olası sorunları belirlemek ürün reçetesi hesaplaması etkinleştirin. Üretilen üründe bir ürün reçetesi veya rota olmaması buna bir örnek olabilir. Uygulanabilir uyarı koşulları, ürün reçetesi hesaplamasını başlatırken geçersiz kılınabilir.

Standart maliyet ürün reçetesi hesaplamasında kullanılan ürün reçetesi bilgileri aşağıdakileri içerir:
-   Ürün reçetesi versiyonu − Üretilen maddeye atanan ürün reçetesi versiyonu etkin başlangıç ve bitiş tarihlerine ve onaylandı veya etkin durumuna sahiptir. Ürün reçetesi versiyonu şirket çapında veya tesise özel olabilir ve isteğe bağlı olarak miktar kırılma noktalarını yansıtabilir.
-   Ürün reçetesi satırı madde miktarı − Bir bileşenin normalde gereken bir değişken miktarı vardır ancak bu sabit  olabilir. Bileşen miktarı genelde bir adet ana madde üretimi için ifade edilir ancak ondalık hassasiyet sorunlarını gidermek için 100 veya 1000'lik miktarlar için de ifade edilebilir. Bileşen miktarı ölçümler temel alınarak da hesaplanabilir.
-   Ürün reçetesi satırı madde hurdası − Bir bileşen, planlanan hurda için değişken veya sabit bir miktara sahip olabilir.
-   Ürün reçetesi satırları madde geçerlilik tarihleri − Bir bileşenin geçerli başlangıç ve bitiş tarihleri olabilir.
-   Üretimin ürün reçetesi satırı madde türü − Sabit maliyetlerin itfasına ilişkin maliyetlendirme lot boyutu ürün reçetesi hesaplama miktarını ve bir sipariş açılım modunu yansıtır çünkü ürün reçetesi hesaplaması üretilen bileşenin tam miktarda (standart sipariş miktarı yerine) üretileceğini varsayar.
-   Üretilen bir bileşenin alt ürün reçetesi − Üretilen bir bileşen isteğe bağlı olarak, ürün reçetesi hesaplamasında maddenin geçerli etkin ürün reçetesi versiyonunun yerine kullanılacak belirtilmiş bir BOM versiyonuna sahip olabilir.
-   Üretilen bir bileşenin alt rotası − Üretilen bir bileşen isteğe bağlı olarak, ürün reçetesi hesaplamasında maddenin geçerli etkin rota versiyonunun yerine kullanılacak belirtilmiş bir rota versiyonuna sahip olabilir.
-   Operasyon numarası ve operasyon hurda yüzdelerinin etkisi − Operasyon numarası bir bileşeni belirli bir operasyona bağlar ve operasyonların bir hurda yüzdesi olabilir. Bu bağlantı, ürün reçetesi hesaplamalarının bileşenin gereken miktarına hurda yüzdelerini ve kümülatif hurda yüzdelerini (birden çok operasyondaki) dahil etmesini sağlar.
-   Maliyet hesaplamalarında ürün reçetesi madde satırını yoksay − Ürün reçetesi hesaplamalarında bir bileşen yok sayılabilir.

Standart maliyet ürün reçetesi hesaplamasında kullanılan operasyon kaynağı bilgileri aşağıdakileri içerir:
-   Saatlik maliyetler − Bir operasyon kaynağıyla ilişkili saatlik maliyetler kurulum süresine ve çalıştırma süresine atanan maliyet kategorileri cinsinden ifade edilir. Bu maliyet kategorileri kaynak grupları ve operasyon kaynakları için tanımlanmalıdır. Bir maliyet kategorisiyle ilişkili saatlik ücretler tesise özel veya şirket çapında olabilir.
-   Birim başına maliyetler − Bazı üretim ortamları operasyon kaynağı maliyetlerini, miktar için farklı bir maliyet kategorisi olarak ifade edilecek çıktı birimi başına atar. Örneğin, miktarla ilgili maliyetler işçilik için parça ücretlerini yansıtabilir veya bir boya üreticisi çıkan her bir galon başına operasyon kaynağı maliyetlerinin atamasını yapabilir.
-   Rota operasyonlarında operasyon kaynağı bilgilerinin üzerine yazma − Maliyet verilerine ilişkin operasyon bilgileri operasyonlar tarafından devralınır ve burada üzerilerine yazılabilir. Ürün reçetesi hesaplaması, rota hesaplamalarında belirtilen maliyet kategorisi bilgilerini kullanacaktır.
-   Maliyet kategorisi için maliyet grubu − Bir maliyet kategorisine atanmış bir maliyet grubu üretilen bir maddenin hesaplanmış maliyetlerinde maliyet bölümlendirmesi sağlar. Örneğin makineler ve işçilikle veya kurulum ve çalıştırma zamanıyla ilişkili hesaplanan maliyetleri bölümlendirmek için farklı maliyet grupları kullanılabilir.

Standart maliyet ürün reçetesi hesaplamasında kullanılan rota bilgileri aşağıdakileri içerir:
-   Rota versiyonu - Üretilen maddeye atanan rota versiyonu etkin başlangıç ve bitiş tarihlerine ve onaylandı veya etkin durumuna sahiptir. Rota versiyonu tesise özel olmalıdır ve isteğe bağlı olarak miktar kırılma noktalarını yansıtabilir.
-   Rota operasyon süresi − Süre, çalışma zamanı ve hazırlık süresi için belirtilebilir. Saatlik süre genelde bir adet ana madde üretimi için ifade edilir ancak ondalık hassasiyet sorunlarını gidermek için 100 veya 1000'lik miktarlar için de ifade edilebilir.
-   İkincil kaynaklar için rota operasyonu süresi − İkincil kaynak, birincil kaynakla aynı operasyon numarasına ve aynı rota operasyon süresine sahiptir. Örneğin bir operasyon için bir makine birincil kaynak ve işçilik ve araçlar ikincil kaynaklar olarak gerekebilir.
-   Rota operasyonu hurda süresi − Ürün reçetesi hesaplamaları, birden çok operasyondaki hurda yüzdelerini ve kümülatif hurda yüzdelerini hesaba alır. Bu, rota operasyonlarına gereken süre ve operasyon numaralarıyla bağlantılı bileşenlere gereken miktar için geçerlidir.
-   Rota operasyonu için maliyet kategorisi − Maliyet kategorilerine ilişkin operasyon kaynağı bilgileri operasyonlar tarafından devralınır ve burada üzerlerine yazılabilir. Ürün reçetesi hesaplaması, rota hesaplamalarında belirtilen maliyet kategorisi bilgilerini kullanacaktır.

Standart maliyet ürün reçetesi hesaplamasında kullanılan üretim genel gider bilgileri aşağıdakileri içerir:
-   Ek talep − Ek talep hesaplama formülü, örneğin işçilik gibi belirli bir maliyet grubuna bağlanmış bir değer yüzdesini (örneğin yüzde 100) yansıtır.
-   Ücret − Ücret hesaplama formülü, örneğin işçilik gibi belirli bir maliyet grubuna bağlanmış birim başına tutarı (örneğin saat başına 10,00 Dolar) yansıtır.
-   Süre tabanlı ve malzeme tabanlı genel giderler − Üretim genel giderleri rota operasyonlarına veya malzeme bileşenlerine bağlanabilir.

Standart maliyet ürün reçetesi hesaplamasında kullanılan maliyetlendirme bilgileri aşağıdakileri içerir:
-   Maliyetlendirme tipi − Maliyet versiyonu standart maliyetleri içermelidir. Standart maliyetleri kullanan ürün reçetesi hesaplamalarına birkaç kısıtlama uygulanır. Örneğin bu kısıtlamalar sair giderlerin birim maliyetlere dahil edilmesi gerektiğini ve ürün reçetesi hesaplama açılımının tek düzeyli olması gerektiğini belirtebilir.
-   Zorunlu geri dönüş ilkesi − Maliyet versiyonu, örneğin belirli bir maliyet versiyonunun veya etkin kayıtların kullanılması gibi bir geri dönüş ilkesinin kullanılmasını zorunlu kılabilir. Zorunlu geri dönüş ilkesi genelde, maliyet güncelleştirmeleri için iki versiyonlu yaklaşımdaki artımlı güncelleştirmeleri temsil eden bir maliyet versiyonuna uygulanır.
-   Beklemedeki maliyetler için bloke etme bayrağı − Bloke etme bayrağı, üretilen maddelere ilişkin beklemedeki maliyetlerin ürün hesaplamalarını engelleyebilir.
-   Belirtilen başlangıç tarihi − Belirtilen başlangıç tarihi, maliyet versiyonuyla ilişkili tüm ürün reçetesi hesaplamaları için varsayılan hesaplama tarihi olarak işlev görür.
-   Belirtilen tesis − Belirtilen tesis ürün reçetesi hesaplamalarını tek bir tesisle sınırlar.
-   Maliyet versiyonunun içeriği maliyetleri içermelidir − İçerik maliyetleri içermelidir. Üretilen maddeler için önerilen satış fiyatlarını hesaplamak üzere, isteğe bağlı olarak satış fiyatlarını içerebilir.

Bir ürün reçetesi hesaplamasını başlatırken birkaç bilgi kaynağı belirtilebilir. Bu kaynaklara tesis, hesaplama tarihi ve maliyet versiyonu dahildir.






