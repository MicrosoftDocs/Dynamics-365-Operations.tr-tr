---
title: Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri
description: Bu konu, ölçek birimlerinin ambar yönetimi iş yükünden seçili işlemleri çalıştırmasını sağlayan özellik hakkında bilgi sağlar.
author: perlynne
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6372e08b7ec737f3abd2f2bd5d4f387eaf869f03
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832406"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Bir ölçek birimi üzerinde iş yükü çalıştıran ambarlar için tüm ambar yönetimi iş işlevleri tam olarak desteklenmez. Yalnızca bu konunun açıkça desteklenen olarak tanımladığı işlemleri kullandığınızdan emin olun.

## <a name="warehouse-execution-on-scale-units"></a>Ölçek birimlerinde ambar yürütme

Bu özellik, ölçek birimlerinin ambar yönetimi özelliklerinden seçili işlemlerin çalıştırılmasını sağlar. Bulut ölçek birimleri, seçtiğiniz Microsoft Azure bölgesinde özel işleme kapasitesini kullanarak iş yüklerini bulutta çalıştırır. Uç ölçek birimlerinde, ölçek birimlerinin bulutla geçici olarak bağlantısı kesilse bile, bazı iş yüklerini şirket içinde bağımsız olarak çalıştırabilirsiniz.

Bu konudaki, ölçek birimi olarak tanımlanan bir ambardaki ambar yönetimi yürütmeleri *Ambar yürütme sistemi* *(WES)* olarak da bilinir.

## <a name="prerequisites"></a>Önkoşullar

Ambar yönetimi iş yüküyle birlikte dağıtılan bir Dynamics 365 Supply Chain Management hub'ına ve ölçek birimine sahip olmalısınız. Mimari ve dağıtım süreçleri hakkında daha fazla bilgi için bkz. [Üretim ve ambar yönetimi iş yükleri için bulut ve edge ölçek birimleri](cloud-edge-landing-page.md).

## <a name="how-the-wes-workload-works-on-scale-units"></a>WES iş yükü ölçek birimlerinde nasıl çalışır?

Ambar yönetimi iş yükündeki işlemler için veriler hub ve ölçek birimleri arasında eşitlenir.

Bir ölçek birimi yalnızca sahip olduğu verileri koruyabilir. Ölçek birimleri için veri sahipliği kavramı çok büyük çakışmaları önlemeye yardımcı olur. Bu nedenle, hangi işlemlerin hub'a ait olduğunu ve hangilerinin ölçek birimlerine ait olduğunu anlamanız önemlidir.

Ölçek birimleri aşağıdaki verilere sahiptir:

- **Dalga işleme verileri**: Seçilen dalga işleme yöntemleri ölçek birimi dalga işlemenin bir parçası olarak yönetilir.
- **İş işleme verileri**: Aşağıdaki iş emri işleme türleri desteklenir:

  - **Stok hareketleri** (el ile hareket ve şablon ile hareket işi)
  - **Satınalma siparişleri** (satınalma siparişleri yüklerle ilişkilendirilmediğinde ambar siparişi aracılığıyla yerine koyma işi)
  - **Satış siparişleri** (basit malzeme çekme ve yükleme işi)
  - **Transfer emirleri** (basit malzeme çekme ve yüklemeyle yalnızca giden iş)

- **Ambar sipariş girişi verileri**: Bu veriler yalnızca ambara el ile serbest bırakılan satın alma siparişleri için kullanılır.
- **Plaka verileri**: Plakalar hub ve ölçek biriminde oluşturulabilir. Özel çakışma yönetimi sağlanmıştır. Bu verilerin ambara özgü olmadığını unutmayın.

## <a name="outbound-process-flow"></a>Giden işleme akışı

Hub aşağıdaki verilere sahiptir:

- Satış siparişleri ve transfer emirleri gibi tüm kaynak belgeler
- Sipariş tahsisi ve giden yük işleme
- Ambara serbest bırakma, sevkiyat oluşturma, dalga oluşturma ve dalgayı kesinleştirme işlemleri

Ölçek birimleri, dalganın serbest bırakılmasından sonra gerçek dalga işlemenin (iş tahsisatı, stok yenileme işi ve talep işi oluşturma gibi) sahibidir. Bu nedenle, ambar çalışanları, ölçek birimine bağlı bir Ambar Yönetimi mobil uygulaması kullanarak giden işleri işleyebilir.

