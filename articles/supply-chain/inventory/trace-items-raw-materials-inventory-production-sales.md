---
title: Stok, üretim ve satıştaki maddeleri ve hammaddeleri izleme
description: Bu konuda, madde izlemesini kullanarak maddelerin veya hammaddelerin üretim ve satış süreçlerinde nerede kullanılmış, kullanılmakta veya kullanılacak olduklarını belirleyebilirsiniz.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f45c39769b71832afe531db8a55097ede8a3c769
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "310082"
---
# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Stok, üretim ve satıştaki maddeleri ve hammaddeleri izleme

[!include [banner](../includes/banner.md)]

Bu konuda, madde izlemesini kullanarak maddelerin veya hammaddelerin üretim ve satış süreçlerinde nerede kullanılmış, kullanılmakta veya kullanılacak olduklarını belirleyebilirsiniz.

Madde izleme işlevi **Madde izleme** sayfasında bulunur. Madde izlemeyi nasıl kullanabileceğiniz ve seçenekler ve sınırlamaların neler olduğu aşağıdaki bölümlerde açıklanmıştır.

## <a name="what-is-item-tracing"></a>Madde İzleme nedir?
Madde izleme, tedarik zincirindeki madde ve hammaddelerin kaynak ve hedefine görünürlük sağlayan bir işletme akıllı (BI) aracıdır. Üreticiler maddeleri, hammaddeleri veya içerikleri satıcıya kadar izleyebilir ve bitmiş ürünün üretiminden satışına kadar ilerleyebilirler. Madde izleme, üreticilerin mevzuat gerekliliklerine uymasına yardımcı olur ve ayrıca kalite görevlileri ile üretim müdürlerinin ürün ve malzemelerin kalitesindeki farkları analiz edip gerekli önlemleri almasına da yardım eder. Burada, üreticilerin madde izlemeyi nasıl kullanabileceklerine dahil çeşitli örnekler verilmiştir:

