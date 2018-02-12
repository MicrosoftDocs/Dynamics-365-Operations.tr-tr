---
title: "Boyut hiyerarşisi"
description: "Bu konu, boyu hiyerarşileri hakkında bilgiler sağlar. Maliyet muhasebesi içerisinde ayarlanmış raporlama yapısını, maliyet ilkelerini ve güvenlik gruplarını tanımlamak için bir boyut hiyerarşisi kullanırsınız."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d183654ada9cdca23cf906f250988a967ffcf1f6
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="dimension-hierarchy"></a>Boyut hiyerarşisi

[!include[banner](../includes/banner.md)]

Bu konu, boyu hiyerarşileri hakkında bilgiler sağlar. Maliyet muhasebesi içerisinde ayarlanmış raporlama yapısını, maliyet ilkelerini ve güvenlik gruplarını tanımlamak için bir boyut hiyerarşisi kullanırsınız.  

## <a name="overview"></a>Özet

Boyut hiyerarşileri Maliyet muhasebesinin çeşitli yerlerinde kullanılır. Bir boyut hiyerarşisi aşağıdaki bilgileri tanımlamanıza olanak sağlar:

-  Kuruluşun gereksinimlerini karşılayan raporlama yapısı
-  Maliyet ilkeleri
-  Güvenlik kurulumu

Bir boyut hiyerarşisi örneği burada verilmiştir.

![Bir boyut hiyerarşisi örneği](./media/dimension-hierarchy.png)

Aşağıdaki boyut türleri için bir boyut hiyerarşisi oluşturulabilir:

-  Maliyet öğesi boyutları
-  Maliyet nesnesi boyutları
-  İstatistiksel boyutlar

> [!NOTE]
> - Farklı görünümler gerekiyorsa aynı boyut için çok sayıda boyut hiyerarşisi oluşturabilirsiniz.
> - Bir boyut hiyerarşisi yalnızca bir boyut ile ilişkilendirilebilir.
> - Bir boyut hiyerarşisi, yapısında sınırsız düzey barındırabilir. Tüm boyutlar **Maliyet kontrolü** çalışma alanında kullanılabilir olacaktır. Raporlama için Microsoft Excel veya Microsoft Power BI kullanırsanız, boyut hiyerarşisinin yalnızca ilk 15 düzeyi raporlanır. Bu sınırlama hem Excel hem de Power BI'ın sabir bir şemaya ihtiyaç duymasından kaynaklanır.
> - Bir boyut hiyerarşisinin yürürlük tarihi yoktur. Bu nedenle bir boyut hiyerarşisinde yapılan değişim kayda anında kaydedilir ve öncesi tarih ve sonrası tarihi kıyaslayamazsınız.

## <a name="dimension-hierarchy-type"></a>Boyut hiyerarşisi türü

Yeni bir boyut hiyerarşisi oluşturduğunuzda bir hiyerarşi türü seçmeniz gerekir. **Maliyet muhasebesi** > **Boyutlar** > **Boyut hiyerarşileri**'ne gidin. **Yeni** üzerine tıklayın ve bir boyut hiyerarşisi türü seçin. Bir **Boyut kategorizasyon hiyerarşisi** veya **Boyut sınıflandırma hiyerarşisi** seçebilirsiniz.

### <a name="dimension-categorization-hierarchy"></a>Boyut sınıflandırması hiyerarşisi

**Boyut kategorizasyon hiyerarşisi** türü raporlama amacıyla kullanılır. Yalnızca maliyet öğesi boyutlarını destekler. Bu türü seçtiğinizde aşağıdaki işleme kuralları geçerlidir:

-  Bir boyut üyesi, hiyerarşi yapısında birden fazla kere ilişkilendirilebilir.
-  Bir maliyet öğesi boyutu üyesini, yaprak düğüme bir maliyet davranışı atayarak farklı düğümlere koyabilirsiniz.

