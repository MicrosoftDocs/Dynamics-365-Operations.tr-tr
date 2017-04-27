---
title: "Finansal raporlarda sütun tanımları"
description: "Bu makalede sütun tanımları hakkında bilgi verilmektedir. Bir sütun tanımı, bir rapordaki sütunların içeriğini tanımlayan bir raporlama bileşeni veya yapıtaşı parçasıdır. Satır tanımları gibi, temel sütun tanımları da birden fazla raporda kullanılabilir."
author: RobinARH
manager: AnnBe
ms.date: 2016-08-09 21 - 27 - 36
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: af336db81f659d80248aa4ab1fbba96ed1ff48c2
ms.lasthandoff: 03/30/2017


---

# <a name="column-definitions-in-financial-reports"></a>Finansal raporlarda sütun tanımları

Bu makalede sütun tanımları hakkında bilgi verilmektedir. Bir sütun tanımı, bir rapordaki sütunların içeriğini tanımlayan bir raporlama bileşeni veya yapıtaşı parçasıdır. Satır tanımları gibi, temel sütun tanımları da birden fazla raporda kullanılabilir.

<a name="create-and-modify-a-column-definition"></a>Bir sütun tanımı oluşturma ve değiştirme
-------------------------------------

Bir sütun tanımı iki ila 255 sütun içerebilir.

### <a name="create-a-column-definition"></a>Bir sütun tanımı oluşturma

1.  Rapor Tasarımcısında gezinme bölmesinde **Sütun Tanımları** öğesine tıklayın.
2.  **Dosya** menüsünde, **Yeni** öğesini ve ardından **Sütun Tanımı** öğesini tıklayın.
3.  Sütun tanımı içeriğini ekleyin.

### <a name="open-a-column-definition"></a>Bir sütun tanımını açma

1.  Rapor Tasarımcısında gezinme bölmesinde **Sütun Tanımları** öğesine tıklayın.
2.  Açmak için bir sütun tanımını çift tıklayın.

### <a name="add-a-column-to-a-column-definition"></a>Sütun tanımına bir sütun ekleme

1.  Rapor Tasarımcısında **Sütun Tanımları** öğesini tıklayın ve ardından değiştirmek istediğiniz sütun tanımını açın.
2.  Yeni sütunun ekleneceği sütunu seçin.
3.  **Düzenle** menüsünden **Sütun Ekle** öğesini tıklayın. Yeni sütun, seçtiğiniz sütununun solunda görüntülenir.

### <a name="delete-a-column-from-a-column-definition"></a>Bir sütun tanımından sütun silme

1.  Rapor Tasarımcısında **Sütun Tanımları** öğesini tıklayın ve ardından değiştirmek istediğiniz sütun tanımını açın.
2.  Silinecek sütunu seçin.
3.  **Düzenle** menüsünden **Sütun Sil** öğesini tıklayın.

## <a name="contents-of-a-column-definition"></a>Bir sütun tanımının içeriği
Bir sütun tanımı şu bilgileri içerir:

-   Satır tanımı için bir açıklama sütunu
-   Mali verilere, bir Microsoft Excel çalışma sayfasına veya sütun tanımındaki diğer verilere dayalı hesaplamalara ait verileri gösterilecek tutar sütunları
-   Biçimlendirme sütunları
-   Öznitelik sütunları

Bu bilgiler, sütun tanımının aşağıda belirtilen alanlarında görüntülenir:

-   Sütun tanımının üstbilgiler alanı, raporda görüntülenecek üstbilgi metnini ve biçimlendirmeyi içerir. Bir üstbilgi, tek bir veri sütununa uygulanabilir, birden çok sütuna yayılabilir veya bir koşullu olarak sütuna uygulanabilir. Sütun tanımı gereksinim duyduğunuz kadar sütun başlık satırları içerebilir. **Not:** Sütun üstbilgileri, raporun her bir veri sütununa uygulanır. Rapor üstbilgileri tüm rapora uygulanır. Rapor üstbilgilerini, rapor tanımının **Üstbilgiler ve Altbilgiler** sekmesinde tanımlarsınız.
-   Sütun ayrıntı satırları, sütun tanımında üstbilgi satırlarının altındaki satırlardır. Sütun ayrıntı satırları rapora dahil edilen bilgileri tanımlar. Aşağıdaki tabloda sütun ayrıntı satırları listelenmiş ve açıklanmıştır.

    | Sütun ayrıntı satırının adı                                                | Açıklama                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Sütun Tipi                                                           | (Zorunlu) Sütundaki verilerin türünü belirtin.                                                     |
    | Defter Kodu/Öznitelik Kategorisi                                          | **FD** ve **ATTR** türlerindeki sütunlar için mali veri bilgilerini tanımlayın.                       |
    | Mali Yıl Dönemleri Kapsanıyor                                    | **FD** türündeki sütunlar için mali veri bilgilerini tanımlayın.                                     |
    | Formül                                                               | **CALC** türündeki sütunlar için hesaplama formülünü tanımlayın.                                        |
    | Sütun Biçimi Atlatma Yazdırma Kontrolünden Önce Sütun Genişliği Ekstra Boşlukları | Özel biçim seçeneklerini belirtin.                                                                        |
    | Sütun Kısıtlamaları                                                   | Verileri sınırlandırın.                                                                                         |
    | Raporlama Birimi                                                        | Sütunu sadece belirtilen raporlama birimi için geçerli verileri gösterecek şekilde sınırlandırın.                      |
    | Görüntülenen Para Birimi Para Birimi Filtresi                                      | Para birimini biçimlendirin.                                                                                       |
    | Boyut Filtresi                                                      | Verileri belirli mali veri raporlama birimleriyle sınırlandırmak için bir filtre belirtin.                           |
    | Öznitelik Filtresi                                                      | Mali verileri sınırlandırmak için bir filtre belirtin.                                                       |
    | Başlangıç Tarihi Bitiş Tarihi                                                   | Mali verileri belirli tarihlerle sınırlandırın.                                                         |
    | Gerekçe                                                         | Satır tanımında belirtilen açıklama metnini sola hizalayın, ortalayın veya sağa hizalayın. |

## <a name="column-restrictions-in-a-column-definition"></a>Bir sütun tanımındaki sütun kısıtlamaları
Bir sütun tanımının verileri nasıl kullanacağını veya bilgileri nasıl hesaplayacağını tanımlamak için sütun kısıtlamalarını kullanabilirsiniz. Ayrıca, bir rapor sütununu belirli bir birimle veya belirli tarihlerle de sınırlandırabilirsiniz. **Not:** Bir **Sütun Kısıtlama** kodu, satır tanımında atanmış, çakışan tüm ayarları geçersiz kılar.

### <a name="column-restrictions-cell"></a>Sütun Kısıtlamaları hücresi

**Sütun Kısıtlamaları** hücresi örneğin satır biçimlendirme, ayrıntılar ve tutarlar vb. gibi o sütun için bilgileri kısıtlayan veya baskılayan kodları içerebilir.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Bir sütun tanımına bir sütun kısıtlaması ekleme

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Sınırlandırılacak sütun için **Sütun Kısıtlamaları** hücresini çift tıklayın.
3.  **Sütun Kısıtlamaları** iletişim kutusunda, listeden bir veya daha fazla sayıda kod girin ve ardından **Tamam** düğmesini tıklayın.

### <a name="column-restriction-codes"></a>Sütun kısıtlama kodları

Aşağıdaki tabloda sütun kısıtlama kodları açıklanmıştır.