-   Stokta bulunan bir maddenin veya hammaddenin tutarını ve nerede depolandığını belirlemek.
-   Madde veya hammaddenin ne kadarının sevk edildiğini ve hangi müşterilere sevk edildiğini belirlemek.
-   Madde veya hammadde içeren planlı sevkıyatları belirlemek.
-   Madde veya hammadde kullanan ve planlı, sürmekte olan veya bitmiş olarak raporlanmış üretim emirlerini bulmak.
-   Madde veya hammaddenin nereden satın alındığını bulmak.
-   Bir madde veya hammaddenin başka bir maddenin üretiminde nerede tüketildiğini araştırmak.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Neyi izleyebilirim ve sınırlamalar var mı?
Madde ve hammaddelere yönelik geçmiş stok hareketlerini bir madde numarasına ve seri numarası, toplu iş numarası veya satıcı toplu iş numarası gibi bir izleme boyutuna dayalı olarak izleyebilirsiniz. Bir madde veya hammaddeyi yalnızca bir izleme boyutu atanmışsa izleyebilirsiniz. İzleme stok hareketlerine dayandığından, maddeleri izlerken bazı sınırlamalar vardır. Örneğin projelere, sabit kıymetlere ve perakendeye yönelik hareketlere ilişkin sınırlamalar vardır. Ayrıca, ortak ürünler izleme ayrıntılarında gösterilir, ancak yan ürünler dahil edilmez. İzleme bir konumdan diğerine tüm ambar hareketlerini içerir. Bu nedenle, kullanıcılar bilgi miktarını aşırı fazla bulabilir. İzleme aynı anda tek bir tüzel kişilik için görüntülenir. Şirketler arası bağlamda hiçbir şirketler arası kabiliyet yoktur. Bir madde alındığında veya gönderildiğinde her bir şirket için mutlaka yeni bir izleme başlatmanız gerekir.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Bir madde izlemesi için hangi kriterleri belirleyebilirim?
Bir madde izlemesi için gereken kriterler (madde numarası, toplu iş numarası veya seri numarası gibi) bir izleme boyutu ve yöndür. Aşağıdaki tabloda, madde izlemesi için kullanabileceğiniz kriterler açıklanmaktadır.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Alan grubu</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Madde kodu</td>
<td>İzlediğiniz madde veya hammadde için tanımlayıcı girin.</td>
</tr>
<tr class="even">
<td>Ürün boyutları</td>
<td>İsteğe bağlı: Yapılandırma, boyut, renk veya stil gibi ürün tanımlarının belirli yönlerini izleyin.</td>
</tr>
<tr class="odd">
<td>İzleme boyutları</td>
<td>Toplu iş numarası, satıcı toplu iş numarası veya seri numarası izleme boyutunu girin. Toplu iş numarasını kriter olarak kullandığınızda, bu bilgileri yakalamanız durumunda satıcı toplu iş numarası görüntülenir.</td>
</tr>
<tr class="even">
<td>Depolama boyutları</td>
<td>İsteğe bağlı: Belirli bir konumda saklanan maddeleri izleyin.</td>
</tr>
<tr class="odd">
<td>Dönem</td>
<td>İsteğe bağlı: izlemeyi belirli bir dönemle sınırlamak için tarihleri girin. İzleme ayrıntıları yalnızca bu tarihler arasında oluşturulmuş belgeleri ve hareketleri görüntüler.</td>
</tr>
<tr class="even">
<td>İleri veya geri</td>
<td>İzleme için yön seçin. İleriye veya geriye doğru izleyebilirsiniz:
<ul>
<li><strong>Geriye doğru</strong> – Kaynağı, elde kalan miktarı ve en azından kısmen bitmiş olarak raporlanan üretim emirlerini belirlemek için aşağı doğru izleyin.</li>
<li><strong>İleriye doğru</strong> – Hedefi belirlemek için yukarı doğru izleyin. Satış emirlerini ve izlenen maddenin veya hammaddenin en azından kısmen sevk edilmiş olduğu müşterileri bulabilirsiniz.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>İzleme ayrıntılarına hangi bilgiler dahildir?
İzlemenin sonuçları, **Madde izleme** sayfasındaki **Ayrıntılar** FastTab'inde ağaç yapısında kronolojik sırada görüntülenir. Sıra, izleme yönüne göre değişir. Ayrıntılar arasında, maddenin satıcıdan satın alınmasından müşteriye satılmasına kadar tüm hareketler vardır. İzleme sonuçları aynı zamanda madde ile ilişkili ara ürünleri veya izleme kriterlerinde belirtilmiş izleme boyutunu da içerir. Üst düğüm stok birimindeki maddenin miktarını, izleme kriterlerinde belirtilmiş depolama boyutlarına göre elde kalanı gösterir. **Not:** İzleme ayrıntıları, izleme yapıldığı sırada görülebilen bilgilerin anlık görüntüsüdür. İzleme ayrıntıları, bilgiler izleme yapıldıktan sonra değiştirilirse güncellenmez.

## <a name="why-dont-some-nodes-contain-any-details"></a>Bazı düğümler neden ayrıntı içermiyor?
İzleme ayrıntılarındaki bilgi miktarını azaltmak için, yalnızca ilk madde veya hammadde örneği için düğüm ayrıntı içerir. Seçili düğüm ayrıntı içermiyorsa, ayrıntı içeren düğümü **İzlenen satıra git** seçeneğine tıklayarak görüntüleyebilirsiniz. **Geri git** düğmesine tıklayarak ayrıldığınız düğüme geri dönebilirsiniz.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Yalnızca belirli bir belge türünü görüntüleyebilir miyim? Örneğin, yalnızca üretim emirlerini, müşterileri veya satıcıları görebilir miyim?
Evet, yalnızca belirli türde bir belge veya hareketten izleme ayrıntıları içeren liste sayfaları açabilirsiniz. Bu sayfalara Eylem Panosundaki **İzleme** menü öğesinden, **Madde**, **Satışlar**, **Satın Alma**, **Üretim** ve **Kalite** gruplarından erişebilirsiniz. Örneğin, izleme ayrıntılarında satıcıların listesini görüntülemek için sırasıyla **İzleme** &gt; **Satın Alma** &gt; **Satıcılar**'a tıklayın. Liste sayfaları, izleme ayrıntılarından belge veya hareketleri özetler. **Bekleyen hareketler**, **Bekleyen siparişler** ve **Sevk edilmemiş satış emirleri** liste sayfaları ayrıca, izleme ayrıntılarına dahil edilmeyen diğer bilgiler görüntülenir. Ek olarak, bir tarih aralığı belirlenmiş olsa dahi, geçerli tarihin sonuçlarını daima gösterirler. Aşağıdaki tabloda, bu sayfaların içerebileceği ek ayrıntılar açıklanmıştır.

