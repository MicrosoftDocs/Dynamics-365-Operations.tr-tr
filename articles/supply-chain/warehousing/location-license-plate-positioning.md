---
title: Yerleşim plakası konumlandırmasıı
description: Lisans levhası yerleşim konumlama, Çift-derin palet yerleşiminden oluşan yerleşim gibi, bir lisans kalıbının çok palet bir yerleşimde nerede konumlanıldığını görmenizi sağlar.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 1235f8fa64fbc87a4c22f4dcf0e9ddd4b4565b76
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359775"
---
# <a name="location-license-plate-positioning"></a>Yerleşim plakası konumlandırmasıı

[!include [banner](../includes/banner.md)]

Lisans levhası yerleşim konumlama, Çift-derin palet yerleşiminden oluşan yerleşim gibi, bir lisans kalıbının çok palet bir yerleşimde nerede konumlanıldığını görmenizi sağlar.

Özellik bir depolama konumuna yerleştirilecek her lisans kalıbına bir sıra numarası ekler. Bu sıra numarası depolama konumundaki lisans levhalarını sipariş etmek için kullanılır. Bu nedenle, özellik, müşterilerin yer çekimi takılabilir bir sistemi kullandığı ve malzeme çekme amaçları doğrultusunda, hangi lisans kalıbının öne geldiği ile ilgili bilinmesi gereken senaryoları akıllıca destekler.

Bu konu özelliğin nasıl ayarlanacağını ve kullanılacağını gösteren bir senaryo sunar.

## <a name="turn-on-the-location-license-plate-positioning-feature"></a>Konum lisans plağı konumlandırma özelliğini aç

Lisans plakası konumlanırmayı kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı**: *Konum lisans plağı konumlandırma*

## <a name="example-scenario"></a>Örnek senaryo

### <a name="make-sample-data-available"></a>Örnek verilerini kullanılabilir hale getirme

Burada önerilen değerleri kullanarak bu senaryoyla çalışmak için, örnek verilerinin yüklenmiş olduğu bir sistemde çalışmanız gerekir. Ek olarak, başlamadan önce **USMF** tüzel kişiliğini seçmeniz gerekir.

### <a name="set-up-the-feature-for-this-scenario"></a>Bu senaryo için özellik ayarla

Bu konuda sunulan senaryoya ait *konum lisans levhası konumlandırma* özelliğini ayarlamak için aşağıdaki yordamları tamamlayın.

#### <a name="location-profiles"></a>Konum profilleri

Özelliğin, kullanılacağı her yerleşim için konum profilinde açık olması gerekir.

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.
1. Sol bölmedeki yerleşim profilleri listesinde, **toplu-06** seçeneğini belirleyin.
1. **Genel** hızlı sekmesinde, özellik tarafından iki yeni seçenek eklenmiştir. Aşağıdaki değerleri ayarlayın:

    - **Lisans plağı konumunu etkinleştir:** *Evet*

        Bu seçenek *Evet* olarak ayarlandığında , bu konumdaki lisans levhaları için lisans levhası konumu korunur.

    - **Mobil aygıtı görüntüle LP konumu:** *Evet*

        Bu seçenek *Evet* olarak ayarlandığında lisans levhası konumu ayarlama ve sayma sırasında mobil cihaz kullanıcıları tarafından gösterilir. Bu seçeneğin ayarını yalnızca özellik açık olduğunda değiştirebilirsiniz.

1. **Kaydet**'i seçin.

#### <a name="location-directives"></a>Konum yönergeleri

1. **Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.
1. Sol bölmede, **iş emri türü** alanının *satış siparişleri* olarak ayarlandığından emin olun.
1. Konum yönergeleri listesinde, **61 SO Alma siparişi** seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **Satırlar** hızlı sekmesinde, **sıra numarası** değeri *2* olan satırı seçin.
1. **Konum yönergesi eylemleri** hızlı sekmesinde, *daha az palet için çekme* **adı** değeri olan satırı seçin  (tek satır olmalıdır) ve **sıra numarası** değerini *2* olarak değiştirin.
1. Yeni bir konum yönergesi eylemine satır eklemek için kılavuzun üzerinde **yeni** 'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Sıra numarası:** *1*
    - **Ad:** *seçim pozisyonu 1*

