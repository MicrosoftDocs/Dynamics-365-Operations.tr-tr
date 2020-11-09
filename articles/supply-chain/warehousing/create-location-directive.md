---
title: Yerleşim yönergeleri oluşturma
description: Bu konuda, yerleşim yönergelerinin nasıl oluşturulacağı açıklanmaktadır. Yerleşim yönergeleri stok hareketi için çekme ve yerine koyma yerleşimlerini belirlemeye yardımcı olan kullanıcı tanımlı kurallardır.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 4f634b7f526fd198b394af6d3870c43ee560813e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016782"
---
# <a name="create-location-directives"></a>Yerleşim yönergeleri oluşturma

[!include [banner](../includes/banner.md)]

Bu konuda, yerleşim yönergelerinin nasıl oluşturulacağı açıklanmaktadır. Yerleşim yönergeleri stok hareketi için çekme ve yerine koyma yerleşimlerini belirlemeye yardımcı olan kullanıcı tanımlı kurallardır. Örneğin, bir satış siparişi hareketinde, maddelerin nereden çekileceği ve nereye konulacağını bir konum yönergesi belirler.

> [!NOTE]
> Bu konu, **Ambar yönetimi** modülündeki özellikler için geçerlidir. [Stok yönetimi](../inventory/inventory-home-page.md) modülündeki özellikler için geçerli değildir.

Yerleşim yönergelerini şu görevleri gerçekleştirmek için kullanabilirsiniz:

- Gelen maddeleri yerine koyma.
- Giden hareketler için maddeleri çekme ve hazırlama.
- Üretim için hammadde çekme ve yerine koyma.
- Yerleşimlerde stok yenileme.

## <a name="prerequisites"></a>Önkoşullar

Bir yerleşim yönergesi oluşturmadan önce, önkoşulların karşılandığından emin olmak için aşağıdaki adımları izlemeniz gerekir.

