---
title: Gider raporları yeniden tasarlandı
description: Bu konu, Microsoft Dynamics 365 for Finance and Operations'daki gider raporu girişi için yeniden tasarlanan ve yenilenmiş olan deneyim hakkında bilgi sağlar. Yeni deneyim, gider raporlarını tamamlama sürecini basitleştirir ve gerekli zamanı azaltır.
author: ryansandness
manager: AnnBe
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: c7a2b95456e812970b135d83f0f7e503310ce185
ms.sourcegitcommit: 97ed74889a09ef385f6ecbab69e84a05ff42ee41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/20/2019
ms.locfileid: "1592649"
---
# <a name="expense-reports-reimagined"></a>Gider raporları yeniden tasarlandı

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Gider raporu girişi, gider raporlarının tamamlanmasını basitleştirmek ve gereken zamanı azaltmak amacıyla yeniden tasarlanmıştır. Yeni gider deneyiminin ana bileşenleri aşağıdadır:

- Temsilcinizin giderlerine erişmenize olanak tanıyan yeni bir gider yönetimi çalışma alanı.
- Başlık düzeyi girişlerini daha iyi göstermek ve gider satırlarına giriş ekleme sürecini basitleştirmek için yeni bir giriş eşleştirme deneyimi.
- Birçok başka gider satırı ve ek veri sütunu görüntülemenizi sağlayan, salt okunur yeni bir ızgara. Artık tüm dökümü yapılmış ve bölünmüş satırları ana giderlerle birlikte görebilirsiniz.
- Giderleri düzenlemek için basitleştirilmiş bölme.
- Sorunun ne olduğunu ve nasıl çözümleneceğini anlamak için doğru içeriğe sahip olmanızı sağlamaya yardımcı olacak şekilde yeniden tasarlanan hata, uyarı ve ilke iletileri. Microsoft, kullanıcıların görevlerini tamamlama ve sorunları bildirme fırsatı olmadan önce görüntülenen tamamlanmamış döküm mesajı gibi birçok iletiyi kaldırmıştır.
- Kuruluşunuz tarafından hangi alanların gerekli olduğunu, hangi alanların isteğe bağlı olduğunu ve hangi alanların yakalanmaması gerektiğini belirtmek için yeni bir sayfa. Bu sayfa, kullanıcıların ayarlaması gereken alan sayısını azaltmaya yardımcı olur.
- Gider raporları için yeni bir görünüm; böylece raporlar artık muhasebe personeli için tasarlandıkları şekilde görünmez.

Yeni deneyimi açmak için **Özellik yönetimi** çalışma alanını kullanarak **Gider raporları yeniden tasarlandı** özelliğini açın. Bu özelliği etkinleştirdiğinizde, aşağıdaki eylemler gerçekleşir:

- Mevcut gider çalışma alanı yeni çalışma alanıyla değiştirilir.
- Gider alanı görünürlüğü için yeni bir menü öğesi eklenir.
- Gider raporları için varolan menü öğeleri (varolan sayfa) veya gider raporu alanları kaldırılmaz.
- İş akışları ve onayların sizi varolan gider raporları sayfasına götürmeye devam eder.

## <a name="getting-started-video-for-new-users"></a>Yeni kullanıcılar için Başlarken videosu

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE2Y7gO]

[Dynamics 365 for Finance and Operations içinde gider deneyimi](https://youtu.be/Ocy-MsTvEE0) videosu (yukarıda gösterilen), YouTube'da bulunan [Finance and Operations oynatma listesinde](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) bulunmaktadır.

## <a name="new-features"></a>Yeni özellikler

| Yeni özellik | Tanım |
|---|----|
| Gider alanı görünürlüğü | Yeni bir kurulum sayfası bir kuruluş için hangi alanların devre dışı bırakılacağını, hangi alanların gerekli olacağını ve hangi alanların önerildiğini belirtmenize olanak tanır. |
| Gerekli alanlar | Yeni basit yapılandırma, ilke çerçevesini kullanmak zorunda kalmadan gerekli bazı alanları yapmanızı sağlar. |
| İsteğe bağlı alanlar | İsteğe bağlı alanlar için ikinci bir sayfa eklendi. Bu şekilde, çalışanlar alanları ayarlamaları gerektiğini hissetmeyecek, ancak alanlara hala kolaylıkla erişilebilecek. |
| İliştirilmemiş girişler ekleme | Gider raporuna iliştirilmemiş girişler ekleme yeteneği çalışma alanından ve gider raporunda daha görünür hale geldi. |
| İyileştirilmiş ileti | Uyarıları veya hataları olan gider satırları için daha iyi görünürlük. |
| İleti çubuğundaki iletilerde azaltma| Bilgi günlüğü iletisi sayısı düşürüldü ve birçok durumda tekrarlanan iletilerin görünmesini engellemeye yönelik çalışma yapıldı. |
| Birlikte gruplanan genel eylemler | En yaygın satır düzeyinde eylemler için yeni eylemler düğmesi ve başlık ve diğer daha az sık kullanılan eylemler için üç nokta düğmesi (...) eklenerek arabirim temizlendi. |
| Görünürlüğü artırmak için yeni çalışma alanı | Yeni bir çalışma alanı, kullanıcıların farklı alanlara gitmesine izin veren özellikleri ve bağlantıları birleştiriyor. |
| Gider oluşturulurken mevcut giderleri ve girişleri ekleyin | Gider raporları oluştururken, tüm veya seçilmiş giderleri ve girişleri ekleyebilirsiniz. |
| Döviz kuru hesaplayıcı | Cepten çok para birimli hareketler için döviz kurunu hesaplamanızı sağlayan bir döviz kuru hesap makinesi eklendi. |
| Kaydet ve yeni gider satırları ekle | Yeni giderler girildiğinde, gider satırlarını hızlı bir şekilde girebilmenize yardımcı olmak için **Kaydet** ve **Yeni** düğmeleri kullanıma sunuldu. |
| Bölünmüş ve dökümü yapılmış satırlar üzerinde daha fazla görünürlük | Dökümü yapılmış ve bölünmüş satırlar doğrudan gider listesine eklenerek görünürlüğü artırır ve ilke hataları veya başka hatalar olup olmadığını kolayca belirlemenize yardımcı olur. |
| Döküm sırasında girişleri göster | Döküm sırasında girişler gösterilebilir. |

İlk sürüm, gider girişi senaryolarına odaklanmıştır. Gider raporu inceleme veya onay senaryosu varolan gider girişi sayfasını kullanmaya devam edecektir.

Aşağıdaki özellikler mevcut sayfada bulunur ancak henüz yeni sayfada yer almamaktadır. Bu özellikler sonraki birkaç sürümde yeniden tanıtılacaktır:

- Onaylar
- Borç hesapları onayları ve muhasebe hesaplarını düzenleme yeteneği
- Çoklu giriş noktaları
- Seyahat talebi tümleştirmesi
- Gider alanı görünürlüğü için veri varlığı
- Harcırah giderleri girişi
- Satır düzeyinde iş akışı
- Geçici onaylayan desteği
- Gelişmiş döküm
