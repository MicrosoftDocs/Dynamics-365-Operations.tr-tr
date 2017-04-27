---
title: "Proje sözleşmeleri"
description: "Bu makalede, Microsoft Dynamics 365 for Operations&quot;da çeşitli proje türleri ve finansman kaynakları için oluşturabileceğiniz proje sözleşmeleri örneklerle açıklanmakta, sözleşmeleri nasıl yöneteceğiniz ve proje müşterilerini nasıl faturalandıracağınız anlatılmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 969a95ddfede4614a346ca07032f4514187de8f2
ms.lasthandoff: 03/31/2017


---

# <a name="project-contracts"></a>Proje sözleşmeleri

[!include[banner](../includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 for Operations'da çeşitli proje türleri ve finansman kaynakları için oluşturabileceğiniz proje sözleşmeleri örneklerle açıklanmakta, sözleşmeleri nasıl yöneteceğiniz ve proje müşterilerini nasıl faturalandıracağınız anlatılmaktadır.

Bir proje sözleşmesi için oluşturduğunuz proje türü, projenin müşterilerinin faturalandırılması için kullanılacak yöntemi belirleyecektir. Bir proje sözleşmesini ve ilgili projeyi değiştirebilirsiniz, ancak proje türünü değiştiremezsiniz. 

Proje sözleşmesi kullanarak, aynı anda bir ya da birden fazla projeyi faturalandırabilirsiniz. Proje sözleşmesi aynı zamanda, bir proje yapısındaki tüm alt projeler için tutarlı bir faturalandırma yordamının uygulanmasını garantilemeye yarar. 

Faturalanacak her projenin bir proje sözleşmesi ile ilişkilendirilmiş olması gerekir. Bir proje sözleşmesi için ayarlar, bu proje sözleşmesi ile ilişkilendirilmiş tüm projelere ve alt projelere uygulanır. 

Bir proje sözleşmesi bir ya da daha fazla finansman kaynağını belirtebilir. Bu nedenle faturalamayı çeşitli finansörlere bölebilir, finansman kaynakları belirli bir tutarın üstünde faturalandırılmasın diye finansman sınırları ayarlayabilir ve borçlandırma harcamalarını için yapılandırabilirsiniz.

## <a name="funding-for-project-contracts"></a>Proje sözleşmeleri için finansman
Bazı proje sözleşmeleri, proje maliyetlerinin finansmanını üstlenme sorumluluğunu birden çok tarafta olduğunu belirtir. Burada bazı örnekler verilmiştir:

-   Birden çok bölüme sahip olan bir müşteri, bir projenin finansmanının bölümler arasında bölünmesini talep eder.
-   Şirketiniz büyük bir projenin maliyetlerini harici bir kuruluşla paylaşır.
-   Bir yol projesi iki belediye tarafından ortaklaşa finanse edilir.
-   Bir köprü projesi bir hükümeti desteği ve bir özel şirket tarafından finanse edilir.

Microsoft Dynamics 365 for Operations'da tek bir işlemin veya tüm bir projenin faturalamasını birden fazla müşteri, bağış veya kuruluş arasında bölebilirsiniz. 

Birden fazla finansöre sahip projelerde, gelişmiş finansman projesine katkıda bulunan tüm taraflar finansman kaynakları olarak adlandırılırlar. Bir müşteri, organizasyon veya destek bir finansman kaynağı olarak tanımlandıktan sonra, bu bir veya daha fazla finansman kuralına atanabilir. Finansman kuralları, giderlerin bir proje için çeşitli finans kaynaklarına nasıl ayrılacağını belirleyen kriterleri içerir. 

Örneğin satınalma taleplerinde veya satınalma siparişlerinde görünenler gibi stoğu tutulan maddeler, bölünemiyor olduklarından, gider tutarı dağıtım zamanında birden fazla finansman kaynağına bölünemez. Bu nedenle, stok çıkışı deftere nakledilene kadar finansman kaynağı değeri 0 (sıfır) kalır. Stok çıkışı deftere nakledildiğinde, maliyet tutarı proje hesap dağıtım kurallarına göre dağıtılır.

Faturalamayı birden fazla fon kaynakları arasında bölmeyi daha kolay hale getirmek için uygulayabileceğiniz bazı adımlar şunlardır:

-   Bir proje için girilen tüm hareketlerin proje sözleşmesindeki para biriminin aynısını kullandığını belirtin.
-   Finansman kaynağının bir proje için belirtilen miktardan daha fazla faturalanmaması için finansman sınırları ayarlayın.
-   Her bir çalışan, kategori, kategori grubu ve hareket türü (veya tüm hareket türleri) için finansman kuralları ve finansman sınırları yapılandırın.
-   Her bir fon kuralının geçerli olacağı dönemi tanımlayan isteğe bağlı başlangıç ve bitiş tarihleri seçin.
-   Her fon kaynağının sorumlu olduğu yüzdeyi belirtin.
-   Hangi finansman kaynağının finansman tahsisat hesaplamalarından kaynaklanacak yuvarlama farklılıklarından sorumlu olduğunu belirtin.
-   Proje maliyetlerinin harici müşterilere nasıl faturalanacağını ve dahili kuruluşlara nasıl masraflandırılacağını belirleyen kurallar ayarların.
-   Hareketleri bir durdurma finans hesabında ek finansman elde edilebilene veya masrafları dahili olarak karşılamaya karar verene kadar kaydedin.

Bir hareket ile hangi vergi grubunun ilişkilendirileceğini belirlemek için, projede bir vergi grubu ataması aranır. Eğer proje düzeyinde hiçbir vergi grubu ataması yapılmadıysa, proje sözleşmesi aranır.

### <a name="example-multiple-funding-sources-simple"></a>Örnek: Birden fazla finansman kaynağı (basit)

Aşağıdaki tablo, birden çok finansman kaynağı arasında finansman tahsisatını yönetmek için senaryolar sağlar. Bu senaryolar aşağıdaki varsayımlar dayanırlar:

-   Öncelik ayarları fonların tahsisatına diğer finansman kuralı ölçütlerinin uygulanmasından önce dahil edilir.
-   Finansman kuralının geçerli olduğu dönem d'yi tanımlamak için hiçbir tarih aralığı belirtilmedi.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Senaryo</strong></td>
<td><strong>Finansman kaynağı </strong></td>
<td><strong>Tahsisat yüzdesi </strong></td>
<td><strong>Ayırma önceliği </strong></td>
</tr>
<tr class="even">
<td>Maliyetleri fonu tükenene kadar bir finansman kaynağına tahsis etmek istiyorsunuz, daha sonra fonları tükenene kadar ikinci bir finansman kaynağına, en sonunda da kalan maliyetleri üçüncü bir finansman kaynağına tahsis etmek istiyorsunuz.</td>
<td><ul>
<li>Finansman　kaynağı　1</li>
<li>Finansman　kaynağı　2</li>
<li>Finansman　kaynağı　3</li>
</ul></td>
<td><ul>
<li>%100</li>
<li>%100</li>
<li>%100</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maliyetlerin yüzde 75'ini bir finansman kaynağına, kalan yüzde 25'i ise ikinci bir finansman kaynağına tahsis etmek istiyorsunuz. Bu finansman kaynaklarından herhangi birisi tükendiğinde, kalan maliyetleri üçüncü bir finansman kaynağından ödemek istiyorsunuz.</td>
<td><ul>
<li>Finansman　kaynağı　1</li>
<li>Finansman　kaynağı　2</li>
<li>Finansman　kaynağı　3</li>
</ul></td>
<td><ul>
<li>%75</li>
<li>%25</li>
<li>%100</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Maliyetlerin yüzde 75'ini bir finansman kaynağına, kalan yüzde 25'i ise ikinci bir finansman kaynağına tahsis etmek istiyorsunuz. Bu finansman kaynaklarından herhangi birisi tükendiğinde, kalan maliyetleri üçüncü ve dördüncü finansman kaynakları arasında bölüştürmek istiyorsunuz.</td>
<td><ul>
<li>Finansman　kaynağı　1</li>
<li>Finansman　kaynağı　2</li>
<li>Finansman　kaynağı　3</li>
<li>Finansman　kaynağı　4</li>
</ul></td>
<td><ul>
<li>%75</li>
<li>%25</li>
<li>%50</li>
<li>%50</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maliyetlerin ilk yüzde 25'ini bir finansman kaynağına, kalanını ise ikinci bir finansman kaynağına tahsis etmek istiyorsunuz.</td>
<td><ul>
<li>Finansman　kaynağı　1</li>
<li>Finansman　kaynağı　2</li>
</ul></td>
<td><ul>
<li>%25</li>
<li>%100</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Örnek: Birden fazla finansman kaynağı (karmaşık)

Aşağıdaki sıralamayla kullanmak istediğiniz üç finansman kaynağınız var:

1.  Finansman kaynağı 2 ve 3'ü, finansman kaynağı 2 tükenene kadar eşit kullanın.
2.  Finansman kaynağı 3 tükenene kadar kullanmaya devam edin.
3.  Finansman kaynağı 3 tükendikten sonra finansman kaynağı 1'i kullanın.

Bu hedefe ulaşmak için, aşağıdakileri yapmalısınız:

-   Finansman kaynağı 2 ve finansman kaynağı 3 için, onlara karşılık gelen tutarlar için finansman sınırları ayarlayın.
-   Aşağıdaki finansman kurallarını oluşturun:
    -   Kural 1 (Öncelik 1): Hareketlerin yüzde 50'sini finansman kaynağı 2'ye ve yüzde 50'sini finansman kaynağı 3'e tahsis edin.
    -   Kural 2 (Öncelik 2): Hareketlerin yüzde 100'ünün finansman kaynağı 3'e tahsis edin.
    -   Kural 3 (Öncelik 3): Hareketlerin yüzde 100'ünün finansman kaynağı 1'e tahsis edin.

Bu kurulum çalışır, çünkü hareket kuralları ve bunlardan herhangi birinin hareketleri için geçerli olup olmadığını belirlemek için sınırları karşı denetlenir. Hareket için hiçbir özel kural uygulanmıyorsa, Tüm hareketler kuralı uygulanır. Tüm hareketler kuralı, tüm hareketlerle eşleşir. 

Bir hareket ile eşleşen bir kural bulunursa, bu kuralda tahsis edilen yüzde ilk önce uygulanır, fakat önce bu eşleşmeler '.'n ayarlanmış olan mevcut sınırlara karşı denetlenmesi gerekir. Eğer bir sınırla karşılaşılırsa, ve bir finansman kaynağı'nın fonları tükenmişse, finansman sınırı ile ilişkilendirilmiş finansman kuralı göz ardı edilir ve program uygulanacak bir sonraki kuralı denetler. 

Bazı durumlarda, bir hareketin yalnızca parçası bir kural altında tahsis edilebilir. Bu, hareket tahsis edildiğinde bir sınıra ulaşıldığında gerçekleşebilir. Bu durumda, kurala sadece belirli bir tutar tahsis edilir, örneğin her finansman kaynağına yüzde 50 gibi. Bu durum, bu bölümde daha önce açıklanmış kural 1'de böyledir. Kalan, sıradaki bir sonraki kurala göre tahsis edilir. 

Aşağıdaki tabloda bu senaryoyu daha ayrıntılı olarak inceler.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Odak </strong></td>
<td><strong>Ayrıntılar</strong></td>
</tr>
<tr class="even">
<td>Finansman kuralları</td>
<td><ul>
<li>Kural 1 (öncelik 1): Tüm hareketler. Finansman kaynağı 2'yi %50'de ve finansman kaynağı 3'ü %50'de tahsis edin.</li>
<li>Kural 2 (Öncelik 2): Tüm hareketler. Finansman kaynağı 3'ü %100'de tahsis edin</li>
<li>Kural 3 (Öncelik 2): Tüm hareketler. Finansman kaynağı 1'ü %100'de tahsis edin</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansman sınırları</td>
<td><ul>
<li>Finansman kaynağı 1 sınırı = 10.000,00</li>
<li>Finansman kaynağı 2 sınırı = 500,00</li>
<li>Finansman kaynağı 3 sınırı = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Hareket 1</td>
<td><strong>Hareket tutarı:</strong> 100,00<strong>Finansman:</strong> Hareket sadece kural 1'e göre ödenecektir çünkü kural 1 uygulandıktan sonra hareket tamamen ödenmiş olacaktır. Hareket, finansman kaynağı 2 ve finansman kaynağı 3 arasında eşit olarak finanse edilir.
<ul>
<li>Finansman kaynağı 2: 50,00</li>
<li>Finansman kaynağı 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Hareket 2</td>
<td><strong>Hareket tutarı:</strong> 5.000,00<strong>Finansman:</strong> Hareket üç kuralın tümüne göre ödenir.<strong>Kural 1</strong>
<ul>
<li>Finansman kaynağı 2: 450,00</li>
<li>Finansman kaynağı 3: 450,00</li>
</ul>
<strong>Kural 2</strong>
<ul>
<li>Finansman kaynağı 3: 250,00 (= 750,00 – 50,00 – 450.00)</li>
</ul>
<strong>Kural 3</strong>
<ul>
<li>Finansman kaynağı 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Her finansman kaynağına dağıtılan toplam fon</td>
<td><ul>
<li>Finansman kaynağı 1: 3.850,00</li>
<li>Finansman kaynağı 2: 500,00</li>
<li>Finansman kaynağı 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Faturalama kuralları
Bir proje sözleşmesi üzerine bir müşteri ile görüşürken, bir proje üzerindeki iş için müşteriye ne zaman ve nasıl fatura kesebileceğinizi tanımlarsınız. Proje sözleşmesini ve projeyi ayarladıktan sonra, proje için faturalama kurallarını ayarlayabilirsiniz. Faturalama kuralları, proje sözleşmesinde belirtilen proje koşullarını temel alır. Oluşturabileceğiniz faturalama kuralları, Zaman ve malzeme veya sabit-fiyat gibi proje sözleşmesindeki faturalama kuralları ile ilişkilendirdiğiniz koşullara ve proje türüne bağlıdır. Proje sözleşmesi için birden fazla ödeme kuralı oluşturabilirsiniz. Aynı proje sözleşmesine ve benzer faturalama kurallarına sahip birden fazla projeye bir faturalama kuralı atayabilirsiniz. 

Aşağıdaki faturalama kural türlerini ayarlayabilirsiniz:

-   **Teslimat birimi** – Bir teslimat birimini tamamladığınızda müşteriye fatura kesin. Teslimat birimlerini sözleşmede tanımlarsınız.
-   **İlerleme** – Projenin belirli bir yüzdesini bitirdiğinizde müşteriye fatura kesin. Tamamlanan çalışma yüzdesini otomatik olarak hesaplamak için bir ödeme kuralı ayarlayabilirsiniz veya yüzdesi tamamlanan çalışmayı ve müşteriye kesilecek fatura tutarını el ile hesaplayabilirsiniz.
-   **Kilometre Taşı** – Projenin kilometre taşına ulaşıldığında müşteriye proje tutarının tamamını faturalandırın.
-   **Ücret** – Müşteriye hizmetleriniz artı (genellikle hizmetlerin bir yüzdesi olan) bir yönetim ücreti için fatura kesin.
-   **Zaman ve malzeme** – Müşteriye projede kullanılan malzemenin ve zamanın değerine göre fatura kesin.

Tüm faturalama kural türleri için, proje önceden anlaşılan bir aşamaya gelene kadar müşteri faturasından düşülecek bir tutma miktarı belirtebilirsiniz. Ödeme tutma yüzdesi proje sözleşmesinde belirtilir. Tutar müşteri faturasındaki satıların toplam değerine dayanarak hesaplanır ve bundan çıkartılır. 

**Zaman ve malzeme** ve **Devam eden** faturalama kuralları için, borçlandırılabilir kategoriler atayabilirsiniz. Borçlandırılabilir kategoriler müşteri faturalarına dahil edilmesi gereken hareketleri gösterir. 

Müşteriyi faturalamaya hazır olduğunuzda, proje için faturalanacak tutar ödeme kuralları esas alınarak hesaplanır ve bir proje fatura teklifi oluşturulur. 

Aşağıdaki bölümlerde bir proje için ödeme kuralları kurmayı ve yönetmeyi gösteren örnekler verilmiştir.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Örnek: Teslim edilen birim sayısını temel alarak bir ödeme kuralı oluşturun

Kuruluşunuz, müşterinin çalışanlarına her biri 10.000 tutarında olacak 5 eğitim seansı vermek üzere bir anlaşmaya imza atar. Her eğitim oturumu sonrasında müşteriye fatura kesersiniz. 

Sözleşme için faturalama kuralları ayarladığınızda, aşağıdaki değerleri kullanırsınız:

-   Bir teslimat birimi, bir eğitim oturumudur.
-   Birim fiyatı eğitim oturumu başına 10.000'dir.
-   Toplam birim sayısı beş eğitim oturumudur.

Bir eğitim oturumunu tamamladığınızda, teslim edilen ilk birim için 10.000'lik bir fatura oluşturabilirsiniz ve faturayı müşteriye gönderebilirsiniz.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Örnek: Projenin belirli bir tamamlanma yüzdesine dayanan bir faturalama kuralı oluşturun (el ile hesaplama).

Bir yazılım danışmanlık şirketi olan kuruluşunuz, bir müşteri ile müşterinin geliştirmekte olduğu bir ürünün bir bölümünü geliştirmek üzere anlaşmaya girer. Kuruluşunuz yazılım kodunu altı aylık bir dönemde teslim etmeyi kabul eder. Müşteri, bu çalışma için kuruluşunuza toplam 100.000 ödemeyi kabul eder. Müşteriye, sözleşmede belirtildiği üzere, tamamlanan işin yüzdesine dayanacak şekilde fatura kesmek üzere bir faturalama kural oluşturursunuz.

-   İlk ayın sonunda tamamlanan çalışma yüzdesini belirlemek için müşteri ile görüşürsünüz. Siz ve müşteri projeyi gözden geçirdikten sonra, projenin tamamlanan yüzdesinin yüzde 15 olduğunu karar verilir.
-   15.000 (100.000'ün yüzde 15'i) için bir fatura oluşturup bunu müşteriye gönderirsiniz.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Örnek: Projenin belirli bir tamamlanma yüzdesine dayanan bir faturalama kuralı oluşturun (otomatik hesaplama).

Bir yazılım geliştirme şirketi olan kuruluşunuz, bir müşteri ile muhasebe bordo paketi yazılımı geliştirmek üzere 30.000'e anlaşır. Müşteri, kuruluşunuza işin tamamlanan yüzdesine dayanarak ödeme yapmayı kabul eder. Proje maliyetinin 20.000 olduğunu tahmin edersiniz. Proje sözleşmesi, faturalama işleminde kullanacağınız iş kategorilerini belirtir. Her kategori için tamamlanan çalışma yüzdesi için fatura tutarlarını otomatik olarak hesaplayacak faturalama kurallarını ayarlarsınız. Her kategori için bir bütçe ayarlarsınız.

-   **Geliştirme** – 15.000'lik maliyet ve 20.000'lik gelir
-   **Kurulum** – 5.000'lik maliyet ve 10.000'lik gelir

İlk kez bir müşteri faturası oluşturduğunuzda, fatura tutarı aşağıdaki bilgilere dayanarak otomatik olarak hesaplanır:

-   Bir ayın sonunda, projeye bakan çalışan, proje için bir zaman çizelgesi gönderir. Çalışanın saatlerinin maliyeti, geliştirme için 5.000 ve kurulum için 1.000'dir. Geliştirme işi yüzde 33 tamamlanmıştır (5.000 fiili maliyet/15.000 bütçe maliyeti) ve kurulum işi yüzde 20 tamamlanmıştır (1.000 fiili maliyet/5.000 bütçe maliyeti).
-   8.667'lik fatura tutarı otomatik olarak hesaplanmış (20.000'in yüzde 33'ü + 10.000'in yüzde 20'si) olur.
-   8.667 için bir fatura oluşturup bunu müşteriye gönderirsiniz.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Örnek: Üzerinde anlaşılmış kilometre taşlarını temel faturalama kuralı oluşturma

Bir yönetim danışmanlık şirketi olan kuruluşunuz, müşterinin satmayı amaçladığı bir ürün için piyasaya araştırması yapmayı kabul eder. Müşteri hizmetlerinizi Mart ayından başlayarak üç aylık bir sürede almayı ve kuruluşunuza 50.000 ödeme yapmayı kabul eder. Projenin üç kilometre taşı vardır:

-   1. Kilometre Taşı: Tüketici verisi toplama - 31 Mart
-   2. Kilometre Taşı: Tüketici verilerini çözümleme – 30 Nisan
-   3. Kilometre Taşı: Ürün uygunluk teklifi sunmak – 31 Mayıs

Müşteri, kuruluşunuza ilk kilometre taşı için 10.000, ikinci kilometre taşı için 20.000 ve üçüncü kilometre taşı için 20.000 ödeme yapmayı kabul eder. 

Proje sözleşmesini ayarladığınızda, müşteriye tamamlanan kilometre taşlarına dayanarak fatura kesmeyi kabul edersiniz. Faturalama kuralı ayarlaması aşağıdaki adımları içerir:

-   Proje kilometre taşlarını tanımla.
-   Her kilometre taşı tamamlandığında, müşteriye faturalanacak miktarı tanımlama.

İlk kilometre taşı 31 Mart tarihinde tamamlandığında, kilometre taşını tamamlandı olarak işaretleyip, 10.000 değerindeki bir faturayı oluşturmak ve müşteriye göndermek. Kilometre taşını tamamlandı olarak seçmediğiniz sürece, bir kilometre taşı için fatura oluşturamazsınız.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Örnek: Hizmetlerin yanı sıra yönetim ücretini de temel alan faturalama kuralı oluşturma

Bir yönetim danışmanlık şirketi olan kuruluşunuz, bir perakende şirketi olan müşterinizin geliştirmekte olduğu bir ürünün uygunluğunu değerlendirmek için piyasa araştırması yapmayı kabul eder. Anlaşmanın koşulları, zaman ve malzeme tabanlı bir araştırma gerçekleştirecek olan en iyi üç yönetim danışmanınızın hizmetlerini sunacağınızı belirtir. Müşteri saat başına 100 artı projeye dahil edilen danışmanlık saatleri için yüzde 10 yönetim ücreti ödemeyi kabul etmiş sayılır. 

Proje sözleşmeni ayarladığınızda, projeye ücretlendirilen danışmanlık saatlerine yüzde 10 yönetim ücret eklemek için bir ödeme kuralı oluşturabilirsiniz. 

Müşteri için bir müşteri faturası oluşturduğunuzda, müşteriye danışmanlık saatlerine ek olarak yüzde 10 yönetim ücreti faturalanır. Örneğin, üç danışman projede toplam 200 saat çalıştıysa, 22.000'lik fatura aşağıdaki hesaplama temel alınarak oluşturulur:

-   Kişi başı 100'den 200 saat = 20.000
-   Yüzde 10 yönetim ücreti = 2.000
-   Toplam fatura tutarı = 22.000

Eğer ücretler müşteriye vergilendirilecekse, proje sözleşmesinde bir vergi grubu seçtiyseniz, vergi grubu ücretlerin faturalama kuralına otomatik olarak girilir.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Örnek: Zaman ve malzemenin değeri için bir faturalama kuralı oluşturma

Bir yazılım danışmanlık firması olan kuruluşunuz, beş teknik danışmanını bir kullanıcının yazılım geliştirme projesi için önümüzdeki altı ay boyunca sağlamak üzere kabul eder. Müşteri her danışmanlık saati için 150 artı ofis malzemelerinin maliyetini ödemeyi kabul eder. Kuruluşunuz, müşteriye her ay sonunda fatura gönderir. 

Proje sözleşmesini ayarladığınızda, projedeki malzeme ve zaman için müşteriye her ay fatura kesmeyi kabul edersiniz. Aşağıdaki bilgileri içeren bir ödeme kuralı oluşturun:

-   Sözleşme dönemi altı aydır.
-   Danışmanlık süresi saatlik 150 olarak hesaplanır.
-   Ofis malzemeleri maliyetinden faturalanır ve proje için maliyeti toplam 10.000'i aşmamalıdır.
-   Proje süresince her takvim ayının sonunda bir müşteri faturası oluşturur.

İlk ay boyunca danışmanlar tarafından proje üzerinde toplam 800 saat kaydedilir. Projeye harcanan ofis malzemelerinin maliyeti 2.000'dir. Bu nedenle ay sonunda, saatlik 150'den 800 saat artı ofis malzemeleri için 2.000 toplamında 122.000'lik bir fatura oluşturursunuz.




