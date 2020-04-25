---
title: İş şablonları ve konum yönergeleri ile ambar işini denetleyin
description: Bu konuda ambar içinde işin nasıl ve nerede gerçekleştirileceğini belirlemek için iş şablonları ve konum yönergelerinin nasıl kullanılacağı açıklanmaktadır.
author: perlynne
manager: tfehr
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aae57af04be8bcc6da2e5635b5ffa96d9fac147c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205748"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>İş şablonları ve konum yönergeleri ile ambar işini denetleyin

[!include [banner](../includes/banner.md)]

Bu konuda ambar içinde işin nasıl ve nerede gerçekleştirileceğini belirlemek için iş şablonları ve konum yönergelerinin nasıl kullanılacağı açıklanmaktadır.

Ambar çalışanlarının bir mobil cihazda aldığı talimatlar, çeşitli ambar işlemleri ve görevlerini tanımlamak üzere ayarladığınız Dynamics 365 Supply Chain Management iş şablonları ile belirlenir. İş şablonları işin her ambar işlemi için nasıl gerçekleştirildiğini belirler. Bir konum yönergesini iş şablonlarına bağlamakla, işin ambarlardaki belli fiziksel bölgelerde yapılmasının güvenceye alınmasına yardımcı olabilirsiniz.

## <a name="work-templates"></a>İş şablonları
**İş şablonları** sayfası ambarda gerçekleştirilmesi gereken iş operasyonlarını tanımlamanıza olanak sağlar. Genellikle, ambar iş operasyonları bir eylemler çiftinden oluşur: bir ambar çalışanı eldeki stoku bir konumdan çeker ve çekilen stoku başka bir konuma indirir. 

İş şablonları bir başlık ve ilişkili satırlardan oluşur. Her iş şablonu belirli bir *iş sipariş türü*ne yöneliktir. Birçok iş sipariş türü, satınalma ve satış siparişleri gibi kaynak belgeler ile ilişkilendirilir. Ancak, diğer iş siparişi türleri döngü sayımı gibi ayrı ambar işlemlerini ifade eder. *İş havuzu kimliği*'si işi gruplar halinde düzenlemenizi sağlar. 

İş başlığı tanımındaki ayarlar yeni bir iş parçasının ne zaman oluşturulması gerektiğini belirlemek için kullanılabilir. Örneğin, maksimum çekme satırları sayısını ve beklenen maksimum çekme süresini ayarlayabilirsiniz. Sonra, bir satış siparişi çekme işlemi işi bu değerlerden birini aşıyorsa, iş iki iş parçasına bölünür. 

İş satırları işi işlemek için gereken fiziksel görevleri ifade eder. Örneğin, bir çıkış ambarı işleminde, ambar içindeki öğeleri çekmeye yönelik bir iş satırı ve bu öğeleri bir hazırlama alanına indirmeye yönelik başka bir satır olabilir. Sonra yükleme işleminin bir parçası olarak hazırlama alanından öğeleri çekmek için ek bir satır ve öğeleri kamyona indirmek için başka bir satır olabilir. İş şablonu satırlarında bir *yönerge kodu* ayarlayabilirsiniz. Bir yönerge kodu bir konum yönergesine bağlıdır ve böylece ambar işinin ambarda doğru konumda işlendiğine dair güvence vermeye yardımcı olur. 

Belirli iş şablonu kullanıldığında kontrol etmek için bir sorgu ayarlayabilirsiniz. Örneğin, bir sınırlama ayarlayabilirsiniz, böylece yalnızca belirli bir ambardaki iş için belirli bir şablon kullanılabilir. Alternatif olarak, satış menşeine bağlı olarak, giden satış siparişi işleme işi oluşturmak için kullanılan pek çok şablonunuz olabilir. Sistem mevcut iş şablonları değerlendirildiği siparişi belirlemek için **Sıra numarası** alanını kullanır. Bu nedenle, belirli bir iş şablonu için özel bir sorgunuz varsa, buna düşük bir sıra numarası vermelisiniz. Daha sonra bu sorgu diğer, daha genel sorgulardan önce değerlendirilecektir. 

