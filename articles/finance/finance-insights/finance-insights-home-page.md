---
title: Finance Insights giriş sayfası
description: Mali içgörüler, şirketinizin nakit akışını doğru ve anlaşılır şekilde tahmin etmek için yapılandırılabilir ve genişletilebilir modeller sağlar, bekleyen alacak ödemeleri için ödemeyi ne zaman alacağınızı tahmin eder ve bütçeleme sürecinizi hızlandırabilecek bir bütçe teklifi oluşturur. Tüm bu özellikler akıllı makine öğrenimi modellerine dayanır.
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2f04ef1a0de815596f629fede25a247c58e026f4
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643890"
---
# <a name="finance-insights-home-page"></a>Finance Insights giriş sayfası

[!include [banner](../includes/banner.md)]

Finance Insights, şirketinizin nakit akışını doğru ve anlaşılır şekilde tahmin etmek için yapılandırılabilir ve genişletilebilir çözümler sağlar, bekleyen alacak ödemeleri için ödemeyi ne zaman alacağınızı tahmin eder ve bütçeleme sürecinizi hızlandırabilecek bir bütçe teklifi oluşturur. Bu özellikler, sağladığınız verileri kullanarak (bir bürodan tüketici rapor bilgileri gibi üçüncü bir tarafın verileri de dahil) modeller oluşturmak için akıllı makine öğrenme şablonlarını kullanır. Bu akıllı yetenekler karar verme ve geçerli ve beklenen iş sorunlarını etkili şekilde yanıtlamak için önlem almanıza yardımcı olur. Finance Insights ile kullanılan veya çıktısını aldığınız tüm veriler sizin sorumluluğunuzdadır.

> [!NOTE]
> Finance Insights, Amerika Birleşik Devletleri, Kanada, Avrupa, Asya Pasifik, Japonya, Avusturalya, Yeni Zelanda ve Birleşik Krallık'ta dağıtım için sunulmuştur. Microsoft, destek sunduğu bölge sayısını kademeli olarak artırmaktadır.

## <a name="prerequisites"></a>Önkoşullar

Bu bölümde, Mali içgörülerin kullanımıyla ilgili gereksinimler listelenmiştir. Mümkün olan her yerde, ek bilgi kaynaklarının bağlantıları sağlanmıştır.

### <a name="system-requirements"></a>Sistem gereksinimleri

Finance Insights önizlemesi için Katman 2 ortamı (çoklu kutu) gereklidir. Ortamlar hakkında arka plan bilgileir için [Ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) konusuna bakın.

### <a name="version-requirements"></a>Sürüm gereksinimleri

Bu makale, Microsoft Dynamics 365 Finance 10.0.21 ve sonraki sürümleri için geçerlidir.

### <a name="license-requirements"></a>Lisans gereksinimleri

Finance Insights, mali öngörüler oluşturmak için AI Builder kredilerini kullanır. Bunun için gerekli tüm lisanslar kiracı lisansına dahil edilir. Her Dynamics 365 Finance kiracısına aylık 20.000 AI Builder kredisi sağlanır. İş gereksinimleri için ek kredi gerekiyorsa, bunlar doğrudan AI Builder'dan satın alabilir.

### <a name="historical-data-requirements"></a>Geçmişe ait veri gereksinimleri

Müşteri ödeme tahminleri özelliği için kullanılan makine öğrenimi modelinin doğru şekilde eğitimi için en az bir yıllık müşteri faturası gereklidir. Nakit akışı tahminlerinde üç yıl geçmiş veri önerilir. Akıllı bütçe teklifleri için üç yıllık geçmiş bütçe ve/veya fiili değer kullanılması önerilir.

## <a name="configure-finance-insights"></a>Finance Insights'ı yapılandırma

Finance Insights kullanabilmeniz için bazı yapılandırma adımlarını tamamlamanız gerekir. Mali içgörüleri yapılandırma hakkında daha fazla bilgi için bkz. [Mali içgörülerde yapılandırma](configure-for-fin-insites.md).

## <a name="create-a-data-integrator-project"></a>Veri tümleştirici projesi oluşturma

Makine öğrenimi modelinin ürettiği verilerin Dynamics 365 Finance'e geçebilmesi için bir veri tümleştirici projesi oluşturmanız gerekir. Bu projeyi oluşturma adımları için bkz. [Veri tümleştiricisi projesi oluşturma](create-data-integrate-project.md).

## <a name="enable-finance-insights-capabilities"></a>Mali içgörüler özelliklerini etkinleştirme

Yapılandırma adımlarını tamamlayıp tanıtım verilerini ayarladığınızda, kullanmayı planladığınız her özelliği açmanız ve ayarlamanız gerekir: müşteri ödeme tahminleri, nakit akışı tahmini ve bütçe teklifleri.

