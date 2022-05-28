---
title: Bağlama
description: Bu konuda, bağlamanın nasıl etkinleştirileceği ve kullanılacağı açıklanmaktadır.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 26a7bf60912ff1e8a23305e9331d520fe8d65727
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676509"
---
# <a name="anchoring"></a>Bağlama

[!include [banner](../includes/banner.md)]

Bu konuda, bağlama işlemi hakkında ayrıntılı bilgi sağlanmaktadır. Gerekli yapılandırmayı ve bir ambar çalışanı hazırlama konumunu veya yükleme konumunu değiştirdiğinde kullanılan mantığı açıklamaktadır.

Bağlama özelliği, hazırlama veya yükleme konumunu geçersiz kılmanıza olanak tanır. Tüm açık yerleştirmeler daha sonra belirttiğiniz yeni hazırlama veya yükleme konumuna yönlendirilir.

Bu özellik, çalışanların malları sevk ederken daha etkili olmalarına yardımcı olabilir. Burada bazı örnekler verilmiştir:

- Sipariş 1 için ürünleri nokta 1 tarafından hazırlama konumuna yerleştirmesi gereken bir çalışan, önceki yük konumu temizlemediği için bu işlemi tamamlayamaz. Çalışan, bağlantı noktası 1 hazırlama konumunun kullanılabilir hale gelmesini beklemek yerine, bağlantı noktası 2 için hazırlama konumunu kullanmaya karar verir. Bu nedenle çalışan, önerilen hazırlama konumunu geçersiz kılar. İş için kalan tüm ürünlerin koyma konumunu daha sonra bağlantı noktası 2 hazırlama konumuna güncelleştirilir.
- Aynı teslimat için birden fazla çekme yapması gereken bir çalışan, tüm yerleştirilen maddelerin aynı yerde monte edildiğinden emin olabilir. Bu nedenle, ürünleri kamyona yüklemek için daha az zaman gereklidir.

**Bağlayıcı** seçeneğini kullanarak mobil cihaz menü öğeleri için bağlamayı yapılandırırsınız. Bu seçeneği *Evet* olarak ayarlarsanız, sevkiyata veya yüke göre bağlamak isteyip istemediğinizi belirtmek için **Bağlayan** alanını kullanabilirsiniz. **Bağlayan** alanını *Sevkiyat* olarak ayarlarsanız, sonraki açık yerleştirmeler o sevkiyat için yeni konuma değiştirilir. *Yük* olarak ayarlarsanız, sonraki açık yerleştirmeler o yük için yeni konuma değiştirilir.

> [!IMPORTANT]
> Sonraki açık yerleştirmelerin konumu yalnızca aynı iş şablonu satırından oluşturulan iş satırlarında değiştirilecektir. Başka bir deyişle, sistem aynı iş şablonu satırından kaynaklanan yerine koyma satırlarını bağlayacaktır.

Bu konuda, bağlamanın nasıl çalıştığını gösteren bir senaryo sağlanmaktadır. Senaryo sırasında, satış siparişleri kümesi oluşturacak ve bunları ambara serbest bırakacaksınız. Ardından, önerilen hazırlama konumunu geçersiz kılacak ve kalan tüm yerine koyma işlerinin yeni konuma yönlendirildiğini doğrulayacaksınız.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Senaryo önkoşulu: Tanıtım verilerini kullanılabilir hale getirme

Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur. Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği *USMF* olarak ayarladığınızdan emin olun.

## <a name="scenario-setup"></a>Senaryo kurulumu

Örnek senaryo üzerinde çalışmadan önce, ilgili mobil cihaz menü öğesi için bağlamayı etkinleştirmelisiniz.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Bağlamayı etkinleştirmek için mobil cihaz menü öğesini ayarlama

