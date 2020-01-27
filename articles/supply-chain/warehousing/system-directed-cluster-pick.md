---
title: Sistem tarafından yönlendirilen küme malzeme çekme
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta sistemle yönlendirilen küme çekmeye genel bir bakış sağlar.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c3b23a5d3b77bae89e4845bdff4ab20f95c46497
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917868"
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

Yeni bir mobil cihaz menü öğesi, sistem tarafından yönlendirilmiş küme çekme işlemi için kullanılır. **Yönlendirilmiş** seçeneği için küme profili kimliği belirtilmelidir. Ek olarak, sistem tarafından yönlendirilen sorgu sırası, şirkete özel ölçütlere göre siparişleri gruplandırabilir. Bu nedenle, sistem yönlendirilmiş sorgu sırasında özelleştirilmiş Sıralama ölçütleri belirleyerek, iş siparişlerinin atanmasını daha da iyi duruma getirebilirsiniz.

Sisteme yönlendirilmiş küme çekme işlemi yapıldığında, ambar çalışanları malzeme çekme emirlerinin küme konumlarına yeniden atanmış olduğu bir kümeyle sunulur. Bu nedenle, çalışanlar çekme konumunu yalnızca bir kez ziyaret ederek çoklu iş emirleri için bir madde çekebilirsiniz. Sistemle yönlendirilen küme çekme işlemi için malzeme çekme süreci, Kullanıcı tarafından yönlendirilen küme çekme işlemiyle aynıdır.

## <a name="set-up-system-directed-cluster-picking"></a>Sistem tarafından yönlendirilen küme malzeme çekme ayarlama

### <a name="create-cluster-profiles"></a>Küme profilleri oluşturma

Küme profilleri, sistemin her kümeyi nasıl oluşturduğunu denetler. Farklı kümeler gerekiyorsa, her mobil cihaz menü öğesi için farklı bir küme profili oluşturulmalıdır.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Küme profilleri**'ne tıklayın.
2. **Yeni**'yi seçin.
3. **Küme profil kodu** alanına **2 pozisyon** girin.
4. **Ad** alanına, **Pozisyon 2** yazın.
5. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Küme kimliği oluştur:** bu seçeneği **Evet** olarak ayarlayın. Bu seçenek, küme kimliğinin sistem tarafından otomatik olarak oluşturulup oluşturulmayacağını veya kullanıcının çekme başlangıcında bunu oluşturup oluşturmayacağını belirler.
    - **Pozisyonları etkinleştir:** Bu seçeneği **Evet** olarak ayarlayın. Bu seçenek pozisyon adlarının ayar adına göre otomatik olarak oluşturulup oluşturulmayacağını belirler. Bu seçenek **Hayır** olarak ayarlıysa değilse konum için plaka kimliği kullanılır.
    - **Pozisyon sayısı:** **2** girin. Bu alan, kümede olabilecek maksimum pozisyon sayısını (yani kutu, sepetler vs. sayısı) belirler.
    - **Konum adı:** sayısalların sürekli numaralar kullanılarak adlandırılmaları için **sayısal**'i seçin. **Alfabetik**'ı seçerseniz, pozisyonlar alfabetik düzende adlandırılır.
    - **Kümeyi kesme zamanı:** **Yerine koy** seçeneğini belirleyin. Bu alan kümenin ne zaman kesildiğini belirler.
    - **Sıralama doğrulama türü:** **konum taramayı** seç. Bu alan, yerine koyma adımının doğrulanıp doğrulanmayacağını belirler.

6. **Küme sıralama** hızlı sekmesinde, yeni bir satır oluşturup aşağıdaki alanları ayarlayarak sıralama ölçütü tanımlayabilirsiniz:

    - **Sıra numarası:** Bu alan, sistemin sıralama yaptığı sırayı belirler. Otomatik olarak bir değer girilir, ancak bunu gereksinim duyduğunuz gibi değiştirebilirsiniz.
    - **Alan adı:** **WMSLocationId**'i seçin. Bu alan, satırla ilgili sıralama ölçütü için kullanılan alanı belirler.
    - **Sıralama:** **artan**'ı seçin. Bu alan, sıralamanın artan veya azalan sırada yapılıp yapılmadığını tanımlar.

### <a name="create-a-mobile-device-menu-item"></a>Mobil cihaz menü öğesi oluşturma

Sisteme yönlendirilmiş kümenin çekilmesi için yeni bir mobil cihaz menü öğesi oluşturmak ve küme profil kimliğini mobil cihaz menü öğesine bağlamak için aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.
2. **Yeni**'yi seçin.
3. **Menü öğesi adı** alanında, **SD kümesi** girin.
4. **Başlık** alanına **SD kümesi** girin.
5. **Mod** alanında, **İş**'i seçin.
6. **Mevcut işi kullan** seçeneğinde **Evet**'i işaretleyin.
7. **Genel** hızlı sekmesinde, aşağıdaki alanları ayarlayın:

    - **Yöneten:** **Sistem tarafından yönetilen**'i seçin.
    - **Lisans kalıbı oluştur:** Bu seçeneğini **Evet** olarak ayarlayın.
    - **Küme profili kimliği:** **konum 2**'yi seçin.

