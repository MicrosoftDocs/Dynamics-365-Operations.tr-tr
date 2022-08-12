---
title: Finans ve operasyon altyapısında İnsan Kaynakları sağlama
description: Bu makalede, finans ve operasyon altyapısında Microsoft Dynamics 365 Human Resources için yeni bir üretim ortamı sağlama işlemi açıklanır.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15060d8bdd598476081c22d7280319da3db0cb31
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178427"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Finans ve operasyon altyapısında İnsan Kaynakları sağlama

_**Uygulandığı Öğe:** Finans ve operasyon uygulaması altyapısında İnsan Kaynakları_ 

> [!NOTE]
> Temmuz 2022 tarihinden başlayarak tek başına İnsan Kaynakları altyapısında yeni İnsan Kaynakları ortamları sağlanamaz ve burada yeni Microsoft Dynamics Lifecycle Services (LCS) projeleri oluşturulamaz. Müşteriler, İnsan Kaynakları ortamları yalnızca finans ve operasyon altyapısı üzerinden dağıtılabilir.

Bu makalede, finans ve operasyon altyapısında Microsoft Dynamics 365 Human Resources için yeni bir üretim ortamı sağlama işlemi açıklanır.

## <a name="prerequisites"></a>Ön Koşullar

Yeni bir ortamı sağlamaya başlamak için aşağıdaki önkoşulların sağlanması gerekir:

- Human Resources'ı bir Bulut Çözümü Sağlayıcısı (CSP) veya kurumsal mimari (EA) sözleşmesi aracılığıyla satın almış olmalısınız. Zaten insan kaynakları hizmet planını içeren mevcut bir Dynamics 365 lisansınız varsa ve bu konudaki adımları tamamlayamıyorsanız Destek birimine başvurun.
- Genel yönetici, [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) hizmetinde oturum açmış ve yeni bir finans ve operasyon projesi oluşturmuş olmalıdır.

## <a name="provision-a-human-resources-trial-environment"></a>Human Resources deneme ortamı sağlama

> [!NOTE]
> Nisan 2022'den itibaren, tek başına çalışan uygulamada İnsan Kaynakları deneme ortamları kullanılamaz. Finans ve operasyon uygulamalarındaki İnsan Kaynakları özelliklerini değerlendirmeyle ilgilenen potansiyel müşteriler bunu, demo verileriyle birlikte ücretsiz 30 günlük deneme sürümünü kullanarak yapabilir. Dynamics 365 Finance, tek başına çalışan uygulamanın birleştirilmesi yoluyla Finance altyapısına getirilen İnsan Kaynakları özelliklerini içerecektir. Daha fazla bilgi için bkz. [İK tekliflerinin birleştirilmesi müşteriler için özellikleri bir araya getirir](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Dynamics 365 Finance denemeleri hakkında daha fazla bilgi için [bu adım adım kılavuza](../fin-ops-core/fin-ops/get-started/before-you-buy.md) bakın.

## <a name="plan-human-resources-environments"></a>Human Resources ortamlarını planlama

İlk Human Resources ortamınızı oluşturmadan önce, projeniz için ortam ihtiyaçlarını dikkatlice planlamalısınız. İnsan Kaynakları'na temel abonelikte iki ortam bulunur: üretim ortamı ve varsayılan standart kabul testi (Korumalı Alan) ortamı. Projenizin karmaşıklığına bağlı olarak, proje etkinliklerini desteklemek için ek korumalı alan ortamları satın alabilirsiniz.

Ek isteğe bağlı ortamlar için dikkat edilmesi gereken bazı hususlar:

