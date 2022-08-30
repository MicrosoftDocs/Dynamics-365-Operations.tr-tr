---
title: Ambar uygulamasından transfer emirleri oluşturma
description: Bu makale, Ambar Yönetimi mobil uygulaması özelliğinden transfer emirlerinin nasıl oluşturulacağını ve işleneceğini açıklamaktadır
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 45cbf7aca431c19e58de75355579304baef3cf7d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336470"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>Ambar uygulamasından transfer emirleri oluşturma

[!include [banner](../includes/banner.md)]

Bu özellik, ambar çalışanlarının doğrudan Ambar Yönetimi mobil uygulamasından transfer emirleri oluşturmasına ve işlemesine olanak tanır. Çalışan hedef ambarı seçerek başlar ve sonra transfer emrine plakalar eklemek için uygulamayı kullanarak bir veya daha fazla plaka tarayabilir. Ambar çalışanı **Siparişi tamamla**'yı seçtiğinde, bir toplu iş bu plakalar için kaydedilen eldeki stoğu temel alan gerekli transfer emri ve sipariş satırlarını oluşturur.

## <a name="turn-on-this-feature-and-its-prerequisites"></a><a name="enable-create-transfer-order-from-warehouse-app"></a>Bu özelliği açma ve özelliğin önkoşulları

Bu özelliği kullanabilmeniz için, özelliği ve önkoşullarını sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanabilir.

