---
title: Esnek ambar düzeyi boyut rezervasyon ilkesi
description: Bu konu, toplu işle izlenen ürünler satan ve lojistiklerini WMS-etkin operasyonlar olarak çalıştıran işletmelerin, ürünlerle ilişkili rezervasyon hiyerarşisi belirli toplu işlerin rezervasyonuna izin vermese bile, belirli toplu işleri rezerve etmelerine izin veren stok rezervasyon ilkesini açıklar.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 6c462a87494c434a6047542d448a85b3bce9f769
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346480"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Esnek ambar düzeyi boyut rezervasyon ilkesi

[!include [banner](../includes/banner.md)]

"Toplu iş-\[yerleşim\] altı" türünde stok rezervasyon hiyerarşisi ürünlerle ilişkiliyse, toplu işle izlenen ürünler satan ve lojistiklerini Microsoft Dynamics 365 Warehouse Management System (WMS) için etkinleştirilmiş operasyonlar olarak yürüten işletmeler, müşteri satış siparişleri için bu ürünlerin belirli toplu işlerini rezerve edemez. Bu konu, ürünler bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisiyle ilişkili olsa bile, bu işletmelerin belirli toplu işleri rezerve etmelerine izin veren stok rezervasyon ilkesini açıklamaktadır.

## <a name="inventory-reservation-hierarchy"></a>Stok rezervasyonu hiyerarşisi

Bu bölüm, varolan stok rezervasyon hiyerarşisini özetlemektedir. Toplu işle izlenen ve seri izlenen kalemlerin işlenme şekline odaklanır.

Ambar mantığı, istenen miktarlara yerleşim atamaktan ve yerleşimi rezerve etmekten sorumluyken, stok rezervasyon hiyerarşisi, depolama boyutlarıyla ilgili olarak, talep emrinin tesis, ambar ve stok durumu zorunlu boyutlarını taşımasını zorunlu kılar. Başka bir deyişle, talep emri ve ambar operasyonları arasındaki etkileşimlerde, talep emrinde siparişin sevk çıkışının yapılacağı yerin (yani tesis ve ambar) belirtilmesi beklenir. Ambar, bunun üzerine, ambar tesislerindeki gerekli miktarı bulmak için kendi mantığını temel alır.

Bununla birlikte, işletmenin operasyon modelini yansıtmak için, izleme boyutları (toplu iş ve seri numaraları) daha fazla esneklik gerektirir. Bir stok rezervasyonu hiyerarşisi aşağıdaki koşulların geçerli olduğu senaryolar barındırabilir:

- İşletme, ambar depolama alanında miktarlar bulunduktan sonra, toplu iş veya seri numaraları olan miktarların çekilmesini yönetmek için kendi ambar operasyonlarını temel alır. Bu modele genellikle *Toplu iş-\[yerleşim\] altı* adı verilir. Genellikle, satıcı şirketle talebi oluşturan müşteriler için bir ürünün toplu iş veya seri numarası tanımlaması önemli olmadığı zaman kullanılır.
- Toplu iş veya seri numaraları bir müşterinin sipariş belirtiminin parçasıysa ve bunlar talep emrinde kaydedilirse, ambardaki miktarları bulan ambar operasyonları istenen belirli sayılarla sınırlandırılır ve bunları değiştirmelerine izin verilmez. Bu modele *Toplu iş-\[yerleşim\] üstü* adı verilir.

Bu senaryolarda sorun, serbest bırakılan her ürüne yalnızca bir stok rezervasyonu hiyerarşisinin atanabilmesidir. Bu nedenle, WMS'nin izlenen kalemleri işlemesi için, hiyerarşi ataması toplu iş veya seri numarasının ne zaman rezerve edilmesi gerektiğini (talep emri alındığı zaman veya ambar çekme işi sırasında) belirledikten sonra bu zamanlama geçici olarak değiştirilemez.

## <a name="flexible-reservation-for-batch-tracked-items"></a>Toplu işle izlenen kalemler için esnek rezervasyon

### <a name="business-scenario"></a>İş senaryosu

Bu senaryoda, bir şirket, mamul malların toplu iş numaralarına göre izlendiği bir stok stratejisi kullanıyor. Bu şirket aynı zamanda WMS iş yükünü de kullanıyor. Bu iş yükünün toplu iş etkin kalemler için ambar çekme ve sevkiyat operasyonları planlamak ve çalıştırmak için iyi donatılmış bir mantığı olduğundan, mamul kalemlerin çoğu bir "Toplu iş\[yerleşim\] altı" stok rezervasyon hiyerarşisiyle ilişkilendirilir. Bu tür operasyon kurulumunun avantajı, hangi toplu işlerin çekileceği ve bu maddelerin ambarda nereye koyulacağı ile ilgili kararların (yürürlükteki rezervasyon kararları), ambar çekme operasyonları başlayana kadar ertelenmesidir. Bunlar müşterinin siparişi verilirken yapılmaz.

"Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi şirketin işletme hedeflerine uygun olmakla birlikte, şirketin mevcut müşterilerinin birçoğu, ürünleri yeniden sipariş ettikleri zaman, daha önce satın aldıkları aynı toplu işi istemektedir. Bu nedenle, şirket, müşterinin aynı kalem için talebine bağlı olarak toplu iş rezervasyonu kurallarının işleniş biçiminde esneklik istiyor ve böylece aşağıdaki davranışlar ortaya çıkıyor:

- Bir toplu iş numarası, satış işlemcisi tarafından sipariş alınırken kaydedilip rezerve edilebilir ve ambar operasyonları sırasında değiştirilemez ve/veya başka taleplerle alınamaz. Bu davranış, sipariş edilen toplu iş numarasının müşteriye sevk edilmesini garantilemeye yardımcı olur.
- Toplu iş numarası müşteri için önemli değilse, ambar operasyonları, satış siparişi kaydı ve rezervasyon yapıldıktan sonra malzeme çekme işi sırasında bir toplu iş numarası belirleyebilir.

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a>Satış siparişinde belirli bir toplu işin rezervasyonuna izin verme

