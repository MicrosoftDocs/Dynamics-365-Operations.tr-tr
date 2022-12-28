---
title: Proaktif kalite güncelleştirmeleri
description: Bu makale, kalite güncelleştirmelerinin proaktif olarak sunulmasına ilişkin bilgi sağlar.
author: rashmansur
ms.date: 11/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 7d8de017c54a13a9935d74d33a57813922c9f823
ms.sourcegitcommit: 8aee31d6dffabe13969dd5b9de4e0bf95f53e67e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887143"
---
# <a name="proactive-quality-updates"></a>Proaktif kalite güncelleştirmeleri

[!include[banner](../includes/banner.md)]

Son yedi yıl boyunca Microsoft [Bir Sürüm ](../../dev-itpro/lifecycle-services/oneversion-overview.md) olarak adlandırdığımız şey üzerinde sürekli olarak ilerleme gerçekleştirdi. Bir Sürüm önermesi basittir: tüm müşterileri aynı yazılım sürümünde olmasını sağlamaya ne kadar yakın olursak o kadar yüksek kalite sunabiliriz. Sorunları bir kerede bulup çözer ve çözümleri müşterilerimize çok daha hızlı sunarız.

Bu önerme şu sonuçlarla onaylanmıştır: ürünlerimizde daha düşük olay sayısı. Müşteriler aynı sürümde olmadığında, sürekli olarak zaten bir çözümü bulunan sorunlardan etkilendiklerini görüyoruz. Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations ve Dynamics 365 Commerce için büyük bir ilerleme kaydettik ve son teknik gelişmeler sayesinde artık sonraki adıma geçebiliriz. Aşağıdaki bilgiler neler yapacağımızı, aşamayı ayarlamak için neler yapmış olduğumuzu ve yeni özellikleri kesinti olmadan ne zaman sunacağımızı açıklamaktadır.

## <a name="what-you-need-to-know"></a>Bilmeniz gerekenler

- Proaktif kalite güncelleştirmeleri (PQU) aylık olarak uygulanır.
- Yalnızca ABD Gıda ve İlaç Dairesi (FDA) düzenlemelerine tabi olan müşteriler için proaktif kalite güncelleştirmeleriyle ilgili özel durumlara izin verilir.
- Önleyici kalite güncelleştirmeleri hiçbir zaman ortamın indirgemeye veya bir hizmet güncelleştirme sürümünden diğerine otomatik olarak yükseltilmeyecek. 
- Düzenlemeye tabi ortamlar ve bağımsız ve kamu bulut müşterileri için proaktif kalite güncelleştirmelerinin nasıl yönetileceğini Microsoft belirler.
- Önleyici kalite güncelleştirmeleriyle ilgili olan bildirimler ileti merkezi [Microsoft 365 İleti Merkezinde](https://admin.microsoft.com/AdminPortal/) paylaşılır.
- Bir ortama proaktif kalite güncelleştirmesi uygulanmadan beş gün önce, müşterilere güncelleştirmenin yapılacağı bildirilir.
- Müşteriler proaktif kalite güncelleştirmelerini iptal edemez veya erteleyemezler.
- Proaktif kalite güncelleştirmeleri bölgeye özel [planlı bakım aralığı](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows) sırasında yüklenir.
- Kalite güncelleştirmeleri, sorun veya gerileme riski düşük olacak şekilde tasarlanmıştır ve Microsoft verileriyle desteklenir.
- Microsoft, proaktif kalite güncelleştirmesiyle ilgili belirli sorunlar veya belirli düzeltmeler için hedeflenmiş testler önerir.
- Yasal nedenlerle zaman sınırlı özel duruma sahip olanlar dışında tüm sanal alanlar ekleme 7 Ocak 2023 tarihine kadar olacaktır.
- Önleyici kalite güncelleştirmeleri için üretim ekleme 21 Ocak 2023'ten başlar. 
- Üretim ekleme, yalnızca korumalı alan eklenmiş ve düzenli aralıklarla proaktif kalite güncelleştirmelerini tüm desteklenen hizmet güncelleştirme sürümleri alan Lifecycle Services projeleri için başlayacaktır. Bu yalnızca, yasal veya yasal nedenlerle özel durum sağlanmayan müşteri ortamları için geçerlidir.
- 2023 emri üzerinden korumalı alan ve üretim ortamları için önleyici kaliteli güncelleştirmelerin tam zamanlaması için aşağıya bakın.
- Her hizmet güncelleştirmesinde, başlamak üzere sürekli veya dengeli en az bir PQU yayın eğitimi vardır. Çevreleriniz PQU işlemine eklendikten sonra, daha yeni bir sürüm hizmeti güncelleştirmesine geçtiğinizde, tümü için önceden zamanlanmış, önleyici bir kalite güncelleştirmesi alabilirsiniz. Daha yeni bir sürüm hizmeti güncelleştirmesine yükseltmeyi planlıyorsanız, hizmet güncelleştirmesi için bir PQU denetiminin zamanlanacağını belirlemek için zamanlamayı denetleyin. 

> [!Note]
> Standart performans testi (katman4), Premium performans test (katman5) sanal alanlar ve üretim ortamları hafta sonları üzerinde PQU alır. 

## <a name="focus-on-quality-updates"></a>Kalite güncelleştirmelerine odaklanma

Şu anda yılda yedi [hizmet güncelleştirmesi](public-preview-releases.md) sunuyoruz. Örneğin, 10.0.29 sürümü bir hizmet güncelleştirmesidir. Son güncelleştirmeye kadar yıl başına sekiz güncelleştirme vardı. Ancak, takvim yılının sonunda yapılan değişikliklerden kaçınmaya yönelik bir isteği ortaya çıkaran müşteri geribildirimlerine yanıt olarak bir güncelleştirmeyi bıraktık.

Hizmet güncelleştirmelerinin temposunu değiştirmeyeceğiz. Bunun yerine, Bir Sürüm yolculuğundaki sonraki adımımız *kalite güncelleştirmelerine* odaklanmak. Kalite güncelleştirmeleri, toplu düzeltme derlemeleridir. Yeni özellikler içermezler. Herhangi bir anda, tüm müşteri topluluğumuz üç veya dört son hizmet güncelleştirmesi arasında dağıtılır. Ancak, herhangi bir hizmet güncelleştirmesi için, kişilere dağıtım yapıldığı tarihe bağlı olarak grup içinde onlarca farklı kalite güncelleştirmesi sürümü kullanılabilir. Sonraki adımımızda, kalite güncelleştirmelerini proaktif olarak yayınlayacağız. Bu modeli zaten Dataverse tabanlı uygulamalarımız zaten kullanyoruz ve kalitenin artması ve destek olaylarının azalması yönünde beklenen sonuçları gördük.

Elbette, hataların azaltılması kalite güncelleştirmelerine duyulan gereksinimi azaltabilir veya tamamen ortadan kaldırabilir. Kalite güncelleştirmeleri gerekitren hataları azaltmaya yönelik yürütülen birçok girişimimiz var. Kalite güncelleştirmesinde yük azaltıldığında bile müşteri tabanındaki tutarlılık desteklenebilme, müşterilere daha hızlı geliştirmeler sağlama ve müşterilerin zaten çözümleri bulunan sorunlarla karşılaşma sıklığını iyileştirecektir.

## <a name="making-proactive-distribution-possible"></a>Proaktif dağıtımı mümkün hale getirme

Kalite güncelleştirmelerinin proaktif şekilde teslim edilmesini sağlayan birden fazla gelişme zaten dağıtıldı:

- **Sıfıra yakın kesinti güncelleştirmesi**: Daha sık kullanılan ortamlara gönderim yapmak için, Dynamics 365 Hizmet Düzeyi Sözleşmlerini (SLA'ları) korumak açısından ortam kullanılabilirliği üzerindeki etkinin azaltılması temeldir. Sıfıra yakın kesinti güncelleştirmesi, başlangıçta güncelleştirilen görüntüyü minimum kesintiyle etkinleştirmek için yük devretme kümesi kullanarak aylık işletim sistemi düzeltme eki uygulamasını geliştirmek amacıyla sunulmuştur. Güncelleştirmeleri uygulama mekanizması daha az kesintiye uğramasını sağlayacak şekilde geliştirilmiştir ve hem işletim sistemi düzeltme eki uygulamasını hem de kalite güncelleştirmesi dağıtımını kapsar.

    Etkileşimli kullanıcılar için, etkin bir oturum yarıda kesilebilir ve yeniden deneme şimdi güncelleştirilmiş ortama gider. [Öncelik temelli toplu iş planlamanın](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) kullanıma sunulmasıyla toplu iş planlama ve işleme kurtarır ve güncelleştirmeden hemen sonra sürdürülür. Öncelik temelli toplu iş planlama, müşterilere üretim ortamları için proaktif kalite güncelleştirmeleri dağıtımına katılmaya başlamadan önce gerçekleştirilecektir.

- **Karanlık saatler**: Karanlık saatler her Azure bölgesi için tanımlanmıştır ve neredeyse sıfır kesinti süresi güncelleştirmeleri karanlık saat döneminde gerçekleştirilecektir.

## <a name="the-proactive-update-process"></a>Proaktif güncelleştirme işlemi

Proaktif kalite güncelleştirmeleri dağıtımı, güvenli bir dağıtım işlemini (SDP) izleyecektir. SDP özellikleri geliştirilecektir ancak kalite güncelleştirmeleri öncelikle korumalı alan ortamlarına dağıtılacaktır. Başarıyla dağıtım yapılan korumalı alanların yüzdesi arttıkça, üretim ortamlarına dağıtım süreci başlayacaktır. Dinleme sistemleri, sistem telemetrisini ve canlı site olaylarını izleyecek ve herhangi bir gerileme algılanırsa belirli bir sürümün dağıtımızını durduracaktır. Müşteriler yine de istemeleri durumunda kalite güncelleştirmelerini proaktif dağıtımdan önce çekebilecektir.

Geçerli sürüm yönetimi verileri, kalite güncelleştirmelerinde gerilemelerin yüzde 3'ten azının sunulduğunu göstermektedir. Gerilemeyi ortadan ve geliştirilmiş bir SDP'ye odaklanmanın artırılamasıyla gerilemelerin olası etkisi, müşterilere genel olarak dağıtılmış düzeltmelerle elde edilen kalite kazançlarına göre önemli ölçüde daha düşük olacaktır.

## <a name="process-changes"></a>Değişiklikleri işle

Proaktif kalite güncelleştirme dağıtımının etkinleştirilmesinin ötesinde bir dizi süreç değişikliği zaten uygulanmaktadır:

- **Şema**: Araç, kalite güncelleştirme derlemelerinin yalnızca hizmet çevrimiçi olduğunda uygulanabilen şema değişikliklerini içermesini sağlayacaktır. Bu yaklaşım, güncelleştirmeyi sıfır kesinti süresiyle uygulama yeteneğini korumanıza yardımcı olur.
- **Artırılmış değişiklik incelemesi**: Şu anda zaten değişikliklerin kalite güncelleştirmesine eklenmesini onaylamaya yönelik ekstra bir süreç adımı bulunmaktadır. Ekstra adımdaki inceleme gerileme potansiyeli azaltmaya yardımcı olmak amacıyla artırılacaktır. Kalite güncelleştirmelerinde hataya neden olan değişikliklere izin verilmez ve artırılmış değişiklik incelemesi bu hedefe ulaşmaya yardımcı olacaktır.
- **Görünürlük**: Gelecekteki proaktif kalite güncelleştirmeleri için bildirimler, yönetim merkezi, Lifecycle Services ve diğer mevcut kanallar üzerinden gönderilir. Ek olarak, destek takımları ve olay liderleri, kalite güncelleştirmelerinin proaktif olarak dağıtıldığı yerler için görünebilirliğe sahip olacaktır.

    > [!NOTE]
    > Microsoft İletişimleri ekibi, e-posta bildirimlerinin teslim edilmesini engelleyen e-posta araçlarının sürekli performans düşüşünü araştırmaktadır. İşe alma ve bildirimle ilgili iletiler için lütfen Microsoft 365 İleti Merkezi'ni izlemeye devam edin.

- **Dağıtım yoluyla Fail Safe** – Dağıtım, bir kalite güncellemesi hata düzeltmesinde uygun olan yerlerde kod değişikliklerini korumak için kullanılır veya düzeltmeyle ilgili mevcut özellik uçuşunu kullanır. Proaktif bir dağıtımdan sonra bir geri dönüş veya değişikliğin kapatılması gerekiyorsa daha fazla başarısızlık oluşmaması için dağıtma sistemi üzerinden yapılabilir.
- **Korumalı alan eşitleme ataması** – Üretimle birlikte seçme için ayrılmış bir sanal alana aşamalı güncelleştirme şu anda desteklenmiyor. Tüm katman 2 ve katman 3 sanal alanlardaki etkin olmayan güncelleştirmeleri, bir Lifecycle Services projesindeki üretim ortamından önce en az 7 gün önce alacaktır. Yine de bu yalnızca, yasal veya yasal nedenlerle özel durum sağlanmayan müşteri ortamları için geçerlidir.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Kalite güncelleştirmeleri için kullanıma sunma yol haritası nedir?

Korumalı alan ortamları için proaktif kalite güncelleştirmeleri dağıtımının Azure genel bulut müşterileri için en geç Eylül 2022'de başlamıştır. 1 Ocak 2023 tarihinde, etkin sanal alanın %99'ı öngörülü kalite güncelleştirmelerine ekleme işlemi tamamlanıyoruz.

Proaktif olarak güncelleştirilen dağıtım işlemiyle ilgili özel durumlara yalnızca FDA düzenlemesine tabi müşteriler için izin verilir. Düzenlenmiş ortamlar ile bağımsız ve kamu bulut müşterilerinin nasıl yönetileceği üzerinde çalışmaya devam ediyoruz. 

Müşteriler düzenli olarak daha küçük yükler alacağından, güncel kalma sürecinin daha kolay hale geleceğini bekliyoruz. Süreci kesintisiz yürütme yeteneğini gösterdiğimizde güncelleştirme dağıtımının sıklığını ayarlayacağız. Bu süreç Dataverse platformumuz ve uygulamalarımız için zaten etkili şekilde çalışıyor ve hizmet kalitesinde beklenen iyileştirmeleri sunuyor. Finans ve operasyon uygulamaları için de aynı adımı atıyoruz.


## <a name="when-will-quality-updates-start-for-production-environments"></a>Üretim ortamları için kalite güncelleştirmeleri ne zaman başlayacak?
2023'ün ilk birkaç ayında 15 Ocak'tan başlayarak üretim ortamlarını önleyici güncelleştirmelere ekleme işlemini başlatacak ve önleyici güncelleştirmeleri alan üretim ortamlarının yüzdesini yavaş şekilde artıracağız. Lifecycle Services içinde yalnızca, proaktif olmayan güncelleştirmeleri almak için zaten eklenmiş korumalı alan ortamları olan bir üretim ortamını hedefliyoruz. Bir güncelleştirmeden önce, üretim ortamlarının eklenen müşterilere Message Center veya LifeCycle Services başlığı kullanılarak bildirim gönderilir. 2023 emri üzerinden korumalı alan ve üretim ortamları için önleyici kaliteli güncelleştirmelerin tam zamanlaması için aşağıya bakın.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Korumalı alan proaktif kalite güncelleştirmeleri için zamanlama nedir?
Her bölgenin aktif olunmayan saatleri hakkında bilgi için bkz. [Bölgeye göre planlanmış bakım süreleri nelerdir?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a>Proaktif kalite güncelleştirmesi sürümü: 10.0.29
**Uygulama sürümü: 10.0.1326.70**  
**İlgili son BB makalesi: 750332**

| İstasyon | Bölgeler | Tamamlanmış Zamanlama | Yaklaşan Korumalı Alan Zamanlaması|
|---|---|---|---|
| 1. İstasyon | Merkez Kanada, Doğu Kanada, Merkez Fransa, Merkez Hindistan, Doğu Norveç, Batı İsviçre | Ekim 14'ten Ekim 17 2022'ye, Kasım 2'den Kasım 5 2022'ye, Kasım 13'ten Kasım 16 2022'ye, Aralık 5'ten Aralık 8 2022'ye | 2 Ocak'tan 5 Ocak 2023'e |
| 2. İstasyon | Güney Fransa, Güney Hindistan, Batı Norveç, Kuzey İsviçre, Kuzey Güney Afrika, Doğu Avustralya, Güney Birleşik Krallık, Kuzey BAE, Doğu Japonya, Güneydoğu Avustralya, Güney Doğu Asya | Ekim 15'ten Ekim 18 2022'ye, Kasım 2'den Kasım 5 2022'ye, Kasım 13'ten Kasım 16 2022'ye, Aralık 5'ten Aralık 8 2022'ye | 2 Ocak'tan 5 Ocak 2023'e |
| 3. İstasyon | Doğu Asya, Batı Birleşik Krallık, Batı Japonya, Güney Brezilya, Batı Avrupa, Doğu ABD, Merkez BAE | Ekim 16'ten Ekim 19 2022'ye, Kasım 2'den Kasım 5 2022'ye, Kasım 13'ten Kasım 16 2022'ye, Aralık 5'ten Aralık 8 2022'ye | 2 Ocak'tan 5 Ocak 2023'e |
| 4. İstasyon | Kuzey Avrupa, Orta ABD, Batı ABD | Ekim 17'ten Ekim 20 2022'ye, Kasım 2'den Kasım 5 2022'ye, Kasım 15'ten Kasım 18 2022'ye, Aralık 5'ten Aralık 8 2022'ye | 2 Ocak'tan 5 Ocak 2023'e |
| 5. İstasyon | DoD, Hükümet Topluluk Bulutu, Çin | Planlanmadı | Planlanmadı |

### <a name="proactive-quality-update-release-10030"></a><a name="schedule"></a>Proaktif kalite güncelleştirmesi sürümü: 10.0.30
**Uygulama sürümü: 10.0.1362.77**
**İlgili son BB makalesini: 767597**

| İstasyon | Bölgeler | Tamamlanmış Zamanlama | Yaklaşan Korumalı Alan Zamanlaması |
|---|---|---|---|
| 1. İstasyon | Merkez Kanada, Doğu Kanada, Merkez Fransa, Merkez Hindistan, Doğu Norveç, Batı İsviçre | 1 Aralık ile 4 Aralık 2022 tarihleri arasında |  13 Aralık ile 16 Aralık 2022 tarihleri arasında | 
| 2. İstasyon | Güney Fransa, Güney Hindistan, Batı Norveç, Kuzey İsviçre, Kuzey Güney Afrika, Doğu Avustralya, Güney Birleşik Krallık, Kuzey BAE, Doğu Japonya, Güneydoğu Avustralya, Güney Doğu Asya | 2 Aralık ile 5 Aralık 2022 tarihleri arasında |  13 Aralık ile 16 Aralık 2022 tarihleri arasında | 
| 3. İstasyon | Doğu Asya, Batı Birleşik Krallık, Batı Japonya, Güney Brezilya, Kuzey Avrupa, Doğu ABD, Merkez BAE | 3 Aralık ile 6 Aralık 2022 tarihleri arasında |  13 Aralık ile 16 Aralık 2022 tarihleri arasında | 
| 4. İstasyon | Batı Avrupa, Orta ABD, Batı ABD | 4 Aralık ile 7 Aralık 2022 tarihleri arasında |  13 Aralık ile 16 Aralık 2022 tarihleri arasında | 
| 5. İstasyon | DoD, Hükümet Topluluk Bulutu, Çin | Planlanmadı | Planlanmadı |

### <a name="proactive-quality-update-calendar-year-2023-schedule"></a><a name="schedule"></a> Önleyici kalite güncelleştirme takvimi yılı 2023 zamanlama

#### <a name="stations-to-region-mapping"></a><a name="Stations-Regions"></a> Bölge eşleme istasyonları

| İstasyonlar | Bölgeler |
|---|---|
| 1. İstasyon | Hesaplanacak |
| 2. İstasyon | Merkez Kanada, Doğu Kanada, Merkez Fransa, Merkez Hindistan, Doğu Norveç, Batı İsviçre |
| 3. İstasyon | Güney Fransa, Güney Hindistan, Batı Norveç, Kuzey İsviçre, Kuzey Güney Afrika, Doğu Avustralya, Güney Birleşik Krallık, Kuzey BAE, Doğu Japonya, Güneydoğu Avustralya, Güney Doğu Asya |
| 4. İstasyon | Doğu Asya, Batı Birleşik Krallık, Batı Japonya, Güney Brezilya, Kuzey Avrupa, Doğu ABD, Merkez BAE |
| 5. İstasyon | Batı Avrupa, Orta ABD, Batı ABD |
| 6. İstasyon | DoD, Hükümet Topluluk Bulutu, Çin |


> [!IMPORTANT]
> Bu, 2023 yılı için yüksek düzey bir zamanlama. Daha somut bir zamanlama için, Ocak 10.0.30 Sürüm 2 için aşağıdaki örneğe bakın. Tam Çizelge ve uygulama sürümü, kalite güncelleştirmesi eğitimi başlangıcından önce 7 gün önce güncelleştirilecektir.

> [!Note]
> Yalnızca eklenen üretim ortamları 10.0.30 Sürüm 2 eğitimi için güncelleştirmeyi alacaktır, eklenen ortamlar açık iletişim alır.

| Kalite Güncelleştirmesi treni | Yayımlama kesimi | Tren süresi |
|---|---|---|
| 10.0.30 Sürüm 2 | 16 Aralık 2022 | 2 Ocak'tan 29 Ocak 2023'e |
| 10.0.30 Sürüm 3 | 13 Ocak 2023 | 30 Ocak'tan 25 Ocak 2023'e |
| 10.0.30 Sürüm 4 | 24 Şubat 2023 | 6 Mart'tan 8 Nisan 2023'e |
| 10.0.31 Sürüm 1 | 3 Şubat 2023 | 13 Şubat 2023'ten 18 Mart 2023'e|
| 10.0.31 Sürüm 2 | 3 Mart 2023 | 13 Mart 2023'ten 15 Nisan 2023'e|
| 10.0.31 Sürüm 3 | 14 Nisan 2023 | 24 Nisan 2023'ten 27 Mayıs 2023'e|
| 10.0.32 Sürüm 1 | 31 Mart 2023 | 10 Nisan 2023'ten 13 Mayıs 2023'e|
| 10.0.32 Sürüm 2 | 28 Nisan 2023 | 8 Mayıs 2023'ten 10 Haziran 2023'e|
| 10.0.32 Sürüm 3 | 26 Mayıs 2023 | 5 Haziran 2023'ten 8 Temmuz 2023'e|
| 10.0.33 Sürüm 1 | 28 Nisan 2023 | 8 Mayıs 2023'ten 10 Haziran 2023'e|
| 10.0.33 Sürüm 2 | 26 Mayıs 2023 | 5 Haziran 2023'ten 8 Temmuz 2023'e|
| 10.0.33 Sürüm 3 | 14 Temmuz 2023 | 24 Temmuz 2023'ten 26 Ağustos 2023'e|
| 10.0.34 Sürüm 1 | 23 Haziran 2023 | 3 Temmuz 2023'ten 5 Ağustos 2023'e|
| 10.0.34 Sürüm 2 | 21 Temmuz 2023 | 31 Temmuz 2023'ten 2 Eylül 2023'e|
| 10.0.34 Sürüm 3 | 1 Eylül 2023 | 11 Eylül 2023'ten 14 Ekim 2023'e|
| 10.0.35 Sürüm 1 | 28 Temmuz 2023 | 7 Ağustos 2023'ten 9 Eylül 2023'e|
| 10.0.35 Sürüm 2 | 25 Ağustos 2023 | 4 Eylül 2023'ten 7 Ekim 2023'e|
| 10.0.35 Sürüm 3 | 20 Ekim 2023 | 30 Ekim 2023'ten 16 Aralık 2023'e|
| 10.0.36 Sürüm 1 | 29 Eylül 2023 | 9 Ekim 2023'ten 11 Kasım 2023'e|
| 10.0.36 Sürüm 2 | 27 Ekim 2023 | 6 Kasım 2023'ten 16 Aralık 2023'e|
| 10.0.36 Sürüm 3 | 12 Ocak 2024 | 22 Ocak 2023'ten 24 Şubat 2024'e|
| 10.0.37 Sürüm 1 | 3 Kasım 2023 | 13 Kasım 2023'ten 6 Ocak 2024'e|
| 10.0.37 Sürüm 2 | 30 Aralık 2023 | 8 Ocak 2024'ten 10 Şubat 2024'e|
| 10.0.37 Sürüm 3 | 27 Ocak 2024 | 5 Şubat 2024'ten 9 Mart 2024'e|
| 10.0.37 Sürüm 4 | 23 Şubat 2024 | 4 Mart 2024'ten 6 Nisan 2024'e|

### <a name="proactive-quality-update-upcoming-10030-release-2-train-schedule"></a><a name="schedule"></a> Yaklaşan kalite güncelleştirmesi 10.0.30 Sürüm 2 tren zamanlaması
**Uygulama sürümü: 10.0.1362.99**

| İstasyonlar | Yaklaşan Korumalı Alan Zamanlaması | Gelen üretim zamanlaması |
|---|---|---|
| 1. İstasyon | NA | NA |
| 2. İstasyon | 2 Ocak'tan 5 Ocak 2023'e | 21 Ocak'tan 22 Ocak 2023'e |
| 3. İstasyon | 3 Ocak'tan 6 Ocak 2023'e | 28 Ocak'tan 29 Ocak 2023'e |
| 4. İstasyon | 9 Ocak'tan 12 Ocak 2023'e | NA |
| 5. İstasyon | 16 Ocak'tan 19 Ocak 2023'e | NA |
| 6. İstasyon | NA | NA |

> [!IMPORTANT] 
> Microsoft, beş gün öncesinde önceki zamanlamayı güncelleştirecek ve kalite güncelleştirmelerini almak üzere zamanlanan ortamlara bir bildirim gönderecektir. Önceki zamanlama, yalnızca yaklaşan güncelleştirmeyle ilgili bildirim almış ortamlar için geçerlidir. Her bölgenin aktif olunmayan saatleri hakkında bilgi için bkz. [Bölgeye göre planlanmış bakım süreleri nelerdir?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
>
> Kalite güncelleştirmesinin kullanıma sunulmak üzere zamanlandığı bölge grubu veya *istasyon* için zamanlama dört günlük bir aralığı gösterir. Kalite güncelleştirmeleri, yalnızca korumalı alan ortamlarıyla başlayacaktır. Sonrasında başarıyla dağıtım yapılan korumalı alan yüzdesi arttıkça müşterilere önceden bildirim ile üretim ortamlarına dağıtım başlayacaktır.
> 
> Kalite güncelleştirmeleri, her zaman zamanlama başına ortam kümesini hedefleyerek ve istasyon için dördüncü günün sonuna kadar tüm kümeleri tamamlamamıza olanak verecek şekilde gerçekleştirilir. Ancak, bu ortam güncelleştirmesinin dört güne yayılacağı anlamına gelmez. Yalnızca, dört günlük süre içerisinde hangi ortam kümesinin hangi günde güncelleştirileceğini önceden belirleyemeyeceğiniz anlamına gelir. Tüm güncelleştirmeler, sıfıra yakın kesintiyle aktif olunmayan saatlerde yapılacaktır. Güncelleştirmeler, kesinlikle bölgenin aktif olunmayan saatleri içerisinde sona erecektir.

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Bir finans ve operasyon uygulamaları örneğine sahip olan ancak birden çok saat diliminde etkin olan müşteriler için aktif olunmayan saatler nasıl işlenir? 
Bir finans ve operasyon uygulamaları örneğinin bulunduğu aktif olunmayan saatler dışında özel bir zamanlama yoktur çünkü kalite güncelleştirmelerini [nZDT](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean) ile minimum düzeyde yıkıcı bir şekilde sunmayı planlıyoruz.

## <a name="what-is-the-current-rollout-cadence-for-proactive-quality-updates"></a>Proaktif kalite güncelleştirmeleri için mevcut kullanıma sunum takvimi nedir?
Proaktif kalite güncelleştirmeleri (PQUs), hizmet güncelleştirmesinin desteklenen her sürümü için ayda bir kere sevk edilir. Müşteriler yeni bir servis güncelleştirme sürümüne taşınmadıkça seçili korumalı alan ortamları için ayda tek güncelleştirme yapılır. Bu durumda, yeni servis güncelleştirmesi için varolan bir sıranın parçası olarak önceden zamanlanmış bir proaktif kalite güncelleştirmesi alabilirler. Güncelleştirmelerin sıklığı, dünya genelinde dağıtım tamamlandıktan sonra 2023 yılında artacaktır. Sevk takviminde değişiklik olduğunda en az bir ay öncesinden bildirim alacaksınız.

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Microsoft bu güncelleştirmelerin kalitesini nasıl sağlayacak?
Microsoft, doğrulama maliyetini düşük tutmak için yayın işlem hattını küçük yükler sunacak kadar verimli tutmaya çalışır. Kalite güncelleştirmesindeki her düzeltme, kaliteyi ve güvenilirliği artırmaya yardımcı olan ve böylece müşteriye etkiyi azaltan titiz ve güvenli bir dağıtım sürecinden geçer. Dağıtım, önce korumalı alan ortamlarında, ardından üretim aşamalarında gerçekleşir. Aşamalı dağıtımlar, daha fazla dağıtımın güvenli olup olmadığını belirlemek için uygun izlemeyi sağlar. Dağıtılan her bir müşteri grubuyla ilgili sorunlar tespit edilirse dağıtımı durdururuz ve kullanıma sunmadaki her adımın sorunların ortaya çıkması için yeterli zamana sahip olmasını sağlayacağız. Yaklaşan her kalite güncelleştirmesi için müşterilerin önceden plan yapabilmesi amacıyla, genel belgelerde ve e-postalarda yapılan güncelleştirmeler aracılığıyla zamanlamaya görünürlük sağlayacağız.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Müşteriler bir kalite güncelleştirmesini geciktirebilir, yeniden zamanlayabilir veya duraklatabilir mi?
Hayır. Kalite güncellemelerinin temel amacı, müşterilerimiz için güvenlik, gizlilik, güvenilirlik, kullanılabilirlik ve performans gibi temel ilkelerin sürekli olarak geliştirilmesini sağlamaktır. Bir güncelleştirmenin geciktirilmesi veya duraklatılması durumunda güvenlik, kullanılabilirlik ve güvenilirlik risk altında olur.

## <a name="how-do-i-know-what-set-of-changes-went-into-a-quality-update-payload"></a>Kalite güncelleştirme yüküne giren değişiklikler kümesini nasıl belirlerim?
Kalite güncelleştirme yükünde bulunan değişikliklerin listesini belirlemek için aşağıdaki adımları izleyin. 

10.0.28 Kalite Güncelleştirmesi eğitimi ve ilgili Uygulama sürümü 10.0.1265.89'u kullanın.

1. Lifecycle Services'te korumalı alanınızın **Ortam ayrıntıları** sayfasını açın. 
2. **Kullanılabilir Güncelleştirmeler** bölümünde en son kalite güncelleştirme derlemesi için **Görünümü Güncelleştir** seçeneğini belirleyin. 
3. Derlemeyi CSV veya Microsoft Excel dosyasına dışarı aktarın.
4. Dışa aktarılan dosyada, 10.0.1265.89 derleme numarasından küçük veya ona eşit olan **Derleme sürümünü** seçin. Delta yükünü görebiliyor olmanız gerekir.
 
> [!NOTE]
> CSV veya Excel dosyasına dışarı aktarma işlemi, ortam güncelleştirilmeden önce yapılmalıdır. Aksi durumda, güncelleştirme yüklü olmayan ve benzer yapılandırmaya sahip bir ortam kullanabilir ve yukarıdaki adımları izleyebilirsiniz.

[![Kalite güncelleştirmesi olan ortam örneği.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Kalite güncelleştirmesinden sonra kritik bir sorun bulunursa süreç nasıl ilerler?
Kritik bir sorun veya gerileme, genellikle birden fazla müşterinin hizmetlerimizden bir veya daha fazlasında düşük bir deneyime sahip olmasına neden olan bir veya daha fazla olaydır. Bu sorunlar, kullanılamama, performans düşüşü ve hizmet yönetimine müdahale dahil olmak üzere planlanmamış kesinti sürelerine neden olabilir. Bu tür gerilemeler nedeniyle müşteriler üzerinde kapsamlı bir etki varsa sorunu iletip düzeltene kadar kalite güncelleştirmesinin kullanıma sunulmasını durdururuz. Genellikle, bir sonraki kalite güncelleştirmesinin kullanıma sunulmaya devam etmesi için gerekli düzeltme yapılmış olacaktır.

Tek bir müşteri ortamı etkilenirse destek talebi açmak için Microsoft desteğine başvurun. Gerekçeye bağlı olarak, sorun giderilene kadar kalite güncelleştirmesinin söz konusu projedeki diğer tüm ortamlara sunulmasını durduracağız.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lifecycle-services"></a>Müşteriler Lifecycle Services'ten düzeltme güncelleştirmelerini el ile uygulamaya devam edebilir mi?
Evet. Düzeltmelerin çalışma şekliyle sürekli eşliğini sağlamak için düzeltme güncelleştirmeleri Lifecycle Services'teki müşteri ortamlarına uygulanmaya devam edebilir. Ancak, kalite güncelleştirmesinin bir parçası olarak dağıtılan düzeltmelerin, güncelleştirme dağıtılmadan önce standart SDP'den geçtiğini unutmayın. Bu durum, daha yüksek kalite nedeniyle gerileme riskini azaltır. Daha fazla güvenilirlik için düzeltmeleri el ile uygulamak yerine bir kalite güncelleştirmesi seçmenizi öneririz.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Müşteriler, kalite güncelleştirmesi derlemesini proaktif olarak zamanlamadan önce yükleyebilir mi?
Evet. Bir kalite güncellemesini proaktif olarak yükleyebilirsiniz. Microsoft, ortamın geçerli derleme sürümü söz konusu kalite güncelleştirmesine eşit veya daha yüksekse güncelleştirmeyi atlar.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Bir ortamın bir hafta içinde yaklaşan zamanlanmış bir aylık hizmet güncelleştirmesi varsa kalite güncelleştirmelerini almaya devam eder mi?
- Kalite güncelleştirmesinin gerçekleşmesinin planlandığı tarihten itibaren bir hafta içinde zamanlanmış yaklaşan bir hizmet güncelleştirmesi varsa kalite güncelleştirmeleri üretim ortamlarına uygulanmaz.
- Bir korumalı alan ortamı, yaklaşmakta olan kalite güncelleştirmesiyle aynı veya daha yüksek derleme sürümüne sahipse bu sürüm atlanır.
- Bir üretim ortamı, yaklaşmakta olan kalite güncelleştirmesiyle aynı veya daha yüksek derleme sürümüne sahipse bu sürüm atlanır.
- Bir korumalı alan, kalite güncelleştirmesi veya üretim ortamına el ile güncelleştirme nedeniyle aynı veya daha yüksek derleme sürümüne sahipse üretim aylık hizmet güncelleştirmesinin zamanlanmış sürümünü almaya devam eder. Zamanlanan üretim ortamının hizmet güncelleştirme sürümüne güncelleştirilmesini istemiyorsanız Lifecycle Services'ten hizmet güncelleştirmesini duraklatabilirsiniz. 
- Daha iyi kararlılık ve sonuçlar için yaklaşan bir hizmet güncelleştirmesi için değişikliklerinizi test etmek üzere en son kalite güncelleştirme derlemesini kullanmanızı öneririz.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Bir ortamda yaklaşan planlanan bir eylem ve aynı bakım aralığında zamanlanmış bir kalite güncelleştirmesi varsa yine de kalite güncelleştirmesi alınacak mı?
Önceden zamanlanmış bir eylemle (belirli bir noktaya geri yüklemeye (PITR) gibi) çakışma varsa kalite güncelleştirmesi, dört günlük aralık içerisinde uygun bir sonraki bakım aralığına zamanlanır. Zamanlama ile ilgili daha fazla ayrıntı için bkz. [Proaktif kalite güncelleştirmeleri zamanlaması nedir?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kalite güncelleştirmesi uygulandıktan sonra sorunlar yaşanırsa ortam önceki durumuna geri getirilebilir mi?
Kalite güncelleştirmesi uygulandıktan sonra, hiçbir koşulda geri alma işlemi yapılmaz. Sorunları azaltmak için yalnızca düzeltme eki iletme seçenekleri vardır.

## <a name="what-about-fda-regulation-and-gxp"></a>FDA yönetmeliği ve GxP ile ilgili durum nedir?
FDA doğrulaması ve düzenlemesine tabi müşteriler için plan değişikliği yapılmaya devam etmektedir. Yakında bu alanda daha fazla güncelleştirme bekliyoruz. Şimdilik, bu tür tüm müşteriler kalite güncelleştirmelerinden muaftır. Müşterinin FDA düzenlemelerine tabi olduğundan emin olmak için lütfen [Microsoft Azure GxP Teklifi](/azure/compliance/offerings/offering-gxp)'ni ziyaret edin.

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Bu kalite güncelleştirmeleri için hizmet güncelleştirmelerinin hangi sürümleri desteklenir?
Hizmet güncelleştirmelerinin desteklenen sürümlerini kullanan müşteriler, kalite güncelleştirmelerini alabilir. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retail-sdk"></a>Perakende bileşenlere sahip finans ve operasyon uygulamaları dağıtımları genellikle MPOS'u yeniden dağıtmak zorunda kalmanın yanı sıra ek çalışma gerektirir. Bu kalite güncelleştirmeleri Retail SDK'yı nasıl etkileyecek? 
Kalite güncelleştirmeleri yükünde düzeltmenin yapısı değişmediğinden, şu anda özellikle perakende bileşenleriyle ilgili herhangi bir ek etki beklemiyoruz.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Bulutta Barındırılan Ortamlar (CHE) üzerinde herhangi bir etkisi var mı? 
Microsoft'un alanı dışında kalması nedeniyle CHE ortamları bazı kalite güncelleştirmelerinin kapsamı dışındadır.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Microsoft Dataverse ile herhangi bir tümleştirme sorunu var mı? 
Kalite güncelleştirmeleri ile ilgili olarak Dataverse ile bilinen bir tümleştirme sorunu bulunmamaktadır.

