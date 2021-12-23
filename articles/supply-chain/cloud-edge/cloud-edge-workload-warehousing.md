---
title: Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri
description: Bu konu, ölçek birimlerinin ambar yönetimi iş yükünden seçili işlemleri çalıştırmasını sağlayan özellik hakkında bilgi sağlar.
author: perlynne
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers, SysWorkloadDuplicateRecord
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ae8e9791b590a32581b66853f55ea11bc389bb19
ms.sourcegitcommit: 96515ddbe2f65905140b16088ba62e9b258863fa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/04/2021
ms.locfileid: "7891783"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Bir ölçek birimi üzerinde iş yükü çalıştıran ambarlar için tüm ambar yönetimi iş işlevleri tam olarak desteklenmez. Yalnızca bu konunun açıkça desteklenen olarak tanımladığı işlemleri kullandığınızdan emin olun.

## <a name="warehouse-execution-on-scale-units"></a>Ölçek birimlerinde ambar yürütme

Ambar yönetimi iş yükleri, bulut ve uç ölçek birimlerinin ambar yönetimi yeteneklerinden seçilen süreçleri çalıştırmasını sağlar.

## <a name="prerequisites"></a>Önkoşullar

Ambar yönetimi iş yüküyle birlikte dağıtılan bir Dynamics 365 Supply Chain Management hub'ına ve ölçek birimine sahip olmalısınız. Mimari ve dağıtım işlemi hakkında daha fazla bilgi için bkz. [Dağıtılmış hibrit topolojide ölçek birimleri](cloud-edge-landing-page.md).

## <a name="how-the-warehouse-execution-workload-works-on-scale-units"></a>Ambar yürütme iş yükünü ölçek birimlerinde çalıştırma

Ambar yönetimi iş yükündeki işlemler için veriler hub ve ölçek birimleri arasında eşitlenir.

Bir ölçek birimi yalnızca sahip olduğu verileri koruyabilir. Ölçek birimleri için veri sahipliği kavramı çok büyük çakışmaları önlemeye yardımcı olur. Bu nedenle, hangi işlem verilerinin merkeze ve hangilerinin ölçek birimlerine ait olduğunu anlamanız önemlidir.

İş süreçlerine bağlı olarak, aynı veri kaydı merkez ile ölçek birimleri arasındaki sahipliği değiştirebilir. Bu senaryonun bir örneği aşağıdaki bölümde verilmiştir.

> [!IMPORTANT]
> Bazı veriler hem merkezde hem de ölçek biriminde oluşturulabilir. **Plakalar** ve **Toplu iş numaraları** örnek olarak verilebilir. Aynı eşitleme döngüsü sırasında hem merkezde hem de ölçek biriminde aynı benzersiz kaydın oluşturulduğu bir senaryo olması durumunda özel çakışma yönetimi sağlanır. Bu durumda, bir sonraki eşitleme başarısız olursa verileri görüntüleyip birleştirebilmek için **Sistem yönetimi > Sorgular > İş yükü sorguları > Yinelenen kayıtlar**'a gitmeniz gerekir.

## <a name="outbound-process-flow"></a>Giden işleme akışı

Bir bulut veya uç ölçek birimine ambar yönetimi iş yükü dağıtmadan önce, kuruluş merkeziniz üzerinde *Çıkış siparişleri için ambar özelliğini serbest bırakmak üzere ölçek birimi desteği* özelliğinin etkin olduğundan emin olun. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Giden siparişlerin ambara serbest bırakılmasına yönelik ölçek birimi desteği*

Giden veri sahipliği işlemi, yük planlama işlemini kullanıp kullanmadığınıza bağlıdır. Merkez, her durumda satış siparişleri ve transfer siparişleri gibi *kaynak belgelerine* ve sipariş tahsisatı işlemi ve ilgili sipariş hareketi verilerine sahiptir. Ancak yük planlama işlemini kullandığınızda, yükler merkez üzerinde oluşturulur ve bu nedenle başlangıçta merkeze ait olur. *Ambara serbest bırakma* işleminin parçası olarak, yük verilerinin sahipliği, sonraki *sevkiyat dalgası işleme*'nin (iş tahsisatı, stok yenileme işi ve talep işi oluşturma gibi) sahibi olacak özel ölçek birimi dağıtımına aktarılır. Bu nedenle, ambar çalışanları yalnızca belirli ölçek birimi iş yükünü çalıştıran dağıtıma bağlı olan bir Warehouse Management mobil uygulamasını kullanarak giden satış ve transfer siparişi işini işleyebilir.