### <a name="dimension-classification-hierarchy"></a>Boyut sınıflandırması hiyerarşisi

**Boyut sınıflandırma hiyerarşisi** türü kuralları tanımlamak ve raporlama amacıyla kullanılır. Maliyet nesneleri, maliyet öğeleri ve istatistiksel boyutlar gibi tüm boyutları destekler. Bu türü seçtiğinizde, bir boyut üyesi, hiyerarşi yapısında yalnızca bir kere ilişkilendirilebilir.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Bir boyut hiyerarşisi oluşturmak ve saklamak

Bir boyut hiyerarşisi, bir düğüm ve yaprak düğüm ilişkilerine sahip bir ağaç yapısı olarak oluşturulur.

-  Bir düğüm 1:_n_ alt düğüme sahip olabilir.
-  Bir düğüme hem alt düğümler hem de yaprak düğümler atanmış olamaz.
-  Hiyerarşideki en alt düzeydeki yalnızca bir yaprak düğüm atayabilirsiniz.

### <a name="example"></a>Örnek

Burada Finans ve İnsan kaynakları yönetimi altındaki departmanları ve derleme ve ambalaj üretim altındaki departmanları aşağıdaki Organizasyon yapısını, küçük bir şirket vardır.

![Bir kuruluş yapısı örneği](./media/dimension-hierarchy-org.png)

Bir maliyet nesne boyutu, kuruluştaki tüm maliyet merkezlerini temsil eder

- Maliyet nesnesi boyutu
    - Maliyet merkezleri

Tüm maliyet merkezlerini temsil eden bir maliyet nesne boyutu burada gösterildiği gibi ayarlanabilir.

| Maliyet merkezleri | Açıklama |
|--------------|-------------|
| CC001        | İK          |
| CC002        | Finans     |
| CC003        | Vergi         |
| CC007        | AR/AP       |
| CC005        | Montaj    |
| CC006        | Paketleme   |

Bir maliyet öğe boyutu, kuruluştaki tüm maliyet öğelerini temsil eder

- Maliyet öğesi boyutu
    - Maliyet öğeleri

Tüm maliyet öğelerini temsil eden bir maliyet öğe boyutu burada gösterildiği gibi ayarlanabilir.

| Maliyet öğeleri | Açıklama |
|---------------|-------------|
| 10001         | Elektrik |
| 10010         | Temizlik    |
| 10011         | Isınma     |
| 40001         | SMM        |

Kuruluşun raporlama gereksinimlerini karşılayan bir boyut hiyerarşisi burada gösterildiği gibi ayarlanabilir.

**Boyut hiyerarşisi ayrıntıları**

| Boyut hiyerarşisi adı | Boyut    | Boyut hiyerarşisi türü adı      | Erişim listesi hiyerarşisi |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizasyon             | Maliyet merkezleri | Boyut sınıflandırması hiyerarşisi | Hayır                    |

Raporlama için boyut hiyerarşisi burada gösterildiği gibi ayarlanabilir.

|                   | Boyut üyesi aralıkları   |                         |
|-------------------|---------------------------|-------------------------|
| **Düğümler**         | **Kaynak boyut üyesi** | **Hedef boyut üyesi** |
| Organizasyon      |                           |                         |
| &nbsp;&nbsp;Yönetici         |                           |                         |
|&nbsp;&nbsp;&nbsp;&nbsp;Finans   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;İK        | CC001                     | CC001                   |
| &nbsp;&nbsp;Üretim    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Paketleme | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Montaj  | CC006                     | CC006                   |

İlke gereksinimlerini karşılayan bir boyut hiyerarşisi burada gösterildiği gibi ayarlanabilir.

**Boyut hiyerarşisi ayrıntıları**

| Boyut hiyerarşisi adı | Boyut     | Boyut hiyerarşisi türü adı      |
|--------------------------|---------------|------------------------------------|
| Maliyet davranışı            | Maliyet öğeleri | Boyut sınıflandırması hiyerarşisi |

