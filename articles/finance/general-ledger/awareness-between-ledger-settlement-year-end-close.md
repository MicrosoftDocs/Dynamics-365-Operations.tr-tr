---
title: Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık
description: Bu konu, genel muhasebe kapatmalarını ve Genel muhasebe yıl sonu kapanışını etkileyen geliştirmeler hakkında bilgi sağlar.
author: kweekley
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: e18f77d73239de23000b5310d9342c6db95bc524
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462366"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık

[!include [banner](../includes/banner.md)]


Microsoft Dynamics 365 Finance sürüm 10.0.25'te, **Özellik yönetimi** çalışma alanında **genel muhasebe kapatma ve yıl sonu kapatma özelliği arasındaki farklar** kullanıma sunuldu. Bu özellik, genel muhasebe kapatma ve genel muhasebe yıl sonu kapanışı etkileyen iki birincil geliştirme ekler.

Genel muhasebe yıl sonu kapanışı sırasında, kapatılan genel muhasebe hareketleri artık bir sonraki mali yılın açılış bakiyesine dahil edilmez. Bu geliştirme, açılış bakiyesine yalnızca dengesiz genel muhasebe hareketlerinin dahil olmasını sağlar. Genel muhasebe yabancı para birimi yeniden değerlemesi çalıştırıldığında önemlidir. Yabancı para birimi yeniden değerlemesi yalnızca **Kapatılmadı** durumundaki genel muhasebe hareketleri için çalıştırılır. Ancak, **Genel muhasebe kapatması ile yıl sonu kapanışı arasındaki farkındalık** özelliği serbest bırakılmadan önce, açılış bakiyesi hem **Kapatıldı** durumundaki hareketleri hem de **Kapatılmadı** durumunda olan hareketleri özetliyordu ve özetlenen tutarın durumu **Kapatıldı** olarak ayarlanıyordu.

İkinci geliştirme, genel muhasebe yıl sonu kapanışı sırasında ayrıntılı açılış bakiyesi hareketlerini deftere nakletmenizi sağlar. **Yıl sonu kapanışı sırasında ayrıntıyı koru** seçeneği **Evet** olarak ayarlanırsa, kapatılmamış her genel muhasebe hareketi için ayrı bir açılış bakiyesi oluşturulur. Bu ayar, genel muhasebe kapatma kurulumundaki her ana hesap için tanımlanır. Açılış bakiyesi için ayrıntılı hareketleri tutarak, bir sonraki mali yılda düzeltilmemiş genel muhasebe hareketlerini kapatma özelliğini büyük ölçüde geliştirirsiniz.

Yeni geliştirmeleri desteklemek için genel muhasebe kapatma ve yıl sonu kapanışı değişiklikleri yapıldı.

### <a name="changes-to-ledger-settlement"></a>Genel muhasebe kapatması değişiklikleri

- Genel muhasebe kapatması bir mali yıl içinde yapılmalıdır.
- Tek bir ana hesaptaki hareketler için genel muhasebe kapatması yapılmalıdır. Ana hesap artık **Genel Muhasebe kapatması** sayfasında gerekli bir filtredir.
- Genel muhasebe kapatması ve genel muhasebe kapatmasının tersine çevrilmesi, kapatılan bir mali yıl içinde deftere nakledilen (başka bir deyişle, yıl sonu kapanışı çalıştırılmıştır) hareketler için yapılamaz.

### <a name="changes-to-year-end-close"></a>Yıl sonu kapanışı değişiklikleri

- Bir sonraki mali yılda herhangi bir açılış bakiyesi hareketi kapatılmışsa, yıl sonu kapanışı geri alınamaz. Bu değişiklik, yıl sonu kapanışı tersine çevrildiğinde veya yıl sonu kapanışı yeniden çalıştırıldığında ve Genel muhasebe parametrelerinde **Yıl sonu girişlerini sil** seçeneği **Evet** olarak ayarlandığında geçerlidir.
- Genel muhasebe kapatmasındaki herhangi bir bilanço hesabı için **Yıl sonu kapanışı sırasında ayrıntıyı koru** seçeneği **Evet** olarak ayarlanmışsa bu ana hesap için daha ayrıntılı açılış bakiyesi hareketleri oluşturulur.

## <a name="before-you-enable-the-feature"></a>Özelliği etkinleştirmeden önce

İşlevsellik ve veri modellerindeki değişiklikler nedeniyle, özelliği etkinleştirmeden önce aşağıdaki noktaları göz önünde bulundurmanız önemlidir:

- Kapatma için işaretlenmiş ancak kapatılmamış tüm hareketlerin, özellik etkinleştirildiğinde otomatik olarak işareti kaldırılır. Herhangi bir iş kaybını önlemek için özelliği etkinleştirmeden önce tüm işaretli hareketleri kapatın.
- Bazı kuruluşlar, aynı mali yıl için birden çok kez yıl sonu kapanışı yapar. Yıl sonu kapanışı zaten bir kez çalıştırıldıysa ve aynı mali yıl için yeniden çalıştırılacaksa özelliği etkinleştirmeyin. Özellik, ilk yıl sonu kapanışını işlemeden önce veya mali yıl için son yıl sonu kapanışını işledikten sonra etkinleştirilmelidir.

  Özelliği etkinleştirmek istiyorsanız ancak yıl sonu kapanışı zaten bir kez çalıştırıldıysa, özelliği etkinleştirmeden önce yıl sonu kapanışını tersine çevirmeniz gerekir.

- Mali yıllar arasında anlaşmaya artık izin verilmediğinden, yıl sonu kapatma işlemine başlamadan önce özelliği etkinleştirmenizi öneririz. Ardından, bir sonraki mali yılın açılış bakiyelerinin önceki mali yıllar arası kapatmalardan etkilenmemesini sağlamak amacıyla kapatılmakta olan mali yıl için açılış bakiyesi hareketi kapatılmalıdır.
- Ana hesaplar arasında kapatma işlemine artık izin verilmediğinden, genel muhasebe kapatmasının aynı ana hesapta yapılabilmesini sağlamak için hesap veya işlem planınızı gerektiği gibi ayarlayın.
- Kamu sektörü yıl sonu kapanışı işlemi kullanılıyorsa özellik etkinleştirilemez.

## <a name="set-up-ledger-settlement"></a>Genel muhasebe kapatmasını ayarlama

Özelliği etkinleştirdikten sonra ve bir sonraki yıl sonu kapanışını çalıştırmadan önce, her kuruluşun yıl sonu kapanışı sırasında hareket ayrıntılarını tutup tutmayacağını belirlemesi gerekir. Seçimin, önceki yıl sonu kapanış süreçlerinden bakiye deftere nakillerinin açılması üzerinde hiçbir etkisi yoktur.

**Genel muhasebe kapatma kurulumu** sayfasındaki her ana hesap için **Yıl sonu kapanışı sırasında ayrıntıyı koru** seçeneği ayarlanır.

1.  **Genel muhasebe** > **Genel muhasebe ayarı** > **Genel muhasebe parametreleri**'ne gidin.
2.  **Genel muhasebe kapatmaları** sekmesinde **Genel muhasebe kapatma hesapları**'nı seçin.

-veya-

1.  **Genel muhasebe** > **Periyodik görevler** > **Genel muhasebe hesabı kapatmaları**'na gidin.
2.  **Genel muhasebe kapatma hesapları**'nı seçin.

**Genel muhasebe kapatmaları** sayfasına iki sütun eklenmiştir:
    
