---
title: Sistem tarafından yönlendirilen küme malzeme çekme
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta sistemle yönlendirilen küme çekmeye genel bir bakış sağlar.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkCluster, WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: dca006ca00e7ff5aa3681daac713f1e93187cd9c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239217"
---
# <a name="system-directed-cluster-picking"></a>Sistem tarafından yönlendirilen küme malzeme çekme

[!include [banner](../includes/banner.md)]

Küme çekme işlemi, çoklu siparişlere ait maddeleri çekme kümelerinde kümeleyerek aynı anda çekmenizi sağlayan bir parça malzeme çekme işlemidir. Daha sonra çekme konumunu yalnızca bir kez ziyaret etmeniz gerekir. Genellikle, bu işlevsellik küçük sipariş çekme veya sandık miktarından az olan miktarlarla kullanılır.

Sistem tarafından yönlendirilen küme çekme işlemi ayarlandığında, sistem tarafından üretilen bir kümeye dayalı olarak küme çekme iş başlıkları oluşturabilirsiniz. Sistem kümesi-küme profilinde belirtilen konum sayısına kadar olan siparişler. Bu nedenle, el ile küme oluşturmak zorunda kalmadan, aynı anda birden fazla siparişi seçebilirsiniz.

Sisteme yönlendirilmiş küme çekme işlemi, küme oluşturmak için küme profilinin kullanıldığı el ile küme oluşturmaya yönelik bir seçenek sunar. Küme profilinde kullanılmadan önce, bazı kurulumla ilgili satırların tanımlanması gerekir:

- **Pozisyon sayısı**, kümeye yerleştirilecek sipariş sayısına karşılık gelir. Bu nedenle, sepet sayısına karşılık gelir.
- **Kümeyi ayır**, kümenin ne zaman bölüneceği belirler.
- **Küme kimliği oluştur**, kullanıcı tarafından oluşturulup oluşturulmayacağını veya Kullanıcı tarafından girilip girilmediğini denetler.
- **Doğrulama türünü sınıflandır**, pozisyon doğrulamanın gerekli olup olmadığını belirtir.

Yeni bir mobil cihaz menü öğesi, sistem tarafından yönlendirilmiş küme çekme işlemi için kullanılır. Seçilen **yönlendirilmiş** seçeneği için **küme profili kimliği** belirtilmelidir. Ek olarak, sistem tarafından yönlendirilen iş sırası sorguları, şirkete özel ölçütlere göre siparişleri gruplandırabilir. Bu nedenle, sistem yönlendirilmiş iş sıralama sorgularu özelleştirilmiş Sıralama ölçütleri belirleyerek, iş siparişlerinin atanmasını daha da iyi duruma getirebilirsiniz.

Sisteme yönlendirilmiş küme çekme işlemi yapıldığında, ambar çalışanları malzeme çekme emirlerinin küme konumlarına yeniden atanmış olduğu bir kümeyle sunulur. Bu nedenle, çalışanlar çekme konumunu yalnızca bir kez ziyaret ederek çoklu iş emirleri için bir madde çekebilirsiniz. Sistemle yönlendirilen küme çekme işlemi için malzeme çekme süreci, Kullanıcı tarafından yönlendirilen küme çekme işlemiyle aynıdır.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Sisteme yönlendirilmiş küme malzeme çekme özelliğini etkinleştir

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanabilir. Burada, özellik şu şekilde listelenmiştir:

- **Modül** - Ambar yönetimi
- **Özellik adı** - Sisteme yönlendirilmiş küme malzeme çekme

Bu özellik, bağımlı bir özelliği etkinleştirmeyi de gerektirir. Bağımlı Özellik:

- **Modül** - Ambar yönetimi
- **Özellik adı** - kuruluş çapında sistem yönlendirilmiş çalışma sıralaması

## <a name="set-up-system-directed-cluster-picking"></a>Sistem tarafından yönlendirilen küme malzeme çekme ayarlama

### <a name="create-cluster-profiles"></a>Küme profilleri oluşturma

