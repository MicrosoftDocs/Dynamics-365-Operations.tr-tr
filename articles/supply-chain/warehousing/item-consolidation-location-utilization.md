---
title: Madde konsolidasyonu - yerleşim kullanımı
description: Bu konu, ambar yöneticilerinin ambar içindeki yerleşimlerin hacimsel kullanımını görüntülemesini ve filtrelemesini kolaylaştıran işlev hakkında bilgi sağlar. Yöneticiler yerleşimleri seçip maddeleri konsolide etmek ve böylece ambar alanını daha iyi kullanabilmek için Madde Konsolidasyonu sayfasından doğrudan stok hareketi işi oluşturabilirler.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3b20b41d27e5faeac7ea88940c086ae33390dc29
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217017"
---
# <a name="item-consolidation---location-utilization"></a>Madde konsolidasyonu - yerleşim kullanımı

[!include [banner](../includes/banner.md)]

Bu konu, ambar yöneticilerinin ambar içindeki yerleşimlerin hacimsel kullanımını görüntülemesini ve filtrelemesini kolaylaştıran işlev hakkında bilgi sağlar. Yöneticiler yerleşimleri seçip maddeleri konsolide etmek ve böylece ambar alanını daha iyi kullanabilmek için **Madde Konsolidasyonu** sayfasından doğrudan stok hareketi işi oluşturabilirler.

## <a name="turn-on-the-features"></a>Özellikleri etkinleştirme

Bu konuda açıklanan özellikleri kullanabilmeniz için, önce bunları sisteminizde açmanız gerekir. Yöneticiler bu özelliklerin durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Aşağıdaki özelliklerin her ikisini de listelendikleri sırayla açın. (Her iki özellik de **Ambar Yönetimi** modülünde yer alır.)

1. Ambar yerleşimi durumu
2. Madde konsolidasyon yerleşimi kullanımı

## <a name="warehouse-location-status"></a>Ambar yerleşimi durumu

*Ambar yerleşimi durumu* özelliği, **Yerleşimler** sayfasına yerleşimin geçerli durumuyla ilgili ek bilgileri izlemek için dört yeni alan ekler:

- **Madde numarası** – Yerleşimdeki mevcut madde. Yerleşimde birden çok madde varsa bu alan boş olacaktır.
- **Son faaliyet tarih ve saati** – Yerleşime göre gerçekleştirilen son ambar hareketinin zaman damgası.
- **Yaşlandırma tarihi** – Yerleşimdeki stokun ambara alındığı tarih. Bu tarih, yaşlandırma tarihi temel alınarak hesaplanır. Bu tarih, plaka izlemeli yerleşimler için doğru olsa da ancak plaka izlenmeyen yerleşimler için doğru olmayabilir.
- **Yerleşim durumu** – Yerleşimin durumu. Kullanılabilir dört değer bulunur:

    - **Belirlenmemiş** – Yerleşim profili durumu izlemez. Bu nedenle, geçerli durum bilinmiyor demektir.
    - **Boş** – Şu anda yerleşimde stok yok.
    - **Malzeme çekme** – Son boş olduğu zamandan sonra yerleşime karşı giden hareketler gerçekleştirilmiştir.
    - **Depolama** – Son boş olduğu zamandan sonra gelen hareketler gerçekleştirilmiştir.

Bu alanlar ambar yöneticilerinin ambar yerleşimlerinin durumu hakkında daha iyi genel fikir edinmesini sağlar. Ayrıca, daha gelişmiş raporlama ve filtreleme işlemlerine de izin verir.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Madde konsolidasyonu ve yerleşim kullanımını ayarlama

Bu bölümde, sistemin madde konsolidasyonu ve yerleşim kullanımını kullanmak için nasıl hazırlanacağı açıklanmaktadır. Bu yordamlar, standart demo verilerinden örnek değerleri kullanır. Bu konunun ilerleyen kısımlarında sağlanan örnek senaryo aracılığıyla çalışmayı planlıyorsanız, **USMF** tüzel kişiliğini (standart demo verilerini içeren) seçin ve bu bölümde açıklanan her kaydı oluşturun. Örnek senaryo aracılığıyla çalışmayı planlamıyorsanız, burada sağlanan değerler, özellikleri kullanmak için tamamlamanız gereken kurulum türleriyle ilgili örnekler olarak kabul edilebilir.

