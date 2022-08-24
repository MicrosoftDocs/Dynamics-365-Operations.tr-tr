---
title: Regulatory Configuration Service (RCS) - Lifecycle Services (LCS) depolama kullanımdan kalkma
description: Bu makalede, Regulatory Configuration Service'ın (RCS) kullanıma sunulmasının bir parçası olarak Microsoft Dynamics Lifecycle Services'ın (LCS) kullanımdan kaldırılmasıyla ilgili bilgiler sağlanmaktadır.
author: kfend
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.custom: 97423
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
ms.openlocfilehash: 717a2b9b00e137631a7cb9a188bdcf1b33e6af02
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277229"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) depolama kullanımdan kalkma

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services'ın (LCS), Elektronik raporlama (ER) yapılandırmaları için saklama deposu olarak kullanılma özelliği kullanımdan kaldırılıyor. Bu kullanımdan kaldırma aşağıdaki değişiklikleri içerecektir:

- Microsoft Dynamics 365 uygulamalarında kullanılan Microsoft tarafından üretilmiş yapılandırmalar artık LCS'deki Paylaşılan varlık kitaplığında yayımlanmayacak. Bunun yerine, yalnızca RCS Global deposu aracılığıyla yayımlanacaklar. Ancak, Dynamics AX 2012 için olan yapılandırmalar, AX 2012 için desteği yaşam döngüsü sona erene kadar LCS'deki Paylaşılan varlık kitaplığında yayımlanmaya devam edecek.
- Finans ve operasyon uygulamalarından ve RCS'den alınan yapılandırmaları LCS içindeki Proje varlığı kitaplığına yüklemenize olanak tanıyan işlev devre dışı bırakılacaktır. Ancak, Proje varlığı kitaplığına yapılandırma yüklemek için LCS'deki tarayıcıyı yine de kullanabilirsiniz. Bu nedenle, çözüm paketlerine eklenmek üzere LCS'ye yapılandırma eklemeye devam edebilirsiniz.
- LCS'deki yapılandırmaların içe aktarılması, bir süre için finans ve operasyon uygulamalarında ve RCS'de kullanılabilir olmaya devam edecektir. Ancak bu işlev de bir süre sonra kullanımdan kaldırılacaktır. (Net kullanımdan kaldırma tarihi daha sonra açıklanacaktır.)

## <a name="deprecation-notice"></a>Kullanımdan kaldırma bildirimi

LCS'nin depolama olarak kullanım özelliğinin kaldırılacağı bilgisi [Dynamics 365 Finance'te kaldırılan veya kullanımdan kaldırılan özellikler - LCS Kullanımdan Kaldırma bildirimi](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release) makalesinde paylaşılmıştı. Planlanan kullanımdan kaldırma tarihi: 1 Nisan 2022.

## <a name="key-features"></a>Önemli özellikler

- ER yapılandırmalar ve Genelleştirme özellikleri oluşturmak ve düzenlemek için RCS'yi kullanın.
- Yapılandırmalarınızda hızlıca değişiklikler yapabilmeniz ve bu değişiklikleri test edebilmeniz için, yapılandırmaları doğrudan RCS tasarımcısından Dynamics 365 Finance ortamı gibi bağlı bir uygulamaya gönderin.
- Merkezi olarak, yönetim deposunun merkezi depolama yoluyla hem ER konfigürasyonların hem de genelleştirme özelliklerinin yaşam döngüsünü merkezi olarak depolayın, paylaşın ve yönetin.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Tek seferlik ve sürekli eylemler için kılavuz

Bu bölümde, bir kez tamamlanması gereken adımlar açıklanmaktadır. Ayrıca, daha sonra devamlı olarak tamamlanması gereken adımları da açıklar.

### <a name="one-time-action"></a>Tek seferlik eylem

LCS'deki tüm gerekli yapılandırmaları RCS 'ye aktarın ve sonra bunları RCS'den genel depoya yayımlayın. Türetilmiş yapılandırmaları LCS'de depolamak için projeye özel varlık kitaplıkları kullanıyorsanız, LCS hâlâ erişilebilir durumdayken aşağıdaki adımları tamamlamanız gerekir.