![Dalga işleme akışı](./media/wes-wave-processing-ga.png "Dalga işleme akışı")

## <a name="inbound-process-flow"></a>Gelen işlem akışı

Hub aşağıdaki verilere sahiptir:

- Satın alma siparişleri ve satış iade siparişleri gibi tüm kaynak belgeler
- Gelen ambar işleme
- Tüm maliyet güncelleştirmeleri ve mali güncelleştirmeler

> [!NOTE]
> Gelen satınalma siparişi akışı, kavramsal olarak giden akıştan farklıdır. Satınalma siparişinin ambara serbest bırakılmış olup olmadığına bağlı olarak, aynı ambara ölçek biriminde veya merkezde çalıştırabilirsiniz. Bir siparişi ambara serbest bıraktıktan sonra söz konusu sipariş üzerinde yalnızca ölçek biriminde oturumunuz açıkken çalışabilirsiniz.

*Ambara serbest bırakma* kullanıyorsanız [*ambar siparişleri*](cloud-edge-warehouse-order.md) oluşturulur ve ilgili alıcı akışının sahipliği ölçek birimine atanır. Hub, gelen alıcıyı kaydedemez.

*Ambara serbest bırakma* işlemini kullanmak için hub'da oturum açmanız gerekir. Aşağıdaki sayfalardan birine giderek işlemi çalıştırın veya zamanlayın:

- **Satın alma ve tedarik > Satın alma siparişleri > Tüm satın alma siparişleri > Ambar > Eylemler > Ambara serbest bırak**
- **Ambar yönetimi > Ambara serbest bırak > Satın alma siparişlerini otomatik serbest bırak**

**Satın alma siparişlerini otomatik olarak serbest bırakma** işlevini kullanırken, sorguyu temel alan belirli satın alma siparişi satırlarını seçebilirsiniz. Tipik bir senaryo örneği, ertesi gün gelmesi beklenen tüm onaylanmış satın alma siparişi satırlarını serbest bırakan yinelenen bir toplu işlem ayarlamaktır.

Çalışan, ölçek birimine bağlı bir Ambar Yönetimi mobil uygulamasını kullanarak teslim alma işlemini çalıştırabilir. Veriler daha sonra ölçek birimi tarafından kaydedilir ve gelen ambar siparişine göre raporlanır. Sonraki yerine koyma işlemlerinin oluşturulması ve işlenmesi de ölçek birimi tarafından yönetilir.

*Ambara serbest bırakma* işlemini kullanmıyorsanız ve bu nedenle *ambar siparişlerini* kullanmıyorsanız hub, ambar teslim alma işlemini ve iş işlemeyi ölçek birimlerinden bağımsız olarak işleyebilir.

![Gelen işlem akışı](./media/wes-inbound-ga.png "Gelen işlem akışı")

## <a name="supported-processes-and-roles"></a>Desteklenen süreçler ve roller

Tüm ambar yönetimi süreçleri bir ölçek birimindeki WES iş yükünde desteklenmez. Bu nedenle, her kullanıcı için kullanılabilen işlevsellikle eşleşen roller atamanızı öneririz.

Bu işlemi kolaylaştırmak için **Sistem yönetimi \> Güvenlik \> Güvenlik yapılandırması**'ndaki demo verilerine *İş yükündeki ambar yöneticisi* adlı örnek bir rol dahildir. Bu rolün amacı, ambar yöneticilerinin ölçek biriminde WES'e erişmesini sağlamaktır. Rol, ölçek biriminde barındırılan bir iş yükü bağlamında ilgili sayfalara erişim sağlar.

Bir ölçek birimindeki kullanıcı rolleri, hub'dan ölçek birimine ilk veri eşitlemesi kapsamında atanır.

Bir kullanıcıya atanan rolleri değiştirmek için **Sistem yönetimi \> Güvenlik \> Kullanıcılara roller atayın** öğesine gidin. Yalnızca ölçek birimlerinde ambar yöneticisi olarak görev yapan kullanıcılara yalnızca *İş yükündeki Ambar yöneticisi* rolü atanmalıdır. Bu yaklaşım, bu kullanıcıların yalnızca desteklenen işlevselliğe erişmesini sağlayacaktır. Bu kullanıcılara atanan diğer rolleri kaldırın.

