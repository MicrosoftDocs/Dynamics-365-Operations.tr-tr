---
title: Esnek ambar düzeyi boyut rezervasyon ilkesi
description: Bu konu, toplu işle izlenen ürünler satan ve lojistiklerini WMS-etkin operasyonlar olarak çalıştıran işletmelerin, ürünlerle ilişkili rezervasyon hiyerarşisi belirli toplu işlerin rezervasyonuna izin vermese bile, belirli toplu işleri rezerve etmelerine izin veren stok rezervasyon ilkesini açıklar.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7d855914e59d90dd082c9e9a027604579a2f411
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235424"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a>Esnek ambar düzeyi boyut rezervasyon ilkesi

[!include [banner](../includes/banner.md)]

"Toplu iş-\[yerleşim\] altı" türünde stok rezervasyon hiyerarşisi ürünlerle ilişkiliyse, toplu işle izlenen ürünler satan ve lojistiklerini Microsoft Dynamics 365 Warehouse Management System (WMS) için etkinleştirilmiş operasyonlar olarak yürüten işletmeler, müşteri satış siparişleri için bu ürünlerin belirli toplu işlerini rezerve edemez.

Benzer şekilde, satış siparişlerindeki ürünler varsayılan rezervasyon hiyerarşisiyle ilişkilendirildiğinde bu ürünler için belirli plakalar rezerve edilemez.

Bu konu, ürünler bir "Toplu iş-\[yerleşim\] altı" rezervasyon hiyerarşisiyle ilişkili olsa bile, bu işletmelerin belirli toplu işleri veya plakaları rezerve etmelerine izin veren stok rezervasyon ilkesini açıklamaktadır.

## <a name="inventory-reservation-hierarchy"></a>Stok rezervasyonu hiyerarşisi

Bu bölüm, varolan stok rezervasyon hiyerarşisini özetlemektedir.

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
> **Toplu iş numarası** ve **Plaka**, hiyerarşide esnek rezervasyon ilkesi için açık olan tek düzeydir. Başka bir deyişle, **Konum** veya **Seri numarası** düzeyi için **Talep emrinde rezervasyona izin ver** onay kutusunu seçemezsiniz.
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

## <a name="example-scenario-batch-number-allocation"></a>Örnek senaryo: Toplu iş numarası tahsisatı

Bu örnek için, demo verilerinin yüklenmiş olması ve **USMF** demo veri şirketini kullanmanız gerekir.

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a>Toplu işe özel rezervasyona izin vermek için bir stok rezervasyonu hiyerarşisi ayarlama

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

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a>Satış siparişi ayrıntılarını girin

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

## <a name="flexible-license-plate-reservation"></a>Esnek plaka rezervasyonu

### <a name="business-scenario"></a>İş senaryosu

Bu senaryoda, bir şirket ambar yönetimi ve iş işlemeyi kullanır ve iş oluşturulmadan önce, yük planlamayı Supply Chain Management dışındaki bağımsız paletler/kapsayıcılar düzeyinde işler. Bu kapsayıcılar, stok boyutlarında plakalarla temsil edilir. Bu nedenle, bu yaklaşım için malzeme çekme işi yapılmadan önce belirli plakaların önceden satış siparişi satırlarına atanması gereklidir. Şirket, plaka kuralları rezervasyonu kurallarının işlenme biçimi ile aşağıdaki davranışlar oluşmasını sağlayacak şekilde esneklik aramaktadır:

- Bir plaka, satış işlemcisi tarafından sipariş alınırken kaydedilip rezerve edilebilir ve başka taleplerle alınamaz. Bu davranış, planlanan plakanın müşteriye sevk edilmesini garantilemeye yardımcı olur.
- Plaka henüz bir satış siparişi satırına atanmamışsa, satış siparişi kaydı ve rezervasyon tamamlandıktan sonra, ambar personeli malzeme çekme işi sırasında bir plaka seçebilir.

### <a name="turn-on-flexible-license-plate-reservation"></a>Esnek plaka rezervasyonunu etkinleştirme

Esnek plaka rezervasyonunu kullanabilmeniz için sisteminizde iki özelliğin etkinleştirilmesi gerekir. Yöneticiler bu özelliklerin durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. Özellikleri aşağıdaki sırada açmanız gerekir:

