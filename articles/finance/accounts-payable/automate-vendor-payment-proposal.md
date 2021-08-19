---
title: Satıcı ödeme tekliflerini otomatikleştirme
description: Bu konu, yinelenen bir zamanlamada satıcıları ödeyen kuruluşların, satıcı ödeme tekliflerini oluşturma sürecini nasıl otomatikleştirebileceğini açıklar.
author: kweekley
ms.date: 04/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 483621a5de2980212926ac1011c16f1b82e4a3d075bbe9bcbbe6a0e35f06e5bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749114"
---
# <a name="automate-vendor-payment-proposals"></a>Satıcı ödeme tekliflerini otomatikleştirme

[!include [banner](../includes/banner.md)]

Yinelenen bir zamanlamada satıcıları ödeyen kuruluşların, satıcı ödeme tekliflerini oluşturma sürecini artık otomatikleştirebilir. Satıcı ödeme teklifi tahminleri aşağıdaki ayrıntıları tanımlayın:

- Ödeme teklifleri çalıştırıldığında
- Ödenmesi gereken faturaları seçmek için hangi ölçütler kullanılır
- Sonuçta elde edilen ödemelerin kaydedildiği satıcı ödeme günlüğü

Ödeme teklif tahminleri otomatik olarak ödemeleri deftere nakletmez. Bu nedenle, şu anda oluşturulan ödemeleri onaylamak için kullandığınız herhangi bir doğrulama ve iş akışı işlemini kullanmaya devam edebilirsiniz.

## <a name="define-the-occurrence-of-vendor-payment-proposals"></a>Satıcı ödeme tekliflerinin oluşumunu tanımla

Satıcı ödeme teklifi otomasyonları, İşlem otomasyonu çerçevesini kullanır. Farklı iş süreçleri seçili bir işlemin tekrarlanma tanımlamak için bu çerçeveyi kullanır. Satıcı ödeme teklifleri için, Otomasyonda **borç hesapları \> ödeme kurulumu \> işlemi otomasyonunda** erişilebilir.

Önce, **Yeni işlem oluştur** Otomasyonu seçeneğini kullanın ve **satıcı ödeme teklifi**'ni seçin. Sihirbaz daha sonra, satıcı ödeme teklifini ayarlama sürecinde size rehberlik eder.

## <a name="general-page"></a>Genel sayfa

Sihirbazın **Genel** sayfasında, oluşturmakta olduğunuz satıcı ödeme teklifinin adını girin. Örneğin, yurtiçi satıcıları Pazartesi günü kontrol ederek ödüyorsanız, **yurtiçi\_çek** gibi açıklayıcı bir ad girin. Girdiğiniz ad, **satıcı ödemeleri** çalışma alanındaki Process Automation haftalık görünümünde gösterilir.

Ardından, oluşturulan ödeme günlüğünün sahibini tanımlayın. Sahibi genellikle, oluşturulduktan sonra ödeme günlüğünden sorumlu borç hesapları (AP) ödeme memuru olur.

Sayfadaki geri kalan ayarlar geneldir ve satıcı ödeme teklifinin bu sürümü için oluşum modelini tanımlamak için kullanılır. Örneğin, bir oluşum Pazartesi günü yapılan çek ödemeleri içinse haftalık çalışacak şekilde tanımlayabilirsiniz ve çalıştığı zaman haftanın günü olarak Pazartesiyi seçebilirsiniz. Ayrıca, işlem otomasyonunun sonraki iş günü başlangıcından önce tamamlanacağı şekilde, 2:00 gibi erken bir planlama zamanı da girebilirsiniz.

Satıcı ödeme teklifinin ne zaman işlendiğini tanımlamak için Sihirbazı kullanmakta olduğunuzu anlamanız önemlidir. Satıcı ödemelerinin ne zaman oluşturulacağını, yazdırılmadığını ve deftere nakledildiğini tanımlamadığınızda. Haftalık görünümde, satıcı ödeme teklifleri için işlem otomasyonu, yineleme deseninde seçili olan günlerde görünür.

