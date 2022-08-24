---
title: Küme konumu dolu
description: Bu makalede, Küme konumu dolu özelliğiyle ilgili bilgiler verilir. Bu özellik, küme malzeme çekme kullanılırken iş kesme kuralına ait daha katı zorlamaya olanak sağlayan bir alternatif sunar, çünkü konteyner ve sepetlerin hacimleri ile ilişki kısıtlamalarda daha büyük hata marjlarına olanak sağlar.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9361448ba7993ba7cc126d6dd60a45fe497b2e84
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218787"
---
# <a name="cluster-position-full"></a>Küme konumu dolu

[!include [banner](../includes/banner.md)]

*Küme konumu dolu* özelliği, küme malzeme çekme kullanılırken iş kesme kuralına ait daha katı zorlamaya olanak sağlayan bir alternatif sunar, çünkü kapsayıcı ve sepetlerin hacimleri ile ilişki kısıtlamalarda daha büyük hata marjlarına olanak sağlar. Ortak bir senaryoda, bir iş emrindeki tüm öğeler seçili bir kapsayıcıya sığmıyor. Küme malzeme çekme iş yapan ambar çalışanları bu senaryoda birkaç seçeneğe sahiptir: Ya daha büyük bir kapsayıcı boyutuna geçmeli ya da farklı bir çözüm bulmak için gözetmen ile çalışmalıdır.

Bu özellik, bir kümedeki çalışma birimlerinden birinde **Dolu** düğmesinin çalıştırılmasını sağlar. Eski sürümlerde bu seçenek, küme çekmede değil, yalnızca normal sipariş çekmesinde kullanılabiliyordu. Ancak, bu özellik kalan çalışmayı iptal eden standart **Dolu** düğmesinden farklıdır. Kullanıcının aynı kümeye başka bir bölme eklemesini önermez ve otomatik olarak yeni bir iş oluşturmaz.

## <a name="turn-the-cluster-position-full-feature-on-or-off"></a>Küme konumu dolu özelliğini açma veya kapatma

Bu makalede açıklanan işlevi kullanmak için *Küme konumu dolu* özelliğinin sisteminizde etkinleştirilmiş olması gerekir. Supply Chain Management 10.0.25 itibarıyla, bu özellik zorunludur ve kapatılamaz. 10.0.25 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Küme konumu dolu* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

## <a name="setup"></a>Kurulum

