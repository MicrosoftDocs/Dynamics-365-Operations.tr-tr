---
title: Planlanmış çapraz sevk
description: Bu konuda, bir sipariş için gereken stok miktarının kabulden veya oluşturma aşamasından doğru çıkış noktasına veya hazırlama alanına kadar yönlendirildiği, ileri düzeyde planlanmış çapraz sevk açıklanmaktadır. Gelen kaynaktan kalan tüm stok, normal yerine koyma işlemiyle doğru depolama yerleşimine yönlendirilir.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: fb598b3ac7dd72e8c500f0c2eaf07462009c67f7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970318"
---
# <a name="planned-cross-docking"></a>Planlanmış çapraz sevk

[!include [banner](../includes/banner.md)]

Bu konuda, ileri düzeyde planlı çapraz sevk açıklanmaktadır. Çapraz sevk, bir sipariş için gereken stok miktarının kabulden veya oluşturma aşamasından doğru çıkış noktasına veya hazırlama alanına kadar yönlendirildiği bir ambar sürecidir. Gelen kaynaktan kalan tüm stok, normal yerine koyma işlemiyle doğru depolama yerleşimine yönlendirilir.

Çapraz sevk, çalışanların zaten bir giden sipariş için işaretlenmiş olan stokun gelen yerine koyma ve giden çekme işlemini atlamasını sağlar. Bu sayede stok işlem sayısı olabildiğince azaltılır. Ek olarak, sistemle daha az etkileşim olduğu için, ambardaki zaman ve alan tasarrufları artar.

Çapraz sevkin çalıştırılabilmesi için, kullanıcının tedarik kaynağının ve çapraz sevke ilişkin diğer gereksinimler dizisinin belirtildiği yeni bir çapraz sevk şablonu yapılandırması gerekir. Giden sipariş oluşturulurken, satır, aynı maddeyi içeren bir gelen siparişe göre işaretlenmelidir.

Her gelen sipariş alındığında, çapraz sevk kurulumu çapraz sevk gereksinimini otomatik olarak belirler ve yerleşim yönergesinin kurulumuna göre, gereken miktar için hareket işini oluşturur.

> [!NOTE]
> Bu becerinin ayarı Ambar yönetimi parametrelerinde açık olsa bile, çapraz sevk işi iptal edildiği zaman stok hareketlerinin **kaydı silinmez**.

## <a name="turn-on-the-planned-cross-docking-feature"></a>Planlanmış çapraz sevk özelliğini açın

İleri düzeyde planlanmış çapraz sevki kullanabilmeniz için özelliğin sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Planlanmış çapraz sevk*

## <a name="setup"></a>Ayar

### <a name="regenerate-load-posting-methods"></a>Yükleme deftere nakil yöntemlerini yeniden oluşturma

Planlanmış çapraz sevk, bir yükleme deftere nakil yöntemi olarak uygulanır. Özelliği açtıktan sonra, yöntemleri yeniden oluşturmanız gerekir.

1. **Ambar yönetimi \> Kurulum \> Yükleme deftere nakil yöntemleri**'ne gidin.
1. Eylem bölmesinde, **Yöntemleri yeniden oluştur**'u seçin.

    Yeniden oluşturma işlemi tamamlanınca **Yöntem adı** değeri *planCcrossDocking* olan bir yöntem göreceksiniz.

1. Sayfayı kapatın.

### <a name="create-a-cross-docking-template"></a>Bir çapraz sevk şablonu oluşturma

1. **Ambar yönetimi \> Kurulum \> İş \> Çapraz sevk şablonları**'na gidin.
1. Eylem bölmesinde, bir şablon oluşturmak için **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Sıra:** *1*

        Bu alan, şablonların değerlendirildiği sırayı tanımlar.

    - **Çapraz sevk şablonu kodu:** *51*
    - **Açıklama:** *Ambar 51*
    - **Talep serbest bırakma ilkesi:** *Tedarik girişinden önce*
    - **Ambar:** *51*

