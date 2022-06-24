---
title: Maddeler için emniyet stoğu karşılama
description: Bu makale, emniyet stoğu karşılamayı ve maddeler için emniyet stoğu miktarının nasıl ayarlanacağını ele alır.
author: t-benebo
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 70461ad1de94c984cb41e6b1d46af9e310a928d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887413"
---
# <a name="safety-stock-fulfillment-for-items"></a>Maddeler için emniyet stoğu karşılama

[!include [banner](../includes/banner.md)]

Emniyet stoğu, maddenin stokta kalmama riskini azaltmak amacıyla bir madde için stokta tutulan ek miktarı belirtir. Emniyet stoğu, satış siparişlerinin gelmesi ve tedarikçinin ek maddeleri müşteri tarafından talep edilen sevk tarihini karşılayacak şekilde teslim edememesi durumunda tampon stok olarak kullanılır. Emniyet stoğu bir satış siparişini karşılamak için kullanıldığında, emniyet stoğu azalacaktır. Stoğu yeniden emniyet düzeyine otomatik olarak getirmek için Master planlamayı kullanabilirsiniz.

## <a name="set-up-safety-stock-levels-for-items"></a>Maddeler için emniyet stoğu düzeyleri ayarlama

Emniyet stoğu **Serbest bırakılan ürünler \> Plan \> Kapsam** altındaki **Madde karşılama** sayfasında madde karşılamanın parçası olarak ayarlanır.

**Minimum** alanına madde için korumak istediğiniz emniyet stoğu düzeyini girin. Değer, stok birimleri cinsinden ifade edilir. Alanı boş bırakırsanız, varsayılan değer sıfır olur. Bu alan, **Karşılama kodu** listesinde **Periyodik**, **Gereksinim** veya **Min/Maks** seçeneğini belirlediğinizde kullanılır. Stok düzeyi sınırı kullanılabilir stoğa uygulanır; bu, fiziksel miktar belirtilen minimum düzeyin altına inmeden önce rezervasyonların ve işaretlemelerin emniyet stoğu yenilemeyi tetikleyebileceği anlamına gelmektedir.

> [!NOTE]
> **Minimum** alanını tanımlayabilmeniz için önce diğer tüm planlı karşılama boyutlarını tanımlamalısınız. Bu, master planlama sırasında geçersiz bir kaydın kullanılmasını engeller. Bu durum, örneğin bir boyut grubu, minimum ve maksimum stok miktarları henüz tanımlanmamış ek planlı karşılama boyutuyla genişletildiği zaman oluşabilir.

Minimum anahtarları periyodik talep dalgalanmalarını yönetmek için kullanabilirsiniz. Örneğin ölü sezonda bir maddenin minimum stok düzeyini azaltabilir ve ilerleyen aylarda bu düzeyi kademeli olarak artırabilirsiniz. **Master planlama \> Kurulum \> Karşılama \> Minimum/maksimum anahtarları** altından bir minimum anahtarı oluşturabilirsiniz. **Madde karşılama** sayfasındaki **Minimum anahtar** alanında emniyet stoğu düzeyini döneme göre ayarlamak için minimum anahtar belirtebilirsiniz.

## <a name="example-minimum-key"></a>Örnek: Minimum anahtarı

Aşağıdaki yordam, ilkbahar ve yaz aylarında artan mevsimsel talep için minimum anahtarın nasıl ayarlanacağını gösteren bir örnektir.

