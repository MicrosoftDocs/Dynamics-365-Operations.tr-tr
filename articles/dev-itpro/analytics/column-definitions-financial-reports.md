---
title: "Finansal raporlarda sütun tanımları"
description: "Bu makalede sütun tanımları hakkında bilgi verilmektedir. Bir sütun tanımı bir rapordaki sütunların içindekileri tanımlayan bir rapor bileşeni veya yapı taşıdır. Satır tanımları gibi, temel sütun tanımları da birden fazla raporda kullanılabilir."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 18ae41c3c1b19edc2d56a7e3480890c8aea28054
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="column-definitions-in-financial-reports"></a>Finansal raporlarda sütun tanımları

[!include [banner](../includes/banner.md)]

Bu makalede sütun tanımları hakkında bilgi verilmektedir. Bir sütun tanımı bir rapordaki sütunların içindekileri tanımlayan bir rapor bileşeni veya yapı taşıdır. Satır tanımları gibi, temel sütun tanımları da birden fazla raporda kullanılabilir.

<a name="create-and-modify-a-column-definition"></a>Bir sütun tanımı oluşturma ve değiştirme
-------------------------------------

Bir sütun tanımı iki ila 255 sütun içerebilir.

### <a name="create-a-column-definition"></a>Sütun tanımı oluşturma

1.  Rapor Tasarımcısı'ndaki gezinti bölmesinde **Sütun Tanımları**'na tıklayın.
2.  **Dosya** menüsünde, **Yeni**'ye ve ardından **Sütun Tanımı**'na tıklayın.
3.  Sütun tanımının içeriklerini ekleyin.

### <a name="open-a-column-definition"></a>Bir sütun tanımını açma

1.  Rapor Tasarımcısı'ndaki gezinti bölmesinde **Sütun Tanımları**'na tıklayın.
2.  Açmak için bir sütun tanımına çift tıklayın.

### <a name="add-a-column-to-a-column-definition"></a>Bir sütun tanımına sütun ekleme

1.  Rapor Tasarımcısı'nda, **Sütun Tanımları**'na tıklayın ve ardından değiştirilecek sütun tanımını açın.
2.  Yeni sütun eklenmesi gereken sütunu seçin.
3.  **Düzenle** menüsünde, **Sütun Ekle**'ye tıklayın. Yeni sütun, seçtiğiniz sütunun solunda görünür.

### <a name="delete-a-column-from-a-column-definition"></a>Bir sütun tanımından sütun silme

1.  Rapor Tasarımcısı'nda, **Sütun Tanımları**'na tıklayın ve ardından değiştirilecek sütun tanımını açın.
2.  Silinecek sütunu seçin.
3.  **Düzenle** menüsünde, **Sütunu Sil**'e tıklayın.

## <a name="contents-of-a-column-definition"></a>Bir sütun tanımının içerikleri
Bir sütun tanımı aşağıdaki bilgileri içerir:

-   Satır tanımının açıklamalarına ait bir sütun
-   Mali veriler, bir Microsoft Excel çalışma sayfası veya bir sütun tanımındaki diğer verileri esas alan hesaplamalara ait verileri gösteren tutar sütunları
-   Biçimlendirme sütunları
-   Öznitelik sütunları

Bu bilgiler sütun tanımındaki şu alanlarda görünür:

-   Sütun tanımının başlıklar alanı raporda görünen başlık metnini ve biçimlendirmesini içerir. Bir başlık tek bir veri sütununa uygulanabilir, birden fazla sütuna yayılabilir veya sütunlara koşula bağlı olarak uygulanabilir. Sütun tanımı ihtiyacınız olduğu kadar çok sütun başlığı satırı içerebilir. **Not:** Sütun başlıkları rapordaki verilerin her sütununa uygulanır. Rapor başlıkları ise tüm rapora uygulanır. Rapor tanımının **Üst Bilgiler ve Alt Bilgiler** sekmesinde rapor üst bilgilerini tanımlayabilirsiniz.
-   Sütun ayrıntısı satırları sütun tanımındaki üst bilgi satırlarının altındaki satırlardır. Sütun ayrıntısı satırları raporda yer alan bilgileri tanımlar. Aşağıdaki tabloda sütun ayrıntısı satırları belirtilip açıklanmaktadır.

    | Sütun ayrıntısı satırı adı                                                | Açıklama                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Sütun Türü                                                           | (Gerekli) Sütundaki veri türünü belirtin.                                                     |
    | Defter Kodu/Öznitelik Kategorisi                                          | **FD** ve **ATTR** türlerine ait sütunlar için mali veri bilgilerini belirtin.                       |
    | Kapsanan Mali Yıl Dönemi Sayısı                                    | **FD** türüne ait sütunlar için mali veri bilgilerini belirtin.                                     |
    | Formül                                                               | **CALC** türüne ait sütunlar hesaplama formülü belirtin.                                        |
    | Sütun Biçimi Geçersiz Kılma Yazdırma Denetiminden Önce Sütun Genişliği Fazladan Boşluk Sayısı | Özel biçim seçenekleri belirtin.                                                                        |
    | Sütun Kısıtlamaları                                                   | Verileri kısıtlayın.                                                                                         |
    | Raporlama Birimi                                                        | Sütunu yalnızca belirtilen raporlama birimine ait verileri gösterecek şekilde kısıtlayın.                      |
    | Para Birimi Ekranı Para Birimi Filtresi                                      | Para birimini biçimlendirin.                                                                                       |
    | Boyut Filtresi                                                      | Verileri belirli mali veri raporlama birimleriyle kısıtlamak için filtre belirtin.                           |
    | Öznitelik Filtresi                                                      | Mali verileri kısıtlamak için filtre belirtin.                                                       |
    | Başlangıç Tarihi Bitiş Tarihi                                                   | Mali verileri belirli tarihlerle kısıtlayın.                                                         |
    | Yaslama                                                         | Satır tanımında belirtilen açıklama metnini sola hizalayın, ortaya hizalayın veya sağa hizalayın. |

## <a name="column-restrictions-in-a-column-definition"></a>Bir sütun tanımındaki sütun kısıtlamaları
Bir sütun tanımının verileri nasıl kullandığını veya bilgileri nasıl hesapladığını belirtmek için sütun kısıtlamaları kullanabilirsiniz. Ayrıca bir rapor sütununu belirli bir birimle veya belirli tarihler için kısıtlayabilirsiniz. **Not:** Bir **Sütun Kısıtlaması** kodu satır tanımında atanan her türlü çakışan ayarı geçersiz kılar.

### <a name="column-restrictions-cell"></a>Sütun Kısıtlamaları hücresi

**Sütun Kısıtlamaları** hücresi söz konusu sütuna ait satır biçimlendirmesi, ayrıntılar ve tutarlar gibi bilgileri kısıtlayan veya gizleyen kodlar içerebilir.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Bir sütun tanımına sütun kısıtlaması ekleme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Kısıtlamak için sütunun **Sütun Kısıtlamaları** hücresine çift tıklayın.
3.  **Sütun Kısıtlamaları** iletişim kutusundaki listeden bir veya daha fazla kod seçin ve ardından **Tamam**'a tıklayın.

### <a name="column-restriction-codes"></a>Sütun kısıtlaması kodları

Aşağıdaki tabloda sütun kısıtlaması kodları açıklanmaktadır.

