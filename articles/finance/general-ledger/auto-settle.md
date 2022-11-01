---
title: Genel muhasebe kapatmalarını otomatikleştirme
description: Bu makalede Genel muhasebe kapatma işlemlerini otomatikleştirme hakkında bilgi sağlanmaktadır.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708340"
---
# <a name="automate-ledger-settlements"></a>Genel muhasebe kapatmalarını otomatikleştirme

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance sürüm 10.0.31'de, **Özellik yönetimi** çalışma alanında **Genel muhasebe kapatma işlemlerini otomatikleştirme** özelliği kullanıma sunuldu. **Genel muhasebe kapatma işlemlerini otomatikleştirme** özelliğini yalnızca **Genel muhasebe kapatma ile yıl sonu kapanışı arasındaki farka duyarlılık** özelliği etkinken etkinleştirebilirsiniz.

Genel muhasebe kapatması, genel muhasebedeki borç ve alacak hareketlerini eşleştirme işlemidir. Genel muhasebe kapatma faaliyetlerini yinelenen bir zamanlamada gerçekleştiren kuruluşlar artık işlemi otomatikleştirebilirler. Otomatik genel muhasebe kapatma işlemi sırasında borç hareketi ve alacak hareketi yalnızca muhasebe para birimindeki tutarları eşitse otomatik olarak eşleştirilebilir. Örneğin, 1,00 ABD Doları borç tutarı, 1,00 ABD Doları alacak tutarıyla otomatik olarak eşleştirilebilir. Ancak 1,00 ABD doları borç değeri, her biri 0,50 ABD doları değerinde olan iki alacakla otomatik olarak eşleştirilemez. Genel muhasebe hareketi tutarlarını kısmi eşleştirme desteklenmez.

Genel muhasebe kapatma otomasyonunda aşağıdaki ayrıntılar tanımlanır:

- Genel muhasebe kapatmaları çalıştırıldığında
- Otomatik olarak kapatılabilen borç ve alacakları eşleştirmek için hangi ölçütlerin kullanıldığı
- Genel muhasebe kapatma bilgilerinin hangi sırayla işlendiği

## <a name="define-the-occurrence-of-ledger-settlements"></a>Tekrarlanan genel muhasebe kapatmaları tanımlama

Genel muhasebe kapatma otomasyonunda Süreç otomasyonu çerçevesi kullanılır. Farklı iş süreçleri seçili bir işlemin tekrarlanma tanımlamak için bu çerçeveyi kullanır. Genel muhasebe kapatmaları için  **Sistem yönetimi \> Kurulum \> Süreç otomasyonları** veya **Genel muhasebe \> Genel muhasebe ayarı \> Süreç otomasyonları**'na gidin.

Önce **Yeni süreç otomasyonu oluştur** seçeneğini belirleyin ve **Genel muhasebe kapatmaları**'nı seçin. Sihirbaz daha sonra, otomasyonu ayarlama sürecinde size rehberlik eder.

## <a name="general-page"></a>Genel sayfa

Sihirbazın **Genel** sayfasında, oluşturduğunuz genel muhasebe kapatma tekrarının adını girin. Örneğin, eşleşen borçlarınız ve alacaklarınız Pazartesi günü genel muhasebe kapatma işlemine tabi tutuluyorsa **LedgerSettle\_Mon** gibi açıklayıcı bir ad girin. Girdiğiniz ad  **Genel muhasebe kapatmaları** sayfasındaki **Otomasyon kuralı** sütununda gösterilir.

Sayfadaki geri kalan ayarlar geneldir ve genel muhasebe kapatmalarının bu sürümü için tekrarlanma modelini tanımlar. Örneğin, bir tekrar Pazartesi günü içinse haftalık çalışacak şekilde tanımlayabilirsiniz ve çalıştığı zaman haftanın günü olarak Pazartesiyi seçebilirsiniz. Ayrıca, işlem otomasyonunun sonraki iş günü başlangıcından önce tamamlanacağı şekilde, 2:00 gibi erken bir planlama zamanı da girebilirsiniz. Süreç otomasyonunu normal çalışma saatlerinizin dışında gerçekleştirilecek şekilde zamanlamanızı öneririz. Bu şekilde iş günü boyunca muhasebe personeliniz üzerindeki baskının azaltılmasına yardımcı olursunuz.

 **Genel** sayfasındaki diğer alanlar hakkında daha fazla bilgi için işlem otomasyonu belgelerine bakın.

## <a name="ledger-settlements-match-criteria-page"></a>Genel muhasebe kapatmaları eşleştirme ölçütleri sayfası

