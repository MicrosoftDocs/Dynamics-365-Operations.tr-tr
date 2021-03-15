---
title: Duvara yerleştirme - mağazaya yerleştirme
description: Bu konu, Duvara yerleştirme - Mağazaya yerleştirme işlevi hakkında bilgi sağlar. Bu işlev, bir ürünü, yapılandırılabilir ölçütlere göre bir ön paketleme hazırlık alanıyla birleştirmeniz gereken senaryoları işlemenize olanak tanır. Tek bir hedef plakaya malzeme çekme ve küme malzeme çekmeye göre daha fazla yerine koyma konumu kullanma olanağı sağladığından, malzeme çekme süresinin azalmasına yardımcı olur.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3f2ae63758fcb6247c5e56433645d9252576c755
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996287"
---
# <a name="put-to-wall---put-to-store"></a>Duvara yerleştirme - mağazaya yerleştirme

[!include [banner](../includes/banner.md)]

*Duvara yerleştirme - mağazaya yerleştirme* işlevi, bir ürünü, yapılandırılabilir ölçütlere göre bir ön paketleme hazırlık alanıyla birleştirmeniz gereken senaryoları işlemenize olanak tanır. Bu işlev tek bir hedef plakaya malzeme çekme işlemi yapılmasına izin verdiğinden ve küme malzeme çekmeye göre daha fazla yerleştirme konumu kullanılmasına olanak sağladığından, mağazalara sevkiyat yapan veya küçük miktarlı maddeleri işleyen şirketler, azalan malzeme çekme süresinden faydalanacaktır.

Bu işlev için iş akışı, çekilen ürünü çeşitli türlerde konteynerlerde dağıtılmak üzere bir tasnif yerleşimine yönlendirir. Genellikle, her tasnif yerleşimi birden fazla tasnif konumu içerir. Her tasnif konumu iş süreci tarafından ayarlanan ölçütlere göre atanır. Tipik ölçüt son varış yeri, sevkiyat veya yüktür. Ürün alındıktan sonra sipariş, hedef, sevkiyat veya yük ile ilişkilendirilmiş miktara dayalı olarak her bir tasnif konumuna dağıtılır. Konteyner dolduğunda veya tamamlandığında, iş sürecine bağlı olarak daha fazla işlem yapmak amacıyla bir hazırlama yerleşimine veya sevkiyat yerleşimine taşınır.

Bu ambarlama işlevi, ışık yönlendirmeli ayrıştırma ve zorla açma gibi diğer adlarla da bilinir.

## <a name="turn-on-the-outbound-sorting-feature"></a>Giden tasnif özelliğini açma

*Duvara yerleştirme - mağazaya yerleştirme* işlevini kullanabilmeniz için *Çıkış tasnifi* özelliğinin sisteminizde açık olması gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Giden tasnif*

*Çıkış tasnifi* özelliği, açıksa *Kuruluş genelinde dalga adımı kodu* özelliğiyle birlikte kullanılabilir. Dalga adım kodlarında ayarlanmış önceden tanımlı kodlar kullanacaksanız da bu özelliği etkinleştirmeniz gerekir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Kuruluş genelindeki dalga adım kodu:*

## <a name="setup"></a>Ayar

Bu demo için, standart Contoso verileri ve ambar *62* kullanılır. Daha sonra belirtilen bazı eklemeler de kullanılmıştır.

### <a name="location-type"></a>Yerleşim türü

1. **Ambar yönetimi \> Kurulum \> Ambar \> Yerleşim türleri** öğesine gidin.
1. Eylem bölmesinde, tasnif için yerleşim türü oluşturmak üzere **Yeni**'yi seçin.
1. Aşağıdaki değerleri ayarlayın:

    - **Yerleşim türü:** *TASNİF*
    - **Açıklama:** *Tasnif*

1. **Kaydet**'i seçin.

### <a name="warehouse-management-parameters"></a>Ambar yönetim parametreleri

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Genel** sekmesinde **Yerleşim türleri** hızlı sekmesinde **Tasnif yerleşimi türü** alanına *TASNİF* girin.
1. **Kaydet**'i seçin.

