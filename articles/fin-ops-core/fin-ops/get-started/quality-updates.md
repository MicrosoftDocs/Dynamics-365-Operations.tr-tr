---
title: Proaktif kalite güncelleştirmeleri
description: Bu makale, kalite güncelleştirmelerinin proaktif olarak sunulmasına ilişkin bilgi sağlar.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338151"
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
- **Sürüm geri dönüşü**: Proaktif kalite güncelleştirmesinde tüm değişiklikleri gruplandırmak için sınırlı dağıtım kullanılacaktır. Proaktif bir dağıtımdan sonra geri dönüş gerekiyorsa bu, sınırlı dağıtım sistemi üzerinden yapılabilir.
- **Korumalı alan eşitleme tanımı**: Günümüzde müşterilerin yüzde 20'sinden azı birden fazla korumalı alana sahiptir ve sorun gidermeye yardımcı olmak için bir korumalı alanı sürümün eşleştiği üretimde dağıtılmış olarak korurlar. Yakın bir tarihte, müşterilere proaktif kalite güncelleştirmesi dağıtımını diğer korumalı alanlarla birlikte değil bunun yerine daha sonra üretim ortamıyla birlikte alacak bir korumalı alan ortamı belirtme olanağı sunacağız. Bir müşteri, üretiminden daha yeni bir sürümü test etmek için bir korumalı alan kullanıyorsa, bu korumalı alanın kalite güncelleştirmelerini yeni sürüme alacağını unutmayın.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Proaktif kalite güncelleştirmeleri ne zaman başlayacak?

Korumalı alan ortamları için proaktif kalite güncelleştirmeleri dağıtımının Azure genel bulut müşterileri için en geç Eylül veya Ekim 2022'de başlaması beklenmektedir. Deneme ortamları da proaktif güncelleştirme dağıtımını o tarihlerde almaya başlayacaktır. Eylül ayında her müşteriye ortamları için beklenen planlamayı bildirmek üzere bir bildirim gönderilecektir. Proaktif olarak güncelleştirilen dağıtım işlemiyle ilgili özel durumlara yalnızca FDA düzenlemesine tabi müşteriler için izin verilecektir. Düzenlenmiş ortamlar ile bağımsız ve kamu bulut müşterilerinin nasıl yönetileceği üzerinde çalışmaya devam ediyoruz.

Sonraki altı aylık dönemde, tanımlanan tüm ortamlar eklenene kadar proaktif güncelleştirmeler alan korumalı alan ortamı yüzdesini kademeli olarak artıracağız ve üretim ortamlarını güncelleştirmeye geçeceğiz. Dönem boyunca, dağıtım işleminin sorunsuz olmasını sağlamak ve kesintiye neden olmayan yükler hedefimizi yakalamak için izlemede olacağız.

Müşteriler düzenli olarak daha küçük yükler alacağından, güncel kalma sürecinin daha kolay hale geleceğini bekliyoruz. Süreci kesintisiz yürütme yeteneğini gösterdiğimizde güncelleştirme dağıtımının sıklığını ayarlayacağız. Bu süreç Dataverse platformumuz ve uygulamalarımız için zaten etkili şekilde çalışıyor ve hizmet kalitesinde beklenen iyileştirmeleri sunuyor. Finans ve operasyon uygulamaları için de aynı adımı atmak istiyoruz.
