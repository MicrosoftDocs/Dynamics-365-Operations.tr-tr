---
title: Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri
description: Bu konu, ölçek birimlerinin ambar yönetimi iş yükünden seçili işlemleri çalıştırmasını sağlayan özellik hakkında bilgi sağlar.
author: perlynne
manager: tfeyr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, SysSecRolesEditUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4ac76ad5cd88c35ac312b8e73d942a692f35c8aa
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516894"
---
# <a name="warehouse-management-workloads-for-cloud-and-edge-scale-units"></a>Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> İş yükü ölçek birimleri kullanıldığında, genel önizlemedeki iş işlevlerin tümü tam olarak desteklenmez. Yalnızca bu konunun açıkça desteklenen olarak tanımladığı işlemleri kullandığınızdan emin olun.

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

    - Stok hareketleri (şablon işiyle el ile hareket ve hareket)
    - Satın alma siparişleri (ambar siparişi ile işi yerine koyma)
    - Satış siparişleri (basit malzeme çekme ve yükleme işi)

- **Ambar sipariş girişi verileri**: Bu veriler yalnızca ambara el ile serbest bırakılan satın alma siparişleri için kullanılır.
- **Plaka verileri**: Plakalar hub ve ölçek biriminde oluşturulabilir. Özel çakışma yönetimi sağlanmıştır. Bu verilerin ambara özgü olmadığını unutmayın.

## <a name="outbound-process-flow"></a>Giden işleme akışı

Hub aşağıdaki verilere sahiptir:

- Satış siparişleri ve transfer emirleri gibi tüm kaynak belgeler
- Sipariş tahsisi ve giden yük işleme
- Ambar, sevkiyat oluşturma ve dalga oluşturma süreçlerine serbest bırakma

Ölçek birimleri, dalganın serbest bırakılmasından sonra gerçek dalga işlemenin (iş tahsisatı, stok yenileme işi ve talep işi oluşturma gibi) sahibidir. Bu nedenle, ambar çalışanları, ölçek birimine bağlı bir ambar uygulaması kullanarak giden işleri işleyebilir.

![Dalga işleme akışı](./media/wes_wave_processing_flow.png "Dalga işleme akışı")

## <a name="inbound-process-flow"></a>Gelen işlem akışı

Hub aşağıdaki verilere sahiptir:

- Satın alma siparişleri ve satış iade siparişleri gibi tüm kaynak belgeler
- Gelen ambar işleme

> [!NOTE]
> Gelen satın alma siparişi akışı, işlemi yapan ölçek biriminin siparişin bir ambara serbest bırakılıp bırakılmadığına bağlı olduğu giden akıştan kavramsal olarak farklıdır.

*Ambara serbest bırakma* kullanıyorsanız ambar siparişleri oluşturulur ve ilgili alıcı akışının sahipliği ölçek birimine atanır. Hub, gelen alıcıyı kaydedemez.

Çalışan, ölçek birimine bağlı bir ambar uygulamasını kullanarak teslim alma işlemini çalıştırabilir. Veriler daha sonra ölçek birimi tarafından kaydedilir ve gelen ambar siparişine göre raporlanır. Sonraki yerine koyma işlemlerinin oluşturulması ve işlenmesi de ölçek birimi tarafından yönetilir.

*Ambara serbest bırakma* işlemini kullanmıyorsanız ve bu nedenle *ambar siparişlerini* kullanmıyorsanız hub, ambar teslim alma işlemini ve iş işlemeyi ölçek birimlerinden bağımsız olarak işleyebilir.

![Gelen işlem akışı](./media/wes_Inbound_flow.png "Gelen işlem akışı")

## <a name="supported-processes-and-roles"></a>Desteklenen süreçler ve roller

Tüm ambar yönetimi süreçleri bir ölçek birimindeki WES iş yükünde desteklenmez. Bu nedenle, her kullanıcı için kullanılabilen işlevsellikle eşleşen roller atamanızı öneririz.

Bu işlemi kolaylaştırmak için **Sistem yönetimi \> Güvenlik \> Güvenlik yapılandırması**'ndaki demo verilerine *İş yükündeki ambar yöneticisi* adlı örnek bir rol dahildir. Bu rolün amacı, ambar yöneticilerinin ölçek biriminde WES'e erişmesini sağlamaktır. Rol, ölçek biriminde barındırılan bir iş yükü bağlamında ilgili sayfalara erişim sağlar.

