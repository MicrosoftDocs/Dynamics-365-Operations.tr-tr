---
title: "Talep tahmini genel bakış"
description: "Talep tahmini, satış siparişlerinden bağımsız talebi ve müşteri siparişlerine ilişkin herhangi bir dekuplaj noktasındaki bağımlı talebi tahmin etmede kullanılır. Geliştirilmiş talep azaltma kuralları yığın özelleştirme için ideal bir çözüm sağlamak tahmin."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Talep tahmini genel bakış

Talep tahmini, satış siparişlerinden bağımsız talebi ve müşteri siparişlerine ilişkin herhangi bir dekuplaj noktasındaki bağımlı talebi tahmin etmede kullanılır. Geliştirilmiş talep azaltma kuralları yığın özelleştirme için ideal bir çözüm sağlamak tahmin.

Başlangıç tahmini oluşturmak için, geçmiş hareketlerin özeti Azure üzerinde barındırılan Microsoft Azure Machine Learning hizmetine geçirilir. Bu hizmet kullanıcılar arasında paylaşılmadığı için, sektöre özgü gereklilikleri karşılayacak şekilde kolayca uyarlanabilir. Tahmin görselleştirmek, tahmin ayarlamak ve tahmin doğruluğu hakkında anahtar performans göstergeleri (APG) görüntülemek için Dynamics 365 işlemleri için kullanabilirsiniz.

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

-   **Modülarite** – Talep tahmini modülerdir ve kolay yapılandırılır. İşlevini açma ve kapatma sırasında konfigürasyon anahtarı değiştirerek kapatabilirsiniz **ticaret**&gt;**stok tahmin**&gt;**talep tahmin**.
-   **Microsoft yığının yeniden** – Microsoft Şubat 2015'de makine öğrenme platformu başlattı. Şimdi Microsoft Cortana Analytics paketinin bir parçası olan makine öğrenme algoritmaları R veya Python programlama dilleri ve basit bir Sürükle ve bırak arabirimini kullanarak Öngörü analizi yapılan deneyler, Talep tahmini deneyler gibi hızla ve kolayca oluşturmanızı sağlar.
    -   Dynamics 365 karşıdan yükleme işlemlerini deneyler tahmin talebinin, onları iş gereksinimlerinizi karşılamak, bunları bir web hizmeti Azure ile ilgili olarak yayımlamak ve bunları talep tahminleri oluşturmak için kullanın. Dynamics 365 kuruluş düzeyinde kullanıcı olarak üretim planlayıcısı için işlem aboneliği için satın aldığınız deneyler karşıdan yükleme için kullanılabilir.
    -   Şu anda mevcut olan talep tahmin deneylerinden birini [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirebilirsiniz. Dynamics 365 deneyler tahmini talep işlemleri için otomatik olarak entegre oysa işlemleri için Dynamics 365 ile müşterilerin ve iş ortaklarının tümleştirilmesi ile karşıdan yükleme yapılan deneyler, işlemelidir [Cortana Analytics galeri](https://gallery.cortanaanalytics.com/). Bu nedenle, gelen deneyler [Cortana Analytics galeri](https://gallery.cortanaanalytics.com/) Dynamics 365 işlemleri isteğe bağlı deneyler tahmini için kullanılacak gibi deildir. Böylece işlemleri uygulama programlama arabirimi (API) Dynamics 365 kullandıkları deneyler kodunu değiştirmeniz gerekir.
    -   Microsoft Azure Machine Learning Studio'da kendi deneylerinizi oluşturabilir, bunları Azure üzerinde hizmetler olarak yayınlayabilir ve talep tahminleri oluşturmak için kullanabilirsiniz.
    -   Yüksek performans gerekmiyorsa veya büyük miktarda verinin işlenmesi gerekmiyorsa, Machine Learning serbest katmanını kullanabilirsiniz. Özellikle uygulama ve test aşamalarında daima bu katmandan başlamanızı tavsiye ederiz. Daha yüksek performansa ve ek depolamaya ihtiyacınız varsa, Machine Learning standart katmanını kullanabilirsiniz. Bu katman, Azure aboneliği gerektirir ve ek ücretler içerir. Machine Learning fiyatlandırması hakkında ayrıntılar için, bkz. <http://aka.ms/machine-learning-price-info>.
-   **Tahmin azaltma decoupling herhangi bir noktada** – Dynamics 365 decoupling herhangi bir noktada bağımlı ve bağımsız talep Tahmin etmenizi sağlayan bu işlevsellik işlemleri yapılar için tahmini isteğe bağlı.

## <a name="basic-flow-in-demand-forecasting"></a>Talep tahminindeki temel akış
Aşağıdaki şemada talep tahminindeki temel akış gösterilmiştir. 

[![Talep tahmin giriş diyagramı](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Talep oluşturma işlemleri için Dynamics 365 başlamasını tahmin. Dynamics 365 işlem veritabanı işlemleri için işlem geçmiş verileri toplanır ve hazırlama tablo doldurur. Bu basamak tablo için bir makine öğrenme hizmeti daha sonra beslenir. En az düzeyde özelleştirme gerçekleştirerek, çeşitli veri kaynakları hazırlama tabloya takabilirsiniz. Veri kaynakları Microsoft Excel dosyaları, virgülle ayrılmış değer (CSV) dosyaları ve Microsoft Dynamics AX 2009 ve Microsoft Dynamics AX 2012 veriler içerebilir. Bu nedenle, birden çok sistemleri arasında yayılan geçmiş verilerini dikkate talep tahminleri oluşturabilirsiniz. Ancak, öğe adları ve ölçü birimleri gibi ana veriler çeşitli veri kaynaklarında aynı olmalıdır.

Dynamics 365 makine öğrenme deneyimleri Tahmin işlemlerinin talep için kullanırsanız, bir temel tahmini hesaplamak için beş saat serisi tahmin yöntemleri arasında iyi bir uyum için arayın. Bu tahmin yöntemlerinin parametrelerini Dynamics 365 işlemleri için yönetilir. 

Tahminleri, geçmiş verileri ve talep tahminleri önceki yineleme içinde yapılan değişikliklerin Dynamics 365 işlemleri için kullanılabilir. 

Görselleştirmek ve temel tahminlerini değiştirmek için Dynamics 365 işlemleri için kullanabilirsiniz. Tahminler planlama için kullanılmadan önce manüel ayarlamalar yetkilendirilmelidir.

## <a name="limitations"></a>Sınırlamalar
Dynamics 365 işlemleri için de Talep tahmini üretim sektörünün müşteriler tahmin işlemler oluşturmak yardımcı olan bir araçtır. Bu bir isteğe bağlı çözüm tahmin çekirdek işlevselliğini sunar ve kolayca genişletilebilir şekilde tasarlanmıştır. En iyi Industries gibi perakende müşteriler için toptan sığmama olması ihtimalini tahmin, depolama, taşıma veya diğer Profesyonel hizmetler talep.

<a name="see-also"></a>Ayrıca bkz.
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


