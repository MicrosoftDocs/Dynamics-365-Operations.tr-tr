---
title: Maddeler için emniyet stoğu karşılama
description: Bu konu, emniyet stoğu karşılamayı ve maddeler için emniyet stoğu miktarının nasıl ayarlanacağını ele alır.
author: roxanadiaconu
manager: tfehr
ms.date: 11/27/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: dbc0ca146327fada1325f4b11965c23948d3565d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987266"
---
# <a name="safety-stock-fulfillment-for-items"></a>Maddeler için emniyet stoğu karşılama

[!include [banner](../includes/banner.md)]

Emniyet stoğu, maddenin stokta kalmama riskini azaltmak amacıyla bir madde için stokta tutulan ek miktarı belirtir. Emniyet stoğu, satış siparişlerinin gelmesi ve tedarikçinin ek maddeleri müşteri tarafından talep edilen sevk tarihini karşılayacak şekilde teslim edememesi durumunda tampon stok olarak kullanılır. Emniyet stoğu bir satış siparişini karşılamak için kullanıldığında, emniyet stoğu azalacaktır. Stoğu yeniden emniyet düzeyine otomatik olarak getirmek için Master planlamayı kullanabilirsiniz.    

## <a name="set-up-safety-stock-levels-for-items"></a>Maddeler için emniyet stoğu düzeyleri ayarlama

Emniyet stoğu **Serbest bırakılan ürünler** > **Plan** > **Kapsam** altındaki **Madde karşılama** sayfasında madde karşılamanın bir bölümü olarak ayarlanır.

**Minimum** alanına madde için korumak istediğiniz emniyet stoğu düzeyini girin. Değer, stok birimleri cinsinden ifade edilir. Alanı boş bırakırsanız, varsayılan değer sıfır olur. Bu alan, **Karşılama kodu** listesinde **Periyodik**, **Gereksinim** veya **Min/Maks** seçeneğini belirlediğinizde kullanılır. Stok düzeyi sınırı kullanılabilir stoğa uygulanır; bu, fiziksel miktar belirtilen minimum düzeyin altına inmeden önce rezervasyonların ve işaretlemelerin emniyet stoğu yenilemeyi tetikleyebileceği anlamına gelmektedir.

> [!NOTE]
> **Minimum** alanını tanımlayabilmeniz için önce diğer tüm planlı karşılama boyutlarını tanımlamalısınız. Bu, master planlama sırasında geçersiz bir kaydın kullanılmasını engeller. Bu durum, örneğin bir boyut grubu, minimum ve maksimum stok miktarları henüz tanımlanmamış ek planlı karşılama boyutuyla genişletildiği zaman oluşabilir.

Minimum anahtarları periyodik talep dalgalanmalarını yönetmek için kullanabilirsiniz. Örneğin ölü sezonda bir maddenin minimum stok düzeyini azaltabilir ve ilerleyen aylarda bu düzeyi kademeli olarak artırabilirsiniz. **Master planlama** > **Kurulum** > **Karşılama** > **Minimum/maksimum anahtarları** altından bir minimum anahtarı oluşturabilirsiniz. **Madde karşılama** sayfasındaki **Minimum anahtar** alanında emniyet stoğu düzeyini döneme göre ayarlamak için minimum anahtar belirtebilirsiniz. 

## <a name="example-minimum-key"></a>Örnek: Minimum anahtarı
Bahar ve yaz aylarında artan dönemsel talebi hesaba katarak bir minimum anahtarı ayarlamak isterseniz, **Master planlama** > **Kurulum** > **Karşılama** > **Minimum / maksimum anahtarları**'na gidin ve şu adımları izleyin.

1. 12 satır oluşturun ve **Değiştir** alanında satırlara 1'den 12'ye kadar bir numara atayın.
2. **Birim** alanında **Aylar**'ı seçin.
3. **Faktör** alanında aşağıdaki tabloda açıklanan değerleri girin.

|Çizgi|Bu değeri girin.|Sonuç|
|---|---|---|
|1-3|1|Minimum stok, **Madde karşılama** sayfasında yer alan Ocak ile Mart arasındaki ayarı temel alır.|
|4-5|2|Minimum stok, Nisan ve Mayıs için 2 faktörüyle çarpılır.|
|6-8|2.5|Minimum stok, Haziran - Ağustos arasında 2,5 faktörüyle çarpılır.|
|9-12|1|Minimum stok, **Madde karşılama** sayfasındaki Eylül - Aralık arasına ilişkin ayara geri döner.|