1. **Özellik adı:** *Esnek ambar düzeyi boyut rezervasyonu*
1. **Özellik adı:** *Esnek sipariş taahhütlü plaka rezervasyonu*

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a>Satış siparişi üzerinde belirli bir plakayı rezerve etme

Bir siparişte plaka rezervasyonunu etkinleştirmek için ilgili öğeyle ilişkilendirilmiş olan hiyerarşi için **Stok rezervasyonu hiyerarşileri** sayfasındaki **Plaka** düzeyi için **Talep üzerine rezervasyona izin ver** onay kutusunu işaretlemeniz gerekir.

![Esnek plaka rezervasyon hiyerarşisi için stok rezervasyonu hiyerarşileri sayfası](media/Flexible-LP-reservation-hierarchy.png)

Plaka rezervasyonunu dağıtımınızdaki herhangi bir noktada, sipariş üzerinde etkinleştirebilirsiniz. Bu değişiklik, değişiklik yapılmadan önce oluşturulan rezervasyonları veya açık ambar işini etkilemez. Ancak, bu rezervasyon hiyerarşisiyle ilişkili bir veya daha fazla kalem için *Siparişte*, *Siparişli rezerve miktar* veya *Fiziksel rezerve miktar* sorun durumuna sahip giden açık stok hareketleri varsa **Talep emrinde rezervasyona izin ver** onay kutusunun işareti kaldırılamaz.

**Plaka** düzeyinde **Talep emrinde rezervasyon izni ver** onay kutusu seçili olsa bile siparişte belirli bir plakanın rezerve edilmesi mümkün *değildir*. Bu durumda, rezervasyon hiyerarşisi için geçerli olan varsayılan ambar operasyonları mantığı geçerlidir.

