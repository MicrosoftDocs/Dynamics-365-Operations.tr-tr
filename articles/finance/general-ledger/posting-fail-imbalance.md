---
title: Dengesizlik nedeniyle yevmiye defterine nakil hatası
description: Bu konuda, fiş hareketlerinde borçlar ve alacakların dengelenememesinin ve dolayısıyla hareketlerin deftere nakledilememesinin nedenleri açıklanmaktadır. Konu ayrıca sorun giderme adımlarını da içermektedir.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a59724ff698b6ad0e84b0642240da5f8953ab3d1
ms.sourcegitcommit: 9642494da87c0d237f9fcbe15df14315d9e88fa2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2021
ms.locfileid: "7385735"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Dengesizlik nedeniyle yevmiye defterine nakil hatası

[!include [banner](../includes/banner.md)]

Bu konuda, fiş hareketlerinde borçlar ve alacakların dengelenememesinin ve dolayısıyla hareketlerin deftere nakledilememesinin nedenleri açıklanmaktadır. Konu ayrıca sorun giderme adımlarını da içermektedir.

## <a name="symptom"></a>Belirti

Bazı durumlarda, yevmiye defteri nakledilemez ve şu ileti görüntülenir: "Belirli bir fişteki hareketler belirli bir tarih itibariyle dengelenmiyor (muhasebe para birimi: 0.01 - raporlama para birimi: 0.06)." Yevmiye defteri neden nakledilemiyor?

## <a name="resolution"></a>Çözüm

Genel muhasebeye nakil sırasında her fişin, hareket para birimi, muhasebe para birimi ve bu para birimleri **Genel muhasebe kurulumu** sayfasında tanımlanmışsa raporlama para birimi cinsinden dengelenmesi gerekir. (Fişler, toplam borçlar toplam alacaklara eşit olduğunda dengelenir.)

Yevmiye defteri satırları sayfasının alt kısmında toplamlar, muhasebe para birimi ve raporlama para birimi cinsinden gösterilir. Yabancı para birimi hareketleri için hareket para biriminde **gösterilmezler**. Ayrıca benzetim veya deftere nakil sırasında kullanıcıların aldığı hata iletisi, yalnızca muhasebe para birimi ve raporlama para birimindeki farklılıkları gösterir. Tek bir fişte birden fazla hareket para birimi olabileceğinden ve yevmiye defteri farklı hareket para birimlerindeki fişleri içerebileceğinden bunları hareket para birimi cinsinden göstermez. Bu nedenle, her fişin hareket para birimi tutarlarının dengelendiğini doğrulamanız önemlidir.

### <a name="transaction-currency"></a>Hareket para birimi

Sistem, benzetim ve deftere nakil sırasında her fişin hareket para biriminde dengelendiğini doğrular. Girilen her fişte, hareket para birimi için bir veya daha fazla para birimi olabilir. Örneğin, genel yevmiye defterine girilen bir fişte euro (EUR) kullanan bir banka hesabından Kanada doları (CAD) kullanan bir banka hesabına para aktarıldığında iki hareket para birimi olabilir.

Fişte yalnızca bir hareket para birimi varsa toplam borçlar, bu fişteki toplam alacaklara eşit olmalıdır. Müşteriler, hareket para birimi tutarları dengelenmediğinden deftere nakil işleminin doğru şekilde yapılamadığı aşağıdaki senaryolarla karşılaştı:

- Toplam borçlar ve toplam alacaklar, hareket para biriminde **dengelenmedi** ancak muhasebe para birimi ve raporlama para birimi için dengelendi. Müşteri, fişin deftere nakledilmeye devam edeceğini varsaydı. Ancak bu varsayım yanlıştı. **Fişteki hareket para birimi tutarları, fişin tüm satırlarında aynı para birimi olduğunda her zaman dengelenmelidir.**
- Fiş, Microsoft Excel aracılığıyla içeri aktarıldı ve kullanıcı, hareket para birimi tutarlarının dengelendiğini düşündü. Excel çalışma kitabında, içeri aktarılan tutarlar **Para birimi** değerleri yerine **Sayısal** değerler olarak ayarlandı. Bu senaryoda, çalışma kitabındaki sayısal tutarların ikiden fazla ondalık basamağı vardı ve tutarlar içeri aktarıldığında ikiden fazla ondalık basamak eklendi. Bu nedenle, kuruşun kesir kısmı kapalı olduğundan borçlar alacaklara eşit değildi. Gösterilen tutarların yalnızca iki ondalık basamağı olduğundan yevmiye defteri bu farkı fiş satırlarına yansıtmadı.
- Fiş, Excel aracılığıyla içeri aktarıldı ve kullanıcı, hareket para birimi tutarlarının dengelendiğini düşündü. Fiş dengelenmiş olsa da fişteki bazı satırlarda farklı hareket tarihleri vardı. Fiş ve hareket tarihi başına toplam borçları ve toplam alacakları eklediğinizde bunlar dengelenmedi. Sistem artık bu senaryoyu önler. Bir fişin yalnızca bir hareket tarihi olabilir. Bu gereksinim, sistemdeki genel yevmiye defteri aracılığıyla bir fiş girdiğinizde uygulanır. Ancak başlangıçta bir fiş Excel aracılığıyla içeri aktarıldığında uygulanmıyordu.

Desteklenen bir senaryoda, bir fişin birden fazla hareket para birimi olabilir. Bu durumda sistem, para birimleri eşleşmediğinden borçların hareket para birimindeki alacaklara eşit olduğunu **doğrulamaz**. Bunun yerine, sistem muhasebe para birimi tutarlarının dengelendiğini doğrular.

### <a name="accounting-currency"></a>Muhasebe para birimi

Fişin tüm satırlarında aynı hareket para birimi varsa ve hareket para birimi tutarları dengelendiyse sistem muhasebe para birimi tutarlarının dengeli olduğunu doğrular. Fiş yabancı para birimi cinsinden girilirse hareket para birimi tutarlarını muhasebe para birimine çevirmek için fiş satırlarındaki döviz kuru kullanılır. İlk olarak, fişin her satırı çevrilir. Ardından toplam borçları ve toplam alacakları belirlemek için satırlar toplanır. Her satır çevrildiğinden toplam borçlar ve toplam alacaklar dengelenmeyebilir. Ancak aradaki fark **Genel muhasebe parametreleri** sayfasında tanımlanan **Maksimum kuruş farkı** değeri dahilindeyse fiş deftere nakledilir ve fark otomatik olarak Kuruş farkı hesabına nakledilir.

Fişte birden fazla hareket para birimi varsa fişin her satırı muhasebe para birimine çevrilir ve ardından toplam borçları ve toplam alacakları belirlemek için satırlar toplanır. Dengelenmiş kabul edilmesi için borç ve alacakların dengelenmesi ve kuruş yuvarlama farkının olmaması gerekir.

### <a name="reporting-currency"></a>Raporlama para birimi

Fişin tüm satırlarında aynı hareket para birimi varsa ve hareket para birimi tutarları dengelendiyse sistem, raporlama para birimi tutarlarının dengeli olduğunu doğrular. Fiş yabancı para birimi cinsinden girilirse hareket para birimi tutarlarını raporlama para birimine çevirmek için fiş satırlarındaki döviz kuru kullanılır. İlk olarak, fişin her satırı çevrilir. Ardından toplam borçları ve toplam alacakları belirlemek için satırlar toplanır. Her satır çevrildiğinden toplam borçlar ve toplam alacaklar dengelenmeyebilir. Ancak aradaki fark **Genel muhasebe parametreleri** sayfasında tanımlanan **Raporlama para birimi cinsinden maksimum kuruş yuvarlama** değeri dahilindeyse fiş deftere nakledilir ve fark otomatik olarak Kuruş farkı hesabına nakledilir.

Fişte birden fazla hareket para birimi varsa fişin her satırı raporlama para birimine çevrilir ve ardından toplam borçları ve toplam alacakları belirlemek için satırlar toplanır. Dengelenmiş kabul edilmesi için borç ve alacakların dengelenmesi ve kuruş yuvarlama farkının olmaması gerekir.
