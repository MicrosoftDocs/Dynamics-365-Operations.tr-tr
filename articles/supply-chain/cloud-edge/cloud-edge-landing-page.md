---
title: Üretim ve ambar yönetimi iş yükleri için bulut ve uç ölçek birimleri
description: Bu konu, üretim ve ambar yönetimi iş yükleri için bulut ve uç ölçek birimleri hakkında bilgi sağlar.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: dbe5833d4c9d8038fcebf1d9d446af757c834e42a2f77f10c7eb7268e738ed28
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780686"
---
# <a name="cloud-and-edge-scale-units-for-manufacturing-and-warehouse-management-workloads"></a>Üretim ve ambar yönetimi iş yükleri için bulut ve uç ölçek birimleri

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Microsoft Dynamics 365 Supply Chain Management ölçek birimi özelliği, hizmetin kullanımını düzenleyen koşullar altında kullanıma sunulur. Daha fazla bilgi için [Microsoft Dynamics Yasal Bilgiler](https://go.microsoft.com/fwlink/?LinkID=290927) bölümüne bakın.
>
> Bulut ve uç ölçek birimlerini etkinleştirdiğinizde, bulut ve uç ölçek birimlerinin yapılandırması ve işlenmesiyle ilgili bazı verilerin ABD'de bulunan bir veri merkezinde depolanabileceğini anladığınızı onaylamanız istenir. Bulut ve uç ölçek birimleri için veri işleme hakkında daha fazla bilgi edinmek için, bu konunun sonraki bölümlerinde yer alan [Ölçek birimleri yönetimi sırasında veri işleme](#data-processing-management) bölümüne bakın.

## <a name="core-value-proposition-for-scale-units"></a>Ölçek birimleri için temel değer önerisi

Üretim ve dağıtım ile çalışan şirketler, önemli iş süreçlerini kesintiye uğramadan ve büyük ölçekte 7/24 çalıştırabilmelidir. Bulut ve uç ölçek birimleri, şirketlerin zaman zaman ağ bağlantısı veya gecikme sorunlarıyla karşılaşsalar bile, görev açısından kritik öneme sahip önemli üretim ve ambar işlemlerini kesintisiz olarak yürütmelerine olanak tanır.

Bulut ve uç ölçek birimleri atölye ve ambar yürütme iş yüklerinin farklı ortamlar arasında dağıtılmasını sağlar. Bu işlevsellik, performansın artırılmasına, hizmet kesintilerinin önlenmesine ve çalışma süresini en üst düzeye çıkarılmasına yardımcı olabilir. Ölçek birimleri, Supply Chain Management aboneliğiniz için aşağıdaki eklentiler aracılığıyla sağlanır:

- Dynamics 365 Supply Chain Management için Bulut Ölçek Birimi Eklentisi ( *Nisan 2021*'de kullanıma sunulmuştur)
- Dynamics 365 Supply Chain Management için Uç Ölçek Birimi Eklentisi ( *yakında kullanıma sunulacaktır*)

İş yükü özellikleri, artımlı geliştirmeler aracılığıyla sürekli olarak yayımlanmaktadır.

## <a name="scale-units-and-dedicated-workloads"></a>Ölçek birimleri ve özel iş yükleri

Ölçek birimleri, özel işleme kapasitesi ekleyerek merkezi Supply Chain Management hub ortamınızı genişletir. Ölçek birimleri bulutta çalışabilir. Alternatif olarak, yerel tesislerde uçta ve şirket içinde de çalıştırabilirsiniz.

:::image type="content" source="./media/cloud_edge-HeroDiagram.png" alt-text="Ölçek birimlerini içeren Dynamics 365.":::

Ölçek birimleri, atanan iş yükleri için esneklik, güvenilirlik ve ölçek sağlar. Uç ölçek birimlerinin bağlantısı bulut merkezi ortamından geçici olarak kaldırılabilir ve çalışanlar uçta atanan iş yüklerinde çalışmaya devam edebilir.

*İş yükü*, hariç tutulup bir ölçek birimine devredilebilen tanımlanmış bir iş işlevi kümesidir. Ambar yönetimi için iş yükü yayımlanmış olsa da, üretim yürütme iş yükü hala önizleme aşamasındadır.

[Ölçek Birimi Yöneticisi portalını](https://sum.dynamics.com) kullanarak merkez ortamınızı ve bulut ölçek birimlerini seçili iş yükleri için yapılandırabilirsiniz. Ölçek birimi başına birden çok iş yükü de atayabilirsiniz. Geçerli sürümdeki bulut ölçek birimlerinin önkoşulları ve sınırlamaları hakkında bilgi için, bu konunun sonraki bölümlerinde yer alan [Bulut ölçek birimleri için önkoşullar ve sınırlamalar](#cloud-scale-unit-prerequisites) bölümüne bakın.

### <a name="dedicated-warehouse-management-workload-capabilities-in-a-scale-unit"></a>Bir ölçek birimindeki özel ambar yönetimi iş yükü özellikleri

Ambar yönetimi iş yükü, genel kullanıma sunaln ölçek birimleri için dağıtılmış ilk iş yüküdür.

Ambar yönetimi için ölçek birimleri aşağıdaki özellikleri sunar:

- Sistem, satış siparişleri ve talep stok yenilemesi için seçili dalga yöntemlerini işleyebilir.
- Ambar çalışanları, Ambar Yönetimi mobil uygulamasını kullanarak satış ve talep stok yenileme ambar işlerini çalıştırabilir.
- Ambar çalışanları,Ambar Yönetimi mobil uygulamasını kullanarak eldeki stokta sorgu çalıştırabilirler.
- Ambar çalışanları Ambar Yönetimi mobil uygulamasını kullanarak stok hareketleri oluşturabilir ve çalıştırabilir.
- Ambar çalışanları satın alma siparişlerini kaydedebilir ve Ambar Yönetimi mobil uygulamasını kullanarak siparişleri kaydedebilir.

Daha fazla bilgi için bkz. [Bulut ve uç ölçek birimleri için ambar yönetimi iş yükleri](cloud-edge-workload-warehousing.md).

### <a name="dedicated-manufacturing-execution-workload-capabilities-in-a-scale-unit"></a>Bir ölçek birimindeki özel üretim yürütme iş yükü özellikleri

Üretim iş yükünün ilk sürümü şu anda önizleme aşamasındadır ve aşağıdaki özellikleri sunar:

- Makine operatörleri ve üretim katı denetçileri operasyonel üretim planına erişebilirler.
- Makine operatörleri, gizli ve süreç üretim işleri çalıştırarak planı güncel tutabilir.
- Üretim katı denetçisi, çalışma planını ayarlayabilir.
- Çalışanlar, doğru çalışan ücret hesaplaması sağlamak için uçta giriş ve çıkış için zaman ve devam bilgilerine erişebilir.

Daha fazla bilgi için bkz. [Bulut ve uç ölçek birimleri için üretim yürütme iş yükleri](cloud-edge-workload-manufacturing.md).

## <a name="considerations-before-you-enable-the-distributed-hybrid-topology-for-supply-chain-management"></a>Supply Chain Management için dağıtılmış, karma topolojiyi etkinleştirmeden önce dikkat edilmesi gereken noktalar

Dağıtılmış, karma topolojiyi etkinleştirerek, Supply Chain Management bulut ortamınızın geçişini yaparak bir merkez olarak çalışmasını sağlarsınız. Ayrıca, bulutta veya uçta ölçek birimleri olarak yapılandırılmış ek ortamları da ilişkilendirebilirsiniz.

### <a name="prerequisites-and-limitations-for-cloud-scale-units"></a><a name="cloud-scale-unit-prerequisites"></a>Bulut ölçek birimleri için önkoşullar ve sınırlamalar

Ölçek birimlerinin geçerli sürümünde, bazı özellikler henüz kullanılabilir değildir ancak zaman içinde artımlı sürümlerle eklenebilir.

#### <a name="you-must-be-a-licensed-customer-of-supply-chain-management"></a>Supply Chain Management lisanslı müşterisi olmanız gerekir

Dağıtılmış topolojiye katılmak için Supply Chain Management lisansına sahip olmanız gerekir. Mevcut bulut ortamınız hibrit topolojinizde merkez haline gelecektir. Hem korumalı alan ortamlarını hem de üretim ortamlarını merkez ortamları olarak bildirebilir ve elde ettiğiniz eklentilere göre ölçek birimleri ekleyebilirsiniz.

#### <a name="your-existing-project-must-be-administered-via-the-global-commercial-version-of-lcs"></a>Mevcut projeniz LCS'nin küresel ticari sürümü aracılığıyla yönetilmelidir

Mevcut Microsoft Dynamics Lifecyle Services (LCS) projeniz aşağıdaki sürüm gereksinimlerini karşılamalıdır:

- Projeniz LCS'nin küresel ticari sürümü aracılığıyla [lcs.dynamics.com](https://lcs.dynamics.com) konumunda yönetilmelidir.
- LCS'nin yerel sürümleri ([eu.lcs.dynamics.com](https://eu.lcs.dynamics.com) ve [fr.lcs.dynamics.com](https://fr.lcs.dynamics.com) gibi) desteklenmez.
- LCS'nin Kamu Bulut sürümleri desteklenmez.
- LCS'nin Mooncake sürümü desteklenmez.

#### <a name="your-current-production-environment-must-be-of-the-self-service-type-in-lcs"></a>Mevcut üretim ortamınız LCS'de Self Servis türünde olmalıdır

Mevcut üretim ortamınız LCS'de **Self Servis** türüyle etiketlenmelidir. Bu tür, LCS projenizin kiracısının Azure Service Fabric barındırma modelini destekleyecek şekilde zaten dönüştürüldüğünü gösterir.

> [!IMPORTANT]
> Hizmet olarak altyapı (IaaS) olarak çalışan ortam türleri desteklenmez. Bu ortamlar genellikle LCS'deki **Microsoft Tarafından Yönetilen** türüyle etiketlenir. Bu tür ortamlarınız varsa, **Self Servis** türüne geçiş zaman çizelgenizi anlamak için Microsoft ilgili kişinizle birlikte çalışın.

Microsoft, Supply Chain Management'ın tüm bulut ortamlarını bir IaaS modelinden Service Fabric'te barındırılan bir topolojiye geçirme sürecindedir. Bu hareket, daha iyi ölçeklenebilirlik sağlar ve hizmet yönetimini kolaylaştırmaya yardımcı olur. Bu nedenle, dağıtım ve bakım işlemleri daha hızlıdır. Benzer şekilde, hizmet bileşenleri mikro hizmetler kavramına geçirilmektedir ve hizmet barındırma modeli sanal makine (VM) modelinden hafif kapsayıcılı mimariye [geçirilecektir](/virtualization/windowscontainers/about/containers-vs-vm).

Sonuç olarak, aynı Service Fabric tabanlı kapsayıcılı hizmet altyapısı, bir kurulumun bulutta bir merkez veya bulutta ya da uçta bir ölçek birimi olmasına bakılmaksızın hizmetin hem bulut hem de uç kurulumlarını destekleyecektir.

Ölçek birimlerini destekleyen hibrit topolojiye katılmadan önce, proje kiracınızın Service Fabric tarafından barındırılan modele geçirilmesi gerekir. Ayrıca, merkez olarak hareket edecek herhangi bir ortam dönüştürülmelidir.

> [!TIP]
> LCS proje kiracınızın durumunu sorgulamak için [LCS](https://lcs.dynamics.com/)'de ortamınızın türünü arayın veya iş ortağınıza ya da Microsoft ilgili kişinize başvurun.

#### <a name="local-business-data-on-premises-environments-arent-supported-as-hubs-for-scale-units"></a>Yerel iş verisi (şirket içi) ortamları ölçek birimleri için merkez olarak desteklenmez

Şirket içi ortamlar ölçek birimleri için merkez olarak çalışamaz. Merkez ortamları her zaman bulutta barındırılmalıdır.

#### <a name="scale-unit-management-capabilities-are-limited"></a>Ölçek birimi yönetimi yetenekleri sınırlıdır

İş yüklerinin taşınmasına yardımcı olabilecek yönetim yetenekleri sınırlıdır. Bazı yönetim işlemleri self servis olarak desteklenmez ve iş ortağınız veya Microsoft ilgili kişiniz aracılığıyla destek istemeniz gerekebilir. Örnek olarak, ölçek birimleri arasındaki bazı iş yükü hareketleri ve olağanüstü durum senaryolarındaki anlık geçici hareketler verilebilir.

#### <a name="metrics-and-measurements-arent-yet-available"></a>Ölçüler ve ölçümler henüz kullanılabilir değildir

Ölçek birimleriniz için en iyi uygulamayı seçmenize yardımcı olabilecek ölçüler ve ölçümler henüz kullanılabilir değildir. En faydalı uygulamayı seçmek için Microsoft ilgili kişinizle veya uygulama iş ortağınızla birlikte çalışın.

### <a name="data-processing-during-management-of-scale-units"></a><a name="data-processing-management"></a>Ölçek birimlerinin yönetimi sırasında veri işleme

Dynamics 365 ortamınızı bulut ve uç ölçek birimleri için dağıtılmış, karma topolojiyi desteklemek üzere etkinleştirdiğinizde, bazı yönetim hizmetleri LCS gibi yalnızca ABD'de barındırılır. Bu davranış, [Ölçek Birimi Yöneticisi portalı](https://sum.dynamics.com) tarafından kullanılan bazı yönetim ve yapılandırma bilgilerinin aktarımını ve depolanmasını etkiler. Burada bazı örnekler verilmiştir:

- Kiracı adlarınız ve kimlikleriniz
- LCS proje kimlikleriniz
- Oturum açmak için kullanılan yönetici ve proje sahibi e-posta adresleri
- Merkez ve ölçek birimleri için ortam kimlikleri
- Topolojinizin coğrafi bir haritada gösterilebilmesi için tüzel kişilerin ve tesislerin adları ve fiziksel adresleri de dahil olmak üzere iş yükü yapılandırmaları
- Ölçek birimlerinizin en faydalı kullanımını seçmenize yardımcı olmak için harita analizi sayfasında gösterilecek toplanan ölçümler (gecikme süresi ve aktarım hızı gibi)

ABD veri merkezlerine aktarılan ve buralarda depolanan veriler Microsoft veri saklama ilkelerine göre silinecektir. Gizliliğiniz Microsoft için önemlidir. Daha fazla bilgi için [Gizlilik Bildirimimizi](https://go.microsoft.com/fwlink/?LinkId=521839) okuyun.

## <a name="onboarding-in-two-stages"></a>İki aşamada katılım

Dağıtılmış, karma topolojiye katılma işleminin iki aşaması vardır. İlk aşamada, ölçek birimlerine sahip dağıtılmış topolojide çalıştıklarından emin olmak için özelleştirmeleri doğrulamanız gerekir. Korumalı alan ve üretim ortamları sadece ikinci aşamada taşınır.

### <a name="stage-1-evaluate-customizations-in-one-box-development-environments"></a>Aşama 1: Özelleştirmeleri yerleşik geliştirme ortamlarında değerlendirme

Korumalı alanınızı veya üretim ortamlarınızı eklemeye başlamadan önce işlemleri, özelleştirmeleri ve çözümleri doğrulayabilmeniz için yerleşik ortam (katman 1 ortam olarak da bilinir) gibi bir geliştirme kurulumunda ölçek birimlerini keşfetmenizi öneririz. Bu aşamada, veriler ve özelleştirmeler yerleşik ortamlara uygulanacaktır. Bir ortam merkez rolünü, diğeri ölçek birimi rolünü alır. Bu kurulum, sorunları tanımlamanın ve düzeltmenin en iyi yolunu sağlar. En son erken erişim (PEAP) derlemesi de bu aşamayı tamamlamak için kullanılabilir.

Aşama 1 için, [yerleşik geliştirme ortamları için ölçek birimi dağıtım araçlarını kullanmanız](https://github.com/microsoft/SCMScaleUnitDevTools) gerekir. Bu araçlar, merkez ve ölçek birimlerini bir veya iki ayrı yerleşik ortamda yapılandırmanıza olanak tanır. Araçlar GitHub'da kaynak kodunda ve ikili sürüm olarak sağlanır. Araçların nasıl kullanıldığını açıklayan [Adım adım kullanım kılavuz](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) içeren proje wiki'sini inceleyin.

### <a name="stage-2-acquire-add-ins-and-deploy-in-your-sandbox-and-production-environments"></a>Aşama 2: Eklentiler alıp korumalı alan ve üretim ortamlarınıza dağıtın

Korumalı alan veya üretim ortamlarınızdan birini yeni topolojiye eklemek için, bir veya daha fazla bulut ölçek birimi için (ve gelecekte uç ölçek birimleri için) eklentiler edinmeniz gerekir. Eklentiler, ölçek birimi ortamlarının dağıtılabilmesi için [LCS](https://lcs.dynamics.com/)'de karşılık gelen proje ve ortam yuvaları sağlar.

> [!NOTE]
> Ölçek birimi eklentileri sınırlı sayıda kullanıcıyla birleştirilmiş değildir ancak yöneticinin atadığı rollere bağlı olarak mevcut abonelikteki herhangi bir kullanıcı tarafından kullanılabilir.

Ölçek birimleri birden fazla stok tutma birimi (SKU) ve fiyatlandırma seçeneğiyle sunulur. Bu nedenle, planlanan aylık işlem hacminizi ve performans gereksinimlerinizi en iyi karşılayan seçeneği belirleyebilirsiniz.

Giriş düzeyi SKU *Temel* olarak ve daha performanslı SKU *Standart* olarak bilinir. Her SKU, belirli sayıda aylık işlemle önceden yüklenir. Ancak, her SKU için fazla kullanım eklentileri ekleyerek aylık işlem bütçesini artırabilirsiniz.

:::image type="content" source="media/SKUs-highlevel.png" alt-text="Bulut ölçek birimleri için eklentiler.":::

> [!TIP]
> Gereksinimlerinizi en iyi karşılayan boyutlandırmayı belirlemek için, gereksinim duyduğunuz aylık işlem boyutunu anlamak üzere iş ortağınız ve Microsoft ile birlikte çalışın.

Satın alınan her ölçek birimi eklentisi size yalnızca aylık bir işlem hacmi sağlamakla kalmaz, aynı zamanda LCS'de belirli sayıda ortam yuvasına da hak sağlar. Her Bulut Ölçek Birimi Eklentisi için bir yeni üretim yuvası ve bir yeni korumalı alan yuvasına sahip olursunuz. Ekleme işlemi sırasında, bu yuvalara sahip yeni bir LCS projesi eklenecektir. Yuvaların kullanım hakları sınırlıdır bu nedenle yuvalar bulut merkezine sahip ölçek birimleri olarak kullanılmalıdır.

Fazla kullanım eklentileri size yeni ortam yuvaları sağlamaz.

Daha fazla korumalı alan ortamı edinmek istiyorsanız, ek normal korumalı alan yuvaları satın alabilirsiniz. Microsoft daha sonra bu yuvaları karma topoloji için korumalı alan ölçek birimleri olarak etkinleştirmenize yardımcı olabilir.

## <a name="onboard-to-the-distributed-hybrid-topology-for-supply-chain-management"></a>Supply Chain Management için dağıtılmış, karma topoloji ekleme

### <a name="select-your-lcs-project-tenant-and-the-detailed-onboarding-process"></a>LCS projesi kiracınızı ve ayrıntılı ekleme işlemini seçin

Supply Chain Management için dağıtılmış, karma topolojiye nasıl katılacağınızı planlamayı tamamladıktan sonra, ekleme işlemine başlamak için [Ölçek Birimi Yöneticisi portalını](https://aka.ms/SCMSUM) kullanacaksınız. Portalda, **Dynamics 365 Kiracıları** sekmesini seçin. Bu sekme, hesabınızın parçası olduğu ve bir LCS projesinin sahibi veya ortam yöneticisi olduğunuz kiracıların listesini gösterir.

Aradığınız kiracı listede yoksa [LCS](https://lcs.dynamics.com/v2)'ye gidin ve bu kiracı için bir ortam yöneticisi veya LCS projesinin proje sahibi olduğunuzdan emin olun. Yalnızca seçilen kiracının Azure Active Directory (Azure AD) hesapları kayıt deneyimini tamamlama yetkisine sahiptir.

> [!NOTE]
> Değişiklikleri LCS'ye uyguladıktan sonra, kiracı listesinde değişikliklerin yansıması 30 dakika kadar sürebilir.

Liste, her kiracı için ekleme durumunu gösterir.

:::image type="content" source="media/cloud_edge-EnableHybrid1.png" alt-text="Dynamics 365 Kiracılar sekmesindeki kiracıların listesi.":::

LCS kiracısı için katılım istemek üzere **Başlamak için buraya tıklayın**'ı seçin. Koşulları kabul etmelisiniz. Ayrıca, Microsoft'un ekleme işlemiyle ilgili iletişimleri gönderebileceği bir iş e-posta adresi de sağlamanız gerekir.

:::image type="content" source="media/cloud_edge-EnableHybrid2.png" alt-text="Kiracı için kayıt gönderme.":::

Microsoft, kayıt formunda sağladığınız adrese bir e-posta göndererek isteğinizi gözden geçirecek ve sonraki adımlar hakkında sizi bilgilendirecektir. Microsoft, iş senaryonuz için karma topolojide ölçek birimlerini etkinleştirmek üzere sizinle yakından çalışacaktır.

Ekleme tamamlandıktan sonra, ölçek birimlerini ve iş yüklerini yapılandırmak için bağlantı noktasını kullanabilirsiniz.

### <a name="manage-cloud-scale-units-and-workloads-by-using-the-scale-unit-manager-portal"></a><a name="scale-unit-manager-portal"></a>Ölçek Birim Yöneticisi portalını kullanarak bulut ölçek birimlerini ve iş yüklerini yönetme

[Ölçek Birimi Yöneticisi portalına](https://aka.ms/SCMSUM) gidin ve kiracı hesabınızı kullanarak oturum açın. **Ölçek birimlerini yapılandır** sayfasında, önceden listelenmemişse bir hub ortamı ekleyebilirsiniz. Daha sonra ölçek birimleri ve iş yükleri ile yapılandırmak istediğiniz hub'ı seçebilirsiniz.

:::image type="content" source="media/cloud_edge-Manage.png" alt-text="Ölçek birimi ve iş yükü yönetimi deneyimi.":::

Aboneliklerinizde bulunan bir veya daha fazla ölçek birimini eklemek için **Ölçek birimleri ekle**'yi seçin.

**Tanımlanan iş yükleri** sekmesinde, ölçek birimlerinizden birine ambar yönetimi iş yükü eklemek için **İş yükü oluştur** düğmesini kullanın. Her iş yükü için iş yükü tarafından sahip olunacak işlemlerin bağlamını belirtmeniz gerekir. Ambar yönetimi iş yükleri için bağlam, belirli bir tesis ve tüzel kişilikteki belirli bir ambardır.

:::image type="content" source="media/cloud_edge-DefineWorkload.png" alt-text="İş yükü oluşturma.":::

> [!TIP]
> Zaman içinde, yaşam döngüsü yönetimi işlemlerini kolaylaştırmaya yardımcı olmak için Ölçek Birim Yöneticisi deneyimine artımlı geliştirmeler eklenecektir. Geçerli sürüme yönelik özellikler, Supply Chain Management için dağıtılmış, karma topolojiye katılma sürecinde olan müşteriler tarafından kullanılabilen bir katılım el kitabında belgelenmiştir. <!-- KFM: Add a link to the handbook when it is published -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
