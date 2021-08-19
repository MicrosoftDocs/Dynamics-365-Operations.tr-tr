---
title: İş planlama çizelgeleme
description: Bu makale, operasyon planlamasından daha ayrıntılı bir planlama biçimi olan iş planlaması hakkında bilgi sağlar. İşleri veya mağaza siparişlerini tek tek programlamak ve üretim ortamını kontrol etmek için iş planlamayı kullanabilirsiniz.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc782a46f01464f2e0fea7eaf1d05a915bf735c7b4280676e45442af9440ae98
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717112"
---
# <a name="job-scheduling"></a>İş planlama çizelgeleme

[!include [banner](../includes/banner.md)]

Bu makale, operasyon planlamasından daha ayrıntılı bir planlama biçimi olan iş planlaması hakkında bilgi sağlar. İşleri veya mağaza siparişlerini tek tek programlamak ve üretim ortamını kontrol etmek için iş planlamayı kullanabilirsiniz.

İşleri veya mağaza siparişlerini tek tek programlamak ve üretim ortamını kontrol etmek için iş planlamayı kullanabilirsiniz. İş planlama her operasyonu tek tek görev veya işlerine böler. Bu işler daha sonra bunları gerçekleştirecek operasyon kaynaklarına atanır. İş planlama ayrıca seçilen iş tarafından referans alınan tüm işleri senkronize etmenizi sağlar. İş için başlangıç veya bitiş tarihi ve saati belirtebilir ve ardından planlamayı çalıştırabilirsiniz. Süre olarak, programlama yönüne bağlı olarak başlangıç zamanını veya bitiş zamanını tanımlayabilirsiniz. Bu işlev örneğin aynı anda makinede sadece bir işin yürütüldüğü veya her bir kaynak için yürütülen işi optimize etmek istediğinizde yararlı olacaktır.

## <a name="tasks-in-the-job-scheduling-process"></a>İş planlama sürecindeki görevler
İş planlama süreci şu görevleri içerir:

-   Operasyonları işlere bölün.
-   İşleri, ilgili operasyon için belirtilen kaynaklara yönelik tarihleri ve saatleri temel alarak planlayın.
-   Her iş için başlangıç ve bitiş zamanlarını hesaplayın. Zamanların birbiriyle çakışmayacağından emin olmak için sonlu kapasite kullanabilirsiniz.
-   Kaynak grubunda hangi kaynakların üzerinde işi çalıştıracağınızı belirtin. Bu görev, bir kaynak grubunun bir operasyon için belirtilmesini gerektirir. İş planlama, kaynakları veya kaynak gruplarını en kısa teslim süresine göre seçer ve ayrıca kaynaklarla ilgili önceden yapılmış rezervasyonları da dikkate alır.
-   İş planlama yürütürken operasyonları işlere dağıtın. İşler, üretim rotası tarafından belirtilen sıraya göre tarih ve saatler dikkate alınarak planlanır. Operasyon kurulumu, planlama süreci sırasında açılacak işleri belirler. Operasyona atanan rota grupları işlerin oluşturulup oluşturulmayacağını kontrol eder. Bir iş, yalnızca özel bir süresi olması koşuluyla oluşturulur. Örneğin, seçilen operasyon için bir taşıma süresi belirtilmişse bir taşıma süresi işi oluşturulacaktır.

## <a name="scheduling-direction"></a>İş planlama çizelgeleme yönü
İşleri ileriye veya geriye doğru planlayabilirsiniz.

-   **İleri** – Üretimi mümkün olduğu kadar erken bir aşamada başlatmak için ileri programlama yönünü kullanın. Üretim sürecinde üretim hızlı bir şekilde ileri doğru itildiğinden, bu yöntem itme yöntemi olarak da bilinir. Üretim mümkün olan en erken tarihlerde başlayacak ve bitecek şekilde planlanır.
-   **Geri** – Üretimi mümkün olduğu kadar geç bir aşamada başlatmak için geri programlama yönünü kullanın. Üretimin mutlaka tamamlanması gereken tarihe dayalı olduğundan bu yöntem çekme yöntemi olarak da bilinir. Geri programlama, hedef teslim süresi kaçırılmadan üretimin başlatılabileceği mümkün olan en geç tarihe doğru geri sayar.

## <a name="finite-capacity"></a>Sınırlı kapasite
İşleri sonlu kapasite kullanarak planlayabilirsiniz. Sonlu kapasite kullanıyorsanız planlanan kapasite, kaynaklar için mevcut olan kapasiteden daha fazla olamaz. Mevcut süre, kaynağın kullanılabilir olduğu ve kapasite üzerinde herhangi bir rezervasyonun bulunmadığı süre olarak tanımlanır. Sonlu kapasiteye dayalı planlama, belirli bir tarihe dayalı bir operasyon için başlangıç ve bitiş tarihlerinin çakışmamasını garanti eder. Halihazırda rezerve edilen kaynak kapasitesi ve ayrıca başlangıç süreleri ile bitiş süreleri arasındaki çakışmalar da dikkate alınır. Sonlu kapasite, bir kaynağın optimum ölçüde kullanılabilmesi için o kaynak için mutlaka kullanılabilir olması gereken kapasite miktarını belirler. Bu işlem, operasyonlar arasındaki en kısa teslim süresinin hesaplanmasıyla dengelenir.