| Sütun kısıtlama kodu | Açıklama                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SU                      | Satır tanımında bir alt çizgi komutunun (**---**) veya bir çift alt çizgi komutun (**===**) girildiği bir sütun için alt çizgiyi baskılayın. Örneğin, bir yüzde hesaplaması tarafından üretilen tutarları alt çizgili görüntülemek istemeyebilirsiniz.                                                                        |
| ST                      | Toplamları sütunda sadece ayrıntılar görüntülenecek şekilde baskılayın (örneğin bir istatistik sütunu).                                                                                                                                                                                                                                      |
| SD                      | Ayrıntıları sütunda sadece **TOT** ve **CAL** satırları (satır tanımından) görüntülenecek şekilde baskılayın.                                                                                                                                                                                                                              |
| DR                      | Bir **FD** sütunundaki tutarları borç tutarlarıyla sınırlandırın.                                                                                                                                                                                                                                                                              |
| CR                      | Bir **FD** sütunundaki tutarları alacak tutarlarıyla sınırlandırın.                                                                                                                                                                                                                                                                             |
| ADJ                     | Sütundaki tutarları, mevcutsa dönem ayar tutarlarıyla sınırlandırın.                                                                                                                                                                                                                                        |
| XAD                     | Sütundaki tutarları, dönem ayar tutarları hariç tutulacak şekilde sınırlandırın.                                                                                                                                                                                                                                                     |
| PT                      | Sütundaki tutarları, mevcutsa sadece nakledilen hareketleri içerecek şekilde sınırlandırın.                                                                                                                                                                                                                 |
| UPT                     | Sütundaki tutarları, mevcutsa sadece nakledilmeyen hareketleri içerecek şekilde sınırlandırın. **Not:** Nakledilmeyen hareketler tüm veri sağlayıcıları tarafından desteklenmemektedir. Daha fazla bilgi için, Microsoft Dynamics ERP sisteminizin [veri entegrasyon kılavuzuna](http://go.microsoft.com/fwlink/?LinkID=162565) bakın. |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Bir sütunu bir raporlama birimiyle sınırlandırma

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Sınırlandırılacak sütun için **Raporlama Birimi** hücresini çift tıklayın.
3.  **Raporlama Birimi Seçimi** iletişim kutusundaki **Raporlama ağacı** listesinden bir ağaç seçin.
4.  Birimler listesini genişletin veya daraltın, bir raporlama birimi seçin ve ardından **Tamam** düğmesini tıklayın.

## <a name="format-column-headers"></a>Sütun üstbilgilerini biçimlendirme
Bir raporda sütunların üstünde görüntülenen üstbilgileri ekleyebilir, değiştirebilir ve silebilirsiniz. Ayrıca, sütun tanımlarındaki **Dönem** alanına ve rapor tanımlarındaki **Temel Dönem** alanına dayalı olarak koşullu genişleyen sütun üstbilgileri de yapılandırabilirsiniz. Temel dönem özelliği, aktarmalı tahmin raporları oluştururken size zaman kazandırabilir.

### <a name="create-and-manage-column-headers"></a>Sütun üstbilgileri oluşturma ve yönetme

Bir raporda sütunların üstünde görüntülenen üstbilgileri eklemek, değiştirmek ve silmek için **Sütun Üstbilgileri** iletişim kutusunu kullanabilirsiniz. Aşağıdaki tabloda **Sütun Üstbilgileri** iletişim kutusunun alanları açıklanmıştır.

| Alan                 | Açıklama                                                                                                                                                                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sütun üstbilgi metni    | Bu metin sütun üstbilgisinde görüntülenir. Metni doğrudan bu alana yazabilir veya **Otomatik Metin Ekle** öğesini tıklayarak rapor oluşturulduğunda her seferinde sütun üstbilgisini güncelleyecek bir seçenek belirleyebilirsiniz. Birden fazla otomatik metin kodu eklemek için **Otomatik Metin Ekle** öğesini yeniden tıklayın ve ardından listedeki başka bir kodu tıklayın. |
| Biçim seçenekleri        | Bir sütun üstbilgisine kutu veya alt çizgi vb. gibi biçimlendirmeler uygulayın.                                                                                                                                                                                                                                                           |
| Üstbilgiyi başlat Üstbilgiyi sonlandır | Üstbilgi metninin uygulanacağı sütun veya sütunları tanımlayın.                                                                                                                                                                                                                                                            |
| Gerekçe         | Sütun üstbilgi metninin **Üstbilgiyi başlat** ve **Üstbilgiyi sonlandır** alanlarında tanımlanan sütun veya sütun aralığı için nasıl hizalanacağını tanımlayın.                                                                                                                                                               |

### <a name="create-a-column-header"></a>Bir sütun üstbilgisi oluşturma

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Bir üstbilgi hücresini çift tıklayın.
3.  **Sütun Üstbilgisi** iletişim kutusunda sütun üstbilgi metnini girin. Alternatif olarak, **Otomatik Metin Ekle** öğesini tıklayın ve bir seçenek belirleyin.
4.  **Biçim seçenekleri** alanından üstbilgi için bir biçim seçin.
5.  **Üstbilgiyi başlat** alanında, sütun üstbilgisinin başlatılacağı sütuna karşılık gelen harfi girin. **Üstbilgiyi sonlandır** alanında, sütun üstbilgisinin sonlandırılacağı sütuna karşılık gelen harfi girin.
6.  **Hizalama** altından, sütun üstbilgi metni için sola hizalama, ortalama veya sağa hizalama seçeneklerinden birini belirleyin.
7.  **Tamam** düğmesini tıklatın.

### <a name="add-a-column-header-row"></a>Bir sütun üstbilgi satırı ekleme

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Üstbilgi satırından bir hücre seçin.
3.  **Düzenle** menüsünden **Satır Ekle** öğesini tıklayın. Yeni satır, 2. adımda seçtiğiniz satırın üzerine eklenir. **Not: **Bir raporda dört ya da daha fazla rapor üstbilgisi satırına sahipseniz, üstbilgiler bir Excel çalışma sayfasına aktarıldığında üst üste binecektir. Rapordaki tüm üstbilgileri görüntülemek için rapor tanımındaki üst kenar boşluğunu artırın.

### <a name="delete-a-column-header-row"></a>Bir sütun üstbilgi satırını silme

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Üstbilgi satırından, silinecek hücreyi seçin.
3.  **Düzenle** menüsündeki **Satır Sil** öğesini tıklayın.

### <a name="create-an-automatically-generated-header"></a>Otomatik üretilen bir üstbilgi oluşturma

Rapor tasarımcısı otomatik metin kodlarına göre otomatik olarak sütun başlıkları üretebilir. Otomatik kodlar bir rapor üretildiğinde her defasında güncellenen değişkenlerdir. Herhangi bir üstbilgi değişebilecek rapor bilgilerini, örneğin tarihleri veya dönem rakamlarını tanımlamak için bu kodları içerebilir. Bu nedenle, sütun tanımını birden fazla rapor tanımı, dönem ve raporlama ağacı için kullanabilirsiniz. Otomatik metin kodları, sütun tanımının ayrıntı satırlarına ait takvim bilgilerine dayalı olduğundan sadece **CALC**, **FD** ve **WKS** sütunları için desteklenir. Sütun üstbilgisinde bir otomatik metin kodunun nasıl görüntüleneceği, bu bilgilerin raporda nasıl görüneceğini etkiler. **Sütun Üstbilgisi** iletişim kutusunda, otomatik metin kodları karışık şekilde görüntülenir. Bu nedenle, metin, raporda karışık şekilde görüntülenir. Örneğin, standart bir takvim yılı içinde **@CalMonthLong** öğesi **7** ile gösterilen ayı **Temmuz** olarak çözümler. Ay adının büyük olması (örneğin **TEMMUZ**) olması gerekiyorsa, **Sütun üstbilgi metni** alanına otomatik metin kodunu büyük harflerle girin. Örneğin: **@CALMONTHLONG**olarak girin. Kodları ve metinleri karıştırabilirsiniz. Örneğin, u üstbilgi metnini girin: **Dönem @FiscalPeriod-@FiscalYear @StartDate - @EndDate.** Oluşturulacak rapor üstbilgisi şu metni üretir: **01/01/02 tarihinden 01/31/02 tarihine kadar 1-02 Dönemi**. **Not:** Uzun tarih vb. gibi bazı metin biçimleri Dynamics 365 for Operations sunucunuzdaki bölgesel ayarlarınıza bağlıdır. Bu ayarları değiştirmek için **Başlat** düğmesini, **Denetim Masası** öğesini ve ardından **Bölge ve Dil** öğesini tıklayın. Aşağıdaki tabloda sütun üstbilgileri için kullanılabilen otomatik metin seçenekleri listelenmiştir.

| Otomatik metin seçeneği ve kodu                | Açıklama                                                                                                                                                                                                                                                                                      |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ay adı (@CalMonthLong)              | Mevcut ayın adını sütun üstbilgisinde yazdırın. Rapordaki tutarları binler, milyonlar veya milyarlar olarak yuvarlamaya karar verdiğinizde ve rapordaki sütun genişliğini dokuz karakterden kısa olarak ayarladığınızda ayın adı, ilk üç karakteri gözükecek şekilde kısaltılır. |
| Kısaltılmış ay adı (@CalMonthShort) | Seçilen mali dönem için ayın kısaltılmış adını yazdırın.                                                                                                                                                                                                                          |
| Dönem numarası (@FiscalPeriod)           | İlgili sütun için tanımlanan mali dönemin sayısını yazdırın. Sütun birden fazla dönemi kapsıyorsa aralıktaki son dönem yazdırılır.                                                                                                                                   |
| Dönem açıklaması (@FiscalPeriodName)  | Mali verilerde açıklanan mali dönem açıklamasını yazdırın.                                                                                                                                                                                                                    |
| Mali yılı (@FiscalYear)               | Sütun için mali yılı sayısal formatta yazdırın.                                                                                                                                                                                                                                            |
| Takvim yılı (@CalYear)                | Sütun için takvim yılını sayısal formatta yazdırın.                                                                                                                                                                                                                                          |
| Başlangıç tarihi (@StartDate)                 | Sütun için başlangıç tarihini yazdırın.                                                                                                                                                                                                                                                             |
| Bitiş Tarihi (@EndDate)                     | Sütun için bitiş tarihini yazdırın.                                                                                                                                                                                                                                                               |
| Ağaçtan birim adı (@UnitName)         | Bir sütunu raporlama ağacının belirli bir birimiyle sınırlandırırsanız birim adını sütun üstbilgisinde yazdırın.                                                                                                                                                                                     |
| Birim açıklama (@UnitDesc)            | Bir sütunu raporlama ağacının belirli bir birimiyle sınırlandırırsanız birim açıklamasını sütun üstbilgisinde yazdırın.                                                                                                                                                                              |
| Defter Kodu (@BookCode)                   | Sütunda tanımlanan defter kodunu yazdırın.                                                                                                                                                                                                                                             |
| Boş satır (@Blank)                     | Sütun başlığına boş bir satır ekleyin.                                                                                                                                                                                                                                                       |

### <a name="create-a-conditional-spanning-header"></a>Koşullu genişleyen bir üstbilgi oluşturma

Koşullu genişleyen üstbilgiler belirli dönem verilerine dayalı olarak birden fazla sütuna yayılabilir. Örneğin, mali yıl için bir bütçe raporuna sahipseniz ve geçmiş aylara ait fiili bütçeleri gelecek aylara ait kestirilen bütçelerle birlikte görüntülemek istiyorsanız, rapor üstbilgisini otomatik olarak güncelleştirmek için koşullu genişleyen üstbilgiyi kullanabilirsiniz. Koşullu genişleyen bir üstbilgi oluşturduğunuzda şu durumlara dikkat edin:

-   Bir başlangıç koşulundan (**Üstbilgiyi başlat** alanı) önce eşleştirilen durdurma koşulları (**Üstbilgiyi Sonlandır** alanı) dikkate alınmaz. Örneğin; B sütunu, TEMEL+1'den TEMEL'e olarak tanımlanmış bir genişleme koşuluna sahip, TEMEL, C sütununda ve TEMEL+1, D sütununda bulunuyor. Bu durumda C sütunundaki durdurma koşulu dikkate alınması ve üstbilgi yazdırma işlemi D sütunundan başlar.
-   Çakışan sütun üstbilgileri tanımlarsanız, bunlar raporda yazdırıldığında üst üste gelir. Rapor oluşturulur, ancak aşağıdaki uyarı **Rapor Sıra Durumu** alanında görüntülenir: "Diğer sütun başlıklarıyla kesişen, taban kesişimi kullanan sütun başlıkları üst üste gelen metine sebep olabilir." Örneğin, sütun B üzerindeki başlık tanımı B eşittir B'den TEMEL +1'edir ve sütun D üzerindeki başlık tanımı TEMEL+1'den F'yedir. Bu durumda, başlıklar birbirlerinin üstüne yazılır ve okunamaz durumda olurlar. Bir **Üstbilgiyi başlat/Üstbilgiyi sonlandır** tanımında TEMEL kullanılıyorsa, üstbilgilerin çakışıp çakışmadığını kontrol etmek için, oluşturulan rapor görüntülediğinizden emin olun.
-   Yazdırılmayacak (**NP**) sütununda genişletme tanımında TEMEL seçimi yapılmışsa, sütun tanımında yapılan tanımlardan bağımsız olarak dikkate alınmayacaktır. Temel olarak, bu senaryo bir sütun üstbilgi tanımının oluşturulmamasıyla aynıdır.
-   Koşullu yazdırma sütunları (**P&lt;B,** **P&gt;=B**) için koşullu genişleyen üstbilgiler herhangi bir normal sütun üstbilgi tanımı gibi davranır. Örneğin, koşul yanlış ise, genişleme koşulu için daha sonraki bir sütun eşleşmesi, üstbilginin yazdırılmasını başlatır.

#### <a name="create-a-conditional-spanning-header"></a>Koşullu genişleyen bir üstbilgi oluşturma

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Bir üstbilgi hücresini çift tıklayın.
3.  **Sütun Üstbilgisi** iletişim kutusunda sütun üstbilgi metnini girin. Alternatif olarak, **Otomatik Metin Ekle** öğesini tıklayın ve bir seçenek belirleyin.
4.   **Biçim seçenekleri** alanından üstbilgi için bir biçimlendirme stili seçin.
5.  Rapor oluşturulduğunda belirtilen temel döneme göre bir dönem belirtin. **Üstbilgiyi başlat** ve **Üstbilgiyi sonlandır** alanlarına aşağıdaki değerlerden birini girin: **TEMEL**, **TEMEL-X** veya **TEMEL+X**; burada X, temel dönemdeki dönem sayısını ifade eder. Örneğin, **Üstbilgiyi sonlandır** alanına **TEMEL** yazarsanız, koşullu genişleyen sütun üstbilgisi metni, rapor tanımının **Temel dönem** değerinin **Dönem** değere eşit olduğu sütun üstbilgisinde başlar. **Üstbilgiyi sonlandır** alanında belirtilen sütunda sona erer. Bu nedenle, genişlik TEMEL ile M sütunu arasındaysa ve rapor tanımının **Temel dönemi** değeri **4** ise üstbilgi, dönemin **4** olarak ayarlandığı sütunda başlar ve M sütununda sona erer. Üstbilgi sadece yazdırılan sütunlarda durur ve başlar.
6.  **Hizalama** altından sütun üstbilgi metni için sola hizalama, ortalama veya sağa hizalama seçeneklerinden birini belirleyin.
7.  **Tamam** düğmesini tıklatın.

#### <a name="example-of-a-conditional-spanning-header"></a>Koşullu genişleyen üstbilgilere örnek

Phyllis, dinamik bir altı aylık tahmin için bir rapor oluşturuyor. Fiili verileri içeren sütunların üzerine "Fiili" sözcüğünün ve bütçe tahminlerini içeren sütunların üzerine "Bütçe" sözcüğünün yazdırılmasını istiyor. Raporun çalıştırıldığı her ay, fiili sütun bir artarken, tahmin sütunu bir azalıyor. Phyllis, her rapor oluşturulduğunda üstbilgileri ayarlamak üzere sütun tanımını el ile değiştirebilmektedir, ancak zamandan ve emekten tasarruf etmek için her rapor oluşturulduğunda uygun sütunları içine alacak şekilde genişleyen üstbilgileri otomatik olarak oluşturacak koşullu genişleyen üstbilgiler oluşturmaya karar veriyor. Phyllis, Rapor Tasarımcısını açıyor, gezinme bölmesindeki **Sütun Tanımı** öğesini tıklıyor ve rapor için sütun tanımını açıyor. Ardından, aşağıdaki bilgileri giriyor. Rapor tanımındaki temel dönem 4'tür.

|                     | A:    | B:             | A             | B             | E:             | C             | G:             | H:             | I:             | J             | K             | L             | P             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Üstbilgi 1            |      | Gerçek        | Bütçe        |               |               |               |               |               |               |               |               |               |               |
| Üstbilgi 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Başlık 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Sütun Tipi         | DESC | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Defter Kodu/Öznitelik |      | FİİLİ        | BÜTÇE2012    | FİİLİ        | BÜTÇE2012    | FİİLİ        | BÜTÇE2012    | FİİLİ        | BÜTÇE2012    | FİİLİ        | BÜTÇE2012    | FİİLİ        | BÜTÇE2012    |
| Mali Yıl         |      | TEMEL          | TEMEL          | TEMEL          | TEMEL          | TEMEL          | TEMEL          | TEMEL          | TEMEL          | TEMEL          | TEMEL          | TEMEL          | TEMEL          |
| Dönem              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Kapsanan Dönemler     |      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      | DÖNEMSEL      |
| Sütun Genişliği        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Yazdırma Kontrolü       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Phyllis, **Sütun Üstbilgisi** iletişim kutusunu açmak üzere bir sütun üstbilgi hücresini çift tıklıyor ve buraya aşağıdaki bilgileri giriyor.

| Alan              | Değer                 |
|--------------------|-----------------------|
| Sütun üstbilgi metni | Fiili                |
| Otomatik Metin Ekle    | Hiçbir seçim yapılmadı. |
| Biçim seçenekleri     | Kutu                   |
| Gerekçe      | Hiçbir seçim yapılmadı. |
| Üstbilgiyi başlat        | B:                     |
| Üstbilgiyi sonlandır          | TEMEL                  |
| Bütçe üstbilgisi      | TEMEL+1 - son sütun  |

Phyllis, bilgileri girmeyi bitirdikten sonra **TAMAM** düğmesini tıklıyor. Ardından, **Sütun Üstbilgisi** iletişim kutusunu açmak üzere C sütunundaki sütun üstbilgisi hücresini çift tıklıyor ve buraya aşağıdaki bilgileri giriyor.

| Alan              | Değer                 |
|--------------------|-----------------------|
| Sütun üstbilgi metni | Bütçe                |
| Otomatik Metin Ekle    | Hiçbir seçim yapılmadı. |
| Biçim seçenekleri     | Kutu                   |
| Gerekçe      | Hiçbir seçim yapılmadı. |
| Üstbilgiyi başlat        | A                     |
| Üstbilgiyi sonlandır          | TEMEL+2                |

Artık, bu rapor her oluşturulduğunda, fiili verileri içeren sütunların üzerinde "Fiili" sözcüğü ve bütçe tahminlerini içeren sütunların üzerinde "Bütçe" sözcüğü yazdırılacaktır. Ek olarak, sütun sayısı her ay ayarlanacaktır.

## <a name="apply-column-justification"></a>Sütun hizalama uygulama
**Hizalama** hücresi bir rapordaki bir açıklama sütununa hizalama biçimlendirmesinin uygulanması için kullanılır. Bu seçenek sadece sütun açıklamalarını etkiler, fiili değerleri etkilemez.

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  **Hizalama** hücresini çift tıklayın.
3.  Listeden aşağıdaki değerlerden birini seçin:
    -   **Yok** – Hiçbir hizalanma uygulanmaz.
    -   **Sola** – Sütun açıklamaları sola hizalanır.
    -   **Ortala** – Sütun açıklamaları ortalanır.
    -   **Sağa** – Sütun açıklamaları sağa hizalanır.

## <a name="add-special-formatting-options"></a>Özel biçimlendirme seçenekleri ekleme
Sütun tanımında, biçimlendirme sütunu ayrıntı satırları, seçilen sütunlara özel biçimlendirme uygular. **Yazdırma Kontrolü** seçeneklerinden ve **Sütun Kısıtlamaları** seçeneklerinden bazıları **FD** sütunlarına özel olmasına rağmen, seçeneklerinden birçoğu tüm sütun türlerine uygulanır. Sütun tanımında belirtilen biçimlendirme, rapor tanımında belirtilen biçimlendirmeyi geçersiz kılar. Ancak, satır tanımında belirtilen biçimlendirme, sütun tanımında belirtilen biçimlendirmeyi geçersiz kılar. Aşağıdaki satırlar biçimlendirme satırları olarak kabul edilir:

-   Sütun Genişliği
-   Sütun Öncesinde Ekstra Boşluklar
-   Biçim/Para Birimi Atlatma
-   Yazdırma Kontrolü

### <a name="changing-the-column-width"></a>Sütun genişliğini değiştirme

**Sütun Genişliğini** hücresi, bu sütunun genişliği için yazdırılan raporda kullanılacak karakter sayısını belirler. Sütun genişliği, tutarlar içeren sütunlar (**CALC**, **WKS** ve **FD** türü sütunlar), açıklamalar (**DESC** türü açıklamalar) veya dolgular (**FILL** türü sütunlar) için önemlidir. Varsayılan olarak, her bir sütunun genişliğinin içerikler sığacak şekilde otomatik olarak ayarlanması için**Otomatik Sığdırma** seçeneği seçilir.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Bir sütunun rapordaki genişliğini belirtme

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  **Sütun Genişliğini** hücresinde, sütun genişliği için boşluk sayısını girin. Herhangi bir sütunun maksimum genişliği 255 karakterdir (Bu rakama kuruşlar, virgüller ve parantezler dahildir). Alternatif olarak, sütun için hücre içeriğine göre uygun genişliği seçmek üzere rapor tasarımcısını etkinleştirmek için **Sütun Genişliği** hücresini çift tıklayın ve ardından **Otomatik Sığdırma** öğesini seçin.

### <a name="add-space-between-columns"></a>Sütunlar arasına boşluk ekleme

**Sütun Öncesi Ekstra Boşluklar** hücresi, sütun tanımında bir sütun ile yandaki sütunlar arasındaki ayracın genişliğini belirler. **Sütun Öncesi Ekstra Boşluklar** ayarı, sütun için tüm sütun ayrıntı satırlarını etkiler, ancak sütun üstbilgi satırlarını etkilemez. Bu seçeneği sütun gruplarını ayırmak veya açıklamadan önce birkaç boşluk eklemek için kullanın, böylece açıklama sütunu raporda sola hizalanan başlıklardan ayrılmış olur. Varsayılan olarak her bir sütun arasında iki boşluk bırakılır. Bu ayarı rapor tanımındaki **Ayarlar** sekmesinden değiştirebilirsiniz.

#### <a name="specify-the-space-between-columns"></a>Sütunlar arasında boşluk ayarlama

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  **Sütun Öncesi Ekstra Boşluklar** hücresinde, sütunlar arasına eklenecek boşluk sayısını girin.

### <a name="specify-a-currency"></a>Bir para birimi seçme

**Biçim/Para Birimi Atlatma** hücresi sütundaki ondalıklı değerlerin, para biriminin ve yüzde tutarlarının biçimlendirmesini belirler. Bu biçimlendirme, sütun tanımında veya sistem varsayılan ayarlarında tanımlanan biçimlendirmeyi geçersiz kılar.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Bir rapor sütununa bir para birimi biçim atlatma atama

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Bir tutar sütunundaki bir **Biçim/Para Birimi Atlatma** hücresini çift tıklayın.
3.  **Biçim Atlatma** iletişim kutusundan biçimlendirme seçeneklerini belirleyin.

### <a name="add-a-print-control-code"></a>Bir yazdırma kontrol kodu ekleme

**Yazdırma Kontrolü** hücresi bir sütunun görüntülenme veya yazdırma özelliklerini ayarlayan kodlar içerebilir.  Normal yazdırma kontrol kodları ve koşullu yazdırma kontrol kodları olmak üzere iki türde yazdırma kontrol kodu bulunmaktadır.

#### <a name="regular-print-control-codes"></a>Normal yazdırma kontrol kodları

| Yazdırma kontrol kodu | Çeviri                                     | Açıklama                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NP                 | Yazdırma yok                                     | Bu sütundaki tutarlar yazdırılan rapordan ve hesaplamalardan hariç tutulur. Yazdırılmayan bir sütunu bir hesaplamaya dahil etmek için sütunu doğrudan hesaplama formülüne atayın. Örneğin, yazdırılmayan C sütunu, şu hesaplamaya dahildir: **B+C+D**. Ancak, yazdırılmayan C sütunu, şu hesaplamaya dahil değildir: **B:D**.                                                                                                                                          |
| XCR                | Tipik satır bakiyesi alacak ise işareti değiştirme | İstenmeyen farkların (örneğin, gelir azalması veya gider artması) her zaman negatif olduğu bir bütçe veya karşılaştırma raporu oluşturun. İlgili satırın bakiyesi genellikle borç ise (satır tanımının **Normal Bakiye** sütununda **C** olarak tanımlanır) sütun tutarının işaretini ters çevirmek için **CALC** sütununa bu kodu uygulayın. **Not:** Tipik olarak bir alacak bakiyesi taşıyan **TOT** satırları ve **CAL** satırları için, satır tanımında **Normal Bakiye** sütununa **C** girdiğinizden emin olun. |
| X0                 | Tümü sıfır veya boş ise sütunu baskılama          | **FD** sütunundaki tüm hücreler boşsa veya sadece sıfır içeriyorsa bu sütun rapordan hariç tutulur.                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SR                 | Yuvarlamayı baskılar                               | Bu sütundaki tutarların yuvarlanmasını engeller.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| XR                 | Nakli baskılama                                 | Bir nakil işlemini baskılar. Rapor bir raporlama ağacı kullanıyorsa, bu sütundaki tutarlar bir sonraki ana düğümlere nakledilmez.                                                                                                                                                                                                                                                                                                                                                                                                   |
| RP                 | Sütunu her sayfada tekrarla                      | Belirtilen sütun raporun her sayfasında tekrarlanır. Örneğin, her sayfada satır kodlarını çeken **ROW** türündeki bir sütunu dahil etmek için **RP** yazdırma kontrol kodunu kullanabilirsiniz.                                                                                                                                                                                                                                                                                                                                           |
| WT                 |  Metni kaydır                                      |  Bir sütundaki metin, ayrılan alana sığmayacak kadar uzun ise, metin tümü sütununda tutulacak şekilde kaydırılır.                                                                                                                                                                                                                                                                                                                                                                                                                            |

#### <a name="conditional-print-control-codes"></a>Koşullu yazdırma kontrol kodları

| Koşullu yazdırma kontrol kodu | Açıklama                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (yok)                         | Koşullu yazdırma seçimini temizler.                                                  |
| P&lt;B                         | Belirtilen sütun sadece dönem, temel dönemden kısa ise görüntüler.             |
| P&gt;B                         | Belirtilen sütun sadece dönem, temel dönemden uzun ise görüntüler.             |
| P=B                            | Belirtilen sütun sadece dönem, temel döneme eşit ise görüntüler.              |
| P&lt;=B                        | Belirtilen sütun sadece dönem, temel döneme eşit veya daha kısa ise görüntüler. |
| P&gt;=B                        | Belirtilen sütun sadece dönem, temel döneme eşit veya daha uzun ise görüntüler. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Bir rapor sütununa yazdırma kontrol kodları ekleme

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  **Yazdırma Kontrolü** hücresini çift tıklayın.
3.  **Yazdırma Kontrolü** iletişim kutusunda, **Yazdırma kontrolü seçeneklerini seç** listesinden bir kod seçin. Birden fazla kod seçmek için, kodları seçerken Ctrl tuşunu basılı tutun.
4.  **Koşullu yazdırma seçenekleri** alanından bir seçenek belirleyin. Varsayılan olarak, **(yok)** seçilir. Aynı anda sadece bir koşullu yazdırma kodu seçebilirsiniz.
5.  **Tamam** düğmesini tıklatın.

**İpucu:** Ayrıca, yazdırma kontrol kodlarını doğrudan **Yazdırma Kontrol** hücresine de girebilirsiniz. Birden fazla yazdırma kontrol kodunu virgülle ayırın.

### 

## <a name="column-types"></a>Sütun tipleri
Bir rapordaki her bir sütunun içerdiği bilgilerin türü, sütun tanımındaki **Sütun Türü** satırındaki değer tarafından belirlenir. Her bir sütun tanımı mutlaka en az bir açıklama (**DESC**) sütunu ve bir tutar (**FD**, **WKS** veya **CALC**) sütunu içermelidir. **Not:** Sütun türü kodları tüm muhasebe sistemlerine uygulanmaz. Muhasebe sisteminiz için geçerli olmayan bir tür seçerseniz, bu sütun raporda boş çıkar.

### <a name="specify-a-column-type"></a>Bir sütun türü belirleme

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Uygun sütunda, **Sütun Türü** satırındaki bir hücreyi çift tıklayın.
3.  Listeden bir sütun türü seçin. Aşağıdaki tabloda çeşitli sütun türleri açıklanmıştır.
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
    <td>Satır tanımında bir <strong>Mali Boyutlara Bağlantı</strong> sütunu veya bir <strong>Çalışma Sayfasına Bağlantı</strong> sütunu kullandığınızda mali veriler veya bir Excel çalışma sayfasındaki veriler görüntülenir. <strong>FD</strong> sütun türünü seçtiğinizde aşağıdaki satırlar için otomatik olarak varsayılan ayarlar tanımlanır:
    <ul>
    <li><strong>Defter Kodu/Öznitelik Kategorisi:</strong> FİİLİ</li>
    <li><strong>Defter Kodu/Öznitelik Kategorisi:</strong> FİİLİ</li>
    <li><strong>Mali Yıl:</strong> TEMEL</li>
    <li><strong>Dönem:</strong> TEMEL</li>
    <li><strong>Kapsadığı Dönemler:</strong> DÖNEMSEL</li>
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
    <td>Satır tanımında satır açıklamasını gösterir. Açıklama sütunu genellikle rapordaki ilk sütun olmasına rağmen herhangi bir konumda olabilir.</td>
    </tr>
    <tr class="even">
    <td>SATIR</td>
    <td>Satır tanımındaki <strong>Satır Kod</strong> sütunundaki mali satırlar için ayrı satır kodlarını gösterir. Daha fazla bilgi için bkz. <a href="row-definitions-financial-reporting.md">Finansal raporlamadaki satır tanımları</a>.</td>
    </tr>
    <tr class="odd">
    <td>ACCT (Hesap kodları)</td>
    <td>Her bir satıra uygulanan mali veri segment değerlerini veya boyut değerlerini gösterir. Ayrıntılı hesap ve hareket raporları tam donanımlı bir hesap yazdırılır (örneğin, <strong>110140-070-0101</strong>). Aralıklar, ilişkili bir satır tanımındaki <strong>Mali Boyutlara Bağlantı</strong> sütunu altında tanımlanmadıysa, aralık köşeli parantez içine alınır ve tek bir değer olarak kabul edilir (örneğin, <strong>[110140:110700]-070-[0101:0200]</strong>). Birkaç hesabın bir kombinasyonu olan mali raporlar ve yüksek düzey raporlar için, satır tanımındaki mali veri bağlantısı yazdırılır (örneğin, <strong>1100:1200</strong>).</td>
    </tr>
    <tr class="even">
    <td>FILL</td>
    <td>Hücre tek tırnak işareti içine aldığınız bir karakterle doldurulur. Bir karakter girmezseniz, sütun boş bırakılır. Örneğin, bir sütunu bir üç nokta (...) işaretiyle doldurmak için <strong>DOLDUR</strong> <strong>'.'</strong> girin.</td>
    </tr>
    <tr class="odd">
    <td>SAYFA</td>
    <td>Rapora bir düşey sayfa sonu ekler. <strong>SAYFA</strong> sütununun sağındaki sütunlar farklı bir sayfada görüntülenir.</td>
    </tr>
    <tr class="even">
    <td>WKS</td>
    <td>Bir Excel çalışma sayfasından çekiler veriler görüntülenir. <strong>WKS</strong> sütun türünü seçtiğinizde aşağıdaki satırlar için otomatik olarak varsayılan ayarlar tanımlanır:
    <ul>
    <li><strong>Mali Yıl:</strong> DÖNEMSEL</li>
    <li><strong>Dönem:</strong> TEMEL</li>
    </ul>
    Bu varsayılan ayarları değiştirebilirsiniz.</td>
    </tr>
    <tr class="odd">
    <td>ATTR</td>
    <td>Muhasebe sisteminiz öznitelikleri destekliyorsa, sütunda bir hesap veya hareket özniteliği görüntülenir. Bir tekli tam hesaba uygulanması gereken bir öznitelik, mali verilerden altı çizili hesap veya hareket bilgilerini çeker. Hesap seviyesi öznitelikleri, hesaptan veriyi görüntüler ve hareket seviyesi öznitelikleri, hareket deftere nakledildiğinde oluşan verileri gösterir. Sütun türü olarak <strong>ATTR</strong> seçerseniz, öznitelik kategorisini, sütun tanımının <strong>Kitap Kodu/Öznitelik Kategorisi</strong> ayrıntı satırında belirtin.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Mali Boyutlar sütunu

Aşağıdaki **Sütun Tanımı** satır tanımları, **FD** (Mali boyutlardan çekilen hesaplar) sütun türüne sahip sütunlara uygulanır.

#### <a name="book-codeattribute-category-cell"></a>Defter Kodu/Öznitelik Kategorisi hücresi

**Defter Kodu/Öznitelik Kategorisi** hücresi, **FD** sütunundaki veriler için defter kodunu tanımlar. Bir sütun tanımı birden çok fiili, bütçe ve istatistik sütunu içerebilir. Bir sütun tanımı, geçerli dönem veya yılbaşından bugüne kadar vb. gibi farklı dönemleri ve farklı tutarları da gösterebilir. Defter kodları listesi, mali verilerinizde belirlenen fiili, bütçe ve istatistik (mali olmayan) seçenekleri yansıtır.

#### <a name="fiscal-year-cell"></a>Mali Yıl hücresi

**Mali Yıl** hücresi, sütunun içermesi gereken mali yılı tanımlar. Bu yıl, rapor oluşturulduğunda belirtilen temel yıla göre tanımlanabilir. Aşağıdaki seçenekler mevcuttur.

| Seçenek  | Açıklama                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| TEMEL    | Rapor zamanında belirtilen temel yıl kullanılır.                                                                          |
| TEMEL+\# | Temel yıldan \# yıl sonraki yıl kullanılır. Örneğin, temel yıldan sonraki üçüncü yılı kullanmak istiyorsanız **TEMEL+3** girin. |
| TEMEL\# | Temel yıldan \# yıl önceki yıl kullanılır. Örneğin, geçen yılı kullanmak için **TEMEL-1** girin.                 |
| \#      | Fiili mali yılı girin.                                                                                                |

#### <a name="period-cell"></a>Dönem hücresi

**Dönem** hücresi, sütunun içermesi gereken mali dönemleri tanımlar. Dönem, rapor oluşturulduğunda belirtilen temel döneme göre tanımlanabilir. Aşağıdaki seçenekler mevcuttur.

| Seçenek          | Açıklama                                                                                                                                                                                                                          |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TEMEL            | Temel dönem kullanılır.                                                                                                                                                                                                                 |
| TEMEL+\#         | Temel dönemden \# dönem sonraki dönem kullanılır. Örneğin, temel dönemden sonraki üçüncü dönemi kullanmak istiyorsanız **TEMEL+3** girin.                                                                                               |
| TEMEL\#         | Temel dönemden \# dönem önceki dönem kullanılır. Örneğin, geçen dönemi kullanmak için **TEMEL-1** girin.                                                                                                                 |
| TEMEL\#:TEMEL    | Temel dönemden önceki birkaç dönemden temel döneme kadar, birden fazla dönem kullanılır. Örneğin, önceki üç dönemi ve temel dönemi kullanmak için **TEMEL-3:TEMEL** girin.                                                |
| TEMEL:TEMEL+\#    | Temel dönemden temel dönemden sonraki birkaç döneme kadar, birden fazla dönem kullanılır. Örneğin, temel dönemi ve sonraki iki dönemi kullanmak için **TEMEL:TEMEL+2** girin.                                                  |
| TEMEL-\#:TEMEL+\# | Temel dönemden önceki birkaç dönemden temel dönemden sonraki birkaç döneme kadar, birden fazla dönem kullanılır. Örneğin, önceki üç dönemi, temel dönemi ve sonraki iki dönemi kullanmak için **TEMEL-3:TEMEL+2** girin. |
| 1:TEMEL          | İlk dönemden temel döneme kadar, birden fazla dönem kullanılır.                                                                                                                                                                 |
| \#              | Her zaman belirli bir dönem numarası kullan. Sütun tanımının esnekliğini azalttığından bu seçeneği kullanmanızı önermiyoruz.                                                                                       |
| \#:\#           | Her zaman belirli bir dönem aralığı kullan. Sütun tanımının esnekliğini azalttığından bu seçeneği kullanmanızı önermiyoruz.                                                                                    |

Dönem özelliklerinin herhangi birinde mali yıl sınırlarının ötesine geçebilir ve bir dönem aralığındaki yılları karıştırabilirsiniz. Örneğin dönemi **TEMEL-5** (son altı ayı temsil etmek için) olarak belirtin ve temel dönemi 2 olan bir rapor çalıştırın. Bu durumda, rapor belirtilen mali yılın ilk iki dönemi ve önceki mali yılın son dört dönemi için verileri gösterir.

### <a name="specify-the-periods-for-an-fd-column"></a>Bir FD sütununa ait dönemleri tanımlama

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Bir **FD** sütununda **Dönem** satırındaki hücreyi çift tıklayın ve ardından listeden bir seçenek belirleyin.
3.  Gezinme çubuğunun üzerindeki formül çubuğunda veya **Dönem** hücresinde, formülü tamamlayın. Varsa, sayı işaretlerini (\#) uygun değerle değiştirin.

#### <a name="periods-covered-cell"></a>Kapsanan Dönemler hücresi

**Kapsanan Dönemler** hücresi, sütunun görüntülemesi gereken tutarı tanımlar. Bu tutar, sütunun **Mali Yıl** ve **Dönem** hücrelerindeki değere göre belirlenir. Aşağıdaki seçenekler mevcuttur.

| Seçenek      | Açıklama                                                                 |
|-------------|-----------------------------------------------------------------------------|
| DÖNEMSEL    | Mevcut dönem veya bir dönem aralığı için faaliyetlerin toplamı görüntülenir. |
| DÖNEMSEL/BB | Mevcut dönem veya bir dönem aralığı için başlangıç bakiyesi görüntülenir.   |
| YTD         | Yılbaşından bugüne kadar olan faaliyetlerin toplamı görüntülenir.                               |
| YTD/BB      | Yıl için başlangıç bakiyesi görüntülenir.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Bir FD sütunu için kapsanan dönemleri tanımlama

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Bir **FD** sütununda **Kapsanan Dönemler** satırını çift tıklayın ve listeden bir seçenek belirleyin.

### <a name="attribute-filter-in-a-column-definition"></a>Bir sütun tanımındaki öznitelik filtresi

Öznitelikler bir hesabı veya hareketi daha ayrıntılı şekilde tanımlanan mali veri değerleridir. Hesap özniteliklerine **Kıymet**, **Pasif**, **Gelir** ve **Gider** dahildir. Hareket özniteliklerine **Hareket Açıklaması** ve **Hareket Uygulama Tarihi** dahildir. Öznitelik desteği, Microsoft Dynamics ERP sistemleri arasında farklılık gösterebilir. **Öznitelik Filtresi** hücresi, **FD** sütunlarındaki verileri belirli değerler veya öznitelik kategorisi aralıklarıyla sınırlar. Bu özellik bir **ATTR** sütunuyla birlikte kullanılabilir, ancak **ATTR** sütunu gerekli değildir. Bir **FD** sütununda, raporun öznitelik filtresinden içerebileceği hesap veya hareket sayısında bir sınırlama mevcuttur. **Not:** ERP sisteminizin desteklediği öznitelikleri görmek için, sisteminizin entegrasyon kılavuzuna bakın.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Rapora bir FD sütunu için bir öznitelik filtresi uygulama

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Bir **FD** sütunu için **Öznitelik Filtresi** hücresini çift tıklayın.
3.  **Öznitelik Filtresi** iletişim kutusunda, **Öznitelik** sütunundaki bir hücreyi çift tıklayın ve ardından filtre türünü seçin.
4.  Sonuçları daha fazla sınırlandırmak için **Başlangıç** ve **Bitiş** sütunlarına bir aralık girin. **Başlangıç** hücresi mutlaka bir değer içermelidir.
5.  **Tamam** düğmesini tıklatın.

#### <a name="example-of-an-attribute-filter"></a>Bir öznitelik filtresine örnek

Aşağıdaki örnekte **Defter Kodu/Öznitelik Kategorisi** satırında bir hesap özniteliğine sahip olan bir sütun açıklamasının bir parçası gösterilmiştir. Bu sütun için öznitelik filtresi, rapora dahil edilmek üzere değerlerin aralığını belirler.

|                              | A:    | B:                    |
|------------------------------|------|----------------------|
| Sütun Tipi                  | DESC | FD                   |
| Defter Kodu/Öznitelik Kategorisi |      | FİİLİ               |
| Mali Yıl                  |      | TEMEL                 |
| Dönem                       |      | 1:TEMEL               |
| Kapsanan Dönemler              |      | DÖNEMSEL             |
| ...                          |      |                      |
| Sütun Genişliği                 | 30   |                      |
| ...                          |      |                      |
| Öznitelik Filtresi             |      |  Referans=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Bir sütun tanımındaki boyut filtresi

Bir boyut filtresi, **FD** sütununu belirli boyut değerleriyle sınırlandırmak için kullanılır. Filtre tek bir boyut, bir boyut aralığı veya bir boyut grubu içerebilir. Filtre de boyut değer kümeleri içerebilir. Boyut değerleri değişebilir olduğundan, bir ..\finansal-boyut\ boyut tabanlı bir sistemin tam bir uzunluğa karşılık gelmesine gerek yoktur. Raporun bir raporlama ağacı içerip içermediğinden bağımsız olarak filtre uygulanır. Bir joker karakterini (\* veya?) herhangi bir konumda kullanabilirsiniz. Birden fazla hesap tanımladığınızda, aşağıdaki örnekte gösterildiği gibi hesaplar arasına virgül koyun: +Hesap=\[1200\], +Hesap=\[1100\], Departman=\[01?\] Belirli bir hesap için tüm departmanları almak için, boyut filtresinden Departman boyutunu çıkarabilirsiniz. Örneğin, aşağıdaki boyut filtrelerinin her ikisi de aynı şekilde işlenir:

-   +Hesap=\[1100\],Departman
-   +Hesap=\[1100\]

Ayrıca, tam eşleştirme için alfasayısal karakterlerin herhangi bir kombinasyonunu kullanabilir ve kısmi boyutlar tanımlayabilirsiniz. Örneğin, **Konum = \[10*\*\]**, 10 ile başlayan tüm konum boyutu değerlerini içerir.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Raporda bir sütun için bir boyut filtresi uygulama

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  Bir **FD** sütunu için **Boyut Filtresi** hücresini çift tıklayın.
3.  **Boyutlar** iletişim kutusunda, uygulanacak filtreyi girin.
4.  **Tamam** düğmesini tıklatın.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Bir sütun tanımında birden fazla para birimi içeren bir raporu biçimlendirme

Birden fazla para birimi içeren bir rapor, tutarlar doğal (lokal) para biriminde, işlevsel (varsayılan) para biriminde veya raporlama para biriminde görüntüleyebilir. Bir şirketin işlevsel para birimi, Microsoft Dynamics ERP sisteminde tanımlanır. Bu ERP ayarını işletme sisteminin bölgesel seçenek ayarlarıyla karıştırmayın, ikincisinde raporlarda kullanılan varsayılan para birimi simgeleri yapılandırılabilir. Aşağıdaki, para birimi ile bağlantılı hücreler sütun tanımında kullanılabilir:

-   **Para Birimi Görüntüleme** – Hareketlerin gösterileceği para birimi türünü belirtin (doğal, işlevsel veya raporlama). Bu işlevselliğe bazen para birimi çevirisi de denir. Para birimi çevirisi, genel muhasebe tutarlarının şirketin işlevsel para birimi veya girilen hareketin para birimi dışında bir para biriminde rapor edilebilmesi anlamına gelir.
-   **Para Birimi Filtresi** – Bir para birimi filtresi belirtin. Raporda sadece seçilen para birimi cinsinden girilen hareketler görüntülenir.

**Not:** Birden fazla para birimi kullanan raporlar oluşturmak için **Rapor** sekmesindeki **Tüm raporlama para birimlerini dahil** onay kutusunu işaretlemeniz gerekir. Bir şirketin işlevsel para birimini belirlemek için aşağıdaki adımları izleyin.

1.  Rapor Tasarımcısında **Şirket** menüsündeki **Şirketler** öğesini tıklayın.
2.  **Şirketler** iletişim kutusunda bir şirket seçin ve ardından **Görünüm** öğesini tıklayın.
3.  **Şirketi Göster** iletişim kutusunda **Bölgesel seçenekler** altından, seçilen şirket için tanımlanan para birimini görüntüleyebilirsiniz.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Birden fazla para birimi içeren bir raporda para birimini belirleme

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  İlgili **FD** sütunundaki **Görüntülenen Para Birimi** öğesini çift tıklayın ve para birimi bilgilerinin görüntülenmesi seçeneğini seçin: **Doğal/ilk para birimi**, **Şirket bilgilerinden alınan işlevsel para birimi** veya raporlama para birimi.
3.  İlgili **FD** sütunundaki **Para Birimi Filtresi** hücresini çift tıklayın ve ardından listeden ilgili para birimi kodunu seçin. Raporda sadece bu para biriminde girilen hareketler görüntülenir.

**Not:** Burada açıklanan seçenekler, ERP sistemine bağlı olarak farklılık gösterebilir. Daha fazla bilgi için bkz. [Microsoft ERP sistem belgesine](https://www.microsoft.com/en-us/download/details.aspx?id=5916).

### <a name="example-for-currency-display-and-currency-filter-cells"></a>Görüntülenen Para Birimi ve Para Birimi Filtresi hücrelerine örnek

Phyllis, sütun tanımında aşağıdaki para birimi seçimlerini yapıyor:

-   **Para Birimi Filtresi:** Yen
-   **Görüntülenen Para Birimi:** İşlevsel (ABD Doları)

Phyllis'in seçtiği para birimi filtresi nedeniyle rapor sadece Japon yeni (JPY) cinsinden girilen hareketleri içeriyor. Seçtiği görüntülenen para birimi nedeniyle rapor, hareketleri işlevsel para birimi olan ABD doları (USD) olarak görüntülüyor.

#### <a name="currency-filter-and-currency-display-combinations"></a>Para Birimi Filtresi ve Görüntülenen Para Birimi kombinasyonları

Aşağıdaki tabloda Phyllis'in yaptığı seçimlere bağlı olarak, **Görüntülenen Para Birimi** ve **Para Birimi Filtresi** hücrelerindeki seçeneklerin çeşitli kombinasyonları için ortaya çıkabilecek sonuçlar gösterilmiştir. İşlevsel para birimi ABD dolarıdır.

| Görüntülenen Para Birimi hücresi                        | Para Birimi Filtresi hücresi | Rapor sonucu                                                                                                                                                                                    |
|----------------------------------------------|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Doğal/ilk para birimi                 | **YEN**              | **Y6,000** – Sonuç sadece JPY cinsinden girilen hareketleri gösterir.                                                                                                                        |
| Şirket bilgilerinden işlevsel para birimi | **YEN**              | **$60** – Sonuç sadece JPY cinsinden girilen hareketleri gösterir ve bu hareketleri Amerikan Doları cinsinde görüntüler. **Not:** Döviz kuru 1 Amerikan Doları için yaklaşık 100 JPY'dir.                    |
| Şirket bilgilerinden işlevsel para birimi | Boş                | **$2.310\*\*** – Sonuç tüm verileri şirket bilgilerinde belirtilen işlevsel para biriminde gösterir. **Not:** Bu tutar, tüm hareketlerin işlevsel para birimindeki toplamıdır. |
| Doğal/ilk para birimi                 | Boşalt                | **$2,250** – Sonuç tüm tutarları hareketin gerçekleştirildiği para biriminde gösterir.                                                                                                 |

### <a name="calculation-column-in-a-column-definition"></a>Bir sütun tanımındaki hesaplama sütunu

Bir sütun tanımındaki bir **CALC** sütun türü, **Formül** hücresinde karmaşık hesaplamaları destekler ve **+**, **-**, **\***, ve **/** operatörlerini ve ayrıca **IF/THEN/ELSE** deyimlerini içerebilir. Bir hesaplama sütunu, daha sonraki sütunları da dahil, herhangi diğer bir sütuna başvurabilir. Ayrıca, bir hesaplama sütunu, sütun üstbilgisini desteklemek üzere mali yılı ve dönemi de içine alabilir. Hesaplama formülünün uzunluğu 1,024 karaktere kadar olabilir.  Hesaplama sonucunu bir yüzde olarak ifade etmek için özel bir biçim atlatma seçeneği kullanın. **Not:** Hesaplama formüllerinin sonuçları, yazdırılmayan sütun aralıklarındaki değerleri içermez. Örneğin, **A:D** seçeneği **0** (sıfır) değerini yazdırırken, yazdırılmayan değerler için **A+B+C** seçeneği değeri hesaplar.

#### <a name="operators-in-calculation-columns"></a>Hesaplama sütunlarındaki işleçler

Sütunları toplamak, çıkarmak, çarpmak veya bölmek için sütun harflerini hesaplama sırasıyla girin ve ardından her bir sütun harfini ayırmak için uygun işleci kullanın. Aşağıdaki tabloda bir hesaplama sütununda kullanılabilecek işleçler açıklanmıştır.

| İşleç | Örnek hesaplama | Açıklama                                                                                                                                                                                                                                    |
|----------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| +        | A+C                 | A sütunundaki tutarı C sütunundaki tutara ekleyin.                                                                                                                                                                                          |
| :        | A:C A:C-D           | Birbirini takip eden bir seri sütun ekleyin. Örneğin, **A:C** formülü, A ile C arasındaki sütunların toplamlarını eklerken, **A:C-D** formülü, A ile C arasındaki sütunların toplamlarını ekler ve ardından D sütunundaki tutarı çıkarır.                          |
| -        | A-C                 | A sütunundaki tutarı C sütunundaki tutardan çıkarın. **Not:** Bir sütundaki işareti ters çevirmek için eksi (-) işaretini de kullanabilirsiniz. Örneğin, A sütunundaki tutarın tersini B sütunundaki tutara eklemek için **-A+B** formülü kullanın. |
| \*       | A\*C                | A sütunundaki tutarı C sütunundaki tutara çarpın.                                                                                                                                                                                     |
| /        | A/C                 | A sütunundaki tutarı C sütunundaki tutara bölün.                                                                                                                                                                                       |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Bir sütun tanımında bir hesaplama formülü kullanma

1.  Rapor Tasarımcısında değiştirmek istediğiniz sütun tanımını açın.
2.  İlgili**CALC** sütununda **Formül** hücresine bir formül girin.

#### <a name="complex-calculations"></a>Kompleks hesaplamalar

Bir kompleks hesaplama hücre başvuruları, işleçler, değerler ve iç içe girmiş parantez düzeylerinin herhangi bir kombinasyonunu içerebilir. Örneğin, A ve B sütunlarının ortalamasını hesaplamak için **((A+B)/2)** hesaplama formülünü kullanın.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Bir sütun hesaplamasında rapor hücreleri tanımlama

Bir sütun harfi ve bir satır kodu girerek belirli bir rapor hücresine başvurabilirsiniz. Örneğin, **B.100**, B sütunundaki 100 satır koduna karşılık gelir. Tüm bir sütunu, aynı sütunda olan belirli bir rapor hücresi tutarına göre bölebilirsiniz. Örneğin, **B/B.100** hesaplaması, B sütunundaki tutarın B sütunundaki 100 satır kodundaki değere bölüneceği anlamına gelir. Hesaplama, başka bir sütuna dayalı bir sütuna başvuruyorsa, öncelikle bağlı sütun çözümlenir. Bir sütun tekrar birinci sütuna başvuran, başka bir sütuna başvuruyorsa, bu durum bir döngüsel başvuru hatasına neden olur. **Not:** Rapor için hesaplama önceliğini değiştirirseniz, hesaplama yanlış olabilir. Hesaplama önceliğini rapor tanımının **Ayarlar** sekmesinden ayarlayabilirsiniz.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Bir sütunu bir temel satırla çarpma veya bir temel satıra bölme

Belirtilen bir sütundaki tüm değerleri bir temel rakamın yüzdesi olarak görüntüleyen bir sütun oluşturabilirsiniz. Bu nedenle, bir satış satırının yüzdesi veya bir toplam giderler satırının yüzdesi vb. gibi, satırlar arasındaki ilişkileri gösterebilirsiniz. Belirli bir sütundaki her bir satırı bir temel satırla çarpmak veya bir temel satıra bölmek için, hesaplamada kullanılacak sütunu girin ve ardından **\*BASEROW** veya **BASEROW** seçimini yapın. Örneğin, **C\*BASEROW** veya **C/BASEROW** girin. **Not:** Bir sütun tanımında bir temel satır hesaplaması kullanıyorsanız bu sütun tanımıyla kullanılan her bir satır tanımının, hesaplamalar için en az bir temel satır içerdiğinden emin olun. 

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Bir sütundaki tutarı dönem sayısına bölme

Bir sütundaki tutarı belirli bir dönem sayısına bölebilirsiniz. Örneğin, **B/Dönemler** formülü, B sütunundaki değeri B sütunundaki dönemlerin sayısına böler. Hesaplama birden fazla sütunu kapsıyorsa hesaplamada kullanılacak dönem sayısını belirtin. Örneğin, **(B+C)/Dönemler** formülü, B ve C sütunundaki tutarları toplar ve ardından sonucu dönem değerine böler.

<a name="see-also"></a>Ayrıca bkz.
--------

[Finansal raporlamada satır tanımları](row-definitions-financial-reporting.md)

[Finansal raporlamada gelişmiş biçimlendirme seçenekleri](advanced-formatting-options-financial-reporting.md)