Karşılama kodu **Min/Maks** ise, madde için korumak istediğiniz **Maksimum** stok miktarını da belirtebilirsiniz. Değer, stok birimleri cinsinden de ifade edilir. Kullanılabilir tahmini stok minimum miktarın altına düşerse, master planlama tüm açık gereksinimleri karşılamak ve kullanılabilir stoğu belirtilen maksimum miktara getirmek için bir planlı sipariş oluşturur. **Minimum** alanını ayarladığınız gibi, **Maksimum** alanını belirlemek için öncelikler tüm diğer planlı karşılama boyutlarını tanımlamanız gerekir.

## <a name="example-minmax-coverage-code"></a>Örnek: Min/Maks karşılama kodu
Minimum miktar 10'dur ve maksimum miktar 15'tir. Eldeki geçerli stok 4'tür. Bu altı adetlik bir minimum miktar gereksinimi oluşturur. Ancak maksimum miktar 15 olduğundan, master planlama 11 madde için bir planlı sipariş oluşturur.

Dönemsel talepleri izleyen maddeler için farklı maksimum düzeyleri korumanız gerekebilir. Bunu yapmak için **Master planlama** > **Kurulum** > **Karşılama** > **Minimum/maksimum anahtarları**'na giderek **Maksimum anahtarlarını** tanımlamanız gerekir. **Madde karşılama** sayfasında **Maksimum anahtarı** alanını doldurun. **Madde karşılama** sayfasındaki **Min/Maks** sekmesinde bulunan minimum anahtarları aracılığıyla tanımlanan emniyet stoğu düzeyleriyle ilgili bilgileri görüntüleyebilirsiniz. Belirli bir dönem için minimum ve maksimum değerlerin eşitlenmiş olarak kaldığından emin olmanız gerekir.

## <a name="safety-stock-fulfillment"></a>Emniyet stoğu karşılama 

**Minimum karşılama** parametresi stok düzeyinin, **Minimum** alanında belirttiğiniz miktarı karşılaması için gereken tarihi veya süreyi seçmenize olanak tanır. Bu alan, **Karşılama kodu** listesinde **Periyodik**, **Gereksinim** veya **Min/Maks** seçeneğini belirlediğinizde kullanılır.

**Minimum anahtarları** kullanılıyorsa, minimum anahtarı için ayarlanan tüm dönemler için minimum stok düzeyini karşılamak için **Minimum dönemler** onay kutusunu seçin. Onay kutusunun seçimi kaldırılırsa, minimum stok yalnızca geçerli dönem için karşılanır.

Aşağıdaki senaryo bu parametrenin nasıl çalıştığını ve değerleri arasındaki farkların neler olduğunu gösterir.

> [!NOTE]
> Bu konudaki tüm örneklerde, x ekseni stoğu, y ekseni günleri, çubuklar stok düzeyini, oklar satış siparişi satırları, satınalma sipariş satırları veya planlı siparişler gibi hareketleri temsil eder.