1. **Ambar yönetimi \> Kurulum \> Ambar  \> Ambarlar** 'a gidin.
1. Ambar oluşturun.
1. **Ambar** hızlı sekmesinde **Ambar yönetimi işlemlerini kullan** seçeneğini *Evet* olarak ayarlayın.
1. Yerleşimler, yerleşim türleri, yerleşim profilleri ve yerleşim biçimleri oluşturun. Daha fazla bilgi için bkz. [WMS özellikli ambarda yerleşimler yapılandırma](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Tesisler, bölgeler ve bölge grupları oluşturun. Daha fazla bilgi için bkz. [Ambar kurulumu](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) ve [WMS özellikli ambarda yerleşimler yapılandırma](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Ayar

### <a name="create-location-directives"></a>Yerleşim yönergeleri oluşturma

Yerleşim yönergesi oluşturmak için aşağıdaki adımları izleyin.

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Liste bölmesinde, **İş emri türü** alanını, yerleşim emri oluşturduğunuz stok hareketinin türüne göre ayarlayın.
1. Eylem bölmesinde **Yeni** 'yi seçerek yeni bir yerleşim yönergesi oluşturun.
1. Yeni yerleşim yönergesi için, alanları aşağıdaki tabloda açıklandığı gibi ayarlayın.

    | Alan | Tanım |
    |---|---|
    | Numara serisi | Yerleşim yönergesinin sıra konumunu gösteren bir tamsayı girin. Sıra konumları, her konum yönergesinin seçilen iş emri türü için ne zaman işleneceğini belirler. |
    | Dosya Adı | Yerleşim yönergesi için bir ad girin. | 
    | İş türü | Yapılması gereken iş türünü seçin. Değerlerin listesi **Çalışma siparişi türü** alanında seçtiğiniz stok hareketi türüne bağlıdır. Aşağıdaki değerler kullanılabilir:<ul><li>**Yerine koyma** : Yerleşim yönergesi teslim alma, üretim veya stok ayarlamaları aracılığıyla sisteme gelen stoğu yerleştirmek veya yerini belirlemek için en iyi konumu bulmaya çalışır. Yerleşim yönergesi ayrıca giden akıştaki yerine koyma konumunu veya son bölme kapısı sevkiyat yerini tanımlamak için de kullanılır.</li><li>**Çekme** : Yerleşim yönergesi, stoğu fiziksel olarak rezerve etmek için (iş oluştur) en iyi konumları bulmaya çalışır. Çekme, iş tamamlanmamış olsa bile tamamlanabilir (çekme iş satırı kapatılabilir). Kullanıcı fiziksel malzeme çekmeyi tamamlayabilir. Sistemde, bu eylem bir çekme adımıdır. Kullanıcı daha sonra mobil cihazdan iptal edebilir ve işi (örneğin yerine koyma) sonra tamamlayabilir. Bununla birlikte, son yerleştirme tamamlandığında iş bağlığı önce kapatılır.</li><li>**Sayım** , **Ayarlamalar** , **Özel** , **Stok durumu değişikliği** , **Plaka oluşturma** , **yazdırma** , **Durum değişikliği** , ve **İç içe geçmiş plakalara paketle** - Bu değerler yerleşim yönergesi kurulumunda kullanılamaz.</li></ul> |
    | Tesis | İşin tamamlanması gereken tesisi seçin. |
    | Ambar | İşin tamamlanması gereken ambar yerleşimini seçin. |
    | Yönerge kodu | Bu kodun atandığı iş şablonu yerine koyma satırlarıyla ilgili yerleşim yönergelerinin seçiminde yön göstermek için bir yönerge kodu seçin. **Yönerge kodu** sayfasında, bir iş şablonunu bir yerleşim yönergesine bağlamak için kullanılabilecek yeni kodlar oluşturabilirsiniz. Ayrıca, herhangi bir iş şablonu satırı ve konum yönergesi (bölme kapısı veya hazırlama konumu gibi) arasındaki bağlantıyı oluşturmak için de bu sayfayı kullanabilirsiniz. İş şablonuyla yönerge kodu yapılandırma hakkında daha fazla bilgi için bkz. [İş şablonları ve konum yönergelerini kullanarak ambar işini denetleme](control-warehouse-location-directives.md)<p>Yönerge kodu ayarlanırsa, iş oluşturulması gerektiğinde, sistem yerleşim yönergelerini sekans yerine yönerge koduna göre arar. Bu şekilde, iş şablonundaki (örneğin malzemelerin hazırlanması gibi) belirli bir adım için hangi yerleşim şablonunun kullanılabileceği konusunda daha spesifik olabilirsiniz.</p> |
    | Elden çıkarma kodu | Alınan maddelerin bir yerleşime koyulması işini yönlendirmek için bir değerlendirme kodu seçin. (Daha fazla bilgi için bkz. [Değerlendirmeleri kodları ayarlama](tasks/set-up-dispositions-codes.md).) Bu alan yalnızca **İş emri türü** alanı *Satınalma siparişleri* , *İade siparişleri* veya *Mamül mal yerine koyma* olarak ayarlandığında kullanılabilir. |
    | Birden çok SKU | Bir yerleşimde birden fazla stok tutma birimi (SKU) kullanmak için bu seçeneği *Evet* olarak ayarlayın. Örneğin, bu seçenek bölme kapısı için *Evet* olarak ayarlanmalıdır.<p>**Çoklu SKU** seçeneği *Evet* olarak ayarlanmışsa, koyma yerleşimi iş içinde (beklendiği gibi) belirtilir. Ancak, koyma yerleşimi yalnızca iş çekilip konulması gereken farklı SU'lar içeriyorsa çoklu madde yerine koyma işlemi gerçekleştirebilir (iş yalnıza yerine konulması gereken tek bir SKU içeriyorsa işlemi gerçekleştiremez).</p><p>**Çoklu SKU** seçeneği *Hayır* olarak ayarlanırsa, yerine koyma yerleşimi yalnızca yerine koyma işleminde tek bir türde SKU'ya sahipse belirtilecektir.</p><p>Her iki yaklaşımı da kullanmak için aynı yapıya ve kuruluma sahip iki satır belirtmeniz gerekir, ancak **Çoklu SKU** seçeneğini satırlardan biri için *Evet* diğeri için *Hayır* olarak ayarlamalısınız. Başka deyişle, iş kimliğinde tek veya çoklu SKU arasında ayrım yapmanız gerekmese bile yerleştirme operasyonları için aynı olan iki yerleşim yönergesi gereklidir. Birden fazla öğeye sahip bir siparişiniz varsa çekme için de bir yerleşim yönergesi ayarlamanız gerekir.</p><p>**Not:** **Yerine koyma** iş türünde bir yerleşim yönergesi için *Çoklu SKU* seçeneğini *Evet* olarak ayarlarsanız, sistem satırlarda oluşturulan diğer kısıtlamalara bakmaksızın her zaman ilk yerleşim yönergesi satırını seçer.</p> |

1. İsteğe bağlı: Eylem Bölmesinde, yerleşimleri seçmek için **Sorguyu düzenle** 'yi seçin veya belirli bir konum yönergesi seçtiğinizde geçerli olacak herhangi bir sınırlama belirtin.
1. **Satırlar** hızlı sekmesinde, birimleri belirtmek ve bir ambardaki miktarı bulmak veya rezerve etmek için bir veya daha fazla satır oluşturun.
1. Her yeni satırda, alanları aşağıdaki tabloda açıklandığı gibi ayarlayın.

    | Alan | Tanım |
    |---|---|
    | Numara serisi | Yerleşim yönergesinin sıra konumunu gösteren bir tamsayı girin. Sıra konumları, her konum yönergesinin seçilen iş türü için ne zaman işleneceğini belirler. |
    | Başlangıç miktarı | Orta kılavuz sekansının seçilmesi durumunda başlangıç miktar aralığını belirtin. **Birim** alanında, miktar için ölçü birimini belirtin. |
    | Son miktar | Orta kılavuz sekansının seçilmesi durumunda bitiş miktar aralığını belirtin. **Birim** alanında, miktar için ölçü birimini belirtin. |
    | Birim | Maddelerin ölçü birimini seçin.<p>yönergenin uygulanacağı bir minimum miktar ve maksimum miktar belirtebilirsiniz. Ayrıca, yönergenin belirli bir stok birimi için kullanılmasını da belirtebilirsiniz. **Birim** alanı yalnızca miktar değerlendirmesi için kullanılır.</p><p>Bir yerleşim yönergesi satırının uygulanıp uygulanmayacağını belirlemek için, sistem miktarları satırda belirtilen **Birim** değerini kullanarak değerlendirir. Bir konum yönergesi satırına ulaşıldığında, sistem talep birimini, satırda belirtilen birime dönüştürmeye çalışacaktır. Birim dönüştürme yoksa, sistem sonraki satıra geçer.</p> |
    | Miktarı bul | Bu alan yalnızca ambardaki miktarı koymaya veya bulmaya çalıştığınızda geçerlidir. Başka bir deyişle, yalnızca *Koyma* işi için geçerlidir. Miktarın  **Başlangıç miktarı**  ve  **Bitiş miktarı**  alanlarında ayarlanan aralıkta olup olmadığını denetlemek için kullanılan yöntemi seçin. Yerleşim yönergesi bir gelen hareket için ise, aşağıdaki seçeneklerden birini belirleyin:<ul><li>**Plaka miktarı** - Miktarın hedef miktar aralığında olup olmadığını değerlendirmek için alınan plakadaki miktarı kullanın.</li><li>**Birimlere ayrılmış miktar** - Miktarın hedef miktar aralığında olup olmadığını değerlendirmek için hareket sırasında birimlere ayrılacak miktarı kullanın. Örneğin, bir ambarda, 1.000 miktarını alabiliyor ve her biri 100 miktarına sahip 10 plakaya bölebiliyorsanız, 100 olan plaka miktarı yerine 1.000 madde miktarını kullanabilirsiniz.</li><li>**Kalan miktar** - Nir miktarın hedef miktar aralığında olup olmadığını değerlendirmek için, mevcut teslim alınan satınalma siparişi satırındaki teslim alınacak kalan miktarı kullanın.</li><li>**Beklenen miktar** - Bir miktarın hedef miktra aralığında olup olmadığını değerlendirmek için, teslim alınan miktarı dikkate almaksızın satınalma sipariş satırındaki toplam miktarı kullanın.</li></ul> |

1. İsteğe bağlı: **Satırlar** hızlı sekmesinde, aşağıdaki ek alanları ayarlayabilirsiniz.

    | Alan | Tanım |
    |---|---|
    | Birime göre kısıtla | Yerleşim yönergesi satırları için geçerli seçim ölçütü olarak kabul edilen ölçü birimlerini sınırlandırmak için bu onay kutusunu seçin. Ölçü birimleri belirtildiğinde, yalnızca birimin birim sırası grubu için tanımlanan en az bir birimle eşleştiği maddeler satır seçimi için geçerli kabul edilir.<p>Örneğin, birim paletlerle sınırlandırılmıştır ve madde *paletler* birimini içeren bir birim sırası grubuyla ilişkilendirilir. Bu durumda, maddeler yerleşim yönergesi için geçerli bir seçenek olarak kabul edilir.</p><p>Ancak, **Birime göre kısıtla** onay kutusu, iş satırları üzerinde uygulanan birim veya birimleri denetlemez. Birim kısıtlaması yalnızca birim sırası grubu aracılığıyla kullanılabilir duruma getirilen birimlere uygulanır.</p><p>Örneğin, bir madde hem *paletler* hem de *parça* birimini içeren bir birim sırası grubuyla ilişkilendirilir. 1 palet = 100 adet olacak şekilde bir ölçü birimi tanımlanır ve yerleşim yönergesi yalnızca paletler için **Birime göre kısıtla** işlevini kullanır. Ayrıca, iş başlığı oluşturmayı 50 adete sınırlayan bir iş şablonu tanımlanmıştır. Bu durumda, 50 adetlik iş satırları oluşturulur.</p><p>Kısıtlama için ölçü birimini belirtmek üzere aşağıdaki adımları izleyin</p><ol><li>**Satırlar** hızlı sekmesinde, **Birime göre kısıtla** 'yı seçin. Bu düğme yalnızca satırdaki **Birime göre kısıtla** onay kutusu seçildikten sonra kullanılabilir duruma gelir; ardından **Kaydet** 'i seçin.</li><li>**Birim** alanında, çekme ve yerine koyma işlemleri için sınırlamada kullanılacak ölçü birimini seçin.</li></ol> |
    | Yukarı yuvarlama birimi | Hammadde çekmenin, **Birime göre kısıtla** alanında belirtilen işleme biriminin katlarına yuvarlanıp yuvarlanmayacağını belirtmek için bu seçeneği belirleyin. Bu alan hammadde çekme ve *Çekme* türünde yerleşim yönergeleri için geçerlidir. |
    | Paketleme miktarını bul | Paketleme birim miktarı **Satış siparişi** sayfasında belirtildiyse bu onay kutusunu seçin. Bu onay kutusunu seçerseniz, yalnızca bu paketleme birim miktarına sahip olan yerleşimler seçilir. |
    | Bölmeye izin ver | Miktarı birden çok konum arasında bölmek için bu onay kutusunu seçin. |
    | Anlık stok yenileme şablonu | Maddeler tahsis edilmemişse stok yenilemeyi hemen başlatmak için stok yenileme şablonuna bir bağlantı oluşturun. Bu alan boş bırakılırsa, yerleşim yönergesindeki tüm satırlar işlenene kadar madde stok yenilemesi başlatılmaz.<p>Bu alan yalnızca, *Satış siparişleri* ve *Hammadde çekme* gibi stok yenileme işlemlerine izni verilen seçili iş emri türlerinde kullanılabilir.</p> |

1. **Yerleşim yönergesi eylemleri** hızlı sekmesinde, yerleşim veya yerleşim aralığını seçmek için **Yeni** 'yi seçin.
1. **Sıra numarası** alanı, seçilen iş türü için yerleşim yönergesinin hangi sırada işlendiğini gösterir. Sırada değişiklik yapabilirsiniz. Ancak, yerleşim yönergesi eylemleri her zaman bu sırada olacağından, yerleşim yönergesi eylemlerine ilişkin sıra numaralarıyla ilgili dikkatli olun.
1. **Ad** alanına yerleşim yönergesi eyleminin adını girin. Eylemin ne olduğunun açık olması için net olun.
1. İsteğe bağlı: Ambar yerleşimlerini ve diğer ölçütleri değiştirmek için **Sorguyu düzenle** 'yi seçin.
1. İsteğe bağlı: Bir yerleşim yönergesi için aşağıdaki ek alanları ayarlayabilirsiniz.

    | Alan | Tanım |
    |---|---|
    | Sabit yerleşim kullanımı | Yerleşim yönergesinin dikkate alması gereken yerleşimleri seçin:<ul><li>**Sabit ve sabit olmayan yerleşimler** - Yerleşim yönergesi tüm yerleşimleri kabul eder.</li><li>**Ürün için yalnızca sabit yerleşimler** - Yerleşim yönergesi ürünler için yalnızca sabit yerleşimleri kabul edecektir.</li><li>**Ürün çeşidi için yalnızca sabit yerleşimler** - Yerleşim yönergesi ürün çeşitleri için yalnızca sabit yerleşimleri kabul edecektir.</li></ul> |
    | Negatif stoğa izin ver | Belirtilen ambar konumunda eksi stoğa izin vermek için bu onay kutusunu seçin. |
    | Toplu iş etkinleştirildi | Etkin toplu iş öğeleri için toplu iş stratejileri kullanmak için bu onay kutusunu seçin. Bu onay kutusu işaretliyse ve **Strateji** alanı *Hiçbiri* olarak ayarlanmışsa , sistem sonraki eylem satırına geçer. |
    | Strateji | Yerleşim yönergesinin kullanması gereken stratejiyi seçin:<ul><li>**Hiçbiri** – Strateji kullanılmaz.</li><li>**Paketleme miktarını eşleştir** - Bu strateji çekme yerleşiminin belirtilen paketleme miktarına sahip olup olmadığını denetler. Bu strateji yalnızca **İş türü** alanı *Çekme* olarak ayarlandığında geçerlidir.</li><li>**Birleştir** - Bu strateji, benzer maddeler kullanılabilir olduğunda maddeleri belirli bir yerleşimde birleştirmek için kullanılır. Bu strateji yalnızca **İş türü** alanı *Koyma* olarak ayarlandığında geçerlidir. Koyma eylemi için normal bir kurulumda, sistem ilk eylem satırında birleştirme yapmaya çalışır ve ardından ikinci eylem satırında birleştirme olmadan koyma işlemini gerçekleştirmeyi dener. Ürünleri birleştirmek, sonraki çekmeleri daha verimli hale getirir.</li><li>**FEFO toplu iş rezervasyonu** - Bu strateji stok toplu iş bitiş tarihi kullanarak konumlandırıldığında ve toplu iş rezervasyonu için tahsis edildiğinde kullanılır. İlk bitiş tarihi, ilk çıkış (FEFO) toplu iş rezervasyon stratejisi, sona erme tarihine ek olarak toplu iş son kullanma tarihini kullanılarak stok bulunduğunda da kullanılır. Bu stratejiyi yalnızca toplu iş etkinleştirilmiş maddelerde kullanabilirsiniz. Bu strateji yalnızca **İş türü** alanı *Çekme* olarak ayarlandığında geçerlidir. Bu stratejiyi seçtiğinizde, uygulanan toplu iş numaraları için tüm sorgu sıralamasını geçersiz kılarsınız.</li><li>**Tam LP'ye yuvarla** - Bu strateji stok miktarını, çekilecek maddelere atanan plaka (LP) miktarıyla eşleşecek şekilde yuvarlamak için kullanılır. Bu strateji yalnızca, yerleşim yönergelerinin stok yenileme türü için ve yalnızca **İş türü** alanı *Çekme* olarak ayarlandığında kullanılabilir.</li><li>**Gelen iş olmadan boş yerleşim** - Bu strateji boş yerleşimleri bulmak için kullanılır. Fiziksel stoğu yoksa ve gelen iş beklenmiyorsa yerleşim boş olarak değerlendirilir. Bu strateji yalnızca **İş türü** alanı *Koyma* olarak ayarlandığında geçerlidir.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Konum yönergelerini kullanım örneği

Bu örnekte, konum yönergesinin, alış noktasında kaydedilen stok öğeleri için bir ambar içinde serbest kapasite bulmasının gerektiği bir satınalma siparişi işlemini ele alacağız. İlk olarak, mevcut eldeki stok ile birleştirerek ambar içinde boş kapasite bulmanız gerekir. Konsolidasyon mümkün değilse, bu durumda boş bir yer bulmanız gerekir.

Bu senaryo için iki konum yönergesi eylemi tanımlamanız gerek. Sıradaki ilk eylemin **Konsolide Et** stratejisini ve ikinci eylemin **Gelen iş olmayan boş yer** stratejisini kullanması gerekir. Bir taşma senaryosunu idare etmek için üçüncü bir eylem tanımlamadığınız takdirde, ambarda daha fazla kapasite olmadığında iki sonucun meydana gelmesi olasıdır: iş hiçbir konum tanımlanmasa da oluşturulabilir veya iş oluşturma işlemi başarısız olabilir. Sonuç **Konum yönergesi hataları** sayfasındaki ayara göre belirlenir; burada her bir iş siparişi türü için **Konum yönergesi hatasında işi durdur** seçeneğini seçip seçmemeye karar verebilirsiniz.

## <a name="next-step"></a>Sonraki adım

Yerleşim yönergeleri oluşturduktan sonra, her yönerge kodunu iş oluşturma için bir iş şablonu koduyla ilişkilendirebilirsiniz. Daha fazla bilgi için bkz. [İş şablonları ve yerleşim yönergeleri kullanarak ambar işini denetleme](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Sistem yöneticileri için teknik bilgiler

Bu görevin tamamlanması için kullanılan sayfalara erişiminiz bulunmuyorsa, sistem yöneticinizle iletişime geçin ve aşağıdaki tabloda gösterilen bilgileri verin.

| Kategori | Önkoşul |
|---|---|
| Konfigürasyon anahtarları | **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin. **Ticaret** lisans anahtarını açın ve **Ambar ve Taşıma yönetimi** yapılandırma anahtarını seçin. |