### <a name="location-profile"></a>Yerleşim profili

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.
1. Eylem bölmesinde, tasnif yerleşimi için yerleşim profili oluşturmak üzere **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Yerleşim profili kimliği:** *Tasnif*
    - **Ad:** *Tasnif*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Yerleşim biçimi:** *PAKETLEME*
    - **Yerleşim türü:** *TASNİF*
    - **Plaka izleme kullan:** *Evet*
    - **Karışık maddelere izin ver:** *Evet*
    - **Karışık stok durumlarına izin ver:** *Evet*

1. **Kaydet**'i seçin.

### <a name="locations"></a>Yerleşimler

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konumlar** öğesine gidin.
1. **Yerleşim için denetleme basamakları oluştur** onay kutusunu temizleyin.
1. Eylem bölmesinde **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:

    - **Ambar:** *62*
    - **Yerleşim:** *Tasnif*
    - **Yerleşim profili kimliği:** *Tasnif*

1. **Kaydet**'i seçin.

### <a name="packing-profiles"></a>Paketleme profilleri

1. **Ambar yönetimi \> Kurulum \> Paketleme \> Paketleme profilleri**'ne gidin.
1. Eylem bölmesinde **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:

    - **Paketleme profili kodu:** *Tasnif*
    - **Açıklama:** *Tasnif*
    - **Konteyner paketleme ilkesi:** Bu alanı boş bırakın.
    - **Konteyner kimliği modu:** *Otomatik*
    - **Konteyner türü:** *PALET 48x48*
    - **Konteyner kapatma sırasında konteyneri otomatik oluştur:** Bu alanı boş bırakın.

1. **Kaydet**'i seçin.

### <a name="wave-step-codes"></a>Dalga adım kodları

*Kuruluş genelinde dalga adımı kodu* özelliğini etkinleştirdiyseniz, aşağıdaki kodu ayarlayın.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga adımı kodları**'na gidin.
1. Eylem bölmesinde **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:

    - **Dalga adımı kodu:** *Tasnif*
    - **Dalga adımı açıklaması:** *Tasnif*
    - **Dalga adımı türü:** *Tasnif şablonu*

1. **Kaydet**'i seçin.

### <a name="outbound-sorting-template"></a>Giden tasnif şablonu

Tasnif şablonu, tasnif konumlarının oluşturulup oluşturulmayacağını, hangi ölçütlerin kullanılacağını ve tasnif işleminin diğer özniteliklerini denetler.

