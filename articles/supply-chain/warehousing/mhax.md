---
title: Malzeme işleme ekipmanı arabirimi (MHAX)
description: Bu konuda, harici fiziksel malzeme işleme (MH) sistemlerine bağlanabilmeniz için malzeme işleme ekipmanı arabiriminin (MHAX) nasıl ayarlanacağı açıklanmaktadır.
author: Mirzaab
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 9273e4a1f6b3f57086c921c4beb0530a67ccd976
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810522"
---
# <a name="material-handling-equipment-interface-mhax"></a>Malzeme işleme ekipmanı arabirimi (MHAX)

[!include [banner](../../includes/banner.md)]

Harici fiziksel malzeme işleme (MH) sistemlerini Microsoft Dynamics 365 Supply Chain Management'ta gelişmiş ambar yönetimi (WMS) tarafından yönetilen bir ambara bağlamak için *malzeme işleme ekipmanı arabirimini* (MHAX) kullanabilirsiniz. WMS ve MH sistemleri arasındaki arabirim iki kuyruktan oluşur: biri giden olaylar (WMS'den MH'ye) ve diğeri gelen olaylar için (MH'den WMS'ye). WMS sistemi, çeşitli iş oluşturma ve yürütme işlemleri sırasında oluşturulan iş satırlarına dayalı giden olaylar oluşturur. MH sistemi daha sonra WMS sistemini düzenli olarak yeni olaylar için yoklar ve yanıtları işler. MH sistemi olayları iş talimatlarına uygun olarak işlemeyi tamamladıktan sonra, iş satırının tamamlanması ve kısa malzeme çekme gibi gelen olayları gönderir.

Aşağıdaki şekilde, MHAX tümleştirmesini kullandığınızda çeşitli maddeler ve işlemlerin gerçekleşme kuyruğu gösterilir.

![MHAX bileşenleri ve etkileşimler](media/mhax-components.png "MHAX bileşenleri ve etkileşimler")

Önceki çizimde gösterilen etkileşimlerin bir açıklaması aşağıdadır:

1. İş oluşturma veya iş yürütme sırasında, giden kuyruğunda giden olaylar oluşturulur.
2. MH ekipmanı, MH ekipman hizmetine bağlanır, onunla ilgili yeni olayları yoklar ve bu olayları işler.
3. MH ekipmanı geri bildirmeye hazır olduğunda, hizmete tekrar bağlanır ve gelen olayları gönderir. Bu olaylar sıra işlemcisi tarafından hemen işlenir.
4. Gelen olay verilerine bağlı olarak, kuyruk işlemcisi var olan çalışmayı çalıştırabilir, değiştirebilir veya yeni çalışma oluşturabilir.

## <a name="turn-on-the-mhax-feature"></a>MHAX özelliğini açma

MHAX özelliğini kullanabilmeniz için önce hem özelliği hem de yapılandırma anahtarını açmanız gerekir.