1. **Planlama** hızlı sekmesindeki kurulum, şablonun nasıl çalıştığını denetler. Aşağıdaki değerleri ayarlayın:

    - **Talep gereksinimleri:** *Yok*

        Bu alan talep stoku gereksinimlerini tanımlar. Talebin serbest bırakmadan önce tedarikle bağlantılı olması gerekiyorsa *İşaretleme*'yi seçin. Talebin serbest bırakmadan önce tedarike göre sipariş rezervasyonunun yapılması gerekiyorsa *Sipariş rezervasyonu*'nu seçin.

    - **Bulma türü:** *Sevkiyat yerleşimleri*

        Bu alan, çapraz sevk işinin sevk irsaliyesindeki hazırlama/yükleme yerleşimlerini kullanıp kullanmayacağını veya kendi hazırlama/yükleme yerleşimlerini bulmak için yerleşim yönergeleri kullanıp kullanmayacağını tanımlar.

    - **İş şablonu:** Bu alanı boş bırakın.

        Bu alan, çapraz sevk işi oluşturulduğunda kullanılması gereken iş şablonunu tanımlar.

    - **Tedarik girişinde yeniden doğrula:** *Hayır*

        Bu seçenek, tedarik girişi sırasında tedarikin yeniden doğrulanıp doğrulanmayacağını tanımlar. Bu seçenek *Evet* olarak ayarlanırsa , maksimum zaman aralığı ve sona erme gün sayısı aralığı da işaretlenir.

    - **Zaman aralığını doğrula:** *Evet*

        Bu seçenek, bir tedarik kaynağı seçildiğinde maksimum zaman aralığının değerlendirilip değerlendirilmeyeceğini tanımlar. Bu seçenek *Evet* olarak ayarlanırsa, maksimum ve minimum zaman aralıklarıyla ilgili alanlar kullanılabilir duruma gelir.

    - **Maksimum zaman aralığı:** *5*

        Bu alan, tedarik varışı ve talep çıkışı arasında izin verilen maksimum süreyi tanımlar.

    - **Maksimum zaman aralığı birimi:** *Gün sayısı*
    - **Minimum zaman aralığı:** *0*

        Bu alan, tedarik varışı ve talep çıkışı arasında izin verilen minimum süreyi tanımlar.

    - **Minimum zaman aralığı birimi:** *Gün sayısı*
    - **Sona erme gün sayısı aralığı:** *0*

        *İlk sona eren ilk çıkar (FEFO) ölçütleri:* Bu alan, ambardaki mevcut ilk sona eren toplu işlemin bitiş tarihi ve alınmakta olan toplu işlem arasındaki maksimum gün sayısını tanımlar.

1. **Tedarik kaynakları** hızlı sekmesinde, bu şablon için geçerli olan tedarik tiplerini belirtirsiniz. **Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** *1*
    - **Tedarik kaynağı:** *Satınalma siparişi*

### <a name="create-a-work-class"></a>İş sınıfı oluşturma

1. **Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.
1. Eylem bölmesinde, bir iş sınıfı oluşturmak için **Yeni**'yi seçin.
1. Aşağıdaki değerleri ayarlayın:

    - **İş sınıfı kodu:** *CrossDock*
    - **Açıklama:** *Çapraz Sevk*
    - **İş emri türü:** *Çapraz sevk*

### <a name="create-a-work-template"></a>İş şablonu oluşturma

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. **İş emri türü** alanını *Çapraz sevk* olarak ayarlayın.
1. Eylem bölmesinde, **Genel bakış** sekmesine satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** *1*
    - **İş şablonu:** *51 Çapraz Sevk*
    - **İş şablonu açıklaması:** *51 Çapraz Sevk*

1. **İş Şablonu Ayrıntıları** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **İş Şablonu Ayrıntıları** hızlı sekmesinde, kılavuza satır için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Çekme*
    - **İş sınıfı kodu:** *CrossDock*

1. **Yeni**'yi seçerek bir satır daha ekleyin ve üzerinde aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Yerine koyma*
    - **İş sınıfı kodu:** *CrossDock*

1. **Kaydet**'i seçin ve *51 Çapraz Sevk* şablonu için **Geçerli** onay kutusunun işaretlendiğini onaylayın.

> [!NOTE]
> *Çekme* ve *Koyma* iş türleri için iş sınıfı kodları aynı olmalıdır.

