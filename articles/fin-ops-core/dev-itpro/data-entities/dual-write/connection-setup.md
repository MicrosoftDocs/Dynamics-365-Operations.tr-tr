---
title: Çift yazma kurulumu kılavuzu
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
ms.openlocfilehash: 47c07dd0e2f311b61297340a48a5a31cb1de3903
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685677"
---
# <a name="guidance-for-dual-write-setup"></a>Çift yazma kurulumu kılavuzu

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finance and Operations ortamı ve Dataverse ortamı arasında çift yazma bağlantısı ayarlayabilirsiniz.

+ **Finance and Operations ortamı** **Finance and Operations uygulamaları** için temel alınan platformu sağlar (örneğin, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ve Dynamics 365 Human Resources).
+ **Dataverse ortamı** **müşteri etkileşimi uygulamaları** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ve Dynamics 365 Project Service Automation) için temel alınan platformu sağlar.

> [!IMPORTANT]
> Dynamics 365 Finance'teki Human Resources modülü, çift yazma bağlantılarını desteklerken Dynamics 365 Human Resources uygulaması desteklemez.

Kurulum mekanizması aboneliğinize ve ortamınıza göre değişir:

+ Finance and Operations uygulamaların yeni kurulumları için, çift yazma bağlantısı kurulumu Microsoft Dynamics Lifecycle Services'ta (LCS) ile başlar. Microsoft Power Platform lisansına sahipseniz, kiracınızın ortamı yoksa yeni bir Dataverse ortamı alırsınız.
+ Mevcut Finance and Operations kurulumları için, çift yazma bağlantısı kurulumu Finance and Operations ortamında başlar.

Bir varlıkta çift yazmaya başlamadan önce, hem Finance and Operations uygulamalarında hem de müşteri etkileşimi uygulamalarında varolan verileri işlemek için bir ilk eşitleme çalıştırabilirsiniz. İki ortam arasında veri eşitlemeniz gerekmiyorsa ilk eşitlemeyi atlayabilirsiniz.

İlk eşitleme, mevcut verileri bir uygulamadan diğerine çift yönlü olarak kopyalamanızı sağlar. Sahip olduğunuz ortamlara ve ortamlardaki veri türüne bağlı olarak birçok farklı kurulum senaryosu mevcuttur.

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
- Tablo eşlemeleri canlı eşitleme için etkinleştirilir.

Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu

Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin. Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:

- Yeni, boş bir Finance and Operations ortamı sağlanır.
- DAT şirket verileri içinçift yazma bağlantısı kurulur.
- Tablo eşlemeleri canlı eşitleme için etkinleştirilir.

Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.

Mevcut Dataverse verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasında yeni bir şirket oluşturun.
2. Şirketi çift yazma bağlantı kurulumuna ekleyin.
3. Üç harfli Uluslararası Standartlaştırma Kuruluşu (ISO) şirket kodunu kullanarak Dataverse verilerini [önyükleyin](bootstrap-company-data.md).
4. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için bu konunun ilerleyen kısımlarındaki [Örnek](#example) bölümüne bakın.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu

Verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının yeni örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#new-new)'ndaki adımları uygulayın. Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.
2. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu

Verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#new-existing)'ndaki adımları uygulayın. Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.
2. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Mevcut Dataverse verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Finance and Operations uygulamasında yeni bir şirket oluşturun.
2. Şirketi çift yazma bağlantı kurulumuna ekleyin.
3. Üç harfli ISO şirket kodunu kullanarak Dataverse verilerini [önyükleyin](bootstrap-company-data.md).
4. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Mevcut Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu

Finance and Operations uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının yeni kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.

1. [Finance and Operations uygulamasından bağlantıyı ayarlayın](enable-dual-write.md).
2. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Mevcut Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu

Finance and Operations uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının mevcut kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.

1. [Finance and Operations uygulamasından bağlantıyı ayarlayın](enable-dual-write.md).
2. Mevcut Dataverse verilerini Finance and Operations uygulamasıyla eşitlemek için, üç harfli ISO şirket kodunu kullanarak Dataverse verilerini [önyükleyin](bootstrap-company-data.md).
3. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.

## <a name="example"></a>Örnek

Örneğin, bkz. [Müşterileri Etkinleştirme V3 - İlgili kişiler tablo eşlemesi](enable-entity-map.md#enable-table-map)

İlk eşitlemeyi çalıştırması gereken her bir varlıktaki veri birimlerine dayalı alternatif bir yaklaşım için bkz. [İlk eşitleme için dikkat edilecek hususlar](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]