1. **Sistem yönetimi \> Çalışma alanları \> Özellik yönetimi**'ne gidin.
2. **[Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** çalışma alanında, *Malzeme işleme ekipmanı arabirimi* adlı özelliği açın.
3. Sisteminizi [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım moduna alın.
4. **Sistem yönetimi \> Kurulum \> Lisans yapılandırma** seçeneğine gidin.
5. **Ticaret \> Ambar ve Taşıma yönetimi**'ni genişletin ve **malzeme işleme ekipmanı arabirimi** onay kutusunu seçin.
6. [Bakım modu](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) bölümünde anlatıldığı şekilde bakım modunu kapatın.

## <a name="set-mhax-parameters"></a>MHAX parametrelerini ayarlama

Özelliği yapılandırmak için **Malzeme işleme ekipmanı arabirim parametreleri** sayfasında birkaç genel parametre ayarlamanız gerekir.

1. **Malzeme işleme ekipmanı arabirimi \> Kurulum \> Malzeme işleme ekipmanı arabirimi parametreleri**'ne gidin.
2. **Genel** sekmesinde, aşağıdaki alanları ayarlayın:

    - **Kullanıcı Kimliği**: Bir çalışan seçin. Bu çalışan, gelen kuyruğu aracılığıyla işlenen tüm iş operasyonlarını (malzeme çekmeler ve yerine koymalar) çalıştırmak için kullanılır.
    - **Gelen ileti kimliğini etkinleştir**: Bu seçenek *Evet* olarak ayarlandığında, yinelenen bir gelen ileti kimliği alınırsa ileti reddedilir ve bir hata iletisi iletinin zaten var olduğunu belirtir. Bu seçenek *Hayır* olarak ayarlandığında, yinelenen gelen ileti kimliklerine izin verilir.

3. **Numara serileri** sekmesinde, gelen kuyruğu maddeleri, giden kuyruğu maddeleri ve iş satırı çiftleri için benzersiz kimlikler oluşturmak üzere kullanılması gereken sistem genelindeki numara serilerini seçin.

## <a name="outbound-events"></a>Giden olaylar

İş oluşturma veya çalışma yürütme sırasında belirli noktalarda, sistem MH sistemine göndermek için giden olaylar oluşturması gerekip gerekmediğini belirler. Bir abonelik ambar işleme sırasında belirli bir nokta için yapılandırılmışsa sistem aboneliğin kurulumuna göre olayı oluşturur.

### <a name="structure-of-outbound-events"></a>Giden olayların yapısı

Her giden olay, giden kuyruğu kimliği tarafından benzersiz olarak tanımlanır. Giden hareket türü olayın türünü belirler. Ambar ve olayı oluşturan aboneliğin kimliği de olaya kaydedilir.

MH sistemine veri taşımak için giden olay, veriler için 10 alan içerir **(data01** - **data10**). Bu veri alanlarının var olan veritabanı alanlarıyla bire bir (1:1) eşlemesi vardır. Özellikle, iş satırı ve iş başlığı tablolarındaki alanlardan ayıklanırlar. Alanlar serbestçe seçilebilir. Bunları, aboneliği oluştururken ayarlarsınız.

Var olan veritabanı alanlarıyla 1:1 eşlemesi olan 10 veri alanının yanı sıra, olay, *yük* olarak bilinen ek bir veri alanı içerebilir. Bu alanın içeriği, *yük oluşturucu* olarak bilinen özel X++ kodu tarafından oluşturulur. Kullanılması gereken tüm yük oluşturucular abonelikte ayarlanır.

MH sisteminin her giden kuyruğu kimliğini yalnızca bir kez aldığından emin olmak için bir olayın dış sisteme gönderilmeye hazır olup olmadığını veya zaten gönderilip gönderilmediğini belirtmek için bir durum alanı kullanılır.

### <a name="outbound-queue-subscriptions"></a>Giden kuyruğu abonelikleri

Herhangi bir olay oluşturulmadan önce, MHAX özelliğine olayların oluşturulup oluşturulmayacağını ve nasıl oluşturulacağını söylemek için bir abonelik ayarlanmalıdır. Oluşturulan olaylar abonelik tanımlayıcısı tarafından etiketlenir. Bu nedenle, birden çok MH sistemi aynı WMS sistemine bağlanabilir ancak olaylarını ayrı tutabilir. MHAX hizmeti yeni olaylar için yoklandığında, abonelik olayları almak için kullanılabilir seçeneklerden biridir.

Abonelik oluşturmak için **Malzeme işleme ekipmanı arabirimi \> Kurulum \> Abonelikler**'e gidin. Her abonelik için aşağıdaki parametreler kullanılabilir:

- **Abonelik Kimliği**: Aboneliği tanımlayan benzersiz bir ad.
- **Açıklama**: Aboneliğin serbest metin açıklaması.
- **Ambar**: Olayların filtrelemesi gereken belirli ambarlar.
- **Giden hareket türü**: Aboneliğin içermesi gereken olayların türü.
- **Yük oluşturucu**: Giden olayın **Yük** alanına ek bilgi girebilen isteğe bağlı bir kod uzantısı.

Her abonelikle bir sorgu ilişkilendirilebilir. Bu sorgu, olayları oluşturmak için aboneliği kullanacak işi daha da sınırlamak üzere iş satırlarını ve başlıklarını filtreler. Aboneliğe sorgu eklemek için **Abonelikler** sayfasında ilgili aboneliğin **Sorguyu çalıştır** onay kutusunu seçin ve ardından Eylem Bölmesinde **Sorguyu düzenle**'yi seçin. Standart Supply Chain Management sorgu düzenleyicisi görüntülenir.

Buna ek olarak abonelik, alanları iş başlığından veya iş satırından, gerektiğinde giden olayın 10 boş veri alanının bir kısmına veya tümüne eşleşen bir *abonelik eşlemesi* içerir. MHAX hizmetine bilgi döndürmek için genellikle iş satırı kayıt kimliği veya *iş satırı çift kimliği* eklenir. (İş satırı çifti kimliği, sistemin malzeme çekme ve yerine koyma satırlarını işlemek için tek bir dönüş komutu kullanmasını sağlayan yeni bir özelliktir.) Kalan alanlar kullanım örneğine bağlıdır. Bu konunun ilerleyen bölümlerinde bazı örnekler verilmiştir.

Abonelik eşlemesi ayarlamak için **Abonelikler** sayfasında ilgili aboneliği seçin ve ardından Eylem Bölmesinde **Abonelik eşlemesi**'ni seçin. Görüntülenen **Abonelik eşlemesi** iletişim kutusunda, kullanılabilir her veri alanı için istediğiniz gibi bir tablo ve alan atayabilirsiniz.

### <a name="outbound-event-types"></a>Giden olay türleri

Bu bölümde, kullanılabilen çeşitli olay türleri açıklanmaktadır. (Olay türleri *hareket türleri* olarak da bilinir.) Ayrıca, her olay türünün WMS sisteminde ne zaman oluşturulduğunu açıklar.

#### <a name="work-creation-events"></a>İş oluşturma olayları

İş oluşturma olayları, uygulama tarafından iş oluşturulduktan sonra oluşturulur. Bu davranış, özellikle malzeme çekme ve stok yenileme çalışmalarının oluşturulması için olmak üzere, çoğu iş oluşturma işlemi türü için geçerlidir. Genel olarak, çalışma bir çalışan tarafından çalıştırılmaya hazır olduğunu gösteren bir *Açık* durumda oluşturulursa bir iş oluşturma olayı oluşturulur. Buna ek olarak, çalışma açık çalışma olarak oluşturulmasa bile, temel taşıma çalışmaları (şablon çalışmasına göre hareket değil) için iş oluşturma olayları oluşturulur.

Bu davranışın önemli bir istisnası, şu anda desteklenmeyen döngü sayma çalışmasıdır. MH sistemindeki stok sayımları MHAX kapsamı dışındadır ve sayımların sonuçları bir stok sayım günlüğüne aktarılmalıdır.

İş oluşturulduktan sonra, MHAX hizmeti oluşturulan iş satırlarını işler ve her iş başlığı için oluşturulan tüm iş satırlarına bir iş satırı çift kimliği atar. Amaç, tüm malzeme çekme iş satırlarını bir iş satırı çift kimliği altında ardışık yerine koymalarla gruplandırmaktır. (Gruplar, iş şablonlarındaki malzeme çekme/yerine koyma çiftlerine karşılık gelir.) Bu şekilde, ilgili tüm malzeme çekme ve yerine koyma satırları için iş tamamlamayı raporlamak için tek bir kimlik kullanılabilir. Gruplandırma işlemi ilk satırla başlar ve sonra ardışık bir yerine koyma/malzeme çekme iş satırı çiftiyle karşılaşana kadar aynı kimlikle devam eder. Çalışan kimlik, bu çiftin yerine koyma satırına atanır. Daha sonra çiftin malzeme çekme satırına yeni bir kimlik atanır. Bu işlem, iş başlığına ait tüm satırları işleyene kadar devam eder.

İş oluşturma olaylarının özel bir özelliği olarak iş başlığında **Engellenen dalga** seçeneği *Evet* olarak ayarlanırsa oluşturulan olaylar, bunları MH sistemine göndermek için kullanılan *Hazır* durumu yerine *Engellendi* durumuna sahip olur. İş başlığındaki **Engellenen dalga** bayrağı, çalışma başlığının, belki de tamamlanmamış stok yenileme çalışmaları nedeniyle çalışanların çalışması için henüz hazır olmadığını gösterir. **Engellenen dalga** bayrağı temizlendiğinde, zaten oluşturulmuş olan olayların engeli kaldırılır ve MH sisteminin sıradan alması için kullanılabilir.

#### <a name="work-initiation-events"></a>İş başlatma olayları

İş başlatma olayları, iş güncelleştirmesi sırasında iş durumu *Açık*'tan *Devam ediyor*'a değiştiğinde tetiklenir.

#### <a name="work-completion-events"></a>İş tamamlama olayları

İş güncelleştirme sırasında iş durumu *Devam ediyor*'dan *Kapalı*'ya değiştiğinde iş tamamlama olayları tetiklenir.

#### <a name="work-cancellation-events"></a>İş iptali olayları

İş iptali olayları, iş durumu iş güncelleştirmesi sırasında *İptal Edildi* dışında bir durumdan *İptal Edildi*'ye değiştiğinde tetiklenir. Ayrıca, iş başlığı ile ilgili diğer tüm olaylar tüm abonelikler için kuyruktan silinir. Bu şekilde, harici sistemlerin gerekli olmayan olayları işlemesi engellenir.

#### <a name="pickput-completion-events"></a>Malzeme çekme/yerine koyma tamamlama olayları

Malzeme çekme/yerine koyma tamamlama olayları, iş satırı güncelleştirmesi sırasında malzeme çekme/yerine koyma satırının durumu *Devam ediyor*'dan *Kapalı*'ya değiştiğinde tetiklenir.

### <a name="monitor-the-outbound-queue"></a>Giden kuyruğunu izleme

Giden kuyruğunuzu gözden geçirmek için **Malzeme işleme ekipmanı arabirimi \> Ortak \> Giden kuyruğu**'na gidin. **Giden kuyruğu** sayfası, her giden kuyruğu öğesini ve durumunu listeler. Ayrıntılarını görüntülemek için bir kuyruk maddesi seçin. Bu ayrıntılar, maddenin hareket türünü, kullandığı aboneliği ve her veri alanı için değerleri **(data01** - **data10)** ve yükü içerir.

### <a name="clean-up-the-outbound-queue"></a>Giden kuyruğunu temizleme

Son olarak, giden kuyruğunuz zaten gönderilmiş kuyruk maddeleriyle dolmaya başlar. Bu maddeleri kaldırmak için **Malzeme işleme ekipmanı arabirimi \> Periyodik görevler \> Temizleme \> Giden kuyruğunu temizle**'ye gidin.

## <a name="inbound-events"></a>Gelen olaylar

Bu bölümde, MH sisteminin WMS sistemine geri bildirebileceği çeşitli gelen olay türleri açıklanmaktadır. Ayrıca, verilerin MH sistemi tarafından sağlanması gerektiğini ve her gelen olayın WMS sisteminde ne yaptığını açıklar.

### <a name="structure-of-inbound-events"></a>Gelen olayların yapısı

Gelen olay gönderildiğinde, dış sistemin gelen işlem türünü en fazla 10 parametreyle **(data01** - **data10)** birlikte sağlaması gerekir. İsteğe bağlı doğrulama, MHAX hizmetinin aynı gelen olayı birden fazla kez almadığından emin olabilir. Bu doğrulamayı etkinleştirmek için her gelen olayın benzersiz bir ileti kimliği olmalıdır. Yinelenen bir ileti kimliği alınırsa ve **Malzeme işleme ekipmanı arabirim parametreleri** sayfasında **Gelen ileti kimliği etkinleştir** seçeneği *Evet* olarak ayarlıysa ileti reddedilir. Bir hata iletisi, iletinin zaten var olduğunu belirtir.

Gelen veri alanlarına ek olarak sistem olaya benzersiz bir gelen kuyruğu kimliği atar.

### <a name="inbound-event-types"></a>Gelen olay türleri

Bu bölümde, desteklenen gelen olay türleri (hareket türleri) ve olayların işlenmesi için sağlanması gereken veriler açıklanmaktadır.

#### <a name="work-confirm-events"></a>İş onaylama olayları

İş onaylama olayları, gelen veri alanlarının aşağıdaki bilgileri içermesini gerektirir:

- **data01**: İş satırı çifti kimliği.
- **data02**: İş satırı kaydı kimliği (`RecId` değeri).

    > [!NOTE]
    > **data01** alanı *veya* **data02** alanından *biri* bulunmalıdır.

- **data03**: Seçim yapılacak plakanın kimliği.
- **data04**: İş başlığının hedef plaka kimliği.

İş satırı çifti kimliği sağlanmışsa iş satırı çifti kimliğiyle işaretlenmiş ve durumu *Açık* veya *Devam ediyor* olan tüm malzeme çekme, yerine koyma veya özel iş satırları sırayla çalıştırılır. Bir iş satırı kaydı kimliği (`RecId` değeri) sağlanmışsa iş satırı *Açık* veya *Devam ediyor* durumuna sahip bir malzeme çekme, yerine koyma veya özel iş satırı olmalıdır.

Plaka kontrollü konumlardan malzeme çekme satırları, satırların iş satırı kaydı kimliği veya iş satırı çifti kimliği ile işaretlenip işaretlenmediğine bakılmaksızın, **data03**'ün çekilmesi gereken plakayı belirtmesi gerekir. **data04** alanında, malzeme çekme için iş başlığının hedef plakası belirtilmelidir.

Yerine koyma satırları daha fazla bilgi kabul etmez. Bunlar yalnızca geçerli iş satırının konumuna ve işin hedef plakasına göre çalıştırılır. Yerine koymanın farklı bir konuma yapılması gerekiyorsa bu konunun sonraki bölümlerindeki [Geçersiz kılma olayları](#override-events) bölümünde açıklandığı gibi iş satırının konumunu değiştirin.

Özel iş satırları, gelen olayda herhangi bir ek bilgi gerektirmez veya desteklemez.

#### <a name="short-pick-events"></a>Kısa malzeme çekme olayları

Kısa malzeme çekme olayları, gelen veri alanlarının aşağıdaki bilgileri içermesini gerektirir:

- **data02**: İş kaydı kimliği (`RecId` değeri).
- **data03**: Seçim yapılacak plakanın kimliği.
- **data04**: Çekilecek miktar.
- **data05**: Kısa malzeme çekme özel durum kodu.
- **data06**: İş başlığının hedef plaka kimliği.

> [!NOTE]
> **data01** alanı kısa malzeme çekme olayları için kullanılmaz.

Bu olay iş onayı olayına benzerdir ancak yalnızca malzeme çekme satırları için geçerlidir.

#### <a name="override-events"></a><a id="override-events"></a>Geçersiz kılma olayları

Geçersiz kılma olayları, gelen veri alanlarının aşağıdaki bilgileri içermesini gerektirir:

- **data01**: İş kaydı kimliği (`RecId` değeri).
- **data02**: Yeni konum kimliği.

İş satırının durumu *Açık* veya *Devam ediyor* olmalıdır ve yeni konum bulunmalıdır.

#### <a name="license-plate-receipt-events"></a>Plaka girişi olayları

Plaka girişi olayları, gelen veri alanlarının aşağıdaki bilgileri içermesini gerektirir:

- **data01**: Alınacak gelen plakanın kimliği.

Sistem, **data01** alanının değeri olarak geçirilen plakaya göre bir plaka alma işlemi gerçekleştirir.

### <a name="monitor-the-inbound-queue"></a>Gelen kuyruğunu izleme

Gelen kuyruğunuzu gözden geçirmek için **Malzeme işleme ekipmanı arabirimi \> Ortak \> Gelen kuyruğu**'na gidin. **Gelen kuyruğu** sayfası, her gelen kuyruğu öğesini ve durumunu listeler. Ayrıntılarını görüntülemek için bir kuyruk maddesi seçin. Bu ayrıntılar, maddenin hareket türünü, ileti kimliğini ve her veri alanı için **(data01** - **data10)** değerleri içerir.

Gelen olaylar işlenirken bir hata veya başka bir günlük öğesi türü oluştuysa Eylem Bölmesinde **Hata günlüğü**'nü seçerek günlüğü inceleyebilirsiniz.

### <a name="inbound-event-processing"></a>Gelen olayı işleme

Gelen olaylar önce veritabanına yazılır ve daha sonra hemen (zaman uyumlu olarak) çalıştırılır. İşlem sırasında bir hata oluşursa olay yine de kuyruğa yazılır ancak durum *Hata verdi* olarak ayarlanır. MHAX hizmeti MH sistemine bir hata iletisi döndürür ve hata günlüğünü daha sonra araştırılmak üzere gelen olay kaydında depolar.

Hata durumu düzeltilirse *Hata verdi* durumuna sahip olaylar daha sonra yeniden işlenebilir. Bu olayları yeniden işlemek için şu adımlardan birini izleyin:

- **Malzeme işleme ekipmanı arabirimi \> Ortak \> Gelen kuyruğu**'na gidin. İlgili gelen kuyruğunu seçin ve ardından Eylem Bölmesinde **Yeniden İşle**'yi seçin.
- **Malzeme işleme ekipmanı arabirimi \> Ortak \> Hatalı gelen kuyruğunu yeniden işle**'ye gidin. Standart bir toplu işlem iletişim kutusu görüntülenir. Burada, bir kayıt filtresi ayarlayabilir ve kuyruğu yeniden işleyebilmek için bir toplu işlem planlayabilir ya da çalıştırabilirsiniz.

Tüm iş operasyonları (malzeme çekmeler ve yerine koymalar), **Malzeme işleme ekipmanı arabirimi parametreleri** sayfasındaki **Kullanıcı Kimliği** alanında seçilen çalışan kullanılarak çalıştırılır.

### <a name="clean-up-the-inbound-queue"></a>Gelen kuyruğunu temizleme

Son olarak, gelen kuyruğunuz zaten işlenmiş kuyruk maddeleriyle dolmaya başlar. Bu maddeleri kaldırmak için **Malzeme işleme ekipmanı arabirimi \> Periyodik görevler \> Temizleme \> Gelen kuyruğunu temizle**'ye gidin.

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Kuyruk yöneticisini kullanarak hızlı bir genel bakış elde etme

Gelen ve giden kuyruklarınızla ilgili tüm etkinliklere hızlı bir genel bakış elde etmek için **Malzeme işleme ekipmanı arabirimi \> Çalışma Alanları \> Kuyruk yöneticisi**'ne gidin. **Kuyruk yöneticisi** sayfası, kuyruklarınızı izlemek ve keşfetmek için kullanabileceğiniz sekmeler ve kutucuklar kümesi sağlar. Ayrıca, bu konuda bahsedilen diğer sayfaların çoğunun yararlı bağlantılarını sağlar.

## <a name="connect-to-the-mhax-service"></a>MHAX hizmetine bağlanma

MHAX özel bir hizmet olarak uygulanır. Bu nedenle, SOAP ve REST çağrıları aracılığıyla erişilebilir. SOAP ve REST uç noktalarının adresleri şunlardır:

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Giden kuyruğundan ileti alma

Giden kuyruğundan ileti almak için aşağıdaki yöntemlerden birini kullanın:

- Abonelik kimliğine göre olayları almak için `readOutboundSubscriptionQueue` kullanın.
- Birden çok abonelikte olay türüne ve ambar kimliğine göre olayları almak için `readOutboundWarehouseQueue` kullanın.
