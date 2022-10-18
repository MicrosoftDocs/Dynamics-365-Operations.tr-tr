---
title: Proaktif kalite güncelleştirmeleri
description: Bu makale, kalite güncelleştirmelerinin proaktif olarak sunulmasına ilişkin bilgi sağlar.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 25306a8ccebb5cd01debc90cf497d4a942840ef4
ms.sourcegitcommit: 43a0fb019bc67c00c39c2778343ba89924c3322c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2022
ms.locfileid: "9671438"
---
# <a name="proactive-quality-updates"></a>Proaktif kalite güncelleştirmeleri

[!include[banner](../includes/banner.md)]

Son yedi yıl boyunca Microsoft [Bir Sürüm ](../../dev-itpro/lifecycle-services/oneversion-overview.md) olarak adlandırdığımız şey üzerinde sürekli olarak ilerleme gerçekleştirdi. Bir Sürüm önermesi basittir: tüm müşterileri aynı yazılım sürümünde olmasını sağlamaya ne kadar yakın olursak o kadar yüksek kalite sunabiliriz. Sorunları bir kerede bulup çözer ve çözümleri müşterilerimize çok daha hızlı sunarız.

Bu önerme şu sonuçlarla onaylanmıştır: ürünlerimizde daha düşük olay sayısı. Müşteriler aynı sürümde olmadığında, sürekli olarak zaten bir çözümü bulunan sorunlardan etkilendiklerini görüyoruz. Dynamics 365 Finance, Dynamics 365 Supply Chain, Dynamics 365 Project Operations ve Dynamics 365 Commerce için büyük bir ilerleme kaydettik ve son teknik gelişmeler sayesinde artık sonraki adıma geçebiliriz. Aşağıdaki bilgiler neler yapacağımızı, aşamayı ayarlamak için neler yapmış olduğumuzu ve yeni özellikleri kesinti olmadan ne zaman sunacağımızı açıklamaktadır.

## <a name="focus-on-quality-updates"></a>Kalite güncelleştirmelerine odaklanma

Şu anda yılda yedi [hizmet güncelleştirmesi](public-preview-releases.md) sunuyoruz. Örneğin, 10.0.29 sürümü bir hizmet güncelleştirmesidir. Son güncelleştirmeye kadar yıl başına sekiz güncelleştirme vardı. Ancak, takvim yılının sonunda yapılan değişikliklerden kaçınmaya yönelik bir isteği ortaya çıkaran müşteri geribildirimlerine yanıt olarak bir güncelleştirmeyi bıraktık.

Hizmet güncelleştirmelerinin temposunu değiştirmeyeceğiz. Bunun yerine, Bir Sürüm yolculuğundaki sonraki adımımız *kalite güncelleştirmelerine* odaklanmak. Kalite güncelleştirmeleri, toplu düzeltme derlemeleridir. Yeni özellikler içermezler. Herhangi bir anda, tüm müşteri topluluğumuz üç veya dört son hizmet güncelleştirmesi arasında dağıtılır. Ancak, herhangi bir hizmet güncelleştirmesi için, kişilere dağıtım yapıldığı tarihe bağlı olarak grup içinde onlarca farklı kalite güncelleştirmesi sürümü kullanılabilir. Sonraki adımımızda, kalite güncelleştirmelerini proaktif olarak yayınlayacağız. Bu modeli zaten Dataverse tabanlı uygulamalarımız zaten kullanyoruz ve kalitenin artması ve destek olaylarının azalması yönünde beklenen sonuçları gördük.

Elbette, hataların azaltılması kalite güncelleştirmelerine duyulan gereksinimi azaltabilir veya tamamen ortadan kaldırabilir. Kalite güncelleştirmeleri gerekitren hataları azaltmaya yönelik yürütülen birçok girişimimiz var. Kalite güncelleştirmesinde yük azaltıldığında bile müşteri tabanındaki tutarlılık desteklenebilme, müşterilere daha hızlı geliştirmeler sağlama ve müşterilerin zaten çözümleri bulunan sorunlarla karşılaşma sıklığını iyileştirecektir.

## <a name="making-proactive-distribution-possible"></a>Proaktif dağıtımı mümkün hale getirme