| Sütun kısıtlaması kodu | Açıklama                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SU                      | Satır tanımında bir alt çizgi komutunun (**---**) veya bir çift alt çizgi komutun (**===**) girildiği bir sütun için alt çizgiyi baskılayın. Örneğin, bir yüzde hesaplaması tarafından üretilen tutarları alt çizgili görüntülemek istemeyebilirsiniz.                                                                        |
| ST                      | Sütunda (örneğin bir istatistik sütunu) yalnızca ayrıntıların gösterilmesi için toplamları gizleyin.                                                                                                                                                                                                                                      |
| SD                      | Sütunda yalnızca **TOT** ve **CAL** satırlarının (satır tanımından) gösterilmesi için ayrıntıları gizleyin.                                                                                                                                                                                                                              |
| DR                      | Bir **FD** sütunundaki tutarları borç tutarlarıyla kısıtlayın.                                                                                                                                                                                                                                                                              |
| CR                      | Bir **FD** sütunundaki tutarları alacak tutarlarıyla kısıtlayın.                                                                                                                                                                                                                                                                             |
| ADJ                     | Sütundaki tutarları dönem düzeltmesi tutarları varsa bu tutarlarla kısıtlayın.                                                                                                                                                                                                                                        |
| XAD                     | Sütundaki tutarları dönem düzeltmesi tutarları hariç tutulacak şekilde kısıtlayın.                                                                                                                                                                                                                                                     |
| PT                      | Sütundaki tutarları deftere nakledilmiş hareketler kullanılabiliyorsa yalnızca bu hareketler dahil edilecek şekilde kısıtlayın.                                                                                                                                                                                                                 |
| UPT                     | Sütundaki tutarları deftere nakledilmemiş hareketler kullanılabiliyorsa yalnızca bu hareketler dahil edilecek şekilde kısıtlayın. **Not:** Tüm veri sağlayıcılar deftere nakledilmemiş hareketleri desteklemez. Daha fazla bilgi için, Microsoft Dynamics ERP sisteminizin [veri tümleştirme kılavuzuna](http://go.microsoft.com/fwlink/?LinkID=162565) bakın. |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Bir sütunu bir raporlama birimiyle kısıtlama

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Kısıtlamak için sütunun **Raporlama Birimi** hücresine çift tıklayın.
3.  **Raporlama Birimi Seçimi** iletişim kutusundaki **Raporlama ağacı** listesinden bir ağaç seçin.
4.  Birim listesini genişletin veya daraltın, bir raporlama birimi seçin ve ardından **Tamam**'a tıklayın.

## <a name="format-column-headers"></a>Biçim sütunu başlıkları
Bir rapordaki sütunların üst kısmında görünen başlıkları ekleyebilir, değiştirebilir ve silebilirsiniz. Ayrıca sütun tanımlarındaki **Dönem** alanın ve rapor tanımlarındaki **Esas Dönem** alanına göre koşullu yayılan sütun başlıkları da yapılandırabilirsiniz. Esas dönem özelliği toplanan tahmin raporları oluşturduğunuzda zaman kazanmanıza yardımcı olur.

### <a name="create-and-manage-column-headers"></a>Sütun başlıkları oluşturma ve yönetme

Bir rapordaki sütunların üst kısmında görünen başlıkları eklemek, değiştirmek ve silmek için **Sütun Başlığı** iletişim kutusunu kullanabilirsiniz. Aşağıdaki tabloda **Sütun Başlığı** iletişim kutusundaki alanlar açıklanmaktadır.

| Alan                 | Açıklama                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sütun başlığı metni    | Bu metin sütun başlığında görünür. Doğrudan bu alanın içine yazabilir ya da rapor her oluşturulduğunda sütun başlığını güncelleştiren bir seçenek seçmek için **Otomatik Metin Ekle**'ye tıklayabilirsiniz. Birden fazla otomatik metin kodu eklemek için **Otomatik Metin Ekle**'ye yeniden tıklayın ve ardından listedeki başka bir koda tıklayın. |
| Biçim seçenekleri        | Bir sütun başlığına kutu veya alt çizgi gibi biçimlendirme uygulayın.                                                                                                                                                                                                                                                           |
| Yayılma başlangıcı Yayılma bitişi | Başlık metninin uygulandığı sütunu veya sütunları tanımlayın.                                                                                                                                                                                                                                                            |
| Yaslama         | **Yayılma başlangıcı** ve **Yayılma bitişi** alanlarında belirtilen sütun veya sütun aralığı için sütun başlığı metninin nasıl hizalanması gerektiğini belirtin.                                                                                                                                                               |

### <a name="create-a-column-header"></a>Sütun başlığı oluşturma

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Bir başlık hücresine çift tıklayın.
3.  **Sütun Başlığı** iletişim kutusunda, sütun başlığı metnini girin. Alternatif olarak **Otomatik Metin Ekle**'ye tıklayın ve bir seçenek seçin.
4.  **Biçim seçenekleri** alanında, başlık için bir biçim seçin.
5.  **Yayılma başlangıcı** alanına, sütun başlığının başlaması gereken sütunun harfini girin. **Yayılma bitişi** alanına ise sütun başlığının bitmesi gereken sütunun harfini girin.
6.  **Yaslama**'nın altında, sütun başlığının sola mı, ortaya mı yoksa sağa mı yaslanmış olması gerektiğini belirtin.
7.  **Tamam** düğmesini tıklatın.

### <a name="add-a-column-header-row"></a>Sütun başlığı satırı ekleme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Başlık satırında bir hücre seçin.
3.  **Düzenle** menüsünde, **Satır Ekle**'ye tıklayın. Yeni satır, 2. adımda seçtiğiniz satırın üzerine eklenir. **Not:** Bir raporda dört ya da daha fazla rapor üstbilgisi satırına sahipseniz, üstbilgiler bir Excel çalışma sayfasına aktarıldığında üst üste binecektir. Rapordaki tüm başlıkları görüntülemek için, rapor tanımındaki üst boşluğu artırın.

### <a name="delete-a-column-header-row"></a>Bir sütun başlığı satırını silme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Başlık satırında, silinecek hücreyi seçin.
3.  **Düzenle** menüsündeki **Satır Sil** öğesini tıklayın.

### <a name="create-an-automatically-generated-header"></a>Otomatik üretilen bir üstbilgi oluşturma

Rapor tasarımcısı otomatik metin kodlarına göre otomatik olarak sütun başlıkları üretebilir. Otomatik metin kodları her rapor oluşturulduğunda güncelleştirilen değişkenlerdir. Her sütun başlığı tarihler ve dönem numaraları gibi değişebilen rapor bilgilerini belirtmek için bu kodları içerebilir. Bu nedenle, birden fazla rapor tanımı, süre ve raporlama ağacı için bir sütun tanımı kullanabilirsiniz. Otomatik metin kodları sütun tanımının ayrıntı satırlarındaki takvim bilgilerine dayandığından yalnızca <strong>CALC</strong>, <strong>FD</strong> ve <strong>WKS</strong> sütunları için desteklenir. Bir otomatik metin kodunun sütun başlığı hücresinde görünme şekli söz konusu bilgilerin raporda nasıl göründüğünü etkiler. <strong>Sütun Başlığı</strong> iletişim kutusunda, otomatik metin kodları büyük-küçük harf karışık olarak görünür. Bu nedenle, metin, raporda karışık şekilde görüntülenir. Örneğin, standart bir takvim yılı içinde <strong>@CalMonthLong</strong> öğesi <strong>7</strong> ile gösterilen ayı <strong>Temmuz</strong> olarak çözümler. Ay adının büyük olması (örneğin <strong>TEMMUZ</strong>) olması gerekiyorsa, <strong>Sütun üstbilgi metni</strong> alanına otomatik metin kodunu büyük harflerle girin. Örneğin: <strong>@CALMONTHLONG</strong> olarak girin. Kodları ve metinleri karıştırabilirsiniz. Örneğin, u üstbilgi metnini girin: <strong>Dönem @FiscalPeriod-@FiscalYear @StartDate - @EndDate.</strong> Oluşturulacak rapor üstbilgisi şu metni üretir: <strong>01/01/02 tarihinden 01/31/02 tarihine kadar 1-02 Dönemi</strong>. <strong>Not:</strong> Uzun tarih vb. gibi bazı metin biçimleri Finance and Operations sunucunuzdaki bölgesel ayarlarınıza bağlıdır. Bu ayarları değiştirmek için <strong>Başlat</strong> düğmesini, <strong>Denetim Masası</strong> öğesini ve ardından <strong>Bölge ve Dil</strong> öğesini tıklayın. Aşağıdaki tabloda sütun üstbilgileri için kullanılabilen otomatik metin seçenekleri listelenmiştir.


|        Otomatik metin seçeneği ve kodu         |                                                                                                                                           Açıklama                                                                                                                                            |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       Ay adı (@CalMonthLong)        | Mevcut ayın adını sütun üstbilgisinde yazdırın. Rapordaki tutarları binler, milyonlar veya milyarlar olarak yuvarlamaya karar verdiğinizde ve rapordaki sütun genişliğini dokuz karakterden kısa olarak ayarladığınızda ayın adı, ilk üç karakteri gözükecek şekilde kısaltılır. |
| Kısaltılmış ay adı (@CalMonthShort) |                                                                                                             Seçilen mali dönem için ayın kısaltılmış adını yazdırın.                                                                                                              |
|      Dönem numarası (@FiscalPeriod)      |                                                                  İlgili sütun için tanımlanan mali dönemin sayısını yazdırın. Sütun birden fazla dönemi kapsıyorsa aralıktaki son dönem yazdırılır.                                                                  |
| Dönem açıklaması (@FiscalPeriodName)  |                                                                                                          Mali verilerde açıklanan mali dönem açıklamasını yazdırın.                                                                                                           |
|        Mali yılı (@FiscalYear)        |                                                                                                                      Sütun için mali yılı sayısal formatta yazdırın.                                                                                                                       |
|        Takvim yılı (@CalYear)         |                                                                                                                     Sütun için takvim yılını sayısal formatta yazdırın.                                                                                                                      |
|         Başlangıç tarihi (@StartDate)         |                                                                                                                               Sütun için başlangıç tarihini yazdırın.                                                                                                                               |
|           Bitiş Tarihi (@EndDate)           |                                                                                                                                Sütun için bitiş tarihini yazdırın.                                                                                                                                |
|     Ağaçtan birim adı (@UnitName)     |                                                                                           Bir sütunu raporlama ağacının belirli bir birimiyle sınırlandırırsanız birim adını sütun üstbilgisinde yazdırın.                                                                                           |
|      Birim açıklama (@UnitDesc)       |                                                                                       Bir sütunu raporlama ağacının belirli bir birimiyle sınırlandırırsanız birim açıklamasını sütun üstbilgisinde yazdırın.                                                                                        |
|          Defter Kodu (@BookCode)          |                                                                                                                       Sütunda tanımlanan defter kodunu yazdırın.                                                                                                                       |
|           Boş satır (@Blank)           |                                                                                                                            Sütun başlığına boş bir satır ekleyin.                                                                                                                            |

### <a name="create-a-conditional-spanning-header"></a>Koşullu genişleyen bir üstbilgi oluşturma

Koşullu kapsayıcı üst bilgiler belirli dönem verilerini esas alan birden fazla sütuna yayılabilir. Örneğin, mali yıl için bir bütçe raporunuz varsa ve gelecek ayların öngörülen bütçeleriyle birlikte geçmiş ayların gerçek bütçelerini görüntülemek istiyorsanız rapor başlığını otomatik olarak güncelleştirmek için bir koşullu kapsayıcı üst bilgi kullanabilirsiniz. Koşullu kapsayıcı üst bilgi oluşturduğunuzda aşağıdaki durumlara dikkat edin:

-   Bir başlangıç koşulundan (**Yayılma başlangıcı** alanı) önce eşleşen herhangi bir koşul (**Yayılma bitişi** alanı) yok sayılır. Örneğin, B sütunu BASE+1 ila BASE olarak tanımlanan yayılma koşuluna sahiptir, BASE C sütununda, BASE+1 ise D sütunundadır. Bu durumda, C sütunundaki durma koşulu yok sayılır ve başlığın yazdırılması D sütununda başlatılır.
-   Çakışan sütun başlıkları belirtirseniz bu başlıklar raporda yazdırıldıklarında çakışır. Rapor oluşturulur, ancak aşağıdaki uyarı **Rapor Sıra Durumu** alanında görüntülenir: "Diğer sütun başlıklarıyla kesişen, taban kesişimi kullanan sütun başlıkları üst üste gelen metine sebep olabilir." Örneğin, sütun B üzerindeki başlık tanımı B eşittir B'den TEMEL +1'edir ve sütun D üzerindeki başlık tanımı TEMEL+1'den F'yedir. Bu durumda, başlıklar birbirlerinin üstüne yazılır ve okunamaz durumda olurlar. BASE **Yayılma başlangıcı/Yayılma bitişi** tanımında her kullanıldığında, başlıkların çakışıp çakışmadığını görmek için mutlaka oluşturulan raporu görüntüleyin.
-   Yayılma tanımındaki BASE'i bir Yazdırma (**NP**) sütununda belirtirseniz sütun tanımında belirtilenlerden bağımsız olarak yok sayılır. Temel olarak, bu senaryo bir sütun üstbilgi tanımının oluşturulmamasıyla aynıdır.
-   Koşullu yazdırma sütunları (**P&lt;B,** **P&gt;=B**) için koşullu genişleyen üstbilgiler herhangi bir normal sütun üstbilgi tanımı gibi davranır. Örneğin, koşul yanlışsa yayılma koşulu için eşleşen sonraki herhangi bir sütun başlığın yazdırılmasını başlatır.

#### <a name="create-a-conditional-spanning-header"></a>Koşullu kapsayıcı üst bilgi oluşturma

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Bir başlık hücresine çift tıklayın.
3.  **Sütun Başlığı** iletişim kutusunda, sütun başlığı metnini girin. Alternatif olarak **Otomatik Metin Ekle**'ye tıklayın ve bir seçenek seçin.
4.   **Biçim seçenekleri** alanında, başlık için bir biçimlendirme stili seçin.
5.  Rapor oluşturulurken belirtilen esas dönemle ilgili bir dönem belirtin. **Yayılma başlangıcı** ve **Yayılma bitişi** alanlarına şu değerlerden birini girin: **BASE**, **BASE-X** veya **BASE+X**. Burada X esas dönemden itibaren dönem sayısıdır. Örneğin, **Yayılma başlangıcı** alanına **BASE** ifadesini girerseniz koşullu kapsayıcı sütun üst bilgisi metni rapor tanımının **Esas dönem** değeri sütun tanımının **Dönem** değerine eşit olduğunda sütun başlığında başlar. **Yayılma bitişi** alanında belirtilen sütunda biter. Bu nedenle yayılma BASE ila M ise rapor tanımının **Esas dönem** değeri **4**'tür, başlık dönemin **4** olarak ayarlandığı durumlarda sütunda başlar ve M sütununda biter. Başlıklar yalnızca yazdırma sütunlarında durur ve başlar.
6.  **Yaslama**'nın altında, sütun başlığının sola mı, ortaya mı yoksa sağa mı yaslanmış olması gerektiğini belirtin.
7.  **Tamam** düğmesini tıklatın.

#### <a name="example-of-a-conditional-spanning-header"></a>Koşullu kapsayıcı üst bilgi örneği

Pelin dinamik bir altı aylık tahmin için bir rapor oluşturuyor. Gerçek verileri içeren sütunların üzerine "Gerçek durum" ifadesinin, bütçe tahminlerini içeren sütunların üzerine ise "Bütçe" ifadesinin yazdırılmasını istiyor. Raporun çalıştırıldığı her ay, bir fazla gerçek durum sütunu ve bir az bütçe sütunu vardır. Pelin başlıkları ayarlamak için sütun tanımını rapor her oluşturulduğunda el ile değiştirebilse de, zamandan ve çabadan tasarruf etmek için rapor her çalıştırıldığında ilgili sütunların üzerinde otomatik olarak başlık oluşturacak koşullu kapsayıcı üst bilgiler oluşturmaya karar veriyor. Pelin Rapor Tasarımcısı'nı açıyor, gezinme bölmesindeki **Sütun Tanımı**'na tıklıyor ve raporun sütun tanımını açıyor. Ardından aşağıdaki bilgileri giriyor. Rapor tanımındaki temel dönem 4'tür.


|                     |  A:   |       B:       |       A       |       B       |       E:       |       C       |       G:       |       H:       |       I:       |       J       |       K       |       L       |       P       |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
|      Üstbilgi 1       |      |    Gerçek     |    Bütçe     |               |               |               |               |               |               |               |               |               |               |
|      Üstbilgi 2       |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
|      Başlık 3       |      |               |               |               |               |               |               |               |               |               |               |               |               |
|     Sütun Tipi     | DESC |      FD       |      FD       |      FD       |      FD       |      FD       |      FD       |      FD       |      FD       |      FD       |      FD       |      FD       |      FD       |
| Defter Kodu/Öznitelik |      |    ACTUAL     |  BUDGET2012   |    ACTUAL     |  BUDGET2012   |    ACTUAL     |  BUDGET2012   |    ACTUAL     |  BUDGET2012   |    ACTUAL     |  BUDGET2012   |    ACTUAL     |  BUDGET2012   |
|     Mali Yıl     |      |     BASE      |     BASE      |     BASE      |     BASE      |     BASE      |     BASE      |     BASE      |     BASE      |     BASE      |     BASE      |     BASE      |     BASE      |
|       Dönem        |      |       1       |       1       |       2       |       2       |       3       |       3       |       4       |       4       |       5       |       5       |       6       |       6       |
|   Kapsanan Dönemler   |      |   PERIODIC    |   PERIODIC    |   PERIODIC    |   PERIODIC    |   PERIODIC    |   PERIODIC    |   PERIODIC    |   PERIODIC    |   PERIODIC    |   PERIODIC    |   PERIODIC    |   PERIODIC    |
|    Sütun Genişliği     |  30  |      10       |      10       |      10       |      10       |      10       |      10       |      10       |      10       |      10       |      10       |      10       |      10       |
|    Yazdırma Kontrolü    |      |    P&lt;=B    |    P&gt;B     |    P&lt;=B    |    P&gt;B     |    P&lt;=B    |    P&gt;B     |    P&lt;=B    |    P&gt;B     |    P&lt;=B    |    P&gt;B     |    P&lt;=B    |    P&gt;B     |

Phyllis, **Sütun Üstbilgisi** iletişim kutusunu açmak üzere bir sütun üstbilgi hücresini çift tıklıyor ve buraya aşağıdaki bilgileri giriyor.

| Alan              | Değer                 |
|--------------------|-----------------------|
| Sütun başlığı metni | Gerçek Durum                |
| Otomatik Metin Ekle    | Seçim yapılmadı. |
| Biçim seçenekleri     | Kutu                   |
| Yaslama      | Seçim yapılmadı. |
| Yayılma başlangıcı        | B                     |
| Yayılma bitişi          | BASE                  |
| Bütçe başlığı      | BASE+1 ila bitiş sütunu  |

Pelin bilgileri girmeyi tamamladıktan sonra **Tamam**'a tıklıyor. Ardından aşağıdaki bilgileri girdiği **Sütun Başlığı** iletişim kutusunu açmak için C sütunundaki sütun başlığı hücresine çift tıklıyor.

| Alan              | Değer                 |
|--------------------|-----------------------|
| Sütun başlığı metni | Bütçe                |
| Otomatik Metin Ekle    | Seçim yapılmadı. |
| Biçim seçenekleri     | Kutu                   |
| Yaslama      | Seçim yapılmadı. |
| Yayılma başlangıcı        | C                     |
| Yayılma bitişi          | BASE+2                |

Artık bu rapor her oluşturulduğunda, gerçek verileri içeren sütunların üzerine "Gerçek durum" ifadesi, bütçe tahminlerini içeren sütunların üzerine ise "Bütçe" ifadesi yazdırılacaktır. Ayrıca, her ay sütunların sayısı ayarlanacaktır.

## <a name="apply-column-justification"></a>Sütun yaslama uygulama
Bir rapordaki açıklama sütununa yaslama biçimlendirmesi uygulamak için **Yaslama** hücresi kullanılır. Bu seçenek gerçek değerleri değil yalnızca sütun açıklamalarını etkiler.

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  **Yaslama** hücresine çift tıklayın.
3.  Listeden aşağıdaki değerlerden birini seçin:
    -   **Yok**: Yaslama uygulanmaz.
    -   **Sol**: Sütun açıklamalarını sola hizalayın.
    -   **Orta**: Sütun açıklamalarını ortaya hizalayın.
    -   **Sağ**: Sütun açıklamalarını sağa hizalayın.

## <a name="add-special-formatting-options"></a>Özel biçimlendirme seçenekleri ekleme
Sütun tanımında, biçimlendirme sütunu ayrıntı satırları seçilen sütunlara özel biçimlendirme uygular. Bazı **Yazdırma Denetimi** seçenekleri ve **Sütun Kısıtlamaları** seçenekleri **FD** sütunlarına özel olsa da seçeneklerin çoğu tüm sütun türleri için geçerlidir. Sütun tanımında belirtilen biçimlendirme rapor tanımında belirtilen biçimlendirmeyi geçersiz kılar. Ancak, satır tanımında belirtilen biçimlendirme sütun tanımında belirtilen biçimlendirmeyi geçersiz kılar. Aşağıdaki satırlar biçimlendirme satırları olarak değerlendirilir:

-   Sütun Genişliği
-   Sütundan Önceki Fazladan Boşluklar
-   Biçim/Para Birimi Geçersiz Kılma
-   Yazdırma Denetimi

### <a name="changing-the-column-width"></a>Sütun genişliğini değiştirme

**Sütun Genişliği** hücresi yazdırılan raporda bu sütunun genişliği için kullanılacak karakter sayısını belirtir. Sütun genişliği tutar (**CALC**, **WKS** veya **FD** türü sütunlar), açıklama (**DESC** türü sütunlar) veya dolgu (**FILL** türü sütunlar) içeren sütunlar için önemlidir. Varsayılan olarak **Otomatik Sığdır** seçeneği seçilidir, böylece her sütunun genişliği otomatik olarak içeriklere uyacak şekilde ayarlanır.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Bir rapordaki bir sütunun genişliğini belirtme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  **Sütun Genişliği** sütunun genişliği için boşluk sayını girin. Herhangi bir sütunun maksimum genişliği 255 karakterdir (Bu rakama kuruşlar, virgüller ve parantezler dahildir). Alternatif olarak, sütun için hücre içeriğine göre uygun genişliği seçmek üzere rapor tasarımcısını etkinleştirmek için **Sütun Genişliği** hücresini çift tıklayın ve ardından **Otomatik Sığdırma** öğesini seçin.

### <a name="add-space-between-columns"></a>Sütunların arasına boşluk ekleme

**Sütundan Önceki Fazladan Boşluklar** sütun tanımındaki bir sütun ile bitişik sütunlar arasındaki ayırıcının genişliğini belirtir. **Sütundan Önceki Fazladan Boşluklar** ayarı sütun için tüm sütun ayrıntısı satırlarını etkiler, ancak sütun başlığı satırlarını etkilemez. Sütun gruplarını ayırmak veya açıklamadan önce birkaç boşluk eklemek için bu seçeneği kullanın, böylece açıklama sütunu rapordaki sola hizalanmış başlıklardan itibaren girintilendirilir. Her sütun arasındaki varsayılan boşluk sayısı ikidir. Bu ayarı rapor tanımındaki **Ayarlar** sekmesinde değiştirebilirsiniz.

#### <a name="specify-the-space-between-columns"></a>Sütunların arasındaki boşluğu belirtme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  **Sütundan Önceki Fazladan Boşluklar** hücresine sütunlar arasına girilecek boşluk sayısını girin.

### <a name="specify-a-currency"></a>Para birimi belirtme

**Biçim/Para Birimi Geçersiz Kılma** hücresi sütundaki ondalık, para birimi ve yüzde tutarlarının biçimlendirmesini belirtir. Bu biçimlendirme rapor tanımında veya sistem varsayılanlarında belirtilen her türlü biçimlendirmeyi geçersiz kılar.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Bir rapor sütununa biçim para birimi geçersiz kılma işlemi atama

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Bir tutar sütunundaki bir **Biçim/Para Birimi Geçersiz Kalma** hücresine çift tıklayın.
3.  **Biçim Geçersiz Kılma** iletişim kutusunda, biçimlendirme seçeneklerini seçin.

### <a name="add-a-print-control-code"></a>Yazdırma denetimi kodu ekleme

**Yazdırma Denetimi** hücresi bir sütunun görüntüleme veya yazdırma özelliklerini ayarlayan kodlar içerebilir. İki tür yazdırma denetimi kodu vardır: normal yazdırma denetimi kodları ve koşullu yazdırma kontrol kodları.

#### <a name="regular-print-control-codes"></a>Normal yazdırma denetimi kodları

| Yazdırma denetimi kodu | Çeviri                                     | Açıklama                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Yazdırılmayan                                     | Yazdırılan rapordaki ve hesaplamalardaki tutarları bu sütunda hariç tutun. Bir hesaplamaya yazdırılmayan bir sütun eklemek için, doğrudan hesaplama formülündeki sütuna bakın. Örneğin, şu hesaplamaya yazdırılmayan C sütunu dahil edilmiştir: **B+C+D**. Ancak, şu hesaplamaya yazdırılmayan C sütunu dahil edilmemiştir: **B:D**.                                                                                                                                          |
| XCR                | Normal satır bakiyesi alacaksa işareti değiştir | Her türlü istenmeyen varyansın (gelir açığı veya gider aşımı gibi) her zaman negatif olduğu durumlarda bir bütçe veya karşılaştırma raporu oluşturun. Belirli bir satırın normal bakiyesi alacaksa (satır tanımının **Normal Bakiye** sütununda **C** ile tanımlanan) sütun tutarının işaretini ters çevirmek için bu kodu bir **CALC** sütununa uygulayın. **Not:** Normalde bir alacak bakiyesi içeren **TOT** satırları ile **CAL** satırları için satır tanımındaki **Normal Bakiye** sütununa mutlaka bir **C** girin. |
| X0                 | Tümü sıfırsa veya boşsa sütunu gizle          | Bir **FD** sütununu bu sütundaki tüm hücreler boşsa veya sıfır içeriyorsa rapordan çıkarın.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SR                 | Yuvarlamayı gizle                               | Bu sütundaki tutarların yuvarlanmasını engelleyin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| XR                 | Toplamayı gizle                                 | Bir toplamayı gizleyin. Raporda bir raporlama ağacı kullanılıyorsa bu sütundaki tutarlar sonraki üst düğümlerde toplanmaz.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RP                 | Sütunu her sayfada yinele                      | Belirtilen bir sütunu bir raporun her sayfasında tekrarlayın. Örneğin, her sayfadaki satır kodlarını alan **ROW** türü bir sütun eklemek için **RP** yazdırma denetimi kodunu kullanabilirsiniz.                                                                                                                                                                                                                                                                                                                                           |
| WT                 |  Metni kaydır                                      |  Bir sütundaki metin boşluğa sığmayacak kadar uzunsa tüm metni sütunda tutmak için metni kaydırın.                                                                                                                                                                                                                                                                                                                                                                                                                            |

#### <a name="conditional-print-control-codes"></a>Koşullu yazdırma kontrol kodları

| Koşullu yazdırma kontrol kodu | Açıklama                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (yok)                         | Koşullu yazdırma seçimini temizler.                                                  |
| P&lt;B                         | Belirtilen sütun sadece dönem, temel dönemden kısa ise görüntüler.             |
| P&gt;B                         | Belirtilen sütun sadece dönem, temel dönemden uzun ise görüntüler.             |
| P=B                            | Belirtilen sütun sadece dönem, temel döneme eşit ise görüntüler.              |
| P&lt;=B                        | Belirtilen sütun sadece dönem, temel döneme eşit veya daha kısa ise görüntüler. |
| P&gt;=B                        | Belirtilen sütun sadece dönem, temel döneme eşit veya daha uzun ise görüntüler. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Bir rapor sütununa yazdırma denetimi kodları ekleme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  **Yazdırma Denetimi** hücresine çift tıklayın.
3.  **Yazdırma Denetimi** iletişim kutusundaki **Yazdırma denetimi seçeneklerini seç** listesinden bir kod seçin. Birden fazla kod seçmek için, kodları seçerken Ctrl tuşunu basılı tutun.
4.  **Koşullu yazdırma seçenekleri** alanında bir seçenek seçin. Varsayılan olarak, **(yok)** seçilidir. Aynı anda sadece bir koşullu yazdırma kodu seçebilirsiniz.
5.  **Tamam** seçeneğini tıklatın.

> [!TIP]
> Ayrıca, yazdırma kontrol kodlarını doğrudan **Yazdırma Kontrol** hücresine de girebilirsiniz. Birden fazla yazdırma denetimi kodunu virgülle ayırın.


## <a name="column-types"></a>Sütun türleri
Bir rapordaki her sütunun içerdiği bilgi türü, sütun tanımındaki **Sütun Türü** satırındaki değerle belirtilir. Her sütun tanımı en az bir açıklama (**DESC**) sütunu ve bir tutar (**FD**, **WKS** veya **CALC**) sütunu içermelidir. **Not:** Sütun türü kodları tüm muhasebe sistemlerinde geçerli değildir. Muhasebe sisteminiz için geçerli olmayan bir tür seçerseniz söz konusu sütun raporda boş olur.

### <a name="specify-a-column-type"></a>Sütun türü belirtme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  İlgili sütunda, **Sütun Türü** satırındaki bir hücreye çift tıklayın.
3.  Listeden bir sütun türü seçin. Aşağıdaki tabloda çeşitli sütun türleri açıklanmaktadır.
    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Sütun türü kodu</th>
    <th>Açıklama</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>FD</td>
    <td>Satır tanımında bir <strong>Mali Boyutlarla İlişkilendir</strong> sütunu veya bir <strong>Çalışma Sayfası Bağlantısı</strong> sütunu kullandığınızda, bir Excel çalışma sayfasındaki mali verileri veya verileri görüntüleyin. <strong>FD</strong> sütun türünü seçtiğinizde, aşağıdaki satırlar için varsayılan ayarlar otomatik olarak belirtilir: <ul>
    <li><strong>Defter Kodu/Öznitelik Kategorisi:</strong> ACTUAL</li>
    <li><strong>Defter Kodu/Öznitelik Kategorisi:</strong> ACTUAL</li>
    <li><strong>Mali Yıl:</strong> BASE</li>
    <li><strong>Dönem:</strong> BASE</li>
    <li><strong>Kapsanan Dönemler:</strong> PERIODIC</li>
    <li><strong>Sütun Genişliği:</strong> 14</li>
    </ul>
Bu varsayılan ayarları değiştirebilirsiniz.</td>
    </tr>
    <tr class="even">
    <td>CALC</td>
    <td><strong>Formül</strong> hücresinde belirtilen basit veya karmaşık bir hesaplamanın sonucunu gösterir. Daha fazla bilgi için bkz. <a href="advanced-formatting-options-financial-reporting.md">Finansal raporlamadaki Gelişmiş biçimlendirme seçenekleri</a>.</td>
    </tr>
    <tr class="odd">
    <td>DESC</td>
    <td>Satır tanımında satır açıklamasını gösterir. Açıklama sütunu genellikle rapordaki ilk sütun olduğu halde, herhangi bir konumda olabilir.</td>
    </tr>
    <tr class="even">
    <td>ROW</td>
    <td>Satır tanımındaki <strong>Satır Kod</strong> sütunundaki mali satırlar için ayrı satır kodlarını gösterir. Daha fazla bilgi için bkz. <a href="row-definitions-financial-reporting.md">Finansal raporlamadaki satır tanımları</a>.</td>
    </tr>
    <tr class="odd">
    <td>ACCT (Hesap kodları)</td>
    <td>Her bir satıra uygulanan mali veri segment değerlerini veya boyut değerlerini gösterir. Hesap ve hareket ayrıntısı raporları için, tamamen uygun bir hesap yazdırılır (örneğin, <strong>110140-070-0101</strong>). İlişkili bir satır tanımındaki <strong>Mali Boyutlarla İlişkilendir</strong> sütununda aralıklar belirtildiyse aralık köşeli parantez içine alınır ve tek bir değer olarak işlem görür (örneğin, <strong>[110140:110700]-070-[0101:0200]</strong>). Birkaç hesabın birleşimi olan mali raporlar ve üst düzey raporlar için, satır tanımındaki mali veri bağlantısı yazdırılır (örneğin, <strong>1100:1200</strong>).</td>
    </tr>
    <tr class="even">
    <td>FILL</td>
    <td>Hücreyi tek tırnak işaretleri arasına aldığınız bir karakterle doldurun. Bir karakter girmezseniz sütun boş olur. Örneğin, bir sütunu üç nokta işaretiyle (...) doldurmak için <strong>FILL</strong> <strong>'.'</strong> ifadesini girin.</td>
    </tr>
    <tr class="odd">
    <td>PAGE</td>
    <td>Rapora dikey bir sayfa sonu ekleyin. <strong>PAGE</strong> sütununun sağındaki sütunlar farklı bir sayfada görünür.</td>
    </tr>
    <tr class="even">
    <td>WKS</td>
    <td>Bir Excel çalışma sayfasından alınan verileri görüntüleyin. <strong>WKS</strong> sütun türünü seçtiğinizde, aşağıdaki satırlar için varsayılan ayarlar otomatik olarak belirtilir: <ul>
    <li><strong>Mali Yıl:</strong> PERIODIC</li>
    <li><strong>Dönem:</strong> BASE</li>
    </ul>
Bu varsayılan ayarları değiştirebilirsiniz.</td>
    </tr>
    <tr class="odd">
    <td>ATTR</td>
    <td>Muhasebe sisteminiz öznitelikleri destekliyorsa sütundaki bir hesap veya hareket özniteliğini görüntüleyin. Tek bir tam hesap için geçerli olması gereken bir öznitelik alttaki hesap veya hareket bilgilerini mali verilerden ayıklar. Hesap düzeyi öznitelikler hesaptaki verileri görüntülerken, hareket düzeyi öznitelikler hareketin deftere nakledildiği zaman oluşan verileri görüntüler. Sütun türü olarak <strong>ATTR</strong>'yi seçerseniz sütun tanımının <strong>Defter Kodu/Öznitelik Kategorisi</strong> ayrıntı satırında öznitelik kategorisini belirtin.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Mali Boyutlar sütunu

Aşağıdaki **Sütun Tanımı** satır tanımları **FD** (Mali boyutlardaki tutarlar) sütun türüne sahip sütunlara uygulanır.

#### <a name="book-codeattribute-category-cell"></a>Defter Kodu/Öznitelik Kategorisi hücresi

**Defter Kodu/Öznitelik Kategorisi** hücresi **FD** sütunundaki veriler için defter kodunu tanımlar. Bir sütun tanımı birden fazla gerçek durum, bütçe ve istatistik sütununu içerebilir. Ayrıca, bir sütun tanımı cari veya yılından beri gibi farklı dönemleri ve farklı tutarları da görüntüleyebilir. Defter kodları listesi mali verilerinizde belirlenen gerçek durum, bütçe ve istatistik (mali olmayan) seçeneklerini yansıtır.

#### <a name="fiscal-year-cell"></a>Mali Yıl hücresi

**Mali Yıl** hücresi sütunun içermesi gereken mali yılı tanımlar. Yıl, rapor oluşturulurken belirtilen esas yılla ilgili olabilir. Aşağıdaki seçenekler kullanılabilir.

| Seçenek  | Açıklama                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| TEMEL    | Rapor zamanında belirtilen temel yıl kullanılır.                                                                          |
| TEMEL+\# | Temel yıldan \# yıl sonraki yıl kullanılır. Örneğin, temel yıldan sonraki üçüncü yılı kullanmak istiyorsanız **TEMEL+3** girin. |
| TEMEL\# | Temel yıldan \# yıl önceki yıl kullanılır. Örneğin, geçen yılı kullanmak için **TEMEL-1** girin.                 |
| \#      | Fiili mali yılı girin.                                                                                                |

#### <a name="period-cell"></a>Dönem hücresi

**Dönem** hücresi, sütunun içermesi gereken mali dönemleri tanımlar. Dönem rapor oluşturulurken belirtilen esas dönemle ilgili olabilir. Aşağıdaki seçenekler mevcuttur.

| Seçenek          | Açıklama                                                                                                                                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TEMEL            | Temel dönem kullanılır.                                                                                                                                                                                                                 |
| TEMEL+\#         | Temel dönemden \# dönem sonraki dönem kullanılır. Örneğin, temel dönemden sonraki üçüncü dönemi kullanmak istiyorsanız **TEMEL+3** girin.                                                                                               |
| TEMEL\#         | Temel dönemden \# dönem önceki dönem kullanılır. Örneğin, geçen dönemi kullanmak için **TEMEL-1** girin.                                                                                                                 |
| TEMEL\#:TEMEL    | Temel dönemden önceki birkaç dönemden temel döneme kadar, birden fazla dönem kullanılır. Örneğin, önceki üç dönemi ve temel dönemi kullanmak için **TEMEL-3:TEMEL** girin.                                                |
| TEMEL:TEMEL+\#    | Temel dönemden temel dönemden sonraki birkaç döneme kadar, birden fazla dönem kullanılır. Örneğin, temel dönemi ve sonraki iki dönemi kullanmak için **TEMEL:TEMEL+2** girin.                                                  |
| TEMEL-\#:TEMEL+\# | Temel dönemden önceki birkaç dönemden temel dönemden sonraki birkaç döneme kadar, birden fazla dönem kullanılır. Örneğin, önceki üç dönem, esas dönem ve sonraki iki dönemi kullanmak için, **BASE-3:BASE+2** ifadesini girin. |
| 1:BASE          | İlk dönemden temel döneme kadar, birden fazla dönem kullanılır.                                                                                                                                                                 |
| \#              | Her zaman belirli bir dönem numarası kullan. Sütun tanımının esnekliğini azalttığından bu seçeneği kullanmanızı önermiyoruz.                                                                                       |
| \#:\#           | Her zaman belirli bir dönem aralığı kullan. Sütun tanımının esnekliğini azalttığından bu seçeneği kullanmanızı önermiyoruz.                                                                                    |

Dönem özelliklerinin herhangi birinde mali yıl sınırlarının ötesine geçebilirsiniz ve yılları bir dönem aralığında karıştırabilirsiniz. Örneğin dönemi **TEMEL-5** (son altı ayı temsil etmek için) olarak belirtin ve temel dönemi 2 olan bir rapor çalıştırın. Bu durumda, rapor belirtilen mali yılın ilk iki dönemi ve önceki mali yılın son dört dönemi için verileri gösterir.

### <a name="specify-the-periods-for-an-fd-column"></a>Bir FD sütunu için dönemleri belirtme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Bir **FD** sütununda, **Dönem** satırındaki hücreye çift tıklayın ve ardından listeden bir seçenek seçin.
3.  Gezinme çubuğunun üzerindeki formül çubuğunda veya **Dönem** hücresinde, formülü tamamlayın. Varsa, sayı işaretlerini (\#) uygun değerle değiştirin.

#### <a name="periods-covered-cell"></a>Kapsanan Dönemler hücresi

**Kapsanan Dönemler** hücresi, sütunun görüntülemesi gereken tutarı tanımlar. Bu tutar sütuna ait **Mali Yıl** ve **Dönem** hücrelerindeki değerle ilgilidir. Aşağıdaki seçenekler kullanılabilir.

| Seçenek      | Açıklama                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODIC    | Geçerli dönem veya dönem aralığı için faaliyet toplamını görüntüler. |
| PERIODIC/BB | Geçerli dönem veya dönem aralığı için başlangıç bakiyesini görüntüler.   |
| YTD         | Yılın başından beri olan faaliyetin toplamını görüntüler.                               |
| YTD/BB      | Yılın başlangıç bakiyesini görüntüler.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Bir FD sütunu için kapsanan dönemleri belirtme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Bir **FD** sütununda, **Kapsanan Dönemler** satırındaki hücreye çift tıklayın ve ardından listeden bir seçenek seçin.

### <a name="attribute-filter-in-a-column-definition"></a>Bir sütun tanımındaki öznitelik filtresi

Öznitelikler bir hesabı veya hareketi ayrıntılı olarak tanımlayan mali veri değerleridir. Hesap öznitelikleri **Varlık**, **Borç**, **Gelir** ve **Gider**'dir. Hareket öznitelikleri ise **Hareket Açıklaması** ve **Hareket Uygulama Tarihi**'dir. Öznitelik desteği Microsoft Dynamics ERP sistemleri arasında farklılık gösterebilir. **Öznitelik Filtresi** hücresi **FD** sütunlarındaki verileri belirli değerlerle veya öznitelik kategorisi aralıklarıyla sınırlar. Bu özellik bir **ATTR** sütunuyla birlikte kullanılabildiği halde, **ATTR** sütunu gerekli değildir. Bir **FD** sütununda raporun öznitelik filtresinden içereceği hesaplar veya hareketlerde bir sınır vardır. **Not:** ERP sisteminizin hangi öznitelikleri desteklediğini görmek için, sisteminize ait tümleştirme kılavuzuna bakın.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Bir rapordaki bir FD sütunu için öznitelik filtresi uygulama

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Bir **FD** sütununa ait **Öznitelik Filtresi** hücresine çift tıklayın.
3.  **Öznitelik Filtresi** iletişim kutusunda, **Öznitelik** sütunundaki bir hücreye çift tıklayın ve ardından filtre türünü seçin.
4.  Sonuçları daha da sınırlandırmak için **Başlangıç** ve **Bitiş** sütunlarına bir aralık girin. **Başlangıç** hücresi bir değer içermelidir.
5.  **Tamam** düğmesini tıklatın.

#### <a name="example-of-an-attribute-filter"></a>Öznitelik filtresi örneği

Aşağıdaki örnek **Defter Kodu/Öznitelik Kategorisi** satırında bir hesap özniteliği bulunan bir sütun açıklaması parçasını göstermektedir. Bu sütuna ait öznitelik filtresi rapora eklenecek değer aralığını belirtir.

|                              | A    | B                    |
|------------------------------|------|----------------------|
| Sütun Türü                  | DESC | FD                   |
| Defter Kodu/Öznitelik Kategorisi |      | ACTUAL               |
| Mali Yıl                  |      | BASE                 |
| Dönem                       |      | 1:BASE               |
| Kapsanan Dönemler              |      | DÖNEMSEL             |
| ...                          |      |                      |
| Sütun Genişliği                 | 30   |                      |
| ...                          |      |                      |
| Öznitelik Filtresi             |      |  Referans=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Bir sütun tanımındaki boyut filtresi

Bir boyut filtresi, **FD** sütununu belirli boyut değerleriyle sınırlandırmak için kullanılır. Filtre tek bir boyut, bir boyut aralığı veya bir boyut grubu içerebilir. Filtre de boyut değer kümeleri içerebilir. Boyut değerleri değişebilir olduğundan, bir ..\finansal-boyut\ boyut tabanlı bir sistemin tam bir uzunluğa karşılık gelmesine gerek yoktur. Raporun bir raporlama ağacı içerip içermediğinden bağımsız olarak filtre uygulanır. Bir joker karakterini (\* veya?) herhangi bir konumda kullanabilirsiniz. Birden fazla hesap belirttiğinizde, aşağıdaki örnekte gösterildiği gibi hesaplar arasında virgül koyun: +Hesap =\[1200\], +Hesap =\[1100\], Departman =\[01?\] Tüm bölümler için özel bir hesap almak için Departman boyutu Boyut Filtresi dışarıda bırakabilirsiniz. Örneğin, aşağıdaki boyut filtrelerinin her ikisi de aynı şekilde işlenir:

-   +Hesap=\[1100\],Departman
-   +Hesap=\[1100\]

Ayrıca, tam eşleştirme için alfasayısal karakterlerin herhangi bir kombinasyonunu kullanabilir ve kısmi boyutlar tanımlayabilirsiniz. Örneğin, **Konum = \[10*\*\]**, 10 ile başlayan tüm konum boyutu değerlerini içerir.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Bir rapordaki bir sütun için boyut filtresi uygulama

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  Bir **FD** sütununa ait **Boyut Filtresi** hücresine çift tıklayın.
3.  **Boyutlar** iletişim kutusunda, uygulanacak filtreleri girin.
4.  **Tamam** düğmesini tıklatın.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Bir sütun tanımındaki birden fazla para birimi içeren bir raporu biçimlendirme

Birden fazla para birimi içeren bir rapor tutarları doğal (yerel) para biriminde, işlevsel (varsayılan) para biriminde veya raporlama para biriminde görüntüleyebilir. Bir şirketin işlevsel para birimi Microsoft Dynamics ERP sisteminde tanımlanır. Bu ERP ayarını, raporlarda kullanılan varsayılan para birimi simgelerini yapılandırabileceğiniz, işletim sisteminin bölgesel seçenekler ayarıyla karıştırmayın. Sütun tanımında aşağıdaki para birimiyle ilgili hücreler bulunur:

-   **Para Birimi Görüntüleme** – Hareketlerin gösterileceği para birimi türünü belirtin (doğal, işlevsel veya raporlama). Bu işlevselliğe bazen para birimi çevirisi de denir. Para birimi dönüştürme, genel muhasebe tutarlarını şirketin işlevsel para birimi ya da hareketin girildiği para birimi olmayabilecek bir para biriminde raporlama yeteneğidir.
-   **Para Birimi Filtresi**: Bir para birimi filtresi belirtin. Raporda sadece seçilen para birimi cinsinden girilen hareketler görüntülenir.

> [!NOTE]
> Birden fazla para birimi kullanan raporlar oluşturmak için **Rapor** sekmesindeki **Tüm raporlama para birimlerini dahil** onay kutusunu işaretlemeniz gerekir. Bir şirketin işlevsel para birimini belirlemek için, şu adımları izleyin.

1.  Rapor Tasarımcısı'nda, **Şirket** menüsünde, **Şirketler**'e tıklayın.
2.  **Şirketler** iletişim kutusunda, bir şirket seçin ve ardından **Görüntüle**'ye tıklayın.
3.  **Şirketi Görüntüle** iletişim kutusunda, **Bölgesel seçenekler**'in altında seçilen şirket için tanımlanan para birimini görüntüleyebilirsiniz.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Birden fazla para birimi içeren bir raporda para birimini belirtme

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  İlgili **FD** sütunundaki **Para Birimi Ekranı**'na çift tıklayın ve ardından para birimi bilgilerini görüntüleme seçeneğini seçin: **Doğal/kaynak para birimi**, **Şirket bilgilerindeki işlevsel para birimi** veya raporlama para birimi.
3.  İlgili **FD** sütunundaki **Para Birimi Filtresi** hücresine çift tıklayın ve ardından listeden uygun para birimi kodunu seçin. Raporda sadece bu para biriminde girilen hareketler görüntülenir.

> [!NOTE]
> Burada açıklanan seçenekler, ERP sistemine bağlı olarak farklılık gösterebilir. Daha fazla bilgi için bkz. [Microsoft ERP sistem belgesine](https://www.microsoft.com/en-us/download/details.aspx?id=5916).

### <a name="example-for-currency-display-and-currency-filter-cells"></a>Para Birimi Ekranı ve Para Birimi Filtresi hücreleri için örnek

Pelin, sütun tanımında aşağıdaki para birimi seçimlerini yaptı:

-   **Para Birimi Filtresi:** Yen
-   **Para Birimi Ekranı:** İşlevsel (ABD doları)

Pelinin seçtiği para birimi filtresi nedeniyle, rapor yalnızca Japon yeni (JPY) olarak girilen hareketleri içerir. Seçtiği para birimi ekranı nedeniyle, rapor işlevsel para birimi olan ABD doları (USD) cinsinden olan hareketleri görüntüler.

#### <a name="currency-filter-and-currency-display-combinations"></a>Para Birimi Filtresi ve Para Birimi Ekranı birleşimleri

Aşağıdaki tabloda, Pelin'in yaptığı seçimler nedeniyle **Para Birimi Ekranı** ve **Para Birimi Filtresi** hücrelerindeki çeşitli seçenek birleşimleri için oluşabilecek rapor sonuçlarını göstermektedir. İşlevsel para birimi USD'dir.


|            Para Birimi Ekranı hücresi             | Para Birimi Filtresi hücresi |                                                                                                       Rapor sonucu                                                                                                        |
|----------------------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|         Doğal/kaynak para birimi         | <strong>YEN</strong> |                                                                   <strong>6.000 Y</strong>: Sonuç yalnızca JPY olarak girilen hareketleri gösterir.                                                                   |
| Şirket bilgilerindeki işlevsel para birimi | <strong>YEN</strong> |          <strong>60 $</strong>: Sonuç yalnızca JPY olarak girilen hareketleri gösterir ve ABD doları cinsinden olan hareketleri görüntüler. <strong>Not:</strong> Dönüşüm oranı USD başına yaklaşık 100 JPY'dir.           |
| Şirket bilgilerindeki işlevsel para birimi |        Boş         | <strong>2.310 $\*\</strong>*: Sonuç, şirket bilgilerinde belirtilen işlevsel para birimindeki tüm verileri gösterir. <strong>Not:</strong> Bu tutar işlevsel para birimindeki tüm işlemlerin toplamıdır. |
|         Doğal/kaynak para birimi         |        Boş         |                                                       <strong>2.250 $</strong>: Sonuç, hareketin gerçekleştirildiği para birimindeki tüm tutarları gösterir.                                                        |

### <a name="calculation-column-in-a-column-definition"></a>Bir sütun tanımındaki hesaplama sütunu

Bir sütun tanımındaki bir **CALC** sütun türü <strong>Formül</strong> hücresindeki karmaşık hesaplamaları destekler ve <strong>+</strong>, <strong>-</strong>, <strong>\</strong>, ve **/* işleçlerinin yanı sıra <strong>IF/THEN/ELSE</strong> deyimlerini içerebilir. Bir hesaplama sütunu aynı zamanda başka herhangi bir sütuna, hatta sonraki sütunlara başvurabilir. Ayrıca, bir hesaplama sütunu sütunun başlıklarını desteklemek için mali yılı ve dönemi de içerebilir. Hesaplama formülü en fazla 1.024 karakter uzunluğunda olabilir. Hesaplama sonucunu yüzde olarak ifade etmek için özel bir biçim geçersiz kılma işlemi kullanın. <strong>Not:</strong> Hesaplama formüllerinin sonuçları yazdırılmayan sütun aralıklarındaki değerleri içermez. Örneğin, <strong>A:D</strong> <strong>0</strong> (sıfır) yazdırırken, yazdırılmayan değerler için <strong>A+B+C</strong> değeri hesaplar.

#### <a name="operators-in-calculation-columns"></a>Hesaplama sütunlarındaki işleçler

Sütunları toplamak, çıkarmak, çarpmak veya bölmek için sütun harflerini hesaplama sırasıyla girin ve ardından her sütun harfini ayırmak için ilgili işleci kullanın. Aşağıdaki tabloda bir hesaplama sütununda kullanılabilecek işleçler açıklanmıştır.

| İşleç | Örnek hesaplama | Açıklama                                                                                                                                                                                                                                    |
|----------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| +        | A+C                 | A sütunundaki tutarı C sütunundaki tutara ekleyin.                                                                                                                                                                                          |
| :        | A:C A:C-D           | Art arda gelen sütunlardan oluşan bir aralığı toplayın. Örneğin, **A:C** formülü, A ile C arasındaki sütunların toplamlarını eklerken, **A:C-D** formülü, A ile C arasındaki sütunların toplamlarını ekler ve ardından D sütunundaki tutarı çıkarır.                          |
| -        | A-C                 | A sütunundaki tutarı C sütunundaki tutardan çıkarın. **Not:** Bir sütundaki işareti ters çevirmek için eksi (-) işaretini de kullanabilirsiniz. Örneğin, A sütunundaki tutarın tersini B sütunundaki tutara eklemek için **-A+B** formülü kullanın. |
| \*       | A\*C                | A sütunundaki tutarı C sütunundaki tutara çarpın.                                                                                                                                                                                     |
| /        | A/C                 | A sütunundaki tutarı C sütunundaki tutara bölün.                                                                                                                                                                                       |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Bir sütun tanımında bir hesaplama formülü kullanma

1.  Rapor Tasarımcısı'nda, değiştirilecek sütun tanımını açın.
2.  İlgili **CALC** sütunundaki **Formül** hücresine bir formül girin.

#### <a name="complex-calculations"></a>Karmaşık hesaplamalar

Karmaşık bir hesaplama hücre referansları, işleçler, değerler ve iç içe parantez düzeylerinden oluşan herhangi bir birleşimi içerebilir. Örneğin, A ve B sütunlarının ortalamasını hesaplamak için **((A+B)/2)** hesaplama formülünü kullanın.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Bir sütun hesaplamasındaki rapor hücrelerini belirtme

Bir sütun harfi ve bir satır kodu girerek belirli bir rapor hücresine başvurabilirsiniz. Örneğin, **B.100** B sütunundaki 100 satır kodu anlamına gelir. Tam bir sütunu aynı sütundaki belirli bir rapor hücresi tutarına bölebilirsiniz. Örneğin, **B/B.100** hesaplaması B sütunundaki tutarın B sütununda 100 satır kodundaki değere bölünmesi gerektiği anlamına gelir. Hesaplama başka bir sütuna bağlı olan bir sütuna başvuruyorsa önce bağlı sütun çözülür. Bir sütunu yeniden ilk sütuna başvuran başka bir sütuna yönlendirirseniz döngüsel bir referans hatasına neden olursunuz. **Not:** Raporun hesaplama önceliğini değiştirirseniz hesaplama yanlış olabilir. Hesaplama önceliğini, rapor tanımındaki **Ayarlar** sekmesinde ayarlayabilirsiniz.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Bir sütunu bir temel satırla çarpma veya bu satıra bölme

Tüm değerleri belirli bir sütunda temel sayının yüzdesi olarak görüntüleyen bir sütun oluşturabilirsiniz. Bu nedenle, satırlar arasındaki ilişkileri bir satış satırının ya da bir toplam giderler satırının yüzdesi olarak gösterebilirsiniz. Belirli bir sütundaki her bir satırı bir temel satırla çarpmak veya bir temel satıra bölmek için, hesaplamada kullanılacak sütunu girin ve ardından **\*BASEROW** veya **BASEROW** seçimini yapın. Örneğin, **C\*BASEROW** veya **C/BASEROW** girin. **Not:** Bir sütun tanımında bir temel satır hesaplaması kullanıyorsanız bu sütun tanımıyla kullanılan her bir satır tanımının, hesaplamalar için en az bir temel satır içerdiğinden emin olun. 

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Bir sütundaki tutarı dönem sayısına bölme

Bir sütundaki tutarı belirtilen bir dönem sayısına bölebilirsiniz. Örneğin, **B/Dönem Sayısı**B sütunundaki değeri B sütunundaki dönem sayısına böler. Hesaplama birden fazla sütuna yayılıyorsa hesaplamada kullanılacak dönem sayısını belirtin. Örneğin, **(B+C)/Dönem Sayısı** formülü B ve C sütunlarındaki tutarları toplar ve ardından sonucu dönem değerine böler.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Finansal raporlamada satır tanımları](row-definitions-financial-reporting.md)

[Finansal raporlamada gelişmiş biçimlendirme seçenekleri](advanced-formatting-options-financial-reporting.md)




