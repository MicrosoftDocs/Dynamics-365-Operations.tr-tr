---
title: Çift yazma kurulumu için desteklenen senaryolar
description: Bu konu, çift yazma kurulumu için desteklenen senaryoları açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d7ff514768ee8e4797b591da89e190a855385885
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172866"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Çift yazma kurulumu için desteklenen senaryolar

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Finance and Operations ortamı ve Common Data Service ortamı arasında çift yazma bağlantısı ayarlayabilirsiniz.

+ **Finance and Operations ortamı** **Finance and Operations uygulamaları** için temel alınan platformu sağlar (örneğin, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail ve Dynamics 365 Human Resources).
+ **Common Data Service ortamı** **Dynamics 365'teki model yönetimli uygulamalar** için temel alınan platformu sağlar (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ve Dynamics 365 Project Service Automation).

Kurulum mekanizması aboneliğinize ve ortamınıza göre değişir.

+ Finance and Operations uygulamaların yeni kurulumları için, çift yazma bağlantısı kurulumu Microsoft Dynamics Lifecycle Services'ta (LCS) ile başlar. Microsoft Power Platform lisansına sahipseniz, kiracınızın ortamı yoksa yeni bir Common Data Service ortamı alırsınız.
+ Mevcut Finance and Operations kurulumları için, çift yazma bağlantısı kurulumu Finance and Operations ortamında başlar.

Aşağıdaki kurulum senaryoları desteklenir:

+ [Yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu](#new-new)
+ [Yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu](#new-existing)
+ [Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu](#new-demo-new)
+ [Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu](#new-demo-existing)
+ [Mevcut Finance and Operations uygulaması kurulumu ve yeni veya mevcut model yönetimli uygulama kurulumu](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu

Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365'teki model yönetimli uygulamanın yeni bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin. Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:

- Yeni, boş bir Finance and Operations ortamı sağlanır.
- CRM ana çözümünün yüklendiği, model yönetimli uygulamanın yeni ve boş bir örneğini sağlanır.
- DAT şirket verileri içinçift yazma bağlantısı kurulur.
- Varlık eşlemeleri canlı eşitleme için etkinleştirilir.

Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu

Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365'teki model yönetimli uygulamanın mevcut bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin. Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:

- Yeni, boş bir Finance and Operations ortamı sağlanır.
- DAT şirket verileri içinçift yazma bağlantısı kurulur.
- Varlık eşlemeleri canlı eşitleme için etkinleştirilir.

Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.

Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasında yeni bir şirket oluşturun.
2. Şirketi çift yazma bağlantı kurulumuna ekleyin.
3. Üç harfli Uluslararası Standartlaştırma Kuruluşu (ISO) şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).

Çift yazma canlı eşitleme modunda olduğundan, Common Data Service'taki veriler otomatik olarak Finance and Operations uygulamasına akmaya başlar.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu

Demo verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365 model yönetimli uygulamanın yeni örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu](#new-new)'ndaki adımları uygulayın. Bağlantı kurulumu tamamlandığında, demo verilerini model yönetimli uygulamayla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.
2. Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu

Demo verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365 model yönetimli uygulamanın mevcut örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu](#new-existing)'ndaki adımları uygulayın. Bağlantı kurulumu tamamlandığında, demo verilerini model yönetimli uygulamayla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.
2. Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.

Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasında yeni bir şirket oluşturun.
2. Şirketi çift yazma bağlantı kurulumuna ekleyin.
3. Üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).

Çift yazma canlı eşitleme modunda olduğundan, Common Data Service'taki veriler otomatik olarak Finance and Operations uygulamasına akmaya başlar.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Mevcut Finance and Operations uygulaması kurulumu ve yeni veya mevcut model yönetimli uygulama kurulumu

Finance and Operations uygulamasının mevcut kurulumu ile Dynamics 365 model yönetimli uygulamasının yeni veya mevcut kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.

1. Finance and Operations uygulamasından bağlantıyı ayarlayın.
2. Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için, üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).

Çift yazma canlı eşitleme modunda olduğundan, Common Data Service'taki veriler otomatik olarak Finance and Operations uygulamasına akmaya başlar.