| Listeler                    | Açıklama                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sevk edilmemiş satış siparişleri | Henüz çekilmemiş ve bu nedenle izleme ayrıntılarında gösterilmeyen satış emri satırlarını görüntüleyin.                                                                                                                                                                                                                        |
| Bekleyen siparişler           | İzleme kriterlerinde kullanılan izleme boyutlarından bağımsız şekilde, izlenen madde için bekleyen tüm emirleri görüntüleyin. Aynı zamanda izlenen maddenin içeriklerinden biri olduğu ve hiçbir kaydın yapılmadığı ve emir için hiçbir hareketin bitmiş olarak rapor edilmediği bekleyen üretim emirlerini de görüntüleyebilirsiniz. |
| Bekleyen hareketler     | Belirtilen izleme boyutlarını veya boş izleme boyutu içeren izlenen maddeye yönelik bekleyen stok hareketlerini görüntüleyin. İzleme ayrıntılarında, maddeler ve izleme boyutu kombinasyonları veya bir boş değer için bekleyen stok hareketlerini de görüntüleyebilirsiniz.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>BOM veya formülünde kaç düzey aşağı veya yukarı izleme yapabilirim?
Ürün reçetesi (BOM) veya formülünde bir düzey aşağı veya yukarı izleme yapabilirsiniz. Örneğin, hammaddeler üzerinde izleme çalıştırırsanız, bitmiş ürünü ve herhangi bir ortak ürünü görebilirsiniz. Ancak, bir ortak ürünü izliyorsanız, izleme ayrıntıları bitmiş ürünü içermez.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>İzleme ayrıntıları içinde bir belge veya hareket hakkında daha fazla ayrıntıyı nasıl görüntüleyebilirim?
**Ayrıntılar** FastTab'inde, izleme ayrıntılarındaki seçili belge veya hareket hakkında daha fazla bilgiyi iki şekilde görüntüleyebilirsiniz:

-   **Ayrıntılar** FastTab'indeki izleme ayrıntılarında bir düğüm seçtiğinizde, sayfadaki diğer FastTab'ler düğümdeki belge veya hareketler hakkında bilgiler görüntüler.
-   **Ayrıntıları göster** düğmesine tıklayarak, seçili bir düğümdeki belge için Ayrıntılar sayfasını açın. Örneğin, bir üretim emrini açıklayan bir düğüm seçerseniz ve **Ayrıntıları göster** düğmesine tıklarsanız, **Üretim emirleri ayrıntıları** sayfası görüntülenir.

Bazı FastTab'ler seçilen düğüme ilişkin ek bilgilere erişim sunar. Örneğin, **Uyumsuzluklar** FastTab'inde, **Sorgular** düğmesine tıklayarak bir uyumsuzluk geçmişi olup olmadığını araştırabilirsiniz. **Toplu iş** FastTab'inde, **Elde olan** düğmesine tıklayarak elde mevcut fiziksel stok tutarını ve toplu işle ilişkili tüm stok hareketlerini görüntüleyebilirsiniz.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Birden fazla izleme çalıştırıp sonra ayrıntıları karşılaştırabilir miyim?
İzlemeyi çalıştırdıktan sonra, **Düğümden izleme** düğmesindeki aşağıdaki seçenekleri kullanarak seçilen düğümdeki hareketlerde yeni bir izleme çalıştırabilirsiniz:

-   **Geri** veya **İleri** – Seçili düğüm için yeni bir izleme başlatın ve geçerli izlemenin ayrıntıları üzerine yazdırın.
-   **Yeni geri** veya **Yeni ileri** – Yeni bir pencerede yeni bir izleme başlatın ve geçerli izlemenin ayrıntılarını tutun.

**Yeni geriye doğru** veya **Yeni ileriye doğru** seçeneğini kullanmak istiyorsanız yeni bir izlemenin yeni bir pencerede görüntülenmesini sağlamak için **Yeni pencerede aç** işlevini kullanmanız gerekir.

