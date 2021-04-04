---
title: Finansal raporlamada gelişmiş biçimlendirme seçenekleri
description: Bu konuda filtreler, sınırlamalar, yazdırılmayan satırlar ve hesaplamalarda koşullu deyimler dahil olmak üzere gelişmiş biçimlendirme işlevleri açıklanmaktadır.
author: panolte
manager: AnnBe
ms.date: 04/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106571
ms.assetid: 895b5127-01d6-4495-b127-343387b743aa
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 08659bac84b07f6e95a83b84612cb035b51cf28d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568478"
---
# <a name="advanced-formatting-options-in-financial-reporting"></a>Finansal raporlamada gelişmiş biçimlendirme seçenekleri

[!include [banner](../includes/banner.md)]

Finansal raporlamada bir rapor oluşturduğunuzda, ek biçimlendirme işlevleri mevcuttur; boyutlar için filtreler, sütunlar ve raporlama birimleri için kısıtlamalar, yazdırılmayan satırlar ve hesaplamalarda THEN/IF/ELSE deyimleri de dahil olmak üzere.

Aşağıdaki tablo, rapor tasarlarken kullanılabilir olan gelişmiş biçimlendirme işlevlerini açıklar.

| İşlev                   | Açıklama |
|----------------------------|-------------|
| Boyut filtresi           | Belirli veri kümelerine erişmek için satır tanımında ve sütun tanımında boyutları kullanabilirsiniz. Raporların çoğu satır biçimlendirmede yalnızca doğal segment kullanır. Ancak, satırlar boyut değerlerini içerecek biçimde değiştirilebilir. Sütun tanımında boyut filtreleri, belirli boyut değerlerine erişmek için kullanılır. |
| Raporlama birimi kısıtlama | Rapor satırını yalnızca belirli bir raporlama birimine bağlı bilgileri gösterecek biçimde ayarlayabilirsiniz. |
| Yazdırılmayan (NP) satırları     | Yazdırılmayan satırlar birçok raporda yararlı olur. Bir değer elde etmek için birçok hesaplama gerekiyorsa, bu hesaplamalar yazdırılan raporda gizlenebilir. Yazdırılmayan satırları ayrıca rapor tasarımları ve gelişmiş hücre yerleşimi sorun giderme için yararlıdır. |
| Sütun kısıtlama         | Satır tanımında sütun kısıtlaması yalnızca raporun bazı satırlarında ilgili değerleri gizlemek için yararlıdır. Bir satırda yüzde hesaplamaları gerçekleştirildiğinde, sütun kısıtlama toplam sütunları veya diğer sütunların, bu numaraları geçerli olmadığında yazdırılmasını önler. |
| Sütun sonu               | Yan yana rapor bilgilerini göstermek için bir satır tanımına sütun sonları ekleyebilirsiniz. Tek bir satır tanımı içinde birden çok sütun sonları ekleyebilirsiniz ve sütun başlıkları sütun sonundan sonra her sütunun üstünde yinelenir. Bir rapor için açıklamalar sütun sonları arasında görüntülenir. |
| IF/THEN/ELSE deyimi     | Bir satır tanımı veya bir sütun tanımında hesaplamaları değiştirebilirsiniz. |
| Boyut değerleri için tek tırnak ('') ve ampersan (&) işaretini kullanın | Rapor tasarımı için ampersan işareti dahil boyut değerlerini kullanabilirsiniz. |

## <a name="advanced-cell-placement"></a>Gelişmiş hücre yerleştirme

Gelişmiş hücre yerleştirme veya *zorlama*, belirli değerlerin belirli hücrelere yerleşimini içerir. Örneğin, zorlamak genellikle doğru bakiyeyi bir nakit akış tablosu içinde taşımak için kullanılır. Aşağıdaki amaçlarla zorlarsınız:

- Değerleri Microsoft Excel'den belirli hücrelere taşıma.
- Bir rapora belirli değerleri sabit kodlar.
- Bir önceki hücreden bir değer kopyalayarak ve bu değeri -1 ile çarparak işaretleri değiştirin.

