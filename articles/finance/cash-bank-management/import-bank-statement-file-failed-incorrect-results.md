---
title: Banka ekstresi dosya alma sorunlarını giderme
description: Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 Finance tarafından desteklenen düzenle eşleşmesi önemlidir. Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır. Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir. Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar. Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5e7e6897f19dc0303ffbd3111f93669a91daa1b
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059388"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Banka ekstresi dosya alma sorunlarını giderme

[!include [banner](../includes/banner.md)]

Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 Finance tarafından desteklenen düzenle eşleşmesi önemlidir. Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır. Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir. Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar. Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar.

<a name="what-is-the-error"></a>Hata nedir?
------------------

Bir banka ekstresi doyasını içe aktarmaya çalıştıktan sonra, hatayı bulmak için Veri yönetimi iş geçmişine ve yürütme ayrıntılarına gidin. Hata, ekstre, bilanço ya da ekstre satırına yönlendirerek yardımcı olabilir. Ancak soruna neden olan alan veya öğeyi tanımlamanıza yardımcı olmaya yeterli olacak bilgi vermesi olası değildir.

## <a name="what-are-the-differences"></a>Farklar nelerdir?
Banka dosya düzeni tanımını, Finance içe aktarma tanımıyla kıyaslayın ve alanlar ve öğelerdeki farklılıkları not edin. Banka ekstreleri dosyasını ilgili örnek Finance dosyasıyla karşılaştırın. ISO20022 dosyalarında farkları görmek kolaydır.

## <a name="time-zone-differences-on-imported-bank-statements"></a>İçe aktarılan banka ekstrelerindeki saat dilimi farklılıkları
İçe aktarma dosyasındaki tarih-saat değerleri, Finance and Operations'da gösterilen tarih-saat değerlerinden farklı olabilir. Bu tutarsızlığı önlemek için **Veri kaynaklarını yapılandır** sayfasına bir saat dilimi tercihi girin. Bir saat dilimi tercihi hakkında daha fazla bilgi için bkz. [Gelişmiş banka mutabakatı içe aktarma işlemi](set-up-advanced-bank-reconciliation-import-process.md).

## <a name="transformations"></a>Dönüşümler
Genellikle, bu değişiklikler üç dönüşümden birinde yapılmalıdır. Her bir dönüşüm belirli bir standart için yazılır.

| Kaynak adı                                         | Dosya adı                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Hata ayıklama dönüştürmeleri
### <a name="adjust-the-bai2-and-mt940-files"></a>BAI2 ve MT940 dosyalarını ayarlama

BAI2 ve MT940 dosyaları metin tabanlı dosyalardır ve Genişletilebilir Stil Sayfası Dil Dönüşümleri (XSLT) hata ayıklamayı etkinleştirmek için bir düzeltme gerektirir. Program bu ayarlamayı bir dosya içe aktarıldığında yapar.

1.  Bir XML dosyası oluşturun ve aşağıdaki metni içine kopyalayın.

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Banka ekstresi dosyasının içeriğini kopyalayın ve bunları XML dosyasına yapıştırarak **PASTESTATEMENTFILEHERE**'ın yerine geçmesini sağlayın.

### <a name="debug-the-xslt"></a>XSLT hata ayıklama

Daha fazla bilgi için <https://msdn.microsoft.com/library/ms255605.aspx> konusuna bakın.

1.  Microsoft Visual Studio'ya başlayın.
2.  Bir konsol uygulaması oluşturun.
3.  Uygun XSLT'yi açın.
4.  XLST'yi ve özellikleri sayfasını tıklatın.
5.  Girişi, banka ekstresi dosyasının konumuna ayarlayın.
6.  Çıktı için bir konum ve dosya adı tanımlayın.
7.  Gerekli kesme noktalarını ayarlayın.
8.  Menüde **XML** &gt; **XSLT Hata Ayıklamayı Başlat**'ı tıklatın.

### <a name="format-the-xslt-output"></a>XSLT çıktısını biçimlendirin

Dönüşüm yürütüldüğünde, Visual Studio'da görüntüleyebileceğiniz bir çıktı dosyası oluşturur. Çıktı dosyasını hızlı şekilde biçimlendirmek için Ctrl+A, Ctrl+K, and Ctrl+D kullanın.

### <a name="adjust-the-transformation"></a>Dönüştürmeyi ayarlayın

Banka ekstresi dosyasında uygun bir alan veya öğeyi almak için dönüştürmeyi ayarlayın. Sonra bu alanı veya öğeyi uygun Finance öğesine eşleyin.

### <a name="debitcredit-indicator"></a>Borç/Alacak göstergesi

Bazı durumlarda, borçlar alacak olarak ve alacaklar borç olarak içeri aktarılmış olabilir. Bu sorunu gidermek için uygun XSLT'yi değiştirmeniz gerekir. Banka Ekstrelerini birden çok bankadan geliyorsa, bunların tümünün aynı borç/alacak yaklaşımını kullandığından veya ayrı dönüşümleri oluşturduğundan emin olun.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator şablonu
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit şablonu
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator şablonu

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Banka ekstresi biçimleri ve teknik düzenlerine örnekler
Aşağıdaki tablo gelişmiş banka mutabakatı içe alma dosyaları ve üç ilgili banka ekstresi örnek dosyalarının teknik düzen tanımlarını örnek olarak verir. Örnek dosyaları ve teknik düzenleri buradan indirebilirsiniz: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Teknik düzen tanımı                             | Banka ekstresi örnek dosya          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |





