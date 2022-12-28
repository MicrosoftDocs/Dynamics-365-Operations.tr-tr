---
title: Store Commerce ve Cloud POS arasında seçim yapma
description: Bu makale, Store Commerce ve bulut POS arasındaki önemli farklılıkları açıklar ve Dynamics 365 Commerce uygulayan perakendeciler tarafından gereksinimler için en iyi seçimi yapmaya yardımcı olmak için dikkate alınması gereken çeşitli faktörleri açıklar.
author: josaw1
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 0e1092c0c5c49c6a99dd441c75f545fc831c0b03
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831570"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Store Commerce ve Cloud POS arasında seçim yapma

[!include [banner](includes/banner.md)]

Bu makale, Store Commerce ve bulut POS arasındaki önemli farklılıkları açıklar ve Dynamics 365 Commerce uygulayan perakendeciler tarafından gereksinimler için en iyi seçimi yapmaya yardımcı olmak için dikkate alınması gereken çeşitli faktörleri açıklar. Aynı zamanda uygulamacılara, Dynamics 365 Commerce dağıtırken dikkate almaları gereken faktörlerle ilgili ek bilgiler, ipuçları ve kılavuzlar sağlar. Dağıtım sürecinin bir parçası olarak bu kılavuzu gözden geçiren ve izleyen uygulamacılar kullanıcı memnuniyetini veya performansı etkileyebilecek sorunları önleyebilir.

## <a name="insights"></a>Öngörüler

Commerce çok çeşitli dağıtım ve topoloji seçenekleri sunar. Bu nedenle, perakendeciler kendi işletmelerine ve teknoloji gereksinimlerine en uygun bileşenleri ve yapılandırmayı seçebilir. Uygulamanın dikkatli şekilde değerlendirilmesi gereken bir yönü satış noktası (POS) bileşeni için form faktörü ve platform seçimidir.

### <a name="pos-platform-and-form-factor-considerations"></a>POS platformu ve form faktörüyle ilgili önemli noktalar

Commerce aşağıdaki POS seçeneklerini destekler:

- Microsoft Windows için Store Commerce
- iOS ve Android için Store Commerce
- Microsoft Edge ve Google Chrome tarayıcılar destekleyen Bulut POS (CPOS)
- Microsoft Windows için Modern POS (MPOS) (MPOS, 2023 Ekim'de kullanımdan kalkacaktır.) 

Tüm durumlarda, POS (Store Commerce ve CPOS) daima aynı temel uygulama kodunu paylaşır. Bu noktada aşağıdaki nedenlerle önemlidir:

- Platform ya da form faktörü ne olursa olsun kullanıcı arabirimi (UI) tutarlıdır.
- İşlevsel özelliklerin çoğu platform ya da form faktöründen bağımsız olarak aynıdır. Ancak, bazı önemli farklar vardır. Bu bölümde bu farklar belirtilmiştir.
- Her mağazada, POS çeşitleri birleştirilebilir ve birlikte çalışabilir. Örneğin, bir perakendeci ana kasaları için Windows işletim sistemli bilgisayarlarda Store Commerce kullanabilir. Ancak, perakendeci bu kasaları tarayıcı tabanlı terminaller veya mobil cihazlarla tamamlayabilir.
- Özelleştirmeler ve uzantılar platformlar ve form faktörleri arasında kolaylıkla kullanılabilir. Temel uygulama kodu paylaşıldığından, çoğu özelleştirme birçok kez yerine bir kez uygulanabilir.

### <a name="store-commerce-vs-cpos"></a>Store Commerce ve CPOS

Store Commerce ve CPOS büyük ölçüde aynı olmakla birlikte, anlamanız gereken bazı önemli farklar vardır.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce, bir aygıta yüklenen ve hizmet verilen bir masaüstü uygulamasıdır.

- **Windows** – Windows için Store Commerce uygulaması, uygulama kodunun tamamını, Commerce Runtime (CRT) ve Hardware Station (HWS) içerir.
- **iOS/Android** – Bu platformlarda, uygulama CPOS uygulama kodu için bir barındırıcı olarak çalışır. Başka bir deyişle, uygulama kodu Commerce Scale Unit (RSSU) üzerinde barındırılan CPOS sunucusundan geliyor. Daha fazla bilgi için bkz. [Commerce Scale Unit'e genel bakış](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

CPOS tarayıcıda çalıştığı için uygulama cihaza yüklenmez. Bunun yerine, tarayıcı uygulama koduna CPOS sunucusundan erişim sağlar. Bu nedenle, CPOS doğrudan POS donanımına erişemez veya çevrimdışı durumda çalışamaz.

### <a name="store-deployment-considerations"></a>Mağaza dağıtımıyla ilgili önemli noktalar

Platform ve form faktörünün yanı sıra, perakendecilerin mağazada bir dağıtım seçeneğini de belirlemesi gerekir. Aşağıdaki tablo, her bir POS seçeneğinde kullanılabilen yapılandırmaları gösterir.

| POS uygulaması            | Commerce Scale Unit | Çevrimdışı kullanılabilir | Yerel HWS desteği |
|----------------------------|---------------------|-------------------|-------------------|
| Windows için Store Commerce | Bulut veya RSSU       | Evet               | Evet               |
| Android için Store Commerce | Bulut veya RSSU       | No.                | Evet               |
| iOS için Store Commerce     | Bulut veya RSSU       | No.                | Evet               |
| Cloud POS                  | Bulut veya RSSU       | No.                | No.                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce Scale Unit, CRT'yi barındıran bir bileşendir. CRT, POS'un kullandığı tüm iş mantığını içerir ve kanal veritabanına erişim sunar. Çevrimiçi olduklarında mağazadaki tüm POS istemcileri Commerce Scale Unit kullanır. Commerce Scale Unit bulutta veya mağazada dağıtılabilir.

#### <a name="offline-mode"></a>Çevrimdışı mod

Windows için Store Commerce, çevrimdışı modu destekler. Çevrimdışı modda, POS Commerce Scale Unit bağlantısı kesilmiş olsa bile satış işlemine devam edebilir. Bağlantı yeniden kurulduğunda kanal veritabanıyla eşitlenebilir. Store Commerce, kendi katıştırılmış CRT kurulumunu kullanır ve kendi yerel veri kaynağını (çevrimdışı SQL Server veritabanı) geçici olarak kullanır. Çevrimdışı işlev hakkında daha fazla bilgi için bkz. [POS çevrimdışı işlevi](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>POS çevre birimi/donanımı hakkında önemli noktalar

Perakendecilerin POS'un yazıcılar, kasa çekmeceleri ve ödeme terminalleri gibi çevre birimlerine ve cihazlara nasıl erişeceğini de göz önünde bulundurmaları gerekir. Donanım istasyonları bir POS kasasına ayrılabilir veya mağazadaki kasalar arasında paylaştırılabilir.

| POS uygulaması            | Yerel HWS OPOS | Ağ çevre birimleri | Paylaşılan HWS desteği |
|----------------------------|----------------|---------------------|--------------------|
| Windows için Store Commerce | Evet            | Evet                 | Evet                |
| Android için Store Commerce | No.             | Evet                 | Evet                |
| iOS için Store Commerce     | No.             | Evet                 | Evet                |
| Cloud POS                  | No.             | No.                  | Evet                |

Donanım istasyonları hakkında daha fazla bilgi için bkz. [Retail donanım istasyonu yapılandırma ve yükleme](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Uygulama ile ilgili hususlar

Mağazalarınızda POS uygulamanızı planlarken aşağıdaki bilgileri göz önünde bulundurun:

- **İşlevsel gereksinimler** – Temel iş süreçleri ve yetenekleri platform, form faktörü veya dağıtım topolojisinden bağımsız olarak aynıdır. Bu nedenle, çoğu perakendecinin uygulamalarını planlarken işlevsel gereksinimleri değerlendirmesine gerek yoktur.
- **Bağlantı** – Ağ kullanılabilirliği (geniş alan ağı \[WAN\] ve yerel alan ağı \[LAN\]) dikkat gerektiren önemli bir etkendir. Sıfır ayak izine sahip, bulutta barındırılan çözümün maliyet ve basitlik açısından sağladığı tüm avantajlar, sistemin iş açısından önemli işlemlerde kullanılamaması durumunda ortadan kalkar.

    Belirli bir cihaz için bağlantı çok güvenilir ve esnek olmadığı veya belirli miktarda bir kesinti perakendeci tarafından kabul edilebilir olmadığı sürece, aşağıdaki seçeneklerden birini öneririz:

    - Windows'ta Store Commerce kullanın ve çevrimdışı modu etkinleştirin.
    - Şirket içi bir Commerce Scale Unit dağıtın.

    Bu iki seçenek karşılıklı olarak birbirini dışarıda bırakmaz. En güvenilir topoloji için perakendeciler internet bağlantısına veya Azure'un kullanılabilirliğine olan bağımlılığı azaltmak amacıyla yerel bir RSSU dağıtabilir. Ayrıca, yerel sunucu veya ağ ile ilgili bir sorun olması durumunda çevrimdışı modun etkinleştirildiği POS kayıtları da dağıtabilir.

- **Donanım cihazları/çevre birimleri** – Retail POS sistemin önemli bir yönü yazıcı, nakit çekmecesi ve ödeme terminalleri gibi POS çevre birimlerini kullanabilme yeteneğidir. Tüm kullanılabilir POS seçenekleri çevre birim cihazlarını kullanabilmesine rağmen, yalnızca Windows için Store Commerce bunları doğrudan destekler. Diğer tüm uygulamalar için bir veya daha fazla donanım istasyonu olması gerekir. Bu yaklaşım esneklik kazandırmasına karşın, ek bileşenlerin dağıtılması, yapılandırılması ve bakımının yapılması gerekir.
- **Sistem gereksinimleri** – POS uygulaması için sistem gereksinimleri farklılık gösterir. En son bilgileri seçiminizi yapmadan önce kontrol ettiğinizden emin olun. Örneğin, CPOS bir tarayıcıda çalıştığı için çok çeşitli işletim sistemlerini destekler. Sistem gereksinimleri hakkında daha fazla bilgi için bkz. [Bulut dağıtımları için sistem gereksinimleri](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Dağıtım ve bakım** – Dağıtım ve bakım gereksinimlerinin karmaşıklığı, uygulamaya ve dağıtım seçimlerine bağlı olarak değişebilir. Örneğin, bulutta barındırılan bir CPOS dağıtımı için, her cihaza uygulamayı yüklemeniz ve güncelleştirmeniz gerekmez. Bu nedenle, bu yaklaşım büyük ölçüde karmaşıklığı ve maliyeti azaltır. Ancak, her kasaya Store Commerce dağıtırsanız, çevrimdışı modu etkinleştirirseniz ve paylaştırılmış donanım istasyonları dağıtırsanız, yönetilmesi gereken uç nokta sayısını önemli ölçüde artırırsınız.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