Sihirbazda sonraki sayfa **Genel muhasebe kapatmaları eşleştirme ölçütleri** sayfasıdır. Süreç otomasyonu tekrarına dahil edilen ana hesapları ve eşleşen borç ve alacakları belirlemek için kullanılan ölçütleri tanımlar.

### <a name="account-selection"></a>Hesap seçimi

Tüzel kişilik için önceden genel muhasebe kapatma hesapları olarak tanımladığınız ana hesaplar gösterilir. (Ana hesapları **Genel muhasebe \> Genel muhasebe ayarı \> Genel muhasebe parametreleri \> Genel muhasebe kapatmaları** bölümünde genel muhasebe kapatma hesapları olarak tanımlarsınız.)

### <a name="main-account-and-posting-layer"></a>Ana hesap ve deftere nakil katmanı

 **Ana hesap** ve **Deftere nakil katmanı** değerleri, gerekli eşleştirme ölçütleridir. Otomatik genel muhasebe kapatma işlemi sırasında, genel muhasebe borç hareketi ve alacak hareketinin **Ana hesap** ve **Deftere nakil katmanı** değerlerinin eşleştirilebilmeleri için eşit olmaları gerekir.

### <a name="posting-type"></a>Deftere nakletme türü

Genel muhasebe borç ve alacak hareketlerinin otomatik genel muhasebe kapatma işlemi sırasında eşleştirilmesi için genel muhasebe borç ve alacak hareketlerinin aynı deftere nakil türüne sahip olması gerekiyorsa **Deftere nakil türü** seçeneğini belirleyin.

### <a name="financial-dimensions"></a>Mali boyutlar

Genel muhasebe borç ve alacak hareketlerinin otomatik genel muhasebe kapatma işlemi sırasında eşleştirilmesi için genel muhasebe borç ve alacak hareketlerinin aynı mali boyutlar sahip olması gerekiyorsa **Mali boyutlar** seçeneğini belirleyin. Bu seçenek belirlendiğinde **Kullanılabilir mali boyutlar** listesinde mali boyut değerleri için ölçütler seçilmelidir. **Kullanılabilir mali boyutlar** listesi eşleştirme ölçütleri kapsamında otomatik olarak gerekli olduğundan ana hesap boyutunu içermez.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Genel muhasebe kapatma otomasyonu sonuçlarını görüntüleme

Genel muhasebe kapatma otomasyon serisi oluşturulduktan sonra her genel muhasebe kapatma tekrarı, süreç otomasyonu haftalık görünümünde gösterilir. Ayrıca, her oluşumun durumu gösterilir. Aşağıdaki durumlar kullanılır:

- **Zamanlandı** : Otomasyon zamanlandı ancak henüz çalıştırılmadı.
- **Yürütülüyor**: Otomasyon şu anda çalışıyor.
- **Hata** : Otomasyon çalıştırıldı ancak hata oluştu. Hataları, **Sonuçları görüntüle** düğmesini seçerek görüntüleyebilirsiniz.
- **Tamamlandı** : Otomasyon başarıyla çalıştırıldı. Kapatma sonuçlarını **Genel muhasebe kapatmaları** sayfasında görüntüleyebilirsiniz.

Eşleşen sonuçları görüntülemek için **Genel muhasebe \> Periyodik görevler \> Genel muhasebe kapatmaları**'na gidin. **Genel muhasebe kapatmaları** sayfasındaki **Otomasyon kuralı** alanında hareketi kapatmak için kullanılan otomatik genel muhasebe kapatma zamanlanmış görevinin adı görüntülenir. Başarısız kapatma deneme sayısı **Otomasyon kuralı** değerini güncelleştirmez. Önceden otomasyon süreciyle başarıyla kapatılmış bir hareketi el ile tersine çevirirseniz **Otomasyon kuralı** değeri kaldırılır.

Eşleşen kayıtlar için **Kapatılan tarih** alanı, otomasyon sürecinin gerçekleştirildiği tarihi gösterir.

## <a name="editing-a-ledger-settlement-automation"></a>Genel muhasebe kapatma otomasyonunu düzenleme

İşlem Otomasyonu çerçevesi genel muhasebe kapatma işlemi için oluşturulan tekrarlamaları düzenlemenize olanak tanır. Seri, **İşlem otomasyonu** sayfasından veya işlem otomasyonu haftalık görünümünden düzenlenebilir. Örneğin, yönetici genel muhasebe kapatma işlemini Pazartesi yerine Çarşamba günü gerçekleştirmeye karar verirse haftalık görünümde bir tekrar bulabilir ve **Görünüm/Düzenle-Seriler**'i seçebilir.