1. Yeni satır seçiliyken, kılavuzun üzerinde **Düzenle sorgu** seçin.
1. Sorgu düzenleyicisinde, **birleşimler** sekmesini seçin.
1. **Stok boyutları** tablosuna birleşimi göstermek için **yerleşimler** tablosunu genişletin.
1. **Mevcut envanter** tablosuna birleşimi göstermek için **envanter boyutları** tablosunu genişletin.
1. **Stok boyutlarını** seçin ve sonra **tablo katılımı Ekle**'yi seçin.
1. Görünen tablolar listesinde, **ilişki** sütununda, **Lisans levhasını (lisans levhası)** seçin. Daha sonra **Stok boyutları** tablo katılmasınına **lisans levhası** eklemek için **Seç**'i seçin.
1. **Lisans levhası** seçiliyken, **Tablo bağlaması ekle**'yi seçin.
1. Görünen tablolar listesinde, **ilişki** sütununda, **Konum lisans levhası konumlandırma (lisans levhası)** seçin. Daha sonra **Stok boyutları** tablo katılmasınına **Konum lisans levhası konumlandırma** eklemek için **Seç**'i seçin.

    ![Tablo birleştirmeleri.](media/LpTableJoin.png "Tablo birleştirmeleri")

1. Güncelleştirilen birleştirilmiş tabloları onaylamak ve sorgu düzenleyicisini kapatmak için **Tamam** 'ı seçin.
1. **Yerleşim yönergesi eylemleri** hızlı sekmesinde sorgu düzenleyiciyi açmak için **Sorguyu düzenle**'yi seçin.
1. **Aralık** sekmesinde, kılavuza satır eklemek için **Ekle**'yi seçin.
1. Yeni satırda aşağıdaki değerleri ayarlayın:

    - **Tablo**: *Konum lisans plağı konumlandırma*
    - **Türetilmiş tablo**: *Konum lisans plağı konumlandırma*
    - **Alan:** *LP Konumu*
    - **Ölçüt:** *1*

    ![Yeni aralık.](media/LpPositionCriteria.png "Yeni Aralık")

1. Değişikliklerinizi onaylayıp sorgu düzenleyicisi kapatmak için **Tamam**'ı seçin.

### <a name="set-up-sample-data-for-this-scenario"></a>Bu senaryo için örnek verilerini ayarla

Bu senaryo için, kullanıcının, iş yapması amacıyla ambar *61* için ayarlanmış bir çalışanı kullanarak ambar mobil uygulamada oturum açması gerekir. Ayrıca, kullanıcının hareketleri tamamlaması de gerekir.

*Konum lisans levhası konumlandırma* özelliği bir konumdaki lisans levhası konumları için yeni bir tanımlayıcı eklemesine göre, önce senaryoyu destekleyecek bazı verileri oluşturmanız gerekir.

#### <a name="spot-count-the-first-location"></a>Nokta-ilk konumu say

1. Ambar mobil uygulamasında ambar *61*'deki bir kullanıcı olarak oturum açın.
1. **Stok \> nokta sayma** gidin.
1. **Nokta sayım** sayfasında, **Konum** alanını *01A01R1S1B* olarak ayarlayın.
1. **Tamam**'ı seçin.

    Sayfa, girdiğiniz konumu gösterir. Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"

1. Yerleşime sayı eklemek için **Yenile** seçin.
1. **Döngü sayımında: Yeni LP veya madde Ekle** sayfası, **madde** alanını seçin ve *A0001* değerini girin.
1. **Tamam**'ı seçin.
1. **Döngü sayımı: Yeni LP veya madde** sayfası ekle, **LP** alanını seçin ve *LP1001* değerini (veya istediğiniz diğer tüm lisans plakası numarasını) girin.

    **Döngü sayısı: Yeni LP veya madde ekle** sayfası **Lisans plağı 1. konumu** gösterir.

1. **Tamam**'ı seçin.

    Şimdi, lisans kalıbına sayılan madde miktarını belirtmeniz gerekir.

1. **Miktar** alanı *10* olarak ayarlanmıştır.
1. **Tamam**'ı seçin.

    Sayfa, girdiğiniz konumu gösterir. Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"