8. **İş sınıfları** hızlı sekmesinde, mobil aygıt menü öğesi için geçerli iş sınıflarını konfigüre etmek üzere aşağıdaki adımları izleyin:

    - **İş sınıfı kimliği:** **satışların** girildiğinden emin olun.
    - **İş emri türü:** **satış siparişleri** girildiğinden emin olun.

9. Sistem tarafından yönlendirilen yeni bir iş sırası sorgusu belirtmek için aşağıdaki adımları izleyin:

    1. **Yeni**'yi seçin.
    2. **Sıra numarası** alanına **1** girin.
    3. **Açıklama** alanında, **İş önceliği – iş kodu** seçin.

10. Menüde, **Düzenle sorgu** seçeneğini belirleyin.
11. **Sınıflandırma** sekmesinde, aşağıdaki alanları ayarlayın:

    - **Tablo:** **İş**'i seçin.
    - **Türetilen tablo:** **İş**'i seçin.
    - **Alan:** **iş önceliğini** seçin.
    - **Arama yönü:** **Azalan**'ı seçin.
    - **Tablo:** **İş**'i seçin.
    - **Türetilen tablo:** **İş**'i seçin.
    - **Alan:** **iş kimliği** seçin.
    - **Arama yönü:** **Azalan**'ı seçin.

Sistem şimdi kümedeki iş kimliklerini, öncelikle iş önceliğine ve sonra iş koduna göre sıralayacak.

### <a name="set-up-a-mobile-device-menu"></a>Mobil cihaz menüsü ayarlama

1. **Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.
2. Yeni oluşturduğunuz menü öğesini istenen menüye ekleyin.

## <a name="example"></a>Örnek

### <a name="create-picking-work"></a>Malzeme çekme işi oluştur

Sistemin yönettiği küme çekmeyi ayarlamadan önce, uygun bazı giden işler oluşturmanız gerekir. Daha önce oluşturduğunuz küme profilinde iki küme konumu belirtilir. Bu nedenle, en az iki iş kodu oluşturmanız gerekir.

1. **Satış ve Pazarlama \> Satış siparişleri \> Tüm satış siparişleri**'ne gidin.
2. Satış siparişi oluşturmak için **Yeni**'yi seçin.
3. **Müşteri hesabı** alanından bir AB müşterisini seçin.
4. **Genel** hızlı sekmesinde, **ambar** alanında, ambar **62**'i seçin.
5. **Tamam**'ı seçin.
6. **Satış siparişleri satırları** hızlı sekmesinde **Satır ekle**'yi seçin.
7. **Öğe numarası** alanında, **A0001**'yi seçin.
8. **Miktar** alanına **1** yazın.
9. İkinci bir satır eklemek için **satır ekle**'yi seçin.
10. **Öğe numarası** alanında, **A0002**'yi seçin.
11. **Miktar** alanına **3** yazın.
12. 2 ile 6 arasındaki adımları yineleyin.
13. **Öğe numarası** alanında, **A0001**'yi seçin.
14. **Miktar** alanına **4** yazın.
15. İkinci bir satır eklemek için **satır ekle**'yi seçin.
16. **Öğe numarası** alanında, **A0002**'yi seçin.
17. **Miktar** alanına **2** yazın.

Stoku rezerve edin ve ambara serbest bırakın. İki farklı iş kimliği oluşturulur. Her iş kodunun iki çekme satırı vardır.

### <a name="run-the-mobile-device-flow"></a>Mobil cihaz akışı çalıştır

1. Mobil cihazda, yeni mobil aygıt menü öğesini içeren menüyü seçin.
2. **SD küme** menü öğesini seçin ve çekmeyi başlatın. Bir küme oluşturulur ve daha önce oluşturduğunuz iki iş kodu buna bağlıdır. İkiden fazla iş kodu oluşturduysanız, kümeye yalnızca ilk ikisi eklenir. İş kimliklerinin, sorgu kurulumunda belirtildiği gibi, artan sırada kümeye eklendiğini unutmayın.

    > [!NOTE]
    > Yeni küme yalnızca, daha önce yeterli ek iş kodu oluşturulmuşsa otomatik olarak oluşturulur. Aksi durumda, aşağıdaki ileti görüntülenir: "Küme için yeterli iş bulunamadı."

    Menüyü seçtikten sonra, ilk seçim ekranı görüntülenir. Sistem, tüm eşleşen çekme satırlarını iki iş kimliğiyle toplar ve tek bir çekme kullanarak her iki siparişi karşılayabilmek için bir kez çekme konumunu ziyaret etmeniz için size yönlendirir. Bu işlem, Kullanıcı tarafından yönlendirilen küme çekme işlemiyle aynı şekilde gerçekleştirilir.

3. İlk çekmeyi onaylayın. Daha sonra, maddelerin doğru pozisyona koyulduğu onaylanacak şekilde pozisyon adını girmeniz gerekir.
4. Tüm maddeler çekilene ve doğru pozisyona koyuluncaya kadar bu süreci tekrarlayın.
5. Mobil cihazdaki son adım, kümeyi son konuma koymada kullanılır. Bu Yerine koyma işlemi teyit edildiğinde, küme profilindeki **küme sonu** alanında ayarladığınız değere göre küme kapanır ve kesilir. İş kimlikleri de kapatılmıştır.
6. Mobil cihazda "küme tamamlandı" iletisi gösterilir.