**Genel** sayfasındaki diğer alanlar hakkında daha fazla bilgi için işlem otomasyonu belgelerine bakın.

## <a name="vendor-payment-proposal-page"></a>Satıcı ödeme teklifi sayfası

Sihirbazdaki sonraki sayfa **satıcı ödeme teklifi** sayfasıdır. Bu, ödenmesi gereken satıcı faturalarını seçme ölçütlerini tanımlamak için kullanılır. Genel olarak, ödeme teklifinde satıcı ödeme günlüğündeki aynı seçenekler bulunur. Ancak, birkaç istisna vardır. Örneğin, bu sayfadaki tüm tarihler, teklif her çalıştırıldığında ödeme teklif tarihi değiştiği için, ilgili tarih olarak tanımlanmalıdır.

### <a name="journal-name"></a>Günlük adı

**Günlük adı** alanı, satıcı ödemelerinin oluşturulduğu günlük adını tanımlar. Satıcı ödeme teklifi otomasyonunun sonuçları tanımlanan günlükte ödemeler oluşturacak, ancak günlük deftere nakledilemez.

### <a name="from-date-and-to-date"></a>"Başlangıç" tarihi ve "bitiş" tarihi

Son Tarih veya nakit iskontosu tarihine dayalı faturaları seçmek üzere "başlangıç" tarihi ve "bitiş" tarihi tanımlamak yerine, "bitiş" tarihini tanımlamak için **tarihe göre ölçüt tanımla** seçeneğini ve **bugüne kadarki ayarlama günleri sayısı** alanını kullanmanız gerekir. Ödeme teklifi için bir "başlangıç" tarihi kavramı yok.

Varsayılan olarak, **Tarih ölçütünü tanımla** seçeneği **Hayır** olarak ayarlanır. Bu varsayılan değeri kullanırsanız, "bitiş" tarihi tanımlanmadığından, işlem çalıştırıldığında tüm faturalar ödeme için seçilecek.

**Tarihe göre değer ölçütünü tanımla** seçeneğini **Evet** olarak ayarlarsanız faturanın çalıştığı tarihten önce veya sonra faturaların seçildiği tarihi tanımlamak için, **bugüne kadarki ayarlama günleri sayısı** alanını kullanın. Sayı pozitif, negatif veya 0 (sıfır) olabilir. Daha sonra sistem, vade sonu veya nakit iskontosu tarihleri, sürecin çalıştırıldığı tarihten önce veya sonra gelen gün sayısı olan faturalar ödemesine neden olacak. Örneğin, süresi Cuma günü Itibariyle veya bu tarihten önce olan tüm faturalarda, ödeme serisi, Çarşamba 'yı denetleyerek Tüm satıcılara ödeme oluşturur. Bu durumda, bitiş **bugüne kadarki ayarlama günleri sayısı** alanını **2** ' ye ayarlayın. Ödeme teklifinin oluşumu 25 Mart Çarşamba günü çalıştırıldığında, vade tarihi veya nakit iskontosu tarihi 27 Mart 'ta veya daha önce olan tüm faturalar ödeme için seçilir.

### <a name="minimum-payment-date"></a>Minimum ödeme tarihi

Minimum ödeme tarihi, ödemeler oluşturulurken kullanılan en erken tarihi olacaktır. Önce **Minimum ödeme tarihi ölçütünü tanımla** seçeneğini **Evet** olarak ayarlamalısınız. Bu ayar, minimum ödeme tarihi işlevini kullanmanızı sağlar. Bu seçeneği **Evet** olarak ayarlarsanız işlemin çalıştığı tarihten önce veya sonra minimum ödeme tarihini bleirtilen gün sayısı olarak tanımlamak içni **minimum ödeme tarihi için ayarlama günleri sayısı** alanını kullanın. Sayı pozitif, negatif veya 0 (sıfır) olabilir. Örneğin, ödeme serisi, önceki Pazartesi günü için minimum ödeme tarihi olan tüm ödemeleri içermek üzere Çarşamba günü ilgili ödemeler oluşturur. Bu durumda, bitiş **Minimum ödeme tarihine kadarki ayarlama günleri sayısı** alanını **-2**'ye ayarlayın.

