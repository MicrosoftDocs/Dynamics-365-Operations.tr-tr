---
title: Dağıtılmış karma topolojideki ölçek birimlerini deneme
description: Bu makale, üretim ve ambar yönetimi iş yükleri için bulut ve uç ölçek birimlerini deneme hakkında bilgi sağlar.
author: perlynne
ms.date: 05/02/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 5645955109e7a942e617b3b90a27065c2a8fe4a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893598"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Dağıtılmış karma topolojideki ölçek birimlerini deneme

[!include [banner](../includes/banner.md)]

Dağıtılmış karma topolojiyi deneme işlemi kolaydır. İlk aşamada, dağıtılmış topolojide çalıştıklarından emin olmak için özelleştirmeleri doğrulamanız gerekir. İki seçeneğiniz vardır.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>Seçenek 1: Özelleştirmeleri, yerleşik geliştirme ortamlarında değerlendirme

Korumalı alanınızı eklemeye başlamadan önce işlemleri, özelleştirmeleri ve çözümleri doğrulayabilmeniz için yerleşik ortam (katman 1 ortam olarak da bilinir) gibi bir geliştirme kurulumunda ölçek birimlerini keşfetmenizi öneririz. Bu aşamada, veriler ve özelleştirmeler yerleşik ortamlara uygulanacaktır. Hem kuruluş hub'ı hem de ölçek birimi rolünü ele alan tek bir ortamda çalıştırabilirsiniz. Alternatif olarak, biri hub'ın ve diğerinin rolünü alan bir ölçeklendirme birimi rolü alan iki geliştirme ortamına sahip olabilirsiniz. Bu kurulum, sorunları tanımlamanın ve düzeltmenin en iyi yolunu sağlar. En son [Önizleme derlemesi](../../fin-ops-core/fin-ops/get-started/one-version.md#how-can-i-get-early-access-to-non-released-platform-updates) de bu aşamayı tamamlamak için kullanılabilir.

Ortamları kurmak ve korumak için [yerleşik geliştirme ortamları için ölçek birimi dağıtım araçlarını kullanmanız](https://github.com/microsoft/SCMScaleUnitDevTools) gerekir. Bu araçlar, merkez ve ölçek birimlerini bir veya iki yerleşik ortamda yapılandırmanıza olanak tanır. Araçlar GitHub'da kaynak kodunda ve ikili sürüm olarak sağlanır. Araçların nasıl kullanıldığını açıklayan [Adım adım kullanım kılavuz](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) içeren proje wiki'sini inceleyin. [Yerel iş verilerini (LBD) kullanarak özel donanımda kenar ölçek birimleri dağıtıyorsanız](cloud-edge-edge-scale-units-lbd.md), farklı bir işlem izlemeniz gerekir.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>Seçenek 2: Eklentiler alıp korumalı alan ortamlarınıza dağıtın

Dağıtılmış karma topolojisini denemek için, biri verilerinizi (kurumsal hub) içeren, diğeri ise ölçek birimi olan ve "boş veri" içeren iki sanal alan ortamınız (katman 2) olmalıdır.

En az bir bulut veya kenar ölçek birimi için eklenti edinmeniz gerekir. İlgili proje ve ortam yuvaları, [Microsoft Dynamics Lifecycle Services'de (LCS)](https://lcs.dynamics.com/) verilir, böylece ölçek birimi ortamları [Ölçek Birim Yöneticisi](https://aka.ms/SCMSUM) portalı kullanılarak dağıtılabilir.

Korumalı alan ortamlarının etkinleştirilmesini istemek için Microsoft desteke başvurun.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
