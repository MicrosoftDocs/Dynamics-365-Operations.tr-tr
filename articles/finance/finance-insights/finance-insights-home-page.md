---
title: Mali içgörüler giriş sayfası (önizleme)
description: Mali içgörüler, şirketinizin nakit akışını doğru ve anlaşılır şekilde tahmin etmek için yapılandırılabilir ve genişletilebilir modeller sağlar, bekleyen alacak ödemeleri için ödemeyi ne zaman alacağınızı tahmin eder ve bütçeleme sürecinizi hızlandırabilecek bir bütçe teklifi oluşturur. Tüm bu özellikler akıllı makine öğrenimi modellerine dayanır.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f0d709ef81fd43c009bf36aba2d4be949b1a737c
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338241"
---
# <a name="finance-insights-home-page-preview"></a>Mali içgörüler giriş sayfası (önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Mali içgörüler, şirketinizin nakit akışını doğru ve anlaşılır şekilde tahmin etmek için yapılandırılabilir ve genişletilebilir modeller sağlar, bekleyen alacak ödemeleri için ödemeyi ne zaman alacağınızı tahmin eder ve bütçeleme sürecinizi hızlandırabilecek bir bütçe teklifi oluşturur. Tüm bu özellikler akıllı makine öğrenimi modellerine dayanır. Bu yeni özellikler satıcı ödemeleri ve tahsilatlardaki otomasyonla birleştirildiğinde, karar verme sürecini hızlandıran ve geçerli ve beklenen ticari zorluklara etkili şekilde yanıt vermek üzere önlem almanıza yardımcı olan kapsamlı ve akıllı finans sistemi sunar.