Mobil cihaz menü öğesi için bağlamayı etkinleştirmek için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Liste bölmesinde, *Satış Çekme* adlı kaydı seçin. Bu ada sahip bir kayıt yoksa, oluşturun. Kayıt için aşağıdaki değerleri onaylayın veya ayarlayın:

    - **Menü öğesi adı:** *Satış Çekme*
    - **Başlık:** *Satış Çekme*
    - **Mod:** *İş*
    - **Mevcut işi kullan:** *Evet*
    - **Yöneten:** *Kullanıcı tarafından yönetilen*
    - **Bağlama:** *Evet*

        Bu ayar, sistemin satış çekme sırasında birden fazla iş emri satırını birbirine bağlamasına neden olur.

    - **Bağlayan:** *Yük*

        Bu ayar, sistemin yüke göre bağlanmasına neden olur.

    - **Hedef plakayı geçersiz kıl:** *Evet*
    - **Yerine koyma sırasında plakayı geçersiz kıl:** *Evet*
    - **Kullanıcı tarafından kilitlenen işi koru:** *Evet*
    - **Fazla malzeme çekmeye izin ver:** *Evet*

### <a name="set-up-a-work-template-to-enable-staging"></a>Hazırlamayı etkinleştirmek için iş şablonunu ayarlama

Hazırlamayı etkinleştirmek üzere bir iş şablonu yapılandırmak için aşağıdaki adımları izleyin. Bu yapılandırma, çalışanın sipariş için ürünleri hazırlama konumuna koyduğu senaryoyu destekleyecektir.

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. **İş siparişi türü** alanında *Satış siparişi*'ni seçin.
1. Kılavuzda, **61 SO Aşaması** iş şablonunu seçin.
1. **İş Şablonu Ayrıntıları** bölümünde, aşağıdaki satırların var olduğundan ve burada gösterildiği gibi yapılandırıldığından emin olun:

    - Satır 1:

        - **İş türü:** *Çekme*
        - **Zorunlu:** Seçili (= *Evet*)
        - **İş sınıfı kodu:** *Satış Siparişi Çekme*

    - Satır 2:

        - **İş türü:** *Yerine koyma*
        - **Zorunlu:** Seçili (= *Evet*)
        - **Yönerge kodu:** *Aşama*
        - **İş sınıfı kodu:** *Satış Siparişi Çekme*

    - Satır 3:

        - **İş türü:** *Çekme*
        - **Zorunlu:** Seçili (= *Evet*)
        - **İşi durdur:** *Evet*
        - **İş sınıfı kodu:** *SO Yükü*

    - Satır 4:

        - **İş türü:** *Yerine koyma*
        - **Zorunlu:** Seçili (= *Evet*)
        - **Yönerge kodu:** *Baydoor*
        - **İş sınıfı kodu:** *SO Yükü*

1. Eylem Bölmesinde, sorgu düzenleyiciyi açmak için **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, aşağıdaki satırın mevcut olduğundan emin olun:

    - **Tablo:** *geçici iş hareketleri*
    - **Türetilmiş Tablo:** *Geçici iş hareketleri*
    - **Alan:** *Ambar*
    - **Ölçüt:** *61*

1. **Sıralama** sekmesinde, aşağıdaki satırın mevcut olduğundan emin olun:

    - **Tablo:** *geçici iş hareketleri*
    - **Türetilmiş Tablo:** *Geçici iş hareketleri*
    - **Alan:** *Sevkiyat kodu*
    - **Arama yönü:** *Artan*

1. Ayarlarınızı uygulamak ve sorgu düzenleyicisini kapatmak için **Tamam**'ı seçin. Sorulduğunda, değişiklikleri kabul edin.
1. Eylem Bölmesinde **İş başlığı sonları**'nı seçin.
1. **Alan adı** alanının *Sevkiyat kodu* olarak ayarlandığı satırda, **Bu alana göre gruplandır** onay kutusunun seçili olduğundan emin olun.

### <a name="set-up-license-plates-locations-and-inventory"></a>Plakaları, konumları ve stokları ayarlama

