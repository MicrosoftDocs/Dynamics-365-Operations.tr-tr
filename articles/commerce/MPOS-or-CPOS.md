---
title: Modern POS (MPOS) ile Cloud POS arasında seçim yapma
description: Bu konu, Modern POS ile Cloud POS arasındaki ana farkları açıklar. Ayrıca, kendi gereksinimlerine en uygun seçimi yapmalarına yardımcı olmak için Dynamics 365 Commerce'ı uygulayan perakendecilerin dikkate almaları gereken çeşitli faktörler de açıklanmaktadır.
author: jblucher
manager: AnnBe
ms.date: 10/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 508fda28d8f815f030e7b163709393f70904a5fd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057706"
---
# <a name="choose-between-modern-pos-mpos-and-cloud-pos"></a>Modern POS (MPOS) ile Cloud POS arasında seçim yapma

[!include [banner](includes/banner.md)]

Bu konu uygulamacılara, Dynamics 365 Commerce dağıtırken dikkate almaları gereken faktörlerle ilgili ek bilgiler, ipuçları ve kılavuzlar sağlar. Dağıtım sürecinin bir parçası olarak bu kılavuzu gözden geçiren ve izleyen uygulamacılar kullanıcı memnuniyetini veya performansı etkileyebilecek sorunları önleyebilir.

## <a name="insights"></a>Öngörüler

Commerce çok çeşitli dağıtım ve topoloji seçenekleri sunar. Bu nedenle, perakendeciler kendi işletmelerine ve teknoloji gereksinimlerine en uygun bileşenleri ve yapılandırmayı seçebilir. Uygulamanın dikkatli şekilde değerlendirilmesi gereken bir yönü satış noktası (POS) bileşeni için form faktörü ve platform seçimidir.

### <a name="pos-platform-and-form-factor-considerations"></a>POS platformu ve form faktörüyle ilgili önemli noktalar

Commerce aşağıdaki POS seçeneklerini destekler:

- Microsoft Windows için Modern POS (MPOS)
- Microsoft Windows Phone için MPOS
- Apple iPad veya Google Android tablet için MPOS
- Microsoft Edge, Internet Explorer ve Google Chrome tarayıcılar destekleyen Bulut POS (CPOS)

Tüm durumlarda, POS (MPOS ve CPOS) daima aynı temel uygulama kodunu paylaşır. Bu noktada aşağıdaki nedenlerle önemlidir:

- Platform ya da form faktörü ne olursa olsun kullanıcı arabirimi (UI) tutarlıdır.
- İşlevsel özelliklerin çoğu platform ya da form faktöründen bağımsız olarak aynıdır. Ancak, bazı önemli farklar vardır. Bu bölümde bu farklar belirtilmiştir.
- Belirli bir mağazada, POS çeşitleri birleştirilebilir ve birlikte çalışabilir. Örneğin, bir perakendeci ana kasaları için Windows işletim sistemli bilgisayarlarda MPOS kullanabilir. Ancak, perakendeci bu kasaları tarayıcı tabanlı terminaller veya mobil cihazlarla tamamlayabilir.
- Özelleştirmeler ve uzantılar platformlar ve form faktörleri arasında kolaylıkla kullanılabilir. Temel uygulama kodu paylaşıldığından, çoğu özelleştirme birçok kez yerine bir kez uygulanabilir.

### <a name="mpos-vs-cpos"></a>MPOS ile CPOS karşılaştırması

MPOS ve CPOS büyük ölçüde aynı olmakla birlikte, anlamanız gereken bazı önemli farklar vardır.

#### <a name="mpos"></a>MPOS

Windows, iOS veya Android cihazdaki MPOS bu cihazda paketlenen, yüklenen ve hizmet veren bir uygulamadır.