Bir "Toplu iş-\[yerleşim\] altı" stok rezervasyon hiyerarşisi ile ilişkilendirilmiş kalemler için toplu iş rezervasyon davranışında istenen esnekliği sağlamak için, stok yöneticilerinin, **Stok rezervasyonu hiyerarşileri** sayfasındaki **Toplu iş numarası** düzeyi için **Talep emrinde rezervasyona izin ver** onay kutusunu işaretlemeleri gerekir.

![Stok rezervasyonu hiyerarşisini esnek hale getirme](media/Flexible-inventory-reservation-hierarchy.png)

Hiyerarşide **Toplu iş numarası** düzeyi seçildiği zaman, o düzeyin üzerindeki ve **Yerleşim** düzeyine kadar olan tüm boyutlar otomatik olarak seçilir. (Varsayılan olarak **Yerleşim** düzeyinin üzerindeki tüm boyutlar önceden seçilmiştir.) Bu davranış, siz sipariş satırında belirli bir toplu iş numarasını rezerve ettikten sonra, toplu iş numarası ve yerleşim arasındaki aralıkta yer alan tüm boyutların da otomatik olarak rezerve edildiği mantığı yansıtır.

> [!NOTE]
> **Talep emrinde rezervasyona izin ver** onay kutusu yalnızca ambar yerleşim boyutunun altındaki rezervasyon hiyerarşisi düzeylerine uygulanır.
>
> **Toplu iş numarası**, hiyerarşide esnek rezervasyon ilkesi için açık olan tek düzeydir. Başka bir deyişle, **Yerleşim**, **Plaka** veya **Seri numarası** düzeyi için **Talep emrinde rezervasyona izin ver** onay kutusunu seçemezsiniz.
>
> Rezervasyon hiyerarşiniz her zaman **Toplu iş numarası** düzeyinin altında olması gereken seri numarası boyutunu içeriyorsa ve toplu iş numarası için toplu işe özel rezervasyonu etkinleştirdiyseniz, "Seri-\[yerleşim\] altı" rezervasyon ilkesi için geçerli olan kurallara dayalı olarak, sistem seri numarası rezervasyonu ve malzeme çekme operasyonlarını işlemeye devam eder.

Herhangi bir noktada, dağıtımınızda varolan bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi için toplu işe özel rezervasyona izin verebilirsiniz. Bu değişiklik, değişiklik yapılmadan önce oluşturulan rezervasyonları ve açık ambar işini etkilemez. Ancak, bu rezervasyon hiyerarşisiyle ilişkili bir veya daha fazla kalem için **Siparişli rezerve miktar**, **Fiziksel rezerve miktar** veya **Sipariş edilen** çıkış türünde stok hareketleri mevcutsa **Talep emrinde rezervasyona izin ver** onay kutusunun işareti kaldırılamaz.

> [!NOTE]
> Bir kalemin varolan rezervasyon hiyerarşisi siparişte toplu iş belirtimine izin vermiyorsa, hiyerarşi düzeyi yapısının her iki hiyerarşide de aynı olması koşuluyla, o kalemi toplu iş belirtimine izin veren bir rezervasyon hiyerarşisine yeniden atayabilirsiniz. Yeniden atamak için **Maddeler için rezervasyon hiyerarşisini değiştir** işlevini kullanın. Bu değişiklik, esnek toplu iş rezervasyonunu toplu iş izlemeli kalemlerin bir alt kümesi için önlemek ama ürün portföyünün geri kalanı için izin vermek istediğinizde uygun olabilir.

**Talep emrinde rezervasyona izin ver** onay kutusunu seçip seçmemenizden bağımsız olarak, bir sipariş satırındaki kalem için belirli bir toplu iş numarasını rezerve etmek istemiyorsanız, "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi için geçerli olan varsayılan ambar operasyonları mantığı uygulanmaya devam eder.

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a>Müşteri siparişi için belirli bir toplu iş numarasını rezerve etme

Toplu iş izlemeli bir maddenin "Toplu iş-\[yerleşim\] altı" stok rezervasyonu hiyerarşisi satış siparişlerinde belirli toplu iş numaralarının rezervasyonuna izin verecek şekilde ayarlandıktan sonra, satış siparişi işlemcileri, müşterinin talebine bağlı olarak, aynı kalem için müşteri siparişlerini aşağıdaki yollardan biriyle alabilir:

- **Sipariş ayrıntılarını bir toplu iş numarası belirtmeden girmek** – Ürünün toplu iş belirtimi müşteri için önemli değilse bu yaklaşım kullanılmalıdır. Sistemde bu tür bir siparişin işlenmesiyle ilişkili tüm varolan işlemler değişmeden kalır. Kullanıcılar tarafında ek bir değerlendirme gerekmez.
- **Sipariş ayrıntılarını girmek ve belirli bir toplu iş numarasını rezerve etmek** – Müşteri belirli bir toplu işi istediğinde bu yaklaşım kullanılmalıdır. Genellikle, müşteriler daha önce satın aldıkları bir ürünü yeniden sipariş ederken belirli bir toplu işi isteyecektir. Bu tür toplu iş rezervasyonuna *sipariş taahhütlü rezervasyon* adı verilir.

Miktarlar işlendiği ve belirli bir sipariş için bir toplu iş numarası taahhüt edildiği zaman aşağıdaki kural kümesi geçerlidir:

- "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesi altındaki bir kalem için belirli bir toplu iş numarasının rezervasyonuna izin vermek amacıyla, sistem yerleşim ve üzerindeki tüm boyutları rezerve etmelidir. Bu aralık genellikle plaka boyutunu içerir.
- Sipariş taahhütlü toplu iş rezervasyonu kullanan bir satış satırı için malzeme çekme işi oluşturulduğunda yerleşim yönergeleri kullanılmaz.
- Sipariş taahhütlü toplu işler için işin ambara işlenmesi sırasında, kullanıcının ve sistemin toplu iş numarasını değiştirmesine izin verilmez. (Bu işlem özel durum işlemeyi kapsar.)

Aşağıdaki örnekte uçtan uca akış gösterilmektedir.

## <a name="example-scenario"></a>Örnek senaryo

Bu örnek için, demo verilerinin yüklenmiş olması ve **USMF** demo veri şirketini kullanmanız gerekir.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a>Toplu işe özel rezervasyona izin vermek için bir stok rezervasyonu hiyerarşisi ayarlama