Son iş süreci, stoku son sevkiyat konumuna (Baydoor) yerleştirdiğinde, ölçek birimi merkeze kaynak belgesi stok hareketlerinin *Çekildi* olarak güncelleştirilmesi için sinyal verir. Bu işlem çalıştırılana ve tekrar eşitlenene kadar ölçek birimi iş yükündeki eldeki stok, ambar düzeyinde fiziksel olarak rezerve edilir ve bu eşitlemenin tamamlanmasını beklemeden giden sevkiyat onayını hemen işleyebilirsiniz. Yük için sonraki satış sevk irsaliyesi ve faturalama veya transfer emri sevkiyatı merkezde ele alınır.

Aşağıdaki diyagramda giden akış ve ayrı ayrı iş süreçlerinin nerede gerçekleştiği gösterilmektedir. (Büyütmek için diyagramı seçin.)

[![Giden işleme akışı.](media/wes_outbound_warehouse_processes-small.png "Giden işleme akışı")](media/wes_outbound_warehouse_processes.png)

### <a name="outbound-processing-with-load-planning"></a>Yük planlama ile giden işleme

Yük planlama işlemini kullandığınızda, yükler ve sevkiyatlar merkezde oluşturulur ve verilerin sahipliği, aşağıdaki şekilde gösterildiği gibi *Ambara serbest bırakma* işleminin parçası olarak ölçek birimlerine aktarılır.

![Yük planlama ile giden işleme.](./media/wes_outbound_processing_with_load_planning.png "Yük planlama ile giden işleme")

### <a name="outbound-processing-without-load-planning"></a>Yük planlama olmadan giden işleme

Yük planlama işlemini kullanmazsanız sevkiyatlar ölçek birimlerinde oluşturulur. Yükler, dalga işleminin parçası olarak ölçek birimlerinde de oluşturulur.

![Yük planlama olmadan giden işleme.](./media/wes_outbound_processing_without_load_planning.png "Yük planlama olmadan giden işleme")

## <a name="inbound-process-flow"></a>Gelen işlem akışı

Hub aşağıdaki verilere sahiptir:

- Satınalma ve üretim siparişleri gibi tüm kaynak belgeler
- Gelen ambar işleme
- Tüm maliyet güncelleştirmeleri ve mali güncelleştirmeler

> [!NOTE]
> Gelen satınalma siparişi akışı, kavramsal olarak giden akıştan farklıdır. Aynı ambarı, satınalma siparişinin ambara serbest bırakılıp bırakılmadığına bağlı olarak ölçek biriminde veya merkezde çalıştırabilirsiniz. Siparişi ambara serbest bıraktıktan sonra, söz konusu sipariş üzerinde yalnızca ölçek biriminde oturumunuz açıkken çalışabilirsiniz.
>
> *Ambara serbest bırakma* kullanıyorsanız [*ambar siparişleri*](cloud-edge-warehouse-order.md) oluşturulur ve ilgili alıcı akışının sahipliği ölçek birimine atanır. Hub, gelen alıcıyı kaydedemez.

*Ambara serbest bırakma* işlemini kullanmak için hub'da oturum açmanız gerekir. Satınalma siparişi işleme için satınalma siparişini çalıştırmak veya planlamak üzere aşağıdaki sayfalardan birine gidin:

- **Satın alma ve tedarik > Satın alma siparişleri > Tüm satın alma siparişleri > Ambar > Eylemler > Ambara serbest bırak**
- **Ambar yönetimi > Ambara serbest bırak > Satın alma siparişlerini otomatik serbest bırak**

**Satın alma siparişlerini otomatik olarak serbest bırakma** işlevini kullanırken, sorguyu temel alan belirli satın alma siparişi satırlarını seçebilirsiniz. Tipik bir senaryo örneği, ertesi gün gelmesi beklenen tüm onaylanmış satın alma siparişi satırlarını serbest bırakan yinelenen bir toplu işlem ayarlamaktır.