1. **Ambar Yönetimi \> Kurulum \> Paketleme \> Giden tasnif şablonu**'na gidin.
1. Eylem bölmesinde, bir tasnif şablonu oluşturmak için **Yeni**'yi seçin.
1. Yeni şablonun üst bilgisinde aşağıdaki değerleri ayarlayın:

    - **Giden tasnif şablonu kodu:** *Dalga Tasnif*
    - **Açıklama:** *Dalga tasnif*
    - **Tasnif şablonu türü:** *Dalga talebi*

        Bu alan, tasnif şablonunun kullanıldığı işlemi tanımlar. Aşağıdaki değerler kullanılabilir:

        - **Dalga talebi**: Tasnif şablonu *Duvara yerleştir* işlemi için kullanılır. Bu şablon türü, paketleme istasyonunu atlamak ve stoğu doğrudan dalga üzerinden işlemek için kullanılır. Bu türü yalnızca **tasnif** dalga işlemi yöntemi dalga şablonuna dahil edilmişse kullanabilirsiniz.
        - **Konteyner**: Tasnif şablonu *Paketlemeden sonra palet oluşturma* işlemi için kullanılır. Bu şablon türü paketleme istasyonunda kapatılmış olan ve paletler üzerinde tasnif edilmesi gereken konteynerleri işlemek için kullanılır.

    - **Ambar:** *62*
    - **Yerleşim:** *Tasnif*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Tasnif doğrulaması:** *Konum tarama*

        Bu alan, tasnif sırasında gerekli olan doğrulamayı tanımlar. Aşağıdaki değerler kullanılabilir:

        - Hiçbiri
        - Plaka taraması
        - Konum taraması

    - **Pozisyon kapanışında iş oluştur:** *Evet*

        Bu seçenek *Evet* olarak ayarlandığında, konum kapatıldığı zaman stoğu nihai sevkiyat yerleşimine taşımak için iş oluşturulur. *Hayır* olarak ayarlanırsa, konum kapatıldığında stok anında sipariş için çekilir.

    - **Konum atama:** *El ile*

        Bu alan konum atama türünü tanımlar. Aşağıdaki değerler kullanılabilir:

        - **El ile**: Kullanıcının her zaman stoğun hangi konumda sıralanacağını belirtmesi gerekir.
        - **Otomaik**: Sistem tasnif şablonu dökümlerini temel alarak mümkün olduğunda stoğu otomatik olarak bir konuma yönlendirir.

    - **Tasnif konumu ata ölçütü:** *Yalnızca boş konum kullan*

        Bu alan, tasnif konumlarında zaten mevcut olan stoğun talep için konum atanırken dikkate alınıp alınmayacağını kontrol eder. Aşağıdaki değerler kullanılabilir:

        - **Yalnızca boş konum kullan**: Önceden ilişkilendirilmiş stoğu olan konumlar dikkate alınacaktır
        - **Konumun boş olduğunu varsay**: Konumda zaten olan tüm stoklar atama sırasında yok sayılır. Kullanılabilir tüm konumlar kullanılır.

    - **Dalga adımı kodu:** *Tasnif*

        *Kuruluş genelinde dalga adımı kodu* özelliği açıksa, *Tasnif* dalga adımı kodu dalga adım kodlarında da ayarlanmalıdır.

    - **Tasnif konumunu otomatik kapat:** *Evet*

        Bu seçenek *Evet* olarak ayarlandığında, konuma gelen tüm iş tamamlandığında, tasnif konumu otomatik olarak kapatılır.

    - **Tasnif konumlarının sayısı:** *3*

        Bu alan, sistemin oluşturulacağı maksimum tasnif konumu sayısını tanımlar.

    - **Tasnif konumu öneki:** *SP-*

        Bu alan, sistemin konum numarasından önce atadığı öneki tanımlar.

    - **Tasnif konumunu otomatik paketle** *Evet*

        Bu seçenek *Evet* olarak ayarlandığında, konum kapatıldığında tasnif konumunda bulunan stok bir konteyner içinde paketlenir.

    - **Paketleme profili kodu:** *Tasnif*

        Bu alana, tasnif konumu bir konteynere paketlenceği zaman kullanılacak paketleme profilini tanımlar.

1. Eylem bölmesinde, bu tasnif şablonu için kullanılan ölçütleri belirtmek üzere **Sorguyu düzenle**'yi seçin.
1. Sorgu iletişim kutusunda, **Tasnif** sekmesinde bir satır eklemek için **Yeni**'yi seçin ve sonra aşağıdaki değerleri ayarlayın:

    - **Tablo:** *ayrıntıları yükle*
    - **Türetilmiş tablo:** *ayrıntıları yükle*
    - **Alan:** *Sevkiyat kodu*
    - **Arama yönü:** *Artan*

1. **Tamam**'ı seçin.
1. Aşağıdaki iletiyi alabilirsiniz: "Gruplama sıfırlanacak, devam edilsin mi?" **Evet**'i seçin.

    Eylem Bölmesindeki **Giden tasnif şablonu dökümleri** düğmesi kullanılabilir duruma gelir.

1. Eylem Bölmesinde, **Giden tasnif şablonu dökümleri**'ni seçin.
1. Sevkiyat koduna göre gruplandırmak için **Alana göre gruplandır** onay kutusunu seçin.

    Bu ayar, her sevkiyat için dalga içindeki bir konteyner olan bir tasnif konumu oluşturur.

1. **Tamam**'ı seçin.

