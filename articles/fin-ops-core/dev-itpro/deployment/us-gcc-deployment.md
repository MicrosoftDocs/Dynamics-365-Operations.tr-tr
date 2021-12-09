---
title: ABD Hükümeti Topluluk Bulutunda (GCC) Dynamics 365 Finance ve Dynamics 365 Supply Chain Management
description: Bu konu, uygun kamu sektörü ve özel varlıklar tarafından kullanılabilen Microsoft Dynamics 365 US Government ürünleri hakkında bilgi sağlar.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 17702ada5bf75a44652e194c2555a83e76e7a36b
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817452"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>ABD Hükümeti Topluluk Bulutunda (GCC) Dynamics 365 Finance ve Dynamics 365 Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Seçili Microsoft Dynamics 365 Amerika Birleşik Devletleri (ABD) Hükümeti ürünleri, onaylı kamu sektörü ve özel varlıklar tarafından kullanılabilir. Bu varlıklar, aşağıdaki türlerle sınırlıdır:

- ABD Federal, eyalet, yerel, kabile ve bölge hükümeti varlıkları
- Kamu varlıklarına veya bulut topluluğunun uygun üyelerine çözüm sağlamak için Dynamics 365 US Government kullanan özel varlıklar
- Kamu düzenlemelerine tabi müşteri verileri bulunan özel varlıklar ve Dynamics 365 US Government, yasal gereksinimleri karşılamak için uygun hizmettir

Bilgi için bkz. [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Onboarding

Microsoft Dynamics Lifecycle Services (LCS) içindeki uygulama projesi için ilk ekleme işlemini tamamlamak üzere, [Uygulama projesine ekleme](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md) bölümündeki talimatları izleyin. Ancak, bu yönergelerde sağlanan genel LCS bağlantısını kullanmayın. Bunun yerine, ABD Hükümeti Topluluk Bulutu (GCC) için LCS'yi açmak üzere aşağıdaki URL'yi kullanın: <https://gov.lcs.microsoftdynamics.us>.

İlk ekleme işlemi tamamlandıktan sonra, [Proje ekleme](../lifecycle-services/project-onboarding.md)'deki yönergeleri izleyin. Yine genel LCS yerine [GCC için LCS](https://gov.lcs.microsoftdynamics.us) kullanın.

## <a name="environment-deployment"></a>Ortam dağıtımı

Proje ekleme işlemi tamamlandıktan sonra, [Finance and Operations uygulaması müşterileri için Lifecycle Services'de (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md) açıklanan LCS'nin ek yeteneklerini gözden geçirebilirsiniz. Sonra ortam dağıtımına geçin.

- Microsoft tarafından yönetilen ortamları LCS aracılığıyla dağıtmak için, [Finance and Operations uygulaması müşterileri için Lifecycle Services'eki (LCS)](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience) yönergeleri izleyin.
- Bulutta barındırılan ortamlar için bkz. [Dağıtım ve erişim geliştirme ortamları](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). [ABD hükümeti Lifecycle Services projeleri için Azure Resource Manager ekleme işlemini tamamlama](arm-onbarding-us-goverment.md) bölümünde açıklandığı gibi, bağlayıcılarınız için Kaynak Yöneticisi ekleme işlemini tamamlamanız da gerekir.

> [!NOTE]
> ABD hükümeti LCS projeleri için yalnızca Azure Kamuya özel Azure abonelikleri desteklenir.

## <a name="features-that-arent-available"></a>Kullanılamayan özellikler

Bazı özellikler GCC'de dağıtım için kullanılamaz veya GCC'de Dynamics 365 ile kullanılmak için kullanılamaz. Örneğin, Azure DevOps Hizmetleri GCC'de kullanılamaz. Ancak, şirket içi Azure DevOps veya ortak Azure DevOps servisleri kullanılabilir. Özellik kullanılabilirliği hakkında ayrıntılı bilgi için, bkz. [Business Applications ABD Hükümeti Özellik Kullanılabilirliği](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Dynamics 365 Finance ve Dynamics 365 Supply Chain Management GCC Yüksekte desteklenir mi?

Hayır. Dynamics 365 Finance ve Dynamics 365 Supply Chain Management, yalnızca GCC'de desteklenir.

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>GCC'de, Finans ve Supply Chain Management ile ortak Azure DevOps kullanabilir miyim?

Evet, Federal Risk and Authorization Management Program (FEDRAMPA) onaylı bir çözüm için gerekli izinleriniz yoksa ortak Azure DevOps hizmetlerini kullanabilirsiniz. Alternatif olarak, Azure DevOps Sunucu da kullanabilirsiniz.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Bulut tarafından barındırılan ortam Katman 1 geliştirme ortamını, Azure Commercial aboneliğine dağıtabilir miyim?

Hayır. [GCC için LCS](https://gov.lcs.microsoftdynamics.us)'de, bulut tarafından barındırılan bir ortam dağıtmak için bir Azure Kamu aboneliği kullanmanız gerekir.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Paylaşılan varlık kitaplığından bir pakete gereksinim duyuyorsam ancak GCC için LCS içinde kullanılamıyorsa ne yapabilirim?

Aynı paketi, [ortak LCS](https://lcs.dynamics.com) içindeki paylaşılan varlık kitaplığından indirebilirsiniz. Alternatif olarak, ortağınız paketi karşıdan yüklemeye yardımcı olabilir.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Kod yükseltme aracı GCC'de kullanılabilir mi?

Hayır, kod yükseltme aracı şu anda GCC'de kullanılabilir durumda değil. Ancak, [genel LCS](https://lcs.dynamics.com) içinde aday müşteri projesi oluşturabilir ve kod yükseltme aracını kullanabilirsiniz. Aday müşteri projelerindeki ortamları dağıtamayacağınızı unutmayın.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Ortak, benim adıma bir destek bileti açabilir mi?

Evet. Ancak, ortağınız GCC olmayan bir kimlik kullanıyorsa, destek bileti ortak destek kuyruğuna yönlendirilir. Destek biletlerini açmak için LCS içindeki müşteri GCC hak edişlerini kullanmanızı öneririz.

## <a name="see-also"></a>Ayrıca bkz.

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Business Applications ABD Hükümeti Özellik Kullanılabilirliği](https://aka.ms/BAPFunctionalParity).
- [Lifecycle Services (LCS) kullanıcı kılavuzu](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Bulut dağıtımına genel bakış](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