Bir iş işlemini durdurmak veya duraklatmak için, iş satırındaki **İşi durdur** ayarını kullanabilirsiniz. Bu durumda, işi gerçekleştiren çalışandan sonraki iş satırı adımını gerçekleştirmesi istenmeyecektir. Sonraki adıma geçmek için, o çalışan veya başka bir çalışan işi tekrar seçmelidir. Ayrıca iş şablonu satırlarında farklı bir *İş sınıfı kimliği* kullanarak bir iş parçası dahilindeki görevleri ayırabilirsiniz.

## <a name="location-directives"></a>Konum yönergeleri
Konum yönergeleri stok hareketi için çekme ve indirme konumlarını belirlemeye yardımcı olan kurallardır. Örneğin, bir satış siparişi hareketinde, öğelerin nereden çekileceğini ve nereye indirileceğini bir konum yönergesi belirler. Konum yönergeleri bir başlık ve ilişkili satırlardan oluşur ve bunları **Konum yönergeleri** sayfasında oluşturursunuz. 

Başlıkta, her konum yönergesi satış siparişleri, stok yenileme veya hammadde çekme gibi yönergenin kullanılacağı stok hareketinin türünü belirten bir *iş sipariş türü* ile ilişkilendirilmelidir. *İş türü* konum yönergesinin çekme veya indirme işi için veya sayım ya da stok durumu değişiklikleri gibi başka bazı ambar işleri için kullanılıp kullanılmayacağını belirtir. Ayrıca bir *tesis* ve *ambar* belirtmeniz gerekir. Konum yönergesini bir veya birden fazla iş şablonuna bağlamak için başlıkta belirttiğiniz bir *yönerge kodu* kullanılabilir. 

İş şablonlarında olduğu gibi, özel bir konum yönergesinin ne zaman kullanılacağını belirlemek için bir sorgu ayarlayabilirsiniz. Örneğin, e-ticaret bir satış siparişinin menşei olduğunda stokun ambardaki tahsis edilmiş bir alandan ne zaman alınması gerektiğini belirtebilirsiniz. Sistem mevcut konum yönergelerinin değerlendirildiği siparişi belirlemek için **Sıra numarası** alanını kullanır. 

Konum yönergesi satırları konum bulma kurallarının uygulanmasına ek kısıtlamalar getirir. Yönergenin uygulanması gereken minimum miktarı ve maksimum miktarı belirtebilirsiniz ve o yönergenin belli bir stok birimine yönelik olması gerektiğini belirtebilirsiniz. Örneğin, ölçü birimi palet ise, belli bir konuma palet cinsinden öğeler indirilebilir. Miktarın birden çok konum arasında bölünüp bölünemeyeceğini de belirtebilirsiniz. Konum yönergesi başlığı gibi, her konum yönergesi satırının da, satırların değerlendirildiği siparişi belirleyen bir sıra numarası vardır. 

Konum yönergelerinin ek bir ayrıntı düzeyi vardır: *konum yönergesi eylemleri*. Her satır için birden fazla konum yönergesi eylemi tanımlayabilirsiniz. Bir kez daha, bir sıra numarası eylemlerin karar sırasını belirlemek için kullanılır. Bu düzeyde, ambardaki en iyi konumun nasıl bulunacağını tanımlamak için bir sorgu ayarlayabilirsiniz. Ayrıca ideal bir konum bulmak için önceden tanımlanmış **Strateji** ayarlarını da kullanabilirsiniz.

## <a name="location-directives-configuration-details"></a>Konum yönergeleri yapılandırma ayrıntıları 

 ### <a name="sequence-number"></a>Numara serisi
 
Bu numara, konum yönergesinin seçilen bir sipariş türüyle işlendiğini belirtir. Menüde **Yukarı Taşı** ve **Aşağı Taşı** kullanarak değiştirilebilir.
 
 ### <a name="work-type"></a>İş türü
 