Kalite güncelleştirmelerinin proaktif şekilde teslim edilmesini sağlayan birden fazla gelişme zaten dağıtıldı:

- **Sıfıra yakın kesinti güncelleştirmesi**: Daha sık kullanılan ortamlara gönderim yapmak için, Dynamics 365 Hizmet Düzeyi Sözleşmlerini (SLA'ları) korumak açısından ortam kullanılabilirliği üzerindeki etkinin azaltılması temeldir. Sıfıra yakın kesinti güncelleştirmesi, başlangıçta güncelleştirilen görüntüyü minimum kesintiyle etkinleştirmek için yük devretme kümesi kullanarak aylık işletim sistemi düzeltme eki uygulamasını geliştirmek amacıyla sunulmuştur. Güncelleştirmeleri uygulama mekanizması daha az kesintiye uğramasını sağlayacak şekilde geliştirilmiştir ve hem işletim sistemi düzeltme eki uygulamasını hem de kalite güncelleştirmesi dağıtımını kapsar.

    Etkileşimli kullanıcılar için, etkin bir oturum yarıda kesilebilir ve yeniden deneme şimdi güncelleştirilmiş ortama gider. Şu anda kullanmayı tercih etme esasıyla sunulan [Öncelik temelli toplu iş planlamanın](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) kullanıma sunulmasıyla toplu iş planlama ve işleme kurtarır ve güncelleştirmeden hemen sonra sürdürülür. Öncelik temelli toplu iş planlama, müşterilere üretim ortamları için proaktif kalite güncelleştirmeleri dağıtımına katılmaya başlamadan önce gerçekleştirilecektir.

- **Karanlık saatler**: Karanlık saatler her Azure bölgesi için tanımlanmıştır ve neredeyse sıfır kesinti süresi güncelleştirmeleri karanlık saat döneminde gerçekleştirilecektir.

## <a name="the-proactive-update-process"></a>Proaktif güncelleştirme işlemi

Proaktif kalite güncelleştirmeleri dağıtımı, güvenli bir dağıtım işlemini (SDP) izleyecektir. SDP özellikleri geliştirilecektir ancak kalite güncelleştirmeleri öncelikle korumalı alan ortamlarına dağıtılacaktır. Süreç, erken dağıtım için kabul edilen ortamlarla başlayacaktır. Başarıyla dağıtım yapılan korumalı alanların yüzdesi arttıkça, üretim ortamlarına dağıtım süreci başlayacaktır. Tekrar belirtirmek isteriz ki süreç erken dağıtım için kabul edilen ortamlarla başlayacaktır. Dinleme sistemleri, sistem telemetrisini ve canlı site olaylarını izleyecek ve herhangi bir gerileme algılanırsa belirli bir sürümün dağıtımızını durduracaktır. Müşteriler yine de istemeleri durumunda kalite güncelleştirmelerini proaktif dağıtımdan önce çekebilecektir.

Geçerli sürüm yönetimi verileri, kalite güncelleştirmelerinde gerilemelerin yüzde 3'ten azının sunulduğunu göstermektedir. Gerilemeyi ortadan ve geliştirilmiş bir SDP'ye odaklanmanın artırılamasıyla gerilemelerin olası etkisi, müşterilere genel olarak dağıtılmış düzeltmelerle elde edilen kalite kazançlarına göre önemli ölçüde daha düşük olacaktır.

## <a name="process-changes"></a>Değişiklikleri işle

Proaktif kalite güncelleştirme dağıtımının etkinleştirilmesinin ötesinde bir dizi süreç değişikliği zaten uygulanmaktadır:

- **Şema**: Araç, kalite güncelleştirme derlemelerinin yalnızca hizmet çevrimiçi olduğunda uygulanabilen şema değişikliklerini içermesini sağlayacaktır. Bu yaklaşım, güncelleştirmeyi sıfır kesinti süresiyle uygulama yeteneğini korumanıza yardımcı olur.
- **Artırılmış değişiklik incelemesi**: Şu anda zaten değişikliklerin kalite güncelleştirmesine eklenmesini onaylamaya yönelik ekstra bir süreç adımı bulunmaktadır. Ekstra adımdaki inceleme gerileme potansiyeli azaltmaya yardımcı olmak amacıyla artırılacaktır. Kalite güncelleştirmelerinde hataya neden olan değişikliklere izin verilmez ve artırılmış değişiklik incelemesi bu hedefe ulaşmaya yardımcı olacaktır.
- **Görünürlük**: Gelecekteki proaktif kalite güncelleştirmeleri için bildirimleri e-posta ve Lifecycle Services (LCS) aracılığıyla göndereceğiz. Ek olarak, destek takımları ve olay liderleri, kalite güncelleştirmelerinin proaktif olarak dağıtıldığı yerler için görünebilirliğe sahip olacaktır.
- **Dağıtım yoluyla Fail Safe** – Dağıtım, bir kalite güncellemesi hata düzeltmesinde uygun olan yerlerde kod değişikliklerini korumak için kullanılır veya düzeltmeyle ilgili mevcut özellik uçuşunu kullanır. Proaktif bir dağıtımdan sonra bir geri dönüş veya değişikliğin kapatılması gerekiyorsa daha fazla başarısızlık oluşmaması için dağıtma sistemi üzerinden yapılabilir.
- **Korumalı alan eşitleme tanımı**: Günümüzde müşterilerin yüzde 20'sinden azı birden fazla korumalı alana sahiptir ve sorun gidermeye yardımcı olmak için bir korumalı alanı sürümün eşleştiği üretimde dağıtılmış olarak korurlar. Bir müşteri, üretiminden daha yeni bir sürümü test etmek için korumalı alan kullanıyorsa bu korumalı alan yeni sürüme yönelik kalite güncelleştirmelerini alır.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Kalite güncelleştirmeleri için kullanıma sunma yol haritası nedir?

Korumalı alan ortamları için proaktif kalite güncelleştirmeleri dağıtımının Azure genel bulut müşterileri için en geç Eylül veya Ekim 2022'de başlaması beklenmektedir. Deneme ortamları da proaktif güncelleştirme dağıtımını o tarihlerde almaya başlayacaktır. Eylül ayında her müşteriye ortamları için beklenen planlamayı bildirmek üzere bir bildirim gönderilecektir. Proaktif olarak güncelleştirilen dağıtım işlemiyle ilgili özel durumlara yalnızca FDA düzenlemesine tabi müşteriler için izin verilecektir. Düzenlenmiş ortamlar ile bağımsız ve kamu bulut müşterilerinin nasıl yönetileceği üzerinde çalışmaya devam ediyoruz.

Sonraki altı aylık dönemde, tanımlanan tüm ortamlar eklenene kadar proaktif güncelleştirmeler alan korumalı alan ortamı yüzdesini kademeli olarak artıracağız ve üretim ortamlarını güncelleştirmeye geçeceğiz. Dönem boyunca, dağıtım işleminin sorunsuz olmasını sağlamak ve kesintiye neden olmayan yükler hedefimizi yakalamak için izlemede olacağız.

Müşteriler düzenli olarak daha küçük yükler alacağından, güncel kalma sürecinin daha kolay hale geleceğini bekliyoruz. Süreci kesintisiz yürütme yeteneğini gösterdiğimizde güncelleştirme dağıtımının sıklığını ayarlayacağız. Bu süreç Dataverse platformumuz ve uygulamalarımız için zaten etkili şekilde çalışıyor ve hizmet kalitesinde beklenen iyileştirmeleri sunuyor. Finans ve operasyon uygulamaları için de aynı adımı atmak istiyoruz.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Üretim ortamları için kalite güncelleştirmeleri ne zaman başlayacak?
Şu anda, kalite güncellemeleri yalnızca korumalı alanları hedeflemektedir. Üretim için hazır olma durumunu ölçmek amacıyla korumalı alanların proaktif güncelleştirmelerinden daha somut veriler ve ölçümler elde ettiğimizde, bu alanı üretim ortamları için bir başlangıç tarihi ile güncelleştireceğiz.

## <a name="what-is-the-schedule-for-sandbox-proactive-quality-updates"></a>Korumalı alan proaktif kalite güncelleştirmeleri için zamanlama nedir?
Her bölgenin aktif olunmayan saatleri hakkında bilgi için bkz. [Bölgeye göre planlanmış bakım süreleri nelerdir?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).

### <a name="proactive-quality-update-release-10028"></a>Proaktif kalite güncelleştirmesi sürümü: 10.0.28
**Uygulama sürümü: 10.0.1265.89**
**İlgili son BB makalesini: 745340**

| İstasyon | Bölgeler | Tamamlanmış Zamanlama| Yaklaşan Korumalı Alan Zamanlaması
|---|---|---|---|
| 1. İstasyon | Merkez Kanada, Doğu Kanada, Merkez Fransa, Merkez Hindistan, Doğu Norveç, Batı İsviçre | 15 Eylül ve 18 Eylül 2022 ile 19 Eylül ve 22 Eylül 2022 tarihleri arasında | 7 Ekim ile 10 Ekim 2022 tarihleri arasında |
| 2. İstasyon | Güney Fransa, Güney Hindistan, Batı Norveç, Kuzey İsviçre, Kuzey Güney Afrika, Doğu Avustralya, Güney Birleşik Krallık, Kuzey BAE, Doğu Japonya, Güneydoğu Avustralya, Güney Doğu Asya | 25 Eylül ile 28 Eylül 2022 tarihleri arasında | 7 Ekim ile 10 Ekim 2022 tarihleri arasında |
| 3. İstasyon | Doğu Asya, Batı Birleşik Krallık, Batı Japonya, Güney Brezilya, Batı Avrupa, Doğu ABD, Merkez BAE | 26 Eylül ile 29 Eylül 2022 tarihleri arasında | 7 Ekim ile 10 Ekim 2022 tarihleri arasında |
| 4. İstasyon | Kuzey Avrupa, Orta ABD, Batı ABD | 28 Eylül ile 1 Ekim 2022 tarihleri arasında | 7 Ekim ile 10 Ekim 2022 tarihleri arasında |
| 5. İstasyon | DoD, Hükümet Topluluk Bulutu, Çin | Planlanmadı | Planlanmadı |

### <a name="proactive-quality-update-release-10029"></a><a name="schedule"></a>Proaktif kalite güncelleştirmesi sürümü: 10.0.29
**Uygulama sürümü: 10.0.1326.70**
**İlgili son BB makalesini: 748926**

| İstasyon | Bölgeler | Yaklaşan Korumalı Alan Zamanlaması
|---|---|---|
| 1. İstasyon | Merkez Kanada, Doğu Kanada, Merkez Fransa, Merkez Hindistan, Doğu Norveç, Batı İsviçre | 14 Ekim ile 17 Ekim 2022 tarihleri arasında |
| 2. İstasyon | Güney Fransa, Güney Hindistan, Batı Norveç, Kuzey İsviçre, Kuzey Güney Afrika, Doğu Avustralya, Güney Birleşik Krallık, Kuzey BAE, Doğu Japonya, Güneydoğu Avustralya, Güney Doğu Asya | 15 Ekim ile 18 Ekim 2022 tarihleri arasında |
| 3. İstasyon | Doğu Asya, Batı Birleşik Krallık, Batı Japonya, Güney Brezilya, Batı Avrupa, Doğu ABD, Merkez BAE | 16 Ekim ile 19 Ekim 2022 tarihleri arasında |
| 4. İstasyon | Kuzey Avrupa, Orta ABD, Batı ABD | 17 Ekim ile 20 Ekim 2022 tarihleri arasında |
| 5. İstasyon | DoD, Hükümet Topluluk Bulutu, Çin | Planlanmadı |

> [!IMPORTANT] 
> Microsoft, beş gün öncesinde önceki zamanlamayı güncelleştirecek ve kalite güncelleştirmelerini almak üzere zamanlanan ortamlara e-posta bildirimi gönderecektir. Önceki zamanlama, yalnızca yaklaşan güncelleştirmeyle ilgili bildirim almış ortamlar için geçerlidir. Her bölgenin aktif olunmayan saatleri hakkında bilgi için bkz. [Bölgeye göre planlanmış bakım süreleri nelerdir?](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#windows).
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
Kalite güncelleştirme yükünde bulunan değişikliklerin listesini belirlemek amacıyla daha iyi bir çözüm sunmak için çalışmaya devam ediyoruz. Bu süreçte, aşağıdaki adımlar geçici çözüm niteliğindedir. 

10.0.28 kalite güncelleştirmesi dizisi ve ilgili uygulama sürümü 10.0.1265.89 için BB# 745340 kullanın.

1. LCS'de korumalı alanınızın **Ortam ayrıntıları** sayfasını açın. 
2. **Kullanılabilir Güncelleştirmeler** bölümünde en son kalite güncelleştirme derlemesi için **Görünümü Güncelleştir** seçeneğini belirleyin. 
3. Derlemeyi CSV veya Microsoft Excel dosyasına dışarı aktarın.
4. Dışa aktarılan dosyada bilgileri zamana göre sıralayın (önce en eski) ve sonra **Kimliği güncelleştir** sütununda BB 745340 numarasını arayın. BB delta listesini görebiliyor olmanız gerekir.
 
 > [!NOTE]
 > CSV veya Excel dosyasına dışarı aktarma işlemi, ortam güncelleştirilmeden önce yapılmalıdır. Aksi durumda, güncelleştirme yüklü olmayan ve benzer yapılandırmaya sahip bir ortam kullanabilir ve yukarıdaki adımları izleyebilirsiniz.

[![Kalite güncelleştirmesi olan ortam örneği.](./media/how-to-get-kb-list-pqu.png)](./media/how-to-get-kb-list-pqu.png)

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Kalite güncelleştirmesinden sonra kritik bir sorun bulunursa süreç nasıl ilerler?
Kritik bir sorun veya gerileme, genellikle birden fazla müşterinin hizmetlerimizden bir veya daha fazlasında düşük bir deneyime sahip olmasına neden olan bir veya daha fazla olaydır. Bu sorunlar, kullanılamama, performans düşüşü ve hizmet yönetimine müdahale dahil olmak üzere planlanmamış kesinti sürelerine neden olabilir. Bu tür gerilemeler nedeniyle müşteriler üzerinde kapsamlı bir etki varsa sorunu iletip düzeltene kadar kalite güncelleştirmesinin kullanıma sunulmasını durdururuz. Genellikle, bir sonraki kalite güncelleştirmesinin kullanıma sunulmaya devam etmesi için gerekli düzeltme yapılmış olacaktır.

Tek bir müşteri ortamı etkilenirse destek talebi açmak için Microsoft desteğine başvurun. Gerekçeye bağlı olarak, sorun giderilene kadar kalite güncelleştirmesinin söz konusu projedeki diğer tüm ortamlara sunulmasını durduracağız.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Müşteriler LCS'den düzeltme güncelleştirmelerini el ile uygulamaya devam edebilir mi?
Evet. Düzeltmelerin çalışma şekliyle sürekli eşliğini sağlamak için düzeltme güncelleştirmeleri LCS'deki müşteri ortamlarına uygulanmaya devam edebilir. Ancak, kalite güncelleştirmesinin bir parçası olarak dağıtılan düzeltmelerin, güncelleştirme dağıtılmadan önce standart SDP'den geçtiğini unutmayın. Bu durum, daha yüksek kalite nedeniyle gerileme riskini azaltır. Daha fazla güvenilirlik için düzeltmeleri el ile uygulamak yerine bir kalite güncelleştirmesi seçmenizi öneririz.

## <a name="can-customers-proactively-install-a-quality-update-build-ahead-of-the-schedule"></a>Müşteriler, kalite güncelleştirmesi derlemesini proaktif olarak zamanlamadan önce yükleyebilir mi?
Evet. Bir kalite güncellemesini proaktif olarak yükleyebilirsiniz. Microsoft, ortamın geçerli derleme sürümü söz konusu kalite güncelleştirmesine eşit veya daha yüksekse güncelleştirmeyi atlar.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Bir ortamın bir hafta içinde yaklaşan zamanlanmış bir aylık hizmet güncelleştirmesi varsa kalite güncelleştirmelerini almaya devam eder mi?
- Kalite güncelleştirmesinin gerçekleşmesinin planlandığı tarihten itibaren bir hafta içinde zamanlanmış yaklaşan bir hizmet güncelleştirmesi varsa kalite güncelleştirmeleri üretim ortamlarına uygulanmaz.
- Bir korumalı alan ortamı, yaklaşmakta olan kalite güncelleştirmesiyle aynı veya daha yüksek derleme sürümüne sahipse bu sürüm atlanır.
- Bir üretim ortamı, yaklaşmakta olan kalite güncelleştirmesiyle aynı veya daha yüksek derleme sürümüne sahipse bu sürüm atlanır.
- Bir korumalı alan, kalite güncelleştirmesi veya üretim ortamına el ile güncelleştirme nedeniyle aynı veya daha yüksek derleme sürümüne sahipse üretim aylık hizmet güncelleştirmesinin zamanlanmış sürümünü almaya devam eder. Zamanlanan üretim ortamının hizmet güncelleştirme sürümüne güncelleştirilmesini istemiyorsanız LCS'den hizmet güncelleştirmesini duraklatabilirsiniz. 
- Daha iyi kararlılık ve sonuçlar için yaklaşan bir hizmet güncelleştirmesi için değişikliklerinizi test etmek üzere en son kalite güncelleştirme derlemesini kullanmanızı öneririz.

## <a name="if-an-environment-has-an-upcoming-scheduled-action-and-a-scheduled-quality-update-in-the-same-maintenance-window-will-it-still-receive-the-quality-update"></a>Bir ortamda yaklaşan planlanan bir eylem ve aynı bakım aralığında zamanlanmış bir kalite güncelleştirmesi varsa yine de kalite güncelleştirmesi alınacak mı?
Önceden zamanlanmış bir eylemle (belirli bir noktaya geri yüklemeye (PITR) gibi) çakışma varsa kalite güncelleştirmesi, dört günlük aralık içerisinde uygun bir sonraki bakım aralığına zamanlanır. Zamanlama ile ilgili daha fazla ayrıntı için bkz. [Proaktif kalite güncelleştirmeleri zamanlaması nedir?](#schedule). 

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Kalite güncelleştirmesi uygulandıktan sonra sorunlar yaşanırsa ortam önceki durumuna geri getirilebilir mi?
Kalite güncelleştirmesi uygulandıktan sonra, hiçbir koşulda geri alma işlemi yapılmaz. Sorunları azaltmak için yalnızca düzeltme eki iletme seçenekleri vardır.

## <a name="what-about-fda-regulation-and-gpx"></a>FDA yönetmeliği ve GPX ile ilgili durum nedir?
FDA doğrulaması ve düzenlemesine tabi müşteriler için plan değişikliği yapılmaya devam etmektedir. Yakında bu alanda daha fazla güncelleştirme bekliyoruz. Şimdilik, bu tür tüm müşteriler kalite güncelleştirmelerinden muaftır. Müşterinin FDA düzenlemelerine tabi olduğundan emin olmak için lütfen [Microsoft Azure GPX Teklifi](/azure/compliance/offerings/offering-gxp)'ni ziyaret edin.

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Bu kalite güncelleştirmeleri için hizmet güncelleştirmelerinin hangi sürümleri desteklenir?
Hizmet güncelleştirmelerinin desteklenen sürümlerini kullanan müşteriler, kalite güncelleştirmelerini alabilir. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Perakende bileşenlere sahip finans ve operasyon uygulamaları dağıtımları genellikle MPOS'u yeniden dağıtmak zorunda kalmanın yanı sıra ek çalışma gerektirir. Bu kalite güncelleştirmeleri RetailSDK'yı nasıl etkileyecek? 
Kalite güncelleştirmeleri yükünde düzeltmenin yapısı değişmediğinden, şu anda özellikle perakende bileşenleriyle ilgili herhangi bir ek etki beklemiyoruz.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che"></a>Bulutta Barındırılan Ortamlar (CHE) üzerinde herhangi bir etkisi var mı? 
Microsoft'un alanı dışında kalması nedeniyle CHE ortamları bazı kalite güncelleştirmelerinin kapsamı dışındadır

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Microsoft Dataverse ile herhangi bir tümleştirme sorunu var mı? 
Kalite güncelleştirmeleri ile ilgili olarak Dataverse ile bilinen bir tümleştirme sorunu bulunmamaktadır.