### <a name="wave-process-methods"></a>Dalga işleme yöntemleri

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.
1. Eylem bölmesinde, **Yöntemleri yeniden oluştur**'u seçin.

    **Tasnif** yöntemi kullanılabilir yöntemler listesine eklenir ve bunun için *Sevkiyat* dalga şablonu türü seçilir.

### <a name="wave-templates"></a>Dalga şablonları

Dalga talep tasnifi için kullanılan dalga şablonunu düzenleyin.

1. **Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.
1. **Dalga şablonu türü** alanında *Sevkiyat*'ı seçin.
1. Varolan **62 Sevkiyat varsayılanı** şablonunu seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Genel** hızlı sekmesinde, aşağıdaki değişiklikleri yapın:

    - **Dalgayı ambara serbest bırakma sırasında işle** seçeneğini *Hayır* olarak ayarlayın.
    - **Açık dalgalara ata** seçeneğini *Evet* olarak ayarlayın.

1. **Yöntemler** hızlı sekmesinde, **tasnif** yöntemini ayarlayın:

    1. **Kalan Yöntemler** kılavuzunda, **tasnif**'i seçin.
    2. **Tasnif** yöntemini **Seçili Yöntemler** kılavuzuna taşımak için sağ oku seçin.
    3. **Seçili Yöntemler** kılavuzunda, **tasnif**'i seçin.
    4. **Dalga adımı kodu** alanını *Tasnif* olarak ayarlayın.

1. **Kaydet**'i seçin.

### <a name="mobile-device-menu-items"></a>Mobil cihaz menü öğeleri

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Menü öğesi adı:** *Tasnif*
    - **Başlık:** *Tasnif*
    - **Mod:** *Dolaylı*
    - **Varolan çalışmayı kullan:** *Hayır*

1. **Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:

    - **Faaliyet kodu:** *Giden tasnif*
    - **İşlem kılavuzunu kullan:** *Evet* (varsayılan değer)
    - **Giden tasnif şablonu kodu:** *Dalga Tasnif*

1. **Kaydet**'i seçin.

### <a name="mobile-device-menu"></a>Mobil cihaz menüsü

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
1. Menüler listesinde **Giden**'i seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Kullanılabilir Menüler ve Menü Öğeleri** kılavuzunda, yeni oluşturduğunuz **Tasnif** menü öğesini bulun ve seçin.
1. **Tasnif** i **Menü Yapısı** kılavuzuna taşımak için sağ ok düğmesini seçin. Böylece, yeni menü öğesini **Giden** menüsüne eklersiniz.
1. **Kaydet**'i seçin.

### <a name="location-directives"></a>Konum yönergeleri

Tasnif tamamlandıktan sonra oluşturulan işe kılavuz olacak yerleşim yönergeleri oluşturmanız gerekir.

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. **İş emri türü** alanında *Tasnif edilen stoğu çekme*'yi seçin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **Sıra:** *1*
    - **Ad:** *Baydoor'a yerleştir*

1. **Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Yerine koyma*
    - **Tesis:** *6*
    - **Ambar:** *62*
    - **Yönerge kodu:** Boş bırakın.
    - **Birden çok SKU:** *Hayır*

1. **Satırlar** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Satırlar** hızlı sekmesinde, **Yeni**'yi seçin ve sonra aşağıdaki değerleri ayarlayın. Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Sıra numarası:** *1*
    - **Başlangıç miktarı:** *0*
    - **Son miktar:** *1000000*

1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde, **Yeni**'yi seçin ve sonra aşağıdaki değerleri ayarlayın: Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **Sıra numarası:** *1*
    - **Ad:** *Baydoor*

1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle** düğmesini kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle**'yi seçin.
1. Sorgu iletişim kutusunda, **Aralık** sekmesinde, **Alan** alanının *Yerleşim* olarak ayarlandığı satırı bulun. Bu satır için **Ölçüt** alanını *Baydoor* olarak ayarlayın.
1. Düzenlemeyi onaylamak için **Tamam**'ı seçin.

### <a name="work-classes"></a>İş sınıfları