Küme profilleri, sistemin her kümeyi nasıl oluşturduğunu denetler. Farklı kümeler gerekiyorsa, her mobil cihaz menü öğesi için farklı bir küme profili oluşturulmalıdır.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Küme profilleri**'ne tıklayın.
2. **Yeni**'yi seçin.
3. **Küme profil kodu** alanına **2 pozisyon** girin.
4. **Ad** alanına, **Pozisyon 2** yazın.
5. **Genel** hızlı sekmesinde, aşağıdaki bilgileri girin:

    - **Küme kimliği oluştur** - **Evet** seçin. Bu seçenek, küme kimliğinin sistem tarafından otomatik olarak oluşturulup oluşturulmayacağını veya kullanıcının çekme başlangıcında bunu oluşturup oluşturmayacağını belirler. 
    - **Pozisyonları Etkinleştir** - **Evet**'i seçin. Bu seçenek pozisyon adlarının ayar adına göre otomatik olarak oluşturulup oluşturulmayacağını belirler. Bu seçenek **Hayır** olarak ayarlıysa değilse konum için plaka kimliği kullanılır.
    - **Pozisyon sayısı:** **2**'yi seçin. Bu alan, kümede olabilecek maksimum pozisyon sayısını (yani kutu, sepetler vs. sayısı) belirler.
    - **Konum adı:** sayısalların sürekli numaralar kullanılarak adlandırılmaları için **sayısal**'i seçin. **Alfabetik**'ı seçerseniz, pozisyonlar alfabetik düzende adlandırılır.
    - **Kümeyi kesme zamanı:** **Yerine koy** seçeneğini belirleyin. Bu alan kümenin ne zaman kesildiğini belirler. 
    - **Sıralama doğrulama türü:** **konum taramayı** seç. Bu alan, yerine koyma adımının doğrulanıp doğrulanmayacağını belirler.
        
6. **Küme sıralama** hızlı sekmesinde, yeni bir satır oluşturup aşağıdaki bilgileri ayarlayarak sıralama ölçütü tanımlayabilirsiniz:

    - **Sıralama numarası** - **1**'i seçin. Bu alan, sistemin sıralama yaptığı sırayı belirler. Otomatik olarak bir değer girilir, ancak bunu gereksinim duyduğunuz gibi değiştirebilirsiniz.
    - **Alan adı:** **WMSLocationId**'i girin. Bu alan, satırla ilgili sıralama ölçütü için kullanılan alanı belirler.
    - **Sıralama:** **artan**'ı seçin. Bu alan, sıralamanın artan veya azalan sırada yapılıp yapılmadığını tanımlar.

### <a name="create-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi oluşturma

Sisteme yönlendirilmiş kümenin çekilmesi için yeni bir mobil cihaz menü öğesi oluşturmak ve küme profil kimliğini mobil cihaz menü öğesine bağlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü öğeleri** seçeneğine gidin.
1. **Yeni**'yi seçin.
1. Üstbilgi bölümüne aşağıdaki bilgileri girin:
    - **Menü öğesi adı** - SD kümesi
    - **Başlık** - SD küme
    - **Mod** - İş
    - **Varolan çalışmayı kullan** - Evet

1. **Genel** hızlı sekmesinde, aşağıdaki bilgileri girin:
    - **Yöneten** - Sistem tarafından yönlendirilen küme malzeme çekme
    - **Plaka oluştur** - Evet
    - **Küme profili kimliği** - konum 2

1. **İş sınıfları** hızlı sekmesinde, mobil aygıt menü öğesi için geçerli iş sınıflarını konfigüre etmek üzere aşağıdaki adımları izleyin:
    - **İş sınıfı kodu** - Satış
    - **İş emri türü** - Satış siparişleri

1. **Mobil aygıt menü öğeleri** Eylem bölmesinde, **sistem yönlendirilmiş iş sırası sorgularını** seçin ve yeni sistemle yönlendirilen bir çalışma sırası sorgusu belirtmek için şu adımları izleyin:
    - Eylem bölmesinde, **Yeni**'yi seçin.
    - **Sıra numarası** - 1
    - **Açıklama** - çalışma önceliği – Iş kodu

1. Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.
1. **Sıralama** sekmesini seçin.
1. Yeni satır eklemek için **Ekle**'yi seçin ve sonra aşağıdakileri girin:
    - **Tablo** - İş
    - **Türetilen tablo** - İş
    - **Alan** - iş önceliği
    - **Arama yönü** - Azalan
1. İkinci satır eklemek için **Ekle**'yi seçin ve sonra aşağıdakileri girin:
    - **Tablo** - İş
    - **Türetilen tablo** - İş
    - **Alan** - iş kimliği
    - **Arama yönü** - Azalan