### <a name="create-location-directives"></a>Yerleşim yönergeleri oluşturma

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Sol bölmede, **İş emri türü** alanını *Çapraz sevk* olarak ayarlayın.
1. Eylem bölmesinde **Yeni**'yi seçin ve aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** *1*
    - **Ad:** *51 Çapraz Sevk Koyma*
    - **İş türü:** *Yerine koyma*
    - **Tesis:** *5*
    - **Ambar:** *51*

1. **Satırlar** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Satırlar** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Başlangıç miktarı:** *1*
    - **Son miktar:** *1000000*

1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Konum Yönerge Eylemleri** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Ad:** *Baydoor*
    - **Sabit yerleşim kullanımı:** *Sabit ve sabit olmayan yerleşimler*

1. **Yerleşim Yönergesi Eylemleri** araç çubuğunda **Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. Sorgu düzenleyicisini açmak için **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, aşağıdaki iki satırın yapılandırıldığından emin olun:

    - Satır 1:

        - **Tablo:** *Yerleşimler*
        - **Türetilmiş Tablo:** *Yerleşimler*
        - **Alan:** *Ambar*
        - **Ölçüt:** *51*

    - Satır 2:

        - **Tablo:** *Yerleşimler*
        - **Türetilmiş Tablo:** *Yerleşimler*
        - **Alan:** *Yerleşim*
        - **Ölçüt:** *Baydoor*

1. Sorgu düzenleyicisini kapatmak için **Tamam**'ı seçin.

### <a name="create-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi oluşturma

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Sol bölmedeki menü öğeleri listesinde, **Satınalma yerine koyma**'yı seçin.
1. **Düzenle** öğesini seçin.
1. **İş sınıfları** hızlı sekmesinde, kılavuza satır eklemek için **Yeni**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **İş sınıfı kodu:** *CrossDock*
    - **İş emri türü:** *Çapraz sevk*

1. **Kaydet**'i seçin.

## <a name="scenario"></a>Senaryo

### <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

Tedarik kaynağı olarak bir satınalma siparişi oluşturmak için bu adımları izleyin.

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satın alma siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Satıcı hesabı:** *104*
    - **Ambar:** *51*

1. **Tamam**'ı seçin ve sipariş numarasını not alın.
1. **Satınalma siparişi satırları** hızlı sekmesine yeni bir satır eklenir. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *5*

### <a name="create-a-sales-order"></a>Satış siparişi oluştur

Talep kaynağı olarak bir satış siparişi oluşturmak için bu adımları izleyin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-002*
    - **Ambar:** *51*

1. **Tamam**'ı seçin.
1. **Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *3*

### <a name="create-planned-cross-docking"></a>Planlanmış çapraz sevk oluşturma

Planlanmış çapraz sevki satış siparişinden oluşturmak için bu adımları izleyin.

1. Az önce oluşturduğunuz satış siparişinin **Satış siparişi ayrıntıları** sayfasında, eylem bölmesindeki **Ambar** sekmesinde, **Eylemler** grubunda **Ambara serbest bırak**'ı seçin.

    Ambara serbest bırakma eylemi, satış siparişi satırı için bir sevkiyat ve yükleme satırı oluşturur ve stok tahsis etmeye çalışır.
    
    Bir bilgi iletisi alırsınız. Ayrıca şu uyarı iletisini alırsınız: "Dalga XXXX için iş oluşturulmadı. Ayrıntılar için iş oluşturma geçmişi günlüğüne bakın." Ambarda stok bulunmadığı için bu davranış olağandır.

1. **Satış siparişi satırları** hızlı sekmesinde **Ambar** menüsünde **Sevkiyat ayrıntıları**'nı seçin.

    **Sevkiyat ayrıntıları** sayfası görüntülenir ve satış siparişi için oluşturulan sevkiyatı gösterir.

1. **Yük satırları** hızlı sekmesinde, **Planlanmış çapraz sevk miktarı** alanının *3* olarak ayarlandığına dikkat edin. Ambarda stok mevcut olmadığı halde çapraz sevk şablonunda tanımlanan zaman aralığında geçerli tedarik kaynağı geleceği için, çapraz sevk miktarı oluşturulmuştur.
1. **Yük satırları** hızlı sekmesinde, oluşturulan çapraz sevkin ayrıntılarını görüntülemek için **Planlanmış çapraz sevk**'i seçin.

## <a name="process-the-cross-docking"></a>Çapraz sevki işleme

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Ambarlama mobil uygulamasında satınalma siparişini teslim alma

Sistem, satınalma siparişindeki 5 miktarını teslim alma yerleşimine alır ve iki iş parçası oluşturur.

Oluşturulan ilk iş kodunun **İş emri türü** değeri *Çapraz sevk*'tir ve satış siparişine bağlıdır. Miktar değeri 3'tür ve hemen sevk edilebilmesi için son sevkiyat yerleşimine yönlendirilir.

Oluşturulan ikinci iş kodunun **İş emri türü** değeri *Satınalma siparişleri*'dir ve satınalma siparişine bağlıdır. Kalan miktarı 2 olan bu parça çapraz sevk edilmemiştir ve depoda yerine koymaya yönlendirilir.

1. Mobil cihazda *51* kodlu ambarda bir kullanıcı olarak oturum açın.
1. **Gelen \> Satınalma Teslim Alma**'ya gidin.
1. **PONum** alanına satınalma sipariş numaranızı girin.
1. **Miktar** alanına *5* girin.
1. **Tamam**'ı seçin.
1. Sonraki sayfada, **Madde** alanını *A0001* olarak ayarlayın.
1. **Tamam**'ı seçin.
1. Sonraki sayfada, **Tamam**'ı seçerek **PONum**, **Madde** ve **Miktar** değerlerini onaylayın.

    Bir "İş Tamamlandı" iletisi alırsınız.

1. Çıkmak için **İptal**'i seçin.

### <a name="put-away-to-cross-docking-and-bulk"></a>Çapraz sevk ve toplu işlem için yerine koyma

Şu anda her iki iş kodunun da hedef plakası aynıdır. Sonraki adımları tamamlamak için iş kodunu ve hedef plaka kodunu almanız gerekir. Bu bilgileri satınalma siparişi satırı ve satış siparişi satırı ile ilgili iş ayrıntılardan edinebilirsiniz. Alternatif olarak, **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidip **Ambar** değerinin *51* olduğu işi filtreleyebilirsiniz.

1. Mobil cihazda **Gelen \> Satın alma yerine koyma**'ya gidin ve işin hedef plakasını girin.
1. **Kod** alanına, iş ayrıntılarından alınan hedef plaka kodunu girin.

    Çapraz sevk çekme sayfası, malzeme çekme yerleşimini (*RECV*), hedef plakayı ( *plaka*), maddeyi (*A0001*) ve miktarı ( *3*) gösterir.

1. **Tamam**'ı seçin.
1. **Hedef Plaka** alanına, sevkiyat yerleşimine yerleştirilmesi (çapraz sevk edilmesi) gereken plaka kodu için bir hedef plaka girin. İstediğiniz herhangi bir plaka kodunu seçebilirsiniz.
1. **Tamam**'ı seçin.
1. Sonraki sayfada, **Kod** alanına, hedef plaka kodunu girin.
1. **Tamam**'ı seçin.
1. Kalan 2 miktarını çekmek için işi onaylayın ve **Tamam**'ı seçin.
1. Sonraki sayfada, malzeme çekme işlemini bitirmek ve yerine koyma işlemine başlamak için **Bitti**'yi seçin.

    Mobil uygulama, size, maddenin yerleştirileceği yerleşimi ve plakayı verir.

1. **Tamam**'ı seçerek toplu depolama **Koyma** işlemini onaylayın.
1. Sonraki sayfada, **Tamam**'ı seçerek çapraz sevk **Koyma** işlemini onaylayın.

    Bir "İş Tamamlandı" iletisi alırsınız.

1. Çıkmak için **İptal**'i seçin.

Aşağıdaki şekil, tamamlanmış çapraz sevk işinin Microsoft Dynamics 365 Supply Chain Management'ta nasıl görünebileceğini gösteriyor.

![Tamamlanmış çapraz sevk işi](media/PlannedCrossDockingWork.png "Tamamlanmış çapraz sevk işi")