[![Emniyet stoğu karşılama için genel senaryo](./media/Scenario1.png)](./media/Scenario1.png) **Minimum karşılama** parametresi aşağıdaki değerlere sahip olabilir:
### <a name="todays-date"></a>Bugünün tarihi 
Belirtilen minimum miktar, master planlamanın gerçekleştirildiği tarihte karşılanır. Sistem, teslimat süresi nedeniyle gerçekçi olmayabilse bile emniyet stoğunu mümkün olan en kısa sürede karşılamayı dener. 
[![Bugünün tarihi gereksinimi](./media/TodayReq.png)](./media/TodayReq.png) Planlı sipariş P1, kullanılabilir stoğun bu tarihteki emniyet stoğu düzeyi üzerine getirilmesi için bugünün tarihi için oluşturulur. S1 ile S3 arasındaki satış siparişi satırları stok düzeyini düşürmeye devam eder. P2 ile P4 arasındaki planlı siparişler master planlama tarafından oluşturulur; böylece stok düzeyi her satış sipariş gereksiniminden sonra tekrar emniyet sınırına getirilir. 
**Gereksinim** karşılama kodu kullanıldığında, birden çok planlı sipariş oluşturulur. Sık olarak talep edilen maddeler ve malzemeler için stok yenilemeyi gruplandırmak için **Dönem** veya **Min/Maks** karşılamayı kullanmak daima iyi bir fikirdir. Aşağıda **Dönem** karşılama kodu için bir örnek gösterilmektedir.
[![Dönem. Bugünün tarihi](./media/TodayPeriod.png)](./media/TodayPeriod.png) Aşağıda **Min/Maks** karşılama kodu için bir örnek gösterilmektedir.
[![MinMaks. Bugünün tarihi](./media/TodayMinMax.png)](./media/TodayMinMax.png)
### <a name="todays-date--procurement-time"></a>Bugünün tarihi + tedarik zamanı 
Belirtilen minimum miktar, master planlamanın çalıştırıldığı tarihte, artı, satınalma veya üretim tarihinde karşılanır. Bu tarih, tüm emniyet marjlarını içerir. Madde bir ticari sözleşme içeriyorsa ve **Master planlama parametreleri** sayfasında **Ticari sözleşmeleri bul** onay kutusu işaretlenmişse, ticari sözleşmedeki teslimat sağlama süresi dikkate alınmaz. Sağlama süreleri madde karşılama ayarlarından veya maddeden alınır.
Bu karşılama modu, maddede ayarlanan karşılama grubundan bağımsız olarak, daha az gecikme ve daha az planlanmış sipariş içeren planlar oluşturur. Aşağıdaki örnekte karşılama kodunun **Gereksinim** veya **Dönem** olması durumunda planın sonucunun ne olacağı gösterilmektedir.  
[![Gereksinim. Dönem. Bugünün tarihi ve sağlama süresi](./media/TodayPLTReq.png)](./media/TodayPLTReq.png) Aşağıdaki örnekte karşılama kodunun **Min/Maks** olması durumunda planın sonucunun ne olacağı gösterilmektedir.  
[![Min Maks. Bugünün tarihi ve sağlama süresi](./media/TodayPLTMinMax.png)](./media/TodayPLTMinMax.png)
### <a name="first-issue"></a>İlk çıkış 
Belirtilen minimum miktar, aşağıda gösterildiği gibi, kullanılabilir stoğun minimum düzeyin altında indiği tarihte karşılanır. Kullanılabilir stok master planlamanın çalıştırıldığı tarihte minimum düzeyin altında olsa bile **İlk çıkış** bir sonraki gereksinim gelene kadar bunu karşılamaya çalışmayacaktır.
Aşağıda **Gereksinim** karşılama kodu için bir örnek gösterilmektedir.
[![Bir maddeyi **Gereksinim** karşılama kodu ve **İlk çıkış** karşılamayla planlama](./media/FirstIssueReq.png)](./media/FirstIssueReq.png) Aşağıda **Dönem** karşılama kodu için bir örnek gösterilmektedir.
[![Bir maddeyi **Dönem** karşılama kodu ve **İlk çıkış** karşılamayla planlama](./media/FirstIssuePeriod.png)](./media/FirstIssuePeriod.png) Aşağıda **Min/Maks** karşılama kodu için bir örnek gösterilmektedir.
[![Bir maddeyi **MinMaks** karşılama kodu ve **İlk çıkış** karşılamayla planlama](./media/FirstIssueMinMax.png)](./media/FirstIssueMinMax.png) Master planlamanın çalıştırıldığı tarihte, kullanılabilir stok zaten emniyet stoğu düzeyinin altındaysa, **Bugünün tarihi** ve **Bugünün tarihi + tedarik zamanı** hemen stok yenilemeyi tetikleyecektir. **İlk çıkış** madde için satış siparişi ve ürün reçetesi satır gereksinimi gibi başka bir çıkış işlemi olana kadar bekler ve daha sonra bu hareket tarihinde stok yenilemeyi tetikler. Master planlamanın çalıştırıldığı tarihte, kullanılabilir stok emniyet stoğu sınırının altında değilse, **Bugünün tarihi** ve **İlk çıkış** aşağıdaki örnekte de gösterildiği gibi tam olarak aynı sonucu sağlar. 