İlke için boyut hiyerarşisi burada gösterildiği gibi ayarlanabilir.

|                   | Boyut üyesi aralıkları   |                         |
|-------------------|---------------------------|-------------------------|
| **Düğümler**         | **Kaynak boyut üyesi** | **Hedef boyut üyesi** |
| Maliyet davranışı     |                           |                         |
| &nbsp;&nbsp;Sabit maliyet    | 10001                     | 10011                   |
|&nbsp;&nbsp;Değişken maliyet | 40001                     | 40010                   |

> [!NOTE]
> **Boyut üye aralığı** altında, bir düğüm 1:_n_ boyut üye aralığı içerebilir. Henüz boyut üyeleri olarak mevcut olmayan boyut üye kodları ekleyebilirsiniz. Bu yaklaşım hiyerarşiyi geleceğe yönelik esnek yapar.  

### <a name="copy-a-hierarchy"></a>Bir hiyerarşiyi kopyala

Yeni bir boyut hiyerarşisi için bir başlangıç noktası olarak geçerli boyut hiyerarşisini kopyalayabilirsiniz. Bu yaklaşım, önceki boyut hiyerarşisini yeni boyut hiyerarşisiyle kıyaslamak istiyorsanız kullanışlı olabilir.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Hiyerarşideki düğümleri yeniden düzenleme

Bir düğümü, yapı içerisindeki mevcut seviyesi içerisinde yukarı ve aşağı taşıyabilirsiniz. Bu şekilde, **Maliyet kontrolü** çalışma alanı içindeki düğümlerin sırasını raporlama için yeniden düzenleyebilirsiniz.

Hedef düğümü seçerek bir düğümü hiyerarşi içinde yeni bir konuma taşırsınız. Bir düğümü taşımanın iki yolu vardır:

- **Aşağı taşı** – Seçili düğümü hiyerarşideki mevcut konumundan yukarı taşı ve seçili hedef düğümün **altına** ekle.
- **Sonrasında taşı** – Seçili düğümü hiyerarşideki mevcut konumundan taşı ve kendi hiyerarşi düzeyindeki seçili hedef düğümden **sonra** yerleştir.

> [!NOTE] 
> Veriyi Excel veya Power BI'a aktarırsanız düğümlerin sırası korunmaz çünkü bu araçlar varsayılan olarak bir alfasayısal sıralama düzeni kullanırlar. Sırayı el ile yeniden düzenlemelisiniz.

## <a name="define-dimension-hierarchies-for-reporting"></a>Raporlama için boyut hiyerarşileri tanımlayın

Boyut hiyerarşileri raporlama için önemlidir. Belirli bir kuruluşa uyan belirli yapıyı tanımlamanıza olanak sağlarlar. Boyut hiyerarşisinin düğüm seviyesinde gerçekleştirilen toplamlar, kuruluşun herhangi bir düzeyinde bulunan hissedarların veriyi herhangi bir düzeyde görmelerini sağlar.

Boyut hiyerarşileri aşağıdaki raporlama araçlarında kullanılabilir. Bu yaklaşım raporlama yapısında tutarlılığı garanti etmeye yardımcı olur.

- **Maliyet kontrolü** çalışma alanı (İstemci):

    - Yapılandırma tarafından denetimli.

- **Maliyet kontrolü** çalışma alanı (Mobil uygulama):

    - Yapılandırma tarafından denetimli.

- Excel

    - Dışa aktarma tanımı başına belirli boyut hiyerarşileri seçme seçeneği sağlar.

        - Bir maliyet öğesi boyut hiyerarşisi (zorunlu)
        - Bir maliyet nesnesi boyut hiyerarşisi (isteğe bağlı)
        - Bir istatistiksel boyut hiyerarşisi (isteğe bağlı)

- Power BI:

    - Tüm boyut hiyerarşileri kullanılabilir.
    