1. **Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Üst bilgide aşağıdaki değerleri ayarlayın:

    - **İş sınıfı kodu:** *Tasnif*
    - **Açıklama:** *Tasnif*
    - **İş emri türü:** *Tasnif edilmiş stok çekme*

1. **Kaydet**'i seçin.

### <a name="work-templates"></a>İş şablonları

1. **Ambar yönetimi \> İş \> İş şablonları**'na gidin.
1. **İş siparişi türü** alanında *Satış siparişi*'ni seçin.
1. Kılavuzda **62 Paketleme için çek** iş şablonunu seçin.
1. Eylem Bölmesinde **İş başlığı sonları**'nı seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Alan adı** alanının *Sevkiyat Kodu* olarak ayarlandığı satırsa **Bu alan göre sınıflandır** onay kutusunu temizleyin.
1. **Kaydet**'i seçin ve sonra **İş başlığı sonları** iletişim kutusunu kapatın.
1. **İş emri türü** alanında *Tasnif edilen stoğu çekme*'yi seçin.
1. Yeni şablon oluşturmak için **Yeni**'yi seçin.
1. **Genel bakış** bölümünde aşağıdaki değerleri ayarlayın. Tüm diğer alanlar için varsayılan değerleri kabul edin.

    - **İş şablonu:** *Tasnif edilmiş çekme*
    - **İş şablonu açıklaması:** *Tasnif edilmiş çekme*

1. **İş Şablonu Ayrıntıları** bölümünü kullanılabilir hale getirmek için **Kaydet**'i seçin.
1. **İş Şablonu Ayrıntıları** bölümünde, iki satır oluşturacaksınız. **Yeni**'yi seçin ve satır 1 için aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Çekme*
    - **Zorunlu:** Seçili (= *Evet*)
    - **İş sınıfı kodu:** *Tasnif*

1. **Yeni**'yi tekrar seçin ve satır 2 için aşağıdaki değerleri ayarlayın:

    - **İş türü:** *Yerine koyma*
    - **Zorunlu:** Seçili (= *Evet*)
    - **İş sınıfı kodu:** *Tasnif*

1. **Kaydet**'i seçin.

## <a name="example-scenario"></a>Örnek senaryo

Bu senaryo, ambarın yerleşimlerde küçük maddeleri depoladığı ve bu maddelerin sevk edilmeden önce kutular içinde paketlenmesinin gerekli olduğu ve paketleme istasyonu işlevinin gerçekten uygun olmadığı bir durumun benzetimini yapar. Çalışanlar, çekme hızını artırmak için birden fazla müşteri ve farklı adres için aynı anda siparişleri çeker. Çekme işlemi tamamlandıktan sonra çalışanlar, çekilen maddelerin gereken ölçütlere göre doğru kutuya tasnif edilebileceği tasnif yerleşimine gelir. Bu örnekte, sevkiyat kodu doğru kutuyu belirlemekte kullanılır, çünkü her sevkiyat farklı bir adrese sahiptir. Yükteki tüm maddeler paketlendikten ve sevkiyat bazında tasnif edildikten sonra, kutular hazırlama alanına taşınacak ve bir kamyona yüklenecektir.

Senaryoya başlamadan önce, tüm standart ambar işlevlerinin ambarınız için doğru ayarlandığından emin olun. Bu amaç için standart Contoso ambar *62* kullanılır. Kurulumundaki açıklamasının yanı sıra standart yapılandırmalar da değiştirilmemiştir.

### <a name="create-demand"></a>Talep oluşturma

İşlevin gösterilebilmesi için öncelikle bir talep oluşturmanız gerekir. Bu senaryo için, farklı teslimat adresleri benzetimi yapmak için üç farklı müşteriye ait üç satış siparişi oluşturacaksınız. Bu şekilde, üç ayrı sevkiyat oluşturacaksınız.