Aşağıda, "bitiş" tarihine ve minimum ödeme tarihine yönelik alanların birlikte nasıl çalıştığını gösteren bir örnek yer verilmektedir. Ödeme teklifi Otomasyonu, Çarşamba günü çalışacak şekilde ayarlanır. Vade tarihine göre "bitiş" tarihini tanımlamak için **bitiş tarihi için ayarlama gün sayısı** alanı **1** olarak ayarlanır. Bitiş **Minimum ödeme tarihine kadarki ayarlama günleri sayısı** alanını **-2**'ye ayarlayın. Ödeme işlemi otomasyonu 25 Mart Çarşamba günü başlıyorsa, ödenmesi gereken veya 26 Mart öncesinde olan tüm faturalar ödeme teklifine dahil edilir. Ödeme teklifleri aşağıdaki şekilde oluşturulur:

- Süresi geçecek veya daha önce olan tüm faturalar 23 Mart ödeme tarihine sahip olacaktır.
- Vadesi 24 mart olan faturalar 24 Mart ödeme tarihine sahip olacaktır.
- Vadesi 25 mart olan faturalar 25 Mart ödeme tarihine sahip olacaktır.
- Vadesi 26 mart olan faturalar 26 Mart ödeme tarihine sahip olacaktır.

### <a name="summarized-payment-date"></a>Özetlenmiş ödeme tarihi

Özetlenmiş ödeme tarihi yalnızca ödeme yöntemi üzerindeki **Dönem** alanı **Toplam** olarak ayarlanmışsa kullanılır. **Dönem** alanı ödeme yöntemleriniz için **toplam** olarak ayarlanmışsa, **özetlenen ödeme tarihi ölçütü tanımla** seçeneğini **Evet** olarak ayarlamalısınız. Bu seçeneği **Evet** olarak ayarlarsanız işlemin çalıştığı tarihten önce veya sonra özetlenmiş ödeme tarihini bleirtilen gün sayısı olarak tanımlamak içni **özetlenmiş ödeme tarihi için ayarlama günleri sayısı** alanını kullanın. Sayı pozitif, negatif veya 0 (sıfır) olabilir. Örneğin, seri Çarşamba günü ödemeleri oluşturur ve şirket Çarşamba günü bir Özet ödeme oluşturmak istemektedir. Bu durumda, bitiş **özetlenmiş ödeme tarihine kadarki ayarlama günleri sayısı** alanını **0**'ye ayarlayın.

### <a name="records-to-include"></a>Eklenecek kayıtlar

Ödeme teklifi için filtre seçenekleri gene de tanımlanabilir. Filtre tanımlanırsa, filtre ölçütü sihirbaz sayfasında gösterilmez. Ancak, filtre yeniden açarak görüntülenebilir.

Teklif için kalan alanlar, satıcı ödeme günlüğündeki ödeme teklifi için çalıştıkları gibi çalışır. Diğer alanlar hakkında daha fazla bilgi için bkz. [Ödeme teklifi kullanarak satıcı ödemeleri oluştur](create-vendor-payments-payment-proposal.md).

> [!NOTE]
> Bazı ülkeye/bölgeye özel alanlar ve bazı genel kesim alanları, henüz satıcı ödeme teklifi için mevcut değil.

Gereksinimlerinize göre, otomasyonunuzun kuruluşunuza yararlı olacağını değerlendirmeniz önerilir.

## <a name="view-the-results-of-a-vendor-payment-proposal-automation"></a>Satıcı ödeme teklifi Otomasyonu sonuçlarını görüntüleme

Satıcı ödeme teklifi Otomasyon serisi oluşturulduktan sonra, her bir ödemenin örnekleri İşlem Otomasyonu haftalık görünümünde gösterilir. Satıcı ödemeleri için İşlem Otomasyonu haftalık görünümü hem **Satıcı ödemeleri** çalışma alanına hem de **İşlem otomasyonu** sayfasına eklenmiştir.