> [!NOTE]
> Çoğu durumda, rapor tanımınızı sütun hesaplamaları satır hesaplamasından önce yapılacak biçimde yapılandırmanız gerekir. Bu yapılandırmayı tamamlamak için aşağıdaki adımları izleyin.
>
> 1. Rapor tanımını Rapor Tasarımcısı içinde açın.
> 2. **Ayarlar** sekmesinde, **Hesaplama önceliği** altında, **Önce sütun ve sonra satır hesaplama gerçekleştir**'i seçin.

## <a name="designing-the-report"></a>Raporu tasarlama

Bir rapor tasarlarken, değerlerin beklendiği gibi çekilmesinden emin olmak için önce tüm ayrıntı satırlarını oluşturmanız gerekir. Sonra son değerleri içeren ayrıntıyı bastırmak için **NP** (No yazdırma) biçimi geçersiz kılmayı ekleyin.

> [!IMPORTANT]
> **CAL** format kodunu satır tanımı içinde kullandığınızda hareket ayrıntısına kadar detaya gidemezsiniz.

Zorlamak için formüller aşağıdaki biçimi kullanır: &lt;hedef sütun&gt;=&lt;kaynak sütun&gt;.&lt;satır kodu&gt; Herhangi bir satırın ek yerleşimlerini bir virgül ve bir boşluk ile ayırın. İşte bir örnek: D=C.190,E=C.100

## <a name="examples-of-advanced-formatting-options"></a>Gelişmiş biçimlendirme seçenekleri örnekleri

Aşağıdaki örnekler satır tanımı ve temel nakit akışı raporu (örnek 1) ve bir istatistik raporu (örnek 2) zorlamak için sütun tanımı biçimlendirmenin nasıl olduğunu gösterir.

### <a name="example-1-basic-forcing"></a>Örnek 1: Temel zorlama

Aşağıdaki tablo temel zorlama kullanan bir satır tanımı örneği gösterir.

| Satır Kodu |           Tanım            | Biçim Kodu | İlgili Formüller/Satırlar/Birimler |        Satır Değiştirici        | Mali Boyutlarla İlişkilendir |
|----------|----------------------------------|-------------|-----------------------------|----------------------------|------------------------------|
| 100      | Dönemin Başlangıcındaki Nakit (NP) |             |                             | Hesap Değiştirici = \[/BB\] | +Segment2 = \[1100\]         |
| 130      | Dönemin Başlangıcındaki Nakit      | CAL         | C=C.100,F=D.100             |                            |                              |
| 160      |                                  |             |                             |                            |                              |
| 190      |                                  |             |                             |                            |                              |

> [!NOTE]
> Boş sütunlar önceki tablodan daha iyi görünürlük için kaldırılmıştır: Biçim Geçersiz Kılma, Normal Bakiye, Yazdırma Denetimi, Sütun Kısıtlama sütunları görüntülenmemektedir.

Aşağıdaki tablo satırda temel zorlama kullanan bir sütun tanımı örneği gösterir.

|           Biçim             | A   | B:    | A        | B      | E:      | C    |
|------------------------------|-----|------|----------|--------|--------|------|
| Başlık 1                     |     |      |          |        |        |      |
| Başlık 2                     | A   | B:    | A        | B      | E:      | C    |
| Başlık 3                     |     |      |          |        |        |      |
| Sütun Türü                  | SATIR | DESC | FD       | FD     | FD     | CALC |
| Defter Kodu/Öznitelik Kategorisi |     |      | ACTUAL   | ACTUAL | ACTUAL |      |
| Mali Yıl                  |     |      | BASE     | BASE   | BASE   |      |
| Dönem                       |     |      | BASE     | BASE   | BASE   |      |
| Kapsanan Dönemler              |     |      | PERIODIC | YTD/BB | YTD    |      |
| Formül                      |     |      |          |        |        | E-D  |
| Sütun Genişliği                 | 5   | 30   | 14       | 14     | 14     | 14   |

### <a name="example-2-statistical-reports"></a>Örnek 2: İstatistik raporları

Aşağıdaki tablo bir istatistik raporu için temel zorlama kullanan bir satır tanımı örneği gösterir.