Bu, gerçekleştirilecek işin türüdür. Kullanılabilir iş türü, **Çalışma siparişi türü** alanında seçtiğiniz stok hareketi türüne bağlıdır.
-   **Yerleştirme** - **Yerleştirme**'ye eşit bir iş türü, konum yönergesinin alınan, üretilen veya stok düzenlemesinden sisteme gelen stoku yerleştirecek veya konumlandıracak en iyi konumu bulacağını belirtir. Bir yerine bir aşama veya bir bölmesi kapı son sevkiyat yerleşimine tanımlamak için de kullanılabilir.
-   **Çekme** - **Çekme**'ye eşit bir iş türü, ambarın stokun rezerve edileceği en ideal konumu bulacağı anlamına gelir (iş oluşturma). Çekme, iş tamamlanmamış olsa bile tamamlanabilir (çekme iş satırı kapatılabilir). Kullanıcı, bir çekme adımı olan fiziksel çekmeyi tamamlayabilir. Kullanıcı daha sonra bir mobil cihazdan iptal edebilir ve işi sonra tamamlayabilir. Bununla birlikte, son yerleştirme tamamlandığında iş üstbilgisinde kapatılır. 
-   **Sayım, Ayarlamalar, Özel, Stok durumu değişikliği, Plaka oluşturma, yazdırma, Durum değişikliği, İç içe geçmiş plakalara paketle** - Bunlar bir konum yönergesi kurulumunda kullanılamamaktadır. Bu bir sıralamadır, böylece iş emri türüne bağlı filtreleme yoktur. 

### <a name="directive-code"></a>Yönerge kodu

Bir iş şablonu veya stok yenileme şablonu için yönerge kodunu seçin. **Yönerge kodu** formunda, bir iş şablonu stok yenileme şablonu ve konum yönergesi arasında bağlantılar için kullanılabilecek yeni kodlar oluşturabilirsiniz. Bu, herhangi bir iş şablonu satırı ve konum yönergesi arasındaki bağlantıyı oluşturmak için de kullanılabilir (baydoor veya aşama konumu gibi).

Kod ayarlanırsa, iş oluşturulduğunda sistem konum yönergesini sekans olarak aramaz, arama yönerge koduna göre olacaktır. Bu, iş şablonundaki örneğin malzemelerin basamaklandırılması gibi belirli bir adım için hangi konum şablonunun kullanılabileceği konusunda daha spesifik olabileceğiniz anlamına gelir. 

### <a name="site"></a>Tesis

Site, konum yönergesinin geçerli olacağı bir site ve ambara ihtiyaç duyacağı için zorunlu bir alandır. 

### <a name="warehouse"></a>Ambar

Ambar, konum yönergesinin geçerli olacağı bir site ve ambara ihtiyaç duyacağı için zorunlu bir alandır.

### <a name="multiple-sku"></a>Birden çok SKU

