---
title: Ambar işi için mobil cihazları ayarlama
description: Bu konuda, ambar çalışanlarının bir mobil cihazda iş gerçekleştirmek için kullandığı menü öğelerinin nasıl konfigüre edileceği açıklanmaktadır.
author: MarkusFogelberg
manager: tfehr
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFSysDirSort, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bb256514175166621847a5d40c16b9b749b1ddc
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016206"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a>Ambar işi için mobil cihazları ayarlama

[!include [banner](../includes/banner.md)]

Bu konuda, ambar çalışanlarının bir mobil cihazda iş gerçekleştirmek için kullandığı menü öğelerinin nasıl konfigüre edileceği açıklanmaktadır.

> [!NOTE]
> Bu konu, Ambar yönetimindeki özellikler için geçerlidir. Stok yönetimindeki özellikler için geçerli değildir. Bir ambar mobil cihazında görülen menü öğeleri, **Mobil cihaz menü öğeleri** sayfasında yapılandırılır. Menü öğeleri farklı menülere konabileceğinden, menü yapılarını yalnızca belirli iş türleri belirli kurallara maruz kalacak şekilde yapılandırmak kolaydır. Menü öğelerini aşağıdaki görevleri gerçekleştirecek şekilde yapılandırabilirsiniz:

- Bir sorgu işleyin veya etiket yazdırma, plaka numarası oluşturma, üretim emrini başlatma ya da bir konumdaki maddeler hakkındaki bilgilere hızlıca bakma gibi bir etkinlik gerçekleştirin.
- Başka bir süreç üzerinden gerçekleştirilecek bir iş oluşturun. Örneğin, bir satınalma emrine yönelik bir madde almak, başka bir çalışan için yerine koyma işi oluşturabilir.
- Bir satınalma emrine yönelik bir madde alındığında oluşturulan yerine koyma işi gibi, başka bir süreç tarafından oluşturulmuş (mevcut iş) işi gerçekleştirin.

Bir etkinlik veya sorgulama için bir menü öğesi oluşturmak için, **Mod** alanını **Dolaylı** olarak ayarlayın. **Etkinlik kodu** seçeneklerinin listesi etkin hale gelir, böylece menü öğesinin hangi sorgu ve etkinlik türünü seçebilirsiniz. Ambarlama işi oluşturma için bir menü öğesi oluşturabilmek için **Mod** alanını **İş** olarak ayarlayın. **İş oluşturma işlemi** seçeneklerinin bir listesi kullanılabilir hale gelir. Mevcut ambar işini işlemek üzere bir menü öğesi oluşturmak için, **Mod** alanını **İş** olarak ayarlayın ve ardından **Mevcut işi kullan** seçeneğini **Evet** olarak ayarlayın. 

> [!NOTE]
> Ek alanlar, menü öğesi için seçtiğiniz moda ve menü öğesinin var olan işi gerçekleştirmek için kullanılıp kullanılmayacağına bağlı olarak menü öğeleri için kullanılabilir olabilir. Ek alan seçimleri hakkında daha fazla bilgi için, bu konunun ilerleyen noktalarındaki "Ek menü maddesi seçenekleri" bölümüne bakınız.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Etkinlik ve sorgular için menü öğeleri yapılandırma
Bir menü öğesine yönelik **Mod** alanı **Dolaylı** olarak ayarlı ise, iş oluşturmayan bir genel etkinlik veya sorgu gerçekleştirmek için bir menü öğesi oluşturabilirsiniz. Plaka etiketlerini yeniden yazdırmak ve bir konumdaki maddeler hakkında sorgu yapmak örnekler arasındadır. Aşağıdaki tabloda, kullanılabilecek seçenekler listelenmiştir.