1. **Ambar yönetimi** \> **Kurulum** \> **Stok \> Rezervasyon hiyerarşisi**'ne gidin.
2. **Yeni**'yi seçin.
3. **Ad** alanına bir ad girin (örneğin **BatchFlex**).
4. **Açıklama** alanına bir açıklama girin (örneğin **Toplu iş alt esnek**).
5. **Seçili** alanda, **Seri numarası** ve **Sahip**'i seçin ve ardından sol ok düğmesini seçerek bunları **Kullanılabilir** alanına taşıyın.
6. **Tamam**'ı seçin.
7. **Toplu iş numarası** boyut düzeyinin satırında, **Talep emrinde rezervasyona izin ver** onay kutusunu seçin. **Plaka** ve **Yerleşim** düzeyleri otomatik olarak seçilir ve bunların onay kutularını temizleyemezsiniz.
8. **Kaydet**'i seçin.

### <a name="create-a-new-released-product"></a>Yeni bir serbest bırakılan ürün oluşturma

1. Bu değerleri kullanarak ürünün üç ana veri parametresini ayarlayın:

    - **Depolama boyutu grubu** alanında **Ambar**'ı seçin.
    - **İzleme boyutu grubu** alanında **Batch-Phy**'yi seçin.
    - **Rezervasyon hiyerarşisi** alanında **BatchFlex**'i seçin.

2. **B11** ve **B22** gibi iki toplu iş numarası oluşturun.
3. Aşağıdaki değerleri kullanarak eldeki stoka kalem miktarları ekleyin.

    | Ambar | Parti numarası | Konum | Plaka | Miktar |
    |-----------|--------------|----------|---------------|----------|
    | 24        | B11          | BULK-001 | Hiçbiri          | 10       |
    | 24        | B11          | FL-001   | LP11          | 10       |
    | 24        | B22          | FL-002   | LP22          | 10       |

### <a name="enter-sales-order-details"></a>Satış siparişi ayrıntılarını girin

1. **Satış ve pazarlama** \> **Satış siparişleri** \> **Tüm satış siparişleri**'ne gidin.
2. **Yeni**'yi seçin.
3. Satış siparişi başlığındaki **Müşteri hesabı** alanına **US-003** girin.
4. Yeni kalem için bir satır ekleyin ve miktar olarak **10** girin. **Ambar** alanının **24**'e ayarlandığından emin olun.
5. **Satış siparişi satırları** hızlı sekmesinde, **Stok**'u ve ardından **Bakım** grubunu seçin ve **Toplu iş rezervasyonu**'nu seçin. **Toplu iş rezervasyonu** sayfası, sipariş satırı rezervasyonu için kullanılabilecek toplu işlerin listesini gösterir. Bu örnekte, **B11** numaralı toplu iş için miktarı **20** ve **B22** numaralı toplu iş için miktarı **10** gösterir. Bir satırdaki kalem "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisiyle ilişkiliyse, toplu işe özel rezervasyona izin vermek üzere ayarlanmadığı sürece, **Toplu iş rezervasyonu** sayfasına o satırdan erişilemeyeceğine dikkat edin.

    > [!NOTE]
    > Bir satış siparişi için belirli bir toplu iş rezerve etmek isterseniz **Toplu iş rezervasyonu** sayfasını kullanmanız gerekir.
    >
    > Toplu iş numarasını doğrudan satış siparişi satırına girerseniz, sistem "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesine tabi olan bir kalem için belirli bir toplu iş değeri girmişsiniz gibi davranır. Satırı kaydettiğinizde bir uyarı iletisi alırsınız. Toplu iş numarasının doğrudan sipariş satırında belirtilmesi gerektiğini onaylarsanız, satır normal ambar yönetimi mantığı tarafından işlenmez.
    >
    > Miktarı **Rezervasyon** sayfasından rezerve ederseniz, belirli bir toplu iş rezerve edilmez ve satır için ambar operasyonları, "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesi altında uygulanabilecek kurallara uygun biçimde yürütülür.

    Genel olarak bu sayfa, ilişkili "Toplu iş-\[yerleşim\] altı" türünde rezervasyon hiyerarşisi olan kalemler için çalıştığı ve etkileşime girdiği şekilde çalışıp etkileşime girer. Ancak, aşağıdaki özel durumlar geçerlidir:

    - **Kaynak satıra taahhütlü toplu iş numaraları** hızlı sekmesi, sipariş satırı için rezerve edilen toplu iş numaralarını gösterir. Kılavuzdaki toplu iş değerleri, ambar işleme aşamaları da dahil olmak üzere, sipariş satırının karşılanma döngüsü boyunca gösterilir. Bunun aksine, **Genel bakış** hızlı sekmesinde, normal sipariş satırı rezervasyonu (yani **Yerleşim** düzeyinin üzerindeki boyutlar için yapılan rezervasyon), ambar işinin oluşturulduğu noktaya kadar kılavuzda gösterilir. Bunun üzerine, iş varlığı satır rezervasyonunu üstlenir ve satır rezervasyonu artık sayfada görünmez. **Kaynak satıra taahhütlü toplu iş numaraları** hızlı sekmesi, satış siparişi işlemcisinin, faturalamaya kadar yaşam döngüsünün her noktasında, müşterinin siparişine taahhüt edilmiş toplu iş numaralarını görüntüleyebilmesine yardımcı olur.
    - Belirli bir toplu işi rezerve etmeye ek olarak, bir kullanıcı sistemin otomatik olarak seçmesine izin vermek yerine toplu işin özel yerleşimini ve plakasını kendisi seçebilir. Bu yetenek, sipariş taahhütlü toplu iş rezervasyon mekanizmasının tasarımıyla ilgilidir. Daha önce belirtildiği gibi, bir toplu iş numarası "Toplu iş-\[yerleşim\] altı" rezervasyon ilkesi altındaki bir kalem için rezerve edildiği zaman, sistem yerleşime kadar olan tüm boyutları rezerve etmelidir. Bu nedenle, ambar işi, siparişlerle çalışan kullanıcılar tarafından rezerve edilmiş olan aynı depolama boyutlarını taşır ve malzeme çekme operasyonları için uygun ve hatta olası olan kalem depolama yerleşimini temsil edemeyebilir. Sipariş işlemciler ambar kısıtlamalarını biliyorsa, toplu iş rezerve ederken belirli yerleşimleri ve plakaları kendileri seçmek isteyebilirler. Bu durumda , kullanıcının sayfa üst bilgisindeki **Boyutları görüntüle** işlevini kullanması, **Genel bakış** hızlı sekmesindeki kılavuza yerleşimi ve plakayı eklemesi gerekir.