- **Ana hesap türü** – Bu sütun yalnızca bilgilendirme amaçlıdır. Ana hesaba atanan türü gösterir.
- **Yıl sonu kapanışı sırasında ayrıntıyı koru** – Varsayılan olarak, seçenek **Hayır** olarak ayarlanır. Yalnızca **Ana hesap türü** sütunundaki değer **Bilanço**, **Varlık** veya **Borç** ise **Evet** olarak ayarlanabilir. Seçenek **Hayır** olarak ayarlandığında, açılış bakiyeleri yıl sonu kapanışlarında olduğu gibi özet olarak deftere nakledilir. **Evet** olarak ayarlanırsa açılış bakiyeleri ana hesap için kapatılmamış her genel muhasebe hareketi için ayrıntılı olarak oluşturulur.

## <a name="year-end-close"></a>Yıl sonu kapanışı

**Genel muhasebe** > **Dönem kapanışı** > **Yıl sonu kapanışı**'na giderek yıl sonu kapanışını çalıştırdığınızda, işlem genel muhasebe kapatma için tanımlanan ana hesaplar için açılış bakiyelerini oluşturur. Açılış bakiyeleri, genel muhasebe kapatma kurulumuna bağlı olarak özet veya ayrıntı olarak oluşturulur. İşlem, her ana hesabın açılış bakiyesini özet olarak mı yoksa ayrıntılı olarak mı deftere naklettiğinize bakılmaksızın kapatılan genel muhasebe hareketlerini hariç tutar.

Örneğin, 2021 mali yılında 130100 ana hesabına birden çok hareket nakledilmiştir.

| Günlük numarası | Fiş  | Tarih       | Tür      | Genel muhasebe hesabı | Hesap adı        | Açıklama       | Para Birimi | Hareket para birimi cinsinden tutar | Tutar  | Raporlama para birimi cinsinden tutar |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 03.12.2021  | İşletim | 130100-001-    | Alacak hesapları | Servis ücreti       | ABD Doları      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 05.12.2021  | İşletim | 130100-002-    | Alacak hesapları | Faturalar         | ABD Doları      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 16.12.2021 | İşletim | 130100-001-    | Alacak hesapları | Geri ödeme            | ABD Doları      | -100                           | -100    | -100                         |
| 20851          | ARP-8000 | 20.12.2021 | İşletim | 130100-002-    | Alacak hesapları |                   | ABD Doları      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | İşletim | 130100-002-    | Alacak hesapları |                   | EUR      | -127,11                        | -174,12 | -174,12                      |
| 20856          | CMV-4010 | 21.12.2021 | İşletim | 130100-002-    | Alacak hesapları | Hesaptaki alacak | ABD Doları      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 28.12.2021 | İşletim | 130100-001-    | Alacak hesapları | Faturalar         | ABD Doları      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 29.12.2021 | İşletim | 130100-002-    | Alacak hesapları | Servis           | ABD Doları      | 300                            | 300     | 300                          |

Bu hareketlerden üçü genel muhasebe kapatması sırasında kapatılır.

175 ABD doları (175 USD) tutarında bir fatura vardır. Bu fatura euro (EUR) cinsinden bir ödeme ile ödendi ve nakit indirimi alındı.

| Günlük numarası | Fiş  | Tarih       | Tür      | Genel muhasebe hesabı | Hesap adı        | Açıklama | Para Birimi | Hareket para birimi cinsinden tutar | Tutar  | Raporlama para birimi cinsinden tutar |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 05.12.2021  | İşletim | 130100-002-    | Alacak hesapları | Faturalar   | ABD Doları      | 175                            | 175     | 175                          |
| 20851          | ARP-8000 | 20.12.2021 | İşletim | 130100-002-    | Alacak hesapları |             | ABD Doları      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | İşletim | 130100-002-    | Alacak hesapları |             | EUR      | -127,11                        | -174,12 | -174,12                      |

130100 ana hesabının sonuçları, yıl sonu kapanışı çalıştırılmadan önce özelliğin etkinleştirilip etkinleştirilmediğine bağlıdır. Özellik etkinleştirilmişse sonuç Yıl sonu kapanışı sırasında ayrıntıyı koru seçeneğinin ayarına da bağlıdır.