Satış siparişlerini ve sevkiyatları oluşturmadan önce gerekli yerleşimlerin, plakaların ve stokların mevcut olduğundan emin olmalısınız.

1. **Ambar yönetimi \> Kurulum \> Ambar \> Plakalar**'a gidin ve iki plaka oluşturun:

    - MyLP1
    - MyLP2

1. **Ambar yönetimi \> Kurulum \> Ambar \> Yerleşimler**'e gidin ve zaten mevcut değilse aşağıdaki konumları oluşturun.

    | Ambar | Yer   | Yerleşim profili kodu | Bölge kodu   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PICK-06             | KAT     |
    | 61        | 06A01R3S1B | PICK-06             | KAT     |
    | 61        | STAGE01    | STAGE               | *(Boş)* |
    | 61        | STAGE02    | STAGE               | *(Boş)* |
    | 61        | STAGE03    | STAGE               | *(Boş)* |
    | 61        | STAGE04    | STAGE               | *(Boş)* |

1. Aşağıdaki stoğun kullanılabilir olduğundan emin olun. Stoku ayarlamanız gerekiyorsa, el ile hareketler oluşturabilir, stok yenilemeyi veya başka bir akışı kullanabilirsiniz.

    | Madde kodu | Miktar | Ambar | Yer   | Plaka |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Talep oluşturma

Bağlama işlevini denemeden önce biraz talep oluşturmalısınız. Bu senaryoda, aynı müşteri için üç satış siparişi oluşturacaksınız.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. İlk satış siparişini oluşturmak için **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-001*
    - **Ambar:** *61*

1. **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesi boş bir satır içerir. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *1*

1. Araç çubuğunda, ikinci bir satış siparişi satırı eklemek için **Satır ekle**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0002*
    - **Miktar:** *1*

1. Stok ayırmak üzere siparişteki her satış satırı için şu adımları izleyin:

    1. **Satış siparişi satırları** hızlı sekmesinde, satış siparişi satırını seçin.
    1. Araç çubuğunda **Stok \> Ayırma**'yı seçin.
    1. **Rezervasyon** sayfasında, **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.
    1. Eylem bölmesinde, **Kaydet**'i seçin.

1. İkinci bir satış siparişi oluşturmak için 2 ile 6 arasındaki adımları yineleyin. Bu kayıt için aşağıdaki değerleri ayarlayın:

    - **Satış siparişi oluştur** iletişim kutusunda:

        - **Müşteri hesabı:** *US-001*
        - **Ambar:** *61*

    - Satış siparişi satırı 1'de:

        - **Madde numarası:** *A0001*
        - **Miktar:** *2*

    - Satış siparişi satırı 2'de:

        - **Madde numarası:** *A0002*
        - **Miktar:** *2*

1. Satış siparişi 2'deki her satırı ayırmak için 7. adımı tekrarlayın.
1. Üçüncü bir satış siparişi oluşturmak için 2 ile 6 arasındaki adımları yineleyin. Bu kayıt için aşağıdaki değerleri ayarlayın:

    - **Satış siparişi oluştur** iletişim kutusunda:

        - **Müşteri hesabı:** *US-001*
        - **Ambar:** *61*

    - Satış siparişi satırı 1'de:

        - **Madde numarası:** *A0001*
        - **Miktar:** *3*

    - Satış siparişi satırı 2'de:

        - **Madde numarası:** *A0002*
        - **Miktar:** *3*

1. Satış siparişi 3'teki her satırı ayırmak için 7. adımı yineleyin.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Yük oluşturmak ve ambara serbest bırakmak için yük planlama çalışma ekranını kullanma