Çalışan, ölçek birimine bağlı bir Warehouse Management mobil uygulamasını kullanarak teslim alma işlemini çalıştırabilir. Veriler daha sonra ölçek birimi tarafından kaydedilir ve gelen ambar siparişine göre raporlanır. Sonraki yerine koyma işlemlerinin oluşturulması ve işlenmesi de ölçek birimi tarafından yönetilir.

*Ambara serbest bırakma* işlemini kullanmıyorsanız ve bu nedenle *ambar siparişlerini* kullanmıyorsanız hub, ambar teslim alma işlemini ve iş işlemeyi ölçek birimlerinden bağımsız olarak işleyebilir.

![Gelen işlem akışı.](./media/wes-inbound-ga.png "Gelen işlem akışı")

Çalışan, ölçek birimine karşı bir Warehouse Management mobil uygulaması alma işlemini kullanarak gelen kaydı yaptığında, ölçek biriminde depolanan ilgili ambar siparişine karşı bir makbuz kaydedilir. Ardından ölçek birimi iş yükü, ilgili satınalma siparişi satırı işlemlerini *Kayıtlı* olarak güncelleştirmek için merkeze sinyal gönderir. Bu işlem tamamlanır tamamlanmaz, bir satınalma siparişi ürün girişini merkezde çalıştırabilirsiniz.

Aşağıdaki diyagramda gelen akış ve ayrı ayrı iş süreçlerinin nerede gerçekleştiği gösterilmektedir. (Büyütmek için diyagramı seçin.)

[![Gelen işleme akışı](media/wes_inbound_warehouse_processes-small.png "Gelen işleme akışı")](media/wes_inbound_warehouse_processes.png)

## <a name="supported-processes-and-roles"></a>Desteklenen süreçler ve roller

Tüm ambar yönetimi işlemleri ölçek birimindeki ambar yürütme iş yükünde desteklenmez. Bu nedenle, her kullanıcı için kullanılabilen işlevsellikle eşleşen roller atamanızı öneririz.

Bu işlemi kolaylaştırmak için **Sistem yönetimi \> Güvenlik \> Güvenlik yapılandırması**'ndaki demo verilerine *İş yükündeki ambar yöneticisi* adlı örnek bir rol dahildir. Bu rolün amacı, ambar yöneticilerinin ölçek birimindeki ambar yürütme iş yüküne erişmesini sağlamaktır. Rol, ölçek biriminde barındırılan bir iş yükü bağlamında ilgili sayfalara erişim sağlar.

Bir ölçek birimindeki kullanıcı rolleri, hub'dan ölçek birimine ilk veri eşitlemesi kapsamında atanır.

Bir kullanıcıya atanan rolleri değiştirmek için **Sistem yönetimi \> Güvenlik \> Kullanıcılara roller atayın** öğesine gidin. Yalnızca ölçek birimlerinde ambar yöneticisi olarak görev yapan kullanıcılara yalnızca *İş yükündeki Ambar yöneticisi* rolü atanmalıdır. Bu yaklaşım, bu kullanıcıların yalnızca desteklenen işlevselliğe erişmesini sağlayacaktır. Bu kullanıcılara atanan diğer rolleri kaldırın.

Hub ve ölçek birimlerinde ambar yöneticisi olarak görev yapan kullanıcılara var olan *Ambar çalışanı* rolü atanmalıdır. Bu rolün ambar çalışanlarına kullanıcı arabiriminde (Kullanıcı Arabirimi) görünen ancak şu anda ölçek birimlerinde desteklenmeyen özelliklere (transfer emri alımını işleme gibi) erişim izni verdiğini unutmayın.

### <a name="supported-warehouse-execution-processes"></a>Desteklenen ambar yürütme işlemleri

Ölçek biriminde bir ambar yürütme iş yükü için aşağıdaki ambar yürütme işlemleri etkinleştirilebilir:

- Satış ve transfer siparişleri için seçilen dalga yöntemleri (doğrulama, yük oluşturma, tahsisat, talep stok yenilemesi, konteyner kullanımı, iş oluşturma ve dalga etiketi yazdırma)

- Ambar uygulamasını kullanarak satış ve transfer siparişi ambar işini işleme (stok yenileme çalışması dahil)
- Ambar uygulamasını kullanarak eldeki stoğu sorgulama
- Ambar uygulamasını kullanarak stok hareketleri oluşturma ve çalıştırma
- Ambar uygulamasını kullanarak döngü sayım işi oluşturma ve işleme
- Ambar uygulamasını kullanarak stok ayarlamaları yapma
- Ambar uygulamasını kullanarak satın alma siparişlerini kaydetme ve yerine koyma işi yapma