| Satır Kodu | Açıklama               | Kodu biçimlendir | İlgili Formüller/Satırlar/Birimler     | Biçim Geçersiz Kılma      | Normal Bakiye | Mali Boyutlarla İlişkilendir               |
|----------|---------------------------|-------------|---------------------------------|----------------------|----------------|--------------------------------------------|
| 50       | İstatistiksel Bilgiler   | REM         |                                 |                      |                |                                            |
| 100      | Çalışan sayısı - ABD            | CAL         | 4                               | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 115      | Çalışan sayısı - Uluslararası | CAL         | 11                              | \#\#\#0.;($\#\#\#0.) |                |                                            |
| 130      |                           |             |                                 |                      |                |                                            |
| 190      | ABD Satış                  |             |                                 |                      | A              | +Segment2 = \[41\*\], Segment3 = \[00\]    |
| 220      | Uluslararası Satış       |             |                                 |                      | A              | +Segment2 = \[41\*\], Segment3 = \[01:99\] |
| 250      |                           |             |                                 |                      |                |                                            |
| 280      |                           |             |                                 |                      |                |                                            |
| 310      | ABD Satış                  | CAL         | D=C.190,E=C.100,F=(C.100/C.190) |                      |                |                                            |
| 340      | Uluslararası Satışlar       | CAL         | D=C.220,E=C115,F=(C.220/C.115)  |                      |                |                                            |

> [!NOTE]
> Boş sütunlar önceki tablodan daha iyi görünürlük için kaldırılmıştır: Yazdırma Denetimi, Sütun Kısıtlama ve Satır Değiştirici sütunları görüntülenmemektedir.

Aşağıdaki tablo bir istatistik raporu için temel zorlama kullanan bir sütun tanımı örneği gösterir.

|    Biçim                    | A   | B:    | A      | B            | E:     | C            |
|------------------------------|-----|------|--------|--------------|-------|--------------|
| Başlık 1                     | A   | B:    | A      | B            | E:     | C            |
| Başlık 2                     | -   | -    | YTD    | Yıllık satış | Personel | Kişi başına $ |
| Başlık 3                     |     |      |        |              |       |              |
| Sütun Tipi                  | SATIR | DESC | FD     | CALC         | CALC  | CALC         |
| Defter Kodu/Öznitelik Kategorisi |     |      | ACTUAL |              |       |              |
| Mali Yıl                  |     |      | BASE   |              |       |              |
| Dönem                       |     |      | BASE   |              |       |              |
| Kapsanan dönemler              |     |      | YILBAŞINDAN BUGÜNE    |              |       |              |
| Formül                      |     |      |        |              |       | E-D          |
| Sütun Genişliği                 | 5   | 30   | 14     | 14           | 14    | 14           |

## <a name="restricting-a-row-to-a-specific-reporting-unit"></a>Belirli bir raporlama birimi için bir satır sınırlama

Rapor satırı belirli bir raporlama birime kısıtlandığında, satır yalnızca adlandırılmış raporlama birimi için bağlantılı verileri gösterir ve diğer raporlama birimleri için raporlama ağacındaki verileri yok sayar. Örneğin, belirli bir bölüm için toplam işletme giderleri için ayrıntıları sağlayan bir satır oluşturabilirsiniz. Rapor hem raporlama ağacı hem de doğal hesaptan daha fazlasına sahip satır tanımını içeriyorsa, raporunuz yinelenen verileri içerebilir. Örneğin, kuruluşunuzdaki altı departmanı listeleyen bir raporlama ağacınız var ve satırda bir hesap ile bir departmanın belirli kombinasyonunu listeleyen satır tanımınız var. Rapor oluşturduğunuzda, bu bölüm ağaçta olanla eşleşmeyebilir olsa da bir hesap ve bir bölümün belirli bir bileşimi raporlama ağacının her düzeyi üzerine yazdırılır. Bu davranış oluşur, çünkü satır rapor tanımına göre genellikle filtreleneni geçersiz kalır. Verilerin yinelenmesini engellemek için bir yok, bir belirli bir raporlama birimi için bir satır kısıtlamaktır.

> [!NOTE]
> Satır boyutları içerirse ve o satırı alt raporlama birim için kısıtlarsanız satır tutarı, alt birimi ve onun üst birimleri için eklenmiştir, ancak hiçbir çoğaltma oluşmaz.

### <a name="restrict-a-row-to-a-reporting-unit"></a>Bir raporlama birimi için bir satır sınırlama