| Seçenek | Açıklama |
|---|---|
| Yok | Bu varsayılan değer, bir etkinlik veya sorgu etkinleştirmez. |
| Hakkında | Sistem hakkında, sürüm numarası, ambar kodu ve şu anda oturum açmış olan çalışan gibi bilgileri görüntüleyin. |
| Ambarı değiştir | Çalışanın oturum açmış olduğu ambarı değiştirin. |
| Yerleşim sorgusu | Bir konuma yönelik tüm maddeler ve miktarlar hakkındaki bilgileri görüntüleyin. |
| Plaka sorgusu | Bir plakadaki madde miktarını ve plakanın konumunu görüntüleyin. |
| Üretim emrini başlat | Bir üretim emri başlatın. |
| Üretim ıskartası | Her üretim reçetesi satırı için üretimi sırasında oluşturulan hurda miktarını girin. |
| Üretimdeki son palet | Son madde paletinin, bir üretim emrine yönelik olarak üretildiğini ve üretim emrinin durumunun **Tamamlandığı bildirildi** olarak güncellenmesi gerektiğini belirtin. Üretim sırasında tüketilmemiş olan hammaddelerin durumu **Malzeme çekildi** 'den tekrar **Siparişte** olarak değişir ve maddeler stoka geri iade edilebilir. |
| Madde sorgusu | Ambarda nerede olduğunu belirlemek için bir maddeyi taratın. Sorgu taranan maddeye yönelik tüm konum ve miktarları döndürür. |
| Etiketi yeniden yazdır | Plaka etiketini yeniden yazdırın. |
| Plaka yapısı | Aynı konumdaki birden fazla plakayı birleştirerek bir ana plaka oluşturun. Bu seçenek, birden fazla plakayı aynı anda taşırsanız kullanışlıdır. Üst plaka taşındıktan sonra, her bir plakadan maddeler almadan önce bir plaka bölme gerçekleştirmeniz gerekir. <p></p>**İpucu:** Bir üst plakayı taşımak için, hareketlere yönelik çalıştırma oluşturmak için yapılandırılmış bir mobil cihaz kullanmanız gerekir. |
| Plaka bölme | Birleştirilen plakalardaki maddeleri alabilmek için birleştirilen plakayı bölün. |
| Sürücü girişi | Taşıma yönetimi kullanıyorsanız, sürücünün ulaştığı saati giden yük kimliğini, atama kodunu veya sevkıyat kodunu tarayarak kaydedin. Bu seçenek için, atamaya yük atanması ve yükün durumunun **Yüklü** olması gerekir. |
| Sürücü çıkışı | Sürücünün atamasını tamamladığını kayda geçirin. |
| Numara serisi önbelleğini temizle | Numara serisi numaralarını numara serisi önbelleğinden silin. Bu etkinlik genellikle mobil cihazlar kullanıldığında önbelleğe alma sorunları çözmek için bir sistem yöneticisi tarafından gerçekleştirilir. |
| Toplu iş değerlendirmesini değiştir | Bir çalışanın bir madde veya toplu iş için bir toplu iş değerlendirme kodu belirlemesine izin verin. Bu seçim, toplu iş için belirtilen değerlendirme kodunu günceller. |
| Açık iş listesini görüntüle | Belirli bir kullanıcı için kullanılabilir iş listesini gösterir. Kullanıcı bunun ardından gerçekleştirilecek işi seçebilir ve ona yönlendirilir. Bu liste, 7 inç veya daha geniş ekran boyutuna sahip tablet cihazlarda görüntülenmek üzere hazırlanmıştır. Bu seçeneği belirlediğinizde, **Sorguyu düzenle** ve **Alan listesi** menü öğeleri kullanılabilir olur. **Sorguyu düzenle** sayfası, listede görünen iş için ölçütleri ayarlamanıza imkan verir. **Alan listesi** sayfası, iş listesinde görüntülenecek alanları seçmenize olanak sağlar. Örneğin, görüntülenen alanların sayısını, kullanıcının en uygun iş öğesini daha hızlı seçebileceği şekilde azaltabilirsiniz. **Genel** FastTab'inde, **Sayfa başına kayıt** alanında, sayfa başına kaç iş kaydı gösterileceğini de seçebilirsiniz. **Kullanıcıların işi hareket türüne göre filtrelemesine izin ver** seçeneği belirlendiğinde, iş listesi, kullanıcının hareket türüne göre filtre kullanabileceği bir **İşi filtrele** denetimi içerecektir. İş listesinde, kullanıcılar yalnızca erişim iznine sahip oldukları işi görür. Kullanıcıların, erişebilmeleri gereken belirli iş sınıfı türlerini destekleyen kullanıcı yönlendirmeli bir veya daha fazla menü öğesi için izni olduğundan emin olmanız gerekir. İzinler, kullanıcı listeden iş yapmaya çalıştığında doğrulanır.|
| Plakadan transfer emri oluştur | Ambar çalışanlarının doğrudan ambar uygulamasından transfer emirleri oluşturmasına ve işlemesine olanak tanır. Ambar çalışanları, hedef ambarı seçerek başlar ve uygulamayı kullanarak bir veya daha fazla plaka tarayabilir. Ambar çalışanı **Siparişi tamamla** 'yı seçtiğinde, bir toplu iş bu plakalar için kaydedilen eldeki stoğu temel alan gerekli transfer emri ve sipariş satırlarını oluşturur. Daha fazla bilgi için, bkz. [Ambar uygulamasından transfer emri oluşturma](create-transfer-order-from-warehouse-app.md)


## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Başka bir iş veya sürece yönelik iş oluşturmak için menü öğelerini yapılandırma
İlk eylem mobil cihazda gerçekleştirildikten sonra, başka bir çalışan için iş oluşturan bir menü öğesi ayarlayabilirsiniz. Örneğin, bir çalışan bir mobil cihaz kullanarak bir madde aldığında, başka bir çalışan için yerine koyma işi oluşturulur. İş oluşturan bir menü öğesi ayarlamak için, **Mobil cihaz menü öğeleri** sayfasında, **Mod** alanında **İş** öğesini seçin. Aşağıdaki tabloda, **İş oluşturma süreci** alanındaki seçenekler iş emri türüne göre düzenlenir.


