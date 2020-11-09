---
title: Çift yazmayı ayarlama kılavuzu
description: Bu konu, çift yazma kurulumu için desteklenen senaryoları açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088518"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a>Çift yazmayı ayarlama kılavuzu

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Finance and Operations ortamı ve Common Data Service ortamı arasında çift yazma bağlantısı ayarlayabilirsiniz.

+ **Finance and Operations ortamı** , **Finance and Operations uygulamalarının** (ör. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management ve Dynamics 365 Retail) temelindeki platformu sağlar.
+ **Common Data Service ortamı** **müşteri etkileşimi uygulamaları** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ve Dynamics 365 Project Service Automation) için temel alınan platformu sağlar.

>[!IMPORTANT]
>Finance and Operations'taki Human Resources, çift yazma bağlantılarını desteklerken Dynamics 365 Human Resources uygulaması desteklemez.

Kurulum mekanizması aboneliğinize ve ortamınıza göre değişir.

+ Finance and Operations uygulamaların yeni kurulumları için, çift yazma bağlantısı kurulumu Microsoft Dynamics Lifecycle Services'ta (LCS) ile başlar. Power Platform lisansına sahipseniz, kiracınızın ortamı yoksa yeni bir Common Data Service ortamı alırsınız.
+ Mevcut Finance and Operations kurulumları için, çift yazma bağlantısı kurulumu Finance and Operations ortamında başlar.

Bir varlıkta çift yazmaya başlamadan önce, Finance and Operations uygulamaların ve müşteri etkileşimi uygulamalarının her iki tarafında varolan verileri işlemek için bir başlangıç eşitlemesi çalıştırabilirsiniz. İki ortam arasında veri eşitlemeniz gerekmiyorsa, ilk eşitlemeyi atlayabilirsiniz.

İlk eşitleme, varolan verileri bir uygulamadan diğerine çift yönlü olarak kopyalamanızı sağlar. Sahip olduğunuz ortamlara ve ortamlardaki veri türüne bağlı olarak birçok farklı kurulum senaryosu vardır.

Aşağıdaki kurulum senaryoları desteklenir:

+ [Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#new-new)
+ [Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#new-existing)
+ [Verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#new-data-new)
+ [Verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#new-data-existing)
+ [Mevcut Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#existing-new)
+ [Mevcut Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu

Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının yeni bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin. Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:

- Yeni, boş bir Finance and Operations ortamı sağlanır.
- CRM ana çözümünün yüklendiği, müşteri etkileşimi uygulamasının yeni ve boş bir kurulumu sağlanır.
- DAT şirket verileri içinçift yazma bağlantısı kurulur.
- Varlık eşlemeleri canlı eşitleme için etkinleştirilir.

Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu

Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin. Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:

- Yeni, boş bir Finance and Operations ortamı sağlanır.
- DAT şirket verileri içinçift yazma bağlantısı kurulur.
- Varlık eşlemeleri canlı eşitleme için etkinleştirilir.

Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.

Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasında yeni bir şirket oluşturun.
2. Şirketi çift yazma bağlantı kurulumuna ekleyin.
3. Üç harfli Uluslararası Standartlaştırma Kuruluşu (ISO) şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).
4. Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu

Verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının yeni örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#new-new)'ndaki adımları uygulayın. Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma** 'ya gidin.
2. Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu

Verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#new-existing)'ndaki adımları uygulayın. Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma** 'ya gidin.
2. Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.

Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasında yeni bir şirket oluşturun.
2. Şirketi çift yazma bağlantı kurulumuna ekleyin.
3. Üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).
4. Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Mevcut Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu

Finance and Operations uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının yeni kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.

1. [Finance and Operations uygulamasından bağlantıyı ayarlayın](enable-dual-write.md).
2. Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Mevcut Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu

Finance and Operations uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının mevcut kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.

1. Finance and Operations uygulamasından bağlantıyı ayarlayın.
2. Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için, üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).
3. Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).

## <a name="example"></a>Örnek

Örneğin, bkz. [Müşterileri Etkinleştirme V3 — İlgili kişiler varlık haritası](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)

İlk eşitlemeyi çalıştırması gereken her bir varlıktaki veri birimlerine dayalı alternatif bir yaklaşım için, bkz. [İlk eşitleme için dikkat edilecek hususlar](initial-sync-guidance.md).