Satış siparişlerini ve sevkiyatları oluşturabilmeniz için, çekme yerleşimlerinde siparişlerdeki tüm maddeler için yeterli stok bulunduğundan emin olun. Satış siparişi çekme için kullanılan çekme yerleşimlerini onaylamak için yerleşim yönergesi ayarlarını gözden geçirin. Stoku ayarlamanız gerekiyorsa, el ile hareketler oluşturabilir, stok yenilemeyi veya başka bir akışı kullanabilirsiniz. Ardından stoğu rezerve edin.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Sipariş 1 için satış siparişi oluşturmak üzere **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri:** *US-001*
    - **Ambar:** *62*

1. **Tamam**'ı seçin.
1. **Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir. Aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *5*

1. **Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0002*
    - **Miktar:** *10*

1. Stok rezerve etmek için, siparişteki her satış satırı için aşağıdaki adımları yineleyin:

    1. **Satış siparişi satırları** hızlı sekmesinde **Stok** menüsünde **Rezervasyon**'u seçin.
    1. **Rezervasyon** sayfasında, **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.
    1. **Kaydet**'i seçin.

1. Sipariş 2 için satış siparişi oluşturmak üzere **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri:** *US-004*
    - **Ambar:** *62*

1. **Tamam**'ı seçin.
1. **Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir. Aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *7*

1. **Satır ekle**'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0002*
    - **Miktar:** *3*

1. Stok rezerve etmek için, siparişteki her satış satırı için aşağıdaki adımları yineleyin:

    1. **Satış siparişi satırları** hızlı sekmesinde **Stok** menüsünde **Rezervasyon**'u seçin.
    1. **Rezervasyon** sayfasında, **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.
    1. **Kaydet**'i seçin.

1. Sipariş 3 için satış siparişi oluşturmak üzere **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri:** *US-007*
    - **Ambar:** *62*

1. **Tamam**'ı seçin.
1. **Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir. Aşağıdaki değerleri ayarlayın:

    - **Madde numarası:** *A0001*
    - **Miktar:** *8*

1. Satış satırı için stok rezerve etmek üzere aşağıdaki adımları izleyin:

    1. **Satış siparişi satırları** hızlı sekmesinde **Stok** menüsünde **Rezervasyon**'u seçin.
    1. **Rezervasyon** sayfasında, **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.
    1. **Kaydet**'i seçin.

Her satış siparişini ambara serbest bırakmak için aşağıdaki yordamı tamamlayın. Üç farklı sevkiyat oluşturulacaktır. Daha sonra, üç sevkiyatı da tek bir yeni dalgaya ekleyeceksiniz.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Kılavuzda, oluşturduğunuz ilk satış siparişini seçin.
1. Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.

    Ouşturulan dalga kimliğini ve sevkiyat kimliğini gösteren bir bilgi iletisi alırsınız.

1. Satış siparişi 2 ve 3'ü ambara serbest bırakmak için önceki adımları yenileyin. Aldığınız bilgi iletisinin, satış siparişi 1'i serbest bıraktığınızda oluşturulan dalgaya bir sevkiayt eklendiğini belirttiğine dikkat edin.
1. **Ambar yönetimi \> Giden dalgalar \> Sevkiyat dalgaları \> Tüm dalgalar**'a gidin.
1. **Dalgalar** sayfasını açmak için satış siparişlerinin serbest bırakma işleminden oluşturulan dalga kodunu seçin. Bu sayfa, dalga ayrıntılarını gösterir. **Dalga satırları** hızlı sekmesi oluşturulan sevkiyatları gösterir.

    Malzeme çekme yerleşimlerinden alınan maddeleri sıralama yerleşimine getirmek için şimdi iş oluşturmanız gerekir.

1. Eylem Bölmesinde, **İşlem**'i seçin.

    Dalga işleme sırasında tasnif yöntemi, stoğu tasnif konumlarına atamak için tasnif şablonunu kullanır. Dalga işleme tamamlandığında, işin oluşturulduğunu ve dalganın deftere nakledildiğini gösteren bilgi iletisi alırsınız.