<table>
<tbody>
<tr>
<th>İş siparişi türü</th>
<th>Seçenek</th>
<th>Açıklama</th>
</tr>
<tr>
<td rowspan="8">Satın alma siparişi</td>
<td>Satınalma siparişi satırı teslim alma</td>
<td>Belirli bir miktarda madde girişini, satınalma emri numarası ve satınalma emri satır numarasını kullanarak kayda geçirin ve başka bir çalışan için yerine koyma işi oluşturun.</td>
</tr>
<tr>
<td>Satınalma siparişi satırı teslim alma ve yerine koyma</td>
<td>Belirli bir miktarda maddenin girişini, satınalma emri numarasını veya satınalma emri satır numarasını kullanarak kayda geçirin ve maddeleri yerine koyun. Aynı çalışan iki eylemi de gerçekleştirir.</td>
</tr>
<tr>
<td>Satınalma siparişi madde teslim alma</td>
<td>Bir satınalma emri için belirli bir miktarda maddenin girişini, satınalma emri numarasını ve madde numarasını kayda geçirerek kaydedin ve başka bir çalışan için yerine koyma işi oluşturun.</td>
</tr>
<tr>
<td>Satınalma siparişi maddesini teslim alma ve yerine koyma</td>
<td>Bir satınalma emri için belirli bir miktarda maddenin girişini, satınalma emri numarasını kaydederek kayda geçirin ve maddeyi yerine koyun. Aynı çalışan iki eylemi de gerçekleştirir.</td>
</tr>
<tr>
<td>Plaka teslim alma</td>
<td>Plaka kodunu kullanarak gelen ön sevkiyat bildirimini (ÖSB) alın.</td>
</tr>
<tr>
<td>Plaka alma ve yerine koyma</td>
<td>Plaka kodunu kullanarak gelen ön sevkiyat bildirimini (ÖSB) alın ve yerine koyun.</td>
</tr>
<tr>
<td>Yük maddesi teslim alma</td>
<td>Bir yük için miktar girişini yük kodunu kullanarak kaydedin ve başka bir çalışan için yerine koyma işi oluşturun. Madde numarası ve ürün boyutları, girişi satınalma emri satırlarına eşleştirir.</td>
</tr>
<tr>
<td>Yük maddesi teslim alma ve yerine koyma</td>
<td>Yükün girişini yük kodunu kullanarak kaydedin ve maddeleri yerine koyun. Madde numarası ve ürün boyutları, girişi satınalma emri satırlarına eşleştirir. Aynı çalışan iki eylemi de gerçekleştirir.</td>
</tr>
<tr>
<td rowspan="2">Siparişi iade et</td>
<td>İade emri alma</td>
<td>Belirli bir miktardaki madde girişini, RMA numarasını kaydederek kayda geçirin ve başka bir çalışan için yerine koyma işi oluşturun.</td>
</tr>
<tr>
<td>İade emri teslim alma ve yerine koyma</td>
<td>Belirli bir miktardaki madde girişini, RMA numarasını kaydederek kayda geçirin ve maddeleri yerine koyun. Aynı çalışan iki eylemi de gerçekleştirir.</td>
</tr>
<tr>
<td rowspan="6">Transfer emri</td>
<td>Transfer emri madde teslim alma</td>
<td>Belirli bir miktardaki madde girişini kayda geçirin ve başka bir çalışan için yerine koyma işi oluşturun.

<strong>Not:</strong> Bu seçeneği, yalnızca maddeler ambar yönetimi süreçlerinin etkinleştirilmediği bir ambardan sevk edildiyse kullanın.</td>
</tr>
<tr>
<td>Transfer emri maddesini teslim alma ve yerine koyma</td>
<td>Belirli bir miktardaki madde girişini kayda geçirin ve maddeleri yerine koyun. Aynı çalışan iki eylemi de gerçekleştirir.

<strong>Not:</strong> Bu seçeneği, yalnızca maddeler ambar yönetimi süreçlerinin etkinleştirilmediği bir ambardan sevk edildiyse kullanın.</td>
</tr>
<tr>
<td>Transfer emri satırı teslim alma</td>
<td>Belirli bir miktardaki madde girişini kayda geçirin ve başka bir çalışan için yerine koyma işi oluşturun.</td>
</tr>
<tr>
<td>Transfer emri satırı teslim alma ve yerine koyma</td>
<td>Belirli bir miktardaki madde girişini kayda geçirin ve maddeleri yerine koyun. Aynı çalışan iki eylemi de gerçekleştirir.</td>
</tr>
<tr>
<td>Plaka teslim alma</td>
<td>Plaka kodunu kullanarak gelen ön sevkiyat bildirimini (ÖSB) alın.</td>
</tr>
<tr>
<td>Plaka alma ve yerine koyma</td>
<td>Plaka kodunu kullanarak gelen ön sevkiyat bildirimini (ÖSB) alın ve yerine koyun.</td>
</tr>
<tr>
<td rowspan="4">Üretim</td>
<td>Tamamlandı bildirimi</td>
<td>Bir üretim için bitmiş olan bitmiş bir maddenin miktarını kayda geçirin ve başka bir çalışan için yerine koyma işi oluşturun. Miktar, üretim için planlanan miktarın tümü veya bir kısmı olabilir.</td>
</tr>
<tr>
<td>Tamamlandı olarak rapor et ve yerine koy</td>
<td>Bir üretim için bitmiş olan bitmiş bir maddenin miktarını kayda geçirin ve maddeleri yerine koyun. Miktar, üretim için planlanan miktarın tümü veya bir kısmı olabilir. Aynı çalışan iki eylemi de gerçekleştirir.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Kanban'ın tamamlandığını belirtin ve başka bir çalışan için yerine koyma işi oluşturun.</td>
</tr>
<tr>
<td>Kanban yerine koyma</td>
<td>Bir kanban'ın tamamlandığını belirtin ve maddeleri yerine koyun. Aynı çalışan iki eylemi de gerçekleştirir.</td>
</tr>
<tr>
<td rowspan="5">Stok</td>
<td>Hareket</td>
<td>Maddelerin bir konumdan diğerine taşındığını kayda geçirin. Çalışan maddelerin hangi konumdan hangi konuma taşındığını belirtir.</td>
</tr>
<tr>
<td>Karantina</td>
<td>Bir plaka veya konum için eldeki stokun durumunu, hasarlı veya eksik stok maddelerini kullanılamaz kılacak şekilde değiştirin.</td>
</tr>
<tr>
<td>Şablonla hareket</td>
<td>Maddeleri bir konumdan diğerine yarı otomatik bir şekilde taşıyın. İşçi, maddelerin taşınacağı konumu seçer ve sistem maddelerin nereye taşınacağını belirlemek için yerleşim yönergesini kullanır.</td>
</tr>
<tr>
<td>Ambar transferi</td>
<td>Bir ambardan diğerine transfer edilmiş maddeleri kayda geçirin. Bu seçenek, çalışanın iki ambarda da çalışmasına izin verilmesini gerektirir.