[![NotUnderLimit](./media/ReqFirstIssue.png)](./media/ReqFirstIssue.png) Master planlamanın çalıştırıldığı tarihte, kullanılabilir stok emniyet stoğu sınırının altında değilse, **Bugünün tarihi + tedarik zamanı** karşılamayı tedarik sağlama süresinin sonuna kadar erteleyeceğinden aşağıdaki sonucu verir.
![Bir maddeyi **Gereksinim** karşılama kodu ve **İlk çıkış** karşılamayla planlama](./media/ReqTodayLT.png)
### <a name="coverage-time-fence"></a>Kapsam zaman dilimi
Belirtilen minimum miktar **Karşılama zaman aralığı** alanında belirtilen süre içinde karşılanır. Master planlama emniyet stoğunu koruma girişiminde, kullanılabilir stoğun satışlar veya transferler gibi gerçek siparişler için kullanılmasına izin vermediğinde bu seçenek yararlıdır. Ancak, gelecekteki bir sürümde, bu stok yenileme moduna artık gerek kalmayacak ve bu seçenek kullanımdan kaldırılacaktır.
## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>İlk süresi dolan, ilk çıkar (FEFO) maddeleri için emniyet stoğu stok yenileme planı
Herhangi bir zamanda, en son bitiş tarihine sahip stok girişi, satış satırı veya ürün reçetesi satırı gibi gerçek bir talebin FEFO (İlk Süresi Dolan, İlk Çıkar) sırasından karşılanmasına olanak tanımak üzere emniyet stoğu için kullanılır.
Bunun nasıl çalıştığını görmek için aşağıdaki senaryoyu inceleyin.
[![FEFOScenario](./media/FEFOScenario.png)](./media/FEFOScenario.png) Planlama çalıştırıldığında, ilk satış siparişini eldeki mevcut stoktan karşılayacak ve ek satınalma siparişi kalan miktar için kullanılacaktır.
[![FEFO1](./media/FEFO1.png)](./media/FEFO1.png) Kullanılabilir stoğun yeniden emniyet sınırına getirilmesi için planlı bir sipariş oluşturulur.
[![FEFO2](./media/FEFO2.png)](./media/FEFO2.png) İkinci satış siparişi planlandığında, emniyet stoğunu karşılayan önceden oluşturulmuş planlı sipariş bu miktarı karşılamak için kullanılır. Bu nedenle, emniyet stoğu sürekli aktarılır.
[![FEFO3](./media/FEFO3.png)](./media/FEFO3.png) Son olarak, emniyet stoğunu karşılamak için başka bir planlı sipariş oluşturulur.
[![FEFO4](./media/FEFO4.png)](./media/FEFO4.png) Tüm toplu işler uygun şekilde sona erer ve bittikten sonra emniyet stoğunu yenilemek için planlı siparişler oluşturulur.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Master planlama emniyet stoğu sınırlamasını nasıl işler

Emniyet stoğu sistemde tıpkı satış satırları veya ürün reçetesi gereksinimleri gibi gereksinim türü olarak izlenir. **Gereksinim türü** sütunundaki varsayılan filtreyi kaldırırsanız, emniyet stoğu gereksinimi satırını **Net gereksinimler** sayfasında görebilirsiniz.

Sistem emniyet stoğu gereksinimi hareketinin satış satırları, ürün reçetesi satırları, transfer gereksinimleri veya talep tahmini satırları gibi gerçek bir talebin karşılanmasında gecikmeye neden olacağını belirlerse, emniyet stoğu karşılama önceliği kaldırılır. Aksi takdirde, kullanılabilir stoğun emniyet stoğu miktarından fazla olduğundan emin olunması diğer talep türleriyle aynı önceliğe sahiptir. Bu, gerçek hareketlerde gecikme olmamasını sağlar ve emniyet stoğunun aşırı yenilenmesini ve erken yenilenmesini önlemeye yardımcı olur.

Master planlamanın karşılama aşaması sırasında, emniyet stoğu yenileme önceliği artık geriye atılmaz. Eldeki stok diğer talep türlerinden önce kullanılabilir. Gecikmenin hesaplanması sırasında, emniyet stoğunun kullanılması durumunda zamanında teslim edilip edilemeyeceğini belirlemek amacıyla geciken satış satırlarının, ürün reçetesi satırı gereksinimlerinin ve diğer tüm talep türlerinin üzerine geçmek üzere yeni bir mantık eklenir. Sistem emniyet stoğunu kullanarak gecikmeleri en aza indirebileceğini belirlerse, satış satırları veya ürün reçetesi satırları başlangıçtaki karşılamayı emniyet stoğuyla doldurur ve sistem bunun yerine emniyet stoğu yenilemesini tetikler.

Plan veya madde gecikme hesaplaması için ayarlanmazsa, emniyet stoğu sınırlaması diğer talep türleriyle aynı önceliğe sahip olur. Bu, eldeki stok rezervi bulunduğu ve diğer talep türlerinden önce başka kullanılabilir stok olduğu anlamına gelir.
