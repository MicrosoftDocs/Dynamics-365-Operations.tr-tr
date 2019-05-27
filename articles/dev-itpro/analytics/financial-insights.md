---
title: Mali Bilgiler
description: Mali Bilgiler mali anahtar performans göstergeleri (KPI'lar), mali tablolar ve grafikleri bir araya getirmek için Microsoft Power BI kullanır.
author: kweekley
manager: AnnBe
ms.date: 08/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 2c261d2aea66b578bc976a66b6184384f0a5bf5d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554104"
---
# <a name="financial-insights"></a>Mali Bilgiler

[!include [banner](../includes/banner.md)]

**Mali Bilgiler** mali anahtar performans göstergeleri (KPI'lar), mali tablolar ve grafikleri bir araya getirmek için Microsoft Power BI kullanır. Power BI, Microsoft Dynamics 365 Finance and Operations içerisine katıştırılmıştır. **Mali Bilgiler**'in odağı analitik raporlamadır. Bir kuruluştaki kişiler görüntüleyebilir, araştırma yapabilir, anlayabilir ve harekete geçebilir. 

**Mali Bilgiler** bir kuruluşun mali durumuna ilişkin eksiksiz bir görünüm sağlamak amacıyla genel muhasebe ve yardımcı muhasebe defterlerinden alınan verileri bir araya getirir.

> [!NOTE]
> Bu belge aşağıdaki Power BI terminolojisini kullanır:
> 
> - **Rapor**: Tüm sekmelerdeki tüm görsellerin kaydedildiği bir tek .pbix dosyası.
> - **Sayfa**: Tek bir .pbix dosyasındaki bir sekme. Her sayfa bir veya daha fazla görsel içerebilir.
> - **Görsel**: Kart, KPI, grafik, şema, matris veya mali tablo gibi tek bir veri kaynağı. Görsel olarak mali tablo içeren bir sayfada, rapor edilecek verilerin boyutu nedeniyle başka hiçbir görsel olamaz.

Şu anda, **Mali Bilgiler** etkin bir tüzel kişilik veya tüm tüzel kişiliklere ilişkin verileri görüntülemek için kullanılır. Gelecekteki sürümlerde, çalışma alanı görselleri düzenlemek veya oluşturmak için Power BI kullanabileceğiniz bir alan olacaktır.

**CFO'ya genel bakış** çalışma alanı **Mali Bilgiler** ile aynı görselleri gösterir ancak mevcut raporlardaki verileri görüntülemenize ve filtrelemenize olanak tanımaya odaklanmıştır. Gelecekteki sürümlerde, **Mali Bilgiler** çalışma alanına yeni görseller de ekleyebileceksiniz. Yeni görseller, proje yöneticileri veya borç hesapları yöneticileri gibi diğer rollere odaklanan çalışma alanlarında da kullanılabilir. **CFO'ya genel bakış** çalışma alanı, rolün tüzel kişiliğe erişim izni olup olmadığına bakılmaksızın, tüm tüzel kişiliklerle ilgili verileri göstermeye devam eder.

## <a name="finance-and-operations-setup"></a>Finance and Operations kurulumu
**Genel muhasebe**

Ana hesap türü ve ana hesap kategorileri, **Mali Bilgiler** içindeki **Bilanço** mali tablosundaki ve çeşitli **Gelir tablosu** finansal tablolarındaki uygun varsayılan ana hesapları doldurmak için kullanılır.

**Ana hesaplar** sayfasında ana hesabınızı tanımlamanız ve aşağıdaki türlerden birinin ana hesaba atanması gerekir:

- Gelir
- Gider
- Kıymetler
- Borçlar
- Öz Varlık

Ana hesaplarınıza **Bilanço** veya **Kar ve Zarar** gibi başka bir ana hesap türü atamayın. Yeterince ayrıntılı olmadıklarından başka ana hesap türleri atandığında raporlama ana hesabın türünü belirleyemez. Ana hesap türü, mali raporlarda borçları ve geliri pozitif tutarlar olarak göstermek için belirlenmelidir.

Mali tablolarda görünmesi ve KPI'lar gibi çeşitli diğer görsellere dahil edilebilmesi için her ana hesaba bir ana hesap kategorisi atanmalıdır. Ana hesap kategorileri, bir görüntüleme sırası içerecek şekilde geliştirilmiştir. Görüntüleme sırası özellikle **Mali Bilgiler**'deki mali tablolarda kullanılır. Ana hesap kategorisini düzenledikten veya yeni bir ana hesap kategorisi ekledikten sonra **Görüntüleme sırası** değerini değiştirerek ana hesap kategorilerinin mali tablolarda görüntülenmesi gereken sırayı tanımlayabilirsiniz. Görüntülenme sırasını birçok ana hesap kategorisi için değiştirmeniz gerekiyorsa, Excel'de Aç özelliğini kullanarak hızlıca düzenleme yapabilir ve değişiklikleri Finance and Operations'a geri yayımlayabilirsiniz.

## <a name="entity-store"></a>Varlık deposu
**Mali Bilgiler** için veriler Varlık deposundan alınır (**Sistem yönetimi** \> **Kurulum** \> **Varlık deposu**). **CFO'ya genel bakış** veya **Mali Bilgiler** çalışma alanını açarsanız ve görsellerde aşağıdaki uyarı iletisi görüntülenirse, varlıkları güncelleştirmeniz gerekir.

![Uyarı](./media/Cantdisplay.png)

**Mali Bilgiler** ve **CFO'ya genel bakış** çalışma alanlarında verileri görmek için aşağıdaki varlıkları güncelleştirmeniz gerekir:

- CustCollectionsBIMeasurements
- FinancialReportingOtherData
- FinancialReportingReferenceData
- FinancialReportingTransactionData
- LedgerCovLiquidityMeasurement
- Satınalma küpü
- Satış küpü

Önceki sürümde, **CFO'ya genel bakış** çalışma alanındaki veriler için LedgerActivityMeasure ve VendPaymentBIMeasure varlıkları kullanılıyordu. Bununla birlikte, bunlar artık geçerli sürümde kullanılmamaktadır.

Varlıklardaki verileri düzenli olarak güncelleştirmek için tekrarlayan bir toplu iş tanımlayabilirsiniz. Her varlık güncelleştirme sırasında tümüyle yeniden oluşturulduğundan, varlık güncelleştirmelerinin sıklığını ve saatini dikkatle seçin. Mali tablolarda kullanılan birincil varlık FinancialReportingTransactionData varlığıdır. Bu nedenle, bu varlığı daha sık güncelleştirmek isteyebilirsiniz.

## <a name="security"></a>Güvenlik
Şu anda, katıştırılmış Power BI raporlarındaki veriler kullanıcının erişimi bulunan tüzel kişiliklerle sınırlandırılamamaktadır. Bu nedenle, katıştırılmış Power BI raporları güvenlik kurulumundaki görevler aracılığıyla denetlenir. Tanımlanan görevler ya tüm tüzel kişilikler veya yalnızca etkin şirkete ilişkin verilere erişim sağlar. Aşağıdaki tabloda mevcut görevler ve atandıkları roller gösterilir. Görevler, kuruluşunuzun gereksinimlerine göre, kaldırılabilir veya farklı rollere atanabilir.

| Harç                                    | Roller | Tanım |
|-----------------------------------------|-------|------------|
| CFO Genel Bakış çalışma alanını görüntüle             | Mali İşler Müdürü | Bu görev CFO'ya genel bakış çalışma alanına erişim sağlar. Varsayılan olarak, etkin şirket filtre olarak kullanılır. Ancak, kullanıcının diğer tüzel kişiliklere erişimi olup olmadığına bakılmaksızın tüm tüzel kişilikleri ekleyebilirsiniz. |
| Geçerli şirketin mali bilgilerini görüntüle | <ul><li>Muhasebeci</li><li>Muhasebe müdürü</li><li>Muhasebe gözetmeni</li><li>Denetçi</li><li>Bütçe yöneticisi</li><li>Yönetim kurulu başkanı</li><li>Mali işler müdürü</li><li>Mali denetleyici</li></ul> | Bu görev Mali Bilgiler'e erişim olanağı sağlar. Varsayılan olarak, etkin şirket filtre olarak kullanılır. Başka tüzel kişilikler ekleyemezsiniz. |
| Şirket içinde mali bilgileri görüntüle   | Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 içinde bu göreve bir rol atanmamıştır. Sonraki sürümde, bu görev Mali işler müdürü rolüne atanacaktır. | Bu görev, CFO'ya genel bakış çalışma alanı için menü öğesine erişim sağlar. Varsayılan olarak, etkin şirket filtre olarak kullanılır. Ancak, kullanıcının diğer tüzel kişiliklere erişimi olup olmadığına bakılmaksızın tüm tüzel kişilikleri ekleyebilirsiniz. |


## <a name="financial-reporting-vs-finanical-insights"></a>Mali raporlama ile Mali bilgilerin karşılaştırılması
**Mali bilgiler** mali tabloları içerse de, Finance and Operations'taki Mali raporlamanın yerine geçecek bir özellik değildir. **Mali bilgiler** içindeki varsayılan mali tabloların kapsamı sınırlıdır ve tüm mali tablo türlerini içermez. Mali raporlama yasal mali tabloları tasarlamak, oluşturmak ve üretmek için birincil araç olmaya devam eder.

Aşağıdaki karşılaştırma grafiği iki seçeneğin ayrılmasına yardımcı olur:


|                                                          | Mali Raporlama                                               | Mali Bilgiler |
|----------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| **Varsayılan raporları düzenle**                                 | Evet                                                               | Hayır |
| **Yeni raporlar oluştur**                                   | Evet                                                               | Hayır |
| **Raporları yazdır**                                        | Evet                                                               | Hayır |
| **Excel'e aktar**                                      | Evet                                                               | Sınırlı Ham verileri Excel'e aktarır, biçimlendirilmiş bir rapora değil |
| **Raporlama hiyerarşisini/Kuruluş hiyerarşisini destekle**   | Evet                                                               | Hayır |
| **Yardımcı defter verilerini raporla**                             | Evet Yalnızca satıcı, müşteri ile sınırlı                              | Evet Satıcı, müşteri, satıcı/müşteri grupları, satıcı/müşteri adresleri vb. |
| **Raporlama para birimi**                                   | Evet Muhasebe para birimi ve raporlama para birimine çevirme       | Hayır Yalnızca muhasebe para birimi |
| **Güvenlik**                                             | Evet Finance and Operations ile raporlama ağacı güvenliğine uyar | Sınırlı Tüm şirketler (Finance and Operations güvenliği ne olursa olsun) veya aktif şirket için raporları görüntüle |
| **Farklı hesap planlarını ve mali yılları destekle** | Evet                                                               | Hayır |
| **harici verileri raporla**                              | Hayır                                                                | Hayır |
| **Konsolidasyonları destekle**                               | Evet                                                               | Sınırlı Birden çok şirketle ilgili rapor verebilir ancak yalnızca muhasebe para birimini kullanır |

Orijinal **CFO'ya genel bakış** çalışma alanındaki kullanıcı arabirimine ek olarak yeni KPI'lar, grafikler ve mali tablolar artık hazır. Aşağıdaki mali tablolar bulunur:

- Geçici Mizan
- Bilanço
- Bölgeye göre gelir tablosu
- Gelir tablosu gerçek durum ile bütçe karşılaştırması
- Farklarla birlikte gelir tablosu
- 12 aylık eğilimi gösteren gelir tablosu
- Üç yıllık gider eğilimi
- Satıcıya göre giderler
- Müşteriye göre satışlar

## <a name="edit-visuals"></a>Görselleri düzenleme
**Mali Bilgiler**'in ilk sürümünde hiçbir görsel düzenlenemez. Gelecekteki sürümlerde, uygun güvenliğe sahip olan kullanıcılar yeni görseller oluşturabilecek, mevcut görselleri kopyalayabilecek ve görselleri düzenleyebilecektir. Raporları içeren dosyaları .pbix dosyaları kaynak olarak kullanılabilir olsa da varsayılan raporları düzenlemenizi önermeyiz. Mali tabloları oluşturmak için kullanılan veri modeli, varsayılan raporlar ve özel mali tablo görselinde ek değişiklikler yapılacaktır. Bu nedenle, gelecek sürümde veri modelindeki yeni özellikler ve değişikliklerden yararlanmak için, Microsoft Power BI Desktop ile varsayılan raporlarda yaptığınız değişiklikleri geri almanız gerekecektir.

## <a name="filtering"></a>Filtreleme
Kullanıcılar soldaki **Filtre** bölmesini kullanarak rapora filtre uygulayabilir. Bu bölme, Power BI Desktop aracılığıyla kullanılabilir olan bölmeyle aynıdır. Birçok filtreleme düzeyi vardır. Bunlardan bazıları sayfadaki (sekmedeki) seçimlerinize veya ayrıntılandırma özelliklerini kullanıp kullanmadığınıza bağlı olarak kullanılamayabilir:

- **Rapor düzeyindeki filtreler**: Bu filtreler tüm sayfalardaki (sekmeler) tüm görsellere uygulanır.
- **Sayfa düzeyindeki filtreler**: Bu filtreler etkin sekmedeki tüm görsellere uygulanır. Bu filtreler rapor düzeyindeki filtrelerin üzerinde uygulanır.
- **Görsel düzeyindeki filtreler**: Bu filtreler yalnızca seçilen görsele uygulanır. Bu filtreler sayfa düzeyinde filtrelerin üzerinde uygulanır.
- **Ayrıntılandırma filtresi**: Bu filtre, kaynak görselden geçerli görsele ayrıntılandırma yaptığınızda geçerli görsele uygulanan "kaynak" görselden filtreleme yapar.

![Filtrele](./media/filter.png)

Bir özel filtre değerini kaldırmak için yanındaki silgi simgesini seçin. Filtreyi X öğesini seçerek kaldırmayın. X öğesini seçerseniz filtre uyguladığınız alan filtre seçeneği olarak kaldırılır. Bir alanı filtreden yanlışlıkla kaldırırsanız, çalışma alanını kapatıp yeniden açın. Varsayılan filtre ayarları yeniden uygulanacaktır.

Varsayılan olarak, çalışma alanını ilk açtığınızda, etkin tüzel kişilik rapor düzeyinde filtre olarak kullanılır. Güvenlik durumlarına bağlı olarak kullanıcılar başka tüzel kişilikler ekleyebilir veya filtrede seçilmiş olan varsayılan tüzel kişiliği değiştirebilir.

**Mali takvim** filtresi görsel için doğru takvimin kullanılmasını sağlamak amacıyla gereklidir. Varsayılan olarak, rapor düzeyinde filtre etkin tüzel kişiliğin mali takvimine ayarlanır. Filtreyi farklı bir başlangıç veya bitiş tarihi olan bir mali takvime değiştirirseniz başlangıç bakiyeleri dahil edilmez. Bu nedenle, **Bilanço** mali tablolarınız doğru bakiyeleri göstermeyecektir. Filtrede ek bir mali takvim seçerseniz, ek bir sütun kümeniz olur. Her ek sütun kümesinde farklı bir mali takvim için tutarlar gösterilir.

**Deftere nakil katmanı** filtresi de gereklidir. Varsayılan olarak filtre Geçerli olarak ayarlanır. Toplanan tutarları göstermek için filtrede ek deftere nakil katmanları seçebilirsiniz.

Filtreler **Tarih** ve **Mali yıl** alanları için de kullanılabilir. Tipik olarak, bu filtreler sayfa düzeyinde uygulanır. Varsayılan olarak, **Tarih** filtresi değiştirebileceğiniz ilişkisel bir tarih kullanır. Ayrıca ilişkisel tarih filtresini kaldırabilir ve yerine **Mali yıl** filtresini kullanabilirsiniz.

## <a name="currency"></a>Para Birimi

Genel muhasebe verilerini rapor eden tüm görseller tutarları muhasebe para birimi cinsinde gösterir. Bu nedenle, tüzel kişiliğe filtre uyguladığınızda, yalnızca aynı muhasebe para birimine sahip tüzel kişilikleri eklemeye dikkat etmeniz gerekir. Aksi durumda, farklı para birimlerindeki verileri toplarsınız.

Yardımcı muhasebe defterindeki verileri rapor eden **Nakit akışı tahmini** ve **İlk 10** gibi tüm görseller, tutarları sistemin para birimi cinsinden gösterir. Sistem para birimi ve sistem döviz kuru türü **Sistem parametreleri** sayfasında tanımlanır.

**Banka hesabına göre bakiye** görseli, banka hesabının para birimi cinsinden tutarlar kullanır.

## <a name="dimensions"></a>Boyutlar

Varsayılan mali tablolar herhangi bir mali boyut içermez ancak yalnızca ana hesaba odaklanır. Finansal boyutlar desteği raporların düzenlenebilir hale geleceği sonraki sürümlerde kullanılabilir olacaktır. Kuruluşlar mali boyut değerlerine filtre uygulayabileceklerdir.

Bazı mali tablolar yardımcı defter hareketlerini temel alan boyutları içerir. Yeni mali tabloların amacı, mali boyutlar olarak ayarlanmayan boyutlar üzerinde filtre uygulamaya olanak tanımaktır. Örneğin, varsayılan Satıcıya göre giderler raporu ana hesabın ötesinde aşağıya doğru genişletme yapmanıza ve satıcıya göre dökümü yapılan bakiyeleri görmenize olanak tanır. Satıcı bir finansal boyut olarak ayarlanmamıştır. Bunun yerine, sistem satıcıyı bulmak için kaynak yardımcı defter hareketine geri döner.

Aşağıdaki boyutlar varsayılan raporlarda kullanılır. Bu boyutların hiçbiri mali boyut değildir.

- Satıcı
- Satıcı grubu
- Müşteri
- Müşteri grubu
- Ülke/bölge
- Eyalet/il
- Şehir

> [!IMPORTANT] 
> Birden fazla satıcı veya müşteriye ilişkin hareketleri mali günlükleri kullanarak tek bir fişte özetlerseniz, veriler yanlış olacaktır. Raporlama hangi satıcı veya müşterinin günlük girişindeki belirli bir genel muhasebe hesabıyla ilgili olduğunu belirleyemez çünkü bu bilgi herhangi bir yerde tutulmamaktadır. Bu nedenle, tek bir fişe birden fazla satıcı, müşteri, sabit kıymet veya proje girmenizi önermeyiz.

## <a name="drill-on-data"></a>Verilerin ayrıntısına inme

Power BI ile çeşitli ayrıntıya inme düzeyleri kullanılabilir. Her düzey farklı bir ada ve farklı işlevlere sahiptir. Satırlar ve sütunlarda da ayrıntıya inebilirsiniz. Bu bölüm **Mizan** mali tablosunu örnek olarak kullanarak ve satırlarda nasıl ayrıntıya inebileceğinizi göstererek çeşitli seçeneklerle ilgili bilgi verir. Aynı işlev sütunlar için de bulunur. **Ayrıntıya in** ayarını değiştirmeniz yeterlidir.

Aşağıdaki örnekte, **Mizan** tablosu satır hiyerarşisinin en üst düzeyi olan ana hesap türüne daraltılmıştır.

![Mizan](./media/trial-balance.png)

Hiyerarşinin sonraki düzeyi olan ana hesap kategorilerini görüntülemek için **Ayrıntıya in** alanını **Satırlar** olarak ayarlayıp **Genişlet** düğmesini (Alanda Ayrıntıya İn'den sonraki üçüncü düğme) seçin. Şimdi tüm ana hesap kategorilerini genişletilmiş olarak görürsünüz. Şu anda, Power BI yalnızca bir satırı veya sütunu genişletmenize olanak tanımamaktadır; diğer tüm satırları veya sütunları görürsünüz.

![Mizan](./media/trial-balance2.png)

Tüm satırlar için ana hesaplara genişletmek üzere tekrar **Genişlet** düğmesini kullanabilirsiniz. Ancak, yalnızca bir satır için ana hesapları ayrıntılı incelemek üzere öncelikle **Ayrıntıya in** düğmesini (pencerenin sağ tarafındaki aşağı doğru bakan tek ok) ve ardından ayrıntılı incelenecek olan satırı seçin. Aşağıdaki örnekte, **Ayrıntıya in** düğmesinin ardından **Satış** satırı seçildiğinde ortaya çıkan sonuç gösterilmektedir.

![Mizan](./media/trial-balance3.png)

Tek bir satırda ayrıntılara indikten sonra, tam mizana dönmek için birden fazla tıklama yapmanız gerekir. **Genele git** düğmesi (alanda **Ayrıntıla**'dan sonraki ilk düğme) aşağıdaki örnekte gösterildiği gibi yalnızca **Satış** kategorisi bağlamında genele doğru gider.

![Mizan](./media/trial-balance4.png)

Satırlar için en üst özet düzeyine dönmek için **Genele git** düğmesini kullanmaya devam edebilirsiniz.

Power BI'da ayrıca hiyerarşide sonraki aşamaya gitmenizi sağlayan bir düğme bulunur (alanda **Ayrıntıla**'dan sonraki ikinci düğme). Bu düğmenin etkisi hiyerarşi genişletmek için kullanılan **Genişlet** düğmesinden farklıdır (alanda **Ayrıntıla**'dan sonraki üçüncü düğme). Hiyerarşiyi genişlettiğinizde, hiyerarşi raporda tutulur. Örneğin, daha önce gösterildiği gibi, ana hesap türü üzerinde genişletirseniz, raporda ana hesap türünü görmeye devam edersiniz. Ancak, hiyerarşide sonraki düzeye gittiğinizde, rapor aşağıdaki örnekte gösterildiği gibi artık hiyerarşideki üst öğeyi göstermez.

![Mizan](./media/trial-balance5.png)

Özetlenmiş bakiyelerin arkasındaki hareket ayrıntılarını görmek için, Finance and Operations'ta bazı tutarlar için geriye doğru ayrıntılandırma yapmayı seçebilirsiniz.

Mali tablolardan geriye ayrıntılandırma yapmak sizi fiş hareketlerine değil Muhasebe kaynağı gezginine (ASE) götürür. ASE yalnızca genel muhasebedeki muhasebe girişlerini göstermez. Bunun yerine, yardımcı defter hareketinin ayrıntılarını gösterir. Bu nedenle, kaynak hareket hakkında daha fazla bilgi alır ve analiz için kullanabilirsiniz. Örneğin, satıcı veya müşterinin kim olduğunu, müşterinin ne aldığını veya satıcının ne sattığını ve hatta hareketteki projenin ne olduğunu görebilirsiniz.

Mali tablolardaki aşağıdaki filtreler ASE'ye gönderilir ve ASE toplanan hareketleri gösterir:

Filtreleme için gerekli alanlar:

- Tüzel kişilik
- Mali takvim
- Yıl
- Ana hesap kodu

Filtreleme için isteğe bağlı alanlar:

- Üç aylık dönem
- Ay
- Dönem

Bir satırı aşağıya doğru yeterince genişletmezseniz detaya gitme çalışmaz. Örneğin, yalnızca ana hesap kategorisine genişletmeniz durumunda, ASE'ye filtre uygulamak için ana hesap gerekli bir alan olduğundan bakiyedeki ASE'de detaya gidemezsiniz.

Bir satırı çok fazla aşağıya doğru genişletirseniz,mali tablolardaki ek filtreler ASE'ye gönderilmez. Bu nedenle, sayılarınızda farklılık görebilirsiniz. Örneğin, Bölgeye göre gelir tablosu mali tablosunun satırlarında ülke veya bölgeye kadar aşağı genişletme yaparsanız ülke veya bölge ASE'de filtre olarak eklenmez.

> [!NOTE]
> Şu anda ASE'nin filtreleme için desteklediğinden daha aşağıya inerek mali tablo satırlarında veya sütunlarında ayrıntılı inceleme yapabilirsiniz. Bu nedenle, bazı durumlarda, ASE'deki ayrıntılı hareketlerin toplamı geriye doğru ayrıntılandırma yaptığınız bakiye ile eşleşmeyecektir. Bu işlev, gelecekte geliştirilmeye devam edecektir.

## <a name="hierarchies"></a>Hiyerarşiler

Varsayılan mali tablolar verileri ayrıntılandırmak ve genişletmek için iki hiyerarşi kullanır. Hiyerarşilerden biri satırlar, diğeri ise sütunlar içindir. Her iki hiyerarşi de mali tablonun tasarımında önceden tanımlanmıştır. Çoğu mali tablo için satır hiyerarşisi **Ana hesap türü** \> **Ana hesap kategorileri** \> **Ana hesap** şeklindedir. Ancak, bazı raporlarda Ülke ve Bölge gibi ek alanlar bulunur. Hiyerarşideki ek düğümler her hareketin yardımcı muhasebe defteri verisini temel alır.

Sütunlar için hiyerarşi tüzel kişiliklere ve mali dönemlere odaklanır. Çoğu mali tablo için sütun hiyerarşisi **Tüzel kişilik** \> **Mali takvim** \> **Mali yıl** \> **Üç aylık** \> **Dönem** şeklindedir.

Şu anda, mali tablolar verileri toplamanıza olanak tanıyan kurumsal hiyerarşileri desteklememektedir.

## <a name="data-limitations"></a>Veri sınırlamaları
Mali tablo görsellerinde gösterilecek satır sayısı için sınır vardır. Şu anda sınır 30.000 olarak ayarlanmıştır. Bu sınırı aşmanız durumunda, görselde size bu durumu bildiren bir uyarı simgesi bulunacaktır.

![Veri sınırlamaları](./media/data-limit.png)

Üst sınır aşılırsa, tüm satırlar görsele yüklenmeyeceğinden mali tabloda gösterilen toplamlar yanlış olacaktır.

### <a name="empty-rows"></a>Boş satırlar
Power BI, boş satırları gizleme ve gösterme seçeneği sunmaz. Bir satırda herhangi bir veri yoksa satır görselde gösterilmez.


## <a name="additional-resources-for-power-bi"></a>Power BI için ek kaynaklar

Aşağıda yer alan kaynaklardaki bilgiler, bir üretim ortamındaki **CFO'ya genel bakış** veya **Mali Bilgiler** çalışma alanı için katıştırılmış raporlara olanak tanımak amacıyla gerekli değildir. Geliştirme kutuları ve kendi Power BI raporlarınızı Finance and Operations'a katıştırmak istemeniz durumunda yararlıdır.

- <https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/>

- <https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces>