1. [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında aşağıdaki iki özelliği (sırayla) etkinleştirin. Supply Chain Management sürüm 10.0.25 itibarıyla her iki özellik de varsayılan olarak açıktır.
    1. *Ambar uygulaması olaylarını işle*<br>(Supply Chain Management sürüm 10.0.29 itibarıyla, özellik zorunludur ve kapatılamaz.)
    1. *Transfer emirlerini ambar uygulamasından oluştur ve işle*<br>(Supply Chain Management sürüm 10.0.29 itibarıyla, özellik zorunludur ve kapatılamaz.)
1. Giden sevkiyatların işlenmesini otomatikleştirmek için [*Giden sevkiyatları toplu işlerden onayla özelliğini*](confirm-outbound-shipments-from-batch-jobs.md) de etkinleştirmeniz gerekir. (Supply Chain Management sürüm 10.0.21 itibarıyla, bu özellik varsayılan olarak açıktır. Supply Chain Management 10.0.25 itibarıyla, bu özellik zorunludur ve kapatılamaz.)

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Transfer emirleri oluşturmak için bir mobil cihaz menü öğesi ayarlama

Burada, transfer emri oluşturmak üzere bir mobil cihaz menü öğesi ayarlamak için genel yönergeler verilmiştir. Kullanıcılar tabandan transfer emirleri oluştururken ayarlanacak otomatikleştirme düzeyi ile ilgili iş gereksinimlerinize bağlı olarak, farklı yapılandırmalar etkinleştirilir. Bu belgedeki senaryo bu tür bir yapılandırmaya göre tanımlanacaktır.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Yeni bir menü öğesi eklemek için **Yeni**'yi seçin. Başlamak için aşağıdaki ayarları yapın:

    - **Menü öğesi adı** - Supply Chain Management'ta görünmesi gereken şekilde bir ad atayın.
    - **Başlık**: Ambar Yönetimi mobil uygulamasında çalışanlara sunulması gereken şekilde bir menü adı atayın.
    - **Mod**: *Dolaylı* olarak ayarlayın (bu menü öğesi iş oluşturmaz).
    - **Faaliyet kodu** - Ambar çalışanlarının bir veya daha fazla taranmış plakaya dayalı bir transfer emri oluşturmasını sağlamak için *Plakalardan transfer emri oluştur* olarak ayarlayın.

1. Transfer emri satırlarının bu menü maddesi tarafından nasıl oluşturulacağını kontrol etmek için **Transfer emri satırı oluşturma ilkesi** ayarını kullanın. Bu satırlar, taranan plakalar için kaydedilen eldeki stoka göre oluşturulur/güncelleştirilir. Aşağıdaki değerlerden birini seçin:

    - **Rezervasyon yok** - Transfer emri satırları rezerve edilmez.
    - **Satır rezervasyonu ile plaka yönlendirmeli** - Transfer emri satırları rezerve edilir ve sipariş satırlarıyla ilişkili olan ilgili plaka kimliklerini depolayan, Plaka tarafından yönlendirilen strateji seçeneğini kullanır. Bu nedenle, transfer emri satırları için iş oluşturma sürecinin parçası olarak Bulunan plaka kodu değerleri kullanılabilir.

1. Giden transfer emri sevkiyat işlemine gerektiğinde daha fazla otomasyon eklemek için **Çıkış sevkiyatı ilkesi** ayarını kullanın. Çalışan **Siparişi tamamla** düğmesini seçtiğinde uygulama, geçerli transfer emrindeki tüm satırlar için *Giden sevkiyat ilkesi* alan değerini uygulayacak olan **Siparişi tamamla** ambar uygulaması olayını oluşturur. Daha sonra, transfer emri oluşturmak üzere olay kuyruğu bir toplu iş tarafından işlenirken, bu alanda depolanan değer toplu işlem tarafından okunabilir ve bu nedenle bu işin her satırı nasıl işleyeceğini kontrol edebilir. Aşağıdakilerden birini seçin:

    - **Hiçbiri** - Otomatik işlem yapılmaz.
    - **Ambara serbest bırak** - Ambara serbest bırakma işlemini otomatikleştirir.
    - **Sevkiyat onayı** - Sevkiyat onaylama işlemini otomatikleştirir.
    - **Serbest bırak ve sevkiyat onayı** - Hem ambara serbest bırakma hem de sevkiyat onayı işlemlerini otomatikleştirir.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>Mobil cihaz menü öğesini menüye ekleme

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin
1. **Düzenle** öğesini seçin.
1. **Mevcut menüler ve menü öğeleri** altında yeni menü öğesinin seçimi ardından mevcut bir menüyü seçin. Sağ ok düğmesini seçerek menü öğesini ekleyin.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Plakalara dayalı bir transfer emri oluşturma

Ambar Yönetimi mobil uygulamasında plakalara dayalı transfer emirleri oluşturmak için basit bir işlem bulunur. Bunu yapmak için, çalışan Ambar Yönetimi mobil uygulamasını kullanarak aşağıdakileri yapar:

1. Transfer emrini oluşturun ve hedef ambarı tanımlayın.
1. Sevk edilecek her plakayı tanımlayın.
1. **Siparişi tamamla**'yı seçin.

>[!NOTE]
> Birden fazla çalışanın **Transfer emri seç** düğmesini kullanarak ambar uygulaması olay kuyruğundan varolan, işlenmemiş bir transfer emri numarası seçerek, aynı transfer emrine yönelik plakalar ataması mümkündür. Transfer emri numarası değerlerini bulma hakkında daha fazla bilgi için bkz. [Ambar uygulaması olaylarını sorgulama](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>Örnek senaryo

Bu senaryo, seçilen plakalarda kaydedilen eldeki stok temel alınarak oluşturulan ve otomatik olarak işlenen transfer emirlerini alma işlemine genel bakış sağlar.

Önerilen değerleri kullanarak bu senaryoya göre çalışmak için, demo verilerinin yüklü olduğu bir sistem üzerinde çalışmanız ve başlamadan önce *USMF* tüzel kişiliğini seçmeniz gerekir.

Bu senaryoda [Ambar uygulaması özelliğinden transfer emirleri oluştur ve işle](#enable-create-transfer-order-from-warehouse-app) ve [ambar uygulaması olay işleme](warehouse-app-events.md) özelliğini etkinleştirmiş olduğunuz varsayılır.

Mobil cihaz menü öğelerinde transfer emri oluşturmayı ayarlamaya ek olarak ek şablonlar, yerleşim yönergeleri ve toplu işlerin da ayarlanması ve etkinleştirilmesi gerekir.

### <a name="example-scenario-blueprint"></a>Örnek Senaryo şeması

Her biri ambarlarınızın birindeki (*Ambar 51*) belirli bir konuma yerleştirilen maddelerin karışımını içeren birden çok plakanız var. Çalışanların taranmış plakaların bir koleksiyonu için başka bir ambara (*Ambar 61*) transfer emri oluşturmasına izin veren işlemi etkinleştirmek istiyorsunuz. Sipariş için en son plaka tanımlandıktan sonra, transfer emrini otomatik olarak sevk edip güncelleştireceksiniz.

![Otomatik transfer emri işlemi örneği.](media/create-transfer-order-from-app-example.png "Otomatik transfer emri işlemi örneği")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Transfer emirleri oluşturmak için bir mobil cihaz menü öğesi oluşturma

Bu bölüm, transfer emirleri oluşturmak için yeni bir mobil cihaz menü öğesinin nasıl oluşturulacağını açıklar. **Mod**'u *Dolaylı* ve **Faaliyet kodu**'nu *Plakalardan transfer emri oluştur* olarak ayarlayın.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Menü öğesi adı** alanına *TE Oluştur* adını girin.
1. **Başlık** alanına *TE Oluştur* açıklamasını girin.
1. **Mod** alanında, *Dolaylı*'yı seçin.
1. **Faaliyet kodu**'nda, *Plakalardan transfer emri oluştur*'u seçin
1. **Sipariş satırı oluşturma ilkesi**'nde *Satır rezervasyonuyla plaka yönlendirmeli*'yi seçin.
1. **Giden sevkiyat ilkesi**'nde *Serbest bırak ve sevkiyat onayı*'nı seçin.
1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. **Düzenle** öğesini seçin.
1. Mevcut **Stok** menüsünü seçin ve **Mevcut menüler ve menü öğeleri** altında yeni menü öğesini seçin. Sağ ok düğmesini seçerek menü öğesini **Stok** menüsüne ekleyin.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>İş şablonlarını otomatik olarak işlenecek şekilde ayarlama ve işi bulunan plakaya göre kesme

Bu bölüm, bir dalga serbest bırakıldığında, bir iş şablonunun şablon tarafından oluşturulan işi otomatik olarak işlemek üzere nasıl etkinleştirileceğini açıklar.

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. **İş emri türü** alanında *Transfer çıkışı*'nı seçin.
1. Yeni iş şablonu oluşturmak için **Yeni**'yi seçin.
1. **İş şablonu** alanında, *51 Plakayı otomatik işle* girin.
1. **İş şablonu açıklaması** alanına, *51 Plakayı otomatik işle* girin.
1. **Otomatik olarak işle** onay kutusunu seçin. Bu, otomasyon adımlarının işlenmesi için seçilmelidir.
1. Demo verilerinde zaten *51 Transfer* bir iş şablonu vardır , **Sıra numarası alanını** yeni iş şablonu, varolan iş şablonu *51 Transfer*'den daha düşük bir sıra numarasına sahip olacak şekilde düzenleyin.
1. **İş Şablonu Ayrıntıları** hızlı sekmesini etkinleştirmek için araç çubuğunda **Kaydet**'i seçin.
1. **İş Şablonu Ayrıntıları** hızlı sekmesinde, araç çubuğunda **Yeni**'yi seçin. İki satır ekleyeceksiniz.
1. **İş türü** alanında *Malzeme çekme* öğesini seçin.
1. **İş sınıfı kodu** alanında *TransfOut*'u seçin.
1. **İş Şablonu Ayrıntıları** araç çubuğunda **Yeni**'yi seçin.
1. **İş türü** alanında, *Yerine koyma*'yı seçin.
1. **İş sınıfı kodu** alanında *TransfOut*'u seçin.
1. **Yönerge kodu** alanını etkinleştirmek için **Kaydet**'i seçin.
1. **İş türü** *Yerine koyma* satırında, **Yönerge kodu** *Bölme kapısı*'nı seçin. Bu yeni iş şablonunun en düşük **Sıra numarasını** alıyor olduğundan emin olun.
1. Sorgu düzenleyicisini açmak için araç çubuğunda **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde **Ekle**'yi seçin.
1. Eklenen satırda **Alan**'da *Ambar* seçeneğini belirleyin.
1. **Ölçüt** alanında *51* öğesini seçin.
1. **Sıralama** sekmesini seçin.
1. **Ekle**'yi seçin ve **Alan**'ı *Bulunan plaka kimliği*'ne ayarlayın. Bu alan seçildiğinde, **İş başlığı sonları** araç çubuğu düğmesi etkinleşir.
1. Gruplandırmayı sıfırlamak ve **İş şablonları** sayfasına dönmek için **Tamam**'ı ve arından **Evet**'i seçin.
1. **İş başlığı sonları**'nı seçin ve **Bulunan plaka kodu** için **Bu alana göre grupla**'yı etkinleştirip kapatın.

> [!NOTE]
> Tüm kurulum otomatik olarak işlenemez (örneğin, fiili ağırlık maddeleri ve karışık izleme boyutları kullanımı).

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Plakayla yönlendirilen strateji için konum yönergeleri ayarlama

Bu bölüm, **Plakayla yönlendirilen** stratejisini kullanmak için konum yönergesi çekme işleminin nasıl ayarlanacağını açıklar.

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. **Düzenle** öğesini seçin.
1. Gezinti listesi başlığında, **İş emri türü** *Transfer çıkışı*'nı seçin.
1. Gezinti listesinde, mevcut konum yönergesi olan **Çekmek için 51**'i seçin.
1. **Satırlar** hızlı sekmesinde, **Bölmeye izin ver** onay kutusunu seçin.
1. **Konum Yönergesi Eylemleri** hızlı sekmesinde, yeni eylem satırı eklemek için **Yeni**'yi seçin.
1. **Ad** alanına, *Plaka Yönlendirmeli* girin.
1. *Strateji* alanına **Plaka yönlendirmeli** girin. Bu eylem en düşük sıra numarasını gerektirir.
1. Araç çubuğunda **Kaydet**'i seçin.
1. Araç çubuğundan **Yenile** sayfası simgesini seçin.
1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde, *TOPick* satırını seçin.
1. **Yerleşim Yönergesi Eylemleri** araç çubuğunda, sıra numarasını yeni oluşturulan **Plaka yönlendirmeli** eyleminin sıra numarasından büyük olacak şekilde değiştirmek için *Aşağı taşı*'yı seçin.

> [!NOTE]
> Plaka yönlendirmeli strateji, transfer emri satırlarıyla ilişkilendirilmiş olan istenen plakaları tutan konumlara göre ayırma ve çekme işi oluşturmayı dener. Ancak bu mümkün değilse ve hala malzeme çekme işi oluşturmak istiyorsanız, iş sürecini gereksinimlerinize bağlı olarak başka bir yerleşim yönergesi eylem stratejisine dönmeniz ve ayrıca belki ambarın başka bir alanında stok araması yapmanız gerekir.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Ambar uygulaması olaylarını işlemek için bir toplu iş ayarlayın

Bu bölüm, ambar uygulaması olaylarını işlemek üzere planlanan bir toplu işin nasıl ayarlanacağını açıklar.

1. **Ambar yönetimi \> Periyodik görevler \> Ambar uygulaması olaylarını işle**'ye gidin.
2. İletişim kutusunda, **Arka planda çalıştır** bölümünde **Toplu işleme**'yi etkinleştirin.
3. **Yineleme**'yi seçin ve toplu işi işletmeniz için gereken aralığa göre işlenecek şekilde ayarlayın.
4. Ana iletişim kutusuna dönmek için **Tamam**'ı seçin.
5. İşi toplu iş kuyruğuna eklemek için ana iletişim kutusunda **Tamam**'ı seçin.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Transfer emirlerini otomatik olarak serbest bırakmak için bir toplu iş ayarlama

Bu bölüm, "serbest bırakmaya hazır" olarak işaretlenmiş transfer emirlerini serbest bırakmak üzere bir planlı toplu işin nasıl ayarlanacağını açıklar.

1. **Ambar yönetimi \> Ambara serbest bırakma \> Transfer emirlerini otomatik serbest bırakma** seçeneğine gidin.
1. İletişim kutusunda, **Dahil edilecek kayıtlar** bölümünü genişletin.
1. **Eklenecek kayıtlar** bölümünde **Filtrele**'yi seçin.
1. **WHSTransferAutoRTWQuery** sorgu sayfasında, **Aralık** sekmesinde sorguya yeni bir satır eklemek için **Ekle**'yi seçin.
1. Yeni satır **Tablo** alanında, açılan menüyü seçin ve **Transfer satırını ambara serbest bırakma** tablosunu seçin.
1. **Alan**  açılır menüsünde **Giden sevkiyat ilkesi**'ni seçin.
1. **Ölçüt** alanında **Serbest bırak ve sevkiyat onayı**'nı seçin.
1. **Alanın** *Kaynak ambar* olarak ayarlandığı satırda, **Ölçüt** alanında, *51*'i seçin.
1. Ana iletişim kutusuna dönmek için **Tamam**'ı seçin.
1. Toplu işlemeyi ayarlamak için **Arka planda çalıştır** bölümünü genişletin.
1. **Arka planda çalıştır** bölümünde **Toplu işleme**'yi etkinleştirin.
1. **Yineleme**'yi seçin ve toplu işi işletmeniz için gereken aralığa göre işlenecek şekilde ayarlayın.
1. Ana iletişim kutusuna dönmek için **Tamam**'ı seçin.
1. Toplu işin toplu iş kuyruğuna eklenmesi için ana iletişim kutusunda **Tamam**'ı seçin.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>"Giden sevkiyatı işle" toplu işini ayarlama

Bu bölümde, "sevk etmeye hazır" transfer emri satırlarıyla ilgili sevk edilmeye hazır yükler için giden sevkiyat onayını çalıştırmak amacıyla bir planlı toplu işin nasıl ayarlanacağı açıklanmaktadır.

1. **Ambar yönetimi \> Periyodik görevler\> Giden sevkiyatları işle**'ye gidin.
1. **Eklenecek kayıtlar** bölümünü genişletin.
1. **Filtre**'yi seç.
1. **WHSLoadShipConfirm** sorgusunda **Birleşimler** sekmesini seçin.
1. **Yükler** ve **Yük ayrıntılarını** genişletmek için tablo hiyerarşisini genişletin.
1. **Yük ayrıntıları** tablosunu seçin.
1. **Tablo birleştirme ekle** düğmesini seçin.
1. Tablo ilişkileri listesinde, **Transfer emri satırları (Referans)** için *İlişki* sütununa filtre uygulayın veya arama yapın.
1. Listede tablo ilişkisine odaklanın ve **Seç** düğmesine basın.
1. **Transfer emri satırları** tablosunu seçin.
1. **Tablo birleştirme ekle** düğmesini seçin.
1. Tablo ilişkileri listesinde, **Stok Transferi Ek Alanları (Kayıt Kodu)** için *İlişki* sütununa filtre uygulayın veya arama yapın.
1. Listede tablo ilişkisine odaklanın ve **Seç** düğmesine basın.
1. **Aralık** sekmesini seçin.
1. **Aralık** sorgu tablolarında, üç sorgu ölçütü aralığı ayarlarsınız. Bir satır eklemek için **Ekle** düğmesini seçin.
1. **Yükler** tablosu için bir aralık ekleyin. **Alan**'ı *Yük durumu* olarak **Ölçüt**'ü *Yüklendi* olarak ayarlayın.
1. **Stok Transferi Ek Alanları** tablosu için başka bir aralık ekleyin. **Alan**'ı *Giden sevkiyat ilkesi* olarak ve **Ölçüt**'ü *Serbest bırakma ve sevkiyat onayı* olarak ayarlayın.
1. **Yük ayrıntıları** tablosu için başka bir aralık ekleyin. **Alan**'ı *Referans* olarak ve **Ölçüt**'ü *Transfer emri sevkiyatı* olarak ayarlayın.
1. Ana iletişim kutusuna dönmek için **Tamam**'ı seçin.
1. **Arka planda çalıştır** bölümünü genişletin.
1. **Toplu işlemi** etkinleştirin.
1. **Yineleme**'yi seçin ve toplu işi işletmeniz için gereken aralığa göre işlenecek şekilde ayarlayın.
1. Ana iletişim kutusuna dönmek için **Tamam**'ı seçin.
1. Toplu işin toplu iş kuyruğuna eklenmesi için ana iletişim kutusunda **Tamam**'ı seçin.

> [!NOTE]
> Daha fazla bilgi için bkz. [Toplu işlerden giden sevkiyatları onaylama](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>"Ambar uygulamasından transfer emri oluştur" örneğini işleme

### <a name="add-on-hand-on-a-license-plate"></a>Plakaya eldeki stoğu ekleme

Bu senaryoda başlangıç noktası olarak, eldeki fiziksel stoğu içeren bir plakaya sahip olmanız gerekir.

| Madde | Ambar | Stok durumu | Yer | Plaka | Miktar |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Mevcut | LP-010 | LP10 | 1 |
| A0002 | 51 | Mevcut | LP-010 | LP10 | 2 |

Aşağıdaki değerleri kullanarak eldeki fiziksel stok miktarlarını ekleyin:

> [!NOTE]
> LP-010 gibi karışık öğeleri düzenlemenize olanak tanıyan konumları kullanmanız ve plaka oluşturmanız gerekir.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>Transfer emirlerini ambar uygulamasından oluştur ve işle

1. Uygulamayı açın ve kullanıcı *51* olarak oturum açın. Geçerli kullanıcı ambarı 51 olacaktır.
1. Kurulum sırasında eklediğiniz menü konumundan **TE Oluştur** menü öğesini seçin.
1. Hedef ambarı (Hedef ambar) **Ambar** alanına *61* olarak girerek bir transfer emri oluşturmayı başlatın. Yeni transfer emri geçerli ambardan 51 (Kaynak ambar) hedef ambara *61* geçer.
1. **Tamam**'ı seçin.
1. **Plaka** alanında plaka kodunu tarayın. Daha önceki bir adımda eklenen stoğun plakasını (*LP10*) girin.
1. **Tamam**'ı seçin.
1. Menü düğmesini seçin ve ardından ambar uygulaması transfer emri oluşturma işlemini sonlandırmak için **Siparişi tamamla**'yı seçin.

Belirtilen örnek için, iki **Ambar uygulaması olayı** (*Transfer emri oluştur* ve *Transfer emrini tamamla*) kullanılır.

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Ambar uygulaması olaylarını sorgulama

Ambar Yönetimi mobil uygulaması tarafından oluşturulan olay kuyruğunu ve olay iletilerini **Ambar yönetimi \> Sorgular ve raporlar \> Mobil cihaz günlükleri \> Ambar uygulaması olayları**'na giderek görüntüleyebilirsiniz.

*Transfer siparişi oluştur* olay iletileri *Bekleme* durumunu alacaktır, bu da **Ambar uygulaması olaylarını işle** toplu işinin olay iletilerini almayacağı ve işlemeyeceği anlamına gelir. Olay iletisi *Kuyruğa alındı* durumuna güncellendiğinde toplu iş olayları işler. Bu, *Transfer emrini tamamla* olayının oluşturulmasıyla (bir çalışan Ambar Yönetimi mobil uygulamasında **Siparişi tamamla** düğmesini seçtiğinde) aynı anda gerçekleşir. *Transfer emri oluştur* olay iletileri işlendiğinde durum *Tamamlandı* veya *Başarısız* olarak güncelleştirilir. *Transfer emrini tamamla* durumu *Tamamlandı* olarak güncelleştirildiğinde, ilgili tüm olaylar kuyruktan silinir.

İletiler **Kuyruğa alındı** durumuna güncelleştirilmeden önce transfer emri verilerinin oluşturulmasıyla ilgili *Ambar uygulaması olayları* toplu iş tarafından işlenmeyeceğinden, **Tanımlayıcı** alanının bir bölümü olarak istenen transfer emri numaralarına bakmanız gerekecektir. **Tanımlayıcı** alanı, **Ambar uygulaması olayları** sayfasının başlığında yer alır.

Ambar olay işlemenin parçası olarak, transfer emri satırının oluşturulması başarısız olabilir. Bu durumda, olay iletisinin durumu *Başarısız* olarak güncelleştirilir ve herhangi bir sorunu düzeltmek için nasıl işlem yapılacağını öğrenmek için **Toplu iş günlüğü** bilgilerini kullanabilirsiniz.

*Transfer emri oluştur* olayı için eksik transit ambarı gibi, işlemin eksik kurulumu ile ilgili genel sorunlar olabilir. Buna benzer bir örnekte, sevkiyat ambarına bir transit ambarı ekler ve tüm ambar uygulaması olay iletilerinin durumunu *Başarısız* yerine *Kuyruğa alındı* olarak değiştirmek için **Sıfırla** seçeneğini kullanabilirsiniz. Bu, toplu işin olay iletilerini kurulum verilerini düzelttikten sonra işleyeceği anlamına gelir.

Üretim ortamlarında, özel durumlar toplu iş işleme sırasında boş olması ve dolayısıyla hiçbir transfer emri satırı oluşturulamaması nedeniyle istenen plaka olması gibi işlem ile ilgili olacaktır. Bu başarısız olay iletisi, **Sil** seçeneği kullanılarak kaldırılabilir veya gerekli fiziksel eldeki miktarı plakaya ekleyebilir ve tüm ilgili olay iletileri için **Sıfırla** seçeneğini kullanabilirsiniz.

Daha fazla bilgi için bkz. [Ambar uygulaması olayı işleme](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>Örnek senaryo işlemeyi takip edin

Bu senaryo sırasında, aşağıdakiler meydana geldi:

1. Ambar Yönetimi mobil uygulamasını kullanarak, **Plakalardan transfer emri oluştur** faaliyet kodunu kullanan bir menü öğesi seçtiniz.
1. Uygulama, transfer emri için hedef ambarı seçmenizi istedi. Kaynak ambar her zaman Çalışan olarak oturum açmış olduğunuz geçerli ambardır.
1. Hedef ambar seçiminde sistem yaklaşan transfer emri için bir kod numarası rezerve etti (sisteminizde tanımlanan transfer emri numara sırasını temel alarak) ancak transfer emrini henüz oluşturmadı.
1. Yeni ambara taşınması gereken eldeki stoğu içeren plaka olan *LP10*'u taradığınızda,daha sonra işlenecek olaylar kuyruğuna bir **Ambar uygulaması olayı** eklendi. Ambar olayı, tasarlanan transfer emri numarası dahil olmak üzere taramayla ilgili ileti ayrıntılarını içeriyordu.
1. Ambar Yönetimi mobil uygulamasında, **Siparişi tamamla** düğmesi seçildiğinde yeni bir ambar uygulama olayı, **Transfer emrini tamamla** oluşturulur ve ilgili mevcut olay, **Transfer emri oluştur** durumu **Kuyruğa alındı** olarak değişir.
1. Arka uçta, **Ambar uygulaması olaylarını işle toplu işi** **Kuyruğa alındı** olayını aldı ve taranmış plakayla ilgili eldeki stoğu topladı. Eldeki stoğa göre, gerçek transfer emri kaydı ile ilişkili satırlar oluşturuldu. İş aynı zamanda transfer emri için **Giden sevkiyat ilkesi** alanını yapılandırılan *Serbest bırakma ve sevkiyat onayı*'nı temel alan değerle doldurdu ve plakayı **Plaka yönlendirmeli** strateji için satırlara göre doldurdu.
1. Transfer emri satırına dayalı olarak **Giden sevkiyat ilkesi** alan değeri **Transfer emirleri toplu işini otomatik serbest bırakma** sorgusu transfer emrinin sevkiyat ambarına serbest bırakılmasıyla sonuçlandı. Kullanılan **Dalga şablonu**, **İş şablonu** ve **Konum yönergelerinin** kurulumu nedeniyle, işin aldığı otomatik işleme **Yük durumu** *Yüklendi* olarak güncelleştirildi.
1. **Giden sevkiyat toplu işini işle** yük için yürütülür ve sevk edilen transfer emri ve Ön Sevkiyat Bildirimi (ÖSB) oluşturulur.
1. Tüm bu olayların zamanlaması oluşturulan toplu işlerin **Yineleme** ayarlarına bağlıdır.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="mobile-device-menu-item-setup"></a>Mobil cihaz menü öğesi ayarlama

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Menü öğesi iş etkinliği açılır listesinde neden "Plakadan transfer emri oluştur" öğesini göremiyorum?

*Ambar uygulamasından transfer emirleri oluştur* özelliğinin etkinleştirilmesi gerekir. Daha fazla bilgi için, bkz. [Ambar uygulamasından transfer emri oluşturmayı etkinleştirme](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-management-mobile-app-processes"></a>Ambar Yönetimi mobil uygulaması işlemleri

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>"Siparişi tamamla" menü düğmesini niçin göremiyorum?

Transfer emrine atanmış en az bir plaka olması gerekir.

#### <a name="can-several-warehouse-management-mobile-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Birçok Ambar Yönetimi mobil uygulaması kullanıcısı aynı anda aynı transfer emrine plaka ekleyebilir mi?

Evet, birçok ambar çalışanı aynı transfer emrine plaka tarayabilir.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Aynı plaka farklı transfer emirlerine eklenebilir mi?

Hayır, plaka bir kerede yalnızca bir transfer emrine eklenebilir.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>"Siparişi tamamla" düğmesini seçtikten sonra, o transfer emri için daha fazla plaka ekleyebilir miyim?

Hayır, **Transfer emrini tamamla** ambar uygulaması olayına sahip bir transfer emrine daha fazla plaka ekleyemezsiniz .

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-management-mobile-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Sipariş henüz arka uç sisteminde oluşturulmadıysa, Ambar Yönetimi mobil uygulamasında "Transfer emri seç" düğmesiyle kullanılacak mevcut transfer emirlerini nasıl bulabilirim?

Çalışanların [veri sorgulama](warehouse-app-data-inquiry.md) yeteneklerini kullanarak Ambar yönetimi mobil uygulamasında transfer emri numaralarını aramasına olanak sağlayabilirsiniz. Örneğin, web istemcisinin **Ambar uygulaması olayları** sayfasında (`WHSMobileDeviceQueueMessageCollection`) *Sipariş seç - MobileDeviceQueueMessageCollectionIdentifierId* adımının parçası olarak görüntülenen verileri sorgulayan bir [sapma](warehouse-app-detours.md) mobil cihaz menü öğesi oluşturabilirsiniz. Transfer emri numarası,**Tanımlayıcı** alanında gösterilen değerle eşleşir. Ayrıca bkz. [Ambar uygulaması olaylarını sorgulama](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-management-mobile-app"></a>Ambar Yönetimi mobil uygulamasıdan kullanılacak transfer emri numarasını el ile seçebilir miyim?

Yalnızca numara serileri ile otomatik olarak oluşturulan transfer emri numaraları desteklenir. Ayrıca, **Transfer emri seç** düğmesinin nasıl ayarlanacağı ile ilgili önceki sorunun yanıtını da bakabilirsiniz. Transfer emri numaralarını bulma hakkında daha fazla bilgi için bkz. [Ambar uygulaması olaylarını sorgulama](#inquire-the-warehouse-app-events).

### <a name="background-processing"></a>Arka planda işleme

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Ambar uygulaması olayları kuyğu ileti tablolarındaki kayıtları nasıl temizleyebilirim?

Bunu **Ambar uygulama olayları** sayfasında görüntüleyebilir ve yönetebilirsiniz. Daha fazla bilgi için bkz. [Ambar uygulaması olaylarını sorgulama](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Transfer emri "Giriş tarihi" neden "Teslimat tarihi denetimi" kurulumuma göre güncelleştirilmedi?

Transfer emirleri **Teslimat tarihi denetimi** özellikleri kullanılmadan oluşturulur.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Eldeki fiziksel stoğu negatif olan bir plaka kullanabilir miyim?

Özellik, lisans plakası düzeyinde yalnızca pozitif fiziksel eldeki miktarları destekler ancak transfer emirlerine lisans plakaları atarken, yüksek ambar ve stok durumu düzeylerinde fiziksel negatif eldeki miktarlarınız olabilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]