### <a name="the-feature-isnt-enabled"></a>Özellik etkin değil
Yıl sonu kapanışı, 2022'de 130100 ana hesabı için üç açılış bakiyesi hareketi oluşturur. Muhasebe para birimi cinsinden işlemlerin toplamı 525 ABD dolarıdır.

| Günlük numarası | Fiş  | Tarih     | Tür    | Genel muhasebe hesabı | Hesap adı        | Açıklama | Para Birimi | Hareket para birimi cinsinden tutar | Tutar  | Raporlama para birimi cinsinden tutar |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-002-    | Alacak hesapları |             | ABD Doları      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-001-    | Alacak hesapları |             | ABD Doları      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-002-    | Alacak hesapları |             | EUR      | -127,11                        | -174,12 | -174,12                      |

Ödemenin -127,11 EUR'lik hareketi deftere nakledilmiş olsa da, işlem yine de başlangıç bakiyesi olarak öne çıkar.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Özellik etkin ve Yıl sonu kapanışı sırasında ayrıntıyı koru = Hayır

Yıl sonu kapanışı, 2022'de 130100 ana hesabı için iki açılış bakiyesi hareketi oluşturur. Muhasebe para birimindeki hareketlerin toplamı hala 525 ABD dolarıdır ancak genel muhasebe tarafından kapatılan hareketler açılış bakiyesinin dışında tutulur. 130100-002- hesabı için toplam tutar 299,12 ABD doları yerine 125 ABD dolarıdır ve 127,11 ABD doları/174,12 ABD doları tutarındaki işlem tamamen hariçtir.

| Günlük numarası | Fiş  | Tarih     | Tür    | Genel muhasebe hesabı | Hesap adı        | Açıklama | Para Birimi | Hareket para birimi cinsinden tutar | Tutar | Raporlama para birimi cinsinden tutar |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-002-    | Alacak hesapları |             | ABD Doları      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-001-    | Alacak hesapları |             | ABD Doları      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Özellik etkin ve Yıl sonu kapanışı sırasında ayrıntıyı koru = Evet

Yıl sonu kapanışı, 2022'de 130100 ana hesabı için beş açılış bakiyesi hareketi oluşturur. Kapatılmamış beş hareketin her biri için ayrı bir açılış bakiyesi hareketi oluşturulur. Muhasebe para birimi cinsinden işlemlerin toplamı hala 525 ABD dolarıdır.

| Günlük numarası | Fiş  | Tarih     | Tür    | Genel muhasebe hesabı | Hesap adı        | Açıklama       | Para Birimi | Hareket para birimi cinsinden tutar | Tutar | Raporlama para birimi cinsinden tutar |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-001-    | Alacak hesapları | Servis ücreti       | ABD Doları      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-001-    | Alacak hesapları | Geri ödeme            | ABD Doları      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-002-    | Alacak hesapları | Hesaptaki alacak | ABD Doları      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-001-    | Alacak hesapları | Faturalar         | ABD Doları      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 01.01.2022 | Açılış | 130100-002-    | Alacak hesapları | Servis           | ABD Doları      | 300                            | 300    | 300                          |

İşlem ayrıntıları tutulduğunda, orijinal ayrıntılı hareketler etkilenmez. Bunlar, kapatılmakta olan mali yılda deftere nakledilmiş ve kapatılmamış olarak kalır. Açılış bakiyesi için bu hareketlerin bir kopyası oluşturulur. Orijinal hareketlerden aşağıdaki değerler açılış bakiyesi hareketlerine kopyalanır.

- Genel muhasebe hesabı (ana hesap ve tüm mali boyutlar)
- Hareket, muhasebe ve raporlama para birimlerindeki tutarlar
- Açıklama
- Deftere nakil katmanı
- Deftere nakil türü

   > [!NOTE]
   > Başka hiçbir açılış bakiyesi hareketine deftere nakil türü atanmaz. Bu nedenle, deftere nakil türü ayrıntılı olarak öne çıkarılan açılış hareketlerini ayırt etmek için kullanılabilir.

Açılış bakiyesi ayrıntılı hareketlerinde orijinal hareketlerdeki bazı alanların değişmesi gerekir. Bakiye hareketlerinin açılış tarihi her zaman bir sonraki mali yılın ilk günüdür. Yevmiye defteri numarası değişmelidir ve fiş numarası yıl sonu kapanışı iletişim kutusuna girilen değere dönüşür.

Orijinal hareketlerden gelen bilgileri **Genel muhasebe kapatması** sayfasında bulabilirsiniz. Her ayrıntılı açılış bakiyesi hareketi, kılavuzdaki **Orijinal hareket tarihi** sütununu gösterir. Bu sütun, yeni mali yıldaki hareketleri eşleştirmenize yardımcı olabilir. Orijinal fişin tamamına geri dönmek için **Orijinal fişi görüntüle**'yi seçebilirsiniz.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Hareketleri kapat
Genel muhasebe hareketlerini kapatmak için bu adımları izleyin.

1. **Genel muhasebe** > **Periyodik görevler** > **Genel muhasebe hesabı kapatmaları**'na gidin.
2.  Sayfanın üst kısmında filtreleri ayarlayın.

    1. Tarih aralığı seçin. Alternatif olarak, tarih aralığını otomatik olarak doldurmak için bir tarih aralığı kodu seçin.

       - Tarih aralığı mali yılları geçemez. Tarih aralığı mali yılları geçerse **Hareketleri görüntüle**'yi seçtiğinizde hiçbir hareket gösterilmez.
       - Tarih aralığı açık bir mali yıldaysa hareketler kapatılabilir ve kapatma tersine çevrilebilir. Tarih aralığı kapalı bir mali yıldaysa veya yıl sonu kapanışı tamamlandıysa hareketler gösterilir ancak kapatılamaz veya kapanışı açılamaz. Hareketlerin işaretini yalnızca kapalı bir mali yılda kaldırabilirsiniz. Tarih aralığı kapalı bir mali yıldaysa, **İşaretlileri seç**, **İşaretli hareketleri kapat** ve **İşaretli hareketleri ters çevir** düğmeleri kullanılamaz.

    2. Hareketleri gösterilecek ana hesabı seçin. Bu alan gereklidir. Arama, yalnızca şirketin hesap planı için **Genel muhasebe kapatması** sayfasında seçilen ana hesapları gösterir.
    3. Deftere nakil katmanını seçin. Farklı deftere nakil katmanlarındaki hareketleri kapatamazsınız.
    4. Ana hesabı ve boyutları ayrı sütunlarda göstermek için bir finansal boyut kümesi seçin.

3.  Ayarladığınız filtrelerle eşleşen tüm hareketleri göstermek için **Hareketleri görüntüle**'yi seçin. Filtreleri veya boyut kümelerini değiştirirseniz, yneiden **Hareketleri görüntüle**'yi seçmelisiniz.
4.  Kapatma için satırları seçin. Sayfanın üstündeki **Seçilen tutar** alanının değeri, seçilen satırlardaki toplam tutara göre artar veya azalır.
5.  Hareketleri seçmeyi tamamladıktan sonra **Seçilen olarak işaretle**'yi seçin. Seçili her hareket için **İşaretli** sütununda bir onay işareti görünür. Ayrıca, kılavuzun üstündeki **İşaretli tutar** alanının değeri, işaretli satırlardaki toplam tutara göre artar veya azalır.
6.  **İşaretli tutar** alanındaki değer **0** (sıfır) iken **İşaretlenmiş hareketleri kapat**'ı seçin.

    - Kısmi mutabakata izin verilmez. Örneğin, 100 ABD doları bir borç hareketini 90 ABD doları alacak hareketiyle kapatamazsınız. Kalan 10 ABD doları alacak işleminin de mutabakata dahil edilmek üzere işaretlenmiş olması gerekir.
    - Bir kapatma tarihi girin. Tarih, kapatma için işaretlenen hareketlerin en son tarihinde veya sonrasında olmalıdır.