1. Yerleşime başka sayı eklemek için **Yenile** seçin.
1. **Döngü sayımında: Yeni LP veya madde Ekle** sayfası, **madde** alanını seçin ve *A0002* değerini girin.
1. **Tamam**'ı seçin.
1. **Döngü sayımı: yenı LP veya madde ekle** sayfası, **LP** alanını seçin ve sonra *LP1002* değerini (veya daha önce belirttiğiniz lisans plakasından farklı olarak istediğiniz diğer herhangi bir lisans plakası numarası) girin.
1. **LP Konumu** alanını *2* olarak ayarlayarak, lisans levhası konumunu değiştirin.
1. **Tamam**'ı seçin.
1. **Miktar** alanını *10* olarak ayarlayarak, lisans plakası üzerinde sayılan maddenin miktarını belirtin.
1. **Tamam**'ı seçin.

    Sayfa, girdiğiniz konumu gösterir. Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"

1. **Tamam**'ı seçin.

İş artık tamamlanmıştır.

#### <a name="spot-count-the-second-location"></a>Nokta ikinci konumu say

1. **Nokta sayım** sayfasında, **Konum** alanını *01A01R1S2B* olarak ayarlayın.
1. **Tamam**'ı seçin.

    Sayfa, girdiğiniz konumu gösterir. Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"

1. Yerleşime sayı eklemek için **Yenile** seçin.
1. **Döngü sayımında: Yeni LP veya madde Ekle** sayfası, **madde** alanını seçin ve *A0002* değerini girin.
1. **Tamam**'ı seçin.
1. **Döngü sayımı: yenı LP veya madde ekle** sayfası, **LP** alanını seçin ve sonra *LP1003* değerini (veya daha önce belirttiğiniz lisans plakasından farklı olarak istediğiniz diğer herhangi bir lisans plakası numarası) girin.

    **Döngü sayısı: Yeni LP veya madde ekle** sayfası **Lisans plağı 1. konumu** gösterir.

1. **Tamam**'ı seçin.
1. **Miktar** alanını *10* olarak ayarlayarak, lisans plakası üzerinde sayılan maddenin miktarını belirtin.
1. **Tamam**'ı seçin.

    Sayfa, girdiğiniz konumu gösterir. Ayrıca şu iletiyi gösterir: "yerleşim tamamlandı, yeni LP veya öğe Ekle?"

1. **Tamam**'ı seçin.

İş artık tamamlanmıştır.

#### <a name="work-details"></a>İş ayrıntıları

> [!NOTE]
> Mobil uygulamadaki nokta sayıları Microsoft Dynamics 365 içinde iş döngüsü sayımı işi oluştur. İş, sayımlar stoka nakledilmeden önce kabul edilmesini gerektirir.

1. Dynamics 365 Supply Chain Management'da oturum açın
1. **Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.
1. **Özet** sekmesinde, aşağıdaki değerlere sahip satırları arayın:

    - **İş emri türü:** *döngü sayımı*
    - **Ambar:** *61*
    - **İş durumu:** *Gözden geçirme bekleniyor*

    Bu satırlar için iki iş kodu oluşturulmuş olmalıdır. Bu iş kimliklerinin her ikisi için olan sayımlar kabul edilmesi gerekir.

1. Kılavuzda, *döngü sayımı* iş emri türü için ilk Iş kodunu seçin.
1. Eylem Bölmesinde **İş** sekmesindeki **İş** grubunda **döngü sayımı**'nı seçin.

    Her biri her madde ve lisans levhası için olmak üzere iki satır gösterilir. **Sayılan miktar**, **yerleşim**, **Lisans levhası** ve **madde** alanlarındaki değerler, mobil cihazda oluşturduğunuz sayım girişleriyle eşleşmelidir. Bu alanlardan herhangi biri görünmüyorsa, kılavuza eklemek Için eylem bölmesindeki **boyutları görüntüle**'yi seçin.

1. Her iki satırı da seçin.
1. Eylem Bölmesinde, **Sayımı kabul et**'i seçin.
1. "Deftere nakil günlüğü" iletisi alıyorsunuz. Deftere nakledilen günlük numarasını görüntülemek için **ileti ayrıntılarını** seçin.
1. İleti ayrıntılarını kapatın.
1. **İş** sayfasını yenileyin.

    İlk iş kodu kapatıldı ve artık gösterilmemektedir.

    > [!TIP]
    > Kapatılan çalışmayı görüntülemek için kılavuzun üzerindeki **kapalı göster** onay kutusunu seçin.

    Şimdi, *01A01R1S2B* konumundaki lisans levhası için işi kabul etmiş olursunuz.

