---
title: "Proje yönetimi ve muhasebe"
description: "Proje yönetimi ve muhasebe işlevi, birden çok sektörde hizmet almak, ürün üretmek veya bir sonuç elde etmek için kullanılabilir."
author: KimANelson
manager: AnnBe
ms.date: 01/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable; ProjProjectManagementWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b8f2f3a33dc19c2ebc941d1a504eae0c276f3cdf
ms.openlocfilehash: 46c8ecf8a6988c32d0202c631bef6901f467bb89
ms.contentlocale: tr-tr
ms.lasthandoff: 06/25/2018

---

# <a name="project-management-and-accounting"></a>Proje yönetimi ve muhasebe

[!include [banner](../includes/banner.md)]

Proje yönetimi ve muhasebe işlevi, birden çok sektörde hizmet almak, ürün üretmek veya bir sonuç elde etmek için kullanılabilir.  

Proje, bir servis sağlamak, bir ürün üretmek veya bir sonuç elde etmek üzere tasarlanmış etkinlikler grubudur. Proje kaynakları kullanır ve gelirler veya kıymetler biçiminde finansal sonuçlar üretir.

## <a name="projects-across-industries"></a>Endüstrilerdeki projeler
Proje yönetimi ve muhasebe işlevi, aşağıdaki şekilde gösterildiği gibi birden fazla endüstride kullanılabilir. [![Endüstriler arasındaki projeler](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

Çağrı merkezinde bir bilet, bir çağrının çözülmesi için gerekli eylemlerin tanımlanması için kullanılabilir. Yönetim veya teknik danışmanlık kuruluşları veya reklam acenteleri gibi danışmanlık şirketleri projeler olarak bu etkinliklere bakar. Pazarlamada, kampanya temsil edilmesi gereken iş kümesini temsil eder. Projeye dayalı üretimlerde bir üretim emri, hedeflenen nihai ürünlerin üretilmesi için gerçekleştirilmesi gereken çeşitli çalışmaları kapsar. Bu projeler nasıl adlandırılırsa adlandırılsın kaynaklar, planlar ve maliyetler içerir ve Microsoft Dynamics 365 for Finance and Operations'taki proje yönetimi ve muhasebe işlevi bu projelerin planlanması, uygulanması ve analiz edilmesine yardımcı olabilir.

## <a name="project-phases"></a>Proje aşamaları
Aşağıdaki süreç akışı, harici projelere veya bir veya daha fazla sayıda müşteri için tamamlanmış bir projeye yönelik olsa dahi bu işlev aynı zamanda dahili, maliyete dayalı projeler için de geçerlidir. 

![Bir projenin 3 aşaması](./media/3-stages-of-a-project.png) 

Önceki şekilde gösterildiği gibi, proje yönetimi ve muhasebesi üç aşamaya bölünebilir:

1.  Başlangıç
2.  Yürüt
3.  Analiz et

## <a name="initiate-the-project"></a>Projenin başlatılması
Proje başlatma sırasında birkaç temel işlem gerçekleşir. Tahmini işçiliği, giderleri ve malzemeleri müşteriye bildirmek için proje teklifini kullanabilirsiniz. Faturalama şartlarını, sınırları ve sözleşmeleri bir proje sözleşmesine kaydedebilirsiniz. İşi planlamak ve tahmin etmek için iş kırılım yapısı (İKY) kullanabilirsiniz. Proje yürütmeye yol göstermesi için tahminleri ve bütçeleri ayarlayabilirsiniz. Aşağıdaki resimde bir proje yapısı gösterilmektedir. [![proje yapısı](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Proje teklifleri oluştur

Bir projenin ilk satış aşamasında bir proje teklifi, müşteriye bağlayıcı nitelikte olmayan bir teklif sunmanıza izin verir. Teklif, teklif edilen maddeler ve hizmetler, temel sözleşme bilgileri, özel ticari sözleşmeleri ve iskontoları ve olası vergiler ve ek giderler gibi öğeleri içerebilir.

Ayrıca, organizasyonunuz ile müşteri arasında bir proje teklif hareketi için bir teminat mektubu da oluşturabilirsiniz. Proje teklifi oluşturulduktan sonra müşteri için teminat mektubu talebi oluşturabilir ve bunu bankaya gönderebilirsiniz. Banka, talebi onayladıktan sonra teminat mektubu müşteriye gönderilir. 

Daha fazla bilgi için [Proje teklifleri](project-quotations.md) bölümüne bakın.

### <a name="create-project-contracts"></a>Proje sözleşmeleri oluştur

Bir müşteri veya başka bir finansman kaynağı ile bir projeyi tamamlamak üzere anlaşmaya vardığınızda öncelikle bir proje sözleşmesi oluşturmanız gerekir. Ardından, projeyi oluşturduğunuzda bunu ilgili sözleşmeye atamalısınız. Bir proje sözleşmesi için oluşturduğunuz proje türü, proje müşterilerinin faturalandırılması için kullanılacak yöntemi belirleyecektir. Bir proje sözleşmesini ve ilgili projeyi değiştirebilirsiniz, ancak proje türünü değiştiremezsiniz. Proje türleri hakkında daha fazla bilgi için "Proje oluşturma" bölümüne bakın.

Proje sözleşmeleri hakkında daha fazla bilgi için [Proje sözleşmeleri](project-contracts.md) bölümüne bakın.

### <a name="create-work-breakdown-structures"></a>Çalışma kırılım yapıları oluşturma

Bir WBS'nin ayrıntı derecesi, tahminlerde gerekli olan kesinlik düzeyine ve bu tahminlerin gerektirdiği izleme düzeyine bağlıdır. Plan veya maliyet açısından hataya çok düşük bir toleransı olan projeler genellikle daha ayrıntılı bir WBS içerir ve ayrıca çalışmanın ilerlemesinin ve maliyetinin WBS ile dikkatli bir şekilde kıyaslanarak takip edilmesini gerektirir. 

Daha fazla bilgi için [İş kırılım yapıları](work-breakdown-structures.md) bölümüne bakın.

### <a name="create-project-forecasts-and-budgets"></a>Proje tahminleri ve bütçeleri oluşturma

Organizasyonunuz bir operasyonel perspektife sahipse ve belirli hareketlerden elde edilen gelirlere ve çıkan maliyetlere odaklanıyorsa tahmin yöntemini kullanabilirsiniz. Ancak, organizasyonunuz daha çok mali tutarlara odaklanıyorsa bütçe yöntemini kullanabilirsiniz. Her yöntemin kendine göre avantajları vardır. Daha fazla bilgi için [Proje tahminleri ve bütçeleri](project-forecasts-budgets.md) bölümüne bakın.

### <a name="create-projects"></a>Projeler oluştur

Microsoft Finance and Operations'da altı proje türü oluşturabilirsiniz. Her proje türü farklı maliyetlerin ve gelirin tanınması için farklı şekilde ayarlanır. Seçtiğiniz proje türü, projenin türüne dayalıdır. Aşağıdaki tabloda her bir proje türünün tipik kullanımı açıklanmıştır.
                                                                                                            
<table>
  <tr>
    <td>Proje türü</th>
    <td>Açıklama</th>
  </tr>
  <tr>
    <td>Zaman ve malzeme</td>
    <td>Zamana ve malzemeye dayalı projelerde müşteri, bir projede yapılan tüm maliyetler için faturalandırılır. Bu maliyetler saat, giderler, maddeler ve ücretler için yapılan maliyetleri de içerir.</td>
  </tr>
  <tr>
    <td>Sabit fiyat</td>
    <td>Sabit fiyatlı projelerde, faturalar açık hesap hareketlerinden oluşur. Bir sabit fiyatlı proje bir proje sözleşmesine dayanan bir faturalama zamanlamasına göre faturalanır. Sabit fiyatlı bir proje için gelir, tamamlanan yüzde yöntemi kullanılarak hesaplanabilir ve proje genelinde nakledilebilir. Alternatif olarak gelir, proje tamamlandığında tamamlanan sözleşme yöntemi kullanılarak hesaplanabilir ve proje genelinde nakledilebilir. Şirketler sıklıkla bir projenin veya bir grup projenin tamamlanma derecesini hesaplamak üzere süren iş (WIP) değerinin sunduğu avantajlardan yararlanır.</td>
  </tr>
  <tr>
    <td>Yatırım</td>
    <td>Yatırım projeleri anlık kazançlar içermeyen projelerdir. Tipik olarak, maliyetlerin mutlaka aktifleştirilmesi gereken, uzun vadeli dahili projeler için kullanılır. Bir yatırım projesi için sadece maddeler, saat ve giderler için yapılan maliyetler kaydedilebilir. Bir Yatırım projesinin maliyeti tahmin işlevi kullanılarak takip ve kontrol edilir. Yatırım projeleri bir opsiyonel maksimum aktifleştirme kullanılarak oluşturulabilir. Bir Yatırım projesi ilerledikçe maliyetlerini WIP hesaplarına kaydedersiniz ve burada maliyetler, proje tamamlanana kadar tutulur. Proje elendiğinde, süren iş değerini sabit bir kıymete, bir genel muhasebe hesabına veya yeni bir projeye transfer edersiniz. <br></br> <strong>NOT:</strong> Yatırım projelerindeki hareketler <strong>Maliyetleri deftere naklet<strong>, <strong>Gelir tahakkuku</strong> ve <strong>Fatura teklifleri oluştur</strong> sayfalarında gösterilmez.</td>
  </tr>
  <tr>
    <td>Maliyet projesi</td>
    <td>Yatırım projelerinde olduğu gibi, Maliyet projeleri de tipik olarak dahili projelerin takip edilmesi için kullanılır ve bu projeler için sadece saatler, giderler ve maddeler kaydedilebilir. Ancak, Maliyet projeleri genellikle Yatırım projelerine kıyasla daha kısa sürelidir. Ek olarak, Yatırım projelerinin aksine, Maliyet projeleri, bilanço hesaplarına aktifleştirilemez. Bunun yerine, proje hareketleri yalnızca kar ve zarar hesaplarına nakledilir. <br></br> <strong>NOT:</strong> Maliyet projelerindeki hareketler <strong>Maliyetleri deftere naklet</strong>, <strong>Gelir tahakkuku</strong> ve <strong>Fatura teklifleri oluştur</strong> sayfalarında yansıtılmaz. Maliyet projeleri genellikle dahili projeleri izlemek için kullanıldığından, genellikle bir müşteri hesabıyla ilişkili olmaları gerekmez. Ancak, kurulumunuz gereği satın alma emirleri için madde gereksinimlerinin oluşturulması gerekiyorsa Maliyet projesini mutlaka bir projeyle ilişkilendirmelisiniz. Bu ilişkilendirme, madde gereksinimlerin satış emri satırları olarak yönetilmesinden ve sistemin bir müşterinin tanımlanmasını gerektirmesinden kaynaklanır. Ancak, bu kurulum, madde gereksinimlerinin otomatik olarak bir satın alma emrinden oluşturulmasına neden olmaz. Maliyet projeleri için <strong>Madde gereksinimi oluştur</strong> ayarı göz ardı edilir. Bir Maliyet projesinde bir madde gereksinimine ihtiyaç duyuyorsanız, projeyle bir müşterinin ilişkilendirilmiş olması şartıyla bunu manuel olarak oluşturabilirsiniz.</td>
  </tr>
  <tr>
    <td>İç</td>
    <td>Dahili projeler, kuruluşunuzdaki dahili bir projedeki maliyetleri izlemek için kullanılır. Dahili projeler kaynak tüketimini yönetmek için bir planlama aracı sağlar. <br></br><strong>NOT:<strong> Dahili projelerdeki hareketler <strong>Gelir tahakkuku</strong> ve <strong>Fatura teklifleri oluştur</strong> sayfalarına yansıtılmaz.</td>
  </tr>
  <tr>
    <td>Zaman</td>
    <td>Zaman projeleri örneğin çalışanların hastalık izinlerinin takip edilmesi projesi vb. gibi ücretlendirilmeyen ve üretimle bağlantılı olmayan faaliyetlerle ilişkilendirilen sürelerin takip edilmesi için kullanılır. Zaman projelerindeki hareketler deftere nakledilmez. Bunun yerine, çalışan yararlanım raporlarına dahil edilir. Zaman projelerinde yalnızca saat hareketleri kaydedilebilir. Bu saatleri projeye kaydetmek için bir saat günlüğü veya zaman çizelgesi kullanılır. Saatler kaydedildikten sonra proje hareketleri olarak görünür ancak karşılık gelen fiş hareketleri yoktur. <br></br><strong>NOT:</strong> Zaman projelerindeki hareketler <strong>Maliyetleri deftere naklet</strong>, <strong>Gelir tahakkuku</strong> ve <strong>Fatura teklifleri oluştur</strong> sayfalarında yansıtılmaz.</td>
  </tr>
</table>


### <a name="assign-workers-categories-and-resources"></a>Çalışan, kategori ve kaynak atama

Çalışan kaynaklarını bir projenin gereksinimlerine ve planına veya çalışanların yeteneklerine ve müsaitlik durumuna bağlı olarak planlayabilirsiniz. Kaynak planlama özelliklerini kullanarak, organizasyonunuzun çalışanlarını üretken ve üretken şekilde kullanabilirsiniz. Projenizde çalışmak için müsait olan, en kalifiye çalışanları hızlı bir şekilde bulabilirsiniz. Ayrıca, proje süresince bu çalışanlardan nasıl daha üretken şekilde yararlanılabileceğini de kolayca görebilirsiniz. 

Burada kaynak planlama işlevinin nasıl kullanılacağına dair bazı yollar gösterilmiştir:

-   Çalışanı bir projenin gereksinimleriyle eşleştirmek için çalışanın özellikleri, örneğin eğitimi, yetenekleri, sertifikaları ve proje deneyimi hakkındaki bilgileri kullanın.
-   Bir çalışanın planını proje takvimiyle eşleştirmek için o çalışanın takvimi ve müsaitliği hakkındaki bilgileri kullanın.
-   Her bir çalışanın kapasitesini gözden geçirin ve kapasitenin nasıl kullanılacağını belirleyin. Örneğin bir çalışandan yeterince yararlanılamıyorsa çalışan, müsaitliğine ve özelliklerine uygun bir projeye atanabilir.
-   Çalışanın görevleriyle bir takvim çakışması bulunmadığından emin olmak için çalışanın müsaitliğini gözden geçirin.
-   Çalışandan faydalanma durumunu bir özet görünümünde (örneğin, departmana veya çalışana göre) veya ayrıntılı görünümde (örneğin, bir departmandaki çalışanlara veya her bir çalışan için haftalık bilgilere göre) gözden geçirin.
-   Çalışanlardan nasıl yararlanıldığını optimize etmek için gün, hafta veya ay gibi çeşitli zaman birimleri için kaynak atamalarını değiştirin.

## <a name="execute-the-project"></a>Proje yürütme
Proje yürütme sırasında ekip üyeleri veya yöneticiler zaman çizelgeleri, gider raporları ve diğer ticari belgeleri kullanarak işi ve yapılan giderleri kaydeder. Proje yöneticileri, proje için bütçelenen tutarların tüketimini izlemek için araçlara sahiptirler. Ayrıca proje yöneticileri malzeme sipariş etme, çekme veya satın alma işlemlerini satın alma emirlerini ve diğer ticari belgeleri kullanarak gerçekleştirebilirler. Müşterilerin devam eden iş için faturalandırılabilmesi için faturalar hazırlanır ve onaylanır. Son olarak, bu süreç sırasında organizasyonun mali durumunu etkileyen gelir belirlenir.

### <a name="manage-work-breakdown-structures"></a>İş kırılım yapılarını yönetme

WBS bir proje için tamamlanacak işlerin açıklamasıdır. WBS, bir görevler hiyerarşisidir. Sadece her bir göreve yönelik işleri temsil etmez, aynı zamanda görevin boyutunu, maliyetini ve süresini de temsil eder. 

Daha fazla bilgi için [İş kırılım yapıları](work-breakdown-structures.md) bölümüne bakın.

### <a name="manage-project-forecasts-and-budgets"></a>Proje tahminlerini ve bütçelerini yönetme

Projelerinizi yönetmenizin ve kontrol etmenizi iki yöntemi vardır: proje tahminleri ve proje bütçeleri. Organizasyonunuz bir operasyonel perspektife sahipse ve belirli hareketlerden elde edilen gelirlere ve çıkan maliyetlere odaklanıyorsa tahmin yöntemini kullanabilirsiniz. Ancak, organizasyonunuz daha çok mali tutarlara odaklanıyorsa bütçe yöntemini kullanabilirsiniz.

Daha fazla bilgi için [Proje tahminleri ve bütçeleri](project-forecasts-budgets.md) bölümüne bakın.

### <a name="create-production-orders"></a>Üretim emirleri oluşturma

Projeyle ilgili bir üretim emri, nihai ürün yöntemi veya tüketilen madde yöntemi kullanılarak bir satış emri veya bir madde gereksinimi ile ilişkilendirilebilir. Buna ek olarak, üretim emri manuel olarak oluşturulmuşsa üretim emri ile satış emri veya madde gereksinimi (emre bağlantı yoktur) arasında hiçbir bağlantı yoktur. Ancak, bir satış emrinin yerine getirilmesi veya bir madde gereksiniminin karşılanması amacıyla üretim emri otomatik olarak oluşturulmuşsa üretim emri ile satış emri veya madde gereksinimi (emre bağlantı vardır) arasında bir bağlantı vardır. 

Bu faktörlerin kombinasyonlarına dayalı olarak, aşağıdaki yöntemlerden birini kullanın:

- **Tamamlanan madde/bağlantılı sipariş** – Projeyi bir satış emrine veya bir madde gereksinimine bağlayın. Bu yöntem kullanılıyorsa satış emri faturalandığında veya sevk irsaliyesi, madde gereksinimini için güncelleştirildiğinde gerçek proje maliyetleri nakledilir. Maliyet bir tamamlanan madde olarak nakledilir.
- **Tamamlanan madde/bağlantılı olmayan sipariş** – Fiili maliyetler, bir madde için üretim döngüsünün durumu **Sonlandırıldı** olmadan nakledilemez. Tamamlanan madde maliyeti tek bir hareket olarak nakledilir.
- **Tüketilen madde/bağlantılı sipariş** – Projeyi bir madde gereksinimine bağlayın. Bu yöntemi kullanarak, üretimin durumu **Başlatıldı** olduğunda veya bitti olarak raporlandığında gerçek proje maliyetlerini görüntüleyebilirsiniz. Maliyetler, üretim için kullanılan hammaddelere ve saatlere yönelik birden çok proje madde hareketi olarak deftere nakledilir. Madde gereksinimi için sevk irsaliyesi güncelleştirildiğinde, hiçbir proje maliyeti deftere nakledilmez. Üretimdeki projelerin takip edildiği ürün reçetesi (BOM) hiyerarşisindeki seviyeyi de tanımlayabilirsiniz.
- *<strong><em>Tüketilen madde/bağlantılı olmayan sipariş</em></strong>*– Projeyi bir madde gereksinimine bağlayın. Bu yöntemi kullanarak, üretimin durumu <strong>Başlatıldı</strong> olduğunda veya bitti olarak raporlandığında gerçek proje maliyetlerini görüntüleyebilirsiniz. Maliyetler, üretim için kullanılan hammaddelere ve saatlere yönelik birden çok proje madde hareketi olarak deftere nakledilir. Üretimdeki projelerin takip edildiği BOM hiyerarşisindeki seviyeyi de tanımlayabilirsiniz.

### <a name="procure-products-and-services"></a>Ürün ve hizmet tedarik etme

Maddelerin satın alınması ve satılması birçok proje temelli ticarette yaygın faaliyetlerdir.

#### <a name="purchase-orders-for-projects"></a>Projeler için satın alma emirleri

Satın alma emrinin amacı, satın alma emrinin ne zaman tamamlanacağını ve buna bağlı olarak maddelerin ne zaman bir projeye gider yazılacağını belirlemektir.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Yöntem</th>
<th>Amaç</th>
<th>Maddelerin tüketimi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Doğrudan bir satın alma emri oluşturun.</td>
<td>Bir projedeki tüketim için harici bir satıcıdan madde satın alın. Satın alma emrini oluşturmak için şu yöntemleri kullanabilirsiniz:
<ul>
<li>Projenin içinden. Bu durumda proje halihazırda satın alma emri için tanımlanmıştır.</li>
<li>Proje satın alma emrine gelerek. Hem satıcıyı hem de satın alma emrinin oluşturulacağı projeyi seçmeniz gerekir.</li>
</ul></td>
<td>Maddeler satıcı faturası güncelleştirildiğinde tüketilir.</td>
</tr>
<tr class="even">
<td>Bir satış siparişinden satınalma siparişi oluşturma.</td>
<td>Maddeleri bir projeden bir satış emri oluşturduğunuzda satın alın.</td>
<td>Maddeler, satış siparişinin faturası müşteriye kesildiğinde tüketilir.</td>
</tr>
<tr class="odd">
<td>Bir madde gereksiniminden satınalma siparişi oluşturma.</td>
<td>Maddeleri bir projeden bir madde gereksinimi oluşturduğunuzda satın alın.</td>
<td>Maddeler, madde gereksinimi sevk irsaliyesi güncelleştirildiğinde tüketilir.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Projeler için satış emirleri

Proje yönetimi ve muhasebesinde madde tüketimini çeşitli yöntemlerle kaydedebilirsiniz. Bir projedeki maddeleri satabilir veya satın alabilir veya bir proje için madde rezerve edebilirsiniz. 

Bir projede tüketilmek üzere maddeleri şirketin stokundan sipariş edebilirsiniz. Alternatif olarak, maddeleri harici bir satıcıdan satın alabilirsiniz. Maddeler Zaman projeleri dışındaki tüm proje türlerinde tüketilebilir. 

Maddeleri sipariş etme yönteminiz bunları nereden sipariş ettiğinize göre değişir:

-   Maddeleri şirketin stokundan sipariş etmek için siparişi mutlaka bir madde gereksinimi olarak girmeniz gerekir. **Madde gereksinimleri** sayfasını kullanıyorsanız, gereksinimi maddeleri kısmi teslimat olarak alacak şekilde ayarlayabilirsiniz. Böylece, maddeler gerekli olana kadar maddelerin bir miktarının tüketimini erteleyebilirsiniz.
-   Maddeleri bir harici satıcıdan sipariş etmek için **Satın alma emri** sayfasında siparişi bir satın alma emri olarak oluşturabilirsiniz.

> [!NOTE] 
> Maddeler halihazırda paketleme için işaretlenmişse bir projeye dayalı satış emri için sevk irsaliyesi iptal edilemez. 

Aşağıdaki tabloda madde sipariş yöntemleri listelenmiş ve maddelerin nasıl tüketileceği açıklanmıştır.

| Yöntem            | Amaç                                                                                                                                                        | Madde tüketim hareketleri                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Satış siparişi       | Bir hareketi doğrudan bir Zaman ve malzeme projesine girin.                                                                                                   | Madde hareketleri müşteri faturası deftere nakledildiğinde tüketilir.                                                                               |
| Stok günlüğü | Madde kayıtlarını hızlı şekilde girin ve bu şekilde kaydını tutun. Örneğin, bir madde gereksinimini yazdırılmış bir listeye göre girmek istiyorsanız stok defteri uygulanabilir. | Madde hareketleri günlük deftere nakledildiğinde tüketilir.                                                                                        |
| Madde gereksinimi  | Hemen tüketilmeyecek olan maddeleri girin. Bu yöntem, tek bir madde gereksinimi kaydında tüketilmiş madde sayısının izlenmesine olanak sağlar.    | Madde hareketleri sevk irsaliyesi güncelleştirildiğinde tüketilir. Diğer bir deyişle, madde gereksinimi, sevk irsaliyesi nakledildiğinde oluşturulur. |
| Satın alma siparişleri   | Hareketleri satın alma yöntemine bağlı olarak üç konumdan birine girin.                                                                              | Madde hareketleri, sevk irsaliyesi güncelleştirmesinde veya müşteri ya da satıcı faturalandığında tüketilir.                                      |

### <a name="process-project-invoices"></a>Proje faturalarını işleme

Proje tipi, hangi faturalama yordamının uygulanacağını belirler. Sadece iki harici proje türü (Zaman ve malzeme ve Sabit fiyatlı) faturalandırılabilir. Zaman ve malzeme projeleri ile sabit fiyatlı projeler her zaman bir proje sözleşmesine iliştirilir. 

Bir proje için bir müşteri faturası oluşturmadan önce, ön fatura ya da fatura teklifi oluşturabilirsiniz. Bir fatura teklifinde, bir proje faturasına dahil edilecek proje hareketlerini seçebilirsiniz. Daha sonra, proje faturasını deftere nakletmeden veya müşteri veya diğer finans kaynağına göndermeden önce fatura ayrıntılarını gözden geçirebilirsiniz. 


Proje faturalarının nasıl işleneceği hakkında daha fazla bilgi için [Proje faturalandırma](../accounts-payable/project-invoicing.md) bölümüne bakın.


### <a name="calculate-the-cost-to-complete-a-project"></a>Bir projenin tamamlanacağı maliyeti hesaplama

Bir tahmin oluşturduğunuzda projenin tamamlanması maliyetini hesaplamak için kullanılan yöntemi seçebilirsiniz. **Tahmin oluştur** sayfasındaki **Proje tamamlama maliyeti** alanından bir yöntem seçin. Seçtiğiniz yöntem, maliyet tahminindeki her bir maliyet satırına ayrı olarak uygulanır. Bir satır **Oluşturuldu** durumuna sahipse, buna uygulanacak yöntemi **Maliyet tahmini** sayfasından değiştirebilirsiniz. 

Aşağıdaki tabloda proje tamamlama maliyetinin hesaplanması için kullanılabilecek yöntemler açıklanmıştır.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Yöntem</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Toplam maliyet – gerçek</td>
<td>Tahmini maliyetleri mutlaka manuel olarak girilmelidir. <strong>Maliyet tahmini</strong> sayfasındaki <strong>Toplam maliyet</strong> veya <strong>Toplam miktar </strong>sütunu tamamlandığında fiili maliyetler, kullanıcı tarafından girilen toplam tutarlardan çıkarılır. Neticesinde proje tamamlama maliyeti elde edilir. Tipik olarak, maliyetlerin ilerleyişi örneğin her bir dönemde kaydedilen otel konaklama ve yemek sayısına göre takip edilmez. Bunun yerine. İzleme genellikle tahmini toplam saat miktarına karşı bir karşılaştırmaya dayanır. Bu yaklaşım bir tahmin modeli gerektirmez ve toplam maliyet ve toplam miktar manuel olarak değiştirilebilir. <strong>Toplam maliyet</strong> veya <strong>Toplam miktar</strong> sütununa bir değer girildiğinde Finance and Operations, bu değeri dönemde aktarılan gerçek hareketlerle karşılaştırır ve ardından <strong>Tamamlanacak miktar</strong> veya <strong>Tamamlama maliyeti</strong> sütunundaki eğeri düşürür.</td>
</tr>
<tr class="even">
<td>Toplam bütçe – gerçek</td>
<td>Fiili maliyetler, maliyeti belirlemek için seçtiğiniz tahmin modeliyle karşılaştırılır. Bu yöntem, tahmin edilen hareketleri içeren bir toplam bütçe modeli kullanır. Projenin daha doğru bir görünümünü elde etmek için proje devam ederken bütçe modelini ayarlayabilirsiniz. Tahmin ayarlamanız gerekiyorsa şu genel süreci izleyin:
<ol>
<li>Tahmin hareketlerini başka bir tahmin modeline kopyalayın.</li>
<li>Tahmin hareketleriyle gerçek hareketleri karşılaştırın.</li>
<li>Sonraki dönem için tahminleri koruyun, azaltın veya artırın.</li>
</ol>
Finance and Operations, öngörülen tahminleri otomatik olarak azaltmaz. Bu nedenle, proje tamamlandığında karşılaştırma için bir temel oluşturmak için Sabit fiyatlı projede bir orijinal tahmin modelinin korunması iyi bir fikirdir. 
<br></br> <strong>NOT:</strong>Bu yöntemi seçtiğinizde en az iki tahmin modeli kullanın. bir modeli orijinal tahmini içermelidir. Diğer model için, tahmin modellerini başka bir modelden kopyalamanız gerekir. Bu yöntem sadece Sabit fiyatlı projeler ve Yatırım projeleri için geçerlidir.</td>
</tr>
<tr class="odd">
<td>Kalan bütçe</td>
<td>Bu yöntem, projenin tamamlanması için gerekli maliyeti hesaplamak için bir kalan bütçe modeli kullanır. Bu yöntemi kullandığınızda, fiili maliyetler ve kalan bütçe modelindeki tahmin edilen tutarlar toplanır. Sonuç toplam maliyettir. Bu yöntemi kullanmadan önce hareketlerin sisteme kaydettiğiniz gerçek hareketlere dayalı olarak düşürülmesi için mutlaka bir kalan bütçe modeli kurulmalıdır. <strong>Tahmin modelleri</strong> sayfasında, alanların <strong>Otomatik tahmin azaltma</strong> grubunda işaretlendiğinden emin olun. Tipik olarak, bir kalan bütçe bir orijinal bütçeden kopyalanır. Hareketler girildikçe kalan bütçedeki hareketler düşürülür. Proje ilerledikçe kalan bütçenin mutlaka ayarlanması gerektiğine karar verirseniz tahmin hareketlerini kalan bütçeye şarj edersiniz. <br></br> <strong>NOT:</strong> Bu yöntem ancak tahmine bir tahmin modeli eklenmişse uygulanabilir.</td>
</tr>
<tr class="even">
<td>Önceki tahmin gibi</td>
<td>Önceki dönem içinde kullanılan aynı tahmin yöntemi uygulanır. Önceki dönem bir tahmin modeli gerektirdiyse bu yöntem bir tahmin modeli gerektirir.</td>
</tr>
<tr class="odd">
<td>Tamamlama maliyetini sıfıra ayarla</td>
<td>Tipik olarak, bu yöntem tahmin projesi kaldırılmadan kullanılır. Bu yöntem, toplam tahminleri nakledilen gerçek hareketlerle eşleştirir ve <strong>Tamamlanacak maliyet</strong> sütununu siler. Neticedeki tamamlanma yüzdesi daima yüzde 100'dür. <strong>Tahmin</strong> alanı, oluşturduğunuz her bir maliyet satırı için seçilmez ve toplam tahmin bir önceki maliyet tahmininden kopyalanır. Tahmin dönemi için asıl tüketim proje tamamlama maliyetinden çıkarılır. Bu yöntem için bir tahmin modeli gerekmez.</td>
</tr>
<tr class="even">
<td>Maliyet şablonundan</td>
<td>Seçilen tahmin yöntemiyle ilişkilendirilen maliyet şablonunda kurulan tamamlama maliyeti yöntemi uygulanır.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Projeyi analiz etme
En temel seviye olduğundan bir proje, maliyetleri kaydeden hareketleri gruplandırmak ve ardından bu maliyetleri gene deftere nakletmek için kullanılır. 

Genellikle, bu hareketler zaman çizelgeleri, gider raporları, satıcı faturaları veya stok hareketleri gibi ticari belgelerin sonucudur. Bir projenin yaşam döngüsü genellikle projenin işlerinin ve mali etkisinin planlanmasına ve kestirilmesine yardımcı olan tahminler, kestirimler ve bütçelerle başlar. Bir projeyi analiz ederken, yalnızca proje sırasında meydana gelen hareketleri değil, aynı zamanda tahminlerinizin ve kestirimlerinizin doğruluğunu, proje ekip üyelerinden yararlanma oranlarını ve projenin genel başarısını değerlendirebilirsiniz.

### <a name="analyze-cash-flow"></a>Nakit akışını analiz etme

Hem tahmin edilen nakit akışlarını hem de bir proje için fiili nakit akışlarını gözden geçirmek için nakit akışı takip işlevini kullanın. Bir proje devam ederken nakit akışlarını gözden geçirebilir veya tamamlanan bir projenin nakit akışlarını görüntüleyebilirsiniz. 

Nakit akışlarını takip ederek tek bir projeyi değerlendirebilir, birden çok projeyi görüntülemek için raporları kullanabilir ve proje nakit akışını genel defterdeki nakit akış tahminlerine transfer edebilirsiniz.

#### <a name="cash-inflow-forecasting"></a>İçeri nakit akışı tahmin etme

Kurulumunuza bağlı olarak, seçili bir proje için içeri nakit girişlerini tahmin edebilirsiniz. Örneğin, projenin tarihi 5 Mart 2012 ise ve faturanız 31 Mart 2012 tarihindeyse, vade tarihini ve beklenen satış ödeme tarihini tahmin etmek için şu yöntemi kullanabilirsiniz:

-   **Proje tarihi:** 5 Mart 2012.
-   **Fatura tarihi:** 31 Mart 2012. Bu tarih fatura sıklığı temel alınarak belirlenir. Bu örnek için, fatura sıklığını güncel ay olarak ayarladınız. Bu nedenle, Mart ayında nakledilen tüm hareketler ayın son günü faturalandırılır.
-   **Vade tarihi:** 14 Nisan 2012. Bu tarih, proje için ayarlanan ödeme koşulları temel alınarak belirlenir. Bu örnek için ödeme süresini 14 gün seçtiniz. Bu nedenle, fatura tarihine 14 gün eklenerek vade tarihi 14 Nisan 2012 olarak bulunur.
-   **Beklenen satış ödeme tarihi:** 27 Nisan 2012. Bu tarih, **Proje yönetimi ve muhasebe parametreleri** sayfasındaki **Genel tampon gün sayısı** alanındaki gün sayısı  **Proje sözleşmeleri** sayfasındaki **Ayrı tampon gün sayısı** alanındaki gün sayısına eklenerek ve ardından bu toplam değer **Vade tarihi** alanındaki gün sayısına eklenerek hesaplanır. Bu örnekte **Genel tampon günleri** alanına **3** ve **Ayrı tampon günleri** alanına **10** değerini girdiniz. Bu nedenle, vade tarihine 13 gün eklenerek beklenen satış ödemesi tarihi 27 Nisan 2012 olarak belirlenir.

Genel tampon günleri, ayrı tampon günlerinin yerini alabilir veya ayrı tampon günlerine eklenebilir:

-   Genel tampon günlerini ayrı tampon günleri yerine kullanmak için, müşteriler için vade tarihi ile gerçek ödeme tarihi arasındaki ortalama gün sayısını girin.
-   Ayrı toplam günlerine genel tampon günleri eklemek için, **Genel tampon günleri** alanında, müşterinin ödemeyi gönderdiği tarih ile organizasyonunuzun ödemeyi aldığı tarih arasındaki gün sayısı için tahmininizi girin.

Ayrı tampon günlerini proje sözleşmesinde ayarlayın. Günler, hem satış faturası vade tarihine hem de müşterinin ödeme düzenine ilişkin organizasyonun deneyimine dayalı olarak hesaplanır.

#### <a name="actual-cash-inflow"></a>Gerçek nakit girişi

Fiili içeri nakit akışı, tahmini temsil eder, ancak hesaplamalarınıza ilk fatura tarihinden itibaren başlayabilirsiniz. Aşağıda bir örnek verilmiştir:

-   **Fatura tarihi:** 2 Mart 2012.
-   **Vade tarihi:** 16 Mart 2012. Ödeme şartları 14 gün olarak ayarlanır.
-   **Beklenen satış ödeme tarihi:** 29 Mart 2012. Hesaplama üç genel tampon gün ve 10 ayrı tampon gün içerir.

#### <a name="cost-forecasting"></a>Maliyet tahmin etme

Tanımlanan günlere dayalı olarak, maliyet ödeme tarihi, proje tarihinden farklı olabilir. Bu durumda maliyet ödeme tarihi, proje tarihindeki tün sayısının ödeme süresindeki gün sayısına eklenmesiyle hesaplanır. 

Örneğin, hareketin proje tarihi 5 Mart 2012'dir ve ödeme süresi şu şekilde ayarlanmıştır:

-   **Saat:** Güncel ay (**M**)
-   **Giderler:** 14 gün (**D14**)
-   **Maddeler:** 30 gün (**D30**)

Bu ayarlara dayalı olarak, her bir hareket türü için maliyet ödeme tarihi şu şekildedir:

-   **Saat:** 31 Mart 2012, seçilen ayın son günüdür.
-   **Giderler:** 19 Mart 2012, hareket tarihinden 14 gün sonradır.
-   **Maddeler:** 4 Nisan 2012, hareket tarihinden 30 gün sonradır.

> [!NOTE] 
> Satınalma siparişinin vade tarihi, proje satınalma siparişi oluşturulduğundaki satıcı hareketine dayalıdır. Vade tarihi, varsayılan ayarlar tarafından belirlenmez. 

Maliyet ödeme tarihi tampon günlerine dayalı olarak hesaplanmaz. Bir proje tamamlandıktan sonra tüm maliyet çıkarma ve faturalandırma işlemleri tamamlandığında, hem maliyet hem de satışlar kar ve zarar hesaplarına nakledilir. 

Tüm satışlar ve satıcı faturaları tamamlandığında, **Nakit akışı** sayfasındaki alanlar ile **Proje ifadeleri** sayfasındaki alanlar arasındaki ilişkiyi görüntüleyebilirsiniz.

:::row::: :::column:::
        #### Cash flow page
        - Cash inflows 
        - Cash outflows
        - Net cash flows
    :::column-end:::
    :::column:::
        #### Project statements page
        - Revenue
        - Total cost
        - Gross margin
    :::column-end:::
:::row-end:::

### <a name="review-costs"></a>Maliyetleri gözden geçirme

Bir proje sırasında organizasyonunuzun üstlendiği maliyetleri **Maliyet kontrolü** sayfasından takip edebilirsiniz. Proje için orijinal bütçelenen maliyetler ile güncel fiili maliyetler ve taahhüt edilen maliyetler karşılaştırılarak, projenin yolunda gidip gitmediğini ve bütçenin altında veya üstünde kalıp kalmadığını belirleyebilirsiniz. 

> [!NOTE] 
> Proje maliyetlerinin geçerli durumunu görüntülemek için **Maliyet kontrolü** sayfasını kullanıyorsanız, orijinal ve kalan bütçe için seçilmiş tahmin modellerini kullanın. Maliyetleri hesaplarken diğer tahmin modellerini seçerseniz hesaplama sonuçları kesin olmayacaktır.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Kalan bütçelenmiş tutarları görüntüleme

**Proje yönetimi ve muhasebe parametreleri** sayfasında maliyet kontrol yöntemi olarak **Proje bütçesi** seçilirse **Maliyet kontrolü** sayfası, fiili olarak nakledilmemiş veya taahhüt edilmiş olarak işaretlenmemiş maliyetleri hesaplar. Özellikle, **Maliyet kontrolü** sayfasının alt panosundaki **Genel** sekmesindeki tutarlar şu şekilde hesaplanır:

-   **Fiili maliyet** – Seçilen maliyet satırı için projede harcanan toplam tutar. Fiili maliyet tutarı, **Defter güncellemeleri** sayfasında hesaplanır.
-   **Taahhüt edilen maliyet** – Tüzel kişiliğin kendisi ödemek üzere taahhüt ettiği giderlerin ilave tutarı. Özgün, tahmin edilen maliyet tutarları **Taahhüt edilen maliyetler** sayfasında hesaplanır.
-   **Kalan bütçe** – Orijinal bütçelenen tutar miktarı seçilen maliyet satırı için kalmaya devam ede.r Kalan bütçe tutarı **Genel muhasebe önizleme** sayfasında hesaplanır.
-   **Toplam maliyet** – Fiili maliyet, taahhüt edilen maliyet ve kalan bütçe tutarlarının toplamı.

**Maliyet kontrolü** sayfasında, **Sapma** semesinde toplam beklenen maliyet ile orijinal bütçenin bir karşılaştırmasını görüntüleyebilirsiniz. Bu karşılaştırma bu tutarlar arasındaki farkı gösterir. Böylece, verilerin eşleşmediği yerleri görebilirsiniz. Sapma tutarları aşağıdaki şekillerde hesaplanır:

-   **Orijinal bütçe** – Seçilen maliyet satırı için orijinal olarak bütçelenen tutar. Orijinal bütçe tutarı, **Genel muhasebe önizleme** sayfasında hesaplanır.
-   **Toplam maliyet** – **Genel** sekmesinde rapor edildiği şekilde fiili maliyet, taahhüt edilen maliyet ve kalan bütçenin toplamı.
-   **Sapma** – Toplam maliyet ile orijinal bütçe arasındaki fark.
-   **Tutara dayalı fark** – Orijinal tahmin ile toplam tahmin arasındaki toplam fark. Bu fark matematiksel olarak şu şekilde ifade edilebilir: (Orijinal tahmin miktarı) × (Orijinal ortalama fiyat – Toplam ortalama fiyat). Bu hesaplama sadece proje saatleri için geçerlidir.
-   **Fiyata dayalı fark** – Orijinal tahmin ile toplam tahmin arasındaki toplam fark. Bu fark matematiksel olarak şöyle ifade edilebilir: (Orijinal tahmin fiyatı) × (Orijinal tahmin miktarı – Toplam tahmin miktarı). Bu hesaplama sadece proje saatleri için geçerlidir.

#### <a name="viewing-the-total-budgeted-amounts"></a>Bütçelendirilen toplam tutarları görüntüleme

**Proje yönetimi ve muhasebe parametreleri** sayfasında maliyet kontrol yöntemi olarak **Toplam bütçe** seçilmişse **Maliyet kontrolü** sayfası, projenin fiili maliyetleri ile toplam maliyetleri hesaplayarak bu ikisi arasındaki farkı tespit etmenize yardımcı olur. Özellikle, **Maliyet kontrolü** sayfasında, **Genel** sekmesinin alt panosundaki sütunlardaki tutarlar şu şekilde hesaplanır:

-   **Toplam bütçelenen maliyet** – Seçilen maliyet satırı için toplam bütçelenen tutar.
-   **Fiili maliyet** – Projede seçilen maliyet satırlarının tarihine kadar üstlenilen maliyetlerin toplam tutarı.
-   **Taahhüt edilen maliyet** – Seçilen maliyet satırı için taahhüt edilmiş toplam tutar.
-   **Fark** – Gerçek ve taahhüt edilen maliyetlerin toplamı ile toplam maliyet arasındaki fark. Fark, ilave maliyetlerin toplam bütçe için belirtilmesinin gerekli olup olmadığını gösterir.

**Maliyet kontrolü** sayfasında **Sapma** sekmesinde, aşağıdaki alanlara bakarak toplam bütçe ile orijinal bütçe arasındaki farkı görüntüleyebilirsiniz:

-   **Orijinal bütçe**– Maliyet satırı için orijinal olarak bütçelenen tutar. Orijinal bütçe, **Genel muhasebe önizleme** sayfasında hesaplanır.
-   **Toplam bütçelenen maliyet** – Maliyet satırı için orijinal olarak bütçelenen toplam maliyet. Toplam bütçelenen maliyet, **Genel muhasebe önizleme** sayfasında hesaplanır.
-   **Sapma** – Maliyet satırı için sapma. Tutar, toplam maliyetin orijinal bütçeden çıkartılmasıyla hesaplanır.
-   **Tutara dayalı fark** – Orijinal bütçe ile toplam bütçe arasındaki toplam fark. Bu tutar, toplam bütçe saatlerinin orijinal bütçe saatlerinden çıkartılması ve ardından farkın orijinal olarak bütçelenen maliyet fiyatıyla çarpılmasıyla hesaplanır. Bu fark matematiksel olarak şu şekilde ifade edilir: (Orijinal olarak bütçelenen maliyet fiyatı) × (Orijinal bütçe saatleri – Toplam bütçe saatleri). Bu hesaplama sadece proje saatleri için geçerlidir.
-   **Fiyata dayalı fark** – Bu tutar, toplam bütçe saatlerini orijinal bütçe saatlerinden çıkarıp ardından aradaki farkı tüketilen toplam saat sayısıyla çarparak hesaplanır. Bu fark matematiksel olarak şu şekilde ifade edilir: (Toplam harcanan saatler) × (Orijinal bütçe saatleri – Toplam bütçe saatleri). Bu hesaplama sadece proje saatleri için geçerlidir.

### <a name="analyze-utilization"></a>Yararlanma analiz etme

Yararlanma oranı, belirli bir çalışma dönemi içinde bir çalışanın fatura edilebilir veya üretime yönelik çalışma gerçekleştirdiği zaman yüzdesini ifade eder. Fatura edilebilen saatler, çalışanın belirli bir müşteriye şarj edilebilecek çalışma saatleridir. 

Bir çalışanın yararlanma oranı belirli bir süre içinde fatura edilebilen saatlerin çalışma saatlerine bölünmesiyle hesaplanır. Örneğin, bir çalışan bir dönemde 30 saat fatura edilebilir iş yapmışsa ve aynı dönemde toplam çalışma saati 40 ise bu çalışanın yararlanma oranı yüzde 75'tir. 

Bir çalışan için yararlanma oranını hesaplarken, fatura edilebilir oranı veya üretkenlik oranını hesaplayabilirsiniz:

-   **Faturalanabilir oran** – Faturalanabilir saatler ve faturalanamayan saatler veya standart saatler arasındaki fark.
-   **Üretkenlik oranı** – Üretken saatler ile üretken olmayan saatler ve standart saatler arasındaki fark. Üretken saatler, çalışanın belirli bir projeye yönelik olarak çalıştığı saatlerdir. Üretken saatler, dahili projeler hariç olmak üzere tipik olarak müşterilere faturalandırılır Üretken olmayan saatler hiçbir zaman müşteriye fatura edilmez.

Yararlanma oranlarını **Saat kullanımı** sayfasında hesaplarsınız. Hesaplamalar varsayılan tercihlere dayalı olarak gerçekleştirilir. Bu tercihler ayrıca saatlerin her bir proje türüne **Yararlanma** veya **Yük** atanarak nasıl hesaplanacağını belirler. Bu da faturalandırılabilir oran hesaplamaları ve üretkenlik oranı hesaplamaları için geçerlidir.

-   **Yararlanma** – Seçili proje türü için raporlanan saatler daima faturalanabilir veya üretkenlik açısından yararlanabilir saatler kapsamında dikkate alınır.
-   **Yük** – Seçili proje türü için raporlanan saatler daima faturalanamayan veya üretkenlik açısından yararlanılmayan saatler kapsamında dikkate alınır.
-   **Satır özelliğine göre** – Belirli bir saat hareketinin satır özellikleri, saatlerin faturalanabilir veya üretkenlik açısından yararlanabilir saatler olup olmadığını belirler.
-   **Dahil edilmeyen** – Saatler, faturalanabilir veya üretkenlik açısından yararlanabilir saatler olarak dikkate alınmaz.

**Saat kullanımı** sayfasında, bir çalışan veya bir proje için genel yararlanma oranı yüzdesinin yanı sıra aşağıdaki saat türlerinin her biri için yararlanma oranı hesaplamaları için kullanılan saat sayılarını görebilirsiniz:

-   **Dahil edilmeyen saatler** – Bu saatler, saat kullanım oranına dahil edilmez.
-   **Dahil edilen saatler** – Bu saatler, yararlanma oranları ve yük saatleri eklenerek hesaplanır. Bu saatler yararlanma oranına dahili edilir.
-   **Yük saatleri** – Faturalandırılabilir oran hesaplanırken bu saatler, şarj edilemeyen saatler ile aynıdır. Bir üretkenlik oranı hesaplıyorsanız bu saatler üretken olmayan saatler ile aynıdır.
-   **Yararlanma saatleri** – Faturalanabilir oran hesabı yapılırken bu saatler şarj edilebilir saatler ile aynıdır. Bir üretkenlik oranı hesaplıyorsanız bu saatler üretken saatler ile aynıdır.

Bir çalışan için yararlanma oranını hesaplıyorsanız normal saatleri veya dahil edilebilen saatleri kullanabilirsiniz. Dahil edilen saatleri kullanıyorsanız çalışanların zaman çizelgesi dönemleri için tüm çalışma süresini dahil ettiğinden emin olmalısınız, çünkü hesaplama girilen saatlerin yüzdesi cinsinden ifade edilir. Bir proje, proje sözleşmesi, müşteri kaydı veya kategori için saat kullanım oranı hesaplanırken mutlaka hesaplamanız için dahil edilen saatleri kullanmalısınız.

### <a name="review-project-statements"></a>Proje bildirimlerini gözden geçirme

Bir projenin ilerleyişini hızlı şekilde görmek için bir proje bildirimi oluşturabilirsiniz. Bir proje bildirimi oluşturduğunuzda **Proje bildirimleri** sayfasındaki **Genel** sekmesinde seçimler yaparak bildirimin hesaplanmasında kullanılacak kriterleri belirleyebilirsiniz. Aşağıdaki bilgilerin eklenmesini veya çıkarılmasını seçebilirsiniz:

-   Proje tipleri
-   Hareket tipleri
-   Project tarihi/defter tarihi
-   Veriler

Bildirim hesaplandıktan sonra **Proje bildirimleri** sayfasının çeşitli sekmelerinde şu bilgileri görüntüleyebilirsiniz:

-   **Genel** – Projenin temel kar ve zarar yapısı hakkında genel bilgiler.
-   **Kar ve zarar** – Tahakkuk eden gelir hakkında bilgiler.
-   **Süren iş** – Süren işin hesap bakiyeleri hakkında bilgiler.
-   **Tüketim** – Saat, madde, gider ve bordro hareketleri tüketimi hakkında bilgiler.
-   **Fatura** – Faturalar ve açık hesap faturalandırma hakkında bilgiler.
-   **Saat oranı** – Gelir ve maliyet hesaplarına nakledilen saatler için saat oranları.