1. Report Designer'da **Satır Tanımları** öğesini tıklayın ve ardından değiştirilecek satır tanımını seçin.
2. Uygun **İlgili Formüller/Satırlar/Birimler** hücresine çift tıklayın.
3. **Raporlama Birimi Seçimi** iletişim kutusundaki **Raporlama ağacı** alanından rapor tanımında atanmış ağacı seçin.
4. Raporlama birimi seçin ve sonra **Tamam**'ı tıklatın. Kısıtlama satır tanımının hücresinde görünür.
5. Kısıtlanmış satırın **Mali boyutlara bağlantı** sütunundaki hücreyi çift tıklatın ve ardından finansal veriler sistemine bir bağlantı girin.

## <a name="selecting-print-control-in-a-row-definition"></a>Bir satır tanımındaki yazdırma denetimi seçme

Her sütun için yazıcı denetim kodlarını **yazdırma denetimi** hücresini kullanarak belirtebilirsiniz.

### <a name="add-print-control-codes-to-a-report-row"></a>Yazıcı Denetim kodlarını rapor satırına ekle

1. Rapor Tasarımcısı'nda, değiştirilecek satır tanımını açın.
2. **Yazdırma Kontrolü** hücresini çift tıklayın.
3. **Yazdırma denetimi** iletişim kutusunda, bir yazdırma denetim kodu seçin veya birden fazla kodu seçmek için Ctrl tuşunu basılı tutun. Ayrıca, yazıcı denetim kodlarını doğrudan **yazdırma denetimi** hücresine yazabilirsiniz. Birden çok yazıcı denetim kodlarını ayırmak için virgül kullanın.
4. Tüm koşullu yazdırma seçeneklerini seçin.
5. **Tamam** düğmesini tıklatın.

### <a name="regular-print-control-codes"></a>Normal yazdırma kontrol kodları

Bir satır tanımı için normal yazdırma denetim kodları aşağıdaki tabloda açıklanmaktadır.

| Yazdırma kontrol kodu | Yazıcı denetim kodu yorumu         | Açıklama |
|--------------------|--------------------------------------------------|-------------|
| NP                 | Yazdırılmayan satır                                 | Satırdaki tutarların raporda yazdırılmasını önler ve hesaplamalardan tutarları hariç tutar. Yazdırılmayan bir sütunu bir hesaplamaya dahil etmek için sütunu doğrudan hesaplama formülüne atayın. Örneğin, yazdırılmayan satır 240 aşağıdaki hesaplamaya dahil edilmiştir: **230 + 240 + 250**. Ancak, yazdırılmayan satır 240 aşağıdaki hesaplamaya dahil edilmemiştir: **230:250**. |
| CS                 | Para birimi simgesi; Bu satırda para birimi biçimi kullanın | Yüzde dışı tüm tutarlarda para birimi simgesini dahil edin. Yüzde değerleri, para birimi simgesi hiçbir zaman almazlar. |
| XD                 | Hesap detay raporu satırı bastır            | Hesap ayrıntılı raporlar ve hareket ayrıntılı raporlarında hesapları görüntülenmesini engelle Bu yazdırma denetimi bir satır hesap ayrıntı raporunda ve hareket ayrıntı raporunda listelenmemesi gereken birden çok hesabı içerdiğinde yararlıdır. |
| X0                 | Tüm sıfırsa satır bastır                        | Satırdaki tüm hücreler boş veya sıfır içeriyorsa satırı rapordan hariç tut. Yalnızca rapor tanımında sıfır bakiyeyi bastır seçeneği seçili olmadığında bu yazdırma denetimi anlamlıdır. |
| B0                 | Sıfır sütunları boş bırak                         | Satırda sıfır miktarları içeren sütunları boş bırakın. |
| XR                 | Toplama bastır                                  | Bir nakil işlemini baskılar. Rapor raporlama ağacı kullanıyorsa, bu satırdaki tutarların sonraki üst düğümlere toplanmaz. |
| SR                 | Yuvarlama bastır                                | Bu satırdaki tutarların yuvarlanmasını engeller. |
| XT                 | Hareket detay raporu satırı bastır        | Hareketlerin hareket ayrıntısı raporlarında görüntülenmesini engeller. Bu yazdırma denetimi bir satır hareket ayrıntı raporunda listelenmemesi gereken birden çok hesabı içerdiğinde yararlıdır. |

### <a name="conditional-print-control-codes"></a>Koşullu yazdırma kontrol kodları

Bir satır tanımı için koşullu yazdırma denetim kodları aşağıdaki tabloda açıklanmaktadır.

