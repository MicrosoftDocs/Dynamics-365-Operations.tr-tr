---
title: Ambar yerleşimi durumu
description: Bu makale Ambar konumu durumu özelliğine genel bakış sunmaktadır.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 6d04ca43895935329b711f2658360c41f611975e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065479"
---
# <a name="warehouse-location-status"></a>Ambar yerleşimi durumu

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management'ta, yerleşimler üzerinde çalışırken ve işlemler yaparken esneklik sağlayacak çeşitli yerleşim konumları içerir. Ambar akışı üzerinde daha iyi kontrol sağlamak için yerleşim yönergesi sorgusuna yerleşim durumları ekleyebilirsiniz.

**Yerleşimler** sayfasında aşağıdaki dört alan, bir yerleşimin geçerli durumuyla ilgili bilgileri izler. Bu alanlar ambar yöneticilerinin ambar yerleşimlerinin durumu hakkında genel bir fikir edinmesini sağlar. Ayrıca, gelişmiş raporlama ve filtreleme işlemlerine de izin verir.

- **Madde numarası** – Yerleşimdeki mevcut madde. Yerleşimde birden çok madde varsa bu alan boştur.
- **Son faaliyet tarih ve saati** – Yerleşime göre gerçekleştirilen son ambar hareketinin zaman damgası.
- **Yaşlandırma tarihi** – Yerleşimdeki stokun ambara alındığı tarih. Bu değer, plakanın yaşlandırma tarihi temel alınarak hesaplanır. Bu, plaka izlemeli yerleşimler için doğrudur ancak plaka izlenmeyen yerleşimler için doğru olmayabilir.
- **Yerleşim durumu** – Yerleşimin durumu. Dört olası değer vardır:

    - **Belirlenmemiş** – Yerleşim profili durumu izleyemez. Bu nedenle, geçerli durum bilinmiyor demektir.
    - **Boş** – Şu anda yerleşimde stok yok.
    - **Malzeme çekme** – Son boş olduğu zamandan sonra yerleşime karşı giden hareketler gerçekleştirilmiştir.
    - **Depolama** – Son boş olduğu zamandan sonra yerleşime karşı gelen hareketler gerçekleştirilmiştir.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Ambar konum durumu özelliğini açma

*Ambar konum durumu* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Ambar konum durumu*

## <a name="set-up-warehouse-location-status"></a>Ambar konumu durumunu ayarlama

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Örnek senaryo için gereken örnek verileri hazırlama

Senaryo üzerinden çalışmaya başlamadan önce, örnek verileri etkinleştirmeniz ve özelliği bu bölümde açıklandığı şekilde ayarlamanız gerekir. Örnek senaryoyu tamamlamak için, Ambar Yönetimi mobil uygulamasını veya tarayıcı tabanlı öykünücüyü kullanmalısınız. Burada belirtilen adımlar Ambar Yönetimi mobil uygulamasını kullanır. Tarayıcı tabanlı öykünücüye ilişkin adımlar benzerdir.

#### <a name="use-the-usmf-legal-entity"></a>Tüzel kişilik olarak USMF'yi kullanın

Burada belirtilen örnek kayıtları ve değerleri kullanarak örnek senaryo üzerinden çalışmak için, standart [tanıtım verilerinin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) yüklenmiş olduğu bir sistemde olmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

#### <a name="set-up-location-profiles"></a>Yerleşim profillerini ayarla

Örnek senaryo için iki yerleşim profili hazırlamanız gerekir.

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.
1. Sayfayı düzenleme moduna sokmak için **Düzenle**'yi seçin.
1. **TOPLU-06** profilini seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Maddeyi yerleşimde etkinleştir:** Bu seçeneği _Evet_ olarak ayarlayın.
    - **Yerleşim faaliyeti tarih ve saatini etkinleştir:** Bu seçeneği _Evet_ olarak ayarlayın.
    - **Yerleşim durumunu etkinleştir:** Bu seçeneği _Evet_ olarak ayarlayın.

    Bu seçenekler, yerleşimdeki başvuru alanlarının etkin olup olmadığını denetler.

1. **PCK-06** profili için 3. ve 4. adımları yineleyin.

> [!NOTE]
> Konum profilindeki parametreler (**Konumda maddeyi etkinleştir**, **Konum etkinliğini etkinleştir**, **Konum durumunu etkinleştir**) *Evet* olarak ayarlandığında, sistem hemen ilgili konumları, *Ambar yerleşimi durumu tutarlılık denetimi* işi yürüterek hemen güncelleştirir.

