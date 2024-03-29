---
title: Banka ekstresi dosyasını içeri aktarma sorunlarını giderme
description: Bu makalede, banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkan sorunların nasıl düzeltileceği açıklanır.
author: angelad116
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44658ea48b9f7dae76c34c5f3d8828c9e8c4ac32
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151775"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Banka ekstresi dosyasını içeri aktarma sorunlarını giderme

[!include [banner](../includes/banner.md)]

>[!NOTE]
>Bu işlevler, Eylül 2022'de kullanımdan kaldırılacağından yeni kullanıcılar elektronik raporlama kullanmalıdır.

Bankadan gelen banka ekstresi dosyasının, Microsoft Dynamics 365 Finance tarafından desteklenen düzenle eşleşmesi önemlidir. Banka ekstreleri için sıkı standartlar bulunduğundan çoğu tümleştirme doğru şekilde çalışacaktır. Ancak, bazen ekstre dosyası alınamayabilir veya hatalı sonuçlara sahip olabilir. Genellikle, bu sorunlar banka ekstresi dosyasındaki küçük farklılıklar nedeniyle ortaya çıkar. Bu makale, bu farklılıkları gidermeyi ve sorunların nasıl çözüleceğini açıklar.

## <a name="what-is-the-error"></a>Hata nedir?

Bir banka ekstresi doyasını içe aktarmaya çalıştıktan sonra, hatayı bulmak için Veri yönetimi iş geçmişine ve yürütme ayrıntılarına gidin. Hata, ekstre, bilanço ya da ekstre satırına yönlendirerek yardımcı olabilir. Ancak soruna neden olan alan veya öğeyi tanımlamanıza yardımcı olmaya yeterli olacak bilgi vermesi olası değildir.

> [!NOTE]
> İçe aktarılan Banka ekstreleri yalnızca bir seferde tek bir nokta ile örtüşebilir.  Örneğin, bir ekstrenin bitiş tarihi 1 Ocak 2021 12:00 ÖÖ ise sonraki ekstrenin başlangıç tarihi 1 Ocak 2021 12:00 ÖÖ olabilir.

## <a name="what-are-the-differences"></a>Farklar nelerdir?
Banka dosya düzeni tanımını, Finance içe aktarma tanımıyla kıyaslayın ve alanlar ve öğelerdeki farklılıkları not edin. Banka ekstreleri dosyasını ilgili örnek Finance dosyasıyla karşılaştırın. ISO20022 dosyalarında farkları görmek kolaydır.

## <a name="time-zone-differences-on-imported-bank-statements"></a>İçe aktarılan banka ekstrelerindeki saat dilimi farklılıkları
İçeri aktarma dosyasındaki tarih-saat değerleri, finans ve operasyon uygulamasında gösterilen tarih-saat değerlerinden farklı olabilir. Bu tutarsızlığı önlemek için **Veri kaynaklarını yapılandır** sayfasına bir saat dilimi tercihi girin. Bir saat dilimi tercihi girme hakkında daha fazla bilgi için bkz. [Gelişmiş banka mutabakatı içe aktarma işlemi](set-up-advanced-bank-reconciliation-import-process.md).

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
Aşağıdaki tablo gelişmiş banka mutabakatı içe alma dosyaları ve üç ilgili banka ekstresi örnek dosyalarının teknik düzen tanımlarını örnek olarak verir. Örnek dosyaları ve teknik düzenleri buradan indirebilirsiniz: [İçe aktarma dosyası örnekleri](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Teknik düzen tanımı                             | Banka ekstresi örnek dosya          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