1. Sistem şimdi kümedeki iş kimliklerini, öncelikle iş önceliğine ve sonra iş koduna göre sıralayacak.

### <a name="set-up-a-mobile-device-menu"></a>Mobil cihaz menüsü ayarlama

1. **Ambar yönetimi > Kurulum > Mobil cihaz > Mobil cihaz menüsü** öğesine gidin.
1. Mobil cihaz menüsüne oluşturmuş olduğunuz **SD Kümesi** menü öğesi ekleyin.
1. **Giden** menüsünü seçin.
1. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
1. **SD kümesini** buluncaya kadar ilerleyin.
1. **SD küme**'yi seçtiğinizde, **menü yapısı** listesine işaret eden ok etkinleştirilir.
1. **SD küme** menü öğesini **giden** menü yapısına taşımak için **ok** düğmesini seçin.
1. **Menü yapısı** listesinden **SD küme**'yi seçin ve sonra menü öğesini mobil aygıt menüsünde istediğiniz konuma taşımak için **yukarı** veya **aşağı** okları seçin.

## <a name="scenario"></a>Senaryo

### <a name="create-picking-work"></a>Malzeme çekme işi oluştur

Sistemin yönettiği küme çekmeyi ayarlamadan önce, uygun bazı giden işler oluşturmanız gerekir. Daha önce oluşturduğunuz küme profilinde iki küme konumu belirtilir. Bu nedenle, en az iki iş kodu oluşturmanız gerekir. Bu senaryoda, iki satış siparişi oluşturulur, stok rezerve edin, satış siparişlerini ambara serbest bırakın ve sonra da dalgaya el ile işlem yapın.

1. **Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri** menüsüne gidin.
1. İlk satış siparişini oluşturmak Için eylem bölmesinde **yeni** 'yi seçin.
    - **Satış siparişi oluştur** menüsü açılırsa, aşağıdaki bilgileri girin:
        - **Müşteri** hızlı sekmesinde, **müşteri hesabı** - **ABD-004** girin.
        - **Genel** hızlı sekmesinde, **ambar** - **62**'yi girin.
        - Menüyü kapatmak için **Tamam**'ı seçin ve satış siparişini oluşturun.
    - **Satış siparişi satırları** hızlı sekmesinde, Yeni bir satır otomatik olarak eklenmemişse **satır ekle**'yi seçin ve aşağıdakileri girin:
        - **Madde numarası** - A0001
        - **Miktar** - 1
        - İkinci bir satır eklemek için **satır ekle**'yi seçin.
        - **Madde numarası** - A0002
        - **Miktar** - 3
    - Az önce oluşturduğunuz satırların her ikisi için stok rezerve edin.
        - **Satır 1**'i seçin.
        - **Satış siparişi satırları** Eylem Bölmesi'nde **Envanter**'i seçin ve ardından listeden **Rezervasyonu** seçin.
        - **Rezervasyon** formunda envanteri rezerve etmek için **lotu rezerve et**'i seçin.
        - **Rezervasyon** tamamlandığında rezervasyon formunu kapatın.
        - **Satır 2** için stok rezerve etmek için bu adımları yineleyin.
1. İkinci satış siparişini oluşturmak Için eylem bölmesinde **yeni** 'yi seçin.
    - **Satış siparişi oluştur** menüsü açılırsa, aşağıdaki bilgileri girin:
        - **Müşteri** hızlı sekmesinde, **müşteri hesabı** - **ABD-005** girin.
        - **Genel** hızlı sekmesinde, **ambar** - **62**'yi girin.
        - Menüyü kapatmak için **Tamam**'ı seçin ve satış siparişini oluşturun
    - **Satış siparişi satırları** hızlı sekmesinde, Yeni bir satır otomatik olarak eklenmemişse **satır ekle**'yi seçin ve aşağıdakileri girin:
        - **Madde numarası** - A0001
        - **Miktar** - 4
        - İkinci bir satır eklemek için **satır ekle**'yi seçin.
        - **Madde numarası** - A0002
        - **Miktar** - 2
    - Az önce oluşturduğunuz satırların her ikisi için stok rezerve edin.
        - **Satır 1**'i seçin.
        - **Satış siparişi satırları** Eylem Bölmesi'nde **Envanter**'i seçin ve ardından listeden **Rezervasyonu** seçin.
        - **Rezervasyon** formunda envanteri rezerve etmek için **lotu rezerve et**'i seçin.
        - **Rezervasyon** tamamlandığında rezervasyon formunu kapatın.
        - **Satır 2** için stok rezerve etmek için bu adımları yineleyin.
    - Satış siparişini kapatın ve **Tüm satış siparişleri** liste sayfasına geri dönün.