<strong>Not:</strong> Bu menü öğesi, <strong>Fiş denetleme</strong> alanının <strong>Deftere nakil</strong> olarak ayarlandığı varsayılan bir stok transfer günlüğü gerektirir.</td>
</tr>
<tr>
<td>Plaka yükleme</td>
<td>Ambarınızı ilk kez ayarlarken bu seçeneği kullanın. Ambardaki tüm konumlarda bulunan tüm plakaları taratın. Konumlar plaka kontrollü olmalıdır. <strong>Seri numarası</strong> veya <strong>Toplu iş numarası</strong>, stok rezervasyon hiyerarşisinde <strong>Konum</strong> üzerinde listeleniyorsa bu seçeneği kullanamazsınız.</td>
</tr>
<tr>
<td rowspan="3">Döngü sayımı</td>
<td>Ayarlama etkin</td>
<td>Stoktaki madde miktarını artırın. Konum, plaka, madde, miktar, ölçü birimi ve durumu belirtin.</td>
</tr>
<tr>
<td>Ayarlama devre dışı</td>
<td>Stoktaki madde miktarını azaltın. Konum, plaka, madde, miktar, ölçü birimi ve stokun durumunu belirtin.</td>
</tr>
<tr>
<td>Nokta döngü sayımı</td>
<td>Bir konum için sayım başlatın. Çalışan, konumdaki tüm maddelerin sayımını yapmalıdır. Sayımın sonucu beklenen miktardan az olduğunda, eksik miktar kayıp sayılır.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Mevcut işi işlemek için menü öğeleri yapılandırma
Ambar işi oluşturmak için menü öğeleri ayarlamaya ek olarak, önceden oluşturulmuş işi işlemek için menü öğeleri de ayarlayabilirsiniz. **Mod** alanını **İş** olarak ayarlayın ve **Geçerli işi kullan** seçeneğini belirleyin. Bunun ardından **Genel** sekmesinde bazı ek seçenekler kullanılabilir hale gelir. Menü öğesine erişimi **İş sınıfı** FastTab'i üzerinde bir veya daha fazla iş sınıfı atayarak kontrol edebilirsiniz. İş sınıfları, menü öğesinin işleyebileceği işi tanımlar. İş sınıfı aynı zamanda belirli kullanıcı rollerine erişim vermek veya farklı operasyon türleri için işlemeyi ayırmak üzere de kullanılabilir. Aşağıdaki tabloda, kullanılabilecek seçenekler açıklanmıştır. Seçenek **Mobil cihaz menü öğeleri** sayfasında **Tarafından yönlendirilen** alanında seçilebilir. 

<table>