[![Satıcı ödemeleri çalışma alanında işlem otomasyonu haftalık görünümü.](./media/vendor-payment-proposal-1.png)](./media/vendor-payment-proposal-1.png)

**Satıcı ödemeleri** çalışma alanında, işlem otomasyonu haftalık görünümü yalnızca satıcı ödeme teklifi tahminleri gösterir. Bu, geçerli hafta için tüm ödemelerin oluşumlarını, oturum açan kullanıcının güvenlik izinleri olan tüm yasal varlıklar için gösterir. Örneğin, USBMF ve USSI şirketlerinde bulunan ödemelerden BH ödeme memuru sorumlu ise, bu iki şirket için satıcı ödeme teklifi otomasyonunun tekrarlamalarını görür, ancak diğer şirketler için görmez.

[![USMF ve USSI şirketleri için işlem otomasyonu haftalık görünümü.](./media/vendor-payment-proposal-2.png)](./media/vendor-payment-proposal-2.png)

Her oluşum, ödeme günlüğünün oluşturulacağı şirketi gösterir. Ödemeler Merkezi ödemeler kullanılarak oluşturulduysa, gösterilen şirket ödemede oluşturulacağı şirkettir. Oluşum, hangi şirket faturalarının ödeneceğini göstermelidir.

Ayrıca, her bir oluşumun adı, ödeme teklifinin tanımlanmasına yardımcı olmak amacıyla da gösterilmiştir.

Ayrıca, her oluşumun durumu gösterilir. Aşağıdaki durumlar kullanılır:

- **Planlanan** – Ödeme teklifi planlanmış, ancak henüz çalışmadı.
- **Hata** – Ödeme teklifi çalıştırıldı, ancak hata oluştu. **Sonuçları görüntüle** düğmesini seçerek hataları görüntüleyebilirsiniz.
- **Tamamlandı** – Ödeme teklifi başarıyla çalıştırıldı. **Ödemeleri görüntüle** bağlantısını seçerek ödemeleri görüntüleyebilirsiniz. Bu bağlantı, oluşumdan oluşturulan ödeme günlüğünü açar.

Ödemeler oluşturulduktan sonra, günlükteki ödeme tutarlarını görüntüleyebilirsiniz. Gösterilen tüm tutarlar işlem para birimleri cinsindendir. Örneğin, ödeme günlüğü ABD doları ve Kanada doları cinsinden ödemeler içeriyorsa, her para birimi için toplam ödemeler gösterilir. 

Ödeme günlüğü, işlem otomasyonu ile oluşturulduktan sonra silinebilir. Bir ödeme tümüyle silinirse, aşağıdaki olaylar gerçekleşir:

- Haftanın işlem otomasyonu durumu **tamamlandı** olarak kalmaya devam eder.
- İşlem ödeme toplamlarını kaldırır ve **ödemeleri görüntüle** bağlantısı, **sonuçları görüntüle** düğmesiyle değiştirilir.
- Sonuçları görüntülediğinizde, özgün günlüğün silindiğini belirten bir ileti alırsınız.

Ödeme silindikten sonra, faturalar ödeme için yeniden açık olur. Daha sonra faturaları tekrar ödemek için yeni bir oluşum oluşturulabilir.

## <a name="edit-a-vendor-payment-proposal-automation"></a>Satıcı ödemesi teklif otomasyonu düzenle

İşlem Otomasyonu Çerçevesi ödemeyi, serileri ve ödeme teklifi için oluşturulan tekrarlamaları düzenlemenize olanak tanır. Seri, **İşlem otomasyonu** sayfasından veya işlem otomasyonu haftalık görünümünden düzenlenebilir. Örneğin, AP Yöneticisi yurtiçi satıcılar için tüm çekleri Pazartesi yerine Çarşamba günü oluşturmaya karar verirse, haftalık görünümde bir oluşum bulabilir ve **Görünüm/Düzenle-Seriler**'i seçebilir. Bir seriyi düzenlerseniz, sistem değişikliğin tüm varolan oluşumlara mı yoksa yalnızca yeni oluşumlara mı getirilmeyeceğini belirtmenizi ister. **Tamamlandı** durumundaki veya **hata** durumunda sona ermiş olan geçmiş oluşumları değiştirilmez.

