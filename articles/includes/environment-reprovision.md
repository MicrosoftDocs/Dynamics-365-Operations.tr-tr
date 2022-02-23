---
ms.openlocfilehash: f6bf4b6c946ebc63d3d84140f762cd4b789deb03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460096"
---
Bir veritabanını ortamlar arasında kopyalarken, tüm Commerce bileşenlerinin güncel olmasını sağlamak için kopyalanan veritabanının tamamen işlevsel olması amacıyla ortam yeniden sağlama aracını çalıştırmanız gerekir.

> [!IMPORTANT]
> Commerce işlevselliği tüm ortamlarda bulunduğundan, Commerce bileşenlerini kullanıyor olsanız ya da olmasanız da bu yordamı çalıştırmanızı öneririz. 

Devam etmeden önce, aşağıdaki önkoşulların karşılandığından emin olmanız gerekir:
1. Temmuz 2017 (7.2 olarak da bilinir) 7.2.11792.56024 sürümüne yükseltiyorsanız, ortamda veri yükseltmesini çalıştırmadan önce hedef ortamda aşağıdaki uygulama X++ düzeltmelerini uygulayın. Bunlar veri yükseltme sırasında oluşan çeşitli hataları engeller:

    - KB 4036156 - Retail küçük sürüm yükseltmesi - 'Ürün çeşidi numara serisi ayarlanmadı.' Bu düzeltme paketi ayrıca KB 4035399 ve KB 4035751'i içerir. Bu paketi kullanabilmeniz için en az Platform Update 9'a sahip olmanız gerekir. Emin değilseniz, en son ikili dosyaları yükleyin.
    
2. Microsoft DynamicsAX 2012'den yükseltiyorsanız, veri yükseltmesini çalıştırmadan önce hedef ortamda aşağıdaki uygulama X++ düzeltmelerini yükleyin:
    - KB 4033183 - Dynamics AX 2012 R2 veya Dynamics AX 2012 R3 Pre-CU8 perakende dışı yükseltme dbo.RETAILTILLLAYOUTZONE için nesne bulunamadı hatasıyla başarısız oldu.
    - KB 4040692 - Dynamics AX 2012 R3'ten Microsoft Dynamics 365 for Operations 7.2'ye yükseltme SalesLineIdx üzerine RetailSalesLine yinelenen dizini nedeniyle başarısız oldu.
    - KB 4035490 - GeneralJournalAccountEntry MainAccount alanı yükseltme koduyla ilgili performans sorunu.


Ortam yeniden sağlama aracını çalıştırmak için bu adımları izleyin.

1. Paylaşılan varlık kitaplığında **Yazılım dağıtılabilir paketi**'ni seçin.
2. Ortam yeniden sağlama aracını indirin.
3. Projenize ilişkin varlık kitaplığında **Yazılım dağıtılabilir paketi**'ni seçin.
4. Yeni bir ana paket oluşturmak için **Yeni**'yi seçin.
5. Paket için bir ad ve açıklama girin. Paket adı olarak **Ortam yeniden sağlama aracı**'nı kullanabilirsiniz.
6. Daha önce indirdiğiniz paketi yükleyin.
7. Hedef ortamınızın **Ortam ayrıntıları** sayfasında **Koru** > **Güncelleştirmeleri uygula**'yı seçin.
8. Daha önce yüklediğiniz Ortam yeniden sağlama aracını ve ardından paketi uygulamak için **Uygula**'yı seçin.
9. Paket dağıtımı ilerlemesini izleyin. 

Dağıtılabilir paket uygulama hakkında daha fazla bilgi edinmek için bkz. [Dağıtılabilir paket uygulama](../deployment/create-apply-deployable-package.md). Dağıtılabilir paketi el ile uygulama hakkında daha fazla bilgi edinmek için bkz. [Dağıtılabilir paket yükleme](../deployment/install-deployable-package.md).