Aşağıdaki iş türleri bir ölçek biriminde oluşturulabilir ve bu nedenle, ambar yönetimi iş yükünün bir parçası olarak işlenebilir:

- **Stok hareketleri**: El ile hareket ve şablon işiyle hareket.
- **Döngü sayımı**: Sayım işlemlerinin parçası olarak ve onay/ret işlemleri bir uyumsuzluk içerir.
- **Satınalma siparişleri**: Satın alma siparişleri yüklerle ilişkilendirilmediğinde ambar siparişi aracılığıyla yerine koyma işi.
- **Satış siparişleri**: Basit malzeme çekme ve yükleme.
- **Transfer sorunu**: Basit malzeme çekme ve yükleme.
- **Stok yenileme**: Üretim için hammadde dahil değildir.
- **Yerine konan mamul mallar**: Tamamlandı olarak bildirme sonrası üretim süreci.
- **Ortak ürün ve yan ürün yerine koyma**: Tamamlandı olarak bildirme sonrası üretim süreci.

Şu anda ölçek birimlerinde başka türde kaynak belge işleme veya ambar işi desteklenmemektedir. Örneğin, ölçek birimindeki bir ambar yürütme iş yükü için transfer emri alımı işlemeyi (transfer girişi) gerçekleştiremezsiniz; bunun merkez kurulumu tarafından işlenmesi gerekir.

> [!NOTE]
> Desteklenmeyen işlevler için mobil cihaz menü öğeleri ve düğmeleri, ölçek birimi dağıtımına bağlı olduğunda _Warehouse Management mobil uygulamasında_ gösterilmez.
> 
> Bir ölçek biriminde iş yükü çalıştırıyorsanız merkezdeki belirli bir ambar için desteklenmeyen işlemleri çalıştıramazsınız. Bu konunun ilerleyen kısımlarında sağlanan tablolar desteklenen özellikleri gösterir.
>
> Seçili ambar iş türleri hem merkezde hem de ölçek birimlerinde oluşturulabilir ancak yalnızca sahibi olan merkez veya ölçek birimi (verileri oluşturan dağıtım) tarafından saklanabilir.
>
> Belirli bir işlem, ölçek birimi tarafından desteklense bile gerekli tüm verilerin merkezden ölçek birimine veya ölçek biriminden merkeze eşitlenmeyebileceğini ve bu durumun beklenmeyen sistem işlemesi riski oluşturabileceğini unutmayın. Bu senaryonun örnekleri şunları içerir:
> 
> - Yalnızca merkez dağıtımında bulunan bir veri tablosu kaydıyla birleştirilen bir yerleşim yönergesi sorgusu kullanmanız.
> - Konum durumu ve/veya yerleşim hacimsel yük işlevleri kullanmanız. Bu veriler, dağıtımlar arasında eşitlenmeyecek ve bu nedenle yalnızca dağıtımlardan birinde eldeki yerleşim stokunu güncelleştirirken çalışacaktır.

Aşağıdaki ambar yönetimi işlevi şu anda ölçek birimi iş yükleri için desteklenmemektedir:

- Yüke atanan satınalma siparişi satırlarının gelen işlemesi.
- Proje için satınalma siparişlerinin gelen işlemesi.
- Varış yeri maliyetini yönetme, seferleri kullanma ve transitteki malları izleme.
- Etkin **Sahip** ve/veya **Seri numarası** izleme boyutları olan maddeler için gelen ve giden işleme.
- Engelleme durumu değeri olan stoku işleme.
- Herhangi bir iş hareketi işlemi sırasında stok durumunun değiştirilmesi.
- Sipariş taahhütlü esnek ambar düzeyinde boyut rezervasyonları.
- *Ambar yerleşimi durumu* işlevinin kullanımı (veriler dağıtımlar arasında eşitlenmez).
- *Yerleşim plakası konumlandırması* işlevinin kullanımı.
- **Toplu işlerin karıştırılacağı gün sayısı** ayarı dahil olmak üzere *Ürün filtreleri* ve *Ürün filtre grupları* kullanımı.
- Kalite yönetimi ile tümleştirme.
- Fiili ağırlık maddeleriyle işleme.
- Yalnızca Taşıma yönetimi (TMS) için etkinleştirilen maddelerle işleme.
- Eldeki negatif stokla işleme.
- Sevkiyat notlarıyla ambar işi işleme.
- Malzeme işlemesi/ambar otomasyonu ile ambar işi işleme.
- Ürün ana verileri görüntüleri (ör. Warehouse Management mobil uygulamasında).
- Ürünler için şirketler arası veri paylaşımı.

