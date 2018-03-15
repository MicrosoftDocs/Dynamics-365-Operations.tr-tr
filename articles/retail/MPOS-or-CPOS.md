---
title: "Modern POS ile Cloud POS arasında seçim yapma"
description: "Bu konu, Retail Modern POS ile Cloud POS arasındaki ana farkları açıklar. Ayrıca, Microsoft Dynamics 365 for Retail uygulayan perakendecilerin gereksinimlerine en uygun seçimi yapmak için dikkate almaları gereken çeşitli faktörleri de açıklar."
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7eb15f9f73f4773d98160e1b0ec5ce74c159cdea
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---

# <a name="choose-between-modern-pos-and-cloud-pos"></a>Modern POS ile Cloud POS arasında seçim yapma

[!include[banner](includes/banner.md)]

Bu konu uygulamacılara, Microsoft Dynamics 365 for Retail dağıtırken dikkate almaları gereken faktörlerle ilgili ek bilgiler, ipuçları ve kılavuzlar sağlar. Dağıtım sürecinin bir parçası olarak bu kılavuzu gözden geçiren ve izleyen uygulamacılar kullanıcı memnuniyetini veya performansı etkileyebilecek sorunları önleyebilir.

## <a name="insights"></a>İçgörüler
Retail çok çeşitli dağıtım ve topoloji seçenekleri sunar. Bu nedenle, perakendeciler kendi işletmelerine ve teknoloji gereksinimlerine en uygun bileşenleri ve yapılandırmayı seçebilir. Uygulamanın dikkatli şekilde değerlendirilmesi gereken bir yönü satış noktası (POS) bileşeni için form faktörü ve platform seçimidir.

### <a name="pos-platform-and-form-factor-considerations"></a>POS platformu ve form faktörüyle ilgili önemli noktalar
Retail aşağıdaki POS seçeneklerini destekler:

- Microsoft Windows için Retail Modern POS (MPOS)
- Microsoft Windows Phone için MPOS
- Apple iPad veya Google Android tablet için MPOS
- Microsoft Edge, Internet Explorer ve Google Chrome tarayıcıları destekleyen Cloud POS (CPOS)

Tüm durumlarda, POS (MPOS ve CPOS) daima aynı temel uygulama kodunu paylaşır. Bu noktada aşağıdaki nedenlerle önemlidir:

- Platform ya da form faktörü ne olursa olsun kullanıcı arabirimi (UI) tutarlıdır.
- İşlevsel özelliklerin çoğu platform ya da form faktöründen bağımsız olarak aynıdır. Ancak, bazı önemli farklar vardır. Bu bölümde bu farklar belirtilmiştir.
- Belirli bir mağazada, POS çeşitleri birleştirilebilir ve birlikte çalışabilir. Örneğin, bir perakendeci ana kasaları için Windows işletim sistemli bilgisayarlarda MPOS kullanabilir. Ancak, perakendeci bu kasaları tarayıcı tabanlı terminaller veya mobil cihazlarla tamamlayabilir.
- Özelleştirmeler ve uzantılar platformlar ve form faktörleri arasında kolaylıkla kullanılabilir. Temel uygulama kodu paylaşıldığından, çoğu özelleştirme birçok kez yerine bir kez uygulanabilir.

### <a name="mpos-vs-cpos"></a>MPOS ile CPOS karşılaştırması
MPOS ve CPOS büyük ölçüde aynı olmakla birlikte, anlamanız gereken bazı önemli farklar vardır.

#### <a name="mpos"></a>MPOS

Windows, iOS veya Android cihazdaki MPOS bu cihazda paketlenen, yüklenen ve hizmet veren bir uygulamadır.

- **Windows** – Windows için MPOS uygulaması tüm uygulama kodunu ve katıştırılmış ticaret çalışma süresini (CRT) içerir. 
- **iOS/Android** – Bu platformlarda, uygulama CPOS uygulama kodu için bir barındırıcı olarak çalışır. Başka bir deyişle, uygulama kodu Microsoft Azure veya Retail Store Scale Unit'teki (RSSU) CPOS sunucusundan gelir. Daha fazla bilgi için bkz. [Retail Store Scale Unit'e genel bakış](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).

#### <a name="cpos"></a>CPOS

CPOS tarayıcıda çalıştığı için uygulama cihaza yüklenmez. Bunun yerine, tarayıcı uygulama koduna CPOS sunucusundan erişim sağlar. Bu nedenle, CPOS doğrudan POS donanımına erişemez veya çevrimdışı durumda çalışamaz.

### <a name="store-deployment-considerations"></a>Mağaza dağıtımıyla ilgili önemli noktalar
Platform ve form faktörünün yanı sıra, perakendecilerin mağazada bir dağıtım seçeneğini de belirlemesi gerekir. Aşağıdaki tablo, her bir POS seçeneğinde kullanılabilen yapılandırmaları gösterir.

| POS uygulaması         | Perakende sunucusu | Çevrimdışı kullanılabilir |
|-------------------------|---------------|-------------------|
| Windows için MPOS        | Bulut veya RSSU | Evet               |
| iOS veya Android için MPOS | Bulut veya RSSU | Hayır                |
| Bulut POS               | Bulut veya RSSU | Hayır                |

#### <a name="retail-server"></a>Perakende sunucusu