Bir ölçek birimindeki kullanıcı rolleri, hub'dan ölçek birimine ilk veri eşitlemesi kapsamında atanır.

Bir kullanıcıya atanan rolleri değiştirmek için ölçek biriminde **Sistem yönetimi \> Güvenlik \> Kullanıcıları rollere atama** öğesine gidin. Yalnızca ölçek birimlerinde ambar yöneticisi olarak görev yapan kullanıcılara yalnızca *İş yükündeki Ambar yöneticisi* rolü atanmalıdır. Bu yaklaşım, bu kullanıcıların yalnızca desteklenen işlevselliğe erişmesini sağlayacaktır. Bu kullanıcılara atanan diğer rolleri kaldırın.

Hub ve ölçek birimlerinde ambar yöneticisi olarak görev yapan kullanıcılara var olan *Ambar çalışanı* rolü atanmalıdır. Bu rolün ambar çalışanlarına kullanıcı arabiriminde (Kullanıcı Arabirimi) görünen ancak şu anda ölçek birimlerinde desteklenmeyen özelliklere (transfer emri işleme gibi) erişim izni verdiğini unutmayın.

## <a name="supported-wes-processes"></a>Desteklenen WES süreçleri

Bir ölçek biriminde WES iş yükü için aşağıdaki ambar yürütme işlemleri etkinleştirilebilir:

- Satış siparişleri ve talep stok yenilemesi için seçilen dalga yöntemleri
- Depo uygulamasını kullanarak satış siparişlerinden iş emirlerinin ve talep stok yenilemesinin çalıştırılması
- Ambar uygulamasını kullanarak eldeki stoğu sorgulama
- Ambar uygulamasını kullanarak stok hareketleri oluşturma ve çalıştırma
- Ambar uygulamasını kullanarak satın alma siparişlerini kaydetme ve yerine koyma işi yapma

Aşağıdaki iş emri türleri şu anda ölçek birimi dağıtımlarında WES iş yükleri için desteklenir:

- Satış siparişleri
- Stok yenileme
- Stok hareketi
- Ambar siparişlerine bağlı satın alma siparişleri

Kaynak belgelerin başka hiçbir işlemesi, şu anda ölçek birimlerinde desteklenmez. Örneğin, bir ölçek birimindeki WES iş yükü için aşağıdaki eylemleri gerçekleştiremezsiniz:

- Transfer emrini serbest bırakma.
- Giden ambardan malzeme çekme ve sevkiyat işlemlerini gerçekleştirme.

> [!IMPORTANT]
> Bir ölçek biriminde iş yükü kullanıyorsanız hub'daki belirli ambar için desteklenmeyen işlemleri çalıştıramazsınız.

Aşağıdaki ambar yönetimi işlevi şu anda ölçek birimlerinde desteklenmemektedir:

- Etkin izleme boyutlarına sahip maddeler (toplu iş veya seri numarası boyutları gibi) için gelen ve giden işlemesi
- Stok durumu değişikliğiklerini işleme
- Engelleme durumu değeri olan stoğu işleme
- Kalite yönetimi ile tümleştirme
- Üretimle tümleştirme
- Fiili ağırlık maddelerini işleme
- Fazla teslimat ve yetersiz teslimatı işleme
- Negatif eldeki stoğu işleme

### <a name="outbound-supported-only-for-sales-orders-and-demand-replenishment"></a>Giden (yalnızca satış siparişleri ve talep stok yenileme için desteklenir)

Aşağıdaki tablo, ambar yönetimi iş yükleri bulut ve uç ölçek birimlerinde kullanıldığında hangi giden özelliklerin desteklendiklerini ve bunların nerede desteklendiklerini gösterir.

> [!WARNING]
> Yalnızca satış siparişi işleme desteklendiğinden, giden ambar yönetimi işlemleri transfer emirleri için kullanılamaz.
>
> Bazı ambar işlevleri, ambar yönetimi iş yüklerini ölçek biriminde çalıştıran ambarlarda kullanılamaz.