> [!WARNING]
> Bazı ambar işlevleri, ölçek biriminde ambar yönetimi iş yüklerini çalıştıran ambarlar için kullanılamaz ve merkezde ya da ölçek birimi iş yükünde desteklenmez.
> 
> Diğer özellikler her ikisinde de işlenebilir, ancak zaman uyumsuz veri güncelleştirme işlemi nedeniyle aynı ambar için hem merkezdeki hem de ölçek birimindeki eldeki stokun güncelleştirilmesi gibi bazı senaryolarda dikkatli kullanılmaları gerekir.
> 
> Hem merkezde hem de ölçek birimlerinde desteklenen belirli işlevler (*iş engelleme* gibi), yalnızca verilerin sahibi için desteklenir.

### <a name="outbound-supported-only-for-sales-and-transfer-orders"></a>Giden (yalnızca satış siparişleri ve transfer emirleri için desteklenir)

Aşağıdaki tablo, ambar yönetimi iş yükleri bulut ve uç ölçek birimlerinde kullanıldığında hangi giden özelliklerin desteklendiklerini ve bunların nerede desteklendiklerini gösterir.

| İşle                                                      | Hub | Ölçek biriminde ambar yürütme iş yükü |
|--------------------------------------------------------------|-----|------------------------------|
| Kaynak belge işleme                                   | Evet | Hayır |
| Yük ve taşıma yönetimini işleme                | Evet, ancak yalnızca yük planlama işlemleri. Taşıma yönetimi işlemi desteklenmez  | Hayır |
| Ambara serbest bırak                                         | Evet | Hayır |
| Planlanmış çapraz sevk                                        | Hayır  | Hayır |
| Sevkiyat konsolidasyonu                                       | Evet, yük planlamasını kullanırken | Evet |
| Sevkiyat dalgası işleme                                     | Hayır  |Evet, **Yük oluşturma ve sıralama** dışında |
| Dalga için sevkiyatları saklama                                  | Hayır  | Evet|
| Ambar iş işleme (plaka baskısı dahil)        | Hayır  | Evet, ancak yalnızca daha önce belirtilmiş desteklenen yetenekler için |
| Küme malzeme çekme                                              | Hayır  | Evet|
| "Sevk edilmiş konteyner çekme işlemi" işini işleme dahil elle ambalaj işleme | Hayır <P>Bazı işlemler, yalnızca ilk çekme işlemi ölçek birimi tarafından gerçekleştirildikten sonra yapılabilir ancak aşağıdaki engelli işlemler nedeniyle bu önerilmez.</p>  | Hayır |
| Konteyneri gruptan kaldır                                  | Hayır  | Hayır |
| Giden sıralama işleme                                  | Hayır  | Hayır |
| Yükle ilgili belgeleri yazdırma                           | Evet | Evet|
| Konşimento ve ASN üretimi                            | Hayır  | Evet|
| Sevkiyat onaylama                                             | Hayır  | Evet|
| "Onayla ve aktar" ile sevkiyat onayı            | Hayır  | Evet|
| Sevk irsaliyesi ve faturalama işlemleri                        | Evet | Hayır |
| Eksik malzeme çekme (satış siparişleri ve transfer emirleri)                    | Hayır  | Evet, kaynak belgeler için rezervasyonları kaldırmadan|
| Fazla malzeme çekme (satış siparişleri ve transfer emirleri)                     | Hayır  | Evet|
| İş yerleşimlerinin değiştirilmesi (satış siparişleri ve transfer emirleri)         | Hayır  | Evet|
| Tüm iş (satış siparişleri ve transfer emirleri)                    | Hayır  | Evet|
| İş raporunu yazdırma                                            | Evet | Evet|
| Dalga etiketi                                                   | Hayır  | Evet|
| İş bölme                                                   | Hayır  | Evet|
| İş işleme - "Taşıma yüklemesi" tarafından yönetilir            | Hayır  | Hayır |
| Çekilen miktarı düş                                       | Hayır  | Evet|
| İşi geri al                                                 | Hayır  | Evet|
| Sevkiyat onayını tersine çevir                                | Hayır  | Evet|

