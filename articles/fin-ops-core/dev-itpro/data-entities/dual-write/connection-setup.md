---
title: Çift yazma kurulumu kılavuzu
description: Bu makalede, çift yazma kurulumu için desteklenen senaryolar açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a0d1b4e1f093874a8fd37cf7aadb331cd1e7adc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873163"
---
# <a name="guidance-for-dual-write-setup"></a>Çift yazma kurulumu kılavuzu

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Finans ve Operasyon ortamı ve Dataverse ortamı arasında çift yazma bağlantısı ayarlayabilirsiniz.

+ **Finance and Operations ortamı**, **Finans ve Operasyon uygulamaları** (ör. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ve Dynamics 365 Human Resources) için temel platformu sağlar.
+ **Dataverse ortamı**, **müşteri etkileşimi uygulamaları** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing ve Dynamics 365 Project Service Automation) için temel platformu sağlar.

> [!IMPORTANT]
> Dynamics 365 Finance'teki Human Resources modülü, çift yazma bağlantılarını desteklerken Dynamics 365 Human Resources uygulaması desteklemez.

Kurulum mekanizması aboneliğinize ve ortamınıza göre değişir:

+ Finans ve Operasyon uygulamaların yeni kurulumları için, çift yazma bağlantısı kurulumu Microsoft Dynamics Lifecycle Services'ta (LCS) başlar. Microsoft Power Platform lisansına sahipseniz, kiracınızın ortamı yoksa yeni bir Dataverse ortamı alırsınız.
+ Finans ve Operasyon uygulamaların mevcut kurulumları için,çift yazma bağlantısı kurulumu Finans ve Operasyon ortamında başlar.

Bir varlıkta çift yazmaya başlamadan önce, hem Finans ve Operasyon uygulamalarında hem de müşteri etkileşimi uygulamalarında varolan verileri işlemek için bir ilk eşitleme çalıştırabilirsiniz. İki ortam arasında veri eşitlemeniz gerekmiyorsa ilk eşitlemeyi atlayabilirsiniz.

İlk eşitleme, mevcut verileri bir uygulamadan diğerine çift yönlü olarak kopyalamanızı sağlar. Sahip olduğunuz ortamlara ve ortamlardaki veri türüne bağlı olarak birçok farklı kurulum senaryosu mevcuttur.

Aşağıdaki kurulum senaryoları desteklenir:

+ [Yeni Finans ve Operasyon uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#new-new)
+ [Yeni Finans ve Operasyon uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#new-existing)
+ [Veri içeren yeni Finans ve Operasyon uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#new-data-new)
+ [Veri içeren yeni Finans ve Operasyon uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#new-data-existing)
+ [Mevcut Finans ve Operasyon uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#existing-new)
+ [Mevcut Finans ve Operasyon uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Yeni Finans ve Operasyon uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu

Veri içermeyen yeni bir Finans ve Operasyon uygulaması kurulumu ile müşteri etkileşimi uygulamasının yeni bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin. Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:

- Yeni, boş bir Finans ve Operasyon ortamı sağlanır.
- CRM ana çözümünün yüklendiği, müşteri etkileşimi uygulamasının yeni ve boş bir kurulumu sağlanır.
- DAT şirket verileri içinçift yazma bağlantısı kurulur.
- Tablo eşlemeleri canlı eşitleme için etkinleştirilir.

Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Yeni Finans ve Operasyon uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu

Veri içermeyen yeni bir Finans ve Operasyon uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin. Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:

- Yeni, boş bir Finans ve Operasyon ortamı sağlanır.
- DAT şirket verileri içinçift yazma bağlantısı kurulur.
- Tablo eşlemeleri canlı eşitleme için etkinleştirilir.

Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.

Mevcut Dataverse verilerini Finans ve Operasyon uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Finans ve Operasyon uygulamasında yeni bir şirket oluşturun.
2. Şirketi çift yazma bağlantı kurulumuna ekleyin.
3. Üç harfli Uluslararası Standartlaştırma Kuruluşu (ISO) şirket kodunu kullanarak Dataverse verilerini [önyükleyin](bootstrap-company-data.md).
4. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için bu makalenin ilerleyen kısımlarındaki [Örnek](#example) bölümüne bakın.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Veri içeren yeni Finans ve Operasyon uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu

Verilere sahip yeni bir Finans ve Operasyon uygulaması kurulumu ile müşteri etkileşimi uygulamasının yeni örneği arasında çift yazma bağlantısı kurmak için, bu makalenin önceki bölümlerinde yer alan [Yeni Finans ve Operasyon uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#new-new)'ndaki adımları uygulayın. Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.

1. Finans ve Operasyon uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.
2. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Veri içeren yeni Finans ve Operasyon uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu

Verilere sahip yeni bir Finans ve Operasyon uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut örneği arasında çift yazma bağlantısı kurmak için, bu makalenin önceki bölümlerinde yer alan [Yeni Finans ve Operasyon uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#new-existing)'ndaki adımları uygulayın. Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.

1. Finans ve Operasyon uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.
2. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Mevcut Dataverse verilerini Finans ve Operasyon uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.

1. Finans ve Operasyon uygulamasında yeni bir şirket oluşturun.
2. Şirketi çift yazma bağlantı kurulumuna ekleyin.
3. Üç harfli ISO şirket kodunu kullanarak Dataverse verilerini [önyükleyin](bootstrap-company-data.md).
4. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Mevcut Finans ve Operasyon uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu

Finans ve Operasyon uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının yeni kurulumu arasında çift yazma bağlantısı kurulumu Finans ve Operasyon ortamında gerçekleşir.

1. [Finans ve Operasyon uygulamasından bağlantıyı kurma](enable-dual-write.md).
2. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Mevcut Finans ve Operasyon uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu

Finans ve Operasyon uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının mevcut kurulumu arasında çift yazma bağlantısı kurulumu Finans ve Operasyon ortamında gerçekleşir.

1. [Finans ve Operasyon uygulamasından bağlantıyı kurma](enable-dual-write.md).
2. Mevcut Dataverse verilerini Finans ve Operasyon uygulamasıyla eşitlemek için üç harfli ISO şirket kodunu kullanarak Dataverse verilerini [önyükleyin](bootstrap-company-data.md).
3. Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.

Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.

## <a name="example"></a>Örnek

Örneğin, bkz. [Müşterileri Etkinleştirme V3 - İlgili kişiler tablo eşlemesi](enable-entity-map.md#enable-table-map)

İlk eşitlemeyi çalıştırması gereken her bir varlıktaki veri birimlerine dayalı alternatif bir yaklaşım için bkz. [İlk eşitleme için dikkat edilecek hususlar](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]