| İşle                                                      | Hub | Bir ölçek biriminde WES iş yükü |
|--------------------------------------------------------------|-----|------------------------------|
| Kaynak belge işleme                                   | Evet | No |
| Yük ve taşıma yönetimini işleme                | Evet | No |
| Ambara serbest bırak                                         | Evet | No |
| Sevkiyat konsolidasyonu                                       | No  | No |
| Merkezden dağıtım (malzeme çekme işi)                                 | No  | No |
| Sevkiyat dalgası işleme                                     | Hayır, ancak dalga durumunun kesinleşmesi hub'da işlenir |<p>Evet, ancak şu özellikler desteklenmez:</p><ul><li>Paralel iş oluşturma</li><li>Yük oluşturma ve sıralama</li><li>Konteyner Kullanımı</li><li>Dalga etiketi yazdırma</li></li></ul><p><b>Not:</b> Dalga işlemenin bir parçası olarak dalga durumunu sonuçlandırmak için hub'a erişim gereklidir.</p> |
| Ambar iş işleme (plaka baskısı dahil)     | No  | <p>Evet, ancak yalnızca şu özellikler için:</p><ul><li>Satış için malzeme çekme (etkin izleme boyutları kullanılmadan)</li><li>Satış yüklemesi (etkin izleme boyutları kullanılmadan)</li></ul> |
| Küme malzeme çekme                                              | No  | No |
| Ambalaj işleme                                           | No  | No |
| Giden sıralama işleme                                  | No  | No |
| Yükle ilgili belgeleri yazdırma                           | Evet | No |
| Konşimento ve ASN üretimi                            | Evet | No |
| Sevkiyat onayı ve sevk irsaliyesi işleme                | Evet | No |
| Eksik malzeme çekme (satış siparişleri)                                 | No  | No |
| İş iptali                                            | No  | No |
| İş konumlarının değiştirilmesi (satış siparişleri)                      | No  | No |
| Tam iş (satış siparişleri)                                 | No  | No |
| İşi engelleme ve engellemeyi kaldırma                                       | No  | No |
| Kullanıcı değiştir                                                  | No  | No |
| İş raporunu yazdırma                                            | No  | No |
| Dalga etiketi                                                   | No  | No |
| İşi geri al                                                 | No  | No |

### <a name="inbound"></a>Gelen

Aşağıdaki tablo, ambar yönetimi iş yükleri bulut ve uç ölçek birimlerinde kullanıldığında hangi gelen özelliklerin desteklendiklerini ve bunların nerede desteklendiklerini gösterir.

| İşle                                                          | Hub | Bir ölçek biriminde WES iş yükü |
|------------------------------------------------------------------|-----|------------------------------|
| Kaynak&nbsp;belge&nbsp;türü                                       | Evet | No |
| Yük ve taşıma yönetimini işleme                    | Evet | No |
| Sevkiyat onayı                                            | Evet | No |
| Ambara satın alma siparişi serbest bırakma (ambar siparişi işleme) | Evet | No |
| Satınalma siparişi maddesini teslim alma ve yerine koyma                        | <p>Evet,&nbsp;ambar&nbsp;siparişi&nbsp;yoksa</p><p>Hayır, ambar siparişi olduğunda</p> | <p>Evet, ambar siparişi olduğunda ve satın alma siparişi <i>yükün</i> parçası olmadığında. Ancak, yerine koymayı işlemek için biri teslim alma <i>(Satın alma siparişi madde teslim alma)</i> ve diğeri, <b>Var olan işi kullanma</b> seçeneği etkinleştirilmiş başka bir tane mobil cihaz menü öğeleri kullanılmalıdır.</p><p>Hayır, ambar siparişi olmadığında.</p> |
| Satınalma siparişi satırı teslim alma ve yerine koyma                        | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| İade emri teslim alma ve yerine koyma                               | Evet | No |
| Karma plaka alımı ve yerine koyma işlemi                        | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| Yük maddesi teslim alma                                              | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| Plaka alma ve yerine koyma                              | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |
| Transfer emri maddesini teslim alma ve yerine koyma                        | Evet | No |
| Transfer emri satırı teslim alma ve yerine koyma                        | Evet | No |
| İş iptali                                                | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | <p><b>Evet, ancak İşi iptal ederken girişin kaydını sil</b> seçeneği <b>(Ambar yönetimi parametreleri</b> sayfasında) desteklenmez.</p> |
| Satın alma siparişi ürün girişi işleme                        | Evet | No |
| Teslim almanın bir parçası olarak merkezden dağıtım işi oluşturma                 | <p>Evet, ambar siparişi olmadığında</p><p>Hayır, ambar siparişi olduğunda</p> | No |