### <a name="scenario"></a>Senaryo

1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Satınalma siparişi oluştur** iletişim kutusunda, **Satıcı** hızlı sekmesinde, **Satıcı hesabı** alanında *104*'ü seçin.
1. **Genel** hızlı sekmesinde, **ambar** alanında, *61*'i seçin.
1. **Tamam**'ı seçin.
1. Yeni satınalma siparişiniz (PO) açılır. **Satınalma siparişi satırları** kılavuzunda boş bir satırı bulunur. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** _A0002_
    - **Miktar:** _5_

1. Eylem bölmesinde, **Satınalma** sekmesinde, **Eylemler** grubunda, satınalma siparişini onaylamak için **Onayla**'yı seçin.
1. Mobil cihazda **Gelen \> Satınalma Teslim Alma**'ya gidin.
1. **PONUM** alanını seçin ve satınalma siparişi numarasını girip onaylayın.
1. **ÖĞE** alanını seçin, madde numarası olarak *A0002* girin ve onaylayın.
1. **MKT** sayfasında miktarı *5* olarak girin ve onaylayın.

    Miktarı aşağıdaki yöntemlerden biriyle girebilirsiniz:

    - Sayısal değer eklemek veya çıkarmak için artı işareti (**+**) veya eksi işareti (**–**) düğmesini seçin.
    - Sayısal tuş takımını açmak için artı işareti (**+**) ve eksi işareti (**–**) düğmeleri arasındaki boş alanı seçin.

1. Madde numarası olarak *A0002* ve miktar olarak *5* seçiminizi onaylayın. Sayfanın alt kısmında bir "İş Tamamlandı" iletisi görüntülenir.
1. Sağ üst köşedeki menü düğmesini (bazen hamburger veya hamburger düğmesi olarak da adlandırılır) seçin ve ardından **Satınalma Teslim Alma**'dan çıkmak ve **Gelen** menüsüne dönmek için **İptal**'i seçin.
1. Satınalma siparişi sayfasında, **Satınalma siparişi satırları** kılavuzunun üzerindeki **İş ayrıntıları**'nı seçin.
1. **Genel** sekmesinde, oluşturulan **İş kodu** ve **Hedef plaka kodu** değerlerine dikkat edin.
1. **Satırlar** bölümünde, *Çekme* ve *Koyma* iş türleri için **Yerleşim** değerlerine dikkat edin.
1. Mobil cihazda **Gelen \> Satınalma Yerine Koyma**'ya gidin.
1. **ID** alanını seçin ve iş kodunu girip onaylayın.
1. *Çekme* girişini tamamlamak için bir kez daha onaylayın.
1. Sağ üst köşedeki Menü düğmesini ve ardından **Bitti**'yi seçerek *Çekme* işini tamamlayın.
1. Yerine koyma yerleşimini not edin ve onaylayın. Sayfanın alt kısmında bir "İş Tamamlandı" iletisi görüntülenir.
1. Sağ üst köşedeki Menü düğmesini seçin ve ardından **İptal**'i seçerek **Satınalma Yerine Koyma**'dan çıkıp **Gelen** menüsüne dönün.
1. Ana menüye dönmek için **Geri**'yi seçin.
1. Dynamics 365 Supply Chain Management'ta **Ambar yönetimi \> Kurulum \> Ambar \> Yerleşimler**'e gidin.
1. **Yerleşim**'e filtre uygulayın ve satınalma siparişi işinden aldığınız yerine koyma yerleşimini girin. Aşağıdaki sonuçları görmeniz gerekir:

    - **Yerleşim durumu** sütunu bir *Depolama* değeri gösterir çünkü bu yerleşime karşılık gelen son hareket bir koyma işlemidir.
    - **Madde numarası** sütunu *A0002* değerini gösterir çünkü bu madde teslim alınıp yerleşime koyulmuştur.
    - **Son faaliyet tarih ve saati** sütunu, işin yerleşimde tamamlandığı tarih ve saatin zaman damgasını gösterir.