### <a name="inbound"></a>Gelen

Aşağıdaki tablo, ambar yönetimi iş yükleri bulut ve uç ölçek birimlerinde kullanıldığında hangi gelen özelliklerin desteklendiklerini ve bunların nerede desteklendiklerini gösterir.

| İşle                                                          | Hub | Ölçek biriminde ambar yürütme iş yükü<BR>*("Evet" olarak işaretlenmiş maddeler yalnızca ambar siparişleri için geçerlidir)* |
|------------------------------------------------------------------|-----|----------------------------------------------------------------------------------|
| Kaynak&nbsp;belge&nbsp;türü                             | Evet | Hayır |
| Yük ve taşıma yönetimini işleme                    | Evet | Hayır |
| Varış yeri maliyeti ve transitteki malları teslim alma                       | Evet | Hayır |
| Gelen sevkiyat onayı                                    | Evet | Hayır |
| Ambara satın alma siparişi serbest bırakma (ambar siparişi işleme) | Evet | Hayır |
| Ambar sipariş satırlarının iptali<p>Bunun yalnızca *iptal isteği* işlemi işlenirken satıra karşılık kayıt gerçekleştirilmediği durumlarda desteklendiğini unutmayın</p> | Evet | Hayır |
| Satınalma siparişi maddesini teslim alma ve yerine koyma                       | <p>Evet,&nbsp;ambar&nbsp;siparişi&nbsp;yoksa</p><p>Hayır, ambar siparişi olduğunda</p> | <p>Evet, satınalma siparişinin bir <i>yükün</i> parçası olmadığı durumlarda</p> |
| Satınalma siparişi satırı teslim alma ve yerine koyma                       | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | <p>Evet, satınalma siparişinin bir <i>yükün</i> parçası olmadığı durumlarda</p></p> |
| İade emri teslim alma ve yerine koyma                              | Evet | Hayır |
| Karma plaka alımı ve yerine koyma işlemi                       | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Evet |
| Yük maddesi teslim alma                                              | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Hayır |
| Plaka alma ve yerine koyma                             | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Hayır |
| Transfer emri maddesini teslim alma ve yerine koyma                       | Evet | Hayır |
| Transfer emri satırı teslim alma ve yerine koyma                       | Evet | Hayır |
| Çalışmayı iptal etme (gelen)                                            | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | <p>Evet, ancak yalnızca <b>İşi iptal ederken girişin kaydını sil</b> seçeneği (<b>Ambar yönetimi parametreleri</b> sayfasında) seçili olmadığında</p> |
| Satın alma siparişi ürün girişi işleme                        | Evet | Hayır |
| Eksik teslimat ile satınalma siparişi alma                      | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Evet, ancak yalnızca hub'dan iptal isteğinde bulunarak |
| Fazla teslimat ile satınalma siparişi alma                       | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Evet  |
| *Çapraz sevk* işinin oluşturulmasıyla alma                 | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Hayır |
| *Kalite emri* işinin oluşturulmasıyla alma                  | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Hayır |
| *Kalite maddesi örnekleme* işinin oluşturulmasıyla alma          | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Hayır |
| *Kalite denetiminde kalite* işinin oluşturulmasıyla alma       | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Hayır |
| Kalite emrinin oluşturulmasıyla alma                            | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | Hayır |
| İş işleme - *Küme yerine koyma* ile yönlendirilir                 | Evet | Hayır |
| *Eksik çekme* ile iş işleme                               | Evet | Evet |
| Plaka yükleme                                           | Evet | Evet |

### <a name="warehouse-operations-and-exception-handing"></a>Ambar işlemleri ve özel durum yönetimi

Aşağıdaki tablo, ambar yönetimi iş yükleri bulut ve uç ölçek birimlerinde kullanıldığında hangi ambar işlemleri ve özel durum yönetimi özelliklerinin desteklendiklerini ve bunların nerede desteklendiklerini gösterir.

