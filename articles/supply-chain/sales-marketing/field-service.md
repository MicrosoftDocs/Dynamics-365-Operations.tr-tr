---
title: Microsoft Dynamics 365 Field Service ile tümleştirmeye genel bakış
description: Bu konu Microsoft Dynamics 365 Field Service ile tümleştirme hakkında bilgi sağlar.
author: ChristianRytt
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 18eef310470cafd9d59bb1c848bbaeb8bf5b9fa1
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528911"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Microsoft Dynamics 365 Field Service ile tümleştirmeye genel bakış

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Supply Chain Management, Dynamics 365 Supply Chain Management ile Dynamics 365 Field Service arasında iş süreçlerinin eşitlenmesini sağlar Tümleştirme senaryoları iş süreçlerinin eşitlenmesine olanak tanımak için genişletilebilir Veri tümleştirici şablonları ve Common Data Service kullanılarak yapılandırılır.
Standart şablonlar özel tümleştirme projeleri oluşturmak için kullanılabilir; bu projelerde ek standart ve özel alanlar ve varlıklar tümleştirmeyi ayarlamak ve özel iş ihtiyaçlarını karşılamak üzere eşlenebilir. 

Field Service tümleştirmesi, mevcut aday-nakit işlevinin üzerine inşa olur.

![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/field-service-integration.png)

Field Service ile Supply Chain Management arasındaki tümleştirmenin birinci aşaması Field Service'taki iş emirlerinin ve sözleşmelerin Supply Chain Management'da faturalandırılmasını sağlamaya odaklanır. Desteklenen akış Field Service'da başlar; iş emirlerinden alınan bilgiler Supply Chain Management'a satış siparişleri olarak eşitlenir. Supply Chain Management'ta, satış siparişleri fatura belgeleri oluşturmak için faturalandırılır. Ayrıca, Field Service sözleşme faturalarındaki bilgiler Supply Chain Management'a eşitlenir. Microsoft Dynamics 365 Veri tümleştirici verileri özelleştirilebilir projeleri kullanarak eşitler. Standart şablonlar özel tümleştirme projeleri oluşturmak için kullanılabilir; bu projelerde ek standart ve özel alanlar ve varlıklar tümleştirmeyi ayarlamak ve özel gereksinimleri karşılamak üzere eşlenebilir.

Field Service ile Supply Chain Management arasındaki tümleştirmenin birinci aşaması aşağıdaki öğelerin eşitlenmesini sağlar:

- [Supply Chain Management'taki ürünleri Field Service'taki ürünlerle eşitleme](field-service-product.md)
- [Field Service'daki iş emirlerini Supply Chain Management'taki satış siparişleriyle eşitleme](field-service-work-order.md)
- [Field Service'daki sözleşme faturalarını Supply Chain Management'daki serbest metin faturalarıyla eşitleme](field-service-invoice.md)

Bir iş emrini Field Service ile Supply Chain Management arasında nasıl eşitleyeceğinize ilişkin bir örnek görmek için kısa YouTube videosunu izleyin: [İş emrini Microsoft Dynamics 365 Tümleştirmesi ile eşitleme](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Field Service ile tümleştirme, stok ve proje bilgisi dahil.

Saha teknisyenlerine, Supply Chain Management'tan stok bilgisi hakkında içgörü vermeye odaklı bu ikinci aşamadaki ek işlev, onların stok düzeylerini güncelleştirmelerine ve malzeme aktarmaları yapmalarına olanak tanır. Ek olarak, satılan malların kurulumunu yapan veya hizmet veren şirketleri, daha iyi kontrol ve tam satışa ve projelerle tümleştirmeye daha iyi görünürlük sahibi olacaklardır.

### <a name="functionality-includes-integration-of"></a>İşlev şunların tümleştirmesini içerir:
- Ambar bilgisi
- Eldeki stok bilgileri
- Stok transferleri
- Stok düzeltmeleri
- Dynamics 365 Field Service iş emirleriyle bağlantılı Supply Chain Management projeleri
- Supply Chain Management projeleri ile bağlantıya sahip Dynamics 365 Field Service iş emirleri, bu proje numarasını satış siparişlerine proje içinden faturalamasına izin vermek için uygular. 

![Supply Chain Management ile Field Service arasında iş süreçlerini eşitleme](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Field Service ile Supply Chain Management arasındaki tümleştirmenin ikinci aşaması aşağıdaki şablonların eşitlenmesini sağlar:
- Ambarlar (Supply Chain Management'tan Field Service'a) - Supply Chain Management'tan Field Service'a Ambarlar [Gelişmiş Sorgu] 
- Ürün Stoğu (Supply Chain Management'tan Field Service'a) - Supply Chain Management'tan Field Service'a stok düzeyinde bilgiler [Gelişmiş Sorgu] 
- Stok Düzenleme (Field Service'tan Supply Chain Management'a) - Field Service'tan Supply Chain Management'a stok düzenlemeleri [Gelişmiş Sorgu] 
- Stok Transferleri (Field Service'tan Supply Chain Management'a) - Field Service'tan Supply Chain Management'a stok transferleri [Gelişmiş Sorgu] 
- Projeler (Supply Chain Management'tan Field Service'a) - Supply Chain Management'tan Field Service'a Proje listesi 
- Proje ile İş Emirleri (Field Service'tan Supply Chain Management'a) - Field Service'taki iş emirlerinden Supply Chain Management'taki Satış siparişlerine , Proje desteği ile [Gelişmiş Sorgu] 
- Stok birimi ile Field Service Ürünleri (Supply Chain Management'tan Sales'a) -Supply Chain Management 'Satılabilir serbest bırakılmış ürünler'den Field Service için Sales 'Ürünlerine', Stok birimi dahil 

## <a name="system-requirements"></a>Sistem gereksinimleri

### <a name="system-requirements-for-supply-chain-management"></a>Supply Chain Management için sistem gereksinimleri
Field Service tümleştirmesi aşağıdaki sürümleri destekler:

- Dynamics 365 for Finance and Operations sürüm 8.1.2 (Aralık 2018), Aralık 2018'da yayımlanmıştır ve uygulama yapı numarası 8.1.195 Platform güncelleştirmesi 22'ye (7.0.5095) sahiptir. 

### <a name="system-requirements-for-field-service"></a>Field Service için sistem gereksinimleri
Field Service tümleştirme çözümünü kullanmak için aşağıdaki bileşenleri yüklemeniz gerekir:

- Field Service (sürüm 8.2.0.286) veya sonraki sürüm Dynamics 365 9.1.x üzerinde - Kasım 2018'de yayımlandı
- Dynamics 365, sürüm 1.15.0.1 veya üstü sürüm için Müşteri Adayından Nakde (P2C) çözümü. Çözüm [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3) üzerinden indirilebilir.
- 'Field Service Tümleştirmesi, Proje ve Stok' çözümü, Dynamics 365, sürüm 2.0.0.0 veya sonraki bir sürüm için. Çözüm [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2) üzerinden indirilebilir.