Hub ve ölçek birimlerinde ambar yöneticisi olarak görev yapan kullanıcılara var olan *Ambar çalışanı* rolü atanmalıdır. Bu rolün ambar çalışanlarına kullanıcı arabiriminde (Kullanıcı Arabirimi) görünen ancak şu anda ölçek birimlerinde desteklenmeyen özelliklere (transfer emri alımını işleme gibi) erişim izni verdiğini unutmayın.

## <a name="supported-wes-processes"></a>Desteklenen WES süreçleri

Bir ölçek biriminde WES iş yükü için aşağıdaki ambar yürütme işlemleri etkinleştirilebilir:

- Satış ve transfer siparişleri (tahsisat, talep stok yenileme, konteyner kullanımı, iş oluşturma ve dalga etiketi yazdırma) için seçilen dalga yöntemleri
- Ambar Yönetimi mobil uygulamasını kullanarak satış ve transfer siparişi ambar işini işleme (stok yenileme çalışması dahil)
- Ambar Yönetimi mobil uygulamasını kullanarak eldeki stoğu sorgulama
- Ambar Yönetimi mobil uygulamasını kullanarak stok hareketleri oluşturma ve çalıştırma
- Ambar Yönetimi mobil uygulamasını kullanarak satın alma siparişlerini kaydetme ve yerine koyma işi yapma

Aşağıdaki iş emri türleri şu anda ölçek birimi dağıtımlarında WES iş yükleri için desteklenir:

- Satış siparişleri
- Transfer sorunu
- Stok yenileme
- Stok hareketi
- Satış siparişleri (ambar siparişlerine bağlı)

Şu anda ölçek birimlerinde başka türde kaynak belge işleme veya depo işi desteklenmemektedir. Örneğin, ölçek birimindeki bir WES iş yükü için transfer emri alımını işleme (transfer girişi) veya işlem döngüsü sayım işini gerçekleştiremezsiniz.

> [!NOTE]
> Desteklenmeyen işlevler için mobil cihaz menü öğeleri ve düğmeleri, ölçek birimi dağıtımına bağlı olduğunda _Ambar Yönetimi mobil uygulamasında_ gösterilmez.

> [!WARNING]
> Bir ölçek biriminde iş yükü çalıştırıyorsanız merkezdeki belirli bir ambar için desteklenmeyen işlemleri çalıştıramazsınız. Bu konunun ilerleyen kısımlarında sağlanan tablolar desteklenen özellikleri gösterir.
>
> Seçili ambar iş türleri hem merkezde hem de ölçek birimlerinde oluşturulabilir ancak yalnızca sahibi olan merkez veya ölçek birimi (verileri oluşturan dağıtım) tarafından saklanabilir.
>
> Belirli bir işlem, ölçek birimi tarafından desteklense bile gerekli tüm verilerin merkezden ölçek birimine veya ölçek biriminden merkeze eşitlenmeyebileceğini ve bu durumun beklenmeyen sistem işlemesi riski oluşturabileceğini unutmayın. Buna örnek olarak şunlar verilebilir:
> 
> - Yalnızca merkez dağıtımında bulunan bir veri tablosu kaydıyla birleştirilen bir yerleşim yönergesi sorgusu kullanmanız.
> - Konum durumu ve/veya yerleşim hacimsel yük işlevleri kullanmanız. Bu veriler, dağıtımlar arasında eşitlenmeyecek ve bu nedenle yalnızca dağıtımlardan birinde eldeki yerleşim stokunu güncelleştirirken çalışacaktır.

Aşağıdaki ambar yönetimi işlevi şu anda ölçek birimi iş yükleri için desteklenmemektedir:

- Yüke atanan satınalma siparişi satırlarının gelen işlemesi
- Bir proje için satınalma siparişlerinin gelen işlemesi
- Etkin izleme boyutları **Sahip** ve/veya **Seri numarası** sahibi olan öğeler için gelen ve giden işlemesi
- Engelleme durumu değeri olan stoğu işleme
- Herhangi bir iş hareketi işlemi sırasında stok durumunu değiştirme
- Sipariş taahhütlü esnek ambar düzeyi boyutu rezervasyonları
- *Ambar yerleşimi durumu* işlevinin kullanımı (veriler dağıtımlar arasında eşitlenmez)
- *Yerleşim plakası konumlandırması* işlevinin kullanımı
- **Toplu işlerin karıştırılacağı gün sayısı** ayarı dahil *Ürün filtreleri* ve *Ürün filtre grupları* kullanımı
- Kalite yönetimi ile tümleştirme
- Fiili ağırlık maddeleriyle işleme
- Yalnızca Taşıma yönetimi (TMS) için etkinleştirilen maddelerle işleme
- Eldeki negatif stokla işleme
- Özel iş türleriyle ambar iş işlemesi
- Sevkiyat notlarıyla ambar işi işleme
- Döngü sayımı eşik tetiklemesiyle ambar işi işleme
- Malzeme işlemesi/ambar otomasyonu ile ambar işi işlemesi
- Ürün ana verileri görüntüsünün kullanımı (ör. Ambar Yönetimi mobil uygulamasında)

> [!WARNING]
> Bazı ambar işlevleri, ölçek biriminde ambar yönetimi iş yüklerini çalıştıran ambarlar için kullanılamaz ve merkezde ya da ölçek birimi iş yükünde desteklenmez.
> 
> Diğer özellikler her ikisinde de işlenebilir, ancak zaman uyumsuz veri güncelleştirme işlemi nedeniyle aynı ambar için hem merkezdeki hem de ölçek birimindeki eldeki stokun güncelleştirilmesi gibi bazı senaryolarda dikkatli kullanılmaları gerekir.
> 
> Hem merkezde hem de ölçek birimlerinde desteklenen belirli işlevler (ör. *iş engelleme*), yalnızca verilerin sahibi için desteklenecektir.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Giden (yalnızca satış siparişleri ve transfer emirleri için desteklenir)

Aşağıdaki tablo, ambar yönetimi iş yükleri bulut ve uç ölçek birimlerinde kullanıldığında hangi giden özelliklerin desteklendiklerini ve bunların nerede desteklendiklerini gösterir.

| İşle                                                      | Hub | Bir ölçek biriminde WES iş yükü |
|--------------------------------------------------------------|-----|------------------------------|
| Kaynak belge işleme                                   | Evet | No |
| Yük ve taşıma yönetimini işleme                | Evet | No |
| Ambara serbest bırak                                         | Evet | No |
| Planlanmış çapraz sevk                                        | No  | No |
| Sevkiyat konsolidasyonu                                       | Evet | No |
| Sevkiyat dalgası işleme                                     | Evet, ancak yalnızca dalganın başlatılması ve sonlandırılması merkezde gerçekleştirilir. Bu, yalnızca giden transfer emri ve satış siparişi işlemenin ölçek birimi tarafından gerçekleştirilebileceği anlamına gelir.|<p>Hayır, başlatma ve sonlandırma merkez tarafından gerçekleştirilir ve **Yük oluşturma ve sıralama** desteklenmez<p><b>Not:</b> Dalga işlemenin bir parçası olarak dalga durumunu sonuçlandırmak için hub'a erişim gereklidir.</p> |
| Dalga için sevkiyatları saklama                                  | Evet | No |
| Ambar iş işleme (plaka baskısı dahil)        | No  | <p>Evet, ancak yalnızca yukarıda belirtilen desteklenen özellikler için geçerlidir. |
| Küme malzeme çekme                                              | No  | Evet|
| "Sevk edilmiş konteyner çekme işlemi" işini işleme dahil elle ambalaj işleme                                           | No <P>Bazı işlemler, yalnızca ilk çekme işlemi ölçek birimi tarafından gerçekleştirildikten sonra yapılabilir ancak aşağıdaki engelli işlemler nedeniyle bu önerilmez.</p>  | No  |
| Konteyneri gruptan kaldır                        | No  | No                           |
| Giden sıralama işleme                                  | No  | No |
| Yükle ilgili belgeleri yazdırma                           | Evet | No |
| Konşimento ve ASN üretimi                            | Evet | No |
| Sevkiyat onaylama                    | Evet  | No |
| "Onayla ve aktar" ile sevkiyat onayı                    | No  | No |
| Sevk irsaliyesi ve faturalama işlemleri                | Evet | No |
| Eksik malzeme çekme (satış siparişleri ve transfer emirleri)                    | No  | No |
| Fazla malzeme çekme (satış siparişleri ve transfer emirleri)                     | No  | No |
| İş yerleşimlerinin değiştirilmesi (satış siparişleri ve transfer emirleri)         | No  | Evet|
| Tüm iş (satış siparişleri ve transfer emirleri)                    | No  | Evet|
| İş raporunu yazdırma                                            | Evet | No |
| Dalga etiketi                                                   | No  | Evet|
| İş bölme                                                   | No  | Evet|
| İş işleme - "Taşıma yüklemesi" tarafından yönetilir            | No  | No |
| Çekilen miktarı düş                                       | No  | No |
| İşi geri al                                                 | No  | No |
| Sevkiyat onayını tersine çevir                                | Evet | No |

