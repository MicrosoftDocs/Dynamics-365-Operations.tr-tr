---
title: "Satır tanımı hücrelerini değiştirme"
description: "Bu makalede bir finansal raporun satır tanımındaki tüm hücreler için gerekli olan bilgiler ve bu bilgilerin nasıl girileceği açıklanmaktadır."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 16 - 09 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: b61364c9055e5c5a63592c7f05551d0c145924b9
ms.lasthandoff: 03/29/2017


---

# <a name="modify-row-definition-cells"></a>Satır tanımı hücrelerini değiştirme

Bu makalede bir finansal raporun satır tanımındaki tüm hücreler için gerekli olan bilgiler ve bu bilgilerin nasıl girileceği açıklanmaktadır. 

# <a name="specify-a-row-code-in-a-row-definition"></a>Bir satır tanımında bir satır kodu belirleme

Satır tanımlarında, **Satır Kodu** hücresindeki rakamlar veya etiketler, satır tanımındaki her bir satırı tanımlar. Hesaplamalardaki ve toplamalardaki verilere başvurmak için satır kodunu belirtebilirsiniz.

### <a name="row-code-requirements"></a>Satır kodu gereksinimleri

Tüm satırlar için bir satır kodu gereklidir. Bir satır tanımında sayısal, alfasayısal ve ayarlanmamış (boş) satır kodlarını karıştırabilirsiniz. Satır kodu herhangi bir pozitif tamsayı (100.000.000'in altında) veya bu satırı tanımlayan bir açıklama etiketi olabilir. Açıklayıcı etiket mutlaka şu kurallara uygun olmalıdır:

-   Etiket mutlaka bir alfabetik karakterle (a'dan z'ye veya A'dan Z'ye) başlamalıdır ve 16 karaktere kadar herhangi bir rakam ve harf kombinasyonundan meydana gelebilir. **Not:** etiket alt çizgi karakterini içerebilir (\_), ancak herhangi bir özel karakterlere izin verilmez.
-   Etiket aşağıdaki ayrılmış sözcüklerden hiçbirini içermez: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO veya RPO.

Aşağıdaki örnekler, geçerli satır kodlarıdır:

-   320
-   TL\_NET\_gelir
-   TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Bir satır tanımındaki bir satır kodunu değiştirme

1.  Rapor Tasarımcısında **Satır Tanımları** öğesine tıklayın ve ardından değiştirmek için satır tanımını açın.
2.  İlgili satırda **Satır Kodu** sütunundaki hücreye yeni bir değer girin.

### <a name="reset-numeric-row-codes"></a>Nümerik satır kodlarını sıfırlama

1.  Rapor Tasarımcısında **Satır Tanımları** öğesini tıklayın ve ardından değiştirmek için satır tanımını açın.
2.  **Düzenle** menüsünde **Satırları Yeniden Numaralandır** öğesini tıklayın.
3.  **Satırları Yeniden Numaralandır** iletişim kutusunda, başlangıç satır kodu ve satır kodu artışı için yeni değerler belirleyin. Nümerik satır kodlarını birbirine eşit değerlere sıfırlayabilirsiniz. Ancak, rapor tasarımcısı sadece rakamla başlayan satır kodlarını (örneğin 130 veya 246) yeniden numaralandırır. Harfleri ile başlayan satır kodlarını yeniden numaralandırmak değildir (örneğin, gelir\_93 veya TP0693). **Not:** Satır kodlarını yeniden numaralandırdığınızda rapor tasarımcısı **TOT** ve **CAL** referanslarını otomatik olarak güncelleştirir. Örneğin, bir **TOT** satırı, 100 satır kodu ile başlayan bir aralığa karşılık geliyorsa ve satırları 90'dan başlayarak yeniden numaralandırırsanız, başlangıç**TOT** referansı 100'den 90'a değişir.

## <a name="add-a-description"></a>Bir açıklama ekle
Açıklama hücresi, örneğin "Gelir" veya "Net Gelir" gibi rapor satırındaki mali verilerin açıklamalarını içerir. **Açıklama** hücresindeki metin, satır tanımına girdiğinizde raporda tam olarak görüntülenir. **Not:** Açıklama sütununun rapordaki genişliği sütun tanımı altından ayarlanır. **Açıklama** sütununda, satır tanımındaki metin uzunsa **DESC** sütununun genişliğini doğrulayın. **Satır Ekle** iletişim kutusunu kullandığınızda, **Açıklama** sütunu altındaki değerler, mali verilerden alınan segment değerleri veya boyut değerleridir. Bölüm başlığı veya bölümün toplamı gibi açıklayıcı metin ve bir toplam satırından önce bir satır vb. gibi biçimlendirme kuralları eklemek üzere satır ekleyebilirsiniz. Rapor bir raporlama ağacı içeriyorsa, raporlama ağacındaki raporlama birimleri için tanımlanan ilave metinleri dahil edebilirsiniz. Ayrıca, ilave metni belirli bir raporlama birimiyle sınırlayabilirsiniz.

### <a name="add-the-description-for-a-line-on-a-report"></a>Bir rapordaki bir satır için açıklama ekleme

1.  Rapor Tasarımcısında **Satır Tanımları** öğesini tıklayın ve ardından değiştirmek için satır tanımını açın.
2.  **Açıklama** hücresini seçin ve ardından rapor satırının adını girin.
3.  Biçimlendirme uygulayın.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Açıklamaya bir raporlama ağacından ilave metin ekleme

1.  Rapor Tasarımcısında **Satır Tanımları** öğesini tıklayın ve ardından değiştirmek için satır tanımını açın.
2.  İlave metin kodunu ve diğer metinleri ilgili **Açıklama** hücresine girin.
3.  Biçimlendirme uygulayın.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>İlave metni belirli bir raporlama birimiyle sınırlandırma

1.  Rapor Tasarımcısında **Satır Tanımları** öğesini tıklayın ve ardından değiştirmek için satır tanımını açın.
2.  İlave metnin oluşturulması gereken satırı bulun ve ardından **İlgili Formüller/Satırlar/Birimler** sütunundaki hücreyi çift tıklayın.
3.  **Raporlama Birimi Seçimi** iletişim kutusundaki **Raporlama ağacı** alanından bir raporlama ağacı seçin.
4.  **Kısıtlama için raporlama birimi seç** alanında, raporlama ağacını genişletin veya daraltın ve ardından bir raporlama birimi seçin.

## <a name="add-a-format-code"></a>Bir biçim kodu ekleme
**Biçim Kodu** hücresi, ilgili satır içeriği için önceden biçimlendirilmiş seçeneklerden oluşan bir seçim sunar. **Biçim Kodu** hücresi boşsa, satır bir mali veri ayrıntı satırı olarak yorumlanır. **Not:** Bir rapor, baskılanan tutar satırlarıyla bağlantılı, tutar içermeyen biçimlendirme satırları içeriyorsa (örneğin, sıfır bakiyeler nedeniyle), başlık ve biçim satırlarının yazdırılmaması için **İlgili Formüller/Satırlar/Birimler** sütununu kullanabilirsiniz.

### <a name="add-a-format-code-to-a-report-row"></a>Bir rapor satırına bir biçim kodu ekleme

1.  Report Designer'da **Satır Tanımları** öğesini tıklayın ve ardından değiştirilecek satır tanımını seçin.
2.  **Biçim Kodu** hücresini çift tıklayın.
3.  Listeden bir biçim kodu seçin. Aşağıdaki tabloda biçim kodları ve eylemleri açıklanmıştır.
    | Biçim kodu                   | Biçim kodunun yorumlanması | Eylem|
    |---|---|---|
    | (Yok)                        |                                    | **Biçim Kodu** hücresini temizler.                                                                                                                                                                               |
    | TOT                           | Toplam                              | **İlgili Formüller/Satır/Birim** sütununda matematiksel işleçler kullanan bir satırı belirtir. Toplamları içeren basit işleçleri gibi **+**veya**-**.                                                      |
    | CAL                           | Hesaplama                        | **İlgili Formüller/Satır/Birim** sütununda matematiksel işleçler kullanan bir satırı belirtir. Hesaplamaları içeren karmaşık işleçleri gibi **+**, **-**, **\***, **/**, ve **o/IF/ELSE** ifadeleri. |
    | DES                           | Açıklama                        | Bir rapordaki başlık satırını veya boş bir satırı tanımlar.                                                                                                                                                        |
    | LFT RGT CEN                   | Sol Sağ Orta                  | Metnin sütun tanımındaki yerleşimine bakılmaksızın, rapor sayfasında satır tanımını metnini hizalar.                                                                                               |
    | CBR                           | Değişiklik Temel Satırı                    | Sütun hesaplamaları için temel satırı ayarlayan bir satırı tanımlar.                                                                                                                                               |
    | SÜTUN                        | Sütun sonu                       | Raporda yeni bir sütun başlatır.                                                                                                                                                                             |
    | SAYFA                          | Sayfa sonu                         | Raporda yeni bir sayfa başlatır.                                                                                                                                                                               |
    | ---                           | Tek alt çizgi                   | Rapordaki tüm tutar sütunlarını tek altı çizili hale getirir.                                                                                                                                                     |
    | ===                           | Çift alt çizgi                   | Rapordaki tüm tutar sütunlarını çift altı çizili hale getirir.                                                                                                                                                     |
    | ÇiZGi1                         | İnce çizgi                          | Sayfa boyunca tek bir ince çizgi çizer.                                                                                                                                                                      |
    | ÇiZGi2                         | Kalın çizgi                         | Sayfa boyunca tek bir kalın çizgi çizer.                                                                                                                                                                     |
    | ÇiZGi3                         | Kesikli çizgi                        | Sayfa boyunca tek bir kesikli çizgi çizer.                                                                                                                                                                    |
    | ÇiZGi4                         | Kalın çizgi ve ince çizgi           | Sayfa boyunca iki çizgi çizer. Üst çizgi kalın ve alt çizgi incedir.                                                                                                                       |
    | ÇiZGi5                         | İnce çizgi ve kalın çizgi           | Sayfa boyunca iki çizgi çizer. Üst çizgi incedir ve alt çizgi kalındır.                                                                                                                       |
    | BXB BXC                       | Kutuyla çevrilmiş satır                          | **BXB** satırı ile başlayan ve **BXC** satırı ile biten rapor satırlarının etrafını kutuyla çevirir.                                                                                                               |
    | REM                           | Açıklama                             | Bir yorum satırı olan ve raporda yazdırılmaması gereken bir satırı tanımlar. Örneğin, bir hatırlatma satırı, biçimlendirme tekniklerini açıklıyor olabilir.                                                            |
    | SIRALAMA SORTDESC ASORTDESC | Sırala                               | Harcamaları veya gelirleri sıralar, bir fiili veya bütçe farkı raporunu en büyük farka göre sıralar veya sıra tanımlarını alfabetik olarak sıralar.                                                                   |

## <a name="specify-related-formulasrowsunits"></a>İlgili formülleri/satırları/birimleri tanımla
**İlgili Formüller/Satırlar/Birimler** hücresi birden fazla amaca sahiptir. Bir**İlgili Formüller/Satırlar/Birimler** hücresi, satır türüne bağlı olarak aşağıdaki işlevlerden birini yerine getirebilir:

-   Bir **TOT** biçim kodu veya bir **CAL** biçim kodu kullandığınızda bir hesaplamaya dahil edilecek satırları tanımlayın.
-   Biçimlendirmenin sadece ilgili tutar yazdırıldığında yazdırılması için bir tutar satırıyla bir biçimlendirme satırı ilişkilendirin.
-   Bir satırı belirli bir raporlama birimiyle sınırlandırın.
-   **BASEROW** biçim kodu kullandığınızda hesaplamalar için temel satırı tanımlayın.
-   Herhangi bir sıralama biçim kodu kullandığınızda sıralanacak satırları tanımlayın.

### <a name="use-a-row-total-in-a-row-definition"></a>Bir satır tanımında bir satır toplamı kullanma

Başka satırlara tutar eklemek veya başka satırlardan tutar çıkarmak için bir satır toplam formülü kullanın. Bir satır toplamının oluşturulması için formül, ayrı satır kodlarını ve aralıklarını birleştirmek üzere + ve - işleçlerini içerebilir. Aralıklar, iki nokta üst üste (:) ile belirtilir. Formül, 1.024 karaktere kadar içerebilir. Burada standart bir toplama formülüne örnek verilmiştir: 400+420+430+450+460BORÇLAR+ÖZ VARLIK520:546520:546-BORÇLAR

### <a name="components-of-a-row-total-formula"></a>Bir satır toplam formülünün bileşenleri

Bir satır toplam formülü oluşturduğunuzda, mevcut satır tanımına hangi satırların ekleneceğini veya mevcut satır tanımından hangi satırların çıkarılacağını belirlemek için yeni kodlar kullanmanız ve satırların nasıl birleştirileceğini tanımlamak için işleçlerden yararlanmanız gerekir. Toplam satırları ve tutar satırları herhangi bir kombinasyonda kullanılabilir. **Not:** Bir aralıkta bulunan tüm toplam satırları hariç tutulur. Bir genel toplam oluşturmak için satır aralığını belirtebilirsiniz. Bir aralığın ilk satırı bir toplam satırı ise, bu satır yeni toplama dahil edilir. Aşağıdaki tabloda işleçlerin satır toplam formüllerinde nasıl kullanıldığı açıklanmıştır.

| İşleç | Örnek formül | Açıklama                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | 100 satırındaki tutarı 330 satırındaki tutara ekler.        |
| :        | 100:330         | Tüm satırların toplamlarını 100 satırı ile 330 satırı arasına ekler.    |
| -        | 100-330         | 100 satırındaki tutarı 330 satırındaki tutardan çıkarır. |

### <a name="create-a-row-total"></a>Bir satır toplamı oluşturma

1.  Rapor Tasarımcısında **Satır Tanımları** öğesini tıklayın ve ardından değiştirmek için satır tanımını açın.
2.  Satır tanımındaki **Biçim Kodu** hücresini çift tıklayın ve **TOT** öğesini seçin.
3.  **İlgili Formüller/Satırlar/Birimler** hücresine toplam formülü girin.

### <a name="relate-a-format-row-to-an-amount-row"></a>Bir format satırını bir tutar satırıyla ilişkilendirme

İçinde **biçim kodu** bir satır tanımındaki bir sütun **DES**, **LFT**, **HİZALA**, **CEN**, **---**, ve **===**biçim kodları tutarı satır için biçimlendirmeyi uygulayın. İlgili tutar satırları baskılandığında (örneğin, tutar satırlarının sıfır değerleri içermesi veya dönem faaliyeti içermemesi nedeniyle) format satırlarını ilgili tutar satırlarıyla ilişkilendirmeniz gerekir. Bu özellik, dönem için yazdırılacak ayrıntı bulunmuyorsa alt toplamlarla ilgili başlıkların veya biçimlendirmenin yazdırılmasını önlemek istediğiniz durumlarda kullanışlıdır. **Not:** Ayrıca, satırları tutarlar olmadan görüntülemek için seçeneği temizleyerek, ayrıntılı tutar satırlarının yazdırılmasını engelleyebilirsiniz. Bu seçenek, rapor tanımının **Ayarlar** sekmesinde bulunur. Varsayılan olarak, bir sıfır bakiyesine sahip olan veya dönem faaliyetine sahip olmayan hareket ayrıntı tutarları raporlarda baskılanır. Bu hareket ayrıntı hesaplarını göstermek için, rapor tanımının **Ayarlar** sekmesindeki **Satırları tutarlar olmadan göster** onay kutusunu işaretleyin.

### <a name="relate-a-format-row-to-an-amount-row"></a>Bir format satırını bir tutar satırıyla ilişkilendirme

1.  Report Designer'da **Satır Tanımları** öğesini tıklayın ve ardından değiştirilecek satır tanımını seçin.
2.  Biçimlendirme satırında, **İlgili Formüller/Satırlar/Birimler** hücresinde baskılanacak tutar satırının satır kodunu girin. **Not:** Bir tutar satırını baskılamak için satır bakiyesi mutlaka 0 (sıfır) olmalıdır. Bakiyesi olan bir tutar satırı baskılanmaz.
3.  **Dosya** menüsünden **Kaydet** düğmesini tıklayın.

### <a name="example-of-preventing-printing-of-rows"></a>Satırların yazdırılmasının önlenmesine örnek

Aşağıdaki örnekte Phyllis raporun başlığının ve **Toplam Nakit** satırındaki alt çizgilerin yazdırılmasını engellemek istiyor, çünkü nakit tutarlarının hiçbirinde faaliyet bulunmuyor. Bu nedenle, sıradaki 220 (, olarak **---**biçim kodu gösterir, biçimlendirme satırın), **ilgili formüller/satır/birim** hücre, Filiz girer **250**, Filiz bastırmak için istediği tutarı Satır satır kodu olduğu. [![RelatedRowsRowDefinition](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Bir sütun hesaplaması için temel satır seçme
İlişkisel raporlamada, satır tanımında **CBR** (temel satırı değiştir) biçim kodunu kullanarak bir veya daha fazla sayıda temel satır atayabilirsiniz. Temel satıra daha sonra sütun tanımındaki bir hesaplama tarafından başvurulur. Burada CBR hesaplamaları için bazı tipik örnekler verilmiştir:

-   Bireysel gelir maddelerle ilişkili toplam gelir yüzdesi
-   Bireysel harcama maddelerle ilişkili toplam harcama yüzdesi
-   Bölüm veya departman ayrıntılarıyla ilişkili brüt kar yüzdesi.

Satır tanımında bir veya daha fazla sayıda temel satır tanımlanır ve ardından sütun tanımı, temel satırın raporlanacağı ilişkiyi belirler. Sütun formülünde **BASEROW** kodu kullanılmaktadır. **BASEROW** ile birlikte şu temel matematiksel işlemler kullanılır: çarpma, bölme, toplama ve çıkarma. En sık kullanılan işlem, **BASEROW** ile bölümdür ve sonuç bir yüzde olarak gösterilir. Formülde **BASEROW** kullanan sütun hesaplamaları, ilgili temel satır kodları için satır tanımını kullanır.  **CBR** satırları şu özelliklere sahiptir:

-   **CBR** satırları, tamamlanan rapora yazdırılmaz.
-   **CBR** biçim kodu ve bununla ilişkili kod, ilgili hesaplamaları gösteren satırın veya bölümün üstüne yerleştirilir.

Sütun tanımında **CALC** sütun türü, **Formül** satırında bir formül gösteren bir sütunu belirtir. Bu formül, raporun bu sütunu için verilere dayalı olarak çalışır ve satırdaki **CBR** biçim kodlarıyla ilgili temel hesaplamalar için Baserow anahtar kelimesini kullanır. Satır tanımında **CBR** biçim kodu, rapordaki her bir satır için temel satırın bir yüzdesini veya çarpımını hesaplayan sütunlar için temel satırı tanımlar. Örneğin bir tanesi net satışlar, bir tanesi brüt satışlar ve biri toplam giderler olmak üzere bir satır formatında birden fazla **CBR** biçim koduna sahip olabilirsiniz. Genellikle, **CBR** biçim kodu, bir toplam satırı ile karşılaştırılan hesaplar için bir yüzde oluşturmak için kullanılır. Bir temel satır, başka bir temel satır tanımlanana kadar tüm hesaplamalar için kullanılır. Bir başlangıç **CBR** biçim kodu ve bir bitiş **CBR **biçim kodu tanımlamanız gerekir. Örneğin, giderleri net satışların bir yüzdesi olarak belirlemek için, her bir gider satırındaki değeri net satışlar satırındaki değere bölebilirsiniz. Bu durumda net satılar satırı temel satırdır. Aşağıdaki örnekte gösterildiği gibi, mevcut ve yılbaşından bugüne sonuçlarını ve her bir sonucun bir temel yüzdesini raporlayan bir sütun tanımı oluşturabilirsiniz. Ayrıntılı bir gelir tablosu ile başlayın.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Bir sütun hesaplaması için bir satır tanımındaki temel satırı seçin.

1.  Report Designer'da **Sütun Tanımları** öğesini tıklayın ve ardından bir gelir tablosu için sütun tanımını açın.
2.  Sütun tanımına yeni bir sütun ekleyin ve sütun türünü **CAC** olarak ayarlayın.
3.  Yeni sütunun **Formül** hücresine **X/BASEROW** formülünü girin; burada **X**, yüzde olarak görüntülenecek **FD** sütun türünü ifade eder.
4.  **Biçim/Para Birimi Atlatma** hücresini çift tıklayın.
5.  **Biçimi Atlatma** iletişim kutusunda, **Biçim Kategorisi** listesinden **Yüzde** öğesini seçin ve **Tamam** öğesini tıklayın.
6.  **Dosya** menüsünde, sütun tanımını yeni bir adla kaydetmek için **Farklı Kaydet** öğesini tıklayın. Append **CBR** için geçerli bir dosya adı (örneğin, **ven\_Yılbaşından BUGÜNE\_CBR**). Bu sütun tanımı, temel satır sütunu tanımınızdır.
7.  Report Designer'da **Satır Tanımları** öğesini tıklayın ve ardından temel satır hesaplamasını kullanarak değiştirmek istediğiniz satır tanımını açın.
8.  Temel satır hesaplamasının başlaması gereken satırın üzerine yeni bir satır ekleyin.
9.  Satır tanımındaki **Biçim Kodu** hücresini çift tıklayın ve ardından **CBR** öğesini seçin.
10. **İlgili Formüller/Satırlar/Birimler** hücresine temel satır için satır kodu numarasını girin.

### <a name="example-of-base-row-calculation"></a>Temel satır hesaplamasına örnek

Aşağıdaki satır tanımı örneğinde, 100 satırı, hesaplamalar için temel satırın 280 olduğunu gösterir. [![Temel satır hesaplama örneği.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png) Aşağıdaki sütun tanımı örneğinde hesaplamalar **CBR** biçim kodunu kullanır. C sütunundaki hesaplama, raporun B sütunundaki değeri B sütununun 280 satırındaki değere böler. B sütunundaki biçim atlatma, hesaplama sonucunu bir yüzde olarak yazdırır. Benzer şekilde, E sütunundaki her bir tutar, net satışların bir yüzdesi olarak D sütunundaki tutardır. [![Sütun tanımı örneği.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png) Aşağıdaki örnekte önceki hesaplamalara göre oluşturulabilecek bir rapor gösterilmiştir. [![Önceki örnek hesaplamalara göre örnek raporu.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Bir satır tanımı için bir sıralama kodu seçin.
Sıralama kodları hesapları veya değerleri sıralar, bir fiili veya bütçe farkı raporunu en büyük farka göre sıralar veya satır tanımlarını alfabetik olarak sıralar. Aşağıdaki sıralama kodları mevcuttur:

-   **SORT** – Raporu belirtilen sütundaki değerlere dayalı olarak artan sırada sıralar.
-   **ASORT** – Raporu belirtilen sütundaki değerlerin mutlak değerlerine dayalı olarak artan sırada sıralar. Diğer bir deyişle, değerler sıralanırken değerlerin işaretleri dikkate alınmaz. Bu biçim kodu, farkın pozitif veya negatif olup olmamasından bağımsız olarak değerleri fark büyüklüğüne göre sıralar.
-   **SORTDESC** – Raporu belirtilen sütundaki değerlere dayalı olarak azalan sırada sıralar.
-   **ASORTDESC** – Raporu belirtilen sütundaki değerlerin mutlak değerlerine dayalı olarak azalan sırada sıralar.

### <a name="select-a-sorting-code"></a>Bir sıralama kodu seçin

1.  Rapor Tasarımcısında **Satır Tanımları** öğesini tıklayın ve ardından değiştirmek için satır tanımını açın.
2.  **Biçim Kodu** hücresini çift tıklayın ve ardından bir sıralama kodu seçin.
3.  **İlgili Formüller/Satırlar/Birimler** hücresinde sıralanacak satır kodlarının aralığını belirtin. Bir aralık belirlemek için ilk satır kodunu, bir iki nokta üst üste işareti (:) ve ardından son satır kodunu girin. Örneğin, aralığın 160 satırından 490 satırına kadar olduğunu belirtmek için **160:490** değerini girin.
4.  **Sütun Kısıtlama** hücresinde sıralama için kullanılacak rapor sütunu harfini girin. **Not:** Bir satır hesaplamasına sadece tutar satırlarını dahil edin.

### <a name="examples-of-ascending-and-descending-column-values"></a>Artan ve azalan sütun değerlerine örnekler

Aşağıdaki örnekte, rapor D sütunundaki değerler 490 ile 160 satırlar için artan düzende sıralanır. Ayrıca, G sütununda raporun mutlak değerler satırların 610 940 yoluyla azalan düzende sıralanır.

| Satır Kodu | Açıklama                                         | Biçim Kodu | İlgili Formüller/Satırlar/Birimler | Normal Bakiye | Sütun Kısıtlama | Mali Boyutlarla İlişkilendirme |
|----------|-----------------------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Aylık Farka Göre Artan Sırada Sıralanır       | DES         |                             |                |                    |                              |
| 130      |                                                     | SORT        | 160:490                     |                | B                  |                              |
| 160      | Satışlar                                               |             |                             | A              |                    | 4100                         |
| 190      | Satış İadeleri                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 490      | Faiz Geliri                                     |             |                             | A              |                    | 7000                         |
| 520      |                                                     | DES         |                             |                |                    |                              |
| 550      | YTD Mutlak Farkına Göre Azalan Sırada Sıralanır | DES         |                             |                |                    |                              |
| 580      |                                                     | ASORTDESC   | 610:940                     |                | G:                  |                              |
| 610      | Satışlar                                               |             |                             | A              |                    | 4100                         |
| 640      | Satış İadeleri                                       |             |                             |                |                    | 4110                         |
|          | ...                                                 |             |                             |                |                    |                              |
| 940      | Faiz Geliri                                     |             |                             | A              |                    | 7000                         |

Burada oluşturulan rapora bir örnek verilmiştir.

**Fark Analizi (Farka Göre Sıralanmış)**

**Beijing ve Atlanta Bölgeleri**

**31 Temmuz 2013 Tarihinde Biten Yedi Ay için**

**Temmuz**

**YTD**

**Fiili**

**Bütçe**

**Fark**

**Fiili**

**Bütçe**

**Fark**

**Aylık Farka Göre Artan Sırada Sıralanır**

SMM

873.872

236.144

(637.728)

4.864.274

1.590.315

(3.273.959)

Maaşlar ve Ücretler

97.624

65.573

(32.051)

653.884

441.664

(212.220)

Satış İskontoları

36.383

24.152

(12.231)

241.562

162.670

(78.892)

Satış İadeleri

10.917

7.246

(3.671)

62.809

48.803

(14.006)

Kira Gideri

12.052

9.019

(3.033)

80.444

60.748

(19.696)

Ofis Gideri

5.023

3.291

(1.732)

33.420

22.098

(11.322)

Seyahat Gideri

7.656

7.641

(15)

51.062

51.469

407

Satışlar

1.240.119

410.389

829.730

7.139.288

2.764.549

4.374.739

**YTD Mutlak Farkına Göre Azalan Sırada Sıralanır**

Satışlar

1.240.119

410.389

829.730

7.139.288

2.764.549

4.374.739

Seyahat Gideri

7.656

7.641

(15)

51.062

51.469

407

Ofis Gideri

5.023

3.291

(1.732)

33.420

22.098

(11.322)

Satış İadeleri

10.917

7.246

(3.671)

62.809

48.803

(14.006)

Kira Gideri

12.052

9.019

(3.033)

80.444

60.748

(19.696)

Satış İskontoları

36.383

24.152

(12.231)

241.562

162.670

(78.892)

Maaşlar ve Ücretler

97.624

65.573

(32.051)

653.884

441.664

(212.220)

SMM

873.872

236.144

(637.728)

4.864.274

1.590.315

(3.273.959)

## <a name="specify-a-format-override-cell"></a>Bir Biçim Atlatma hücresi tanımlama
**Biçim Atlatma** hücresi, rapor yazdırıldığında satır için kullanılan biçimlendirmeyi belirtir. Bu biçimlendirme, sütun tanımında ve rapor tanımında belirtilen biçimlendirmeyi geçersiz kılar. Varsayılan olarak, bu tanımlarda belirtilen biçimlendirme para birimidir. Raporun bir satırı, bina sayısı gibi kıymetlerin sayısını listeliyorsa ve başka bir satırı bu kıymetlerin parasal değerini listeliyorsa para birimi biçimlendirmesini atlatabilir ve binaların sayısını belirleyen satır için nümerik biçimlendirmeyi girebilirsiniz. Bu bilgileri **Biçim Atlatma** iletişim kutusunda belirtirsiniz. Kullanılabilir seçenekler, seçtiğiniz biçim kategorisine bağlıdır. İletişim kutusunun **Örnek** alanında örnek biçimler gösterilir. Aşağıdaki biçim kategorileri kullanılabilir:

-   Para birimi biçimlendirmesi
-   Nümerik biçimlendirme
-   Yüzde biçimlendirmesi
-   Özel biçimlendirme

### <a name="override-cell-formatting"></a>Hücre biçimlendirmesini atlatma

1.  Rapor Tasarımcısında değiştirilecek satır tanımını açın.
2.  Biçimin atlatılacak satırda **Biçimi Atlat** sütunundaki hücreyi çift tıklayın.
3.  **Biçim Atlatma** iletişim kutusunda rapordaki bu satır için kullanılacak biçimlendirme seçeneklerini belirleyin.
4.  **Tamam** düğmesini tıklatın.

### <a name="currency-formatting"></a>Para birimi biçimlendirmesi

Para birimi biçimlendirmesi bir mali bir tutara uygulanır ve para birimi simgesini içerir. Aşağıdaki seçenekler bulunur:

-   **Para birimi simgesi** – Rapor için para birimi simgesi. Bu değer, şirket bilgileri için **Bölgesel Seçenekler** ayarını geçersiz kılar.
-   **Negatif sayılar** – Negatif sayılar eksi işaretine (-) sahip olabilir, parantez içinde görüntülenebilir veya bir üçgen (∆) ile görüntülenebilir.
-   **Ondalık basamak sayısı** – Virgülden sonra gösterilen basamak sayısıdır.
-   **Sıfır değeri atlatma metni** – Tutar, 0 (sıfır) olduğunda rapora eklenecek metindir. Bu metin **Örnek** alanında son satır olarak görüntülenir. **Not:** Yazdırma işlemi sıfır değerleri veya aktif olmayan dönem için baskılanırsa bu metin de baskılanır.

### <a name="numeric-formatting"></a>Nümerik biçimlendirme

Nümerik biçimlendirme, herhangi bir tutara uygulanır ve bir para birimi simgesini içermez. Aşağıdaki seçenekler bulunur:

-   **Negatif sayılar** – Negatif sayılar eksi işaretine (-) sahip olabilir, parantez içinde görüntülenebilir veya bir üçgen (∆) ile görüntülenebilir.
-   **Ondalık basamak sayısı** – Virgülden sonra gösterilen basamak sayısıdır.
-   **Sıfır değeri atlatma metni** – Tutar, 0 (sıfır) olduğunda rapora eklenecek metindir. Bu metin **Örnek** alanında son satır olarak görüntülenir. **Not:** Yazdırma işlemi sıfır değerleri veya aktif olmayan dönem için baskılanırsa bu metin de baskılanır.

### <a name="percentage-formatting"></a>Yüzde biçimlendirmesi

Yüzde biçimlendirmesi yüzde işareti (%) içerir. Aşağıdaki seçenekler bulunur:

-   **Negatif sayılar** – Negatif sayılar eksi işaretine (-) sahip olabilir, parantez içinde görüntülenebilir veya bir üçgen (∆) ile görüntülenebilir.
-   **Ondalık basamak sayısı** – Virgülden sonra görüntülenecek basamak sayısıdır.
-   **Sıfır değeri atlatma metni** – Tutar, 0 (sıfır) olduğunda rapora eklenecek metindir. Bu metin **Örnek** alanında son satır olarak görüntülenir. **Not:** Yazdırma işlemi sıfır değerleri veya aktif olmayan dönem için baskılanırsa bu metin de baskılanır.

### <a name="custom-formatting"></a>Özel biçimlendirme

Bir özel biçim atlatması oluşturmak için özel biçimlendirme kategorisini kullanın. Aşağıdaki seçenekler bulunur:

-   **Tür** – Özel biçim.
-   **Sıfır değeri atlatma metni** – Tutar, 0 (sıfır) olduğunda rapora eklenecek metindir. Bu metin **Örnek** alanında son satır olarak görüntülenir. **Not:** Yazdırma işlemi sıfır değerleri veya aktif olmayan dönem için baskılanırsa bu metin de baskılanır.

Tür, pozitif değeri ve ardından negatif değeri temsil etmelidir. Genellikle, pozitif ve negatif değerleri ayıran, benzer bir biçim girersiniz. Örneğin, iki ondalık basamakla pozitif ve negatif değerlere sahip, ancak negatif değerler ayraç içinde görünür belirtmek için girin **0.00;(0.00)**. Aşağıdaki tabloda değerlerinizin biçimini kontrol etmek için kullanabileceğiniz özel biçimler gösterilmiştir. Tüm örnekler, 1234.56 değerinden başlar.

| Biçim                         | Pozitif   | Eksi     | Sıfır    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);“”       | 1.235      | (1.235)      | (Boş) |
| \#,\#\#0.00;(\#,\#\#0.00);zero | 1.234,56   | (1.234,56)   | sıfır    |
| %0,00;(%0,00)                  | %123456,00 | (%123456,00) | %0,00   |

## <a name="specify-a-normal-balance-cell"></a>Bir Normal bakiye hücresi tanımlama
Bir satır tanımında **Normal Bakiye** hücresi, o satırdaki tutarların işaretini kontrol eder. Bir satırın işaretini ters çevirmek veya bir hesabın normal bakiyesi bir borç ise, bu satır **Normal Bakiye** hücresine **C** yazın. Rapor Tasarımcısı, o satırdaki tüm kredi bilanço hesaplarına oturum tersine çevirir. Rapor tasarımcısı bu hesapları ters çevirdiğinde tüm tutarlardan alacak/borç özelliğini kaldırır ve böylece toplama işlemi kolaylaşır. Örneğin, net geliri hesaplamak için giderleri gelirden çıkartırsınız. Genellikle, toplanan ve hesaplanan satırlar **C** kodundan etkilenmez. Ancak, sütun tanımındaki **XCR** baskı kontrolü, **Normal Bakiye** sütununda **C** içeren herhangi bir satırın işaretini ters çevirir. Bu biçimlendirme özellikle, tüm istenmeyen farkları negatif tutarlar olarak göstermek istediğiniz durumlarda önemlidir. Toplanan veya hesaplanan rakam eski işarete sahipse işaretini değiştirmek istediğiniz satır için **Normal Bakiye** hücresine **C** yazın.

## <a name="specify-a-row-modifier-cell"></a>Bir Satır Değiştirici hücresi tanımlama
Bir satır tanımındaki **Satır Değiştirici** hücresinin içeriği o satır için sütun tanımında belirtilen mali yılları, dönemleri ve diğer bilgileri atlatır. Seçilen değiştirici satırdaki her hesap için geçerlidir. Her bir satırı aşağıdaki değiştirici türlerinin birini veya birkaçını kullanarak değiştirebilirsiniz:

-   Hesap değiştiriciler
-   Defter kodu değiştiriciler
-   Hesap ve hareket özellikleri

### <a name="override-a-column-definition"></a>Bir sütun tanımını atlatma

1.  Rapor Tasarımcısında değiştirilecek satır tanımını açın.
2.  Sütun tanımını atlatmak istediğiniz satırda **Satır Değiştirici** hücresini çift tıklayın.
3.  **Satır Değiştirici** iletişim kutusunda, bir**Hesap değiştirici** alanından bir seçenek belirleyin. Seçeneklerin açıklamaları için "Hesap değiştiriciler" bölümüne bakın.
4.  **Defter kodu değiştirici** alanında o satır için kullanılacak defter kodunu seçin.
5.  **Öznitelikler** altında, satır koduyla birlikte dahil edilmesi gereken her bir öznitelik için bir giriş eklemek üzere bu adımları takip edin:
    1.  **Öznitelik** hücresini çift tıklayın ve bir öznitelik adı seçin. **Dikkat:** sayı işareti Değiştir (\#) sayısal bir değere sahip.
    2.  **Başlangıç** hücresini çift tıklayın ve aralık için ilk değeri girin.
    3.  **Bitiş** hücresini çift tıklayın ve aralık için son değeri girin.

6.  **Tamam** düğmesini tıklatın.

### <a name="account-modifiers"></a>Hesap değiştiriciler

Belirli bir hesap seçtiğinizde, rapor tasarımcısı genellikle sütun tanımında belirlediğiniz hesabı ve mali yılları, dönemleri ve diğer bilgileri birleştirir. Belirli satırlar için, farklı mali dönemler vb. gibi farklı bilgiler kullanabilirsiniz. Aşağıdaki tabloda kullanılabilecek hesap değiştiriciler gösterilmiştir. Sayı işareti Değiştir (\#) bir mali yıl içinde eşit veya nokta sayısından daha az bir değere sahip.

| Hesap değiştirici | Ne yazdırılır                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Bir hesap için başlangıç bakiyesi.                                                     |
| /\#              | Belirtilen dönem için bakiye.                                                     |
| /-\#             | Bakiye dönemi için \#önce geçerli dönem dönem.                  |
| /+\#             | Bakiye dönemi için \#sonra geçerli dönem dönem.                   |
| /C               | Mevcut dönem için bakiye.                                                       |
| /C-\#            | Bakiye dönemi için \#önce geçerli dönem dönem.                  |
| /C+\#            | Bakiye dönemi için \#sonra geçerli dönem dönem.                   |
| /Y               | Geçerli dönem üzerinden yılın bugüne kadarki bakiyesi.                                      |
| /Y-\#            | Yıl-tarih bakiye dönemi boyunca \#önce geçerli dönem dönem. |
| /Y+\#            | Yıl tarihi bakiye dönemi boyunca \#sonra geçerli dönem dönem.  |

### <a name="book-code-modifiers"></a>Defter kodu değiştiriciler

Bir satırı mevcut bir defter koduyla sınırlayabilirsiniz. Sütun tanımı bir defter koduna sahip olan en az bir **FD** sütunu içermelidir. **Not:** Bir satır için defter kodu kısıtlaması, o satır için sütun tanımındaki defter kodu kısıtlamalarını atlatır.

### <a name="account-and-transaction-attributes"></a>Hesap ve hareket özellikleri

Bazı muhasebe sistemleri, mali verilerdeki hesap özniteliklerini ve hareket özniteliklerini destekler. Bu öznitelikler, sanal hesap segmentleri gibi çalışır ve hesap veya hareket hakkında ilave bilgiler taşıyabilir. Bu ilave bilgiler hesap kimlikleri, toplu iş kimlikleri, posta kodları veya diğer öznitelikler olabilir. Muhasebe sisteminiz öznitelikleri destekliyorsa, satır tanımında satır değiştirici olarak hesap özniteliklerini veya hareket özniteliklerini kullanabilirsiniz. Satır bilgilerinin nasıl atlatılacağı hakkında bilgi için, bu makalenin başındaki "Bir sütun tanımını atlatma" bölümüne bakın.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Mali Boyutlar hücresi için bir Bağlantı tanımlama
**Mali Boyutlara Bağlantı** hücresi, bir raporun her bir satırına dahil edilmesi gereken mali verilere bağlantılar içerir. Bu hücre, boyut değerlerini içerir, ancak bunun yerine bir Microsoft Excel çalışma sayfasında hücreler tanımlayabilir ve buna ek olarak segment değerleri veya boyut değerleri belirtebilirsiniz. **Boyutlar** iletişim kutusunu açmak için **Mali Boyutlara Bağlantı** hücresini çift tıklayın. **Not:** Rapor Tasarımcısı aşağıdaki ayrılmış karakterleri içeren Microsoft Dynamics ERP sisteminden seçemezsiniz hesaplar, Boyutlar veya alanları: &, \*, \[, \], {, veya}. Halihazırda satır tanımında olan bir satır için bilgileri belirlemek için, bilgileri **Mali Boyutlara Bağlantı** hücresine ekleyin. Mali verilere bağlanan yeni satırlar eklemek için, rapor tanımında yeni satırlar oluşturmak için **Satır Ekleme kaynağı** iletişim kutusunu kullanın. Sütun başlığı, aşağıdaki tabloda gösterildiği gibi sütunun nasıl yapılandırıldığına bağlı olarak değişir.

| Seçilen bağlantı türü       | Bağlantı sütununun tanımı şuna değiştirir |
|----------------------------------|----------------------------------------------------|
| Mali Boyutlar             | Mali Boyutlarla İlişkilendirme                       |
| Dış Çalışma Sayfası               | Çalışma Sayfası Bağlantı                                  |
| Mali Boyutları + Çalışma Sayfası | Mali Boyutlarla Bağlantı + Çalışma Sayfası           |
| Management Reporter Raporu       | Management Reporter Raporu                         |

### <a name="specify-a-dimension-or-range"></a>Bir boyut veya aralık belirleme

1.  Rapor Tasarımcısında değiştirilecek satır tanımını açın.
2.  **Mali Boyutlara Bağlantı** sütunundaki bir hücreyi çift tıklayın.
3.  **Boyutlar** iletişim kutusunda, boyut adının altındaki hücreyi çift tıklatın.
4.  Boyut için iletişim kutusunda **Bireysel veya aralık** öğesini seçin.
5.  İçinde **gelen** 'ı tıklatın, başlangıç boyutu girin veya alanı ![göz](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "göz") kullanılabilir boyutlar için aramak için. Bir boyut aralığı girmek için **Bitiş** alanına bitiş boyutunu girin.
6.  Boyut için iletişim kutusunu kapatmak için **Tamam** düğmesini tıklayın. **Boyutlar** iletişim kutusunda güncellenen boyut veya aralık görüntüler.
7.  **Tamam** düğmesini tıklayarak **Boyutlar** iletişim kutusunu kapatın.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Bir satır tanımında sıfır bakiye hesaplarını görüntüleme
Varsayılan olarak, rapor tasarımcısı mali verilerinde karşılık gelen bir bakiye bulunmayan hiçbir satırı yazdırmaz. Bu nedenle, tüm doğal segment değerlerini veya tüm boyut değerlerini içeren bir satır tanımı oluşturabilir ve ardından bu satır tanımını departmanlarınızdan herhangi biri için kullanabilirsiniz.

### <a name="modify-zero-balance-settings"></a>Sıfır bakiye ayarlarını değiştirme

1.  Rapor Tasarımcısında değiştirmek istediğiniz rapor tanımını açın.
2.  **Ayarlar** sekmesinde, **Diğer biçimlendirme** altından, rapor tanımında kullanılan satır tanımı için seçenekleri belirleyin.
3.  **Dosya** menüsünde değişiklikleri kaydetmek için **Kaydet** düğmesini tıklayın.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Bir satır tanımında joker karakterler ve aralıklar kullanma
Doğal segment değer girdiğinizde **boyutları** iletişim kutusunda, bir joker karakter (? koyabilirsiniz Veya \*), bir kesim herhangi bir konumda. Rapor Tasarımcısı, joker karakterler düşünmeden tanımlanmış pozisyonlar için tüm değerleri ayıklar. Örneğin, satır tanımı yalnızca doğal segment değerlerini içeriyor ve doğal segmentler dört karaktere sahip. Girerek **6???** Bir satırda, 6 ile başlayan bir doğal segment değerine sahip tüm hesaplarını dahil etmek için Rapor Tasarımcısı söyleyin. Girerseniz, **6\***, aynı sonuçları döndürülür, ancak sonuçlar da değişken genişlikli değerleri şunları içerir: **60** ve **600000**. Rapor tasarımcısı her bir joker karakterini (?) harfler ve özel karakterler içeren tam bir olası değer aralığıyla değiştirir. Örneğin,**12?0** ile **12?4** arasındaki aralıkta, **12?0** altındaki joker karakteri, karakter setindeki en düşük değerle değiştirilir ve **12?4** altındaki joker karakteri, karakter setindeki en yüksek değerle değiştirilir. **Not:** Aralığın başlangıç ve bitiş hesapları için joker karakterler kullanmaktan kaçınmalısınız. Başlangıç hesabında veya bitiş hesabında joker karakterler kullanırsanız, beklenmeyen sonuçlar alabilirsiniz.

### <a name="single-segment-or-single-dimension-ranges"></a>Tek segmentli veya tek boyutlu aralıklar

Bir segment değerleri veya boyut değerleri aralığı belirtebilirsiniz. Bir aralık belirlemenin avantajı, mali verilere yeni bir segment değeri veya boyut değeri eklendiğinde her defasında satır tanımını güncelleştirmenize gerek kalmamasıdır. Örneğin, aralık **+ hesap =\[6100:6900\]** hesapları 6100 6900 üzerinden gelen değerler satır tutarı çeker. Bir aralık bir joker karakter (?) içeriyorsa, rapor tasarımcısı aralığı karakterlere dayalı bir şekilde değerlendirmez. Bunun yerine, aralığın düşük ve yüksek noktaları belirlenir ve ardından bitiş değerleri ve bunlar arasında kalan tüm değerler dahil edilir. **Not:** Rapor Tasarımcısı aşağıdaki ayrılmış karakterleri içeren Microsoft Dynamics ERP sisteminden seçemezsiniz hesaplar, Boyutlar veya alanları: &, \*, \[, \], {, veya}. Ve (&) işaretini sadece **Boyutlardan Satırlar Ekle** iletişim kutusunu kullanarak otomatik olarak satır tanımları oluşturduğunuzda ekleyebilirsiniz.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Çok segmentli veya çok boyutlu aralıklar

Birden çok boyut değer birleşimlerini kullanarak bir aralık girin zaman aralığı karşılaştırma üzerinde yapılır bir... \financial-dimensions\dimension-by-Dimension temel. Aralık karşılaştırma, tek tek karakterlere dayalı olarak veya kısmi segmente dayalı olarak gerçekleştirilmez. Örneğin, aralık **+ hesap =\[5000:6000\], departman =\[1000:2000\], maliyet merkezi =\[00\]** eşleşen her kesimi hesaplarını içerir. Bu senaryoda, ilk boyut 5000-6000 aralığında olmalıdır, ikinci boyutu 1000 ile 2000 aralığında olmalıdır ve son boyut 00 olmalıdır. Örneğin, **+ hesap =\[5100\], departman =\[1100\], maliyet merkezi =\[01\]** son kesimi belirtilen aralık dışında olduğundan raporda dahil değildir. Bir segment değer boşluk içeriyorsa, bu değer köşeli parantezler içine alın (\[\]). Dört karakterlik segment için aşağıdaki değerler geçerlidir: **\[234\], \[123 \], \[1 34\]**. Boyut değerlerini, köşeli ayraçlar içine alınmalıdır (\[\]) ve Rapor Tasarımcısı sizin için bu parantez ekler. Ne zaman birden çok kesimi veya birden çok boyut aralığı joker karakterlerini (?) içerir Veya \*), tüm çoklu kesim veya birden çok boyut aralığının düşük ve yüksek uçları belirlenir ve sonra da son ve bunlar arasındaki tüm değerleri dahil edilir. Örneğin 40000 ile 99999 arasındaki tüm hesap aralığı gibi geniş bir aralığa sahipseniz, mümkün olduğu durumlarda geçerli bir başlangıç hesabı ve bitiş hesabı belirtmelisiniz. **Not:** Rapor Tasarımcısı aşağıdaki ayrılmış karakterleri içeren Microsoft Dynamics ERP sisteminden seçemezsiniz hesaplar, Boyutlar veya alanları: &, \*, \[, \], {, veya}. Ve (&) işaretini sadece **Boyutlardan Satırlar Ekle** iletişim kutusunu kullanarak otomatik olarak satır tanımları oluşturduğunuzda ekleyebilirsiniz.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Bir satır tanımına başka hesaplar ekleme veya bir satır tanımındaki hesapları çıkarma
Bir hesaba başka bir hesaptaki parasal tutarlardan parasal tutar eklemek veya bir hesaptan aynı şekilde parasal tutar çıkarmak için **Mali Boyutlara Bağlantı** hücresindeki artı işaretini (+) ve eksi işaretini (-) kullanabilirsiniz. Aşağıdaki tabloda mali verilere bağlantılar eklemek veya bağlantılar çıkarmak için kullanılabilecek biçimler gösterilmiştir.

| Operasyon                                                                               | Bu biçimi kullanma                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| İki tam donanımlı hesap ekleyin.                                                       | + Bölüm =\[000\], hesabı =\[1205\], departman =\[00\]+ bölüm =\[100\], hesabı =\[1205\], departman =\[00\] |
| İki segment değeri ekleyin.                                                                 | + Hesap =\[1205\]+ hesap =\[1210\]                                                                           |
| Joker karakterleri içeren segment değerleri ekleyin.                                    | + Hesap =\[120? + hesap =\[11??\]                                                                             |
| Bir tam donanımlı hesap aralığı ekleyin.                                                | + Bölüm =\[000:100\], hesabı =\[1205\], departman =\[00\]                                                   |
| Bir segment değeri aralığı ekleyin.                                                          | + Hesap =\[1200:1205\]                                                                                       |
| Joker karakterleri içeren bir segment değeri aralığı ekleyin.                         | + Hesap =\[120?: 130?\]                                                                                       |
| Bir tam donanımlı hesabı başka bir tam donanımlı hesaptan çıkarın.              | + Bölüm =\[000\], hesabı =\[1205\], departman =\[00\]-bölme =\[100\], hesabı =\[1205\], departman =\[00\] |
| Bir segment değerini başka bir segment değerinden çıkarın.                                  | + Hesap =\[1205\]-hesap =\[1210\]                                                                           |
| Bir joker karakteri içeren segment değerini başka bir segment değerinden çıkarın. | + Hesap =\[1200\]-hesap =\[11??\]                                                                           |
| Bir tam donanımlı hesap aralığını çıkarın.                                           | -Bölme =\[000:100\], hesabı =\[1200:1205\], departman =\[00:01\]                                           |
| Bir segment değeri aralığını çıkarın.                                                     | -Hesap =\[1200:1205\]                                                                                       |
| Joker karakterleri içeren bir segment değeri aralığını çıkarın.                    | -Hesap =\[120?: 130?\]                                                                                       |

Hesapları doğrudan değiştirebilirsiniz, ancak mali veri bağlantılarına doğru biçimlendirmeyi uygulamak için **Boyutlar** iletişim kutusunu da kullanabilirsiniz. Değerlerden herhangi birini joker karakterlerini (?) içerebilir Or \*). Ancak, Rapor Tasarımcısı hesaplar, Boyutlar veya alanları aşağıdaki ayrılmış karakterleri içeren Microsoft Dynamics ERP sisteminden seçemezsiniz: &, \*, \[, \], {, veya}. **Not:** Değerleri çıkarmak için bu değerler etrafına parantez eklemelisiniz. Girerseniz, örneğin, **450?-(4509)**, olarak gösterilen **+ hesap =\[4509\]-hesap =\[450? \]**, ve tutarını 450 ile başlayan tüm hesap kesim için tutar 4509 segmentten hesap çıkarmak için Rapor Tasarımcısı tetiklemesini bildiren.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Diğer hesaplara hesap ekleme veya diğer hesaplardan hesap çıkarma

1.  Rapor Tasarımcısında değiştirilecek satır tanımını açın.
2.  Uygun satırda **Mali Boyutlara Bağlantı** sütunundaki hücreyi çift tıklayın.
3.  **Boyutlar** iletişim kutusunun ilk satırında, şu adımları takip edin:
    1.  İlk alanda tüm boyutları (varsayılan) seçin veya **Boyut Kümelerini Yönet** iletişim kutusunu açmak üzere tıklayın; burada bir set oluşturabilir veya mevcut bir seti değiştirebilir, kopyalayabilir veya silebilirsiniz.
    2.  Çift **işleç +/-** hücre ve artı seçin (**+**) veya eksi (**-**) bir veya daha fazla boyut değerleri uygular veya satır içinde ayarlayan işleci.
    3.  Uygun boyut değeri sütununda, **Boyutlar** iletişim kutusunu açmak için hücreyi çift tıklatın ve bu boyut değerinin bir ayrı değer veya aralık için mi, bir boyut değeri seti için mi, yoksa toplama hesapları için mi olduğunu seçin. **Boyutlar** iletişim kutusundaki alanların açıklamaları için, "Boyut Açıklaması iletişim kutusu" bölümüne bakın.
    4.  **Başlangıç** ve **Bitiş** sütunlarına segment değerlerini girin.

4.  Daha fazla işleç eklemek için 2 ile 3. adımlar arasındaki işlemleri tekrarlayın.

**Not:** İşleç, satırdaki tüm boyutlar için geçerlidir.

## <a name="description-of-the-dimensions-dialog-box"></a>Boyut Açıklaması iletişim kutusu
Aşağıdaki tabloda **Boyutlar** iletişim kutusunun alanları açıklanmıştır.

| Madde                | Açıklama                                                                                                                                                                                                                                                                                             |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ayrı veya aralık | İçinde **gelen** tıklatın, hesabın adını girin veya alanı **göz** düğmesini ![göz](https://i-technet.sec.s-msft.com/dynimg/IC679490.gif "göz") hesaba gidin. Bir aralık seçmek için, **Bitiş** alanına bir değer girin veya bu değeri arayın.                                             |
| Boyut Değeri Seti | **Ad** alanına bir boyut değeri setinin adını girin. Bir set oluşturmak veya bir seti değiştirmek, kopyalamak veya silmek için **Boyut Değeri Setlerini Yönet** öğesini tıklayın. **Formül** alanına yerleştirilir formülle birlikte **mali boyutları bağlantı** hücre içinde satır tanımını ayarlayın bu boyut değeri için. |
| Toplama hesapları   | **Ad** alanına toplama hesapları için bir boyut girin veya bunu arayın. **Formül** alanı, rapor tanımındaki bu toplama hesabı için **Mali Boyutlara Bağlantı** hücresindeki formülden doldurulur.                                                                       |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Bir satır tanımına boyut değeri setleri ekleme
Bir boyut değeri seti, boyut değerlerinin adlandırılmış bir grubudur. Bir boyut değeri seti sadece tek bir boyuttaki değerleri içerir, ancak birden fazla satır tanımındaki, sütun tanımındaki, raporlama ağaç tanımlarındaki ve rapor tanımlarındaki bir boyut değeri setini kullanabilirsiniz. Ayrıca, bir rapor tanımında boyut değerleri setlerini de birleştirebilirsiniz. Mali verilerinizdeki bir değişiklik, boyut değer setini değiştirmenizi gerektiriyorsa, boyut değer seti aralığını güncelleştirebilirsiniz ve bu güncelleştirme boyut değer setini kullanan tüm alanlar için geçerli olur. Örneğin, mali verilerinize bağlantı için genellikle bir değer aralığı, örneğin 5100 ile 5600 arasındaki değerleri belirtiyorsanız, bu aralığı Satışlar olarak adlandırılan bir hesap setine atayabilirsiniz. Boyut değerleri kümesi oluşturduktan sonra finansal veri bağlantısı ayarlanmış seçebilirsiniz. Başka bir örnek olarak, 5600-5100 değer aralığı satış için atanır ve 4175 için indirimler, atanırsa, toplam satışların satış iskontoları çıkararak belirleyebilirsiniz. Bu işlemi olarak gösterilen **(5100:5600)-4175**.

### <a name="create-a-set-of-dimension-values"></a>Bir boyut değeri seti oluşturma

1.  Rapor Tasarımcısında değiştirmek istediğiniz satır, sütun veya ağaç tanımını açın.
2.  **Düzen** menüsünden **Boyut Değer Setlerini Yönet** öğesini tıklayın.
3.  **Boyut Değer Setlerini Yönet** iletişim kutusundaki **Boyut** alanında, oluşturulacak boyut değeri setinin türünü seçin ve ardından **Yeni** öğesini tıklayın.
4.  **Yeni** iletişim kutusunda set için bir ad ve açıklama girin.
5.  **Başlangıç** sütununda bir hücreyi çift tıklatın.
6.  **Hesap** iletişim kutusunda, listeden hesap adını seçin veya **Arama** alanında girişi arayın. Ardından **Tamam**'ı tıklatın.
7.  Bu işleç için bir formül oluşturmak üzere 5 ile 6. adımlar arasındaki işlemleri **Bitiş** sütunu için tekrarlayın.
8.  Formül tamamlandığında **Tamam** öğesini tıklayın.
9.  **Boyut Setlerini Yönet** iletişim kutusunda **Kapat** öğesini tıklayın.

### <a name="update-a-set-of-dimension-values"></a>Bir boyut değeri setini güncelleştirme

1.  Rapor Tasarımcısında değiştirmek istediğiniz satır, sütun veya ağaç tanımını açın.
2.  **Düzen** menüsünden **Boyut Değer Setlerini Yönet** öğesini tıklayın.
3.  **Boyut Değer Setlerini Yönet** iletişim kutusundaki **Boyut** alanında, boyut türünü seçin.
4.  Listede, güncellenecek boyut değeri setini seçin ve ardından **Değiştir** düğmesini tıklayın.
5.  **Değiştir** iletişim kutusunda, sete dahil edilecek formül değerlerini değiştirin. **Not:** Yeni hesaplar veya boyutlar eklerseniz, değişiklikleri dahil etmek için mevcut boyut değeri setlerini değiştirdiğinizden emin olun.
6.  Hücreyi çift tıklatın ve uygun bir işleç, **Başlangıç** hesabını ve **Bitiş** hesabını seçin.
7.  **Tamam** düğmesini tıklayarak **Değiştir** iletişim kutusunu kapatın ve değişikliklerinizi kaydedin.

### <a name="copy-a-dimension-set"></a>Bir boyut kümesi kopyalama

1.  Rapor Tasarımcısında değiştirmek istediğiniz satır, sütun veya ağaç tanımını açın.
2.  **Düzen** menüsünden **Boyut Değer Setlerini Yönet** öğesini tıklayın.
3.  **Boyut Değer Setlerini Yönet** iletişim kutusundaki **Boyut** alanından boyut türünü seçin.
4.  Listede, kopyalanacak seti seçin ve ardından **Farklı Kaydet** düğmesini tıklatın.
5.  Kopyalanan set için yeni bir ad girin ve ardından **Tamam** düğmesini tıklatın.

### <a name="delete-a-dimension-set"></a>Bir boyut setini silme

1.  Rapor Tasarımcısında değiştirmek istediğiniz satır, sütun veya ağaç tanımını açın.
2.  **Düzen** menüsünden **Boyut Değer Setlerini Yönet** öğesini tıklayın.
3.  **Boyut Değer Setlerini Yönet** iletişim kutusundaki **Boyut** alanında, boyut türünü seçin.
4.  Silinecek seti seçin ve ardından **Sil** düğmesini tıklayın. Boyut değer setini kalıcı olarak silmek için **Evet** düğmesini tıklayın.


<a name="see-also"></a>Ayrıca bkz.
--------

[Finansal raporlama için Microsoft Dynamics 365 işlemleri için](financial-reporting-intro.md)