1. **Genel bakış** sekmesinde *döngü sayımı* iş emri türü için ikinci iş kodunu seçin.
1. Eylem Bölmesinde **İş** sekmesindeki **İş** grubunda **döngü sayımı**'nı seçin.

    Madde ve lisans levhası için bir satır gösterilir. **Sayılan miktar**, **yerleşim**, **Lisans levhası** ve **madde** alanlarındaki değerler, mobil cihazda oluşturduğunuz sayım girişleriyle eşleşmelidir.

1. Satırı seçin.
1. Eylem Bölmesinde, **Sayımı kabul et**'i seçin.
1. "Deftere nakil günlüğü" iletisi alıyorsunuz. Deftere nakledilen günlük numarasını görüntülemek için **ileti ayrıntılarını** seçin.
1. İleti ayrıntılarını kapatın.
1. **İş** sayfasını yenileyin.

    İkinci iş kodu kapatıldı ve artık gösterilmemektedir.

    > [!TIP]
    > Kapatılan çalışmayı görüntülemek için kılavuzun üzerindeki **kapalı göster** onay kutusunu seçin.

#### <a name="on-hand-by-location"></a>Konuma göre eldeki

1. **Ambar yönetimi \> Sorgular ve raporlar \> Yerleşime göre eldeki**'ye gidin.
1. Aşağıdaki değerleri ayarlayın:

    - **Tesis:** *6*
    - **Ambar:** *61*
    - **Konumlar arasında Yenile:** *Evet*

1. *01A01R1S1B* konumunun iki lisans tabakadığına sahip olduğuna dikkat edin:

    - **A0001**, **LP Konumu** alanının *1* olarak ayarlandığı yerdir
    - **A0002**, **LP Konumu** alanının *2* olarak ayarlandığı yerdir

1. *01A01R1S2B* konumunun bir lisans tabakadığına sahip olduğuna dikkat edin:

    - **A0002**, **LP Konumu** alanının *1* olarak ayarlandığı yerdir

### <a name="sales-order-scenario"></a>Satış siparişi senaryosu

*Yerleşim lisansı plak konumlama* özelliği ayarlanmış ve stok hazırlanmıştır, böylece ambar çalışanını Palet kodunun pozisyon *1* ' deki stok yerleşiminden çekme maddesi *A0002* yönlendirecek şekilde bir satış siparişi oluşturmanız gerekir.

1. **Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. **Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:

    - **Müşteri hesabı:** *US-004*
    - **Ambar:** *61*

1. **Tamam**'ı seçin.
1. **Satış siparişi satırları** hızlı sekmesine yeni bir satır eklenir. Bu yeni satırda aşağıdaki değerleri ayarlayın.

    - **Madde numarası:** *A0002*
    - **Miktar:** *1*

1. Kılavuzun üzerindeki **stok** menüsünde **rezervasyon**'yı seçin.
1. **Rezervasyon** sayfasında, Eylem Bölmesi'nde sipariş satırı için envanter rezerve etmek için **Lotu rezerve et**'i seçin.
1. **Rezervasyon** sayfasını kapatın.
1. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.

    Satış siparişi için oluşturulan dalga kimliğini ve sevkiyat kimliklerini gösteren bilgi iletileri alırsınız.

1. **Satış siparişi satırları** hızlı sekmesinde kılavuz üzerinde **Ambar** menüsünde **İş ayrıntıları**'nı seçin.
1. **İş** sayfası görüntülenir ve satış satırı için oluşturulan işi gösterir. Gösterilen iş kimliğini not edin.

### <a name="sales-picking-scenario"></a>Satış malzeme çekme senaryosu

1. Mobil uygulamasında ambar *61*'deki bir kullanıcı olarak oturum açın.
1. **Giden \> Satış Çekme**'yi gidin.
1. **Iş kodu Tara/lisans levhası kimlik** sayfasında **kimlik** alanını seçin ve satış satırındaki iş kodunu girin.
1. Malzeme çekme çalışmasının *A0002* *01A01R1S2B* konumundan maddeyi çekmesini yönlendirdiğine dikkat edin. Bu yönergeyi, madde *A0002* Bu konumdaki *1* konumunda bulunan bir lisans kalıbının açık olması nedeniyle alırsınız.

    ![Pozisyon 1 konumu.](media/LocationLicensePlatePositioning.png "Pozisyon 1 konumu")

1. Konum için oluşturduğunuz lisans plakası kodunu girin ve satış siparişini seçmek için istemleri izleyin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]