<thead>
<tr class="header">
<th>Seçenek</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hiçbiri</td>
<td>Bu varsayılan değer iş işlemez.</td>
</tr>
<tr class="even">
<td>Sistem yönlendirmesinde</td>
<td>Supply Chain Management denetimleri, bir çalışana atanan iş türlerini ve çalışanın işi gerçekleştirdiği sıralamayı denetler. Bu seçeneği belirlediğinizde, iş için sıralama ölçütünü ayarlayabileceğiniz <strong>Sistem tarafından yönlendirilen sıralama düzeni</strong> sayfasını açmak için Eylem Bölmesi'nde <strong>Sistem tarafından yönlendirilen çalışma</strong> seçeneğine belirleyebilirsiniz. Bu sıralama kriteri, çalışanın işi hangi sırada yapacağını denetler. İhtiyaç duyduğunuz sayıda ölçüt ekleyebilirsiniz.</td>
</tr>
<tr class="odd">
<td>Kullanıcı yönlendirmesinde</td>
<td>Çalışan gerçekleştirilecek işi ve hangi sırada gerçekleştireceğini seçer.</td>
</tr>
<tr class="even">
<td>Kullanıcı gruplandırma</td>
<td>Çalışan işi el ile gruplandırır. Bu seçenek, örneğin bir çalışan bir konumdan aynı anda birden fazla maddeyi çekebildiği zaman faydalıdır. Bir çalışan gereken tüm maddeleri çekmeyi tamamladıktan sonra, maddeleri yerine koyabilir.</td>
</tr>
<tr class="odd">
<td>Sistem gruplandırma</td>
<td>Supply Chain Management, belirli bir alana dayalı olarak işi işçi için gruplandırır. Örneğin, bir çalışanın bir sevkıyat kodu, yük kodu veya her bir iş birimine bağlanabilecek herhangi bir değer taradığında çekme işi gruplanır. Bu seçeneği belirlemeniz halinde, aşağıdaki alanlar gereklidir:
<ul>
<li><strong>Sistem gruplandırma alanı</strong> – Çalışanın işi gruplandırmak için tarayacağı alanı seçin.</li>
<li><strong>Sistem gruplandırma etiketi</strong> – Çalışana işi gruplandırmak için ne taraması gerektiğini bildiren metni girin.</li>
</ul></td>
</tr>
<tr class="even">
<td>Doğrulanmış kullanıcının yönlendirmesinde</td>
<td>Çalışan, iş yük veya sevkıyat gibi daha büyük bir varlıkla ilişkiliyken gerçekleştirilecek işi seçer. Çalışan, öğelerin çekileceği sıraları belirler. Bu seçeneği belirlemeniz halinde, aşağıdaki alanlar gereklidir:
<ul>
<li><strong>Doğrulanmış kullanıcı yönlendirmesindeki alan</strong> – Çalışanın işi gruplandırmak için tarayacağı alanı seçin.</li>
<li><strong>Doğrulanmış kullanıcı yönlendirmesindeki etiket</strong> – Çalışana çekme işi sistem tarafından gruplandığında ne tarayacağını bildiren metni girin.</li>
</ul>
Bu seçenek örneğin bir yük için birden fazla palet hazırlandıysa faydalıdır. <strong>Doğrulanmış Kullanıcı Yönlendirmesinde</strong> alanında <strong>LoadId</strong> seçmeniz halinde, çalışan yükle ilişkili herhangi bir paleti çekebilir. Çalışan, yükle ilişkilendirilmemiş bir maddeyi taradığında hata iletisi alır.</td>
</tr>
<tr class="odd">
<td>Küme malzeme çekme</td>
<td>Çalışan işi kümeler halinde gruplandırır. Kümeler, çalışanların tek bir konumdan maddeleri birden fazla iş emri için aynı anda çekmesine imkan verir.</td>
</tr>
<tr class="even">
<td>Döngü sayımı gruplandırma</td>
<td>İşçi, bir bölge, iş havuzu veya konum seçer ve Supply Chain Management seçime bağlı olarak işi atar. Bu seçeneği belirlemeniz halinde, Eylem Bölmesi'nde <strong>Döngü sayımı</strong> seçeneğine tıklayarak görüntülenecek ek bilgileri belirtebilir ve ayrıca çalışanın fark bulunması halinde sayımı kaç kez tekrarlaması gerektiğini de belirtebilirsiniz.</td>
</tr>
 <tr class="odd">
<td>Taşıma yüklemesi</td>
<td>Bu özellik, birden fazla ambar çalışanının, tam olarak veya kısmen nakledilmiş yüklere sahip envanteri aynı veya farklı yüklerden aynı kamyona yüklemesine olanak tanır.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Ek menü öğesi seçenekleri
Ek menü öğeleri seçenekleri **Mobil cihaz menü öğeleri** sayfasında bulunabilir. Seçenekler, menü öğesini yapılandırdığınız sürece bağlı olarak değişiklik gösterir. 

Aşağıdaki tablo bu seçenekleri açıklar.

<table>