1. Zaten kullanılabilir bir RCS örneği yoksa, kullanılabilir bir örnek sağlayın. Daha fazla bilgi için bkz. [RCS'ye genel bakış](rcs-overview.md).
2. Sağlanan RCS örneğinde, Varlık kitaplığındaki türetilmiş ER yapılandırmaları içeren her LCS projesi için uygun LCS deposunu kaydedin.
3. LCS depolarından ER yapılandırmalarını RCS'ye aktarın. Daha fazla bilgi için bkz. [Yapılandırmaları LCS'den içe aktarma](/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services).
4. Genel depo otomatik olarak sağlanmazsa, RCS'de kaydedin.
5. Geçerli RCS örneğindeki tüm türetilmiş yapılandırmaları Genel depoya yükleyin. Karşıya yüklemeye yardımcı olması için **Konfigürasyon paketleri** özelliğini kullanın. Daha fazla bilgi için bkz. [RCS genel depo yüklemesi](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Gelecekte

Aşağıdaki amaçlar için RCS'de görsel tasarımcıları kullanın:

- Microsoft tarafından sağlanan şablonları genişletin.
- Kuruluşunuzun gerektirdiği yeni yapılandırmalar oluşturun.
- Elektronik faturalama ve vergi hesaplama servisi için Genelleştirme özelliklerini özelleştirin.

Aşağıdaki amaçlar için Genelleştirme depolarını kullanın:

- Microsoft tarafından üretilen yapılandırmalara ve Genelleştirme özelliklerine erişin.
- Oluşturduğunuz veya genişletilen konfigürasyonları depolama için Genel depoya yükleyin ve bunları kuruluşunuzun Dynamics 365 uygulama ortamları veya harici organizasyonlarla paylaşın. Daha fazla bilgi için bkz. [RCS'de ER yapılandırması oluşturma ve Genel depoya yükleme](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Bu değişiklik, LCS'nin yapılandırmalar için merkezi depolama olarak kullanılamayacağı anlamına mı geliyor?

Evet. Finans ve operasyon uygulamalarından alınan yapılandırmaları LCS içindeki Proje varlığı kitaplığına yüklemenize olanak tanıyan işlev kullanımdan kaldırılacaktır. Ancak, Proje varlığı kitaplığına yapılandırma yüklemek için LCS'deki tarayıcıyı yine de gerektiği şekilde kullanabilirsiniz.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>RCS'nin, genel şablon dosyalarını içe aktarma için bir yedek depo olduğunu düşünmüştüm. Yapılandırmaları depolamak için kullanıldığını düşünmemiştim. Hangisi doğru?

RCS, ER yapılandırmaları oluşturma ve düzenlemeye yönelik bir tasarım hizmetidir. RCS'nin, Genel depo olarak bilinen kendi deposu vardır. Bu depo, RCS'de oluşturulan yapılandırmaları depolamak için kullanılır. LCS'nin depolama olarak kullanımı kullanım dışı bırakıldıktan sonra, Microsoft yapılandırmalarının tek kaynağı Genel depo olacak. LCS'den RCS'ye gereksinim duyduğunuz tüm yapılandırmaları aktarmak ve sonra bunları Genel depoya yayımlamak için bir defalık eylemi tamamlamanız gerekir.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>LCS olmadan, "test" ve "üretim" yapılandırmalarını kolayca yönetmek ve transfer etmek için önerilen saklama yöntemi nedir?

RCS, *bağlı uygulama* kavramını kullanır. Bağlı uygulama, RCS ve tüm finans ve operasyon uygulaması örnekleri arasında bir bağlantı oluşturur. Yapılandırmaları düzenlemek üzere RCS kullanılabileceği için, bağlı uygulama yapılandırmaları doğrudan tasarımcıdan finans ve operasyon uygulamaları ortamına göndermek için kullanılabilir. Bu nedenle, LCS proje düzeyinde depolama yerine, yapılandırmalarınızı hızlı şekilde değiştirebilir ve test edebilirsiniz.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Kurulum ve yönetimi gösteren örnekler var mı?

Örnek yoktur, ancak yapılandırmalarınızı RCS Genel deposuna geçirmek için bu makaledeki önceki adımları tamamlayabilirsiniz.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>RCS, Elektronik raporlama konfigüre etmek için ön koşul mudur?

Evet. RCS, elektronik faturalama ve vergi hesaplama servisi gibi Genelleştirme hizmetleri tarafından kullanılan Genelleştirme özelliklerinin kurulumunu destekleyen yetenekleri içerir. Ancak, hizmet, yeni ER yapılandırmalarını genişletmenizi veya oluşturmanızı sağlayan görsel tasarımcı işlevselliğine sahiptir. RCS ayrıca, hem ER konfigürasyon hem de Genelleştirme özellikleri için yaşam döngüsü yönetimi sağlar.

### <a name="which-regions-can-rcs-be-deployed-in"></a>RCS, hangi bölgeler dağıtılacaktır?

RCS, aşağıdaki Azure bölgelerinde kullanıma sunulmuştur:

- Amerika Birleşik Devletleri
- Hindistan
- Fransa
- Avrupa

Ürün desteği hakkında daha fazla bilgi için bkz. [Dynamics Genelleştirme hizmetlerine genel bakış](globalization-services-overview.md). Coğrafi destek hakkında daha fazla bilgi için bkz. [Dynamics 365 ve Power Platform: Kullanılabilirlik, veri konumu, dil ve yerelleştirme](https://aka.ms/rcs/D365Productavailabilityguide).

### <a name="whats-the-cost-of-using-rcs"></a>RCS kullanmanın maliyeti nedir?

RCS ve Genelleştirme deposu, mevcut finans ve operasyon uygulama lisanslarının bir parçası olarak ücretsiz olarak sağlanır. RCS tasarım hizmetinin kullanımıyla veya genel depoda konfigürasyonlarda depolanan ayrı maliyet yoktur. Şu anda konfigürasyonların veya bağlı uygulamaların sayısında sınır yoktur.
