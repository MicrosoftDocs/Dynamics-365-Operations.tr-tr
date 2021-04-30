---
title: Küçük paket sevkiyatı
description: Bu konuda, küçük paket sevkiyatı (SPS) özelliğiyle ilgili bilgiler verilir. Bu özellik, paketlenmiş konteyner hakkındaki ayrıntıların taşıyıcıya gönderilmesi ve ardından söz konusu taşıyıcıdan gönderim etiketi, sevkiyat ücreti ve izleme numarası almak için Microsoft Dynamics 365 Supply Chain Management'ı etkinleştirmeyi sağlar.
author: Mirzaab
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 3e72959d79e9b3b03e061a0f26750e3bd025219e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910221"
---
# <a name="small-parcel-shipping"></a>Küçük paket sevkiyatı

[!include [banner](../../includes/banner.md)]

Küçük paket sevkiyatı (SPS) özelliği, taşıyıcı API'leri aracılığıyla iletişim için bir çerçeve sağlayarak sevkiyat taşıyıcılarıyla doğrudan etkileşim için Microsoft Dynamics 365 Supply Chain Management'ı etkinleştirmeyi sağlar. Bu işlev, bağımsız satış siparişlerini konteyner sevkiyatı veya kamyon yükünden az (LTL) sevkiyatı kullanmak yerine ticari sevkiyat taşıyıcıları aracılığıyla gönderdiğiniz durumlar için faydalıdır.

SPS özelliği, sevkiyat taşıyıcınızla özel bir *değerlendirme altyapısı* aracılığıyla etkileşim kurar. Kuruluşunuzun bu değerlendirme altyapısını taşıyıcınız veya taşıyıcı merkez hizmetiniz ile birlikte çalıştırarak geliştirmesi gerekir. Bu değerlendirme altyapısı, paketlenmiş konteyner hakkındaki ayrıntıların taşıyıcınıza gönderilmesi ve ardından söz konusu taşıyıcıdan gönderim etiketi, sevkiyat ücreti ve izleme numarası almak için Supply Chain Management'ı etkinleştirmeyi sağlar.

Döndürülen sevkiyat ücreti, ilişkili satış siparişine sair gider olarak eklenir. Daha sonra döndürülen gönderim etiketi, Zebra Programlama Dili (ZPL) yazıcısı kullanılarak otomatik olarak yazdırılıp sevkiyata uygulanabilir. Taşıyıcı, ambarınızdan paketleri alırken bu gönderim etiketini tarar.

## <a name="prepare-your-system-to-support-sps"></a>Sisteminizi SPS'yi destekleyecek şekilde hazırlama

SPS işlevini kullanmaya başlamadan önce, Özellik yönetimi'nde SPS özelliğini açmanız, değerlendirme altyapınızı eklemeniz ve bunu desteklemek için **Taşıma yönetimi** ve **Ambar yönetimi** modüllerini ayarlamanız gerekir.

### <a name="turn-on-the-sps-feature"></a>SPS özelliğini açma

SPS özelliğini kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Taşıma yönetimi*
- **Özellik adı:** *Küçük paket sevkiyatı*

### <a name="deploy-and-set-up-rate-engines"></a>Değerlendirme altyapılarını dağıtma ve ayarlama

Supply Chain Management, değerlendirme altyapısı içermez. Gereksinim duyduğunuz değerlendirme altyapılarını edinmeniz veya oluşturmanız ve sonra bunları sisteminize eklemeniz gerekir. Ancak Microsoft, test etmek için kullanabileceğiniz bir tanıtım değerlendirme altyapısı sunar.

#### <a name="download-and-deploy-the-demo-rate-engine"></a>Tanıtım amaçlı değerlendirme altyapısını indirme ve dağıtma

Tanıtım amaçlı değerlendirme altyapısını edinmek için aşağıdaki adımları izleyin.

1. GitHub'da, [tanıtım amaçlı değerlendirme altyapısı için dinamik bağlantı kitaplığı (DLL)](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS) öğesini indirin.
1. Supply Chain Management sunucunuzda DLL'yi  **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** klasörüne kaydedin.

