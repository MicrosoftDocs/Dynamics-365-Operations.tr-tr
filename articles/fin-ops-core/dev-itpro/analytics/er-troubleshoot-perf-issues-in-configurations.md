---
title: ER yapılandırmalarında performans sorunlarını giderme
description: Bu konu, Elektronik raporlama (ER) yapılandırmalarında performans sorunlarının nasıl bulunabileceğini ve düzeltileceğini açıklamaktadır.
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: d77c2aad904ba911ac19009d6a981ea4153aaa48
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216877"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>ER yapılandırmalarında performans sorunlarını giderme

Bu konu, [Elektronik raporlama](general-electronic-reporting.md) (ER) [yapılandırmalarında](general-electronic-reporting.md#Configuration) performans sorunlarının nasıl bulunabileceğini ve çözüleceğini açıklamaktadır.

Genellikle, performans araştırmaları birkaç adımdan oluşur.

1. Veri [toplayın](#collecting-data).
2. Toplanan verileri analiz edin.
3. Analiz sonuçlarına göre, [değişiklik yapmak](#making-changes) için ER yapılandırmalarını kullanın veya daha fazla veri toplamaya karar verin.

## <a name="troubleshooting"></a>Sorun Giderme

### <a name="analyze-execution-time"></a>Yürütme süresini çözümleme

Yürütme süresi, aynı ortamda çalışan diğer görevler ve ilk kez çağrıldığında veri kullanan önbellekleme gibi öngörülemeyen etkenlere bağlı olabilir. Bu nedenle, yürütmeyi ve ölçümü birkaç kere tekrarlamanız gerekir.

Bazı durumlarda, performans sorunlarına raporlama için kullanılan bir ER biçimi yapılandırması neden olmaz. Bunun yerine, bu ER biçimi yapılandırmasını açmak için kullanılan X++ kodundan kaynaklanır.

1. [Eylem merkezinde](#infolog-time) veya [olay günlüğünde](#event-log-time), raporun yürütme zamanına bakın.
2. Rapordaki yürütme süresini, senaryodaki toplam yürütme süresiyle karşılaştırın.
3. Raporun yürütme zamanı, toplam yürütme süresinden çok daha azsa, raporun işlediği veri miktarını göz önünde bulundurun:

    - Rapor az miktarda veri işliyorsa, sorun yapılandırmayı yükleme süresiyle alakalı olabilir.
    - Rapor büyük miktarda veri işliyorsa, sorun X++ önişlemesi ile ilgili olabilir. Bu olay setini çözümlemek için [İzleme ayrıştırıcı](#analyze-trace-parser-trace)'yı kullanın.

    Diğer olay setleri için sonraki bölümlere bakın.

4. Yürütme süresinin veri miktarıyla nasıl ilişkili olduğunu belirlemek için farklı miktarda veriyle ilgili birden çok test çalıştırın.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>İzleme ayrıştırıcı izlemelerini çözümleme

Küçük bir örnek hazırlayın veya rapor oluşturmanın rasgele bölümleri sırasında birkaç izleme toplayın.

Sonra, [İzleme ayrıştırıcısında](#trace-parser) standart bir alttan üste çözümleme yapın ve aşağıdaki soruları yanıtlayın:

- En çok zaman tüketen yöntemler hangisidir?
- Bu yöntemler genel sürenin ne kadarını kullanır?

Aynı soruları sorgular için yanıtlayın.

Yöntemlerin önünde "ER" öneki görürseniz sonraki bölüme geçin.

Yöntem ve sorguların uygulama paketinden geldiğini görürseniz, genel iyileştirmeler (örneğin, dizinler oluşturun) yapmayı düşünün.

Çağrı sayısını analiz edin. Sayı, beklenenden önemli ölçüde yüksekse ilgili düğümlerin karşılık gelen düğümlerini önbelleğe almayı düşünebilirsiniz.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Veritabanı çağrılarını çözümleme

Küçük miktarda veri içeren bir örnek hazırlayın, böylece bir [Er izlemesi](#electronic-reporting-traces) toplayabilirsiniz.

Sonra, izlemeyi ER model eşleme tasarımcısında açın ve sayfanın altına bakın. Aşağıdaki soruları yanıtlayın:

- Herhangi bir sorgu yinelemesi var mı? Varsa, aşağıdaki çözümlerden birini deneyin:

    - Bir üst kayıt içinde birkaç çağrı olduğunu düşünüyorsanız [önbelleğe almayı kullanın](#use-caching).
    - Farklı kayıtlar içinde aynı kayda çağrı olduğunu düşünüyorsanız, [önbelleğe alınmış, parametreli hesaplanan alan kullanın](#cached-parameterized).
    - Veritabanından önemli sayıda farklı kayıt okumanız halinde [**JOIN** veri kaynağı kullanın](#use-join-datasource).

- Sorgu ve alınan kayıtların sayısı, genel veri miktarına karşılık geliyor mu? Örneğin, bir belgede 10 satır varsa istatistikler, raporun 10 satır veya 1.000 satır ayıkladığını gösteriyor mu? Çok sayıda alınan kaydınız varsa, aşağıdaki çözümlerden birini deneyin:

    - SQL Server tarafında veri işlemek için [**WHERE** işlevi yerine **FILTER** işlevini kullanın](#filter).
    - Aynı verileri getirmeyi önlemek için önbelleğe almayı kullanın.
    - Özette aynı verileri getirmeyi önlemek için [toplanan veri işlevlerini kullanın](#collected-data).

### <a name="analyze-perfview-traces"></a>PerfView izlemelerini analiz etme

[PerfView ](#perfview), deneyimli geliştiriciler için bir araçtır. Aşağıdaki adımlar hakkında daha ayrıntılı bilgi için bkz. [Duvar Saati Süresi İncelemenin Temelleri](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. İş parçacığı süresini kullanarak bir izleme toplayın.
2. Yalnızca yapılandırma yürütmesi olan iş parçacığını filtrelemek için **runUnattended** kullanan yığınları dahil edin. (**IncPats** giriş kutusuna **runUnattended** öğesini ekleyin.)
3. Tüm CPU, ağ ve engellenme süresini katlayın.
4. [PerfView için ER ön ayarlarını](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml) yükleyin.
5. **ER** \> **Diğer ön ayar**'ı seçin.
6. Adlara bakın:

    - Büyük olasılıkla en fazla kullanılan platform kodunu görürsünüz.
    - Çift dokunup (veya çift tıklayarak) **arananlar**'ı inceleyebilirsiniz.

        "ERExpression" önekine sahip sınıflar bulursanız ve bunlar formüllerle ilişkili işlevlerse, sınıf adını temel alan işlev adını tahmin edebilirsiniz ve öznitelikleri görmek için ER deposuna bakabilirsiniz.

### <a name="fixes"></a>Çözümler

- CPU süresinin çoğunluğunun sorgu tarafından tüketildiğini görürseniz, sorgu sayısını azaltmayı deneyin:

    - Çoğaltılan sorgular için [ER izlemesini gözden geçirin](#analyze-database-calls).
    - Kaç kaydın getirildiğine bakın ve teorik olarak ne kadar veri getirilmesi gerektiğini değerlendirin.

- CPU zamanının çoğunun işlevler tarafından kullanıldığını görürseniz, yapılandırmada en fazla kaynağı tüketen yeri bulmaya çalışın.
- CPU zamanının çoğunun veri toplama işlevleri tarafından tüketildiğini görürseniz, bunları model eşleme tarafında *SQL gruplama ölçütü* ile değiştirmeyi düşünebilirsiniz.

### <a name="collecting-data"></a><a name="collecting-data"></a>Veri toplama

Ortamınıza bağlı olarak, kullanılabilir verileri toplamanın birkaç yolu vardır:

- Toplam çalışma zamanını alın:

    - Eylem merkezinden
    - Olay günlüğünden

- Yürütme profilini çıkarın:

    - ER araçlarını kullanarak
    - Izleme ayrıştırıcısı kullanarak
    - PerfView kullanarak

#### <a name="collecting-data-in-a-production-environment"></a>Üretim ortamında verileri toplama

Bazen, sorunlar yalnızca üretim ortamında yeniden oluşturulabilir. Veriler aşağıdaki yollarla toplanabilir:

- [İzleme ayrıştırıcı](../perf-test/trace-trace-tutorial.md) izlemeleri kullanarak
- [ER yürütme](trace-execution-er-troubleshoot-perf.md) izlemelerini kullanarak
- Toplam yürütme süresini kullanarak

#### <a name="collecting-data-in-a-development-environment"></a>Geliştirme ortamında verileri toplama

Üretim ortamında kullanılabilen araçlara ek olarak, geliştirme ortamında kullanabileceğiniz çeşitli araçlar vardır:

- Olay günlüğü (Microsoft-Dynamics-ElectronicReporting). Bu günlük, size toplam yürütme süresini verebilir.
- PerfView gibi yaygın .NET araçları.

Ek olarak, geliştirme ortamı size daha fazla esneklik sağlar. Örneğin, yürütme süresinin nasıl etkilendiğini görmek için raporların belirli parçalarını kapatabilirsiniz.

### <a name="tools"></a><a name="tools"></a>Araçlar

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Eylem merkezindeki yürütme süresi

ER, Eylem merkezindeki yapılandırmanın yürütme süresini gösterebilir. Bu seçenek yalnızca belirli bir kullanıcı ve belirli bir şirket için ve yalnızca etkileşimli oturumlar için kullanılabilir. Bu özelliği kullanılabilir hale getirmek için aşağıdaki adımları izleyin.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Kullanıcı parametreleri** iletişim kutusunda, **Dosya oluşum süresini göster** seçeneğini **Evet** olarak ayarlayın.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Olay günlüğündeki yürütme süresi

1. Windows Olay Görüntüleyici'yi açın.
2. **Uygulamalar ve Hizmetler günlükleri** altında, **Microsoft-Dynamics-ElectronicReporting/Operational**'ı açın.
3. Bu olaylar, geçen süre bilgilerini içerdiğinden, **EventID = 2** olan **FormatMapingrun** olaylarını arayın.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>İzleme ayrıştırıcı izlemeleri 

ER, X++ içinde uygulandığından, performansı analiz etmek için yaygın X++ araçlarını kullanabilirsiniz. Daha fazla bilgi için bkz. [İzleme ayrıştırıcısı kullanarak izlemeleri alma](../perf-test/trace-trace-tutorial.md).

Bu yaklaşımın birkaç sınırlaması bulunmaktadır. ER'nin bir parçası C#'ta uygulandığından, ayrıntıların tümü kullanılabilir olmayacak. Ancak, veri kullanım ayrıntılarını görüntüleyebilirsiniz. Ek olarak, uzun rapor çalışmaları izleme depolama sınırlamalarını aşabilir.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER izleri

ER, kendi izlemelerini toplayabilir ve bu izlemeler için görselleştirme ve analiz araçlarına sahiptir. Daha fazla bilgi için, bkz. [Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Hem X++ hem de .NET platformunun üzerine uygulandığı için, yaygın .NET araçlarını kullanabilirsiniz. Örneğin, ücretsiz [PerfView](https://github.com/Microsoft/perfview) aracını kullanabilirsiniz.

Ayrıca, komut satırından da veri toplayabilirsiniz. Örneğin, aşağıdaki Windows PowerShell betiği, makinede herhangi bir biçim yürütmesi durduruluncaya kadar yürütme süresini toplar.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Bu yaklaşımın birkaç sınırlaması bulunmaktadır. Makineye yönetici erişiminiz olmalıdır. Ek olarak, büyük bir öğrenme eğrisi bulunduğundan deneyimli bir geliştirici olmalısınız.

### <a name="making-changes"></a><a name="making-changes"></a>Değişiklik yapma

#### <a name="use-caching"></a><a name="use-caching"></a>Önbelleğe almayı kullanma

Önbelleğe alma, veriyi tekrar getirmek için gereken süreyi azaltıyor olsa da bellekten harcar. Alınan veri miktarının çok büyük olmadığı durumlarda önbelleğe almayı kullanın. Önbelleğe almayı nasıl kullanacağınıza dair daha fazla bilgi ve bir örnek için bkz. [Yürütme izlemesinin bilgilerine dayalı olarak model eşlemeyi geliştirme](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Önbelleğe alınmış, parametreli hesaplanan alan kullanma

Bazı durumlarda, değerlerin tekrar aranması gerekir. Örnek arasında hesap adları ve hesap numaraları sayılabilir. Zamandan tasarruf etmek için en üst düzeyde parametreleri olan bir hesaplanmış alan oluşturabilir ve bu alanı önbelleğe ekleyebilirsiniz.

Bu yaklaşımı yalnızca, önbelleğe alınan verilerin boyutu küçükse kullanmanızı öneririz. Daha fazla bilgi için bkz. [Parametreli CALCULATED FIELD veri kaynakları ekleyerek ER çözümlerinin performansını iyileştirme](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>JOIN veri kaynağı kullanma

**JOIN** veri kaynağı, birkaç bağlantılı kaydın tek bir sorgu ile alınmasına olanak tanır. Her bağlı kaydı getirmek için ayrı bir sorgu kullanılması gerekmez. Örneğin, 1.000 satırınız varsa ve her satır ilişkisine göre madde verileri alıyorsanız, 1.001 sorguya sahip olursunuz (= 1.000 + 1). **JOIN** veri kaynağı kullanırsanız, aynı verileri getirmek için yalnızca bir sorgu kullanırsınız. Daha fazla bilgi için bkz. [ER model eşlemelerinde birden çok uygulama tablosundan veri almak için JOIN veri kaynaklarını kullanma](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>WHERE işlevi yerine FILTER fonksiyonunu kullanma

**[FILTER](er-functions-list-filter.md)** işlevi, koşulları SQL Server'da çalıştırırken **WHERE** işlevi listedeki tüm verileri getirir (bir seferde bir kayıt) ve her kayıt için koşulu uygular. Örneğin, 1.000 kayıttan bir kayıt seçmek istiyorsunuz. **WHERE** işlevini kullanırsanız, 1.000 kayıdın tümü getirilecektir. Ancak, **FILTER** işlevini kullanırsanız, yalnızca bir kayıt getirilecektir. **FILTER** aynı zamanda veritabanı tarafındaki dizinleri de kullanabilir.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Toplanan veri işlevlerini veya birikmiş veri veri kaynağını kullanma

Yapılandırmanız, rapora göre daha önce getirilen verileri özetleyen bir *gruplama ölçütüne* sahipse, bileşen tüm verileri yeniden alır. Toplanan veri işlevlerini kullanarak, ER'nin ilk getirme sırasında veri birikmesine olanak tanırsınız. Daha fazla bilgi için bkz. [Sayım ve toplama işlemlerini yapmak için ER Yapılandırma biçimi](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Yapılandırmanın parçalarını X++ ile yeniden yazın

ER, uzantılar da dahil olmak üzere tablo ve sınıfların arama yöntemlerini destekler. Performansı artırmaya yardımcı olmak için, X++ ile model eşleme parçalarını yeniden yazmayı düşünün.

ER, aşağıdaki kaynaklardaki verileri kullanabilir:

- Sınıflar ( **nesne** ve **sınıf** veri kaynakları)
- Tablolar (**tablo** ve **tablo kayıtları** veri kaynakları)

[ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory), önceden hesaplanmış verileri çağrı kodundan göndermek için de bir yol sağlar. Uygulama paketi bu yaklaşım için çok sayıda örnek içerir.