Bu, baydoor gibi bir konumda birden fazla Stok Tutma Birimi'ne (SKU) olanak sağlar. **Birden çok SKU**'yu seçerseniz, yerleştirme konumu çalışma içerisinde belirtilmiş olur (bu da beklenmektedir), ancak yalnızca çoklu öğe girişi yapabilir (iş çekilmesi ve yerleştirilmesi gereken birden çok SKU'ya sahipse, tek bir SKU yerleştirmesi değil). **Birden çok SKU** seçmezseniz, yerleştirme konumu, yerleştirme yalnızca tek bir türde SKU'ya sahipse belirtilecektir. Her iki eylemi kullanmak için, iki satır belirtmeniz gerekir, birden çok SKU Açık ile ve birden çok SKU Kapalı ile. Bunların aynı yapıya ve kuruluma sahip olması gerekir. Yerleştirme operasyonları için aynı olan konum yönergelerini ihtiyacınız vardır, iş kimliğinde tekil veya çoklu SKU arasında ayrım yapmıyorsanız bile. Birden fazla öğeye sahip bir siparişiniz varsa çekme için de bir ayarlama yapmanız gerekir.

### <a name="sequence-number"></a>Numara serisi

Bu, konum yönergesinin satırının seçilen iş türü için işleme sırasını girin. Bu sekansı gerekirse değiştirebilirsiniz, **Yukarı taşı** ve **Aşağı taşı**'yı kullanarak.

### <a name="fromto-quantity"></a>Gelen/Giden miktar

Bu, orta kılavuz sekansının seçilecek olması durumunda bir miktar aralığı belirtmenize olanak sağlar. İlgili birimde Gelen/Giden aralığını miktar cinsinden belirtebilirsiniz.

### <a name="unit"></a>Birim

Yönergenin uygulanması gereken minimum miktarı ve maksimum miktarı belirtebilirsiniz ve o yönergenin belli bir stok birimine yönelik olması gerektiğini belirtebilirsiniz. Satırda kullanılan birim alanı yalnızca miktar değerlendirmesi için kullanılır.

Konum yönergesi satırı uygulanabilir olduğunda, konum yönergesi satırında belirtilen ilgili birimdeki miktara dayanacaktır. Bir konum yönergesi satırına ulaşıldığında, sistem talep birimini, satırda belirtilen birime dönüştürmeye çalışacaktır. Ölçü birimi dönüştürme mevcut değilse, sonraki satıra devam edecektir. 

### <a name="locate-quantity"></a>Miktarı bul

Bu seçenek yalnızca ambara miktarı yerine/bulmak için kullanılır. Yalnızca yerleştirme iş türü içindir. Geçerli değerler şunlardır:

-   **Plaka Mik** - "Gelen" ve "Giden" miktar aralıklarındaki miktarı değerlendirirken, alınan plakadaki miktarı kullan.
-   **Birimleştirilmiş Mik** - Miktarın "Gelen" ve "Giden" miktar aralıklarında olup olmadığını değerlendirirken, belirtilen işlemde birimleştirilen miktarı kullanın.
-   **Kalan Mik** - Miktarın "Gelen" ve "Giden" miktar aralıklarında olup olmadığında değerlendirirken, mevcut teslim alınan satınalma sipariş satırındaki kalan miktarı kullanın.
-   **Beklenen Mik** - Miktarın "Gelen" ve "Giden" miktar aralıklarında olup olmadığını değerlendirirken, satınalma sipariş satırındaki toplam kitarı kullanın, halihazırda alınmış olanın ne olduğundan bağımsız olarak.

### <a name="restrict-by-unit"></a>Birime göre kısıtla

Bu, konum yönergesi satırını belirli bir ölçü birimi veya birden çok ölçü biriminde yapılmasına olanak sağlar. Miktar rezerve ederken, yalnızca belirli konumlardaki paletlerden rezerve etmek isterseniz, orta kılavuz sekansı bu belirli sekansı "PL" olarak sınırlar, böylece bir paletten az bir miktardaki herhangi bir miktar sekansı seçmez. Birimleri ayarlamak için **Birimle sınırla**'yı seçin. Satırı birden fazla birime de sınırlayabilirsiniz. Bu yalnızca tür çekme türündeki konum yönergeleriyle çalışır. 

### <a name="round-up-to-unit"></a>Yukarı yuvarlama birimi

Bu alan, **Birime göre sınırla** alanıyla birlikte çalışır. **Birime göre sınırla** konum yönergesi satırı "kutu" olarak ayarlandıysa, **Birime yukarı yuvarla**, hammadde çekmede için yönerge için oluşturulan işin, bir işleme biriminin katına yukarı yuvarlanacağı anlamına gelir (**Birime göre sınırla**'da belirtildiği üzere). Bunun yalnızca hammadde çekme ve yalnızca bu tür çekme konum yönergeleri için çalıştığını unutmayın.

### <a name="locate-packing-qty"></a>Paketleme Mik bul

Bir paketleme miktarı satış siparişi, sevk emri veya üretim emri üzerinde belirtilirse, bu sistemin yalnızca konumdaki paketleme miktarı ile olan konumları seçeceğini dair kısıtlar. Bu yalnızca tür çekme türündeki konum yönergeleriyle çalışır.

### <a name="allow-split"></a>Bölmeye izin ver

Bu, bir konum yönergesinin alınan miktarı veya birden çok ambar konumu arasında rezerve edilen miktarın bölmesine izin verilip verilmeyeceğini veya işin oluşturulması için tüm miktarın tek bir konum veya rezerve edilen edilmesi gerekip gerekmediğini belirtir. 

### <a name="sequence-number"></a>Numara serisi

Bu numara, konum yönergesinin seçilen iş türü için işleme sırasıdır. Gerekirse sırada değişiklik yapabilirsiniz. Bununla birlikte, sekans numaraları kullanmakta dikkatli olun çünkü işlem her zaman sekansta çalışır. 

### <a name="name"></a>Dosya Adı

Konum yönergesi eylemi için bir ad girin. Bir ad belirtirken özel olmasına dikkat edin.

### <a name="fixed-location-usage"></a>Sabit yerleşim kullanımı 

-   **Sabit ve sabit olmayan yerleşimler** - Yerleşim yönergesi tüm konumları kabul eder.
-   **Ürün için yalnızca sabit yerleşimler** - Yerleşim yönergesi ürünler için yalnızca sabit yerleşimleri kabul edecektir.
-   **Ürün çeşidi için yalnızca sabit yerleşimler** - Yerleşim yönergesi ürün çeşitleri için yalnızca sabit yerleşimleri kabul edecektir.

### <a name="allow-negative-inventory"></a>Negatif stoğa izin ver

Konum yönergelerinde belirtilen ambar konumunda eksi stoğa izin vermek için bunu seçin. 

### <a name="batch-enabled"></a>Toplu iş etkinleştirildi 

Etkin toplu iş öğeleri için toplu iş stratejileri kullanmak için seçin. Bir satır, toplu iş olmayan bir öğede **Toplu iş etkin**'e ulaşırsa, işlem bir sonraki eylem satırına devam eder. 

### <a name="strategy"></a>Strateji

-   **Birleştir** - Bu strateji, benzer öğeleri kullanılabilir olduğunda öğeleri belirli bir konumda birleştirmek için kullanılır. Bu yalnızca yerleştirme türü konum yönergelerinde çalışır. Yerleştirme için yaygın bir kurulum, ilk eylem satırında birleştirmek ve sonra ikinci denemede birleştirme olmadan yerleştirmek olacaktır. Ürünleri birleştirmek, sonraki çekmeleri daha verimli hale getirir.
-   **Ambalaj miktarını eşleştir**- Bu strateji, gerekli miktarı tam olarak içeren bir plakası olan bir yerleşim bulacaktır. Plaka denetimli olmayan yerleşimlerle kullanılamaz. Bu strateji yalnızca bir Çekme işi türündeki yerleşim yönergesinde çalışır.
-   **FEFO toplu iş rezervasyonu** - Bu strateji stok toplu iş bitiş tarihi kullanarak konumlandırıldığında ve toplu iş rezervasyonu için tahsis edildiğinde kullanılır. Bu stratejiyi yalnızca toplu iş etkinleştirilmiş maddelerde kullanabilirsiniz. Bu yalnızca bir Çekme işi türündeki konum yönergesinde çalışacaktır. 
-   **Tam LP'ye yuvarla** - Bu strateji stok miktarını çekilecek maddelere atanan plaka (LP) miktarıyla eşleşecek şekilde yuvarlamak için kullanılır, bu strateji yalnızca stok yenileme için kullanılabilir. Bu stratejiyi yalnızca stok yenileme türündeki konum yönergesi çekme türünde kullanabilirsiniz. 
-   **Gelen iş olmadan boş konum**- Bu strateji boş konumları bulmak için kullanılır. Fiziksel stoğu yoksa ve gelen iş beklenmiyorsa konum boş olarak değerlendirilir. Bu strateji yalnızca yerleştirme türü yerleşim yönerge için kullanılır. 

### <a name="example-of-the-use-of-location-directives"></a>Konum yönergelerini kullanım örneği

Bu örnekte, konum yönergesinin, alış noktasında kaydedilen stok öğeleri için bir ambar içinde serbest kapasite bulmasının gerektiği bir satınalma siparişi işlemini ele alacağız. İlk olarak, mevcut eldeki stok ile birleştirerek ambar içinde boş kapasite bulmanız gerekir. Konsolidasyon mümkün değilse, bu durumda boş bir yer bulmanız gerekir. 

Bu senaryo için iki konum yönergesi eylemi tanımlamanız gerek. Sıradaki ilk eylemin **Konsolide Et** stratejisini ve ikinci eylemin **Gelen iş olmayan boş yer** stratejisini kullanması gerekir. Bir taşma senaryosunu idare etmek için üçüncü bir eylem tanımlamadığınız takdirde, ambarda daha fazla kapasite olmadığında iki sonucun meydana gelmesi olasıdır: iş hiçbir konum tanımlanmasa da oluşturulabilir veya iş oluşturma işlemi başarısız olabilir. Sonuç **Konum yönergesi hataları** sayfasındaki ayara göre belirlenir; burada her bir iş siparişi türü için **Konum yönergesi hatasında işi durdur** seçeneğini seçip seçmemeye karar verebilirsiniz.