1. Yeni oluşturduğunuz iki satış siparişini bulun (sayfayı yenilemeniz gerekebilir). Tabloda, her iki satış siparişini de bölüm onay işaretini kullanarak seçin.
    - **Tüm satış siparişleri** eylemi bölmesinde, **Ambar** sekmesini seçin.
    - **Eylemler** grubunda, her iki satış siparişini ambara serbest bırakmak için **ambarı serbest bırak** 'ı seçin.
1. Ambar bırakma işlemi tamamlandığında, bir bilgi iletisi görüntülenir.
    - Her satış siparişi için sevkiyatlar oluşturulur.
    - Bir dalga oluşturulur ve her iki sevkiyat da dalgaya atanır. **Dalga kodunu** not edin.
1. **Ambar yönetimi > Giden dalgalar > Sevkiyat dalgaları > Tüm dalgalar**'a gidin.
    - **Tüm dalgalar** listesinde , önceki adımda oluşturduğunuz **dalga kimliğini** bulun ve seçin.
    - Eylem panosunda **Dalga** sekmesini seçin.
    - **Dalga** grubunda, dalgayı işlemek ve **iş** oluşturmak için **işle**'yi seçin.
    - İşlem tamamlandığında, işin oluşturulduğunu ve dalgasının deftere nakledildiğini gösteren bilgi iletileri oluşturulur.
1. **İsteğe bağlı**: oluşturulan işi görüntülemek için **Ambar yönetimi > iş > iş ayrıntıları**'na gidin. İki farklı iş kimliği oluşturulur. Her iş kodunun iki çekme satırı vardır.

### <a name="run-the-mobile-device-flow"></a>Mobil cihaz akışı çalıştır

1. Ambar **62**'deki bir kullanıcının mobil aygıtında oturum açın.
1. **Ana menüde** **gidiş**'i seçin.
1. **Gidiş** menüsünde çekmeyi başlatmak için **SD kümesini** seçin.
    - Bir küme oluşturulur ve daha önce oluşturduğunuz iki iş kodu buna bağlıdır. İkiden fazla iş kodu oluşturduysanız, kümeye yalnızca ilk ikisi eklenir. İş kimliklerinin, sorgu kurulumunda belirtildiği gibi, artan sırada kümeye eklendiğini unutmayın.

    > [!NOTE]
    > Yeni küme yalnızca, daha önce yeterli ek iş kodu oluşturulmuşsa otomatik olarak oluşturulur. Aksi durumda, aşağıdaki ileti görüntülenir: "Küme için yeterli iş bulunamadı."

    - Menüyü seçtikten sonra, ilk seçim ekranı görüntülenir. Sistem, tüm eşleşen çekme satırlarını iki iş kimliğiyle toplar ve tek bir çekme kullanarak her iki siparişi karşılayabilmek için bir kez çekme konumunu ziyaret etmeniz için size yönlendirir. Bu işlem, Kullanıcı tarafından yönlendirilen küme çekme işlemiyle aynı şekilde gerçekleştirilir.

1. **Tamam**'ı seçerek, ilk malzeme çekme yerleşimini ve maddesini onaylayın.
    - Çekme miktarı, kümedeki satış siparişlerinde görüntülenen maddenin toplamı olacaktır.
1. Pozisyon için çekilen madde miktarının doğru pozisyona koyulacağını onaylamak için pozisyon adını (sayısal veya alfabetik) girin.
1. Tüm madde miktarları çekilene ve doğru pozisyona koyuluncaya kadar bu süreci tekrarlayın.
1. Mobil cihazdaki son adım, kümeyi son konuma **koymada** kullanılır. **Tamam**'ı seçin
    - Bu Yerine koyma işlemi teyit edildiğinde, küme profilindeki **küme sonu** alanında ayarladığınız değere göre küme kapanır ve kesilir. İş kimlikleri de kapatılmıştır.
1. Mobil cihazda "küme tamamlandı" iletisi gösterilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]