Bir seriyi düzenlerseniz değişikliğin tüm mevcut tekrarlarda mı yoksa yalnızca yeni tekrarlarda mı yapılacağını belirtmeniz istenir. **Tamamlandı** durumundaki veya **Hata** durumunda sona ermiş olan geçmiş tekrarlar değiştirilmez.

Ayrıca, yeni bir olay ekleyebilir veya varolan bir oluşumu değiştirebilirsiniz. Örneğin, sonraki genel muhasebe kapatma tekrarı 1 Ocak Çarşamba günü çalışması için zamanlanır ancak bu tarih tatil günüdür. Tekrarı **Süreç otomasyonu** sayfasından veya süreç otomasyonu haftalık görünümünden değiştirebilirsiniz. Zamanlama ayrıntılarını ve eşleştirme ölçütlerini gösteren bir sayfa açılır. Burada, planlanan saati ve tarihi düzenleyebilirsiniz. Ayrıca değişiklik gerekiyorsa eşleştirme ölçütlerini düzenleyebilirsiniz. 

Ayrıca bir oluşumu veya seriyi devre dışı bırakabilirsiniz. Bir tekrarı devre dışı bırakmak ve işlemeyi askıya almak için işlem otomasyonu haftalık görünümünde seçin ve **Devre dışı bırak** seçeneğini belirleyin. **İşlem otomasyonu** sayfasında bir seriyi devre dışı bırakabilirsiniz.

## <a name="security-for-ledger-settlement-automation"></a>Genel muhasebe kapatma otomasyonu için güvenlik

Genel muhasebe kapatma otomasyonları için Muhasebe yöneticisi ve Muhasebe gözetmeni rollerine **Genel muhasebe kapatmaları otomasyon serisi ayarlarını koru** görevi ve Muhasebeci, Muhasebe yöneticisi ve Muhasebe gözetmeni rollerine **Genel muhasebe kapatmaları otomasyon serisi ayarlarını görüntüle** görevi eklenmiştir. Bu görevler varsayılan güvenlik ayarları, ancak kuruluşunuzun gereksinimlerine göre değiştirilebilir.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Genel muhasebe kapatma otomasyonu için genel muhasebe parametreleri

**Kapatma tipik bakiyesi** alanı, otomatik muhasebe kapatma işleminin işleneceği sırayı gösterir. **Kapatma tipik bakiyesi** değerini ayarlamak veya görüntülemek için **Genel muhasebe \> Kurulum \> Genel muhasebe parametreleri**'ne gidin ve **Genel muhasebe kapatmaları** sekmesini seçin.

**Borç** seçilirse borç tarafında otomatik muhasebe kapatma işlemi başlatılır ve karşılık gelen alacaklar aranır. **Alacak** seçilirse alacak tarafında otomatik muhasebe kapatma işlemi başlatılır ve karşılık gelen borçlar aranır. Bu seçenek, ana hesabın tipik bakiyesini yansıtmalıdır.

## <a name="processing-a-ledger-settlement-automation"></a>Genel muhasebe kapatma otomasyonunu işleme

Otomasyon çalıştırıldığında sistem, süreç otomasyonu serisinde tanımlanan ana hesaplar için genel muhasebe hareketlerini seçer. Mali yılın başlangıcından süreç otomasyonunun çalıştırıldığı tarihe kadar olan bir tarih aralığını kullanarak hareketleri tarihe göre sıralar. Belirtilen eşleştirme ölçütüne göre eşleştirme yapar. Borç ve alacakların muhasebe para birimi tutarlarının mutlak değerlerinin kapatılacak şekilde eşleştirilmesi gerekir.

Ana hesap, bir genel muhasebe kapatma otomasyonunun tekrarı ile işlenir ancak bunu **Genel muhasebe kapatmaları** sayfasında görüntüleyemezsiniz. Otomasyon süreci tamamlanana kadar beklemeniz gerekir. Çakışmaları önlemeye yardımcı olması için süreç otomasyonunu çalışma saatleri dışında çalışacak şekilde zamanlamanızı öneririz.

Otomasyon süreci, **Genel muhasebe kapatmaları** sayfasında kapatma için el ile işaretlenen hareketler dışında ölçütleri karşılayan tüm işlemleri içerir.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Otomasyon süreci ile kapatılan hareketleri ters çevirme

Otomatik genel muhasebe kapatma işlemi ile yapılan bir kapatmayı tersine çevirebilirsiniz. Otomasyon süreciyle kapatılmış bir hareketi tersine çevirirseniz **Otomasyon kuralı** değeri kaldırılır.