1. **Master planlama \> Kurulum \> Kapsam \> Minimum/maksimum anahtarları**'na gidin.
1. Minimum/maksimum anahtarı oluşturmak için **Yeni**'yi seçin.
1. **Minimum veya maksimum anahtar** alanına, anahtar için bir tanımlayıcı girin. **Ad** alanına, anahtar için bir ad girin.
1. **Yürürlük tarihini kullan** seçeneğini *Evet* olarak ayarlayın ve anahtarı geçerli yılın ilk gününden itibaren geçerli kılmak için **Yürürlük tarihi** alanını boş bırakın.

    > [!NOTE]
    > **Yürürlük tarihini kullan** ve **Yürürlük tarihi** ayarlarının birleşimi, anahtarın geçerli olduğu tarihi tanımlar.
    >
    > - **Yürürlük tarihini kullan** seçeneği *Hayır* olarak ayarlandığında, anahtar geçerli tarihten veya sistem tarihinden itibaren geçerlidir.
    > - **Yürürlük tarihini kullan** seçeneği *Evet* olarak ayarlandığında, anahtar **Geçerlilik tarihi** alanında tanımlanan tarihten itibaren geçerlidir.

1. **Dönemler** bölümünde, 12 satır oluşturun ve bunlar için aşağıdaki değerleri ayarlayın:

    - **Değiştir**: Her satıra 1 ile 12 arasında benzersiz bir sayı atayın. Bu alan, **Birim** alanı tarafından tanımlanan zaman birimindeki artımlı değişikliği gösterir.
    - **Birim**: Her satır için *Aylar*'ı seçin.
    - **Başlangıç tarihi**, **Bitiş tarihi** ve **Ay**: Bu alanlar, **Değiştirme** ve **Birim** ayarlarına göre otomatik olarak ayarlanır. Aylık dönemler, geçerli yılın ilk gününden başlar.
    - **Faktör**: Aşağıdaki tabloda açıklanan değerleri girin. Bu alan, minimum stok ile çarpmak istediğiniz faktörü tanımlar.

        | Satır (Değiştirme) | Faktör | Sonuç |
        |---|---|---|
        | 1–3 | 1 | Minimum stok, **Madde karşılama** sayfasında yer alan Ocak ile Mart arasındaki ayarı temel alır. |
        | 4–5 | 2 | Minimum stok, Nisan ve Mayıs için 2 faktörüyle çarpılır. |
        | 6–8 | 2.5 | Minimum stok, Haziran - Ağustos arasında 2,5 faktörüyle çarpılır. |
        | 9–12 | 1 | Minimum stok, **Madde karşılama** sayfasındaki Eylül - Aralık arasına ilişkin ayara geri döner. |

    Artık ayarlarınız aşağıdaki şekildeki ayarlara benzemelidir.

    ![Minimum veya maksimum anahtar dönemleri.](media/min-max-key-periods.png "Minimum veya maksimum anahtarı dönemleri")

> [!NOTE]
> Minimum/maksimum anahtarı oluşturmak için sihirbaz da kullanabilirsiniz. **Minimum veya maksimum anahtarları** sayfasındaki Eylem Bölmesi'nde **Sihirbaz**'ı seçerek **Minimum/Maksimum Anahtarları** sihirbazını açın. Sihirbaz, minimum/maksimum anahtarı oluşturma ve ayarlama işleminde size adım adım rehberlik edecektir.

Karşılama kodu *Min/Maks* ise madde için tutmak istediğiniz maksimum stok miktarını da belirtebilirsiniz. Değer, stok birimleri cinsinden de ifade edilir. Kullanılabilir tahmini stok minimum miktarın altına düşerse, master planlama tüm açık gereksinimleri karşılamak ve kullanılabilir stoğu belirtilen maksimum miktara getirmek için bir planlı sipariş oluşturur. Minimum stok miktarını ayarladığınızda olduğu gibi, **Maksimum** alanını ayarlayabilmeniz için diğer tüm planlı karşılama boyutlarını tanımlamalısınız.

## <a name="example-minmax-coverage-code"></a>Örnek: Min/Maks karşılama kodu

Minimum miktar 10'dur ve maksimum miktar 15'tir. Eldeki geçerli stok 4'tür. Bu altı adetlik bir minimum miktar gereksinimi oluşturur. Ancak maksimum miktar 15 olduğundan, master planlama 11 madde için bir planlı sipariş oluşturur.