Belirli bir plakayı rezerve etmek için bir [Açık Veri Protokolü (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) işlemi kullanmanız gerekir. Uygulamada bu rezervasyonu doğrudan bir satış siparişinden, **Excel'de aç** komutunun **Lisans levhası başına sipariş taahhütlü rezervasyon sayısı** seçeneğini kullanarak yapabilirsiniz. Excel eklentilerinde açılan varlık verilerinde, aşağıdaki rezervasyon ile ilgili verileri girmeniz ve sonra verileri Supply Chain Management'a geri göndermek için **Yayımla**'yı seçmeniz gerekir:

- Referans (Yalnızca *Satış siparişi* değeri desteklenir.)
- Sipariş numarası (Değer lotun içinden türetilebilir.)
- Lot kodu
- Plaka
- Miktar

Toplu olarak izlenen bir kalem için belirli bir plakayı rezerve etmeniz gerekiyorsa, [Satış siparişi ayrıntılarını girme](#sales-order-details) bölümünde açıklandığı şekilde **Toplu rezervasyon** sayfasını kullanın.

Sipariş taahhütlü bir plaka rezervasyonu kullanan satış siparişi satırı ambar operasyonları tarafından işlendiğinde, konum yönergeleri kullanılmaz.

Ambar iş maddesi tam palete eşit ve plaka taahhütlü miktarlara sahip satırlardan oluşuyorsa, **Plakaya göre işle** seçeneği *Evet* olarak ayarlanmış bir mobil cihaz menü öğesini kullanarak malzeme çekme işlemini optimize edebilirsiniz. Böylece bir ambar çalışanı, bir işe ait kalemleri tek tek taramak yerine, bir malzeme çekme işlemini tamamlamak için bir plakayı tarayabilir.

![Plakaya göre işle seçeneğinin Evet olarak ayarlandığı mobil cihaz menü öğesi](media/Handle-by-LP-menu-item.png)

**Plakaya göre işle** işlevi, çoklu paletleri kapsayan işleri desteklemediğinden, farklı plakalar için ayrı bir iş maddesi olması daha iyidir. Bu yaklaşımı kullanmak için **Sipariş taahhüttlü plaka kimliği** alanını **İş şablonu** sayfasında ,iş üst bilgisi sonu olarak ekleyin.

> [!NOTE]
> Siparişle taahhüt edilen iş oluşturma işlemi için, malzeme çekme işi satırlarına bir "siparişle taahhüt edilen stok boyutu" değeri atanacaktır ve plaka değerini doğrudan görüntülemek mümkün olmayacaktır. Mobil cihaz menü öğesi ayarlanırken yalnızca *Kullanıcı tarafından yönlendirilen* işlem desteklenir.

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a>Örnek senaryo: Sipariş taahhütlü plaka rezervasyonunu ayarlama ve işleme

Bu senaryoda sipariş taahhütlü plaka rezervasyonunun ayarlanması ve işlenmesi gösterilmektedir.

### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu senaryo, Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerler ve kayıtlarla ilgilidir. Burada sunulan değerleri kullanarak bu senaryoyla çalışmak istiyorsanız demo verilerinin yüklenmiş olduğu bir ortamda çalışmanız gerekir. Ek olarak, başlamadan önce tüzek kişiliği **USMF** olarak ayarlayın.

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a>Plaka rezervasyonuna izin veren bir stok rezervasyonu hiyerarşisi oluşturma

1. **Ambar yönetimi \> Kurulum \> Stok \> Rezervasyon hiyerarşisi**'ne gidin.
1. **Yeni**'yi seçin.
1. **Ad** alanına bir değer girin (örneğin *FlexibleLP*).
1. **Açıklama** alanına bir değer girin (örneğin *Esnek LP rezervasyonu*).
1. **Seçili** listede **Toplu iş numarası**, **Seri numarası** ve **Sahip** seçin.
1. Seçili kayıtları **Kullanılabilir** listesine taşımak için **Kaldır** düğmesini ![geri ok](media/backward-button.png) seçin.
1. **Tamam**'ı seçin.
1. **Plaka** boyut düzeyinin satırında, **Talep emrinde rezervasyona izin ver** onay kutusunu seçin. **Konum** düzeyi otomatik olarak seçilir ve onay kutusunun işaretini kaldıramazsınız.
1. **Kaydet**'i seçin.

### <a name="create-two-released-products"></a>Yayımlanan iki ürün oluşturma

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Yeni yayımlanan ürün** iletişim kutusunda aşağıdaki değerleri ayarlayın:

    - **Ürün numarası:** *Kalem1*
    - **Kalem numarası:** *Kalem1*
    - **Kalem modeli grubu:** *FIFO*
    - **Kalem grubu:** *Ses*
    - **Depolama boyutu grubu:** *Ambar*
    - **İzleme boyutu grubu:** *Yok*
    - **Rezervasyon hiyerarşisi:** *FlexibleLP*

1. Ürün oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni ürün açılır. **Ambar** hızlı sekmesinde, **Birim sıra grubu kodu** alanını *beher* olarak ayarlayın.
1. Aynı ayarlara sahip ikinci bir ürün oluşturmak için önceki adımları yineleyin ancak **ürün numarası** ve **kalem numarası** alanlarını *Kalem2* olarak ayarlayın.
1. Eylem Bölmesinde, **Stoku yönet** sekmesindeki **Görünüm** grubunda, **Eldeki stoku**'u seçin. Ardından **Miktar düzeltmesi**'ni seçin.
1. Yeni kalemlerin eldeki stokunu aşağıdaki tabloda belirtildiği gibi ayarlayın.

    | Madde  | Ambar | Yer | Plaka | Miktar |
    |-------|-----------|----------|---------------|----------|
    | Kalem1 | 24        | FL-010   | LP01          | 10       |
    | Kalem1 | 24        | FL-011   | LP02          | 10       |
    | Kalem2 | 24        | FL-010   | LP01          | 5        |
    | Kalem2 | 24        | FL-011   | LP02          | 5        |

    > [!NOTE]
    > İki plaka oluşturmanız ve *FL-010* ile *FL-011* gibi karışık kalemlere izin veren konumları kullanmanız gerekir.

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a>Satış siparişi oluşturma ve belirli bir plakayı rezerve etme

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *24*

1. **Satış siparişi oluştur** iletişim kutusunu kapatmak ve yeni satış siparişini açmak için **Tamam**'ı seçin.
1. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Kalem numarası:** *Kalem1*
    - **Miktar:** *10*

1. Aşağıdaki ayarlara sahip ikinci bir satış siparişi satırı oluşturun:

    - **Kalem numarası:** *Kalem2*
    - **Miktar:** *5*

1. **Kaydet**'i seçin.
1. **Satır ayrıntıları** hızlı sekmesinde, **Kurulum** sekmesinde her satırın **Lot kodu** değerini not edin. Bu değerler, belirli plakaların rezervasyonu sırasında gereklidir.

    > [!NOTE]
    > Belirli bir plakayı rezerve etmek için **Plaka başına sipariş taahhütlü rezervasyon sayısı** veri varlığını kullanmanız gerekir. Belirli bir plakada toplu olarak izlenen bir kalemi izlemek için [Satış siparişi ayrıntılarını girme](#sales-order-details) bölümünde açıklandığı şekilde **Toplu rezervasyon** sayfasını da kullanabilirsiniz.
    >
    > Plakayı doğrudan satış siparişi satırına girip sistemde onayladıysanız, ambar yönetimi işlemi satır için kullanılmaz.

1. **Microsoft Office'te Aç**'ı ve ardından **Plaka başına sipariş taahhütlü rezervasyon sayısı**'nı seçip dosyayı indirin.
1. İndirilen dosyayı Excel'de açın ve **Düzenlemeyi etkinleştir**'i seçerek Excel eklentisini etkinleştirin.
1. Excel eklentisini ilk kez çalıştırıyorsanız **Bu eklentiyle güven**'i seçin.
1. Oturum açmanız istendiğinde **Oturum aç**'ı seçin ve ardından Supply Chain Management'ta oturum açmak için kullandığınız kimlik bilgilerini kullanarak oturum açın.
1. Belirli bir plakada bir kalemi rezerve etmek için Excel eklentisinde **Yeni**'yi seçerek rezervasyon satırı ekleyin ve sonra aşağıdaki değerleri ayarlayın:

    - **Lot Kodu:** *Kalem1* için satış siparişi satırına yönelik bulduğunuz **Lot Kodu** değerini girin.
    - **Plaka:** *LP02*
    - **ReservedInventoryQuantity:** *10*

1. **Yeni**'yi seçerek başka bir rezervasyon satırı daha ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Lot Kodu:** *Kalem2* için satış siparişi satırına yönelik bulduğunuz **Lot Kodu** değerini girin.
    - **Plaka:** *LP02*
    - **ReservedInventoryQuantity:** *5*

1. Verileri Supply Chain Management'a geri göndermek için Excel eklentisinde **Yayımla**'yı seçin.

    > [!NOTE]
    > Rezervasyon satırı yalnızca, yayımlanma hatasız olarak tamamlanırsa sistemde görüntülenir.

1. Supply Chain Management'a geri dönün. 
1. Kalemin rezervasyonunu gözden geçirmek için **Satış siparişi satırları** hızlı sekmesinde, **Stok** menüsünde **Koru \> Rezervasyon**'u seçin. *Kalem1* satış siparişi satırı için *10* stok rezerve edildiğine ve *Kalem2* satış siparişi satırı için ise *5* stok rezerve edildiğine dikkat edin.
1. Satış siparişi satırı rezervasyonuna ilişkin stok hareketlerini gözden geçirmek için **Satış siparişi satırları** hızlı sekmesinde, **Stok** menüsünde **Görüntüle \> Hareketler**'i seçin. Rezervasyonla ilgili iki hareket olduğuna dikkat edin: **Referans** alanının *Satış Siparişi* olarak ayarlandığı yer ve **Referans** alanının *Sipariş taahhütlü rezervasyon* olarak ayarlandığı yer.

    > [!NOTE]
    > **Referans** alanının *Satış siparişi* olarak ayarlandığı bir hareket, **Konum** düzeyinin üzerindeki stok boyutları (tesis, ambar ve stok durumu) için sipariş satırı rezervasyonunu temsil eder. **Referans** alanının *Sipariş taahhütlü rezervasyon* olarak ayarlandığı bir hareket, belirli bir plaka ve konum için sipariş satırı rezervasyonunu temsil eder.

1. Satış siparişini serbest bırakmak için Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda **Ambara serbest bırak**'ı seçin.

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a>Sipariş taahhütlü plaka atanmış ambar işini gözden geçirme ve işleme

1. **Satış siparişi satırları** hızlı sekmesinde, **Ambar** menüsünde **İş ayrıntıları**'nı seçin.

    Belirli bir toplu iş için rezervasyon yapıldığında, sistem, plaka rezervasyonunu kullanan satış siparişi için işi oluşturduğunda konum yönergelerini kullanmaz. Sipariş taahhütlü rezervasyon, konum da dahil olmak üzere tüm stok boyutlarını belirttiğinden, bu stok boyutları işe girilmiş olduğu için konum yönergelerinin kullanılması gerekmez. Bunlar **İş stok hareketleri** sayfasındaki **Stok boyutlarından** bölümünde gösterilir.

    > [!NOTE]
    > İş oluşturulduktan sonra, **Referans** alanının *Sipariş taahhütlü rezervasyon* olarak ayarlandığı kalem stok hareketi kaldırılır. **Referans** alanının *İş* olarak ayarlandığı stok hareketi, miktarın tüm stok boyutlarında fiziksel rezervasyonu tutar.

1. Mobil cihazda, **Plakaya göre işle** onay kutusunun seçili olduğu bir menü öğesi kullanarak işi çekmeyi ve yerleştirmeyi tamamlayın.

    > [!NOTE]
    > **Plakaya göre işle** işlevi, tüm plakayı işlemenize yardımcı olur. Plakanın bir kısmını işlemeniz gerekiyorsa bu işlevi kullanamazsınız.
    >
    > Her plaka için oluşturulmuş ayrı işinizin olmasını öneririz. Bu sonuca ulaşmak için **İş şablonu** sayfasındaki **İş üst bilgisi sonları** özelliğini kullanın.

    *LP02* plakası, satış siparişi satırları için alınır ve *Baydoor* konumuna yerleştirilir. Bu noktada, yüklenmeye ve müşteriye gönderilmeye hazırdır.

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a>Sipariş taahhütlü toplu iş numaraları olan ambar işinin özel durumunu işleme

Sipariş taahhütlü toplu iş numaralarını toplama için yapılan ambar işi, normal işle aynı standart ambar özel durum işlemeye tabidir. Genel olarak, açık iş veya iş satırı iptal edilebilir, bir kullanıcı yerleşimi dolu olduğu için durdurulabilir ve bir hareket nedeniyle güncelleştirilebilir. Benzer şekilde, zaten tamamlanmış olan çekilmiş iş miktarı azaltılabilir veya işe ters işlem uygulanabilir.

Tüm bu özel durum işleme eylemlerine şu temel kural uygulanır: Müşteri için rezerve edilen parti numarası başka bir toplu iş numarasıyla değiştirilemez ancak depolama boyutları (yerleşim ve plaka) bir kullanıcının el ile yapacağı güncelleştirmeyle ya da sistemin otomatik güncelleştirmesiyle değiştirilebilir. Otomatik güncelleştirme, belirli bir toplu iş otomatik olarak rezerve edildiği ama depolama boyutları belirlenmediği zaman uygulanan aynı rastgele depolama boyutları atamasına dayanır.

### <a name="example-scenario"></a>Örnek senaryo

Bu senaryoya bir örnek, önceden tamamlanan işin seçiminin **Çekilen miktarı düş** işleviyle iptal edildiği durumdur. Bu örnekte, [Örnek senaryo: Toplu iş numarası tahsisatı](#Example-batch-allocation) konusunda açıklanan adımları zaten tamamladığınız varsayılmaktadır. Bu örnekten devam edilir.

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

- Yönerge birimine göre ambalajlama için konteyner konsolidasyon kuralında sınırlamalar vardır. Sipariş taahhütlü rezervasyonlar için, **Yönerge birimine gör ambalajla** alanının etkinleştirildiği konteyner yapı şablonlarını kullanmamanızı öneririz. Geçerli tasarımda, ambar işi oluşturulurken yerleşim yönergeleri kullanılmaz. Bu nedenle, konteyner kullanımı dalga adımı sırasında yalnızca birim sıra grubundaki en küçük birim uygulanır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]