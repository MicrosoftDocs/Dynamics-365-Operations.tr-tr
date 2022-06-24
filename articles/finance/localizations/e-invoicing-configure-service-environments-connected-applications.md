---
title: Servis ortamlarını ve bağlı uygulamaları yapılandırma
description: Bu makalede, servis ortamlarınızın ve bağlı uygulamalarınızın nasıl yapılandırılacağı hakkında bilgiler sağlanmaktadır.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c1bb3f784148f04c01223ac4e280a18bacfe0e51
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853236"
---
# <a name="configure-service-environments-and-connected-applications"></a>Servis ortamlarını ve bağlı uygulamaları yapılandırma

[!include [banner](../includes/banner.md)]

Bu makalede, servis ortamlarınızın ve bağlı uygulamalarınızın nasıl yapılandırılacağı hakkında bilgiler sağlanmaktadır. Bu işlem için üç adım vardır. 1. adım zorunludur, 2. ve 3. adımlar isteğe bağlıdır.

## <a name="step-1-create-a-service-environment"></a>Adım 1: Hizmet ortamı oluşturma

Servis ortamınızı oluştururken, kendisine Genelleştirme özellikleri dağıtabilecek kullanıcıların listesini tanımlayın. İsteğe bağlı olarak, bazı senaryolarda Elektronik Faturalama hizmetiyle iletişim kurabilen harici uygulamaların listesini tanımlayın. Senaryolarınız içinde kullanacağınız numara serilerini ayarlayın.

Bu adımı tamamlamak için [Servis ortamları](e-invoicing-service-environments.md)'na bakın.

## <a name="step-2-add-certificates-and-secrets"></a>Adım 2: Sertifikaları ve parolaları ekleme

Microsoft Azure Key Vault'a bir referans ve bunları senaryolarınızda kullanmak için gizli diziler ekleyin. Bu adım, işlem ardışık düzeninde eylemler, dijital imzalama veya harici web hizmetleriyle iletişim için sertifika ve gizli kod kullanımı açısından zorunludur.

Bu adımı tamamlamak için [Müşteri sertifikaları ve gizli dizileri](e-invoicing-customer-certificates-secrets.md) konusuna bakın.

## <a name="step-3-configure-connected-applications"></a>Adım 3: Bağlı uygulamaları yapılandırın

Dynamics 365 Finance veya Dynamics 365 Supply Chain Management uygulamalarla elektronik faturalama arasında iletişim kurmak için Elektronik Faturalama hizmetine çağrı oluşturmak ve iş verilerini gerekli elektronik biçime dönüştürülebilecek birleşik bir yapıda hazırlamak üzere Finance veya Supply Chain Management'ı yapılandırmalısınız. Ayrıca uygulamalar, hizmetin yanıtlarını aynı zamanda doğru şekilde işlemelidir. Bu konfigürasyonu doğrudan Finance veya Supply Chain Management ortamınızda tamamlayabilirsiniz veya Regulatory Configuration Service'de (RCS) tamamlayabilirsiniz. Konfigürasyonu RCS'de tamamındaysanız, daha sonra Finance veya Supply Chain Management ortamınıza dağıtabilirsiniz. Bu adımda, parametre dağıtımı için bağlı uygulamayı kaydedilecektir.

Bu adımı tamamlamak için [Bağlı uygulamalar](e-invoicing-connected-applications.md)'a bakın.
