---
title: Talep tahminine genel bakış
description: Talep tahmini, satış siparişlerinden bağımsız talebi ve müşteri siparişlerine ilişkin herhangi bir dekuplaj noktasındaki bağımlı talebi tahmin etmede kullanılır. Geliştirilmiş talep tahmin azaltma kuralları, kitlesel özelleştirme için ideal bir çözüm sunar.
author: roxanadiaconu
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca463d821292a2ad53462a3575f2d5712b9e53cc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004054"
---
# <a name="demand-forecasting-overview"></a>Talep tahminine genel bakış

[!include [banner](../includes/banner.md)]

Talep tahmini, satış siparişlerinden bağımsız talebi ve müşteri siparişlerine ilişkin herhangi bir dekuplaj noktasındaki bağımlı talebi tahmin etmede kullanılır. Geliştirilmiş talep tahmin azaltma kuralları, kitlesel özelleştirme için ideal bir çözüm sunar.

Başlangıç tahmini oluşturmak için, geçmiş hareketlerin özeti Azure üzerinde barındırılan Microsoft Azure Machine Learning'e geçirilir. Bu hizmet kullanıcılar arasında paylaşılmadığı için, sektöre özgü gereklilikleri karşılayacak şekilde kolayca uyarlanabilir. Tahmini görselleştirmek, tahmini ayarlamak ve tahminin doğruluğu hakkındaki ana performans göstergelerini (KPI'ler) görüntülemek için Supply Chain Management'ı kullanabilirsiniz.

## <a name="key-features-of-demand-forecasting"></a>Talep tahmininin ana özellikleri
Talep tahmininin ana özelliklerden bazıları aşağıda verilmiştir:

-   Geçmiş verilere dayalı bir istatistik temel tahmin oluşturur.
-   Dinamik bir tahmin boyutları kümesi kullanır.
-   Talep eğilimlerini, güven aralıklarını ve tahmin ayarlamalarını görselleştirir.
-   Planlama süreçlerinde kullanılacak ayarlanmış tahmini yetkilendirir.
-   Aykırı değerleri kaldırır.
-   Tahmin doğruluğu ölçümleri oluşturur.

## <a name="major-themes-in-demand-forecasting"></a>Talep tahmininin önemli konuları
Talep tahmininde üç önemli konu gerçekleştirilir:

