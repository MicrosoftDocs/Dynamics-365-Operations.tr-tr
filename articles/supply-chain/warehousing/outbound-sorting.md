---
title: Giden sıralama
description: Bu konuda giden tasnifi hakkında bilgiler verilmiştir. Bu işlev küçük konteynerleri kullanmayı kolaylaştırır ve ambar çalışanlarının kamyondaki palet kapasitesini daha iyi planlamasına ve organize etmesine yardımcı olur.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 84c4ec83ed16762e6c3c1a22425cf60e5b3ae8da
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439718"
---
# <a name="outbound-sorting"></a>Giden sıralama

[!include [banner](../includes/banner.md)]

Bu işlev küçük konteynerleri kullanmayı kolaylaştırır ve ambar çalışanlarının kamyondaki palet kapasitesini daha iyi planlamasına ve organize etmesine yardımcı olur. Giden tasnif işlevini kullandığınızda, paketleme istasyonuna geldikten sonra paketlenen konteynerlerin doğru palete tasnif edilmesini sağlayabilirsiniz. Ayrıca bir paketleme hiyerarşisi de oluşturabilirsiniz.

Bu işlev, paketleme işleviyle paketlenmiş konteynerlerden palet oluşturmanızı sağlar. Konteyner, orijinal sevk akışında olduğundan son sevkiyat yerleşimine gönderilmez. Bunun yerine, çalışanlar konteyneri kapatabilir ve bunu bir tasnif türündeki yerleşime taşıyabilir. Böylece konteynerleri her birinin plakası bulunan (LP) konumlara göre tasnif edebilirler. Konteynerler tasnif edildikten sonra, tüm plakayı konum yönergelerine veya kendi gereksinimlerinize göre nihai sevkiyat noktasına veya hazırlama yerleşimlerine göndermek için iş oluşturulabilir. Ayrıca, tasnif konumunu kapatma eylemi stoğu anında son sevkiyat yerleşimine taşıyabilir ve siparişe çekebilir.

## <a name="turn-on-the-outbound-sorting-feature"></a>Giden tasnif özelliğini açma

Özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Giden tasnif*

## <a name="setup"></a>Ayar

Bu senaryo için standart **USMF** demo verilerini ve ambar *62*'yi kullanmanız gerekir. Ayrıca, aşağıdaki alt bölümlerde açıklanan kurulumu da tamamlamanız gerekir.

### <a name="set-up-a-wave-template"></a>Dalga şablonu ayarlama

Bu kurulum satır ambara serbest bırakıldığında dalgayı otomatik olarak işler ve işi oluşturur.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. Şablon listesinde **Ambar 62**'yi seçin.
1. **Genel** hızlı sekmesinde, **Ambara serbest bırakıldığında dalgayı işle** seçeneğinin *Evet* olarak ayarlandığından emin olun.

### <a name="set-up-a-worker"></a>Çalışan ayarlama

Paketleme istasyonu bir yerleşim olarak kabul edilir. Ambalaj istasyonunda oturum açan ambar çalışanları, yalnızca söz konusu belirli paketleme yerleşiminde planlanan sevkiyatlar ve konteynerleri görebilir ve bunlar üzerinde çalışabilirler. Microsoft Dynamics 365'te oturum açan bir kullanıcının Ambar yönetiminde çalışan olarak ayarlanması gerekir. Kullanıcının adı iş kullanıcıları listesinde görünmüyorsa, bunu eklemek için aşağıdaki yordamı kullanın.

> [!NOTE]
> Bu adımlarda, kullanıcının sistemde zaten var olduğu ve **İnsan Kaynakları** modülünde personel veya çalışan olarak ilişkilendirilmiş olduğu varsayılır.

1. **Ambar yönetimi \> Kurulum \> Çalışan**'a gidin.
1. **Yeni**'yi seçin.
1. **Çalışan** alanında, personel listesinden hedef kullanıcıyı seçin.
1. **Seç** öğesini seçin.
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Kullanıcılar** hızlı sekmesinde, mobil cihaz hesabı oluşturmak için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Kullanıcı Kimliği:** Benzersiz bir kimlik girin.
    - **Kullanıcı adı:** Kimlik için bir ad girin.
    - **Varsayılan ambar:** *62*
    - **Menü adı:** *Ana*

1. Eylem bölmesinde, **Kaydet**'i seçin.
1. **Parola ayarla** iletişim kutusu görüntülenir; bu iletişim kutusunda kullanıcının mobil uygulamada oturum açmak için kullanabileceği basit bir parola oluşturabilirsiniz. Aşağıdaki değerleri ayarlayın:

    - **Parola:** Basit bir parola girin.
    - **Parolayı onayla:** Aynı parolayı yeniden girin.

1. **Parola ayarlama**'yı seçin.

    İşlem Merkezindeki bir bildirim, oluşturduğunuz kullanıcı için parolanın ayarlanmış olduğunu bildirir.

### <a name="create-a-location-type"></a>Yerleşim türü oluşturma

1. **Ambar yönetimi \> Kurulum \> Ambar \> Yerleşim türleri** öğesine gidin.
1. Eylem Bölmesinde, bir yerleşim türü oluşturmak için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Yerleşim türü:** *TASNİF*
    - **Açıklama:** *Tasnif*

1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-warehouse-management-parameters"></a>Ambar yönetimi parametreleri ayarlama

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Genel** sekmesinde **Yerleşim türleri** hızlı sekmesinde **Tasnif yerleşimi türü** alanını *TASNİF* olarak ayarlayın.
1. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-a-location-profile"></a>Yerleşim profili ayarlama

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Yerleşim profili kimliği:** *Tasnif*
    - **Ad:** *Tasnif*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Yerleşim biçimi:** *ASRB* (Koridor-Dolap-Raf-Bölme)
    - **Yerleşim türü:** *TASNİF*
    - **Plaka izleme kullan:** *Evet*
    - **Karışık maddelere izin ver:** *Evet* (Bu seçeneği *Evet* olarak ayarladığınızda **Karışık stok toplu işlemlerine izin ver** seçeneği otomatik olarak *Evet*'e ayarlanır ve bağımsız olarak değiştirilemez.)

1. **Kaydet**'i seçin.

### <a name="set-up-a-location"></a>Yerleşim ayarlama

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konumlar** öğesine gidin.
1. Başlıkta, **Yerleşim için denetleme basamakları oluştur** onay kutusunu temizleyin.
1. Eylem Bölmesinde, bir yerleşim oluşturmak için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Ambar:** *62*
    - **Yerleşim:** *SORT*
    - **Yerleşim profili kimliği:** *TASNİF*

1. **Kaydet**'i seçin.

### <a name="set-up-an-outbound-sorting-template"></a>Giden tasnif şablonu ayarlama

Giden tasnif şablonu, işin tasnif yerleşiminin dışında oluşturulup oluşturulmayacağını ve tasnifin el ile mi yoksa otomatik olarak mı yapılacağını belirler.

Bu senaryo için, paketleme istasyonundan sonra palet oluşturmak üzere bir tasnif şablonu oluşturacaksınız.

1. **Ambar Yönetimi \> Kurulum \> Paketleme \> Giden tasnif şablonu**'na gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni şablonun üst bilgisinde aşağıdaki değerleri ayarlayın:

    - **Giden tasnif şablonu kodu:** *AutoWork*
    - **Açıklama:** *Otomatik İş Oluşturma*
    - **Giden tasnif şablon türü:** *Konteyner*
    - **Ambar:** *62*
    - **Yerleşim:** *SORT*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Tasnif doğrulaması:** *Konum tarama*
    - **Pozisyon kapanışında iş oluştur:** *Evet*

        Bu seçenek *Evet* olarak ayarlandığında, konum kapatıldığı zaman stoğu nihai sevkiyat yerleşimine taşımak için iş oluşturulur. *Hayır* olarak ayarlanırsa, konum kapatıldığında stok anında sipariş için çekilir.

    - **Pozisyon atama:** *Otomatik*

        Bu alan *El ile* olarak ayarlandığında, kullanıcının her zaman stoğun hangi konumda sıralanacağını belirtmesi gerekir. *Otomaik* olarak ayarlandığında sistem tasnif şablonu dökümlerini temel alarak mümkün olduğunda stoğu otomatik olarak bir konuma yönlendirir.

1. Eylem bölmesinde **Sorguyu düzenle** seçeneğini kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. Eylem bölmesinde **Sorgu düzenle**'yi seçin.
1. Sorgu düzenleyicisinde, **Tasnif** sekmesinde, aşağıdaki değerlere sahip bir satır ekleyin:

    - **Tablo:** *Sevkiyatlar*
    - **Türetilmiş tablo:** *Sevkiyatlar*
    - **Alan:** *Taşıyıcı hizmeti*

        Bu değeri seçtiğinizde sonra şu iletiyi alabilirsiniz: "Taşıyıcı hizmeti alanı bir dizin alanı değil. Bunun üzerinde sıralama eklemek istiyor musunuz?" **Evet**'i seçin.

    - **Arama yönü:** *Artan*

1. **Tamam**'ı seçin.
1. Aşağıdaki iletiyi alabilirsiniz: "Gruplama sıfırlanacak, devam edilsin mi?" **Evet**'i seçin.

    Eylem Bölmesindeki **Giden tasnif şablonu dökümleri** düğmesi kullanılabilir duruma gelir.

1. Eylem Bölmesinde, **Giden tasnif şablonu dökümleri**'ni seçin.
1. **Giden tasnif ölçüsü** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Referans tablosu adı:** *Sevkiyatlar*
    - **Referans alanı adı:** *Taşıyıcı hizmeti*
    - **Alana göre gruplandır:** Sevkıyatları taşıyıcı hizmetine göre gruplandırmak için bu onay kutusunu seçin.

1. Ayarlarınızı kaydedip iletişim kutusunu kapatmak için **Tamam**'ı seçin.

### <a name="set-up-container-packing-policies"></a>Konteyner paketleme ilkelerini ayarlama

1. **Ambar yönetimi\> Kurulum \> Konteynerler \> Konteyner paketleme ilkeleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni ilkenin üst bilgisinde aşağıdaki değerleri ayarlayın:

    - **Konteyner paketleme ilkesi:** *Tasnif*
    - **Açıklama:** *Tasnif*

1. **Genel bakış** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Ambar:** *62*
    - **Tasnif için varsayılan yerleşim:** *TASNİF*
    - **Ağırlık birimi:** *kg*
    - **Konteyner kapatma ilkesi:** *Otomatik serbest bırakma*
    - **Konteyner serbest bırakma ilkesi:** *Giden tasnif konumuna konteyner ata*

1. **Kaydet**'i seçin.

### <a name="set-up-packing-profiles"></a>Paketleme profilleri ayarla

Tasnif işleviyle birlikte kullanılacak yeni bir paketleme profili oluşturun.

1. **Ambar yönetimi \> Kurulum \> Paketleme \> Paketleme profilleri**'ne gidin.
1. Eylem Bölmesinde, bir satır oluşturmak için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **Paketleme profili kodu:** *Tasnif*
    - **Açıklama:** *Tasnif*
    - **Konteyner paketleme ilkesi:** *Tasnif*
    - **Konteyner kimliği modu:** *Otomatik*
    - **Konteyner türü:** *Kutu-Büyük*
    - **Konteyner kapatıldığında otomatik konteyner oluştur:** İşareti kaldırıldı (= *Hayır*)

1. **Kaydet**'i seçin.

### <a name="set-up-work-classes"></a>İş sınıflarını ayarlama

Tasnif ile birlikte kullanılacak bir iş sınıfı ayarlayın.

1. **Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.
1. Eylem Bölmesinde, tasnif için iş sınıfı oluşturmak için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **İş sınıfı kodu:** *Tasnif*
    - **Açıklama:** *Tasnif*
    - **İş emri türü:** *Tasnif edilmiş stok çekme*

1. **Kaydet**'i seçin.

### <a name="set-up-mobile-device-menu-items"></a>Mobil cihaz menü öğeleri ayarlama

#### <a name="set-up-a-new-pallet-menu-item"></a>Yeni palet menü öğesi ayarlama

Tasnif sırasında paletleri oluşturmak için mobil cihaz menü öğesi oluşturun.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Palet oluşturma*
    - **Başlık:** *Palet oluşturma*
    - **Mod:** *Dolaylı*
    - **Varolan çalışmayı kullan:** *Hayır*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Faaliyet kodu:** *Giden tasnif*

        Bu alan *Giden tasnif* olarak ayarlandığında, **Giden tasnif şablonu kimliği** alanı görüntülenir.

    - **İşlem kılavuzu kullan:** *Evet*

        **Faaliyet kodu** alanı *Giden tasnif* olarak ayarlandığında, bu seçenek otomatik olarak *Evet*'e ayarlanır.

    - **Giden tasnif şablonu kodu:** *AutoWork*

1. **Kaydet**'i seçin.

#### <a name="set-up-a-new-loading-menu-item"></a>Yeni yükleme menü öğesi ayarlama

Daha sonra kullanıcıların tasnif edilen stok maddelerini sevkiyat yerleşimine taşımasına olanak tanıyan bir menü öğesi oluşturun.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Tasniften yükle*
    - **Başlık:** *Tasniften yükle*
    - **Mod:** *İş*
    - **Mevcut işi kullan:** *Evet*

1. **Genel** hızlı sekmesinde **Yöneten** alanı *Kullanıcı tarafından yönetilen* olarak ayarlanmalıdır.
1. **İş sınıfları** hızlı sekmesinde, **Yeni**'yi seçin ve sonra aşağıdaki değerleri ayarlayın:

    - **İş sınıfı kodu:** *TASNİF*
    - **İş emri türü:** *Tasnif edilmiş stok çekme*

1. **Kaydet**'i seçin.

### <a name="set-up-the-mobile-device-menu"></a>Mobil cihaz menüsünü ayarlama

Şimdi yeni menü öğelerini mobil cihaz menüsüne eklemelisiniz.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. **Giden** menüsünü seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Mevcut menüler ve menü öğeleri** sütununda **Palet oluşturma**'yı bulun ve seçin.
1. **Palet oluşturma**'yı **Menü yapısı** sütununa taşımak için sağ ok düğmesini seçin.
1. **Palet oluşturma** menü öğesini mobil cihaz menüsünde istenen konuma taşımak için yukarı ok ve aşağı ok düğmelerini kullanın.
1. **Kaydet**'i seçin.
1. **Tasniften yükleme** menü öğesini **Tasnif** menüsüne eklemek için bu prosedürü tekrarlayın.

### <a name="set-up-location-directives"></a>Yerleşim yönergelerini kur

*Yerleşim yönergeleri* stok hareketi için çekme ve indirme konumlarını belirlemeye yardımcı olan kurallardır. Tasnif işini yönetmek için şimdi bir kural oluşturmanız gerekir.

#### <a name="set-up-a-single-sku-directive"></a>Tek SKU yönergesi ayarlama

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Sol bölmede, **İş emri türü** alanının değerini *Tasnif edilen stoktan malzeme çekme* olarak ayarlayın.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Sıra:** *1*
    - **Ad:** *Baydoor*

1. **Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Yerine koyma*
    - **Tesis:** *6*
    - **Ambar:** *62*
    - **Birden çok SKU:** *Hayır*

1. Araç çubuğunu **Satırlar** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Satırlar** hızlı sekmesinde, **Yeni**'yi seçin ve sonra yeni satırda aşağıdaki değerleri ayarlayın: Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Sıra:** *1*
    - **Başlangıç:** *0*
    - **Bitiş:** *1.000.000*

1. Araç çubuğunu **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde, **Yeni**'yi seçin ve sonra yeni satırda aşağıdaki değerleri ayarlayın: Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Sıra:** *1*
    - **Ad:** *Baydoor*

1. **Kaydet**'i seçin.
1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle**'yi seçin.
1. Sorgu düzenleyicisinde, **Aralık** sekmesinde, **Alan** alanının *Yerleşim* olarak ayarlandığı satırı bulun. Bu satır için **Ölçüt** alanını *Baydoor* olarak ayarlayın.
1. Ayarlarınızı kaydedip sorgu düzenleyicisini kapatmak için **Tamam**'ı seçin.

#### <a name="set-up-a-multiple-sku-directive"></a>Birden çok SKU yönergesi ayarlama

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Sol bölmede, **İş emri türü** alanının değerini *Tasnif edilen stoktan malzeme çekme* olarak ayarlayın.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Sıra:** *2*
    - **Ad:** *Baydoor Multi*

1. **Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Yerine koyma*
    - **Tesis:** *6*
    - **Ambar:** *62*
    - **Birden çok SKU:** *Evet*

1. Araç çubuğunu **Satırlar** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Satırlar** hızlı sekmesinde, **Yeni**'yi seçin ve sonra yeni satırda aşağıdaki değerleri ayarlayın: Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Sıra:** *1*
    - **Başlangıç:** *0*
    - **Bitiş:** *1.000.000*

1. Araç çubuğunu **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde, **Yeni**'yi seçin ve sonra yeni satırda aşağıdaki değerleri ayarlayın: Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Sıra:** *1*
    - **Ad:** *Baydoor Multi*

1. **Kaydet**'i seçin.
1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle**'yi seçin.
1. Sorgu düzenleyicisinde, **Aralık** sekmesinde, **Alan** alanının *Yerleşim* olarak ayarlandığı satırı bulun. Bu satır için **Ölçüt** alanını *Baydoor* olarak ayarlayın.
1. Ayarlarınızı kaydedip sorgu düzenleyicisini kapatmak için **Tamam**'ı seçin.

### <a name="set-up-work-templates"></a>İş şablonlarını ayarla

1. **Ambar yönetimi \> Kurulum \> İş \> İş şablonları**'na gidin.
1. **İş emri türü** alanının değerini *Tasnif edilen stoktan malzeme çekme* olarak değiştirin.
1. Eylem bölmesinde, bir iş şablonu oluşturmak için **Yeni**'yi seçin.
1. **Genel bakış** sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Sıra:** *1*
    - **İş şablonu:** *Tasnif*
    - **İş şablonu açıklaması:** *Tasnif*

1. **İş Şablonu Ayrıntıları** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **İş Şablonu Ayrıntıları** hızlı sekmesinde, satır eklemek için **Yeni**'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Çekme*
    - **İş sınıfı kodu:** *TASNİF*

1. **Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Yerine koyma*
    - **İş sınıfı kodu:** *TASNİF*

1. **Kaydet**'i seçin.

## <a name="scenario"></a>Senaryo

Bu senaryo, sevkiyat taşıma hizmetine bağlı olarak, paketlenen konteynerlerin paket istasyonu ardından otomatik olarak farklı konumlara (paletlere) tasnif edilmesi gereken bir durumun benzetimini yapar. Yükten gelen tüm maddeler paketlendikten ve adrese göre tasnif edildikten sonra, paletler bölme kapısına taşınacaktır.

### <a name="create-sales-orders-and-picking-work"></a>Satış siparişi ve çekme işi oluşturma

#### <a name="create-sales-order-1"></a>Satış siparişi oluşturma 1

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-005*
    - **Ambar:** *62*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

    Yeni satış siparişi açılır.

1. **Üst bilgi** görünümüne geçin.
1. **Teslimat** hızlı sekmesinde, **Taşıma** bölümünde aşağıdaki değerleri ayarlayın:

    - **Sevkiyat taşıyıcısı:** *Hava nakliyesi*
    - **Taşıyıcı hizmeti:** *Hava*

1. **Satırlar** görünümüne geçin.
1. **Satış siparişi satırları** hızlı sekmesinde, kılavuza yeni bir satır otomatik olarak eklenmemişse **Satır ekle**'yi seçin seçerek ekleyin:
1. Yeni sipariş satırında aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *2*

1. Yeni sipariş satırı **Satış siparişi satırları** hızlı sekmesinde seçiliyken, kılavuzun üzerindeki **Stok** menüsünden **Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.
1. Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız. Dalga kodu ve sevkiyat kodu numaralarını not edin.

#### <a name="sales-order-2"></a>Satış siparişi 2

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-006*
    - **Ambar:** *62*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. Yeni satış siparişi açılır. **Satış siparişi satırları** hızlı sekmesi 'ndeki kılavuza yeni, boş bir satır dahil etmelidir. Bu sipariş satırında aşağıdaki değerleri ayarlayın:

    - **Madde:** *A0001*
    - **Miktar:** *1*

1. **Satır ayrıntıları** hızlı sekmesinde **Teslimat** sekmesinde, **Teslimat yöntemi** alanını *Flowe-STD* olarak ayarlayın.
1. **Satış siparişi satırları** hızlı sekmesinde, **Satır ekle**'yi seçin ve sonra ikinci sipariş satırında aşağıdaki değerleri ayarlayın:

    - **Madde:** *A0002*
    - **Miktar:** *1*

1. **Satır ayrıntıları** hızlı sekmesinde **Teslimat** sekmesinde, **Teslimat yöntemi** alanının değerini *Air C-Air* olarak değiştirin.
1. **Satış siparişi satırları** hızlı sekmesinde ilk sipariş satırını seçin. Ardından, kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. **Satış siparişi satırları** hızlı sekmesinde ikinci sipariş satırını seçin. Ardından, kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır**'ı seçin.
1. Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.
1. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.
1. Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız. Satış siparişi satırlarındaki her teslimat yöntemi için bir tane olmak üzere iki dalga kodu numarası ve iki sevkiyat kodu numarasının oluşturulmuş olduğuna dikkat edin.

#### <a name="get-the-work-ids-from-the-work-details"></a>İş ayrıntılardan iş kodlarını alma

1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. Sayfa, satış siparişlerinden oluşturulan iş kodlarını gösterir. Her bir dalga ve sevkiyatla ilgili iş kodunu bulmak için oluşturduğunuz satış siparişlerindeki dalga kodlarını ve sevkiyat kimliklerini kullanın. Bir sonraki adımda gereksinim duyacağınız tüm iş kodlarını not alın. İkinci satış siparişi için iki iş kodu oluşturulduğuna dikkat edin. Farklı konumlardan farklı maddeler çekildiğinde, ayrı iş kodları oluşturulur.

### <a name="pick-items-for-the-sales-orders"></a>Satış siparişleri için maddeleri çekme

Maddeleri paket istasyonuna taşımak için mobil cihaz kullanarak oluşturulan işi tamamlayın.

1. Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62*'de oturum açın.
1. Ana menüde **Giden**'i seçin.
1. **Giden** menüsünden **Satış Çekme**'yi seçin.
1. **Kod** alanına, satış siparişi 1 için oluşturulan iş kodunu girin.
1. **Tamam**'ı seçin.
1. **Satış siparişleri - Çekme** sayfasında, satış siparişi 1 için oluşturulmuş olan hedef bir LP girin. Çekme yerleşimi (*toplu-001*), madde (*A0001*) ve miktar (*2 adet*) gösterildiğine dikkat edin.
1. **Tamam**'ı seçin.
1. **Satış siparişleri: Yerine koyma** sayfası hakkındaki bilgileri inceleyin. **Yerleşim** alanı, çekilen maddelerin *Paket* yerleşimine gittiğini göstermelidir.
1. **Tamam**'ı seçin.

    **İş kodu/plaka kodu tara** sayfasında, satış sipariş i1'deki iş kodunun tamamlandığını belirten "İş Tamamlandı" iletisi alırsınız.

    Şimdi satış siparişi 2'yi çekeceksiniz.

1. **Kod** alanına, satış siparişi 2 için oluşturulan iş kodunu girin; burada satır 1'de *A0001* maddesi bulunur.
1. **Tamam**'ı seçin.
1. **Satış siparişleri - Çekme** sayfasında bir hedef LP girin. Çekme yerleşimi (*toplu-001*), madde (*A0001*) ve miktar (*1 adet*) gösterildiğine dikkat edin.
1. **Tamam**'ı seçin.
1. **Satış siparişleri: Yerine koyma** sayfası hakkındaki bilgileri inceleyin. **Yerleşim** alanı, çekilen maddelerin *Paket* yerleşimine gittiğini göstermelidir.
1. **Tamam**'ı seçin.

    **İş kodu/plaka kodu tara** sayfasında "İş Tamamlandı" iletisi alırsınız. Bu ileti, satış siparişi 2'nin satır 1'indeki iş kodunun tamamlandığını gösterir.

1. **Kod** alanına, satış siparişi 2 için oluşturulan iş kodunu girin; burada satır 2'de *A0002* maddesi bulunur.
1. **Tamam**'ı seçin.
1. **Satış siparişleri - Çekme** sayfasında bir hedef LP girin. Çekme yerleşimi (*toplu-002*), madde (*A0001*) ve miktar (*1 adet*) gösterildiğine dikkat edin.
1. **Tamam**'ı seçin.
1. **Satış siparişleri: Yerine koyma** sayfası hakkındaki bilgileri inceleyin. **Yerleşim** alanı, çekilen maddelerin *Paket* yerleşimine gittiğini göstermelidir.
1. **Tamam**'ı seçin.

    **İş kodu/plaka kodu tara** sayfasında "İş Tamamlandı" iletisi alırsınız. Bu ileti, satış siparişi 2'nin satır 2'indeki iş kodunun tamamlandığını gösterir.

### <a name="pack-sales-orders-into-containers"></a>Satış siparişlerini konteynerlerde paketleme

#### <a name="pack-sales-order-1-into-containers"></a>Satış siparişi 1'i konteynerlerde paketleme

1. **Ambar Yönetimi \> Paketleme ve Konteyner kullanımı \> Paket**'e gidin.

    **Paketleme istasyonu seç** iletişim kutusu görüntülenir. Varsayılan olarak, **Çalışan** alanı daha önce ayarladığınız çalışanın adı olarak ayarlanmalıdır.

1. Belirli bir paketleme yerleşiminde planlanan sevkiyatları ve konteynerleri görüntülemek ve bunlarla çalışmak için aşağıdaki değerleri ayarlayın:

    - **Tesis:** *6*
    - **Ambar:** *62*
    - **Yerleşim:** *Paket*
    - **Paketleme profili kodu:** *Tasnif*

1. İletişim kutusunu kapatmak için **Tamam**'ı seçin.
1. **Paket** sayfasında, **Plaka veya sevkiyat** alanına, satış siparişi 1 için hedef LP girin. Ardından alanın dışına gitmek için klavyenizden **Sekme** veya **Enter** tuşunu seçin.
1. Eylem Bölmesinde **Yeni konteyner**'i seçin.
1. Tüm varsayılan ayarları kabul edin ve **Tamam**'ı seçin. Konteyner kodunu not edin.
1. **Madde paketleme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Miktar:** *1*
    - **Tanımlayıcı:** Madde *A0001*

1. Eylem Bölmesinde **Konteyneri kapat**'ı seçin.
1. **Konteyneri kapat** iletişim kutusunda, sistemin **Brüt ağırlık** alanını güncelleştirmesi için **Sistem ağırlığını al**'ı seçin.
1. **Tamam**'ı seçin. Konteyner, *TASNİF* yerleşimine taşınır ve tasnif için hazırdır.
1. Satış siparişi 1 için LP'den ikinci maddeyi yeni bir konteynere eklemek üzere ikinci bir konteyner oluşturun.
1. Eylem Bölmesinde **Yeni konteyner**'i seçin.
1. Tüm varsayılan ayarları kabul edin ve **Tamam**'ı seçin. Konteyner kodunu not edin.
1. **Madde paketleme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Miktar:** *1*
    - **Tanımlayıcı:** Madde *A0001*

1. Eylem Bölmesinde **Konteyneri kapat**'ı seçin.
1. **Konteyneri kapat** iletişim kutusunda, sistemin **Brüt ağırlık** alanını güncelleştirmesi için **Sistem ağırlığını al**'ı seçin.
1. **Tamam**'ı seçin. Konteyner, *TASNİF* yerleşimine taşınır ve tasnif için hazırdır.

#### <a name="pack-sales-order-2-into-containers"></a>Satış siparişi 2'yi konteynerlerde paketleme

1. **Paket** sayfasında, **Plaka veya sevkiyat** alanına, satış siparişi 2'nin satır 1'i için hedef LP girin. Ardından alanın dışına gitmek için klavyenizden **Sekme** veya **Enter** tuşunu seçin.
1. Eylem Bölmesinde **Yeni konteyner**'i seçin.
1. Tüm varsayılan ayarları kabul edin ve **Tamam**'ı seçin. Konteyner kodunu not edin.
1. **Madde paketleme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Miktar:** *1*
    - **Tanımlayıcı:** Madde *A0001*

1. Eylem Bölmesinde **Konteyneri kapat**'ı seçin.
1. **Konteyneri kapat** iletişim kutusunda, sistemin **Brüt ağırlık** alanını güncelleştirmesi için **Sistem ağırlığını al**'ı seçin.
1. **Tamam**'ı seçin. Konteyner, *TASNİF* yerleşimine taşınır ve tasnif için hazırdır.
1. **Plaka veya sevkiyat** alanına, satış siparişi 2'nin satır 2'si için hedef LP girin. Ardından alanın dışına gitmek için klavyenizden **Sekme** veya **Enter** tuşunu seçin.
1. Eylem Bölmesinde **Yeni konteyner**'i seçin.
1. Tüm varsayılan ayarları kabul edin ve **Tamam**'ı seçin. Konteyner kodunu not edin.
1. **Madde paketleme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Miktar:** *1*
    - **Tanımlayıcı alanı:** Madde *A0002*

1. Eylem Bölmesinde **Konteyneri kapat**'ı seçin.
1. **Konteyneri kapat** iletişim kutusunda, sistemin **Brüt ağırlık** alanını güncelleştirmesi için **Sistem ağırlığını al**'ı seçin.
1. **Tamam**'ı seçin. Konteyner, *TASNİF* yerleşimine taşınır ve tasnif için hazırdır.

Konteyner ayrıntılarını görüntülemek için **Ambar yönetimi \> Paketleme ve konteyner kullanımı \> Konteynerler**'e gidin ve paketleme sırasında oluşturulan konteyner kodlarını arayın.

### <a name="sort-the-containers"></a>Konteynerleri tasnif etme

> [!IMPORTANT]
> Giden tasnifi yapmak için mobil uygulamada **Palet derleme** menü öğesine eriştiğinizde, **Tam** olarak etiketlenmiş bir düğme görürsünüz. *Konumu tasnif etmek veya kapatmak için **Tam** düğmesini kullanmayın.*
>
> **Tam** düğmesi varsayılan olarak sağlanır ve devre dışı bırakılamaz veya sayfadan kaldırılamaz. *Giden tasnif* özelliği için kullanılmaz.

#### <a name="sort-the-first-container"></a>İlk konteyneri tasnif etme

1. Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62*'de oturum açın.
1. Ana menüde **Giden**'i seçin.
1. **Giden** menüsünden **Palet derleme**'yi seçin.
1. **LP/Kon** alanına, satış siparişi 1 ile ilişkilendirilen ilk konteyner kodunu girin.
1. **Tamam**'ı seçin.
1. Şu anda tasnif konumu bulunmadığından, bir tane belirtmeniz gerekir. **Tasnif konumu kodu** alanına *SP01* girin.
1. Şu anda *SP01* sıralama konumuyla ilişkilendirilmiş bir LP olmadığından, bir tane belirtmeniz gerekir. **LP** alanına *PLP01* girin.
1. **Tamam**'ı seçin.
1. Tasnif konumu doğrulaması açık olduğundan, tasnif konumu kodunu yeniden girmeniz gerekir. **Tasnif Konumu kodu** alanına *SP01* girin.
1. **Tamam**'ı seçin.

    Bir "İş tamamlandı" iletisi alırsınız.

> [!TIP]
> Tasnif konumunu ve içindeki LP'yi görüntülemek için **Ambar yönetimi \> Paketleme ve konteyner kullanımı \> Giden tasnif konumu atamaları**'na gidin.
>
> **Giden tasnif konumu atamaları** sayfası, etkin olan tüm tasnif konumlarını gösterir. **Tasnif konumu hareketleri** alanı, her tasnif konumuyla ilişkilendirilmiş LP'yi ve tasnif konumundaki konteynerleri gösterir. Bir tasnif konumunun var olduğuna ve **Tasnif konumu ölçütleri** hızlı sekmesinin **Sevkiyat – Taşıyıcı hizmeti - Hava** ölçütünü gösterdiğine dikkat edin.

#### <a name="sort-the-remaining-containers"></a>Kalan konteynerleri tasnif etme

1. Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62*'de oturum açın.
1. Ana menüde **Giden**'i seçin.
1. **Giden** menüsünden **Palet derleme**'yi seçin.
1. **LP/Kon** alanına, satış siparişi 1 ile ilişkilendirilen ikinci konteyner kodunu girin.
1. **Tamam**'ı seçin. Tasnif şablonu otomatik olarak tasnif edecek şekilde ayarlandığından ve eşleşen ölçütleri olan bir tasnif konumu zaten var olduğundan, otomatik olarak doğru tasnif konumuna yönlendirilirsiniz.
1. **Tamam**'ı seçin.
1. Stoğun doğru yerde olduğunu belirtmek için tasnif konumu kodunu onaylayın. **Tasnif Konumu kodu** alanına *SP01* girin.
1. **Tamam**'ı seçin.

    İş satış siparişi 1'deki ikinci konteynerden tamamlanır. Şimdi, satış siparişi 2'deki kalan konteynerleri tasnif etmeniz gerekir.

1. **LP/Kon** alanına, *A0001* maddesini içeren satış siparişi 2'deki konteynerin konteyner kodunu girin. Taşıyıcı hizmeti farklı olduğundan, yeni bir tasnif konumu girmeniz ve o konuma bir LP atamanız istenir. Tasnif konumu *SP02*'yi ve LP *PLP02*'yi kullanın.
1. **Tamam**'ı seçin.
1. *Tasnif konumu kodu* alanına **SP02** girerek tasnif konumunu onaylayın.
1. **Tamam**'ı seçin.

    İş konteynerde tamamlanır.

1. **LP/Kon** alanına, *A0002* maddesini içeren satış siparişi 2'deki kalan konteynerin konteyner kodunu girin. Taşıyıcı hizmeti satış siparişi 1'in taşıyıcı hizmetiyle aynı olduğundan sistem eşleşen ölçütlere sahip mevcut tasnif konumunu gösterir.
1. **Tamam**'ı seçin.
1. *Tasnif konumu kodu* alanına **SP01** girerek tasnif konumunu onaylayın.
1. **Tamam**'ı seçin.

    İş konteynerde tamamlanır.

### <a name="close-the-outbound-sorting-positions"></a>Giden tasnif konumlarını kapatma

Tüm stoklar tasnif edildiğinde, işin oluşturulabilmesi için konumun kapatılması gerekir. Tasnif edilen stok çekme işi, stoğu bölme kapısına almak amacıyla oluşturulacaktır.

#### <a name="close-a-position-from-the-mobile-device"></a>Konumu mobil cihazdan kapatma

1. Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62*'de oturum açın.
1. Ana menüde **Giden**'i seçin.
1. **Giden** menüsünden **Palet derleme**'yi seçin.
1. **LP/Kon** alanına, *SP01* tasnif konumuna tasnif edilmiş olan bir konteyner kodu girin.
1. **Tamam**'ı seçin.
1. Aşağıdaki iletiyi alırsınız: "Konteyner zaten SP01 konumuna tasnif edilmiş. Konum kapatılsın mı?" **Kapat**'ı seçin.

    İş tamamlanır.

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a>Giden tasnif konumu atamalarından konum kapatma

1. **Ambar yönetimi \> Paketleme ve konteyner kullanımı \> Giden tasnif konumu atamaları**'na gidin.
1. Sol sütunda **SP02 seçin**. Bu giden tasnif konumu satırı kapatacağınız konum satırıdır.
1. Eylem Bölmesinde **Konumu kapat**'ı seçin. Tasnif konumu kaydı kapatılır ve artık gösterilmez.

    > [!TIP]
    > Tüm kapalı konum kayıtlarını göstermek için, **Kapalı olanı göster** onay kutusunu seçin.

### <a name="sorted-inventory-picking"></a>Tasnif edilmiş stok çekme

Tasnif edilen stok çekme işini tamamlamanız gerekir. Tamamlandığında, stok satış siparişine çekilir. Bu noktada, diğer tüm ambar süreçleri geçerlidir.

1. Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62*'de oturum açın.
1. Ana menüde **Giden**'i seçin.
1. **Giden** menüsünde, **Tasniften yükle**'yi seçin.
1. İlk tasnif konumu olan *SP01*'den hedef LP kodunu girin. **Kod** alanını *PLP01* olarak ayarlayın.
1. **Tamam**'ı seçin.
1. **Tasnif edilen stok çekme: Çekme** sayfası gerçekleştirilmesi gereken çekme işini gösterir. Birden fazla madde içeren ve *3* miktarına sahip olan *TASNİF* yerleşiminden ve hedef plaka *PLP01*'den çekin.
1. **Tamam**'ı seçin.
1. **Tasnif edilen stok çekme: Yerine koyma** sayfası gerçekleştirilmesi gereken yerine koyma işini gösterir. Birden fazla madde içeren ve *3* miktarına sahip olan *Bölme kapısı* yerleşimine ve hedef plaka *PLP01*'e koyun.
1. **Tamam**'ı seçin.

    İş tamamlanır.

1. İkinci tasnif konumu olan *SP02*'den hedef plaka kodunu girin. **Kod** alanını *PLP02* olarak ayarlayın.
1. **Tamam**'ı seçin.
1. **Tasnif edilen stok çekme: Çekme** sayfası gerçekleştirilmesi gereken çekme işini gösterir. Birden fazla madde içeren ve *1* miktarına sahip olan *TASNİF* yerleşiminden ve hedef plaka *PLP02*'den çekin.
1. **Tamam**'ı seçin.
1. **Tasnif edilen stok çekme: Yerine koyma** sayfası gerçekleştirilmesi gereken yerine koyma işini gösterir. Birden fazla madde içeren ve *1* miktarına sahip olan *Bölme kapısı* yerleşimine ve hedef plaka *PLP02*'e koyun.
1. **Tamam**'ı seçin.

    İş tamamlanır.

Bu noktadan itibaren, diğer tüm ambar süreçleri geçerlidir.