<thead>
<tr class="header">
<th>Alan</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>İşin bölünmesine izin ver</td>
<td>Kullanıcıların iş emri için maddeleri birden fazla hedef plakaya koymasına izin vermek için bu seçeneği seçin. Bu seçenek örneğin, bir hedef plaka dolu olduğunda ve çalışanın diğer maddeler için başka bir plaka eklemesi gerektiğinde yararlıdır. Çalışan plakanın dolduğunu belirtmek ve bunun için çekme işi almayı durdurmak için <strong>Dolu</strong>'yu seçebilir. Çekilen maddeleri için yrine koyma konumu görüntülenir ve tamamlanmış olan çekme işi yeni bir iş emrine taşınır. Hedef plaka için kalan çekme işi orijinal iş sırasında durur.</td>
</tr>
<tr class="even">
<td>Bağlama</td>
<td>Çalışanların önerilen hazırlama veya yükleme konumunu geçersiz kılan bir konum belirtmelerine izin vermek için bu seçeneği seçin. Kalan tüm yerine koyma işi yeni konuma yönlendirilir. Bu seçenek örneğin, bir çalışanın sipariş 1 için Nokta 1'in hazırlık konumunda maddeleri yerine koyması gerekiyorsa ancak önceki yük konumdan kaldırılmadığı için bunu yapamıyorsa kullanışlıdır. Dock 1 hazırlama konumunun kullanılır olmasını beklemek yerine, çalışan Dock 2 için hazırlama konumunu kullanmaya karar verebilir. Bu durumda, çalışan önerilen hazırlama konumunu geçersiz kılar. Bunun ardından iş emri için kalan tüm maddelerin yerine koyma konumu Nokta 2 hazırlama konumu olarak güncelleştirilir. Bu seçeneği belirlerseniz, <strong>Bağlayan</strong> alanını ayarlamanız gerekir.</td>
</tr>
<tr class="odd">
<td>Bağlayan</td>
<td>Bağlama kullanıyorsanız, sevkiyatla mı yoksa yükle mi bağlayacağınızı belirtmeniz gerekir.</td>
</tr>
<tr class="even">
<td>Denetim şablonu kodu</td>
<td>Başka bir işlemin yapılabilmesi için bu menü öğesinin iş sürecini kesintiye uğratacak iş denetimi şablonunu seçin. Örneğin, bu menü öğesi gelen iş içinse, denetim şablonu çalışanın teslimat konteynerindeki sıcaklığı denetlemesini gerektirebilir. İşlemin kesintiye uğradığı nokta, denetim şablonu üzerinde belirtilir. Bu noktada, örneğin, iş başladığında veya tamamlandığında ya da durumu değiştiğinde olabilir.</td>
</tr>
<tr class="odd">
<td>Küme profili kodu</td>
<td>Küme çekme için kullanılacak küme profilini seçin. Küme profili, kümelerin otomatik oluşturup oluşturulmayacağı, atanabilecekleri pozisyonların isimleri ve iş birimlerinin sayısı, kümelerin tek tek birimlere ne zaman ayrılacağı ve doğrulama gerekip gerekmediği gibi ayarları içerir. Bu alan yalnızca <strong>Yöneten</strong> alanında <strong>Küme çekme</strong> seçili ise kullanılabilir.</td>
</tr>
<tr class="even">
<td>Önce toplammadde miktarını say</td>
<td>Çalışanın sayım sırasında önce toplam miktarı sayması gerekiyorsa bu seçeneği seçin. Bir fark bulunursa çalışan, plaka numarası, toplu iş numarası, seri numarası gibi ek bilgileri sağlamalıdır.</td>
</tr>
<tr class="odd">
<td>Hareket oluştur</td>
<td>Bir çalışanın, işi hemen gerçekleştirmesini gerektirmeksizin bir hareket için iş oluşturmasına izin vermek üzere bu seçeneği belirleyin. Bu seçenek örneğin, bir kalite incelemesi tamamlanmışsa ve denetçi maddenin kalite inceleme alanından taşınmasını istiyorsa kullanışlıdır.</td>
</tr>
<tr class="even">
<td>Yönerge kodu</td>
<td>Belirli bir konum yönergesini kullanmak için konum yönergesiyle ilişkili olan yönerge kodunu seçin. İş oluşturduğunuzda ve iş oluşturma işlemi <strong>Şablonla hareket</strong> olduğunda bu alan kullanılabilir.</td>
</tr>
<tr class="odd">
<td>Döngü sayımı eşiklerini devre dışı bırak</td>
<td>Döngü sayımı eşiklerini yoksaymak için bu seçeneği belirleyin. Bu seçeneği belirlerseniz, döngü sayımı işi eşik değerler aşıldığında oluşturulmaz.</td>
</tr>
<tr class="even">
<td>Toplu iş değerlendirme kodunu görüntüle</td>
<td>Toplu iş değerlendirme kodlarını görüntülemek için bu seçeneği seçin. Örneğin, iade toplu iş aldığınızda, toplu iş değerlendirme kodlarını görüntüleyebilirsiniz. Çalışanlar, toplu işin durumunu ve kalitesini değerlendirip uygun kodu seçebilir. Toplu iş değerlendirme kodundaki kurallar toplu işin diğer ambar süreçlerinde kullanılıp kullanılamayacağını belirler. Bu seçeneği belirlemezseniz, aşağıdaki toplu iş değerlendirme kodlarından biri kullanılır:
<ul>
<li>Yeni bir toplu iş numarası alırsanız, madde model grubunda belirtilen varsayılan toplu iş değerlendirme kodu.</li>
<li>Toplu iş için önceden atanmış olan toplu iş değerlendirme kodu.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Değerlendirme kodunu görüntüle</td>
<td>Değerlendirme kodlarını görüntülemek için bu seçeneği belirleyin. Örneğin, iade maddeler aldığınızda, değerlendirme kodlarını görüntüleyebilirsiniz. Çalışanlar, maddelerin durumunu ve kalitesini değerlendirip uygun kodu seçebilir. Değerlendirme kodundaki kurallar ürünlerin diğer ambar süreçlerinde kullanılıp kullanılamayacağını belirler.</td>
</tr>
<tr class="even">
<td>Stok durumunu görüntüle</td>
<td>Stoktaki maddelerin durumunu görüntülemek için bu seçeneği belirleyin. Bu seçenek, döngü sayımı haricinde geçerli işi kullanan tüm menü öğeleri için kullanılabilir.</td>
</tr>
<tr class="odd">
<td>Çekme ekranının özetini görüntüle</td>
<td>Seçilen iş emrine yönelik çekme işinin özetini görüntülemek için bu seçeneği belirleyin. İş emri için ilk iş satırı işlenene dek özet görüntülenir.</td>
</tr>
<tr class="even">
<td>Plaka oluştur</td>
<td>Numara sırası seçimini temel alan benzersiz bir plaka numarası üretmek için bu seçeneği kullanın. Örneğin, satınalma emirleri için alınan maddelere yönelik bir plaka numarası üretebilirsiniz.</td>
</tr>
<tr class="odd">
<td>Grup yerine koyma</td>
<td>Yerine koyma işini gruplandırmak için bu seçeneği belirleyin. Bu seçenek, iş ya işçi ya da Supply Chain Management tarafından gruplandığında kullanılabilir. Çalışan gruptaki tüm çekme işini bitirdiğinde, aynı grup için yerine koyma işi oluşturulur.</td>
</tr>
<tr class="even">
<td>Stok düzeltmesi türleri</td>
<td>Ayarı nakletmek ve rezervasyonları kaldırmak için kullanılan stok sayım günlüğünü belirleyen stok ayar türünü seçin. Bu alan yalnızca <strong>Ayarlama etkin</strong> veya <strong>Ayarlama devre dışı</strong> çalışma oluşturma süreci için kullanılabilir.</td>
</tr>
<tr class="odd">
<td>Toplu iş numarasını geçersiz kıl</td>
<td>Bir üretim emri için bir miktarı bitmiş olarak raporlayan çalışanların, üretim emrine atanan toplu iş numarasından başka bir toplu iş numarasını girmesine izin vermek üzere bu seçeneği belirleyin.</td>
</tr>
<tr class="even">
<td>Hedef plakayı geçersiz kıl</td>
<td>Çalışanların önerilen hedef plakadan farklı bir hedef plakasının numarası belirtmesine izin vermek için bu seçeneği seçin. Bir iş emri için ilk çekme plakadaki tüm madde miktarı için olduğunda bu seçeneği kullanın. Bu seçenek örneğin bir paleti yeniden kullanırken kullanışlıdır.</td>
</tr>
<tr class="odd">
<td>Çek ve paketle</td>
<td>Çalışanların bir satış siparişi işini veya yükü tek bir iş biriminde birleştirmesine izin vermek için bu seçeneği seçin. Bir çalışan yalnızca satış siparişi veya yük için iş gerçekleştirebilir. Bu seçenek örneğin satış siparişi için yükleme, sevkıyat ve iş oluşturulduktan sonra satış siparişi için miktarı artırmanız gerektiğinde kullanışlıdır. Bu seçenek, menü maddesi mevcut işi kullandığında ve iş kullanıcı veya sistem tarafından yönlendirildiğinde kullanılabilir.</td>
</tr>
<tr class="even">
<td>En eski toplu işi çek</td>
<td>Çalışanın konumdaki en eski toplu işi ilk çekip çekmemesi gerektiğini belirtin. Aşağıdaki seçenekler bulunur:
<ul>
<li><strong>Yok</strong> – Çalışan konumdaki herhangi bir toplu işi çekebilir. Çalışan ileti almaz.</li>
<li><strong>Uyarı</strong> – Çalışan konumdaki herhangi bir toplu işi çekebilir fakat toplu iş en eski toplu iş değilse bir uyarı iletisi alır.</li>
<li><strong>Zorla</strong> – Çalışan konumdaki en eski toplu işi çekmelidir. Çalışan toplu iş en eski toplu iş değilse bir hata iletisi alır. <strong>Not:</strong> Bu seçenek yalnızca <strong>Toplu iş numarası</strong> maddeye atanan rezervasyon hiyerarşisindeki <strong>Konum</strong>'dan daha düşükse geçerlidir.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Etiket yazdır</td>
<td>Çalışanların plaka etiketlerini yazdırmasına izin vermek için bu seçeneği belirleyin.</td>
</tr>
<tr class="even">
<td>Sistem gruplandırma alanı</td>
<td>Supply Chain Management'ın işçiler için çekme işini nasıl gruplayacağını belirlemek için alanı seçin. Örneğin, <strong>ShipmentId</strong> alanını seçerseniz çalışan çekme işini gruplandırmak için sevkıyat kodunu tarayacaktır. Böylece sevkıyat için tüm iş çalışana atanır. Bu alan, sistem tarafından gruplanan mevcut işi kullanmak için bir menü öğesi oluşturmanızı gerektirir. Çalışana ne tarayacağını bildirmek için <strong>Sistem gruplandırma etiketi</strong> alanına metin girmeniz de gerekir.</td>
</tr>
<tr class="odd">
<td>Sistem gruplandırma etiketi</td>
<td>Çekme işi Supply Chain Management tarafından gruplandığında işçinin ne tarayacağını bildiren metni girin. Örneğin çekme işini sevkiyata göre gruplandırmak için <strong>ShipmentId</strong> alanını kullanıyorsanız alana <strong>Sevkıyat kodu</strong> girebilirsiniz. Bu alan, sistem tarafından gruplanan mevcut işi kullanmak için bir menü öğesi oluşturmanızı gerektirir. <strong>Sistem gruplandırma</strong> alanında alanı nasıl gruplandıracağınızı da seçmelisiniz.</td>
</tr>
<tr class="even">
<td>Varsayılan verileri kullan</td>
<td>Eylem Bölmesi'nde, çalışanın günlük işlerinde genellikle ihtiyaç duyduğu verileri görüntüleyecek alanları seçebildiğiniz <strong>Varsayılan veri</strong> tuşunu etkinleştirmek için bu seçeneği belirleyin. Örneğin bu seçenek, çalışan genellikle aynı konumdan maddeleri çekiyorsa yararlıdır. Konumu varsayılan olarak görüntülemek için <strong>Gönderen konum</strong> alanını seçebilirsiniz.</td>
</tr>
<tr class="odd">
<td>Doğrulanmış Kullanıcı Yönlendirmesindeki Alan</td>
<td>Çalışanın işi gruplamak için tarayacağı alanı seçin. Örneğin, <strong>LoadId</strong>'yi seçerseniz, çalışan seçilen bir işle ilişkili tüm işleri çekebilir. Çalışana ne tarayacağını bildirmek için <strong>Doğrulanmış Kullanıcı Yönlendirmesindeki Etiket</strong> alanına metin girmeniz de gerekir.</td>
</tr>
<tr class="even">
<td>Doğrulanmış Kullanıcı Yönlendirmesindeki Etiket</td>
<td>Çalışana çekme işi doğrulanmış kullanıcı yönlendirmesindeki bir alan tarafından gruplandığında ne tarayacağını bildiren metni girin. Örneğin çekme işini yüke göre gruplandırmak için <strong>LoadId</strong> alanını kullanıyorsanız alana <strong>Yük kodu</strong> girebilirsiniz.</td>
</tr>
<tr class="odd">
<td>İş şablonu kodu</td>
<td>Bir işlem için işi oluşturacak iş şablonunu seçin. Örneğin, bir satınalma siparişi için bir ürün alırsanız, yerine koyma işi iş şablonuna dayalı olarak oluşturulur. Bir iş şablonu seçmezseniz, Supply Chain Management sorgu kriterine dayanarak bir şablon atar. İş Şablonları hakkında daha fazla bilgi için bkz. <a href="control-warehouse-location-directives.md">İş şablonları ve konum yönergeleri ile ambar çalışmasını denetleme</a>.</td>
<tr class="even">
<td>İş satırı listesini göster</td>
<td>Çalışanların şu anda seçili malzeme çekme çalışmasının satırlarını nasıl görüntüleyebileceğini ve etkileşimde bulunabileceğini seçmek için bir seçenek belirleyin. Bu seçenek hakkında daha fazla bilgi edinmek için, bkz. <a href="pick-line-overview.md">Bir mobil cihaz menü öğesini malzeme çekme satırı özeti sağlayacak şekilde ayarlama</a>.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Çalışanların madde çekerken ürün, konum veya miktarı doğrulamasını gerektirme
Bir çalışanın, ambardaki işi gerçekleştirirken konumu veya miktarı kayda geçirmek için mobil cihaz kullanmasını gerektiren iş doğrulamaları ayarlayabilirsiniz. İş doğrulamaları, çalışanın doğru konumda olmasını veya doğru miktarda madde ile uğraşmasını sağlamaya yardımcı olur. Supply Chain Management'ın işçinin kaydını otomatik olarak doğrulamasını da etkinleştirebilirsiniz. Otomatik doğrulamayı etkinleştirirseniz, konum veya miktar için de doğrulama isteyemezsiniz. İş doğrulamaları, ürünleri ve ürün çeşitlerini de içerir. Ayrıca, bir barkod tarayarak da doğrulamaları kayda geçirebilirsiniz. Ürünleri ve ürün varyantlarını doğrulamak için, ürün veya ürün varyantı için kod girmeniz gerekir. Bu kod, bir ürün kodu, ürün arama kodu, harici kod, GTIN veya barkod olabilir. Kodu girdikten veya barkodu taradıktan sonra, ürün varyantına yönelik boyutlar mobil cihazda görüntülenir. 