## <a name="finite-materials"></a>Sonlu malzemeler
Sonlu malzemelere dayalı iş planlama, operasyon başladığında gerekli malzemelerin hazır olacağını garanti eder. Maddeler için kapsam kuralları bu sınırları tanımlar. Planlama, bileşen maddelerin ne zaman hazır olacağını belirlemek için gereksinim dağıtma işlevini kullanır. Sonlu malzemeler ayarlamadan planlama yaparsanız sistem tüm maddelerin gerektiği zamanlarda mevcut olduğunu ve olacağını kabul eder.

## <a name="finite-properties"></a>Sonlu özellikler
Özel özelliklere dayalı gerçekleştirilen iş planlama, özelliklerin üretim rotasına ilişkin operasyonlar için belirtilmesini gerektirir. Yedek kapasite sağlanması için bu özellikler karşılanmalıdır.

## <a name="references"></a>Referanslar
İş planlama, mevcut üretim tarafından yansıtılan tüm üretimlerini planlar. Bir üretimde bir veya birden çok alt üretimi varsa, bu alt üretimler ana üretimle aynı anda planlanmalıdır, çünkü ana üretim, ilgili alt üretimler tamamlanmadan başlatılamaz.

## <a name="schedule-resources"></a>Kaynakları planlama
Planlama motoru, gereksinimleri karşılayabilecek kombinasyonları belirlemek için kaynak kombinasyonlarını kontrol eder. **Planlama parametreleri** sayfasındaki **Temel kaynak seçimi** alanında bulunan, aşağıdaki değerlerden birini seçerek seçim kriterlerini belirleyebilirsiniz:

-   **Süre** – Planlama motoru, en kısa teslim süresine sahip kaynağı seçer. **Not:** Süreye göre planlama, aynı kaynak grubunun çok sayıda kaynak içermesi ve ikincil operasyonların kullanılması durumunda performans düşüşüne neden olabilir. Operasyon başına en fazla 32 kaynak planlayabilirsiniz. Bu miktarı aşarsanız bir Infolog mesajı görüntülenir ve iş planlama mümkün olan en iyi kaynak alternatifini bulamaz.
-   **Öncelik** – Planlama motoru, iki veya daha fazla sayıda kaynağın aynı kabiliyetlere ve düzeylere sahip olması durumunda en yüksek önceliğe sahip olacak kaynağı seçer. Bu alanda en düşük nümerik değere sahip olan kaynak en yüksek önceliğe sahiptir.

İş planlama devam ederken sistem, kaynakları kaynak parametreleri altında tanımlanan sınırlamalara dayalı olarak planlar. Takvim ayarlarını kullanarak kaynakların kapasitesini kontrol edebilirsiniz. Sistem, planlama süreci sırasında kaynaklar için yükleri hesaplar. **Not:** Operasyon planlama işlevini kullanan üretimler için, operasyon planlamadan sonra iş planlamayı çalıştırabilirsiniz. Operasyon planlamayı kullanmıyorsanız yalnızca iş planlamayı çalıştırabilirsiniz.

## <a name="maximum-capacities-for-resources-per-job-order"></a>İş siparişi başına kaynaklar için maksimum kapasiteler
Kaynaklar, iş planlamayla işlere atanır. İş siparişi başına kaynaklar için maksimum kapasiteler oluşturabilirsiniz. Örneğin, sistemi bir üretim emri için toplam kapasitenin yüzde 50'sini geçmeyecek şekilde planlama yapması için ayarlayabilirsiniz. Bu kurulum, iş planlama seviyesinde kaynakların planlanması açısından size daha fazla kontrol verecektir. Bu nedenle, eş zamanlı üretimleri gerçekleştirmek için yeterli kapasite bulunmamasından doğacak sorunların önlenmesine yardımcı olabilir.

## <a name="resource-efficiency"></a>Kaynak verimliliği
İş planlama, kaynaklar için belirtilen verimlilik yüzdelerini dikkate alır. Verimlilik yüzdeleri, kaynak için ayrılan süreyi düşürür veya yükseltir. Bu nedenle, teslim süresi de artırılır veya azaltılır. Hesaplanmada aşağıdaki formül kullanılır: Planlama süresi = Zaman x 100÷ Formüldeki verimlilik yüzdesi, *Zaman* hem çalışma zamanını hem kurulum zamanını içerir.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]