Ayrıca, yeni bir olay ekleyebilir veya varolan bir oluşumu değiştirebilirsiniz. Örneğin, sonraki ödeme teklifi oluşumu 1 Ocak, ancak bu tarih bir tatil olan Çarşamba çalışması için zamanlanır. Oluşumu **İşlem otomasyonu** sayfasından veya işlem otomasyonu haftalık görünümünden değiştriebilirsiniz. Zamanlama ayrıntılarını ve ödeme teklifi ölçütlerini gösteren bir sayfa açılır. Burada, planlanan saati ve tarihi düzenleyebilirsiniz. Ayrıca, değişiklik gerekiyorsa, ödeme teklif ölçütlerini düzenleyebilirsiniz. Örneğin, ödeme oluşumunun planlanan tarihini 1 Ocak ile 2 Ocak arasında değiştirirseniz, "bitiş" tarihi için de göreli tarihleri değiştirmek isteyebilirsiniz.

Ayrıca bir oluşumu veya seriyi devre dışı bırakabilirsiniz. Bir oluşumu devre dışı bırakmak ve işlemeyi askıya almak için, İşlem Otomasyonu haftalık görünümünde seçin ve **devre dışı bırak**'ı seçin. **İşlem otomasyon** sayfasında bir seriyi devre dışı bırakabilirsiniz.

## <a name="security-for-payment-proposal-automations"></a>Ödeme teklif otomasyonları güvenliği

Satıcı ödeme teklifi için aşağıdaki görevler ve ayrıcalıklar eklendi. Bu görevler ve ayrıcalıklar varsayılan güvenlik ayarları, ancak kuruluşunuzun gereksinimlerine göre değiştirilebilir. Örneğin, yalnızca BH Yöneticisi değil de AP ödeme memuru düzenleyip zamanlama yinelemesi oluştururtabilecekse, **iş planlama çizelgeleme tekrarlarını** AP ödeme memuru rolündeki kişiye atayın.

| Görev                              | Rol                                                                       | Ayrıcalıklar |
|-----------------------------------|----------------------------------------------------------------------------|------------|
| Çizelge serisi tut          | Borç hesapları müdürü                                                   | Bu vergi, aşağıdaki ayrıcalıklar sayesinde ödeme teklifi Otomasyonu serisi ve oluşumlarını oluşturma ve sürdürme hakkını verir:<ul><li>Çizelge tekrarlamalarını koru</li><li>Çizelge serisi tut</li><li>ProcessScheduleOccurrenceListMaintain</li><li>Oluşumlar görüntüle Haftalık Görünüm</li></ul> |
| Zamanlama tekrarlarıyla sorgulama | Borç hesapları ödeme memuru, borç hesapları Merkezi ödeme memuru | Bu vergi, aşağıdaki ayrıcalıklar sayesinde ödeme teklifi Otomasyonu oluşumlarını görüntüleme hakkını verir:<ul><li>Çizelge tekrarlamalarını görüntüle</li><li>Oluşumlar görüntüle Haftalık Görünüm</li></ul> |
| Zamanlama serisine sorgula      | Hiçbiri                                                                       | Bu vergi, aşağıdaki ayrıcalıklar sayesinde seri ayarlarını ve oluşumlarını görüntüleme hakkını verir:<ul><li>Çizelge tekrarlamalarını görüntüle</li><li>Oluşum listesi sayfasını görüntüle</li><li>Oluşumlar görüntüle Haftalık Görünüm</li></ul>|
| Çizelge tekrarlamalarını koru     | Hiçbiri                                                                       | Bu vergi, aşağıdaki ayrıcalıklarla bir oluşumu oluşturma ve bakımını yapma hakkını verir:<ul><li>Çizelge tekrarlamalarını koru</li><li>Oluşumlar görüntüle Haftalık Görünüm</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]