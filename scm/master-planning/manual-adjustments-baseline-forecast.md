---
title: "Temel tahminde manüel ayarlamalar yapma"
description: "Bu makalede bir temel tahminde manüel ayarlamalar yapma ve tahminin ayrıntılarını görüntüleme yolları açıklanmıştır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 24caafcd01875f04cf3ae5299aadcf9b38ac0e15
ms.lasthandoff: 03/31/2017


---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Temel tahminde manüel ayarlamalar yapma

[!include[banner](../includes/banner.md)]


Bu makalede bir temel tahminde manüel ayarlamalar yapma ve tahminin ayrıntılarını görüntüleme yolları açıklanmıştır. 

Manüel ayarlamalar yapmadan önce, çeşitli sayfalarda bulunan birkaç kavramı anlamanız önemlidir.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Ayarlanan talep tahmini sayfası kılavuzu
**Ayarlanmış talep tahmini** sayfası aşağıdaki yapıya sahip bir kılavuz içerir:

-   İlk sütunda tahminin oluşturulma amacı olan maddeler, madde tahsisat anahtarları, şirketler vb. gösterilir. Sayfanın alt başlığı kılavuzda gösterilen geçerli tahmin boyutları için bir açıklama sağlar. Örneğin, sayfanın alt başlığı **Şirket / Tesis / Madde tahsisat anahtarı** ve kılavuzdaki satır başlıklarından biri **USMF / 1 / D\_Alloc** ise, bu satır USMF şirketi, 1. tesis ve **D\_Alloc** madde tahsisat anahtarına ilişkin tahmini gösterir.
-   Sonraki sütunlar tahminin oluşturulma amacı olan tahmin aralıklarını temsil eder. Her sütun başlığı sütunun gösterdiği tahmin aralığının ilk tarihidir.
-   Hücrelerdeki değerler, o özel tahmin aralığında bir maddeyi, madde tahsisat anahtarını, vb. temsil eder.

## <a name="forecast-aggregation-and-deaggregation"></a>Tahmin toplama ve toplamayı kaldırma
Sayfanın alt başlığı tahmin toplama düzeyini gösterir. 

Örneğin, sayfanın alt başlığı **Şirket / Tesis / Tahsisat anahtarı / Madde numarası / Renk / Boyut / Yapılandırma / Stil** ise, hiç tahmin toplama yoktur ve tahmin madde ve boyutları düzeyinde gösterilir. Toplamı değiştirmek için, uygulama menüsünden açabileceğiniz** Tahmin boyutlarını değiştir** sayfasını kullanabilirsiniz. 

Tahmini değiştirmek için, kullanılabilen hücrelerden birine tıklayın ve ayarlanmış tahmin değeri yazın. Düzenlenen hücre, gösterilen tahminin talep tahmini hizmetinin oluşturduğu tahmin olmadığını, ancak manüel olarak ayarlandığını gösterecek şekilde kalınlaşır. 

Sayfanın daha toplanmış veriler göstermesini sağlamak için toplamı değiştirirseniz, toplanmış tahmini oluşturan ayrı ayrı tahmin satırlarını görmek üzere , **Talep tahmin satırları** sayfasını kullanabilirsiniz. 

Örneğin, tahmini madde düzeyinde oluşturdunuz, ancak bu maddeye talebin bir promosyon veya başka benzer bir etkinlik nedeniyle tüm tesiste artacağını biliyorsunuz. Bu durumda, toplamı **Tahmin boyutlarını değiştir** sayfasındaki **Şirket / Madde tahsisat anahtarı / Madde** seçeneğine ayarlayabilirsiniz. Tüm tesislerde maddeye ilişkin global tahmini **Ayarlanmış talep tahmini** kılavuzunda ayarlayabilirsiniz. Tüm tesisler arasında yaptığınız değişikliğin etkisini görmek için, **Talep tahmin satırları** sayfasını açın. Bu sayfada, her tesise ait madde, ayarlanan tahmin miktarı ve orijinal tahmin miktarı için bir satır görürsünüz. 

Tahmin edilen miktar ayarlaması toplanmış bir düzeyde yapıldığında, sistem değişikliği toplamı oluşturan satırlar arasında dağıtmak için ağırlıklı tahsisatı kullanır. 

Ayrıca manüel ayarlamaları **Talep tahmin satırları** sayfasında, toplamı kaldırma kılavuzundaki **Toplam miktar** değerini veya **Miktar** hücrelerini değiştirerek de yapabilirsiniz.

## <a name="viewing-details-of-the-forecast"></a>Tahminin ayrıntılarını görüntüleme
Tahmin hakkında daha fazla bilgi görüntülemek için** Talep tahmini ayrıntıları** sayfasını açabilirsiniz. 

**Talep tahmini ayrıntıları** sayfası aşağıdaki bilgileri grafik ve tablo biçimlerinde gösterir:

-   Tahmin öngörülerinin temel alındığı geçmiş talep.
-   Master planlama tarafından kullanılan geçerli tahmin.
-   Yeni talep tahmin değerleri ve bu değerlerin manüel olarak ayarlandığı tutarlar.
-   Tahmin edilen değerler için güven aralığı.
-   Tahmin oluşturmak için kullanılan tahmin modeli. Toplanan verileri görüntülüyorsanız, toplanan saat dizisi için kullanılan tüm yöntemlerin listesini görürsünüz.
-   Dahili model doğruluğu (MAPE). Tahmin doğruluğu hakkında daha fazla bilgi için, bkz. [Tahmin doğruluğunu izleme](monitor-forecast-accuracy.md).

**Notlar:**

-   Sayfanın **tahmin** bölümünde görülen güven aralığı, güven aralığı üst sınırı ile güven aralığı alt sınırı arasındaki farkı temsil eder. Üst ve alt sınırların değerlerini görmek için, **Grafiksel olarak geçmiş talep ve tahmin** bölümündeki grafikte gezinin.
-   Dynamics 365 for Operations Talep tahmini Microsoft Azure Machine Learning hizmetini kullanırsanız, oluşturulan tahminde olması gereken güven düzeyi yüzdesini belirtebilirsiniz. Güven aralığı talep tahmini için iyi tahminler olarak hareket eden bir değerler aralığından oluşur. Yüzde 95'lik bir güven düzeyi yüzdesi, talep tahmininin güven aralığı sınırlarının dışına çıkma konusunda yüzde 5'lik bir risk bulunduğunu gösterir.

Manüel ayarlamaları, **Talep tahmini ayrıntıları** sayfasında, **Tahmin** bölümündeki **Tahmin** satırında belirtilen değerleri değiştirerek de yapabilirsiniz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Tahmin doğruluğunu izleme](monitor-forecast-accuracy.md)

[İstatistik temel tahmin oluşturma](generate-statistical-baseline-forecast.md)