Dönemsel talepleri izleyen maddeler için farklı maksimum düzeyleri korumanız gerekebilir. Bunu yapmak için **Master planlama \> Kurulum \> Karşılama \> Minimum/maksimum anahtarları**'na giderek **Maksimum anahtarları**'nı tanımlamanız gerekir. **Madde karşılama** sayfasında **Maksimum anahtarı** alanını doldurun. **Madde karşılama** sayfasındaki **Min/Maks** sekmesinde bulunan minimum anahtarları aracılığıyla tanımlanan emniyet stoğu düzeyleriyle ilgili bilgileri görüntüleyebilirsiniz. Belirli bir dönem için minimum ve maksimum değerlerin eşitlenmiş olarak kaldığından emin olmanız gerekir.

## <a name="safety-stock-fulfillment"></a>Emniyet stoğu karşılama

**Minimum karşılama** parametresi stok düzeyinin, **Minimum** alanında belirttiğiniz miktarı karşılaması için gereken tarihi veya süreyi seçmenize olanak tanır. Bu alan, **Karşılama kodu** listesinde **Periyodik**, **Gereksinim** veya **Min/Maks** seçeneğini belirlediğinizde kullanılır.

**Minimum anahtarları** kullanılıyorsa, minimum anahtarı için ayarlanan tüm dönemler için minimum stok düzeyini karşılamak için **Minimum dönemler** onay kutusunu seçin. Onay kutusunun seçimi kaldırılırsa, minimum stok yalnızca geçerli dönem için karşılanır.

Aşağıdaki senaryo bu parametrenin nasıl çalıştığını ve değerleri arasındaki farkların neler olduğunu gösterir.

> [!NOTE]
> Bu makaledeki tüm örneklerde, x ekseni stoğu, y ekseni günleri, çubuklar stok düzeyini, oklar satış siparişi satırları, satınalma sipariş satırları veya planlı siparişler gibi hareketleri temsil eder.

[![Emniyet stoğu karşılama için genel senaryo.](media/Scenario1.png)](media/Scenario1.png)

**Minimum karşılama** parametresi aşağıdaki değerleri alabilir:

### <a name="todays-date"></a>Bugünün tarihi

Belirtilen minimum miktar, master planlamanın gerçekleştirildiği tarihte karşılanır. Sistem, sağlama süresi nedeniyle gerçekçi olmasa da, emniyet stoku limitini en kısa sürede karşılamaya çalışır.

[![Bugünün tarihli gereksinim.](media/TodayReq.png)](media/TodayReq.png)

Planlı sipariş P1, kullanılabilir stoğun bu tarihteki emniyet stoğu düzeyi üzerine getirilmesi için bugünün tarihi için oluşturulur. S1 ile S3 arasındaki satış siparişi satırları stok düzeyini düşürmeye devam eder. P2 ile P4 arasındaki planlı siparişler master planlama tarafından oluşturulur; böylece stok düzeyi her satış sipariş gereksiniminden sonra tekrar emniyet sınırına getirilir. 

**Gereksinim** karşılama kodu kullanıldığında, birden çok planlı sipariş oluşturulur. Sık olarak talep edilen maddeler ve malzemeler için stok yenilemeyi gruplandırmak için **Dönem** veya **Min/Maks** karşılamayı kullanmak daima iyi bir fikirdir. Aşağıda **Dönem** karşılama kodu için bir örnek gösterilmektedir.

[![Dönem. Bugünün tarihi.](media/TodayPeriod.png)](media/TodayPeriod.png)

Aşağıda **Min/Maks** karşılama kodu için bir örnek gösterilmektedir.

