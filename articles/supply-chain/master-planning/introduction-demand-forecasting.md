---
title: Talep tahminine genel bakış
description: Talep tahmini, satış siparişlerinden bağımsız talebi ve müşteri siparişlerine ilişkin herhangi bir dekuplaj noktasındaki bağımlı talebi tahmin etmede kullanılır. Geliştirilmiş talep tahmin azaltma kuralları, kitlesel özelleştirme için ideal bir çözüm sunar.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: a645ee6f7e6085abc6e872d490b078f512c15aa1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "310013"
---
# <a name="demand-forecasting-overview"></a>Talep tahminine genel bakış

[!include [banner](../includes/banner.md)]

Talep tahmini, satış siparişlerinden bağımsız talebi ve müşteri siparişlerine ilişkin herhangi bir dekuplaj noktasındaki bağımlı talebi tahmin etmede kullanılır. Geliştirilmiş talep tahmin azaltma kuralları, kitlesel özelleştirme için ideal bir çözüm sunar.

Başlangıç tahmini oluşturmak için, geçmiş hareketlerin özeti Azure üzerinde barındırılan Microsoft Azure Machine Learning hizmetine geçirilir. Bu hizmet kullanıcılar arasında paylaşılmadığı için, sektöre özgü gereklilikleri karşılayacak şekilde kolayca uyarlanabilir. Tahmini görselleştirmek, tahmini ayarlamak ve tahminin doğruluğu hakkında ana performans göstergelerini (KPI'ler) görüntülemek için Finance and Operations'ta kullanabilirsiniz.

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
    -   Finance and Operations Talep tahmin deneylerini indirebilir, bunları iş gerekliliklerinizi karşılayacak şekilde değiştirebilir, Azure üzerinde web hizmeti olarak yayınlayabilir ve talep tahminleri oluşturmak için kullanabilirsiniz. Kuruluş düzeyinde kullanıcı olarak bir üretim planlayıcı için Finance and Operations aboneliği aldıysanız, deneyler indirilmeye hazırdır.
    -   Şu anda mevcut olan talep tahmin deneylerinden birini [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirebilirsiniz. Finance and Operations Talep tahmini deneyleri Finance and Operations ile otomatik olarak bütünleşirken, müşteriler ve ortaklar [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirdikleri deneylerin entegrasyonunu kendileri yapmalıdır. Bu yüzden, [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirilen deneylerin kullanımı, Finance and Operations Talep tahmini deneyleri kadar basit değildir. Deneylerin kodunu, Finance and Operations uygulama programlama arabiriminin (API) kullanılabilmesi için modifiye etmeniz gerekir.
    -   Microsoft Azure Machine Learning Studio'da kendi deneylerinizi oluşturabilir, bunları Azure üzerinde hizmetler olarak yayınlayabilir ve talep tahminleri oluşturmak için kullanabilirsiniz.
    -   Yüksek performans gerekmiyorsa veya büyük miktarda verinin işlenmesi gerekmiyorsa, Machine Learning serbest katmanını kullanabilirsiniz. Özellikle uygulama ve test aşamalarında daima bu katmandan başlamanızı tavsiye ederiz. Daha yüksek performansa ve ek depolamaya ihtiyacınız varsa, Machine Learning standart katmanını kullanabilirsiniz. Bu katman, Azure aboneliği gerektirir ve ek ücretler içerir. Machine Learning fiyatlandırmasıyla ilgili ayrıntılı bilgi için bkz. <http://aka.ms/machine-learning-price-info>.
-   **Herhangi bir dekuplaj noktasında tahmin azaltma** – Finance and Operations'daki talep tahmini, size herhangi bir dekuplaj noktasında hem bağımlı hem de bağımsız talepleri tahmin etme olanağı veren bu işlev üzerine kurulur.

## <a name="basic-flow-in-demand-forecasting"></a>Talep tahminindeki temel akış
Aşağıdaki şemada talep tahminindeki temel akış gösterilmiştir. 

[![talep tahminine giriş şeması](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Talep tahmin oluşturması Finance and Operations içerisinde başlar. Finance and Operations hareket veritabanından alınan geçmiş hareket verileri bir araya getirilir ve bir aşamalandırma tablosu doldurulur. Bu hazırlama tablosu, daha sonra Makine Öğrenimi hizmetine beslenir. En az düzeyde özelleştirme gerçekleştirerek, önceki veri kaynaklarını hazırlama tablosuna takabilirsiniz. Veri kaynakları Microsoft Excel dosyaları, virgülle ayrılmış değerler (CSV) dosyaları ve Microsoft Dynamics AX 2009 ve Microsoft Dynamics AX 2012'den veriler içerebilir. Bu nedenle, birden fazla sisteme yayılmış geçmişe verileri dikkate alan talep tahminleri oluşturabilirsiniz. Ancak, öğe adları ve ölçü birimleri gibi ana veriler çeşitli veri kaynaklarında aynı olmalıdır.

Finance and Operations Talep tahmini Machine Learning deneylerini kullanırsanız, bir başlangıç tahmini hesaplamak için beş zaman serisi tahmin yöntemi arasından en uygununu arar. Bu tahmin yöntemlerine ilişkin parametreler Finance and Operations'ta yönetilir. 

Tahminler, geçmiş veriler ve önceki yinelemelerdeki talep tahminlerinde yapılan tüm değişiklikler artık Finance and Operations'te de kullanılabilir. 

Finance and Operations'ı başlangıç tahminlerini görselleştirmek ve modifiye etmek için kullanabilirsiniz. Tahminler planlama için kullanılmadan önce manüel ayarlamalar yetkilendirilmelidir.

## <a name="limitations"></a>Sınırlamalar
Finance and Operations'taki talep tahmini, üretim sektöründeki müşterilere tahmin süreçleri oluşturmada yardımcı olan bir araçtır. Bir talep tahmini çözümünün temel işlevini sunar ve kolayca genişletilebilmek üzere tasarlanmıştır. Talep tahmini, perakende, toptan satış, ambarlama, nakliye ve diğer profesyonel hizmetler gibi sektörlerde bulunan müşteriler için en iyi tercih olmayabilir.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Talep tahmini kurulumu](demand-forecasting-setup.md)

[İstatistik temel tahmin oluşturma](generate-statistical-baseline-forecast.md)

[Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)

[Ayarlanmış tahmini yetkilendirme](authorize-adjusted-forecast.md)

[Tahmin doğruluğunu izleme](monitor-forecast-accuracy.md)

[Bir talep tahmin hesaplarken, geçmiş işlem verilerinden aykırı değerleri kaldırın.](remove-historical-outliers-calculating-demand-forecast.md)

[Talep tahmini işlevini genişletme](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