Excel veya Power BI kullanarak raporlar oluşturursanız, boyut hiyerarşilerinin yalnızca ilk 15 düzeyi dışa aktarılır. Bu sınırlama Excel ve Power BI içerisinde bir sabit şema gerektiğinden mevcuttur. Bir hiyerarşinin 15'ten fazla düzeyi varsa, ek düzeyler dışa aktarılmaz. Normalleştirilmiş tablo, hiyerarşi içerisindeki her bir boyut üyesi için bir kayıt içerir. Bu nedenle, otomatik toplama gerçekleşir. Bu davranış, hiyerarşi içerisindeki kullanılabilir 15 seviyeden herhangi birinin bakiyesinin halen doğru olmasını garanti etmeye yardımcı olur.

Aşağıdaki örnek, bir boyut hiyerarşisinin raporlama yapısında nasıl görünebileceğini gösterir.

| Maliyet nesnesi boyut hiyerarşisi – Düzey 1 | Maliyet nesnesi boyut hiyerarşisi – Düzey 2 | Maliyet nesnesi boyut hiyerarşisi – Düzey 3 | Maliyet nesnesi boyut hiyerarşisi – Düzey 4 | Maliyet nesnesi boyut hiyerarşisi – Düzey 15 |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organizasyon                              | Yönetici                                     | Finans                                   | CC002                                     |                                            |
| Organizasyon                              | Yönetici                                     | Finans                                   | CC003                                     |                                            |
| Organizasyon                              | Yönetici                                     | Finans                                   | CC007                                     |                                            |
| Organizasyon                              | Yönetici                                     | İK                                        | CC001                                     |                                            |
| Organizasyon                              | Üretim                                | Paketleme                                 | CC005                                     |                                            |
| Organizasyon                              | Üretim                                | Montaj                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Raporlama için kullanılan boyut hiyerarşilerini güncelleştir 

Zaman içerisinde önceden belirtilen raporlama araçlarında kullanılan boyut hiyerarşilerinin güncelleştirilmesi gerekecektir. Boyut hiyerarşilerini istemciyi yenileyerek güncelleştirebilirsiniz.

- **Maliyet kontrolü** çalışma alanı (İstemci)
- **Maliyet kontrolü** çalışma alanı (Mobil uygulama)

Boyut hiyerarşilerindeki güncelleştirmeler, önceden önbelleğe alınmış bir iş tarafından her 24 saatte bir çekilir. Dışa aktarılan veri güncelleştirildikten sonra, güncelleştirilen boyut hiyerarşileri halen aşağıdaki araçlarda kullanılabilir:

- Excel
- Power BI

> [!NOTE] 
> Boyut hiyerarşisi önbelleğinin güncelleştirilmesini el ile tetiklemek için boyut hiyerarşisi veya güncelleştirilmesi gereken hiyerarşiler için Excel'e yeni bir dışa aktarma oluşturabilirsiniz.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Maliyet ilkeleri için boyut hiyerarşileri tanımlayın

Maliyet muhasebesi, ayrıntılı kuralların tanımlandığı birden fazla ilkeden oluşur. Aşağıdaki ilkeler için bir veya daha fazla boyut hiyerarşisi tanımlamalısınız:

- Maliyet davranışı
- Maliyet dağılımı
- Maliyet tahsisatı
- Maliyet yuvarlaması

Boyut hiyerarşileri kurallar oluşturmayı kolaylaştırır. Her bir boyut üyesi için kurallar yaratmaktan kaçınmak amacıyla, boyut hiyerarşi düzeyleri tarafından sağlanan boyut üyelerinin toplamından yararlanabilirsiniz. Çakışan kurallara sahipseniz, genel gider hesaplaması yaptığında sistemin dikkate alacağı belirli kurallar tanımlamalısınız.

### <a name="example-define-a-cost-behavior-policy"></a>Örnek: Bir maliyet davranışı ilkesi tanımla