- **Veri taşıma**: Korumalı alan ortamınızın proje boyunca test amacıyla kullanılmasını sağlamak için veri taşıma etkinlikleri. Ek bir ortama sahip olduğunuzda, test ve yapılandırma etkinlikleri aynı anda farklı bir ortamda gerçekleşirken veri geçişi etkinlikleri devam edebilir.
- **Tümleştirme**: Yerel tümleştirmeleri veya bordro, başvuran izleme sistemleri veya yan hak sistemleri ve sağlayıcıları gibi özel tümleştirmeleri içerebilen tümleştirmeleri yapılandırın ve test edin.
- **Eğitim**: Personelinizi yeni sistemin kullanımı konusunda eğitmek için bir dizi eğitim verisiyle yapılandırılmış ayrı bir ortama ihtiyacınız olabilir. 
- **Çok aşamalı proje**: Projenin ilk yayınlanmasından sonra planlanan bir proje aşamasında yapılandırmayı, veri geçişini, testi veya diğer etkinlikleri desteklemek için ek bir ortama ihtiyacınız olabilir.
- **Geliştirme**: Finans ve operasyonlar altyapısında, artık çözümü genişletebilir ve kendi özelleştirmelerinizi geliştirebilirsiniz. Her geliştiricinin kendi geliştirme ortamını kullanması gereklidir. Daha fazla bilgi için bkz. [Dağıtım ve erişim geliştirme ortamları](/fin-ops-core/dev-itpro/dev-tools/access-instances).
- **GOLD**: Yeni dağıtımlar için, yapılandırma ve veri geçişi için bozulmadan tutulan ayrı bir GOLD ortam kullanmak yaygın bir uygulamadır. Bu ortam, uygulama boyunca diğer ortamları yenilemek için kullanılabilir. Bu, temel yapılandırmaya ve veri geçişine sahip yeni üretim ortamını oluşturmak için kullanılır. Kullanıma almaya hazırlık sürecini tamamlayana kadar finans ve operasyon altyapısında bir üretim ortamı dağıtamazsınız. Daha fazla bilgi için bkz. [Kullanıma alma için hazırlık](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live).

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Ortamlarınızı değerlendirirken aşağıdaki yaklaşımı uygulamanızı öneririz:
>
> - Kullanıma almadan sahte bir geçiş yapmak için varsayılan standart kabul testinizi (eski adıyla Korumalı Alan) ortamınızı veya başka bir ortamı kullanın.
> - Kullanıma alma kesin bitiş işlemi sırasında son verileri üretim ortamına geçirmek için gereken her veri paketini içeren ayrıntılı bir kesin bitiş denetim listesi tutun. Bu öneri, yapılandırmalarınızı saklamak için ayrı bir GOLD ortamınız yoksa özellikle önemlidir.
> - Projeniz boyunca TEST ortamınız olarak varsayılan standart kabul testi (eski adıyla Korumalı Alan) ortamınızı ya da diğer katman 2 veya daha üstü bir ortamı kullanın. Ek ortamlara ihtiyacınız olursa kuruluşunuz bunları ek bir ücret karşılığında satın alabilir.

## <a name="create-an-lcs-project"></a>LCS projesi oluşturma

İnsan Kaynakları ortamlarınızı yönetmek üzere LCS'yi kullanmak için öncelikle bir LCS projesi oluşturmanız gerekir. İnsan Kaynakları ortamınızı finans ve operasyon altyapısına aktarıyorsanız finans ve operasyon uygulamaları için yeni bir LCS projesi oluşturmanız gerekir. Daha fazla bilgi için bkz: [İnsan Kaynakları ortamınızı taşıma](hr-admin-migrate-overview). Diğer finans ve operasyon uygulamaları için zaten bir LCS projeniz varsa **Özellik yönetimi** çalışma alanındaki İnsan Kaynakları özellikleri etkinleştirebilirsiniz. Daha fazla bilgi için bkz. [Özellik yönetimine genel bakış](/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Yeni bir müşteri İnsan Kaynakları için kaydolduğunda, bu abonelik bir uygulama projesi çalışma alanı içerir. Müşteri, hizmeti etkinleştirdikten sonra, kiracı yöneticisinin kiracı hesabını kullanarak <https://lcs.dynamics.com> adresinde oturum açması gerekir. Proje çalışma alanı, kuruluş için otomatik olarak oluşturulur. Daha fazla bilgi için bkz. [Finans ve Operasyon uygulamaları müşterileri için Lifecycle Services (LCS)](/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs).