- **Windows** – Windows için MPOS uygulaması, uygulama kodunun tamamını ve katıştırılmış Commerce Runtime'ı (CRT) içerir. 
- **iOS/Android** – Bu platformlarda, uygulama CPOS uygulama kodu için bir barındırıcı olarak çalışır. Başka bir deyişle, uygulama kodu Microsoft Azure üzerindeki CPOS sunucusundan veya Commerce Scale Unit (RSSU) üzerinden geliyor. Daha fazla bilgi için bkz. [Commerce Scale Unit'e genel bakış](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).

#### <a name="cpos"></a>CPOS

CPOS tarayıcıda çalıştığı için uygulama cihaza yüklenmez. Bunun yerine, tarayıcı uygulama koduna CPOS sunucusundan erişim sağlar. Bu nedenle, CPOS doğrudan POS donanımına erişemez veya çevrimdışı durumda çalışamaz.

### <a name="store-deployment-considerations"></a>Mağaza dağıtımıyla ilgili önemli noktalar

Platform ve form faktörünün yanı sıra, perakendecilerin mağazada bir dağıtım seçeneğini de belirlemesi gerekir. Aşağıdaki tablo, her bir POS seçeneğinde kullanılabilen yapılandırmaları gösterir.

| POS uygulaması         | Commerce Scale Unit | Çevrimdışı kullanılabilir |
|-------------------------|---------------|-------------------|
| Windows için MPOS        | Bulut veya RSSU | Evet               |
| iOS veya Android için MPOS | Bulut veya RSSU | Hayır                |
| Bulut POS               | Bulut veya RSSU | Hayır                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit, CRT'yi barındıran bir bileşendir. CRT, POS'un kullandığı tüm iş mantığını içerir ve kanal veritabanına erişim sunar. Çevrimiçi olduklarında mağazadaki tüm POS istemcileri Commerce Scale Unit kullanır. Commerce Scale Unit bulutta veya mağazada dağıtılabilir.

#### <a name="offline-mode"></a>Çevrimdışı mod

Windows için MPOS çevrimdışı modu destekler. Çevrimdışı modda, POS Commerce Scale Unit bağlantısı kesilmiş olsa bile satış işlemine devam edebilir. Bağlantı yeniden kurulduğunda kanal veritabanıyla eşitlenebilir. MPOS, kendi katıştırılmış CRT kurulumunu kullanır ve kendi yerel veri kaynağını (çevrimdışı SQL Server veritabanı) geçici olarak kullanır. Çevrimdışı işlev hakkında daha fazla bilgi için bkz. [POS çevrimdışı işlevi](https://docs.microsoft.com/dynamics365/unified-operations/retail/pos-offline-functionality).

### <a name="pos-peripheralhardware-considerations"></a>POS çevre birimi/donanımı hakkında önemli noktalar

Perakendecilerin POS'un yazıcılar, kasa çekmeceleri ve ödeme terminalleri gibi çevre birimlerine ve cihazlara nasıl erişeceğini de göz önünde bulundurmaları gerekir. Yalnızca Windows için MPOS bu cihazlarla ile doğrudan iletişimi destekler. Windows Phone, iOS ve Android için MPOS ve Cloud POS bu cihazlara erişim için bir donanım istasyonu gerektirir. Donanım istasyonları bir POS kasasına ayrılabilir veya mağazadaki kasalar arasında paylaştırılabilir. Donanım istasyonları hakkında daha fazla bilgi için bkz. [Retail donanım istasyonu yapılandırma ve yükleme](https://docs.microsoft.com/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).

## <a name="implementation-considerations"></a>Uygulama ile ilgili hususlar

Mağazalarınızda POS uygulamanızı planlarken aşağıdaki bilgileri göz önünde bulundurun:

- **İşlevsel gereksinimler** – Temel iş süreçleri ve yetenekleri platform, form faktörü veya dağıtım topolojisinden bağımsız olarak aynıdır. Bu nedenle, çoğu perakendecinin uygulamalarını planlarken işlevsel gereksinimleri değerlendirmesine gerek yoktur.
- **Bağlantı** – Ağ kullanılabilirliği (geniş alan ağı \[WAN\] ve yerel alan ağı \[LAN\]) dikkat gerektiren önemli bir etkendir. Sıfır ayak izine sahip, bulutta barındırılan çözümün maliyet ve basitlik açısından sağladığı tüm avantajlar, sistemin iş açısından önemli işlemlerde kullanılamaması durumunda ortadan kalkar.

    Belirli bir cihaz için bağlantı çok güvenilir ve esnek olmadığı veya belirli miktarda bir kesinti perakendeci tarafından kabul edilebilir olmadığı sürece, aşağıdaki seçeneklerden birini öneririz:

    - Windows'ta MPOS kullanın ve çevrimdışı modu etkinleştirin.
    - Şirket içi bir Commerce Scale Unit dağıtın.

    Bu iki seçenek karşılıklı olarak birbirini dışarıda bırakmaz. En güvenilir topoloji için perakendeciler internet bağlantısına veya Azure'un kullanılabilirliğine olan bağımlılığı azaltmak amacıyla yerel bir RSSU dağıtabilir. Ayrıca, yerel sunucu veya ağ ile ilgili bir sorun olması durumunda çevrimdışı modun etkinleştirildiği POS kayıtları da dağıtabilir.

- **Donanım cihazları/çevre birimleri** – Retail POS sistemin önemli bir yönü yazıcı, nakit çekmecesi ve ödeme terminalleri gibi POS çevre birimlerini kullanabilme yeteneğidir. Tüm kullanılabilir POS seçenekleri çevre birim cihazlarını kullanabilmesine rağmen, yalnızca Windows için MPOS bunları doğrudan destekler. Diğer tüm uygulamalar için bir veya daha fazla donanım istasyonu olması gerekir. Bu yaklaşım esneklik kazandırmasına karşın, ek bileşenlerin dağıtılması, yapılandırılması ve bakımının yapılması gerekir.
- **Sistem gereksinimleri** – POS uygulaması için sistem gereksinimleri farklılık gösterir. En son bilgileri seçiminizi yapmadan önce kontrol ettiğinizden emin olun. Örneğin, CPOS bir tarayıcıda çalıştığı için çok çeşitli işletim sistemlerini destekler. Sistem gereksinimleri hakkında daha fazla bilgi için bkz. [Bulut dağıtımları için sistem gereksinimleri](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).
- **Dağıtım ve bakım** – Dağıtım ve bakım gereksinimlerinin karmaşıklığı, uygulamaya ve dağıtım seçimlerine bağlı olarak değişebilir. Örneğin, bulutta barındırılan bir CPOS dağıtımı için, her cihaza uygulamayı yüklemeniz ve güncelleştirmeniz gerekmez. Bu nedenle, bu yaklaşım büyük ölçüde karmaşıklığı ve maliyeti azaltır. Ancak, her kasaya MPOS dağıtırsanız, çevrimdışı modu etkinleştirirseniz ve paylaştırılmış donanım istasyonları dağıtırsanız, yönetilmesi gereken uç nokta sayısını önemli ölçüde artırırsınız.