1. Mobil cihazda **Kalite \> Hareket**'e gidin.
1. **LOC/LP** alanını seçin ve önceki adımlarda not ettiğiniz yerleşimi girin.
1. Gösterilen bilgileri onaylayın. Oluşturulan plaka numarasını not edin.
1. **Hedef Bilgileri** ekranında, **LOC/LP** alanını seçin ve maddenin taşınacağı yerleşim olarak *06A07R2S1B* girin.
1. **Hedef Bilgileri** ekranında, otomatik olarak oluşturulan **LP** değerini (hedef plaka kodu) onaylayın. Sayfanın alt kısmında bir "İş Tamamlandı" iletisi görüntülenir.
1. Sağ üst köşedeki Menü düğmesini seçin ve ardından **İptal**'i seçerek **Hareket**'ten çıkıp **Kalite Yönetimi** menüsüne dönün.
1. Ana menüye dönmek için **Geri**'yi seçin.
1. Dynamics 365 Supply Chain Management'ta **Ambar yönetimi \> Kurulum \> Ambar \> Yerleşimler**'e gidin.
1. **Yerleşimler** sayfasını yenileyin ve ilk yerine koyma yerleşimini yeniden görüntüleyin. **Yerleşim durumu** alanının şimdi *Boş* olarak ayarlandığına ve **Madde numarası** sütununun boş olduğuna dikkat edin.
1. *06A07R2S1B* kodlu yerleşimin kaydını görüntüleyin ve **Durum** değerinin *Depolama* olarak değiştiğine ve **Madde numarası** ile **Son faaliyet tarih ve saati** alanlarının güncelleştirildiğine dikkat edin.
1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusundaki **Müşteri hesabı** alanında *ABD-002*'yi seçin.
1. **Ambar** alanında *61*'i seçin.
1. **Tamam**'ı seçin.
1. Yeni satış siparişiniz açılır. **Satış siparişi satırları** kılavuzunda boş bir satırı bulunur. Bu satır için aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** _A0002_
    - **Miktar:** _1_

1. **Satış siparişi satırları** hızlı sekmesinde **Stok** menüsünde **Rezervasyon**'u seçin.
1. **Rezervasyon** sayfasında sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin. Bunun ardından sağ üst köşedeki **Kapat** düğmesini (**X**) seçerek sayfayı kapatın.
1. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.
1. **Satış siparişi satırları** bölümünde **Ambar** menüsünde **İş ayrıntıları**'nı seçin.
1. Oluşturulan **İş kodu** değerini kopyalayın.
1. Mobil cihazda **Giden \> Satış için malzeme çekme**'ye gidin.
1. **ID** alanını seçin ve daha önce kopyaladığınız iş kodunu girip onaylayın.
1. **Satış siparişleri: Malzeme çekme** sayfasında, **LOC** alanı daha önce oluşturulan yerine koyma yerleşimi olarak malzeme çekme yerleşimini önerir. Yerleşimi not edin.
1. **LOC** alanını seçin ve yerleşimi girip onaylayın.
1. **LP** alanını seçin, Hareket faaliyeti sırasında not aldığınız plaka numarasını girin ve onaylayın.
1. **Öğe** alanını seçin, madde numarası olarak *A0002* girin ve onaylayın.
1. **MKT** sayfasında miktarı *1* olarak girin ve onaylayın.

    Miktarı aşağıdaki yöntemlerden biriyle girebilirsiniz:

    - Sayısal değer eklemek veya çıkarmak için artı işareti (**+**) veya eksi işareti (**–**) düğmesini seçin.
    - Sayısal tuş takımını açmak için artı işareti (**+**) ve eksi işareti (**–**) düğmeleri arasındaki boş alanı seçin.

1. **HEDEF LP** alanını seçin, kullanıcı tanımlı bir hedef plaka kodu girin ve onaylayın.
1. Malzeme çekme işini tamamlamak için bir kez daha onaylayın. Sayfanın alt kısmında bir "İş Tamamlandı" iletisi görüntülenir.
1. Sağ üst köşedeki Menü düğmesini seçin ve ardından **İptal**'i seçerek malzeme çekme faaliyetini tamamlayıp **Giden** menüsüne dönün.
1. Dynamics 365 Supply Chain Management'ta **Ambar yönetimi \> Kurulum \> Ambar \> Yerleşimler**'e gidin.
1. **Yerleşim**'e filtre uygulayın ve satış siparişi işinden aldığınız malzeme çekme yerleşimini girin.
1. Satış siparişinin çekildiği yerleşim için **Yerleşim durumu** alanının şimdi *Malzeme çekme* olarak ayarlandığına ve **Son faaliyet tarih ve saati** alanının güncelleştirildiğine dikkat edin.

> [!NOTE]
> Yerleşim alanları yalnızca ambar hareketleriyle güncelleştirilir. Günlük veya diğer WMS dışı işlemleri kullanarak stok taşırsanız, alanlar güncelleştirilmez.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]