-   **Modülarite** – Talep tahmini modülerdir ve kolay yapılandırılır. İşlevselliği **Ticaret** &gt; **Stok tahmini** &gt; **Talep tahmini** içindeki yapılandırma anahtarını değiştirerek açıp kapayabilirsiniz.
-   **Microsoft yığının yeniden kullanılması** – Microsoft, Şubat 2015'te makine öğrenme platformu başlattı. Şimdi Microsoft Cortana Analytics Suite'in bir parçası haline gelen Makine Öğrenimi, talep tahmin deneyleri gibi tahmine dayalı analiz deneylerini R veya Python gibi programlama dilleri algoritmaları kullanarak ve basit bir sürükle bırak arabirimi ile hızlı ve kolay oluşturmanızı sağlar.
    -   Talep tahmini deneylerini indirebilir, iş gereksinimlerinizi karşılayacak şekilde değiştirebilir, Azure üzerinde web hizmeti olarak yayınlayabilir ve talep tahminleri oluşturmak için kullanabilirsiniz. Kuruluş düzeyinde kullanıcı olarak bir üretim planlayıcı için Supply Chain Management aboneliği aldıysanız, deneyler indirilmeye hazırdır.
    -   Şu anda mevcut olan talep tahmin deneylerinden birini [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirebilirsiniz. Talep tahmini deneyleri, Supply Chain Management ile otomatik olarak bütünleşirken, müşteriler ve ortaklar [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirdikleri deneylerin entegrasyonunu kendileri yapmalıdır. Bu yüzden, [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirilen deneylerin kullanımı, Finance and Operations Talep tahmini deneyleri kadar basit değildir. Deneylerin kodunu, Finance and Operations uygulama programlama arabiriminin (API) kullanılabilmesi için modifiye etmeniz gerekir.
    -   Microsoft Azure Machine Learning Studio'da (klasik) kendi deneylerinizi oluşturabilir, bunları Azure üzerinde hizmetler olarak yayınlayabilir ve talep tahminleri oluşturmak için kullanabilirsiniz.
    -   Yüksek performans gerekmiyorsa veya büyük miktarda verinin işlenmesi gerekmiyorsa, Machine Learning serbest katmanını kullanabilirsiniz. Özellikle uygulama ve test aşamalarında daima bu katmandan başlamanızı tavsiye ederiz. Daha yüksek performansa ve ek depolamaya ihtiyacınız varsa, Machine Learning standart katmanını kullanabilirsiniz. Bu katman, Azure aboneliği gerektirir ve ek ücretler içerir. Bu konudaki ayrıntılar için bkz. [Machine Learning Studio fiyatlandırması](https://aka.ms/machine-learning-price-info).
-   **Herhangi bir dekuplaj noktasında tahmin azaltma** – Talep tahmini, size herhangi bir dekuplaj noktasında hem bağımlı hem de bağımsız talepleri tahmin etme olanağı veren bu işlev üzerine kurulur.

## <a name="basic-flow-in-demand-forecasting"></a>Talep tahminindeki temel akış
Aşağıdaki şemada talep tahminindeki temel akış gösterilmiştir. 

[![talep tahminine giriş şeması](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Talep tahmini oluşturma, Supply Chain Management'ta başlar. Supply Chain Management hareket veritabanından alınan geçmiş hareket verileri bir araya getirilir ve bir aşamalandırma tablosu doldurulur. Bu hazırlama tablosu, daha sonra Makine Öğrenimi hizmetine beslenir. En az düzeyde özelleştirme gerçekleştirerek, önceki veri kaynaklarını hazırlama tablosuna takabilirsiniz. Veri kaynakları Microsoft Excel dosyaları, virgülle ayrılmış değerler (CSV) dosyaları ve Microsoft Dynamics AX 2009 ve Microsoft Dynamics AX 2012'den veriler içerebilir. Bu nedenle, birden fazla sisteme yayılmış geçmişe verileri dikkate alan talep tahminleri oluşturabilirsiniz. Ancak, öğe adları ve ölçü birimleri gibi ana veriler çeşitli veri kaynaklarında aynı olmalıdır.

Talep tahmini Machine Learning deneylerini kullanırsanız bu deneyler, bir başlangıç tahmini hesaplamak için beş zaman serisi tahmin yöntemi arasından en uygununu arar. Bu tahmin yöntemlerine ilişkin parametreler Supply Chain Management'ta yönetilir. 

Tahminler, geçmiş veriler ve önceki yinelemelerdeki talep tahminlerinde yapılan tüm değişiklikler artık Supply Chain Management'ta da kullanılabilir. 

Başlangıç tahminlerini görselleştirmek ve değiştirmek için Supply Chain Management'ı kullanabilirsiniz. Tahminler planlama için kullanılmadan önce manüel ayarlamalar yetkilendirilmelidir.

## <a name="limitations"></a>Sınırlamalar
Talep tahmini, üretim sektöründeki müşterilere tahmin süreçleri oluşturmada yardımcı olan bir araçtır. Bir talep tahmini çözümünün temel işlevini sunar ve kolayca genişletilebilmek üzere tasarlanmıştır. Talep tahmini, ticaret, toptan satış, ambarlama, nakliye ve diğer profesyonel hizmetler gibi sektörlerde bulunan müşteriler için en iyi tercih olmayabilir.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Talep tahmini kurulumu](demand-forecasting-setup.md)

[İstatistik temel tahmini oluşturma](generate-statistical-baseline-forecast.md)

[Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)

[Düzeltilen tahmini yetkilendirme](authorize-adjusted-forecast.md)

[Tahmin doğruluğunu izleme](monitor-forecast-accuracy.md)

[Bir talep tahmini hesaplarken aykırı değerleri geçmiş hareket verilerinden kaldırma](remove-historical-outliers-calculating-demand-forecast.md)

[Talep tahmini işlevini genişletme](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