### <a name="released-product"></a>Serbest bırakılan ürün

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. **Madde numarası** alanında, *M9201* seçeneğini belirleyin ve ayrıntılar sayfasını açın.
1. Eylem Bölmesinde, **Stoğu yönet** sekmesindeki **Ambar** grubunda, **Fiziksel boyutlar**'ı seçin.
1. **Fiziksel boyut** sayfasında, eylem bölmesinde, **Yeni**'yi seçin.

    Kılavuza yeni bir satır eklenir. **Madde numarası** alanı önceden ayarlanmıştır.

1. **Birim** alanında *ea*'yı seçin. Satırdaki kalan alanlar otomatik olarak ayarlanır.
1. **Kaydet**'i seçip sayfayı kapatın.

### <a name="location-profile"></a>Yerleşim profili

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.
1. Yerleşim profilleri listesinde **FLOOR-05**'i seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki seçeneklerin her ikisinin de *Evet* olarak ayarlandığından emin olun:

    - Maddeyi yerleşimde etkinleştir
    - Yerleşim durumunu etkinleştir

1. **Kaydet**'i seçin.

    > [!IMPORTANT]
    > **Yerleşimde madde etkinleştir** ve **Yerleşim durumunu etkinleştir** seçenekleri zaten *Evet* olarak ayarlandıysa , 10. adımda **Boyutlar** hızlı sekmesini ayarlama yönergelerine atlayın. Seçenekler önceden *Evet* olarak ayarlanmamışsa , bunları el ile ayarladıktan sonra **Ambar yönetimi** modülü için bir tutarlılık denetimi çalıştırmanız gerekir. Bu durumda, sonraki adımla devam edin.

1. Tutarlılık denetimini çalıştırmak için, **Sistem yönetimi \> Periyodik görevler \> Veritabanı \> Tutarlılık denetimi** bölümüne gidin.
1. **Tutarlılık denetimi** iletişim kutusunda aşağıdaki değerleri ayarlayın.

    - **Modül:** *Ambar yönetimi*
    - **Denetle/Onar:** *Denetle*
    - **Başlangıç tarihi:** Bu alanı boş bırakın.
    - **Ambar yerleşim durumu tutarlılık denetimi:** Bu onay kutusunu seçin.

1. **Tamam**'ı seçin.

    > [!TIP]
    > Tutarlılık denetimi tamamlandığında bir bildirim alırsınız. İletiyi görüntülemek için [İşlem Merkezi](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications)'ni açın. Ayrıntıları görüntülemek için **İleti ayrıntıları**'nı seçin.
    >
    > Tutarlılık denetimi iletisinde "Ambar XX'deki XXXX yerleşimi için yanlış yerleşim durumu bilgileri bulundu" ifadesi varsa tutarlılık denetimini tekrar çalıştırmalısınız. Bu kez, **Denetle/Onar** alanını *Hatayı düzelt* olarak ayarlayın. Herhangi bir hata bulunmadığından emin olmak için iletileri görüntüleyin.

1. Şimdi yerleşim profili kurulumunu tamamlamanız gerekir. **Ambar Yönetimi \> Kurulum \> Ambar \> Yerleşim profilleri**'ne dönün, yerleşim profili **FLOOR-05**'i seçin ve eylem bölmesinde **Düzenle**'yi seçin.
1. **Boyutlar** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Hacim kullanım yüzdesi:** *100*
    - **Stok yerleşimi için kullanılan hacimsel yöntem:** *Yerleşim hacmi kullan*
    - **Gerçek yerleşim yüksekliği:** *10*
    - **Gerçek yerleşim genişliği:** *10*
    - **Gerçek yerleşim derinliği:** *10*
    - **Maksimum ağırlık:** *100*

1. **Kaydet**'i seçin.

### <a name="mobile-device-menu-items"></a>Mobil cihaz menü öğeleri

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem bölmesinde, sıralama amacıyla kullanılacak menü öğesini oluşturmak için **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Ayarla*
    - **Başlık:** *Ayarla*
    - **Mod:** *İş*
    - **Varolan çalışmayı kullan:** *Hayır*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **İş oluşturma işlemi:** *Ayarlama*
    - **Stok ayarlama türleri:** *Ayarlama*

1. **Kaydet**'i seçin.

### <a name="mobile-device-menu"></a>Mobil cihaz menüsü

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. Menüler listesinde **Stok** öğesini seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Mevcut menüler ve menü öğeleri** listesinde, **Ayarla** menüsü öğesini bulun ve seçin.
1. **Ayarla**'yı **Menü Yapısı** listesine taşımak için sağ ok düğmesini seçin. Böylece, yeni menü öğesini seçili menüye eklersiniz.
1. **Kaydet**'i seçin.

### <a name="movement-types"></a>Hareket türleri

1. **Ambar yönetimi \> Kurulum \> Stok \> Hareket türleri** öğesine gidin.
1. Eylem bölmesinde **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:

    - **Hareket türü kodu:** *KONSOLİDE ETME*
    - **Açıklama:** *Yerleşimleri konsolide et*
    - **İş sınıfı kodu:** *InvMov*

1. **Kaydet**'i seçin.

## <a name="example-scenario"></a>Örnek senaryo

Aşağıdaki senaryo, ambarda iki yerleşimde stok *ayarlaması* yapmak için mobil cihazda ambar uygulamasını kullanır.

### <a name="add-inventory-to-locations"></a>Yerleşimlere stok ekleme

1. Ambar *51* için ayarlanmış olan bir kullanıcı olarak mobil cihazda oturum açın.
1. **Stok \> Ayarla**'ya gidin.

    Şimdi ilk yerleşim ayarlamasını gireceksiniz.

1. **Ayarlama** görevinde stok ayarlamasının yapılacağı yerleşimi seçin. **YERLEŞİM** alanında, *Lp-001*'i seçin.
1. Yerleşimi onaylayın.
1. Yerleşime eklenecek madde için bir plaka kodu oluşturun. **LP** alanına *LP00101* girin.
1. Plakayı onaylayın.
1. Plakaya eklenecek maddeyi girin. **ITEM** alanına *M9201* girin.
1. Maddeyi onaylayın.
1. Eklenecek madde miktarını girin. **MİKTAR** alanına, *10* girin.
1. Onaylanan miktar.

    Bir "İş Tamamlandı" iletisi alırsınız. Şimdi ikinci yerleşim ayarlamasını gireceksiniz.

1. **Ayarlama** görevinde stok ayarlamasının yapılacağı yerleşimi seçin. **YERLEŞİM** alanında, *Lp-002*'yi seçin.
1. Yerleşimi onaylayın.
1. Yerleşime eklenecek madde için bir plaka kodu oluşturun. **LP** alanına *LP00201* girin.
1. Plakayı onaylayın.
1. Plakaya eklenecek maddeyi girin. **ITEM** alanına *M9201* girin.
1. Maddeyi onaylayın.
1. Eklenecek madde miktarını girin. **MİKTAR** alanına, *15* girin.
1. Miktarı onaylayın.

    Bir "İş Tamamlandı" iletisi alırsınız.

1. Menü düğmesini seçin (bazen hamburger veya hamburger düğmesi olarak da adlandırılır) ve **Ayarlama** görevinden çıkmak için **İptal**'i seçin.

### <a name="consolidate-locations"></a>Yerleşimleri konsolide etme

1. **Ambar Yönetimi \> Periyodik görevler \> Madde konsolidasyonu**'na gidin.
1. Başlıkta, konsolidasyon yapılacak bir ambar seçin. **Ambar** alanına *51* girin.

    Madde *M9201*'in ayarlandığı her yerleşim için bir kayıt gösterilir. **Kullanım yüzdesi** sütunu her yerleşimin hacimsel kullanımını gösterir.

1. Stok konsolide etmek için, konsolide edilmesi gereken tüm yerleşimleri seçin ve sonra Eylem Bölmesinde **Stoğu konsolide et**'i seçin.
1. **Stoğu konsolide et** iletişim kutusunda, stok hareketi için iş oluşturmak üzere kullanılması gereken konumu ve hareket türünü belirtin. Aşağıdaki değerleri ayarlayın:

    - **Yerleşim:** *LP-001*
    - **Hareket türü kodu:** *KONSOLİDE ETME*

1. **Tamam**'ı seçin.
1. Ouşturulan hareket işini gösteren bir bilgi iletisi alırsınız. Hareket işi kodunu not edin.

### <a name="view-movement-work"></a>Hareket işini görüntüleme

1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. Oluşturulan işi görüntüleyin. İş kılavuzuna filtre uygulamak veya arama yapmak için stok konsolidasyonundan hareket işi kodunu kullanın.

    Bu senaryoda, stok konsolidasyon yerleşimi olarak stok içeren mevcut bir yerleşim kullanılmıştır. Bu nedenle, yalnızca bir iş kodu oluşturuldu.

    > [!NOTE]
   > Sistem, tamamlanması gereken her bir hareket için bir iş kodu oluşturur. Önceden stok içeren bir yerleşim belirlerseniz, yalnızca bir iş kodu oluşturulur. Yeni bir yerleşim belirtirseniz, iki iş kodu oluşturulur.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]