Yeni bir maliyet davranışı ilkesi oluşturuldu ve uygun boyut hiyerarşileri ilkeye, burada gösterildiği gibi atandı.

**Maliyet davranışı ilkesi**

| İlke adı   | Maliyet öğesi boyut hiyerarşisi | Maliyet nesnesi boyut hiyerarşisi | Muhasebe para birimi |
|---------------|----------------------------------|---------------------------------|---------------------|
| Maliyet davranışı | Maliyet davranışı                    | Organizasyon                    | ABD Doları                 |

**Kurallar**

| Maliyet öğesi boyut hiyerarşisi düğümü | Maliyet nesnesi boyut hiyerarşisi düğümü | Sabit yüzde | Sabit tutar | Geçerlilik başlangıcı | Geçerlilik bitişi |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Sabit maliyet                            | Organizasyon                         | 100,00           | 0,00         | 1/1/2017   | Hiçbir Zaman    |
| 10001                                 | Organizasyon                         | 0,00             | 150.00       | 1/1/2017   | Hiçbir Zaman    |
| 10001 (\*)                             | Finans                              |                  | 50,00        | 1/1/2017   | Hiçbir Zaman    |
| Maliyet davranışı veya Değişken maliyet (\*\*)   | Organizasyon                         | 0,00             | 0,00         | 1/1/2017   | Hiçbir Zaman    |

\* Değişken maliyet düğümü gerekli değildir. Maliyet, bir sabit maliyet olarak sınıflandırılmamışsa, bir değişken maliyet olmalıdır.

\*\* Maliyet öğe üyesi 10001 ve Finans hiyerarşisi düzeyi altında toplanan tüm maliyet üyelerinin (CC002, CC003, CC007)kombinasyonu için ayrıntılı bir kural oluşturuldu.

Önceki kurallar, boyut hiyerarşilerinin sağladığı esnekliği gösterir. Yüksek seviye kurallar tanımlayarak bakımı en aza indirmeye yardımcı olabilirsiniz. Daha sonra belirli iş amaçlarına uyacak şekilde ayrıntılı kurallar tanımlayabilirsiniz.

Kurallar içinde kullanılan boyut hiyerarşileri güncelleştirilirse, sistem otomatik olarak güncelleştirmeleri öne getirir.

Kurallar içerisindeki bir ayrıntı düzeyi daha fazla gerekmiyorsa, kural sonra erdirilebilir.

Örneğin, Finans maliyet nesne boyut hiyerarşi düğümü için belirli bir maliyet davranış kuralı daha fazla gerekli değildir. Bu durumda kuralı sonlandırmak için **Kuralı sonlandır** üzerine tıklayın.

| Maliyet öğesi boyut hiyerarşisi düğümü | Maliyet nesnesi boyut hiyerarşisi düğümü | Sabit yüzde | Sabit tutar | Geçerlilik başlangıcı | Geçerlilik bitişi  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Sabit maliyet                            | Organizasyon                         | 100,00           | 0.00         | 1/1/2017   | Hiçbir Zaman     |
| 10001                                 | Organizasyon                         | 0.00             | 150,00       | 1/1/2017   | Hiçbir Zaman     |
| 10001                                 | Finans                              |                  | 50,00        | 1/1/2017   | 20/1/2017 |
| Maliyet davranışı veya Değişken maliyet        | Organizasyon                         | 0.00             | 0.00         | 1/1/2017   | Hiçbir Zaman     |

20 Ocak 2017'den sonra çalıştırılacak herhangi bir genel gider hesaplaması bu kuralı dikkate almaz.

> [!NOTE] 
> **Geçerlilik başlangıcı** ve **Geçerlilik son tarihi** alanları saat ve tarihe dayalıdır. Kuralı sona erdirebilir ve aynı gün içerisinde yeni bir genel gider hesaplaması çalıştırabilirsiniz.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Güvelik kurulumu için boyut hiyerarşileri tanımlayın