### <a name="enable-customer-payment-predictions"></a>Müşteri ödeme tahminlerini etkinleştirme
Müşteri ödeme tahminlerini test etmek için tanıtım verileri kullanıyorsanız, yapay zeka modelinizi başarılı şekilde oluşturmak için ek tanıtım verilerini içeri aktarmanız gerekebilir. 

Müşteri ödeme tahminlerini etkinleştirmek için, müşterilerin bekleyen faturaları ne zaman ödeyeceğine ve belirli faturaların ne zaman ödeneceğine dair tahminler oluşturmak için kuruluşunuzun verilerini kullanan bir makine öğreinimi modeli oluşturma adımlarını tamamlamanız gerekir. Daha fazla bilgi ve tamamlanması gereken adımlar için bkz. [Müşteri ödeme tahminlerini etkinleştirme](enable-cust-paymnt-prediction.md). 

### <a name="enable-cash-flow-forecasting"></a>Nakit akışı tahminini etkinleştirme
Nakit akışı tahmini özelliğini etkinleştirmek için, nakit akışı tahminleri oluşturmak üzere kuruluşunuzun verilerini kullanan bir makine öğrenimi modeli oluşturmak için bir dizi adımı tamamlamanız gerekir. Daha fazla bilgi ve tamamlanması gereken adımlar için bkz. [Nakit akışı tahminini etkinleştirme](enable-cash-flow-forecasting.md).

### <a name="enable-budget-proposals"></a>Bütçe tekliflerini etkinleştirme

Bütçe teklifleri özelliği, bütçe teklifi oluşturmak için kuruluşunuzun geçmiş verileriyle birlikte bir makine öğrenimi modeli kullanır. Oluşturulan teklif, el ile gerçekleştirilen bir işlemden daha etkili ve verimli olan bir bütçeleme işlemi başlatmanıza yardımcı olabilir. Bu özelliği etkinleştirmekle ilgili belirli adımlar için bkz. [Bütçe tekliflerini etkinleştirme](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Mali içgörüler özelliklerini kullanma

### <a name="using-customer-payment-predictions"></a>Müşteri ödeme tahminlerini kullanma

- Müşteri ödeme tahminlerinin tahsilat faaliyetlerini proaktif şekilde başlatmak için gerekli bilgileri nasıl sağlayabileceğini öğrenmek için bkz. [Müşteri ödeme tahminlerini kullanma](use-customer-payment-predictions.md).
- Özelliği kullanmayı başlattıktan sonra tahmin modelinin etkililiğini değerlendirmenize yardımcı olabilecek bilgiler için bkz. [İlk müşteri ödeme tahmini modelini değerlendirme](evaluate-payment-prediction.md).
- Tahmini oluşturmak ve böylece verimliliğini artırmak için kullanılan verileri ayarlamanıza yardımcı olabilecek bilgiler için bkz. [Tahmin modelini iyileştirme](improve-model.md).
- AI tahmin modellerinin sonuçları hakkında daha fazla bilgi edinmek için bkz. [Makine öğrenimi modellerinin sonuçları](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Nakit akışı tahminlerini kullanma

Nakit akışı tahmini özelliği, nakit pozisyonunuzu daha doğru tahmin etmenize yardımcı olabilir. Akıllı nakit akışı tahmini, Dynamics 365 Finance'teki mevcut nakit akışı tahmin işlevinin üzerine kurulmuştur. Mevcut özelliği incelemek için bkz. [Nakit akışı tahmini](../cash-bank-management/cash-flow-forecasting.md).

- Nakit akışı tahminlerindeki yeni özellikler hakkında bilgi edinmek için bkz. [Nakit akışı tahmini](cash-flow-forecast-intro.md).
- Nakit akışı tahmininize dahil etmek üzere dış verilerin içeri aktarılması hakkında bilgi için bkz. [Nakit akışı tahminlerinde dış verileri kullanma](external-data-in-cash-flow.md). 
- Kısa vadeli nakit akışını öngörmek için yapay zeka modelinin nasıl kullanılacağı hakkında bilgi için bkz. [Nakit konumu](cash-position.md).
- Nakit akışı pozisyonlarının ve nakit akışı tahminlerinin anlık görüntü olarak kaydedilmesi ve anlık görüntüyü gerçek değerlerle karşılaştırmak hakkında bilgi için bkz. [Anlık görüntülere genel bakış](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Bütçe teklifini kullanma

Bütçenin oluşturulmasını hızlandırma hakkında bilgi için bkz. [Bütçe teklifleri](budget-proposals.md). 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