### <a name="warehouse-operations-and-exception-handing"></a>Ambar işlemleri ve özel durum yönetimi

Aşağıdaki tablo, ambar yönetimi iş yükleri bulut ve uç ölçek birimlerinde kullanıldığında hangi ambar işlemleri ve özel durum yönetimi özelliklerinin desteklendiklerini ve bunların nerede desteklendiklerini gösterir.

| İşle                                            | Hub | Bir ölçek biriminde WES iş yükü |
|----------------------------------------------------|-----|------------------------------|
| Plaka sorgusu                              | Evet | Evet                          |
| Madde sorgusu                                       | Evet | Evet                          |
| Konum sorgusu                                   | Evet | Evet                          |
| Ambarı değiştir                                   | Evet | Evet                          |
| Hareket                                           | No  | Evet                          |
| Şablonla hareket                               | No  | Evet                          |
| Ayarlama (giriş/çıkış)                                | Evet | No                           |
| Döngü sayma ve Sayma tutarsızlığı işleme | Evet | No                           |
| Plaka etiketini yeniden yazdırma (plakayı yeniden yazdır)             | Evet | No                           |
| Plaka yapısı                                | Evet | No                           |
| Plaka bölme                                | Evet | No                           |
| Sürücü girişi                                    | Evet | No                           |
| Sürücü çıkışı                                   | Evet | No                           |
| Toplu iş değerlendirme kodunu değiştirme                      | Evet | No                           |
| Açık iş listesini görüntüle                             | Evet | No                           |
| Plakaları birleştir                         | No  | No                           |
| Konteyneri gruptan kaldır                        | No  | No                           |
| İşi iptal et                                        | No  | No                           |
| Min/maks stok yenileme işleme                   | No  | No                           |
| Yerleştirme stok yenileme işleme                  | No  | No                           |

### <a name="production"></a>Üretim

Üretim senaryoları için ambar yönetimi tümleştirmesi, aşağıdaki tabloda belirtildiği gibi şu anda desteklenmez.

| İşle | Hub | Bir ölçek biriminde WES iş yükü |
|---------|-----|------------------------------|
| <p>Üretimle ilgili tüm ambar yönetim süreçleri. Burada bazı örnekler verilmiştir:</p><li>Ambara serbest bırak</li><li>Üretim dalgası işleme</li><li>Hammadde çekme</li><li>Yerine konan mamul mallar</li><li>Yerine konan ortak ürün ve yan ürün</li><li>Kanban yerine koyma</li><li>Kanban çekme</li><li>Üretim emrini başlat</li><li>Üretim ıskartası</li><li>Üretimdeki son palet</li><li>Malzeme tüketimini kaydet</li><li>Kanban boş</li></ul> | No | No |

## <a name="maintaining-scale-units-for-wes"></a>WES için ölçek birimleri bakımı

Hem hub hem de ölçek birimlerinde birden çok toplu iş çalışır.

Hub dağıtımında toplu işleri el ile koruyabilirsiniz. **Ambar yönetimi \> Periyodik görevler \> Arka ofis iş yükü yönetimi**'nde aşağıdaki üç işi yönetebilirsiniz:

- İşleme işi durumu güncelleştirme olayları
- Dalga yürütme kontrolü transfer olaylarını işle
- Kaynak sipariş girişlerini kaydet

Ölçek birimlerindeki iş yükünde, **Ambar yönetimi \> Periyodik görevler \> İş yükü yönetimi**'nde aşağıdaki iki toplu işi yönetebilirsiniz:

- Dalga tablosu kayıtlarını işleme
- Dalga yürütme kontrolü transfer olaylarını işle


[!INCLUDE[footer-include](../../includes/footer-banner.md)]