| Yazdırma kontrol kodu | Açıklama                                  |
|--------------------|----------------------------------------------|
| (yok)             | Koşullu yazdırma seçimini temizler.       |
| DR                 | Bu satır için yalnızca borç bakiyeleri yazdır.  |
| CR                 | Bu satır için yalnızca alacak bakiyeleri yazdır. |

## <a name="column-restriction-cell-in-a-row-definition"></a>Bir satır tanımında Sütun kısıtlama hücresi

Bir satır tanımında **Sütun kısıtlama** hücresi birden çok amaca sahiptir. Satır türüne bağlı olarak, **sütun kısıtlama** hücresini aşağıdaki işlevlerden birini belirtmek için kullanabilirsiniz:

- Hücre, satır tutarlarının belirli bir sütuna yazdırılmasını sınırlayabilir. Sekmeli bir bilanço oluşturuyorsanız, bu işlev yararlıdır.
- Hücre sıralanacak tutar sütununu belirtebilir.

## <a name="using-a-calculation-formula-in-a-row-definition"></a>Bir satır tanımındaki bir hesaplama formülü kullanmak

Satır tanımlarındaki hesaplama formülleri **+**, **-**, **\**_ ve _*/** işleçlerini ve ayrıca **IF/THEN/ELSE** deyimlerini içerebilir. Ayrıca, bir hesaplama tek tek hücreler ve mutlak (formülünde gerçek rakamlar) tutarlar içerebilir. Formül, 1.024 karaktere kadar içerebilir. Hesaplamalar **mali boyutlara bağlantı** (FD) türü hücreleri içeren satırlara uygulanamaz. Ancak, birbirini izleyen satırda hesaplamaları içerebilir, bu satırları yazdırmayı bastırabilir ve sonra hesaplama satırlarını toplayabilirsiniz.

### <a name="operators-in-a-calculation-formula"></a>Bir hesaplama formülündeki işleçler

Bir hesaplama formülü bir satır toplam formülünden daha karmaşık işleçler kullanır. Ancak, tutarları çarpmak (\*) ve bölmek (/) için **\**_ ve _*/** işleçlerini ek işleçlerle birlikte kullanabilirsiniz. Satır tanımındaki bir sütun kullanmadığınız sürece, bir hesaplama formülünde bir aralık veya toplam kullanmak için herhangi bir satır kodu önünde (@) işareti kullanmanız gerekir. Örneğin, satır 100 miktarını satır 330 miktarına eklemek için satır toplam formülü **100+330** veya hesaplama formülü **@100+@330** kullanabilirsiniz.

> [!NOTE]
> Bir hesaplama formülünde kullandığınız her satır kodundan önce (@) işareti kullanmanız gerekir. Aksi takdirde, sayı mutlak tutar olarak okunur. Örneğin, formül **@100+330** 100 satır tutarına 330 USD ekler. Bir hesaplama formülünde bir sütuna başvuru yaptığınızda bir at işareti (@) gerekli değildir.

### <a name="create-a-calculation-formula"></a>Hesaplama formülü oluşturma

1. Rapor Tasarımcısında **Satır Tanımları** öğesini tıklayın ve ardından değiştirmek için satır tanımını açın.
2. **biçim kodu** hücresini çift tıklatın ve **CAL** seçin.
3. **ilgili formüller/satır/birim** hücresinde, hesaplama formülü yazın.

### <a name="example-of-a-calculation-formula-for-specific-rows"></a>Belirli satırlar için bir hesaplama formülü örneği

