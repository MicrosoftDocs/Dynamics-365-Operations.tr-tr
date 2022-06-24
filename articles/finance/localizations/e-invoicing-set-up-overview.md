---
title: Elektronik faturalama kurulumu
description: Bu makalede, Elektronik faturalama kurulumu ve yapılandırma işlemine dair genel bir bakış sağlanmaktadır.
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
ms.openlocfilehash: 8e2aa89119530a0ba00a8561d94006285d67a71b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883133"
---
# <a name="electronic-invoicing-setup"></a>Elektronik faturalama kurulumu

[!include [banner](../includes/banner.md)]

Makalede, Elektronik faturalama kurulumu ve yapılandırma işlemine dair genel bir bakış sağlanmaktadır. Kurulum adımlarını burada belirtilen sırayla tamamlamanız gerekir. Bir adım zorunluysa ancak bunu atlarsanız, işlevler doğru çalışmaz ve sonraki adımlar sırasında veya işlevselliği kullandığınızda birden çok hata oluşacaktır. 

Başlamadan önce tüm ana bileşenlerin doğru şekilde kurulduğundan, Regulatory Configuration Service'e (RCS) kayıt olduğunuzdan ve bir RCS örneğiniz olduğundan, ve Elektronik faturalama eklentinizin Microsoft Dynamics 365 Finance veya Dynamics 365 Supply Chain Management ortamınızda kurulu olduğundan emin olun. Daha fazla bilgi için bkz. [Elektronik faturalamaya kaydolma ve kurma](e-invoicing-install-add-in-microservices-lcs.md).

Sonra, Elektronik faturalamanın işini yapmak için gerek duyduğu Azure kaynaklarını ayarlayın. Daha fazla bilgi için bkz. [Elektronik faturalama için Azure kaynaklarını ayarlama](e-invoicing-set-up-azure-resources.md).

Ana bileşenler konfigüre ettikten sonra, Elektronik faturalamanın ana mantıksal bileşenlerini ayarlamak için RCS ile çalışın. Önce, koruyacağınız servis ortamının sayısını tanımlayın. Bu şekilde, geliştirme veya test ortamı ile üretim ortamları arasında bir sınıra sahip olduğunuzdan emin olmak için mantıksal verileri ve konfigürasyon bölümlemeyi tanımlarsınız. Geliştirme sürecinizi esnek bir yolla ayarlamak için, birkaç ayrı geliştirme ve test ortamı gerekebilir. Servis ortamları tanımlamaya ek olarak, Elektronik faturalama ile doğru bir işlem için gereken parametreleri ayarlamak üzere, Finance veya Supply Chain Management gibi iş uygulamalarınız için doğrudan RCS'den bir bağlantı ayarlayın. Ortamlar hakkında daha fazla bilgi için [Hizmet ortamları](e-invoicing-service-environments.md) konusuna bakın.

Her şey oluşturulduktan sonra, elektronik belgeleri işlemek ve verileri dönüştürmek veya Genel depodan belge almak için farklı senaryoları tanımlayan kendi Genelleştirme özelliklerinizi oluşturabilirsiniz. Genelleştirme özellikleri ile nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [Genelleştirme özellikleriyle çalışma](e-invoicing-working-globalization-features.md).

Senaryolarınızı, gelen elektronik belgeleri işlemek için e-posta veya SharePoint ile tümleştirmek gerekiyorsa, bu kanalların nasıl ayarlanacağı ve kullanılacağı hakkında bilgi için bu kanalları kurma ve kullanma hakkında bilgi sağlayan [Gelen elektronik belgeleri işleme](e-invoicing-process-incoming-electronic-documents.md) konusuna bakın.
