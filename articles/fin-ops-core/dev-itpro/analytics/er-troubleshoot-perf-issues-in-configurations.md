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
# <a name="troubleshooting-performance-issues-in-er-configurations"></a><span data-ttu-id="dd142-103">ER yapılandırmalarında performans sorunlarını giderme</span><span class="sxs-lookup"><span data-stu-id="dd142-103">Troubleshooting performance issues in ER configurations</span></span>

<span data-ttu-id="dd142-104">Bu konu, [Elektronik raporlama](general-electronic-reporting.md) (ER) [yapılandırmalarında](general-electronic-reporting.md#Configuration) performans sorunlarının nasıl bulunabileceğini ve çözüleceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="dd142-104">This topic explains how to find and solve performance issues in [Electronic reporting](general-electronic-reporting.md) (ER) [configurations](general-electronic-reporting.md#Configuration).</span></span>

<span data-ttu-id="dd142-105">Genellikle, performans araştırmaları birkaç adımdan oluşur.</span><span class="sxs-lookup"><span data-stu-id="dd142-105">Typically, performance investigation consists of several steps.</span></span>

1. <span data-ttu-id="dd142-106">Veri [toplayın](#collecting-data).</span><span class="sxs-lookup"><span data-stu-id="dd142-106">[Collect](#collecting-data) data.</span></span>
2. <span data-ttu-id="dd142-107">Toplanan verileri analiz edin.</span><span class="sxs-lookup"><span data-stu-id="dd142-107">Analyze the collected data.</span></span>
3. <span data-ttu-id="dd142-108">Analiz sonuçlarına göre, [değişiklik yapmak](#making-changes) için ER yapılandırmalarını kullanın veya daha fazla veri toplamaya karar verin.</span><span class="sxs-lookup"><span data-stu-id="dd142-108">Based on the results of the analysis, use ER configurations to [make changes](#making-changes), or decide to collect more data.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="dd142-109">Sorun Giderme</span><span class="sxs-lookup"><span data-stu-id="dd142-109">Troubleshooting</span></span>

### <a name="analyze-execution-time"></a><span data-ttu-id="dd142-110">Yürütme süresini çözümleme</span><span class="sxs-lookup"><span data-stu-id="dd142-110">Analyze execution time</span></span>

<span data-ttu-id="dd142-111">Yürütme süresi, aynı ortamda çalışan diğer görevler ve ilk kez çağrıldığında veri kullanan önbellekleme gibi öngörülemeyen etkenlere bağlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-111">Execution time can depend on unpredictable factors, such as other tasks that are running in the same environment and caching that uses data when it's called for the first time.</span></span> <span data-ttu-id="dd142-112">Bu nedenle, yürütmeyi ve ölçümü birkaç kere tekrarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd142-112">Therefore, you should repeat the execution and measurement several times.</span></span>

<span data-ttu-id="dd142-113">Bazı durumlarda, performans sorunlarına raporlama için kullanılan bir ER biçimi yapılandırması neden olmaz.</span><span class="sxs-lookup"><span data-stu-id="dd142-113">Sometimes, performance issues aren't caused by an ER format configuration that is used for reporting.</span></span> <span data-ttu-id="dd142-114">Bunun yerine, bu ER biçimi yapılandırmasını açmak için kullanılan X++ kodundan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="dd142-114">Instead, they are caused by the X++ code that is used to open that ER format configuration.</span></span>

1. <span data-ttu-id="dd142-115">[Eylem merkezinde](#infolog-time) veya [olay günlüğünde](#event-log-time), raporun yürütme zamanına bakın.</span><span class="sxs-lookup"><span data-stu-id="dd142-115">In either the [Action center](#infolog-time) or the [event log](#event-log-time), look at the execution time of the report.</span></span>
2. <span data-ttu-id="dd142-116">Rapordaki yürütme süresini, senaryodaki toplam yürütme süresiyle karşılaştırın.</span><span class="sxs-lookup"><span data-stu-id="dd142-116">Compare the execution time of the report with the total execution time in the scenario.</span></span>
3. <span data-ttu-id="dd142-117">Raporun yürütme zamanı, toplam yürütme süresinden çok daha azsa, raporun işlediği veri miktarını göz önünde bulundurun:</span><span class="sxs-lookup"><span data-stu-id="dd142-117">If the execution time of the report is much less than the total execution time, consider the amount of data that the report processes:</span></span>

    - <span data-ttu-id="dd142-118">Rapor az miktarda veri işliyorsa, sorun yapılandırmayı yükleme süresiyle alakalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-118">If the report processes a small amount of data, the issue might involve the loading time of the configuration.</span></span>
    - <span data-ttu-id="dd142-119">Rapor büyük miktarda veri işliyorsa, sorun X++ önişlemesi ile ilgili olabilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-119">If the report processes a large amount of data, the issue might involve preprocessing X++.</span></span> <span data-ttu-id="dd142-120">Bu olay setini çözümlemek için [İzleme ayrıştırıcı](#analyze-trace-parser-trace)'yı kullanın.</span><span class="sxs-lookup"><span data-stu-id="dd142-120">Use [Trace parser](#analyze-trace-parser-trace) to analyze this case.</span></span>

    <span data-ttu-id="dd142-121">Diğer olay setleri için sonraki bölümlere bakın.</span><span class="sxs-lookup"><span data-stu-id="dd142-121">For other cases, see the next sections.</span></span>

4. <span data-ttu-id="dd142-122">Yürütme süresinin veri miktarıyla nasıl ilişkili olduğunu belirlemek için farklı miktarda veriyle ilgili birden çok test çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="dd142-122">Run multiple tests that involve different amounts of data to determine how the execution time depends on the amount of data.</span></span>

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a><span data-ttu-id="dd142-123">İzleme ayrıştırıcı izlemelerini çözümleme</span><span class="sxs-lookup"><span data-stu-id="dd142-123">Analyze Trace parser traces</span></span>

<span data-ttu-id="dd142-124">Küçük bir örnek hazırlayın veya rapor oluşturmanın rasgele bölümleri sırasında birkaç izleme toplayın.</span><span class="sxs-lookup"><span data-stu-id="dd142-124">Prepare a small example, or collect several traces during random parts of the report generation.</span></span>

<span data-ttu-id="dd142-125">Sonra, [İzleme ayrıştırıcısında](#trace-parser) standart bir alttan üste çözümleme yapın ve aşağıdaki soruları yanıtlayın:</span><span class="sxs-lookup"><span data-stu-id="dd142-125">Then, in [Trace parser](#trace-parser), do a standard bottom-to-up analysis, and answer the following questions:</span></span>

- <span data-ttu-id="dd142-126">En çok zaman tüketen yöntemler hangisidir?</span><span class="sxs-lookup"><span data-stu-id="dd142-126">What are the top methods in terms of time consumption?</span></span>
- <span data-ttu-id="dd142-127">Bu yöntemler genel sürenin ne kadarını kullanır?</span><span class="sxs-lookup"><span data-stu-id="dd142-127">What part of the overall time do those methods use?</span></span>

<span data-ttu-id="dd142-128">Aynı soruları sorgular için yanıtlayın.</span><span class="sxs-lookup"><span data-stu-id="dd142-128">Answer the same questions for queries.</span></span>

<span data-ttu-id="dd142-129">Yöntemlerin önünde "ER" öneki görürseniz sonraki bölüme geçin.</span><span class="sxs-lookup"><span data-stu-id="dd142-129">If you see that methods are prefixed with "ER," move on to the next section.</span></span>

<span data-ttu-id="dd142-130">Yöntem ve sorguların uygulama paketinden geldiğini görürseniz, genel iyileştirmeler (örneğin, dizinler oluşturun) yapmayı düşünün.</span><span class="sxs-lookup"><span data-stu-id="dd142-130">If you see that methods or queries originated in the application suite, consider generic optimizations (for example, create indexes).</span></span>

<span data-ttu-id="dd142-131">Çağrı sayısını analiz edin.</span><span class="sxs-lookup"><span data-stu-id="dd142-131">Analyze the number of calls.</span></span> <span data-ttu-id="dd142-132">Sayı, beklenenden önemli ölçüde yüksekse ilgili düğümlerin karşılık gelen düğümlerini önbelleğe almayı düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-132">If the number is significantly higher than expected, consider caching the corresponding nodes of the configuration.</span></span>

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a><span data-ttu-id="dd142-133">Veritabanı çağrılarını çözümleme</span><span class="sxs-lookup"><span data-stu-id="dd142-133">Analyze database calls</span></span>

<span data-ttu-id="dd142-134">Küçük miktarda veri içeren bir örnek hazırlayın, böylece bir [Er izlemesi](#electronic-reporting-traces) toplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-134">Prepare an example that has a small amount of data, so that you can collect an [ER trace](#electronic-reporting-traces).</span></span>

<span data-ttu-id="dd142-135">Sonra, izlemeyi ER model eşleme tasarımcısında açın ve sayfanın altına bakın.</span><span class="sxs-lookup"><span data-stu-id="dd142-135">Then open the trace in the ER model mapping designer, and look at the bottom of the page.</span></span> <span data-ttu-id="dd142-136">Aşağıdaki soruları yanıtlayın:</span><span class="sxs-lookup"><span data-stu-id="dd142-136">Answer the following questions:</span></span>

- <span data-ttu-id="dd142-137">Herhangi bir sorgu yinelemesi var mı?</span><span class="sxs-lookup"><span data-stu-id="dd142-137">Is there any query duplication?</span></span> <span data-ttu-id="dd142-138">Varsa, aşağıdaki çözümlerden birini deneyin:</span><span class="sxs-lookup"><span data-stu-id="dd142-138">If there is, consider one of the following fixes:</span></span>

    - <span data-ttu-id="dd142-139">Bir üst kayıt içinde birkaç çağrı olduğunu düşünüyorsanız [önbelleğe almayı kullanın](#use-caching).</span><span class="sxs-lookup"><span data-stu-id="dd142-139">[Use caching](#use-caching) if you think that there are several calls inside one parent record.</span></span>
    - <span data-ttu-id="dd142-140">Farklı kayıtlar içinde aynı kayda çağrı olduğunu düşünüyorsanız, [önbelleğe alınmış, parametreli hesaplanan alan kullanın](#cached-parameterized).</span><span class="sxs-lookup"><span data-stu-id="dd142-140">[Use a cached, parameterized calculated field](#cached-parameterized) if you think that there are calls to the same record inside different records.</span></span>
    - <span data-ttu-id="dd142-141">Veritabanından önemli sayıda farklı kayıt okumanız halinde [**JOIN** veri kaynağı kullanın](#use-join-datasource).</span><span class="sxs-lookup"><span data-stu-id="dd142-141">[Use a **JOIN** data source](#use-join-datasource) if you have to read to a substantial number of different records from a database.</span></span>

- <span data-ttu-id="dd142-142">Sorgu ve alınan kayıtların sayısı, genel veri miktarına karşılık geliyor mu?</span><span class="sxs-lookup"><span data-stu-id="dd142-142">Does the number of queries and fetched records correspond to the overall amount of data?</span></span> <span data-ttu-id="dd142-143">Örneğin, bir belgede 10 satır varsa istatistikler, raporun 10 satır veya 1.000 satır ayıkladığını gösteriyor mu?</span><span class="sxs-lookup"><span data-stu-id="dd142-143">For example, if a document has 10 lines, do the statistics show that the report extracts 10 lines or 1,000 lines?</span></span> <span data-ttu-id="dd142-144">Çok sayıda alınan kaydınız varsa, aşağıdaki çözümlerden birini deneyin:</span><span class="sxs-lookup"><span data-stu-id="dd142-144">If you have a substantial number of fetched records, consider one of the following fixes:</span></span>

    - <span data-ttu-id="dd142-145">SQL Server tarafında veri işlemek için [**WHERE** işlevi yerine **FILTER** işlevini kullanın](#filter).</span><span class="sxs-lookup"><span data-stu-id="dd142-145">[Use the **FILTER** function instead of the **WHERE** function](#filter) to process data on the SQL Server side.</span></span>
    - <span data-ttu-id="dd142-146">Aynı verileri getirmeyi önlemek için önbelleğe almayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="dd142-146">Use caching to avoid fetching the same data.</span></span>
    - <span data-ttu-id="dd142-147">Özette aynı verileri getirmeyi önlemek için [toplanan veri işlevlerini kullanın](#collected-data).</span><span class="sxs-lookup"><span data-stu-id="dd142-147">[Use collected data functions](#collected-data) to avoid fetching the same data for summarization.</span></span>

### <a name="analyze-perfview-traces"></a><span data-ttu-id="dd142-148">PerfView izlemelerini analiz etme</span><span class="sxs-lookup"><span data-stu-id="dd142-148">Analyze PerfView traces</span></span>

<span data-ttu-id="dd142-149">[PerfView ](#perfview), deneyimli geliştiriciler için bir araçtır.</span><span class="sxs-lookup"><span data-stu-id="dd142-149">[PerfView](#perfview) is a tool for experienced developers.</span></span> <span data-ttu-id="dd142-150">Aşağıdaki adımlar hakkında daha ayrıntılı bilgi için bkz. [Duvar Saati Süresi İncelemenin Temelleri](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span><span class="sxs-lookup"><span data-stu-id="dd142-150">For more detailed information about the following steps, see [Wall Clock Time Investigation Basics](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).</span></span>

1. <span data-ttu-id="dd142-151">İş parçacığı süresini kullanarak bir izleme toplayın.</span><span class="sxs-lookup"><span data-stu-id="dd142-151">Collect a trace by using thread time.</span></span>
2. <span data-ttu-id="dd142-152">Yalnızca yapılandırma yürütmesi olan iş parçacığını filtrelemek için **runUnattended** kullanan yığınları dahil edin.</span><span class="sxs-lookup"><span data-stu-id="dd142-152">Include only stacks that use **runUnattended**, to filter only the thread that has configuration execution.</span></span> <span data-ttu-id="dd142-153">(**IncPats** giriş kutusuna **runUnattended** öğesini ekleyin.)</span><span class="sxs-lookup"><span data-stu-id="dd142-153">(Add **runUnattended** to the **IncPats** input box.)</span></span>
3. <span data-ttu-id="dd142-154">Tüm CPU, ağ ve engellenme süresini katlayın.</span><span class="sxs-lookup"><span data-stu-id="dd142-154">Fold all CPU, network, and blocked time.</span></span>
4. <span data-ttu-id="dd142-155">[PerfView için ER ön ayarlarını](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml) yükleyin.</span><span class="sxs-lookup"><span data-stu-id="dd142-155">Load [ER presets for PerfView](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).</span></span>
5. <span data-ttu-id="dd142-156">**ER** \> **Diğer ön ayar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="dd142-156">Select **ER** \> **Other preset**.</span></span>
6. <span data-ttu-id="dd142-157">Adlara bakın:</span><span class="sxs-lookup"><span data-stu-id="dd142-157">Look at the names:</span></span>

    - <span data-ttu-id="dd142-158">Büyük olasılıkla en fazla kullanılan platform kodunu görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="dd142-158">You will probably see the platform code that consumes the most time.</span></span>
    - <span data-ttu-id="dd142-159">Çift dokunup (veya çift tıklayarak) **arananlar**'ı inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-159">You can double-tap (or double-click) and go up through **callees**.</span></span>

        <span data-ttu-id="dd142-160">"ERExpression" önekine sahip sınıflar bulursanız ve bunlar formüllerle ilişkili işlevlerse, sınıf adını temel alan işlev adını tahmin edebilirsiniz ve öznitelikleri görmek için ER deposuna bakabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-160">If you find classes that have the prefix "ERExpression," and if they are functions that are related to formulas, you can guess the function name based on the class name, and you can look at the ER repo to view the attributes.</span></span>

### <a name="fixes"></a><span data-ttu-id="dd142-161">Çözümler</span><span class="sxs-lookup"><span data-stu-id="dd142-161">Fixes</span></span>

- <span data-ttu-id="dd142-162">CPU süresinin çoğunluğunun sorgu tarafından tüketildiğini görürseniz, sorgu sayısını azaltmayı deneyin:</span><span class="sxs-lookup"><span data-stu-id="dd142-162">If you see that most of the CPU time is consumed by queries, try to reduce the number of queries:</span></span>

    - <span data-ttu-id="dd142-163">Çoğaltılan sorgular için [ER izlemesini gözden geçirin](#analyze-database-calls).</span><span class="sxs-lookup"><span data-stu-id="dd142-163">[Review the ER trace](#analyze-database-calls) for duplicated queries.</span></span>
    - <span data-ttu-id="dd142-164">Kaç kaydın getirildiğine bakın ve teorik olarak ne kadar veri getirilmesi gerektiğini değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="dd142-164">See how many records are fetched, and evaluate how much data should theoretically be fetched.</span></span>

- <span data-ttu-id="dd142-165">CPU zamanının çoğunun işlevler tarafından kullanıldığını görürseniz, yapılandırmada en fazla kaynağı tüketen yeri bulmaya çalışın.</span><span class="sxs-lookup"><span data-stu-id="dd142-165">If you see that most of the CPU time is consumed by the functions that are used, try to find the place in the configuration that consumes the most resources.</span></span>
- <span data-ttu-id="dd142-166">CPU zamanının çoğunun veri toplama işlevleri tarafından tüketildiğini görürseniz, bunları model eşleme tarafında *SQL gruplama ölçütü* ile değiştirmeyi düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-166">If you see that most of the CPU time is consumed by data collection functions, consider replacing them with *SQL group by* on the model mapping side.</span></span>

### <a name="collecting-data"></a><a name="collecting-data"></a><span data-ttu-id="dd142-167">Veri toplama</span><span class="sxs-lookup"><span data-stu-id="dd142-167">Collecting data</span></span>

<span data-ttu-id="dd142-168">Ortamınıza bağlı olarak, kullanılabilir verileri toplamanın birkaç yolu vardır:</span><span class="sxs-lookup"><span data-stu-id="dd142-168">Depending on your environment, there are several ways to collect available data:</span></span>

- <span data-ttu-id="dd142-169">Toplam çalışma zamanını alın:</span><span class="sxs-lookup"><span data-stu-id="dd142-169">Get the total running time:</span></span>

    - <span data-ttu-id="dd142-170">Eylem merkezinden</span><span class="sxs-lookup"><span data-stu-id="dd142-170">From the Action center</span></span>
    - <span data-ttu-id="dd142-171">Olay günlüğünden</span><span class="sxs-lookup"><span data-stu-id="dd142-171">From the event log</span></span>

- <span data-ttu-id="dd142-172">Yürütme profilini çıkarın:</span><span class="sxs-lookup"><span data-stu-id="dd142-172">Profile the execution:</span></span>

    - <span data-ttu-id="dd142-173">ER araçlarını kullanarak</span><span class="sxs-lookup"><span data-stu-id="dd142-173">By using ER tools</span></span>
    - <span data-ttu-id="dd142-174">Izleme ayrıştırıcısı kullanarak</span><span class="sxs-lookup"><span data-stu-id="dd142-174">By using Trace parser</span></span>
    - <span data-ttu-id="dd142-175">PerfView kullanarak</span><span class="sxs-lookup"><span data-stu-id="dd142-175">By using PerfView</span></span>

#### <a name="collecting-data-in-a-production-environment"></a><span data-ttu-id="dd142-176">Üretim ortamında verileri toplama</span><span class="sxs-lookup"><span data-stu-id="dd142-176">Collecting data in a production environment</span></span>

<span data-ttu-id="dd142-177">Bazen, sorunlar yalnızca üretim ortamında yeniden oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-177">Sometimes, issues can be reproduced only in a production environment.</span></span> <span data-ttu-id="dd142-178">Veriler aşağıdaki yollarla toplanabilir:</span><span class="sxs-lookup"><span data-stu-id="dd142-178">Data can be collected in the following ways:</span></span>

- <span data-ttu-id="dd142-179">[İzleme ayrıştırıcı](../perf-test/trace-trace-tutorial.md) izlemeleri kullanarak</span><span class="sxs-lookup"><span data-stu-id="dd142-179">By using [Trace parser](../perf-test/trace-trace-tutorial.md) traces</span></span>
- <span data-ttu-id="dd142-180">[ER yürütme](trace-execution-er-troubleshoot-perf.md) izlemelerini kullanarak</span><span class="sxs-lookup"><span data-stu-id="dd142-180">By using [ER execution](trace-execution-er-troubleshoot-perf.md) traces</span></span>
- <span data-ttu-id="dd142-181">Toplam yürütme süresini kullanarak</span><span class="sxs-lookup"><span data-stu-id="dd142-181">By using the total execution time</span></span>

#### <a name="collecting-data-in-a-development-environment"></a><span data-ttu-id="dd142-182">Geliştirme ortamında verileri toplama</span><span class="sxs-lookup"><span data-stu-id="dd142-182">Collecting data in a development environment</span></span>

<span data-ttu-id="dd142-183">Üretim ortamında kullanılabilen araçlara ek olarak, geliştirme ortamında kullanabileceğiniz çeşitli araçlar vardır:</span><span class="sxs-lookup"><span data-stu-id="dd142-183">In addition to the tools that can be used in a production environment, there are several tools that you can use in a development environment:</span></span>

- <span data-ttu-id="dd142-184">Olay günlüğü (Microsoft-Dynamics-ElectronicReporting).</span><span class="sxs-lookup"><span data-stu-id="dd142-184">Event log (Microsoft-Dynamics-ElectronicReporting).</span></span> <span data-ttu-id="dd142-185">Bu günlük, size toplam yürütme süresini verebilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-185">This log can give you the total execution time.</span></span>
- <span data-ttu-id="dd142-186">PerfView gibi yaygın .NET araçları.</span><span class="sxs-lookup"><span data-stu-id="dd142-186">Common .NET tools, such as PerfView.</span></span>

<span data-ttu-id="dd142-187">Ek olarak, geliştirme ortamı size daha fazla esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="dd142-187">Additionally, a development environment gives you more flexibility to experiment.</span></span> <span data-ttu-id="dd142-188">Örneğin, yürütme süresinin nasıl etkilendiğini görmek için raporların belirli parçalarını kapatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-188">For example, you can turn off parts of reports to see how the execution time is affected.</span></span>

### <a name="tools"></a><a name="tools"></a><span data-ttu-id="dd142-189">Araçlar</span><span class="sxs-lookup"><span data-stu-id="dd142-189">Tools</span></span>

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a><span data-ttu-id="dd142-190">Eylem merkezindeki yürütme süresi</span><span class="sxs-lookup"><span data-stu-id="dd142-190">Execution time in the Action center</span></span>

<span data-ttu-id="dd142-191">ER, Eylem merkezindeki yapılandırmanın yürütme süresini gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-191">ER can show the execution time of the configuration in the Action center.</span></span> <span data-ttu-id="dd142-192">Bu seçenek yalnızca belirli bir kullanıcı ve belirli bir şirket için ve yalnızca etkileşimli oturumlar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-192">This option works only for a specific user and a specific company, and only for interactive sessions.</span></span> <span data-ttu-id="dd142-193">Bu özelliği kullanılabilir hale getirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="dd142-193">To make this feature available, follow these steps.</span></span>

1. <span data-ttu-id="dd142-194">**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="dd142-194">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="dd142-195">**Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="dd142-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="dd142-196">**Kullanıcı parametreleri** iletişim kutusunda, **Dosya oluşum süresini göster** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="dd142-196">In the **User parameters** dialog box, set the **Show file generation time** option to **Yes**.</span></span>

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a><span data-ttu-id="dd142-197">Olay günlüğündeki yürütme süresi</span><span class="sxs-lookup"><span data-stu-id="dd142-197">Execution time in the event log</span></span>

1. <span data-ttu-id="dd142-198">Windows Olay Görüntüleyici'yi açın.</span><span class="sxs-lookup"><span data-stu-id="dd142-198">Open Windows Event Viewer.</span></span>
2. <span data-ttu-id="dd142-199">**Uygulamalar ve Hizmetler günlükleri** altında, **Microsoft-Dynamics-ElectronicReporting/Operational**'ı açın.</span><span class="sxs-lookup"><span data-stu-id="dd142-199">Under **Applications and Services logs**, open **Microsoft-Dynamics-ElectronicReporting/Operational**.</span></span>
3. <span data-ttu-id="dd142-200">Bu olaylar, geçen süre bilgilerini içerdiğinden, **EventID = 2** olan **FormatMapingrun** olaylarını arayın.</span><span class="sxs-lookup"><span data-stu-id="dd142-200">Look for **FormatMapingRun** events where **EventID=2**, because these events contain the information about elapsed time.</span></span>

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a><span data-ttu-id="dd142-201">İzleme ayrıştırıcı izlemeleri</span><span class="sxs-lookup"><span data-stu-id="dd142-201">Trace parser traces</span></span> 

<span data-ttu-id="dd142-202">ER, X++ içinde uygulandığından, performansı analiz etmek için yaygın X++ araçlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-202">Because ER is implemented in X++, you can use common X++ tools to analyze performance.</span></span> <span data-ttu-id="dd142-203">Daha fazla bilgi için bkz. [İzleme ayrıştırıcısı kullanarak izlemeleri alma](../perf-test/trace-trace-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="dd142-203">For more information, see [Take traces by using Trace parser](../perf-test/trace-trace-tutorial.md).</span></span>

<span data-ttu-id="dd142-204">Bu yaklaşımın birkaç sınırlaması bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dd142-204">There are a few limitations to this approach.</span></span> <span data-ttu-id="dd142-205">ER'nin bir parçası C#'ta uygulandığından, ayrıntıların tümü kullanılabilir olmayacak.</span><span class="sxs-lookup"><span data-stu-id="dd142-205">Because part of ER is implemented in C#, not all the details will be available.</span></span> <span data-ttu-id="dd142-206">Ancak, veri kullanım ayrıntılarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-206">However, you can view the data usage details.</span></span> <span data-ttu-id="dd142-207">Ek olarak, uzun rapor çalışmaları izleme depolama sınırlamalarını aşabilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-207">Additionally, long report runs can exceed trace storage limitations.</span></span>

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a><span data-ttu-id="dd142-208">ER izleri</span><span class="sxs-lookup"><span data-stu-id="dd142-208">ER traces</span></span>

<span data-ttu-id="dd142-209">ER, kendi izlemelerini toplayabilir ve bu izlemeler için görselleştirme ve analiz araçlarına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="dd142-209">ER can collect its own traces, and it has visualization and analysis tools for those traces.</span></span> <span data-ttu-id="dd142-210">Daha fazla bilgi için, bkz. [Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="dd142-210">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

#### <a name="perfview"></a><a name="perfview"></a><span data-ttu-id="dd142-211">PerfView</span><span class="sxs-lookup"><span data-stu-id="dd142-211">PerfView</span></span>

<span data-ttu-id="dd142-212">Hem X++ hem de .NET platformunun üzerine uygulandığı için, yaygın .NET araçlarını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-212">Because both X++ and ER are implemented on top of the .NET platform, you can use common .NET tools.</span></span> <span data-ttu-id="dd142-213">Örneğin, ücretsiz [PerfView](https://github.com/Microsoft/perfview) aracını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-213">For example, you can use the free [PerfView](https://github.com/Microsoft/perfview) tool.</span></span>

<span data-ttu-id="dd142-214">Ayrıca, komut satırından da veri toplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-214">You can also collect data from the command line.</span></span> <span data-ttu-id="dd142-215">Örneğin, aşağıdaki Windows PowerShell betiği, makinede herhangi bir biçim yürütmesi durduruluncaya kadar yürütme süresini toplar.</span><span class="sxs-lookup"><span data-stu-id="dd142-215">For example, the following Windows PowerShell script collects the execution time until any format execution is stopped on the machine.</span></span>

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

<span data-ttu-id="dd142-216">Bu yaklaşımın birkaç sınırlaması bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dd142-216">There are a few limitations to this approach.</span></span> <span data-ttu-id="dd142-217">Makineye yönetici erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dd142-217">You must have administrative access to the machine.</span></span> <span data-ttu-id="dd142-218">Ek olarak, büyük bir öğrenme eğrisi bulunduğundan deneyimli bir geliştirici olmalısınız.</span><span class="sxs-lookup"><span data-stu-id="dd142-218">Additionally, you must be an experienced developer, because there is a steep learning curve.</span></span>

### <a name="making-changes"></a><a name="making-changes"></a><span data-ttu-id="dd142-219">Değişiklik yapma</span><span class="sxs-lookup"><span data-stu-id="dd142-219">Making changes</span></span>

#### <a name="use-caching"></a><a name="use-caching"></a><span data-ttu-id="dd142-220">Önbelleğe almayı kullanma</span><span class="sxs-lookup"><span data-stu-id="dd142-220">Use caching</span></span>

<span data-ttu-id="dd142-221">Önbelleğe alma, veriyi tekrar getirmek için gereken süreyi azaltıyor olsa da bellekten harcar.</span><span class="sxs-lookup"><span data-stu-id="dd142-221">Although caching reduces the amount of time that is required to fetch data again, it costs memory.</span></span> <span data-ttu-id="dd142-222">Alınan veri miktarının çok büyük olmadığı durumlarda önbelleğe almayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="dd142-222">Use caching in cases where the amount of fetched data isn't very large.</span></span> <span data-ttu-id="dd142-223">Önbelleğe almayı nasıl kullanacağınıza dair daha fazla bilgi ve bir örnek için bkz. [Yürütme izlemesinin bilgilerine dayalı olarak model eşlemeyi geliştirme](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span><span class="sxs-lookup"><span data-stu-id="dd142-223">For more information and an example that shows how to use caching, see [Improve the model mapping based on information from the execution trace](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).</span></span>

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a><span data-ttu-id="dd142-224">Önbelleğe alınmış, parametreli hesaplanan alan kullanma</span><span class="sxs-lookup"><span data-stu-id="dd142-224">Use a cached, parameterized calculated field</span></span>

<span data-ttu-id="dd142-225">Bazı durumlarda, değerlerin tekrar aranması gerekir.</span><span class="sxs-lookup"><span data-stu-id="dd142-225">Sometimes, values must be looked up repeatedly.</span></span> <span data-ttu-id="dd142-226">Örnek arasında hesap adları ve hesap numaraları sayılabilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-226">Examples include account names and account numbers.</span></span> <span data-ttu-id="dd142-227">Zamandan tasarruf etmek için en üst düzeyde parametreleri olan bir hesaplanmış alan oluşturabilir ve bu alanı önbelleğe ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dd142-227">To help save time, you can create a calculated field that has parameters on the top level, and then add the field to the cache.</span></span>

<span data-ttu-id="dd142-228">Bu yaklaşımı yalnızca, önbelleğe alınan verilerin boyutu küçükse kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="dd142-228">We recommend that you use this approach only when the size of the cached data is small.</span></span> <span data-ttu-id="dd142-229">Daha fazla bilgi için bkz. [Parametreli CALCULATED FIELD veri kaynakları ekleyerek ER çözümlerinin performansını iyileştirme](er-calculated-field-ds-performance.md).</span><span class="sxs-lookup"><span data-stu-id="dd142-229">For more information, see [Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources](er-calculated-field-ds-performance.md).</span></span>

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a><span data-ttu-id="dd142-230">JOIN veri kaynağı kullanma</span><span class="sxs-lookup"><span data-stu-id="dd142-230">Use a JOIN data source</span></span>

<span data-ttu-id="dd142-231">**JOIN** veri kaynağı, birkaç bağlantılı kaydın tek bir sorgu ile alınmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="dd142-231">A **JOIN** data source enables several connected records to be fetched by one query.</span></span> <span data-ttu-id="dd142-232">Her bağlı kaydı getirmek için ayrı bir sorgu kullanılması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="dd142-232">A separate query doesn't have to be used to fetch each connected record.</span></span> <span data-ttu-id="dd142-233">Örneğin, 1.000 satırınız varsa ve her satır ilişkisine göre madde verileri alıyorsanız, 1.001 sorguya sahip olursunuz (= 1.000 + 1).</span><span class="sxs-lookup"><span data-stu-id="dd142-233">For example, if you have 1,000 lines, and you fetch item data for each line by relation, you will have 1,001 queries (= 1,000 + 1).</span></span> <span data-ttu-id="dd142-234">**JOIN** veri kaynağı kullanırsanız, aynı verileri getirmek için yalnızca bir sorgu kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="dd142-234">If you use a **JOIN** data source, you will use only one query to fetch the same data.</span></span> <span data-ttu-id="dd142-235">Daha fazla bilgi için bkz. [ER model eşlemelerinde birden çok uygulama tablosundan veri almak için JOIN veri kaynaklarını kullanma](er-join-data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="dd142-235">For more information, see [Use JOIN data sources in ER model mappings to get data from multiple application tables](er-join-data-sources.md).</span></span>

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a><span data-ttu-id="dd142-236">WHERE işlevi yerine FILTER fonksiyonunu kullanma</span><span class="sxs-lookup"><span data-stu-id="dd142-236">Use the FILTER function instead of the WHERE function</span></span>

<span data-ttu-id="dd142-237">**[FILTER](er-functions-list-filter.md)** işlevi, koşulları SQL Server'da çalıştırırken **WHERE** işlevi listedeki tüm verileri getirir (bir seferde bir kayıt) ve her kayıt için koşulu uygular.</span><span class="sxs-lookup"><span data-stu-id="dd142-237">The **[FILTER](er-functions-list-filter.md)** function runs conditions on SQL Server, whereas the **WHERE** function fetches all data from the list, one record at a time, and applies the condition for each record.</span></span> <span data-ttu-id="dd142-238">Örneğin, 1.000 kayıttan bir kayıt seçmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="dd142-238">For example, you want to select one record out of 1,000 records.</span></span> <span data-ttu-id="dd142-239">**WHERE** işlevini kullanırsanız, 1.000 kayıdın tümü getirilecektir.</span><span class="sxs-lookup"><span data-stu-id="dd142-239">If you use **WHERE**, all 1,000 records will be fetched.</span></span> <span data-ttu-id="dd142-240">Ancak, **FILTER** işlevini kullanırsanız, yalnızca bir kayıt getirilecektir.</span><span class="sxs-lookup"><span data-stu-id="dd142-240">However, if you use **FILTER**, exactly one record will be fetched.</span></span> <span data-ttu-id="dd142-241">**FILTER** aynı zamanda veritabanı tarafındaki dizinleri de kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="dd142-241">**FILTER** can also use indexes on the database side.</span></span>

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a><span data-ttu-id="dd142-242">Toplanan veri işlevlerini veya birikmiş veri veri kaynağını kullanma</span><span class="sxs-lookup"><span data-stu-id="dd142-242">Using collected data functions or an accumulated data data source</span></span>

<span data-ttu-id="dd142-243">Yapılandırmanız, rapora göre daha önce getirilen verileri özetleyen bir *gruplama ölçütüne* sahipse, bileşen tüm verileri yeniden alır.</span><span class="sxs-lookup"><span data-stu-id="dd142-243">If your configuration has a *group by* component that summarizes previously fetched data by report, the component will fetch all the data again.</span></span> <span data-ttu-id="dd142-244">Toplanan veri işlevlerini kullanarak, ER'nin ilk getirme sırasında veri birikmesine olanak tanırsınız.</span><span class="sxs-lookup"><span data-stu-id="dd142-244">By using collected data functions, you enable ER to accumulate data during the first fetch.</span></span> <span data-ttu-id="dd142-245">Daha fazla bilgi için bkz. [Sayım ve toplama işlemlerini yapmak için ER Yapılandırma biçimi](tasks/er-format-counting-summing-2.md).</span><span class="sxs-lookup"><span data-stu-id="dd142-245">For more information, see [ER Configure format to do counting and summing](tasks/er-format-counting-summing-2.md).</span></span>

#### <a name="rewrite-parts-of-the-configuration-in-x"></a><span data-ttu-id="dd142-246">Yapılandırmanın parçalarını X++ ile yeniden yazın</span><span class="sxs-lookup"><span data-stu-id="dd142-246">Rewrite parts of the configuration in X++</span></span>

<span data-ttu-id="dd142-247">ER, uzantılar da dahil olmak üzere tablo ve sınıfların arama yöntemlerini destekler.</span><span class="sxs-lookup"><span data-stu-id="dd142-247">ER supports calling methods of tables and classes, including extensions.</span></span> <span data-ttu-id="dd142-248">Performansı artırmaya yardımcı olmak için, X++ ile model eşleme parçalarını yeniden yazmayı düşünün.</span><span class="sxs-lookup"><span data-stu-id="dd142-248">Consider rewriting parts of the model mapping in X++ to help improve performance.</span></span>

<span data-ttu-id="dd142-249">ER, aşağıdaki kaynaklardaki verileri kullanabilir:</span><span class="sxs-lookup"><span data-stu-id="dd142-249">ER can consume data from the following sources:</span></span>

- <span data-ttu-id="dd142-250">Sınıflar ( **nesne** ve **sınıf** veri kaynakları)</span><span class="sxs-lookup"><span data-stu-id="dd142-250">Classes (**object** and **class** data sources)</span></span>
- <span data-ttu-id="dd142-251">Tablolar (**tablo** ve **tablo kayıtları** veri kaynakları)</span><span class="sxs-lookup"><span data-stu-id="dd142-251">Tables (**table** and **table records** data sources)</span></span>

<span data-ttu-id="dd142-252">[ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory), önceden hesaplanmış verileri çağrı kodundan göndermek için de bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="dd142-252">The [ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) also provides a way to send precalculated data from the calling code.</span></span> <span data-ttu-id="dd142-253">Uygulama paketi bu yaklaşım için çok sayıda örnek içerir.</span><span class="sxs-lookup"><span data-stu-id="dd142-253">The application suite contains numerous examples of this approach.</span></span>
