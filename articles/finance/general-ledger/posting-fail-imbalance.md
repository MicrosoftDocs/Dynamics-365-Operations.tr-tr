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
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 07408e608496dcc19562b866449b3b27f5f80edd
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2022
ms.locfileid: "8719946"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Dengesizlik nedeniyle yevmiye defterine nakil hatası

[!include [banner](../includes/banner.md)]

Bu konuda, fiş hareketlerinde borçlar ve alacakların dengelenememesinin ve dolayısıyla hareketlerin deftere nakledilememesinin nedenleri açıklanmaktadır. Konu ayrıca sorun giderme adımlarını da içermektedir.

## <a name="symptom"></a>Belirti

Bazı durumlarda, yevmiye defteri nakledilemez ve şu ileti görüntülenir: "Belirli bir fişteki hareketler belirli bir tarih itibariyle dengelenmiyor (muhasebe para birimi: 0.01 - raporlama para birimi: 0.06)." Yevmiye defteri neden nakledilemiyor?

## <a name="resolution"></a>Çözüm

Genel muhasebeye nakil sırasında her fişin, hareket para birimi, muhasebe para birimi ve bu para birimleri **Genel muhasebe kurulumu** sayfasında tanımlanmışsa raporlama para birimi cinsinden dengelenmesi gerekir. (Fişler, toplam borçlar toplam alacaklara eşit olduğunda dengelenir.)

Yevmiye defteri satırları sayfasının alt kısmında toplamlar, muhasebe para birimi ve raporlama para birimi cinsinden gösterilir. Yabancı para birimi hareketleri için hareket para biriminde **gösterilmezler**. Ayrıca benzetim veya deftere nakil sırasında kullanıcıların aldığı hata iletisi, yalnızca muhasebe para birimi ve raporlama para birimindeki farklılıkları gösterir. Tek bir fişte birden fazla hareket para birimi olabileceğinden ve yevmiye defteri farklı hareket para birimlerindeki fişleri içerebileceğinden bunları hareket para birimi cinsinden göstermez. Bu nedenle, yalnızca bir hareket para birimi olan tüm fişlerin hareket para birimi tutarlarının dengelenmesi için el ile doğrulamanız önemlidir.

### <a name="transaction-currency"></a>Hareket para birimi

Sistem, benzetim ve deftere nakil sırasında her fişin işlem para biriminde yalnızca bir işlem para biriminin dengelendiğini doğrular. Girilen her fişte, hareket para birimi için bir veya daha fazla para birimi olabilir. Örneğin, genel yevmiye defterine girilen bir fişte euro (EUR) kullanan bir banka hesabından Kanada doları (CAD) kullanan bir banka hesabına para aktarıldığında iki hareket para birimi olabilir.

Fişte yalnızca bir hareket para birimi varsa toplam borçlar, bu fişteki işlem para biriminde toplam alacaklara eşit olmalıdır. Müşteriler, hareket para birimi tutarları dengelenmediğinden deftere nakil işleminin doğru şekilde yapılamadığı aşağıdaki senaryolarla karşılaştı:

- Toplam borçlar ve toplam alacaklar, hareket para biriminde **dengelenmedi** ancak muhasebe para birimi ve raporlama para birimi için dengelendi. Müşteri, fişin deftere nakledilmeye devam edeceğini varsaydı. Ancak bu varsayım yanlıştı. **Fişteki hareket para birimi tutarları, fişin tüm satırlarında aynı işlem para birimi olduğunda her zaman dengelenmelidir.**
- Fiş veri yönetim çerçevesi (DMF) aracılığıyla bir veri varlığıyla içe aktarıldı ve Kullanıcı hareket para birimi tutarlarının dengelenen olduğunu düşünmedi. İçe aktarma dosyasında, aynı miktarların ikiden fazla ondalık basamağı vardı ve tutarlar içeri aktarıldığında ikiden fazla ondalık basamak eklendi. Bu nedenle, kuruşun kesir kısmı kapalı olduğundan borçlar alacaklara eşit değildi. Gösterilen tutarların yalnızca iki ondalık basamağı olduğundan yevmiye defteri bu farkı fiş satırlarına yansıtmadı.
- Fiş, DMF aracılığıyla veri varlığı ile birlikte içeri aktarıldı ve kullanıcı, hareket para birimi tutarlarının dengelendiğini düşündü. **Fiş** dengelenmiş olsa da fişteki bazı satırlarda farklı hareket tarihleri vardı. **Fiş ve işlem tarihi** başına işlem para biriminden toplam borçları ve toplam alacakları eklediğinizde bunlar dengelenmedi. Bu gereksinim, sistemdeki genel yevmiye defteri aracılığıyla bir fiş girdiğinizde uygulanır. Ancak, DMF aracılığıyla bir veri varlığı ile bir fiş içe aktarıldığında zorlanmaz.

