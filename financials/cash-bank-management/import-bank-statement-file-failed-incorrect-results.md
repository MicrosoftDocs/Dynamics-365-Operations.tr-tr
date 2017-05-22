---
title: "Banka ekstresi dosya alma sorunlarını giderme"
description: "Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 for Operations tarafından desteklenen düzenle eşleşmesi önemlidir. Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır. Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir. Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar. Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 97d48e978a82805fd9050668c6ddc51a1d3759be
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="bank-statement-file-import-troubleshooting"></a>Banka ekstresi dosya alma sorunlarını giderme

[!include[banner](../includes/banner.md)]


Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 for Operations tarafından desteklenen düzenle eşleşmesi önemlidir. Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır. Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir. Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar. Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar.

<a name="what-is-the-error"></a>Hata nedir?
------------------

Bir banka ekstresi doyasını içe aktarmaya çalıştıktan sonra, hatayı bulmak için Veri yönetimi iş geçmişine ve yürütme ayrıntılarına gidin. Hata, ekstre, bilanço ya da ekstre satırına yönlendirerek yardımcı olabilir. Ancak soruna neden olan alan veya öğeyi tanımlamanıza yardımcı olmaya yeterli olacak bilgi vermesi olası değildir.

## <a name="what-are-the-differences"></a>Farklar nelerdir?
Banka dosya düzeni tanımını, Microsoft Dynamics 365 for Operations içe aktarma tanımıyla kıyaslayın ve alanlar ve öğelerdeki farklılıkları not edin. Banka ekstreleri dosyasını ilgili örnek Dynamics 365 for Operations dosyasıyla karşılaştırın. ISO20022 dosyalarında farkları görmek kolaydır.

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

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Banka ekstresi dosyasının içeriğini kopyalayın ve bunları XML dosyasına yapıştırarak **PASTESTATEMENTFILEHERE**'ın yerine geçmesini sağlayın.

### <a name="debug-the-xslt"></a>XSLT hata ayıklama

Daha fazla bilgi için, bkz. <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Microsoft Visual Studio'yu Başlatın.
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

Banka ekstresi dosyasında uygun bir alan veya öğeyi almak için dönüştürmeyi ayarlayın. Sonra bu alanı veya öğeyi uygun Dynamics 365 for Operations öğesine eşleyin.

### <a name="debitcredit-indicator"></a>Borç/Alacak göstergesi

Bazı durumlarda, borçlar alacak olarak ve alacaklar borç olarak içeri aktarılmış olabilir. Bu sorunu gidermek için uygun XSLT'yi değiştirmeniz gerekir. Banka Ekstrelerini birden çok bankadan geliyorsa, bunların tümünün aynı borç/alacak yaklaşımını kullandığından veya ayrı dönüşümleri oluşturduğundan emin olun.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator şablonu
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit şablonu
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator şablonu

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Banka ekstresi biçimleri ve teknik düzenlerine örnekler
Aşağıdaki tablo gelişmiş banka mutabakatı içe alma dosyaları ve üç ilgili banka ekstresi örnek dosyalarının teknik düzen tanımlarını örnek olarak verir. Teknik düzenleri ve örnek dosya buradan indirebilirsiniz: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Teknik düzen tanımı                             | Banka ekstresi örnek dosya          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |





