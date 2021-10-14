---
title: Talep tahminine genel bakış
description: Talep tahmini, satış siparişlerinden bağımsız talebi ve müşteri siparişlerine ilişkin herhangi bir dekuplaj noktasındaki bağımlı talebi tahmin etmede kullanılır. Geliştirilmiş talep tahmin azaltma kuralları, kitlesel özelleştirme için ideal bir çözüm sunar.
author: ChristianRytt
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "72004"
- intro-internal
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 980001dda67e96ab3f428ad60cb7951dd5de4d0c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571029"
---
# <a name="demand-forecasting-overview"></a>Talep tahminine genel bakış

[!include [banner](../includes/banner.md)]

Talep tahmini, satış siparişlerinden bağımsız talebi ve müşteri siparişlerine ilişkin herhangi bir dekuplaj noktasındaki bağımlı talebi tahmin etmede kullanılır. Geliştirilmiş talep tahmin azaltma kuralları, kitlesel özelleştirme için ideal bir çözüm sunar.

Başlangıç tahmini oluşturmak için, geçmiş hareketlerin özeti Azure üzerinde barındırılan Microsoft Azure Machine Learning'e geçirilir. Bu hizmet kullanıcılar arasında paylaşılmadığı için, sektöre özgü gereklilikleri karşılayacak şekilde kolayca uyarlanabilir. Tahmini görselleştirmek, tahmini ayarlamak ve tahminin doğruluğu hakkındaki ana performans göstergelerini (KPI'ler) görüntülemek için Supply Chain Management'ı kullanabilirsiniz.

> [!NOTE]
> Microsoft Azure Machine Learning Studio (klasik), makine öğrenimiyle tahmin oluşturma için gereklidir. 1 Aralık 2021 itibarıyla yeni Machine Learning Studio (klasik) kaynakları oluşturamayacaksınız. Ancak mevcut Machine Learning Studio (klasik) kaynaklarınızı 31 Ağustos 2024 tarihine kadar kullanmaya devam edebilirsiniz. Güncelleştirilmiş bilgiler için bkz. [Azure Machine Learning Studio](/azure/machine-learning/overview-what-is-machine-learning-studio#ml-studio-classic-vs-azure-machine-learning-studio).
> 
> Dynamics 365 Supply Chain Management sürüm 10.0.23 ve sonrası, yeni Azure Machine Learning Studio'yu destekler.

## <a name="key-features-of-demand-forecasting"></a>Talep tahmininin ana özellikleri

Talep tahmininin ana özelliklerden bazıları aşağıda verilmiştir:

- Geçmiş verilere dayalı bir istatistik temel tahmin oluşturur.
- Dinamik bir tahmin boyutları kümesi kullanır.
- Talep eğilimlerini, güven aralıklarını ve tahmin ayarlamalarını görselleştirir.
- Planlama süreçlerinde kullanılacak ayarlanmış tahmini yetkilendirir.
- Aykırı değerleri kaldırır.
- Tahmin doğruluğu ölçümleri oluşturur.

## <a name="major-themes-in-demand-forecasting"></a>Talep tahmininin önemli konuları

Talep tahmininde üç önemli konu gerçekleştirilir:

- **Modülarite** – Talep tahmini modülerdir ve kolay yapılandırılır. İşlevselliği **Ticaret** &gt; **Stok tahmini** &gt; **Talep tahmini** içindeki yapılandırma anahtarını değiştirerek açıp kapayabilirsiniz.
- **Microsoft yığınını yeniden kullanma** – Microsoft Cortana Analytics Suite'in bir parçası haline gelen Makine Öğrenimi, talep tahmin deneyleri gibi tahmine dayalı analiz deneylerini R veya Python gibi programlama dilleri algoritmaları kullanarak ve basit bir sürükle bırak arabirimi ile hızlı ve kolay oluşturmanızı sağlar.
  - Talep tahmini deneylerini indirebilir, iş gereksinimlerinizi karşılayacak şekilde değiştirebilir, Azure üzerinde web hizmeti olarak yayınlayabilir ve talep tahminleri oluşturmak için kullanabilirsiniz. Kuruluş düzeyinde kullanıcı olarak bir üretim planlayıcı için Supply Chain Management aboneliği aldıysanız denemeler indirilmeye hazırdır.
  - Şu anda mevcut olan talep tahmin deneylerinden birini [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirebilirsiniz. Talep tahmini deneyleri, Supply Chain Management ile otomatik olarak bütünleşirken, müşteriler ve ortaklar [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirdikleri deneylerin entegrasyonunu kendileri yapmalıdır. Bu yüzden, [Cortana Analytics Gallery](https://gallery.cortanaanalytics.com/)'den indirilen deneylerin kullanımı, Finance and Operations Talep tahmini deneyleri kadar basit değildir. Deneylerin kodunu, Finance and Operations uygulama programlama arabiriminin (API) kullanılabilmesi için modifiye etmeniz gerekir.
  - Microsoft Azure Machine Learning Studio'da (klasik) kendi deneylerinizi oluşturabilir, bunları Azure üzerinde hizmetler olarak yayınlayabilir ve talep tahminleri oluşturmak için kullanabilirsiniz.
  - Yüksek performans gerekmiyorsa veya büyük miktarda verinin işlenmesi gerekmiyorsa, Machine Learning serbest katmanını kullanabilirsiniz. Özellikle uygulama ve test aşamalarında daima bu katmandan başlamanızı tavsiye ederiz. Daha yüksek performansa ve ek depolamaya ihtiyacınız varsa, Machine Learning standart katmanını kullanabilirsiniz. Bu katman, Azure aboneliği gerektirir ve ek ücretler içerir. Bu konudaki ayrıntılar için bkz. [Machine Learning Studio fiyatlandırması](https://aka.ms/machine-learning-price-info).
- **Herhangi bir dekuplaj noktasında tahmin azaltma** – Talep tahmini, size herhangi bir dekuplaj noktasında hem bağımlı hem de bağımsız talepleri tahmin etme olanağı veren bu işlev üzerine kurulur.

## <a name="basic-flow-in-demand-forecasting"></a>Talep tahminindeki temel akış

Aşağıdaki şemada talep tahminindeki temel akış gösterilmiştir.

[![talep tahminine giriş şeması.](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Talep tahmini oluşturma, Supply Chain Management'ta başlar. Supply Chain Management hareket veritabanından alınan geçmiş hareket verileri bir araya getirilir ve bir aşamalandırma tablosu doldurulur. Bu hazırlama tablosu, daha sonra Makine Öğrenimi hizmetine beslenir. En az düzeyde özelleştirme gerçekleştirerek, önceki veri kaynaklarını hazırlama tablosuna takabilirsiniz. Veri kaynakları Microsoft Excel dosyaları, virgülle ayrılmış değerler (CSV) dosyaları ve Microsoft Dynamics AX 2009 ve Microsoft Dynamics AX 2012'den veriler içerebilir. Bu nedenle, birden fazla sisteme yayılmış geçmişe verileri dikkate alan talep tahminleri oluşturabilirsiniz. Ancak, öğe adları ve ölçü birimleri gibi ana veriler çeşitli veri kaynaklarında aynı olmalıdır.

Talep tahmini Machine Learning deneylerini kullanırsanız bu deneyler, bir başlangıç tahmini hesaplamak için beş zaman serisi tahmin yöntemi arasından en uygununu arar. Bu tahmin yöntemlerine ilişkin parametreler Supply Chain Management'ta yönetilir.

Tahminler, geçmiş veriler ve önceki yinelemelerdeki talep tahminlerinde yapılan tüm değişiklikler artık Supply Chain Management'ta da kullanılabilir.

Başlangıç tahminlerini görselleştirmek ve değiştirmek için Supply Chain Management'ı kullanabilirsiniz. Tahminler planlama için kullanılmadan önce manüel ayarlamalar yetkilendirilmelidir.

## <a name="limitations"></a>Sınırlamalar

Talep tahmini, üretim sektöründeki müşterilere tahmin süreçleri oluşturmada yardımcı olan bir araçtır. Bir talep tahmini çözümünün temel işlevini sunar ve kolayca genişletilebilmek üzere tasarlanmıştır. Talep tahmini, ticaret, toptan satış, ambarlama, nakliye ve diğer profesyonel hizmetler gibi sektörlerde bulunan müşteriler için en iyi tercih olmayabilir.

### <a name="demand-forecast-variant-conversion-limitation"></a>Talep tahmini varyant dönüştürme sınırlaması

Stok ölçü birimi talep tahmini ölçü biriminden farklıysa talep tahmini oluşturulurken varyant dönüştürme için ölçü birimi (UOM) tam olarak desteklenmez.

Tahmin oluşturma (**Stok ölçü birimi > Talep tahmini ölçü birimi**) ürün ölçü birimi dönüştürmeyi kullanır. Talep tahmini oluşturma için geçmiş verileri yüklenirken, varyant düzeyinde tanımlanmış dönüştürmeler olsa bile, stok ölçü biriminden talep tahmini ölçü birimine dönüştürme yapılırken her zaman ürün düzeyinde ölçü birimi dönüştürme kullanılacaktır.

Tahmini yetkilendirmenin ilk bölümü (**Talep tahmini ölçü birimi > Stok ölçü birimi**) ürün ölçü birimi dönüşümünü kullanır. Tahmini yetkilendirme işleminin ikinci kısmı (**Stok ölçü birimi > Satış ölçü birimi**), varyant ölçü birimi dönüşümünü kullanır. Oluşturulan talep tahmini yetkilendirildiğinde, talep tahmini ölçü biriminden stok ölçü birimine dönüştürme işlemi, ürün düzeyinde ölçü birimi dönüştürme kullanılarak yapılır. Aynı zamanda, stok birimi ile satış ölçü birimi arasındaki dönüştürme, varyant düzeyinde tanımlanan dönüştürmelere göre yapılır.

Talep tahmini ölçü biriminin belirli anlamı olması gerekmediğini unutmayın. "Talep tahmin birimi" olarak tanımlanabilir. Ürünlerin her biri için, stok ölçü birimiyle dönüşümü 1:1 olacak şekilde tanımlayabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

[Talep tahmini kurulumu](demand-forecasting-setup.md)

[İstatistik temel tahmini oluşturma](generate-statistical-baseline-forecast.md)

[Temel tahminde manüel ayarlamalar yapma](manual-adjustments-baseline-forecast.md)

[Düzeltilen tahmini yetkilendirme](authorize-adjusted-forecast.md)

[Tahmin doğruluğunu izleme](monitor-forecast-accuracy.md)

[Bir talep tahmini hesaplarken aykırı değerleri geçmiş hareket verilerinden kaldırma](remove-historical-outliers-calculating-demand-forecast.md)

[Talep tahmini işlevini genişletme](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