Retail sunucusu CRT'yi barındıran bir bileşendir. CRT POS'un kullandığı tüm iş mantığını içerir ve kanal veritabanına erişim sağlar. Çevrimiçi olduklarında mağazadaki tüm POS istemcileri Retail sunucusunu kullanır.  Retail sunucusu bulutta veya mağazada (RSSU) dağıtılabilir.

#### <a name="offline-mode"></a>Çevrimdışı mod

Windows için MPOS çevrimdışı modu destekler. Çevrimdışı modda, POS Retail sunucusu bağlantısı kesilmiş olsa bile satış işlemine devam edebilir. Bağlantı yeniden kurulduğunda kanal veritabanıyla eşitlenebilir. MPOS kendi katıştırılmış CRT kurulumunu kullanır ve kendi yerel veri kaynağını (çevrimdışı SQL Server veritabanı) geçici olarak kullanır. Çevrimdışı işlev hakkında daha fazla bilgi için bkz. [POS çevrimdışı işlevi](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-offline-functionality).

### <a name="pos-peripheralhardware-considerations"></a>POS çevre birimi/donanımı hakkında önemli noktalar
Perakendecilerin POS'un yazıcılar, kasa çekmeceleri ve ödeme terminalleri gibi çevre birimlerine ve cihazlara nasıl erişeceğini de göz önünde bulundurmaları gerekir. Yalnızca Windows için MPOS bu cihazlarla ile doğrudan iletişimi destekler. Windows Phone, iOS ve Android için MPOS ve Cloud POS bu cihazlara erişim için bir donanım istasyonu gerektirir. Donanım istasyonları bir POS kasasına ayrılabilir veya mağazadaki kasalar arasında paylaştırılabilir. Donanım istasyonları hakkında daha fazla bilgi için bkz. [Retail donanım istasyonu yapılandırma ve yükleme](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).

## <a name="implementation-considerations"></a>Uygulama ile ilgili hususlar
Perakende mağazalarınızda POS uygulamanızı planlarken aşağıdaki bilgileri göz önünde bulundurun:

- **İşlevsel gereksinimler** – Temel iş süreçleri ve yetenekleri platform, form faktörü veya dağıtım topolojisinden bağımsız olarak aynıdır. Bu nedenle, çoğu perakendecinin uygulamalarını planlarken işlevsel gereksinimleri değerlendirmesine gerek yoktur.
- **Bağlantı** - Ağ kullanılabilirliği (geniş alan ağı \[WAN\] ve yerel alan ağı \[LAN\]) dikkat gerektiren önemli bir etkendir. Sıfır ayak izine sahip, bulutta barındırılan çözümün maliyet ve basitlik açısından sağladığı tüm avantajlar, sistemin iş açısından önemli işlemlerde kullanılamaması durumunda ortadan kalkar.

    Belirli bir cihaz için bağlantı çok güvenilir ve esnek olmadığı veya belirli miktarda bir kesinti perakendeci tarafından kabul edilebilir olmadığı sürece, aşağıdaki seçeneklerden birini öneririz:

    - Windows'ta MPOS kullanın ve çevrimdışı modu etkinleştirin.
    - Bir şirket için RSSU dağıtın.

    Bu iki seçenek karşılıklı olarak birbirini dışarıda bırakmaz. En güvenilir topoloji için perakendeciler internet bağlantısına veya Azure'un kullanılabilirliğine olan bağımlılığı azaltmak amacıyla yerel bir RSSU dağıtabilir. Ayrıca, yerel sunucu veya ağ ile ilgili bir sorun olması durumunda çevrimdışı modun etkinleştirildiği POS kayıtları da dağıtabilir.

- **Donanım cihazları/çevre birimleri** – Retail POS sistemin önemli bir yönü yazıcı, nakit çekmecesi ve ödeme terminalleri gibi POS çevre birimlerini kullanabilme yeteneğidir. Tüm kullanılabilir POS seçenekleri çevre birim cihazlarını kullanabilmesine rağmen, yalnızca Windows için MPOS bunları doğrudan destekler. Diğer tüm uygulamalar için bir veya daha fazla donanım istasyonu olması gerekir. Bu yaklaşım esneklik kazandırmasına karşın, ek bileşenlerin dağıtılması, yapılandırılması ve bakımının yapılması gerekir.
- **Sistem gereksinimleri** – POS uygulaması için sistem gereksinimleri farklılık gösterir. En son bilgileri seçiminizi yapmadan önce kontrol ettiğinizden emin olun. Örneğin, CPOS bir tarayıcıda çalıştığı için çok çeşitli işletim sistemlerini destekler. Sistem gereksinimleri hakkında daha fazla bilgi için bkz. [Bulut dağıtımları için sistem gereksinimleri](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).
- **Dağıtım ve bakım** – Dağıtım ve bakım gereksinimlerinin karmaşıklığı, uygulamaya ve dağıtım seçimlerine bağlı olarak değişebilir. Örneğin, bulutta barındırılan bir CPOS dağıtımı için, her cihaza uygulamayı yüklemeniz ve güncelleştirmeniz gerekmez. Bu nedenle, bu yaklaşım büyük ölçüde karmaşıklığı ve maliyeti azaltır. Ancak, her kasaya MPOS dağıtırsanız, çevrimdışı modu etkinleştirirseniz ve paylaştırılmış donanım istasyonları dağıtırsanız, yönetilmesi gereken uç nokta sayısını önemli ölçüde artırırsınız.