### <a name="inbound"></a>Gelen

Aşağıdaki tablo, ambar yönetimi iş yükleri bulut ve uç ölçek birimlerinde kullanıldığında hangi gelen özelliklerin desteklendiklerini ve bunların nerede desteklendiklerini gösterir.

| İşle                                                          | Hub | Bir ölçek biriminde WES iş yükü<BR>*("Evet" olarak işaretlenmiş maddeler yalnızca ambar siparişleri için geçerlidir)*</p> |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Kaynak&nbsp;belge&nbsp;türü                                       | Evet | No |
| Yük ve taşıma yönetimini işleme                    | Evet | No |
| Gelen sevkiyat onayı                                            | Evet | No |
| Ambara satın alma siparişi serbest bırakma (ambar siparişi işleme) | Evet | No |
| Ambar sipariş satırlarının iptali<p>Bunun yalnızca satıra karşılık kayıt gerçekleştirilmediği durumlarda desteklendiğini unutmayın</p>          | Evet | No |
| Satınalma siparişi maddesini teslim alma ve yerine koyma                       | <p>Evet,&nbsp;ambar&nbsp;siparişi&nbsp;yoksa</p><p>Hayır, ambar siparişi olduğunda</p> | <p>Evet, satınalma siparişinin bir <i>yükün</i> parçası olmadığı durumlarda</p> |
| Satınalma siparişi satırı teslim alma ve yerine koyma                        | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | <p>Evet, satınalma siparişinin bir <i>yükün</i> parçası olmadığı durumlarda</p></p> |
| İade emri teslim alma ve yerine koyma                               | Evet | No |
| Karma plaka alımı ve yerine koyma işlemi                        | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| Yük maddesi teslim alma                                             | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| Plaka alma ve yerine koyma                              | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| Transfer emri maddesini teslim alma ve yerine koyma                        | Evet | No |
| Transfer emri satırı teslim alma ve yerine koyma                        | Evet | No |
| Çalışmayı iptal etme (gelen)                                              | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | <p>Evet, ancak yalnızca <b>İşi iptal ederken girişin kaydını sil</b> seçeneği (<b>Ambar yönetimi parametreleri</b> sayfasında) seçili olmadığında</p> |
| Satın alma siparişi ürün girişi işleme                          | Evet | No |
| Eksik teslimat ile satınalma siparişi alma                        | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Evet, ancak yalnızca hub'dan iptal isteğinde bulunarak |
| Fazla teslimat ile satınalma siparişi alma                        | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Evet  |
| *Çapraz sevk* işinin oluşturulmasıyla alma                   | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| *Kalite emri* işinin oluşturulmasıyla alma                  | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| *Kalite maddesi örnekleme* işinin oluşturulmasıyla alma          | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| *Kalite denetiminde kalite* işinin oluşturulmasıyla alma       | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| Kalite emrinin oluşturulmasıyla alma                            | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| İş işleme - *Küme yerine koyma* ile yönlendirilir                             | Evet | No |
| *Eksik çekme* ile iş işleme                                           | Evet | No |
| Plaka yükleme                                           | Evet | No |

### <a name="warehouse-operations-and-exception-handing"></a>Ambar işlemleri ve özel durum yönetimi

Aşağıdaki tablo, ambar yönetimi iş yükleri bulut ve uç ölçek birimlerinde kullanıldığında hangi ambar işlemleri ve özel durum yönetimi özelliklerinin desteklendiklerini ve bunların nerede desteklendiklerini gösterir.