İşaretli hareketlerin durumu **Kapatıldı** olarak değiştirilir.

> [!IMPORTANT]
> Etkin tüzel kişilik ve seçili ana hesap için kapatma için işaretlediğiniz tüm hareketler kapatılacaktır. Hareketlerin sayfada görünmesine gerek yoktur. Bir filtre nedeniyle gizlenseler bile kapatılacaklardır.

Bir hareketin tersine çevrilmesi gibi bazı işlemler, genel muhasebe hareketlerini otomatik olarak kapatır. Örneğin, bir ödeme ve fatura Alacak Hesapları'nda kapatılır ve kapatma bir kazanç/zarar oluşturur. Ödeme ve faturanın kapatması, Alacak hesapları genel muhasebe hesabı hareketleri gibi genel muhasebe hareketlerini kapatmaz. Ancak, alacak hesaplarında ödeme ve faturanın kapanmamış olması durumunda, Alacak hesapları kapatmasının tersine çevrilmesi sırasında deftere nakledilen ters muhasebe girişi, orijinal ve ters muhasebe girişlerinin genel muhasebeye nakledilmesine neden olur. **Genel muhasebe kapatması ile yıl sonu kapanışı arasındaki farklar** özelliği etkinleştirildiğinde, ters çevirme tarihi farklı bir mali yıldaysa, ters çevirmenin genel muhasebe kapatması otomatik olarak gerçekleşmez.

## <a name="use-excel-for-ledger-settlement"></a>Genel muhasebe kapatması için Excel'i kullanma

**Genel muhasebe kapatması** sayfasında gösterilen hareketler Excel'e dışarı aktarılabilir. Excel'de, kapatma için hangi hareketlerin işaretlenebileceğini belirlemek için hareketleri daha fazla filtreleyebilirsiniz.
Her iki Genel Muhasebe kapatma varlığı, yalnızca **Genel muhasebe kapatması** sayfasında seçili ana hesap için genel muhasebe hareketlerini dışarı aktarır. Kapatılan mali yıllara ait hareketler Excel kullanılarak işaretlenebilir veya işareti kaldırılabilir ancak bunlar kapatılamaz. Ayrıca, kapatılan hareketler bu mali yıl için tersine çevrilemez.

## <a name="make-transactions-easier-to-find"></a>Hareketleri bulmayı kolaylaştırın

**Genel muhasebe hesabı kapatmaları** sayfası, kapatmak için gereken hareketleri görüntülemenizi kolaylaştıran özellikler içerir.

•   **İşaretli** onay kutusunun seçili olup olmadığına bağlı olarak hareketleri filtrelemek için **İşaretli** filtresini kullanın.
•   Hareketleri durumlarına göre filtrelemek için **Durum** filtresini kullanın.
•   Tutarları mutlak değere göre sıralamak için **Mutlak tutara göre sırala**'yı seçin. Bu şekilde, aynı tutara sahip borç ve alacakları gruplayabilirsiniz.

## <a name="reverse-a-settlement"></a>Kapatmayı ters çevirin

Yanlışlıkla yapılan bir kapatmayı tersine çevirin.

1.  [Hareketleri kapatma](#settle-transactions) bölümündeki 1 ila 3 adımlarını izleyerek ilgilendiğiniz hareketleri gösterin.
2.  **Durum** filtresinde, **Kapatılmış**'ı seçin.
3.  Ters çevrilmesi için satırları seçin.
4.  **İşaretli hareketleri ters çevir**'i seçin. Aynı kapatma kimliğine sahip tüm hareketlerin durumu **Kapatılmadı** olarak güncelleştirilir.

> [!IMPORTANT]
> Aynı kapatma kimliğine sahip tüm hareketler işaretli olmasalar bile tersine çevrilir. Örneğin, dört satır işaretliydi ve kapatıldı. Dört satırın da kapatma kimliği aynıdır. Bu dört satırdan birini işaretler ve **işaretli hareketleri ters çevir**'i seçerseniz dört satır da ters çevrilir.