## <a name="can-i-save-the-trace-details"></a>İzleme ayrıntılarını kaydedebilir miyim?
<strong>Ayrıntılar</strong> sekmesindeki bilgileri Eylem Bölmesinde *<strong><em>İzleme</em></strong>* eyleminin altındaki <strong>Dışa Aktar</strong> düğmesine tıklayarak bir XML dosyası olarak kaydedebilirsiniz. İzleme ayrıntılarına ek olarak XML dosyası; izleme kriterleri, ana düğüm ve eldeki miktar da dahil edilir. Örneğin, bilgileri bir kalite emrine veya diğer uyum belgelerine eklemek istiyorsanız izleme ayrıntılarını kaydetme özelliği faydalıdır. Dosyanın nereye kaydedildiği belirtebilirsiniz. Dosyayı hemen görüntülemek için <strong>Belgeyi göster</strong> öğesini seçin. <strong>Not:</strong> Sadece görüntülemek isteseniz dahi, dosya her zaman kaydedilir. Varsayılan olarak, XML dosyası bir tarayıcı penceresinde açılır. Ancak dosyaya sağ tıklayıp <strong>Birlikte aç</strong>'ı seçtikten sonra içerikleri görüntülemek için kullanılacak programı seçebilirsiniz.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Belirli bir madde veya içerik için bakiyeyi hesaplayabilir miyim?
Bilgileri özet sayfalarından Microsoft Excel'e aktarabilirsiniz. İlgili sayfada, **Microsoft Office'de aç** simgesine tıklayın ve ardından **Microsoft Excel'e Ver** öğesini seçin. Bu işlev, **Hareketler özeti** sayfasından bir madde veya içerik için toplu bakiye hesaplamak istediğinizde özellikle faydalıdır. **Hareketler özeti** sayfasında, madde veya içeriği ve isteğe bağlı olarak toplu işi filtreleyebilir ve ardından bilgileri Excel'e aktarabilirsiniz. Excel'de, örneğin eldeki miktarı, satılan miktarı ve üretimde kullanılmış olan miktarı izole edebilirsiniz.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Maddeler veya hammaddelerle ilgili sorunların bir geçmişi olup olmadığını araştırabilir miyim?
İzleme ayrıntıları, madde veya hammadde ile ilişkili kalite emirleri ve uyumsuzluklarla ilgili bilgiler içerir. Kalite emirleri ve uyumsuzlukların özetini görüntülemek için, Eylem Bölmesinde **Kalite emirleri** veya **Uyumsuzluklar** düğmesine tıklayın. **Not:** Bozucu kalite emirleri, izleme ayrıntılarında birden fazla kez görülebilir. Satın alma emri gibi bir belge için bozucu kalite emri oluşturulduğunda, o belgenin her bir hareketi için görüntülenir.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Madde izlemesi ile ilişkili raporlama özellikleri var mı?
**Müşteriye sevk edildi** raporunu üreterek sevk edilmiş madde veya hammadde tutarını ve sevk edildiği müşterileri belirleyebilirsiniz. Bir uyumluluk ile bağlantılı bir sorgu için tüm müşteriler için rapor oluşturabilirsiniz. Bir müşteri hizmeti ile bağlantılı bir sorgu için, seçilen bir müşteri için rapor oluşturabilirsiniz. Ürün bitmiş maddenin üretiminde kullanılmış bir hammadde ise, bitmiş madde de dahil edilir. **Not:** Satış emirlerini silme veya arşivleme özelliklerini kullanıyorsanız, rapor sonuçları aynı zamanda silinmiş veya arşivlenmiş satış emirlerini de içerir.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Ortak ürünleri ve yan ürünleri izleyebilir miyim?
Ortak ürünleri izleyebilirsiniz, ancak genellikle yan ürünlere atanmış izleme boyutları olmadığından bir yan ürünü izleyemezsiniz. Bir maddeyi izlerken, izleme ayrıntıları ilişkili tüm ortak ürünleri içerir. Ortak ürünü içeren bir düğüm, ayrıntılarda "ortak ürün" sözcüğünü içerir. Ortak ürün hakkındaki ayrıntıları, izleme ayrıntılarında düğümü seçip **Üretim** FastTab'ine tıklayarak görüntüleyebilirsiniz.