Bu senaryo için oluşturduğunuz siparişler için bir yük oluşturmak ve ardından bunu ambara serbest bırakmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.
1. **Satış satırları** sekmesinde, satış siparişi 1 ve satış siparişi 2 için tüm satış siparişi satırlarını bulun ve seçin.
1. Eylem Bölmesinde **Arz ve talep** sekmesindeki **Ekle** grubunda **Yeni yüke**'yi seçin.
1. **Yük şablonu ataması** iletişim kutusundaki **Yük şablonu kimliği** alanında, *Stnd Yük Şablonu* gibi bir yük şablonu seçin.
1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Yükler** bölümünde, oluşturduğunuz yükü bulun ve seçin.
1. Araç çubuğunda, **Serbest bırakma \> Ambara serbest bırakma**'yı seçin.
1. **Yükü ambara serbest bırak** iletişim kutusunda, seçilen yükü ambara serbest bırakmak için **Tamam**'ı seçin.
1. Oluşturulan işi görüntülemek için **Ambar yönetimi \> İş \> Tüm işler**'e gidin. Her sevkiyat için bir tane olmak üzere iki yeni iş kimliği bulmalısınız. Her iş kimliği, çekme konumlarından hazırlama konumuna ve hazırlama konumundan baydoor'a stok getiren çekme ve yerine koyma satırlarına sahiptir. Bir sonraki yordamda kullanmanız gerekeceğinden ilk sevkiyat için **İş kodu** değerini not edin.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>İlk sevkiyat için hazırlama konumuna satış siparişi çekme

1. Ambar *61*'de bir çalışan olarak Warehouse Management mobil uygulamasında oturum açın. (Standart demo verilerinde, kullanıcı kimliği olarak _61_ ve parola olarak _1_ kullanarak oturum açabilirsiniz.)
1. Ana menüde **Giden**'i seçin.
1. **Giden** menüsünden **Satış Çekme**'yi seçin.
1. **Kod** alanını seçin ve ardından ilk sevkiyat için iş kodunu girin.
1. Girişinizi onaylayın.
1. **LP** alanına, ilk madde için plaka numarası girin (*MyLP1*).
1. Girişinizi onaylayın.
1. **Hedef LP** alanına herhangi bir sayı girin (hedef plakanın zaten mevcut olması gerekmez).

    İşlenen dalgadan aynı hedef plakaya oluşturulan tüm satırları çekeceksiniz.

1. Girişinizi onaylayın.
1. **LP** alanına ikinci öğe (*MyLP2*) için bir plaka numarası girin.
1. Girişinizi onaylayın.

    Çalışanın şimdi siparişi topladığını ancak işte belirtilen hazırlama konumuna ulaştıklarında, alanın zaten dolu olduğunu gördüğünü düşünelim. Ancak çalışan başka bir yakındaki konumun (*STAGE03*) kullanılabildiğini görebiliyor. Bu nedenle, hazırlama konumunu değiştirmek ister. Bağlama özelliği etkin olduğundan, sistem bunun için hazırlama konumunu ve ilgili tüm işleri otomatik olarak güncelleştirir.

1. Önerilen hazırlama konumunu geçersiz kılmak için **Konumu geçersiz kıl**'ı seçin.
1. **İş özel durumları** alanında, *Hazırlama şeridi değiştirildi*'yi belirtin.
1. **Konum** alanına yeni bir hazırlama konumu (*STAGE03*) girin.
1. Girişinizi onaylayın. Bir "İş tamamlandı" iletisi alırsınız.
1. **Ambar yönetimi \> İş \> Tüm çalışmalar**'a gidin.
1. İlk sevkiyat için iş kodunu açın. Hazırlama konumunun mobil cihaz kullanılarak tanımlanan yeni konuma (*STAGE03*) güncelleştirildiğini doğrulayın.
1. İkinci sevkiyat için iş kodunu açın. Bağlama kurulumu nedeniyle hazırlama konumunun yeni hazırlama konumuna (*STAGE03*) güncelleştirildiğini doğrulayın.