Bu bölümde, yönergeler ile *küme konumu dolu* özelliğinin nasıl ayarlanacağını ve kullanılacağını gösteren bir örnek verilmiştir.

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada belirtilen örnek kayıtları ve değerleri kullanarak [örnek senaryo](#example-scenario) üzerinden çalışmak için standart [demo verilerinin](../../fin-ops-core/fin-ops/get-started/demo-data.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

Örnek senaryodan, üretim sisteminde özelliği kullanmaya yönelik kılavuz olarak da yararlanabilirsiniz. Ancak, bu durumda, burada açıklanan her ayar için kendi değerlerinizi kullanmanız gerekir.

### <a name="cluster-profiles"></a>Küme profilleri

Küme kimliklerinin otomatik olarak oluşturulup oluşturulmayacağını, kaç pozisyonda kullanılacağını, kümelerin ne zaman kesileceğini ve malzeme çekme çalışmasının nasıl sıralandığını ve doğrulanacağını belirtmeniz gerekir.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Küme profilleri**'ne tıklayın.
1. Liste bölmesinde, **Küme Oluştur**'u seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki değerleri doğrulayın:

    - **Küme kimliği oluştur:** *Evet*
    - **Pozisyonları etkinleştir:** *Evet*
    - **Pozisyon sayısı:** *2*
    - **Pozisyon adı:** *Sayısal*
    - **Kümeyi böl:** *Yerine koy*
    - **Sıralama doğrulama türü:** *Pozisyon taraması*

1. **Küme sıralama** hızlı sekmesinde. Kılavuz boş olmalıdır (başka bir deyişle, hiçbir satır içermemelidir).

### <a name="work-templates"></a>İş şablonları

Küme malzeme çekme için çekme işinin nasıl oluşturulacağını tanımlamanız gerekir.

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. Sayfanın üst kısmında, **İş emri türü** alanını *Satış siparişleri* olarak ayarlayın.
1. Demo verilerinden alınan aşağıdaki çalışma şablonlarının listelendiğinden emin olun. Kullanılabilir değillerse, senaryoyu tamamlayamazsınız.

    - 61 Satış Siparişi Hazırlama
    - 61 Satış Siparişi Küme malzeme çekme

### <a name="location-directives"></a>Konum yönergeleri

Maddelerin nereden çekildiklerini ve nereye koyulacağını belirtmeniz gerekir.

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Liste başlığında **İş emri türü** alanını *Satış siparişleri* olarak ayarlayın.
1. Demo verilerinden alınan aşağıdaki satış yönergelerinin listelendiğinden emin olun. Kullanılabilir değillerse, senaryoyu tamamlayamazsınız.

    - 61 Küme malzeme çekme
    - 61 Satış Siparişi Malzeme çekme emri

### <a name="mobile-device-menu-items"></a>Mobil cihaz menü öğeleri

Küme malzeme çekme tarafından yönlendirilen mevcut işi kullanmak için bir mobil cihaz menü öğesini yapılandırmanız gerekir. Küme malzeme çekme işlemi için mobil cihaz menü öğesinde, **İşin bölünmesine izin ver** parametresi açık olmalıdır ve *Satış Siparişi Malzeme Çekme* iş sınıfı eklenmelidir.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Liste bölmesinde, **Küme Malzeme Çekme Oluştur** kaydını seçin.
1. Eylem bölmesinde, **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Yöneten:** *Küme malzeme çekme*
    - **Plaka oluştur:** *Evet*
    - **İşin bölünmesine izin ver:** *Evet*
    - **Küme profili kimliği:** *Küme oluştur*

    Tüm diğer alanlar için varsayılan değerleri kabul edin.

1. **İş sınıfları** hızlı sekmesinde, gerektiğinde aşağıdaki iki satırı ekleyin:

    - Satır 1 (genellikle demo verilerinde vardır):

        - **İş sınıfı kodu:** *Satış* 
        - **İş emri türü:** *Satış siparişleri*

    - Satır 2 (demo verilerinde olmayabilir):

        - **İş sınıfı kodu:** *Satış Siparişi Çekme*
        - **İş emri türü:** *Satış siparişleri*

1. Eylem bölmesinde **İş onayı kurulumu** bölümüne gidin.
1. **Düzenle** öğesini seçin.
1. Kılavuzda satıra aşağıdaki değerleri girin.
    - **İş türü** - *Çekme*
    - **Ürün onayı** - *Onay kutusunu seç*

1. Eylem bölmesinde **Kaydet**'i seçin ve sayfayı kapatın.

## <a name="create-picking-work"></a>Malzeme çekme işi oluştur

Küme çekmeyi başlatabilmeniz için önce, bazı çıkış çalışmaları oluşturmanız gerekir. Daha önce oluşturduğunuz küme profilinde iki küme konumu belirtilir. Bu nedenle, satış siparişi çekme için en az iki iş kodu oluşturulmalıdır. Bu senaryoda, ambar *61*'de hareketler gerçekleşir ve bunlar *L0101* ve *T0100* öğelerini kullanır. Demo verilerinde bu maddelerin elde yeterli miktarda stokunun bulunması gerekir. Hareketleri tamamlamak için yeterli stokunuzun bulunduğundan emin olun.

### <a name="create-sales-order-1"></a>Satış siparişi oluşturma 1

1. **Satış ve Pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Satış siparişi 1'i oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-010*
    - **Ambar:** *61*

1. **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Madde numarası:** *T0100*
    - **Miktar:** *5*

1. **Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde **Onaylanan sevkiyat tarihi** alanını bugünün tarihine ayarlayın.
1. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip ikinci satırı ekleyin:

    - **Madde numarası:** *L0101*
    - **Miktar:** *20*

1. **Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde **Onaylanan sevkiyat tarihi** alanını bugünün tarihine ayarlayın.
1. Yeni eklediğiniz her satır için, stoku rezerve etmek üzere aşağıdaki adımları izleyin:

    1. Rezerve edilecek satırı seçin.
    2. **Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.
    3. **Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.
    4. **Rezervasyon** sayfasını kapatın.

1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Serbest bırakma işlemi tamamlanınca oluşturulan dalga kimliğini ve yük kimliklerini gösteren bilgi iletileri alırsınız.

### <a name="create-sales-order-2"></a>Satış siparişi oluşturma 2

1. **Satış ve Pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Satış siparişi 2'i oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-011*
    - **Ambar:** *61*

1. **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:

    - **Madde numarası:** *L0101*
    - **Miktar:** *20*

1. **Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde **Onaylanan sevkiyat tarihi** alanını bugünün tarihine ayarlayın.
1. **Satış siparişi satırları** hızlı sekmesinde, aşağıdaki ayarlara sahip ikinci satırı ekleyin:

    - **Madde numarası:** *T0100*
    - **Miktar:** *2*

1. **Satır ayrıntıları** hızlı sekmesinin **Teslimat** sekmesinde **Onaylanan sevkiyat tarihi** alanını bugünün tarihine ayarlayın.
1. Yeni eklediğiniz her satır için, stoku rezerve etmek üzere aşağıdaki adımları izleyin:

    1. Rezerve edilecek satırı seçin.
    2. **Satış siparişi satırları** hızlı sekmesinde **Stok \> Rezervasyon**'u seçin.
    3. **Rezervasyon** sayfasında, Eylem Bölmesi'nde stok rezerve etmek için **Lotu rezerve et**'i seçin.
    4. **Rezervasyon** sayfasını kapatın.

1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Serbest bırakma işlemi tamamlanınca oluşturulan dalga kimliğini ve yük kimliklerini gösteren bilgi iletileri alırsınız.

### <a name="get-work-ids-and-license-plate-numbers"></a>İş kimliklerini ve plaka numaralarını alma

Her biri iki çekme satırı içeren iki iş kodu oluşturulmalıdır. İş kimliklerini ve plaka atamalarını bulmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. **Genel Bakış** kılavuzunda, az önce oluşturduğunuz iki satış siparişi için **Sipariş numarası** sütununu arayın. Her satış siparişi için ilişkili iş kodunu not edin.
1. **Satır** kılavuzunda ilgili bilgileri göstermek üzere her satış siparişinin satırını seçin. Her bir maddenin hangi konumdan çekileceğini not edin.
1. **Stok yönetimi \> Sorgular ve raporlar \>> Eldeki stok** öğesine gidin.
1. Eylem Bölmesi'nde, **Boyut görünümü** iletişim kutusunu açmak için **Boyutlar**'ı seçin.
1. **Plaka**, **Ambar** ve **Madde numarası** onay kutularının işaretlendiğinden emin olun ve **Tamam**'ı seçin.
1. **Filtre** bölmesinde, aşağıdaki filtreleri ayarlayın:

    - **Madde numarası** – **biri** - *L0101* ve *T100*
    - **Ambar** – **ile başlar** - *61*

1. Gösterilen **Plaka numarası** değerlerini not edin.

## <a name="example-scenario"></a><a name="example-scenario"></a>Örnek senaryo

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Mobil cihaz akışı yürütme – ürün için çalışma onayı kurulumu

1. Ambar *61*'de bir kullanıcı olarak Ambar Yönetimi mobil uygulamasına oturum açın.
1. **Giden \> Küme malzeme çekme oluşturma** bölümüne gidin.

    **GÖREV: Kümeye iş ata** sayfası görüntülenir.

1. Küme konumu 1'e atamak üzere satış siparişi 1 için iş kimliği girin.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. Küme konumu 2'e atamak üzere satış siparişi 2 için iş kimliği girin.
1. **Tamam**'ı (onay işareti simgesi) seçin.

    **Görev: Küme Malzeme Çekme Oluşturma: Çekme** sayfası açılır ve *Madde L0101 2 PL* görüntülenir.

Küme profili pozisyon sayısını 2 olarak ayarladığından, sistem sizi otomatik olarak ilk konsolide malzeme çekmeye yönlendirir: madde *L0101* için iki palet (PL).

Aşağıdaki adımlarda herhangi bir zamanda, malzeme çekme konumu gibi görevle ilgili ek bilgileri görüntülemek için **Ayrıntılar** sekmesini seçebilirsiniz.

1. **MADDE** alanını *L0101* olarak ayarlayın. Bu menü maddesi için gerekli olan madde numarası bu şekilde onaylanır. (Bu menü öğesini oluştururken **Mobil cihaz menü öğesi** sayfasından **İş onayı kurulumunu** seçerek daha önce yapılandırabilirsiniz.)
1. Konumda çekilen maddeyle ilişkilendirilmiş olan plaka numarasını girin. İki palet çekersiniz.
1. **LP** alanını *LP\_PICK\_01* olarak ayarlayın.
1. **Tamam**'ı (onay işareti simgesi) seçin.

    **GÖREV: Sıralama: Küme Çekme Oluşturma** sayfası görüntülenir. Burada, iki çekilen paleti bir çekme konumuna sıralamanız gerekir. Bu pozisyon, çekilen stoku satış siparişine göre ayırmak için kullanılan bir sepet veya kapsayıcı olabilir.

1. (Satış siparişi 1 için) pozisyon 1'e sıralanacak madde (*L0101*) ve miktar (*20* ea) için gösterilen ayrıntıları görüntüleyin.
1. **POZİSYON NA** alanını *1* olarak ayarlayın.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. (Satış siparişi 2 için) pozisyon 2'e sıralanacak madde (*L0101*) ve miktar (*20* ea) için gösterilen ayrıntıları görüntüleyin.
1. **POZİSYON NA** alanını *2* olarak ayarlayın.
1. **Tamam**'ı (onay işareti simgesi) seçin.

    **GÖREV: Küme Malzeme Çekme Oluşturma: Çekme** sayfası açılır ve *Madde T0100 7 ea* görüntülenir.

Bu senaryoda, pozisyon 1, satış siparişi 1'i karşılamak için çekilmesi gereken tüm madde miktarını kabul edemez. Pozisyonun tam olarak işaretlenmesi gerekir. Bu senaryoda, ikinci öğe kısmen çekilir. İkinci madde pozisyon 1 için kısmen çekilir ve siparişin karşılanması için kalan miktarı çekmek üzere yeni iş oluşturulur.

1. Menü düğmesini seçin (bazen hamburger veya hamburger düğmesi olarak da adlandırılır) ve **Pozisyon dolu** seçeneğini belirleyin.
1. Dolu olan konumu tanımlayın ve *1*'i seçin.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. Yine de, pozisyon 1'e çekilecek malzeme çekme miktarını girin. Sistem hangi madde numarasının çekileceğini belirleyebilir.
1. *2* girin.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. Kalan maddenin çekme işlemini, pozisyon 2 olarak tamamlamak için madde numarasını onaylayın.
1. **MADDE** alanını *T0100* olarak ayarlayın.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. **LP** alanını *LPREPL04* olarak ayarlayarak, maddenin çekildiği plaka numarasını girin.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. (Satış siparişi 2 için) pozisyon 2'e sıralanacak madde (*T0100*) ve miktar (*2* ea) için gösterilen ayrıntıları görüntüleyin.
1. **POZİSYON NA** alanını *2* olarak ayarlayın.
1. **Tamam**'ı (onay işareti simgesi) seçin.
1. (Satış siparişi 1 için) pozisyon 1'e sıralanacak madde (*T0100*) ve miktar (*2* ea) için gösterilen ayrıntıları görüntüleyin.
1. **POZİSYON NA** alanını *1* olarak ayarlayın.
1. **Tamam**'ı (onay işareti simgesi) seçin.

    **GÖREV: Küme Çekme Oluşturma: Yerine koyma** sayfası görüntülenir.

Bu senaryoda, küme çekme tamamlanmıştır ve kullanıcı, pozisyon 1 ve pozisyon 2'den çekilen maddeleri *STAGE1* hazırlık konumuna koymak üzere yönlendirilir.

1. Sayfadaki bilgileri gözden geçirin. Bu, toplam *44* tanesinin hazırlık konumuna koyulacağını gösterir.
1. **Tamam**'ı (onay işareti simgesi) seçin.

    Bir "Küme Tamamlandı" iletisi alırsınız.

Artık kalan miktarı çekmek için **Satış Malzeme Çekme** menü öğesini kullanabilirsiniz. Daha sonra, maddeleri hazırlama yerleşiminden yükleme noktasına taşımak için **Satış yükleme** menü öğesini kullanabilirsiniz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]