| İşle                                            | Hub | Bir ölçek biriminde WES iş yükü |
|----------------------------------------------------|-----|------------------------------|
| Plaka sorgusu                              | Evet | Evet                          |
| Madde sorgusu                                       | Evet | Evet                          |
| Konum sorgusu                                   | Evet | Evet                          |
| Ambarı değiştir                                   | Evet | Evet                          |
| Hareket                                           | Evet | Evet                          |
| Şablonla hareket                               | Evet | Evet                          |
| Ambar transferi                                 | Evet | No                           |
| Ambar Yönetimi mobil uygulamasından transfer emri oluşturma           | Evet | No                           |
| Ayarlama (giriş/çıkış)                                | Evet | No                           |
| Stok durumu değişikliği                            | Evet | No                           |
| Döngü sayma ve Sayma tutarsızlığı işleme | Evet | No                           |
| Plaka etiketini yeniden yazdırma (plakayı yeniden yazdır)             | Evet | Evet                          |
| Plaka yapısı                                | Evet | No                           |
| Plaka bölme                                | Evet | No                           |
| İç içe plakalar olarak paketle                                | Evet | No                           |
| Sürücü girişi                                    | Evet | No                           |
| Sürücü çıkışı                                   | Evet | No                           |
| Toplu iş değerlendirme kodunu değiştirme                      | Evet | Evet                          |
| Açık iş listesini görüntüle                             | Evet | Evet                          |
| Plakaları birleştir                         | Evet | No                           |
| Minimum/maksimum ve bölge eşiği stok yenileme işlemi| Evet <p>Sorguların parçası olarak aynı yerleşimleri eklememeniz önerilir</p>| Evet                          |
| Yerleştirme stok yenileme işleme                  | Evet  | Evet<p>Kurulumun ölçek biriminde gerçekleştirilmesi gerektiğini unutmayın</p>                           |
| İşi engelleme ve engellemeyi kaldırma                             | Evet | Evet                          |
| Kullanıcı değiştir                                        | Evet | Evet                          |
| İşteki iş havuzunu değiştirme                           | Evet | Evet                          |
| İşi iptal et                                        | Evet | Evet                          |


### <a name="production"></a>Üretim

Ambar yönetimi üretim senaryoları, aşağıdaki tabloda belirtildiği gibi şu anda ölçek birimi iş yüklerinde desteklenmez.

| İşle | Hub | Bir ölçek biriminde WES iş yükü |
|---------|-----|------------------------------|
| <p>Üretimle ilgili tüm ambar yönetim süreçleri. Burada bazı örnekler verilmiştir:</p><li>Ambara serbest bırak</li><li>Üretim dalgası işleme</li><li>Hammadde çekme</li><li>RAF ve yerine konan mamul mallar</li><li>Yerine konan ortak ürün ve yan ürün</li><li>Kanban yerine koyma</li><li>Kanban çekme</li><li>Üretim emrini başlat</li><li>Üretim ıskartası</li><li>Üretimdeki son palet</li><li>Malzeme tüketimini kaydet</li><li>Kanban boş</li></ul> | Evet | No |

## <a name="maintaining-scale-units-for-wes"></a>WES için ölçek birimleri bakımı

Hem hub hem de ölçek birimlerinde birden çok toplu iş çalışır.

Hub dağıtımında toplu işleri el ile koruyabilirsiniz. **Ambar yönetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi**'nde aşağıdaki toplu işleri yönetebilirsiniz:

- İşleme işi durumu güncelleştirme olayları
- Ölçek biriminden hub'a ileti işlemcisi
- Kaynak sipariş girişlerini kaydet
- Ambar siparişlerini tamamla
- Ambar sipariş satırları için miktar güncelleştirme yanıtlarını işle

Ölçek birimlerindeki iş yükünde, **Ambar yönetimi \> Periyodik görevler \> İş yükü yönetimi**'nde aşağıdaki toplu işleri yönetebilirsiniz:

- Dalga tablosu kayıtlarını işleme
- Ambar hub'ından ölçek birimine ileti işlemcisi
- Ambar sipariş satırları için miktar güncelleştirme isteklerini işle


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
