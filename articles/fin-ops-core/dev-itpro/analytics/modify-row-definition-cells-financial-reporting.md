---
title: Satır tanımı hücrelerini değiştirme
description: Bu makalede bir finansal raporun satır tanımındaki tüm hücreler için gerekli olan bilgiler ve bu bilgilerin nasıl girileceği açıklanmaktadır.
author: aprilolson
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 58881
ms.assetid: 0af492df-a84e-450c-8045-78ef1211abaf
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1c125369a5b2134759bf3650175276acf42b69e0
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802836"
---
# <a name="modify-row-definition-cells"></a>Satır tanımı hücrelerini değiştirme

[!include [banner](../includes/banner.md)]

Bu makalede bir finansal raporun satır tanımındaki tüm hücreler için gerekli olan bilgiler ve bu bilgilerin nasıl girileceği açıklanmaktadır.

## <a name="specify-a-row-code-in-a-row-definition"></a>Bir satır tanımında bir satır kodu belirleme

Satır tanımlarında, **Satır kodu** hücresindeki rakamlar veya etiketler, satır tanımındaki her bir satırı tanımlar. Hesaplamalar ve toplamlardaki verilere bakmak için satır kodunu belirtebilirsiniz.

### <a name="row-code-requirements"></a>Satır kodu gereksinimleri