1. Eylem Bölmesinde, **Dalga** sekmesinde, **İlgili bilgi** grubunda, oluşturulan işi görüntülemek için **İş**'i seçin. İş kodunu not edin.
1. **Ambar yönetimi \> Paketleme ve konteyner kullanımı \> Giden tasnif konumu atamaları**'na gidin.
1. Sol sütunda, her sevkiyat için oluşturulan giden tasnif konumunu görüntüleyebilirsiniz.
1. **Tasnif konumu ölçütleri** hızlı sekmesinde, o konumun sevkiyat kodunu görüntüleyebilirsiniz.

Stoğu malzeme çekme yerleşimlerinden tasnif yerleşimine getirmek için bir iş oluşturulmuştur. İşi tamamlamak için, dalga işleme sırasında oluşturulan iş koduna ihtiyacınız olacaktır.

### <a name="sales-order-picking-to-the-sorting-location"></a>Tasnif yerleşimine satış siparişi çekme

1. Mobil cihazınızdan Ambar *62*'de çalışan olarak oturum açın.
1. Ana menüde **Giden**'i seçin.
1. **Giden** menüsünden **Satış Çekme**'yi seçin.
1. **Kod** alanını seçin ve sonra dalga işlemeden gelen iş kodunu girin.
1. Girişinizi onaylayın.

    Sonra, bir hedef plaka (LP) girmeniz istenir. Satış siparişi 1' deki satır 1'in çekilip hedef plakaya eklenmesi gereken öğe olduğunu unutmayın. Madde numarası, miktar, madde açıklaması ve çekme yerleşimi gösterilir.

1. **Hedef LP** alanında plaka numarasını girin.

    İşlenen bir dalgadan oluşturulan tüm satırları aynı hedef plakaya çekeceksiniz.

1. Girişinizi onaylayın.

    Mobil uygulama şimdi, sizi çekme yerleşimine ve çekilmesi gereken maddeye ve miktara yönlendireen bir dizi **Çekme** sayfası sunar. Çekilen madde plakaya eklendikten sonra çekme işini onaylarsınız. Son sayfa, çekilen maddeleri tasnif konumuna yerleştirecek iş olacaktır.

1. İlk çekme işini onaylayın.
1. Sonraki çekme işi görüntülenir. Çekme işlemini onaylayın.
1. Kalan çekme işini onaylamak için devam edin.
1. Son adım, yerine koyma işini tamamlamaktır. Tasnif yerleşiminde yerine koymayı onaylayın.

    Bir "İş tamamlandı" iletisi alırsınız.

1. Mobil uygulamada **Satış Çekme**'den çıkın.

### <a name="sortingput-to-wall"></a>Tasnif/duvara yerleştirme

Tüm stoklar tasnif yerleşimine konulduğu için, doğru tasnif konumuna tasnif edilmesi gerekir.

1. Mobil uygulamada oturum açın.
1. Ana menüde **Giden**'i seçin.
1. **Giden** menüsünde, maddeleri tasnif etmeye başlamak için **Tasnif**'i seçin.
1. **LP/YER** alanına, çekilen satış siparişi işinin hedef plakasını girin.
1. Girişinizi onaylayın.
1. Öncelikle tasnif edilecek madde numarasını girin.
1. Sistem, gösterilmesi gereken ilk tasnif konumunu belirler. Tasnif konumunu onaylayın.
1. Tasnif konumuna bir plaka atamanız istenir. **LP** alanını seçin, plaka numarası girin ve sonra girişinizi onaylayın.

    Tasnif konumu sevkiyat koduyla ilişkili olduğundan, çekilen maddeleri giden sevk irsaliyesine ve satış siparişine özel olan bir plakaya tasnif edersiniz.

    Sonraki sayfada madde kodu, miktar, tasnif konumu kodu ve "kaynak" (malzeme çekme) ve "hedef" (tasnif) plaka kodları gösterilir. Bu sayfadaki bilgiler, belirtilen madde ve miktarları malzeme çekme plakasından tasnif plakasına tasnif etmenizi belirtir.