Aşağıdaki tabloda, iş doğrulamalarını birlikte kullanabileceğiniz çeşitli iş türleri açıklanmaktadır.

| Seçenek | Açıklama |
|------------------------|----------------------------------------------------------------------------|
| Seç | Maddeler çekileceği zaman doğrulama gerektirin. |
| Yerine Koy | Maddeler bir konuma konacağı zaman doğrulama gerektirin. |
| Sayım | Döngü sayımı sırasında doğrulama gerektirin. |
| Ayarlamalar | Stok miktarları ayarlandığında doğrulama gerektirin. |
| Özel | Özel iş için doğrulama gerektirin. |
| Karantina | Öğeler karantinaya alınırken doğrulama gerektirin. |
| Plaka oluşturma | Maddeler plaka oluşturmak için konsolide edilirken doğrulama gerektirin. |
| Yazdır | Plaka etiketleri yazdırılırken doğrulama gerektirin. |
| Durum değişikliği | Stok durumunu değiştirilirken doğrulama gerektirin. |

> [!NOTE]
> Ürün onayını yalnızca çekme ve yerine yerleştirme türleri için zorunlu tutabilirsiniz.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Satınalma siparişi iş türünü tamamlamak için bir mobil cihaz menü öğesi ayarlama](tasks/set-up-mobile-device-menu.md)

[Alınan maddeleri kaydetmek için bir mobil cihaz menü öğesi ayarlama](tasks/set-up-mobile-device-menu-item-register-received-items.md)

[Stok durumları](../inventory/inventory-statuses.md)