| İşle                                            | Hub | Ölçek biriminde ambar yürütme iş yükü |
|----------------------------------------------------|-----|------------------------------|
| Plaka sorgusu                              | Evet | Evet                          |
| Madde sorgusu                                       | Evet | Evet                          |
| Konum sorgusu                                   | Evet | Evet                          |
| Ambarı değiştir                                   | Evet | Evet                          |
| Hareket                                           | Evet | Evet                          |
| Şablonla hareket                               | Evet | Evet                          |
| Ambar transferi                                 | Evet | Hayır                           |
| Ambar uygulamasından transfer emri oluşturma           | Evet | Hayır                           |
| Ayarlama (giriş/çıkış)                                | Evet | Evet, ancak stok ayarlama türlerindeki **Rezervasyonları kaldır** ayarı kullanılarak stok rezervasyonunun kaldırılması gereken bir ayarlama senaryosu için değil</p>                           |
| Stok durumu değişikliği                            | Evet | Hayır                           |
| Döngü sayma ve Sayma tutarsızlığı işleme | Evet | Evet                           |
| Plaka etiketini yeniden yazdırma (plakayı yeniden yazdır)             | Evet | Evet                          |
| Plaka yapısı                                | Evet | Hayır                           |
| Plaka bölme                                | Evet | Hayır                           |
| İç içe plakalar olarak paketle                                | Evet | Hayır                           |
| Sürücü girişi                                    | Evet | Hayır                           |
| Sürücü çıkışı                                   | Evet | Hayır                           |
| Toplu iş değerlendirme kodunu değiştirme                      | Evet | Evet                          |
| Açık iş listesini görüntüle                             | Evet | Evet                          |
| Plakaları birleştir                         | Evet | Hayır                           |
| Minimum/maksimum ve bölge eşiği stok yenileme işlemi| Evet <p>Sorguların parçası olarak aynı yerleşimleri eklememeniz önerilir</p>| Evet                          |
| Yerleştirme stok yenileme işleme                  | Evet  | Evet<p>Kurulumun ölçek biriminde gerçekleştirilmesi gerektiğini unutmayın</p>                           |
| İşi engelleme ve engellemeyi kaldırma                             | Evet | Evet                          |
| Kullanıcı değiştir                                        | Evet | Evet                          |
| İşteki iş havuzunu değiştirme                           | Evet | Evet                          |
| İşi iptal et                                        | Evet | Evet                          |

### <a name="production"></a>Üretim

Aşağıdaki tabloda, ambar yönetimi üretim senaryolarının hangilerinin şu anda ölçek birimi iş yüklerinde desteklendiği gösterilmektedir.

| İşle | Hub | Ölçek biriminde ambar yürütme iş yükü |
|---------|-----|------------------------------|
| Tamamlandı ve tamalanan ürünler kaldırıldı olarak bildirme | Evet | Evet |
| Yerine konan ortak ürün ve yan ürün | Evet | Evet |
| Üretim emrini başlat | Evet | Evet |
| <p>Üretimle ilgili diğer tüm ambar yönetim süreçleri, aşağıdakiler dahil olmak üzere:</p><li>Ambara serbest bırak</li><li>Üretim dalgası işleme</li><li>Hammadde çekme</li><li>Kanban yerine koyma</li><li>Kanban çekme</li><li>Üretim ıskartası</li><li>Üretimdeki son palet</li><li>Malzeme tüketimini kaydet</li><li>Kanban boş</li></ul> | Evet | Hayır |
| Hammadde stok yenilemesi | Hayır | Hayır |

## <a name="maintaining-scale-units-for-warehouse-execution"></a>Ambar yürütme için ölçek birimlerinin bakımı

Hem hub hem de ölçek birimlerinde birden çok toplu iş çalışır.

Hub dağıtımında toplu işleri el ile koruyabilirsiniz. **Ambar yönetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi**'nde aşağıdaki toplu işleri yönetebilirsiniz:

- Ölçek biriminden hub'a ileti işlemcisi
- Kaynak sipariş girişlerini kaydet
- Ambar siparişlerini tamamla

Ölçek birimlerindeki iş yükünde, **Ambar yönetimi \> Periyodik görevler \> İş yükü yönetimi**'nde aşağıdaki toplu işleri yönetebilirsiniz:

- Dalga tablosu kayıtlarını işleme
- Ambar hub'ından ölçek birimine ileti işlemcisi
- Ambar sipariş satırları için miktar güncelleştirme isteklerini işle

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