> [!NOTE]
> Sağlamanın başarılı olmasını sağlamak amacıyla, İnsan Kaynakları ortamını sağlamak için kullandığınız hesap, İnsan kaynakları ortamıyla ilişkilendirilmiş Power Apps ortamındaki **Sistem Yöneticisi** rolü veya **Sistem Özelleştirici** rolüne atanmalıdır. Microsoft Power Platform'da kullanıcılara güvenlik rollerinin nasıl atanacağı hakkında daha fazla bilgi için bkz. [Kaynaklara kullanıcı güvenliği yapılandırma](/power-platform/admin/database-security).

Ortamları dağıtmaya başlamadan önce LCS proje ekleme işlemini tamamlamanız gerekir. Daha fazla bilgi için bkz. [Proje ekleme](/fin-ops-core/dev-itpro/lifecycle-services/project-onboarding). LCS 'yi kullanma hakkında daha fazla bilgi için bkz. [Lifecycle Services (LCS) kullanıcı kılavuzu](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide).

## <a name="deploy-human-resources-environments"></a>Human Resources ortamlarını dağıtma

İnsan Kaynakları de dahil olmak üzere finans ve operasyon uygulamalarının bulut içinde dağıtımı, dağıtım yaptığınız ortamı ve aboneliği, hangi görevlerin kimin gerçekleştirebileceğini ve hangi verileri ve özelleştirmeleri yönetmeniz gerektiğini anlamanıza gerek duyar. Yeni ortamları dağıtırken adlandırılmış bir kullanıcı yerine bir hizmet hesabı kullanmanızı öneririz. Finans ve operasyon altyapısında ortam dağıtma hakkında daha fazla bilgi için bkz. [Bulut dağıtımına genel bakış](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Finans ve operasyon altyapısında İnsan Kaynakları için bir üretim ortamı dağıtmak için kullanıma almaya hazırlık sürecini tamamlamanız gerekir. Daha fazla bilgi için bkz. [Kullanıma alma için hazırlık](/fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live). Bu işlem LCS'deki abonelik tahmin aracını içerir. Daha fazla bilgi için bkz. [Abonelik tahmin aracı](/fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Human Resources ile Microsoft Power Platform tümleştirme

Microsoft Power Platform, Power Platform yönetici merkezi yoluyla Dynamics 365 uygulamaları için bir yetenek seti sağlar. Human Resources veri kullanımını, Microsoft Power Platform'u kullanarak tümleştirebilir ve genişletebilirsiniz. Microsoft Power Platform ile Human Resources'ı tümleştirme hakkında daha fazla bilgi için bkz. [Finans ve Operasyon uygulamaları ile Microsoft Power Platform tümleştirme](/fin-ops-core/dev-itpro/power-platform/overview).

## <a name="supported-geographies"></a>Desteklenen coğrafyalar

Human Resources için desteklenen diller ve coğrafyalar hakkında bilgi için bkz. [Tasarım gereği global: desteklenen ülke/bölge ve diller hakkında bilgi edinin](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Ortama erişim izni verme

Varsayılan olarak, ortamı oluşturan genel yöneticinin ortama erişimi vardır. Ek uygulama kullanıcılarına erişim izninin açıkça verilmesi gerekir. Human Resources ortamında kullanıcılar eklemeniz ve kullanıcılara uygun roller atamanız gerekir. Daha fazla bilgi için bkz. [Yeni kullanıcılar oluşturmak](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) ve [Kullanıcıları güvenlik rollerine atamak](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Ek kaynaklar
Aşağıdaki kaynakları kullanarak, finans ve operasyon uygulama altyapısında LCS içindeki projelerin nasıl kullanılacağı ve yönetileceği hakkında daha fazla bilgi edinebilirsiniz:

- [Lifecycle Services kaynakları](/fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Lifecycle Services (LCS) kullanıcı kılavuzu](/fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Self servis dağıtıma genel bakış](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Veritabanı taşıma işlemleri ana sayfası](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