#### <a name="create-and-deploy-functional-rate-engines"></a>İşlevsel değerlendirme altyapıları oluşturma ve dağıtma

Üretim veya test ortamında kullanılabilmeleri için işlevsel değerlendirme altyapılarının nasıl oluşturulduğu ve dağıtılacağı hakkında bilgi için, aşağıdaki konulara bakın:

- [Yeni bir taşıma yönetimi altyapısı oluşturma](../transportation/create-new-transportation-management-engine.md)
- [Taşıma yönetimi altyapılarını ayarlama](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

SPS değerlendirme altyapısı oluşturma hakkında daha fazla bilgi için şu blog gönderisini okuyun: [Küçük Paket Sevkiyatı: Microsoft Dynamics 365'te küçük paket sevkiyatı işlevinden yararlanma](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>Supply Chain Management'ta değerlendirme altyaspısı ayarlama

SPS için bir değerlendirme altyapısı oluşturup dağıttıktan sonra, bu altyapıyı ayarlamak için aşağıdaki adımları izleyin.

1. **Taşıma yönetimi \> Kurulum \> Altyapılar \> Değerlendirme altyapısı**'na gidin.
1. Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki alanları ayarlayın:

    - **Değerlendirme altyapısı**: Değerlendirme altyapısı için benzersiz bir ad girin. Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız *Tanıtım amaçlı değerlendirme altyapısı* adını girin.
    - **Ad**: Değerlendirme alt yapısının kısa açıklamasını girin. Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız *Tanıtım amaçlı değerlendirme altyapısı* adını girin.
    - **Değerlendirme metaverileri kodu**: Ücretinizi hesaplamak için kullanılacak temeli seçin. Örneğin, ücretiniz mesafe göre hesaplanabilir. Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız, bu alanı boş bırakabilirsiniz.
    - **Altyapı derlemesi**: Dağıttığınız DLL paketinin dosya adını girin. Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız *TMSSmallParcelShippingEngine.dll* adını girin.
    - **Altyapı sınıfı**: Değerlendirme altyapınız için belirlenen sınıf adını girin. Tanıtım amaçlı değerlendirme altyapısını kullanıyorsanız *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine* adını girin.

## <a name="example-scenario"></a>Örnek senaryo

Bu örnek senaryo, bu konunun önceki bölümlerinde anlatılan şekilde sisteminizi hazırladıktan sonra SPS'nin nasıl ayarlanacağını ve kullanılacağını gösterir. Bu senaryoda, yukarıda sözü edilen tanıtım amaçlı değerlendirme altyapısı kullanılır.

### <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Burada belirtilen tanıtım kayıtlarını ve değerlerini kullanarak bu senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

### <a name="set-up-the-scenario"></a>Senaryoyu ayarlama

Bu örnek senaryo için bir tanıtım taşıyıcınız, taşıyıcı grubunuz, paketleme ilkeniz ve paketleme profiliniz olmalıdır. Aşağıdaki alt bölümler senaryo için gereken kayıtların nasıl hazırlanacağını açıklamaktadır. Üretim senaryosunda, kurulum işlemi genellikle burada açıklanan işleme benzer. Ancak, farklı değerler ayarlarsınız.

#### <a name="set-up-carriers"></a>Taşıyıcıları ayarlama

Taşıyıcı ayarlamak için aşağıdaki adımları izleyin.

1. **Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Sevkiyat taşıyıcıları** seçeneğine gidin.
1. Eylem Bölmesi'nde, bir taşıyıcı eklemek için **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Sevkiyat taşıyıcısı:** *Tanıtım Taşıyıcısı*
    - **Ad:** *Tanıtım Taşıyıcısı*
    - **Mod:** *Kara yolu*

1. **Genel bakış** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Sevkiyat taşıyıcısını etkinleştir**: *Evet*
    - **Taşıyıcı değerlendirmesini etkinleştir**: *Evet*

1. **Hizmetler** hızlı sekmesinde, ızgaraya hizmet eklemek için **Yeni**'yi seçin.
1. Yeni hizmet için aşağıdaki değerleri ayarlayın:

    - **Taşıyıcı hizmeti:** *Tanıtım taşıyıcı hizmeti*
    - **Ad:** *Tanıtım taşıyıcı hizmeti*
    - **Taşıma yöntemi:** *Kara yolu*

    Tüm diğer alanlar için gerektiği gibi rastgele değerler girin. (Yeni sevkiyat taşıyıcısı kaydını kaydettiğinizde, yeni bir teslimat modu oluşturulur ve **Teslimat şekli** alanı otomatik olarak ayarlanır.)

1. Izgaraya değerlendirme profili eklemek için **Değerlendirme profilleri** hızlı sekmesinde, **Yeni**'yi seçin.
1. Yeni profil için aşağıdaki değerleri ayarlayın:

    - **Değerlendirme profili:** *Tanıtım taşıyıcı hizmeti*
    - **Ad:** *Tanıtım taşıyıcı hizmeti*
    - **Değerlendirme altyapısı:** *Tanıtım değerlendirme alt yapısı*

    Tüm diğer alanlar için gerektiği gibi rastgele değerler girin.

1. Eylem bölmesinde, **Kaydet**'i seçin.

Taşıyıcıların nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Sevkiyat taşıyıcılarını ayarlama](../transportation/tasks/set-up-shipping-carriers.md).

#### <a name="set-up-carrier-service-accounts"></a>Taşıyıcı hizmeti hesaplarını ayarlama

Taşıyıcı hizmeti hesabını ayarlamak için aşağıdaki adımları izleyin.

1. **Taşıma yönetimi \> Kurulum \> Değerlendirme \> Taşıyıcı hizmeti hesabı**'na gidin.
1. Eylem bölmesinde taşıyıcı hizmeti hesabı eklemek için **Yeni**'yi seçin.
1. Yeni hesap için aşağıdaki değerleri ayarlayın:

    - **Sevkiyat Taşıyıcısı:** *Tanıtım Taşıyıcısı*
    - **Taşıyıcı hizmeti:** *Tanıtım taşıyıcı hizmeti*
    - **Taşıyıcı müşteri hesap numarası:** Sevkiyat taşıyıcısı bağlantısını teyit etmek ve kimliğini doğrulamak için kullanılan taşıyıcı müşteri hesap numarası. Taşıyıcınız, bu değeri sağlayacaktır. Tanıtım hizmetini kullanıyorsanız rastgele bir değer girebilirsiniz.
    - **Tesis:** *6*
    - **Ambar:** *62*

    > [!NOTE]
    > Genellikle, **Taşıyıcı müşteri hesap numarası** değeri bağlantının kimliğini doğrulamak için gereken tek değerdir. Ancak, taşıyıcınız ek kimlik doğrulama parametreleri gerektiriyorsa, kuruluşunuz bu sayfayı uygun alanları gerektiği gibi ekleyecek şekilde özelleştirmelidir.

#### <a name="set-up-a-container-packing-policy"></a>Konteyner paketleme ilkesi ayarlama

Konteyner paketleme ilkesi ayarlamak için aşağıdaki adımları izleyin.

1. Daha önce bir ZPL yazıcı tanımı ayarlamadıysanız ayarlamak için Belge Yönlendirme Aracısını uygulamasını kullanın. Daha fazla bilgi için [Belge yazdırmaya genel bakış](../../fin-ops-core/dev-itpro/analytics/print-documents.md) ve ilgili konuları inceleyin.
1. **Ambar Yönetimi\> Kurulum \> Konteynerler \> Konteyner paketleme ilkeleri**'ne gidin.
1. Eylem bölmesinde konteyner paketleme ilkesi eklemek için **Yeni**'yi seçin.
1. Yeni ilkenin üst bilgisinde aşağıdaki değerleri ayarlayın:

    - **Konteyner paketleme ilkesi:** *Tanıtım paketleme ilkesi*
    - **Açıklama**: İlke için açıklama girin

1. **Genel bakış** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Ambar:** *62*
    - **Son sevkiyat için varsayılan yerleşim:** *Baydoor*
    - **Ağırlık birimi:** *KG*
    - **Konteyner kapatma ilkesi:** *Otomatik serbest bırakma*
    - **Konteyner serbest bırakma ilkesi:** *Son sevk yerleşiminde kullanılabilir hale getir*

1. **Konteyner bildirimi** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Konteyner kapanışında otomatik bildirim:** *Evet*
    - **Konteynere ilişkin bildirim gereksinimleri:** *Taşıma yönetimi*
    - **Konteyner içeriğini yazdır:** *Hayır*

1. **Taşıyıcı etiketini yazdırma** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Konteyner gönderim etiketini yazdır:** *Her zaman*
    - **Yazıcı adı:** Gönderim etiketlerini yazdırması gereken ZPL yazıcısının adı

#### <a name="set-up-a-packing-profile"></a>Paketleme profili ayarlama

Paketleme profili ayarlamak için aşağıdaki adımları izleyin.

1. **Ambar Yönetimi \> Kurulum \> Paketleme \> Paketleme profilleri**'ne gidin.
1. Eylem Bölmesinde, ızgaraya paketleme profili eklemek için **Yeni**'yi seçin.
1. Yeni profil için aşağıdaki değerleri ayarlayın:

    - **Paketleme profili kodu:** *Tanıtım paketleme profili*
    - **Açıklama**: Profil için açıklama girin
    - **Konteyner paketleme ilkesi:** *Tanıtım paketleme ilkesi*
    - **Konteyner kimliği modu:** *Otomatik*
    - **Konteyner türü:** *SmallBox*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>SPS taşıyıcısını kullanmak için müşteri ayarlama

Oluşturduğunuz taşıyıcıyı kullanacak bir müşteri ayarlamak için bu adımları izleyin.

1. **Alacak hesapları \> müşteriler \> Tüm müşteriler**'e gidin.
1. Izgarada, *US-027* müşterisini bulup seçin.
1. Eylem Bölmesi'nde, **Genel** sekmesindeki **Kurulum** grubunda **Taşıyıcı müşteri hesapları**'nı seçin.
1. **Taşıyıcı müşteri hesapları** sayfasındaki Eylem Bölmesinde **Yeni**'yi seçerek ızgaraya bir hesap ekleyin.
1. Yeni hesap için aşağıdaki değerleri ayarlayın:

    - **Sevkiyat taşıyıcısı:** *Tanıtım Taşıyıcısı*
    - **Taşıyıcı müşteri hesap numarası:** *12345* (Bu senaryoda bu değer önemli değildir ancak sonraki bölümde başvurulacaktır.)

### <a name="go-through-the-example-scenario"></a>Örnek senaryoda ilerleyin

Önceki bölümde açıklandığı gibi tüm örnek verileri ayarladıktan sonra örnek senaryo için hazırsınız demektir.

#### <a name="create-a-sales-order-and-process-the-work"></a>Satış siparişi oluşturma ve işi işleme

Satış siparişi oluşturmak için şu adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Satış siparişi oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanını *US-027* olarak ayarlayın.
1. Satış siparişi oluşturmak ve iletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi başlığı** hızlı sekmesinde, **Taşıyıcı müşteri hesap numarası** alanını daha önce bu müşteri için seçtiğiniz değere (*12345*) ayarlayın.
1. **Satış siparişi satırları** bölümünde bir satış satırı ekleyin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0002*
    - **Miktar:** *1*
    - **Tesis:** *6*
    - **Ambar:** *62*

1. **Üst bilgi** görünümüne geçin.
1. **Teslimat** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Sevkiyat taşıyıcısı:** *Tanıtım Taşıyıcısı*
    - **Taşıyıcı hizmeti:** *Tanıtım taşıyıcı hizmeti*

1. **Satırlar** görünümüne dönün. Satış satırları için teslimat şeklini güncelleştirmeniz istenirse **Evet**'i seçin.
1. **Satış siparişi satırları** bölümünde, daha önce ayarladığınız sipariş satırını seçin ve **Stok \> Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Maddeleri malzeme çekme yerleşiminden paketleme istasyonuna taşımak için bir iş oluşturulur.

1. **Satış siparişi satırları** bölümünde **Ambar \> Sevkiyat ayrıntıları**'nı seçin.
1. **Sevkiyat ayrıntıları** sayfasında, sevkiyat kodunu not edin. Paketleme istasyonunda sevkiyatı paketlerken buna ihtiyacınız olacak.
1. Satış siparişine dönmek için **Sevkiyat ayrıntıları** sayfasını kapatın.
1. Satış siparişi numarasını not edin ve **Ambar yönetimi \> İş \> Tüm işler**'e gidin.
1. Sipariş için oluşturulan işi bulmak ve seçmek için satış siparişi numarasını kullanın.
1. Eylem Bölmesindeki **İş** sekmesinde, **İşi tamamla**'yı seçin.
1. **İşi tamamlama** sayfasındaki **Kullanıcı kimliği** alanında bir kullanıcı kodu seçin. Ardından, Eylem Bölmesi'nde **İşi doğrula**'yı seçin.
1. İş doğrulama aşamasından geçerse Eylem Bölmesinde **İşi tamamla**'yı seçin.

    Maddelerin sevk istasyonuna taşınmasının simülasyonu için iş tamamlandı olarak işaretlenir.

#### <a name="pack-the-shipment"></a>Sevkiyatı paketleme

Sevkiyatı paketlemek için şu adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Çalışan** bölümüne gidin ve kullanıcı hesabınızın ambar yönetimi için bir çalışan hesabıyla ilişkilendirildiğinden emin olun.
1. **Ambar yönetimi \> Malzeme çekme ve konteyner kullanımı \> Paket**'e gidin.
1. **Sevk istasyonu seç** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Tesis:** *6*
    - **Ambar:** *62*
    - **Yerleşim:** *Paket*
    - **Paketleme profili kodu:** *Tanıtım paketleme profili*

1. **Tamam**'ı seçin.
1. **Paket** sayfası görüntülenir. Üretim senaryosunda, bir çalışan bir lisans plakası veya sevkiyat kodunu taratır. Ancak, bu senaryo için **Tüm sevkiyatlar** sayfasını açın ve az önce oluşturduğunuz sevkiyatın sevkiyat numarasını arayın. Daha sonra, bu değeri **Paket** sayfasındaki **Plaka veya sevkiyat** alanına girin. Alternatif olarak, az önce not ettiğiniz sevkiyat kodunu girin.
1. Eylem Bölmesinde **Yeni konteyner**'i seçin.
1. Yeni konteynerin ayrıntılarını gösteren iletişim kutusu görüntülenir. Varsayılan değerleri olduğu gibi bırakın ve sonra **Tamam**'ı seçin.
1. **Paket** sayfasındaki **Madde sevki** hızlı sekmesinde yer alan **Tanımlayıcı** alanında, maddeyi paketlemek için *A0002*'yi seçin. Madde konteynere eklenir.
1. Eylem Bölmesi'nde, **Sevk edilecek konteynerler**'i seçin.

    Görüntülenen **Sevk edilecek konteynerler** sayfasında az önce oluşturduğunuz konteyner satırı bulunur. Ancak, henüz taşıyıcıdan gönderim etiketini ve izleme numarasını almadığınız için bu satırdaki **Konteyner bildirim kodu** alanı şu anda boştur.

1. Eylem Bölmesinde **Konteyneri kapat**'ı seçin.
1. **Konteyneri kapat** iletişim kutusunda **Brüt ağırlık** alanını *1 kg* olarak ayarlayıp **Tamam**'ı seçin.

    Şimdi gönderim etiketi, seçtiğiniz ZPL yazıcısında yazdırılmalıdır. Bu etiket, aşağıdaki örneğe benzeyecektir.

    ![Örnek gönderim etiketi](media/sps-label-example.png "Örnek gönderim etiketi")

1. **Konteyner bildirim kodu** ve **Toplam navlun** değerlerinin, taşıyıcıdan alındığı şekilde eklendiğini görürsünüz.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]