1. Tasnif konumunu onaylayın.
1. İlk tasnif konumundaki maddeleri tasnif edin. Bitirdiğinizde, sistem sizi sonraki tasnif konumuna yönlendirir.
1. Bu işlemi, iş emrindeki tüm çekilen satırlar için yineleyin. Aynı madde numarasına sahip birden fazla çekme satırı olduğunda da bu işlemi kullanmanız gerekir.

    Bu işlemi tüm maddeler için tekrarlamak amacıyla, sistem ölçütü bir sonraki taranan maddeden (iş satırı) değerlendirir ve hangi tasnif konumuna konulması gerektiğini belirler. Maddeyi doğru tasnif konumuna koymak için otomatik olarak yönlendirilirsiniz. Onay kurulumuna bağlı olarak, konum numarasını veya plaka kodunu girerek bu eylemi onaylamak üzere de yönlendirilirsiniz.

    > [!NOTE]
    > Otomatik tasnif açıksa el ile geçersiz kılma kullanılamaz.

1. Bitirdiğinizde, Microsoft Dynamics 365 Supply Chain Management'ta konumların durumunu gözden geçirmek için **Giden tasnif konumu atamaları** sayfasını açın.

    - Konumlar otomatik olarak kapatılırsa, kapalı konumları göstermek için **Kapatılanı göster**'i seçin.
    - Tasnif konumu hareketlerinin gösterildiğine dikkat edin. Konumla işlenen madde ve miktar gösterilir.

    Giden tasnif şablonunu ayarlarken, **Tasnif konumunu otomatik kapat** seçeneğini *Evet* olarak ayarlarsınız. Bu nedenle, son beklenen stok koyulduktan sonra konum otomatik olarak kapatılır. Tasnif pozisyonları **Kapalı** durumundadır ve iş tasnif edilen stoğu *Bölme kapısı* yerleşimine taşımak üzere oluşturulmuştur.

1. Stoğu sevkiyat yerleşimine taşımak için tasnif edilmiş stok malzeme çekme işini tamamlayın. Stok hazır olduğunda, sevkiyat için onaylayın.

> [!NOTE]
> Tasnif edilen stok çekme işinin doğru olarak işlenmesi için, taşıma ve yükleme işlemleri için **İş emri türü** alanının *Tasnif edilmiş stok çekme* olarak ayarlandığı iş sınıfı koduna sahip bir mobil cihaz menüsü kullanılmalıdır.

### <a name="manually-close-a-position-optional"></a>Konumu el ile kapatma (isteğe bağlı)

Tasnif konumlarının el ile kapatılması gerekiyorsa, giden tasnif şablonu için **Tasnif konumunu otomatik kapat** seçeneği *Hayır* olarak ayarlanmalıdır ve stoğun bölme kapısı alanına taşınabilmesi için kapatma işlemi yapılmalıdır. Konumlar çeşitli şekillerde kapatılabilir:

- Ambar uygulaması aracılığıyla:

    - Kullanıcı, zaten o konumdaki maddelerden birini tarayabilir ve konumu kapatmak için **Kapat**'ı seçebilir.
    - Kullanıcı zaten tasnif edilmiş bir konteyneri tararsa, bir hata iletisi görüntülenir. Ancak, kullanıcı konumu kapatmaya devam edebilir.

- Microsoft Dynamics 365 Supply Chain Management **Giden tasnif konum atamaları** sayfasından:

    - Kullanıcı giden tasnif konumu kaydını seçebilir ve sonra Eylem Bölmesinde **Konumu kapat**'ı seçebilir.

## <a name="tips"></a>İpuçları

- Maddeler birine atandıktan sonra konumlar arasında taşınamaz. Sistem her bir maddeden kaç tanesinin belirtilen konuma gitmesi gerektiğini değerlendirir.
- Tasnifler şablonu, konumlar kapatıldığında konteynerleri otomatik olarak oluşturmak üzere yapılandırılabilir. Bu yaklaşım, belirtilen paketleme profilini temel alan standart konteyner kodu yapısı oluşturur.

> [!IMPORTANT]
> Hareket işi tasnif yerleşiminden oluşturulduktan sonra, işi iptal etmeniz gerekir. Aksi durumda, konum ve içerdiği konteynerler sistemden silinir ve daha fazla işlem için kullanılamaz. Stok da kaldırılır.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]