6. **Toplu iş rezervasyonu** sayfasında toplu iş **B11** numaralı toplu işe ait satırı ve ardından **Satırı rezerve et**'i seçin. Otomatik rezervasyon sırasında yerleşimleri ve plakaları atamak için belirlenmiş bir mantık yoktur. Miktarı **Rezervasyon** alanına el ile girebilirsiniz. **Kaynak satırına taahhütlü toplu iş numaraları** hızlı sekmesinde, **B11** numaralı toplu işin **Taahhüt edilen** olarak gösterildiğine dikkat edin.

    ![Toplu iş rezervasyonu sayfasındaki bir satış siparişi satırı için belirli bir toplu iş numarasını taahhüt etme](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > Bir satış siparişi satırındaki miktarın rezervasyonu çoklu toplu işler arasında yapılabilir. Benzer şekilde, aynı toplu işin rezervasyonu birden çok yerleşime ve plakaya karşı yapılabilir (yerleşimler için plakalar etkinleştirilirse).
    >
    > Bir satış siparişi satırındaki miktar için belirli bir toplu işin rezervasyonu kısmi de olabilir. Örneğin, 100 birimlik toplam miktar, belirli bir toplu işe 20 birim taahhüt edilirken, uygun herhangi bir toplu işe tesis ve ambar düzeylerinde 80 birim rezerve edilecek şekilde rezerve edilebilir. Bu durumda, WMS malzeme çekme işlemlerini iki ayrı iş satırı kullanarak işler.

7. **Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılmış ürünler**'e gidin. Kaleminizi ve ardından **Stok yönetimi** \> **Görüntüle** \> **Hareketler**'i seçin.

    ![Bir stok hareketi türü olarak sipariş taahhütlü rezervasyon](media/Inventory-transactions-for-order-committed-reservation.png)

8. Kalemin, satış siparişi satırı rezervasyonuna ilişkin stok hareketlerini inceleyin.

    - **Referans** alanının **Satış siparişi** olarak ve **Çıkış** alanının **Fiziksel rezerve miktar** olarak ayarlandığı bir hareket, **Yerleşim** düzeyinin üzerindeki stok boyutları için sipariş satırı rezervasyonunu temsil eder. Kalemin stok rezervasyonu hiyerarşisine göre bu boyutlar tesis, ambar ve stok durumudur.
    - **Referans** alanının **Sipariş taahhütlü rezervasyon** olarak ve **Çıkış** alanının **Fiziksel rezerve miktar** olarak ayarlandığı bir hareket, belirli toplu iş ve onun üzerindeki tüm stok boyutları için sipariş satırı rezervasyonunu temsil eder. Kalemin stok rezervasyonu hiyerarşisine göre bu boyutlar toplu iş numarası ve yerleşimidir. Bu örnekte yerleşim **Bulk-001**'dir.

9. Satış siparişi üst bilgisinde **Ambar** \> **Eylemler** \> **Ambara serbest bırak**'ı seçin. Sipariş satırı artık dalgalıdır ve bir yük ve iş oluşturulur.

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a>Sipariş taahhütlü toplu iş numaraları olan ambar işini inceleyin ve işleyin

1. **Satış siparişi satırları** hızlı sekmesinde **Ambar** \> **İş ayrıntıları**'nı seçin.

    Satış siparişi satırına taahhüt edilen toplu iş miktarları için malzeme çekme işlemini işleyen iş aşağıdaki özelliklere sahiptir:

    - Sistem iş oluşturmak için, yerleşim yönergelerini değil sistem çalışma şablonlarını kullanır. Yeni işin oluşturulacağı zamanı belirlemek için, en fazla malzeme çekme satırı veya özel bir ölçü birimi gibi iş şablonları için tanımlanan tüm standart ayarlar uygulanır. Bununla birlikte, sipariş taahhütlü rezervasyon tüm stok boyutlarını zaten belirttiğinden, çekme yerleşimlerinin belirlenmesi ile ilgili yerleşim yönergeleriyle ilişkili kurallar dikkate alınmaz. Bu stok boyutları, ambar depolama düzeyindeki boyutları içerir. Bu nedenle, iş, yerleşim yönergelerine danışmak zorunda kalmadan bu boyutları devralır.
    - Toplu iş numarası, çekme satırında gösterilmez (ilişkili bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisi olan bir kalem için oluşturulan iş satırında olduğu gibi). Bunun yerine, "ilk" toplu iş numarası ve tüm diğer depolama boyutları, ilişkili stok hareketlerinden referansta bulunulan iş satırı iş stok hareketinde gösterilir.

        ![Sipariş taahhütlü rezervasyondan kaynaklanan iş için ambar stok hareketi](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - İş oluşturulduktan sonra, **Referans** alanının **Sipariş taahhütlü rezervasyon** olarak ayarlandığı kalem stok hareketi kaldırılır. **Referans** alanının **İş** olarak ayarlandığı stok hareketi, miktarın tüm stok boyutlarında fiziksel rezervasyonu tutar.

        Ambar operasyonları her zaman olduğu gibi işin yürütülmesini işlemeye devam edebilir. Ancak, mobil cihazdaki yönergelerde çalışandan belirli bir toplu iş numarası seçmesi istenir. Yerleşimlerin plaka denetimli olduğu ambar ortamlarında, bir çalışan birden fazla plakada aynı toplu işi depolayan bir yerleşime ulaştığında, henüz rezerve edilmemiş olan (örneğin başka bir sipariş taahhütlü rezervasyon veya o türde bir rezervasyondan kaynaklanan iş tarafından) herhangi bir plakayı seçebilir.

        İş satırında belirtilen yerleşimden seçim yapılması pratik değilse, ambar operatörleri, belirli toplu işin çekilmesini daha uygun bir yerleşimden yeniden yönlendirmek için aşağıdaki eylemlerden birini kullanabilir:

        - Bir mobil cihazdaki standart **Konumu geçersiz kıl** eylemi (ambar çalışanının **Çekme yerleşimini geçersiz kılmaya izin ver** ayarını etkinleştirmesi koşuluyla)
        - **Çalışma listesi ayrıntıları** sayfasında **Yerleşimi değiştir** eylemi. 

2. Mobil cihazda, işi çekme ve yerleştirme işlemini tamamlayın.

    Artık **B11** numaralı toplu iş için **10** miktarı artık satış siparişi satırı için çekilmiş ve **Baydoor** yerleşimine yerleştirilmiştir. Bu noktada, miktar kamyona yüklenmeye ve müşterinin adresine gönderilmeye hazırdır.

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a>Sipariş taahhütlü toplu iş numaraları olan ambar işinin özel durumunu işleme

Sipariş taahhütlü toplu iş numaralarını toplama için yapılan ambar işi, normal işle aynı standart ambar özel durum işlemeye tabidir. Genel olarak, açık iş veya iş satırı iptal edilebilir, bir kullanıcı yerleşimi dolu olduğu için durdurulabilir ve bir hareket nedeniyle güncelleştirilebilir. Benzer şekilde, zaten tamamlanmış olan çekilmiş iş miktarı azaltılabilir veya işe ters işlem uygulanabilir.

Tüm bu özel durum işleme eylemlerine şu temel kural uygulanır: Müşteri için rezerve edilen parti numarası başka bir toplu iş numarasıyla değiştirilemez ancak depolama boyutları (yerleşim ve plaka) bir kullanıcının el ile yapacağı güncelleştirmeyle ya da sistemin otomatik güncelleştirmesiyle değiştirilebilir. Otomatik güncelleştirme, belirli bir toplu iş otomatik olarak rezerve edildiği ama depolama boyutları belirlenmediği zaman uygulanan aynı rastgele depolama boyutları atamasına dayanır.

### <a name="example-scenario"></a>Örnek senaryo

Bu senaryoya bir örnek, önceden tamamlanan işin seçiminin **Çekilen miktarı düş** işleviyle iptal edildiği durumdur. Bu örnek, bu konudaki önceki örneğin devamıdır.

1. **Ambar yönetimi** \> **Yükler** \> **Etkin yükler**'e gidin.
2. Satış siparişinin sevkiyatı ile bağlantılı olarak oluşturulan yükü seçin.
3. **Yük emri satırları** hızlı sekmesinden, **Çekilen miktarı düş**'ü seçin.
4. **Çekilen miktarı düş** sayfasındaki **Yerleşime taşı** alanında **FL-001**'i seçin.
5. **Plakaya taşı** alanında **LP33**'ü seçin.
6. Kılavuzdaki **Çekme işlemi geri alınacak stok miktarı** alanına **10** girin.
7. **Tamam**'ı seçin.

Çekme işlemini geri alma eyleminin sonuçları:

- Daha önce kapatılan işin durumu **İptal edildi** olarak ayarlanır.
- **B11** numaralı toplu işte çekme işlemi iptal edilen **10** miktarı için **Stok hareketi** türünde yeni iş oluşturulur. Bu iş, **Baydoor** yerleşiminden **FL-001** yerleşimindeki **LP33** numaralı plakaya hareketi temsil eder. Durum ayarı **Kapalı** yapılır.
- Sistem, başlangıçta sipariş edilen toplu iş numarasını yeniden rezerve edip yerleşim ve plaka kodlarının atamasını yapar. (Bu işlem, belirli bir toplu iş numarasına yönelik olarak sipariş satırı için **Satırı rezerve et** işlevini çalıştırmaya eşdeğerdir.) Sonuç olarak **B11** numaralı toplu iş, **Toplu iş rezervasyonu** sayfasının **Kaynak satırına taahhütlü toplu iş numaraları** hızlı sekmesinde Taahhüt edildi olarak gösterilir ve **Rezervasyon** alanında **B11** numaralı toplu iş için **10** miktarı yer alır. Ek olarak, **Yerleşim** alanı ayarı **FL-001**, **Plaka** alanı ayarı **LP11** olur. (Bu alanlar görünmüyorsa, kılavuza ekleyebilirsiniz.)

Aşağıdaki tablolarda, sistemin belirli ambar eylemleri için sipariş taahhütlü toplu iş rezervasyonunu nasıl işleyeceğine ilişkin genel bilgiler verilmektedir. Tablolardaki içeriği yorumlamak için, her ambar eyleminin, sipariş taahhütlü bir toplu iş rezervasyonundan kaynaklanan mevcut ambar işi bağlamında çalıştırıldığını veya her ambar eyleminin bu türdeki işi etkilediğini varsayın.

> [!NOTE]
> Bu tablolarda "Toplu iş miktarı kullanılabilir" sütunu, mevcut sipariş taahhütlü rezervasyonlar için zaten rezerve edilmiş veya o türdeki rezervasyonlardan kaynaklanan ambar işi tarafından önceden rezerve edilmiş miktara ek olarak bir toplu iş miktarının kullanılabilir olup olmadığını gösterir.

#### <a name="override-the-pick-location-on-the-open-work"></a>Açık işte çekme yerleşimini geçersiz kılma

<table>
<thead>
<tr>
<th>Temel kurulum parametresi</th>
<th>Toplu iş miktarı kullanılabilir</th>
<th>Temel kullanıcı adımları</th>
<th>Ambar işi</th>
<th>Sipariş taahhütlü toplu iş rezervasyonu</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><strong>Çekme yerleşimini geçersiz kılmaya izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</td>
<td>Evet</td>
<td>
<ol>
<li>Malzeme çekme işini başlatırken ambarlama uygulamasında <strong>Konumu geçersiz kıl</strong> menü öğesini seçin.</li>
<li><strong>Öner</strong>'i seçin.</li>
<li>Toplu iş miktarı kullanılabilirliğine dayalı olarak önerilen yeni yerleşimi onaylayın.</li>
</ol>
</td>
<td>Geçerli işte aşağıdaki eylemler gerçekleşir:
<ul>
<li>Çekme satırındaki yerleşim yeni yerleşime güncelleştirilir. (Yerleşim plaka denetimliyse, iş stok hareketine rastgele bir plaka atanır ve çalışan, kullanılabilir miktarlı herhangi bir plakadan çekme işlemi yapabilir.)</li>
<li>Miktar yeni yerleşimde birden fazla plakada bulunursa, orijinal çekme satırı her bir plakayla eşleştirilmek üzere birden çok satıra bölünür.</li>
</ul>
</td>
<td>Geçerli değil</td>
</tr>
<tr>
<td>No</td>
<td>
<ol>
<li>Malzeme çekme işini başlatırken ambarlama uygulamasında <strong>Konumu geçersiz kıl</strong> menü öğesini seçin.</li>
<li>El ile bir yerleşim girin.</li>
</ol>
</td>
<td><strong>Konumu geçersiz kıl</strong> eylemi mümkün değildir. Başarısız olur ve bir hata oluşur.</td>
<td>Uygulanamaz</td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a>Tam düğme – Kullanıcı yerleşimindeki taşma nedeniyle bir iş satırını bölün

<table>
<thead>
<tr>
<th>Temel kurulum parametresi</th>
<th>Toplu iş miktarı kullanılabilir</th>
<th>Temel kullanıcı adımları</th>
<th>Ambar işi</th>
<th>Sipariş taahhütlü toplu iş rezervasyonu</th>
</tr>
</thead>
<tbody>
<tr>
<td>Mobil cihaz menü öğesinde <strong>İşin bölünmesine izin ver</strong> seçeneği etkinleştirilir.</td>
<td>Geçerli değil</td>
<td>
<ol>
<li>Malzeme çekme işini işlerken ambarlama uygulamasındaki <strong>Tam</strong> menü öğesini seçin.</li>
<li><strong>Çekme Miktarı</strong> alanında, tam kapasiteyi belirtmek için gereken kısmi bir çekme miktarı girin.</li>
</ol>
</td>
<td>
<ul>
<li>Geçerli işte, miktar, çekilmesi gereken kalan miktara güncelleştirilir.</li>
<li>Çekilen miktar için yeni iş oluşturulur ve kapatılır.</li>
</ul></td>
<td>Uygulanamaz</td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a>Tamamlanan işin çekilen miktarını bir yükten düşme

<table>
<thead>
<tr>
<th>Temel kurulum parametresi</th>
<th>Toplu iş miktarı kullanılabilir</th>
<th>Temel kullanıcı adımları</th>
<th>Ambar işi</th>
<th>Sipariş taahhütlü toplu iş rezervasyonu</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'>Uygulanamaz</td>
<td>Evet</td>
<td>
<ol>
<li>Yük satırından <strong>Çekilen miktarı düş</strong> sayfasını açın.</li>
<li>Çekme işlemi iptal edilecek tam miktarı girin.</li>
<li>Bir "taşıma" yerleşimi/plakası seçin.</li>
</ol>
</td>
<td>
<ul> 
<li>Yük satırıyla ilişkili iş iptal edilir.</li>
<li>Stok hareketi için yeni iş oluşturulur ve kapatılır.</li>
</ul>
</td>
<td>Miktar aynı toplu iş için yeniden rezerve edilir. Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</td>
</tr>
<tr>
<td>Hayır</td>
<td>Önceki satıra bakın.</td>
<td>Önceki satıra bakın.</td>
<td>Miktar; aynı toplu iş için ve çekme işlemi iptal sırasında girilen aynı yerleşim ve plaka (yerleşim plaka denetimliyse) için yeniden rezerve edilir.</td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a>Ambar içinde bir kalemi taşıma

> [!NOTE]
> Bu ambar eylemi şablonla hareket için değil, yalnızca **İş oluşturma işlemi** türündeki hareket için geçerlidir.

<table>
<thead>
<tr>
<th>Temel kurulum parametresi</th>
<th>Toplu iş miktarı kullanılabilir</th>
<th>Temel kullanıcı adımları</th>
<th>Ambar işi</th>
<th>Sipariş taahhütlü toplu iş rezervasyonu</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><strong>Stoğun ilişkili işle birlikte taşınmasına izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</td>
<td>Evet</td>
<td>
<ol>
<li>Ambarlama uygulamasında bir hareket başlatın.</li>
<li>"Çıkış" ve "hedef" yerleşimlerini girin.</li>
</ol></td>
<td>
<ul>
<li>Taşımadan etkilenen mevcut tüm işte çekme yerleşimi yeni "hedef" yerleşime güncelleştirilir.</li>
<li>Stok hareketi için yeni iş oluşturulur ve kapatılır.</li>
</ul>
</td>
<td>Belirtilen yerleşimden miktar hareketinden etkilenen mevcut tüm rezervasyonlar aynı toplu iş için yeniden rezerve edilir. Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</td>
</tr>
<tr>
<td>Hayır</td>
<td>Önceki satıra bakın.</td>
<td>Önceki satıra bakın.</td>
<td>Belirtilen yerleşimden miktar hareketinden etkilenen tüm mevcut rezervasyonlar aynı toplu iş için ve yeni "hedef" yerleşim ve plaka (yerleşim plaka denetimliyse) için yeniden rezerve edilir.</td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a>Tamamlanan işin çekilen miktarını bir yükten veya dalgadan geri alma

<table>
<thead>
<tr>
<th>Temel kurulum parametresi</th>
<th>Toplu iş miktarı kullanılabilir</th>
<th>Temel kullanıcı adımları</th>
<th>Ambar işi</th>
<th>Sipariş taahhütlü toplu iş rezervasyonu</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'>Uygulanamaz</td>
<td>Evet</td>
<td>
<ol>
<li><strong>İşi geri al</strong> sayfasını açın.</li>
<li>İstek sayfasında <strong>Maddeleri geçerli konumda bırak</strong>seçeneğini belirleyin.</li>
</ol>
</td>
<td>Yükle ilişkili tüm iş iptal edilir.</td>
<td>Miktar aynı toplu iş için yeniden rezerve edilir. Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</td>
</tr>
<tr>
<td>Hayır</td>
<td>Önceki satıra bakın.</td>
<td>Önceki satıra bakın.</td>
<td>Miktar, aynı toplu iş için ve miktarın geri almaya bırakıldığı yerleşim ve plaka için yeniden rezerve edilir.</td>
</tr>
<tr>
<td>Evet</td>
<td>
<ol>
<li><strong>İşi geri al</strong> sayfasını açın.</li>
<li>İstek sayfasında <strong>Maddeleri bu konuma ata</strong>seçeneğini belirleyin.</li>
</ol>
</td>
<td>
<ul>
<li>Geçerli iş iptal edilir.</li>
<li>Stok hareketi için yeni iş oluşturulur ve kapatılır.</li>
</ul>
</td>
<td>Miktar aynı toplu iş için yeniden rezerve edilir. Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</td>
</tr>
<tr>
<td>Hayır</td>
<td>Önceki satıra bakın.</td>
<td>Önceki satıra bakın.</td>
<td>Miktar, aynı toplu iş için ve miktarın geri alma işlemine atandığı yerleşim ve plaka için yeniden rezerve edilir.</td>
</tr>
<tr>
<td>Evet/Hayır</td>
<td>
<ol>
<li><strong>İşi geri al</strong> sayfasını açın.</li>
<li>İstek sayfasında <strong>Maddeleri bu konuma taşı</strong>seçeneğini belirleyin.</li>
</ol>
</td>
<td>Ters işlem desteklenmez.</td>
<td>Uygulanamaz</td>
</tr>
<tr>
<td>Evet/Hayır</td>
<td>
<ol>
<li><strong>İşi geri al</strong> sayfasını açın.</li>
<li>İstek sayfasında <strong>Maddeleri konum yönergelerine göre taşı</strong> seçeneğini belirleyin.</li>
</ol>
</td>
<td>Ters işlem desteklenmez. </td>
<td>Uygulanamaz</td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a>Miktarı eksik seçme – Siz malzeme çekme işini gerçekleştirirken, miktarın kaydını yerleşimde/plakada fiziksel olarak bulunamadı şeklinde yapın

<table>
<thead>
<tr>
<th>Temel kurulum parametresi</th>
<th>Toplu iş miktarı kullanılabilir</th>
<th>Temel kullanıcı adımları</th>
<th>Ambar işi</th>
<th>Sipariş taahhütlü toplu iş rezervasyonu</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>Yok</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Hayır</strong>.</td>
<td>Evet</td>
<td>
<ol>
<li>Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</li>
<li><strong>Malzeme çekme miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</li>
<li><strong>Neden</strong> alanına <strong>Yeniden tahsis yok</strong> girin.</li>
</ol>
</td>
<td>
<ul>
<li>Geçerli iş kapalı ve çekilen miktar 0 (sıfır).</li>
<li>Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</li>
</ul>
</td>
<td>Miktar aynı toplu iş için yeniden rezerve edilir. Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</td>
</tr>
<tr>
<td>Hayır</td>
<td>Önceki satıra bakın.</td>
<td>
<ul>
<li>Eksik malzeme çekme eylemi başarısız olur ve bir hata oluşur.</li>
<li>Geçerli iş açık kalır.</li>
</ul>
</td>
<td>Uygulanamaz</td>
</tr>
<tr>
<td rowspan='2'><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>Yok</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Evet</strong>.</td>
<td>Evet</td>
<td>
<ol>
<li>Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</li>
<li><strong>Malzeme çekme miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</li>
<li><strong>Neden</strong> alanına <strong>Yeniden tahsis yok</strong> girin.</li>
</ol>
</td>
<td>
<ul>
<li>Geçerli iş kapalı ve çekilen miktar 0 (sıfır).</li>
<li>Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</li>
</ul>
</td>
<td>Eksik çekilen yerleşimde miktar düzeltmeden etkilenen mevcut tüm rezervasyonlar aynı toplu iş için yeniden rezerve edilir. Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</td>
</tr>
<tr>
<td>Hayır</td>
<td>Önceki satıra bakın.</td>
<td>Önceki satıra bakın.</td>
<td>Eksik çekilen yerleşimde miktar düzeltmeden etkilenen mevcut tüm rezervasyonlar kaldırılır.</td>
</tr>
<tr>
<td><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>El ile</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Hayır/Evet</strong>. Ek olarak, <strong>El ile madde yeniden tahsisine izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</td>
<td>Evet</td>
<td>
<ol>
<li>Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</li>
<li><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</li>
<li><strong>Neden</strong> alanında <strong>El ile tahsisatla kısa malzeme çekme</strong>'yi seçin.</li>
<li>Listede yerleşimi/plakayı seçin.</li>
</ol>
</td>
<td>
<ul>
<li>Geçerli işte aşağıdaki eylemler gerçekleşir:
<ul>
<li>Çekme satırı kapalı ve çekilen miktar 0 (sıfır).</li>
<li>Yerine koyma satırı iptal edilir.</li>
<li>Yeni bir çekme satırı oluşturulur. Satır, kullanıcının seçtiği yerleşimi/plakayı kullanır.</li>
<li>Yeni bir yerine koyma satırı oluşturulur.</li>
</ul>
</li>
<li>Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</li>
</ul>
</td>
<td>Uygulanamaz</td>
</tr>
<tr>
<td><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>El ile</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Hayır</strong>. Ek olarak, <strong>El ile madde yeniden tahsisine izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</td>
<td>No</td>
<td>
<ol>
<li>Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</li>
<li><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</li>
<li><strong>Neden</strong> alanında <strong>El ile tahsisatla kısa malzeme çekme</strong>'yi seçin.</li>
</ol>
</td>
<td>Eksik malzeme çekme eylemi başarısız olur ve bir hata oluşur.</td>
<td>Uygulanamaz</td>
</tr>
<tr>
<td><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>El ile</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Evet</strong>. Ek olarak, <strong>El ile madde yeniden tahsisine izin ver</strong> seçeneği çalışanda etkinleştirilmiştir.</td>
<td>No</td>
<td>
<ol>
<li>Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</li>
<li><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</li>
<li><strong>Neden</strong> alanında <strong>El ile tahsisatla kısa malzeme çekme</strong>'yi seçin.</li>
<li>Listede yerleşimi/plakayı seçin.</li>
</ol>
</td>
<td>
<ul>
<li>Geçerli işte aşağıdaki eylemler gerçekleşir:
<ul>
<li>Çekme satırı kapalı ve çekilen miktar 0 (sıfır).</li>
<li>Yerine koyma satırı iptal edilir.</li>
</ul>
</li>
<li>Düzeltmeyi temsil için <strong>Sayım</strong> türünde ve <strong>Satıldı</strong> çıkış türünde bir stok hareketi oluşturulur.</li>
</ul>
</td>
<td>Eksik çekilen yerleşimde/plakada miktar düzeltmeden etkilenen mevcut tüm rezervasyonlar kaldırılır.</td>
</tr>
<tr>
<td><strong>Eksik çekme</strong> türünde bir iş özel durumu ayarlanmıştır ve bu özel durumda ayarlar şöyledir: <strong>Madde yeniden tahsisi</strong> = <strong>Otomatik</strong>, <strong>Stoğu ayarla</strong> = <strong>Evet/Hayır</strong> ve <strong>Rezervasyonları kaldır</strong> = <strong>Evet/Hayır</strong>.</td>
<td>Geçerli değil</td>
<td>
<ol>
<li>Malzeme çekme işini çalıştırırken ambarlama uygulamasındaki <strong>Eksik çekme</strong> menü öğesini seçin.</li>
<li><strong>Eksik Çekme Miktarı</strong> alanına <strong>0</strong> (sıfır) girin.</li>
<li><strong>Neden</strong> alanında <strong>Otomatik tahsisatla kısa malzeme çekme</strong>'yi seçin.</li>
</ol>
</td>
<td>Otomatik yeniden tahsisat içeren eksik çekme desteklenmez.</td>
<td>Otomatik yeniden tahsisat içeren eksik çekme desteklenmez.</td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a>Stok durumunu değiştir

> [!NOTE]
> Bu ambar eylemi birden fazla giriş noktasından gerçekleştirilebilir. Burada gösterilen örnek, **Konuma göre eldeki** sayfasında **Stok durumu değişikliği** eylemini kullanır.

<table>
<thead>
<tr>
<th>Temel kurulum parametresi</th>
<th>Toplu iş miktarı kullanılabilir</th>
<th>Temel kullanıcı adımları</th>
<th>Ambar işi</th>
<th>Sipariş taahhütlü toplu iş rezervasyonu</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><strong>Ambar</strong> sekmesindeki <strong>Ambar</strong> kaydında, <strong>Rezervasyonları ve işaretleri kaldır</strong> alanının ayarı <strong>Rezervasyonlar</strong> veya <strong>İşaretler ve rezervasyonlar</strong> yapılır.</td>
<td>Evet</td>
<td>
<ol>
<li>Belirli bir yerleşim seçin.</li>
<li>Belirli bir kalem, yerleşim ve plakası (yerleşim plaka denetimliyse) olan bir satırı seçin.</li>
<li><strong>Stok durumu değişikliği</strong>'ni seçin.</li>
<li><strong>Stok durumu</strong> alanının ayarını <strong>Durdurma</strong> yapın.</li>
</ol>
</td>
<td>İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</td>
<td>
<ul>
<li>Miktar aynı toplu iş için yeniden rezerve edilir. Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</li>
<li>Stok durumu boyutundaki değişikliği temsil için <strong>Stok durumu değişikliği</strong> türünde iki stok hareketi oluşturulur.</li>
<li>Durdurulan miktarın rezervasyonunu temsil için <strong>Stok durdurma</strong> türünde ve <strong>Fiziksel rezerve miktar</strong> çıkış türünde bir stok hareketi oluşturulur.</li>
</ul>
</td>
</tr>
<tr>
<td>Hayır</td>
<td>Önceki satıra bakın.</td>
<td>İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</td>
<td>
<ul>
<li>Rezervasyon kaldırılır.</li>
<li>Stok durumu boyutundaki değişikliği temsil için <strong>Stok durumu değişikliği</strong> türünde iki stok hareketi oluşturulur.</li>
<li>Durdurulan miktarın rezervasyonunu temsil için <strong>Stok durdurma</strong> türünde ve <strong>Fiziksel rezerve miktar</strong> çıkış türünde bir stok hareketi oluşturulur.</li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><strong>Ambar</strong> sekmesindeki <strong>Ambar</strong> kaydında, <strong>Rezervasyonları ve işaretleri kaldır</strong> alanının ayarı <strong>Yok</strong> yapılır.</td>
<td>Evet</td>
<td>
<ol>
<li>Belirli bir yerleşim seçin.</li>
<li>Belirli bir kalem, yerleşim ve plakası (yerleşim plaka denetimliyse) olan bir satırı seçin.</li>
<li><strong>Stok durumu değişikliği</strong>'ni seçin.</li>
<li><strong>Stok durumu</strong> alanının ayarını <strong>Durdurma</strong> yapın.</li>
</ol>
</td>
<td>İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</td>
<td>Miktar aynı toplu iş için yeniden rezerve edilir. Sistem miktarın kullanılabilir olduğu bir yerleşimi ve plakayı (yerleşim plaka denetimliyse) rastgele atar.</td>
</tr>
<tr>
<td>Hayır</td>
<td>Önceki satıra bakın.</td>
<td>İş için rezerve edilen miktarlar için stok durumu değişikliklerine izin verilmez.</td>
<td>Stok durumu değişikliklerine izin verilmez.</td>
</tr>
</tbody>
</table>

## <a name="limitations"></a>Sınırlamalar

- Esnek ambar düzeyinde boyut rezervasyonu işlevi aşağıdaki özellikleri desteklemez:

    - Fiili ağırlık yönetimi
    - Fiziksel negatif stok
    - Sipariş edilen tedarikte rezervasyon
    - Transfer emirleri ve hammadde çekme

- Yönerge birimine göre ambalajlama için konteyner konsolidasyon kuralında sınırlamalar vardır. Sipariş taahhütlü rezervasyonlar için, **Yönerge birimine gör ambalajla**alanının etkinleştirildiği konteyner yapı şablonlarını kullanmamanızı öneririz. Geçerli tasarımda, ambar işi oluşturulurken yerleşim yönergeleri kullanılmaz. Bu nedenle, konteyner kullanımı dalga adımı sırasında yalnızca birim sıra grubundaki en küçük birim uygulanır.