Bu örnekte, hesaplama formülü **@100+@330**, satır 100'deki tutarın, satır 330'daki tutara ekleneceği anlamına gelir. Satır toplamı formülü **340+370**, satır 340'daki tutarı satır 370'e ekler. (Satır 370'deki tutar, hesaplama formülündeki tutardır.)

| Satır Kodu | Açıklama                 | Kodu biçimlendir | İlgili formüller/satırlar/birim | Yazdırma Denetimi | Satır Değiştirici | Mali Boyutlarla İlişkilendirme |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Dönemin Başlangıcındaki Nakit |             |                            | NP            | BB           | +Hesap=\[1100:1110\]       |
| 370      | Yılın Başındaki Nakit   | CAL         | @100+@330                  | NP            |              |                              |
| 400      | Dönemin Başlangıcındaki Nakit | TOT         | 340+370                    |               |              |                              |

Bir satır tanımında satırın **CAL** biçimlendirme kodu olduğunda ve **ilgili formüller/satırlar/birimler** hücresine matematiksel bir hesaplama girdiğinizde, ilişkili sütun ve satır harfini raporda da girmeniz gerekir. Örneğin; **A.120** girmek, A sütunundaki satır 120'yi temsil eder. Alternatif olarak, tüm sütunları göstermek için bir at işareti (@) kullanabilirsiniz. Örneğin, satır 120'deki tüm satırları temsil etmek için **@120** girin. Bir sütun harfine veya at işareti (@) sahip olmayan herhangi bir matematiksel hesaplamanın gerçek bir sayı olduğu kabul edilir.

> [!NOTE]
> Bir satır başvurusu için bir etiket satır kodu kullanırsanız, sütun harfi ve etiket arasında ayırıcı olarak nokta (.) kullanmanız gerekir (örneğin, **A.GROSS\_MARGIN/A.SALES**). (@) işareti kullanırsanız ayırıcı gerekli değildir (örneğin, **\@GROSS\_MARGIN/@SALES**).

### <a name="example-of-a-calculation-formula-for-a-specific-column"></a>Belirli bir satır için bir hesaplama formülü örneği

Bu örnekte, hesaplama formülü **E=C.340** C sütunu, 340 satırındaki hücredeki hesaplamanın yalnızca E sütununda gerçekleştirildiği anlamına gelir.

> [!NOTE]
> Bir hesaplama formülünde bir sütuna başvuru yaptığınızda bir at işareti (@) gerekli değildir.

| Satır Kodu | Açıklama                 | Kodu biçimlendir | İlgili formüller/satırlar/birim | Yazdırma Denetimi | Satır Değiştirici | Mali Boyutlarla İlişkilendirme |
|----------|-----------------------------|-------------|----------------------------|---------------|--------------|------------------------------|
| 340      | Dönem başlangıcında Nakit |             |                            | NP            | BB           | +Hesap=\[1100:1110\]       |
| 370      | Yıl başlangıcında Nakit   | CAL         | E=C.340                    | NP            |              |                              |
| 400      | Dönem başlangıcında Nakit | TOT         | 340+370                    |               |              |                              |

### <a name="modifying-a-number-in-selected-columns"></a>Seçili sütunlarda sayıyı değiştirme

Bir sayı veya bir sütun belirli bir satırın hesaplamada değiştirir, ancak rapor üzerindeki diğer sütunlar etkileyen istemediğiniz zaman belirtebilirsiniz **CAL** (hesaplama) içinde **biçim kodu** satır tanımının sütun.

- Tüm rapor sütunları üzerinde bir hesaplama gerçekleştirmek için (**FD**), sütun atama girmeyin.
- Bir formül için belirli sütunları kısıtlamak için sütun harfini, eşittir işareti (**=**) ve sonra formülü girin.
- Birden çok sütun belirtebilirsiniz. Bir (@) işaretini belirli sütun yerleşimi ile kullandığınızda (@) işareti satırla ilişkilendirilir.
- Tek bir satırda birden çok sütuna formül girebilirsiniz. Formülleri virgülle ayırın.

### <a name="calculation-examples"></a>Hesaplama örnekleri

| Hesaplama            | Oluşturulan eylem                                                                                                   |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| @130\*.75              | Her sütun için 130. satırdaki değer 0.75 ile çarpılır. Sonuç her sütunun geçerli satırına sonra koyulur. |
| B=@130\*.75            | Aynı hesaplama yalnızca B sütununda gerçekleştirilir.                                                                      |
| A,B,C=(@100/@130)\*.75 | A=(A.100/A.130)\*.75 B=(B.100/B.130)\*.75 C=(C.100/C.130)\*.75                                                           |

### <a name="ifthenelse-statements-in-a-row-definition"></a>Satır tanımında IF/THEN/ELSE deyimleri

**IF/THEN/ELSE** ifadeleri için geçerli olan herhangi bir maliyet hesaplama eklenebilir ve **CAL** biçimi ile kullanılabilir. **IF/THEN/ELSE** hesaplama formüllerini **ilgili formüller/satır/birim** sütunundaki hücreye girersiniz. **IF/THEN/ELSE** hesaplama formülleri şu biçimi kullanır: IF &lt;true/false ifadesi&gt; THEN &lt;formül&gt; ELSE &lt;formül&gt; **ELSE &lt;formülü&gt;** ifadesi parçası isteğe bağlıdır.

#### <a name="if-statements"></a>IF deyimleri

**EĞER** deyimini takip eden deyim doğru veya yanlış olarak değerlendirilebilecek herhangi bir ifade olabilir. **EĞER** deyimini takip eden deyim basit bir değerlendirme içerebilir veya birden çok ifade içeren karmaşık bir ifade olabilir. Burada bazı örnekler verilmiştir:

- **IF A.200&gt;0** (Basit değerlendirme)
- **IF A.200&gt;0 AND A.200&lt;10,000** (Karmaşık ifade)
- **IF A.200&gt;10000 OR ((A.340/B.1200)\*2 &lt;1200)** (birden çok ifade içeren karmaşık ifade)

**EĞER** ifadesi içindeki **nokta** terimi rapor için dönem sayısını temsil eder. Bu terim genellikle bir yıldan bugüne ortalamasını hesaplamak için kullanılır. Örneğin, 7 YTD dönemi için rapor çalıştırdığınızda, ifade **B.150/Periods** B sütununun satır 150 değerinde 7 tarafından ayrılmıştır anlamına gelir.

#### <a name="then-and-else-formulas"></a>THEN ve ELSE formülleri

**THEN** ve **ELSE** formülleri herhangi geçerli hesaplama, karmaşık formülleri için çok basit bir değer atamaları sonucu olabilir. Örneğin **IF A.200&gt;0 THEN A=B.200** deyimi "Satır 200'ün A sütununda hücre değeri, 0'dan (sıfır) fazlaysa, satır 200'ün B sütunundaki hücre değerini geçerli satırın A sütunundaki hücreye yerleştirin. Önceki **IF/THEN** deyimi geçerli satırın bir sütununa değeri yerleştirir. Bununla birlikte (@) işaretini doğru/yanlış değerlendirmeler veya tüm sütunları göstermek için formülde kullanabilirsiniz. Aşağıdaki bölümlerde açıklanan diğer bazı örnekler şunlardır:

- **IF A.200 &gt;0 THEN B.200**: A.200 hücredeki değeri pozitifse B.200 hücreden değeri geçerli satırın her sütuna yerleştirilir.
- **IF A.200 &gt;0 THEN @200**: A.200 hücredeki değeri pozitifse 200 satırındaki her sütundan değer geçerli satırın ilgili sütununa yerleştirilir.
- **IF @200 &gt;0 THEN @200**: geçerli sütunun 200 satır değeri pozitifse, 200 satır değeri geçerli satırın aynı sütununa yerleştirilir.

### <a name="restricting-a-calculation-to-a-reporting-unit-in-a-row-definition"></a>Bir hesaplamayı bir satır tanımı raporlama biriminde sınırlandırma

Böylece sonuç tutarı daha yüksek düzey bir birime yuvarlanmayacak şekilde bir hesaplamayı raporlama ağacında tek bir raporlama birimine sınırlamak için, satır tanımındaki **İlgili Formüller/Satırlar/Birimler** hücresinde **\@Unit** kodunu kullanabilirsiniz. **\@Unit** kodu, raporlama ağacının adlı B sütununda (**Birim Adı**) listelenir. **\@Unit** kodunu kullandığınızda değerler toplanmaz, ancak hesaplama raporlama ağacının her düzeyinde değerlendirilir.

> [!NOTE]
> Bu işlevi kullanmak için raporlama ağacı satır tanımı ile ilişkili olmalıdır.

Hesaplama satırı bir hesaplama satırı veya bir mali veri satırına başvurabilir. Hesaplama satır tanımının ve finansal veri türündeki kısıtlamanın **ilgili formüller/satır/birim** hücresine kaydedilir. Hesaplama **IF \@Unit** yapımı ile başlayan bir koşullu hesaplama kullanmalıdır. İşte bir örnek: IF @Unit(SALES) THEN @100 ELSE 0 Bu hesaplama yalnızca satış birimi için raporun her sütununda 100 satır tutarı içerir. Birden çok birim adı satış ise, bu birimlerin her birinde tutar görüntülenir. Ayrıca, satır 100 finansal verileri olabilir ve yazdırılmayan tanımlanabilir. Bu durumda, tutarın ağaçtaki tüm birimlerde görünmesi engellenir. Tutar raporun tek bir sütunu için, örneğin sütun H, yalnızca söz konusu rapor sütununun değerini yazdırmak için bir sütun kısıtlama kullanarak da sınırlandırabilirsiniz. Bir **IF** ifadesine **OR** birleşimleri dahil edebilirsiniz. Örneğin: **IF @Unit(SALES) OR @Unit(SALESWEST) THEN 5 ELSE @100**. Bir hesaplama türü kısıtlamada birimi aşağıdaki şekillerde belirtebilirsiniz:

- Eşleşen birim içerecek şekilde bir birim adı girin. Örneğin, **IF \@Unit(SALES)** raporlama ağacında birkaç satış birimi olsa bile hesaplamayı Satışlar adlı bir birim için etkinleştirir.
- Belirli birimler cinsinden belirli bir şirket için hesaplama kısıtlamak için şirket ve birim adını girin. Örneğin, hesaplamayı ACME şirketindeki satış birimlerine kısıtlamak için **IF @Unit (ACME:SALES)** girin.
- Belirli bir birim için hesaplama kısıtlamak için raporlama ağaç hiyerarşisinde tam kodunu girin. Örneğin **IF @Unit(SUMMARY^ACME^WEST COAST^SALES)**.

> [!NOTE]
> Tam hiyerarşi kodunu bulmak için, raporlama ağacı tanımına sağ tıklayın ve ardından **Raporlama Birimi Tanımlayıcısını (H kodu) Kopyala**'yı seçin.

#### <a name="restrict-a-calculation-to-a-reporting-unit"></a>Bir hesaplamayı bir raporlama birimiyle kısıtlama

1. Rapor Tasarımcısı'nda, **Satır Tanımları**'na tıklayın ve ardından değiştirilecek satır tanımını açın.
2. **biçim kodu** hücresini çift tıklatın ve **CAL** seçin.
3. **İlgili formüller/satırlar/birimler** hücresini tıklatın ve daha sonra **IF \@Unit** yapımıyla başlayan bir koşullu hesaplamayı girin.

### <a name="ifthenelse-statements-in-a-column-definition"></a>Sütun tanımında IF/THEN/ELSE deyimleri

Bir **IF/THEN/ELSE** deyimi herhangi hesaplama sonuçlarının diğer bir sütuna dayalı olmasını sağlar. Diğer sütunlara başvuruda bulunabilirsiniz, ancak **EĞER** ifadesinde bir rapor hücresine başvuruda bulunamazsınız. Herhangi bir hesaplamanın tüm sütuna uygulanmış olması gerekir. Örneğin, **IF B&gt;100 THEN B ELSE C\*1.25** deyimi anlamı, B sütunundaki tutar 100'den fazla ise B sütunundan değeri **CALC** sütuna yerleştir. B sütunundaki tutar 100'den fazla değilse, C sütunundaki değeri 1,25 ile çarp ve sonucu **CALC** sütununa yerleştir." Her zaman **EĞER** deyimini doğru veya yanlış olarak değerlendirilebilecek bir mantık ifadesiyle takip edin. **THEN** deyimi ve **ELSE** deyimi için kullanılan formüller herhangi bir sayıda sütun başvuruları içerebilir ve bu formüller bunları yapmak istediğiniz kadar karmaşık olabilir.

> [!NOTE]
> Diğer bir sütuna bir hesaplamanın sonuçlarını koyamazsınız. Sonuçların formülü içeren sütunda olması gerekir.

#### <a name="use-single-quotes-and-an-ampersand-for-dimension-values-in-a-row-column-or-tree"></a>Bir satır, sütun veya ağaçta boyut değerleri için tek tırnak ve ampersan (&) işaretini kullanın

Ampersan işaretini (&) içeren boyut değerlerini kullanarak raporlar tasarlayabilirsiniz.

Herhangi bir **Mali Boyuta Bağlantı** alanına, **'P&L'** gibi bir değer girebilirsiniz. Boyut değerinin her iki tarafına tek tırnak işareti (' ') ekleme, (&) ampersan karakterlerini eklemek gibi gerçek değeri kullanmakta olduğunuz anlamına gelir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