> [!NOTE]
> Finance Insights önizlemesi, Amerika Birleşik Devletleri, Kanada, Avrupa, Asya Pasifik, Avusturalya, Yeni Zelanda ve Birleşik Krallık'ta dağıtım için sunulmuştur. Microsoft, destek sunduğu bölge sayısını kademeli olarak artırmaktadır. Finance Insights'ı Üretim ortamlarında etkinleştirmek için [Data Lake'e aktar](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) özelliklerinin üretim ortamında etkinleştirilmiş olması gerekir.

> [!NOTE]
> Bu işlevsellik, bir önizleme özelliği kümesi olarak sunuluyor. Önizleme özelliği olduğundan, elde edilen makine öğrenimi modellerini iş kararlarını almak veya bütçeleme tekliflerine yön vermek için kullanmamalısınız. Bu özelliğin kullanımı [Ek Kullanım Koşulları](https://go.microsoft.com/fwlink/?linkid=2105274) tarafından yönetilir.

## <a name="prerequisites"></a>Önkoşullar

Bu bölümde, Mali içgörülerin kullanımıyla ilgili gereksinimler listelenmiştir. Mümkün olan her yerde, ek bilgi kaynaklarının bağlantıları sağlanmıştır.

### <a name="legal-requirements"></a>Yasal gereksinimler

Önizleme programına başvurmak için [Dynamics 365 Finance için Mali içgörüler önizleme sözleşmesi](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u) formunu doldurun.

### <a name="system-requirements"></a>Sistem gereksinimleri

Finance Insights önizlemesi için Katman 2 ortamı (çoklu kutu) gereklidir. Ortamlar hakkında arka plan bilgileir için [Ortam planlama](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) konusuna bakın.

### <a name="version-requirements"></a>Sürüm gereksinimleri

Bu belge, Finance and Operations uygulamalarının (Platform update 35) 10.0.11 sürümü ve sonraki sürümleri için geçerlidir.

### <a name="historical-data-requirements"></a>Geçmişe ait veri gereksinimleri

Müşteri ödeme tahminleri özelliği için kullanılan makine öğrenimi modelinin doğru şekilde eğitimi için en az bir yıllık müşteri faturası gereklidir.

### <a name="role-and-permission-requirements"></a>Rol ve izin gereksinimleri

Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Power Apps ve Azure'da değişiklikler yapılacaktır. Bu ortamlarda doğru izinler gereklidir. Aşağıda yapılacak değişikliklere bazı örnekleri görebilirsiniz:

- Microsoft Power Platform'da yeni bir ortam oluşturulacaktır.
- Azure'da bir depolama hesabı, anahtar kasası ve uygulama oluşturulacaktır.
- Active Directory kiracı yöneticisi, AI Builder uygulamasına veri gölüne erişim izni vermesi gerekecektir.
- Bu özellik Dynamics 365'te etkinleştirilecektir.

Azure, Microsoft Dataverse ve LCS'te kaynak oluşturma ve yönetme işlemi hakkında bilgi sahibi olmak bu işlemi tamamlamak için faydalı olacaktır.

## <a name="configure-finance-insights"></a>Mali içgörüleri yapılandırma

Mali içgörüleri kullanabilmeniz için bazı yapılandırma adımlarını tamamlamanız gerekir. Finans Insights'ı yapılandırma hakkında daha fazla bilgi için bkz.
  - 10.0.19 sürümüne kadar olan sürümler için: [10.0.19 sürümüne kadar Finance Insights (önizleme)](configure-for-fin-insites.md).
  - 10.0.20 ve sonrasındaki sürümler için: [10.0.20 sürümü ve sonrası için Finance Insights (preview) yapılandırması](configure-for-fin-insites-PubPrvw.md).

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

Akıllı nakit akışı tahmini, Dynamics 365 Finance'teki mevcut nakit akışı tahmin işlevinin üzerine kurulmuştur. Mevcut özelliği incelemek için bkz. [Nakit akışı tahmini](../cash-bank-management/cash-flow-forecasting.md).

- Müşteri ödeme tahminlerinin tahsilat faaliyetlerini proaktif şekilde yapmak için gerekli bilgileri nasıl sağlayabileceğini öğrenmek için bkz. [Müşteri ödeme tahminlerini kullanma](use-customer-payment-predictions.md).
- Özelliği kullanmayı başlattıktan sonra tahmin modelinin etkililiğini değerlendirmenize yardımcı olabilecek bilgiler için bkz. [İlk müşteri ödeme tahmini modelini değerlendirme](evaluate-payment-prediction.md).
- Tahmini oluşturmak ve böylece verimliliğini artırmak için kullanılan verileri ayarlamanıza yardımcı olabilecek bilgiler için bkz. [Tahmin modelini iyileştirme](improve-model.md).

AI tahmin modellerinin sonuçları hakkında daha fazla bilgi edinmek için bkz. [Makine öğrenimi modellerinin sonuçları](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Nakit akışı tahminlerini kullanma

Nakit akışı tahmini özelliği, nakit pozisyonunuzu daha doğru tahmin etmenize yardımcı olabilir. 

- Nakit akışı tahminlerindeki yeni özellikler hakkında bilgi edinmek için bkz. [Nakit akışı tahmini](cash-flow-forecast-intro.md).
- Nakit akışı tahmininize dahil etmek üzere dış verilerin içeri aktarılması hakkında bilgi için bkz. [Nakit akışı tahminlerinde dış verileri kullanma](external-data-in-cash-flow.md). 
- Kısa vadeli nakit akışını öngörmek için yapay zeka modelinin nasıl kullanılacağı hakkında bilgi için bkz. [Nakit konumu](cash-position.md).
- Nakit akışı pozisyonlarının ve nakit akışı tahminlerinin anlık görüntü olarak kaydedilmesi ve anlık görüntüyü gerçek değerlerle karşılaştırmak hakkında bilgi için bkz. [Anlık görüntülere genel bakış](payment-snapshots.md).

### <a name="using-budget-proposal"></a>Bütçe teklifini kullanma

Bütçenin oluşturulmasını hızlandırma hakkında bilgi için bkz. [Bütçe teklifleri](budget-proposals.md). 

## <a name="feedback-and-support"></a>Geri bildirim ve destek

Geri bildirim sağlamak veya destek almak istiyorsanız lütfen [Müşteri ödeme içgörüleri (Önizleme)](mailto:fiap@microsoft.com) ekibine e-posta gönderin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