Tüm satırlar için bir satır kodu gereklidir. Bir satır tanımında, sayısal, alfa sayısal ve ayarlanmamış (boş) satır kodlarını karıştırabilirsiniz. Satır kodu söz konusu satırı tanımlayan herhangi bir pozitif tamsayı (100.000.000'dan küçük) veya açıklayıcı bir etiket olabilir. Açıklayıcı bir etiket şu kurallara uymalıdır:

- Etiket mutlaka bir alfabetik karakterle (a'dan z'ye veya A'dan Z'ye) başlamalıdır ve 16 karaktere kadar herhangi bir rakam ve harf kombinasyonundan meydana gelebilir.

    > [!NOTE]
    > Bir etiketi, alt çizgi karakteri (\_) içerebilir, ancak diğer özel karakterler kullanılamaz.

- Etiket aşağıdaki ayrılmış sözcüklerden hiçbirini içermez: AND, OR, IF, THEN, ELSE, PERIODS, TO, BASEROW, UNIT, NULL, CPO veya RPO.

Aşağıdaki örnekler, geçerli satır kodlarıdır:

- 320
- TL\_NET\_INCOME
- TL\_NET\_94

### <a name="change-a-row-code-in-a-row-definition"></a>Bir satır tanımındaki bir satır kodunu değiştirme

1. Report Designer'da **Satır tanımları** öğesine tıklayın ve ardından değiştirmek için satır tanımını açın.
2. İlgili satırda, **Satır kodu** sütunundaki hücreye yeni değeri girin.

### <a name="reset-numeric-row-codes"></a>Sayısal satır kodlarını sıfırlama

1. Report Designer'da **Satır tanımları** öğesine tıklayın ve ardından değiştirmek için satır tanımını açın.
2. **Düzenle** menüsünde, **Satırları yeniden numaralandır**'a tıklayın.
3. **Satırları yeniden numaralandır** iletişim kutusunda, başlangıç satır kodu ve satır kodu artışı için yeni değerler belirtin. Nümerik satır kodlarını birbirine eşit değerlere sıfırlayabilirsiniz. Ancak, rapor tasarımcısı sadece rakamla başlayan satır kodlarını (örneğin 130 veya 246) yeniden numaralandırır. Harflerle başlayan (örneğin INCOME\_93 veya TP0693) satır kodlarını yeniden numaralandırmaz.

> [!NOTE]
> Satır kodlarını yeniden numaralandırdığınızda rapor tasarımcısı **TOT** ve **CAL** referanslarını otomatik olarak güncelleştirir. Örneğin, bir **TOT** satırı, 100 satır kodu ile başlayan bir aralığa karşılık geliyorsa ve satırları 90'dan başlayarak yeniden numaralandırırsanız, başlangıç **TOT** referansı 100'den 90'a değişir.

## <a name="add-a-description"></a>Açıklama ekleme
Açıklama hücresi raporun satırındaki "Gelir" veya "Net Gelir" gibi mali verilerin açıklamasını sunar. **Açıklama** hücresindeki metin, satır tanımına girdiğinizde raporda tam olarak görüntülenir.

> [!NOTE]
> Açıklama sütununun rapordaki genişliği sütun tanımı altından ayarlanır. Satır tanımında yer alan **Açıklama** sütunundaki metin uzunsa **DESC** sütununun genişliğini kontrol edin. **Şunlardan Satır Ekle:** iletişim kutusunu kullandığınızda, **Açıklama** sütunundaki değerler mali verilerden alınan segment değerleri veya boyut değerleridir. Bölüm başlığı veya bölüm toplamı gibi açıklayıcı metin ve bir toplam satırından önce bir çizgi gibi biçimlendirme eklemek için satır ekleyebilirsiniz. Rapor raporlama ağacı içeriyorsa raporlama ağacına raporlama birimleri için tanımlanan ek metni ekleyebilirsiniz. Ayrıca, ek metni belirli bir raporlama birimiyle de sınırlandırabilirsiniz.

### <a name="add-the-description-for-a-line-on-a-report"></a>Bir rapordaki bir satıra açıklama ekleme

1. Report Designer'da **Satır tanımları** öğesine tıklayın ve ardından değiştirmek için satır tanımını açın.
2. **Açıklama** hücresini seçin ve ardından rapor satırının adını girin.
3. Biçimlendirme uygulayın.

### <a name="add-additional-text-from-a-reporting-tree-in-the-description"></a>Açıklamadaki bir raporlama ağacından ek metin ekleme

1. Report Designer'da **Satır tanımları** öğesine tıklayın ve ardından değiştirmek için satır tanımını açın.
2. Uygun **Açıklama** hücresine ek metin kodunu ve her türlü diğer metni girin.
3. Biçimlendirme uygulayın.

### <a name="limit-the-additional-text-to-a-specific-reporting-unit"></a>Ek metni belirli bir raporlama birimiyle sınırlandırın.

1. Report Designer'da **Satır tanımları** öğesine tıklayın ve ardından değiştirmek için satır tanımını açın.
2. Ek metnin oluşturulması gereken satırı bulun ve ardından **İlgili Formüller/Satırlar/Birimler** sütunundaki hücreye çift tıklayın.
3. **Raporlama birimi seçimi** iletişim kutusundaki **Raporlama ağacı** alanından bir raporlama ağacı seçin.
4. **Kısıtlama için raporlama birimi seç** alanında, raporlama ağacını genişletin veya daraltın ve ardından bir raporlama birimi seçin.

## <a name="add-a-format-code"></a>Biçim kodu ekleme
**Biçim kodu** hücresi söz konusu satırın içeriği için önceden biçimlendirilmiş bir seçki sunar. **Biçim kodu** hücresi boşsa, satır bir mali veri ayrıntı satırı olarak yorumlanır.

> [!NOTE]
> Bir rapor, baskılanan tutar satırlarıyla bağlantılı, tutar içermeyen biçimlendirme satırları içeriyorsa (örneğin, sıfır bakiyeler nedeniyle), başlık ve biçim satırlarının yazdırılmaması için **İlgili Formüller/Satırlar/Birimler** sütununu kullanabilirsiniz.

### <a name="add-a-format-code-to-a-report-row"></a>Bir rapor satırına biçim kodu ekleme

1. Report Designer'da, **Satır tanımları**'na tıklayın ve ardından değiştirmek için bir satır tanımı seçin.
2. **Biçim kodu** hücresine çift tıklayın.
3. Listedeki bir biçim kodunu seçin. Aşağıdaki tabloda biçim kodları ve bunların eylemleri açıklanmaktadır.

    | Biçim kodu                   | Biçim koduna ilişkin yorum | Eylem |
    |-------------------------------|-----------------------------------|--------|
    | (Hiçbiri)                        |                                   | **Biçim kodu** hücresini temizler. |
    | TOT                           | Toplam                             | **İlgili Formüller/Satır/Birim** sütununda matematiksel işleçler kullanan bir satırı belirtir. Toplamlar **+** veya **-** gibi basit işleçler içerir. |
    | CAL                           | Hesaplama                       | **İlgili Formüller/Satır/Birim** sütununda matematiksel işleçler kullanan bir satırı belirtir. Hesaplamalar **+**, **-**, **\**_, _*/** gibi işleçleri ve **IF/THEN/ELSE** deyimlerini içerir. |
    | DES                           | Tanım                       | Bir rapordaki başlık satırını veya boş bir satırı tanımlar. |
    | LFT RGT CEN                   | Sol Sağ Orta                 | Metnin sütun tanımındaki yerinden bağımsız olarak rapor sayfasındaki satır açıklaması metnini hizalar. |
    | CBR                           | Temel Satırı Değiştir                   | Sütun hesaplamaları için temel satırı ayarlayan bir satır tanımlar. |
    | COLUMN                        | Sütun sonu                      | Raporda yeni bir sütun başlatır. |
    | SAYFA                          | Sayfa sonu                        | Raporda yeni bir sayfa başlatır. |
    | \---                          | Tek alt çizgi                  | Rapordaki tüm tutar sütunlarını tek altı çizili hale getirir. |
    | ===                           | Çift alt çizgi                  | Rapordaki tüm tutar sütunlarını çift altı çizili hale getirir. |
    | LINE1                         | İnce çizgi                         | Sayfa boyunca tek bir ince çizgi çizer. |
    | LINE2                         | Kalın çizgi                        | Sayfa boyunca tek bir kalın çizgi çizer. |
    | LINE3                         | Noktalı çizgi                       | Sayfa boyunca tek bir noktalı çizgi çizer. |
    | LINE4                         | Kalın çizgi ve ince çizgi          | Sayfa boyunca çift çizgi çizer. Üstteki çizgi kalın, alttaki çizgi ise incedir. |
    | LINE5                         | İnce çizgi ve kalın çizgi          | Sayfa boyunca çift çizgi çizer. Üstteki çizgi ince, alttaki çizgi ise kalındır. |
    | BXB BXC                       | Kutu içinde satır                         | **BXB** satırıyla başlayan ve **BXC** satırıyla biten rapor satırlarının çevresine bir kutu çizer. |
    | REM                           | Açıklama                            | Bir satırın yorum satırı olduğunu ve raporda yazdırılmaması gerektiğini belirtir. Örneğin, bir açıklama satırı biçimlendirme tekniklerinizi açıklayabilir. |
    | SORT ASORT SORTDESC ASORTDESC | Sırala                              | Giderleri veya gelirleri sıralar, en büyük varyansa göre gerçek varyans veya bütçe varyansı raporunu sıralar ya da satır açıklamalarını alfabetik olarak sıralar. |

## <a name="specify-related-formulasrowsunits"></a>İlgili formülleri/satırları/birimleri belirt
**İlgili formüller/Satırlar/Birimler** hücresinin birden fazla amacı vardır. Satırın türüne bağlı olarak, bir **İlgili Formüller/Satırlar/Birimler** hücresi aşağıdaki işlevlerden birini gerçekleştirir:

- Bir **TOT** veya **CAL** biçim kodunu kullandığınızda bir hesaplamaya eklenecek satırları tanımlama.
- Biçimlendirmenin yalnızca ilgili tutar yazdırıldığında yazdırılması için bir biçimlendirme satırını bir tutar satırıyla ilişkilendirme.
- Bir satırı belirli bir raporlama birimiyle sınırlandırma.
- **BASEROW** biçim kodunu kullandığınızda hesaplamalar için temel satırı tanımlama.
- Sıralama biçim kodlarından herhangi birini kullandığınızda sıralanacak satırları tanımlama.

### <a name="use-a-row-total-in-a-row-definition"></a>Bir satır tanımındaki bir satır toplamını kullanma

Diğer satırlara tutar eklemek ve bunlardan tutar çıkarmak için bir satır toplamı formülü kullanın. Satır toplamı oluşturma amaçlı bir formül, bağımsız satır kodlarını ve aralıklarını birleştirmek için + ve - işleçlerini kullanabilir. Aralıkla bir iki nokta üst üste işaretiyle (:) gösterilir. Formül en fazla 1.024 karakter içerebilir. Standart bir toplama formülü örneği şu şekildedir: 400+420+430+450+460LIABILITIES+EQUITY520:546520:546-LIABILITIES

### <a name="components-of-a-row-total-formula"></a>Bir satır toplamı formülünün bileşenleri

Bir satır toplamı formülü oluşturduğunuzda, geçerli satır tanımına hangi satırların ekleneceğini veya bu tanımdan hangi satırların çıkarılacağını belirtmek için satır kodlarını, ayrıca satırların nasıl birleştirileceğini belirtmek için de işleçleri kullanmanız gerekir. Toplam satırları ve tutar satırları herhangi bir birleşimde kullanılabilir.

> [!NOTE]
> Bir aralıktaki tüm toplam satırları hariçtir. Bir genel toplam oluşturmak için, satır aralığını belirtebilirsiniz. Bir aralığın ilk satırı bir toplam satırıysa söz konusu satır yeni toplama eklenir. Aşağıdaki tabloda işleçlerin satır toplam formüllerinde nasıl kullanıldığı açıklanmıştır.

| İşleç | Örnek formül | Açıklama                                                 |
|----------|-----------------|-------------------------------------------------------------|
| +        | 100+330         | 100 satırındaki tutarı 330 satırındaki tutara ekler.        |
| :        | 100:330         | Tüm satırların toplamlarını 100 satırı ile 330 satırı arasına ekler.    |
| -        | 100-330         | 100 satırındaki tutarı 330 satırındaki tutardan çıkarır. |

### <a name="create-a-row-total"></a>Satır toplamı oluşturma

1. Report Designer'da **Satır tanımları** öğesine tıklayın ve ardından değiştirmek için satır tanımını açın.
2. Satır tanımındaki **Biçim kodu** hücresine çift tıklayın ve **TOT**'u seçin.
3. **İlgili Formüller/Satırlar/Birimler** hücresine toplam formülünü girin.

### <a name="relate-a-format-row-to-an-amount-row"></a>Bir biçim satırını bir tutar satırıyla ilişkilendirme

Bir satır tanımındaki **Biçim kodu** sütununda **DES**, **LFT**, **RGT**, **CEN**, **---** ve **===** biçim kodları, biçimlendirmeyi tutar içermeyen satırlara uygular. İlgili tutar satırları baskılandığında (örneğin, tutar satırlarının sıfır değerleri içermesi veya dönem faaliyeti içermemesi nedeniyle) format satırlarını ilgili tutar satırlarıyla ilişkilendirmeniz gerekir. Bu işlev, döneme ait yazdırılacak ayrıntı olmadığında alt toplamlarla ilgili başlıkların veya biçimlendirmenin yazdırılmasını engellemek istediğinizde kullanışlıdır.

> [!NOTE]
> Ayrıca, tutar bulunmayan satırları görüntüleme seçeneğini temizleyerek ayrıntılı tutar satırlarının yazdırılmasını da engelleyebilirsiniz. Bu seçenek rapor tanımının **Ayarlar** sekmesinde yer alır. Varsayılan olarak, sıfır bakiyeye sahip veya dönem faaliyeti olmayan hareket ayrıntısı hesapları raporlarda gizlenir. Bu hareket ayrıntısı hesaplarını göstermek için, rapor tanımının **Ayarlar** sekmesindeki **Tutar bulunmayan satırları görüntüle** onay kutusunu seçin.

### <a name="relate-a-format-row-to-an-amount-row"></a>Bir biçim satırını bir tutar satırıyla ilişkilendirme

1. Report Designer'da, **Satır tanımları**'na tıklayın ve ardından değiştirmek için bir satır tanımı seçin.
2. Biçimlendirme satırındaki **İlgili Formüller/Satırlar/Birimler** hücresine gizlenecek tutar satırının satır kodunu girin.

    > [!NOTE]
    > Tutar satırını gizlemek için satırın bakiyesi 0 (sıfır) olmalıdır. Bakiyesi olan bir tutar satırı gizlenmez.

3. **Dosya** menüsünde **Kaydet**'e tıklayın.

### <a name="example-of-preventing-printing-of-rows"></a>Satırların yazdırılmasını engellemeye ilişkin örnek

Aşağıdaki örnekte nakit tutarlarının hiçbiriyle ilgili bir etkinlik gerçekleşmediğinden bir kullanıcı, raporun **Toplam nakit** satırındaki başlığın ve alt çizgilerin yazdırılmasını engellemek istiyor. Bu nedenle, 220 satırında (**---** biçim kodunun da belirttiği gibi bir biçimlendirme satırıdır), **İlgili Formüller/Satırlar/Birimler** hücresinde, baskılamak istediği tutar satırının satır kodu olan **250** değerini giriyor.

[![RelatedRowsRowDefinition.](./media/relatedrowsrowdefinition-1024x144.png)](./media/relatedrowsrowdefinition.png)

## <a name="select-the-base-row-for-a-column-calculation"></a>Bir sütun hesaplaması için temel satırı seçme
İlişkiye dayalı raporlamada **CBR** (temel satırı değiştir) biçim kodunu kullanarak satır tanımındaki bir veya daha fazla satırı atarsınız. Böylece sütun tanımındaki bir hesaplama bir temel satıra başvurur. Aşağıda CBR hesaplamalarının tipik bazı örnekleri sunulmuştur:

- Bağımsız gelir maddeleriyle ilişkili olduğundan toplam gelir yüzdesi
- Bağımsız gider maddeleriyle ilişkili olduğundan toplam gider yüzdesi
- Bölüm veya departman ayrıntılarıyla ilişkili olduğundan brüt marj yüzdesi.

Satır tanımında bir veya daha fazla temel satır tanımlanır ve ardından sütun tanımı temel satırın rapor edildiği ilişkiyi belirler. Sütun formülünde kullanılan kod **BASEROW**'dur. Şu temel matematik işlemleri **BASEROW** ile birlikte kullanılır: bölme, çarpma, toplama veya çıkarma. En sık kullanılan işlem sonucun yüzde olarak gösterildiği **BASEROW**'a bölmektir. Formülde **BASEROW**'un kullanıldığı sütun hesaplamaları ilgili temel satır kodları için satır tanımından yararlanır. **CBR** satırları aşağıdaki özelliklere sahiptir:

- **CBR** satırları tamamlanan raporda yazdırılmaz.
- **CBR** biçim kodu ve ilgili satır kodu ilgili hesaplamaları gösteren satırın veya bölümün üst kısmına konumlandırılır.

Bir sütun tanımında, **CALC** sütun türü **Formül** satırındaki bir formülü belirten bir sütunu gösterir. Bu formül raporun bu sütununa ilişkin verilerde çalışır ve hesaplamaları satırdaki **CBR** biçim kodlarına dayandırmak için Baserow'u kullanır. Satır tanımında **CBR** biçim kodu rapordaki her satır için bir yüzde hesaplayan veya temel satırla çarpım yapan sütunlar için temel satırı tanımlar. Bir satır biçiminde, net satış için bir, brüt satış için bir ve toplam giderler için bir adet gibi birden fazla **CBR** biçim kodunuz olabilir. Genellikle **CBR** biçim kodu, bir toplam satırıyla karşılaştırılan hesaplar için bir yüzde oluşturmak üzere kullanılır. Başka bir temel satır tanımlanana kadar tüm hesaplamalar için bir temel satır kullanılır. Bir başlangıç **CBR** biçim kodu ile bir son **CBR** biçim kodu tanımlamanız gerekir. Örneğin, giderleri net satışın yüzdesi olarak belirlemek için her gider satırındaki değeri net satış satırındaki değere bölebilirsiniz. Bu durumda, net satış satırı temel satırdır. Aşağıdaki örnekte gösterildiği gibi her sonucun taban yüzdesiyle birlikte cari ve yılın başından beri alınan sonuçları raporlayan bir sütun tanımı tanımlayabilirsiniz. Ayrıntılı bir gelir tablosuyla başlayın.

### <a name="select-the-base-row-in-a-row-definition-for-a-column-calculation"></a>Bir sütun hesaplaması için bir satır tanımında temel satırı seçme

1. Report Designer'da, **Sütun tanımları**'na tıklayın ve ardından bir gelir tablosuna ait sütun tanımını açın.
2. Sütun tanımına yeni sütun ekleyin ve sütun türünü **CALC** olarak ayarlayın.
3. Yeni sütunun **Formül** hücresine **X/BASEROW** formülünü girin. Burada **X** yüzdesi olarak görülecek **FD** sütun türüdür.
4. **Biçim/Para Birimi geçersiz kalma** hücresine çift tıklayın.
5. **Biçim geçersiz kılma** iletişim kutusundaki **Biçim kategorisi** listesinde **Yüzde**'yi seçin ve ardından **Tamam**'a tıklayın.
6. **Dosya** menüsünde, sütun tanımını yeni bir adla kaydetmek için **Farklı Kaydet** öğesini tıklayın. **CBR** öğesini mevcut dosya adına ekleyin (örneğin **CUR\_YTD\_CBR**). Bu sütun tanımı, temel satır sütunu tanımınızdır.
7. Report Designer'da, **Satır tanımları**'na tıklayın ve ardından temel satır hesaplamasını kullanarak değişiklik yapmak için satır tanımını açın.
8. Temel satır hesaplamasının başlaması gereken satırın üzerine yeni bir satır ekleyin.
9. Satır tanımının **Biçim kodu** hücresine çift tıklayın ve ardından **CBR**'yi seçin.
10. **İlgili Formüller/Satırlar/Birimler** hücresine temel satırın satır kodu numarasını girin.

### <a name="example-of-base-row-calculation"></a>Temel satır hesaplaması örneği

Aşağıdaki satır tanımı örneğinde, 100 satırı, hesaplamalar için temel satırın 280 olduğunu gösterir.

[![Temel satır hesaplamasına örnek.](./media/cbrrowdefinition.png)](./media/cbrrowdefinition.png)

Aşağıdaki sütun tanımı örneğinde, hesaplamalarda **CBR** biçim kodu kullanılmaktadır. C sütunundaki hesaplama raporun B sütunundaki değeri sütunun 280. satırındaki değere bölmektedir. B sütunundaki biçim geçersiz kılma işlemi, hesaplamanın sonucunu yüzde olarak yazdırmaktadır. Benzer şekilde, E sütunundaki her tutar net satışın yüzdesi olarak D sütunundaki tutardır.

[![Sütun tanımı örneği.](./media/cbrcolumndefinition2.png)](./media/cbrcolumndefinition2.png)

Aşağıdaki örnek önceki hesaplamalara göre oluşturulabilecek bir raporu göstermektedir.

[![Önceki örnek hesaplamalarına dayalı örnek rapor.](./media/cbrreport-1024x272.png)](./media/cbrreport.png)

## <a name="select-a-sorting-code-for-a-row-definition"></a>Bir satır tanımı için bir sıralama kodu seçme
Sıralama kodları hesapları veya gelirleri sıralar, en büyük varyansa göre gerçek varyans veya bütçe varyansı raporunu sıralar ya da satır açıklamalarını alfabetik olarak sıralar. Aşağıdaki sıralama kodları kullanılabilir:

- **SORT**: Raporu belirtilen sütundaki değerlere göre artan sırada sıralar.
- **ASORT**: Raporu belirtilen sütundaki değerlerin mutlak değerine göre artan sırada sıralar. Başka bir deyişle, değerler sıralanırken her değerin işareti yok sayılır. Bu biçim kodu değerleri varyansın pozitif veya negatif olmasından bağımsız olarak varyansın büyüklüğüne göre sıralar.
- **SORTDESC**: Raporu belirtilen sütundaki değerlere göre azalan sırada sıralar.
- **ASORTDESC**: Raporu belirtilen sütundaki değerlerin mutlak değerine göre azalan sırada sıralar.

### <a name="select-a-sorting-code"></a>Sıralama kodu seçme

1. Report Designer'da **Satır tanımları** öğesine tıklayın ve ardından değiştirmek için satır tanımını açın.
2. **Biçim kodu** hücresine çift tıklayın ve ardından bir sıralama kodu seçin.
3. **İlgili Formüller/Satırlar/Birimler** hücresinde, sıralanacak satır kodları aralığını belirtin. Aralık belirtmek için ilk satır kodunu, bir iki nokta üst üste işareti (:) ve ardından son satır kodunu girin. Örneğin, aralığın 160. satır ila 490. satır arasında olduğunu belirtmek için **160:490** girin.
4. **Sütun kısıtlama** hücresinde sıralama için kullanılacak rapor sütunu harfini girin.

    > [!NOTE]
    > Bir satır hesaplamasına sadece tutar satırlarını dahil edin.

### <a name="examples-of-ascending-and-descending-column-values"></a>Artan ve azalan sütun değerlerine örnekler

Aşağıdaki örnekte, raporun D sütunundaki değerler 160 ile 490 arasındaki satırlar için artan düzende sıralanır. Buna ek olarak, raporun G sütunundaki mutlak değerler 610 ile 940 arasındaki satırlar için azalan düzende sıralanır.

| Satır kodu | Açıklama                             | Biçim kodu | İlgili Formüller/Satırlar/Birimler | Normal bakiye | Sütun kısıtlama | Mali boyutlara bağlantı |
|----------|-----------------------------------------|-------------|-----------------------------|----------------|--------------------|------------------------------|
| 100      | Aylık Varyansa Göre Artan Sırada Sıralanmış       | DES         |                |                |                    |                              |
| 130      |                                        | SORT        | 160:490                     |                | D                  |                              |
| 160      | Satış                                   |             |                             | C              |                    | 4100                         |
| 190      | Satış İadeleri                        |             |                             |                |                    | 4110                         |
|          | ...                             |             |                             |                |                    |                              |
| 490      | Faiz Geliri              |             |                             | C              |                    | 7000                         |
| 520      |                                     | DES         |                             |                |                    |                              |
| 550      | YTD Mutlak Varyansına Göre Azalan Sırada Sıralanmış | DES         |             |                |                    |                              |
| 580      |                              | ASORTDESC   | 610:940                     |                | G                  |                              |
| 610      | Satış                     |             |                             | Ş              |                    | 4100                         |
| 640      | Satış İadeleri                |             |                             |                |                    | 4110                         |
|          | ...                       |             |                             |                |                    |                              |
| 940      | Faiz Geliri               |             |                             | A              |                    | 7000                         |


## <a name="specify-a-format-override-cell"></a>Biçim geçersiz kılma hücresi belirtin
**Biçim geçersiz kılma** hücresi rapor yazdırıldığında satır için kullanılan biçimlendirmeyi belirtir. Bu biçimlendirme sütun tanımında ve rapor tanımında belirtilen biçimlendirmeyi geçersiz kılar. Varsayılan olarak bu tanımlarda belirtilen biçimlendirme para birimidir. Raporun bir satırı bina sayısı gibi varlık sayısını, başka bir satır ise bu varlıkların parasal değerini belirtirse para birimi biçimlendirmesini geçersiz kılarak bina sayısını belirten satır için sayısal biçimlendirme girebilirsiniz. Bu bilgileri **Biçim geçersiz kılma** iletişim kutusunda belirtin. Kullanılabilir seçenekler seçtiğiniz biçim kategorisine bağlıdır. İletişim kutusunun **Örnek** alanı örnek biçimleri gösterir. Aşağıdaki biçim kategorileri kullanılabilir:

- Para birimi biçimlendirmesi
- Sayısal biçimlendirme
- Yüzde biçimlendirmesi
- Özel biçimlendirme

### <a name="override-cell-formatting"></a>Geçersiz kılma hücresi biçimlendirmesi

1. Report Designer'da, değiştirilecek satır tanımını açın.
2. Biçim geçersiz kılma satırında, **Biçim geçersiz kılma** sütunundaki hücreye çift tıklayın.
3. **Biçim geçersiz kılma** iletişim kutusunda, rapordaki söz konusu satır için kullanacağınız biçimlendirme seçeneklerini seçin.
4. **Tamam** düğmesini tıklatın.

### <a name="currency-formatting"></a>Para birimi biçimlendirmesi

Para birimi biçimlendirmesi mali bir tutara uygulanır ve para birimi simgesini içerir. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Para birimi simgesi**: Raporun para birimi simgesi. Bu değer şirket bilgileri için **Bölgesel Seçenekler** ayarını geçersiz kılar.
- **Negatif sayılar**: Negatif sayılar eksi işaretine (-) sahip olabilir, parantez içinde görünebilir veya bir üçgen işaretine (∆) sahip olabilir.
- **Ondalık basamaklar**: Virgülden sonra gösterilecek basamak sayısı.
- **Sıfır değeri atlatma metni**: Tutar, 0 (sıfır) olduğunda rapora eklenecek metindir. Bu metin **Örnek** alanında son satır olarak görüntülenir.

    > [!NOTE]
    > Yazdırma işlemi sıfır değerleri veya aktif olmayan dönem için baskılanırsa bu metin de baskılanır.

### <a name="numeric-formatting"></a>Sayısal biçimlendirme

Sayısal biçimlendirme her türlü tutara uygulanır ve para birimi simgesi içermez. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Negatif sayılar**: Negatif sayılar eksi işaretine (-) sahip olabilir, parantez içinde görünebilir veya bir üçgen işaretine (∆) sahip olabilir.
- **Ondalık basamaklar**: Virgülden sonra gösterilecek basamak sayısı.
- **Sıfır değeri atlatma metni**: Tutar, 0 (sıfır) olduğunda rapora eklenecek metindir. Bu metin **Örnek** alanında son satır olarak görüntülenir.

    > [!NOTE]
    > Yazdırma işlemi sıfır değerleri veya aktif olmayan dönem için baskılanırsa bu metin de baskılanır.

### <a name="percentage-formatting"></a>Yüzde biçimlendirmesi

Yüzde biçimlendirme yüzde işaretini (%) içerir. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Negatif sayılar**: Negatif sayılar eksi işaretine (-) sahip olabilir, parantez içinde görünebilir veya bir üçgen işaretine (∆) sahip olabilir.
- **Ondalık basamaklar**: Virgülden sonra gösterilecek basamak sayısı.
- **Sıfır değeri atlatma metni**: Tutar, 0 (sıfır) olduğunda rapora eklenecek metindir. Bu metin **Örnek** alanında son satır olarak görüntülenir.

    > [!NOTE]
    > Yazdırma işlemi sıfır değerleri veya aktif olmayan dönem için baskılanırsa bu metin de baskılanır.

### <a name="custom-formatting"></a>Özel biçimlendirme

Özel bir biçim geçersiz kılma işlemi oluşturmak için özel biçimlendirme kategorisini kullanın. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Tür**: Özel biçim.
- **Sıfır değeri atlatma metni**: Tutar, 0 (sıfır) olduğunda rapora eklenecek metindir. Bu metin **Örnek** alanında son satır olarak görüntülenir.

    > [!NOTE]
    > Yazdırma işlemi sıfır değerleri veya aktif olmayan dönem için baskılanırsa bu metin de baskılanır.

Tür pozitif değeri ve ardından negatif değeri temsil etmelidir. Genellikle pozitif ve negatif değerleri birbirinden ayıran benzer bir biçim girebilirsiniz. Örneğin, hem pozitif hem negatif değerlerin iki ondalık basamağa sahip olmasını, ancak negatif değerlerin parantez içinde görüntülenmesini belirtmek için **0.00;(0.00)** girin. Aşağıdaki tabloda, değerlerinizin biçimini kontrol etmek için kullanabileceğiniz özel biçimler gösterilmektedir. Tüm örnekler 1234.56 değerinden başlamaktadır.

| Biçim                         | Pozitif   | Eksi     | Sıfır    |
|--------------------------------|------------|--------------|---------|
| 0                              | 1235       | -1235        | 0       |
| 0;0                            | 1235       | 1235         | 0       |
| 0;(0);-                        | 1235       | 1235         | -       |
| \#,\#\#\#;(\#,\#\#\#);""       | 1.235      | (1.235)      | (Boş) |
| \#,\#\#0.00;(\#,\#\#0.00);sıfır | 1,234.56   | (1.234,56)   | sıfır    |
| %0,00;(%0,00)                  | %123456,00 | (123456.00%) | 0.00%   |

## <a name="specify-a-normal-balance-cell"></a>Normal Bakiye hücresi belirtme
Bir satır tanımındaki **Normal Bakiye** hücresi bir satırdaki tutarların işaretini kontrol edin. Bir satırın işaretini ters çevirmek veya bir hesabın normal bakiyesi bir borç ise, bu satır **Normal bakiye** hücresine **C** yazın. Rapor tasarımcısı o satırdaki tüm borç bakiyesi hesaplarının işaretini ters çevirir. Report Designer bu hesapları ters çevirdiğinde tüm tutarlardan alacak/borç özelliğini kaldırır ve böylece toplama işlemi kolaylaşır. Örneğin, net geliri hesaplamak için giderleri gelirlerden çıkarırsınız. Genellikle, toplanan ve hesaplanan satırlar **C** kodundan etkilenmez. Ancak, sütun tanımındaki **XCR** yazdırma denetimi, **Normal bakiye** sütununda bir **C** içeren her türlü satırın işaretini ters çevirir. Bu biçimlendirme özellikle tüm olumsuz varyansları negatif tutarlar olarak göstermek istediğinizde önemlidir. Toplanan veya hesaplanan sayı yanlış işarete sahipse işareti ters çevirmek için satırın **Normal bakiye** hücresine bir **C** girin.

## <a name="specify-a-row-modifier-cell"></a>Satır değiştirici hücre belirtin
Bir satır tanımındaki **Satır değiştirici** hücresinin içeriği söz konusu satıra ait sütun tanımında belirtilen mali yıllar, dönemler ve diğer bilgileri geçersiz kılar. Seçilen değiştirici satırdaki her hesaba uygulanır. Aşağıdaki değiştirici türlerinden birini veya daha fazlasını kullanarak her satırı değiştirebilirsiniz:

- Hesap değiştiriciler
- Defter kodu değiştiriciler
- Hesap ve hareket öznitelikleri

### <a name="override-a-column-definition"></a>Bir sütun tanımını geçersiz kılma

1. Report Designer'da, değiştirilecek satır tanımını açın.
2. Sütun tanımını geçersiz kılmak istediğiniz satırda, **Satır değiştirici** hücresine çift tıklayın.
3. **Satır değiştirici** iletişim kutusunda, **Hesap değiştirici** alanında bir seçenek seçin. Seçeneklerin açıklaması için "Hesap değiştiriciler" bölümüne bakın.
4. **Defter kodu değiştirici** alanında, satır için kullanılacak defter kodunu seçin.
5. **Öznitelikler**'in altında, satır koduyla eklenmesi gereken her öznitelik için bir giriş eklemek üzere şu adımları izleyin:

    1. **Öznitelik** hücresine çift tıklayın ve bir öznitelik adı seçin.

        > [!IMPORTANT]
        > Sayı işaretini (\#) sayısal bir değerle değiştirin.

    2. **Başlangıç** hücresine çift tıklayın ve aralığın ilk değerini girin.
    3. **Bitiş** hücresine çift tıklayın ve aralığın son değerini girin.

6. **Tamam** düğmesini tıklatın.

### <a name="account-modifiers"></a>Hesap değiştiriciler

Belirli bir hesap seçtiğinizde, rapor tasarımcısı genellikle sütun tanımında belirlediğiniz hesabı ve mali yılları, dönemleri ve diğer bilgileri birleştirir. Belirli satırlar için farklı mali yıllar gibi farklı bilgiler kullanabilirsiniz. Aşağıdaki tabloda kullanılabilecek hesap değiştiriciler gösterilmiştir. Sayı işaretini (\#) bir mali yıl içindeki dönemlerin sayısına eşit veya bundan daha düşük bir değerle değiştirin.

| Hesap değiştirici | Ne yazdırılır                                                                           |
|------------------|-------------------------------------------------------------------------------------------|
| /BB              | Bir hesap için başlangıç bakiyesi.                                                     |
| /\#              | Belirtilen dönem için bakiye.                                                     |
| /-\#             | Mevcut dönem öncesindeki \# dönem için dönem bakiyesi.                  |
| /+\#             | Mevcut dönem sonrasındaki \# dönem için dönem bakiyesi.                   |
| /C               | Mevcut dönem için bakiye.                                                       |
| /C-\#            | Mevcut dönem öncesindeki \# dönem için dönem bakiyesi.                  |
| /C+\#            | Mevcut dönem sonrasındaki \# dönem için dönem bakiyesi.                   |
| /Y               | Geçerli dönem üzerinden yılın bugüne kadarki bakiyesi.                                      |
| /Y-\#            | Mevcut dönemden \# dönem önce olan dönem üzerinden yılın bugüne kadarki bakiyesi. |
| /Y+\#            | Mevcut dönemden \# dönem sonra olan dönem üzerinden yılın bugüne kadarki bakiyesi.  |

### <a name="book-code-modifiers"></a>Defter kodu değiştiriciler

Bir satırı mevcut bir defter koduyla sınırlayabilirsiniz. Sütun tanımı bir defter koduna sahip olan en az bir **FD** sütunu içermelidir.

> [!NOTE]
> Bir satır için defter kodu kısıtlaması, o satır için sütun tanımındaki defter kodu kısıtlamalarını atlatır.

### <a name="account-and-transaction-attributes"></a>Hesap ve hareket öznitelikleri

Bazı muhasebe sistemleri, mali verilerdeki hesap özniteliklerini ve hareket özniteliklerini destekler. Bu öznitelikler sanal hesap segmentleri gibi çalışır ve hesap veya hareket hakkında ek bilgiler taşıyabilir. Bu ek bilgiler hesap kodları, toplu iş kodları, posta kodları ve diğer öznitelikler olabilir. Muhasebe sisteminiz öznitelikleri destekliyorsa satır tanımında hesap özniteliklerini veya hareket özniteliklerini satır değiştiriciler olarak kullanabilirsiniz. Satır bilgilerini geçersiz kılma hakkında bilgi için, bu makalenin önceki kısmındaki "Bir sütun tanımını geçersiz kılma" bölümüne bakın.

## <a name="specify-a-link-to-financial-dimensions-cell"></a>Mali boyutlarla bağlantı hücresi belirtin
**Mali boyutlara bağlantı** hücresi bir raporun her satırına eklenmesi gereken mali verilerin bağlantılarını içerir. Bu hücre boyut değerlerini içerir. **Boyutlar** iletişim kutusunu açmak için **Mali boyutlara bağlantı** hücresine çift tıklayın.

> [!NOTE]
> Report Designer Microsoft Dynamics 365 Finance sisteminden şu ayrılmış karakterlerden herhangi birini içeren hesaplar, boyutlar veya alanları seçemez: &, \*, \[, \], {, veya }. Zaten satır tanımında yer alan bir satıra ait bilgileri belirtmek için, bilgileri **Mali boyutlara bağlantı** hücresine ekleyin. Mali verilerle ilişkilendirilen yeni satırlar eklemek için, rapor tanımında yeni satırlar oluşturmak için **Şuradan satır ekle:** iletişim kutusunu kullanın. Aşağıdaki tabloda gösterildiği gibi sütunun nasıl yapılandırıldığına bağlı olarak sütun başlığı değişir.

| Seçilen bağlantı türü       | Bağlantı sütununun açıklaması şu şekilde değişir |
|----------------------------------|----------------------------------------------------|
| Mali Boyutlar             | Mali Boyutlarla İlişkilendir                       |
| Rapor Çalışma sayfası                 | Mali Raporlamalar Raporu                         |

### <a name="specify-a-dimension-or-range"></a>Boyut veya aralık belirtme

1. Report Designer'da, değiştirilecek satır tanımını açın.
2. **Mali boyutlara bağlantı** sütunundaki bir hücreye çift tıklayın.
3. **Boyutlar** iletişim kutusunda, boyut adının altındaki bir hücreye çift tıklayın.
4. Boyuta ait iletişim kutusunda, **Tek veya aralık**'ı seçin.
5. **Başlangıç** alanına başlangıç boyutunu girin veya ![Gözat.](media/browse.gif "Gözat") düğmesini tıklayarak kullanılabilir boyutları arayın. Boyut aralığı girmek için **Bitiş** alanına bitiş boyutunu girin.
6. **Tamam**'a tıklayarak boyuta ait iletişim kutusunu kapatın. **Boyutlar** iletişim kutusu güncelleştirilniş boyutu veya aralığı görüntüler.
7. **Tamam**'a tıklayarak **Boyutlar** iletişim kutusunu kapatın.

## <a name="display-zero-balance-accounts-in-a-row-definition"></a>Bir satır tanımında sıfır bakiye hesaplarını görüntüleme
Varsayılan olarak, rapor tasarımcısı mali verilerinde karşılık gelen bir bakiye bulunmayan hiçbir satırı yazdırmaz. Bu nedenle, tüm ana hesap kodu segmenti değerlerini veya tüm boyut değerlerini içeren bir satır tanımı oluşturabilir ve ardından bu satır tanımını departmanlarınızdan biri için kullanabilirsiniz.

### <a name="modify-zero-balance-settings"></a>Sıfır bakiye ayarlarını değiştirme

1. Report Designer'da, değiştirilecek rapor tanımını açın.
2. **Ayarlar** sekmesinde, **Diğer biçimlendirme**'nin altında rapor tanımında kullanılan satır tanımına ilişkin seçenekleri seçin.
3. Yaptığınız değişiklikleri kaydetmek için **Dosya** menüsünde **Kaydet**'e tıklayın.

## <a name="use-wildcard-characters-and-ranges-in-a-row-definition"></a>Bir satır tanımında joker karakterleri ve aralıkları kullanma
**Boyutlar** iletişim kutusuna bir doğal segment değeri girdiğinizde, bir segmentin herhangi bir konumuna bir joker karakter (? veya \*) girebilirsiniz. Rapor tasarımcısı, joker karakterleri dikkate almadan tanımlanan konumlar için tüm değerleri ayıklar. Örneğin, satır tanımı yalnızca doğal segment değerlerini içeriyor ve doğal segmentler dört karaktere sahip. Bir satıra **6???** girerek rapor tasarımcısına 6 ile başlayan bir doğal segment değerine sahip tüm hesapları dahil etmesini söylersiniz. **6\**_ girerseniz aynı sonuçlar döndürülür ancak sonuçlar _* 60** ve **600000** gibi değişken genişliği değerleri de içerir. Rapor tasarımcısı her bir joker karakterini (?) harfler ve özel karakterler içeren tam bir olası değer aralığıyla değiştirir. Örneğin,**12?0** ile **12?4** arasındaki aralıkta, **12?0** altındaki joker karakteri, karakter setindeki en düşük değerle değiştirilir ve **12?4** altındaki joker karakteri, karakter setindeki en yüksek değerle değiştirilir.

> [!NOTE]
> Aralığın başlangıç ve bitiş hesapları için joker karakterler kullanmaktan kaçınmalısınız. Başlangıç hesabında veya bitiş hesabında joker karakterleri kullanırsanız beklenmedik sonuçlarla karşılaşabilirsiniz.

### <a name="single-segment-or-single-dimension-ranges"></a>Tek segmentli veya tek boyutlu aralıklar

Bir segment değerleri veya boyut değerleri aralığı belirtebilirsiniz. Bir aralık belirlemenin avantajı, mali verilere yeni bir segment değeri veya boyut değeri eklendiğinde her defasında satır tanımını güncelleştirmenize gerek kalmamasıdır. Örneğin, **+Hesap=\[6100:6900\]** aralığı, 6100 ile 6900 arasındaki hesaplardan değerleri satır tutarına çeker. Bir aralık bir joker karakter (?) içeriyorsa, rapor tasarımcısı aralığı karakterlere dayalı bir şekilde değerlendirmez. Bunun yerine, aralığın düşük ve yüksek noktaları belirlenir ve ardından bitiş değerleri ve bunlar arasında kalan tüm değerler dahil edilir.

> [!NOTE]
> Report Designer Microsoft Dynamics 365 Finance sisteminden şu ayrılmış karakterlerden herhangi birini içeren hesaplar, boyutlar veya alanları seçemez: &, \*, \[, \], {, veya }. **Boyutlardan satır ekle** iletişim kutusunu kullanarak yalnızca otomatik olarak satır tanımları oluştururken ampersand (&) ekleyebilirsiniz.

### <a name="multiple-segment-or-multiple-dimension-ranges"></a>Birden fazla segment veya birden fazla boyut bulunan aralıklar

Birden fazla boyut değeri içeren birleşimleri kullanarak bir aralık girdiğinizde aralık karşılaştırması ..\\mali-boyutlar\\tek tek boyutlar temelinde yapılır. Aralık karşılaştırması karakter karakter veya kısmi segment temelinde yapılamaz. Örneğin, **+Hesap=\[5000:6000\], Departman=\[1000:2000\], Maliyet merkezi=\[00\]** aralığı sadece her bir segmentle eşleşen hesapları içerir. Bu senaryoda, ilk boyut 5000-6000 aralığında olmalıdır, ikinci boyut 1000 ile 2000 aralığında olmalıdır ve son boyut 00 olmalıdır. Örneğin, **+Hesap=\[5100\], Departman=\[1100\], Maliyet merkezi=\[01\]** son segment belirtilen aralık dışında olduğundan rapora dahil edilmez. Bir segment değeri boşluk içeriyorsa, değeri köşeli parantez (\[ \]) içine alın. Aşağıdaki değerler dört karakterli bir segment için geçerlidir: **\[ 234\], \[123 \], \[1 34\]**. Boyut değerleri köşeli parantez (\[ \]) içine alınmalıdır ve rapor tasarımcısı bu köşeli parantezleri sizin için ekler. Birden fazla segment veya birden fazla boyut aralığı joker karakterleri (? veya \*) içerdiğinde, tüm çoklu segment veya çoklu boyut aralığının düşük ve yüksek noktaları belirlenir ve ardından bitiş değerleri ve bunlar arasında kalan tüm değerler dahil edilir. Örneğin 40000 ile 99999 arasındaki tüm hesap aralığı gibi geniş bir aralığa sahipseniz, mümkün olduğu durumlarda geçerli bir başlangıç hesabı ve bitiş hesabı belirtmelisiniz.

> [!NOTE] 
> Report Designer Microsoft Dynamics 365 Finance sisteminden şu ayrılmış karakterlerden herhangi birini içeren hesaplar, boyutlar veya alanları seçemez: &, \*, \[, \], {, veya }. **Boyutlardan satır ekle** iletişim kutusunu kullanarak yalnızca otomatik olarak satır tanımları oluştururken ampersand (&) ekleyebilirsiniz.

## <a name="add-or-subtract-from-other-accounts-in-a-row-definition"></a>Bir satır tanımındaki diğer hesaplarda toplama veya çıkarma işlemi yapma
Bir hesaptaki parasal tutarları başka bir hesaptaki parasal tutarlara eklemek veya bunlardan çıkarmak için, **Mali Boyutlarla İlişkilendir** hücresinde artı işareti (+) ve eksi işareti (-) kullanabilirsiniz. Aşağıdaki tablo mali verilere bağlantı eklemek veya bunlardaki bağlantıları kaldırmak için uygun biçimleri göstermektedir.

| İşlem                                            | Bu biçimi kullanma                                                                                              |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| İki tam donanımlı hesap ekleyin.      | +Bölüm=\[000\], Hesap=\[1205\], Departman=\[00\]+Bölüm=\[100\], Hesap=\[1205\], Departman=\[00\] |
| İki segment değeri ekleyin.                    | +Hesap=\[1205\]+Hesap=\[1210\]                                                                           |
| Joker karakterleri içeren segment değerleri ekleyin.  | +Hesap=\[120?+Hesap=\[11??\]                                                                     |
| Bir tam donanımlı hesap aralığı ekleyin.              | +Bölüm=\[000:100\], Hesap=\[1205\], Departman=\[00\]                                           |
| Bir segment değeri aralığı ekleyin.                | +Hesap=\[1200:1205\]                                                                                       |
| Joker karakterleri içeren bir segment değeri aralığı ekleyin.         | +Hesap=\[120?:130?\]                                                           |
| Bir tam donanımlı hesabı başka bir tam donanımlı hesaptan çıkarın.              | +Bölüm=\[000\], Hesap=\[1205\], Departman=\[00\]-Bölüm=\[100\], Hesap=\[1205\], Departman=\[00\] |
| Bir segment değerini başka bir segment değerinden çıkarın.          | +Hesap=\[1205\]-Hesap=\[1210\]                                                               |
| Bir joker karakteri içeren segment değerini başka bir segment değerinden çıkarın. | +Hesap=\[1200\]-Hesap=\[11??\]                                        |
| Bir tam donanımlı hesap aralığını çıkarın.                               | -Bölüm=\[000:100\], Hesap=\[1200:1205\], Departman=\[00:01\]                   |
| Bir segment değeri aralığını çıkarın.                   | -Hesap=\[1200:1205\]                                                                                       |
| Joker karakterleri içeren bir segment değeri aralığını çıkarın.                    | -Hesap=\[120?:130?\]                                               |

Hesapları doğrudan değiştirebilirsiniz, ancak mali veri bağlantılarına doğru biçimlendirmeyi uygulamak için **Boyutlar** iletişim kutusunu da kullanabilirsiniz. Değerlerden herhangi biri joker karakterler (? veya  \*) içerebilir. Ancak, Rapor Tasarımcısı Microsoft Dynamics ERP sisteminden şu ayrılmış karakterlerden herhangi birini içeren hesaplar, boyutlar veya alanları seçemez: &, \*, \[, \], {, veya }.

> [!NOTE]
> Değerleri çıkarmak için bu değerler etrafına parantez eklemelisiniz. Örneğin **450?-(4509)** girerseniz **+Hesap\[4509\]-Hesap=\[450?\]** olarak görüntülenir ve rapor tasarımcısına 4509 hesap segmenti için tutarı 450 ile başlayan herhangi bir hesap segmenti tutarından çıkarma komutu vermiş olursunuz.

### <a name="add-or-subtract-accounts-from-other-accounts"></a>Hesapları diğer hesaplarla toplama veya bunlardan çıkarma

1. Report Designer'da, değiştirilecek satır tanımını açın.
2. İlgili satırda, **Mali boyutlara bağlantı** sütunundaki hücreye çift tıklayın.
3. **Boyutlar** iletişim kutusunun ilk satırında, şu adımları izleyin:

    1. İlk alanda tüm boyutları (varsayılan) seçin veya **Boyut kümelerini yönet** iletişim kutusunu açmak üzere tıklayın; burada bir set oluşturabilir veya mevcut bir seti değiştirebilir, kopyalayabilir veya silebilirsiniz.
    2. **İşleç +/-** hücresini çift tıklayın ve satırdaki bir veya daha fazla sayıdaki boyut değerine veya sete uygulanacak artı (**+**+) veya eksi (**-**) işlecini seçin.
    3. İlgili boyut değeri sütununda, **Boyutlar** iletişim kutusunu açmak için hücreye çift tıklayın ve bu boyut değerinin tek mi yoksa aralık, boyut değeri kümesi veya toplam alma hesapları mı olduğunu seçin. **Boyutlar** iletişim kutusundaki alanların açıklamaları için, "Boyut iletişim kutusunun açıklaması" bölümüne bakın.
    4. **Başlangıç** ve **Bitiş** sütunlarına segment değerlerini girin.

4. Daha fazla işleç eklemek için 2 ile 3. adımlar arasındaki işlemleri tekrarlayın.

> [!NOTE]
> İşleç, satırdaki tüm boyutlar için geçerlidir.

## <a name="description-of-the-dimensions-dialog-box"></a>Boyut açıklaması iletişim kutusu
Aşağıdaki tabloda **Boyutlar** iletişim kutusundaki alanlar açıklanmaktadır.

| Madde                | Açıklama |
|---------------------|-------------|
| Tek veya aralık | **Başlangıç** alanında, bir hesabın adını girin veya hesabı aramak için **Gözat** düğmesini ![Gözat.](media/browse.gif "Gözat") tıklayın. Aralık seçmek için **Bitiş** alanına bir değer girin veya bu alanda bir değere göz atın. |
| Boyut Değeri Kümesi | **Ad** alanına boyut değeri kümesinin adını girin. Bir kümeyi oluşturmak, değiştirmek, kopyalamak veya silmek için, **Boyut Değeri Kümelerini Yönet**'e tıklayın. **Formül** alanı, satır tanımında ayarlanan bu boyut değeri için **Mali boyutlara bağlantı** hücresindeki formülle doldurulur. |
| Toplam alma hesapları   | **Ad** alanına toplam alma hesaplarına ait bir boyut girin veya bu boyuta göz atın. **Formül** alanı rapor tanımındaki bu toplam alma hesabına ait **Mali boyutlara bağlantı** hücresindeki formülle doldurulur. |

## <a name="add-dimension-value-sets-in-a-row-definition"></a>Bir satır tanımına boyut değeri kümeleri ekleme
Boyut değeri kümesi, adlandırılmış bir boyut değerleri grubudur. Bir boyut değeri kümesi yalnızca tek bir boyuttaki değerleri içerebilir, ancak birden fazla satır tanımı, sütun tanımı, raporlama ağacı tanımı ve rapor tanımında bir boyut değeri kümesi kullanabilirsiniz. Ayrıca, bir rapor tanımındaki boyut değerlerini de birleştirebilirsiniz. Mali değerlerinizde yapılan bir değişiklik boyut değeri kümesini değiştirmenizi gerektirdiğinde, boyut değeri kümesi tanımını güncelleştirebilir ve bu güncelleştirme boyut değeri kümesini kullanan tüm alanlara uygulanır. Örneğin, mali verilerinizi ilişkilendirmek için sıkça 5100 ila 5600 arasındaki değerler gibi bir değer aralığını belirtiyorsanız bu aralığı Satış adındaki bir hesap kümesine atayabilirsiniz. Bir boyut değerleri kümesi oluşturmanızın ardından, mali veri bağlantınız olarak bu kümeyi seçebilirsiniz. Başka bir örnek olarak, 5100 ila 5600 arasındaki değer aralığı Satışa, 4175 ise İskontolara atanırsa toplam satışı İskontoları Satıştan çıkararak belirleyebilirsiniz. Bu işlem **(5100:5600)-4175** olarak gösterilir.

### <a name="create-a-set-of-dimension-values"></a>Boyut değerleri kümesi oluşturma

1. Report Designer'da, değiştirilecek satır, sütun veya ağaç tanımını açın.
2. **Düzenle** menüsünde, **Boyut değeri kümelerini yönet**'e tıklayın.
3. **Boyut değeri kümelerini yönet** iletişim kutusundaki **Boyut** alanında, oluşturulacak boyut değeri kümesinin türünü seçin ve ardından **Yeni**'ye tıklayın.
4. **Yeni** iletişim kutusunda küme için ad ve açıklama girin.
5. **Başlangıç** sütununda, bir hücreye çift tıklayın.
6. **Hesap** iletişim kutusunda, listeden hesap adını seçin veua **Arama** alanında girişi arayın. Ardından **Tamam**'a tıklayın.
7. Söz konusu işleç için formül tasarlamak üzere **Bitiş** sütunundaki 5 ila 6. adımları tekrarlayın.
8. Formül tamamlandığında, **Tamam**'a tıklayın.
9. **Boyut kümelerini yönet** iletişim kutusunda, **Kapat**'a tıklayın.

### <a name="update-a-set-of-dimension-values"></a>Bir boyut değerleri kümesini güncelleştirme

1. Report Designer'da, değiştirilecek satır, sütun veya ağaç tanımını açın.
2. **Düzenle** menüsünde, **Boyut değeri kümelerini yönet**'e tıklayın.
3. **Boyut değeri kümelerini yönet** iletişim kutusundaki **Boyut** alanından boyut türünü seçin.
4. Listeden güncelleştirilecek boyut değeri kümesini seçin ve ardından **Değiştir**'e tıklayın.
5. **Değiştir** iletişim kutusunda, sete dahil edilecek formül değerlerini değiştirin.

    > [!NOTE]
    > Yeni hesaplar veya boyutlar eklerseniz, değişiklikleri dahil etmek için mevcut boyut değeri setlerini değiştirdiğinizden emin olun.

6. Hücreye çift tıklayın ve ilgili işleci, **Başlangıç** hesabını ve **Bitiş** hesabını seçin.
7. **Tamam**'a tıklayarak **Değiştir** iletişim kutusunu kapatın ve yaptığınız değişiklikleri kaydedin.

### <a name="copy-a-dimension-set"></a>Bir boyut kümesini kopyalama

1. Report Designer'da, değiştirilecek satır, sütun veya ağaç tanımını açın.
2. **Düzenle** menüsünde, **Boyut değeri kümelerini yönet**'e tıklayın.
3. **Boyut değeri kümelerini yönet** iletişim kutusundaki **Boyut** alanından boyut türünü seçin.
4. Listeden kopyalanacak kümeyi seçin ve ardından **Farklı Kaydet**'e tıklayın.
5. Kopyalanan küme için yeni bir ad girin ve ardından **Tamam**'a tıklayın.

### <a name="delete-a-dimension-set"></a>Bir boyut kümesini silme

1. Report Designer'da, değiştirilecek satır, sütun veya ağaç tanımını açın.
2. **Düzenle** menüsünde, **Boyut değeri kümelerini yönet**'e tıklayın.
3. **Boyut değeri kümelerini yönet** iletişim kutusundaki **Boyut** alanından boyut türünü seçin.
4. Silinecek kümeyi seçin ve ardından **Sil**'e tıklayın. Boyut değeri kümesini kalıcı olarak silmek için **Evet**'e tıklayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlama](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