Desteklenen bir senaryoda, bir fişin birden fazla hareket para birimi olabilir. Bu durumda sistem, para birimleri eşleşmediğinden borçların hareket para birimindeki alacaklara eşit olduğunu **doğrulamaz**. Bunun yerine, sistem muhasebe para birimi ve raporlama para birimi tutarlarının dengelendiğini doğrular.

### <a name="accounting-currency"></a>Muhasebe para birimi

Fişin tüm satırlarında aynı hareket para birimi varsa ve hareket para birimi tutarları dengelendiyse sistem muhasebe para birimi tutarlarının dengeli olduğunu doğrular. Fiş yabancı para birimi cinsinden girilirse hareket para birimi tutarlarını muhasebe para birimine çevirmek için fiş satırlarındaki döviz kuru kullanılır. Öncelikle, fişin her satırı çevrilir ve iki ondalık basamağa yuvarlanır. Ardından toplam borçları ve toplam alacakları belirlemek için satırlar toplanır. Her satır çevrildiğinden toplam borçlar ve toplam alacaklar dengelenmeyebilir. Ancak aradaki farkın net değeri **Genel muhasebe parametreleri** sayfasında tanımlanan **Maksimum kuruş farkı** değeri dahilindeyse fiş deftere nakledilir ve fark otomatik olarak Kuruş farkı hesabına nakledilir.

Fişte birden fazla hareket para birimi varsa fişin her satırı muhasebe para birimine çevrilir ve iki onluk noktaya yuvarlanır, ardından toplam borçları ve toplam alacakları belirlemek için satırlar toplanır. Dengeli sayılabilmesi için borç ve kredilerin muhasebe para birimi cinsinden dengelenmiş olması gerekir.  Borç ve kredileri bakiyeye getirmek için muhasebe para birimi cinsinden fişe hiçbir zaman bir kuruş fark hesabı eklenmez. 

### <a name="reporting-currency"></a>Raporlama para birimi

Fişin tüm satırlarında aynı hareket para birimi varsa ve hareket para birimi tutarları dengelendiyse sistem, raporlama para birimi tutarlarının dengeli olduğunu doğrular. Fiş yabancı para birimi cinsinden girilirse hareket para birimi tutarlarını raporlama para birimine çevirmek için fiş satırlarındaki döviz kuru kullanılır. Öncelikle, fişin her satırı çevrilir ve iki ondalık basamağa yuvarlanır. Ardından toplam borçları ve toplam alacakları belirlemek için satırlar toplanır. Her satır çevrildiğinden toplam borçlar ve toplam alacaklar dengelenmeyebilir. Ancak aradaki fark **Genel muhasebe parametreleri** sayfasında tanımlanan **Raporlama para birimi cinsinden maksimum kuruş yuvarlama** değeri dahilindeyse fiş deftere nakledilir ve fark otomatik olarak Kuruş farkı hesabına nakledilir.

Fişte birden fazla hareket para birimi varsa fişin her satırı raporlama para birimine çevrilir ve iki onluk noktaya yuvarlanır, ardından toplam borçları ve toplam alacakları belirlemek için satırlar toplanır. Dengeli olarak kabul edilebilmesi için borç ve kredilerin raporlama para birimi cinsinden dengelenmiş olması gerekir.  Borç ve kredileri dengeye getirmek için raporlama para birimi cinsinden fişe hiçbir zaman bir akçe fark hesabı eklenmez.

### <a name="example-for-an-accounting-currency-imbalance"></a>Muhasebe para birimi dengesizliği örneği

> [!NOTE]
> Raporlama para birimi tutarı, işlem para birimi tutarından muhasebe para birimi tutarıyla aynı şekilde hesaplanır.

Döviz kuru: 1,5

| Satır | Fiş | Hesap | Para birimi | Ödeme (işlem) | Kredi (işlem) | Ödeme (Muhasebe) | Kredi (Muhasebe) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3.33 | | 5,00 (4,995) | |
| 2 | 001 | 1101-02 | EUR | 3.33 | | 5,00 (4,995) | |
| 3 | 001 | 1101-03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10,00 | | 15.00 |
| **Toplam** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

Muhasebe para birimi, 0,01 kadar bakiye dışında. Ancak, muhasebe para birimi cinsinden maksimum kuruş yuvarlaması en az 0,01 olduğu sürece, fark otomatik olarak kuruş farkı hesabına nakledilir ve fiş başarıyla deftere nakledilir.
