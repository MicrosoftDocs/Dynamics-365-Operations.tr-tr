---
title: Elektronik faturalama kurulumu
description: Bu konu, Elektronik faturalama kurulumu ve konfigüre etme işlemine genel bakış sağlar.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8138c63e9eff1d2ca934f9d4467e4e3b73dae941
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371775"
---
# <a name="electronic-invoicing-setup"></a>Elektronik faturalama kurulumu

[!include [banner](../includes/banner.md)]

Konu, Elektronik faturalama kurulumu ve konfigüre etme işlemine genel bakış sağlar. Kurulum adımlarını burada belirtilen sırayla tamamlamanız gerekir. Bir adım zorunluysa ancak bunu atlarsanız, işlevler doğru çalışmaz ve sonraki adımlar sırasında veya işlevselliği kullandığınızda birden çok hata oluşacaktır. 

Başlamadan önce tüm ana bileşenlerin doğru şekilde kurulduğundan, Regulatory Configuration Service'e (RCS) kayıt olduğunuzdan ve bir RCS örneğiniz olduğundan, ve Elektronik faturalama eklentinizin Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management ortamınızda kurulu olduğundan emin olun. Daha fazla bilgi için bkz. [Elektronik faturalamaya kaydolma ve kurma](e-invoicing-install-add-in-microservices-lcs.md).

Sonra, Elektronik faturalamanın işini yapmak için gerek duyduğu Azure kaynaklarını ayarlayın. Daha fazla bilgi için bkz. [Elektronik faturalama için Azure kaynaklarını ayarlama](e-invoicing-set-up-azure-resources.md).

Ana bileşenler konfigüre ettikten sonra, Elektronik faturalamanın ana mantıksal bileşenlerini ayarlamak için RCS ile çalışın. Önce, koruyacağınız servis ortamının sayısını tanımlayın. Bu şekilde, geliştirme veya test ortamı ile üretim ortamları arasında bir sınıra sahip olduğunuzdan emin olmak için mantıksal verileri ve konfigürasyon bölümlemeyi tanımlarsınız. Geliştirme sürecinizi esnek bir yolla ayarlamak için, birkaç ayrı geliştirme ve test ortamı gerekebilir. Servis ortamları tanımlamaya ek olarak, Elektronik faturalama ile doğru bir işlem için gereken parametreleri ayarlamak üzere, Finance veya Supply Chain Management gibi iş uygulamalarınız için doğrudan RCS'den bir bağlantı ayarlayın. Ortamlar hakkında daha fazla bilgi için [Hizmet ortamları](e-invoicing-service-environments.md) konusuna bakın.

Her şey oluşturulduktan sonra, elektronik belgeleri işlemek ve verileri dönüştürmek veya Genel depodan belge almak için farklı senaryoları tanımlayan kendi Genelleştirme özelliklerinizi oluşturabilirsiniz. Genelleştirme özellikleri ile nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Genelleştirme özellikleriyle çalışma](e-invoicing-working-globalization-features.md).

Genelleştirme özelliklerinde derlenecek işlemi oluşturan işlem ardışık düzeninde eylemler hakkında bilgi için bkz. **[COMPLETE!: Belge işleme eylemleri]**.

Senaryolarınızı, gelen elektronik belgeleri işlemek için e-posta veya SharePoint ile tümleştirmek gerekiyorsa, bu kanalların nasıl ayarlanacağı ve kullanılacağı hakkında bilgi için bu kanalları kurma ve kullanma hakkında bilgi sağlayan [Gelen elektronik belgeleri işleme](e-invoicing-process-incoming-electronic-documents.md) konusuna bakın.