Maliyet muhasebesi verisi, bir raporlama biriminden sorumlu tüm yöneticilere kullanılabilir yapılmalıdır. Bir raporlama birimi, maliyet muhasebesi terminolojisinde bir maliyet nesnesi veya maliyet nesnelerinin bir kümesi olarak temsil edilir.

Potansiyel olarak tüm yöneticileri, gelirler ve marjlar gibi yüksek hassasiyete sahip işletme verilerine erişebileceklerdir. Bu nedenle, güvenlik kurulumu yapmanız, yöneticilerin yalnızca kendilerini ilgilendiren verileri görmeleri için önemlidir. Veri güvenliğini denetlemeye yardımcı olmak için boyut hiyerarşilerini tanımlarsınız.

- Boyut hiyerarşilerinin kullanımı, boyut hiyerarşisi referansında seçilen bir boyut değeri yalnızca bir maliyet nesne boyutu olduğunda uygulanır.
- Erişim listesi hiyerarşisinde yalnızca bir boyut hiyerarşisi, maliyet nesne boyutu başına etkinleştirilebilir.

**Boyut hiyerarşisi ayrıntıları**

| Boyut hiyerarşisi adı | Boyut    | Boyut hiyerarşisi türü adı      | Erişim listesi hiyerarşisi |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizasyon             | Maliyet merkezleri | Boyut sınıflandırması hiyerarşisi | **Evet**               |

Yeni bir **Kullanıcılar** hızlı sekmesi hiyerarşi tasarımcısında kullanılabilir. Burada bir veya birden fazla kullanıcı kimliğini, hiyerarşi içerisindeki her bir düğümde ekleyebilirsiniz.

|                 | Kullanıcılar            | Boyut üyesi aralıkları   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| **Düğümler**       | **Kullanıcı Kimliği**      | **Kaynak boyut üyesi** | **Hedef boyut üyesi** |
| Organizasyon    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Yönetici         | Nisan            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finans   | Alicia           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;İK        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Üretim    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Paketleme | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Montaj  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Maliyet muhasebesindeki tüm girişleri görebilmeleri için maliyet muhasebecileri, hiyerarşinin en üst düzeyine atanmalıdır.

Erişim listesi hiyerarşisi ve bunun güvenlik ayarlarını etkinleştirmek için **Maliyet muhasebesi** > **Kurulum** > **Parametreler** > **Genel**'e gidin. **Maliyet nesnesi boyut üyeleri için görüntüleme erişimini etkinleştir** parametresini seçin.

Erişim listesi hiyerarşisi için ayarlar, aşağıdaki alanlarda gösterilen veriyi denetlemek için kullanılır:

- **Maliyet kontrolü** çalışma alanı (İstemci):

    - Ayrıntıya in senaryolarında kullanılan formlardaki veriler

- **Maliyet kontrolü** çalışma alanı (Mobil uygulama):

    - Kartlardaki bakiyeler

- Power BI:

    - Veri, Power BI görselleştirmeleri içinde gösterilir
    - Microsoft Dynamics 365 for Finance and Operations, Enterprise edition istemcisinde gömülü veri Power BI görselleştirmeleri

> [!NOTE] 
> - Erişim listesi hiyerarşisi Power BI içerisindeki veriyi etkileyebilmeden önce, Power BI içindeki erişim listesi hiyerarşisi ve satır düzeyi güvenliği eşleştirilmelidir. Daha fazla bilgi için bkz [Maliyet muhasebesi İçerik Paketi için güvenlik kurma](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Erişim listesi hiyerarşisi, verinin Excel'e aktarılmasını güvenli hale getirmeye yardımcı olmaz. Bu nedenle, bu raporlama aracı yalnızca veriyi görüntülemeye tam erişime sahip maliyet muhasebecileri ve yöneticiler tarafından kullanılmalıdır.