[![Min/Maks. Bugünün tarihi.](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>Bugünün tarihi + tedarik zamanı

Belirtilen minimum miktar, master planlamanın çalıştırıldığı tarihte, artı, satınalma veya üretim tarihinde karşılanır. Bu tarih, tüm emniyet marjlarını içerir. Madde bir ticari sözleşme içeriyorsa ve **Master planlama parametreleri** sayfasında **Ticari sözleşmeleri bul** onay kutusu işaretlenmişse, ticari sözleşmedeki teslimat sağlama süresi dikkate alınmaz. Sağlama süreleri madde karşılama ayarlarından veya maddeden alınır.

Bu karşılama modu, maddede ayarlanan karşılama grubundan bağımsız olarak daha az gecikme ve daha az planlanmış sipariş içeren planlar oluşturur.

Aşağıdaki örnekte karşılama kodunun **Gereksinim** veya **Dönem** olması durumunda planın sonucunun ne olacağı gösterilmektedir.

[![Gereksinim veya Dönem. Bugünün tarihi ve sağlama süresi.](media/TodayPLTReq.png)](media/TodayPLTReq.png)

Aşağıdaki örnekte karşılama kodunun **Min/Maks** olması durumunda planın sonucunun ne olacağı gösterilmektedir.

[![Min/maks. Bugünün tarihi ve sağlama süresi.](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>İlk çıkış

Belirtilen minimum miktar, aşağıda gösterildiği gibi, kullanılabilir stoğun minimum düzeyin altında indiği tarihte karşılanır. Kullanılabilir stok master planlamanın çalıştırıldığı tarihte minimum düzeyin altında olsa bile **İlk çıkış** bir sonraki gereksinim gelene kadar bunu karşılamaya çalışmayacaktır.

Aşağıda **Gereksinim** karşılama kodu için bir örnek gösterilmektedir.

[![Bir maddeyi Gereksinim karşılama kodu ve İlk çıkış karşılamayla planlama.](media/FirstIssueReq.png)](media/FirstIssueReq.png)

Aşağıda **Dönem** karşılama kodu için bir örnek gösterilmektedir.

[![Bir maddeyi Dönem karşılama kodu ve İlk çıkış karşılamayla planlama.](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

Aşağıda **Min/Maks** karşılama kodu için bir örnek gösterilmektedir.

[![Bir maddeyi MinMaks karşılama kodu ve İlk çıkış karşılamayla planlama.](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

Master planlamanın çalıştırıldığı tarihte, kullanılabilir stok zaten emniyet stoğu düzeyinin altındaysa, **Bugünün tarihi** ve **Bugünün tarihi + tedarik zamanı** hemen stok yenilemeyi tetikleyecektir. **İlk çıkış** madde için satış siparişi ve ürün reçetesi satır gereksinimi gibi başka bir çıkış işlemi olana kadar bekler ve daha sonra bu hareket tarihinde stok yenilemeyi tetikler.

Master planlamanın çalıştırıldığı tarihte, kullanılabilir stok, emniyet stoku sınırının altında değilse **Bugünün tarihi** ve **İlk çıkış** aşağıdaki şekilde de gösterildiği gibi tam olarak aynı sonucu sağlar.

[![Limitin altında değil.](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

Master planlamanın çalıştırıldığı tarihte, kullanılabilir stok emniyet stoğu sınırının altında değilse, **Bugünün tarihi + tedarik zamanı** karşılamayı tedarik sağlama süresinin sonuna kadar erteleyeceğinden aşağıdaki sonucu verir.

![Karşılama, tedarik sağlama süresinin sonuna kadar ertelendi.](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>Kapsam zaman dilimi

Belirtilen minimum miktar **Karşılama zaman aralığı** alanında belirtilen süre içinde karşılanır. Master planlama emniyet stoğunu koruma girişiminde, kullanılabilir stoğun satışlar veya transferler gibi gerçek siparişler için kullanılmasına izin vermediğinde bu seçenek yararlıdır. Ancak, gelecekteki bir sürümde, bu stok yenileme moduna artık gerek kalmayacak ve bu seçenek kullanımdan kaldırılacaktır.

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>İlk süresi dolan, ilk çıkar (FEFO) maddeleri için emniyet stoğu stok yenileme planı

Herhangi bir zamanda, en son bitiş tarihine sahip stok girişi, satış satırı veya ürün reçetesi satırı gibi gerçek bir talebin FEFO (İlk Süresi Dolan, İlk Çıkar) sırasından karşılanmasına olanak tanımak üzere emniyet stoğu için kullanılır.

Bunun nasıl çalıştığını görmek için aşağıdaki senaryoyu inceleyin.

[![FEFO Senaryosu.](media/FEFOScenario.png)](media/FEFOScenario.png)

Planlama çalıştırıldığında, ilk satış siparişini eldeki mevcut stoktan karşılayacak ve ek satınalma siparişi kalan miktar için kullanılacaktır.

[![FEFO 1.](media/FEFO1.png)](media/FEFO1.png)

Kullanılabilir stoğun yeniden emniyet sınırına getirilmesi için planlı bir sipariş oluşturulur.

[![FEFO 2.](media/FEFO2.png)](media/FEFO2.png)

İkinci satış siparişi planlandığında, emniyet stoğunu karşılayan önceden oluşturulmuş planlı sipariş bu miktarı karşılamak için kullanılır. Bu nedenle, emniyet stoğu sürekli aktarılır.

[![FEFO 3.](media/FEFO3.png)](media/FEFO3.png)

Son olarak, emniyet stoğunu karşılamak için başka bir planlı sipariş oluşturulur.

[![FEFO 4.](media/FEFO4.png)](media/FEFO4.png)

Tüm toplu işler uygun şekilde sona erer ve bittikten sonra emniyet stokunu yenilemek için planlı siparişler oluşturulur.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Master planlama emniyet stoğu sınırlamasını nasıl işler

Emniyet stoğu sistemde tıpkı satış satırları veya ürün reçetesi gereksinimleri gibi gereksinim türü olarak izlenir. **Gereksinim türü** sütunundaki varsayılan filtreyi kaldırırsanız, emniyet stoğu gereksinimi satırını **Net gereksinimler** sayfasında görebilirsiniz.

Sistem emniyet stoğu gereksinimi hareketinin satış satırları, ürün reçetesi satırları, transfer gereksinimleri veya talep tahmini satırları gibi gerçek bir talebin karşılanmasında gecikmeye neden olacağını belirlerse, emniyet stoğu karşılama önceliği kaldırılır. Aksi takdirde, kullanılabilir stoğun emniyet stoğu miktarından fazla olduğundan emin olunması diğer talep türleriyle aynı önceliğe sahiptir. Bu, gerçek hareketlerde gecikme olmamasını sağlar ve emniyet stoğunun aşırı yenilenmesini ve erken yenilenmesini önlemeye yardımcı olur.

Master planlamanın karşılama aşaması sırasında, emniyet stoğu yenileme önceliği artık geriye atılmaz. Eldeki stok diğer talep türlerinden önce kullanılabilir. Gecikmenin hesaplanması sırasında, emniyet stoğunun kullanılması durumunda zamanında teslim edilip edilemeyeceğini belirlemek amacıyla geciken satış satırlarının, ürün reçetesi satırı gereksinimlerinin ve diğer tüm talep türlerinin üzerine geçmek üzere yeni bir mantık eklenir. Sistem emniyet stoğunu kullanarak gecikmeleri en aza indirebileceğini belirlerse, satış satırları veya ürün reçetesi satırları başlangıçtaki karşılamayı emniyet stoğuyla doldurur ve sistem bunun yerine emniyet stoğu yenilemesini tetikler.

Plan veya madde gecikme hesaplaması için ayarlanmazsa, emniyet stoğu sınırlaması diğer talep türleriyle aynı önceliğe sahip olur. Bu, eldeki stok rezervi bulunduğu ve diğer talep türlerinden önce başka kullanılabilir stok olduğu anlamına gelir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Maddeler için minimum kapsamı güncelleştirmek için emniyet stoku günlüğünü kullanma](safety-stock-journal.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