> [!NOTE]
> Aynı hazırlama konumuna sahip olan ve aynı iş şablonu satırından oluşturulan kalan tüm açık yerleştirme iş satırlarının konumu, yeni konuma güncelleştirilir.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Mevcut yüklemeye yeni satış siparişini eklemek için yük planlama çalışma ekranını kullanma

Yüklemeye bir sipariş eklemek ve sonra ambara serbest bırakmak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.
1. **Satış satırları** sekmesinde, satış siparişi 3 için tüm satış siparişi satırlarını bulun ve seçin.
1. Eylem Bölmesi'nde, **Arz ve talep** sekmesinde, **Ekleme** grubunda, seçili sipariş satırlarını mevcut yüke eklemek için **Mevcut yüke**'yi seçin.
1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Yükler** bölümünde, önceki adımlardan yükü bulun ve seçin.
1. **Serbest bırak \> Ambara serbest bırak**'ı seçin.
1. **Yükü ambara serbest bırak** iletişim kutusunda, seçilen yükü ambara serbest bırakmak için **Tamam**'ı seçin.
1. Oluşturulan işi görüntülemek için **Ambar yönetimi \> İş \> Tüm işler**'e gidin. Bir sonraki yordamda kullanmanız gerekeceğinden **İş kodu** değerini not edin.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Üçüncü sevkiyat için hazırlama konumuna satış siparişi çekme

1. Mobil cihazınızdan Ambar *61*'de çalışan olarak oturum açın.
1. Ana menüde **Giden**'i seçin.
1. **Giden** menüsünden **Satış Çekme**'yi seçin.
1. **Kod** alanını seçin ve ardından üçüncü sevkiyat için iş kodunu girin.
1. Girişinizi onaylayın.
1. **LP** alanına, ilk madde için plaka numarası girin (*MyLP1*).
1. Girişinizi onaylayın.
1. **Hedef LP** alanına herhangi bir sayı girin (hedef plakanın zaten mevcut olması gerekmez).
1. Girişinizi onaylayın.
1. **LP** alanına ikinci öğe (*MyLP2*) için bir plaka numarası girin.
1. Girişinizi onaylayın.

    İlk yükte olduğu gibi, çalışanın belirtilen hazırlama konumunu kullanılamaz olarak bulduğunu varsayalım. Bu nedenle, farklı bir hazırlama konumu (*STAGE04*) kullanmak ister.

1. Önerilen hazırlama konumunu geçersiz kılmak için **Konumu geçersiz kıl**'ı seçin.
1. **İş özel durumları** alanında, *Hazırlama şeridi değiştirildi*'yi belirtin.
1. **Konum** alanına yeni bir hazırlama konumu (*STAGE04*) girin.
1. Girişinizi onaylayın. Bir "İş tamamlandı" iletisi alırsınız.
1. **Ambar yönetimi \> İş \> Tüm çalışmalar**'a gidin.
1. İlk sevkiyat için iş kodunu açın. Kalan açık yerine koyma satırı, tamamlanmış yerine koyma satırının iş şablonu satırına karşılık gelmediğinden, hazırlama konumunun yeni hazırlama konumuna (*STAGE04*) güncelleştirilmediğini doğrulayın.
1. İkinci sevkiyat için iş kodunu açın. Hazırlama konumunun yeni hazırlama konumuna (*STAGE04*) güncelleştirilmediğini doğrulayın çünkü hazırlama konumu, tamamlanmış yerine koyma satırının hazırlama konumuna karşılık gelmiyor. Başka bir deyişle, tamamlanan yerine koyma işi satırı ve kalan açık iş satırının farklı hazırlama konumları vardır ve bu durumda yalnızca aynı hazırlama konumlarına sahip satırlar güncelleştirilir.
1. Üçüncü sevkiyat için iş kodunu açın. Hazırlama konumunun yeni hazırlama konumuna (*STAGE04*) güncelleştirildiğini doğrulayın.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
